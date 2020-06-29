---
title: Informationen über die Registerkarte "Virtuelle Registrierung"
description: Informationen über die Registerkarte "Virtuelle Registrierung"
author: dansimp
ms.assetid: ca8d837f-8218-4f86-95fd-13a44dccd022
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 77decee4a8e07333b466db0a1bd0513efe859c9a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808088"
---
# <span data-ttu-id="7203d-103">Informationen über die Registerkarte "Virtuelle Registrierung"</span><span class="sxs-lookup"><span data-stu-id="7203d-103">About the Virtual Registry Tab</span></span>


<span data-ttu-id="7203d-104">Während der Sequenzierung wird eine virtuelle Registrierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="7203d-104">A virtual registry is created during sequencing.</span></span> <span data-ttu-id="7203d-105">Auf der Registerkarte **virtuelle Registrierung** werden alle Registrierungsschlüssel und Werte angezeigt, die für die Ausführung eines sequenzierten Anwendungspakets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7203d-105">The **Virtual Registry** tab displays all the registry keys and values that are required for a sequenced application package to run.</span></span> <span data-ttu-id="7203d-106">Verwenden Sie diese Registerkarte, um Registrierungsschlüssel und Registrierungswerte hinzuzufügen, zu bearbeiten und zu löschen.</span><span class="sxs-lookup"><span data-stu-id="7203d-106">Use this tab to add, edit, and delete registry keys and registry values.</span></span>

<span data-ttu-id="7203d-107">Sie können auch die Schlüssel des Hostsystems ignorieren, indem Sie den **lokalen Schlüssel außer Kraft setzen**auswählen, oder Sie können eine zusammengeführte Ansicht des Schlüssels in der virtuellen Umgebung erstellen, indem Sie **Zusammenführen mit dem lokalen Schlüssel**auswählen.</span><span class="sxs-lookup"><span data-stu-id="7203d-107">You can also choose to ignore the hosting system’s keys by selecting **Override Local Key**, or you can create a merged view of the key from within the virtual environment by selecting **Merge with Local Key**.</span></span>

<span data-ttu-id="7203d-108">Die Änderungen an der Registerkarte "virtuelle Registrierungs **Einstellungen** " wirken sich auf Anwendungen aus, die Teil des spezifischen sequenzierten Anwendungspakets sind, aber Sie wirken sich nicht auf den Betrieb anderer Anwendungen aus, die auf dem Application Virtualization Desktop Client gestreamt oder lokal installiert werden.</span><span class="sxs-lookup"><span data-stu-id="7203d-108">The changes to the virtual registry **Settings** tab affect applications that are part of the specific sequenced application package, but they do not affect the operation of other applications that are streamed to or locally installed on the Application Virtualization Desktop Client.</span></span>

<span data-ttu-id="7203d-109">**Hinweis**  Beim Ändern von virtuellen Registrierungsschlüsseln und-Werten sollten Sie Vorsicht walten lassen.</span><span class="sxs-lookup"><span data-stu-id="7203d-109">**Note** Exercise caution when changing virtual registry keys and values.</span></span> <span data-ttu-id="7203d-110">Durch das Ändern dieser Schlüssel und Werte kann das sequenzierte Anwendungspaket möglicherweise nicht mehr funktionsfähig sein.</span><span class="sxs-lookup"><span data-stu-id="7203d-110">Changing these keys and values might render your sequenced application package inoperable.</span></span>

 

<span data-ttu-id="7203d-111">Der linke Bereich der Registerkarte " **virtuelle Registrierung** " zeigt die vollständige Liste der virtuellen Register an, die während der Sequenzierung einer Anwendung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="7203d-111">The left pane of the **Virtual Registry** tab displays the full list of virtual registries created during the sequencing of an application.</span></span>

## <span data-ttu-id="7203d-112">Spalten</span><span class="sxs-lookup"><span data-stu-id="7203d-112">Columns</span></span>


<a href="" id="name"></a>**<span data-ttu-id="7203d-113">Name</span><span class="sxs-lookup"><span data-stu-id="7203d-113">Name</span></span>**  
<span data-ttu-id="7203d-114">Der Name für den Eintrag in der virtuellen Registrierung.</span><span class="sxs-lookup"><span data-stu-id="7203d-114">The name for the entry in the virtual registry.</span></span>

<a href="" id="type"></a>**<span data-ttu-id="7203d-115">Typ</span><span class="sxs-lookup"><span data-stu-id="7203d-115">Type</span></span>**  
<span data-ttu-id="7203d-116">Speichert die Daten des Eintrags.</span><span class="sxs-lookup"><span data-stu-id="7203d-116">How the entry stores its data.</span></span>

<a href="" id="data"></a>**<span data-ttu-id="7203d-117">Daten</span><span class="sxs-lookup"><span data-stu-id="7203d-117">Data</span></span>**  
<span data-ttu-id="7203d-118">Der durch den Eintrag gespeicherte Wert.</span><span class="sxs-lookup"><span data-stu-id="7203d-118">The value stored by the entry.</span></span>

<a href="" id="attributes"></a>**<span data-ttu-id="7203d-119">Attribute</span><span class="sxs-lookup"><span data-stu-id="7203d-119">Attributes</span></span>**  
<span data-ttu-id="7203d-120">Zeigt die Dateiattribute an.</span><span class="sxs-lookup"><span data-stu-id="7203d-120">Displays the file attributes.</span></span>

## <span data-ttu-id="7203d-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7203d-121">Related topics</span></span>


[<span data-ttu-id="7203d-122">So ändern Sie die Schlüsselinformationen der virtuellen Registrierung</span><span class="sxs-lookup"><span data-stu-id="7203d-122">How to Modify Virtual Registry Key Information</span></span>](how-to-modify-virtual-registry-key-information.md)

[<span data-ttu-id="7203d-123">Sequencer Console</span><span class="sxs-lookup"><span data-stu-id="7203d-123">Sequencer Console</span></span>](sequencer-console.md)

 

 





