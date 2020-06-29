---
title: Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.0
description: Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.0
author: dansimp
ms.assetid: 5ef66cd1-ba2b-4383-9f45-e7cde41f1ba1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad3deffa5cd567a70711e5447197e630f04ea254
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811062"
---
# <span data-ttu-id="ad5b2-103">Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.0</span><span class="sxs-lookup"><span data-stu-id="ad5b2-103">Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes</span></span>


<span data-ttu-id="ad5b2-104">Drücken Sie STRG + F, um die Microsoft User Experience Virtualization (UE-V) 2,0-Versionshinweise zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-104">To search Microsoft User Experience Virtualization (UE-V) 2.0 release notes, press Ctrl+F.</span></span>

<span data-ttu-id="ad5b2-105">Lesen Sie diese Versionshinweise gründlich, bevor Sie UE-V installieren.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="ad5b2-106">Die Anmerkungen zu dieser Version enthalten Informationen, die erforderlich sind, um die Virtualisierung der Benutzeroberfläche erfolgreich zu installieren, und zusätzliche Informationen enthalten, die in der Produktdokumentation nicht zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="ad5b2-107">Wenn es Unterschiede zwischen diesen Versionshinweisen und anderen UE-V-Dokumentationen gibt, sollte die neueste Änderung als autorisierend angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="ad5b2-108">Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="ad5b2-109">Abgeben von Feedback</span><span class="sxs-lookup"><span data-stu-id="ad5b2-109">Providing feedback</span></span>


<span data-ttu-id="ad5b2-110">Teilen Sie uns Ihre Meinung zu unserer Dokumentation zu MDOP mit, indem Sie uns Feedback und Kommentare geben.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-110">Tell us what you think about our documentation for MDOP by giving us your feedback and comments.</span></span> <span data-ttu-id="ad5b2-111">Senden Sie Ihr Feedback zur Dokumentation an [mdopdocs@Microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span><span class="sxs-lookup"><span data-stu-id="ad5b2-111">Send your documentation feedback to [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span></span>

## <span data-ttu-id="ad5b2-112">Bekannte Probleme in UE-V</span><span class="sxs-lookup"><span data-stu-id="ad5b2-112">UE-V known issues</span></span>


<span data-ttu-id="ad5b2-113">Dieser Abschnitt enthält Anmerkungen zu dieser Version für die Virtualisierung der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-113">This section contains release notes for User Experience Virtualization.</span></span>

### <span data-ttu-id="ad5b2-114">Registrierungseinstellungen werden nicht zwischen App-V und systemeigenen Anwendungen auf demselben Computer synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-114">Registry settings do not synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="ad5b2-115">Wenn ein Computer über eine Anwendung verfügt, die über Application Virtualization (App-V) und eine lokal mit einer Windows Installer-Datei (MSI) installiert ist, werden die registrierungsbasierten Einstellungen nicht zwischen den Technologien synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-115">When a computer has an application that is installed through both Application Virtualization (App-V) and a locally with a Windows Installer (.msi) file, the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="ad5b2-116">**Problemumgehung:** Um dieses Problem zu beheben, führen Sie die Anwendung aus, indem Sie eine der beiden Technologien auswählen, aber nicht beide.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-116">**WORKAROUND:** To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <a href="" id="settings-do-not-synchronization-when-network-share-is-outside-user-s-domain"></a><span data-ttu-id="ad5b2-117">Einstellungen werden nicht synchronisiert, wenn die Netzwerkfreigabe außerhalb der Benutzerdomäne liegt</span><span class="sxs-lookup"><span data-stu-id="ad5b2-117">Settings do not synchronization when network share is outside user’s domain</span></span>

<span data-ttu-id="ad5b2-118">Wenn Windows® 8 die Synchronisierung der Betriebssystem Einstellungen versucht, schlägt die Synchronisierung mit der folgenden Fehlermeldung fehl: **Boost:: File System:: EXISTS:: Falscher Benutzername oder Kennwort**.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-118">When Windows® 8 attempts operating system settings synchronization, the synchronization fails with the following error message: **boost::filesystem::exists::Incorrect user name or password**.</span></span> <span data-ttu-id="ad5b2-119">Dieser Fehler kann darauf hindeuten, dass sich die Netzwerkfreigabe außerhalb der Domäne des Benutzers oder einer Domäne mit einer Vertrauensstellung zu dieser Domäne befindet.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-119">This error can indicate that the network share is outside the user’s domain or a domain with a trust relationship to that domain.</span></span> <span data-ttu-id="ad5b2-120">Wenn Sie nach Betriebsprotokoll Ereignissen suchen möchten, öffnen Sie die **Ereignisanzeige** , und navigieren Sie zu **Anwendungen und Dienstprotokolle**, die  /  **Microsoft**  /  **User Experience Virtualization**-  /  **Protokollierung**in  /  **Betrieb**sind.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-120">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span> <span data-ttu-id="ad5b2-121">Netzwerkfreigaben, die für die Speicherorte der UE-V-Einstellungen verwendet werden, sollten sich in derselben Active Directory-Domäne wie der Benutzer oder einer vertrauenswürdigen Domäne der Domäne des Benutzers befinden.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-121">Network shares that are used for UE-V settings storage locations should reside in the same Active Directory domain as the user or a trusted domain of the user’s domain.</span></span>

<span data-ttu-id="ad5b2-122">**Problemumgehung:** Verwenden Sie Netzwerkfreigaben aus derselben Active Directory-Domäne wie der Benutzer.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-122">**WORKAROUND:** Use network shares from the same Active Directory domain as the user.</span></span>

### <span data-ttu-id="ad5b2-123">Unvorhersehbare Ergebnisse mit installiertem Office 2010 und Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad5b2-123">Unpredictable results with both Office 2010 and Office 2013 installed</span></span>

<span data-ttu-id="ad5b2-124">Wenn ein Benutzer sowohl Office 2010 als auch Office 2013 installiert hat, werden alle gängigen Einstellungen zwischen den beiden Office-Versionen von UE-V durchsucht.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-124">When a user has both Office 2010 and Office 2013 installed, any common settings between the two versions of Office are roamed by UE-V.</span></span> <span data-ttu-id="ad5b2-125">Dies kann dazu führen, dass die Größe des Office 2010-Pakets recht groß ist oder zu unvorhersehbaren Konflikten mit 2013 führt, insbesondere dann, wenn Office 365 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-125">This could cause the Office 2010 package size to be quite large or result in unpredictable conflicts with 2013, particularly if Office 365 is used.</span></span>

<span data-ttu-id="ad5b2-126">**Problemumgehung:** Installieren Sie nur eine Version von Office, oder begrenzen Sie, welche Einstellungen von UE-V synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-126">**WORKAROUND:** Install only one version of Office or limit which settings are synchronized by UE-V.</span></span>

### <span data-ttu-id="ad5b2-127">Deinstallieren und erneutes Installieren der Windows 8-App kehrt Einstellungen in den Anfangszustand zurück</span><span class="sxs-lookup"><span data-stu-id="ad5b2-127">Uninstall and re-install of Windows 8 app reverts settings to initial state</span></span>

<span data-ttu-id="ad5b2-128">Bei Verwendung der UE-V-Synchronisierungseinstellungen für eine Windows 8-App werden die Einstellungen der APP wieder auf die Standardwerte zurückgesetzt, wenn der Benutzer die APP deinstalliert und die APP dann neu installiert.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-128">While using UE-V settings synchronization for a Windows 8 app, if the user uninstalls the app and then reinstalls the app, the app’s settings revert to their default values.</span></span><span data-ttu-id="ad5b2-129">Dies geschieht, weil die Deinstallation die lokale (zwischengespeicherte) Kopie der App-Einstellungen entfernt, aber nicht das lokale UE-V-Einstellungspaket entfernt.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-129"> This happens because the uninstall removes the local (cached) copy of the app’s settings but does not remove the local UE-V settings package.</span></span><span data-ttu-id="ad5b2-130">Wenn die APP neu installiert und gestartet wird, sammeln UE-V die App-Einstellungen, die auf die APP-Standardeinstellungen zurückgesetzt wurden, und laden dann die Standardeinstellungen an den zentralen Speicherort hoch.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-130"> When the app is reinstalled and launched, UE-V gather the app settings that were reset to the app defaults and then uploads the default settings to the central storage location.</span></span><span data-ttu-id="ad5b2-131">Auf anderen Computern, auf denen die app ausgeführt wird, werden die Standardeinstellungen heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-131"> Other computers running the app then download the default settings.</span></span><span data-ttu-id="ad5b2-132">Dieses Verhalten ist mit dem Verhalten von Desktopanwendungen identisch.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-132"> This behavior is identical to the behavior of desktop applications.</span></span>

<span data-ttu-id="ad5b2-133">**Problemumgehung:** Keine.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-133">**WORKAROUND:** None.</span></span>

### <span data-ttu-id="ad5b2-134">E-Mail-Signatur-Roaming für Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="ad5b2-134">Email signature roaming for Outlook 2010</span></span>

<span data-ttu-id="ad5b2-135">UE-V durchstreift die Outlook 2010-Signaturdateien zwischen Geräten.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-135">UE-V will roam the Outlook 2010 signature files between devices.</span></span> <span data-ttu-id="ad5b2-136">Die standardmäßigen Signaturoptionen für neue Nachrichten und Antworten oder Weiterleitungen werden jedoch nicht synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-136">However, the default signature options for new messages and replies or forwards are not synchronized.</span></span> <span data-ttu-id="ad5b2-137">Diese beiden Einstellungen werden im Outlook-Profil gespeichert, das UE-V nicht durchwandert.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-137">These two settings are stored in the Outlook profile, which UE-V does not roam.</span></span>

<span data-ttu-id="ad5b2-138">**Problemumgehung:** Keine.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-138">**WORKAROUND:** None.</span></span>

### <span data-ttu-id="ad5b2-139">UE-V unterstützt keine Roamingeinstellungen zwischen 32-Bit-und 64-Bit-Versionen von Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-139">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="ad5b2-140">Wir empfehlen, dass Sie die 64-Bit-Version von Microsoft Office für moderne Computer installieren.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-140">We recommend that you install the 64-bit version of Microsoft Office for modern computers.</span></span> <span data-ttu-id="ad5b2-141">Wenn Sie feststellen möchten, welche Version Sie benötigen, [Klicken Sie hier](https://support.office.com/article/choose-between-the-64-bit-or-32-bit-version-of-office-2dee7807-8f95-4d0c-b5fe-6c6f49b8d261?ui=en-US&rs=en-US&ad=US#32or64Bit=Newer_Versions).</span><span class="sxs-lookup"><span data-stu-id="ad5b2-141">To determine which version you need, [click here](https://support.office.com/article/choose-between-the-64-bit-or-32-bit-version-of-office-2dee7807-8f95-4d0c-b5fe-6c6f49b8d261?ui=en-US&rs=en-US&ad=US#32or64Bit=Newer_Versions).</span></span> <span data-ttu-id="ad5b2-142">UE-V unterstützt Roamingeinstellungen zwischen identischen Architekturversionen von Office.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-142">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="ad5b2-143">Beispielsweise werden die Office-Einstellungen für 32-Bit zwischen allen 32-Bit-Office-Instanzen durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-143">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="ad5b2-144">UE-V unterstützt keine Roamingeinstellungen zwischen 32-Bit-und 64-Bit-Versionen von Office.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-144">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="ad5b2-145">**Problemumgehung:** Keine</span><span class="sxs-lookup"><span data-stu-id="ad5b2-145">**WORKAROUND:** None</span></span>

### <a href="" id="msi-s-are-not-localized"></a><span data-ttu-id="ad5b2-146">MSI-Versionen sind nicht lokalisiert</span><span class="sxs-lookup"><span data-stu-id="ad5b2-146">MSI’s are not localized</span></span>

<span data-ttu-id="ad5b2-147">UE-v 2,0 umfasst ein lokalisiertes Setupprogramm für den UE-v-Agent und den UE-v-Generator.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-147">UE-V 2.0 includes a localized setup program for both the UE-V Agent and UE-V generator.</span></span> <span data-ttu-id="ad5b2-148">Diese MSI-Dateien sind weiterhin verfügbar, die Benutzeroberfläche wird jedoch minimiert, und die MSI-Datei wird nur in Englisch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-148">These MSI files are still available but the user interface is minimized and the MSI’s only display in English.</span></span> <span data-ttu-id="ad5b2-149">Obwohl die Datei in Englisch ist, werden alle unterstützten Sprachen während der Installation von dem Setup-Programm installiert.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-149">Despite the file being in English, the setup program installs all supported languages during the installation.</span></span>

<span data-ttu-id="ad5b2-150">**Problemumgehung:** Keine</span><span class="sxs-lookup"><span data-stu-id="ad5b2-150">**WORKAROUND:** None</span></span>

### <span data-ttu-id="ad5b2-151">Favicons, die mit Internet Explorer 9-Favoriten verknüpft sind, werden nicht durchwandert</span><span class="sxs-lookup"><span data-stu-id="ad5b2-151">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="ad5b2-152">Die Favicons, die mit Internet Explorer 9-Favoriten verknüpft sind, werden nicht von der Benutzeroberflächen-Virtualisierung durchlaufen und nicht angezeigt, wenn die Favoriten auf einem neuen Computer erstmalig angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-152">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="ad5b2-153">**Problemumgehung:** Favicons werden mit den zugehörigen Favoriten angezeigt, sobald die Textmarke verwendet und im Internet Explorer 9-Browser zwischengespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-153">**WORKAROUND:** Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="ad5b2-154">Datei Einstellungs Pfade werden in der Registrierung gespeichert</span><span class="sxs-lookup"><span data-stu-id="ad5b2-154">File settings paths are stored in registry</span></span>

<span data-ttu-id="ad5b2-155">In einigen Anwendungseinstellungen werden die Pfade Ihrer Konfigurations-und Einstellungsdateien als Werte in der Registrierung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-155">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="ad5b2-156">Die Dateien, die als Pfade in der Registrierung referenziert werden, müssen synchronisiert werden, wenn die Einstellungen zwischen Computern durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-156">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="ad5b2-157">**Problemumgehung:** Verwenden Sie die Ordnerumleitung oder eine andere Technologie, um sicherzustellen, dass alle Dateien, auf die als Pfad für Datei Einstellungen verwiesen wird, vorhanden sind und sich auf allen Computern, auf denen die Einstellungen durchlaufen, an demselben Speicherort befinden.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-157">**WORKAROUND:** Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="ad5b2-158">Lange Einstellungen Speicherpfade können einen Fehler verursachen</span><span class="sxs-lookup"><span data-stu-id="ad5b2-158">Long Settings Storage Paths could cause an error</span></span>

<span data-ttu-id="ad5b2-159">Behalten Sie die Einstellungen für den Speicherpfad so kurz wie möglich.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-159">Keep settings storage paths as short as possible.</span></span> <span data-ttu-id="ad5b2-160">Lange Pfade können die Auflösung oder Synchronisierung verhindern.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-160">Long paths could prevent resolution or synchronization.</span></span> <span data-ttu-id="ad5b2-161">UE-V verwendet den Einstellungsspeicher Pfad als Teil des berechneten Pfads zum Speichern von Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-161">UE-V uses the Settings storage path as part of the calculated path to store settings.</span></span> <span data-ttu-id="ad5b2-162">Dieser Pfad wird folgendermaßen berechnet: Einstellungsspeicher Pfad + "settingspackages" + Paket dir (Vorlagen-ID) + Paketname (Vorlagen-ID) +. pkgx.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-162">That path is calculated in the following way: settings storage path + “settingspackages” + package dir (template ID) + package name (template ID) + .pkgx.</span></span> <span data-ttu-id="ad5b2-163">Wenn der berechnete Pfad 260 Zeichen überschreitet, schlägt der Paketspeicher fehl, und es wird die folgende Fehlermeldung im operationellen UE-V-Ereignisprotokoll generiert:</span><span class="sxs-lookup"><span data-stu-id="ad5b2-163">If that calculated path exceeds 260 characters, package storage will fail and generate the following error message in the UE-V operational event log:</span></span>

`[boost::filesystem::copy_file: The system cannot find the path specified]`

<span data-ttu-id="ad5b2-164">Zum Überprüfen der Betriebsprotokoll Ereignisse öffnen Sie die Ereignisanzeige, und navigieren Sie zu Anwendungen und Dienstprotokolle/Microsoft/User Experience Virtualization/Logging/Operational.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-164">To check the operational log events, open the Event Viewer and navigate to Applications and Services Logs / Microsoft / User Experience Virtualization / Logging / Operational.</span></span>

<span data-ttu-id="ad5b2-165">**Problemumgehung:** Keine.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-165">**WORKAROUND:** None.</span></span>

### <span data-ttu-id="ad5b2-166">Einige Betriebssystemeinstellungen wechseln nur zwischen Betriebssystemversionen</span><span class="sxs-lookup"><span data-stu-id="ad5b2-166">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="ad5b2-167">Die Betriebssystemeinstellungen für Sprachausgaben und Währungszeichen, die für das gebietsschemaspezifisch sind (also sprach-und Regionaleinstellungen), werden nur über die Betriebssystemversionen von Windows durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-167">Operating system settings for Narrator and currency characters specific to the locale (i.e. language and regional settings) will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="ad5b2-168">Währungszeichen werden beispielsweise nicht zwischen Windows 7 und Windows 8 durchwandert.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-168">For example, currency characters will not roam between Windows 7 and Windows 8.</span></span>

<span data-ttu-id="ad5b2-169">**Problemumgehung:** Keine</span><span class="sxs-lookup"><span data-stu-id="ad5b2-169">**WORKAROUND:** None</span></span>

### <span data-ttu-id="ad5b2-170">Bei Windows 8-Apps werden die Einstellungen nicht synchronisiert, wenn die APP neu gestartet wird, nachdem Sie unerwartet geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-170">Windows 8 apps do not sync settings when the app restarts after closing unexpectedly</span></span>

<span data-ttu-id="ad5b2-171">Wenn eine Windows 8-App kurz nach dem Start unerwartet geschlossen wird, werden die Einstellungen für die Anwendung möglicherweise nicht synchronisiert, wenn die Anwendung neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-171">If a Windows 8 app closes unexpectedly soon after startup, settings for the application may not be synchronized when the application is restarted.</span></span>

<span data-ttu-id="ad5b2-172">**Problemumgehung:** Schließen Sie die Windows 8-APP, schließen Sie die UevAppMonitor.exe-Anwendung, und starten Sie Sie neu (kann Task Manager verwenden), und starten Sie dann die Windows 8-APP neu.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-172">**WORKAROUND:** Close the Windows 8 app, close and restart the UevAppMonitor.exe application (can use TaskManager), and then restart the Windows 8 app.</span></span>

### <a href="" id="ue-v-1-agent-generates-errors-when-running-ue-v-2-templates-"></a><span data-ttu-id="ad5b2-173">UE-v 1-Agent generiert Fehler beim Ausführen von UE-v 2-Vorlagen</span><span class="sxs-lookup"><span data-stu-id="ad5b2-173">UE-V 1 agent generates errors when running UE-V 2 templates</span></span>

<span data-ttu-id="ad5b2-174">Wenn eine Standort Vorlage für die UE-v 2-Einstellungen an einen Computer verteilt wird, der mit einem UE-v 1-Agent installiert ist, können einige Einstellungen nicht zwischen Computern synchronisiert werden, und der Agent meldet Fehler im Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-174">If a UE-V 2 settings location template is distributed to a computer installed with a UE-V 1 agent, some settings fail to synchronize between computers and the agent reports errors in the event log.</span></span>

<span data-ttu-id="ad5b2-175">**Problemumgehung:** Wenn Sie von UE-v 1 zu UE-v 2 migrieren und wahrscheinlich auf Computern die vorherige Version des Agents ausgeführt wird, erstellen Sie einen separaten UE-v 2,0-Katalog zur Unterstützung des UE-v 2,0-Agents und der Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-175">**WORKAROUND:** When migrating from UE-V 1 to UE-V 2 and it is likely you’ll have computers running the previous version of the agent, create a separate UE-V 2.0 catalog to support the UE-V 2.0 Agent and templates.</span></span>

## <span data-ttu-id="ad5b2-176">Hotfixes und Knowledge Base-Artikel für UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="ad5b2-176">Hotfixes and Knowledge Base articles for UE-V 2.0</span></span>


<span data-ttu-id="ad5b2-177">Dieser Abschnitt enthält Hotfixes und KB-Artikel für UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-177">This section contains hotfixes and KB articles for UE-V 2.0.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="ad5b2-178">KB-Artikel</span><span class="sxs-lookup"><span data-stu-id="ad5b2-178">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="ad5b2-179">Title</span><span class="sxs-lookup"><span data-stu-id="ad5b2-179">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="ad5b2-180">Link</span><span class="sxs-lookup"><span data-stu-id="ad5b2-180">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad5b2-181">2927019</span><span class="sxs-lookup"><span data-stu-id="ad5b2-181">2927019</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad5b2-182">Hotfix-Paket 1 für Microsoft User Experience Virtualization 2,0</span><span class="sxs-lookup"><span data-stu-id="ad5b2-182">Hotfix Package 1 for Microsoft User Experience Virtualization 2.0</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2927019" data-raw-source="[support.microsoft.com/kb/2927019](https://support.microsoft.com/kb/2927019)"><span data-ttu-id="ad5b2-183">support.microsoft.com/kb/2927019</span><span class="sxs-lookup"><span data-stu-id="ad5b2-183">support.microsoft.com/kb/2927019</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad5b2-184">2903501</span><span class="sxs-lookup"><span data-stu-id="ad5b2-184">2903501</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad5b2-185">UE-v: User Experience Virtualization (UE-v)-Kompatibilität mit Benutzerprofilen</span><span class="sxs-lookup"><span data-stu-id="ad5b2-185">UE-V: User Experience Virtualization (UE-V) compatibility with user profiles</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2903501/EN-US" data-raw-source="[support.microsoft.com/kb/2903501/EN-US](https://support.microsoft.com/kb/2903501/EN-US)"><span data-ttu-id="ad5b2-186">support.microsoft.com/kb/2903501/EN-US</span><span class="sxs-lookup"><span data-stu-id="ad5b2-186">support.microsoft.com/kb/2903501/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad5b2-187">2770042</span><span class="sxs-lookup"><span data-stu-id="ad5b2-187">2770042</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad5b2-188">UE-V-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="ad5b2-188">UE-V Registry Settings</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2770042/EN-US" data-raw-source="[support.microsoft.com/kb/2770042/EN-US](https://support.microsoft.com/kb/2770042/EN-US)"><span data-ttu-id="ad5b2-189">support.microsoft.com/kb/2770042/EN-US</span><span class="sxs-lookup"><span data-stu-id="ad5b2-189">support.microsoft.com/kb/2770042/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad5b2-190">2847017</span><span class="sxs-lookup"><span data-stu-id="ad5b2-190">2847017</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad5b2-191">Von Internet Explorer replizierte UE-V-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="ad5b2-191">UE-V settings replicated by Internet Explorer</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2847017/EN-US" data-raw-source="[support.microsoft.com/kb/2847017/EN-US](https://support.microsoft.com/kb/2847017/EN-US)"><span data-ttu-id="ad5b2-192">support.microsoft.com/kb/2847017/EN-US</span><span class="sxs-lookup"><span data-stu-id="ad5b2-192">support.microsoft.com/kb/2847017/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad5b2-193">2930271</span><span class="sxs-lookup"><span data-stu-id="ad5b2-193">2930271</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad5b2-194">Grundlegendes zu den Einschränkungen beim Roaming von Outlook-Signaturen in Microsoft UE-V</span><span class="sxs-lookup"><span data-stu-id="ad5b2-194">Understanding the limitations of roaming Outlook signatures in Microsoft UE-V</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2930271/EN-US" data-raw-source="[support.microsoft.com/kb/2930271/EN-US](https://support.microsoft.com/kb/2930271/EN-US)"><span data-ttu-id="ad5b2-195">support.microsoft.com/kb/2930271/EN-US</span><span class="sxs-lookup"><span data-stu-id="ad5b2-195">support.microsoft.com/kb/2930271/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad5b2-196">2769631</span><span class="sxs-lookup"><span data-stu-id="ad5b2-196">2769631</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad5b2-197">Reparieren einer beschädigten UE-V-Installation</span><span class="sxs-lookup"><span data-stu-id="ad5b2-197">How to repair a corrupted UE-V install</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769631/EN-US" data-raw-source="[support.microsoft.com/kb/2769631/EN-US](https://support.microsoft.com/kb/2769631/EN-US)"><span data-ttu-id="ad5b2-198">support.microsoft.com/kb/2769631/EN-US</span><span class="sxs-lookup"><span data-stu-id="ad5b2-198">support.microsoft.com/kb/2769631/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad5b2-199">2850989</span><span class="sxs-lookup"><span data-stu-id="ad5b2-199">2850989</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad5b2-200">Das Migrieren von MAPI-Profilen mit Microsoft UE-V wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-200">Migrating MAPI profiles with Microsoft UE-V is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850989/EN-US" data-raw-source="[support.microsoft.com/kb/2850989/EN-US](https://support.microsoft.com/kb/2850989/EN-US)"><span data-ttu-id="ad5b2-201">support.microsoft.com/kb/2850989/EN-US</span><span class="sxs-lookup"><span data-stu-id="ad5b2-201">support.microsoft.com/kb/2850989/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad5b2-202">2769586</span><span class="sxs-lookup"><span data-stu-id="ad5b2-202">2769586</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad5b2-203">UE-V durchstreift leere Ordner und Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="ad5b2-203">UE-V roams empty folders and registry keys</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769586/EN-US" data-raw-source="[support.microsoft.com/kb/2769586/EN-US](https://support.microsoft.com/kb/2769586/EN-US)"><span data-ttu-id="ad5b2-204">support.microsoft.com/kb/2769586/EN-US</span><span class="sxs-lookup"><span data-stu-id="ad5b2-204">support.microsoft.com/kb/2769586/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad5b2-205">2782997</span><span class="sxs-lookup"><span data-stu-id="ad5b2-205">2782997</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad5b2-206">Aktivieren der Debug-Protokollierung in Microsoft User Experience Virtualization (UE-V)</span><span class="sxs-lookup"><span data-stu-id="ad5b2-206">How To Enable Debug Logging in Microsoft User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2782997/EN-US" data-raw-source="[support.microsoft.com/kb/2782997/EN-US](https://support.microsoft.com/kb/2782997/EN-US)"><span data-ttu-id="ad5b2-207">support.microsoft.com/kb/2782997/EN-US</span><span class="sxs-lookup"><span data-stu-id="ad5b2-207">support.microsoft.com/kb/2782997/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad5b2-208">2769570</span><span class="sxs-lookup"><span data-stu-id="ad5b2-208">2769570</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad5b2-209">UE-V aktualisiert das Design nicht in RDS-oder VDI-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="ad5b2-209">UE-V does not update the theme on RDS or VDI sessions</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769570/EN-US" data-raw-source="[support.microsoft.com/kb/2769570/EN-US](https://support.microsoft.com/kb/2769570/EN-US)"><span data-ttu-id="ad5b2-210">support.microsoft.com/kb/2769570/EN-US</span><span class="sxs-lookup"><span data-stu-id="ad5b2-210">support.microsoft.com/kb/2769570/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad5b2-211">2901856</span><span class="sxs-lookup"><span data-stu-id="ad5b2-211">2901856</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad5b2-212">Anwendungseinstellungen werden nicht synchronisiert, nachdem Sie einen Neustart auf einem UE-V-fähigen Computer erzwungen haben</span><span class="sxs-lookup"><span data-stu-id="ad5b2-212">Application settings do not sync after you force a restart on a UE-V-enabled computer</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2901856/EN-US" data-raw-source="[support.microsoft.com/kb/2901856/EN-US](https://support.microsoft.com/kb/2901856/EN-US)"><span data-ttu-id="ad5b2-213">support.microsoft.com/kb/2901856/EN-US</span><span class="sxs-lookup"><span data-stu-id="ad5b2-213">support.microsoft.com/kb/2901856/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad5b2-214">2850582</span><span class="sxs-lookup"><span data-stu-id="ad5b2-214">2850582</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad5b2-215">Verwenden der Microsoft-Benutzeroberflächen-Virtualisierung mit App-V-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="ad5b2-215">How To Use Microsoft User Experience Virtualization With App-V Applications</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850582/EN-US" data-raw-source="[support.microsoft.com/kb/2850582/EN-US](https://support.microsoft.com/kb/2850582/EN-US)"><span data-ttu-id="ad5b2-216">support.microsoft.com/kb/2850582/EN-US</span><span class="sxs-lookup"><span data-stu-id="ad5b2-216">support.microsoft.com/kb/2850582/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad5b2-217">3041879</span><span class="sxs-lookup"><span data-stu-id="ad5b2-217">3041879</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad5b2-218">Aktuelle Dateiversionen für Microsoft User Experience Virtualization</span><span class="sxs-lookup"><span data-stu-id="ad5b2-218">Current file versions for Microsoft User Experience Virtualization</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3041879/EN-US" data-raw-source="[support.microsoft.com/kb/3041879/EN-US](https://support.microsoft.com/kb/3041879/EN-US)"><span data-ttu-id="ad5b2-219">support.microsoft.com/kb/3041879/EN-US</span><span class="sxs-lookup"><span data-stu-id="ad5b2-219">support.microsoft.com/kb/3041879/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad5b2-220">2843592</span><span class="sxs-lookup"><span data-stu-id="ad5b2-220">2843592</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad5b2-221">Informationen zur Benutzeroberflächen-Virtualisierung und zu einer höheren Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="ad5b2-221">Information on User Experience Virtualization and High Availability</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2843592/EN-US" data-raw-source="[support.microsoft.com/kb/2843592/EN-US](https://support.microsoft.com/kb/2843592/EN-US)"><span data-ttu-id="ad5b2-222">support.microsoft.com/kb/2843592/EN-US</span><span class="sxs-lookup"><span data-stu-id="ad5b2-222">support.microsoft.com/kb/2843592/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 

 

 





