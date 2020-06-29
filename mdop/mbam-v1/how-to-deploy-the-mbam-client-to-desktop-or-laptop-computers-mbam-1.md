---
title: So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit
description: So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit
author: dansimp
ms.assetid: f32927a2-4c05-4da8-acca-1108d1dfdb7e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce4f8597cc182c037983a89efd60c5ef935712ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811218"
---
# <span data-ttu-id="552dc-103">So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit</span><span class="sxs-lookup"><span data-stu-id="552dc-103">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="552dc-104">Der Client für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) ermöglicht Administratoren das erzwingen und Überwachen der BitLocker-Laufwerkverschlüsselung auf Computern im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="552dc-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="552dc-105">Der MBAM-Client kann in eine Organisation integriert werden, indem der Client mithilfe von Tools wie Active Directory-Domänendiensten oder einem Enterprise-Softwarebereitstellungstool wie MicrosoftSystemCenter2012 ConfigurationManager bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="552dc-105">The MBAM Client can be integrated into an organization by deploying the client through tools, such as Active Directory Domain Services or an enterprise software deployment tool such as MicrosoftSystemCenter2012 ConfigurationManager.</span></span>

<span data-ttu-id="552dc-106">**Hinweis**  Informationen zum Überprüfen der MBAM-Client Systemanforderungen finden Sie unter [unterstützte MBAM 1,0-Konfigurationen](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="552dc-106">**Note** To review the MBAM Client system requirements, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

**<span data-ttu-id="552dc-107">So stellen Sie den MBAM-Client auf Desktop-oder Laptopcomputern bereit</span><span class="sxs-lookup"><span data-stu-id="552dc-107">To deploy the MBAM Client to desktop or laptop computers</span></span>**

1.  <span data-ttu-id="552dc-108">Suchen Sie die MBAM-Client Installationsdateien, die mit der MBAM-Software bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="552dc-108">Locate the MBAM Client installation files that are provided with the MBAM software.</span></span>

2.  <span data-ttu-id="552dc-109">Bereitstellen des Windows Installer-Pakets auf Zielcomputern mithilfe von Active Directory-Domänendiensten oder eines Enterprise-Softwarebereitstellungstools wie MicrosoftSystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="552dc-109">Deploy the Windows Installer package to target computers by using Active Directory Domain Services or an enterprise software deployment tool, such as MicrosoftSystemCenter2012 ConfigurationManager.</span></span>

    <span data-ttu-id="552dc-110">**Hinweis**  Verwenden Sie Gruppenrichtlinien nicht zum Bereitstellen des Windows Installer-Pakets.</span><span class="sxs-lookup"><span data-stu-id="552dc-110">**Note** You should not use Group Policy to deploy the Windows Installer package.</span></span>

     

3.  <span data-ttu-id="552dc-111">Konfigurieren Sie die Verteilungseinstellungen oder Gruppenrichtlinien so, dass die MBAM-Client Installationsdatei ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="552dc-111">Configure the distribution settings or Group Policy to run the MBAM Client installation file.</span></span> <span data-ttu-id="552dc-112">Nach der erfolgreichen Installation wendet der MBAM-Client die Gruppenrichtlinieneinstellungen an, die von einem Domänencontroller empfangen werden, um BitLocker-Verschlüsselungs-und-Verwaltungsfunktionen zu starten.</span><span class="sxs-lookup"><span data-stu-id="552dc-112">After successful installation, the MBAM Client applies the Group Policy settings that are received from a domain controller to begin BitLocker encryption and management functions.</span></span> <span data-ttu-id="552dc-113">Weitere Informationen zu den MBAM-Gruppenrichtlinieneinstellungen finden Sie unter [Planen von MBAM 1,0-Gruppenrichtlinienanforderungen](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="552dc-113">For more information about MBAM Group Policy settings, see [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span>

    <span data-ttu-id="552dc-114">**Wichtig**  Der MBAM-Client startet keine BitLocker-Verschlüsselungs Aktionen, wenn eine Remotedesktopprotokoll-Verbindung aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="552dc-114">**Important** The MBAM Client will not start BitLocker encryption actions if a remote desktop protocol connection is active.</span></span> <span data-ttu-id="552dc-115">Alle Remotekonsolen Verbindungen müssen geschlossen werden, bevor die BitLocker-Verschlüsselung beginnt.</span><span class="sxs-lookup"><span data-stu-id="552dc-115">All remote console connections must be closed before BitLocker encryption will begin.</span></span>

     

## <span data-ttu-id="552dc-116">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="552dc-116">Related topics</span></span>


[<span data-ttu-id="552dc-117">Bereitstellen des MBAM 1.0-Clients</span><span class="sxs-lookup"><span data-stu-id="552dc-117">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)

 

 





