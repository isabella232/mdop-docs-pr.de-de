---
title: So installieren und konfigurieren Sie die Standardanwendung
description: So installieren und konfigurieren Sie die Standardanwendung
author: dansimp
ms.assetid: 5c5d5ad1-af40-4f83-8234-39e972f2c29a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083de7a8ebf94bce0b41c0d3c3edf350a9aff38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807079"
---
# So installieren und konfigurieren Sie die Standardanwendung


Die Standardanwendung wird als Teil der Installation bereitgestellt und während der Installation automatisch auf den Microsoft Application Virtualization (App-V)-Verwaltungs Server kopiert. Sie wird verwendet, um zu überprüfen, ob der Verwaltungs Server ordnungsgemäß installiert und konfiguriert wurde, muss aber auf dem Microsoft Application Virtualization (App-V)-Client veröffentlicht werden, damit der Benutzer darauf zugreifen kann.

Führen Sie die folgenden Verfahren aus, um die Standardanwendung zu veröffentlichen und zu streamen.

**So veröffentlichen Sie die Standardanwendung**

1.  Melden Sie sich beim APP-v-Verwaltungs Server mit einem Konto an, das Mitglied der während der Installation angegebenen app-v-Administratorengruppe ist.

2.  Klicken Sie auf dem App-V-Verwaltungs Server auf **Start**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **Application Virtualization Management Console**.

3.  Klicken Sie in der App-V-Verwaltungskonsole auf **Aktionen**, und klicken Sie dann auf mit **Application Virtualization System verbinden**.

4.  Deaktivieren Sie auf der Seite **Verbindung konfigurieren** das Kontrollkästchen **sichere Verbindung verwenden** .

5.  Geben Sie im Feld **Hostname des Webdiensts** den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des App-V-Verwaltungsservers ein, und klicken Sie dann auf **OK**.

    **Hinweis**  Sie können **localhost** auch für den Webdienst-Hostnamen verwenden, wenn er auf dem Verwaltungs Server installiert ist.

     

6.  Klicken Sie in der App-V-Verwaltungskonsole mit der rechten Maustaste auf den **Server** Knoten, und klicken Sie auf **System Optionen**.

7.  Geben Sie auf der Registerkarte **Allgemein** im Feld **Standardinhalts Pfad** den UNC-Pfad (Universal Naming Convention) zu dem Inhaltsordner ein, den Sie während der Installation auf dem Server erstellt haben. Beispiel: \ \ \ \ &lt; Server Name &gt; \\Content, und klicken Sie dann auf **OK**.

    **Wichtig**  Verwenden Sie den FQDN für den Servernamen, damit der Client den Namen richtig auflösen kann.

     

8.  Erweitern Sie in der App-V-Verwaltungskonsole im Navigationsbereich den **Server** Knoten, und klicken Sie dann auf **Anwendungen**.

9.  Klicken Sie im Themenbereich auf **Standardanwendung**, und klicken Sie dann im Bereich **Aktionen** auf **Eigenschaften**.

10. Klicken Sie im Dialogfeld **Eigenschaften** neben dem Feld **OSD-Pfad** auf **Durchsuchen**.

11. Geben Sie im Dialogfeld **Öffnen** den UNC-Pfad zu dem Inhaltsordner ein, den Sie während der Installation auf dem Server erstellt haben. Beispiel: \ \ \ \ &lt; Server Name &gt; \\Content, und drücken Sie die EINGABETASTE. Sie müssen den tatsächlichen Servernamen verwenden und den **localhost** hier nicht verwenden.

    **Wichtig**  Stellen Sie sicher, dass sich die Werte in den Feldern " **OSD-Pfad** **" und "Symbolpfad"** im UNC-Format befinden (beispielsweise \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ &lt; Server Name &gt; \\Content\\DefaultApp.ico) und auf den Inhaltsordner Verwenden Sie keine **localhost** -Datei oder einen Dateipfad, der einen Laufwerkbuchstaben wie c:\\Programme Files\\.. \\.. Inhalts.

     

12. Wählen Sie die DefaultApp. OSD-Datei aus, und klicken Sie auf **Öffnen**.

13. Wiederholen Sie die vorherigen Schritte zum Konfigurieren des Symbolpfads.

14. Klicken Sie auf die Registerkarte **Zugriffsberechtigungen** , und vergewissern Sie sich, dass die App-V-Benutzergruppe über Zugriffsberechtigungen für die Anwendung verfügt.

15. Klicken Sie auf die Registerkarte **Verknüpfungen** , und klicken Sie dann auf **auf dem Desktop des Benutzers veröffentlichen**. Klicken Sie auf **OK**.

16. Öffnen Sie den Windows-Explorer, und suchen Sie nach dem Inhaltsverzeichnis.

17. Doppelklicken Sie auf die DefaultApp. OSD-Datei, und öffnen Sie Sie mit Editor.

18. Suchen Sie die Zeile, die das **href** -Tag enthält, und ändern Sie Sie in den folgenden Code:

         `CODEBASEHREF=”RTSP://<FQDN of your server>:554/DefaultApp.sft”`

    Wenn Sie RTSPS verwenden:

         `CODEBASEHREF=”RTSPS://<FQDN of your server>:322/DefaultApp.sft”`

19. Schließen Sie die DefaultApp. OSD-Datei, und speichern Sie die Änderungen.

**So streamen Sie die Standardanwendung**

1.  Melden Sie sich auf dem Computer, auf dem der App-V-Client installiert ist, als Benutzer an, der Mitglied der Application Virtualization users-Gruppe ist, die während der Server Installation angegeben wurde.

2.  Auf dem Desktop wird die **Standardtastenkombination der Application Virtualization-Anwendung** angezeigt. Doppelklicken Sie auf die Verknüpfung, um die Anwendung zu starten.

3.  Eine Statusleiste, die über dem Windows-Infobereich angezeigt wird, gibt an, dass die Anwendung gestartet wird. Wenn der Anwendungsstart erfolgreich ist, wird der Titelbildschirm für die Standardanwendung angezeigt. Klicken Sie auf **OK** , um das Dialogfeld zu schließen. Sie haben nun bestätigt, dass das App-V-System ordnungsgemäß ausgeführt wird.

## Verwandte Themen


[So konfigurieren Sie Server für die serverbasierte Bereitstellung](how-to-configure-servers-for-server-based-deployment.md)

 

 





