---
title: So ändern Sie die Cachegröße des Servers
description: So ändern Sie die Cachegröße des Servers
author: dansimp
ms.assetid: 24e63744-21c3-458e-b137-9592f4fe785c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92e56a8a28f7a00d71805b497f9e404cca65919d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807343"
---
# <span data-ttu-id="958bd-103">So ändern Sie die Cachegröße des Servers</span><span class="sxs-lookup"><span data-stu-id="958bd-103">How to Change the Server Cache Size</span></span>


<span data-ttu-id="958bd-104">Mit dem folgenden Verfahren können Sie die Cachegröße für jeden Server direkt in der Application Virtualization Server-Verwaltungskonsole ändern.</span><span class="sxs-lookup"><span data-stu-id="958bd-104">You can use the following procedure to change the cache size for any server directly from the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="958bd-105">**Hinweis**  Zwar können Sie die Cachegröße ändern, es wird jedoch empfohlen, die Cachegröße auf die Standardwerte festzulegen, es sei denn, Sie müssen die Größe speziell für die Konfiguration ändern.</span><span class="sxs-lookup"><span data-stu-id="958bd-105">**Note** Although you can change the cache size, unless your configuration specifically requires you to change the size, it is recommended that you leave the cache size set to the default values.</span></span>

 

**<span data-ttu-id="958bd-106">So ändern Sie die Größe des Server Caches</span><span class="sxs-lookup"><span data-stu-id="958bd-106">To change the server cache size</span></span>**

1.  <span data-ttu-id="958bd-107">Klicken Sie im linken Bereich auf den Knoten **Servergruppen** , um die Liste der Servergruppen zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="958bd-107">Click the **Server Groups** node in the left pane to expand the list of server groups.</span></span>

2.  <span data-ttu-id="958bd-108">Doppelklicken Sie im **Ergebnis** Bereich auf die gewünschte Servergruppe, um die Liste der Server in der Gruppe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="958bd-108">In the **Results** pane, double-click the desired server group to display the list of servers in the group.</span></span>

3.  <span data-ttu-id="958bd-109">Klicken Sie im **Ergebnis** Bereich mit der rechten Maustaste auf den gewünschten Server, und wählen Sie **Eigenschaften**aus.</span><span class="sxs-lookup"><span data-stu-id="958bd-109">In the **Results** pane, right-click the desired server and select **Properties**.</span></span>

4.  <span data-ttu-id="958bd-110">Wählen Sie die Registerkarte **erweitert** aus.</span><span class="sxs-lookup"><span data-stu-id="958bd-110">Select the **Advanced** tab.</span></span>

5.  <span data-ttu-id="958bd-111">Geben Sie im Feld **Maximale Speicherzuteilung** für den Server Cache einen Wert ein, und geben Sie einen Wert für die Schwellenwert Warnstufe im Feld Warnungs **Speicherzuteilung** ein.</span><span class="sxs-lookup"><span data-stu-id="958bd-111">Enter a value in the **Maximum Memory Allocation** field for the server cache, and enter a value for the threshold warning level in the **Warn Memory Allocation** field.</span></span>

6.  <span data-ttu-id="958bd-112">Geben Sie einen Wert in das Feld **Maximale Block Größe** ein.</span><span class="sxs-lookup"><span data-stu-id="958bd-112">Enter a value in the **Maximum Block Size** field.</span></span> <span data-ttu-id="958bd-113">Diese Zahl muss größer oder gleich der maximalen Blockgröße des größten Pakets sein, das vom Server gestreamt wird.</span><span class="sxs-lookup"><span data-stu-id="958bd-113">This number must be greater than or equal to the maximum block size of the largest package that will be streamed from the server.</span></span>

7.  <span data-ttu-id="958bd-114">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="958bd-114">Click **OK**.</span></span>

## <span data-ttu-id="958bd-115">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="958bd-115">Related topics</span></span>


[<span data-ttu-id="958bd-116">So ändern Sie den Server-Port</span><span class="sxs-lookup"><span data-stu-id="958bd-116">How to Change the Server Port</span></span>](how-to-change-the-server-port.md)

[<span data-ttu-id="958bd-117">So verwalten Sie Server in der Server Management Console</span><span class="sxs-lookup"><span data-stu-id="958bd-117">How to Manage Servers in the Server Management Console</span></span>](how-to-manage-servers-in-the-server-management-console.md)

 

 





