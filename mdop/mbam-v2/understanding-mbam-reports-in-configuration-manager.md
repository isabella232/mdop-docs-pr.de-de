---
title: Grundlegende Informationen zu MBAM Berichten im Konfigurations-Manager
description: Grundlegende Informationen zu MBAM Berichten im Konfigurations-Manager
author: dansimp
ms.assetid: b2582190-c9de-4e64-bd5a-f31ac1916f53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 995d628cafd03c8bdd209e467c9d22169b7e03c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810186"
---
# <span data-ttu-id="2ef1e-103">Grundlegende Informationen zu MBAM Berichten im Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="2ef1e-103">Understanding MBAM Reports in Configuration Manager</span></span>


<span data-ttu-id="2ef1e-104">Wenn die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mit der integrierten Configuration Manager-Topologie installiert wird, werden die Hardware Kompatibilitäts-und Berichterstattungsfeatures in die Configuration Manager-Infrastruktur und aus MBAM verschoben.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-104">When Microsoft BitLocker Administration and Monitoring (MBAM) is installed with the Configuration Manager Integrated topology, the hardware compliance and reporting features are moved into the Configuration Manager infrastructure and out of MBAM.</span></span> <span data-ttu-id="2ef1e-105">Wenn Sie die Configuration Manager-Topologie verwenden, führen Sie Berichte von Configuration Manager anstatt von MBAM aus, mit Ausnahme des Wiederherstellungs Überwachungsberichts, auf den Sie weiterhin mithilfe der Website Verwaltung und Überwachung zugreifen.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-105">When you use the Configuration Manager topology, you run reports from Configuration Manager rather than from MBAM, except for the Recovery Audit Report, which you continue to access by using the Administration and Monitoring Website.</span></span>

<span data-ttu-id="2ef1e-106">Die Berichte für die integrierte Configuration Manager-Topologie zeigen die BitLocker-Kompatibilität für das Unternehmen und für einzelne Computer und Geräte an, die von MBAM verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-106">The reports for the Configuration Manager Integrated topology show BitLocker compliance for the enterprise and for individual computers and devices that MBAM manages.</span></span> <span data-ttu-id="2ef1e-107">In den Berichten werden sowohl tabellarische Informationen als auch Diagramme bereitgestellt, und Sie können Berichte filtern, um Daten aus unterschiedlichen Perspektiven anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-107">The reports provide both tabular information and charts, and enable you to filter reports to view data from different perspectives.</span></span>

<span data-ttu-id="2ef1e-108">Die Informationen in diesem Thema beschreiben die MBAM-Berichte, die Sie über Configuration Manager ausführen.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-108">The information in this topic describes the MBAM reports that you run from Configuration Manager.</span></span> <span data-ttu-id="2ef1e-109">Informationen zu MBAM-Berichten für die eigenständige Topologie finden Sie unter [Grundlegendes zu MBAM-Berichten](understanding-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="2ef1e-109">For information about MBAM reports for the Stand-alone topology, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span></span>

## <span data-ttu-id="2ef1e-110">Zugreifen auf Berichte in Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="2ef1e-110">Accessing Reports in Configuration Manager</span></span>


<span data-ttu-id="2ef1e-111">Um in Configuration Manager auf das Feature Berichte zuzugreifen, öffnen Sie die **Configuration Manager-Konsole**.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-111">To access the Reports feature in Configuration Manager, open the **Configuration Manager console**.</span></span> <span data-ttu-id="2ef1e-112">So zeigen Sie die Liste der verfügbaren Berichte an:</span><span class="sxs-lookup"><span data-stu-id="2ef1e-112">To display the list of available reports:</span></span>

-   <span data-ttu-id="2ef1e-113">Erweitern Sie in Configuration Manager 2007 den Knoten **Computer Verwaltung** , und erweitern Sie dann den Knoten **Berichterstellung** .</span><span class="sxs-lookup"><span data-stu-id="2ef1e-113">In Configuration Manager 2007, expand the **Computer Management** node, and then expand the **Reporting** node.</span></span>

-   <span data-ttu-id="2ef1e-114">Erweitern Sie in SystemCenter2012 ConfigurationManager im Bereich Überwachung unter **Übersicht**den Knoten **Berichterstattung** , und klicken Sie dann auf **Berichte**.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-114">In SystemCenter2012 ConfigurationManager, in the Monitoring workspace under **Overview**, expand the **Reporting** node and then click **Reports**.</span></span>

### <span data-ttu-id="2ef1e-115">BitLocker Enterprise Compliance-Dashboard</span><span class="sxs-lookup"><span data-stu-id="2ef1e-115">BitLocker Enterprise Compliance Dashboard</span></span>

<span data-ttu-id="2ef1e-116">Das BitLocker Enterprise Compliance-Dashboard bietet die folgenden Diagramme, die den BitLocker-Kompatibilitätsstatus im gesamten Unternehmen anzeigen:</span><span class="sxs-lookup"><span data-stu-id="2ef1e-116">The BitLocker Enterprise Compliance Dashboard provides the following graphs, which show BitLocker compliance status across the enterprise:</span></span>

-   <span data-ttu-id="2ef1e-117">Verteilung des Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="2ef1e-117">Compliance Status Distribution</span></span>

-   <span data-ttu-id="2ef1e-118">Verteilung nicht kompatibler Fehler</span><span class="sxs-lookup"><span data-stu-id="2ef1e-118">Non Compliant Errors Distribution</span></span>

-   <span data-ttu-id="2ef1e-119">Kompatibilitäts Status Verteilung nach Laufwerktyp</span><span class="sxs-lookup"><span data-stu-id="2ef1e-119">Compliance Status Distribution by Drive Type</span></span>

**<span data-ttu-id="2ef1e-120">Verteilung des Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="2ef1e-120">Compliance Status Distribution</span></span>**

<span data-ttu-id="2ef1e-121">Dieses Kreisdiagramm zeigt den Computer Kompatibilitätsstatus innerhalb des Unternehmens an und zeigt den Prozentsatz der Computer im Vergleich zur Gesamtzahl der Computer in der ausgewählten Sammlung an, die diesen Kompatibilitätsstatus aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-121">This pie chart shows computer compliance statuses within the enterprise, and shows the percentage of computers, compared to the total number of computers in the selected collection, that have that compliance status.</span></span> <span data-ttu-id="2ef1e-122">Die tatsächliche Anzahl der Computer mit jedem Status wird ebenfalls angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-122">The actual number of computers with each status is also shown.</span></span> <span data-ttu-id="2ef1e-123">Das Kreisdiagramm zeigt die folgenden Konformitätsstatus:</span><span class="sxs-lookup"><span data-stu-id="2ef1e-123">The pie chart shows the following compliance statuses:</span></span>

-   <span data-ttu-id="2ef1e-124">Kompatibel</span><span class="sxs-lookup"><span data-stu-id="2ef1e-124">Compliant</span></span>

-   <span data-ttu-id="2ef1e-125">Nicht kompatibel</span><span class="sxs-lookup"><span data-stu-id="2ef1e-125">Non Compliant</span></span>

-   <span data-ttu-id="2ef1e-126">Benutzer freigestellt</span><span class="sxs-lookup"><span data-stu-id="2ef1e-126">User Exempt</span></span>

-   <span data-ttu-id="2ef1e-127">Temporärer Benutzer ausgenommen</span><span class="sxs-lookup"><span data-stu-id="2ef1e-127">Temporary User Exempt</span></span>

-   <span data-ttu-id="2ef1e-128">Richtlinie nicht erzwungen</span><span class="sxs-lookup"><span data-stu-id="2ef1e-128">Policy Not Enforced</span></span>

-   <span data-ttu-id="2ef1e-129">Unbekannt – Computer, deren Status als Fehler gemeldet wurde, oder Geräte, die Teil der Sammlung sind, aber ihren Kompatibilitätsstatus nie gemeldet haben, beispielsweise, wenn Sie von der Organisation getrennt wurden</span><span class="sxs-lookup"><span data-stu-id="2ef1e-129">Unknown -computers whose status was reported as an error, or devices that are part of the collection but have never reported their compliance status, for example, if they are disconnected from the organization</span></span>

**<span data-ttu-id="2ef1e-130">Verteilung nicht kompatibler Fehler</span><span class="sxs-lookup"><span data-stu-id="2ef1e-130">Non Compliant Errors Distribution</span></span>**

<span data-ttu-id="2ef1e-131">Dieses Kreisdiagramm zeigt die Kategorien von Computern im Unternehmen, die nicht mit der BitLocker-Laufwerk Verschlüsselungsrichtlinie kompatibel sind, und zeigt die Anzahl der Computer in jeder Kategorie an.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-131">This pie chart shows the categories of computers in the enterprise that are not compliant with the BitLocker drive encryption policy, and shows the number of computers in each category.</span></span> <span data-ttu-id="2ef1e-132">Jeder Kategorie-Prozentsatz wird anhand der Gesamtzahl der nicht kompatiblen Computer in der Sammlung berechnet.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-132">Each category percentage is calculated from the total number of non-compliant computers in the collection.</span></span>

-   <span data-ttu-id="2ef1e-133">Benutzer verzögerte Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="2ef1e-133">User postponed encryption</span></span>

-   <span data-ttu-id="2ef1e-134">Kompatibles TPM konnte nicht gefunden werden</span><span class="sxs-lookup"><span data-stu-id="2ef1e-134">Unable to find compatible TPM</span></span>

-   <span data-ttu-id="2ef1e-135">System Partition nicht verfügbar oder groß genug</span><span class="sxs-lookup"><span data-stu-id="2ef1e-135">System Partition not available or large enough</span></span>

-   <span data-ttu-id="2ef1e-136">Richtlinienkonflikt</span><span class="sxs-lookup"><span data-stu-id="2ef1e-136">Policy conflict</span></span>

-   <span data-ttu-id="2ef1e-137">Warten auf die automatische TPM-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="2ef1e-137">Waiting for TPM auto provisioning</span></span>

-   <span data-ttu-id="2ef1e-138">Ein unbekannter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-138">An unknown error has occurred</span></span>

-   <span data-ttu-id="2ef1e-139">Keine Informationen – Computer, auf denen der MBAM-Client nicht installiert ist, oder die den MBAM-Client installiert, aber nicht aktiviert haben, beispielsweise funktioniert der Dienst nicht</span><span class="sxs-lookup"><span data-stu-id="2ef1e-139">No information – computers that do not have the MBAM Client installed, or that have the MBAM Client installed but not activated, for example, the service is not working</span></span>

**<span data-ttu-id="2ef1e-140">Kompatibilitäts Status Verteilung nach Laufwerktyp</span><span class="sxs-lookup"><span data-stu-id="2ef1e-140">Compliance Status Distribution by Drive Type</span></span>**

<span data-ttu-id="2ef1e-141">Dieses Balkendiagramm zeigt den aktuellen BitLocker-Konformitätsstatus nach Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-141">This bar chart shows the current BitLocker compliance status by drive type.</span></span> <span data-ttu-id="2ef1e-142">Die Status sind "kompatibel" und "nicht kompatibel".</span><span class="sxs-lookup"><span data-stu-id="2ef1e-142">The statuses are “Compliant” and “Non Compliant.”</span></span> <span data-ttu-id="2ef1e-143">Für feste Datenlaufwerke und Betriebssystemlaufwerke werden Balken angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-143">Bars are shown for fixed data drives and operating system drives.</span></span> <span data-ttu-id="2ef1e-144">Computer, die nicht über ein festes Datenlaufwerk verfügen, sind enthalten und zeigen nur einen Wert in der Betriebs System-Laufwerkleiste an.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-144">Computers that do not have a fixed data drive are included and show a value only in the Operating System Drive bar.</span></span> <span data-ttu-id="2ef1e-145">Das Diagramm enthält keine Benutzer, denen eine Ausnahme von der BitLocker-Laufwerk Verschlüsselungsrichtlinie oder der Kategorie "keine Richtlinie" gewährt wurde.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-145">The chart does not include users who have been granted an exemption from the BitLocker drive encryption policy or the “No Policy” category.</span></span>

### <span data-ttu-id="2ef1e-146">BitLocker Enterprise Compliance-Detailbericht</span><span class="sxs-lookup"><span data-stu-id="2ef1e-146">BitLocker Enterprise Compliance Details Report</span></span>

<span data-ttu-id="2ef1e-147">Dieser Bericht enthält Informationen zur allgemeinen BitLocker-Compliance im gesamten Unternehmen für die Sammlung von Computern, die für die BitLocker-Verwendung vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-147">This report shows information about the overall BitLocker compliance across your enterprise for the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="2ef1e-148">BitLocker-Berichtsfelder für Unternehmens Konformitäts Details</span><span class="sxs-lookup"><span data-stu-id="2ef1e-148">BitLocker Enterprise Compliance Details Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ef1e-149">Spalten Name</span><span class="sxs-lookup"><span data-stu-id="2ef1e-149">Column Name</span></span></th>
<th align="left"><span data-ttu-id="2ef1e-150">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ef1e-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-151">Verwaltete Computer</span><span class="sxs-lookup"><span data-stu-id="2ef1e-151">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-152">Die Anzahl der Computer, die von MBAM verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-152">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-153">%-Kompatibel</span><span class="sxs-lookup"><span data-stu-id="2ef1e-153">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-154">Prozentsatz der kompatiblen Computer im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-154">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-155">% Nicht kompatibel</span><span class="sxs-lookup"><span data-stu-id="2ef1e-155">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-156">Prozentsatz der nicht kompatiblen Computer im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-156">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-157">% Unknown Compliance</span><span class="sxs-lookup"><span data-stu-id="2ef1e-157">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-158">Prozentsatz der Computer, deren Konformitätsstatus unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-158">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-159">% Ausgenommen</span><span class="sxs-lookup"><span data-stu-id="2ef1e-159">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-160">Prozentsatz der Computer, die von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-160">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-161">% Nicht freigestellt</span><span class="sxs-lookup"><span data-stu-id="2ef1e-161">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-162">Prozentsatz der Computer, die von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-162">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-163">Kompatibel</span><span class="sxs-lookup"><span data-stu-id="2ef1e-163">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-164">Prozentsatz der kompatiblen Computer im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-164">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-165">Nicht kompatibel</span><span class="sxs-lookup"><span data-stu-id="2ef1e-165">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-166">Prozentsatz der nicht kompatiblen Computer im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-166">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-167">Unbekannte Compliance</span><span class="sxs-lookup"><span data-stu-id="2ef1e-167">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-168">Prozentsatz der Computer, deren Konformitätsstatus unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-168">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-169">Befreit</span><span class="sxs-lookup"><span data-stu-id="2ef1e-169">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-170">Gesamtzahl der Computer, die von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-170">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-171">Nicht freigestellt</span><span class="sxs-lookup"><span data-stu-id="2ef1e-171">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-172">Gesamtzahl der Computer, die nicht von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-172">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="2ef1e-173">BitLocker Enterprise Compliance Details-Bericht – Konformitätsstatus</span><span class="sxs-lookup"><span data-stu-id="2ef1e-173">BitLocker Enterprise Compliance Details Report - Compliance States</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ef1e-174">Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="2ef1e-174">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="2ef1e-175">Befreiung</span><span class="sxs-lookup"><span data-stu-id="2ef1e-175">Exemption</span></span></th>
<th align="left"><span data-ttu-id="2ef1e-176">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ef1e-176">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-177">Nicht kompatibler</span><span class="sxs-lookup"><span data-stu-id="2ef1e-177">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-178">Nicht ausgenommen</span><span class="sxs-lookup"><span data-stu-id="2ef1e-178">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-179">Der Computer ist gemäß der angegebenen Richtlinie nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-179">The computer is noncompliant, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-180">Kompatibel</span><span class="sxs-lookup"><span data-stu-id="2ef1e-180">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-181">Nicht ausgenommen</span><span class="sxs-lookup"><span data-stu-id="2ef1e-181">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-182">Der Computer ist gemäß der angegebenen Richtlinie kompatibel.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-182">The computer is compliant in accordance with the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="2ef1e-183">BitLocker Enterprise Compliance-Zusammenfassungsbericht</span><span class="sxs-lookup"><span data-stu-id="2ef1e-183">BitLocker Enterprise Compliance Summary Report</span></span>

<span data-ttu-id="2ef1e-184">Verwenden Sie diesen Berichtstyp, um Informationen zur allgemeinen BitLocker-Konformität im gesamten Unternehmen anzuzeigen und die Kompatibilität einzelner Computer anzuzeigen, die sich in der Sammlung von Computern befinden, die für die BitLocker-Verwendung vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-184">Use this report type to show information about the overall BitLocker compliance across your enterprise and to show the compliance for individual computers that are in the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="2ef1e-185">BitLocker Enterprise Compliance-Zusammenfassungsbericht (Felder)</span><span class="sxs-lookup"><span data-stu-id="2ef1e-185">BitLocker Enterprise Compliance Summary Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ef1e-186">Spalten Name</span><span class="sxs-lookup"><span data-stu-id="2ef1e-186">Column Name</span></span></th>
<th align="left"><span data-ttu-id="2ef1e-187">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ef1e-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-188">Verwaltete Computer</span><span class="sxs-lookup"><span data-stu-id="2ef1e-188">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-189">Die Anzahl der Computer, die von MBAM verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-189">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-190">%-Kompatibel</span><span class="sxs-lookup"><span data-stu-id="2ef1e-190">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-191">Prozentsatz der kompatiblen Computer im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-191">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-192">% Nicht kompatibel</span><span class="sxs-lookup"><span data-stu-id="2ef1e-192">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-193">Prozentsatz der nicht kompatiblen Computer im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-193">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-194">% Unknown Compliance</span><span class="sxs-lookup"><span data-stu-id="2ef1e-194">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-195">Prozentsatz der Computer, deren Konformitätsstatus unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-195">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-196">% Ausgenommen</span><span class="sxs-lookup"><span data-stu-id="2ef1e-196">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-197">Prozentsatz der Computer, die von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-197">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-198">% Nicht freigestellt</span><span class="sxs-lookup"><span data-stu-id="2ef1e-198">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-199">Prozentsatz der Computer, die von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-199">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-200">Kompatibel</span><span class="sxs-lookup"><span data-stu-id="2ef1e-200">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-201">Prozentsatz der kompatiblen Computer im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-201">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-202">Nicht kompatibel</span><span class="sxs-lookup"><span data-stu-id="2ef1e-202">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-203">Prozentsatz der nicht kompatiblen Computer im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-203">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-204">Unbekannte Compliance</span><span class="sxs-lookup"><span data-stu-id="2ef1e-204">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-205">Prozentsatz der Computer, deren Konformitätsstatus unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-205">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-206">Befreit</span><span class="sxs-lookup"><span data-stu-id="2ef1e-206">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-207">Gesamtzahl der Computer, die von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-207">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-208">Nicht freigestellt</span><span class="sxs-lookup"><span data-stu-id="2ef1e-208">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-209">Gesamtzahl der Computer, die nicht von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-209">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="2ef1e-210">BitLocker Enterprise Compliance-Zusammenfassungsbericht – Computer Details</span><span class="sxs-lookup"><span data-stu-id="2ef1e-210">BitLocker Enterprise Compliance Summary Report - Computer Details</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ef1e-211">Spalten Name</span><span class="sxs-lookup"><span data-stu-id="2ef1e-211">Column Name</span></span></th>
<th align="left"><span data-ttu-id="2ef1e-212">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ef1e-212">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-213">Computer Name</span><span class="sxs-lookup"><span data-stu-id="2ef1e-213">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-214">Vom Benutzer festgelegter DNS-Computername, der von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-214">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-215">Domänen Name</span><span class="sxs-lookup"><span data-stu-id="2ef1e-215">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-216">Vollständig qualifizierter Domänenname, in dem sich der Clientcomputer befindet und von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-216">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-217">Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="2ef1e-217">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-218">Gesamt Kompatibilitäts Status des Computers, der von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-218">Overall Compliance Status of the computer managed by MBAM.</span></span> <span data-ttu-id="2ef1e-219">Gültige Zustände sind kompatibel und nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-219">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="2ef1e-220">Beachten Sie, dass der Kompatibilitätsstatus pro Laufwerk (siehe nachfolgenden Tabelle) möglicherweise auf unterschiedliche Konformitäts Zustände hindeutet.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-220">Notice that the compliance status per drive (see table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="2ef1e-221">Dieses Feld stellt jedoch diesen Konformitätsstatus gemäß der angegebenen Richtlinie dar.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-221">However, this field represents that compliance state, in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-222">Befreiung</span><span class="sxs-lookup"><span data-stu-id="2ef1e-222">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-223">Status, der angibt, ob der Benutzer von der BitLocker-Richtlinie ausgenommen oder nicht freigestellt ist.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-223">Status that indicates whether the user is exempt or non-exemption from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-224">Geräte Benutzer</span><span class="sxs-lookup"><span data-stu-id="2ef1e-224">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-225">Benutzer des Geräts.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-225">User of the device.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-226">Details zum Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="2ef1e-226">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-227">Fehler-und Statusmeldungen des Kompatibilitätszustands des Computers in Übereinstimmung mit der angegebenen Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-227">Error and status messages of the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-228">Letzter Kontakt</span><span class="sxs-lookup"><span data-stu-id="2ef1e-228">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-229">Datum und Uhrzeit des letzten Kontakts des Computers mit dem Server, um den Kompatibilitätsstatus zu melden.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-229">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="2ef1e-230">Die Kontakthäufigkeit ist konfigurierbar (siehe MBAM-Richtlinieneinstellungen).</span><span class="sxs-lookup"><span data-stu-id="2ef1e-230">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="2ef1e-231">BitLocker-Computer Kompatibilitätsbericht</span><span class="sxs-lookup"><span data-stu-id="2ef1e-231">BitLocker Computer Compliance Report</span></span>

<span data-ttu-id="2ef1e-232">Verwenden Sie diesen Berichtstyp, um Informationen zu sammeln, die für einen Computer spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-232">Use this report type to collect information that is specific to a computer.</span></span> <span data-ttu-id="2ef1e-233">Der Computer Kompatibilitätsbericht enthält detaillierte Verschlüsselungsinformationen zu jedem Laufwerk (Betriebs System und feste Datenlaufwerke) auf einem Computer sowie einen Hinweis auf die Richtlinie, die auf die einzelnen Laufwerktypen auf dem Computer angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-233">The Computer Compliance Report provides detailed encryption information about each drive (Operating System and Fixed data drives) on a computer, and also an indication of the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="2ef1e-234">Um die Details der einzelnen Laufwerke anzuzeigen, erweitern Sie den Eintrag Computer Name.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-234">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="2ef1e-235">**Hinweis**  Der Verschlüsselungsstatus für Wechseldatenträger wird im Bericht nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-235">**Note** Removable Data Volume encryption status is not shown in the report.</span></span>

 

**<span data-ttu-id="2ef1e-236">BitLocker-Computer Kompatibilitätsbericht – Felder für Computer Details</span><span class="sxs-lookup"><span data-stu-id="2ef1e-236">BitLocker Computer Compliance Report – Computer Details Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ef1e-237">Spalten Name</span><span class="sxs-lookup"><span data-stu-id="2ef1e-237">Column Name</span></span></th>
<th align="left"><span data-ttu-id="2ef1e-238">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ef1e-238">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-239">Computer Name</span><span class="sxs-lookup"><span data-stu-id="2ef1e-239">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-240">Vom Benutzer festgelegter DNS-Computername, der von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-240">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-241">Domänen Name</span><span class="sxs-lookup"><span data-stu-id="2ef1e-241">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-242">Vollständig qualifizierter Domänenname, in dem sich der Clientcomputer befindet und von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-242">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-243">Computertyp</span><span class="sxs-lookup"><span data-stu-id="2ef1e-243">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-244">Der Typ des Computers.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-244">Type of computer.</span></span> <span data-ttu-id="2ef1e-245">Gültige Typen sind nicht portabel und portabel.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-245">Valid types are non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-246">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="2ef1e-246">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-247">Der Typ des Betriebssystems, der auf dem verwalteten MBAM-Clientcomputer gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-247">Operating System type found on the MBAM managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-248">Allgemeine Compliance</span><span class="sxs-lookup"><span data-stu-id="2ef1e-248">Overall Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-249">Gesamt Kompatibilitäts Status des Computers, der von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-249">Overall Compliance Status of the computer managed by MBAM.</span></span> <span data-ttu-id="2ef1e-250">Gültige Zustände sind kompatibel und nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-250">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="2ef1e-251">Beachten Sie, dass der Kompatibilitätsstatus pro Laufwerk (siehe nachfolgenden Tabelle) möglicherweise auf unterschiedliche Konformitäts Zustände hindeutet.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-251">Notice that the compliance status per drive (see table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="2ef1e-252">Dieses Feld stellt jedoch diesen Konformitätsstatus gemäß der angegebenen Richtlinie dar.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-252">However, this field represents that compliance state, in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-253">Kompatibilität des Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="2ef1e-253">Operating System Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-254">Kompatibilitätsstatus des Betriebssystems, das von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-254">Compliance status of the operating system that is managed by MBAM.</span></span> <span data-ttu-id="2ef1e-255">Gültige Zustände sind kompatibel und nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-255">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-256">Festgelegte Datenlaufwerks Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="2ef1e-256">Fixed Data Drive Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-257">Kompatibilitätsstatus des festen Datenlaufwerks, das von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-257">Compliance status of the Fixed Data Drive that is managed by MBAM.</span></span> <span data-ttu-id="2ef1e-258">Gültige Zustände sind kompatibel und nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-258">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-259">Datum der letzten Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="2ef1e-259">Last Update Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-260">Datum und Uhrzeit des letzten Kontakts des Computers mit dem Server, um den Kompatibilitätsstatus zu melden.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-260">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="2ef1e-261">Die Kontakthäufigkeit ist konfigurierbar (siehe MBAM-Richtlinieneinstellungen).</span><span class="sxs-lookup"><span data-stu-id="2ef1e-261">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-262">Befreiung</span><span class="sxs-lookup"><span data-stu-id="2ef1e-262">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-263">Status, der angibt, ob der Benutzer von der BitLocker-Richtlinie ausgenommen oder nicht freigestellt ist.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-263">Status that indicates whether the user is exempt or non-exemption from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-264">Befreite Benutzer</span><span class="sxs-lookup"><span data-stu-id="2ef1e-264">Exempted User</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-265">Der Benutzer, der von der BitLocker-Richtlinie ausgenommen ist.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-265">User who is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-266">Befreiungs Datum</span><span class="sxs-lookup"><span data-stu-id="2ef1e-266">Exemption Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-267">Das Datum, an dem die Befreiung gewährt wurde.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-267">Date on which the exemption was granted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-268">Details zum Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="2ef1e-268">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-269">Fehler-und Statusmeldungen des Kompatibilitätszustands des Computers in Übereinstimmung mit der angegebenen Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-269">Error and status messages of the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-270">Richtlinien Verschlüsselungsstärke</span><span class="sxs-lookup"><span data-stu-id="2ef1e-270">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-271">Die vom Administrator während der MBAM-Richtlinien Spezifikation ausgewählte Verschlüsselungsstärke.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-271">Cipher Strength selected by the Administrator during MBAM policy specification.</span></span> <span data-ttu-id="2ef1e-272">(Beispiel: 128-Bit mit Diffusor).</span><span class="sxs-lookup"><span data-stu-id="2ef1e-272">(for example, 128-bit with Diffuser).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-273">Richtlinie: Betriebs System Laufwerk</span><span class="sxs-lookup"><span data-stu-id="2ef1e-273">Policy: Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-274">Gibt an, ob für den O/S und den entsprechenden Protector-Typ eine Verschlüsselung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-274">Indicates if encryption is required for the O/S and the appropriate protector type.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-275">Richtlinie: Festes Datenlaufwerk</span><span class="sxs-lookup"><span data-stu-id="2ef1e-275">Policy:Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-276">Gibt an, ob für das festgelegte Laufwerk eine Verschlüsselung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-276">Indicates if encryption is required for the Fixed Drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-277">Hersteller</span><span class="sxs-lookup"><span data-stu-id="2ef1e-277">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-278">Name des Computerherstellers, wie er im Computer-BIOS angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-278">Computer manufacturer name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-279">Modell</span><span class="sxs-lookup"><span data-stu-id="2ef1e-279">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-280">Name des Computerhersteller-Modells, wie er im Computer-BIOS angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-280">Computer manufacturer model name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-281">Geräte Benutzer</span><span class="sxs-lookup"><span data-stu-id="2ef1e-281">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-282">Bekannte Benutzer auf dem Computer, der von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-282">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="2ef1e-283">BitLocker-Computer Kompatibilitätsbericht – Computer Volumen Felder</span><span class="sxs-lookup"><span data-stu-id="2ef1e-283">BitLocker Computer Compliance Report – Computer Volume Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ef1e-284">Spalten Name</span><span class="sxs-lookup"><span data-stu-id="2ef1e-284">Column Name</span></span></th>
<th align="left"><span data-ttu-id="2ef1e-285">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ef1e-285">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-286">Laufwerkbuchstabe</span><span class="sxs-lookup"><span data-stu-id="2ef1e-286">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-287">Computer Laufwerkbuchstabe, der dem jeweiligen Laufwerk vom Benutzer zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-287">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-288">Laufwerktyp</span><span class="sxs-lookup"><span data-stu-id="2ef1e-288">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-289">Der Typ des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-289">Type of drive.</span></span> <span data-ttu-id="2ef1e-290">Gültige Werte sind Betriebs System Laufwerk und festes Datenlaufwerk.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-290">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="2ef1e-291">Hierbei handelt es sich um physikalische Laufwerke anstatt um logische Volumes.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-291">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-292">Verschlüsselungsstärke</span><span class="sxs-lookup"><span data-stu-id="2ef1e-292">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-293">Die vom Administrator während der MBAM-Richtlinien Spezifikation ausgewählte Verschlüsselungsstärke.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-293">Cipher Strength selected by the Administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-294">Schutztypen</span><span class="sxs-lookup"><span data-stu-id="2ef1e-294">Protector Types</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-295">Der Typ des Beschützers, der über eine Richtlinie zum Verschlüsseln eines Betriebssystems oder eines festen Volumes ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-295">Type of protector selected via policy used to encrypt an operating system or Fixed volume.</span></span> <span data-ttu-id="2ef1e-296">Die gültigen Schutztypen für ein Betriebssystem sind TPM oder TPM + PIN, und bei einem festen Datenvolumen handelt es sich um ein Kennwort.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-296">The valid protector types on an operating system are TPM or TPM+PIN and for a Fixed Data Volume is Password.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ef1e-297">Protector-Status</span><span class="sxs-lookup"><span data-stu-id="2ef1e-297">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-298">Gibt an, dass der Computer, der von MBAM verwaltet wird, den in der Richtlinie angegebenen Protector-Typ aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-298">Indicates that the computer being managed by MBAM has enabled the protector type specified in the policy.</span></span> <span data-ttu-id="2ef1e-299">Die gültigen Zustände sind ein-oder ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-299">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ef1e-300">Verschlüsselungsstatus</span><span class="sxs-lookup"><span data-stu-id="2ef1e-300">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ef1e-301">Verschlüsselungsstatus des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-301">Encryption state of the drive.</span></span> <span data-ttu-id="2ef1e-302">Gültige Zustände sind verschlüsselt, nicht verschlüsselt und verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="2ef1e-302">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="2ef1e-303">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2ef1e-303">Related topics</span></span>


[<span data-ttu-id="2ef1e-304">Verwenden von MBAM mit dem Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="2ef1e-304">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)

 

 





