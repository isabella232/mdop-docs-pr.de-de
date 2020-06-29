---
title: Zusätzliche Komponenten für virtuelle Anwendungspakete
description: Zusätzliche Komponenten für virtuelle Anwendungspakete
author: dansimp
ms.assetid: 476b0f40-ebd6-4296-92fa-61fa9495c03c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d30c2c6561b0d2c08fd75e0c977bf4590d7e6688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806163"
---
# <span data-ttu-id="03720-103">Zusätzliche Komponenten für virtuelle Anwendungspakete</span><span class="sxs-lookup"><span data-stu-id="03720-103">Virtual Application Package Additional Components</span></span>


<span data-ttu-id="03720-104">Der App-V-Sequenzer hat ein Verzeichnis gefunden, das 64-Bit-und 32-Bit-Dateien und/oder DLL-Dateien (Dynamic Link Library) enthält, die von der gleichen parallelen Assembly abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="03720-104">The App-V Sequencer has detected a directory that contains 64-bit and 32-bit executables and/or dynamic-link library (.dll) files that depend on the same side-by-side assembly.</span></span> <span data-ttu-id="03720-105">In der Regel erstellt der Sequencer private nebeneinander angeordnete Assemblys für alle öffentlichen Assemblys, die vom Paket verwendet werden. Es ist jedoch nicht möglich, 32-Bit-und 64-Bit-Versionen der privaten Assemblys im gleichen Verzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="03720-105">Typically, the Sequencer creates private side-by-side assemblies for all public assemblies that are used by the package; however, it is not possible to create 32-bit and 64-bit versions of the private assemblies in the same directory.</span></span>

<span data-ttu-id="03720-106">Wenn der Sequencer einen einzelnen Konflikt erkennt, führt er die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="03720-106">If the Sequencer detects a single conflict, it will perform the following actions:</span></span>

-   <span data-ttu-id="03720-107">Entfernen Sie alle vorhandenen 64-Bit-privaten Assemblys im gesamten Paket, unabhängig davon, ob das Verzeichnis einen Konflikt aufweist.</span><span class="sxs-lookup"><span data-stu-id="03720-107">Remove all of the existing 64-bit private assemblies in the entire package, whether or not the directory has a conflict.</span></span>

-   <span data-ttu-id="03720-108">Erstellen Sie nur 32-Bit-Versionen der privaten nebeneinander angeordneten Assemblys.</span><span class="sxs-lookup"><span data-stu-id="03720-108">Create only 32-bit versions of the private side-by-side assemblies.</span></span>

<span data-ttu-id="03720-109">Sie sollten die öffentlichen Versionen aller erforderlichen 64-Bit-Assemblys auf dem Computer, auf dem der Sequencer ausgeführt wird, und auf allen App-V-Clientcomputern nativ installieren.</span><span class="sxs-lookup"><span data-stu-id="03720-109">You should natively install public versions of all the required 64-bit assemblies on the computer running the Sequencer and on all App-V client computers.</span></span>

<span data-ttu-id="03720-110">Um die erforderlichen vorhandenen öffentlichen Assemblys zu finden, öffnen Sie das Verzeichnis, in dem das Paket gespeichert ist, und suchen Sie im **VFS** -Ordner.</span><span class="sxs-lookup"><span data-stu-id="03720-110">To locate the required existing public assemblies, open the directory where the package is saved and look in the **VFS** folder.</span></span> <span data-ttu-id="03720-111">Wenn beispielsweise der Paketstamm **Q:\\MyApp**ist, suchen Sie beim Sequenzieren der Anwendung in **Q:\\MyApp\\VFS\\CSIDL\ _Windows \\winsxs\\manifests** , und suchen Sie alle vorhandenen öffentlichen Assemblys.</span><span class="sxs-lookup"><span data-stu-id="03720-111">For example, if the package root is **Q:\\MyApp**, when you sequence the application, look in **Q:\\MyApp\\VFS\\CSIDL\_Windows\\WinSxS\\Manifests** and locate all of the existing public assemblies.</span></span> <span data-ttu-id="03720-112">Die 64-Bit-Versionen dieser Dateien beginnen immer mit dem folgenden Text am Anfang des manifestnamens: **amd64.**...</span><span class="sxs-lookup"><span data-stu-id="03720-112">The 64-bit versions of these files will always start with the following text at the beginning of the manifest name: **amd64…**.</span></span> <span data-ttu-id="03720-113">Der genaue Name und die Version der Assembly finden Sie in der zugehörigen Manifestdatei.</span><span class="sxs-lookup"><span data-stu-id="03720-113">The exact name and version of the assembly can be found in the associated manifest file.</span></span>

<span data-ttu-id="03720-114">Verwenden Sie einen der folgenden Links, um die richtige Version der erforderlichen Voraussetzungen herunterzuladen und zu installieren:</span><span class="sxs-lookup"><span data-stu-id="03720-114">Use any of the following links to download and install the correct version of the required prerequisites:</span></span>

-   [<span data-ttu-id="03720-115">Microsoft Visual C++ 2005 Redistributable Package (x64)</span><span class="sxs-lookup"><span data-stu-id="03720-115">Microsoft Visual C++ 2005 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152697)

-   [<span data-ttu-id="03720-116">Microsoft Visual C++ 2005 SP1 Redistributable Package (x64)</span><span class="sxs-lookup"><span data-stu-id="03720-116">Microsoft Visual C++ 2005 SP1 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152698)

-   [<span data-ttu-id="03720-117">Microsoft Visual C++ 2008 Redistributable Package (x64)</span><span class="sxs-lookup"><span data-stu-id="03720-117">Microsoft Visual C++ 2008 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152699)

-   [<span data-ttu-id="03720-118">Microsoft Visual C++ 2008 SP1 Redistributable Package (x64)</span><span class="sxs-lookup"><span data-stu-id="03720-118">Microsoft Visual C++ 2008 SP1 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152700)

 

 





