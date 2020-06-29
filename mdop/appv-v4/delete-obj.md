---
title: DELETE OBJ
description: DELETE OBJ
author: dansimp
ms.assetid: fb17a261-f378-4ce6-a538-ab2f0ada0f2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d74fc1ac098d7dc4dd2f28633e9ca58d4211d74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808914"
---
# <span data-ttu-id="18949-103">DELETE OBJ</span><span class="sxs-lookup"><span data-stu-id="18949-103">DELETE OBJ</span></span>


<span data-ttu-id="18949-104">Entfernt alle Anwendungsdatensätze.</span><span class="sxs-lookup"><span data-stu-id="18949-104">Removes all of your application records.</span></span>

`SFTMIME DELETE OBJ:APP [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="18949-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="18949-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="18949-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18949-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18949-107">/Global</span><span class="sxs-lookup"><span data-stu-id="18949-107">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="18949-108">Wenn angegeben, werden alle Anwendungen entfernt.</span><span class="sxs-lookup"><span data-stu-id="18949-108">If specified, all applications are removed.</span></span> <span data-ttu-id="18949-109">Standardmäßig werden nur Anwendungen entfernt, auf die der aktuelle Benutzer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="18949-109">By default, only applications the current user has access to are removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18949-110">/Log</span><span class="sxs-lookup"><span data-stu-id="18949-110">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="18949-111">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="18949-111">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18949-112">/Console</span><span class="sxs-lookup"><span data-stu-id="18949-112">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="18949-113">Wenn angegeben, wird die Ausgabe im aktiven Konsolenfenster angezeigt (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="18949-113">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18949-114">/GUI</span><span class="sxs-lookup"><span data-stu-id="18949-114">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="18949-115">Wenn angegeben, wird die Ausgabe in einem Windows-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="18949-115">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="18949-116">Für Version 4.6 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="18949-116">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18949-117">/LOGU</span><span class="sxs-lookup"><span data-stu-id="18949-117">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="18949-118">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</span><span class="sxs-lookup"><span data-stu-id="18949-118">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="18949-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="18949-119">Related topics</span></span>


[<span data-ttu-id="18949-120">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="18949-120">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





