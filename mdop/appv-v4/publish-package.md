---
title: PUBLISH PACKAGE
description: PUBLISH PACKAGE
author: dansimp
ms.assetid: a33e72dd-194f-4283-8e99-4584ab13de53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00b63389986f495d9405939245a50575bae453f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806456"
---
# <span data-ttu-id="7419e-103">PUBLISH PACKAGE</span><span class="sxs-lookup"><span data-stu-id="7419e-103">PUBLISH PACKAGE</span></span>


<span data-ttu-id="7419e-104">Veröffentlicht den Inhalt eines gesamten Pakets.</span><span class="sxs-lookup"><span data-stu-id="7419e-104">Publishes the contents of an entire package.</span></span>

`SFTMIME PUBLISH PACKAGE:package-name /MANIFEST manifest-path [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7419e-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="7419e-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="7419e-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7419e-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7419e-107">Paket: &lt; Package-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="7419e-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="7419e-108">Benutzersicht barer und benutzerfreundlicher Name für das Paket.</span><span class="sxs-lookup"><span data-stu-id="7419e-108">User-visible and user-friendly name for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7419e-109">/Manifest &lt; -Manifest-Pfad&gt;</span><span class="sxs-lookup"><span data-stu-id="7419e-109">/MANIFEST &lt;manifest-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="7419e-110">Der Pfad oder die URL der Manifestdatei, in der die im Paket enthaltenen Anwendungen sowie alle Veröffentlichungsinformationen aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="7419e-110">The path or URL of the manifest file that lists the applications included in the package and all of their publishing information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7419e-111">/Global</span><span class="sxs-lookup"><span data-stu-id="7419e-111">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="7419e-112">Falls vorhanden, ist das Paket für alle Benutzer auf diesem Computer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7419e-112">If present, the package will be available for all users on this computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7419e-113">/Log</span><span class="sxs-lookup"><span data-stu-id="7419e-113">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="7419e-114">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="7419e-114">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7419e-115">/Console</span><span class="sxs-lookup"><span data-stu-id="7419e-115">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="7419e-116">Wenn angegeben, wird die Ausgabe im aktiven Konsolenfenster angezeigt (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="7419e-116">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7419e-117">/GUI</span><span class="sxs-lookup"><span data-stu-id="7419e-117">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="7419e-118">Wenn angegeben, wird die Ausgabe in einem Windows-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7419e-118">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7419e-119">Für Version 4.6 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7419e-119">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7419e-120">/LOGU</span><span class="sxs-lookup"><span data-stu-id="7419e-120">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="7419e-121">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</span><span class="sxs-lookup"><span data-stu-id="7419e-121">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7419e-122">**Wichtig**  Das Paket muss dem Application Virtualization-Client bereits hinzugefügt worden sein, und die Manifestdatei ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7419e-122">**Important** The package must already have been added to the Application Virtualization Client, and the manifest file is required.</span></span>

<span data-ttu-id="7419e-123">Um den Parameter **Global** verwenden zu können, muss der Befehl Paket veröffentlichen als lokaler Administrator ausgeführt werden. Andernfalls werden nur **ManageTypes** -und **PublishShortcut** -Berechtigungen benötigt.</span><span class="sxs-lookup"><span data-stu-id="7419e-123">To use the **GLOBAL** parameter, the PUBLISH PACKAGE command must be run as local Administrator; otherwise, only **ManageTypes** and **PublishShortcut** permissions are needed.</span></span>

<span data-ttu-id="7419e-124">Durch die Veröffentlichung ohne den **globalen** Parameter wird dem Benutzer der Zugriff auf die Anwendungen im Paket gewährt, und die im Manifest aufgelisteten Dateitypen und Verknüpfungen werden im Profil des Benutzers veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="7419e-124">Publishing without the **GLOBAL** parameter grants the user access to the applications in the package and publishes the file types and shortcuts listed in the manifest to the user’s profile.</span></span>

<span data-ttu-id="7419e-125">Durch die Veröffentlichung mit dem Parameter **Global** werden die im Manifest aufgelisteten Dateitypen und Tastenkombinationen dem Profil "alle Benutzer" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7419e-125">Publishing with the **GLOBAL** parameter adds the file types and shortcuts listed in the manifest to the “All Users” profile.</span></span>

<span data-ttu-id="7419e-126">Wenn das Paket nicht global ist, bevor der Anruf und der **globale** Parameter verwendet werden, wird das Paket Global und allen Benutzern zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="7419e-126">If the package is not global before the call and the **GLOBAL** parameter is used, the package is made global and available to all users.</span></span>

 

## <span data-ttu-id="7419e-127">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7419e-127">Related topics</span></span>


[<span data-ttu-id="7419e-128">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="7419e-128">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





