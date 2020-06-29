---
title: So verwalten Sie App-V 5.0-Pakete auf einem eigenständigen Computer mithilfe von PowerShell
description: So verwalten Sie App-V 5.0-Pakete auf einem eigenständigen Computer mithilfe von PowerShell
author: dansimp
ms.assetid: 1d6c2d25-81ec-4ff8-9262-6b4cf484a376
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b7af1781a7a443a4fcfc8e7d4a92525b34986763
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805339"
---
# <span data-ttu-id="b5821-103">So verwalten Sie App-V 5.0-Pakete auf einem eigenständigen Computer mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="b5821-103">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span>


<span data-ttu-id="b5821-104">In den folgenden Abschnitten wird erläutert, wie verschiedene Verwaltungsaufgaben auf einem eigenständigen Clientcomputer mithilfe von PowerShell durchgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="b5821-104">The following sections explain how to perform various management tasks on a stand-alone client computer by using PowerShell:</span></span>

-   [<span data-ttu-id="b5821-105">So geben Sie eine Liste der Pakete zurück</span><span class="sxs-lookup"><span data-stu-id="b5821-105">To return a list of packages</span></span>](#bkmk-return-pkgs-standalone-posh)

-   [<span data-ttu-id="b5821-106">So fügen Sie ein Paket hinzu</span><span class="sxs-lookup"><span data-stu-id="b5821-106">To add a package</span></span>](#bkmk-add-pkgs-standalone-posh)

-   [<span data-ttu-id="b5821-107">So veröffentlichen Sie ein Paket</span><span class="sxs-lookup"><span data-stu-id="b5821-107">To publish a package</span></span>](#bkmk-pub-pkg-standalone-posh)

-   [<span data-ttu-id="b5821-108">So veröffentlichen Sie ein Paket für einen bestimmten Benutzer</span><span class="sxs-lookup"><span data-stu-id="b5821-108">To publish a package to a specific user</span></span>](#bkmk-pub-pkg-a-user-standalone-posh)

-   [<span data-ttu-id="b5821-109">So fügen Sie ein Paket hinzu und veröffentlichen es</span><span class="sxs-lookup"><span data-stu-id="b5821-109">To add and publish a package</span></span>](#bkmk-add-pub-pkg-standalone-posh)

-   [<span data-ttu-id="b5821-110">So heben Sie die Veröffentlichung eines vorhandenen Pakets auf</span><span class="sxs-lookup"><span data-stu-id="b5821-110">To unpublish an existing package</span></span>](#bkmk-unpub-pkg-standalone-posh)

-   [<span data-ttu-id="b5821-111">So heben Sie die Veröffentlichung eines Pakets für einen bestimmten Benutzer auf</span><span class="sxs-lookup"><span data-stu-id="b5821-111">To unpublish a package for a specific user</span></span>](#bkmk-unpub-pkg-specfc-use)

-   [<span data-ttu-id="b5821-112">So entfernen Sie ein vorhandenes Paket</span><span class="sxs-lookup"><span data-stu-id="b5821-112">To remove an existing package</span></span>](#bkmk-remove-pkg-standalone-posh)

-   [<span data-ttu-id="b5821-113">So aktivieren Sie nur Administratoren zum Veröffentlichen oder Aufheben der Veröffentlichung von Paketen</span><span class="sxs-lookup"><span data-stu-id="b5821-113">To enable only administrators to publish or unpublish packages</span></span>](#bkmk-admins-pub-pkgs)

-   [<span data-ttu-id="b5821-114">Grundlegendes zu ausstehenden Paketen (UserPending und GlobalPending)</span><span class="sxs-lookup"><span data-stu-id="b5821-114">Understanding pending packages (UserPending and GlobalPending)</span></span>](#bkmk-understd-pend-pkgs)

## <a href="" id="bkmk-return-pkgs-standalone-posh"></a><span data-ttu-id="b5821-115">So geben Sie eine Liste der Pakete zurück</span><span class="sxs-lookup"><span data-stu-id="b5821-115">To return a list of packages</span></span>


<span data-ttu-id="b5821-116">Verwenden Sie die folgenden Informationen, um eine Liste der Pakete zurückzugeben, die für einen bestimmten Benutzer berechtigt sind:</span><span class="sxs-lookup"><span data-stu-id="b5821-116">Use the following information to return a list of packages that are entitled to a specific user:</span></span>

<span data-ttu-id="b5821-117">**Cmdlet**: Get-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="b5821-117">**Cmdlet**: Get-AppvClientPackage</span></span>

<span data-ttu-id="b5821-118">**Parameter**:-Name-Version-Package-Version-Version-Nr.</span><span class="sxs-lookup"><span data-stu-id="b5821-118">**Parameters**: -Name -Version -PackageID -VersionID</span></span>

<span data-ttu-id="b5821-119">**Beispiel**: Get-AppvClientPackage – Name "ContosoApplication" – Version 2</span><span class="sxs-lookup"><span data-stu-id="b5821-119">**Example**: Get-AppvClientPackage –Name “ContosoApplication” -Version 2</span></span>

## <a href="" id="bkmk-add-pkgs-standalone-posh"></a><span data-ttu-id="b5821-120">So fügen Sie ein Paket hinzu</span><span class="sxs-lookup"><span data-stu-id="b5821-120">To add a package</span></span>


<span data-ttu-id="b5821-121">Verwenden Sie die folgenden Informationen, um einem Computer ein Paket hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b5821-121">Use the following information to add a package to a computer.</span></span>

<span data-ttu-id="b5821-122">**Wichtig**  In diesem Beispiel wird nur ein Paket hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b5821-122">**Important** This example only adds a package.</span></span> <span data-ttu-id="b5821-123">Das Paket wird nicht für den Benutzer oder den Computer veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="b5821-123">It does not publish the package to the user or the computer.</span></span>

 

<span data-ttu-id="b5821-124">**Cmdlet**: Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="b5821-124">**Cmdlet**: Add-AppvClientPackage</span></span>

<span data-ttu-id="b5821-125">**Beispiel**: $contoso = Add-AppvClientPackage \\\\path\\to\\appv\\package.AppV</span><span class="sxs-lookup"><span data-stu-id="b5821-125">**Example**: $Contoso = Add-AppvClientPackage \\\\path\\to\\appv\\package.appv</span></span>

## <a href="" id="bkmk-pub-pkg-standalone-posh"></a><span data-ttu-id="b5821-126">So veröffentlichen Sie ein Paket</span><span class="sxs-lookup"><span data-stu-id="b5821-126">To publish a package</span></span>


<span data-ttu-id="b5821-127">Verwenden Sie die folgenden Informationen, um ein Paket zu veröffentlichen, das einem bestimmten Benutzer oder Global einem beliebigen Benutzer auf dem Computer hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5821-127">Use the following information to publish a package that has been added to a specific user or globally to any user on the computer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b5821-128">Veröffentlichungsmethode</span><span class="sxs-lookup"><span data-stu-id="b5821-128">Publishing method</span></span></th>
<th align="left"><span data-ttu-id="b5821-129">Cmdlet und Beispiel</span><span class="sxs-lookup"><span data-stu-id="b5821-129">Cmdlet and example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b5821-130">Veröffentlichen für den Benutzer</span><span class="sxs-lookup"><span data-stu-id="b5821-130">Publishing to the user</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="b5821-131">Cmdlet </strong> : Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="b5821-131">Cmdlet</strong>: Publish-AppvClientPackage</span></span></p>
<p><strong><span data-ttu-id="b5821-132">Beispiel </strong> : Publish-AppvClientPackage "ContosoApplication"</span><span class="sxs-lookup"><span data-stu-id="b5821-132">Example</strong>: Publish-AppvClientPackage “ContosoApplication”</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b5821-133">Global publizieren</span><span class="sxs-lookup"><span data-stu-id="b5821-133">Publishing globally</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="b5821-134">Cmdlet </strong> : Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="b5821-134">Cmdlet</strong>: Publish-AppvClientPackage</span></span></p>
<p><strong><span data-ttu-id="b5821-135">Beispiel </strong> : Publish-AppvClientPackage "ContosoApplication" – Global</span><span class="sxs-lookup"><span data-stu-id="b5821-135">Example</strong>: Publish-AppvClientPackage “ContosoApplication” -Global</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-pub-pkg-a-user-standalone-posh"></a><span data-ttu-id="b5821-136">So veröffentlichen Sie ein Paket für einen bestimmten Benutzer</span><span class="sxs-lookup"><span data-stu-id="b5821-136">To publish a package to a specific user</span></span>


<span data-ttu-id="b5821-137">**Hinweis**  Sie müssen App-V 5,0 SP2-Hotfix-Paket 5 oder höher verwenden, um diesen Parameter zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b5821-137">**Note** You must use App-V 5.0 SP2 Hotfix Package 5 or later to use this parameter.</span></span>

 

<span data-ttu-id="b5821-138">Ein Administrator kann ein Paket für einen bestimmten Benutzer veröffentlichen, indem er den optionalen **– Users** -Parameter mit dem Cmdlet **Publish-AppvClientPackage** angibt, wobei **-Benutzer-** ID die Sicherheits-ID (SID) des Endbenutzers darstellt.</span><span class="sxs-lookup"><span data-stu-id="b5821-138">An administrator can publish a package to a specific user by specifying the optional **–UserSID** parameter with the **Publish-AppvClientPackage** cmdlet, where **-UserSID** represents the end user’s security identifier (SID).</span></span>

<span data-ttu-id="b5821-139">So verwenden Sie diesen Parameter:</span><span class="sxs-lookup"><span data-stu-id="b5821-139">To use this parameter:</span></span>

-   <span data-ttu-id="b5821-140">Sie können dieses Cmdlet in der Benutzer-oder Administrator Sitzung ausführen.</span><span class="sxs-lookup"><span data-stu-id="b5821-140">You can run this cmdlet from the user or administrator session.</span></span>

-   <span data-ttu-id="b5821-141">Sie müssen mit administrativen Anmeldeinformationen angemeldet sein, um den Parameter verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="b5821-141">You must be logged in with administrative credentials to use the parameter.</span></span>

-   <span data-ttu-id="b5821-142">Der Endbenutzer muss angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="b5821-142">The end user must be logged in.</span></span>

-   <span data-ttu-id="b5821-143">Sie müssen die Sicherheits-ID (Security Identifier, SID) des Endbenutzers angeben.</span><span class="sxs-lookup"><span data-stu-id="b5821-143">You must provide the end user’s security identifier (SID).</span></span>

<span data-ttu-id="b5821-144">**Cmdlet**: Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="b5821-144">**Cmdlet**: Publish-AppvClientPackage</span></span>

<span data-ttu-id="b5821-145">**Beispiel**: Publish-AppvClientPackage "ContosoApplication"-Benutzer-e-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="b5821-145">**Example**: Publish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span>

## <a href="" id="bkmk-add-pub-pkg-standalone-posh"></a><span data-ttu-id="b5821-146">So fügen Sie ein Paket hinzu und veröffentlichen es</span><span class="sxs-lookup"><span data-stu-id="b5821-146">To add and publish a package</span></span>


<span data-ttu-id="b5821-147">Verwenden Sie die folgenden Informationen zum Hinzufügen eines Pakets zu einem Computer, und veröffentlichen Sie es für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b5821-147">Use the following information to add a package to a computer and publish it to the user.</span></span>

<span data-ttu-id="b5821-148">**Cmdlet**: Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="b5821-148">**Cmdlet**: Add-AppvClientPackage</span></span>

<span data-ttu-id="b5821-149">**Beispiel**: Add-AppvClientPackage \\\\path\\to\\appv\\package.AppV | Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="b5821-149">**Example**: Add-AppvClientPackage \\\\path\\to\\appv\\package.appv | Publish-AppvClientPackage</span></span>

## <a href="" id="bkmk-unpub-pkg-standalone-posh"></a><span data-ttu-id="b5821-150">So heben Sie die Veröffentlichung eines vorhandenen Pakets auf</span><span class="sxs-lookup"><span data-stu-id="b5821-150">To unpublish an existing package</span></span>


<span data-ttu-id="b5821-151">Verwenden Sie die folgenden Informationen zum Aufheben der Veröffentlichung eines Pakets, das für einen Benutzer berechtigt ist, das Paket aber nicht vom Computer entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5821-151">Use the following information to unpublish a package which has been entitled to a user but not remove the package from the computer.</span></span>

<span data-ttu-id="b5821-152">**Cmdlet**: Unpublish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="b5821-152">**Cmdlet**: Unpublish-AppvClientPackage</span></span>

<span data-ttu-id="b5821-153">**Beispiel**: Unpublish-AppvClientPackage "ContosoApplication"</span><span class="sxs-lookup"><span data-stu-id="b5821-153">**Example**: Unpublish-AppvClientPackage “ContosoApplication”</span></span>

## <a href="" id="bkmk-unpub-pkg-specfc-use"></a><span data-ttu-id="b5821-154">So heben Sie die Veröffentlichung eines Pakets für einen bestimmten Benutzer auf</span><span class="sxs-lookup"><span data-stu-id="b5821-154">To unpublish a package for a specific user</span></span>


<span data-ttu-id="b5821-155">**Hinweis**  Sie müssen App-V 5,0 SP2-Hotfix-Paket 5 oder höher verwenden, um diesen Parameter zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b5821-155">**Note** You must use App-V 5.0 SP2 Hotfix Package 5 or later to use this parameter.</span></span>

 

<span data-ttu-id="b5821-156">Ein Administrator kann die Veröffentlichung eines Pakets für einen bestimmten Benutzer mit dem optionalen **– Users** -Parameter mit dem Cmdlet " **UNPUBLISH-AppvClientPackage** " aufheben, wobei **-Benutzer-** ID die Sicherheits-ID (SID) des Endbenutzers darstellt.</span><span class="sxs-lookup"><span data-stu-id="b5821-156">An administrator can unpublish a package for a specific user by using the optional **–UserSID** parameter with the **Unpublish-AppvClientPackage** cmdlet, where **-UserSID** represents the end user’s security identifier (SID).</span></span>

<span data-ttu-id="b5821-157">So verwenden Sie diesen Parameter:</span><span class="sxs-lookup"><span data-stu-id="b5821-157">To use this parameter:</span></span>

-   <span data-ttu-id="b5821-158">Sie können dieses Cmdlet in der Benutzer-oder Administrator Sitzung ausführen.</span><span class="sxs-lookup"><span data-stu-id="b5821-158">You can run this cmdlet from the user or administrator session.</span></span>

-   <span data-ttu-id="b5821-159">Sie müssen mit administrativen Anmeldeinformationen angemeldet sein, um den Parameter verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="b5821-159">You must be logged in with administrative credentials to use the parameter.</span></span>

-   <span data-ttu-id="b5821-160">Der Endbenutzer muss angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="b5821-160">The end user must be logged in.</span></span>

-   <span data-ttu-id="b5821-161">Sie müssen die Sicherheits-ID (Security Identifier, SID) des Endbenutzers angeben.</span><span class="sxs-lookup"><span data-stu-id="b5821-161">You must provide the end user’s security identifier (SID).</span></span>

<span data-ttu-id="b5821-162">**Cmdlet**: Unpublish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="b5821-162">**Cmdlet**: Unpublish-AppvClientPackage</span></span>

<span data-ttu-id="b5821-163">**Beispiel**: Unpublish-AppvClientPackage "ContosoApplication"-Benutzer-e-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="b5821-163">**Example**: Unpublish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span>

## <a href="" id="bkmk-remove-pkg-standalone-posh"></a><span data-ttu-id="b5821-164">So entfernen Sie ein vorhandenes Paket</span><span class="sxs-lookup"><span data-stu-id="b5821-164">To remove an existing package</span></span>


<span data-ttu-id="b5821-165">Verwenden Sie die folgenden Informationen, um ein Paket vom Computer zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="b5821-165">Use the following information to remove a package from the computer.</span></span>

<span data-ttu-id="b5821-166">**Cmdlet**: Remove-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="b5821-166">**Cmdlet**: Remove-AppvClientPackage</span></span>

<span data-ttu-id="b5821-167">**Beispiel**: Remove-AppvClientPackage "ContosoApplication"</span><span class="sxs-lookup"><span data-stu-id="b5821-167">**Example**: Remove-AppvClientPackage “ContosoApplication”</span></span>

<span data-ttu-id="b5821-168">**Hinweis**  App-V-Cmdlets wurden Variablen für die vorherigen Beispiele nur zur besseren Übersichtlichkeit zugewiesen. Zuordnung ist keine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b5821-168">**Note** App-V cmdlets have been assigned to variables for the previous examples for clarity only; assignment is not a requirement.</span></span> <span data-ttu-id="b5821-169">Die meisten Cmdlets können so kombiniert werden [, wie Sie zum Hinzufügen und Veröffentlichen eines Pakets](#bkmk-add-pub-pkg-standalone-posh)angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b5821-169">Most cmdlets can be combined as displayed in [To add and publish a package](#bkmk-add-pub-pkg-standalone-posh).</span></span> <span data-ttu-id="b5821-170">Ein ausführliches Lernprogramm finden Sie unter [App-V 5,0 Client PowerShell Deep Dive](https://go.microsoft.com/fwlink/?LinkId=324466).</span><span class="sxs-lookup"><span data-stu-id="b5821-170">For a detailed tutorial, see [App-V 5.0 Client PowerShell Deep Dive](https://go.microsoft.com/fwlink/?LinkId=324466).</span></span>

 

## <a href="" id="bkmk-admins-pub-pkgs"></a><span data-ttu-id="b5821-171">So aktivieren Sie nur Administratoren zum Veröffentlichen oder Aufheben der Veröffentlichung von Paketen</span><span class="sxs-lookup"><span data-stu-id="b5821-171">To enable only administrators to publish or unpublish packages</span></span>


<span data-ttu-id="b5821-172">**Hinweis** 
 **Dieses Feature wird ab App-V 5,0 SP3 unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="b5821-172">**Note**
**This feature is supported starting in App-V 5.0 SP3.**</span></span>

 

<span data-ttu-id="b5821-173">Verwenden Sie das folgende Cmdlet und den folgenden Parameter, um nur Administratoren (nicht Endbenutzern) das veröffentlichen oder Aufheben der Veröffentlichung von Paketen zu ermöglichen:</span><span class="sxs-lookup"><span data-stu-id="b5821-173">Use the following cmdlet and parameter to enable only administrators (not end users) to publish or unpublish packages:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b5821-174">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b5821-174">Cmdlet</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b5821-175">Satz-AppvClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5821-175">Set-AppvClientConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b5821-176">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5821-176">Parameter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b5821-177">-RequirePublishAsAdmin</span><span class="sxs-lookup"><span data-stu-id="b5821-177">-RequirePublishAsAdmin</span></span></p>
<p><span data-ttu-id="b5821-178">Parameter Werte:</span><span class="sxs-lookup"><span data-stu-id="b5821-178">Parameter values:</span></span></p>
<ul>
<li><p><span data-ttu-id="b5821-179">0-falsch</span><span class="sxs-lookup"><span data-stu-id="b5821-179">0 - False</span></span></p></li>
<li><p><span data-ttu-id="b5821-180">1-wahr</span><span class="sxs-lookup"><span data-stu-id="b5821-180">1 - True</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="b5821-181">Beispiel: </strong> : Satz-AppvClientConfiguration – RequirePublishAsAdmin1</span><span class="sxs-lookup"><span data-stu-id="b5821-181">Example:</strong>: Set-AppvClientConfiguration –RequirePublishAsAdmin1</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b5821-182">Informationen zum Verwenden der App-V-Verwaltungskonsole zum Einrichten dieser Konfiguration finden Sie unter [Veröffentlichen eines Pakets mithilfe der Verwaltungskonsole](how-to-publish-a-package-by-using-the-management-console-50.md).</span><span class="sxs-lookup"><span data-stu-id="b5821-182">To use the App-V Management console to set this configuration, see [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md).</span></span>

## <a href="" id="bkmk-understd-pend-pkgs"></a><span data-ttu-id="b5821-183">Grundlegendes zu ausstehenden Paketen (UserPending und GlobalPending)</span><span class="sxs-lookup"><span data-stu-id="b5821-183">Understanding pending packages (UserPending and GlobalPending)</span></span>


<span data-ttu-id="b5821-184">**Ab App-V 5,0 SP2**: Wenn Sie ein PowerShell-Cmdlet ausführen, das sich auf ein aktuell verwendetes Paket auswirkt, wird die Aufgabe, die Sie durchführen möchten, in einem ausstehenden Zustand angeordnet.</span><span class="sxs-lookup"><span data-stu-id="b5821-184">**Starting in App-V 5.0 SP2**: If you run a PowerShell cmdlet that affects a package that is currently in use, the task that you are trying to perform is placed in a pending state.</span></span> <span data-ttu-id="b5821-185">Wenn Sie beispielsweise versuchen, ein Paket zu veröffentlichen, wenn eine Anwendung in diesem Paket verwendet wird, und dann **Get-AppvClientPackage**ausführen, wird der ausstehende Status in der Ausgabe des Cmdlets wie folgt angezeigt:</span><span class="sxs-lookup"><span data-stu-id="b5821-185">For example, if you try to publish a package when an application in that package is being used, and then run **Get-AppvClientPackage**, the pending status appears in the cmdlet output as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b5821-186">Ausgabeelement für Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b5821-186">Cmdlet output item</span></span></th>
<th align="left"><span data-ttu-id="b5821-187">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b5821-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b5821-188">UserPending</span><span class="sxs-lookup"><span data-stu-id="b5821-188">UserPending</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5821-189">Gibt an, ob das aufgelistete Paket eine ausstehende Aufgabe aufweist, die auf den Benutzer angewendet wird:</span><span class="sxs-lookup"><span data-stu-id="b5821-189">Indicates whether the listed package has a pending task that is being applied to the user:</span></span></p>
<ul>
<li><p><span data-ttu-id="b5821-190">Wahr</span><span class="sxs-lookup"><span data-stu-id="b5821-190">True</span></span></p></li>
<li><p><span data-ttu-id="b5821-191">False</span><span class="sxs-lookup"><span data-stu-id="b5821-191">False</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b5821-192">GlobalPending</span><span class="sxs-lookup"><span data-stu-id="b5821-192">GlobalPending</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5821-193">Gibt an, ob das aufgelistete Paket eine ausstehende Aufgabe aufweist, die Global auf den Computer angewendet wird:</span><span class="sxs-lookup"><span data-stu-id="b5821-193">Indicates whether the listed package has a pending task that is being applied globally to the computer:</span></span></p>
<ul>
<li><p><span data-ttu-id="b5821-194">Wahr</span><span class="sxs-lookup"><span data-stu-id="b5821-194">True</span></span></p></li>
<li><p><span data-ttu-id="b5821-195">False</span><span class="sxs-lookup"><span data-stu-id="b5821-195">False</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b5821-196">Die ausstehende Aufgabe wird später entsprechend den folgenden Regeln ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="b5821-196">The pending task will run later, according to the following rules:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b5821-197">Art der Hintergrundaufgabe</span><span class="sxs-lookup"><span data-stu-id="b5821-197">Task type</span></span></th>
<th align="left"><span data-ttu-id="b5821-198">Anwendbare Regel</span><span class="sxs-lookup"><span data-stu-id="b5821-198">Applicable rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b5821-199">Benutzerbasierte Aufgaben, beispielsweise die Veröffentlichung eines Pakets für einen Benutzer</span><span class="sxs-lookup"><span data-stu-id="b5821-199">User-based task, e.g., publishing a package to a user</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5821-200">Die ausstehende Aufgabe wird ausgeführt, nachdem sich der Benutzer abgemeldet hat und sich dann wieder anmeldet.</span><span class="sxs-lookup"><span data-stu-id="b5821-200">The pending task will be performed after the user logs off and then logs back on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b5821-201">Global basierender Vorgang, beispielsweise Aktivieren einer Verbindungsgruppe Global</span><span class="sxs-lookup"><span data-stu-id="b5821-201">Globally based task, e.g., enabling a connection group globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5821-202">Die ausstehende Aufgabe wird ausgeführt, wenn der Computer heruntergefahren und neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b5821-202">The pending task will be performed when the computer is shut down and then restarted.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b5821-203">Weitere Informationen zu ausstehenden Aufgaben finden Sie unter [Informationen zu App-V 5,0 SP2](about-app-v-50-sp2.md#bkmk-pkg-upgr-pendg-tasks).</span><span class="sxs-lookup"><span data-stu-id="b5821-203">For more information about pending tasks, see [About App-V 5.0 SP2](about-app-v-50-sp2.md#bkmk-pkg-upgr-pendg-tasks).</span></span>

<span data-ttu-id="b5821-204">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="b5821-204">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="b5821-205">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="b5821-205">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="b5821-206">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="b5821-206">Got an App-V issue?</span></span>** <span data-ttu-id="b5821-207">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="b5821-207">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="b5821-208">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b5821-208">Related topics</span></span>


[<span data-ttu-id="b5821-209">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="b5821-209">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="b5821-210">Verwalten von App-V mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="b5821-210">Administering App-V by Using PowerShell</span></span>](administering-app-v-by-using-powershell.md)

 

 





