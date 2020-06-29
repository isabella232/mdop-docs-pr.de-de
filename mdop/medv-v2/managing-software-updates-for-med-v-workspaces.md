---
title: Verwalten von Softwareupdates für MED-V-Arbeitsbereiche
description: Verwalten von Softwareupdates für MED-V-Arbeitsbereiche
author: dansimp
ms.assetid: a28d6dcd-cb9f-46ba-8dac-1d990837a3a3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 696238a2f5ad9b7e5120f75f6cd09d890d12519b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810780"
---
# <span data-ttu-id="22af5-103">Verwalten von Softwareupdates für MED-V-Arbeitsbereiche</span><span class="sxs-lookup"><span data-stu-id="22af5-103">Managing Software Updates for MED-V Workspaces</span></span>


<span data-ttu-id="22af5-104">Für die Bereitstellung von Softwareupdates für die Anwendungen im bereitgestellten MED-V-Arbeitsbereich stehen Ihnen verschiedene Optionen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="22af5-104">You have several different options available to you for providing software updates for the applications in the deployed MED-V workspace.</span></span>

<span data-ttu-id="22af5-105">**Hinweis**  Informationen dazu, wie Sie die Konfigurationseinstellungen angeben, die definieren, wie Med-v automatische Updates erhält, finden Sie unter [Verwalten von automatischen Updates für med-v-Arbeitsbereiche](managing-automatic-updates-for-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="22af5-105">**Note** For information about how to specify the configuration settings that define how MED-V receives automatic updates, see [Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md).</span></span>

 

**<span data-ttu-id="22af5-106">Aktualisieren von Software in einem MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="22af5-106">Updating Software in a MED-V Workspace</span></span>**

1.  **<span data-ttu-id="22af5-107">Verwenden eines elektronischen Software Verteilungssystems</span><span class="sxs-lookup"><span data-stu-id="22af5-107">Using an Electronic Software Distribution System</span></span>**

    <span data-ttu-id="22af5-108">Wenn Ihr Unternehmen ein ESD-System (Electronic Software Distribution System) zum Bereitstellen von Software verwendet, können Sie es verwenden, um Softwareupdates für Anwendungen in MED-V-Arbeitsbereichen bereitzustellen, genauso wie Sie Updates für Anwendungen auf physischen Computern bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="22af5-108">If your organization uses an Electronic Software Distribution System (ESD) system to deploy software, you can use it to provide software updates for applications on MED-V workspaces just as you provide updates for applications on physical computers.</span></span>

2.  **<span data-ttu-id="22af5-109">Verwenden von Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="22af5-109">Using Group Policy</span></span>**

    <span data-ttu-id="22af5-110">Wenn Ihre Organisation Software mithilfe von Gruppenrichtlinien bereitstellt, können Sie Sie verwenden, um Softwareupdates für Anwendungen in MED-V-Arbeitsbereichen bereitzustellen, genauso wie Sie Updates für Anwendungen auf physischen Computern bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="22af5-110">If your organization deploys software by using Group Policy, you can use it to provide software updates for applications on MED-V workspaces just as you provide updates for applications on physical computers.</span></span>

3.  **<span data-ttu-id="22af5-111">Verwenden von Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="22af5-111">Using Application Virtualization (APP-V)</span></span>**

    <span data-ttu-id="22af5-112">Wenn Sie Med-v zusammen mit App-v verwenden, können Sie Softwareupdates für Anwendungen im Med-v-Arbeitsbereich bereitstellen, indem Sie die Schritte ausführen, die für App-v zum Aktualisieren von Software erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="22af5-112">If you use MED-V together with App-V, you can provide software updates to applications in the MED-V workspace by following the steps that are required by App-V for updating software.</span></span> <span data-ttu-id="22af5-113">Weitere Informationen finden Sie unter [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) .</span><span class="sxs-lookup"><span data-stu-id="22af5-113">For more information, see [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939).</span></span>

4.  **<span data-ttu-id="22af5-114">Aktualisieren der Software im Core-Abbild</span><span class="sxs-lookup"><span data-stu-id="22af5-114">Updating Software in the Core Image</span></span>**

    <span data-ttu-id="22af5-115">Obwohl es sich nicht um eine MED-V-bewährte Methode handelt, können Sie Softwareupdates für Anwendungen im Core-Abbild installieren.</span><span class="sxs-lookup"><span data-stu-id="22af5-115">Although not considered a MED-V best practice, you can install software updates to applications on the core image.</span></span> <span data-ttu-id="22af5-116">Nachdem Sie die Updates installiert haben, können Sie den MED-V-Arbeitsbereich wieder in Ihrem Unternehmen bereitstellen, genauso wie Sie ihn ursprünglich bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="22af5-116">After you have installed the updates, you can then redeploy the MED-V workspace back out to your enterprise just as you deployed it originally.</span></span>

    <span data-ttu-id="22af5-117">**Wichtig**  Diese Methode zum Verwalten von Softwareupdates wird nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="22af5-117">**Important** We do not recommend this method of managing software updates.</span></span> <span data-ttu-id="22af5-118">Wenn Sie außerdem Software im kernbild aktualisieren und den MED-V-Arbeitsbereich wieder in Ihrem Unternehmen bereitstellen, muss das erstmalige Setup erneut ausgeführt werden, und alle auf dem virtuellen Computer gespeicherten Daten gehen verloren.</span><span class="sxs-lookup"><span data-stu-id="22af5-118">In addition, if you update software in the core image and redeploy the MED-V workspace back out to your enterprise, first time setup must run again, and any data saved in the virtual machine is lost.</span></span>

     

## <span data-ttu-id="22af5-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="22af5-119">Related topics</span></span>


[<span data-ttu-id="22af5-120">Verwalten von automatischen Updates für MED-V-Arbeitsbereiche</span><span class="sxs-lookup"><span data-stu-id="22af5-120">Managing Automatic Updates for MED-V Workspaces</span></span>](managing-automatic-updates-for-med-v-workspaces.md)

[<span data-ttu-id="22af5-121">So testen Sie die Anwendungsveröffentlichung</span><span class="sxs-lookup"><span data-stu-id="22af5-121">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="22af5-122">Informationen zum Veröffentlichen und Aufheben der Veröffentlichung einer Anwendung im MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="22af5-122">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





