---
title: Informationen über Clientkonfigurationseinstellungen
description: Informationen über Clientkonfigurationseinstellungen
author: dansimp
ms.assetid: cc7ae28c-b2ac-4f68-b992-5ccdbd5316a4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 289f5b35ac223d488152ff7ee1f42b1cf50341df
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806104"
---
# <span data-ttu-id="b83dc-103">Informationen über Clientkonfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="b83dc-103">About Client Configuration Settings</span></span>


<span data-ttu-id="b83dc-104">Der Microsoft Application Virtualization (App-V) 5,0-Client speichert seine Konfiguration in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="b83dc-104">The Microsoft Application Virtualization (App-V) 5.0 client stores its configuration in the registry.</span></span> <span data-ttu-id="b83dc-105">Sie können einige nützliche Informationen zu dem Client sammeln, wenn Sie das Format der Daten in der Registrierung verstehen.</span><span class="sxs-lookup"><span data-stu-id="b83dc-105">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="b83dc-106">Sie können auch viele Clientaktionen konfigurieren, indem Sie Registrierungseinträge ändern.</span><span class="sxs-lookup"><span data-stu-id="b83dc-106">You can also configure many client actions by changing registry entries.</span></span> <span data-ttu-id="b83dc-107">In diesem Thema werden die Konfigurationseinstellungen des App-V 5,0-Clients sowie deren Verwendung erläutert.</span><span class="sxs-lookup"><span data-stu-id="b83dc-107">This topic lists the App-V 5.0 Client configuration settings and explains their uses.</span></span> <span data-ttu-id="b83dc-108">Sie können PowerShell verwenden, um die Clientkonfigurationseinstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b83dc-108">You can use PowerShell to modify the client configuration settings.</span></span> <span data-ttu-id="b83dc-109">Weitere Informationen zur Verwendung von PowerShell und App-v 5,0 finden Sie unter [Verwalten von App-v mithilfe von PowerShell](administering-app-v-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="b83dc-109">For more information about using PowerShell and App-V 5.0 see [Administering App-V by Using PowerShell](administering-app-v-by-using-powershell.md).</span></span>

## <a href="" id="---------app-v-5-0-client-configuration-settings"></a> <span data-ttu-id="b83dc-110">App-V 5,0-Client Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="b83dc-110">App-V 5.0 Client Configuration Settings</span></span>


<span data-ttu-id="b83dc-111">In der folgenden Tabelle werden Informationen zu den Clientkonfigurationseinstellungen für App-V 5,0 angezeigt:</span><span class="sxs-lookup"><span data-stu-id="b83dc-111">The following table displays information about the App-V 5.0 client configuration settings:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b83dc-112">Einstellungs Name</span><span class="sxs-lookup"><span data-stu-id="b83dc-112">Setting Name</span></span></th>
<th align="left"><span data-ttu-id="b83dc-113">Setup-Flag</span><span class="sxs-lookup"><span data-stu-id="b83dc-113">Setup Flag</span></span></th>
<th align="left"><span data-ttu-id="b83dc-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b83dc-114">Description</span></span></th>
<th align="left"><span data-ttu-id="b83dc-115">Einstellungsoptionen</span><span class="sxs-lookup"><span data-stu-id="b83dc-115">Setting Options</span></span></th>
<th align="left"><span data-ttu-id="b83dc-116">Registrierungsschlüsselwert</span><span class="sxs-lookup"><span data-stu-id="b83dc-116">Registry Key Value</span></span></th>
<th align="left"><span data-ttu-id="b83dc-117">Deaktivierte Richtlinien Zustandsschlüssel und-Werte</span><span class="sxs-lookup"><span data-stu-id="b83dc-117">Disabled Policy State Keys and Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b83dc-118">PackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="b83dc-118">PackageInstallationRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-119">PACKAGEINSTALLATIONROOT</span><span class="sxs-lookup"><span data-stu-id="b83dc-119">PACKAGEINSTALLATIONROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-120">Gibt das Verzeichnis an, in dem alle neuen Anwendungen und Updates installiert werden.</span><span class="sxs-lookup"><span data-stu-id="b83dc-120">Specifies directory where all new applications and updates will be installed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-121">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b83dc-121">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-122">Streaming\PackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="b83dc-122">Streaming\PackageInstallationRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-123">Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-123">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b83dc-124">PackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="b83dc-124">PackageSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-125">PACKAGESOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="b83dc-125">PACKAGESOURCEROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-126">Überschreibt den Quellspeicherort zum Herunterladen von Paketinhalten.</span><span class="sxs-lookup"><span data-stu-id="b83dc-126">Overrides source location for downloading package content.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b83dc-127">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-128">Streaming\PackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="b83dc-128">Streaming\PackageSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-129">Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-129">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b83dc-130">AllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="b83dc-130">AllowHighCostLaunch</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-131">Ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-131">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-132">Mit dieser Einstellung wird gesteuert, ob virtualisierte Anwendungen auf Windows 8-Computern gestartet werden, die über eine getaktete Netzwerkverbindung verbunden sind (beispielsweise 4G).</span><span class="sxs-lookup"><span data-stu-id="b83dc-132">This setting controls whether virtualized applications are launched on Windows 8 machines connected via a metered network connection (For example, 4G).</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-133">True (aktiviert); Falsch (deaktivierter Zustand)</span><span class="sxs-lookup"><span data-stu-id="b83dc-133">True (enabled); False (Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-134">Streaming\AllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="b83dc-134">Streaming\AllowHighCostLaunch</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-135">0</span><span class="sxs-lookup"><span data-stu-id="b83dc-135">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b83dc-136">ReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="b83dc-136">ReestablishmentRetries</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-137">Ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-137">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-138">Gibt an, wie oft eine gelöschte Sitzung wiederholt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b83dc-138">Specifies the number of times to retry a dropped session.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-139">Ganzzahl (0-99)</span><span class="sxs-lookup"><span data-stu-id="b83dc-139">Integer (0-99)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-140">Streaming\ReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="b83dc-140">Streaming\ReestablishmentRetries</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-141">Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-141">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b83dc-142">ReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="b83dc-142">ReestablishmentInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-143">Ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-143">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-144">Gibt die Anzahl der Sekunden zwischen den versuchen, eine gelöschte Sitzung wiederherzustellen, an.</span><span class="sxs-lookup"><span data-stu-id="b83dc-144">Specifies the number of seconds between attempts to reestablish a dropped session.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-145">Ganzzahl (0-3600)</span><span class="sxs-lookup"><span data-stu-id="b83dc-145">Integer (0-3600)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-146">Streaming\ReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="b83dc-146">Streaming\ReestablishmentInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-147">Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-147">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b83dc-148">AutoLoad</span><span class="sxs-lookup"><span data-stu-id="b83dc-148">AutoLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-149">AUTOLOAD</span><span class="sxs-lookup"><span data-stu-id="b83dc-149">AUTOLOAD</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-150">Gibt an, wie neue Pakete automatisch von App-V auf einem bestimmten Computer geladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b83dc-150">Specifies how new packages should be loaded automatically by App-V on a specific computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-151">(0x0) keine; (0x1) zuvor verwendet; (0x2) alle</span><span class="sxs-lookup"><span data-stu-id="b83dc-151">(0x0) None; (0x1) Previously used; (0x2) All</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-152">Streaming\AutoLoad</span><span class="sxs-lookup"><span data-stu-id="b83dc-152">Streaming\AutoLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-153">Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-153">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b83dc-154">LocationProvider</span><span class="sxs-lookup"><span data-stu-id="b83dc-154">LocationProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-155">Ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-155">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-156">Gibt die CLSID für eine kompatible Implementierung der IAppvPackageLocationProvider-Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="b83dc-156">Specifies the CLSID for a compatible implementation of the IAppvPackageLocationProvider interface.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-157">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b83dc-157">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-158">Streaming\LocationProvider</span><span class="sxs-lookup"><span data-stu-id="b83dc-158">Streaming\LocationProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-159">Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-159">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b83dc-160">CertFilterForClientSsl</span><span class="sxs-lookup"><span data-stu-id="b83dc-160">CertFilterForClientSsl</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-161">Ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-161">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-162">Gibt den Pfad zu einem gültigen Zertifikat im Zertifikatspeicher an.</span><span class="sxs-lookup"><span data-stu-id="b83dc-162">Specifies the path to a valid certificate in the certificate store.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-163">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b83dc-163">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-164">Streaming\CertFilterForClientSsl</span><span class="sxs-lookup"><span data-stu-id="b83dc-164">Streaming\CertFilterForClientSsl</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-165">Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-165">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b83dc-166">VerifyCertificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="b83dc-166">VerifyCertificateRevocationList</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-167">Ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-167">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-168">Überprüft den Sperrungsstatus des Server Zertifikats vor dem dämpfen mithilfe von HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b83dc-168">Verifies Server certificate revocation status before steaming using HTTPS.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-169">True (aktiviert); Falsch (deaktivierter Zustand)</span><span class="sxs-lookup"><span data-stu-id="b83dc-169">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-170">Streaming\VerifyCertificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="b83dc-170">Streaming\VerifyCertificateRevocationList</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-171">0</span><span class="sxs-lookup"><span data-stu-id="b83dc-171">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b83dc-172">SharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="b83dc-172">SharedContentStoreMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-173">SHAREDCONTENTSTOREMODE</span><span class="sxs-lookup"><span data-stu-id="b83dc-173">SHAREDCONTENTSTOREMODE</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-174">Gibt an, dass Streaming-Paketinhalt nicht auf der lokalen Festplatte gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b83dc-174">Specifies that streamed package contents will be not be saved to the local hard disk.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-175">True (aktiviert); Falsch (deaktivierter Zustand)</span><span class="sxs-lookup"><span data-stu-id="b83dc-175">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-176">Streaming\SharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="b83dc-176">Streaming\SharedContentStoreMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-177">0</span><span class="sxs-lookup"><span data-stu-id="b83dc-177">0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b83dc-178">Name</span><span class="sxs-lookup"><span data-stu-id="b83dc-178">Name</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b83dc-179">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b83dc-179">Note</span></span></strong><br/><p><span data-ttu-id="b83dc-180">Diese Einstellung kann mit dem cmdLet "AppvclientConfiguration" nicht geändert werden <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="b83dc-180">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b83dc-181">Sie müssen das <strong> Cmdlet "Satz-AppvPublishingServer" verwenden </strong> .</span><span class="sxs-lookup"><span data-stu-id="b83dc-181">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b83dc-182">PUBLISHINGSERVERNAME</span><span class="sxs-lookup"><span data-stu-id="b83dc-182">PUBLISHINGSERVERNAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-183">Zeigt den Namen des Veröffentlichungsservers an.</span><span class="sxs-lookup"><span data-stu-id="b83dc-183">Displays the name of publishing server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-184">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b83dc-184">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-185">Publishing\Servers {Server-Nr} \ FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b83dc-185">Publishing\Servers{serverId}\FriendlyName</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-186">Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-186">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b83dc-187">URL</span><span class="sxs-lookup"><span data-stu-id="b83dc-187">URL</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b83dc-188">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b83dc-188">Note</span></span></strong><br/><p><span data-ttu-id="b83dc-189">Diese Einstellung kann mit dem cmdLet "AppvclientConfiguration" nicht geändert werden <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="b83dc-189">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b83dc-190">Sie müssen das <strong> Cmdlet "Satz-AppvPublishingServer" verwenden </strong> .</span><span class="sxs-lookup"><span data-stu-id="b83dc-190">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b83dc-191">PUBLISHINGSERVERURL</span><span class="sxs-lookup"><span data-stu-id="b83dc-191">PUBLISHINGSERVERURL</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-192">Zeigt die URL des Veröffentlichungsservers an.</span><span class="sxs-lookup"><span data-stu-id="b83dc-192">Displays the URL of publishing server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-193">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b83dc-193">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-194">Publishing\Servers {Server-Nr} \ URL</span><span class="sxs-lookup"><span data-stu-id="b83dc-194">Publishing\Servers{serverId}\URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-195">Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-195">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b83dc-196">GlobalRefreshEnabled</span><span class="sxs-lookup"><span data-stu-id="b83dc-196">GlobalRefreshEnabled</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b83dc-197">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b83dc-197">Note</span></span></strong><br/><p><span data-ttu-id="b83dc-198">Diese Einstellung kann mit dem cmdLet "AppvclientConfiguration" nicht geändert werden <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="b83dc-198">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b83dc-199">Sie müssen das <strong> Cmdlet "Satz-AppvPublishingServer" verwenden </strong> .</span><span class="sxs-lookup"><span data-stu-id="b83dc-199">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b83dc-200">GLOBALREFRESHENABLED</span><span class="sxs-lookup"><span data-stu-id="b83dc-200">GLOBALREFRESHENABLED</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-201">Aktivieren der globalen Veröffentlichungsaktualisierung (boolescher Wert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-201">Enables global publishing refresh (Boolean)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-202">True (aktiviert); Falsch (deaktivierter Zustand)</span><span class="sxs-lookup"><span data-stu-id="b83dc-202">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-203">Publishing\Servers {Server-Nr} \ GlobalEnabled</span><span class="sxs-lookup"><span data-stu-id="b83dc-203">Publishing\Servers{serverId}\GlobalEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-204">False</span><span class="sxs-lookup"><span data-stu-id="b83dc-204">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b83dc-205">GlobalRefreshOnLogon</span><span class="sxs-lookup"><span data-stu-id="b83dc-205">GlobalRefreshOnLogon</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b83dc-206">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b83dc-206">Note</span></span></strong><br/><p><span data-ttu-id="b83dc-207">Diese Einstellung kann mit dem cmdLet "AppvclientConfiguration" nicht geändert werden <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="b83dc-207">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b83dc-208">Sie müssen das <strong> Cmdlet "Satz-AppvPublishingServer" verwenden </strong> .</span><span class="sxs-lookup"><span data-stu-id="b83dc-208">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b83dc-209">GLOBALREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="b83dc-209">GLOBALREFRESHONLOGON</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-210">Löst eine Aktualisierung der globalen Veröffentlichung bei der Anmeldung aus.</span><span class="sxs-lookup"><span data-stu-id="b83dc-210">Triggers a global publishing refresh on logon.</span></span> <span data-ttu-id="b83dc-211">Boolean</span><span class="sxs-lookup"><span data-stu-id="b83dc-211">( Boolean)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-212">True (aktiviert); Falsch (deaktivierter Zustand)</span><span class="sxs-lookup"><span data-stu-id="b83dc-212">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-213">Publishing\Servers {Server-Nr} \ GlobalLogonRefresh</span><span class="sxs-lookup"><span data-stu-id="b83dc-213">Publishing\Servers{serverId}\GlobalLogonRefresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-214">False</span><span class="sxs-lookup"><span data-stu-id="b83dc-214">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b83dc-215">GlobalRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="b83dc-215">GlobalRefreshInterval</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b83dc-216">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b83dc-216">Note</span></span></strong><br/><p><span data-ttu-id="b83dc-217">Diese Einstellung kann mit dem cmdLet "AppvclientConfiguration" nicht geändert werden <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="b83dc-217">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b83dc-218">Sie müssen das <strong> Cmdlet "Satz-AppvPublishingServer" verwenden </strong> .</span><span class="sxs-lookup"><span data-stu-id="b83dc-218">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b83dc-219">GLOBALREFRESHINTERVAL</span><span class="sxs-lookup"><span data-stu-id="b83dc-219">GLOBALREFRESHINTERVAL</span></span>  </p></td>
<td align="left"><p><span data-ttu-id="b83dc-220">Gibt das Aktualisierungsintervall für die Veröffentlichung mithilfe von GlobalRefreshIntervalUnit an.</span><span class="sxs-lookup"><span data-stu-id="b83dc-220">Specifies the publishing refresh interval using the GlobalRefreshIntervalUnit.</span></span> <span data-ttu-id="b83dc-221">Um die Paketaktualisierung zu deaktivieren, wählen Sie 0 aus.</span><span class="sxs-lookup"><span data-stu-id="b83dc-221">To disable package refresh, select 0.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-222">Ganzzahl (0-744</span><span class="sxs-lookup"><span data-stu-id="b83dc-222">Integer (0-744</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-223">Publishing\Servers {Server-Nr} \ GlobalPeriodicRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="b83dc-223">Publishing\Servers{serverId}\GlobalPeriodicRefreshInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-224">0</span><span class="sxs-lookup"><span data-stu-id="b83dc-224">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b83dc-225">GlobalRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="b83dc-225">GlobalRefreshIntervalUnit</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b83dc-226">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b83dc-226">Note</span></span></strong><br/><p><span data-ttu-id="b83dc-227">Diese Einstellung kann mit dem cmdLet "AppvclientConfiguration" nicht geändert werden <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="b83dc-227">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b83dc-228">Sie müssen das <strong> Cmdlet "Satz-AppvPublishingServer" verwenden </strong> .</span><span class="sxs-lookup"><span data-stu-id="b83dc-228">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b83dc-229">GLOBALREFRESHINTERVALUNI</span><span class="sxs-lookup"><span data-stu-id="b83dc-229">GLOBALREFRESHINTERVALUNI</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-230">Gibt die Intervalleinheit an (Stunde 0-23; Tag 0-31).</span><span class="sxs-lookup"><span data-stu-id="b83dc-230">Specifies the interval unit (Hour 0-23, Day 0-31).</span></span> </p></td>
<td align="left"><p><span data-ttu-id="b83dc-231">0 für Stunde, 1 für Tag</span><span class="sxs-lookup"><span data-stu-id="b83dc-231">0 for hour, 1 for day</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-232">Publishing\Servers {Server-Nr} \ GlobalPeriodicRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="b83dc-232">Publishing\Servers{serverId}\GlobalPeriodicRefreshIntervalUnit</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-233">1</span><span class="sxs-lookup"><span data-stu-id="b83dc-233">1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b83dc-234">UserRefreshEnabled</span><span class="sxs-lookup"><span data-stu-id="b83dc-234">UserRefreshEnabled</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b83dc-235">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b83dc-235">Note</span></span></strong><br/><p><span data-ttu-id="b83dc-236">Diese Einstellung kann mit dem cmdLet "AppvclientConfiguration" nicht geändert werden <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="b83dc-236">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b83dc-237">Sie müssen das <strong> Cmdlet "Satz-AppvPublishingServer" verwenden </strong> .</span><span class="sxs-lookup"><span data-stu-id="b83dc-237">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b83dc-238">USERREFRESHENABLED</span><span class="sxs-lookup"><span data-stu-id="b83dc-238">USERREFRESHENABLED</span></span> </p></td>
<td align="left"><p><span data-ttu-id="b83dc-239">Aktiviert die Aktualisierung der Benutzer Veröffentlichung (boolescher Wert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-239">Enables user publishing refresh (Boolean)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-240">True (aktiviert); Falsch (deaktivierter Zustand)</span><span class="sxs-lookup"><span data-stu-id="b83dc-240">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-241">Publishing\Servers {Server-Nr} \ UserEnabled</span><span class="sxs-lookup"><span data-stu-id="b83dc-241">Publishing\Servers{serverId}\UserEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-242">False</span><span class="sxs-lookup"><span data-stu-id="b83dc-242">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b83dc-243">UserRefreshOnLogon</span><span class="sxs-lookup"><span data-stu-id="b83dc-243">UserRefreshOnLogon</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b83dc-244">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b83dc-244">Note</span></span></strong><br/><p><span data-ttu-id="b83dc-245">Diese Einstellung kann mit dem cmdLet "AppvclientConfiguration" nicht geändert werden <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="b83dc-245">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b83dc-246">Sie müssen das <strong> Cmdlet "Satz-AppvPublishingServer" verwenden </strong> .</span><span class="sxs-lookup"><span data-stu-id="b83dc-246">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b83dc-247">USERREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="b83dc-247">USERREFRESHONLOGON</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-248">Löst eine Benutzer Veröffentlichungsaktualisierung onlogon aus.</span><span class="sxs-lookup"><span data-stu-id="b83dc-248">Triggers a user publishing refresh onlogon.</span></span> <span data-ttu-id="b83dc-249">Boolean</span><span class="sxs-lookup"><span data-stu-id="b83dc-249">( Boolean)</span></span></p>
<p><span data-ttu-id="b83dc-250">Wortanzahl (mit Leerzeichen): 60</span><span class="sxs-lookup"><span data-stu-id="b83dc-250">Word count (with spaces): 60</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-251">True (aktiviert); Falsch (deaktivierter Zustand)</span><span class="sxs-lookup"><span data-stu-id="b83dc-251">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-252">Publishing\Servers {Server-Nr} \ UserLogonRefresh</span><span class="sxs-lookup"><span data-stu-id="b83dc-252">Publishing\Servers{serverId}\UserLogonRefresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-253">False</span><span class="sxs-lookup"><span data-stu-id="b83dc-253">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b83dc-254">UserRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="b83dc-254">UserRefreshInterval</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b83dc-255">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b83dc-255">Note</span></span></strong><br/><p><span data-ttu-id="b83dc-256">Diese Einstellung kann mit dem cmdLet "AppvclientConfiguration" nicht geändert werden <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="b83dc-256">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b83dc-257">Sie müssen das <strong> Cmdlet "Satz-AppvPublishingServer" verwenden </strong> .</span><span class="sxs-lookup"><span data-stu-id="b83dc-257">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b83dc-258">USERREFRESHINTERVAL</span><span class="sxs-lookup"><span data-stu-id="b83dc-258">USERREFRESHINTERVAL</span></span>     </p></td>
<td align="left"><p><span data-ttu-id="b83dc-259">Gibt das Aktualisierungsintervall für die Veröffentlichung mithilfe von UserRefreshIntervalUnit an.</span><span class="sxs-lookup"><span data-stu-id="b83dc-259">Specifies the publishing refresh interval using the UserRefreshIntervalUnit.</span></span> <span data-ttu-id="b83dc-260">Um die Paketaktualisierung zu deaktivieren, wählen Sie 0 aus.</span><span class="sxs-lookup"><span data-stu-id="b83dc-260">To disable package refresh, select 0.</span></span></p>
<p><span data-ttu-id="b83dc-261">Wortanzahl (mit Leerzeichen): 85</span><span class="sxs-lookup"><span data-stu-id="b83dc-261">Word count (with spaces): 85</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-262">Ganzzahl (0-744 Stunden)</span><span class="sxs-lookup"><span data-stu-id="b83dc-262">Integer (0-744 Hours)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-263">Publishing\Servers {Server-Nr} \ UserPeriodicRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="b83dc-263">Publishing\Servers{serverId}\UserPeriodicRefreshInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-264">0</span><span class="sxs-lookup"><span data-stu-id="b83dc-264">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b83dc-265">UserRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="b83dc-265">UserRefreshIntervalUnit</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b83dc-266">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b83dc-266">Note</span></span></strong><br/><p><span data-ttu-id="b83dc-267">Diese Einstellung kann mit dem cmdLet "AppvclientConfiguration" nicht geändert werden <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="b83dc-267">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b83dc-268">Sie müssen das <strong> Cmdlet "Satz-AppvPublishingServer" verwenden </strong> .</span><span class="sxs-lookup"><span data-stu-id="b83dc-268">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b83dc-269">USERREFRESHINTERVALUNIT</span><span class="sxs-lookup"><span data-stu-id="b83dc-269">USERREFRESHINTERVALUNIT</span></span>  </p></td>
<td align="left"><p><span data-ttu-id="b83dc-270">Gibt die Intervalleinheit an (Stunde 0-23; Tag 0-31).</span><span class="sxs-lookup"><span data-stu-id="b83dc-270">Specifies the interval unit (Hour 0-23, Day 0-31).</span></span> </p></td>
<td align="left"><p><span data-ttu-id="b83dc-271">0 für Stunde, 1 für Tag</span><span class="sxs-lookup"><span data-stu-id="b83dc-271">0 for hour, 1 for day</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-272">Publishing\Servers {Server-Nr} \ UserPeriodicRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="b83dc-272">Publishing\Servers{serverId}\UserPeriodicRefreshIntervalUnit</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-273">1</span><span class="sxs-lookup"><span data-stu-id="b83dc-273">1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b83dc-274">MigrationMode</span><span class="sxs-lookup"><span data-stu-id="b83dc-274">MigrationMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-275">MIGRATIONMODE</span><span class="sxs-lookup"><span data-stu-id="b83dc-275">MIGRATIONMODE</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-276">Der Migrationsmodus ermöglicht es dem App-v-Client, Tastenkombinationen und FTA für Pakete zu ändern, die mit einer früheren Version von App-v erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b83dc-276">Migration mode allows the App-V client to modify shortcuts and FTA’s for packages created using a previous version of App-V.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-277">True (aktivierter Zustand); Falsch (deaktivierter Zustand)</span><span class="sxs-lookup"><span data-stu-id="b83dc-277">True(enabled state); False (disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-278">Coexistence\MigrationMode</span><span class="sxs-lookup"><span data-stu-id="b83dc-278">Coexistence\MigrationMode</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b83dc-279">CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="b83dc-279">CEIPOPTIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-280">CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="b83dc-280">CEIPOPTIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-281">Ermöglicht es dem Computer, der den App-V 5,0-Client ausführt, bestimmte Nutzungsinformationen zu sammeln und zurückzugeben, damit wir die Anwendung weiter verbessern können.</span><span class="sxs-lookup"><span data-stu-id="b83dc-281">Allows the computer running the App-V 5.0 Client to collect and return certain usage information to help allow us to further improve the application.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-282">0 für disabled; 1 für aktiviert</span><span class="sxs-lookup"><span data-stu-id="b83dc-282">0 for disabled; 1 for enabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-283">Software/Microsoft/AppV/CEIP/CEIPEnable</span><span class="sxs-lookup"><span data-stu-id="b83dc-283">SOFTWARE/Microsoft/AppV/CEIP/CEIPEnable</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-284">0</span><span class="sxs-lookup"><span data-stu-id="b83dc-284">0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b83dc-285">EnablePackageScripts</span><span class="sxs-lookup"><span data-stu-id="b83dc-285">EnablePackageScripts</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-286">ENABLEPACKAGESCRIPTS</span><span class="sxs-lookup"><span data-stu-id="b83dc-286">ENABLEPACKAGESCRIPTS</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-287">Aktiviert Skripts, die im Paketmanifest der Konfigurationsdateien definiert sind, die ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b83dc-287">Enables scripts defined in the package manifest of configuration files that should run.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-288">True (aktiviert); Falsch (deaktivierter Zustand)</span><span class="sxs-lookup"><span data-stu-id="b83dc-288">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-289">\Scripting\EnablePackageScripts</span><span class="sxs-lookup"><span data-stu-id="b83dc-289">\Scripting\EnablePackageScripts</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b83dc-290">RoamingFileExclusions</span><span class="sxs-lookup"><span data-stu-id="b83dc-290">RoamingFileExclusions</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-291">ROAMINGFILEEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="b83dc-291">ROAMINGFILEEXCLUSIONS</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-292">Gibt die Dateipfade relativ zu% User Profile% an, die nicht mit einem Benutzer&#39;s-Profil Roaming durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="b83dc-292">Specifies the file paths relative to %userprofile% that do not roam with a user&#39;s profile.</span></span> <span data-ttu-id="b83dc-293">Beispiel Verwendung:/ROAMINGFILEEXCLUSIONS =&#39;Desktop; meine Bilder&#39;</span><span class="sxs-lookup"><span data-stu-id="b83dc-293">Example usage:  /ROAMINGFILEEXCLUSIONS=&#39;desktop;my pictures&#39;</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b83dc-294">RoamingRegistryExclusions</span><span class="sxs-lookup"><span data-stu-id="b83dc-294">RoamingRegistryExclusions</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-295">ROAMINGREGISTRYEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="b83dc-295">ROAMINGREGISTRYEXCLUSIONS</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-296">Gibt die Registrierungspfade an, die nicht mit einem Benutzerprofil durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="b83dc-296">Specifies the registry paths that do not roam with a user profile.</span></span> <span data-ttu-id="b83dc-297">Verwendungsbeispiel:/ROAMINGREGISTRYEXCLUSIONS = software\classes; Software\Clients</span><span class="sxs-lookup"><span data-stu-id="b83dc-297">Example usage: /ROAMINGREGISTRYEXCLUSIONS=software\classes;software\clients</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-298">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b83dc-298">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-299">Integration\RoamingRegistryExclusions</span><span class="sxs-lookup"><span data-stu-id="b83dc-299">Integration\RoamingRegistryExclusions</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-300">Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-300">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b83dc-301">IntegrationRootUser</span><span class="sxs-lookup"><span data-stu-id="b83dc-301">IntegrationRootUser</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-302">Ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-302">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-303">Gibt den Ort an, an dem symbolische Links erstellt werden, die der aktuellen Version eines pro Benutzer veröffentlichten Pakets zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b83dc-303">Specifies the location to create symbolic links associated with the current version of a per-user published package.</span></span> <span data-ttu-id="b83dc-304">alle virtuellen Anwendungserweiterungen, beispielsweise Verknüpfungen und Dateitypzuordnungen, verweisen auf diesen Pfad.</span><span class="sxs-lookup"><span data-stu-id="b83dc-304">all virtual application extensions, for example shortcuts and file type associations, will point to this path.</span></span> <span data-ttu-id="b83dc-305">Wenn Sie keinen Pfad angeben, werden beim Veröffentlichen des Pakets symbolische Links nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b83dc-305">If you do not specify a path, symbolic links will not be used when you publish the package.</span></span> <span data-ttu-id="b83dc-306">Beispiel:%localappdata%\Microsoft\AppV\Client\Integration.</span><span class="sxs-lookup"><span data-stu-id="b83dc-306">For example: %localappdata%\Microsoft\AppV\Client\Integration.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-307">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b83dc-307">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-308">Integration\IntegrationRootUser</span><span class="sxs-lookup"><span data-stu-id="b83dc-308">Integration\IntegrationRootUser</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-309">Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-309">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b83dc-310">IntegrationRootGlobal</span><span class="sxs-lookup"><span data-stu-id="b83dc-310">IntegrationRootGlobal</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-311">Ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-311">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-312">Gibt den Ort an, an dem symbolische Links erstellt werden, die der aktuellen Version eines Global veröffentlichten Pakets zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b83dc-312">Specifies the location to create symbolic links associated with the current version of a globally published package.</span></span> <span data-ttu-id="b83dc-313">alle virtuellen Anwendungserweiterungen, beispielsweise Verknüpfungen und Dateitypzuordnungen, verweisen auf diesen Pfad.</span><span class="sxs-lookup"><span data-stu-id="b83dc-313">all virtual application extensions, for example shortcuts and file type associations, will point to this path.</span></span> <span data-ttu-id="b83dc-314">Wenn Sie keinen Pfad angeben, werden beim Veröffentlichen des Pakets symbolische Links nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b83dc-314">If you do not specify a path, symbolic links will not be used when you publish the package.</span></span> <span data-ttu-id="b83dc-315">Beispiel:%ALLUSERSPROFILE%\Microsoft\AppV\Client\Integration</span><span class="sxs-lookup"><span data-stu-id="b83dc-315">For example: %allusersprofile%\Microsoft\AppV\Client\Integration</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-316">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b83dc-316">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-317">Integration\IntegrationRootGlobal</span><span class="sxs-lookup"><span data-stu-id="b83dc-317">Integration\IntegrationRootGlobal</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-318">Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-318">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b83dc-319">VirtualizableExtensions</span><span class="sxs-lookup"><span data-stu-id="b83dc-319">VirtualizableExtensions</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-320">Ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-320">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-321">Eine durch trennzeichengetrennte Liste mit Dateinamenerweiterungen, die verwendet werden kann, um zu ermitteln, ob eine lokal installierte Anwendung in der virtuellen Umgebung ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b83dc-321">A comma -delineated list of file name extensions that can be used to determine if a locally installed application can be run in the virtual environment.</span></span></p>
<p><span data-ttu-id="b83dc-322">Wenn während der Veröffentlichung Verknüpfungen, FTA und andere Erweiterungspunkte erstellt werden, vergleicht App-V die Dateinamenerweiterung mit der Liste, wenn die Anwendung, die dem Erweiterungspunkt zugeordnet ist, lokal installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b83dc-322">When shortcuts, FTAs, and other extension points are created during publishing, App-V will compare the file name extension to the list if the application that is associated with the extension point is locally installed.</span></span> <span data-ttu-id="b83dc-323">Wenn sich die Erweiterung befindet, <strong> wird der RunVirtual- </strong> Befehlszeilenparameter hinzugefügt, und die Anwendung wird praktisch ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b83dc-323">If the extension is located, the <strong>RunVirtual</strong> command line parameter will be added, and the application will run virtually.</span></span></p>
<p><span data-ttu-id="b83dc-324">Weitere Informationen zum <strong> RunVirtual </strong> -Parameter finden Sie unter <a href="running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md" data-raw-source="[Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)"> Ausführen einer lokal installierten Anwendung in einer virtuellen Umgebung mit virtualisierten Anwendungen </a> .</span><span class="sxs-lookup"><span data-stu-id="b83dc-324">For more information about the <strong>RunVirtual</strong> parameter, see <a href="running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md" data-raw-source="[Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)">Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications</a>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-325">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b83dc-325">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-326">Integration\VirtualizableExtensions</span><span class="sxs-lookup"><span data-stu-id="b83dc-326">Integration\VirtualizableExtensions</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-327">Richtlinienwert nicht geschrieben</span><span class="sxs-lookup"><span data-stu-id="b83dc-327">Policy value not written</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b83dc-328">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="b83dc-328">ReportingEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-329">Ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-329">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-330">Ermöglicht es dem Client, Informationen an einen Berichtsserver zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="b83dc-330">Enables the client to return information to a reporting server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-331">True (aktiviert); Falsch (deaktivierter Zustand)</span><span class="sxs-lookup"><span data-stu-id="b83dc-331">True (enabled); False (Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-332">Reporting\EnableReporting</span><span class="sxs-lookup"><span data-stu-id="b83dc-332">Reporting\EnableReporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-333">False</span><span class="sxs-lookup"><span data-stu-id="b83dc-333">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b83dc-334">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="b83dc-334">ReportingServerURL</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-335">Ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-335">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-336">Gibt den Speicherort auf dem Berichtsserver an, auf dem Clientinformationen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b83dc-336">Specifies the location on the reporting server where client information is saved.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-337">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b83dc-337">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-338">Reporting\ReportingServer</span><span class="sxs-lookup"><span data-stu-id="b83dc-338">Reporting\ReportingServer</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-339">Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-339">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b83dc-340">ReportingDataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="b83dc-340">ReportingDataCacheLimit</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-341">Ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-341">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-342">Gibt die maximale Größe in Megabyte (MB) des XML-Caches zum Speichern von Berichtsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="b83dc-342">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="b83dc-343">Die Größe bezieht sich auf den Cache im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="b83dc-343">The size applies to the cache in memory.</span></span> <span data-ttu-id="b83dc-344">Wenn das Limit erreicht ist, wird die Protokolldatei überschrieben.</span><span class="sxs-lookup"><span data-stu-id="b83dc-344">When the limit is reached, the log file will roll over.</span></span> <span data-ttu-id="b83dc-345">Zwischen 0 und 1024.</span><span class="sxs-lookup"><span data-stu-id="b83dc-345">Set between 0 and 1024.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-346">Ganzzahl [0-1024]</span><span class="sxs-lookup"><span data-stu-id="b83dc-346">Integer [0-1024]</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-347">Reporting\DataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="b83dc-347">Reporting\DataCacheLimit</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-348">Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-348">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b83dc-349">ReportingDataBlockSize</span><span class="sxs-lookup"><span data-stu-id="b83dc-349">ReportingDataBlockSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-350">Ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-350">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-351">Gibt die maximale Größe in Bytes an, die an den Server gesendet werden soll, um Upload-Anforderungen zu melden.</span><span class="sxs-lookup"><span data-stu-id="b83dc-351">Specifies the maximum size in bytes to transmit to the server for reporting upload requests.</span></span> <span data-ttu-id="b83dc-352">Dies kann dazu beitragen, dauerhafte Übertragungsfehler zu vermeiden, wenn das Protokoll eine signifikante Größe erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="b83dc-352">This can help avoid permanent transmission failures when the log has reached a significant size.</span></span> <span data-ttu-id="b83dc-353">Zwischen 1024 und unbegrenzt eingestellt.</span><span class="sxs-lookup"><span data-stu-id="b83dc-353">Set between 1024 and unlimited.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-354">Ganzzahl [1024-unbegrenzt]</span><span class="sxs-lookup"><span data-stu-id="b83dc-354">Integer [1024 - Unlimited]</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-355">Reporting\DataBlockSize</span><span class="sxs-lookup"><span data-stu-id="b83dc-355">Reporting\DataBlockSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-356">Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-356">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b83dc-357">ReportingStartTime</span><span class="sxs-lookup"><span data-stu-id="b83dc-357">ReportingStartTime</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-358">Ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-358">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-359">Gibt den Zeitpunkt an, zu dem der Client initiiert werden soll, um Daten an den Berichtsserver zu senden.</span><span class="sxs-lookup"><span data-stu-id="b83dc-359">Specifies the time to initiate the client to send data to the reporting server.</span></span> <span data-ttu-id="b83dc-360">Sie müssen eine gültige Ganzzahl zwischen 0-23 angeben, die der Stunde des Tages entspricht.</span><span class="sxs-lookup"><span data-stu-id="b83dc-360">You must specify a valid integer between 0-23 corresponding to the hour of the day.</span></span> <span data-ttu-id="b83dc-361">Standardmäßig <strong> wird der ReportingStartTime am </strong> aktuellen Tag um 10 P. M oder 22 gestartet.</span><span class="sxs-lookup"><span data-stu-id="b83dc-361">By default the <strong>ReportingStartTime</strong> will start on the current day at 10 P.M.or 22.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b83dc-362">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b83dc-362">Note</span></span></strong><br/><p><span data-ttu-id="b83dc-363">Sie sollten diese Einstellung auf einen Zeitpunkt konfigurieren, zu dem Computer, auf denen der App-V 5,0-Client ausgeführt wird, am ehesten offline sind.</span><span class="sxs-lookup"><span data-stu-id="b83dc-363">You should configure this setting to a time when computers running the App-V 5.0 client are least likely to be offline.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b83dc-364">Ganzzahl (0 – 23)</span><span class="sxs-lookup"><span data-stu-id="b83dc-364">Integer (0 – 23)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-365">Berichterstellung \ Startzeit</span><span class="sxs-lookup"><span data-stu-id="b83dc-365">Reporting\ StartTime</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-366">Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-366">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b83dc-367">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="b83dc-367">ReportingInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-368">Ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-368">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-369">Gibt das Wiederholungsintervall an, das vom Client zum erneuten Senden von Daten an den Berichtsserver verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b83dc-369">Specifies the retry interval that the client will use to resend data to the reporting server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-370">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="b83dc-370">Integer</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-371">Reporting\RetryInterval</span><span class="sxs-lookup"><span data-stu-id="b83dc-371">Reporting\RetryInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-372">Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-372">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b83dc-373">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="b83dc-373">ReportingRandomDelay</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-374">Ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-374">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-375">Gibt die maximale Verzögerung (in Minuten) für Daten an, die an den Berichtsserver gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b83dc-375">Specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="b83dc-376">Wenn der geplante Task gestartet wird, generiert der Client eine zufällige Verzögerung zwischen 0 und <strong> ReportingRandomDelay </strong> und wartet die angegebene Dauer vor dem Senden von Daten.</span><span class="sxs-lookup"><span data-stu-id="b83dc-376">When the scheduled task is started, the client generates a random delay between 0 and <strong>ReportingRandomDelay</strong> and will wait the specified duration before sending data.</span></span> <span data-ttu-id="b83dc-377">Dies kann dazu beitragen, Kollisionen auf dem Server zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="b83dc-377">This can help to prevent collisions on the server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-378">Ganzzahl [0-ReportingRandomDelay]</span><span class="sxs-lookup"><span data-stu-id="b83dc-378">Integer [0 - ReportingRandomDelay]</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-379">Reporting\RandomDelay</span><span class="sxs-lookup"><span data-stu-id="b83dc-379">Reporting\RandomDelay</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-380">Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-380">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b83dc-381">EnableDynamicVirtualization</span><span class="sxs-lookup"><span data-stu-id="b83dc-381">EnableDynamicVirtualization</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b83dc-382">Wichtig</span><span class="sxs-lookup"><span data-stu-id="b83dc-382">Important</span></span></strong><br/><p><span data-ttu-id="b83dc-383">Diese Einstellung ist nur mit App-V 5,0 SP2 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-383">This setting is available only with App-V 5.0 SP2 or later.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b83dc-384">Ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-384">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-385">Ermöglicht unterstützte Shell-Erweiterungen, Browser-helferobjekte und ActiveX-Steuerelemente, die virtualisiert und mit virtuellen Anwendungen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="b83dc-385">Enables supported Shell Extensions, Browser Helper Objects, and Active X controls to be virtualized and run with virtual applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-386">1 (aktiviert), 0 (deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-386">1 (Enabled), 0 (Disabled)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-387">HKEY_LOCAL_MACHINE \software\microsoft\appv\client\virtualization</span><span class="sxs-lookup"><span data-stu-id="b83dc-387">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\Virtualization</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b83dc-388">EnablePublishingRefreshUI</span><span class="sxs-lookup"><span data-stu-id="b83dc-388">EnablePublishingRefreshUI</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b83dc-389">Wichtig</span><span class="sxs-lookup"><span data-stu-id="b83dc-389">Important</span></span></strong><br/><p><span data-ttu-id="b83dc-390">Diese Einstellung ist nur mit App-V 5,0 SP2 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-390">This setting is available only with App-V 5.0 SP2.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b83dc-391">Ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-391">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-392">Aktiviert die Statusleiste für die Veröffentlichungsaktualisierung für den Computer, auf dem der App-V 5,0-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b83dc-392">Enables the publishing refresh progress bar for the computer running the App-V 5.0 Client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-393">1 (aktiviert), 0 (deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-393">1 (Enabled), 0 (Disabled)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-394">HKEY_LOCAL_MACHINE \software\microsoft\appv\client\publishing</span><span class="sxs-lookup"><span data-stu-id="b83dc-394">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\Publishing</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b83dc-395">HideUI</span><span class="sxs-lookup"><span data-stu-id="b83dc-395">HideUI</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b83dc-396">Wichtig</span><span class="sxs-lookup"><span data-stu-id="b83dc-396">Important</span></span></strong><br/><p><span data-ttu-id="b83dc-397">Diese Einstellung ist nur mit App-V 5,0 SP2 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-397">This setting is available only with App-V 5.0 SP2.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b83dc-398">Ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-398">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-399">Blendet die Statusleiste der Veröffentlichungsaktualisierung aus.</span><span class="sxs-lookup"><span data-stu-id="b83dc-399">Hides the publishing refresh progress bar.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-400">1 (aktiviert), 0 (deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="b83dc-400">1 (Enabled), 0 (Disabled)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b83dc-401">ProcessesUsingVirtualComponents</span><span class="sxs-lookup"><span data-stu-id="b83dc-401">ProcessesUsingVirtualComponents</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-402">Ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b83dc-402">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-403">Gibt eine Liste von Prozess Pfaden an (die möglicherweise Platzhalter enthalten), die Kandidaten für die Verwendung der dynamischen Virtualisierung sind (unterstützte Shell-Erweiterungen, Browser-helferobjekte und ActiveX-Steuerelemente).</span><span class="sxs-lookup"><span data-stu-id="b83dc-403">Specifies a list of process paths (that may contain wildcards), which are candidates for using dynamic virtualization (supported shell extensions, browser helper objects, and ActiveX controls).</span></span> <span data-ttu-id="b83dc-404">Nur Prozesse, deren vollständiger Pfad einem dieser Elemente entspricht, können Dynamic Virtualization verwenden.</span><span class="sxs-lookup"><span data-stu-id="b83dc-404">Only processes whose full path matches one of these items can use dynamic virtualization.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-405">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b83dc-405">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-406">Virtualization\ProcessesUsingVirtualComponents</span><span class="sxs-lookup"><span data-stu-id="b83dc-406">Virtualization\ProcessesUsingVirtualComponents</span></span></p></td>
<td align="left"><p><span data-ttu-id="b83dc-407">Leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b83dc-407">Empty string.</span></span></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="b83dc-408">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b83dc-408">Related topics</span></span>


[<span data-ttu-id="b83dc-409">Bereitstellen von App-V 5.0-Sequencer und -Client</span><span class="sxs-lookup"><span data-stu-id="b83dc-409">Deploying the App-V 5.0 Sequencer and Client</span></span>](deploying-the-app-v-50-sequencer-and-client.md)

[<span data-ttu-id="b83dc-410">So ändern Sie die App-V 5.0-Clientkonfiguration mithilfe der ADMX-Vorlage und -Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="b83dc-410">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span>](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)

[<span data-ttu-id="b83dc-411">So stellen Sie App-V-Client bereit</span><span class="sxs-lookup"><span data-stu-id="b83dc-411">How to Deploy the App-V Client</span></span>](how-to-deploy-the-app-v-client-gb18030.md)









