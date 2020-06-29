---
title: ADD APP
description: ADD APP
author: dansimp
ms.assetid: 329fd0c8-a795-49be-b0fd-1367c5b4a34b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ac83c0cf130e8de1d34d42d74e946716e4503246
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808091"
---
# <span data-ttu-id="0f3d5-103">ADD APP</span><span class="sxs-lookup"><span data-stu-id="0f3d5-103">ADD APP</span></span>


<span data-ttu-id="0f3d5-104">Fügt einen Anwendungseintrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="0f3d5-104">Adds an application record.</span></span>

`SFTMIME ADD APP:application /OSD osd-pathname [/ICON icon-pathname] [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0f3d5-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f3d5-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="0f3d5-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f3d5-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0f3d5-107">App: &lt; Anwendung&gt;</span><span class="sxs-lookup"><span data-stu-id="0f3d5-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f3d5-108">Der Name und die Version (optional) der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0f3d5-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0f3d5-109">/OSD &lt; OSD-Pfadname&gt;</span><span class="sxs-lookup"><span data-stu-id="0f3d5-109">/OSD &lt;osd-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f3d5-110">Der Pfad oder die URL für die OSD-Datei.</span><span class="sxs-lookup"><span data-stu-id="0f3d5-110">The path or URL for the OSD file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0f3d5-111">/Icon &lt; -Symbolpfadname&gt;</span><span class="sxs-lookup"><span data-stu-id="0f3d5-111">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f3d5-112">Der Pfad oder die URL für die Symboldatei.</span><span class="sxs-lookup"><span data-stu-id="0f3d5-112">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0f3d5-113">/Log</span><span class="sxs-lookup"><span data-stu-id="0f3d5-113">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f3d5-114">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="0f3d5-114">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0f3d5-115">/Console</span><span class="sxs-lookup"><span data-stu-id="0f3d5-115">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f3d5-116">Wenn angegeben, wird die Ausgabe im aktiven Konsolenfenster angezeigt (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="0f3d5-116">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0f3d5-117">/GUI</span><span class="sxs-lookup"><span data-stu-id="0f3d5-117">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f3d5-118">Wenn angegeben, wird die Ausgabe in einem Windows-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0f3d5-118">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="0f3d5-119">Für Version 4.6 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0f3d5-119">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0f3d5-120">/LOGU</span><span class="sxs-lookup"><span data-stu-id="0f3d5-120">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f3d5-121">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</span><span class="sxs-lookup"><span data-stu-id="0f3d5-121">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="0f3d5-122">**Hinweis**  Der resultierende Name der Anwendung wird aus der OSD-Datei und nicht aus dem in App: Application angegebenen Namen &lt; übernommen &gt; .</span><span class="sxs-lookup"><span data-stu-id="0f3d5-122">**Note** The resulting name of the application will be taken from the OSD file and not from the name provided in APP:&lt;application&gt;.</span></span>

 

## <span data-ttu-id="0f3d5-123">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="0f3d5-123">Related topics</span></span>


[<span data-ttu-id="0f3d5-124">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="0f3d5-124">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





