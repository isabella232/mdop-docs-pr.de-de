---
title: Konfigurieren des Unternehmenseinstellungen-Centers für UE-V 2. x
description: Konfigurieren des Unternehmenseinstellungen-Centers für UE-V 2. x
author: dansimp
ms.assetid: 48fadb0a-c0dc-4287-9474-f94ce1417003
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0226b3c156a6d6ca39b0214de8acf0c5990db349
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809868"
---
# Konfigurieren des Unternehmenseinstellungen-Centers für UE-V 2. x


Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 und 2,1 SP1 beinhalten eine neue Anwendung, das Unternehmenseinstellungen-Center, mit dem Benutzer die Einstellungen für die Synchronisierung verwalten können. Das Unternehmenseinstellungen-Center wird mithilfe des UE-V-Agents installiert. Benutzer greifen auf das Unternehmenseinstellungen-Center in der Systemsteuerung, im **Startmenü** oder auf dem **Start** Bildschirm und über das Symbol "UE-V-Benachrichtigungsbereich" zu. Das Unternehmenseinstellungen-Center zeigt an, welche Einstellungen synchronisiert sind, und hilft Benutzern, den Synchronisierungsstatus von UE-V anzuzeigen. Benutzer können das Unternehmenseinstellungen-Center verwenden, um auszuwählen, welche Anwendungen oder Windows-Features Ihre Einstellungen zwischen Computern synchronisieren. Sie können auch auf die Schaltfläche " **Jetzt synchronisieren** " klicken, um alle Einstellungen sofort zu synchronisieren. Der Administrator kann auch einen Link zur Unterstützung im Unternehmenseinstellungen-Center hinzufügen.

## Informationen zum Unternehmenseinstellungen-Center


Die Desktopanwendung "Unternehmenseinstellungen Center" bietet Benutzern Informationen zur Synchronisierung der UE-V-Einstellungen. Auf das Unternehmenseinstellungen-Center kann auf verschiedene Arten zugegriffen werden:

-   Symbol "Benachrichtigungsbereich" – Wenn die Gruppenrichtlinieneinstellung für das **Taskleistensymbol** oder die Windows PowerShell-Konfiguration aktiviert ist, wird das UE-V-Symbol im Infobereich angezeigt. Klicken Sie auf das UE-V-Symbol, um das Unternehmenseinstellungen-Center zu öffnen.

    **Hinweis**  Das Symbol für das Infobereich kann mithilfe der folgenden Einstellungen deaktiviert werden:

    -   Gruppenrichtlinieneinstellung: `Policy Tray Icon`

    -   Windows PowerShell-Cmdlet: `TrayIconEnabled`

    -   Konfigurationselement im UE-V-Konfigurationspaket für SystemCenter2012 ConfigurationManager: `Tray icon enabled`

     

-   Control Panel-Anwendung – navigieren Sie in der Systemsteuerung zu **Darstellung und Personalisierung**, und klicken Sie dann auf **Unternehmenseinstellungen Center**.

-   Erste Verwendung Benachrichtigung – sofern nicht deaktiviert, benachrichtigt der UE-v-Agent den Benutzer, dass die Einstellungen jetzt synchronisiert werden, wenn der UE-v-Agent zum ersten Mal auf einem Computer ausgeführt wird. Klicken Sie auf das Dialogfeld Benachrichtigung, um das Unternehmenseinstellungen-Center zu öffnen.

-   Der **Start** Bildschirm oder das **Startmenü** enthält einen Link zum Unternehmenseinstellungen-Center. Eine Suche nach dem Unternehmenseinstellungen-Center findet die Anwendung.

## Konfigurieren des Support-Links im Unternehmenseinstellungen-Center


Das Unternehmenseinstellungen-Center kann einen Hyperlink enthalten, auf den Benutzer klicken können, um Unterstützung bei Synchronisierungsproblemen mit UE-V-Einstellungen zu erhalten. Dieser Link kann ein beliebiges gültiges URL-Protokoll öffnen, beispielsweise http://für eine Webseite oder mailto://für eine e-Mail. Der Support-Link kann mithilfe von Gruppenrichtlinien, Windows PowerShell oder dem System Center 2012 Configuration Manager UE-V-Konfigurationspaket konfiguriert werden.

**Konfigurieren des Support Links für das Unternehmenseinstellungen-Center**

1.  Öffnen Sie Ihr bevorzugtes Verwaltungstool:

    -   **Gruppenrichtlinie** – Wenn Sie dies noch nicht getan haben, laden Sie die ADMX-Vorlage für UE-V 2 aus [MDOP administrative Vorlagen](https://go.microsoft.com/fwlink/p/?LinkId=393941)herunter.

    -   **Windows PowerShell** – öffnen Sie **Windows PowerShell**auf einem Computer, auf dem der UE-V-Agent installiert ist. Weitere Informationen zum Verwalten von UE-v mithilfe von Windows PowerShell finden Sie unter [Verwalten von UE-v 2. x mit Windows PowerShell und WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md).

    -   **System Center 2012-Konfigurationspaket für Microsoft User Experience Virtualization (UE-v)** – importieren Sie das UE-v-Konfigurationspaket, und befolgen Sie die Konfigurationspaket Dokumentation, um Konfigurationselemente zu erstellen. Weitere Informationen zum UE-v-Konfigurationspaket finden Sie unter [Konfigurieren von UE-v 2. x mit System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).

2.  Bearbeiten Sie die Einstellungen für die folgenden Richtlinien:

    -   **Kontakt mit dem Link Text** – mit dieser Einstellung wird der Text des Links "URL des Kontakts" im Unternehmenseinstellungen-Center angegeben. Wenn Sie diese Einstellung aktivieren, wird im Unternehmenseinstellungen-Center der angegebene Text im Link zur URL des Kontakts angezeigt.

        -   Gruppenrichtlinieneinstellungen: `Contact IT Link Text`

        -   Windows PowerShell-Cmdlet: `ContactITDescription`

        -   Konfigurationselement des Konfigurationspakets: `IT contact descriptive text`

    -   **Kontakt-URL** -diese Einstellung gibt die URL für den Link "Kontakt" im Unternehmens Einstellungs Center in einem gültigen URL-Protokoll an, beispielsweise http://für eine Webseite oder mailto://für eine e-Mail.

        -   Gruppenrichtlinieneinstellungen: `Contact IT URL`

        -   Windows PowerShell-Cmdlet: `ContactITUrl`

        -   Konfigurationselement des Konfigurationspakets: `IT contact URL`

3.  Stellen Sie mithilfe des Verwaltungstools Einstellungen auf den Computern der Benutzer bereit.






 

 





