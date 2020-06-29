---
title: Infos zu MBAM 2.0 SP1
description: Infos zu MBAM 2.0 SP1
author: dansimp
ms.assetid: 5ba89ed8-bb6e-407b-82c2-e2e36dd1078e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 73b92cd852d4f75f63f3dcba9f18167012b61401
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810024"
---
# <span data-ttu-id="aa0b8-103">Infos zu MBAM 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="aa0b8-103">About MBAM 2.0 SP1</span></span>

<span data-ttu-id="aa0b8-104">In diesem Thema werden die Änderungen in Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,0 Service Pack 1 (SP1) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-104">This topic describes the changes in Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1).</span></span> <span data-ttu-id="aa0b8-105">Eine allgemeine Beschreibung von MBAM finden Sie unter [Erste Schritte mit MBAM 2,0](getting-started-with-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="aa0b8-105">For a general description of MBAM, see [Getting Started with MBAM 2.0](getting-started-with-mbam-20-mbam-2.md).</span></span>

## <a href="" id="what-s-new-in-mbam-2-0-sp1"></a><span data-ttu-id="aa0b8-106">Neuerungen in MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="aa0b8-106">What’s new in MBAM 2.0 SP1</span></span>

<span data-ttu-id="aa0b8-107">Diese Version von MBAM bietet die folgenden neuen Features und Funktionen.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-107">This version of MBAM provides the following new features and functionality.</span></span>

### <span data-ttu-id="aa0b8-108">Unterstützung für Windows 8,1, Windows Server 2012 R2 und System Center 2012 R2-Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="aa0b8-108">Support for Windows 8.1, Windows Server 2012 R2, and System Center 2012 R2 Configuration Manager</span></span>

<span data-ttu-id="aa0b8-109">Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,0 Service Pack 1 (SP1) bietet Unterstützung für Windows 8,1, Windows Server 2012 R2 und System Center 2012 R2-Konfigurations-Manager.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-109">Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1) adds support for Windows 8.1, Windows Server 2012 R2, and System Center 2012 R2 Configuration Manager.</span></span>

### <span data-ttu-id="aa0b8-110">Unterstützung für Microsoft SQL Server 2008 R2 SP2</span><span class="sxs-lookup"><span data-stu-id="aa0b8-110">Support for Microsoft SQL Server 2008 R2 SP2</span></span>

<span data-ttu-id="aa0b8-111">Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,0 Service Pack 1 (SP1) fügt Unterstützung für Microsoft SQL Server 2008 R2 SP2 hinzu.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-111">Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1) adds support for Microsoft SQL Server 2008 R2 SP2.</span></span> <span data-ttu-id="aa0b8-112">Sie müssen Microsoft SQL Server 2008 R2 oder höher verwenden, wenn Sie Microsoft System Center Configuration Manager 2007 R2 ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-112">You must use Microsoft SQL Server 2008 R2 or higher if you are running Microsoft System Center Configuration Manager 2007 R2.</span></span>

### <span data-ttu-id="aa0b8-113">Kundenfeedback-Rollup</span><span class="sxs-lookup"><span data-stu-id="aa0b8-113">Customer feedback rollup</span></span>

<span data-ttu-id="aa0b8-114">MBAM 2,0 SP1 enthält ein Rollup mit Korrekturen zur Behebung von Problemen, die seit der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,0-Version gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-114">MBAM 2.0 SP1 includes a rollup of fixes to address issues that were found since the Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 release.</span></span> <span data-ttu-id="aa0b8-115">Im Rahmen dieser Änderungen wird das Feld Computer Name nun in den Berichten BitLocker Computer Compliance und BitLocker Enterprise Compliance Details angezeigt, wenn Sie MBAM mit Microsoft System Center Configuration Manager 2007 ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-115">As part of these changes, the Computer Name field now appears in the BitLocker Computer Compliance and BitLocker Enterprise Compliance Details reports when you run MBAM with Microsoft System Center Configuration Manager 2007.</span></span>

### <span data-ttu-id="aa0b8-116">Firewall-Ausnahme muss für Ports für das Self-Service-Portal und die Website "Verwaltung und Überwachung" eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-116">Firewall exception must be set on ports for the Self-Service Portal and the Administration and Monitoring website</span></span>

<span data-ttu-id="aa0b8-117">Wenn Sie das Self-Service-Portal und die Verwaltungs-und Überwachungs Website konfigurieren, müssen Sie eine Firewall-Ausnahme festlegen, um die Kommunikation über die angegebenen Ports zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-117">When you configure the Self-Service Portal and the Administration and Monitoring website, you must set a firewall exception to enable communication through the specified ports.</span></span> <span data-ttu-id="aa0b8-118">Zuvor hat die MBAM-Server Installation die Ports automatisch in der Windows-Firewall geöffnet.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-118">Previously, the MBAM server installation opened the ports automatically in Windows Firewall.</span></span>

### <span data-ttu-id="aa0b8-119">Speicherort von MBAM-Berichten in Configuration Manager geändert</span><span class="sxs-lookup"><span data-stu-id="aa0b8-119">Location of MBAM reports has changed in Configuration Manager</span></span>

<span data-ttu-id="aa0b8-120">MBAM-Berichte für die integrierte Configuration Manager-Topologie sind jetzt unter Unterordner innerhalb des MBAM-Knotens verfügbar.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-120">MBAM reports for the Configuration Manager integrated topology are now available under subfolders within the MBAM node.</span></span> <span data-ttu-id="aa0b8-121">Die Namen der Unterordner stellen die Sprache der Berichte innerhalb des Unterordners dar.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-121">The subfolder names represent the language of the reports within the subfolder.</span></span>

### <span data-ttu-id="aa0b8-122">Möglichkeit zum Installieren von MBAM auf einem primären Standortserver bei der Installation von MBAM mit Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="aa0b8-122">Ability to install MBAM on a primary site server when you install MBAM with Configuration Manager</span></span>

<span data-ttu-id="aa0b8-123">Sie können MBAM auf einem primären Standortserver oder einem Website Server für die Zentraladministration installieren, wenn Sie MBAM mit der integrierten Configuration Manager-Topologie installieren.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-123">You can install MBAM on a primary site server or a central administration site server when you install MBAM with the Configuration Manager integrated topology.</span></span> <span data-ttu-id="aa0b8-124">Zuvor mussten Sie MBAM auf einem Website Server der Zentraladministration installieren.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-124">Previously, you were required to install MBAM on a central administration site server.</span></span>

**<span data-ttu-id="aa0b8-125">Wichtig</span><span class="sxs-lookup"><span data-stu-id="aa0b8-125">Important</span></span>**  
<span data-ttu-id="aa0b8-126">Der Server, auf dem Sie MBAM installieren, muss der oberste Ebene Server in Ihrer Hierarchie sein.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-126">The server on which you install MBAM must be the top-tier server in your hierarchy.</span></span>



<span data-ttu-id="aa0b8-127">Die MBAM-Installation funktioniert unterschiedlich für Microsoft System Center Configuration Manager 2007 und Microsoft System Center 2012 Configuration Manager wie folgt:</span><span class="sxs-lookup"><span data-stu-id="aa0b8-127">The MBAM installation works differently for Microsoft System Center Configuration Manager 2007 and Microsoft System Center 2012 Configuration Manager as follows:</span></span>

-   <span data-ttu-id="aa0b8-128">**Configuration Manager 2007** : Wenn Sie MBAM auf einem primären Standortserver installieren, der Teil einer größeren Configuration Manager-Hierarchie ist und über einen zentralen Standort übergeordneten Server verfügt, löst MBAM den übergeordneten zentralen Standortserver auf und führt alle Installationsaktionen auf dem übergeordneten Server aus.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-128">**Configuration Manager 2007** : If you install MBAM on a primary site server that is part of a larger Configuration Manager hierarchy and has a central site parent server, MBAM resolves the central site parent server and performs all of the installation actions on that parent server.</span></span> <span data-ttu-id="aa0b8-129">Zu den Installationsaktionen gehören das Überprüfen von Voraussetzungen und das Installieren der Configuration Manager-Objekte und-Berichte.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-129">The installation actions include checking prerequisites and installing the Configuration Manager objects and reports.</span></span> <span data-ttu-id="aa0b8-130">Wenn Sie beispielsweise MBAM auf einem primären Standortserver installieren, der ein untergeordnetes Element eines übergeordneten zentralen Standortservers ist, installiert MBAM alle Configuration Manager-Objekte und-Berichte auf dem übergeordneten Server.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-130">For example, if you install MBAM on a primary site server that is a child of a central site parent server, MBAM installs all of the Configuration Manager objects and reports on the parent server.</span></span> <span data-ttu-id="aa0b8-131">Wenn Sie MBAM auf dem übergeordneten Server installieren, führt MBAM alle Installationsaktionen auf dem übergeordneten Server aus.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-131">If you install MBAM on the parent server, MBAM performs all of the installation actions on that parent server.</span></span>

-   <span data-ttu-id="aa0b8-132">**System Center 2012-Konfigurations-Manager** : Wenn Sie MBAM auf einem primären Standortserver oder auf einem zentralen Administrationsserver installieren, führt MBAM alle Installationsaktionen auf diesem Website Server aus.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-132">**System Center 2012 Configuration Manager** : If you install MBAM on a primary site server or on a central administration server, MBAM performs all of the installation actions on that site server.</span></span>

### <a href="" id="-------------configuration-manager-console-must-be-installed-on-the--computer-on-which-you-install-the-mbam-server"></a> <span data-ttu-id="aa0b8-133">Die Configuration Manager-Konsole muss auf dem Computer installiert sein, auf dem Sie den MBAM-Server installieren.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-133">Configuration Manager Console must be installed on the computer on which you install the MBAM Server</span></span>

<span data-ttu-id="aa0b8-134">Wenn Sie MBAM mit der integrierten Configuration Manager-Topologie installieren, müssen Sie die Configuration Manager-Konsole auf dem Computer installieren, auf dem MBAM installiert wird.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-134">When you install MBAM with the Configuration Manager integrated topology, you must install the Configuration Manager Console on the same computer on which MBAM will be installed.</span></span> <span data-ttu-id="aa0b8-135">Wenn Sie die empfohlene Architektur verwenden, die unter [Erste Schritte – verwenden von MBAM mit Configuration Manager](getting-started---using-mbam-with-configuration-manager.md)beschrieben wird, würden Sie MBAM auf dem primären Configuration Manager-Standort Server installieren.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-135">If you use the recommended architecture, which is described in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md), you would install MBAM on the Configuration Manager Primary Site Server.</span></span>

### <span data-ttu-id="aa0b8-136">Neue Setup-Befehlszeilenparameter für die integrierte Configuration Manager-Topologie</span><span class="sxs-lookup"><span data-stu-id="aa0b8-136">New setup command-line parameters for the Configuration Manager integrated topology</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aa0b8-137">Befehlszeilen Parameter</span><span class="sxs-lookup"><span data-stu-id="aa0b8-137">Command-Line Parameter</span></span></th>
<th align="left"><span data-ttu-id="aa0b8-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa0b8-138">Description</span></span></th>
<th align="left"><span data-ttu-id="aa0b8-139">Beispiel</span><span class="sxs-lookup"><span data-stu-id="aa0b8-139">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa0b8-140">CM_SSRS_REMOTE_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="aa0b8-140">CM_SSRS_REMOTE_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa0b8-141">Ermöglicht es Ihnen, die Configuration Manager-Berichte auf einem Remoteserver für SQL Server Reporting Services (SSRS) zu installieren, der Teil desselben Configuration Manager-Standorts ist, auf dem MBAM installiert ist.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-141">Enables you to install the Configuration Manager reports on a remote SQL Server Reporting Services (SSRS) server that is part of the same Configuration Manager site to which MBAM is installed.</span></span> <span data-ttu-id="aa0b8-142">Sie können den Wert auf den vollqualifizierten Domänennamen des Remote-SSRS-Punkt Rollen Servers einstellen.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-142">You can set the value to the fully qualified domain name of the remote SSRS point role server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa0b8-143">MbamSetup.exe CM_SSRS_REMOTE_SERVER_NAME = ssrsServer. contoso. com</span><span class="sxs-lookup"><span data-stu-id="aa0b8-143">MbamSetup.exe CM_SSRS_REMOTE_SERVER_NAME=ssrsServer.Contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aa0b8-144">CM_REPORTS_ONLY</span><span class="sxs-lookup"><span data-stu-id="aa0b8-144">CM_REPORTS_ONLY</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa0b8-145">Ermöglicht es Ihnen, nur die Configuration Manager-Berichte zu installieren, ohne andere Configuration Manager-Objekte wie die Basisplan-, Sammlungs-und Konfigurationselemente.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-145">Enables you to install only the Configuration Manager reports, without other Configuration Manager objects, such as the baseline, collection, and configuration items.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="aa0b8-146">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="aa0b8-146">Note</span></span></strong><br/><p><span data-ttu-id="aa0b8-147">Sie müssen diesen Parameter mit dem CM_REPORTS_COLLECTION_ID-Parameter kombinieren.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-147">You must combine this parameter with the CM_REPORTS_COLLECTION_ID parameter.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="aa0b8-148">Gültige Parameterwerte:</span><span class="sxs-lookup"><span data-stu-id="aa0b8-148">Valid parameter values:</span></span></p>
<ul>
<li><p><span data-ttu-id="aa0b8-149">Wahr</span><span class="sxs-lookup"><span data-stu-id="aa0b8-149">True</span></span></p></li>
<li><p><span data-ttu-id="aa0b8-150">False</span><span class="sxs-lookup"><span data-stu-id="aa0b8-150">False</span></span></p></li>
</ul>
<p><span data-ttu-id="aa0b8-151">Sie können diesen Parameter mit dem CM_SSRS_REMOTE_SERVER_NAME-Parameter kombinieren, wenn Sie die Berichte nur auf einem Remote-SSRS-Punkt Rollen Server installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-151">You can combine this parameter with the CM_SSRS_REMOTE_SERVER_NAME parameter if you want to install the reports only to a remote SSRS point role server.</span></span></p>
<p><span data-ttu-id="aa0b8-152">Wenn Sie den Parameter nicht festlegen oder auf "false" festlegen, installiert MBAM Setup alle Configuration Manager-Objekte, einschließlich der Berichte.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-152">If you do not set the parameter or if you set it to False, MBAM Setup installs all of the Configuration Manager objects, including the reports.</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa0b8-153">MbamSetup.exe CM_REPORTS_ONLY = true</span><span class="sxs-lookup"><span data-stu-id="aa0b8-153">MbamSetup.exe CM_REPORTS_ONLY=True</span></span></p>
<p><span data-ttu-id="aa0b8-154">CM_REPORTS_COLLECTION_ID = SMS00001</span><span class="sxs-lookup"><span data-stu-id="aa0b8-154">CM_REPORTS_COLLECTION_ID=SMS00001</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa0b8-155">CM_REPORTS_COLLECTION_ID</span><span class="sxs-lookup"><span data-stu-id="aa0b8-155">CM_REPORTS_COLLECTION_ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa0b8-156">Eine vorhandene Sammlungs-ID, die die Sammlung identifiziert, für die Berichterstattungs Kompatibilitätsdaten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-156">An existing collection ID that identifies the collection for which reporting compliance data will be displayed.</span></span> <span data-ttu-id="aa0b8-157">Sie können eine beliebige Sammlungs-ID angeben.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-157">You can specify any collection ID.</span></span> <span data-ttu-id="aa0b8-158">Sie müssen die Sammlungs-ID "MBAM-unterstützte Computer" nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-158">You are not required to use the “MBAM Supported Computers” collection ID.</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa0b8-159">MbamSetup.exe CM_REPORTS_ONLY = true</span><span class="sxs-lookup"><span data-stu-id="aa0b8-159">MbamSetup.exe CM_REPORTS_ONLY=True</span></span></p>
<p><span data-ttu-id="aa0b8-160">CM_REPORTS_COLLECTION_ID = SMS00001</span><span class="sxs-lookup"><span data-stu-id="aa0b8-160">CM_REPORTS_COLLECTION_ID=SMS00001</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="aa0b8-161">Möglichkeit zum Aktivieren oder Deaktivieren des Self-Service-Portal-Notiztexts</span><span class="sxs-lookup"><span data-stu-id="aa0b8-161">Ability to turn Self-Service Portal notice text on or off</span></span>

<span data-ttu-id="aa0b8-162">Mit MBAM 2,0 SP1 können Sie den Hinweistext im Self-Service-Portal deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-162">MBAM 2.0 SP1 enables you to turn off the notice text on the Self-Service Portal.</span></span> <span data-ttu-id="aa0b8-163">Zuvor wurde der Hinweistext standardmäßig angezeigt, und Sie können ihn nicht deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-163">Previously, the notice text displayed by default, and you could not turn it off.</span></span>

**<span data-ttu-id="aa0b8-164">So deaktivieren Sie den Hinweistext</span><span class="sxs-lookup"><span data-stu-id="aa0b8-164">To turn off the notice text</span></span>**

1.  <span data-ttu-id="aa0b8-165">Öffnen Sie auf dem Server, auf dem Sie das Self-Service-Portal installiert haben, Internet Informationsdienste (IIS), und navigieren Sie zu **Websites &gt; Microsoft BitLocker-Verwaltungs-und Überwachungs &gt; Selfservice- &gt; Anwendungseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-165">On the server where you installed the Self-Service Portal, open Internet Information Services (IIS) and browse to **Sites &gt; Microsoft BitLocker Administration and Monitoring &gt; SelfService &gt; Application Settings**.</span></span>

2.  <span data-ttu-id="aa0b8-166">Wählen Sie in der Spalte **Name** die Option **DisplayNotice**aus, und legen Sie den Wert auf **false**fest.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-166">From the **Name** column, select **DisplayNotice**, and set the value to **false**.</span></span>

### <span data-ttu-id="aa0b8-167">Möglichkeit zum Lokalisieren der HelpdeskText-Anweisung, die Benutzer auf mehr Self-Service-Portal Informationen verweist</span><span class="sxs-lookup"><span data-stu-id="aa0b8-167">Ability to localize the HelpdeskText statement that points users to more Self-Service Portal information</span></span>

<span data-ttu-id="aa0b8-168">Sie können eine lokalisierte Version der Self-Service-Portal-Anweisung "HelpdeskText" konfigurieren, in der Endbenutzer erfahren, wie Sie bei Verwendung des Self-Service-Portals weitere Hilfe erhalten.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-168">You can configure a localized version of the Self-Service Portal “HelpdeskText” statement, which tells end users how to get additional help when they are using the Self-Service Portal.</span></span> <span data-ttu-id="aa0b8-169">Wenn Sie lokalisierten Text für die Anweisung konfigurieren, wie in den folgenden Anleitungen beschrieben, wird in MBAM die lokalisierte Version angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-169">If you configure localized text for the statement, as described in the following instructions, MBAM will display the localized version.</span></span> <span data-ttu-id="aa0b8-170">Wenn MBAM die lokalisierte Version nicht findet, wird der Wert im **HelpdeskText** -Parameter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-170">If MBAM does not find the localized version, it displays the value that is in the **HelpdeskText** parameter.</span></span>

**<span data-ttu-id="aa0b8-171">So zeigen Sie eine lokalisierte Version der HelpdeskText-Anweisung an</span><span class="sxs-lookup"><span data-stu-id="aa0b8-171">To display a localized version of the HelpdeskText statement</span></span>**

1.  <span data-ttu-id="aa0b8-172">Öffnen Sie auf dem Server, auf dem Sie das Self-Service-Portal installiert haben, IIS, und navigieren Sie zu **Websites &gt; Microsoft BitLocker-Verwaltungs-und Überwachungs &gt; Selfservice- &gt; Anwendungseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-172">On the server where you installed the Self-Service Portal, open IIS and browse to **Sites &gt; Microsoft BitLocker Administration and Monitoring &gt; SelfService &gt; Application Settings**.</span></span>

2.  <span data-ttu-id="aa0b8-173">Klicken Sie im Bereich **Aktionen** auf **Hinzufügen** , um das Dialogfeld **Anwendungseinstellung hinzufügen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-173">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="aa0b8-174">Geben Sie im Feld **Name den Namen** **HelpdeskText**\ _ &lt; *Language*ein &gt; , wobei &lt; *Sprache* &gt; der für den Text geeignete Sprachcode ist.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-174">In the **Name** field, type **HelpdeskText**\_&lt;*language*&gt;, where &lt;*language*&gt; is the appropriate language code for the text.</span></span> <span data-ttu-id="aa0b8-175">Wenn Sie beispielsweise eine lokalisierte HelpdeskText-Anweisung in Spanisch erstellen möchten, benennen Sie den Parameter HelpdeskText \ _ES-es.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-175">For example, to create a localized HelpdeskText statement in Spanish, you would name the parameter HelpdeskText\_es-es.</span></span> <span data-ttu-id="aa0b8-176">Eine Liste der gültigen Sprachcodes, die Sie verwenden können, finden Sie unter [National Language Support (NLS)-API-Referenz](https://go.microsoft.com/fwlink/?LinkId=317947).</span><span class="sxs-lookup"><span data-stu-id="aa0b8-176">For a list of the valid language codes that you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="aa0b8-177">Geben Sie im Feld **Wert** den lokalisierten Text ein, der Endbenutzern angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-177">In the **Value** field, type the localized text that you want to display to end users.</span></span>

### <span data-ttu-id="aa0b8-178">Möglichkeit zum Lokalisieren des Self-Service-Portals HelpdeskURL</span><span class="sxs-lookup"><span data-stu-id="aa0b8-178">Ability to localize the Self-Service Portal HelpdeskURL</span></span>

<span data-ttu-id="aa0b8-179">Sie können eine lokalisierte Version des Self-Service-Portals HelpdeskURL konfigurieren, damit die Endbenutzer standardmäßig angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-179">You can configure a localized version of the Self-Service Portal HelpdeskURL to display to end users by default.</span></span> <span data-ttu-id="aa0b8-180">Wenn Sie eine lokalisierte Version erstellen, wie in den folgenden Anleitungen beschrieben, findet MBAM die lokalisierte Version und zeigt Sie an.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-180">If you create a localized version, as described in the following instructions, MBAM finds and displays the localized version.</span></span> <span data-ttu-id="aa0b8-181">Wenn MBAM keine lokalisierte Version findet, wird die für den HelpDeskURL-Parameter konfigurierte URL angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-181">If MBAM does not find a localized version, it displays the URL that is configured for the HelpDeskURL parameter.</span></span>

**<span data-ttu-id="aa0b8-182">So zeigen Sie einen lokalisierten HelpdeskURL an</span><span class="sxs-lookup"><span data-stu-id="aa0b8-182">To display a localized HelpdeskURL</span></span>**

1.  <span data-ttu-id="aa0b8-183">Öffnen Sie auf dem Server, auf dem Sie das Self-Service-Portal installiert haben, IIS, und navigieren Sie zu **Websites &gt; Microsoft BitLocker-Verwaltungs-und Überwachungs &gt; Selfservice- &gt; Anwendungseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-183">On the server where you installed the Self-Service Portal, open IIS and browse to **Sites &gt; Microsoft BitLocker Administration and Monitoring &gt; SelfService &gt; Application Settings**.</span></span>

2.  <span data-ttu-id="aa0b8-184">Klicken Sie im Bereich **Aktionen** auf **Hinzufügen** , um das Dialogfeld **Anwendungseinstellung hinzufügen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-184">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="aa0b8-185">Geben Sie im Feld **Name den Namen** **HelpdeskURL**\ _ &lt; *Language*ein &gt; , wobei &lt; *Sprache* &gt; der geeignete Sprachcode für die URL ist.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-185">In the **Name** field, type **HelpdeskURL**\_&lt;*language*&gt;, where &lt;*language*&gt; is the appropriate language code for the URL.</span></span> <span data-ttu-id="aa0b8-186">Wenn Sie beispielsweise einen lokalisierten HelpdeskURL in Spanisch erstellen möchten, benennen Sie den Parameter HelpdeskURL \ _ES-es.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-186">For example, to create a localized HelpdeskURL in Spanish, you would name the parameter HelpdeskURL\_es-es.</span></span> <span data-ttu-id="aa0b8-187">Eine Liste der gültigen Sprachcodes, die Sie verwenden können, finden Sie unter [National Language Support (NLS)-API-Referenz](https://go.microsoft.com/fwlink/?LinkId=317947).</span><span class="sxs-lookup"><span data-stu-id="aa0b8-187">For a list of the valid language codes you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="aa0b8-188">Geben Sie im Feld **Wert** den lokalisierten HelpdeskURL ein, der den Endbenutzern angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-188">In the **Value** field, type the localized HelpdeskURL that you want to display to end users.</span></span>

### <span data-ttu-id="aa0b8-189">Möglichkeit zum Lokalisieren des Self-Service-Portal-Notiztexts</span><span class="sxs-lookup"><span data-stu-id="aa0b8-189">Ability to localize the Self-Service Portal notice text</span></span>

<span data-ttu-id="aa0b8-190">Sie können lokalisierten Benachrichtigungstext so konfigurieren, dass er für Endbenutzer standardmäßig im Self-Service-Portal angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-190">You can configure localized notice text to display to end users by default in the Self-Service Portal.</span></span> <span data-ttu-id="aa0b8-191">Die notice.txt-Datei, die den Hinweistext anzeigt, befindet sich im folgenden Stammverzeichnis:</span><span class="sxs-lookup"><span data-stu-id="aa0b8-191">The notice.txt file, which displays the notice text, is located in the following root directory:</span></span>

<span data-ttu-id="aa0b8-192">&lt;*MBAM Self-Service-Installationsverzeichnis* &gt; \\Self-Dienst Website</span><span class="sxs-lookup"><span data-stu-id="aa0b8-192">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

<span data-ttu-id="aa0b8-193">Wenn Sie lokalisierten Hinweistext anzeigen möchten, erstellen Sie eine lokalisierte notice.txt Datei, und speichern Sie Sie unter einem bestimmten Sprachordner im folgenden Verzeichnis:</span><span class="sxs-lookup"><span data-stu-id="aa0b8-193">To display localized notice text, you create a localized notice.txt file and save it under a specific language folder in the following directory:</span></span>

<span data-ttu-id="aa0b8-194">&lt;*MBAM Self-Service-Installationsverzeichnis* &gt; \\Self-Dienst Website</span><span class="sxs-lookup"><span data-stu-id="aa0b8-194">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

<span data-ttu-id="aa0b8-195">MBAM zeigt den Hinweistext auf der Grundlage der folgenden Regeln an:</span><span class="sxs-lookup"><span data-stu-id="aa0b8-195">MBAM displays the notice text, based on the following rules:</span></span>

-   <span data-ttu-id="aa0b8-196">Wenn Sie eine lokalisierte notice.txt Datei im entsprechenden Sprachordner erstellen, zeigt MBAM den lokalisierten Hinweistext an.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-196">If you create a localized notice.txt file in the appropriate language folder, MBAM displays the localized notice text.</span></span>

-   <span data-ttu-id="aa0b8-197">Wenn MBAM keine lokalisierte Version der notice.txt-Datei findet, wird der Text in der standardmäßigen notice.txt Datei angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-197">If MBAM does not find a localized version of the notice.txt file, it displays the text in the default notice.txt file.</span></span>

-   <span data-ttu-id="aa0b8-198">Wenn MBAM keine Standard notice.txt Datei findet, wird der Standardtext im Self-Service-Portal angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-198">If MBAM does not find a default notice.txt file, it displays the default text in the Self-Service Portal.</span></span>

**<span data-ttu-id="aa0b8-199">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="aa0b8-199">Note</span></span>**  
<span data-ttu-id="aa0b8-200">Wenn der Browser eines Endbenutzers auf eine Sprache festgesetzt ist, die keinen entsprechenden Unterordner "Sprache" oder notice.txt hat, wird der Text in der notice.txt Datei im folgenden Stammverzeichnis angezeigt:</span><span class="sxs-lookup"><span data-stu-id="aa0b8-200">If an end user’s browser is set to a language that does not have a corresponding language subfolder or notice.txt, the text that is in the notice.txt file in the following root directory is displayed:</span></span>

<span data-ttu-id="aa0b8-201">&lt;*MBAM Self-Service-Installationsverzeichnis* &gt; \\Self-Dienst Website</span><span class="sxs-lookup"><span data-stu-id="aa0b8-201">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\



**<span data-ttu-id="aa0b8-202">So erstellen Sie eine lokalisierte notice.txt-Datei</span><span class="sxs-lookup"><span data-stu-id="aa0b8-202">To create a localized notice.txt file</span></span>**

1.  <span data-ttu-id="aa0b8-203">Erstellen Sie auf dem Server, auf dem Sie das Self-Service-Portal installiert haben, einen &lt; *sprach* &gt; Ordner im folgenden Verzeichnis, wobei &lt; *Sprache* &gt; den Namen der lokalisierten Sprache darstellt:</span><span class="sxs-lookup"><span data-stu-id="aa0b8-203">On the server where you installed the Self-Service Portal, create a &lt;*language*&gt; folder in the following directory, where &lt;*language*&gt; represents the name of the localized language:</span></span>

    <span data-ttu-id="aa0b8-204">&lt;*MBAM Self-Service-Installationsverzeichnis* &gt; \\Self-Dienst Website</span><span class="sxs-lookup"><span data-stu-id="aa0b8-204">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

    **<span data-ttu-id="aa0b8-205">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="aa0b8-205">Note</span></span>**  
    <span data-ttu-id="aa0b8-206">Da einige Sprachordner bereits vorhanden sind, müssen Sie möglicherweise keine erstellen.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-206">Some language folders already exist, so you may not have to create one.</span></span> <span data-ttu-id="aa0b8-207">Wenn Sie einen Sprachordner erstellen müssen, finden Sie unter [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947) eine Liste der gültigen Namen, die Sie für den &lt; *sprach* &gt; Ordner verwenden können.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-207">If you do need to create a language folder, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947) for a list of the valid names that you can use for the &lt;*language*&gt; folder.</span></span>



2.  <span data-ttu-id="aa0b8-208">Erstellen Sie eine notice.txt-Datei, die den lokalisierten Benachrichtigungstext enthält.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-208">Create a notice.txt file that contains the localized notice text.</span></span>

3.  <span data-ttu-id="aa0b8-209">Speichern Sie die notice.txt Datei im &lt; Ordner *Sprache* &gt; .</span><span class="sxs-lookup"><span data-stu-id="aa0b8-209">Save the notice.txt file in the &lt;*language*&gt; folder.</span></span> <span data-ttu-id="aa0b8-210">Wenn Sie beispielsweise eine lokalisierte notice.txt Datei in Spanisch erstellen möchten, speichern Sie die lokalisierte notice.txt Datei im folgenden Ordner:</span><span class="sxs-lookup"><span data-stu-id="aa0b8-210">For example, to create a localized notice.txt file in Spanish, you would save the localized notice.txt file in the following folder:</span></span>

    <span data-ttu-id="aa0b8-211">&lt;*MBAM Self-Service-Installationsverzeichnis* &gt; \\Self-Dienst Website\\es-es</span><span class="sxs-lookup"><span data-stu-id="aa0b8-211">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\es-es</span></span>

## <span data-ttu-id="aa0b8-212">Upgrade auf MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="aa0b8-212">Upgrading to MBAM 2.0 SP1</span></span>


<span data-ttu-id="aa0b8-213">Sie können von jeder vorherigen Version von MBAM auf MBAM 2,0 SP1 aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-213">You can upgrade to MBAM 2.0 SP1 from any previous version of MBAM.</span></span>

### <span data-ttu-id="aa0b8-214">Aktualisieren der MBAM-Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="aa0b8-214">Upgrading the MBAM infrastructure</span></span>

<span data-ttu-id="aa0b8-215">Sie können die MBAM-Server Infrastruktur wie folgt auf MBAM 2,0 SP1 aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="aa0b8-215">You can upgrade the MBAM Server infrastructure to MBAM 2.0 SP1 as follows:</span></span>

<span data-ttu-id="aa0b8-216">**Manueller in-Place-Server Austausch**: Sie müssen die vorhandene MBAM-Serverinfrastruktur manuell deinstallieren und dann die MBAM 2,0 SP1-Serverinfrastruktur installieren.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-216">**Manual in-place server replacement**: You must manually uninstall the existing MBAM Server infrastructure, and then install the MBAM 2.0 SP1 Server infrastructure.</span></span> <span data-ttu-id="aa0b8-217">Sie müssen die Datenbanken nicht entfernen, um das Upgrade durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-217">You do not have to remove the databases to do the upgrade.</span></span> <span data-ttu-id="aa0b8-218">Stattdessen wählen Sie die vorhandenen Datenbanken aus, die von der vorherigen Version von MBAM erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-218">Instead, you select the existing databases, which the previous version of MBAM created.</span></span> <span data-ttu-id="aa0b8-219">Die MBAM 2,0 SP1-Upgrade-Installation migriert dann die vorhandenen Datenbanken zu MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-219">The MBAM 2.0 SP1 upgrade installation then migrates the existing databases to MBAM 2.0 SP1.</span></span>

<span data-ttu-id="aa0b8-220">**Upgrade des verteilten Clients**: Wenn Sie die eigenständige MBAM-Topologie verwenden, können Sie die MBAM-Clients nach der Installation der MBAM 2,0 SP1-Server Infrastruktur schrittweise aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-220">**Distributed client upgrade**: If you are using the Stand-alone MBAM topology, you can upgrade the MBAM Clients gradually after you install the MBAM 2.0 SP1 Server infrastructure.</span></span>

<span data-ttu-id="aa0b8-221">Nachdem Sie die MBAM-Server Infrastruktur aktualisiert haben, werden MBAM 1,0-oder 2,0-Clients dem MBAM 2,0 SP1-Server erfolgreich Bericht erstatten und die Wiederherstellungsdaten speichern, die Compliance basiert jedoch auf den Richtlinien, die für die derzeit installierte MBAM-Client Version verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-221">After you upgrade the MBAM Server infrastructure, MBAM 1.0 or 2.0 Clients will report to the MBAM 2.0 SP1 Server successfully and will store the recovery data, but compliance will be based on the policies available for the MBAM Client version that is currently installed.</span></span> <span data-ttu-id="aa0b8-222">Um die Berichterstellung für MBAM 2,0 SP1-Richtlinien zu aktivieren, müssen Sie Clientcomputer auf MBAM 2,0 SP1 aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-222">To enable reporting against MBAM 2.0 SP1 policies, you must upgrade client computers to MBAM 2.0 SP1.</span></span> <span data-ttu-id="aa0b8-223">Sie können die Clientcomputer auf den MBAM 2,0 SP1-Client aktualisieren, ohne den vorherigen Client zu deinstallieren, und der Client wird basierend auf den MBAM 2,0 SP1-Richtlinien mit der Anwendung und dem Bericht beginnen.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-223">You can upgrade the client computers to the MBAM 2.0 SP1 Client without uninstalling the previous Client, and the Client will start to apply and report, based on the MBAM 2.0 SP1 policies.</span></span>

<span data-ttu-id="aa0b8-224">Weitere Informationen zum Aktualisieren der MBAM-Server finden Sie unter [Upgrade von früheren Versionen von MBAM](upgrading-from-previous-versions-of-mbam.md).</span><span class="sxs-lookup"><span data-stu-id="aa0b8-224">For more information about upgrading the MBAM servers, see [Upgrading from Previous Versions of MBAM](upgrading-from-previous-versions-of-mbam.md).</span></span>

### <span data-ttu-id="aa0b8-225">Aktualisieren des MBAM-Clients auf MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="aa0b8-225">Upgrading the MBAM Client to MBAM 2.0 SP1</span></span>

<span data-ttu-id="aa0b8-226">Um Endbenutzercomputer auf den MBAM 2,0 SP1-Client zu aktualisieren, führen Sie **MbamClientSetup.exe** auf jedem Clientcomputer aus.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-226">To upgrade end-user computers to the MBAM 2.0 SP1 Client, run **MbamClientSetup.exe** on each client computer.</span></span> <span data-ttu-id="aa0b8-227">Das Installationsprogramm aktualisiert den Client automatisch auf den MBAM 2,0 SP1-Client.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-227">The installer automatically updates the Client to the MBAM 2.0 SP1 Client.</span></span> <span data-ttu-id="aa0b8-228">Nach der Installation müssen Clientcomputer nicht neu gestartet werden, und der MBAM 2,0 SP1-Client beginnt, die Richtlinien für MBAM 2,0 SP1 anzuwenden und zu melden.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-228">After the installation, client computers do not have to be rebooted, and the MBAM 2.0 SP1 Client starts to apply and report against MBAM 2.0 SP1 policies.</span></span>

<span data-ttu-id="aa0b8-229">Wenn Sie MBAM mit Configuration Manager verwenden, müssen Sie die MBAM-Clientcomputer auf MBAM 2,0 SP1 aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-229">If you are using MBAM with Configuration Manager, you must upgrade the MBAM client computers to MBAM 2.0 SP1.</span></span>

<span data-ttu-id="aa0b8-230">Weitere Informationen zum Aktualisieren der MBAM-Clientcomputer finden Sie unter [Upgrade von früheren Versionen von MBAM](upgrading-from-previous-versions-of-mbam.md).</span><span class="sxs-lookup"><span data-stu-id="aa0b8-230">For more information about upgrading the MBAM client computers, see [Upgrading from Previous Versions of MBAM](upgrading-from-previous-versions-of-mbam.md).</span></span>

## <span data-ttu-id="aa0b8-231">Installieren oder Aktualisieren auf MBAM 2,0 SP1 mit Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="aa0b8-231">Installing or upgrading to MBAM 2.0 SP1 with Configuration Manager</span></span>


<span data-ttu-id="aa0b8-232">In diesem Abschnitt werden die Anforderungen beschrieben, die bei der Installation von MBAM 2,0 SP1 als neue Installation oder als Upgrade auf eine vorherige MBAM 2,0 SP1-Installation auftreten.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-232">This section describes the requirements when you are installing MBAM 2.0 SP1 as a new installation or as an upgrade to a previous MBAM 2.0 SP1 installation.</span></span>

### <span data-ttu-id="aa0b8-233">Erforderliche Dateien für die Installation von MBAM 2,0 SP1, wenn Sie MBAM mit Configuration Manager verwenden</span><span class="sxs-lookup"><span data-stu-id="aa0b8-233">Required files for installing MBAM 2.0 SP1 if you are using MBAM with Configuration Manager</span></span>

<span data-ttu-id="aa0b8-234">Wenn Sie MBAM zum ersten Mal installieren und MBAM 2,0 SP1 mit System Center Configuration Manager verwenden, müssen Sie MOF-Dateien erstellen oder bearbeiten, damit MBAM mit Configuration Manager ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-234">If you are installing MBAM for the first time and you are using MBAM 2.0 SP1 with System Center Configuration Manager, you must create or edit mof files to enable MBAM to work correctly with Configuration Manager.</span></span>

-   **<span data-ttu-id="aa0b8-235">Datei "Configuration. mof"</span><span class="sxs-lookup"><span data-stu-id="aa0b8-235">configuration.mof file</span></span>**

    -   <span data-ttu-id="aa0b8-236">Wenn Sie Configuration Manager 2007 verwenden, müssen Sie die Datei "Configuration. mof" Bearbeiten, indem Sie Schritt 3 aus dem Element **Aktualisieren der Datei "Configuration. mof" ausführen, wenn Sie ein Upgrade auf MBAM 2,0 SP1 durchführen und MBAM mit Configuration Manager 2007 verwenden**, das diesem Element folgt.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-236">If you are using Configuration Manager 2007, you must edit the configuration.mof file by completing step 3 from the item **Update the configuration.mof file if you upgrade to MBAM 2.0 SP1 and you are using MBAM with Configuration Manager 2007**, which follows this item.</span></span>

    -   <span data-ttu-id="aa0b8-237">Wenn Sie den System Center 2012-Konfigurations-Manager verwenden, bearbeiten Sie die Datei "Configuration. mof", indem Sie die Anweisungen unter [Bearbeiten der Datei "Configuration. MOF](edit-the-configurationmof-file.md)" befolgen.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-237">If you are using System Center 2012 Configuration Manager, edit the configuration.mof file by following the instructions in [Edit the Configuration.mof File](edit-the-configurationmof-file.md).</span></span>

-   <span data-ttu-id="aa0b8-238">**SMS \ _def. MOF-Datei** – folgen Sie den Anweisungen unter [erstellen oder Bearbeiten der SMS \ _def. MOF-Datei](create-or-edit-the-sms-defmof-file.md).</span><span class="sxs-lookup"><span data-stu-id="aa0b8-238">**sms\_def.mof file** – follow the instructions in [Create or Edit the Sms\_def.mof File](create-or-edit-the-sms-defmof-file.md).</span></span>

### <span data-ttu-id="aa0b8-239">Aktualisieren Sie die Datei "Configuration. mof", wenn Sie ein Upgrade auf MBAM 2,0 SP1 durchführen und MBAM mit Configuration Manager 2007 verwenden.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-239">Update the configuration.mof file if you upgrade to MBAM 2.0 SP1 and you are using MBAM with Configuration Manager 2007</span></span>

<span data-ttu-id="aa0b8-240">Wenn Sie ein Upgrade auf MBAM 2,0 SP1 durchführt und MBAM mit Configuration Manager 2007 verwenden, müssen Sie die Datei "Configuration. mof" aktualisieren, um sicherzustellen, dass MBAM 2,0 SP1 ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-240">If you are upgrading to MBAM 2.0 SP1 and you are using MBAM with Configuration Manager 2007, you must update the configuration.mof file to ensure that MBAM 2.0 SP1 works correctly.</span></span>

**<span data-ttu-id="aa0b8-241">So aktualisieren Sie die Datei "Configuration. mof":</span><span class="sxs-lookup"><span data-stu-id="aa0b8-241">To update the configuration.mof file:</span></span>**

1.  <span data-ttu-id="aa0b8-242">Navigieren Sie auf dem Configuration Manager-Server zum Speicherort der Datei "Configuration. mof":</span><span class="sxs-lookup"><span data-stu-id="aa0b8-242">On the Configuration Manager Server, browse to the location of the Configuration.mof file:</span></span>

    <span data-ttu-id="aa0b8-243">&lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv</span><span class="sxs-lookup"><span data-stu-id="aa0b8-243">&lt;CMInstallLocation&gt;\\Inboxes\\clifiles.src\\hinv</span></span>\\

    <span data-ttu-id="aa0b8-244">Bei einer Standardinstallation ist der Installationsspeicherort%SystemDrive%\\Program-Dateien (x86) \\Microsoft-Konfigurations-Manager.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-244">On a default installation, the installation location is %systemdrive%\\Program Files (x86)\\Microsoft Configuration Manager.</span></span>

2.  <span data-ttu-id="aa0b8-245">Überprüfen Sie den Codeblock, den Sie an die Datei "Configuration. mof" angefügt haben, und löschen Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-245">Review the block of code that you appended to the configuration.mof file, and delete it.</span></span> <span data-ttu-id="aa0b8-246">Der Codeblock ähnelt dem im folgenden Schritt gezeigten Code.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-246">The block of code will be similar to the one shown in the following step.</span></span>

3.  <span data-ttu-id="aa0b8-247">Kopieren Sie den folgenden Codebaustein, und fügen Sie ihn dann an die Datei "Configuration. mof" an, um der Datei die folgenden erforderlichen MBAM-Klassen hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="aa0b8-247">Copy the following block of code, and then append it to the configuration.mof file to add the following required MBAM classes to the file:</span></span>

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL) 

    [Union, ViewSources{"select DeviceId, BitlockerPersistentVolumeId, BitLockerManagementPersistentVolumeId, BitLockerManagementVolumeType, DriveLetter, Compliant, ReasonsForNonCompliance, KeyProtectorTypes, EncryptionMethod, ConversionStatus, ProtectionStatus, IsAutoUnlockEnabled from Mbam_Volume"}, ViewSpaces{"\\\\.\\root\\microsoft\\mbam"}, dynamic, Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class Win32_BitLockerEncryptionDetails
    {
        [PropertySources{"DeviceId"},key]
        String     DeviceId;
        [PropertySources{"BitlockerPersistentVolumeId"}]
        String     BitlockerPersistentVolumeId;
        [PropertySources{"BitLockerManagementPersistentVolumeId"}]
        String     MbamPersistentVolumeId;
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        [PropertySources{"BitLockerManagementVolumeType"}]
        SInt32     MbamVolumeType;
        [PropertySources{"DriveLetter"}]
        String     DriveLetter;
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        [PropertySources{"Compliant"}]
        SInt32     Compliant;
        [PropertySources{"ReasonsForNonCompliance"}]
        SInt32     ReasonsForNonCompliance[];
        [PropertySources{"KeyProtectorTypes"}]
        SInt32     KeyProtectorTypes[];
        [PropertySources{"EncryptionMethod"}]
        SInt32     EncryptionMethod;
        [PropertySources{"ConversionStatus"}]
        SInt32     ConversionStatus;
        [PropertySources{"ProtectionStatus"}]
        SInt32     ProtectionStatus;
        [PropertySources{"IsAutoUnlockEnabled"}]
        Boolean     IsAutoUnlockEnabled;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
     [DYNPROPS]
    Class Win32Reg_MBAMPolicy
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate;
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

     [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy
    {
        KeyName="BitLocker policy";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy_64", NOFAIL)
    [DYNPROPS]
    Class Win32Reg_MBAMPolicy_64
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

    [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy_64
    {
        KeyName="BitLocker policy 64";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
         [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,OperatingSystemSKU from Win32_OperatingSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_OperatingSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"OperatingSystemSKU"}]
        uint32     SKU;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,PCSystemType from Win32_ComputerSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_ComputerSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"PCSystemType"}]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================

    ```

### <span data-ttu-id="aa0b8-248">Übersetzung von MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="aa0b8-248">Translation of MBAM 2.0 SP1</span></span>

<span data-ttu-id="aa0b8-249">MBAM 2,0 SP1 steht nun in den folgenden Sprachen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="aa0b8-249">MBAM 2.0 SP1 is now available in the following languages:</span></span>

-   <span data-ttu-id="aa0b8-250">Englisch (USA) en-US</span><span class="sxs-lookup"><span data-stu-id="aa0b8-250">English (United States) en-US</span></span>
-   <span data-ttu-id="aa0b8-251">Französisch (Frankreich) fr-FR</span><span class="sxs-lookup"><span data-stu-id="aa0b8-251">French (France) fr-FR</span></span>
-   <span data-ttu-id="aa0b8-252">Italienisch (Italien) IT-IT</span><span class="sxs-lookup"><span data-stu-id="aa0b8-252">Italian (Italy) it-IT</span></span>
-   <span data-ttu-id="aa0b8-253">Deutsch (Deutschland) de-de</span><span class="sxs-lookup"><span data-stu-id="aa0b8-253">German (Germany) de-DE</span></span>
-   <span data-ttu-id="aa0b8-254">Spanisch, internationale Sortierung (Spanien) es-es</span><span class="sxs-lookup"><span data-stu-id="aa0b8-254">Spanish, International Sort (Spain) es-ES</span></span>
-   <span data-ttu-id="aa0b8-255">Koreanisch (Korea) ko-kr</span><span class="sxs-lookup"><span data-stu-id="aa0b8-255">Korean (Korea) ko-KR</span></span>
-   <span data-ttu-id="aa0b8-256">Japanisch (Japan) ja-JP</span><span class="sxs-lookup"><span data-stu-id="aa0b8-256">Japanese (Japan) ja-JP</span></span>
-   <span data-ttu-id="aa0b8-257">Portugiesisch (Brasilien) pt-br</span><span class="sxs-lookup"><span data-stu-id="aa0b8-257">Portuguese (Brazil) pt-BR</span></span>
-   <span data-ttu-id="aa0b8-258">Russisch (Russland) ru-ru</span><span class="sxs-lookup"><span data-stu-id="aa0b8-258">Russian (Russia) ru-RU</span></span>
-   <span data-ttu-id="aa0b8-259">Chinesisch (traditionell) zh-tw</span><span class="sxs-lookup"><span data-stu-id="aa0b8-259">Chinese Traditional zh-TW</span></span>
-   <span data-ttu-id="aa0b8-260">Chinesisch (vereinfacht) zh-cn</span><span class="sxs-lookup"><span data-stu-id="aa0b8-260">Chinese Simplified zh-CN</span></span>

## <span data-ttu-id="aa0b8-261">So erhalten Sie MDOP-Technologien</span><span class="sxs-lookup"><span data-stu-id="aa0b8-261">How to Get MDOP Technologies</span></span>

<span data-ttu-id="aa0b8-262">MBAM 2,0 SP1 ist Teil des Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="aa0b8-262">MBAM 2.0 SP1 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="aa0b8-263">MDOP ist Teil von Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="aa0b8-263">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="aa0b8-264">Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter [wie erhalte ich MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="aa0b8-264">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="aa0b8-265">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="aa0b8-265">Related topics</span></span>

[<span data-ttu-id="aa0b8-266">Versionshinweise für MBAM 2.0SP1</span><span class="sxs-lookup"><span data-stu-id="aa0b8-266">Release Notes for MBAM 2.0 SP1</span></span>](release-notes-for-mbam-20-sp1.md)









