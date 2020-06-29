---
title: Planen der Clientbereitstellung für MBAM 1.0
description: Planen der Clientbereitstellung für MBAM 1.0
author: dansimp
ms.assetid: 3af2e7f3-134b-4ab9-9847-b07474ca6ac3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d58d6420febd2da9ee9cd4074fc8b5870285b0b4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811419"
---
# <span data-ttu-id="6794a-103">Planen der Clientbereitstellung für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="6794a-103">Planning for MBAM 1.0 Client Deployment</span></span>


<span data-ttu-id="6794a-104">Je nachdem, wann Sie den Microsoft BitLocker-Verwaltungs-und-Überwachungs Client (MBAM) bereitstellen, können Sie die BitLocker-Verschlüsselung auf einem Computer in Ihrer Organisation aktivieren, bevor der Endbenutzer den Computer oder anschließend empfängt.</span><span class="sxs-lookup"><span data-stu-id="6794a-104">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client, you can enable BitLocker encryption on a computer in your organization either before the end user receives the computer or afterwards.</span></span> <span data-ttu-id="6794a-105">Um die BitLocker-Verschlüsselung zu aktivieren, nachdem der Endbenutzer den Computer empfangen hat, konfigurieren Sie die Gruppenrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="6794a-105">To enable BitLocker encryption after the end user receives the computer, configure Group Policy.</span></span> <span data-ttu-id="6794a-106">Um die BitLocker-Verschlüsselung zu aktivieren, bevor der Endbenutzer den Computer empfängt, stellen Sie die MBAM-Client Software mithilfe eines Enterprise-Software Bereitstellungssystems bereit.</span><span class="sxs-lookup"><span data-stu-id="6794a-106">To enable BitLocker encryption before the end user receives the computer, deploy the MBAM Client software by using an enterprise software deployment system.</span></span>

<span data-ttu-id="6794a-107">Sie können eine oder beide Methoden in Ihrer Organisation verwenden.</span><span class="sxs-lookup"><span data-stu-id="6794a-107">You can use one or both methods in your organization.</span></span> <span data-ttu-id="6794a-108">Wenn Sie beide Methoden verwenden, können Sie Compliance, Berichterstellung und Unterstützung für die Schlüsselwiederherstellung verbessern.</span><span class="sxs-lookup"><span data-stu-id="6794a-108">If you use both methods, you can improve compliance, reporting, and key recovery support.</span></span>

<span data-ttu-id="6794a-109">**Hinweis**  Informationen zum Überprüfen der MBAM-Client Systemanforderungen finden Sie unter [unterstützte MBAM 1,0-Konfigurationen](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="6794a-109">**Note** To review the MBAM Client system requirements, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

## <span data-ttu-id="6794a-110">Bereitstellen des MBAM-Clients zum Aktivieren der BitLocker-Verschlüsselung nach der Computer Verteilung an Endbenutzer</span><span class="sxs-lookup"><span data-stu-id="6794a-110">Deploying the MBAM Client to enable BitLocker encryption after computer distribution to end users</span></span>


<span data-ttu-id="6794a-111">Nachdem Sie die Gruppenrichtlinie konfiguriert haben, können Sie ein Produkt des Enterprise-Software Bereitstellungssystems wie Microsoft System Center Configuration Manager 2012 oder Active Directory-Domänendienste verwenden, um die Windows Installer-Dateien für die MBAM-Client Installation auf den Zielcomputern bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6794a-111">After you configure the Group Policy, you can use an enterprise software deployment system product, such as Microsoft System Center Configuration Manager 2012 or Active Directory Domain Services, to deploy the MBAM Client installation Windows Installer files to the target computers.</span></span> <span data-ttu-id="6794a-112">Die beiden Windows Installer-Dateien für die MBAM-Client Installation sind MBAMClient-64bit.msi und MBAMClient-32bit.msi, die mit der MBAM-Software bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6794a-112">The two MBAM Client installation Windows Installer files are MBAMClient-64bit.msi and MBAMClient-32bit.msi, which are provided with the MBAM software.</span></span> <span data-ttu-id="6794a-113">Weitere Informationen zum Bereitstellen von MBAM-Gruppenrichtlinienobjekten finden Sie unter [Bereitstellen von MBAM 1,0-Gruppenrichtlinienobjekten](deploying-mbam-10-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6794a-113">For more information about how to deploy MBAM Group Policy Objects, see [Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md).</span></span>

<span data-ttu-id="6794a-114">Wenn Sie den MBAM-Client bereitstellen, werden die Endbenutzer nach dem Verteilen der Computer an Endbenutzer aufgefordert, ihre Computer zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="6794a-114">When you deploy the MBAM Client, after you distribute the computers to end users, the end users are prompted to encrypt their computers.</span></span> <span data-ttu-id="6794a-115">Damit können MBAM die Daten sammeln, die PIN und das Kennwort einbeziehen und dann den Verschlüsselungsprozess beginnen.</span><span class="sxs-lookup"><span data-stu-id="6794a-115">This lets MBAM collect the data, to include the PIN and password, and then begin the encryption process.</span></span>

<span data-ttu-id="6794a-116">**Hinweis**  Bei dieser Vorgehensweise werden Benutzer aufgefordert, den TPM-Chip (Trusted Platform Module) zu aktivieren und zu initialisieren, wenn er zuvor nicht aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="6794a-116">**Note** In this approach, users are prompted to activate and initialize the Trusted Platform Module (TPM) chip, if it has not been previously activated.</span></span>

 

## <span data-ttu-id="6794a-117">Verwenden des MBAM-Clients zum Aktivieren der BitLocker-Verschlüsselung vor der Computer Verteilung an Endbenutzer</span><span class="sxs-lookup"><span data-stu-id="6794a-117">Using the MBAM Client to enable BitLocker encryption before computer distribution to end users</span></span>


<span data-ttu-id="6794a-118">In Organisationen, in denen Computer zentral empfangen und konfiguriert werden, können Sie den MBAM-Client installieren, um die BitLocker-Verschlüsselung auf jedem Computer zu verwalten, bevor Benutzerdaten darauf geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6794a-118">In organizations where computers are received and configured centrally, you can install the MBAM Client to manage BitLocker encryption on each computer before any user data is written on it.</span></span> <span data-ttu-id="6794a-119">Der Vorteil dieses Prozesses besteht darin, dass jeder Computer dann mit der BitLocker-Verschlüsselung kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="6794a-119">The benefit of this process is that every computer will then be compliant with the BitLocker encryption.</span></span> <span data-ttu-id="6794a-120">Diese Methode ist nicht auf Benutzeraktionen angewiesen, da der Administrator den Computer bereits verschlüsselt hat.</span><span class="sxs-lookup"><span data-stu-id="6794a-120">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="6794a-121">Eine wichtige Annahme für dieses Szenario ist, dass die Richtlinie des Unternehmens ein Windows-Abbild des Unternehmens installiert, bevor der Computer für den Benutzer bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6794a-121">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span>

<span data-ttu-id="6794a-122">Wenn Ihre Organisation (TPM) zum Verschlüsseln von Computern verwenden möchte, muss der Administrator die Betriebssystem Lautstärke des Computers mit TPM-Protector verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="6794a-122">If your organization wants to use (TPM) to encrypt computers, the administrator must encrypt the operating system volume of the computer with TPM protector.</span></span> <span data-ttu-id="6794a-123">Wenn Ihre Organisation den TPM-Chip und eine PIN-Schutzkomponente verwenden möchte, muss der Administrator das System Volume mit dem TPM-Schutz verschlüsseln, und die Benutzer wählen dann bei der ersten Anmeldung eine PIN aus.</span><span class="sxs-lookup"><span data-stu-id="6794a-123">If your organization wants to use the TPM chip and a PIN protector, the administrator must encrypt the system volume with the TPM protector, and then the users select a PIN the first time they log on.</span></span> <span data-ttu-id="6794a-124">Wenn Ihre Organisation entscheidet, nur die PIN-Beschützer zu verwenden, muss der Administrator das Volume nicht zuerst verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="6794a-124">If your organization decides to use only the PIN protector, the administrator does not have to encrypt the volume first.</span></span> <span data-ttu-id="6794a-125">Wenn Benutzer sich auf ihren Computern anmelden, fordert MBAM Sie auf, eine PIN oder eine PIN und ein Kennwort anzugeben, die Sie verwenden, wenn Sie Ihren Computer später erneut starten.</span><span class="sxs-lookup"><span data-stu-id="6794a-125">When users log on their computers, MBAM prompts them to provide a PIN or a PIN and a password that they will use when they restart their computer later.</span></span>

<span data-ttu-id="6794a-126">**Hinweis**  Die TPM-Schutzoption erfordert, dass der Administrator die BIOS-Eingabeaufforderung akzeptiert, um das TPM zu aktivieren und zu initialisieren, bevor der Computer an den Benutzer bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6794a-126">**Note** The TPM protector option requires for the administrator to accept the BIOS prompt to activate and initialize the TPM before delivering the computer to the user.</span></span>

 

## <span data-ttu-id="6794a-127">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="6794a-127">Related topics</span></span>


[<span data-ttu-id="6794a-128">Planen der Bereitstellung von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="6794a-128">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="6794a-129">Bereitstellen des MBAM 1.0-Clients</span><span class="sxs-lookup"><span data-stu-id="6794a-129">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)

 

 





