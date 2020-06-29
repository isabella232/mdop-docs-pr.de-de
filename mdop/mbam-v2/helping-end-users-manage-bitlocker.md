---
title: Unterstützung für Endbenutzer beim Verwalten von BitLocker
description: Unterstützung für Endbenutzer beim Verwalten von BitLocker
author: dansimp
ms.assetid: 47776fb3-2d94-4970-b687-c35ec3dd6c64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26ef2bc33a75ff7773b75807ab0e10e5aa67b109
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810759"
---
# <span data-ttu-id="4561e-103">Unterstützung für Endbenutzer beim Verwalten von BitLocker</span><span class="sxs-lookup"><span data-stu-id="4561e-103">Helping End Users Manage BitLocker</span></span>


<span data-ttu-id="4561e-104">Inhalte auf einem verlorenen oder gestohlenen Computer sind anfällig für unbefugten Zugriff, der sowohl für Personen als auch für Unternehmen ein Sicherheitsrisiko darstellen kann.</span><span class="sxs-lookup"><span data-stu-id="4561e-104">Content on a lost or stolen computer is vulnerable to unauthorized access, which can present a security risk to both people and companies.</span></span> <span data-ttu-id="4561e-105">Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) verwendet BitLocker, um unbefugten Zugriff zu verhindern, indem Sie Ihren Computer sperren, um vertrauliche Daten vor böswilligen Benutzern zu schützen.</span><span class="sxs-lookup"><span data-stu-id="4561e-105">Microsoft BitLocker Administration and Monitoring (MBAM) uses BitLocker to help prevent unauthorized access by locking your computer to help protect sensitive data from malicious users.</span></span>

## <span data-ttu-id="4561e-106">Was ist BitLocker?</span><span class="sxs-lookup"><span data-stu-id="4561e-106">What is BitLocker?</span></span>


<span data-ttu-id="4561e-107">Die BitLocker-Laufwerkverschlüsselung bietet Schutz für Betriebssystemlaufwerke, Datenlaufwerke und Wechseldatenträger (wie ein USB-Thumb-Laufwerk), indem die Laufwerke verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="4561e-107">BitLocker Drive Encryption can provide protection for operating system drives, data drives, and removable drives (such as a USB thumb drive) by encrypting the drives.</span></span> <span data-ttu-id="4561e-108">Je nachdem, wie BitLocker konfiguriert ist, müssen die Benutzer möglicherweise einen Schlüssel (ein Kennwort oder eine PIN) bereitstellen, um die auf den verschlüsselten Laufwerken gespeicherten Informationen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="4561e-108">Depending on how BitLocker is configured, users may have to provide a key (a password or PIN) to unlock the information that is stored on the encrypted drives.</span></span>

<span data-ttu-id="4561e-109">Wenn Sie einem mit BitLocker verschlüsselten Laufwerk neue Dateien hinzufügen, werden Sie von BitLocker automatisch verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="4561e-109">When you add new files to a drive that is encrypted with BitLocker, BitLocker encrypts them automatically.</span></span> <span data-ttu-id="4561e-110">Dateien bleiben nur verschlüsselt, während Sie auf dem verschlüsselten Laufwerk gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="4561e-110">Files remain encrypted only while they are stored in the encrypted drive.</span></span> <span data-ttu-id="4561e-111">Dateien, die auf ein anderes Laufwerk oder einen anderen Computer kopiert werden, werden entschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="4561e-111">Files that are copied to another drive or computer are decrypted.</span></span> <span data-ttu-id="4561e-112">Wenn Sie Dateien für andere Benutzer freigeben, beispielsweise über ein Netzwerk, werden diese Dateien verschlüsselt, während Sie auf dem verschlüsselten Laufwerk gespeichert sind, aber Sie können normalerweise von autorisierten Benutzern aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4561e-112">If you share files with other users, such as through a network, these files are encrypted while stored on the encrypted drive, but they can be accessed normally by authorized users.</span></span>

<span data-ttu-id="4561e-113">Wenn Sie das Betriebssystemlaufwerk verschlüsseln, überprüft BitLocker den Computer während des Starts auf alle Bedingungen, die ein Sicherheitsrisiko darstellen könnten (beispielsweise eine Änderung des BIOS oder Änderungen an Startdateien).</span><span class="sxs-lookup"><span data-stu-id="4561e-113">If you encrypt the operating system drive, BitLocker checks the computer during startup for any conditions that could represent a security risk (for example, a change to the BIOS or changes to any startup files).</span></span> <span data-ttu-id="4561e-114">Wenn ein potenzielles Sicherheitsrisiko erkannt wird, sperrt BitLocker das Betriebssystemlaufwerk und erfordert einen speziellen BitLocker-Wiederherstellungsschlüssel, um es zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="4561e-114">If a potential security risk is detected, BitLocker will lock the operating system drive and require a special BitLocker recovery key to unlock it.</span></span> <span data-ttu-id="4561e-115">Stellen Sie sicher, dass Sie diesen Wiederherstellungsschlüssel erstellen, wenn Sie BitLocker zum ersten Mal aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4561e-115">Make sure that you create this recovery key when you turn on BitLocker for the first time.</span></span> <span data-ttu-id="4561e-116">Andernfalls können Sie den Zugriff auf Ihre Dateien dauerhaft verlieren.</span><span class="sxs-lookup"><span data-stu-id="4561e-116">Otherwise, you could permanently lose access to your files.</span></span>

<span data-ttu-id="4561e-117">Wenn Sie Datenlaufwerke (behoben oder abnehmbar) verschlüsseln, können Sie ein verschlüsseltes Laufwerk mit einem Kennwort oder einer Smartcard entsperren oder das Laufwerk so einrichten, dass es automatisch entsperrt wird, wenn Sie sich am Computer anmelden.</span><span class="sxs-lookup"><span data-stu-id="4561e-117">If you encrypt data drives (fixed or removable), you can unlock an encrypted drive with a password or a smart card, or set the drive to automatically unlock when you log on to the computer.</span></span>

<span data-ttu-id="4561e-118">Neben Kennwörtern und Pins kann BitLocker den TPM-Chip (Trusted Platform Module) verwenden, der auf vielen neueren Computern bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4561e-118">In addition to passwords and PINs, BitLocker can use the Trusted Platform Module (TPM) chip that is provided in many newer computers.</span></span> <span data-ttu-id="4561e-119">Der TPM-Chip wird verwendet, um sicherzustellen, dass Ihr Computer nicht manipuliert wurde, bevor BitLocker das Betriebssystemlaufwerk aufheben kann.</span><span class="sxs-lookup"><span data-stu-id="4561e-119">The TPM chip is used to ensure that your computer has not been tampered with before BitLocker will unlock the operating system drive.</span></span> <span data-ttu-id="4561e-120">Während des Verschlüsselungsprozesses müssen Sie möglicherweise den TPM-Chip aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4561e-120">During the encryption process, you may have to enable the TPM chip.</span></span> <span data-ttu-id="4561e-121">Wenn Sie Ihren Computer starten, fragt BitLocker das TPM nach den Schlüsseln für das Laufwerk und entsperrt es.</span><span class="sxs-lookup"><span data-stu-id="4561e-121">When you start your computer, BitLocker asks the TPM for the keys to the drive and unlocks it.</span></span> <span data-ttu-id="4561e-122">Um den TPM-Chip zu aktivieren, müssen Sie Ihren Computer neu starten und dann eine Einstellung im BIOS, einer Pre-Windows-Schicht ihrer Computer Software, ändern.</span><span class="sxs-lookup"><span data-stu-id="4561e-122">To enable the TPM chip, you will have to restart your computer and then change a setting in the BIOS, a pre-Windows layer of your computer software.</span></span> <span data-ttu-id="4561e-123">Weitere Informationen zum TPM finden Sie unter Informationen zum TPM- [Chip des Computers](about-the-computer-tpm-chip.md).</span><span class="sxs-lookup"><span data-stu-id="4561e-123">For more information about the TPM, see [About the Computer TPM Chip](about-the-computer-tpm-chip.md).</span></span>

<span data-ttu-id="4561e-124">Sobald Ihr Computer von BitLocker geschützt ist, müssen Sie möglicherweise jedes Mal eine PIN oder ein Kennwort eingeben, wenn der Computer aus dem Ruhezustand oder gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="4561e-124">Once your computer is protected by BitLocker, you may have to enter a PIN or password every time that the computer wakes from hibernation or starts.</span></span> <span data-ttu-id="4561e-125">Der Helpdesk für Ihr Unternehmen oder Ihre Organisation kann Ihnen helfen, wenn Sie jemals Ihre PIN oder Ihr Kennwort vergessen.</span><span class="sxs-lookup"><span data-stu-id="4561e-125">The Help Desk for your company or organization can help if you ever forget your PIN or password.</span></span>

<span data-ttu-id="4561e-126">Sie können BitLocker entweder vorübergehend deaktivieren, indem Sie das Laufwerk entschlüsseln oder dauerhaft sperren.</span><span class="sxs-lookup"><span data-stu-id="4561e-126">You can turn off BitLocker, either temporarily, by suspending it, or permanently, by decrypting the drive.</span></span>

<span data-ttu-id="4561e-127">**Hinweis**  Da BitLocker das gesamte Laufwerk und nicht nur die einzelnen Dateien selbst verschlüsselt, seien Sie vorsichtig, wenn Sie sensible Daten zwischen Laufwerken verschieben.</span><span class="sxs-lookup"><span data-stu-id="4561e-127">**Note** Because BitLocker encrypts the whole drive and not just the individual files themselves, be careful when you move sensitive data between drives.</span></span> <span data-ttu-id="4561e-128">Wenn Sie eine Datei von einem mit BitLocker geschützten Laufwerk auf ein nicht verschlüsseltes Laufwerk verschieben, wird die Datei nicht mehr verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="4561e-128">If you move a file from a BitLocker-protected drive to a nonencrypted drive, the file will no longer be encrypted.</span></span>

 

## <span data-ttu-id="4561e-129">Informationen zur BitLocker-Verschlüsselungsoptionen-Anwendung</span><span class="sxs-lookup"><span data-stu-id="4561e-129">About the BitLocker Encryption Options Application</span></span>


<span data-ttu-id="4561e-130">Wenn Sie Festplattenlaufwerke auf dem Computer entsperren und Ihre PIN und Kennwörter verwalten möchten, verwenden Sie die BitLocker-Anwendung Verschlüsselungsoptionen in der Windows-Systemsteuerung, indem Sie das hier beschriebene Verfahren ausführen.</span><span class="sxs-lookup"><span data-stu-id="4561e-130">To unlock hard disk drives on your computer and to manage your PIN and passwords, use the BitLocker Encryption Options application in the Windows Control Panel by following the procedure outlined here.</span></span> <span data-ttu-id="4561e-131">Sie können Kennwörter zum Entsperren geschützter Laufwerke eingeben und den BitLocker-Status von angefügten Laufwerken mithilfe dieser Anwendung überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4561e-131">You can enter passwords to unlock protected drives and can check the BitLocker status of attached drives by using this application.</span></span>

**<span data-ttu-id="4561e-132">So öffnen Sie die BitLocker-Verschlüsselungsoptionen-Anwendung</span><span class="sxs-lookup"><span data-stu-id="4561e-132">To open the BitLocker Encryption Options application</span></span>**

1.  <span data-ttu-id="4561e-133">Klicken Sie auf **Start**, und wählen Sie **System**Steuerung aus.</span><span class="sxs-lookup"><span data-stu-id="4561e-133">Click **Start**, and select **Control Panel**.</span></span> <span data-ttu-id="4561e-134">Die Systemsteuerung wird in einem neuen Fenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="4561e-134">The Control Panel opens in a new window.</span></span>

2.  <span data-ttu-id="4561e-135">Wählen Sie **in der** **Systemsteuerung System und Sicherheit**aus.</span><span class="sxs-lookup"><span data-stu-id="4561e-135">In **Control Panel**, select **System and Security**.</span></span>

3.  <span data-ttu-id="4561e-136">Wählen Sie **BitLocker-Verschlüsselungsoptionen** aus, um die BitLocker-Verschlüsselungsoptionen-Anwendung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4561e-136">Select **BitLocker Encryption Options** to open the BitLocker Encryption Options application.</span></span>

    <span data-ttu-id="4561e-137">Eine Beschreibung der verfügbaren Optionen finden Sie im folgenden Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="4561e-137">For a description of the available options, see the following section.</span></span>

## <span data-ttu-id="4561e-138">Optionen für die BitLocker-Verschlüsselungsoptionen-Anwendung</span><span class="sxs-lookup"><span data-stu-id="4561e-138">Options on the BitLocker Encryption Options Application</span></span>


<span data-ttu-id="4561e-139">Mit der BitLocker-Anwendung für Verschlüsselungsoptionen in der Systemsteuerung können Sie Ihre PIN und Kennwörter verwalten, die BitLocker zum Schutz Ihres Computers verwendet.</span><span class="sxs-lookup"><span data-stu-id="4561e-139">The BitLocker Encryption Options application on Control Panel lets you manage your PIN and passwords, which BitLocker uses to protect your computer.</span></span>

**<span data-ttu-id="4561e-140">BitLocker-Laufwerkverschlüsselung – feste Festplatten:</span><span class="sxs-lookup"><span data-stu-id="4561e-140">BitLocker Drive Encryption – Fixed Disk Drives:</span></span>**

<span data-ttu-id="4561e-141">In diesem Abschnitt können Sie Informationen zu Festplatten, die mit Ihrem Computer verbunden sind, und deren aktuellen BitLocker-Verschlüsselungsstatus anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4561e-141">In this section, you can view information about hard disk drives connected to your computer and their current BitLocker Encryption status.</span></span>

-   <span data-ttu-id="4561e-142">**Verwalten der PIN** – ändert die PIN, die von BitLocker zum Entsperren Ihres Betriebssystemlaufwerks verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4561e-142">**Manage your PIN** - changes the PIN used by BitLocker to unlock your operating system drive.</span></span>

-   <span data-ttu-id="4561e-143">**Verwalten Ihres Kennworts** – ändert das Kennwort, das von BitLocker zum Entsperren ihrer anderen internen Laufwerke verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4561e-143">**Manage your password** - changes the password that is used by BitLocker to unlock your other internal drives.</span></span>

**<span data-ttu-id="4561e-144">BitLocker-Laufwerkverschlüsselung – externe Laufwerke:</span><span class="sxs-lookup"><span data-stu-id="4561e-144">BitLocker Drive Encryption - External Drives:</span></span>**

<span data-ttu-id="4561e-145">In diesem Abschnitt können Sie Informationen zu externen Laufwerken (wie einem USB-Daumen Laufwerk) anzeigen, die mit Ihrem Computer verbunden sind, und deren aktuellen BitLocker-Verschlüsselungsstatus.</span><span class="sxs-lookup"><span data-stu-id="4561e-145">In this section, you can view information about external drives (such as a USB thumb drive) connected to your computer, and their current BitLocker encryption status.</span></span>

-   <span data-ttu-id="4561e-146">**Verwalten Ihres Kennworts** – ändert das Kennwort, das von BitLocker zum Entsperren ihrer anderen internen Laufwerke verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4561e-146">**Manage your password** - changes the password that is used by BitLocker to unlock your other internal drives.</span></span>

**<span data-ttu-id="4561e-147">Erweiterte</span><span class="sxs-lookup"><span data-stu-id="4561e-147">Advanced:</span></span>**

-   <span data-ttu-id="4561e-148">**TPM-Administration** – öffnet das TPM-Verwaltungstool in einem separaten Fenster.</span><span class="sxs-lookup"><span data-stu-id="4561e-148">**TPM Administration** - opens the TPM Administration tool in a separate window.</span></span> <span data-ttu-id="4561e-149">Hier können Sie allgemeine TPM-Aufgaben konfigurieren und Informationen zum TPM-Chipsatz abrufen.</span><span class="sxs-lookup"><span data-stu-id="4561e-149">From here you can configure common TPM tasks and obtain information about the TPM chipset.</span></span> <span data-ttu-id="4561e-150">Sie müssen über Administratorrechte auf dem Computer verfügen, um auf dieses Tool zugreifen zu können.</span><span class="sxs-lookup"><span data-stu-id="4561e-150">You must have administrative permissions on your computer to access this tool.</span></span>

-   <span data-ttu-id="4561e-151">**Datenträgerverwaltung** – öffnen Sie das Datenträger Verwaltungstool.</span><span class="sxs-lookup"><span data-stu-id="4561e-151">**Disk Management** -open the Disk Management tool.</span></span> <span data-ttu-id="4561e-152">Hier können Sie die Informationen für alle an den Computer angeschlossenen Festplatten anzeigen sowie Partitionen und Laufwerksoptionen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="4561e-152">From here you can view the information for all hard drives connected to the computer and configure partitions and drive options.</span></span> <span data-ttu-id="4561e-153">Sie müssen über Administratorrechte auf dem Computer verfügen, um auf dieses Tool zugreifen zu können.</span><span class="sxs-lookup"><span data-stu-id="4561e-153">You must have administrative rights on your computer to access this tool.</span></span>

 

 





