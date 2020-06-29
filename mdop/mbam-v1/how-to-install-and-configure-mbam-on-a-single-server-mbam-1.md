---
title: So installieren und Konfigurieren von MBAM auf einem Server
description: So installieren und Konfigurieren von MBAM auf einem Server
author: dansimp
ms.assetid: 55841c63-bad9-44e7-b7fd-ea7037febbd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 225f66493ceafce5461df3fcc6f701e9a2922a5f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810351"
---
# <span data-ttu-id="547a4-103">So installieren und Konfigurieren von MBAM auf einem Server</span><span class="sxs-lookup"><span data-stu-id="547a4-103">How to Install and Configure MBAM on a Single Server</span></span>


<span data-ttu-id="547a4-104">Die Verfahren in diesem Thema beschreiben die vollständige Installation der Features Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) auf einem einzelnen Server.</span><span class="sxs-lookup"><span data-stu-id="547a4-104">The procedures in this topic describe the full installation of the Microsoft BitLocker Administration and Monitoring (MBAM) features on a single server.</span></span>

<span data-ttu-id="547a4-105">Jedes Server Feature hat bestimmte Voraussetzungen.</span><span class="sxs-lookup"><span data-stu-id="547a4-105">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="547a4-106">Wenn Sie überprüfen möchten, ob Sie die Voraussetzungen und die Hardware-und Softwareanforderungen erfüllt haben, lesen Sie [MBAM 1,0-Bereitstellungsvoraussetzungen](mbam-10-deployment-prerequisites.md) und [MBAM 1,0-unterstützte Konfigurationen](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="547a4-106">To verify that you have met the prerequisites and the hardware and software requirements, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span> <span data-ttu-id="547a4-107">Darüber hinaus verfügen einige Features auch über Informationen, die während des Installationsvorgangs bereitgestellt werden müssen, um das Feature erfolgreich bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="547a4-107">In addition, some features also have information that must be provided during the installation process to successfully deploy the feature.</span></span> <span data-ttu-id="547a4-108">Sie sollten auch überprüfen, [wie Sie Ihre Umgebung für MBAM 1,0 vorbereiten](preparing-your-environment-for-mbam-10.md) , bevor Sie mit der MBAM-Bereitstellung beginnen.</span><span class="sxs-lookup"><span data-stu-id="547a4-108">You should also review [Preparing your Environment for MBAM 1.0](preparing-your-environment-for-mbam-10.md) before you begin the MBAM deployment.</span></span>

<span data-ttu-id="547a4-109">**Hinweis**  Um die Setupprotokolldateien zu erhalten, müssen Sie MBAM mit dem **msiexec** -Paket und der Option " **/l** &lt; Location &gt; " installieren.</span><span class="sxs-lookup"><span data-stu-id="547a4-109">**Note** To obtain the setup log files, you must install MBAM by using the **msiexec** package and the **/l** &lt;location&gt; option.</span></span> <span data-ttu-id="547a4-110">Protokolldateien werden an dem von Ihnen angegebenen Speicherort erstellt.</span><span class="sxs-lookup"><span data-stu-id="547a4-110">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="547a4-111">Zusätzliche Setupprotokolldateien werden im Ordner "% Temp%" des Benutzers erstellt, der MBAM installiert.</span><span class="sxs-lookup"><span data-stu-id="547a4-111">Additional setup log files are created in the %temp% folder of the user who is installing MBAM.</span></span>

 

## <span data-ttu-id="547a4-112">So installieren Sie die MBAM-Server Features auf einem einzelnen Server</span><span class="sxs-lookup"><span data-stu-id="547a4-112">To install MBAM Server features on a single server</span></span>


<span data-ttu-id="547a4-113">In den folgenden Schritten wird beschrieben, wie allgemeine MBAM-Features installiert werden.</span><span class="sxs-lookup"><span data-stu-id="547a4-113">The following steps describe how to install general MBAM features.</span></span>

<span data-ttu-id="547a4-114">**Hinweis**  Stellen Sie sicher, dass Sie das 32-Bit-Setup auf 32-Bit-Servern und das 64-Bit-Setup auf 64-Bit-Servern verwenden.</span><span class="sxs-lookup"><span data-stu-id="547a4-114">**Note** Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>

 

**<span data-ttu-id="547a4-115">So starten Sie die Installation von MBAM Server Features</span><span class="sxs-lookup"><span data-stu-id="547a4-115">To start MBAM Server features installation</span></span>**

1.  <span data-ttu-id="547a4-116">Starten Sie den MBAM-Installations-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="547a4-116">Start the MBAM installation wizard.</span></span> <span data-ttu-id="547a4-117">Klicken Sie auf der Willkommensseite auf **Installieren** .</span><span class="sxs-lookup"><span data-stu-id="547a4-117">Click **Install** at the Welcome page.</span></span>

2.  <span data-ttu-id="547a4-118">Lesen und akzeptieren Sie die Microsoft-Software-Lizenzbestimmungen, und klicken Sie auf **weiter** , um die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="547a4-118">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

3.  <span data-ttu-id="547a4-119">Standardmäßig sind alle MBAM-Features für die Installation ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="547a4-119">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="547a4-120">Features, die auf demselben Computer installiert werden, müssen zur gleichen Zeit zusammen installiert werden.</span><span class="sxs-lookup"><span data-stu-id="547a4-120">Features that will be installed on the same computer must be installed together at the same time.</span></span> <span data-ttu-id="547a4-121">Deaktivieren Sie die Features, die Sie an anderer Stelle installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="547a4-121">Clear the features that you want to install elsewhere.</span></span> <span data-ttu-id="547a4-122">Sie müssen die MBAM-Features in der folgenden Reihenfolge installieren:</span><span class="sxs-lookup"><span data-stu-id="547a4-122">You must install the MBAM features in the following order:</span></span>

    -   <span data-ttu-id="547a4-123">Wiederherstellungs-und Hardware Datenbank</span><span class="sxs-lookup"><span data-stu-id="547a4-123">Recovery and Hardware Database</span></span>

    -   <span data-ttu-id="547a4-124">Konformitäts-und Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="547a4-124">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="547a4-125">Konformitätsprüfung und Berichte</span><span class="sxs-lookup"><span data-stu-id="547a4-125">Compliance Audit and Reports</span></span>

    -   <span data-ttu-id="547a4-126">Verwaltungs-und Überwachungs Server</span><span class="sxs-lookup"><span data-stu-id="547a4-126">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="547a4-127">MBAM-Gruppenrichtlinienvorlage</span><span class="sxs-lookup"><span data-stu-id="547a4-127">MBAM Group Policy Template</span></span>

    <span data-ttu-id="547a4-128">**Hinweis**  Der Installations-Assistent überprüft die Voraussetzungen für die Installation und zeigt die fehlenden Voraussetzungen an.</span><span class="sxs-lookup"><span data-stu-id="547a4-128">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="547a4-129">Wenn alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="547a4-129">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="547a4-130">Wenn eine fehlende Voraussetzung erkannt wird, müssen Sie die fehlenden Voraussetzungen beheben und dann **erneut auf Voraussetzungen prüfen**klicken.</span><span class="sxs-lookup"><span data-stu-id="547a4-130">If a missing prerequisite is detected, you must resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="547a4-131">Nachdem alle Voraussetzungen erfüllt wurden, wird die Installation fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="547a4-131">After all prerequisites are met, the installation resumes.</span></span>

     

4.  <span data-ttu-id="547a4-132">Sie werden aufgefordert, die Netzwerk Kommunikationssicherheit zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="547a4-132">You are prompted to configure the network communication security.</span></span> <span data-ttu-id="547a4-133">MBAM kann die Kommunikation zwischen der Wiederherstellungs-und Hardware Datenbank, dem Verwaltungs-und Überwachungs Server und den Clients verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="547a4-133">MBAM can encrypt the communication between the Recovery and Hardware Database, the Administration and Monitoring Server, and the clients.</span></span> <span data-ttu-id="547a4-134">Wenn Sie sich entschließen, die Kommunikation zu verschlüsseln, werden Sie aufgefordert, das Zertifizierungsstellenzertifikat auszuwählen, das für die Verschlüsselung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="547a4-134">If you decide to encrypt the communication, you are asked to select the authority-provisioned certificate that will be used for encryption.</span></span>

5.  <span data-ttu-id="547a4-135">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="547a4-135">Click **Next** to continue.</span></span>

6.  <span data-ttu-id="547a4-136">Der MBAM-Setup-Assistent zeigt die Installationsseiten für die ausgewählten Features an.</span><span class="sxs-lookup"><span data-stu-id="547a4-136">The MBAM Setup wizard will display the installation pages for the selected features.</span></span>

**<span data-ttu-id="547a4-137">So stellen Sie MBAM-Server Features bereit</span><span class="sxs-lookup"><span data-stu-id="547a4-137">To deploy MBAM Server features</span></span>**

1.  <span data-ttu-id="547a4-138">Geben Sie im Fenster **Wiederherstellungs-und Hardware Datenbank konfigurieren** die Instanz von SQL Server und den Namen der Datenbank an, in der die Wiederherstellungs-und Hardware Daten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="547a4-138">In the **Configure the Recovery and Hardware database** window, specify the instance of SQL Server and the name of the database that will store the recovery and hardware data.</span></span> <span data-ttu-id="547a4-139">Außerdem müssen Sie sowohl den Speicherort der Datenbankdateien als auch den Speicherort der Protokollinformationen angeben.</span><span class="sxs-lookup"><span data-stu-id="547a4-139">You must also specify both the database files location and the log information location.</span></span>

2.  <span data-ttu-id="547a4-140">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="547a4-140">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="547a4-141">Geben Sie im Fenster **Compliance-und Überwachungsdatenbank konfigurieren** die Instanz von SQL Server und den Namen der Datenbank an, in der die Konformitäts-und Überwachungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="547a4-141">In the **Configure the Compliance and Audit database** window, specify the instance of the SQL Server and the name of the database that will store the compliance and audit data.</span></span> <span data-ttu-id="547a4-142">Geben Sie dann den Speicherort der Datenbankdateien und den Speicherort der Protokollinformationen an.</span><span class="sxs-lookup"><span data-stu-id="547a4-142">Then, specify the database files location and the log information location.</span></span>

4.  <span data-ttu-id="547a4-143">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="547a4-143">Click **Next** to continue.</span></span>

5.  <span data-ttu-id="547a4-144">Geben Sie im Fenster **Konformitäts-und Überwachungsberichte** die Instanz des Berichts Diensts an, die verwendet wird, und geben Sie ein Domänenbenutzerkonto für den Zugriff auf die Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="547a4-144">In the **Compliance and Audit Reports** window, specify the report service instance that will be used and provide a domain user account for accessing the database.</span></span> <span data-ttu-id="547a4-145">Hierbei sollte es sich um ein Benutzerkonto handeln, das speziell für diese Verwendung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="547a4-145">This should be a user account that is provisioned specifically for this use.</span></span> <span data-ttu-id="547a4-146">Das Benutzerkonto sollte in der Lage sein, auf alle Daten zuzugreifen, die der Gruppe MBAM-Berichte Benutzer zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="547a4-146">The user account should be able to access all data available to the MBAM Reports Users group.</span></span>

6.  <span data-ttu-id="547a4-147">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="547a4-147">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="547a4-148">Geben Sie im Fenster **Verwaltungs-und Überwachungsserver konfigurieren** die **Port Bindung**, den **Hostnamen** (optional) und den **Installationspfad** für den MBAM-Verwaltungs-und-Überwachungsserver ein.</span><span class="sxs-lookup"><span data-stu-id="547a4-148">In the **Configure the Administration and Monitoring Server** window, enter the **Port Binding**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring server.</span></span>

    <span data-ttu-id="547a4-149">**Warnung**  Die von Ihnen angegebene Portnummer muss eine nicht verwendete Portnummer auf dem Verwaltungs-und Überwachungsserver sein, es sei denn, es wird ein eindeutiger Hostheadername angegeben.</span><span class="sxs-lookup"><span data-stu-id="547a4-149">**Warning** The port number that you specify must be an unused port number on the Administration and Monitoring server, unless a unique host header name is specified.</span></span>

     

8.  <span data-ttu-id="547a4-150">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="547a4-150">Click **Next** to continue.</span></span>

9.  <span data-ttu-id="547a4-151">Geben Sie an, ob Microsoft Updates dazu beitragen soll, Ihren Computer zu schützen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="547a4-151">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="547a4-152">Mit der Option "Microsoft Updates" werden die automatischen Updates in Windows nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="547a4-152">The Microsoft Updates option does not turn on the Automatic Updates in Windows.</span></span>

10. <span data-ttu-id="547a4-153">Wenn der Setup-Assistent die erforderlichen Funktionsinformationen gesammelt hat, kann die MBAM-Installation gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="547a4-153">When the Setup wizard has collected the necessary feature information, the MBAM installation is ready to start.</span></span> <span data-ttu-id="547a4-154">Klicken Sie auf **zurück** , um durch den Assistenten zurückzukehren, wenn Sie die Installationseinstellungen überprüfen oder ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="547a4-154">Click **Back** to move back through the wizard if you want to review or change your installation settings.</span></span> <span data-ttu-id="547a4-155">Klicken Sie auf **Installieren** , um mit der Installation zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="547a4-155">Click **Install** to begin the installation.</span></span> <span data-ttu-id="547a4-156">Klicken Sie auf **Abbrechen** , um Setup zu beenden.</span><span class="sxs-lookup"><span data-stu-id="547a4-156">Click **Cancel** to exit Setup.</span></span> <span data-ttu-id="547a4-157">Setup installiert die MBAM-Features und benachrichtigt Sie, dass die Installation abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="547a4-157">Setup installs the MBAM features and notifies you that the installation is completed.</span></span>

11. <span data-ttu-id="547a4-158">Klicken Sie auf **Fertig stellen** , um den Assistenten zu beenden.</span><span class="sxs-lookup"><span data-stu-id="547a4-158">Click **Finish** to exit the wizard.</span></span>

12. <span data-ttu-id="547a4-159">Nachdem Sie die MBAM-Server Features installiert haben, müssen Sie den MBAM-Rollen Benutzer hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="547a4-159">After you install MBAM server features, you must add users to the MBAM roles.</span></span> <span data-ttu-id="547a4-160">Weitere Informationen finden Sie unter [Planen von MBAM 1,0-Administrator Rollen](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="547a4-160">For more information, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

**<span data-ttu-id="547a4-161">So führen Sie die Konfiguration nach der Installation durch</span><span class="sxs-lookup"><span data-stu-id="547a4-161">To perform post installation configuration</span></span>**

1.  <span data-ttu-id="547a4-162">Nach Abschluss des Setups müssen Sie Benutzerrollen hinzufügen, damit Sie Benutzern den Zugriff auf Features auf der MBAM-Verwaltungswebsite gewähren können.</span><span class="sxs-lookup"><span data-stu-id="547a4-162">After Setup is finished, you must add user roles so that you can give users access to features in the MBAM administration website.</span></span> <span data-ttu-id="547a4-163">Fügen Sie auf dem Verwaltungs-und Überwachungs Server den folgenden lokalen Gruppen Benutzer hinzu:</span><span class="sxs-lookup"><span data-stu-id="547a4-163">On the Administration and Monitoring Server, add users to the following local groups:</span></span>

    -   <span data-ttu-id="547a4-164">**MBAM-Hardware Benutzer**: Mitglieder dieser lokalen Gruppe können auf das Hardware Feature auf der MBAM-Verwaltungswebsite zugreifen.</span><span class="sxs-lookup"><span data-stu-id="547a4-164">**MBAM Hardware Users**: Members of this local group can access the Hardware feature in the MBAM administration website.</span></span>

    -   <span data-ttu-id="547a4-165">**MBAM Helpdesk-Benutzer**: Mitglieder dieser lokalen Gruppe können auf die Laufwerk Wiederherstellung zugreifen und TPM-Features auf der MBAM-Verwaltungswebsite verwalten.</span><span class="sxs-lookup"><span data-stu-id="547a4-165">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage TPM features in the MBAM administration website.</span></span> <span data-ttu-id="547a4-166">Alle Felder in Laufwerk Wiederherstellung und TPM verwalten sind für einen Helpdesk-Benutzer Pflichtfelder.</span><span class="sxs-lookup"><span data-stu-id="547a4-166">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="547a4-167">**MBAM Advanced Helpdesk-Benutzer**: Mitglieder dieser lokalen Gruppe haben erweiterten Zugriff auf die Drive Recovery-und TPM-Features auf der MBAM-Verwaltungswebsite.</span><span class="sxs-lookup"><span data-stu-id="547a4-167">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features in the MBAM administration website.</span></span> <span data-ttu-id="547a4-168">Für erfahrene Helpdesk-Benutzer ist in Drive Recovery nur das Schlüssel-ID-Feld erforderlich.</span><span class="sxs-lookup"><span data-stu-id="547a4-168">For Advanced Helpdesk Users, only the Key ID field is required in Drive Recovery.</span></span> <span data-ttu-id="547a4-169">Für das Verwalten von TPM-Benutzern sind nur das Feld Computerdomäne und der Computer Name erforderlich.</span><span class="sxs-lookup"><span data-stu-id="547a4-169">For Manage TPM users, only the Computer Domain field and Computer Name field are required.</span></span>

2.  <span data-ttu-id="547a4-170">Fügen Sie auf der Verwaltungs-und Überwachungs Server-, Konformitäts-und Überwachungsdatenbank sowie auf dem Computer, der die Konformitäts-und Überwachungsberichte hostet, Benutzer zur folgenden lokalen Gruppe hinzu, damit Sie auf das Feature Berichte auf der MBAM-Verwaltungswebsite zugreifen können:</span><span class="sxs-lookup"><span data-stu-id="547a4-170">On the Administration and Monitoring Server, Compliance and Audit Database, and on the computer that hosts the Compliance and Audit Reports, add users to the following local group to enable them to access the Reports feature in the MBAM administration website:</span></span>

    -   <span data-ttu-id="547a4-171">**MBAM-Berichtsbenutzer**: Mitglieder dieser lokalen Gruppe können auf die Berichtsfeatures auf der MBAM-Verwaltungswebsite zugreifen.</span><span class="sxs-lookup"><span data-stu-id="547a4-171">**MBAM Report Users**: Members of this local group can access the Reports features in the MBAM administration website.</span></span>

    <span data-ttu-id="547a4-172">**Hinweis**  Identische Benutzermitgliedschaften oder Gruppenmitgliedschaften der lokalen Gruppe **MBAM-Berichtsbenutzer** müssen auf allen Computern verwaltet werden, auf denen die Verwaltungs-und Überwachungs Server Features, die Kompatibilitäts-und Überwachungsdatenbank sowie Compliance-und Überwachungsberichte installiert sind.</span><span class="sxs-lookup"><span data-stu-id="547a4-172">**Note** Identical user membership or group membership of the **MBAM Report Users** local group must be maintained on all computers where the Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports are installed.</span></span>

    <span data-ttu-id="547a4-173">Wenn Sie identische Mitgliedschaften auf allen Computern beibehalten möchten, sollten Sie eine Domänensicherheitsgruppe erstellen und diese Domänengruppe jeder lokalen MBAM-Berichtsbenutzer Gruppe hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="547a4-173">To maintain identical memberships on all computers, you should create a domain security group and add that domain group to each local MBAM Report Users group.</span></span> <span data-ttu-id="547a4-174">In diesem Fall können Sie die Gruppenmitgliedschaften mithilfe der Domänengruppe verwalten.</span><span class="sxs-lookup"><span data-stu-id="547a4-174">When you do this, you can manage the group memberships by using the domain group.</span></span>

     

## <span data-ttu-id="547a4-175">Überprüfen der MBAM Server-Feature-Installation</span><span class="sxs-lookup"><span data-stu-id="547a4-175">Validating the MBAM Server feature installation</span></span>


<span data-ttu-id="547a4-176">Wenn die MBAM-Installation abgeschlossen ist, überprüfen Sie, ob die Installation alle erforderlichen MBAM-Features erfolgreich eingerichtet hat, die für die BitLocker-Verwaltung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="547a4-176">When the MBAM installation is complete, validate that the installation has successfully set up all the necessary MBAM features that are required for BitLocker management.</span></span> <span data-ttu-id="547a4-177">Gehen Sie wie folgt vor, um zu überprüfen, ob der MBAM-Dienst funktionsfähig ist:</span><span class="sxs-lookup"><span data-stu-id="547a4-177">Use the following procedure to confirm that the MBAM service is functional:</span></span>

**<span data-ttu-id="547a4-178">So überprüfen Sie die Installation von MBAM Server Features</span><span class="sxs-lookup"><span data-stu-id="547a4-178">To validate MBAM Server feature installation</span></span>**

1. <span data-ttu-id="547a4-179">Öffnen Sie auf jedem Server, auf dem ein MBAM-Feature bereitgestellt wird, die **System**Steuerung.</span><span class="sxs-lookup"><span data-stu-id="547a4-179">On each server where an MBAM feature is deployed, open **Control Panel**.</span></span> <span data-ttu-id="547a4-180">Klicken Sie auf **Programme**und dann auf **Programme und Funktionen**.</span><span class="sxs-lookup"><span data-stu-id="547a4-180">Click **Programs**, and then click **Programs and Features**.</span></span> <span data-ttu-id="547a4-181">Überprüfen Sie, ob die **Microsoft BitLocker-Verwaltung und-Überwachung** in der Liste " **Programme und Features** " angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="547a4-181">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="547a4-182">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="547a4-182">Note</span></span>**  
   <span data-ttu-id="547a4-183">Um die Installation zu überprüfen, müssen Sie ein Domänenkonto verwenden, das über lokale Computeradministrator Anmeldeinformationen auf jedem Server verfügt.</span><span class="sxs-lookup"><span data-stu-id="547a4-183">To validate the installation, you must use a Domain Account that has local computer administrative credentials on each server.</span></span>

     

2. <span data-ttu-id="547a4-184">Öffnen Sie auf dem Server, auf dem die Wiederherstellungs-und Hardware Datenbank installiert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Wiederherstellungs-und Hardware** Datenbank installiert ist.</span><span class="sxs-lookup"><span data-stu-id="547a4-184">On the server where the Recovery and Hardware Database is installed, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="547a4-185">Öffnen Sie auf dem Server, auf dem die Compliance-und Überwachungsdatenbank installiert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Konformitäts-und Überwachungsdatenbank** installiert ist.</span><span class="sxs-lookup"><span data-stu-id="547a4-185">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio and verify that the **MBAM Compliance and Audit Database** is installed.</span></span>

4. <span data-ttu-id="547a4-186">Öffnen Sie auf dem Server, auf dem die Konformitäts-und Überwachungsberichte installiert sind, einen Webbrowser mit Administratorrechten, und navigieren Sie zu "Start" der SQL Server Reporting Services-Website.</span><span class="sxs-lookup"><span data-stu-id="547a4-186">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative privileges and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="547a4-187">Der standardmäßige Startspeicherort einer SQL Server Reporting Services-Websiteinstanz befindet sich unter http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.</span><span class="sxs-lookup"><span data-stu-id="547a4-187">The default Home location of a SQL Server Reporting Services site instance is at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.</span></span> <span data-ttu-id="547a4-188">Um die tatsächliche URL zu finden, verwenden Sie das Reporting Services-Konfigurations-Manager-Tool, und wählen Sie die während des Setups angegebenen Instanzen aus.</span><span class="sxs-lookup"><span data-stu-id="547a4-188">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances specified during setup.</span></span>

   <span data-ttu-id="547a4-189">Vergewissern Sie sich, dass ein Ordner mit dem Namen **Malta-Konformitätsberichte** aufgelistet ist und fünf Berichte und eine Datenquelle enthält.</span><span class="sxs-lookup"><span data-stu-id="547a4-189">Confirm that a folder named **Malta Compliance Reports** is listed and that it contains five reports and one data source.</span></span>

   **<span data-ttu-id="547a4-190">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="547a4-190">Note</span></span>**  
   <span data-ttu-id="547a4-191">Wenn SQL Server Reporting Services als benannte Instanz konfiguriert wurde, sollte die URL wie folgt aussehen: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="547a4-191">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following:http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>

     

5. <span data-ttu-id="547a4-192">Führen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungsfunktion installiert ist, den **Server-Manager** aus, navigieren Sie zu **Rollen**, wählen Sie **Webserver (IIS)** aus, und klicken Sie auf **Internet Informationsdienste (IIS)-Manager** .</span><span class="sxs-lookup"><span data-stu-id="547a4-192">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**, select **Web Server (IIS)**, and click **Internet Information Services (IIS) Manager**</span></span>

6. <span data-ttu-id="547a4-193">Navigieren Sie in **Verbindungen**zu \* &lt; Computername &gt; \*, wählen Sie **Websites**aus, und wählen Sie **Microsoft BitLocker-Verwaltung und-Überwachung**aus.</span><span class="sxs-lookup"><span data-stu-id="547a4-193">In **Connections**, browse to *&lt;computername&gt;*, select **Sites**, and select **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="547a4-194">Überprüfen Sie, ob **MBAMAdministrationService**, **MBAMComplianceStatusService**und **MBAMRecoveryAndHardwareService** aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="547a4-194">Verify that **MBAMAdministrationService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

7. <span data-ttu-id="547a4-195">Öffnen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungsfunktion installiert ist, einen Webbrowser mit Administratorrechten, und navigieren Sie dann zu den folgenden Speicherorten auf der MBAM-Website, um sicherzustellen, dass Sie erfolgreich geladen werden:</span><span class="sxs-lookup"><span data-stu-id="547a4-195">On the server where the Administration and Monitoring feature is installed, open a web browser with administrative privileges, and then browse to the following locations in the MBAM website to verify that they load successfully:</span></span>

   -   <span data-ttu-id="547a4-196">*http:// &lt; Computername &gt; /default.aspx* , und bestätigen Sie die einzelnen Links für Navigation und Berichte.</span><span class="sxs-lookup"><span data-stu-id="547a4-196">*http://&lt;computername&gt;/default.aspx* and confirm each of the links for navigation and reports</span></span>

   -   *<span data-ttu-id="547a4-197">http:// &lt; Computername &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="547a4-197">http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>*

   -   *<span data-ttu-id="547a4-198">http:// &lt; Computername &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="547a4-198">http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>*

   -   *<span data-ttu-id="547a4-199">http:// &lt; Computername &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="547a4-199">http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>*

   **<span data-ttu-id="547a4-200">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="547a4-200">Note</span></span>**  
   <span data-ttu-id="547a4-201">In der Regel werden die Dienste auf dem Standard Port 80 ohne Netzwerk Verschlüsselung installiert.</span><span class="sxs-lookup"><span data-stu-id="547a4-201">Typically, the services are installed on the default port 80 without network encryption.</span></span> <span data-ttu-id="547a4-202">Wenn die Dienste an einem anderen Port installiert sind, ändern Sie die URLs so, dass Sie den entsprechenden Port umfassen.</span><span class="sxs-lookup"><span data-stu-id="547a4-202">If the services are installed on a different port, change the URLs to include the appropriate port.</span></span> <span data-ttu-id="547a4-203">Beispiel\* &lt; : http://Computername &gt; : &lt; Port &gt; \*/default.aspx oder http:// <em> &lt; Hostheadername &gt; / </em> default. aspx.</span><span class="sxs-lookup"><span data-stu-id="547a4-203">For example, http://*&lt;computername&gt;:&lt;port&gt;*/default.aspx or http://<em>&lt;hostheadername&gt;/</em>default.aspx.</span></span>

   <span data-ttu-id="547a4-204">Wenn die Dienste mit Netzwerk Verschlüsselung installiert werden, ändern Sie http://in https://.</span><span class="sxs-lookup"><span data-stu-id="547a4-204">If the services are installed with network encryption, change http:// to https://.</span></span>

     

## <span data-ttu-id="547a4-205">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="547a4-205">Related topics</span></span>


[<span data-ttu-id="547a4-206">Bereitstellen der Serverinfrastruktur von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="547a4-206">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)

 

 





