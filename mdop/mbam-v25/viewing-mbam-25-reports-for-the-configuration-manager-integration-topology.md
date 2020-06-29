---
title: Anzeigen von MBAM 2.5-Berichten für die Configuration Manager-Integrationstopologie
description: Anzeigen von MBAM 2.5-Berichten für die Configuration Manager-Integrationstopologie
author: dansimp
ms.assetid: 60d11b2f-3a76-4023-8da4-f89e9f35b790
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3384fee62d302ac47775fe106265456ef119ab47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810318"
---
# <span data-ttu-id="9847e-103">Anzeigen von MBAM 2.5-Berichten für die Configuration Manager-Integrationstopologie</span><span class="sxs-lookup"><span data-stu-id="9847e-103">Viewing MBAM 2.5 Reports for the Configuration Manager Integration Topology</span></span>


<span data-ttu-id="9847e-104">In diesem Thema werden die Berichte beschrieben, die verfügbar sind, wenn Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mit der Configuration Manager-Integrations Topologie konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="9847e-104">This topic describes the reports that are available when you configure Microsoft BitLocker Administration and Monitoring (MBAM) with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="9847e-105">Die Berichte zeigen die BitLocker-Konformität für das Unternehmen und für einzelne Computer und Geräte an, die von MBAM verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="9847e-105">The reports show BitLocker compliance for the enterprise and for individual computers and devices that MBAM manages.</span></span> <span data-ttu-id="9847e-106">Die Berichte liefern tabellarische Informationen und Diagramme und verfügen über Filter, mit denen Sie Daten aus unterschiedlichen Perspektiven anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="9847e-106">The reports provide tabular information and charts, and they have filters that let you view data from different perspectives.</span></span>

<span data-ttu-id="9847e-107">In der Configuration Manager-Integrations Topologie können Sie Berichte aus Configuration Manager anstatt von der Websiteverwaltung und Überwachung anzeigen, mit Ausnahme des Berichts zur **Wiederherstellung**, den Sie auf der Websiteverwaltung und Überwachung weiterhin anzeigen.</span><span class="sxs-lookup"><span data-stu-id="9847e-107">In the Configuration Manager Integration topology, you view reports from Configuration Manager rather than from the Administration and Monitoring Website, with the exception of the **Recovery Audit Report**, which you continue to view from the Administration and Monitoring Website.</span></span>

<span data-ttu-id="9847e-108">Informationen zu MBAM-Berichten für die eigenständige Topologie finden Sie unter [Anzeigen von MBAM 2,5-Berichten für die eigenständige Topologie](viewing-mbam-25-reports-for-the-stand-alone-topology.md).</span><span class="sxs-lookup"><span data-stu-id="9847e-108">For information about MBAM reports for the Stand-alone topology, see [Viewing MBAM 2.5 Reports for the Stand-alone Topology](viewing-mbam-25-reports-for-the-stand-alone-topology.md).</span></span>

## <span data-ttu-id="9847e-109">Zugreifen auf Berichte in Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="9847e-109">Accessing reports in Configuration Manager</span></span>


<span data-ttu-id="9847e-110">So greifen Sie in Configuration Manager auf das Feature Berichte zu:</span><span class="sxs-lookup"><span data-stu-id="9847e-110">To access the Reports feature in Configuration Manager:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9847e-111">Version von Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="9847e-111">Version of Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="9847e-112">Anzeigen der Berichte</span><span class="sxs-lookup"><span data-stu-id="9847e-112">How to view the reports</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-113">SystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="9847e-113">SystemCenter2012 ConfigurationManager</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="9847e-114">Wählen Sie im linken Bereich den <strong> </strong> Arbeitsbereich Überwachung aus.</span><span class="sxs-lookup"><span data-stu-id="9847e-114">In the left pane, select the <strong>Monitoring</strong> workspace.</span></span></p></li>
<li><p><span data-ttu-id="9847e-115">Erweitern Sie in der Struktur <strong> Übersicht </strong> &gt; <strong> Bericht Erstellungs </strong> &gt; <strong> Berichte </strong> &gt; <strong> MBAM </strong> .</span><span class="sxs-lookup"><span data-stu-id="9847e-115">In the tree, expand <strong>Overview</strong> &gt; <strong>Reporting</strong> &gt; <strong>Reports</strong> &gt; <strong>MBAM</strong>.</span></span></p></li>
<li><p><span data-ttu-id="9847e-116">Wählen Sie den Ordner aus, der die Sprache darstellt, in der Sie Berichte anzeigen möchten, und wählen Sie dann im rechten Bereich den Bericht aus.</span><span class="sxs-lookup"><span data-stu-id="9847e-116">Select the folder that represents the language in which you want to view reports, and then select the report from the right pane.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-117">Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="9847e-117">Configuration Manager 2007</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="9847e-118">Erweitern Sie im linken Bereich <strong> Computer Management </strong> &gt; <strong> Reporting </strong> &gt; <strong> Reporting Services </strong> &gt; <strong> &lt; Servername &gt; </strong> &gt; <strong> Report Folders </strong> &gt; <strong> MBAM </strong> .</span><span class="sxs-lookup"><span data-stu-id="9847e-118">In the left pane, expand <strong>Computer Management</strong> &gt; <strong>Reporting</strong> &gt; <strong>Reporting Services</strong> &gt; <strong>&lt;server name&gt;</strong> &gt; <strong>Report folders</strong> &gt; <strong>MBAM</strong>.</span></span></p></li>
<li><p><span data-ttu-id="9847e-119">Wählen Sie den Ordner aus, der die Sprache darstellt, in der Sie Berichte anzeigen möchten, und wählen Sie dann im rechten Bereich den Bericht aus.</span><span class="sxs-lookup"><span data-stu-id="9847e-119">Select the folder that represents the language in which you want to view reports, and then select the report from the right pane.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="9847e-120">Beschreibung von Berichten in Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="9847e-120">Description of reports in Configuration Manager</span></span>


<span data-ttu-id="9847e-121">Es gibt einige geringfügige Unterschiede in den Berichten für die Configuration Manager-Integrations Topologie und die eigenständige Topologie.</span><span class="sxs-lookup"><span data-stu-id="9847e-121">There are a few minor differences in the reports for the Configuration Manager Integration topology and the Stand-alone topology.</span></span> <span data-ttu-id="9847e-122">In den folgenden Abschnitten werden die Daten in den MBAM-Berichten für die Configuration Manager-Integrations Topologie beschrieben:</span><span class="sxs-lookup"><span data-stu-id="9847e-122">The following sections describe the data in the MBAM reports for the Configuration Manager Integration topology:</span></span>

-   [<span data-ttu-id="9847e-123">BitLocker Enterprise Compliance-Dashboard</span><span class="sxs-lookup"><span data-stu-id="9847e-123">BitLocker Enterprise Compliance Dashboard</span></span>](#bkmk-dashboard)

-   [<span data-ttu-id="9847e-124">Details zur BitLocker-Unternehmenskonformität</span><span class="sxs-lookup"><span data-stu-id="9847e-124">BitLocker Enterprise Compliance Details</span></span>](#bkmk-compliancedetails)

-   [<span data-ttu-id="9847e-125">Zusammenfassung der BitLocker-Unternehmenskonformität</span><span class="sxs-lookup"><span data-stu-id="9847e-125">BitLocker Enterprise Compliance Summary</span></span>](#bkmk-compliancesummary)

-   [<span data-ttu-id="9847e-126">BitLocker-Computer Kompatibilitätsbericht</span><span class="sxs-lookup"><span data-stu-id="9847e-126">BitLocker Computer Compliance Report</span></span>](#bkmk-compliancereport)

### <a href="" id="bkmk-dashboard"></a><span data-ttu-id="9847e-127">BitLocker Enterprise Compliance-Dashboard</span><span class="sxs-lookup"><span data-stu-id="9847e-127">BitLocker Enterprise Compliance Dashboard</span></span>

<span data-ttu-id="9847e-128">Das BitLocker Enterprise Compliance-Dashboard bietet die folgenden Diagramme, die den BitLocker-Kompatibilitätsstatus im gesamten Unternehmen anzeigen:</span><span class="sxs-lookup"><span data-stu-id="9847e-128">The BitLocker Enterprise Compliance Dashboard provides the following graphs, which show BitLocker compliance status across the enterprise:</span></span>

-   <span data-ttu-id="9847e-129">Verteilung des Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="9847e-129">Compliance Status Distribution</span></span>

-   <span data-ttu-id="9847e-130">Verteilung nicht kompatibler Fehler</span><span class="sxs-lookup"><span data-stu-id="9847e-130">Non Compliant Errors Distribution</span></span>

-   <span data-ttu-id="9847e-131">Kompatibilitäts Status Verteilung nach Laufwerktyp</span><span class="sxs-lookup"><span data-stu-id="9847e-131">Compliance Status Distribution by Drive Type</span></span>

**<span data-ttu-id="9847e-132">Verteilung des Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="9847e-132">Compliance Status Distribution</span></span>**

<span data-ttu-id="9847e-133">Dieses Kreisdiagramm zeigt den Kompatibilitätsstatus für Computer innerhalb des Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="9847e-133">This pie chart shows compliance status for computers within the enterprise.</span></span> <span data-ttu-id="9847e-134">Darüber hinaus wird der Prozentsatz der Computer im Vergleich zur Gesamtzahl der Computer in der ausgewählten Sammlung angezeigt, die diesen Kompatibilitätsstatus aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9847e-134">It also shows the percentage of computers, compared to the total number of computers in the selected collection, that has that compliance status.</span></span> <span data-ttu-id="9847e-135">Die tatsächliche Anzahl der Computer mit jedem Status wird ebenfalls angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9847e-135">The actual number of computers with each status is also shown.</span></span> <span data-ttu-id="9847e-136">Das Kreisdiagramm zeigt die folgenden Konformitätsstatus:</span><span class="sxs-lookup"><span data-stu-id="9847e-136">The pie chart shows the following compliance statuses:</span></span>

-   <span data-ttu-id="9847e-137">Kompatibel</span><span class="sxs-lookup"><span data-stu-id="9847e-137">Compliant</span></span>

-   <span data-ttu-id="9847e-138">Nicht kompatibel</span><span class="sxs-lookup"><span data-stu-id="9847e-138">Non Compliant</span></span>

-   <span data-ttu-id="9847e-139">Benutzer freigestellt</span><span class="sxs-lookup"><span data-stu-id="9847e-139">User Exempt</span></span>

-   <span data-ttu-id="9847e-140">Temporärer Benutzer ausgenommen</span><span class="sxs-lookup"><span data-stu-id="9847e-140">Temporary User Exempt</span></span>

-   <span data-ttu-id="9847e-141">Richtlinie nicht erzwungen</span><span class="sxs-lookup"><span data-stu-id="9847e-141">Policy Not Enforced</span></span>

-   <span data-ttu-id="9847e-142">Unbekannten.</span><span class="sxs-lookup"><span data-stu-id="9847e-142">Unknown.</span></span> <span data-ttu-id="9847e-143">Diese Computer haben einen Status Fehler gemeldet, oder Sie sind Teil der Sammlung, haben aber ihren Kompatibilitätsstatus nie gemeldet.</span><span class="sxs-lookup"><span data-stu-id="9847e-143">These computers reported a status error, or they are part of the collection, but have never reported their compliance status.</span></span> <span data-ttu-id="9847e-144">Das Fehlen eines Kompatibilitätsstatus kann auftreten, wenn der Computer von der Organisation getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="9847e-144">The lack of a compliance status could occur if the computer is disconnected from the organization.</span></span>

**<span data-ttu-id="9847e-145">Verteilung nicht kompatibler Fehler</span><span class="sxs-lookup"><span data-stu-id="9847e-145">Non Compliant Errors Distribution</span></span>**

<span data-ttu-id="9847e-146">Dieses Kreisdiagramm zeigt die Kategorien von Computern im Unternehmen, die nicht mit der BitLocker-Laufwerk Verschlüsselungsrichtlinie kompatibel sind, und zeigt die Anzahl der Computer in jeder Kategorie an.</span><span class="sxs-lookup"><span data-stu-id="9847e-146">This pie chart shows the categories of computers in the enterprise that are not compliant with the BitLocker Drive Encryption policy, and shows the number of computers in each category.</span></span> <span data-ttu-id="9847e-147">Jeder Kategorie-Prozentsatz wird anhand der Gesamtzahl der nicht kompatiblen Computer in der Sammlung berechnet.</span><span class="sxs-lookup"><span data-stu-id="9847e-147">Each category percentage is calculated from the total number of non-compliant computers in the collection.</span></span>

-   <span data-ttu-id="9847e-148">Benutzer verzögerte Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="9847e-148">User postponed encryption</span></span>

-   <span data-ttu-id="9847e-149">Kompatibles TPM konnte nicht gefunden werden</span><span class="sxs-lookup"><span data-stu-id="9847e-149">Unable to find compatible TPM</span></span>

-   <span data-ttu-id="9847e-150">System Partition nicht verfügbar oder groß genug</span><span class="sxs-lookup"><span data-stu-id="9847e-150">System partition not available or large enough</span></span>

-   <span data-ttu-id="9847e-151">Richtlinienkonflikt</span><span class="sxs-lookup"><span data-stu-id="9847e-151">Policy conflict</span></span>

-   <span data-ttu-id="9847e-152">Warten auf die automatische TPM-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="9847e-152">Waiting for TPM auto provisioning</span></span>

-   <span data-ttu-id="9847e-153">Ein unbekannter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="9847e-153">An unknown error has occurred</span></span>

-   <span data-ttu-id="9847e-154">Keine Informationen.</span><span class="sxs-lookup"><span data-stu-id="9847e-154">No information.</span></span> <span data-ttu-id="9847e-155">Auf diesen Computern ist der MBAM-Client nicht installiert, oder der MBAM-Client ist installiert, aber nicht aktiviert (beispielsweise funktioniert der Dienst nicht).</span><span class="sxs-lookup"><span data-stu-id="9847e-155">These computers do not have the MBAM Client installed, or they have the MBAM Client installed but not activated (for example, the service is not working).</span></span>

**<span data-ttu-id="9847e-156">Kompatibilitäts Status Verteilung nach Laufwerktyp</span><span class="sxs-lookup"><span data-stu-id="9847e-156">Compliance Status Distribution by Drive Type</span></span>**

<span data-ttu-id="9847e-157">Dieses Balkendiagramm zeigt den aktuellen BitLocker-Konformitätsstatus nach Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="9847e-157">This bar chart shows the current BitLocker compliance status by drive type.</span></span> <span data-ttu-id="9847e-158">Die Status sind **kompatibel** und **nicht kompatibel**.</span><span class="sxs-lookup"><span data-stu-id="9847e-158">The statuses are **Compliant** and **Non Compliant**.</span></span> <span data-ttu-id="9847e-159">Für feste Datenlaufwerke und Betriebssystemlaufwerke werden Balken angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9847e-159">Bars are shown for fixed data drives and operating system drives.</span></span> <span data-ttu-id="9847e-160">Computer, die nicht über ein festes Datenlaufwerk verfügen, sind enthalten und zeigen nur einen Wert in der **Betriebs System-Laufwerk** Leiste an.</span><span class="sxs-lookup"><span data-stu-id="9847e-160">Computers that do not have a fixed data drive are included and show a value only in the **Operating System Drive** bar.</span></span> <span data-ttu-id="9847e-161">Das Diagramm enthält keine Benutzer, denen eine Ausnahme von der BitLocker-Laufwerk Verschlüsselungsrichtlinie oder der Kategorie "keine Richtlinie" gewährt wurde.</span><span class="sxs-lookup"><span data-stu-id="9847e-161">The chart does not include users who have been granted an exemption from the BitLocker Drive Encryption policy or the No Policy category.</span></span>

### <a href="" id="bkmk-compliancedetails"></a><span data-ttu-id="9847e-162">Details zur BitLocker-Unternehmenskonformität</span><span class="sxs-lookup"><span data-stu-id="9847e-162">BitLocker Enterprise Compliance Details</span></span>

<span data-ttu-id="9847e-163">Dieser Bericht enthält Informationen zur allgemeinen BitLocker-Compliance im gesamten Unternehmen für die Sammlung von Computern, die für die BitLocker-Verwendung vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="9847e-163">This report shows information about the overall BitLocker compliance across your enterprise for the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="9847e-164">BitLocker-Felder für Unternehmens Konformitäts Details</span><span class="sxs-lookup"><span data-stu-id="9847e-164">BitLocker Enterprise Compliance Details Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9847e-165">Spalten Name</span><span class="sxs-lookup"><span data-stu-id="9847e-165">Column Name</span></span></th>
<th align="left"><span data-ttu-id="9847e-166">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9847e-166">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-167">Verwaltete Computer</span><span class="sxs-lookup"><span data-stu-id="9847e-167">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-168">Die Anzahl der Computer, die von MBAM verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="9847e-168">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-169">%-Kompatibel</span><span class="sxs-lookup"><span data-stu-id="9847e-169">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-170">Prozentsatz der kompatiblen Computer im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="9847e-170">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-171">% Nicht kompatibel</span><span class="sxs-lookup"><span data-stu-id="9847e-171">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-172">Prozentsatz der nicht kompatiblen Computer im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="9847e-172">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-173">% Unknown Compliance</span><span class="sxs-lookup"><span data-stu-id="9847e-173">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-174">Prozentsatz der Computer mit einem Kompatibilitätsstatus, der unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="9847e-174">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-175">% Ausgenommen</span><span class="sxs-lookup"><span data-stu-id="9847e-175">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-176">Prozentsatz der Computer, die von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</span><span class="sxs-lookup"><span data-stu-id="9847e-176">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-177">% Nicht freigestellt</span><span class="sxs-lookup"><span data-stu-id="9847e-177">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-178">Prozentsatz der Computer, die nicht von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</span><span class="sxs-lookup"><span data-stu-id="9847e-178">Percentage of computers not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-179">Kompatibel</span><span class="sxs-lookup"><span data-stu-id="9847e-179">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-180">Prozentsatz der kompatiblen Computer im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="9847e-180">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-181">Nicht kompatibel</span><span class="sxs-lookup"><span data-stu-id="9847e-181">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-182">Prozentsatz der nicht kompatiblen Computer im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="9847e-182">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-183">Unbekannte Compliance</span><span class="sxs-lookup"><span data-stu-id="9847e-183">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-184">Prozentsatz der Computer mit einem Kompatibilitätsstatus, der unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="9847e-184">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-185">Befreit</span><span class="sxs-lookup"><span data-stu-id="9847e-185">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-186">Gesamtzahl der Computer, die von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</span><span class="sxs-lookup"><span data-stu-id="9847e-186">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-187">Nicht freigestellt</span><span class="sxs-lookup"><span data-stu-id="9847e-187">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-188">Gesamtzahl der Computer, die nicht von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</span><span class="sxs-lookup"><span data-stu-id="9847e-188">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="9847e-189">BitLocker Enterprise Compliance-Detailstatus</span><span class="sxs-lookup"><span data-stu-id="9847e-189">BitLocker Enterprise Compliance Details States</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9847e-190">Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="9847e-190">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="9847e-191">Befreiung</span><span class="sxs-lookup"><span data-stu-id="9847e-191">Exemption</span></span></th>
<th align="left"><span data-ttu-id="9847e-192">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9847e-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-193">Nicht kompatibler</span><span class="sxs-lookup"><span data-stu-id="9847e-193">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-194">Nicht ausgenommen</span><span class="sxs-lookup"><span data-stu-id="9847e-194">Not exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-195">Der Computer ist gemäß der angegebenen Richtlinie nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="9847e-195">The computer is noncompliant, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-196">Kompatibel</span><span class="sxs-lookup"><span data-stu-id="9847e-196">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-197">Nicht ausgenommen</span><span class="sxs-lookup"><span data-stu-id="9847e-197">Not exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-198">Der Computer ist gemäß der angegebenen Richtlinie kompatibel.</span><span class="sxs-lookup"><span data-stu-id="9847e-198">The computer is compliant in accordance with the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancesummary"></a><span data-ttu-id="9847e-199">Zusammenfassung der BitLocker-Unternehmenskonformität</span><span class="sxs-lookup"><span data-stu-id="9847e-199">BitLocker Enterprise Compliance Summary</span></span>

<span data-ttu-id="9847e-200">Verwenden Sie diesen Berichtstyp, um Informationen zur allgemeinen BitLocker-Konformität im gesamten Unternehmen anzuzeigen und die Kompatibilität einzelner Computer anzuzeigen, die sich in der Sammlung von Computern befinden, die für die BitLocker-Verwendung vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="9847e-200">Use this report type to show information about the overall BitLocker compliance across your enterprise and to show the compliance for individual computers that are in the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="9847e-201">Zusammenfassungsfelder für BitLocker-Unternehmenskonformität</span><span class="sxs-lookup"><span data-stu-id="9847e-201">BitLocker Enterprise Compliance Summary Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9847e-202">Spalten Name</span><span class="sxs-lookup"><span data-stu-id="9847e-202">Column Name</span></span></th>
<th align="left"><span data-ttu-id="9847e-203">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9847e-203">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-204">Verwaltete Computer</span><span class="sxs-lookup"><span data-stu-id="9847e-204">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-205">Die Anzahl der Computer, die von MBAM verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="9847e-205">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-206">%-Kompatibel</span><span class="sxs-lookup"><span data-stu-id="9847e-206">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-207">Prozentsatz der kompatiblen Computer im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="9847e-207">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-208">% Nicht kompatibel</span><span class="sxs-lookup"><span data-stu-id="9847e-208">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-209">Prozentsatz der nicht kompatiblen Computer im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="9847e-209">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-210">% Unknown Compliance</span><span class="sxs-lookup"><span data-stu-id="9847e-210">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-211">Prozentsatz der Computer mit einem Kompatibilitätsstatus, der unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="9847e-211">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-212">% Ausgenommen</span><span class="sxs-lookup"><span data-stu-id="9847e-212">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-213">Prozentsatz der Computer, die von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</span><span class="sxs-lookup"><span data-stu-id="9847e-213">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-214">% Nicht freigestellt</span><span class="sxs-lookup"><span data-stu-id="9847e-214">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-215">Prozentsatz der Computer, die nicht von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</span><span class="sxs-lookup"><span data-stu-id="9847e-215">Percentage of computers not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-216">Kompatibel</span><span class="sxs-lookup"><span data-stu-id="9847e-216">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-217">Prozentsatz der kompatiblen Computer im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="9847e-217">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-218">Nicht kompatibel</span><span class="sxs-lookup"><span data-stu-id="9847e-218">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-219">Prozentsatz der nicht kompatiblen Computer im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="9847e-219">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-220">Unbekannte Compliance</span><span class="sxs-lookup"><span data-stu-id="9847e-220">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-221">Prozentsatz der Computer mit einem Kompatibilitätsstatus, der unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="9847e-221">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-222">Befreit</span><span class="sxs-lookup"><span data-stu-id="9847e-222">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-223">Gesamtzahl der Computer, die von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</span><span class="sxs-lookup"><span data-stu-id="9847e-223">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-224">Nicht freigestellt</span><span class="sxs-lookup"><span data-stu-id="9847e-224">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-225">Gesamtzahl der Computer, die nicht von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</span><span class="sxs-lookup"><span data-stu-id="9847e-225">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="9847e-226">BitLocker-Zusammenfassungs Computer für Unternehmens Konformitäts Details</span><span class="sxs-lookup"><span data-stu-id="9847e-226">BitLocker Enterprise Compliance Summary Computer Details</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9847e-227">Spalten Name</span><span class="sxs-lookup"><span data-stu-id="9847e-227">Column Name</span></span></th>
<th align="left"><span data-ttu-id="9847e-228">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9847e-228">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-229">Computer Name</span><span class="sxs-lookup"><span data-stu-id="9847e-229">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-230">Vom Benutzer festgelegter DNS-Computername, der von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="9847e-230">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-231">Domänen Name</span><span class="sxs-lookup"><span data-stu-id="9847e-231">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-232">Vollständig qualifizierter Domänenname, in dem sich der Clientcomputer befindet und von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="9847e-232">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-233">Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="9847e-233">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-234">Gesamt Kompatibilitätsstatus des Computers, der von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="9847e-234">Overall compliance status of the computer managed by MBAM.</span></span> <span data-ttu-id="9847e-235">Gültige Zustände sind kompatibel und nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="9847e-235">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="9847e-236">Beachten Sie, dass der Kompatibilitätsstatus pro Laufwerk (siehe die folgende Tabelle) möglicherweise auf unterschiedliche Konformitäts Zustände hindeutet.</span><span class="sxs-lookup"><span data-stu-id="9847e-236">Notice that the compliance status per drive (see the table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="9847e-237">Dieses Feld stellt jedoch diesen Konformitätsstatus gemäß der angegebenen Richtlinie dar.</span><span class="sxs-lookup"><span data-stu-id="9847e-237">However, this field represents that compliance state, in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-238">Befreiung</span><span class="sxs-lookup"><span data-stu-id="9847e-238">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-239">Status, der angibt, ob der Benutzer von der BitLocker-Richtlinie ausgenommen oder nicht freigestellt ist.</span><span class="sxs-lookup"><span data-stu-id="9847e-239">Status that indicates whether the user is exempt or non-exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-240">Geräte Benutzer</span><span class="sxs-lookup"><span data-stu-id="9847e-240">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-241">Benutzer des Geräts.</span><span class="sxs-lookup"><span data-stu-id="9847e-241">User of the device.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-242">Details zum Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="9847e-242">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-243">Fehler-und Statusmeldungen bezüglich des Kompatibilitätszustands des Computers in Übereinstimmung mit der angegebenen Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="9847e-243">Error and status messages about the compliance state of the computer in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-244">Letzter Kontakt</span><span class="sxs-lookup"><span data-stu-id="9847e-244">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-245">Datum und Uhrzeit des letzten Kontakts des Computers mit dem Server, um den Kompatibilitätsstatus zu melden.</span><span class="sxs-lookup"><span data-stu-id="9847e-245">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="9847e-246">Die Kontakthäufigkeit kann über die Gruppenrichtlinieneinstellungen konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="9847e-246">The contact frequency is configurable through the Group Policy settings.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancereport"></a><span data-ttu-id="9847e-247">BitLocker-Computer Kompatibilitätsbericht</span><span class="sxs-lookup"><span data-stu-id="9847e-247">BitLocker Computer Compliance Report</span></span>

<span data-ttu-id="9847e-248">Verwenden Sie diesen Berichtstyp, um Informationen zu sammeln, die für einen Computer spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="9847e-248">Use this report type to collect information that is specific to a computer.</span></span> <span data-ttu-id="9847e-249">Der BitLocker-Computer Kompatibilitätsbericht enthält detaillierte Verschlüsselungsinformationen zu jedem Laufwerk auf einem Computer (Betriebssystem und fest Netzlaufwerke).</span><span class="sxs-lookup"><span data-stu-id="9847e-249">The BitLocker Computer Compliance Report provides detailed encryption information about each drive on a computer (operating system and fixed data drives).</span></span> <span data-ttu-id="9847e-250">Darüber hinaus gibt es einen Hinweis auf die Richtlinie, die auf die einzelnen Laufwerktypen auf dem Computer angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9847e-250">It also provides an indication of the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="9847e-251">Um die Details der einzelnen Laufwerke anzuzeigen, erweitern Sie den Eintrag Computer Name.</span><span class="sxs-lookup"><span data-stu-id="9847e-251">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="9847e-252">**Hinweis**  Der Verschlüsselungsstatus für Wechseldatenträger wird in diesem Bericht nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9847e-252">**Note** The Removable Data Volume encryption status is not shown in this report.</span></span>

 

**<span data-ttu-id="9847e-253">BitLocker-Computer Kompatibilitätsbericht: Felder für Computer Details</span><span class="sxs-lookup"><span data-stu-id="9847e-253">BitLocker Computer Compliance Report: Computer Details Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9847e-254">Spalten Name</span><span class="sxs-lookup"><span data-stu-id="9847e-254">Column Name</span></span></th>
<th align="left"><span data-ttu-id="9847e-255">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9847e-255">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-256">Computer Name</span><span class="sxs-lookup"><span data-stu-id="9847e-256">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-257">Vom Benutzer festgelegter DNS-Computername, der von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="9847e-257">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-258">Domänen Name</span><span class="sxs-lookup"><span data-stu-id="9847e-258">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-259">Vollständig qualifizierter Domänenname, in dem sich der Clientcomputer befindet und von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="9847e-259">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-260">Computertyp</span><span class="sxs-lookup"><span data-stu-id="9847e-260">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-261">Der Typ des Computers.</span><span class="sxs-lookup"><span data-stu-id="9847e-261">Type of computer.</span></span> <span data-ttu-id="9847e-262">Gültige Typen sind nicht portabel und portabel.</span><span class="sxs-lookup"><span data-stu-id="9847e-262">Valid types are Non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-263">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="9847e-263">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-264">Der Typ des Betriebssystems, der auf dem verwalteten MBAM-Clientcomputer gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="9847e-264">Operating System type found on the MBAM managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-265">Allgemeine Compliance</span><span class="sxs-lookup"><span data-stu-id="9847e-265">Overall Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-266">Gesamt Kompatibilitätsstatus des Computers, der von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="9847e-266">Overall compliance status of the computer managed by MBAM.</span></span> <span data-ttu-id="9847e-267">Gültige Zustände sind kompatibel und nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="9847e-267">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="9847e-268">Beachten Sie, dass der Kompatibilitätsstatus pro Laufwerk (siehe die folgende Tabelle) möglicherweise auf unterschiedliche Konformitäts Zustände hindeutet.</span><span class="sxs-lookup"><span data-stu-id="9847e-268">Notice that the compliance status per drive (see the table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="9847e-269">Dieses Feld steht jedoch für diesen Kompatibilitätszustand in Übereinstimmung mit der angegebenen Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="9847e-269">However, this field represents that compliance state in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-270">Kompatibilität des Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="9847e-270">Operating System Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-271">Kompatibilitätsstatus des Betriebssystems, das von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="9847e-271">Compliance status of the operating system that is managed by MBAM.</span></span> <span data-ttu-id="9847e-272">Gültige Zustände sind kompatibel und nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="9847e-272">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-273">Festgelegte Datenlaufwerks Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="9847e-273">Fixed Data Drive Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-274">Kompatibilitätsstatus des festen Datenlaufwerks, das von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="9847e-274">Compliance status of the fixed data drive that is managed by MBAM.</span></span> <span data-ttu-id="9847e-275">Gültige Zustände sind kompatibel und nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="9847e-275">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-276">Datum der letzten Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="9847e-276">Last Update Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-277">Datum und Uhrzeit des letzten Kontakts des Computers mit dem Server, um den Kompatibilitätsstatus zu melden.</span><span class="sxs-lookup"><span data-stu-id="9847e-277">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="9847e-278">Die Kontakthäufigkeit kann über die Gruppenrichtlinieneinstellungen konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="9847e-278">The contact frequency is configurable through the Group Policy settings.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-279">Befreiung</span><span class="sxs-lookup"><span data-stu-id="9847e-279">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-280">Status, der angibt, ob der Benutzer von der BitLocker-Richtlinie ausgenommen oder nicht freigestellt ist.</span><span class="sxs-lookup"><span data-stu-id="9847e-280">Status that indicates whether the user is exempt or non-exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-281">Befreite Benutzer</span><span class="sxs-lookup"><span data-stu-id="9847e-281">Exempted User</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-282">Der Benutzer, der von der BitLocker-Richtlinie ausgenommen ist.</span><span class="sxs-lookup"><span data-stu-id="9847e-282">User who is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-283">Befreiungs Datum</span><span class="sxs-lookup"><span data-stu-id="9847e-283">Exemption Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-284">Das Datum, an dem die Befreiung gewährt wurde.</span><span class="sxs-lookup"><span data-stu-id="9847e-284">Date on which the exemption was granted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-285">Details zum Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="9847e-285">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-286">Fehler-und Statusmeldungen bezüglich des Kompatibilitätszustands des Computers in Übereinstimmung mit der angegebenen Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="9847e-286">Error and status messages about the compliance state of the computer in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-287">Richtlinien Verschlüsselungsstärke</span><span class="sxs-lookup"><span data-stu-id="9847e-287">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-288">Die vom Administrator während der MBAM-Richtlinien Spezifikation ausgewählte Verschlüsselungsstärke (beispielsweise 128-Bit mit Diffusor).</span><span class="sxs-lookup"><span data-stu-id="9847e-288">Cipher strength selected by the Administrator during the MBAM policy specification (for example, 128-bit with diffuser).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-289">Richtlinie: Betriebs System Laufwerk</span><span class="sxs-lookup"><span data-stu-id="9847e-289">Policy: Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-290">Gibt an, ob für das Betriebssystem und den entsprechenden Protector-Typ eine Verschlüsselung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9847e-290">Indicates if encryption is required for the operating system and the appropriate protector type.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-291">Richtlinie: Festes Datenlaufwerk</span><span class="sxs-lookup"><span data-stu-id="9847e-291">Policy: Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-292">Gibt an, ob für das festgelegte Datenlaufwerk eine Verschlüsselung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9847e-292">Indicates if encryption is required for the fixed data drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-293">Hersteller</span><span class="sxs-lookup"><span data-stu-id="9847e-293">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-294">Name des Computerherstellers, wie er im Computer-BIOS angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9847e-294">Computer manufacturer name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-295">Modell</span><span class="sxs-lookup"><span data-stu-id="9847e-295">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-296">Name des Computerhersteller-Modells, wie er im Computer-BIOS angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9847e-296">Computer manufacturer model name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-297">Geräte Benutzer</span><span class="sxs-lookup"><span data-stu-id="9847e-297">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-298">Bekannte Benutzer auf dem Computer, der von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="9847e-298">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="9847e-299">BitLocker-Computer Kompatibilitätsbericht: Computer Volumen Felder</span><span class="sxs-lookup"><span data-stu-id="9847e-299">BitLocker Computer Compliance Report: Computer Volume Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9847e-300">Spalten Name</span><span class="sxs-lookup"><span data-stu-id="9847e-300">Column Name</span></span></th>
<th align="left"><span data-ttu-id="9847e-301">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9847e-301">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-302">Laufwerkbuchstabe</span><span class="sxs-lookup"><span data-stu-id="9847e-302">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-303">Computer Laufwerkbuchstabe, der dem jeweiligen Laufwerk vom Benutzer zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="9847e-303">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-304">Laufwerktyp</span><span class="sxs-lookup"><span data-stu-id="9847e-304">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-305">Der Typ des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="9847e-305">Type of drive.</span></span> <span data-ttu-id="9847e-306">Gültige Werte sind Betriebs System Laufwerk und festes Datenlaufwerk.</span><span class="sxs-lookup"><span data-stu-id="9847e-306">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="9847e-307">Hierbei handelt es sich um physikalische Laufwerke anstatt um logische Volumes.</span><span class="sxs-lookup"><span data-stu-id="9847e-307">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-308">Verschlüsselungsstärke</span><span class="sxs-lookup"><span data-stu-id="9847e-308">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-309">Die vom Administrator während der MBAM-Richtlinien Spezifikation ausgewählte Verschlüsselungsstärke.</span><span class="sxs-lookup"><span data-stu-id="9847e-309">Cipher strength selected by the Administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-310">Schutztypen</span><span class="sxs-lookup"><span data-stu-id="9847e-310">Protector Types</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-311">Der Typ des Beschützers, der über die Richtlinie zum Verschlüsseln eines Betriebssystems oder eines festen Datenlaufwerks ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="9847e-311">Type of protector selected through the policy used to encrypt an operating system or fixed data drive.</span></span> <span data-ttu-id="9847e-312">Die gültigen Schutztypen für ein Betriebssystem sind TPM oder TPM + PIN.</span><span class="sxs-lookup"><span data-stu-id="9847e-312">The valid protector types for an operating system are TPM or TPM+PIN.</span></span> <span data-ttu-id="9847e-313">Der gültige Protector-Typ für ein festes Datenlaufwerk ist ein Kennwort.</span><span class="sxs-lookup"><span data-stu-id="9847e-313">The valid protector type for a fixed data drive is a password.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9847e-314">Protector-Status</span><span class="sxs-lookup"><span data-stu-id="9847e-314">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-315">Gibt an, dass der Computer, der von MBAM verwaltet wird, den in der Richtlinie angegebenen Protector-Typ aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="9847e-315">Indicates that the computer being managed by MBAM has enabled the protector type specified in the policy.</span></span> <span data-ttu-id="9847e-316">Die gültigen Zustände sind ein-oder ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="9847e-316">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9847e-317">Verschlüsselungsstatus</span><span class="sxs-lookup"><span data-stu-id="9847e-317">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="9847e-318">Verschlüsselungsstatus des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="9847e-318">Encryption state of the drive.</span></span> <span data-ttu-id="9847e-319">Gültige Zustände sind verschlüsselt, nicht verschlüsselt und verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="9847e-319">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="9847e-320">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9847e-320">Related topics</span></span>


[<span data-ttu-id="9847e-321">BitLocker-Kompatibilitätsüberwachung und -berichterstellung mit MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="9847e-321">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

 

## <span data-ttu-id="9847e-322">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="9847e-322">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="9847e-323">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="9847e-323">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="9847e-324">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="9847e-324">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





