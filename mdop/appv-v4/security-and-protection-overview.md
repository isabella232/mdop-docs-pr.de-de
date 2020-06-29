---
title: Übersicht über Sicherheit und Schutz
description: Übersicht über Sicherheit und Schutz
author: dansimp
ms.assetid: a43e1c53-7936-4d48-a110-0be26c8e9d97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b08b7dcb3defa8a01a4fd8a3e7234b5ac2956c4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806395"
---
# <span data-ttu-id="5679f-103">Übersicht über Sicherheit und Schutz</span><span class="sxs-lookup"><span data-stu-id="5679f-103">Security and Protection Overview</span></span>


<span data-ttu-id="5679f-104">Microsoft Application Virtualization 4.5 bietet die folgenden erweiterten Sicherheitsfeatures, die Ihnen bei der Planung und Implementierung einer sichereren Bereitstellungsstrategie helfen:</span><span class="sxs-lookup"><span data-stu-id="5679f-104">Microsoft Application Virtualization4.5 provides the following enhanced security features to help you plan and implement a more secure deployment strategy:</span></span>

-   <span data-ttu-id="5679f-105">Application Virtualization unterstützt jetzt TLS (Transport Layer Security) mithilfe von X. 509 v3-Zertifikaten.</span><span class="sxs-lookup"><span data-stu-id="5679f-105">Application Virtualization now supports Transport Layer Security (TLS) using X.509 V3 certificates.</span></span> <span data-ttu-id="5679f-106">Vorausgesetzt, dass ein Serverzertifikat dem geplanten Application Virtualization Management oder Streaming Server bereitgestellt wurde, wird die Installation standardmäßig mit dem RTSPS-Protokoll über Port 322 gesichert.</span><span class="sxs-lookup"><span data-stu-id="5679f-106">Provided that a server certificate has been provisioned to the planned Application Virtualization Management or Streaming Server, the installation will default to secure, using the RTSPS protocol over port 322.</span></span> <span data-ttu-id="5679f-107">Durch die Verwendung von RTSPS wird sichergestellt, dass die Kommunikation zwischen den Application Virtualization-Servern und den Application Virtualization-Clients signiert und verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="5679f-107">Using RTSPS ensures that communication between the Application Virtualization Servers and the Application Virtualization Clients is signed and encrypted.</span></span> <span data-ttu-id="5679f-108">Wenn dem Server während der Installation von Application Virtualization Server kein Zertifikat zugewiesen ist, wird die Kommunikation auf RTSP über Port 554 eingestellt.</span><span class="sxs-lookup"><span data-stu-id="5679f-108">If no certificate is assigned to the server during the Application Virtualization Server installation, the communication will be set to RTSP over port 554.</span></span>

    **<span data-ttu-id="5679f-109">Sicherheitshinweis:</span><span class="sxs-lookup"><span data-stu-id="5679f-109">Security Note:</span></span>**

    <span data-ttu-id="5679f-110">Damit Sie eine sichere Einrichtung des Servers gewährleisten können, müssen Sie sicherstellen, dass die RTSP-Ports deaktiviert sind, auch wenn Sie alle Pakete für die Verwendung von RTSPS konfiguriert haben.</span><span class="sxs-lookup"><span data-stu-id="5679f-110">To help provide a secure setup of the server, you must make sure that RTSP ports are disabled even if you have all packages configured to use RTSPS.</span></span>

    <span data-ttu-id="5679f-111">Wenn Sie dem Server nach der Installation des Servers Sicherheitszertifikate hinzufügen, werden die Zertifikate möglicherweise nicht vom Server erkannt.</span><span class="sxs-lookup"><span data-stu-id="5679f-111">If you add security certificates to the server after installing the server, the server might not detect the certificates.</span></span> <span data-ttu-id="5679f-112">Um die Erkennung von Sicherheitszertifikaten zu gewährleisten, starten Sie den Server nach dem Hinzufügen der Zertifikate neu.</span><span class="sxs-lookup"><span data-stu-id="5679f-112">To help ensure security certificate detection, restart the server after adding the certificates.</span></span>

-   <span data-ttu-id="5679f-113">Der Client muss so konfiguriert sein, dass er dasselbe Protokoll und denselben Port wie der Server verwendet, oder er kann nicht mit dem Server kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="5679f-113">The client must be configured to use the same protocol and port as the server, or it will not be able to communicate with the server.</span></span> <span data-ttu-id="5679f-114">Der Client muss auch dem Aussteller des Zertifikats Vertrauen und mit mehreren primären Anbietern im vertrauenswürdigen Stammspeicher ausgeliefert werden.</span><span class="sxs-lookup"><span data-stu-id="5679f-114">The client must also trust the issuer of the certificate and ships with several of the primary providers in its Trusted Root Store.</span></span> <span data-ttu-id="5679f-115">Sie können selbstsignierte Zertifikate verwenden, doch müssen Sie die Clients aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5679f-115">You can use self-signed certificates, but you will need to update the clients.</span></span>

-   <span data-ttu-id="5679f-116">Wenn Sie IIS-Server für die Verwendung des HTTPS-Protokolls für Streaming konfigurieren, müssen Sie SSL (Secure Sockets Layer) auf dem IIS-Server einrichten und das Zertifikat für den Server bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5679f-116">When configuring IIS servers to use the HTTPS protocol for streaming, you will need to set up Secure Sockets Layer (SSL) on the IIS server and provision the certificate for the server.</span></span> <span data-ttu-id="5679f-117">Die Clients müssen auch so konfiguriert werden, dass Sie der Stammzertifizierungsstelle vertrauen, die das Serverzertifikat ausgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="5679f-117">The clients will also need to be configured to trust the root certification authority that issued the server certificate.</span></span>

-   <span data-ttu-id="5679f-118">Die Kerberos-Authentifizierung wurde Microsoft Application Virtualization als Standardauthentifizierungsmechanismus hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5679f-118">Kerberos authentication has been added to Microsoft Application Virtualization as the default authentication mechanism.</span></span> <span data-ttu-id="5679f-119">Frühere Versionen haben sich auf NTLM v2 für die Authentifizierung verlassen.</span><span class="sxs-lookup"><span data-stu-id="5679f-119">Earlier versions relied upon NTLM V2 for authentication.</span></span> <span data-ttu-id="5679f-120">Die Verwendung der Kerberos-Authentifizierung stärkt die Sicherheit der Kommunikation zwischen dem Client und dem Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="5679f-120">Using Kerberos Authentication strengthens the security of the communication between the client and the Application Virtualization server.</span></span> <span data-ttu-id="5679f-121">Wenn eine Verbindung vom Client initiiert wurde, überprüft der Application Virtualization Server das Sitzungsticket mit dem Schlüssel Verteilungs Center (Key Distribution Center, KDC).</span><span class="sxs-lookup"><span data-stu-id="5679f-121">When a connection has been initiated from the client, the Application Virtualization Server verifies the session ticket with the Key Distribution Center (KDC).</span></span>

-   <span data-ttu-id="5679f-122">Aufgrund der Unterstützung für die Verwendung von Serverzertifikaten und die Verwendung von RTSPS-oder HTTPS-Protokollen können Sie nun Clients außerhalb des Unternehmensnetzwerks unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5679f-122">Because of the support for using server certificates and using the RTSPS or HTTPS protocols, you can now support clients outside of the corporate network.</span></span> <span data-ttu-id="5679f-123">Dies kann dazu beitragen, dass Mobile Benutzer keine sichere Verbindung mit dem Unternehmensnetzwerk (VPN, RAS usw.) einrichten müssen, bevor Sie die bereitgestellten Application Virtualization-Anwendungen starten.</span><span class="sxs-lookup"><span data-stu-id="5679f-123">This can help eliminate the need for mobile users to set up a secure connection to the corporate network (VPN, RAS, and so on) prior to launching Application Virtualization provisioned applications.</span></span>

<span data-ttu-id="5679f-124">Die folgenden wichtigen Sicherheitsüberlegungen sollten Sie berücksichtigen:</span><span class="sxs-lookup"><span data-stu-id="5679f-124">Other important security considerations to consider include the following:</span></span>

-   <span data-ttu-id="5679f-125">Halten Sie die Server immer vollständig aktualisiert und geschützt.</span><span class="sxs-lookup"><span data-stu-id="5679f-125">Always keep servers fully updated and protected.</span></span>

-   <span data-ttu-id="5679f-126">Wenn Sie ein Zertifikat hinzufügen möchten, um eine sicherere Kommunikation mit dem Application Virtualization Management Server zu ermöglichen, müssen die folgenden Kriterien erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="5679f-126">To add a certificate to enable more secure communications to the Application Virtualization Management Server, the following criteria must be met:</span></span>

    -   <span data-ttu-id="5679f-127">Der Benutzer, der das Zertifikat hinzufügen wird, muss ein Administrator auf dem Server sein, auf dem sich der Zertifikatspeicher befindet.</span><span class="sxs-lookup"><span data-stu-id="5679f-127">The user who will be adding the certificate must be an administrator on the server where the certificate store is located.</span></span>

    -   <span data-ttu-id="5679f-128">Der Server Dienst muss gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="5679f-128">The server service must be started.</span></span>

    -   <span data-ttu-id="5679f-129">Port 139 auf dem Verwaltungs Server muss für den Webdienst server'sIP geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="5679f-129">Port 139 on the Management Server must be open to the Web Service server’sIP.</span></span>

-   <span data-ttu-id="5679f-130">Verwenden Sie Zugriffssteuerungslisten (ACLs), um sicherzustellen, dass die Anwendungspakete und alle Paketdateien geschützt sind und nicht manipuliert werden können.</span><span class="sxs-lookup"><span data-stu-id="5679f-130">Use access control lists (ACLs) to ensure that the application packages and all package files are protected and cannot be tampered.</span></span> <span data-ttu-id="5679f-131">ACLs beschränken den Zugriff auf den Speicherort oder den Ordner, in dem Sie die Pakete speichern, sodass der Zugriff nur auf bestimmte Konten möglich ist.</span><span class="sxs-lookup"><span data-stu-id="5679f-131">ACLs restrict access to the location or folder where you store the packages, allowing access only to certain accounts.</span></span>

-   <span data-ttu-id="5679f-132">Stellen Sie sicher, dass der Kanal zwischen dem Application Virtualization-Verwaltungs Server und der Datenbank gesichert ist, beispielsweise mithilfe von IPSec.</span><span class="sxs-lookup"><span data-stu-id="5679f-132">Make sure that the channel between the Application Virtualization Management Server and the database is secured—for example, by using IPsec.</span></span>

-   <span data-ttu-id="5679f-133">Wenn Pakete auf einem SAN oder NAS gespeichert werden, stellen Sie sicher, dass die Verbindung zwischen dem zentralen Speichergerät und den Application Virtualization-Servern geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="5679f-133">If packages are stored on a SAN or NAS, ensure the connection between the central storage device and the Application Virtualization Servers is protected.</span></span>

-   <span data-ttu-id="5679f-134">Alle Kommunikationskanäle für den Client sollten geschützt werden – einschließlich Verbindungen mit dem Veröffentlichungsserver, dem Application Virtualization Server und dem Pfad zu den OSD-und ICO-Dateien – mithilfe eines Protokolls wie HTTPS oder IPSec.</span><span class="sxs-lookup"><span data-stu-id="5679f-134">All communication channels to the client should be protected—including connections to the publishing server, the Application Virtualization Server, and the path to the OSD and ICO files—by using a protocol such as HTTPS or IPsec.</span></span> 

-   <span data-ttu-id="5679f-135">Client Berechtigungen sollten so konfiguriert werden, dass Sie sicherstellen, dass Pakete nicht von Benutzern manipuliert werden können.</span><span class="sxs-lookup"><span data-stu-id="5679f-135">Client permissions should be configured to help ensure that packages cannot be tampered with by users.</span></span> <span data-ttu-id="5679f-136">Es ist besonders wichtig, dass Sie Benutzern keine Berechtigung zum Hinzufügen oder Aktualisieren von Paketen auf Systemen gewähren, wie etwa RDSession-Hostserver (Remote Desktop-Sitzungshost), die für mehrere Benutzer freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="5679f-136">It is especially important that you do not grant users permission to add or update packages on systems, such as Remote Desktop Session Host (RDSession Host) servers, that are shared with multiple users.</span></span>

-   <span data-ttu-id="5679f-137">Die Kerberos-Authentifizierung muss in Domänen-oder Gesamtstrukturumgebungen zulässig sein, damit die Server Verwaltungskonsole ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="5679f-137">Kerberos authentication must be permitted across domain or forest environments for the Server Management Console to work correctly.</span></span>

-   <span data-ttu-id="5679f-138">Diese Version der Software unterstützt nicht das Hosten eines Kerberos-basierten RTSP-Servers und eines Microsoft NTLM-basierten IIS-Servers auf demselben Computer.</span><span class="sxs-lookup"><span data-stu-id="5679f-138">This release of the software does not support hosting a Kerberos-based RTSP server and a Microsoft NTLM-only-based IIS server on the same computer.</span></span> <span data-ttu-id="5679f-139">Wenn Sie einen RTSP-Server und einen IIS-Server auf demselben Computer hosten möchten, entfernen Sie den SPN vom IIS-Server, und verwenden Sie die NTLM-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="5679f-139">To host an RTSP server and an IIS server on the same computer, remove the SPN from the IIS server and use NTLM authentication.</span></span>

## <span data-ttu-id="5679f-140">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5679f-140">Related topics</span></span>


[<span data-ttu-id="5679f-141">Planen der Bereitstellung von Application Virtualization System</span><span class="sxs-lookup"><span data-stu-id="5679f-141">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





