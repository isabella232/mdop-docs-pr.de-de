---
title: UNLOCK APP
description: UNLOCK APP
author: dansimp
ms.assetid: 91fc8ceb-b4f5-4a06-8193-05189f830943
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2ea47191450014856b4a9823728e3e275c7fb4cf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806188"
---
# <span data-ttu-id="2f87a-103">UNLOCK APP</span><span class="sxs-lookup"><span data-stu-id="2f87a-103">UNLOCK APP</span></span>


<span data-ttu-id="2f87a-104">Entsperrt die im Dateisystemcache angegebene Anwendung.</span><span class="sxs-lookup"><span data-stu-id="2f87a-104">Unlocks the application specified in the file system cache.</span></span>

`SFTMIME UNLOCK APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f87a-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f87a-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="2f87a-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f87a-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f87a-107">App: &lt; Anwendung&gt;</span><span class="sxs-lookup"><span data-stu-id="2f87a-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f87a-108">Der Name und die Version (optional) der zu entriegelenden Anwendung.</span><span class="sxs-lookup"><span data-stu-id="2f87a-108">The name and version (optional) of the application to unlock.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f87a-109">/Log</span><span class="sxs-lookup"><span data-stu-id="2f87a-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f87a-110">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="2f87a-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f87a-111">/Console</span><span class="sxs-lookup"><span data-stu-id="2f87a-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f87a-112">Wenn angegeben, wird die Ausgabe im aktiven Konsolenfenster angezeigt (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="2f87a-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f87a-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="2f87a-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f87a-114">Wenn angegeben, wird die Ausgabe in einem Windows-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2f87a-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2f87a-115">Für Version 4.6 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2f87a-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f87a-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="2f87a-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f87a-117">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</span><span class="sxs-lookup"><span data-stu-id="2f87a-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="2f87a-118">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2f87a-118">Related topics</span></span>


[<span data-ttu-id="2f87a-119">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="2f87a-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 




