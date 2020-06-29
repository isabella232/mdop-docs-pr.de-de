---
title: Versionshinweise für MED-V 1.0
description: Versionshinweise für MED-V 1.0
author: dansimp
ms.assetid: 006a3537-5c5b-43b5-8df8-4bf6ddd3cd2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 683056f768a3d547828996a9b191d58337c21ad6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811848"
---
# <span data-ttu-id="f8afb-103">Versionshinweise für MED-V 1.0</span><span class="sxs-lookup"><span data-stu-id="f8afb-103">MED-V 1.0 Release Notes</span></span>


## <span data-ttu-id="f8afb-104">Bekannte Probleme mit MED-V</span><span class="sxs-lookup"><span data-stu-id="f8afb-104">Known Issues with MED-V</span></span>


<span data-ttu-id="f8afb-105">Dieser Abschnitt enthält die aktuellsten Informationen zu allgemeinen Problemen mit der Microsoft Enterprise Desktop Virtualization (MED-V)-Plattform.</span><span class="sxs-lookup"><span data-stu-id="f8afb-105">This section provides the most up-to-date information about general issues with the Microsoft Enterprise Desktop Virtualization (MED-V) platform.</span></span> <span data-ttu-id="f8afb-106">Diese Probleme werden in der Produktdokumentation nicht angezeigt und können in einigen Fällen der vorhandenen Produktdokumentation widersprechen.</span><span class="sxs-lookup"><span data-stu-id="f8afb-106">These issues do not appear in the product documentation and in some cases might contradict existing product documentation.</span></span> <span data-ttu-id="f8afb-107">Wenn möglich, werden diese Probleme in späteren Versionen behoben.</span><span class="sxs-lookup"><span data-stu-id="f8afb-107">Whenever possible, these issues will be addressed in later releases.</span></span>

### <span data-ttu-id="f8afb-108">Dateidownloads folgen nicht den webumleitungs Regeln</span><span class="sxs-lookup"><span data-stu-id="f8afb-108">File downloads do not follow Web redirection rules</span></span>

<span data-ttu-id="f8afb-109">Dateidownloads folgen nicht den webumleitungs Regeln, die in einer MED-V-Arbeitsbereichs Richtlinie festgesetzt sind.</span><span class="sxs-lookup"><span data-stu-id="f8afb-109">File downloads do not follow Web redirection rules set in a MED-V workspace policy.</span></span>

### <span data-ttu-id="f8afb-110">Wenn Sie ein von der Konsole veröffentlichtes Anwendungsfenster auf den Vollbildmodus erweitern, wird es nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f8afb-110">When expanding a console-published application window to full screen, it disappears</span></span>

<span data-ttu-id="f8afb-111">Wenn Sie eine von der Konsole veröffentlichte Anwendung (wie cmd.exe) auf Vollbild in einem im Seamless-Integrationsmodus konfigurierten MED-V-Arbeitsbereich erweitern, kann das Anwendungsfenster verschwinden oder nicht reagieren.</span><span class="sxs-lookup"><span data-stu-id="f8afb-111">If you expand a console-published application (such as cmd.exe) window to full screen inside a MED-V workspace configured in seamless integration mode, the application window might disappear or not respond.</span></span>

### <span data-ttu-id="f8afb-112">Wenn Sie im vollständigen Desktopmodus arbeiten, werden die Symbolspeicherorte auf dem Desktop nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f8afb-112">When working in full desktop mode, icon locations on the desktop are not saved</span></span>

<span data-ttu-id="f8afb-113">Wenn Sie im vollständigen Desktopmodus arbeiten, werden die Änderungen manueller Standort Symbole auf dem Desktop nicht zwischen MED-V Workspace-Sitzungen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f8afb-113">When working in full desktop mode, manual location changes of icons on the desktop are not saved between MED-V workspace sessions.</span></span>

### <span data-ttu-id="f8afb-114">Ein lokales Bild und ein Testbild mit demselben Namen können in der gleichen Domäne nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="f8afb-114">A local image and a test image with the same name cannot exist in the same domain</span></span>

<span data-ttu-id="f8afb-115">Wenn ein lokales Bild zur Domäne hinzugefügt wird und der Administrator eine neue Version desselben Bilds mit dem gleichen Computernamen wie ein Testbild erstellt, wenn das Testbild der Domäne Beitritt, schlägt entweder die Aktion für die Join-Domäne fehl, oder es ist erfolgreich, und das lokale Bild wird aus der Domäne entfernt.</span><span class="sxs-lookup"><span data-stu-id="f8afb-115">If a local image is joined to the domain and the administrator creates a new version of the same image with the same computer name as a test image, when the test image joins the domain, either the join domain action fails or it succeeds and the local image is removed from the domain.</span></span>

### <span data-ttu-id="f8afb-116">MED-V unterstützt keine Windows Aero-Features</span><span class="sxs-lookup"><span data-stu-id="f8afb-116">MED-V does not support Windows Aero features</span></span>

<span data-ttu-id="f8afb-117">MED-V unterstützt keine Windows Aero-Features (wie Aero Flip 3D).</span><span class="sxs-lookup"><span data-stu-id="f8afb-117">MED-V does not support Windows Aero features (such as Aero Flip 3D).</span></span>

### <span data-ttu-id="f8afb-118">Die Verwaltungskonsole kann nur von einem Windows-Benutzer pro Computer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8afb-118">The management console can be used by only one Windows user per computer</span></span>

<span data-ttu-id="f8afb-119">Die MED-V-Verwaltungskonsole kann nur von Administratoren und dem Windows-Benutzer verwendet werden, der die Verwaltungsanwendung installiert hat.</span><span class="sxs-lookup"><span data-stu-id="f8afb-119">The MED-V management console can be used only by administrators and the Windows user who installed the management application.</span></span>

### <span data-ttu-id="f8afb-120">Das Med-v Server-Konfigurationsdienstprogramm testet die Microsoft SQL Server-Konnektivität unter dem Benutzerkontext und nicht unter dem Med-v Server-Dienstkontext.</span><span class="sxs-lookup"><span data-stu-id="f8afb-120">The MED-V Server configuration utility tests Microsoft SQL Server connectivity under user context rather than under MED-V Server service context</span></span>

<span data-ttu-id="f8afb-121">Med-v verwendet den Med-v-Server Dienstkontext, um Berichte aus der Microsoft SQL Server-Berichtsdatenbank zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="f8afb-121">MED-V uses MED-V Server service context to collect reports from the Microsoft SQL Server reports database.</span></span> <span data-ttu-id="f8afb-122">Das MED-V Server-Konfigurationsdienstprogramm überprüft die Datenbank und testet die Datenbankverbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f8afb-122">The MED-V Server configuration utility verifies the database and tests the database connection string.</span></span> <span data-ttu-id="f8afb-123">Der Zugriff des MED-V-Server Diensts auf die Datenbank wird nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="f8afb-123">It does not validate the access of MED-V Server service to the database.</span></span>

 

 





