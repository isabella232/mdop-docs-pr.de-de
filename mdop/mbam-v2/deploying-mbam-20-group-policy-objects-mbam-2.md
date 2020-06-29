---
title: Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.0
description: Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.0
author: dansimp
ms.assetid: f17f3897-73ab-431b-a6ec-5a6cff9f279a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1ce2c2a37631d9d678d6de7c1d66b7fdafb2ade9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809988"
---
# <span data-ttu-id="7a98e-103">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="7a98e-103">Deploying MBAM 2.0 Group Policy Objects</span></span>


<span data-ttu-id="7a98e-104">Zur erfolgreichen Bereitstellung von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) müssen Sie zunächst die Gruppenrichtlinien ermitteln, die Sie bei der Implementierung der Microsoft BitLocker-Verwaltung und-Überwachung verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="7a98e-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you first have to determine the Group Policies that you will use in your implementation of Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="7a98e-105">Weitere Informationen zu den verschiedenen verfügbaren Richtlinien finden Sie unter [Planen von MBAM 2,0-Gruppenrichtlinienanforderungen](planning-for-mbam-20-group-policy-requirements-mbam-2.md) .</span><span class="sxs-lookup"><span data-stu-id="7a98e-105">See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for more information on the different policies that are available.</span></span> <span data-ttu-id="7a98e-106">Nachdem Sie die Richtlinien festgelegt haben, die Sie verwenden möchten, müssen Sie ein oder mehrere Gruppenrichtlinienobjekte (Group Policy Objects, GPO) erstellen und bereitstellen, die die Richtlinieneinstellungen für MBAM enthalten, indem Sie die MBAM 2,0-Gruppenrichtlinienvorlage verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a98e-106">When you have determined the policies that you are going to use, you then must create and deploy one or more Group Policy Objects (GPO) that include the policy settings for MBAM by using the MBAM 2.0 Group Policy template.</span></span>

## <span data-ttu-id="7a98e-107">Installieren der MBAM 2,0-Gruppenrichtlinienvorlage</span><span class="sxs-lookup"><span data-stu-id="7a98e-107">Install the MBAM 2.0 Group Policy Template</span></span>


<span data-ttu-id="7a98e-108">Zusätzlich zu den serverbezogenen Microsoft BitLocker-Verwaltungs-und-Überwachungsfeatures umfasst die Server Setupanwendung eine MBAM-Gruppenrichtlinienvorlage.</span><span class="sxs-lookup"><span data-stu-id="7a98e-108">In addition to the server-related Microsoft BitLocker Administration and Monitoring features, the server setup application includes a MBAM Group Policy template.</span></span> <span data-ttu-id="7a98e-109">Diese Vorlage kann auf jedem Computer installiert werden, in dem die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7a98e-109">This template can be installed on any computer able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

[<span data-ttu-id="7a98e-110">So installieren Sie die Gruppenrichtlinienvorlage für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="7a98e-110">How to Install the MBAM 2.0 Group Policy Template</span></span>](how-to-install-the-mbam-20-group-policy-template-mbam-2.md)

## <span data-ttu-id="7a98e-111">Bereitstellen von MBAM 2,0-Gruppenrichtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="7a98e-111">Deploy MBAM 2.0 Group Policy Settings</span></span>


<span data-ttu-id="7a98e-112">Nachdem Sie die erforderlichen GPOs erstellt haben, müssen Sie die MBAM-Gruppenrichtlinieneinstellungen auf den Clientcomputern Ihrer Organisation bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7a98e-112">After you create the necessary GPOs, you must deploy the MBAM Group Policy settings to your organization’s client computers.</span></span>

[<span data-ttu-id="7a98e-113">So bearbeiten Sie GPO-Einstellungen für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="7a98e-113">How to Edit MBAM 2.0 GPO Settings</span></span>](how-to-edit-mbam-20-gpo-settings-mbam-2.md)

## <span data-ttu-id="7a98e-114">Anzeigen der MBAM-Systemsteuerung in Windows</span><span class="sxs-lookup"><span data-stu-id="7a98e-114">Display the MBAM Control Panel in Windows</span></span>


<span data-ttu-id="7a98e-115">Da MBAM ein angepasstes MBAM-Control Panel bietet, das die standardmäßige Windows BitLocker-Systemsteuerung ersetzen kann, können Sie auch die standardmäßige BitLocker-Systemsteuerung von Endbenutzern mithilfe von Gruppenrichtlinien ausblenden.</span><span class="sxs-lookup"><span data-stu-id="7a98e-115">Because MBAM offers a customized MBAM control panel that can replace the default Windows BitLocker control panel, you can also choose to hide the default BitLocker Control Panel from end users by using Group Policy.</span></span>

[<span data-ttu-id="7a98e-116">So blenden Sie die standardmäßige BitLocker-Verschlüsselung in der Windows-Systemsteuerung aus</span><span class="sxs-lookup"><span data-stu-id="7a98e-116">How to Hide Default BitLocker Encryption in the Windows Control Panel</span></span>](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md)

## <span data-ttu-id="7a98e-117">Weitere Ressourcen für die Bereitstellung von MBAM 2,0-Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="7a98e-117">Other Resources for Deploying MBAM 2.0 Group Policy Objects</span></span>


[<span data-ttu-id="7a98e-118">Bereitstellen von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="7a98e-118">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)

 

 





