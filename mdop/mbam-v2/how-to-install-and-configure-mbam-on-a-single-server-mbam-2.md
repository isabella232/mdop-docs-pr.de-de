---
title: So installieren und Konfigurieren von MBAM auf einem Server
description: So installieren und Konfigurieren von MBAM auf einem Server
author: dansimp
ms.assetid: 45e6a012-6c8c-4d90-902c-d09de9a0cbea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 53e170f421bdce8dd6f771af3902af627a15a085
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810333"
---
# <span data-ttu-id="db6be-103">So installieren und Konfigurieren von MBAM auf einem Server</span><span class="sxs-lookup"><span data-stu-id="db6be-103">How to Install and Configure MBAM on a Single Server</span></span>


<span data-ttu-id="db6be-104">In den Verfahren in diesem Thema wird beschrieben, wie Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) in der eigenständigen Topologie auf einem einzelnen Server installieren.</span><span class="sxs-lookup"><span data-stu-id="db6be-104">The procedures in this topic describe how to install Microsoft BitLocker Administration and Monitoring (MBAM) in the Stand-alone topology on a single server.</span></span> <span data-ttu-id="db6be-105">Verwenden Sie die Konfiguration mit einem Server nur in einer Testumgebung.</span><span class="sxs-lookup"><span data-stu-id="db6be-105">Use the single-server configuration only in a test environment.</span></span> <span data-ttu-id="db6be-106">Verwenden Sie für Produktionsumgebungen zwei oder mehr Server.</span><span class="sxs-lookup"><span data-stu-id="db6be-106">For production environments, use two or more servers.</span></span> <span data-ttu-id="db6be-107">Wenn Sie die Microsoft BitLocker-Verwaltung und-Überwachung mithilfe der Configuration Manager-Topologie installieren, lesen Sie [Bereitstellen von MBAM mit Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span><span class="sxs-lookup"><span data-stu-id="db6be-107">If you are installing Microsoft BitLocker Administration and Monitoring by using the Configuration Manager topology, see [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span></span>

<span data-ttu-id="db6be-108">Das folgende Diagramm zeigt ein Beispiel für eine Architektur mit einem einzelnen Server.</span><span class="sxs-lookup"><span data-stu-id="db6be-108">The following diagram shows an example of a single-server architecture.</span></span> <span data-ttu-id="db6be-109">Eine Beschreibung der Datenbanken und Features finden Sie unter [Architektur auf höherer Ebene für MBAM 2,0](high-level-architecture-for-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="db6be-109">For a description of the databases and features, see [High-Level Architecture for MBAM 2.0](high-level-architecture-for-mbam-20-mbam-2.md).</span></span>

![mbam 2 Einzelserver-Bereitstellungstopologie](images/mbam2-1-server.gif)

<span data-ttu-id="db6be-111">Jedes Server Feature hat bestimmte Voraussetzungen.</span><span class="sxs-lookup"><span data-stu-id="db6be-111">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="db6be-112">Wenn Sie sicherstellen möchten, dass Sie die Voraussetzungen und Hardware-und Softwareanforderungen erfüllt haben, lesen Sie [MBAM 2,0-Bereitstellungsvoraussetzungen](mbam-20-deployment-prerequisites-mbam-2.md) und [MBAM 2,0-unterstützte Konfigurationen](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="db6be-112">To verify that you have met the prerequisites and hardware and software requirements, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) and [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span> <span data-ttu-id="db6be-113">Darüber hinaus verfügen einige Features auch über Informationen, die während des Installationsvorgangs bereitgestellt werden müssen, um das Feature erfolgreich bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="db6be-113">In addition, some features also have information that must be provided during the installation process to successfully deploy the feature.</span></span> <span data-ttu-id="db6be-114">Sie sollten auch überprüfen, [wie Sie Ihre Umgebung für MBAM 2,0 vorbereiten](preparing-your-environment-for-mbam-20-mbam-2.md) , bevor Sie mit der MBAM-Bereitstellung beginnen.</span><span class="sxs-lookup"><span data-stu-id="db6be-114">You should also review [Preparing your Environment for MBAM 2.0](preparing-your-environment-for-mbam-20-mbam-2.md) before you start MBAM deployment.</span></span>

**<span data-ttu-id="db6be-115">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="db6be-115">Note</span></span>**  
<span data-ttu-id="db6be-116">Um die Setupprotokolldateien zu erhalten, verwenden Sie das msiexec-Paket und die Option **/l** &lt; Location &gt; , um MBAM zu installieren.</span><span class="sxs-lookup"><span data-stu-id="db6be-116">To obtain the setup log files, you have use the Msiexec package and the **/L** &lt;location&gt; option to install MBAM.</span></span> <span data-ttu-id="db6be-117">Protokolldateien werden an dem von Ihnen angegebenen Speicherort erstellt.</span><span class="sxs-lookup"><span data-stu-id="db6be-117">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="db6be-118">Zusätzliche Setupprotokolldateien werden im Ordner% Temp% auf dem Server des Benutzers erstellt, der MBAM installiert.</span><span class="sxs-lookup"><span data-stu-id="db6be-118">Additional setup log files are created in the %temp% folder on the server of the user who is installing MBAM.</span></span>



## <span data-ttu-id="db6be-119">So installieren Sie die MBAM-Server Features auf einem einzelnen Server</span><span class="sxs-lookup"><span data-stu-id="db6be-119">To install MBAM Server features on a single server</span></span>


<span data-ttu-id="db6be-120">In den folgenden Schritten wird beschrieben, wie allgemeine MBAM-Features installiert werden.</span><span class="sxs-lookup"><span data-stu-id="db6be-120">The following steps describe how to install general MBAM features.</span></span>

**<span data-ttu-id="db6be-121">So starten Sie die Installation von MBAM Server Features</span><span class="sxs-lookup"><span data-stu-id="db6be-121">To start the MBAM Server features installation</span></span>**

1.  <span data-ttu-id="db6be-122">Führen Sie auf dem Server, auf dem Sie MBAM installieren möchten, **MBAMSetup.exe** aus, um den MBAM-Installations-Assistenten zu starten.</span><span class="sxs-lookup"><span data-stu-id="db6be-122">On the server where you want to install MBAM, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="db6be-123">Wählen Sie auf der **Willkommens** Seite optional das **Programm zur Verbesserung der Benutzerfreundlichkeit**aus, und klicken Sie dann auf **Start**.</span><span class="sxs-lookup"><span data-stu-id="db6be-123">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="db6be-124">Lesen und akzeptieren Sie den Microsoft-Software-Lizenzvertrag, und klicken Sie auf **weiter** , um die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="db6be-124">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="db6be-125">Wählen Sie auf der Seite **Topologie Auswahl** die **eigenständige** Topologie aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="db6be-125">On the **Topology Selection** page, select the **Stand-alone** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="db6be-126">Wählen Sie auf der Seite **zu installierende Features auswählen** die Features aus, die Sie installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="db6be-126">On the **Select features to install** page, select the features that you want to install.</span></span> <span data-ttu-id="db6be-127">Standardmäßig sind alle MBAM-Features für die Installation ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="db6be-127">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="db6be-128">Features, die auf demselben Computer installiert werden sollen, müssen zur gleichen Zeit zusammen installiert werden.</span><span class="sxs-lookup"><span data-stu-id="db6be-128">Features that are to be installed on the same computer must be installed together at the same time.</span></span> <span data-ttu-id="db6be-129">Deaktivieren Sie die Kontrollkästchen für alle Features, die Sie an anderer Stelle installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="db6be-129">Clear the check boxes for any features that you want to install elsewhere.</span></span> <span data-ttu-id="db6be-130">Sie müssen die MBAM-Features in der folgenden Reihenfolge installieren:</span><span class="sxs-lookup"><span data-stu-id="db6be-130">You must install MBAM features in the following order:</span></span>

    -   <span data-ttu-id="db6be-131">Wiederherstellungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="db6be-131">Recovery Database</span></span>

    -   <span data-ttu-id="db6be-132">Konformitäts-und Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="db6be-132">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="db6be-133">Konformitäts-und Überwachungsberichte</span><span class="sxs-lookup"><span data-stu-id="db6be-133">Compliance and Audit Reports</span></span>

    -   <span data-ttu-id="db6be-134">Self-Service-Server</span><span class="sxs-lookup"><span data-stu-id="db6be-134">Self-Service Server</span></span>

    -   <span data-ttu-id="db6be-135">Verwaltungs-und Überwachungs Server</span><span class="sxs-lookup"><span data-stu-id="db6be-135">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="db6be-136">MBAM-Gruppenrichtlinienvorlage</span><span class="sxs-lookup"><span data-stu-id="db6be-136">MBAM Group Policy template</span></span>

    **<span data-ttu-id="db6be-137">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="db6be-137">Note</span></span>**  
    <span data-ttu-id="db6be-138">Der Installations-Assistent überprüft die Voraussetzungen für die Installation und zeigt die fehlenden Voraussetzungen an.</span><span class="sxs-lookup"><span data-stu-id="db6be-138">The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="db6be-139">Wenn alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="db6be-139">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="db6be-140">Wenn eine fehlende Voraussetzung erkannt wird, müssen Sie die fehlenden Voraussetzungen beheben und dann **erneut auf Voraussetzungen prüfen**klicken.</span><span class="sxs-lookup"><span data-stu-id="db6be-140">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="db6be-141">Wenn dieses Mal alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="db6be-141">If all prerequisites are met this time, the installation resumes.</span></span>



6.  <span data-ttu-id="db6be-142">Wählen Sie auf der Seite **Netzwerk Kommunikationssicherheit konfigurieren** aus, ob die Kommunikation zwischen den Webdiensten auf dem Administrations-und Überwachungs Server und den Clients verschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="db6be-142">On the **Configure network communication security** page, choose whether to encrypt the communication between the Web Services on the Administration and Monitoring Server and the clients.</span></span> <span data-ttu-id="db6be-143">Wenn Sie sich entschließen, die Kommunikation zu verschlüsseln, wählen Sie das für die Verschlüsselung zu verwendende Zertifizierungsstellenzertifikat aus.</span><span class="sxs-lookup"><span data-stu-id="db6be-143">If you decide to encrypt the communication, select the certification authority-provisioned certificate to use for encryption.</span></span> <span data-ttu-id="db6be-144">Das Zertifikat muss vor diesem Schritt erstellt werden, damit Sie es auf dieser Seite auswählen können.</span><span class="sxs-lookup"><span data-stu-id="db6be-144">The certificate must be created prior to this step to enable you to select it on this page.</span></span>

    **<span data-ttu-id="db6be-145">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="db6be-145">Note</span></span>**  
    <span data-ttu-id="db6be-146">Diese Seite wird nur angezeigt, wenn Sie auf der Seite **zu installierende Features auswählen** das Self-Service-Portal oder die Verwaltungs-und Überwachungs Server Funktion ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="db6be-146">This page appears only if you selected the Self-Service Portal or the Administration and Monitoring Server feature on the **Select features to install** page.</span></span>



7.  <span data-ttu-id="db6be-147">Klicken Sie auf **weiter**, und fahren Sie mit den nächsten Schritten fort, um die MBAM-Server Features zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="db6be-147">Click **Next**, and then continue to the next set of steps to configure the MBAM Server features.</span></span>

**<span data-ttu-id="db6be-148">So konfigurieren Sie die MBAM-Server Features</span><span class="sxs-lookup"><span data-stu-id="db6be-148">To configure the MBAM Server features</span></span>**

1.  <span data-ttu-id="db6be-149">Geben Sie auf der Seite " **Wiederherstellungsdatenbank konfigurieren** " den Namen der SQL Server-Instanz und den Namen der Datenbank an, in der die Wiederherstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="db6be-149">On the **Configure the Recovery database** page, specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="db6be-150">Sie müssen außerdem angeben, wo die Datenbankdateien gespeichert werden sollen und wo sich die Protokollinformationen befinden sollen.</span><span class="sxs-lookup"><span data-stu-id="db6be-150">You must also specify both where the database files will be located and where the log information will be located.</span></span>

2.  <span data-ttu-id="db6be-151">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="db6be-151">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="db6be-152">Geben Sie auf der Seite **Compliance-und Überwachungsdatenbank konfigurieren** den Namen der SQL Server-Instanz und den Namen der Datenbank an, in der die Konformitäts-und Überwachungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="db6be-152">On the **Configure the Compliance and Audit database** page, specify the SQL Server instance name and the name of the database that will store the compliance and audit data.</span></span> <span data-ttu-id="db6be-153">Sie müssen außerdem angeben, wo die Datenbankdateien gespeichert werden sollen und wo sich die Protokollinformationen befinden sollen.</span><span class="sxs-lookup"><span data-stu-id="db6be-153">You must also specify where the database files will be located and where the log information will be located.</span></span>

4.  <span data-ttu-id="db6be-154">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="db6be-154">Click **Next** to continue.</span></span>

5.  <span data-ttu-id="db6be-155">Geben Sie auf der Seite **Compliance-und Überwachungsberichte konfigurieren** die SQL Server Reporting Services-Instanz an, in der die Kompatibilitäts-und Überwachungsberichte installiert werden, und geben Sie ein Domänenbenutzerkonto und ein Kennwort für den Zugriff auf die Datenbank Compliance und Audit an.</span><span class="sxs-lookup"><span data-stu-id="db6be-155">On the **Configure the Compliance and Audit Reports** page, specify the SQL Server Reporting Services instance where the Compliance and Audit reports will be installed, and provide a domain user account and password for accessing the Compliance and Audit database.</span></span> <span data-ttu-id="db6be-156">Konfigurieren Sie das Kennwort für dieses Konto so, dass es nie abläuft.</span><span class="sxs-lookup"><span data-stu-id="db6be-156">Configure the password for this account to never expire.</span></span> <span data-ttu-id="db6be-157">Das Benutzerkonto sollte in der Lage sein, auf alle Daten zuzugreifen, die der Gruppe MBAM-Berichte Benutzer zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="db6be-157">The user account should be able to access all data available to the MBAM Reports Users group.</span></span>

6.  <span data-ttu-id="db6be-158">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="db6be-158">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="db6be-159">Geben Sie auf der Seite **Self-Service-Portal konfigurieren** die Portnummer, den Hostnamen, den Namen des virtuellen Verzeichnisses und den Installationspfad für das Self-Service-Portal ein.</span><span class="sxs-lookup"><span data-stu-id="db6be-159">On the **Configure the Self-Service Portal** page, enter the port number, host name, virtual directory name, and installation path for the Self-Service Portal.</span></span>

    **<span data-ttu-id="db6be-160">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="db6be-160">Note</span></span>**  
    <span data-ttu-id="db6be-161">Die von Ihnen angegebene Portnummer muss eine nicht verwendete Portnummer auf dem Verwaltungs-und Überwachungs Server sein, sofern Sie keinen eindeutigen Hostheadernamen angeben.</span><span class="sxs-lookup"><span data-stu-id="db6be-161">The port number that you specify must be an unused port number on the Administration and Monitoring Server unless you specify a unique host header name.</span></span> <span data-ttu-id="db6be-162">Wenn Sie die Windows-Firewall verwenden, wird der Port automatisch geöffnet.</span><span class="sxs-lookup"><span data-stu-id="db6be-162">If you are using Windows Firewall, the port will be opened automatically.</span></span>



8.  <span data-ttu-id="db6be-163">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="db6be-163">Click **Next** to continue.</span></span>

9.  <span data-ttu-id="db6be-164">Geben Sie an, ob Microsoft Updates dazu beitragen soll, Ihren Computer zu schützen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="db6be-164">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="db6be-165">Damit werden die automatischen Updates in Windows nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="db6be-165">This does not turn on Automatic Updates in Windows.</span></span>

10. <span data-ttu-id="db6be-166">Geben Sie auf der Seite **Verwaltungs-und Überwachungs Server konfigurieren** die Portnummer, den Hostnamen, den Namen des virtuellen Verzeichnisses und den Installationspfad für die Helpdesk-Website ein.</span><span class="sxs-lookup"><span data-stu-id="db6be-166">On the **Configure the Administration and Monitoring Server** page, enter the port number, host name, virtual directory name, and installation path for the Help Desk website.</span></span>

    **<span data-ttu-id="db6be-167">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="db6be-167">Note</span></span>**  
    <span data-ttu-id="db6be-168">Die von Ihnen angegebene Portnummer muss eine nicht verwendete Portnummer auf dem Verwaltungs-und Überwachungs Server sein, sofern Sie keinen eindeutigen Hostheadernamen angeben.</span><span class="sxs-lookup"><span data-stu-id="db6be-168">The port number that you specify must be an unused port number on the Administration and Monitoring Server unless you specify a unique host header name.</span></span> <span data-ttu-id="db6be-169">Wenn Sie die Windows-Firewall verwenden, wird der Port automatisch geöffnet.</span><span class="sxs-lookup"><span data-stu-id="db6be-169">If you are using Windows Firewall, the port will be opened automatically.</span></span>



11. <span data-ttu-id="db6be-170">Überprüfen Sie auf der Seite **Installationszusammenfassung** die Liste der Features, die installiert werden sollen, und klicken Sie auf **Installieren** , um mit der Installation der MBAM-Features zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="db6be-170">On the **Installation Summary** page, review the list of features that will be installed, and click **Install** to start installing the MBAM features.</span></span> <span data-ttu-id="db6be-171">Klicken Sie auf **zurück** , um durch den Assistenten zurückzukehren, wenn Sie die Installationseinstellungen überprüfen oder ändern müssen, oder klicken Sie auf **Abbrechen** , um Setup zu beenden.</span><span class="sxs-lookup"><span data-stu-id="db6be-171">Click **Back** to move back through the wizard if you have to review or change your installation settings, or click **Cancel** to exit Setup.</span></span> <span data-ttu-id="db6be-172">Setup installiert die MBAM-Features und benachrichtigt Sie, dass die Installation abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="db6be-172">Setup installs the MBAM features and notifies you that the installation is complete.</span></span>

12. <span data-ttu-id="db6be-173">Klicken Sie auf **Fertig stellen** , um den Assistenten zu beenden.</span><span class="sxs-lookup"><span data-stu-id="db6be-173">Click **Finish** to exit the wizard.</span></span> <span data-ttu-id="db6be-174">Nachdem die Microsoft BitLocker-Verwaltungs-und Überwachungs Server Features installiert wurden, fahren Sie mit dem nächsten Abschnitt fort, und führen Sie die Schritte zum Hinzufügen von Benutzern zu den Microsoft BitLocker-Verwaltungs-und Überwachungs Rollen aus.</span><span class="sxs-lookup"><span data-stu-id="db6be-174">After the Microsoft BitLocker Administration and Monitoring Server features have been installed, continue to the next section and complete the steps have to add users to the Microsoft BitLocker Administration and Monitoring roles.</span></span> <span data-ttu-id="db6be-175">Weitere Informationen zu Rollen finden Sie unter [Planen von MBAM 2,0-Administrator Rollen](planning-for-mbam-20-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="db6be-175">For more information about roles, see [Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md).</span></span>

**<span data-ttu-id="db6be-176">So führen Sie die Konfiguration nach der Installation durch</span><span class="sxs-lookup"><span data-stu-id="db6be-176">To perform post-installation configuration</span></span>**

1.  <span data-ttu-id="db6be-177">Fügen Sie auf dem Verwaltungs-und Überwachungs Server den folgenden lokalen Gruppen Benutzer hinzu, um Ihnen Zugriff auf die Features der MBAM Help Desk-Website zu gewähren:</span><span class="sxs-lookup"><span data-stu-id="db6be-177">On the Administration and Monitoring Server, add users to the following local groups to give them access to the MBAM Help Desk website features:</span></span>

    -   <span data-ttu-id="db6be-178">**MBAM Helpdesk-Benutzer**: Mitglieder dieser lokalen Gruppe können auf der MBAM-Website für Verwaltung und Überwachung auf die Laufwerk Wiederherstellung zugreifen und TPM-Features verwalten.</span><span class="sxs-lookup"><span data-stu-id="db6be-178">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="db6be-179">Alle Felder in Laufwerk Wiederherstellung und TPM verwalten sind für einen Helpdesk-Benutzer Pflichtfelder.</span><span class="sxs-lookup"><span data-stu-id="db6be-179">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="db6be-180">**MBAM Advanced Helpdesk-Benutzer**: Mitglieder dieser lokalen Gruppe haben erweiterten Zugriff auf die Drive Recovery-und TPM-Features auf der MBAM-Website für Verwaltung und Überwachung.</span><span class="sxs-lookup"><span data-stu-id="db6be-180">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="db6be-181">Für erfahrene Helpdesk-Benutzer ist in Drive Recovery nur das **Schlüssel-ID-** Feld erforderlich.</span><span class="sxs-lookup"><span data-stu-id="db6be-181">For Advanced Helpdesk Users, only the **Key ID** field is required in Drive Recovery.</span></span> <span data-ttu-id="db6be-182">In TPM verwalten sind nur das Feld **Computerdomäne** und das Feld **Computer Name** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="db6be-182">In Manage TPM, only the **Computer Domain** field and **Computer Name** field are required.</span></span>

2.  <span data-ttu-id="db6be-183">Fügen Sie auf dem Verwaltungs-und Überwachungs Server der folgenden lokalen Gruppe Benutzer hinzu, damit Sie auf der MBAM-Websiteverwaltung und Überwachung auf das Feature Berichte zugreifen können:</span><span class="sxs-lookup"><span data-stu-id="db6be-183">On the Administration and Monitoring Server, add users to the following local group to enable them to access the Reports feature on the MBAM Administration and Monitoring website:</span></span>

    -   <span data-ttu-id="db6be-184">**MBAM-Berichtsbenutzer**: Mitglieder dieser lokalen Gruppe können auf die Berichtsfeatures auf der MBAM-Website für Verwaltung und Überwachung zugreifen.</span><span class="sxs-lookup"><span data-stu-id="db6be-184">**MBAM Report Users**: Members of this local group can access the Reports features on the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="db6be-185">Branding des Self-Service-Portals mit dem Namen Ihres Unternehmens, dem Hinweistext und anderen unternehmensspezifischen Informationen</span><span class="sxs-lookup"><span data-stu-id="db6be-185">Brand the Self-Service Portal with your company name, notice text, and other company-specific information.</span></span> <span data-ttu-id="db6be-186">Anweisungen hierzu finden Sie unter so wird es [gemacht: Branding des Self-Service-Portals](how-to-brand-the-self-service-portal.md).</span><span class="sxs-lookup"><span data-stu-id="db6be-186">For instructions, see [How to Brand the Self-Service Portal](how-to-brand-the-self-service-portal.md).</span></span>

    **<span data-ttu-id="db6be-187">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="db6be-187">Note</span></span>**  
    <span data-ttu-id="db6be-188">Die identische Benutzer-oder Gruppenmitgliedschaft der lokalen Gruppe " **MBAM-Berichtsbenutzer** " muss auf allen Computern verwaltet werden, auf denen die MBAM-Verwaltungs-und Überwachungs Server Features, die Kompatibilitäts-und Überwachungsdatenbank sowie Compliance-und Überwachungsberichte installiert sind.</span><span class="sxs-lookup"><span data-stu-id="db6be-188">Identical user or group membership of the **MBAM Report Users** local group must be maintained on all computers where the MBAM Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports are installed.</span></span> <span data-ttu-id="db6be-189">Die empfohlene Vorgehensweise besteht darin, eine Domänensicherheitsgruppe zu erstellen und diese Domänengruppe jeder lokalen MBAM-Berichtsbenutzer Gruppe hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="db6be-189">The recommended way to do this is to create a domain security group and add that domain group to each local MBAM Report Users group.</span></span> <span data-ttu-id="db6be-190">Wenn Sie diesen Prozess verwenden, können Sie die Gruppenmitgliedschaften über die Domänengruppe verwalten.</span><span class="sxs-lookup"><span data-stu-id="db6be-190">When you use this process, manage the group memberships by way of the domain group.</span></span>



## <span data-ttu-id="db6be-191">Überprüfen der MBAM Server-Feature-Installation</span><span class="sxs-lookup"><span data-stu-id="db6be-191">Validating the MBAM Server feature installation</span></span>


<span data-ttu-id="db6be-192">Wenn die Microsoft BitLocker-Administrator-und-überwachungsinstallation abgeschlossen ist, überprüfen Sie, ob die Installation alle erforderlichen MBAM-Features erfolgreich eingerichtet hat, die für die BitLocker-Verwaltung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="db6be-192">When the Microsoft BitLocker Administration and Monitoring installation is completed, validate that the installation has successfully set up all the necessary MBAM features that are required for BitLocker management.</span></span> <span data-ttu-id="db6be-193">Gehen Sie wie folgt vor, um zu überprüfen, ob der MBAM-Dienst funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="db6be-193">Use the following procedure to confirm that the MBAM service is functional.</span></span>

**<span data-ttu-id="db6be-194">So überprüfen Sie die Installation von MBAM Server Features</span><span class="sxs-lookup"><span data-stu-id="db6be-194">To validate the MBAM Server feature installation</span></span>**

1. <span data-ttu-id="db6be-195">Öffnen Sie auf jedem Server, auf dem ein MBAM-Feature bereitgestellt wird, die **System**Steuerung.</span><span class="sxs-lookup"><span data-stu-id="db6be-195">On each server where a MBAM feature is deployed, open **Control Panel**.</span></span> <span data-ttu-id="db6be-196">Wählen Sie **Programme**und dann **Programme und Funktionen**aus.</span><span class="sxs-lookup"><span data-stu-id="db6be-196">Select **Programs**, and then select **Programs and Features**.</span></span> <span data-ttu-id="db6be-197">Überprüfen Sie, ob die **Microsoft BitLocker-Verwaltung und-Überwachung** in der Liste " **Programme und Features** " angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="db6be-197">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="db6be-198">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="db6be-198">Note</span></span>**  
   <span data-ttu-id="db6be-199">Um die Installation zu überprüfen, müssen Sie ein Domänenkonto verwenden, das über lokale Computeradministrator Anmeldeinformationen auf jedem Server verfügt.</span><span class="sxs-lookup"><span data-stu-id="db6be-199">To validate the installation, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2. <span data-ttu-id="db6be-200">Öffnen Sie auf dem Server, auf dem die Wiederherstellungsdatenbank installiert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Wiederherstellungs-und-Hardware** Datenbank installiert ist.</span><span class="sxs-lookup"><span data-stu-id="db6be-200">On the server where the Recovery Database is installed, open SQL Server Management Studio, and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="db6be-201">Öffnen Sie auf dem Server, auf dem die Compliance-und Überwachungsdatenbank installiert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Konformitäts Status Datenbank** installiert ist.</span><span class="sxs-lookup"><span data-stu-id="db6be-201">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio, and verify that the **MBAM Compliance Status Database** is installed.</span></span>

4. <span data-ttu-id="db6be-202">Öffnen Sie auf dem Server, auf dem die Konformitäts-und Überwachungsberichte installiert sind, einen Webbrowser mit administrativen Anmeldeinformationen, und navigieren Sie zu "Start" der SQL Server Reporting Services-Website.</span><span class="sxs-lookup"><span data-stu-id="db6be-202">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative credentials and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="db6be-203">Der standardmäßige Startspeicherort einer SQL Server Reporting Services-Websiteinstanz befindet sich unter http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.</span><span class="sxs-lookup"><span data-stu-id="db6be-203">The default Home location of a SQL Server Reporting Services site instance is at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.</span></span> <span data-ttu-id="db6be-204">Um die tatsächliche URL zu finden, verwenden Sie das Reporting Services-Konfigurations-Manager-Tool, und wählen Sie die Instanzen aus, die während der Installation angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="db6be-204">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances that are specified during setup.</span></span>

   <span data-ttu-id="db6be-205">Vergewissern Sie sich, dass ein Berichtsordner mit dem Namen Microsoft BitLocker-Verwaltung und-Überwachung eine Datenquelle namens **MaltaDataSource** enthält und dass ein **en-US-** Ordner vier Berichte enthält.</span><span class="sxs-lookup"><span data-stu-id="db6be-205">Confirm that a Reports folder named Microsoft BitLocker Administration and Monitoring contains a data source called **MaltaDataSource** and that an **en-us** folder contains four reports.</span></span>

   **<span data-ttu-id="db6be-206">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="db6be-206">Note</span></span>**  
   <span data-ttu-id="db6be-207">Wenn SQL Server Reporting Services als benannte Instanz konfiguriert wurde, sollte die URL wie folgt aussehen: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="db6be-207">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following: http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. <span data-ttu-id="db6be-208">Führen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungsfunktion installiert ist, den **Server-Manager** aus, und navigieren Sie zu **Rollen**.</span><span class="sxs-lookup"><span data-stu-id="db6be-208">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**.</span></span> <span data-ttu-id="db6be-209">Wählen Sie **Webserver (IIS)** aus, und klicken Sie dann auf **Internet Informationsdienste (IIS)-Manager.**</span><span class="sxs-lookup"><span data-stu-id="db6be-209">Select **Web Server (IIS)**, and then click **Internet Information Services (IIS) Manager.**</span></span>

6. <span data-ttu-id="db6be-210">Navigieren Sie in **Verbindungen** zu \* &lt; Computername &gt; \*, wählen Sie **Websites**aus, und wählen Sie dann **Microsoft BitLocker-Verwaltung und-Überwachung**aus.</span><span class="sxs-lookup"><span data-stu-id="db6be-210">In **Connections,** browse to *&lt;computername&gt;*, select **Sites**, and then select **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="db6be-211">Überprüfen Sie, ob **MBAMAdministrationService**, **MBAMUserSupportService**, **MBAMComplianceStatusService**und **MBAMRecoveryAndHardwareService** aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="db6be-211">Verify that **MBAMAdministrationService**, **MBAMUserSupportService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

7. <span data-ttu-id="db6be-212">Öffnen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungsfeatures sowie das Self-Service-Portal installiert sind, einen Webbrowser mit administrativen Anmeldeinformationen, und navigieren Sie zu den folgenden Speicherorten, um sicherzustellen, dass Sie erfolgreich geladen werden:</span><span class="sxs-lookup"><span data-stu-id="db6be-212">On the server where the Administration and Monitoring features and Self-Service Portal are installed, open a web browser with administrative credentials and browse to the following locations to verify that they load successfully:</span></span>

   -   <span data-ttu-id="db6be-213">*http:// &lt; Hostname &gt; /Helpdesk/default.aspx* , und bestätigen Sie die einzelnen Links für Navigation und Berichte.</span><span class="sxs-lookup"><span data-stu-id="db6be-213">*http://&lt;hostname&gt;/HelpDesk/default.aspx* and confirm each of the links for navigation and reports</span></span>

   -   *<span data-ttu-id="db6be-214">http:// &lt; Hostname &gt; /Selfservice&gt;/</span><span class="sxs-lookup"><span data-stu-id="db6be-214">http://&lt;hostname&gt;/SelfService&gt;/</span></span>*

   -   *<span data-ttu-id="db6be-215">http:// &lt; Computername &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="db6be-215">http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>*

   -   *<span data-ttu-id="db6be-216">http:// &lt; Hostname &gt; /MBAMUserSupportService/UserSupportService.svc</span><span class="sxs-lookup"><span data-stu-id="db6be-216">http://&lt;hostname&gt;/MBAMUserSupportService/UserSupportService.svc</span></span>*

   -   *<span data-ttu-id="db6be-217">http:// &lt; Computername &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="db6be-217">http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>*

   -   *<span data-ttu-id="db6be-218">http:// &lt; Computername &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="db6be-218">http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>*

   **<span data-ttu-id="db6be-219">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="db6be-219">Note</span></span>**  
   <span data-ttu-id="db6be-220">Es wird davon ausgegangen, dass die Server Features auf dem Standardport ohne Netzwerk Verschlüsselung installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="db6be-220">It is assumed that the server features were installed on the default port without network encryption.</span></span> <span data-ttu-id="db6be-221">Wenn Sie die Server Features in einem anderen Port oder virtuellen Verzeichnis installiert haben, ändern Sie die URLs so, dass Sie den entsprechenden Port aufweisen, beispielsweise *http:// &lt; Hostname &gt; : &lt; Port &gt; /Helpdesk/default.ASP*x oder*http:// &lt; Hostname &gt; : &lt; Port &gt; / &lt; VirtualDirectory &gt; /default.aspx*</span><span class="sxs-lookup"><span data-stu-id="db6be-221">If you installed the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example, *http://&lt;hostname&gt;:&lt;port&gt;/HelpDesk/default.asp*x or*http://&lt;hostname&gt;:&lt;port&gt;/&lt;virtualdirectory&gt;/default.aspx*</span></span>

   <span data-ttu-id="db6be-222">Wenn die Server Features mit Netzwerk Verschlüsselung installiert wurden, ändern Sie http://in https://.</span><span class="sxs-lookup"><span data-stu-id="db6be-222">If the server features were installed with network encryption, change http:// to https://.</span></span>



## <span data-ttu-id="db6be-223">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="db6be-223">Related topics</span></span>


[<span data-ttu-id="db6be-224">Bereitstellen der Serverinfrastruktur von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="db6be-224">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









