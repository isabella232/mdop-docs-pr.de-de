---
title: So installieren und konfigurieren Sie die MED-V-Serverkomponente
description: So installieren und konfigurieren Sie die MED-V-Serverkomponente
author: dansimp
ms.assetid: 2d3c5b15-df2c-4ab6-bf78-f47ef8ae7418
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4fb0cc5c9ffe76e987e316d0285f172dd0b76578
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812079"
---
# So installieren und konfigurieren Sie die MED-V-Serverkomponente


In diesem Abschnitt wird erläutert, wie Sie den MED-V-Server [Installieren](#bkmk-howtoinstallthemedvserver) und [Konfigurieren](#bkmk-howtoconfigurethemedvserver) .

## <a href="" id="bkmk-howtoinstallthemedvserver"></a>Installieren des MED-V-Servers


**So installieren Sie den MED-V-Server**

1.  Installieren Sie das MED-V Server. MSI-Paket.

    Das MED-V Server. MSI-Paket heißt *MED-V\_Server\_x.msi*, wobei x die Versionsnummer ist.

    Beispiel: *MED-V\_Server\_1.0.65.msi*.

2.  Wenn der **Begrüßungs** Bildschirm des InstallShield-Assistenten angezeigt wird, klicken Sie auf **weiter**.

3.  Lesen Sie auf dem Bildschirm **Lizenzvertrag** den Lizenzvertrag, klicken Sie auf **Ich stimme den Bedingungen des Lizenzvertrags**zu, und klicken Sie dann auf **weiter**.

    Der Bildschirm **Zielordner** wird angezeigt, und der Standardinstallationsordner wird angezeigt.

    Der Standardinstallationsordner ist *%systemdrive%\\Program c:\\Programme\\Microsoft Enterprise Desktop Virtualization\\*.

    -   Wenn Sie den Ordner ändern möchten, in dem MED-V installiert werden soll, klicken Sie auf **ändern** , und navigieren Sie zu einem vorhandenen Ordner.

4.  Klicken Sie auf **Weiter**.

5.  Klicken Sie auf dem Bildschirm **bereit zum Installieren des Programms** auf **Installieren**.

    Die Installation von MED-V Server wird gestartet. Dies kann mehrere Minuten dauern, und auf dem Bildschirm wird möglicherweise kein Text angezeigt. Während der Installation werden mehrere Status Bildschirme angezeigt. Wenn eine Meldung angezeigt wird, folgen Sie den Anweisungen.

6.  Wenn der Bildschirm **InstallShield-Assistent abgeschlossen** angezeigt wird, klicken Sie auf **Fertig stellen** , um den Assistenten abzuschließen.

**Hinweis:**  
Wenn Sie den MED-V-Server über Microsoft Remote Desktop installieren, verwenden Sie die folgende Syntax: **mstsc/Administrator**. Stellen Sie sicher, dass Ihre RDP-Sitzung an die Konsole weitergeleitet wird.



## <a href="" id="bkmk-howtoconfigurethemedvserver"></a>Konfigurieren des MED-V-Servers


Die folgenden Servereinstellungen können konfiguriert werden:

-   [Verbindungen](#bkmk-configuringconnections)

-   [Images](#bkmk-configuringimages)

-   [Berechtigungen](#bkmk-configuringpermissions)

-   [Berichte](#bkmk-configuringreports)

### <a href="" id="bkmk-configuringconnections"></a>Konfigurieren von Verbindungen

**So konfigurieren Sie Verbindungen**

1.  Wählen Sie im Windows-Startmenü **Alle Programme &gt; Med-v &gt; Med-v Server Configuration Manager**aus.

    **Hinweis:**  
    Hinweis: Wenn Sie während der Server Installation das Kontrollkästchen **Med-v Server-Konfigurations-Manager starten** aktiviert haben, wird der Med-v Server-Konfigurations-Manager automatisch gestartet, nachdem die Server Installation abgeschlossen ist.



~~~
The MED-V Server Configuration Manager appears.
~~~

2. Konfigurieren Sie auf der Registerkarte **Verbindungen** die folgenden Clientverbindungseinstellungen:

   -   **Aktivieren von nicht verschlüsselten Verbindungen (http) mithilfe von Port**– aktivieren Sie dieses Kontrollkästchen, um unverschlüsselte Verbindungen über einen angegebenen Port zu aktivieren. Geben Sie im Feld Port den Serverport ein, auf dem unverschlüsselte Verbindungen (http) akzeptiert werden sollen.

   -   **Aktivieren von verschlüsselten Verbindungen (HTTPS) mithilfe von Port**– aktivieren Sie dieses Kontrollkästchen, um verschlüsselte Verbindungen über einen angegebenen Port zu aktivieren. Geben Sie im Feld Port den Serverport ein, auf dem verschlüsselte Verbindungen (HTTPS) akzeptiert werden sollen.

       HTTPS ist eine optionale Konfiguration, mit der Sie sichere Transaktionen zwischen dem Med-v-Server und Med-v-Clients sicherstellen können. Um HTTPS zu konfigurieren, müssen Sie die folgenden Schritte ausführen:

       -   Konfigurieren Sie ein Zertifikat auf dem Server.

       -   Ordnen Sie das Serverzertifikat dem mit Netsh angegebenen Port zu. Informationen finden Sie unter den folgenden Themen:

           -   [Netsh-Befehle für Hypertext Transfer Protocol (http)](https://go.microsoft.com/fwlink/?LinkId=183314)

           -   [So wird es gemacht: Konfigurieren eines Ports mit einem SSL-Zertifikat](https://go.microsoft.com/fwlink/?LinkID=183315)

           -   [So wird es gemacht: Konfigurieren eines Ports mit einem SSL-Zertifikat](https://msdn.microsoft.com/library/ms733791.aspx)

3. Klicken Sie auf **OK**.

### <a href="" id="bkmk-configuringimages"></a>Konfigurieren von Bildern

**So konfigurieren Sie Bilder**

1.  Klicken Sie auf die Registerkarte **Bilder** .

2.  Konfigurieren Sie die folgenden Einstellungen für die Bildverwaltung:

    -   **VMS-Verzeichnis**– das Verzeichnis der virtuellen Computer (das Verzeichnis, in dem die Bilder gespeichert sind). Dieses Feld enthält einen UNC-Pfad zum Bildverzeichnis auf dem Bildverteilungsserver, auf das vom MED-V-Server aus zugegriffen werden sollte.

    -   **VMS-URL**– der Speicherort des Servers, auf dem die Bilder gespeichert sind.

3.  Klicken Sie auf **OK**.

### <a href="" id="bkmk-configuringpermissions"></a>Konfigurieren von Berechtigungen

**So konfigurieren Sie Berechtigungen**

1.  Klicken Sie auf die Registerkarte **Berechtigungen** .

2.  Es wird eine Liste aller Benutzer bereitgestellt, die sich anmelden können. Wenn Sie Lese-und Schreibberechtigungen für einen Benutzer anwenden möchten, aktivieren Sie das Kontrollkästchen neben dem Benutzer. Deaktivieren Sie das Kontrollkästchen, um einem Benutzer schreibgeschützte Berechtigungen zuzuweisen.

3.  Klicken Sie zum Hinzufügen von Domänenbenutzern oder-Gruppen auf **Hinzufügen**.

    Das Dialogfeld **Benutzer-oder Gruppennamen eingeben** wird angezeigt.

    1.  Wählen Sie Domänenbenutzer oder-Gruppen aus, indem Sie eine der folgenden Aktionen ausführen:

        -   Geben Sie im Feld **Benutzer-oder Gruppennamen eingeben** einen Benutzer oder eine Gruppe ein, der in der Domäne vorhanden oder als lokaler Benutzer oder eine Gruppe auf dem Computer vorhanden ist. Klicken Sie dann auf **Namen überprüfen** , um Sie in den vollständigen vorhandenen Namen aufzulösen.

        -   Klicken Sie auf **Suchen** , um das Dialogfeld **Benutzer oder Gruppen Standard auswählen** zu öffnen. Wählen Sie dann Domänenbenutzer oder Gruppen aus.

    2.  Klicken Sie auf **OK**.

4.  Wenn Sie Domänenbenutzer oder-Gruppen entfernen möchten, wählen Sie einen Benutzer oder eine Gruppe aus, und klicken Sie auf **Entfernen**.

5.  Klicken Sie auf **OK**.

### <a href="" id="bkmk-configuringreports"></a>Konfigurieren von Berichten

**So konfigurieren Sie Berichte**

1.  Klicken Sie auf die Registerkarte **Berichte** .

2.  Wenn Sie Berichte unterstützen möchten, wählen Sie **Berichte aktivieren**aus.

3.  Geben Sie im Feld **Verbindungszeichenfolge** eine Verbindungszeichenfolge für die MSSQL-Datenbank ein.

    -   Wenn SQL Server auf einem Remoteserver installiert ist, verwenden Sie die folgende Verbindungszeichenfolge:

        `Data Source=<ServerName>;Initial Catalog=<DBName>;uid=sa;pwd=<Password>;`

        **Hinweis:**  
        Hinweis: zum Herstellen einer Verbindung mit SQL Express verwenden Sie: `Data Source=<ServerName>\sqlexpress.`



4.  Klicken Sie zum Erstellen der Datenbank auf **Datenbank erstellen**.

5.  Klicken Sie auf **Verbindung testen**, um die Verbindung zu testen.

6.  Klicken Sie auf **Optionen löschen**, um die Optionen zum Löschen von Datenbanken zu konfigurieren.

    Das Dialogfeld **Datenbankoptionen löschen** wird angezeigt.

    1.  Wählen Sie eine der folgenden Optionen aus:

        -   **Löschen von Daten**, die älter als sind, löschen Sie alle Daten, die älter als die angegebene Anzahl von Tagen sind. Geben Sie im Feld Zahl eine Anzahl von Tagen ein.

        -   **Löschen aller Daten aus einer Datenbank**– löschen Sie alle vorhandenen Daten in der Datenbank.

        -   **Drop Database**– löschen Sie die Datenbank.

    2.  Klicken Sie auf **OK** , um Änderungen zu übernehmen und das Dialogfeld zu schließen.

7.  Klicken Sie auf **OK** , um die Änderungen zu speichern, oder auf **Abbrechen** , um das Dialogfeld zu schließen, ohne die Änderungen zu speichern.

8.  Wenn Sie dazu aufgefordert werden, starten Sie den MED-V-Server Dienst neu, um Änderungen auf die Netzwerkeinstellungen anzuwenden.

## Verwandte Themen


[Unterstützte Konfigurationen](supported-configurationsmedv-orientation.md)

[Entwerfen der MED-V-Server-Infrastruktur](design-the-med-v-server-infrastructure.md)









