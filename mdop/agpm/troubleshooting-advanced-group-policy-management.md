---
title: Problembehandlung bei Advanced Group Policy Management
description: Problembehandlung bei Advanced Group Policy Management
author: dansimp
ms.assetid: f58849cf-6c5b-44d8-b356-0ed7a5b24cee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c22b9a0983b26252ee0d9c8d99b63cd4ab5dc2b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807432"
---
# <span data-ttu-id="9f6d8-103">Problembehandlung bei Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="9f6d8-103">Troubleshooting Advanced Group Policy Management</span></span>


<span data-ttu-id="9f6d8-104">In diesem Abschnitt werden einige häufige Probleme aufgeführt, die bei der Verwendung der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) zum Verwalten von Gruppenrichtlinienobjekten auftreten können.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-104">This section lists a few common issues you may encounter when using Advanced Group Policy Management (AGPM) to manage Group Policy objects (GPOs).</span></span>

## <span data-ttu-id="9f6d8-105">Welche Probleme haben Sie?</span><span class="sxs-lookup"><span data-stu-id="9f6d8-105">What problems are you having?</span></span>


-   [<span data-ttu-id="9f6d8-106">Ich kann nicht auf ein Archiv zugreifen</span><span class="sxs-lookup"><span data-stu-id="9f6d8-106">I am unable to access an archive</span></span>](#bkmk-access-an-archive)

-   [<span data-ttu-id="9f6d8-107">Der GPO-Status variiert für verschiedene Gruppenrichtlinienadministratoren</span><span class="sxs-lookup"><span data-stu-id="9f6d8-107">The GPO state varies for different Group Policy administrators</span></span>](#bkmk-state-varies)

-   [<span data-ttu-id="9f6d8-108">Ich kann die AGPM-Server Verbindung nicht ändern</span><span class="sxs-lookup"><span data-stu-id="9f6d8-108">I am unable to modify the AGPM Server connection</span></span>](#bkmk-modify-archive-location)

-   [<span data-ttu-id="9f6d8-109">Ich kann die Standardvorlage oder das anzeigen, erstellen, bearbeiten, umbenennen, bereitstellen oder Löschen von GPOs nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-109">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>](#bkmk-perform-task)

-   [<span data-ttu-id="9f6d8-110">Ich kann einen bestimmten GPO-Namen nicht verwenden</span><span class="sxs-lookup"><span data-stu-id="9f6d8-110">I am unable to use a particular GPO name</span></span>](#bkmk-use-particular-name)

-   [<span data-ttu-id="9f6d8-111">Ich erhalte keine AGPM-e-Mail-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="9f6d8-111">I am not receiving AGPM e-mail notifications</span></span>](#bkmk-email)

-   [<span data-ttu-id="9f6d8-112">Ich kann Port 4600 für den AGPM-Dienst nicht verwenden</span><span class="sxs-lookup"><span data-stu-id="9f6d8-112">I cannot use port 4600 for the AGPM Service</span></span>](#bkmk-port)

-   [<span data-ttu-id="9f6d8-113">Der AGPM-Dienst wird nicht gestartet</span><span class="sxs-lookup"><span data-stu-id="9f6d8-113">The AGPM Service will not start</span></span>](#bkmk-not-start)

-   [<span data-ttu-id="9f6d8-114">Software Installation für Gruppenrichtlinien kann nicht installiert werden</span><span class="sxs-lookup"><span data-stu-id="9f6d8-114">Group Policy Software Installation fails to install software</span></span>](#bkmk-software-installation)

### <a href="" id="bkmk-access-an-archive"></a><span data-ttu-id="9f6d8-115">Ich kann nicht auf ein Archiv zugreifen</span><span class="sxs-lookup"><span data-stu-id="9f6d8-115">I am unable to access an archive</span></span>

-   <span data-ttu-id="9f6d8-116">**Ursache**: Sie haben nicht den richtigen Server und Port für das Archiv ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-116">**Cause**: You have not selected the correct server and port for the archive.</span></span>

-   <span data-ttu-id="9f6d8-117">**Lösung**:</span><span class="sxs-lookup"><span data-stu-id="9f6d8-117">**Solution**:</span></span>

    -   <span data-ttu-id="9f6d8-118">Wenn Sie ein AGPM-Administrator sind, lesen Sie [Konfigurieren der AGPM-Server Verbindung](configure-the-agpm-server-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9f6d8-118">If you are an AGPM Administrator: See [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).</span></span>

    -   <span data-ttu-id="9f6d8-119">Wenn Sie kein AGPM-Administrator sind: fordern Sie die Verbindungsdetails für den AGPM-Server von einem AGPM-Administrator an.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-119">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="9f6d8-120">Informationen finden Sie unter [Konfigurieren der AGPM-Server Verbindung](configure-the-agpm-server-connection-reviewer.md).</span><span class="sxs-lookup"><span data-stu-id="9f6d8-120">See [Configure the AGPM Server Connection](configure-the-agpm-server-connection-reviewer.md).</span></span>

-   <span data-ttu-id="9f6d8-121">**Ursache**: der erweiterte Gruppenrichtlinien-Verwaltungsdienst wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-121">**Cause**: The Advanced Group Policy Management Service is not running.</span></span>

-   <span data-ttu-id="9f6d8-122">**Lösung**:</span><span class="sxs-lookup"><span data-stu-id="9f6d8-122">**Solution**:</span></span>

    -   <span data-ttu-id="9f6d8-123">Wenn Sie ein AGPM-Administrator sind: Starten Sie den AGPM-Dienst.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-123">If you are an AGPM Administrator: Start the AGPM Service.</span></span> <span data-ttu-id="9f6d8-124">Weitere Informationen finden Sie unter [starten und Beenden des AGPM-Diensts](start-and-stop-the-agpm-service.md).</span><span class="sxs-lookup"><span data-stu-id="9f6d8-124">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service.md).</span></span>

    -   <span data-ttu-id="9f6d8-125">Wenn Sie kein AGPM-Administrator sind: wenden Sie sich an einen AGPM-Administrator, um Hilfe zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-125">If you are not an AGPM Administrator: Contact an AGPM Administrator for assistance.</span></span>

### <a href="" id="bkmk-state-varies"></a><span data-ttu-id="9f6d8-126">Der GPO-Status variiert für verschiedene Gruppenrichtlinienadministratoren</span><span class="sxs-lookup"><span data-stu-id="9f6d8-126">The GPO state varies for different Group Policy administrators</span></span>

-   <span data-ttu-id="9f6d8-127">**Ursache**: verschiedene Gruppenrichtlinienadministratoren haben verschiedene AGPM-Server für dasselbe Archiv ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-127">**Cause**: Different Group Policy administrators have selected different AGPM Servers for the same archive.</span></span>

-   <span data-ttu-id="9f6d8-128">**Lösung**:</span><span class="sxs-lookup"><span data-stu-id="9f6d8-128">**Solution**:</span></span>

    -   <span data-ttu-id="9f6d8-129">Wenn Sie ein AGPM-Administrator sind, lesen Sie [Konfigurieren der AGPM-Server Verbindung](configure-the-agpm-server-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9f6d8-129">If you are an AGPM Administrator: See [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).</span></span>

    -   <span data-ttu-id="9f6d8-130">Wenn Sie kein AGPM-Administrator sind: fordern Sie die Verbindungsdetails für den AGPM-Server von einem AGPM-Administrator an.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-130">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="9f6d8-131">Informationen finden Sie unter [Konfigurieren der AGPM-Server Verbindung](configure-the-agpm-server-connection-reviewer.md).</span><span class="sxs-lookup"><span data-stu-id="9f6d8-131">See [Configure the AGPM Server Connection](configure-the-agpm-server-connection-reviewer.md).</span></span>

### <a href="" id="bkmk-modify-archive-location"></a><span data-ttu-id="9f6d8-132">Ich kann die AGPM-Server Verbindung nicht ändern</span><span class="sxs-lookup"><span data-stu-id="9f6d8-132">I am unable to modify the AGPM Server connection</span></span>

-   <span data-ttu-id="9f6d8-133">**Ursache**: Wenn die Einstellungen auf der Registerkarte **AGPM-Server** nicht verfügbar sind, wurde der AGPM-Server mithilfe einer administrativen Vorlage zentral konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-133">**Cause**: If the settings on the **AGPM Server** tab are unavailable, the AGPM Server has been centrally configured using an Administrative template.</span></span>

-   <span data-ttu-id="9f6d8-134">**Lösung**:</span><span class="sxs-lookup"><span data-stu-id="9f6d8-134">**Solution**:</span></span>

    -   <span data-ttu-id="9f6d8-135">Wenn Sie ein AGPM-Administrator sind: Wenn die Einstellungen auf der Registerkarte **AGPM-Server** nicht verfügbar sind, lesen Sie [Konfigurieren der AGPM-Serververbindung](configure-the-agpm-server-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9f6d8-135">If you are an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, see [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).</span></span>

    -   <span data-ttu-id="9f6d8-136">Wenn Sie kein AGPM-Administrator sind: Wenn die Einstellungen auf der Registerkarte **AGPM-Server** nicht verfügbar sind, müssen Sie den AGPM-Server nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-136">If you are not an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, you do not need to modify the AGPM Server.</span></span>

### <a href="" id="bkmk-perform-task"></a><span data-ttu-id="9f6d8-137">Ich kann die Standardvorlage oder das anzeigen, erstellen, bearbeiten, umbenennen, bereitstellen oder Löschen von GPOs nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-137">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>

-   <span data-ttu-id="9f6d8-138">**Ursache**: Ihnen wurde keine Rolle mit den Berechtigungen zugewiesen, die zum Ausführen der Aufgabe oder Aufgaben erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-138">**Cause**: You have not been assigned a role with the permissions required to perform the task or tasks.</span></span>

-   <span data-ttu-id="9f6d8-139">**Lösung**:</span><span class="sxs-lookup"><span data-stu-id="9f6d8-139">**Solution**:</span></span>

    -   <span data-ttu-id="9f6d8-140">Wenn Sie ein AGPM-Administrator sind, lesen Sie Delegieren des Zugriffs auf [Domänenebene](delegate-domain-level-access.md) und [Delegieren des Zugriffs auf ein einzelnes Gruppenrichtlinienobjekt](delegate-access-to-an-individual-gpo.md).</span><span class="sxs-lookup"><span data-stu-id="9f6d8-140">If you are an AGPM Administrator: See [Delegate Domain-Level Access](delegate-domain-level-access.md) and [Delegate Access to an Individual GPO](delegate-access-to-an-individual-gpo.md).</span></span> <span data-ttu-id="9f6d8-141">AGPM-Berechtigungen werden von der Domäne zu allen GPOs, die sich derzeit im Archiv befinden, kaskadiert.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-141">AGPM permissions will cascade from the domain to all GPOs currently in the archive.</span></span> <span data-ttu-id="9f6d8-142">Wenn neue Gruppenrichtlinienadministratoren auf Domänenebene hinzugefügt werden, müssen Ihre Berechtigungen so festgesetzt sein, dass Sie auf **dieses Objekt und verschachtelte Objekte**angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-142">As new Group Policy administrators are added at the domain level, their permissions must be set to apply to **This object and nested objects**.</span></span> <span data-ttu-id="9f6d8-143">Informationen dazu, welche Rollen eine Aufgabe ausführen können und welche Berechtigungen für die Ausführung einer Aufgabe erforderlich sind, finden Sie in der Hilfe zu dieser Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-143">For details about which roles can perform a task and what permissions are necessary to perform a task, refer to the help for that task.</span></span>

    -   <span data-ttu-id="9f6d8-144">Wenn Sie kein AGPM-Administrator sind und zusätzliche Rollen oder Berechtigungen benötigen: wenden Sie sich an einen AGPM-Administrator, um Hilfe zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-144">If you are not an AGPM Administrator and you require additional roles or permissions: Contact an AGPM Administrator for assistance.</span></span> <span data-ttu-id="9f6d8-145">Beachten Sie, dass Sie, wenn Sie ein Editor sind, den Vorgang des Erstellens eines GPO, der Bereitstellungeines Gruppenrichtlinienobjekts oder des Löschens eines Gruppenrichtlinienobjekts aus der Produktionsumgebung beginnen können, aber eine genehmigende Person oder ein AGPM-Administrator Ihre Anforderung genehmigen muss.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-145">Note that if you are an Editor, you can begin the process of creating a GPO, deploying a GPO, or deleting a GPO from the production environment, but an Approver or AGPM Administrator must approve your request.</span></span>

### <a href="" id="bkmk-use-particular-name"></a><span data-ttu-id="9f6d8-146">Ich kann einen bestimmten GPO-Namen nicht verwenden</span><span class="sxs-lookup"><span data-stu-id="9f6d8-146">I am unable to use a particular GPO name</span></span>

-   <span data-ttu-id="9f6d8-147">**Ursache**: entweder der GPO-Name wird bereits verwendet, oder Sie haben keine Berechtigung, das Gruppenrichtlinienobjekt aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-147">**Cause**: Either the GPO name is already in use or you lack permission to list the GPO.</span></span>

-   <span data-ttu-id="9f6d8-148">**Lösung**:</span><span class="sxs-lookup"><span data-stu-id="9f6d8-148">**Solution**:</span></span>

    -   <span data-ttu-id="9f6d8-149">Wenn der Name des Gruppenrichtlinienobjekts auf der Registerkarte **gesteuert**, **unkontrolliert**oder **Ausstehend** angezeigt wird, wählen Sie einen anderen Namen aus.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-149">If the GPO name appears on the **Controlled**, **Uncontrolled**, or **Pending** tab, choose another name.</span></span> <span data-ttu-id="9f6d8-150">Wenn ein bereitgestelltes GPO umbenannt, aber noch nicht erneut bereitgestellt wurde, wird es unter seinem alten Namen in der Produktionsumgebung angezeigt, daher wird der alte Name noch verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-150">If a GPO that has been deployed is renamed but not yet redeployed, it will be displayed under its old name in the production environment—therefore, the old name is still in use.</span></span> <span data-ttu-id="9f6d8-151">Stellen Sie das Gruppenrichtlinienobjekt erneut bereit, um dessen Namen in der Produktionsumgebung zu aktualisieren und diesen Namen für die Verwendung durch ein anderes GPO freizugeben.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-151">Redeploy the GPO to update its name in the production environment and release that name for use by another GPO.</span></span>

    -   <span data-ttu-id="9f6d8-152">Wenn der GPO-Name nicht auf der Registerkarte **gesteuert**, **unkontrolliert**oder **Ausstehend** angezeigt wird, ist möglicherweise keine Berechtigung zum Auflisten des Gruppenrichtlinienobjekts vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-152">If the GPO name does not appear on the **Controlled**, **Uncontrolled**, or **Pending** tab, you may lack permission to list the GPO.</span></span> <span data-ttu-id="9f6d8-153">Wenden Sie sich an einen AGPM-Administrator, um die Berechtigung anzufordern.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-153">To request permission, contact an AGPM Administrator.</span></span>

### <a href="" id="bkmk-email"></a><span data-ttu-id="9f6d8-154">Ich erhalte keine AGPM-e-Mail-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="9f6d8-154">I am not receiving AGPM e-mail notifications</span></span>

-   <span data-ttu-id="9f6d8-155">**Ursache**: Es wurde kein gültiger SMTP-e-Mail-Server und keine e-Mail-Adresse bereitgestellt, oder es wurde keine Aktion durchgeführt, die eine e-Mail-Benachrichtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-155">**Cause**: A valid SMTP e-mail server and e-mail address has not been provided, or no action has been taken that generates an e-mail notification.</span></span>

-   <span data-ttu-id="9f6d8-156">**Lösung**:</span><span class="sxs-lookup"><span data-stu-id="9f6d8-156">**Solution**:</span></span>

    -   <span data-ttu-id="9f6d8-157">Wenn Sie ein AGPM-Administrator sind: Wenn e-Mail-Benachrichtigungen über ausstehende Aktionen von AGPM gesendet werden sollen, muss ein AGPM-Administrator auf der Registerkarte **Domänendelegierung** einen gültigen SMTP-e-Mail-Server und e-Mail-Adressen für genehmigende Personen bereitstellen. Weitere Informationen finden Sie unter [Konfigurieren von e-Mail-Benachrichtigungen](configure-e-mail-notification.md).</span><span class="sxs-lookup"><span data-stu-id="9f6d8-157">If you are an AGPM Administrator: For e-mail notifications about pending actions to be sent by AGPM, an AGPM Administrator must provide a valid SMTP e-mail server and e-mail addresses for Approvers on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification.md).</span></span>

    -   <span data-ttu-id="9f6d8-158">E-Mail-Benachrichtigungen werden nur generiert, wenn ein Bearbeiter, Prüfer oder ein anderer Gruppenrichtlinienadministrator, der über die zum Erstellen, bereitstellen oder Löschen eines Gruppenrichtlinienobjekts erforderliche Berechtigung verfügt, eine Anforderung für eine dieser Aktionen übermittelt.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-158">E-mail notifications are generated only when an Editor, Reviewer, or other Group Policy administrator who lacks the permission necessary to create, deploy, or delete a GPO submits a request for one of those actions to occur.</span></span> <span data-ttu-id="9f6d8-159">Es erfolgt keine automatische Benachrichtigung über die Genehmigung oder Ablehnung einer Anfrage.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-159">There is no automatic notification of approval or rejection of a request.</span></span>

### <a href="" id="bkmk-port"></a><span data-ttu-id="9f6d8-160">Ich kann Port 4600 für den AGPM-Dienst nicht verwenden</span><span class="sxs-lookup"><span data-stu-id="9f6d8-160">I cannot use port 4600 for the AGPM Service</span></span>

-   <span data-ttu-id="9f6d8-161">**Ursache**: Standardmäßig ist der Port, auf dem der AGPM-Dienst lauscht, Port 4600.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-161">**Cause**: By default, the port on which the AGPM Service listens is port 4600.</span></span>

-   <span data-ttu-id="9f6d8-162">**Lösung**: Wenn Port 4600 für den AGPM-Dienst nicht verfügbar ist, ändern Sie die einzelnen Archiv Indexdateien so, dass Sie einen anderen Port verwenden, und aktualisieren Sie dann den AGPM-Server für alle Gruppenrichtlinienadministratoren.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-162">**Solution**: If port 4600 is not available for the AGPM Service, modify each archive index file to use another port and then update the AGPM Server for all Group Policy administrators.</span></span> <span data-ttu-id="9f6d8-163">Weitere Informationen finden Sie unter [Ändern des Ports, auf den der AGPM-Dienst lauscht](modify-the-port-on-which-the-agpm-service-listens.md).</span><span class="sxs-lookup"><span data-stu-id="9f6d8-163">For more information, see [Modify the Port on Which the AGPM Service Listens](modify-the-port-on-which-the-agpm-service-listens.md).</span></span>

### <a href="" id="bkmk-not-start"></a><span data-ttu-id="9f6d8-164">Der AGPM-Dienst wird nicht gestartet</span><span class="sxs-lookup"><span data-stu-id="9f6d8-164">The AGPM Service will not start</span></span>

-   <span data-ttu-id="9f6d8-165">**Ursache**: Sie haben die Einstellungen für den AGPM-Dienst im Betriebssystemunter **Administrative Tools** und **Dienste**geändert.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-165">**Cause**: You have modified settings for the AGPM Service in the operating system under **Administrative Tools** and **Services**.</span></span>

-   <span data-ttu-id="9f6d8-166">**Lösung**: Ändern Sie die Einstellungen für **Microsoft Advanced Group Policy Management-Server** unter **Software**.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-166">**Solution**: Modify the settings for **Microsoft Advanced Group Policy Management - Server** under **Add or Remove Programs**.</span></span> <span data-ttu-id="9f6d8-167">Weitere Informationen finden Sie unter [Ändern des AGPM-Dienstkontos](modify-the-agpm-service-account.md).</span><span class="sxs-lookup"><span data-stu-id="9f6d8-167">For more information, see [Modify the AGPM Service Account](modify-the-agpm-service-account.md).</span></span>

### <a href="" id="bkmk-software-installation"></a><span data-ttu-id="9f6d8-168">Software Installation für Gruppenrichtlinien kann nicht installiert werden</span><span class="sxs-lookup"><span data-stu-id="9f6d8-168">Group Policy Software Installation fails to install software</span></span>

-   <span data-ttu-id="9f6d8-169">**Ursache**: AGPM erhält die Integrität von Gruppenrichtlinien-Software Installationspaketen.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-169">**Cause**: AGPM preserves the integrity of Group Policy Software Installation packages.</span></span> <span data-ttu-id="9f6d8-170">Obwohl GPOs offline bearbeitet werden, bleiben Verknüpfungen zwischen Paketen und zwischengespeicherten Clientinformationen erhalten.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-170">Although GPOs are edited offline, links between packages as well as cached client information are preserved.</span></span> <span data-ttu-id="9f6d8-171">Dies ist entwurfsbedingt.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-171">This is by design.</span></span>

-   <span data-ttu-id="9f6d8-172">**Lösung**: Wenn Sie ein Gruppenrichtlinienobjekt offline mit AGPM bearbeiten, konfigurieren Sie ein Upgrade für die Gruppenrichtlinien-Software Installation eines Pakets in einem anderen Gruppenrichtlinienobjekt, um auf das bereitgestellte GPO zu verweisen, nicht auf die ausgecheckte Kopie.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-172">**Solution**: When editing a GPO offline with AGPM, configure any Group Policy Software Installation upgrade of a package in another GPO to reference the deployed GPO, not the checked-out copy.</span></span> <span data-ttu-id="9f6d8-173">Der Editor muss über die Berechtigung " **Lesen** " für das bereitgestellte Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="9f6d8-173">The Editor must have **Read** permission for the deployed GPO.</span></span>

 

 





