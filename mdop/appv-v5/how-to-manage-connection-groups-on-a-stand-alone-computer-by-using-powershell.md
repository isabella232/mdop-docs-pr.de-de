---
title: So verwalten Sie Verbindungsgruppen auf einem eigenständigen Computer mithilfe von PowerShell
description: So verwalten Sie Verbindungsgruppen auf einem eigenständigen Computer mithilfe von PowerShell
author: dansimp
ms.assetid: b73ae74d-8a6f-4bb3-b1f2-0067c7bd5212
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 32dd4f9c5ad1ba4ae9e25246d5ec52a6363ef303
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805342"
---
# <span data-ttu-id="5b16f-103">So verwalten Sie Verbindungsgruppen auf einem eigenständigen Computer mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="5b16f-103">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span>


<span data-ttu-id="5b16f-104">Mit einer App-V-Verbindungsgruppe können Sie alle virtuellen Anwendungen als definierten Satz von Paketen in einer einzelnen virtuellen Umgebung ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b16f-104">An App-V connection group allows you to run all the virtual applications as a defined set of packages in a single virtual environment.</span></span> <span data-ttu-id="5b16f-105">So können Sie beispielsweise eine Anwendung und ihre Plug-Ins mithilfe separater Pakete virtualisieren, Sie aber in einer einzelnen Verbindungsgruppe zusammenführen.</span><span class="sxs-lookup"><span data-stu-id="5b16f-105">For example, you can virtualize an application and its plug-ins by using separate packages, but run them together in a single connection group.</span></span>

<span data-ttu-id="5b16f-106">Eine Verbindungsgruppen-XML-Datei definiert die Verbindungsgruppe, die auf dem Computer ausgeführt wird, auf dem Sie den App-V-Client installiert haben.</span><span class="sxs-lookup"><span data-stu-id="5b16f-106">A connection group XML file defines the connection group that runs on the computer where you’ve installed the App-V client.</span></span> <span data-ttu-id="5b16f-107">Informationen zur XML-Verbindungsgruppen-Datei und deren Konfiguration finden Sie unter Informationen zur [Verbindungsgruppen Datei](about-the-connection-group-file.md).</span><span class="sxs-lookup"><span data-stu-id="5b16f-107">For information about the connection group XML file and how to configure it, see [About the Connection Group File](about-the-connection-group-file.md).</span></span>

<span data-ttu-id="5b16f-108">In diesem Thema werden die folgenden Verfahren erläutert:</span><span class="sxs-lookup"><span data-stu-id="5b16f-108">This topic explains the following procedures:</span></span>

-   [<span data-ttu-id="5b16f-109">So fügen Sie die App-V-Pakete in der Verbindungsgruppe hinzu und veröffentlichen Sie</span><span class="sxs-lookup"><span data-stu-id="5b16f-109">To add and publish the App-V packages in the connection group</span></span>](#bkmk-add-pub-pkgs-in-cg)

-   [<span data-ttu-id="5b16f-110">So fügen Sie die Verbindungsgruppe auf dem App-V-Client hinzu und aktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="5b16f-110">To add and enable the connection group on the App-V client</span></span>](#bkmk-add-enable-cg-on-clt)

-   [<span data-ttu-id="5b16f-111">So aktivieren oder deaktivieren Sie eine Verbindungsgruppe für einen bestimmten Benutzer</span><span class="sxs-lookup"><span data-stu-id="5b16f-111">To enable or disable a connection group for a specific user</span></span>](#bkmk-enable-cg-for-user-poshtopic)

-   [<span data-ttu-id="5b16f-112">So ermöglichen Sie es nur Administratoren, Verbindungsgruppen zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="5b16f-112">To allow only administrators to enable connection groups</span></span>](#bkmk-admin-only-posh-topic-cg)

<a href="" id="bkmk-add-pub-pkgs-in-cg"></a>**<span data-ttu-id="5b16f-113">So fügen Sie die App-V-Pakete in der Verbindungsgruppe hinzu und veröffentlichen Sie</span><span class="sxs-lookup"><span data-stu-id="5b16f-113">To add and publish the App-V packages in the connection group</span></span>**

1.  <span data-ttu-id="5b16f-114">Zum Hinzufügen und Veröffentlichen der APP-v 5,0-Pakete auf dem Computer, auf dem der APP-v-Client ausgeführt wird, geben Sie den folgenden Befehl ein:</span><span class="sxs-lookup"><span data-stu-id="5b16f-114">To add and publish the App-V 5.0 packages to the computer running the App-V client, type the following command:</span></span>

    <span data-ttu-id="5b16f-115">Add-AppvClientPackage – Pfad-c:\\tmpstore\\quartfin.AppV | Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="5b16f-115">Add-AppvClientPackage –path c:\\tmpstore\\quartfin.appv | Publish-AppvClientPackage</span></span>

2.  <span data-ttu-id="5b16f-116">Wiederholen Sie **Schritt 1** dieses Verfahrens für jedes Paket in der Verbindungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="5b16f-116">Repeat **step 1** of this procedure for each package in the connection group.</span></span>

<a href="" id="bkmk-add-enable-cg-on-clt"></a>**<span data-ttu-id="5b16f-117">So fügen Sie die Verbindungsgruppe auf dem App-V-Client hinzu und aktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="5b16f-117">To add and enable the connection group on the App-V client</span></span>**

1.  <span data-ttu-id="5b16f-118">Fügen Sie die Verbindungsgruppe hinzu, indem Sie den folgenden Befehl eingeben:</span><span class="sxs-lookup"><span data-stu-id="5b16f-118">Add the connection group by typing the following command:</span></span>

    <span data-ttu-id="5b16f-119">Add-AppvClientConnectionGroup – Pfad c:\\tmpstore\\financ.xml</span><span class="sxs-lookup"><span data-stu-id="5b16f-119">Add-AppvClientConnectionGroup –path c:\\tmpstore\\financ.xml</span></span>

2.  <span data-ttu-id="5b16f-120">Aktivieren Sie die Verbindungsgruppe, indem Sie den folgenden Befehl eingeben:</span><span class="sxs-lookup"><span data-stu-id="5b16f-120">Enable the connection group by typing the following command:</span></span>

    <span data-ttu-id="5b16f-121">Enable-AppvClientConnectionGroup – Name "Financial Applications"</span><span class="sxs-lookup"><span data-stu-id="5b16f-121">Enable-AppvClientConnectionGroup –name “Financial Applications”</span></span>

    <span data-ttu-id="5b16f-122">Wenn alle virtuellen Anwendungen, die sich in den Mitglieds Paketen befinden, auf dem Zielcomputer ausgeführt werden, werden Sie innerhalb der virtuellen Umgebung der Verbindungsgruppe ausgeführt und stehen für alle virtuellen Anwendungen in den anderen Paketen in der Verbindungsgruppe zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="5b16f-122">When any virtual applications that are in the member packages are run on the target computer, they will run inside the connection group’s virtual environment and will be available to all the virtual applications in the other packages in the connection group.</span></span>

<a href="" id="bkmk-enable-cg-for-user-poshtopic"></a>**<span data-ttu-id="5b16f-123">So aktivieren oder deaktivieren Sie eine Verbindungsgruppe für einen bestimmten Benutzer</span><span class="sxs-lookup"><span data-stu-id="5b16f-123">To enable or disable a connection group for a specific user</span></span>**

1.  <span data-ttu-id="5b16f-124">Überprüfen Sie die Parameter Beschreibung und die Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="5b16f-124">Review the parameter description and requirements:</span></span>

    -   <span data-ttu-id="5b16f-125">Mithilfe des Parameters kann ein Administrator eine Verbindungsgruppe für einen bestimmten Benutzer aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="5b16f-125">The parameter enables an administrator to enable or disable a connection group for a specific user.</span></span>

    -   <span data-ttu-id="5b16f-126">Sie müssen App-V 5,0 SP2-Hotfix-Paket 5 oder höher verwenden, um diesen Parameter zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5b16f-126">You must use App-V 5.0 SP2 Hotfix Package 5 or later to use this parameter.</span></span>

    -   <span data-ttu-id="5b16f-127">Sie können dieses Cmdlet in der Benutzer-oder Administrator Sitzung ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b16f-127">You can run this cmdlet from the user or administrator session.</span></span>

    -   <span data-ttu-id="5b16f-128">Sie müssen mit administrativen Anmeldeinformationen angemeldet sein, um den Parameter verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="5b16f-128">You must be logged in with administrative credentials to use the parameter.</span></span>

    -   <span data-ttu-id="5b16f-129">Der Endbenutzer muss angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="5b16f-129">The end user must be logged in.</span></span>

    -   <span data-ttu-id="5b16f-130">Sie müssen die Sicherheits-ID (Security Identifier, SID) des Endbenutzers angeben.</span><span class="sxs-lookup"><span data-stu-id="5b16f-130">You must provide the end user’s security identifier (SID).</span></span>

2.  <span data-ttu-id="5b16f-131">Verwenden Sie die folgenden Cmdlets, und fügen Sie den optionalen **– Users** -Parameter hinzu, wobei **-Benutzer-** ID die Sicherheits-ID (SID) des Endbenutzers darstellt:</span><span class="sxs-lookup"><span data-stu-id="5b16f-131">Use the following cmdlets, and add the optional **–UserSID** parameter, where **-UserSID** represents the end user’s security identifier (SID):</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="5b16f-132">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b16f-132">Cmdlet</span></span></th>
    <th align="left"><span data-ttu-id="5b16f-133">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b16f-133">Examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="5b16f-134">Enable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="5b16f-134">Enable-AppVClientConnectionGroup</span></span></p></td>
    <td align="left"><p><span data-ttu-id="5b16f-135">Enable-AppVClientConnectionGroup "ConnectionGroupA"-Benutzer-e-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="5b16f-135">Enable-AppVClientConnectionGroup “ConnectionGroupA” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="5b16f-136">Deaktivieren-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="5b16f-136">Disable -AppVClientConnectionGroup</span></span></p></td>
    <td align="left"><p><span data-ttu-id="5b16f-137">Disable-AppVClientConnectionGroup "ConnectionGroupA"-Benutzer-e-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="5b16f-137">Disable -AppVClientConnectionGroup “ConnectionGroupA” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
    </tr>
    </tbody>
    </table>

<a href="" id="bkmk-admin-only-posh-topic-cg"></a>**<span data-ttu-id="5b16f-138">So ermöglichen Sie es nur Administratoren, Verbindungsgruppen zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="5b16f-138">To allow only administrators to enable connection groups</span></span>**

1.  <span data-ttu-id="5b16f-139">Überprüfen Sie die Beschreibung und die Voraussetzungen für die Verwendung dieses Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="5b16f-139">Review the description and requirement for using this cmdlet:</span></span>

    -   <span data-ttu-id="5b16f-140">Mithilfe dieses Cmdlets und Parameters können Sie den App-V-Client so konfigurieren, dass nur Administratoren (nicht Endbenutzer) Verbindungsgruppen aktivieren oder deaktivieren können.</span><span class="sxs-lookup"><span data-stu-id="5b16f-140">Use this cmdlet and parameter to configure the App-V client to allow only administrators (not end users) to enable or disable connection groups.</span></span>

    -   <span data-ttu-id="5b16f-141">Sie müssen mindestens App-V 5,0 SP3 verwenden, um dieses Cmdlet verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="5b16f-141">You must be using at least App-V 5.0 SP3 to use this cmdlet.</span></span>

2.  <span data-ttu-id="5b16f-142">Führen Sie das folgende Cmdlet und den folgenden Parameter aus:</span><span class="sxs-lookup"><span data-stu-id="5b16f-142">Run the following cmdlet and parameter:</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="5b16f-143">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b16f-143">Cmdlet</span></span></th>
    <th align="left"><span data-ttu-id="5b16f-144">Parameter und Werte</span><span class="sxs-lookup"><span data-stu-id="5b16f-144">Parameter and values</span></span></th>
    <th align="left"><span data-ttu-id="5b16f-145">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5b16f-145">Example</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="5b16f-146">Satz-AppvClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b16f-146">Set-AppvClientConfiguration</span></span></p></td>
    <td align="left"><p><span data-ttu-id="5b16f-147">–RequirePublishAsAdmin</span><span class="sxs-lookup"><span data-stu-id="5b16f-147">–RequirePublishAsAdmin</span></span></p>
    <ul>
    <li><p><span data-ttu-id="5b16f-148">0-falsch</span><span class="sxs-lookup"><span data-stu-id="5b16f-148">0 - False</span></span></p></li>
    <li><p><span data-ttu-id="5b16f-149">1-wahr</span><span class="sxs-lookup"><span data-stu-id="5b16f-149">1 - True</span></span></p></li>
    </ul></td>
    <td align="left"><p><span data-ttu-id="5b16f-150">Satz-AppvClientConfiguration – RequirePublishAsAdmin1</span><span class="sxs-lookup"><span data-stu-id="5b16f-150">Set-AppvClientConfiguration –RequirePublishAsAdmin1</span></span></p></td>
    </tr>
    </tbody>
    </table>

    <span data-ttu-id="5b16f-151">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="5b16f-151">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="5b16f-152">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="5b16f-152">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="5b16f-153">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="5b16f-153">Got an App-V issue?</span></span>** <span data-ttu-id="5b16f-154">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="5b16f-154">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="5b16f-155">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5b16f-155">Related topics</span></span>


[<span data-ttu-id="5b16f-156">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="5b16f-156">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="5b16f-157">Verwalten von App-V mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="5b16f-157">Administering App-V by Using PowerShell</span></span>](administering-app-v-by-using-powershell.md)

 

 





