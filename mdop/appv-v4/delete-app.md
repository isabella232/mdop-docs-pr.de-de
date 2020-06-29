---
title: DELETE APP
description: DELETE APP
author: dansimp
ms.assetid: 2f89c0c0-373b-4389-a26d-67b3f9712957
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c27c70ef3227ebaf6b16bcb1fbb4b4e65b7cb7f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808923"
---
# <span data-ttu-id="96fc8-103">DELETE APP</span><span class="sxs-lookup"><span data-stu-id="96fc8-103">DELETE APP</span></span>


<span data-ttu-id="96fc8-104">Entfernt einen Anwendungseintrag aus dem Dateisystemcache, damit er nicht mehr angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="96fc8-104">Removes an application record from the file system cache to make it no longer visible.</span></span> <span data-ttu-id="96fc8-105">Die Verknüpfungen und Dateitypzuordnungen von Benutzern werden ausgeblendet, aber nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="96fc8-105">Users’ shortcuts and file type associations are hidden but not deleted.</span></span> <span data-ttu-id="96fc8-106">Es werden keine Benutzereinstellungen entfernt.</span><span class="sxs-lookup"><span data-stu-id="96fc8-106">No user settings are removed.</span></span>

`SFTMIME DELETE APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="96fc8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="96fc8-107">Parameter</span></span></th>
<th align="left"><span data-ttu-id="96fc8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96fc8-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="96fc8-109">App: &lt; Anwendung&gt;</span><span class="sxs-lookup"><span data-stu-id="96fc8-109">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="96fc8-110">Der Name und die Version (optional) der zu entfernende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="96fc8-110">The name and version (optional) of the application to be removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="96fc8-111">/Log</span><span class="sxs-lookup"><span data-stu-id="96fc8-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="96fc8-112">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="96fc8-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="96fc8-113">/Console</span><span class="sxs-lookup"><span data-stu-id="96fc8-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="96fc8-114">Wenn angegeben, wird die Ausgabe im aktiven Konsolenfenster angezeigt (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="96fc8-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="96fc8-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="96fc8-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="96fc8-116">Wenn angegeben, wird die Ausgabe in einem Windows-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="96fc8-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="96fc8-117">Für Version 4.6 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="96fc8-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="96fc8-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="96fc8-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="96fc8-119">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</span><span class="sxs-lookup"><span data-stu-id="96fc8-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="96fc8-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="96fc8-120">Related topics</span></span>


[<span data-ttu-id="96fc8-121">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="96fc8-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





