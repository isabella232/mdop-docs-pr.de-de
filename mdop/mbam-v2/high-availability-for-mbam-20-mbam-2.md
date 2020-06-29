---
title: Hohe Verfügbarkeit von MBAM 2.0
description: Hohe Verfügbarkeit von MBAM 2.0
author: dansimp
ms.assetid: 244ee013-9e2a-48d2-b842-4e10594fd74f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6482a099d96aee731f81368b8b787325e592c453
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810729"
---
# <span data-ttu-id="66176-103">Hohe Verfügbarkeit von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="66176-103">High Availability for MBAM 2.0</span></span>


<span data-ttu-id="66176-104">Dieses Thema enthält grundlegende Informationen zu einer hoch verfügbaren Installation von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM).</span><span class="sxs-lookup"><span data-stu-id="66176-104">This topic provides basic information about a highly available installation of Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="66176-105">Szenarien mit hoher Verfügbarkeit werden in dieser Version von MBAM nicht vollständig unterstützt, daher werden Sie hier nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="66176-105">High-availability scenarios are not fully supported in this version of MBAM, so they are not described here.</span></span> <span data-ttu-id="66176-106">Es wird empfohlen, Verwandte Blogs und Foren zu durchsuchen, in denen Benutzer beschreiben, wie Sie die Höchstverfügbarkeit für MBAM in ihren Umgebungen erfolgreich konfiguriert haben.</span><span class="sxs-lookup"><span data-stu-id="66176-106">It is recommended that you search related blogs and forums, where users describe how they have successfully configured high availability for MBAM in their environments.</span></span>

## <span data-ttu-id="66176-107">Szenarien für die Höchstverfügbarkeit für MBAM</span><span class="sxs-lookup"><span data-stu-id="66176-107">High Availability Scenarios for MBAM</span></span>


<span data-ttu-id="66176-108">Die Microsoft BitLocker-Verwaltung und-Überwachung wurde als fehlertolerant konzipiert.</span><span class="sxs-lookup"><span data-stu-id="66176-108">Microsoft BitLocker Administration and Monitoring is designed to be fault-tolerant.</span></span> <span data-ttu-id="66176-109">Wenn ein Server nicht mehr zur Verfügung steht, sollten die Benutzer nicht negativ beeinflusst werden.</span><span class="sxs-lookup"><span data-stu-id="66176-109">If a server becomes unavailable, users should not be negatively affected.</span></span> <span data-ttu-id="66176-110">Wenn beispielsweise der MBAM-Agent keine Verbindung mit dem MBAM-Webserver herstellen kann, sollten Benutzer nicht zur Eingabe einer Aktion aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="66176-110">For example, if the MBAM agent cannot connect to the MBAM web server, users should not be prompted for action.</span></span>

<span data-ttu-id="66176-111">Wenn Sie Ihre MBAM-Installation planen, sollten Sie die folgenden Elemente in Frage stellen, die sich auf die Verfügbarkeit des MBAM-Diensts auswirken können:</span><span class="sxs-lookup"><span data-stu-id="66176-111">When you plan your MBAM installation, consider the following items, which can affect the availability of the MBAM service:</span></span>

-   <span data-ttu-id="66176-112">Laufwerksverschlüsselung und Wiederherstellungskennwort – wenn ein Wiederherstellungskennwort nicht über einen Treuhandservice verfügt, wird die Verschlüsselung nicht auf dem Clientcomputer gestartet.</span><span class="sxs-lookup"><span data-stu-id="66176-112">Drive encryption and recovery password – If a recovery password cannot be escrowed, the encryption does not start on the client computer.</span></span>

-   <span data-ttu-id="66176-113">Upload von Kompatibilitätsstatus Daten – Wenn der Server, auf dem der Kompatibilitätsstatus-Berichtsdienst gehostet wird, nicht verfügbar ist, bleiben die Kompatibilitätsdaten nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="66176-113">Compliance status data upload – If the server that hosts the compliance status report service is not available, the compliance data does not remain current.</span></span>

-   <span data-ttu-id="66176-114">Zugriff auf Helpdesk-Wiederherstellungsschlüssel – wenn der Helpdesk nicht auf Informationen zu MBAM-Datenbanken zugreifen kann, kann der Helpdesk keine Wiederherstellungsschlüssel für Benutzer bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="66176-114">Help Desk recovery key access - If the Help Desk cannot access MBAM database information, the Help Desk cannot provide recovery keys to users.</span></span>

-   <span data-ttu-id="66176-115">Verfügbarkeit von Berichten – wenn der Server, auf dem die Konformitäts-und Überwachungsberichte gehostet werden, nicht verfügbar ist, stehen Berichte nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="66176-115">Availability of reports –If the server that hosts the Compliance and Audit Reports is not available, reports will not be available.</span></span>

## <a href="" id="how-the-mbam-backup-uses-the-volume-shadow-copy-service--vss--"></a><span data-ttu-id="66176-116">Verwendung des Volumeschattenkopie-Diensts (Volume Shadow Copy Service, VSS) durch die MBAM-Sicherung</span><span class="sxs-lookup"><span data-stu-id="66176-116">How the MBAM Backup Uses the Volume Shadow Copy Service (VSS)</span></span>


<span data-ttu-id="66176-117">Mbam 2.0 bietet einen VSS-Writer (Volume Shadow Copy Service) mit dem Namen Microsoft BitLocker-Verwaltungs-und-Verwaltungs-Writer, der die Sicherung der Compliance-und Überwachungsdatenbank sowie der Wiederherstellungsdatenbank vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="66176-117">MBAM2.0 provides a Volume Shadow Copy Service (VSS) writer, called the Microsoft BitLocker Administration and Management Writer, which facilitates the backup of the Compliance and Audit Database and the Recovery Database.</span></span>

<span data-ttu-id="66176-118">Der MBAM-Server Windows Installer registriert den MBAM-VSS-Writer.</span><span class="sxs-lookup"><span data-stu-id="66176-118">The MBAM Server Windows Installer registers the MBAM VSS Writer.</span></span> <span data-ttu-id="66176-119">Jeder Fehler während der VSS-Writer-Registrierung führt dazu, dass die MBAM-Server Installation zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="66176-119">Any failure during the VSS writer registration causes the MBAM Server installation to roll back.</span></span> <span data-ttu-id="66176-120">In einer Topologie, in der die Kompatibilitäts-und Überwachungsdatenbank sowie die Wiederherstellungsdatenbank auf unterschiedlichen Servern installiert sind, wird eine separate Instanz von MBAM VSS Writer auf jedem Server registriert.</span><span class="sxs-lookup"><span data-stu-id="66176-120">In a topology where the Compliance and Audit Database and the Recovery Database are installed on different servers, a separate instance of MBAM VSS Writer is registered on each server.</span></span> <span data-ttu-id="66176-121">Der MBAM-VSS-Writer ist vom SQL Server VSS-Writer abhängig.</span><span class="sxs-lookup"><span data-stu-id="66176-121">The MBAM VSS Writer is dependent on the SQL Server VSS Writer.</span></span> <span data-ttu-id="66176-122">Der SQL Server-VSS-Writer wird als Teil der Microsoft SQL Server-Installation registriert.</span><span class="sxs-lookup"><span data-stu-id="66176-122">The SQL Server VSS Writer is registered as part of the Microsoft SQL Server installation.</span></span> <span data-ttu-id="66176-123">Jede Sicherungstechnologie, die VSS-Writer zum Durchführen einer Sicherung verwendet, kann den MBAM VSS-Writer ermitteln.</span><span class="sxs-lookup"><span data-stu-id="66176-123">Any backup technology that uses VSS writers to perform backup can discover the MBAM VSS Writer.</span></span>

## <span data-ttu-id="66176-124">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="66176-124">Related topics</span></span>


[<span data-ttu-id="66176-125">Verwalten von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="66176-125">Maintaining MBAM 2.0</span></span>](maintaining-mbam-20-mbam-2.md)

 

 





