---
title: So entfernen Sie ein Paket über die Befehlszeile
description: So entfernen Sie ein Paket über die Befehlszeile
author: dansimp
ms.assetid: 47697ec7-20e5-4258-8865-a0a710d41d5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b282830802f34bfb0670ddfdb8e2852d3559e3f7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806860"
---
# <span data-ttu-id="869f5-103">So entfernen Sie ein Paket über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="869f5-103">How to Remove a Package by Using the Command Line</span></span>


<span data-ttu-id="869f5-104">Sie können die folgenden Befehlszeilenverfahren zum Löschen eines virtuellen Anwendungspakets aus dem Application Virtualization (App-V)-Client auf einem bestimmten Computer verwenden.</span><span class="sxs-lookup"><span data-stu-id="869f5-104">You can use the following command-line procedures to delete a virtual application package from the Application Virtualization (App-V) Client on a specific computer.</span></span>

**<span data-ttu-id="869f5-105">So löschen Sie ein virtuelles Anwendungspaket für alle Benutzer</span><span class="sxs-lookup"><span data-stu-id="869f5-105">To delete a virtual application package for all users</span></span>**

-   <span data-ttu-id="869f5-106">Wenn das Paket zuvor für alle Benutzer mithilfe des/Global-Schalters hinzugefügt wurde, verwenden Sie den folgenden Befehl, um das Paket und die globalen Dateitypen und Verknüpfungen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="869f5-106">If the package was previously added for all users by using the /GLOBAL switch, use the following command to delete the package and the global file types and shortcuts.</span></span> <span data-ttu-id="869f5-107">Es sind Administrator Rechte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="869f5-107">Administrator rights are required.</span></span> <span data-ttu-id="869f5-108">In diesem Fall wird der/Global-Schalter nicht benötigt, da der Befehl immer ein globales Löschen des Pakets ausführt.</span><span class="sxs-lookup"><span data-stu-id="869f5-108">The /GLOBAL switch is not needed in this case because the command always performs a global deletion of the package.</span></span>

    `SFTMIME DELETE PACKAGE:”name”`

**<span data-ttu-id="869f5-109">So löschen Sie ein Paket, das zuvor für einzelne Benutzer hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="869f5-109">To delete a package previously added for individual users</span></span>**

1.  <span data-ttu-id="869f5-110">Wenn das Paket zuvor für einzelne Benutzer hinzugefügt wurde, stehen Ihnen mehrere Optionen zur Auswahl.</span><span class="sxs-lookup"><span data-stu-id="869f5-110">If the package was previously added for individual users, you have several options.</span></span>

    <span data-ttu-id="869f5-111">Führen Sie den folgenden Befehl einmal unter dem Benutzerkonto jeder Person aus, in der das Paket veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="869f5-111">Run the following command once under the user account of each person the package was published to.</span></span> <span data-ttu-id="869f5-112">Dadurch wird dem Benutzer der Zugriff auf die Anwendungen verweigert, wenn er auf einen anderen Computer wechselt.</span><span class="sxs-lookup"><span data-stu-id="869f5-112">This denies the user access to the applications if they roam to another computer.</span></span> <span data-ttu-id="869f5-113">Sie löscht die Einstellungen, Verknüpfungen und Dateitypen des jeweiligen Benutzers aus dem Profil und beendet die Hintergrund Auslastung unter dem Kontext des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="869f5-113">It deletes the specific user’s settings, shortcuts, and file types from the profile, and it stops background loads under the user’s context.</span></span>

    `SFTMIME UNPUBLISH PACKAGE:”name”`

2.  <span data-ttu-id="869f5-114">Alternativ können Sie den folgenden Befehl unter dem Benutzerkonto jeder Person ausführen, in der das Paket veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="869f5-114">Alternatively, run the following command under the user account of each person the package was published to.</span></span>

    `SFTMIME UNPUBLISH PACKAGE:”name”`

    <span data-ttu-id="869f5-115">Führen Sie dann diesen Befehl für das Paket aus.</span><span class="sxs-lookup"><span data-stu-id="869f5-115">Then run this command for the package.</span></span>

    `SFTMIME DELETE PACKAGE:”name”`

    <span data-ttu-id="869f5-116">Dadurch wird das Paket vollständig entfernt, und es werden alle Benutzereinstellungen, Verknüpfungen und Dateitypen aus ihren Profilen gelöscht.</span><span class="sxs-lookup"><span data-stu-id="869f5-116">This completely removes the package, and it deletes all user settings, shortcuts, and file types from their profiles.</span></span> <span data-ttu-id="869f5-117">Wenn das Paket anschließend erneut hinzugefügt wird, müssen die Benutzer die Einstellungen erneut angeben.</span><span class="sxs-lookup"><span data-stu-id="869f5-117">If the package is subsequently re-added, the users will have to specify their settings again.</span></span> <span data-ttu-id="869f5-118">Zum Ausführen dieses Befehls ist nur die Berechtigung "Delete Applications" (**DeleteApp**) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="869f5-118">Only “Delete applications” (**DeleteApp**) permission is needed to run this command.</span></span>

3.  <span data-ttu-id="869f5-119">Als dritte Alternative können Sie einfach den Befehl **Paket löschen** ausführen, ohne den Befehl **Paket veröffentlichen** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="869f5-119">As a third alternative, you can simply run the **DELETE PACKAGE** command without using the **UNPUBLISH PACKAGE** command.</span></span> <span data-ttu-id="869f5-120">In diesem Fall werden Dateitypen und Tastenkombinationen für jeden Benutzer ausgeblendet und nicht gelöscht, und die Benutzereinstellungen bleiben erhalten.</span><span class="sxs-lookup"><span data-stu-id="869f5-120">In this case, file types and shortcuts for each user are hidden rather than deleted, and the user settings are retained.</span></span> <span data-ttu-id="869f5-121">Wenn das Paket anschließend für den Benutzer erneut hinzugefügt wird, werden die Dateitypen und Verknüpfungen wiederhergestellt, und die Benutzereinstellungen werden erneut angewendet.</span><span class="sxs-lookup"><span data-stu-id="869f5-121">This means that if the package is subsequently re-added for the user, the file types and shortcuts are restored, and the user settings are reapplied.</span></span>

## <span data-ttu-id="869f5-122">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="869f5-122">Related topics</span></span>


[<span data-ttu-id="869f5-123">So fügen Sie ein Paket über die Befehlszeile hinzu</span><span class="sxs-lookup"><span data-stu-id="869f5-123">How to Add a Package by Using the Command Line</span></span>](how-to-add-a-package-by-using-the-command-line.md)

[<span data-ttu-id="869f5-124">So löschen Sie alle virtuelle Anwendungen über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="869f5-124">How to Delete All Virtual Applications by Using the Command Line</span></span>](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

 

 





