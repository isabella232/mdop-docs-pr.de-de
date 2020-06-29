---
title: CONFIGURE APP
description: CONFIGURE APP
author: dansimp
ms.assetid: fcfb4f86-8b7c-4208-bca3-955fd067079f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 42ff17e180df262deed3fe79674ad6fda6f0be4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807883"
---
# <span data-ttu-id="d459e-103">CONFIGURE APP</span><span class="sxs-lookup"><span data-stu-id="d459e-103">CONFIGURE APP</span></span>


<span data-ttu-id="d459e-104">Ermöglicht es dem Benutzer, das mit einer Anwendung verknüpfte Symbol zu ändern, aber das Symbol für vorhandene Verknüpfungen oder Dateitypzuordnungen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d459e-104">Enables the user to change the icon associated with an application but does not update the icon on existing shortcuts or file type associations.</span></span>

`SFTMIME CONFIGURE APP:application /ICON icon-pathname                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d459e-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="d459e-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="d459e-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d459e-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d459e-107">App: &lt; Anwendung&gt;</span><span class="sxs-lookup"><span data-stu-id="d459e-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="d459e-108">Der Name und die Version (optional) der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d459e-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d459e-109">/Icon &lt; -Symbolpfadname&gt;</span><span class="sxs-lookup"><span data-stu-id="d459e-109">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="d459e-110">Der Pfad oder die URL für die Symboldatei.</span><span class="sxs-lookup"><span data-stu-id="d459e-110">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d459e-111">/Log</span><span class="sxs-lookup"><span data-stu-id="d459e-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="d459e-112">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="d459e-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d459e-113">/Console</span><span class="sxs-lookup"><span data-stu-id="d459e-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="d459e-114">Wenn angegeben, wird die Ausgabe im aktiven Konsolenfenster angezeigt (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="d459e-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d459e-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="d459e-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="d459e-116">Wenn angegeben, wird die Ausgabe in einem Windows-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d459e-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="d459e-117">Für Version 4.6 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d459e-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d459e-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="d459e-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="d459e-119">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</span><span class="sxs-lookup"><span data-stu-id="d459e-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="d459e-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d459e-120">Related topics</span></span>


[<span data-ttu-id="d459e-121">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="d459e-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





