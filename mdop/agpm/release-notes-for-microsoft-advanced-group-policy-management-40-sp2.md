---
title: Versionshinweise für Microsoft Advanced Group Policy Management 4.0 SP2
description: Versionshinweise für Microsoft Advanced Group Policy Management 4.0 SP2
author: dansimp
ms.assetid: 0593cd11-3308-4942-bf19-8a7bb9447f01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 736eb8d41cbb72b274a2941c60b0357bbc948c9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808287"
---
# <span data-ttu-id="e4fc3-103">Versionshinweise für Microsoft Advanced Group Policy Management 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="e4fc3-103">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP2</span></span>


<span data-ttu-id="e4fc3-104">Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="e4fc3-105">Lesen Sie diese Versionshinweise gründlich, bevor Sie Microsoft Advanced Group Policy Management (AGPM) 4.0 Service Pack2 (SP2) installieren.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-105">Read these release notes thoroughly before you install Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack2 (SP2).</span></span> <span data-ttu-id="e4fc3-106">Diese Anmerkungen zu dieser Version enthalten Informationen, die erforderlich sind, um AGPM 4.0 SP2 erfolgreich zu installieren und Informationen zu enthalten, die in der Produktdokumentation nicht zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-106">These release notes contain information that is required to successfully install AGPM4.0 SP2 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="e4fc3-107">Wenn es einen Unterschied zwischen diesen Versionshinweisen und anderen AGPM-Dokumentationen gibt, sollten Sie die neueste autorisierende Änderung in Frage stellen.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-107">If there is a difference between these release notes and other AGPM documentation, consider the latest change authoritative.</span></span> <span data-ttu-id="e4fc3-108">Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-108">These release notes supersede the content included with this product.</span></span>

## <span data-ttu-id="e4fc3-109">Bekannte Probleme mit AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="e4fc3-109">AGPM4.0 SP2 known issues</span></span>


<span data-ttu-id="e4fc3-110">In diesem Abschnitt werden die bekannten Probleme für AGPM 4,0 SP2 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-110">This section describes the known issues for AGPM 4.0 SP2.</span></span>

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a><span data-ttu-id="e4fc3-111">Das Tool "deinstallieren" der Systemsteuerung funktioniert möglicherweise nicht, wenn Sie versuchen, AGPM-Server Einstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-111">Control Panel’s “Uninstall” tool may not work when you try to change AGPM Server settings</span></span>

<span data-ttu-id="e4fc3-112">Das Tool in der Systemsteuerung, mit dem Sie ein Programm deinstallieren oder ändern, funktioniert möglicherweise nicht, wenn Sie versuchen, AGPM-Server Einstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-112">The tool in Control Panel that you use to uninstall or change a program may not work when you try to change AGPM Server settings.</span></span>

<span data-ttu-id="e4fc3-113">**Problemumgehung:** Bevor Sie versuchen, AGPM-Server Einstellungen mithilfe der Systemsteuerung zu ändern, erstellen Sie eine Kopie des AGPM-Archivordners.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-113">**Workaround:** Before you try to change AGPM Server settings by using Control Panel, make a copy of the AGPM Archive folder.</span></span> <span data-ttu-id="e4fc3-114">Anschließend können Sie Setup.exe verwenden, um den AGPM-Server erneut zu installieren und die gewünschten Konfigurationsparameter auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-114">You can then use Setup.exe to reinstall the AGPM Server and choose the configuration parameters that you want.</span></span>

### <span data-ttu-id="e4fc3-115">In Berichten werden die Links, die einem Gruppenrichtlinienobjekt hinzugefügt wurden, nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-115">Reports do not display the links that were added to a Group Policy Object</span></span>

<span data-ttu-id="e4fc3-116">Die AGPM-Einstellungen und-Differenz Berichte zeigen nicht die Links an, die einem Gruppenrichtlinienobjekt (Group Policy Object, GPO) hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-116">The AGPM settings and difference reports do not display the links that were added to a Group Policy Object (GPO).</span></span>

<span data-ttu-id="e4fc3-117">**Problemumgehung:** Wenn Sie die Links in den Berichten anzeigen möchten, wählen Sie das Gruppenrichtlinienobjekt in der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) aus, und klicken Sie dann im rechten Bereich auf die Registerkarte **Einstellungen** .</span><span class="sxs-lookup"><span data-stu-id="e4fc3-117">**Workaround:** To view the links in the reports, select the GPO in the Group Policy Management Console (GPMC), and then click the **Settings** tab in the right pane.</span></span>

### <span data-ttu-id="e4fc3-118">In Berichten werden nicht alle Eigenschafteneinstellungen für Auswahloptionen angezeigt</span><span class="sxs-lookup"><span data-stu-id="e4fc3-118">Reports do not display all Choice Options Properties settings</span></span>

<span data-ttu-id="e4fc3-119">Die AGPM-Einstellungen und-Differenz Berichte zeigen nicht alle Einstellungen an, die im Eigenschaftenfenster der **Auswahloptionen** im Gruppenrichtlinienobjekt-Editor ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-119">The AGPM settings and difference reports do not display all of the settings that were selected in the **Choice Options Properties** window in the Group Policy Object Editor.</span></span>

<span data-ttu-id="e4fc3-120">**Problemumgehung:** Verwenden Sie die GPMC, um die ausgewählten Eigenschafteneinstellungen für **Auswahloptionen** in den Berichten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-120">**Workaround:** Use the GPMC to view the selected **Choice Options Properties** settings in the reports.</span></span>

### <span data-ttu-id="e4fc3-121">In bestimmten Browsern werden die Registerkarten "einblenden" und "ausblenden" möglicherweise nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="e4fc3-121">Reports may not display the Show and Hide tabs in certain browsers</span></span>

<span data-ttu-id="e4fc3-122">Die Registerkarten " **Einblenden** " und " **Ausblenden** " auf der rechten Seite der AGPM-Einstellungen und-Differenz Berichte werden möglicherweise nicht angezeigt, wenn Sie die Berichte in Google Chrome oder Mozilla Firefox anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-122">The **Show** and **Hide** tabs, on the right side of the AGPM settings and difference reports, may not appear when you view the reports in Google Chrome or Mozilla Firefox.</span></span>

<span data-ttu-id="e4fc3-123">**Problemumgehung:** Zeigen Sie die Berichte mithilfe des Internet Explorer-Browsers an.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-123">**Workaround:** View the reports by using the Internet Explorer browser.</span></span>

### <span data-ttu-id="e4fc3-124">AGPM-Einstellungen und Unterschiedsberichte können unterschiedliche Inhalte aus GPMC-Berichten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-124">AGPM settings and difference reports may show different content from GPMC reports</span></span>

<span data-ttu-id="e4fc3-125">Die AGPM-Einstellungen und-Differenz Berichte zeigen möglicherweise nicht denselben Inhalt wie Berichte in der GPMC an.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-125">The AGPM settings and difference reports may not show the same content as reports in the GPMC.</span></span>

<span data-ttu-id="e4fc3-126">**Problemumgehung:** Verwenden Sie die GPMC, um die AGPM-Berichte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-126">**Workaround:** Use the GPMC to view the AGPM reports.</span></span>

### <span data-ttu-id="e4fc3-127">AGPM-Dienst wird nicht gestartet, wenn der Domänencontroller offline ist</span><span class="sxs-lookup"><span data-stu-id="e4fc3-127">AGPM Service does not start if the domain controller is offline</span></span>

<span data-ttu-id="e4fc3-128">Wenn der AGPM-Dienst auf einem Domänencontroller auf den Betriebssystemen Windows® 8 oder höher installiert ist, wird der Dienst nicht gestartet, wenn der Domänencontroller offline ist.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-128">When the AGPM Service is installed on a domain controller on the Windows® 8 operating systems or later operating systems, the service does not start if the domain controller is offline.</span></span>

<span data-ttu-id="e4fc3-129">**Problemumgehung:** Starten Sie den AGPM-Dienst manuell, nachdem der Domänencontroller online ist.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-129">**Workaround:** Manually start the AGPM Service after the domain controller is online.</span></span>

### <span data-ttu-id="e4fc3-130">Das Upgrade des AGPM-Servers auf AGPM 4.0 SP2 wird blockiert, wenn Sie ein Upgrade von der AGPM 4.0-Version plus HotFix1 durchführen.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-130">Upgrade of AGPM Server to AGPM4.0 SP2 is blocked when you upgrade from the AGPM4.0 release plus hotfix1</span></span>

<span data-ttu-id="e4fc3-131">Wenn Sie versuchen, den AGPM-Server auf AGPM 4,0 zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-131">If you try to upgrade the AGPM server to AGPM 4.0.</span></span> <span data-ttu-id="e4fc3-132">SP2 nach der Installation von AGPM 4,0 Server und dem Installieren des AGPM-Hotfix namens AGPM 4,0 werden falsche Unterschiede im HTML-Bericht gemeldet (siehe Knowledge Base-Artikel [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), das Upgrade schlägt fehl, und kann nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-132">SP2 after installing AGPM 4.0 Server and then installing the AGPM hotfix named AGPM 4.0 reports incorrect differences in the HTML report (see Knowledge Base article [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), the upgrade fails and cannot be completed.</span></span>

<span data-ttu-id="e4fc3-133">**Problemumgehung:** Deinstallieren Sie den AGPM 4,0-Server, und installieren Sie dann AGPM 4,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-133">**Workaround:** Uninstall the AGPM 4.0 Server and then install AGPM 4.0 SP2.</span></span>

### <span data-ttu-id="e4fc3-134">In Berichten werden keine Organisations Einheits Verknüpfungen angezeigt</span><span class="sxs-lookup"><span data-stu-id="e4fc3-134">Reports do not display organizational unit links</span></span>

<span data-ttu-id="e4fc3-135">Wenn Sie ein nicht gesteuertes Gruppenrichtlinienobjekt mit einer Organisationseinheit verknüpfen und dann das Gruppenrichtlinienobjekt mithilfe von AGPM steuern, werden in den AGPM-Einstellungen und-Unterschiedsberichten die Links für die Organisationseinheit nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-135">If you link an uncontrolled GPO to an organizational unit and then control that GPO by using AGPM, the AGPM settings and difference reports do not display the organizational unit links.</span></span>

<span data-ttu-id="e4fc3-136">**Problemumgehung:** Klicken Sie auf der Registerkarte **gesteuert** des Knotens **Einstellungen ändern** mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, klicken Sie auf **Einstellungen**, und klicken Sie dann auf **GPO-Links** , um die organisatorischen Links anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-136">**Workaround:** On the **Controlled** tab of the **Change Settings** node, right-click the GPO, click **Settings**, and then click **GPO Links** to view the organizational links.</span></span> <span data-ttu-id="e4fc3-137">Sie können auch die GPMC verwenden, um die Links zu einem GPO über die Registerkarte **Bereich** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-137">Alternatively, you can use the GPMC to view the links to a GPO from the **Scope** tab.</span></span>

### <span data-ttu-id="e4fc3-138">AGPM zeigt einen Fehler an, wenn Sie im Dialogfeld "AGPM-Client ändern, reparieren oder entfernen" auf die Schaltfläche "zurück" klicken</span><span class="sxs-lookup"><span data-stu-id="e4fc3-138">AGPM displays an error if you click the Back button from the Change, Repair, or Remove AGPM Client dialog box</span></span>

<span data-ttu-id="e4fc3-139">Wenn Sie in der Systemsteuerung zu **Programme und Funktionen** navigieren und dann **Microsoft Advanced Group Policy Management – Client**auswählen, zeigt AGPM einen Fehler an, wenn Sie auf **ändern** klicken und dann im Dialogfeld **AGPM-Client ändern, reparieren oder entfernen** auf die Schaltfläche **zurück** klicken.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-139">If you browse to **Programs and Features** in Control Panel and then select **Microsoft Advanced Group Policy Management – Client**, AGPM displays an error if you click **Modify** and then click the **Back** button in the **Change, Repair, or Remove AGPM Client** dialog box.</span></span>

<span data-ttu-id="e4fc3-140">**Problemumgehung:** Klicken Sie auf **Abbrechen** , um den Fehler zu löschen, und starten Sie den Vorgang dann erneut.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-140">**Workaround:** Click **Cancel** to clear the error, and then start the process again.</span></span> <span data-ttu-id="e4fc3-141">Klicken Sie nicht auf die Schaltfläche **zurück** , nachdem Sie auf **ändern** geklickt haben.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-141">Do not click the **Back** button after you click **Modify** .</span></span>

### <span data-ttu-id="e4fc3-142">Kommentar wird im Fenster "Verlauf" nicht angezeigt, wenn die genehmigende Person ein GPO bereitstellt und einen Kommentar eingibt</span><span class="sxs-lookup"><span data-stu-id="e4fc3-142">Comment fails to appear in the History window when the Approver deploys a GPO and enters a comment</span></span>

<span data-ttu-id="e4fc3-143">Wenn ein Benutzer mit der Rolle "Bearbeiter" eine Anforderung zum Bereitstellen eines Gruppenrichtlinienobjekts übermittelt und der Benutzer, der die Rolle "genehmigende Person" hat, das Gruppenrichtlinienobjekt bereitstellt und einen Kommentar eingibt, wird der Kommentar im Fenster " **Verlauf** " nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-143">If a user who has the Editor role submits a request to deploy a GPO, and the user who has the Approver role then deploys the GPO and enters a comment, the comment fails to appear in the **History** window.</span></span>

<span data-ttu-id="e4fc3-144">**Problemumgehung:** Keine.</span><span class="sxs-lookup"><span data-stu-id="e4fc3-144">**Workaround:** None.</span></span>

## <span data-ttu-id="e4fc3-145">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="e4fc3-145">Related topics</span></span>


[<span data-ttu-id="e4fc3-146">Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="e4fc3-146">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="e4fc3-147">Neuigkeiten in AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="e4fc3-147">What's New in AGPM 4.0 SP2</span></span>](whats-new-in-agpm-40-sp2.md)

 

 





