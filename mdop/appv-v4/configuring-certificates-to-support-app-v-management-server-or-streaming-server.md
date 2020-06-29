---
title: Konfigurieren von Zertifikaten zur Unterstützung von App-V Management Server oder Streaming Server
description: Konfigurieren von Zertifikaten zur Unterstützung von App-V Management Server oder Streaming Server
author: dansimp
ms.assetid: 2f24e550-585e-4b7e-b486-22a3f181f543
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e537244b24d7303af550b3ced8286ba2680009e7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809031"
---
# <span data-ttu-id="557d9-103">Konfigurieren von Zertifikaten zur Unterstützung von App-V Management Server oder Streaming Server</span><span class="sxs-lookup"><span data-stu-id="557d9-103">Configuring Certificates to Support App-V Management Server or Streaming Server</span></span>


<span data-ttu-id="557d9-104">Nachdem Sie den Zertifikat Bereitstellungsprozess abgeschlossen und die Berechtigungen für den privaten Schlüssel zur Unterstützung der App-V-Installation geändert haben, können Sie das Setup des Verwaltungsservers oder des Streaming Servers starten.</span><span class="sxs-lookup"><span data-stu-id="557d9-104">After you complete the certificate provisioning process and change the private key permissions to support the App-V installation, you can launch the setup of the Management Server or the Streaming Server.</span></span> <span data-ttu-id="557d9-105">Wenn während des Setups ein Zertifikat bereitgestellt wird, bevor das Setupprogramm ausgeführt wird, zeigt der Assistent das Zertifikat im Bildschirm **Verbindungssicherheitsmodus** an, und das Kontrollkästchen **verstärkte Sicherheit verwenden** ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="557d9-105">During setup, if a certificate is provisioned before running the setup program, the wizard displays the certificate in the **Connection Security Mode** screen and, by default, the **Use enhanced security** check box is selected.</span></span>

<span data-ttu-id="557d9-106">**Hinweis**  Wählen Sie das Zertifikat aus, das für App-V konfiguriert wurde, wenn mehr als ein Zertifikat für diesen Server bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="557d9-106">**Note** Select the certificate that was configured for App-V if there is more than one certificate provisioned for this server.</span></span>

 

<span data-ttu-id="557d9-107">**Wichtig**  Beim Upgrade von Version 4,2 auf Version 4,5 verfügt das Setup über eine Option für die **Verwendung von erweiterter Sicherheit**. Wenn Sie diese Option auswählen, wird das Streaming über RTSP jedoch nicht deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="557d9-107">**Important** When upgrading from version 4.2 to version 4.5, the setup has an option for **Use enhanced security**; however, selecting this option will not disable streaming over RTSP.</span></span> <span data-ttu-id="557d9-108">Sie müssen die Verwaltungskonsole verwenden, um RTSP nach der Installation zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="557d9-108">You must use the Management Console to disable RTSP after installation.</span></span>

 

<span data-ttu-id="557d9-109">Wählen Sie den TCP-Port aus, den der Dienst für die Clientkommunikation verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="557d9-109">Select the TCP port that the service will use for client communications.</span></span> <span data-ttu-id="557d9-110">Der Standardport ist TCP 322; Sie können den Port jedoch in einen benutzerdefinierten Port für Ihre Umgebung ändern.</span><span class="sxs-lookup"><span data-stu-id="557d9-110">The default port is TCP 322; however, you can change the port to a custom port for your environment.</span></span>

<span data-ttu-id="557d9-111">Die verbleibenden Schritte des Assistenten sind identisch mit der Bereitstellungeines App-V-Verwaltungs-oder Streaming-Servers, ohne das Feature **Erweiterte Sicherheit** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="557d9-111">The remaining steps of the wizard are the same as if you were deploying an App-V Management or Streaming Server without using the **Enhanced security** feature.</span></span>

## <span data-ttu-id="557d9-112">Konfigurieren von Zertifikaten für NLB-Umgebungen</span><span class="sxs-lookup"><span data-stu-id="557d9-112">Configuring Certificates for NLB Environments</span></span>


<span data-ttu-id="557d9-113">Um große Unternehmen zu unterstützen, wird der Verwaltungs Server häufig in einem NLB-Cluster (Network Load Balancing, Netzwerklastenausgleich) gespeichert, um die große Anzahl von Verbindungen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="557d9-113">To support large enterprises, often the Management Server is placed into a Network Load Balancing (NLB) cluster to support the large number of connections.</span></span> <span data-ttu-id="557d9-114">Dazu sind mindestens zwei Verwaltungsserver erforderlich, die anscheinend ein einzelner Verwaltungsserver sind.</span><span class="sxs-lookup"><span data-stu-id="557d9-114">This requires at least two Management Servers that appear to be a single Management Server.</span></span> <span data-ttu-id="557d9-115">Wenn in Ihrer Umgebung ein NLB-Cluster mit mehreren Verwaltungsservern verwendet wird, benötigen Sie eine erweiterte Konfiguration des für den NLB-Cluster verwendeten Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="557d9-115">When your environment uses an NLB cluster with several Management Servers, you need an advanced configuration of the certificate used for the NLB cluster.</span></span>

<span data-ttu-id="557d9-116">Das App-V-Zertifikat wird an eine Zertifizierungsstelle (Certification Authority, ca) übermittelt, die auf einem Computer mit Windows-Server2003 konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="557d9-116">The App-V certificate is submitted to a certification authority (CA) that is configured on a computer running Windows Server2003.</span></span> <span data-ttu-id="557d9-117">Mit dem San können Sie eine Verbindung mit einem bestimmten Verwaltungs Server-NLB-Clusterhost Namen herstellen, indem Sie einen DNS-Namen (Domain Name System) verwenden, der möglicherweise von den tatsächlichen Computernamen abweicht, da es bis zu 32-Server geben kann, die den NLB-Cluster umfassen.</span><span class="sxs-lookup"><span data-stu-id="557d9-117">The SAN lets you connect to a specific Management Server NLB cluster host name by using a Domain Name System (DNS) name that might differ from the actual computer names, because there can be up to 32 servers that comprise the NLB cluster.</span></span>

<span data-ttu-id="557d9-118">Diese Konfiguration ist nur bei Verwendung eines NLB-Clusters erforderlich.</span><span class="sxs-lookup"><span data-stu-id="557d9-118">This configuration is necessary only when using an NLB cluster.</span></span> <span data-ttu-id="557d9-119">Wenn der Client eine Verbindung mit dem Server herstellt, wird er mit dem vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des NLB-Clusters und nicht mit dem FQDN eines einzelnen Servers verbunden.</span><span class="sxs-lookup"><span data-stu-id="557d9-119">When the client connects to the server, it will connect using the fully qualified domain name (FQDN) of the NLB cluster and not the FQDN of an individual server.</span></span> <span data-ttu-id="557d9-120">Wenn Sie die San-Eigenschaft nicht mit dem FQDN der Serverknoten im Cluster hinzufügen, werden alle Clientverbindungen abgelehnt, weil der allgemeine Name des Zertifikats nicht mit dem Servernamen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="557d9-120">If you do not add the SAN property with the FQDN of the server nodes in the cluster, all client connections are refused because the common name of the certificate won’t match the server name.</span></span>

<span data-ttu-id="557d9-121">Ausführlichere Informationen zum Konfigurieren von Zertifikaten mit dem San-Attribut finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=133228> .</span><span class="sxs-lookup"><span data-stu-id="557d9-121">For more detailed information about configuring certificates with the SAN attribute, see <https://go.microsoft.com/fwlink/?LinkId=133228>.</span></span>

## <span data-ttu-id="557d9-122">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="557d9-122">Related topics</span></span>


[<span data-ttu-id="557d9-123">Konfigurieren von Zertifikaten zur Unterstützung von sicherem Streaming</span><span class="sxs-lookup"><span data-stu-id="557d9-123">Configuring Certificates to Support Secure Streaming</span></span>](configuring-certificates-to-support-secure-streaming.md)

[<span data-ttu-id="557d9-124">So ändern Sie Berechtigungen für private Schlüssel zur Unterstützung von Management Server oder Streaming Server</span><span class="sxs-lookup"><span data-stu-id="557d9-124">How to Modify Private Key Permissions to Support Management Server or Streaming Server</span></span>](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)

 

 





