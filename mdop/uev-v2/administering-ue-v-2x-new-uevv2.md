---
title: Verwalten von UE-V 2. x
description: Verwalten von UE-V 2. x
author: dansimp
ms.assetid: 996e4797-8383-4627-b714-24a84c907798
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2674f6ace80672c1e89bb4f9c765b56f260c3bc0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811296"
---
# <span data-ttu-id="df870-103">Verwalten von UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="df870-103">Administering UE-V 2.x</span></span>


<span data-ttu-id="df870-104">Nachdem Sie die Microsoft User Experience Virtualization (UE-v) 2,0, 2,1 oder 2,1 SP1 bereitgestellt haben, müssen Sie in der Lage sein, verschiedene fortlaufende administrative Aufgaben auszuführen, wie etwa das Verwalten der Konfiguration des UE-v-Agents und das Wiederherstellen verlorener Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="df870-104">After you have deployed Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1, you must be able to perform various ongoing administrative tasks, such as managing the configuration of the UE-V Agent and recovering lost settings.</span></span> <span data-ttu-id="df870-105">Diese Aufgaben nach der Installation werden in den folgenden Abschnitten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="df870-105">These post-installation tasks are described in the following sections.</span></span>

## <span data-ttu-id="df870-106">Verwalten von UE-V 2. x-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="df870-106">Managing UE-V 2.x configurations</span></span>


<span data-ttu-id="df870-107">Im Rahmen des UE-v-Lebenszyklus müssen Sie die Konfiguration des UE-v-Agents verwalten und auch Speicherorte für Ressourcen wie Einstellungen-Paketdateien verwalten.</span><span class="sxs-lookup"><span data-stu-id="df870-107">In the course of the UE-V lifecycle, you have to manage the configuration of the UE-V Agent and also manage storage locations for resources such as settings package files.</span></span>

[<span data-ttu-id="df870-108">Verwalten von Konfigurationen für UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="df870-108">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

## <span data-ttu-id="df870-109">Arbeiten mit benutzerdefinierten UE-v-Vorlagen und dem UE-v 2. x-Generator</span><span class="sxs-lookup"><span data-stu-id="df870-109">Working with custom UE-V templates and the UE-V 2.x Generator</span></span>


<span data-ttu-id="df870-110">In diesem Thema finden Sie Anweisungen zum Verwenden des UE-V-Generators und zum Verwalten von benutzerdefinierten Speicherort Vorlagen für Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="df870-110">This topic provides instructions for how to use the UE-V Generator and manage custom settings location templates.</span></span>

[<span data-ttu-id="df870-111">Arbeiten mit benutzerdefinierten UE-v 2. x-Vorlagen und dem UE-v 2. x-Generator</span><span class="sxs-lookup"><span data-stu-id="df870-111">Working with Custom UE-V 2.x Templates and the UE-V 2.x Generator</span></span>](working-with-custom-ue-v-2x-templates-and-the-ue-v-2x-generator-new-uevv2.md)

## <span data-ttu-id="df870-112">Sichern und Wiederherstellen von Anwendungs-und Windows-Einstellungen, die mit UE-V 2. x synchronisiert werden</span><span class="sxs-lookup"><span data-stu-id="df870-112">Backup and restore application and Windows settings that are synchronized with UE-V 2.x</span></span>


<span data-ttu-id="df870-113">Windows-Verwaltungsinstrumentation (WMI) und Windows PowerShell-Features von UE-V bieten die Möglichkeit zum Wiederherstellen von Einstellungspaketen.</span><span class="sxs-lookup"><span data-stu-id="df870-113">Windows Management Instrumentation (WMI) and Windows PowerShell features of UE-V provide the ability to restore settings packages.</span></span> <span data-ttu-id="df870-114">Mithilfe von WMI-und Windows PowerShell-Befehlen können Sie die Anwendungs-und Windows-Einstellungen in Ihrem ursprünglichen Zustand wiederherstellen und zusätzliche Einstellungen wiederherstellen, wenn ein Benutzer ein neues Gerät annimmt.</span><span class="sxs-lookup"><span data-stu-id="df870-114">By using WMI and Windows PowerShell commands, you can restore application and Windows settings to their original state and restore additional settings when a user adopts a new device.</span></span>

[<span data-ttu-id="df870-115">Verwalten der administrativen Sicherung und Wiederherstellung in UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="df870-115">Manage Administrative Backup and Restore in UE-V 2.x</span></span>](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md)

## <span data-ttu-id="df870-116">Ändern der Häufigkeit von geplanten Aufgaben in UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="df870-116">Changing the frequency of UE-V 2.x scheduled tasks</span></span>


<span data-ttu-id="df870-117">Sie können die geplanten Aufgaben konfigurieren, die verwaltet werden, wenn UE-V nach neuen oder aktualisierten Einstellungen oder nach aktualisierten Standort Vorlagen für benutzerdefinierte Einstellungen im Vorlagenkatalog für Einstellungen sucht.</span><span class="sxs-lookup"><span data-stu-id="df870-117">You can configure the scheduled tasks that manage when UE-V checks for new or updated settings or for updated custom settings location templates in the settings template catalog.</span></span>

[<span data-ttu-id="df870-118">Ändern der Häufigkeit von geplanten Aufgaben in UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="df870-118">Changing the Frequency of UE-V 2.x Scheduled Tasks</span></span>](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

## <span data-ttu-id="df870-119">Migrieren von UE-V 2. x-Einstellungspaketen</span><span class="sxs-lookup"><span data-stu-id="df870-119">Migrating UE-V 2.x settings packages</span></span>


<span data-ttu-id="df870-120">Sie können die Benutzer Einstellungs Pakete entweder bei der Migration zu einem neuen Server oder zu Sicherungszwecken verschieben.</span><span class="sxs-lookup"><span data-stu-id="df870-120">You can relocate the user settings packages either when they migrate to a new server or for backup purposes.</span></span>

[<span data-ttu-id="df870-121">Migrieren von UE-V 2. x-Einstellungspaketen</span><span class="sxs-lookup"><span data-stu-id="df870-121">Migrating UE-V 2.x Settings Packages</span></span>](migrating-ue-v-2x-settings-packages-both-uevv2.md)

## <span data-ttu-id="df870-122">Verwenden von UE-V 2. x mit Application Virtualization-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="df870-122">Using UE-V 2.x with Application Virtualization applications</span></span>


<span data-ttu-id="df870-123">Sie können UE-v mit Microsoft Application Virtualization (app-v) verwenden, um die Einstellungen zwischen virtuellen Anwendungen und installierten Anwendungen auf mehreren Computern freizugeben.</span><span class="sxs-lookup"><span data-stu-id="df870-123">You can use UE-V with Microsoft Application Virtualization (App-V) to share settings between virtual applications and installed applications across multiple computers.</span></span>

[<span data-ttu-id="df870-124">Verwenden von UE-V 2. x mit Application Virtualization-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="df870-124">Using UE-V 2.x with Application Virtualization Applications</span></span>](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md)

## <span data-ttu-id="df870-125">Weitere Ressourcen für dieses Produkt</span><span class="sxs-lookup"><span data-stu-id="df870-125">Other resources for this product</span></span>


-   [<span data-ttu-id="df870-126">Microsoft User Experience Virtualization (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="df870-126">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>](index.md)

-   [<span data-ttu-id="df870-127">Erste Schritte mit UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="df870-127">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="df870-128">Vorbereiten einer UE-V 2. x-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="df870-128">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [<span data-ttu-id="df870-129">Problembehandlung bei UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="df870-129">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="df870-130">Technische Referenz für UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="df870-130">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)






 

 





