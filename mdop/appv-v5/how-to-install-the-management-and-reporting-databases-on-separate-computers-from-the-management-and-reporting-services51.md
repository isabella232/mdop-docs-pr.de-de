---
title: So installieren Sie die Verwaltungs- und Berichtsdatenbanken auf verschiedenen Computern über die Verwaltungs- und Berichtsdienste
description: So installieren Sie die Verwaltungs- und Berichtsdatenbanken auf verschiedenen Computern über die Verwaltungs- und Berichtsdienste
author: dansimp
ms.assetid: 2a67402e-3119-40ea-a247-24d166af1ced
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2332f674f10a9b60aa1cee814c6eac4ddbe4f5af
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805423"
---
# So installieren Sie die Verwaltungs- und Berichtsdatenbanken auf verschiedenen Computern über die Verwaltungs- und Berichtsdienste

Gehen Sie wie folgt vor, um den Datenbankserver und den Verwaltungsserver auf unterschiedlichen Computern zu installieren. Auf dem Computer, auf dem Sie den Datenbankserver installieren möchten, muss eine unterstützte Version von Microsoft SQL ausgeführt werden, oder die Installation schlägt fehl.

> [!NOTE]
> Nachdem Sie die Bereitstellung abgeschlossen haben, müssen der **Microsoft SQL Server-Name**, der **Instanzname** und der **Datenbankname** vom Administrator installiert werden, um eine Verbindung mit diesen Datenbanken herstellen zu können.

## So installieren Sie die Verwaltungsdatenbank und den Verwaltungsserver auf separaten Computern

1. Kopieren Sie die App-V 5,1 Server-Installationsdateien auf den Computer, auf dem Sie Sie installieren möchten. Um die App-V 5,1 Server-Installation zu starten, klicken Sie mit der rechten Maustaste, und führen Sie **appv\_server\_setup.exe** als Administrator aus. Klicken Sie auf **Installieren**.
1. Überprüfen und akzeptieren Sie auf der Seite **Erste Schritte** die Lizenzbestimmungen, und klicken Sie auf **weiter**.
1. Aktivieren Sie auf der Seite **Microsoft Update verwenden, um die Sicherheit Ihres Computers zu gewährleisten und auf dem neuesten Stand zu bleiben** , um Microsoft Updates zu aktivieren, die Option **Microsoft Update verwenden, wenn ich auf Updates Suche (empfohlen).** Wenn Sie Microsoft-Updates deaktivieren möchten, wählen Sie **Ich möchte Microsoft Update nicht verwenden**aus. Klicken Sie auf **Weiter**.
1. Wählen Sie auf der Seite **Featureauswahl** die Komponenten aus, die Sie installieren möchten, indem Sie das Kontrollkästchen **Verwaltungs Server-Datenbank** auswählen und auf **weiter**klicken.
1. Übernehmen Sie auf der Seite **Installationsspeicherort** den Standardspeicherort, und klicken Sie auf **weiter**.
1. Übernehmen Sie auf der **Seite erste neue Verwaltungs Server-Datenbank erstellen**die Standardauswahl, falls zutreffend, und klicken Sie auf **weiter**.

    Wenn Sie eine benutzerdefinierte SQL Server-Instanz verwenden, wählen Sie **benutzerdefinierte Instanz verwenden** aus, und geben Sie den Namen der Instanz ein. \
    Wenn Sie einen benutzerdefinierten Datenbanknamen verwenden, wählen Sie **benutzerdefinierte Konfiguration** aus, und geben Sie den Datenbanknamen ein.

1. Wählen Sie auf der nächsten Seite **neue Verwaltungs Server-Datenbank erstellen** die Option **Remotecomputer verwenden**aus, und geben Sie das Konto des Remotecomputers mit dem folgenden Format ein: **Domain\\MachineAccount**.

    > [!NOTE]
    > Wenn Sie den Verwaltungsserver auf demselben Computer bereitstellen möchten, müssen Sie **diesen lokalen Computer verwenden**auswählen.

1. Geben Sie den Benutzernamen für den Verwaltungsserver- **Installations Administrator** unter Verwendung des folgenden Formats an: **Domain\\AdministratorLoginName**. Klicken Sie auf **Weiter**.
1. Klicken Sie auf **Installieren**, um die Installation zu starten.

## So installieren Sie die Berichtsdatenbank und den Berichtsserver auf separaten Computern

1. Kopieren Sie die App-V 5,1 Server-Installationsdateien auf den Computer, auf dem Sie Sie installieren möchten. Um die App-V 5,1 Server-Installation zu starten, klicken Sie mit der rechten Maustaste, und führen Sie **appv\_server\_setup.exe** als Administrator aus. Klicken Sie auf **Installieren**.
1. Überprüfen und akzeptieren Sie auf der Seite **Erste Schritte** die Lizenzbestimmungen, und klicken Sie auf **weiter**.
1. Aktivieren Sie auf der Seite **Microsoft Update verwenden, um die Sicherheit Ihres Computers zu gewährleisten und auf dem neuesten Stand zu bleiben** , um Microsoft Updates zu aktivieren, die Option **Microsoft Update verwenden, wenn ich auf Updates Suche (empfohlen).** Wenn Sie Microsoft-Updates deaktivieren möchten, wählen Sie **Ich möchte Microsoft Update nicht verwenden**aus. Klicken Sie auf **Weiter**.
1. Wählen Sie auf der Seite **Featureauswahl** die Komponenten aus, die Sie installieren möchten, indem Sie das Kontrollkästchen **Berichts Server-Datenbank** auswählen und auf **weiter**klicken.
1. Übernehmen Sie auf der Seite **Installationsspeicherort** den Standardspeicherort, und klicken Sie auf **weiter**.
1. Übernehmen Sie auf der Seite erste **neue Berichts Server-Datenbank erstellen** die Standardauswahl, falls zutreffend, und klicken Sie auf **weiter**.

    Wenn Sie eine benutzerdefinierte SQL Server-Instanz verwenden, wählen Sie **benutzerdefinierte Instanz verwenden** aus, und geben Sie den Namen der Instanz ein.
    Wenn Sie einen benutzerdefinierten Datenbanknamen verwenden, wählen Sie **benutzerdefinierte Konfiguration** aus, und geben Sie den Datenbanknamen ein.

1. Wählen Sie auf der nächsten Seite **neue Berichts Server-Datenbank erstellen** die Option **Remotecomputer verwenden**aus, und geben Sie das Konto des Remotecomputers mit dem folgenden Format ein: **Domain\\MachineAccount**.

    > [!NOTE]
    > Wenn Sie den Berichtsserver auf demselben Computer bereitstellen möchten, müssen Sie **diesen lokalen Computer verwenden**auswählen.

1. Geben Sie den Benutzernamen für den Berichterstellungsserver- **Installations Administrator** mit dem folgenden Format an: **Domain\\AdministratorLoginName**. Klicken Sie auf **Weiter**.
1. Klicken Sie auf **Installieren**, um die Installation zu starten.

## So installieren Sie die Verwaltungs-und Berichtsdatenbanken mithilfe von App-V 5,1-Datenbankskripts

1. Kopieren Sie die App-V 5,1 Server-Installationsdateien auf den Computer, auf dem Sie Sie installieren möchten.
1. Wenn Sie die App-V 5,1-Datenbankskripts extrahieren möchten, öffnen Sie eine Eingabeaufforderung, geben Sie den Speicherort der Installationsdateien an, und führen Sie den folgenden Befehl aus:

    **appv\_server\_setup.exe** **/Layout** **/LAYOUTDIR = "InstallationExtractionLocation"**.

1. Nachdem die Extrahierung abgeschlossen wurde, können Sie auf die App-V 5,1-Datenbankskripts und Anweisungen in der Readme-Datei zugreifen:

    - Die Readme-Datei für die App-V 5,1-Verwaltungsdatenbank und die Anweisungen für die Anleitung finden Sie im folgenden Ordner: **InstallationExtractionLocation**  \\  **Database Scripts**  \\  **Management Database**.
    - Die Readme-Datei für die App-V 5,1-Berichtsdatenbank und die Anweisungen für die Anleitung finden Sie im folgenden Ordner: **InstallationExtractionLocation**  \\  **Database Scripts**  \\  **Reporting Database**.

1. Kopieren Sie für jede Datenbank die Skripts auf eine Freigabe, und ändern Sie Sie, und folgen Sie den Anweisungen in der Readme-Datei.

    > [!NOTE]
    > Weitere Informationen zum Ändern der erforderlichen SIDs in den Skripts finden Sie unter so wird es [gemacht: Installieren der App-V-Datenbanken und Konvertieren der zugehörigen Sicherheitsbezeichner mithilfe von PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell51.md).

1. Führen Sie die Skripts auf dem Computer aus, auf dem Microsoft SQL Server ausgeführt wird.

**Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen

[Bereitstellen von App-V 5.1](deploying-app-v-51.md)
