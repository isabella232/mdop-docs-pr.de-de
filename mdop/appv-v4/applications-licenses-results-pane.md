---
title: Bereich „Ergebnisse für Anwendungslizenzen“
description: Bereich „Ergebnisse für Anwendungslizenzen“
author: dansimp
ms.assetid: 8b519715-b2fe-451e-ad9b-e9b73f454961
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e5a86c22e67e061ec873317c455958536fae75b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807935"
---
# <span data-ttu-id="1d9da-103">Bereich „Ergebnisse für Anwendungslizenzen“</span><span class="sxs-lookup"><span data-stu-id="1d9da-103">Applications Licenses Results Pane</span></span>


<span data-ttu-id="1d9da-104">Der Bereich **Anwendungen-Lizenzen Ergebnisse** in der Application Virtualization Server Management Console zeigt eine Liste der verfügbaren Anwendungslizenzgruppen und Anwendungslizenzen an.</span><span class="sxs-lookup"><span data-stu-id="1d9da-104">The **Applications Licenses Results** pane in the Application Virtualization Server Management Console displays a list of the available application license groups and application licenses.</span></span>

<span data-ttu-id="1d9da-105">Klicken Sie mit der rechten Maustaste auf eine beliebige Anwendungslizenzgruppe, um ein Popupmenü anzuzeigen, das die folgenden Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="1d9da-105">Right-click any application license group to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-unlimited-license"></a>**<span data-ttu-id="1d9da-106">Neue unbegrenzte Lizenz</span><span class="sxs-lookup"><span data-stu-id="1d9da-106">New Unlimited License</span></span>**  
<span data-ttu-id="1d9da-107">Zeigt den Assistenten für neue unbegrenzte Lizenzen an.</span><span class="sxs-lookup"><span data-stu-id="1d9da-107">Displays the New Unlimited License Wizard.</span></span> <span data-ttu-id="1d9da-108">Diese Option steht nur zur Verfügung, wenn die Lizenzgruppe keine Lizenzen aufweist.</span><span class="sxs-lookup"><span data-stu-id="1d9da-108">This option is available only when the license group has no licenses.</span></span> <span data-ttu-id="1d9da-109">Dieser Assistent besteht aus drei Seiten:</span><span class="sxs-lookup"><span data-stu-id="1d9da-109">This wizard consists of three pages:</span></span>

1.  <span data-ttu-id="1d9da-110">Geben Sie im Feld Name der **Anwendungslizenzgruppe** einen Gruppennamen und einen Wert (in Minuten) im Feld " **Lizenzablauf Warnung** " ein.</span><span class="sxs-lookup"><span data-stu-id="1d9da-110">Enter a group name in the **Applications License Group Name** field and a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="1d9da-111">(Sie können einen beliebigen Wert von 0 bis 100 eingeben.) Sie können auch die nach-oben-und nach-unten-Taste verwenden, um die Anzahl der Minuten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1d9da-111">(You can enter any value from 0–100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="1d9da-112">Geben Sie im Feld **Lizenzbeschreibung** den kurzen beschreibenden Text ein, und aktivieren Sie das Kontrollkästchen **aktiviert** .</span><span class="sxs-lookup"><span data-stu-id="1d9da-112">Enter brief descriptive text in the **License Description** field, and select the **Enabled** check box.</span></span> <span data-ttu-id="1d9da-113">Optional können Sie das Feld **Ablaufdatum** verwenden, um ein Ablaufdatum für die Lizenz anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1d9da-113">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="1d9da-114">Sie können das Standardkontrollkästchen aktivieren oder das Kalenderdienstprogramm verwenden, um zum gewünschten Ablaufdatum zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="1d9da-114">You can select the default check box or use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="1d9da-115">Klicken Sie auf **Fertig stellen** , um die neue Lizenz hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1d9da-115">Click **Finish** to add the new license.</span></span>

<a href="" id="new-concurrent-license"></a>**<span data-ttu-id="1d9da-116">Neue Concurrent-Lizenz</span><span class="sxs-lookup"><span data-stu-id="1d9da-116">New Concurrent License</span></span>**  
<span data-ttu-id="1d9da-117">Zeigt den Assistenten für neue parallel Lizenzen an.</span><span class="sxs-lookup"><span data-stu-id="1d9da-117">Displays the New Concurrent License Wizard.</span></span> <span data-ttu-id="1d9da-118">Diese Option steht nur zur Verfügung, wenn die Lizenzgruppe keine unbegrenzten Lizenzen besitzt.</span><span class="sxs-lookup"><span data-stu-id="1d9da-118">This option is available only when the license group has no unlimited licenses.</span></span> <span data-ttu-id="1d9da-119">Dieser Assistent besteht aus den folgenden Seiten und ist nahezu identisch mit dem Assistenten für neue unbegrenzte Lizenzen:</span><span class="sxs-lookup"><span data-stu-id="1d9da-119">This wizard consists of the following pages and is almost identical to the New Unlimited License Wizard:</span></span>

1.  <span data-ttu-id="1d9da-120">Geben Sie im Feld Name der **Anwendungslizenzgruppe** einen Gruppennamen und einen Wert (in Minuten) im Feld " **Lizenzablauf Warnung** " ein.</span><span class="sxs-lookup"><span data-stu-id="1d9da-120">Enter a group name in the **Applications License Group Name** field and a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="1d9da-121">(Sie können einen beliebigen Wert von 0 bis 100 eingeben.) Sie können auch die nach-oben-und nach-unten-Taste verwenden, um die Anzahl der Minuten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1d9da-121">(You can enter any value from 0–100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="1d9da-122">Geben Sie im Feld **Lizenzbeschreibung** einen kurzen beschreibenden Text ein, und geben Sie einen Wert in das Feld **Concurrent License Quantity** ein.</span><span class="sxs-lookup"><span data-stu-id="1d9da-122">Enter brief descriptive text in the **License Description** field, and enter a value in the **Concurrent License Quantity** field.</span></span> <span data-ttu-id="1d9da-123">Sie können auch die aufwärts-und Abwärtspfeile verwenden, um die Anzahl der gleichzeitigen Lizenzen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1d9da-123">You can also use the up and down arrows to specify the number of concurrent licenses.</span></span> <span data-ttu-id="1d9da-124">Aktivieren Sie das Kontrollkästchen **aktiviert** , um die Lizenz zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1d9da-124">Select the **Enabled** check box to enable the license.</span></span> <span data-ttu-id="1d9da-125">Optional können Sie das Feld **Ablaufdatum** verwenden, um ein Ablaufdatum für die Lizenz auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="1d9da-125">Optionally, you can use the **Expiration Date** field to select an expiration date for the license.</span></span> <span data-ttu-id="1d9da-126">Sie können das Kontrollkästchen aktivieren, um das angezeigte Ablaufdatum zu verwenden, oder Sie können das Kalenderdienstprogramm verwenden, um zum gewünschten Ablaufdatum zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="1d9da-126">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="1d9da-127">Klicken Sie auf **Fertig stellen** , um die neuen Lizenzen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1d9da-127">Click **Finish** to add the new licenses.</span></span>

<a href="" id="new-named-license"></a>**<span data-ttu-id="1d9da-128">Neue benannte Lizenz</span><span class="sxs-lookup"><span data-stu-id="1d9da-128">New Named License</span></span>**  
<span data-ttu-id="1d9da-129">Zeigt den Assistenten für neue benannte Lizenzen an.</span><span class="sxs-lookup"><span data-stu-id="1d9da-129">Displays the New Named License Wizard.</span></span> <span data-ttu-id="1d9da-130">Diese Option steht nur zur Verfügung, wenn die Lizenzgruppe keine unbegrenzten Lizenzen besitzt.</span><span class="sxs-lookup"><span data-stu-id="1d9da-130">This option is available only when the license group has no unlimited licenses.</span></span> <span data-ttu-id="1d9da-131">Dieser Assistent besteht aus den folgenden Seiten:</span><span class="sxs-lookup"><span data-stu-id="1d9da-131">This wizard consists of the following pages:</span></span>

1.  <span data-ttu-id="1d9da-132">Geben Sie im Feld Name der **Anwendungslizenzgruppe** einen Gruppennamen und einen Wert (in Minuten) im Feld " **Lizenzablauf Warnung** " ein.</span><span class="sxs-lookup"><span data-stu-id="1d9da-132">Enter a group name in the **Applications License Group Name** field and a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="1d9da-133">(Sie können einen beliebigen Wert von 0 bis 100 eingeben.) Sie können auch die nach-oben-und nach-unten-Taste verwenden, um die Anzahl der Minuten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1d9da-133">(You can enter any value from 0–100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="1d9da-134">Geben Sie einen kurzen beschreibenden Text in die **Lizenzbeschreibung**ein, und aktivieren Sie das Kontrollkästchen **aktiviert** .</span><span class="sxs-lookup"><span data-stu-id="1d9da-134">Enter brief descriptive text in the **License Description**, and select the **Enabled** check box.</span></span> <span data-ttu-id="1d9da-135">Optional können Sie das Feld **Ablaufdatum** verwenden, um ein Ablaufdatum für die Lizenz anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1d9da-135">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="1d9da-136">Sie können das Kontrollkästchen aktivieren, um das angezeigte Ablaufdatum zu verwenden, oder das Kalenderdienstprogramm verwenden, um zum gewünschten Ablaufdatum zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="1d9da-136">You can select the check box to use the displayed expiration date, or use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="1d9da-137">Klicken Sie auf benannte Benutzer **Hinzufügen**, **Bearbeiten**oder **Entfernen** .</span><span class="sxs-lookup"><span data-stu-id="1d9da-137">Click **Add**, **Edit**, or **Remove** named users.</span></span>

4.  <span data-ttu-id="1d9da-138">Klicken Sie auf **Fertig stellen** , um die neue Lizenz hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1d9da-138">Click **Finish** to add the new license.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="1d9da-139">Neues Fenster von hier</span><span class="sxs-lookup"><span data-stu-id="1d9da-139">New Window from Here</span></span>**  
<span data-ttu-id="1d9da-140">Öffnet eine neue Verwaltungskonsole mit dem ausgewählten Knoten als Stammknoten.</span><span class="sxs-lookup"><span data-stu-id="1d9da-140">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="1d9da-141">Delete</span><span class="sxs-lookup"><span data-stu-id="1d9da-141">Delete</span></span>**  
<span data-ttu-id="1d9da-142">Löscht die Lizenzgruppe aus der Liste.</span><span class="sxs-lookup"><span data-stu-id="1d9da-142">Deletes the license group from the list.</span></span>

<a href="" id="rename"></a>**<span data-ttu-id="1d9da-143">Rename</span><span class="sxs-lookup"><span data-stu-id="1d9da-143">Rename</span></span>**  
<span data-ttu-id="1d9da-144">Ändert den Namen der Anwendungslizenzgruppe.</span><span class="sxs-lookup"><span data-stu-id="1d9da-144">Changes the name of the applications license group.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="1d9da-145">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1d9da-145">Properties</span></span>**  
<span data-ttu-id="1d9da-146">Zeigt das Dialogfeld **Eigenschaften** für die ausgewählten Anwendungslizenzgruppen an.</span><span class="sxs-lookup"><span data-stu-id="1d9da-146">Displays the **Properties** dialog box for the selected application license groups.</span></span> <span data-ttu-id="1d9da-147">Dieses Dialogfeld enthält die folgenden Registerkarten:</span><span class="sxs-lookup"><span data-stu-id="1d9da-147">This dialog box has the following tabs:</span></span>

-   <span data-ttu-id="1d9da-148">Registerkarte **Allgemein** – zeigt allgemeine Informationen zur Lizenzgruppe an.</span><span class="sxs-lookup"><span data-stu-id="1d9da-148">**General** tab—Displays general information about the license group.</span></span> <span data-ttu-id="1d9da-149">Auf dieser Registerkarte können Sie den Zeitwert (in Minuten) im Feld " **Lizenzablauf Warnung** " ändern.</span><span class="sxs-lookup"><span data-stu-id="1d9da-149">From this tab, you can change the time value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="1d9da-150">Sie können einen beliebigen Wert von 0 – 100 eingeben.</span><span class="sxs-lookup"><span data-stu-id="1d9da-150">You can enter any value from 0–100.</span></span>

-   <span data-ttu-id="1d9da-151">Registerkarte **Anwendungen** – zeigt die Liste der Anwendungen an, die der Lizenzgruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1d9da-151">**Applications** tab—Displays the list of applications associated with the license group.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="1d9da-152">Hilfe</span><span class="sxs-lookup"><span data-stu-id="1d9da-152">Help</span></span>**  
<span data-ttu-id="1d9da-153">Zeigt das Hilfesystem der Application Virtualization Server Management Console an.</span><span class="sxs-lookup"><span data-stu-id="1d9da-153">Displays the Application Virtualization Server Management Console help system.</span></span>

<span data-ttu-id="1d9da-154">Wenn im Bereich " **Ergebnisse** " Anwendungslizenzgruppen angezeigt werden, klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im **Ergebnis** Bereich, mit Ausnahme einer Lizenzgruppe, um ein Popupmenü anzuzeigen, das die folgenden Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="1d9da-154">When the **Results** pane displays application license groups, right-click anywhere in the **Results** pane, except on a license group, to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="1d9da-155">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="1d9da-155">Refresh</span></span>**  
<span data-ttu-id="1d9da-156">Aktualisiert die Ansicht des Servers.</span><span class="sxs-lookup"><span data-stu-id="1d9da-156">Refreshes the view of the server.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="1d9da-157">Liste exportieren</span><span class="sxs-lookup"><span data-stu-id="1d9da-157">Export List</span></span>**  
<span data-ttu-id="1d9da-158">Erstellt eine tabstoppgetrennte Textdatei, die den Inhalt des **Ergebnis** Bereichs enthält.</span><span class="sxs-lookup"><span data-stu-id="1d9da-158">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="1d9da-159">Dieses Element zeigt das Dialogfeld Standard **Dateispeicherung** an, in dem Sie den Speicherort für die zu erstellende Textdatei angeben.</span><span class="sxs-lookup"><span data-stu-id="1d9da-159">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="1d9da-160">Ansicht</span><span class="sxs-lookup"><span data-stu-id="1d9da-160">View</span></span>**  
<span data-ttu-id="1d9da-161">Ändert die Darstellung und den Inhalt des **Ergebnis** Bereichs.</span><span class="sxs-lookup"><span data-stu-id="1d9da-161">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="arrange-line-up-icons"></a>**<span data-ttu-id="1d9da-162">Symbole für anordnen/ausrichten</span><span class="sxs-lookup"><span data-stu-id="1d9da-162">Arrange/Line Up Icons</span></span>**  
<span data-ttu-id="1d9da-163">Ändert, wie die Symbole im **Ergebnis** Bereich angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1d9da-163">Changes how the icons are displayed in the **Results** pane.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="1d9da-164">Hilfe</span><span class="sxs-lookup"><span data-stu-id="1d9da-164">Help</span></span>**  
<span data-ttu-id="1d9da-165">Zeigt das Hilfesystem für die Application Virtualization Server Management Console an.</span><span class="sxs-lookup"><span data-stu-id="1d9da-165">Displays the help system for the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="1d9da-166">Wenn im Bereich " **Ergebnisse** " Lizenzen angezeigt werden, klicken Sie mit der rechten Maustaste auf eine beliebige Anwendungslizenz, um ein Popupmenü anzuzeigen, das die folgenden Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="1d9da-166">When the **Results** pane displays licenses, right-click any application license to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="1d9da-167">Delete</span><span class="sxs-lookup"><span data-stu-id="1d9da-167">Delete</span></span>**  
<span data-ttu-id="1d9da-168">Löscht die Lizenz aus der Liste.</span><span class="sxs-lookup"><span data-stu-id="1d9da-168">Deletes the license from the list.</span></span>

<a href="" id="rename"></a>**<span data-ttu-id="1d9da-169">Rename</span><span class="sxs-lookup"><span data-stu-id="1d9da-169">Rename</span></span>**  
<span data-ttu-id="1d9da-170">Ändert den Namen der Lizenz.</span><span class="sxs-lookup"><span data-stu-id="1d9da-170">Changes the name of the license.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="1d9da-171">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1d9da-171">Properties</span></span>**  
<span data-ttu-id="1d9da-172">Zeigt das Dialogfeld **Eigenschaften** für die ausgewählte Anwendungslizenz an.</span><span class="sxs-lookup"><span data-stu-id="1d9da-172">Displays the **Properties** dialog box for the selected application license.</span></span>

<span data-ttu-id="1d9da-173">Die Registerkarte " **Allgemein** " im Dialogfeld " **Eigenschaften** " zeigt Informationen zur Lizenz an und ermöglicht Ihnen, den aktivierten Status, das Ablaufdatum der Lizenz und die Lizenzschlüsselinformationen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1d9da-173">The **General** tab of the **Properties** dialog box displays information about the license and lets you change the enabled status, license expiration date, and license key information.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="1d9da-174">Hilfe</span><span class="sxs-lookup"><span data-stu-id="1d9da-174">Help</span></span>**  
<span data-ttu-id="1d9da-175">Zeigt das Hilfesystem der Serververwaltungskonsole an.</span><span class="sxs-lookup"><span data-stu-id="1d9da-175">Displays the server management console help system.</span></span>

<span data-ttu-id="1d9da-176">Wenn im Bereich " **Ergebnisse** " Lizenzen angezeigt werden, klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im **Ergebnis** Bereich, außer auf eine Lizenz, um ein Popupmenü anzuzeigen, das die folgenden Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="1d9da-176">When the **Results** pane displays licenses, right-click anywhere in the **Results** pane, except on a license, to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="1d9da-177">Liste exportieren</span><span class="sxs-lookup"><span data-stu-id="1d9da-177">Export List</span></span>**  
<span data-ttu-id="1d9da-178">Erstellt eine tabstoppgetrennte Textdatei, die den Inhalt des **Ergebnis** Bereichs enthält.</span><span class="sxs-lookup"><span data-stu-id="1d9da-178">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="1d9da-179">Dieses Element zeigt das Dialogfeld Standard **Dateispeicherung** an, in dem Sie den Speicherort für die zu erstellende Textdatei angeben.</span><span class="sxs-lookup"><span data-stu-id="1d9da-179">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="1d9da-180">Ansicht</span><span class="sxs-lookup"><span data-stu-id="1d9da-180">View</span></span>**  
<span data-ttu-id="1d9da-181">Ändert die Darstellung und den Inhalt des **Ergebnis** Bereichs.</span><span class="sxs-lookup"><span data-stu-id="1d9da-181">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="arrange-line-up-icons"></a>**<span data-ttu-id="1d9da-182">Symbole für anordnen/ausrichten</span><span class="sxs-lookup"><span data-stu-id="1d9da-182">Arrange/Line Up Icons</span></span>**  
<span data-ttu-id="1d9da-183">Ändert, wie die Symbole im **Ergebnis** Bereich angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1d9da-183">Changes how the icons are displayed in the **Results** pane.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="1d9da-184">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1d9da-184">Properties</span></span>**  
<span data-ttu-id="1d9da-185">Zeigt das Dialogfeld " **Eigenschaften** " für die ausgewählte Lizenz an.</span><span class="sxs-lookup"><span data-stu-id="1d9da-185">Displays the **Properties** dialog box for the selected license.</span></span>

<span data-ttu-id="1d9da-186">Die Registerkarte " **Allgemein** " im Dialogfeld " **Eigenschaften** " zeigt Informationen zur Lizenz an und ermöglicht Ihnen, den aktivierten Status, das Ablaufdatum der Lizenz und die Lizenzschlüsselinformationen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1d9da-186">The **General** tab of the **Properties** dialog box displays information about the license and lets you change the enabled status, license expiration date, and license key information.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="1d9da-187">Hilfe</span><span class="sxs-lookup"><span data-stu-id="1d9da-187">Help</span></span>**  
<span data-ttu-id="1d9da-188">Zeigt das Hilfesystem für die Application Virtualization Server Management Console an.</span><span class="sxs-lookup"><span data-stu-id="1d9da-188">Displays the help system for the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="1d9da-189">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1d9da-189">Related topics</span></span>


[<span data-ttu-id="1d9da-190">Informationen zur Anwendungslizenzierung</span><span class="sxs-lookup"><span data-stu-id="1d9da-190">About Application Licensing</span></span>](about-application-licensing.md)

[<span data-ttu-id="1d9da-191">So verwalten Sie Anwendungslizenzen in der Server Management Console</span><span class="sxs-lookup"><span data-stu-id="1d9da-191">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="1d9da-192">Server Management Console: Knoten „Anwendungslizenzen“</span><span class="sxs-lookup"><span data-stu-id="1d9da-192">Server Management Console: Application Licenses Node</span></span>](server-management-console-application-licenses-node.md)

 

 





