---
title: Verwalten von BitLocker mit MBAM
description: Verwalten von BitLocker mit MBAM
author: dansimp
ms.assetid: 9bfc6c67-f12c-4daa-8f08-5884fb47443c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d261ec4fa789cd331209afe1c2f1858d627209a3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811791"
---
# <span data-ttu-id="a476c-103">Verwalten von BitLocker mit MBAM</span><span class="sxs-lookup"><span data-stu-id="a476c-103">Performing BitLocker Management with MBAM</span></span>


<span data-ttu-id="a476c-104">Nachdem Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) geplant und dann bereitgestellt haben, können Sie diese zum Verwalten der BitLocker-Unternehmens-Verschlüsselung konfigurieren und verwenden.</span><span class="sxs-lookup"><span data-stu-id="a476c-104">After planning and then deploying Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use it to manage enterprise BitLocker encryption.</span></span> <span data-ttu-id="a476c-105">Die Informationen in diesem Abschnitt beschreiben die täglichen Aufgaben der BitLocker-Verschlüsselungs Verwaltung nach der Installation, die mithilfe der Microsoft BitLocker-Verwaltung und-Überwachung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a476c-105">The information in this section describes post-installation day-to-day BitLocker encryption management tasks that are accomplished by using Microsoft BitLocker Administration and Monitoring.</span></span>

## <span data-ttu-id="a476c-106">Zurücksetzen einer TPM-Sperrung mithilfe von MBAM</span><span class="sxs-lookup"><span data-stu-id="a476c-106">Reset a TPM Lockout by Using MBAM</span></span>


<span data-ttu-id="a476c-107">Bei einem Trusted Platform Module (TPM) handelt es sich um einen Mikrochip, der grundlegende sicherheitsrelevante Funktionen bereitstellen soll, in erster Linie mit Verschlüsselungsschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="a476c-107">A Trusted Platform Module (TPM) is a microchip that is designed to provide basic security-related functions, primarily involving encryption keys.</span></span> <span data-ttu-id="a476c-108">Das TPM wird normalerweise auf der Hauptplatine eines Computers oder Laptops installiert und kommuniziert mit dem restlichen System mithilfe eines Hardware Busses.</span><span class="sxs-lookup"><span data-stu-id="a476c-108">The TPM is usually installed on the motherboard of a computer or laptop, and communicates with the rest of the system by using a hardware bus.</span></span> <span data-ttu-id="a476c-109">Computer, die ein TPM integrieren, können kryptografische Schlüssel erstellen und verschlüsseln, damit Sie nur vom TPM entschlüsselt werden können.</span><span class="sxs-lookup"><span data-stu-id="a476c-109">Computers that incorporate a TPM have the ability to create cryptographic keys and encrypt them so that they can be decrypted only by the TPM.</span></span>

<span data-ttu-id="a476c-110">Eine TPM-Sperrung kann auftreten, wenn ein Benutzer die falsche PIN zu oft eingibt.</span><span class="sxs-lookup"><span data-stu-id="a476c-110">A TPM lockout can occur if a user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="a476c-111">Gibt an, wie oft ein Benutzer eine falsche PIN eingeben kann, bevor die TPM-Sperren von Hersteller zu Hersteller variieren.</span><span class="sxs-lookup"><span data-stu-id="a476c-111">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span> <span data-ttu-id="a476c-112">Sie können MBAM verwenden, um auf das Datensystem für die zentralisierte Schlüsselwiederherstellung auf der Websiteverwaltung und Überwachung zuzugreifen, auf der Sie eine TPM-Besitzerkennwort-Datei abrufen können, wenn Sie eine Computer-ID und eine zugeordnete Benutzerkennung angeben.</span><span class="sxs-lookup"><span data-stu-id="a476c-112">You can use MBAM to access the centralized Key Recovery data system in the Administration and Monitoring website, where you can retrieve a TPM owner password file when you supply a computer ID and associated user identifier.</span></span>

[<span data-ttu-id="a476c-113">So setzen Sie eine TPM-Sperre zurück</span><span class="sxs-lookup"><span data-stu-id="a476c-113">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-2.md)

## <span data-ttu-id="a476c-114">Wiederherstellen von Laufwerken mit MBAM</span><span class="sxs-lookup"><span data-stu-id="a476c-114">Recover Drives with MBAM</span></span>


<span data-ttu-id="a476c-115">Bei der Verschlüsselung von Daten insbesondere in einer Unternehmensumgebung sollten Sie berücksichtigen, wie diese Daten bei einem Hardwarefehler, personellen Änderungen oder anderen Situationen, in denen Verschlüsselungsschlüssel verloren gehen können, wiederhergestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="a476c-115">When you are dealing with the encryption of data, especially in an enterprise environment, consider how that data can be recovered in the event of a hardware failure, changes in personnel, or other situations in which encryption keys can be lost.</span></span>

<span data-ttu-id="a476c-116">Die verschlüsselten Laufwerk Wiederherstellungsfeatures von MBAM stellen sicher, dass Daten erfasst und gespeichert werden können und dass die erforderlichen Tools für den Zugriff auf ein von BitLocker geschütztes Volume verfügbar sind, wenn BitLocker in den Wiederherstellungsmodus wechselt, verschoben wird oder beschädigt wird.</span><span class="sxs-lookup"><span data-stu-id="a476c-116">The encrypted drive recovery features of MBAM ensure that data can be captured and stored and that the required tools are available to access a BitLocker-protected volume when BitLocker goes into recovery mode, is moved, or becomes corrupted.</span></span>

[<span data-ttu-id="a476c-117">So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her</span><span class="sxs-lookup"><span data-stu-id="a476c-117">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

[<span data-ttu-id="a476c-118">So stellen Sie ein verschobenes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="a476c-118">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-2.md)

[<span data-ttu-id="a476c-119">So stellen Sie ein beschädigtes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="a476c-119">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-2.md)

## <span data-ttu-id="a476c-120">Ermitteln des BitLocker-Verschlüsselungsstatus von verlorenen Computern mithilfe von MBAM</span><span class="sxs-lookup"><span data-stu-id="a476c-120">Determine BitLocker Encryption State of Lost Computers by Using MBAM</span></span>


<span data-ttu-id="a476c-121">Mithilfe von MBAM können Sie den letzten bekannten BitLocker-Verschlüsselungsstatus von verloren gegangenen oder gestohlenen Computern ermitteln.</span><span class="sxs-lookup"><span data-stu-id="a476c-121">Using MBAM, you can determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span>

[<span data-ttu-id="a476c-122">So ermitteln Sie den BitLocker-Verschlüsselungsstatus verloren gegangener Computer</span><span class="sxs-lookup"><span data-stu-id="a476c-122">How to Determine BitLocker Encryption State of Lost Computers</span></span>](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

## <span data-ttu-id="a476c-123">Verwenden des Self-Service-Portals zum wieder Zugriff auf einen Computer</span><span class="sxs-lookup"><span data-stu-id="a476c-123">Use the Self-Service Portal to Regain Access to a Computer</span></span>


<span data-ttu-id="a476c-124">Wenn Endbenutzer von BitLocker von Windows ausgeschlossen werden, können Sie die Anweisungen in diesem Abschnitt verwenden, um einen BitLocker-Wiederherstellungsschlüssel abzurufen, um wieder Zugriff auf Ihren Computer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a476c-124">If end users get locked out of Windows by BitLocker, they can use the instructions in this section to get a BitLocker recovery key to regain access to their computer.</span></span>

[<span data-ttu-id="a476c-125">So verwenden Sie das Self-Service-Portal, um wieder auf einen Computer zugreifen zu können</span><span class="sxs-lookup"><span data-stu-id="a476c-125">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>](how-to-use-the-self-service-portal-to-regain-access-to-a-computer.md)

## <span data-ttu-id="a476c-126">Weitere Ressourcen zum Durchführen der BitLocker-Verwaltung mit MBAM</span><span class="sxs-lookup"><span data-stu-id="a476c-126">Other Resources for Performing BitLocker Management with MBAM</span></span>


[<span data-ttu-id="a476c-127">Vorgänge für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a476c-127">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





