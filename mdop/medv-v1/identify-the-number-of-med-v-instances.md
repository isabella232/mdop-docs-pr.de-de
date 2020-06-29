---
title: Identifizieren Sie die Anzahl der Instanzen von MED-V
description: Identifizieren Sie die Anzahl der Instanzen von MED-V
author: dansimp
ms.assetid: edea9bdf-a28c-4d24-9298-7bd6536c3a94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22f7d54318d2dc489461474e5531c5162d8c087d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810447"
---
# <span data-ttu-id="4efb5-103">Identifizieren Sie die Anzahl der Instanzen von MED-V</span><span class="sxs-lookup"><span data-stu-id="4efb5-103">Identify the Number of MED-V Instances</span></span>


<span data-ttu-id="4efb5-104">Sie müssen die Anzahl der MED-V-Instanzen ermitteln und den Bereich für jede Instanz definieren, damit Sie die Serverinfrastruktur entwerfen können.</span><span class="sxs-lookup"><span data-stu-id="4efb5-104">You need to determine the number of MED-V instances, as well as define the scope for each instance so that you can design the server infrastructure.</span></span> <span data-ttu-id="4efb5-105">Eine MED-V-Instanz enthält Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4efb5-105">A MED-V instance includes the following:</span></span>

-   <span data-ttu-id="4efb5-106">Der Med-v-Server und die auf dem Server gespeicherten Med-v-Arbeitsbereiche, einschließlich der Active Directory-Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="4efb5-106">The MED-V server and the MED-V workspaces stored on the server, including Active Directory permissions.</span></span>

-   <span data-ttu-id="4efb5-107">Eine SQL Server-Datenbank, in der Clientereignisse gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4efb5-107">A SQL Server database that stores client events.</span></span> <span data-ttu-id="4efb5-108">Die Datenbank kann von mehreren MED-V-Instanzen freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4efb5-108">The database may be shared by multiple MED-V instances.</span></span>

-   <span data-ttu-id="4efb5-109">Das Bild-Repository für die komprimierten MED-V-Bilder.</span><span class="sxs-lookup"><span data-stu-id="4efb5-109">The image repository for the packed MED-V images.</span></span> <span data-ttu-id="4efb5-110">Das Repository kann von mehreren MED-V-Instanzen freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4efb5-110">The repository may be shared by multiple MED-V instances.</span></span>

-   <span data-ttu-id="4efb5-111">Die Verwaltungskonsole, die zum Erstellen und Verpacken von Bildern und zum Erstellen von MED-V-Arbeitsbereichen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4efb5-111">The management console used to create and pack images and to create MED-V workspaces.</span></span> <span data-ttu-id="4efb5-112">Die Konsole kann nicht gleichzeitig von mehreren Med-v-Instanzen verwendet werden, kann aber von einem Med-v-Server getrennt und dann mit einem anderen Med-v-Server verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="4efb5-112">The console cannot be used simultaneously by multiple MED-V instances, but it can be disconnected from one MED-V server and then connected to a different MED-V server.</span></span>

-   <span data-ttu-id="4efb5-113">Med-v-Clients, die Med-v-Arbeitsbereiche empfangen, und die Autorisierung, Sie vom Server zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4efb5-113">MED-V clients that receive MED-V workspaces, and authorization to use them, from the server.</span></span>

<span data-ttu-id="4efb5-114">Separate Med-v-Instanzen können nicht integriert oder Med-v-Arbeitsbereiche freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4efb5-114">Separate MED-V instances cannot be integrated or share MED-V workspaces.</span></span> <span data-ttu-id="4efb5-115">Deshalb dezentralisiert jede zusätzliche Instanz die Virtualisierungs-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="4efb5-115">Therefore, each additional instance decentralizes the virtualization management.</span></span>

## <span data-ttu-id="4efb5-116">Ermitteln der Anzahl der erforderlichen MED-V-Instanzen</span><span class="sxs-lookup"><span data-stu-id="4efb5-116">Determine the Number of MED-V Instances Required</span></span>


<span data-ttu-id="4efb5-117">Beginnen Sie mit der Annahme, dass Sie eine MED-V-Instanz verwenden.</span><span class="sxs-lookup"><span data-stu-id="4efb5-117">Start by assuming you are using one MED-V instance.</span></span> <span data-ttu-id="4efb5-118">Nehmen Sie dann die folgenden Bedingungen in Frage, und fügen Sie weitere Instanzen für jede für Ihre Infrastruktur geltende Bedingung hinzu.</span><span class="sxs-lookup"><span data-stu-id="4efb5-118">Then, consider the following conditions, and add additional instances for each condition that applies to your infrastructure.</span></span>

-   <span data-ttu-id="4efb5-119">Anzahl unterstützter Benutzer – jede MED-V-Instanz kann bis zu 5.000 gleichzeitig aktive Clients unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4efb5-119">Number of supported users—Each MED-V instance can support up to 5,000 concurrently active clients.</span></span> <span data-ttu-id="4efb5-120">Gleichzeitig aktiv bedeutet, dass der Client mit dem MED-V-Server Online ist und Umfragen an den Server sendet, um Richtlinien-und Bildaktualisierungen sowie Ereignisse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4efb5-120">Concurrently active means the client is online with the MED-V server and sending polls to the server for policy and image updates, as well as events.</span></span> <span data-ttu-id="4efb5-121">Wenn Ihre Infrastruktur mehr als 5.000 aktive Benutzer umfassen soll, fügen Sie eine Instanz für alle 5.000-Benutzer hinzu.</span><span class="sxs-lookup"><span data-stu-id="4efb5-121">If your infrastructure will include more than 5,000 active users, add one instance for every 5,000 users.</span></span>

-   <span data-ttu-id="4efb5-122">Benutzer in nicht vertrauenswürdigen Domänen – die Med-v Server Associates Med-v Workspace-Berechtigungen für Active Directory-Benutzer und/oder-Gruppen.</span><span class="sxs-lookup"><span data-stu-id="4efb5-122">Users in untrusted domains—The MED-V server associates MED-V workspace permissions with Active Directory users and/or groups.</span></span> <span data-ttu-id="4efb5-123">Dies erfordert, dass Med-v-Benutzer innerhalb der Vertrauensgrenze des Med-v-Servers vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="4efb5-123">This requires MED-V users to exist within the trust boundary of the MED-V server.</span></span> <span data-ttu-id="4efb5-124">Hinzufügen einer Med-v-Instanz für jede Gruppe von Med-v-Benutzern, die sich in einer separaten, nicht vertrauenswürdigen Domäne befindet</span><span class="sxs-lookup"><span data-stu-id="4efb5-124">Add one MED-V instance for each group of MED-V users that is in a separate, untrusted domain.</span></span>

-   <span data-ttu-id="4efb5-125">Clients in isolierten Netzwerken – ermitteln Sie, ob sich Clients in isolierten Netzwerken befinden und daher eine separate MED-V-Instanz erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4efb5-125">Clients in isolated networks—Determine whether any clients reside in networks that are isolated and therefore require a separate MED-V instance.</span></span> <span data-ttu-id="4efb5-126">Beispielsweise isolieren Organisationen häufig Lab-Netzwerke aus Produktionsnetzwerken.</span><span class="sxs-lookup"><span data-stu-id="4efb5-126">For example, organizations often isolate lab networks from production networks.</span></span> <span data-ttu-id="4efb5-127">Fügen Sie für jedes isolierte Netzwerk, das Med-v-Clients enthalten soll, eine Med-v-Instanz hinzu.</span><span class="sxs-lookup"><span data-stu-id="4efb5-127">Add a MED-V instance for each isolated network that will contain MED-V clients.</span></span>

-   <span data-ttu-id="4efb5-128">Organisatorische Anforderungen – für die Organisation kann es erforderlich sein, dass eine Gruppe von Clients aus Sicherheitsgründen von einer separaten MED-V-Instanz verwaltet wird, beispielsweise wenn vertrauliche Anwendungen nur an eine eingeschränkte Anzahl von Benutzern innerhalb einer Domäne übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="4efb5-128">Organizational requirements—The organization may require that a group of clients be managed by a separate MED-V instance for security reasons, such as when sensitive applications are delivered only to a restricted set of users within a domain.</span></span> <span data-ttu-id="4efb5-129">Beispielsweise kann die lohnabteilung Benutzern aus anderen Abteilungen den Zugriff auf die MED-V-Instanz verweigern, in der die Richtlinie für die Lohnbearbeitung gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="4efb5-129">For example, the payroll department may deny users from other departments access to the MED-V instance that stores policy for payroll processing.</span></span> <span data-ttu-id="4efb5-130">Wenn die Organisation darüber hinaus ein verteiltes Verwaltungsmodell verwendet, ist möglicherweise eine separate Med-v-Instanz für jede Unternehmensgruppe erforderlich, die Med-v-Clients hat, damit die Gruppe ihre eigene virtualisierte Umgebung verwalten kann.</span><span class="sxs-lookup"><span data-stu-id="4efb5-130">Additionally, if the organization uses a distributed management model, a separate MED-V instance may be required for each business group having MED-V clients in order to enable the group to manage its own virtualized environment.</span></span> <span data-ttu-id="4efb5-131">Fügen Sie für jede einzelne organisatorische Anforderung eine MED-V-Instanz hinzu.</span><span class="sxs-lookup"><span data-stu-id="4efb5-131">Add one MED-V instance for each separate organizational requirement.</span></span>

-   <span data-ttu-id="4efb5-132">Rechtliche Hinweise – nationale Sicherheit, Datenschutz und treuhänderische Gesetze könnten die Trennung bestimmter Daten oder die Verhinderung anderer Daten an Grenzübergängen erforderlich machen.</span><span class="sxs-lookup"><span data-stu-id="4efb5-132">Legal considerations—National security or privacy issues and fiduciary laws could require the separation of certain data or prevent other data from crossing national borders.</span></span> <span data-ttu-id="4efb5-133">Fügen Sie bei Bedarf weitere MED-V-Instanzen hinzu, um diese Anforderung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="4efb5-133">If necessary, add additional MED-V instances to address this need.</span></span>

<span data-ttu-id="4efb5-134">Nachdem Sie die Anzahl der für Ihre Infrastruktur erforderlichen MED-V-Instanzen sowie die Begründung für jede Instanz ermittelt haben, geben Sie einen Namen für jede Instanz an.</span><span class="sxs-lookup"><span data-stu-id="4efb5-134">After you determine the number of MED-V instances required for your infrastructure, as well as the reasoning for each one, provide a name for each instance.</span></span>

 

 





