---
title: So generieren Sie Berichte
description: So generieren Sie Berichte
author: dansimp
ms.assetid: 9f8ba28e-1993-4c11-a28a-493718051e5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 930b7061d3e5e2fb9951d45b1422915836cbc00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812088"
---
# <span data-ttu-id="3bb11-103">So generieren Sie Berichte</span><span class="sxs-lookup"><span data-stu-id="3bb11-103">How to Generate Reports</span></span>


<span data-ttu-id="3bb11-104">Die folgenden Berichtstypen können von Administratoren in MED-V erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="3bb11-104">The following report types can be created by administrators in MED-V:</span></span>

-   <span data-ttu-id="3bb11-105">[Status](#bkmk-generatingastatusreport)– verwenden Sie den Statusbericht, um den aktuellen Status aller aktiven Benutzer und aller MED-V-Arbeitsbereiche jedes Benutzers auf Grundlage eines definierten Zeitraums zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3bb11-105">[Status](#bkmk-generatingastatusreport)—Use the status report to review the current status of all active users and all MED-V workspaces of each user based on a defined period of time.</span></span> <span data-ttu-id="3bb11-106">Dazu gehören das Anzeigen von Computern, die derzeit mit dem Server verbunden sind, oder, wenn Sie derzeit nicht verbunden sind, das Datum und die Uhrzeit der letzten Verbindung mit dem Server, den Status der einzelnen Computer und andere relevante Informationen.</span><span class="sxs-lookup"><span data-stu-id="3bb11-106">This includes viewing computers that are currently connected to the server or, if they are not currently connected, the date and time they were last connected to the server, the status of each computer, and other relevant information.</span></span>

-   <span data-ttu-id="3bb11-107">[Aktivitätsprotokoll](#bkmk-generatinganactivitylogreport)– verwenden Sie diesen Bericht, um Ereignisse zu überprüfen, die von einem bestimmten Host oder Benutzer in einem definierten Datumsbereich stammen.</span><span class="sxs-lookup"><span data-stu-id="3bb11-107">[Activity Log](#bkmk-generatinganactivitylogreport)—Use this report to review events that originated from a specific host or user in a defined date range.</span></span>

-   <span data-ttu-id="3bb11-108">[Fehlerprotokoll](#bkmk-generatinganerrorlogreport)– verwenden Sie diesen Bericht, um Fehler anzuzeigen, die von einem bestimmten Host oder Benutzer in einem definierten Datumsbereich stammen.</span><span class="sxs-lookup"><span data-stu-id="3bb11-108">[Error Log](#bkmk-generatinganerrorlogreport)—Use this report to view errors that originated from a specific host or user in a defined date range.</span></span>

<span data-ttu-id="3bb11-109">Die Berichtsergebnisse können nach jeder beliebigen Spalte sortiert werden, indem Sie auf den entsprechenden Spaltennamen klicken.</span><span class="sxs-lookup"><span data-stu-id="3bb11-109">The report results can be sorted by any column by clicking the appropriate column name.</span></span>

<span data-ttu-id="3bb11-110">Die Berichtsergebnisse können gruppiert werden, indem Sie eine Spaltenüberschrift an den Anfang des Berichts ziehen.</span><span class="sxs-lookup"><span data-stu-id="3bb11-110">The report results can be grouped by dragging a column header to the top of the report.</span></span> <span data-ttu-id="3bb11-111">Ziehen Sie mehrere Spaltenüberschriften, um eine Spalte nach der anderen zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="3bb11-111">Drag multiple column headers to group one column after another.</span></span>

## <a href="" id="bkmk-generatingastatusreport"></a><span data-ttu-id="3bb11-112">Erstellen eines Status Berichts</span><span class="sxs-lookup"><span data-stu-id="3bb11-112">How to Generate a Status Report</span></span>


**<span data-ttu-id="3bb11-113">So erstellen Sie einen Statusbericht</span><span class="sxs-lookup"><span data-stu-id="3bb11-113">To generate a status report</span></span>**

1.  <span data-ttu-id="3bb11-114">Klicken Sie auf die Schaltfläche **Berichts** Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="3bb11-114">Click the **Reports** management button.</span></span>

2.  <span data-ttu-id="3bb11-115">Wählen Sie im Modul **Berichte** im Menü **Berichtstypen** den Eintrag **Status**aus, und klicken Sie auf **generieren**.</span><span class="sxs-lookup"><span data-stu-id="3bb11-115">In the **Reports** module, on the **Report Types** menu, select **Status**, and click **Generate**.</span></span>

    <span data-ttu-id="3bb11-116">Das Dialogfeld Berichtsparameter wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3bb11-116">The Report Parameters dialog box appears.</span></span>

3.  <span data-ttu-id="3bb11-117">Geben Sie im Dialogfeld **Berichtsparameter** im Feld **Anzahl der Tage** eine Zahl ein, oder verwenden Sie die Pfeile, um die Anzahl der Tage auszuwählen, die in den Statusbericht aufgenommen werden sollen, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="3bb11-117">In the **Report Parameters** dialog box, in the **Number of days** field, enter a number or use the arrows to select the number of days to include in the status report, and click **OK**.</span></span>

    <span data-ttu-id="3bb11-118">Es wird ein Statusbericht generiert.</span><span class="sxs-lookup"><span data-stu-id="3bb11-118">A status report is generated.</span></span> <span data-ttu-id="3bb11-119">Die Berichtsparameter sind in der folgenden Tabelle definiert.</span><span class="sxs-lookup"><span data-stu-id="3bb11-119">The report parameters are defined in the following table.</span></span>

**<span data-ttu-id="3bb11-120">Client MED-V-Arbeitsbereichseigenschaften</span><span class="sxs-lookup"><span data-stu-id="3bb11-120">Client MED-V Workspace Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3bb11-121">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3bb11-121">Property</span></span></th>
<th align="left"><span data-ttu-id="3bb11-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3bb11-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bb11-123">Zeit</span><span class="sxs-lookup"><span data-stu-id="3bb11-123">Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-124">Das Datum und die Uhrzeit, zu der das Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="3bb11-124">The date and time the event occurred.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3bb11-125">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3bb11-125">Note</span></span></strong><br/><p><span data-ttu-id="3bb11-126">Standardmäßig werden die Ereignisse in absteigender Datumsreihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3bb11-126">By default, the events are displayed in descending date order.</span></span> <span data-ttu-id="3bb11-127">Sie können jedoch durch Klicken auf die Spalte Zeit empfangen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3bb11-127">However, it can be changed by clicking the Time Received column.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bb11-128">Benutzername</span><span class="sxs-lookup"><span data-stu-id="3bb11-128">User Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-129">Der Benutzer, der das Ereignis initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="3bb11-129">The user who initiated the event.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3bb11-130">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3bb11-130">Note</span></span></strong><br/><p><span data-ttu-id="3bb11-131">Wenn das Ereignis vor einem angemeldeten Benutzer aufgetreten ist, lautet der Benutzername "System".</span><span class="sxs-lookup"><span data-stu-id="3bb11-131">If the event occurred before a user logged on, the user name is SYSTEM.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bb11-132">Hostname</span><span class="sxs-lookup"><span data-stu-id="3bb11-132">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-133">Der Name des Hostcomputers.</span><span class="sxs-lookup"><span data-stu-id="3bb11-133">The name of the host computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bb11-134">Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="3bb11-134">Workspace Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-135">Der Name des MED-V-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="3bb11-135">The name of the MED-V workspace.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bb11-136">Arbeitsbereichs Computer Name</span><span class="sxs-lookup"><span data-stu-id="3bb11-136">Workspace Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-137">Der Name des Computers, auf dem der MED-V-Arbeitsbereich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3bb11-137">The name of the computer the MED-V workspace is running on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bb11-138">Online</span><span class="sxs-lookup"><span data-stu-id="3bb11-138">Online</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-139">Der aktuelle Status des Clientcomputers:</span><span class="sxs-lookup"><span data-stu-id="3bb11-139">The current state of the client computer:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="3bb11-140">Funktioniert nicht mehr</span><span class="sxs-lookup"><span data-stu-id="3bb11-140">Stopped</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="3bb11-141">Begonnen zu &lt; Datum und Uhrzeit des Starts des Arbeitsbereichs&gt;</span><span class="sxs-lookup"><span data-stu-id="3bb11-141">Started at &lt;date and time the workspace was started&gt;</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bb11-142">Client Version</span><span class="sxs-lookup"><span data-stu-id="3bb11-142">Client Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-143">Die Versionsnummer des Clients.</span><span class="sxs-lookup"><span data-stu-id="3bb11-143">The version number of the client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bb11-144">Richtlinien Version</span><span class="sxs-lookup"><span data-stu-id="3bb11-144">Policy Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-145">Die Richtlinienversion, die der MED-V Workspace zurzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="3bb11-145">The policy version that the MED-V workspace is currently using.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bb11-146">Name des Bilds</span><span class="sxs-lookup"><span data-stu-id="3bb11-146">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-147">Der Name des Bilds.</span><span class="sxs-lookup"><span data-stu-id="3bb11-147">The name of the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bb11-148">Bild Version</span><span class="sxs-lookup"><span data-stu-id="3bb11-148">Image Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-149">Die Bildversion, die der MED-V Workspace zurzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="3bb11-149">The image version that the MED-V workspace is currently using.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3bb11-150">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3bb11-150">Note</span></span></strong><br/><p><span data-ttu-id="3bb11-151">Die Version des MED-V-Arbeitsbereichs kann unbekannt sein, wenn Sie noch nicht auf einen Computer heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="3bb11-151">MED-V workspace version can be Unknown if it has not yet been downloaded onto a computer.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganactivitylogreport"></a><span data-ttu-id="3bb11-152">Erstellen eines Aktivitätsprotokoll Berichts</span><span class="sxs-lookup"><span data-stu-id="3bb11-152">How to Generate an Activity Log Report</span></span>


**<span data-ttu-id="3bb11-153">So generieren Sie einen Aktivitätsprotokollbericht</span><span class="sxs-lookup"><span data-stu-id="3bb11-153">To generate an activity log report</span></span>**

1.  <span data-ttu-id="3bb11-154">Klicken Sie auf die Schaltfläche **Berichts** Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="3bb11-154">Click the **Reports** management button.</span></span>

    <span data-ttu-id="3bb11-155">Das Modul "Berichte" wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3bb11-155">The Reports module appears.</span></span>

2.  <span data-ttu-id="3bb11-156">Wählen Sie im Modul **Berichte** im Menü **Berichtstypen** die Option **Aktivitätsprotokoll**aus, und klicken Sie auf **generieren**.</span><span class="sxs-lookup"><span data-stu-id="3bb11-156">In the **Reports** module, on the **Report Types** menu, select **Activity Log**, and click **Generate**.</span></span>

3.  <span data-ttu-id="3bb11-157">Konfigurieren Sie im Dialogfeld **Berichtsparameter** einen oder mehrere der folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="3bb11-157">In the **Report Parameters** dialog box, configure one or more of the following parameters:</span></span>

    -   <span data-ttu-id="3bb11-158">**Anzahl der Tage**: die Anzahl der Tage, die im Bericht angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3bb11-158">**Number of days**—The number of days to display in the report.</span></span>

    -   <span data-ttu-id="3bb11-159">**Benutzername enthält**– jedes Ereignis, bei dem der Benutzername den eingegebenen Text enthält, wird im Bericht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="3bb11-159">**User name contains**—Any event where the user name contains the text entered is included in the report.</span></span>

    -   <span data-ttu-id="3bb11-160">**Hostname enthält**– jedes Ereignis, bei dem der Hostname den eingegebenen Text enthält, wird im Bericht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="3bb11-160">**Host name contains**—Any event where the host name contains the text entered is included in the report.</span></span>

4.  <span data-ttu-id="3bb11-161">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="3bb11-161">Click **OK**.</span></span>

    <span data-ttu-id="3bb11-162">Ein Bericht wird mit den ausgewählten Ereignissen und Datumsangaben erstellt.</span><span class="sxs-lookup"><span data-stu-id="3bb11-162">A report is generated with the events and dates selected.</span></span> <span data-ttu-id="3bb11-163">Die Berichtsparameter sind in der folgenden Tabelle definiert.</span><span class="sxs-lookup"><span data-stu-id="3bb11-163">The report parameters are defined in the following table.</span></span>

**<span data-ttu-id="3bb11-164">Eigenschaften des Aktivitätsprotokoll Berichts</span><span class="sxs-lookup"><span data-stu-id="3bb11-164">Activity Log Report Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3bb11-165">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3bb11-165">Property</span></span></th>
<th align="left"><span data-ttu-id="3bb11-166">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3bb11-166">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bb11-167">Ereignis-ID</span><span class="sxs-lookup"><span data-stu-id="3bb11-167">Event ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-168">Die Ereignis-ID.</span><span class="sxs-lookup"><span data-stu-id="3bb11-168">The event ID.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bb11-169">Schweregrad</span><span class="sxs-lookup"><span data-stu-id="3bb11-169">Severity</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="3bb11-170">Informationen, Fehler, Warnung</span><span class="sxs-lookup"><span data-stu-id="3bb11-170">Information, Error, Warning</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bb11-171">Kategorie</span><span class="sxs-lookup"><span data-stu-id="3bb11-171">Category</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-172">Das Modul, auf das der Bericht verweist.</span><span class="sxs-lookup"><span data-stu-id="3bb11-172">The module that the report is referring to.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bb11-173">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3bb11-173">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-174">Eine Beschreibung des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="3bb11-174">A description of the event.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bb11-175">Empfangene Zeit</span><span class="sxs-lookup"><span data-stu-id="3bb11-175">Time Received</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-176">Das Datum und die Uhrzeit, zu der das Ereignis auf dem Server empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="3bb11-176">The date and time the event was received on the server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3bb11-177">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3bb11-177">Note</span></span></strong><br/><p><span data-ttu-id="3bb11-178">Wenn der Client offline arbeitet, empfängt der Server die Berichte, wenn der Client online ist.</span><span class="sxs-lookup"><span data-stu-id="3bb11-178">If the client is working offline, the server receives the reports when the client is online.</span></span></p>
</div>
<div>

</div>
<div class="alert">
<strong><span data-ttu-id="3bb11-179">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3bb11-179">Note</span></span></strong><br/><p><span data-ttu-id="3bb11-180">Standardmäßig werden die Ereignisse in absteigender Datumsreihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3bb11-180">By default, the events are displayed in descending date order.</span></span> <span data-ttu-id="3bb11-181">Sie können jedoch durch Klicken auf die <strong> Spalte Zeit empfangen geändert werden </strong> .</span><span class="sxs-lookup"><span data-stu-id="3bb11-181">However, it can be changed by clicking the <strong>Time Received</strong> column.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bb11-182">Client Zeit</span><span class="sxs-lookup"><span data-stu-id="3bb11-182">Client Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-183">Das Datum und die Uhrzeit, zu der das Ereignis gemäß der Client Uhr aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="3bb11-183">The date and time the event occurred according to the client clock.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bb11-184">Hostname</span><span class="sxs-lookup"><span data-stu-id="3bb11-184">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-185">Der Name des Hostcomputers.</span><span class="sxs-lookup"><span data-stu-id="3bb11-185">The name of the host computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bb11-186">Benutzername</span><span class="sxs-lookup"><span data-stu-id="3bb11-186">User Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-187">Der Benutzer, der das Ereignis initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="3bb11-187">The user who initiated the event.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bb11-188">Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="3bb11-188">Workspace Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-189">Der Name des MED-V-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="3bb11-189">The name of the MED-V workspace.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bb11-190">Arbeitsbereichs Computer Name</span><span class="sxs-lookup"><span data-stu-id="3bb11-190">Workspace Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-191">Der Name des Computers, auf dem der MED-V-Arbeitsbereich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3bb11-191">The name of the computer the MED-V workspace is running on.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganerrorlogreport"></a><span data-ttu-id="3bb11-192">Erstellen eines Fehlerprotokoll Berichts</span><span class="sxs-lookup"><span data-stu-id="3bb11-192">How to Generate an Error Log Report</span></span>


**<span data-ttu-id="3bb11-193">So generieren Sie einen Fehlerprotokoll Bericht</span><span class="sxs-lookup"><span data-stu-id="3bb11-193">To generate an error log report</span></span>**

1.  <span data-ttu-id="3bb11-194">Klicken Sie auf die Schaltfläche **Berichts** Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="3bb11-194">Click the **Reports** management button.</span></span>

2.  <span data-ttu-id="3bb11-195">Wählen Sie im Modul **Berichte** im Menü **Berichtstypen** die Option **Fehlerprotokoll**aus, und klicken Sie auf **generieren**.</span><span class="sxs-lookup"><span data-stu-id="3bb11-195">In the **Reports** module, on the **Report Types** menu, select **Error Log**, and click **Generate**.</span></span>

3.  <span data-ttu-id="3bb11-196">Konfigurieren Sie im Dialogfeld **Berichtsparameter** einen oder mehrere der folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="3bb11-196">In the **Report Parameters** dialog box, configure one or more of the following parameters:</span></span>

    -   <span data-ttu-id="3bb11-197">**Anzahl der Tage**: die Anzahl der Tage, die im Bericht angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3bb11-197">**Number of days**—The number of days to display in the report.</span></span>

    -   <span data-ttu-id="3bb11-198">**Benutzername enthält**– jedes Ereignis, bei dem der Benutzername den eingegebenen Text enthält, wird im Bericht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="3bb11-198">**User name contains**—Any event where the user name contains the text entered is included in the report.</span></span>

    -   <span data-ttu-id="3bb11-199">**Hostname enthält**– jedes Ereignis, bei dem der Hostname den eingegebenen Text enthält, wird im Bericht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="3bb11-199">**Host name contains**—Any event where the host name contains the text entered is included in the report.</span></span>

4.  <span data-ttu-id="3bb11-200">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="3bb11-200">Click **OK**.</span></span>

    <span data-ttu-id="3bb11-201">Ein Bericht wird mit den ausgewählten Ereignissen und Datumsangaben erstellt.</span><span class="sxs-lookup"><span data-stu-id="3bb11-201">A report is generated with the events and dates selected.</span></span> <span data-ttu-id="3bb11-202">Die Berichtsparameter sind in der folgenden Tabelle definiert.</span><span class="sxs-lookup"><span data-stu-id="3bb11-202">The report parameters are defined in the following table.</span></span>

**<span data-ttu-id="3bb11-203">Fehlerprotokoll-Berichtseigenschaften</span><span class="sxs-lookup"><span data-stu-id="3bb11-203">Error Log Report Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3bb11-204">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3bb11-204">Property</span></span></th>
<th align="left"><span data-ttu-id="3bb11-205">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3bb11-205">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bb11-206">Ereignis-ID</span><span class="sxs-lookup"><span data-stu-id="3bb11-206">Event ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-207">Die Ereignis-ID.</span><span class="sxs-lookup"><span data-stu-id="3bb11-207">The event ID.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bb11-208">Kategorie</span><span class="sxs-lookup"><span data-stu-id="3bb11-208">Category</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-209">Das Modul, auf das der Bericht verweist.</span><span class="sxs-lookup"><span data-stu-id="3bb11-209">The module that the report is referring to.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bb11-210">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3bb11-210">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-211">Eine Beschreibung des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="3bb11-211">A description of the event.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bb11-212">Empfangene Zeit</span><span class="sxs-lookup"><span data-stu-id="3bb11-212">Time Received</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-213">Das Datum und die Uhrzeit, zu der das Ereignis auf dem Server empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="3bb11-213">The date and time the event was received on the server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3bb11-214">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3bb11-214">Note</span></span></strong><br/><p><span data-ttu-id="3bb11-215">Wenn der Client offline arbeitet, empfängt der Server die Berichte, wenn der Client online ist.</span><span class="sxs-lookup"><span data-stu-id="3bb11-215">If the client is working offline, the server receives the reports when the client is online.</span></span></p>
</div>
<div>

</div>
<div class="alert">
<strong><span data-ttu-id="3bb11-216">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3bb11-216">Note</span></span></strong><br/><p><span data-ttu-id="3bb11-217">Standardmäßig werden die Ereignisse in absteigender Datumsreihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3bb11-217">By default, the events are displayed in descending date order.</span></span> <span data-ttu-id="3bb11-218">Sie können jedoch durch Klicken auf die <strong> Spalte Zeit empfangen geändert werden </strong> .</span><span class="sxs-lookup"><span data-stu-id="3bb11-218">However, it can be changed by clicking the <strong>Time Received</strong> column.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bb11-219">Client Zeit</span><span class="sxs-lookup"><span data-stu-id="3bb11-219">Client Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-220">Das Datum und die Uhrzeit, zu der das Ereignis gemäß der Client Uhr aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="3bb11-220">The date and time the event occurred according to the client clock.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bb11-221">Hostname</span><span class="sxs-lookup"><span data-stu-id="3bb11-221">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-222">Der Name des Hostcomputers.</span><span class="sxs-lookup"><span data-stu-id="3bb11-222">The name of the host computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bb11-223">Benutzername</span><span class="sxs-lookup"><span data-stu-id="3bb11-223">User Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-224">Der Benutzer, der das Ereignis initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="3bb11-224">The user who initiated the event.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bb11-225">Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="3bb11-225">Workspace Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bb11-226">Der Name des MED-V-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="3bb11-226">The name of the MED-V workspace.</span></span></p></td>
</tr>
</tbody>
</table>











