---
title: Bereitstellen von Gruppenrichtlinienobjekten für MBAM 1.0
description: Bereitstellen von Gruppenrichtlinienobjekten für MBAM 1.0
author: dansimp
ms.assetid: 2129291e-d2b2-41ed-b643-1e311c49fee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d14123f1d5b197146e425cba063e8ce4c180641
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808623"
---
# <span data-ttu-id="8c213-103">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="8c213-103">Deploying MBAM 1.0 Group Policy Objects</span></span>


<span data-ttu-id="8c213-104">Wenn Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) erfolgreich bereitstellen möchten, müssen Sie zuerst die Gruppenrichtlinien ermitteln, die Sie bei der Implementierung von MBAM verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="8c213-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you must first determine the Group Policies that you will use in your implementation of MBAM.</span></span> <span data-ttu-id="8c213-105">Weitere Informationen zu den verschiedenen verfügbaren Richtlinien finden Sie unter [Planen von MBAM 1,0-Gruppenrichtlinienanforderungen](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8c213-105">For more information about the various available policies, see [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span> <span data-ttu-id="8c213-106">Wenn Sie die Richtlinien festgelegt haben, die Sie verwenden möchten, müssen Sie die MBAM 1,0-Gruppenrichtlinienvorlage verwenden, um ein oder mehrere Gruppenrichtlinienobjekte zu erstellen und bereitzustellen, die die MBAM-Richtlinieneinstellungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="8c213-106">When you have determined the policies that you are going to use, you must use the MBAM 1.0 Group Policy template to create and deploy one or more Group Policy objects (GPO) that include the MBAM policy settings.</span></span>

## <span data-ttu-id="8c213-107">Installieren der MBAM 1,0-Gruppenrichtlinienvorlage</span><span class="sxs-lookup"><span data-stu-id="8c213-107">Install the MBAM 1.0 Group Policy template</span></span>


<span data-ttu-id="8c213-108">Zusätzlich zum Bereitstellen von serverbezogenen Features von MBAM umfasst die Server Setupanwendung eine MBAM-Gruppenrichtlinienvorlage.</span><span class="sxs-lookup"><span data-stu-id="8c213-108">In addition to providing server-related features of MBAM, the server setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="8c213-109">Sie können diese Vorlage auf jedem Computer installieren, auf dem die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8c213-109">You can install this template on any computer that is able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

[<span data-ttu-id="8c213-110">So installieren Sie die Gruppenrichtlinienvorlage für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="8c213-110">How to Install the MBAM 1.0 Group Policy Template</span></span>](how-to-install-the-mbam-10-group-policy-template.md)

## <span data-ttu-id="8c213-111">Bereitstellen von MBAM 1,0-Gruppenrichtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="8c213-111">Deploy MBAM 1.0 Group Policy settings</span></span>


<span data-ttu-id="8c213-112">Nachdem Sie die erforderlichen GPOs erstellt haben, müssen Sie die MBAM-Gruppenrichtlinieneinstellungen auf den Clientcomputern Ihrer Organisation bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8c213-112">After you create the necessary GPOs, you must deploy the MBAM Group Policy settings to your organization’s client computers.</span></span>

[<span data-ttu-id="8c213-113">So bearbeiten Sie die GPO-Einstellungen für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="8c213-113">How to Edit MBAM 1.0 GPO Settings</span></span>](how-to-edit-mbam-10-gpo-settings.md)

## <span data-ttu-id="8c213-114">Anzeigen der MBAM-Systemsteuerung in Windows</span><span class="sxs-lookup"><span data-stu-id="8c213-114">Display the MBAM Control Panel in Windows</span></span>


<span data-ttu-id="8c213-115">Da MBAM ein angepasstes MBAM-Control Panel bietet, das die standardmäßige Windows BitLocker-Systemsteuerung ersetzen kann, können Sie auch die standardmäßige BitLocker-Systemsteuerung von Endbenutzern mithilfe von Gruppenrichtlinien ausblenden.</span><span class="sxs-lookup"><span data-stu-id="8c213-115">Because MBAM offers a customized MBAM control panel that can replace the default Windows BitLocker control panel, you can also choose to hide the default BitLocker Control Panel from end users by using Group Policy.</span></span>

[<span data-ttu-id="8c213-116">So blenden Sie die standardmäßige BitLocker-Verschlüsselung in der Windows-Systemsteuerung aus</span><span class="sxs-lookup"><span data-stu-id="8c213-116">How to Hide Default BitLocker Encryption in The Windows Control Panel</span></span>](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md)

## <span data-ttu-id="8c213-117">Weitere Ressourcen für die Bereitstellung von MBAM 1,0-Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="8c213-117">Other resources for deploying MBAM 1.0 Group Policy Objects</span></span>


[<span data-ttu-id="8c213-118">Bereitstellen von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="8c213-118">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

 

 





