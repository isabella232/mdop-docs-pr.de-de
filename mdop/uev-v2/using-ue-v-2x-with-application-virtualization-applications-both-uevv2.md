---
title: Verwenden von UE-V 2. x mit Application Virtualization-Anwendungen
description: Verwenden von UE-V 2. x mit Application Virtualization-Anwendungen
author: dansimp
ms.assetid: 4644b810-fc48-4fd0-96e4-2fc6cd64d8ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221d21c5815b36b57a04a0299352e5fe64f657c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812256"
---
# <span data-ttu-id="d3844-103">Verwenden von UE-V 2. x mit Application Virtualization-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="d3844-103">Using UE-V 2.x with Application Virtualization Applications</span></span>


<span data-ttu-id="d3844-104">Microsoft User Experience Virtualization (UE-v) 2,0, 2,1 und 2,1 SP1 unterstützen Microsoft Application Virtualization (app-v)-Anwendungen ohne erforderliche Änderungen am APP-v-Paket oder der UE-v-Vorlage.</span><span class="sxs-lookup"><span data-stu-id="d3844-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 support Microsoft Application Virtualization (App-V) applications without any required modifications to either the App-V package or the UE-V template.</span></span> <span data-ttu-id="d3844-105">Ein weiterer Schritt ist jedoch erforderlich, da Sie den UE-v-Generator nicht direkt in einer virtualisierten App-v-Anwendung ausführen können.</span><span class="sxs-lookup"><span data-stu-id="d3844-105">However, an additional step is required because you cannot run the UE-V Generator directly on a virtualized App-V application.</span></span> <span data-ttu-id="d3844-106">Stattdessen müssen Sie die Anwendung lokal installieren, die Vorlage generieren und dann die Vorlage auf die virtualisierte Anwendung anwenden.</span><span class="sxs-lookup"><span data-stu-id="d3844-106">Instead, you must install the application locally, generate the template, and then apply the template to the virtualized application.</span></span> <span data-ttu-id="d3844-107">UE-v unterstützt App-v 4,5, App-v 4,6 und App-v 5,0-Pakete.</span><span class="sxs-lookup"><span data-stu-id="d3844-107">UE-V supports App-V 4.5, App-V 4.6, and App-V 5.0 packages.</span></span>

## <span data-ttu-id="d3844-108">Synchronisierung der UE-v-Einstellungen für App-v-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="d3844-108">UE-V settings synchronization for App-V applications</span></span>


<span data-ttu-id="d3844-109">UE-v überwacht, wenn eine Anwendung durch den Programmnamen und optional durch Dateiversionsnummern und Produktversionsnummern geöffnet wird, unabhängig davon, ob die Anwendung lokal oder virtuell mithilfe von App-v installiert wird.</span><span class="sxs-lookup"><span data-stu-id="d3844-109">UE-V monitors when an application opens by the program name and, optionally, by file version numbers and product version numbers, whether the application is installed locally or virtually by using App-V.</span></span> <span data-ttu-id="d3844-110">Wenn die Anwendung gestartet wird, überwacht UE-v den App-v-Prozess, wendet alle Einstellungen an, die im Einstellungsspeicher Pfad des Benutzers gespeichert sind, und ermöglicht dann, dass die Anwendung normal gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d3844-110">When the application starts, UE-V monitors the App-V process, applies any settings that are stored in the user's settings storage path, and then enables the application to start normally.</span></span> <span data-ttu-id="d3844-111">UE-v überwacht App-v-Anwendungen und übersetzt die relevanten Datei-und Registrierungspfade automatisch an den virtualisierten Speicherort, anstatt an den physikalischen Standort außerhalb der APP-v-Computerumgebung.</span><span class="sxs-lookup"><span data-stu-id="d3844-111">UE-V monitors App-V applications and automatically translates the relevant file and registry paths to the virtualized location as opposed to the physical location outside the App-V computing environment.</span></span>

 **<span data-ttu-id="d3844-112">So implementieren Sie die Synchronisierung von Einstellungen für eine virtualisierte Anwendung</span><span class="sxs-lookup"><span data-stu-id="d3844-112">To implement settings synchronization for a virtualized application</span></span>**

1.  <span data-ttu-id="d3844-113">Führen Sie den UE-V-Generator aus, um die Einstellungen der lokal installierten Anwendung zu erfassen, deren Einstellungen Sie zwischen Computern synchronisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d3844-113">Run the UE-V Generator to collect the settings of the locally installed application whose settings you want to synchronize between computers.</span></span> <span data-ttu-id="d3844-114">Durch diesen Vorgang wird eine Vorlage für Einstellungs Speicherort erstellt.</span><span class="sxs-lookup"><span data-stu-id="d3844-114">This process creates a settings location template.</span></span> <span data-ttu-id="d3844-115">Wenn Sie eine integrierte Vorlage wie die Vorlage Microsoft Office 2010 verwenden, überspringen Sie diesen Schritt.</span><span class="sxs-lookup"><span data-stu-id="d3844-115">If you use a built-in template such as the Microsoft Office 2010 template, skip this step.</span></span> <span data-ttu-id="d3844-116">Weitere Informationen zum Ausführen des UE-v-Generators finden Sie unter [Bereitstellen von UE-v 2. x für benutzerdefinierte Anwendungen](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#createcustomtemplates).</span><span class="sxs-lookup"><span data-stu-id="d3844-116">For more information about running the UE-V Generator, see [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#createcustomtemplates).</span></span>

2.  <span data-ttu-id="d3844-117">Installieren Sie das App-V-Anwendungspaket, wenn dies noch nicht geschehen ist.</span><span class="sxs-lookup"><span data-stu-id="d3844-117">Install the App-V application package if you have not already done so.</span></span>

3.  <span data-ttu-id="d3844-118">Veröffentlichen Sie die Vorlage am Speicherort des Vorlagen Katalogs für Einstellungen, oder installieren Sie die Vorlage manuell mithilfe des `Register-UEVTemplate` Windows PowerShell-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="d3844-118">Publish the template to the location of your settings template catalog or manually install the template by using the `Register-UEVTemplate` Windows PowerShell cmdlet.</span></span>

    <span data-ttu-id="d3844-119">**Hinweis**  Wenn Sie die neu erstellte Vorlage im Vorlagenkatalog für Einstellungen veröffentlichen, erhält der Client die Vorlage erst, nachdem der Synchronisierungsanbieter die Einstellungen aktualisiert hat.</span><span class="sxs-lookup"><span data-stu-id="d3844-119">**Note** If you publish the newly created template to the settings template catalog, the client does not receive the template until the sync provider updates the settings.</span></span> <span data-ttu-id="d3844-120">Wenn Sie diesen Vorgang manuell starten möchten, öffnen Sie den **Aufgabenplaner**, erweitern Sie **Aufgabenplanungsbibliothek**, erweitern Sie **Microsoft**, und erweitern Sie **UE-V**.</span><span class="sxs-lookup"><span data-stu-id="d3844-120">To manually start this process, open **Task Scheduler**, expand **Task Scheduler Library**, expand **Microsoft**, and expand **UE-V**.</span></span> <span data-ttu-id="d3844-121">Klicken Sie im Ergebnisbereich mit der rechten Maustaste auf **Vorlage Auto Update**, und klicken Sie dann auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="d3844-121">In the results pane, right-click **Template Auto Update**, and then click **Run**.</span></span>

     

4.  <span data-ttu-id="d3844-122">Starten Sie das App-V-Paket.</span><span class="sxs-lookup"><span data-stu-id="d3844-122">Start the App-V package.</span></span>






## <span data-ttu-id="d3844-123">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d3844-123">Related topics</span></span>


[<span data-ttu-id="d3844-124">Verwalten von UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="d3844-124">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

 

 





