---
title: Übersicht über die Szenarien für die eigenständige Bereitstellung
description: Übersicht über die Szenarien für die eigenständige Bereitstellung
author: dansimp
ms.assetid: b109f309-f3c1-43af-996f-2a9b138dd171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f29b1c8d1c9ae97f7a21498369647f31f552839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806255"
---
# <span data-ttu-id="cd6a6-103">Übersicht über die Szenarien für die eigenständige Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="cd6a6-103">Stand-Alone Delivery Scenario Overview</span></span>


<span data-ttu-id="cd6a6-104">Das eigenständige Zustellungs Szenario ist eine ideale Application Virtualization-Lösung für Umgebungen, in denen eine Verbindung mit niedriger Bandbreite oder keine Konnektivität die Möglichkeit des Application Virtualization Desktop-Clients zum Streamen von Anwendungen von zentralisierten Servern begrenzt.</span><span class="sxs-lookup"><span data-stu-id="cd6a6-104">The stand-alone delivery scenario is an ideal application virtualization solution for environments where either low bandwidth connectivity or no connectivity limits the ability of the Application Virtualization Desktop Client to stream applications from centralized servers.</span></span> <span data-ttu-id="cd6a6-105">In diesen Umgebungen arbeiten Benutzer häufig Remote, und Gerätebesitzer installieren Anwendungen mithilfe von Windows Installer-Dateien.</span><span class="sxs-lookup"><span data-stu-id="cd6a6-105">In these environments, users often work remotely and device owners install applications by using Windows Installer files.</span></span>

<span data-ttu-id="cd6a6-106">Sie können den Application Virtualization Sequencer verwenden, um sequenzierte Anwendungen zu erstellen, die Windows Installer-Dateien enthalten.</span><span class="sxs-lookup"><span data-stu-id="cd6a6-106">You can use the Application Virtualization Sequencer to create sequenced applications that include Windows Installer files.</span></span> <span data-ttu-id="cd6a6-107">Diese Pakete umfassen virtualisierte Anwendungen, Veröffentlichungsinformationen und die erforderlichen Installationsroutinen für die Installation der Pakete auf den Clientsystemen.</span><span class="sxs-lookup"><span data-stu-id="cd6a6-107">These packages include the virtualized applications, publication information, and the necessary installer routines for installing the packages on the client systems.</span></span> <span data-ttu-id="cd6a6-108">Das Installationsprogramm fügt das virtuelle Anwendungspaket dem Microsoft Application Virtualization-Desktop Client hinzu.</span><span class="sxs-lookup"><span data-stu-id="cd6a6-108">The installer adds the virtual application package to the Microsoft Application Virtualization Desktop Client.</span></span> <span data-ttu-id="cd6a6-109">Die Veröffentlichungsinformationen sind so konfiguriert, dass Anwendungen von einem lokalen Speicherort geladen werden, anstatt Sie über ein WAN zu streamen.</span><span class="sxs-lookup"><span data-stu-id="cd6a6-109">The publication information is configured to load applications from a local location rather than stream them across a WAN.</span></span> <span data-ttu-id="cd6a6-110">Benutzer können temporär eine Verbindung mit einem Netzwerk herstellen, um die Windows Installer-Dateien abzurufen, oder Sie können Sie von einer DVD ausführen.</span><span class="sxs-lookup"><span data-stu-id="cd6a6-110">Users can temporarily connect to a network to retrieve the Windows Installer files or can run them from a DVD.</span></span>

<span data-ttu-id="cd6a6-111">Das eigenständige Zustellungs Szenario bietet Benutzern die folgenden Vorteile:</span><span class="sxs-lookup"><span data-stu-id="cd6a6-111">The stand-alone delivery scenario provides users the following benefits:</span></span>

-   <span data-ttu-id="cd6a6-112">Einfacher Bereitstellungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="cd6a6-112">Simple deployment operation.</span></span>

-   <span data-ttu-id="cd6a6-113">Netzwerk und Server werden zur Laufzeit nicht benötigt.</span><span class="sxs-lookup"><span data-stu-id="cd6a6-113">Network and servers not needed at runtime.</span></span>

-   <span data-ttu-id="cd6a6-114">Anwendungen werden vorab zwischengespeichert und allen Benutzern zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="cd6a6-114">Applications pre-cached and available to all users.</span></span>

<span data-ttu-id="cd6a6-115">Für das eigenständige Zustellungs Szenario gelten die folgenden Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="cd6a6-115">The stand-alone delivery scenario has the following limitations:</span></span>

-   <span data-ttu-id="cd6a6-116">Integrierte, automatisierte Berichte sind nicht verfügbar. Berichte müssen mit externen Berichterstellungstools erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="cd6a6-116">Built-in, automated reporting is unavailable; reports must be generated with external reporting tools.</span></span>

-   <span data-ttu-id="cd6a6-117">Anwendungen müssen wie die ursprünglichen Windows Installer-Dateien manuell an den Client übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="cd6a6-117">Applications must be delivered to the client manually like the original Windows Installer files.</span></span>

## <span data-ttu-id="cd6a6-118">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="cd6a6-118">Related topics</span></span>


[<span data-ttu-id="cd6a6-119">So installieren Sie Application Virtualization Client manuell</span><span class="sxs-lookup"><span data-stu-id="cd6a6-119">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="cd6a6-120">So veröffentlichen Sie eine virtuelle Anwendung auf dem Client</span><span class="sxs-lookup"><span data-stu-id="cd6a6-120">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

 

 





