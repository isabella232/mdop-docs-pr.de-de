---
title: Verwalten von BitLocker mit MBAM
description: Verwalten von BitLocker mit MBAM
author: dansimp
ms.assetid: 2d24390a-87bf-48b3-96a9-3882d6f2a15c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d0de3711d5b7c3696783a054ee7c7f8220b5356
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811428"
---
# <span data-ttu-id="40b3e-103">Verwalten von BitLocker mit MBAM</span><span class="sxs-lookup"><span data-stu-id="40b3e-103">Performing BitLocker Management with MBAM</span></span>


<span data-ttu-id="40b3e-104">Nachdem Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) bereitgestellt haben, können Sie MBAM konfigurieren und verwenden, um die BitLocker-Unternehmens-Verschlüsselung zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="40b3e-104">After you deploy Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use MBAM to manage enterprise BitLocker encryption.</span></span> <span data-ttu-id="40b3e-105">In diesem Abschnitt werden die nach der Installation täglichen BitLocker-Verschlüsselungs Verwaltungsaufgaben beschrieben, die mithilfe von MBAM ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="40b3e-105">This section describes post-installation, day-to-day BitLocker encryption management tasks that can be accomplished by using MBAM.</span></span>

## <span data-ttu-id="40b3e-106">Zurücksetzen einer TPM-Sperrung mit MBAM</span><span class="sxs-lookup"><span data-stu-id="40b3e-106">Reset a TPM Lockout with MBAM</span></span>


<span data-ttu-id="40b3e-107">Ein TPM-Microchip (Trusted Platform Module) bietet grundlegende sicherheitsrelevante Funktionen.</span><span class="sxs-lookup"><span data-stu-id="40b3e-107">A Trusted Platform Module (TPM) microchip provides basic security-related functions.</span></span> <span data-ttu-id="40b3e-108">Diese Funktionen werden in erster Linie durch die Verwendung von Verschlüsselungsschlüsseln erreicht.</span><span class="sxs-lookup"><span data-stu-id="40b3e-108">These functions are accomplished primarily by the use of encryption keys.</span></span> <span data-ttu-id="40b3e-109">Das TPM ist in der Regel auf der Hauptplatine eines Computers oder Laptops installiert und kommuniziert mit dem restlichen System mithilfe eines Hardware Busses.</span><span class="sxs-lookup"><span data-stu-id="40b3e-109">The TPM is typically installed on the motherboard of a computer or laptop and communicates with the rest of the system by using a hardware bus.</span></span> <span data-ttu-id="40b3e-110">Computer, die ein TPM integrieren, können kryptografische Schlüssel erstellen, die nur vom TPM entschlüsselt werden können.</span><span class="sxs-lookup"><span data-stu-id="40b3e-110">Computers that incorporate a TPM can create cryptographic keys that can be decrypted only by the TPM.</span></span> <span data-ttu-id="40b3e-111">Eine TPM-Sperrung kann auftreten, wenn ein Benutzer zu oft eine falsche PIN eingibt.</span><span class="sxs-lookup"><span data-stu-id="40b3e-111">A TPM lockout can occur if a user enters an incorrect PIN too many times.</span></span> <span data-ttu-id="40b3e-112">Gibt an, wie oft ein Benutzer eine falsche PIN eingeben kann, bevor die TPM-Sperren von Hersteller zu Hersteller variieren.</span><span class="sxs-lookup"><span data-stu-id="40b3e-112">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span> <span data-ttu-id="40b3e-113">Mit dem Schlüssel Wiederherstellungsdaten System auf der MBAM-Verwaltungswebsite können Sie eine TPM-Besitzerkennwort-Datei zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="40b3e-113">The Key Recovery data system on the MBAM administration website enables you to obtain a reset TPM owner password file.</span></span>

[<span data-ttu-id="40b3e-114">So setzen Sie eine TPM-Sperre zurück</span><span class="sxs-lookup"><span data-stu-id="40b3e-114">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-1.md)

## <span data-ttu-id="40b3e-115">Wiederherstellen von Laufwerken mit MBAM</span><span class="sxs-lookup"><span data-stu-id="40b3e-115">Recover drives with MBAM</span></span>


<span data-ttu-id="40b3e-116">Stellen Sie sicher, dass Sie wissen, wie Sie bei einem Hardwarefehler, personellen Änderungen oder anderen Situationen, in denen Verschlüsselungsschlüssel verloren gehen, Datenwiederherstellung von verschlüsselten Laufwerken versuchen.</span><span class="sxs-lookup"><span data-stu-id="40b3e-116">Make sure that you know how to attempt data recovery from encrypted drives in the event of hardware failure, changes in personnel, or other situations in which encryption keys are lost.</span></span> <span data-ttu-id="40b3e-117">Die verschlüsselten Laufwerk Wiederherstellungsfeatures von MBAM bieten die Erfassung und Speicherung von Daten und die Verfügbarkeit von Tools, die für den Zugriff auf ein von BitLocker geschütztes Volume erforderlich sind, wenn das Volume in den Wiederherstellungsmodus wechselt, verschoben wird oder beschädigt wird.</span><span class="sxs-lookup"><span data-stu-id="40b3e-117">The Encrypted Drive Recovery features of MBAM provide the capture and storage of data and availability of tools required to access a BitLocker-protected volume when the volume goes into recovery mode, is moved, or becomes corrupted.</span></span>

[<span data-ttu-id="40b3e-118">So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her</span><span class="sxs-lookup"><span data-stu-id="40b3e-118">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-1.md)

[<span data-ttu-id="40b3e-119">So stellen Sie ein verschobenes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="40b3e-119">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-1.md)

[<span data-ttu-id="40b3e-120">So stellen Sie ein beschädigtes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="40b3e-120">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-1.md)

## <span data-ttu-id="40b3e-121">Ermitteln des BitLocker-Verschlüsselungsstatus von verlorenen Computern mithilfe von MBAM</span><span class="sxs-lookup"><span data-stu-id="40b3e-121">Determine BitLocker Encryption State of lost computers by Using MBAM</span></span>


<span data-ttu-id="40b3e-122">Wenn Sie MBAM verwenden, können Sie den letzten bekannten BitLocker-Verschlüsselungsstatus von verloren gegangenen oder gestohlenen Computern ermitteln.</span><span class="sxs-lookup"><span data-stu-id="40b3e-122">When you use MBAM, you can determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span>

[<span data-ttu-id="40b3e-123">Wie Sie den BitLocker-Verschlüsselung Zustand von einer nicht mehr auffindbar Computern zu ermitteln</span><span class="sxs-lookup"><span data-stu-id="40b3e-123">How to Determine the BitLocker Encryption State of a Lost Computers</span></span>](how-to-determine-the-bitlocker-encryption-state-of-a-lost-computers-mbam-1.md)

## <span data-ttu-id="40b3e-124">Weitere Ressourcen zum Durchführen der BitLocker-Verwaltung mit MBAM</span><span class="sxs-lookup"><span data-stu-id="40b3e-124">Other resources for performing BitLocker Management with MBAM</span></span>


[<span data-ttu-id="40b3e-125">Vorgänge für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="40b3e-125">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





