---
title: Durchführen der BitLocker-Verwaltung mit MBAM 2.5
description: Durchführen der BitLocker-Verwaltung mit MBAM 2.5
author: dansimp
ms.assetid: 068f3ee0-300c-4083-ba18-7065eef997ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a0ee5802f945176914c56659e0ff7e34e93a969
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811497"
---
# <span data-ttu-id="c464e-103">Durchführen der BitLocker-Verwaltung mit MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c464e-103">Performing BitLocker Management with MBAM 2.5</span></span>


<span data-ttu-id="c464e-104">Nachdem Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) geplant und dann bereitgestellt haben, können Sie Sie konfigurieren und verwenden, um die BitLocker-Laufwerkverschlüsselung in Ihrem Unternehmen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="c464e-104">After planning and then deploying Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use it to manage BitLocker Drive Encryption across your enterprise.</span></span> <span data-ttu-id="c464e-105">Die Informationen in diesem Abschnitt beschreiben die nach der Installation täglichen BitLocker-Verschlüsselungs Verwaltungsaufgaben, die mithilfe der Microsoft BitLocker-Verwaltung und-Überwachung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c464e-105">The information in this section describes post-installation, day-to-day BitLocker encryption management tasks that are accomplished by using Microsoft BitLocker Administration and Monitoring.</span></span>

## <span data-ttu-id="c464e-106">Zurücksetzen einer TPM-Sperrung</span><span class="sxs-lookup"><span data-stu-id="c464e-106">Reset a TPM lockout</span></span>


<span data-ttu-id="c464e-107">Bei einem Trusted Platform Module (TPM) handelt es sich um einen Mikrochip, der grundlegende sicherheitsrelevante Funktionen bereitstellen soll, in erster Linie mit Verschlüsselungsschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="c464e-107">A Trusted Platform Module (TPM) is a microchip that is designed to provide basic security-related functions, primarily involving encryption keys.</span></span> <span data-ttu-id="c464e-108">Das TPM wird normalerweise auf der Hauptplatine eines Computers installiert, und es kommuniziert mit dem restlichen System mithilfe eines Host-Bus-Adapters.</span><span class="sxs-lookup"><span data-stu-id="c464e-108">The TPM is usually installed on the motherboard of a computer, and it communicates with the rest of the system by using a host bus adapter.</span></span> <span data-ttu-id="c464e-109">Auf Computern, auf denen ein TPM integriert ist, können Sie kryptografische Schlüssel erstellen und verschlüsseln, sodass Sie nur vom TPM entschlüsselt werden können.</span><span class="sxs-lookup"><span data-stu-id="c464e-109">On computers that incorporate a TPM, you can create cryptographic keys and encrypt them so that they can be decrypted only by the TPM.</span></span>

<span data-ttu-id="c464e-110">Eine TPM-Sperrung kann auftreten, wenn ein Benutzer die falsche PIN zu oft eingibt.</span><span class="sxs-lookup"><span data-stu-id="c464e-110">A TPM lockout can occur if a user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="c464e-111">Gibt an, wie oft ein Benutzer eine falsche PIN eingeben kann, bevor die TPM-Sperren je nach Hersteller variieren.</span><span class="sxs-lookup"><span data-stu-id="c464e-111">The number of times that a user can enter an incorrect PIN before the TPM locks varies by manufacturer.</span></span> <span data-ttu-id="c464e-112">Sie können MBAM verwenden, um auf der Website Verwaltung und Überwachung auf das Datensystem für die zentrale Schlüsselwiederherstellung zuzugreifen, in dem Sie eine TPM-Besitzerkennwort-Datei abrufen können, wenn Sie eine Computer-ID und eine zugeordnete Benutzerkennung angeben.</span><span class="sxs-lookup"><span data-stu-id="c464e-112">You can use MBAM to access the centralized key recovery data system on the Administration and Monitoring Website, where you can retrieve a TPM owner password file when you supply a computer ID and an associated user identifier.</span></span>

[<span data-ttu-id="c464e-113">So setzen Sie eine TPM-Sperre zurück</span><span class="sxs-lookup"><span data-stu-id="c464e-113">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-25.md)

## <span data-ttu-id="c464e-114">Wiederherstellen von Laufwerken</span><span class="sxs-lookup"><span data-stu-id="c464e-114">Recover drives</span></span>


<span data-ttu-id="c464e-115">Bei der Verschlüsselung von Daten insbesondere in einer Unternehmensumgebung sollten Sie berücksichtigen, wie diese Daten bei einem Hardwarefehler, personellen Änderungen oder anderen Situationen, in denen Verschlüsselungsschlüssel verloren gehen können, wiederhergestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="c464e-115">When you are dealing with the encryption of data, especially in an enterprise environment, consider how that data can be recovered in the event of a hardware failure, changes in personnel, or other situations in which encryption keys can be lost.</span></span>

<span data-ttu-id="c464e-116">Die verschlüsselten Laufwerk Wiederherstellungsfeatures in MBAM stellen sicher, dass Daten erfasst und gespeichert werden können und dass die erforderlichen Tools für den Zugriff auf ein von BitLocker geschütztes Volume verfügbar sind, wenn BitLocker in den Wiederherstellungsmodus wechselt, verschoben wird oder beschädigt wird.</span><span class="sxs-lookup"><span data-stu-id="c464e-116">The encrypted drive recovery features in MBAM ensure that data can be captured and stored and that the required tools are available to access a BitLocker-protected volume when BitLocker goes into recovery mode, is moved, or becomes corrupted.</span></span>

[<span data-ttu-id="c464e-117">So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her</span><span class="sxs-lookup"><span data-stu-id="c464e-117">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)

[<span data-ttu-id="c464e-118">So stellen Sie ein verschobenes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="c464e-118">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-25.md)

[<span data-ttu-id="c464e-119">So stellen Sie ein beschädigtes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="c464e-119">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-25.md)

## <span data-ttu-id="c464e-120">Ermitteln des BitLocker-Verschlüsselungsstatus von verlorenen Computern</span><span class="sxs-lookup"><span data-stu-id="c464e-120">Determine BitLocker encryption state of lost computers</span></span>


<span data-ttu-id="c464e-121">Mithilfe von MBAM können Sie den letzten bekannten BitLocker-Verschlüsselungsstatus von verloren gegangenen oder gestohlenen Computern ermitteln.</span><span class="sxs-lookup"><span data-stu-id="c464e-121">By using MBAM, you can determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span>

[<span data-ttu-id="c464e-122">So ermitteln Sie den BitLocker-Verschlüsselungsstatus verloren gegangener Computer</span><span class="sxs-lookup"><span data-stu-id="c464e-122">How to Determine BitLocker Encryption State of Lost Computers</span></span>](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)

## <span data-ttu-id="c464e-123">Verwenden des Self-Service-Portals zum wieder Zugriff auf einen Computer</span><span class="sxs-lookup"><span data-stu-id="c464e-123">Use the Self-Service Portal to regain access to a computer</span></span>


<span data-ttu-id="c464e-124">Wenn Endbenutzer von BitLocker von Windows ausgeschlossen werden, können Sie die Anweisungen in diesem Abschnitt verwenden, um einen BitLocker-Wiederherstellungsschlüssel abzurufen, um wieder Zugriff auf Ihren Computer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c464e-124">If end users get locked out of Windows by BitLocker, they can use the instructions in this section to get a BitLocker recovery key to regain access to their computer.</span></span>

[<span data-ttu-id="c464e-125">So verwenden Sie das Self-Service-Portal, um wieder auf einen Computer zugreifen zu können</span><span class="sxs-lookup"><span data-stu-id="c464e-125">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>](how-to-use-the-self-service-portal-to-regain-access-to-a-computer-mbam-25.md)



## <span data-ttu-id="c464e-126">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c464e-126">Related topics</span></span>


[<span data-ttu-id="c464e-127">Vorgänge für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c464e-127">Operations for MBAM 2.5</span></span>](operations-for-mbam-25.md)

 

## <span data-ttu-id="c464e-128">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="c464e-128">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="c464e-129">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="c464e-129">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="c464e-130">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="c464e-130">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





