---
title: Informationen zur Anwendungslizenzierung
description: Informationen zur Anwendungslizenzierung
author: dansimp
ms.assetid: 6b487641-1627-4e91-b829-04f001008176
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546bc630b95fe52f960c7bdfb771d3e2561f9318
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808171"
---
# <span data-ttu-id="43773-103">Informationen zur Anwendungslizenzierung</span><span class="sxs-lookup"><span data-stu-id="43773-103">About Application Licensing</span></span>


<span data-ttu-id="43773-104">Sie können Anwendungslizenzen direkt in der Application Virtualization Server-Verwaltungskonsole verwalten.</span><span class="sxs-lookup"><span data-stu-id="43773-104">You can manage application licenses directly from the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="43773-105">Lizenztypen</span><span class="sxs-lookup"><span data-stu-id="43773-105">License Types</span></span>


<span data-ttu-id="43773-106">Das System Center Application Virtualization-System unterstützt derzeit die folgenden Lizenztypen:</span><span class="sxs-lookup"><span data-stu-id="43773-106">The System Center Application Virtualization System currently supports the following license types:</span></span>

-   <span data-ttu-id="43773-107">**Unbegrenzte Lizenz**– ermöglicht den Zugriff auf die Anwendung durch eine beliebige Anzahl von gleichzeitigen Benutzern.</span><span class="sxs-lookup"><span data-stu-id="43773-107">**Unlimited License**—Allows access to the application by any number of simultaneous users.</span></span> <span data-ttu-id="43773-108">Diese Lizenzierungsmethode ist geeignet, wenn Sie einer Anwendung eine unternehmensweite Lizenz zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="43773-108">This method of licensing is appropriate when you want to associate an enterprise-wide license with an application.</span></span>

-   <span data-ttu-id="43773-109">**Concurrent License**– ermöglicht Ihnen, die maximale Anzahl von gleichzeitigen Benutzern zu definieren, die die Anwendung verwenden dürfen.</span><span class="sxs-lookup"><span data-stu-id="43773-109">**Concurrent License**—Enables you to define the maximum number of concurrent users who are allowed to use the application.</span></span>

-   <span data-ttu-id="43773-110">**Benannte Lizenz**– ermöglicht Ihnen, einem einzelnen Benutzer eine Lizenz zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="43773-110">**Named License**—Enables you to assign a license to an individual user.</span></span> <span data-ttu-id="43773-111">Eine benannte Lizenz kann verwendet werden, um sicherzustellen, dass ein bestimmter Benutzer immer in der Lage ist, die Anwendung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="43773-111">A named license can be used to ensure that a particular user will always be able to run the application.</span></span>

<span data-ttu-id="43773-112">Sie können gleichzeitige und benannte Lizenzen für dieselbe Anwendung kombinieren.</span><span class="sxs-lookup"><span data-stu-id="43773-112">You can combine concurrent and named licenses for the same application.</span></span>

<span data-ttu-id="43773-113">Die Lizenzierung ist standardmäßig deaktiviert, kann aber über die Registerkarte **Anbieter Pipeline** im Dialogfeld **Anbietereigenschaften** aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="43773-113">Licensing is disabled by default, but you can enable it from the **Provider Pipeline** tab of the **Provider Properties** dialog.</span></span> <span data-ttu-id="43773-114">Details zum Aktivieren und Deaktivieren der Lizenzierung finden Sie unter [so wird es gemacht: Einrichten oder Deaktivieren der Anwendungslizenzierung](how-to-set-up-or-disable-application-licensing.md).</span><span class="sxs-lookup"><span data-stu-id="43773-114">For details about enabling and disabling licensing, see [How to Set Up or Disable Application Licensing](how-to-set-up-or-disable-application-licensing.md).</span></span>

## <span data-ttu-id="43773-115">Anbieterrichtlinien</span><span class="sxs-lookup"><span data-stu-id="43773-115">Provider Policies</span></span>


<span data-ttu-id="43773-116">Für das ASP-Modell (Application Service Provider) wurden Anbieterrichtlinien entwickelt.</span><span class="sxs-lookup"><span data-stu-id="43773-116">Provider policies were developed for the Application Service Provider (ASP) model.</span></span> <span data-ttu-id="43773-117">In diesem Modell kann eine einzelne ASP-Anwendung ein einzelnes Application Virtualization-System für mehrere Clients hosten, wobei jeder Client isoliert bleiben muss.</span><span class="sxs-lookup"><span data-stu-id="43773-117">In this model, a single ASP can host a single Application Virtualization System for multiple clients, where each client needs to remain isolated.</span></span> <span data-ttu-id="43773-118">Clients haben möglicherweise unterschiedliche Anforderungen – beispielsweise kann ein Client eine Authentifizierung erfordern, während eine andere nicht.</span><span class="sxs-lookup"><span data-stu-id="43773-118">Clients might have dramatically different requirements—for example, one client might require authentication while another does not.</span></span> <span data-ttu-id="43773-119">Sie können Anbieterrichtlinien verwenden, um Berechtigungen für Clients zuzuordnen, damit nur die genehmigten Benutzer auf die einzelnen virtuellen Anwendungen oder virtuellen Anwendungspakete zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="43773-119">You can use provider policies to associate permissions with clients so that only the approved users can access each virtual application or virtual application package.</span></span>

<span data-ttu-id="43773-120">Für den Unternehmenskunden können Sie dieses Feature verwenden, wenn Sie über strenge Lizenzierungsanforderungen für eine oder mehrere Anwendungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="43773-120">For the enterprise customer, you can use this feature when you have strict licensing requirements for one or more applications.</span></span> <span data-ttu-id="43773-121">In diesem Fall ist die Lizenzierungskomponente auf der Registerkarte **Anbieter Pipeline** im Dialogfeld **Anbietereigenschaften** deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="43773-121">Under this situation, the licensing component is disabled on the **Provider Pipeline** tab of the **Provider Properties** dialog.</span></span>

<span data-ttu-id="43773-122">Die Registerkarte **Anbieter Pipeline** enthält ebenfalls Kontrollkästchen zum Aktivieren der Authentifizierung, Autorisierung (**Zugriffsberechtigungseinstellungen erzwingen**) und Dosierung (**Protokoll Nutzungsinformationen**).</span><span class="sxs-lookup"><span data-stu-id="43773-122">The **Provider Pipeline** tab also has check boxes to enable authentication, authorization (**Enforce Access Permission Settings**), and metering (**Log Usage Information**).</span></span> <span data-ttu-id="43773-123">Wenn Ihre Konfiguration besondere Anforderungen hat, können Sie Ihre eigenen Pipelinekomponenten schreiben und dem System hinzufügen, indem Sie auf die Schaltfläche **erweitert** klicken.</span><span class="sxs-lookup"><span data-stu-id="43773-123">If your configuration has special requirements, you can write your own pipeline components and add them to the system by clicking the **Advanced** button.</span></span>

## <span data-ttu-id="43773-124">Konto Verwaltungen</span><span class="sxs-lookup"><span data-stu-id="43773-124">Account Authorities</span></span>


<span data-ttu-id="43773-125">Die Konto Berechtigung ist die Domäne, in der der Application Virtualization Server installiert ist.</span><span class="sxs-lookup"><span data-stu-id="43773-125">The account authority is the domain in which the Application Virtualization Server is installed.</span></span> <span data-ttu-id="43773-126">Wenn Sie die Server Installation durchlaufen, werden Sie aufgefordert, einen Domänennamen anzugeben. die Domäne, in der der Computer installiert ist, wird standardmäßig erkannt und verwendet.</span><span class="sxs-lookup"><span data-stu-id="43773-126">As you proceed through the server installation, you are prompted to supply a domain name; the domain in which the computer is installed is detected and used by default.</span></span> <span data-ttu-id="43773-127">Wenn Benutzer versuchen, sich beim System anzumelden, werden Sie aufgefordert, Ihre Anmeldeinformationen einzugeben, bevor Sie auf diese Domäne zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="43773-127">When users attempt to log in to the system, they are prompted for their credentials before they can access that domain.</span></span>

<span data-ttu-id="43773-128">Das Application Virtualization System unterstützt mehrere Domänen.</span><span class="sxs-lookup"><span data-stu-id="43773-128">The Application Virtualization System supports multiple domains.</span></span> <span data-ttu-id="43773-129">Sie können Anwendungszugriff auf Benutzergruppen in anderen Domänen gewähren, wenn zwischen Domänen eine Vertrauensstellung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="43773-129">You can grant application access to user groups in other domains if a trust relationship is established between domains.</span></span> <span data-ttu-id="43773-130">Benutzer müssen Anmeldeinformationen angeben, die von jeder Domäne erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="43773-130">Users must supply credentials that are recognized by each domain.</span></span>

<span data-ttu-id="43773-131">In der Application Virtualization Server-Verwaltungskonsole können Sie die primäre Domäne (Kontoautorität) und die Anmeldeinformationen ändern, die für den Zugriff verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43773-131">In the Application Virtualization Server Management Console, you can change the primary domain (account authority) and the credentials that are used to access it.</span></span>

## <span data-ttu-id="43773-132">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="43773-132">Authentication</span></span>


<span data-ttu-id="43773-133">Authentifizierung ist der Mechanismus, der zum Bestätigen der Identität eines Benutzers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="43773-133">Authentication is the mechanism used to confirm a user's identity.</span></span> <span data-ttu-id="43773-134">Jeder Benutzer mit einem anerkannten Benutzernamen und Kennwort hat Zugriff.</span><span class="sxs-lookup"><span data-stu-id="43773-134">Any user with a recognized user name and password has access.</span></span>

<span data-ttu-id="43773-135">Im Application Virtualization System können Sie die Authentifizierung über ein Kontrollkästchen auf der Registerkarte **Anbieter Pipeline** aktivieren oder deaktivieren. Standardmäßig ist die Windows-Authentifizierung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="43773-135">In the Application Virtualization System, you can enable or disable authentication through a check box on the **Provider Pipeline** tab. By default, Windows Authentication is enabled.</span></span>

## <span data-ttu-id="43773-136">Autorisierung</span><span class="sxs-lookup"><span data-stu-id="43773-136">Authorization</span></span>


<span data-ttu-id="43773-137">Autorisierung ist der Prozess, der zum Bestätigen der Identität eines Benutzers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="43773-137">Authorization is the process used to confirm a user’s identity.</span></span> <span data-ttu-id="43773-138">Nach der Bestätigung der Identität des Benutzers ermittelt das System, ob dem Benutzer Zugriff auf das System gewährt wurde und welchen Anwendungen der Benutzer Zugriff gewährt wurde.</span><span class="sxs-lookup"><span data-stu-id="43773-138">After confirming the user's identity, the system determines whether the user was granted access to the system and to which applications the user was granted access.</span></span> <span data-ttu-id="43773-139">Die Application Virtualization Server-Verwaltungskonsole verfügt über das Kontrollkästchen **Zugriffsberechtigungseinstellungen erzwingen** auf der Registerkarte **Anbieter Pipeline** , um die Autorisierung zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="43773-139">The Application Virtualization Server Management Console has an **Enforce Access Permission Settings** check box on the **Provider Pipeline** tab to enable or disable authorization.</span></span>

<span data-ttu-id="43773-140">Im Application Virtualization System wird der Zugriff nur einer Benutzergruppe und nicht einzelnen Benutzern gewährt.</span><span class="sxs-lookup"><span data-stu-id="43773-140">In the Application Virtualization System, access is granted to a user group only, not to individual users.</span></span>

## <span data-ttu-id="43773-141">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="43773-141">Related topics</span></span>


[<span data-ttu-id="43773-142">So verwalten Sie Anwendungslizenzen in der Server Management Console</span><span class="sxs-lookup"><span data-stu-id="43773-142">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="43773-143">So richten Sie die Anwendungslizenzierung ein oder deaktivieren Sie sie</span><span class="sxs-lookup"><span data-stu-id="43773-143">How to Set Up or Disable Application Licensing</span></span>](how-to-set-up-or-disable-application-licensing.md)

[<span data-ttu-id="43773-144">Server Management Console: Knoten „Anbieterrichtlinien“</span><span class="sxs-lookup"><span data-stu-id="43773-144">Server Management Console: Provider Policies Node</span></span>](server-management-console-provider-policies-node.md)

 

 





