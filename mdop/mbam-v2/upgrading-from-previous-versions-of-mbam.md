---
title: Aktualisieren von früheren MBAM-Versionen
description: Aktualisieren von früheren MBAM-Versionen
author: dansimp
ms.assetid: 73b425cf-9cd9-4ebc-a35e-1b3bf18596ce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af45d193a5e8001288e70389ff220cb5d8269918
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810177"
---
# <span data-ttu-id="4a86b-103">Aktualisieren von früheren MBAM-Versionen</span><span class="sxs-lookup"><span data-stu-id="4a86b-103">Upgrading from Previous Versions of MBAM</span></span>


<span data-ttu-id="4a86b-104">Sie können die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mit der eigenständigen Topologie oder der Configuration Manager-Topologie auf MBAM 2.0 aktualisieren, indem Sie wie folgt vorgehen:</span><span class="sxs-lookup"><span data-stu-id="4a86b-104">You can upgrade Microsoft BitLocker Administration and Monitoring (MBAM) to MBAM2.0, with the Stand-alone topology or Configuration Manager topology, by doing the following:</span></span>

-   <span data-ttu-id="4a86b-105">**Manueller in-Place-Server Austausch** – um den MBAM-Server zu aktualisieren, deinstallieren Sie MBAM manuell mithilfe des Installationsprogramms oder der Systemsteuerung, und installieren Sie dann die MBAM 2.0-Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="4a86b-105">**Manual in-place server replacement** – To upgrade the MBAM Server, manually uninstall MBAM by using either the installer or Control Panel, and then install the MBAM2.0 infrastructure.</span></span> <span data-ttu-id="4a86b-106">Sie müssen die Datenbanken nicht entfernen.</span><span class="sxs-lookup"><span data-stu-id="4a86b-106">You do not have to remove the databases.</span></span> <span data-ttu-id="4a86b-107">Bei der Deinstallation des MBAM 1,0-Servers bleiben die MBAM-Datenbanken intakt.</span><span class="sxs-lookup"><span data-stu-id="4a86b-107">Uninstalling the MBAM 1.0 Server leaves the MBAM databases intact.</span></span> <span data-ttu-id="4a86b-108">Wenn Sie dieselben Datenbanken angeben, die von MBAM 1,0 verwendet wurden, behält die MBAM 2.0-Installation MBAM 1,0-Daten in den Datenbanken bei und wandelt die Datenbanken in die Arbeit mit MBAM 2.0 um.</span><span class="sxs-lookup"><span data-stu-id="4a86b-108">If you specify the same databases that MBAM 1.0 was using, the MBAM2.0 installation retains MBAM 1.0 data in the databases and converts the databases to work with MBAM2.0.</span></span>

-   <span data-ttu-id="4a86b-109">**Upgrade des verteilten Clients** – Wenn Sie die eigenständige MBAM-Topologie verwenden, können Sie die MBAM-Clients nach der Installation der MBAM 2,0-Server Infrastruktur schrittweise aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4a86b-109">**Distributed Client Upgrade** - If you are using the Stand-alone MBAM topology, you can upgrade the MBAM Clients gradually after you install the MBAM 2.0 Server infrastructure.</span></span> <span data-ttu-id="4a86b-110">Der MBAM 2,0-Server erkennt die Version des vorhandenen Clients und führt die erforderlichen Schritte aus, um auf den 2,0-Client zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4a86b-110">The MBAM 2.0 Server detects the version of the existing Client and performs the required steps to upgrade to the 2.0 Client.</span></span>

    <span data-ttu-id="4a86b-111">Nachdem Sie die MBAM 2,0-Serverinfrastruktur aktualisiert haben, melden MBAM 1,0-Clients weiterhin erfolgreich an den MBAM 2,0-Server, indem Sie Wiederherstellungsdaten überwachen, aber die Compliance basiert auf den Richtlinien in MBAM 1,0.</span><span class="sxs-lookup"><span data-stu-id="4a86b-111">After you upgrade the MBAM 2.0 Server infrastructure, MBAM 1.0 Clients continue to report to the MBAM 2.0 Server successfully, escrowing recovery data, but compliance will be based on the policies in MBAM 1.0.</span></span> <span data-ttu-id="4a86b-112">Sie müssen Clients auf MBAM 2,0 aktualisieren, damit Clientcomputer die Kompatibilität mit den MBAM 2,0-Richtlinien exakt melden.</span><span class="sxs-lookup"><span data-stu-id="4a86b-112">You must upgrade clients to MBAM 2.0 to have client computers accurately report compliance against the MBAM 2.0 policies.</span></span> <span data-ttu-id="4a86b-113">Sie können die Clients auf den MBAM 2,0-Client aktualisieren, ohne den vorherigen Client zu deinstallieren, und der Client beginnt, MBAM 2,0-Richtlinien anzuwenden und zu melden.</span><span class="sxs-lookup"><span data-stu-id="4a86b-113">You can upgrade the clients to the MBAM 2.0 Client without uninstalling the previous client, and the client will start to apply and report MBAM 2.0 policies.</span></span>

    <span data-ttu-id="4a86b-114">Wenn Sie MBAM mit Configuration Manager verwenden, müssen Sie die MBAM 1,0-Clients auf MBAM 2,0 aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4a86b-114">If you are using MBAM with Configuration Manager, you must upgrade the MBAM 1.0 clients to MBAM 2.0.</span></span>

## <span data-ttu-id="4a86b-115">Aktualisieren von MBAM von einer Architektur mit zwei Servern</span><span class="sxs-lookup"><span data-stu-id="4a86b-115">Upgrading MBAM from a Two-Server Architecture</span></span>


<span data-ttu-id="4a86b-116">Führen Sie die folgenden Anweisungen aus, um eine frühere Version von MBAM zu aktualisieren, wenn Sie eine Architektur mit zwei Servern verwenden, bei der ein Server die Microsoft SQL Server-Komponenten hostet und der andere Server die Websites und Dienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4a86b-116">Use the following instructions to upgrade from a previous version of MBAM when you are using a two-server architecture, where one server is hosting the Microsoft SQL Server components, and the other server is hosting the websites and services.</span></span>

**<span data-ttu-id="4a86b-117">So aktualisieren Sie MBAM von einer Architektur mit zwei Servern</span><span class="sxs-lookup"><span data-stu-id="4a86b-117">To upgrade MBAM from a two-server architecture</span></span>**

1.  <span data-ttu-id="4a86b-118">Wählen Sie auf dem Server mit den SQL Server-Features in der Systemsteuerung die Option **Programme und Features**aus, und deinstallieren Sie dann die **Microsoft BitLocker-Verwaltung und-Überwachung**.</span><span class="sxs-lookup"><span data-stu-id="4a86b-118">On the server with the SQL Server features, in Control Panel, select **Programs and Features**, and then uninstall **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="4a86b-119">Die Datenbank für die Wiederherstellung und die Konformitäts-und Überwachungsdatenbank bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="4a86b-119">The Recovery Database and Compliance and Audit database remain unchanged.</span></span>

2.  <span data-ttu-id="4a86b-120">Führen Sie **MBAMSetup.exe** für Version MBAM 2,0 aus, und wählen Sie optional das **Programm zur Verbesserung der Benutzerfreundlichkeit**aus, und klicken Sie dann auf **Start**.</span><span class="sxs-lookup"><span data-stu-id="4a86b-120">Run **MBAMSetup.exe** for version MBAM 2.0, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="4a86b-121">Lesen und akzeptieren Sie den Microsoft-Software-Lizenzvertrag, und klicken Sie auf **weiter** , um die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="4a86b-121">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="4a86b-122">Wählen Sie auf der Seite **Topologie Auswahl** die **eigenständige** oder **System Center Configuration Manager-Integrations** Topologie aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="4a86b-122">On the **Topology Selection** page, select the **Stand-alone** or **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="4a86b-123">Deaktivieren Sie auf der Seite **zu installierende Features auswählen** die Features **Self-Service Server** und **Administration und Monitoring Server** , und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="4a86b-123">On the **Select features to install** page, clear the **Self-Service Server** and **Administration and Monitoring Server** features, and then click **Next**.</span></span>

6.  <span data-ttu-id="4a86b-124">Warten Sie, bis die Voraussetzungen für die Prüfung abgeschlossen sind, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="4a86b-124">Wait for the prerequisite checks to finish, and then click **Next**.</span></span> <span data-ttu-id="4a86b-125">Wenn eine fehlende Voraussetzung erkannt wird, beheben Sie die fehlenden Voraussetzungen, und klicken Sie dann **erneut auf Voraussetzungen prüfen**.</span><span class="sxs-lookup"><span data-stu-id="4a86b-125">If a missing prerequisite is detected, resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span>

7.  <span data-ttu-id="4a86b-126">Geben Sie auf dem Konto für den **Zugriff auf die Seite MBAM-Datenbanken** den Computernamen für den Server ein, der die Websites und Dienste hosten soll, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="4a86b-126">On the **Provide account used to access the MBAM databases** page, provide the computer name for the server that will host the sites and services, and then click **Next**.</span></span>

8.  <span data-ttu-id="4a86b-127">Geben Sie auf der Seite " **Wiederherstellungsdatenbank konfigurieren** " den Namen der SQL Server-Instanz und den Namen der Datenbank an, in der die Wiederherstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4a86b-127">On the **Configure the Recovery database** page, specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="4a86b-128">Sie müssen außerdem angeben, wo sich die Datenbankdateien und Protokollinformationen befinden sollen.</span><span class="sxs-lookup"><span data-stu-id="4a86b-128">You must also specify where the database files and log information will be located.</span></span>

9.  <span data-ttu-id="4a86b-129">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="4a86b-129">Click **Next** to continue.</span></span>

10. <span data-ttu-id="4a86b-130">Geben Sie auf der Seite **Compliance-und Überwachungsdatenbank konfigurieren** den Namen der SQL Server-Instanz und den Namen der Datenbank an, in der die Konformitäts-und Überwachungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4a86b-130">On the **Configure the Compliance and Audit database** page, specify the SQL Server instance name and the name of the database that will store the compliance and audit data.</span></span>

11. <span data-ttu-id="4a86b-131">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="4a86b-131">Click **Next** to continue.</span></span>

12. <span data-ttu-id="4a86b-132">Geben Sie auf der Seite **Compliance-und Überwachungsberichte konfigurieren** die SQL Server Reporting Services-Instanz an, in der die Kompatibilitäts-und Überwachungsberichte installiert werden, und geben Sie ein Domänenbenutzerkonto und ein Kennwort für den Zugriff auf die Datenbank Compliance und Audit an.</span><span class="sxs-lookup"><span data-stu-id="4a86b-132">On the **Configure the Compliance and Audit Reports** page, specify the SQL Server Reporting Services instance where the Compliance and Audit reports will be installed, and provide a domain user account and password to access the Compliance and Audit database.</span></span> <span data-ttu-id="4a86b-133">Konfigurieren Sie das Kennwort für dieses Konto so, dass es nie abläuft.</span><span class="sxs-lookup"><span data-stu-id="4a86b-133">Configure the password for this account to never expire.</span></span> <span data-ttu-id="4a86b-134">Das Benutzerkonto kann auf alle Daten zugreifen, die der Gruppe MBAM-Berichte Benutzer zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="4a86b-134">The user account can access all data available to the MBAM Reports Users group.</span></span>

13. <span data-ttu-id="4a86b-135">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="4a86b-135">Click **Next** to continue.</span></span>

14. <span data-ttu-id="4a86b-136">Geben Sie an, ob Microsoft Updates dazu beitragen soll, Ihren Computer zu schützen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="4a86b-136">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="4a86b-137">Damit werden die automatischen Updates in Windows nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4a86b-137">This does not turn on Automatic Updates in Windows.</span></span> <span data-ttu-id="4a86b-138">Wenn Sie zuvor entschieden haben, Microsoft Update für dieses Produkt oder ein anderes Produkt zu verwenden, wird die Seite Microsoft Update nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4a86b-138">If you previously chose to use Microsoft Update for this product or another product, the Microsoft Update page does not appear.</span></span>

15. <span data-ttu-id="4a86b-139">Überprüfen Sie auf der Seite **Installationszusammenfassung** die Features, die installiert werden sollen, und klicken Sie dann auf **Installieren** , um die Installation zu starten.</span><span class="sxs-lookup"><span data-stu-id="4a86b-139">On the **Installation Summary** page, review the features that will be installed, and then click **Install** to start the installation.</span></span>

**<span data-ttu-id="4a86b-140">So deinstallieren Sie die Verwaltungs-und Überwachungs Server Features und führen das Upgrade durch</span><span class="sxs-lookup"><span data-stu-id="4a86b-140">To uninstall the Administration and Monitoring Server features and to complete the upgrade</span></span>**

1.  <span data-ttu-id="4a86b-141">Wählen Sie auf dem Computer, der die Verwaltungs-und Überwachungs Server Features hostet, in der Systemsteuerung die Option **Programme und Features**aus, und deinstallieren Sie MBAM, um die zuvor installierten Websites und Dienste zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="4a86b-141">On the computer that hosts the Administration and Monitoring Server features, in Control Panel, select **Programs and Features**, and then uninstall MBAM to remove the previously installed websites and services.</span></span>

2.  <span data-ttu-id="4a86b-142">Führen Sie die **MBAMSetup.exe** für Version 2,0 aus, und wählen Sie optional das **Programm zur Verbesserung der Benutzerfreundlichkeit**aus, und klicken Sie dann auf **Start**.</span><span class="sxs-lookup"><span data-stu-id="4a86b-142">Run the **MBAMSetup.exe** for version 2.0, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="4a86b-143">Lesen und akzeptieren Sie den Microsoft-Software-Lizenzvertrag, und klicken Sie auf **weiter** , um die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="4a86b-143">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="4a86b-144">Wählen Sie auf der Seite **Topologie Auswahl** die **eigenständige** oder **System Center Configuration Manager-Integrations** Topologie aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="4a86b-144">On the **Topology Selection** page, select the **Stand-alone** or **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="4a86b-145">Deaktivieren Sie auf der Seite **zu installierende Features auswählen** die Features **Recovery Database** und **Compliance und Audit Database** sowie **Compliance und Überwachungsberichte** , und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="4a86b-145">On the **Select features to install** page, clear the **Recovery Database** and **Compliance and Audit Database** and **Compliance and Audit Reports** features, and then click **Next**.</span></span>

6.  <span data-ttu-id="4a86b-146">Warten Sie, bis die Voraussetzungen für die Prüfung abgeschlossen sind, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="4a86b-146">Wait for the prerequisite checks to finish, and then click **Next**.</span></span> <span data-ttu-id="4a86b-147">Wenn eine fehlende Voraussetzung erkannt wird, beheben Sie zuerst die fehlenden Voraussetzungen, und klicken Sie dann **erneut auf Voraussetzungen prüfen**.</span><span class="sxs-lookup"><span data-stu-id="4a86b-147">If a missing prerequisite is detected, resolve the missing prerequisites first, and then click **Check prerequisites again**.</span></span>

7.  <span data-ttu-id="4a86b-148">Wählen Sie auf der Seite **Netzwerk Kommunikationssicherheit konfigurieren** aus, ob die SSL-Verschlüsselung (Secure Socket Layer) für die Websites und Dienste verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a86b-148">On the **Configure network communication security** page, choose whether to use Secure Socket Layer (SSL) encryption for the websites and services.</span></span> <span data-ttu-id="4a86b-149">Wenn Sie sich entschließen, die Kommunikation zu verschlüsseln, wählen Sie das Zertifizierungsstellenzertifikat aus, das Sie für die Verschlüsselung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="4a86b-149">If you decide to encrypt the communication, select the certification authority (CA) certificate to use for encryption.</span></span>

    <span data-ttu-id="4a86b-150">**Hinweis**  Das Zertifikat muss vor diesem Schritt erstellt werden, damit Sie es auf dieser Seite auswählen können.</span><span class="sxs-lookup"><span data-stu-id="4a86b-150">**Note** The certificate must be created before this step to enable you to select it on this page.</span></span>

     

8.  <span data-ttu-id="4a86b-151">Geben Sie auf der Seite **Konfigurieren Sie den Speicherort der Kompatibilitäts Status Datenbank** den Namen der SQL Server-Instanz und den Namen der Datenbank an, in der die Konformitäts-und Überwachungsdaten gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="4a86b-151">On the **Configure the location of the Compliance Status database** page, specify the SQL Server instance name and the name of the database that stores the compliance and audit data.</span></span> <span data-ttu-id="4a86b-152">Sie müssen außerdem angeben, wo sich die Datenbankdateien und Protokollinformationen befinden sollen.</span><span class="sxs-lookup"><span data-stu-id="4a86b-152">You must also specify where the database files and log information will be located.</span></span>

9.  <span data-ttu-id="4a86b-153">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="4a86b-153">Click **Next** to continue.</span></span>

10. <span data-ttu-id="4a86b-154">Geben Sie auf der Seite **Konfigurieren Sie den Speicherort der Wiederherstellungsdatenbank** an den Namen der SQL Server-Instanz und den Namen der Datenbank an, in der die Wiederherstellungsdaten gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="4a86b-154">On the **Configure the location of the Recovery Database** page, specify the SQL Server instance name and the name of the database that stores the recovery data.</span></span>

11. <span data-ttu-id="4a86b-155">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="4a86b-155">Click **Next** to continue.</span></span>

12. <span data-ttu-id="4a86b-156">Geben Sie auf der Seite **Compliance-und Überwachungsberichte konfigurieren** die URL für die Berichterstellungsinstanz ein, die Sie auf dem anderen Server konfiguriert haben.</span><span class="sxs-lookup"><span data-stu-id="4a86b-156">On the **Configure the Compliance and Audit Reports** page, enter the URL for the reporting instance that you configured on the other server.</span></span> <span data-ttu-id="4a86b-157">Verwenden Sie die Schaltfläche **Testen** , um zu überprüfen, ob Sie die Website erreichen können.</span><span class="sxs-lookup"><span data-stu-id="4a86b-157">Use the **Test** button to verify that you can reach the site.</span></span>

13. <span data-ttu-id="4a86b-158">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="4a86b-158">Click **Next** to continue.</span></span>

14. <span data-ttu-id="4a86b-159">Geben Sie auf der Seite **Self-Service-Portal konfigurieren** die Portnummer, den Hostnamen, den Namen des virtuellen Verzeichnisses und den Installationspfad für das Self-Service-Portal ein.</span><span class="sxs-lookup"><span data-stu-id="4a86b-159">On the **Configure the Self-Service Portal** page, enter the port number, host name, virtual directory name, and installation path for the Self-Service Portal.</span></span>

    <span data-ttu-id="4a86b-160">**Hinweis**  Die von Ihnen angegebene Portnummer muss eine nicht verwendete Portnummer auf dem Verwaltungs-und Überwachungs Server sein, sofern Sie keinen eindeutigen Hostheadernamen angeben.</span><span class="sxs-lookup"><span data-stu-id="4a86b-160">**Note** The port number that you specify must be an unused port number on the Administration and Monitoring Server unless you specify a unique host header name.</span></span>

     

15. <span data-ttu-id="4a86b-161">Geben Sie auf der Seite **Verwaltungs-und Überwachungs Server konfigurieren** das gewünschte virtuelle Verzeichnis für die Helpdesk-Website an.</span><span class="sxs-lookup"><span data-stu-id="4a86b-161">On the **Configure the Administration and Monitoring Server** page, specify the desired virtual directory for the Help Desk website.</span></span>

16. <span data-ttu-id="4a86b-162">Geben Sie an, ob Microsoft Updates dazu beitragen soll, Ihren Computer zu schützen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="4a86b-162">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="4a86b-163">In diesem Schritt werden die automatischen Updates in Windows nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4a86b-163">This step does not turn on Automatic Updates in Windows.</span></span> <span data-ttu-id="4a86b-164">Wenn Sie zuvor entschieden haben, Microsoft Update für dieses Produkt oder ein anderes Produkt zu verwenden, wird die Seite Microsoft Update nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4a86b-164">If you previously chose to use Microsoft Update for this product or another product, the Microsoft Update page does not appear.</span></span>

17. <span data-ttu-id="4a86b-165">Überprüfen Sie auf der Seite **Installationszusammenfassung** die Features, die installiert werden sollen, und klicken Sie dann auf **Installieren** , um die Installation zu starten.</span><span class="sxs-lookup"><span data-stu-id="4a86b-165">On the **Installation Summary** page, review the features that will be installed, and then click **Install** to start the installation.</span></span>

18. <span data-ttu-id="4a86b-166">Um zu überprüfen, ob das Upgrade erfolgreich war, stellen Sie sicher, dass Sie jede Website von einem anderen Computer in der Domäne erreichen können.</span><span class="sxs-lookup"><span data-stu-id="4a86b-166">To validate that the upgrade was successful, verify that you can reach each site from another computer in the domain.</span></span>

## <span data-ttu-id="4a86b-167">Aktualisieren des MBAM-Clients auf Endbenutzercomputern</span><span class="sxs-lookup"><span data-stu-id="4a86b-167">Upgrading the MBAM Client on End-User Computers</span></span>


<span data-ttu-id="4a86b-168">Führen Sie **MbamClientSetup.exe** auf jedem Clientcomputer aus, um die Endbenutzercomputer auf den MBAM 2,0-Client zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4a86b-168">To upgrade end-user computers to the MBAM 2.0 Client, run **MbamClientSetup.exe** on each client computer.</span></span> <span data-ttu-id="4a86b-169">Das Installationsprogramm aktualisiert den Client automatisch auf den MBAM 2,0-Client.</span><span class="sxs-lookup"><span data-stu-id="4a86b-169">The installer automatically updates the Client to the MBAM 2.0 Client.</span></span> <span data-ttu-id="4a86b-170">Sie können den MBAM-Client über ein elektronisches Softwareverteilungssystem, Tools wie Active Directory-Domänendienste oder System Center Configuration Manager installieren.</span><span class="sxs-lookup"><span data-stu-id="4a86b-170">You can install the MBAM Client through an electronic software distribution system, tools such as Active Directory Domain Services or System Center Configuration Manager.</span></span>

<span data-ttu-id="4a86b-171">Gehen Sie wie folgt vor, um das Client Upgrade zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="4a86b-171">To validate the Client upgrade, do the following:</span></span>

1.  <span data-ttu-id="4a86b-172">Warten Sie, bis der konfigurierte Berichtszyklus endet, und starten Sie dann **SQL Server Management Studio** auf dem SQL Server-Computer.</span><span class="sxs-lookup"><span data-stu-id="4a86b-172">Wait until the configured reporting cycle is finished, and then start **SQL Server Management Studio** on the SQL Server computer.</span></span>

2.  <span data-ttu-id="4a86b-173">Starten Sie **SQL Server Management Studio**auf dem SQL Server-Computer.</span><span class="sxs-lookup"><span data-stu-id="4a86b-173">On the SQL Server computer, start **SQL Server Management Studio**.</span></span>

3.  <span data-ttu-id="4a86b-174">Überprüfen Sie, ob die Tabelle **RecoveryAndHardwareCore. Machines** eine Zeile enthält, die den Computernamen des Endbenutzers anzeigt.</span><span class="sxs-lookup"><span data-stu-id="4a86b-174">Verify that the **RecoveryAndHardwareCore.Machines** table contains a row that shows the end-user’s computer name.</span></span>

## <span data-ttu-id="4a86b-175">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="4a86b-175">Related topics</span></span>


[<span data-ttu-id="4a86b-176">Bereitstellen von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="4a86b-176">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)

 

 





