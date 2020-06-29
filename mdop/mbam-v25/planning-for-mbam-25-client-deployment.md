---
title: Planen der Clientbereitstellung für MBAM 2.5
description: Planen der Clientbereitstellung für MBAM 2.5
author: dansimp
ms.assetid: 23c89976-af24-4753-9412-ce0ea42d1964
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ff03b58da0985b2f57308c99a9bc15f4a0554623
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811488"
---
# <span data-ttu-id="390c6-103">Planen der Clientbereitstellung für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="390c6-103">Planning for MBAM 2.5 Client Deployment</span></span>


<span data-ttu-id="390c6-104">Je nachdem, wann Sie die Microsoft BitLocker-Verwaltungs-und Überwachungs-Client Software (MBAM) bereitstellen, können Sie die BitLocker-Laufwerkverschlüsselung auf einem Computer in Ihrer Organisation aktivieren, bevor der Endbenutzer den Computer oder anschließend empfängt.</span><span class="sxs-lookup"><span data-stu-id="390c6-104">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client software, you can enable BitLocker Drive Encryption on a computer in your organization either before the end user receives the computer or afterwards.</span></span> <span data-ttu-id="390c6-105">Für die MBAM eigenständige und die System Center Configuration Manager-Integrations Topologien müssen Sie die Gruppenrichtlinieneinstellungen für MBAM konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="390c6-105">For both the MBAM Stand-alone and the System Center Configuration Manager Integration topologies, you have to configure Group Policy settings for MBAM.</span></span>

<span data-ttu-id="390c6-106">Wenn Sie die eigenständige MBAM-Topologie verwenden, empfiehlt es sich, ein Enterprise-Software Bereitstellungssystem zu verwenden, um die MBAM-Client Software auf Endbenutzercomputern bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="390c6-106">If you are using the MBAM Stand-alone topology, we recommend that you use an enterprise software deployment system to deploy the MBAM Client software to end-user computers.</span></span>

<span data-ttu-id="390c6-107">Wenn Sie MBAM mit der Configuration Manager-Integrations Topologie bereitstellen, können Sie mithilfe von Configuration Manager die MBAM-Client Software auf Endbenutzercomputern bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="390c6-107">If you deploy MBAM with the Configuration Manager Integration topology, you can use Configuration Manager to deploy the MBAM Client software to end-user computers.</span></span> <span data-ttu-id="390c6-108">In Configuration Manager erstellt die MBAM-Installation eine Sammlung von Computern, die von MBAM verwaltet werden können.</span><span class="sxs-lookup"><span data-stu-id="390c6-108">In Configuration Manager, the MBAM installation creates a collection of computers that MBAM can manage.</span></span> <span data-ttu-id="390c6-109">Diese Sammlung umfasst Workstations und Geräte, die nicht über ein Trusted Platform Module (TPM) verfügen, aber unter Windows 8, Windows 8,1 oder Windows 10 ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="390c6-109">This collection includes workstations and devices that do not have a Trusted Platform Module (TPM), but that are running Windows 8, Windows 8.1, or Windows 10.</span></span>

<span data-ttu-id="390c6-110">**Hinweis**  Windows to go wird bei der Installation der Configuration Manager-Integrations Topologie nicht unterstützt, wenn Sie Configuration Manager 2007 verwenden.</span><span class="sxs-lookup"><span data-stu-id="390c6-110">**Note** Windows To Go is not supported for the Configuration Manager Integration topology installation when you are using Configuration Manager 2007.</span></span>

 

## <span data-ttu-id="390c6-111">Bereitstellen des MBAM-Clients zum Aktivieren der BitLocker-Laufwerkverschlüsselung nach der Computer Verteilung an Endbenutzer</span><span class="sxs-lookup"><span data-stu-id="390c6-111">Deploying the MBAM Client to enable BitLocker Drive Encryption after computer distribution to end users</span></span>


<span data-ttu-id="390c6-112">Nachdem Sie die Gruppenrichtlinie konfiguriert haben, können Sie ein Produkt des Enterprise-Software Bereitstellungssystems wie Microsoft System Center Configuration Manager oder Active Directory-Domänendienste (AD DS) verwenden, um die Windows Installer-Dateien der MBAM-Client Installation auf Zielcomputern bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="390c6-112">After you configure Group Policy, you can use an enterprise software deployment system product like Microsoft System Center Configuration Manager or Active Directory Domain Services (AD DS) to deploy the Windows Installer files of the MBAM Client installation to target computers.</span></span> <span data-ttu-id="390c6-113">Zum Bereitstellen des MBAM-Clients können Sie entweder die 32-oder 64-Bit-MbamClientSetup.exe Dateien oder MBAMClient.msi Dateien verwenden, die mit der MBAM-Client Software bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="390c6-113">To deploy the MBAM Client, you can use either the 32-bit or 64-bit MbamClientSetup.exe files or MBAMClient.msi files, which are provided with the MBAM Client software.</span></span>

<span data-ttu-id="390c6-114">**Hinweis**  Ab MBAM 2,5 SP1 ist eine separate MSI-Version nicht mehr im MBAM-Produkt enthalten.</span><span class="sxs-lookup"><span data-stu-id="390c6-114">**Note** Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="390c6-115">Sie können die MSI-Datei jedoch aus der ausführbaren Datei (. exe) extrahieren, die im Lieferumfang des Produkts enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="390c6-115">However, you can extract the MSI from the executable file (.exe) that is included with the product.</span></span>

 

<span data-ttu-id="390c6-116">Wenn Sie den MBAM-Client nach dem Verteilen von Computern an Client Computer bereitstellen, werden Endbenutzer aufgefordert, Ihren Computer zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="390c6-116">When you deploy the MBAM Client after you distribute computers to client computers, end users are prompted to encrypt their computer.</span></span> <span data-ttu-id="390c6-117">Diese Aktion ermöglicht es MBAM, die Daten zu sammeln, einschließlich der PIN und des Kennworts (bei Bedarf nach Richtlinie), und dann den Verschlüsselungsprozess zu starten.</span><span class="sxs-lookup"><span data-stu-id="390c6-117">This action enables MBAM to collect the data, which includes the PIN and password (if required by policy), and then to begin the encryption process.</span></span>

<span data-ttu-id="390c6-118">**Hinweis**  Bei dieser Vorgehensweise werden Endbenutzer, die über Computer mit einem TPM-Chip verfügen, aufgefordert, den TPM-Chip zu aktivieren und zu initialisieren, wenn der Chip zuvor nicht aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="390c6-118">**Note** In this approach, end users who have computers with a TPM chip are prompted to activate and initialize the TPM chip if the chip has not been previously activated.</span></span>

 

## <span data-ttu-id="390c6-119">Verwenden des MBAM-Clients zum Aktivieren der BitLocker-Laufwerkverschlüsselung vor der Computer Verteilung an Endbenutzer</span><span class="sxs-lookup"><span data-stu-id="390c6-119">Using the MBAM Client to enable BitLocker Drive Encryption before computer distribution to end users</span></span>


<span data-ttu-id="390c6-120">In Organisationen, in denen Computer zentral empfangen und konfiguriert werden und Computer über einen kompatiblen TPM-Chip verfügen, können Sie den MBAM-Client verwenden, um die BitLocker-Laufwerkverschlüsselung auf jedem Computer zu verwalten, bevor Benutzerdaten darin geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="390c6-120">In organizations where computers are received and configured centrally, and where computers have a compliant TPM chip, you can use the MBAM Client to manage BitLocker Drive Encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="390c6-121">Der Vorteil dieses Prozesses liegt darin, dass jeder Computer dann kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="390c6-121">The benefit of this process is that every computer is then compliant.</span></span> <span data-ttu-id="390c6-122">Diese Methode ist nicht auf Endbenutzeraktionen angewiesen, da der Administrator den Computer bereits verschlüsselt hat.</span><span class="sxs-lookup"><span data-stu-id="390c6-122">This method does not rely on end-user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="390c6-123">Eine wichtige Voraussetzung für dieses Szenario ist, dass die Richtlinie des Unternehmens ein Windows-Abbild des Unternehmens installiert, bevor der Computer an den Endbenutzer übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="390c6-123">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the end user.</span></span>

<span data-ttu-id="390c6-124">Wenn Ihre Organisation den TPM-Chip zum Verschlüsseln von Computern verwenden möchte, fügt der Administrator die TPM-Beschützer hinzu, um das Betriebssystem Volumen des Computers zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="390c6-124">If your organization wants to use the TPM chip to encrypt computers, the administrator adds the TPM protector to encrypt the operating system volume of the computer.</span></span> <span data-ttu-id="390c6-125">Wenn Ihre Organisation den TPM-Chip und eine PIN-Schutzkomponente verwenden möchte, verschlüsselt der Administrator das Betriebssystemvolume mit dem TPM-Schutz, und dann wählen Endbenutzer eine PIN aus, wenn Sie sich zum ersten Mal anmelden.</span><span class="sxs-lookup"><span data-stu-id="390c6-125">If your organization wants to use the TPM chip and a PIN protector, the administrator encrypts the operating system volume with the TPM protector, and then end users select a PIN when they log on for the first time.</span></span> <span data-ttu-id="390c6-126">Wenn Ihre Organisation entscheidet, nur die PIN-Beschützer zu verwenden, muss der Administrator das Volume nicht zuerst verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="390c6-126">If your organization decides to use only the PIN protector, the administrator does not have to encrypt the volume first.</span></span> <span data-ttu-id="390c6-127">Wenn sich die Endbenutzer anmelden, werden Sie von der Microsoft BitLocker-Verwaltung und-Überwachung aufgefordert, eine PIN oder eine PIN und ein Kennwort anzugeben, die bei einem späteren Neustart des Computers verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="390c6-127">When end users log on, Microsoft BitLocker Administration and Monitoring prompts them to provide a PIN, or a PIN and password to be used on later computer restarts.</span></span>

<span data-ttu-id="390c6-128">**Hinweis**  Die TPM-Schutzoption setzt voraus, dass der Administrator die BIOS-Eingabeaufforderung akzeptiert, um das TPM zu aktivieren und zu initialisieren, bevor der Computer an den Endbenutzer übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="390c6-128">**Note** The TPM protector option requires the administrator to accept the BIOS prompt to activate and initialize the TPM before the computer is delivered to the end user.</span></span>

 

## <span data-ttu-id="390c6-129">MBAM-Client Unterstützung für verschlüsselte Festplatten</span><span class="sxs-lookup"><span data-stu-id="390c6-129">MBAM Client support for Encrypted Hard Drives</span></span>


<span data-ttu-id="390c6-130">MBAM unterstützt BitLocker auf verschlüsselten Festplatten, die die TCG-Spezifikationsanforderungen für Opal-und IEEE-1667-Standards erfüllen.</span><span class="sxs-lookup"><span data-stu-id="390c6-130">MBAM supports BitLocker on Encrypted Hard Drives that meet TCG specification requirements for Opal as well as IEEE 1667 standards.</span></span> <span data-ttu-id="390c6-131">Wenn BitLocker auf diesen Geräten aktiviert ist, generiert es Schlüssel und führt Verwaltungsfunktionen auf dem verschlüsselten Laufwerk aus.</span><span class="sxs-lookup"><span data-stu-id="390c6-131">When BitLocker is enabled on these devices, it will generate keys and perform management functions on the encrypted drive.</span></span> <span data-ttu-id="390c6-132">Weitere Informationen finden Sie unter [verschlüsselte Festplatte](https://technet.microsoft.com/library/hh831627.aspx) .</span><span class="sxs-lookup"><span data-stu-id="390c6-132">See [Encrypted Hard Drive](https://technet.microsoft.com/library/hh831627.aspx) for more information.</span></span>


## <span data-ttu-id="390c6-133">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="390c6-133">Related topics</span></span>


[<span data-ttu-id="390c6-134">Planen der Bereitstellung von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="390c6-134">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="390c6-135">Bereitstellen des MBAM 2.5-Clients</span><span class="sxs-lookup"><span data-stu-id="390c6-135">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

 

 
## <span data-ttu-id="390c6-136">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="390c6-136">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="390c6-137">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="390c6-137">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="390c6-138">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="390c6-138">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




