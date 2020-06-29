---
title: Hohe Verfügbarkeit von MBAM 1.0
description: Hohe Verfügbarkeit von MBAM 1.0
author: dansimp
ms.assetid: 5869ecf8-1056-4c32-aecb-838a37e05d39
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1227967d647cbfbc16967b5936066fd73d2412e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811110"
---
# <span data-ttu-id="07be7-103">Hohe Verfügbarkeit von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="07be7-103">High Availability for MBAM 1.0</span></span>


<span data-ttu-id="07be7-104">In diesem Thema wird beschrieben, wie Sie eine hoch verfügbare Installation von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="07be7-104">This topic describes how to configure a highly available installation of Microsoft BitLocker Administration and Monitoring (MBAM).</span></span>

## <span data-ttu-id="07be7-105">Szenarien für die Höchstverfügbarkeit für MBAM</span><span class="sxs-lookup"><span data-stu-id="07be7-105">High Availability Scenarios for MBAM</span></span>


<span data-ttu-id="07be7-106">Die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) wurde als fehlertolerant konzipiert.</span><span class="sxs-lookup"><span data-stu-id="07be7-106">Microsoft BitLocker Administration and Monitoring (MBAM) is designed to be fault-tolerant.</span></span> <span data-ttu-id="07be7-107">Wenn ein Server nicht mehr zur Verfügung steht, sollten die Benutzer nicht negativ beeinflusst werden.</span><span class="sxs-lookup"><span data-stu-id="07be7-107">If a server becomes unavailable, the users should not be negatively affected.</span></span> <span data-ttu-id="07be7-108">Wenn beispielsweise der MBAM-Agent keine Verbindung mit dem MBAM-Webserver herstellen kann, sollten Benutzer nicht zur Eingabe einer Aktion aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="07be7-108">For example, if the MBAM agent cannot connect to the MBAM web server, users should not be prompted for action.</span></span>

<span data-ttu-id="07be7-109">Berücksichtigen Sie bei der Planung Ihrer MBAM-Installation die folgenden Bedenken, die sich auf die Verfügbarkeit des MBAM-Diensts auswirken können:</span><span class="sxs-lookup"><span data-stu-id="07be7-109">When you plan your MBAM installation, consider the following concerns that can affect the availability of the MBAM service:</span></span>

-   <span data-ttu-id="07be7-110">Laufwerksverschlüsselung und Wiederherstellungskennwort – wenn ein Wiederherstellungskennwort nicht über einen Treuhandservice verfügt, wird die Verschlüsselung auf dem Clientcomputer nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="07be7-110">Drive encryption and recovery password – If a recovery password cannot be escrowed, the encryption will not start on the client computer.</span></span>

-   <span data-ttu-id="07be7-111">Upload von Kompatibilitätsstatus Daten – Wenn der Server, auf dem der Kompatibilitätsstatus-Berichtsdienst gehostet wird, nicht verfügbar ist, bleiben die Kompatibilitätsdaten nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="07be7-111">Compliance status data upload – If the server that hosts the compliance status report service is not available, the compliance data will not remain current.</span></span>

-   <span data-ttu-id="07be7-112">Help Desk-Wiederherstellungsschlüssel Zugriff – wenn der Helpdesk nicht auf MBAM-Datenbankinformationen zugreifen kann, können Sie den Benutzern keine Wiederherstellungsschlüssel zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="07be7-112">Help Desk recovery key access - If the Help Desk cannot access MBAM database information, they will be unable to provide recovery keys to users.</span></span>

-   <span data-ttu-id="07be7-113">Verfügbarkeit von Berichten – Berichte stehen nicht zur Verfügung, wenn der Server, auf dem die Konformitäts-und Überwachungsberichte gehostet werden, nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="07be7-113">Availability of reports – Reports will not be available if the server that hosts the Compliance and Audit Reports is not available.</span></span>

<span data-ttu-id="07be7-114">Das Hauptproblem bei der MBAM-Höchstverfügbarkeit ist die Verfügbarkeit der BitLocker-Schlüsselwiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="07be7-114">The main concern for MBAM high availability is BitLocker key recovery availability.</span></span> <span data-ttu-id="07be7-115">Wenn der Helpdesk keine Wiederherstellungsschlüssel bereitstellen kann, können Benutzer, die gesperrt sind, ihre Computer nicht entsperren.</span><span class="sxs-lookup"><span data-stu-id="07be7-115">If the help desk cannot provide recovery keys, users who are locked out cannot unlock their computers.</span></span> <span data-ttu-id="07be7-116">Um dieses Problem zu vermeiden, sollten Sie redundante Webserver und Datenbanken implementieren, um eine optimale Verfügbarkeit zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="07be7-116">To avoid this problem, consider implementing redundant web servers and databases to ensure high availability.</span></span>

<span data-ttu-id="07be7-117">Weitere Informationen zur MBAM-Skalierbarkeit und zu einer höheren Verfügbarkeit finden Sie unter [Whitepaper zur MBAM-Skalierbarkeit](https://go.microsoft.com/fwlink/p/?LinkId=229025) ( https://go.microsoft.com/fwlink/p/?LinkId=229025) .</span><span class="sxs-lookup"><span data-stu-id="07be7-117">For more information about MBAM scalability and high availability, see the [MBAM Scalability White Paper](https://go.microsoft.com/fwlink/p/?LinkId=229025) (https://go.microsoft.com/fwlink/p/?LinkId=229025).</span></span>

<span data-ttu-id="07be7-118">Allgemeine Anleitungen zur Hochverfügbarkeits-Verfügbarkeit für Microsoft SQL Server finden Sie unter [Höchstverfügbarkeit](https://go.microsoft.com/fwlink/p/?LinkId=221504) ( https://go.microsoft.com/fwlink/p/?LinkId=221504) .</span><span class="sxs-lookup"><span data-stu-id="07be7-118">For general guidance on high availability for Microsoft SQL Server, see [High Availability](https://go.microsoft.com/fwlink/p/?LinkId=221504) (https://go.microsoft.com/fwlink/p/?LinkId=221504).</span></span>

<span data-ttu-id="07be7-119">Allgemeine Anleitungen zur Verfügbarkeit und Skalierbarkeit für Webserver finden Sie unter [Verfügbarkeit und Skalierbarkeit](https://go.microsoft.com/fwlink/p/?LinkId=221503) ( https://go.microsoft.com/fwlink/p/?LinkId=221503) .</span><span class="sxs-lookup"><span data-stu-id="07be7-119">For general guidance on availability and scalability for web servers, see [Availability and Scalability](https://go.microsoft.com/fwlink/p/?LinkId=221503) (https://go.microsoft.com/fwlink/p/?LinkId=221503).</span></span>

## <span data-ttu-id="07be7-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="07be7-120">Related topics</span></span>


[<span data-ttu-id="07be7-121">Verwalten von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="07be7-121">Maintaining MBAM 1.0</span></span>](maintaining-mbam-10.md)

 

 





