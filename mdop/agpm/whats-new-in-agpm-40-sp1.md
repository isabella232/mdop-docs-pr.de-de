---
title: Neuigkeiten in AGPM 4.0 SP1
description: Neuigkeiten in AGPM 4.0 SP1
author: dansimp
ms.assetid: c6a3d94a-13c3-44e6-a466-c3011879999e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca1ee4a1c2eb943a25246dc31b127eaf72ff5fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807392"
---
# <span data-ttu-id="81cfc-103">Neuigkeiten in AGPM 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="81cfc-103">What's New in AGPM 4.0 SP1</span></span>


<span data-ttu-id="81cfc-104">Dieser Inhalt "Neuerungen" beschreibt Verbesserungen und unterstützte Konfigurationen für Microsoft Advanced Group Policy Management (AGPM) 4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="81cfc-104">This “What’s New” content describes enhancements and supported configurations for Microsoft Advanced Group Policy Management (AGPM) 4.0 SP1.</span></span> <span data-ttu-id="81cfc-105">Wenn es einen Unterschied zwischen diesem Inhalt und einer anderen AGPM-Dokumentation gibt, sollte dieser Inhalt als autorisierend gelten und den in diesem Produkt enthaltenen Inhalt ersetzen.</span><span class="sxs-lookup"><span data-stu-id="81cfc-105">If there is a difference between this content and other AGPM documentation, this content should be considered authoritative and should supersede the content included with this product.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="81cfc-106">Neuigkeiten </span><span class="sxs-lookup"><span data-stu-id="81cfc-106">What’s new</span></span>


<span data-ttu-id="81cfc-107">AGPM 4,0 SP1 unterstützt die folgenden Verbesserungen:</span><span class="sxs-lookup"><span data-stu-id="81cfc-107">AGPM 4.0 SP1 supports the following enhancements:</span></span>

### <span data-ttu-id="81cfc-108">Neue und geänderte clientseitige Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="81cfc-108">New and changed client-side extensions</span></span>

<span data-ttu-id="81cfc-109">Für AGPM wurden Gruppenrichtlinien-clientseitige Erweiterungen (CSES) hinzugefügt oder geändert, um neue Gruppenrichtlinien in Windows 8 und Windows Server 2012 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="81cfc-109">Group Policy client-side extensions (CSEs) have been added or changed for AGPM to support new Group Policies in Windows 8 and Windows Server 2012.</span></span> <span data-ttu-id="81cfc-110">Mithilfe dieser Gruppenrichtlinien können Gruppenrichtlinienadministratoren Windows 8-spezifische Gruppenrichtlinieneinstellungen verwalten und nachvollziehen, die zwischen zwei Gruppenrichtlinienobjekten (Group Policy Objects, GPOs) oder Vorlagen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="81cfc-110">These group policies enable Group Policy administrators to manage and track Windows 8-specific Group Policy settings that change between two Group Policy Objects (GPOs) or templates.</span></span> <span data-ttu-id="81cfc-111">Sie können auch benutzerdefinierte GPOs mit Windows 8-spezifischen Einstellungen erstellen und die GPOs als Vorlage konfigurieren und speichern.</span><span class="sxs-lookup"><span data-stu-id="81cfc-111">You can also create custom GPOs, with Windows 8-specific settings, and configure and save the GPOs as a template.</span></span> <span data-ttu-id="81cfc-112">Verwenden Sie zum Anzeigen Ihrer CSEs die Einstellungen und Differenz Berichte, die im AGPM 4,0 SP1-Client verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="81cfc-112">To view your CSEs, use the settings and difference reports that are available in the AGPM 4.0 SP1 client.</span></span>

<span data-ttu-id="81cfc-113">Die neuen und geänderten Gruppenrichtlinien-clientseitigen Erweiterungen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="81cfc-113">The new and changed Group Policy client-side extensions are:</span></span>

-   <span data-ttu-id="81cfc-114">**Zentrale Zugriffsrichtlinie:** Ermöglicht Gruppenrichtlinienadministratoren, zentrale Zugriffsrichtlinien auf Gruppenrichtlinien Servern anzugeben, beispielsweise Dateiserver.</span><span class="sxs-lookup"><span data-stu-id="81cfc-114">**Central Access Policy:** Enables Group Policy administrators to specify Central Access Policies on Group Policy servers, for example, file servers.</span></span> <span data-ttu-id="81cfc-115">Bei der zentralen Zugriffsrichtlinie handelt es sich um eine Autorisierungsrichtlinie, die durch ein GPO-Element angegeben und auf Richtlinienziele angewendet wird, um den zentralisierten Zugriff und die Steuerung von Ressourcen zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="81cfc-115">Central Access Policy is an authorization policy that is specified by a GPO item and applied to policy targets to facilitate centralized access and control of resources.</span></span> <span data-ttu-id="81cfc-116">Diese Richtlinien für den zentralen Zugriff müssen auf einem Gruppenrichtlinien-Clientcomputer in Active Directory konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="81cfc-116">These Central Access Policies must be configured on a Group Policy client computer from within Active Directory.</span></span> <span data-ttu-id="81cfc-117">Eine Gruppenrichtlinie verteilt die Kenntnisse einer anwendbaren zentralen Zugriffsrichtlinie auf die Computer, die Sie erzwingen müssen.</span><span class="sxs-lookup"><span data-stu-id="81cfc-117">A Group Policy distributes the knowledge of an applicable Central Access Policy to the computers that have to enforce it.</span></span>

-   <span data-ttu-id="81cfc-118">**Richtlinienänderungen zur Namensauflösung:** Ermöglicht Gruppenrichtlinienadministratoren, Einstellungen für DNS-Sicherheit und DirectAccess auf DNS-Clientcomputern zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="81cfc-118">**Name Resolution Policy changes:** Enables Group Policy administrators to configure settings for DNS security and DirectAccess on DNS client computers.</span></span> <span data-ttu-id="81cfc-119">Neue Registerkarten zum Konfigurieren von generischen DNS-Server Einstellungen und Codierungseinstellungen wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="81cfc-119">New tabs for configuring Generic DNS Server settings and Encoding settings have been added.</span></span>

-   <span data-ttu-id="81cfc-120">**Änderungen der Gruppenrichtlinieneinstellungen:** Fügt Unterstützung für die Konfiguration und Verwaltung von Internet Explorer 10-Einstellungen hinzu, die für Windows 8 hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="81cfc-120">**Group Policy Preference changes:** Adds support for the configuration and management of Internet Explorer 10 settings that were added for Windows 8.</span></span>

-   <span data-ttu-id="81cfc-121">**Remote Anwendungen und Desktop Verbindungen:** Ermöglicht Gruppenrichtlinienadministratoren die Angabe der Standard Verbindungs-URL, die für Remote Anwendungen und Desktop Verbindungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="81cfc-121">**Remote Application and Desktop Connections:** Lets Group Policy administrators specify the default connection URL that is used for Remote Application and Desktop Connections.</span></span>

-   <span data-ttu-id="81cfc-122">**Windows to go-Startoptionen:** Ermöglicht Gruppenrichtlinienadministratoren, zu konfigurieren, ob der Computer mit Windows to go gestartet wird, wenn ein USB-Gerät mit einem Windows to go-Arbeitsbereich verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="81cfc-122">**Windows To Go Startup Options:** Lets Group Policy administrators configure whether the computer will boot to Windows To Go if a USB device that contains a Windows To Go workspace is connected.</span></span>

-   <span data-ttu-id="81cfc-123">**Windows to go-Optionen für den Ruhezustand:** Ermöglicht Gruppenrichtlinienadministratoren, zu konfigurieren, ob ein Computer den Ruhezustands Ruhezustand (S4) verwenden kann, wenn der Computer von einem Windows to go-Arbeitsbereich gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="81cfc-123">**Windows To Go Hibernate Options:** Lets Group Policy administrators configure whether a computer can use the hibernation sleep state (S4) when the computer is started from a Windows To Go workspace.</span></span>

### <span data-ttu-id="81cfc-124">Kundenfeedback und Hotfix-Rollup</span><span class="sxs-lookup"><span data-stu-id="81cfc-124">Customer feedback and hotfix rollup</span></span>

<span data-ttu-id="81cfc-125">AGPM 4,0 SP1 enthält ein Rollup mit Korrekturen zur Behebung von Problemen, die seit der AGPM 4,0-Version gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="81cfc-125">AGPM 4.0 SP1 includes a rollup of fixes to address issues found since the AGPM 4.0 release.</span></span> <span data-ttu-id="81cfc-126">AGPM 4,0 SP1 enthält die neuesten Fixes bis einschließlich Microsoft Advanced Group Policy Management 4,0 Hotfix 1.</span><span class="sxs-lookup"><span data-stu-id="81cfc-126">AGPM 4.0 SP1 contains the latest fixes up to and including Microsoft Advanced Group Policy Management 4.0 Hotfix 1.</span></span>

### <span data-ttu-id="81cfc-127">Einstellungen und Differenz Berichte zeigen neue Gruppenrichtlinienerweiterungen an</span><span class="sxs-lookup"><span data-stu-id="81cfc-127">Settings and difference reports show new Group Policy extensions</span></span>

<span data-ttu-id="81cfc-128">Die neuen Gruppenrichtlinienerweiterungen wurden zu den Einstellungen und Unterschiedsberichten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="81cfc-128">The new Group Policy extensions have been added to the settings and difference reports.</span></span>

### <span data-ttu-id="81cfc-129">Änderungen und Support für das Installationsprogramm</span><span class="sxs-lookup"><span data-stu-id="81cfc-129">Installer changes and support</span></span>

<span data-ttu-id="81cfc-130">Die Änderungen und Unterstützung für das AGPM 4,0 SP1-Installationsprogramm sind:</span><span class="sxs-lookup"><span data-stu-id="81cfc-130">The changes and support for the AGPM 4.0 SP1 installer are:</span></span>

-   <span data-ttu-id="81cfc-131">Wenn Sie AGPM 4,0 SP1 unter Windows 8 oder Windows Server 2012 installieren, überprüft das AGPM-Installationsprogramm, ob die erforderliche erforderliche Software (Gruppenrichtlinien-Verwaltungskonsole und .NET 3,5-Framework) installiert ist.</span><span class="sxs-lookup"><span data-stu-id="81cfc-131">If you install AGPM 4.0 SP1 on Windows 8 or Windows Server 2012, the AGPM installer verifies that the required prerequisite software (Group Policy Management Console and the .NET 3.5 Framework) is installed.</span></span> <span data-ttu-id="81cfc-132">Wenn diese Voraussetzungen nicht installiert sind, ist die Installation von AGPM 4,0 SP1 blockiert.</span><span class="sxs-lookup"><span data-stu-id="81cfc-132">If these prerequisites are not installed, the AGPM 4.0 SP1 installation is blocked.</span></span>

-   <span data-ttu-id="81cfc-133">Wenn Sie AGPM 4,0 SP1 installieren, werden die WCF-Aktivierung, die nicht-HTTP-Aktivierung und der Windows-Prozessaktivierungsdienst automatisch aktiviert.</span><span class="sxs-lookup"><span data-stu-id="81cfc-133">When you install AGPM 4.0 SP1, WCF Activation, Non-HTTP Activation, and Windows Process Activation Service are automatically enabled.</span></span>

-   <span data-ttu-id="81cfc-134">Laden Sie unter Windows Vista, Windows 7 und Windows 8-Clientbetriebssysteme die entsprechende Version des Remote System Administration Toolkit für Ihr Betriebs System herunter, bevor Sie AGPM 4,0 SP1 installieren.</span><span class="sxs-lookup"><span data-stu-id="81cfc-134">On Windows Vista, Windows 7, and Windows 8 client operating systems, download the appropriate version of the Remote System Administration Toolkit for your operating system before you install AGPM 4.0 SP1.</span></span>

-   <span data-ttu-id="81cfc-135">Abwärtskompatibilität mit älteren unterstützten Betriebssystemen wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="81cfc-135">Backward compatibility with older supported operating systems is supported.</span></span>

### <span data-ttu-id="81cfc-136">Möglichkeit zum Upgraden oder Aktualisieren auf AGPM 4,0 SP1 ohne erneutes Eingeben von Konfigurationsparametern</span><span class="sxs-lookup"><span data-stu-id="81cfc-136">Ability to upgrade or update to AGPM 4.0 SP1 without re-entering configuration parameters</span></span>

<span data-ttu-id="81cfc-137">Sie können den AGPM-Client oder-Server nur von AGPM 4,0 auf AGPM 4,0 SP1 aktualisieren, ohne dazu aufgefordert zu werden, die Konfigurationsparameter erneut einzugeben (so genannte "Smart Upgrade"), wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="81cfc-137">You can upgrade the AGPM client or server to AGPM 4.0 SP1 only from AGPM 4.0 without being prompted to re-enter configuration parameters (called “Smart Upgrade”), as shown in the following table.</span></span> <span data-ttu-id="81cfc-138">Wenn Sie ein Upgrade auf AGPM 4,0 SP1 aus anderen Versionen von AGPM durchführen, wie in der Tabelle gezeigt, müssen Sie das "klassische Upgrade" verwenden, bei dem Sie die Konfigurationsparameter erneut eingeben müssen.</span><span class="sxs-lookup"><span data-stu-id="81cfc-138">If you are upgrading to AGPM 4.0 SP1 from other versions of AGPM, as shown in the table, you must use the “Classic Upgrade,” which requires you to re-enter the configuration parameters.</span></span> <span data-ttu-id="81cfc-139">Da jede Version von AGPM einem bestimmten Betriebssystem zugeordnet ist, lesen Sie [auswählen, welche Version von AGPM installiert](https://go.microsoft.com/fwlink/?LinkId=254350)werden soll, und stellen Sie sicher, dass Sie vor dem Durchführen eines Upgrades Ihr Betriebssystem entsprechend aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="81cfc-139">Since each version of AGPM is associated with a particular operating system, refer to [Choosing Which Version of AGPM to Install](https://go.microsoft.com/fwlink/?LinkId=254350), and be sure to upgrade your operating system as appropriate before performing an upgrade.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="81cfc-140">AGPM-Version, auf der Sie ein Upgrade durchführen können</span><span class="sxs-lookup"><span data-stu-id="81cfc-140">AGPM Version From Which You Can Upgrade</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="81cfc-141">2,5</span><span class="sxs-lookup"><span data-stu-id="81cfc-141">2.5</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="81cfc-142">3.0</span><span class="sxs-lookup"><span data-stu-id="81cfc-142">3.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="81cfc-143">4.0</span><span class="sxs-lookup"><span data-stu-id="81cfc-143">4.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="81cfc-144">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="81cfc-144">4.0 SP1</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81cfc-145">2,5</span><span class="sxs-lookup"><span data-stu-id="81cfc-145">2.5</span></span></p></td>
<td align="left"><p><span data-ttu-id="81cfc-146">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="81cfc-146">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="81cfc-147">Klassisches Upgrade</span><span class="sxs-lookup"><span data-stu-id="81cfc-147">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="81cfc-148">Klassisches Upgrade</span><span class="sxs-lookup"><span data-stu-id="81cfc-148">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="81cfc-149">Die Installation ist blockiert</span><span class="sxs-lookup"><span data-stu-id="81cfc-149">Installation is blocked</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81cfc-150">3.0</span><span class="sxs-lookup"><span data-stu-id="81cfc-150">3.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="81cfc-151">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="81cfc-151">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="81cfc-152">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="81cfc-152">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="81cfc-153">Klassisches Upgrade</span><span class="sxs-lookup"><span data-stu-id="81cfc-153">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="81cfc-154">Die Installation ist blockiert</span><span class="sxs-lookup"><span data-stu-id="81cfc-154">Installation is blocked</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81cfc-155">4.0</span><span class="sxs-lookup"><span data-stu-id="81cfc-155">4.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="81cfc-156">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="81cfc-156">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="81cfc-157">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="81cfc-157">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="81cfc-158">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="81cfc-158">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="81cfc-159">Intelligentes Upgrade</span><span class="sxs-lookup"><span data-stu-id="81cfc-159">Smart Upgrade</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="81cfc-160">Unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="81cfc-160">Supported configurations</span></span>


<span data-ttu-id="81cfc-161">AGPM unterstützt die Konfigurationen in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="81cfc-161">AGPM supports the configurations in the following table.</span></span> <span data-ttu-id="81cfc-162">Obwohl AGPM Gemischte Konfigurationen unterstützt, wird dringend empfohlen, dass Sie den AGPM-Client und Server unter derselben Betriebssystemfamilie ausführen, beispielsweise Windows 8 mit Windows Server 2012, Windows 7 mit Windows Server 2008 R2 usw.</span><span class="sxs-lookup"><span data-stu-id="81cfc-162">Although AGPM supports mixed configurations, it is strongly recommended that you run the AGPM client and server on the same operating system family, for example, Windows 8 with Windows Server 2012, Windows 7 with Windows Server 2008 R2, and so on.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="81cfc-163">Unterstützte Konfigurationen für AGPM 4,0 SP1-Server</span><span class="sxs-lookup"><span data-stu-id="81cfc-163">Supported Configurations for AGPM 4.0 SP1 Server</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="81cfc-164">Unterstützte Konfigurationen für AGPM 4,0 SP1-Client</span><span class="sxs-lookup"><span data-stu-id="81cfc-164">Supported Configurations for AGPM 4.0 SP1 Client</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="81cfc-165">Unterstützung für AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="81cfc-165">AGPM 4.0 SP1 Support</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81cfc-166">Windows 8 oder Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="81cfc-166">Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="81cfc-167">Windows 8 oder Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="81cfc-167">Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="81cfc-168">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="81cfc-168">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81cfc-169">Windows Server 2008 R2 oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="81cfc-169">Windows Server 2008 R2 or Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="81cfc-170">Windows Server 2008 R2 oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="81cfc-170">Windows Server 2008 R2 or Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="81cfc-171">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows 8 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="81cfc-171">Supported, but cannot edit policy settings or preference items that exist only in Windows 8</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81cfc-172">Windows Server 2008 R2 oder Windows 7 oder Windows 8 oder Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="81cfc-172">Windows Server 2008 R2 or Windows 7 or Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="81cfc-173">Windows Server 2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="81cfc-173">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="81cfc-174">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server 2008 R2 oder Windows 7 oder Windows 8 vorhanden sind, können nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="81cfc-174">Supported, but cannot edit policy settings or preference items that exist only in Windows Server 2008 R2 or Windows 7 or Windows 8.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81cfc-175">Windows Server 2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="81cfc-175">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="81cfc-176">Windows Server 2008 R2 oder Windows 7 oder Windows 8 oder Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="81cfc-176">Windows Server 2008 R2 or Windows 7 or Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="81cfc-177">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="81cfc-177">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81cfc-178">Windows Server 2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="81cfc-178">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="81cfc-179">Windows Server 2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="81cfc-179">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="81cfc-180">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server 2008 R2 oder Windows 7 oder Windows 8 vorhanden sind, können nicht gemeldet oder bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="81cfc-180">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server 2008 R2 or Windows 7 or Windows 8</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="81cfc-181">Voraussetzungen für die Installation von AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="81cfc-181">Prerequisites for installing AGPM 4.0 SP1</span></span>


<span data-ttu-id="81cfc-182">In der folgenden Tabelle wird das Verhalten unter Windows 8 von AGPM 4,0 SP1-Client-und Server Installationsprogrammen beschrieben, wenn .NET 3,5 oder die Gruppenrichtlinien-Verwaltungskonsole in den Remote Server-Verwaltungs Tools (Remoteserver Administration Tools, Remoteserver-Verwaltungs Tools) fehlt.</span><span class="sxs-lookup"><span data-stu-id="81cfc-182">The following table describes the behavior on Windows 8 of AGPM 4.0 SP1 client and server installers when .NET 3.5 or the Group Policy Management Console in the Remote Server Administration Tools (RSAT) is missing.</span></span>

**<span data-ttu-id="81cfc-183">AGPM-Client 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="81cfc-183">AGPM Client 4.0 SP1</span></span>**

**<span data-ttu-id="81cfc-184">AGPM Server 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="81cfc-184">AGPM Server 4.0 SP1</span></span>**

**<span data-ttu-id="81cfc-185">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="81cfc-185">Operating System</span></span>**

**<span data-ttu-id="81cfc-186">.NET</span><span class="sxs-lookup"><span data-stu-id="81cfc-186">.NET</span></span>**

**<span data-ttu-id="81cfc-187">RSAT</span><span class="sxs-lookup"><span data-stu-id="81cfc-187">RSAT</span></span>**

**<span data-ttu-id="81cfc-188">.NET</span><span class="sxs-lookup"><span data-stu-id="81cfc-188">.NET</span></span>**

**<span data-ttu-id="81cfc-189">RSAT</span><span class="sxs-lookup"><span data-stu-id="81cfc-189">RSAT</span></span>**

**<span data-ttu-id="81cfc-190">Windows 8</span><span class="sxs-lookup"><span data-stu-id="81cfc-190">Windows 8</span></span>**

<span data-ttu-id="81cfc-191">Wenn .NET 3,5 nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation.</span><span class="sxs-lookup"><span data-stu-id="81cfc-191">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="81cfc-192">Wenn die GPMC nicht aktiviert oder auf dem System installiert ist, blockiert das Installationsprogramm die Installation.</span><span class="sxs-lookup"><span data-stu-id="81cfc-192">If GPMC is not enabled or installed on the system, the installer blocks the installation.</span></span>

<span data-ttu-id="81cfc-193">Wenn .NET 3,5 nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation.</span><span class="sxs-lookup"><span data-stu-id="81cfc-193">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="81cfc-194">Wenn die GPMC nicht aktiviert oder auf dem System installiert ist, blockiert das Installationsprogramm die Installation.</span><span class="sxs-lookup"><span data-stu-id="81cfc-194">If GPMC is not enabled or installed on the system, the installer blocks the installation.</span></span>

**<span data-ttu-id="81cfc-195">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="81cfc-195">Windows Server 2012</span></span>**

<span data-ttu-id="81cfc-196">Wenn .NET 3,5 nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation.</span><span class="sxs-lookup"><span data-stu-id="81cfc-196">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="81cfc-197">Wenn die GPMC nicht aktiviert ist, wird Sie während der Installation von dem Installationsprogramm aktiviert.</span><span class="sxs-lookup"><span data-stu-id="81cfc-197">If GPMC is not enabled, the installer enables it during the installation.</span></span>

<span data-ttu-id="81cfc-198">Wenn .NET 3,5 nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation.</span><span class="sxs-lookup"><span data-stu-id="81cfc-198">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="81cfc-199">Wenn die GPMC nicht aktiviert ist, wird Sie während der Installation von dem Installationsprogramm aktiviert.</span><span class="sxs-lookup"><span data-stu-id="81cfc-199">If GPMC is not enabled, the installer enables it during the installation.</span></span>

 

## <span data-ttu-id="81cfc-200">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="81cfc-200">Related topics</span></span>


[<span data-ttu-id="81cfc-201">Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="81cfc-201">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="81cfc-202">Versionshinweise für Microsoft Advanced Group Policy Management 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="81cfc-202">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP1</span></span>](release-notes-for-microsoft-advanced-group-policy-management-40-sp1.md)

 

 





