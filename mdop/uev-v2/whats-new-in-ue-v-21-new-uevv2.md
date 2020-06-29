---
title: Neuigkeiten in UE-V 2.1
description: Neuigkeiten in UE-V 2.1
author: dansimp
ms.assetid: 7f385183-7d97-4602-b19a-baa710334ade
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7816fc8309a29347048172b2104750140c483587
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811650"
---
# <span data-ttu-id="6e8b9-103">Neuigkeiten in UE-V 2.1</span><span class="sxs-lookup"><span data-stu-id="6e8b9-103">What's New in UE-V 2.1</span></span>


<span data-ttu-id="6e8b9-104">Die User Experience Virtualization 2,1 stellt diese neuen Features und Funktionen im Vergleich zu UE-V 2,0 zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-104">User Experience Virtualization 2.1 provides these new features and functionality compared to UE-V 2.0.</span></span> <span data-ttu-id="6e8b9-105">Die [Microsoft User Experience Virtualization (UE-v) 2,1-Versionshinweise](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md) bieten weitere Informationen zur Version UE-v 2,1.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-105">The [Microsoft User Experience Virtualization (UE-V) 2.1 Release Notes](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md) provide more information about the UE-V 2.1 release.</span></span>

## <span data-ttu-id="6e8b9-106">Office 2013-Einstellungen, Speicherort Vorlage</span><span class="sxs-lookup"><span data-stu-id="6e8b9-106">Office 2013 Settings Location Template</span></span>


<span data-ttu-id="6e8b9-107">UE-V 2,1 enthält die Vorlage für Microsoft Office 2013-Einstellungen mit verbesserter Unterstützung für Outlook-Signaturen.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-107">UE-V 2.1 includes the Microsoft Office 2013 settings location template with improved Outlook signature support.</span></span> <span data-ttu-id="6e8b9-108">In UE-V 2,1 werden die Signaturdaten zwischen Benutzergeräten synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-108">In UE-V 2.1, the signature data synchronizes between user devices.</span></span> <span data-ttu-id="6e8b9-109">Wir haben die Synchronisierung von standardmäßigen Signatureinstellungen für neue, Antworten und weitergeleitete e-Mails hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-109">We’ve added synchronization of default signature settings for new, reply, and forwarded emails.</span></span> <span data-ttu-id="6e8b9-110">Kunden müssen die standardmäßigen Signatureinstellungen nicht mehr auswählen.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-110">Customers no longer have to choose the default signature settings.</span></span>

<span data-ttu-id="6e8b9-111">**Hinweis**  Für jedes Gerät, auf dem ein Benutzer seine Outlook-Signatur synchronisieren möchte, muss ein Outlook-Profil erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-111">**Note** An Outlook profile must be created for any device on which a user wants to sync their Outlook signature.</span></span> <span data-ttu-id="6e8b9-112">Wenn das Profil noch nicht erstellt wurde, kann der Benutzer eine erstellen und dann Outlook auf diesem Gerät neu starten, um die Signatur Synchronisierung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-112">If the profile is not already created, the user can create one and then restart Outlook on that device to enable signature synchronization.</span></span>

 

<span data-ttu-id="6e8b9-113">Zuvor enthielt UE-v die Microsoft Office 2010-Einstellungen für Standort Vorlagen, die automatisch verteilt und beim UE-v-Agent registriert wurden.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-113">Previously UE-V included Microsoft Office 2010 settings location templates that were automatically distributed and registered with the UE-V Agent.</span></span> <span data-ttu-id="6e8b9-114">UE-V 2,1 arbeitet mit Office 365, um festzustellen, ob die Office 2013-Einstellungen von Office 365 durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-114">UE-V 2.1 works with Office 365 to determine whether Office 2013 settings are roamed by Office 365.</span></span> <span data-ttu-id="6e8b9-115">Wenn die Einstellungen von Office 365 durchlaufen werden, werden Sie nicht von UE-V durchsucht.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-115">If settings are roamed by Office 365 they are not roamed by UE-V.</span></span> <span data-ttu-id="6e8b9-116">Eine Übersicht über die [Einstellungen für Benutzer und Roaming für Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) bietet weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-116">[Overview of user and roaming settings for Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) provides more information.</span></span>

<span data-ttu-id="6e8b9-117">Führen Sie eine der folgenden Aktionen aus, um die Synchronisierung von Einstellungen mithilfe von UE-V 2,1 zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="6e8b9-117">To enable settings synchronization using UE-V 2.1, do one of the following:</span></span>

-   <span data-ttu-id="6e8b9-118">Verwenden von Gruppenrichtlinien zum Deaktivieren der Office 365-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="6e8b9-118">Use Group Policy to disable Office 365 synchronization</span></span>

-   <span data-ttu-id="6e8b9-119">Aktivieren der Office 365-Synchronisierungs Erfahrung während der Installation von Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e8b9-119">Do not enable the Office 365 synchronization experience during Office 2013 installation</span></span>

<span data-ttu-id="6e8b9-120">UE-V 2,1 liefert [Office 2013-und Office 2010-Vorlagen](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="6e8b9-120">UE-V 2.1 ships [Office 2013 and Office 2010 templates](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span></span> <span data-ttu-id="6e8b9-121">Diese Version entfernt die Office 2007-Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-121">This release removes the Office 2007 templates.</span></span> <span data-ttu-id="6e8b9-122">Benutzer können weiterhin Office 2007-Vorlagen aus UE-v 2,0 oder früheren Versionen verwenden und können weiterhin die Vorlagen aus dem [hier](https://go.microsoft.com/fwlink/p/?LinkID=246589)befindlichen UE-v-Vorlagenkatalog abrufen.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-122">Users can still use Office 2007 templates from UE-V 2.0 or earlier and can still get the templates from the UE-V template gallery located [here](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span>

## <span data-ttu-id="6e8b9-123">Fix für Benutzer von verteilten Datei System-Namespaces</span><span class="sxs-lookup"><span data-stu-id="6e8b9-123">Fix for Distributed File System Namespace Users</span></span>


<span data-ttu-id="6e8b9-124">UE-v hat eine verbesserte Unterstützung für Distributed File System Namespace (DFSN) durch Hinzufügen einer UE-v-Konfiguration mit dem Namen SyncProviderPingEnabled.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-124">UE-V has improved Distributed File System Namespace (DFSN) support by adding a UE-V configuration called SyncProviderPingEnabled.</span></span> <span data-ttu-id="6e8b9-125">Durch das Deaktivieren dieser Konfiguration mithilfe von PowerShell oder WMI können Benutzer den UE-V-Ping deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-125">Disabling this configuration using PowerShell or WMI allows users to disable the UE-V ping.</span></span> <span data-ttu-id="6e8b9-126">Der UE-V-Ping verursacht einen Fehler bei der Verwendung von DFSN-Servern, da diese Server nicht auf Pings reagieren.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-126">The UE-V ping causes an error when using DFSN servers because these servers do not respond to pings.</span></span> <span data-ttu-id="6e8b9-127">Die nicht Antwort verhindert, dass UE-V die Einstellungen synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-127">The non-response prevents UE-V from synchronizing settings.</span></span> <span data-ttu-id="6e8b9-128">Durch Deaktivieren des UE-v-Pings kann die UE-v-Synchronisierung normal funktionieren.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-128">Disabling the UE-V ping allows UE-V synchronization to work normally.</span></span>

<span data-ttu-id="6e8b9-129">Verwenden Sie dieses PowerShell-Cmdlet, um UE-V-Ping zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="6e8b9-129">To disable UE-V ping, use this PowerShell cmdlet:</span></span>

``` syntax
Set-UevConfiguration -DisableSyncProviderPing
```

## <span data-ttu-id="6e8b9-130">Synchronisierung für Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="6e8b9-130">Synchronization for Credentials</span></span>


<span data-ttu-id="6e8b9-131">UE-V 2,1 bietet Kunden die Möglichkeit, die im Windows-Anmelde Informations-Manager gespeicherten Anmeldeinformationen und Zertifikate zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-131">UE-V 2.1 gives customers the ability to synchronize credentials and certificates stored in the Windows Credential Manager.</span></span> <span data-ttu-id="6e8b9-132">Diese Komponente ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-132">This component is disabled by default.</span></span> <span data-ttu-id="6e8b9-133">Wenn Sie diese Komponente aktivieren, können Benutzer ihre Domänenanmeldeinformationen und Zertifikate synchron halten. Benutzer können sich einmal auf einem Gerät anmelden, und diese Anmeldeinformationen werden für diesen Benutzer auf allen ihren UE-V-fähigen Geräten gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-133">Enabling this component lets users keep their domain credentials and certificates in sync. Users can sign in one time on a device, and these credentials will roam for that user across all of their UE-V enabled devices.</span></span> <span data-ttu-id="6e8b9-134">[Zum Verwalten von Anmeldeinformationen mit UE-V 2,1](https://technet.microsoft.com/library/dn458932.aspx#creds) finden Sie weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-134">[Manage Credentials with UE-V 2.1](https://technet.microsoft.com/library/dn458932.aspx#creds) provides more information.</span></span>

<span data-ttu-id="6e8b9-135">**Hinweis**  In Windows 8 und höher enthält der Anmelde Informations-Manager webanmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-135">**Note** In Windows 8 and later, Credential Manager contains web credentials.</span></span> <span data-ttu-id="6e8b9-136">Diese Anmeldeinformationen werden nicht zwischen den Geräten der Benutzer synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-136">These credentials are not synchronized between users’ devices.</span></span>

 

## <span data-ttu-id="6e8b9-137">UE-V und Microsoft-Konto Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="6e8b9-137">UE-V and Microsoft Account Synchronization</span></span>


<span data-ttu-id="6e8b9-138">UE-V erkennt, ob "Synchronisierungseinstellungen mit OneDrive", auch bekannt als Microsoft-Konto Synchronisierung, aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-138">UE-V detects if “Sync settings with OneDrive”, also known as Microsoft Account synchronization, is on.</span></span> <span data-ttu-id="6e8b9-139">Wenn das Microsoft-Konto nicht für die Synchronisierung von Einstellungen konfiguriert ist, synchronisiert UE-V Windows-apps, AppX-Pakete und Windows-Desktopeinstellungen zwischen Geräten.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-139">If the Microsoft Account is not configured to synchronize settings, UE-V synchronizes Windows apps, AppX packages, and Windows desktop settings between devices.</span></span> <span data-ttu-id="6e8b9-140">Auf diese Weise können Benutzer auf Ihre Store-Apps, Musik, Bilder und andere Microsoft-Konto fähige Anwendungen zugreifen, ohne die Synchronisierung außerhalb der Unternehmensfirewall zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-140">This lets users access their Store apps, music, pictures and other Microsoft Account-enabled applications without syncing outside of the enterprise firewall.</span></span> <span data-ttu-id="6e8b9-141">UE-V überprüft, ob Gruppenrichtlinien die Synchronisierung von Einstellungen mit OneDrive beenden oder ob der Benutzer die **Synchronisierung Ihrer Einstellungen auf diesem Computer** in den Benutzersteuerelementen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-141">UE-V checks whether Group Policy will stop synchronizing settings with OneDrive or if the user disables **Sync your settings on this computer** in the user controls.</span></span>

## <span data-ttu-id="6e8b9-142">Unterstützung für das SyncMethod extern</span><span class="sxs-lookup"><span data-stu-id="6e8b9-142">Support for the SyncMethod External</span></span>


<span data-ttu-id="6e8b9-143">Eine neue [SyncMethod-Konfiguration](https://technet.microsoft.com/library/dn554321.aspx) mit dem Namen **External** gibt an, dass wenn UE-V-Einstellungen in einen lokalen Ordner auf dem Benutzer Computer geschrieben werden, dann ein externes Synchronisierungsmodul (wie OneDrive for Business, Arbeitsordner, SharePoint oder Dropbox) verwendet werden kann, um diese Einstellungen auf die verschiedenen Computer anzuwenden, auf die Benutzer zugreifen.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-143">A new [SyncMethod configuration](https://technet.microsoft.com/library/dn554321.aspx) called **External** specifies that if UE-V settings are written to a local folder on the user computer, then any external sync engine (such as OneDrive for Business, Work Folders, Sharepoint, or Dropbox) can be used to apply these settings to the different computers that users access.</span></span>

## <span data-ttu-id="6e8b9-144">Verbesserte Unterstützung für den VDI-Modus</span><span class="sxs-lookup"><span data-stu-id="6e8b9-144">Enhanced Support for VDI Mode</span></span>


<span data-ttu-id="6e8b9-145">UE-V 2,1 umfasst [Unterstützung für VDI-Sitzungen](https://technet.microsoft.com/library/dn458932.aspx#vdi) , die von Endbenutzern freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-145">UE-V 2.1 includes [support for VDI sessions](https://technet.microsoft.com/library/dn458932.aspx#vdi) that are shared among end users.</span></span> <span data-ttu-id="6e8b9-146">Als Administrator können Sie eine spezielle VDI-Vorlage registrieren und konfigurieren, die sicherstellt, dass UE-V alle Funktionen für nicht persistente VDI-Sitzungen intakt hält.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-146">As an administrator, you can register and configure a special VDI template, which ensures that UE-V keeps all of its functionality intact for non-persistent VDI sessions.</span></span>

<span data-ttu-id="6e8b9-147">**Hinweis**  Wenn Sie den VDI-Modus nicht für nicht persistente VDI-Sitzungen aktivieren, funktionieren bestimmte Features nicht, beispielsweise die Datensicherung/-Wiederherstellung und LKG.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-147">**Note** If you do not enable VDI mode for non-persistent VDI sessions, certain features do not work, such as back-up/restore and LKG.</span></span>

 

## <span data-ttu-id="6e8b9-148">Administrative Sicherung und Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="6e8b9-148">Administrative Backup and Restore</span></span>


<span data-ttu-id="6e8b9-149">Sie können zusätzliche Einstellungen wiederherstellen, wenn ein Benutzer ein neues Gerät annimmt, indem Sie eine Vorlage für die Einstellungsposition im **Backup** -oder Roam-Profil **(Standard)** mithilfe des PowerShell-Cmdlets "UevTemplateProfile" festlegen.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-149">You can restore additional settings when a user adopts a new device by putting a settings location template in **backup** or **roam (default)** profile using the Set-UevTemplateProfile PowerShell cmdlet.</span></span> <span data-ttu-id="6e8b9-150">Auf diese Weise können Computereinstellungen zusätzlich zu den Benutzereinstellungen mit dem neuen Computer synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-150">This lets computer settings sync to the new computer, in addition to user settings.</span></span> <span data-ttu-id="6e8b9-151">Vorlagen, die dem Sicherungsprofil zugewiesen sind, werden für dieses Gerät gesichert und auf Gerätebasis konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-151">Templates assigned to the backup profile are backed up for that device and configured on a per-device basis.</span></span> <span data-ttu-id="6e8b9-152">Das [Verwalten von Verwaltungs-Backup und-Wiederherstellung in UE-V 2. x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md) enthält weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-152">[Manage Administrative Backup and Restore in UE-V 2.x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md) provides more information.</span></span>

## <span data-ttu-id="6e8b9-153">Synchronisierung für zusätzliche Windows-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="6e8b9-153">Synchronization for Additional Windows Settings</span></span>


<span data-ttu-id="6e8b9-154">UE-V synchronisiert nun die Personalisierung von Touchscreen-Tastaturen, das Rechtschreibwörterbuch und ermöglicht die APP-Umschaltung für aktuelle apps und Einstellungen für den Bildschirmrand, um zwischen Windows 8-und Windows 8,1-Geräten zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="6e8b9-154">UE-V now synchronizes touch keyboard personalization, the spelling dictionary, and enables the App Switching for recent apps and screen edge settings to synchronize between Windows 8 and Windows 8.1 devices.</span></span>






## <span data-ttu-id="6e8b9-155">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="6e8b9-155">Related topics</span></span>


[<span data-ttu-id="6e8b9-156">Erste Schritte mit UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="6e8b9-156">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="6e8b9-157">Vorbereiten einer UE-V 2. x-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="6e8b9-157">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="6e8b9-158">Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.1</span><span class="sxs-lookup"><span data-stu-id="6e8b9-158">Microsoft User Experience Virtualization (UE-V) 2.1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

 

 





