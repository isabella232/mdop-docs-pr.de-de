---
title: UNPUBLISH PACKAGE
description: UNPUBLISH PACKAGE
author: dansimp
ms.assetid: 1651427c-72a5-4701-bb57-71e14a7a3803
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7704fb3ed03be4864a837767d9e890d28b63f175
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806184"
---
# <span data-ttu-id="b20b7-103">UNPUBLISH PACKAGE</span><span class="sxs-lookup"><span data-stu-id="b20b7-103">UNPUBLISH PACKAGE</span></span>


<span data-ttu-id="b20b7-104">Ermöglicht Ihnen, die Verknüpfungen und Dateitypen für ein gesamtes Paket zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="b20b7-104">Enables you to remove the shortcuts and file types for an entire package.</span></span>

`SFTMIME UNPUBLISH PACKAGE:package-name [/CLEAR] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b20b7-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="b20b7-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="b20b7-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b20b7-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b20b7-107">Paket: &lt; Package-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="b20b7-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="b20b7-108">Der Name des Pakets.</span><span class="sxs-lookup"><span data-stu-id="b20b7-108">The name of the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b20b7-109">/Clear</span><span class="sxs-lookup"><span data-stu-id="b20b7-109">/CLEAR</span></span></p></td>
<td align="left"><p><span data-ttu-id="b20b7-110">Falls vorhanden, werden die Benutzereinstellungen ebenfalls entfernt.</span><span class="sxs-lookup"><span data-stu-id="b20b7-110">If present, user settings will also be removed.</span></span> <span data-ttu-id="b20b7-111">(Weitere Informationen finden Sie weiter unten in diesem Thema unter wichtige Hinweise.)</span><span class="sxs-lookup"><span data-stu-id="b20b7-111">(For more information, see the Important note later in this topic.)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b20b7-112">/Global</span><span class="sxs-lookup"><span data-stu-id="b20b7-112">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="b20b7-113">Falls vorhanden, wird das Paket für alle Benutzer auf diesem Computer unveröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="b20b7-113">If present, the package will be unpublished for all users on this computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b20b7-114">/Log</span><span class="sxs-lookup"><span data-stu-id="b20b7-114">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="b20b7-115">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="b20b7-115">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b20b7-116">/Console</span><span class="sxs-lookup"><span data-stu-id="b20b7-116">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="b20b7-117">Wenn angegeben, wird die Ausgabe im aktiven Konsolenfenster angezeigt (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="b20b7-117">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b20b7-118">/GUI</span><span class="sxs-lookup"><span data-stu-id="b20b7-118">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="b20b7-119">Wenn angegeben, wird die Ausgabe in einem Windows-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b20b7-119">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b20b7-120">Für Version 4.6 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b20b7-120">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b20b7-121">/LOGU</span><span class="sxs-lookup"><span data-stu-id="b20b7-121">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="b20b7-122">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</span><span class="sxs-lookup"><span data-stu-id="b20b7-122">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b20b7-123">**Wichtig**  Bevor Sie den Befehl " **Paket veröffentlichen** " ausführen können, muss das Paket bereits dem Application Virtualization-Client hinzugefügt worden sein.</span><span class="sxs-lookup"><span data-stu-id="b20b7-123">**Important** Before you can run the **UNPUBLISH PACKAGE** command, the package must already have been added to the Application Virtualization Client.</span></span>

<span data-ttu-id="b20b7-124">Zur Verwendung von " **Global**" muss " **veröffentlichungspaket** aufheben" als lokaler Administrator ausgeführt werden. Andernfalls ist nur **ClearApp** -Berechtigung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b20b7-124">To use **GLOBAL**, **UNPUBLISH PACKAGE** must be run as local Administrator; otherwise, only **ClearApp** permission is needed.</span></span>

<span data-ttu-id="b20b7-125">Bei Verwendung von "nicht **veröffentlichen** " mit " **Global** " werden alle globalen Dateitypen und Tastenkombinationen für das Paket entfernt.</span><span class="sxs-lookup"><span data-stu-id="b20b7-125">Using **UNPUBLISH PACKAGE** with **GLOBAL** removes any global file types and shortcuts for the package.</span></span> <span data-ttu-id="b20b7-126">**Clear** ist nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="b20b7-126">**CLEAR** is not applicable.</span></span>

<span data-ttu-id="b20b7-127">Bei Verwendung von " **UNPUBLISH-Paket** ohne **Global** " werden die Benutzer Verknüpfungen und Dateitypen für das Paket entfernt, und wenn **Clear** festgesetzt ist, werden auch Benutzereinstellungen entfernt und Hintergrund Lasten unter dem Kontext des Benutzers angehalten.</span><span class="sxs-lookup"><span data-stu-id="b20b7-127">Using **UNPUBLISH PACKAGE** without **GLOBAL** removes the user shortcuts and file types for the package and, if **CLEAR** is set, also removes user settings and stops background loads under the user’s context.</span></span>

<span data-ttu-id="b20b7-128">Das **Paket "Veröffentlichung** aufheben" funktioniert in Anwendungen mit dem gleichen Paketnamen oder der gleichen GUID, die als Quell-ID für das **Add**-, **Edit**-und **Publish-Paket**verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="b20b7-128">**UNPUBLISH PACKAGE** works on applications from the same package name or GUID that was used as the source ID for **ADD**, **EDIT**, and **PUBLISH PACKAGE**.</span></span>

<span data-ttu-id="b20b7-129">Das **Paket "Veröffentlichung** aufheben" löscht immer alle Benutzereinstellungen, Verknüpfungen und Dateitypen, unabhängig von der Verwendung des/Clear-Schalters.</span><span class="sxs-lookup"><span data-stu-id="b20b7-129">**UNPUBLISH PACKAGE** always clears all the user settings, shortcuts, and file types regardless of the use of the /CLEAR switch.</span></span>

 

## <span data-ttu-id="b20b7-130">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b20b7-130">Related topics</span></span>


[<span data-ttu-id="b20b7-131">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="b20b7-131">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





