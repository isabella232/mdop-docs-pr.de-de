---
title: Neuigkeiten in AGPM 4.0
description: Neuigkeiten in AGPM 4.0
author: dansimp
ms.assetid: 31775f7f-a59c-4e64-a875-0adc9f5bc835
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 82b4445a7d22fb7c1ef4f42d896f11908a22f2f5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808172"
---
# <span data-ttu-id="44194-103">Neuigkeiten in AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="44194-103">What's New in AGPM 4.0</span></span>


<span data-ttu-id="44194-104">Microsoft Advanced Group Policy Management (AGPM) 4.0 enthält neue Features, mit denen Sie nach Gruppenrichtlinienobjekten (Group Policy Objects, GPOs) suchen, die Liste der angezeigten GPOs filtern, ein GPO in eine andere Gesamtstruktur exportieren und importieren sowie AGPM auf Computern installieren können, auf denen Windows7 und Windows Server2008R2 ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="44194-104">Microsoft Advanced Group Policy Management (AGPM)4.0 includes new features that let you search for Group Policy Objects (GPOs), filter the list of GPOs displayed, export and import a GPO to a different forest, and install AGPM on computers running Windows7 and Windows Server2008R2.</span></span>

## <span data-ttu-id="44194-105">Suchen und Filtern von GPOs</span><span class="sxs-lookup"><span data-stu-id="44194-105">Search and filter GPOs</span></span>


<span data-ttu-id="44194-106">In AGPM 4,0 können Sie die Liste der GPOs nach bestimmten Attributen durchsuchen, um die Liste der angezeigten GPOs zu filtern.</span><span class="sxs-lookup"><span data-stu-id="44194-106">In AGPM 4.0, you can search the list of GPOs for specific attributes to filter the list of GPOs displayed.</span></span> <span data-ttu-id="44194-107">So können Sie beispielsweise nach GPOs mit einem bestimmten Namen, Zustand oder Kommentar suchen.</span><span class="sxs-lookup"><span data-stu-id="44194-107">For example, you can search for GPOs with a particular name, state, or comment.</span></span> <span data-ttu-id="44194-108">Sie können auch nach GPOs suchen, die zuletzt von einem bestimmten Gruppenrichtlinienadministrator oder an einem bestimmten Datum geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="44194-108">You can also search for GPOs that were last changed by a particular Group Policy administrator or on a particular date.</span></span>

<span data-ttu-id="44194-109">Sie können eine komplexe Suchzeichenfolge erstellen, indem Sie das Gruppenrichtlinien *Objekt-Attribut 1: Suchtext 1 GPO-Attribut 2: Suchtext 2...* verwenden, wobei ein GPO-Attribut eine beliebige Spaltenüberschrift in der Liste der GPOs in AGPM ist.</span><span class="sxs-lookup"><span data-stu-id="44194-109">You can create a complex search string by using the format *GPO attribute 1: search text 1 GPO attribute 2: search text 2…*, where a GPO attribute is any column heading in the list of GPOs in AGPM.</span></span> <span data-ttu-id="44194-110">Wenn Sie beispielsweise nach allen GPOs mit Namen suchen möchten, einschließlich des Texts "eigenes", der eingecheckt wurde und zuletzt vom Benutzer Editor03 geändert wurde, geben Sie Folgendes in das Suchfeld ein: **Name: eigenes Zustand:\*\*\*\*eingecheckt\*\*\*\*geändert von: Editor03**.</span><span class="sxs-lookup"><span data-stu-id="44194-110">For example, to search for all GPOs with names including the text "MyGPO" that are checked in and were last changed by the user Editor03, you would type the following in the Search box: **name: MyGPO state:\*\*\*\*checked in\*\*\*\*changed by: Editor03**.</span></span> <span data-ttu-id="44194-111">Die Suche gibt partielle Übereinstimmungen zurück, sodass Sie einen Teil eines GPO-namens oder Benutzernamens eingeben und eine Liste aller GPOs anzeigen können, die diesen Text in seinem Namen enthalten.</span><span class="sxs-lookup"><span data-stu-id="44194-111">The search returns partial matches so that you can enter part of a GPO name or user name and view a list of all GPOs that include that text in their name.</span></span>

<span data-ttu-id="44194-112">Darüber hinaus können Sie die gleichen speziellen Begriffe verwenden, die bei der Suche in Windows für die Suche nach GPOs, die an einem bestimmten Datum oder Datumsbereich geändert wurden, verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="44194-112">Additionally, you can use the same special terms available when you search in Windows to search for GPOs changed on a specific date or range of dates.</span></span> <span data-ttu-id="44194-113">Ändern Sie beispielsweise **Datum:\*\*\*\*lastmonth** oder **Datum ändern:\*\*\*\*thisWeek**.</span><span class="sxs-lookup"><span data-stu-id="44194-113">For example, **change date:\*\*\*\*lastmonth** or **change date:\*\*\*\*thisweek**.</span></span>

## <span data-ttu-id="44194-114">Exportieren und Importieren von GPOs in unterschiedliche Gesamtstrukturen</span><span class="sxs-lookup"><span data-stu-id="44194-114">Export and import GPOs to different forests</span></span>


<span data-ttu-id="44194-115">Mithilfe von AGPM 4,0 können Sie ein gesteuertes Gruppenrichtlinienobjekt aus einer Domäne in einer Gesamtstruktur in eine Domäne in einer zweiten Gesamtstruktur kopieren.</span><span class="sxs-lookup"><span data-stu-id="44194-115">Using AGPM 4.0, you can copy a controlled GPO from a domain in one forest to a domain in a second forest.</span></span> <span data-ttu-id="44194-116">So können Sie beispielsweise ein GPO aus einer Domäne in einer Gesamtstruktur in eine CAB-Datei exportieren, indem Sie AGPM verwenden, diese CAB-Datei auf ein USB-Laufwerk kopieren, das USB-Laufwerk an einen Computer in einer Domäne in einer zweiten Gesamtstruktur anschließen und das Gruppenrichtlinienobjekt in AGPM in einer Domäne in der zweiten Gesamtstruktur importieren.</span><span class="sxs-lookup"><span data-stu-id="44194-116">For example, you can export a GPO from a domain in one forest to a CAB file by using AGPM, copy that CAB file to a USB drive, plug the USB drive into a computer in a domain in a second forest, and import the GPO into AGPM in a domain in the second forest.</span></span> <span data-ttu-id="44194-117">Sie können das Gruppenrichtlinienobjekt entweder als neues gesteuertes Gruppenrichtlinienobjekt importieren oder es importieren, um die Einstellungen eines vorhandenen Gruppenrichtlinienobjekts zu ersetzen, das ausgecheckt ist.</span><span class="sxs-lookup"><span data-stu-id="44194-117">You can either import the GPO as a new controlled GPO, or import it to replace the settings of an existing GPO that is checked out.</span></span>

## <span data-ttu-id="44194-118">Unterstützung für Windows Server 2008 R2 und Windows 7</span><span class="sxs-lookup"><span data-stu-id="44194-118">Support for Windows Server 2008 R2 and Windows 7</span></span>


<span data-ttu-id="44194-119">AGPM 4,0 unterstützt Windows Server2008R2 und Windows7 und unterstützt dennoch Windows Server2008 und Windows Vista® mit Service Pack1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="44194-119">AGPM 4.0 supports Windows Server2008R2 and Windows7, yet still supports Windows Server2008 and WindowsVista® with Service Pack1 (SP1).</span></span> <span data-ttu-id="44194-120">Es gibt jedoch Einschränkungen in einer gemischten Umgebung, die sowohl das neuere als auch das ältere Betriebssystem enthält, wie in der folgenden Tabelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="44194-120">However, there are limitations in a mixed environment that includes both the newer and older operating systems, as indicated in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="44194-121">Betriebssystem, auf dem AGPM Server 4,0 ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="44194-121">Operating system on which AGPM Server 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="44194-122">Betriebssystem, auf dem AGPM-Client 4,0 ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="44194-122">Operating system on which AGPM Client 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="44194-123">Status der Unterstützung von AGPM 4,0</span><span class="sxs-lookup"><span data-stu-id="44194-123">Status of AGPM 4.0 support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44194-124">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="44194-124">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="44194-125">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="44194-125">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="44194-126">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="44194-126">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44194-127">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="44194-127">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="44194-128">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="44194-128">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="44194-129">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2008R2 oder Windows7 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="44194-129">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44194-130">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="44194-130">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="44194-131">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="44194-131">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="44194-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="44194-132">Unsupported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44194-133">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="44194-133">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="44194-134">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="44194-134">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="44194-135">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2008R2 oder Windows7 vorhanden sind, können nicht gemeldet oder bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="44194-135">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 





