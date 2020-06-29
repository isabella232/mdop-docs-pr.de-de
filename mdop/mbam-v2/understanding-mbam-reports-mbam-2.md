---
title: Grundlegende Informationen zu MBAM-Berichten
description: Grundlegende Informationen zu MBAM-Berichten
author: dansimp
ms.assetid: 8778f333-760e-4f26-acb4-4e73b6fbb536
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c3ca5e4da4cbcea80c87520f0ecd05e1e7d6be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810180"
---
# <span data-ttu-id="b686a-103">Grundlegende Informationen zu MBAM-Berichten</span><span class="sxs-lookup"><span data-stu-id="b686a-103">Understanding MBAM Reports</span></span>


<span data-ttu-id="b686a-104">Wenn Sie die eigenständige Topologie bei der Installation von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) ausgewählt haben, können Sie in MBAM verschiedene Berichte ausführen, um die BitLocker-Verwendung und-Kompatibilität zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="b686a-104">If you chose the Stand-alone topology when you installed Microsoft BitLocker Administration and Monitoring (MBAM), you can run different reports in MBAM to monitor BitLocker usage and compliance.</span></span> <span data-ttu-id="b686a-105">MBAM meldet Compliance und weitere Informationen zu allen Computern und Geräten, die es verwaltet.</span><span class="sxs-lookup"><span data-stu-id="b686a-105">MBAM reports compliance and other information about all of the computers and devices it manages.</span></span> <span data-ttu-id="b686a-106">Die Informationen in diesem Thema können verwendet werden, um Ihnen zu helfen, die Microsoft BitLocker-Verwaltungs-und-Überwachungsberichte für Enterprise-und einzelne Computer Konformität sowie für wichtige Wiederherstellungsaktivitäten zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="b686a-106">The information in this topic can be used to help you understand the Microsoft BitLocker Administration and Monitoring reports for enterprise and individual computer compliance and for key recovery activity.</span></span>

<span data-ttu-id="b686a-107">**Hinweis**  Wenn Sie bei der Installation von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) die Configuration Manager-Topologie ausgewählt haben, werden Berichte vom Configuration Manager und nicht von MBAM generiert.</span><span class="sxs-lookup"><span data-stu-id="b686a-107">**Note** If you chose the Configuration Manager topology when you installed Microsoft BitLocker Administration and Monitoring (MBAM), reports are generated from Configuration Manager rather than from MBAM.</span></span> <span data-ttu-id="b686a-108">Weitere Informationen zu berichten, die in Configuration Manager ausgeführt werden, finden Sie unter [Grundlegendes zu MBAM-Berichten in Configuration Manager](understanding-mbam-reports-in-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="b686a-108">For more information about reports that are run from Configuration Manager, see [Understanding MBAM Reports in Configuration Manager](understanding-mbam-reports-in-configuration-manager.md).</span></span>

 

## <span data-ttu-id="b686a-109">Grundlegendes zu berichten</span><span class="sxs-lookup"><span data-stu-id="b686a-109">Understanding Reports</span></span>


<span data-ttu-id="b686a-110">Um auf das Feature Berichte der Microsoft BitLocker-Verwaltung und-Überwachung zuzugreifen, öffnen Sie einen Webbrowser, und öffnen Sie die Websiteverwaltung und Überwachung.</span><span class="sxs-lookup"><span data-stu-id="b686a-110">To access the Reports feature of Microsoft BitLocker Administration and Monitoring, open a web browser and open the Administration and Monitoring website.</span></span> <span data-ttu-id="b686a-111">Wählen Sie in der linken Menüleiste **Berichte** aus, und wählen Sie dann in der oberen Menüleiste die Art des zu generierenden Berichts aus.</span><span class="sxs-lookup"><span data-stu-id="b686a-111">Select **Reports** in the left menu bar and then select from the top menu bar the kind of report that you want to generate.</span></span>

### <span data-ttu-id="b686a-112">Enterprise-Konformitätsbericht</span><span class="sxs-lookup"><span data-stu-id="b686a-112">Enterprise Compliance Report</span></span>

<span data-ttu-id="b686a-113">Mithilfe dieses Berichtstyps können Sie Informationen zur allgemeinen BitLocker-Konformität in Ihrer Organisation sammeln.</span><span class="sxs-lookup"><span data-stu-id="b686a-113">Use this report type to collect information on overall BitLocker compliance in your organization.</span></span> <span data-ttu-id="b686a-114">Sie können verschiedene Filter verwenden, um Ihre Suchergebnisse auf den Konformitätsstatus und den Fehlerstatus zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="b686a-114">You can use different filters to narrow your search results to Compliance state and Error status.</span></span> <span data-ttu-id="b686a-115">Die Berichtsinformationen werden alle sechs Stunden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b686a-115">The report information is updated every six hours.</span></span>

**<span data-ttu-id="b686a-116">Enterprise-Konformitäts Berichtsfelder</span><span class="sxs-lookup"><span data-stu-id="b686a-116">Enterprise Compliance Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b686a-117">Spalten Name</span><span class="sxs-lookup"><span data-stu-id="b686a-117">Column Name</span></span></th>
<th align="left"><span data-ttu-id="b686a-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b686a-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b686a-119">Computer Name</span><span class="sxs-lookup"><span data-stu-id="b686a-119">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-120">Vom Benutzer festgelegter DNS-Name, der von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="b686a-120">User-specified DNS name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b686a-121">Domänen Name</span><span class="sxs-lookup"><span data-stu-id="b686a-121">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-122">Vollständig qualifizierter Domänenname, in dem sich der Clientcomputer befindet und von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="b686a-122">Fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b686a-123">Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="b686a-123">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-124">Der Konformitätsstatus für den Computer gemäß der für den Computer angegebenen Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="b686a-124">State of compliance for the computer, according to the policy specified for the computer.</span></span> <span data-ttu-id="b686a-125">Die Zustände sind nicht kompatibel und kompatibel.</span><span class="sxs-lookup"><span data-stu-id="b686a-125">The states are Noncompliant and Compliant.</span></span> <span data-ttu-id="b686a-126">Weitere Informationen dazu, wie Kompatibilitätszustände interpretiert werden, finden Sie in der Tabelle Compliance-Status des Enterprise-Konformitäts Berichts.</span><span class="sxs-lookup"><span data-stu-id="b686a-126">See the Enterprise Compliance Report Compliance States table for more information about how to interpret compliance states.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b686a-127">Details zum Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="b686a-127">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-128">Fehler-und Statusmeldungen des Kompatibilitätszustands des Computers in Übereinstimmung mit der angegebenen Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="b686a-128">Error and status messages of the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b686a-129">Letzter Kontakt</span><span class="sxs-lookup"><span data-stu-id="b686a-129">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-130">Datum und Uhrzeit des letzten Kontakts des Computers mit dem Server, um den Kompatibilitätsstatus zu melden.</span><span class="sxs-lookup"><span data-stu-id="b686a-130">Date and time when the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="b686a-131">Die Kontakthäufigkeit ist konfigurierbar (siehe MBAM-Richtlinieneinstellungen).</span><span class="sxs-lookup"><span data-stu-id="b686a-131">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="b686a-132">Kompatibilitätsstatus für Unternehmens Konformitätsberichte</span><span class="sxs-lookup"><span data-stu-id="b686a-132">Enterprise Compliance Report Compliance States</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b686a-133">Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="b686a-133">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="b686a-134">Befreiung</span><span class="sxs-lookup"><span data-stu-id="b686a-134">Exemption</span></span></th>
<th align="left"><span data-ttu-id="b686a-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b686a-135">Description</span></span></th>
<th align="left"><span data-ttu-id="b686a-136">Benutzeraktion</span><span class="sxs-lookup"><span data-stu-id="b686a-136">User Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b686a-137">Nicht kompatibler</span><span class="sxs-lookup"><span data-stu-id="b686a-137">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-138">Nicht ausgenommen</span><span class="sxs-lookup"><span data-stu-id="b686a-138">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-139">Der Computer ist gemäß der angegebenen Richtlinie nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="b686a-139">The computer is noncompliant, according to the specified policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-140">Erweitern Sie die Details des Computer Compliance-Berichts, indem Sie auf <strong> Computer Name klicken </strong> und ermitteln, ob der Status der einzelnen Laufwerke der angegebenen Richtlinie entspricht.</span><span class="sxs-lookup"><span data-stu-id="b686a-140">Expand the Computer Compliance Report details by clicking <strong>Computer Name</strong>, and determine whether the state of each drive complies with the specified policy.</span></span> <span data-ttu-id="b686a-141">Wenn der Verschlüsselungsstatus angibt, dass der Computer nicht verschlüsselt ist, kann die Verschlüsselung in Bearbeitung sein, oder es liegt ein Fehler auf dem Computer vor.</span><span class="sxs-lookup"><span data-stu-id="b686a-141">If the encryption state indicates that the computer is not encrypted, encryption may be in process, or there is an error on the computer.</span></span> <span data-ttu-id="b686a-142">Wenn kein Fehler vorliegt, besteht die wahrscheinlichste Ursache darin, dass der Computer noch eine Verbindung herstellt oder den Verschlüsselungsstatus herstellt.</span><span class="sxs-lookup"><span data-stu-id="b686a-142">If there is no error, the likely cause is that the computer is still in the process of connecting or establishing the encryption status.</span></span> <span data-ttu-id="b686a-143">Überprüfen Sie später, ob sich der Status ändert.</span><span class="sxs-lookup"><span data-stu-id="b686a-143">Check back later to determine if the state changes.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b686a-144">Kompatibel</span><span class="sxs-lookup"><span data-stu-id="b686a-144">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-145">Nicht ausgenommen</span><span class="sxs-lookup"><span data-stu-id="b686a-145">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-146">Der Computer ist gemäß der angegebenen Richtlinie kompatibel.</span><span class="sxs-lookup"><span data-stu-id="b686a-146">The computer is compliant, according to the specified policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-147">Keine Aktion erforderlich; Sie können den Status des Computers bestätigen, indem Sie den Computer Kompatibilitätsbericht anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b686a-147">No action needed; the state of the computer can be confirmed by viewing the Computer Compliance Report.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="b686a-148">Bericht zur Computer Konformität</span><span class="sxs-lookup"><span data-stu-id="b686a-148">Computer Compliance Report</span></span>

<span data-ttu-id="b686a-149">Verwenden Sie diesen Berichtstyp, um Informationen zu sammeln, die für einen Computer oder benutzerspezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="b686a-149">Use this report type to collect information that is specific to a computer or user.</span></span>

<span data-ttu-id="b686a-150">Dieser Bericht kann angezeigt werden, indem Sie im Enterprise-Konformitätsbericht auf den Computernamen klicken oder den Computernamen im Bericht zur Computer Konformität eingeben.</span><span class="sxs-lookup"><span data-stu-id="b686a-150">This report can be viewed by clicking the computer name in the Enterprise Compliance Report, or by typing the computer name in the Computer Compliance Report.</span></span> <span data-ttu-id="b686a-151">Der Computer Kompatibilitätsbericht enthält detaillierte Verschlüsselungsinformationen zu jedem Laufwerk (Betriebssystem und feste Datenlaufwerke) auf einem Computer sowie einen Hinweis auf die Richtlinie, die auf die einzelnen Laufwerktypen auf dem Computer angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="b686a-151">The Computer Compliance Report provides detailed encryption information about each drive (operating system and fixed data drives) on a computer, and also an indication of the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="b686a-152">Um die Details der einzelnen Laufwerke anzuzeigen, erweitern Sie den Eintrag Computer Name.</span><span class="sxs-lookup"><span data-stu-id="b686a-152">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="b686a-153">**Hinweis**  Der Verschlüsselungsstatus für Wechseldatenträger wird im Bericht nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b686a-153">**Note** Removable Data Volume encryption status will not be shown in the report.</span></span>

 

**<span data-ttu-id="b686a-154">Bericht Felder für Computer Konformitätsberichte</span><span class="sxs-lookup"><span data-stu-id="b686a-154">Computer Compliance Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b686a-155">Spalten Name</span><span class="sxs-lookup"><span data-stu-id="b686a-155">Column Name</span></span></th>
<th align="left"><span data-ttu-id="b686a-156">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b686a-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b686a-157">Computer Name</span><span class="sxs-lookup"><span data-stu-id="b686a-157">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-158">Vom Benutzer festgelegter DNS-Computername, der von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="b686a-158">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b686a-159">Domänen Name</span><span class="sxs-lookup"><span data-stu-id="b686a-159">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-160">Vollständig qualifizierter Domänenname, in dem sich der Clientcomputer befindet und von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="b686a-160">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b686a-161">Computertyp</span><span class="sxs-lookup"><span data-stu-id="b686a-161">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-162">Der Typ des Computers.</span><span class="sxs-lookup"><span data-stu-id="b686a-162">Type of computer.</span></span> <span data-ttu-id="b686a-163">Gültige Typen sind nicht portabel und portabel.</span><span class="sxs-lookup"><span data-stu-id="b686a-163">Valid types are non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b686a-164">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="b686a-164">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-165">Der Typ des Betriebssystems, der auf dem von MBAM verwalteten Clientcomputer gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="b686a-165">Operating system type found on the MBAM-managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b686a-166">Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="b686a-166">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-167">Gesamt Kompatibilitätsstatus des Computers, der von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="b686a-167">Overall compliance status of the computer managed by MBAM.</span></span> <span data-ttu-id="b686a-168">Gültige Zustände sind kompatibel und nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="b686a-168">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="b686a-169">Beachten Sie, dass der Kompatibilitätsstatus pro Laufwerk (siehe die folgende Tabelle) möglicherweise auf unterschiedliche Konformitäts Zustände hindeutet.</span><span class="sxs-lookup"><span data-stu-id="b686a-169">Notice that the compliance status per drive (see the following table) may indicate different compliance states.</span></span> <span data-ttu-id="b686a-170">Dieses Feld stellt jedoch den Konformitätsstatus gemäß der angegebenen Richtlinie dar.</span><span class="sxs-lookup"><span data-stu-id="b686a-170">However, this field represents that compliance state, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b686a-171">Richtlinien Verschlüsselungsstärke</span><span class="sxs-lookup"><span data-stu-id="b686a-171">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-172">Die vom Administrator während der MBAM-Richtlinien Spezifikation ausgewählte Verschlüsselungsstärke (beispielsweise 128-Bit mit Diffusor).</span><span class="sxs-lookup"><span data-stu-id="b686a-172">Cipher strength selected by the administrator during MBAM policy specification (for example, 128-bit with Diffuser).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b686a-173">Richtlinien-Betriebs System Laufwerk</span><span class="sxs-lookup"><span data-stu-id="b686a-173">Policy Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-174">Gibt an, ob für das Betriebssystem eine Verschlüsselung erforderlich ist, und zeigt den entsprechenden Protector-Typ an.</span><span class="sxs-lookup"><span data-stu-id="b686a-174">Indicates if encryption is required for the operating system and shows the appropriate protector type.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b686a-175">Richtlinie – festes Datenlaufwerk</span><span class="sxs-lookup"><span data-stu-id="b686a-175">Policy-Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-176">Gibt an, ob für das festgelegte Datenlaufwerk eine Verschlüsselung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b686a-176">Indicates if encryption is required for the fixed data drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b686a-177">Richtlinie Wechseldatenträger-Datenlaufwerk</span><span class="sxs-lookup"><span data-stu-id="b686a-177">Policy Removable Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-178">Gibt an, ob für das Wechsellaufwerk eine Verschlüsselung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b686a-178">Indicates if encryption is required for the removable drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b686a-179">Geräte Benutzer</span><span class="sxs-lookup"><span data-stu-id="b686a-179">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-180">Bekannte Benutzer auf dem Computer, der von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="b686a-180">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b686a-181">Hersteller</span><span class="sxs-lookup"><span data-stu-id="b686a-181">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-182">Name des Computerherstellers, wie er im Computer-BIOS angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b686a-182">Computer manufacturer name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b686a-183">Modell</span><span class="sxs-lookup"><span data-stu-id="b686a-183">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-184">Name des Computerhersteller-Modells, wie er im Computer-BIOS angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b686a-184">Computer manufacturer model name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b686a-185">Details zum Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="b686a-185">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-186">Fehler-und Statusmeldungen des Kompatibilitätszustands des Computers in Übereinstimmung mit der angegebenen Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="b686a-186">Error and status messages of the compliance state of the computer, in accordance with the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b686a-187">Letzter Kontakt</span><span class="sxs-lookup"><span data-stu-id="b686a-187">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-188">Datum und Uhrzeit des letzten Kontakts des Computers mit dem Server, um den Kompatibilitätsstatus zu melden.</span><span class="sxs-lookup"><span data-stu-id="b686a-188">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="b686a-189">Die Kontakthäufigkeit ist konfigurierbar (siehe MBAM-Richtlinieneinstellungen).</span><span class="sxs-lookup"><span data-stu-id="b686a-189">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="b686a-190">Computer Konformitäts Berichts Laufwerk (Felder)</span><span class="sxs-lookup"><span data-stu-id="b686a-190">Computer Compliance Report Drive Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b686a-191">Spalten Name</span><span class="sxs-lookup"><span data-stu-id="b686a-191">Column Name</span></span></th>
<th align="left"><span data-ttu-id="b686a-192">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b686a-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b686a-193">Laufwerkbuchstabe</span><span class="sxs-lookup"><span data-stu-id="b686a-193">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-194">Computer Laufwerkbuchstabe, der dem jeweiligen Laufwerk vom Benutzer zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="b686a-194">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b686a-195">Laufwerktyp</span><span class="sxs-lookup"><span data-stu-id="b686a-195">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-196">Der Typ des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="b686a-196">Type of drive.</span></span> <span data-ttu-id="b686a-197">Gültige Werte sind Betriebs System Laufwerk und festes Datenlaufwerk.</span><span class="sxs-lookup"><span data-stu-id="b686a-197">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="b686a-198">Hierbei handelt es sich um physikalische Laufwerke anstatt um logische Volumes.</span><span class="sxs-lookup"><span data-stu-id="b686a-198">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b686a-199">Verschlüsselungsstärke</span><span class="sxs-lookup"><span data-stu-id="b686a-199">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-200">Die vom Administrator während der MBAM-Richtlinien Spezifikation ausgewählte Verschlüsselungsstärke.</span><span class="sxs-lookup"><span data-stu-id="b686a-200">Cipher strength selected by the administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b686a-201">Protector-Typ</span><span class="sxs-lookup"><span data-stu-id="b686a-201">Protector Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-202">Der Typ des Beschützers, der über die Richtlinie zum Verschlüsseln eines Betriebssystems oder eines festen Datenvolume ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="b686a-202">Type of protector selected via the policy used to encrypt an operating system or fixed data volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b686a-203">Protector-Status</span><span class="sxs-lookup"><span data-stu-id="b686a-203">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-204">Gibt an, dass der Computer, der von MBAM verwaltet wird, den in der Richtlinie angegebenen Protector-Typ aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="b686a-204">Indicates that the computer being managed by MBAM has enabled the protector type that is specified in the policy.</span></span> <span data-ttu-id="b686a-205">Die gültigen Zustände sind ein-oder ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="b686a-205">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b686a-206">Verschlüsselungsstatus</span><span class="sxs-lookup"><span data-stu-id="b686a-206">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-207">Verschlüsselungsstatus des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="b686a-207">Encryption state of the drive.</span></span> <span data-ttu-id="b686a-208">Gültige Zustände sind verschlüsselt, nicht verschlüsselt und verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="b686a-208">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b686a-209">Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="b686a-209">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-210">Status, der angibt, ob das Laufwerk der Richtlinie entspricht.</span><span class="sxs-lookup"><span data-stu-id="b686a-210">State that indicates whether the drive is in accordance with the policy.</span></span> <span data-ttu-id="b686a-211">Status sind nicht kompatibel und kompatibel.</span><span class="sxs-lookup"><span data-stu-id="b686a-211">States are Noncompliant and Compliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b686a-212">Details zum Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="b686a-212">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-213">Fehler-und Statusmeldungen des Kompatibilitätszustands des Computers entsprechend der angegebenen Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="b686a-213">Error and status messages of the compliance state of the computer, according to the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="b686a-214">Wiederherstellungs Überwachungsbericht</span><span class="sxs-lookup"><span data-stu-id="b686a-214">Recovery Audit Report</span></span>

<span data-ttu-id="b686a-215">Verwenden Sie diesen Berichtstyp, um Benutzer zu überwachen, die den Zugriff auf Wiederherstellungsschlüssel angefordert haben.</span><span class="sxs-lookup"><span data-stu-id="b686a-215">Use this report type to audit users who have requested access to recovery keys.</span></span> <span data-ttu-id="b686a-216">Der Bericht bietet mehrere Filter basierend auf den gewünschten Filterkriterien.</span><span class="sxs-lookup"><span data-stu-id="b686a-216">The report offers several filters based on the desired filtering criteria.</span></span> <span data-ttu-id="b686a-217">Benutzer können nach einer bestimmten Art von Benutzer filtern, entweder einem Helpdesk-Benutzer oder einem Endbenutzer, ob die Anforderung fehlgeschlagen ist oder erfolgreich war, der spezifische Typ des angeforderten Schlüssels und ein Datumsbereich, in dem der Abruf erfolgte.</span><span class="sxs-lookup"><span data-stu-id="b686a-217">Users can filter on a specific type of user, either a Help Desk user or an end user, whether the request failed or was successful, the specific type of key requested, and a date range during which the retrieval occurred.</span></span> <span data-ttu-id="b686a-218">Der Administrator kann basierend auf dem Bedarf kontextbezogene Berichte erstellen.</span><span class="sxs-lookup"><span data-stu-id="b686a-218">The administrator can produce contextual reports based on need.</span></span>

**<span data-ttu-id="b686a-219">Wiederherstellungs Überwachungsbericht (Felder)</span><span class="sxs-lookup"><span data-stu-id="b686a-219">Recovery Audit Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b686a-220">Spalten Name</span><span class="sxs-lookup"><span data-stu-id="b686a-220">Column Name</span></span></th>
<th align="left"><span data-ttu-id="b686a-221">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b686a-221">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b686a-222">Datum und Uhrzeit anfordern</span><span class="sxs-lookup"><span data-stu-id="b686a-222">Request Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-223">Datum und Uhrzeit, zu dem eine Schlüssel Abrufanforderung von einem Endbenutzer oder Helpdesk-Benutzer vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="b686a-223">Date and time that a key retrieval request was made by an end user or Help Desk user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b686a-224">Status anfordern</span><span class="sxs-lookup"><span data-stu-id="b686a-224">Request Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-225">Der Status der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b686a-225">Status of the request.</span></span> <span data-ttu-id="b686a-226">Gültige Status sind entweder erfolgreich (der Schlüssel wurde abgerufen) oder Fehler (der Schlüssel wurde nicht abgerufen).</span><span class="sxs-lookup"><span data-stu-id="b686a-226">Valid statuses are either Successful (the key was retrieved), or Failed (the key was not retrieved).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b686a-227">Helpdesk-Nutzer</span><span class="sxs-lookup"><span data-stu-id="b686a-227">Helpdesk User</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-228">Helpdesk-Benutzer, der die Anforderung zum Abrufen von Schlüsseln initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="b686a-228">Help Desk user that initiated the request for key retrieval.</span></span> <span data-ttu-id="b686a-229">Hinweis: Wenn der Benutzer des Helpdesks den Schlüssel für einen Endbenutzer im Auftrag abruft, ist das Feld Endbenutzer leer.</span><span class="sxs-lookup"><span data-stu-id="b686a-229">Note: If the Help Desk user retrieves the key on behalf on an end-user, the End User field will be blank.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b686a-230">Benutzer</span><span class="sxs-lookup"><span data-stu-id="b686a-230">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-231">Endbenutzer, der die Anforderung zum Abrufen von Schlüsseln initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="b686a-231">End user who initiated the request for key retrieval.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b686a-232">Schlüsseltyp</span><span class="sxs-lookup"><span data-stu-id="b686a-232">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-233">Der Typ des Schlüssels, der entweder vom Helpdesk-Benutzer oder vom Endbenutzer angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="b686a-233">Type of key that was requested by either the Help Desk user or the end user.</span></span> <span data-ttu-id="b686a-234">Die drei Arten von Schlüsseln, die MBAM sammelt, sind: Wiederherstellungsschlüssel Kennwort (zum Wiederherstellen eines Computers im Wiederherstellungsmodus), Wiederherstellungsschlüssel-ID (wird zum Wiederherstellen eines Computers im Wiederherstellungsmodus für einen anderen Benutzer verwendet) und TPM-Kenn Wort Hash (wird zum Wiederherstellen eines Computers mit einem gesperrten TPM verwendet).</span><span class="sxs-lookup"><span data-stu-id="b686a-234">The three types of keys that MBAM collects are: Recovery Key Password (used to recovery a computer in recovery mode), Recovery Key ID (used to recover a computer in recovery mode on behalf of another user), and TPM Password Hash (used to recover a computer with a locked TPM).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b686a-235">Beschreibung des Grunds</span><span class="sxs-lookup"><span data-stu-id="b686a-235">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="b686a-236">Der Grund dafür, dass der angegebene Schlüsseltyp vom Helpdesk-Benutzer oder vom Endbenutzer angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="b686a-236">Reason the specified Key Type was requested by the Help Desk user or the end user.</span></span> <span data-ttu-id="b686a-237">Die Gründe sind in den Features Drive Recovery und TPM Verwalten der Verwaltungs-und Überwachungs Website angegeben.</span><span class="sxs-lookup"><span data-stu-id="b686a-237">The reasons are specified in the Drive Recovery and Manage TPM features of the Administration and Monitoring website.</span></span> <span data-ttu-id="b686a-238">Bei den gültigen Einträgen handelt es sich um einen vom Benutzer eingegebenen Text oder einen der folgenden Ursachencodes:</span><span class="sxs-lookup"><span data-stu-id="b686a-238">The valid entries are either user-entered text, or one of the following reason codes:</span></span></p>
<ul>
<li><p><span data-ttu-id="b686a-239">Betriebs System-Startreihenfolge geändert</span><span class="sxs-lookup"><span data-stu-id="b686a-239">Operating System Boot Order changed</span></span></p></li>
<li><p><span data-ttu-id="b686a-240">BIOS geändert</span><span class="sxs-lookup"><span data-stu-id="b686a-240">BIOS Changed</span></span></p></li>
<li><p><span data-ttu-id="b686a-241">Geänderte Betriebs System Dateien</span><span class="sxs-lookup"><span data-stu-id="b686a-241">Operating System files changed</span></span></p></li>
<li><p><span data-ttu-id="b686a-242">Startschlüssel verloren</span><span class="sxs-lookup"><span data-stu-id="b686a-242">Lost Startup key</span></span></p></li>
<li><p><span data-ttu-id="b686a-243">PIN verloren</span><span class="sxs-lookup"><span data-stu-id="b686a-243">Lost PIN</span></span></p></li>
<li><p><span data-ttu-id="b686a-244">TPM-Reset</span><span class="sxs-lookup"><span data-stu-id="b686a-244">TPM Reset</span></span></p></li>
<li><p><span data-ttu-id="b686a-245">Passphrase verloren</span><span class="sxs-lookup"><span data-stu-id="b686a-245">Lost Passphrase</span></span></p></li>
<li><p><span data-ttu-id="b686a-246">Smartcard verloren</span><span class="sxs-lookup"><span data-stu-id="b686a-246">Lost Smartcard</span></span></p></li>
<li><p><span data-ttu-id="b686a-247">PIN-Sperrung zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="b686a-247">Reset PIN lockout</span></span></p></li>
<li><p><span data-ttu-id="b686a-248">Aktivieren von TPM</span><span class="sxs-lookup"><span data-stu-id="b686a-248">Turn on TPM</span></span></p></li>
<li><p><span data-ttu-id="b686a-249">Deaktivieren von TPM</span><span class="sxs-lookup"><span data-stu-id="b686a-249">Turn off TPM</span></span></p></li>
<li><p><span data-ttu-id="b686a-250">TPM-Kennwort ändern</span><span class="sxs-lookup"><span data-stu-id="b686a-250">Change TPM password</span></span></p></li>
<li><p><span data-ttu-id="b686a-251">TPM löschen</span><span class="sxs-lookup"><span data-stu-id="b686a-251">Clear TPM</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b686a-252">**Hinweis**  Berichtsergebnisse können in einer Datei gespeichert werden, indem Sie auf der Menüleiste Berichte auf die Schaltfläche **exportieren** klicken.</span><span class="sxs-lookup"><span data-stu-id="b686a-252">**Note** Report results can be saved to a file by clicking the **Export** button on the reports menu bar.</span></span> <span data-ttu-id="b686a-253">Weitere Informationen zum Ausführen von MBAM-Berichten finden Sie unter [so](how-to-generate-mbam-reports-mbam-2.md)wird es gemacht: Erstellen von MBAM-Berichten.</span><span class="sxs-lookup"><span data-stu-id="b686a-253">For more information about how to run MBAM reports, see [How to Generate MBAM Reports](how-to-generate-mbam-reports-mbam-2.md).</span></span>

 

## <span data-ttu-id="b686a-254">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b686a-254">Related topics</span></span>


[<span data-ttu-id="b686a-255">BitLocker-Kompatibilitätsüberwachung und -berichterstellung mit MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="b686a-255">Monitoring and Reporting BitLocker Compliance with MBAM 2.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





