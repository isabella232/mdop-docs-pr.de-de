---
title: Planen der Speicherung und Bereitstellung des DaRT 8.0-Wiederherstellungsabbilds
description: Planen der Speicherung und Bereitstellung des DaRT 8.0-Wiederherstellungsabbilds
author: dansimp
ms.assetid: 939fbe17-0e30-4c85-8782-5b84d69442a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2e5cca90c644eb3edf233564c474d2601d4227fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808638"
---
# <span data-ttu-id="293bf-103">Planen der Speicherung und Bereitstellung des DaRT 8.0-Wiederherstellungsabbilds</span><span class="sxs-lookup"><span data-stu-id="293bf-103">Planning How to Save and Deploy the DaRT 8.0 Recovery Image</span></span>


<span data-ttu-id="293bf-104">Sie können das Microsoft Diagnostics and Recovery Toolset (Dart) 8,0-Wiederherstellungsabbild mithilfe der folgenden Methoden speichern und bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="293bf-104">You can save and deploy the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 recovery image by using the following methods.</span></span> <span data-ttu-id="293bf-105">Berücksichtigen Sie die vor-und Nachteile der einzelnen Methoden, wenn Sie die Methode ermitteln, die Sie verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="293bf-105">When you are determining the method that you will use, consider the advantages and disadvantages of each.</span></span> <span data-ttu-id="293bf-106">Berücksichtigen Sie auch Ihre Infrastruktur-und Supportmitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="293bf-106">You should also consider your infrastructure and support staff.</span></span> <span data-ttu-id="293bf-107">Wenn Sie über eine kleine Infrastruktur verfügen, möchten Sie möglicherweise Dart 8,0 mithilfe von Wechselmedien bereitstellen, da das Wiederherstellungsabbild immer verfügbar ist, wenn Sie es auf der lokalen Festplatte installieren.</span><span class="sxs-lookup"><span data-stu-id="293bf-107">If you have a small infrastructure, you might want to deploy DaRT 8.0 by using removable media, since the recovery image will always be available if you install it to the local hard drive.</span></span>

<span data-ttu-id="293bf-108">Wenn Ihre Organisation Active Directory-Domänendienste (AD DS) verwendet, möchten Sie möglicherweise Wiederherstellungs Bilder mithilfe von Windows DS als Netzwerkdienst bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="293bf-108">If your organization uses Active Directory Domain Services (AD DS), you may want to deploy recovery images as a network service by using Windows DS.</span></span> <span data-ttu-id="293bf-109">Wiederherstellungs Bilder sind immer für jeden angeschlossenen Computer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="293bf-109">Recovery images are always available to any connected computer.</span></span> <span data-ttu-id="293bf-110">Sie können mehrere Bilder aus Windows DS bereitstellen und alle an einem zentralen Ort verwalten.</span><span class="sxs-lookup"><span data-stu-id="293bf-110">You can deploy multiple images from Windows DS and maintain them all in one place.</span></span>

<span data-ttu-id="293bf-111">**Hinweis**  Möglicherweise möchten Sie in Ihrer Organisation mehr als eine Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="293bf-111">**Note** You may want to use more than one method in your organization.</span></span> <span data-ttu-id="293bf-112">So können Sie beispielsweise für die meisten Situationen in DART von einer Remotepartition Booten und einen USB-Stick zur Verfügung stellen, falls der Endbenutzercomputer keine Verbindung mit dem Netzwerk herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="293bf-112">For example, you can boot into DaRT from a remote partition for most situations and have a USB flash drive available in case the end-user computer cannot connect to the network.</span></span>

 

<span data-ttu-id="293bf-113">Die folgende Tabelle zeigt einige vor-und Nachteile der einzelnen Methoden der Verwendung von Dart in Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="293bf-113">The following table shows some advantages and disadvantages of each method of using DaRT in your organization.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="293bf-114">Methode zum Booten in DART</span><span class="sxs-lookup"><span data-stu-id="293bf-114">Method to Boot into DaRT</span></span></th>
<th align="left"><span data-ttu-id="293bf-115">Vorteile</span><span class="sxs-lookup"><span data-stu-id="293bf-115">Advantages</span></span></th>
<th align="left"><span data-ttu-id="293bf-116">Nachteile</span><span class="sxs-lookup"><span data-stu-id="293bf-116">Disadvantages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="293bf-117">Wechselmedien</span><span class="sxs-lookup"><span data-stu-id="293bf-117">Removable Media</span></span></strong></p>
<p><span data-ttu-id="293bf-118">Das Wiederherstellungsabbild wird auf eine CD, DVD oder ein USB-Laufwerk geschrieben, damit das Supportpersonal die Wiederherstellungstools auf dem unstable-Computer nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="293bf-118">The recovery image is written to a CD, DVD, or USB drive to enable support staff to take the recovery tools with them to the unstable computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="293bf-119">Unterstützt Szenarien, in denen der Master Boot Record (MBR) beschädigt ist und Sie nicht auf die Festplatte zugreifen können, und unterstützt Fälle, in denen keine Netzwerkverbindung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="293bf-119">Supports scenarios in which the master boot record (MBR) is corrupted and you cannot access the hard disk and supports cases in which there is no network connection.</span></span></p>
<p><span data-ttu-id="293bf-120">Ermöglicht Ihnen das Erstellen mehrerer Wiederherstellungs Bilder mit verschiedenen Tools, um unterschiedliche Supportstufen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="293bf-120">Enables you to create multiple recovery images with different tools to provide different levels of support.</span></span></p>
<p><span data-ttu-id="293bf-121">Bietet ein integriertes Tool zum Brennen von Wiederherstellungs Bildern auf Wechselmedien.</span><span class="sxs-lookup"><span data-stu-id="293bf-121">Provides a built-in tool for burning recovery images to removable media.</span></span></p></td>
<td align="left"><p><span data-ttu-id="293bf-122">Erfordert, dass die Supportmitarbeiter physisch am Endbenutzercomputer sind, um in DART zu booten.</span><span class="sxs-lookup"><span data-stu-id="293bf-122">Requires that support staff are physically at the end-user computer to boot into DaRT.</span></span></p>
<p><span data-ttu-id="293bf-123">Erfordert Zeit und Wartung, um mehrere Medien mit unterschiedlichen Konfigurationen für 32-Bit-und 64-Bit-Computer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="293bf-123">Requires time and maintenance to create multiple media with different configurations for 32-bit and 64-bit computers.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="293bf-124">Von einer Remote-(Netzwerk-) Partition</span><span class="sxs-lookup"><span data-stu-id="293bf-124">From a remote (network) partition</span></span></strong></p>
<p><span data-ttu-id="293bf-125">Das Wiederherstellungsabbild wird auf einem Netzwerkstart Server wie Windows-Bereitstellungsdienste (Windows Deployment Services, Windows DS) gehostet, mit dem Benutzer oder Mitarbeiter des Supports Sie bei Bedarf auf Computer streamen können.</span><span class="sxs-lookup"><span data-stu-id="293bf-125">The recovery image is hosted on a network boot server like Windows Deployment Services (Windows DS), which allows users or support staff to stream it to computers on demand.</span></span></p></td>
<td align="left"><p><span data-ttu-id="293bf-126">Für alle Computer verfügbar, die Zugriff auf den Netzwerk Boot Server haben.</span><span class="sxs-lookup"><span data-stu-id="293bf-126">Available to all computers that have access to the network boot server.</span></span></p>
<p><span data-ttu-id="293bf-127">Wiederherstellungs Bilder werden auf einem zentralen Server gehostet, der zentralisierte Updates ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="293bf-127">Recovery images are hosted on a central server, which enables centralized updates.</span></span></p>
<p><span data-ttu-id="293bf-128">Zentralisierte Helpdesk-Mitarbeiter können Reparaturen mithilfe der Remotekonnektivität bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="293bf-128">Centralized help desk staff can provide repairs by using remote connectivity.</span></span></p>
<p><span data-ttu-id="293bf-129">Kein lokaler Speicherbedarf für die Clients.</span><span class="sxs-lookup"><span data-stu-id="293bf-129">No local storage requirement on the clients.</span></span></p>
<p><span data-ttu-id="293bf-130">Möglichkeit zum Erstellen mehrerer Wiederherstellungs Bilder mit unterschiedlichen Tools für bestimmte Supportebenen.</span><span class="sxs-lookup"><span data-stu-id="293bf-130">Ability to create multiple recovery images with different tools for specific support levels.</span></span></p></td>
<td align="left"><p><span data-ttu-id="293bf-131">Die Notwendigkeit, die Windows DS-Infrastruktur zu sichern, um sicherzustellen, dass reguläre Benutzer nur das DART-Wiederherstellungsabbild und nicht den vollständigen Betriebssystem-Bilderstellungs Prozess starten können.</span><span class="sxs-lookup"><span data-stu-id="293bf-131">The need to secure Windows DS infrastructure to ensure that regular users can start only the DaRT recovery image and not the full operating system imaging process.</span></span></p>
<p></p>
<p></p>
<p><span data-ttu-id="293bf-132">Erfordert, dass der Endbenutzercomputer zur Laufzeit mit dem Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="293bf-132">Requires that the end-user computer is connected to the network at runtime.</span></span></p>
<p><span data-ttu-id="293bf-133">Erfordert, dass das Wiederherstellungsabbild über das Netzwerk gebracht wird.</span><span class="sxs-lookup"><span data-stu-id="293bf-133">Requires that the recovery image is brought across the network.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="293bf-134">Von einer Wiederherstellungspartition auf der lokalen Festplatte</span><span class="sxs-lookup"><span data-stu-id="293bf-134">From a recovery partition on the local hard drive</span></span></strong></p>
<p><span data-ttu-id="293bf-135">Das Wiederherstellungsabbild wird entweder manuell oder mithilfe elektronischer Softwareverteilungssysteme wie System Center Configuration Manager auf einer lokalen Festplatte installiert.</span><span class="sxs-lookup"><span data-stu-id="293bf-135">The recovery image is installed on a local hard drive either manually or by using electronic software distribution systems like System Center Configuration Manager.</span></span></p></td>
<td align="left"><p><span data-ttu-id="293bf-136">Das Wiederherstellungsabbild steht immer zur Verfügung, da es auf dem Computer vorab bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="293bf-136">The recovery image is always available because it is pre-staged on the computer.</span></span></p>
<p><span data-ttu-id="293bf-137">Zentralisierte Helpdesk-Mitarbeiter können mithilfe der Remote Verbindung Support bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="293bf-137">Centralized help desk staff can provide support by using Remote Connection.</span></span></p>
<p><span data-ttu-id="293bf-138">Das Wiederherstellungsabbild wird zentral verwaltet und bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="293bf-138">The recovery image is centrally managed and deployed.</span></span></p>
<p><span data-ttu-id="293bf-139">Weitere Wiederherstellungsschlüssel Anforderungen auf Computern, die durch die Windows BitLocker-Laufwerkverschlüsselung geschützt sind, werden eliminiert.</span><span class="sxs-lookup"><span data-stu-id="293bf-139">Additional recovery key requests on computers that are protected by Windows BitLocker drive encryption are eliminated.</span></span></p></td>
<td align="left"><p><span data-ttu-id="293bf-140">Lokaler Speicher ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="293bf-140">Local storage is required.</span></span></p>
<p><span data-ttu-id="293bf-141">Es wird empfohlen, eine dedizierte, unverschlüsselte Partition für die Bildplatzierung zur Wiederherstellung zu finden, um das Risiko einer fehlgeschlagenen Startpartition zu verringern.</span><span class="sxs-lookup"><span data-stu-id="293bf-141">A dedicated, unencrypted partition for recovery image placement is recommended to reduce the risk of a failed boot partition.</span></span></p>
<p><span data-ttu-id="293bf-142">Beim Aktualisieren von DART müssen Sie alle Computer in Ihrem Unternehmen anstatt nur eine Partition (im Netzwerk) oder ein Wechsel Gerät aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="293bf-142">When updating DaRT, you must update all computers in your enterprise instead of just one partition (on the network) or removable device.</span></span></p>
<p><span data-ttu-id="293bf-143">Weitere Überlegungen sind erforderlich, wenn Sie das Wiederherstellungsabbild bereitstellen, nachdem BitLocker aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="293bf-143">Additional consideration is required if you deploy the recovery image after BitLocker has been enabled.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="293bf-144">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="293bf-144">Related topics</span></span>


[<span data-ttu-id="293bf-145">Planen der Bereitstellung von DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="293bf-145">Planning to Deploy DaRT 8.0</span></span>](planning-to-deploy-dart-80-dart-8.md)

 

 





