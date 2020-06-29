---
title: Migrieren zu App-V 5.1 von einer früheren Version
description: Migrieren zu App-V 5.1 von einer früheren Version
author: dansimp
ms.assetid: e7ee0edc-7544-4c0a-aaca-d922a33bc1bb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb6ddbfed4f6fd1ae9613d2ee86361a51918a65
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805063"
---
# Migrieren zu App-V 5.1 von einer früheren Version


Mit Microsoft Application Virtualization (app-v) 5,1 können Sie Ihre vorhandene App-v 4,6-oder App-v 5,0-Infrastruktur auf die flexiblere, integrierte und einfacher zu verwaltende App-v 5,1-Infrastruktur migrieren.
Sie können jedoch nicht direkt von App-v 4. x zu app-v 5,1 migrieren, sondern müssen zuerst zu app-v 5,0 migrieren. Weitere Informationen zum Migrieren von App-v 4. x zu app-v 5,0 finden Sie unter [Migrieren von einer früheren Version](migrating-from-a-previous-version-app-v-50.md) .  

**Hinweis**  App-v 5,1-Pakete sind genauso wie App-v 5,0-Pakete. Es wurde keine Änderung des Paketformats zwischen den Versionen vorgenommen, und daher ist es nicht erforderlich, App-v 5,0-Pakete in App-v 5,1-Pakete zu konvertieren.

Weitere Informationen zu den Unterschieden zwischen App-v 4,6 und App-v 5,1 finden Sie unter **Unterschiede zwischen App-v 4,6 und App-v 5,0 im Abschnitt** [über APP-v 5,0](about-app-v-50.md).

 

## <a href="" id="bkmk-pkgconvimprove"></a>Verbesserungen des App-V 5,1-Paket Konverters


Sie können jetzt den Paket Konverter verwenden, um App-V 4,6-Pakete zu konvertieren, die Skripts enthalten, und Registrierungsinformationen und Skripts aus den Dateien des Quell-OSD sind jetzt in der Ausgabe des Paket Konverters enthalten.

Sie können auch den `–OSDsToIncludeInPackage` Parameter mit dem `ConvertFrom-AppvLegacyPackage` Cmdlet verwenden, um anzugeben, welche OSD-Dateiinformationen konvertiert und in das neue Paket gestellt werden.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Neu in App-V 5,1</th>
<th align="left">Vor App-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Neue XML-Dateien werden entsprechend den OSD-Dateien erstellt, die einem Paket zugeordnet sind. Diese Dateien umfassen die folgenden Informationen:</p>
<ul>
<li><p>Umgebungsvariablen</p></li>
<li><p>Kombinationen</p></li>
<li><p>Dateitypzuordnungen</p></li>
<li><p>Registrierungsinformationen</p></li>
<li><p>Skripts</p></li>
</ul>
<p>Sie können jetzt mithilfe des Parameters auswählen, dass Informationen aus einer Teilmenge der OSD-Dateien im Quellverzeichnis zum Paket hinzugefügt werden sollen <code>-OSDsToIncludeInPackage</code> .</p></td>
<td align="left"><p>Registrierungsinformationen und Skripts, die in OSD-Dateien enthalten sind, die einem Paket zugeordnet sind, wurden in der Paket Konverter-Ausgabe nicht berücksichtigt.</p>
<p>Der Paket Konverter füllt das neue Paket mit Informationen aus allen OSD-Dateien im Quellverzeichnis auf.</p></td>
</tr>
</tbody>
</table>

 

### Beispiel für eine Konvertierungsanweisung

Wenn Sie den neuen Prozess verstehen möchten, lesen Sie die folgende Beispiel `ConvertFrom-AppvLegacyPackage` Paket Konverter-Anweisung.

**Wenn das Quellverzeichnis (\\\\OldPkgStore\\ContosoApp) Folgendes enthält:**

-   ContosoApp. SFT

-   ContosoApp.msi

-   ContosoApp. SPRJ

-   ContosoApp\_manifest.xml

-   X. OSD

-   Y. OSD

-   Z. OSD

**Und führen Sie diesen Befehl aus:**

``` syntax
ConvertFrom-AppvLegacyPackage –SourcePath \\OldPkgStore\ContosoApp\ 
-DestinationPath \\NewPkgStore\ContosoApp\
-OSDsToIncludeInPackage X.osd,Y.osd
```

**Im Zielverzeichnis (\\\\NewPkgStore\\ContosoApp) wird Folgendes erstellt:**

-   ContosoApp. AppV

-   ContosoApp.msi

-   ContosoApp\_DeploymentConfig.xml

-   ContosoApp\_UserConfig.xml

-   X\_Config.xml

-   Y\_Config.xml

-   Z\_Config.xml

**Im obigen Beispiel:**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Diese Quellverzeichnis Dateien...</th>
<th align="left">... werden in diese Zielverzeichnis Dateien konvertiert...</th>
<th align="left">... und enthält die folgenden Elemente</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p>X. OSD</p></li>
<li><p>Y. OSD</p></li>
<li><p>Z. OSD</p></li>
</ul></td>
<td align="left"><ul>
<li><p>X_Config.xml</p></li>
<li><p>Y_Config.xml</p></li>
<li><p>Z_Config.xml</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Umgebungsvariablen</p></li>
<li><p>Kombinationen</p></li>
<li><p>Dateitypzuordnungen</p></li>
<li><p>Registrierungsinformationen</p></li>
<li><p>Skripts</p></li>
</ul></td>
<td align="left"><p>Jede OSD-Datei wird in eine separate, entsprechende XML-Datei konvertiert, die die Elemente enthält, die hier im App-V 5,1-Bereitstellungs Konfigurationsformat aufgelistet sind. Diese Elemente können dann aus diesen XML-Dateien kopiert und wie gewünscht in die Bereitstellungskonfiguration oder die Benutzerkonfigurationsdateien eingefügt werden.</p>
<p>In diesem Beispiel gibt es drei XML-Dateien, die den drei OSD-Dateien im Quellverzeichnis entsprechen. Jede XML-Datei enthält die Umgebungsvariablen, Verknüpfungen, Dateitypen Zuordnungen, Registrierungsinformationen und Skripts in der entsprechenden OSD-Datei.</p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p>X. OSD</p></li>
<li><p>Y. OSD</p></li>
</ul></td>
<td align="left"><ul>
<li><p>ContosoApp. AppV</p></li>
<li><p>ContosoApp_DeploymentConfig.xml</p></li>
<li><p>ContosoApp_UserConfig.xml</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Umgebungsvariablen</p></li>
<li><p>Kombinationen</p></li>
<li><p>Dateitypzuordnungen</p></li>
</ul></td>
<td align="left"><p>Die Informationen aus den im Parameter angegebenen OSD-Dateien <code>-OSDsToIncludeInPackage</code> werden konvertiert und innerhalb des Pakets gespeichert. Der Konverter füllt dann die Konfigurationsdatei für die Bereitstellung und die Benutzerkonfigurationsdatei mit dem Inhalt des Pakets auf, ebenso wie App-V Sequencer beim Sequenzieren eines neuen Pakets.</p>
<p>In diesem Beispiel wurden Umgebungsvariablen, Verknüpfungen und Dateitypzuordnungen, die in X. OSD und Y. OSD enthalten sind, konvertiert und in das App-V-Paket eingefügt, und einige dieser Informationen wurden auch in die Bereitstellungskonfiguration und die Konfigurationsdateien der Benutzer aufgenommen. X. OSD und Y. OSD wurden verwendet, weil Sie als Argumente für den Parameter hinzugefügt wurden <code>-OSDsToIncludeInPackage</code> . Im Paket sind keine Informationen von Z. OSD enthalten, da es nicht als eines dieser Argumente enthalten war.</p></td>
</tr>
</tbody>
</table>

 

## Konvertieren von Paketen, die mit einer früheren Version von App-V erstellt wurden


Verwenden Sie das Paket Konverter-Dienstprogramm, um virtuelle Anwendungspakete zu aktualisieren, die mit den Versionen von App-v vor App-v 5,0 erstellt wurden. Der Paket Konverter verwendet PowerShell zum Konvertieren von Paketen und kann die Automatisierung des Prozesses unterstützen, wenn viele Pakete vorhanden sind, für die eine Konvertierung erforderlich ist.

**Wichtig**  Nachdem Sie ein vorhandenes Paket konvertiert haben, sollten Sie das Paket vor der Bereitstellung des Pakets testen, um sicherzustellen, dass der Konvertierungsvorgang erfolgreich war.

 

**Was Sie wissen müssen, bevor Sie vorhandene Pakete konvertieren**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Problem</th>
<th align="left">Problemumgehung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Virtuelle Pakete, die DSC verwenden, werden nach der Konvertierung nicht verknüpft.</p></td>
<td align="left"><p>Verknüpfen Sie die Pakete mithilfe von Verbindungsgruppen. Siehe <a href="managing-connection-groups51.md" data-raw-source="[Managing Connection Groups](managing-connection-groups51.md)"> Verwalten von Verbindungsgruppen </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Während der Konvertierung werden Umgebungsvariablen Konflikte erkannt.</p></td>
<td align="left"><p>Beheben Sie alle Konflikte in der zugehörigen <strong> OSD- </strong> Datei.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Während der Konvertierung werden hart codierte Pfade erkannt.</p></td>
<td align="left"><p>Hart codierte Pfade sind schwierig, richtig zu konvertieren. Der Paket Konverter erkennt Pakete mit Dateien, die hart codierte Pfade enthalten, und gibt diese zurück. Zeigen Sie die Datei mit dem hartcodierten Pfad an, und ermitteln Sie, ob das Paket die Datei erfordert. Wenn dies der Fall ist, empfiehlt es sich, das Paket neu zu sequenzieren.</p></td>
</tr>
</tbody>
</table>

 

Beim Konvertieren einer Paketprüfung auf fehlerhafte Dateien oder Verknüpfungen. Suchen Sie das Element in App-V 4,6-Paket. Möglicherweise handelt es sich um einen hartcodierten Pfad. Konvertieren Sie den Pfad.

**Hinweis**  Es wird empfohlen, den App-V 5,1-Sequenzer zum Konvertieren kritischer Anwendungen oder Anwendungen zu verwenden, die Features nutzen müssen. Lesen Sie, [wie Sie eine neue Anwendung mit App-V 5,1 Sequenzieren](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md).

Wenn ein konvertiertes Paket nicht geöffnet wird, nachdem Sie es konvertiert haben, empfiehlt es sich auch, die Anwendung mithilfe des App-V 5,1-Sequencers neu zu sequenzieren.

 

[So konvertieren Sie ein Paket, das in einer früheren Version von App-V erstellt wurde](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

## Migrieren von Clients


In der folgenden Tabelle wird die empfohlene Methode zum Aktualisieren von Clients angezeigt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabe</th>
<th align="left">Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aktualisieren Ihrer Umgebung auf die neueste Version von App-v 4.6</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Überlegungen zur Implementierung und zum Upgrade von Application Virtualization </a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Installieren Sie den App-V 5,1-Client mit aktivierter Koexistenz.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)">Bereitstellen der APP-v 4,6 und des App-v 5,1-Clients auf </a> demselben Computer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sequenzieren und Rollout von App-V 5,1-Paketen. Bei Bedarf können Sie die Veröffentlichung von App-V 4,6-Paketen aufheben.</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md)">So wird es gemacht: Sequenzierung einer neuen Anwendung mit APP- </a> V 5,1</p></td>
</tr>
</tbody>
</table>

 

**Wichtig**  Sie müssen die neueste Version von App-v 4.6 ausführen, um den Koexistenzmodus verwenden zu können. Wenn Sie ein Paket sequenzieren, müssen Sie außerdem die Einstellung für die Verwaltungsautorität konfigurieren, die sich in der **Benutzerkonfiguration** befindet, die sich im Abschnitt **Benutzerkonfiguration** befindet.

 

## Migrieren der vollständigen Infrastruktur des App-V 5,1-Servers


Es gibt keine direkte Methode zum Upgrade auf eine vollständige App-V 5,1-Infrastruktur. Verwenden Sie die Informationen im folgenden Abschnitt, um Informationen zum Upgrade des App-V-Servers zu erhalten.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabe</th>
<th align="left">Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aktualisieren Sie Ihre Umgebung auf die neueste Version von App-v 4.6.</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Überlegungen zur Implementierung und zum Upgrade von Application Virtualization </a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Bereitstellen der App-V 5,1-Version des Clients</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-51gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md)">Bereitstellen des App-V </a> -Clients</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Installieren Sie den App-V 5,1-Server.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)">Bereitstellen des App-V 5,1 </a> -Servers</p></td>
</tr>
<tr class="even">
<td align="left"><p>Migrieren vorhandener Pakete</p></td>
<td align="left"><p>Weitere Informationen finden Sie unter <strong> Konvertieren von Paketen, die mit einer früheren Version von App-V </strong> in diesem Artikel erstellt wurden.</p></td>
</tr>
</tbody>
</table>

 

## Zusätzliche Migrationsaufgaben


Sie können auch zusätzliche Migrationsaufgaben wie die Neukonfiguration von Endpunkten und das Öffnen eines Pakets ausführen, das mit einer früheren Version auf einem Computer mit dem App-V 5,1-Client erstellt wurde. Die folgenden Links enthalten weitere Informationen zum Ausführen dieser Aufgaben.

[So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu einem konvertierten App-V 5.1-Paket für alle Benutzer eines bestimmten Computers](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

[So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu App-V 5.1 für einen bestimmten Benutzer](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

[So setzen Sie Erweiterungspunkte von einem App-V 5.1-Paket auf ein App-V 4.6-Paket für alle Benutzer eines bestimmten Computers zurück](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[So setzen Sie Erweiterungspunkte von einem App-V 5.1-Paket auf ein App-V 4.6-Paket für einen bestimmten Benutzer zurück](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)







## Weitere Ressourcen für die Ausführung von App-V-Migrationsaufgaben


[Vorgänge für App-V 5.1](operations-for-app-v-51.md)

[Ein vereinfachtes Upgrade-Verfahren für Microsoft App-V 5,1-Verwaltungs Server](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





