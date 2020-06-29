---
title: SFTMIME-Befehlsreferenz
description: SFTMIME-Befehlsreferenz
author: dansimp
ms.assetid: a4a69228-9dd3-4623-b773-899d03c0cf10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 47aac9110febaf3f349461d74fef840326b1c6e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806271"
---
# <span data-ttu-id="4d31c-103">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="4d31c-103">SFTMIME Command Reference</span></span>


<span data-ttu-id="4d31c-104">SFTMIME ist eine Befehlszeilenschnittstelle, die von Application Virtualization (App-V) verwendet wird, mit der Sie viele Clientkonfigurationsdetails verwalten können.</span><span class="sxs-lookup"><span data-stu-id="4d31c-104">SFTMIME is a command-line interface used by Application Virtualization (App-V) that enables you to manage many client configuration details.</span></span> <span data-ttu-id="4d31c-105">Dieser Abschnitt enthält alle Befehle und deren Parameter mit einer kurzen Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="4d31c-105">This section contains all the commands and their parameters, with a brief description of each.</span></span>

**<span data-ttu-id="4d31c-106">Wichtig</span><span class="sxs-lookup"><span data-stu-id="4d31c-106">Important</span></span>**  
-   <span data-ttu-id="4d31c-107">Alle umgekehrten Schrägstriche müssen mit einem vorangehenden umgekehrten Schrägstrich maskiert werden, oder der Pfad wird nicht richtig analysiert.</span><span class="sxs-lookup"><span data-stu-id="4d31c-107">All backslash characters must be escaped using a preceding backslash, or the path will not be parsed correctly.</span></span>

-   <span data-ttu-id="4d31c-108">Wenn Sie ein aufrufendes Programm zum Aufrufen von SFTMIME mit **CreateProcess**verwenden, müssen Sie sicherstellen, dass der erste Parameter der Pfad zu sftmime.exe ist.</span><span class="sxs-lookup"><span data-stu-id="4d31c-108">If you are using a calling program to invoke SFTMIME with **CreateProcess**, you must ensure that the first parameter is the path to sftmime.exe.</span></span>

-   <span data-ttu-id="4d31c-109">Die Ausgabe des SFTMIME- **Abfrage-obj** -Befehls kann nicht an den **findstr** -Befehl umgeleitet werden, um nach einer Zeichenfolge zu suchen.</span><span class="sxs-lookup"><span data-stu-id="4d31c-109">The output of the SFTMIME **QUERY OBJ** command cannot be piped to the **findstr** command to search for a string.</span></span>

-   <span data-ttu-id="4d31c-110">Für die Verwendung des **globalen** Switches sind lokale Administratorrechte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4d31c-110">Use of the **GLOBAL** switch requires local administrator rights.</span></span>

-   <span data-ttu-id="4d31c-111">Die Verwendung von kurzen Pfaden und relativen Pfaden kann zu unerwarteten Ergebnissen führen und sollte vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="4d31c-111">Use of short paths and relative paths can lead to unexpected results and should be avoided.</span></span> <span data-ttu-id="4d31c-112">Verwenden Sie immer vollständige Pfade.</span><span class="sxs-lookup"><span data-stu-id="4d31c-112">Always use full paths.</span></span>

 

## <span data-ttu-id="4d31c-113">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="4d31c-113">In This Section</span></span>


[<span data-ttu-id="4d31c-114">ADD APP</span><span class="sxs-lookup"><span data-stu-id="4d31c-114">ADD APP</span></span>](add-app.md)

[<span data-ttu-id="4d31c-115">ADD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="4d31c-115">ADD PACKAGE</span></span>](add-package.md)

[<span data-ttu-id="4d31c-116">ADD SERVER</span><span class="sxs-lookup"><span data-stu-id="4d31c-116">ADD SERVER</span></span>](add-server.md)

[<span data-ttu-id="4d31c-117">ADD TYPE</span><span class="sxs-lookup"><span data-stu-id="4d31c-117">ADD TYPE</span></span>](add-type.md)

[<span data-ttu-id="4d31c-118">CLEAR APP</span><span class="sxs-lookup"><span data-stu-id="4d31c-118">CLEAR APP</span></span>](clear-app.md)

[<span data-ttu-id="4d31c-119">CLEAR OBJ</span><span class="sxs-lookup"><span data-stu-id="4d31c-119">CLEAR OBJ</span></span>](clear-obj.md)

[<span data-ttu-id="4d31c-120">CONFIGURE APP</span><span class="sxs-lookup"><span data-stu-id="4d31c-120">CONFIGURE APP</span></span>](configure-app.md)

[<span data-ttu-id="4d31c-121">CONFIGURE PACKAGE</span><span class="sxs-lookup"><span data-stu-id="4d31c-121">CONFIGURE PACKAGE</span></span>](configure-package.md)

[<span data-ttu-id="4d31c-122">CONFIGURE SERVER</span><span class="sxs-lookup"><span data-stu-id="4d31c-122">CONFIGURE SERVER</span></span>](configure-server.md)

[<span data-ttu-id="4d31c-123">CONFIGURE TYPE</span><span class="sxs-lookup"><span data-stu-id="4d31c-123">CONFIGURE TYPE</span></span>](configure-type.md)

[<span data-ttu-id="4d31c-124">DELETE APP</span><span class="sxs-lookup"><span data-stu-id="4d31c-124">DELETE APP</span></span>](delete-app.md)

[<span data-ttu-id="4d31c-125">DELETE OBJ</span><span class="sxs-lookup"><span data-stu-id="4d31c-125">DELETE OBJ</span></span>](delete-obj.md)

[<span data-ttu-id="4d31c-126">DELETE PACKAGE</span><span class="sxs-lookup"><span data-stu-id="4d31c-126">DELETE PACKAGE</span></span>](delete-package.md)

[<span data-ttu-id="4d31c-127">DELETE SERVER</span><span class="sxs-lookup"><span data-stu-id="4d31c-127">DELETE SERVER</span></span>](delete-server.md)

[<span data-ttu-id="4d31c-128">DELETE TYPE</span><span class="sxs-lookup"><span data-stu-id="4d31c-128">DELETE TYPE</span></span>](delete-type.md)

[<span data-ttu-id="4d31c-129">HELP</span><span class="sxs-lookup"><span data-stu-id="4d31c-129">HELP</span></span>](help.md)

[<span data-ttu-id="4d31c-130">LOAD APP</span><span class="sxs-lookup"><span data-stu-id="4d31c-130">LOAD APP</span></span>](load-app.md)

[<span data-ttu-id="4d31c-131">LOAD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="4d31c-131">LOAD PACKAGE</span></span>](load-package.md)

[<span data-ttu-id="4d31c-132">LOCK APP</span><span class="sxs-lookup"><span data-stu-id="4d31c-132">LOCK APP</span></span>](lock-app.md)

[<span data-ttu-id="4d31c-133">PUBLISH APP</span><span class="sxs-lookup"><span data-stu-id="4d31c-133">PUBLISH APP</span></span>](publish-app.md)

[<span data-ttu-id="4d31c-134">PUBLISH PACKAGE</span><span class="sxs-lookup"><span data-stu-id="4d31c-134">PUBLISH PACKAGE</span></span>](publish-package.md)

[<span data-ttu-id="4d31c-135">QUERY OBJ</span><span class="sxs-lookup"><span data-stu-id="4d31c-135">QUERY OBJ</span></span>](query-obj.md)

[<span data-ttu-id="4d31c-136">REFRESH SERVER</span><span class="sxs-lookup"><span data-stu-id="4d31c-136">REFRESH SERVER</span></span>](refresh-server.md)

[<span data-ttu-id="4d31c-137">REPAIR APP</span><span class="sxs-lookup"><span data-stu-id="4d31c-137">REPAIR APP</span></span>](repair-app.md)

[<span data-ttu-id="4d31c-138">UNLOAD APP</span><span class="sxs-lookup"><span data-stu-id="4d31c-138">UNLOAD APP</span></span>](unload-app.md)

[<span data-ttu-id="4d31c-139">UNLOAD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="4d31c-139">UNLOAD PACKAGE</span></span>](unload-package.md)

[<span data-ttu-id="4d31c-140">UNLOCK APP</span><span class="sxs-lookup"><span data-stu-id="4d31c-140">UNLOCK APP</span></span>](unlock-app.md)

[<span data-ttu-id="4d31c-141">UNPUBLISH PACKAGE</span><span class="sxs-lookup"><span data-stu-id="4d31c-141">UNPUBLISH PACKAGE</span></span>](unpublish-package.md)

 

 





