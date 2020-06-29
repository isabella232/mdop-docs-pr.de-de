---
title: So migrieren Sie die SQL-Datenbank von App-V zu einem anderen SQL Server
description: So migrieren Sie die SQL-Datenbank von App-V zu einem anderen SQL Server
author: dansimp
ms.assetid: 353892a1-9327-4489-a19c-4ec7bd1b736f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e3d84b0cb328873db3722ad3eb9af6a2b442fdcf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806960"
---
# So migrieren Sie die SQL-Datenbank von App-V zu einem anderen SQL Server


In den folgenden Verfahren wird ausführlich beschrieben, wie Sie die SQL-Datenbank des Microsoft Application Virtualization (App-V)-Verwaltungsservers zu einem anderen SQL Server migrieren.

**Wichtig**  Diese Vorgehensweise setzt voraus, dass der App-V Server-Dienst beendet wird und dadurch verhindert wird, dass Endbenutzer Ihre Anwendungen verwenden.

 

**So sichern Sie die App-V SQL-Datenbank**

1.  Öffnen Sie das Programm "Services. msc", und beenden Sie den App-V-Verwaltungsserverdienst auf allen Verwaltungsservern, die die zu migrierende Datenbank verwenden.

2.  Öffnen Sie auf dem Computer, auf dem sich die App-V-Datenbank befindet, SQL Server Management Studio.

3.  Erweitern Sie den Knoten **Datenbanken** , und suchen Sie die App-V-Datenbank (Standardname lautet APPVIRT).

4.  Klicken Sie mit der rechten Maustaste auf die Datenbank, wählen Sie **Aufgaben** aus, und wählen Sie dann **sichern**aus.

5.  Stellen Sie sicher, dass das **Wiederherstellungsmodell** auf " **einfach** " und der **Sicherungstyp** auf " **voll**" festgesetzt ist. Ändern Sie bei Bedarf den **Sicherungssatz** und die **Ziel** Einstellungen.

6.  Klicken Sie auf **OK** , um die Datenbank zu sichern. Nachdem die Sicherung erfolgreich abgeschlossen wurde, klicken Sie auf **OK**.

7.  Öffnen Sie Windows-Explorer, und navigieren Sie zu dem Ordner, der die Datenbanksicherungsdatei enthält, beispielsweise APPVIRT. BAK. Kopieren Sie die Datenbanksicherungsdatei auf den Zielcomputer, auf dem SQL Server ausgeführt wird.

**So stellen Sie die App-V SQL-Datenbank auf dem Zielcomputer wieder her**

1.  Öffnen Sie auf dem Zielcomputer SQL Server Management Studio, klicken Sie mit der rechten Maustaste auf den Knoten **Datenbanken** , und wählen Sie **Datenbank wiederherstellen**aus.

2.  Wählen Sie unter **Quelle für wiederherstellen**die Option **vom Gerät aus** , und klicken Sie dann auf das Symbol "**..**.". .

3.  Stellen Sie im Dialogfeld **Sicherung angeben** sicher, dass das **Sicherungsmedium** auf **Datei** festgelegt ist, und klicken Sie dann auf **Hinzufügen**.

4.  Wählen Sie die Sicherungsdatei aus, die Sie von dem ursprünglichen Computer, auf dem SQL Server ausgeführt wird, kopiert haben, und klicken Sie dann auf **OK**.

5.  Klicken Sie auf **OK** , und wählen Sie dann den wiederherzustellenden Sicherungssatz aus.

6.  Klicken Sie unter **Ziel für Wiederherstellung**auf die Dropdownliste für die **Datenbank** , und wählen Sie den Namen der App-V-Datenbank aus, beispielsweise APPVIRT.

7.  Klicken Sie auf **OK** , um die Wiederherstellung zu starten. Nachdem die Wiederherstellung erfolgreich abgeschlossen wurde, klicken Sie auf **OK**.

8.  Erweitern Sie den Knoten **Sicherheit** , klicken Sie mit der rechten Maustaste auf **Anmeldungen** , und wählen Sie **neue Anmeldung**aus.

9.  Geben Sie im Feld **Anmelde Name** die Details des Netzwerkdienstkontos für den App-V-Verwaltungs Server im Format DOMAIN\\SERVERNAME $ ein.

10. Wählen Sie auf der Seite **Allgemein** unter **Standarddatenbank** den Namen der App-V-Datenbank aus, beispielsweise APPVIRT, und klicken Sie dann auf **OK**.

11. Klicken Sie unter **Seite auswählen**auf die Seite **Benutzerzuordnung** . Klicken Sie unter Benutzern, die **dieser Anmeldung zugeordnet**sind, auf das Kontrollkästchen in der Spalte **Karte** , um die App-V-Datenbank auszuwählen.

12. Klicken Sie unter **Datenbankrollenmitgliedschaft für: &lt; appvdatabasename &gt; **auf **SFTEveryone** , und klicken Sie dann auf **OK**.

13. Stellen Sie sicher, dass die Windows-Firewall auf dem neuen Computer, auf dem SQL Server ausgeführt wird, so konfiguriert ist, dass der App-V-Verwaltungs Server auf das System zugreifen kann. Verwenden Sie unter **Verwaltungs Tools**das Programm **Windows-Firewall mit erweiterter Sicherheit** , um eine **Eingehende Regel** für den von SQL Server verwendeten Port zu erstellen (Standard ist Port 1433).

**So migrieren Sie die Aufträge des App-V-SQL Server-Agents**

1.  Erweitern Sie auf dem ursprünglichen Computer, auf dem SQL Server ausgeführt wird, in SQL Server Management Studio den Knoten **SQL Server-Agent** , und erweitern Sie dann den Knoten **Aufträge** .

2.  Klicken Sie mit der rechten Maustaste auf die folgenden vier App-V-Aufträge, und wählen Sie **Skript Auftrag als | aus. Erstellen in | Datei**, und speichern Sie jedes Skript in einem Ordner, und geben Sie jedem Skript einen aussagekräftigen Namen.

    -   **SoftGrid-Datenbank (appvdbname) Überprüfen des Verwendungs Verlaufs**

    -   **SoftGrid-Datenbank (appvdbname) schließen verwaister Sitzungen**

    -   **SoftGrid-Datenbank (appvdbname) Größenbeschränkung erzwingen**

    -   **SoftGrid-Datenbank (appvdbname) Monitor Benachrichtigung/Auftrags Status**

3.  Kopieren Sie die vier Skriptdateien (SQL) auf den Zielcomputer, auf dem SQL Server ausgeführt wird, und öffnen Sie SQL Server Management Studio.

4.  Klicken Sie im Windows-Explorer mit der rechten Maustaste auf jede SQL-Datei, und klicken Sie dann auf **Ausführen**. Jedes Skript wird in einem Abfragefenster in SQL Server Management Studio geöffnet. Klicken Sie für jedes Skript auf **Ausführen** , und überprüfen Sie, ob die einzelnen Skripts erfolgreich abgeschlossen wurden.

5.  Aktualisieren Sie den Knoten **Aufträge** unter dem Knoten **SQL Server-Agent** , und bestätigen Sie, dass die vier Aufträge erfolgreich erstellt wurden.

**So aktualisieren Sie die Konfiguration des App-V-Verwaltungsservers**

1.  Ändern Sie auf dem App-V-Verwaltungs Server die folgenden Registrierungsschlüssel:

    -   **SQLServerName**  =  &lt; Servername&gt;

    -   **SQLServerPort**  =  SQLServerPort &lt; newserverport&gt;

    Starten Sie den App-V Server-Dienst erneut.

2.  Navigieren Sie zu der Datei SftMgmt. udl unter dem App-V Management Server-Installationsverzeichnis (Standard ist c:\\Programme c:\\Programme\\Microsoft System Center App virt Management Server\\App virt-Verwaltungsdienst). Klicken Sie mit der rechten Maustaste auf die Datei, und wählen Sie **Öffnen**aus.

3.  Geben Sie auf der Registerkarte **Verbindung** den Namen des Zielcomputers ein, auf dem SQL Server ausgeführt wird, und klicken Sie dann auf **Verbindung testen**. Wenn der Test erfolgreich war, klicken Sie auf **OK** , und klicken Sie dann erneut auf **OK** .

4.  Für App-V Management Server-Versionen vor 4,5 SP2 müssen Sie die SQL-Protokollierungseinstellungen aktualisieren. Klicken Sie unter **Servergruppen**mit der rechten Maustaste auf die Servergruppe, der der Server angehört, und wählen Sie **Eigenschaften**aus.

5.  Klicken Sie auf der Registerkarte **Protokollierung** auf den Eintrag **SQL-Datenbank** , und klicken Sie dann auf **Bearbeiten**.

6.  Ändern Sie den **Namen des DNS-Hosts** in den Hostnamen des neuen Computers, auf dem SQL Server ausgeführt wird, und klicken Sie dann auf **OK**. Klicken Sie zwei Mal auf **OK** , und starten Sie den App-V-Server Dienst erneut.

7.  Öffnen Sie die App-V-Verwaltungskonsole, klicken Sie mit der rechten Maustaste auf den Knoten **Anwendungen** , und wählen Sie **Aktualisieren**aus. Die Liste der Anwendungen sollte wie zuvor angezeigt werden.

 

 





