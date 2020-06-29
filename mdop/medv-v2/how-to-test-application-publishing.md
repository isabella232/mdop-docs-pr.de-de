---
title: So testen Sie die Anwendungsveröffentlichung
description: So testen Sie die Anwendungsveröffentlichung
author: dansimp
ms.assetid: 17ba2e12-50a0-4f41-8300-f61f09db9f6c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 8dffb4f79ac89c7d419b27640f4f05364bd69e5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812040"
---
# <span data-ttu-id="405b4-103">So testen Sie die Anwendungsveröffentlichung</span><span class="sxs-lookup"><span data-stu-id="405b4-103">How to Test Application Publishing</span></span>


<span data-ttu-id="405b4-104">Nachdem Ihr Test der erstmaligen Einrichtung abgeschlossen wurde, können Sie überprüfen, ob die Veröffentlichungsfunktionalität der Anwendung wie erwartet funktioniert, indem Sie die folgenden Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="405b4-104">After your test of first time setup finishes, you can verify that the application publishing functionality is working as expected by performing the following tasks.</span></span>

<a href="" id="bkmk-apppub"></a>**<span data-ttu-id="405b4-105">So testen Sie die Anwendungsveröffentlichung</span><span class="sxs-lookup"><span data-stu-id="405b4-105">To test application publishing</span></span>**

1.  <span data-ttu-id="405b4-106">Überprüfen Sie, ob die für die Veröffentlichung angegebenen Anwendungen sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="405b4-106">Verify that the applications that you specified for publishing are visible.</span></span>

    <span data-ttu-id="405b4-107">Klicken Sie auf **Start** und dann auf **Alle Programme** , und suchen Sie nach den angegebenen Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="405b4-107">Click **Start** and then click **All Programs** and search for the specified applications.</span></span>

    <span data-ttu-id="405b4-108">In einigen Fällen ist es möglich, dass dieselbe Anwendung zwei Mal installiert wird, einmal auf dem Hostcomputer und einmal auf dem Gast.</span><span class="sxs-lookup"><span data-stu-id="405b4-108">In some cases, you might have the same application installed two times, one time on the host computer and one time on the guest.</span></span> <span data-ttu-id="405b4-109">Wenn eine veröffentlichte Anwendung mit demselben Namen im **Start** Menü des Hosts an demselben Speicherort veröffentlicht wird, wird Sie von der Host Anwendungsverknüpfung unterschieden, indem der Name des virtuellen Computers dem Namen der Verknüpfung hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="405b4-109">If a published application that has the same name is published to the same location on the host **Start** menu, it is distinguished from the host application shortcut by adding the virtual machine name to the shortcut name.</span></span> <span data-ttu-id="405b4-110">Bei einem virtuellen Computer mit dem Namen "MEDVHost1" kann eine Hostanwendung beispielsweise "Notepad" sein, und eine veröffentlichte Anwendung kann "Notepad (MEDVHost1)" sein.</span><span class="sxs-lookup"><span data-stu-id="405b4-110">For example, for a virtual machine named “MEDVHost1”, a host application might be "Notepad" and a published application might be "Notepad (MEDVHost1)".</span></span>

2.  <span data-ttu-id="405b4-111">Überprüfen Sie, ob die Anwendungen wie beabsichtigt funktionieren.</span><span class="sxs-lookup"><span data-stu-id="405b4-111">Verify that the applications function as intended.</span></span>

    <span data-ttu-id="405b4-112">Starten Sie auf dem Hostcomputer die von Ihnen veröffentlichten Anwendungen, und überprüfen Sie, ob Sie in Windows XP SP3 auf dem Gast geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="405b4-112">On the host computer, start the applications that you published and verify that they open in Windows XP SP3 on the guest.</span></span> <span data-ttu-id="405b4-113">Die Anwendung muss in einem Windows XP-Fenster auf dem Desktop des Hostcomputers angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="405b4-113">The application must appear in a Windows XP-style window on the host computer desktop.</span></span>

3.  <span data-ttu-id="405b4-114">Überprüfen Sie ggf., ob die Dokumentumleitung wie beabsichtigt funktioniert.</span><span class="sxs-lookup"><span data-stu-id="405b4-114">If applicable, verify that document redirection functions as intended.</span></span>

    <span data-ttu-id="405b4-115">Wenn eine veröffentlichte Anwendung auf dem Gast einen Ordner auf dem Hostsystem Laufwerk öffnen muss, stellen Sie sicher, dass Sie den angegebenen Ordner öffnen kann.</span><span class="sxs-lookup"><span data-stu-id="405b4-115">If a published application on the guest has to open a folder on the host system drive, ensure that it can open the specified folder.</span></span>

    <span data-ttu-id="405b4-116">**Wichtig**  Da Windows Virtual PC das Erstellen einer Freigabe aus einem bereits freigegebenen Ordner nicht unterstützt, erfolgt die Umleitung nicht für Dokumente, die in einem freigegebenen Ordner geöffnet werden, beispielsweise im Ordner "eigene Dateien", der sich im Netzwerk befindet.</span><span class="sxs-lookup"><span data-stu-id="405b4-116">**Important** Because Windows Virtual PC does not support creating a share from a folder that is already shared, redirection does not occur for any documents that open from a shared folder, such as a My Documents folder that is located on the network.</span></span> <span data-ttu-id="405b4-117">Weitere Informationen finden Sie unter [Problembehandlung bei Vorgängen](operations-troubleshooting-medv2.md).</span><span class="sxs-lookup"><span data-stu-id="405b4-117">For more information, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

<span data-ttu-id="405b4-118">Nachdem Sie überprüft haben, ob veröffentlichte Anwendungen installiert sind und ordnungsgemäß funktionieren, können Sie testen, ob Anwendungen dem MED-V-Arbeitsbereich hinzugefügt oder daraus entfernt werden können.</span><span class="sxs-lookup"><span data-stu-id="405b4-118">After you have verified that published applications are installed and functioning correctly, you can test whether applications can be added or removed from the MED-V workspace.</span></span>

**<span data-ttu-id="405b4-119">So testen Sie, ob eine Anwendung hinzugefügt oder entfernt werden kann</span><span class="sxs-lookup"><span data-stu-id="405b4-119">To test that an application can be added or removed</span></span>**

1.  <span data-ttu-id="405b4-120">Hinzufügen oder Entfernen einer Anwendung aus dem MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="405b4-120">Add or remove an application from the MED-V workspace.</span></span>

    <span data-ttu-id="405b4-121">Informationen zum Hinzufügen und Entfernen von Anwendungen aus einem Med-v-Arbeitsbereich finden Sie unter [Verwalten von Anwendungen, die in Med-v-Arbeitsbereichen bereitgestellt](managing-applications-deployed-to-med-v-workspaces.md)werden.</span><span class="sxs-lookup"><span data-stu-id="405b4-121">For information about how to add and remove applications from a MED-V workspace, see [Managing Applications Deployed to MED-V Workspaces](managing-applications-deployed-to-med-v-workspaces.md).</span></span>

2.  <span data-ttu-id="405b4-122">Wenn Sie eine Anwendung hinzugefügt haben, wiederholen Sie die Schritte unter [So testen Sie die Anwendungsveröffentlichung](#bkmk-apppub) , um zu überprüfen, ob die neue Anwendung wie beabsichtigt funktioniert.</span><span class="sxs-lookup"><span data-stu-id="405b4-122">If you added an application, repeat the steps in [To Test Application Publishing](#bkmk-apppub) to verify that the new application functions as intended.</span></span>

3.  <span data-ttu-id="405b4-123">Wenn Sie eine Anwendung entfernt haben, klicken Sie auf **Start** und dann auf **Alle Programme** , und stellen Sie sicher, dass alle von Ihnen entfernten Anwendungen nicht mehr aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="405b4-123">If you removed an application, click **Start** and then click **All Programs** and verify that any applications that you removed are no longer listed.</span></span>

<span data-ttu-id="405b4-124">**Hinweis**  Wenn bei der Überprüfung ihrer Publikationseinstellungen für die Anwendung Probleme auftreten, finden Sie Informationen unter [Behandeln von Vorgängen](operations-troubleshooting-medv2.md).</span><span class="sxs-lookup"><span data-stu-id="405b4-124">**Note** If you encounter any problems when verifying your application publication settings, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

<span data-ttu-id="405b4-125">Nachdem Sie das Testen der Anwendungsveröffentlichung abgeschlossen haben, können Sie andere MED-V-Arbeitsbereichskonfigurationen testen, um zu überprüfen, ob Sie wie beabsichtigt funktionieren.</span><span class="sxs-lookup"><span data-stu-id="405b4-125">After you have completed testing application publishing, you can test other MED-V workspace configurations to verify that they function as intended.</span></span>

<span data-ttu-id="405b4-126">Nachdem Sie das Testen des Med-v-Arbeitsbereichs Pakets abgeschlossen haben und überprüft haben, dass es wie beabsichtigt funktioniert, können Sie den Med-v-Arbeitsbereich für Ihr Unternehmen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="405b4-126">After you have completed testing your MED-V workspace package and have verified that it is functioning as intended, you can deploy the MED-V workspace to your enterprise.</span></span>

## <span data-ttu-id="405b4-127">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="405b4-127">Related topics</span></span>

[<span data-ttu-id="405b4-128">So testen Sie die URL-Umleitung</span><span class="sxs-lookup"><span data-stu-id="405b4-128">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

[<span data-ttu-id="405b4-129">So überprüfen Sie erstmalige Einstellungen für das Setup</span><span class="sxs-lookup"><span data-stu-id="405b4-129">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

[<span data-ttu-id="405b4-130">Bereitstellen des MED-V-Arbeitsbereichspakets</span><span class="sxs-lookup"><span data-stu-id="405b4-130">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)

 

 





