---
title: Verwalten von UE-V 1.0
description: Verwalten von UE-V 1.0
author: dansimp
ms.assetid: c399ae8d-c839-4f84-9bfc-adacd8f89f34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce4dcafd1949dcedd195569dabb7540ce55a2f1a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809511"
---
# <span data-ttu-id="ccdbb-103">Verwalten von UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="ccdbb-103">Administering UE-V 1.0</span></span>


<span data-ttu-id="ccdbb-104">Nachdem Sie die Microsoft User Experience Virtualization (UE-V) bereitgestellt haben, müssen Sie in der Lage sein, verschiedene fortlaufende administrative Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ccdbb-104">After you have deployed Microsoft User Experience Virtualization (UE-V), you must be able to perform various ongoing administrative tasks.</span></span> <span data-ttu-id="ccdbb-105">Diese Aufgaben nach der Installation werden in den folgenden Abschnitten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ccdbb-105">These post-installation tasks are described in the following sections.</span></span>

## <span data-ttu-id="ccdbb-106">Verwalten von UE-V-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ccdbb-106">Managing UE-V resources</span></span>


<span data-ttu-id="ccdbb-107">Im Rahmen des UE-v-Lebenszyklus müssen Sie die Konfiguration des UE-v-Agents verwalten und auch Speicherorte für Ressourcen wie Einstellungs Pakete verwalten.</span><span class="sxs-lookup"><span data-stu-id="ccdbb-107">In the course of the UE-V lifecycle, you will need to manage the configuration of the UE-V agent and also manage storage locations for resources such as settings packages.</span></span> <span data-ttu-id="ccdbb-108">Möglicherweise müssen Sie andere Aufgaben ausführen, um die Einstellungen eines Benutzers wieder in seinen ursprünglichen Zustand zu versetzen, bevor UE-V installiert wurde, um verlorene Einstellungen wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="ccdbb-108">You might need to perform other tasks such as to restore a user’s settings to their original state from before UE-V was installed in order to recover lost settings.</span></span> <span data-ttu-id="ccdbb-109">Die folgenden Themen enthalten Anleitungen zum Verwalten von UE-V-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="ccdbb-109">The following topics provide guidance for managing UE-V resources.</span></span>

### <span data-ttu-id="ccdbb-110">Ändern der Häufigkeit von geplanten UE-V-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="ccdbb-110">Changing the Frequency of UE-V Scheduled Tasks</span></span>

<span data-ttu-id="ccdbb-111">Sie können die geplanten Aufgaben konfigurieren, die verwaltet werden, wenn UE-V im Einstellungs Vorlagenkatalog nach neuen, aktualisierten oder entfernten Standort Vorlagen für benutzerdefinierte Einstellungen sucht.</span><span class="sxs-lookup"><span data-stu-id="ccdbb-111">You can configure the scheduled tasks that manage when UE-V checks for new, updated, or removed custom settings location templates in the settings template catalog.</span></span>

[<span data-ttu-id="ccdbb-112">Ändern der Häufigkeit von geplanten UE-V-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="ccdbb-112">Changing the Frequency of UE-V Scheduled Tasks</span></span>](changing-the-frequency-of-ue-v-scheduled-tasks.md)

### <a href="" id="sharing-settings-location-templates-with-the-ue-v-template-gallery-"></a><span data-ttu-id="ccdbb-113">Freigeben der Speicherortvorlagen für den UE-V-Vorlagenkatalog</span><span class="sxs-lookup"><span data-stu-id="ccdbb-113">Sharing Settings Location Templates with the UE-V Template Gallery</span></span>

<span data-ttu-id="ccdbb-114">Der UE-v-Vorlagenkatalog vereinfacht die Freigabe von Standort Vorlagen für UE-v-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="ccdbb-114">The UE-V template gallery facilitates the sharing of UE-V settings location templates.</span></span> <span data-ttu-id="ccdbb-115">Im Katalog können Sie Ihre Einstellungen-Standort Vorlagen hochladen, damit Sie für andere Personen freigegeben und Vorlagen heruntergeladen werden, die von anderen Personen erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ccdbb-115">The gallery enables you to upload your settings location templates to share with other people and to download templates that other people have created.</span></span>

[<span data-ttu-id="ccdbb-116">Freigeben der Speicherortvorlagen für den UE-V-Vorlagenkatalog</span><span class="sxs-lookup"><span data-stu-id="ccdbb-116">Sharing Settings Location Templates with the UE-V Template Gallery</span></span>](sharing-settings-location-templates-with-the-ue-v-template-gallery.md)

### <span data-ttu-id="ccdbb-117">Wiederherstellen von Anwendungs-und Windows-Einstellungen, die mit UE-V 1,0 synchronisiert wurden</span><span class="sxs-lookup"><span data-stu-id="ccdbb-117">Restoring application and Windows settings synchronized with UE-V 1.0</span></span>

<span data-ttu-id="ccdbb-118">WMI-und PowerShell-Features von UE-V bieten die Möglichkeit zum Wiederherstellen von Einstellungspaketen.</span><span class="sxs-lookup"><span data-stu-id="ccdbb-118">WMI and PowerShell features of UE-V provide the ability to restore settings packages.</span></span> <span data-ttu-id="ccdbb-119">Mit WMI-und PowerShell-Befehlen können Sie Anwendungseinstellungen und Windows-Einstellungen auf die Einstellungswerte zurücksetzen, die sich auf dem Computer befanden, als die Anwendung zum ersten Mal gestartet wurde, nachdem der UE-V-Agent gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="ccdbb-119">WMI and PowerShell commands allow you to restore application settings and Windows settings to the settings values that were on the computer the first time the application was started after the UE-V agent was launched.</span></span>

[<span data-ttu-id="ccdbb-120">Wiederherstellen von Anwendungs- und Windows-Einstellungen, die mit UE-V 1.0 synchronisiert sind</span><span class="sxs-lookup"><span data-stu-id="ccdbb-120">Restoring Application and Windows Settings Synchronized with UE-V 1.0</span></span>](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md)

### <span data-ttu-id="ccdbb-121">Konfigurieren von UE-V mit Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="ccdbb-121">Configuring UE-V with Group Policy Objects</span></span>

<span data-ttu-id="ccdbb-122">Sie können Gruppenrichtlinien verwenden, um die Einstellungen zu ändern, die definieren, wie UE-V die Einstellungen auf Computern synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="ccdbb-122">You can use Group Policy to modify the settings that define how UE-V synchronizes settings on computers.</span></span>

[<span data-ttu-id="ccdbb-123">Konfigurieren von UE-V mit Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="ccdbb-123">Configuring UE-V with Group Policy Objects</span></span>](configuring-ue-v-with-group-policy-objects.md)

### <span data-ttu-id="ccdbb-124">Verwalten von UE-V mit PowerShell und WMI</span><span class="sxs-lookup"><span data-stu-id="ccdbb-124">Administering UE-V with PowerShell and WMI</span></span>

<span data-ttu-id="ccdbb-125">Sie können PowerShell und WMI verwenden, um die Einstellungen zu ändern, die definieren, wie UE-V die Einstellungen auf Computern synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="ccdbb-125">You can use PowerShell and WMI to modify the settings that define how UE-V synchronizes settings on computers.</span></span>

[<span data-ttu-id="ccdbb-126">Verwalten des UE-V 1.0-Agents und von Paketen mit PowerShell und WMI</span><span class="sxs-lookup"><span data-stu-id="ccdbb-126">Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI</span></span>](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

### <span data-ttu-id="ccdbb-127">Migrieren von UE-V-Einstellungspaketen</span><span class="sxs-lookup"><span data-stu-id="ccdbb-127">Migrating UE-V Settings Packages</span></span>

<span data-ttu-id="ccdbb-128">Sie können die Benutzer Einstellungs Pakete entweder beim Migrieren zu einem neuen Server oder zu Sicherungszwecken verschieben.</span><span class="sxs-lookup"><span data-stu-id="ccdbb-128">You can relocate the user settings packages either when migrating to a new server or for backup purposes.</span></span>

[<span data-ttu-id="ccdbb-129">Migrieren von UE-V-Einstellungspaketen</span><span class="sxs-lookup"><span data-stu-id="ccdbb-129">Migrating UE-V Settings Packages</span></span>](migrating-ue-v-settings-packages.md)

## <span data-ttu-id="ccdbb-130">Weitere Ressourcen für dieses Produkt</span><span class="sxs-lookup"><span data-stu-id="ccdbb-130">Other resources for this product</span></span>


[<span data-ttu-id="ccdbb-131">Vorgänge für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="ccdbb-131">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





