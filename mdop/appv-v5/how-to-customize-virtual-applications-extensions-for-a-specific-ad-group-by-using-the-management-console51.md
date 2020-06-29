---
title: So passen Sie mithilfe der Verwaltungskonsole virtuelle Anwendungserweiterungen für eine spezifische AD-Gruppe an
description: So passen Sie mithilfe der Verwaltungskonsole virtuelle Anwendungserweiterungen für eine spezifische AD-Gruppe an
author: dansimp
ms.assetid: dd71df05-512f-4eb4-a55f-e5b93601323d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bf086da3fbb6938a4fc602af5ab63adb1621532
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805591"
---
# <span data-ttu-id="e26c4-103">So passen Sie mithilfe der Verwaltungskonsole virtuelle Anwendungserweiterungen für eine spezifische AD-Gruppe an</span><span class="sxs-lookup"><span data-stu-id="e26c4-103">How to Customize Virtual Applications Extensions for a Specific AD Group by Using the Management Console</span></span>


<span data-ttu-id="e26c4-104">Gehen Sie wie folgt vor, um die Erweiterungen der virtuellen Anwendung für eine Active Directory-Gruppe (AD) anzupassen.</span><span class="sxs-lookup"><span data-stu-id="e26c4-104">Use the following procedure to customize the virtual application extensions for an Active Directory (AD) group.</span></span>

**<span data-ttu-id="e26c4-105">So passen Sie die Erweiterungen virtueller Anwendungen für eine Anzeigengruppe an</span><span class="sxs-lookup"><span data-stu-id="e26c4-105">To customize virtual applications extensions for an AD group</span></span>**

1.  <span data-ttu-id="e26c4-106">Um das Paket anzuzeigen, das Sie konfigurieren möchten, öffnen Sie die App-V 5,1-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="e26c4-106">To view the package that you want to configure, open the App-V 5.1 Management Console.</span></span> <span data-ttu-id="e26c4-107">Wenn Sie die Konfiguration anzeigen möchten, die einer bestimmten Benutzergruppe zugewiesen ist, wählen Sie das Paket aus, klicken Sie mit der rechten Maustaste auf den Paketnamen, und wählen Sie **Active Directory-Zugriff bearbeiten**aus.</span><span class="sxs-lookup"><span data-stu-id="e26c4-107">To view the configuration that is assigned to a given user group, select the package, and right-click the package name and select **Edit active directory access**.</span></span> <span data-ttu-id="e26c4-108">Alternativ können Sie das Paket auswählen und im Bereich **anzeigen Zugriff** auf **Bearbeiten** klicken.</span><span class="sxs-lookup"><span data-stu-id="e26c4-108">Alternatively, select the package and click **EDIT** in the **AD ACCESS** pane.</span></span>

2.  <span data-ttu-id="e26c4-109">Zum Anpassen einer Anzeigengruppe können Sie die Gruppe in der Liste der **anzeigen Entitäten mit Access**finden.</span><span class="sxs-lookup"><span data-stu-id="e26c4-109">To customize an AD group, you can find the group from the list of **AD Entities with Access**.</span></span> <span data-ttu-id="e26c4-110">Wählen Sie dann über das Dropdownfeld im Bereich **zugewiesene Konfiguration** die Option **Benutzerdefiniert**aus, und klicken Sie dann auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="e26c4-110">Then, using the drop-down box in the **Assigned Configuration** pane, select **Custom**, and then click **EDIT**.</span></span>

3.  <span data-ttu-id="e26c4-111">Um alle Erweiterungen für eine bestimmte Anwendung zu deaktivieren, deaktivieren Sie **aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="e26c4-111">To disable all extensions for a given application, clear **ENABLE**.</span></span>

    <span data-ttu-id="e26c4-112">Wenn Sie eine neue Verknüpfung für die ausgewählte Anwendung hinzufügen möchten, klicken Sie im Bereich " **Verknüpfungen** " mit der rechten Maustaste auf die Anwendung, und wählen Sie **neue Verknüpfung hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="e26c4-112">To add a new shortcut for the selected application, right-click the application in the **SHORTCUTS** pane, and select **Add new shortcut**.</span></span> <span data-ttu-id="e26c4-113">Um eine Verknüpfung zu entfernen, klicken Sie im Bereich " **Verknüpfungen** " mit der rechten Maustaste auf die Anwendung, und wählen Sie **Verknüpfung entfernen**aus.</span><span class="sxs-lookup"><span data-stu-id="e26c4-113">To remove a shortcut, right-click the application in the **SHORTCUTS** pane, and select **Remove Shortcut**.</span></span> <span data-ttu-id="e26c4-114">Wenn Sie eine vorhandene Verknüpfung bearbeiten möchten, klicken Sie mit der rechten Maustaste auf die Anwendung, und wählen Sie **Verknüpfung bearbeiten**aus.</span><span class="sxs-lookup"><span data-stu-id="e26c4-114">To edit an existing shortcut, right-click the application, and select **Edit Shortcut**.</span></span>

4.  <span data-ttu-id="e26c4-115">Wenn Sie weitere Anwendungserweiterungen anzeigen möchten, klicken Sie auf **erweitert**, und klicken Sie dann auf **Konfiguration exportieren**.</span><span class="sxs-lookup"><span data-stu-id="e26c4-115">To view any other application extensions, click **Advanced**, and click **Export Configuration**.</span></span> <span data-ttu-id="e26c4-116">Geben Sie einen Dateinamen ein, und klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="e26c4-116">Type in a filename and click **Save**.</span></span> <span data-ttu-id="e26c4-117">Mit der Konfigurationsdatei können Sie alle Anwendungserweiterungen anzeigen, die dem Paket zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e26c4-117">You can view all application extensions that are associated with the package using the configuration file.</span></span>

5.  <span data-ttu-id="e26c4-118">Wenn Sie zusätzliche Anwendungserweiterungen bearbeiten möchten, ändern Sie die Konfigurationsdatei, und klicken Sie auf **importieren, und überschreiben Sie diese Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e26c4-118">To edit additional application extensions, modify the configuration file and click **Import and Overwrite this Configuration**.</span></span> <span data-ttu-id="e26c4-119">Wählen Sie die geänderte Datei aus, und klicken Sie auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="e26c4-119">Select the modified file and click **Open**.</span></span> <span data-ttu-id="e26c4-120">Klicken Sie im Dialogfeld auf über **Schreiben** , um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="e26c4-120">In the dialog, click **Overwrite** to complete the process.</span></span>

    <span data-ttu-id="e26c4-121">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="e26c4-121">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="e26c4-122">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="e26c4-122">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="e26c4-123">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="e26c4-123">Got an App-V issue?</span></span>** <span data-ttu-id="e26c4-124">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="e26c4-124">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="e26c4-125">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="e26c4-125">Related topics</span></span>


[<span data-ttu-id="e26c4-126">Vorgänge für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="e26c4-126">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





