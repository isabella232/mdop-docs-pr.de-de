---
title: Ermitteln, welche Art von Anwendung zu sequenzieren ist (App-V 4,6 SP1)
description: Ermitteln, welche Art von Anwendung zu sequenzieren ist (App-V 4,6 SP1)
author: dansimp
ms.assetid: 936abee2-98f1-45fb-9f0d-786e1d7464b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 001f6afa36ca28eb1b8e0cc2ccc161cef4194d24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807127"
---
# <span data-ttu-id="5af43-103">Ermitteln, welche Art von Anwendung zu sequenzieren ist (App-V 4,6 SP1)</span><span class="sxs-lookup"><span data-stu-id="5af43-103">How to Determine Which Type of Application to Sequence (App-V 4.6 SP1)</span></span>


<span data-ttu-id="5af43-104">Sie können drei grundlegende Arten von Anwendungen mithilfe von Microsoft Application Virtualization (App-V) Sequencer abgleichen.</span><span class="sxs-lookup"><span data-stu-id="5af43-104">You can sequence three basic types of applications by using Microsoft Application Virtualization (App-V) Sequencer.</span></span>

## <span data-ttu-id="5af43-105">So ermitteln Sie, welche Art von Anwendung Abfolge ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="5af43-105">To determine which type of application to sequence</span></span>


<span data-ttu-id="5af43-106">Ermitteln Sie anhand der folgenden Tabelle, welche Art von Anwendung Sie abbilden sollten, und erhalten Sie weitere Informationen zum Sequenzieren der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5af43-106">Use the following table to determine which type of application you should sequence and to obtain more information about how to sequence the application.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5af43-107">Anwendungstyp</span><span class="sxs-lookup"><span data-stu-id="5af43-107">Application Type</span></span></th>
<th align="left"><span data-ttu-id="5af43-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5af43-108">Description</span></span></th>
<th align="left"><span data-ttu-id="5af43-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5af43-109">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5af43-110">Standard</span><span class="sxs-lookup"><span data-stu-id="5af43-110">Standard</span></span></p></td>
<td align="left"><p><span data-ttu-id="5af43-111">Wählen Sie diese Option aus, um ein Paket zu erstellen, das eine Anwendung oder eine Suite von Anwendungen enthält.</span><span class="sxs-lookup"><span data-stu-id="5af43-111">Select this option to create a package that contains an application or a suite of applications.</span></span> <span data-ttu-id="5af43-112">Wählen Sie diese Option für die meisten Anwendungen aus, die Sie abgleichen möchten.</span><span class="sxs-lookup"><span data-stu-id="5af43-112">You should select this option for most applications that you plan to sequence.</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-standard-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Standard Application (App-V 4.6 SP1)](how-to-sequence-a-new-standard-application--app-v-46-sp1-.md)"><span data-ttu-id="5af43-113">So sequenzieren Sie eine neue Standardanwendung (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="5af43-113">How to Sequence a New Standard Application (App-V 4.6 SP1)</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5af43-114">Add-on oder Plug-in</span><span class="sxs-lookup"><span data-stu-id="5af43-114">Add-on or Plug-in</span></span></p></td>
<td align="left"><p><span data-ttu-id="5af43-115">Wählen Sie diese Option aus, um ein Paket zu erstellen, das die Funktionalität einer Standardanwendung erweitert, beispielsweise ein Plug-in für Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="5af43-115">Select this option to create a package that extends the functionality of a standard application, for example, a plug-in for Microsoft Excel.</span></span> <span data-ttu-id="5af43-116">Darüber hinaus können Sie Plug-Ins für nativ installierte Anwendungen oder ein anderes Paket verwenden, das mithilfe der Dynamic Suite-Komposition verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="5af43-116">Additionally, you can use plug-ins for natively installed applications, or another package that is linked by using Dynamic Suite Composition.</span></span> <span data-ttu-id="5af43-117">Weitere Informationen zur Komposition von Dynamic Suite finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)"> Verwenden der Dynamic Suite Composition </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804"> https://go.microsoft.com/fwlink/?LinkId=203804 </a> ).</span><span class="sxs-lookup"><span data-stu-id="5af43-117">For more information about Dynamic Suite Composition, see <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)">How To Use Dynamic Suite Composition</a> (<a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804">https://go.microsoft.com/fwlink/?LinkId=203804</a>).</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-add-on-or-plug-in-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Add-on or Plug-in Application (App-V 4.6 SP1)](how-to-sequence-a-new-add-on-or-plug-in-application--app-v-46-sp1-.md)"><span data-ttu-id="5af43-118">So sequenzieren Sie eine neue Add-On- oder Plug-In-Anwendung (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="5af43-118">How to Sequence a New Add-on or Plug-in Application (App-V 4.6 SP1)</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5af43-119">Middleware</span><span class="sxs-lookup"><span data-stu-id="5af43-119">Middleware</span></span></p></td>
<td align="left"><p><span data-ttu-id="5af43-120">Wählen Sie diese Option aus, um ein Paket zu erstellen, das für eine Standardanwendung erforderlich ist, beispielsweise Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="5af43-120">Select this option to create a package that is required by a standard application, for example, the Microsoft .NET Framework.</span></span> <span data-ttu-id="5af43-121">Middleware-Pakete werden zum Verknüpfen mit anderen Paketen mithilfe der Dynamic Suite-Komposition verwendet.</span><span class="sxs-lookup"><span data-stu-id="5af43-121">Middleware packages are used for linking to other packages by using Dynamic Suite Composition.</span></span> <span data-ttu-id="5af43-122">Weitere Informationen zur Komposition von Dynamic Suite finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)"> Verwenden der Dynamic Suite Composition </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804"> https://go.microsoft.com/fwlink/?LinkId=203804 </a> ).</span><span class="sxs-lookup"><span data-stu-id="5af43-122">For more information about Dynamic Suite Composition, see <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)">How To Use Dynamic Suite Composition</a> (<a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804">https://go.microsoft.com/fwlink/?LinkId=203804</a>).</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-middleware-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Middleware Application (App-V 4.6 SP1)](how-to-sequence-a-new-middleware-application--app-v-46-sp1-.md)"><span data-ttu-id="5af43-123">So sequenzieren Sie eine neue Middleware Anwendung (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="5af43-123">How to Sequence a New Middleware Application (App-V 4.6 SP1)</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5af43-124">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5af43-124">Related topics</span></span>


[<span data-ttu-id="5af43-125">Aufgaben für Application Virtualization Sequencer (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="5af43-125">Tasks for the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

 

 





