---
title: Informationen zu virtuellen Umgebungen
description: Informationen zu virtuellen Umgebungen
author: dansimp
ms.assetid: e03a8c72-56c1-4ae9-aa45-0283c50a154c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 15f3ae29ae8d5586f83baa98ea6821e09ae5c305
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809328"
---
# <span data-ttu-id="a5184-103">Informationen zu virtuellen Umgebungen</span><span class="sxs-lookup"><span data-stu-id="a5184-103">About Virtual Environments</span></span>


<span data-ttu-id="a5184-104">Virtuelle Anwendungen werden in virtuellen Umgebungen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5184-104">Virtual applications run in virtual environments.</span></span> <span data-ttu-id="a5184-105">In virtuellen Umgebungen kann jede Anwendung auf einem Desktop-, Laptop-oder Remote Desktop-Sitzungshost Server (RDSession-Host) ohne Installation und Änderung des Hostbetriebssystems ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a5184-105">Virtual environments enable each application to run on a desktop, laptop, or Remote Desktop Session Host (RDSession Host) server without installation and alteration of the host operating system.</span></span> <span data-ttu-id="a5184-106">Jede Anwendung enthält eigene Konfigurationsinformationen in der virtuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="a5184-106">Each application carries its own configuration information in the virtual environment.</span></span> <span data-ttu-id="a5184-107">Daher laufen viele Anwendungen parallel mit anderen Anwendungen auf demselben Computer ohne Konflikte.</span><span class="sxs-lookup"><span data-stu-id="a5184-107">As a result, many applications run side by side with other applications on the same computer without any conflicts.</span></span>

<span data-ttu-id="a5184-108">Virtuelle Anwendungen werden lokal ausgeführt, sodass Sie mit der vollständigen Leistung, Funktionalität und dem Zugriff auf lokale Dienste ausgeführt werden, die Sie von einer lokal installierten Anwendung erwarten.</span><span class="sxs-lookup"><span data-stu-id="a5184-108">Virtual applications run locally, so they run with the full performance, functionality, and access to local services that you would expect from any application installed locally.</span></span>

<span data-ttu-id="a5184-109">Da jede Anwendung in einer virtuellen Umgebung ausgeführt wird, werden die folgenden Probleme reduziert:</span><span class="sxs-lookup"><span data-stu-id="a5184-109">Because each application runs in a virtual environment, the following problems are reduced:</span></span>

-   <span data-ttu-id="a5184-110">Anwendungskonflikte – in Umgebungen, die keine Anwendungsvirtualisierung verwenden, müssen Sie jede Anwendung gründlich testen, um sicherzustellen, dass Sie keine anderen installierten Anwendungen stört.</span><span class="sxs-lookup"><span data-stu-id="a5184-110">Application conflicts—In environments that do not use Application Virtualization, you must thoroughly test every application to ensure that it does not interfere with other installed applications.</span></span>

-   <span data-ttu-id="a5184-111">Regressionstests – da die Anwendung das zugrunde liegende Betriebssystem nicht ändert, werden langwierige Regressionstests eliminiert.</span><span class="sxs-lookup"><span data-stu-id="a5184-111">Regression testing—Because the application does not change the underlying operating system, lengthy regression testing is eliminated.</span></span>

-   <span data-ttu-id="a5184-112">Versionsinkompatibilitäten – verschiedene Versionen der gleichen Anwendung können gleichzeitig auf demselben Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a5184-112">Version incompatibilities—Different versions of the same application can run simultaneously on the same computer.</span></span>

-   <span data-ttu-id="a5184-113">Mehrbenutzerzugriff – Anwendungen, die nicht im Mehrbenutzermodus ausgeführt werden und daher nicht in einem RDSession-Host ausgeführt werden können, können dies nun tun und für mehrere Benutzer auf einem einzelnen RDSession-Host ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="a5184-113">Multiuser access—Applications that do not run in multiuser mode, and therefore cannot run within an RDSession Host, can now do so and function correctly for multiple users on a single RDSession Host.</span></span>

-   <span data-ttu-id="a5184-114">Probleme mit mehreren Instanzen: zwei Instanzen der gleichen Anwendung, die unterschiedliche Konfigurationen verwenden, können gleichzeitig auf demselben Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a5184-114">Multitenancy issues—Two instances of the same application that use different configurations can run on the same computer at the same time.</span></span>

-   <span data-ttu-id="a5184-115">Server-siloing – die Notwendigkeit für viele getrennte Serverfarmen wird eliminiert.</span><span class="sxs-lookup"><span data-stu-id="a5184-115">Server siloing—The need for many separate server farms is eliminated.</span></span>

<span data-ttu-id="a5184-116">Virtuelle Umgebungen umfassen eine virtuelle Registrierung für jede Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a5184-116">Virtual environments include a virtual registry for each application.</span></span> <span data-ttu-id="a5184-117">Von einer Anwendung erstellte Registrierungseinstellungen können von anderen Anwendungen oder Dienstprogrammen wie "regedit" nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a5184-117">Registry settings created by one application cannot be seen by other applications or utilities such as Regedit.</span></span> <span data-ttu-id="a5184-118">Anstatt die gesamte Registrierung zu kopieren, verwendet die virtuelle Registrierung eine *Overlay* -Methode.</span><span class="sxs-lookup"><span data-stu-id="a5184-118">Rather than copying the entire registry, the virtual registry uses an *overlay* method.</span></span> <span data-ttu-id="a5184-119">Elemente in der Clientregistrierung können von der Anwendung gelesen werden, solange eine virtuelle Kopie dieses Registrierungselements nicht in der virtuellen Registrierung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a5184-119">Items in the client registry can be read by the application as long as a virtual copy of that registry item is not included in the virtual registry.</span></span> <span data-ttu-id="a5184-120">Alle Anwendungs Schreibvorgänge in der Registrierung sind in der virtuellen Registrierung enthalten.</span><span class="sxs-lookup"><span data-stu-id="a5184-120">All application writes to the registry are contained in the virtual registry.</span></span>

<span data-ttu-id="a5184-121">Zu den virtuellen Umgebungen gehören auch ein virtuelles Dateisystem und andere virtuelle Komponenten, einschließlich virtueller Dienste und virtueller com.</span><span class="sxs-lookup"><span data-stu-id="a5184-121">Virtual environments also include a virtual file system and other virtual components, including virtual services and virtual COM.</span></span>

## <span data-ttu-id="a5184-122">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a5184-122">Related topics</span></span>


[<span data-ttu-id="a5184-123">Application Virtualization Client Management Console – Übersicht</span><span class="sxs-lookup"><span data-stu-id="a5184-123">Application Virtualization Client Management Console Overview</span></span>](application-virtualization-client-management-console-overview.md)

 

 





