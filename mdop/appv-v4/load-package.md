---
title: LOAD PACKAGE
description: LOAD PACKAGE
author: dansimp
ms.assetid: eb19116d-e5d0-445c-b2f0-3116a09384d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 938aa92696c8530c91d9a7acaac42408de534edc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806627"
---
# <span data-ttu-id="ed953-103">LOAD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="ed953-103">LOAD PACKAGE</span></span>


<span data-ttu-id="ed953-104">Lädt das angegebene Paket in den Dateisystemcache.</span><span class="sxs-lookup"><span data-stu-id="ed953-104">Loads the specified package into the file system cache.</span></span>

`SFTMIME LOAD PACKAGE:package-name [/SFTPATH sft-pathname]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ed953-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed953-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="ed953-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed953-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed953-107">Paket: &lt; Package-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="ed953-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed953-108">Der Name des zu ladenden Pakets.</span><span class="sxs-lookup"><span data-stu-id="ed953-108">The name of the package to load.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ed953-109">/SFTPATH &lt; SFT-Pfadname&gt;</span><span class="sxs-lookup"><span data-stu-id="ed953-109">/SFTPATH &lt;sft-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed953-110">Wenn angegeben, der Pfad zu einer SFT-Datei, aus der geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed953-110">If specified, the path to an SFT file to load from.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed953-111">/Log</span><span class="sxs-lookup"><span data-stu-id="ed953-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed953-112">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="ed953-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ed953-113">/Console</span><span class="sxs-lookup"><span data-stu-id="ed953-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed953-114">Wenn angegeben, wird die Ausgabe im aktiven Konsolenfenster angezeigt (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="ed953-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed953-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="ed953-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed953-116">Wenn angegeben, wird die Ausgabe in einem Windows-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ed953-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ed953-117">Für Version 4.6 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ed953-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed953-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="ed953-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed953-119">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</span><span class="sxs-lookup"><span data-stu-id="ed953-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ed953-120">**Hinweis**  Wenn kein SFTPATH angegeben ist, lädt der Client das Paket unter Verwendung des Pfads, der für die Verwendung konfiguriert wurde, basierend auf der OSD-Datei, dem ApplicationSourceRoot-Registrierungsschlüsselwert oder der OVERRIDEURL-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="ed953-120">**Note** If no SFTPATH is specified, the client will load the package by using the path it has been configured to use, based on the OSD file, the ApplicationSourceRoot registry key value, or the OverrideURL setting.</span></span>

<span data-ttu-id="ed953-121">Der Befehl " **Paket laden** " führt eine synchrone Auslastung aus und ist erst dann abgeschlossen, wenn das Paket vollständig geladen oder auf eine Fehlerbedingung stößt.</span><span class="sxs-lookup"><span data-stu-id="ed953-121">The **LOAD PACKAGE** command performs a synchronous load and will not be complete until the package is fully loaded or until it encounters an error condition.</span></span>

 

## <span data-ttu-id="ed953-122">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ed953-122">Related topics</span></span>


[<span data-ttu-id="ed953-123">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="ed953-123">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





