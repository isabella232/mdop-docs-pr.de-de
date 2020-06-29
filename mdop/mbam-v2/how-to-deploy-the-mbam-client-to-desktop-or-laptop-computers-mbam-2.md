---
title: So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit
description: So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit
author: dansimp
ms.assetid: 56744922-bfdd-48f6-ae01-645ff53b64a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 49340ae970dafc9d263f5564e7981a402da40f19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804655"
---
# <span data-ttu-id="c05e6-103">So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit</span><span class="sxs-lookup"><span data-stu-id="c05e6-103">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="c05e6-104">Der Client für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) ermöglicht Administratoren das erzwingen und Überwachen der BitLocker-Laufwerkverschlüsselung auf Computern im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="c05e6-104">The Microsoft BitLocker Administration and Monitoring (MBAM) client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="c05e6-105">Der BitLocker-Client kann in eine Organisation integriert werden, indem der Client über ein elektronisches Softwareverteilungssystem wie Active Directory-Domänendienste oder MicrosoftSystemCenterConfigurationManager bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c05e6-105">The BitLocker client can be integrated into an organization by deploying the client through an electronic software distribution system, such as Active Directory Domain Services or MicrosoftSystemCenterConfigurationManager.</span></span>

<span data-ttu-id="c05e6-106">**Hinweis**  Informationen zum Überprüfen der Systemanforderungen für die Microsoft BitLocker-Verwaltung und-Überwachung finden Sie unter [unterstützte MBAM 2,0-Konfigurationen](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="c05e6-106">**Note** To review the Microsoft BitLocker Administration and Monitoring Client system requirements, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>

 

**<span data-ttu-id="c05e6-107">So stellen Sie den MBAM-Client auf Desktop-oder Laptopcomputern bereit</span><span class="sxs-lookup"><span data-stu-id="c05e6-107">To deploy the MBAM Client to desktop or laptop computers</span></span>**

1.  <span data-ttu-id="c05e6-108">Suchen Sie die MBAM-Clientinstallationsdateien, die mit der MBAM-Software bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c05e6-108">Locate the MBAM client installation files that are provided with the MBAM software.</span></span>

2.  <span data-ttu-id="c05e6-109">Verwenden Sie Active Directory-Domänendienste oder ein Enterprise-Softwarebereitstellungstool wie MicrosoftSystemCenterConfigurationManager, um das Windows Installer-Paket auf Zielcomputern bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c05e6-109">Use Active Directory Domain Services or an enterprise software deployment tool like MicrosoftSystemCenterConfigurationManager to deploy the Windows Installer package to target computers.</span></span>

3.  <span data-ttu-id="c05e6-110">Konfigurieren Sie die Verteilungseinstellungen oder Gruppenrichtlinien so, dass die MBAM-Client Installationsdatei ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c05e6-110">Configure the distribution settings or Group Policy to run the MBAM Client installation file.</span></span> <span data-ttu-id="c05e6-111">Nach der erfolgreichen Installation wendet der MBAM-Client die Gruppenrichtlinieneinstellungen an, die von einem Domänencontroller empfangen werden, um BitLocker-Verschlüsselungs-und-Verwaltungsfunktionen zu starten.</span><span class="sxs-lookup"><span data-stu-id="c05e6-111">After successful installation, the MBAM Client applies the Group Policy settings that are received from a domain controller to begin BitLocker encryption and management functions.</span></span> <span data-ttu-id="c05e6-112">Weitere Informationen zu den MBAM-Gruppenrichtlinieneinstellungen finden Sie unter [Planen von MBAM 2,0-Gruppenrichtlinienanforderungen](planning-for-mbam-20-group-policy-requirements-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="c05e6-112">For more information about MBAM group policy settings, see [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md).</span></span>

    <span data-ttu-id="c05e6-113">**Wichtig**  Der MBAM-Client startet keine BitLocker-Verschlüsselungs Aktionen, wenn eine Remotedesktopprotokoll-Verbindung aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="c05e6-113">**Important** The MBAM Client will not start BitLocker encryption actions if a remote desktop protocol connection is active.</span></span> <span data-ttu-id="c05e6-114">Alle Remotekonsolen Verbindungen müssen geschlossen werden, bevor die BitLocker-Verschlüsselung beginnt.</span><span class="sxs-lookup"><span data-stu-id="c05e6-114">All remote console connections must be closed before BitLocker encryption will begin.</span></span>

     

## <span data-ttu-id="c05e6-115">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c05e6-115">Related topics</span></span>


[<span data-ttu-id="c05e6-116">Bereitstellen des MBAM 2.0-Clients</span><span class="sxs-lookup"><span data-stu-id="c05e6-116">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)

 

 





