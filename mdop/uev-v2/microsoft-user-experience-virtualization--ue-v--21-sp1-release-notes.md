---
title: Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.1 SP1
description: Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.1 SP1
author: dansimp
ms.assetid: 561988c4-cc5c-4e15-970b-16e942c8f2ef
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/30/2017
ms.openlocfilehash: 974914421c61c829b5a32e336bddf8ea1addf514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811212"
---
# <span data-ttu-id="68f74-103">Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.1 SP1</span><span class="sxs-lookup"><span data-stu-id="68f74-103">Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes</span></span>


<span data-ttu-id="68f74-104">Drücken Sie STRG + F, um die Microsoft User Experience Virtualization 2,1 SP1-Versionshinweise zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="68f74-104">To search Microsoft User Experience Virtualization 2.1 SP1 release notes, press Ctrl+F.</span></span>

<span data-ttu-id="68f74-105">Lesen Sie diese Versionshinweise gründlich, bevor Sie UE-V installieren.</span><span class="sxs-lookup"><span data-stu-id="68f74-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="68f74-106">Die Anmerkungen zu dieser Version enthalten Informationen, die erforderlich sind, um die Virtualisierung der Benutzeroberfläche erfolgreich zu installieren, und zusätzliche Informationen enthalten, die in der Produktdokumentation nicht zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="68f74-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="68f74-107">Wenn es Unterschiede zwischen diesen Versionshinweisen und anderen UE-V-Dokumentationen gibt, sollte die neueste Änderung als autorisierend angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="68f74-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="68f74-108">Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="68f74-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="68f74-109">Abgeben von Feedback</span><span class="sxs-lookup"><span data-stu-id="68f74-109">Providing feedback</span></span>


<span data-ttu-id="68f74-110">Teilen Sie uns Ihre Meinung zu unserer Dokumentation zu MDOP mit, indem Sie uns Feedback und Kommentare geben.</span><span class="sxs-lookup"><span data-stu-id="68f74-110">Tell us what you think about our documentation for MDOP by giving us your feedback and comments.</span></span> <span data-ttu-id="68f74-111">Senden Sie Ihr Feedback zur Dokumentation an [mdopdocs@Microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span><span class="sxs-lookup"><span data-stu-id="68f74-111">Send your documentation feedback to [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span></span>

## <span data-ttu-id="68f74-112">Bekannte Probleme in UE-V</span><span class="sxs-lookup"><span data-stu-id="68f74-112">UE-V known issues</span></span>


<span data-ttu-id="68f74-113">Dieser Abschnitt enthält Anmerkungen zu dieser Version von User Experience Virtualization 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="68f74-113">This section contains release notes for User Experience Virtualization 2.1 SP1.</span></span>

### <span data-ttu-id="68f74-114">Standort Vorlagen für die UE-V-Einstellungen für Skype führen zum Absturz von Skype</span><span class="sxs-lookup"><span data-stu-id="68f74-114">UE-V settings location templates for Skype cause Skype to crash</span></span>

<span data-ttu-id="68f74-115">Wenn ein Benutzer eine gültige Einstellungen-Standort Vorlage für die Skype-Desktopanwendung erstellt, diese registriert und dann die Skype-Desktopanwendung startet, stürzt Skype ab.</span><span class="sxs-lookup"><span data-stu-id="68f74-115">When a user generates a valid settings location template for the Skype desktop application, registers it, and then launches the Skype desktop application, Skype crashes.</span></span> <span data-ttu-id="68f74-116">Eine Access-_VIOLATION wird im Ereignisprotokoll der Anwendung aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="68f74-116">An ACCESS\_VIOLATION is recorded in the Application Event Log.</span></span>

<span data-ttu-id="68f74-117">Problemumgehung: Entfernen Sie die Skype-Vorlage, oder heben Sie die Registrierung auf, damit Skype wieder funktioniert.</span><span class="sxs-lookup"><span data-stu-id="68f74-117">WORKAROUND: Remove or unregister the Skype template to allow Skype to work again.</span></span>

### <span data-ttu-id="68f74-118">Vorhandene Skripts für unbeaufsichtigte Installationen von UE-V können fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="68f74-118">Existing scripts for silent installations of UE-V may fail</span></span>

<span data-ttu-id="68f74-119">Zwei Änderungen am UE-v-Installationsprogramm können dazu führen, dass Silent-Installationsskripts, die bei früheren Versionen von UE-v funktioniert haben, bei der Installation von UE-v 2,1 SP1 fehlerhaft sind.</span><span class="sxs-lookup"><span data-stu-id="68f74-119">Two changes made to the UE-V installer can cause silent installation scripts that worked for previous versions of UE-V to fail when installing UE-V 2.1 SP1.</span></span> <span data-ttu-id="68f74-120">Die erste ist eine neue Anforderung, dass Benutzer die Lizenzbedingungen akzeptieren und die Teilnahme am Programm zur Verbesserung der Benutzerfreundlichkeit (User Experience Improvement Program, CEIP) zustimmen oder ablehnen müssen, selbst während einer unbeaufsichtigten Installation.</span><span class="sxs-lookup"><span data-stu-id="68f74-120">The first is a new requirement that users must accept the license terms and agree to or decline participation in the Customer Experience Improvement Program (CEIP), even during a silent installation.</span></span> <span data-ttu-id="68f74-121">Die Verwendung des/q-Parameters reicht nicht mehr aus, um die Akzeptanz der Lizenzbedingungen und der Vereinbarung zur Teilnahme am CEIP anzugeben.</span><span class="sxs-lookup"><span data-stu-id="68f74-121">Using the /q parameter is no longer sufficient to indicate acceptance of the license terms and agreement to participate in CEIP.</span></span>

<span data-ttu-id="68f74-122">Zweitens erzwingt das Installationsprogramm nach der Installation des UE-V-Agents nun einen Neustart des Computers.</span><span class="sxs-lookup"><span data-stu-id="68f74-122">Second, the installer now forces a computer restart after installing the UE-V Agent.</span></span> <span data-ttu-id="68f74-123">Dies kann dazu führen, dass ein Installationsskript fehlschlägt, wenn der Neustart nicht erwartet wird (beispielsweise wird zuerst der UE-V-Agent installiert und dann der Generator sofort installiert).</span><span class="sxs-lookup"><span data-stu-id="68f74-123">This can cause an install script to fail if it is not expecting the restart (for example, it installs the UE-V Agent first and then immediately installs the generator).</span></span>

<span data-ttu-id="68f74-124">Problemumgehung: das UE-V-Installationsprogramm (MSI) verfügt über zwei neue Befehlszeilenparameter, die unbeaufsichtigte Installationen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="68f74-124">WORKAROUND: The UE-V installer (.msi) has two new command-line parameters that support silent installations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="68f74-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="68f74-125">Parameter</span></span></th>
<th align="left"><span data-ttu-id="68f74-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68f74-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="68f74-127">/ACCEPTLICENSETERMS = wahr</span><span class="sxs-lookup"><span data-stu-id="68f74-127">/ACCEPTLICENSETERMS=True</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="68f74-128">Legen Sie diesen Parameter auf "true" fest <strong> </strong> , um UE-V lautlos zu installieren.</span><span class="sxs-lookup"><span data-stu-id="68f74-128">Set this parameter to <strong>True</strong> to install UE-V silently.</span></span> <span data-ttu-id="68f74-129">Das Hinzufügen dieses Parameters impliziert, dass der Benutzer die UE-V-Lizenzbestimmungen akzeptiert, die hier (standardmäßig) gefunden werden:%ProgramFiles%\Microsoft-Benutzeroberflächen-Virtualization\Agent</span><span class="sxs-lookup"><span data-stu-id="68f74-129">Adding this parameter implies that the user accepts the UE-V license terms, which are found (by default) here: %ProgramFiles%\Microsoft User Experience Virtualization\Agent</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="68f74-130">/NORESTART</span><span class="sxs-lookup"><span data-stu-id="68f74-130">/NORESTART</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="68f74-131">Dieser Parameter verhindert den obligatorischen Neustart nach der Installation des UE-V-Agents.</span><span class="sxs-lookup"><span data-stu-id="68f74-131">This parameter prevents the mandatory restart after the UE-V agent is installed.</span></span> <span data-ttu-id="68f74-132">Ein Rückgabecode von 3010 gibt an, dass vor der Verwendung von UE-V ein Neustart erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="68f74-132">A return code of 3010 indicates that a restart is required prior to using UE-V.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="68f74-133">Registrierungseinstellungen werden nicht zwischen App-V und systemeigenen Anwendungen auf demselben Computer synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="68f74-133">Registry settings do not synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="68f74-134">Wenn ein Computer über eine Anwendung verfügt, die sowohl über Application Virtualization (App-V) als auch lokal mit einer Windows Installer-Datei (MSI) installiert ist, werden die registrierungsbasierten Einstellungen nicht zwischen den Technologien synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="68f74-134">When a computer has an application that is installed through both Application Virtualization (App-V) and locally with a Windows Installer (.msi) file, the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="68f74-135">Problemumgehung: um dieses Problem zu beheben, führen Sie die Anwendung aus, indem Sie eine der beiden Technologien auswählen, aber nicht beide.</span><span class="sxs-lookup"><span data-stu-id="68f74-135">WORKAROUND: To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <span data-ttu-id="68f74-136">Unvorhersehbare Ergebnisse mit installiertem Office 2010 und Office 2013</span><span class="sxs-lookup"><span data-stu-id="68f74-136">Unpredictable results with both Office 2010 and Office 2013 installed</span></span>

<span data-ttu-id="68f74-137">Wenn ein Benutzer sowohl Office 2010 als auch Office 2013 installiert hat, werden alle gängigen Einstellungen zwischen den beiden Office-Versionen von UE-V durchsucht.</span><span class="sxs-lookup"><span data-stu-id="68f74-137">When a user has both Office 2010 and Office 2013 installed, any common settings between the two versions of Office are roamed by UE-V.</span></span> <span data-ttu-id="68f74-138">Dies kann dazu führen, dass die Größe des Office 2010-Pakets recht groß ist oder zu unvorhersehbaren Konflikten mit 2013 führt, insbesondere dann, wenn Office 365 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="68f74-138">This could cause the Office 2010 package size to be quite large or result in unpredictable conflicts with 2013, particularly if Office 365 is used.</span></span>

<span data-ttu-id="68f74-139">Problemumgehung: Installieren Sie nur eine Version von Office, oder begrenzen Sie, welche Einstellungen von UE-V synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="68f74-139">WORKAROUND: Install only one version of Office or limit which settings are synchronized by UE-V.</span></span>

### <span data-ttu-id="68f74-140">Deinstallieren und erneutes Installieren der Windows 8-App kehrt Einstellungen in den Anfangszustand zurück</span><span class="sxs-lookup"><span data-stu-id="68f74-140">Uninstall and re-install of Windows 8 app reverts settings to initial state</span></span>

<span data-ttu-id="68f74-141">Bei Verwendung der UE-V-Synchronisierungseinstellungen für eine Windows 8-App werden die Einstellungen der APP wieder auf die Standardwerte zurückgesetzt, wenn der Benutzer die APP deinstalliert und die APP dann neu installiert.</span><span class="sxs-lookup"><span data-stu-id="68f74-141">While using UE-V settings synchronization for a Windows 8 app, if the user uninstalls the app and then reinstalls the app, the app’s settings revert to their default values.</span></span><span data-ttu-id="68f74-142">Dies geschieht, weil die Deinstallation die lokale (zwischengespeicherte) Kopie der App-Einstellungen entfernt, aber nicht das lokale UE-V-Einstellungspaket entfernt.</span><span class="sxs-lookup"><span data-stu-id="68f74-142"> This happens because the uninstall removes the local (cached) copy of the app’s settings but does not remove the local UE-V settings package.</span></span><span data-ttu-id="68f74-143">Wenn die APP neu installiert und gestartet wird, sammeln UE-V die App-Einstellungen, die auf die APP-Standardeinstellungen zurückgesetzt wurden, und laden dann die Standardeinstellungen an den zentralen Speicherort hoch.</span><span class="sxs-lookup"><span data-stu-id="68f74-143"> When the app is reinstalled and launched, UE-V gather the app settings that were reset to the app defaults and then uploads the default settings to the central storage location.</span></span><span data-ttu-id="68f74-144">Auf anderen Computern, auf denen die app ausgeführt wird, werden die Standardeinstellungen heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="68f74-144"> Other computers running the app then download the default settings.</span></span><span data-ttu-id="68f74-145">Dieses Verhalten ist mit dem Verhalten von Desktopanwendungen identisch.</span><span class="sxs-lookup"><span data-stu-id="68f74-145"> This behavior is identical to the behavior of desktop applications.</span></span>

<span data-ttu-id="68f74-146">Problemumgehung: keine.</span><span class="sxs-lookup"><span data-stu-id="68f74-146">WORKAROUND: None.</span></span>

### <span data-ttu-id="68f74-147">UE-V unterstützt keine Roamingeinstellungen zwischen 32-Bit-und 64-Bit-Versionen von Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="68f74-147">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="68f74-148">Wir empfehlen, die 32-Bit-Version von Microsoft Office sowohl für 32-Bit-als auch für 64-Bit-Betriebssysteme zu installieren.</span><span class="sxs-lookup"><span data-stu-id="68f74-148">We recommend that you install the 32-bit version of Microsoft Office for both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="68f74-149">Wenn Sie die von Ihnen benötigte Microsoft Office-Version auswählen möchten, klicken Sie hier.</span><span class="sxs-lookup"><span data-stu-id="68f74-149">To choose the Microsoft Office version that you need, click here.</span></span> <span data-ttu-id="68f74-150">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span><span class="sxs-lookup"><span data-stu-id="68f74-150">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span></span> <span data-ttu-id="68f74-151">UE-V unterstützt Roamingeinstellungen zwischen identischen Architekturversionen von Office.</span><span class="sxs-lookup"><span data-stu-id="68f74-151">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="68f74-152">Beispielsweise werden die Office-Einstellungen für 32-Bit zwischen allen 32-Bit-Office-Instanzen durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="68f74-152">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="68f74-153">UE-V unterstützt keine Roamingeinstellungen zwischen 32-Bit-und 64-Bit-Versionen von Office.</span><span class="sxs-lookup"><span data-stu-id="68f74-153">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="68f74-154">Problemumgehung: keine</span><span class="sxs-lookup"><span data-stu-id="68f74-154">WORKAROUND: None</span></span>

### <a href="" id="msi-s-are-not-localized"></a><span data-ttu-id="68f74-155">MSI-Versionen sind nicht lokalisiert</span><span class="sxs-lookup"><span data-stu-id="68f74-155">MSI’s are not localized</span></span>

<span data-ttu-id="68f74-156">UE-v umfasst ein lokalisiertes Setupprogramm für den UE-v-Agent und den UE-v-Generator.</span><span class="sxs-lookup"><span data-stu-id="68f74-156">UE-V includes a localized setup program for both the UE-V Agent and UE-V generator.</span></span> <span data-ttu-id="68f74-157">Diese MSI-Dateien sind weiterhin verfügbar, die Benutzeroberfläche wird jedoch minimiert, und die MSI-Datei wird nur in Englisch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="68f74-157">These MSI files are still available but the user interface is minimized and the MSI’s only display in English.</span></span> <span data-ttu-id="68f74-158">Obwohl die Datei in Englisch ist, werden alle unterstützten Sprachen während der Installation von dem Setup-Programm installiert.</span><span class="sxs-lookup"><span data-stu-id="68f74-158">Despite the file being in English, the setup program installs all supported languages during the installation.</span></span>

<span data-ttu-id="68f74-159">Problemumgehung: keine</span><span class="sxs-lookup"><span data-stu-id="68f74-159">WORKAROUND: None</span></span>

### <span data-ttu-id="68f74-160">Favicons, die mit Internet Explorer 9-Favoriten verknüpft sind, werden nicht durchwandert</span><span class="sxs-lookup"><span data-stu-id="68f74-160">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="68f74-161">Die Favicons, die mit Internet Explorer 9-Favoriten verknüpft sind, werden nicht von der Benutzeroberflächen-Virtualisierung durchlaufen und nicht angezeigt, wenn die Favoriten auf einem neuen Computer erstmalig angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="68f74-161">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="68f74-162">Problemumgehung: Favicons werden mit den zugehörigen Favoriten angezeigt, sobald die Textmarke verwendet und im Internet Explorer 9-Browser zwischengespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="68f74-162">WORKAROUND: Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="68f74-163">Datei Einstellungs Pfade werden in der Registrierung gespeichert</span><span class="sxs-lookup"><span data-stu-id="68f74-163">File settings paths are stored in registry</span></span>

<span data-ttu-id="68f74-164">In einigen Anwendungseinstellungen werden die Pfade Ihrer Konfigurations-und Einstellungsdateien als Werte in der Registrierung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="68f74-164">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="68f74-165">Die Dateien, die als Pfade in der Registrierung referenziert werden, müssen synchronisiert werden, wenn die Einstellungen zwischen Computern durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="68f74-165">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="68f74-166">Problemumgehung: Verwenden Sie die Ordnerumleitung oder eine andere Technologie, um sicherzustellen, dass alle Dateien, auf die als Pfad für Datei Einstellungen verwiesen wird, vorhanden sind und auf allen Computern, auf denen die Einstellungen durchlaufen werden, an derselben Stelle abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="68f74-166">WORKAROUND: Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="68f74-167">Lange Einstellungen Speicherpfade können einen Fehler verursachen</span><span class="sxs-lookup"><span data-stu-id="68f74-167">Long Settings Storage Paths could cause an error</span></span>

<span data-ttu-id="68f74-168">Behalten Sie die Einstellungen für den Speicherpfad so kurz wie möglich.</span><span class="sxs-lookup"><span data-stu-id="68f74-168">Keep settings storage paths as short as possible.</span></span> <span data-ttu-id="68f74-169">Lange Pfade können die Auflösung oder Synchronisierung verhindern.</span><span class="sxs-lookup"><span data-stu-id="68f74-169">Long paths could prevent resolution or synchronization.</span></span> <span data-ttu-id="68f74-170">UE-V verwendet den Einstellungsspeicher Pfad als Teil des berechneten Pfads zum Speichern von Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="68f74-170">UE-V uses the Settings storage path as part of the calculated path to store settings.</span></span> <span data-ttu-id="68f74-171">Dieser Pfad wird folgendermaßen berechnet: Einstellungsspeicher Pfad + "settingspackages" + Paket dir (Vorlagen-ID) + Paketname (Vorlagen-ID) +. pkgx.</span><span class="sxs-lookup"><span data-stu-id="68f74-171">That path is calculated in the following way: settings storage path + “settingspackages” + package dir (template ID) + package name (template ID) + .pkgx.</span></span> <span data-ttu-id="68f74-172">Wenn der berechnete Pfad 260 Zeichen überschreitet, schlägt der Paketspeicher fehl, und es wird die folgende Fehlermeldung im operationellen UE-V-Ereignisprotokoll generiert:</span><span class="sxs-lookup"><span data-stu-id="68f74-172">If that calculated path exceeds 260 characters, package storage will fail and generate the following error message in the UE-V operational event log:</span></span>

`[boost::filesystem::copy_file: The system cannot find the path specified]`

<span data-ttu-id="68f74-173">Zum Überprüfen der Betriebsprotokoll Ereignisse öffnen Sie die Ereignisanzeige, und navigieren Sie zu Anwendungen und Dienstprotokolle/Microsoft/User Experience Virtualization/Logging/Operational.</span><span class="sxs-lookup"><span data-stu-id="68f74-173">To check the operational log events, open the Event Viewer and navigate to Applications and Services Logs / Microsoft / User Experience Virtualization / Logging / Operational.</span></span>

<span data-ttu-id="68f74-174">Problemumgehung: keine.</span><span class="sxs-lookup"><span data-stu-id="68f74-174">WORKAROUND: None.</span></span>

### <span data-ttu-id="68f74-175">Einige Betriebssystemeinstellungen wechseln nur zwischen Betriebssystemversionen</span><span class="sxs-lookup"><span data-stu-id="68f74-175">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="68f74-176">Die Betriebssystemeinstellungen für Sprachausgaben und Währungszeichen, die für das gebietsschemaspezifisch sind (also sprach-und Regionaleinstellungen), werden nur über die Betriebssystemversionen von Windows durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="68f74-176">Operating system settings for Narrator and currency characters specific to the locale (i.e. language and regional settings) will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="68f74-177">Währungszeichen werden beispielsweise nicht zwischen Windows 7 und Windows 8 durchwandert.</span><span class="sxs-lookup"><span data-stu-id="68f74-177">For example, currency characters will not roam between Windows 7 and Windows 8.</span></span>

<span data-ttu-id="68f74-178">Problemumgehung: keine</span><span class="sxs-lookup"><span data-stu-id="68f74-178">WORKAROUND: None</span></span>

### <a href="" id="ue-v-1-agent-generates-errors-when-running-ue-v-2-templates-"></a><span data-ttu-id="68f74-179">UE-v 1-Agent generiert Fehler beim Ausführen von UE-v 2-Vorlagen</span><span class="sxs-lookup"><span data-stu-id="68f74-179">UE-V 1 agent generates errors when running UE-V 2 templates</span></span>

<span data-ttu-id="68f74-180">Wenn eine Standort Vorlage für die UE-v 2-Einstellungen an einen Computer verteilt wird, der mit einem UE-v 1-Agent installiert ist, können einige Einstellungen nicht zwischen Computern synchronisiert werden, und der Agent meldet Fehler im Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="68f74-180">If a UE-V 2 settings location template is distributed to a computer installed with a UE-V 1 agent, some settings fail to synchronize between computers and the agent reports errors in the event log.</span></span>

<span data-ttu-id="68f74-181">Problemumgehung: Wenn Sie von UE-v 1 zu UE-v 2 migrieren und wahrscheinlich auf Computern die vorherige Version des Agents ausgeführt wird, erstellen Sie einen separaten UE-v 2. x-Katalog, um den UE-v 2. x-Agent und die Vorlagen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="68f74-181">WORKAROUND: When migrating from UE-V 1 to UE-V 2 and it is likely you’ll have computers running the previous version of the agent, create a separate UE-V 2.x catalog to support the UE-V 2.x Agent and templates.</span></span>

### <span data-ttu-id="68f74-182">UE-V-Abmelde Verzögerung</span><span class="sxs-lookup"><span data-stu-id="68f74-182">UE-V logoff delay</span></span>

<span data-ttu-id="68f74-183">Beim Abmelden nimmt UE-V gelegentlich eine lange Zeit für die Synchronisierung von Einstellungen in Anspruch.</span><span class="sxs-lookup"><span data-stu-id="68f74-183">Occasionally on logoff, UE-V takes a long time to sync settings.</span></span> <span data-ttu-id="68f74-184">In der Regel liegt dies an einem Netzwerk mit höherer Latenz oder einer falschen Verwendung des distrubuted-Dateisystems (DFS).</span><span class="sxs-lookup"><span data-stu-id="68f74-184">Typically, this is due to a high latency network or incorrect use of Distrubuted File System (DFS).</span></span>
<span data-ttu-id="68f74-185">Informationen zur DFS-Unterstützung finden Sie [in der Microsoft-Support-Anweisung rund um replizierte Benutzerprofildaten](https://support.microsoft.com/kb/2533009) .</span><span class="sxs-lookup"><span data-stu-id="68f74-185">For DFS support, see [Microsoft’s Support Statement Around Replicated User Profile Data](https://support.microsoft.com/kb/2533009) for further details.</span></span>

<span data-ttu-id="68f74-186">Problemumgehung: beginnend mit HF03 wurde ein neuer Registrierungsschlüssel eingeführt der folgende Registrierungsschlüssel bietet einen Mechanismus, mit dem die maximale Abmelde Verzögerung angegeben werden kann \\Software\\Microsoft\\UEV\\Agent\\Configuration\\LogOffWaitInterval</span><span class="sxs-lookup"><span data-stu-id="68f74-186">WORKAROUND: Starting with HF03, a new registry key has been introduced The following registry key provides a mechanism by which the maximum logoff delay can be specified \\Software\\Microsoft\\UEV\\Agent\\Configuration\\LogOffWaitInterval</span></span>

<span data-ttu-id="68f74-187">Weitere Informationen finden Sie unter [UE-V-Registrierungseinstellungen](https://support.microsoft.com/kb/2770042) .</span><span class="sxs-lookup"><span data-stu-id="68f74-187">See [UE-V registry settings](https://support.microsoft.com/kb/2770042) for further details</span></span>

## <span data-ttu-id="68f74-188">Hotfixes und Knowledge Base-Artikel für UE-V 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="68f74-188">Hotfixes and Knowledge Base articles for UE-V 2.1 SP1</span></span>


<span data-ttu-id="68f74-189">Dieser Abschnitt enthält Hotfixes und KB-Artikel für UE-V 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="68f74-189">This section contains hotfixes and KB articles for UE-V 2.1 SP1.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="68f74-190">KB-Artikel</span><span class="sxs-lookup"><span data-stu-id="68f74-190">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="68f74-191">Title</span><span class="sxs-lookup"><span data-stu-id="68f74-191">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="68f74-192">Link</span><span class="sxs-lookup"><span data-stu-id="68f74-192">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68f74-193">3018608</span><span class="sxs-lookup"><span data-stu-id="68f74-193">3018608</span></span></p></td>
<td align="left"><p><span data-ttu-id="68f74-194">UE-v 2,1 – TemplateConsole.exe stürzt ab, wenn UE-v-WMI-Klassen fehlen</span><span class="sxs-lookup"><span data-stu-id="68f74-194">UE-V 2.1 - TemplateConsole.exe crashes when UE-V WMI classes are missing</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3018608/EN-US" data-raw-source="[support.microsoft.com/kb/3018608/EN-US](https://support.microsoft.com/kb/3018608/EN-US)"><span data-ttu-id="68f74-195">support.microsoft.com/kb/3018608/EN-US</span><span class="sxs-lookup"><span data-stu-id="68f74-195">support.microsoft.com/kb/3018608/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68f74-196">2903501</span><span class="sxs-lookup"><span data-stu-id="68f74-196">2903501</span></span></p></td>
<td align="left"><p><span data-ttu-id="68f74-197">UE-v: User Experience Virtualization (UE-v)-Kompatibilität mit Benutzerprofilen</span><span class="sxs-lookup"><span data-stu-id="68f74-197">UE-V: User Experience Virtualization (UE-V) compatibility with user profiles</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2903501/EN-US" data-raw-source="[support.microsoft.com/kb/2903501/EN-US](https://support.microsoft.com/kb/2903501/EN-US)"><span data-ttu-id="68f74-198">support.microsoft.com/kb/2903501/EN-US</span><span class="sxs-lookup"><span data-stu-id="68f74-198">support.microsoft.com/kb/2903501/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68f74-199">2770042</span><span class="sxs-lookup"><span data-stu-id="68f74-199">2770042</span></span></p></td>
<td align="left"><p><span data-ttu-id="68f74-200">UE-V-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="68f74-200">UE-V Registry Settings</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2770042/EN-US" data-raw-source="[support.microsoft.com/kb/2770042/EN-US](https://support.microsoft.com/kb/2770042/EN-US)"><span data-ttu-id="68f74-201">support.microsoft.com/kb/2770042/EN-US</span><span class="sxs-lookup"><span data-stu-id="68f74-201">support.microsoft.com/kb/2770042/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68f74-202">2847017</span><span class="sxs-lookup"><span data-stu-id="68f74-202">2847017</span></span></p></td>
<td align="left"><p><span data-ttu-id="68f74-203">Von Internet Explorer replizierte UE-V-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="68f74-203">UE-V settings replicated by Internet Explorer</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2847017/EN-US" data-raw-source="[support.microsoft.com/kb/2847017/EN-US](https://support.microsoft.com/kb/2847017/EN-US)"><span data-ttu-id="68f74-204">support.microsoft.com/kb/2847017/EN-US</span><span class="sxs-lookup"><span data-stu-id="68f74-204">support.microsoft.com/kb/2847017/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68f74-205">2769631</span><span class="sxs-lookup"><span data-stu-id="68f74-205">2769631</span></span></p></td>
<td align="left"><p><span data-ttu-id="68f74-206">Reparieren einer beschädigten UE-V-Installation</span><span class="sxs-lookup"><span data-stu-id="68f74-206">How to repair a corrupted UE-V install</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769631/EN-US" data-raw-source="[support.microsoft.com/kb/2769631/EN-US](https://support.microsoft.com/kb/2769631/EN-US)"><span data-ttu-id="68f74-207">support.microsoft.com/kb/2769631/EN-US</span><span class="sxs-lookup"><span data-stu-id="68f74-207">support.microsoft.com/kb/2769631/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68f74-208">2850989</span><span class="sxs-lookup"><span data-stu-id="68f74-208">2850989</span></span></p></td>
<td align="left"><p><span data-ttu-id="68f74-209">Das Migrieren von MAPI-Profilen mit Microsoft UE-V wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="68f74-209">Migrating MAPI profiles with Microsoft UE-V is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850989/EN-US" data-raw-source="[support.microsoft.com/kb/2850989/EN-US](https://support.microsoft.com/kb/2850989/EN-US)"><span data-ttu-id="68f74-210">support.microsoft.com/kb/2850989/EN-US</span><span class="sxs-lookup"><span data-stu-id="68f74-210">support.microsoft.com/kb/2850989/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68f74-211">2769586</span><span class="sxs-lookup"><span data-stu-id="68f74-211">2769586</span></span></p></td>
<td align="left"><p><span data-ttu-id="68f74-212">UE-V durchstreift leere Ordner und Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="68f74-212">UE-V roams empty folders and registry keys</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769586/EN-US" data-raw-source="[support.microsoft.com/kb/2769586/EN-US](https://support.microsoft.com/kb/2769586/EN-US)"><span data-ttu-id="68f74-213">support.microsoft.com/kb/2769586/EN-US</span><span class="sxs-lookup"><span data-stu-id="68f74-213">support.microsoft.com/kb/2769586/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68f74-214">2782997</span><span class="sxs-lookup"><span data-stu-id="68f74-214">2782997</span></span></p></td>
<td align="left"><p><span data-ttu-id="68f74-215">Aktivieren der Debug-Protokollierung in Microsoft User Experience Virtualization (UE-V)</span><span class="sxs-lookup"><span data-stu-id="68f74-215">How To Enable Debug Logging in Microsoft User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2782997/EN-US" data-raw-source="[support.microsoft.com/kb/2782997/EN-US](https://support.microsoft.com/kb/2782997/EN-US)"><span data-ttu-id="68f74-216">support.microsoft.com/kb/2782997/EN-US</span><span class="sxs-lookup"><span data-stu-id="68f74-216">support.microsoft.com/kb/2782997/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68f74-217">2769570</span><span class="sxs-lookup"><span data-stu-id="68f74-217">2769570</span></span></p></td>
<td align="left"><p><span data-ttu-id="68f74-218">UE-V aktualisiert das Design nicht in RDS-oder VDI-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="68f74-218">UE-V does not update the theme on RDS or VDI sessions</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769570/EN-US" data-raw-source="[support.microsoft.com/kb/2769570/EN-US](https://support.microsoft.com/kb/2769570/EN-US)"><span data-ttu-id="68f74-219">support.microsoft.com/kb/2769570/EN-US</span><span class="sxs-lookup"><span data-stu-id="68f74-219">support.microsoft.com/kb/2769570/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68f74-220">2850582</span><span class="sxs-lookup"><span data-stu-id="68f74-220">2850582</span></span></p></td>
<td align="left"><p><span data-ttu-id="68f74-221">Verwenden der Microsoft-Benutzeroberflächen-Virtualisierung mit App-V-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="68f74-221">How To Use Microsoft User Experience Virtualization With App-V Applications</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850582/EN-US" data-raw-source="[support.microsoft.com/kb/2850582/EN-US](https://support.microsoft.com/kb/2850582/EN-US)"><span data-ttu-id="68f74-222">support.microsoft.com/kb/2850582/EN-US</span><span class="sxs-lookup"><span data-stu-id="68f74-222">support.microsoft.com/kb/2850582/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68f74-223">3041879</span><span class="sxs-lookup"><span data-stu-id="68f74-223">3041879</span></span></p></td>
<td align="left"><p><span data-ttu-id="68f74-224">Aktuelle Dateiversionen für Microsoft User Experience Virtualization</span><span class="sxs-lookup"><span data-stu-id="68f74-224">Current file versions for Microsoft User Experience Virtualization</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3041879/EN-US" data-raw-source="[support.microsoft.com/kb/3041879/EN-US](https://support.microsoft.com/kb/3041879/EN-US)"><span data-ttu-id="68f74-225">support.microsoft.com/kb/3041879/EN-US</span><span class="sxs-lookup"><span data-stu-id="68f74-225">support.microsoft.com/kb/3041879/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68f74-226">2843592</span><span class="sxs-lookup"><span data-stu-id="68f74-226">2843592</span></span></p></td>
<td align="left"><p><span data-ttu-id="68f74-227">Informationen zur Benutzeroberflächen-Virtualisierung und zu einer höheren Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="68f74-227">Information on User Experience Virtualization and High Availability</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2843592/EN-US" data-raw-source="[support.microsoft.com/kb/2843592/EN-US](https://support.microsoft.com/kb/2843592/EN-US)"><span data-ttu-id="68f74-228">support.microsoft.com/kb/2843592/EN-US</span><span class="sxs-lookup"><span data-stu-id="68f74-228">support.microsoft.com/kb/2843592/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 






 

 





