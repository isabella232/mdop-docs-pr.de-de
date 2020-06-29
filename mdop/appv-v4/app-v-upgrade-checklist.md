---
title: Upgrade-Prüfliste für App-V
description: Upgrade-Prüfliste für App-V
author: dansimp
ms.assetid: 64e317d2-d260-4b67-8a49-ba9ac513087a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad856ce3067c327f3e604f9269ee384a66a1675a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808027"
---
# Upgrade-Prüfliste für App-V


Bevor Sie versuchen, auf Microsoft Application Virtualization (app-v) 4,5 oder höhere Versionen zu aktualisieren, muss jede frühere Version als App-v 4,1 auf App-v 4,1 aktualisiert werden. Sie sollten zunächst planen, Clients zu aktualisieren und dann die Server Komponenten zu aktualisieren. App-v-Clients, die auf App-v 4,5 aktualisiert wurden, arbeiten weiterhin mit App-v-Servern, die noch nicht aktualisiert wurden. Frühere Versionen des Clients werden auf Servern, die auf App-V 4,5 aktualisiert wurden, nicht unterstützt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Schritt</th>
<th align="left">Verweis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aktualisieren Sie die App-V-Clients.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-client.md" data-raw-source="[How to Upgrade the Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)">So aktualisieren Sie Application Virtualization Client</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Aktualisieren Sie die App-V-Server und-Datenbank.</p>
<div class="alert">
<strong>Wichtig</strong><br/><p>Wenn Sie über mehr als einen Serverfreigabe Zugriff auf die App-V-Datenbank verfügen, müssen alle diese Server offline geschaltet werden, während die Datenbank aktualisiert wird. Sie sollten ihre normalen Geschäftsmethoden für die Datenbankaktualisierung befolgen, aber wir empfehlen, dass Sie das Datenbankupgrade mithilfe einer Sicherungskopie der Datenbank zuerst auf einem Testserver testen. Wählen Sie dann einen der Server für das erste Upgrade aus, um das Datenbankschema zu aktualisieren. Nachdem die Produktionsdatenbank erfolgreich aktualisiert wurde, können Sie die App-V-Software auf den anderen Servern aktualisieren.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)">So aktualisieren Sie die Server und Systemkomponenten</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Aktualisieren des App-V-Verwaltungs-Webdiensts</p>
<p>Dieser Schritt gilt nur, wenn sich der Verwaltungs-Web-Service auf einem separaten Server befindet, was erfordert, dass Sie das Serverinstallationsprogramm auf diesem separaten Server ausführen, um den Verwaltungs-Webservice zu aktualisieren. Andernfalls führt der vorherige Server Upgrade-Schritt automatisch zu einem Upgrade des Verwaltungs-Webdiensts.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)">So aktualisieren Sie die Server und Systemkomponenten</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Aktualisieren Sie die App-V-Verwaltungskonsole.</p>
<p>Dieser Schritt gilt nur, wenn sich die Verwaltungskonsole auf einem separaten Computer befindet, was erfordert, dass Sie das Serverinstallationsprogramm auf diesem separaten Computer ausführen, um die Konsole zu aktualisieren. Andernfalls wird der vorherige Server Aktualisierungsschritt die Verwaltungskonsole aktualisieren.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)">So aktualisieren Sie die Server und Systemkomponenten</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Aktualisieren Sie den App-V-Sequenzer.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-sequencer.md" data-raw-source="[How to Upgrade the Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)">So aktualisieren Sie Application Virtualization Sequencer</a></p></td>
</tr>
</tbody>
</table>



## Weitere Überlegungen zu Upgrades


-   Alle virtuellen Anwendungspakete, die in Version 4,2 sequenziert sind, müssen für die Verwendung mit Version 4,5 nicht erneut sequenziert werden. Sie sollten jedoch erwägen, die virtuellen Pakete auf das Microsoft Application Virtualization 4,5-Format zu aktualisieren, wenn Sie standardmäßige Zugriffssteuerungslisten verwenden oder eine Windows Installer-Datei generieren möchten. Dies ist ein einfacher Vorgang und erfordert nur, dass das vorhandene virtuelle Anwendungspaket mit dem App-V 4,5-Sequenzer geöffnet und gespeichert wird. Dies kann mithilfe der Befehlszeilenschnittstelle für die APP-VSequencer automatisiert werden. Weitere Informationen finden Sie unter [erstellen oder Aktualisieren virtueller Anwendungen mit dem App-V-Sequenzer](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md) .

-   Eines der Features des 4,5-Sequenzers ist die Möglichkeit zum Erstellen von Windows Installer-Dateien (MSI) als Kontrollpunkte für die Interoperabilität des virtuellen Anwendungspakets mit ESD-Systemen (Electronic Software Distribution) wie Microsoft Endpoint Configuration Manager. Frühere Windows Installer-Dateien, die mit dem MSI-Tool für Application Virtualization erstellt wurden, die auf einem App-v 4,1-oder 4,2-Client installiert wurden und anschließend auf App-v 4,5 aktualisiert wurden, funktionieren weiterhin, auch wenn Sie nicht auf dem App-v 4,5-Client installiert werden können. Sie können jedoch nur dann entfernt oder aktualisiert werden, wenn Sie im App-V 4,5-Sequenzer aktualisiert wurden. Das ursprüngliche App-v-Paket, das älter als 4,5 ist, muss im App-v 4,5-Sequenzer geöffnet und dann als Windows Installer-Datei gespeichert werden.

    **Hinweis:**  
    Wenn der APP-v 4,2-Client bereits auf App-v 4,5 aktualisiert wurde, ist es möglich, eine Problemumgehung zu erstellen, um die Version 4,2-Pakete auf Version 4,5-Clients beizubehalten und deren Verwaltung zu ermöglichen. Dieses Skript muss zwei Dateien, msvcp71.dll und msvcr71.dll, in den App-V-Installationsordner kopieren und die folgenden Registrierungsschlüsselwerte unter dem Registrierungsschlüssel einrichten: \ [HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\configuration\]:

    "Clientversion" = "4.2.1.20"

    "GlobalDataDirectory" = "C:\\\\Documents und Settings\\\\All Users\\\\Documents\\\\" (ein Global beschreibbarer Speicherort)



-   Windows Installer-Dateien, die vom APP-v 4,5-Sequenzer generiert werden, zeigen die Fehlermeldung "dieses Paket erfordert Microsoft Application Virtualization Client 4,5 oder höher" an, wenn Sie versuchen, Sie auf einem App-v 4,6-Client auszuführen. Öffnen Sie das alte Paket entweder mit dem App-v 4,5 SP1-Sequenzer oder dem App-v 4,6-Sequenzer, und generieren Sie eine neue MSI-Datei für das Paket.

-   Alle Berichte der Version 4,2, die erstellt und gespeichert wurden, werden überschrieben, wenn der Server auf Version 4,5 aktualisiert wird. Wenn Sie diese Berichte behalten müssen, müssen Sie eine Sicherungskopie der "SftMMC. MSC-Datei speichern, die sich im Ordner SoftGrid-Verwaltungskonsole auf dem Server befindet, und diese Kopie verwenden, um das neue" SftMMC. msc zu ersetzen, das während des Upgrades installiert ist.

-   Weitere Informationen zum Upgrade von vorherigen Versionen finden Sie unter [Upgrade auf Microsoft Application Virtualization 4,5 FAQ](https://go.microsoft.com/fwlink/?LinkId=120358) ( https://go.microsoft.com/fwlink/?LinkId=120358) .

## <a href="" id="app-v-4-6-client-package-support-"></a>Unterstützung für App-V 4,6-Client Pakete


Sie können Pakete bereitstellen, die in früheren Versionen von App-v für App-v 4,6-Clients erstellt wurden. Sie müssen jedoch die zugehörige OSD-Datei so ändern, dass Sie die entsprechenden Informationen zum Betriebssystem und zur Chiparchitektur enthält. Die folgenden Werte können verwendet werden:

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem Wert</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>&lt;BS-Wert = "Win2003TS"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;BS-Wert = "Win2003TS64"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;BS-Wert = "Win2008TS"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;BS-Wert = "Win2008TS64"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;BS-Wert = "Win2008R2TS64"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;BS-Wert = "Win7"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;BS-Wert = "Win764"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;BS-Wert = "WinVista"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;BS-Wert = "WinVista64"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;BS-Wert = "WinXP"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;BS-Wert = "WinXP64"/&gt;</p></td>
</tr>
</tbody>
</table>



Wenn Sie ein neu erstelltes 32-Bit-Paket ausführen möchten, müssen Sie die Anwendung auf einem Computer abgleichen, auf dem ein 32-Bit-Betriebssystem ausgeführt wird, wobei der App-V 4,6-Sequencer installiert ist. Nachdem Sie die Anwendung sequenziert haben, klicken Sie in der Sequencer-Konsole auf die Registerkarte **Bereitstellung** , und geben Sie dann die entsprechende Betriebssystem-und Chiparchitektur nach Bedarf an.

**Wichtig**  
Anwendungen, die auf einem Computer mit einem 64-Bit-Betriebssystem sequenziert sind, müssen auf Computern bereitgestellt werden, auf denen ein 64-Bit-Betriebssystem ausgeführt wird. Neue 32-Bit-Pakete, die mit dem App-v 4,6-Sequenzer erstellt wurden, werden auf Computern, auf denen der APP-v 4,5-Client ausgeführt wird, nicht ausgeführt.



Wenn Sie neue 64-Bit-Pakete auf dem App-v 4,6-Client ausführen möchten, müssen Sie die Anwendung auf einem Computer mit dem App-v 4,6-Sequenzer abgleichen, auf dem ein 64-Bit-Betriebssystem ausgeführt wird. Nachdem Sie die Anwendung sequenziert haben, klicken Sie in der Sequencer-Konsole auf die Registerkarte **Bereitstellung** , und geben Sie dann die gewünschte Betriebssystem-und Chiparchitektur an.

In der folgenden Tabelle wird aufgeführt, welche Clientversionen Pakete ausführen, die mit den verschiedenen Versionen des Sequencers erstellt wurden.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Sequenziert mithilfe des App-V 4,2-Sequenzers</th>
<th align="left">Sequenziert mithilfe des App-V 4,5-Sequenzers</th>
<th align="left">Sequenziert mithilfe des 32-Bit-App-V 4,6-Sequenzers</th>
<th align="left">Sequenziert mithilfe des 64-Bit-App-V 4,6-Sequenzers</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>4,2-Client</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Nein</p></td>
<td align="left"><p>Nein</p></td>
<td align="left"><p>Nein</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,5-Client ¹</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Nein</p></td>
<td align="left"><p>Nein</p></td>
</tr>
<tr class="odd">
<td align="left"><p>4,6-Client (32-Bit)</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Nein.</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,6-Client (64-Bit)</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
</tr>
</tbody>
</table>



¹ gilt für alle Versionen des App-v 4,5-Clients, einschließlich APP-v 4,5, App-v 4,5 CU1 und App-v 4,5 SP1.









