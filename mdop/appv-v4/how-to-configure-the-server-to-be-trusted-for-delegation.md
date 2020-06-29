---
title: So konfigurieren Sie den Server, damit ihm für Delegierungszwecke vertraut wird
description: So konfigurieren Sie den Server, damit ihm für Delegierungszwecke vertraut wird
author: dansimp
ms.assetid: d8d11588-17c0-4bcb-a7e6-86b5e4ba7e1c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7164b3046671853216b870d68e651fed4fd84695
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807231"
---
# So konfigurieren Sie den Server, damit ihm für Delegierungszwecke vertraut wird


Wenn Sie die Microsoft Application Virtualization (App-V)-Verwaltungs Server Software installieren, können Sie Sie mithilfe einer verteilten Systemarchitektur installieren. Wenn Sie die Konsole, den Verwaltungs-Webdienst und die Datenbank auf unterschiedlichen Computern installieren, müssen Sie den IIS-Server (Internet Information Services) so konfigurieren, dass er für die Delegierung als vertrauenswürdig eingestuft wird. Dies ist erforderlich, da der Verwaltungs-Webdienst versucht, eine Verbindung mit dem App-v-Datenspeicher mithilfe der Anmeldeinformationen des App-v-Administrators herzustellen, der die Konsole verwendet. Der Datenbankserver, auf dem der Datenspeicher installiert ist, akzeptiert die Anmeldeinformationen des Administrators nicht vom IIS-Server, es sei denn, der IIS-Server ist für die Delegierung als vertrauenswürdig eingestuft, und der Verwaltungs-Webdienst kann keine Verbindung mit dem App-V-Datenspeicher herstellen.

**Hinweis**  Wenn Sie die App-V Management Server-Software auf einem einzelnen Server installieren und den Datenspeicher auf einem separaten Server platzieren, gibt es eine Situation, in der Sie den Server weiterhin als vertrauenswürdig für die Delegierung konfigurieren müssen, obwohl sich der Verwaltungs-Webservice und die Verwaltungskonsole auf demselben Server befinden. Diese Situation tritt auf, wenn Sie eine Verbindung mit dem Verwaltungs-Webdienst in der Konsole herstellen müssen, indem Sie die Option **Alternative Anmeldeinformationen verwenden verwenden** .

 

Die Art der Delegierung, die Sie verwenden können, hängt von der Domänenfunktionsebene ab, die Sie in Ihrer Infrastruktur für Active Directory-Domänendienste (Adds) konfiguriert haben. In der folgenden Tabelle sind die Delegierungs Typen aufgeführt, die für die einzelnen Domänenfunktionsebenen für App-V konfiguriert werden können. Eine detaillierte Anleitung finden Sie in der Tabelle.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Domänenfunktionsebene</th>
<th align="left">Verfügbare Delegierungs Ebenen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 2000 Native</p></td>
<td align="left"><ul>
<li><p>Keine Delegierung (Standard)</p></li>
<li><p>Nicht eingeschränkte Delegierung</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2003, Windows Server 2008 oder Windows Server 2008 R2</p></td>
<td align="left"><ul>
<li><p>Keine Delegierung (Standard)</p></li>
<li><p>Uneingeschränkte Delegierung ¹</p></li>
<li><p>Beschränkte Delegierung (nur Kerberos-Protokolle verwenden)</p></li>
<li><p>Beschränkte Delegierung (Verwenden eines beliebigen Authentifizierungsprotokolls) ¹</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

¹ nicht empfohlen.

## So konfigurieren Sie eine uneingeschränkte Delegierung, wenn die Domänenfunktionsebene Windows 2000 native ist


Führen Sie auf dem Domänencontroller für die Domäne Ihres Webservers die folgenden Schritte aus.

****

1.  Klicken Sie auf **Start**, **Verwaltungs Tools**und dann auf **Active Directory-Benutzer und-Computer**.

2.  Erweitern Sie Domäne, und erweitern Sie dann den Ordner Computer.

3.  Klicken Sie im rechten Bereich mit der rechten Maustaste auf den Computernamen für den Webserver, und klicken Sie dann auf **Eigenschaften**.

4.  Stellen Sie auf der Registerkarte **Allgemein** sicher, dass das Kontrollkästchen **Computer für Delegierungszwecke vertrauen** aktiviert ist.

5.  Klicken Sie auf **OK**.

## So konfigurieren Sie eine uneingeschränkte Delegierung, wenn es sich bei der Domänenfunktionsebene um Windows Server 2003, Windows Server 2008 oder Windows Server 2008 R2 handelt


Führen Sie auf dem Domänencontroller für die Domäne Ihres Webservers die folgenden Schritte aus.

****

1.  Klicken Sie auf **Start**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **Active Directory-Benutzer und-Computer**.

2.  Erweitern Sie Domäne, und erweitern Sie den Ordner Computer.

3.  Klicken Sie im rechten Bereich mit der rechten Maustaste auf den Computernamen für den Webserver, wählen Sie **Eigenschaften**aus, und klicken Sie dann auf die Registerkarte **Delegierung** .

4.  Klicken Sie auf **diesen Computer für die Delegierung an einen beliebigen Dienst Vertrauen (nur Kerberos)**.

5.  Klicken Sie auf **OK**.

## So konfigurieren Sie eine begrenzte Delegierung, wenn die Domänenfunktionsebene Windows Server 2003, Windows Server 2008 oder Windows Server 2008 R2 ist


Führen Sie auf dem Domänencontroller für die Domäne Ihres Webservers die folgenden Schritte aus.

****

1.  Klicken Sie auf **Start**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **Active Directory-Benutzer und-Computer**.

2.  Erweitern Sie Domäne, und erweitern Sie dann den Ordner Computer.

3.  Klicken Sie im rechten Bereich mit der rechten Maustaste auf den Computernamen für den Webserver, wählen Sie **Eigenschaften**aus, und klicken Sie dann auf die Registerkarte **Delegierung** .

4.  Klicken Sie auf **diesen Computer für Delegierung nur an angegebene Dienste vertrauen**.

5.  Stellen Sie sicher, dass **nur Kerberos verwenden** ausgewählt ist, und klicken Sie dann auf **OK**.

6.  Klicken Sie auf die Schaltfläche **Hinzufügen**. Klicken Sie im Dialogfeld **Dienste hinzufügen** auf **Benutzer oder Computer**, und navigieren Sie dann zu dem Namen des Microsoft SQL Server, auf dem sich der App-V-Datenspeicher befindet, oder geben Sie ihn ein, um die Anmeldeinformationen des Benutzers aus IIS zu erhalten. Klicken Sie auf **OK**.

7.  Wählen Sie in der Liste **verfügbare Dienste** den MSSQLSvc-Dienst aus, der die Portnummer auflistet, für die der Microsoft SQL Server Verbindungen für die App-V-Datenbank akzeptiert (der Standardport ist 1433). Klicken Sie auf **OK**.

### Zusätzliche Schritte zum Konfigurieren von IIS 7 für eine begrenzte Delegierung

Wenn Sie den Verwaltungs-Webdienst auf einem IIS 7-Server ausführen, müssen Sie die folgenden Schritte ausführen, um die IIS 7- *useAppPoolCredentials* -Variable auf "true" festzulegen.

1.  Öffnen Sie ein Eingabeaufforderungsfenster mit erhöhten Rechten. Klicken Sie zum Öffnen eines Eingabeaufforderungsfensters mit erhöhten Rechten auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Zubehör**, klicken Sie mit der rechten Maustaste auf **Eingabeaufforderung**, und klicken Sie dann auf **als Administrator ausführen**.

2.  Navigieren zu%windir%\\system32\\inetsrv.

3.  Geben Sie **appcmd.exe Satz config-section: System. Webserver/Security/Authentication/WindowsAuthentication-useAppPoolCredentials: true**ein, und drücken Sie dann die EINGABETASTE.

 

 





