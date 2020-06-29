---
title: Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 1.0
description: Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 1.0
author: dansimp
ms.assetid: 920f3fae-e9b5-4b94-beda-32c19d31e94b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9f9942eef7ea84cf7010a0c0173427827a512216
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804265"
---
# <span data-ttu-id="42df2-103">Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="42df2-103">Microsoft User Experience Virtualization (UE-V) 1.0 Release Notes</span></span>


<span data-ttu-id="42df2-104">Drücken Sie STRG + F, um Microsoft User Experience Virtualization (UE-V)-Versionshinweise zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="42df2-104">To search Microsoft User Experience Virtualization (UE-V) release notes, press Ctrl+F.</span></span>

<span data-ttu-id="42df2-105">Lesen Sie diese Versionshinweise gründlich, bevor Sie UE-V installieren.</span><span class="sxs-lookup"><span data-stu-id="42df2-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="42df2-106">Die Anmerkungen zu dieser Version enthalten Informationen, die erforderlich sind, um die Virtualisierung der Benutzeroberfläche erfolgreich zu installieren, und zusätzliche Informationen enthalten, die in der Produktdokumentation nicht zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="42df2-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="42df2-107">Wenn es Unterschiede zwischen diesen Versionshinweisen und anderen UE-V-Dokumentationen gibt, sollte die neueste Änderung als autorisierend angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="42df2-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="42df2-108">Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="42df2-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="42df2-109">Abgeben von Feedback</span><span class="sxs-lookup"><span data-stu-id="42df2-109">Providing feedback</span></span>


<span data-ttu-id="42df2-110">Teilen Sie uns Ihre Meinung zu unserer Dokumentation zu MDOP mit, indem Sie uns Feedback und Kommentare geben.</span><span class="sxs-lookup"><span data-stu-id="42df2-110">Tell us what you think about our documentation for MDOP by giving us your feedback and comments.</span></span> <span data-ttu-id="42df2-111">Senden Sie Ihr Feedback zur Dokumentation an [mdopdocs@Microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span><span class="sxs-lookup"><span data-stu-id="42df2-111">Send your documentation feedback to [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span></span>

## <span data-ttu-id="42df2-112">Bekannte Probleme in UE-V</span><span class="sxs-lookup"><span data-stu-id="42df2-112">UE-V known issues</span></span>


<span data-ttu-id="42df2-113">Dieser Abschnitt enthält Anmerkungen zu dieser Version für die Virtualisierung der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="42df2-113">This section contains release notes for User Experience Virtualization.</span></span>

### <span data-ttu-id="42df2-114">Registrierungseinstellungen können nicht zwischen App-V und systemeigenen Anwendungen auf demselben Computer synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="42df2-114">Registry settings fail to synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="42df2-115">Wenn ein Computer über eine Anwendung verfügt, die sowohl über die Application Virtualization (App-V)-Anwendung als auch über eine systemeigene Installationsanwendung (mit einer MSI-Datei installiert) verfügbar ist, werden die registrierungsbasierten Einstellungen nicht zwischen den Technologien synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="42df2-115">When a computer has an application that is available through both the Application Virtualization (App-V) application and a native installation application (installed with an .msi file), the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="42df2-116">Problemumgehung: um dieses Problem zu beheben, führen Sie die Anwendung aus, indem Sie eine der beiden Technologien auswählen, aber nicht beide.</span><span class="sxs-lookup"><span data-stu-id="42df2-116">WORKAROUND: To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <span data-ttu-id="42df2-117">Bei der Synchronisierung von Windows 8-Einstellungen tritt ein Fehler auf: "Boost:: Dateisystem:: EXISTS:: Falscher Benutzername oder Kennwort"</span><span class="sxs-lookup"><span data-stu-id="42df2-117">Windows 8 setting synchronization fails with error: "boost::filesystem::exists::Incorrect user name or password"</span></span>

<span data-ttu-id="42df2-118">Die Synchronisierung der Betriebssystem Einstellungen für Windows® 8 schlägt mit der folgenden Fehlermeldung fehl: **Boost:: File System:: EXISTS:: Falscher Benutzername oder Kennwort**.</span><span class="sxs-lookup"><span data-stu-id="42df2-118">The Windows® 8 operating system settings synchronization fails with the following error message: **boost::filesystem::exists::Incorrect user name or password**.</span></span> <span data-ttu-id="42df2-119">Wenn Sie nach Betriebsprotokoll Ereignissen suchen möchten, öffnen Sie die **Ereignisanzeige** , und navigieren Sie zu **Anwendungen und Dienstprotokolle**, die  /  **Microsoft**  /  **User Experience Virtualization**-  /  **Protokollierung**in  /  **Betrieb**sind.</span><span class="sxs-lookup"><span data-stu-id="42df2-119">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span> <span data-ttu-id="42df2-120">Netzwerkfreigaben, die für die Speicherorte der UE-V-Einstellungen verwendet werden, sollten sich in derselben Active Directory-Domäne wie der Benutzer befinden.</span><span class="sxs-lookup"><span data-stu-id="42df2-120">Network shares that are used for UE-V settings storage locations should reside in the same Active Directory domain as the user.</span></span> <span data-ttu-id="42df2-121">Andernfalls kann der folgende Fehler auftreten: "Falscher Benutzername oder Kennwort".</span><span class="sxs-lookup"><span data-stu-id="42df2-121">Otherwise, the following error might occur: "Incorrect user name or password".</span></span>

<span data-ttu-id="42df2-122">Problemumgehung: Verwenden Sie Netzwerkfreigaben aus der gleichen Active Directory-Domäne wie der Benutzer.</span><span class="sxs-lookup"><span data-stu-id="42df2-122">WORKAROUND: Use network shares from the same Active Directory domain as the user.</span></span> <span data-ttu-id="42df2-123">.</span><span class="sxs-lookup"><span data-stu-id="42df2-123">.</span></span>

### <span data-ttu-id="42df2-124">E-Mail-Signatur-Roaming für Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="42df2-124">Email signature roaming for Outlook 2010</span></span>

<span data-ttu-id="42df2-125">UE-V durchstreift die Outlook 2010-Signaturdateien zwischen Geräten.</span><span class="sxs-lookup"><span data-stu-id="42df2-125">UE-V will roam the Outlook 2010 signature files between devices.</span></span> <span data-ttu-id="42df2-126">Die standardmäßigen Signaturoptionen für neue Nachrichten und Antworten/Weiterleitungen sind jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="42df2-126">However, the default signature options for new messages and replies/forwards are not.</span></span><span data-ttu-id="42df2-127">Diese beiden Einstellungen werden im Outlook-Profil gespeichert, das UE-Vdoes nicht durchwandert.</span><span class="sxs-lookup"><span data-stu-id="42df2-127"> These two settings are stored in the Outlook profile, which UE-Vdoes not roam.</span></span>

<span data-ttu-id="42df2-128">Problemumgehung: keine.</span><span class="sxs-lookup"><span data-stu-id="42df2-128">WORKAROUND: None.</span></span>

### <span data-ttu-id="42df2-129">Synchronisierungseinstellungen werden nicht im erwarteten Intervall synchronisiert, wenn Sie im Slow-Link-Modus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="42df2-129">Synchronization settings do not synchronize on expected interval when running in slow-link mode</span></span>

<span data-ttu-id="42df2-130">Unter normalen Bedingungen sollten Einstellungen Speicherorte über eine fast Link-Netzwerkverbindung zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="42df2-130">Under normal conditions, settings storage locations should be available over a fast link network connection.</span></span> <span data-ttu-id="42df2-131">Im Modus für langsame Verbindungen erfolgt die Synchronisierung nur regelmäßig.</span><span class="sxs-lookup"><span data-stu-id="42df2-131">In slow-link mode, synchronization will only occur on a periodic basis.</span></span> <span data-ttu-id="42df2-132">Standardmäßig ist der Synchronisierungszeitplan für den Slow-Link-Modus auf alle 360 Minuten eingestellt.</span><span class="sxs-lookup"><span data-stu-id="42df2-132">By default, the slow-link mode synchronization schedule is set to every 360 minutes.</span></span>

<span data-ttu-id="42df2-133">Problemumgehung: Wenn Sie die Häufigkeit der Hintergrundsynchronisierung für Computer im Slow-Link-Modus ändern möchten, können Sie die Gruppenrichtlinie für die Hintergrund Synchronisierungs Richtlinie für **Offline Dateien**konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="42df2-133">WORKAROUND: To change the frequency of the background synchronization for computers in slow-link mode, you can configure the Group Policy for Background Sync policy for **Offline files**.</span></span>

### <span data-ttu-id="42df2-134">Sonderzeichen werden nicht synchronisiert</span><span class="sxs-lookup"><span data-stu-id="42df2-134">Special characters do not synchronize</span></span>

<span data-ttu-id="42df2-135">Bestimmte Zeichen wie Währungssymbole können nicht zwischen Windows 7-und Windows 8-Computern synchronisiert werden, auf denen der UE-V-Agent ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42df2-135">Certain characters, such as currency symbols, do not synchronize between Windows 7 and Windows 8 computers that run the UE-V agent.</span></span>

<span data-ttu-id="42df2-136">Problemumgehung: keine.</span><span class="sxs-lookup"><span data-stu-id="42df2-136">WORKAROUND: None.</span></span>

### <span data-ttu-id="42df2-137">UE-V unterstützt keine Roamingeinstellungen zwischen 32-Bit-und 64-Bit-Versionen von Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="42df2-137">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="42df2-138">Wir empfehlen, die 32-Bit-Version von Microsoft Office sowohl für 32-Bit-als auch für 64-Bit-Betriebssysteme zu installieren.</span><span class="sxs-lookup"><span data-stu-id="42df2-138">We recommend that you install the 32-bit version of Microsoft Office for both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="42df2-139">Wenn Sie die von Ihnen benötigte Microsoft Office-Version auswählen möchten, klicken Sie hier.</span><span class="sxs-lookup"><span data-stu-id="42df2-139">To choose the Microsoft Office version that you need, click here.</span></span> <span data-ttu-id="42df2-140">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span><span class="sxs-lookup"><span data-stu-id="42df2-140">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span></span> <span data-ttu-id="42df2-141">UE-V unterstützt Roamingeinstellungen zwischen identischen Architekturversionen von Office.</span><span class="sxs-lookup"><span data-stu-id="42df2-141">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="42df2-142">Beispielsweise werden die Office-Einstellungen für 32-Bit zwischen allen 32-Bit-Office-Instanzen durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="42df2-142">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="42df2-143">UE-V unterstützt keine Roamingeinstellungen zwischen 32-Bit-und 64-Bit-Versionen von Office.</span><span class="sxs-lookup"><span data-stu-id="42df2-143">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="42df2-144">Problemumgehung: keine</span><span class="sxs-lookup"><span data-stu-id="42df2-144">WORKAROUND: None</span></span>

### <span data-ttu-id="42df2-145">Andere Ordner auf der Freigabe mit dem Einstellungs Speicherort sind im Modus für langsame Verbindung nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="42df2-145">Other folders on the share with the setting storage location are unavailable in slow-connection mode</span></span>

<span data-ttu-id="42df2-146">Einstellungen Speicherfreigaben sollten sich nicht auf einer Netzwerkfreigabe befinden, die für andere Ordner verwendet wird, die immer verfügbar sein müssen.</span><span class="sxs-lookup"><span data-stu-id="42df2-146">Settings store shares should not be located on a network share that is used for other folders that must always be available.</span></span> <span data-ttu-id="42df2-147">Wenn die Netzwerkfreigabe, die den festgelegten Speicherplatz hostet, in den Modus für langsame Verbindung wechselt, ist der einzige verfügbare Ordner der Ordner Einstellungen-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="42df2-147">When the network share that hosts the setting storage location goes into slow-connection mode, the only available folder is the settings storage location folder.</span></span> <span data-ttu-id="42df2-148">Andere Ordner auf der Freigabe stehen im Modus für langsame Verbindung nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="42df2-148">Other folders on the Share are not available in slow-connection mode.</span></span>

<span data-ttu-id="42df2-149">Problemumgehung: keine</span><span class="sxs-lookup"><span data-stu-id="42df2-149">Workaround: None</span></span>

### <span data-ttu-id="42df2-150">Favicons, die mit Internet Explorer 9-Favoriten verknüpft sind, werden nicht durchwandert</span><span class="sxs-lookup"><span data-stu-id="42df2-150">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="42df2-151">Die Favicons, die mit Internet Explorer 9-Favoriten verknüpft sind, werden nicht von der Benutzeroberflächen-Virtualisierung durchlaufen und nicht angezeigt, wenn die Favoriten auf einem neuen Computer erstmalig angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="42df2-151">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="42df2-152">Problemumgehung: Favicons werden mit den zugehörigen Favoriten angezeigt, sobald die Textmarke verwendet und im Internet Explorer 9-Browser zwischengespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="42df2-152">WORKAROUND: Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="42df2-153">Datei Einstellungs Pfade werden in der Registrierung gespeichert</span><span class="sxs-lookup"><span data-stu-id="42df2-153">File settings paths are stored in registry</span></span>

<span data-ttu-id="42df2-154">In einigen Anwendungseinstellungen werden die Pfade Ihrer Konfigurations-und Einstellungsdateien als Werte in der Registrierung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="42df2-154">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="42df2-155">Die Dateien, die als Pfade in der Registrierung referenziert werden, müssen synchronisiert werden, wenn die Einstellungen zwischen Computern durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="42df2-155">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="42df2-156">Problemumgehung: Verwenden Sie die Ordnerumleitung oder eine andere Technologie, um sicherzustellen, dass alle Dateien, auf die als Pfad für Datei Einstellungen verwiesen wird, vorhanden sind und auf allen Computern, auf denen die Einstellungen durchlaufen werden, an derselben Stelle abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="42df2-156">WORKAROUND: Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="42df2-157">Pfade, die länger als 260 Zeichen sind, werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42df2-157">Paths longer than 260 characters are not supported</span></span>

<span data-ttu-id="42df2-158">Einstellungen Speicherpfade, die länger als 260 Zeichen sind, werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42df2-158">Settings storage paths that are longer than 260 characters are not supported.</span></span> <span data-ttu-id="42df2-159">Das Kopieren der UE-v-Einstellungs Pakete in Einstellungen Speicherpfade, die länger als 260 Zeichen sind, schlägt fehl, und die folgende Ausnahmemeldung wird im operationellen UE-v-Ereignisprotokoll generiert: **\ [Boost:: Dateisystem:: Kopieren \ _File: das System kann den angegebenen Pfad nicht finden \]**.</span><span class="sxs-lookup"><span data-stu-id="42df2-159">Copying the UE-V settings packages to settings storage paths that are longer than 260 characters will fail and generate the following exception message in the UE-V operational event log: **\[boost::filesystem::copy\_file: The system cannot find the path specified\]**.</span></span> <span data-ttu-id="42df2-160">Wenn Sie nach Betriebsprotokoll Ereignissen suchen möchten, öffnen Sie die **Ereignisanzeige** , und navigieren Sie zu **Anwendungen und Dienstprotokolle**, die  /  **Microsoft**  /  **User Experience Virtualization**-  /  **Protokollierung**in  /  **Betrieb**sind.</span><span class="sxs-lookup"><span data-stu-id="42df2-160">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span>

<span data-ttu-id="42df2-161">Datei Einstellungs Pfade, die länger als 260 Zeichen sind, werden zurzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42df2-161">File settings paths that are longer than 260 characters are not currently supported.</span></span> <span data-ttu-id="42df2-162">Datei Einstellungen, auf die in UE-V-Einstellungen verwiesen wird, können sich nicht in einem Verzeichnispfad befinden, der mehr als 260 Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="42df2-162">File settings that are referenced in UE-V settings location templates cannot be located in a directory path that is longer than 260 characters.</span></span>

<span data-ttu-id="42df2-163">Problemumgehung: keine.</span><span class="sxs-lookup"><span data-stu-id="42df2-163">WORKAROUND: None.</span></span>

### <span data-ttu-id="42df2-164">UE-V-Agenten Verzögerungen beim Abmelden oder anmelden</span><span class="sxs-lookup"><span data-stu-id="42df2-164">UE-V agent delays upon logout or login</span></span>

<span data-ttu-id="42df2-165">Wenn eine Anmeldung oder Abmeldung stattfindet, bevor Offline Dateien festgestellt haben, dass eine langsame Verbindung vorhanden ist, kann sich das Abmelden oder anmelden verzögert werden.</span><span class="sxs-lookup"><span data-stu-id="42df2-165">If a logon or logout occurs before Offline Files has determined that a slow link is in place, logout or login might be delayed.</span></span> <span data-ttu-id="42df2-166">Das Feature "Offline Dateien" kann bis zu drei Minuten dauern, um den aktuellen Netzwerkzustand zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="42df2-166">The Offline Files feature may take up to three minutes to detect the current network state.</span></span> <span data-ttu-id="42df2-167">Wenn die Anmeldung oder das Herunterfahren eintritt, bevor Offline Dateien festgestellt haben, dass der Computer mit einer langsamen Verbindung verbunden ist, wird das UE-V-Einstellungspaket an den Server anstelle des lokalen Caches gesendet.</span><span class="sxs-lookup"><span data-stu-id="42df2-167">If the logon or shutdown occurs before Offline Files has determined that the computer is connected to a slow link, the UE-V settings package will be sent to the server instead of the local cache.</span></span>

<span data-ttu-id="42df2-168">Problemumgehung: keine.</span><span class="sxs-lookup"><span data-stu-id="42df2-168">WORKAROUND: None.</span></span>

### <span data-ttu-id="42df2-169">Konflikte beim Versuch, die Einstellungen des Betriebssystems unter Windows 8 zu durchlaufen</span><span class="sxs-lookup"><span data-stu-id="42df2-169">Settings conflict when trying to roam operating system settings on Windows 8</span></span>

<span data-ttu-id="42df2-170">Unter Windows 8, wenn die Microsoft-Konto Synchronisierung zusammen mit UE-V für Betriebssystemeinstellungen aktiviert ist, sind die angewendeten Einstellungen möglicherweise inkonsistent.</span><span class="sxs-lookup"><span data-stu-id="42df2-170">On Windows 8 if Microsoft Account Sync is enabled along with UE-V for operating system settings, the settings that are applied may be inconsistent.</span></span>

<span data-ttu-id="42df2-171">Problemumgehung: führen Sie eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="42df2-171">WORKAROUND: Do one of the following:</span></span>

-   <span data-ttu-id="42df2-172">Deaktivieren der Microsoft-Konto Synchronisierung, wenn Sie UE-V für die Roaming-Einstellungen des Betriebssystems verwenden</span><span class="sxs-lookup"><span data-stu-id="42df2-172">Disable Microsoft Account Sync if you are using UE-V to roam operating system settings</span></span>

-   <span data-ttu-id="42df2-173">Deaktivieren von UE-V für Betriebssystemeinstellungen</span><span class="sxs-lookup"><span data-stu-id="42df2-173">Disable UE-V for operating system settings</span></span>

### <span data-ttu-id="42df2-174">Einige Betriebssystemeinstellungen wechseln nur zwischen Betriebssystemversionen</span><span class="sxs-lookup"><span data-stu-id="42df2-174">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="42df2-175">Die Betriebssystemeinstellungen für Sprachausgaben und Währungszeichen, die für das gebietsschemaspezifisch sind, werden nur wie Betriebssystemversionen von Windows durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="42df2-175">Operating system settings for Narrator and currency characters specific to the locale will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="42df2-176">Währungszeichen können beispielsweise nur von Windows 7 zu Windows 7 gewechselt werden.</span><span class="sxs-lookup"><span data-stu-id="42df2-176">For example currency characters will only roam from Windows 7 to Windows 7.</span></span>

<span data-ttu-id="42df2-177">Problemumgehung: keine</span><span class="sxs-lookup"><span data-stu-id="42df2-177">WORKAROUND: None</span></span>

### <span data-ttu-id="42df2-178">Internet Explorer-Lesezeichen werden in der SmartBar von Internet Explorer nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="42df2-178">Internet Explorer bookmarks do not appear in the Internet Explorer smartbar</span></span>

<span data-ttu-id="42df2-179">Wenn Internet Explorer-Lesezeichen von einem Computer auf einen anderen Computer übertragen werden, kann der Index auf dem zweiten Computer nicht aktualisiert werden, sodass der Favorit beim eingeben in der Adressleiste nicht als mögliches Suchergebnis auf Computer 2 angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="42df2-179">When Internet Explorer bookmarks roam from one computer to another computer, the index on the second computer cannot update, so when typing in the address bar, the favorite will not appear as a possible search result on computer 2.</span></span>

<span data-ttu-id="42df2-180">Problemumgehung: keine</span><span class="sxs-lookup"><span data-stu-id="42df2-180">WORKAROUND: None</span></span>

 

 





