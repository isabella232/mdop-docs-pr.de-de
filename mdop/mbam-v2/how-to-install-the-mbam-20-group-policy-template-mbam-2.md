---
title: So installieren Sie die Gruppenrichtlinienvorlage für MBAM 2.0
description: So installieren Sie die Gruppenrichtlinienvorlage für MBAM 2.0
author: dansimp
ms.assetid: bc193232-d060-4285-842e-d194a74dd3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6420fc4d499de05ed740b038b40aff6a9cd8a05f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811644"
---
# <span data-ttu-id="315f6-103">So installieren Sie die Gruppenrichtlinienvorlage für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="315f6-103">How to Install the MBAM 2.0 Group Policy Template</span></span>


<span data-ttu-id="315f6-104">Zusätzlich zu den serverbezogenen Features für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) umfasst die Server Setupanwendung eine Microsoft BitLocker-Verwaltungs-und-Überwachungsgruppen Richtlinienvorlage.</span><span class="sxs-lookup"><span data-stu-id="315f6-104">In addition to the server-related Microsoft BitLocker Administration and Monitoring (MBAM) features, the server setup application includes an Microsoft BitLocker Administration and Monitoring Group Policy template.</span></span> <span data-ttu-id="315f6-105">Diese Vorlage kann auf jedem Computer installiert werden, der die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ausführt.</span><span class="sxs-lookup"><span data-stu-id="315f6-105">This template can be installed on any computer capable of running the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="315f6-106">In den folgenden Schritten wird beschrieben, wie die MBAM-Gruppenrichtlinienvorlage installiert wird.</span><span class="sxs-lookup"><span data-stu-id="315f6-106">The following steps describe how to install the MBAM Group Policy template.</span></span>

<span data-ttu-id="315f6-107">**Hinweis**  Stellen Sie sicher, dass Sie das 32-Bit-Setup auf 32-Bit-Servern und das 64-Bit-Setup auf 64-Bit-Servern verwenden.</span><span class="sxs-lookup"><span data-stu-id="315f6-107">**Note** Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>

 

**<span data-ttu-id="315f6-108">So installieren Sie die MBAM-Gruppenrichtlinienvorlage</span><span class="sxs-lookup"><span data-stu-id="315f6-108">To install the MBAM Group Policy template</span></span>**

1.  <span data-ttu-id="315f6-109">Führen Sie auf dem Server, auf dem Sie MBAM installieren möchten, **MBAMSetup.exe** aus, um den MBAM-Installations-Assistenten zu starten.</span><span class="sxs-lookup"><span data-stu-id="315f6-109">On the server where you want to install MBAM, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="315f6-110">Wählen Sie auf der **Willkommens** Seite optional das **Programm zur Verbesserung der Benutzerfreundlichkeit**aus, und klicken Sie dann auf **Start**.</span><span class="sxs-lookup"><span data-stu-id="315f6-110">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="315f6-111">Lesen und akzeptieren Sie die Microsoft-Software-Lizenzbestimmungen, und klicken Sie auf **weiter** , um die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="315f6-111">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="315f6-112">Standardmäßig sind alle Microsoft BitLocker-Verwaltungs-und Überwachungsfeatures für die Installation ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="315f6-112">By default, all Microsoft BitLocker Administration and Monitoring features are selected for installation.</span></span> <span data-ttu-id="315f6-113">Deaktivieren Sie alle Feature-Optionen mit Ausnahme der **Richtlinienvorlage**, und klicken Sie auf **weiter** , um die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="315f6-113">Clear all feature options except for **Policy Template**, and then click **Next** to continue the installation.</span></span>

    <span data-ttu-id="315f6-114">**Hinweis**  Der Installations-Assistent überprüft die Voraussetzungen für die Installation und zeigt die fehlenden Voraussetzungen an.</span><span class="sxs-lookup"><span data-stu-id="315f6-114">**Note** The installation wizard checks the prerequisites for your installation and displays prerequisites that are missing.</span></span> <span data-ttu-id="315f6-115">Wenn alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="315f6-115">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="315f6-116">Wenn eine fehlende Voraussetzung erkannt wird, müssen Sie die fehlenden Voraussetzungen beheben und dann **erneut auf Voraussetzungen prüfen**klicken.</span><span class="sxs-lookup"><span data-stu-id="315f6-116">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="315f6-117">Sobald alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="315f6-117">Once all prerequisites are met, the installation will resume.</span></span>

     

5.  <span data-ttu-id="315f6-118">Detaillierte Informationen dazu, wie und wo Sie die Vorlagen installieren, finden Sie unter [herunterladen und Bereitstellen von MDOP-Gruppenrichtlinien-Vorlagen (ADMX)](https://technet.microsoft.com/library/dn659707.aspx).</span><span class="sxs-lookup"><span data-stu-id="315f6-118">For specific steps about how and where to install the templates, see [How to Download and Deploy MDOP Group Policy (.admx) Templates](https://technet.microsoft.com/library/dn659707.aspx).</span></span>

6.  <span data-ttu-id="315f6-119">Klicken Sie nach dem Setup-Assistenten für Microsoft BitLocker-Verwaltung und-Überwachung auf Installationsseiten für die ausgewählten Features, und klicken Sie auf **Fertig stellen** , um das MBAM-Setup zu schließen</span><span class="sxs-lookup"><span data-stu-id="315f6-119">After the Microsoft BitLocker Administration and Monitoring Setup wizard displays installation pages for the selected features, click **Finish** to close MBAM Setup.</span></span>

## <span data-ttu-id="315f6-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="315f6-120">Related topics</span></span>


[<span data-ttu-id="315f6-121">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="315f6-121">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 





