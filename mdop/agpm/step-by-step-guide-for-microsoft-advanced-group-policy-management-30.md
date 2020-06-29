---
title: Schrittweise Anleitung für Microsoft Advanced Group Policy Management 3.0
description: Schrittweise Anleitung für Microsoft Advanced Group Policy Management 3.0
author: dansimp
ms.assetid: d067f465-d7c8-4f6d-b311-66b9b06874f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b4efa5075027e99a3e50a344aafcdf6f6f69a147
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807463"
---
# <span data-ttu-id="8c305-103">Schrittweise Anleitung für Microsoft Advanced Group Policy Management 3.0</span><span class="sxs-lookup"><span data-stu-id="8c305-103">Step-by-Step Guide for Microsoft Advanced Group Policy Management 3.0</span></span>


<span data-ttu-id="8c305-104">Diese Schritt-für-Schritt-Anleitung zeigt erweiterte Techniken für die Gruppenrichtlinienverwaltung mithilfe der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) und Microsoft Advanced Group Policy Management (AGPM).</span><span class="sxs-lookup"><span data-stu-id="8c305-104">This step-by-step guide demonstrates advanced techniques for Group Policy management using the Group Policy Management Console (GPMC) and Microsoft Advanced Group Policy Management (AGPM).</span></span> <span data-ttu-id="8c305-105">AGPM vergrößert die Funktionen der GPMC und bietet Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8c305-105">AGPM increases the capabilities of the GPMC, providing:</span></span>

-   <span data-ttu-id="8c305-106">Standard Rollen für das Delegieren von Berechtigungen zum Verwalten von Gruppenrichtlinienobjekten (GPOs) an mehrere Gruppenrichtlinienadministratoren sowie die Möglichkeit, den Zugriff auf GPOs in der Produktionsumgebung zu delegieren.</span><span class="sxs-lookup"><span data-stu-id="8c305-106">Standard roles for delegating permissions to manage Group Policy objects (GPOs) to multiple Group Policy administrators, as well as the ability to delegate access to GPOs in the production environment.</span></span>

-   <span data-ttu-id="8c305-107">Ein Archiv, damit Gruppenrichtlinienadministratoren GPOs offline erstellen und ändern können, bevor Sie in einer Produktionsumgebung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8c305-107">An archive to enable Group Policy administrators to create and modify GPOs offline before deploying them to a production environment.</span></span>

-   <span data-ttu-id="8c305-108">Die Möglichkeit, einen Rollback zu einer beliebigen vorherigen Version eines GPO im Archiv durchführen und die Anzahl der im Archiv gespeicherten Versionen zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="8c305-108">The ability to roll back to any previous version of a GPO in the archive and to limit the number of versions stored in the archive.</span></span>

-   <span data-ttu-id="8c305-109">Möglichkeit zum ein-und Auschecken von GPOs, um sicherzustellen, dass Gruppenrichtlinienadministratoren die Arbeit des anderen nicht versehentlich überschreiben.</span><span class="sxs-lookup"><span data-stu-id="8c305-109">Check-in/check-out capability for GPOs to ensure that Group Policy administrators do not inadvertently overwrite each other's work.</span></span>

## <span data-ttu-id="8c305-110">Übersicht über AGPM-Szenarien</span><span class="sxs-lookup"><span data-stu-id="8c305-110">AGPM scenario overview</span></span>


<span data-ttu-id="8c305-111">In diesem Szenario verwenden Sie für jede Rolle in AGPM ein separates Benutzerkonto, um zu veranschaulichen, wie Gruppenrichtlinien in einer Umgebung mit mehreren Gruppenrichtlinienadministratoren verwaltet werden können, die unterschiedliche Berechtigungsstufen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8c305-111">For this scenario, you will use a separate user account for each role in AGPM to demonstrate how Group Policy can be managed in an environment with multiple Group Policy administrators who have different levels of permissions.</span></span> <span data-ttu-id="8c305-112">Insbesondere führen Sie die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="8c305-112">Specifically, you will perform the following tasks:</span></span>

-   <span data-ttu-id="8c305-113">Wenn Sie ein Konto verwenden, das Mitglied der Gruppe der Domänenadministratoren ist, installieren Sie AGPM Server, und weisen Sie die Rolle AGPM-Administrator einem Konto oder einer Gruppe zu.</span><span class="sxs-lookup"><span data-stu-id="8c305-113">Using an account that is a member of the Domain Admins group, install AGPM Server and assign the AGPM Administrator role to an account or group.</span></span>

-   <span data-ttu-id="8c305-114">Installieren Sie AGPM-Client mithilfe von Konten, denen Sie AGPM-Rollen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="8c305-114">Using accounts to which you will assign AGPM roles, install AGPM Client.</span></span>

-   <span data-ttu-id="8c305-115">Wenn Sie ein Konto mit der Rolle AGPM-Administrator verwenden, konfigurieren Sie AGPM, und delegieren Sie den Zugriff auf GPOs, indem Sie anderen Konten Rollen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="8c305-115">Using an account with the AGPM Administrator role, configure AGPM and delegate access to GPOs by assigning roles to other accounts.</span></span>

-   <span data-ttu-id="8c305-116">Wenn Sie ein Konto mit der Rolle des Editors verwenden, fordern Sie die Erstellung eines Gruppenrichtlinienobjekts an, das Sie dann mit einem Konto mit der Rolle genehmigende Person genehmigen.</span><span class="sxs-lookup"><span data-stu-id="8c305-116">Using an account with the Editor role, request the creation of a GPO, which you then approve using an account with the Approver role.</span></span> <span data-ttu-id="8c305-117">Überprüfen Sie mit dem Editor-Konto das Gruppenrichtlinienobjekt aus dem Archiv, bearbeiten Sie das Gruppenrichtlinienobjekt, überprüfen Sie das Gruppenrichtlinienobjekt in das Archiv, und fordern Sie die Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="8c305-117">With the Editor account, check the GPO out of the archive, edit the GPO, check the GPO into the archive, and request deployment.</span></span>

-   <span data-ttu-id="8c305-118">Überprüfen Sie das Gruppenrichtlinienobjekt, und stellen Sie es in Ihrer Produktionsumgebung bereit, indem Sie ein Konto mit der Rolle genehmigende Person verwenden.</span><span class="sxs-lookup"><span data-stu-id="8c305-118">Using an account with the Approver role, review the GPO and deploy it to your production environment.</span></span>

-   <span data-ttu-id="8c305-119">Erstellen Sie mithilfe eines Kontos mit der Rolle "Editor" eine GPO-Vorlage, und verwenden Sie Sie als Ausgangspunkt zum Erstellen eines neuen Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="8c305-119">Using an account with the Editor role, create a GPO template and use it as a starting point to create a new GPO.</span></span>

-   <span data-ttu-id="8c305-120">Wenn Sie ein Konto mit der Rolle genehmigende Person verwenden, löschen Sie ein GPO, und stellen Sie es wieder her.</span><span class="sxs-lookup"><span data-stu-id="8c305-120">Using an account with the Approver role, delete and restore a GPO.</span></span>

![Entwicklungsprozess für Gruppenrichtlinienobjekte](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <span data-ttu-id="8c305-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c305-122">Requirements</span></span>


<span data-ttu-id="8c305-123">Computer, auf denen Sie AGPM installieren möchten, müssen die folgenden Anforderungen erfüllen, und Sie müssen Konten erstellen, die in diesem Szenario verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="8c305-123">Computers on which you want to install AGPM must meet the following requirements, and you must create accounts for use in this scenario.</span></span>

<span data-ttu-id="8c305-124">**Hinweis**  Wenn Sie AGPM 2,5 installiert haben und ein Upgrade von Windows Server® 2003 auf Windows Server2008 oder Windows Vista® ohne installierte Service Packs für Windows Vista mit Dienst pack1 durchführen, müssen Sie das Betriebssystem aktualisieren, bevor Sie auf AGPM 3.0 aktualisieren können.</span><span class="sxs-lookup"><span data-stu-id="8c305-124">**Note** If you have AGPM 2.5 installed and are upgrading from Windows Server®2003 to Windows Server2008 or WindowsVista® with no service packs installed to WindowsVista with Service Pack1, you must upgrade the operating system before you can upgrade to AGPM3.0.</span></span>

 

### <span data-ttu-id="8c305-125">AGPM-Server Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c305-125">AGPM Server requirements</span></span>

<span data-ttu-id="8c305-126">AGPM Server 3.0 erfordert Windows Server2008 oder Windows Vista mit dem Dienst Pack1 und der GPMC von Remote Server-Verwaltungs Tools (Remote Server Administration Tools), die installiert werden.</span><span class="sxs-lookup"><span data-stu-id="8c305-126">AGPM Server3.0 requires Windows Server2008 or WindowsVista with Service Pack1 and the GPMC from Remote Server Administration Tools (RSAT) installed.</span></span> <span data-ttu-id="8c305-127">Sowohl 32-Bit-als auch 64-Bit-Versionen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8c305-127">Both 32-bit and 64-bit versions are supported.</span></span>

<span data-ttu-id="8c305-128">Bevor Sie AGPM Server installieren, müssen Sie Mitglied der Gruppe der Domänenadministratoren sein, und die folgenden Windows-Features müssen vorhanden sein, sofern nicht anders angegeben:</span><span class="sxs-lookup"><span data-stu-id="8c305-128">Before you install AGPM Server, you must be a member of the Domain Admins group and the following Windows features must be present unless otherwise noted:</span></span>

-   <span data-ttu-id="8c305-129">GPMC</span><span class="sxs-lookup"><span data-stu-id="8c305-129">GPMC</span></span>

    -   <span data-ttu-id="8c305-130">Windows Server 2008: die GPMC wird automatisch von AGPM installiert, wenn Sie nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8c305-130">Windows Server 2008: The GPMC is automatically installed by AGPM if not present.</span></span>

    -   <span data-ttu-id="8c305-131">Windows Vista: Sie müssen die GPMC vor der Installation von AGPM über die Remoteverwaltungskonsole installieren.</span><span class="sxs-lookup"><span data-stu-id="8c305-131">Windows Vista: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="8c305-132">Weitere Informationen finden Sie unter <https://go.microsoft.com/fwlink/?LinkID=116179>.</span><span class="sxs-lookup"><span data-stu-id="8c305-132">For more information, see <https://go.microsoft.com/fwlink/?LinkID=116179>.</span></span>

-   <span data-ttu-id="8c305-133">.NET Framework 3.5</span><span class="sxs-lookup"><span data-stu-id="8c305-133">.NET Framework 3.5</span></span>

<span data-ttu-id="8c305-134">Die folgenden Windows-Features sind für AGPM Server erforderlich und werden automatisch installiert, wenn Sie nicht vorhanden sind:</span><span class="sxs-lookup"><span data-stu-id="8c305-134">The following Windows features are required by AGPM Server and will be automatically installed if not present:</span></span>

-   <span data-ttu-id="8c305-135">WCF-Aktivierung; Nicht-HTTP-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="8c305-135">WCF Activation; Non-HTTP Activation</span></span>

-   <span data-ttu-id="8c305-136">Windows-Prozessaktivierungsdienst</span><span class="sxs-lookup"><span data-stu-id="8c305-136">Windows Process Activation Service</span></span>

    -   <span data-ttu-id="8c305-137">Prozessmodell</span><span class="sxs-lookup"><span data-stu-id="8c305-137">Process Model</span></span>

    -   <span data-ttu-id="8c305-138">.NET-Umgebung</span><span class="sxs-lookup"><span data-stu-id="8c305-138">.NET Environment</span></span>

    -   <span data-ttu-id="8c305-139">Konfigurations-APIs</span><span class="sxs-lookup"><span data-stu-id="8c305-139">Configuration APIs</span></span>

### <span data-ttu-id="8c305-140">AGPM-Client Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c305-140">AGPM Client requirements</span></span>

<span data-ttu-id="8c305-141">AGPM Client 3.0 erfordert Windows-Server2008 oder Windows Vista mit Service Pack 1 und der GPMC von Remote Server-Verwaltungs Tools (Remote Server Administration Tools).</span><span class="sxs-lookup"><span data-stu-id="8c305-141">AGPM Client3.0 requires Windows Server2008 or WindowsVista with Service Pack 1 and the GPMC from Remote Server Administration Tools (RSAT) installed.</span></span> <span data-ttu-id="8c305-142">Sowohl 32-Bit-als auch 64-Bit-Versionen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8c305-142">Both 32-bit and 64-bit versions are supported.</span></span> <span data-ttu-id="8c305-143">AGPM-Client kann auf einem Computer mit AGPM Server installiert werden.</span><span class="sxs-lookup"><span data-stu-id="8c305-143">AGPM Client can be installed on a computer running AGPM Server.</span></span>

<span data-ttu-id="8c305-144">Die folgenden Windows-Features sind für AGPM-Client erforderlich und werden automatisch installiert, wenn Sie nicht vorhanden sind, sofern nicht anders angegeben:</span><span class="sxs-lookup"><span data-stu-id="8c305-144">The following Windows features are required by AGPM Client and will be automatically installed if not present unless otherwise noted:</span></span>

-   <span data-ttu-id="8c305-145">GPMC</span><span class="sxs-lookup"><span data-stu-id="8c305-145">GPMC</span></span>

    -   <span data-ttu-id="8c305-146">Windows Server 2008: die GPMC wird automatisch von AGPM installiert, wenn Sie nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8c305-146">Windows Server 2008: The GPMC is automatically installed by AGPM if not present.</span></span>

    -   <span data-ttu-id="8c305-147">Windows Vista: Sie müssen die GPMC vor der Installation von AGPM über die Remoteverwaltungskonsole installieren.</span><span class="sxs-lookup"><span data-stu-id="8c305-147">Windows Vista: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="8c305-148">Weitere Informationen finden Sie unter <https://go.microsoft.com/fwlink/?LinkID=116179>.</span><span class="sxs-lookup"><span data-stu-id="8c305-148">For more information, see <https://go.microsoft.com/fwlink/?LinkID=116179>.</span></span>

-   <span data-ttu-id="8c305-149">.NET Framework 3,0</span><span class="sxs-lookup"><span data-stu-id="8c305-149">.NET Framework 3.0</span></span>

### <span data-ttu-id="8c305-150">Voraussetzungen für Szenarien</span><span class="sxs-lookup"><span data-stu-id="8c305-150">Scenario requirements</span></span>

<span data-ttu-id="8c305-151">Bevor Sie mit diesem Szenario beginnen, erstellen Sie vier Benutzerkonten.</span><span class="sxs-lookup"><span data-stu-id="8c305-151">Before you begin this scenario, create four user accounts.</span></span> <span data-ttu-id="8c305-152">Während des Szenarios weisen Sie jedem dieser Konten eine der folgenden AGPM-Rollen zu: AGPM-Administrator (Vollzugriff), genehmigende Person, Editor und Bearbeiter.</span><span class="sxs-lookup"><span data-stu-id="8c305-152">During the scenario, you will assign one of the following AGPM roles to each of these accounts: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="8c305-153">Diese Konten müssen in der Lage sein, e-Mail-Nachrichten zu senden und zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="8c305-153">These accounts must be able to send and receive e-mail messages.</span></span> <span data-ttu-id="8c305-154">Weisen Sie den Konten mit den Rollen des AGPM-Administrators, genehmigenden und (optional)-Editors die Berechtigung " **Link-GPOs** " zu.</span><span class="sxs-lookup"><span data-stu-id="8c305-154">Assign **Link GPOs** permission to the accounts with the AGPM Administrator, Approver, and (optionally) Editor roles.</span></span>

<span data-ttu-id="8c305-155">**Hinweis** 
 Die Berechtigung " **GPOs verknüpfen** " wird standardmäßig Mitgliedern von Domänenadministratoren und Unternehmensadministratoren zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="8c305-155">**Note**
**Link GPOs** permission is assigned to members of Domain Administrators and Enterprise Administrators by default.</span></span> <span data-ttu-id="8c305-156">Klicken Sie auf den Knoten für die Domäne, und klicken Sie dann auf die Registerkarte **Delegierung** , wählen Sie **GPOs verknüpfen**aus, klicken Sie auf **Hinzufügen**, und wählen Sie dann Benutzer oder Gruppen aus, denen die Berechtigung zugewiesen werden soll, wenn Sie zusätzlichen Benutzern oder Gruppen die Berechtigung zum **Verknüpfen von GPOs** zuweisen möchten (beispielsweise Konten mit den Rollen AGPM-Administrator oder genehmigende Person).</span><span class="sxs-lookup"><span data-stu-id="8c305-156">To assign **Link GPOs** permission to additional users or groups (such as accounts with the roles of AGPM Administrator or Approver), click the node for the domain and then click the **Delegation** tab, select **Link GPOs**, click **Add**, and select users or groups to which to assign the permission.</span></span>

 

## <span data-ttu-id="8c305-157">Schritte zum Installieren und Konfigurieren von AGPM</span><span class="sxs-lookup"><span data-stu-id="8c305-157">Steps for installing and configuring AGPM</span></span>


<span data-ttu-id="8c305-158">Sie müssen die folgenden Schritte ausführen, um AGPM zu installieren und zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8c305-158">You must complete the following steps to install and configure AGPM.</span></span>

[<span data-ttu-id="8c305-159">Schritt 1: Installieren des AGPM-Servers</span><span class="sxs-lookup"><span data-stu-id="8c305-159">Step 1: Install AGPM Server</span></span>](#bkmk-config1)

[<span data-ttu-id="8c305-160">Schritt 2: Installieren des AGPM-Clients</span><span class="sxs-lookup"><span data-stu-id="8c305-160">Step 2: Install AGPM Client</span></span>](#bkmk-config2)

[<span data-ttu-id="8c305-161">Schritt 3: Konfigurieren einer AGPM-Server Verbindung</span><span class="sxs-lookup"><span data-stu-id="8c305-161">Step 3: Configure an AGPM Server connection</span></span>](#bkmk-config3)

[<span data-ttu-id="8c305-162">Schritt 4: Konfigurieren einer e-Mail-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="8c305-162">Step 4: Configure e-mail notification</span></span>](#bkmk-config4)

[<span data-ttu-id="8c305-163">Schritt 5: Delegieren des Zugriffs</span><span class="sxs-lookup"><span data-stu-id="8c305-163">Step 5: Delegate access</span></span>](#bkmk-config5)

### <a href="" id="bkmk-config1"></a><span data-ttu-id="8c305-164">Schritt 1: Installieren des AGPM-Servers</span><span class="sxs-lookup"><span data-stu-id="8c305-164">Step 1: Install AGPM Server</span></span>

<span data-ttu-id="8c305-165">In diesem Schritt installieren Sie AGPM Server auf dem Mitglieds Server oder Domänencontroller, auf dem der AGPM-Dienst ausgeführt wird, und konfigurieren das Archiv.</span><span class="sxs-lookup"><span data-stu-id="8c305-165">In this step, you install AGPM Server on the member server or domain controller that will run the AGPM Service, and you configure the archive.</span></span> <span data-ttu-id="8c305-166">Alle AGPM-Vorgänge werden über diesen Windows-Dienst verwaltet und mit den Anmeldeinformationen des Diensts ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c305-166">All AGPM operations are managed through this Windows service and are executed with the service's credentials.</span></span> <span data-ttu-id="8c305-167">Das von einem AGPM-Server verwaltete Archiv kann auf diesem Server oder auf einem anderen Server in derselben Gesamtstruktur gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="8c305-167">The archive managed by an AGPM Server can be hosted on that server or on another server in the same forest.</span></span>

**<span data-ttu-id="8c305-168">So installieren Sie AGPM Server auf dem Computer, der den AGPM-Dienst hosten soll</span><span class="sxs-lookup"><span data-stu-id="8c305-168">To install AGPM Server on the computer that will host the AGPM Service</span></span>**

1.  <span data-ttu-id="8c305-169">Melden Sie sich mit einem Konto an, das Mitglied der Gruppe der Domänenadministratoren ist.</span><span class="sxs-lookup"><span data-stu-id="8c305-169">Log on with an account that is a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="8c305-170">Starten Sie die Microsoft Desktop Optimization Pack-CD, und folgen Sie den Anweisungen auf dem Bildschirm, um **Advanced Group Policy Management-Server**auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="8c305-170">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Server**.</span></span>

3.  <span data-ttu-id="8c305-171">Klicken Sie im Dialogfeld **Willkommen** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="8c305-171">In the **Welcome** dialog box, click **Next**.</span></span>

4.  <span data-ttu-id="8c305-172">Akzeptieren Sie im Dialogfeld **Microsoft-Software-Lizenzbestimmungen** die Begriffe, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="8c305-172">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

5.  <span data-ttu-id="8c305-173">Wählen Sie im Dialogfeld **Anwendungspfad** einen Speicherort aus, an dem AGPM Server installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c305-173">In the **Application Path** dialog box, select a location in which to install AGPM Server.</span></span> <span data-ttu-id="8c305-174">Auf dem Computer, auf dem AGPM Server installiert ist, wird der AGPM-Dienst gehostet und das Archiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="8c305-174">The computer on which AGPM Server is installed will host the AGPM Service and manage the archive.</span></span> <span data-ttu-id="8c305-175">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="8c305-175">Click **Next**.</span></span>

6.  <span data-ttu-id="8c305-176">Wählen Sie im Dialogfeld **Archivpfad** einen Speicherort für das Archiv relativ zum AGPM-Server aus.</span><span class="sxs-lookup"><span data-stu-id="8c305-176">In the **Archive Path** dialog box, select a location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="8c305-177">Der Archivpfad kann auf einen Ordner auf dem AGPM-Server oder an anderer Stelle verweisen, Sie sollten jedoch einen Speicherort mit genügend Speicherplatz zum Speichern aller GPOs und Verlaufsdaten auswählen, die von diesem AGPM-Server verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="8c305-177">The archive path can point to a folder on the AGPM Server or elsewhere, but you should select a location with sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span> <span data-ttu-id="8c305-178">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="8c305-178">Click **Next**.</span></span>

7.  <span data-ttu-id="8c305-179">Wählen Sie im Dialogfeld **AGPM-Dienstkonto** ein Dienstkonto aus, unter dem der AGPM-Dienst ausgeführt wird, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="8c305-179">In the **AGPM Service Account** dialog box, select a service account under which the AGPM Service will run and then click **Next**.</span></span>

8.  <span data-ttu-id="8c305-180">Wählen Sie im Dialogfeld **Besitzer des Archivs** ein Konto oder eine Gruppe aus, dem Sie zunächst die Rolle AGPM-Administrator (Vollzugriff) zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="8c305-180">In the **Archive Owner** dialog box, select an account or group to which to initially assign the AGPM Administrator (Full Control) role.</span></span> <span data-ttu-id="8c305-181">Dieser AGPM-Administrator kann anderen Gruppenrichtlinienadministratoren AGPM-Rollen und-Berechtigungen zuweisen (einschließlich der Rolle des AGPM-Administrators).</span><span class="sxs-lookup"><span data-stu-id="8c305-181">This AGPM Administrator can assign AGPM roles and permissions to other Group Policy administrators (including the role of AGPM Administrator).</span></span> <span data-ttu-id="8c305-182">Wählen Sie in diesem Szenario das Konto aus, das in der Rolle des AGPM-Administrators dienen soll.</span><span class="sxs-lookup"><span data-stu-id="8c305-182">For this scenario, select the account to serve in the AGPM Administrator role.</span></span> <span data-ttu-id="8c305-183">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="8c305-183">Click **Next**.</span></span>

9.  <span data-ttu-id="8c305-184">Geben Sie im Dialogfeld **Portkonfiguration** einen Port ein, den der AGPM-Dienst abhören soll.</span><span class="sxs-lookup"><span data-stu-id="8c305-184">In the **Port Configuration** dialog box, type a port on which the AGPM Service should listen.</span></span> <span data-ttu-id="8c305-185">Deaktivieren Sie das Kontrollkästchen **Portausnahme für Firewall hinzufügen** , es sei denn, Sie konfigurieren Portausnahmen manuell oder verwenden Regeln, um Portausnahmen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8c305-185">Do not clear the **Add port exception to firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="8c305-186">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="8c305-186">Click **Next**.</span></span>

10. <span data-ttu-id="8c305-187">Wählen Sie im Dialogfeld **Sprachen** eine oder mehrere Anzeigesprachen aus, die für AGPM Server installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8c305-187">In the **Languages** dialog box, select one or more display languages to install for AGPM Server.</span></span>

11. <span data-ttu-id="8c305-188">Klicken Sie auf **Installieren**, und klicken Sie dann auf **Fertig stellen** , um den Setup-Assistenten zu beenden.</span><span class="sxs-lookup"><span data-stu-id="8c305-188">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

    <span data-ttu-id="8c305-189">**Vorsicht**  Ändern Sie die Einstellungen für den AGPM-Dienst nicht über **Administrative Tools** und **Dienste** im Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="8c305-189">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="8c305-190">Dadurch kann der Start des AGPM-Diensts verhindert werden.</span><span class="sxs-lookup"><span data-stu-id="8c305-190">Doing so can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="8c305-191">Informationen zum Ändern der Einstellungen für den Dienst finden Sie unter Hilfe zur erweiterten Gruppenrichtlinienverwaltung.</span><span class="sxs-lookup"><span data-stu-id="8c305-191">For information on how to modify settings for the service, see Help for Advanced Group Policy Management.</span></span>

     

### <a href="" id="bkmk-config2"></a><span data-ttu-id="8c305-192">Schritt 2: Installieren des AGPM-Clients</span><span class="sxs-lookup"><span data-stu-id="8c305-192">Step 2: Install AGPM Client</span></span>

<span data-ttu-id="8c305-193">Jeder Gruppenrichtlinienadministrator – jeder, der GPOs erstellt, bearbeitet, bereitstellt, überprüft oder löscht, muss AGPM-Client auf Computern installiert haben, die Sie zum Verwalten von GPOs verwenden.</span><span class="sxs-lookup"><span data-stu-id="8c305-193">Each Group Policy administrator—anyone who creates, edits, deploys, reviews, or deletes GPOs—must have AGPM Client installed on computers that they use to manage GPOs.</span></span> <span data-ttu-id="8c305-194">In diesem Szenario installieren Sie AGPM-Client auf mindestens einem Computer.</span><span class="sxs-lookup"><span data-stu-id="8c305-194">For this scenario, you install AGPM Client on at least one computer.</span></span> <span data-ttu-id="8c305-195">Sie müssen den AGPM-Client nicht auf den Computern von Endbenutzern installieren, die keine Gruppenrichtlinienverwaltung durchführen.</span><span class="sxs-lookup"><span data-stu-id="8c305-195">You do not need to install AGPM Client on the computers of end users who do not perform Group Policy administration.</span></span>

**<span data-ttu-id="8c305-196">So installieren Sie den AGPM-Client auf dem Computer eines Gruppenrichtlinienadministrators</span><span class="sxs-lookup"><span data-stu-id="8c305-196">To install AGPM Client on the computer of a Group Policy administrator</span></span>**

1.  <span data-ttu-id="8c305-197">Starten Sie die Microsoft Desktop Optimization Pack-CD, und folgen Sie den Anweisungen auf dem Bildschirm, um **Erweiterte Gruppenrichtlinienverwaltung-Client**auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="8c305-197">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Client**.</span></span>

2.  <span data-ttu-id="8c305-198">Klicken Sie im Dialogfeld **Willkommen** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="8c305-198">In the **Welcome** dialog box, click **Next**.</span></span>

3.  <span data-ttu-id="8c305-199">Akzeptieren Sie im Dialogfeld **Microsoft-Software-Lizenzbestimmungen** die Begriffe, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="8c305-199">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

4.  <span data-ttu-id="8c305-200">Wählen Sie im Dialogfeld **Anwendungspfad** einen Speicherort aus, an dem AGPM-Client installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c305-200">In the **Application Path** dialog box, select a location in which to install AGPM Client.</span></span> <span data-ttu-id="8c305-201">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="8c305-201">Click **Next**.</span></span>

5.  <span data-ttu-id="8c305-202">Geben Sie im Dialogfeld **AGPM-Server** den vollqualifizierten Computernamen für den AGPM-Server und den Port ein, mit dem die Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c305-202">In the **AGPM Server** dialog box, type the fully-qualified computer name for the AGPM Server and the port to which to connect.</span></span> <span data-ttu-id="8c305-203">Der Standardport für den AGPM-Dienst ist 4600.</span><span class="sxs-lookup"><span data-stu-id="8c305-203">The default port for the AGPM Service is 4600.</span></span> <span data-ttu-id="8c305-204">Deaktivieren Sie das Kontrollkästchen **Microsoft Management Console über das Firewall zulassen** , es sei denn, Sie konfigurieren Portausnahmen manuell oder verwenden Regeln, um Portausnahmen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8c305-204">Do not clear the **Allow Microsoft Management Console through the firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="8c305-205">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="8c305-205">Click **Next**.</span></span>

6.  <span data-ttu-id="8c305-206">Wählen Sie im Dialogfeld **Sprachen** eine oder mehrere Anzeigesprachen aus, die für AGPM-Client installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8c305-206">In the **Languages** dialog box, select one or more display languages to install for AGPM Client.</span></span>

7.  <span data-ttu-id="8c305-207">Klicken Sie auf **Installieren**, und klicken Sie dann auf **Fertig stellen** , um den Setup-Assistenten zu beenden.</span><span class="sxs-lookup"><span data-stu-id="8c305-207">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

### <a href="" id="bkmk-config3"></a><span data-ttu-id="8c305-208">Schritt 3: Konfigurieren einer AGPM-Server Verbindung</span><span class="sxs-lookup"><span data-stu-id="8c305-208">Step 3: Configure an AGPM Server connection</span></span>

<span data-ttu-id="8c305-209">AGPM speichert alle Versionen der einzelnen gesteuerten Gruppenrichtlinienobjekte (GPO) – ein GPO, für das AGPM das Änderungs Steuerelement bereitstellt – in einem zentralen Archiv, sodass Gruppenrichtlinienadministratoren GPOs offline anzeigen und ändern können, ohne dass sich dies unmittelbar auf die bereitgestellte Version jedes GPO auswirkt.</span><span class="sxs-lookup"><span data-stu-id="8c305-209">AGPM stores all versions of each controlled Group Policy object (GPO)—a GPO for which AGPM provides change control—in a central archive, so Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="8c305-210">In diesem Schritt konfigurieren Sie eine AGPM-Serververbindung und stellen sicher, dass alle Gruppenrichtlinienadministratoren eine Verbindung mit dem gleichen AGPM-Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="8c305-210">In this step, you configure an AGPM Server connection and ensure that all Group Policy administrators connect to the same AGPM Server.</span></span> <span data-ttu-id="8c305-211">(Informationen zum Konfigurieren mehrerer AGPM-Server finden Sie unter Hilfe zur erweiterten Gruppenrichtlinienverwaltung.)</span><span class="sxs-lookup"><span data-stu-id="8c305-211">(For information about configuring multiple AGPM Servers, see Help for Advanced Group Policy Management.)</span></span>

**<span data-ttu-id="8c305-212">So konfigurieren Sie eine AGPM-Server Verbindung für alle Gruppenrichtlinienadministratoren</span><span class="sxs-lookup"><span data-stu-id="8c305-212">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="8c305-213">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit dem Benutzerkonto an, das Sie als Archiv Besitzer ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="8c305-213">On a computer on which you have installed AGPM Client, log on with the user account that you selected as the Archive Owner.</span></span> <span data-ttu-id="8c305-214">Dieser Benutzer hat die Rolle des AGPM-Administrators (Vollzugriff).</span><span class="sxs-lookup"><span data-stu-id="8c305-214">This user has the role of AGPM Administrator (Full Control).</span></span>

2.  <span data-ttu-id="8c305-215">Klicken Sie auf **Start**, zeigen Sie auf **Verwaltung**, und klicken Sie auf **Gruppenrichtlinienverwaltung** , um die GPMC zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8c305-215">Click **Start**, point to **Administrative Tools**, and click **Group Policy Management** to open the GPMC.</span></span>

3.  <span data-ttu-id="8c305-216">Bearbeiten Sie ein Gruppenrichtlinienobjekt, das auf alle Gruppenrichtlinienadministratoren angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c305-216">Edit a GPO that is applied to all Group Policy administrators.</span></span>

4.  <span data-ttu-id="8c305-217">Doppelklicken Sie im Fenster **Gruppenrichtlinien-Verwaltungs-Editor** auf **Benutzerkonfiguration**, **Richtlinien**, **Administrative Vorlagen**, **Windows-Komponenten**und **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="8c305-217">In the **Group Policy Management Editor** window, double-click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

5.  <span data-ttu-id="8c305-218">Doppelklicken Sie im Detailbereich auf **AGPM: standardmäßiger AGPM-Server (alle Domänen) angeben**.</span><span class="sxs-lookup"><span data-stu-id="8c305-218">In the details pane, double-click **AGPM: Specify default AGPM Server (all domains)**.</span></span>

6.  <span data-ttu-id="8c305-219">Wählen Sie im **Eigenschaften** Fenster die Option **aktiviert** aus, und geben Sie den vollqualifizierten Computernamen und-Port (beispielsweise **Server.contoso.com:4600**) für den Server ein, der das Archiv hostet.</span><span class="sxs-lookup"><span data-stu-id="8c305-219">In the **Properties** window, select **Enabled** and type the fully-qualified computer name and port (for example, **server.contoso.com:4600**) for the server hosting the archive.</span></span> <span data-ttu-id="8c305-220">Standardmäßig verwendet der AGPM-Dienst Port 4600.</span><span class="sxs-lookup"><span data-stu-id="8c305-220">By default, the AGPM Service uses port 4600.</span></span>

7.  <span data-ttu-id="8c305-221">Klicken Sie auf **OK**, und schließen Sie dann das Fenster **Gruppenrichtlinien-Verwaltungs-Editor** .</span><span class="sxs-lookup"><span data-stu-id="8c305-221">Click **OK**, and then close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="8c305-222">Wenn die Gruppenrichtlinie aktualisiert wird, wird die AGPM-Server Verbindung für jeden Gruppenrichtlinienadministrator konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="8c305-222">When Group Policy is updated, the AGPM Server connection is configured for each Group Policy administrator.</span></span>

### <a href="" id="bkmk-config4"></a><span data-ttu-id="8c305-223">Schritt 4: Konfigurieren einer e-Mail-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="8c305-223">Step 4: Configure e-mail notification</span></span>

<span data-ttu-id="8c305-224">Als AGPM-Administrator (Vollzugriff) legen Sie die e-Mail-Adressen von Genehmigern und AGPM-Administratoren fest, denen eine e-Mail-Nachricht mit einer Anforderung gesendet wird, wenn ein Editor versucht, ein GPO zu erstellen, bereitzustellen oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="8c305-224">As an AGPM Administrator (Full Control), you designate the e-mail addresses of Approvers and AGPM Administrators to whom an e-mail message containing a request is sent when an Editor attempts to create, deploy, or delete a GPO.</span></span> <span data-ttu-id="8c305-225">Darüber hinaus ermitteln Sie den Alias, aus dem diese Nachrichten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c305-225">You also determine the alias from which these messages are sent.</span></span>

**<span data-ttu-id="8c305-226">So konfigurieren Sie die e-Mail-Benachrichtigung für AGPM</span><span class="sxs-lookup"><span data-stu-id="8c305-226">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="8c305-227">Klicken Sie im Detailbereich auf die Registerkarte **Domänendelegierung** .</span><span class="sxs-lookup"><span data-stu-id="8c305-227">In the details pane, click the **Domain Delegation** tab.</span></span>

2.  <span data-ttu-id="8c305-228">Geben Sie im Feld **von e-Mail-Adresse** den e-Mail-Alias für AGPM ein, aus dem Benachrichtigungen gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8c305-228">In the **From e-mail address** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

3.  <span data-ttu-id="8c305-229">Geben Sie im Feld **an e-Mail-Adresse** die e-Mail-Adresse für das Benutzerkonto ein, dem Sie die genehmigende Rolle zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="8c305-229">In the **To e-mail address** field, type the e-mail address for the user account to which you intend to assign the Approver role.</span></span>

4.  <span data-ttu-id="8c305-230">Geben Sie im Feld **SMTP-Server** einen gültigen SMTP-e-Mail-Server ein.</span><span class="sxs-lookup"><span data-stu-id="8c305-230">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

5.  <span data-ttu-id="8c305-231">Geben Sie in den Feldern **Benutzername** und **Kennwort** die Anmeldeinformationen eines Benutzers mit Zugriff auf den SMTP-Dienst ein.</span><span class="sxs-lookup"><span data-stu-id="8c305-231">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span> <span data-ttu-id="8c305-232">Klicken Sie auf **Übernehmen**.</span><span class="sxs-lookup"><span data-stu-id="8c305-232">Click **Apply**.</span></span>

### <a href="" id="bkmk-config5"></a><span data-ttu-id="8c305-233">Schritt 5: Delegieren des Zugriffs</span><span class="sxs-lookup"><span data-stu-id="8c305-233">Step 5: Delegate access</span></span>

<span data-ttu-id="8c305-234">Als AGPM-Administrator (Vollzugriff) delegieren Sie den Zugriff auf Gruppenrichtlinienobjekte auf Domänenebene, wobei dem Konto jedes Gruppenrichtlinienadministrators Rollen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="8c305-234">As an AGPM Administrator (Full Control), you delegate domain-level access to GPOs, assigning roles to the account of each Group Policy administrator.</span></span>

<span data-ttu-id="8c305-235">**Hinweis**  Sie können den Zugriff auch auf der GPO-Ebene und nicht auf der Domänenebene delegieren.</span><span class="sxs-lookup"><span data-stu-id="8c305-235">**Note** You can also delegate access at the GPO level rather than the domain level.</span></span> <span data-ttu-id="8c305-236">Ausführliche Informationen finden Sie unter Hilfe zur erweiterten Gruppenrichtlinienverwaltung.</span><span class="sxs-lookup"><span data-stu-id="8c305-236">For details, see Help for Advanced Group Policy Management.</span></span>

 

<span data-ttu-id="8c305-237">**Wichtig**  Sie sollten die Mitgliedschaft in der Gruppe der Gruppenrichtlinien Ersteller-Besitzer einschränken, damit Sie nicht dazu verwendet werden kann, die AGPM-Verwaltung des Zugriffs auf GPOs zu umgehen.</span><span class="sxs-lookup"><span data-stu-id="8c305-237">**Important** You should restrict membership in the Group Policy Creator Owners group, so it cannot be used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="8c305-238">(Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gruppenrichtlinienobjekte** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, klicken Sie auf **Delegierung**, und konfigurieren Sie dann die Einstellungen, um die Anforderungen Ihrer Organisation zu erfüllen.)</span><span class="sxs-lookup"><span data-stu-id="8c305-238">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

 

**<span data-ttu-id="8c305-239">So delegieren Sie den Zugriff auf alle GPOs in einer Domäne</span><span class="sxs-lookup"><span data-stu-id="8c305-239">To delegate access to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="8c305-240">Klicken Sie auf der Registerkarte **Domänendelegierung** auf die Schaltfläche **Hinzufügen** , wählen Sie das Benutzerkonto des Gruppenrichtlinienadministrators aus, das als genehmigende Person fungieren soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c305-240">On the **Domain Delegation** tab, click the **Add** button, select the user account of the Group Policy administrator to serve as Approver, and then click **OK**.</span></span>

2.  <span data-ttu-id="8c305-241">Wählen Sie im Dialogfeld **Gruppe oder Benutzer hinzufügen** die Rolle **genehmigende Person** aus, um diese Rolle dem Konto zuzuweisen, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c305-241">In the **Add Group or User** dialog box, select the **Approver** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="8c305-242">(Diese Rolle umfasst die Rolle Prüfer.)</span><span class="sxs-lookup"><span data-stu-id="8c305-242">(This role includes the Reviewer role.)</span></span>

3.  <span data-ttu-id="8c305-243">Klicken Sie auf die Schaltfläche **Hinzufügen** , wählen Sie das Benutzerkonto des Gruppenrichtlinienadministrators aus, das als Editor fungieren soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c305-243">Click the **Add** button, select the user account of the Group Policy administrator to serve as Editor, and then click **OK**.</span></span>

4.  <span data-ttu-id="8c305-244">Wählen Sie im Dialogfeld **Gruppe oder Benutzer hinzufügen** die **Editor** Rolle aus, um diese Rolle dem Konto zuzuweisen, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c305-244">In the **Add Group or User** dialog box, select the **Editor** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="8c305-245">(Diese Rolle umfasst die Rolle Prüfer.)</span><span class="sxs-lookup"><span data-stu-id="8c305-245">(This role includes the Reviewer role.)</span></span>

5.  <span data-ttu-id="8c305-246">Klicken Sie auf die Schaltfläche **Hinzufügen** , wählen Sie das Benutzerkonto des Gruppenrichtlinienadministrators aus, das als Bearbeiter fungieren soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c305-246">Click the **Add** button, select the user account of the Group Policy administrator to serve as Reviewer, and then click **OK**.</span></span>

6.  <span data-ttu-id="8c305-247">Wählen Sie im Dialogfeld **Gruppe oder Benutzer hinzufügen** die Rolle **Prüfer** aus, um dem Konto nur diese Rolle zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="8c305-247">In the **Add Group or User** dialog box, select the **Reviewer** role to assign only that role to the account.</span></span>

## <span data-ttu-id="8c305-248">Schritte zum Verwalten von GPOs</span><span class="sxs-lookup"><span data-stu-id="8c305-248">Steps for managing GPOs</span></span>


<span data-ttu-id="8c305-249">Sie müssen die folgenden Schritte ausführen, um GPOs mithilfe von AGPM zu erstellen, zu bearbeiten, zu überprüfen und bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8c305-249">You must complete the following steps to create, edit, review, and deploy GPOs using AGPM.</span></span> <span data-ttu-id="8c305-250">Darüber hinaus erstellen Sie eine Vorlage, löschen ein GPO und Wiederherstellen eines gelöschten Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="8c305-250">Additionally, you will create a template, delete a GPO, and restore a deleted GPO.</span></span>

[<span data-ttu-id="8c305-251">Schritt 1: Erstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="8c305-251">Step 1: Create a GPO</span></span>](#bkmk-manage1)

[<span data-ttu-id="8c305-252">Schritt 2: Bearbeiten eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="8c305-252">Step 2: Edit a GPO</span></span>](#bkmk-manage2)

[<span data-ttu-id="8c305-253">Schritt 3: überprüfen und Bereitstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="8c305-253">Step 3: Review and deploy a GPO</span></span>](#bkmk-manage3)

[<span data-ttu-id="8c305-254">Schritt 4: Verwenden einer Vorlage zum Erstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="8c305-254">Step 4: Use a template to create a GPO</span></span>](#bkmk-manage4)

[<span data-ttu-id="8c305-255">Schritt 5: Löschen und Wiederherstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="8c305-255">Step 5: Delete and restore a GPO</span></span>](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a><span data-ttu-id="8c305-256">Schritt 1: Erstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="8c305-256">Step 1: Create a GPO</span></span>

<span data-ttu-id="8c305-257">In einer Umgebung mit mehreren Gruppenrichtlinienadministratoren können Personen, die die Rolle des Editors besitzen, die Erstellung neuer GPOs anfordern, doch eine solche Anforderung muss von einer Person mit der Rolle Genehmiger genehmigt werden, da sich die Erstellung eines neuen Gruppenrichtlinienobjekts auf die Produktionsumgebung auswirkt.</span><span class="sxs-lookup"><span data-stu-id="8c305-257">In an environment with multiple Group Policy administrators, those with the Editor role have the ability to request the creation of new GPOs, but such a request must be approved by someone with the Approver role because the creation of a new GPO impacts the production environment.</span></span>

<span data-ttu-id="8c305-258">In diesem Schritt verwenden Sie ein Konto mit der Rolle "Editor", um die Erstellung eines neuen Gruppenrichtlinienobjekts anzufordern.</span><span class="sxs-lookup"><span data-stu-id="8c305-258">In this step, you use an account with the Editor role to request the creation of a new GPO.</span></span> <span data-ttu-id="8c305-259">Wenn Sie ein Konto mit der Rolle Genehmiger verwenden, genehmigen Sie diese Anforderung und schließen die Erstellung eines Gruppenrichtlinienobjekts ab.</span><span class="sxs-lookup"><span data-stu-id="8c305-259">Using an account with the Approver role, you approve this request and complete the creation of a GPO.</span></span>

**<span data-ttu-id="8c305-260">So fordern Sie die Erstellung eines über AGPM verwalteten neuen Gruppenrichtlinienobjekts an</span><span class="sxs-lookup"><span data-stu-id="8c305-260">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="8c305-261">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle des Editors in AGPM zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="8c305-261">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the Editor role in AGPM.</span></span>

2.  <span data-ttu-id="8c305-262">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="8c305-262">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="8c305-263">Klicken Sie mit der rechten Maustaste auf den Knoten **Change Control** , und klicken Sie dann auf **Neues gesteuertes Gruppenrichtlinienobjekt**.</span><span class="sxs-lookup"><span data-stu-id="8c305-263">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

4.  <span data-ttu-id="8c305-264">Im Dialogfeld " **Neues gesteuertes GPO** ":</span><span class="sxs-lookup"><span data-stu-id="8c305-264">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="8c305-265">Wenn Sie eine Kopie der Anfrage erhalten möchten, geben Sie Ihre e-Mail-Adresse in das Feld **CC** ein.</span><span class="sxs-lookup"><span data-stu-id="8c305-265">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="8c305-266">Geben Sie **eigenes** als Namen für das neue Gruppenrichtlinienobjekt ein.</span><span class="sxs-lookup"><span data-stu-id="8c305-266">Type **MyGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="8c305-267">Geben Sie einen Kommentar für das neue Gruppenrichtlinienobjekt ein.</span><span class="sxs-lookup"><span data-stu-id="8c305-267">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="8c305-268">Klicken Sie auf **Live erstellen** , damit das neue Gruppenrichtlinienobjekt unmittelbar nach der Genehmigung in der Produktionsumgebung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8c305-268">Click **Create live** so the new GPO will be deployed to the production environment immediately upon approval.</span></span> <span data-ttu-id="8c305-269">Klicken Sie auf **Übermitteln**.</span><span class="sxs-lookup"><span data-stu-id="8c305-269">Click **Submit**.</span></span>

5.  <span data-ttu-id="8c305-270">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="8c305-270">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8c305-271">Das neue Gruppenrichtlinienobjekt wird auf der Registerkarte **Ausstehend** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c305-271">The new GPO is displayed on the **Pending** tab.</span></span>

**<span data-ttu-id="8c305-272">So genehmigen Sie die ausstehende Anforderung zum Erstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="8c305-272">To approve the pending request to create a GPO</span></span>**

1.  <span data-ttu-id="8c305-273">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle der genehmigenden Person in AGPM zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="8c305-273">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span>

2.  <span data-ttu-id="8c305-274">Öffnen Sie den e-Mail-Posteingang für das Konto, und beachten Sie, dass Sie eine e-Mail-Nachricht vom AGPM-Alias mit der Anforderung des Editors zum Erstellen eines Gruppenrichtlinienobjekts erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="8c305-274">Open the e-mail inbox for the account, and note that you have received an e-mail message from the AGPM alias with the Editor's request to create a GPO.</span></span>

3.  <span data-ttu-id="8c305-275">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="8c305-275">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="8c305-276">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **Ausstehend** , um die ausstehenden GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8c305-276">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

5.  <span data-ttu-id="8c305-277">Klicken Sie mit der rechten Maustaste auf **eigenes**, und klicken Sie dann auf **genehmigen**.</span><span class="sxs-lookup"><span data-stu-id="8c305-277">Right-click **MyGPO**, and then click **Approve**.</span></span>

6.  <span data-ttu-id="8c305-278">Klicken Sie auf **Ja** , um die Genehmigung für die Erstellung des Gruppenrichtlinienobjekts zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="8c305-278">Click **Yes** to confirm approval of the creation of the GPO.</span></span> <span data-ttu-id="8c305-279">Das Gruppenrichtlinienobjekt wird auf die Registerkarte **gesteuert** verschoben.</span><span class="sxs-lookup"><span data-stu-id="8c305-279">The GPO is moved to the **Controlled** tab.</span></span>

### <a href="" id="bkmk-manage2"></a><span data-ttu-id="8c305-280">Schritt 2: Bearbeiten eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="8c305-280">Step 2: Edit a GPO</span></span>

<span data-ttu-id="8c305-281">Sie können GPOs verwenden, um Computer-oder Benutzereinstellungen zu konfigurieren und für viele Computer oder Benutzer bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8c305-281">You can use GPOs to configure computer or user settings and deploy them to many computers or users.</span></span> <span data-ttu-id="8c305-282">In diesem Schritt verwenden Sie ein Konto mit der Rolle "Editor", um ein GPO aus dem Archiv auszuchecken, das Gruppenrichtlinienobjekt offline zu bearbeiten, das bearbeitete GPO in das Archiv zu überprüfen und die Bereitstellung des Gruppenrichtlinienobjekts in der Produktionsumgebung anzufordern.</span><span class="sxs-lookup"><span data-stu-id="8c305-282">In this step, you use an account with the Editor role to check out a GPO from the archive, edit the GPO offline, check the edited GPO into the archive, and request deployment of the GPO to the production environment.</span></span> <span data-ttu-id="8c305-283">In diesem Szenario konfigurieren Sie eine Einstellung im Gruppenrichtlinienobjekt, um zu erzwingen, dass das Kennwort mindestens acht Zeichen lang sein muss.</span><span class="sxs-lookup"><span data-stu-id="8c305-283">For this scenario, you configure a setting in the GPO to require that the password be at least eight characters in length.</span></span>

**<span data-ttu-id="8c305-284">So überprüfen Sie das Gruppenrichtlinienobjekt aus dem Archiv zur Bearbeitung</span><span class="sxs-lookup"><span data-stu-id="8c305-284">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="8c305-285">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle des Editors in AGPM zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="8c305-285">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="8c305-286">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="8c305-286">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="8c305-287">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8c305-287">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="8c305-288">Klicken Sie mit der rechten Maustaste auf **eigenes**, und klicken Sie dann auf **Auschecken**.</span><span class="sxs-lookup"><span data-stu-id="8c305-288">Right-click **MyGPO**, and then click **Check Out**.</span></span>

5.  <span data-ttu-id="8c305-289">Geben Sie einen Kommentar ein, der im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, während es ausgecheckt ist, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c305-289">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

6.  <span data-ttu-id="8c305-290">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="8c305-290">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8c305-291">Auf der Registerkarte **gesteuert** wird der Status des Gruppenrichtlinienobjekts als **ausgecheckt**identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8c305-291">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="8c305-292">So bearbeiten Sie das Gruppenrichtlinienobjekt offline und konfigurieren die minimale Kennwortlänge</span><span class="sxs-lookup"><span data-stu-id="8c305-292">To edit the GPO offline and configure the minimum password length</span></span>**

1.  <span data-ttu-id="8c305-293">Klicken Sie auf der Registerkarte **gesteuert** mit der rechten Maustaste auf **eigenes**, und klicken Sie dann auf **Bearbeiten** , um das Fenster **Gruppenrichtlinien-Verwaltungs-Editor** zu öffnen und Änderungen an einer Offlinekopie des Gruppenrichtlinienobjekts vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="8c305-293">On the **Controlled** tab, right-click **MyGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="8c305-294">Konfigurieren Sie in diesem Szenario die minimale Kennwortlänge:</span><span class="sxs-lookup"><span data-stu-id="8c305-294">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="8c305-295">Doppelklicken Sie unter **Computer Konfiguration**auf **Richtlinien**, **Windows-Einstellungen**, **Sicherheitseinstellungen**, **Kontorichtlinien**und **Kennwortrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="8c305-295">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Password Policy**.</span></span>

    2.  <span data-ttu-id="8c305-296">Doppelklicken Sie im Detailbereich auf **minimale Kennwortlänge**.</span><span class="sxs-lookup"><span data-stu-id="8c305-296">In the details pane, double-click **Minimum password length**.</span></span>

    3.  <span data-ttu-id="8c305-297">Aktivieren Sie im Eigenschaftenfenster das Kontrollkästchen **diese Richtlinieneinstellung definieren** , legen Sie die Anzahl der Zeichen auf **8**fest, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c305-297">In the properties window, select the **Define this policy setting** check box, set the number of characters to **8**, and then click **OK**.</span></span>

2.  <span data-ttu-id="8c305-298">Schließen Sie das Fenster **Gruppenrichtlinien-Verwaltungs-Editor** .</span><span class="sxs-lookup"><span data-stu-id="8c305-298">Close the **Group Policy Management Editor** window.</span></span>

**<span data-ttu-id="8c305-299">So überprüfen Sie das Gruppenrichtlinienobjekt in das Archiv</span><span class="sxs-lookup"><span data-stu-id="8c305-299">To check the GPO into the archive</span></span>**

1.  <span data-ttu-id="8c305-300">Klicken Sie auf der Registerkarte **gesteuert** mit der rechten Maustaste auf **eigenes** , und klicken Sie dann auf **Einchecken**.</span><span class="sxs-lookup"><span data-stu-id="8c305-300">On the **Controlled** tab, right-click **MyGPO** and then click **Check In**.</span></span>

2.  <span data-ttu-id="8c305-301">Geben Sie einen Kommentar ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c305-301">Type a comment, and then click **OK**.</span></span>

3.  <span data-ttu-id="8c305-302">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="8c305-302">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8c305-303">Auf der Registerkarte **gesteuert** wird der Status des Gruppenrichtlinienobjekts als **eingecheckt**gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8c305-303">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

**<span data-ttu-id="8c305-304">So fordern Sie die Bereitstellung des Gruppenrichtlinienobjekts in der Produktionsumgebung an</span><span class="sxs-lookup"><span data-stu-id="8c305-304">To request the deployment of the GPO to the production environment</span></span>**

1.  <span data-ttu-id="8c305-305">Klicken Sie auf der Registerkarte **gesteuert** mit der rechten Maustaste auf **eigenes** , und klicken Sie dann auf **Bereitstellen**.</span><span class="sxs-lookup"><span data-stu-id="8c305-305">On the **Controlled** tab, right-click **MyGPO** and then click **Deploy**.</span></span>

2.  <span data-ttu-id="8c305-306">Da es sich bei diesem Konto nicht um eine genehmigende Person oder einen AGPM-Administrator handelt, müssen Sie eine Anforderung für die Bereitstellung einreichen.</span><span class="sxs-lookup"><span data-stu-id="8c305-306">Because this account is not an Approver or AGPM Administrator, you must submit a request for deployment.</span></span> <span data-ttu-id="8c305-307">Wenn Sie eine Kopie der Anfrage erhalten möchten, geben Sie Ihre e-Mail-Adresse in das Feld **CC** ein.</span><span class="sxs-lookup"><span data-stu-id="8c305-307">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="8c305-308">Geben Sie einen Kommentar ein, der im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **Absenden**.</span><span class="sxs-lookup"><span data-stu-id="8c305-308">Type a comment to be displayed in the history of the GPO, and then click **Submit**.</span></span>

3.  <span data-ttu-id="8c305-309">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="8c305-309">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8c305-310">**Eigenes** wird in der Liste der GPOs auf der Registerkarte **Ausstehend** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c305-310">**MyGPO** is displayed on the list of GPOs on the **Pending** tab.</span></span>

### <a href="" id="bkmk-manage3"></a><span data-ttu-id="8c305-311">Schritt 3: überprüfen und Bereitstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="8c305-311">Step 3: Review and deploy a GPO</span></span>

<span data-ttu-id="8c305-312">In diesem Schritt fungieren Sie als genehmigende Person, erstellen Berichte und analysieren die Einstellungen und Änderungen an den Einstellungen im Gruppenrichtlinienobjekt, um festzustellen, ob Sie diese genehmigen sollten.</span><span class="sxs-lookup"><span data-stu-id="8c305-312">In this step, you act as an Approver, creating reports and analyzing the settings and changes to settings in the GPO to determine whether you should approve them.</span></span> <span data-ttu-id="8c305-313">Nachdem Sie das Gruppenrichtlinienobjekt ausgewertet haben, stellen Sie es in der Produktionsumgebung bereit, und verknüpfen Sie es mit einer Domäne oder einer Organisationseinheit, damit es wirksam wird, wenn die Gruppenrichtlinie für Computer in dieser Domäne oder OU aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="8c305-313">After evaluating the GPO, you deploy it to the production environment and link it to a domain or an organizational unit (OU) so that it takes effect when Group Policy is refreshed for computers in that domain or OU.</span></span>

**<span data-ttu-id="8c305-314">So überprüfen Sie die Einstellungen im Gruppenrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="8c305-314">To review settings in the GPO</span></span>**

1. <span data-ttu-id="8c305-315">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle der genehmigenden Person in AGPM zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="8c305-315">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span> <span data-ttu-id="8c305-316">(Jeder Gruppenrichtlinienadministrator mit der Rolle Prüfer, der in allen anderen Rollen enthalten ist, kann die Einstellungen in einem Gruppenrichtlinienobjekt überprüfen.)</span><span class="sxs-lookup"><span data-stu-id="8c305-316">(Any Group Policy administrator with the Reviewer role, which is included in all of the other roles, can review the settings in a GPO.)</span></span>

2. <span data-ttu-id="8c305-317">Öffnen Sie den e-Mail-Posteingang für das Konto, und beachten Sie, dass Sie eine e-Mail-Nachricht vom AGPM-Alias mit der Anforderung eines Editors zum Bereitstellen eines Gruppenrichtlinienobjekts erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="8c305-317">Open the e-mail inbox for the account and note that you have received an e-mail message from the AGPM alias with an Editor's request to deploy a GPO.</span></span>

3. <span data-ttu-id="8c305-318">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="8c305-318">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4. <span data-ttu-id="8c305-319">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **Ausstehend** .</span><span class="sxs-lookup"><span data-stu-id="8c305-319">On the **Contents** tab in the details pane, click the **Pending** tab.</span></span>

5. <span data-ttu-id="8c305-320">Doppelklicken Sie auf **eigenes** , um dessen Verlauf anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8c305-320">Double-click **MyGPO** to display its history.</span></span>

6. <span data-ttu-id="8c305-321">Überprüfen Sie die Einstellungen in der neuesten Version von eigenes:</span><span class="sxs-lookup"><span data-stu-id="8c305-321">Review the settings in the most recent version of MyGPO:</span></span>

   1.  <span data-ttu-id="8c305-322">Klicken Sie im **Verlaufs** Fenster mit der rechten Maustaste auf die GPO-Version mit dem neuesten Zeitstempel, klicken Sie auf **Einstellungen**, und klicken Sie dann auf **HTML-Bericht** , um eine Zusammenfassung der GPO-Einstellungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8c305-322">In the **History** window, right-click the GPO version with the most recent timestamp, click **Settings**, and then click **HTML Report** to display a summary of the GPO's settings.</span></span>

   2.  <span data-ttu-id="8c305-323">Klicken Sie im Webbrowser auf **Alle anzeigen** , um alle Einstellungen im Gruppenrichtlinienobjekt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8c305-323">In the Web browser, click **show all** to display all of the settings in the GPO.</span></span> <span data-ttu-id="8c305-324">Schließen Sie den Browser.</span><span class="sxs-lookup"><span data-stu-id="8c305-324">Close the browser.</span></span>

7. <span data-ttu-id="8c305-325">Vergleichen Sie die neueste Version von eigenes mit der ersten Version, die in das Archiv eingecheckt wurde:</span><span class="sxs-lookup"><span data-stu-id="8c305-325">Compare the most recent version of MyGPO to the first version checked in to the archive:</span></span>

   1. <span data-ttu-id="8c305-326">Klicken Sie im Fenster " **Verlauf** " auf die GPO-Version mit dem letzten Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="8c305-326">In the **History** window, click the GPO version with the most recent time stamp.</span></span> <span data-ttu-id="8c305-327">Drücken Sie STRG, und klicken Sie auf die älteste GPO-Version, für die die **Computer Version** nicht \* \* \ \ \* \* \* ist.</span><span class="sxs-lookup"><span data-stu-id="8c305-327">Press CTRL and click the oldest GPO version for which the **Computer Version** is not \*\*\\*\*\*.</span></span>

   2. <span data-ttu-id="8c305-328">Klicken Sie auf die Schaltfläche **Unterschiede** .</span><span class="sxs-lookup"><span data-stu-id="8c305-328">Click the **Differences** button.</span></span> <span data-ttu-id="8c305-329">Der Abschnitt **Kontorichtlinien/Kennwortrichtlinie** ist grün hervorgehoben und wird mit **\ [+ \]** vorangestellt, was darauf hinweist, dass diese Einstellung nur in der letzten Version des Gruppenrichtlinienobjekts konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="8c305-329">The **Account Policies/Password Policy** section is highlighted in green and preceded by **\[+\]**, indicating that this setting is configured only in the latter version of the GPO.</span></span>

   3. <span data-ttu-id="8c305-330">Klicken Sie auf **Kontorichtlinien/Kennwortrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="8c305-330">Click **Account Policies/Password Policy**.</span></span> <span data-ttu-id="8c305-331">Die Einstellung **minimale Kennwortlänge** ist auch in grün hervorgehoben und mit **\ [+ \]** gekennzeichnet, was darauf hinweist, dass Sie nur in der letzten Version des Gruppenrichtlinienobjekts konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="8c305-331">The **Minimum password length** setting is also highlighted in green and preceded by **\[+\]**, indicating that it is configured only in the latter version of the GPO.</span></span>

   4. <span data-ttu-id="8c305-332">Schließen Sie den Webbrowser.</span><span class="sxs-lookup"><span data-stu-id="8c305-332">Close the Web browser.</span></span>

**<span data-ttu-id="8c305-333">So stellen Sie das Gruppenrichtlinienobjekt in der Produktionsumgebung bereit</span><span class="sxs-lookup"><span data-stu-id="8c305-333">To deploy the GPO to the production environment</span></span>**

1.  <span data-ttu-id="8c305-334">Klicken Sie auf der Registerkarte **Ausstehend** mit der rechten Maustaste auf **eigenes** , und klicken Sie dann auf **genehmigen**.</span><span class="sxs-lookup"><span data-stu-id="8c305-334">On the **Pending** tab, right-click **MyGPO** and then click **Approve**.</span></span>

2.  <span data-ttu-id="8c305-335">Geben Sie einen Kommentar ein, der in das Protokoll des Gruppenrichtlinienobjekts aufgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c305-335">Type a comment to include in the history of the GPO.</span></span>

3.  <span data-ttu-id="8c305-336">Klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8c305-336">Click **Yes**.</span></span> <span data-ttu-id="8c305-337">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="8c305-337">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8c305-338">Das Gruppenrichtlinienobjekt wird in der Produktionsumgebung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="8c305-338">The GPO is deployed to the production environment.</span></span>

**<span data-ttu-id="8c305-339">So verknüpfen Sie das Gruppenrichtlinienobjekt mit einer Domäne oder Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="8c305-339">To link the GPO to a domain or organizational unit</span></span>**

1.  <span data-ttu-id="8c305-340">Klicken Sie in der GPMC mit der rechten Maustaste auf die Domäne oder auf eine Organisationseinheit, auf die das von Ihnen konfigurierte Gruppenrichtlinienobjekt angewendet werden soll, und klicken Sie dann auf **vorhandenes Gruppenrichtlinienobjekt verknüpfen**.</span><span class="sxs-lookup"><span data-stu-id="8c305-340">In the GPMC, right-click the domain or an OU to which to apply the GPO that you configured, and then click **Link an Existing GPO**.</span></span>

2.  <span data-ttu-id="8c305-341">Klicken Sie im Dialogfeld **GPO auswählen** auf **eigenes**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c305-341">In the **Select GPO** dialog box, click **MyGPO**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage4"></a><span data-ttu-id="8c305-342">Schritt 4: Verwenden einer Vorlage zum Erstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="8c305-342">Step 4: Use a template to create a GPO</span></span>

<span data-ttu-id="8c305-343">In diesem Schritt verwenden Sie ein Konto mit der Rolle "Editor", um eine Vorlage zu erstellen – eine nicht bearbeitbare, statische Version eines GPO, die als Ausgangspunkt zum Erstellen neuer GPOs verwendet werden soll, und dann basierend auf dieser Vorlage ein neues Gruppenrichtlinienobjekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="8c305-343">In this step, you use an account with the Editor role to create a template—an uneditable, static version of a GPO for use as a starting point for creating new GPOs—and then create a new GPO based upon that template.</span></span> <span data-ttu-id="8c305-344">Vorlagen sind hilfreich für das schnelle Erstellen mehrerer GPOs, in denen viele der gleichen Einstellungen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="8c305-344">Templates are useful for quickly creating multiple GPOs that include many of the same settings.</span></span>

**<span data-ttu-id="8c305-345">So erstellen Sie eine Vorlage auf der Grundlage eines vorhandenen Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="8c305-345">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="8c305-346">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle des Editors in AGPM zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="8c305-346">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="8c305-347">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="8c305-347">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="8c305-348">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** .</span><span class="sxs-lookup"><span data-stu-id="8c305-348">On the **Contents** tab in the details pane, click the **Controlled** tab.</span></span>

4.  <span data-ttu-id="8c305-349">Klicken Sie mit der rechten Maustaste auf **eigenes**, und klicken Sie dann auf **als Vorlage speichern** , um eine Vorlage zu erstellen, die alle Einstellungen umfasst, die derzeit in eigenes enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="8c305-349">Right-click **MyGPO**, and then click **Save as Template** to create a template incorporating all settings currently in MyGPO.</span></span>

5.  <span data-ttu-id="8c305-350">Geben Sie **MyTemplate** als Namen für die Vorlage und einen Kommentar ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c305-350">Type **MyTemplate** as the name for the template and a comment, and then click **OK**.</span></span>

6.  <span data-ttu-id="8c305-351">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="8c305-351">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8c305-352">Die neue Vorlage wird auf der Registerkarte **Vorlagen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c305-352">The new template appears on the **Templates** tab.</span></span>

**<span data-ttu-id="8c305-353">So fordern Sie die Erstellung eines über AGPM verwalteten neuen Gruppenrichtlinienobjekts an</span><span class="sxs-lookup"><span data-stu-id="8c305-353">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="8c305-354">Klicken Sie auf die Registerkarte **gesteuert** .</span><span class="sxs-lookup"><span data-stu-id="8c305-354">Click the **Controlled** tab.</span></span>

2.  <span data-ttu-id="8c305-355">Klicken Sie mit der rechten Maustaste auf den Knoten **Change Control** , und klicken Sie dann auf **Neues gesteuertes Gruppenrichtlinienobjekt**.</span><span class="sxs-lookup"><span data-stu-id="8c305-355">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="8c305-356">Im Dialogfeld " **Neues gesteuertes GPO** ":</span><span class="sxs-lookup"><span data-stu-id="8c305-356">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="8c305-357">Wenn Sie eine Kopie der Anfrage erhalten möchten, geben Sie Ihre e-Mail-Adresse in das Feld **CC** ein.</span><span class="sxs-lookup"><span data-stu-id="8c305-357">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="8c305-358">Geben Sie **Gruppenrichtlinienverwaltungs** als Namen für das neue Gruppenrichtlinienobjekt ein.</span><span class="sxs-lookup"><span data-stu-id="8c305-358">Type **MyOtherGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="8c305-359">Geben Sie einen Kommentar für das neue Gruppenrichtlinienobjekt ein.</span><span class="sxs-lookup"><span data-stu-id="8c305-359">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="8c305-360">Klicken Sie auf **Live erstellen**, damit das neue Gruppenrichtlinienobjekt unmittelbar nach der Genehmigung in der Produktionsumgebung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8c305-360">Click **Create live**, so the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="8c305-361">Wählen Sie für **aus GPO-Vorlage**die Option meine **Vorlage**aus.</span><span class="sxs-lookup"><span data-stu-id="8c305-361">For **From GPO template**, select **MyTemplate**.</span></span> <span data-ttu-id="8c305-362">Klicken Sie auf **Übermitteln**.</span><span class="sxs-lookup"><span data-stu-id="8c305-362">Click **Submit**.</span></span>

4.  <span data-ttu-id="8c305-363">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="8c305-363">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8c305-364">Das neue Gruppenrichtlinienobjekt wird auf der Registerkarte **Ausstehend** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c305-364">The new GPO is displayed on the **Pending** tab.</span></span>

<span data-ttu-id="8c305-365">Verwenden Sie ein Konto, dem die Rolle der genehmigenden Person zugewiesen wurde, um die ausstehende Anforderung zum Erstellen des Gruppenrichtlinienobjekts zu genehmigen, wie in [Schritt 1: Erstellen eines Gruppenrichtlinienobjekts](#bkmk-manage1).</span><span class="sxs-lookup"><span data-stu-id="8c305-365">Use an account that has been assigned the role of Approver to approve the pending request to create the GPO as you did in [Step 1: Create a GPO](#bkmk-manage1).</span></span> <span data-ttu-id="8c305-366">MyTemplate enthält alle Einstellungen, die Sie in eigenes konfiguriert haben.</span><span class="sxs-lookup"><span data-stu-id="8c305-366">MyTemplate incorporates all of the settings that you configured in MyGPO.</span></span> <span data-ttu-id="8c305-367">Da Gruppenrichtlinienverwaltungs mit MyTemplate erstellt wurde, enthält es zunächst alle Einstellungen, die eigenes zum Zeitpunkt der Erstellung von MyTemplate enthielt.</span><span class="sxs-lookup"><span data-stu-id="8c305-367">Because MyOtherGPO was created using MyTemplate, it initially contains all of the settings that MyGPO contained at the time that MyTemplate was created.</span></span> <span data-ttu-id="8c305-368">Sie können dies bestätigen, indem Sie einen Differenz Bericht generieren, um Gruppenrichtlinienverwaltungs mit MyTemplate zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="8c305-368">You can confirm this by generating a difference report to compare MyOtherGPO to MyTemplate.</span></span>

**<span data-ttu-id="8c305-369">So überprüfen Sie das Gruppenrichtlinienobjekt aus dem Archiv zur Bearbeitung</span><span class="sxs-lookup"><span data-stu-id="8c305-369">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="8c305-370">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle des Editors in AGPM zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="8c305-370">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="8c305-371">Klicken Sie mit der rechten Maustaste auf **Gruppenrichtlinienverwaltungs**, und klicken Sie dann auf **Auschecken**.</span><span class="sxs-lookup"><span data-stu-id="8c305-371">Right-click **MyOtherGPO**, and then click **Check Out**.</span></span>

3.  <span data-ttu-id="8c305-372">Geben Sie einen Kommentar ein, der im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, während es ausgecheckt ist, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c305-372">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

4.  <span data-ttu-id="8c305-373">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="8c305-373">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8c305-374">Auf der Registerkarte **gesteuert** wird der Status des Gruppenrichtlinienobjekts als **ausgecheckt**identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8c305-374">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="8c305-375">So bearbeiten Sie das Gruppenrichtlinienobjekt offline und konfigurieren die Kontosperrungsdauer</span><span class="sxs-lookup"><span data-stu-id="8c305-375">To edit the GPO offline and configure the account lockout duration</span></span>**

1.  <span data-ttu-id="8c305-376">Klicken Sie auf der Registerkarte **gesteuert** mit der rechten Maustaste auf **Gruppenrichtlinienverwaltungs**, und klicken Sie dann auf **Bearbeiten** , um das Fenster **Gruppenrichtlinien-Verwaltungs-Editor** zu öffnen und Änderungen an einer Offlinekopie des Gruppenrichtlinienobjekts vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="8c305-376">On the **Controlled** tab, right-click **MyOtherGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="8c305-377">Konfigurieren Sie in diesem Szenario die minimale Kennwortlänge:</span><span class="sxs-lookup"><span data-stu-id="8c305-377">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="8c305-378">Doppelklicken Sie unter **Computer Konfiguration**auf **Richtlinien**, **Windows-Einstellungen**, **Sicherheitseinstellungen**, **Kontorichtlinien**und **Kontosperrungsrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="8c305-378">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Account Lockout Policy**.</span></span>

    2.  <span data-ttu-id="8c305-379">Doppelklicken Sie im Detailbereich auf **Kontosperrungsdauer**.</span><span class="sxs-lookup"><span data-stu-id="8c305-379">In the details pane, double-click **Account lockout duration**.</span></span>

    3.  <span data-ttu-id="8c305-380">Aktivieren Sie im Fenster Eigenschaften die Option **diese Richtlinieneinstellung definieren**, legen Sie die Dauer auf **30** Minuten fest, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c305-380">In the properties window, check **Define this policy setting**, set the duration to **30** minutes, and then click **OK**.</span></span>

2.  <span data-ttu-id="8c305-381">Schließen Sie das Fenster **Gruppenrichtlinien-Verwaltungs-Editor** .</span><span class="sxs-lookup"><span data-stu-id="8c305-381">Close the **Group Policy Management Editor** window.</span></span>

<span data-ttu-id="8c305-382">Überprüfen Sie Gruppenrichtlinienverwaltungs in die Archivierungs-und Anforderungs Bereitstellung wie bei eigenes in [Schritt 2: Bearbeiten eines Gruppenrichtlinienobjekts](#bkmk-manage2).</span><span class="sxs-lookup"><span data-stu-id="8c305-382">Check MyOtherGPO into the archive and request deployment as you did for MyGPO in [Step 2: Edit a GPO](#bkmk-manage2).</span></span> <span data-ttu-id="8c305-383">Sie können Gruppenrichtlinienverwaltungs mit eigenes oder mit MyTemplate mithilfe von Unterschiedsberichten vergleichen.</span><span class="sxs-lookup"><span data-stu-id="8c305-383">You can compare MyOtherGPO to MyGPO or to MyTemplate using difference reports.</span></span> <span data-ttu-id="8c305-384">Jedes Konto, das die Rolle Prüfer enthält (AGPM-Administrator \ [Vollzugriff \], genehmigende Person, Bearbeiter oder Bearbeiter) kann Berichte generieren.</span><span class="sxs-lookup"><span data-stu-id="8c305-384">Any account that includes the Reviewer role (AGPM Administrator \[Full Control\], Approver, Editor, or Reviewer) can generate reports.</span></span>

**<span data-ttu-id="8c305-385">So vergleichen Sie ein GPO mit einem anderen Gruppenrichtlinienobjekt und einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="8c305-385">To compare a GPO to another GPO and to a template</span></span>**

1.  <span data-ttu-id="8c305-386">So vergleichen Sie eigenes und Gruppenrichtlinienverwaltungs:</span><span class="sxs-lookup"><span data-stu-id="8c305-386">To compare MyGPO and MyOtherGPO:</span></span>

    1.  <span data-ttu-id="8c305-387">Klicken Sie auf der Registerkarte **gesteuert** auf **eigenes**.</span><span class="sxs-lookup"><span data-stu-id="8c305-387">On the **Controlled** tab, click **MyGPO**.</span></span> <span data-ttu-id="8c305-388">Drücken Sie STRG, und klicken Sie dann auf **Gruppenrichtlinienverwaltungs**.</span><span class="sxs-lookup"><span data-stu-id="8c305-388">Press CTRL and then click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="8c305-389">Klicken Sie mit der rechten Maustaste auf **Gruppenrichtlinienverwaltungs**, zeigen Sie auf **Unterschiede**, und klicken Sie auf **HTML-Bericht**.</span><span class="sxs-lookup"><span data-stu-id="8c305-389">Right-click **MyOtherGPO**, point to **Differences**, and click **HTML Report**.</span></span>

2.  <span data-ttu-id="8c305-390">So vergleichen Sie Gruppenrichtlinienverwaltungs und MyTemplate:</span><span class="sxs-lookup"><span data-stu-id="8c305-390">To compare MyOtherGPO and MyTemplate:</span></span>

    1.  <span data-ttu-id="8c305-391">Klicken Sie auf der Registerkarte **gesteuert** auf **Gruppenrichtlinienverwaltungs**.</span><span class="sxs-lookup"><span data-stu-id="8c305-391">On the **Controlled** tab, click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="8c305-392">Klicken Sie mit der rechten Maustaste auf **Gruppenrichtlinienverwaltungs**, zeigen Sie auf **Unterschiede**, und klicken Sie auf **Vorlage**.</span><span class="sxs-lookup"><span data-stu-id="8c305-392">Right-click **MyOtherGPO**, point to **Differences**, and click **Template**.</span></span>

    3.  <span data-ttu-id="8c305-393">Wählen Sie **MyTemplate** und **HTML-Bericht**aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c305-393">Select **MyTemplate** and **HTML Report**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage5"></a><span data-ttu-id="8c305-394">Schritt 5: Löschen und Wiederherstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="8c305-394">Step 5: Delete and restore a GPO</span></span>

<span data-ttu-id="8c305-395">In diesem Schritt fungieren Sie als genehmigende Person, um ein GPO zu löschen.</span><span class="sxs-lookup"><span data-stu-id="8c305-395">In this step, you act as an Approver to delete a GPO.</span></span>

**<span data-ttu-id="8c305-396">So löschen Sie ein Gruppenrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="8c305-396">To delete a GPO</span></span>**

1.  <span data-ttu-id="8c305-397">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle der genehmigenden Person zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="8c305-397">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver.</span></span>

2.  <span data-ttu-id="8c305-398">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="8c305-398">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="8c305-399">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8c305-399">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="8c305-400">Klicken Sie mit der rechten Maustaste auf **eigenes**, und klicken Sie dann auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="8c305-400">Right-click **MyGPO**, and then click **Delete**.</span></span> <span data-ttu-id="8c305-401">Klicken Sie auf **Gruppenrichtlinienobjekt aus Archiv und Produktion löschen** , um sowohl die Version im Archiv als auch die bereitgestellte Version des Gruppenrichtlinienobjekts in der Produktionsumgebung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="8c305-401">Click **Delete GPO from archive and production** to delete both the version in the archive as well as the deployed version of the GPO in the production environment.</span></span>

5.  <span data-ttu-id="8c305-402">Geben Sie einen Kommentar ein, der im Überwachungspfad für das Gruppenrichtlinienobjekt angezeigt werden soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c305-402">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

6.  <span data-ttu-id="8c305-403">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="8c305-403">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8c305-404">Das Gruppenrichtlinienobjekt wird von der Registerkarte " **gesteuert** " entfernt und auf der Registerkarte " **Papierkorb** " angezeigt, wo es wiederhergestellt oder gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="8c305-404">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

<span data-ttu-id="8c305-405">Gelegentlich können Sie nach dem Löschen eines GPO feststellen, dass es noch benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="8c305-405">Occasionally you may discover after deleting a GPO that it is still needed.</span></span> <span data-ttu-id="8c305-406">In diesem Schritt fungieren Sie als genehmigende Person zum Wiederherstellen eines gelöschten Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="8c305-406">In this step, you act as an Approver to restore a GPO that has been deleted.</span></span>

**<span data-ttu-id="8c305-407">So stellen Sie ein gelöschtes Gruppenrichtlinienobjekt wieder her</span><span class="sxs-lookup"><span data-stu-id="8c305-407">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="8c305-408">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **Papierkorb** , um gelöschte GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8c305-408">On the **Contents** tab, click the **Recycle Bin** tab to display deleted GPOs.</span></span>

2.  <span data-ttu-id="8c305-409">Klicken Sie mit der rechten Maustaste auf **eigenes**, und klicken Sie dann auf **Wiederherstellen**.</span><span class="sxs-lookup"><span data-stu-id="8c305-409">Right-click **MyGPO**, and then click **Restore**.</span></span>

3.  <span data-ttu-id="8c305-410">Geben Sie einen Kommentar ein, der im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c305-410">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="8c305-411">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="8c305-411">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8c305-412">Das Gruppenrichtlinienobjekt wird von der Registerkarte " **Papierkorb** " entfernt und auf der Registerkarte " **gesteuert** " angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c305-412">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

    <span data-ttu-id="8c305-413">**Hinweis**  Wenn Sie ein GPO im Archiv wiederherstellen, wird es nicht automatisch in der Produktionsumgebung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="8c305-413">**Note** Restoring a GPO to the archive does not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="8c305-414">Wenn Sie das Gruppenrichtlinienobjekt an die Produktionsumgebung zurückgeben möchten, stellen Sie das Gruppenrichtlinienobjekt wie in [Schritt 3: überprüfen und Bereitstellen eines Gruppenrichtlinien](#bkmk-manage3)Objekts bereit.</span><span class="sxs-lookup"><span data-stu-id="8c305-414">To return the GPO to the production environment, deploy the GPO as in [Step 3: Review and deploy a GPO](#bkmk-manage3).</span></span>

     

<span data-ttu-id="8c305-415">Nachdem Sie ein GPO bearbeitet und bereitgestellt haben, stellen Sie möglicherweise fest, dass die letzten Änderungen am Gruppenrichtlinienobjekt ein Problem verursachen.</span><span class="sxs-lookup"><span data-stu-id="8c305-415">After editing and deploying a GPO, you may discover that recent changes to the GPO are causing a problem.</span></span> <span data-ttu-id="8c305-416">In diesem Schritt fungieren Sie als genehmigende Person, um einen Rollback zu einer früheren Version des Gruppenrichtlinienobjekts durchführen zu können.</span><span class="sxs-lookup"><span data-stu-id="8c305-416">In this step, you act as an Approver to roll back to a previous version of the GPO.</span></span> <span data-ttu-id="8c305-417">Sie können einen Rollback zu einer beliebigen Version im Verlauf des Gruppenrichtlinienobjekts ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c305-417">You can roll back to any version in the history of the GPO.</span></span> <span data-ttu-id="8c305-418">Sie können Kommentare und Beschriftungen verwenden, um bekannte gute Versionen zu identifizieren und wenn bestimmte Änderungen vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="8c305-418">You can use comments and labels to identify known good versions and when specific changes were made.</span></span>

**<span data-ttu-id="8c305-419">So führen Sie einen Rollback zu einer früheren Version eines GPO durch</span><span class="sxs-lookup"><span data-stu-id="8c305-419">To roll back to a previous version of a GPO</span></span>**

1.  <span data-ttu-id="8c305-420">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8c305-420">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

2.  <span data-ttu-id="8c305-421">Doppelklicken Sie auf **eigenes** , um dessen Verlauf anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8c305-421">Double-click **MyGPO** to display its history.</span></span>

3.  <span data-ttu-id="8c305-422">Klicken Sie mit der rechten Maustaste auf die bereit **zustellende**Version, klicken Sie auf bereitstellen, und klicken Sie dann auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8c305-422">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

4.  <span data-ttu-id="8c305-423">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="8c305-423">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8c305-424">Klicken Sie im Fenster **Verlauf** auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="8c305-424">In the **History** window, click **Close**.</span></span>

    <span data-ttu-id="8c305-425">**Hinweis**  Um zu überprüfen, ob die Version, die erneut bereitgestellt wurde, die beabsichtigte Version ist, untersuchen Sie einen Unterschiedsbericht für die beiden Versionen.</span><span class="sxs-lookup"><span data-stu-id="8c305-425">**Note** To verify that the version that has been redeployed is the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="8c305-426">Wählen Sie im Fenster **Verlauf** für das Gruppenrichtlinienobjekt die beiden Versionen aus, klicken Sie mit der rechten Maustaste darauf, zeigen Sie auf **Differenz**, und klicken Sie dann auf **HTML-Bericht** oder **XML-Bericht**.</span><span class="sxs-lookup"><span data-stu-id="8c305-426">In the **History** window for the GPO, select the two versions, right-click them, point to **Difference**, and then click either **HTML Report** or **XML Report**.</span></span>

     

 

 





