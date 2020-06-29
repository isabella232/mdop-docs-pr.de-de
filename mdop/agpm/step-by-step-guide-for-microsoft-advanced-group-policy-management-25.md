---
title: Schrittweise Anleitung für Microsoft Advanced Group Policy Management 2.5
description: Schrittweise Anleitung für Microsoft Advanced Group Policy Management 2.5
author: dansimp
ms.assetid: 454298c9-0fab-497a-9808-c0246a4c8db5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 67925e417e4fb1f5398dfd030f366936f1d36909
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808208"
---
# <span data-ttu-id="661d0-103">Schrittweise Anleitung für Microsoft Advanced Group Policy Management 2.5</span><span class="sxs-lookup"><span data-stu-id="661d0-103">Step-by-Step Guide for Microsoft Advanced Group Policy Management 2.5</span></span>


<span data-ttu-id="661d0-104">Diese Schritt-für-Schritt-Anleitung zeigt erweiterte Techniken für die Gruppenrichtlinienverwaltung mithilfe der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) und Microsoft Advanced Group Policy Management (AGPM).</span><span class="sxs-lookup"><span data-stu-id="661d0-104">This step-by-step guide demonstrates advanced techniques for Group Policy management using the Group Policy Management Console (GPMC) and Microsoft Advanced Group Policy Management (AGPM).</span></span> <span data-ttu-id="661d0-105">AGPM vergrößert die Funktionen der GPMC und bietet Folgendes:</span><span class="sxs-lookup"><span data-stu-id="661d0-105">AGPM increases the capabilities of the GPMC, providing:</span></span>

-   <span data-ttu-id="661d0-106">Standard Rollen für das Delegieren von Berechtigungen zum Verwalten von Gruppenrichtlinienobjekten (GPOs) an mehrere Gruppenrichtlinienadministratoren.</span><span class="sxs-lookup"><span data-stu-id="661d0-106">Standard roles for delegating permissions to manage Group Policy objects (GPOs) to multiple Group Policy administrators.</span></span>

-   <span data-ttu-id="661d0-107">Ein Archiv, damit Gruppenrichtlinienadministratoren GPOs offline erstellen und ändern können, bevor Sie in einer Produktionsumgebung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="661d0-107">An archive to enable Group Policy administrators to create and modify GPOs offline before deploying them to a production environment.</span></span>

-   <span data-ttu-id="661d0-108">Die Möglichkeit, einen Rollback zu einer beliebigen vorherigen Version eines GPO durchführen zu können.</span><span class="sxs-lookup"><span data-stu-id="661d0-108">The ability to roll back to any previous version of a GPO.</span></span>

-   <span data-ttu-id="661d0-109">Möglichkeit zum ein-und Auschecken von GPOs, um sicherzustellen, dass Gruppenrichtlinienadministratoren die Arbeit des anderen nicht versehentlich überschreiben.</span><span class="sxs-lookup"><span data-stu-id="661d0-109">Check-in/check-out capability for GPOs to ensure that Group Policy administrators do not inadvertently overwrite each other's work.</span></span>

## <span data-ttu-id="661d0-110">Übersicht über AGPM-Szenarien</span><span class="sxs-lookup"><span data-stu-id="661d0-110">AGPM scenario overview</span></span>


<span data-ttu-id="661d0-111">In diesem Szenario verwenden Sie für jede Rolle in AGPM ein separates Benutzerkonto, um zu veranschaulichen, wie Gruppenrichtlinien in einer Umgebung mit mehreren Gruppenrichtlinienadministratoren verwaltet werden können, die unterschiedliche Berechtigungsstufen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="661d0-111">For this scenario, you will use a separate user account for each role in AGPM to demonstrate how Group Policy can be managed in an environment with multiple Group Policy administrators who have different levels of permissions.</span></span> <span data-ttu-id="661d0-112">Insbesondere führen Sie die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="661d0-112">Specifically, you will perform the following tasks:</span></span>

-   <span data-ttu-id="661d0-113">Wenn Sie ein Konto verwenden, das Mitglied der Gruppe der Domänenadministratoren ist, installieren Sie AGPM Server, und weisen Sie die Rolle AGPM-Administrator einem Konto oder einer Gruppe zu.</span><span class="sxs-lookup"><span data-stu-id="661d0-113">Using an account that is a member of the Domain Admins group, install AGPM Server and assign the AGPM Administrator role to an account or group.</span></span>

-   <span data-ttu-id="661d0-114">Installieren Sie AGPM-Client mithilfe von Konten, denen Sie AGPM-Rollen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="661d0-114">Using accounts to which you will assign AGPM roles, install AGPM Client.</span></span>

-   <span data-ttu-id="661d0-115">Wenn Sie ein Konto mit der Rolle AGPM-Administrator verwenden, konfigurieren Sie AGPM, und delegieren Sie den Zugriff auf GPOs, indem Sie anderen Konten Rollen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="661d0-115">Using an account with the AGPM Administrator role, configure AGPM and delegate access to GPOs by assigning roles to other accounts.</span></span>

-   <span data-ttu-id="661d0-116">Wenn Sie ein Konto mit der Rolle des Editors verwenden, fordern Sie die Erstellung eines Gruppenrichtlinienobjekts an, das Sie dann mit einem Konto mit der Rolle genehmigende Person genehmigen.</span><span class="sxs-lookup"><span data-stu-id="661d0-116">Using an account with the Editor role, request the creation of a GPO, which you then approve using an account with the Approver role.</span></span> <span data-ttu-id="661d0-117">Überprüfen Sie mit dem Editor-Konto das Gruppenrichtlinienobjekt aus dem Archiv, bearbeiten Sie das Gruppenrichtlinienobjekt, überprüfen Sie das Gruppenrichtlinienobjekt in das Archiv, und fordern Sie die Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="661d0-117">With the Editor account, check the GPO out of the archive, edit the GPO, check the GPO into the archive, and request deployment.</span></span>

-   <span data-ttu-id="661d0-118">Überprüfen Sie das Gruppenrichtlinienobjekt, und stellen Sie es in Ihrer Produktionsumgebung bereit, indem Sie ein Konto mit der Rolle genehmigende Person verwenden.</span><span class="sxs-lookup"><span data-stu-id="661d0-118">Using an account with the Approver role, review the GPO and deploy it to your production environment.</span></span>

-   <span data-ttu-id="661d0-119">Erstellen Sie mithilfe eines Kontos mit der Rolle "Editor" eine GPO-Vorlage, und verwenden Sie Sie als Ausgangspunkt zum Erstellen eines neuen Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="661d0-119">Using an account with the Editor role, create a GPO template and use it as a starting point to create a new GPO.</span></span>

-   <span data-ttu-id="661d0-120">Wenn Sie ein Konto mit der Rolle genehmigende Person verwenden, löschen Sie ein GPO, und stellen Sie es wieder her.</span><span class="sxs-lookup"><span data-stu-id="661d0-120">Using an account with the Approver role, delete and restore a GPO.</span></span>

![Entwicklungsprozess für Gruppenrichtlinienobjekte](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <span data-ttu-id="661d0-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="661d0-122">Requirements</span></span>


<span data-ttu-id="661d0-123">Computer, auf denen Sie AGPM installieren möchten, müssen die folgenden Anforderungen erfüllen, und Sie müssen Konten erstellen, die in diesem Szenario verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="661d0-123">Computers on which you want to install AGPM must meet the following requirements, and you must create accounts for use in this scenario.</span></span>

### <span data-ttu-id="661d0-124">AGPM-Server Anforderungen</span><span class="sxs-lookup"><span data-stu-id="661d0-124">AGPM Server requirements</span></span>

<span data-ttu-id="661d0-125">AGPM Server 2.5 erfordert Windows Vista® (32-Bit-Version) ohne installierte Service Packs oder Windows Server® 2003 (32-Bit-Version) sowie die GPMC.</span><span class="sxs-lookup"><span data-stu-id="661d0-125">AGPM Server2.5 requires WindowsVista® (32-bit version) with no service packs installed or Windows Server®2003 (32-bit version), as well as the GPMC.</span></span> <span data-ttu-id="661d0-126">Darüber hinaus müssen Sie ein Mitglied der Gruppe der Domänenadministratoren sein, um AGPM Server installieren zu können.</span><span class="sxs-lookup"><span data-stu-id="661d0-126">Additionally, you must be a member of the Domain Admins group to install AGPM Server.</span></span>

<span data-ttu-id="661d0-127">Sie sollten AGPM Server auf einem Mitglieds Server oder Domänencontroller mit der neuesten Version der GPMC installieren, die für Sie verfügbar ist und von AGPM unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="661d0-127">You should install AGPM Server on a member server or domain controller with the most recent version of the GPMC that is available to you and supported by AGPM.</span></span> <span data-ttu-id="661d0-128">AGPM verwendet die GPMC zum Sichern und Wiederherstellen von GPOs, und neuere Versionen der GPMC bieten zusätzliche Richtlinieneinstellungen, die in früheren Versionen nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="661d0-128">AGPM uses the GPMC to back up and restore GPOs, and newer versions of the GPMC provide additional policy settings not available in preceding versions.</span></span> <span data-ttu-id="661d0-129">Wenn die Version der GPMC auf dem AGPM-Server älter als die Version auf den Computern ist, die von Administratoren zum Verwalten von Gruppenrichtlinien verwendet werden, kann der AGPM-Server diese Richtlinieneinstellungen nicht speichern, die in der älteren Version der GPMC nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="661d0-129">If the version of the GPMC on your AGPM Server is older than the version on the computers that administrators use to manage Group Policy, the AGPM Server will be unable to store those policy settings not available in the older version of the GPMC.</span></span>

<span data-ttu-id="661d0-130">Insbesondere können Sie die meisten Richtlinieneinstellungen weiterhin verwalten, wenn auf dem AGPM-Server Windows Server2003 ausgeführt wird und die Version der GPMC, die Sie begleitet hat, und die Computer der Gruppenrichtlinienadministratoren Windows Vista und die Version der GPMC, die Sie begleitet hat, ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="661d0-130">Specifically, if your AGPM Server is running Windows Server2003 and the version of the GPMC that accompanied it, and your Group Policy administrators’ computers are running WindowsVista and the version of the GPMC that accompanied it, you can still manage most policy settings.</span></span> <span data-ttu-id="661d0-131">Richtlinieneinstellungen aus der GPMC in Windows Vista, die nicht in der GPMC in Windows Server 2003 verfügbar sind, beispielsweise in Bezug auf Ordnerumleitung, Drahtlosnetzwerke (IEEE 802,11) und bereitgestellte Drucker, können vom AGPM-Server nicht gespeichert werden, obwohl Administratoren Sie mithilfe von AGPM auf ihren Computern konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="661d0-131">However, policy settings from the GPMC in Windows Vista that are not available in the GPMC in Windows Server 2003—such as those related to folder redirection, wireless networking (IEEE 802.11), and deployed printers—cannot be stored by the AGPM Server, even though administrators can configure them using AGPM on their computers.</span></span>

<span data-ttu-id="661d0-132">Wenn Sie AGPM Server auf einem Computer mit einer älteren Version von GPMC installieren müssen, als die Gruppenrichtlinienadministratoren ausgeführt werden, finden Sie Informationen dazu, welche Richtlinieneinstellungen für welche Betriebssysteme verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="661d0-132">If you must install AGPM Server on a computer with an older version of GPMC than your Group Policy administrators are running, see the Group Policy Settings Reference for details about which policy settings are available with which operating systems.</span></span> <span data-ttu-id="661d0-133">Informationen zum Herunterladen der Gruppenrichtlinien Einstellungsreferenz finden Sie unter <https://go.microsoft.com/fwlink/?LinkID=106147> .</span><span class="sxs-lookup"><span data-stu-id="661d0-133">To download the Group Policy Settings Reference, see <https://go.microsoft.com/fwlink/?LinkID=106147>.</span></span>

<span data-ttu-id="661d0-134">**Hinweis**  Archive können nicht von einem AGPM-Server oder einem GPOVault-Server mit Windows Server2003 zu einem AGPM-Server migriert werden, auf dem Windows Vista ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="661d0-134">**Note** Archives cannot be migrated from an AGPM Server or a GPOVault Server running Windows Server2003 to an AGPM Server running WindowsVista.</span></span>

<span data-ttu-id="661d0-135">Wenn GPOVault Server auf dem Computer installiert ist, auf dem Sie AGPM Server installieren möchten, empfiehlt es sich für Windows Server2003, GPOVault Server vor Beginn der Installation nicht zu deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="661d0-135">For Windows Server2003, if GPOVault Server is installed on the computer on which you want to install AGPM Server, it is recommended that you do not uninstall GPOVault Server before beginning the installation.</span></span> <span data-ttu-id="661d0-136">Die Installation von AGPM Server wird GPOVault Server deinstallieren und Ihre vorhandenen GPOVault-Archivdaten automatisch in ein AGPM-Archiv übertragen.</span><span class="sxs-lookup"><span data-stu-id="661d0-136">The installation of AGPM Server will uninstall GPOVault Server and automatically transfer your existing GPOVault archive data to an AGPM archive.</span></span>

 

### <span data-ttu-id="661d0-137">AGPM-Client Anforderungen</span><span class="sxs-lookup"><span data-stu-id="661d0-137">AGPM Client requirements</span></span>

<span data-ttu-id="661d0-138">AGPM Client 2.5 erfordert Windows Vista (32-Bit-Version) ohne installierte Service Packs oder Windows Server2003 (32-Bit-Version) sowie die GPMC.</span><span class="sxs-lookup"><span data-stu-id="661d0-138">AGPM Client2.5 requires WindowsVista (32-bit version) with no service packs installed or Windows Server2003 (32-bit version), as well as the GPMC.</span></span> <span data-ttu-id="661d0-139">AGPM-Client kann auf einem Computer mit AGPM Server installiert werden.</span><span class="sxs-lookup"><span data-stu-id="661d0-139">AGPM Client can be installed on a computer running AGPM Server.</span></span>

### <span data-ttu-id="661d0-140">Voraussetzungen für Szenarien</span><span class="sxs-lookup"><span data-stu-id="661d0-140">Scenario requirements</span></span>

<span data-ttu-id="661d0-141">Bevor Sie mit diesem Szenario beginnen, erstellen Sie vier Benutzerkonten.</span><span class="sxs-lookup"><span data-stu-id="661d0-141">Before you begin this scenario, create four user accounts.</span></span> <span data-ttu-id="661d0-142">Während des Szenarios weisen Sie jedem dieser Konten eine der folgenden AGPM-Rollen zu: AGPM-Administrator (Vollzugriff), genehmigende Person, Editor und Bearbeiter.</span><span class="sxs-lookup"><span data-stu-id="661d0-142">During the scenario, you will assign one of the following AGPM roles to each of these accounts: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="661d0-143">Diese Konten müssen in der Lage sein, e-Mail-Nachrichten zu senden und zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="661d0-143">These accounts must be able to send and receive e-mail messages.</span></span> <span data-ttu-id="661d0-144">Weisen Sie den Konten mit den Rollen des AGPM-Administrators, genehmigenden und (optional)-Editors die Berechtigung " **Link-GPOs** " zu.</span><span class="sxs-lookup"><span data-stu-id="661d0-144">Assign **Link GPOs** permission to the accounts with the AGPM Administrator, Approver, and (optionally) Editor roles.</span></span>

<span data-ttu-id="661d0-145">**Hinweis** 
 Die Berechtigung " **GPOs verknüpfen** " wird standardmäßig Mitgliedern von Domänenadministratoren und Unternehmensadministratoren zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="661d0-145">**Note**
**Link GPOs** permission is assigned to members of Domain Administrators and Enterprise Administrators by default.</span></span> <span data-ttu-id="661d0-146">Klicken Sie auf den Knoten für die Domäne, und klicken Sie dann auf die Registerkarte **Delegierung** , wählen Sie **GPOs verknüpfen**aus, klicken Sie auf **Hinzufügen**, und wählen Sie dann Benutzer oder Gruppen aus, denen die Berechtigung zugewiesen werden soll, wenn Sie zusätzlichen Benutzern oder Gruppen die Berechtigung zum **Verknüpfen von GPOs** zuweisen möchten (beispielsweise Konten mit den Rollen AGPM-Administrator oder genehmigende Person).</span><span class="sxs-lookup"><span data-stu-id="661d0-146">To assign **Link GPOs** permission to additional users or groups (such as accounts with the roles of AGPM Administrator or Approver), click the node for the domain and then click the **Delegation** tab, select **Link GPOs**, click **Add**, and select users or groups to which to assign the permission.</span></span>

 

<span data-ttu-id="661d0-147">In diesem Szenario führen Sie Aktionen mit unterschiedlichen Konten aus.</span><span class="sxs-lookup"><span data-stu-id="661d0-147">For this scenario, you perform actions with different accounts.</span></span> <span data-ttu-id="661d0-148">Sie können sich entweder mit jedem Konto wie angegeben anmelden, oder Sie können den Befehl **Ausführen als** verwenden, um die GPMC mit dem angegebenen Konto zu starten.</span><span class="sxs-lookup"><span data-stu-id="661d0-148">You can either log on with each account as indicated, or you can use the **Run as** command to start the GPMC with the indicated account.</span></span>

<span data-ttu-id="661d0-149">**Hinweis**  Wenn Sie den Befehl **Ausführen als** in der GPMC unter Windows Server2003 verwenden möchten, klicken Sie auf **Start**, zeigen Sie auf **Verwaltung**, klicken Sie mit der rechten Maustaste auf **Gruppenrichtlinienverwaltung**, und klicken Sie dann auf **Ausführen als**.</span><span class="sxs-lookup"><span data-stu-id="661d0-149">**Note** To use the **Run as** command with GPMC on Windows Server2003, click **Start**, point to **Administrative Tools**, right-click **Group Policy Management**, and click **Run as**.</span></span> <span data-ttu-id="661d0-150">Klicken Sie auf **den folgenden Benutzer** , und geben Sie die Anmeldeinformationen für ein Konto ein.</span><span class="sxs-lookup"><span data-stu-id="661d0-150">Click **The following user** and enter credentials for an account.</span></span>

<span data-ttu-id="661d0-151">Wenn Sie den Befehl **Ausführen als** in der GPMC unter Windows Vista verwenden möchten, klicken Sie auf die Schaltfläche **Start** , zeigen Sie auf **Ausführen**, und geben Sie **runas/User:** <em> DomainName\\UserName </em> **"MMC%windir%\\system32\\gpmc.msc"** ein, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="661d0-151">To use the **Run as** command with GPMC on Windows Vista, click the **Start** button, point to **Run**, and type **runas /user:**<em>DomainName\\UserName</em>**"mmc %windir%\\system32\\gpmc.msc"**, and click **OK**.</span></span> <span data-ttu-id="661d0-152">Geben Sie das Kennwort für das Konto ein, wenn Sie dazu aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="661d0-152">Type the password for the account when prompted.</span></span>

 

## <span data-ttu-id="661d0-153">Schritte zum Installieren und Konfigurieren von AGPM</span><span class="sxs-lookup"><span data-stu-id="661d0-153">Steps for installing and configuring AGPM</span></span>


<span data-ttu-id="661d0-154">Sie müssen die folgenden Schritte ausführen, um AGPM zu installieren und zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="661d0-154">You must complete the following steps to install and configure AGPM.</span></span>

[<span data-ttu-id="661d0-155">Schritt 1: Installieren des AGPM-Servers</span><span class="sxs-lookup"><span data-stu-id="661d0-155">Step 1: Install AGPM Server</span></span>](#bkmk-config1)

[<span data-ttu-id="661d0-156">Schritt 2: Installieren des AGPM-Clients</span><span class="sxs-lookup"><span data-stu-id="661d0-156">Step 2: Install AGPM Client</span></span>](#bkmk-config2)

[<span data-ttu-id="661d0-157">Schritt 3: Konfigurieren einer AGPM-Server Verbindung</span><span class="sxs-lookup"><span data-stu-id="661d0-157">Step 3: Configure an AGPM Server connection</span></span>](#bkmk-config3)

[<span data-ttu-id="661d0-158">Schritt 4: Konfigurieren einer e-Mail-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="661d0-158">Step 4: Configure e-mail notification</span></span>](#bkmk-config4)

[<span data-ttu-id="661d0-159">Schritt 5: Delegieren des Zugriffs</span><span class="sxs-lookup"><span data-stu-id="661d0-159">Step 5: Delegate access</span></span>](#bkmk-config5)

### <a href="" id="bkmk-config1"></a><span data-ttu-id="661d0-160">Schritt 1: Installieren des AGPM-Servers</span><span class="sxs-lookup"><span data-stu-id="661d0-160">Step 1: Install AGPM Server</span></span>

<span data-ttu-id="661d0-161">In diesem Schritt installieren Sie AGPM Server auf dem Mitglieds Server oder Domänencontroller, auf dem der AGPM-Dienst ausgeführt wird, und konfigurieren das Archiv.</span><span class="sxs-lookup"><span data-stu-id="661d0-161">In this step, you install AGPM Server on the member server or domain controller that will run the AGPM Service, and you configure the archive.</span></span> <span data-ttu-id="661d0-162">Alle AGPM-Vorgänge werden über diesen Windows-Dienst verwaltet und mit den Anmeldeinformationen des Diensts ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="661d0-162">All AGPM operations are managed through this Windows service and are executed with the service's credentials.</span></span> <span data-ttu-id="661d0-163">Das von einem AGPM-Server verwaltete Archiv kann auf diesem Server oder auf einem anderen Server in derselben Gesamtstruktur gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="661d0-163">The archive managed by an AGPM Server can be hosted on that server or on another server in the same forest.</span></span>

**<span data-ttu-id="661d0-164">So installieren Sie AGPM Server auf dem Computer, der den AGPM-Dienst hosten soll</span><span class="sxs-lookup"><span data-stu-id="661d0-164">To install AGPM Server on the computer that will host the AGPM Service</span></span>**

1.  <span data-ttu-id="661d0-165">Melden Sie sich mit einem Konto an, das Mitglied der Gruppe der Domänenadministratoren ist.</span><span class="sxs-lookup"><span data-stu-id="661d0-165">Log on with an account that is a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="661d0-166">Starten Sie die Microsoft Desktop Optimization Pack-CD, und folgen Sie den Anweisungen auf dem Bildschirm, um **Advanced Group Policy Management-Server**auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="661d0-166">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Server**.</span></span>

3.  <span data-ttu-id="661d0-167">Klicken Sie im Dialogfeld **Willkommen** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="661d0-167">In the **Welcome** dialog box, click **Next**.</span></span>

4.  <span data-ttu-id="661d0-168">Akzeptieren Sie im Dialogfeld **Microsoft-Software-Lizenzbestimmungen** die Begriffe, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="661d0-168">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

5.  <span data-ttu-id="661d0-169">Wählen Sie im Dialogfeld **Anwendungspfad** einen Speicherort aus, an dem AGPM Server installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="661d0-169">In the **Application Path** dialog box, select a location in which to install AGPM Server.</span></span> <span data-ttu-id="661d0-170">Auf dem Computer, auf dem AGPM Server installiert ist, wird der AGPM-Dienst gehostet und das Archiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="661d0-170">The computer on which AGPM Server is installed will host the AGPM Service and manage the archive.</span></span> <span data-ttu-id="661d0-171">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="661d0-171">Click **Next**.</span></span>

6.  <span data-ttu-id="661d0-172">Wählen Sie im Dialogfeld **Archivpfad** einen Speicherort für das Archiv relativ zum AGPM-Server aus.</span><span class="sxs-lookup"><span data-stu-id="661d0-172">In the **Archive Path** dialog box, select a location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="661d0-173">Der Archivpfad kann auf einen Ordner auf dem AGPM-Server oder an anderer Stelle verweisen, Sie sollten jedoch einen Speicherort mit genügend Speicherplatz zum Speichern aller GPOs und Verlaufsdaten auswählen, die von diesem AGPM-Server verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="661d0-173">The archive path can point to a folder on the AGPM Server or elsewhere, but you should select a location with sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span> <span data-ttu-id="661d0-174">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="661d0-174">Click **Next**.</span></span>

7.  <span data-ttu-id="661d0-175">Wählen Sie im Dialogfeld **AGPM-Dienstkonto** ein Dienstkonto aus, unter dem der AGPM-Dienst ausgeführt wird, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="661d0-175">In the **AGPM Service Account** dialog box, select a service account under which the AGPM Service will run and then click **Next**.</span></span>

8.  <span data-ttu-id="661d0-176">Wählen Sie im Dialogfeld **Besitzer des Archivs** ein Konto oder eine Gruppe aus, dem Sie zunächst die Rolle AGPM-Administrator (Vollzugriff) zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="661d0-176">In the **Archive Owner** dialog box, select an account or group to which to initially assign the AGPM Administrator (Full Control) role.</span></span> <span data-ttu-id="661d0-177">Dieser AGPM-Administrator kann anderen Gruppenrichtlinienadministratoren AGPM-Rollen und-Berechtigungen zuweisen (einschließlich der Rolle des AGPM-Administrators).</span><span class="sxs-lookup"><span data-stu-id="661d0-177">This AGPM Administrator can assign AGPM roles and permissions to other Group Policy administrators (including the role of AGPM Administrator).</span></span> <span data-ttu-id="661d0-178">Wählen Sie in diesem Szenario das Konto aus, das in der Rolle des AGPM-Administrators dienen soll.</span><span class="sxs-lookup"><span data-stu-id="661d0-178">For this scenario, select the account to serve in the AGPM Administrator role.</span></span> <span data-ttu-id="661d0-179">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="661d0-179">Click **Next**.</span></span>

9.  <span data-ttu-id="661d0-180">Klicken Sie auf **Installieren**, und klicken Sie dann auf **Fertig stellen** , um den Setup-Assistenten zu beenden.</span><span class="sxs-lookup"><span data-stu-id="661d0-180">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

    <span data-ttu-id="661d0-181">**Vorsicht**  Ändern Sie die Einstellungen für den AGPM-Dienst nicht über **Administrative Tools** und **Dienste** im Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="661d0-181">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="661d0-182">Dadurch kann der Start des AGPM-Diensts verhindert werden.</span><span class="sxs-lookup"><span data-stu-id="661d0-182">Doing so can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="661d0-183">Informationen zum Ändern der Einstellungen für den Dienst finden Sie unter Hilfe zur erweiterten Gruppenrichtlinienverwaltung.</span><span class="sxs-lookup"><span data-stu-id="661d0-183">For information on how to modify settings for the service, see Help for Advanced Group Policy Management.</span></span>

     

### <a href="" id="bkmk-config2"></a><span data-ttu-id="661d0-184">Schritt 2: Installieren des AGPM-Clients</span><span class="sxs-lookup"><span data-stu-id="661d0-184">Step 2: Install AGPM Client</span></span>

<span data-ttu-id="661d0-185">Jeder Gruppenrichtlinienadministrator – jeder, der GPOs erstellt, bearbeitet, bereitstellt, überprüft oder löscht, muss AGPM-Client auf Computern installiert haben, die Sie zum Verwalten von GPOs verwenden.</span><span class="sxs-lookup"><span data-stu-id="661d0-185">Each Group Policy administrator—anyone who creates, edits, deploys, reviews, or deletes GPOs—must have AGPM Client installed on computers that they use to manage GPOs.</span></span> <span data-ttu-id="661d0-186">In diesem Szenario installieren Sie AGPM-Client auf mindestens einem Computer.</span><span class="sxs-lookup"><span data-stu-id="661d0-186">For this scenario, you install AGPM Client on at least one computer.</span></span> <span data-ttu-id="661d0-187">Sie müssen den AGPM-Client nicht auf den Computern von Endbenutzern installieren, die keine Gruppenrichtlinienverwaltung durchführen.</span><span class="sxs-lookup"><span data-stu-id="661d0-187">You do not need to install AGPM Client on the computers of end users who do not perform Group Policy administration.</span></span>

**<span data-ttu-id="661d0-188">So installieren Sie den AGPM-Client auf dem Computer eines Gruppenrichtlinienadministrators</span><span class="sxs-lookup"><span data-stu-id="661d0-188">To install AGPM Client on the computer of a Group Policy administrator</span></span>**

1.  <span data-ttu-id="661d0-189">Starten Sie die Microsoft Desktop Optimization Pack-CD, und folgen Sie den Anweisungen auf dem Bildschirm, um **Erweiterte Gruppenrichtlinienverwaltung-Client**auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="661d0-189">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Client**.</span></span>

2.  <span data-ttu-id="661d0-190">Klicken Sie im Dialogfeld **Willkommen** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="661d0-190">In the **Welcome** dialog box, click **Next**.</span></span>

3.  <span data-ttu-id="661d0-191">Akzeptieren Sie im Dialogfeld **Microsoft-Software-Lizenzbestimmungen** die Begriffe, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="661d0-191">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

4.  <span data-ttu-id="661d0-192">Wählen Sie im Dialogfeld **Anwendungspfad** einen Speicherort aus, an dem AGPM-Client installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="661d0-192">In the **Application Path** dialog box, select a location in which to install AGPM Client.</span></span> <span data-ttu-id="661d0-193">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="661d0-193">Click **Next**.</span></span>

5.  <span data-ttu-id="661d0-194">Geben Sie im Dialogfeld **AGPM-Server** den vollqualifizierten Computernamen und den Port für den AGPM-Server ein, mit dem die Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="661d0-194">In the **AGPM Server** dialog box, type the fully-qualified computer name and the port for the AGPM Server to which to connect.</span></span> <span data-ttu-id="661d0-195">Der Standardport für den AGPM-Dienst ist 4600.</span><span class="sxs-lookup"><span data-stu-id="661d0-195">The default port for the AGPM Service is 4600.</span></span> <span data-ttu-id="661d0-196">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="661d0-196">Click **Next**.</span></span>

6.  <span data-ttu-id="661d0-197">Klicken Sie auf **Installieren**, und klicken Sie dann auf **Fertig stellen** , um den Setup-Assistenten zu beenden.</span><span class="sxs-lookup"><span data-stu-id="661d0-197">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

### <a href="" id="bkmk-config3"></a><span data-ttu-id="661d0-198">Schritt 3: Konfigurieren einer AGPM-Server Verbindung</span><span class="sxs-lookup"><span data-stu-id="661d0-198">Step 3: Configure an AGPM Server connection</span></span>

<span data-ttu-id="661d0-199">AGPM speichert alle Versionen der einzelnen gesteuerten Gruppenrichtlinienobjekte (GPO) – ein GPO, für das AGPM das Änderungs Steuerelement bereitstellt – in einem zentralen Archiv, sodass Gruppenrichtlinienadministratoren GPOs offline anzeigen und ändern können, ohne dass sich dies unmittelbar auf die bereitgestellte Version jedes GPO auswirkt.</span><span class="sxs-lookup"><span data-stu-id="661d0-199">AGPM stores all versions of each controlled Group Policy object (GPO)—a GPO for which AGPM provides change control—in a central archive, so Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="661d0-200">In diesem Schritt konfigurieren Sie eine AGPM-Serververbindung und stellen sicher, dass alle Gruppenrichtlinienadministratoren eine Verbindung mit dem gleichen AGPM-Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="661d0-200">In this step, you configure an AGPM Server connection and ensure that all Group Policy administrators connect to the same AGPM Server.</span></span> <span data-ttu-id="661d0-201">(Informationen zum Konfigurieren mehrerer AGPM-Server finden Sie unter Hilfe zur erweiterten Gruppenrichtlinienverwaltung.)</span><span class="sxs-lookup"><span data-stu-id="661d0-201">(For information about configuring multiple AGPM Servers, see Help for Advanced Group Policy Management.)</span></span>

**<span data-ttu-id="661d0-202">So konfigurieren Sie eine AGPM-Server Verbindung für alle Gruppenrichtlinienadministratoren</span><span class="sxs-lookup"><span data-stu-id="661d0-202">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="661d0-203">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit dem Benutzerkonto an, das Sie als Archiv Besitzer ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="661d0-203">On a computer on which you have installed AGPM Client, log on with the user account that you selected as the Archive Owner.</span></span> <span data-ttu-id="661d0-204">Dieser Benutzer hat die Rolle des AGPM-Administrators (Vollzugriff).</span><span class="sxs-lookup"><span data-stu-id="661d0-204">This user has the role of AGPM Administrator (Full Control).</span></span>

2.  <span data-ttu-id="661d0-205">Klicken Sie auf **Start**, zeigen Sie auf **Verwaltung**, und klicken Sie auf **Gruppenrichtlinienverwaltung** , um die **Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC)** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="661d0-205">Click **Start**, point to **Administrative Tools**, and click **Group Policy Management** to open the **Group Policy Management Console (GPMC)**.</span></span>

3.  <span data-ttu-id="661d0-206">Bearbeiten Sie in der **Gruppenrichtlinien-Verwaltungskonsolen** Struktur ein GPO, das auf alle Gruppenrichtlinienadministratoren angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="661d0-206">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span>

4.  <span data-ttu-id="661d0-207">Klicken Sie im **Gruppenrichtlinienobjekt-Editor** -Fenster auf **Benutzerkonfiguration**, **Administrative Vorlagen**und **Windows-Komponenten**.</span><span class="sxs-lookup"><span data-stu-id="661d0-207">In the **Group Policy Object Editor** window, click **User Configuration**, **Administrative Templates**, and **Windows Components**.</span></span>

5.  <span data-ttu-id="661d0-208">Wenn **AGPM** nicht unter Windows- **Komponenten**aufgeführt ist:</span><span class="sxs-lookup"><span data-stu-id="661d0-208">If **AGPM** is not listed under **Windows Components**:</span></span>

    1.  <span data-ttu-id="661d0-209">Klicken Sie mit der rechten Maustaste auf **Administrative Vorlagen** , und wählen Sie **Vorlagen hinzufügen/entfernen**aus.</span><span class="sxs-lookup"><span data-stu-id="661d0-209">Right-click **Administrative Templates** and select **Add/Remove Templates**.</span></span>

    2.  <span data-ttu-id="661d0-210">Klicken Sie auf **Hinzufügen**, wählen Sie **AGPM. ADMX** oder **AGPM. adm**aus, klicken Sie auf **Öffnen**und dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="661d0-210">Click **Add**, select **agpm.admx** or **agpm.adm**, click **Open**, and then click **Close**.</span></span>

6.  <span data-ttu-id="661d0-211">Doppelklicken Sie unter **Windows-Komponenten**auf **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="661d0-211">Under **Windows Components**, double-click **AGPM**.</span></span>

7.  <span data-ttu-id="661d0-212">Doppelklicken Sie im Detailbereich auf **AGPM-Server (alle Domänen)**.</span><span class="sxs-lookup"><span data-stu-id="661d0-212">In the details pane, double-click **AGPM Server (all domains)**.</span></span>

8.  <span data-ttu-id="661d0-213">Wählen Sie im **Eigenschaftenfenster AGPM-Server (alle Domänen)** die Option **aktiviert** aus, und geben Sie den vollqualifizierten Computernamen und-Port (beispielsweise Server.contoso.com:4600) für den Server ein, der das Archiv hostet.</span><span class="sxs-lookup"><span data-stu-id="661d0-213">In the **AGPM Server (all domains) Properties** window, select **Enabled** and type the fully-qualified computer name and port (for example, server.contoso.com:4600) for the server hosting the archive.</span></span> <span data-ttu-id="661d0-214">Der vom AGPM-Dienst verwendete Port ist Port 4600.</span><span class="sxs-lookup"><span data-stu-id="661d0-214">The port used by the AGPM Service is port 4600.</span></span>

9.  <span data-ttu-id="661d0-215">Klicken Sie auf **OK**, und schließen Sie dann das **Gruppenrichtlinienobjekt-Editor-** Fenster.</span><span class="sxs-lookup"><span data-stu-id="661d0-215">Click **OK**, and then close the **Group Policy Object Editor** window.</span></span> <span data-ttu-id="661d0-216">Wenn die Gruppenrichtlinie aktualisiert wird, wird die AGPM-Server Verbindung für jeden Gruppenrichtlinienadministrator konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="661d0-216">When Group Policy is updated, the AGPM Server connection is configured for each Group Policy administrator.</span></span>

### <a href="" id="bkmk-config4"></a><span data-ttu-id="661d0-217">Schritt 4: Konfigurieren einer e-Mail-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="661d0-217">Step 4: Configure e-mail notification</span></span>

<span data-ttu-id="661d0-218">Als AGPM-Administrator (Vollzugriff) legen Sie die e-Mail-Adressen von Genehmigern und AGPM-Administratoren fest, denen eine e-Mail-Nachricht mit einer Anforderung gesendet wird, wenn ein Editor versucht, ein GPO zu erstellen, bereitzustellen oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="661d0-218">As an AGPM Administrator (Full Control), you designate the e-mail addresses of Approvers and AGPM Administrators to whom an e-mail message containing a request is sent when an Editor attempts to create, deploy, or delete a GPO.</span></span> <span data-ttu-id="661d0-219">Darüber hinaus ermitteln Sie den Alias, aus dem diese Nachrichten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="661d0-219">You also determine the alias from which these messages are sent.</span></span>

**<span data-ttu-id="661d0-220">So konfigurieren Sie die e-Mail-Benachrichtigung für AGPM</span><span class="sxs-lookup"><span data-stu-id="661d0-220">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="661d0-221">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="661d0-221">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="661d0-222">Klicken Sie im Detailbereich auf die Registerkarte **Domänendelegierung** .</span><span class="sxs-lookup"><span data-stu-id="661d0-222">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="661d0-223">Geben Sie im Feld **von** den e-Mail-Alias für AGPM ein, aus dem Benachrichtigungen gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="661d0-223">In the **From** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="661d0-224">Geben Sie im Feld **an** die e-Mail-Adresse für das Benutzerkonto ein, dem Sie die genehmigende Rolle zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="661d0-224">In the **To** field, type the e-mail address for the user account to which you intend to assign the Approver role.</span></span>

5.  <span data-ttu-id="661d0-225">Geben Sie im Feld **SMTP-Server** einen gültigen SMTP-e-Mail-Server ein.</span><span class="sxs-lookup"><span data-stu-id="661d0-225">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="661d0-226">Geben Sie in den Feldern **Benutzername** und **Kennwort** die Anmeldeinformationen eines Benutzers mit Zugriff auf den SMTP-Dienst ein.</span><span class="sxs-lookup"><span data-stu-id="661d0-226">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span>

7.  <span data-ttu-id="661d0-227">Klicken Sie auf **Übernehmen**.</span><span class="sxs-lookup"><span data-stu-id="661d0-227">Click **Apply**.</span></span>

### <a href="" id="bkmk-config5"></a><span data-ttu-id="661d0-228">Schritt 5: Delegieren des Zugriffs</span><span class="sxs-lookup"><span data-stu-id="661d0-228">Step 5: Delegate access</span></span>

<span data-ttu-id="661d0-229">Als AGPM-Administrator (Vollzugriff) delegieren Sie den Zugriff auf Gruppenrichtlinienobjekte auf Domänenebene, wobei dem Konto jedes Gruppenrichtlinienadministrators Rollen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="661d0-229">As an AGPM Administrator (Full Control), you delegate domain-level access to GPOs, assigning roles to the account of each Group Policy administrator.</span></span>

<span data-ttu-id="661d0-230">**Hinweis**  Sie können den Zugriff auch auf der GPO-Ebene und nicht auf der Domänenebene delegieren.</span><span class="sxs-lookup"><span data-stu-id="661d0-230">**Note** You can also delegate access at the GPO level rather than the domain level.</span></span> <span data-ttu-id="661d0-231">Ausführliche Informationen finden Sie unter Hilfe zur erweiterten Gruppenrichtlinienverwaltung.</span><span class="sxs-lookup"><span data-stu-id="661d0-231">For details, see Help for Advanced Group Policy Management.</span></span>

 

<span data-ttu-id="661d0-232">**Wichtig**  Sie sollten die Mitgliedschaft in der Gruppe der Gruppenrichtlinien Ersteller-Besitzer einschränken, damit Sie nicht dazu verwendet werden kann, die AGPM-Verwaltung des Zugriffs auf GPOs zu umgehen.</span><span class="sxs-lookup"><span data-stu-id="661d0-232">**Important** You should restrict membership in the Group Policy Creator Owners group, so it cannot be used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="661d0-233">(Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gruppenrichtlinienobjekte** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, klicken Sie auf **Delegierung**, und konfigurieren Sie dann die Einstellungen, um die Anforderungen Ihrer Organisation zu erfüllen.)</span><span class="sxs-lookup"><span data-stu-id="661d0-233">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

 

**<span data-ttu-id="661d0-234">So delegieren Sie den Zugriff auf alle GPOs in einer Domäne</span><span class="sxs-lookup"><span data-stu-id="661d0-234">To delegate access to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="661d0-235">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="661d0-235">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="661d0-236">Klicken Sie auf der Registerkarte **Domänendelegierung** auf die Schaltfläche **erweitert** .</span><span class="sxs-lookup"><span data-stu-id="661d0-236">On the **Domain Delegation** tab, click the **Advanced** button.</span></span>

3.  <span data-ttu-id="661d0-237">Im Dialogfeld " **Berechtigungen** ":</span><span class="sxs-lookup"><span data-stu-id="661d0-237">In the **Permissions** dialog box:</span></span>

    1.  <span data-ttu-id="661d0-238">Klicken Sie auf das Benutzerkonto eines Gruppenrichtlinienadministrators, und aktivieren Sie dann das Kontrollkästchen **Genehmiger** , um diese Rolle dem Konto zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="661d0-238">Click the user account of a Group Policy administrator, and then select the **Approver** check box to assign that role to the account.</span></span> <span data-ttu-id="661d0-239">Deaktivieren Sie das Kontrollkästchen **Editor** .</span><span class="sxs-lookup"><span data-stu-id="661d0-239">Clear the **Editor** check box.</span></span> <span data-ttu-id="661d0-240">(Diese Rolle umfasst die Rolle Prüfer.)</span><span class="sxs-lookup"><span data-stu-id="661d0-240">(This role includes the Reviewer role.)</span></span>

    2.  <span data-ttu-id="661d0-241">Klicken Sie auf das Benutzerkonto eines anderen Gruppenrichtlinienadministrators, und aktivieren Sie dann das Kontrollkästchen **Editor** , um diese Rolle dem Konto zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="661d0-241">Click the user account of another Group Policy administrator, and then select the **Editor** check box to assign that role to the account.</span></span> <span data-ttu-id="661d0-242">(Diese Rolle umfasst die Rolle Prüfer.)</span><span class="sxs-lookup"><span data-stu-id="661d0-242">(This role includes the Reviewer role.)</span></span>

    3.  <span data-ttu-id="661d0-243">Klicken Sie auf ein drittes Konto, und aktivieren Sie dann **das Kontrollkästchen Prüfer,** um dem Konto dieses Gruppenrichtlinienadministrators nur die Rolle Prüfer zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="661d0-243">Click a third account and then select the **Reviewer** check box to assign only the Reviewer role to the account of that Group Policy administrator.</span></span> <span data-ttu-id="661d0-244">Deaktivieren Sie das Kontrollkästchen **Editor** .</span><span class="sxs-lookup"><span data-stu-id="661d0-244">Clear the **Editor** check box.</span></span>

    4.  <span data-ttu-id="661d0-245">Klicken Sie auf die Schaltfläche **erweitert** .</span><span class="sxs-lookup"><span data-stu-id="661d0-245">Click the **Advanced** button.</span></span>

4.  <span data-ttu-id="661d0-246">Im Dialogfeld " **Erweiterte Sicherheitseinstellungen** ":</span><span class="sxs-lookup"><span data-stu-id="661d0-246">In the **Advanced Security Settings** dialog box:</span></span>

    1.  <span data-ttu-id="661d0-247">Wählen Sie einen Gruppenrichtlinienadministrator aus, und klicken Sie dann auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="661d0-247">Select a Group Policy administrator, and then click **Edit**.</span></span>

    2.  <span data-ttu-id="661d0-248">Wählen Sie für **anwenden auf**die Option **dieses Objekt und verschachtelte Objekte**aus, und klicken Sie dann im Dialogfeld **Berechtigungs** **Eintrag** auf **OK** .</span><span class="sxs-lookup"><span data-stu-id="661d0-248">For **Apply onto**, select **This object and nested objects**, and then click **OK** in the **Permission** **Entry** dialog box.</span></span>

    3.  <span data-ttu-id="661d0-249">Wiederholen Sie diesen Vorgang für jeden Gruppenrichtlinienadministrator.</span><span class="sxs-lookup"><span data-stu-id="661d0-249">Repeat for each Group Policy administrator.</span></span>

5.  <span data-ttu-id="661d0-250">Klicken Sie im Dialogfeld **Erweiterte Sicherheitseinstellungen** auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="661d0-250">In the **Advanced Security Settings** dialog box, click **OK**.</span></span>

6.  <span data-ttu-id="661d0-251">Klicken Sie im Dialogfeld **Berechtigungen** auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="661d0-251">In the **Permissions** dialog box, click **OK**.</span></span>

## <span data-ttu-id="661d0-252">Schritte zum Verwalten von GPOs</span><span class="sxs-lookup"><span data-stu-id="661d0-252">Steps for managing GPOs</span></span>


<span data-ttu-id="661d0-253">Sie müssen die folgenden Schritte ausführen, um GPOs mithilfe von AGPM zu erstellen, zu bearbeiten, zu überprüfen und bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="661d0-253">You must complete the following steps to create, edit, review, and deploy GPOs using AGPM.</span></span> <span data-ttu-id="661d0-254">Darüber hinaus erstellen Sie eine Vorlage, löschen ein GPO und Wiederherstellen eines gelöschten Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="661d0-254">Additionally, you will create a template, delete a GPO, and restore a deleted GPO.</span></span>

[<span data-ttu-id="661d0-255">Schritt 1: Erstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="661d0-255">Step 1: Create a GPO</span></span>](#bkmk-manage1)

[<span data-ttu-id="661d0-256">Schritt 2: Bearbeiten eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="661d0-256">Step 2: Edit a GPO</span></span>](#bkmk-manage2)

[<span data-ttu-id="661d0-257">Schritt 3: überprüfen und Bereitstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="661d0-257">Step 3: Review and deploy a GPO</span></span>](#bkmk-manage3)

[<span data-ttu-id="661d0-258">Schritt 4: Verwenden einer Vorlage zum Erstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="661d0-258">Step 4: Use a template to create a GPO</span></span>](#bkmk-manage4)

[<span data-ttu-id="661d0-259">Schritt 5: Löschen und Wiederherstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="661d0-259">Step 5: Delete and restore a GPO</span></span>](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a><span data-ttu-id="661d0-260">Schritt 1: Erstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="661d0-260">Step 1: Create a GPO</span></span>

<span data-ttu-id="661d0-261">In einer Umgebung mit mehreren Gruppenrichtlinienadministratoren können Personen, die die Rolle des Editors besitzen, die Erstellung neuer GPOs anfordern, doch eine solche Anforderung muss von einer Person mit der Rolle Genehmiger genehmigt werden, da sich die Erstellung eines neuen Gruppenrichtlinienobjekts auf die Produktionsumgebung auswirkt.</span><span class="sxs-lookup"><span data-stu-id="661d0-261">In an environment with multiple Group Policy administrators, those with the Editor role have the ability to request the creation of new GPOs, but such a request must be approved by someone with the Approver role because the creation of a new GPO impacts the production environment.</span></span>

<span data-ttu-id="661d0-262">In diesem Schritt verwenden Sie ein Konto mit der Rolle "Editor", um die Erstellung eines neuen Gruppenrichtlinienobjekts anzufordern.</span><span class="sxs-lookup"><span data-stu-id="661d0-262">In this step, you use an account with the Editor role to request the creation of a new GPO.</span></span> <span data-ttu-id="661d0-263">Wenn Sie ein Konto mit der Rolle Genehmiger verwenden, genehmigen Sie diese Anforderung und schließen die Erstellung eines Gruppenrichtlinienobjekts ab.</span><span class="sxs-lookup"><span data-stu-id="661d0-263">Using an account with the Approver role, you approve this request and complete the creation of a GPO.</span></span>

**<span data-ttu-id="661d0-264">So fordern Sie die Erstellung eines über AGPM verwalteten neuen Gruppenrichtlinienobjekts an</span><span class="sxs-lookup"><span data-stu-id="661d0-264">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="661d0-265">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle des Editors in AGPM zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="661d0-265">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the Editor role in AGPM.</span></span>

2.  <span data-ttu-id="661d0-266">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="661d0-266">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="661d0-267">Klicken Sie mit der rechten Maustaste auf den Knoten **Change Control** , und klicken Sie dann auf **Neues gesteuertes Gruppenrichtlinienobjekt**.</span><span class="sxs-lookup"><span data-stu-id="661d0-267">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

4.  <span data-ttu-id="661d0-268">Im Dialogfeld " **Neues gesteuertes GPO** ":</span><span class="sxs-lookup"><span data-stu-id="661d0-268">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="661d0-269">Wenn Sie eine Kopie der Anfrage erhalten möchten, geben Sie Ihre e-Mail-Adresse in das Feld **CC** ein.</span><span class="sxs-lookup"><span data-stu-id="661d0-269">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="661d0-270">Geben Sie **eigenes** als Namen für das neue Gruppenrichtlinienobjekt ein.</span><span class="sxs-lookup"><span data-stu-id="661d0-270">Type **MyGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="661d0-271">Geben Sie einen Kommentar für das neue Gruppenrichtlinienobjekt ein.</span><span class="sxs-lookup"><span data-stu-id="661d0-271">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="661d0-272">Klicken Sie auf **Live erstellen** , damit das neue Gruppenrichtlinienobjekt unmittelbar nach der Genehmigung in der Produktionsumgebung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="661d0-272">Click **Create live** so the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="661d0-273">Klicken Sie auf **Übermitteln**.</span><span class="sxs-lookup"><span data-stu-id="661d0-273">Click **Submit**.</span></span>

5.  <span data-ttu-id="661d0-274">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="661d0-274">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="661d0-275">Das neue Gruppenrichtlinienobjekt wird auf der Registerkarte **Ausstehend** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="661d0-275">The new GPO is displayed on the **Pending** tab.</span></span>

**<span data-ttu-id="661d0-276">So genehmigen Sie die ausstehende Anforderung zum Erstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="661d0-276">To approve the pending request to create a GPO</span></span>**

1.  <span data-ttu-id="661d0-277">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle der genehmigenden Person in AGPM zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="661d0-277">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span>

2.  <span data-ttu-id="661d0-278">Öffnen Sie den e-Mail-Posteingang für das Konto, und beachten Sie, dass Sie eine e-Mail-Nachricht vom AGPM-Alias mit der Anforderung des Editors zum Erstellen eines Gruppenrichtlinienobjekts erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="661d0-278">Open the e-mail inbox for the account, and note that you have received an e-mail message from the AGPM alias with the Editor's request to create a GPO.</span></span>

3.  <span data-ttu-id="661d0-279">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="661d0-279">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="661d0-280">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **Ausstehend** , um die ausstehenden GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="661d0-280">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

5.  <span data-ttu-id="661d0-281">Klicken Sie mit der rechten Maustaste auf **eigenes**, und klicken Sie dann auf **genehmigen**.</span><span class="sxs-lookup"><span data-stu-id="661d0-281">Right-click **MyGPO**, and then click **Approve**.</span></span>

6.  <span data-ttu-id="661d0-282">Klicken Sie auf **Ja** , um die Genehmigung für die Erstellung des Gruppenrichtlinienobjekts zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="661d0-282">Click **Yes** to confirm approval of the creation of the GPO.</span></span> <span data-ttu-id="661d0-283">Das Gruppenrichtlinienobjekt wird auf die Registerkarte **gesteuert** verschoben.</span><span class="sxs-lookup"><span data-stu-id="661d0-283">The GPO is moved to the **Controlled** tab.</span></span>

### <a href="" id="bkmk-manage2"></a><span data-ttu-id="661d0-284">Schritt 2: Bearbeiten eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="661d0-284">Step 2: Edit a GPO</span></span>

<span data-ttu-id="661d0-285">Sie können GPOs verwenden, um Computer-oder Benutzereinstellungen zu konfigurieren und für viele Computer oder Benutzer bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="661d0-285">You can use GPOs to configure computer or user settings and deploy them to many computers or users.</span></span> <span data-ttu-id="661d0-286">In diesem Schritt verwenden Sie ein Konto mit der Rolle "Editor", um ein GPO aus dem Archiv auszuchecken, das Gruppenrichtlinienobjekt offline zu bearbeiten, das bearbeitete GPO in das Archiv zu überprüfen und die Bereitstellung des Gruppenrichtlinienobjekts in der Produktionsumgebung anzufordern.</span><span class="sxs-lookup"><span data-stu-id="661d0-286">In this step, you use an account with the Editor role to check out a GPO from the archive, edit the GPO offline, check the edited GPO into the archive, and request deployment of the GPO to the production environment.</span></span> <span data-ttu-id="661d0-287">In diesem Szenario konfigurieren Sie eine Einstellung im Gruppenrichtlinienobjekt, um zu erzwingen, dass das Kennwort mindestens acht Zeichen lang sein muss.</span><span class="sxs-lookup"><span data-stu-id="661d0-287">For this scenario, you configure a setting in the GPO to require that the password be at least eight characters in length.</span></span>

**<span data-ttu-id="661d0-288">So überprüfen Sie das Gruppenrichtlinienobjekt aus dem Archiv zur Bearbeitung</span><span class="sxs-lookup"><span data-stu-id="661d0-288">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="661d0-289">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle des Editors in AGPM zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="661d0-289">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="661d0-290">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="661d0-290">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="661d0-291">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="661d0-291">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="661d0-292">Klicken Sie mit der rechten Maustaste auf **eigenes**, und klicken Sie dann auf **Auschecken**.</span><span class="sxs-lookup"><span data-stu-id="661d0-292">Right-click **MyGPO**, and then click **Check Out**.</span></span>

5.  <span data-ttu-id="661d0-293">Geben Sie einen Kommentar ein, der im **Verlauf** des Gruppenrichtlinienobjekts angezeigt werden soll, während es ausgecheckt ist, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="661d0-293">Type a comment to be displayed in the **History** of the GPO while it is checked out, and then click **OK**.</span></span>

6.  <span data-ttu-id="661d0-294">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="661d0-294">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="661d0-295">Auf der Registerkarte **gesteuert** wird der Status des Gruppenrichtlinienobjekts als **ausgecheckt**identifiziert.</span><span class="sxs-lookup"><span data-stu-id="661d0-295">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="661d0-296">So bearbeiten Sie das Gruppenrichtlinienobjekt offline und konfigurieren die minimale Kennwortlänge</span><span class="sxs-lookup"><span data-stu-id="661d0-296">To edit the GPO offline and configure the minimum password length</span></span>**

1.  <span data-ttu-id="661d0-297">Klicken Sie auf der Registerkarte **gesteuert** mit der rechten Maustaste auf **eigenes**, und klicken Sie dann auf **Bearbeiten** , um das Fenster **Gruppenrichtlinienobjekt-Editor** zu öffnen und Änderungen an einer Offlinekopie des Gruppenrichtlinienobjekts vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="661d0-297">On the **Controlled** tab, right-click **MyGPO**, and then click **Edit** to open the **Group Policy Object Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="661d0-298">Konfigurieren Sie in diesem Szenario die minimale Kennwortlänge:</span><span class="sxs-lookup"><span data-stu-id="661d0-298">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="661d0-299">Doppelklicken Sie unter **Computer Konfiguration**auf **Windows-Einstellungen**, doppelklicken Sie auf **Sicherheitseinstellungen**, doppelklicken Sie auf **Kontorichtlinien**, und doppelklicken Sie auf **Kennwortrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="661d0-299">Under **Computer Configuration**, double-click **Windows Settings**, double-click **Security Settings**, double-click **Account Policies**, and double-click **Password Policy**.</span></span>

    2.  <span data-ttu-id="661d0-300">Doppelklicken Sie im Detailbereich auf **minimale Kennwortlänge**.</span><span class="sxs-lookup"><span data-stu-id="661d0-300">In the details pane, double-click **Minimum password length**.</span></span>

    3.  <span data-ttu-id="661d0-301">Aktivieren Sie im Eigenschaftenfenster das Kontrollkästchen **diese Richtlinieneinstellung definieren** , legen Sie die Anzahl der Zeichen auf **8**fest, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="661d0-301">In the properties window, select the **Define this policy setting** check box, set the number of characters to **8**, and then click **OK**.</span></span>

2.  <span data-ttu-id="661d0-302">Schließen Sie das Fenster des **Gruppenrichtlinienobjekt-Editors** .</span><span class="sxs-lookup"><span data-stu-id="661d0-302">Close the **Group Policy Object Editor** window.</span></span>

**<span data-ttu-id="661d0-303">So überprüfen Sie das Gruppenrichtlinienobjekt in das Archiv</span><span class="sxs-lookup"><span data-stu-id="661d0-303">To check the GPO into the archive</span></span>**

1.  <span data-ttu-id="661d0-304">Klicken Sie auf der Registerkarte **gesteuert** mit der rechten Maustaste auf **eigenes** , und klicken Sie dann auf **Einchecken**.</span><span class="sxs-lookup"><span data-stu-id="661d0-304">On the **Controlled** tab, right-click **MyGPO** and then click **Check In**.</span></span>

2.  <span data-ttu-id="661d0-305">Geben Sie einen Kommentar ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="661d0-305">Type a comment, and then click **OK**.</span></span>

3.  <span data-ttu-id="661d0-306">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="661d0-306">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="661d0-307">Auf der Registerkarte **gesteuert** wird der Status des Gruppenrichtlinienobjekts als **eingecheckt**gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="661d0-307">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

**<span data-ttu-id="661d0-308">So fordern Sie die Bereitstellung des Gruppenrichtlinienobjekts in der Produktionsumgebung an</span><span class="sxs-lookup"><span data-stu-id="661d0-308">To request the deployment of the GPO to the production environment</span></span>**

1.  <span data-ttu-id="661d0-309">Klicken Sie auf der Registerkarte **gesteuert** mit der rechten Maustaste auf **eigenes** , und klicken Sie dann auf **Bereitstellen**.</span><span class="sxs-lookup"><span data-stu-id="661d0-309">On the **Controlled** tab, right-click **MyGPO** and then click **Deploy**.</span></span>

2.  <span data-ttu-id="661d0-310">Da es sich bei diesem Konto nicht um eine genehmigende Person oder einen AGPM-Administrator handelt, müssen Sie eine Anforderung für die Bereitstellung einreichen.</span><span class="sxs-lookup"><span data-stu-id="661d0-310">Because this account is not an Approver or AGPM Administrator, you must submit a request for deployment.</span></span> <span data-ttu-id="661d0-311">Wenn Sie eine Kopie der Anfrage erhalten möchten, geben Sie Ihre e-Mail-Adresse in das Feld **CC** ein.</span><span class="sxs-lookup"><span data-stu-id="661d0-311">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="661d0-312">Geben Sie einen Kommentar ein, der im **Verlauf** des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **Absenden**.</span><span class="sxs-lookup"><span data-stu-id="661d0-312">Type a comment to be displayed in the **History** of the GPO, and then click **Submit**.</span></span>

3.  <span data-ttu-id="661d0-313">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="661d0-313">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="661d0-314">**Eigenes** wird in der Liste der GPOs auf der Registerkarte **Ausstehend** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="661d0-314">**MyGPO** is displayed on the list of GPOs on the **Pending** tab.</span></span>

### <a href="" id="bkmk-manage3"></a><span data-ttu-id="661d0-315">Schritt 3: überprüfen und Bereitstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="661d0-315">Step 3: Review and deploy a GPO</span></span>

<span data-ttu-id="661d0-316">In diesem Schritt fungieren Sie als genehmigende Person, erstellen Berichte und analysieren die Einstellungen und Änderungen an den Einstellungen im Gruppenrichtlinienobjekt, um festzustellen, ob Sie diese genehmigen sollten.</span><span class="sxs-lookup"><span data-stu-id="661d0-316">In this step, you act as an Approver, creating reports and analyzing the settings and changes to settings in the GPO to determine whether you should approve them.</span></span> <span data-ttu-id="661d0-317">Nachdem Sie das Gruppenrichtlinienobjekt ausgewertet haben, stellen Sie es in der Produktionsumgebung bereit, und verknüpfen Sie es mit einer Domäne oder einer Organisationseinheit, damit es wirksam wird, wenn die Gruppenrichtlinie für Computer in dieser Domäne oder OU aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="661d0-317">After evaluating the GPO, you deploy it to the production environment and link it to a domain or an organizational unit (OU) so that it takes effect when Group Policy is refreshed for computers in that domain or OU.</span></span>

**<span data-ttu-id="661d0-318">So überprüfen Sie die Einstellungen im Gruppenrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="661d0-318">To review settings in the GPO</span></span>**

1.  <span data-ttu-id="661d0-319">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle der genehmigenden Person in AGPM zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="661d0-319">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span> <span data-ttu-id="661d0-320">(Jeder Gruppenrichtlinienadministrator mit der Rolle Prüfer, der in allen anderen Rollen enthalten ist, kann die Einstellungen in einem Gruppenrichtlinienobjekt überprüfen.)</span><span class="sxs-lookup"><span data-stu-id="661d0-320">(Any Group Policy administrator with the Reviewer role, which is included in all of the other roles, can review the settings in a GPO.)</span></span>

2.  <span data-ttu-id="661d0-321">Öffnen Sie den e-Mail-Posteingang für das Konto, und beachten Sie, dass Sie eine e-Mail-Nachricht vom AGPM-Alias mit der Anforderung eines Editors zum Bereitstellen eines Gruppenrichtlinienobjekts erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="661d0-321">Open the e-mail inbox for the account and note that you have received an e-mail message from the AGPM alias with an Editor's request to deploy a GPO.</span></span>

3.  <span data-ttu-id="661d0-322">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="661d0-322">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="661d0-323">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **Ausstehend** .</span><span class="sxs-lookup"><span data-stu-id="661d0-323">On the **Contents** tab in the details pane, click the **Pending** tab.</span></span>

5.  <span data-ttu-id="661d0-324">Doppelklicken Sie auf **eigenes** , um dessen Verlauf anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="661d0-324">Double-click **MyGPO** to display its history.</span></span>

6.  <span data-ttu-id="661d0-325">Überprüfen Sie die Einstellungen in der neuesten Version von eigenes:</span><span class="sxs-lookup"><span data-stu-id="661d0-325">Review the settings in the most recent version of MyGPO:</span></span>

    1.  <span data-ttu-id="661d0-326">Klicken Sie im **Verlaufs** Fenster mit der rechten Maustaste auf die GPO-Version mit dem neuesten Zeitstempel, klicken Sie auf **Einstellungen**, und klicken Sie dann auf **HTML-Bericht** , um eine Zusammenfassung der GPO-Einstellungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="661d0-326">In the **History** window, right-click the GPO version with the most recent timestamp, click **Settings**, and then click **HTML Report** to display a summary of the GPO's settings.</span></span>

    2.  <span data-ttu-id="661d0-327">Klicken Sie im Webbrowser auf **Alle anzeigen** , um alle Einstellungen im Gruppenrichtlinienobjekt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="661d0-327">In the Web browser, click **show all** to display all of the settings in the GPO.</span></span>

    3.  <span data-ttu-id="661d0-328">Schließen Sie den Browser.</span><span class="sxs-lookup"><span data-stu-id="661d0-328">Close the browser.</span></span>

7.  <span data-ttu-id="661d0-329">Vergleichen Sie die neueste Version von eigenes mit der ersten Version, die in das Archiv eingecheckt wurde:</span><span class="sxs-lookup"><span data-stu-id="661d0-329">Compare the most recent version of MyGPO to the first version checked in to the archive:</span></span>

    1.  <span data-ttu-id="661d0-330">Klicken Sie im Fenster " **Verlauf** " auf die GPO-Version mit dem aktuellsten Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="661d0-330">In the **History** window, click the GPO version with the most recent timestamp.</span></span> <span data-ttu-id="661d0-331">Drücken Sie **STRG** , und klicken Sie auf die älteste GPO-Version mit dem Status **eingecheckt**.</span><span class="sxs-lookup"><span data-stu-id="661d0-331">Press **CTRL** and click the oldest GPO version that has a state of **Checked In**.</span></span>

    2.  <span data-ttu-id="661d0-332">Klicken Sie auf die Schaltfläche **Unterschiede** .</span><span class="sxs-lookup"><span data-stu-id="661d0-332">Click the **Differences** button.</span></span> <span data-ttu-id="661d0-333">Der Abschnitt **Kontorichtlinien/Kennwortrichtlinie** ist grün hervorgehoben und wird mit **\ [+ \]** vorangestellt, was darauf hinweist, dass diese Einstellung nur in der letzten Version des Gruppenrichtlinienobjekts konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="661d0-333">The **Account Policies/Password Policy** section is highlighted in green and preceded by **\[+\]**, indicating that this setting is configured only in the latter version of the GPO.</span></span>

    3.  <span data-ttu-id="661d0-334">Klicken Sie auf **Kontorichtlinien/Kennwortrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="661d0-334">Click **Account Policies/Password Policy**.</span></span> <span data-ttu-id="661d0-335">Die Einstellung **minimale Kennwortlänge** ist auch in grün hervorgehoben und mit **\ [+ \]** gekennzeichnet, was darauf hinweist, dass Sie nur in der letzten Version des Gruppenrichtlinienobjekts konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="661d0-335">The **Minimum password length** setting is also highlighted in green and preceded by **\[+\]**, indicating that it is configured only in the latter version of the GPO.</span></span>

    4.  <span data-ttu-id="661d0-336">Schließen Sie den Webbrowser.</span><span class="sxs-lookup"><span data-stu-id="661d0-336">Close the Web browser.</span></span>

**<span data-ttu-id="661d0-337">So stellen Sie das Gruppenrichtlinienobjekt in der Produktionsumgebung bereit</span><span class="sxs-lookup"><span data-stu-id="661d0-337">To deploy the GPO to the production environment</span></span>**

1.  <span data-ttu-id="661d0-338">Klicken Sie auf der Registerkarte **Ausstehend** mit der rechten Maustaste auf **eigenes** , und klicken Sie dann auf **genehmigen**.</span><span class="sxs-lookup"><span data-stu-id="661d0-338">On the **Pending** tab, right-click **MyGPO** and then click **Approve**.</span></span>

2.  <span data-ttu-id="661d0-339">Geben Sie einen Kommentar ein, der in das Protokoll des Gruppenrichtlinienobjekts aufgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="661d0-339">Type a comment to include in the history of the GPO.</span></span>

3.  <span data-ttu-id="661d0-340">Klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="661d0-340">Click **Yes**.</span></span> <span data-ttu-id="661d0-341">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="661d0-341">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="661d0-342">Das Gruppenrichtlinienobjekt wird in der Produktionsumgebung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="661d0-342">The GPO is deployed to the production environment.</span></span>

**<span data-ttu-id="661d0-343">So verknüpfen Sie das Gruppenrichtlinienobjekt mit einer Domäne oder Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="661d0-343">To link the GPO to a domain or organizational unit</span></span>**

1.  <span data-ttu-id="661d0-344">Klicken Sie in der GPMC mit der rechten Maustaste auf die Domäne oder auf eine Organisationseinheit, auf die das von Ihnen konfigurierte Gruppenrichtlinienobjekt angewendet werden soll, und klicken Sie dann auf **vorhandenes Gruppenrichtlinienobjekt verknüpfen**.</span><span class="sxs-lookup"><span data-stu-id="661d0-344">In the GPMC, right-click the domain or an OU to which to apply the GPO that you configured, and then click **Link an Existing GPO**.</span></span>

2.  <span data-ttu-id="661d0-345">Klicken Sie im Dialogfeld **GPO auswählen** auf **eigenes**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="661d0-345">In the **Select GPO** dialog box, click **MyGPO**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage4"></a><span data-ttu-id="661d0-346">Schritt 4: Verwenden einer Vorlage zum Erstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="661d0-346">Step 4: Use a template to create a GPO</span></span>

<span data-ttu-id="661d0-347">In diesem Schritt verwenden Sie ein Konto mit der Rolle "Editor", um eine Vorlage zu erstellen – eine nicht bearbeitbare, statische Version eines GPO, die als Ausgangspunkt zum Erstellen neuer GPOs verwendet werden soll, und dann basierend auf dieser Vorlage ein neues Gruppenrichtlinienobjekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="661d0-347">In this step, you use an account with the Editor role to create a template—an uneditable, static version of a GPO for use as a starting point for creating new GPOs—and then create a new GPO based upon that template.</span></span> <span data-ttu-id="661d0-348">Vorlagen sind hilfreich für das schnelle Erstellen mehrerer GPOs, in denen viele der gleichen Einstellungen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="661d0-348">Templates are useful for quickly creating multiple GPOs that include many of the same settings.</span></span>

**<span data-ttu-id="661d0-349">So erstellen Sie eine Vorlage auf der Grundlage eines vorhandenen Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="661d0-349">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="661d0-350">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle des Editors in AGPM zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="661d0-350">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="661d0-351">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="661d0-351">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="661d0-352">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** .</span><span class="sxs-lookup"><span data-stu-id="661d0-352">On the **Contents** tab in the details pane, click the **Controlled** tab.</span></span>

4.  <span data-ttu-id="661d0-353">Klicken Sie mit der rechten Maustaste auf **eigenes**, und klicken Sie dann auf **als Vorlage speichern** , um eine Vorlage zu erstellen, die alle Einstellungen umfasst, die derzeit in eigenes enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="661d0-353">Right-click **MyGPO**, and then click **Save as Template** to create a template incorporating all settings currently in MyGPO.</span></span>

5.  <span data-ttu-id="661d0-354">Geben Sie **MyTemplate** als Namen für die Vorlage und einen Kommentar ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="661d0-354">Type **MyTemplate** as the name for the template and a comment, and then click **OK**.</span></span>

6.  <span data-ttu-id="661d0-355">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="661d0-355">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="661d0-356">Die neue Vorlage wird auf der Registerkarte **Vorlagen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="661d0-356">The new template appears on the **Templates** tab.</span></span>

**<span data-ttu-id="661d0-357">So fordern Sie die Erstellung eines über AGPM verwalteten neuen Gruppenrichtlinienobjekts an</span><span class="sxs-lookup"><span data-stu-id="661d0-357">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="661d0-358">Klicken Sie auf die Registerkarte **gesteuert** .</span><span class="sxs-lookup"><span data-stu-id="661d0-358">Click the **Controlled** tab.</span></span>

2.  <span data-ttu-id="661d0-359">Klicken Sie mit der rechten Maustaste auf den Knoten **Change Control** , und klicken Sie dann auf **Neues gesteuertes Gruppenrichtlinienobjekt**.</span><span class="sxs-lookup"><span data-stu-id="661d0-359">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="661d0-360">Im Dialogfeld " **Neues gesteuertes GPO** ":</span><span class="sxs-lookup"><span data-stu-id="661d0-360">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="661d0-361">Wenn Sie eine Kopie der Anfrage erhalten möchten, geben Sie Ihre e-Mail-Adresse in das Feld **CC** ein.</span><span class="sxs-lookup"><span data-stu-id="661d0-361">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="661d0-362">Geben Sie **Gruppenrichtlinienverwaltungs** als Namen für das neue Gruppenrichtlinienobjekt ein.</span><span class="sxs-lookup"><span data-stu-id="661d0-362">Type **MyOtherGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="661d0-363">Geben Sie einen Kommentar für das neue Gruppenrichtlinienobjekt ein.</span><span class="sxs-lookup"><span data-stu-id="661d0-363">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="661d0-364">Klicken Sie auf **Live erstellen**, damit das neue Gruppenrichtlinienobjekt unmittelbar nach der Genehmigung in der Produktionsumgebung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="661d0-364">Click **Create live**, so the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="661d0-365">Wählen Sie für **aus GPO-Vorlage**die Option meine **Vorlage**aus.</span><span class="sxs-lookup"><span data-stu-id="661d0-365">For **From GPO template**, select **MyTemplate**.</span></span>

    6.  <span data-ttu-id="661d0-366">Klicken Sie auf **Übermitteln**.</span><span class="sxs-lookup"><span data-stu-id="661d0-366">Click **Submit**.</span></span>

4.  <span data-ttu-id="661d0-367">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="661d0-367">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="661d0-368">Das neue Gruppenrichtlinienobjekt wird auf der Registerkarte **Ausstehend** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="661d0-368">The new GPO is displayed on the **Pending** tab.</span></span>

<span data-ttu-id="661d0-369">Verwenden Sie ein Konto, dem die Rolle der genehmigenden Person zugewiesen wurde, um die ausstehende Anforderung zum Erstellen des Gruppenrichtlinienobjekts zu genehmigen, wie in [Schritt 1: Erstellen eines Gruppenrichtlinienobjekts](#bkmk-manage1).</span><span class="sxs-lookup"><span data-stu-id="661d0-369">Use an account that has been assigned the role of Approver to approve the pending request to create the GPO as you did in [Step 1: Create a GPO](#bkmk-manage1).</span></span> <span data-ttu-id="661d0-370">MyTemplate enthält alle Einstellungen, die Sie in eigenes konfiguriert haben.</span><span class="sxs-lookup"><span data-stu-id="661d0-370">MyTemplate incorporates all of the settings that you configured in MyGPO.</span></span> <span data-ttu-id="661d0-371">Da Gruppenrichtlinienverwaltungs mit MyTemplate erstellt wurde, enthält es zunächst alle Einstellungen, die eigenes zum Zeitpunkt der Erstellung von MyTemplate enthielt.</span><span class="sxs-lookup"><span data-stu-id="661d0-371">Because MyOtherGPO was created using MyTemplate, it initially contains all of the settings that MyGPO contained at the time that MyTemplate was created.</span></span> <span data-ttu-id="661d0-372">Sie können dies bestätigen, indem Sie einen Differenz Bericht generieren, um Gruppenrichtlinienverwaltungs mit MyTemplate zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="661d0-372">You can confirm this by generating a difference report to compare MyOtherGPO to MyTemplate.</span></span>

**<span data-ttu-id="661d0-373">So überprüfen Sie das Gruppenrichtlinienobjekt aus dem Archiv zur Bearbeitung</span><span class="sxs-lookup"><span data-stu-id="661d0-373">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="661d0-374">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle des Editors in AGPM zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="661d0-374">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="661d0-375">Klicken Sie mit der rechten Maustaste auf **Gruppenrichtlinienverwaltungs**, und klicken Sie dann auf **Auschecken**.</span><span class="sxs-lookup"><span data-stu-id="661d0-375">Right-click **MyOtherGPO**, and then click **Check Out**.</span></span>

3.  <span data-ttu-id="661d0-376">Geben Sie einen Kommentar ein, der im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, während es ausgecheckt ist, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="661d0-376">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

4.  <span data-ttu-id="661d0-377">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="661d0-377">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="661d0-378">Auf der Registerkarte **gesteuert** wird der Status des Gruppenrichtlinienobjekts als **ausgecheckt**identifiziert.</span><span class="sxs-lookup"><span data-stu-id="661d0-378">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="661d0-379">So bearbeiten Sie das Gruppenrichtlinienobjekt offline und konfigurieren die Kontosperrungsdauer</span><span class="sxs-lookup"><span data-stu-id="661d0-379">To edit the GPO offline and configure the account lockout duration</span></span>**

1.  <span data-ttu-id="661d0-380">Klicken Sie auf der Registerkarte **gesteuert** mit der rechten Maustaste auf **Gruppenrichtlinienverwaltungs**, und klicken Sie dann auf **Bearbeiten** , um das Fenster **Gruppenrichtlinienobjekt-Editor** zu öffnen und Änderungen an einer Offlinekopie des Gruppenrichtlinienobjekts vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="661d0-380">On the **Controlled** tab, right-click **MyOtherGPO**, and then click **Edit** to open the **Group Policy Object Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="661d0-381">Konfigurieren Sie in diesem Szenario die minimale Kennwortlänge:</span><span class="sxs-lookup"><span data-stu-id="661d0-381">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="661d0-382">Doppelklicken Sie unter **Computer Konfiguration**auf **Windows-Einstellungen**, doppelklicken Sie auf **Sicherheitseinstellungen**, doppelklicken Sie auf **Kontorichtlinien**, und doppelklicken Sie auf **Kontosperrungsrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="661d0-382">Under **Computer Configuration**, double-click **Windows Settings**, double-click **Security Settings**, double-click **Account Policies**, and double-click **Account Lockout Policy**.</span></span>

    2.  <span data-ttu-id="661d0-383">Doppelklicken Sie im Detailbereich auf **Kontosperrungsdauer**.</span><span class="sxs-lookup"><span data-stu-id="661d0-383">In the details pane, double-click **Account lockout duration**.</span></span>

    3.  <span data-ttu-id="661d0-384">Aktivieren Sie im Fenster Eigenschaften die Option **diese Richtlinieneinstellung definieren**, legen Sie die Dauer auf **30** Minuten fest, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="661d0-384">In the properties window, check **Define this policy setting**, set the duration to **30** minutes, and then click **OK**.</span></span>

2.  <span data-ttu-id="661d0-385">Schließen Sie das Fenster des **Gruppenrichtlinienobjekt-Editors** .</span><span class="sxs-lookup"><span data-stu-id="661d0-385">Close the **Group Policy Object Editor** window.</span></span>

<span data-ttu-id="661d0-386">Überprüfen Sie Gruppenrichtlinienverwaltungs in die Archivierungs-und Anforderungs Bereitstellung wie bei eigenes in [Schritt 2: Bearbeiten eines Gruppenrichtlinienobjekts](#bkmk-manage2).</span><span class="sxs-lookup"><span data-stu-id="661d0-386">Check MyOtherGPO into the archive and request deployment as you did for MyGPO in [Step 2: Edit a GPO](#bkmk-manage2).</span></span> <span data-ttu-id="661d0-387">Sie können Gruppenrichtlinienverwaltungs mit eigenes oder mit MyTemplate mithilfe von Unterschiedsberichten vergleichen.</span><span class="sxs-lookup"><span data-stu-id="661d0-387">You can compare MyOtherGPO to MyGPO or to MyTemplate using difference reports.</span></span> <span data-ttu-id="661d0-388">Jedes Konto, das die Rolle Prüfer enthält (AGPM-Administrator \ [Vollzugriff \], genehmigende Person, Bearbeiter oder Bearbeiter) kann Berichte generieren.</span><span class="sxs-lookup"><span data-stu-id="661d0-388">Any account that includes the Reviewer role (AGPM Administrator \[Full Control\], Approver, Editor, or Reviewer) can generate reports.</span></span>

**<span data-ttu-id="661d0-389">So vergleichen Sie ein GPO mit einem anderen Gruppenrichtlinienobjekt und einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="661d0-389">To compare a GPO to another GPO and to a template</span></span>**

1.  <span data-ttu-id="661d0-390">So vergleichen Sie eigenes und Gruppenrichtlinienverwaltungs:</span><span class="sxs-lookup"><span data-stu-id="661d0-390">To compare MyGPO and MyOtherGPO:</span></span>

    1.  <span data-ttu-id="661d0-391">Klicken Sie auf der Registerkarte **gesteuert** auf **eigenes**.</span><span class="sxs-lookup"><span data-stu-id="661d0-391">On the **Controlled** tab, click **MyGPO**.</span></span> <span data-ttu-id="661d0-392">Drücken Sie **STRG** , und klicken Sie dann auf **Gruppenrichtlinienverwaltungs**.</span><span class="sxs-lookup"><span data-stu-id="661d0-392">Press **CTRL** and then click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="661d0-393">Klicken Sie mit der rechten Maustaste auf **Gruppenrichtlinienverwaltungs**, zeigen Sie auf **Unterschiede**, und klicken Sie auf **HTML-Bericht**.</span><span class="sxs-lookup"><span data-stu-id="661d0-393">Right-click **MyOtherGPO**, point to **Differences**, and click **HTML Report**.</span></span>

2.  <span data-ttu-id="661d0-394">So vergleichen Sie Gruppenrichtlinienverwaltungs und MyTemplate:</span><span class="sxs-lookup"><span data-stu-id="661d0-394">To compare MyOtherGPO and MyTemplate:</span></span>

    1.  <span data-ttu-id="661d0-395">Klicken Sie auf der Registerkarte **gesteuert** auf **Gruppenrichtlinienverwaltungs**.</span><span class="sxs-lookup"><span data-stu-id="661d0-395">On the **Controlled** tab, click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="661d0-396">Klicken Sie mit der rechten Maustaste auf **Gruppenrichtlinienverwaltungs**, zeigen Sie auf **Unterschiede**, und klicken Sie auf **Vorlage**.</span><span class="sxs-lookup"><span data-stu-id="661d0-396">Right-click **MyOtherGPO**, point to **Differences**, and click **Template**.</span></span>

    3.  <span data-ttu-id="661d0-397">Wählen Sie **MyTemplate** und **HTML-Bericht**aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="661d0-397">Select **MyTemplate** and **HTML Report**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage5"></a><span data-ttu-id="661d0-398">Schritt 5: Löschen und Wiederherstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="661d0-398">Step 5: Delete and restore a GPO</span></span>

<span data-ttu-id="661d0-399">In diesem Schritt fungieren Sie als genehmigende Person, um ein GPO zu löschen.</span><span class="sxs-lookup"><span data-stu-id="661d0-399">In this step, you act as an Approver to delete a GPO.</span></span>

**<span data-ttu-id="661d0-400">So löschen Sie ein Gruppenrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="661d0-400">To delete a GPO</span></span>**

1.  <span data-ttu-id="661d0-401">Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle der genehmigenden Person zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="661d0-401">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver.</span></span>

2.  <span data-ttu-id="661d0-402">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="661d0-402">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="661d0-403">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="661d0-403">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="661d0-404">Klicken Sie mit der rechten Maustaste auf **eigenes**, und klicken Sie dann auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="661d0-404">Right-click **MyGPO**, and then click **Delete**.</span></span> <span data-ttu-id="661d0-405">Klicken Sie auf **Gruppenrichtlinienobjekt aus Archiv und Produktion löschen** , um sowohl die Version im Archiv als auch die bereitgestellte Version des Gruppenrichtlinienobjekts in der Produktionsumgebung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="661d0-405">Click **Delete GPO from archive and production** to delete both the version in the archive as well as the deployed version of the GPO in the production environment.</span></span>

5.  <span data-ttu-id="661d0-406">Geben Sie einen Kommentar ein, der im Überwachungspfad für das Gruppenrichtlinienobjekt angezeigt werden soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="661d0-406">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

6.  <span data-ttu-id="661d0-407">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="661d0-407">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="661d0-408">Das Gruppenrichtlinienobjekt wird von der Registerkarte " **gesteuert** " entfernt und auf der Registerkarte " **Papierkorb** " angezeigt, wo es wiederhergestellt oder gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="661d0-408">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

<span data-ttu-id="661d0-409">Gelegentlich können Sie nach dem Löschen eines GPO feststellen, dass es noch benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="661d0-409">Occasionally you may discover after deleting a GPO that it is still needed.</span></span> <span data-ttu-id="661d0-410">In diesem Schritt fungieren Sie als genehmigende Person zum Wiederherstellen eines gelöschten Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="661d0-410">In this step, you act as an Approver to restore a GPO that has been deleted.</span></span>

**<span data-ttu-id="661d0-411">So stellen Sie ein gelöschtes Gruppenrichtlinienobjekt wieder her</span><span class="sxs-lookup"><span data-stu-id="661d0-411">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="661d0-412">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **Papierkorb** , um gelöschte GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="661d0-412">On the **Contents** tab, click the **Recycle Bin** tab to display deleted GPOs.</span></span>

2.  <span data-ttu-id="661d0-413">Klicken Sie mit der rechten Maustaste auf **eigenes**, und klicken Sie dann auf **Wiederherstellen**.</span><span class="sxs-lookup"><span data-stu-id="661d0-413">Right-click **MyGPO**, and then click **Restore**.</span></span>

3.  <span data-ttu-id="661d0-414">Geben Sie einen Kommentar ein, der im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="661d0-414">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="661d0-415">Wenn im Fenster " **AGPM-Status** " angezeigt wird, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="661d0-415">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="661d0-416">Das Gruppenrichtlinienobjekt wird von der Registerkarte " **Papierkorb** " entfernt und auf der Registerkarte " **gesteuert** " angezeigt.</span><span class="sxs-lookup"><span data-stu-id="661d0-416">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

    <span data-ttu-id="661d0-417">**Hinweis**  Wenn Sie ein GPO im Archiv wiederherstellen, wird es nicht automatisch in der Produktionsumgebung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="661d0-417">**Note** Restoring a GPO to the archive does not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="661d0-418">Wenn Sie das Gruppenrichtlinienobjekt an die Produktionsumgebung zurückgeben möchten, stellen Sie das Gruppenrichtlinienobjekt wie in [Schritt 3: überprüfen und Bereitstellen eines Gruppenrichtlinien](#bkmk-manage3)Objekts bereit.</span><span class="sxs-lookup"><span data-stu-id="661d0-418">To return the GPO to the production environment, deploy the GPO as in [Step 3: Review and deploy a GPO](#bkmk-manage3).</span></span>

     

<span data-ttu-id="661d0-419">Nachdem Sie ein GPO bearbeitet und bereitgestellt haben, stellen Sie möglicherweise fest, dass die letzten Änderungen am Gruppenrichtlinienobjekt ein Problem verursachen.</span><span class="sxs-lookup"><span data-stu-id="661d0-419">After editing and deploying a GPO, you may discover that recent changes to the GPO are causing a problem.</span></span> <span data-ttu-id="661d0-420">In diesem Schritt fungieren Sie als genehmigende Person, um einen Rollback zu einer früheren Version des Gruppenrichtlinienobjekts durchführen zu können.</span><span class="sxs-lookup"><span data-stu-id="661d0-420">In this step, you act as an Approver to roll back to a previous version of the GPO.</span></span> <span data-ttu-id="661d0-421">Sie können einen Rollback zu einer beliebigen Version im Verlauf des Gruppenrichtlinienobjekts ausführen.</span><span class="sxs-lookup"><span data-stu-id="661d0-421">You can roll back to any version in the history of the GPO.</span></span> <span data-ttu-id="661d0-422">Sie können Kommentare und Beschriftungen verwenden, um bekannte gute Versionen zu identifizieren und wenn bestimmte Änderungen vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="661d0-422">You can use comments and labels to identify known good versions and when specific changes were made.</span></span>

**<span data-ttu-id="661d0-423">So führen Sie einen Rollback zu einer früheren Version eines GPO durch</span><span class="sxs-lookup"><span data-stu-id="661d0-423">To roll back to a previous version of a GPO</span></span>**

1.  <span data-ttu-id="661d0-424">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="661d0-424">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

2.  <span data-ttu-id="661d0-425">Doppelklicken Sie auf **eigenes** , um dessen Verlauf anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="661d0-425">Double-click **MyGPO** to display its history.</span></span>

3.  <span data-ttu-id="661d0-426">Klicken Sie mit der rechten Maustaste auf die bereit **zustellende**Version, klicken Sie auf bereitstellen, und klicken Sie dann auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="661d0-426">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

4.  <span data-ttu-id="661d0-427">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="661d0-427">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="661d0-428">Klicken Sie im Fenster **Verlauf** auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="661d0-428">In the **History** window, click **Close**.</span></span>

    <span data-ttu-id="661d0-429">**Hinweis**  Um zu überprüfen, ob die Version, die erneut bereitgestellt wurde, die beabsichtigte Version ist, untersuchen Sie einen Unterschiedsbericht für die beiden Versionen.</span><span class="sxs-lookup"><span data-stu-id="661d0-429">**Note** To verify that the version that has been redeployed is the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="661d0-430">Wählen Sie im Fenster **Verlauf** für das Gruppenrichtlinienobjekt die beiden Versionen aus, klicken Sie mit der rechten Maustaste darauf, zeigen Sie auf **Differenz**, und klicken Sie dann auf **HTML-Bericht** oder **XML-Bericht**.</span><span class="sxs-lookup"><span data-stu-id="661d0-430">In the **History** window for the GPO, select the two versions, right-click them, point to **Difference**, and then click either **HTML Report** or **XML Report**.</span></span>

     

 

 





