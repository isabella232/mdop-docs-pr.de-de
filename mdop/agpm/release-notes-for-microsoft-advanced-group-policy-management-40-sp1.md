---
title: Versionshinweise für Microsoft Advanced Group Policy Management 4.0 SP1
description: Versionshinweise für Microsoft Advanced Group Policy Management 4.0 SP1
author: dansimp
ms.assetid: 91835bf8-e53c-4202-986e-8d37050d1267
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff9ce0405df766aef9b30e67d07ceb579c4fa89f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807544"
---
# <span data-ttu-id="b41ed-103">Versionshinweise für Microsoft Advanced Group Policy Management 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="b41ed-103">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP1</span></span>


<span data-ttu-id="b41ed-104">Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="b41ed-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="b41ed-105">Lesen Sie diese Versionshinweise gründlich, bevor Sie Microsoft Advanced Group Policy Management (AGPM) 4,0 SP1 installieren.</span><span class="sxs-lookup"><span data-stu-id="b41ed-105">Read these release notes thoroughly before you install Microsoft Advanced Group Policy Management (AGPM) 4.0 SP1.</span></span> <span data-ttu-id="b41ed-106">Diese Versionshinweise enthalten Informationen, die erforderlich sind, um AGPM 4,0 SP1 erfolgreich zu installieren und Informationen zu enthalten, die in der Produktdokumentation nicht zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="b41ed-106">These release notes contain information that is required to successfully install AGPM 4.0 SP1 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="b41ed-107">Wenn es einen Unterschied zwischen diesen Versionshinweisen und anderer AGPM-Dokumentation gibt, sollte die neueste Änderung als autorisierend angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="b41ed-107">If there is a difference between these release notes and other AGPM documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="b41ed-108">Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b41ed-108">These release notes supersede the content included with this product.</span></span>

## <span data-ttu-id="b41ed-109">Bekannte Probleme mit AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="b41ed-109">AGPM 4.0 SP1 known issues</span></span>


<span data-ttu-id="b41ed-110">Dieser Abschnitt enthält Anmerkungen zu dieser Version von AGPM 4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="b41ed-110">This section contains release notes for AGPM 4.0 SP1.</span></span>

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a><span data-ttu-id="b41ed-111">Das Tool "deinstallieren" der Systemsteuerung funktioniert möglicherweise nicht, wenn Sie versuchen, AGPM-Server Einstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b41ed-111">Control Panel’s “Uninstall” tool may not work when you try to change AGPM Server settings</span></span>

<span data-ttu-id="b41ed-112">Das Tool in der Systemsteuerung, mit dem Sie ein Programm deinstallieren oder ändern können, funktioniert möglicherweise nicht, wenn Sie versuchen, AGPM-Servereinstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b41ed-112">The tool in Control Panel that lets you uninstall or change a program may not work when you try to change AGPM server settings.</span></span>

<span data-ttu-id="b41ed-113">Problemumgehung: Erstellen Sie eine Kopie des AGPM-Archivordners, bevor Sie versuchen, AGPM-Servereinstellungen mithilfe der Systemsteuerung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b41ed-113">WORKAROUND: Before you try to change AGPM server settings by using Control Panel, make a copy of the AGPM Archive folder.</span></span> <span data-ttu-id="b41ed-114">Anschließend können Sie Setup.exe verwenden, um den AGPM-Server erneut zu installieren und die gewünschten Konfigurationsparameter auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="b41ed-114">You can then use Setup.exe to reinstall the AGPM server and choose the configuration parameters that you want.</span></span>

### <span data-ttu-id="b41ed-115">In Berichten werden die Links, die einem Gruppenrichtlinienobjekt hinzugefügt wurden, nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b41ed-115">Reports do not display the links that were added to a Group Policy Object</span></span>

<span data-ttu-id="b41ed-116">Die AGPM-Einstellungen und-Differenz Berichte zeigen nicht die Links an, die einem Gruppenrichtlinienobjekt (Group Policy Object, GPO) hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="b41ed-116">The AGPM settings and difference reports do not display the links that were added to a Group Policy Object (GPO).</span></span>

<span data-ttu-id="b41ed-117">Problemumgehung: Wenn Sie die Links in den Berichten anzeigen möchten, wählen Sie das Gruppenrichtlinienobjekt in der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) aus, und klicken Sie im rechten Bereich auf die Registerkarte **Einstellungen** .</span><span class="sxs-lookup"><span data-stu-id="b41ed-117">WORKAROUND: To view the links in the reports, select the GPO in the Group Policy Management Console (GPMC), and click the **Settings** tab in the right pane.</span></span>

### <a href="" id="reports-do-not-display-all--choice-options-properties--settings"></a><span data-ttu-id="b41ed-118">In den Berichten werden nicht alle Einstellungen für "Auswahloptionen" angezeigt</span><span class="sxs-lookup"><span data-stu-id="b41ed-118">Reports do not display all “Choice Options Properties” settings</span></span>

<span data-ttu-id="b41ed-119">Die AGPM-Einstellungen und-Differenz Berichte zeigen nicht alle Einstellungen an, die im Eigenschaftenfenster der Auswahloptionen im Gruppenrichtlinienobjekt-Editor ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="b41ed-119">The AGPM settings and difference reports do not display all of the settings that were selected on the Choice Options Properties window in the Group Policy Object Editor.</span></span>

<span data-ttu-id="b41ed-120">Problemumgehung: Verwenden Sie die GPMC, um die ausgewählten Eigenschafteneinstellungen für Auswahloptionen in den Berichten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b41ed-120">WORKAROUND: Use the GPMC to view the selected Choice Options Properties settings in the reports.</span></span>

### <span data-ttu-id="b41ed-121">In bestimmten Browsern werden in Berichten die Registerkarten "einblenden" und "ausblenden" nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b41ed-121">Reports do not display the Show and Hide tabs in certain browsers</span></span>

<span data-ttu-id="b41ed-122">Die Registerkarten "einblenden" und "ausblenden" werden auf der rechten Seite der AGPM-Einstellungen und-Differenz Berichte nicht angezeigt, wenn Sie die Berichte in Google Chrome oder Mozilla Firefox anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b41ed-122">The Show and Hide tabs, shown on the right side of the AGPM settings and difference reports, are not displayed when you view the reports in Google Chrome or Mozilla Firefox.</span></span>

<span data-ttu-id="b41ed-123">Problemumgehung: Anzeigen der Berichte mithilfe von Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b41ed-123">WORKAROUND: View the reports by using Internet Explorer.</span></span>

### <span data-ttu-id="b41ed-124">AGPM-Einstellungen und Unterschiedsberichte können unterschiedliche Inhalte aus GPMC-Berichten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b41ed-124">AGPM settings and difference reports may show different content from GPMC reports</span></span>

<span data-ttu-id="b41ed-125">Die AGPM-Einstellungen und-Differenz Berichte zeigen möglicherweise nicht denselben Inhalt wie Berichte in der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) an.</span><span class="sxs-lookup"><span data-stu-id="b41ed-125">The AGPM settings and difference reports may not show the same content as reports in the Group Policy Management Console (GPMC).</span></span>

<span data-ttu-id="b41ed-126">Problemumgehung: Verwenden Sie die GPMC, um die AGPM-Berichte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b41ed-126">WORKAROUND: Use the GPMC to view the AGPM reports.</span></span>

### <span data-ttu-id="b41ed-127">AGPM-Dienst wird nicht gestartet, wenn der Domänencontroller nicht online ist</span><span class="sxs-lookup"><span data-stu-id="b41ed-127">AGPM Service does not start if the domain controller is not online</span></span>

<span data-ttu-id="b41ed-128">Wenn der AGPM-Dienst auf einem Domänencontroller unter Windows 8 installiert ist, wird der Dienst nicht gestartet, wenn der Domänencontroller nicht online ist.</span><span class="sxs-lookup"><span data-stu-id="b41ed-128">When the AGPM Service is installed on a domain controller on Windows 8, the Service does not start if the domain controller is not online.</span></span>

<span data-ttu-id="b41ed-129">Problemumgehung: Starten Sie den AGPM-Dienst manuell, nachdem der Domänencontroller online ist.</span><span class="sxs-lookup"><span data-stu-id="b41ed-129">WORKAROUND: Manually start the AGPM Service after the domain controller is online.</span></span>

### <span data-ttu-id="b41ed-130">Das Upgrade des AGPM-Servers auf AGPM 4,0 SP1 wird blockiert, wenn Sie ein Upgrade von der AGPM 4,0-Version und dem Hotfix durchführen.</span><span class="sxs-lookup"><span data-stu-id="b41ed-130">Upgrade of AGPM Server to AGPM 4.0 SP1 is blocked when you upgrade from the AGPM 4.0 release plus the hotfix</span></span>

<span data-ttu-id="b41ed-131">Wenn Sie versuchen, den AGPM-Server auf AGPM 4,0 zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b41ed-131">If you try to upgrade the AGPM server to AGPM 4.0.</span></span> <span data-ttu-id="b41ed-132">SP1 nachdem Sie AGPM 4,0 installiert und dann den AGPM-Hotfix installiert haben (siehe Knowledge Base-Artikel [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), schlägt die Aktualisierung fehl und kann nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="b41ed-132">SP1 after installing AGPM 4.0 and then installing the AGPM hotfix (see Knowledge Base article [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), the upgrade fails and cannot be completed.</span></span>

<span data-ttu-id="b41ed-133">Problemumgehung: Deinstallieren Sie den AGPM 4,0-Server, und installieren Sie dann AGPM 4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="b41ed-133">WORKAROUND: Uninstall the AGPM 4.0 Server and then install AGPM 4.0 SP1.</span></span>

### <span data-ttu-id="b41ed-134">In Berichten werden keine Organisations Einheits Verknüpfungen angezeigt</span><span class="sxs-lookup"><span data-stu-id="b41ed-134">Reports do not display organizational unit links</span></span>

<span data-ttu-id="b41ed-135">Wenn Sie ein nicht gesteuertes Gruppenrichtlinienobjekt mit einer Organisationseinheit verknüpfen und dann das Gruppenrichtlinienobjekt mithilfe von AGPM steuern, werden in den AGPM-Einstellungen und-Unterschiedsberichten die Links für die Organisationseinheit nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b41ed-135">If you link an uncontrolled GPO to an organizational unit and then control that GPO using AGPM, the AGPM settings and difference reports do not display the organizational unit links.</span></span>

<span data-ttu-id="b41ed-136">Problemumgehung: Klicken Sie auf der Registerkarte **gesteuert** des Knotens **Einstellungen ändern** mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, klicken Sie auf **Einstellungen** , und klicken Sie dann auf **GPO-Links** , um die Organisations Verknüpfungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b41ed-136">WORKAROUND: From the **Controlled** tab of the **Change Settings** node, right-click the GPO and click **Settings** and then click **GPO Links** to view the organizational links.</span></span> <span data-ttu-id="b41ed-137">Sie können auch die GPMC verwenden, um die Links zu einem GPO über die Registerkarte **Bereich** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b41ed-137">Alternatively, you can use the GPMC to view the links to a GPO from the **Scope** tab.</span></span>

## <span data-ttu-id="b41ed-138">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b41ed-138">Related topics</span></span>


[<span data-ttu-id="b41ed-139">Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="b41ed-139">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="b41ed-140">Neuigkeiten in AGPM 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="b41ed-140">What's New in AGPM 4.0 SP1</span></span>](whats-new-in-agpm-40-sp1.md)

 

 





