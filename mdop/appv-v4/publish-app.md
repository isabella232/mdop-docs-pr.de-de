---
title: PUBLISH APP
description: PUBLISH APP
author: dansimp
ms.assetid: f25f06a8-ca23-435b-a0c2-16a5f39b6b97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2ccb19255786ee47a8356feef14be1c4d9b4fb2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806459"
---
# <span data-ttu-id="f7a7d-103">PUBLISH APP</span><span class="sxs-lookup"><span data-stu-id="f7a7d-103">PUBLISH APP</span></span>


<span data-ttu-id="f7a7d-104">Veröffentlicht eine Anwendungsverknüpfung im Startmenü, auf dem Desktop oder an einem anderen angegebenen Speicherort des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="f7a7d-104">Publishes an application shortcut to the user's Start menu, desktop, or other specified location.</span></span>

`SFTMIME PUBLISH APP:application                 {/DESKTOP | /START | /TARGET target-path} [/ICON icon-pathname]                 [/DISPLAY display-name] [/ARGS command-args...]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f7a7d-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7a7d-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="f7a7d-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7a7d-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7a7d-107">Anwendung: &lt; Anwendung&gt;</span><span class="sxs-lookup"><span data-stu-id="f7a7d-107">APPLICATION:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7a7d-108">Der Name und die Version (optional) der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="f7a7d-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f7a7d-109">/Desktop</span><span class="sxs-lookup"><span data-stu-id="f7a7d-109">/DESKTOP</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7a7d-110">Veröffentlicht eine Verknüpfung auf dem Desktop des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="f7a7d-110">Publishes a shortcut to the user's desktop.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7a7d-111">/Start</span><span class="sxs-lookup"><span data-stu-id="f7a7d-111">/START</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7a7d-112">Veröffentlicht eine Verknüpfung im Ordner "Application Virtualization Applications" im Ordner "Programme" des Menüs "Start".</span><span class="sxs-lookup"><span data-stu-id="f7a7d-112">Publishes a shortcut to the Application Virtualization Applications folder in the Programs folder of the Start menu.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f7a7d-113">/Target &lt; -Zielpfad&gt;</span><span class="sxs-lookup"><span data-stu-id="f7a7d-113">/TARGET &lt;target-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7a7d-114">Der absolute Pfad, in dem die Verknüpfung veröffentlicht werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7a7d-114">The absolute path where the shortcut should be published.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7a7d-115">/Icon &lt; -Symbolpfadname&gt;</span><span class="sxs-lookup"><span data-stu-id="f7a7d-115">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7a7d-116">Der Pfad oder die URL für die Symboldatei.</span><span class="sxs-lookup"><span data-stu-id="f7a7d-116">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f7a7d-117">Names &lt; -Anzeigename&gt;</span><span class="sxs-lookup"><span data-stu-id="f7a7d-117">/DISPLAY &lt;display-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7a7d-118">Der Anzeigename für die Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="f7a7d-118">The display name for the shortcut.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7a7d-119">/ARGS &lt; Command-args&gt;</span><span class="sxs-lookup"><span data-stu-id="f7a7d-119">/ARGS &lt;command-args&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7a7d-120">Parameter, die an die Anwendung übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f7a7d-120">Parameters to be passed to the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f7a7d-121">/Log</span><span class="sxs-lookup"><span data-stu-id="f7a7d-121">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7a7d-122">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="f7a7d-122">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7a7d-123">/Console</span><span class="sxs-lookup"><span data-stu-id="f7a7d-123">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7a7d-124">Wenn angegeben, wird die Ausgabe im aktiven Konsolenfenster angezeigt (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="f7a7d-124">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f7a7d-125">/GUI</span><span class="sxs-lookup"><span data-stu-id="f7a7d-125">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7a7d-126">Wenn angegeben, wird die Ausgabe in einem Windows-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f7a7d-126">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f7a7d-127">Für Version 4.6 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f7a7d-127">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7a7d-128">/LOGU</span><span class="sxs-lookup"><span data-stu-id="f7a7d-128">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7a7d-129">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</span><span class="sxs-lookup"><span data-stu-id="f7a7d-129">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f7a7d-130">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="f7a7d-130">Related topics</span></span>


[<span data-ttu-id="f7a7d-131">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="f7a7d-131">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





