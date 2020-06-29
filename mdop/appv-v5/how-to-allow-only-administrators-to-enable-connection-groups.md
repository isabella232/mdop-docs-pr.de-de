---
title: So schränken Sie die Aktivierung von Verbindungsgruppen auf Administratoren ein
description: So schränken Sie die Aktivierung von Verbindungsgruppen auf Administratoren ein
author: dansimp
ms.assetid: 60e62426-624f-4f26-851e-41cd78520883
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 53461d5c93bf246210c7427c95a8bbe8acca9cf7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805744"
---
# <span data-ttu-id="9dfcb-103">So schränken Sie die Aktivierung von Verbindungsgruppen auf Administratoren ein</span><span class="sxs-lookup"><span data-stu-id="9dfcb-103">How to Allow Only Administrators to Enable Connection Groups</span></span>


<span data-ttu-id="9dfcb-104">Sie können den App-V-Client so konfigurieren, dass nur Administratoren (nicht Endbenutzer) Verbindungsgruppen aktivieren oder deaktivieren können.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-104">You can configure the App-V client so that only administrators (not end users) can enable or disable connection groups.</span></span> <span data-ttu-id="9dfcb-105">In früheren Versionen von App-V konnten Sie nicht verhindern, dass Endbenutzer diese Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-105">In earlier versions of App-V, you could not prevent end users from performing these tasks.</span></span>

<span data-ttu-id="9dfcb-106">**Hinweis** 
 **Dieses Feature wird ab App-V 5,0 SP3 unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="9dfcb-106">**Note**
**This feature is supported starting in App-V 5.0 SP3.**</span></span>

 

<span data-ttu-id="9dfcb-107">Verwenden Sie eine der folgenden Methoden, damit nur Administratoren Verbindungsgruppen aktivieren oder deaktivieren können.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-107">Use one of the following methods to allow only administrators to enable or disable connection groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9dfcb-108">Methode</span><span class="sxs-lookup"><span data-stu-id="9dfcb-108">Method</span></span></th>
<th align="left"><span data-ttu-id="9dfcb-109">Schritte</span><span class="sxs-lookup"><span data-stu-id="9dfcb-109">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9dfcb-110">Gruppenrichtlinieneinstellung</span><span class="sxs-lookup"><span data-stu-id="9dfcb-110">Group Policy setting</span></span></p></td>
<td align="left"><p><span data-ttu-id="9dfcb-111">Aktivieren Sie die Gruppenrichtlinieneinstellung "Veröffentlichung als Administrator anfordern", die sich im folgenden Gruppenrichtlinien-Objektknoten befindet:</span><span class="sxs-lookup"><span data-stu-id="9dfcb-111">Enable the “Require publish as administrator” Group Policy setting, which is located in the following Group Policy Object node:</span></span></p>
<p><strong><span data-ttu-id="9dfcb-112">Computerkonfigurations &gt; Richtlinien &gt; , administrative Vorlagen &gt; &gt; , System App-V &gt; Publishing</span><span class="sxs-lookup"><span data-stu-id="9dfcb-112">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9dfcb-113">PowerShell-Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9dfcb-113">PowerShell cmdlet</span></span></p></td>
<td align="left"><p><span data-ttu-id="9dfcb-114">Führen Sie das <strong> Cmdlet "Satz-AppvClientConfiguration </strong> " mit dem <strong> Parameter "– RequirePublishAsAdmin" aus </strong> .</span><span class="sxs-lookup"><span data-stu-id="9dfcb-114">Run the <strong>Set-AppvClientConfiguration</strong> cmdlet with the <strong>–RequirePublishAsAdmin</strong> parameter.</span></span></p>
<p><span data-ttu-id="9dfcb-115">Parameter Werte:</span><span class="sxs-lookup"><span data-stu-id="9dfcb-115">Parameter values:</span></span></p>
<ul>
<li><p><span data-ttu-id="9dfcb-116">0-falsch</span><span class="sxs-lookup"><span data-stu-id="9dfcb-116">0 - False</span></span></p></li>
<li><p><span data-ttu-id="9dfcb-117">1-wahr</span><span class="sxs-lookup"><span data-stu-id="9dfcb-117">1 - True</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="9dfcb-118">Beispiel: </strong> : Satz-AppvClientConfiguration – RequirePublishAsAdmin1</span><span class="sxs-lookup"><span data-stu-id="9dfcb-118">Example:</strong>: Set-AppvClientConfiguration –RequirePublishAsAdmin1</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="9dfcb-119">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="9dfcb-119">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="9dfcb-120">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-120">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="9dfcb-121">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="9dfcb-121">Got an App-V issue?</span></span>** <span data-ttu-id="9dfcb-122">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="9dfcb-122">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="9dfcb-123">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9dfcb-123">Related topics</span></span>


[<span data-ttu-id="9dfcb-124">Verwalten von Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="9dfcb-124">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





