---
title: Bereitstellen des MBAM 2.0-Clients
description: Bereitstellen des MBAM 2.0-Clients
author: dansimp
ms.assetid: 3dd584fe-2a54-40f0-9bab-13ea74040b01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa42c8ab3adc273f0e00ba56a59f487deba89c6f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809961"
---
# <span data-ttu-id="e7abb-103">Bereitstellen des MBAM 2.0-Clients</span><span class="sxs-lookup"><span data-stu-id="e7abb-103">Deploying the MBAM 2.0 Client</span></span>


<span data-ttu-id="e7abb-104">Der Client für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) ermöglicht Administratoren das erzwingen und Überwachen der BitLocker-Laufwerkverschlüsselung auf Computern im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="e7abb-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="e7abb-105">Der BitLocker-Client kann in eine Organisation integriert werden, indem der Client über ein elektronisches Softwareverteilungssystem, wie etwa Active Directory-Domänendienste, bereitgestellt wird, oder indem die Clientcomputer im Rahmen des anfänglichen Imaging-Prozesses direkt verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="e7abb-105">The BitLocker client can be integrated into an organization by deploying the client through an electronic software distribution system, such as Active Directory Domain Services, or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="e7abb-106">Je nachdem, ob Sie den Microsoft BitLocker-Verwaltungs-und Überwachungs Client bereitstellen, können Sie die BitLocker-Verschlüsselung auf einem Computer in Ihrer Organisation aktivieren, bevor der Endbenutzer den Computer empfängt, oder anschließend, indem Sie die Gruppenrichtlinie konfigurieren und die MBAM-Client Software mithilfe eines Enterprise-Software Bereitstellungssystems bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e7abb-106">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring Client, you can enable BitLocker encryption on a computer in your organization either before the end user receives the computer or afterwards by configuring Group Policy and deploying the MBAM Client software by using an enterprise software deployment system.</span></span>

## <span data-ttu-id="e7abb-107">Bereitstellen des MBAM-Clients auf Desktop-oder Laptop Computern</span><span class="sxs-lookup"><span data-stu-id="e7abb-107">Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="e7abb-108">Nachdem Sie die Gruppenrichtlinie konfiguriert haben, können Sie ein Produkt des Enterprise-Software Bereitstellungssystems wie Microsoft System Center Configuration Manager 2012 oder Active Directory-Domänendienste verwenden, um die Windows Installer-Dateien für die MBAM-Client Installation auf Zielcomputern bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e7abb-108">After configuring Group Policy, you can use an enterprise software deployment system product like Microsoft System Center Configuration Manager 2012 or Active Directory Domain Services to deploy the MBAM Client installation Windows Installer files to target computers.</span></span> <span data-ttu-id="e7abb-109">Sie können den Client entweder mithilfe der 32-oder 64-Bit-MbamClientSetup.exe Dateien oder der 32-Bit-oder 64-Bit-MBAMClient.msi Dateien bereitstellen, die mit der MBAM-Software bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e7abb-109">You can deploy the client by using either the 32-bit or 64-bit MbamClientSetup.exe files, or the 32-bit or 64-bit MBAMClient.msi files, which are provided with the MBAM software.</span></span> <span data-ttu-id="e7abb-110">Weitere Informationen zum Bereitstellen von MBAM-Gruppenrichtlinienobjekten finden Sie unter [Bereitstellen von MBAM 2,0-Gruppenrichtlinienobjekten](deploying-mbam-20-group-policy-objects-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="e7abb-110">For more information about deploying MBAM Group Policy Objects, see [Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md).</span></span>

[<span data-ttu-id="e7abb-111">So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit</span><span class="sxs-lookup"><span data-stu-id="e7abb-111">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-2.md)

## <span data-ttu-id="e7abb-112">Bereitstellen des MBAM-Clients als Teil einer Windows-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="e7abb-112">Deploy the MBAM Client as Part of a Windows Deployment</span></span>


<span data-ttu-id="e7abb-113">In Organisationen, in denen Computer zentral empfangen und konfiguriert werden, können Sie den MBAM-Client installieren, um die BitLocker-Verschlüsselung auf jedem Computer zu verwalten, bevor Benutzerdaten darin geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e7abb-113">In organizations where computers are received and configured centrally, you can install the MBAM Client to manage BitLocker encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="e7abb-114">Der Vorteil dieses Prozesses liegt darin, dass jeder Computer dann BitLocker-Verschlüsselungs kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="e7abb-114">The benefit of this process is that every computer is then BitLocker encryption compliant.</span></span> <span data-ttu-id="e7abb-115">Diese Methode ist nicht auf Benutzeraktionen angewiesen, da der Administrator den Computer bereits verschlüsselt hat.</span><span class="sxs-lookup"><span data-stu-id="e7abb-115">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="e7abb-116">Eine wichtige Annahme für dieses Szenario ist, dass die Richtlinie des Unternehmens ein Windows-Abbild des Unternehmens installiert, bevor der Computer für den Benutzer bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e7abb-116">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span> <span data-ttu-id="e7abb-117">Wenn die Gruppenrichtlinie so konfiguriert ist, dass eine PIN erforderlich ist, werden die Benutzer aufgefordert, eine PIN festzulegen, nachdem Sie die Gruppenrichtlinie empfangen haben.</span><span class="sxs-lookup"><span data-stu-id="e7abb-117">If the Group Policy has been configured to require a PIN, users are prompted to set a PIN after they receive the Group Policy.</span></span>

[<span data-ttu-id="e7abb-118">So stellen Sie den MBAM-Client im Rahmen einer Windows-Bereitstellung bereit</span><span class="sxs-lookup"><span data-stu-id="e7abb-118">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-2.md)

## <span data-ttu-id="e7abb-119">So verwenden Sie eine Befehlszeile zum Installieren des MBAM-Clients</span><span class="sxs-lookup"><span data-stu-id="e7abb-119">How to Use a Command Line to Install the MBAM Client</span></span>


<span data-ttu-id="e7abb-120">In diesem Abschnitt wird erläutert, wie Sie den MBAM-Client mithilfe einer Befehlszeile installieren.</span><span class="sxs-lookup"><span data-stu-id="e7abb-120">This section explains how to install the MBAM Client by using a command line.</span></span>

[<span data-ttu-id="e7abb-121">So verwenden Sie eine Befehlszeile zum Installieren des MBAM-Clients</span><span class="sxs-lookup"><span data-stu-id="e7abb-121">How to Use a Command Line to Install the MBAM Client</span></span>](how-to-use-a-command-line-to-install-the-mbam-client.md)

## <span data-ttu-id="e7abb-122">Weitere Ressourcen für die Bereitstellung des MBAM-Clients</span><span class="sxs-lookup"><span data-stu-id="e7abb-122">Other Resources for Deploying the MBAM Client</span></span>


<span data-ttu-id="e7abb-123">[Bereitstellen von MBAM 2,0](deploying-mbam-20-mbam-2.md)[Planung für MBAM 2,0-Client Bereitstellung](planning-for-mbam-20-client-deployment-mbam-2.md)</span><span class="sxs-lookup"><span data-stu-id="e7abb-123">[Deploying MBAM 2.0](deploying-mbam-20-mbam-2.md)[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)</span></span>

 

 





