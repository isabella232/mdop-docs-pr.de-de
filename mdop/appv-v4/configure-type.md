---
title: CONFIGURE TYPE
description: CONFIGURE TYPE
author: dansimp
ms.assetid: 2caf9433-5449-486f-ab94-83ee8e44d7f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b70cdd1b27eba0109183f1eb9cfb42f08b3f341
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809055"
---
# <span data-ttu-id="60de0-103">CONFIGURE TYPE</span><span class="sxs-lookup"><span data-stu-id="60de0-103">CONFIGURE TYPE</span></span>


<span data-ttu-id="60de0-104">Ermöglicht es dem Benutzer, Einstellungen für eine Dateitypzuordnung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="60de0-104">Enables the user to change settings for a file type association.</span></span>

`SFTMIME CONFIGURE TYPE:file-extension [/GLOBAL] [/APP application]                 [/ICON icon-pathname] [/DESCRIPTION type-desc]                 [/CONTENT-TYPE content-type] [/PERCEIVED-TYPE perceived-type]                 [/PROGID progid] [/CONFIRMOPEN {YES|NO}]                 [/SHOWEXT {YES|NO}] [/NEWMENU {YES|NO}]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="60de0-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="60de0-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="60de0-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60de0-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="60de0-107">Typ: &lt; Dateierweiterung&gt;</span><span class="sxs-lookup"><span data-stu-id="60de0-107">TYPE:&lt;file-extension&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="60de0-108">Die Dateinamenerweiterung, die konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="60de0-108">The file name extension to be configured.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="60de0-109">/APP- &lt; Anwendung&gt;</span><span class="sxs-lookup"><span data-stu-id="60de0-109">/APP &lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="60de0-110">Der Name und die Version (optional) der Anwendung, der dieser Dateityp zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="60de0-110">The name and version (optional) of the application to associate this file type with.</span></span> <span data-ttu-id="60de0-111">Kann nicht mit ProgID angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="60de0-111">Cannot be specified with PROGID.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="60de0-112">/Icon &lt; -Symbolpfadname&gt;</span><span class="sxs-lookup"><span data-stu-id="60de0-112">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="60de0-113">Der Pfad oder die URL für die Symboldatei.</span><span class="sxs-lookup"><span data-stu-id="60de0-113">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="60de0-114">/Description &lt; -Typ-DESC&gt;</span><span class="sxs-lookup"><span data-stu-id="60de0-114">/DESCRIPTION &lt;type-desc&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="60de0-115">Der benutzerfreundliche Name für den Dateityp.</span><span class="sxs-lookup"><span data-stu-id="60de0-115">The user-friendly name for the file type.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="60de0-116">/Content-Type &lt; -Inhaltstyp&gt;</span><span class="sxs-lookup"><span data-stu-id="60de0-116">/CONTENT-TYPE &lt;content-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="60de0-117">Der Inhaltstyp der Datei.</span><span class="sxs-lookup"><span data-stu-id="60de0-117">The content type of the file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="60de0-118">/Global</span><span class="sxs-lookup"><span data-stu-id="60de0-118">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="60de0-119">Gibt an, dass die Zuordnung, die für alle Benutzer gilt, geändert werden soll, nicht die benutzerspezifische.</span><span class="sxs-lookup"><span data-stu-id="60de0-119">If present, indicates that the association that applies to all users should be edited, not the user-specific one.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="60de0-120">/Perceived-Type &lt; wahrgenommen-Typ&gt;</span><span class="sxs-lookup"><span data-stu-id="60de0-120">/PERCEIVED-TYPE &lt;perceived-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="60de0-121">Der wahrgenommene Typ der Datei.</span><span class="sxs-lookup"><span data-stu-id="60de0-121">The perceived type of the file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="60de0-122">/ProgID- &lt; ProgID&gt;</span><span class="sxs-lookup"><span data-stu-id="60de0-122">/PROGID &lt;progid&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="60de0-123">Gibt an, dass die Erweiterung einem anderen Dateityp zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="60de0-123">Indicates that the extension should be associated with a different file type.</span></span> <span data-ttu-id="60de0-124">Der vorherige Dateityp wird nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="60de0-124">The previous file type is not deleted.</span></span> <span data-ttu-id="60de0-125">Kann nicht mit app, Icon, Description, CONFIRMOPEN oder SHOWEXT angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="60de0-125">Cannot be specified with APP, ICON, DESCRIPTION, CONFIRMOPEN, or SHOWEXT.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="60de0-126">/CONFIRMOPEN</span><span class="sxs-lookup"><span data-stu-id="60de0-126">/CONFIRMOPEN</span></span></p></td>
<td align="left"><p><span data-ttu-id="60de0-127">Gibt an, ob Benutzer, die eine Datei dieses Typs herunterladen, aufgefordert werden, die Datei zu öffnen oder zu speichern.</span><span class="sxs-lookup"><span data-stu-id="60de0-127">Indicates whether users downloading a file of this type should be asked whether to open or save the file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="60de0-128">/SHOWEXT</span><span class="sxs-lookup"><span data-stu-id="60de0-128">/SHOWEXT</span></span></p></td>
<td align="left"><p><span data-ttu-id="60de0-129">Gibt an, ob die Dateierweiterung immer angezeigt werden soll, auch wenn der Benutzer angefordert hat, dass alle Erweiterungen ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="60de0-129">Indicates whether the file's extension should always be shown, even if the user has requested that all extensions be hidden.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="60de0-130">/NEWMENU</span><span class="sxs-lookup"><span data-stu-id="60de0-130">/NEWMENU</span></span></p></td>
<td align="left"><p><span data-ttu-id="60de0-131">Gibt an, ob dem neuen Menü der Shell ein Eintrag hinzugefügt werden soll <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="60de0-131">Indicates whether an entry should be added to the shell's <strong>New</strong> menu.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="60de0-132">/Log</span><span class="sxs-lookup"><span data-stu-id="60de0-132">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="60de0-133">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="60de0-133">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="60de0-134">/Console</span><span class="sxs-lookup"><span data-stu-id="60de0-134">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="60de0-135">Wenn angegeben, wird die Ausgabe im aktiven Konsolenfenster angezeigt (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="60de0-135">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="60de0-136">/GUI</span><span class="sxs-lookup"><span data-stu-id="60de0-136">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="60de0-137">Wenn angegeben, wird die Ausgabe in einem Windows-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="60de0-137">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="60de0-138">Für Version 4.6 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="60de0-138">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="60de0-139">/LOGU</span><span class="sxs-lookup"><span data-stu-id="60de0-139">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="60de0-140">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</span><span class="sxs-lookup"><span data-stu-id="60de0-140">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="60de0-141">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="60de0-141">Related topics</span></span>


[<span data-ttu-id="60de0-142">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="60de0-142">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





