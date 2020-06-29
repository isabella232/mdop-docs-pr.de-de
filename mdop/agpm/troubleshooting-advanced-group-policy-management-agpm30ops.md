---
title: Problembehandlung bei Advanced Group Policy Management
description: Problembehandlung bei Advanced Group Policy Management
author: dansimp
ms.assetid: f7ece97c-e9f8-4b18-8c7a-a615c98d5c60
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4815378a17a7c083501cfd7772e62415ec285237
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808203"
---
# <span data-ttu-id="93f77-103">Problembehandlung bei Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="93f77-103">Troubleshooting Advanced Group Policy Management</span></span>


<span data-ttu-id="93f77-104">In diesem Abschnitt werden häufige Probleme aufgeführt, die bei der Verwendung der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) zum Verwalten von Gruppenrichtlinienobjekten (Group Policy Objects, GPOs) auftreten können.</span><span class="sxs-lookup"><span data-stu-id="93f77-104">This section lists common issues that you may encounter when you use Advanced Group Policy Management (AGPM) to manage Group Policy Objects (GPOs).</span></span> <span data-ttu-id="93f77-105">Wenn Sie Probleme diagnostizieren möchten, die hier nicht aufgeführt sind, kann es für einen AGPM-Administrator (Vollzugriff) hilfreich sein, Protokollierung und Ablaufverfolgung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="93f77-105">To diagnose issues not listed here, it may be helpful for an AGPM Administrator (Full Control) to use logging and tracing.</span></span> <span data-ttu-id="93f77-106">Weitere Informationen finden Sie unter [Konfigurieren der Protokollierung und Ablaufverfolgung](configure-logging-and-tracing-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="93f77-106">For more information, see [Configure Logging and Tracing](configure-logging-and-tracing-agpm30ops.md).</span></span>

**<span data-ttu-id="93f77-107">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="93f77-107">Note</span></span>**  
-   <span data-ttu-id="93f77-108">Informationen zum Zurücksetzen auf eine frühere Version eines GPO, wenn Probleme auftreten, finden Sie unter [Rollback zu einer früheren Version eines Gruppenrichtlinienobjekts](roll-back-to-a-previous-version-of-a-gpo-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="93f77-108">For information about rolling back to an earlier version of a GPO if there are problems, see [Roll Back to a Previous Version of a GPO](roll-back-to-a-previous-version-of-a-gpo-agpm30ops.md).</span></span>

-   <span data-ttu-id="93f77-109">Informationen dazu, wie Sie nach einem Notfall wiederherstellen können, indem Sie das vollständige Archiv aus einer Sicherung wiederherstellen, finden Sie unter [Wiederherstellen des Archivs aus einer Sicherung](restore-the-archive-from-a-backup.md).</span><span class="sxs-lookup"><span data-stu-id="93f77-109">For information about how to recover from a disaster by restoring the complete archive from a backup, see [Restore the Archive from a Backup](restore-the-archive-from-a-backup.md).</span></span>

 

## <span data-ttu-id="93f77-110">Welche Probleme haben Sie?</span><span class="sxs-lookup"><span data-stu-id="93f77-110">What problems are you having?</span></span>


-   [<span data-ttu-id="93f77-111">Ich kann nicht auf ein Archiv zugreifen</span><span class="sxs-lookup"><span data-stu-id="93f77-111">I am unable to access an archive</span></span>](#bkmk-access-an-archive)

-   [<span data-ttu-id="93f77-112">Der GPO-Status variiert für verschiedene Gruppenrichtlinienadministratoren</span><span class="sxs-lookup"><span data-stu-id="93f77-112">The GPO state varies for different Group Policy administrators</span></span>](#bkmk-state-varies)

-   [<span data-ttu-id="93f77-113">Ich kann die AGPM-Server Verbindung nicht ändern</span><span class="sxs-lookup"><span data-stu-id="93f77-113">I am unable to modify the AGPM Server connection</span></span>](#bkmk-modify-archive-location)

-   [<span data-ttu-id="93f77-114">Ich kann die Standardvorlage oder das anzeigen, erstellen, bearbeiten, umbenennen, bereitstellen oder Löschen von GPOs nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="93f77-114">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>](#bkmk-perform-task)

-   [<span data-ttu-id="93f77-115">Ich kann einen bestimmten GPO-Namen nicht verwenden</span><span class="sxs-lookup"><span data-stu-id="93f77-115">I am unable to use a particular GPO name</span></span>](#bkmk-use-particular-name)

-   [<span data-ttu-id="93f77-116">Ich erhalte keine AGPM-e-Mail-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="93f77-116">I am not receiving AGPM e-mail notifications</span></span>](#bkmk-email)

-   [<span data-ttu-id="93f77-117">Ich kann Port 4600 für den AGPM-Dienst nicht verwenden</span><span class="sxs-lookup"><span data-stu-id="93f77-117">I cannot use port 4600 for the AGPM Service</span></span>](#bkmk-port)

-   [<span data-ttu-id="93f77-118">Der AGPM-Dienst wird nicht gestartet</span><span class="sxs-lookup"><span data-stu-id="93f77-118">The AGPM Service will not start</span></span>](#bkmk-not-start)

-   [<span data-ttu-id="93f77-119">Software Installation für Gruppenrichtlinien kann nicht installiert werden</span><span class="sxs-lookup"><span data-stu-id="93f77-119">Group Policy Software Installation fails to install software</span></span>](#bkmk-software-installation)

-   [<span data-ttu-id="93f77-120">Beim Wiederherstellen des Archivs auf einem neuen AGPM-Server ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="93f77-120">An error occurred when I restored the archive to a new AGPM Server</span></span>](#bkmk-error-on-restore)

### <a href="" id="bkmk-access-an-archive"></a><span data-ttu-id="93f77-121">Ich kann nicht auf ein Archiv zugreifen</span><span class="sxs-lookup"><span data-stu-id="93f77-121">I am unable to access an archive</span></span>

-   <span data-ttu-id="93f77-122">**Ursache**: Sie haben nicht den richtigen Server und Port für das Archiv ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="93f77-122">**Cause**: You have not selected the correct server and port for the archive.</span></span>

-   <span data-ttu-id="93f77-123">**Lösung**:</span><span class="sxs-lookup"><span data-stu-id="93f77-123">**Solution**:</span></span>

    -   <span data-ttu-id="93f77-124">Wenn Sie ein AGPM-Administrator sind, lesen Sie [Konfigurieren von AGPM-Server Verbindungen](configure-agpm-server-connections-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="93f77-124">If you are an AGPM Administrator: See [Configure AGPM Server Connections](configure-agpm-server-connections-agpm30ops.md).</span></span>

    -   <span data-ttu-id="93f77-125">Wenn Sie kein AGPM-Administrator sind: fordern Sie die Verbindungsdetails für den AGPM-Server von einem AGPM-Administrator an.</span><span class="sxs-lookup"><span data-stu-id="93f77-125">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="93f77-126">Informationen finden Sie unter [Konfigurieren einer AGPM-Server Verbindung](configure-an-agpm-server-connection-reviewer-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="93f77-126">See [Configure an AGPM Server Connection](configure-an-agpm-server-connection-reviewer-agpm30ops.md).</span></span>

-   <span data-ttu-id="93f77-127">**Ursache**: der AGPM-Dienst wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="93f77-127">**Cause**: The AGPM Service is not running.</span></span>

-   <span data-ttu-id="93f77-128">**Lösung**:</span><span class="sxs-lookup"><span data-stu-id="93f77-128">**Solution**:</span></span>

    -   <span data-ttu-id="93f77-129">Wenn Sie ein AGPM-Administrator sind: Starten Sie den AGPM-Dienst.</span><span class="sxs-lookup"><span data-stu-id="93f77-129">If you are an AGPM Administrator: Start the AGPM Service.</span></span> <span data-ttu-id="93f77-130">Weitere Informationen finden Sie unter [starten und Beenden des AGPM-Diensts](start-and-stop-the-agpm-service-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="93f77-130">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm30ops.md).</span></span>

    -   <span data-ttu-id="93f77-131">Wenn Sie kein AGPM-Administrator sind: wenden Sie sich an einen AGPM-Administrator, um Hilfe zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="93f77-131">If you are not an AGPM Administrator: Contact an AGPM Administrator for assistance.</span></span>

### <a href="" id="bkmk-state-varies"></a><span data-ttu-id="93f77-132">Der GPO-Status variiert für verschiedene Gruppenrichtlinienadministratoren</span><span class="sxs-lookup"><span data-stu-id="93f77-132">The GPO state varies for different Group Policy administrators</span></span>

-   <span data-ttu-id="93f77-133">**Ursache**: verschiedene Gruppenrichtlinienadministratoren haben verschiedene AGPM-Server für dasselbe Archiv ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="93f77-133">**Cause**: Different Group Policy administrators have selected different AGPM Servers for the same archive.</span></span>

-   <span data-ttu-id="93f77-134">**Lösung**:</span><span class="sxs-lookup"><span data-stu-id="93f77-134">**Solution**:</span></span>

    -   <span data-ttu-id="93f77-135">Wenn Sie ein AGPM-Administrator sind, lesen Sie [Konfigurieren von AGPM-Server Verbindungen](configure-agpm-server-connections-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="93f77-135">If you are an AGPM Administrator: See [Configure AGPM Server Connections](configure-agpm-server-connections-agpm30ops.md).</span></span>

    -   <span data-ttu-id="93f77-136">Wenn Sie kein AGPM-Administrator sind: fordern Sie die Verbindungsdetails für den AGPM-Server von einem AGPM-Administrator an.</span><span class="sxs-lookup"><span data-stu-id="93f77-136">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="93f77-137">Informationen finden Sie unter [Konfigurieren einer AGPM-Server Verbindung](configure-an-agpm-server-connection-reviewer-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="93f77-137">See [Configure an AGPM Server Connection](configure-an-agpm-server-connection-reviewer-agpm30ops.md).</span></span>

### <a href="" id="bkmk-modify-archive-location"></a><span data-ttu-id="93f77-138">Ich kann die AGPM-Server Verbindung nicht ändern</span><span class="sxs-lookup"><span data-stu-id="93f77-138">I am unable to modify the AGPM Server connection</span></span>

-   <span data-ttu-id="93f77-139">**Ursache**: Wenn die Einstellungen auf der Registerkarte **AGPM-Server** nicht verfügbar sind, wurde der AGPM-Server mithilfe einer administrativen Vorlage zentral konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="93f77-139">**Cause**: If the settings on the **AGPM Server** tab are unavailable, the AGPM Server has been centrally configured using an Administrative template.</span></span>

-   <span data-ttu-id="93f77-140">**Lösung**:</span><span class="sxs-lookup"><span data-stu-id="93f77-140">**Solution**:</span></span>

    -   <span data-ttu-id="93f77-141">Wenn Sie ein AGPM-Administrator sind: Wenn die Einstellungen auf der Registerkarte **AGPM-Server** nicht verfügbar sind, finden Sie Informationen unter Konfigurieren von [AGPM-Serververbindungen](configure-agpm-server-connections-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="93f77-141">If you are an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm30ops.md).</span></span>

    -   <span data-ttu-id="93f77-142">Wenn Sie kein AGPM-Administrator sind: Wenn die Einstellungen auf der Registerkarte **AGPM-Server** nicht verfügbar sind, müssen Sie den AGPM-Server nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="93f77-142">If you are not an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, you do not need to modify the AGPM Server.</span></span>

### <a href="" id="bkmk-perform-task"></a><span data-ttu-id="93f77-143">Ich kann die Standardvorlage oder das anzeigen, erstellen, bearbeiten, umbenennen, bereitstellen oder Löschen von GPOs nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="93f77-143">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>

-   <span data-ttu-id="93f77-144">**Ursache**: Ihnen wurde keine Rolle mit den Berechtigungen zugewiesen, die zum Ausführen der Aufgabe oder Aufgaben erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="93f77-144">**Cause**: You have not been assigned a role with the permissions required to perform the task or tasks.</span></span>

-   <span data-ttu-id="93f77-145">**Lösung**:</span><span class="sxs-lookup"><span data-stu-id="93f77-145">**Solution**:</span></span>

    -   <span data-ttu-id="93f77-146">Wenn Sie ein AGPM-Administrator sind: Lesen Sie [Delegieren des Zugriffs auf das Archiv auf Domänenebene](delegate-domain-level-access-to-the-archive-agpm30ops.md) und [Delegieren des Zugriffs auf ein einzelnes GPO im Archiv](delegate-access-to-an-individual-gpo-in-the-archive-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="93f77-146">If you are an AGPM Administrator: See [Delegate Domain-Level Access to the Archive](delegate-domain-level-access-to-the-archive-agpm30ops.md) and [Delegate Access to an Individual GPO in the Archive](delegate-access-to-an-individual-gpo-in-the-archive-agpm30ops.md).</span></span> <span data-ttu-id="93f77-147">AGPM-Berechtigungen werden von der Domäne zu allen GPOs, die sich derzeit im Archiv befinden, kaskadiert.</span><span class="sxs-lookup"><span data-stu-id="93f77-147">AGPM permissions will cascade from the domain to all GPOs currently in the archive.</span></span> <span data-ttu-id="93f77-148">Informationen dazu, welche Rollen eine Aufgabe ausführen können und welche Berechtigungen zum Ausführen einer Aufgabe erforderlich sind, finden Sie in der Hilfe zu dieser Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="93f77-148">For details about which roles can perform a task and which permissions are necessary to perform a task, refer to the help for that task.</span></span>

    -   <span data-ttu-id="93f77-149">Wenn Sie kein AGPM-Administrator sind und zusätzliche Rollen oder Berechtigungen benötigen: wenden Sie sich an einen AGPM-Administrator, um Hilfe zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="93f77-149">If you are not an AGPM Administrator and you require additional roles or permissions: Contact an AGPM Administrator for assistance.</span></span> <span data-ttu-id="93f77-150">Beachten Sie, dass Sie, wenn Sie ein Editor sind, den Vorgang zum Erstellen eines Gruppenrichtlinienobjekts, zum Bereitstellen eines Gruppenrichtlinienobjekts oder zum Löschen eines Gruppenrichtlinienobjekts aus der Produktionsumgebung beginnen können, aber eine genehmigende Person oder ein AGPM-Administrator Ihre Anforderung genehmigen muss.</span><span class="sxs-lookup"><span data-stu-id="93f77-150">Be aware that if you are an Editor, you can begin the process of creating a GPO, deploying a GPO, or deleting a GPO from the production environment, but an Approver or AGPM Administrator must approve your request.</span></span>

### <a href="" id="bkmk-use-particular-name"></a><span data-ttu-id="93f77-151">Ich kann einen bestimmten GPO-Namen nicht verwenden</span><span class="sxs-lookup"><span data-stu-id="93f77-151">I am unable to use a particular GPO name</span></span>

-   <span data-ttu-id="93f77-152">**Ursache**: entweder der GPO-Name wird bereits verwendet, oder Sie haben keine Berechtigung, das Gruppenrichtlinienobjekt aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="93f77-152">**Cause**: Either the GPO name is already in use or you lack permission to list the GPO.</span></span>

-   <span data-ttu-id="93f77-153">**Lösung**:</span><span class="sxs-lookup"><span data-stu-id="93f77-153">**Solution**:</span></span>

    -   <span data-ttu-id="93f77-154">Wenn der Name des Gruppenrichtlinienobjekts auf der Registerkarte **gesteuert**, **unkontrolliert**oder **Ausstehend** angezeigt wird, wählen Sie einen anderen Namen aus.</span><span class="sxs-lookup"><span data-stu-id="93f77-154">If the GPO name appears on the **Controlled**, **Uncontrolled**, or **Pending** tab, choose another name.</span></span> <span data-ttu-id="93f77-155">Wenn ein bereitgestelltes Gruppenrichtlinienobjekt umbenannt, aber noch nicht erneut bereitgestellt wurde, wird es unter seinem alten Namen in der Produktionsumgebung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="93f77-155">If a GPO that was deployed is renamed but not yet redeployed, it will be displayed under its old name in the production environment.</span></span> <span data-ttu-id="93f77-156">Daher wird der alte Name weiterhin verwendet.</span><span class="sxs-lookup"><span data-stu-id="93f77-156">Therefore, the old name is still being used.</span></span> <span data-ttu-id="93f77-157">Stellen Sie das Gruppenrichtlinienobjekt erneut bereit, um dessen Namen in der Produktionsumgebung zu aktualisieren und diesen Namen für die Verwendung durch ein anderes GPO freizugeben.</span><span class="sxs-lookup"><span data-stu-id="93f77-157">Redeploy the GPO to update its name in the production environment and release that name for use by another GPO.</span></span>

    -   <span data-ttu-id="93f77-158">Wenn der GPO-Name nicht auf der Registerkarte **gesteuert**, **unkontrolliert**oder **Ausstehend** angezeigt wird, ist möglicherweise keine Berechtigung zum Auflisten des Gruppenrichtlinienobjekts vorhanden.</span><span class="sxs-lookup"><span data-stu-id="93f77-158">If the GPO name does not appear on the **Controlled**, **Uncontrolled**, or **Pending** tab, you may lack permission to list the GPO.</span></span> <span data-ttu-id="93f77-159">Wenden Sie sich an einen AGPM-Administrator, um die Berechtigung anzufordern.</span><span class="sxs-lookup"><span data-stu-id="93f77-159">To request permission, contact an AGPM Administrator.</span></span>

### <a href="" id="bkmk-email"></a><span data-ttu-id="93f77-160">Ich erhalte keine AGPM-e-Mail-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="93f77-160">I am not receiving AGPM e-mail notifications</span></span>

-   <span data-ttu-id="93f77-161">**Ursache**: Es wurde kein gültiger SMTP-e-Mail-Server und keine e-Mail-Adresse bereitgestellt, oder es wurde keine Aktion durchgeführt, die eine e-Mail-Benachrichtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="93f77-161">**Cause**: A valid SMTP e-mail server and e-mail address has not been provided, or no action has been taken that generates an e-mail notification.</span></span>

-   <span data-ttu-id="93f77-162">**Lösung**:</span><span class="sxs-lookup"><span data-stu-id="93f77-162">**Solution**:</span></span>

    -   <span data-ttu-id="93f77-163">Wenn Sie ein AGPM-Administrator sind: Wenn e-Mail-Benachrichtigungen über ausstehende Aktionen von AGPM gesendet werden sollen, muss ein AGPM-Administrator auf der Registerkarte **Domänendelegierung** einen gültigen SMTP-e-Mail-Server und e-Mail-Adressen für genehmigende Personen bereitstellen. Weitere Informationen finden Sie unter [Konfigurieren von e-Mail-Benachrichtigungen](configure-e-mail-notification-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="93f77-163">If you are an AGPM Administrator: For e-mail notifications about pending actions to be sent by AGPM, an AGPM Administrator must provide a valid SMTP e-mail server and e-mail addresses for Approvers on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification-agpm30ops.md).</span></span>

    -   <span data-ttu-id="93f77-164">E-Mail-Benachrichtigungen werden nur generiert, wenn ein Bearbeiter, Prüfer oder ein anderer Gruppenrichtlinienadministrator, der über die zum Erstellen, bereitstellen oder Löschen eines Gruppenrichtlinienobjekts erforderliche Berechtigung verfügt, eine Anforderung für eine dieser Aktionen übermittelt.</span><span class="sxs-lookup"><span data-stu-id="93f77-164">E-mail notifications are generated only when an Editor, Reviewer, or other Group Policy administrator who lacks the permission necessary to create, deploy, or delete a GPO submits a request for one of those actions to occur.</span></span> <span data-ttu-id="93f77-165">Es erfolgt keine automatische Benachrichtigung über die Genehmigung oder Ablehnung einer Anfrage.</span><span class="sxs-lookup"><span data-stu-id="93f77-165">There is no automatic notification of approval or rejection of a request.</span></span>

### <a href="" id="bkmk-port"></a><span data-ttu-id="93f77-166">Ich kann Port 4600 für den AGPM-Dienst nicht verwenden</span><span class="sxs-lookup"><span data-stu-id="93f77-166">I cannot use port 4600 for the AGPM Service</span></span>

-   <span data-ttu-id="93f77-167">**Ursache**: Standardmäßig ist der Port, auf dem der AGPM-Dienst lauscht, Port 4600.</span><span class="sxs-lookup"><span data-stu-id="93f77-167">**Cause**: By default, the port on which the AGPM Service listens is port 4600.</span></span>

-   <span data-ttu-id="93f77-168">**Lösung**: Wenn Port 4600 für den AGPM-Dienst nicht verfügbar ist, ändern Sie die Portkonfiguration auf dem AGPM-Server, um einen anderen Port zu verwenden, und aktualisieren Sie dann den Port in der AGPM-Serververbindung für AGPM-Clients.</span><span class="sxs-lookup"><span data-stu-id="93f77-168">**Solution**: If port 4600 is not available for the AGPM Service, modify the port configuration on the AGPM Server to use another port and then update the port in the AGPM Server connection for AGPM Clients.</span></span> <span data-ttu-id="93f77-169">Weitere Informationen finden Sie unter [Ändern des AGPM-Diensts](modify-the-agpm-service-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="93f77-169">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm30ops.md).</span></span>

### <a href="" id="bkmk-not-start"></a><span data-ttu-id="93f77-170">Der AGPM-Dienst wird nicht gestartet</span><span class="sxs-lookup"><span data-stu-id="93f77-170">The AGPM Service will not start</span></span>

-   <span data-ttu-id="93f77-171">**Ursache**: Sie haben die Einstellungen für den AGPM-Dienst im Betriebssystemunter **Administrative Tools** und **Dienste**geändert.</span><span class="sxs-lookup"><span data-stu-id="93f77-171">**Cause**: You have modified settings for the AGPM Service in the operating system under **Administrative Tools** and **Services**.</span></span>

-   <span data-ttu-id="93f77-172">**Lösung**: Ändern Sie die Einstellungen für **Microsoft Advanced Group Policy Management-Server** unter **Programme und Funktionen** in der Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="93f77-172">**Solution**: Modify the settings for **Microsoft Advanced Group Policy Management - Server** under **Programs and Features** in Control Panel.</span></span> <span data-ttu-id="93f77-173">Weitere Informationen finden Sie unter [Ändern des AGPM-Diensts](modify-the-agpm-service-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="93f77-173">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm30ops.md).</span></span>

### <a href="" id="bkmk-software-installation"></a><span data-ttu-id="93f77-174">Software Installation für Gruppenrichtlinien kann nicht installiert werden</span><span class="sxs-lookup"><span data-stu-id="93f77-174">Group Policy Software Installation fails to install software</span></span>

-   <span data-ttu-id="93f77-175">**Ursache**: AGPM erhält die Integrität von Gruppenrichtlinien-Software Installationspaketen.</span><span class="sxs-lookup"><span data-stu-id="93f77-175">**Cause**: AGPM preserves the integrity of Group Policy Software Installation packages.</span></span> <span data-ttu-id="93f77-176">Obwohl GPOs offline bearbeitet werden, bleiben Verknüpfungen zwischen Paketen sowie zwischengespeicherte Clientinformationen erhalten.</span><span class="sxs-lookup"><span data-stu-id="93f77-176">Although GPOs are edited offline, links between packages in addition to cached client information are preserved.</span></span> <span data-ttu-id="93f77-177">Dies ist entwurfsbedingt.</span><span class="sxs-lookup"><span data-stu-id="93f77-177">This is by design.</span></span>

-   <span data-ttu-id="93f77-178">**Lösung**: Wenn Sie ein GPO offline mit AGPM bearbeiten, konfigurieren Sie alle Gruppenrichtlinien-Software Installations Upgrades eines Pakets in einem anderen Gruppenrichtlinienobjekt, um auf das bereitgestellte Gruppenrichtlinienobjekt zu verweisen, nicht auf die ausgecheckte Kopie.</span><span class="sxs-lookup"><span data-stu-id="93f77-178">**Solution**: When you edit a GPO offline with AGPM, configure any Group Policy Software Installation upgrade of a package in another GPO to reference the deployed GPO, not the checked-out copy.</span></span> <span data-ttu-id="93f77-179">Der Editor muss über die Berechtigung " **Lesen** " für das bereitgestellte Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="93f77-179">The Editor must have **Read** permission for the deployed GPO.</span></span>

### <a href="" id="bkmk-error-on-restore"></a><span data-ttu-id="93f77-180">Beim Wiederherstellen des Archivs auf einem neuen AGPM-Server ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="93f77-180">An error occurred when I restored the archive to a new AGPM Server</span></span>

-   <span data-ttu-id="93f77-181">**Ursache**: aus Sicherheitsgründen führt die Verschlüsselung, die das auf der Registerkarte **Domänendelegierung** eingegebene Kennwort schützt, dazu, dass das Kennwort fehlschlägt, wenn das Archiv auf einen anderen Computer verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="93f77-181">**Cause**: For security reasons, the encryption protecting the password entered on the **Domain Delegation** tab causes the password to fail if the archive is moved to another computer.</span></span>

-   <span data-ttu-id="93f77-182">**Lösung**: Geben Sie das Kennwort auf der Registerkarte **Domänendelegierung** erneut ein, und bestätigen Sie es. Weitere Informationen finden Sie unter [Konfigurieren von e-Mail-Benachrichtigungen](configure-e-mail-notification-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="93f77-182">**Solution**: Re-enter and confirm the password on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification-agpm30ops.md).</span></span>

 

 





