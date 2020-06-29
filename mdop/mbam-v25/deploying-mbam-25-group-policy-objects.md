---
title: Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.5
description: Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.5
author: dansimp
ms.assetid: 4b835054-6846-463d-af58-8ac4639a1188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9624b94e9d4808a35e1199290f4cd90a8122f767
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810525"
---
# <span data-ttu-id="711d4-103">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="711d4-103">Deploying MBAM 2.5 Group Policy Objects</span></span>


<span data-ttu-id="711d4-104">Zum Bereitstellen von MBAM müssen Sie Gruppenrichtlinieneinstellungen festlegen, die MBAM-Implementierungs Einstellungen für die BitLocker-Laufwerkverschlüsselung definieren.</span><span class="sxs-lookup"><span data-stu-id="711d4-104">To deploy MBAM, you have to set Group Policy settings that define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="711d4-105">Zum Ausführen dieser Aufgabe müssen Sie die MBAM-Gruppenrichtlinienvorlagen auf einen Server oder eine Workstation kopieren, die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ausführen können, und dann die Einstellungen bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="711d4-105">To complete this task, you must copy the MBAM Group Policy Templates to a server or workstation that are capable of running Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM), and then edit the settings.</span></span>

<span data-ttu-id="711d4-106">**Wichtig**  Ändern Sie die Gruppenrichtlinieneinstellungen im **BitLocker Drive Encryption** -Knoten nicht, oder MBAM wird nicht ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="711d4-106">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node, or MBAM will not work correctly.</span></span> <span data-ttu-id="711d4-107">Wenn Sie die Gruppenrichtlinieneinstellungen im MDOP- **MBAM (BitLocker-Verwaltungsknoten)** konfigurieren, konfiguriert MBAM automatisch die **BitLocker-Laufwerk Verschlüsselungs** Einstellungen für Sie.</span><span class="sxs-lookup"><span data-stu-id="711d4-107">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the **BitLocker Drive Encryption** settings for you.</span></span>

 

## <span data-ttu-id="711d4-108">Kopieren die Gruppenrichtlinienvorlagen für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="711d4-108">Copying the MBAM 2.5 Group Policy Templates</span></span>


<span data-ttu-id="711d4-109">Bevor Sie den MBAM-Client installieren, müssen Sie MBAM-spezifische Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) auf die Verwaltungsarbeitsstation kopieren.</span><span class="sxs-lookup"><span data-stu-id="711d4-109">Before you install the MBAM Client, you must copy MBAM-specific Group Policy Objects (GPOs) to the Management Workstation.</span></span> <span data-ttu-id="711d4-110">Diese GPOs definieren MBAM-Implementierungs Einstellungen für die BitLocker-Laufwerkverschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="711d4-110">These GPOs define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="711d4-111">Sie können die Gruppenrichtlinienvorlagen auf alle Server oder Workstations kopieren, die ein unterstützter Windows-Server oder-Clientcomputer sind und die in der Lage sind, die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="711d4-111">You can copy the Group Policy templates to any server or workstation that is a supported Windows server or client computer and that is able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

[<span data-ttu-id="711d4-112">Kopieren die Gruppenrichtlinienvorlagen für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="711d4-112">Copying the MBAM 2.5 Group Policy Templates</span></span>](copying-the-mbam-25-group-policy-templates.md)

## <span data-ttu-id="711d4-113">Bearbeiten von MBAM 2,0-GPO-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="711d4-113">Editing MBAM 2.0 GPO settings</span></span>


<span data-ttu-id="711d4-114">Nachdem Sie die erforderlichen GPOs erstellt haben, müssen Sie die MBAM-Gruppenrichtlinieneinstellungen auf den Clientcomputern Ihrer Organisation bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="711d4-114">After you create the necessary GPOs, you must deploy the MBAM Group Policy settings to your organization’s client computers.</span></span> <span data-ttu-id="711d4-115">Um GPOs anzuzeigen und zu erstellen, müssen Sie die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder eine erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) installiert haben.</span><span class="sxs-lookup"><span data-stu-id="711d4-115">To view and create GPOs, you must have Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM) installed.</span></span>

[<span data-ttu-id="711d4-116">Bearbeiten der Gruppenrichtlinieneinstellungen für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="711d4-116">Editing the MBAM 2.5 Group Policy Settings</span></span>](editing-the-mbam-25-group-policy-settings.md)

## <span data-ttu-id="711d4-117">Anzeigen oder Ausblenden der MBAM-Systemsteuerung in der Windows-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="711d4-117">Showing or hiding the MBAM Control Panel in Windows Control Panel</span></span>


<span data-ttu-id="711d4-118">Da MBAM ein angepasstes MBAM-Control Panel bietet, das die standardmäßige Windows BitLocker-Systemsteuerung ersetzen kann, können Sie auch die standardmäßige BitLocker-Systemsteuerung von Endbenutzern mithilfe von Gruppenrichtlinieneinstellungen anzeigen oder ausblenden.</span><span class="sxs-lookup"><span data-stu-id="711d4-118">Since MBAM offers a customized MBAM control panel that can replace the default Windows BitLocker control panel, you can also choose to show or hide the default BitLocker Control Panel from end users by using Group Policy settings.</span></span>

[<span data-ttu-id="711d4-119">Ausblenden der Standard-BitLocker-Laufwerkverschlüsselung in der Windows-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="711d4-119">Hiding the Default BitLocker Drive Encryption Item in Control Panel</span></span>](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)

## <span data-ttu-id="711d4-120">Weitere Ressourcen für die Bereitstellung von MBAM 2,0-Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="711d4-120">Other Resources for deploying MBAM 2.0 Group Policy Objects</span></span>


[<span data-ttu-id="711d4-121">Bereitstellen von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="711d4-121">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

## <span data-ttu-id="711d4-122">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="711d4-122">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="711d4-123">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="711d4-123">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="711d4-124">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="711d4-124">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 





