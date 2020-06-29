---
title: Informationen zum Veröffentlichen und Aufheben der Veröffentlichung einer Anwendung im MED-V-Arbeitsbereich
description: Informationen zum Veröffentlichen und Aufheben der Veröffentlichung einer Anwendung im MED-V-Arbeitsbereich
author: dansimp
ms.assetid: fd5a62e9-0577-44d2-ae17-61c0aef78ce8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cc8f9579d800aa0e5da0d67e0cd71bcae5e912a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812046"
---
# <span data-ttu-id="d784d-103">Informationen zum Veröffentlichen und Aufheben der Veröffentlichung einer Anwendung im MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="d784d-103">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>


<span data-ttu-id="d784d-104">Obwohl eine Anwendung in einem MED-V-Arbeitsbereich installiert ist, müssen Sie möglicherweise auch die Anwendung veröffentlichen, bevor Sie für den Endbenutzer verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="d784d-104">Even though an application is installed in a MED-V workspace, you might also have to publish the application before it becomes available to the end user.</span></span> <span data-ttu-id="d784d-105">Standardmäßig werden die meisten Anwendungen zu dem Zeitpunkt veröffentlicht, zu dem Sie installiert sind, und Verknüpfungen werden erstellt und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d784d-105">By default, most applications are published at the time that they are installed and shortcuts are created and enabled.</span></span>

<span data-ttu-id="d784d-106">In einigen Fällen möchten Sie möglicherweise Anwendungen im MED-V-Arbeitsbereich installieren, ohne Sie für den Endbenutzer verfügbar zu machen, beispielsweise für die Virenscanner-Software.</span><span class="sxs-lookup"><span data-stu-id="d784d-106">In some cases, you might want to install applications on the MED-V workspace without making them available to the end user, for example, virus-scanning software.</span></span> <span data-ttu-id="d784d-107">Es gibt auch Situationen, in denen Sie eine Anwendung veröffentlichen möchten, die auf dem MED-V-Arbeitsbereich installiert ist, die dem Endbenutzer zuvor nicht zur Verfügung stand.</span><span class="sxs-lookup"><span data-stu-id="d784d-107">Similarly, there are occasions in which you want to publish an application that is installed on the MED-V workspace that was previously unavailable to the end user.</span></span> <span data-ttu-id="d784d-108">Möglicherweise müssen Sie eine installierte Anwendung veröffentlichen, wenn die Installation im **Startmenü** nicht automatisch eine Verknüpfung erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="d784d-108">For example, you might have to publish an installed application if the installation did not automatically create a shortcut on the **Start** menu.</span></span>

<span data-ttu-id="d784d-109">**Wichtig**  Wenn Sie eine Anwendung veröffentlichen, die keine UNC-Pfade unterstützt, empfehlen wir, die Anwendung einem Laufwerk zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="d784d-109">**Important** If you publish an application that does not support UNC paths, we recommend that you map the application to a drive.</span></span>

 

<span data-ttu-id="d784d-110">Sie können Anwendungen in einem bereitgestellten MED-V-Arbeitsbereich veröffentlichen oder deren Veröffentlichung aufheben, indem Sie eine der folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="d784d-110">You can publish or unpublish applications to a deployed MED-V workspace by performing one of the following tasks:</span></span>

**<span data-ttu-id="d784d-111">Veröffentlichen oder Aufheben der Veröffentlichung einer installierten Anwendung</span><span class="sxs-lookup"><span data-stu-id="d784d-111">To publish or unpublish an installed application</span></span>**

1.  <span data-ttu-id="d784d-112">Wenn Sie eine Anwendung in einem bereitgestellten MED-V-Arbeitsbereich veröffentlichen möchten, kopieren Sie eine Verknüpfung für diese Anwendung in den folgenden Ordner auf dem virtuellen Computer:</span><span class="sxs-lookup"><span data-stu-id="d784d-112">To publish an application on a deployed MED-V workspace, copy a shortcut for that application to the following folder on the virtual machine:</span></span>

    <span data-ttu-id="d784d-113">C:\\Dokumente und Einstellungen\\All Users\\Start Menü</span><span class="sxs-lookup"><span data-stu-id="d784d-113">C:\\Documents and Settings\\All Users\\Start Menu</span></span>

    <span data-ttu-id="d784d-114">Verwenden Sie bei Bedarf Gruppenrichtlinien oder ein ESD-System, um ein Skript bereitzustellen, das die Verknüpfung für diese Anwendung in den Ordner "All Users\\Start" kopiert.</span><span class="sxs-lookup"><span data-stu-id="d784d-114">If it is necessary, use Group Policy or an ESD system to deploy a script that copies the shortcut for that application to the All Users\\Start Menu folder.</span></span>

2.  <span data-ttu-id="d784d-115">Wenn Sie die Veröffentlichung einer Anwendung in einem bereitgestellten MED-V-Arbeitsbereich aufheben möchten, löschen Sie die Verknüpfung für diese Anwendung aus dem folgenden Ordner auf dem virtuellen Computer:</span><span class="sxs-lookup"><span data-stu-id="d784d-115">To unpublish an application on a deployed MED-V workspace, delete the shortcut for that application from the following folder on the virtual machine:</span></span>

    <span data-ttu-id="d784d-116">C:\\Dokumente und Einstellungen\\All Users\\Start Menü</span><span class="sxs-lookup"><span data-stu-id="d784d-116">C:\\Documents and Settings\\All Users\\Start Menu</span></span>

    <span data-ttu-id="d784d-117">Verwenden Sie bei Bedarf Gruppenrichtlinien oder ein ESD-System, um ein Skript bereitzustellen, das die Verknüpfung für diese Anwendung aus dem Menü Ordner alle Users\\Start löscht.</span><span class="sxs-lookup"><span data-stu-id="d784d-117">If it is necessary, use Group Policy or an ESD system to deploy a script that deletes the shortcut for that application from the All Users\\Start Menu folder.</span></span>

    <span data-ttu-id="d784d-118">**Hinweis**  Häufig wird die Verknüpfung automatisch aus dem **Startmenü** des Hostcomputers gelöscht, wenn Sie die Anwendung deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="d784d-118">**Note** Frequently, the shortcut is automatically deleted from the host computer **Start** menu when you uninstall the application.</span></span> <span data-ttu-id="d784d-119">In einigen Fällen, beispielsweise für einen MED-V-Arbeitsbereich, der für alle Benutzer eines freigegebenen Computers konfiguriert ist, müssen Sie möglicherweise die Verknüpfung im **Startmenü** nach der Deinstallation der Anwendung manuell löschen.</span><span class="sxs-lookup"><span data-stu-id="d784d-119">However, in some cases, such as for a MED-V workspace that is configured for all users of a shared computer, you might have to manually delete the shortcut on the **Start** menu after the application is uninstalled.</span></span> <span data-ttu-id="d784d-120">Der Endbenutzer kann dies tun, indem Sie mit der rechten Maustaste auf die Verknüpfung klicken und dann **Löschen**auswählen.</span><span class="sxs-lookup"><span data-stu-id="d784d-120">The end-user can do this by right-clicking the shortcut and selecting **Delete**.</span></span>

     

<span data-ttu-id="d784d-121">Um zu testen, ob die Anwendung veröffentlicht oder nicht veröffentlicht wurde, überprüfen Sie im MED-V-Arbeitsbereich, ob die entsprechende Verknüpfung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d784d-121">To test that the application was published or unpublished, verify on the MED-V workspace whether the corresponding shortcut is available or not.</span></span>

<span data-ttu-id="d784d-122">**Hinweis**  Anwendungen, die in Windows XP SP3 enthalten sind und sich im Start Menü Ordner des virtuellen Computers befinden, werden nicht automatisch auf dem Host veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="d784d-122">**Note** Applications that are included in Windows XP SP3 and are located in the virtual machine Start Menu folder are not automatically published to the host.</span></span> <span data-ttu-id="d784d-123">Sie werden von Registrierungseinstellungen gesteuert, die die automatische Veröffentlichung blockieren.</span><span class="sxs-lookup"><span data-stu-id="d784d-123">They are controlled by registry settings that block automatic publishing.</span></span> <span data-ttu-id="d784d-124">Weitere Informationen finden Sie unter [Ausschlussliste für Windows Virtual PC-Anwendung](windows-virtual-pc-application-exclude-list.md).</span><span class="sxs-lookup"><span data-stu-id="d784d-124">For more information, see [Windows Virtual PC Application Exclude List](windows-virtual-pc-application-exclude-list.md).</span></span>

 

**<span data-ttu-id="d784d-125">So veröffentlichen Sie Elemente in der Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="d784d-125">To publish Control Panel items</span></span>**

1.  <span data-ttu-id="d784d-126">Erstellen Sie eine Verknüpfung auf dem virtuellen Computer, wobei das Ziel der Name des Elements ist, beispielsweise C:\\WINDOWS\\system32\\appwiz.cpl.</span><span class="sxs-lookup"><span data-stu-id="d784d-126">Create a shortcut on the virtual machine where the target is the name of the item, such as C:\\WINDOWS\\system32\\appwiz.cpl.</span></span>

    <span data-ttu-id="d784d-127">Die Verknüpfung muss entweder erstellt oder in den Ordner "%ALLUSERSPROFILE%\\Start Menu\\" oder einen der Unterordner verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="d784d-127">The shortcut must be either created in or moved to the "%ALLUSERSPROFILE%\\Start Menu\\" folder or one of its subfolders.</span></span>

    <span data-ttu-id="d784d-128">Das Element wird auf dem Hostcomputer an der entsprechenden Stelle im Start Menü Ordner des Hosts veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="d784d-128">The item will be published to the host computer in the corresponding location in the host Start Menu folder.</span></span>

2.  <span data-ttu-id="d784d-129">Starten Sie die Verknüpfung für das Element im Host.</span><span class="sxs-lookup"><span data-stu-id="d784d-129">Start the shortcut for the item in the host.</span></span>

<span data-ttu-id="d784d-130">**Vorsicht**  Wenn Sie die Verknüpfung erstellen, geben Sie% systemroot% \\control.exe nicht an.</span><span class="sxs-lookup"><span data-stu-id="d784d-130">**Caution** When you create the shortcut, do not specify %SystemRoot%\\control.exe.</span></span> <span data-ttu-id="d784d-131">Diese Anwendung wird nicht veröffentlicht, da Sie in den Registrierungseinstellungen enthalten ist, die die automatische Veröffentlichung blockieren.</span><span class="sxs-lookup"><span data-stu-id="d784d-131">This application will not be published because it is contained in the registry settings that block automatic publishing.</span></span>

 

**<span data-ttu-id="d784d-132">So behandelt MED-V die automatische Anwendungsveröffentlichung</span><span class="sxs-lookup"><span data-stu-id="d784d-132">How MED-V handles automatic application publishing</span></span>**

1.  <span data-ttu-id="d784d-133">Während der Anwendungsveröffentlichung kopiert MED-V die Verknüpfungen vom virtuellen Gastcomputer auf den Hostcomputer, indem er versucht, die im Gast vorhandene Ordnerhierarchie zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="d784d-133">During application publishing, MED-V copies the shortcuts from the guest virtual machine to the host computer by trying to match the folder hierarchy that exists in the guest.</span></span> <span data-ttu-id="d784d-134">Auf diese Weise kopiert MED-V mithilfe der folgenden Schritte Verknüpfungen aus dem Gast an den Host:</span><span class="sxs-lookup"><span data-stu-id="d784d-134">By doing this, MED-V copies shortcuts from the guest to the host by following these steps:</span></span>

    1.  <span data-ttu-id="d784d-135">MED-V versucht, einen Ordner unter Start Menu\\Programs auf dem Hostcomputer zu finden, der mit dem Ordner in dem Gast identisch ist, in dem sich die Verknüpfung befindet.</span><span class="sxs-lookup"><span data-stu-id="d784d-135">MED-V tries to locate a folder under Start Menu\\Programs in the host computer that is named the same as the folder in the guest where the shortcut resides.</span></span>

    2.  <span data-ttu-id="d784d-136">Wenn kein übereinstimmender Ordner vorhanden ist, versucht MED-V dann, einen Ordner im Start Menü Ordner des Hosts zu finden, der mit dem Ordner in dem Gast identisch ist, in dem sich die Verknüpfung befindet.</span><span class="sxs-lookup"><span data-stu-id="d784d-136">If there is no matching folder, MED-V then tries to locate a folder in the host Start Menu folder that is named the same as the folder in the guest where the shortcut resides.</span></span>

    3.  <span data-ttu-id="d784d-137">Wenn kein übereinstimmender Ordner vorhanden ist, kopiert MED-V die Verknüpfung in den Standardordner auf dem Host, den Ordner Start Menu\\Programs.</span><span class="sxs-lookup"><span data-stu-id="d784d-137">If there is no matching folder, MED-V copies the shortcut to the default folder on the host, the Start Menu\\Programs folder.</span></span>

2.  <span data-ttu-id="d784d-138">Beispiel für den Anwendungs Veröffentlichungsprozess:</span><span class="sxs-lookup"><span data-stu-id="d784d-138">Example of application publishing process:</span></span>

    1.  <span data-ttu-id="d784d-139">Wenn eine Anwendungsverknüpfung im Ordner Start Menu\\Programs\\AppShortcuts des Gastes veröffentlicht wird, sucht MED-V auf dem Hostcomputer nach einem Ordner Start Menu\\Programs\\ AppShortcuts, und wenn gefunden, wird die Verknüpfung in diesen Ordner kopiert.</span><span class="sxs-lookup"><span data-stu-id="d784d-139">If an application shortcut is published to the Start Menu\\Programs\\AppShortcuts folder in the guest, then MED-V looks in the host computer for a Start Menu\\Programs\\ AppShortcuts folder and if found, copies the shortcut to that folder.</span></span>

    2.  <span data-ttu-id="d784d-140">Wenn der Ordner nicht gefunden wird, sucht MED-V auf dem Hostcomputer nach einem Start Menu\\AppShortcuts-Ordner, und wenn gefunden, wird die Verknüpfung in diesen Ordner kopiert.</span><span class="sxs-lookup"><span data-stu-id="d784d-140">If the folder is not found, then MED-V looks in the host computer for a Start Menu\\AppShortcuts folder and if found, copies the shortcut to that folder.</span></span>

    3.  <span data-ttu-id="d784d-141">Wenn der Ordner nicht gefunden wird, kopiert MED-V die Verknüpfung in den Ordner Start Menu\\Programs.</span><span class="sxs-lookup"><span data-stu-id="d784d-141">If the folder is not found, then MED-V copies the shortcut to the Start Menu\\Programs folder.</span></span>

<span data-ttu-id="d784d-142">**Hinweis**  Ein Ordner muss bereits im Start Menü Ordner des Hostcomputers für MED-V vorhanden sein, um die Verknüpfung dort zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="d784d-142">**Note** A folder must already exist in the host computer Start Menu folder for MED-V to copy the shortcut there.</span></span> <span data-ttu-id="d784d-143">MED-V erstellt den Ordner nicht, wenn er noch nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d784d-143">MED-V does not create the folder if it does not already exist.</span></span>

 

## <span data-ttu-id="d784d-144">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d784d-144">Related topics</span></span>


[<span data-ttu-id="d784d-145">Installieren und Entfernen einer Anwendung im MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="d784d-145">Installing and Removing an Application on the MED-V Workspace</span></span>](installing-and-removing-an-application-on-the-med-v-workspace.md)

[<span data-ttu-id="d784d-146">Verwalten von Softwareupdates für MED-V-Arbeitsbereiche</span><span class="sxs-lookup"><span data-stu-id="d784d-146">Managing Software Updates for MED-V Workspaces</span></span>](managing-software-updates-for-med-v-workspaces.md)

[<span data-ttu-id="d784d-147">Liste auszuschließender Anwendungen für virtuelle Windows-PCs</span><span class="sxs-lookup"><span data-stu-id="d784d-147">Windows Virtual PC Application Exclude List</span></span>](windows-virtual-pc-application-exclude-list.md)

 

 





