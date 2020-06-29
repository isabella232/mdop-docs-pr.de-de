---
title: So installieren Sie die Gruppenrichtlinienvorlage für MBAM 1.0
description: So installieren Sie die Gruppenrichtlinienvorlage für MBAM 1.0
author: dansimp
ms.assetid: 451a50b0-939c-47ad-9248-a138deade550
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a055c84fb6b1645592b53d957daf157a6055880
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811095"
---
# <span data-ttu-id="4cf2c-103">So installieren Sie die Gruppenrichtlinienvorlage für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="4cf2c-103">How to Install the MBAM 1.0 Group Policy Template</span></span>


<span data-ttu-id="4cf2c-104">Zusätzlich zu den serverbezogenen Features der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) enthält die Server Setupanwendung eine MBAM-Gruppenrichtlinienvorlage.</span><span class="sxs-lookup"><span data-stu-id="4cf2c-104">In addition to the server-related features of Microsoft BitLocker Administration and Monitoring (MBAM), the server setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="4cf2c-105">Sie können diese Vorlage auf jedem Computer installieren, auf dem die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="4cf2c-105">You can install this template on any computer that is capable of running the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="4cf2c-106">In den folgenden Schritten wird beschrieben, wie die MBAM-Gruppenrichtlinienvorlage installiert wird.</span><span class="sxs-lookup"><span data-stu-id="4cf2c-106">The following steps describe how to install the MBAM Group Policy template.</span></span>

<span data-ttu-id="4cf2c-107">**Hinweis**  Stellen Sie sicher, dass Sie das 32-Bit-Setup auf 32-Bit-Servern und das 64-Bit-Setup auf 64-Bit-Servern verwenden.</span><span class="sxs-lookup"><span data-stu-id="4cf2c-107">**Note** Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>

 

**<span data-ttu-id="4cf2c-108">So installieren Sie die MBAM-Gruppenrichtlinienvorlage</span><span class="sxs-lookup"><span data-stu-id="4cf2c-108">To install the MBAM Group Policy template</span></span>**

1.  <span data-ttu-id="4cf2c-109">Starten Sie den MBAM-Installations-Assistenten. Klicken Sie dann auf der Seite Willkommen auf **Installieren** .</span><span class="sxs-lookup"><span data-stu-id="4cf2c-109">Start the MBAM installation wizard; then, click **Install** on the Welcome page.</span></span>

2.  <span data-ttu-id="4cf2c-110">Lesen und akzeptieren Sie die Microsoft-Software-Lizenzbestimmungen, und klicken Sie auf **weiter** , um die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="4cf2c-110">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

3.  <span data-ttu-id="4cf2c-111">Standardmäßig sind alle MBAM-Features für die Installation ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="4cf2c-111">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="4cf2c-112">Deaktivieren Sie alle Feature-Optionen mit Ausnahme der **Richtlinienvorlage**, und klicken Sie auf **weiter** , um die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="4cf2c-112">Clear all feature options except for **Policy Template**, and then click **Next** to continue the installation.</span></span>

    <span data-ttu-id="4cf2c-113">**Hinweis**  Der Installations-Assistent überprüft die Voraussetzungen für die Installation und zeigt die fehlenden Voraussetzungen an.</span><span class="sxs-lookup"><span data-stu-id="4cf2c-113">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="4cf2c-114">Wenn alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="4cf2c-114">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="4cf2c-115">Wenn eine fehlende Voraussetzung erkannt wird, müssen Sie die fehlende Voraussetzungen beheben und dann **erneut auf Voraussetzungen prüfen**klicken.</span><span class="sxs-lookup"><span data-stu-id="4cf2c-115">If a missing prerequisite is detected, you must resolve the missing prerequisite and then click **Check prerequisites again**.</span></span> <span data-ttu-id="4cf2c-116">Sobald alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="4cf2c-116">Once all prerequisites are met, the installation will resume.</span></span>

     

4.  <span data-ttu-id="4cf2c-117">Nachdem der MBAM-Setup-Assistent Installationsseiten für die ausgewählten Features angezeigt hat, klicken Sie auf **Fertig stellen** , um das MBAM-Setup zu schließen.</span><span class="sxs-lookup"><span data-stu-id="4cf2c-117">After the MBAM Setup wizard displays installation pages for the selected features, click **Finish** to close MBAM Setup.</span></span>

## <span data-ttu-id="4cf2c-118">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="4cf2c-118">Related topics</span></span>


[<span data-ttu-id="4cf2c-119">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="4cf2c-119">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)

 

 





