---
title: CONFIGURE SERVER
description: CONFIGURE SERVER
author: dansimp
ms.assetid: c916eddd-74f2-46e4-953d-120b23284e37
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7757f281ec57645d20367056ba0013ef476a91a1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809076"
---
# <span data-ttu-id="a0dfd-103">CONFIGURE SERVER</span><span class="sxs-lookup"><span data-stu-id="a0dfd-103">CONFIGURE SERVER</span></span>


<span data-ttu-id="a0dfd-104">Ermöglicht es einem Benutzer, die Einrichtung eines Servers zu ändern. alle nicht angegebenen Einstellungen werden nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="a0dfd-104">Enables a user to change the setup of a server; any settings not specified will not be modified.</span></span>

`SFTMIME CONFIGURE SERVER:server-name [/NAME display-name] [/HOST hostname]                 [/PORT port] [/PATH path] [/TYPE {HTTP|RTSP}]                 [/REFRESH {ON|OFF}] [/SECURE]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a0dfd-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0dfd-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="a0dfd-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0dfd-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a0dfd-107">Server: &lt; Servername&gt;</span><span class="sxs-lookup"><span data-stu-id="a0dfd-107">SERVER:&lt;server-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0dfd-108">Der Anzeigename für den Veröffentlichungsserver.</span><span class="sxs-lookup"><span data-stu-id="a0dfd-108">The display name for the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a0dfd-109">/Name &lt; -Anzeige Name&gt;</span><span class="sxs-lookup"><span data-stu-id="a0dfd-109">/NAME &lt;display-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0dfd-110">Neuer Anzeigename für den Server.</span><span class="sxs-lookup"><span data-stu-id="a0dfd-110">New display name for the server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a0dfd-111">/Host &lt; Hostname&gt;</span><span class="sxs-lookup"><span data-stu-id="a0dfd-111">/HOST &lt;hostname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0dfd-112">Der Hostname oder die IP-Adresse des Veröffentlichungsservers.</span><span class="sxs-lookup"><span data-stu-id="a0dfd-112">The host name or IP address for the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a0dfd-113">/Port- &lt; Port&gt;</span><span class="sxs-lookup"><span data-stu-id="a0dfd-113">/PORT &lt;port&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0dfd-114">Der Port, auf dem der Veröffentlichungsserver lauscht.</span><span class="sxs-lookup"><span data-stu-id="a0dfd-114">The port on which the publishing server listens.</span></span> <span data-ttu-id="a0dfd-115">Standardmäßig wird 80 für normale HTTP-Server, 443 für http-Server mit erweiterter Sicherheit, 554 für normale Application Virtualization-Server und 322 für Server mit erweiterter Sicherheit verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0dfd-115">Defaults to 80 for normal HTTP servers, 443 for HTTP servers using enhanced security, 554 for normal Application Virtualization Servers, and 322 for servers using enhanced security.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a0dfd-116">/Path- &lt; Pfad&gt;</span><span class="sxs-lookup"><span data-stu-id="a0dfd-116">/PATH &lt;path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0dfd-117">Der Pfadabschnitt der in einer Veröffentlichungsanforderung verwendeten URL.</span><span class="sxs-lookup"><span data-stu-id="a0dfd-117">The path portion of the URL used in a publishing request.</span></span> <span data-ttu-id="a0dfd-118">Wenn der Parameter Type auf RTSP eingestellt ist, ist der Pfad optional und standardmäßig auf &quot; / &quot; .</span><span class="sxs-lookup"><span data-stu-id="a0dfd-118">If the TYPE parameter is set to RTSP, the path is optional and defaults to &quot;/&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a0dfd-119">/Type</span><span class="sxs-lookup"><span data-stu-id="a0dfd-119">/TYPE</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0dfd-120">Gibt an, ob es sich bei dem Veröffentlichungsserver um einen Webserver ( &quot; http &quot; ) oder einen Application Virtualization Server ( &quot; RTSP &quot; ) handelt.</span><span class="sxs-lookup"><span data-stu-id="a0dfd-120">Indicates whether the publishing server is a Web server (&quot;HTTP&quot;) or an Application Virtualization Server (&quot;RTSP&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a0dfd-121">/Refresh</span><span class="sxs-lookup"><span data-stu-id="a0dfd-121">/REFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0dfd-122">Wenn die Einstellung auf ein gesetzt ist, werden Veröffentlichungsinformationen aktualisiert, wenn sich der Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="a0dfd-122">If set to ON, publishing information will be refreshed when the user logs in.</span></span> <span data-ttu-id="a0dfd-123">Standardmäßig auf ein.</span><span class="sxs-lookup"><span data-stu-id="a0dfd-123">Defaults to ON.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a0dfd-124">/Secure</span><span class="sxs-lookup"><span data-stu-id="a0dfd-124">/SECURE</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0dfd-125">Gibt an, dass eine Verbindung mit erweiterter Sicherheit auf dem Veröffentlichungsserver eingerichtet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="a0dfd-125">If present, indicates that a connection with enhanced security should be established to the publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a0dfd-126">/Log</span><span class="sxs-lookup"><span data-stu-id="a0dfd-126">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0dfd-127">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="a0dfd-127">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a0dfd-128">/Console</span><span class="sxs-lookup"><span data-stu-id="a0dfd-128">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0dfd-129">Wenn angegeben, wird die Ausgabe im aktiven Konsolenfenster angezeigt (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="a0dfd-129">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a0dfd-130">/GUI</span><span class="sxs-lookup"><span data-stu-id="a0dfd-130">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0dfd-131">Wenn angegeben, wird die Ausgabe in einem Windows-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a0dfd-131">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a0dfd-132">Für Version 4.6 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a0dfd-132">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a0dfd-133">/LOGU</span><span class="sxs-lookup"><span data-stu-id="a0dfd-133">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0dfd-134">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</span><span class="sxs-lookup"><span data-stu-id="a0dfd-134">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="a0dfd-135">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a0dfd-135">Related topics</span></span>


[<span data-ttu-id="a0dfd-136">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="a0dfd-136">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





