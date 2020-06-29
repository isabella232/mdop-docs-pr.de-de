---
title: Installieren und Entfernen einer Anwendung im MED-V-Arbeitsbereich
description: Installieren und Entfernen einer Anwendung im MED-V-Arbeitsbereich
author: dansimp
ms.assetid: 24f32720-51ab-4385-adfe-4f5a65e45fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 22cb98c167b53b1b206b8b5be2ba18fc0fba4f06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812223"
---
# <span data-ttu-id="302e6-103">Installieren und Entfernen einer Anwendung im MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="302e6-103">Installing and Removing an Application on the MED-V Workspace</span></span>


<span data-ttu-id="302e6-104">Anwendungen, die mit dem Betriebssystem "Host" nicht kompatibel sind, können im Med-v-Arbeitsbereich ausgeführt und im Med-v-Arbeitsbereich auf die gleiche Weise wie auf dem Hostcomputer, im **Startmenü** oder mithilfe einer localhost-Verknüpfung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="302e6-104">Applications that are incompatible with the host operating system can be run in the MED-V workspace and opened in the MED-V workspace in the same manner in which they are opened from the host computer, on the **Start** menu or by using a localhost shortcut.</span></span>

<span data-ttu-id="302e6-105">Nachdem Sie einen Med-v-Arbeitsbereich bereitgestellt haben, stehen Ihnen verschiedene Optionen zum Installieren und Entfernen von Anwendungen im Med-v-Arbeitsbereich zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="302e6-105">After you have deployed a MED-V workspace, you have several different options available to you for installing and removing applications in the MED-V workspace.</span></span> <span data-ttu-id="302e6-106">Zu den folgenden Optionen gehören:</span><span class="sxs-lookup"><span data-stu-id="302e6-106">These options include the following:</span></span>

-   [<span data-ttu-id="302e6-107">Verwenden von Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="302e6-107">Using Group Policy</span></span>](#bkmk-grouppolicy)

-   [<span data-ttu-id="302e6-108">Verwenden eines elektronischen Software Verteilungssystems</span><span class="sxs-lookup"><span data-stu-id="302e6-108">Using an Electronic Software Distribution System</span></span>](#bkmk-esd)

-   [<span data-ttu-id="302e6-109">Verwenden von Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="302e6-109">Using Application Virtualization (APP-V)</span></span>](#bkmk-appv)

-   [<span data-ttu-id="302e6-110">Aktualisieren des Kern Abbilds</span><span class="sxs-lookup"><span data-stu-id="302e6-110">Updating the Core Image</span></span>](#bkmk-coreimage)

<span data-ttu-id="302e6-111">**Wichtig**  Wenn Sie sicherstellen möchten, dass eine installierte Anwendung automatisch auf dem Host veröffentlicht wird, installieren Sie die Anwendung auf dem virtuellen Computer für **alle Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="302e6-111">**Important** To make sure that an installed application is automatically published to the host, install the application on the virtual machine for **All Users**.</span></span> <span data-ttu-id="302e6-112">Weitere Informationen zur Anwendungsveröffentlichung finden Sie unter [veröffentlichen und Aufheben der Veröffentlichung einer Anwendung im MED-V-Arbeitsbereich](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="302e6-112">For more information about application publishing, see [How to Publish and Unpublish an Application on the MED-V Workspace](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span></span>

 

<span data-ttu-id="302e6-113">**Tipp**  Med-v unterstützt keine Gast-zu-Host-Umleitung für die Inhaltsbehandlung, wie das Doppelklicken auf ein Microsoft Word-Dokument in Internet Explorer im Med-v-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="302e6-113">**Tip** MED-V does not support guest-to-host redirection for content handling, such as double-clicking a Microsoft Word document in Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="302e6-114">Daher müssen die erforderlichen Anwendungen wie Microsoft Word in MED-V Workspace installiert werden, um die standardmäßige Inhalts Behandlungsfunktion bereitzustellen, die ein Endbenutzer möglicherweise erwartet.</span><span class="sxs-lookup"><span data-stu-id="302e6-114">Therefore, the required applications, such as Microsoft Word, must be installed in MED-V workspace to provide the default content handling functionality that an end user might expect.</span></span>

 

## <a href="" id="bkmk-grouppolicy"></a> <span data-ttu-id="302e6-115">Hinzufügen und Entfernen von Anwendungen mithilfe von Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="302e6-115">Adding and Removing Applications by Using Group Policy</span></span>


<span data-ttu-id="302e6-116">Sie können Gruppenrichtlinien-und Gruppenrichtlinienobjekte verwenden, um Anwendungen allen oder einigen MED-V-Arbeitsbereichen in Ihrem Unternehmen zuzuweisen oder zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="302e6-116">You can use Group Policy and Group Policy objects to assign or publish applications to all or some MED-V workspaces in your enterprise.</span></span> <span data-ttu-id="302e6-117">Bei zugewiesenen Anwendungen wird die Anwendung im **Startmenü** angezeigt, wenn sich ein Endbenutzer bei seinem Computer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="302e6-117">For assigned applications, when an end user logs on to their computer, the application appears on the **Start** menu.</span></span> <span data-ttu-id="302e6-118">Wenn Sie die neue Anwendung zum ersten Mal auswählen, wird die Anwendung installiert und kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="302e6-118">When they select the new application for the first time, the application installs and is ready for use.</span></span> <span data-ttu-id="302e6-119">Für veröffentlichte Anwendungen wird die Anwendung nicht im **Startmenü** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="302e6-119">For published applications, the application does not appear on the **Start** menu.</span></span> <span data-ttu-id="302e6-120">Sie steht nur für den Endbenutzer zur Verfügung, indem Sie in der **System** Steuerung **Software** verwenden oder eine Datei öffnen, die der Anwendung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="302e6-120">It is only available for the end user to install by using **Add or Remove Programs** in **Control Panel** or by opening a file that is associated with the application.</span></span>

<span data-ttu-id="302e6-121">Sie können auch Gruppenrichtlinien-und Gruppenrichtlinienobjekte auf die gleiche Weise verwenden, um Anwendungen aus dem MED-V-Arbeitsbereich zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="302e6-121">You can also use Group Policy and Group Policy objects in the same manner to remove applications from the MED-V workspace.</span></span>

<span data-ttu-id="302e6-122">Weitere Informationen zum Hinzufügen und Entfernen von Anwendungen mithilfe von Gruppenrichtlinien finden Sie unter [Gruppenrichtlinien-Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .</span><span class="sxs-lookup"><span data-stu-id="302e6-122">For more information about how to add and remove applications by using Group Policy, see [Group Policy Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) (https://go.microsoft.com/fwlink/?LinkId=195931).</span></span>

## <a href="" id="bkmk-esd"></a> <span data-ttu-id="302e6-123">Hinzufügen und Entfernen von Anwendungen mithilfe eines ESD-Systems</span><span class="sxs-lookup"><span data-stu-id="302e6-123">Adding and Removing Applications by Using an ESD System</span></span>


<span data-ttu-id="302e6-124">Ein ESD-System (Electronic Software Distribution) ist so konzipiert, dass Software und andere Informationen auf vielen verschiedenen Computern über Netzwerkverbindungen effizient bereitgestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="302e6-124">An electronic software distribution (ESD) system is designed to efficiently deploy software and other information to many different computers over network connections.</span></span> <span data-ttu-id="302e6-125">Wenn Ihre Organisation ein ESD-System zum Bereitstellen von Software verwendet, können Sie diese zum Hinzufügen und Entfernen von Anwendungen in MED-V-Arbeitsbereichen verwenden, genauso wie beim Hinzufügen und Entfernen von Anwendungen auf physischen Computern.</span><span class="sxs-lookup"><span data-stu-id="302e6-125">If your organization uses an ESD system to deploy software, you can use it to add and remove applications on MED-V workspaces just as you add and remove applications on physical computers.</span></span>

## <a href="" id="bkmk-appv"></a> <span data-ttu-id="302e6-126">Hinzufügen und Entfernen von Anwendungen mithilfe von App-V</span><span class="sxs-lookup"><span data-stu-id="302e6-126">Adding and Removing Applications by Using APP-V</span></span>


<span data-ttu-id="302e6-127">Microsoft Application Virtualization (App-V) bietet die Verwaltungsfunktion, um Anwendungen für Endbenutzercomputer verfügbar zu machen, ohne die Anwendungen direkt auf diesen Computern installieren zu müssen.</span><span class="sxs-lookup"><span data-stu-id="302e6-127">Microsoft Application Virtualization (App-V) provides the administrative capability to make applications available to end-user computers without having to install the applications directly on those computers.</span></span> <span data-ttu-id="302e6-128">Möglicherweise möchten Sie Med-v und App-v zusammen verwenden, wenn Ihre Organisation beispielsweise Anwendungen aufweist, die Sie mit App-v in Windows XP sequenziert haben, und Sie durch eine erneute Sequenzierung Ihre Migration zu Windows 7 verzögern würden.</span><span class="sxs-lookup"><span data-stu-id="302e6-128">You might want to use MED-V and App-V together if, for example, your organization has applications that you sequenced with App-V in Windows XP, and re-sequencing them would delay your migration to Windows 7.</span></span>

<span data-ttu-id="302e6-129">Sie können Med-v zusammen mit App-v verwenden, um virtuelle Anwendungen in einem bereitgestellten Med-v-Arbeitsbereich hinzuzufügen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="302e6-129">You can use MED-V together with App-V to add and remove virtual applications on a deployed MED-V workspace.</span></span> <span data-ttu-id="302e6-130">Zum Verwalten von Anwendungen auf diese Weise müssen Sie zuerst den App-v-Agent auf dem Med-v-Gastbetriebssystem installieren.</span><span class="sxs-lookup"><span data-stu-id="302e6-130">To manage applications in this manner, you must first install the App-V agent on the MED-V guest operating system.</span></span> <span data-ttu-id="302e6-131">Sie können dann App-v im Med-v-Arbeitsbereich verwenden, um die virtuellen Anwendungen hinzuzufügen und zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="302e6-131">You can then use App-V in the MED-V workspace to add and remove the virtual applications.</span></span>

<span data-ttu-id="302e6-132">Informationen zum Installieren und Verwenden von App-V finden Sie unter [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) .</span><span class="sxs-lookup"><span data-stu-id="302e6-132">For information about how to install and use App-V, see [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939).</span></span>

<span data-ttu-id="302e6-133">**Wichtig**  App-v-Anwendungen, die Sie im Med-v-Arbeitsbereich veröffentlichen, weisen Dateitypzuordnungen auf, die nicht vom Hostcomputer auf den virtuellen Gastcomputer umgeleitet werden können.</span><span class="sxs-lookup"><span data-stu-id="302e6-133">**Important** App-V applications that you publish to the MED-V workspace have file-type associations that cannot redirect from the host computer to the guest virtual machine.</span></span> <span data-ttu-id="302e6-134">Der Endbenutzer kann jedoch weiterhin auf diese Dateitypen zugreifen, indem Sie auf **Datei**und dann in der veröffentlichten App-V-Anwendung auf **Öffnen** klicken.</span><span class="sxs-lookup"><span data-stu-id="302e6-134">However, the end user can still access these file types by clicking **File**, and then by clicking **Open** on the published App-V application.</span></span>

<span data-ttu-id="302e6-135">Wenn Sie die Umleitung dieser Dateitypzuordnungen erzwingen möchten, geben Sie App-V für zugeordnete Dateitypzuordnungen an, indem Sie Folgendes an einer Eingabeaufforderung auf dem virtuellen Gastcomputer eingeben: **SFTMIME/Query obj: Type**.</span><span class="sxs-lookup"><span data-stu-id="302e6-135">To force redirection of those file-type associations, query App-V for mapped file type associations by typing the following at a command prompt in the guest virtual machine: **sftmime /QUERY OBJ:TYPE**.</span></span> <span data-ttu-id="302e6-136">Ordnen Sie dann diese Dateitypzuordnungen auf dem Hostcomputer zu.</span><span class="sxs-lookup"><span data-stu-id="302e6-136">Then, map those file type associations in the host computer.</span></span>

 

## <a href="" id="bkmk-coreimage"></a> <span data-ttu-id="302e6-137">Hinzufügen und Entfernen von Anwendungen im Core-Abbild</span><span class="sxs-lookup"><span data-stu-id="302e6-137">Adding and Removing Applications on the Core Image</span></span>


<span data-ttu-id="302e6-138">Obwohl es sich nicht um ein MED-V-bewährtes Verfahren handelt, können Sie Anwendungen direkt im kernbild hinzufügen und entfernen.</span><span class="sxs-lookup"><span data-stu-id="302e6-138">Although not considered a MED-V best practice, you can add and remove applications directly on the core image.</span></span> <span data-ttu-id="302e6-139">Nachdem Sie eine Anwendung hinzugefügt oder entfernt haben, können Sie den MED-V-Arbeitsbereich wieder in Ihrem Unternehmen bereitstellen, genauso wie Sie ihn ursprünglich bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="302e6-139">After you have added or removed an application, you can redeploy the MED-V workspace back out to your enterprise just as you deployed it originally.</span></span>

<span data-ttu-id="302e6-140">Weitere Informationen zum Hinzufügen oder Entfernen von Anwendungen für das kernbild finden Sie unter [Installieren von Anwendungen auf einem Windows Virtual PC-Abbild](installing-applications-on-a-windows-virtual-pc-image.md).</span><span class="sxs-lookup"><span data-stu-id="302e6-140">For more information about how to add or remove applications on the core image, see [Installing Applications on a Windows Virtual PC Image](installing-applications-on-a-windows-virtual-pc-image.md).</span></span>

<span data-ttu-id="302e6-141">**Wichtig**  Diese Methode zum Verwalten von Anwendungen wird nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="302e6-141">**Important** We do not recommend this method of managing applications.</span></span> <span data-ttu-id="302e6-142">Wenn Sie Anwendungen im kernbild hinzufügen oder entfernen und den MED-V-Arbeitsbereich wieder in Ihrem Unternehmen bereitstellen, muss das erstmalige Setup erneut ausgeführt werden, und alle auf dem virtuellen Computer gespeicherten Daten gehen verloren.</span><span class="sxs-lookup"><span data-stu-id="302e6-142">If you add or remove applications on the core image and redeploy the MED-V workspace back out to your enterprise, first time setup must run again, and any data saved on the virtual machine is lost.</span></span>

 

<span data-ttu-id="302e6-143">**Hinweis**  Obwohl eine Anwendung in einem MED-V-Arbeitsbereich installiert ist, müssen Sie möglicherweise auch die Anwendung veröffentlichen, bevor Sie für den Endbenutzer verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="302e6-143">**Note** Even though an application is installed into a MED-V workspace, you might also have to publish the application before it becomes available to the end user.</span></span> <span data-ttu-id="302e6-144">Möglicherweise müssen Sie eine installierte Anwendung veröffentlichen, wenn die Installation im **Startmenü** nicht automatisch eine Verknüpfung erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="302e6-144">For example, you might have to publish an installed application if the installation did not automatically create a shortcut on the **Start** menu.</span></span> <span data-ttu-id="302e6-145">Wenn Sie die Veröffentlichung einer Anwendung aufheben möchten, müssen Sie möglicherweise eine Verknüpfung manuell aus dem **Startmenü** entfernen.</span><span class="sxs-lookup"><span data-stu-id="302e6-145">Likewise, to unpublish an application, you might have to manually remove a shortcut from the **Start** menu.</span></span>

<span data-ttu-id="302e6-146">Standardmäßig werden die meisten Anwendungen zu dem Zeitpunkt veröffentlicht, zu dem Sie installiert werden, wenn Verknüpfungen automatisch erstellt und aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="302e6-146">By default, most applications are published at the time that they are installed, when shortcuts are automatically created and enabled.</span></span>

 

## <span data-ttu-id="302e6-147">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="302e6-147">Related topics</span></span>


[<span data-ttu-id="302e6-148">So testen Sie die Anwendungsveröffentlichung</span><span class="sxs-lookup"><span data-stu-id="302e6-148">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="302e6-149">Informationen zum Veröffentlichen und Aufheben der Veröffentlichung einer Anwendung im MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="302e6-149">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





