---
title: Informationen zu User Experience Virtualization 1.0
description: Informationen zu User Experience Virtualization 1.0
author: dansimp
ms.assetid: 3758b100-35a8-4e10-ac08-f583fb8ddbd9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6010f9c4ebc260eec0324fb880dc2c92fd675130
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809520"
---
# <span data-ttu-id="a8c3f-103">Informationen zu User Experience Virtualization 1.0</span><span class="sxs-lookup"><span data-stu-id="a8c3f-103">About User Experience Virtualization 1.0</span></span>


<span data-ttu-id="a8c3f-104">Microsoft User Experience Virtualization (UE-V) überwacht die von Benutzern vorgenommenen Änderungen an den Anwendungseinstellungen und den Einstellungen des Windows-Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="a8c3f-104">Microsoft User Experience Virtualization (UE-V) monitors the changes that are made by users to application settings and Windows operating system settings.</span></span> <span data-ttu-id="a8c3f-105">Die Benutzereinstellungen werden erfasst und an einem Einstellungs Speicherort zentralisiert.</span><span class="sxs-lookup"><span data-stu-id="a8c3f-105">The user settings are captured and centralized to a settings storage location.</span></span> <span data-ttu-id="a8c3f-106">Diese Einstellungen können dann auf die verschiedenen Computer angewendet werden, auf die der Benutzer zugreifen kann, einschließlich Desktopcomputern, Laptops und Virtual Desktop Infrastructure (VDI)-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="a8c3f-106">These settings can then be applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span>

<span data-ttu-id="a8c3f-107">Die Virtualisierung der Benutzeroberfläche verwendet Einstellungen für Standort Vorlagen, um anzugeben, welche Anwendungen und Windows-Einstellungen auf den Benutzercomputern überwacht und zentralisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a8c3f-107">User Experience Virtualization uses settings location templates to specify what applications and Windows settings on the user computers are monitored and centralized.</span></span> <span data-ttu-id="a8c3f-108">Die Vorlage "Settings Location" ist eine XML-Datei, die angibt, welche Datei-und Registrierungsspeicherorte den einzelnen Anwendungs-oder Betriebssystem Einstellungen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a8c3f-108">The settings location template is an XML file that specifies which file and registry locations are associated with each application or operating system setting.</span></span> <span data-ttu-id="a8c3f-109">Die Vorlage enthält keine Werte für die Einstellungen; Sie enthält nur die Speicherorte der Einstellungen, die überwacht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a8c3f-109">The template does not contain values for the settings; it contains only the locations of the settings that are to be monitored.</span></span>

<span data-ttu-id="a8c3f-110">Die Anwendungseinstellungen und Windows-Einstellungen werden von UE-V überwacht, wenn Benutzer auf ihren Computern arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a8c3f-110">The application settings and Windows settings are monitored by UE-V when users are working on their computers.</span></span> <span data-ttu-id="a8c3f-111">Die Werte für die Anwendungseinstellungen werden auf dem Speicherserver für Einstellungen gespeichert, wenn der Benutzer die Anwendung schließt.</span><span class="sxs-lookup"><span data-stu-id="a8c3f-111">The values for the application settings are stored on the settings storage server when the user closes the application.</span></span> <span data-ttu-id="a8c3f-112">Die Werte für die Windows-Einstellungen werden gespeichert, wenn sich der Benutzer abmeldet, wenn der Computer gesperrt ist oder wenn er die Verbindung von einem Computer entfernt trennt.</span><span class="sxs-lookup"><span data-stu-id="a8c3f-112">The values for the Windows settings are stored when the user logs off, when the computer is locked, or when they disconnect remotely from a computer.</span></span>

<span data-ttu-id="a8c3f-113">Ein Administrator kann eine Standort Vorlage für UE-V-Einstellungen erstellen, um anzugeben, welche Enterprise-Anwendungseinstellungen durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="a8c3f-113">An administrator can create a UE-V settings location template to specify which enterprise application settings will roam.</span></span> <span data-ttu-id="a8c3f-114">UE-V enthält eine Reihe von Einstellungen für die Speicherort Vorlagen für einige Microsoft-Anwendungen und Windows-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="a8c3f-114">UE-V includes a set of settings location templates for some Microsoft applications and Windows settings.</span></span> <span data-ttu-id="a8c3f-115">Eine Liste der Standardanwendungen und-Einstellungen in UE-v finden Sie unter [Planen der zu synchronisierenden Anwendungen mit UE-v 1,0](planning-which-applications-to-synchronize-with-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="a8c3f-115">For a list of default applications and settings in UE-V, see [Planning Which Applications to Synchronize with UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md).</span></span>

## <span data-ttu-id="a8c3f-116">UEV 1,0-Versionshinweise</span><span class="sxs-lookup"><span data-stu-id="a8c3f-116">UEV 1.0 Release Notes</span></span>


<span data-ttu-id="a8c3f-117">Weitere Informationen sowie aktuelle Nachrichten, die nicht in die Dokumentation eingehen, finden Sie unter [Microsoft User Experience Virtualization (UE-V) 1,0-Versionshinweise](microsoft-user-experience-virtualization--ue-v--10-release-notes.md).</span><span class="sxs-lookup"><span data-stu-id="a8c3f-117">For more information, and for late-breaking news that did not make it into the documentation, see [Microsoft User Experience Virtualization (UE-V) 1.0 Release Notes](microsoft-user-experience-virtualization--ue-v--10-release-notes.md).</span></span>

## <span data-ttu-id="a8c3f-118">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a8c3f-118">Related topics</span></span>


[<span data-ttu-id="a8c3f-119">Erste Schritte mit User Experience Virtualization 1.0</span><span class="sxs-lookup"><span data-stu-id="a8c3f-119">Getting Started With User Experience Virtualization 1.0</span></span>](getting-started-with-user-experience-virtualization-10.md)

[<span data-ttu-id="a8c3f-120">Microsoft-User Experience Virtualization (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="a8c3f-120">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="a8c3f-121">High-Level-Architektur für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="a8c3f-121">High-Level Architecture for UE-V 1.0</span></span>](high-level-architecture-for-ue-v-10.md)

 

 





