---
title: Anzeigen und Konfigurieren von MED-V-Protokollen
description: Anzeigen und Konfigurieren von MED-V-Protokollen
author: dansimp
ms.assetid: a15537ce-981d-4f55-9c3c-e7fbf94b8fe5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7984cec072827136db9ea52a535c0ea44c6bc2c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810129"
---
# <span data-ttu-id="242cf-103">Anzeigen und Konfigurieren von MED-V-Protokollen</span><span class="sxs-lookup"><span data-stu-id="242cf-103">Viewing and Configuring MED-V Logs</span></span>


<span data-ttu-id="242cf-104">Wenn Sie Probleme und Probleme mit Med-v beheben, finden Sie es möglicherweise hilfreich oder notwendig, auf die Med-v-Ereignisprotokolle zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="242cf-104">When you are troubleshooting MED-V issues and problems, you may find it helpful or necessary to access the MED-V event logs.</span></span> <span data-ttu-id="242cf-105">Mit dem MED-V Administration Toolkit können Sie die Ereignisanzeige für den Hostcomputer und den virtuellen Gastcomputer öffnen.</span><span class="sxs-lookup"><span data-stu-id="242cf-105">You can open Event Viewer for the host computer and the guest virtual machine by using the MED-V Administration Toolkit.</span></span> <span data-ttu-id="242cf-106">Sie können auch das Med-v-Administrations-Toolkit verwenden, um den Protokolliergrad festzulegen, auf dem die Med-v-Ereignisprotokolle Bericht Med-v-Ereignisse protokollieren.</span><span class="sxs-lookup"><span data-stu-id="242cf-106">You can also use the MED-V Administration Toolkit to set the logging level at which the MED-V event logs report MED-V events.</span></span>

<span data-ttu-id="242cf-107">Informationen zum Öffnen des Med-v-Administrations-Toolkits finden Sie unter [Problembehandlung bei Med-v mit dem Administrations-Toolkit](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span><span class="sxs-lookup"><span data-stu-id="242cf-107">For information about how to open the MED-V Administration Toolkit, see [Troubleshooting MED-V by Using the Administration Toolkit](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span></span>

## <span data-ttu-id="242cf-108">Anzeigen von MED-V-Ereignisprotokollen</span><span class="sxs-lookup"><span data-stu-id="242cf-108">Viewing MED-V Event Logs</span></span>


<span data-ttu-id="242cf-109">Klicken Sie im Fenster **MED-V Administration Toolkit** auf **Host Ereignisse** , um die Ereignisanzeige für den Hostcomputer zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="242cf-109">On the **MED-V Administration Toolkit** window, click **Host Events** to open the event viewer for the host computer.</span></span> <span data-ttu-id="242cf-110">Oder klicken Sie auf **gastereignisse** , um die Ereignisanzeige für den virtuellen Gastcomputer zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="242cf-110">Or, click **Guest Events** to open Event Viewer for the guest virtual machine.</span></span>

<span data-ttu-id="242cf-111">Die Ereignisanzeige wird geöffnet und zeigt die entsprechenden Ereignisprotokolle an, mit denen Sie die Probleme behandeln können, die beim Bereitstellen oder Verwalten von MED-V auftreten können.</span><span class="sxs-lookup"><span data-stu-id="242cf-111">Event Viewer opens and displays the corresponding event logs that you can use to troubleshoot the issues that you might encounter when you deploy or manage MED-V.</span></span> <span data-ttu-id="242cf-112">Standardmäßig werden nur Fehler und Warnungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="242cf-112">By default, only errors and warnings are displayed.</span></span> <span data-ttu-id="242cf-113">Weitere Informationen zu bestimmten Ereignis-IDs und Nachrichten finden Sie unter [MED-V-Ereignisprotokollmeldungen](med-v-event-log-messages.md).</span><span class="sxs-lookup"><span data-stu-id="242cf-113">For more information about specific event IDs and messages, see [MED-V Event Log Messages](med-v-event-log-messages.md).</span></span>

<span data-ttu-id="242cf-114">**Hinweis**  Endbenutzer können Ereignisprotokolldateien nur im Gast speichern, wenn Sie über Administratorberechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="242cf-114">**Note** End users can only save event log files in the guest if they have administrative permissions.</span></span>

 

### <span data-ttu-id="242cf-115">So öffnen Sie die Ereignisanzeige auf dem Hostcomputer manuell</span><span class="sxs-lookup"><span data-stu-id="242cf-115">To manually open the Event Viewer in the host computer</span></span>

1.  <span data-ttu-id="242cf-116">Klicken Sie auf **Start**, klicken Sie auf **System**Steuerung, und klicken Sie dann auf **Verwaltungs Tools**.</span><span class="sxs-lookup"><span data-stu-id="242cf-116">Click **Start**, click **Control Panel**, and then click **Administrative Tools**.</span></span>

2.  <span data-ttu-id="242cf-117">Doppelklicken Sie auf **Ereignisanzeige**, und klicken Sie dann auf **Anwendungen und Dienstprotokolle**.</span><span class="sxs-lookup"><span data-stu-id="242cf-117">Double-click **Event Viewer**, and then click **Applications and Services Logs**.</span></span>

3.  <span data-ttu-id="242cf-118">Doppelklicken Sie auf **MEDV**.</span><span class="sxs-lookup"><span data-stu-id="242cf-118">Double-click **MEDV**.</span></span>

## <span data-ttu-id="242cf-119">Konfigurieren von MED-V-Ereignisprotokollen</span><span class="sxs-lookup"><span data-stu-id="242cf-119">Configuring MED-V Event Logs</span></span>


<span data-ttu-id="242cf-120">Sie können die Med-v-Ereignisprotokollierungsstufe angeben, indem Sie das entsprechende Optionsfeld im Med-v-Administrations-Toolkit auswählen.</span><span class="sxs-lookup"><span data-stu-id="242cf-120">You can specify the MED-V event logging level by selecting the corresponding option button on the MED-V Administration Toolkit.</span></span> <span data-ttu-id="242cf-121">Sie können entscheiden, ob die Ereignisprotokollierung nur Fehler, Fehler und Warnungen sowie Fehler, Warnungen und Informationsmeldungen enthält.</span><span class="sxs-lookup"><span data-stu-id="242cf-121">You can decide whether event logging includes errors only, errors and warnings, or errors, warnings and informational messages.</span></span> <span data-ttu-id="242cf-122">Der angegebene ereignisprotokollierungsgrad wird sowohl für den Hostcomputer als auch für den virtuellen Gastcomputer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="242cf-122">The event logging level specified is set for both the host computer and the guest virtual machine.</span></span>

<span data-ttu-id="242cf-123">Sie können auch die Ereignisprotokollierungsstufe angeben, indem Sie den Registrierungswert EventLogLevel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="242cf-123">You can also specify the event logging level by editing the EventLogLevel registry value.</span></span> <span data-ttu-id="242cf-124">Weitere Informationen finden Sie unter [Verwalten von MED-V Workspace-Konfigurationseinstellungen](managing-med-v-workspace-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="242cf-124">For more information, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).</span></span>

<span data-ttu-id="242cf-125">**Hinweis**  Die Ebene, die Sie im Fenster **Med-v-Administrations-Toolkit** angeben, bezieht sich auf die zukünftige Med-v-Ereignisprotokollierung.</span><span class="sxs-lookup"><span data-stu-id="242cf-125">**Note** The level you specify on the **MED-V Administration Toolkit** window applies to future MED-V event logging.</span></span> <span data-ttu-id="242cf-126">Wenn Sie die Ebene so festzulegen, dass alle Fehler, Warnungen und Informationsmeldungen erfasst werden, werden die Ereignisprotokolle schneller gefüllt, und ältere Ereignisse werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="242cf-126">If you set the level to capture all errors, warnings, and informational messages, then the event logs fill more quickly and older events are removed.</span></span>

 

## <span data-ttu-id="242cf-127">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="242cf-127">Related topics</span></span>


[<span data-ttu-id="242cf-128">Neu starten und das Zurücksetzen eines MED-V-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="242cf-128">Restarting and Resetting a MED-V Workspace</span></span>](restarting-and-resetting-a-med-v-workspace.md)

[<span data-ttu-id="242cf-129">Anzeigen von MED-V-Arbeitsbereichskonfigurationen</span><span class="sxs-lookup"><span data-stu-id="242cf-129">Viewing MED-V Workspace Configurations</span></span>](viewing-med-v-workspace-configurations.md)

 

 





