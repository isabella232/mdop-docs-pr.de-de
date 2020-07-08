---
title: Planen der Migration von früheren Versionen
description: Planen der Migration von früheren Versionen
author: dansimp
ms.assetid: 62967bf1-542f-41b0-838f-c62f3430ac73
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9b239e09da06270b30b401151cf12e817e2cf8d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806503"
---
# Planen der Migration von früheren Versionen


Bevor Sie versuchen, auf Microsoft Application Virtualization 4.5 oder höhere Versionen zu aktualisieren, muss jede Version vor 4.1 auf Version 4.1 aktualisiert werden. Sie sollten zunächst planen, Ihre Clients zu aktualisieren und dann die Server Komponenten zu aktualisieren. Clients, die auf 4.5 aktualisiert wurden, arbeiten weiterhin mit Application Virtualization-Servern, die noch nicht aktualisiert wurden. Frühere Versionen des Clients werden auf Servern, die auf 4.5 aktualisiert wurden, nicht unterstützt. Weitere Informationen zum Aktualisieren der Systemkomponenten finden Sie unter [Überlegungen zur Implementierung und zum Upgrade von Application Virtualization](application-virtualization-deployment-and-upgrade-considerations.md).

Zur Sicherstellungeiner erfolgreichen Migration sollten die Komponenten des Application Virtualization-Systems in der folgenden Reihenfolge aktualisiert werden:

1.  **Microsoft Application Virtualization-Clients.** Eine Schritt-für-Schritt-Anleitung finden Sie unter [Aktualisieren des Application Virtualization-Clients](how-to-upgrade-the-application-virtualization-client.md).

2.  **Microsoft Application Virtualization-Server und-Datenbank** Eine schrittweise Anleitung zum Upgrade finden Sie unter [Aktualisieren der Server und System Komponenten](how-to-upgrade-the-servers-and-system-components.md).

    **Hinweis**  Wenn Sie über mehr als einen Serverfreigabe Zugriff auf die Application Virtualization-Datenbank verfügen, müssen alle diese Server offline geschaltet werden, während die Datenbank aktualisiert wird. Sie sollten ihre normalen Geschäftsmethoden für das Datenbankupgrade befolgen, es empfiehlt sich jedoch, das Datenbankupgrade mithilfe einer Sicherungskopie der Datenbank zuerst auf einem Testserver zu testen. Wählen Sie dann einen der Server für das erste Upgrade aus, um das Datenbankschema zu aktualisieren. Nachdem die Produktionsdatenbank erfolgreich aktualisiert wurde, können Sie die anderen Server aktualisieren.

     

3.  **Microsoft Application Virtualization Management Web Service.** Dieser Schritt gilt nur, wenn sich der Verwaltungs-Web-Service auf einem separaten Server befindet, was erfordert, dass Sie das Serverinstallationsprogramm auf diesem separaten Server ausführen, um den Webdienst zu aktualisieren. Andernfalls führt der vorherige Server Upgrade-Schritt automatisch zu einem Upgrade des Verwaltungs-Webdiensts.

4.  **Microsoft Application Virtualization-Verwaltungskonsole.** Dieser Schritt gilt nur, wenn sich die Verwaltungskonsole auf einem separaten Computer befindet, was erfordert, dass Sie das Serverinstallationsprogramm auf diesem separaten Computer ausführen, um die Konsole zu aktualisieren. Andernfalls wird der vorherige Server Aktualisierungsschritt die Verwaltungskonsole aktualisieren.

5.  **Microsoft Application Virtualization Sequencer.** Schritt-für-Schritt-Anleitungen finden Sie unter so wird es [gemacht: Installieren des Application Virtualization Sequencers](how-to-install-the-application-virtualization-sequencer.md). Alle virtuellen Anwendungspakete, die in Version 4.2 sequenziert sind, müssen nicht für die Verwendung mit Version 4.5 neu sequenziert werden. Sie sollten jedoch das Upgrade der virtuellen Pakete auf das Microsoft Application Virtualization 4.5-Format erwägen, wenn Sie standardmäßige Zugriffssteuerungslisten (Access Control Lists, ACLs) anwenden oder eine Windows Installer-Datei generieren möchten. Dies ist ein einfacher Vorgang und erfordert nur, dass das vorhandene virtuelle Anwendungspaket mit dem 4.5-Sequenzer geöffnet und gespeichert wird. Dies kann mithilfe der Befehlszeilenschnittstelle Application Virtualization Sequencer automatisiert werden.

## <a href="" id="app-v-4-6-client-package-support-"></a>Unterstützung für App-v 4.6-Client Pakete


Sie können Pakete bereitstellen, die in früheren Versionen von App-v für App-v 4.6-Clients erstellt wurden. Sie müssen jedoch die zugehörige **OSD** -Datei so ändern, dass Sie die entsprechenden Informationen zum Betriebssystem und zur Chiparchitektur enthält. Verwenden Sie die folgenden Werte.

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

 

Wenn Sie ein neu erstelltes 32-Bit-Paket ausführen möchten, müssen Sie die Anwendung auf einem Computer mit einem 32-Bit-Betriebssystem mit dem App-v 4.6 Sequencer abgleichen. Nachdem Sie die Anwendung sequenziert haben, wählen Sie in der Sequencer-Konsole die Registerkarte **Bereitstellung** aus, und geben Sie dann die gewünschte Betriebssystem-und Chiparchitektur an.

**Wichtig**  Anwendungen, die auf einem Computer mit einem 64-Bit-Betriebssystem sequenziert sind, müssen auf Computern bereitgestellt werden, auf denen ein 64-Bit-Betriebssystem ausgeführt wird. Neue 32-Bit-Pakete, die mit dem App-v 4.6-Sequenzer erstellt wurden, werden auf Computern, auf denen der APP-v 4,5-Client ausgeführt wird, nicht ausgeführt.

 

Wenn Sie neue 64-Bit-Pakete auf dem App-v 4.6-Client ausführen möchten, müssen Sie die Anwendung auf einem Computer mit dem App-v 4.6-Sequenzer abgleichen, auf dem ein 64-Bit-Betriebssystem ausgeführt wird. Nachdem Sie die Anwendung sequenziert haben, wählen Sie in der Sequencer-Konsole die Registerkarte **Bereitstellung** aus, und geben Sie dann die gewünschte Betriebssystem-und Chiparchitektur an.

In der folgenden Tabelle wird aufgeführt, welche Clientversionen Pakete ausführen, die mit den verschiedenen Versionen des Sequencers erstellt wurden.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Sequenziert mithilfe des App-V 4,2-Sequenzers</th>
<th align="left">Sequenziert mithilfe des App-V 4,5-Sequenzers</th>
<th align="left">Sequenziert mithilfe des 32-Bit-App-V 4,6-Sequenzers</th>
<th align="left">Sequenziert mithilfe des 64-Bit-App-V 4,6-Sequenzers</th>
<th align="left">Sequenziert mithilfe der 32-Bit-App-V 4,6 SP1-Sequenzer</th>
<th align="left">Sequenziert mithilfe der 64-Bit-App-V 4,6 SP1-Sequenzer</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>4,2-Client</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Nein</p></td>
<td align="left"><p>Nein</p></td>
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
<td align="left"><p>Nein</p></td>
<td align="left"><p>Nein</p></td>
</tr>
<tr class="odd">
<td align="left"><p>4,6-Client (32-Bit)</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Nein.</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Nein.</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,6-Client (64-Bit)</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="odd">
<td align="left"><p>4,6 SP1-Client</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Nein.</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Nein.</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,6 SP1-Client (64-Bit)</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
</tr>
</tbody>
</table>

 

¹ gilt für alle Versionen des App-v 4.5-Clients, einschließlich APP-v 4.5, App-v 4.5 CU1 und App-v 4.5 SP1.

## Weitere Überlegungen zur Migration


Eines der Features des App-v 4.5-Sequenzers ist die Möglichkeit, Windows Installer-Dateien (MSI) als Kontrollpunkte für die Interoperabilität des virtuellen Anwendungspakets mit ESD-Systemen (Electronic Software Distribution) wie Microsoft Endpoint Configuration Manager zu erstellen. Frühere Windows Installer-Dateien, die mit dem MSI-Tool für Application Virtualization erstellt wurden, die auf einem App-v 4.1-oder 4.2-Client installiert wurden und anschließend auf 4.5 aktualisiert wurden, funktionieren weiterhin, auch wenn Sie nicht auf dem 4.5-Client installiert werden können. Sie können jedoch nur dann entfernt oder aktualisiert werden, wenn Sie im 4.5-Sequenzer aktualisiert wurden. Das ursprüngliche virtuelle Anwendungspaket vor 4,5 muss im 4.5-Sequenzer geöffnet und dann als Windows Installer-Datei gespeichert werden.

**Hinweis**  Wenn der APP-v 4.2-Client bereits auf 4.5 aktualisiert wurde, ist es möglich, das Skript als Problemumgehung zu verwenden, um die 4.2-Pakete auf 4.5-Clients beizubehalten und zu verwalten. Dieses Skript muss zwei Dateien, msvcp71.dll und msvcr71.dll, in den App-V-Installationsordner kopieren und die folgenden Registrierungsschlüsselwerte unter dem Registrierungsschlüssel \ [HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\configuration\] einrichten:

"Clientversion" = "4.2.1.20"

"GlobalDataDirectory" = "C:\\\\Documents und Settings\\\\All Users\\\\Documents\\\\" (ein Global beschreibbarer Speicherort)

 

Windows Installer-Dateien, die vom APP-v 4,5-Sequenzer generiert werden, zeigen die Fehlermeldung "dieses Paket erfordert Microsoft Application Virtualization Client 4,5 oder höher" an, wenn Sie versuchen, Sie auf einem App-v 4,6-Client auszuführen. Öffnen Sie das alte Paket entweder mit dem App-v 4,5 SP1-Sequenzer oder dem App-v 4,6-Sequenzer, und generieren Sie eine neue MSI-Version für das Paket.

Alle 4,2 Berichte, die erstellt und gespeichert wurden, werden überschrieben, wenn der Server auf 4.5 aktualisiert wird. Wenn Sie diese Berichte behalten möchten, müssen Sie eine Sicherungskopie der "SftMMC. MSC-Datei speichern, die sich im Ordner SoftGrid-Verwaltungskonsole auf dem Server befindet, und diese Kopie verwenden, um das neue" SftMMC. msc zu ersetzen, das während des Upgrades installiert ist.

Weitere Informationen zum Upgrade von vorherigen Versionen finden Sie unter [Upgrade auf Microsoft Application Virtualization 4,5 FAQ](https://go.microsoft.com/fwlink/?LinkId=120358) ( https://go.microsoft.com/fwlink/?LinkId=120358) .

## Verwandte Themen


[Planen der Bereitstellung von Application Virtualization System](planning-for-application-virtualization-system-deployment.md)

 

 





