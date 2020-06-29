---
title: Planen der Clientbereitstellung für MBAM 2.0
description: Planen der Clientbereitstellung für MBAM 2.0
author: dansimp
ms.assetid: 3a92cf29-092f-4cad-bdfa-d5f6aafe554b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c3a7383188d4064247d8e493c8e6125fc24a1d2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804364"
---
# <span data-ttu-id="dd8d5-103">Planen der Clientbereitstellung für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="dd8d5-103">Planning for MBAM 2.0 Client Deployment</span></span>


<span data-ttu-id="dd8d5-104">Je nachdem, wann Sie den Microsoft BitLocker-Verwaltungs-und-Überwachungs Client (MBAM) bereitstellen, können Sie die BitLocker-Laufwerkverschlüsselung auf einem Computer in Ihrer Organisation aktivieren, bevor der Endbenutzer den Computer oder anschließend empfängt.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-104">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client, you can enable BitLocker drive encryption on a computer in your organization either before the end user receives the computer or afterwards.</span></span> <span data-ttu-id="dd8d5-105">Sowohl für die eigenständige MBAM als auch für die Configuration Manager-Topologien müssen Sie die Gruppenrichtlinieneinstellungen für MBAM konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-105">For both the MBAM Stand-alone and the Configuration Manager topologies, you have to configure Group Policy settings for MBAM.</span></span>

<span data-ttu-id="dd8d5-106">Wenn Sie die eigenständige MBAM-Topologie verwenden, empfiehlt es sich, ein Enterprise-Software Bereitstellungssystem zu verwenden, um die MBAM-Client Software auf Endbenutzercomputern bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-106">If you are using the MBAM Stand-alone topology, it is recommended that you use an enterprise software deployment system to deploy the MBAM Client software to end-user computers.</span></span>

<span data-ttu-id="dd8d5-107">Wenn Sie MBAM mit der Configuration Manager-Topologie bereitstellen, können Sie mithilfe von Configuration Manager die MBAM-Client Software auf Endbenutzercomputern bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-107">If you deploy MBAM with the Configuration Manager topology, you can use Configuration Manager to deploy the MBAM Client software to end-user computers.</span></span> <span data-ttu-id="dd8d5-108">In Configuration Manager erstellt die MBAM-Installation eine Sammlung von Computern, die von MBAM verwaltet werden können.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-108">In Configuration Manager, the MBAM installation creates a collection of computers that MBAM can manage.</span></span> <span data-ttu-id="dd8d5-109">Diese Sammlung umfasst Workstations und Geräte, die nicht über ein Trusted Platform Module (TPM) verfügen, aber unter Windows 8 ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-109">This collection includes workstations and devices that do not have a Trusted Platform Module (TPM), but that are running Windows 8.</span></span>

<span data-ttu-id="dd8d5-110">**Hinweis**  Windows to go wird für integrierte Configuration Manager-Installationen von MBAM nicht unterstützt, wenn Sie Configuration Manager 2007 verwenden.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-110">**Note** Windows To Go is not supported for integrated Configuration Manager installations of MBAM if you are using Configuration Manager 2007.</span></span>

 

## <span data-ttu-id="dd8d5-111">Bereitstellen des MBAM-Clients zum Aktivieren der BitLocker-Verschlüsselung nach der Computer Verteilung an Endbenutzer</span><span class="sxs-lookup"><span data-stu-id="dd8d5-111">Deploying the MBAM Client to Enable BitLocker Encryption After Computer Distribution to End Users</span></span>


<span data-ttu-id="dd8d5-112">Nachdem Sie die Gruppenrichtlinie konfiguriert haben, können Sie ein Produkt des Enterprise-Software Bereitstellungssystems wie Microsoft System Center Configuration Manager oder Active Directory-Domänendienste (AD DS) verwenden, um die Windows Installer-Dateien der MBAM-Client Installation auf Zielcomputern bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-112">After you configure Group Policy, you can use an enterprise software deployment system product like Microsoft System Center Configuration Manager or Active Directory Domain Services (AD DS) to deploy the Windows Installer files of the MBAM Client installation to target computers.</span></span> <span data-ttu-id="dd8d5-113">Zum Bereitstellen des MBAM-Clients können Sie entweder die 32-oder 64-Bit-MbamClientSetup.exe Dateien oder MBAMClient.msi Dateien verwenden, die mit der MBAM-Software bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-113">To deploy the MBAM Client, you can use either the 32-bit or 64-bit MbamClientSetup.exe files or MBAMClient.msi files, which are provided with the MBAM software.</span></span>

<span data-ttu-id="dd8d5-114">Wenn Sie den MBAM-Client nach dem Verteilen von Computern an Client Computer bereitstellen, werden Endbenutzer aufgefordert, Ihren Computer zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-114">When you deploy the MBAM Client after you distribute computers to client computers, end users are prompted to encrypt their computer.</span></span> <span data-ttu-id="dd8d5-115">Dadurch kann MBAM die Daten sammeln, die die PIN und das Kennwort enthalten, und dann den Verschlüsselungsprozess beginnen.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-115">This enables MBAM to collect the data, which includes the PIN and password, and then to begin the encryption process.</span></span>

<span data-ttu-id="dd8d5-116">**Hinweis**  Bei dieser Vorgehensweise werden Benutzer, die über Computer mit einem TPM-Chip verfügen, aufgefordert, den TPM-Chip zu aktivieren und zu initialisieren, wenn der Chip zuvor nicht aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-116">**Note** In this approach, users who have computers with a TPM chip are prompted to activate and initialize the TPM chip if the chip has not been previously activated.</span></span>

 

## <span data-ttu-id="dd8d5-117">Verwenden des MBAM-Clients zum Aktivieren der BitLocker-Verschlüsselung vor der Computer Verteilung an Endbenutzer</span><span class="sxs-lookup"><span data-stu-id="dd8d5-117">Using the MBAM Client to Enable BitLocker Encryption Before Computer Distribution to End Users</span></span>


<span data-ttu-id="dd8d5-118">In Organisationen, in denen Computer zentral empfangen und konfiguriert werden und Computer über einen kompatiblen TPM-Chip verfügen, können Sie den MBAM-Client installieren, um die BitLocker-Verschlüsselung auf jedem Computer zu verwalten, bevor Benutzerdaten darin geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-118">In organizations where computers are received and configured centrally, and where computers have a compliant TPM chip, you can install the MBAM Client to manage BitLocker encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="dd8d5-119">Der Vorteil dieses Prozesses liegt darin, dass jeder Computer dann BitLocker-Verschlüsselungs kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-119">The benefit of this process is that every computer will then be BitLocker encryption-compliant.</span></span> <span data-ttu-id="dd8d5-120">Diese Methode ist nicht auf Benutzeraktionen angewiesen, da der Administrator den Computer bereits verschlüsselt hat.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-120">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="dd8d5-121">Eine wichtige Annahme für dieses Szenario ist, dass die Richtlinie des Unternehmens ein Windows-Abbild des Unternehmens installiert, bevor der Computer für den Benutzer bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-121">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span>

<span data-ttu-id="dd8d5-122">Wenn Ihre Organisation den TPM-Chip zum Verschlüsseln von Computern verwenden möchte, fügt der Administrator die TPM-Beschützer hinzu, um das Betriebssystem Volumen des Computers zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-122">If your organization wants to use the TPM chip to encrypt computers, the administrator adds the TPM protector to encrypt the operating system volume of the computer.</span></span> <span data-ttu-id="dd8d5-123">Wenn Ihre Organisation den TPM-Chip und eine PIN-Schutzkomponente verwenden möchte, verschlüsselt der Administrator das Betriebssystemvolume mit dem TPM-Schutz, und dann wählen Benutzer eine PIN aus, wenn Sie sich zum ersten Mal anmelden.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-123">If your organization wants to use the TPM chip and a PIN protector, the administrator encrypts the operating system volume with the TPM protector, and then users select a PIN when they log on for the first time.</span></span> <span data-ttu-id="dd8d5-124">Wenn Ihre Organisation entscheidet, nur die PIN-Beschützer zu verwenden, muss der Administrator das Volume nicht zuerst verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-124">If your organization decides to use only the PIN protector, the administrator does not have to encrypt the volume first.</span></span> <span data-ttu-id="dd8d5-125">Wenn Benutzer sich anmelden, werden Sie von der Microsoft BitLocker-Verwaltung und-Überwachung aufgefordert, eine PIN oder eine PIN und ein Kennwort anzugeben, die für spätere Computerneustarts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-125">When users log on, Microsoft BitLocker Administration and Monitoring prompts them to provide a PIN, or a PIN and password to be used on later computer restarts.</span></span>

<span data-ttu-id="dd8d5-126">**Hinweis**  Die TPM-Schutzoption setzt voraus, dass der Administrator die BIOS-Eingabeaufforderung akzeptiert, um das TPM zu aktivieren und zu initialisieren, bevor der Computer an den Benutzer übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-126">**Note** The TPM protector option requires the administrator to accept the BIOS prompt to activate and initialize the TPM before the computer is delivered to the user.</span></span>

 

## <span data-ttu-id="dd8d5-127">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="dd8d5-127">Related topics</span></span>


[<span data-ttu-id="dd8d5-128">Planen der Bereitstellung von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="dd8d5-128">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="dd8d5-129">Bereitstellen des MBAM 2.0-Clients</span><span class="sxs-lookup"><span data-stu-id="dd8d5-129">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)

 

 





