---
title: Bereitstellen des MBAM 2.5-Clients
description: Bereitstellen des MBAM 2.5-Clients
author: dansimp
ms.assetid: 0a96a0ee-f280-49d9-a244-88f4147fe9fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 375af8966c8e66a58baec5065d065891187899fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811659"
---
# <span data-ttu-id="d5384-103">Bereitstellen des MBAM 2.5-Clients</span><span class="sxs-lookup"><span data-stu-id="d5384-103">Deploying the MBAM 2.5 Client</span></span>


<span data-ttu-id="d5384-104">Die Microsoft BitLocker-Client Software für die Verwaltung und Überwachung (MBAM) ermöglicht Administratoren das erzwingen und Überwachen der BitLocker-Laufwerkverschlüsselung auf Computern im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="d5384-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client software enables administrators to enforce and monitor BitLocker Drive Encryption on computers in the enterprise.</span></span> <span data-ttu-id="d5384-105">Der BitLocker-Client kann in eine Organisation integriert werden, indem der Client über ein elektronisches Softwareverteilungssystem, wie etwa Active Directory-Domänendienste, bereitgestellt wird, oder indem die Clientcomputer im Rahmen des anfänglichen Imaging-Prozesses direkt verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="d5384-105">The BitLocker client can be integrated into an organization by deploying the client through an electronic software distribution system, such as Active Directory Domain Services, or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="d5384-106">Je nachdem, ob Sie die Microsoft BitLocker-Verwaltungs-und-Überwachungs Client Software bereitstellen, können Sie die BitLocker-Laufwerkverschlüsselung auf einem Computer in Ihrer Organisation aktivieren, bevor der Endbenutzer den Computer empfängt, oder anschließend, indem Sie die Gruppenrichtlinie konfigurieren und die MBAM-Client Software mithilfe eines Enterprise-Software Bereitstellungssystems bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d5384-106">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring Client software, you can enable BitLocker Drive Encryption on a computer in your organization either before the end user receives the computer or afterwards by configuring Group Policy and deploying the MBAM Client software by using an enterprise software deployment system.</span></span>

## <span data-ttu-id="d5384-107">Bereitstellen des MBAM-Clients auf Desktop-oder Laptopcomputern</span><span class="sxs-lookup"><span data-stu-id="d5384-107">Deploy the MBAM Client to desktop or laptop computers</span></span>


<span data-ttu-id="d5384-108">Nachdem Sie die Gruppenrichtlinieneinstellungen konfiguriert haben, können Sie ein Produkt des Enterprise-Software Bereitstellungssystems wie MicrosoftSystemCenter2012 ConfigurationManager oder Active Directory-Domänendienste verwenden, um die Windows Installer-Dateien für die MBAM-Client Installation auf Zielcomputern bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d5384-108">After configuring Group Policy settings, you can use an enterprise software deployment system product like MicrosoftSystemCenter2012 ConfigurationManager or Active Directory Domain Services to deploy the MBAM Client installation Windows Installer files to target computers.</span></span> <span data-ttu-id="d5384-109">Sie können entweder die 32-Bit-oder 64-Bit-MbamClientSetup.exe Dateien oder die 32-Bit-oder 64-Bit-MBAMClient.msi Dateien verwenden, die mit der MBAM-Client Software bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d5384-109">You can use either the 32-bit or 64-bit MbamClientSetup.exe files or the 32-bit or 64-bit MBAMClient.msi files, which are provided with the MBAM Client software.</span></span> <span data-ttu-id="d5384-110">Weitere Informationen zum Bereitstellen von MBAM-Gruppenrichtlinieneinstellungen finden Sie unter [Bereitstellen von MBAM 2,5-Gruppenrichtlinienobjekten](deploying-mbam-25-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d5384-110">For more information about deploying MBAM Group Policy settings, see [Deploying MBAM 2.5 Group Policy Objects](deploying-mbam-25-group-policy-objects.md).</span></span>

<span data-ttu-id="d5384-111">**Hinweis**  Ab MBAM 2,5 SP1 ist eine separate MSI-Version nicht mehr im MBAM-Produkt enthalten.</span><span class="sxs-lookup"><span data-stu-id="d5384-111">**Note** Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="d5384-112">Sie können die MSI-Datei jedoch aus der ausführbaren Datei (. exe) extrahieren, die im Lieferumfang des Produkts enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d5384-112">However, you can extract the MSI from the executable file (.exe) that is included with the product.</span></span>

 

[<span data-ttu-id="d5384-113">So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit</span><span class="sxs-lookup"><span data-stu-id="d5384-113">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25.md)

## <span data-ttu-id="d5384-114">Bereitstellen des MBAM-Clients als Teil einer Windows-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="d5384-114">Deploy the MBAM Client as part of a Windows deployment</span></span>


<span data-ttu-id="d5384-115">In Organisationen, in denen Computer zentral empfangen und konfiguriert werden, können Sie den MBAM-Client installieren, um die BitLocker-Laufwerkverschlüsselung auf jedem Computer zu verwalten, bevor Benutzerdaten darin geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d5384-115">In organizations where computers are received and configured centrally, you can install the MBAM Client to manage BitLocker Drive Encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="d5384-116">Der Vorteil dieses Prozesses liegt darin, dass jeder Computer dann mit der BitLocker-Laufwerkverschlüsselung kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="d5384-116">The benefit of this process is that every computer is then BitLocker Drive Encryption-compliant.</span></span> <span data-ttu-id="d5384-117">Diese Methode ist nicht auf Benutzeraktionen angewiesen, da der Administrator den Computer bereits verschlüsselt hat.</span><span class="sxs-lookup"><span data-stu-id="d5384-117">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="d5384-118">Eine wichtige Annahme für dieses Szenario ist, dass die Richtlinie des Unternehmens ein Windows-Abbild des Unternehmens installiert, bevor der Computer für den Benutzer bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d5384-118">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span> <span data-ttu-id="d5384-119">Wenn die Gruppenrichtlinieneinstellungen so konfiguriert sind, dass eine PIN erforderlich ist, werden die Benutzer aufgefordert, eine PIN festzulegen, nachdem Sie die Richtlinie erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="d5384-119">If the Group Policy settings has been configured to require a PIN, users are prompted to set a PIN after they receive the policy.</span></span>

[<span data-ttu-id="d5384-120">So aktivieren Sie BitLocker im Rahmen einer Windows-Bereitstellung mithilfe von MBAM</span><span class="sxs-lookup"><span data-stu-id="d5384-120">How to Enable BitLocker by Using MBAM as Part of a Windows Deployment</span></span>](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)

## <span data-ttu-id="d5384-121">Bereitstellen des MBAM-Clients mithilfe einer Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="d5384-121">How to deploy the MBAM Client by using a command line</span></span>


<span data-ttu-id="d5384-122">In diesem Abschnitt wird erläutert, wie Sie den MBAM-Client mithilfe einer Befehlszeile installieren.</span><span class="sxs-lookup"><span data-stu-id="d5384-122">This section explains how to install the MBAM Client by using a command line.</span></span>

[<span data-ttu-id="d5384-123">So stellen Sie den MBAM-Client über eine Befehlszeile bereit</span><span class="sxs-lookup"><span data-stu-id="d5384-123">How to Deploy the MBAM Client by Using a Command Line</span></span>](how-to-deploy-the-mbam-client-by-using-a-command-line.md)

## <span data-ttu-id="d5384-124">Weitere Ressourcen für die Bereitstellung des MBAM-Clients</span><span class="sxs-lookup"><span data-stu-id="d5384-124">Other resources for deploying the MBAM Client</span></span>


[<span data-ttu-id="d5384-125">Bereitstellen von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d5384-125">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)



## <span data-ttu-id="d5384-126">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d5384-126">Related topics</span></span>


[<span data-ttu-id="d5384-127">Bereitstellen von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d5384-127">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

[<span data-ttu-id="d5384-128">Planen von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d5384-128">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

 
## <span data-ttu-id="d5384-129">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="d5384-129">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="d5384-130">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="d5384-130">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="d5384-131">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="d5384-131">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





