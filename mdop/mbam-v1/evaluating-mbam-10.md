---
title: Auswerten von MBAM 1.0
description: Auswerten von MBAM 1.0
author: dansimp
ms.assetid: a1e2b674-eda9-4e1c-9b4c-e748470c71f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f09b06af52f5738fd50bfe727987b760d98552d9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811044"
---
# <span data-ttu-id="bdaae-103">Auswerten von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bdaae-103">Evaluating MBAM 1.0</span></span>


<span data-ttu-id="bdaae-104">Bevor Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) in einer Produktionsumgebung bereitstellen, sollten Sie Sie in einer Lab-Umgebung auswerten.</span><span class="sxs-lookup"><span data-stu-id="bdaae-104">Before you deploy Microsoft BitLocker Administration and Monitoring (MBAM) into a production environment, you should evaluate it in a lab environment.</span></span> <span data-ttu-id="bdaae-105">Sie können die Informationen in diesem Thema verwenden, um MBAM in einer einzigen Server-Lab-Umgebung zu Evaluierungszwecken einzurichten.</span><span class="sxs-lookup"><span data-stu-id="bdaae-105">You can use the information in this topic to set up MBAM in a single server lab environment for evaluation purposes only.</span></span>

<span data-ttu-id="bdaae-106">Während die tatsächlichen Bereitstellungsschritte dem Szenario ähnlich sind, das unter [Anleitung zum Installieren und Konfigurieren von MBAM auf einem einzelnen Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)beschrieben wird, enthält dieses Thema zusätzliche Informationen, mit denen Sie in kürzester Zeit eine MBAM-Evaluierungsumgebung einrichten können.</span><span class="sxs-lookup"><span data-stu-id="bdaae-106">While the actual deployment steps are very similar to the scenario that is described in [How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md), this topic contains additional information to enable you to set up an MBAM evaluation environment in the least amount of time.</span></span>

## <span data-ttu-id="bdaae-107">Einrichten der Lab-Umgebung</span><span class="sxs-lookup"><span data-stu-id="bdaae-107">Set up the Lab Environment</span></span>


<span data-ttu-id="bdaae-108">Auch wenn Sie eine Nichtproduktionsinstanz von MBAM für die Auswertung in einer Lab-Umgebung einrichten, sollten Sie dennoch sicherstellen, dass Sie die Voraussetzungen für die Bereitstellung sowie die Hardware-und Softwareanforderungen erfüllt haben.</span><span class="sxs-lookup"><span data-stu-id="bdaae-108">Even when you set up a non-production instance of MBAM to evaluate in a lab environment, you should still verify that you have met the deployment prerequisites and the hardware and software requirements.</span></span> <span data-ttu-id="bdaae-109">Weitere Informationen finden Sie unter [Voraussetzungen für die MBAM 1,0-Bereitstellung](mbam-10-deployment-prerequisites.md) und [unterstützte MBAM 1,0-Konfigurationen](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="bdaae-109">For more information, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span> <span data-ttu-id="bdaae-110">Sie sollten auch überprüfen, [wie Sie Ihre Umgebung für MBAM 1,0 vorbereiten](preparing-your-environment-for-mbam-10.md) , bevor Sie mit der MBAM-Evaluierungsbereitstellung beginnen.</span><span class="sxs-lookup"><span data-stu-id="bdaae-110">You should also review [Preparing your Environment for MBAM 1.0](preparing-your-environment-for-mbam-10.md) before you begin the MBAM evaluation deployment.</span></span>

### <span data-ttu-id="bdaae-111">Planen einer MBAM-Evaluierungsbereitstellung</span><span class="sxs-lookup"><span data-stu-id="bdaae-111">Plan for an MBAM Evaluation Deployment</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="bdaae-112">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="bdaae-112">Task</span></span></th>
<th align="left"><span data-ttu-id="bdaae-113">Verweise</span><span class="sxs-lookup"><span data-stu-id="bdaae-113">References</span></span></th>
<th align="left"><span data-ttu-id="bdaae-114">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="bdaae-114">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bdaae-115">Lesen Sie die Informationen zu den ersten Schritten zu MBAM, um ein grundlegendes Verständnis des Produkts zu erhalten, bevor Sie mit der Bereitstellungsplanung beginnen.</span><span class="sxs-lookup"><span data-stu-id="bdaae-115">Review the Getting Started information about MBAM to gain a basic understanding of the product before you begin your deployment planning.</span></span></p></td>
<td align="left"><p><a href="getting-started-with-mbam-10.md" data-raw-source="[Getting Started with MBAM 1.0](getting-started-with-mbam-10.md)"><span data-ttu-id="bdaae-116">Erste Schritte mit MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bdaae-116">Getting Started with MBAM 1.0</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p></p>
<p><span data-ttu-id="bdaae-117">Bereiten Sie Ihre Computerumgebung für die MBAM-Installation vor.</span><span class="sxs-lookup"><span data-stu-id="bdaae-117">Prepare your computing environment for the MBAM installation.</span></span> <span data-ttu-id="bdaae-118">Dazu müssen Sie die transparente Datenverschlüsselung (transparent Data Encryption, DSA) auf den SQL Server-Instanzen aktivieren, die MBAM-Datenbanken hosten werden.</span><span class="sxs-lookup"><span data-stu-id="bdaae-118">To do so, you must enable the Transparent Data Encryption (TDE) on the SQL Server instances that will host MBAM databases.</span></span> <span data-ttu-id="bdaae-119">Zum Aktivieren von DSA in ihrer Lab-Umgebung können Sie eine SQL-Datei erstellen, die für die Master-Datenbank ausgeführt wird, die auf der Instanz von SQL Server gehostet wird, die von MBAM verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bdaae-119">To enable TDE in your lab environment, you can create a .sql file to run against the master database that is hosted on the instance of the SQL Server that MBAM will use.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="bdaae-120">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="bdaae-120">Note</span></span></strong><br/><p><span data-ttu-id="bdaae-121">Mit dem folgenden Beispiel können Sie eine SQL-Datei für Ihre Lab-Umgebung erstellen, um DSA schnell auf der SQL Server-Instanz zu aktivieren, die die MBAM-Datenbanken hosten soll.</span><span class="sxs-lookup"><span data-stu-id="bdaae-121">You can use the following example to create a .sql file for your lab environment to quickly enable TDE on the SQL Server instance that will host the MBAM databases.</span></span> <span data-ttu-id="bdaae-122">Mit diesen SQL Server-Befehlen wird DSA mithilfe eines lokal signierten SQL Server-Zertifikats aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bdaae-122">These SQL Server commands will enable TDE by using a locally signed SQL Server certificate.</span></span> <span data-ttu-id="bdaae-123">Stellen Sie sicher, dass das DSA-Zertifikat und der zugehörige Verschlüsselungsschlüssel auf dem Beispiel lokalen Sicherungspfad von C:\backup gesichert werden <em> </em> .</span><span class="sxs-lookup"><span data-stu-id="bdaae-123">Make sure to back up the TDE certificate and its associated encryption key to the example local backup path of <em>C:\Backup</em>.</span></span> <span data-ttu-id="bdaae-124">Das DSA-Zertifikat und der Schlüssel sind erforderlich, wenn Sie die Datenbank wiederherstellen oder das Zertifikat und den Schlüssel auf einen anderen Server verschieben, auf dem die DSA-Verschlüsselung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bdaae-124">The TDE certificate and key are required when recover the database or move the certificate and key to another server that has TDE encryption in place.</span></span></p>
</div>
<div>

</div>
<pre class="syntax" space="preserve"><code>USE master;
GO
CREATE MASTER KEY ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;;
GO
CREATE CERTIFICATE tdeCert WITH SUBJECT = &#39;TDE Certificate&#39;;
GO
BACKUP CERTIFICATE tdeCert TO FILE = &#39;C:\Backup\TDECertificate.cer&#39;
   WITH PRIVATE KEY (
         FILE = &#39;C:\Backup\TDECertificateKey.pvk&#39;,
         ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;);
GO</code></pre></td>
<td align="left"><p><a href="mbam-10-deployment-prerequisites.md" data-raw-source="[MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md)"><span data-ttu-id="bdaae-125">Bereitstellungsvoraussetzungen für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bdaae-125">MBAM 1.0 Deployment Prerequisites</span></span></a></p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=269703" data-raw-source="[Database Encryption in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703)"><span data-ttu-id="bdaae-126">Datenbankverschlüsselung in SQL Server 2008 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="bdaae-126">Database Encryption in SQL Server 2008 Enterprise Edition</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bdaae-127">Planen und Konfigurieren von MBAM-Gruppenrichtlinienanforderungen</span><span class="sxs-lookup"><span data-stu-id="bdaae-127">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-group-policy-requirements.md" data-raw-source="[Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md)"><span data-ttu-id="bdaae-128">Planen der Gruppenrichtlinienanforderungen für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bdaae-128">Planning for MBAM 1.0 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bdaae-129">Planen und erstellen Sie die erforderlichen Active Directory-Domänendienste-Sicherheitsgruppen, und planen Sie die Mitgliedschaftsanforderungen für MBAM Local Security Group.</span><span class="sxs-lookup"><span data-stu-id="bdaae-129">Plan for and create the necessary Active Directory Domain Services security groups and plan for MBAM local security group membership requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)"><span data-ttu-id="bdaae-130">Planen der Administratorrollen für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bdaae-130">Planning for MBAM 1.0 Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bdaae-131">Planen der Bereitstellung von MBAM Server Features</span><span class="sxs-lookup"><span data-stu-id="bdaae-131">Plan for MBAM Server feature deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-server-deployment.md" data-raw-source="[Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md)"><span data-ttu-id="bdaae-132">Planen der Serverbereitstellung für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bdaae-132">Planning for MBAM 1.0 Server Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bdaae-133">Planen der MBAM-Client Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="bdaae-133">Plan for MBAM Client deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-client-deployment.md" data-raw-source="[Planning for MBAM 1.0 Client Deployment](planning-for-mbam-10-client-deployment.md)"><span data-ttu-id="bdaae-134">Planen der Clientbereitstellung für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bdaae-134">Planning for MBAM 1.0 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="bdaae-135">Durchführen einer MBAM-Evaluierungsbereitstellung</span><span class="sxs-lookup"><span data-stu-id="bdaae-135">Perform an MBAM Evaluation Deployment</span></span>

<span data-ttu-id="bdaae-136">Nachdem Sie die erforderlichen Planungs-und Softwarevoraussetzungen installiert haben, um Ihre Computerumgebung für eine MBAM-Installation vorzubereiten, können Sie mit der MBAM-Evaluierungsbereitstellung beginnen.</span><span class="sxs-lookup"><span data-stu-id="bdaae-136">After you complete the necessary planning and software prerequisite installations to prepare your computing environment for an MBAM installation, you can begin the MBAM evaluation deployment.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bdaae-137">Überprüfen Sie die MBAM-unterstützten Konfigurationsinformationen, um sicherzustellen, dass die ausgewählten Client-und Server Computer für die MBAM-Feature-Installation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="bdaae-137">Review the MBAM supported configurations information to make sure that the selected client and server computers are supported for the MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)"><span data-ttu-id="bdaae-138">Von MBAM 1.0 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="bdaae-138">MBAM 1.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bdaae-139">Führen Sie MBAM-Setup aus, um MBAM-Server Features für Evaluierungszwecke auf einem einzelnen Server bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="bdaae-139">Run MBAM Setup to deploy MBAM Server features on a single server for evaluation purposes.</span></span></p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)"><span data-ttu-id="bdaae-140">So installieren und Konfigurieren von MBAM auf einem Server</span><span class="sxs-lookup"><span data-stu-id="bdaae-140">How to Install and Configure MBAM on a Single Server</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bdaae-141">Fügen Sie die Sicherheitsgruppen für Active Directory-Domänendienste, die Sie während der Planungsphase erstellt haben, zu den entsprechenden lokalen MBAM-Server Feature-lokalen Gruppen auf dem neuen MBAM-Server hinzu.</span><span class="sxs-lookup"><span data-stu-id="bdaae-141">Add the Active Directory Domain Services security groups that you created during the planning phase to the appropriate local MBAM Server feature local groups on the new MBAM server.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)"><span data-ttu-id="bdaae-142">Planen von MBAM 1,0-Administratorrollen </a> und <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> Verwalten von MBAM-Administratorrollen</span><span class="sxs-lookup"><span data-stu-id="bdaae-142">Planning for MBAM 1.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bdaae-143">Erstellen und Bereitstellen der erforderlichen MBAM-Gruppenrichtlinienobjekte</span><span class="sxs-lookup"><span data-stu-id="bdaae-143">Create and deploy the required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)"><span data-ttu-id="bdaae-144">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bdaae-144">Deploying MBAM 1.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bdaae-145">Bereitstellen der MBAM-Client Software.</span><span class="sxs-lookup"><span data-stu-id="bdaae-145">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)"><span data-ttu-id="bdaae-146">Bereitstellen des MBAM 1.0-Clients</span><span class="sxs-lookup"><span data-stu-id="bdaae-146">Deploying the MBAM 1.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="bdaae-147">Konfigurieren von Lab-Computern für die MBAM-Evaluierung</span><span class="sxs-lookup"><span data-stu-id="bdaae-147">Configure Lab Computers for MBAM Evaluation</span></span>


<span data-ttu-id="bdaae-148">Mit dem Registrierungs-Editor können Sie die Häufigkeitseinstellungen für den MBAM-Client Statusbericht ändern.</span><span class="sxs-lookup"><span data-stu-id="bdaae-148">You can change the frequency settings on the MBAM Client status reporting by using Registry Editor.</span></span> <span data-ttu-id="bdaae-149">Diese Änderungen sollten jedoch nur zu Testzwecken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bdaae-149">However, these modifications should be used for testing purposes only.</span></span>

**<span data-ttu-id="bdaae-150">Warnung</span><span class="sxs-lookup"><span data-stu-id="bdaae-150">Warning</span></span>**  
<span data-ttu-id="bdaae-151">In diesem Thema wird beschrieben, wie Sie die Windows-Registrierung mit dem Registrierungs-Editor ändern.</span><span class="sxs-lookup"><span data-stu-id="bdaae-151">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="bdaae-152">Wenn Sie die Windows-Registrierung falsch ändern, können Sie zu schwerwiegenden Problemen führen, bei denen Sie möglicherweise eine Neuinstallation von Windows erforderlich machen.</span><span class="sxs-lookup"><span data-stu-id="bdaae-152">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="bdaae-153">Bevor Sie die Registrierung ändern, sollten Sie eine Sicherungskopie der Registrierungsdateien (System. dat und User. dat) erstellen.</span><span class="sxs-lookup"><span data-stu-id="bdaae-153">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="bdaae-154">Microsoft kann nicht garantieren, dass die Probleme, die beim Ändern der Registrierung auftreten, behoben werden können.</span><span class="sxs-lookup"><span data-stu-id="bdaae-154">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="bdaae-155">Ändern Sie die Registrierung auf Ihr eigenes Risiko.</span><span class="sxs-lookup"><span data-stu-id="bdaae-155">Change the registry at your own risk.</span></span>



### <a href="" id="modify-the-frequency-settings-on-mbam-client-status-reporting-"></a><span data-ttu-id="bdaae-156">Ändern der Häufigkeitseinstellungen für MBAM-Client Status Berichte</span><span class="sxs-lookup"><span data-stu-id="bdaae-156">Modify the Frequency Settings on MBAM Client Status Reporting</span></span>

<span data-ttu-id="bdaae-157">Die MBAM-Client Aktivierungs-und Statusberichts Frequenzen weisen einen Mindestwert von 90 Minuten auf, wenn Sie für die Verwendung von Gruppenrichtlinien eingestellt sind.</span><span class="sxs-lookup"><span data-stu-id="bdaae-157">The MBAM Client wakeup and status reporting frequencies have a minimum value of 90 minutes when they are set to use Group Policy.</span></span> <span data-ttu-id="bdaae-158">Sie können diese Frequenzen auf MBAM-Clientcomputern ändern, indem Sie die Windows-Registrierung auf niedrigere Werte bearbeiten, wodurch die Tests beschleunigt werden.</span><span class="sxs-lookup"><span data-stu-id="bdaae-158">You can change these frequencies on MBAM client computers by editing the Windows registry to lower values, which will help speed up the testing.</span></span> <span data-ttu-id="bdaae-159">Wenn Sie die Häufigkeitseinstellungen für MBAM-Client Statusberichte ändern möchten, verwenden Sie einen Registrierungs-Editor, um zu **HKLM\\Software\\Policies\\FVE\\MDOPBitLockerManagement**zu navigieren, ändern Sie die Werte für **ClientWakeupFrequency** und **StatusReportingFrequency** in **1** als Mindestwert für vom Client unterstützt, und starten Sie dann den BitLocker-Verwaltungs Client Dienst erneut.</span><span class="sxs-lookup"><span data-stu-id="bdaae-159">To modify the frequency settings on MBAM Client status reporting, use a registry editor to navigate to **HKLM\\Software\\Policies\\FVE\\MDOPBitLockerManagement**, change the values for **ClientWakeupFrequency** and **StatusReportingFrequency** to **1** as the minimum client supported value, and then restart BitLocker Management Client Service.</span></span> <span data-ttu-id="bdaae-160">Wenn Sie diese Änderung vornehmen, wird der MBAM-Client jede Minute darüber berichten.</span><span class="sxs-lookup"><span data-stu-id="bdaae-160">When you make this change, the MBAM Client will report every minute.</span></span> <span data-ttu-id="bdaae-161">Sie können diese Werte nur dann einstellen, wenn Sie dies manuell in der Registrierung tun.</span><span class="sxs-lookup"><span data-stu-id="bdaae-161">You can set values this low only when you do so manually in the registry.</span></span>

### <a href="" id="modify-the-startup-delay-on-mbam-client-service-"></a><span data-ttu-id="bdaae-162">Ändern der Startverzögerung für den MBAM-Client Dienst</span><span class="sxs-lookup"><span data-stu-id="bdaae-162">Modify the Startup Delay on MBAM Client Service</span></span>

<span data-ttu-id="bdaae-163">Zusätzlich zu den MBAM-Client Wakeup-und Statusberichts Frequenzen gibt es eine zufällige Verzögerung von bis zu 90 Minuten, wenn der MBAM-Client-Agent-Dienst auf Clientcomputern gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="bdaae-163">In addition to the MBAM Client wakeup and status reporting frequencies, there is a random delay of up to 90 minutes when the MBAM Client agent service starts on client computers.</span></span> <span data-ttu-id="bdaae-164">Wenn Sie die zufällige Verzögerung nicht möchten, erstellen Sie einen **DWORD** -Wert von **NoStartupDelay** unter **HKLM\\Software\\Microsoft\\MBAM**, legen Sie seinen Wert auf **1**, und starten Sie dann den BitLocker-Verwaltungs Client Dienst erneut.</span><span class="sxs-lookup"><span data-stu-id="bdaae-164">If you do not want the random delay, create a **DWORD** value of **NoStartupDelay** under **HKLM\\Software\\Microsoft\\MBAM**, set its value to **1**, and then restart BitLocker Management Client Service.</span></span>

## <span data-ttu-id="bdaae-165">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="bdaae-165">Related topics</span></span>


[<span data-ttu-id="bdaae-166">Erste Schritte mit MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bdaae-166">Getting Started with MBAM 1.0</span></span>](getting-started-with-mbam-10.md)









