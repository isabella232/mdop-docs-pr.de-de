---
title: Unterbrochener Betriebsmodus
description: Unterbrochener Betriebsmodus
author: dansimp
ms.assetid: 3f9849ea-ba53-4c68-85d3-87a4218f59c6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6e9534b93f23b17e5258ef5e2d548eb93213f2f8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808866"
---
# <span data-ttu-id="8cb9e-103">Unterbrochener Betriebsmodus</span><span class="sxs-lookup"><span data-stu-id="8cb9e-103">Disconnected Operation Mode</span></span>


<span data-ttu-id="8cb9e-104">Die Einstellungen für den getrennten Betriebsmodus – Barrierefrei, indem Sie mit der rechten Maustaste auf den Knoten **Application Virtualization** klicken, **Eigenschaften**auswählen und auf die Registerkarte **Konnektivität** klicken – ermöglicht es dem Application Virtualization Desktop Client oder-Client für Remote Desktop Dienste (ehemals Terminal Dienste), Anwendungen auszuführen, die im Dateisystemcache des Clients gespeichert sind, wenn der Client keine Verbindung mit dem Application Virtualization Management Server herstellen kann</span><span class="sxs-lookup"><span data-stu-id="8cb9e-104">The disconnected operation mode settings—accessible by right-clicking the **Application Virtualization** node, selecting **Properties**, and clicking the **Connectivity** tab—enables the Application Virtualization Desktop Client or Client for Remote Desktop Services (formerly Terminal Services) to run applications that are stored in the file system cache of the client when the client is unable to connect to the Application Virtualization Management Server.</span></span>

<span data-ttu-id="8cb9e-105">Gründe für die fehlerhafte Verbindung mit dem Server sind Serverfehler, Netzwerkausfälle oder die Trennung vom Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="8cb9e-105">Reasons for failure to connect to the server include server failure, network outage, or disconnection from the network.</span></span> <span data-ttu-id="8cb9e-106">Wenn ein Fehler auftritt, wechselt der Client automatisch in den getrennten Betrieb.</span><span class="sxs-lookup"><span data-stu-id="8cb9e-106">If any failure occurs, the client will automatically switch to disconnected operation.</span></span> <span data-ttu-id="8cb9e-107">Wenn der Client nach dem Trennen der Verbindung zusätzliche Daten vom Server benötigt, um weiterhin eine Anwendung auszuführen, oder wenn das Timeout des getrennten Vorgangs abgelaufen ist, versucht der Client erneut, eine Verbindung mit dem Server herzustellen.</span><span class="sxs-lookup"><span data-stu-id="8cb9e-107">After it is disconnected, if the client needs additional data from the server to continue to run an application or if the disconnected operation time-out expires, the client will attempt to reconnect to the server.</span></span> <span data-ttu-id="8cb9e-108">Wenn dieser Verbindungsversuch fehlschlägt, wird die Anwendung beendet.</span><span class="sxs-lookup"><span data-stu-id="8cb9e-108">If this connection attempt fails, the application will be shut down.</span></span>

<span data-ttu-id="8cb9e-109">Standardmäßig ist der getrennte Vorgang aktiviert, und das Timeout ist auf 90 Tage festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8cb9e-109">By default, disconnected operation is enabled and the time-out is set to 90 days.</span></span> <span data-ttu-id="8cb9e-110">Der Timeoutwert wird als die Anzahl der Tage angegeben, die Sie den unterbrochenen Betriebsmodus begrenzen möchten, und Sie können einen Wert von 1 bis 999 eingeben.</span><span class="sxs-lookup"><span data-stu-id="8cb9e-110">The time-out value is specified as the number of days you want to limit disconnected operation mode, and you can enter a value from 1–999.</span></span>

## <span data-ttu-id="8cb9e-111">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="8cb9e-111">Related topics</span></span>


[<span data-ttu-id="8cb9e-112">So deaktivieren oder ändern Sie Einstellungen für den unterbrochenen Betriebsmodus</span><span class="sxs-lookup"><span data-stu-id="8cb9e-112">How to Disable or Modify Disconnected Operation Mode Settings</span></span>](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 





