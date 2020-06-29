---
title: Sicheres Installieren von App-V Management Server oder Streaming Server
description: Sicheres Installieren von App-V Management Server oder Streaming Server
author: dansimp
ms.assetid: d2a51a81-a80f-427c-a727-611e1eb74f02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0150f4dc7f489731c4a818fed9780ebb25dbd24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806663"
---
# <span data-ttu-id="873e9-103">Sicheres Installieren von App-V Management Server oder Streaming Server</span><span class="sxs-lookup"><span data-stu-id="873e9-103">Installing App-V Management Server or Streaming Server Securely</span></span>


<span data-ttu-id="873e9-104">Die Themen in diesem Abschnitt enthalten Informationen zum Installieren einer erweiterten Sicherheitsversion des App-v-Verwaltungsservers oder des App-v-Streaming-Servers.</span><span class="sxs-lookup"><span data-stu-id="873e9-104">The topics in this section provide information for installing an enhanced security version of the App-V Management Server or the App-V Streaming Server.</span></span>

<span data-ttu-id="873e9-105">**Hinweis**  Zum Installieren oder Konfigurieren eines App-v-Verwaltungs-oder Streaming-Servers zur Verwendung der erweiterten Sicherheit (beispielsweise Transport Layer Security oder TLS) muss ein X. 509 v3-Zertifikat für den App-v-Server bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="873e9-105">**Note** Installing or configuring an App-V Management or Streaming Server to use enhanced security (for example, Transport Layer Security, or TLS) requires that an X.509 V3 certificate has been provisioned to the App-V server.</span></span>

 

<span data-ttu-id="873e9-106">Wenn Sie sich für die Installation oder Konfiguration eines sicheren Management-oder Streaming-Servers vorbereiten, sollten Sie die folgenden technischen Voraussetzungen Bedenken:</span><span class="sxs-lookup"><span data-stu-id="873e9-106">When you prepare to install or configure a secure Management or Streaming Server, consider the following technical requirements:</span></span>

-   <span data-ttu-id="873e9-107">Das Zertifikat muss gültig sein.</span><span class="sxs-lookup"><span data-stu-id="873e9-107">The certificate must be valid.</span></span> <span data-ttu-id="873e9-108">Wenn das Zertifikat ungültig ist, beendet der Client die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="873e9-108">If the certificate is not valid, the client ends the connection.</span></span>

-   <span data-ttu-id="873e9-109">Das Zertifikat muss die korrekte *Erweiterte Schlüsselverwendung (Enhanced Key Usage* , EKU) – Server Authentifizierung (OID 1.3.6.1.5.5.7.3.1) enthalten.</span><span class="sxs-lookup"><span data-stu-id="873e9-109">The certificate must contain the correct *Enhanced Key Usage* (EKU)—Server Authentication (OID 1.3.6.1.5.5.7.3.1).</span></span> <span data-ttu-id="873e9-110">Wenn das Zertifikat diese EKU nicht enthält, beendet der Client die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="873e9-110">If the certificate does not contain this EKU, the client ends the connection.</span></span>

-   <span data-ttu-id="873e9-111">Der vollqualifizierte Domänenname (Fully Qualified Domain Name, FQDN) des Zertifikats muss mit dem Server übereinstimmen, auf dem er installiert ist.</span><span class="sxs-lookup"><span data-stu-id="873e9-111">The certificate fully qualified domain name (FQDN) must match the server on which it is installed.</span></span> <span data-ttu-id="873e9-112">Wenn beispielsweise der Client angerufen wird `RTSPS://Myserver.mycompany.com/content/MyApp.sft` und das **für Field ausgegebene** Zertifikat auf eingestellt ist `Server1.mycompany.com` , stellt der Client keine Verbindung mit dem Server her, und die Sitzung endet.</span><span class="sxs-lookup"><span data-stu-id="873e9-112">For example, if the client is calling `RTSPS://Myserver.mycompany.com/content/MyApp.sft` and the certificate **Issued To** field is set to `Server1.mycompany.com`, the client will not connect to the server and the session ends.</span></span> <span data-ttu-id="873e9-113">Der Fehler wird dem Benutzer gemeldet.</span><span class="sxs-lookup"><span data-stu-id="873e9-113">The failure is reported to the user.</span></span>

    <span data-ttu-id="873e9-114">**Hinweis**  Wenn Sie App-V in einem Netzwerklastenausgleich-Cluster verwenden, müssen Sie das Zertifikat mit "Subject Alternate Names (SANs)" konfigurieren, um RTSPS zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="873e9-114">**Note** If you are using App-V in a Network Load Balancing cluster, you must configure the certificate with Subject Alternate Names (SANs) to support RTSPS.</span></span> <span data-ttu-id="873e9-115">Informationen zum Konfigurieren der Zertifizierungsstelle und zum Erstellen von Zertifikaten mit Sans finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=133228> .</span><span class="sxs-lookup"><span data-stu-id="873e9-115">For information about configuring the certification authority (CA) and creating certificates with SANs, see <https://go.microsoft.com/fwlink/?LinkId=133228>.</span></span>

     

-   <span data-ttu-id="873e9-116">Der Client und der Server müssen der Stammzertifizierungsstelle vertrauen – die Zertifizierungsstelle, die das Zertifikat an den App-V-Server ausgibt, muss vom Client als vertrauenswürdig eingestuft werden.</span><span class="sxs-lookup"><span data-stu-id="873e9-116">The client and the server need to trust the root CA—The CA issuing the certificate to the App-V server must by trusted by the client connecting to the server.</span></span> <span data-ttu-id="873e9-117">Wenn dies nicht der Fall ist, beendet der Client die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="873e9-117">If not, the client ends the connection.</span></span>

-   <span data-ttu-id="873e9-118">Für den privaten Schlüssel des Zertifikats muss die Berechtigung geändert werden, damit das App-V-Dienstkonto auf das Zertifikat zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="873e9-118">The certificate’s private key must have permissions changed to allow the App-V Service account to access the certificate.</span></span> <span data-ttu-id="873e9-119">Standardmäßig verwendet App-V das Netzwerkdienstkonto, und das Netzwerkdienstkonto verfügt standardmäßig nicht über die Berechtigung für den Zugriff auf den privaten Schlüssel, wodurch sichere Verbindungen verhindert werden.</span><span class="sxs-lookup"><span data-stu-id="873e9-119">By default, App-V uses the Network Service account, and by default, the Network Service account does not have permission to access the private key, which will prevent secure connections.</span></span>

## <span data-ttu-id="873e9-120">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="873e9-120">In This Section</span></span>


<a href="" id="configuring-certificates-to-support-secure-streaming"></a>[<span data-ttu-id="873e9-121">Konfigurieren von Zertifikaten zur Unterstützung von sicherem Streaming</span><span class="sxs-lookup"><span data-stu-id="873e9-121">Configuring Certificates to Support Secure Streaming</span></span>](configuring-certificates-to-support-secure-streaming.md)  
<span data-ttu-id="873e9-122">Enthält Informationen zum Abrufen, konfigurieren und Installieren von Zertifikaten zur Unterstützung von Secure Streaming.</span><span class="sxs-lookup"><span data-stu-id="873e9-122">Provides information about obtaining, configuring, and installing certificates to support secure streaming.</span></span>

<a href="" id="how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server"></a>[<span data-ttu-id="873e9-123">So ändern Sie Berechtigungen für private Schlüssel zur Unterstützung von Management Server oder Streaming Server</span><span class="sxs-lookup"><span data-stu-id="873e9-123">How to Modify Private Key Permissions to Support Management Server or Streaming Server</span></span>](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)  
<span data-ttu-id="873e9-124">Stellt Prozeduren bereit, die Sie zum Ändern von Schlüsseln in Windows Server2003 und Windows Server2008 verwenden können.</span><span class="sxs-lookup"><span data-stu-id="873e9-124">Provides procedures you can use to modify keys in Windows Server2003 and Windows Server2008.</span></span>

<a href="" id="configuring-certificates-to-support-app-v-management-server-or-streaming-server"></a>[<span data-ttu-id="873e9-125">Konfigurieren von Zertifikaten zur Unterstützung von App-V Management Server oder Streaming Server</span><span class="sxs-lookup"><span data-stu-id="873e9-125">Configuring Certificates to Support App-V Management Server or Streaming Server</span></span>](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)  
<span data-ttu-id="873e9-126">Enthält Informationen zum Konfigurieren von Zertifikaten für die App-V-Verwaltungs-oder Streaming-Server, einschließlich Informationen zum Konfigurieren von Zertifikaten für Netzwerklastenausgleich-Umgebungen.</span><span class="sxs-lookup"><span data-stu-id="873e9-126">Provides information about configuring certificates for the App-V Management or Streaming Servers, including information about configuring certificates for Network Load Balancing environments.</span></span>

 

 





