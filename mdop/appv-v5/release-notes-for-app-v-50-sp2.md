---
title: Versionshinweise für App-V 5.0 SP2
description: Versionshinweise für App-V 5.0 SP2
author: dansimp
ms.assetid: fe73139d-240c-4ed5-8e59-6ae76ee8e80c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5e885e67023d0e5c1e36aeb340933c64ae92610e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804895"
---
# <span data-ttu-id="424ab-103">Versionshinweise für App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="424ab-103">Release Notes for App-V 5.0 SP2</span></span>


**<span data-ttu-id="424ab-104">Drücken Sie STRG + F, um nach einem bestimmten Problem in diesen Versionshinweisen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="424ab-104">To search for a specific issue in these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="424ab-105">Lesen Sie diese Versionshinweise gründlich, bevor Sie App-V 5,0 SP2 installieren.</span><span class="sxs-lookup"><span data-stu-id="424ab-105">Read these release notes thoroughly before you install App-V 5.0 SP2.</span></span>

<span data-ttu-id="424ab-106">Diese Anmerkungen zu dieser Version enthalten Informationen, die zur erfolgreichen Installation von App-V 5,0 SP2 erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="424ab-106">These release notes contain information that is required to successfully install App-V 5.0 SP2.</span></span> <span data-ttu-id="424ab-107">Die Anmerkungen zu dieser Version enthalten auch Informationen, die in der Produktdokumentation nicht zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="424ab-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="424ab-108">Wenn es Unterschiede zwischen diesen Anmerkungen zu dieser Version und einer anderen App-V 5,0-Dokumentation gibt, sollte die neueste Änderung als autorisierend angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="424ab-108">If there are differences between these release notes and other App-V 5.0 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="424ab-109">Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="424ab-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="424ab-110">Informationen zur Produktdokumentation</span><span class="sxs-lookup"><span data-stu-id="424ab-110">About the Product Documentation</span></span>


<span data-ttu-id="424ab-111">Informationen zur APP-v 5,0-Dokumentation finden Sie auf der APP-v 5,0-Startseite auf der Microsoft TechNet-Website.</span><span class="sxs-lookup"><span data-stu-id="424ab-111">For information about App-V 5.0 documentation, see the App-V 5.0 home page on Microsoft TechNet.</span></span>

## <span data-ttu-id="424ab-112">Feedback geben</span><span class="sxs-lookup"><span data-stu-id="424ab-112">Provide Feedback</span></span>


<span data-ttu-id="424ab-113">Wir sind an Ihrem Feedback zu App-V 5,0 interessiert.</span><span class="sxs-lookup"><span data-stu-id="424ab-113">We are interested in your feedback on App-V 5.0.</span></span> <span data-ttu-id="424ab-114">Sie können Ihr Feedback an senden <mdopdocs@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="424ab-114">You can send your feedback to <mdopdocs@microsoft.com>.</span></span>

<span data-ttu-id="424ab-115">**Hinweis**  Diese e-Mail-Adresse ist kein Supportkanal, aber Ihr Feedback wird uns helfen, zukünftige Änderungen in unseren Dokumentations-und Produktversionen zu planen.</span><span class="sxs-lookup"><span data-stu-id="424ab-115">**Note** This email address is not a support channel, but your feedback will help us to plan for future changes in our documentation and product releases.</span></span>

 

<span data-ttu-id="424ab-116">Die neuesten Informationen zu MDOP und weiteren Lernressourcen finden Sie auf der Seite [MDOP-Informationen](https://go.microsoft.com/fwlink/p/?LinkId=236032) .</span><span class="sxs-lookup"><span data-stu-id="424ab-116">For the latest information about MDOP and additional learning resources, see the [MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) page.</span></span>

<span data-ttu-id="424ab-117">Wenn Sie weitere Informationen zu neuen Updates oder Feedback geben möchten, folgen Sie uns auf [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) oder [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="424ab-117">For more information about new updates or to provide feedback, follow us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

## <span data-ttu-id="424ab-118">Bekannte Probleme mit dem Hotfix-Paket 4 für Application Virtualization 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="424ab-118">Known Issues with Hotfix Package 4 for Application Virtualization 5.0 SP2</span></span>


### <span data-ttu-id="424ab-119">Pakete funktionieren nach dem Deinstallieren des Hotfix-Pakets 4 für Application Virtualization 5,0 SP2 nicht mehr</span><span class="sxs-lookup"><span data-stu-id="424ab-119">Packages stop working after you uninstall Hotfix Package 4 for Application Virtualization 5.0 SP2</span></span>

<span data-ttu-id="424ab-120">Pakete, die veröffentlicht werden, wenn Hotfix-Paket 4 für Application Virtualization 5,0 SP2 angewendet wird, funktionieren nicht mehr, wenn das Hotfix-Paket 4 für Application Virtualization 5,0 SP2 entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="424ab-120">Packages published when Hotfix Package 4 for Application Virtualization 5.0 SP2 is applied stop working when Hotfix Package 4 for Application Virtualization 5.0 SP2 is removed.</span></span>

<span data-ttu-id="424ab-121">WORKAROUND</span><span class="sxs-lookup"><span data-stu-id="424ab-121">WORKAROUND:</span></span>

<span data-ttu-id="424ab-122">Wenn der folgende Ordner vorhanden ist, müssen Sie ihn löschen:</span><span class="sxs-lookup"><span data-stu-id="424ab-122">If the following folder exists, then you must delete it:</span></span>

<span data-ttu-id="424ab-123">**% LocalAppData%**  \\  **Microsoft Office**  \\  **AppV**  \\  **Client**  \\  **VFS**  \\  die \*\* &lt; Paket &gt; -ID\*\* für jedes veröffentlichte Paket.</span><span class="sxs-lookup"><span data-stu-id="424ab-123">**%localappdata%** \\ **Microsoft** \\ **AppV** \\ **Client** \\ **VFS** \\ **&lt;package ID&gt;** for each package that was published.</span></span>

<span data-ttu-id="424ab-124">**Hinweis**  Sie müssen über erhöhte Berechtigungen verfügen, um diesen Ordner zu löschen.</span><span class="sxs-lookup"><span data-stu-id="424ab-124">**Note** You must have elevated privileges to delete this folder.</span></span>

 

<span data-ttu-id="424ab-125">So verwenden Sie ein Skript für jedes Benutzerkonto auf dem Computer und für jede Paket-ID, die nach der Installation des Hotfix-Pakets 4 für Application Virtualization 5,0 SP2 veröffentlicht wurde:</span><span class="sxs-lookup"><span data-stu-id="424ab-125">To use a script, for each user account on the computer and for each package id that was published after installing Hotfix Package 4 for Application Virtualization 5.0 SP2:</span></span>

`Rd /s /q “%systemdrive%\users\[UserName]\AppData\Local\Microsoft\AppV\Client\VFS\[Package ID]`

-   <span data-ttu-id="424ab-126">Die Tastenkombinationen bleiben auch nach dem Löschen des Ordners aus dem Verzeichnis im vorherigen Abschnitt in den Benutzersitzungen erhalten, sodass Sie auf die Verknüpfung klicken können, um die Anwendung erneut auszuführen.</span><span class="sxs-lookup"><span data-stu-id="424ab-126">The shortcuts will remain with the user sessions even after deleting the folder from the directory in the previous section, so you can click on the shortcut to run the application again.</span></span> <span data-ttu-id="424ab-127">Die Anwendung muss nicht erneut veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="424ab-127">There is no need to re-publish the application.</span></span>

-   <span data-ttu-id="424ab-128">Dieses Problem tritt für veröffentlichte, von Benutzern veröffentlichte, verpackte und Global veröffentlichte Pakete auf, beispielsweise Microsoft Office2013.</span><span class="sxs-lookup"><span data-stu-id="424ab-128">This issue happens for both user published packaged and globally published packages for example, Microsoft Office2013.</span></span> <span data-ttu-id="424ab-129">Der Ordner muss für beide Arten von Paketen gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="424ab-129">The folder must be deleted for both types of packages.</span></span>

-   <span data-ttu-id="424ab-130">Sie müssen den VFS-Ordner in den Roaming-App-Daten (**% AppData%**) nicht löschen.</span><span class="sxs-lookup"><span data-stu-id="424ab-130">You do not need to delete the VFS folder in the Roaming app data (**%appdata%**).</span></span> <span data-ttu-id="424ab-131">Nur die **% LocalAppData%** müssen gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="424ab-131">Only the **%localappdata%** must be deleted.</span></span>

### <span data-ttu-id="424ab-132">Microsoft Office-Integration verweist auf falschen Speicherort für das Dateisystem</span><span class="sxs-lookup"><span data-stu-id="424ab-132">Microsoft Office integration points to wrong file system location</span></span>

<span data-ttu-id="424ab-133">Microsoft Office-Integration verweist auf den falschen Speicherort des Dateisystems (Groove.exe-Fehlermeldung).</span><span class="sxs-lookup"><span data-stu-id="424ab-133">Microsoft Office integration points to wrong file system location (Groove.exe error message).</span></span>

<span data-ttu-id="424ab-134">WORKAROUND</span><span class="sxs-lookup"><span data-stu-id="424ab-134">WORKAROUND:</span></span>

<span data-ttu-id="424ab-135">Verwenden Sie eine der folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="424ab-135">Use one of the following methods:</span></span>

1.  <span data-ttu-id="424ab-136">Löschen Sie die Verknüpfung im Startordner nach dem Upgrade.</span><span class="sxs-lookup"><span data-stu-id="424ab-136">Delete the shortcut in the start-up folder after upgrade.</span></span>

2.  <span data-ttu-id="424ab-137">Ändern Sie die Verknüpfung im Startordner mithilfe eines Skripts.</span><span class="sxs-lookup"><span data-stu-id="424ab-137">Change the shortcut in the start-up folder using a script.</span></span>

3.  <span data-ttu-id="424ab-138">Verwenden Sie die Konfigurationsdatei für die Bereitstellung, um das Verknüpfungsziel für den Integrations Stamm festzulegen.</span><span class="sxs-lookup"><span data-stu-id="424ab-138">Use the deployment configuration file to specify the shortcut target to the integration root.</span></span>

### <a href="" id="-------------hotfix-package-4-for-application-virtualization-5-0-sp2-installer-can-take-a-long-time"></a> <span data-ttu-id="424ab-139">Hotfix-Paket 4 für Application Virtualization 5,0 SP2-Installationsprogramm kann sehr lange dauern</span><span class="sxs-lookup"><span data-stu-id="424ab-139">Hotfix Package 4 for Application Virtualization 5.0 SP2 installer can take a long time</span></span>

<span data-ttu-id="424ab-140">Das Hotfix-Paket 4 für das Application Virtualization 5,0 SP2-Installationsprogramm kann möglicherweise sehr lange dauern, je nachdem, wie viele Dateien im vorhandenen Paketcache gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="424ab-140">The Hotfix Package 4 for Application Virtualization 5.0 SP2 installer can potentially take a long time depending on how many files are stored in the existing package cache.</span></span>

<span data-ttu-id="424ab-141">Das Aktualisieren der zugehörigen Paket Sicherheitsbeschreibungen während des Hotfix-Pakets 4 für die Installation von Application Virtualization 5,0 SP2 hat erhebliche Auswirkungen darauf, wie lange die Installation dauern wird.</span><span class="sxs-lookup"><span data-stu-id="424ab-141">Updating associated package security descriptors during the Hotfix Package 4 for Application Virtualization 5.0 SP2 installation has a significant impact on how long it takes the installation will take.</span></span> <span data-ttu-id="424ab-142">Zuvor war die Installations Installation standardmäßig in Dauer.</span><span class="sxs-lookup"><span data-stu-id="424ab-142">Previously, the installation install was standard in duration.</span></span> <span data-ttu-id="424ab-143">Es hängt nun jedoch davon ab, wie viele Dateien im Paketcache bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="424ab-143">However, it now depends on how many files you have staged in the package cache.</span></span>

<span data-ttu-id="424ab-144">Problemumgehung: keine</span><span class="sxs-lookup"><span data-stu-id="424ab-144">WORKAROUND: None</span></span>

### <span data-ttu-id="424ab-145">Deinstallieren des Hotfix-Pakets 4 für Application Virtualization 5,0 SP2 schlägt fehl, wenn das JIT-V-Paket verwendet wird</span><span class="sxs-lookup"><span data-stu-id="424ab-145">Uninstalling Hotfix Package 4 for Application Virtualization 5.0 SP2 fails if JIT-V package is in use</span></span>

<span data-ttu-id="424ab-146">Wenn Sie das Hotfix-Paket 4 für Application Virtualization 5,0 SP2 installieren und dann versuchen, den Hotfix zu deinstallieren, wenn Just-in-Time-Virtualisierung (JIT-V) verwendet wird, schlägt der Vorgang fehl, wenn alle der folgenden Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="424ab-146">If you install Hotfix Package 4 for Application Virtualization 5.0 SP2 and then try to uninstall the hotfix when just-in-time virtualization (JIT-V) is being used, the operation will fail if all of the following conditions are true:</span></span>

-   <span data-ttu-id="424ab-147">Sie haben mithilfe einer Windows Installer-Datei (MSI) installiert, und Sie können Updates dann mithilfe einer Microsoft Installer-Patchdatei (MSP) anwenden.</span><span class="sxs-lookup"><span data-stu-id="424ab-147">You installed by using a Windows Installer file (.msi), and then you apply updates by using a Microsoft Installer Patch File (.msp).</span></span>

-   <span data-ttu-id="424ab-148">Sie versuchen, ein Update mithilfe des Elements "Software" in der Systemsteuerung zu deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="424ab-148">You try to uninstall an update by using the Add or Remove Programs item in Control Panel.</span></span>

-   <span data-ttu-id="424ab-149">Auf dem Computer wird ein JIT-V-fähiges Paket ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="424ab-149">A JIT-V-enabled package is running on the computer.</span></span>

<span data-ttu-id="424ab-150">Problemumgehung: führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="424ab-150">WORKAROUND: Complete the following steps:</span></span>

1.  <span data-ttu-id="424ab-151">Öffnen Sie Windows PowerShell, und führen Sie die folgenden Befehle aus:</span><span class="sxs-lookup"><span data-stu-id="424ab-151">Open Windows PowerShell and run the following commands:</span></span>

    -   **<span data-ttu-id="424ab-152">Import-Modul appvclient</span><span class="sxs-lookup"><span data-stu-id="424ab-152">Import-module appvclient</span></span>**

    -   **<span data-ttu-id="424ab-153">Get-AppvClientPackage | Stopp-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="424ab-153">Get-AppvClientPackage | Stop-AppvClientPackage</span></span>**

2.  <span data-ttu-id="424ab-154">Deinstallieren Sie das Update mithilfe von Software.</span><span class="sxs-lookup"><span data-stu-id="424ab-154">Uninstall the update using Add or Remove Programs.</span></span>

## <span data-ttu-id="424ab-155">Bekannte Probleme mit App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="424ab-155">Known Issues with App-V 5.0 SP2</span></span>


### <a href="" id="bkmk-folderredirection"></a><span data-ttu-id="424ab-156">App-V-Clientordner Umleitung schlägt manchmal fehl, um Dateien von% APPDATA% auf% LocalAppData% zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="424ab-156">App-V client folder redirection sometimes fails to move files from %AppData% to %LocalAppData%</span></span>

<span data-ttu-id="424ab-157">Wenn% APPDATA% ein freigegebener Netzwerkordner ist, den Sie für die Ordnerumleitung konfiguriert haben, können die Änderungen, die Endbenutzer an APPDATA (Roaming) vornehmen, verloren gehen, wenn Sie den Computer wechseln oder wenn die lokale APPDATA gelöscht wird, wenn Sie sich abmelden und dann wieder anmelden.</span><span class="sxs-lookup"><span data-stu-id="424ab-157">When %AppData% is a shared network folder that you have configured for folder redirection, the changes that end users make to AppData (Roaming) can be lost when they switch computers or when their local AppData is cleared when they log off and then log back on.</span></span> <span data-ttu-id="424ab-158">Dieser Fehler tritt auf, weil der Registrierungsschlüssel (AppDataTime), der den letzten bekannten Upload angibt, nicht mehr mit dem lokalen zwischengespeicherten APPDATA synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="424ab-158">This error occurs because the registry key (AppDataTime), which indicates the last known upload, gets out of synchronization with the local cached AppData.</span></span>

<span data-ttu-id="424ab-159">Problemumgehung: Löschen Sie den folgenden Registrierungsschlüssel für jedes relevante Paket manuell, wenn sich ein Endbenutzer anmeldet oder deaktiviert:</span><span class="sxs-lookup"><span data-stu-id="424ab-159">WORKAROUND: Manually delete the following registry key for each relevant package when an end user logs on or off:</span></span>

``` syntax
HKCU\Software\Microsoft\AppV\Client\Packages\<PACKAGE_GUID>\AppDataTime
```

<span data-ttu-id="424ab-160">Wenn Endbenutzer zum ersten Mal eine Anwendung im Paket starten, nachdem Sie sich angemeldet haben, erzwingt App-V einen Download des gezippten% APPDATA%, auch wenn% LocalAppData% bereits auf dem neuesten Stand ist.</span><span class="sxs-lookup"><span data-stu-id="424ab-160">The first time that end users start an application in the package after they log in, App-V forces a download of the zipped %AppData%, even if %LocalAppData% is already up to date.</span></span>

### <a href="" id="-------------app-v-5-0-service-pack-2--app-v-5-0-sp2--does-not-include-a-new-version-of-the-app-v-server"></a> <span data-ttu-id="424ab-161">App-v 5,0 Service Pack 2 (app-v 5,0 SP2) enthält keine neue Version des App-v-Servers</span><span class="sxs-lookup"><span data-stu-id="424ab-161">App-V 5.0 Service Pack 2 (App-V 5.0 SP2) does not include a new version of the App-V Server</span></span>

<span data-ttu-id="424ab-162">App-v 5.0 SP2 enthält keine neue Version des App-v-Servers.</span><span class="sxs-lookup"><span data-stu-id="424ab-162">App-V 5.0SP2 does not include a new version of the App-V Server.</span></span> <span data-ttu-id="424ab-163">Wenn Sie App-v 5,0 SP2-Clients mit Windows 8,1 in Ihrer Umgebung bereitstellen und planen, die Clients mithilfe der APP-v-Infrastruktur zu verwalten, müssen Sie das [Hotfix-Paket 2 für Microsoft Application Virtualization 5,0 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=386634)installieren.</span><span class="sxs-lookup"><span data-stu-id="424ab-163">If you deploy App-V 5.0 SP2 clients running Windows 8.1 in your environment and plan to manage the clients using the App-V infrastructure, you must install [Hotfix Package 2 for Microsoft Application Virtualization 5.0 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=386634).</span></span> <span data-ttu-id="424ab-164">(https://go.microsoft.com/fwlink/?LinkId=386634)</span><span class="sxs-lookup"><span data-stu-id="424ab-164">(https://go.microsoft.com/fwlink/?LinkId=386634)</span></span>

<span data-ttu-id="424ab-165">Wenn Sie App-V 5,0 SP2-Clients mit einer der folgenden Methoden ausführen und verwalten, ist kein Client Update erforderlich:</span><span class="sxs-lookup"><span data-stu-id="424ab-165">If you are running and managing App-V 5.0 SP2 clients using any of the following methods no client update is required:</span></span>

-   <span data-ttu-id="424ab-166">Eigenständiger Modus.</span><span class="sxs-lookup"><span data-stu-id="424ab-166">Standalone mode.</span></span>

-   <span data-ttu-id="424ab-167">Konfigurations-Manager.</span><span class="sxs-lookup"><span data-stu-id="424ab-167">Configuration Manager.</span></span>

-   <span data-ttu-id="424ab-168">ESD von Drittanbietern.</span><span class="sxs-lookup"><span data-stu-id="424ab-168">Third party ESD.</span></span>

<span data-ttu-id="424ab-169">Der App-V 5,0 SP2-Client ist vollständig mit Windows 8,1 kompatibel</span><span class="sxs-lookup"><span data-stu-id="424ab-169">The App-V 5.0 SP2 client is fully compatible with Windows 8.1</span></span>

<span data-ttu-id="424ab-170">Problemumgehung: keine.</span><span class="sxs-lookup"><span data-stu-id="424ab-170">WORKAROUND: None.</span></span>

## <span data-ttu-id="424ab-171">Anmerkungen zu dieser Version Copyright-Informationen</span><span class="sxs-lookup"><span data-stu-id="424ab-171">Release Notes Copyright Information</span></span>


<span data-ttu-id="424ab-172">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune und WindowsPowerShell sind Marken der Microsoft-Unternehmensgruppe.</span><span class="sxs-lookup"><span data-stu-id="424ab-172">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="424ab-173">Alle anderen Marken sind Eigentum ihrer jeweiligen Eigentümer.</span><span class="sxs-lookup"><span data-stu-id="424ab-173">All other trademarks are property of their respective owners.</span></span>








## <span data-ttu-id="424ab-174">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="424ab-174">Related topics</span></span>


[<span data-ttu-id="424ab-175">Informationen zu App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="424ab-175">About App-V 5.0 SP2</span></span>](about-app-v-50-sp2.md)

 

 





