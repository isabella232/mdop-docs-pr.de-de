---
title: So überprüfen Sie erstmalige Einstellungen für das Setup
description: So überprüfen Sie erstmalige Einstellungen für das Setup
author: dansimp
ms.assetid: e8a07d4c-5786-4455-ac43-2deac4042efd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859d627ec90fbc26d18019062d5e316f907cec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804667"
---
# <span data-ttu-id="b8dbe-103">So überprüfen Sie erstmalige Einstellungen für das Setup</span><span class="sxs-lookup"><span data-stu-id="b8dbe-103">How to Verify First Time Setup Settings</span></span>


<span data-ttu-id="b8dbe-104">Während der Test der erstmaligen Einrichtung ausgeführt wird oder nachdem er abgeschlossen wurde, können Sie die Einstellungen überprüfen, die Sie in Ihrem MED-V-Arbeitsbereich konfiguriert haben, indem Sie die folgenden Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-104">While your test of first time setup is running or after it finishes, you can verify the settings that you configured in your MED-V workspace by performing the following tasks.</span></span>

<span data-ttu-id="b8dbe-105">**Hinweis**  Informationen dazu, wie Sie den erfolgreichen Abschluss der erstmaligen Einrichtung in Ihrem Unternehmen nach der Bereitstellung überwachen können, finden Sie unter über [Wachen von MED-V-Arbeitsbereichs Bereitstellungen](monitoring-med-v-workspace-deployments.md).</span><span class="sxs-lookup"><span data-stu-id="b8dbe-105">**Note** For information about how to monitor the successful completion of first time setup throughout your enterprise after deployment, see [Monitoring MED-V Workspace Deployments](monitoring-med-v-workspace-deployments.md).</span></span>

 

**<span data-ttu-id="b8dbe-106">So überprüfen Sie die Einstellungen während der erstmaligen Einrichtung</span><span class="sxs-lookup"><span data-stu-id="b8dbe-106">To verify settings during first time setup</span></span>**

1.  <span data-ttu-id="b8dbe-107">Überprüfen Sie Folgendes, während die erstmalige Einrichtung ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="b8dbe-107">While first time setup is running, verify the following:</span></span>

    <span data-ttu-id="b8dbe-108">Wenn Sie den **unbeaufsichtigten** Modus angegeben haben, stellen Sie sicher, dass der virtuelle Computer nicht angezeigt wird, wenn die erstmalige Einrichtung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-108">If you specified **Unattended** mode, verify that the virtual machine does not appear when first time setup is running.</span></span>

    <span data-ttu-id="b8dbe-109">Wenn Sie den beaufsichtigten Modus angegeben haben, überprüfen Sie, ob der virtuelle Computer angezeigt wird und alle Felder angezeigt werden, für die Benutzereingaben erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-109">If you specified attended mode, verify that the virtual machine appears and that all fields that require user input are displayed.</span></span>

2.  <span data-ttu-id="b8dbe-110">Sie können auch den vollständigen erstmaligen Setupprozess überwachen, indem Sie den virtuellen Computer anzeigen, wenn die erstmalige Einrichtung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-110">You can also monitor the complete first time setup process by viewing the virtual machine when first time setup is running.</span></span> <span data-ttu-id="b8dbe-111">Gehen Sie hierzu folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="b8dbe-111">To do this, follow these steps:</span></span>

    1.  <span data-ttu-id="b8dbe-112">Öffnen Sie die Windows Virtual PC-Konsole.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-112">Open the Windows Virtual PC Console.</span></span>

        <span data-ttu-id="b8dbe-113">Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Windows Virtual PC**, und klicken Sie dann auf **Windows Virtual PC**.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-113">Click **Start**, click **All Programs**, click **Windows Virtual PC**, and then click **Windows Virtual PC**.</span></span>

    2.  <span data-ttu-id="b8dbe-114">Starten Sie MED-V, wenn es noch nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-114">Start MED-V if it is not already running.</span></span>

        <span data-ttu-id="b8dbe-115">Wenn Sie nicht bereits vorhanden sind, wird in kurzer Zeit ein virtueller Computer mit dem Namen des bereitgestellten MED-V-Arbeitsbereichs in der Liste der virtuellen Computer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-115">If not already present, in a short time, a virtual machine with the name of the deployed MED-V workspace appears in the list of virtual machines.</span></span>

    3.  <span data-ttu-id="b8dbe-116">Doppelklicken Sie auf den MED-V-virtuellen Computer, um ihn zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-116">Double-click the MED-V virtual machine to open it.</span></span>

        <span data-ttu-id="b8dbe-117">Sie können den virtuellen MED-V-Computer beobachten, wenn er eingerichtet wird, und Sie können eine Problembehandlung für die Mini Einrichtung ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-117">You can observe the MED-V virtual machine when it is being set up, and you can troubleshoot the Mini-Setup procedure.</span></span> <span data-ttu-id="b8dbe-118">Überprüfen Sie die Informationen in den verschiedenen Bildschirmen während ihrer Vorgehensweise, wie etwa die Konfiguration von Netzwerkeinstellungen, Informationen zu Computer Domänenbeitritt, Konfigurieren des Gast-Agents, Einrichten persönlicher Einstellungen und Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-118">Verify the information in the different screens as they go by, such as configuring networking settings, computer domain join information, configuring of the Guest Agent, set up of personal settings, and shutdown.</span></span>

    4.  <span data-ttu-id="b8dbe-119">Der virtuelle Computer wird automatisch geschlossen, wenn die erstmalige Einrichtung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-119">The virtual machine closes automatically when first time setup finishes.</span></span>

        <span data-ttu-id="b8dbe-120">**Hinweis**  Sie können das Fenster des virtuellen Computers jederzeit schließen, und das erstmalige Setup wird fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-120">**Note** You can close the virtual machine window at any time and first time setup continues.</span></span>

         

**<span data-ttu-id="b8dbe-121">So überprüfen Sie die Einstellungen nach Abschluss der erstmaligen Einrichtung</span><span class="sxs-lookup"><span data-stu-id="b8dbe-121">To verify settings after first time setup finishes</span></span>**

1.  <span data-ttu-id="b8dbe-122">Stellen Sie sicher, dass die erstmalige Einrichtung erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-122">Ensure that first time setup finished successfully.</span></span>

2.  <span data-ttu-id="b8dbe-123">Überprüfen Sie, ob der MED-V-Arbeitsbereich ordnungsgemäß eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-123">Verify that the MED-V workspace is set up correctly.</span></span>

    1.  <span data-ttu-id="b8dbe-124">Öffnen Sie die Windows Virtual PC-Konsole.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-124">Open the Windows Virtual PC Console.</span></span>

        <span data-ttu-id="b8dbe-125">Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Windows Virtual PC**, und klicken Sie dann auf **Windows Virtual PC**.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-125">Click **Start**, click **All Programs**, click **Windows Virtual PC**, and then click **Windows Virtual PC**.</span></span>

    2.  <span data-ttu-id="b8dbe-126">Doppelklicken Sie auf Ihren installierten MED-V-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-126">Double-click your installed MED-V workspace.</span></span>

        <span data-ttu-id="b8dbe-127">Wenn der MED-V-Arbeitsbereich bereits eine virtuelle Anwendung ausführt, werden Sie möglicherweise aufgefordert, die Anwendung zu schließen, bevor Sie den virtuellen Computer öffnen können.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-127">If the MED-V workspace is already running a virtual application, you might be prompted to close the application before you can open the virtual machine.</span></span>

    3.  <span data-ttu-id="b8dbe-128">Klicken Sie im MED-V-Arbeitsbereich mit der rechten Maustaste auf Arbeits **Platz**, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-128">In the MED-V workspace, right-click **My Computer**, and then click **Properties**.</span></span>

    4.  <span data-ttu-id="b8dbe-129">Überprüfen Sie, ob der MED-V-Arbeitsbereich der richtigen Domäne beigetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-129">Verify that the MED-V workspace joined the correct domain.</span></span> <span data-ttu-id="b8dbe-130">Wenn Sie auf Ihre Organisation zutreffen, testen Sie die Domänenmitgliedschaft, indem Sie zwei verschiedene Domänen angeben, um zu überprüfen, ob die Gast Domäne von der Hostdomäne überschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-130">If applicable to your organization, test domain joining by specifying two different domains to verify that the guest domain is overridden by the host domain.</span></span>

    5.  <span data-ttu-id="b8dbe-131">Überprüfen Sie, ob der MED-V-Arbeitsbereich der von Ihnen angegebenen Domänen Organisationseinheit beigetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-131">Verify that the MED-V workspace joined the domain organizational unit that you specified.</span></span>

    6.  <span data-ttu-id="b8dbe-132">Wenn Sie die Computernamen Maske angegeben haben, überprüfen Sie, ob der Name des neuen Computers mit dem angegebenen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-132">If you specified the computer name mask, verify that the new computer name matches what was specified.</span></span>

3.  <span data-ttu-id="b8dbe-133">Überprüfen Sie, ob die von Ihnen angegebenen Gebietsschemaeinstellungen richtig sind.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-133">Verify that the locale settings that you specified are correct.</span></span>

    1.  <span data-ttu-id="b8dbe-134">Klicken Sie im MED-V-Arbeitsbereich auf **Start** und dann auf **System**Steuerung.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-134">In the MED-V workspace, click **Start** and then click **Control Panel**.</span></span>

    2.  <span data-ttu-id="b8dbe-135">Überprüfen Sie die angegebenen Konfigurationseinstellungen, beispielsweise **Datum und Uhrzeit** sowie **Region und Sprache**.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-135">Verify your specified configuration settings, for example, **Date and Time** and **Regional and Language**.</span></span>

<span data-ttu-id="b8dbe-136">**Hinweis**  Wenn bei der Überprüfung der Einstellungen für die erstmalige Einrichtung Probleme auftreten, lesen Sie [Problembehandlung bei Vorgängen](operations-troubleshooting-medv2.md).</span><span class="sxs-lookup"><span data-stu-id="b8dbe-136">**Note** If you encounter any problems when verifying your first time setup settings, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

 

<span data-ttu-id="b8dbe-137">Nachdem Sie überprüft haben, dass die Einstellungen für die erstmalige Einrichtung korrekt sind, können Sie andere MED-V-Arbeitsbereichskonfigurationen testen, um zu überprüfen, ob Sie wie beabsichtigt funktionieren, beispielsweise die Veröffentlichung von Anwendungen und die URL-Umleitung.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-137">After you have verified that your first time setup settings are correct, you can test other MED-V workspace configurations to verify that they function as intended, such as application publishing and URL redirection.</span></span>

<span data-ttu-id="b8dbe-138">Nachdem Sie alle Tests Ihres Med-v-Arbeitsbereichs Pakets abgeschlossen haben und überprüft haben, dass es wie beabsichtigt funktioniert, können Sie den Med-v-Arbeitsbereich für Ihr Unternehmen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b8dbe-138">After you have completed all testing of your MED-V workspace package and have verified that it is functioning as intended, you can deploy the MED-V workspace to your enterprise.</span></span>

## <span data-ttu-id="b8dbe-139">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b8dbe-139">Related topics</span></span>


[<span data-ttu-id="b8dbe-140">So testen Sie die Anwendungsveröffentlichung</span><span class="sxs-lookup"><span data-stu-id="b8dbe-140">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="b8dbe-141">So testen Sie die URL-Umleitung</span><span class="sxs-lookup"><span data-stu-id="b8dbe-141">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

[<span data-ttu-id="b8dbe-142">Bereitstellen des MED-V-Arbeitsbereichspakets</span><span class="sxs-lookup"><span data-stu-id="b8dbe-142">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)

[<span data-ttu-id="b8dbe-143">Verwalten von MED-V-Arbeitsbereichseinstellungen</span><span class="sxs-lookup"><span data-stu-id="b8dbe-143">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





