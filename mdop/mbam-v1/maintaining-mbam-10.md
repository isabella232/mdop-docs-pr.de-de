---
title: Verwalten von MBAM 1.0
description: Verwalten von MBAM 1.0
author: dansimp
ms.assetid: 02ffb093-c364-4837-bbe8-23d4c09fbd3d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7eecef4e82680b08fde1b1bef88487a6fc156fe4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811356"
---
# <span data-ttu-id="00b3b-103">Verwalten von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="00b3b-103">Maintaining MBAM 1.0</span></span>


<span data-ttu-id="00b3b-104">Nachdem Sie die erforderliche Planung abgeschlossen und dann die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) bereitgestellt haben, können Sie MBAM so konfigurieren, dass es auf hoch verfügbare Weise ausgeführt wird, während Sie es zum Verwalten von BitLocker-Verschlüsselungsvorgängen in Unternehmen verwenden.</span><span class="sxs-lookup"><span data-stu-id="00b3b-104">After you complete all the necessary planning and then deploy Microsoft BitLocker Administration and Monitoring (MBAM), you can configure MBAM to run in a highly available fashion while using it to manage enterprise BitLocker encryption operations.</span></span> <span data-ttu-id="00b3b-105">In den Informationen in diesem Abschnitt werden die Optionen für die Verfügbarkeit von MBAM sowie die Möglichkeit zum Verschieben von MBAM-Server Features beschrieben.</span><span class="sxs-lookup"><span data-stu-id="00b3b-105">The information in this section describes high availability options for MBAM, as well as how to move MBAM Server features if necessary.</span></span>

## <span data-ttu-id="00b3b-106">MBAM-Management Pack</span><span class="sxs-lookup"><span data-stu-id="00b3b-106">MBAM Management Pack</span></span>


<span data-ttu-id="00b3b-107">Das MicrosoftSystemCenterOperationsManager-Management Pack für MBAM steht im Microsoft Download Center zum Download zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="00b3b-107">The MicrosoftSystemCenterOperationsManager Management Pack for MBAM is available for download from the Microsoft Download Center.</span></span>

<span data-ttu-id="00b3b-108">Dieses Management Pack überwacht die kritischen Interaktionen in der serverseitigen Infrastruktur, beispielsweise die Verbindungen zwischen den Webdiensten und-Datenbanken und den operativen Aufrufen zwischen Websites und deren unterstützenden Webdiensten.</span><span class="sxs-lookup"><span data-stu-id="00b3b-108">This management pack monitors the critical interactions in the server-side infrastructure, such as the connections between the web services and databases and the operational calls between websites and their supportive web service.</span></span> <span data-ttu-id="00b3b-109">Außerdem werden die Anforderungen zwischen Desktop Clients und den jeweiligen empfangenden Webdienstendpunkten hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="00b3b-109">It also uploads the requests between desktop clients and their respective receiving web service endpoints.</span></span>

[<span data-ttu-id="00b3b-110">Management Pack für Microsoft BitLocker-Verwaltung und-Überwachung</span><span class="sxs-lookup"><span data-stu-id="00b3b-110">Microsoft BitLocker Administration And Monitoring Management Pack</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=258390)

## <span data-ttu-id="00b3b-111">Sicherstellen einer höheren Verfügbarkeit für MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="00b3b-111">Ensure high availability for MBAM 1.0</span></span>


<span data-ttu-id="00b3b-112">MBAM ist als fehlertolerant konzipiert.</span><span class="sxs-lookup"><span data-stu-id="00b3b-112">MBAM is designed to be fault-tolerant.</span></span> <span data-ttu-id="00b3b-113">Wenn ein Server nicht mehr zur Verfügung steht, sollten die Benutzer nicht negativ beeinflusst werden.</span><span class="sxs-lookup"><span data-stu-id="00b3b-113">If a server becomes unavailable, the users should not be negatively affected.</span></span> <span data-ttu-id="00b3b-114">Die Informationen in diesem Abschnitt können zum Konfigurieren einer hoch verfügbaren MBAM-Installation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00b3b-114">The information in this section can be used to configure a highly available MBAM installation.</span></span>

[<span data-ttu-id="00b3b-115">Hohe Verfügbarkeit von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="00b3b-115">High Availability for MBAM 1.0</span></span>](high-availability-for-mbam-10.md)

## <span data-ttu-id="00b3b-116">Verschieben von MBAM 1,0-Features auf einen anderen Server</span><span class="sxs-lookup"><span data-stu-id="00b3b-116">Move MBAM 1.0 features to another server</span></span>


<span data-ttu-id="00b3b-117">Wenn Sie ein MBAM-Server Feature von einem Server Computer auf einen anderen verschieben müssen, gibt es eine bestimmte Reihenfolge und erforderliche Schritte, die Sie ausführen sollten, um Produktivitäts-oder Datenverluste zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="00b3b-117">When you need to move an MBAM Server feature from one server computer to another, there is a specific order and required steps that you should follow to avoid loss of productivity or data.</span></span> <span data-ttu-id="00b3b-118">In diesem Abschnitt werden die Schritte beschrieben, die Sie ausführen müssen, um ein oder mehrere MBAM-Server Features auf einen anderen Computer zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="00b3b-118">This section describes the steps that you should take to move one or more MBAM Server features to a different computer.</span></span>

[<span data-ttu-id="00b3b-119">Vorgehensweise beim Verschieben von MBAM 1.0-Funktionen auf einen anderen Computer</span><span class="sxs-lookup"><span data-stu-id="00b3b-119">How to Move MBAM 1.0 Features to Another Computer</span></span>](how-to-move-mbam-10-features-to-another-computer.md)

## <span data-ttu-id="00b3b-120">Weitere Ressourcen zum Verwalten von MBAM</span><span class="sxs-lookup"><span data-stu-id="00b3b-120">Other resources for maintaining MBAM</span></span>


[<span data-ttu-id="00b3b-121">Vorgänge für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="00b3b-121">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





