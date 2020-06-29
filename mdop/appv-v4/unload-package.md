---
title: UNLOAD PACKAGE
description: UNLOAD PACKAGE
author: dansimp
ms.assetid: a076eb5a-ce3d-49e4-ac7a-4d4df10e3477
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fbee040f97bf5675ace7e873741a4270a993a911
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806191"
---
# <span data-ttu-id="374aa-103">UNLOAD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="374aa-103">UNLOAD PACKAGE</span></span>


<span data-ttu-id="374aa-104">Entladen des Pakets aus dem Dateisystemcache</span><span class="sxs-lookup"><span data-stu-id="374aa-104">Unloads the package from the file system cache.</span></span>

`SFTMIME UNLOAD PACKAGE:package-name [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="374aa-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="374aa-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="374aa-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="374aa-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="374aa-107">Paket: &lt; Package-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="374aa-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="374aa-108">Der Name des zu entladenden Pakets.</span><span class="sxs-lookup"><span data-stu-id="374aa-108">The name of the package to unload.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="374aa-109">/Log</span><span class="sxs-lookup"><span data-stu-id="374aa-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="374aa-110">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="374aa-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="374aa-111">/Console</span><span class="sxs-lookup"><span data-stu-id="374aa-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="374aa-112">Wenn angegeben, wird die Ausgabe im aktiven Konsolenfenster angezeigt (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="374aa-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="374aa-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="374aa-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="374aa-114">Wenn angegeben, wird die Ausgabe in einem Windows-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="374aa-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="374aa-115">Für Version 4.6 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="374aa-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="374aa-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="374aa-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="374aa-117">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</span><span class="sxs-lookup"><span data-stu-id="374aa-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="374aa-118">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="374aa-118">Related topics</span></span>


[<span data-ttu-id="374aa-119">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="374aa-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





