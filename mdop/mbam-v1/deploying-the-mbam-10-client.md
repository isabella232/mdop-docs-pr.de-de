---
title: Bereitstellen des MBAM 1.0-Clients
description: Bereitstellen des MBAM 1.0-Clients
author: dansimp
ms.assetid: f7ca233f-5035-4ff9-ab3a-f2453b4929d1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dee8c2f4a9b398c9f0797ada35e4c36610c755b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809634"
---
# <span data-ttu-id="f7e72-103">Bereitstellen des MBAM 1.0-Clients</span><span class="sxs-lookup"><span data-stu-id="f7e72-103">Deploying the MBAM 1.0 Client</span></span>


<span data-ttu-id="f7e72-104">Der Client für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) ermöglicht Administratoren das erzwingen und Überwachen der BitLocker-Laufwerkverschlüsselung auf Computern im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="f7e72-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="f7e72-105">Der BitLocker-Client kann in eine Organisation integriert werden, indem der Client mithilfe von Tools wie Active Directory-Domänendiensten oder durch direkte Verschlüsselung der Clientcomputer im Rahmen des anfänglichen Imaging-Prozesses bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f7e72-105">The BitLocker client can be integrated into an organization by deploying the client through tools like Active Directory Domain Services or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="f7e72-106">Je nachdem, ob Sie den MBAM-Client bereitstellen, können Sie die BitLocker-Verschlüsselung auf einem Computer in Ihrer Organisation aktivieren, bevor oder nachdem der Endbenutzer den Computer empfängt.</span><span class="sxs-lookup"><span data-stu-id="f7e72-106">Depending on when you deploy the MBAM Client, you can enable BitLocker encryption on a computer in your organization either before or after the end user receives the computer.</span></span> <span data-ttu-id="f7e72-107">Um diesen Zeitpunkt zu steuern, konfigurieren Sie Gruppenrichtlinien und stellen die MBAM-Client Software mithilfe eines Enterprise-Software Bereitstellungssystems bereit.</span><span class="sxs-lookup"><span data-stu-id="f7e72-107">To control this timing, you configure Group Policy and deploy the MBAM Client software by using an enterprise software deployment system.</span></span>

<span data-ttu-id="f7e72-108">Sie können eine oder beide dieser Methoden in Ihrer Organisation verwenden.</span><span class="sxs-lookup"><span data-stu-id="f7e72-108">You can use either or both of these methods in your organization.</span></span> <span data-ttu-id="f7e72-109">Wenn Sie beide Methoden verwenden, können Sie Compliance, Berichterstellung und Unterstützung für die Schlüsselwiederherstellung verbessern.</span><span class="sxs-lookup"><span data-stu-id="f7e72-109">If you use both methods, you can improve compliance, reporting, and key recovery support.</span></span>

## <span data-ttu-id="f7e72-110">Bereitstellen des MBAM-Clients auf Desktop-oder Laptopcomputern</span><span class="sxs-lookup"><span data-stu-id="f7e72-110">Deploy the MBAM Client to desktop or laptop computers</span></span>


<span data-ttu-id="f7e72-111">Nachdem Sie die Gruppenrichtlinie konfiguriert haben, können Sie die Windows Installer-Dateien für die MBAM-Client Installation auf Zielcomputern bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f7e72-111">After you have configured Group Policy, you can deploy the MBAM Client installation Windows Installer files to target computers.</span></span> <span data-ttu-id="f7e72-112">Dazu können Sie ein Produkt des Enterprise-Software Bereitstellungssystems wie Microsoft System Center 2012 Configuration Manager oder Active Directory-Domänendienste verwenden.</span><span class="sxs-lookup"><span data-stu-id="f7e72-112">You can do this by use of an enterprise software deployment system product like Microsoft System Center 2012 Configuration Manager or Active Directory Domain Services.</span></span> <span data-ttu-id="f7e72-113">Die beiden verfügbaren Windows Installer-Dateien für die MBAM-Client Installation sind MBAMClient-64bit.msi und MBAMClient-32bit.msi.</span><span class="sxs-lookup"><span data-stu-id="f7e72-113">The two available MBAM Client installation Windows Installer files are MBAMClient-64bit.msi and MBAMClient-32bit.msi.</span></span> <span data-ttu-id="f7e72-114">Diese Dateien werden mit der MBAM-Software bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="f7e72-114">These files are provided with the MBAM software.</span></span> <span data-ttu-id="f7e72-115">Weitere Informationen zum Bereitstellen von MBAM-Gruppenrichtlinienobjekten finden Sie unter [Bereitstellen von MBAM 1,0-Gruppenrichtlinienobjekten](deploying-mbam-10-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f7e72-115">For more information about how to deploy MBAM Group Policy Objects, see [Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md).</span></span>

[<span data-ttu-id="f7e72-116">So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit</span><span class="sxs-lookup"><span data-stu-id="f7e72-116">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-1.md)

## <span data-ttu-id="f7e72-117">Bereitstellen des MBAM-Clients als Teil einer Windows-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="f7e72-117">Deploy the MBAM Client as part of a Windows deployment</span></span>


<span data-ttu-id="f7e72-118">In einigen Organisationen werden neue Computer zentral empfangen und konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="f7e72-118">In some organizations, new computers are received and configured centrally.</span></span> <span data-ttu-id="f7e72-119">In dieser Situation können Administratoren den MBAM-Client installieren, um die BitLocker-Verschlüsselung auf jedem Computer zu verwalten, bevor Benutzerdaten auf den Computer geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f7e72-119">This situation enables administrators to install the MBAM Client to manage BitLocker encryption on each computer before any user data is written to the computer.</span></span> <span data-ttu-id="f7e72-120">Dieser Ansatz trägt dazu bei, sicherzustellen, dass Computer ordnungsgemäß verschlüsselt sind, da der Administrator die Aktion ausführt, ohne auf die Endbenutzer Aktion Vertrauen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="f7e72-120">This approach helps to ensure that computers are properly encrypted because the administrator performs the action without reliance on end-user action.</span></span> <span data-ttu-id="f7e72-121">Eine wichtige Annahme für dieses Szenario ist, dass die Richtlinie des Unternehmens ein Windows-Abbild des Unternehmens installiert, bevor der Computer für den Benutzer bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f7e72-121">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span>

[<span data-ttu-id="f7e72-122">So stellen Sie den MBAM-Client im Rahmen einer Windows-Bereitstellung bereit</span><span class="sxs-lookup"><span data-stu-id="f7e72-122">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-1.md)

## <span data-ttu-id="f7e72-123">Weitere Ressourcen für die Bereitstellung des MBAM-Clients</span><span class="sxs-lookup"><span data-stu-id="f7e72-123">Other resources for deploying the MBAM Client</span></span>


[<span data-ttu-id="f7e72-124">Bereitstellen von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="f7e72-124">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

[<span data-ttu-id="f7e72-125">Planen der Clientbereitstellung für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="f7e72-125">Planning for MBAM 1.0 Client Deployment</span></span>](planning-for-mbam-10-client-deployment.md)

 

 





