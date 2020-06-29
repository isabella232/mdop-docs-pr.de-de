---
title: Planen der Speicherung und Bereitstellung des DaRT 7.0-Wiederherstellungsabbilds
description: Planen der Speicherung und Bereitstellung des DaRT 7.0-Wiederherstellungsabbilds
author: dansimp
ms.assetid: d96e9363-6186-4fc3-9b83-ba15ed9694a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c292633949865d4b3f5053700f4219db3f1cf465
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809571"
---
# <span data-ttu-id="c0e6d-103">Planen der Speicherung und Bereitstellung des DaRT 7.0-Wiederherstellungsabbilds</span><span class="sxs-lookup"><span data-stu-id="c0e6d-103">Planning How to Save and Deploy the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="c0e6d-104">Verwenden Sie die Informationen in diesem Abschnitt, wenn Sie beabsichtigen, das Microsoft Diagnostics and Recovery Toolset (Dart) 7-Wiederherstellungsabbild zu speichern und bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c0e6d-104">Use the information in this section when you plan for saving and deploying the Microsoft Diagnostics and Recovery Toolset (DaRT)7 recovery image.</span></span>

## <span data-ttu-id="c0e6d-105">Planen des Speicherns und Bereitstellens des DART-Wiederherstellungs Bilds</span><span class="sxs-lookup"><span data-stu-id="c0e6d-105">Planning How to Save and Deploy the DaRT Recovery Image</span></span>


<span data-ttu-id="c0e6d-106">Sie können das DART-Wiederherstellungsabbild mithilfe der folgenden Methoden speichern und bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c0e6d-106">You can save and deploy the DaRT recovery image by using the following methods.</span></span> <span data-ttu-id="c0e6d-107">Berücksichtigen Sie die vor-und Nachteile der einzelnen Methoden, wenn Sie die Methode ermitteln, die Sie verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="c0e6d-107">When you are determining the method that you will use, consider the advantages and disadvantages of each.</span></span> <span data-ttu-id="c0e6d-108">Denken Sie auch daran, wie Sie Dart in Ihrem Unternehmen verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="c0e6d-108">Also, consider how you want to use DaRT in your enterprise.</span></span>

<span data-ttu-id="c0e6d-109">**Hinweis**  Möglicherweise möchten Sie in Ihrer Organisation mehr als eine Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="c0e6d-109">**Note** You might want to use more than one method in your organization.</span></span> <span data-ttu-id="c0e6d-110">So können Sie beispielsweise für die meisten Situationen in DART von einer Remotepartition Booten und einen USB-Stick zur Verfügung stellen, falls der Endbenutzercomputer keine Verbindung mit dem Netzwerk herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="c0e6d-110">For example, you can boot into DaRT from a remote partition for most situations and have a USB flash drive available in case the end-user computer cannot connect to the network.</span></span>

 

<span data-ttu-id="c0e6d-111">Die folgende Tabelle zeigt einige vor-und Nachteile der einzelnen Methoden der Verwendung von Dart in Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="c0e6d-111">The following table shows some advantages and disadvantages of each method of using DaRT in your organization.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c0e6d-112">Methode zum Booten in DART</span><span class="sxs-lookup"><span data-stu-id="c0e6d-112">Method to Boot into DaRT</span></span></th>
<th align="left"><span data-ttu-id="c0e6d-113">Vorteile</span><span class="sxs-lookup"><span data-stu-id="c0e6d-113">Advantages</span></span></th>
<th align="left"><span data-ttu-id="c0e6d-114">Nachteile</span><span class="sxs-lookup"><span data-stu-id="c0e6d-114">Disadvantages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e6d-115">Von einer CD oder DVD</span><span class="sxs-lookup"><span data-stu-id="c0e6d-115">From a CD or DVD</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e6d-116">Unterstützt Szenarien, in denen der Master Boot Record (MBR) beschädigt ist und Sie nicht auf die Festplatte zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="c0e6d-116">Supports scenarios in which the master boot record (MBR) is corrupted and you cannot access the hard disk.</span></span> <span data-ttu-id="c0e6d-117">Unterstützt auch Fälle, in denen keine Netzwerkverbindung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c0e6d-117">Also supports cases in which there is no network connection.</span></span></p>
<p><span data-ttu-id="c0e6d-118">Diese Vorgehensweise ist für Benutzer mit früheren DART-Versionen am besten bekannt, und eine CD oder DVD kann direkt aus dem <strong> Dart-Wiederherstellungsbild-Assistenten gebrannt werden </strong> .</span><span class="sxs-lookup"><span data-stu-id="c0e6d-118">This is most familiar to users of earlier versions of DaRT, and a CD or DVD can be burned directly from the <strong>DaRT Recovery Image Wizard</strong>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e6d-119">Erfordert, dass eine Person mit Zugriff auf die CD oder DVD physisch auf dem Computer des Endbenutzers ist, um in DART zu booten.</span><span class="sxs-lookup"><span data-stu-id="c0e6d-119">Requires that someone with access to the CD or DVD is physically at the end-user computer to boot into DaRT.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e6d-120">Über einen USB-Stick (USB-Stick)</span><span class="sxs-lookup"><span data-stu-id="c0e6d-120">From a USB flash drive (UFD)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e6d-121">Bietet dieselben Vorteile wie das Booten von einer CD oder DVD und bietet auch Unterstützung für Computer, die kein CD-oder DVD-Laufwerk besitzen.</span><span class="sxs-lookup"><span data-stu-id="c0e6d-121">Provides same advantages as booting from a CD or DVD and also provides support to computers that have no CD or DVD drive.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e6d-122">Erfordert die Formatierung des USB-Flashlaufwerks, bevor Sie es zum Starten in DART verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c0e6d-122">Requires you to format the UFD before you can use it to boot into DaRT.</span></span> <span data-ttu-id="c0e6d-123">Erfordert auch, dass eine Person mit Zugriff auf das USB-Flashlaufwerk physisch auf dem Computer des Endbenutzers ist, um in DART zu booten.</span><span class="sxs-lookup"><span data-stu-id="c0e6d-123">Also requires that someone with access to the UFD is physically at the end-user computer to boot into DaRT.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e6d-124">Von einer Remote-(Netzwerk-) Partition</span><span class="sxs-lookup"><span data-stu-id="c0e6d-124">From a remote (network) partition</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e6d-125">Ermöglicht das Booten in Dart, ohne dass eine CD, DVD oder ein USB-Laufwerk benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="c0e6d-125">Lets you boot into DaRT without needing a CD, DVD, or UFD.</span></span> <span data-ttu-id="c0e6d-126">Ermöglicht auch einfache Upgrades von Dart, da nur ein Dateispeicherort zu aktualisieren ist.</span><span class="sxs-lookup"><span data-stu-id="c0e6d-126">Also allows for easy upgrades of DaRT because there is only one file location to update.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e6d-127">Funktioniert nicht, wenn der Computer des Endbenutzers nicht mit dem Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="c0e6d-127">Does not work if the end-user computer is not connected to the network.</span></span></p>
<p><span data-ttu-id="c0e6d-128">Für Endbenutzer weithin verfügbar und erfordern möglicherweise zusätzliche Sicherheitsüberlegungen, wenn Sie das Wiederherstellungsabbild erstellen.</span><span class="sxs-lookup"><span data-stu-id="c0e6d-128">Widely available to end users and might require additional security considerations when you are creating the recovery image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e6d-129">Von einer Wiederherstellungspartition</span><span class="sxs-lookup"><span data-stu-id="c0e6d-129">From a recovery partition</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e6d-130">Mit dieser Option können Sie in DART Booten, ohne eine CD, DVD oder ein USB-Flashlaufwerk zu benötigen, das Instanzen enthält, in denen keine Netzwerkkonnektivität vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c0e6d-130">Lets you boot into DaRT without needing a CD, DVD, or UFD that includes instances in which there is no network connectivity.</span></span></p>
<p><span data-ttu-id="c0e6d-131">Darüber hinaus können Sie mithilfe von automatisierten Verteilungstools wie Microsoft Endpoint Configuration Manager als Teil Ihres standardmäßigen Windows-Abbild Prozesses implementiert und verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="c0e6d-131">Also, can be implemented and managed as part of your standard Windows image process by using automated distribution tools, such as Microsoft Endpoint Configuration Manager.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e6d-132">Beim Aktualisieren von DART müssen Sie alle Computer in Ihrem Unternehmen anstatt nur eine Partition (im Netzwerk) oder ein Gerät (CD, DVD oder USB-Flashlaufwerk) aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c0e6d-132">When updating DaRT, requires you to update all computers in your enterprise instead of just one partition (on the network) or device (CD, DVD, or UFD).</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c0e6d-133">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c0e6d-133">Related topics</span></span>


[<span data-ttu-id="c0e6d-134">Planen der Bereitstellung von DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="c0e6d-134">Planning to Deploy DaRT 7.0</span></span>](planning-to-deploy-dart-70.md)

 

 





