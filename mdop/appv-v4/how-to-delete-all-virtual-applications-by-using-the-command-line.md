---
title: So löschen Sie alle virtuelle Anwendungen über die Befehlszeile
description: So löschen Sie alle virtuelle Anwendungen über die Befehlszeile
author: dansimp
ms.assetid: bfe13b5c-825a-4eb1-a979-6c4b8d8b2a9c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 55c809df31fa5c19f2f1a56c143d492b092156c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807147"
---
# <span data-ttu-id="3df28-103">So löschen Sie alle virtuelle Anwendungen über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="3df28-103">How to Delete All Virtual Applications by Using the Command Line</span></span>


<span data-ttu-id="3df28-104">Mit dem folgenden Verfahren können Sie alle virtuellen Anwendungen von einem bestimmten Computer löschen.</span><span class="sxs-lookup"><span data-stu-id="3df28-104">You can use the following procedure to delete all virtual applications from a specific computer.</span></span>

<span data-ttu-id="3df28-105">**Hinweis**  Wenn alle Anwendungen aus einem Paket gelöscht werden, löscht der Application Virtualization (App-V)-Client auch das Paket.</span><span class="sxs-lookup"><span data-stu-id="3df28-105">**Note** When all applications are deleted from a package, the Application Virtualization (App-V) Client also deletes the package.</span></span>

 

**<span data-ttu-id="3df28-106">So löschen Sie alle Anwendungen</span><span class="sxs-lookup"><span data-stu-id="3df28-106">To delete all applications</span></span>**

-   <span data-ttu-id="3df28-107">Führen Sie den folgenden Befehl aus, um alle Anwendungen für das Benutzerkonto zu löschen, unter dem der Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3df28-107">Run the following command to delete all applications for the user account under which the command is run.</span></span> <span data-ttu-id="3df28-108">Wenn Sie den Befehl mit dem optionalen/Global-Schalter ausführen und ein Konto mit Administratorrechten verwenden, werden alle Anwendungen für alle Benutzer gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3df28-108">If you run the command with the optional /GLOBAL switch, using an account with administrative rights, all applications are deleted for all users.</span></span>

    `SFTMIME DELETE OBJ:APP [/GLOBAL]`

    <span data-ttu-id="3df28-109">**Hinweis**  Wenn alle Anwendungen aus einem Paket gelöscht werden, löscht der Application Virtualization (App-V)-Client auch das Paket.</span><span class="sxs-lookup"><span data-stu-id="3df28-109">**Note** When all applications are deleted from a package, the Application Virtualization (App-V) Client also deletes the package.</span></span>

     

## <span data-ttu-id="3df28-110">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3df28-110">Related topics</span></span>


[<span data-ttu-id="3df28-111">So fügen Sie ein Paket über die Befehlszeile hinzu</span><span class="sxs-lookup"><span data-stu-id="3df28-111">How to Add a Package by Using the Command Line</span></span>](how-to-add-a-package-by-using-the-command-line.md)

[<span data-ttu-id="3df28-112">So entfernen Sie ein Paket über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="3df28-112">How to Remove a Package by Using the Command Line</span></span>](how-to-remove-a-package-by-using-the-command-line.md)

 

 





