---
title: DELETE TYPE
description: DELETE TYPE
author: dansimp
ms.assetid: f2852723-c894-49f3-a3c5-56f9648bb9ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0df68c0a0efcd0e269410d1580f7b0a82301c46d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808905"
---
# <span data-ttu-id="800b8-103">DELETE TYPE</span><span class="sxs-lookup"><span data-stu-id="800b8-103">DELETE TYPE</span></span>


<span data-ttu-id="800b8-104">Entfernt die angegebene Dateitypzuordnung.</span><span class="sxs-lookup"><span data-stu-id="800b8-104">Removes the specified file type association.</span></span>

`SFTMIME DELETE TYPE:file-extension [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="800b8-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="800b8-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="800b8-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="800b8-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="800b8-107">Typ: &lt; Dateierweiterung&gt;</span><span class="sxs-lookup"><span data-stu-id="800b8-107">TYPE:&lt;file-extension&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="800b8-108">Die Dateinamenerweiterung, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="800b8-108">The file name extension to be removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="800b8-109">/Global</span><span class="sxs-lookup"><span data-stu-id="800b8-109">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="800b8-110">Gibt bei Angabe an, dass die globale Zuordnung für die Dateinamenerweiterung entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="800b8-110">If specified, indicates that the global association for the file name extension should be removed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="800b8-111">/Log</span><span class="sxs-lookup"><span data-stu-id="800b8-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="800b8-112">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="800b8-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="800b8-113">/Console</span><span class="sxs-lookup"><span data-stu-id="800b8-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="800b8-114">Wenn angegeben, wird die Ausgabe im aktiven Konsolenfenster angezeigt (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="800b8-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="800b8-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="800b8-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="800b8-116">Wenn angegeben, wird die Ausgabe in einem Windows-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="800b8-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="800b8-117">Für Version 4.6 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="800b8-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="800b8-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="800b8-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="800b8-119">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</span><span class="sxs-lookup"><span data-stu-id="800b8-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="800b8-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="800b8-120">Related topics</span></span>


[<span data-ttu-id="800b8-121">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="800b8-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





