---
title: Auswerten von MBAM 2.0
description: Auswerten von MBAM 2.0
author: dansimp
ms.assetid: bfc77eec-0fd7-4fec-9c78-6870afa87152
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b7be883f44f5f09a904f619972ae3e7c35261d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810735"
---
# <span data-ttu-id="483c5-103">Auswerten von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="483c5-103">Evaluating MBAM 2.0</span></span>


<span data-ttu-id="483c5-104">Bevor Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) in einer Produktionsumgebung bereitstellen, sollten Sie Sie in einer Testumgebung auswerten.</span><span class="sxs-lookup"><span data-stu-id="483c5-104">Before deploying Microsoft BitLocker Administration and Monitoring (MBAM) into a production environment, you should evaluate it in a test environment.</span></span> <span data-ttu-id="483c5-105">Die Informationen in diesem Thema können verwendet werden, um die Microsoft BitLocker-Verwaltung und-Überwachung mit einer eigenständigen Topologie in einer einzigen Server Testumgebung zu Evaluierungszwecken einzurichten.</span><span class="sxs-lookup"><span data-stu-id="483c5-105">The information in this topic can be used to set up Microsoft BitLocker Administration and Monitoring with a Stand-alone topology in a single-server test environment for evaluation purposes only.</span></span> <span data-ttu-id="483c5-106">Eine Single-Server-Topologie wird für Produktionsumgebungen nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="483c5-106">A single-server topology is not recommended for production environments.</span></span>

<span data-ttu-id="483c5-107">Anweisungen zum Bereitstellen von MBAM in einer Testumgebung finden Sie unter so wird es [gemacht: Installieren und Konfigurieren von MBAM auf einem einzelnen Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="483c5-107">For instructions on deploying MBAM in a test environment, see [How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md).</span></span>

## <span data-ttu-id="483c5-108">Einrichten der Test Umgebung</span><span class="sxs-lookup"><span data-stu-id="483c5-108">Setting up the Test Environment</span></span>


<span data-ttu-id="483c5-109">Auch wenn Sie eine Nichtproduktionsinstanz von MBAM für die Auswertung in einer Testumgebung einrichten, sollten Sie dennoch überprüfen, ob Sie die Voraussetzungen und Hardware-und Softwareanforderungen erfüllt haben.</span><span class="sxs-lookup"><span data-stu-id="483c5-109">Even though you are setting up a non-production instance of MBAM to evaluate in a test environment, you should still verify that you have met the prerequisites and hardware and software requirements.</span></span> <span data-ttu-id="483c5-110">Bevor Sie mit der Installation beginnen, lesen Sie [MBAM 2,0-Bereitstellungsvoraussetzungen](mbam-20-deployment-prerequisites-mbam-2.md), [MBAM 2,0-unterstützte Konfigurationen](mbam-20-supported-configurations-mbam-2.md)und [Vorbereiten Ihrer Umgebung für MBAM 2,0](preparing-your-environment-for-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="483c5-110">Before you start the installation, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md), [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md), and [Preparing your Environment for MBAM 2.0](preparing-your-environment-for-mbam-20-mbam-2.md).</span></span>

### <span data-ttu-id="483c5-111">Planen einer MBAM-Evaluierungsbereitstellung</span><span class="sxs-lookup"><span data-stu-id="483c5-111">Plan for an MBAM Evaluation Deployment</span></span>

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
<th align="left"><span data-ttu-id="483c5-112">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="483c5-112">Task</span></span></th>
<th align="left"><span data-ttu-id="483c5-113">Verweise</span><span class="sxs-lookup"><span data-stu-id="483c5-113">References</span></span></th>
<th align="left"><span data-ttu-id="483c5-114">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="483c5-114">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="483c5-115">Lesen Sie die Informationen zu den ersten Schritten zu MBAM, um ein grundlegendes Verständnis des Produkts zu erhalten, bevor Sie mit der Bereitstellungsplanung beginnen.</span><span class="sxs-lookup"><span data-stu-id="483c5-115">Review the Getting Started information about MBAM to gain a basic understanding of the product before beginning deployment planning.</span></span></p></td>
<td align="left"><p><a href="getting-started-with-mbam-20-mbam-2.md" data-raw-source="[Getting Started with MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)"><span data-ttu-id="483c5-116">Erste Schritte mit MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="483c5-116">Getting Started with MBAM 2.0</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="483c5-117">Planen Sie die Voraussetzungen für MBAM 2,0-Bereitstellung, und bereiten Sie Ihre Computerumgebung vor.</span><span class="sxs-lookup"><span data-stu-id="483c5-117">Plan for MBAM 2.0 Deployment Prerequisites and prepare your computing environment.</span></span></p></td>
<td align="left"><p><a href="mbam-20-deployment-prerequisites-mbam-2.md" data-raw-source="[MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md)"><span data-ttu-id="483c5-118">Bereitstellungsvoraussetzungen für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="483c5-118">MBAM 2.0 Deployment Prerequisites</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="483c5-119">Planen und Konfigurieren von MBAM-Gruppenrichtlinienanforderungen</span><span class="sxs-lookup"><span data-stu-id="483c5-119">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)"><span data-ttu-id="483c5-120">Planen der Gruppenrichtlinienanforderungen für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="483c5-120">Planning for MBAM 2.0 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="483c5-121">Planen und erstellen Sie die erforderlichen ActiveDirectoryDomainServices-Sicherheitsgruppen, und planen Sie die MBAM-Mitgliedschaftsanforderungen für lokale Sicherheitsgruppen.</span><span class="sxs-lookup"><span data-stu-id="483c5-121">Plan for and create necessary ActiveDirectoryDomainServices security groups, and plan for MBAM local security group membership requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="483c5-122">Planen der Administratorrollen für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="483c5-122">Planning for MBAM 2.0 Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="483c5-123">Planen der Bereitstellung der MBAM-Server Features</span><span class="sxs-lookup"><span data-stu-id="483c5-123">Plan for deploying MBAM Server feature deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-server-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md)"><span data-ttu-id="483c5-124">Planen der Serverbereitstellung für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="483c5-124">Planning for MBAM 2.0 Server Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="483c5-125">Planen der Bereitstellung der MBAM-Client Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="483c5-125">Plan for deploying MBAM Client deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)"><span data-ttu-id="483c5-126">Planen der Clientbereitstellung für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="483c5-126">Planning for MBAM 2.0 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="483c5-127">Durchführen einer MBAM-Evaluierungsbereitstellung</span><span class="sxs-lookup"><span data-stu-id="483c5-127">Perform an MBAM Evaluation Deployment</span></span>

<span data-ttu-id="483c5-128">Nachdem Sie die erforderlichen Planungs-und Softwarevoraussetzungen installiert haben, um Ihre Computing-Umgebung für die MBAM-Installation vorzubereiten, können Sie mit der MBAM-Evaluierungsbereitstellung beginnen.</span><span class="sxs-lookup"><span data-stu-id="483c5-128">After completing the necessary planning and software prerequisite installations to prepare your computing environment for the MBAM installation, you can begin the MBAM evaluation deployment.</span></span>

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
<td align="left"><p><span data-ttu-id="483c5-129">Überprüfen Sie die MBAM-unterstützten Konfigurationsinformationen, um sicherzustellen, dass ausgewählte Client-und Server Computer für die MBAM-Feature-Installation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="483c5-129">Review the MBAM supported configurations information to make sure that selected client and server computers are supported for MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"><span data-ttu-id="483c5-130">Von MBAM 2.0 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="483c5-130">MBAM 2.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="483c5-131">Führen Sie MBAM-Setup aus, um MBAM-Server Features für Evaluierungszwecke auf einem einzelnen Server bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="483c5-131">Run MBAM Setup to deploy MBAM Server features on a single server for evaluation purposes.</span></span></p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md)"><span data-ttu-id="483c5-132">So installieren und Konfigurieren von MBAM auf einem Server</span><span class="sxs-lookup"><span data-stu-id="483c5-132">How to Install and Configure MBAM on a Single Server</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="483c5-133">Hinzufügen von ActiveDirectoryDomainServices-Sicherheitsgruppen, die Sie während der Planungsphase erstellt haben, zu den entsprechenden lokalen MBAM-Server Features für lokale Gruppen auf dem neuen MBAM-Server.</span><span class="sxs-lookup"><span data-stu-id="483c5-133">Add ActiveDirectoryDomainServices security groups, that you created during the planning phase, to the appropriate local MBAM Server feature local groups on the new MBAM Server.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="483c5-134">Planen von MBAM 2,0-Administratorrollen </a> und <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> Verwalten von MBAM-Administratorrollen</span><span class="sxs-lookup"><span data-stu-id="483c5-134">Planning for MBAM 2.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="483c5-135">Erstellen und Bereitstellen erforderlicher MBAM-Gruppenrichtlinienobjekte</span><span class="sxs-lookup"><span data-stu-id="483c5-135">Create and deploy required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)"><span data-ttu-id="483c5-136">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="483c5-136">Deploying MBAM 2.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="483c5-137">Bereitstellen der MBAM-Client Software.</span><span class="sxs-lookup"><span data-stu-id="483c5-137">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)"><span data-ttu-id="483c5-138">Bereitstellen des MBAM 2.0-Clients</span><span class="sxs-lookup"><span data-stu-id="483c5-138">Deploying the MBAM 2.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="483c5-139">Konfigurieren von Lab-Computern für die MBAM-Evaluierung</span><span class="sxs-lookup"><span data-stu-id="483c5-139">Configure Lab Computers for MBAM Evaluation</span></span>


<span data-ttu-id="483c5-140">Dieser Abschnitt enthält Informationen, die verwendet werden können, um die MBAM-Client Statusberichte zu beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="483c5-140">This section contains information that can be used to speed up the MBAM Client status reporting.</span></span> <span data-ttu-id="483c5-141">Diese Änderungen sollten jedoch nur zu Testzwecken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="483c5-141">However, these modifications should be used for testing purposes only.</span></span>

<span data-ttu-id="483c5-142">**Hinweis**  Die Informationen im folgenden Abschnitt beschreiben, wie Sie die Windows-Registrierung ändern.</span><span class="sxs-lookup"><span data-stu-id="483c5-142">**Note** The information in following section describes how to modify the Windows registry.</span></span> <span data-ttu-id="483c5-143">Wenn Sie den Registrierungs-Editor falsch verwenden, kann dies zu schwerwiegenden Problemen führen, die eine Neuinstallation von Windows erforderlich machen.</span><span class="sxs-lookup"><span data-stu-id="483c5-143">Using Registry Editor incorrectly can cause serious problems that may require you to reinstall Windows.</span></span> <span data-ttu-id="483c5-144">Microsoft kann nicht garantieren, dass Probleme, die sich aus der fehlerhaften Verwendung des Registrierungs-Editors ergeben, behoben werden können.</span><span class="sxs-lookup"><span data-stu-id="483c5-144">Microsoft cannot guarantee that problems resulting from the incorrect use of Registry Editor can be solved.</span></span> <span data-ttu-id="483c5-145">Verwenden Sie den Registrierungs-Editor auf eigenes Risiko.</span><span class="sxs-lookup"><span data-stu-id="483c5-145">Use Registry Editor at your own risk.</span></span>

 

### <span data-ttu-id="483c5-146">Ändern der Häufigkeitseinstellungen für MBAM-Client Status Berichte</span><span class="sxs-lookup"><span data-stu-id="483c5-146">Modify MBAM Client Status Reporting Frequency Settings</span></span>

<span data-ttu-id="483c5-147">Die MBAM-Client Aktivierungs-und Statusberichts Frequenzen weisen einen Mindestwert von 90 Minuten auf, wenn Sie mithilfe von Gruppenrichtlinien eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="483c5-147">The MBAM Client wakeup and status reporting frequencies have a minimum value of 90 minutes when they are set using Group Policy.</span></span> <span data-ttu-id="483c5-148">Sie können die Windows-Registrierung verwenden, um diese Frequenzen auf MBAM-Clientcomputern auf einen niedrigeren Wert zu ändern, um die Test Geschwindigkeit zu beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="483c5-148">You can use the Windows registry to change these frequencies to a lower value on MBAM client computers to help speed up testing.</span></span>

<span data-ttu-id="483c5-149">So ändern Sie die Häufigkeitseinstellungen für MBAM-Client Statusberichte:</span><span class="sxs-lookup"><span data-stu-id="483c5-149">To modify the MBAM Client status reporting frequency settings:</span></span>

1.  <span data-ttu-id="483c5-150">Verwenden Sie einen Registrierungs-Editor, um zu **HKLM\\Software\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement**zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="483c5-150">Use a registry editor to navigate to **HKLM\\Software\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement**.</span></span>

2.  <span data-ttu-id="483c5-151">Ändern Sie die Werte für **ClientWakeupFrequency** und **StatusReportingFrequency** in **1** als mindestens vom Client unterstützter Wert.</span><span class="sxs-lookup"><span data-stu-id="483c5-151">Change the values for **ClientWakeupFrequency** and **StatusReportingFrequency** to **1** as the minimum client-supported value.</span></span> <span data-ttu-id="483c5-152">Diese Änderung bewirkt, dass der MBAM-Client jede Minute meldet.</span><span class="sxs-lookup"><span data-stu-id="483c5-152">This change causes the MBAM Client to report every minute.</span></span>

3.  <span data-ttu-id="483c5-153">Starten Sie den **BitLocker-Verwaltungs Client Dienst**neu.</span><span class="sxs-lookup"><span data-stu-id="483c5-153">Restart **BitLocker Management Client Service**.</span></span>

<span data-ttu-id="483c5-154">**Hinweis**  Um Werte festzulegen, die so gering sind, müssen Sie Sie manuell in der Registrierung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="483c5-154">**Note** To set values that are this low, you must set them in the registry manually.</span></span>

 

### <span data-ttu-id="483c5-155">Ändern der Startverzögerung des MBAM-Client Diensts</span><span class="sxs-lookup"><span data-stu-id="483c5-155">Modify MBAM Client Service Startup Delay</span></span>

<span data-ttu-id="483c5-156">Zusätzlich zu den MBAM-Client Wakeup-und Statusberichts Frequenzen gibt es eine zufällige Verzögerung von bis zu 90 Minuten, wenn der MBAM-Client-Agent-Dienst auf Clientcomputern gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="483c5-156">In addition to the MBAM Client wakeup and status reporting frequencies, there is a random delay of up to 90 minutes when the MBAM Client agent service starts on client computers.</span></span> <span data-ttu-id="483c5-157">Wenn Sie die zufällige Verzögerung nicht möchten, erstellen Sie einen **DWORD** -Wert von **NoStartupDelay** unter **HKLM\\Software\\Microsoft\\MBAM**, legen Sie seinen Wert auf **1**, und starten Sie dann den **BitLocker-Verwaltungs Client Dienst**erneut.</span><span class="sxs-lookup"><span data-stu-id="483c5-157">If you do not want the random delay, create a **DWORD** value of **NoStartupDelay** under **HKLM\\Software\\Microsoft\\MBAM**, set its value to **1**, and then restart **BitLocker Management Client Service**.</span></span>

## <span data-ttu-id="483c5-158">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="483c5-158">Related topics</span></span>


[<span data-ttu-id="483c5-159">Erste Schritte mit MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="483c5-159">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)

 

 





