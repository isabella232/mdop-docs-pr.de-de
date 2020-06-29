---
title: ADD PACKAGE
description: ADD PACKAGE
author: dansimp
ms.assetid: aa83928d-a234-4395-831e-2a7ef786ff53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 925349ce5bdf041b6a8768b5413692966e1cfc1e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809331"
---
# <span data-ttu-id="29d68-103">ADD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="29d68-103">ADD PACKAGE</span></span>


<span data-ttu-id="29d68-104">Fügt einen Paket Eintrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="29d68-104">Adds a package record.</span></span> <span data-ttu-id="29d68-105">Wenn das Paket bereits vorhanden ist, wird mit diesem Befehl die Konfiguration des vorhandenen Pakets aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="29d68-105">If the package already exists, this command will update the configuration of the existing package.</span></span>

`SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                 [/OVERRIDEURL url [/AUTOLOADONREFRESH] [/AUTOLOADONLOGIN]                 [/AUTOLOADONLAUNCH] [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="29d68-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="29d68-106">Parameter</span></span></th>
<th align="left"><span data-ttu-id="29d68-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29d68-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29d68-108">Paket: &lt; Package-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="29d68-108">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="29d68-109">Benutzersicht barer und benutzerfreundlicher Name für das Paket.</span><span class="sxs-lookup"><span data-stu-id="29d68-109">User-visible and user-friendly name for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29d68-110">/Manifest &lt; -Manifest-Pfad&gt;</span><span class="sxs-lookup"><span data-stu-id="29d68-110">/MANIFEST &lt;manifest-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="29d68-111">Der Pfad der Manifestdatei, in der die im Paket enthaltenen Anwendungen sowie alle Veröffentlichungsinformationen aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="29d68-111">The path of the manifest file that lists the applications included in the package and all of their publishing information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29d68-112">/OVERRIDEURL- &lt; URL&gt;</span><span class="sxs-lookup"><span data-stu-id="29d68-112">/OVERRIDEURL &lt;URL&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="29d68-113">Der Speicherort der SFT-Datei des Pakets.</span><span class="sxs-lookup"><span data-stu-id="29d68-113">The location of the package's SFT file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29d68-114">/AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="29d68-114">/AUTOLOADONREFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="29d68-115">Das Laden des Hintergrunds wird nach einer Veröffentlichungsaktualisierung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29d68-115">Background loading is performed after a publishing refresh.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29d68-116">/AUTOLOADONLOGIN</span><span class="sxs-lookup"><span data-stu-id="29d68-116">/AUTOLOADONLOGIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="29d68-117">Das Laden des Hintergrunds wird durchgeführt, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="29d68-117">Background loading is performed when a user logs in.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29d68-118">/AUTOLOADONLAUNCH</span><span class="sxs-lookup"><span data-stu-id="29d68-118">/AUTOLOADONLAUNCH</span></span></p></td>
<td align="left"><p><span data-ttu-id="29d68-119">Das Laden des Hintergrunds wird ausgeführt, nachdem ein Benutzer eine Anwendung aus dem Paket gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="29d68-119">Background loading is performed after a user starts an application from the package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29d68-120">/AUTOLOADTARGET-Ziel</span><span class="sxs-lookup"><span data-stu-id="29d68-120">/AUTOLOADTARGET target</span></span></p></td>
<td align="left"><p><span data-ttu-id="29d68-121">Gibt an, welche Anwendungen aus dem Paket automatisch geladen werden.</span><span class="sxs-lookup"><span data-stu-id="29d68-121">Indicates which applications from the package will be autoloaded.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29d68-122">Keine</span><span class="sxs-lookup"><span data-stu-id="29d68-122">NONE</span></span></p></td>
<td align="left"><p><span data-ttu-id="29d68-123">Trotz des Vorhandenseins von/AUTOLOADONxxx-Flags wird kein Autoloading durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="29d68-123">No autoloading will be performed, despite the presence of any /AUTOLOADONxxx flags.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29d68-124">Alle</span><span class="sxs-lookup"><span data-stu-id="29d68-124">ALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="29d68-125">Wenn ein automatischer Trigger aktiviert ist, werden alle Anwendungen im Paket in den Cache geladen, unabhängig davon, ob Sie zuvor gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="29d68-125">If an autoload trigger is enabled, all applications in the package will be loaded into cache whether or not they have been previously started.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29d68-126">PREVUSED</span><span class="sxs-lookup"><span data-stu-id="29d68-126">PREVUSED</span></span></p></td>
<td align="left"><p><span data-ttu-id="29d68-127">Wenn ein automatischer Trigger aktiviert ist, wird das Paket geladen, wenn Anwendungen in diesem Paket zuvor von einem Benutzer gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="29d68-127">If an autoload trigger is enabled, the package will load if any applications in this package have previously been started by a user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29d68-128">/Global</span><span class="sxs-lookup"><span data-stu-id="29d68-128">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="29d68-129">Falls vorhanden, ist das Paket für alle Benutzer auf diesem Computer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="29d68-129">If present, the package will be available for all users on this computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29d68-130">/Log</span><span class="sxs-lookup"><span data-stu-id="29d68-130">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="29d68-131">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="29d68-131">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29d68-132">/Console</span><span class="sxs-lookup"><span data-stu-id="29d68-132">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="29d68-133">Wenn angegeben, wird die Ausgabe im aktiven Konsolenfenster angezeigt (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="29d68-133">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29d68-134">/GUI</span><span class="sxs-lookup"><span data-stu-id="29d68-134">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="29d68-135">Wenn angegeben, wird die Ausgabe in einem Windows-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="29d68-135">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="29d68-136">Für Version 4.6 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="29d68-136">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29d68-137">/LOGU</span><span class="sxs-lookup"><span data-stu-id="29d68-137">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="29d68-138">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</span><span class="sxs-lookup"><span data-stu-id="29d68-138">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="29d68-139">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="29d68-139">Related topics</span></span>


[<span data-ttu-id="29d68-140">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="29d68-140">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





