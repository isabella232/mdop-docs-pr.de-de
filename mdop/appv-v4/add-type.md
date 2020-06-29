---
title: ADD TYPE
description: ADD TYPE
author: dansimp
ms.assetid: 8f1d3978-9977-4851-9f46-fee6aefa3535
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d2dcfb24a32dc733aa91b5534e0011090ef12b9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809322"
---
# <span data-ttu-id="a7f39-103">ADD TYPE</span><span class="sxs-lookup"><span data-stu-id="a7f39-103">ADD TYPE</span></span>


<span data-ttu-id="a7f39-104">Fügt die angegebene Dateitypzuordnung hinzu.</span><span class="sxs-lookup"><span data-stu-id="a7f39-104">Adds the specified file type association.</span></span>

`SFTMIME ADD TYPE:file-extension /APP application [/ICON icon-pathname]                 [/DESCRIPTION type-desc] [/CONTENT-TYPE content-type] [/GLOBAL]                 [/PERCEIVED-TYPE perceived-type] [/PROGID progid]                 [/CONFIRMOPEN {YES|NO}] [/SHOWEXT {YES|NO}]                 [/NEWMENU {YES|NO}]  [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a7f39-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7f39-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="a7f39-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7f39-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7f39-107">Typ: &lt; Dateierweiterung&gt;</span><span class="sxs-lookup"><span data-stu-id="a7f39-107">TYPE:&lt;file-extension&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7f39-108">Die Dateinamenerweiterung, die der angegebenen Anwendung zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="a7f39-108">The file name extension that will be associated with the application specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a7f39-109">/APP- &lt; Anwendung&gt;</span><span class="sxs-lookup"><span data-stu-id="a7f39-109">/APP &lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7f39-110">Der Name und die Version (optional) der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a7f39-110">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7f39-111">/Icon &lt; -Symbolpfadname&gt;</span><span class="sxs-lookup"><span data-stu-id="a7f39-111">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7f39-112">Der Pfad oder die URL für die Symboldatei.</span><span class="sxs-lookup"><span data-stu-id="a7f39-112">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a7f39-113">/Description &lt; -Typ-DESC&gt;</span><span class="sxs-lookup"><span data-stu-id="a7f39-113">/DESCRIPTION &lt;type-desc&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7f39-114">Der benutzerfreundliche Name für den Dateityp.</span><span class="sxs-lookup"><span data-stu-id="a7f39-114">The user-friendly name for the file type.</span></span> <span data-ttu-id="a7f39-115">Standardmäßig wird die &quot; Erweiterungsdatei verwendet.&quot;</span><span class="sxs-lookup"><span data-stu-id="a7f39-115">Defaults to &quot;EXTENSION File.&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7f39-116">/Content-Type &lt; -Inhaltstyp&gt;</span><span class="sxs-lookup"><span data-stu-id="a7f39-116">/CONTENT-TYPE &lt;content-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7f39-117">Der Inhaltstyp der Datei.</span><span class="sxs-lookup"><span data-stu-id="a7f39-117">The content type of the file.</span></span> <span data-ttu-id="a7f39-118">Standardmäßig wird &quot; Application/Softricity-Extension verwendet.&quot;</span><span class="sxs-lookup"><span data-stu-id="a7f39-118">Defaults to &quot;application/softricity-extension.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a7f39-119">/Global</span><span class="sxs-lookup"><span data-stu-id="a7f39-119">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7f39-120">Falls vorhanden, ist das Paket für alle Benutzer auf diesem Computer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a7f39-120">If present, the package will be available for all users on this computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7f39-121">/Perceived-Type &lt; wahrgenommen-Typ&gt;</span><span class="sxs-lookup"><span data-stu-id="a7f39-121">/PERCEIVED-TYPE &lt;perceived-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7f39-122">Der wahrgenommene Typ der Datei.</span><span class="sxs-lookup"><span data-stu-id="a7f39-122">The perceived type of the file.</span></span> <span data-ttu-id="a7f39-123">Der Standardwert ist Nothing.</span><span class="sxs-lookup"><span data-stu-id="a7f39-123">Defaults to nothing.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a7f39-124">/ProgID- &lt; ProgID&gt;</span><span class="sxs-lookup"><span data-stu-id="a7f39-124">/PROGID &lt;progid&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7f39-125">Der programmgesteuerte Bezeichner für den Dateityp.</span><span class="sxs-lookup"><span data-stu-id="a7f39-125">The programmatic identifier for the file type.</span></span> <span data-ttu-id="a7f39-126">Standardmäßig wird die APP virt. Extension. File verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7f39-126">Defaults to App Virt.extension.File.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7f39-127">/CONFIRMOPEN</span><span class="sxs-lookup"><span data-stu-id="a7f39-127">/CONFIRMOPEN</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7f39-128">Gibt an, ob Benutzer, die eine Datei dieses Typs herunterladen, aufgefordert werden, die Datei zu öffnen oder zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a7f39-128">Indicates whether users downloading a file of this type should be asked whether to open or save the file.</span></span> <span data-ttu-id="a7f39-129">Standardwert ist "Ja".</span><span class="sxs-lookup"><span data-stu-id="a7f39-129">Defaults to YES.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a7f39-130">/SHOWEXT</span><span class="sxs-lookup"><span data-stu-id="a7f39-130">/SHOWEXT</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7f39-131">Gibt an, ob die Dateierweiterung immer angezeigt werden soll, auch wenn der Benutzer angefordert hat, dass alle Erweiterungen ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="a7f39-131">Indicates whether the file's extension should always be shown, even if the user has requested that all extensions be hidden.</span></span> <span data-ttu-id="a7f39-132">Standardmäßig auf Nein.</span><span class="sxs-lookup"><span data-stu-id="a7f39-132">Defaults to NO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7f39-133">/NEWMENU</span><span class="sxs-lookup"><span data-stu-id="a7f39-133">/NEWMENU</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7f39-134">Gibt an, ob dem neuen Menü der Shell ein Eintrag hinzugefügt werden soll <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="a7f39-134">Indicates whether an entry should be added to the shell's <strong>New</strong> menu.</span></span> <span data-ttu-id="a7f39-135">Standardmäßig auf Nein.</span><span class="sxs-lookup"><span data-stu-id="a7f39-135">Defaults to NO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a7f39-136">/Log</span><span class="sxs-lookup"><span data-stu-id="a7f39-136">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7f39-137">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="a7f39-137">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7f39-138">/Console</span><span class="sxs-lookup"><span data-stu-id="a7f39-138">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7f39-139">Wenn angegeben, wird die Ausgabe im aktiven Konsolenfenster angezeigt (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="a7f39-139">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a7f39-140">/GUI</span><span class="sxs-lookup"><span data-stu-id="a7f39-140">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7f39-141">Wenn angegeben, wird die Ausgabe in einem Windows-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a7f39-141">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a7f39-142">Für Version 4.6 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a7f39-142">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7f39-143">/LOGU</span><span class="sxs-lookup"><span data-stu-id="a7f39-143">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7f39-144">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</span><span class="sxs-lookup"><span data-stu-id="a7f39-144">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="a7f39-145">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a7f39-145">Related topics</span></span>


[<span data-ttu-id="a7f39-146">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="a7f39-146">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





