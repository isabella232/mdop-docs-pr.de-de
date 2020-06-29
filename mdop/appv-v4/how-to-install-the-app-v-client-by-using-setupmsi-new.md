---
title: So installieren Sie App-V-Client mit Setup.msi
description: So installieren Sie App-V-Client mit Setup.msi
author: dansimp
ms.assetid: 7221f384-36d6-409a-94a2-86f54fd75322
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb3a145a6c57cccbae3f4e6b191b89d93278ff8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807064"
---
# So installieren Sie App-V-Client mit Setup.msi


In diesem Thema wird beschrieben, wie Sie den App-V-Client mit dem setup.msi-Programm installieren. Bevor Sie den App-V-Client mit dem setup.msi-Programm installieren, müssen Sie zunächst ermitteln, ob eine erforderliche Software installiert werden muss, und Sie müssen Sie installieren. Informationen zum Installieren der erforderlichen Software finden Sie im Abschnitt [Installieren der erforderlichen Software](#prereq-sw) in diesem Thema. Informationen zum Installieren der Client Software finden Sie unter [Installieren des App-V-Clients im Abschnitt Setup.msi Programm](#msi-setup) in diesem Thema.

## <a href="" id="prereq-sw"></a>Installieren der erforderlichen Software


Mit den folgenden Verfahren können Sie die erforderliche Software installieren. Sie können eine Befehlsdatei erstellen und die Befehle an der Eingabeaufforderung ausführen, oder Sie können eine Skriptsprache wie VBScript oder Windows PowerShell verwenden, um die Befehle auszuführen.

**Hinweis**  Für x86-und x64-Versionen des App-V-Clients sind die x86-Versionen der folgenden Software erforderlich.

 

**So installieren Sie Microsoft VisualC + + 2005SP1 Redistributable Package (x86)**

1. Laden Sie das [Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)-](https://go.microsoft.com/fwlink/?LinkId=119961) Softwarepaket aus dem Microsoft Download Center ( <https://go.microsoft.com/fwlink/?LinkId=119961> ) herunter. \ [Vorlagen Tokenwert \] für Version 4,5 SP2 und höher des App-V-Clients laden Sie vcredist\_x86.exe aus dem [Microsoft Visual C++ 2005 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=169360) verteilbaren Paket ATL-Sicherheits Update herunter ( https://go.microsoft.com/fwlink/?LinkId=169360).\ [Vorlagen Tokenwert \]

2. Verwenden Sie zum unbeaufsichtigten installieren die Befehlszeilenoption "/q" mit vcredist\_x86.exe, beispielsweise **vcredist\_x86.exe/q**.

3. Wenn Sie die Software mithilfe der vcredist\_x86.msi-Datei installieren möchten, verwenden Sie die Befehlszeilenoption "/c/t: &lt; fullpathtofolder &gt; ", um die Dateien vcredist.msi und vcredis1.cab aus vcredist\_x86.exe in einen temporären Ordner zu extrahieren. Verwenden Sie zum unbeaufsichtigten installieren die Befehlszeilenoption/quiet – beispielsweise **msiexec/i vcredist.msi** /quiet.

### So installieren Sie Microsoft VisualC + + 2008SP1 Redistributable Package (x86)

**Wichtig**  Für Version 4.6 und höher des App-V-Clients müssen Sie auch das ATL-Sicherheits Update "Microsoft Visual C++ 2008 Service Pack 1 Redistributable Package" installieren.

 

****

1.  Laden Sie das [Microsoft Visual C++ 2008 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=150700) -Softwarepaket aus dem Microsoft Download Center ( https://go.microsoft.com/fwlink/?LinkId=150700) .

2.  Verwenden Sie zum unbeaufsichtigten installieren die Befehlszeilenoption "/q" mit vcredist\_x86.exe, beispielsweise **vcredist\_x86.exe/q**.

### So installieren Sie Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)

****

1.  Herunterladen des [Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) -Softwarepakets aus dem Microsoft Download Center ( https://go.microsoft.com/fwlink/?LinkId=63266) .

2.  Verwenden Sie zum unbeaufsichtigten installieren die Befehlszeilenoption/quiet, beispielsweise **msiexec/i msxml6\_x86.msi/quiet**.

### So installieren Sie die Microsoft-Anwendungsfehler Berichterstattung

Wenn Sie die Microsoft-Anwendungsfehler Berichterstattung installieren, müssen Sie den *AppGUID* -Parameter verwenden, um den App-V-Produktcode anzugeben. Der Produktcode ist für jeden App-V-Clienttyp und jede Version eindeutig. Wählen Sie den richtigen Produktcode aus der folgenden Tabelle aus.

**Wichtig**  Für App-v 4.6 SP2 und höher müssen Sie die Microsoft-Anwendungsfehler Berichterstattung (dw20shared.msi) nicht mehr installieren. App-V verwendet jetzt die Microsoft-Fehlerberichterstattung.

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Version</th>
<th align="left">Produkt Code für den Desktop Client</th>
<th align="left">Produkt Code für Client für Remote Desktop Dienste</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 4,5 CU1</p></td>
<td align="left"><p>FE495DBC-6D42-4698-B61F-86E655E0796D</p></td>
<td align="left"><p>8A97C241-D92A-47DC-B360-E716C1AAA929</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,5 SP1</p></td>
<td align="left"><p>93468B43-C19D-44F9-8BCC-114076DB0443</p></td>
<td align="left"><p>0042AD3C-99A4-4E58-B5F0-744D5AD96E1C</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,5 SP2</p></td>
<td align="left"><p>C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D</p></td>
<td align="left"><p>ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 x86</p></td>
<td align="left"><p>9E9D30B2-2065-4FDE-B756-8F1A6EABAFC3</p></td>
<td align="left"><p>439FAC21-B423-41D4-8126-54F9FCB70039</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,6 x64</p></td>
<td align="left"><p>E569E45F-7BA6-4C7F-B6BA-3FFCBE92FC22</p></td>
<td align="left"><p>D2977C18-D88A-47CB-AFD8-652DD36F4D0D</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 x86 ¹</p></td>
<td align="left"><p>40C3258B-F9D1-46DF-AE97-72C1F86F2427</p></td>
<td align="left"><p>9915D911-CC73-4122-AF4F-564F89454655</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,6 x64 ¹</p></td>
<td align="left"><p>1650E31F-23B8-40B5-A60A-C5934F557E3B</p></td>
<td align="left"><p>7580D918-C621-49E7-9877-3CC59F9BD1DA</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 x86 SP1</p></td>
<td align="left"><p>DB9F70CD-29BC-480B-8BA2-C9C2232C4553</p></td>
<td align="left"><p>1354855A-2298-4C73-9022-EF0686C65991</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,6 x64 SP1</p></td>
<td align="left"><p>342C9BB8-65A0-46DE-AB7A-8031E151AF69</p></td>
<td align="left"><p>B2C6C8D5-FE76-4056-A326-EE5D633EA175</p></td>
</tr>
</tbody>
</table>

 

¹ App-V "Sprachen"-Version.

**Hinweis**  Wenn Sie den Produktcode finden müssen, können Sie den Orca.exe-Datenbankeditor oder ein ähnliches Tool verwenden, um Windows Installer-Dateien zu untersuchen, um den Wert der *ProductCode* -Eigenschaft zu finden. Weitere Informationen zum Verwenden von Orca.exe finden Sie unter [Windows Installer-Entwicklungs Tools](https://go.microsoft.com/fwlink/?LinkId=150008) ( https://go.microsoft.com/fwlink/?LinkId=150008) .

 

****

1.  Suchen Sie das Installationsprogramm für die Microsoft-Anwendungsfehler Berichterstattung dw20shared.msi, das im Ordner **Support\\Watson** auf dem Veröffentlichungsmedium zu finden ist.

2.  Führen Sie den folgenden Befehl aus, um die Software zu installieren:

         **msiexec /i dw20shared.msi APPGUID={valuefromtable} REBOOT=Suppress REINSTALL=ALL REINSTALLMODE=vomus**

## <a href="" id="msi-setup"></a>Installieren des App-V-Clients mithilfe des Setup.msi-Programms


Gehen Sie wie folgt vor, um den App-V-Client zu installieren. Stellen Sie sicher, dass alle erforderlichen Softwarekomponenten installiert wurden. \ [Vorlagen Tokenwert \] für Version 4.6 und höher des App-V-Clients überprüft das setup.msi-Programm das System, und wenn die erforderliche Software nicht installiert ist, wird eine Fehlermeldung mit dem Hinweis angezeigt, dass die Installation nicht fortgesetzt werden kann. \ [Vorlage-Tokenwert \]

**So installieren Sie den Application Virtualization-Client mithilfe von Setup.msi**

1.  Stellen Sie sicher, dass Sie mit einem Konto angemeldet sind, das über Administratorrechte auf dem Computer verfügt.

2.  Öffnen Sie ein Eingabeaufforderungsfenster, indem Sie erhöhte Rechte verwenden, und ändern Sie dann das Verzeichnis in den Ordner, in dem die Setupdateien enthalten sind. Wenn Sie Version 4.6 oder eine neuere Version des App-V-Clients installieren, müssen Sie das richtige Installationsprogramm für das Betriebssystem des Computers, 32-Bit oder 64-Bit verwenden. Bei der Installation tritt ein Fehler auf, und es wird eine Fehlermeldung angezeigt, wenn Sie das falsche Installationsprogramm verwenden.

3.  Geben Sie die Befehlszeichenfolge für den Installationsbefehl an der Eingabeaufforderung ein. Alternativ können Sie eine Befehlsdatei erstellen und diese über die Eingabeaufforderung ausführen. Sie können auch eine Skriptsprache wie VBScript oder Windows PowerShell verwenden, um den Befehl auszuführen.

4.  Das folgende Befehlszeilenbeispiel zeigt, wie setup.msi mit einer Reihe optionaler Parameter verwendet werden kann. Weitere Informationen zu diesen Parametern finden Sie unter [Befehlszeilenparameter für Application Virtualization Client Installer](application-virtualization-client-installer-command-line-parameters.md).

    **msiexec.exe/i "setup.msi" SWICACHESIZE = "10240" SWIPUBSVRDISPLAY = "Production System" SWIPUBSVRTYPE = "http/Secure" SWIPUBSVRHOST = "PRODSYS" SWIPUBSVRPORT = "443" SWIPUBSVRPATH = "/AppVirt/appsntype.xml" SWIPUBSVRREFRESH = "SWIGLOBALDATA =" D:\\AppVirt\\Global "SWIUSERDATA =" ^% LocalAppData ^%\\Windows\\Application Virtualization Client "SWIFSDRIVE =" S "/q**

    **Wichtig**  
    -   Der Windows Installer-Schalter "**/q**" wird verwendet, um dies zu einer unbeaufsichtigten Installation zu machen.

    -   Dem "" " **%** -Zeichen in"**% HOMEDRIVE%**"muss das Escapezeichen" "vorangestellt werden **^** . Andernfalls legt die Windows-Befehlsshell den Wert auf den Wert des Benutzers fest, der die Installation ausführt.

    -   Um die Installationsprotokollierung zu aktivieren, verwenden Sie den msiexec-Schalter **/l\ * v filename. log**.

     

## Verwandte Themen


[So installieren Sie den Client über die Befehlszeile](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





