---
title: LOAD APP
description: LOAD APP
author: dansimp
ms.assetid: 7b727d0c-5423-419d-92ef-7ebbc6343e79
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 02bd6e35da898f5b34f7efc21cbc01a72d555b8d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806631"
---
# <span data-ttu-id="db68f-103">LOAD APP</span><span class="sxs-lookup"><span data-stu-id="db68f-103">LOAD APP</span></span>


<span data-ttu-id="db68f-104">Lädt die angegebene Anwendung und alle anderen Anwendungen im Paket in den Dateisystemcache.</span><span class="sxs-lookup"><span data-stu-id="db68f-104">Loads the specified application and all other applications in the package into the file system cache.</span></span>

<span data-ttu-id="db68f-105">**Hinweis**  Mit dem Befehl **Load App** wird der Ladevorgang gestartet, und im Desktop Benachrichtigungsbereich wird eine Statusanzeige angezeigt.</span><span class="sxs-lookup"><span data-stu-id="db68f-105">**Note** The **LOAD APP** command starts the load process and a progress bar is displayed in the Desktop Notification Area.</span></span> <span data-ttu-id="db68f-106">Der Befehl wird unmittelbar nach dem Starten dieses Prozesses beendet, sodass alle Ladefehler am gleichen Speicherort angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="db68f-106">The command exits immediately after starting this process, so any load errors are displayed in the same location.</span></span> <span data-ttu-id="db68f-107">Verwenden Sie den Befehl **Paket laden** , wenn Sie den Ladevorgang über die Befehlszeile starten möchten, ohne den Desktop Benachrichtigungsbereich zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="db68f-107">Use the **LOAD PACKAGE** command if you want to start the load process from the command line without using the Desktop Notification Area.</span></span>

 

`SFTMIME LOAD APP:application [/LOG log-pathname | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="db68f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="db68f-108">Parameter</span></span></th>
<th align="left"><span data-ttu-id="db68f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="db68f-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db68f-110">App: &lt; Anwendung&gt;</span><span class="sxs-lookup"><span data-stu-id="db68f-110">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="db68f-111">Der Name und die Version (optional) der zu ladenden Anwendung.</span><span class="sxs-lookup"><span data-stu-id="db68f-111">The name and version (optional) of the application to load.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db68f-112">/Log</span><span class="sxs-lookup"><span data-stu-id="db68f-112">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="db68f-113">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="db68f-113">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db68f-114">/GUI</span><span class="sxs-lookup"><span data-stu-id="db68f-114">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="db68f-115">Wenn angegeben, wird die Ausgabe in einem Windows-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="db68f-115">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="db68f-116">Für Version 4.6 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="db68f-116">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db68f-117">/LOGU</span><span class="sxs-lookup"><span data-stu-id="db68f-117">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="db68f-118">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</span><span class="sxs-lookup"><span data-stu-id="db68f-118">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="db68f-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="db68f-119">Related topics</span></span>


[<span data-ttu-id="db68f-120">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="db68f-120">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





