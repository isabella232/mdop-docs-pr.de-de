---
title: Bereitstellen des App-V 5.1-Servers
description: Bereitstellen des App-V 5.1-Servers
author: dansimp
ms.assetid: 987b61dc-00d6-49ba-8f1b-92d7b948e702
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bcff2a3211ea3e2f666aff1d6f2ad919509aa3a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805822"
---
# <span data-ttu-id="54dd9-103">Bereitstellen des App-V 5.1-Servers</span><span class="sxs-lookup"><span data-stu-id="54dd9-103">Deploying the App-V 5.1 Server</span></span>

<span data-ttu-id="54dd9-104">Sie können die 5,1-Server Features von Microsoft Application Virtualization (App-V) mithilfe verschiedener Bereitstellungskonfigurationen installieren, die in diesem Thema beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="54dd9-104">You can install the Microsoft Application Virtualization (App-V) 5.1 server features by using different deployment configurations, which described in this topic.</span></span> <span data-ttu-id="54dd9-105">Bevor Sie die Server Features installieren, lesen Sie den Abschnitt Server der [Sicherheitsüberlegungen zu App-V 5,1](app-v-51-security-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="54dd9-105">Before you install the server features, review the server section of [App-V 5.1 Security Considerations](app-v-51-security-considerations.md).</span></span>

<span data-ttu-id="54dd9-106">Informationen zum Bereitstellen des App-v-Servers finden Sie unter Informationen [zu app-v 5,1](about-app-v-51.md#bkmk-migrate-to-51).</span><span class="sxs-lookup"><span data-stu-id="54dd9-106">For information about deploying the App-V Server, see [About App-V 5.1](about-app-v-51.md#bkmk-migrate-to-51).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="54dd9-107">Bevor Sie die App-V 5,1-Server installieren und konfigurieren, müssen Sie einen Port angeben, in dem die einzelnen Komponenten gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="54dd9-107">Before you install and configure the App-V 5.1 servers, you must specify a port where each component will be hosted.</span></span> <span data-ttu-id="54dd9-108">Sie müssen auch die zugehörigen Firewallregeln hinzufügen, damit eingehende Anforderungen auf die angegebenen Ports zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="54dd9-108">You must also add the associated firewall rules to allow incoming requests to access the specified ports.</span></span> <span data-ttu-id="54dd9-109">Das Installationsprogramm ändert keine Firewalleinstellungen.</span><span class="sxs-lookup"><span data-stu-id="54dd9-109">The installer does not modify firewall settings.</span></span>

## <a href="" id="---------app-v-5-1-server-overview"></a> <span data-ttu-id="54dd9-110">App-V 5,1 Server – Übersicht</span><span class="sxs-lookup"><span data-stu-id="54dd9-110">App-V 5.1 Server overview</span></span>

<span data-ttu-id="54dd9-111">Der App-V 5,1-Server besteht aus fünf Komponenten.</span><span class="sxs-lookup"><span data-stu-id="54dd9-111">The App-V 5.1 Server is made up of five components.</span></span> <span data-ttu-id="54dd9-112">Jede Komponente dient in der App-V 5,1-Umgebung einem anderen Zweck.</span><span class="sxs-lookup"><span data-stu-id="54dd9-112">Each component serves a different purpose within the App-V 5.1 environment.</span></span> <span data-ttu-id="54dd9-113">Jede der fünf Komponenten wird hier kurz beschrieben:</span><span class="sxs-lookup"><span data-stu-id="54dd9-113">Each of the five components is briefly described here:</span></span>

- <span data-ttu-id="54dd9-114">Verwaltungs Server – bietet allgemeine Verwaltungsfunktionen für die App-V 5,1-Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="54dd9-114">Management Server – provides overall management functionality for the App-V 5.1 infrastructure.</span></span>
- <span data-ttu-id="54dd9-115">Verwaltungsdatenbank – ermöglicht die Bereitstellung von Datenbankbereitstellungen für die App-V 5,1-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="54dd9-115">Management Database – facilitates database predeployments for App-V 5.1 management.</span></span>
- <span data-ttu-id="54dd9-116">Publishing Server – bietet Hosting-und Streamingfunktionen für virtuelle Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="54dd9-116">Publishing Server – provides hosting and streaming functionality for virtual applications.</span></span>
- <span data-ttu-id="54dd9-117">Reporting Server – bietet App-V 5,1 Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="54dd9-117">Reporting Server – provides App-V 5.1 reporting services.</span></span>
- <span data-ttu-id="54dd9-118">Berichtsdatenbank – ermöglicht die Bereitstellung von Datenbanken für App-V 5,1-Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="54dd9-118">Reporting Database – facilitates database predeployments for App-V 5.1 reporting.</span></span>

## <a href="" id="---------app-v-5-1-stand-alone-deployment"></a> <span data-ttu-id="54dd9-119">App-V 5,1 eigenständige Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="54dd9-119">App-V 5.1 stand-alone deployment</span></span>

<span data-ttu-id="54dd9-120">Die eigenständige App-V 5,1-Bereitstellung bietet eine gute Topologie für eine kleine Bereitstellung oder eine Testumgebung.</span><span class="sxs-lookup"><span data-stu-id="54dd9-120">The App-V 5.1 standalone deployment provides a good topology for a small deployment or a test environment.</span></span> <span data-ttu-id="54dd9-121">Wenn Sie diese Art von Implementierung verwenden, werden alle Server Komponenten auf einem einzelnen Computer bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="54dd9-121">When you use this type of implementation, all server components are deployed to a single computer.</span></span> <span data-ttu-id="54dd9-122">Die Dienste und zugehörigen Datenbanken konkurrieren um die Ressourcen auf dem Computer, auf dem die App-V 5,1-Komponenten ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="54dd9-122">The services and associated databases will compete for the resources on the computer that runs the App-V 5.1 components.</span></span> <span data-ttu-id="54dd9-123">Daher sollten Sie diese Topologie nicht für größere Bereitstellungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="54dd9-123">Therefore, you should not use this topology for larger deployments.</span></span>

[<span data-ttu-id="54dd9-124">So stellen Sie den App-V 5.1-Server bereit</span><span class="sxs-lookup"><span data-stu-id="54dd9-124">How to Deploy the App-V 5.1 Server</span></span>](how-to-deploy-the-app-v-51-server.md)

[<span data-ttu-id="54dd9-125">So stellen Sie den App-V 5.1-Server mithilfe eines Skripts bereit</span><span class="sxs-lookup"><span data-stu-id="54dd9-125">How to Deploy the App-V 5.1 Server Using a Script</span></span>](how-to-deploy-the-app-v-51-server-using-a-script.md)

## <a href="" id="---------app-v-5-1-server-distributed-deployment"></a> <span data-ttu-id="54dd9-126">App-V 5,1 Server – verteilte Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="54dd9-126">App-V 5.1 Server distributed deployment</span></span>

<span data-ttu-id="54dd9-127">Die verteilte Bereitstellungstopologie kann eine große App-V 5,1-Clientbasis unterstützen, sodass Sie Ihre Umgebung einfacher verwalten und skalieren können.</span><span class="sxs-lookup"><span data-stu-id="54dd9-127">The distributed deployment topology can support a large App-V 5.1 client base and it allows you to more easily manage and scale your environment.</span></span> <span data-ttu-id="54dd9-128">Wenn Sie diese Art der Bereitstellung verwenden, werden die App-V 5,1-Server Komponenten basierend auf der Struktur und den Anforderungen der Organisation auf mehreren Computern bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="54dd9-128">When you use this type of deployment, the App-V 5.1 Server components are deployed across multiple computers, based on the structure and requirements of the organization.</span></span>

[<span data-ttu-id="54dd9-129">So installieren Sie die Verwaltungs- und Berichtsdatenbanken auf verschiedenen Computern über die Verwaltungs- und Berichtsdienste</span><span class="sxs-lookup"><span data-stu-id="54dd9-129">How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services</span></span>](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md)

[<span data-ttu-id="54dd9-130">So installieren Sie den Verwaltungsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank</span><span class="sxs-lookup"><span data-stu-id="54dd9-130">How to install the Management Server on a Standalone Computer and Connect it to the Database</span></span>](how-to-install-the-management-server-on-a-standalone-computer-and-connect-it-to-the-database51.md)

[<span data-ttu-id="54dd9-131">So stellen Sie den App-V 5.1-Server mithilfe eines Skripts bereit</span><span class="sxs-lookup"><span data-stu-id="54dd9-131">How to Deploy the App-V 5.1 Server Using a Script</span></span>](how-to-deploy-the-app-v-51-server-using-a-script.md)

[<span data-ttu-id="54dd9-132">So installieren Sie den Veröffentlichungsserver auf einem Remotecomputer</span><span class="sxs-lookup"><span data-stu-id="54dd9-132">How to Install the Publishing Server on a Remote Computer</span></span>](how-to-install-the-publishing-server-on-a-remote-computer51.md)

[<span data-ttu-id="54dd9-133">So installieren Sie den Verwaltungsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank</span><span class="sxs-lookup"><span data-stu-id="54dd9-133">How to install the Management Server on a Standalone Computer and Connect it to the Database</span></span>](how-to-install-the-management-server-on-a-standalone-computer-and-connect-it-to-the-database51.md)

## <span data-ttu-id="54dd9-134">Verwenden einer ESD-Lösung (Enterprise Software Distribution) und App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="54dd9-134">Using an Enterprise Software Distribution (ESD) solution and App-V 5.1</span></span>

<span data-ttu-id="54dd9-135">Sie können die APP-v 5,1-Clients und-Pakete auch mithilfe eines ESD bereitstellen, ohne APP-v 5,1 bereitstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="54dd9-135">You can also deploy the App-V 5.1 clients and packages by using an ESD without having to deploy App-V 5.1.</span></span> <span data-ttu-id="54dd9-136">Die vollständigen Funktionen für die Integration sind je nach verwendetem ESD unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="54dd9-136">The full capabilities for integration will vary depending on the ESD that you use.</span></span>

> [!NOTE]
> <span data-ttu-id="54dd9-137">Der APP-v 5,1-Berichtsserver und die Berichtsdatenbank können neben dem ESD weiterhin bereitgestellt werden, um die Berichtsdaten von den App-v 5,1-Clients zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="54dd9-137">The App-V 5.1 reporting server and reporting database can still be deployed alongside the ESD to collect the reporting data from the App-V 5.1 clients.</span></span> <span data-ttu-id="54dd9-138">Die anderen drei Server Komponenten sollten jedoch nicht bereitgestellt werden, da Sie mit der ESD-Funktionalität in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="54dd9-138">However, the other three server components should not be deployed, because they will conflict with the ESD functionality.</span></span>

[<span data-ttu-id="54dd9-139">Bereitstellen von App-V 5.1-Paketen mithilfe einer ESD-Lösung (Electronic Software Distribution)</span><span class="sxs-lookup"><span data-stu-id="54dd9-139">Deploying App-V 5.1 Packages by Using Electronic Software Distribution (ESD)</span></span>](deploying-app-v-51-packages-by-using-electronic-software-distribution--esd-.md)

## <a href="" id="---------app-v-5-1-server-logs"></a> <span data-ttu-id="54dd9-140">App-V 5,1-Server Protokolle</span><span class="sxs-lookup"><span data-stu-id="54dd9-140">App-V 5.1 Server logs</span></span>

<span data-ttu-id="54dd9-141">Sie können APP-v 5,1 Server-Protokollinformationen verwenden, um bei der Verwendung von App-v 5,1 bei der Behandlung von Server Installations-und Betriebsereignissen zu helfen.</span><span class="sxs-lookup"><span data-stu-id="54dd9-141">You can use App-V 5.1 server log information to help troubleshoot the server installation and operational events while using App-V 5.1.</span></span> <span data-ttu-id="54dd9-142">Die serverbezogenen Protokollinformationen können mit der **Ereignisanzeige**überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="54dd9-142">The server-related log information can be reviewed with the **Event Viewer**.</span></span> <span data-ttu-id="54dd9-143">In der folgenden Zeile wird der spezifische Pfad für Server bezogene Ereignisse angezeigt:</span><span class="sxs-lookup"><span data-stu-id="54dd9-143">The following line displays the specific path for Server-related events:</span></span>

**<span data-ttu-id="54dd9-144">Ereignisanzeige \ \ Anwendungen und Dienstprotokolle \ \ Microsoft \ \ App V</span><span class="sxs-lookup"><span data-stu-id="54dd9-144">Event Viewer \\ Applications and Services Logs \\ Microsoft \\ App V</span></span>**

<span data-ttu-id="54dd9-145">Zugeordnete Setupprotokolle werden im folgenden Verzeichnis gespeichert:</span><span class="sxs-lookup"><span data-stu-id="54dd9-145">Associated setup logs are saved in the following directory:</span></span>

**<span data-ttu-id="54dd9-146">Temp</span><span class="sxs-lookup"><span data-stu-id="54dd9-146">%temp%</span></span>**

<span data-ttu-id="54dd9-147">In App-V 5,0 SP3 wurden einige Protokolle konsolidiert und verschoben.</span><span class="sxs-lookup"><span data-stu-id="54dd9-147">In App-V 5.0 SP3, some logs were consolidated and moved.</span></span> <span data-ttu-id="54dd9-148">Informationen finden Sie unter [App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span><span class="sxs-lookup"><span data-stu-id="54dd9-148">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span></span>

## <a href="" id="---------app-v-5-1-reporting"></a> <span data-ttu-id="54dd9-149">App-V 5,1-Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="54dd9-149">App-V 5.1 reporting</span></span>

<span data-ttu-id="54dd9-150">App-v 5,1-Berichterstellung ermöglicht es App-v 5,1-Clients, Daten zu sammeln und dann zurückzusenden, damit Sie in einem zentralen Repository gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="54dd9-150">App-V 5.1 reporting allows App-V 5.1 clients to collect data and then send it back to be stored in a central repository.</span></span> <span data-ttu-id="54dd9-151">Sie können diese Informationen verwenden, um eine bessere Sicht auf die Verwendung der virtuellen Anwendung in Ihrer Organisation zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="54dd9-151">You can use this information to get a better view of the virtual application usage within your organization.</span></span> <span data-ttu-id="54dd9-152">In der folgenden Liste werden einige der Arten von Informationen angezeigt, die der App-V 5,1-Client sammelt:</span><span class="sxs-lookup"><span data-stu-id="54dd9-152">The following list displays some of the types of information the App-V 5.1 client collects:</span></span>

- <span data-ttu-id="54dd9-153">Informationen zu dem Computer, auf dem der App-V 5,1-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54dd9-153">Information about the computer that runs the App-V 5.1 client.</span></span>
- <span data-ttu-id="54dd9-154">Informationen zu virtualisierten Paketen auf einem bestimmten Computer, auf dem der App-V 5,1-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54dd9-154">Information about virtualized packages on a specific computer that runs the App-V 5.1 client.</span></span>
- <span data-ttu-id="54dd9-155">Informationen zum Öffnen und Herunterfahren des Pakets für einen bestimmten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="54dd9-155">Information about package open and shutdown for a specific user.</span></span>

<span data-ttu-id="54dd9-156">Die Berichterstattungs Informationen werden so lange verwaltet, bis Sie erfolgreich an die Berichtsserver-Datenbank gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="54dd9-156">The reporting information will be maintained until it is successfully sent to the reporting server database.</span></span> <span data-ttu-id="54dd9-157">Nachdem sich die Daten in der Datenbank befinden, können Sie Microsoft SQL Server Reporting Services verwenden, um alle erforderlichen Berichte zu generieren.</span><span class="sxs-lookup"><span data-stu-id="54dd9-157">After the data is in the database, you can use Microsoft SQL Server Reporting Services to generate any necessary reports.</span></span>

<span data-ttu-id="54dd9-158">Wenn Sie Berichtsinformationen abrufen möchten, müssen Sie Microsoft SQL Server Reporting Services (SSRS) verwenden, das in Microsoft SQL verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="54dd9-158">If you want to retrieve report information, you must use Microsoft SQL Server Reporting Services (SSRS) which is available with Microsoft SQL.</span></span> <span data-ttu-id="54dd9-159">SSRS wird nicht installiert, wenn Sie den App-V 5,1-Berichtsserver installieren und separat bereitgestellt werden muss, um die zugehörigen Berichte zu generieren.</span><span class="sxs-lookup"><span data-stu-id="54dd9-159">SSRS is not installed when you install the App-V 5.1 reporting server and it must be deployed separately to generate the associated reports.</span></span>

<span data-ttu-id="54dd9-160">Verwenden Sie den folgenden Link, um weitere Informationen [zur App-V 5,1-Berichterstellung](about-app-v-51-reporting.md)zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="54dd9-160">Use the following link for more information [About App-V 5.1 Reporting](about-app-v-51-reporting.md).</span></span>

[<span data-ttu-id="54dd9-161">So aktivieren Sie die Berichterstellung auf dem App-V 5.1-Client mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="54dd9-161">How to Enable Reporting on the App-V 5.1 Client by Using PowerShell</span></span>](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md)

## <span data-ttu-id="54dd9-162">Weitere Ressourcen für den App-V-Server</span><span class="sxs-lookup"><span data-stu-id="54dd9-162">Other resources for the App-V server</span></span>

[<span data-ttu-id="54dd9-163">Bereitstellen von App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="54dd9-163">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)
