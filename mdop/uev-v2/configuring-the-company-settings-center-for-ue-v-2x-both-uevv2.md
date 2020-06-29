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
# <span data-ttu-id="3b335-103">Konfigurieren des Unternehmenseinstellungen-Centers für UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="3b335-103">Configuring the Company Settings Center for UE-V 2.x</span></span>


<span data-ttu-id="3b335-104">Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 und 2,1 SP1 beinhalten eine neue Anwendung, das Unternehmenseinstellungen-Center, mit dem Benutzer die Einstellungen für die Synchronisierung verwalten können.</span><span class="sxs-lookup"><span data-stu-id="3b335-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 include a new application, the Company Settings Center, which helps users manage settings to synchronize.</span></span> <span data-ttu-id="3b335-105">Das Unternehmenseinstellungen-Center wird mithilfe des UE-V-Agents installiert.</span><span class="sxs-lookup"><span data-stu-id="3b335-105">The Company Settings Center is installed by using the UE-V Agent.</span></span> <span data-ttu-id="3b335-106">Benutzer greifen auf das Unternehmenseinstellungen-Center in der Systemsteuerung, im **Startmenü** oder auf dem **Start** Bildschirm und über das Symbol "UE-V-Benachrichtigungsbereich" zu.</span><span class="sxs-lookup"><span data-stu-id="3b335-106">Users access the Company Settings Center in Control Panel, in the **Start** menu or on the **Start** screen, and via the UE-V notification area icon.</span></span> <span data-ttu-id="3b335-107">Das Unternehmenseinstellungen-Center zeigt an, welche Einstellungen synchronisiert sind, und hilft Benutzern, den Synchronisierungsstatus von UE-V anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3b335-107">Company Settings Center displays which settings are synchronized and helps users see the synchronization status of UE-V.</span></span> <span data-ttu-id="3b335-108">Benutzer können das Unternehmenseinstellungen-Center verwenden, um auszuwählen, welche Anwendungen oder Windows-Features Ihre Einstellungen zwischen Computern synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="3b335-108">Users can use the Company Settings Center to select which applications or Windows features synchronize their settings between computers.</span></span> <span data-ttu-id="3b335-109">Sie können auch auf die Schaltfläche " **Jetzt synchronisieren** " klicken, um alle Einstellungen sofort zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="3b335-109">They can also click the **Sync Now** button to synchronize all settings immediately.</span></span> <span data-ttu-id="3b335-110">Der Administrator kann auch einen Link zur Unterstützung im Unternehmenseinstellungen-Center hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3b335-110">The administrator can also include a link for support in the Company Settings Center.</span></span>

## <span data-ttu-id="3b335-111">Informationen zum Unternehmenseinstellungen-Center</span><span class="sxs-lookup"><span data-stu-id="3b335-111">About the Company Settings Center</span></span>


<span data-ttu-id="3b335-112">Die Desktopanwendung "Unternehmenseinstellungen Center" bietet Benutzern Informationen zur Synchronisierung der UE-V-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="3b335-112">The Company Settings Center desktop application provides users with information about UE-V settings synchronization.</span></span> <span data-ttu-id="3b335-113">Auf das Unternehmenseinstellungen-Center kann auf verschiedene Arten zugegriffen werden:</span><span class="sxs-lookup"><span data-stu-id="3b335-113">The Company Settings Center is accessible in several different ways:</span></span>

-   <span data-ttu-id="3b335-114">Symbol "Benachrichtigungsbereich" – Wenn die Gruppenrichtlinieneinstellung für das **Taskleistensymbol** oder die Windows PowerShell-Konfiguration aktiviert ist, wird das UE-V-Symbol im Infobereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3b335-114">Notification area icon – With the **Tray Icon** Group Policy setting or Windows PowerShell configuration enabled, the UE-V icon appears in the notification area.</span></span> <span data-ttu-id="3b335-115">Klicken Sie auf das UE-V-Symbol, um das Unternehmenseinstellungen-Center zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3b335-115">Click the UE-V icon to open the Company Settings Center.</span></span>

    <span data-ttu-id="3b335-116">**Hinweis**  Das Symbol für das Infobereich kann mithilfe der folgenden Einstellungen deaktiviert werden:</span><span class="sxs-lookup"><span data-stu-id="3b335-116">**Note** The notification area icon can be disabled by using the following settings:</span></span>

    -   <span data-ttu-id="3b335-117">Gruppenrichtlinieneinstellung:</span><span class="sxs-lookup"><span data-stu-id="3b335-117">Group Policy setting:</span></span> `Policy Tray Icon`

    -   <span data-ttu-id="3b335-118">Windows PowerShell-Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="3b335-118">Windows PowerShell cmdlet:</span></span> `TrayIconEnabled`

    -   <span data-ttu-id="3b335-119">Konfigurationselement im UE-V-Konfigurationspaket für SystemCenter2012 ConfigurationManager:</span><span class="sxs-lookup"><span data-stu-id="3b335-119">Configuration item in the UE-V Configuration Pack for SystemCenter2012 ConfigurationManager:</span></span> `Tray icon enabled`

     

-   <span data-ttu-id="3b335-120">Control Panel-Anwendung – navigieren Sie in der Systemsteuerung zu **Darstellung und Personalisierung**, und klicken Sie dann auf **Unternehmenseinstellungen Center**.</span><span class="sxs-lookup"><span data-stu-id="3b335-120">Control Panel application – In Control Panel, browse to **Appearance and Personalization**, and then click **Company Settings Center**.</span></span>

-   <span data-ttu-id="3b335-121">Erste Verwendung Benachrichtigung – sofern nicht deaktiviert, benachrichtigt der UE-v-Agent den Benutzer, dass die Einstellungen jetzt synchronisiert werden, wenn der UE-v-Agent zum ersten Mal auf einem Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b335-121">First use notification – Unless disabled, the UE-V Agent alerts the user that settings are now synchronized when the UE-V agent runs for the first time on a computer.</span></span> <span data-ttu-id="3b335-122">Klicken Sie auf das Dialogfeld Benachrichtigung, um das Unternehmenseinstellungen-Center zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3b335-122">Click the notification dialog box to open the Company Settings Center.</span></span>

-   <span data-ttu-id="3b335-123">Der **Start** Bildschirm oder das **Startmenü** enthält einen Link zum Unternehmenseinstellungen-Center.</span><span class="sxs-lookup"><span data-stu-id="3b335-123">The **Start** screen or **Start** menu includes a link to the Company Settings Center.</span></span> <span data-ttu-id="3b335-124">Eine Suche nach dem Unternehmenseinstellungen-Center findet die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3b335-124">A search for Company Settings Center finds the application.</span></span>

## <span data-ttu-id="3b335-125">Konfigurieren des Support-Links im Unternehmenseinstellungen-Center</span><span class="sxs-lookup"><span data-stu-id="3b335-125">Configuring the support link in the Company Settings Center</span></span>


<span data-ttu-id="3b335-126">Das Unternehmenseinstellungen-Center kann einen Hyperlink enthalten, auf den Benutzer klicken können, um Unterstützung bei Synchronisierungsproblemen mit UE-V-Einstellungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3b335-126">The Company Settings Center can include a hyperlink that users can click to get support with UE-V settings synchronization problems.</span></span> <span data-ttu-id="3b335-127">Dieser Link kann ein beliebiges gültiges URL-Protokoll öffnen, beispielsweise http://für eine Webseite oder mailto://für eine e-Mail.</span><span class="sxs-lookup"><span data-stu-id="3b335-127">This link can open any valid URL protocol, such as http:// for a webpage or mailto:// for an email.</span></span> <span data-ttu-id="3b335-128">Der Support-Link kann mithilfe von Gruppenrichtlinien, Windows PowerShell oder dem System Center 2012 Configuration Manager UE-V-Konfigurationspaket konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="3b335-128">The support link can be configured by using Group Policy, Windows PowerShell, or the System Center 2012 Configuration Manager UE-V Configuration Pack.</span></span>

**<span data-ttu-id="3b335-129">Konfigurieren des Support Links für das Unternehmenseinstellungen-Center</span><span class="sxs-lookup"><span data-stu-id="3b335-129">How to configure the Company Settings Center support link</span></span>**

1.  <span data-ttu-id="3b335-130">Öffnen Sie Ihr bevorzugtes Verwaltungstool:</span><span class="sxs-lookup"><span data-stu-id="3b335-130">Open your preferred management tool:</span></span>

    -   <span data-ttu-id="3b335-131">**Gruppenrichtlinie** – Wenn Sie dies noch nicht getan haben, laden Sie die ADMX-Vorlage für UE-V 2 aus [MDOP administrative Vorlagen](https://go.microsoft.com/fwlink/p/?LinkId=393941)herunter.</span><span class="sxs-lookup"><span data-stu-id="3b335-131">**Group Policy** - If you have not already done so, download the ADMX template for UE-V 2 from [MDOP Administrative Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941).</span></span>

    -   <span data-ttu-id="3b335-132">**Windows PowerShell** – öffnen Sie **Windows PowerShell**auf einem Computer, auf dem der UE-V-Agent installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3b335-132">**Windows PowerShell** – On a computer with the UE-V Agent installed, open **Windows PowerShell**.</span></span> <span data-ttu-id="3b335-133">Weitere Informationen zum Verwalten von UE-v mithilfe von Windows PowerShell finden Sie unter [Verwalten von UE-v 2. x mit Windows PowerShell und WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="3b335-133">For more information about administering UE-V by using Windows PowerShell, see [Administering UE-V 2.x with Windows PowerShell and WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md).</span></span>

    -   <span data-ttu-id="3b335-134">**System Center 2012-Konfigurationspaket für Microsoft User Experience Virtualization (UE-v)** – importieren Sie das UE-v-Konfigurationspaket, und befolgen Sie die Konfigurationspaket Dokumentation, um Konfigurationselemente zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3b335-134">**System Center 2012 Configuration Pack for Microsoft User Experience Virtualization (UE-V)** – Import the UE-V Configuration Pack and follow the Configuration Pack documentation to create configuration items.</span></span> <span data-ttu-id="3b335-135">Weitere Informationen zum UE-v-Konfigurationspaket finden Sie unter [Konfigurieren von UE-v 2. x mit System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="3b335-135">For more information about the UE-V Configuration Pack, see [Configuring UE-V 2.x with System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span></span>

2.  <span data-ttu-id="3b335-136">Bearbeiten Sie die Einstellungen für die folgenden Richtlinien:</span><span class="sxs-lookup"><span data-stu-id="3b335-136">Edit the settings for the following policies:</span></span>

    -   <span data-ttu-id="3b335-137">**Kontakt mit dem Link Text** – mit dieser Einstellung wird der Text des Links "URL des Kontakts" im Unternehmenseinstellungen-Center angegeben.</span><span class="sxs-lookup"><span data-stu-id="3b335-137">**Contact IT Link Text** - This setting specifies the text of the Contact IT URL hyperlink in the Company Settings Center.</span></span> <span data-ttu-id="3b335-138">Wenn Sie diese Einstellung aktivieren, wird im Unternehmenseinstellungen-Center der angegebene Text im Link zur URL des Kontakts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3b335-138">If you enable this setting, the Company Settings Center displays the specified text in the link to the Contact IT URL.</span></span>

        -   <span data-ttu-id="3b335-139">Gruppenrichtlinieneinstellungen:</span><span class="sxs-lookup"><span data-stu-id="3b335-139">Group Policy settings:</span></span> `Contact IT Link Text`

        -   <span data-ttu-id="3b335-140">Windows PowerShell-Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="3b335-140">Windows PowerShell cmdlet:</span></span> `ContactITDescription`

        -   <span data-ttu-id="3b335-141">Konfigurationselement des Konfigurationspakets:</span><span class="sxs-lookup"><span data-stu-id="3b335-141">Configuration Pack configuration item:</span></span> `IT contact descriptive text`

    -   <span data-ttu-id="3b335-142">**Kontakt-URL** -diese Einstellung gibt die URL für den Link "Kontakt" im Unternehmens Einstellungs Center in einem gültigen URL-Protokoll an, beispielsweise http://für eine Webseite oder mailto://für eine e-Mail.</span><span class="sxs-lookup"><span data-stu-id="3b335-142">**Contact IT URL** - This setting specifies the URL for the Contact IT link in the Company Settings Center in a valid URL protocol, such as http:// for a webpage or mailto:// for an email.</span></span>

        -   <span data-ttu-id="3b335-143">Gruppenrichtlinieneinstellungen:</span><span class="sxs-lookup"><span data-stu-id="3b335-143">Group Policy settings:</span></span> `Contact IT URL`

        -   <span data-ttu-id="3b335-144">Windows PowerShell-Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="3b335-144">Windows PowerShell cmdlet:</span></span> `ContactITUrl`

        -   <span data-ttu-id="3b335-145">Konfigurationselement des Konfigurationspakets:</span><span class="sxs-lookup"><span data-stu-id="3b335-145">Configuration Pack configuration item:</span></span> `IT contact URL`

3.  <span data-ttu-id="3b335-146">Stellen Sie mithilfe des Verwaltungstools Einstellungen auf den Computern der Benutzer bereit.</span><span class="sxs-lookup"><span data-stu-id="3b335-146">Deploy settings to users’ computers by using the management tool.</span></span>






 

 





