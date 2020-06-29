---
title: So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit
description: So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit
author: dansimp
ms.assetid: 3a7639e0-468e-4496-8be2-ed29b8e07c53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b67533a555da4dabec6654ed3f95f91ad8d37bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810579"
---
# <span data-ttu-id="b5cc4-103">So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit</span><span class="sxs-lookup"><span data-stu-id="b5cc4-103">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="b5cc4-104">In diesem Thema wird erläutert, wie der MBAM-Client auf Computern der Endbenutzer bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b5cc4-104">This topic explains how to deploy the MBAM Client to end users’ computers.</span></span> <span data-ttu-id="b5cc4-105">Sie können den MBAM-Client über ein elektronisches Softwareverteilungssystem wie Active Directory-Domänendienste oder MicrosoftSystemCenterConfiguration-Manager bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b5cc4-105">You can deploy the MBAM Client through an electronic software distribution system, such as Active Directory Domain Services or MicrosoftSystemCenterConfiguration Manager.</span></span>

<span data-ttu-id="b5cc4-106">Informationen zum Bereitstellen des MBAM-Clients als Teil einer Windows-Bereitstellung finden Sie unter [Aktivieren von BitLocker mithilfe von MBAM als Teil einer Windows-Bereitstellung](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="b5cc4-106">To deploy the MBAM Client as part of a Windows deployment, see [How to Enable BitLocker by Using MBAM as Part of a Windows Deployment](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md).</span></span>

<span data-ttu-id="b5cc4-107">Bevor Sie die MBAM-Client Bereitstellung starten, überprüfen Sie die [MBAM 2,5-unterstützten Konfigurationen](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="b5cc4-107">Before you start the MBAM Client deployment, review the [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

**<span data-ttu-id="b5cc4-108">So stellen Sie den MBAM-Client auf Desktop-oder Laptopcomputern bereit</span><span class="sxs-lookup"><span data-stu-id="b5cc4-108">To deploy the MBAM Client to desktop or laptop computers</span></span>**

1.  <span data-ttu-id="b5cc4-109">Suchen Sie die MBAM-Client Installationsdateien, die mit der MBAM-Software bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b5cc4-109">Locate the MBAM Client installation files that are provided with the MBAM software.</span></span>

2.  <span data-ttu-id="b5cc4-110">Verwenden Sie Active Directory-Domänendienste oder ein Enterprise-Softwarebereitstellungstool wie MicrosoftSystemCenterConfiguration-Manager, um das Windows Installer-Paket auf Zielcomputern bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b5cc4-110">Use Active Directory Domain Services or an enterprise software deployment tool like MicrosoftSystemCenterConfiguration Manager to deploy the Windows Installer package to target computers.</span></span>

3.  <span data-ttu-id="b5cc4-111">Konfigurieren Sie die Verteilungseinstellungen oder Gruppenrichtlinieneinstellungen, um die MBAM-Client Installationsdatei auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b5cc4-111">Configure the distribution settings or Group Policy settings to run the MBAM Client installation file.</span></span>

    <span data-ttu-id="b5cc4-112">Nach der erfolgreichen Installation wendet der MBAM-Client die Gruppenrichtlinieneinstellungen an, die von einem Domänencontroller empfangen werden, um die BitLocker-Laufwerkverschlüsselung und-Verwaltungsfunktionen zu starten.</span><span class="sxs-lookup"><span data-stu-id="b5cc4-112">After successful installation, the MBAM Client applies the Group Policy settings that are received from a domain controller to begin BitLocker Drive Encryption and management functions.</span></span>

    <span data-ttu-id="b5cc4-113">**Wichtig**  Der MBAM-Client startet keine BitLocker-Laufwerk Verschlüsselungs Aktionen, wenn eine Remotedesktopprotokoll-Verbindung aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="b5cc4-113">**Important** The MBAM Client does not start BitLocker Drive Encryption actions if a remote desktop protocol connection is active.</span></span> <span data-ttu-id="b5cc4-114">Alle Remotekonsolen Verbindungen müssen geschlossen sein, und ein Benutzer muss an einer physikalischen Konsolensitzung angemeldet sein, bevor die BitLocker-Laufwerkverschlüsselung beginnt.</span><span class="sxs-lookup"><span data-stu-id="b5cc4-114">All remote console connections must be closed and a user must be logged on to a physical console session before BitLocker Drive Encryption begins.</span></span>

     


## <span data-ttu-id="b5cc4-115">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b5cc4-115">Related topics</span></span>
[<span data-ttu-id="b5cc4-116">Bereitstellen des MBAM 2.5-Clients</span><span class="sxs-lookup"><span data-stu-id="b5cc4-116">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

[<span data-ttu-id="b5cc4-117">Planen der Clientbereitstellung für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="b5cc4-117">Planning for MBAM 2.5 Client Deployment</span></span>](planning-for-mbam-25-client-deployment.md)

 

## <span data-ttu-id="b5cc4-118">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="b5cc4-118">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="b5cc4-119">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="b5cc4-119">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="b5cc4-120">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="b5cc4-120">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





