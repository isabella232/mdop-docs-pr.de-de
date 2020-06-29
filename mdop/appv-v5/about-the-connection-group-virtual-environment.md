---
title: Über die virtuelle Verbindungsgruppenumgebung
description: Über die virtuelle Verbindungsgruppenumgebung
author: dansimp
ms.assetid: 535fa640-cbd9-425e-8437-94650a70c264
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bd93c9e7acbf7bbf3f9da506d5d95b8df09e1f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806080"
---
# <span data-ttu-id="6a9d3-103">Über die virtuelle Verbindungsgruppenumgebung</span><span class="sxs-lookup"><span data-stu-id="6a9d3-103">About the Connection Group Virtual Environment</span></span>


**<span data-ttu-id="6a9d3-104">In diesem Thema:</span><span class="sxs-lookup"><span data-stu-id="6a9d3-104">In this topic:</span></span>**

-   [<span data-ttu-id="6a9d3-105">Ermitteln der Paketpriorität</span><span class="sxs-lookup"><span data-stu-id="6a9d3-105">How package priority is determined</span></span>](#bkmk-pkg-priority-deter)

-   [<span data-ttu-id="6a9d3-106">Zusammenführen identischer Paket Pfade zu einem virtuellen Verzeichnis in Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="6a9d3-106">Merging identical package paths into one virtual directory in connection groups</span></span>](#bkmk-merged-root-ve-exp)

## <a href="" id="bkmk-pkg-priority-deter"></a><span data-ttu-id="6a9d3-107">Ermitteln der Paketpriorität</span><span class="sxs-lookup"><span data-stu-id="6a9d3-107">How package priority is determined</span></span>


<span data-ttu-id="6a9d3-108">Die virtuelle Umgebung und Ihr aktueller Zustand sind der Verbindungsgruppe zugeordnet, nicht den einzelnen Paketen.</span><span class="sxs-lookup"><span data-stu-id="6a9d3-108">The virtual environment and its current state are associated with the connection group, not with the individual packages.</span></span> <span data-ttu-id="6a9d3-109">Wenn ein App-V-Paket aus der Verbindungsgruppe entfernt wird, wird der Zustand, der als Teil der Verbindungsgruppe vorhanden war, nicht mit dem Paket migriert.</span><span class="sxs-lookup"><span data-stu-id="6a9d3-109">If an App-V package is removed from the connection group, the state that existed as part of the connection group will not migrate with the package.</span></span>

<span data-ttu-id="6a9d3-110">Wenn das gleiche Paket Bestandteil von zwei verschiedenen Verbindungsgruppen ist, müssen Sie angeben, welche Verbindungsgruppe App-V verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="6a9d3-110">If the same package is a part of two different connection groups, you have to indicate which connection group App-V should use.</span></span> <span data-ttu-id="6a9d3-111">So können Sie beispielsweise zwei Pakete in einer Verbindungsgruppe haben, die jeweils denselben Registrierungs-DWORD-Wert definieren.</span><span class="sxs-lookup"><span data-stu-id="6a9d3-111">For example, you might have two packages in a connection group that each define the same registry DWORD value.</span></span>

<span data-ttu-id="6a9d3-112">Die verwendete Verbindungsgruppe basiert auf der Reihenfolge, in der ein Paket im **AppConnectionGroup** -XML-Dokument angezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="6a9d3-112">The connection group that is used is based on the order in which a package appears inside the **AppConnectionGroup** XML document:</span></span>

-   <span data-ttu-id="6a9d3-113">Das erste Paket hat die höchste Priorität.</span><span class="sxs-lookup"><span data-stu-id="6a9d3-113">The first package has the highest precedence.</span></span>

-   <span data-ttu-id="6a9d3-114">Das zweite Paket hat die zweithöchste Priorität.</span><span class="sxs-lookup"><span data-stu-id="6a9d3-114">The second package has the second highest precedence.</span></span>

<span data-ttu-id="6a9d3-115">Sehen Sie sich den folgenden Beispielabschnitt an:</span><span class="sxs-lookup"><span data-stu-id="6a9d3-115">Consider the following example section:</span></span>

```xml
<appv:Packages><appv:PackagePackageId="A8731008-4523-4713-83A4-CD1363907160"VersionId="E889951B-7F30-418B-A69C-B37283BC0DB9"/><appv:PackagePackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"VersionId="01F1943B-C778-40AD-BFAD-AC34A695DF3C"/><appv:PackagePackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"/></appv:Packages>
```

<span data-ttu-id="6a9d3-116">Angenommen, derselbe DWORD-Wert ABC (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region) wird im ersten und dritten Paket definiert, beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="6a9d3-116">Assume that same DWORD value ABC (HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region) is defined in the first and third package, such as:</span></span>

-   <span data-ttu-id="6a9d3-117">Paket 1 (A8731008-4523-4713-83A4-CD1363907160): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5</span><span class="sxs-lookup"><span data-stu-id="6a9d3-117">Package 1 (A8731008-4523-4713-83A4-CD1363907160): HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region=5</span></span>

-   <span data-ttu-id="6a9d3-118">Paket 3 (04220DCA-EE77-42BE-A9F5-96FD8E8593F2): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 10</span><span class="sxs-lookup"><span data-stu-id="6a9d3-118">Package 3 (04220DCA-EE77-42BE-A9F5-96FD8E8593F2): HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region=10</span></span>

<span data-ttu-id="6a9d3-119">Da Paket 1 zuerst angezeigt wird, weist die virtuelle Umgebung des AppConnectionGroup den einzelnen DWORD-Wert 5 auf (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5).</span><span class="sxs-lookup"><span data-stu-id="6a9d3-119">Since Package 1 appears first, the AppConnectionGroup's virtual environment will have the single DWORD value of 5 (HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region=5).</span></span> <span data-ttu-id="6a9d3-120">Das bedeutet, dass die virtuellen Anwendungen in Paket 1, Paket 2 und Paket 3 alle den Wert 5 sehen, wenn Sie eine Abfrage nach HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region.</span><span class="sxs-lookup"><span data-stu-id="6a9d3-120">This means that the virtual applications in Package 1, Package 2, and Package 3 will all see the value 5 when they query for HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region.</span></span>

<span data-ttu-id="6a9d3-121">Andere virtuelle Umgebungs Ressourcen werden in ähnlicher Weise aufgelöst, aber der übliche Fall ist, dass die Kollisionen in der Registrierung auftreten.</span><span class="sxs-lookup"><span data-stu-id="6a9d3-121">Other virtual environment resources are resolved similarly, but the usual case is that the collisions occur in the registry.</span></span>

## <a href="" id="bkmk-merged-root-ve-exp"></a><span data-ttu-id="6a9d3-122">Zusammenführen identischer Paket Pfade zu einem virtuellen Verzeichnis in Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="6a9d3-122">Merging identical package paths into one virtual directory in connection groups</span></span>


<span data-ttu-id="6a9d3-123">Wenn zwei oder mehr Pakete in einer Verbindungsgruppe identische Verzeichnispfade enthalten, werden die Pfade in einem einzigen virtuellen Verzeichnis innerhalb der virtuellen Umgebung der Verbindungsgruppe zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="6a9d3-123">If two or more packages in a connection group contain identical directory paths, the paths are merged into a single virtual directory inside the connection group virtual environment.</span></span> <span data-ttu-id="6a9d3-124">Dieses Zusammenführen von Pfaden ermöglicht es einer Anwendung in einem Paket, auf Dateien zuzugreifen, die in einem anderen Paket enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6a9d3-124">This merging of paths allows an application in one package to access files that are in a different package.</span></span>

<span data-ttu-id="6a9d3-125">Wenn Sie ein Paket aus einer Verbindungsgruppe entfernen, können die Anwendungen in diesem entfernten Paket nicht mehr auf Dateien in den verbleibenden Paketen in der Verbindungsgruppe zugreifen.</span><span class="sxs-lookup"><span data-stu-id="6a9d3-125">When you remove a package from a connection group, the applications in that removed package are no longer able to access files in the remaining packages in the connection group.</span></span>

<span data-ttu-id="6a9d3-126">Die Reihenfolge, in der APP-v den Namen einer Datei in der Verbindungsgruppe nachschlägt, wird in der Reihenfolge angegeben, in der die APP-v-Pakete in der Manifestdatei der Verbindungsgruppe aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="6a9d3-126">The order in which App-V looks up a file’s name in the connection group is specified by the order in which the App-V packages are listed in the connection group manifest file.</span></span>

<span data-ttu-id="6a9d3-127">Das folgende Beispiel zeigt die Reihenfolge und Beziehung einer Dateinamen Suche in einer Verbindungsgruppe für **Paket a** und **Paket B**.</span><span class="sxs-lookup"><span data-stu-id="6a9d3-127">The following example shows the order and relationship of a file name lookup in a connection group for **Package A** and **Package B**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a9d3-128">Paket A</span><span class="sxs-lookup"><span data-stu-id="6a9d3-128">Package A</span></span></th>
<th align="left"><span data-ttu-id="6a9d3-129">Paket B</span><span class="sxs-lookup"><span data-stu-id="6a9d3-129">Package B</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a9d3-130">C:\Windows\System32</span><span class="sxs-lookup"><span data-stu-id="6a9d3-130">C:\Windows\System32</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a9d3-131">C:\Windows\System32</span><span class="sxs-lookup"><span data-stu-id="6a9d3-131">C:\Windows\System32</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a9d3-132">C:\AppTest</span><span class="sxs-lookup"><span data-stu-id="6a9d3-132">C:\AppTest</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a9d3-133">C:\AppTest</span><span class="sxs-lookup"><span data-stu-id="6a9d3-133">C:\AppTest</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6a9d3-134">Wenn in dem obigen Beispiel eine virtualisierte Anwendung versucht, eine bestimmte Datei zu finden, wird Paket a zuerst nach einem übereinstimmenden Dateipfad durchsucht.</span><span class="sxs-lookup"><span data-stu-id="6a9d3-134">In the example above, when a virtualized application tries to find a specific file, Package A is searched first for a matching file path.</span></span> <span data-ttu-id="6a9d3-135">Wenn kein übereinstimmender Pfad gefunden wird, wird Paket B mithilfe der folgenden Zuordnungsregeln durchsucht:</span><span class="sxs-lookup"><span data-stu-id="6a9d3-135">If a matching path is not found, Package B is searched, using the following mapping rules:</span></span>

-   <span data-ttu-id="6a9d3-136">Wenn eine Datei mit dem Namen **test.txt** in der gleichen virtuellen Ordnerhierarchie in beiden Anwendungspaketen vorhanden ist, wird die erste übereinstimmende Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="6a9d3-136">If a file named **test.txt** exists in the same virtual folder hierarchy in both application packages, the first matching file is used.</span></span>

-   <span data-ttu-id="6a9d3-137">Wenn eine Datei mit dem Namen **bar.txt** in der virtuellen Ordnerhierarchie eines Anwendungspakets vorhanden ist, aber nicht im anderen, wird die erste übereinstimmende Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="6a9d3-137">If a file named **bar.txt** exists in the virtual folder hierarchy of one application package, but not in the other, the first matching file is used.</span></span>






## <span data-ttu-id="6a9d3-138">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="6a9d3-138">Related topics</span></span>


[<span data-ttu-id="6a9d3-139">Verwalten von Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="6a9d3-139">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





