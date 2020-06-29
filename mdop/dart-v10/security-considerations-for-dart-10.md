---
title: Sicherheitsüberlegungen zu DaRT 10
description: Sicherheitsüberlegungen zu DaRT 10
author: dansimp
ms.assetid: c653daf1-f12a-4667-98cc-f0c89fa38e3f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f10ecf81021d41fbc08b288573c05a8d64c47d7c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809724"
---
# <span data-ttu-id="92f94-103">Sicherheitsüberlegungen zu DaRT 10</span><span class="sxs-lookup"><span data-stu-id="92f94-103">Security Considerations for DaRT 10</span></span>


<span data-ttu-id="92f94-104">Dieses Thema enthält eine kurze Übersicht über die Konten und Gruppen, Protokolldateien und andere sicherheitsrelevante Überlegungen für Microsoft Diagnostics and Recovery Toolset (Dart) 10.</span><span class="sxs-lookup"><span data-stu-id="92f94-104">This topic contains a brief overview about the accounts and groups, log files, and other security-related considerations for Microsoft Diagnostics and Recovery Toolset (DaRT) 10.</span></span> <span data-ttu-id="92f94-105">Weitere Informationen finden Sie unter den Links in diesem Artikel.</span><span class="sxs-lookup"><span data-stu-id="92f94-105">For more information, follow the links within this article.</span></span>

## <span data-ttu-id="92f94-106">Allgemeine Sicherheitsüberlegungen</span><span class="sxs-lookup"><span data-stu-id="92f94-106">General security considerations</span></span>


<span data-ttu-id="92f94-107">Grund **Legendes zu den Sicherheitsrisiken**</span><span class="sxs-lookup"><span data-stu-id="92f94-107">**Understand the security risks**.</span></span> <span data-ttu-id="92f94-108">Dart 10 enthält Funktionen, mit denen ein Administrator oder ein Helpdesk-Mitarbeiter die Dart-Tools Remote ausführen kann, um Probleme auf einem Endbenutzercomputer zu beheben.</span><span class="sxs-lookup"><span data-stu-id="92f94-108">DaRT 10 includes functionality that lets an administrator or a help desk worker run the DaRT tools remotely to resolve problems on an end-user computer.</span></span> <span data-ttu-id="92f94-109">Darüber hinaus können Sie das Image der internationalen Organisation für Standardisierung (ISO) auf einem USB-Flashlaufwerk speichern oder das ISO-Abbild in ein Netzwerk setzen, um dessen Inhalt als Wiederherstellungspartition auf der Festplatte eines Computers einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="92f94-109">In addition, you can save the International Organization for Standardization (ISO) image to a USB flash drive or put the ISO image on a network to include its contents as a recovery partition on a computer’s hard disk.</span></span> <span data-ttu-id="92f94-110">Diese Funktionen bieten Flexibilität, aber auch potenzielle Sicherheitsrisiken, die bei der Konfiguration von DART berücksichtigt werden sollten.</span><span class="sxs-lookup"><span data-stu-id="92f94-110">These capabilities provide flexibility, but also create potential security risks that you should consider when configuring DaRT.</span></span>

<span data-ttu-id="92f94-111">**Physisches sichern ihrer Computer**.</span><span class="sxs-lookup"><span data-stu-id="92f94-111">**Physically secure your computers**.</span></span> <span data-ttu-id="92f94-112">Wenn Administratoren und Helpdesk-Mitarbeiter nicht physisch an ihren Computern sind, sollten Sie Ihre Computer sperren und einen sicheren Bildschirmschoner verwenden.</span><span class="sxs-lookup"><span data-stu-id="92f94-112">When administrators and help desk workers are not physically at their computers, they should lock their computers and use a secured screen saver.</span></span>

<span data-ttu-id="92f94-113">**Wenden Sie die neuesten Sicherheitsupdates auf alle Computer an**.</span><span class="sxs-lookup"><span data-stu-id="92f94-113">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="92f94-114">Bleiben Sie über neue Updates für Betriebssysteme auf dem laufenden, indem Sie den Security Notification Service ( <https://go.microsoft.com/fwlink/?LinkId=28819> ) abonnieren.</span><span class="sxs-lookup"><span data-stu-id="92f94-114">Stay informed about new updates for operating systems by subscribing to the Security Notification service (<https://go.microsoft.com/fwlink/?LinkId=28819>).</span></span>

## <span data-ttu-id="92f94-115">Einschränken des Endbenutzerzugriffs auf DART-Tools</span><span class="sxs-lookup"><span data-stu-id="92f94-115">Limit end-user access to DaRT tools</span></span>


<span data-ttu-id="92f94-116">Wenn Sie das DART-Wiederherstellungsbild erstellen, können Sie die Tools auswählen, die Sie einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="92f94-116">When you are creating the DaRT recovery image, you can select the tools that you want to include.</span></span> <span data-ttu-id="92f94-117">Aus Sicherheitsgründen ist es möglicherweise sinnvoll, den Endbenutzer Zugriff auf die leistungsstärkeren Dart-Tools wie Datenträger Zurücksetzung und Schlosser zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="92f94-117">For security reasons, you might want to restrict end-user access to the more powerful DaRT tools, such as Disk Wipe and Locksmith.</span></span> <span data-ttu-id="92f94-118">In DART 10 können Sie bestimmte Tools während der Konfiguration deaktivieren und diese weiterhin den Helpdesk-Mitarbeitern zur Verfügung stellen, wenn der Endbenutzer das Remote Verbindungs Feature startet.</span><span class="sxs-lookup"><span data-stu-id="92f94-118">In DaRT 10, you can disable certain tools during configuration and still make them available to help desk workers when the end user starts the Remote Connection feature.</span></span>

<span data-ttu-id="92f94-119">Sie können das DART-Bild sogar so konfigurieren, dass die Option zum Starten einer Remote Verbindungssitzung das einzige Tool ist, das einem Endbenutzer zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="92f94-119">You can even configure the DaRT image so that the option to start a remote connection session is the only tool available to an end user.</span></span>

<span data-ttu-id="92f94-120">**Wichtig**  Nachdem die Remoteverbindung hergestellt wurde, werden alle Tools, die Sie in das Wiederherstellungsabbild aufgenommen haben, einschließlich der für den Endbenutzer nicht verfügbaren Tools, für alle Helpdesk-Mitarbeiter zur Verfügung gestellt, die am Endbenutzercomputer arbeiten.</span><span class="sxs-lookup"><span data-stu-id="92f94-120">**Important** After the remote connection is established, all the tools that you included in the recovery image, including those unavailable to the end user, will become available to any help desk worker who is working on the end–user computer.</span></span>

 

<span data-ttu-id="92f94-121">Weitere Informationen zum Einbeziehen von Tools in das DART-Wiederherstellungsbild finden Sie unter [Übersicht über die Tools in DART 10](overview-of-the-tools-in-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="92f94-121">For more information about including tools in the DaRT recovery image, see [Overview of the Tools in DaRT 10](overview-of-the-tools-in-dart-10.md).</span></span>

## <span data-ttu-id="92f94-122">Sichern des DART-Wiederherstellungs Bilds</span><span class="sxs-lookup"><span data-stu-id="92f94-122">Secure the DaRT recovery image</span></span>


<span data-ttu-id="92f94-123">Wenn Sie das DART-Wiederherstellungsabbild bereitstellen, indem Sie es auf einem USB-Stick oder durch Erstellen einer Remotepartition oder einer Wiederherstellungspartition speichern, möchten Sie möglicherweise die bevorzugte Methode für die Laufwerkverschlüsselung Ihres Unternehmens auf der ISO-Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="92f94-123">If you deploy the DaRT recovery image by saving it to a USB flash drive or by creating a remote partition or a recovery partition, you might want to include your company’s preferred method of drive encryption on the ISO.</span></span> <span data-ttu-id="92f94-124">Das Verschlüsseln der ISO-Datei hilft, sicherzustellen, dass Endbenutzer DART-Funktionen nicht verwenden können, wenn Sie Zugriff auf das Wiederherstellungsabbild erhalten, und es wird sichergestellt, dass nicht autorisierte Benutzer in DART auf Computern booten können, die einer anderen Person angehören.</span><span class="sxs-lookup"><span data-stu-id="92f94-124">Encrypting the ISO helps to ensure that end users cannot use DaRT functionality if they were to gain access to the recovery image, and it ensures that unauthorized users cannot boot into DaRT on computers that belong to someone else.</span></span> <span data-ttu-id="92f94-125">Wenn Sie eine Verschlüsselungsmethode verwenden, stellen Sie sicher, dass Sie auf allen Computern bereitgestellt und aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="92f94-125">If you use an encryption method, be sure to deploy and enable it in all computers.</span></span>

<span data-ttu-id="92f94-126">**Hinweis**  Dart 10 unterstützt BitLocker nativ.</span><span class="sxs-lookup"><span data-stu-id="92f94-126">**Note** DaRT 10 supports BitLocker natively.</span></span>

 

<span data-ttu-id="92f94-127">Wenn Sie die Laufwerkverschlüsselung einbeziehen möchten, fügen Sie die Verschlüsselungs Projektmappendateien hinzu, wenn Sie das Wiederherstellungsabbild erstellen.</span><span class="sxs-lookup"><span data-stu-id="92f94-127">To include drive encryption, add the encryption solution files when you create the recovery image.</span></span> <span data-ttu-id="92f94-128">Ihre Verschlüsselungslösung muss auf WinPE ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="92f94-128">Your encryption solution must be able to run on WinPE.</span></span> <span data-ttu-id="92f94-129">Endbenutzer, die von der ISO-Datei booten, können dann auf diese Verschlüsselungslösung zugreifen und das Laufwerk freigeben.</span><span class="sxs-lookup"><span data-stu-id="92f94-129">End users who boot from the ISO are then able to access that encryption solution and unblock the drive.</span></span>

## <span data-ttu-id="92f94-130">Verwalten der Sicherheit zwischen zwei Computern, wenn Sie eine Remote Verbindung verwenden</span><span class="sxs-lookup"><span data-stu-id="92f94-130">Maintain security between two computers when you use Remote Connection</span></span>


<span data-ttu-id="92f94-131">Standardmäßig ist die Kommunikation zwischen zwei Computern, die eine **Remote Verbindungs** Sitzung eingerichtet haben, möglicherweise nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="92f94-131">By default, the communication between two computers that have established a **Remote Connection** session may not be encrypted.</span></span> <span data-ttu-id="92f94-132">Um die Sicherheit zwischen den beiden Computern zu gewährleisten, empfehlen wir daher, dass beide Computer Teil desselben Netzwerks sind.</span><span class="sxs-lookup"><span data-stu-id="92f94-132">Therefore, to help maintain security between the two computers, we recommend that both computers are a part of the same network.</span></span>

## <span data-ttu-id="92f94-133">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="92f94-133">Related topics</span></span>


[<span data-ttu-id="92f94-134">Sicherheit und Datenschutz für DaRT 10</span><span class="sxs-lookup"><span data-stu-id="92f94-134">Security and Privacy for DaRT 10</span></span>](security-and-privacy-for-dart-10.md)

 

 





