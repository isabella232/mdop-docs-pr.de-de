---
title: Installieren und Konfigurieren von MBAM auf verteilten Servern
description: Installieren und Konfigurieren von MBAM auf verteilten Servern
author: dansimp
ms.assetid: 67b91e6b-ae2e-4e47-9ef2-6819aba95976
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 841b894430d14604f0fd923703708d7a3f588c07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810327"
---
# <span data-ttu-id="53c2f-103">Installieren und Konfigurieren von MBAM auf verteilten Servern</span><span class="sxs-lookup"><span data-stu-id="53c2f-103">How to Install and Configure MBAM on Distributed Servers</span></span>


<span data-ttu-id="53c2f-104">In den Verfahren in diesem Thema wird beschrieben, wie Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,0 in der eigenständigen Topologie auf verteilten Servern installieren.</span><span class="sxs-lookup"><span data-stu-id="53c2f-104">The procedures in this topic describe how to install Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 in the Stand-alone topology on distributed servers.</span></span> <span data-ttu-id="53c2f-105">Ein Diagramm der empfohlenen Architektur sowie eine Beschreibung der Datenbanken und Features finden Sie unter [Bereitstellen der MBAM 2,0-Server Infrastruktur](deploying-the-mbam-20-server-infrastructure-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="53c2f-105">To see a diagram of the recommended architecture, along with a description of the databases and features, see [Deploying the MBAM 2.0 Server Infrastructure](deploying-the-mbam-20-server-infrastructure-mbam-2.md).</span></span> <span data-ttu-id="53c2f-106">Informationen zum Installieren der Microsoft BitLocker-Verwaltung und-Überwachung mit der Configuration Manager-Topologie finden Sie unter [Bereitstellen von MBAM mit Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span><span class="sxs-lookup"><span data-stu-id="53c2f-106">To install Microsoft BitLocker Administration and Monitoring with the Configuration Manager topology, see [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span></span>

<span data-ttu-id="53c2f-107">Jedes Server Feature hat bestimmte Voraussetzungen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-107">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="53c2f-108">Wenn Sie sicherstellen möchten, dass Sie die Voraussetzungen und Hardware-und Softwareanforderungen erfüllt haben, lesen Sie [MBAM 2,0-Bereitstellungsvoraussetzungen](mbam-20-deployment-prerequisites-mbam-2.md) und [MBAM 2,0-unterstützte Konfigurationen](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="53c2f-108">To verify that you have met the prerequisites and hardware and software requirements, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) and [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span> <span data-ttu-id="53c2f-109">Darüber hinaus erfordern einige Features, dass Sie während des Installationsvorgangs bestimmte Informationen bereitstellen, um das Feature erfolgreich bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-109">In addition, some features require that you provide certain information during the installation process to successfully deploy the feature.</span></span> <span data-ttu-id="53c2f-110">Sie sollten auch die [Planung für die MBAM 2,0-Server Bereitstellung](planning-for-mbam-20-server-deployment-mbam-2.md) überprüfen, bevor Sie mit der MBAM-Bereitstellung beginnen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-110">You should also review [Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md) before you start the MBAM deployment.</span></span>

**<span data-ttu-id="53c2f-111">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="53c2f-111">Note</span></span>**  
<span data-ttu-id="53c2f-112">Um die Setupprotokolldateien zu erhalten, müssen Sie das msiexec-Paket und die Option **/l** &lt; Location verwenden, &gt; um MBAM zu installieren.</span><span class="sxs-lookup"><span data-stu-id="53c2f-112">To obtain the setup log files, you have to use the Msiexec package and the **/L** &lt;location&gt; option to install MBAM.</span></span> <span data-ttu-id="53c2f-113">Protokolldateien werden an dem von Ihnen angegebenen Speicherort erstellt.</span><span class="sxs-lookup"><span data-stu-id="53c2f-113">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="53c2f-114">Zusätzliche Setupprotokolldateien werden im Ordner% Temp% auf dem Server des Benutzers erstellt, der MBAM installiert.</span><span class="sxs-lookup"><span data-stu-id="53c2f-114">Additional setup log files are created in the %temp% folder on the server of the user who is installing MBAM.</span></span>



## <a href="" id="deploying-mbam-server-features-"></a><span data-ttu-id="53c2f-115">Bereitstellen von MBAM-Server Features</span><span class="sxs-lookup"><span data-stu-id="53c2f-115">Deploying MBAM Server Features</span></span>


<span data-ttu-id="53c2f-116">In den folgenden Schritten wird beschrieben, wie allgemeine MBAM-Features installiert werden.</span><span class="sxs-lookup"><span data-stu-id="53c2f-116">The following steps describe how to install general MBAM features.</span></span>

**<span data-ttu-id="53c2f-117">So starten Sie den MBAM-Server Installations-Assistenten</span><span class="sxs-lookup"><span data-stu-id="53c2f-117">To start the MBAM Server installation wizard</span></span>**

1.  <span data-ttu-id="53c2f-118">Führen Sie auf dem Server, auf dem Sie die Microsoft BitLocker-Verwaltung und-Überwachung installieren möchten, **MBAMSetup.exe** aus, um den MBAM-Installations-Assistenten zu starten.</span><span class="sxs-lookup"><span data-stu-id="53c2f-118">On the server where you want to install Microsoft BitLocker Administration and Monitoring, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="53c2f-119">Wählen Sie auf der **Willkommens** Seite optional das **Programm zur Verbesserung der Benutzerfreundlichkeit**aus, und klicken Sie dann auf **Start**.</span><span class="sxs-lookup"><span data-stu-id="53c2f-119">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="53c2f-120">Lesen und akzeptieren Sie den Microsoft-Software-Lizenzvertrag, und klicken Sie auf **weiter** , um die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-120">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="53c2f-121">Wählen Sie auf der Seite **Topologie Auswahl** die **eigenständige** Topologie aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="53c2f-121">On the **Topology Selection** page, select the **Stand-alone** topology, and then click **Next**.</span></span>

    **<span data-ttu-id="53c2f-122">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="53c2f-122">Note</span></span>**  
    <span data-ttu-id="53c2f-123">Wenn Sie MBAM mit der integrierten Configuration Manager-Topologie installieren möchten, lesen Sie [Bereitstellen von MBAM mit Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span><span class="sxs-lookup"><span data-stu-id="53c2f-123">If you want to install MBAM with the Configuration Manager integrated topology, see [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span></span>



5.  <span data-ttu-id="53c2f-124">Wählen Sie die Features aus, die Sie installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="53c2f-124">Select the features that you want to install.</span></span> <span data-ttu-id="53c2f-125">Standardmäßig sind alle MBAM-Features für die Installation ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="53c2f-125">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="53c2f-126">Deaktivieren Sie die Features, die Sie an anderer Stelle installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="53c2f-126">Clear the features that you want to install elsewhere.</span></span> <span data-ttu-id="53c2f-127">Features, die auf demselben Computer installiert werden, müssen zur gleichen Zeit zusammen installiert werden.</span><span class="sxs-lookup"><span data-stu-id="53c2f-127">Features that will be installed on the same computer must be installed together at the same time.</span></span> <span data-ttu-id="53c2f-128">Sie müssen die MBAM-Features in der folgenden Reihenfolge installieren:</span><span class="sxs-lookup"><span data-stu-id="53c2f-128">You must install MBAM features in the following order:</span></span>

    -   <span data-ttu-id="53c2f-129">Wiederherstellungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="53c2f-129">Recovery Database</span></span>

    -   <span data-ttu-id="53c2f-130">Konformitäts-und Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="53c2f-130">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="53c2f-131">Konformitäts-und Überwachungsberichte</span><span class="sxs-lookup"><span data-stu-id="53c2f-131">Compliance and Audit Reports</span></span>

    -   <span data-ttu-id="53c2f-132">Self-Service-Portal</span><span class="sxs-lookup"><span data-stu-id="53c2f-132">Self-Service Portal</span></span>

    -   <span data-ttu-id="53c2f-133">Verwaltungs-und Überwachungs Server</span><span class="sxs-lookup"><span data-stu-id="53c2f-133">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="53c2f-134">MBAM-Gruppenrichtlinienvorlage</span><span class="sxs-lookup"><span data-stu-id="53c2f-134">MBAM Group Policy template</span></span>

    **<span data-ttu-id="53c2f-135">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="53c2f-135">Note</span></span>**  
    <span data-ttu-id="53c2f-136">Der Installations-Assistent überprüft die Voraussetzungen für die Installation und zeigt die fehlenden Voraussetzungen an.</span><span class="sxs-lookup"><span data-stu-id="53c2f-136">The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="53c2f-137">Wenn alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="53c2f-137">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="53c2f-138">Wenn eine fehlende Voraussetzung erkannt wird, müssen Sie die fehlenden Voraussetzungen beheben und dann **erneut auf Voraussetzungen prüfen**klicken.</span><span class="sxs-lookup"><span data-stu-id="53c2f-138">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="53c2f-139">Wenn dieses Mal alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="53c2f-139">If all prerequisites are met this time, the installation resumes.</span></span>



~~~
The MBAM Setup wizard displays installation pages for the features that you select. The following sections describe the installation procedures for each feature.

**Note**  
For the following instructions, it is assumed that each feature is to be installed on a separate server. If you install multiple features on a single server, you can change or eliminate some steps.
~~~



**<span data-ttu-id="53c2f-140">So installieren Sie die Wiederherstellungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="53c2f-140">To install the Recovery Database</span></span>**

1.  <span data-ttu-id="53c2f-141">Geben Sie auf der Seite " **Wiederherstellungsdatenbank konfigurieren** " die Namen der Computer an, auf denen das Feature "Verwaltungs-und Überwachungs Server" ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="53c2f-141">On the **Configure the Recovery database** page, specify the names of the computers that will be running the Administration and Monitoring Server feature.</span></span> <span data-ttu-id="53c2f-142">Nach der Bereitstellung des Verwaltungs-und Überwachungs Server Features wird mit dem Domänenkonto eine Verbindung mit der Datenbank hergestellt.</span><span class="sxs-lookup"><span data-stu-id="53c2f-142">After the Administration and Monitoring Server feature is deployed, it uses its domain account to connect to the database.</span></span>

2.  <span data-ttu-id="53c2f-143">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-143">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="53c2f-144">Geben Sie den Namen der SQL Server-Instanz und den Namen der Datenbank an, in der die Wiederherstellungsdaten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-144">Specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="53c2f-145">Sie müssen außerdem angeben, an welcher Stelle die Datenbank gespeichert werden soll und wo sich die Protokollinformationen befinden sollen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-145">You must also specify both where the database will be located and where the log information will be located.</span></span>

4.  <span data-ttu-id="53c2f-146">Klicken Sie auf **weiter** , um mit dem MBAM-Setup-Assistenten fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="53c2f-146">Click **Next** to continue with the MBAM Setup wizard.</span></span>

**<span data-ttu-id="53c2f-147">So installieren Sie die Konformitäts-und Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="53c2f-147">To install the Compliance and Audit Database</span></span>**

1.  <span data-ttu-id="53c2f-148">Geben Sie auf der Seite **Compliance-und Überwachungsdatenbank konfigurieren** das Benutzerkonto an, das für den Zugriff auf die Datenbank für Berichte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="53c2f-148">On the **Configure the Compliance and Audit Database** page, specify the user account that will be used to access the database for reports.</span></span>

2.  <span data-ttu-id="53c2f-149">Geben Sie die Computernamen der Computer an, auf denen der Verwaltungs-und Überwachungs Server ausgeführt werden soll, sowie die Konformitäts-und Überwachungsberichte.</span><span class="sxs-lookup"><span data-stu-id="53c2f-149">Specify the computer names of the computers that will be running the Administration and Monitoring Server and the Compliance and Audit Reports.</span></span> <span data-ttu-id="53c2f-150">Nachdem die Verwaltung und Überwachung sowie der Server für Konformitäts-und Überwachungsberichte bereitgestellt wurden, verwenden Sie Ihre Domänenkonten, um eine Verbindung mit den Datenbankenherzustellen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-150">After the Administration and Monitoring and the Compliance and Audit Reports Server are deployed, they use their domain accounts to connect to the databases.</span></span>

    **<span data-ttu-id="53c2f-151">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="53c2f-151">Note</span></span>**  
    <span data-ttu-id="53c2f-152">Wenn Sie die Konformitäts-und Überwachungsdatenbank ohne das Feature Konformitäts-und Überwachungsberichte installieren, müssen Sie auf dem Computer Compliance-und Überwachungsdatenbank eine Ausnahme hinzufügen, um eingehenden Datenverkehr auf dem Microsoft SQL Server-Port zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="53c2f-152">If you are installing the Compliance and Audit Database without the Compliance and Audit Reports feature, you must add an exception on the Compliance and Audit Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="53c2f-153">Die Standardportnummer ist 1433.</span><span class="sxs-lookup"><span data-stu-id="53c2f-153">The default port number is 1433.</span></span>



3.  <span data-ttu-id="53c2f-154">Geben Sie den Namen der SQL Server-Instanz und den Namen der Datenbank an, in der die Konformitäts-und Überwachungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="53c2f-154">Specify the SQL Server instance name and the name of the database that will store the compliance and audit data.</span></span> <span data-ttu-id="53c2f-155">Sie müssen außerdem angeben, wo sich die Datenbank-und Protokollinformationen befinden sollen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-155">You must also specify where the database and log information will be located.</span></span>

4.  <span data-ttu-id="53c2f-156">Klicken Sie auf **weiter** , um den Setup-Assistenten für Microsoft BitLocker-Verwaltung und-Überwachung fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-156">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

**<span data-ttu-id="53c2f-157">So installieren Sie die Konformitäts-und Überwachungsberichte</span><span class="sxs-lookup"><span data-stu-id="53c2f-157">To install the Compliance and Audit Reports</span></span>**

1.  <span data-ttu-id="53c2f-158">Geben Sie auf der Seite **Compliance-und Überwachungsberichte konfigurieren** den Namen der Remote-SQL Server-Instanz an (beispielsweise &lt; Servername &gt; ), in dem die Kompatibilitäts-und Überwachungsdatenbank installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="53c2f-158">On the **Configure the Compliance and Audit Reports** page, specify the remote SQL Server instance name (for example, &lt;ServerName&gt;) where the Compliance and Audit Database was installed.</span></span>

    **<span data-ttu-id="53c2f-159">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="53c2f-159">Note</span></span>**  
    <span data-ttu-id="53c2f-160">Wenn Sie die Konformitäts-und Überwachungsberichte ohne den Verwaltungs-und Überwachungsserver installieren, müssen Sie auf dem Computer für Konformitäts-und Überwachungsberichte eine Ausnahme hinzufügen, um eingehenden Datenverkehr auf dem Reporting Server-Port zu aktivieren (der Standardport ist 80).</span><span class="sxs-lookup"><span data-stu-id="53c2f-160">If you are installing the Compliance and Audit Reports without the Administration and Monitoring Server, you must add an exception on the Compliance and Audit Report computer to enable inbound traffic on the Reporting Server port (the default port is 80).</span></span>



2.  <span data-ttu-id="53c2f-161">Geben Sie den Namen der Konformitäts-und Überwachungsdatenbank an.</span><span class="sxs-lookup"><span data-stu-id="53c2f-161">Specify the name of the Compliance and Audit Database.</span></span> <span data-ttu-id="53c2f-162">Standardmäßig ist der Datenbankname MBAM-Konformitäts Status, obwohl Sie den Namen beim Installieren der Konformitäts-und Überwachungsdatenbank ändern können.</span><span class="sxs-lookup"><span data-stu-id="53c2f-162">By default, the database name is MBAM Compliance Status, although you can change the name when you install the Compliance and Audit Database.</span></span>

3.  <span data-ttu-id="53c2f-163">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-163">Click **Next** to continue.</span></span>

4.  <span data-ttu-id="53c2f-164">Wählen Sie die Instanz von SQL Server Reporting Services aus, in der die Kompatibilitäts-und Überwachungsberichte installiert werden.</span><span class="sxs-lookup"><span data-stu-id="53c2f-164">Select the instance of SQL Server Reporting Services where the Compliance and Audit Reports will be installed.</span></span> <span data-ttu-id="53c2f-165">Stellen Sie ein Domänenbenutzerkonto und ein Kennwort für den Zugriff auf die Datenbank Compliance und Audit bereit.</span><span class="sxs-lookup"><span data-stu-id="53c2f-165">Provide a domain user account and password to access the Compliance and Audit Database.</span></span> <span data-ttu-id="53c2f-166">Konfigurieren Sie das Kennwort für dieses Konto so, dass es nie abläuft.</span><span class="sxs-lookup"><span data-stu-id="53c2f-166">Configure the password for this account to never expire.</span></span> <span data-ttu-id="53c2f-167">Das Benutzerkonto sollte auf alle Daten zugreifen können, die für die Gruppe MBAM-Berichte Benutzer verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="53c2f-167">The user account should be able to access all data that is available to the MBAM Reports Users group.</span></span>

5.  <span data-ttu-id="53c2f-168">Klicken Sie auf **weiter** , um den Setup-Assistenten für Microsoft BitLocker-Verwaltung und-Überwachung fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-168">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

**<span data-ttu-id="53c2f-169">So installieren Sie das Self-Service-Portal</span><span class="sxs-lookup"><span data-stu-id="53c2f-169">To install the Self-Service Portal</span></span>**

1.  <span data-ttu-id="53c2f-170">Auf der Seite **Self-Service-Portal konfigurieren** können Sie optional die Kommunikation zwischen dem Self-Service-Portal und den Verwaltungs-und Überwachungs Servern verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="53c2f-170">On the **Configure the Self-Service Portal** page, you can optionally encrypt the communication between the Self-Service Portal and the Administration and Monitoring servers.</span></span> <span data-ttu-id="53c2f-171">Wenn Sie die Option zum Verschlüsseln der Kommunikation auswählen, werden Sie aufgefordert, das Zertifikat der Zertifizierungsstelle zu wählen, das für die Verschlüsselung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="53c2f-171">If you choose the option to encrypt the communication, you are prompted to select the certification authority-provisioned certificate to use for encryption.</span></span>

2.  <span data-ttu-id="53c2f-172">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-172">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="53c2f-173">Geben Sie die Remoteinstanz von SQL Server an (beispielsweise \* &lt; Servername &gt; \*), in der die Kompatibilitäts-und Überwachungsdatenbank installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="53c2f-173">Specify the remote instance of SQL Server (for example, *&lt;ServerName&gt;*) where the Compliance and Audit Database was installed.</span></span>

4.  <span data-ttu-id="53c2f-174">Geben Sie den Namen der Konformitäts-und Überwachungsdatenbank an.</span><span class="sxs-lookup"><span data-stu-id="53c2f-174">Specify the name of the Compliance and Audit Database.</span></span> <span data-ttu-id="53c2f-175">Standardmäßig ist der Datenbankname MBAM-Konformitäts Status.</span><span class="sxs-lookup"><span data-stu-id="53c2f-175">By default, the database name is MBAM Compliance Status.</span></span> <span data-ttu-id="53c2f-176">Sie können den Namen jedoch ändern, wenn Sie die Kompatibilitäts-und Überwachungsdatenbank installieren.</span><span class="sxs-lookup"><span data-stu-id="53c2f-176">However, you can change the name when you install the Compliance and Audit Database.</span></span>

5.  <span data-ttu-id="53c2f-177">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-177">Click **Next** to continue.</span></span>

6.  <span data-ttu-id="53c2f-178">Geben Sie die Remoteinstanz von SQL Server an (beispielsweise \* &lt; Servername &gt; \*), in der die Wiederherstellungsdatenbank installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="53c2f-178">Specify the remote instance of SQL Server (for example, *&lt;ServerName&gt;*) where the Recovery Database was installed.</span></span>

7.  <span data-ttu-id="53c2f-179">Geben Sie den Namen der Wiederherstellungsdatenbank an.</span><span class="sxs-lookup"><span data-stu-id="53c2f-179">Specify the name of the Recovery Database.</span></span> <span data-ttu-id="53c2f-180">Standardmäßig ist der Datenbankname **MBAM-Wiederherstellung und-Hardware**.</span><span class="sxs-lookup"><span data-stu-id="53c2f-180">By default, the database name is **MBAM Recovery and Hardware**.</span></span> <span data-ttu-id="53c2f-181">Sie können den Namen jedoch bei der Installation des Wiederherstellungsdaten Bank Features ändern.</span><span class="sxs-lookup"><span data-stu-id="53c2f-181">However, you can change the name when you install the Recovery Database feature.</span></span>

8.  <span data-ttu-id="53c2f-182">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-182">Click **Next** to continue.</span></span>

9.  <span data-ttu-id="53c2f-183">Geben Sie die **Port Nummer**, den **Hostnamen** (optional) und den **Installationspfad** für den MBAM-Verwaltungs-und-Überwachungs Server ein.</span><span class="sxs-lookup"><span data-stu-id="53c2f-183">Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring Server.</span></span>

    **<span data-ttu-id="53c2f-184">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="53c2f-184">Note</span></span>**  
    <span data-ttu-id="53c2f-185">Die von Ihnen angegebene Portnummer muss eine nicht verwendete Portnummer auf dem Verwaltungs-und Überwachungsserver sein, sofern Sie keinen eindeutigen Hostheadernamen angeben.</span><span class="sxs-lookup"><span data-stu-id="53c2f-185">The port number that you specify must be an unused port number on the Administration and Monitoring server unless you specify a unique host header name.</span></span> <span data-ttu-id="53c2f-186">Wenn Sie die Windows-Firewall verwenden, wird der Port automatisch geöffnet.</span><span class="sxs-lookup"><span data-stu-id="53c2f-186">If you are using Windows Firewall, the port will be opened automatically.</span></span>



10. <span data-ttu-id="53c2f-187">Wenn Sie optional einen Dienstprinzipalnamen (Service Principal Name, SPN) für das Self-Service-Portal registrieren möchten, wählen Sie **Dienstprinzipalnamen (Service Principal Names, SPN) dieses Computers registrieren für Active Directory (für die Windows-Authentifizierung erforderlich)** aus.</span><span class="sxs-lookup"><span data-stu-id="53c2f-187">To optionally register a Service Principal Name (SPN) for the Self-Service Portal, select **Register this machine’s Service Principal Names (SPN) with Active Directory (Required for Windows Authentication)**.</span></span> <span data-ttu-id="53c2f-188">Wenn Sie dieses Kontrollkästchen aktivieren, versucht MBAM Setup nicht, die vorhandenen SPNs zu registrieren, und Sie können den SPN vor oder nach der Installation von MBAM manuell registrieren.</span><span class="sxs-lookup"><span data-stu-id="53c2f-188">If you select this check box, MBAM Setup will not try to register the existing SPNs, and you can manually register the SPN before or after the MBAM installation.</span></span> <span data-ttu-id="53c2f-189">Anweisungen zum manuellen Registrieren des SPN finden Sie unter [Manuelle SPN-Registrierung](https://go.microsoft.com/fwlink/?LinkId=286758).</span><span class="sxs-lookup"><span data-stu-id="53c2f-189">For instructions on registering the SPN manually, see [Manual SPN Registration](https://go.microsoft.com/fwlink/?LinkId=286758).</span></span>

11. <span data-ttu-id="53c2f-190">Klicken Sie auf **weiter** , um den Setup-Assistenten für Microsoft BitLocker-Verwaltung und-Überwachung fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-190">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

12. <span data-ttu-id="53c2f-191">Geben Sie an, ob Microsoft Updates dazu beitragen soll, Ihren Computer zu schützen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="53c2f-191">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span>

13. <span data-ttu-id="53c2f-192">Wenn die ausgewählten MBAM-Funktionsinformationen abgeschlossen sind, können Sie die MBAM-Installation mithilfe des Setup-Assistenten starten.</span><span class="sxs-lookup"><span data-stu-id="53c2f-192">When the selected MBAM feature information is completed, you are ready to start the MBAM installation by using the Setup wizard.</span></span> <span data-ttu-id="53c2f-193">Klicken Sie auf **zurück** , um den Assistenten zu durchlaufen, wenn Sie Ihre Installationseinstellungen überprüfen oder ändern müssen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-193">Click **Back** to move through the wizard if you have to review or change your installation settings.</span></span> <span data-ttu-id="53c2f-194">Klicken Sie auf **Installieren** , um die Installation zu starten.</span><span class="sxs-lookup"><span data-stu-id="53c2f-194">Click **Install** to start the installation.</span></span> <span data-ttu-id="53c2f-195">Klicken Sie auf **Abbrechen** , um den Assistenten zu beenden.</span><span class="sxs-lookup"><span data-stu-id="53c2f-195">Click **Cancel** to exit the wizard.</span></span> <span data-ttu-id="53c2f-196">Setup installiert die von Ihnen ausgewählten MBAM-Features und benachrichtigt Sie, dass die Installation abzuschließen ist.</span><span class="sxs-lookup"><span data-stu-id="53c2f-196">Setup installs the MBAM features that you selected and notifies you that the installation is finished.</span></span>

14. <span data-ttu-id="53c2f-197">Klicken Sie auf **Fertig stellen** , um den Assistenten zu beenden.</span><span class="sxs-lookup"><span data-stu-id="53c2f-197">Click **Finish** to exit the wizard.</span></span>

    **<span data-ttu-id="53c2f-198">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="53c2f-198">Note</span></span>**  
    <span data-ttu-id="53c2f-199">Wenn Sie das Self-Service-Portal nach der Installation konfigurieren möchten, sollten Sie das Self-Service-Portal mit dem Namen Ihres Unternehmens und anderen unternehmensspezifischen Informationen versehen, und erfahren Sie, wie Sie das Self- [Service-Portal](how-to-brand-the-self-service-portal.md) für Anweisungen kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-199">To configure the Self-Service Portal after you installed it, brand the Self-Service Portal with your company name and other company-specific information, see [How to Brand the Self-Service Portal](how-to-brand-the-self-service-portal.md) for instructions.</span></span>



15. <span data-ttu-id="53c2f-200">Wenn die Clientcomputer Zugriff auf das Microsoft Content Delivery Network (CDN) haben, das dem Self-Service-Portal den erforderlichen Zugriff auf bestimmte JavaScript-Dateien gewährt, sind Sie mit der Installation des Self-Service-Portals am Ende.</span><span class="sxs-lookup"><span data-stu-id="53c2f-200">If the client computers have access to the Microsoft Content Delivery Network (CDN), which gives the Self-Service Portal the required access to certain JavaScript files, you are finished with the Self-Service Portal installation.</span></span> <span data-ttu-id="53c2f-201">Wenn die Clientcomputer keinen Zugriff auf das Microsoft CDN haben, führen Sie die Schritte im nächsten Abschnitt aus, um das Self-Service-Portal so zu konfigurieren, dass es von einer barrierefreien Quelle aus auf die JavaScript-Dateien verweist.</span><span class="sxs-lookup"><span data-stu-id="53c2f-201">If the client computers does not have access to the Microsoft CDN, complete the steps in the next section to configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span>

**<span data-ttu-id="53c2f-202">So konfigurieren Sie das Self-Service-Portal, wenn Endbenutzer nicht auf das Microsoft Content Delivery Network zugreifen können</span><span class="sxs-lookup"><span data-stu-id="53c2f-202">To configure the Self-Service Portal when end users cannot access the Microsoft Content Delivery Network</span></span>**

1. <span data-ttu-id="53c2f-203">Wenn die Clientcomputer Zugriff auf das Microsoft Content Delivery Network (CDN) haben, das dem Self-Service-Portal den erforderlichen Zugriff auf bestimmte JavaScript-Dateien gewährt, ist die Self-Service-Portal-Installation abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-203">If the client computers have access to the Microsoft Content Delivery Network (CDN), which gives the Self-Service Portal the required access to certain JavaScript files, the Self-Service Portal installation is completed.</span></span> <span data-ttu-id="53c2f-204">Wenn die Clientcomputer keinen Zugriff auf das Microsoft CDN haben, führen Sie die verbleibenden Schritte in diesem Abschnitt aus, um das Self-Service-Portal so zu konfigurieren, dass es von einer barrierefreien Quelle aus auf die JavaScript-Dateien verweist.</span><span class="sxs-lookup"><span data-stu-id="53c2f-204">If the client computers do not have access to the Microsoft CDN, complete the remaining steps in this section to configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span>

2. <span data-ttu-id="53c2f-205">Laden Sie die vier JavaScript-Dateien aus dem Microsoft CDN herunter:</span><span class="sxs-lookup"><span data-stu-id="53c2f-205">Download the four JavaScript files from the Microsoft CDN:</span></span>

   -   <span data-ttu-id="53c2f-206">jQuery-1.7.2.min.js-[https://go.microsoft.com/p/fwlink/?LinkID=271736](https://go.microsoft.com/fwlink/p/?LinkID=271736)</span><span class="sxs-lookup"><span data-stu-id="53c2f-206">jQuery-1.7.2.min.js - [https://go.microsoft.com/p/fwlink/?LinkID=271736](https://go.microsoft.com/fwlink/p/?LinkID=271736)</span></span>

   -   <span data-ttu-id="53c2f-207">MicrosoftAjax.js –[https://go.microsoft.com/p/fwlink/?LinkId=272283](https://go.microsoft.com/fwlink/p/?LinkId=272283)</span><span class="sxs-lookup"><span data-stu-id="53c2f-207">MicrosoftAjax.js –[https://go.microsoft.com/p/fwlink/?LinkId=272283](https://go.microsoft.com/fwlink/p/?LinkId=272283)</span></span>

   -   <span data-ttu-id="53c2f-208">MicrosoftMvcAjax.js-[https://go.microsoft.com/p/fwlink/?LinkId=272284](https://go.microsoft.com/fwlink/p/?LinkId=272284)</span><span class="sxs-lookup"><span data-stu-id="53c2f-208">MicrosoftMvcAjax.js - [https://go.microsoft.com/p/fwlink/?LinkId=272284](https://go.microsoft.com/fwlink/p/?LinkId=272284)</span></span>

   -   <span data-ttu-id="53c2f-209">MicrosoftMvcValidation.js-</span><span class="sxs-lookup"><span data-stu-id="53c2f-209">MicrosoftMvcValidation.js -</span></span> <https://go.microsoft.com/fwlink/p/?LinkId=272285>

3. <span data-ttu-id="53c2f-210">Kopieren Sie die JavaScript-Dateien in das Verzeichnis **Skripts** des Self-Service-Portals.</span><span class="sxs-lookup"><span data-stu-id="53c2f-210">Copy the JavaScript files to the **Scripts** directory of the Self-Service Portal.</span></span> <span data-ttu-id="53c2f-211">Dieses Verzeichnis befindet sich in <em> &lt; MBAM Self-Service-Installationsverzeichnis &gt; \\ </em> Self-Service Website\\Scripts.</span><span class="sxs-lookup"><span data-stu-id="53c2f-211">This directory is located in <em>&lt;MBAM Self-Service Install Directory&gt;\\</em>Self Service Website\\Scripts.</span></span>

4. <span data-ttu-id="53c2f-212">Öffnen Sie **Internet Informationsdienste (IIS)-Manager**.</span><span class="sxs-lookup"><span data-stu-id="53c2f-212">Open **Internet Information Services (IIS) Manager**.</span></span>

5. <span data-ttu-id="53c2f-213">Erweitern Sie **Sites** &gt; **Microsoft BitLocker-Verwaltung und-Überwachung**, und markieren Sie **Selfservice**.</span><span class="sxs-lookup"><span data-stu-id="53c2f-213">Expand **Sites** &gt; **Microsoft BitLocker Administration and Monitoring**, and highlight **SelfService**.</span></span>

   **<span data-ttu-id="53c2f-214">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="53c2f-214">Note</span></span>**  
   <span data-ttu-id="53c2f-215">*Selfservice* ist der Name des virtuellen Standardverzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="53c2f-215">*SelfService* is the default virtual directory name.</span></span> <span data-ttu-id="53c2f-216">Wenn Sie während der Installation einen anderen Namen für dieses Verzeichnis gewählt haben, vergessen Sie nicht, *Selfservice* in den restlichen Anweisungen durch den von Ihnen gewählten Namen zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-216">If you chose a different name for this directory during installation, remember to replace *SelfService* in the rest of these instructions with the name you chose.</span></span>



6. <span data-ttu-id="53c2f-217">Doppelklicken Sie im mittleren Bereich auf **Anwendungseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="53c2f-217">In the middle pane, double-click **Application Settings**.</span></span>

7. <span data-ttu-id="53c2f-218">Bearbeiten Sie für jedes Element in der folgenden Liste die Anwendungseinstellungen, um auf den neuen Speicherort zu verweisen, indem &lt; Sie virtuelles Verzeichnis durch &gt; /Selfservice/ersetzen (oder den Namen, den Sie während der Installation ausgewählt haben).</span><span class="sxs-lookup"><span data-stu-id="53c2f-218">For each item in the following list, edit the application settings to reference the new location by replacing &lt;virtual directory&gt; with /SelfService/ (or the name you chose during installation).</span></span> <span data-ttu-id="53c2f-219">Beispielsweise ist der Pfad des virtuellen Verzeichnisses mit/Selfservice/Scripts/jquery-1.7.2.min.js vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="53c2f-219">For example, the virtual directory path will be similar to /selfservice/scripts/jquery-1.7.2.min.js.</span></span>

   -   <span data-ttu-id="53c2f-220">jQueryPath:/ &lt; virtuelles Verzeichnis &gt; /Scripts/jQuery-1.7.2.min.js</span><span class="sxs-lookup"><span data-stu-id="53c2f-220">jQueryPath: /&lt;virtual directory&gt;/Scripts/ jQuery-1.7.2.min.js</span></span>

   -   <span data-ttu-id="53c2f-221">MicrosoftAjaxPath:/ &lt; virtuelles Verzeichnis &gt; /Scripts/MicrosoftAjax.js</span><span class="sxs-lookup"><span data-stu-id="53c2f-221">MicrosoftAjaxPath: /&lt;virtual directory&gt;/Scripts/ MicrosoftAjax.js</span></span>

   -   <span data-ttu-id="53c2f-222">MicrosoftMvcAjaxPath:/ &lt; virtuelles Verzeichnis &gt; /Scripts/MicrosoftMvcAjax.js</span><span class="sxs-lookup"><span data-stu-id="53c2f-222">MicrosoftMvcAjaxPath: /&lt;virtual directory&gt;/Scripts/ MicrosoftMvcAjax.js</span></span>

   -   <span data-ttu-id="53c2f-223">MicrosoftMvcValidationPath:/ &lt; virtuelles Verzeichnis &gt; /Scripts/MicrosoftMvcValidation.js</span><span class="sxs-lookup"><span data-stu-id="53c2f-223">MicrosoftMvcValidationPath: /&lt;virtual directory&gt;/Scripts/ MicrosoftMvcValidation.js</span></span>

**<span data-ttu-id="53c2f-224">So installieren Sie das Feature "Verwaltungs-und Überwachungs Server"</span><span class="sxs-lookup"><span data-stu-id="53c2f-224">To install the Administration and Monitoring Server feature</span></span>**

1. <span data-ttu-id="53c2f-225">MBAM kann die Kommunikation zwischen den Webdiensten und den Verwaltungs-und Überwachungs Servern verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="53c2f-225">MBAM can encrypt the communication between the Web Services and the Administration and Monitoring servers.</span></span> <span data-ttu-id="53c2f-226">Wenn Sie die Option zum Verschlüsseln der Kommunikation auswählen, werden Sie aufgefordert, das Zertifikat der Zertifizierungsstelle zu wählen, das für die Verschlüsselung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="53c2f-226">If you choose the option to encrypt the communication, you are prompted to select the certification authority-provisioned certificate to use for encryption.</span></span>

2. <span data-ttu-id="53c2f-227">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-227">Click **Next** to continue.</span></span>

3. <span data-ttu-id="53c2f-228">Geben Sie die Remoteinstanz von SQL Server an (beispielsweise \* &lt; Servername &gt; \*), in der die Kompatibilitäts-und Überwachungsdatenbank installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="53c2f-228">Specify the remote instance of SQL Server (for example: *&lt;ServerName&gt;*) where the Compliance and Audit Database was installed.</span></span>

4. <span data-ttu-id="53c2f-229">Geben Sie den Namen der Konformitäts-und Überwachungsdatenbank an.</span><span class="sxs-lookup"><span data-stu-id="53c2f-229">Specify the name of the Compliance and Audit Database.</span></span> <span data-ttu-id="53c2f-230">Standardmäßig ist der Datenbankname MBAM-Konformitäts Status.</span><span class="sxs-lookup"><span data-stu-id="53c2f-230">By default, the database name is MBAM Compliance Status.</span></span> <span data-ttu-id="53c2f-231">Sie können den Namen jedoch ändern, wenn Sie die Kompatibilitäts-und Überwachungsdatenbank installieren.</span><span class="sxs-lookup"><span data-stu-id="53c2f-231">However, you can change the name when you install the Compliance and Audit Database.</span></span>

5. <span data-ttu-id="53c2f-232">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-232">Click **Next** to continue.</span></span>

6. <span data-ttu-id="53c2f-233">Geben Sie die Remoteinstanz von SQL Server an, auf der die Wiederherstellungsdatenbank installiert wurde (beispielsweise: \* &lt; Servername &gt; \*).</span><span class="sxs-lookup"><span data-stu-id="53c2f-233">Specify the remote instance of SQL Server (for example: *&lt;ServerName&gt;*) where the Recovery Database was installed.</span></span>

7. <span data-ttu-id="53c2f-234">Geben Sie den Namen der Wiederherstellungsdatenbank an.</span><span class="sxs-lookup"><span data-stu-id="53c2f-234">Specify the name of the Recovery Database.</span></span> <span data-ttu-id="53c2f-235">Standardmäßig ist der Datenbankname **MBAM-Wiederherstellung und-Hardware**.</span><span class="sxs-lookup"><span data-stu-id="53c2f-235">By default, the database name is **MBAM Recovery and Hardware**.</span></span> <span data-ttu-id="53c2f-236">Sie können den Namen jedoch bei der Installation des Wiederherstellungsdaten Bank Features ändern.</span><span class="sxs-lookup"><span data-stu-id="53c2f-236">However, you can change the name when you install the Recovery Database feature.</span></span>

8. <span data-ttu-id="53c2f-237">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-237">Click **Next** to continue.</span></span>

9. <span data-ttu-id="53c2f-238">Geben Sie die URL für das "Home" der SQL Server Reporting Services (SRS)-Website an.</span><span class="sxs-lookup"><span data-stu-id="53c2f-238">Specify the URL for the “Home” of the SQL Server Reporting Services (SRS) site.</span></span> <span data-ttu-id="53c2f-239">Der standardmäßige Startspeicherort einer SQL Server Reporting Services-Websiteinstanz lautet:</span><span class="sxs-lookup"><span data-stu-id="53c2f-239">The default Home location of a SQL Server Reporting Services site instance is at:</span></span>

   <span data-ttu-id="53c2f-240">http:// <em> &lt; NameofMBAMReportsServer &gt; / </em> Report Server</span><span class="sxs-lookup"><span data-stu-id="53c2f-240">http://<em>&lt;NameofMBAMReportsServer&gt;/</em>ReportServer</span></span>

   **<span data-ttu-id="53c2f-241">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="53c2f-241">Note</span></span>**  
   <span data-ttu-id="53c2f-242">Wenn SQL Server Reporting Services als benannte Instanz konfiguriert wurde, sieht die URL wie folgt aus: http://\* &lt; NameofMBAMReportsServer &gt; */ReportServer\_* &lt; SRSInstanceName &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="53c2f-242">If SQL Server Reporting Services was configured as a named instance, the URL resembles the following: http://*&lt;NameofMBAMReportsServer&gt;*/ReportServer\_*&lt;SRSInstanceName&gt;*.</span></span>



10. <span data-ttu-id="53c2f-243">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-243">Click **Next** to continue.</span></span>

11. <span data-ttu-id="53c2f-244">Geben Sie die **Port Nummer**, den **Hostnamen** (optional) und den **Installationspfad** für den MBAM-Verwaltungs-und-Überwachungs Server ein.</span><span class="sxs-lookup"><span data-stu-id="53c2f-244">Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring Server.</span></span>

    **<span data-ttu-id="53c2f-245">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="53c2f-245">Note</span></span>**  
    <span data-ttu-id="53c2f-246">Die von Ihnen angegebene Portnummer muss eine nicht verwendete Portnummer auf dem Verwaltungs-und Überwachungsserver sein, sofern Sie keinen eindeutigen Hostheadernamen angeben.</span><span class="sxs-lookup"><span data-stu-id="53c2f-246">The port number that you specify must be an unused port number on the Administration and Monitoring server unless you specify a unique host header name.</span></span> <span data-ttu-id="53c2f-247">Wenn Sie die Windows-Firewall verwenden, wird der Port automatisch geöffnet.</span><span class="sxs-lookup"><span data-stu-id="53c2f-247">If you are using Windows Firewall, the port will be opened automatically.</span></span>



12. <span data-ttu-id="53c2f-248">Wenn Sie optional einen Dienstprinzipalnamen (Service Principal Name, SPN) für das Self-Service-Portal registrieren möchten, wählen Sie **Dienstprinzipalnamen (Service Principal Names, SPN) dieses Computers registrieren für Active Directory (für die Windows-Authentifizierung erforderlich)** aus.</span><span class="sxs-lookup"><span data-stu-id="53c2f-248">To optionally register a Service Principal Name (SPN) for the Self-Service Portal, select **Register this machine’s Service Principal Names (SPN) with Active Directory (Required for Windows Authentication)**.</span></span> <span data-ttu-id="53c2f-249">Wenn Sie dieses Kontrollkästchen aktivieren, versucht MBAM Setup nicht, die vorhandenen SPNs zu registrieren, und Sie können den SPN vor oder nach der Installation von MBAM manuell registrieren.</span><span class="sxs-lookup"><span data-stu-id="53c2f-249">If you select this check box, MBAM Setup will not try to register the existing SPNs, and you can manually register the SPN before or after the MBAM installation.</span></span> <span data-ttu-id="53c2f-250">Anweisungen zum manuellen Registrieren des SPN finden Sie unter [Manuelle SPN-Registrierung](https://go.microsoft.com/fwlink/?LinkId=286758).</span><span class="sxs-lookup"><span data-stu-id="53c2f-250">For instructions on registering the SPN manually, see [Manual SPN Registration](https://go.microsoft.com/fwlink/?LinkId=286758).</span></span>

13. <span data-ttu-id="53c2f-251">Klicken Sie auf **weiter** , um den Setup-Assistenten für Microsoft BitLocker-Verwaltung und-Überwachung fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-251">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

14. <span data-ttu-id="53c2f-252">Geben Sie an, ob Microsoft Updates dazu beitragen soll, Ihren Computer zu schützen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="53c2f-252">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span>

15. <span data-ttu-id="53c2f-253">Wenn die ausgewählten MBAM-Funktionsinformationen abgeschlossen sind, können Sie die MBAM-Installation mithilfe des Setup-Assistenten starten.</span><span class="sxs-lookup"><span data-stu-id="53c2f-253">When the selected MBAM feature information is completed, you are ready to start the MBAM installation by using the Setup wizard.</span></span> <span data-ttu-id="53c2f-254">Klicken Sie auf **zurück** , um den Assistenten zu durchlaufen, wenn Sie Ihre Installationseinstellungen überprüfen oder ändern müssen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-254">Click **Back** to move through the wizard if you have to review or change your installation settings.</span></span> <span data-ttu-id="53c2f-255">Klicken Sie auf installieren, um die Installation zu **Installieren** .</span><span class="sxs-lookup"><span data-stu-id="53c2f-255">Click **Install** to being the installation.</span></span> <span data-ttu-id="53c2f-256">Klicken Sie auf **Abbrechen** , um den Assistenten zu beenden.</span><span class="sxs-lookup"><span data-stu-id="53c2f-256">Click **Cancel** to exit the wizard.</span></span> <span data-ttu-id="53c2f-257">Setup installiert die von Ihnen ausgewählten MBAM-Features und benachrichtigt Sie, dass die Installation abzuschließen ist.</span><span class="sxs-lookup"><span data-stu-id="53c2f-257">Setup installs the MBAM features that you selected and notifies you that the installation is finished.</span></span>

16. <span data-ttu-id="53c2f-258">Klicken Sie auf **Fertig stellen** , um den Assistenten zu beenden.</span><span class="sxs-lookup"><span data-stu-id="53c2f-258">Click **Finish** to exit the wizard.</span></span>

**<span data-ttu-id="53c2f-259">So führen Sie die Konfiguration nach der Installation durch</span><span class="sxs-lookup"><span data-stu-id="53c2f-259">To perform post-installation configuration</span></span>**

1.  <span data-ttu-id="53c2f-260">Fügen Sie auf dem Verwaltungs-und Überwachungs Server den folgenden lokalen Gruppen Benutzer hinzu, um Ihnen Zugriff auf die Features auf der MBAM-Verwaltungs-und-Überwachungs Website zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="53c2f-260">On the Administration and Monitoring Server, add users to the following local groups to give them access to the features on the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="53c2f-261">**MBAM Helpdesk-Benutzer**: Mitglieder dieser lokalen Gruppe können auf der MBAM-Website für Verwaltung und Überwachung auf die Laufwerk Wiederherstellung zugreifen und TPM-Features verwalten.</span><span class="sxs-lookup"><span data-stu-id="53c2f-261">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="53c2f-262">Alle Felder in Laufwerk Wiederherstellung und TPM verwalten sind für einen Helpdesk-Benutzer Pflichtfelder.</span><span class="sxs-lookup"><span data-stu-id="53c2f-262">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="53c2f-263">**MBAM Advanced Helpdesk-Benutzer**: Mitglieder dieser lokalen Gruppe haben erweiterten Zugriff auf die Drive Recovery-und TPM-Features auf der MBAM-Website für Verwaltung und Überwachung.</span><span class="sxs-lookup"><span data-stu-id="53c2f-263">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="53c2f-264">Für erfahrene Helpdesk-Benutzer ist in Drive Recovery nur das Schlüssel-ID-Feld erforderlich.</span><span class="sxs-lookup"><span data-stu-id="53c2f-264">For Advanced Helpdesk Users, only the Key ID field is required in Drive Recovery.</span></span> <span data-ttu-id="53c2f-265">In **TPM verwalten**sind nur das Feld **Computerdomäne** und das Feld **Computer Name** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="53c2f-265">In **Manage TPM**, only the **Computer Domain** field and **Computer Name** field are required.</span></span>

2.  <span data-ttu-id="53c2f-266">Fügen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungsserver sowie die Compliance-und Überwachungsdatenbank gehostet werden, sowie auf dem Server, auf dem die Konformitäts-und Überwachungsberichte gehostet werden, Benutzer zur folgenden lokalen Gruppe hinzu, um Ihnen Zugriff auf das Feature Berichte auf der MBAM-Verwaltungs-und-Überwachungs Website zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="53c2f-266">On the server that hosts Administration and Monitoring Server and the Compliance and Audit Database and on the server that hosts the Compliance and Audit Reports, add users to the following local group to give them access to the Reports feature on the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="53c2f-267">**MBAM-Berichtsbenutzer**: Mitglieder dieser lokalen Gruppe können auf die Berichte auf der MBAM-Website zugreifen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-267">**MBAM Report Users**: Members of this local group can access the reports on the MBAM Administration and Monitoring website.</span></span>

    **<span data-ttu-id="53c2f-268">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="53c2f-268">Note</span></span>**  
    <span data-ttu-id="53c2f-269">Die identische Benutzer-oder Gruppenmitgliedschaft der lokalen Gruppe **MBAM-Berichtsbenutzer** muss auf allen Computern verwaltet werden, auf denen die MBAM-Verwaltungs-und Überwachungs Server Features, die Kompatibilitäts-und Überwachungsdatenbank sowie die Kompatibilitäts-und Überwachungsberichte installiert sind.</span><span class="sxs-lookup"><span data-stu-id="53c2f-269">Identical user or group membership of the **MBAM Report Users** local group must be maintained on all computers where the MBAM Administration and Monitoring Server features, Compliance and Audit Database, and the Compliance and Audit Reports are installed.</span></span>



## <span data-ttu-id="53c2f-270">Überprüfen der MBAM Server-Feature-Installation</span><span class="sxs-lookup"><span data-stu-id="53c2f-270">Validating the MBAM Server Feature Installation</span></span>


<span data-ttu-id="53c2f-271">Wenn die Installation der Microsoft BitLocker-Verwaltungs-und Monitoring Server-Features abgeschlossen ist, empfehlen wir, dass Sie überprüfen, ob die Installation alle erforderlichen Features für MBAM erfolgreich eingerichtet hat.</span><span class="sxs-lookup"><span data-stu-id="53c2f-271">When Microsoft BitLocker Administration and Monitoring Server feature installation is completed, we recommend that you validate that the installation has successfully set up all the necessary features for MBAM.</span></span> <span data-ttu-id="53c2f-272">Gehen Sie wie folgt vor, um zu überprüfen, ob der Dienst Microsoft BitLocker-Verwaltung und-Überwachung funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="53c2f-272">Use the following procedure to confirm that the Microsoft BitLocker Administration and Monitoring service is functional.</span></span>

**<span data-ttu-id="53c2f-273">So überprüfen Sie eine MBAM-Server Installation</span><span class="sxs-lookup"><span data-stu-id="53c2f-273">To validate an MBAM Server installation</span></span>**

1. <span data-ttu-id="53c2f-274">Öffnen Sie auf jedem Server, auf dem ein MBAM-Feature bereitgestellt wird, die **System**Steuerung, wählen Sie **Programme**und dann **Programme und Funktionen**aus.</span><span class="sxs-lookup"><span data-stu-id="53c2f-274">On each server where an MBAM feature is deployed, open **Control Panel**, select **Programs**, and then select **Programs and Features**.</span></span> <span data-ttu-id="53c2f-275">Überprüfen Sie, ob die **Microsoft BitLocker-Verwaltung und-Überwachung** in der Liste " **Programme und Features** " angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="53c2f-275">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="53c2f-276">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="53c2f-276">Note</span></span>**  
   <span data-ttu-id="53c2f-277">Um die MBAM-Installation zu überprüfen, müssen Sie ein Domänenkonto verwenden, das über lokale Computeradministrator Anmeldeinformationen auf jedem Server verfügt.</span><span class="sxs-lookup"><span data-stu-id="53c2f-277">To validate the MBAM installation, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2. <span data-ttu-id="53c2f-278">Öffnen Sie auf dem Server, auf dem die Wiederherstellungsdatenbank installiert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Wiederherstellungs-und-Hardware** Datenbank installiert ist.</span><span class="sxs-lookup"><span data-stu-id="53c2f-278">On the server where the Recovery Database is installed, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="53c2f-279">Öffnen Sie auf dem Server, auf dem die Compliance-und Überwachungsdatenbank installiert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Konformitäts Status Datenbank** installiert ist.</span><span class="sxs-lookup"><span data-stu-id="53c2f-279">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio and verify that the **MBAM Compliance Status Database** is installed.</span></span>

4. <span data-ttu-id="53c2f-280">Öffnen Sie auf dem Server, auf dem die Konformitäts-und Überwachungsberichte installiert sind, einen Webbrowser mit administrativen Anmeldeinformationen, und navigieren Sie zu "Start" der SQL Server Reporting Services-Website.</span><span class="sxs-lookup"><span data-stu-id="53c2f-280">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative credentials and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="53c2f-281">Der standardmäßige Startspeicherort einer SQL Server Reporting Services-Websiteinstanz befindet sich unter http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.aspx.</span><span class="sxs-lookup"><span data-stu-id="53c2f-281">The default Home location of a SQL Server Reporting Services site instance can be found is at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.aspx.</span></span> <span data-ttu-id="53c2f-282">Um die tatsächliche URL zu finden, verwenden Sie das Reporting Services-Konfigurations-Manager-Tool, und wählen Sie die Instanzen aus, die während der Installation angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="53c2f-282">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances that were specified during setup.</span></span>

   <span data-ttu-id="53c2f-283">Vergewissern Sie sich, dass ein Berichtsordner mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung** eine Datenquelle namens **MaltaDataSource** enthält und dass ein **en-US-** Ordner vier Berichte enthält.</span><span class="sxs-lookup"><span data-stu-id="53c2f-283">Confirm that a reports folder named **Microsoft BitLocker Administration and Monitoring** contains a data source called **MaltaDataSource** and that an **en-us** folder contains four reports.</span></span>

   **<span data-ttu-id="53c2f-284">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="53c2f-284">Note</span></span>**  
   <span data-ttu-id="53c2f-285">Wenn SQL Server Reporting Services als benannte Instanz konfiguriert wurde, sollte die URL wie folgt aussehen: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="53c2f-285">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following:http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. <span data-ttu-id="53c2f-286">Führen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungsfunktion installiert ist, den **Server-Manager** aus, und navigieren Sie zu **Rollen**.</span><span class="sxs-lookup"><span data-stu-id="53c2f-286">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**.</span></span> <span data-ttu-id="53c2f-287">Wählen Sie **Webserver (IIS)** aus, und klicken Sie dann auf **Internet Informationsdienste (IIS)-Manager**.</span><span class="sxs-lookup"><span data-stu-id="53c2f-287">Select **Web Server (IIS)**, and then click **Internet Information Services (IIS) Manager**.</span></span>

6. <span data-ttu-id="53c2f-288">Navigieren Sie in **Verbindungen**zu \* &lt; Computername &gt; \*, wählen Sie **Websites**aus, und wählen Sie **Microsoft BitLocker-Verwaltung und-Überwachung**aus.</span><span class="sxs-lookup"><span data-stu-id="53c2f-288">In **Connections**, browse to *&lt;computername&gt;*, select **Sites**, and select **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="53c2f-289">Überprüfen Sie, ob **MBAMAdministrationService**, **MBAMComplianceStatusService**und **MBAMRecoveryAndHardwareService** aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="53c2f-289">Verify that **MBAMAdministrationService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

7. <span data-ttu-id="53c2f-290">Öffnen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungsfeatures sowie das Self-Service-Portal installiert sind, einen Webbrowser mit administrativen Anmeldeinformationen, und navigieren Sie zu den folgenden Speicherorten, um sicherzustellen, dass Sie erfolgreich geladen werden.</span><span class="sxs-lookup"><span data-stu-id="53c2f-290">On the server where the Administration and Monitoring features and Self-Service Portal are installed, open a web browser with administrative credentials and browse to the following locations to verify that they load successfully.</span></span>

   **<span data-ttu-id="53c2f-291">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="53c2f-291">Note</span></span>**  
   <span data-ttu-id="53c2f-292">Die URLs, die in ". svc" enden, zeigen keine Website an.</span><span class="sxs-lookup"><span data-stu-id="53c2f-292">The URLs ending in “.svc” do not display a website.</span></span> <span data-ttu-id="53c2f-293">Der Erfolg wird durch die Meldung "Metadaten-Veröffentlichung für diesen Dienst ist zurzeit deaktiviert" oder durch Informationen angezeigt, die mit Code vergleichbar sind.</span><span class="sxs-lookup"><span data-stu-id="53c2f-293">Success is indicated by the message “Metadata publishing for this service is currently disabled” or by information resembling code.</span></span> <span data-ttu-id="53c2f-294">Wenn eine andere Fehlermeldung angezeigt wird oder die Seite nicht gefunden wird, wurde die Seite nicht erfolgreich geladen.</span><span class="sxs-lookup"><span data-stu-id="53c2f-294">If you see some other error message or if the page cannot be found, the page has not loaded successfully.</span></span>



~~~
-   *http://&lt;hostname&gt;/HelpDesk/default.aspx* and confirm each of the links for navigation and reports

-   *http://&lt;hostname&gt;/SelfService&gt;/*

-   *http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc*

-   *http://&lt;hostname&gt;/MBAMUserSupportService/UserSupportService.svc*

-   *http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc*

-   *http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc*

**Note**  
It is assumed that the server features were installed on the default port without network encryption. If you installed the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example, *http://&lt;hostname&gt;:&lt;port&gt;/HelpDesk/default.aspx* or*http://&lt;hostname&gt;:&lt;port&gt;/&lt;virtualdirectory&gt;/default.aspx*

If the server features were installed with network encryption, change http:// to https://.
~~~



8. <span data-ttu-id="53c2f-295">Überprüfen Sie, ob jede Webseite erfolgreich geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="53c2f-295">Verify that each webpage loads successfully.</span></span>

## <span data-ttu-id="53c2f-296">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="53c2f-296">Related topics</span></span>


[<span data-ttu-id="53c2f-297">Bereitstellen der Serverinfrastruktur von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="53c2f-297">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









