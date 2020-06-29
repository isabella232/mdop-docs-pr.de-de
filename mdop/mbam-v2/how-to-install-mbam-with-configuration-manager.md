---
title: So installieren Sie MBAM mit dem Konfigurations-Manager
description: So installieren Sie MBAM mit dem Konfigurations-Manager
author: dansimp
ms.assetid: fd0832e4-3b79-4e56-9550-d2f396be6d09
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a556ce961e6a423caecdd0766cf8623383897b58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810969"
---
# <span data-ttu-id="71e6a-103">So installieren Sie MBAM mit dem Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="71e6a-103">How to Install MBAM with Configuration Manager</span></span>


<span data-ttu-id="71e6a-104">In diesem Abschnitt werden die Schritte zum Installieren von MBAM mit Configuration Manager unter Verwendung der empfohlenen Konfiguration beschrieben, die in [Erste Schritte mit MBAM mit Configuration Manager](getting-started---using-mbam-with-configuration-manager.md)veranschaulicht wird.</span><span class="sxs-lookup"><span data-stu-id="71e6a-104">This section describes the steps to install MBAM with Configuration Manager by using the recommended configuration, which is illustrated in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span></span> <span data-ttu-id="71e6a-105">Die Schritte sind in die folgenden Aufgaben gegliedert:</span><span class="sxs-lookup"><span data-stu-id="71e6a-105">The steps are divided into the following tasks:</span></span>

-   <span data-ttu-id="71e6a-106">Installieren und Konfigurieren von MBAM auf dem Configuration Manager-Server</span><span class="sxs-lookup"><span data-stu-id="71e6a-106">Install and configure MBAM on the Configuration Manager Server</span></span>

-   <span data-ttu-id="71e6a-107">Installieren der Wiederherstellungs-und Überwachungsdatenbanken auf dem Daten Bank Server</span><span class="sxs-lookup"><span data-stu-id="71e6a-107">Install the Recovery and Audit Databases on the Database Server</span></span>

-   <span data-ttu-id="71e6a-108">Installieren der Verwaltungs-und Überwachungsserver Features auf dem Verwaltungs-und Überwachungsserver</span><span class="sxs-lookup"><span data-stu-id="71e6a-108">Install the Administration and Monitoring Server features on the Administration and Monitoring Server</span></span>

<span data-ttu-id="71e6a-109">Bevor Sie mit der Installation beginnen, stellen Sie sicher, dass Sie die erforderlichen MOF-Dateien bearbeitet oder erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="71e6a-109">Before you begin the installation, ensure that you have edited or created the necessary mof files.</span></span> <span data-ttu-id="71e6a-110">Anweisungen hierzu finden Sie unter [erstellen oder Bearbeiten von MOF-Dateien](how-to-create-or-edit-the-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="71e6a-110">For instructions, see [How to Create or Edit the mof Files](how-to-create-or-edit-the-mof-files.md).</span></span>

<span data-ttu-id="71e6a-111">**Wichtig**  Wenn Sie eine nicht standardmäßige SQL Server Reporting Services (SSRS)-Instanz verwenden, müssen Sie das MBAM-Setup mithilfe der folgenden Befehlszeile starten, um die benannte SSRS-Instanz anzugeben:</span><span class="sxs-lookup"><span data-stu-id="71e6a-111">**Important** If you are using a non-default SQL Server Reporting Services (SSRS) instance, you must start the MBAM Setup by using the following command line to specify the SSRS named instance:</span></span>

`MbamSetup.exe CM_SSRS_INSTANCE_NAME=<NamedInstance>`

 

**<span data-ttu-id="71e6a-112">So installieren Sie MBAM auf dem Configuration Manager-Server</span><span class="sxs-lookup"><span data-stu-id="71e6a-112">To install MBAM on the Configuration Manager Server</span></span>**

1.  <span data-ttu-id="71e6a-113">Führen Sie auf dem Configuration Manager-Server **MBAMSetup.exe** aus, um den MBAM-Installations-Assistenten zu starten.</span><span class="sxs-lookup"><span data-stu-id="71e6a-113">On the Configuration Manager Server, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

    <span data-ttu-id="71e6a-114">**Hinweis**  Um die Setupprotokolldateien zu erhalten, müssen Sie das msiexec-Paket und die Option **/l** &lt; Location verwenden, &gt; um Configuration Manager zu installieren.</span><span class="sxs-lookup"><span data-stu-id="71e6a-114">**Note** To obtain the setup log files, you have to use the Msiexec package and the **/L** &lt;location&gt; option to install Configuration Manager.</span></span> <span data-ttu-id="71e6a-115">Protokolldateien werden an dem von Ihnen angegebenen Speicherort erstellt.</span><span class="sxs-lookup"><span data-stu-id="71e6a-115">Log files are created in the location that you specify.</span></span>

    <span data-ttu-id="71e6a-116">Zusätzliche Setupprotokolldateien werden im Ordner% Temp% auf dem Computer des Benutzers erstellt, der Configuration Manager installiert.</span><span class="sxs-lookup"><span data-stu-id="71e6a-116">Additional setup log files are created in the %temp% folder on the computer of the user who is installing Configuration Manager.</span></span>

     

2.  <span data-ttu-id="71e6a-117">Wählen Sie auf der **Willkommens** Seite optional das **Programm zur Verbesserung der Benutzerfreundlichkeit**aus, und klicken Sie dann auf **Start**.</span><span class="sxs-lookup"><span data-stu-id="71e6a-117">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="71e6a-118">Lesen und akzeptieren Sie den Microsoft-Software-Lizenzvertrag, und klicken Sie auf **weiter** , um die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="71e6a-118">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="71e6a-119">Wählen Sie auf der Seite **Topologie Auswahl** die Option **System Center Configuration Manager-Integration**aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="71e6a-119">On the **Topology Selection** page, select **System Center Configuration Manager Integration**, and then click **Next**.</span></span>

5.  <span data-ttu-id="71e6a-120">Wählen Sie auf der Seite **zu installierende Features auswählen** die Option **System Center Configuration Manager-Integration**aus.</span><span class="sxs-lookup"><span data-stu-id="71e6a-120">On the **Select features to install** page, select **System Center Configuration Manager Integration**.</span></span>

    <span data-ttu-id="71e6a-121">**Hinweis**  Klicken Sie auf der Seite **Voraussetzungen prüfen** auf **weiter** , nachdem der Installations-Assistent die Voraussetzungen für die Installation überprüft hat, und bestätigt, dass keine vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="71e6a-121">**Note** On the **Checking Prerequisites** page, click **Next** after the installation wizard checks the prerequisites for your installation and confirms that none are missing.</span></span> <span data-ttu-id="71e6a-122">Wenn eine fehlende Voraussetzung erkannt wird, müssen Sie die fehlenden Voraussetzungen beheben und dann **erneut auf Voraussetzungen prüfen klicken.**</span><span class="sxs-lookup"><span data-stu-id="71e6a-122">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again.**</span></span>

     

6.  <span data-ttu-id="71e6a-123">Geben Sie an, ob Microsoft Updates dazu beitragen soll, Ihren Computer zu schützen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="71e6a-123">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="71e6a-124">Bei Verwendung von Microsoft Updates werden die automatischen Updates in Windows nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="71e6a-124">Using Microsoft Updates does not turn on Automatic Updates in Windows.</span></span>

7.  <span data-ttu-id="71e6a-125">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="71e6a-125">Click **Next** to continue.</span></span>

8.  <span data-ttu-id="71e6a-126">Überprüfen Sie auf der Seite **Installationszusammenfassung** die Liste der Features, die installiert werden sollen, und klicken Sie auf **Installieren** , um mit der Installation der MBAM-Features zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="71e6a-126">On the **Installation Summary** page, review the list of features that will be installed, and click **Install** to start installing the MBAM features.</span></span> <span data-ttu-id="71e6a-127">Klicken Sie auf **zurück** , um durch den Assistenten zurückzukehren, wenn Sie die Installationseinstellungen überprüfen oder ändern müssen, oder klicken Sie auf **Abbrechen** , um Setup zu beenden.</span><span class="sxs-lookup"><span data-stu-id="71e6a-127">Click **Back** to move back through the wizard if you have to review or change your installation settings, or click **Cancel** to exit Setup.</span></span> <span data-ttu-id="71e6a-128">Setup installiert die MBAM-Features und benachrichtigt Sie, dass die Installation abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="71e6a-128">Setup installs the MBAM features and notifies you that the installation is completed.</span></span>

9.  <span data-ttu-id="71e6a-129">Klicken Sie auf **Fertig stellen** , um den Assistenten zu beenden.</span><span class="sxs-lookup"><span data-stu-id="71e6a-129">Click **Finish** to exit the wizard.</span></span>

**<span data-ttu-id="71e6a-130">So installieren Sie die Wiederherstellungs-und Überwachungsdatenbanken auf dem Daten Bank Server</span><span class="sxs-lookup"><span data-stu-id="71e6a-130">To install the Recovery and Audit Databases on the Database Server</span></span>**

1.  <span data-ttu-id="71e6a-131">Führen Sie auf dem Daten Bank Server **MBAMSetup.exe** aus, um den MBAM-Installations-Assistenten zu starten.</span><span class="sxs-lookup"><span data-stu-id="71e6a-131">On the Database Server, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="71e6a-132">Wählen Sie auf der **Willkommens** Seite optional das **Programm zur Verbesserung der Benutzerfreundlichkeit**aus, und klicken Sie dann auf **Start**.</span><span class="sxs-lookup"><span data-stu-id="71e6a-132">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="71e6a-133">Lesen und akzeptieren Sie den Microsoft-Software-Lizenzvertrag, und klicken Sie auf **weiter** , um die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="71e6a-133">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="71e6a-134">Wählen Sie auf der Seite **Topologie Auswahl** die **System Center Configuration Manager-Integrations** Topologie aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="71e6a-134">On the **Topology Selection** page, select the **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="71e6a-135">Wählen Sie in der Liste der zu installierenden Features die Option **Wiederherstellungsdatenbank** und **Überwachungsdatenbank**aus, und deaktivieren Sie die restlichen Features.</span><span class="sxs-lookup"><span data-stu-id="71e6a-135">From the list of features to install, select **Recovery Database** and **Audit Database**, and clear the remaining features.</span></span>

    <span data-ttu-id="71e6a-136">**Hinweis**  Der Installations-Assistent überprüft die Voraussetzungen für die Installation und zeigt die fehlenden Voraussetzungen an.</span><span class="sxs-lookup"><span data-stu-id="71e6a-136">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="71e6a-137">Wenn alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="71e6a-137">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="71e6a-138">Wenn eine fehlende Voraussetzung erkannt wird, müssen Sie die fehlenden Voraussetzungen beheben und dann **erneut auf Voraussetzungen prüfen**klicken.</span><span class="sxs-lookup"><span data-stu-id="71e6a-138">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="71e6a-139">Wenn dieses Mal alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="71e6a-139">If all prerequisites are met this time, the installation resumes.</span></span>

     

6.  <span data-ttu-id="71e6a-140">Geben Sie auf der Seite " **Wiederherstellungsdatenbank konfigurieren** " die Namen der Computer an, auf denen das Feature "Verwaltungs-und Überwachungs Server" ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="71e6a-140">On the **Configure the Recovery Database** page, specify the names of the computers that will be running the Administration and Monitoring Server feature.</span></span> <span data-ttu-id="71e6a-141">Nach der Bereitstellung des Verwaltungs-und Überwachungs Server Features wird mit dem Domänenkonto eine Verbindung mit der Datenbank hergestellt.</span><span class="sxs-lookup"><span data-stu-id="71e6a-141">After the Administration and Monitoring Server feature is deployed, it uses its domain account to connect to the database.</span></span>

7.  <span data-ttu-id="71e6a-142">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="71e6a-142">Click **Next** to continue.</span></span>

8.  <span data-ttu-id="71e6a-143">Geben Sie den Namen der SQL Server-Instanz und den Namen der Datenbank an, in der die Wiederherstellungsdaten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="71e6a-143">Specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="71e6a-144">Sie müssen außerdem angeben, an welcher Stelle die Datenbank gespeichert werden soll und wo sich die Protokollinformationen befinden sollen.</span><span class="sxs-lookup"><span data-stu-id="71e6a-144">You must also specify both where the database will be located and where the log information will be located.</span></span>

9.  <span data-ttu-id="71e6a-145">Klicken Sie auf **weiter** , um mit dem MBAM Setup-Installations-Assistenten fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="71e6a-145">Click **Next** to continue with the MBAM Setup installation wizard.</span></span>

10. <span data-ttu-id="71e6a-146">Geben Sie auf der Seite **Audit Database konfigurieren** das Benutzerkonto an, das für den Zugriff auf die Datenbank für Berichte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="71e6a-146">On the **Configure the Audit Database** page, specify the user account that will be used to access the database for reports.</span></span>

11. <span data-ttu-id="71e6a-147">Geben Sie die Computernamen der Computer an, auf denen der Verwaltungs-und Überwachungs Server und die Überwachungsberichte ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="71e6a-147">Specify the computer names of the computers that will be running the Administration and Monitoring Server and the Audit Reports.</span></span> <span data-ttu-id="71e6a-148">Nachdem die Verwaltungs-und Überwachungs-und Überwachungsberichts Features bereitgestellt wurden, werden Ihre Domänenkonten zum Herstellen einer Verbindung mit den Datenbanken verwendet.</span><span class="sxs-lookup"><span data-stu-id="71e6a-148">After the Administration and Monitoring and the Audit Reports features are deployed, their domain accounts will be used to connect to the databases.</span></span>

    <span data-ttu-id="71e6a-149">**Hinweis**  Wenn Sie die Überwachungsdatenbank ohne das Feature Überwachungsberichte installieren, müssen Sie auf dem Überwachungsdaten Bank Computer eine Ausnahme hinzufügen, um eingehenden Datenverkehr auf dem Microsoft SQL Server-Port zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="71e6a-149">**Note** If you are installing the Audit Database without the Audit Reports feature, you must add an exception on the Audit Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="71e6a-150">Die Standardportnummer ist 1433.</span><span class="sxs-lookup"><span data-stu-id="71e6a-150">The default port number is 1433.</span></span>

     

12. <span data-ttu-id="71e6a-151">Geben Sie den Namen der SQL Server-Instanz und den Namen der Datenbank an, in der die Überwachungsdaten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="71e6a-151">Specify the SQL Server instance name and the name of the database that will store the audit data.</span></span> <span data-ttu-id="71e6a-152">Sie müssen außerdem angeben, wo sich die Datenbank-und Protokollinformationen befinden sollen.</span><span class="sxs-lookup"><span data-stu-id="71e6a-152">You must also specify where the database and log information will be located.</span></span>

13. <span data-ttu-id="71e6a-153">Klicken Sie auf **Installieren** , um die Installation zu starten, und klicken Sie dann auf **Fertig stellen** , um die Installation abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="71e6a-153">Click **Install** to start the installation, and then click **Finish** to complete the installation.</span></span>

**<span data-ttu-id="71e6a-154">So installieren Sie die Verwaltungs-und Überwachungsserver Features auf dem Verwaltungs-und Überwachungsserver</span><span class="sxs-lookup"><span data-stu-id="71e6a-154">To install the Administration and Monitoring Server features on the Administration and Monitoring Server</span></span>**

1.  <span data-ttu-id="71e6a-155">Führen Sie auf dem Verwaltungs-und Überwachungs Server **MBAMSetup.exe** aus, um den MBAM-Installations-Assistenten zu starten.</span><span class="sxs-lookup"><span data-stu-id="71e6a-155">On the Administration and Monitoring Server, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="71e6a-156">Wählen Sie auf der **Willkommens** Seite optional das **Programm zur Verbesserung der Benutzerfreundlichkeit**aus, und klicken Sie dann auf **Start**.</span><span class="sxs-lookup"><span data-stu-id="71e6a-156">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="71e6a-157">Lesen und akzeptieren Sie den Microsoft-Software-Lizenzvertrag, und klicken Sie auf **weiter** , um die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="71e6a-157">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="71e6a-158">Wählen Sie auf der Seite **Topologie Auswahl** die **System Center Configuration Manager-Integrations** Topologie aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="71e6a-158">On the **Topology Selection** page, select the **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="71e6a-159">Wählen Sie in der Liste der zu installierenden Features **Administration und Monitoring Server** und **Self-Service Portal**aus, und deaktivieren Sie die restlichen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="71e6a-159">From the list of features to install, select **Administration and Monitoring Server** and **Self-Service Portal**, and clear the remaining features.</span></span>

    <span data-ttu-id="71e6a-160">**Hinweis**  Der Installations-Assistent überprüft die Voraussetzungen für die Installation und zeigt die fehlenden Voraussetzungen an.</span><span class="sxs-lookup"><span data-stu-id="71e6a-160">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="71e6a-161">Wenn alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="71e6a-161">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="71e6a-162">Wenn eine fehlende Voraussetzung erkannt wird, müssen Sie die fehlenden Voraussetzungen beheben und dann **erneut auf Voraussetzungen prüfen**klicken.</span><span class="sxs-lookup"><span data-stu-id="71e6a-162">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="71e6a-163">Wenn dieses Mal alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="71e6a-163">If all prerequisites are met this time, the installation resumes.</span></span>

     

6.  <span data-ttu-id="71e6a-164">Installieren Sie das Self-Service-Portal, indem Sie die Schritte im Abschnitt **So installieren Sie das Self-Service-Portal** unter [so wird es gemacht: Installieren und Konfigurieren von MBAM auf verteilten Servern](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="71e6a-164">Install the Self-Service Portal by following the steps in the **To install the Self-Service Portal** section in [How to Install and Configure MBAM on Distributed Servers](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span></span>

    <span data-ttu-id="71e6a-165">**Hinweis**  Wenn die Clientcomputer nicht auf das Microsoft Content Delivery Network (CDN) zugreifen können, wodurch dem Self-Service-Portal der erforderliche Zugriff auf bestimmte JavaScript-Dateien gewährt wird, führen Sie die Schritte unter **so konfigurieren Sie das Self-Service-Portal aus, wenn Endbenutzer nicht auf den Abschnitt Microsoft Content Delivery Network zugreifen können** , [wie Sie MBAM auf verteilten Servern installieren und konfigurieren](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md) können, um das Self-Service-Portal so zu konfigurieren, dass es von einer barrierefreien Quelle aus</span><span class="sxs-lookup"><span data-stu-id="71e6a-165">**Note** If the client computers will not have access to the Microsoft Content Delivery Network (CDN), which gives the Self-Service Portal the required access to certain JavaScript files, complete the steps in the **To configure the Self-Service Portal when end users cannot access the Microsoft Content Delivery Network** section [How to Install and Configure MBAM on Distributed Servers](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md) to configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span>

     

7.  <span data-ttu-id="71e6a-166">Installieren Sie die Verwaltungs-und Überwachungsserver Features, indem Sie die Schritte im Abschnitt **So installieren Sie den Verwaltungs-und Überwachungsserver-Feature** unter Installieren [und Konfigurieren von MBAM auf verteilten Servern](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md)ausführen.</span><span class="sxs-lookup"><span data-stu-id="71e6a-166">Install the Administration and Monitoring Server features by following the steps in the **To install the Administration and Monitoring Server feature** section in [How to Install and Configure MBAM on Distributed Servers](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span></span>

8.  <span data-ttu-id="71e6a-167">Klicken Sie auf **Fertig stellen** , um die Installation abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="71e6a-167">Click **Finish** to complete the installation.</span></span>

## <span data-ttu-id="71e6a-168">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="71e6a-168">Related topics</span></span>


[<span data-ttu-id="71e6a-169">So überprüfen Sie die MBAM-Installation mit dem Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="71e6a-169">How to Validate the MBAM Installation with Configuration Manager</span></span>](how-to-validate-the-mbam-installation-with-configuration-manager.md)

[<span data-ttu-id="71e6a-170">Bereitstellen von MBAM mit dem Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="71e6a-170">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





