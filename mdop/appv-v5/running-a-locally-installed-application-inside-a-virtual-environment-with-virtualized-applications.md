---
title: Ausführen einer lokal installierten Anwendung in einer virtuellen Umgebung mit virtualisierter Anwendungen
description: Ausführen einer lokal installierten Anwendung in einer virtuellen Umgebung mit virtualisierter Anwendungen
author: dansimp
ms.assetid: a8affa46-f1f7-416c-8125-9595cfbfdbc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 10c0f3f3c8a1b88cf1a98fd64fe8f7f49b597a91
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804883"
---
# Ausführen einer lokal installierten Anwendung in einer virtuellen Umgebung mit virtualisierter Anwendungen


Sie können eine lokal installierte Anwendung in einer virtuellen Umgebung neben Anwendungen ausführen, die mit Microsoft Application Virtualization (App-V) virtualisiert wurden. Möglicherweise möchten Sie dies tun, wenn Sie:

-   Sie möchten eine Anwendung lokal auf Clientcomputern installieren und ausführen, möchten aber bestimmte Plug-ins, die mit dieser lokalen Anwendung funktionieren, virtualisieren und ausführen.

-   Behandeln ein App-v-Clientpaket und möchten eine lokale Anwendung in der virtuellen App-v-Umgebung öffnen.

Verwenden Sie eine der folgenden Methoden, um eine lokale Anwendung innerhalb der virtuellen App-V-Umgebung zu öffnen:

-   [RunVirtual-Registrierungsschlüssel](#bkmk-runvirtual-regkey)

-   [Cmdlet "Get-AppvClientPackage PowerShell"](#bkmk-get-appvclientpackage-posh)

-   [Befehlszeilen Schalter/appvpid: &lt; PID&gt;](#bkmk-cl-switch-appvpid)

-   [Befehlszeilen-Hook-Schalter/appvve: &lt; GUID&gt;](#bkmk-cl-hook-switch-appvve)

Jede Methode erfüllt im Wesentlichen dieselbe Aufgabe, aber einige Methoden sind möglicherweise für einige Anwendungen besser geeignet als für andere, je nachdem, ob die virtualisierte Anwendung bereits ausgeführt wird.

## <a href="" id="bkmk-runvirtual-regkey"></a>RunVirtual-Registrierungsschlüssel


Wenn Sie eine lokal installierte Anwendung zu einem Paket oder zur virtuellen Umgebung einer Verbindungsgruppe hinzufügen möchten, fügen Sie dem `RunVirtual` Registrierungsschlüssel im Registrierungs-Editor einen Unterschlüssel hinzu, wie in den folgenden Abschnitten beschrieben.

Es ist keine Gruppenrichtlinieneinstellung verfügbar, um diesen Registrierungsschlüssel zu verwalten, daher müssen Sie System Center Configuration Manager oder ein anderes ESD-System (Electronic Software Distribution) verwenden oder die Registrierung manuell bearbeiten.

### <a href="" id="bkmk-"></a>Unterstützte Methoden zum Veröffentlichen von Paketen bei Verwendung von RunVirtual

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">App-V-Version</th>
<th align="left">Unterstützte Veröffentlichungsmethoden</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 5,0 SP3</p></td>
<td align="left"><p>Global oder für den Benutzer veröffentlicht</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-v 5,0 über APP-v 5,0 SP2</p></td>
<td align="left"><p>Nur global veröffentlicht</p></td>
</tr>
</tbody>
</table>

 

### Schritte zum Erstellen des Unterschlüssels

1.  Erstellen Sie mithilfe der Informationen in der folgenden Tabelle einen neuen Registrierungsschlüssel mit dem Namen der ausführbaren Datei, beispielsweise **MyApp.exe**.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Paket Veröffentlichungsmethode</th>
    <th align="left">Wo soll der Registrierungsschlüssel erstellt werden?</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Global veröffentlicht</p></td>
    <td align="left"><p>HKEY_LOCAL_MACHINE \software\microsoft\appv\client\runvirtual</p>
    <p><strong>Beispiel </strong> : HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Für den Benutzer veröffentlicht</p></td>
    <td align="left"><p>HKEY_CURRENT_USER \software\microsoft\appv\client\runvirtual</p>
    <p><strong>Beispiel </strong> : HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Die Verbindungsgruppe kann Folgendes enthalten:</p>
    <ul>
    <li><p>Pakete, die nur global oder nur für den Benutzer veröffentlicht werden</p></li>
    <li><p>Pakete, die Global und für den Benutzer veröffentlicht werden</p></li>
    </ul></td>
    <td align="left"><p>Entweder HKEY_LOCAL_MACHINE oder HKEY_CURRENT_USER-Taste, aber alle der folgenden Bedingungen müssen erfüllt sein:</p>
    <ul>
    <li><p>Wenn Sie mehrere Pakete in die virtuelle Umgebung einbeziehen möchten, müssen Sie Sie in eine aktivierte Verbindungsgruppe einbeziehen.</p></li>
    <li><p>Erstellen Sie nur einen Unterschlüssel für eines der Pakete in der Verbindungsgruppe. Wenn Sie beispielsweise ein Paket haben, das Global veröffentlicht wird, und ein weiteres Paket, das für den Benutzer veröffentlicht wird, erstellen Sie einen Unterschlüssel für eines der beiden Pakete, aber nicht für beide. Obwohl Sie einen Unterschlüssel nur für eines der Pakete erstellen, sind alle Pakete in der Verbindungsgruppe sowie die lokale Anwendung in der virtuellen Umgebung verfügbar.</p></li>
    <li><p>Der Schlüssel, unter dem Sie den Unterschlüssel erstellen, muss mit der Veröffentlichungsmethode übereinstimmen, die Sie für das Paket verwendet haben.</p>
    <p>Wenn Sie das Paket beispielsweise für den Benutzer veröffentlicht haben, müssen Sie den Unterschlüssel erstellen <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</code> .</p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

     

2.  Setzen Sie den Wert des neuen Registrierungsunterschlüssels auf die Paket-und Versions-Nr des Pakets, wobei die Werte durch einen Unterstrich voneinander getrennt werden.

    **Syntax**: &lt; Paket-Nr &gt; \ _ &lt; Version-Nr&gt;

    **Beispiel**: 4c909996-AFC9-4352-b606-0b74542a09c1 \ _be463724-Oct1-48f1-8604-c4bd7ca92fa

    Die Anwendung im vorherigen Beispiel würde eine Registrierungsexport Datei (reg-Datei) wie die folgende erstellen:

    ``` syntax
    Windows Registry Editor Version 5.00 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual] 
    @="" 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe] 
    @="aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-555555555
    ```

## <a href="" id="bkmk-get-appvclientpackage-posh"></a>Cmdlet "Get-AppvClientPackage PowerShell"


Sie können das Cmdlet **Start-AppVVirtualProcess** verwenden, um den Paketnamen abzurufen und einen Prozess in der virtuellen Umgebung des angegebenen Pakets zu starten. Mit dieser Methode können Sie einen beliebigen Befehl im Kontext eines App-V-Pakets starten, unabhängig davon, ob das Paket gerade ausgeführt wird.

Verwenden Sie die folgende Beispielsyntax, und ersetzen Sie den Namen Ihres Pakets für ** &lt; Paket &gt; **:

`$AppVName = Get-AppvClientPackage <Package>`

`Start-AppvVirtualProcess -AppvClientObject $AppVName cmd.exe`

Wenn Sie den genauen Namen Ihres Pakets nicht kennen, können Sie die Befehlszeile **Get-AppvClientPackage \ * executable\\**verwenden <em> , wobei **Executable </em> * der Name der Anwendung ist, beispielsweise: Get-AppvClientPackage \ * Word \ *.

## <a href="" id="bkmk-cl-switch-appvpid"></a>Befehlszeilen Schalter/appvpid: &lt; PID&gt;


Sie können den **/appvpid: &lt; PID &gt; ** -Schalter auf einen beliebigen Befehl anwenden, wodurch dieser Befehl innerhalb eines virtuellen Prozesses ausgeführt werden kann, den Sie durch Angabe der Prozess-ID (PID) auswählen. Mit dieser Methode wird die neue ausführbare Datei in derselben App-V-Umgebung wie eine ausführbare Datei gestartet, die bereits ausgeführt wird.

Beispiel: `cmd.exe /appvpid:8108`

Um die Prozess-ID (PID) des App-V-Prozesses zu finden, führen Sie den Befehl **tasklist.exe** über eine Eingabeaufforderung mit erhöhten Rechten aus.

## <a href="" id="bkmk-cl-hook-switch-appvve"></a>Befehlszeilen-Hook-Schalter/appvve: &lt; GUID&gt;


Mit dieser Option können Sie einen lokalen Befehl innerhalb der virtuellen Umgebung eines App-V-Pakets ausführen. Im Gegensatz zum **/appvid** -Schalter, in dem die virtuelle Umgebung bereits ausgeführt werden muss, können Sie mit dieser Option die virtuelle Umgebung starten.

Syntax `cmd.exe /appvve:<PACKAGEGUID_VERSIONGUID>`

Beispiel: `cmd.exe /appvve:aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-55555555`

Führen Sie das Cmdlet " **Get-AppvClientPackage** " aus, um die Paket-GUID und die Versions-GUID der Anwendung abzurufen. Verketten Sie den **/appvve** -Schalter mit folgendem:

-   Ein Doppelpunkt

-   Paket-GUID des gewünschten Pakets

-   Ein Unterstrich

-   Versions-ID des gewünschten Pakets

Wenn Sie den genauen Namen Ihres Pakets nicht kennen, verwenden Sie die Befehlszeile **Get-AppvClientPackage \ * executable\\** <em> , wobei **Executable </em> * der Name der Anwendung ist, beispielsweise: Get-AppvClientPackage \ * Word \ *.

Mit dieser Methode können Sie einen beliebigen Befehl im Kontext eines App-V-Pakets starten, unabhängig davon, ob das Paket gerade ausgeführt wird.






## Verwandte Themen


[Technische Referenz zu App-V 5.0](technical-reference-for-app-v-50.md)

 

 





