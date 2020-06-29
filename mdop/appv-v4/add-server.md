---
title: ADD SERVER
description: ADD SERVER
author: dansimp
ms.assetid: 4be2ac2e-a410-4711-9f84-f305393c8fa7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e15a5943b40e14b2f9031bf8b3ddffa693e32dea
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808087"
---
# <span data-ttu-id="bb4c2-103">ADD SERVER</span><span class="sxs-lookup"><span data-stu-id="bb4c2-103">ADD SERVER</span></span>


<span data-ttu-id="bb4c2-104">Fügt einen Veröffentlichungsserver hinzu.</span><span class="sxs-lookup"><span data-stu-id="bb4c2-104">Adds a publishing server.</span></span>

`SFTMIME ADD SERVER:server-name /HOST hostname /TYPE {HTTP|RTSP}                 /PATH path [/PORT port] [/REFRESH {ON|OFF}] [/SECURE]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bb4c2-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb4c2-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="bb4c2-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb4c2-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bb4c2-107">Server: &lt; Servername&gt;</span><span class="sxs-lookup"><span data-stu-id="bb4c2-107">SERVER:&lt;server-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="bb4c2-108">Der Anzeigename für den Veröffentlichungsserver.</span><span class="sxs-lookup"><span data-stu-id="bb4c2-108">The display name for the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bb4c2-109">/Host &lt; Hostname&gt;</span><span class="sxs-lookup"><span data-stu-id="bb4c2-109">/HOST &lt;hostname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="bb4c2-110">Der Hostname oder die IP-Adresse des Veröffentlichungsservers.</span><span class="sxs-lookup"><span data-stu-id="bb4c2-110">The host name or IP address for the publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bb4c2-111">/Type {http | RTSP</span><span class="sxs-lookup"><span data-stu-id="bb4c2-111">/TYPE {HTTP|RTSP}</span></span></p></td>
<td align="left"><p><span data-ttu-id="bb4c2-112">Gibt an, ob es sich bei dem Veröffentlichungsserver um einen Webserver ( &quot; http &quot; ) oder einen Application Virtualization Server ( &quot; RTSP &quot; ) handelt.</span><span class="sxs-lookup"><span data-stu-id="bb4c2-112">Indicates whether the publishing server is a Web server (&quot;HTTP&quot;) or an Application Virtualization Server (&quot;RTSP&quot;).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bb4c2-113">/Port- &lt; Port&gt;</span><span class="sxs-lookup"><span data-stu-id="bb4c2-113">/PORT &lt;port&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="bb4c2-114">Der Port, auf dem der Veröffentlichungsserver lauscht.</span><span class="sxs-lookup"><span data-stu-id="bb4c2-114">The port on which the publishing server listens.</span></span> <span data-ttu-id="bb4c2-115">Standardmäßig wird 80 für normale HTTP-Server, 443 für http-Server mit erweiterter Sicherheit, 554 für normale Application Virtualization-Server und 322 für Server mit erweiterter Sicherheit verwendet.</span><span class="sxs-lookup"><span data-stu-id="bb4c2-115">Defaults to 80 for normal HTTP servers, 443 for HTTP servers using enhanced security, 554 for normal Application Virtualization Servers, and 322 for servers using enhanced security.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bb4c2-116">/Path- &lt; Pfad&gt;</span><span class="sxs-lookup"><span data-stu-id="bb4c2-116">/PATH &lt;path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="bb4c2-117">Der Pfadabschnitt der in einer Veröffentlichungsanforderung verwendeten URL.</span><span class="sxs-lookup"><span data-stu-id="bb4c2-117">The path portion of the URL used in a publishing request.</span></span> <span data-ttu-id="bb4c2-118">Wenn der Parameter Type auf RTSP eingestellt ist, ist der Pfad optional und standardmäßig auf &quot; / &quot; .</span><span class="sxs-lookup"><span data-stu-id="bb4c2-118">If the TYPE parameter is set to RTSP, the path is optional and defaults to &quot;/&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bb4c2-119">/Refresh</span><span class="sxs-lookup"><span data-stu-id="bb4c2-119">/REFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="bb4c2-120">Wenn die Einstellung auf ein gesetzt ist, werden Veröffentlichungsinformationen aktualisiert, wenn sich der Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="bb4c2-120">If set to ON, publishing information will be refreshed when the user logs in.</span></span> <span data-ttu-id="bb4c2-121">Standardmäßig auf ein.</span><span class="sxs-lookup"><span data-stu-id="bb4c2-121">Defaults to ON.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bb4c2-122">/Secure</span><span class="sxs-lookup"><span data-stu-id="bb4c2-122">/SECURE</span></span></p></td>
<td align="left"><p><span data-ttu-id="bb4c2-123">Gibt an, dass eine Verbindung mit erweiterter Sicherheit auf dem Veröffentlichungsserver eingerichtet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="bb4c2-123">If present, indicates that a connection with enhanced security should be established to the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bb4c2-124">/Log</span><span class="sxs-lookup"><span data-stu-id="bb4c2-124">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="bb4c2-125">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="bb4c2-125">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bb4c2-126">/Console</span><span class="sxs-lookup"><span data-stu-id="bb4c2-126">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="bb4c2-127">Wenn angegeben, wird die Ausgabe im aktiven Konsolenfenster angezeigt (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="bb4c2-127">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bb4c2-128">/GUI</span><span class="sxs-lookup"><span data-stu-id="bb4c2-128">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="bb4c2-129">Wenn angegeben, wird die Ausgabe in einem Windows-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bb4c2-129">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="bb4c2-130">Für Version 4.6 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bb4c2-130">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bb4c2-131">/LOGU</span><span class="sxs-lookup"><span data-stu-id="bb4c2-131">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="bb4c2-132">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</span><span class="sxs-lookup"><span data-stu-id="bb4c2-132">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="bb4c2-133">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="bb4c2-133">Related topics</span></span>


[<span data-ttu-id="bb4c2-134">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="bb4c2-134">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





