---
title: Neuigkeiten in AGPM 4.0 SP2
description: Neuigkeiten in AGPM 4.0 SP2
author: dansimp
ms.assetid: 5c0dcab4-f27d-4153-8b8e-b280b080be51
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 56369207780cf0795f16eda91f249a26270c4b47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807391"
---
# <span data-ttu-id="8e915-103">Neuigkeiten in AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="8e915-103">What's New in AGPM 4.0 SP2</span></span>


<span data-ttu-id="8e915-104">Dieser Inhalt beschreibt Verbesserungen und unterstützte Konfigurationen für Microsoft Advanced Group Policy Management (AGPM) 4.0 Service Pack2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="8e915-104">This content describes enhancements and supported configurations for Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack2 (SP2).</span></span> <span data-ttu-id="8e915-105">Wenn es einen Unterschied zwischen diesem Inhalt und anderer AGPM-Dokumentation gibt, sollten Sie diesen Inhalt als autorisierend ansehen und davon ausgehen, dass er die andere Dokumentation ersetzt.</span><span class="sxs-lookup"><span data-stu-id="8e915-105">If there is a difference between this content and other AGPM documentation, consider this content authoritative and assume that it supersedes the other documentation.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="8e915-106">Neuigkeiten </span><span class="sxs-lookup"><span data-stu-id="8e915-106">What’s new</span></span>


<span data-ttu-id="8e915-107">AGPM 4.0 SP2 unterstützt die folgenden Features und Funktionen.</span><span class="sxs-lookup"><span data-stu-id="8e915-107">AGPM4.0 SP2 supports the following features and functionality.</span></span>

### <span data-ttu-id="8e915-108">Unterstützung für Windows 8.1 und Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="8e915-108">Support for Windows8.1 and Windows Server2012 R2</span></span>

<span data-ttu-id="8e915-109">AGPM 4.0 SP2 bietet Unterstützung für die Windows 8.1-und Windows Server2012 R2-Betriebssysteme.</span><span class="sxs-lookup"><span data-stu-id="8e915-109">AGPM4.0 SP2 adds support for the Windows8.1 and Windows Server2012 R2 operating systems.</span></span>

### <span data-ttu-id="8e915-110">Neue und geänderte clientseitige Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="8e915-110">New and changed client-side extensions</span></span>

<span data-ttu-id="8e915-111">Clientseitige Gruppenrichtlinienerweiterungen wurden hinzugefügt oder geändert, damit AGPM neue Richtlinieneinstellungen in Windows 8.1 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8e915-111">Group Policy client-side extensions have been added or changed for AGPM to support new policy settings in Windows8.1.</span></span> <span data-ttu-id="8e915-112">Mithilfe dieser Richtlinieneinstellungen können Gruppenrichtlinienadministratoren Windows 8.1-spezifische Richtlinieneinstellungen verwalten und nachvollziehen, die zwischen zwei Gruppenrichtlinienobjekten (Group Policy Objects, GPOs) oder Vorlagen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="8e915-112">These policy settings enable Group Policy administrators to manage and track Windows8.1–specific policy settings that change between two Group Policy Objects (GPOs) or templates.</span></span> <span data-ttu-id="8e915-113">Verwenden Sie zum Anzeigen der clientseitigen Erweiterungen die im AGPM-Client verfügbaren Einstellungen und Differenz Berichte.</span><span class="sxs-lookup"><span data-stu-id="8e915-113">To view your client-side extensions, use the settings and difference reports that are available in the AGPM Client.</span></span>

<span data-ttu-id="8e915-114">Die neuen und geänderten Gruppenrichtlinien-clientseitigen Erweiterungen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8e915-114">The new and changed Group Policy client-side extensions are:</span></span>

-   <span data-ttu-id="8e915-115">**Geben Sie die Einstellungen für Arbeitsordner an**.</span><span class="sxs-lookup"><span data-stu-id="8e915-115">**Specify Work Folders settings**.</span></span> <span data-ttu-id="8e915-116">Wenn Sie diese Richtlinieneinstellung aktivieren, können IT-Administratoren Arbeitsordner so konfigurieren, dass Sie automatisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8e915-116">If you enable this policy setting, IT administrators can configure Work Folders to be created automatically.</span></span> <span data-ttu-id="8e915-117">Das Feature "Arbeitsordner" ermöglicht es Endbenutzern, Dateien von Ihren Windows-Desktopgeräten mit ihren anderen Geräten zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="8e915-117">The Work Folders feature enables end users to synchronize files from their Windows desktop devices to their other devices.</span></span> <span data-ttu-id="8e915-118">Verwenden Sie diese Richtlinieneinstellung, um die Synchronisierungsbeziehung auf den Geräten eines Endbenutzers zu erstellen und zu konfigurieren, wie der Dateiserver identifiziert wird, in dem die Arbeitsordner des Benutzers gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="8e915-118">Use this policy setting to create the synchronization relationship on an end user’s devices and to configure how to identify the file server that stores the user’s Work Folders.</span></span> <span data-ttu-id="8e915-119">Wenn Sie das Kontrollkästchen **Synchronisierung automatisch bereit** stellen aktivieren, wird die Synchronisierungspartnerschaft ohne Benutzereingabe erstellt, und die Daten werden automatisch mit dem Gerät des Benutzers synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="8e915-119">If you select the **Auto provision synchronization** check box, the synchronization partnership will be created without user input, and data will automatically start synchronizing to the user’s device.</span></span> <span data-ttu-id="8e915-120">Wenn Sie das Kontrollkästchen **Synchronisierung automatisch bereit** stellen nicht aktivieren, müssen die Benutzereingaben angeben, um die Synchronisierung zu starten.</span><span class="sxs-lookup"><span data-stu-id="8e915-120">If you do not select the **Auto provision synchronization** check box, users must provide input to start the synchronization.</span></span>

-   <span data-ttu-id="8e915-121">**Erzwingen der automatischen Einrichtung für alle Benutzer**</span><span class="sxs-lookup"><span data-stu-id="8e915-121">**Force automatic setup for all users**.</span></span> <span data-ttu-id="8e915-122">Wenn Sie diese Richtlinieneinstellung aktivieren, können IT-Administratoren ermitteln, ob die Arbeitsordner Partnerschaft automatisch auf Endbenutzergeräten ohne Eingabe von Endbenutzern erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e915-122">If you enable this policy setting, IT administrators can determine whether to create the Work Folders partnership automatically on end-user devices without input from end users.</span></span> <span data-ttu-id="8e915-123">Wenn Sie diese Richtlinieneinstellung aktivieren, wird die Synchronisierung so eingerichtet, wie Sie die Richtlinieneinstellung " **Arbeitsordner angeben** " konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8e915-123">If you enable this policy setting, the synchronization will be set up according to how you configure the **Specify Work Folders settings** policy setting.</span></span> <span data-ttu-id="8e915-124">Wenn Sie die Richtlinieneinstellung " **automatische Einrichtung für alle Benutzer erzwingen** " auf " **deaktiviert** " oder " **nicht konfiguriert**" festlegen, wird die Partnerschaft "Arbeitsordner" entsprechend der Festlegung der Option für die **automatische Bereitstellung** in der Richtlinieneinstellung für die **Einstellungen für Arbeitsordner** festlegen konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="8e915-124">If you set the **Force automatic setup for all users** policy setting to **Disabled** or **Not configured**, the Work Folders partnership will be configured according to how you set the **Automatic Provisioning** option in the **Specify Work Folders settings** policy setting.</span></span>

<span data-ttu-id="8e915-125">Weitere Informationen zum Feature "Arbeitsordner" finden Sie unter [Übersicht über Arbeitsordner](https://go.microsoft.com/fwlink/?LinkId=330444).</span><span class="sxs-lookup"><span data-stu-id="8e915-125">For more information about the Work Folders feature, see [Work Folders Overview](https://go.microsoft.com/fwlink/?LinkId=330444).</span></span>

### <span data-ttu-id="8e915-126">Kundenfeedback und Hotfix-Rollup</span><span class="sxs-lookup"><span data-stu-id="8e915-126">Customer feedback and hotfix rollup</span></span>

<span data-ttu-id="8e915-127">AGPM 4.0 SP2 enthält ein Rollup von Hotfixes, um Probleme zu beheben, die seit der Version AGPM 4.0 Service Pack1 (SP1) gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="8e915-127">AGPM4.0 SP2 includes a rollup of hotfixes to address issues found since the AGPM4.0 Service Pack1 (SP1) release.</span></span> <span data-ttu-id="8e915-128">AGPM 4.0 SP2 enthält die neuesten Fixes bis einschließlich Microsoft Advanced Group Policy Management 4.0 SP1-Hotfix1.</span><span class="sxs-lookup"><span data-stu-id="8e915-128">AGPM4.0 SP2 contains the latest fixes up to and including Microsoft Advanced Group Policy Management4.0 SP1 Hotfix1.</span></span> <span data-ttu-id="8e915-129">Weitere Informationen finden Sie im Knowledge Base-Artikel [2873472](https://go.microsoft.com/fwlink/?LinkId=325400)).</span><span class="sxs-lookup"><span data-stu-id="8e915-129">For more information, see Knowledge Base article [2873472](https://go.microsoft.com/fwlink/?LinkId=325400)).</span></span>

### <span data-ttu-id="8e915-130">Neue Gruppenrichtlinienerweiterungen in Einstellungen und Unterschiedsberichten</span><span class="sxs-lookup"><span data-stu-id="8e915-130">New Group Policy extensions in settings and difference reports</span></span>

<span data-ttu-id="8e915-131">Die neuen Gruppenrichtlinienerweiterungen wurden zu den Einstellungen und Unterschiedsberichten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8e915-131">The new Group Policy extensions have been added to the settings and difference reports.</span></span>

### <span data-ttu-id="8e915-132">Änderungen und Support für das Installationsprogramm</span><span class="sxs-lookup"><span data-stu-id="8e915-132">Installer changes and support</span></span>

<span data-ttu-id="8e915-133">Die Änderungen und Unterstützung für das AGPM 4.0 SP2-Installationsprogramm sind:</span><span class="sxs-lookup"><span data-stu-id="8e915-133">The changes and support for the AGPM4.0 SP2 installer are:</span></span>

-   <span data-ttu-id="8e915-134">Wenn Sie AGPM 4.0 SP2 unter dem BetriebssystemWindows 8 oder Windows Server 2012 oder höher installieren, überprüft das AGPM-Installationsprogramm, ob die erforderliche erforderliche Software (die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) und Microsoft .NET Framework 3.5) installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8e915-134">If you install AGPM4.0 SP2 on the Windows 8 or Windows Server 2012 operating system or later operating systems, the AGPM installer verifies that the required prerequisite software (the Group Policy Management Console (GPMC) and the Microsoft .NET Framework3.5) is installed.</span></span> <span data-ttu-id="8e915-135">Wenn diese erforderliche Software nicht installiert ist, ist die Installation von AGPM 4.0 SP2 blockiert.</span><span class="sxs-lookup"><span data-stu-id="8e915-135">If this prerequisite software is not installed, the AGPM4.0 SP2 installation is blocked.</span></span>

-   <span data-ttu-id="8e915-136">Wenn Sie den AGPM-Server installieren, werden die WCF-Aktivierung, die nicht-HTTP-Aktivierung und der Windows-Prozessaktivierungsdienst automatisch aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8e915-136">When you install the AGPM Server, WCF Activation, Non-HTTP Activation, and Windows Process Activation Service are automatically enabled.</span></span>

-   <span data-ttu-id="8e915-137">Laden Sie auf dem Windows Vista-Clientbetriebssystem und neueren Betriebssystemen die entsprechende Version der Remote System-Verwaltungs Tools für Ihr Betriebssystem herunter, bevor Sie AGPM 4.0 SP2 installieren.</span><span class="sxs-lookup"><span data-stu-id="8e915-137">On the WindowsVista client operating system and later operating systems, download the appropriate version of the Remote System Administration Tools for your operating system before you install AGPM4.0 SP2.</span></span>

-   <span data-ttu-id="8e915-138">AGPM 4.0 SP2 unterstützt die Abwärtskompatibilität mit älteren unterstützten Betriebssystemen.</span><span class="sxs-lookup"><span data-stu-id="8e915-138">AGPM4.0 SP2 supports backward compatibility with older supported operating systems.</span></span>

### <span data-ttu-id="8e915-139">Möglichkeit zum Upgrade auf AGPM 4.0 SP2 ohne erneutes Eingeben von Konfigurationsparametern</span><span class="sxs-lookup"><span data-stu-id="8e915-139">Ability to upgrade to AGPM4.0 SP2 without reentering configuration parameters</span></span>

<span data-ttu-id="8e915-140">Sie können den AGPM-Client oder AGPM-Server auf AGPM 4.0 SP2 aktualisieren, ohne dazu aufgefordert zu werden, die Konfigurationsparameter (so genannte Smart Upgrade) nur von AGPM 4.0 weiter einzugeben, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8e915-140">You can upgrade the AGPM Client or AGPM Server to AGPM4.0 SP2 without being prompted to reenter configuration parameters (called the Smart Upgrade) only from AGPM4.0 onward, as shown in the following table.</span></span> <span data-ttu-id="8e915-141">Wenn Sie von anderen Versionen von AGPM auf AGPM 4.0 SP2 aktualisieren, wie in der Tabelle gezeigt, müssen Sie das klassische Upgrade verwenden, das eine erneute Eingabe der Konfigurationsparameter erfordert.</span><span class="sxs-lookup"><span data-stu-id="8e915-141">If you are upgrading to AGPM4.0 SP2 from other versions of AGPM, as shown in the table, you must use the Classic Upgrade, which requires you to reenter the configuration parameters.</span></span> <span data-ttu-id="8e915-142">Da jede Version von AGPM einem bestimmten Betriebssystem zugeordnet ist, lesen Sie [Auswählen der zu installierenden AGPM-Version](https://go.microsoft.com/fwlink/?LinkId=254350) , und stellen Sie sicher, dass Sie das Betriebssystem entsprechend aktualisieren, bevor Sie AGPM aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="8e915-142">Because each version of AGPM is associated with a particular operating system, see [Choosing Which Version of AGPM to Install](https://go.microsoft.com/fwlink/?LinkId=254350) and make sure that you upgrade your operating system as appropriate before you upgrade AGPM.</span></span>

**<span data-ttu-id="8e915-143">Unterstützte Upgrades für AGPM 4,0 SP2</span><span class="sxs-lookup"><span data-stu-id="8e915-143">AGPM 4.0 SP2 supported upgrades</span></span>**

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8e915-144">AGPM-Version, auf der Sie ein Upgrade durchführen können</span><span class="sxs-lookup"><span data-stu-id="8e915-144">AGPM version from which you can upgrade</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="8e915-145">2,5</span><span class="sxs-lookup"><span data-stu-id="8e915-145">2.5</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="8e915-146">3.0</span><span class="sxs-lookup"><span data-stu-id="8e915-146">3.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="8e915-147">4.0</span><span class="sxs-lookup"><span data-stu-id="8e915-147">4.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="8e915-148">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="8e915-148">4.0 SP1</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="8e915-149">4,0 SP2</span><span class="sxs-lookup"><span data-stu-id="8e915-149">4.0 SP2</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8e915-150">2,5</span><span class="sxs-lookup"><span data-stu-id="8e915-150">2.5</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-151">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8e915-151">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-152">Klassisches Upgrade</span><span class="sxs-lookup"><span data-stu-id="8e915-152">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-153">Klassisches Upgrade</span><span class="sxs-lookup"><span data-stu-id="8e915-153">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-154">Die Installation ist blockiert</span><span class="sxs-lookup"><span data-stu-id="8e915-154">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-155">Die Installation ist blockiert</span><span class="sxs-lookup"><span data-stu-id="8e915-155">Installation is blocked</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8e915-156">3.0</span><span class="sxs-lookup"><span data-stu-id="8e915-156">3.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-157">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8e915-157">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-158">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8e915-158">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-159">Klassisches Upgrade</span><span class="sxs-lookup"><span data-stu-id="8e915-159">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-160">Die Installation ist blockiert</span><span class="sxs-lookup"><span data-stu-id="8e915-160">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-161">Die Installation ist blockiert</span><span class="sxs-lookup"><span data-stu-id="8e915-161">Installation is blocked</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8e915-162">4.0</span><span class="sxs-lookup"><span data-stu-id="8e915-162">4.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-163">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8e915-163">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-164">Nicht anwendbar</span><span class="sxs-lookup"><span data-stu-id="8e915-164">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-165">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8e915-165">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-166">Intelligentes Upgrade</span><span class="sxs-lookup"><span data-stu-id="8e915-166">Smart Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-167">Intelligentes Upgrade</span><span class="sxs-lookup"><span data-stu-id="8e915-167">Smart Upgrade</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8e915-168">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="8e915-168">4.0 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-169">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8e915-169">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-170">Nicht anwendbar</span><span class="sxs-lookup"><span data-stu-id="8e915-170">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-171">Nicht anwendbar</span><span class="sxs-lookup"><span data-stu-id="8e915-171">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-172">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8e915-172">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-173">Intelligentes Upgrade</span><span class="sxs-lookup"><span data-stu-id="8e915-173">Smart Upgrade</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8e915-174">Unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="8e915-174">Supported configurations</span></span>


<span data-ttu-id="8e915-175">AGPM 4.0 SP2 unterstützt die Konfigurationen in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8e915-175">AGPM4.0 SP2 supports the configurations in the following table.</span></span> <span data-ttu-id="8e915-176">Obwohl AGPM Gemischte Konfigurationen unterstützt, wird dringend empfohlen, den AGPM-Client und AGPM-Server auf derselben Betriebssystem Zeile auszuführen, beispielsweise Windows 8.1 mit Windows Server2012 R2, Windows 8 mit Windows Server 2012 usw.</span><span class="sxs-lookup"><span data-stu-id="8e915-176">Although AGPM supports mixed configurations, we strongly recommend that you run the AGPM Client and AGPM Server on the same operating system line—for example, Windows8.1 with Windows Server2012 R2, Windows 8 with Windows Server 2012, and so on.</span></span>

**<span data-ttu-id="8e915-177">AGPM 4.0 SP2 unterstützte Betriebssysteme und Richtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="8e915-177">AGPM4.0 SP2 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="8e915-178">Unterstützte Konfigurationen für den AGPM-Server</span><span class="sxs-lookup"><span data-stu-id="8e915-178">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="8e915-179">Unterstützte Konfigurationen für den AGPM-Client</span><span class="sxs-lookup"><span data-stu-id="8e915-179">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="8e915-180">AGPM-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="8e915-180">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8e915-181">Windows Server2012 R2 oder Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8e915-181">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-182">Windows Server2012 R2 oder Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8e915-182">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-183">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="8e915-183">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8e915-184">Windows Server2012 R2, Windows Server 2012, Windows 8.1 oder Windows 8</span><span class="sxs-lookup"><span data-stu-id="8e915-184">Windows Server2012 R2, Windows Server 2012, Windows8.1, or Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-185">Windows Server 2012 oder Windows 8</span><span class="sxs-lookup"><span data-stu-id="8e915-185">Windows Server 2012 or Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-186">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows 8.1 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="8e915-186">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8e915-187">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="8e915-187">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-188">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="8e915-188">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-189">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur unter Windows 8.1 oder Windows 8 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="8e915-189">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1 or Windows 8</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8e915-190">Windows Server 2012, Windows Server2008R2, Windows 8 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="8e915-190">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-191">Windows Server2008 oder Windows Vista mit Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="8e915-191">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-192">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 oder Windows7 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="8e915-192">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, Windows 8, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8e915-193">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="8e915-193">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-194">Windows Server 2012, Windows Server2008R2, Windows 8 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="8e915-194">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-195">Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8e915-195">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8e915-196">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="8e915-196">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-197">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="8e915-197">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e915-198">Unterstützt, jedoch können keine Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 oder Windows7 vorhanden sind, gemeldet oder bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="8e915-198">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, Windows 8, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8e915-199">Voraussetzungen für die Installation von AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="8e915-199">Prerequisites for installing AGPM4.0 SP2</span></span>


<span data-ttu-id="8e915-200">In der folgenden Tabelle wird das Verhalten von AGPM 4.0 SP2-Client-und Server-Installationsprogrammen unter Windows 8.1 beschrieben, wenn .NET Framework 3.5 oder die GPMC in den Remote Server-Verwaltungs Tools nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8e915-200">The following table describes the behavior of AGPM4.0 SP2 Client and Server installers on Windows8.1 when the .NET Framework3.5 or the GPMC in the Remote Server Administration Tools is missing.</span></span>

**<span data-ttu-id="8e915-201">AGPM-Client</span><span class="sxs-lookup"><span data-stu-id="8e915-201">AGPM Client</span></span>**

**<span data-ttu-id="8e915-202">AGPM-Server</span><span class="sxs-lookup"><span data-stu-id="8e915-202">AGPM Server</span></span>**

**<span data-ttu-id="8e915-203">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="8e915-203">Operating system</span></span>**

**<span data-ttu-id="8e915-204">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="8e915-204">.NET Framework</span></span>**

**<span data-ttu-id="8e915-205">Remoteserver-Verwaltungstools</span><span class="sxs-lookup"><span data-stu-id="8e915-205">Remote Server Administration Tools</span></span>**

**<span data-ttu-id="8e915-206">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="8e915-206">.NET Framework</span></span>**

**<span data-ttu-id="8e915-207">Remoteserver-Verwaltungstools</span><span class="sxs-lookup"><span data-stu-id="8e915-207">Remote Server Administration Tools</span></span>**

**<span data-ttu-id="8e915-208">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8e915-208">Windows8.1</span></span>**

<span data-ttu-id="8e915-209">Wenn .NET Framework 3.5 nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation.</span><span class="sxs-lookup"><span data-stu-id="8e915-209">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="8e915-210">Wenn die GPMC nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation.</span><span class="sxs-lookup"><span data-stu-id="8e915-210">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="8e915-211">Wenn .NET Framework 3.5 nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation.</span><span class="sxs-lookup"><span data-stu-id="8e915-211">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="8e915-212">Wenn die GPMC nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation.</span><span class="sxs-lookup"><span data-stu-id="8e915-212">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span>

**<span data-ttu-id="8e915-213">Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="8e915-213">Windows Server2012 R2</span></span>**

<span data-ttu-id="8e915-214">Wenn .NET Framework 3.5 nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation.</span><span class="sxs-lookup"><span data-stu-id="8e915-214">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="8e915-215">Wenn die GPMC nicht aktiviert ist, wird Sie während der Installation von dem Installationsprogramm aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8e915-215">If the GPMC is not enabled, the installer enables it during the installation.</span></span>

<span data-ttu-id="8e915-216">Wenn .NET Framework 3.5 nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation.</span><span class="sxs-lookup"><span data-stu-id="8e915-216">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="8e915-217">Wenn die GPMC nicht aktiviert ist, wird Sie während der Installation von dem Installationsprogramm aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8e915-217">If the GPMC is not enabled, the installer enables it during the installation.</span></span>

 

## <span data-ttu-id="8e915-218">So erhalten Sie MDOP-Technologien</span><span class="sxs-lookup"><span data-stu-id="8e915-218">How to Get MDOP Technologies</span></span>


<span data-ttu-id="8e915-219">AGPM 4,0 SP2 ist Teil des Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="8e915-219">AGPM 4.0 SP2 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="8e915-220">MDOP ist Teil von Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="8e915-220">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="8e915-221">Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter [wie erhalte ich MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="8e915-221">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="8e915-222">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="8e915-222">Related topics</span></span>


[<span data-ttu-id="8e915-223">Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="8e915-223">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="8e915-224">Versionshinweise für Microsoft Advanced Group Policy Management 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="8e915-224">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP2</span></span>](release-notes-for-microsoft-advanced-group-policy-management-40-sp2.md)

[<span data-ttu-id="8e915-225">Welche Version von AGPM zur Installation auswählen</span><span class="sxs-lookup"><span data-stu-id="8e915-225">Choosing Which Version of AGPM to Install</span></span>](choosing-which-version-of-agpm-to-install.md)

 

 





