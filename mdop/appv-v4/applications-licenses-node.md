---
title: Knoten „Anwendungslizenzen“
description: Knoten „Anwendungslizenzen“
author: dansimp
ms.assetid: 2b8752ff-aa56-483e-b844-966941af2d94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 720de1860e72ae2c71298f93e9b346afd66da569
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807936"
---
# <span data-ttu-id="03b74-103">Knoten „Anwendungslizenzen“</span><span class="sxs-lookup"><span data-stu-id="03b74-103">Applications Licenses Node</span></span>


<span data-ttu-id="03b74-104">Der Knoten Anwendungs **Lizenzen** befindet sich eine Ebene unterhalb des Knotens Application Virtualization System im **Bereich** Bereich der Application Virtualization Server-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="03b74-104">The **Applications Licenses** node is one level below the Application Virtualization System node in the **Scope** pane in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="03b74-105">Wenn Sie diesen Knoten auswählen, wird im **Ergebnis** Bereich eine Liste der Lizenzen und Lizenzgruppen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="03b74-105">When you select this node, the **Results** pane displays a list of licenses and license groups.</span></span> <span data-ttu-id="03b74-106">Die folgenden Lizenztypen sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="03b74-106">The following license types are available:</span></span>

-   <span data-ttu-id="03b74-107">**Unbegrenzte Lizenz**– bietet Zugriff für eine beliebige Anzahl von gleichzeitigen Benutzern.</span><span class="sxs-lookup"><span data-stu-id="03b74-107">**Unlimited License**—Provides access for any number of simultaneous users.</span></span> <span data-ttu-id="03b74-108">Diese Lizenzierungsmethode ist geeignet, wenn Sie einer Anwendung eine unternehmensweite Lizenz zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="03b74-108">This method of licensing is appropriate when you want to associate an enterprise-wide license with an application.</span></span>

-   <span data-ttu-id="03b74-109">**Concurrent License**– ermöglicht Ihnen, die maximale Anzahl von gleichzeitigen Benutzern zu definieren, die die Anwendung verwenden dürfen.</span><span class="sxs-lookup"><span data-stu-id="03b74-109">**Concurrent License**—Enables you to define the maximum number of concurrent users who are allowed to use the application.</span></span>

-   <span data-ttu-id="03b74-110">**Benannte Lizenz**– ermöglicht Ihnen, einem einzelnen Benutzer eine Lizenz zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="03b74-110">**Named License**—Enables you to assign a license to an individual user.</span></span> <span data-ttu-id="03b74-111">Eine benannte Lizenz kann verwendet werden, um sicherzustellen, dass ein bestimmter Benutzer immer in der Lage ist, die Anwendung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="03b74-111">A named license can be used to ensure that a particular user will always be able to run the application.</span></span>

<span data-ttu-id="03b74-112">**Hinweis**  Sie können gleichzeitige und benannte Lizenzen für dieselbe Anwendung kombinieren.</span><span class="sxs-lookup"><span data-stu-id="03b74-112">**Note** You can combine concurrent and named licenses for the same application.</span></span>

 

<span data-ttu-id="03b74-113">Klicken Sie mit der rechten Maustaste auf den Knoten **Anwendungslizenzen** , um ein Popupmenü anzuzeigen, das die folgenden Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="03b74-113">Right-click the **Applications Licenses** node to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-unlimited-license"></a>**<span data-ttu-id="03b74-114">Neue unbegrenzte Lizenz</span><span class="sxs-lookup"><span data-stu-id="03b74-114">New Unlimited License</span></span>**  
<span data-ttu-id="03b74-115">Zeigt den Assistenten für neue unbegrenzte Lizenzen an.</span><span class="sxs-lookup"><span data-stu-id="03b74-115">Displays the New Unlimited License Wizard.</span></span> <span data-ttu-id="03b74-116">Dieser Assistent besteht aus den folgenden Seiten:</span><span class="sxs-lookup"><span data-stu-id="03b74-116">This wizard consists of the following pages:</span></span>

1.  <span data-ttu-id="03b74-117">Geben Sie im Feld **Name der Anwendungslizenzgruppe** den Namen der Lizenzgruppe ein, und geben Sie einen Wert (in Minuten) im Feld " **Lizenzablauf Warnung** " ein.</span><span class="sxs-lookup"><span data-stu-id="03b74-117">Enter the name of the license group in the **Applications License Group Name** field, and enter a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="03b74-118">(Sie können einen beliebigen Wert von 0 bis 100 eingeben.) Sie können auch die nach-oben-und nach-unten-Taste verwenden, um die Anzahl der Minuten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="03b74-118">(You can enter any value from 0 through 100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="03b74-119">Geben Sie im Feld **Lizenzbeschreibung** den kurzen beschreibenden Text ein, und aktivieren Sie das Kontrollkästchen **aktiviert** , um die Lizenz zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="03b74-119">Enter brief descriptive text in the **License Description** field, and select the **Enabled** check box to enable the license.</span></span>

    <span data-ttu-id="03b74-120">Optional können Sie das Feld **Ablaufdatum** verwenden, um ein Ablaufdatum für die Lizenz anzugeben.</span><span class="sxs-lookup"><span data-stu-id="03b74-120">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="03b74-121">Sie können das Kontrollkästchen aktivieren, um das angezeigte Ablaufdatum zu verwenden, oder Sie können das Kalenderdienstprogramm verwenden, um zum gewünschten Ablaufdatum zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="03b74-121">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="03b74-122">Klicken Sie auf **Fertig stellen** , um die neue Lizenz hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="03b74-122">Click **Finish** to add the new license.</span></span>

<a href="" id="new-concurrent-license"></a>**<span data-ttu-id="03b74-123">Neue Concurrent-Lizenz</span><span class="sxs-lookup"><span data-stu-id="03b74-123">New Concurrent License</span></span>**  
<span data-ttu-id="03b74-124">Zeigt den Assistenten für neue parallel Lizenzen an.</span><span class="sxs-lookup"><span data-stu-id="03b74-124">Displays the New Concurrent License Wizard.</span></span> <span data-ttu-id="03b74-125">Dieser Assistent besteht aus den folgenden drei Seiten und ist nahezu identisch mit dem Assistenten für neue unbegrenzte Lizenzen:</span><span class="sxs-lookup"><span data-stu-id="03b74-125">This wizard consists of the following three pages and is almost identical to the New Unlimited License Wizard:</span></span>

1.  <span data-ttu-id="03b74-126">Geben Sie im Feld **Name der Anwendungslizenzgruppe** den Namen der Lizenzgruppe ein, und geben Sie einen Wert (in Minuten) im Feld " **Lizenzablauf Warnung** " ein.</span><span class="sxs-lookup"><span data-stu-id="03b74-126">Enter the name of the license group in the **Applications License Group Name** field, and enter a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="03b74-127">(Sie können einen beliebigen Wert von 0 bis 100 eingeben.) Sie können auch die nach-oben-und nach-unten-Taste verwenden, um die Anzahl der Minuten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="03b74-127">(You can enter any value from 0 through 100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="03b74-128">Geben Sie im Feld **Lizenzbeschreibung** einen kurzen beschreibenden Text ein, und geben Sie einen Wert in das Feld **Concurrent License Quantity** ein.</span><span class="sxs-lookup"><span data-stu-id="03b74-128">Enter brief descriptive text in the **License Description** field, and enter a value in the **Concurrent License Quantity** field.</span></span>

    <span data-ttu-id="03b74-129">Sie können auch die aufwärts-und Abwärtspfeile verwenden, um die Anzahl der gleichzeitigen Lizenzen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="03b74-129">You can also use the up and down arrows to specify the number of concurrent licenses.</span></span> <span data-ttu-id="03b74-130">Aktivieren Sie das Kontrollkästchen **aktiviert** , um die Lizenz zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="03b74-130">Select the **Enabled** check box to enable the license.</span></span>

    <span data-ttu-id="03b74-131">Optional können Sie das Feld **Ablaufdatum** verwenden, um ein Ablaufdatum für die Lizenz anzugeben.</span><span class="sxs-lookup"><span data-stu-id="03b74-131">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="03b74-132">Sie können das Kontrollkästchen aktivieren, um das angezeigte Ablaufdatum zu verwenden, oder Sie können das Kalenderdienstprogramm verwenden, um zum gewünschten Ablaufdatum zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="03b74-132">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="03b74-133">Klicken Sie auf **Fertig stellen** , um die neuen Lizenzen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="03b74-133">Click **Finish** to add the new licenses.</span></span>

<a href="" id="new-named-license"></a>**<span data-ttu-id="03b74-134">Neue benannte Lizenz</span><span class="sxs-lookup"><span data-stu-id="03b74-134">New Named License</span></span>**  
<span data-ttu-id="03b74-135">Zeigt den Assistenten für neue benannte Lizenzen an.</span><span class="sxs-lookup"><span data-stu-id="03b74-135">Displays the New Named License Wizard.</span></span> <span data-ttu-id="03b74-136">Dieser Assistent besteht aus den folgenden vier Seiten:</span><span class="sxs-lookup"><span data-stu-id="03b74-136">This wizard consists of the following four pages:</span></span>

1.  <span data-ttu-id="03b74-137">Geben Sie im Feld **Name der Anwendungslizenzgruppe** den Namen der Lizenzgruppe ein, und geben Sie einen Wert (in Minuten) im Feld " **Lizenzablauf Warnung** " ein.</span><span class="sxs-lookup"><span data-stu-id="03b74-137">Enter the name of the license group in the **Applications License Group Name** field, and enter a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="03b74-138">(Sie können einen beliebigen Wert von 0 bis 100 eingeben).</span><span class="sxs-lookup"><span data-stu-id="03b74-138">(You can enter any value from 0 through 100).</span></span> <span data-ttu-id="03b74-139">Sie können auch die nach-oben-und nach-unten-Taste verwenden, um die Anzahl der Minuten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="03b74-139">You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="03b74-140">Geben Sie im Feld **Lizenzbeschreibung** den kurzen beschreibenden Text ein, und aktivieren Sie das Kontrollkästchen **aktiviert** , um die Lizenz zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="03b74-140">Enter brief descriptive text in the **License Description** field, and select the **Enabled** check box to enable the license.</span></span>

    <span data-ttu-id="03b74-141">Optional können Sie das Feld **Ablaufdatum** verwenden, um ein Ablaufdatum für die Lizenz anzugeben.</span><span class="sxs-lookup"><span data-stu-id="03b74-141">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="03b74-142">Sie können das Kontrollkästchen aktivieren, um das angezeigte Ablaufdatum zu verwenden, oder Sie können das Kalenderdienstprogramm verwenden, um zum gewünschten Ablaufdatum zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="03b74-142">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="03b74-143">Klicken Sie auf benannte Benutzer **Hinzufügen**, **Bearbeiten**oder **Entfernen** .</span><span class="sxs-lookup"><span data-stu-id="03b74-143">Click **Add**, **Edit**, or **Remove** named users.</span></span>

4.  <span data-ttu-id="03b74-144">Klicken Sie auf **Fertig stellen** , um die neue Lizenz hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="03b74-144">Click **Finish** to add the new license.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="03b74-145">Ansicht</span><span class="sxs-lookup"><span data-stu-id="03b74-145">View</span></span>**  
<span data-ttu-id="03b74-146">Ändert die Darstellung und den Inhalt des **Ergebnis** Bereichs.</span><span class="sxs-lookup"><span data-stu-id="03b74-146">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="03b74-147">Neues Fenster von hier</span><span class="sxs-lookup"><span data-stu-id="03b74-147">New Window from Here</span></span>**  
<span data-ttu-id="03b74-148">Öffnet eine neue Verwaltungskonsole mit dem ausgewählten Knoten als Stammknoten.</span><span class="sxs-lookup"><span data-stu-id="03b74-148">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="03b74-149">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="03b74-149">Refresh</span></span>**  
<span data-ttu-id="03b74-150">Aktualisiert die Ansicht des Servers.</span><span class="sxs-lookup"><span data-stu-id="03b74-150">Refreshes the view of the server.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="03b74-151">Liste exportieren</span><span class="sxs-lookup"><span data-stu-id="03b74-151">Export List</span></span>**  
<span data-ttu-id="03b74-152">Erstellt eine tabstoppgetrennte Textdatei, die den Inhalt des **Ergebnis** Bereichs enthält.</span><span class="sxs-lookup"><span data-stu-id="03b74-152">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="03b74-153">Dieses Element zeigt das Dialogfeld Standard **Dateispeicherung** an, in dem Sie den Speicherort für die zu erstellende Textdatei angeben.</span><span class="sxs-lookup"><span data-stu-id="03b74-153">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="03b74-154">Hilfe</span><span class="sxs-lookup"><span data-stu-id="03b74-154">Help</span></span>**  
<span data-ttu-id="03b74-155">Zeigt das Hilfesystem für die Application Virtualization Server Management Console an.</span><span class="sxs-lookup"><span data-stu-id="03b74-155">Displays the help system for the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="03b74-156">Wenn Sie im Bereich Bereich auf eine Lizenzgruppe oder Lizenz klicken, die unter dem Knoten **Anwendungslizenzen** angezeigt wird, **stehen die folgenden** Elemente zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="03b74-156">If you click a license group or license that appears under the **Application Licenses** node in the **Scope** pane, the following elements are available.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="03b74-157">Ansicht</span><span class="sxs-lookup"><span data-stu-id="03b74-157">View</span></span>**  
<span data-ttu-id="03b74-158">Ändert die Darstellung und den Inhalt des **Ergebnis** Bereichs.</span><span class="sxs-lookup"><span data-stu-id="03b74-158">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="03b74-159">Neues Fenster von hier</span><span class="sxs-lookup"><span data-stu-id="03b74-159">New Window from Here</span></span>**  
<span data-ttu-id="03b74-160">Öffnet eine neue Verwaltungskonsole mit dem ausgewählten Knoten als Stammknoten.</span><span class="sxs-lookup"><span data-stu-id="03b74-160">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="03b74-161">Delete</span><span class="sxs-lookup"><span data-stu-id="03b74-161">Delete</span></span>**  
<span data-ttu-id="03b74-162">Löscht ein Paket aus dem **Ergebnis** Bereich.</span><span class="sxs-lookup"><span data-stu-id="03b74-162">Deletes a package from the **Results** pane.</span></span>

<a href="" id="rename"></a>**<span data-ttu-id="03b74-163">Rename</span><span class="sxs-lookup"><span data-stu-id="03b74-163">Rename</span></span>**  
<span data-ttu-id="03b74-164">Ändert den Namen eines Pakets im **Ergebnis** Bereich.</span><span class="sxs-lookup"><span data-stu-id="03b74-164">Changes the name of a package in the **Results** pane.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="03b74-165">Liste exportieren</span><span class="sxs-lookup"><span data-stu-id="03b74-165">Export List</span></span>**  
<span data-ttu-id="03b74-166">Erstellt eine tabstoppgetrennte Textdatei, die den Inhalt des **Ergebnis** Bereichs enthält.</span><span class="sxs-lookup"><span data-stu-id="03b74-166">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="03b74-167">Dieses Element zeigt das Dialogfeld Standard **Dateispeicherung** an, in dem Sie den Speicherort für die zu erstellende Textdatei angeben.</span><span class="sxs-lookup"><span data-stu-id="03b74-167">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="03b74-168">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03b74-168">Properties</span></span>**  
<span data-ttu-id="03b74-169">Zeigt das Dialogfeld " **Eigenschaften** " für die ausgewählte Lizenzgruppe an.</span><span class="sxs-lookup"><span data-stu-id="03b74-169">Displays the **Properties** dialog box for the selected license group.</span></span> <span data-ttu-id="03b74-170">Die Registerkarte " **Allgemein** " im Dialogfeld " **Eigenschaften** " zeigt Informationen zur Lizenzgruppe an und ermöglicht Ihnen, den Zeitwert im Warnungsfeld " **Lizenzablauf** " zu ändern.</span><span class="sxs-lookup"><span data-stu-id="03b74-170">The **General** tab of the **Properties** dialog box displays information about the license group and lets you change the time value in the **License Expiration Warning** field.</span></span> <span data-ttu-id="03b74-171">Auf der Registerkarte **Anwendungen** wird die Liste der Anwendungen angezeigt, die der Lizenzgruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="03b74-171">The **Applications** tab displays the list of applications associated with the license group.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="03b74-172">Hilfe</span><span class="sxs-lookup"><span data-stu-id="03b74-172">Help</span></span>**  
<span data-ttu-id="03b74-173">Zeigt das Hilfesystem für die Application Virtualization Server Management Console an.</span><span class="sxs-lookup"><span data-stu-id="03b74-173">Displays the help system for the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="03b74-174">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="03b74-174">Related topics</span></span>


[<span data-ttu-id="03b74-175">Informationen zur Anwendungslizenzierung</span><span class="sxs-lookup"><span data-stu-id="03b74-175">About Application Licensing</span></span>](about-application-licensing.md)

[<span data-ttu-id="03b74-176">So verwalten Sie Anwendungslizenzen in der Server Management Console</span><span class="sxs-lookup"><span data-stu-id="03b74-176">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="03b74-177">Server Management Console: Knoten „Anwendungslizenzen“</span><span class="sxs-lookup"><span data-stu-id="03b74-177">Server Management Console: Application Licenses Node</span></span>](server-management-console-application-licenses-node.md)

 

 





