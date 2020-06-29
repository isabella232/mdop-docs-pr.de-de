---
title: So fügen Sie ein Paket über die Befehlszeile hinzu
description: So fügen Sie ein Paket über die Befehlszeile hinzu
author: dansimp
ms.assetid: e75af49e-811a-407a-a7f0-6de8562b9188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ab418017a075300f308d4ef4c6eceb4f623a05c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808737"
---
# <span data-ttu-id="dc70c-103">So fügen Sie ein Paket über die Befehlszeile hinzu</span><span class="sxs-lookup"><span data-stu-id="dc70c-103">How to Add a Package by Using the Command Line</span></span>


<span data-ttu-id="dc70c-104">In den folgenden Verfahren sind die Schritte aufgeführt, die zum Hinzufügen eines virtuellen Anwendungspakets zum Application Virtualization (App-V)-Client auf einem bestimmten Computer erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="dc70c-104">The following procedures list the steps that are necessary to add a virtual application package to the Application Virtualization (App-V) Client on a specific computer.</span></span>

**<span data-ttu-id="dc70c-105">So fügen Sie ein virtuelles Anwendungspaket für einen bestimmten Benutzer hinzu</span><span class="sxs-lookup"><span data-stu-id="dc70c-105">To add a virtual application package for a specific user</span></span>**

-   <span data-ttu-id="dc70c-106">Führen Sie den folgenden Befehl unter dem Benutzerkonto der Person aus, die das Paket erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="dc70c-106">Run the following command under the user account of the person who is to get the package.</span></span> <span data-ttu-id="dc70c-107">Mit dem Befehl wird das Paket für diesen Benutzer hinzugefügt und veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="dc70c-107">The command adds and publishes the package for that user.</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

**<span data-ttu-id="dc70c-108">So fügen Sie ein virtuelles Anwendungspaket für alle Benutzer hinzu</span><span class="sxs-lookup"><span data-stu-id="dc70c-108">To add a virtual application package for all users</span></span>**

-   <span data-ttu-id="dc70c-109">Führen Sie den folgenden Befehl unter einem Konto mit Administratorrechten aus.</span><span class="sxs-lookup"><span data-stu-id="dc70c-109">Run the following command under an account that has administrator rights.</span></span> <span data-ttu-id="dc70c-110">Das Paket wird für alle Benutzer auf dem Computer hinzugefügt und veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="dc70c-110">The package is added and published for all users on the computer.</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

**<span data-ttu-id="dc70c-111">So fügen Sie ein Paket mit einem elektronischen Softwareverteilungssystem hinzu</span><span class="sxs-lookup"><span data-stu-id="dc70c-111">To add a package using an electronic software distribution system</span></span>**

1.  <span data-ttu-id="dc70c-112">Wenn Sie ein elektronisches Softwareverteilungssystem verwenden, das die Befehle unter dem **System** Konto des Computers ausführt, wird das Paket nur für dieses Konto veröffentlicht, es sei denn, Sie verwenden den/Global-Schalter.</span><span class="sxs-lookup"><span data-stu-id="dc70c-112">If you are using an electronic software distribution system that runs the commands under the computer’s **SYSTEM** account, the package is published for that account only, unless you use the /GLOBAL switch.</span></span> <span data-ttu-id="dc70c-113">Führen Sie den folgenden Befehl aus, um das Paket für alle Benutzer auf dem Computer hinzuzufügen und zu veröffentlichen:</span><span class="sxs-lookup"><span data-stu-id="dc70c-113">Run the following command to add and publish the package for all users on the computer:</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

2.  

    <span data-ttu-id="dc70c-114">Wenn Sie das Paket nur für bestimmte Benutzer hinzufügen möchten, führen Sie den Befehl **Paket hinzufügen** aus, und veröffentlichen Sie dann das Paket für jeden Benutzer explizit, indem Sie den folgenden Befehl zum **veröffentlichen** des Pakets unter dem Benutzerkonto jeder Person ausführen:</span><span class="sxs-lookup"><span data-stu-id="dc70c-114">If you want to add the package for specific users only, run the **ADD PACKAGE** command, and then explicitly publish the package for each user by running the following **PUBLISH PACKAGE** command under each person’s user account:</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

    `SFTMIME PUBLISH PACKAGE:”name” /MANIFEST <manifest-path>`

    <span data-ttu-id="dc70c-115">Durch die Veröffentlichung des Pakets ohne den globalen Parameter wird dem Benutzer der Zugriff auf die Anwendungen im Paket gewährt, und die im Manifest aufgelisteten Dateitypen und Verknüpfungen werden im Profil des Benutzers veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="dc70c-115">Publishing the package without the GLOBAL parameter grants the user access to the applications in the package and publishes the file types and shortcuts that are listed in the manifest to the user’s profile.</span></span> <span data-ttu-id="dc70c-116">Die erforderlichen Berechtigungen sind "Verwalten von Dateitypzuordnungen" (**ManageTypes**) und "Veröffentlichungs Verknüpfungen" (**PublishShortcut**).</span><span class="sxs-lookup"><span data-stu-id="dc70c-116">Permissions required are “Manage file type associations” (**ManageTypes**) and “Publish shortcuts” (**PublishShortcut**).</span></span>

## <span data-ttu-id="dc70c-117">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="dc70c-117">Related topics</span></span>


[<span data-ttu-id="dc70c-118">So löschen Sie alle virtuelle Anwendungen über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="dc70c-118">How to Delete All Virtual Applications by Using the Command Line</span></span>](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

[<span data-ttu-id="dc70c-119">So entfernen Sie ein Paket über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="dc70c-119">How to Remove a Package by Using the Command Line</span></span>](how-to-remove-a-package-by-using-the-command-line.md)

 

 





