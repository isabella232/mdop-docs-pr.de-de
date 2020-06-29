---
title: DELETE PACKAGE
description: DELETE PACKAGE
author: dansimp
ms.assetid: 8f7a4598-610d-490e-a224-426acce01a9f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0051967ca308e88d143b8116330f5d770d6086d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808911"
---
# <span data-ttu-id="05995-103">DELETE PACKAGE</span><span class="sxs-lookup"><span data-stu-id="05995-103">DELETE PACKAGE</span></span>


<span data-ttu-id="05995-104">Entfernt einen paketdatensatz und die zugehörigen Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="05995-104">Removes a package record and the applications associated with it.</span></span>

`SFTMIME DELETE PACKAGE:package-name                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="05995-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="05995-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="05995-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05995-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="05995-107">Paket: &lt; Package-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="05995-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="05995-108">Der Name des zu entfernende Pakets.</span><span class="sxs-lookup"><span data-stu-id="05995-108">The name of the package to be removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="05995-109">/Log</span><span class="sxs-lookup"><span data-stu-id="05995-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="05995-110">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="05995-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="05995-111">/Console</span><span class="sxs-lookup"><span data-stu-id="05995-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="05995-112">Wenn angegeben, wird die Ausgabe im aktiven Konsolenfenster angezeigt (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="05995-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="05995-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="05995-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="05995-114">Wenn angegeben, wird die Ausgabe in einem Windows-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="05995-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="05995-115">Für Version 4.6 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="05995-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="05995-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="05995-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="05995-117">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</span><span class="sxs-lookup"><span data-stu-id="05995-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="05995-118">**Wichtig**  Der Befehl "Paket löschen" führt immer eine globale Löschung des Pakets durch und löscht nur globale Dateitypen und Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="05995-118">**Important** The DELETE PACKAGE command always performs a global delete of the package and deletes only global file types and shortcuts.</span></span>

<span data-ttu-id="05995-119">Wenn das Paket Global ist, muss dieser Befehl als lokaler Administrator ausgeführt werden. Andernfalls ist nur **DeleteApp** -Berechtigung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="05995-119">If the package is global, this command must be run as local Administrator; otherwise, only **DeleteApp** permission is needed.</span></span>

 

## <span data-ttu-id="05995-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="05995-120">Related topics</span></span>


[<span data-ttu-id="05995-121">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="05995-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





