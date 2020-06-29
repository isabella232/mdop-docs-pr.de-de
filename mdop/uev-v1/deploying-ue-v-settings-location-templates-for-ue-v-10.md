---
title: Bereitstellen von UE-V-Speicherortvorlagen für UE-V 1.0
description: Bereitstellen von UE-V-Speicherortvorlagen für UE-V 1.0
author: dansimp
ms.assetid: 7e0cc553-14f7-40fa-828a-281c8d2d1934
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b276fb9d6c0b3749f9818483869dfe98bbc147c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812166"
---
# <span data-ttu-id="fcf98-103">Bereitstellen von UE-V-Speicherortvorlagen für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="fcf98-103">Deploying UE-V Settings Location Templates for UE-V 1.0</span></span>


<span data-ttu-id="fcf98-104">Microsoft User Experience Virtualization (UE-V) verwendet Einstellungen-Standort Vorlagen (XML-Dateien), die die Einstellungen definieren, die von der Benutzeroberflächen-Virtualisierung erfasst und angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="fcf98-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings that are captured and applied by User Experience Virtualization.</span></span> <span data-ttu-id="fcf98-105">UE-v umfasst eine Reihe von Standardvorlagen sowie ein Tool, den UE-v-Generator, mit dem Sie benutzerdefinierte Speicherort Vorlagen für Einstellungen erstellen können.</span><span class="sxs-lookup"><span data-stu-id="fcf98-105">UE-V includes a set of standard templates, as well as a tool, the UE-V Generator, which allows you to create custom settings location templates.</span></span> <span data-ttu-id="fcf98-106">Nachdem Sie eine Vorlage für Einstellungs Speicherort erstellt haben, sollten Sie Sie testen, um sicherzustellen, dass die Anwendungseinstellungen in einer Testumgebung ordnungsgemäß durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="fcf98-106">After you create a settings location template, you should test it to ensure that the application settings roam correctly in a test environment.</span></span> <span data-ttu-id="fcf98-107">Anschließend können Sie die Vorlage für die Einstellungsposition sicher auf Computern im Unternehmen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="fcf98-107">You can then safely deploy the settings location template to computers in the enterprise.</span></span>

<span data-ttu-id="fcf98-108">Einstellungen Speicherort Vorlagen können mithilfe von ESD (Enterprise Software Distribution), Gruppenrichtlinieneinstellungen oder durch Konfigurieren eines UE-V-Einstellungs Vorlagen Katalogs bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="fcf98-108">Settings location templates can be deployed by using enterprise software distribution (ESD), Group Policy preferences, or by configuring a UE-V settings template catalog.</span></span> <span data-ttu-id="fcf98-109">Vorlagen, die mithilfe einer ESD-oder Gruppenrichtlinie bereitgestellt werden, müssen über UE-V WMI oder PowerShell registriert werden.</span><span class="sxs-lookup"><span data-stu-id="fcf98-109">Templates that are deployed by using an ESD or Group Policy must be registered through UE-V WMI or PowerShell.</span></span> <span data-ttu-id="fcf98-110">Vorlagen, die im Katalogspeicherort für Einstellungs Vorlagen gespeichert sind, werden vom UE-V-Agent automatisch registriert.</span><span class="sxs-lookup"><span data-stu-id="fcf98-110">Templates that are stored in the settings template catalog location are automatically registered by the UE-V agent.</span></span>

## <span data-ttu-id="fcf98-111">Bereitstellen der Einstellungen-Speicherort Vorlagen mit einem Katalogpfad für Einstellungs Vorlagen</span><span class="sxs-lookup"><span data-stu-id="fcf98-111">Deploy the settings location templates with a settings template catalog path</span></span>


<span data-ttu-id="fcf98-112">Der Katalogpfad der UE-V-Einstellungen für die Standort Vorlage kann mithilfe der folgenden Methoden definiert werden: Gruppenrichtlinien, Befehlszeilenparameter für Agenteninstallation, WMI oder PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fcf98-112">The UE-V settings location template catalog path can be defined by using the following methods: Group Policy, the agent install command-line parameters, WMI, or PowerShell.</span></span> <span data-ttu-id="fcf98-113">Nach dem Definieren des Vorlagenkatalog Pfads ruft der UE-V-Agent die neuen oder aktualisierten Vorlagen von diesem Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="fcf98-113">After the template catalog path has been defined, the UE-V agent retrieves the new or updated templates from this location.</span></span> <span data-ttu-id="fcf98-114">Der UE-V-Agent überprüft diesen Standort einmal täglich und aktualisiert sein Synchronisierungsverhalten auf der Grundlage der in diesem Ordner gefundenen Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="fcf98-114">The UE-V agent checks this location once each day and updates its synchronization behavior based on the templates found in this folder.</span></span> <span data-ttu-id="fcf98-115">Vorlagen, die seit der letzten Überprüfung in diesem Ordner hinzugefügt oder aktualisiert wurden, werden vom UE-V-Agent registriert.</span><span class="sxs-lookup"><span data-stu-id="fcf98-115">Templates that have been added or updated in this folder since the last check are registered by the UE-V agent.</span></span> <span data-ttu-id="fcf98-116">Der UE-V-Agent hebt auch die Registrierung von Vorlagen auf, die aus diesem Ordner entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="fcf98-116">The UE-V agent also unregisters templates that have been removed from this folder.</span></span> <span data-ttu-id="fcf98-117">Vorlagen werden vom Aufgabenplaner einmal pro Tag registriert und nicht registriert.</span><span class="sxs-lookup"><span data-stu-id="fcf98-117">Templates are registered and unregistered one time per day by the task scheduler.</span></span>

**<span data-ttu-id="fcf98-118">So verwenden Sie den Katalogpfad der Einstellungs Vorlage zum Bereitstellen von UE-V-Einstellungen Speicherort Vorlagen</span><span class="sxs-lookup"><span data-stu-id="fcf98-118">To use settings template catalog path to deploy UE-V settings location templates</span></span>**

1.  <span data-ttu-id="fcf98-119">Navigieren Sie zu dem Netzwerkfreigabeordner, der als Vorlagenkatalog für Einstellungen definiert ist.</span><span class="sxs-lookup"><span data-stu-id="fcf98-119">Navigate to the network share folder that is defined as the settings template catalog.</span></span>

2.  <span data-ttu-id="fcf98-120">Hinzufügen, entfernen oder Aktualisieren von Einstellungen für Standort Vorlagen im Einstellungs Vorlagenkatalog, um die gewünschte UE-v-Agent-Vorlagenkonfiguration für UE-v-Computer wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="fcf98-120">Add, remove, or update settings location templates in the settings template catalog to reflect the desired UE-V agent template configuration for UE-V computers.</span></span>

3.  <span data-ttu-id="fcf98-121">Vorlagen auf Computern werden basierend auf Änderungen am Vorlagenkatalog für Einstellungen täglich aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fcf98-121">Templates on computers are updated daily based on changes to the settings template catalog.</span></span>

4.  <span data-ttu-id="fcf98-122">Öffnen Sie eine Eingabeaufforderung mit erhöhten Rechten, und navigieren Sie zu \*\*% Program Files%\\Microsoft User Experience Virtualization \ \ Agent \ \ &lt; x86 oder x64 &gt; \*\*, und führen Sie dann **ApplySettingsTemplateCatalog.exe** aus, um Vorlagen auf einem Computer, auf dem der UE-V-Agent ausgeführt wird, manuell zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="fcf98-122">Open an elevated command prompt and navigate to **%program files%\\Microsoft user Experience Virtualization \\ Agent \\ &lt;x86 or x64 &gt;**, and then run **ApplySettingsTemplateCatalog.exe** to manually update templates on a computer that runs the UE-V agent.</span></span>

## <span data-ttu-id="fcf98-123">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="fcf98-123">Related topics</span></span>


[<span data-ttu-id="fcf98-124">Microsoft-User Experience Virtualization (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="fcf98-124">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="fcf98-125">Bereitstellen von UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="fcf98-125">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="fcf98-126">Planen der Verwendung von Anwendungen zum Synchronisieren mit UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="fcf98-126">Planning Which Applications to Synchronize with UE-V 1.0</span></span>](planning-which-applications-to-synchronize-with-ue-v-10.md)

 

 





