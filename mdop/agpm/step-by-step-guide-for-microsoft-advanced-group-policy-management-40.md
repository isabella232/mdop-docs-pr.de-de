---
title: Schrittweise Anleitung für Microsoft Advanced Group Policy Management 4.0
description: Schrittweise Anleitung für Microsoft Advanced Group Policy Management 4.0
author: dansimp
ms.assetid: dc6f9b16-b1d4-48f3-88bb-f29301f0131c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 819d536451095d23080115799016aa0ac5242dee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808211"
---
# <span data-ttu-id="aa997-103">Schrittweise Anleitung für Microsoft Advanced Group Policy Management 4.0</span><span class="sxs-lookup"><span data-stu-id="aa997-103">Step-by-Step Guide for Microsoft Advanced Group Policy Management 4.0</span></span>


<span data-ttu-id="aa997-104">Diese schrittweise Anleitung zeigt erweiterte Techniken für die Gruppenrichtlinienverwaltung, die die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) und Microsoft Advanced Group Policy Management (AGPM) verwenden.</span><span class="sxs-lookup"><span data-stu-id="aa997-104">This step-by-step guide demonstrates advanced techniques for Group Policy management that use the Group Policy Management Console (GPMC) and Microsoft Advanced Group Policy Management (AGPM).</span></span> <span data-ttu-id="aa997-105">AGPM vergrößert die Funktionen der GPMC und bietet Folgendes:</span><span class="sxs-lookup"><span data-stu-id="aa997-105">AGPM increases the capabilities of the GPMC, providing:</span></span>

-   <span data-ttu-id="aa997-106">Standard Rollen für das Delegieren von Berechtigungen zum Verwalten von Gruppenrichtlinienobjekten (GPOs) an mehrere Gruppenrichtlinienadministratoren sowie die Möglichkeit, den Zugriff auf GPOs in der Produktionsumgebung zu delegieren.</span><span class="sxs-lookup"><span data-stu-id="aa997-106">Standard roles for delegating permissions to manage Group Policy Objects (GPOs) to multiple Group Policy administrators, in addition to the ability to delegate access to GPOs in the production environment.</span></span>

-   <span data-ttu-id="aa997-107">Ein Archiv, damit Gruppenrichtlinienadministratoren GPOs offline erstellen und ändern können, bevor die GPOs in einer Produktionsumgebung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="aa997-107">An archive to enable Group Policy administrators to create and modify GPOs offline before the GPOs are deployed into a production environment.</span></span>

-   <span data-ttu-id="aa997-108">Die Möglichkeit, auf eine frühere Version eines GPO im Archiv zurückzusetzen und die Anzahl der im Archiv gespeicherten Versionen zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="aa997-108">The ability to roll back to any earlier version of a GPO in the archive and to limit the number of versions stored in the archive.</span></span>

-   <span data-ttu-id="aa997-109">Möglichkeit zum ein-und Auschecken von GPOs, um sicherzustellen, dass Gruppenrichtlinienadministratoren die Arbeit des anderen nicht versehentlich überschreiben.</span><span class="sxs-lookup"><span data-stu-id="aa997-109">Check-in and check-out capability for GPOs to make sure that Group Policy administrators do not unintentionally overwrite each other's work.</span></span>

-   <span data-ttu-id="aa997-110">Die Möglichkeit, nach GPOs mit bestimmten Attributen zu suchen und die Liste der angezeigten GPOs zu filtern.</span><span class="sxs-lookup"><span data-stu-id="aa997-110">The ability to search for GPOs with specific attributes and to filter the list of GPOs displayed.</span></span>

## <span data-ttu-id="aa997-111">Übersicht über AGPM-Szenarien</span><span class="sxs-lookup"><span data-stu-id="aa997-111">AGPM scenario overview</span></span>


<span data-ttu-id="aa997-112">In diesem Szenario verwenden Sie für jede Rolle in AGPM ein separates Benutzerkonto, um zu veranschaulichen, wie Gruppenrichtlinien in einer Umgebung verwaltet werden können, die mehrere Gruppenrichtlinienadministratoren mit unterschiedlichen Berechtigungsstufen aufweist.</span><span class="sxs-lookup"><span data-stu-id="aa997-112">For this scenario, you will use a separate user account for each role in AGPM to demonstrate how Group Policy can be managed in an environment that has multiple Group Policy administrators who have different levels of permissions.</span></span> <span data-ttu-id="aa997-113">Insbesondere führen Sie die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="aa997-113">Specifically, you will perform the following tasks:</span></span>

-   <span data-ttu-id="aa997-114">Wenn Sie ein Konto verwenden, das Mitglied der Gruppe der Domänenadministratoren ist, installieren Sie AGPM Server, und weisen Sie die Rolle AGPM-Administrator einem Konto oder einer Gruppe zu.</span><span class="sxs-lookup"><span data-stu-id="aa997-114">Using an account that is a member of the Domain Admins group, install AGPM Server and assign the AGPM Administrator role to an account or group.</span></span>

-   <span data-ttu-id="aa997-115">Installieren Sie AGPM-Client mithilfe von Konten, denen Sie AGPM-Rollen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="aa997-115">Using accounts to which you will assign AGPM roles, install AGPM Client.</span></span>

-   <span data-ttu-id="aa997-116">Verwenden Sie ein Konto mit der Rolle AGPM-Administrator, konfigurieren Sie AGPM, und delegieren Sie den Zugriff auf GPOs, indem Sie anderen Konten Rollen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="aa997-116">Using an account that has the AGPM Administrator role, configure AGPM and delegate access to GPOs by assigning roles to other accounts.</span></span>

-   <span data-ttu-id="aa997-117">Fordern Sie von einem Konto mit der Rolle "Editor" an, dass ein neues Gruppenrichtlinienobjekt erstellt wird, das Sie dann mit einem Konto genehmigen, das über die Rolle "genehmigende Person" verfügt.</span><span class="sxs-lookup"><span data-stu-id="aa997-117">From an account that has the Editor role, request that a new GPO be created that you then approve by using an account that has the Approver role.</span></span> <span data-ttu-id="aa997-118">Verwenden Sie das Editor-Konto, um das Gruppenrichtlinienobjekt aus dem Archiv zu überprüfen, das Gruppenrichtlinienobjekt zu bearbeiten, das Gruppenrichtlinienobjekt in das Archiv zu überprüfen und die Bereitstellung anzufordern.</span><span class="sxs-lookup"><span data-stu-id="aa997-118">Use the Editor account to check the GPO out of the archive, edit the GPO, check the GPO into the archive, and then request deployment.</span></span>

-   <span data-ttu-id="aa997-119">Überprüfen Sie das Gruppenrichtlinienobjekt, und stellen Sie es in Ihrer Produktionsumgebung bereit, indem Sie ein Konto verwenden, das die Rolle genehmigende Person aufweist.</span><span class="sxs-lookup"><span data-stu-id="aa997-119">Using an account that has the Approver role, review the GPO and deploy it to your production environment.</span></span>

-   <span data-ttu-id="aa997-120">Erstellen Sie mithilfe eines Kontos mit der Rolle "Editor" eine GPO-Vorlage, und verwenden Sie Sie als Ausgangspunkt zum Erstellen eines neuen Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="aa997-120">Using an account that has the Editor role, create a GPO template and use it as a starting point to create a new GPO.</span></span>

-   <span data-ttu-id="aa997-121">Wenn Sie ein Konto verwenden, das über die Rolle genehmigende Person verfügt, löschen Sie ein GPO, und stellen Sie es wieder her.</span><span class="sxs-lookup"><span data-stu-id="aa997-121">Using an account that has the Approver role, delete and restore a GPO.</span></span>

![Entwicklungsprozess für Gruppenrichtlinienobjekte](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <span data-ttu-id="aa997-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa997-123">Requirements</span></span>


<span data-ttu-id="aa997-124">Computer, auf denen Sie AGPM installieren möchten, müssen die folgenden Anforderungen erfüllen, und Sie müssen Konten erstellen, die in diesem Szenario verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="aa997-124">Computers on which you want to install AGPM must meet the following requirements, and you must create accounts for use in this scenario.</span></span>

<span data-ttu-id="aa997-125">**Hinweis**  Wenn Sie AGPM 2,5 installiert haben und ein Upgrade von Windows Server® 2003 auf Windows Server2008R2 oder Windows Server2008 durchführen oder ein Upgrade von Windows Vista ohne installierte Service Packs auf Windows7 oder Windows Vista® mit Service Pack1 (SP1) durchführen, müssen Sie das Betriebssystem aktualisieren, bevor Sie auf AGPM 4.0 aktualisieren können.</span><span class="sxs-lookup"><span data-stu-id="aa997-125">**Note** If you have AGPM 2.5 installed and are upgrading from Windows Server®2003 to Windows Server2008R2 or Windows Server2008, or are upgrading from WindowsVista with no service packs installed to Windows7 or WindowsVista® with Service Pack1 (SP1), you must upgrade the operating system before you can upgrade to AGPM4.0.</span></span>

<span data-ttu-id="aa997-126">Wenn Sie AGPM 3,0 installiert haben, müssen Sie das Betriebssystem nicht aktualisieren, bevor Sie auf AGPM 4,0 aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="aa997-126">If you have AGPM 3.0 installed, you do not have to upgrade the operating system before you upgrade to AGPM 4.0</span></span>

 

<span data-ttu-id="aa997-127">In einer gemischten Umgebung, die sowohl neuere als auch ältere Betriebssysteme umfasst, gibt es einige Funktionseinschränkungen, wie in der folgenden Tabelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="aa997-127">In a mixed environment that includes both newer and older operating systems, there are some limitations to functionality, as indicated in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aa997-128">Betriebssystem, auf dem AGPM Server 4,0 ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="aa997-128">Operating system on which AGPM Server 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="aa997-129">Betriebssystem, auf dem AGPM-Client 4,0 ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="aa997-129">Operating system on which AGPM Client 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="aa997-130">Status der Unterstützung von AGPM 4,0</span><span class="sxs-lookup"><span data-stu-id="aa997-130">Status of AGPM 4.0 support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa997-131">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="aa997-131">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa997-132">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="aa997-132">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa997-133">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="aa997-133">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aa997-134">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="aa997-134">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa997-135">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="aa997-135">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa997-136">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2008R2 oder Windows7 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="aa997-136">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa997-137">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="aa997-137">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa997-138">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="aa997-138">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa997-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="aa997-139">Unsupported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aa997-140">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="aa997-140">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa997-141">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="aa997-141">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa997-142">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2008R2 oder Windows7 vorhanden sind, können nicht gemeldet oder bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="aa997-142">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="aa997-143">AGPM-Server Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa997-143">AGPM Server requirements</span></span>

<span data-ttu-id="aa997-144">Für AGPM Server 4.0 sind Windows-Server2008R2, Windows Server2008, Windows7 und die GPMC von Remote Server-Verwaltungs Tools (Remote Server Administration Tools) oder Windows Vista mit SP1 und die GPMC von Remote Server-Verwaltungskonsole erforderlich.</span><span class="sxs-lookup"><span data-stu-id="aa997-144">AGPM Server4.0 requires Windows Server2008R2, Windows Server2008, Windows7 and the GPMC from Remote Server Administration Tools (RSAT), or Windows Vista with SP1 and the GPMC from RSAT installed.</span></span> <span data-ttu-id="aa997-145">Sowohl 32-Bit-als auch 64-Bit-Versionen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aa997-145">Both 32-bit and 64-bit versions are supported.</span></span>

<span data-ttu-id="aa997-146">Bevor Sie AGPM Server installieren, müssen Sie Mitglied der Gruppe der Domänenadministratoren sein, und die folgenden Windows-Features müssen vorhanden sein, sofern nicht anders angegeben:</span><span class="sxs-lookup"><span data-stu-id="aa997-146">Before you install AGPM Server, you must be a member of the Domain Admins group and the following Windows features must be present unless otherwise noted:</span></span>

-   <span data-ttu-id="aa997-147">GPMC</span><span class="sxs-lookup"><span data-stu-id="aa997-147">GPMC</span></span>

    -   <span data-ttu-id="aa997-148">Windows Server2008R2 oder Windows Server2008: Wenn die GPMC nicht vorhanden ist, wird Sie von AGPM automatisch installiert.</span><span class="sxs-lookup"><span data-stu-id="aa997-148">Windows Server2008R2 or Windows Server2008: If the GPMC is not present, it is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="aa997-149">Windows7: Sie müssen die GPMC vor der Installation von AGPM über die Remoteverwaltungskonsole installieren.</span><span class="sxs-lookup"><span data-stu-id="aa997-149">Windows7: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="aa997-150">Weitere Informationen finden Sie unter [Remote Server-Verwaltungs Tools für Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) ( https://go.microsoft.com/fwlink/?LinkID=131280) .</span><span class="sxs-lookup"><span data-stu-id="aa997-150">For more information, see [Remote Server Administration Tools for Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) (https://go.microsoft.com/fwlink/?LinkID=131280).</span></span>

    -   <span data-ttu-id="aa997-151">Windows Vista mit SP1: Sie müssen die GPMC vor der Installation von AGPM über die Remoteverwaltungskonsole installieren.</span><span class="sxs-lookup"><span data-stu-id="aa997-151">Windows Vista with SP1: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="aa997-152">Weitere Informationen finden Sie unter [Remote Server-Verwaltungs Tools für Windows Vista mit Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) ( https://go.microsoft.com/fwlink/?LinkID=116179) .</span><span class="sxs-lookup"><span data-stu-id="aa997-152">For more information, see [Remote Server Administration Tools for Windows Vista with Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) (https://go.microsoft.com/fwlink/?LinkID=116179).</span></span>

-   <span data-ttu-id="aa997-153">.NET Framework 3,5 oder höhere Versionen</span><span class="sxs-lookup"><span data-stu-id="aa997-153">The .NET Framework 3.5 or later versions</span></span>

    -   <span data-ttu-id="aa997-154">Windows Server2008R2 oder Windows7: Wenn die .NET Framework-Version 3,5 oder höher nicht vorhanden ist, wird .NET Framework 3,5 automatisch von AGPM installiert.</span><span class="sxs-lookup"><span data-stu-id="aa997-154">Windows Server2008R2 or Windows7: If the .NET Framework 3.5 or later version is not present, the .NET Framework 3.5 is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="aa997-155">Windows Server2008 oder Windows Vista mit SP1: Sie müssen .NET Framework 3,5 oder eine neuere Version installieren, bevor Sie AGPM installieren.</span><span class="sxs-lookup"><span data-stu-id="aa997-155">Windows Server2008 or Windows Vista with SP1: You must install the .NET Framework 3.5 or a later version before you install AGPM.</span></span>

<span data-ttu-id="aa997-156">Die folgenden Windows-Features sind für AGPM Server erforderlich und werden automatisch installiert, wenn Sie nicht vorhanden sind:</span><span class="sxs-lookup"><span data-stu-id="aa997-156">The following Windows features are required by AGPM Server and will be automatically installed if they are not present:</span></span>

-   <span data-ttu-id="aa997-157">WCF-Aktivierung; Nicht-HTTP-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="aa997-157">WCF Activation; Non-HTTP Activation</span></span>

-   <span data-ttu-id="aa997-158">Windows-Prozessaktivierungsdienst</span><span class="sxs-lookup"><span data-stu-id="aa997-158">Windows Process Activation Service</span></span>

    -   <span data-ttu-id="aa997-159">Prozessmodell</span><span class="sxs-lookup"><span data-stu-id="aa997-159">Process Model</span></span>

    -   <span data-ttu-id="aa997-160">.NET-Umgebung</span><span class="sxs-lookup"><span data-stu-id="aa997-160">The .NET Environment</span></span>

    -   <span data-ttu-id="aa997-161">Konfigurations-APIs</span><span class="sxs-lookup"><span data-stu-id="aa997-161">Configuration APIs</span></span>

### <span data-ttu-id="aa997-162">AGPM-Client Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa997-162">AGPM Client requirements</span></span>

<span data-ttu-id="aa997-163">AGPM Client 4.0 erfordert Windows-Server2008R2, Windows Server2008, Windows7 und die GPMC von der Remote-Verwaltungskonsole oder Windows Vista mit SP1 und die GPMC von Remote-Verwaltungskonsole installiert.</span><span class="sxs-lookup"><span data-stu-id="aa997-163">AGPM Client4.0 requires Windows Server2008R2, Windows Server2008, Windows7 and the GPMC from RSAT, or Windows Vista with SP1 and the GPMC from RSAT installed.</span></span> <span data-ttu-id="aa997-164">Sowohl 32-Bit-als auch 64-Bit-Versionen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aa997-164">Both 32-bit and 64-bit versions are supported.</span></span> <span data-ttu-id="aa997-165">AGPM-Client kann auf einem Computer installiert werden, auf dem AGPM Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa997-165">AGPM Client can be installed on a computer that is running AGPM Server.</span></span>

<span data-ttu-id="aa997-166">Die folgenden Windows-Features sind für AGPM-Client erforderlich und werden, sofern nicht anders angegeben, automatisch installiert, wenn Sie nicht vorhanden sind:</span><span class="sxs-lookup"><span data-stu-id="aa997-166">The following Windows features are required by AGPM Client and unless otherwise noted are automatically installed if they are not present:</span></span>

-   <span data-ttu-id="aa997-167">GPMC</span><span class="sxs-lookup"><span data-stu-id="aa997-167">GPMC</span></span>

    -   <span data-ttu-id="aa997-168">Windows Server2008R2 oder Windows Server2008: Wenn die GPMC nicht vorhanden ist, wird Sie von AGPM automatisch installiert.</span><span class="sxs-lookup"><span data-stu-id="aa997-168">Windows Server2008R2 or Windows Server2008: If the GPMC is not present, it is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="aa997-169">Windows7: Sie müssen die GPMC vor der Installation von AGPM über die Remoteverwaltungskonsole installieren.</span><span class="sxs-lookup"><span data-stu-id="aa997-169">Windows7: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="aa997-170">Weitere Informationen finden Sie unter [Remote Server-Verwaltungs Tools für Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) ( https://go.microsoft.com/fwlink/?LinkID=131280) .</span><span class="sxs-lookup"><span data-stu-id="aa997-170">For more information, see [Remote Server Administration Tools for Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) (https://go.microsoft.com/fwlink/?LinkID=131280).</span></span>

    -   <span data-ttu-id="aa997-171">Windows Vista mit SP1: Sie müssen die GPMC vor der Installation von AGPM über die Remoteverwaltungskonsole installieren.</span><span class="sxs-lookup"><span data-stu-id="aa997-171">Windows Vista with SP1: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="aa997-172">Weitere Informationen finden Sie unter [Remote Server-Verwaltungs Tools für Windows Vista mit Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) ( https://go.microsoft.com/fwlink/?LinkID=116179) .</span><span class="sxs-lookup"><span data-stu-id="aa997-172">For more information, see [Remote Server Administration Tools for Windows Vista with Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) (https://go.microsoft.com/fwlink/?LinkID=116179).</span></span>

-   <span data-ttu-id="aa997-173">.NET Framework 3,0 oder höhere Version</span><span class="sxs-lookup"><span data-stu-id="aa997-173">The .NET Framework 3.0 or later version</span></span>

    -   <span data-ttu-id="aa997-174">Windows Server2008R2 oder Windows7: Wenn die .NET Framework-Version 3,0 oder höher nicht vorhanden ist, wird .NET Framework 3,5 automatisch von AGPM installiert.</span><span class="sxs-lookup"><span data-stu-id="aa997-174">Windows Server2008R2 or Windows7: If the .NET Framework 3.0 or later version is not present, the .NET Framework 3.5 is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="aa997-175">Windows Server2008 oder Windows Vista mit SP1: Wenn die .NET Framework-Version 3,0 oder höher nicht vorhanden ist, wird .NET Framework 3,0 automatisch von AGPM installiert.</span><span class="sxs-lookup"><span data-stu-id="aa997-175">Windows Server2008 or Windows Vista with SP1: If the .NET Framework 3.0 or later version is not present, the .NET Framework 3.0 is automatically installed by AGPM.</span></span>

### <span data-ttu-id="aa997-176">Voraussetzungen für Szenarien</span><span class="sxs-lookup"><span data-stu-id="aa997-176">Scenario requirements</span></span>

<span data-ttu-id="aa997-177">Bevor Sie mit diesem Szenario beginnen, erstellen Sie vier Benutzerkonten.</span><span class="sxs-lookup"><span data-stu-id="aa997-177">Before you begin this scenario, create four user accounts.</span></span> <span data-ttu-id="aa997-178">Während des Szenarios weisen Sie jedem dieser Konten eine der folgenden AGPM-Rollen zu: AGPM-Administrator (Vollzugriff), genehmigende Person, Editor und Bearbeiter.</span><span class="sxs-lookup"><span data-stu-id="aa997-178">During the scenario, you will assign one of the following AGPM roles to each of these accounts: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="aa997-179">Diese Konten müssen in der Lage sein, e-Mail-Nachrichten zu senden und zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="aa997-179">These accounts must be able to send and receive e-mail messages.</span></span> <span data-ttu-id="aa997-180">Weisen Sie den Konten mit den Rollen des AGPM-Administrators, genehmigenden und (optional)-Editors die Berechtigung **Link-GPOs** zu.</span><span class="sxs-lookup"><span data-stu-id="aa997-180">Assign **Link GPOs** permission to the accounts that have the AGPM Administrator, Approver, and (optionally) Editor roles.</span></span>

<span data-ttu-id="aa997-181">**Hinweis** 
 Die Berechtigung " **GPOs verknüpfen** " wird standardmäßig Mitgliedern von Domänenadministratoren und Unternehmensadministratoren zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="aa997-181">**Note**
**Link GPOs** permission is assigned to members of Domain Administrators and Enterprise Administrators by default.</span></span> <span data-ttu-id="aa997-182">Klicken Sie auf den Knoten für die Domäne, und klicken Sie dann auf die Registerkarte **Delegierung** , wählen Sie **GPOs verknüpfen**aus, klicken Sie auf **Hinzufügen**, und wählen Sie dann Benutzer oder Gruppen aus, denen Sie **die Berechtigung zuweisen** möchten, um anderen Benutzern oder Gruppen (wie Konten, die die Rollen "AGPM-Administrator" oder "Genehmiger" aufweisen) Berechtigungen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="aa997-182">To assign **Link GPOs** permission to additional users or groups (such as accounts that have the roles of AGPM Administrator or Approver), click the node for the domain and then click the **Delegation** tab, select **Link GPOs**, click **Add**, and select users or groups to which you want to assign the permission.</span></span>

 

## <span data-ttu-id="aa997-183">Schritte zum Installieren und Konfigurieren von AGPM</span><span class="sxs-lookup"><span data-stu-id="aa997-183">Steps for installing and configuring AGPM</span></span>


<span data-ttu-id="aa997-184">Sie müssen die folgenden Schritte ausführen, um AGPM zu installieren und zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="aa997-184">You must complete the following steps to install and configure AGPM.</span></span>

[<span data-ttu-id="aa997-185">Schritt 1: Installieren des AGPM-Servers</span><span class="sxs-lookup"><span data-stu-id="aa997-185">Step 1: Install AGPM Server</span></span>](#bkmk-config1)

[<span data-ttu-id="aa997-186">Schritt 2: Installieren des AGPM-Clients</span><span class="sxs-lookup"><span data-stu-id="aa997-186">Step 2: Install AGPM Client</span></span>](#bkmk-config2)

[<span data-ttu-id="aa997-187">Schritt 3: Konfigurieren einer AGPM-Server Verbindung</span><span class="sxs-lookup"><span data-stu-id="aa997-187">Step 3: Configure an AGPM Server connection</span></span>](#bkmk-config3)

[<span data-ttu-id="aa997-188">Schritt 4: Konfigurieren einer e-Mail-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="aa997-188">Step 4: Configure e-mail notification</span></span>](#bkmk-config4)

[<span data-ttu-id="aa997-189">Schritt 5: Delegieren des Zugriffs</span><span class="sxs-lookup"><span data-stu-id="aa997-189">Step 5: Delegate access</span></span>](#bkmk-config5)

### <a href="" id="bkmk-config1"></a><span data-ttu-id="aa997-190">Schritt 1: Installieren des AGPM-Servers</span><span class="sxs-lookup"><span data-stu-id="aa997-190">Step 1: Install AGPM Server</span></span>

<span data-ttu-id="aa997-191">In diesem Schritt installieren Sie AGPM Server auf dem Mitglieds Server oder Domänencontroller, auf dem der AGPM-Dienst ausgeführt wird, und konfigurieren das Archiv.</span><span class="sxs-lookup"><span data-stu-id="aa997-191">In this step, you install AGPM Server on the member server or domain controller that will run the AGPM Service, and you configure the archive.</span></span> <span data-ttu-id="aa997-192">Alle AGPM-Vorgänge werden über diesen Windows-Dienst verwaltet und mit den Anmeldeinformationen des Diensts ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa997-192">All AGPM operations are managed through this Windows service and are executed with the service's credentials.</span></span> <span data-ttu-id="aa997-193">Das von einem AGPM-Server verwaltete Archiv kann auf diesem Server oder auf einem anderen Server in derselben Gesamtstruktur gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="aa997-193">The archive managed by an AGPM Server can be hosted on that server or on another server in the same forest.</span></span>

**<span data-ttu-id="aa997-194">So installieren Sie AGPM Server auf dem Computer, der den AGPM-Dienst hosten soll</span><span class="sxs-lookup"><span data-stu-id="aa997-194">To install AGPM Server on the computer that will host the AGPM Service</span></span>**

1.  <span data-ttu-id="aa997-195">Melden Sie sich mit einem Konto an, das Mitglied der Gruppe der Domänenadministratoren ist.</span><span class="sxs-lookup"><span data-stu-id="aa997-195">Log on with an account that is a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="aa997-196">Starten Sie die Microsoft Desktop Optimization Pack-CD, und folgen Sie den Anweisungen auf dem Bildschirm, um **Advanced Group Policy Management-Server**auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="aa997-196">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Server**.</span></span>

3.  <span data-ttu-id="aa997-197">Klicken Sie im Dialogfeld **Willkommen** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="aa997-197">In the **Welcome** dialog box, click **Next**.</span></span>

4.  <span data-ttu-id="aa997-198">Akzeptieren Sie im Dialogfeld **Microsoft-Software-Lizenzbestimmungen** die Begriffe, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="aa997-198">In the **Microsoft Software License Terms** dialog box, accept the terms and then click **Next**.</span></span>

5.  <span data-ttu-id="aa997-199">Wählen Sie im Dialogfeld **Anwendungspfad** einen Speicherort aus, an dem AGPM Server installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa997-199">In the **Application Path** dialog box, select a location in which to install AGPM Server.</span></span> <span data-ttu-id="aa997-200">Auf dem Computer, auf dem AGPM Server installiert ist, wird der AGPM-Dienst gehostet und das Archiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="aa997-200">The computer on which AGPM Server is installed will host the AGPM Service and manage the archive.</span></span> <span data-ttu-id="aa997-201">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="aa997-201">Click **Next**.</span></span>

6.  <span data-ttu-id="aa997-202">Wählen Sie im Dialogfeld **Archivpfad** einen Speicherort für das Archiv in Bezug auf den AGPM-Server aus.</span><span class="sxs-lookup"><span data-stu-id="aa997-202">In the **Archive Path** dialog box, select a location for the archive in relation to the AGPM Server.</span></span> <span data-ttu-id="aa997-203">Der Archivpfad kann auf einen Ordner auf dem AGPM-Server oder anderswo verweisen.</span><span class="sxs-lookup"><span data-stu-id="aa997-203">The archive path can point to a folder on the AGPM Server or elsewhere.</span></span> <span data-ttu-id="aa997-204">Sie sollten jedoch einen Speicherort mit genügend Speicherplatz auswählen, um alle GPOs und Verlaufsdaten zu speichern, die von diesem AGPM-Server verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="aa997-204">However, you should select a location with sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span> <span data-ttu-id="aa997-205">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="aa997-205">Click **Next**.</span></span>

7.  <span data-ttu-id="aa997-206">Wählen Sie im Dialogfeld **AGPM-Dienstkonto** ein Dienstkonto aus, unter dem der AGPM-Dienst ausgeführt wird, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="aa997-206">In the **AGPM Service Account** dialog box, select a service account under which the AGPM Service will run and then click **Next**.</span></span>

    <span data-ttu-id="aa997-207">Dieses Konto muss ein Mitglied der Gruppe der Domänenadministratoren oder, bei einer Konfiguration mit geringsten Berechtigungen, die folgenden Gruppen in jeder vom AGPM-Server verwalteten Domäne sein:</span><span class="sxs-lookup"><span data-stu-id="aa997-207">This account must be a member of the either the Domain Admins group or, for a least-privilege configuration, the following groups in each domain managed by the AGPM Server:</span></span>

    -   <span data-ttu-id="aa997-208">Besitzer von Gruppenrichtlinien Erstellern</span><span class="sxs-lookup"><span data-stu-id="aa997-208">Group Policy Creator Owners</span></span>

    -   <span data-ttu-id="aa997-209">Sicherungs-Operatoren</span><span class="sxs-lookup"><span data-stu-id="aa997-209">Backup Operators</span></span>

    <span data-ttu-id="aa997-210">Darüber hinaus erfordert dieses Konto die Berechtigung "Vollzugriff" für die folgenden Ordner:</span><span class="sxs-lookup"><span data-stu-id="aa997-210">Additionally, this account requires Full Control permission for the following folders:</span></span>

    -   <span data-ttu-id="aa997-211">Der Ordner "AGPM-Archiv", für den diese Berechtigung automatisch während der Installation von AGPM Server erteilt wird, wenn Sie auf einem lokalen Laufwerk installiert ist.</span><span class="sxs-lookup"><span data-stu-id="aa997-211">The AGPM archive folder, for which this permission is automatically granted during the installation of AGPM Server if it is installed on a local drive.</span></span>

    -   <span data-ttu-id="aa997-212">Der temporäre Ordner des lokalen Systems, in der Regel%windir%\\temp.</span><span class="sxs-lookup"><span data-stu-id="aa997-212">The local system temp folder, typically %windir%\\temp.</span></span>

8.  <span data-ttu-id="aa997-213">Wählen Sie im Dialogfeld **Besitzer des Archivs** ein Konto oder eine Gruppe aus, dem Sie die Rolle AGPM-Administrator (Vollzugriff) zuweisen.</span><span class="sxs-lookup"><span data-stu-id="aa997-213">In the **Archive Owner** dialog box, select an account or group to which you assign the AGPM Administrator (Full Control) role.</span></span> <span data-ttu-id="aa997-214">AGPM-Administratoren können AGPM-Rollen und-Berechtigungen anderen Gruppenrichtlinienadministratoren zuweisen, damit Sie später die Rolle des AGPM-Administrators zusätzlichen Gruppenrichtlinienadministratoren zuweisen können.</span><span class="sxs-lookup"><span data-stu-id="aa997-214">AGPM Administrators can assign AGPM roles and permissions to other Group Policy administrators, so that later you can assign the role of AGPM Administrator to additional Group Policy administrators.</span></span> <span data-ttu-id="aa997-215">Wählen Sie in diesem Szenario das Konto aus, das in der Rolle des AGPM-Administrators dienen soll.</span><span class="sxs-lookup"><span data-stu-id="aa997-215">For this scenario, select the account to serve in the AGPM Administrator role.</span></span> <span data-ttu-id="aa997-216">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="aa997-216">Click **Next**.</span></span>

9.  <span data-ttu-id="aa997-217">Geben Sie im Dialogfeld **Portkonfiguration** einen Port ein, den der AGPM-Dienst abhören soll.</span><span class="sxs-lookup"><span data-stu-id="aa997-217">In the **Port Configuration** dialog box, type a port on which the AGPM Service should listen.</span></span> <span data-ttu-id="aa997-218">Deaktivieren Sie das Kontrollkästchen **Portausnahme für Firewall hinzufügen** , es sei denn, Sie konfigurieren Portausnahmen manuell oder verwenden Regeln, um Portausnahmen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="aa997-218">Do not clear the **Add port exception to firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="aa997-219">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="aa997-219">Click **Next**.</span></span>

10. <span data-ttu-id="aa997-220">Wählen Sie im Dialogfeld **Sprachen** eine oder mehrere Anzeigesprachen aus, die für AGPM Server installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="aa997-220">In the **Languages** dialog box, select one or more display languages to install for AGPM Server.</span></span>

11. <span data-ttu-id="aa997-221">Klicken Sie auf **Installieren**, und klicken Sie dann auf **Fertig stellen** , um den Setup-Assistenten zu beenden.</span><span class="sxs-lookup"><span data-stu-id="aa997-221">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

    <span data-ttu-id="aa997-222">**Vorsicht**  Ändern Sie die Einstellungen für den AGPM-Dienst nicht über **Administrative Tools** und **Dienste** im Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="aa997-222">**Caution** Do not change settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="aa997-223">Dadurch kann der Start des AGPM-Diensts verhindert werden.</span><span class="sxs-lookup"><span data-stu-id="aa997-223">Doing this can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="aa997-224">Informationen zum Ändern der Einstellungen für den Dienst finden Sie unter Hilfe zur erweiterten Gruppenrichtlinienverwaltung.</span><span class="sxs-lookup"><span data-stu-id="aa997-224">For information about how to change settings for the service, see Help for Advanced Group Policy Management.</span></span>

     

### <a href="" id="bkmk-config2"></a><span data-ttu-id="aa997-225">Schritt 2: Installieren des AGPM-Clients</span><span class="sxs-lookup"><span data-stu-id="aa997-225">Step 2: Install AGPM Client</span></span>

<span data-ttu-id="aa997-226">Jeder Gruppenrichtlinienadministrator – jeder, der GPOs erstellt, bearbeitet, bereitstellt, überprüft oder löscht, muss AGPM-Client auf Computern installiert haben, die Sie zum Verwalten von GPOs verwenden.</span><span class="sxs-lookup"><span data-stu-id="aa997-226">Each Group Policy administrator—anyone who creates, edits, deploys, reviews, or deletes GPOs—must have AGPM Client installed on computers that they use to manage GPOs.</span></span> <span data-ttu-id="aa997-227">Der Knoten Änderungs Steuerelement, mit dem Sie viele der GPO-Verwaltungsaufgaben ausführen, wird nur dann in der Gruppenrichtlinien-Verwaltungskonsole angezeigt, wenn Sie den AGPM-Client installieren.</span><span class="sxs-lookup"><span data-stu-id="aa997-227">The Change Control node, which you use to perform many of the GPO management tasks, appears in the Group Policy Management Console only if you install the AGPM Client.</span></span> <span data-ttu-id="aa997-228">In diesem Szenario installieren Sie AGPM-Client auf mindestens einem Computer.</span><span class="sxs-lookup"><span data-stu-id="aa997-228">For this scenario, you install AGPM Client on at least one computer.</span></span> <span data-ttu-id="aa997-229">Sie müssen den AGPM-Client nicht auf den Computern von Endbenutzern installieren, die keine Gruppenrichtlinienverwaltung durchführen.</span><span class="sxs-lookup"><span data-stu-id="aa997-229">You do not need to install AGPM Client on the computers of end users who do not perform Group Policy administration.</span></span>

**<span data-ttu-id="aa997-230">So installieren Sie den AGPM-Client auf dem Computer eines Gruppenrichtlinienadministrators</span><span class="sxs-lookup"><span data-stu-id="aa997-230">To install AGPM Client on the computer of a Group Policy administrator</span></span>**

1.  <span data-ttu-id="aa997-231">Starten Sie die Microsoft Desktop Optimization Pack-CD, und folgen Sie den Anweisungen auf dem Bildschirm, um **Erweiterte Gruppenrichtlinienverwaltung-Client**auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="aa997-231">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Client**.</span></span>

2.  <span data-ttu-id="aa997-232">Klicken Sie im Dialogfeld **Willkommen** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="aa997-232">In the **Welcome** dialog box, click **Next**.</span></span>

3.  <span data-ttu-id="aa997-233">Akzeptieren Sie im Dialogfeld **Microsoft-Software-Lizenzbestimmungen** die Begriffe, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="aa997-233">In the **Microsoft Software License Terms** dialog box, accept the terms and then click **Next**.</span></span>

4.  <span data-ttu-id="aa997-234">Wählen Sie im Dialogfeld **Anwendungspfad** einen Speicherort aus, an dem AGPM-Client installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa997-234">In the **Application Path** dialog box, select a location in which to install AGPM Client.</span></span> <span data-ttu-id="aa997-235">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="aa997-235">Click **Next**.</span></span>

5.  <span data-ttu-id="aa997-236">Geben Sie im Dialogfeld **AGPM-Server** den DNS-Namen oder die IP-Adresse für den AGPM-Server und den Port ein, mit dem Sie eine Verbindung herstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="aa997-236">In the **AGPM Server** dialog box, type the DNS name or IP address for the AGPM Server and the port to which you want to connect.</span></span> <span data-ttu-id="aa997-237">Der Standardport für den AGPM-Dienst ist 4600.</span><span class="sxs-lookup"><span data-stu-id="aa997-237">The default port for the AGPM Service is 4600.</span></span> <span data-ttu-id="aa997-238">Deaktivieren Sie das Kontrollkästchen **Microsoft Management Console über das Firewall zulassen** , es sei denn, Sie konfigurieren Portausnahmen manuell oder verwenden Regeln, um Portausnahmen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="aa997-238">Do not clear the **Allow Microsoft Management Console through the firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="aa997-239">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="aa997-239">Click **Next**.</span></span>

6.  <span data-ttu-id="aa997-240">Wählen Sie im Dialogfeld **Sprachen** eine oder mehrere Anzeigesprachen aus, die für AGPM-Client installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="aa997-240">In the **Languages** dialog box, select one or more display languages to install for AGPM Client.</span></span>

7.  <span data-ttu-id="aa997-241">Klicken Sie auf **Installieren**, und klicken Sie dann auf **Fertig stellen** , um den Setup-Assistenten zu beenden.</span><span class="sxs-lookup"><span data-stu-id="aa997-241">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

### <a href="" id="bkmk-config3"></a><span data-ttu-id="aa997-242">Schritt 3: Konfigurieren einer AGPM-Server Verbindung</span><span class="sxs-lookup"><span data-stu-id="aa997-242">Step 3: Configure an AGPM Server connection</span></span>

<span data-ttu-id="aa997-243">AGPM speichert alle Versionen der einzelnen gesteuerten Gruppenrichtlinienobjekte (GPO), also jedes GPO, für das AGPM Änderungs Steuerelemente bereitstellt, in einem zentralen Archiv.</span><span class="sxs-lookup"><span data-stu-id="aa997-243">AGPM stores all versions of each controlled Group Policy Object (GPO), that is, each GPO for which AGPM provides change control, in a central archive.</span></span> <span data-ttu-id="aa997-244">Dadurch können Gruppenrichtlinienadministratoren Gruppenrichtlinienobjekte offline anzeigen und ändern, ohne die bereitgestellte Version jedes GPO unmittelbar zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="aa997-244">This lets Group Policy administrators view and change GPOs offline without immediately affecting the deployed version of each GPO.</span></span>

<span data-ttu-id="aa997-245">In diesem Schritt konfigurieren Sie eine AGPM-Serververbindung und stellen sicher, dass alle Gruppenrichtlinienadministratoren eine Verbindung mit dem gleichen AGPM-Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="aa997-245">In this step, you configure an AGPM Server connection and ensure that all Group Policy administrators connect to the same AGPM Server.</span></span> <span data-ttu-id="aa997-246">(Informationen zum Konfigurieren mehrerer AGPM-Server finden Sie unter Hilfe zur erweiterten Gruppenrichtlinienverwaltung.)</span><span class="sxs-lookup"><span data-stu-id="aa997-246">(For information about how to configure multiple AGPM Servers, see Help for Advanced Group Policy Management.)</span></span>

**<span data-ttu-id="aa997-247">So konfigurieren Sie eine AGPM-Server Verbindung für alle Gruppenrichtlinienadministratoren</span><span class="sxs-lookup"><span data-stu-id="aa997-247">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="aa997-248">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit dem Benutzerkonto an, das Sie als Archiv Besitzer ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="aa997-248">On a computer on which you have installed AGPM Client, log on with the user account that you selected as the Archive Owner.</span></span> <span data-ttu-id="aa997-249">Dieser Benutzer hat die Rolle des AGPM-Administrators (Vollzugriff).</span><span class="sxs-lookup"><span data-stu-id="aa997-249">This user has the role of AGPM Administrator (Full Control).</span></span>

2.  <span data-ttu-id="aa997-250">Klicken Sie auf **Start**, zeigen Sie auf **Verwaltung**, und klicken Sie dann auf **Gruppenrichtlinienverwaltung** , um die GPMC zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="aa997-250">Click **Start**, point to **Administrative Tools**, and then click **Group Policy Management** to open the GPMC.</span></span>

3.  <span data-ttu-id="aa997-251">Bearbeiten Sie ein Gruppenrichtlinienobjekt, das auf alle Gruppenrichtlinienadministratoren angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="aa997-251">Edit a GPO that is applied to all Group Policy administrators.</span></span>

4.  <span data-ttu-id="aa997-252">Doppelklicken Sie im Fenster **Gruppenrichtlinien-Verwaltungs-Editor** auf **Benutzerkonfiguration**, **Richtlinien**, **Administrative Vorlagen**, **Windows-Komponenten**und **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="aa997-252">In the **Group Policy Management Editor** window, double-click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

5.  <span data-ttu-id="aa997-253">Doppelklicken Sie im Detailbereich auf **AGPM: standardmäßiger AGPM-Server (alle Domänen) angeben**.</span><span class="sxs-lookup"><span data-stu-id="aa997-253">In the details pane, double-click **AGPM: Specify default AGPM Server (all domains)**.</span></span>

6.  <span data-ttu-id="aa997-254">Wählen Sie im **Eigenschaften** Fenster die Option **aktiviert** aus, und geben Sie den DNS-Namen oder die IP-Adresse und den Port (beispielsweise **Server.contoso.com:4600**) für den Server ein, der das Archiv hostet.</span><span class="sxs-lookup"><span data-stu-id="aa997-254">In the **Properties** window, select **Enabled** and type the DNS name or IP address and port (for example, **server.contoso.com:4600**) for the server hosting the archive.</span></span> <span data-ttu-id="aa997-255">Standardmäßig verwendet der AGPM-Dienst Port 4600.</span><span class="sxs-lookup"><span data-stu-id="aa997-255">By default, the AGPM Service uses port 4600.</span></span>

7.  <span data-ttu-id="aa997-256">Klicken Sie auf **OK**, und schließen Sie dann das Fenster **Gruppenrichtlinien-Verwaltungs-Editor** .</span><span class="sxs-lookup"><span data-stu-id="aa997-256">Click **OK**, and then close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="aa997-257">Wenn die Gruppenrichtlinie aktualisiert wird, wird die AGPM-Server Verbindung für jeden Gruppenrichtlinienadministrator konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="aa997-257">When Group Policy is updated, the AGPM Server connection is configured for each Group Policy administrator.</span></span>

### <a href="" id="bkmk-config4"></a><span data-ttu-id="aa997-258">Schritt 4: Konfigurieren einer e-Mail-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="aa997-258">Step 4: Configure e-mail notification</span></span>

<span data-ttu-id="aa997-259">Als AGPM-Administrator (Vollzugriff) legen Sie die e-Mail-Adressen von Genehmigern und AGPM-Administratoren fest, denen eine e-Mail-Nachricht mit einer Anforderung gesendet wird, wenn ein Editor versucht, ein GPO zu erstellen, bereitzustellen oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="aa997-259">As an AGPM Administrator (Full Control), you designate the e-mail addresses of Approvers and AGPM Administrators to whom an e-mail message that contains a request is sent when an Editor tries to create, deploy, or delete a GPO.</span></span> <span data-ttu-id="aa997-260">Darüber hinaus ermitteln Sie den Alias, aus dem diese Nachrichten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="aa997-260">You also determine the alias from which these messages are sent.</span></span>

**<span data-ttu-id="aa997-261">So konfigurieren Sie die e-Mail-Benachrichtigung für AGPM</span><span class="sxs-lookup"><span data-stu-id="aa997-261">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="aa997-262">Navigieren Sie im **Gruppenrichtlinien-Verwaltungs-Editor** zum Ordner **Change Control** .</span><span class="sxs-lookup"><span data-stu-id="aa997-262">In **Group Policy Management Editor** , navigate to the **Change Control** folder</span></span> 

2.  <span data-ttu-id="aa997-263">Klicken Sie im Detailbereich auf die Registerkarte **Domänendelegierung** .</span><span class="sxs-lookup"><span data-stu-id="aa997-263">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="aa997-264">Geben Sie im Feld **von e-Mail-Adresse** den e-Mail-Alias für AGPM ein, aus dem Benachrichtigungen gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="aa997-264">In the **From e-mail address** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="aa997-265">Geben Sie im Feld **an e-Mail-Adresse** die e-Mail-Adresse für das Benutzerkonto ein, dem Sie die genehmigende Rolle zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="aa997-265">In the **To e-mail address** field, type the e-mail address for the user account to which you intend to assign the Approver role.</span></span>

5.  <span data-ttu-id="aa997-266">Geben Sie im Feld **SMTP-Server** einen gültigen SMTP-e-Mail-Server ein.</span><span class="sxs-lookup"><span data-stu-id="aa997-266">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="aa997-267">Geben Sie in den Feldern **Benutzername** und **Kennwort** die Anmeldeinformationen eines Benutzers ein, der auf den SMTP-Dienst zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="aa997-267">In the **User name** and **Password** fields, type the credentials of a user who has access to the SMTP service.</span></span> <span data-ttu-id="aa997-268">Klicken Sie auf **Übernehmen**.</span><span class="sxs-lookup"><span data-stu-id="aa997-268">Click **Apply**.</span></span>

### <a href="" id="bkmk-config5"></a><span data-ttu-id="aa997-269">Schritt 5: Delegieren des Zugriffs</span><span class="sxs-lookup"><span data-stu-id="aa997-269">Step 5: Delegate access</span></span>

<span data-ttu-id="aa997-270">Als AGPM-Administrator (Vollzugriff) delegieren Sie den Zugriff auf Gruppenrichtlinienobjekte auf Domänenebene, wobei dem Konto jedes Gruppenrichtlinienadministrators Rollen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="aa997-270">As an AGPM Administrator (Full Control), you delegate domain-level access to GPOs, assigning roles to the account of each Group Policy administrator.</span></span>

<span data-ttu-id="aa997-271">**Hinweis**  Sie können den Zugriff auch auf der GPO-Ebene anstelle der Domänenebene delegieren.</span><span class="sxs-lookup"><span data-stu-id="aa997-271">**Note** You can also delegate access at the GPO level instead of the domain level.</span></span> <span data-ttu-id="aa997-272">Weitere Informationen finden Sie unter Hilfe zur erweiterten Gruppenrichtlinienverwaltung.</span><span class="sxs-lookup"><span data-stu-id="aa997-272">For more information, see Help for Advanced Group Policy Management.</span></span>

 

<span data-ttu-id="aa997-273">**Wichtig**  Sie sollten die Mitgliedschaft in der Gruppe der Gruppenrichtlinien Ersteller-Besitzer einschränken, damit Sie nicht dazu verwendet werden kann, die AGPM-Verwaltung des Zugriffs auf GPOs zu umgehen.</span><span class="sxs-lookup"><span data-stu-id="aa997-273">**Important** You should restrict membership in the Group Policy Creator Owners group so that it cannot be used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="aa997-274">(Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gruppenrichtlinienobjekte** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, klicken Sie auf **Delegierung**, und konfigurieren Sie dann die Einstellungen, um die Anforderungen Ihrer Organisation zu erfüllen.)</span><span class="sxs-lookup"><span data-stu-id="aa997-274">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

 

**<span data-ttu-id="aa997-275">So delegieren Sie den Zugriff auf alle GPOs in einer Domäne</span><span class="sxs-lookup"><span data-stu-id="aa997-275">To delegate access to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="aa997-276">Klicken Sie auf der Registerkarte **Domänendelegierung** auf die Schaltfläche **Hinzufügen** , wählen Sie das Benutzerkonto des Gruppenrichtlinienadministrators aus, das als genehmigende Person fungieren soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa997-276">On the **Domain Delegation** tab, click the **Add** button, select the user account of the Group Policy administrator to serve as Approver, and then click **OK**.</span></span>

2.  <span data-ttu-id="aa997-277">Wählen Sie im Dialogfeld **Gruppe oder Benutzer hinzufügen** die Rolle **genehmigende Person** aus, um diese Rolle dem Konto zuzuweisen, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa997-277">In the **Add Group or User** dialog box, select the **Approver** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="aa997-278">(Diese Rolle umfasst die Rolle Prüfer.)</span><span class="sxs-lookup"><span data-stu-id="aa997-278">(This role includes the Reviewer role.)</span></span>

3.  <span data-ttu-id="aa997-279">Klicken Sie auf die Schaltfläche **Hinzufügen** , wählen Sie das Benutzerkonto des Gruppenrichtlinienadministrators aus, das als Editor fungieren soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa997-279">Click the **Add** button, select the user account of the Group Policy administrator to serve as Editor, and then click **OK**.</span></span>

4.  <span data-ttu-id="aa997-280">Wählen Sie im Dialogfeld **Gruppe oder Benutzer hinzufügen** die **Editor** Rolle aus, um diese Rolle dem Konto zuzuweisen, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa997-280">In the **Add Group or User** dialog box, select the **Editor** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="aa997-281">(Diese Rolle umfasst die Rolle Prüfer.)</span><span class="sxs-lookup"><span data-stu-id="aa997-281">(This role includes the Reviewer role.)</span></span>

5.  <span data-ttu-id="aa997-282">Klicken Sie auf die Schaltfläche **Hinzufügen** , wählen Sie das Benutzerkonto des Gruppenrichtlinienadministrators aus, das als Bearbeiter fungieren soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa997-282">Click the **Add** button, select the user account of the Group Policy administrator to serve as Reviewer, and then click **OK**.</span></span>

6.  <span data-ttu-id="aa997-283">Wählen Sie im Dialogfeld **Gruppe oder Benutzer hinzufügen** die Rolle **Prüfer** aus, um dem Konto nur diese Rolle zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="aa997-283">In the **Add Group or User** dialog box, select the **Reviewer** role to assign only that role to the account.</span></span>

## <span data-ttu-id="aa997-284">Schritte zum Verwalten von GPOs</span><span class="sxs-lookup"><span data-stu-id="aa997-284">Steps for managing GPOs</span></span>


<span data-ttu-id="aa997-285">Sie müssen die folgenden Schritte ausführen, um GPOs mithilfe von AGPM zu erstellen, zu bearbeiten, zu überprüfen und bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="aa997-285">You must complete the following steps to create, edit, review, and deploy GPOs by using AGPM.</span></span> <span data-ttu-id="aa997-286">Darüber hinaus erstellen Sie eine Vorlage, löschen ein GPO und Wiederherstellen eines gelöschten Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="aa997-286">Additionally, you will create a template, delete a GPO, and restore a deleted GPO.</span></span>

[<span data-ttu-id="aa997-287">Schritt 1: Erstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="aa997-287">Step 1: Create a GPO</span></span>](#bkmk-manage1)

[<span data-ttu-id="aa997-288">Schritt 2: Bearbeiten eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="aa997-288">Step 2: Edit a GPO</span></span>](#bkmk-manage2)

[<span data-ttu-id="aa997-289">Schritt 3: überprüfen und Bereitstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="aa997-289">Step 3: Review and deploy a GPO</span></span>](#bkmk-manage3)

[<span data-ttu-id="aa997-290">Schritt 4: Verwenden einer Vorlage zum Erstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="aa997-290">Step 4: Use a template to create a GPO</span></span>](#bkmk-manage4)

[<span data-ttu-id="aa997-291">Schritt 5: Löschen und Wiederherstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="aa997-291">Step 5: Delete and restore a GPO</span></span>](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a><span data-ttu-id="aa997-292">Schritt 1: Erstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="aa997-292">Step 1: Create a GPO</span></span>

<span data-ttu-id="aa997-293">In einer Umgebung mit mehreren Gruppenrichtlinienadministratoren können Personen mit der Rolle des Editors anfordern, dass neue GPOs erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="aa997-293">In an environment that has multiple Group Policy administrators, those with the Editor role can request that new GPOs be created.</span></span> <span data-ttu-id="aa997-294">Diese Anforderung muss jedoch von einer Person mit der Rolle Genehmiger genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="aa997-294">However, that request must be approved by someone with the Approver role.</span></span>

<span data-ttu-id="aa997-295">In diesem Schritt verwenden Sie ein Konto mit der Rolle "Bearbeiter", um die Erstellung eines neuen Gruppenrichtlinienobjekts anzufordern.</span><span class="sxs-lookup"><span data-stu-id="aa997-295">In this step, you use an account that has the Editor role to request that a new GPO be created.</span></span> <span data-ttu-id="aa997-296">Wenn Sie ein Konto mit der Rolle genehmigende Person verwenden, genehmigen Sie diese Anforderung zum Erstellen des Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="aa997-296">Using an account that has the Approver role, you approve this request to create the GPO.</span></span>

**<span data-ttu-id="aa997-297">So fordern Sie die Erstellung und Verwaltung eines neuen Gruppenrichtlinienobjekts über AGPM an</span><span class="sxs-lookup"><span data-stu-id="aa997-297">To request that a new GPO be created and managed through AGPM</span></span>**

1.  <span data-ttu-id="aa997-298">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle des Editors in AGPM zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="aa997-298">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the Editor role in AGPM.</span></span>

2.  <span data-ttu-id="aa997-299">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="aa997-299">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="aa997-300">Klicken Sie mit der rechten Maustaste auf den Knoten **Change Control** , und klicken Sie dann auf **Neues gesteuertes Gruppenrichtlinienobjekt**.</span><span class="sxs-lookup"><span data-stu-id="aa997-300">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

4.  <span data-ttu-id="aa997-301">Im Dialogfeld " **Neues gesteuertes GPO** ":</span><span class="sxs-lookup"><span data-stu-id="aa997-301">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="aa997-302">Wenn Sie eine Kopie der Anfrage erhalten möchten, geben Sie Ihre e-Mail-Adresse in das Feld **CC** ein.</span><span class="sxs-lookup"><span data-stu-id="aa997-302">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="aa997-303">Geben Sie **eigenes** als Namen für das neue Gruppenrichtlinienobjekt ein.</span><span class="sxs-lookup"><span data-stu-id="aa997-303">Type **MyGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="aa997-304">Geben Sie einen Kommentar für das neue Gruppenrichtlinienobjekt ein.</span><span class="sxs-lookup"><span data-stu-id="aa997-304">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="aa997-305">Klicken Sie auf **Live erstellen** , damit das neue Gruppenrichtlinienobjekt unmittelbar nach der Genehmigung in der Produktionsumgebung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="aa997-305">Click **Create live** so that the new GPO will be deployed to the production environment immediately upon approval.</span></span> <span data-ttu-id="aa997-306">Klicken Sie auf **Übermitteln**.</span><span class="sxs-lookup"><span data-stu-id="aa997-306">Click **Submit**.</span></span>

5.  <span data-ttu-id="aa997-307">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="aa997-307">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="aa997-308">Das neue Gruppenrichtlinienobjekt wird auf der Registerkarte **Ausstehend** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aa997-308">The new GPO is displayed on the **Pending** tab.</span></span>

**<span data-ttu-id="aa997-309">So genehmigen Sie die ausstehende Anforderung zum Erstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="aa997-309">To approve the pending request to create a GPO</span></span>**

1.  <span data-ttu-id="aa997-310">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, das die Rolle der genehmigenden Person in AGPM hat.</span><span class="sxs-lookup"><span data-stu-id="aa997-310">On a computer on which you have installed AGPM Client, log on with a user account that has the role of Approver in AGPM.</span></span>

2.  <span data-ttu-id="aa997-311">Öffnen Sie den e-Mail-Posteingang für das Konto, und beachten Sie, dass Sie eine e-Mail-Nachricht vom AGPM-Alias mit der Anforderung des Editors zum Erstellen eines Gruppenrichtlinienobjekts erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="aa997-311">Open the e-mail inbox for the account, and notice that you have received an e-mail message from the AGPM alias with the Editor's request to create a GPO.</span></span>

3.  <span data-ttu-id="aa997-312">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="aa997-312">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="aa997-313">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **Ausstehend** , um die ausstehenden GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="aa997-313">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

5.  <span data-ttu-id="aa997-314">Klicken Sie mit der rechten Maustaste auf **eigenes**, und klicken Sie dann auf **genehmigen**.</span><span class="sxs-lookup"><span data-stu-id="aa997-314">Right-click **MyGPO**, and then click **Approve**.</span></span>

6.  <span data-ttu-id="aa997-315">Klicken Sie auf **Ja** , um die Genehmigung zu bestätigen und das Gruppenrichtlinienobjekt auf die Registerkarte **gesteuert** zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="aa997-315">Click **Yes** to confirm approval and move the GPO to the **Controlled** tab.</span></span>

### <a href="" id="bkmk-manage2"></a><span data-ttu-id="aa997-316">Schritt 2: Bearbeiten eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="aa997-316">Step 2: Edit a GPO</span></span>

<span data-ttu-id="aa997-317">Sie können GPOs verwenden, um Computer-oder Benutzereinstellungen zu konfigurieren und für viele Computer oder Benutzer bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="aa997-317">You can use GPOs to configure computer or user settings and deploy them to many computers or users.</span></span> <span data-ttu-id="aa997-318">In diesem Schritt verwenden Sie ein Konto mit der Rolle "Bearbeiter", um ein GPO aus dem Archiv auszuchecken, das Gruppenrichtlinienobjekt offline zu bearbeiten, das bearbeitete GPO in das Archiv zu überprüfen und die Bereitstellung des Gruppenrichtlinienobjekts in der Produktionsumgebung anzufordern.</span><span class="sxs-lookup"><span data-stu-id="aa997-318">In this step, you use an account that has the Editor role to check out a GPO from the archive, edit the GPO offline, check the edited GPO into the archive, and request deployment of the GPO to the production environment.</span></span> <span data-ttu-id="aa997-319">In diesem Szenario konfigurieren Sie eine Einstellung im Gruppenrichtlinienobjekt so, dass das Kennwort mindestens acht Zeichen lang sein muss.</span><span class="sxs-lookup"><span data-stu-id="aa997-319">For this scenario, you configure a setting in the GPO to require that the password be at least eight characters long.</span></span>

**<span data-ttu-id="aa997-320">So überprüfen Sie das Gruppenrichtlinienobjekt aus dem Archiv zur Bearbeitung</span><span class="sxs-lookup"><span data-stu-id="aa997-320">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="aa997-321">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, das die Rolle des Editors in AGPM hat.</span><span class="sxs-lookup"><span data-stu-id="aa997-321">On a computer on which you have installed AGPM Client, log on with a user account that has the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="aa997-322">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="aa997-322">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="aa997-323">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="aa997-323">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="aa997-324">Klicken Sie mit der rechten Maustaste auf **eigenes**, und klicken Sie dann auf **Auschecken**.</span><span class="sxs-lookup"><span data-stu-id="aa997-324">Right-click **MyGPO**, and then click **Check Out**.</span></span>

5.  <span data-ttu-id="aa997-325">Geben Sie einen Kommentar ein, der im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, während es ausgecheckt ist, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa997-325">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

6.  <span data-ttu-id="aa997-326">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="aa997-326">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="aa997-327">Auf der Registerkarte **gesteuert** wird der Status des Gruppenrichtlinienobjekts als **ausgecheckt**identifiziert.</span><span class="sxs-lookup"><span data-stu-id="aa997-327">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="aa997-328">So bearbeiten Sie das Gruppenrichtlinienobjekt offline und konfigurieren die minimale Kennwortlänge</span><span class="sxs-lookup"><span data-stu-id="aa997-328">To edit the GPO offline and configure the minimum password length</span></span>**

1.  <span data-ttu-id="aa997-329">Klicken Sie auf der Registerkarte **gesteuert** mit der rechten Maustaste auf **eigenes**, und klicken Sie dann auf **Bearbeiten** , um das Fenster **Gruppenrichtlinien-Verwaltungs-Editor** zu öffnen und eine Offlinekopie des Gruppenrichtlinienobjekts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="aa997-329">On the **Controlled** tab, right-click **MyGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and change an offline copy of the GPO.</span></span> <span data-ttu-id="aa997-330">Konfigurieren Sie in diesem Szenario die minimale Kennwortlänge:</span><span class="sxs-lookup"><span data-stu-id="aa997-330">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="aa997-331">Doppelklicken Sie unter **Computer Konfiguration**auf **Richtlinien**, **Windows-Einstellungen**, **Sicherheitseinstellungen**, **Kontorichtlinien**und **Kennwortrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="aa997-331">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Password Policy**.</span></span>

    2.  <span data-ttu-id="aa997-332">Doppelklicken Sie im Detailbereich auf **minimale Kennwortlänge**.</span><span class="sxs-lookup"><span data-stu-id="aa997-332">In the details pane, double-click **Minimum password length**.</span></span>

    3.  <span data-ttu-id="aa997-333">Aktivieren Sie im Eigenschaftenfenster das Kontrollkästchen **diese Richtlinieneinstellung definieren** , legen Sie die Anzahl der Zeichen auf **8**fest, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa997-333">In the properties window, select the **Define this policy setting** check box, set the number of characters to **8**, and then click **OK**.</span></span>

2.  <span data-ttu-id="aa997-334">Schließen Sie das Fenster **Gruppenrichtlinien-Verwaltungs-Editor** .</span><span class="sxs-lookup"><span data-stu-id="aa997-334">Close the **Group Policy Management Editor** window.</span></span>

**<span data-ttu-id="aa997-335">So überprüfen Sie das Gruppenrichtlinienobjekt in das Archiv</span><span class="sxs-lookup"><span data-stu-id="aa997-335">To check the GPO into the archive</span></span>**

1.  <span data-ttu-id="aa997-336">Klicken Sie auf der Registerkarte **gesteuert** mit der rechten Maustaste auf **eigenes** , und klicken Sie dann auf **Einchecken**.</span><span class="sxs-lookup"><span data-stu-id="aa997-336">On the **Controlled** tab, right-click **MyGPO** and then click **Check In**.</span></span>

2.  <span data-ttu-id="aa997-337">Geben Sie einen Kommentar ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa997-337">Type a comment, and then click **OK**.</span></span>

3.  <span data-ttu-id="aa997-338">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="aa997-338">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="aa997-339">Auf der Registerkarte **gesteuert** wird der Status des Gruppenrichtlinienobjekts als **eingecheckt**gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="aa997-339">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

**<span data-ttu-id="aa997-340">So fordern Sie die Bereitstellung des Gruppenrichtlinienobjekts in der Produktionsumgebung an</span><span class="sxs-lookup"><span data-stu-id="aa997-340">To request the deployment of the GPO to the production environment</span></span>**

1.  <span data-ttu-id="aa997-341">Klicken Sie auf der Registerkarte **gesteuert** mit der rechten Maustaste auf **eigenes** , und klicken Sie dann auf **Bereitstellen**.</span><span class="sxs-lookup"><span data-stu-id="aa997-341">On the **Controlled** tab, right-click **MyGPO** and then click **Deploy**.</span></span>

2.  <span data-ttu-id="aa997-342">Da es sich bei diesem Konto nicht um eine genehmigende Person oder einen AGPM-Administrator handelt, müssen Sie eine Anforderung für die Bereitstellung einreichen.</span><span class="sxs-lookup"><span data-stu-id="aa997-342">Because this account is not an Approver or AGPM Administrator, you must submit a request for deployment.</span></span> <span data-ttu-id="aa997-343">Wenn Sie eine Kopie der Anfrage erhalten möchten, geben Sie Ihre e-Mail-Adresse in das Feld **CC** ein.</span><span class="sxs-lookup"><span data-stu-id="aa997-343">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="aa997-344">Geben Sie einen Kommentar ein, der im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **Absenden**.</span><span class="sxs-lookup"><span data-stu-id="aa997-344">Type a comment to be displayed in the history of the GPO, and then click **Submit**.</span></span>

3.  <span data-ttu-id="aa997-345">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="aa997-345">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="aa997-346">**Eigenes** wird in der Liste der GPOs auf der Registerkarte **Ausstehend** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aa997-346">**MyGPO** is displayed on the list of GPOs on the **Pending** tab.</span></span>

### <a href="" id="bkmk-manage3"></a><span data-ttu-id="aa997-347">Schritt 3: überprüfen und Bereitstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="aa997-347">Step 3: Review and deploy a GPO</span></span>

<span data-ttu-id="aa997-348">In diesem Schritt fungieren Sie als genehmigende Person, erstellen Berichte und analysieren die Einstellungen und Änderungen an den Einstellungen im Gruppenrichtlinienobjekt, um festzustellen, ob Sie diese genehmigen sollten.</span><span class="sxs-lookup"><span data-stu-id="aa997-348">In this step, you act as an Approver, creating reports and analyzing the settings and changes to settings in the GPO to determine whether you should approve them.</span></span> <span data-ttu-id="aa997-349">Nachdem Sie das Gruppenrichtlinienobjekt ausgewertet haben, müssen Sie es in der Produktionsumgebung bereitstellen und das Gruppenrichtlinienobjekt mit einer Domäne oder einer Organisationseinheit verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="aa997-349">After you evaluate the GPO, you deploy it to the production environment and link the GPO to a domain or an organizational unit (OU).</span></span> <span data-ttu-id="aa997-350">Das Gruppenrichtlinienobjekt wird wirksam, wenn Gruppenrichtlinien für Computer in dieser Domäne oder OU aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="aa997-350">The GPO takes effect when Group Policy is refreshed for computers in that domain or OU.</span></span>

**<span data-ttu-id="aa997-351">So überprüfen Sie die Einstellungen im Gruppenrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="aa997-351">To review settings in the GPO</span></span>**

1. <span data-ttu-id="aa997-352">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle der genehmigenden Person in AGPM zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="aa997-352">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Approver in AGPM.</span></span> <span data-ttu-id="aa997-353">Jeder Gruppenrichtlinienadministrator mit der Rolle Prüfer, die in allen anderen Rollen enthalten ist, kann die Einstellungen in einem Gruppenrichtlinienobjekt überprüfen.</span><span class="sxs-lookup"><span data-stu-id="aa997-353">Any Group Policy administrator with the Reviewer role, which is included in all of the other roles, can review the settings in a GPO.</span></span>

2. <span data-ttu-id="aa997-354">Öffnen Sie den e-Mail-Posteingang für das Konto, und beachten Sie, dass Sie eine e-Mail-Nachricht vom AGPM-Alias mit der Anforderung eines Editors zum Bereitstellen eines Gruppenrichtlinienobjekts erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="aa997-354">Open the e-mail inbox for the account and notice that you have received an e-mail message from the AGPM alias with an Editor's request to deploy a GPO.</span></span>

3. <span data-ttu-id="aa997-355">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="aa997-355">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4. <span data-ttu-id="aa997-356">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **Ausstehend** .</span><span class="sxs-lookup"><span data-stu-id="aa997-356">On the **Contents** tab in the details pane, click the **Pending** tab.</span></span>

5. <span data-ttu-id="aa997-357">Doppelklicken Sie auf **eigenes** , um dessen Verlauf anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="aa997-357">Double-click **MyGPO** to display its history.</span></span>

6. <span data-ttu-id="aa997-358">Überprüfen Sie die Einstellungen in der neuesten Version von eigenes:</span><span class="sxs-lookup"><span data-stu-id="aa997-358">Review the settings in the most recent version of MyGPO:</span></span>

   1.  <span data-ttu-id="aa997-359">Klicken Sie im **Verlaufs** Fenster mit der rechten Maustaste auf die GPO-Version mit dem letzten Zeitstempel, klicken Sie auf **Einstellungen**, und klicken Sie dann auf **HTML-Bericht** , um eine Zusammenfassung der Einstellungen des Gruppenrichtlinienobjekts anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="aa997-359">In the **History** window, right-click the GPO version with the most recent time stamp, click **Settings**, and then click **HTML Report** to display a summary of the GPO's settings.</span></span>

   2.  <span data-ttu-id="aa997-360">Klicken Sie im Webbrowser auf **Alle anzeigen** , um alle Einstellungen im Gruppenrichtlinienobjekt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="aa997-360">In the Web browser, click **show all** to display all the settings in the GPO.</span></span> <span data-ttu-id="aa997-361">Schließen Sie den Browser.</span><span class="sxs-lookup"><span data-stu-id="aa997-361">Close the browser.</span></span>

7. <span data-ttu-id="aa997-362">Vergleichen Sie die neueste Version von eigenes mit der ersten Version, die in das Archiv eingecheckt wurde:</span><span class="sxs-lookup"><span data-stu-id="aa997-362">Compare the most recent version of MyGPO to the first version checked in to the archive:</span></span>

   1. <span data-ttu-id="aa997-363">Klicken Sie im Fenster " **Verlauf** " auf die GPO-Version mit dem letzten Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="aa997-363">In the **History** window, click the GPO version with the most recent time stamp.</span></span> <span data-ttu-id="aa997-364">Drücken Sie STRG, und klicken Sie dann auf die älteste GPO-Version, für die die **Computer Version** nicht \* \* \ \ \* \* \* ist.</span><span class="sxs-lookup"><span data-stu-id="aa997-364">Press CTRL and then click the oldest GPO version for which the **Computer Version** is not \*\*\\*\*\*.</span></span>

   2. <span data-ttu-id="aa997-365">Klicken Sie auf die Schaltfläche **Unterschiede** .</span><span class="sxs-lookup"><span data-stu-id="aa997-365">Click the **Differences** button.</span></span> <span data-ttu-id="aa997-366">Der Abschnitt **Kontorichtlinien/Kennwortrichtlinie** ist grün hervorgehoben und wird mit **\ [+ \]** vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="aa997-366">The **Account Policies/Password Policy** section is highlighted in green and preceded by **\[+\]**.</span></span> <span data-ttu-id="aa997-367">Dies zeigt an, dass die Einstellung nur in der letzten Version des Gruppenrichtlinienobjekts konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="aa997-367">This indicates that the setting is configured only in the latter version of the GPO.</span></span>

   3. <span data-ttu-id="aa997-368">Klicken Sie auf **Kontorichtlinien/Kennwortrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="aa997-368">Click **Account Policies/Password Policy**.</span></span> <span data-ttu-id="aa997-369">Die Einstellung **minimale Kennwortlänge** ist auch in grün hervorgehoben und mit **\ [+ \]** gekennzeichnet, was darauf hinweist, dass Sie nur in der letzten Version des Gruppenrichtlinienobjekts konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="aa997-369">The **Minimum password length** setting is also highlighted in green and preceded by **\[+\]**, indicating that it is configured only in the latter version of the GPO.</span></span>

   4. <span data-ttu-id="aa997-370">Schließen Sie den Webbrowser.</span><span class="sxs-lookup"><span data-stu-id="aa997-370">Close the Web browser.</span></span>

**<span data-ttu-id="aa997-371">So stellen Sie das Gruppenrichtlinienobjekt in der Produktionsumgebung bereit</span><span class="sxs-lookup"><span data-stu-id="aa997-371">To deploy the GPO to the production environment</span></span>**

1.  <span data-ttu-id="aa997-372">Klicken Sie auf der Registerkarte **Ausstehend** mit der rechten Maustaste auf **eigenes** , und klicken Sie dann auf **genehmigen**.</span><span class="sxs-lookup"><span data-stu-id="aa997-372">On the **Pending** tab, right-click **MyGPO** and then click **Approve**.</span></span>

2.  <span data-ttu-id="aa997-373">Geben Sie einen Kommentar ein, der in das Protokoll des Gruppenrichtlinienobjekts aufgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa997-373">Type a comment to include in the history of the GPO.</span></span>

3.  <span data-ttu-id="aa997-374">Klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="aa997-374">Click **Yes**.</span></span> <span data-ttu-id="aa997-375">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="aa997-375">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="aa997-376">Das Gruppenrichtlinienobjekt wird in der Produktionsumgebung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="aa997-376">The GPO is deployed to the production environment.</span></span>

**<span data-ttu-id="aa997-377">So verknüpfen Sie das Gruppenrichtlinienobjekt mit einer Domäne oder Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="aa997-377">To link the GPO to a domain or organizational unit</span></span>**

1.  <span data-ttu-id="aa997-378">Klicken Sie in der GPMC mit der rechten Maustaste entweder auf die Domäne oder auf eine Organisationseinheit, auf die Sie das konfigurierte Gruppenrichtlinienobjekt anwenden möchten, und klicken Sie dann auf **vorhandenes Gruppenrichtlinienobjekt verknüpfen**.</span><span class="sxs-lookup"><span data-stu-id="aa997-378">In the GPMC, right-click either the domain or an organizational unit (OU) to which you want to apply the GPO that you configured, and then click **Link an Existing GPO**.</span></span>

2.  <span data-ttu-id="aa997-379">Klicken Sie im Dialogfeld **GPO auswählen** auf **eigenes**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa997-379">In the **Select GPO** dialog box, click **MyGPO**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage4"></a><span data-ttu-id="aa997-380">Schritt 4: Verwenden einer Vorlage zum Erstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="aa997-380">Step 4: Use a template to create a GPO</span></span>

<span data-ttu-id="aa997-381">In diesem Schritt verwenden Sie ein Konto, das über die Rolle des Editors verfügt, um eine Vorlage zu erstellen und zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="aa997-381">In this step, you use an account that has the Editor role to create and use a template.</span></span> <span data-ttu-id="aa997-382">Bei dieser Vorlage handelt es sich um eine statische Version eines GPO, die als Ausgangspunkt zum Erstellen neuer GPOs verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="aa997-382">That template is a static version of a GPO for use as a starting point for creating new GPOs.</span></span> <span data-ttu-id="aa997-383">Obwohl Sie eine Vorlage nicht bearbeiten können, können Sie ein neues Gruppenrichtlinienobjekt basierend auf einer Vorlage erstellen.</span><span class="sxs-lookup"><span data-stu-id="aa997-383">Although you cannot edit a template, you can create a new GPO based on a template.</span></span> <span data-ttu-id="aa997-384">Vorlagen sind hilfreich für das schnelle Erstellen mehrerer GPOs, in denen viele der gleichen Richtlinieneinstellungen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="aa997-384">Templates are useful for quickly creating multiple GPOs that include many of the same policy settings.</span></span>

**<span data-ttu-id="aa997-385">So erstellen Sie eine Vorlage auf der Grundlage eines vorhandenen Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="aa997-385">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="aa997-386">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle des Editors in AGPM zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="aa997-386">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="aa997-387">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="aa997-387">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="aa997-388">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** .</span><span class="sxs-lookup"><span data-stu-id="aa997-388">On the **Contents** tab in the details pane, click the **Controlled** tab.</span></span>

4.  <span data-ttu-id="aa997-389">Klicken Sie mit der rechten Maustaste auf **eigenes**, und klicken Sie dann auf **als Vorlage speichern** , um eine Vorlage zu erstellen, die alle Einstellungen umfasst, die derzeit in eigenes enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="aa997-389">Right-click **MyGPO**, and then click **Save as Template** to create a template incorporating all settings currently in MyGPO.</span></span>

5.  <span data-ttu-id="aa997-390">Geben Sie **MyTemplate** als Namen für die Vorlage und einen Kommentar ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa997-390">Type **MyTemplate** as the name for the template and a comment, and then click **OK**.</span></span>

6.  <span data-ttu-id="aa997-391">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="aa997-391">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="aa997-392">Die neue Vorlage wird auf der Registerkarte **Vorlagen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aa997-392">The new template appears on the **Templates** tab.</span></span>

**<span data-ttu-id="aa997-393">So fordern Sie die Erstellung und Verwaltung eines neuen Gruppenrichtlinienobjekts über AGPM an</span><span class="sxs-lookup"><span data-stu-id="aa997-393">To request that a new GPO be created and managed through AGPM</span></span>**

1.  <span data-ttu-id="aa997-394">Klicken Sie auf die Registerkarte **gesteuert** .</span><span class="sxs-lookup"><span data-stu-id="aa997-394">Click the **Controlled** tab.</span></span>

2.  <span data-ttu-id="aa997-395">Klicken Sie mit der rechten Maustaste auf den Knoten **Change Control** , und klicken Sie dann auf **Neues gesteuertes Gruppenrichtlinienobjekt**.</span><span class="sxs-lookup"><span data-stu-id="aa997-395">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="aa997-396">Im Dialogfeld " **Neues gesteuertes GPO** ":</span><span class="sxs-lookup"><span data-stu-id="aa997-396">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="aa997-397">Wenn Sie eine Kopie der Anfrage erhalten möchten, geben Sie Ihre e-Mail-Adresse in das Feld **CC** ein.</span><span class="sxs-lookup"><span data-stu-id="aa997-397">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="aa997-398">Geben Sie **Gruppenrichtlinienverwaltungs** als Namen für das neue Gruppenrichtlinienobjekt ein.</span><span class="sxs-lookup"><span data-stu-id="aa997-398">Type **MyOtherGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="aa997-399">Geben Sie einen Kommentar für das neue Gruppenrichtlinienobjekt ein.</span><span class="sxs-lookup"><span data-stu-id="aa997-399">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="aa997-400">Klicken Sie auf **Live erstellen** , damit das neue Gruppenrichtlinienobjekt unmittelbar nach der Genehmigung in der Produktionsumgebung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="aa997-400">Click **Create live** so that the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="aa997-401">Wählen Sie für **aus GPO-Vorlage**die Option meine **Vorlage**aus.</span><span class="sxs-lookup"><span data-stu-id="aa997-401">For **From GPO template**, select **MyTemplate**.</span></span> <span data-ttu-id="aa997-402">Klicken Sie auf **Übermitteln**.</span><span class="sxs-lookup"><span data-stu-id="aa997-402">Click **Submit**.</span></span>

4.  <span data-ttu-id="aa997-403">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="aa997-403">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="aa997-404">Das neue Gruppenrichtlinienobjekt wird auf der Registerkarte **Ausstehend** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aa997-404">The new GPO is displayed on the **Pending** tab.</span></span>

<span data-ttu-id="aa997-405">Verwenden Sie ein Konto, dem die Rolle der genehmigenden Person zugewiesen ist, um die ausstehende Anforderung zum Erstellen des Gruppenrichtlinienobjekts zu genehmigen, wie in [Schritt 1: Erstellen eines Gruppenrichtlinienobjekts](#bkmk-manage1).</span><span class="sxs-lookup"><span data-stu-id="aa997-405">Use an account that is assigned the role of Approver to approve the pending request to create the GPO as you did in [Step 1: Create a GPO](#bkmk-manage1).</span></span> <span data-ttu-id="aa997-406">MyTemplate enthält alle Einstellungen, die Sie in eigenes konfiguriert haben.</span><span class="sxs-lookup"><span data-stu-id="aa997-406">MyTemplate incorporates all the settings that you configured in MyGPO.</span></span> <span data-ttu-id="aa997-407">Da Gruppenrichtlinienverwaltungs mit MyTemplate erstellt wurde, enthält es zunächst alle Einstellungen, die eigenes zum Zeitpunkt der Erstellung von MyTemplate enthielt.</span><span class="sxs-lookup"><span data-stu-id="aa997-407">Because MyOtherGPO was created using MyTemplate, it at first contains all the settings that MyGPO contained at the time that MyTemplate was created.</span></span> <span data-ttu-id="aa997-408">Sie können dies bestätigen, indem Sie einen Differenz Bericht generieren, um Gruppenrichtlinienverwaltungs mit MyTemplate zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="aa997-408">You can confirm this by generating a difference report to compare MyOtherGPO to MyTemplate.</span></span>

**<span data-ttu-id="aa997-409">So überprüfen Sie das Gruppenrichtlinienobjekt aus dem Archiv zur Bearbeitung</span><span class="sxs-lookup"><span data-stu-id="aa997-409">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="aa997-410">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle des Editors in AGPM zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="aa997-410">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="aa997-411">Klicken Sie mit der rechten Maustaste auf **Gruppenrichtlinienverwaltungs**, und klicken Sie dann auf **Auschecken**.</span><span class="sxs-lookup"><span data-stu-id="aa997-411">Right-click **MyOtherGPO**, and then click **Check Out**.</span></span>

3.  <span data-ttu-id="aa997-412">Geben Sie einen Kommentar ein, der im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, während es ausgecheckt ist, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa997-412">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

4.  <span data-ttu-id="aa997-413">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="aa997-413">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="aa997-414">Auf der Registerkarte **gesteuert** wird der Status des Gruppenrichtlinienobjekts als **ausgecheckt**identifiziert.</span><span class="sxs-lookup"><span data-stu-id="aa997-414">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="aa997-415">So bearbeiten Sie das Gruppenrichtlinienobjekt offline und konfigurieren die Kontosperrungsdauer</span><span class="sxs-lookup"><span data-stu-id="aa997-415">To edit the GPO offline and configure the account lockout duration</span></span>**

1.  <span data-ttu-id="aa997-416">Klicken Sie auf der Registerkarte **gesteuert** mit der rechten Maustaste auf **Gruppenrichtlinienverwaltungs**, und klicken Sie dann auf **Bearbeiten** , um das Fenster **Gruppenrichtlinien-Verwaltungs-Editor** zu öffnen und eine Offlinekopie des Gruppenrichtlinienobjekts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="aa997-416">On the **Controlled** tab, right-click **MyOtherGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and change an offline copy of the GPO.</span></span> <span data-ttu-id="aa997-417">Konfigurieren Sie in diesem Szenario die minimale Kennwortlänge:</span><span class="sxs-lookup"><span data-stu-id="aa997-417">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="aa997-418">Doppelklicken Sie unter **Computer Konfiguration**auf **Richtlinien**, **Windows-Einstellungen**, **Sicherheitseinstellungen**, **Kontorichtlinien**und **Kontosperrungsrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="aa997-418">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Account Lockout Policy**.</span></span>

    2.  <span data-ttu-id="aa997-419">Doppelklicken Sie im Detailbereich auf **Kontosperrungsdauer**.</span><span class="sxs-lookup"><span data-stu-id="aa997-419">In the details pane, double-click **Account lockout duration**.</span></span>

    3.  <span data-ttu-id="aa997-420">Aktivieren Sie im Fenster Eigenschaften die Option **diese Richtlinieneinstellung definieren**, legen Sie die Dauer auf **30** Minuten fest, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa997-420">In the properties window, check **Define this policy setting**, set the duration to **30** minutes, and then click **OK**.</span></span>

2.  <span data-ttu-id="aa997-421">Schließen Sie das Fenster **Gruppenrichtlinien-Verwaltungs-Editor** .</span><span class="sxs-lookup"><span data-stu-id="aa997-421">Close the **Group Policy Management Editor** window.</span></span>

<span data-ttu-id="aa997-422">Überprüfen Sie Gruppenrichtlinienverwaltungs in die Archivierungs-und Anforderungs Bereitstellung wie bei eigenes in [Schritt 2: Bearbeiten eines Gruppenrichtlinienobjekts](#bkmk-manage2).</span><span class="sxs-lookup"><span data-stu-id="aa997-422">Check MyOtherGPO into the archive and request deployment as you did for MyGPO in [Step 2: Edit a GPO](#bkmk-manage2).</span></span> <span data-ttu-id="aa997-423">Sie können Gruppenrichtlinienverwaltungs mit eigenes oder mit MyTemplate vergleichen, indem Sie Differenz Berichte verwenden.</span><span class="sxs-lookup"><span data-stu-id="aa997-423">You can compare MyOtherGPO to MyGPO or to MyTemplate by using difference reports.</span></span> <span data-ttu-id="aa997-424">Jedes Konto, das die Rolle Prüfer enthält (AGPM-Administrator \ [Vollzugriff \], genehmigende Person, Bearbeiter oder Bearbeiter) kann Berichte generieren.</span><span class="sxs-lookup"><span data-stu-id="aa997-424">Any account that includes the Reviewer role (AGPM Administrator \[Full Control\], Approver, Editor, or Reviewer) can generate reports.</span></span>

**<span data-ttu-id="aa997-425">So vergleichen Sie ein GPO mit einem anderen Gruppenrichtlinienobjekt und einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="aa997-425">To compare a GPO to another GPO and to a template</span></span>**

1.  <span data-ttu-id="aa997-426">So vergleichen Sie eigenes und Gruppenrichtlinienverwaltungs:</span><span class="sxs-lookup"><span data-stu-id="aa997-426">To compare MyGPO and MyOtherGPO:</span></span>

    1.  <span data-ttu-id="aa997-427">Klicken Sie auf der Registerkarte **gesteuert** auf **eigenes**.</span><span class="sxs-lookup"><span data-stu-id="aa997-427">On the **Controlled** tab, click **MyGPO**.</span></span> <span data-ttu-id="aa997-428">Drücken Sie STRG, und klicken Sie dann auf **Gruppenrichtlinienverwaltungs**.</span><span class="sxs-lookup"><span data-stu-id="aa997-428">Press CTRL and then click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="aa997-429">Klicken Sie mit der rechten Maustaste auf **Gruppenrichtlinienverwaltungs**, zeigen Sie auf **Unterschiede**, und klicken Sie dann auf **HTML-Bericht**.</span><span class="sxs-lookup"><span data-stu-id="aa997-429">Right-click **MyOtherGPO**, point to **Differences**, and then click **HTML Report**.</span></span>

2.  <span data-ttu-id="aa997-430">So vergleichen Sie Gruppenrichtlinienverwaltungs und MyTemplate:</span><span class="sxs-lookup"><span data-stu-id="aa997-430">To compare MyOtherGPO and MyTemplate:</span></span>

    1.  <span data-ttu-id="aa997-431">Klicken Sie auf der Registerkarte **gesteuert** auf **Gruppenrichtlinienverwaltungs**.</span><span class="sxs-lookup"><span data-stu-id="aa997-431">On the **Controlled** tab, click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="aa997-432">Klicken Sie mit der rechten Maustaste auf **Gruppenrichtlinienverwaltungs**, zeigen Sie auf **Unterschiede**, und klicken Sie dann auf **Vorlage**.</span><span class="sxs-lookup"><span data-stu-id="aa997-432">Right-click **MyOtherGPO**, point to **Differences**, and then click **Template**.</span></span>

    3.  <span data-ttu-id="aa997-433">Wählen Sie **MyTemplate** und **HTML-Bericht**aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa997-433">Select **MyTemplate** and **HTML Report**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage5"></a><span data-ttu-id="aa997-434">Schritt 5: Löschen und Wiederherstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="aa997-434">Step 5: Delete and restore a GPO</span></span>

<span data-ttu-id="aa997-435">In diesem Schritt fungieren Sie als genehmigende Person, um ein GPO zu löschen.</span><span class="sxs-lookup"><span data-stu-id="aa997-435">In this step, you act as an Approver to delete a GPO.</span></span>

**<span data-ttu-id="aa997-436">So löschen Sie ein Gruppenrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="aa997-436">To delete a GPO</span></span>**

1.  <span data-ttu-id="aa997-437">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle der genehmigenden Person zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="aa997-437">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Approver.</span></span>

2.  <span data-ttu-id="aa997-438">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="aa997-438">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="aa997-439">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="aa997-439">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="aa997-440">Klicken Sie mit der rechten Maustaste auf **eigenes**, und klicken Sie dann auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="aa997-440">Right-click **MyGPO**, and then click **Delete**.</span></span> <span data-ttu-id="aa997-441">Klicken Sie auf **Gruppenrichtlinienobjekt aus Archiv und Produktion löschen** , um sowohl die Version im Archiv als auch die bereitgestellte Version des Gruppenrichtlinienobjekts in der Produktionsumgebung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="aa997-441">Click **Delete GPO from archive and production** to delete both the version in the archive and the deployed version of the GPO in the production environment.</span></span>

5.  <span data-ttu-id="aa997-442">Geben Sie einen Kommentar ein, der im Überwachungspfad für das Gruppenrichtlinienobjekt angezeigt werden soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa997-442">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

6.  <span data-ttu-id="aa997-443">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="aa997-443">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="aa997-444">Das Gruppenrichtlinienobjekt wird von der Registerkarte " **gesteuert** " entfernt und auf der Registerkarte " **Papierkorb** " angezeigt, wo es wiederhergestellt oder gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="aa997-444">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

<span data-ttu-id="aa997-445">Gelegentlich können Sie feststellen, dass Sie nach dem Löschen eines Gruppenrichtlinienobjekts nach wie vor benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="aa997-445">Occasionally you may discover after you delete a GPO that it is still needed.</span></span> <span data-ttu-id="aa997-446">In diesem Schritt fungieren Sie als genehmigende Person zum Wiederherstellen eines gelöschten Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="aa997-446">In this step, you act as an Approver to restore a GPO that was deleted.</span></span>

**<span data-ttu-id="aa997-447">So stellen Sie ein gelöschtes Gruppenrichtlinienobjekt wieder her</span><span class="sxs-lookup"><span data-stu-id="aa997-447">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="aa997-448">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **Papierkorb** , um gelöschte GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="aa997-448">On the **Contents** tab, click the **Recycle Bin** tab to display deleted GPOs.</span></span>

2.  <span data-ttu-id="aa997-449">Klicken Sie mit der rechten Maustaste auf **eigenes**, und klicken Sie dann auf **Wiederherstellen**.</span><span class="sxs-lookup"><span data-stu-id="aa997-449">Right-click **MyGPO**, and then click **Restore**.</span></span>

3.  <span data-ttu-id="aa997-450">Geben Sie einen Kommentar ein, der im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa997-450">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="aa997-451">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="aa997-451">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="aa997-452">Das Gruppenrichtlinienobjekt wird von der Registerkarte " **Papierkorb** " entfernt und auf der Registerkarte " **gesteuert** " angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aa997-452">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

    <span data-ttu-id="aa997-453">**Hinweis**  Wenn Sie ein GPO im Archiv wiederherstellen, wird es nicht automatisch in der Produktionsumgebung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="aa997-453">**Note** Restoring a GPO to the archive does not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="aa997-454">Wenn Sie das Gruppenrichtlinienobjekt an die Produktionsumgebung zurückgeben möchten, stellen Sie das Gruppenrichtlinienobjekt wie in [Schritt 3: überprüfen und Bereitstellen eines Gruppenrichtlinien](#bkmk-manage3)Objekts bereit.</span><span class="sxs-lookup"><span data-stu-id="aa997-454">To return the GPO to the production environment, deploy the GPO as in [Step 3: Review and deploy a GPO](#bkmk-manage3).</span></span>

     

<span data-ttu-id="aa997-455">Nachdem Sie ein GPO bearbeitet und bereitgestellt haben, stellen Sie möglicherweise fest, dass die letzten Änderungen am Gruppenrichtlinienobjekt ein Problem verursachen.</span><span class="sxs-lookup"><span data-stu-id="aa997-455">After editing and deploying a GPO, you may discover that recent changes to the GPO are causing a problem.</span></span> <span data-ttu-id="aa997-456">In diesem Schritt fungieren Sie als genehmigende Person, um einen Rollback zu einer früheren Version des Gruppenrichtlinienobjekts durchführen zu können.</span><span class="sxs-lookup"><span data-stu-id="aa997-456">In this step, you act as an Approver to roll back to an earlier version of the GPO.</span></span> <span data-ttu-id="aa997-457">Sie können einen Rollback zu einer beliebigen Version im Verlauf des Gruppenrichtlinienobjekts ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa997-457">You can roll back to any version in the history of the GPO.</span></span> <span data-ttu-id="aa997-458">Sie können Kommentare und Beschriftungen verwenden, um bekannte gute Versionen zu identifizieren und wenn bestimmte Änderungen vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="aa997-458">You can use comments and labels to identify known good versions and when specific changes were made.</span></span>

**<span data-ttu-id="aa997-459">So führen Sie einen Rollback zu einer früheren Version eines GPO durch</span><span class="sxs-lookup"><span data-stu-id="aa997-459">To roll back to an earlier version of a GPO</span></span>**

1.  <span data-ttu-id="aa997-460">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="aa997-460">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

2.  <span data-ttu-id="aa997-461">Doppelklicken Sie auf **eigenes** , um dessen Verlauf anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="aa997-461">Double-click **MyGPO** to display its history.</span></span>

3.  <span data-ttu-id="aa997-462">Klicken Sie mit der rechten Maustaste auf die bereit **zustellende**Version, klicken Sie auf bereitstellen, und klicken Sie dann auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="aa997-462">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

4.  <span data-ttu-id="aa997-463">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="aa997-463">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="aa997-464">Klicken Sie im Fenster **Verlauf** auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="aa997-464">In the **History** window, click **Close**.</span></span>

    <span data-ttu-id="aa997-465">**Hinweis**  Um zu überprüfen, ob die Version, die erneut bereitgestellt wurde, die beabsichtigte Version ist, untersuchen Sie einen Unterschiedsbericht für die beiden Versionen.</span><span class="sxs-lookup"><span data-stu-id="aa997-465">**Note** To verify that the version that was redeployed is the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="aa997-466">Wählen Sie im Fenster **Verlauf** für das Gruppenrichtlinienobjekt die beiden Versionen aus, klicken Sie mit der rechten Maustaste darauf, zeigen Sie auf **Differenz**, und klicken Sie dann auf **HTML-Bericht** oder **XML-Bericht**.</span><span class="sxs-lookup"><span data-stu-id="aa997-466">In the **History** window for the GPO, select the two versions, right-click them, point to **Difference**, and then click either **HTML Report** or **XML Report**.</span></span>

     

 

 





