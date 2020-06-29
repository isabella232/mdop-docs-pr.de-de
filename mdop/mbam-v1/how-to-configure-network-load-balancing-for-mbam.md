---
title: So konfigurieren Sie den Netzwerklastenausgleich für MBAM
description: So konfigurieren Sie den Netzwerklastenausgleich für MBAM
author: dansimp
ms.assetid: df2208c3-352b-4a48-9722-237b0c8cd6a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a04bc74a9dab7bfe18eed8e5a3c1b6ca64d88b5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811200"
---
# <span data-ttu-id="4cb56-103">So konfigurieren Sie den Netzwerklastenausgleich für MBAM</span><span class="sxs-lookup"><span data-stu-id="4cb56-103">How to Configure Network Load Balancing for MBAM</span></span>


<span data-ttu-id="4cb56-104">Wenn Sie sicherstellen möchten, dass Sie die Voraussetzungen und Hardware-und Softwareanforderungen für die Installation des Features Verwaltung und Monitoring Server erfüllt haben, lesen Sie [MBAM 1,0-Bereitstellungsvoraussetzungen](mbam-10-deployment-prerequisites.md) und [MBAM 1,0-unterstützte Konfigurationen](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="4cb56-104">To verify that you have met the prerequisites and hardware and software requirements to install the Administration and Monitoring Server feature, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

<span data-ttu-id="4cb56-105">**Hinweis**  Um die Setupprotokolldateien zu erhalten, müssen Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mithilfe des **msiexec** -Pakets und der Option " **/l** &lt; Location &gt; " installieren.</span><span class="sxs-lookup"><span data-stu-id="4cb56-105">**Note** To obtain the setup log files, you must install Microsoft BitLocker Administration and Monitoring (MBAM) by using the **msiexec** package and the **/l** &lt;location&gt; option.</span></span> <span data-ttu-id="4cb56-106">Die Protokolldateien werden an dem von Ihnen angegebenen Speicherort erstellt.</span><span class="sxs-lookup"><span data-stu-id="4cb56-106">The Log files are created in the location that you specify.</span></span>

<span data-ttu-id="4cb56-107">Zusätzliche Setupprotokolldateien werden im Ordner "% Temp%" des Benutzers erstellt, der MBAM installiert.</span><span class="sxs-lookup"><span data-stu-id="4cb56-107">Additional setup log files are created in the %temp% folder of the user who installs MBAM.</span></span>

 

<span data-ttu-id="4cb56-108">Die Netzwerklastenausgleich-Cluster (NLB) für das Verwaltungs-und Überwachungs Server Feature bieten Skalierbarkeit in MBAM und sollten mehr als 55.000 MBAM-Clientcomputer unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4cb56-108">The Network Load Balancing (NLB) clusters for the Administration and Monitoring Server feature provides scalability in MBAM and it should support more than 55,000 MBAM client computers.</span></span>

<span data-ttu-id="4cb56-109">**Hinweis**  Der Windows Server-Netzwerklastenausgleich verteilt Clientanforderungen auf eine Reihe von Servern, die in einem einzelnen Servercluster konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="4cb56-109">**Note** Windows Server Network Load Balancing distributes client requests across a set of servers that are configured into a single server cluster.</span></span> <span data-ttu-id="4cb56-110">Wenn der Netzwerklastenausgleich auf den einzelnen Servern (Hosts) eines Clusters installiert ist, stellt der Cluster eine virtuelle IP-Adresse oder einen vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) für Clientanforderungen dar.</span><span class="sxs-lookup"><span data-stu-id="4cb56-110">When Network Load Balancing is installed on each of the servers (hosts) in a cluster, the cluster presents a virtual IP address or fully qualified domain name (FQDN) to client requests.</span></span> <span data-ttu-id="4cb56-111">Die anfänglichen Clientanforderungen gehen an alle Hosts im Cluster, aber nur ein Host akzeptiert und verarbeitet die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4cb56-111">The initial client requests go to all the hosts in the cluster, but only one host accepts and handles the request.</span></span>

<span data-ttu-id="4cb56-112">Alle Computer, die zu einem NLB-Cluster gehören, weisen die folgenden Voraussetzungen auf:</span><span class="sxs-lookup"><span data-stu-id="4cb56-112">All computers that will be part of a NLB cluster have the following requirements:</span></span>

-   <span data-ttu-id="4cb56-113">Alle Computer im NLB-Cluster müssen sich in derselben Domäne befinden.</span><span class="sxs-lookup"><span data-stu-id="4cb56-113">All computers in the NLB cluster must be in the same domain.</span></span>

-   <span data-ttu-id="4cb56-114">Jeder Computer im NLB-Cluster muss eine statische IP-Adresse verwenden.</span><span class="sxs-lookup"><span data-stu-id="4cb56-114">Each computer in the NLB cluster must use a static IP address.</span></span>

-   <span data-ttu-id="4cb56-115">Auf jedem Computer im NLB-Cluster muss der Netzwerklastenausgleich aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="4cb56-115">Each computer in the NLB cluster must have Network Load Balancing enabled.</span></span>

-   <span data-ttu-id="4cb56-116">Der NLB-Cluster erfordert eine statische IP-Adresse, und ein Hosteintrag muss manuell im DNS (Domain Name System) erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4cb56-116">The NLB cluster requires a static IP address, and a host record must be manually created in the domain name system (DNS).</span></span>

 

## <span data-ttu-id="4cb56-117">Konfigurieren des Netzwerklastenausgleichs für MBAM-Verwaltungs-und-Überwachungsserver</span><span class="sxs-lookup"><span data-stu-id="4cb56-117">Configuring Network Load Balancing for MBAM Administration and Monitoring Servers</span></span>


<span data-ttu-id="4cb56-118">In den folgenden Schritten wird beschrieben, wie Sie einen virtuellen NLB-Clusternamen und eine IP-Adresse für zwei MBAM-Verwaltungs-und-Überwachungsserver konfigurieren und wie Sie MBAM-Clients für die Verwendung des NLB-Clusters konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="4cb56-118">The following steps describe how to configure an NLB cluster virtual name and IP address for two MBAM Administration and Monitoring servers, and how to configure MBAM Clients to use the NLB Cluster.</span></span>

<span data-ttu-id="4cb56-119">Bevor Sie mit den in diesem Thema beschriebenen Verfahren beginnen, müssen Sie das MBAM-Verwaltungs-und Überwachungs Server Feature erfolgreich installieren, indem Sie dieselbe IIS-Portbindung auf zwei separaten Server Computern verwenden, die die Voraussetzungen für die Installation von MBAM-Server Features und die NLB-Cluster Konfiguration erfüllen.</span><span class="sxs-lookup"><span data-stu-id="4cb56-119">Before you begin the procedures described in this topic, you must have the MBAM Administration and Monitoring Server feature successfully installed by using the same IIS port binding on two separate server computers that meet the prerequisites for both MBAM Server feature installation and NLB Cluster configuration.</span></span>

<span data-ttu-id="4cb56-120">**Hinweis**  In diesem Thema wird der grundlegende Prozess der Verwendung des Netzwerklastenausgleich-Managers zum Erstellen eines NLB-Clusters beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4cb56-120">**Note** This topic describes the basic process of using Network Load Balancing Manager to create an NLB Cluster.</span></span> <span data-ttu-id="4cb56-121">Die genauen Schritte zum Konfigurieren eines Windows-Servers als Teil eines NLB-Clusters hängen von der verwendeten Windows Server-Version ab.</span><span class="sxs-lookup"><span data-stu-id="4cb56-121">The exact steps to configure a Windows Server as part of an NLB cluster depend on the Windows Server version in use..</span></span> <span data-ttu-id="4cb56-122">Weitere Informationen zum Erstellen von NLBS auf WindowsServer2008 finden Sie unter [Erstellen von Netzwerklastenausgleich-Clustern](https://go.microsoft.com/fwlink/?LinkId=197176) in der Windows Server2008 TechNet-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="4cb56-122">For more information about how to create NLBs on WindowsServer2008, see [Creating Network Load Balancing Clusters](https://go.microsoft.com/fwlink/?LinkId=197176) in the Windows Server2008 TechNet library.</span></span>

 

**<span data-ttu-id="4cb56-123">So konfigurieren Sie einen virtuellen NLB-Cluster Namen und eine IP-Adresse für zwei MBAM-Verwaltungs-und-Überwachungsserver</span><span class="sxs-lookup"><span data-stu-id="4cb56-123">To configure an NLB Cluster Virtual Name and IP address for two MBAM Administration and Monitoring Servers</span></span>**

1.  <span data-ttu-id="4cb56-124">Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **Netzwerklastenausgleich-Manager**.</span><span class="sxs-lookup"><span data-stu-id="4cb56-124">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Network Load Balancing Manager**.</span></span>

    <span data-ttu-id="4cb56-125">**Hinweis**  Wenn der NLB-Manager nicht vorhanden ist, können Sie ihn als Windows Server-Feature installieren.</span><span class="sxs-lookup"><span data-stu-id="4cb56-125">**Note** If the NLB Manager is not present, you can install it as a WindowsServer feature.</span></span> <span data-ttu-id="4cb56-126">Sie müssen dieses Feature auf beiden MBAM-Verwaltungs-und-Überwachungs Servern installieren, wenn Sie es in den NLB-Cluster konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="4cb56-126">You must install this feature on both MBAM Administration and Monitoring servers if you want to configure it into the NLB cluster.</span></span>

     

2.  <span data-ttu-id="4cb56-127">Klicken Sie auf der Menüleiste auf **Cluster**, und klicken Sie dann auf **neu** , um das Dialogfeld **Clusterparameter** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4cb56-127">On the menu bar, click **Cluster**, and then click **New** to open the **Cluster Parameters** dialog box.</span></span>

3.  <span data-ttu-id="4cb56-128">Geben Sie im Dialogfeld **Clusterparameter** die Informationen für die IP-Konfiguration des NLB-Clusters ein:</span><span class="sxs-lookup"><span data-stu-id="4cb56-128">In the **Cluster Parameters** dialog box, enter the information for the NLB cluster IP configuration:</span></span>

    -   <span data-ttu-id="4cb56-129">**IP-Adresse:** In DNS registrierte IP-Adresse des NLB-Clusters</span><span class="sxs-lookup"><span data-stu-id="4cb56-129">**IP address:** NLB cluster IP address registered in DNS</span></span>

    -   <span data-ttu-id="4cb56-130">**Subnetzmaske:** NLB-Cluster-IP-Adressen-Subnetzmaske in DNS registriert</span><span class="sxs-lookup"><span data-stu-id="4cb56-130">**Subnet mask:** NLB cluster IP address subnet mask registered in DNS</span></span>

    -   <span data-ttu-id="4cb56-131">**Vollständiger Internet Name:** FQDN des in DNS registrierten NLB-Clusternamens</span><span class="sxs-lookup"><span data-stu-id="4cb56-131">**Full Internet name:** FQDN of NLB cluster name registered in DNS</span></span>

4.  <span data-ttu-id="4cb56-132">Stellen Sie sicher, dass **Unicast** im **Cluster Betriebsmodus**ausgewählt ist, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="4cb56-132">Ensure that **Unicast** is selected in **Cluster operation mode**, and then click **Next**.</span></span>

5.  <span data-ttu-id="4cb56-133">Klicken Sie auf der Seite **Cluster-IP-Adressen** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="4cb56-133">On the **Cluster IP Addresses** page, click **Next**.</span></span>

6.  <span data-ttu-id="4cb56-134">Klicken Sie auf der Seite **Port Regeln** auf **Bearbeiten** , um die Ports zu definieren, auf die der NLB-Cluster antwortet, und konfigurieren Sie die Ports, die für die Client-zu-Standort-Systemkommunikation verwendet werden, wie Sie für die Website definiert sind, oder klicken Sie auf **weiter** , um die IP-Adresse des NLB-Clusters zu aktivieren, um auf alle TCP/IP-Ports</span><span class="sxs-lookup"><span data-stu-id="4cb56-134">On the **Port Rules** page, click **Edit** to define the ports that the NLB cluster will respond to and configure the ports that are used for client-to-site system communication as they are defined for the site, or click **Next** to enable the NLB cluster IP address to respond to all TCP/IP ports.</span></span>

    <span data-ttu-id="4cb56-135">**Hinweis**  Stellen Sie sicher, dass **Affinität** auf **Single**festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="4cb56-135">**Note** Ensure that **Affinity** is set to **Single**.</span></span>

     

7.  <span data-ttu-id="4cb56-136">Geben Sie auf der Seite **verbinden** einen Hostnamen für die MBAM-Verwaltungs-und-Überwachungsserverinstanz ein, der Teil des NLB-Clusters in **Host**sein soll, und klicken Sie dann auf **verbinden**.</span><span class="sxs-lookup"><span data-stu-id="4cb56-136">On the **Connect** page, enter an MBAM Administration and Monitoring server instance host name that will be part of the NLB cluster in **Host**, and then click **Connect**.</span></span>

8.  <span data-ttu-id="4cb56-137">Wählen Sie unter **für die Konfiguration eines neuen Clusters verfügbare Schnittstellen**die Netzwerkschnittstelle aus, die für die Reaktion auf die NLB-Clusterkommunikation konfiguriert wird, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="4cb56-137">In **Interfaces available for configuring a new cluster**, select the networking interface that will be configured to respond to NLB cluster communication, and then click **Next**.</span></span>

9.  <span data-ttu-id="4cb56-138">Überprüfen Sie auf der Seite **Host Parameter** die angezeigten Informationen, um sicherzustellen, dass die dedizierten **IP-Konfigurations** Einstellungen die dedizierte Host-IP-Konfiguration für den richtigen NLB-Clusterhost anzeigen, überprüfen Sie, ob der ursprüngliche **Standardzustand** des Hoststatus: **gestartet**ist, und klicken Sie dann auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="4cb56-138">On the **Host Parameters** page, review the information displayed to ensure that the **Dedicated IP configuration** settings display the dedicated host IP configuration for the correct NLB cluster host, check that the Initial host state **Default state:** is **Started**, and then click **Finish**.</span></span>

    <span data-ttu-id="4cb56-139">**Hinweis**  Auf der Seite " **Hostparameter** " wird auch die NLB-Cluster Host Priorität (1 bis 32) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4cb56-139">**Note** The **Host Parameters** page also displays the NLB cluster host priority, which is 1 through 32.</span></span> <span data-ttu-id="4cb56-140">Wenn dem NLB-Cluster neue Hosts hinzugefügt werden, muss sich die Hostpriorität von den zuvor hinzugefügten Hosts unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="4cb56-140">As new hosts are added to the NLB cluster, the host priority must differ from the previously added hosts.</span></span> <span data-ttu-id="4cb56-141">Die Priorität wird bei Verwendung des Netzwerklastenausgleich-Managers automatisch erhöht.</span><span class="sxs-lookup"><span data-stu-id="4cb56-141">The priority is automatically incremented when you use the Network Load Balancing Manager.</span></span>

     

10. <span data-ttu-id="4cb56-142">Klicken Sie auf \*\* &lt; NLB &gt; -Clustername\*\* , und stellen Sie sicher, dass der NLB-Hostschnittstellen **Status** **konvergiert** angezeigt wird, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="4cb56-142">Click **&lt;NLB cluster name&gt;** and ensure that the NLB host interface **Status** displays **Converged** before you continue.</span></span> <span data-ttu-id="4cb56-143">Für diesen Schritt müssen Sie möglicherweise die Anzeige des NLB-Clusters als Host-TCP/IP-Konfiguration aktualisieren, die vom NLB-Manager geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4cb56-143">This step might require that you refresh the NLB cluster display as the host TCP/IP configuration that is being modified by the NLB Manager.</span></span>

11. <span data-ttu-id="4cb56-144">Wenn Sie dem NLB-Cluster weitere Hosts hinzufügen möchten, klicken Sie mit der rechten Maustaste auf \*\* &lt; NLB-Cluster &gt; Name\*\*, klicken Sie auf **Host zu Cluster hinzufügen,** und wiederholen Sie dann die Schritte 7 bis 10 für jedes Website System, das Teil des NLB-Clusters sein wird.</span><span class="sxs-lookup"><span data-stu-id="4cb56-144">To add additional hosts to the NLB cluster, right-click **&lt;NLB cluster name&gt;**, click **Add Host to Cluster,** and then repeat steps 7 through 10 for each site system that will be part of the NLB cluster.</span></span>

12. <span data-ttu-id="4cb56-145">Ändern Sie auf einem Computer, auf dem die MBAM-Gruppenrichtlinienvorlage installiert ist, die MBAM-Gruppenrichtlinieneinstellungen, um die MBAM-Dienstendpunkte so zu konfigurieren, dass der NLB-Clustername und die entsprechende IIS-Portbindung für den Zugriff auf die auf den NLB-Clustercomputern installierten MBAM-Verwaltungs-und Überwachungs Server Features verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4cb56-145">On a computer that has MBAM Group Policy template installed, modify the MBAM Group Policy settings to configure the MBAM services endpoints to use the NLB Cluster name and the appropriate IIS port binding to access the MBAM Administration and Monitoring Server features that are installed on the NLB Cluster computers.</span></span> <span data-ttu-id="4cb56-146">Weitere Informationen zum Bearbeiten von MBAM-GPO-Einstellungen finden Sie unter [Bearbeiten von MBAM 1,0-GPO-Einstellungen](how-to-edit-mbam-10-gpo-settings.md).</span><span class="sxs-lookup"><span data-stu-id="4cb56-146">For more information about how to edit MBAM GPO settings, see [How to Edit MBAM 1.0 GPO Settings](how-to-edit-mbam-10-gpo-settings.md).</span></span> <span data-ttu-id="4cb56-147">Wenn die MBAM-Verwaltungs-und-Überwachungsserver für Ihre Umgebung neu sind, stellen Sie sicher, dass die erforderlichen Mitgliedschaften der lokalen Sicherheitsgruppe ordnungsgemäß konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="4cb56-147">If the MBAM Administration and Monitoring servers are new to your environment, ensure that the required local security group memberships have been properly configured.</span></span> <span data-ttu-id="4cb56-148">Weitere Informationen zu Sicherheitsgruppen Anforderungen finden Sie unter [Planen von MBAM 1,0-Administrator Rollen](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4cb56-148">For more information about security group requirements, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

13. <span data-ttu-id="4cb56-149">Wenn die NLB-Cluster Konfiguration abgeschlossen ist, empfehlen wir, dass Sie überprüfen, ob der NLB-Cluster MBAM-Verwaltung und-Überwachung funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="4cb56-149">When the NLB Cluster configuration is complete, we recommend that you validate that the MBAM Administration and Monitoring NLB Cluster is functional.</span></span> <span data-ttu-id="4cb56-150">Öffnen Sie dazu einen Webbrowser auf einem anderen Computer als den Servern, die im NLB konfiguriert sind, und stellen Sie sicher, dass Sie mithilfe des NLB-FQDN auf die Website MBAM-Verwaltung und-Überwachung zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="4cb56-150">To do this, open a web browser on a computer other than the servers that are configured in the NLB, and ensure that you can access the MBAM Administration and Monitoring web site by using the NLB FQDN.</span></span>

## <span data-ttu-id="4cb56-151">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="4cb56-151">Related topics</span></span>


[<span data-ttu-id="4cb56-152">Bereitstellen der Serverinfrastruktur von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="4cb56-152">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)

 

 





