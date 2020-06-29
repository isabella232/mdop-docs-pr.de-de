---
title: Konfigurieren von App-V-Verwaltung für eine verteilte Umgebung
description: Konfigurieren von App-V-Verwaltung für eine verteilte Umgebung
author: dansimp
ms.assetid: 53971fa9-8319-435c-be74-c37feb9af1da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c1a638d6afde9270859c8aa98fc9f421c39cfc72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809040"
---
# <span data-ttu-id="e9eb6-103">Konfigurieren von App-V-Verwaltung für eine verteilte Umgebung</span><span class="sxs-lookup"><span data-stu-id="e9eb6-103">Configuring App-V Administration for a Distributed Environment</span></span>


<span data-ttu-id="e9eb6-104">Wenn Sie die Infrastruktur für Ihre spezifische Organisation entwerfen, können Sie den App-v Management Web Service auf einem anderen Computer als dem Computer installieren, auf dem Sie den App-v-Verwaltungs Server installieren.</span><span class="sxs-lookup"><span data-stu-id="e9eb6-104">When designing the infrastructure for your specific organization, you can install the App-V Management Web Service on a computer other than the computer where you install the App-V Management Server.</span></span> <span data-ttu-id="e9eb6-105">Häufige Gründe für die Trennung dieser App-V-Komponenten sind die folgenden:</span><span class="sxs-lookup"><span data-stu-id="e9eb6-105">Common reasons for separating these App-V components include the following:</span></span>

-   <span data-ttu-id="e9eb6-106">Leistung</span><span class="sxs-lookup"><span data-stu-id="e9eb6-106">Performance</span></span>

-   <span data-ttu-id="e9eb6-107">Zuverlässigkeit</span><span class="sxs-lookup"><span data-stu-id="e9eb6-107">Reliability</span></span>

-   <span data-ttu-id="e9eb6-108">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="e9eb6-108">Availability</span></span>

-   <span data-ttu-id="e9eb6-109">Skalierbarkeit</span><span class="sxs-lookup"><span data-stu-id="e9eb6-109">Scalability</span></span>

<span data-ttu-id="e9eb6-110">Das Trennen des Verwaltungsservers und des Verwaltungs-Webdiensts erfordert eine zusätzliche Konfiguration für die ordnungsgemäße Funktionsweise der Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="e9eb6-110">Separating the Management Server and Management Web Service requires additional configuration for the infrastructure to operate correctly.</span></span> <span data-ttu-id="e9eb6-111">Wenn Sie diese beiden Features trennen, aber die in diesem Thema beschriebenen Verfahren nicht ausführen, stellt die Verwaltungskonsole eine Verbindung mit dem Verwaltungs-Webdienst her, kann sich aber nicht ordnungsgemäß mit dem Datenspeicher authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="e9eb6-111">When you separate these two features but do not complete the procedures described in this topic, the Management Console will connect to the Management Web Service but will not be able to properly authenticate with the data store.</span></span> <span data-ttu-id="e9eb6-112">Die Verwaltungskonsole wird nicht ordnungsgemäß geladen, und der Administrator kann keine administrativen Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="e9eb6-112">The Management Console will not load properly, and the administrator will not be able to complete any administrative tasks.</span></span>

<span data-ttu-id="e9eb6-113">Dieses Verhalten tritt auf, weil der Verwaltungs Webdienst die Anmeldeinformationen, die an ihn über die Verwaltungskonsole übergeben werden, nicht verwenden kann, um auf den Datenspeicher zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="e9eb6-113">This behavior occurs because the Management Web Service cannot use the credentials, passed to it from the Management Console, to access the data store.</span></span> <span data-ttu-id="e9eb6-114">Die Lösung besteht darin, den Management Web Service-Server so zu konfigurieren, dass er "für Delegierungszwecke vertraut" ist.</span><span class="sxs-lookup"><span data-stu-id="e9eb6-114">The solution is to configure the Management Web Service server to be “Trusted for delegation.”</span></span>

## <span data-ttu-id="e9eb6-115">Konfigurieren von Active Directory-Domänendiensten</span><span class="sxs-lookup"><span data-stu-id="e9eb6-115">Configuring Active Directory Domain Services</span></span>


<span data-ttu-id="e9eb6-116">Darüber hinaus ist es erforderlich, die Active Directory-Domänendienste ordnungsgemäß für die Arbeit in einer verteilten Umgebung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e9eb6-116">It is also necessary to configure Active Directory Domain Services properly to work in a distributed environment.</span></span> <span data-ttu-id="e9eb6-117">Dieser Abschnitt enthält die Informationen, die Sie benötigen, um die Active Directory-Domänendienste zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e9eb6-117">This section includes the information you need configure Active Directory Domain Services.</span></span>

### <span data-ttu-id="e9eb6-118">Wenn der SQL-Dienst lokales System Konto verwendet</span><span class="sxs-lookup"><span data-stu-id="e9eb6-118">When SQL Service Uses Local System account</span></span>

<span data-ttu-id="e9eb6-119">Wenn Sie die Umgebung einrichten möchten, in der der SQL-Dienst das lokale Systemkonto verwendet, ändern Sie die Eigenschaften des Computerkontos des Verwaltungs-Webdiensts, damit es für die Delegierung als vertrauenswürdig eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="e9eb6-119">To set up the environment where the SQL Service uses the local system account, change the properties of the machine account of the Management Web Service to be trusted for delegation.</span></span> <span data-ttu-id="e9eb6-120">Detaillierte Verfahren zur Vorgehensweise finden Sie unter [so wird es gemacht: Konfigurieren des Servers für die Delegierung als vertrauenswürdig](how-to-configure-the-server-to-be-trusted-for-delegation.md)</span><span class="sxs-lookup"><span data-stu-id="e9eb6-120">For detailed procedures about how to do this, see [How to Configure the Server to be Trusted for Delegation](how-to-configure-the-server-to-be-trusted-for-delegation.md)</span></span>

### <span data-ttu-id="e9eb6-121">Wenn der SQL-Dienstdomänen basiertes Konto verwendet</span><span class="sxs-lookup"><span data-stu-id="e9eb6-121">When SQL Service Uses Domain-Based Account</span></span>

<span data-ttu-id="e9eb6-122">Zum Einrichten der Umgebung, in der SQL-Server domänenbasierte Dienstkonten verwenden, müssen Sie berücksichtigen, ob eine Vielzahl von Faktoren gelten soll, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="e9eb6-122">To set up the environment where SQL Servers use domain-based service accounts, you need to consider whether or not a variety of factors apply, including the following:</span></span>

-   <span data-ttu-id="e9eb6-123">Clustering von SQL Server</span><span class="sxs-lookup"><span data-stu-id="e9eb6-123">Clustering of SQL Server</span></span>

-   <span data-ttu-id="e9eb6-124">Replikation</span><span class="sxs-lookup"><span data-stu-id="e9eb6-124">Replication</span></span>

-   <span data-ttu-id="e9eb6-125">Automatisierte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="e9eb6-125">Automated tasks</span></span>

-   <span data-ttu-id="e9eb6-126">Verknüpfte Server</span><span class="sxs-lookup"><span data-stu-id="e9eb6-126">Linked servers</span></span>

<span data-ttu-id="e9eb6-127">Informationen zum Konfigurieren von Active Directory-Domänendiensten, wenn der SQL-Dienst ein domänenbasiertes Konto verwendet, finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=151968> .</span><span class="sxs-lookup"><span data-stu-id="e9eb6-127">For information about configuring Active Directory Domain Services when the SQL service uses a domain-based account, see <https://go.microsoft.com/fwlink/?LinkId=151968>.</span></span>

 

 





