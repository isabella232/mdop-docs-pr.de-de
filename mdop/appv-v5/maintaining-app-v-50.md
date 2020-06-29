---
title: Warten von App-V 5.0
description: Warten von App-V 5.0
author: dansimp
ms.assetid: 66851ec3-c674-493b-ad6d-db8fcbf1956c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3445bfe00ba7703a66fa3da2f9d7089990dd3854
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805111"
---
# <span data-ttu-id="3e80f-103">Warten von App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="3e80f-103">Maintaining App-V 5.0</span></span>


<span data-ttu-id="3e80f-104">Nachdem Sie die erforderliche Planung abgeschlossen und dann App-v 5,0 bereitgestellt haben, können Sie die folgenden Informationen zum Verwalten der APP-v 5,0-Infrastruktur verwenden.</span><span class="sxs-lookup"><span data-stu-id="3e80f-104">After you have completed all the necessary planning, and then deployment of App-V 5.0, you can use the following information to maintain the App-V 5.0 infrastructure.</span></span>

## <a href="" id="move-the-app-v-5-0-server-"></a><span data-ttu-id="3e80f-105">Verschieben des App-V 5,0-Servers</span><span class="sxs-lookup"><span data-stu-id="3e80f-105">Move the App-V 5.0 Server</span></span>


<span data-ttu-id="3e80f-106">Der APP-v 5,0-Server stellt eine Verbindung mit der APP-v 5,0-Datenbank her.</span><span class="sxs-lookup"><span data-stu-id="3e80f-106">The App-V 5.0 server connects to the App-V 5.0 database.</span></span> <span data-ttu-id="3e80f-107">Daher können Sie die Verwaltungskomponente auf einem beliebigen Computer im Netzwerk installieren und dann mit der App-V 5,0-Datenbank verbinden.</span><span class="sxs-lookup"><span data-stu-id="3e80f-107">Therefore you can install the management component to any computer on the network and then connect it to the App-V 5.0 database.</span></span>

[<span data-ttu-id="3e80f-108">So verschieben Sie den App-V-Server auf einen anderen Computer</span><span class="sxs-lookup"><span data-stu-id="3e80f-108">How to Move the App-V Server to Another Computer</span></span>](how-to-move-the-app-v-server-to-another-computer.md)

## <a href="" id="determine-if-an-app-v-5-0-application-is-running-virtualized-"></a><span data-ttu-id="3e80f-109">Ermitteln, ob eine App-V 5,0-Anwendung virtualisiert ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="3e80f-109">Determine if an App-V 5.0 Application is Running Virtualized</span></span>


<span data-ttu-id="3e80f-110">Unabhängige Softwareanbieter (Independent Software Vendors, ISV), die ermitteln möchten, ob eine Anwendung mit App-V 5,0 oder höher virtualisiert ausgeführt wird, sollten im Standardnamespace ein benanntes Objekt namens \*\*AppVVirtual- &lt; PID &gt; \*\* öffnen.</span><span class="sxs-lookup"><span data-stu-id="3e80f-110">Independent software vendors (ISV) who want to determine if an application is running virtualized with App-V 5.0 or above, should open a named object called **AppVVirtual-&lt;PID&gt;** in the default namespace.</span></span> <span data-ttu-id="3e80f-111">So kann beispielsweise die Windows-API **GetCurrentProcessId ()** verwendet werden, um die ID des aktuellen Prozesses zu erhalten, beispielsweise 4052, und dann, wenn ein benanntes Ereignisobjekt namens **AppVVirtual-4052** erfolgreich mit **OpenEvent ()** im Standardnamespace für Lesezugriff geöffnet werden kann, ist die Anwendung virtuell.</span><span class="sxs-lookup"><span data-stu-id="3e80f-111">For example, Windows API **GetCurrentProcessId()** can be used to obtain the current process's ID, for example 4052, and then if a named Event object called **AppVVirtual-4052** can be successfully opened using **OpenEvent()** in the default namespace for read access, then the application is virtual.</span></span> <span data-ttu-id="3e80f-112">Wenn der **OpenEvent ()** -Aufruf fehlschlägt, ist die Anwendung nicht virtuell.</span><span class="sxs-lookup"><span data-stu-id="3e80f-112">If the **OpenEvent()** call fails, the application is not virtual.</span></span>

<span data-ttu-id="3e80f-113">Darüber hinaus können ISV-Benutzer, die Aufrufe mit App-V 5,0 und höher für bestimmte APIs explizit virtualisieren oder nicht virtualisieren möchten, die **VirtualizeCurrentThread ()** -und **CurrentThreadIsVirtualized ()** -Funktionen verwenden, die im AppEntSubsystems32.dll-Modul implementiert sind.</span><span class="sxs-lookup"><span data-stu-id="3e80f-113">Additionally, ISV’s who want to explicitly virtualize or not virtualize calls on specific API’s with App-V 5.0 and above, can use the **VirtualizeCurrentThread()** and **CurrentThreadIsVirtualized()** functions implemented in the AppEntSubsystems32.dll module.</span></span> <span data-ttu-id="3e80f-114">Diese stellen eine Möglichkeit dar, auf eine Downstream-Komponente zu deuten, dass der Anruf virtualisiert werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="3e80f-114">These provide a way of hinting at a downstream component that the call should or should not be virtualized.</span></span>






## <span data-ttu-id="3e80f-115">Weitere Ressourcen für die Verwaltung von App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="3e80f-115">Other resources for maintaining App-V 5.0</span></span>


[<span data-ttu-id="3e80f-116">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="3e80f-116">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





