---
title: DELETE SERVER
description: DELETE SERVER
author: dansimp
ms.assetid: 4c929639-1c1d-47c3-9225-cc4d7a8736f0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92af31a818174fb4b0e82a11c918af2484ac2bce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808908"
---
# <span data-ttu-id="f8ab1-103">DELETE SERVER</span><span class="sxs-lookup"><span data-stu-id="f8ab1-103">DELETE SERVER</span></span>


<span data-ttu-id="f8ab1-104">Entfernt einen Veröffentlichungsserver.</span><span class="sxs-lookup"><span data-stu-id="f8ab1-104">Removes a publishing server.</span></span>

<span data-ttu-id="f8ab1-105">**Hinweis**  Mit diesem Befehl werden keine Anwendungen oder Pakete entfernt, die vom Server auf dem Client veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="f8ab1-105">**Note** This command does not remove any applications or packages published to the client by the server.</span></span> <span data-ttu-id="f8ab1-106">Verwenden Sie für jede Anwendung den Befehl SFTMIME **Clear App** , gefolgt vom Befehl **Paket löschen** , um diese Anwendungen und Pakete vollständig vom Client zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="f8ab1-106">For each application, use the SFTMIME **CLEAR APP** command followed by the **DELETE PACKAGE** command to completely remove those applications and packages from the client.</span></span>

 

`SFTMIME DELETE SERVER:server-name [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f8ab1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8ab1-107">Parameter</span></span></th>
<th align="left"><span data-ttu-id="f8ab1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8ab1-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f8ab1-109">Server: &lt; Servername&gt;</span><span class="sxs-lookup"><span data-stu-id="f8ab1-109">SERVER:&lt;server-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8ab1-110">Der Anzeigename des Veröffentlichungsservers.</span><span class="sxs-lookup"><span data-stu-id="f8ab1-110">The display name of the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f8ab1-111">/Log</span><span class="sxs-lookup"><span data-stu-id="f8ab1-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8ab1-112">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="f8ab1-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f8ab1-113">/Console</span><span class="sxs-lookup"><span data-stu-id="f8ab1-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8ab1-114">Wenn angegeben, wird die Ausgabe im aktiven Konsolenfenster angezeigt (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="f8ab1-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f8ab1-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="f8ab1-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8ab1-116">Wenn angegeben, wird die Ausgabe in einem Windows-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f8ab1-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f8ab1-117">Für Version 4.6 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f8ab1-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f8ab1-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="f8ab1-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8ab1-119">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</span><span class="sxs-lookup"><span data-stu-id="f8ab1-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f8ab1-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="f8ab1-120">Related topics</span></span>


[<span data-ttu-id="f8ab1-121">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="f8ab1-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





