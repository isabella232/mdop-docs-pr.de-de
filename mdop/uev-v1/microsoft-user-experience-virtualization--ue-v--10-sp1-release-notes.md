---
title: Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 1.0 SP1
description: Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 1.0 SP1
author: dansimp
ms.assetid: 447fae0c-fe87-4d1c-b616-6f92fbdaf6d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8584999d9fdbdfccc3e9b2b1486cb97635475747
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804262"
---
# <span data-ttu-id="d5132-103">Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 1.0 SP1</span><span class="sxs-lookup"><span data-stu-id="d5132-103">Microsoft User Experience Virtualization (UE-V) 1.0 SP1 Release Notes</span></span>


<span data-ttu-id="d5132-104">Drücken Sie STRG + F, um die Microsoft User Experience Virtualization (UE-V) 1,0 Service Pack 1-Versionshinweise zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="d5132-104">To search Microsoft User Experience Virtualization (UE-V) 1.0 Service Pack 1 release notes, press Ctrl+F.</span></span>

<span data-ttu-id="d5132-105">Lesen Sie diese Versionshinweise gründlich, bevor Sie UE-V installieren.</span><span class="sxs-lookup"><span data-stu-id="d5132-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="d5132-106">Die Anmerkungen zu dieser Version enthalten Informationen, die erforderlich sind, um die Virtualisierung der Benutzeroberfläche erfolgreich zu installieren, und zusätzliche Informationen enthalten, die in der Produktdokumentation nicht zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="d5132-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="d5132-107">Wenn es Unterschiede zwischen diesen Versionshinweisen und anderen UE-V-Dokumentationen gibt, sollte die neueste Änderung als autorisierend angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="d5132-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="d5132-108">Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d5132-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="d5132-109">Bekannte Probleme in UE-V</span><span class="sxs-lookup"><span data-stu-id="d5132-109">UE-V known issues</span></span>


<span data-ttu-id="d5132-110">Dieser Abschnitt enthält Anmerkungen zu dieser Version von User Experience Virtualization 1,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="d5132-110">This section contains release notes for User Experience Virtualization 1.0 SP1.</span></span>

### <span data-ttu-id="d5132-111">Registrierungseinstellungen können nicht zwischen App-V und systemeigenen Anwendungen auf demselben Computer synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d5132-111">Registry settings fail to synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="d5132-112">Wenn ein Computer über eine Anwendung verfügt, die sowohl über die Application Virtualization (App-V)-Anwendung als auch über eine systemeigene Installationsanwendung verfügt, die mit einer Windows Installer-Datei (MSI-Datei) installiert ist, werden die registrierungsbasierten Einstellungen nicht zwischen den Technologien synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="d5132-112">When a computer has an application that is available through both the Application Virtualization (App-V) application and a native installation application installed with a Windows Installer (.msi file), the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="d5132-113">Problemumgehung: um dieses Problem zu beheben, führen Sie die Anwendung aus, indem Sie eine der beiden Technologien auswählen, aber nicht beide.</span><span class="sxs-lookup"><span data-stu-id="d5132-113">WORKAROUND: To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <a href="" id="windows-8-setting-synchronization-fails-when-network-share-is-outside-user-s-domain"></a><span data-ttu-id="d5132-114">Die Synchronisierung von Windows 8-Einstellungen schlägt fehl, wenn die Netzwerkfreigabe außerhalb der Domäne des Benutzers liegt</span><span class="sxs-lookup"><span data-stu-id="d5132-114">Windows 8 setting synchronization fails when network share is outside user’s domain</span></span>

<span data-ttu-id="d5132-115">Wenn Windows® 8 die Synchronisierung der Betriebssystem Einstellungen versucht, schlägt die synchrnization mit der folgenden Fehlermeldung fehl: **Boost:: File System:: EXISTS:: Falscher Benutzername oder Kennwort**.</span><span class="sxs-lookup"><span data-stu-id="d5132-115">When Windows® 8 attempts operating system settings synchronization, the synchrnization fails with the following error message: **boost::filesystem::exists::Incorrect user name or password**.</span></span> <span data-ttu-id="d5132-116">Dieser Fehler kann darauf hindeuten, dass sich die Netzwerkfreigabe außerhalb der Domäne des Benutzers befindet.</span><span class="sxs-lookup"><span data-stu-id="d5132-116">This error can indicate that the network share is outside the user’s domain.</span></span> <span data-ttu-id="d5132-117">Wenn Sie nach Betriebsprotokoll Ereignissen suchen möchten, öffnen Sie die **Ereignisanzeige** , und navigieren Sie zu **Anwendungen und Dienstprotokolle**, die  /  **Microsoft**  /  **User Experience Virtualization**-  /  **Protokollierung**in  /  **Betrieb**sind.</span><span class="sxs-lookup"><span data-stu-id="d5132-117">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span> <span data-ttu-id="d5132-118">Netzwerkfreigaben, die für die Speicherorte der UE-V-Einstellungen verwendet werden, sollten sich in derselben Active Directory-Domäne wie der Benutzer befinden.</span><span class="sxs-lookup"><span data-stu-id="d5132-118">Network shares that are used for UE-V settings storage locations should reside in the same Active Directory domain as the user.</span></span>

<span data-ttu-id="d5132-119">Problemumgehung: Verwenden Sie Netzwerkfreigaben aus der gleichen Active Directory-Domäne wie der Benutzer.</span><span class="sxs-lookup"><span data-stu-id="d5132-119">WORKAROUND: Use network shares from the same Active Directory domain as the user.</span></span> <span data-ttu-id="d5132-120">.</span><span class="sxs-lookup"><span data-stu-id="d5132-120">.</span></span>

### <span data-ttu-id="d5132-121">E-Mail-Signatur-Roaming für Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="d5132-121">Email signature roaming for Outlook 2010</span></span>

<span data-ttu-id="d5132-122">UE-V durchstreift die Outlook 2010-Signaturdateien zwischen Geräten.</span><span class="sxs-lookup"><span data-stu-id="d5132-122">UE-V will roam the Outlook 2010 signature files between devices.</span></span> <span data-ttu-id="d5132-123">Die standardmäßigen Signaturoptionen für neue Nachrichten und Antworten/Weiterleitungen werden jedoch nicht durchstreift.</span><span class="sxs-lookup"><span data-stu-id="d5132-123">However, the default signature options for new messages and replies/forwards are not roamed.</span></span> <span data-ttu-id="d5132-124">Diese beiden Einstellungen werden im Outlook-Profil gespeichert, das UE-V nicht durchwandert.</span><span class="sxs-lookup"><span data-stu-id="d5132-124">These two settings are stored in the Outlook profile, which UE-V does not roam.</span></span>

<span data-ttu-id="d5132-125">Problemumgehung: keine.</span><span class="sxs-lookup"><span data-stu-id="d5132-125">WORKAROUND: None.</span></span>

### <span data-ttu-id="d5132-126">Synchronisierungseinstellungen werden nicht im erwarteten Intervall synchronisiert, wenn Sie im Slow-Link-Modus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d5132-126">Synchronization settings do not synchronize on expected interval when running in slow-link mode</span></span>

<span data-ttu-id="d5132-127">Unter normalen Bedingungen sollten Einstellungen Speicherorte über eine fast Link-Netzwerkverbindung zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="d5132-127">Under normal conditions, settings storage locations should be available over a fast link network connection.</span></span> <span data-ttu-id="d5132-128">Im Modus für langsame Verbindungen erfolgt die Synchronisierung nur regelmäßig.</span><span class="sxs-lookup"><span data-stu-id="d5132-128">In slow-link mode, synchronization will only occur on a periodic basis.</span></span> <span data-ttu-id="d5132-129">Standardmäßig ist der Synchronisierungszeitplan für den Slow-Link-Modus auf alle 360 Minuten eingestellt.</span><span class="sxs-lookup"><span data-stu-id="d5132-129">By default, the slow-link mode synchronization schedule is set to every 360 minutes.</span></span>

<span data-ttu-id="d5132-130">Problemumgehung: Wenn Sie die Häufigkeit der Hintergrundsynchronisierung für Computer im Slow-Link-Modus ändern möchten, können Sie die Gruppenrichtlinie für die Hintergrund Synchronisierungs Richtlinie für **Offline Dateien**konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d5132-130">WORKAROUND: To change the frequency of the background synchronization for computers in slow-link mode, you can configure the Group Policy for Background Sync policy for **Offline files**.</span></span>

### <span data-ttu-id="d5132-131">Sonderzeichen werden nicht synchronisiert</span><span class="sxs-lookup"><span data-stu-id="d5132-131">Special characters do not synchronize</span></span>

<span data-ttu-id="d5132-132">Bestimmte Zeichen wie Währungssymbole können nicht zwischen Windows 7-und Windows 8-Computern synchronisiert werden, auf denen der UE-V-Agent ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5132-132">Certain characters, such as currency symbols, do not synchronize between Windows 7 and Windows 8 computers that run the UE-V agent.</span></span>

<span data-ttu-id="d5132-133">Problemumgehung: keine.</span><span class="sxs-lookup"><span data-stu-id="d5132-133">WORKAROUND: None.</span></span>

### <span data-ttu-id="d5132-134">UE-V unterstützt keine Roamingeinstellungen zwischen 32-Bit-und 64-Bit-Versionen von Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="d5132-134">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="d5132-135">Wir empfehlen, die 32-Bit-Version von Microsoft Office sowohl für 32-Bit-als auch für 64-Bit-Betriebssysteme zu installieren.</span><span class="sxs-lookup"><span data-stu-id="d5132-135">We recommend that you install the 32-bit version of Microsoft Office for both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="d5132-136">Wenn Sie die von Ihnen benötigte Microsoft Office-Version auswählen möchten, klicken Sie hier ( [http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623) ).</span><span class="sxs-lookup"><span data-stu-id="d5132-136">To choose the Microsoft Office version that you need, click here ([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span></span> <span data-ttu-id="d5132-137">UE-V unterstützt Roamingeinstellungen zwischen identischen Architekturversionen von Office.</span><span class="sxs-lookup"><span data-stu-id="d5132-137">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="d5132-138">Beispielsweise werden die Office-Einstellungen für 32-Bit zwischen allen 32-Bit-Office-Instanzen durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="d5132-138">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="d5132-139">UE-V unterstützt keine Roamingeinstellungen zwischen 32-Bit-und 64-Bit-Versionen von Office.</span><span class="sxs-lookup"><span data-stu-id="d5132-139">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="d5132-140">Problemumgehung: keine</span><span class="sxs-lookup"><span data-stu-id="d5132-140">WORKAROUND: None</span></span>

### <a href="" id="msi-s-are-not-localized"></a><span data-ttu-id="d5132-141">MSI-Versionen sind nicht lokalisiert</span><span class="sxs-lookup"><span data-stu-id="d5132-141">MSI’s are not localized</span></span>

<span data-ttu-id="d5132-142">UE-v 1,0 SP1 umfasst ein lokalisiertes Setupprogramm für den UE-v-Agent und den UE-v-Generator.</span><span class="sxs-lookup"><span data-stu-id="d5132-142">UE-V 1.0 SP1 includes a localized setup program for both the UE-V Agent and UE-V generator.</span></span> <span data-ttu-id="d5132-143">Diese MSI-Dateien sind weiterhin verfügbar, die Benutzeroberfläche wird jedoch minimiert, und die MSI-Datei wird nur in Englisch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d5132-143">These MSI files are still available but the user interface is minimized and the MSI’s only display in English.</span></span> <span data-ttu-id="d5132-144">Obwohl die Datei in Englisch ist, werden alle unterstützten Sprachen während der Installation von dem Setup-Programm installiert.</span><span class="sxs-lookup"><span data-stu-id="d5132-144">Despite the file being in English, the setup program installs all supported languages during the installation.</span></span>

<span data-ttu-id="d5132-145">Problemumgehung: keine</span><span class="sxs-lookup"><span data-stu-id="d5132-145">WORKAROUND: None</span></span>

### <span data-ttu-id="d5132-146">Andere Ordner auf der Freigabe mit dem Einstellungs Speicherort sind im Modus für langsame Verbindung nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d5132-146">Other folders on the share with the setting storage location are unavailable in slow-connection mode</span></span>

<span data-ttu-id="d5132-147">Einstellungen Speicherfreigaben sollten sich nicht auf einer Netzwerkfreigabe befinden, die für andere Ordner verwendet wird, die immer verfügbar sein müssen.</span><span class="sxs-lookup"><span data-stu-id="d5132-147">Settings store shares should not be located on a network share that is used for other folders that must always be available.</span></span> <span data-ttu-id="d5132-148">Wenn die Netzwerkfreigabe, die den festgelegten Speicherplatz hostet, in den Modus für langsame Verbindung wechselt, ist der einzige verfügbare Ordner der Ordner Einstellungen-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="d5132-148">When the network share that hosts the setting storage location goes into slow-connection mode, the only available folder is the settings storage location folder.</span></span> <span data-ttu-id="d5132-149">Andere Ordner auf der Freigabe stehen im Modus für langsame Verbindung nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d5132-149">Other folders on the Share are not available in slow-connection mode.</span></span>

<span data-ttu-id="d5132-150">Problemumgehung: keine</span><span class="sxs-lookup"><span data-stu-id="d5132-150">Workaround: None</span></span>

### <span data-ttu-id="d5132-151">Favicons, die mit Internet Explorer 9-Favoriten verknüpft sind, werden nicht durchwandert</span><span class="sxs-lookup"><span data-stu-id="d5132-151">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="d5132-152">Die Favicons, die mit Internet Explorer 9-Favoriten verknüpft sind, werden nicht von der Benutzeroberflächen-Virtualisierung durchlaufen und nicht angezeigt, wenn die Favoriten auf einem neuen Computer erstmalig angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d5132-152">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="d5132-153">Problemumgehung: Favicons werden mit den zugehörigen Favoriten angezeigt, sobald die Textmarke verwendet und im Internet Explorer 9-Browser zwischengespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="d5132-153">WORKAROUND: Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="d5132-154">Datei Einstellungs Pfade werden in der Registrierung gespeichert</span><span class="sxs-lookup"><span data-stu-id="d5132-154">File settings paths are stored in registry</span></span>

<span data-ttu-id="d5132-155">In einigen Anwendungseinstellungen werden die Pfade Ihrer Konfigurations-und Einstellungsdateien als Werte in der Registrierung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d5132-155">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="d5132-156">Die Dateien, die als Pfade in der Registrierung referenziert werden, müssen synchronisiert werden, wenn die Einstellungen zwischen Computern durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="d5132-156">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="d5132-157">Problemumgehung: Verwenden Sie die Ordnerumleitung oder eine andere Technologie, um sicherzustellen, dass alle Dateien, auf die als Pfad für Datei Einstellungen verwiesen wird, vorhanden sind und auf allen Computern, auf denen die Einstellungen durchlaufen werden, an derselben Stelle abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d5132-157">WORKAROUND: Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="d5132-158">Lange Einstellungen Speicherpfade können einen Fehler verursachen</span><span class="sxs-lookup"><span data-stu-id="d5132-158">Long Settings Storage Paths could cause an error</span></span>

<span data-ttu-id="d5132-159">Behalten Sie die Einstellungen für den Speicherpfad so kurz wie möglich.</span><span class="sxs-lookup"><span data-stu-id="d5132-159">Keep settings storage paths as short as possible.</span></span> <span data-ttu-id="d5132-160">Lange Pfade können die Auflösung oder Synchronisierung verhindern.</span><span class="sxs-lookup"><span data-stu-id="d5132-160">Long paths could prevent resolution or synchronization.</span></span> <span data-ttu-id="d5132-161">UE-V verwendet den Einstellungsspeicher Pfad als Teil des berechneten Pfads zum Speichern von Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="d5132-161">UE-V uses the Settings storage path as part of the calculated path to store settings.</span></span> <span data-ttu-id="d5132-162">Dieser Pfad wird folgendermaßen berechnet: Einstellungsspeicher Pfad + "settingspackages" + Paket dir (Vorlagen-ID) + Paketname (Vorlagen-ID).</span><span class="sxs-lookup"><span data-stu-id="d5132-162">That path is calculated in the following way: settings storage path + “settingspackages” + package dir (template ID) + package name (template ID).</span></span> <span data-ttu-id="d5132-163">Wenn der berechnete Pfad 260 Zeichen überschreitet, schlägt der Paketspeicher fehl, und es wird die folgende Fehlermeldung im operationellen UE-V-Ereignisprotokoll generiert:</span><span class="sxs-lookup"><span data-stu-id="d5132-163">If that calculated path exceeds 260 characters, package storage will fail and generate the following error message in the UE-V operational event log:</span></span>

`[boost::filesystem::copy_file: The system cannot find the path specified]`

<span data-ttu-id="d5132-164">Zum Überprüfen der Betriebsprotokoll Ereignisse öffnen Sie die Ereignisanzeige, und navigieren Sie zu Anwendungen und Dienstprotokolle/Microsoft/User Experience Virtualization/Logging/Operational.</span><span class="sxs-lookup"><span data-stu-id="d5132-164">To check the operational log events, open the Event Viewer and navigate to Applications and Services Logs / Microsoft / User Experience Virtualization / Logging / Operational.</span></span>

<span data-ttu-id="d5132-165">Problemumgehung: keine.</span><span class="sxs-lookup"><span data-stu-id="d5132-165">WORKAROUND: None.</span></span>

### <span data-ttu-id="d5132-166">UE-V-Agenten Verzögerungen beim Abmelden oder anmelden</span><span class="sxs-lookup"><span data-stu-id="d5132-166">UE-V agent delays upon logout or login</span></span>

<span data-ttu-id="d5132-167">Wenn eine Anmeldung oder Abmeldung stattfindet, bevor Offline Dateien festgestellt haben, dass eine langsame Verbindung vorhanden ist, kann sich das Abmelden oder anmelden verzögert werden.</span><span class="sxs-lookup"><span data-stu-id="d5132-167">If a logon or logout occurs before Offline Files has determined that a slow link is in place, logout or login might be delayed.</span></span> <span data-ttu-id="d5132-168">Das Feature "Offline Dateien" kann bis zu drei Minuten dauern, um den aktuellen Netzwerkzustand zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="d5132-168">The Offline Files feature may take up to three minutes to detect the current network state.</span></span> <span data-ttu-id="d5132-169">Wenn die Anmeldung oder das Herunterfahren eintritt, bevor Offline Dateien festgestellt haben, dass der Computer mit einer langsamen Verbindung verbunden ist, wird das UE-V-Einstellungspaket an den Server anstelle des lokalen Caches gesendet.</span><span class="sxs-lookup"><span data-stu-id="d5132-169">If the logon or shutdown occurs before Offline Files has determined that the computer is connected to a slow link, the UE-V settings package will be sent to the server instead of the local cache.</span></span>

<span data-ttu-id="d5132-170">Problemumgehung: keine.</span><span class="sxs-lookup"><span data-stu-id="d5132-170">WORKAROUND: None.</span></span>

### <span data-ttu-id="d5132-171">Konflikte beim Versuch, die Einstellungen des Betriebssystems unter Windows 8 zu durchlaufen</span><span class="sxs-lookup"><span data-stu-id="d5132-171">Settings conflict when trying to roam operating system settings on Windows 8</span></span>

<span data-ttu-id="d5132-172">Unter Windows 8, wenn die Microsoft-Konto Synchronisierung zusammen mit UE-V für Betriebssystemeinstellungen aktiviert ist, sind die angewendeten Einstellungen möglicherweise inkonsistent.</span><span class="sxs-lookup"><span data-stu-id="d5132-172">On Windows 8 if Microsoft Account Sync is enabled along with UE-V for operating system settings, the settings that are applied may be inconsistent.</span></span>

<span data-ttu-id="d5132-173">Problemumgehung: führen Sie eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="d5132-173">WORKAROUND: Do one of the following:</span></span>

-   <span data-ttu-id="d5132-174">Deaktivieren der Microsoft-Konto Synchronisierung, wenn Sie UE-V für die Roaming-Einstellungen des Betriebssystems verwenden</span><span class="sxs-lookup"><span data-stu-id="d5132-174">Disable Microsoft Account Sync if you are using UE-V to roam operating system settings</span></span>

-   <span data-ttu-id="d5132-175">Deaktivieren von UE-V für Betriebssystemeinstellungen</span><span class="sxs-lookup"><span data-stu-id="d5132-175">Disable UE-V for operating system settings</span></span>

### <span data-ttu-id="d5132-176">Einige Betriebssystemeinstellungen wechseln nur zwischen Betriebssystemversionen</span><span class="sxs-lookup"><span data-stu-id="d5132-176">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="d5132-177">Die Betriebssystemeinstellungen für Sprachausgaben und Währungszeichen, die für das gebietsschemaspezifisch sind, werden nur wie Betriebssystemversionen von Windows durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="d5132-177">Operating system settings for Narrator and currency characters specific to the locale will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="d5132-178">Währungszeichen können beispielsweise nur von Windows 7 zu Windows 7 gewechselt werden.</span><span class="sxs-lookup"><span data-stu-id="d5132-178">For example currency characters will only roam from Windows 7 to Windows 7.</span></span>

<span data-ttu-id="d5132-179">Problemumgehung: keine</span><span class="sxs-lookup"><span data-stu-id="d5132-179">WORKAROUND: None</span></span>

 

 





