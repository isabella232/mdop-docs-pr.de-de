---
title: Auswerten von MBAM 2.5 in einer Testumgebung
description: Auswerten von MBAM 2.5 in einer Testumgebung
author: dansimp
ms.assetid: 72959b7a-e55f-4797-91b3-5be23c8c2844
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d7ba8a62f5ddecf85fe56e04fc16a6bae374ba9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809784"
---
# <span data-ttu-id="5b750-103">Auswerten von MBAM 2.5 in einer Testumgebung</span><span class="sxs-lookup"><span data-stu-id="5b750-103">Evaluating MBAM 2.5 in a Test Environment</span></span>


<span data-ttu-id="5b750-104">In diesem Thema wird beschrieben, wie Sie eine Testumgebung einrichten können, um die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 in der eigenständigen oder System Center Configuration Manager-Integrations Topologie auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="5b750-104">This topic describes how you can set up a test environment to evaluate Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in the Stand-alone or System Center Configuration Manager Integration topology.</span></span>

## <span data-ttu-id="5b750-105">Auswerten von MBAM 2,5 mithilfe der eigenständigen Topologie</span><span class="sxs-lookup"><span data-stu-id="5b750-105">Evaluating MBAM 2.5 by using the Stand-alone topology</span></span>


<span data-ttu-id="5b750-106">Zum Auswerten von MBAM mithilfe der eigenständigen Topologie verwenden Sie die Informationen in den folgenden Tabellen, um die MBAM-Server Software zu installieren, und konfigurieren Sie dann die MBAM-Server Features in Ihrer Testumgebung.</span><span class="sxs-lookup"><span data-stu-id="5b750-106">To evaluate MBAM by using the Stand-alone topology, use the information in the following tables to install the MBAM Server software, and then configure the MBAM Server features in your test environment.</span></span>

**<span data-ttu-id="5b750-107">So evaluieren Sie MBAM 2,5 mithilfe der eigenständigen Topologie</span><span class="sxs-lookup"><span data-stu-id="5b750-107">To evaluate MBAM 2.5 by using the Stand-alone topology</span></span>**

1. <span data-ttu-id="5b750-108">Bevor Sie MBAM installieren, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="5b750-108">Before installing MBAM, do the following:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="5b750-109">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="5b750-109">Task</span></span></th>
   <th align="left"><span data-ttu-id="5b750-110">Wo erhalte ich Anweisungen?</span><span class="sxs-lookup"><span data-stu-id="5b750-110">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5b750-111">Stellen Sie sicher, dass Sie alle erforderlichen Software installiert haben.</span><span class="sxs-lookup"><span data-stu-id="5b750-111">Ensure that you have installed all of the prerequisite software.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="5b750-112">MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien</span><span class="sxs-lookup"><span data-stu-id="5b750-112">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="5b750-113">Überprüfen Sie die erforderlichen Hardware-, RAM-und anderen Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5b750-113">Check the required hardware, RAM, and other specifications.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="5b750-114">Von MBAM 2.5 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="5b750-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5b750-115">Überprüfen Sie die Voraussetzungen für die Verwendung von Windows PowerShell, wenn Sie die Cmdlets zum Konfigurieren von MBAM verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="5b750-115">Review the prerequisites for using Windows PowerShell if you plan to use the cmdlets to configure MBAM.</span></span></p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="5b750-116">Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5b750-116">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="5b750-117">Installieren Sie die MBAM-Server Software, und konfigurieren Sie dann die gewünschten Features.</span><span class="sxs-lookup"><span data-stu-id="5b750-117">Install the MBAM Server software, and then configure the features you want.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="5b750-118">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="5b750-118">Task</span></span></th>
   <th align="left"><span data-ttu-id="5b750-119">Wo erhalte ich Anweisungen?</span><span class="sxs-lookup"><span data-stu-id="5b750-119">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5b750-120">Installieren Sie die MBAM-Server Software auf jedem Server, auf dem Sie ein MBAM-Server Feature konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="5b750-120">Install the MBAM Server software on each server where you want to configure an MBAM Server feature.</span></span></p></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="5b750-121">Installieren der MBAM 2.5-Serversoftware</span><span class="sxs-lookup"><span data-stu-id="5b750-121">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="5b750-122">Konfigurieren Sie die Datenbank für Compliance und Audit sowie die Wiederherstellungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="5b750-122">Configure the Compliance and Audit Database and the Recovery Database.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="5b750-123">So konfigurieren Sie die MBAM 2.5-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="5b750-123">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5b750-124">Konfigurieren Sie das Feature Berichte.</span><span class="sxs-lookup"><span data-stu-id="5b750-124">Configure the Reports feature.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="5b750-125">So konfigurieren Sie die MBAM 2.5-Berichte</span><span class="sxs-lookup"><span data-stu-id="5b750-125">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="5b750-126">Konfigurieren Sie die Webanwendungen.</span><span class="sxs-lookup"><span data-stu-id="5b750-126">Configure the web applications.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="5b750-127">So konfigurieren Sie die MBAM 2.5-Webanwendungen</span><span class="sxs-lookup"><span data-stu-id="5b750-127">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="5b750-128">Gehen Sie auf einem Clientcomputer wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="5b750-128">On a client computer, do the following:</span></span>

   1.  <span data-ttu-id="5b750-129">Installieren Sie den MBAM-Client auf einem Clientcomputer.</span><span class="sxs-lookup"><span data-stu-id="5b750-129">Install the MBAM Client on a client computer.</span></span>

   2.  <span data-ttu-id="5b750-130">Wenden Sie die MBAM-Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) auf den Computer an.</span><span class="sxs-lookup"><span data-stu-id="5b750-130">Apply the MBAM Group Policy Objects (GPOs) to the computer.</span></span>

   3.  <span data-ttu-id="5b750-131">Legen Sie die folgenden Registrierungsschlüssel fest, um zu erzwingen, dass der MBAM-Client schneller und in regelmäßigen Abständen aktiviert wird:</span><span class="sxs-lookup"><span data-stu-id="5b750-131">Set the following registry keys to force the MBAM Client to wake up faster and at regular intervals:</span></span>

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **<span data-ttu-id="5b750-132">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="5b750-132">Note</span></span>**  
       <span data-ttu-id="5b750-133">Da diese Tasten den MBAM-Client pro Minute reaktivieren, empfehlen wir, diese Registrierungsschlüsseleinstellungen nur in einer Testumgebung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5b750-133">Because these keys wake up the MBAM Client every minute, we recommend that you use these registry key settings only in a test environment.</span></span>



   4.  <span data-ttu-id="5b750-134">Starten Sie den **BitLocker-Verwaltungs Client Dienst**erneut.</span><span class="sxs-lookup"><span data-stu-id="5b750-134">Restart the **BitLocker Management Client Service**.</span></span>

## <span data-ttu-id="5b750-135">Auswerten von MBAM 2,5 mithilfe der Configuration Manager-Integrations Topologie von System Center 2012</span><span class="sxs-lookup"><span data-stu-id="5b750-135">Evaluating MBAM 2.5 by using the System Center 2012 Configuration Manager Integration topology</span></span>


<span data-ttu-id="5b750-136">Zum Auswerten von MBAM mithilfe der Configuration Manager-Integrations Topologie verwenden Sie die Informationen in den folgenden Tabellen, um die MBAM-Server Software zu installieren, und konfigurieren Sie dann die MBAM-Server Features in Ihrer Testumgebung.</span><span class="sxs-lookup"><span data-stu-id="5b750-136">To evaluate MBAM by using the Configuration Manager Integration topology, use the information in the following tables to install the MBAM Server software, and then configure the MBAM Server features in your test environment.</span></span> <span data-ttu-id="5b750-137">Nachdem Sie den MBAM-Client auf einem Clientcomputer installiert haben, führen Sie weitere Schritte durch, um zu erzwingen, dass der MBAM-Client den Status des Computers an MBAM schneller meldet.</span><span class="sxs-lookup"><span data-stu-id="5b750-137">After installing the MBAM Client on a client computer, you will complete additional steps to force the MBAM Client to report the computer’s status to MBAM more quickly.</span></span>

**<span data-ttu-id="5b750-138">So evaluieren Sie MBAM 2,5 mithilfe der Configuration Manager-Integrations Topologie von System Center 2012</span><span class="sxs-lookup"><span data-stu-id="5b750-138">To evaluate MBAM 2.5 by using the System Center 2012 Configuration Manager Integration topology</span></span>**

1. <span data-ttu-id="5b750-139">Überprüfen Sie vor der Installation von MBAM die erforderliche Software und die unterstützte Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5b750-139">Before installing MBAM, review the prerequisite software and supported configuration.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="5b750-140">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="5b750-140">Task</span></span></th>
   <th align="left"><span data-ttu-id="5b750-141">Wo erhalte ich Anweisungen?</span><span class="sxs-lookup"><span data-stu-id="5b750-141">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5b750-142">Stellen Sie sicher, dass Sie alle erforderlichen Software installiert haben.</span><span class="sxs-lookup"><span data-stu-id="5b750-142">Ensure that you have installed all of the prerequisite software.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="5b750-143">MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien</span><span class="sxs-lookup"><span data-stu-id="5b750-143">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="5b750-144">MBAM 2.5-Servervoraussetzungen, die nur für die Configuration Manager-Integrationstopologie gelten</span><span class="sxs-lookup"><span data-stu-id="5b750-144">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="5b750-145">Überprüfen Sie die erforderlichen Hardware-, RAM-und anderen Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5b750-145">Check the required hardware, RAM, and other specifications.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="5b750-146">Von MBAM 2.5 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="5b750-146">MBAM 2.5 Supported Configurations</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5b750-147">Überprüfen Sie die Voraussetzungen für die Verwendung von Windows PowerShell, wenn Sie die Cmdlets zum Konfigurieren von MBAM verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="5b750-147">Review the prerequisites for using Windows PowerShell if you plan to use the cmdlets to configure MBAM.</span></span></p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="5b750-148">Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5b750-148">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="5b750-149">Erstellen oder bearbeiten Sie die MOF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="5b750-149">Create or edit the .mof files.</span></span></p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)"><span data-ttu-id="5b750-150">Bearbeiten der Datei „Configuration.mof“</span><span class="sxs-lookup"><span data-stu-id="5b750-150">Edit the Configuration.mof File</span></span></a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)"><span data-ttu-id="5b750-151">Erstellen oder Bearbeiten der Datei „Sms_def.mof“</span><span class="sxs-lookup"><span data-stu-id="5b750-151">Create or Edit the Sms_def.mof File</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="5b750-152">Installieren Sie die MBAM-Server Software, und konfigurieren Sie dann die gewünschten Features.</span><span class="sxs-lookup"><span data-stu-id="5b750-152">Install the MBAM Server software, and then configure the features you want.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="5b750-153">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="5b750-153">Task</span></span></th>
   <th align="left"><span data-ttu-id="5b750-154">Wo erhalte ich Anweisungen?</span><span class="sxs-lookup"><span data-stu-id="5b750-154">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5b750-155">Installieren Sie die MBAM-Server Software auf jedem Server, auf dem Sie ein MBAM-Server Feature konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="5b750-155">Install the MBAM Server software on each server where you want to configure an MBAM Server feature.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="5b750-156">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="5b750-156">Note</span></span></strong><br/><p><span data-ttu-id="5b750-157">Sie können die Datenbanken auf einem SQL Server-Remotecomputer mit Windows PowerShell oder einem exportierten Data-tier Application (DAC)-Paket installieren.</span><span class="sxs-lookup"><span data-stu-id="5b750-157">You can install the databases to a remote SQL Server computer by using Windows PowerShell or an exported data-tier application (DAC) package.</span></span> <span data-ttu-id="5b750-158">Weitere Informationen zu DAC-Paketen finden Sie unter <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> Datenebenen-Anwendungen </a> .</span><span class="sxs-lookup"><span data-stu-id="5b750-158">For more information about DAC packages, see <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)">Data-tier Applications</a>.</span></span></p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="5b750-159">Installieren der MBAM 2.5-Serversoftware</span><span class="sxs-lookup"><span data-stu-id="5b750-159">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="5b750-160">Konfigurieren Sie die Datenbank für Compliance und Audit sowie die Wiederherstellungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="5b750-160">Configure the Compliance and Audit Database and the Recovery Database.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="5b750-161">So konfigurieren Sie die MBAM 2.5-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="5b750-161">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5b750-162">Konfigurieren Sie das Feature Berichte.</span><span class="sxs-lookup"><span data-stu-id="5b750-162">Configure the Reports feature.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="5b750-163">So konfigurieren Sie die MBAM 2.5-Berichte</span><span class="sxs-lookup"><span data-stu-id="5b750-163">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="5b750-164">Konfigurieren Sie die Webanwendungen.</span><span class="sxs-lookup"><span data-stu-id="5b750-164">Configure the web applications.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="5b750-165">So konfigurieren Sie die MBAM 2.5-Webanwendungen</span><span class="sxs-lookup"><span data-stu-id="5b750-165">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5b750-166">Konfigurieren Sie den System Center-Konfigurations-Manager, um die Configuration Manager-Objekte zu installieren.</span><span class="sxs-lookup"><span data-stu-id="5b750-166">Configure the System Center Configuration Manager to install the Configuration Manager objects.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)"><span data-ttu-id="5b750-167">So konfigurieren Sie die Integration von MBAM 2.5 in System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="5b750-167">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="5b750-168">Gehen Sie auf einem Clientcomputer wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="5b750-168">On a client computer, do the following:</span></span>

   1.  <span data-ttu-id="5b750-169">Installieren Sie den MBAM-Client und den Configuration Manager-Client auf einem Clientcomputer.</span><span class="sxs-lookup"><span data-stu-id="5b750-169">Install the MBAM Client and the Configuration Manager Client on a client computer.</span></span>

   2.  <span data-ttu-id="5b750-170">Wenden Sie die MBAM-Gruppenrichtlinienobjekte auf den Computer an.</span><span class="sxs-lookup"><span data-stu-id="5b750-170">Apply the MBAM Group Policy Objects to the computer.</span></span>

   3.  <span data-ttu-id="5b750-171">Legen Sie die folgenden Registrierungsschlüssel fest, um zu erzwingen, dass der MBAM-Client schneller und in regelmäßigen Abständen aktiviert wird:</span><span class="sxs-lookup"><span data-stu-id="5b750-171">Set the following registry keys to force the MBAM Client to wake up faster and at regular intervals:</span></span>

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **<span data-ttu-id="5b750-172">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="5b750-172">Note</span></span>**  
       <span data-ttu-id="5b750-173">Da diese Tasten den MBAM-Client pro Minute reaktivieren, empfehlen wir, diese Registrierungsschlüsseleinstellungen nur in einer Testumgebung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5b750-173">Because these keys wake up the MBAM Client every minute, we recommend that you use these registry key settings only in a test environment.</span></span>



   4.  <span data-ttu-id="5b750-174">Starten Sie den **BitLocker-Verwaltungs Client Dienst**erneut.</span><span class="sxs-lookup"><span data-stu-id="5b750-174">Restart the **BitLocker Management Client Service**.</span></span>

   5.  <span data-ttu-id="5b750-175">Öffnen Sie in der Systemsteuerung **Configuration Manager**, und klicken Sie dann auf die Registerkarte **Aktionen** .</span><span class="sxs-lookup"><span data-stu-id="5b750-175">In Control Panel, open **Configuration Manager**, and then click the **Actions** tab.</span></span>

   6.  <span data-ttu-id="5b750-176">Wählen Sie **Hardware Inventurzyklus**aus, und klicken Sie dann auf **jetzt ausführen**.</span><span class="sxs-lookup"><span data-stu-id="5b750-176">Select **Hardware Inventory Cycle**, and then click **Run Now**.</span></span> <span data-ttu-id="5b750-177">Dieser Schritt führt die Hardwareinventur mithilfe der neuen Klassen aus, die Sie in Ihre MOF-Dateien importiert haben, und sendet die Daten dann an den Configuration Manager-Server.</span><span class="sxs-lookup"><span data-stu-id="5b750-177">This step runs the hardware inventory by using the new classes that you imported to your .mof files, and then sends the data to the Configuration Manager server.</span></span>

   7.  <span data-ttu-id="5b750-178">Wählen Sie **Computerrichtlinienabruf & Evaluierungszyklus**aus, und klicken Sie dann auf **jetzt ausführen** , um die Gruppenrichtlinienobjekte anzuwenden, die für diesen Clientcomputer relevant sind.</span><span class="sxs-lookup"><span data-stu-id="5b750-178">Select **Machine Policy Retrieval & Evaluation Cycle**, and then click **Run Now** to apply the Group Policy Objects that are relevant to that client computer.</span></span>



4. <span data-ttu-id="5b750-179">Gehen Sie in der Configuration Manager-Konsole wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="5b750-179">In the Configuration Manager console, do the following:</span></span>

   1.  <span data-ttu-id="5b750-180">Klicken Sie im Navigationsbereich mit der rechten Maustaste auf **MBAM unterstützte Computer**, klicken Sie auf **Mitgliedschaft aktualisieren**, und klicken Sie dann auf **Ja** , um den Clientcomputer zu zwingen, seine Mitgliedschaft sofort zu melden.</span><span class="sxs-lookup"><span data-stu-id="5b750-180">In the navigation pane, right-click **MBAM Supported Computers**, click **Update Membership**, and then click **Yes** to force the client computer to report its membership immediately.</span></span>

   2.  <span data-ttu-id="5b750-181">Klicken Sie im Navigationsbereich auf von **MBAM unterstützte Computer** , um zu überprüfen, ob der Clientcomputer in der Sammlung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5b750-181">In the navigation pane, click **MBAM Supported Computers** to verify that the client computer appears in the collection.</span></span>

5. <span data-ttu-id="5b750-182">Öffnen Sie **Configuration Manager** auf dem Clientcomputer in der Systemsteuerung erneut, und gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="5b750-182">On the client computer, in Control Panel, reopen **Configuration Manager** again, and do the following:</span></span>

   1.  <span data-ttu-id="5b750-183">Klicken Sie auf die Registerkarte **Aktionen** , und führen Sie dann den **Computerrichtlinienabruf & Evaluierungszyklus**erneut aus.</span><span class="sxs-lookup"><span data-stu-id="5b750-183">Click the **Actions** tab, and then rerun **Machine Policy Retrieval & Evaluation Cycle**.</span></span>

   2.  <span data-ttu-id="5b750-184">Klicken Sie auf die Registerkarte **Konfigurationen** , wählen Sie den BitLocker-Basisplan aus, und klicken Sie dann auf **bewerten**.</span><span class="sxs-lookup"><span data-stu-id="5b750-184">Click the **Configurations** tab, select the BitLocker baseline, and then click **Evaluate**.</span></span>

6. <span data-ttu-id="5b750-185">Überprüfen Sie in der Configuration Manager-Konsole, ob der Clientcomputer im Enterprise-Konformitätsbericht wie folgt angezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="5b750-185">In the Configuration Manager console, verify that the client computer appears on the Enterprise Compliance Report: as follows:</span></span>

   1.  <span data-ttu-id="5b750-186">Wählen Sie im Navigationsbereich den Arbeitsbereich **Überwachung** aus.</span><span class="sxs-lookup"><span data-stu-id="5b750-186">In the navigation pane, select the **Monitoring** workspace.</span></span>

   2.  <span data-ttu-id="5b750-187">Erweitern Sie in der Konsolenstruktur **Übersicht** &gt; **Bericht Erstellungs** &gt; **Berichte** &gt; **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="5b750-187">In the console tree, expand **Overview** &gt; **Reporting** &gt; **Reports** &gt; **MBAM**.</span></span>

   3.  <span data-ttu-id="5b750-188">Wählen Sie den Ordner aus, der die Sprache darstellt, in der Sie Berichte anzeigen möchten, und wählen Sie dann den Bericht im Bereich Ergebnisse aus.</span><span class="sxs-lookup"><span data-stu-id="5b750-188">Select the folder that represents the language in which you want to view reports, and then select the report in the results pane.</span></span>

## <span data-ttu-id="5b750-189">Auswerten von MBAM 2,5 mithilfe der System Center Configuration Manager 2007-Integrations Topologie</span><span class="sxs-lookup"><span data-stu-id="5b750-189">Evaluating MBAM 2.5 by using the System Center Configuration Manager 2007 Integration topology</span></span>


<span data-ttu-id="5b750-190">Wenn Sie MBAM mithilfe der Configuration Manager-Integrations Topologie auswerten möchten, führen Sie die gleichen Schritte aus, um MBAM in Ihrer Testumgebung während der Verwendung in einer Produktionsumgebung zu installieren und zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="5b750-190">To evaluate MBAM by using the Configuration Manager Integration topology, follow the same steps to install and configure MBAM in your test environment as you use in a production environment.</span></span> <span data-ttu-id="5b750-191">Nachdem Sie den MBAM-Client auf einem Clientcomputer installiert haben, führen Sie die zusätzlichen Schritte in diesem Thema aus, um dem MBAM-Client zu ermöglichen, den Status des Computers an MBAM schneller zu melden.</span><span class="sxs-lookup"><span data-stu-id="5b750-191">After installing the MBAM Client on a client computer, complete the additional steps in this topic to enable the MBAM Client to start reporting the computer’s status to MBAM more quickly.</span></span>

**<span data-ttu-id="5b750-192">So evaluieren Sie MBAM mithilfe der Configuration Manager 2007-Integrations Topologie</span><span class="sxs-lookup"><span data-stu-id="5b750-192">To evaluate MBAM by using the Configuration Manager 2007 Integration topology</span></span>**

1. <span data-ttu-id="5b750-193">Bevor Sie MBAM installieren, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="5b750-193">Before you install MBAM, do the following:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="5b750-194">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="5b750-194">Task</span></span></th>
   <th align="left"><span data-ttu-id="5b750-195">Wo erhalte ich Anweisungen?</span><span class="sxs-lookup"><span data-stu-id="5b750-195">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5b750-196">Stellen Sie sicher, dass Sie alle erforderlichen Software installiert haben.</span><span class="sxs-lookup"><span data-stu-id="5b750-196">Ensure that you have installed all of the prerequisite software.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="5b750-197">MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien</span><span class="sxs-lookup"><span data-stu-id="5b750-197">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="5b750-198">MBAM 2.5-Servervoraussetzungen, die nur für die Configuration Manager-Integrationstopologie gelten</span><span class="sxs-lookup"><span data-stu-id="5b750-198">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="5b750-199">Überprüfen Sie die erforderlichen Hardware-, RAM-und anderen Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5b750-199">Check the required hardware, RAM, and other specifications.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="5b750-200">Von MBAM 2.5 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="5b750-200">MBAM 2.5 Supported Configurations</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5b750-201">Erstellen oder bearbeiten Sie die MOF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="5b750-201">Create or edit the .mof files.</span></span></p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)"><span data-ttu-id="5b750-202">Bearbeiten der Datei „Configuration.mof“</span><span class="sxs-lookup"><span data-stu-id="5b750-202">Edit the Configuration.mof File</span></span></a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)"><span data-ttu-id="5b750-203">Erstellen oder Bearbeiten der Datei „Sms_def.mof“</span><span class="sxs-lookup"><span data-stu-id="5b750-203">Create or Edit the Sms_def.mof File</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="5b750-204">Installieren Sie die MBAM-Server Software, und konfigurieren Sie dann die gewünschten Features.</span><span class="sxs-lookup"><span data-stu-id="5b750-204">Install the MBAM Server software, and then configure the features you want.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="5b750-205">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="5b750-205">Task</span></span></th>
   <th align="left"><span data-ttu-id="5b750-206">Wo erhalte ich Anweisungen?</span><span class="sxs-lookup"><span data-stu-id="5b750-206">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5b750-207">Installieren Sie die MBAM-Server Software auf jedem Server, auf dem Sie ein MBAM-Server Feature konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="5b750-207">Install the MBAM Server software on each server where you want to configure an MBAM Server feature.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="5b750-208">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="5b750-208">Note</span></span></strong><br/><p><span data-ttu-id="5b750-209">Sie können die Datenbanken auf einem SQL Server-Remotecomputer mit Windows PowerShell oder einem exportierten Data-tier Application (DAC)-Paket installieren.</span><span class="sxs-lookup"><span data-stu-id="5b750-209">You can install the databases to a remote SQL Server computer by using Windows PowerShell or an exported data-tier application (DAC) package.</span></span> <span data-ttu-id="5b750-210">Weitere Informationen zu DAC-Paketen finden Sie unter <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> Datenebenen-Anwendungen </a> .</span><span class="sxs-lookup"><span data-stu-id="5b750-210">For more information about DAC packages, see <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)">Data-tier Applications</a>.</span></span></p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="5b750-211">Installieren der MBAM 2.5-Serversoftware</span><span class="sxs-lookup"><span data-stu-id="5b750-211">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="5b750-212">Konfigurieren Sie die Datenbank für Compliance und Audit sowie die Wiederherstellungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="5b750-212">Configure the Compliance and Audit Database and the Recovery Database.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="5b750-213">So konfigurieren Sie die MBAM 2.5-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="5b750-213">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5b750-214">Konfigurieren Sie das Feature Berichte.</span><span class="sxs-lookup"><span data-stu-id="5b750-214">Configure the Reports feature.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="5b750-215">So konfigurieren Sie die MBAM 2.5-Berichte</span><span class="sxs-lookup"><span data-stu-id="5b750-215">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="5b750-216">Konfigurieren Sie die Webanwendungen.</span><span class="sxs-lookup"><span data-stu-id="5b750-216">Configure the web applications.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="5b750-217">So konfigurieren Sie die MBAM 2.5-Webanwendungen</span><span class="sxs-lookup"><span data-stu-id="5b750-217">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5b750-218">Konfigurieren Sie den System Center-Konfigurations-Manager, um die Configuration Manager-Objekte zu installieren.</span><span class="sxs-lookup"><span data-stu-id="5b750-218">Configure the System Center Configuration Manager to install the Configuration Manager objects.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)"><span data-ttu-id="5b750-219">So konfigurieren Sie die Integration von MBAM 2.5 in System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="5b750-219">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="5b750-220">Gehen Sie auf einem Clientcomputer wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="5b750-220">On a client computer, do the following:</span></span>

   1.  <span data-ttu-id="5b750-221">Installieren Sie den MBAM-Client auf einem Clientcomputer.</span><span class="sxs-lookup"><span data-stu-id="5b750-221">Install the MBAM Client on a client computer.</span></span>

   2.  <span data-ttu-id="5b750-222">Wenden Sie die MBAM-Gruppenrichtlinienobjekte auf den Computer an.</span><span class="sxs-lookup"><span data-stu-id="5b750-222">Apply the MBAM Group Policy Objects to the computer.</span></span>

   3.  <span data-ttu-id="5b750-223">Setzen Sie die folgenden Registrierungsschlüssel, um zu erzwingen, dass der MBAM-Client schneller und in schnelleren Intervallen aufwacht:</span><span class="sxs-lookup"><span data-stu-id="5b750-223">Set the following registry keys to force the MBAM Client to wake up more quickly and at faster intervals:</span></span>

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **<span data-ttu-id="5b750-224">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="5b750-224">Note</span></span>**  
       <span data-ttu-id="5b750-225">Da diese Tasten den MBAM-Client pro Minute reaktivieren, empfehlen wir, diese Registrierungsschlüsseleinstellungen nur in einer Evaluierungsumgebung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5b750-225">Because these keys wake up the MBAM Client every minute, we recommend that you use these registry key settings only in an evaluation environment.</span></span>



   4.  <span data-ttu-id="5b750-226">Starten Sie den **BitLocker-Verwaltungs Client Dienst**erneut.</span><span class="sxs-lookup"><span data-stu-id="5b750-226">Restart the **BitLocker Management Client Service**.</span></span>

   5.  <span data-ttu-id="5b750-227">Öffnen Sie in der Systemsteuerung **Configuration Manager**, und klicken Sie dann auf die Registerkarte **Aktionen** .</span><span class="sxs-lookup"><span data-stu-id="5b750-227">In Control Panel, open **Configuration Manager**, and then click the **Actions** tab.</span></span>

   6.  <span data-ttu-id="5b750-228">Wählen Sie **Computerrichtlinienabruf & Evaluierungszyklus**aus, und klicken Sie dann auf **jetzt ausführen** , um die Gruppenrichtlinienobjekte anzuwenden, die für diesen Clientcomputer relevant sind.</span><span class="sxs-lookup"><span data-stu-id="5b750-228">Select **Machine Policy Retrieval & Evaluation Cycle**, and then click **Run Now** to apply the Group Policy Objects that are relevant to that client computer.</span></span>

   7.  <span data-ttu-id="5b750-229">Wählen Sie **Hardware Inventurzyklus**aus, und klicken Sie dann auf **jetzt ausführen**.</span><span class="sxs-lookup"><span data-stu-id="5b750-229">Select **Hardware Inventory Cycle**, and then click **Run Now**.</span></span> <span data-ttu-id="5b750-230">Dieser Schritt führt die Hardwareinventur mithilfe der neuen Klassen aus, die Sie in Ihre MOF-Dateien importiert haben, und sendet die Daten dann an den Configuration Manager-Server.</span><span class="sxs-lookup"><span data-stu-id="5b750-230">This step runs the hardware inventory by using the new classes that you imported to your .mof files and then sends the data to the Configuration Manager server.</span></span>

4. <span data-ttu-id="5b750-231">Gehen Sie in der Configuration Manager-Konsole wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="5b750-231">In the Configuration Manager console, do the following:</span></span>

   1.  <span data-ttu-id="5b750-232">Klicken Sie im Navigationsbereich mit der rechten Maustaste auf **MBAM unterstützte Computer**, klicken Sie auf **Mitgliedschaft aktualisieren**, und klicken Sie dann auf **Ja** , um den Clientcomputer zu zwingen, seine Mitgliedschaft sofort zu melden.</span><span class="sxs-lookup"><span data-stu-id="5b750-232">In the navigation pane, right-click **MBAM Supported Computers**, click **Update Membership**, and then click **Yes** to force the client computer to report its membership immediately.</span></span>

   2.  <span data-ttu-id="5b750-233">Klicken Sie im Navigationsbereich auf von **MBAM unterstützte Computer** , um zu überprüfen, ob der Clientcomputer in der Sammlung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5b750-233">In the navigation pane, click **MBAM Supported Computers** to verify that the client computer appears in the collection.</span></span>

5. <span data-ttu-id="5b750-234">Öffnen Sie **Configuration Manager** auf dem Clientcomputer in der Systemsteuerung erneut, und gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="5b750-234">On the client computer, in Control Panel, reopen **Configuration Manager** again, and do the following:</span></span>

   1.  <span data-ttu-id="5b750-235">Klicken Sie auf die Registerkarte **Aktionen** , und führen Sie dann den **Computerrichtlinienabruf & Evaluierungszyklus**erneut aus.</span><span class="sxs-lookup"><span data-stu-id="5b750-235">Click the **Actions** tab, and then rerun **Machine Policy Retrieval & Evaluation Cycle**.</span></span>

   2.  <span data-ttu-id="5b750-236">Klicken Sie auf die Registerkarte **Konfigurationen** , wählen Sie den BitLocker-Basisplan aus, und klicken Sie auf **bewerten**.</span><span class="sxs-lookup"><span data-stu-id="5b750-236">Click the **Configurations** tab, select the BitLocker baseline, and click **Evaluate**.</span></span>

6. <span data-ttu-id="5b750-237">Überprüfen Sie in der Configuration Manager-Konsole, ob der Clientcomputer im Enterprise-Konformitätsbericht wie folgt angezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="5b750-237">In the Configuration Manager console, verify that the client computer appears on the Enterprise Compliance Report, as follows</span></span>

   1.  <span data-ttu-id="5b750-238">Erweitern Sie im Navigationsbereich **Computer Management** &gt; **Reporting** &gt; **Reporting Services** - &gt; \*\* &lt; Servername &gt; MBAM\*\*.</span><span class="sxs-lookup"><span data-stu-id="5b750-238">In the navigation pane, expand **Computer Management** &gt; **Reporting** &gt; **Reporting Services** &gt; **&lt;server name&gt;MBAM**.</span></span>

   2.  <span data-ttu-id="5b750-239">Wählen Sie im Knoten **MBAM** den Ordner aus, der die Sprache darstellt, in der Sie Berichte anzeigen möchten, und wählen Sie dann den Bericht im Bereich Ergebnisse aus.</span><span class="sxs-lookup"><span data-stu-id="5b750-239">Within the **MBAM** node, select the folder that represents the language in which you want to view reports, and then select the report from the results pane.</span></span>


## <span data-ttu-id="5b750-240">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5b750-240">Related topics</span></span>


[<span data-ttu-id="5b750-241">Erste Schritte mit MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="5b750-241">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)


## <span data-ttu-id="5b750-242">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="5b750-242">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="5b750-243">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="5b750-243">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="5b750-244">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="5b750-244">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>





