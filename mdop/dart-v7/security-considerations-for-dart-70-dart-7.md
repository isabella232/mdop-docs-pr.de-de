---
title: Sicherheitsüberlegungen zu DaRT 7.0
description: Sicherheitsüberlegungen zu DaRT 7.0
author: dansimp
ms.assetid: 52ad7e6c-c169-4ba4-aa76-56335a585eb8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 739c0319195aeb26e38d55ffe01d14b623de7f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809532"
---
# <span data-ttu-id="3c3c4-103">Sicherheitsüberlegungen zu DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="3c3c4-103">Security Considerations for DaRT 7.0</span></span>


<span data-ttu-id="3c3c4-104">Microsoft Diagnostics and Recovery Toolset (Dart) 7 enthält Funktionen, mit denen ein Administrator die Dart-Tools Remote ausführen kann, um Probleme auf einem Endbenutzercomputer zu beheben.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 includes functionality that lets an administrator run the DaRT tools remotely to resolve problems on an end-user computer.</span></span> <span data-ttu-id="3c3c4-105">In früheren Versionen von DART musste sich ein Helpdesk-Techniker oder Administrator physisch auf einem Endbenutzercomputer befinden und mit der CD oder DVD, die das DART-Wiederherstellungsbild enthielt, in DART Booten.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-105">In earlier releases of DaRT, a help desk technician or administrator had to physically be at an end-user computer and boot into DaRT by using the CD or DVD that included the DaRT recovery image.</span></span> <span data-ttu-id="3c3c4-106">Nun kann der Helpdesk-Techniker oder Administrator die gleichen Verfahren Remote durchführen.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-106">Now, the help desk technician or administrator can perform the same procedures remotely.</span></span>

<span data-ttu-id="3c3c4-107">Darüber hinaus können Sie in DaRT7 neben dem Brennen einer CD oder DVD nun auch das Image der internationalen Organisation für Standardisierung (ISO) auf einem USB-Stick speichern.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-107">Also in DaRT7, in addition to burning a CD or DVD, you are now able to save the International Organization for Standardization (ISO) image to a USB flash drive.</span></span> <span data-ttu-id="3c3c4-108">Sie können das ISO-Abbild auch in einem Netzwerk speichern oder seinen Inhalt als Wiederherstellungspartition auf einer Festplatte des Computers einfügen.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-108">You can also put the ISO image on a network or include its contents as a recovery partition on a computer hard disk.</span></span>

<span data-ttu-id="3c3c4-109">Mit der Funktion **Remote Verbindung** in DaRT7 können Endbenutzer auf DART zugreifen, indem Sie eine der folgenden neuen Bereitstellungsmethoden verwenden.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-109">The **Remote Connection** feature in DaRT7 lets end users access DaRT by using one of these new deployment methods.</span></span> <span data-ttu-id="3c3c4-110">Daher können Sie Dart einfacher starten und auf die Dart-Tools zugreifen.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-110">Therefore, they can more easily start DaRT and access the DaRT tools.</span></span>

<span data-ttu-id="3c3c4-111">Die neuen Funktionen in DaRT7 bieten viel mehr Flexibilität bei der Verwendung von Dart in Ihrem Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-111">The new functionalities in DaRT7 provide much more flexibility in how you use DaRT in your enterprise.</span></span> <span data-ttu-id="3c3c4-112">Sie erstellen jedoch auch einen eigenen Satz von Sicherheitsproblemen, die behoben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-112">However, they also create their own set of security issues that must be addressed.</span></span> <span data-ttu-id="3c3c4-113">Wir empfehlen, beim Konfigurieren von DART die folgenden Sicherheitstipps zu bedenken.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-113">We recommend that you consider the following security tips when you configure DaRT.</span></span>

## <span data-ttu-id="3c3c4-114">So gewährleisten Sie die Sicherheit beim Erstellen des DART-Wiederherstellungs Bilds</span><span class="sxs-lookup"><span data-stu-id="3c3c4-114">To help maintain security when you create the DaRT recovery image</span></span>


<span data-ttu-id="3c3c4-115">Wenn Sie das DART-Wiederherstellungsbild erstellen, können Sie die Tools auswählen, die Sie einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-115">When you are creating the DaRT recovery image, you can select the tools that you want to include.</span></span> <span data-ttu-id="3c3c4-116">Aus Sicherheitsgründen ist es möglicherweise sinnvoll, den Endbenutzer Zugriff auf die leistungsstärkeren Dart-Tools wie Datenträger Zurücksetzung und Schlosser zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-116">For security reasons, you might want to restrict end-user access to the more powerful DaRT tools, such as Disk Wipe and Locksmith.</span></span> <span data-ttu-id="3c3c4-117">In DaRT7 können Sie bestimmte Tools während der Konfiguration deaktivieren und diese weiterhin für Helpdesk-Agents verfügbar machen, wenn der Endbenutzer das Remote Verbindungs Feature startet.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-117">In DaRT7, you can disable certain tools during configuration and still make them available to helpdesk agents when the end user starts the Remote Connection feature.</span></span>

<span data-ttu-id="3c3c4-118">Sie können das DART-Bild sogar so konfigurieren, dass die Option zum Starten einer Remote Verbindungssitzung das einzige Tool ist, das einem Endbenutzer zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-118">You can even configure the DaRT image so that the option to start a remote connection session is the only tool available to an end user.</span></span>

<span data-ttu-id="3c3c4-119">**Wichtig**  Nachdem die Remoteverbindung hergestellt wurde, werden alle Tools, die Sie in das Wiederherstellungsabbild aufgenommen haben, einschließlich der für den Endbenutzer nicht verfügbaren Tools, dem Helpdesk-Mitarbeiter zur Verfügung stehen, der auf dem Endbenutzercomputer arbeitet.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-119">**Important** After the remote connection is established, all the tools that you included in the recovery image, including those unavailable to the end user, will become available to the helpdesk agent working on the end–user computer.</span></span>

 

<span data-ttu-id="3c3c4-120">Weitere Informationen zum Einschließen von Tools in das DART-Wiederherstellungsabbild finden Sie unter [Verwenden des DART-Wiederherstellungsbild-Assistenten zum Erstellen des Wiederherstellungs](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md)Abbilds.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-120">For more information about including tools in the DaRT recovery image, see [How to Use the DaRT Recovery Image Wizard to Create the Recovery Image](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md).</span></span>

## <span data-ttu-id="3c3c4-121">So gewährleisten Sie die Sicherheit durch Verschlüsseln des DART-Wiederherstellungs Bilds</span><span class="sxs-lookup"><span data-stu-id="3c3c4-121">To help maintain security by encrypting the DaRT recovery image</span></span>


<span data-ttu-id="3c3c4-122">Wenn Sie eine der in DaRT7 neuen Bereitstellungsoptionen verwenden, beispielsweise das Speichern auf einem USB-Flashlaufwerk oder das Erstellen einer Remotepartition oder einer Wiederherstellungspartition, können Sie die bevorzugte Methode für die Laufwerkverschlüsselung Ihres Unternehmens auf der ISO-Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-122">If you use one of the deployment options new in DaRT7, for example, saving to a USB flash drive or creating a remote partition or a recovery partition, you can include your company’s preferred method of drive encryption on the ISO.</span></span> <span data-ttu-id="3c3c4-123">Dadurch wird sichergestellt, dass ein Endbenutzer die Funktionalität von DART nicht verwenden kann, wenn er Zugriff auf das Wiederherstellungsabbild erhält.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-123">This will help make sure that an end user cannot use the functionality of DaRT should they gain access to the recovery image.</span></span> <span data-ttu-id="3c3c4-124">Außerdem wird sichergestellt, dass nicht autorisierte Benutzer in DART auf Computern booten können, die einer anderen Person gehören.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-124">And it will also make sure that unauthorized users cannot boot into DaRT on computers that belong to someone else.</span></span>

<span data-ttu-id="3c3c4-125">Ihre Verschlüsselungsmethode sollte auf allen Computern bereitgestellt und aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-125">Your encryption method should be deployed and enabled in all computers.</span></span>

<span data-ttu-id="3c3c4-126">**Hinweis**  DaRT7 unterstützt BitLocker nativ.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-126">**Note** DaRT7 supports BitLocker natively.</span></span>

 

## <span data-ttu-id="3c3c4-127">So gewährleisten Sie die Sicherheit zwischen zwei Computern während der Remote Verbindung</span><span class="sxs-lookup"><span data-stu-id="3c3c4-127">To help maintain security between two computers during Remote Connection</span></span>


<span data-ttu-id="3c3c4-128">Standardmäßig ist die Kommunikation zwischen zwei Computern, die eine **Remote Verbindungs** Sitzung eingerichtet haben, möglicherweise nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-128">By default, the communication between two computers that have established a **Remote Connection** session may not be encrypted.</span></span> <span data-ttu-id="3c3c4-129">Um die Sicherheit zwischen den beiden Computern zu gewährleisten, empfehlen wir daher, dass beide Computer Teil desselben Netzwerks sind.</span><span class="sxs-lookup"><span data-stu-id="3c3c4-129">Therefore, to help maintain security between the two computers, we recommend that both computers are a part of the same network.</span></span>

## <span data-ttu-id="3c3c4-130">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3c3c4-130">Related topics</span></span>


[<span data-ttu-id="3c3c4-131">Vorgänge für DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="3c3c4-131">Operations for DaRT 7.0</span></span>](operations-for-dart-70-new-ia.md)

 

 





