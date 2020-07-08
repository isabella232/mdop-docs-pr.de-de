---
title: Informationen zu Microsoft Application Virtualization 4.6SP2
description: Informationen zu Microsoft Application Virtualization 4.6SP2
author: dansimp
ms.assetid: 1429e314-9c38-472b-8687-3bed6cf0015c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 16303380782a086cfd750c7a8b2f99bf4f4c8b5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808139"
---
# Informationen zu Microsoft Application Virtualization 4.6SP2


Microsoft Application Virtualization (App-V) 4.6 SP2 bietet verschiedene Verbesserungen und neue Features, die in diesem Thema beschrieben werden.

**Vorsicht**  In diesem Thema wird beschrieben, wie Sie die Windows-Registrierung mit dem Registrierungs-Editor ändern. Wenn Sie die Windows-Registrierung falsch ändern, können Sie zu schwerwiegenden Problemen führen, bei denen Sie möglicherweise eine Neuinstallation von Windows erforderlich machen. Bevor Sie die Registrierung ändern, sollten Sie eine Sicherungskopie der Registrierungsdateien (System. dat und User. dat) erstellen. Microsoft kann nicht garantieren, dass die Probleme, die beim Ändern der Registrierung auftreten, behoben werden können. Ändern Sie die Registrierung auf Ihr eigenes Risiko.

 

**Unterstützung für Windows 8 und Windows Server 2012**

App-v 4.6 SP2 bietet Unterstützung für Windows 8-und Windows Server 2012-Remote Desktop Dienste.

**Unterstützung für die Koexistenz mit App-V 5,0-Client**

App-v 4.6 SP2 bietet Unterstützung für die Koexistenz mit dem Microsoft Application Virtualization 5,0-Client. Lesen Sie die APP-v 5,0-Dokumentation, um Anweisungen zum Konfigurieren des App-v 5,0-Clients für die Koexistenz mit dem App-v 4.6 SP2-Client zu erhalten. Weitere Informationen zu App-V 5,0 finden Sie unter [Application Virtualization 5](https://go.microsoft.com/fwlink/?LinkId=267599) auf TechNet.

**Möglichkeit zum Virtualisieren von Adobe Reader X mit dem geschützten Modus**

Mit den folgenden Verfahren können Sie Adobe Reader X mit aktiviertem Feature für geschützten Modus virtualisieren. Zuvor mussten Sie den geschützten Modus deaktivieren, um Adobe Reader X zu virtualisieren.

Bevor Sie den App-V-Sequencer starten, erstellen Sie den folgenden Registrierungswert unter HKEY \ _LOCAL \ _MACHINE Verzeichnis \\software \\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides:

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Name</p></td>
<td align="left"><p>Typ</p></td>
<td align="left"><p>Daten</p></td>
<td align="left"><p>Beschreibung</p></td>
</tr>
<tr class="even">
<td align="left"><p>EnableVFSPassthrough</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>1</p></td>
<td align="left"><p>Legen Sie diesen Wert auf 1, um <strong> </strong> Adobe Reader X im geschützten Modus während der Startphase zu starten.</p></td>
</tr>
</tbody>
</table>

 

**Hinweis**  Erstellen Sie auf einem Computer, auf dem ein 64-Bit-Betriebssystem ausgeführt wird, den Registrierungswert unter HKEY \ _LOCAL \ _MACHINE \\software\\wow6432node\\microsoft\\softgrid\\4.5\\systemguard\\overrides.

 

Fügen Sie für jede OSD-Datei in Ihrem Adobe Reader X-Paket die folgenden Elemente unter dem &lt; Richtlinien &gt; Element hinzu:

`<VIRTUAL_FILE_SYSTEM_PASS_THROUGH>TRUE</VIRTUAL_FILE_SYSTEM_PASS_THROUGH>`

`<VIRTUAL_REGISTRY_PASS_THROUGH>TRUE</VIRTUAL_REGISTRY_PASS_THROUGH>`

`<ENFORCE_ACLS_ON_VREG_MODIFY>TRUE</ENFORCE_ACLS_ON_VREG_MODIFY>`

**Befehlszeilenparameter für neuen Sequenzer**

Wenn Sie einen Paket Beschleuniger (PA) über die Sequencer-GUI erstellen, können Sie eine RTF-oder txt-Datei auswählen, die dem Administrator, der den Paket Beschleuniger anwendet, Verpackungs-und Bereitstellungsanleitungen zur Verfügung stellt. Diese Funktionalität steht nun über die Sequencer-CLI zur Verfügung.

`/ACCELERATORDESCRIPTIONFILE:PathToDescriptionFile`

Geben Sie einen Pfad zu einer RTF-oder txt-Datei an, die beim Erstellen eines Paket Beschleunigers Verpackungs-und Bereitstellungsanleitungen bereitstellt.

**Die Microsoft-Anwendungsfehler Berichterstattung muss nicht mehr installiert werden**

Wenn Sie den App-v 4.6 SP2-Client mithilfe von setup.msi installieren, müssen Sie die Microsoft-Anwendungsfehler Berichterstattung (dw20shared.msi) nicht mehr installieren. App-v 4.6 SP2 verwendet jetzt die Microsoft-Fehlerberichterstattung. Weitere Informationen finden Sie unter [so wird es gemacht: Installieren des App-V-Clients mithilfe von Setup.msi](https://go.microsoft.com/fwlink/?LinkId=267237).

**Kundenfeedback und Hotfix-Rollup**

App-v 4.6 SP2 enthält ein Rollup von Korrekturen, um Probleme zu beheben, die seit der APP-v 4,6 SP1-Version gefunden wurden. App-v 4.6 SP2 enthält die neuesten Fixes bis einschließlich Microsoft Application Virtualization 4,6 SP1 Hotfix 6.

## Inhalt dieses Abschnitts


<a href="" id="app-v-4-6-sp2-release-notes"></a>[App-V 4.6 SP2 – Versionshinweise](https://go.microsoft.com/fwlink/?LinkId=267600)  
Bietet die aktuellsten Informationen zu bekannten Problemen mit App-v 4.6 SP2.

 

 





