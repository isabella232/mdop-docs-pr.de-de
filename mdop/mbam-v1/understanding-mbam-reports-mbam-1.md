---
title: Grundlegende Informationen zu MBAM-Berichten
description: Grundlegende Informationen zu MBAM-Berichten
author: dansimp
ms.assetid: 34e4aaeb-7f89-41a1-b816-c6fe8397b060
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa64a4724c87a42774e569b556013bfec2ed5514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809613"
---
# <span data-ttu-id="4cde3-103">Grundlegende Informationen zu MBAM-Berichten</span><span class="sxs-lookup"><span data-stu-id="4cde3-103">Understanding MBAM Reports</span></span>


<span data-ttu-id="4cde3-104">Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) generiert verschiedene Berichte, um die BitLocker-Verwendung und-Kompatibilität zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="4cde3-104">Microsoft BitLocker Administration and Monitoring (MBAM) generates various reports to monitor BitLocker usage and compliance.</span></span> <span data-ttu-id="4cde3-105">In diesem Thema werden die MBAM-Berichte für Unternehmenskonformität, einzelne Computer, Hardwarekompatibilität und wichtige Wiederherstellungsaktivitäten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4cde3-105">This topic describes the MBAM reports for enterprise compliance, individual computers, hardware compatibility, and key recovery activity.</span></span>

## <span data-ttu-id="4cde3-106">Grundlegendes zu berichten</span><span class="sxs-lookup"><span data-stu-id="4cde3-106">Understanding Reports</span></span>


<span data-ttu-id="4cde3-107">Wenn Sie auf das Feature Berichte von MBAM zugreifen möchten, öffnen Sie die MBAM-Verwaltungswebsite.</span><span class="sxs-lookup"><span data-stu-id="4cde3-107">To access the Reports feature of MBAM, open the MBAM administration website.</span></span> <span data-ttu-id="4cde3-108">Wählen Sie im Navigationsbereich **Berichte** aus.</span><span class="sxs-lookup"><span data-stu-id="4cde3-108">Select **Reports** in the navigation pane.</span></span> <span data-ttu-id="4cde3-109">Klicken Sie dann im Hauptinhaltsbereich auf die Registerkarte für Ihren Berichtstyp: **Enterprise-Konformitätsbericht**, **Computer Kompatibilitätsbericht**, **Hardware Überwachungsbericht**oder **Wiederherstellungs Überwachungsbericht**.</span><span class="sxs-lookup"><span data-stu-id="4cde3-109">Then, in the main content pane, click the tab for your report type: **Enterprise Compliance Report**, **Computer Compliance Report**, **Hardware Audit Report**, or **Recovery Audit Report**.</span></span>

### <span data-ttu-id="4cde3-110">Enterprise-Konformitätsbericht</span><span class="sxs-lookup"><span data-stu-id="4cde3-110">Enterprise Compliance Report</span></span>

<span data-ttu-id="4cde3-111">Ein Enterprise-Konformitätsbericht enthält Informationen zur allgemeinen BitLocker-Konformität in Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="4cde3-111">An Enterprise Compliance Report provides information on overall BitLocker compliance in your organization.</span></span> <span data-ttu-id="4cde3-112">Mit den verfügbaren Filtern für diesen Bericht können Sie Ihre Suchergebnisse nach dem Konformitätsstatus und dem Fehlerstatus einschränken.</span><span class="sxs-lookup"><span data-stu-id="4cde3-112">The available filters for this report allow you to narrow your search results according to Compliance state and Error status.</span></span> <span data-ttu-id="4cde3-113">Dieser Bericht wird alle sechs Stunden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4cde3-113">This report runs every six hours.</span></span>

**<span data-ttu-id="4cde3-114">Enterprise-Konformitäts Berichtsfelder</span><span class="sxs-lookup"><span data-stu-id="4cde3-114">Enterprise Compliance Report fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4cde3-115">Spalten Name</span><span class="sxs-lookup"><span data-stu-id="4cde3-115">Column Name</span></span></th>
<th align="left"><span data-ttu-id="4cde3-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4cde3-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-117">Computer Name</span><span class="sxs-lookup"><span data-stu-id="4cde3-117">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-118">Der vom Benutzer angegebene DNS-Name, der von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="4cde3-118">The user-specified DNS name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cde3-119">Domänen Name</span><span class="sxs-lookup"><span data-stu-id="4cde3-119">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-120">Der vollqualifizierte Domänenname, in dem sich der Clientcomputer befindet und von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="4cde3-120">The fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-121">Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="4cde3-121">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-122">Der Konformitätsstatus für den Computer entsprechend der für den Computer angegebenen Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="4cde3-122">The state of compliance for the computer, according to the policy specified for the computer.</span></span> <span data-ttu-id="4cde3-123">Die möglichen Zustände sind nicht kompatibel und kompatibel.</span><span class="sxs-lookup"><span data-stu-id="4cde3-123">The possible states are Noncompliant and Compliant.</span></span> <span data-ttu-id="4cde3-124">Weitere Informationen finden Sie unter Konformitätsberichte für den Unternehmens Konformitätsstatus in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="4cde3-124">For more information, see Enterprise Compliance Report Compliance States in this topic.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cde3-125">Befreiung</span><span class="sxs-lookup"><span data-stu-id="4cde3-125">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-126">Der Status der Computer Hardware zum Ermitteln der Identifizierung des Hardwaretyps und ob der Computer von der Richtlinie ausgenommen ist.</span><span class="sxs-lookup"><span data-stu-id="4cde3-126">The state of the computer hardware for determining the identification of the hardware type and whether the computer is exempt from policy.</span></span> <span data-ttu-id="4cde3-127">Es gibt drei mögliche Zustände: Hardware unbekannt (der Hardwaretyp wurde nicht von MBAM identifiziert), Hardware ausgenommen (der Hardwaretyp wurde identifiziert und als von der MBAM-Richtlinie ausgenommen gekennzeichnet) und nicht ausgenommen (die Hardware wurde identifiziert und ist nicht von der Richtlinie ausgenommen).</span><span class="sxs-lookup"><span data-stu-id="4cde3-127">There are three possible states: Hardware Unknown (the hardware type has not been identified by MBAM), Hardware Exempt (the hardware type was identified and was marked as exempt from MBAM policy), and Not Exempt (the hardware was identified and is not exempt from policy).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-128">Geräte Benutzer</span><span class="sxs-lookup"><span data-stu-id="4cde3-128">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-129">Bekannte Benutzer auf dem Computer, der von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="4cde3-129">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cde3-130">Details zum Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="4cde3-130">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-131">Fehler-und Statusmeldungen bezüglich des Kompatibilitätszustands des Computers in Übereinstimmung mit der angegebenen Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="4cde3-131">Error and status messages about the compliance state of the computer in accordance to the specified policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-132">Letzter Kontakt</span><span class="sxs-lookup"><span data-stu-id="4cde3-132">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-133">Datum und Uhrzeit des letzten Kontakts des Computers mit dem Server, um den Kompatibilitätsstatus zu melden.</span><span class="sxs-lookup"><span data-stu-id="4cde3-133">Date and time when the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="4cde3-134">Dieses Mal kann konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="4cde3-134">This time is configurable.</span></span> <span data-ttu-id="4cde3-135">Siehe MBAM-Richtlinieneinstellungen.</span><span class="sxs-lookup"><span data-stu-id="4cde3-135">See MBAM policy settings.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="4cde3-136">Kompatibilitätsstatus für Unternehmens Konformitätsberichte</span><span class="sxs-lookup"><span data-stu-id="4cde3-136">Enterprise Compliance Report Compliance states</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4cde3-137">Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="4cde3-137">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="4cde3-138">Befreiung</span><span class="sxs-lookup"><span data-stu-id="4cde3-138">Exemption</span></span></th>
<th align="left"><span data-ttu-id="4cde3-139">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4cde3-139">Description</span></span></th>
<th align="left"><span data-ttu-id="4cde3-140">Benutzeraktion</span><span class="sxs-lookup"><span data-stu-id="4cde3-140">User Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-141">Nicht kompatibler</span><span class="sxs-lookup"><span data-stu-id="4cde3-141">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-142">Nicht ausgenommen</span><span class="sxs-lookup"><span data-stu-id="4cde3-142">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-143">Der Computer ist gemäß der angegebenen Richtlinie nicht kompatibel, und der Hardwaretyp wurde nicht als von der Richtlinie ausgenommen angegeben.</span><span class="sxs-lookup"><span data-stu-id="4cde3-143">The computer is noncompliant according to the specified policy, and the hardware type has not been indicated as exempt from policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-144">Klicken Sie auf <strong> Computer Name </strong> , um den Bericht zur Computer Konformität zu erweitern und festzustellen, ob der Status der einzelnen Laufwerke der angegebenen Richtlinie entspricht.</span><span class="sxs-lookup"><span data-stu-id="4cde3-144">Click <strong>Computer Name</strong> to expand the Computer Compliance Report and determine whether the state of each drive complies with the specified policy.</span></span> <span data-ttu-id="4cde3-145">Wenn der Verschlüsselungsstatus angibt, dass der Computer nicht verschlüsselt ist, ist möglicherweise die Verschlüsselung noch in Bearbeitung, oder es liegt ein Fehler auf dem Computer vor.</span><span class="sxs-lookup"><span data-stu-id="4cde3-145">If the encryption state indicates that the computer is not encrypted, encryption might still be in process, or there might be an error on the computer.</span></span> <span data-ttu-id="4cde3-146">Wenn kein Fehler vorliegt, besteht die wahrscheinlichste Ursache darin, dass der Computer noch eine Verbindung herstellt oder den Verschlüsselungsstatus herstellt.</span><span class="sxs-lookup"><span data-stu-id="4cde3-146">If there is no error, the likely cause is that the computer is still in the process of connecting or establishing the encryption status.</span></span> <span data-ttu-id="4cde3-147">Überprüfen Sie später, ob sich der Status ändert.</span><span class="sxs-lookup"><span data-stu-id="4cde3-147">Check back later to determine if the state changes.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cde3-148">Kompatibel</span><span class="sxs-lookup"><span data-stu-id="4cde3-148">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-149">Nicht ausgenommen</span><span class="sxs-lookup"><span data-stu-id="4cde3-149">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-150">Der Computer ist gemäß der angegebenen Richtlinie kompatibel.</span><span class="sxs-lookup"><span data-stu-id="4cde3-150">The computer is compliant in accordance with the specified policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-151">Keine Aktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4cde3-151">No Action needed.</span></span> <span data-ttu-id="4cde3-152">Optional können Sie den Bericht zur Computer Konformität anzeigen, um den Zustand des Computers zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="4cde3-152">Optionally, you can view the Computer Compliance Report to confirm the state of the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-153">Kompatibel</span><span class="sxs-lookup"><span data-stu-id="4cde3-153">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-154">Hardware ausgenommen</span><span class="sxs-lookup"><span data-stu-id="4cde3-154">Hardware Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-155">Wenn der Hardwaretyp ausgenommen ist.</span><span class="sxs-lookup"><span data-stu-id="4cde3-155">If the Hardware type is exempt.</span></span> <span data-ttu-id="4cde3-156">Unabhängig davon, wie die Richtlinie festgesetzt wird, oder der einzelne Status jeder Festplatte, wird der Gesamtzustand als kompatibel angesehen.</span><span class="sxs-lookup"><span data-stu-id="4cde3-156">Regardless of how the policy is set or the individual status of each hard-drive, the overall state is considered to be compliant.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-157">Keine Aktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4cde3-157">No action needed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cde3-158">Kompatibel</span><span class="sxs-lookup"><span data-stu-id="4cde3-158">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-159">Hardware unbekannt</span><span class="sxs-lookup"><span data-stu-id="4cde3-159">Hardware Unknown</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-160">MBAM erkennt den Hardware-Typ, aber MBAM weiß nicht, ob es sich um eine Befreiung oder nicht um eine Befreiung handelt.</span><span class="sxs-lookup"><span data-stu-id="4cde3-160">MBAM recognizes the hardware type, but MBAM does not know whether it is exempt or not exempt.</span></span> <span data-ttu-id="4cde3-161">Dies tritt auf, wenn der Administrator den kompatiblen Status für die Hardware nicht eingerichtet hat.</span><span class="sxs-lookup"><span data-stu-id="4cde3-161">This occurs if the administrator has not set the Compatible status for the hardware.</span></span> <span data-ttu-id="4cde3-162">Daher wird MBAM standardmäßig auf den kompatiblen Status zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="4cde3-162">Therefore, MBAM reverts to Compliant status by default.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-163">Dies ist der Anfangszustand eines neu bereitgestellten MBAM-Clients.</span><span class="sxs-lookup"><span data-stu-id="4cde3-163">This is the initial state of a newly deployed MBAM client.</span></span> <span data-ttu-id="4cde3-164">Sie ist in der Regel nur ein vorübergehender Zustand.</span><span class="sxs-lookup"><span data-stu-id="4cde3-164">It is typically only a transient state.</span></span> <span data-ttu-id="4cde3-165">Auch wenn der Administrator die Hardware als kompatibel gekennzeichnet hat, kann es zu einer erheblichen Verzögerung oder konfigurierbarer Wartezeit kommen, bevor der Clientcomputer wieder meldet.</span><span class="sxs-lookup"><span data-stu-id="4cde3-165">Even if the administrator has marked the Hardware as Compatible, there can be a significant delay or configurable wait time before the client computer reports back in.</span></span> <span data-ttu-id="4cde3-166">Notieren Sie sich die Uhrzeit des letzten Kontakts, und melden Sie sich nach dem angegebenen Intervall erneut an, um festzustellen, ob sich der Zustand geändert hat.</span><span class="sxs-lookup"><span data-stu-id="4cde3-166">Make note of the time of Last Contact, and check in again after the specified interval to see if the state has changed.</span></span> <span data-ttu-id="4cde3-167">Wenn sich der Status nicht geändert hat, liegt möglicherweise ein Fehler für diesen Computer oder Hardwaretyp vor.</span><span class="sxs-lookup"><span data-stu-id="4cde3-167">If the state has not changed, there may be an error for this computer or hardware type.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="4cde3-168">Bericht zur Computer Konformität</span><span class="sxs-lookup"><span data-stu-id="4cde3-168">Computer Compliance Report</span></span>

<span data-ttu-id="4cde3-169">Der Bericht zur Computer Konformität zeigt Informationen an, die für einen Computer oder benutzerspezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="4cde3-169">The Computer Compliance Report displays information that is specific to a computer or user.</span></span>

<span data-ttu-id="4cde3-170">Der Bericht zur Computer Konformität enthält detaillierte Verschlüsselungsinformationen und anwendbare Richtlinien für jedes Laufwerk auf einem Computer, einschließlich Betriebssystemlaufwerke und fest Netzlaufwerke.</span><span class="sxs-lookup"><span data-stu-id="4cde3-170">The Computer Compliance Report provides detailed encryption information and applicable policies for each drive on a computer, including operating system drives and fixed data drives.</span></span> <span data-ttu-id="4cde3-171">Wenn Sie diesen Berichtstyp anzeigen möchten, klicken Sie im Enterprise Compliance-Bericht auf den Computernamen, oder geben Sie den Computernamen in den Computer Kompatibilitätsbericht ein.</span><span class="sxs-lookup"><span data-stu-id="4cde3-171">To view this report type, click the computer name in the Enterprise Compliance Report or type the computer name in the Computer Compliance Report.</span></span> <span data-ttu-id="4cde3-172">Um die Details der einzelnen Laufwerke anzuzeigen, erweitern Sie den Eintrag Computer Name.</span><span class="sxs-lookup"><span data-stu-id="4cde3-172">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="4cde3-173">**Hinweis**  Dieser Bericht bietet keinen Verschlüsselungsstatus für Wechseldaten-Volumes.</span><span class="sxs-lookup"><span data-stu-id="4cde3-173">**Note** This report does not provide encryption status for Removable Data Volumes.</span></span>

 

**<span data-ttu-id="4cde3-174">Bericht Felder für Computer Konformitätsberichte</span><span class="sxs-lookup"><span data-stu-id="4cde3-174">Computer Compliance Report fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4cde3-175">Spalten Name</span><span class="sxs-lookup"><span data-stu-id="4cde3-175">Column Name</span></span></th>
<th align="left"><span data-ttu-id="4cde3-176">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4cde3-176">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-177">Computer Name</span><span class="sxs-lookup"><span data-stu-id="4cde3-177">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-178">Der vom Benutzer angegebene DNS-Computername, der von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="4cde3-178">The user-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cde3-179">Domänen Name</span><span class="sxs-lookup"><span data-stu-id="4cde3-179">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-180">Der vollqualifizierte Domänenname, in dem sich der Clientcomputer befindet und von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="4cde3-180">The fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-181">Computertyp</span><span class="sxs-lookup"><span data-stu-id="4cde3-181">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-182">Der Portabilitäts des Computers.</span><span class="sxs-lookup"><span data-stu-id="4cde3-182">The portability type of computer.</span></span> <span data-ttu-id="4cde3-183">Gültige Typen sind nicht portabel und portabel.</span><span class="sxs-lookup"><span data-stu-id="4cde3-183">Valid types are non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cde3-184">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="4cde3-184">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-185">Der Typ des Betriebssystems, der auf dem verwalteten MBAM-Clientcomputer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4cde3-185">Operating System type installed on the MBAM managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-186">Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="4cde3-186">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-187">Der allgemeine Kompatibilitäts Status des Computers, der von MBAM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="4cde3-187">The overall Compliance Status of the computer managed by MBAM.</span></span> <span data-ttu-id="4cde3-188">Gültige Zustände sind kompatibel und nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="4cde3-188">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="4cde3-189">Obwohl es möglich ist, kompatible und nicht konforme Laufwerke auf demselben Computer zu haben, gibt dieses Feld die gesamte Computer Konformität pro angegebene Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="4cde3-189">While it is possible to have Compliant and Noncompliant drives in the same computer, this field indicates the overall computer compliance per specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cde3-190">Policy-Cypher-Stärke</span><span class="sxs-lookup"><span data-stu-id="4cde3-190">Policy Cypher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-191">Die vom Administrator während der MBAM-Richtlinien Spezifikation ausgewählte Verschlüsselungsstärke.</span><span class="sxs-lookup"><span data-stu-id="4cde3-191">The Cipher Strength selected by the Administrator during MBAM policy specification.</span></span> <span data-ttu-id="4cde3-192">Beispiel: 128-Bit mit Diffusor</span><span class="sxs-lookup"><span data-stu-id="4cde3-192">For example, 128-bit with Diffuser</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-193">Richtlinien-Betriebs System Laufwerk</span><span class="sxs-lookup"><span data-stu-id="4cde3-193">Policy Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-194">Gibt an, ob für den Typ O/S und Protector eine Verschlüsselung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4cde3-194">Indicates whether encryption is required for the O/S and the protector type as applicable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cde3-195">Richtlinie mit festem Datenlaufwerk</span><span class="sxs-lookup"><span data-stu-id="4cde3-195">Policy Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-196">Gibt an, ob für das festgelegte Laufwerk eine Verschlüsselung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4cde3-196">Indicates whether encryption is required for the Fixed Drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-197">Richtlinie Wechseldatenträger-Datenlaufwerk</span><span class="sxs-lookup"><span data-stu-id="4cde3-197">Policy Removable Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-198">Gibt an, ob für das Wechsellaufwerk eine Verschlüsselung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4cde3-198">Indicates whether encryption is required for the Removable Drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cde3-199">Geräte Benutzer</span><span class="sxs-lookup"><span data-stu-id="4cde3-199">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-200">Stellt die Identität bekannter Benutzer auf dem Computer bereit.</span><span class="sxs-lookup"><span data-stu-id="4cde3-200">Provides the identity of known users on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-201">Befreiung</span><span class="sxs-lookup"><span data-stu-id="4cde3-201">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-202">Gibt an, ob der Computer-Hardwaretyp von MBAM erkannt wird und, falls bekannt, ob der Computer als von der Richtlinie ausgenommen angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="4cde3-202">Indicates whether the computer hardware type is recognized by MBAM and, if known, whether the computer has been indicated as exempt from policy.</span></span> <span data-ttu-id="4cde3-203">Es gibt drei Zustände: Hardware unbekannt (der Hardwaretyp wurde nicht von MBAM identifiziert); Hardware ausgenommen (der Hardwaretyp wurde identifiziert und als von der MBAM-Richtlinie ausgenommen markiert); und nicht ausgenommen (die Hardware wurde identifiziert und ist nicht von der Richtlinie ausgenommen).</span><span class="sxs-lookup"><span data-stu-id="4cde3-203">There are three states: Hardware Unknown (the hardware type has not been identified by MBAM); Hardware Exempt (the hardware type was identified and was marked as exempt from MBAM policy); and Not Exempt (the hardware was identified and is not exempt from policy).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cde3-204">Hersteller</span><span class="sxs-lookup"><span data-stu-id="4cde3-204">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-205">Der Name des Computerherstellers, wie er im Computer-BIOS angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4cde3-205">The computer manufacturer name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-206">Modell</span><span class="sxs-lookup"><span data-stu-id="4cde3-206">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-207">Der Modellname des Computerherstellers, wie er im Computer-BIOS angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4cde3-207">The computer manufacturer model name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cde3-208">Details zum Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="4cde3-208">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-209">Fehler-und Statusmeldungen des Kompatibilitätszustands des Computers in Übereinstimmung mit der angegebenen Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="4cde3-209">Error and status messages of the compliance state of the computer in accordance with the specified policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-210">Letzter Kontakt</span><span class="sxs-lookup"><span data-stu-id="4cde3-210">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-211">Datum und Uhrzeit des letzten Kontakts des Computers mit dem Server, um den Kompatibilitätsstatus zu melden.</span><span class="sxs-lookup"><span data-stu-id="4cde3-211">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="4cde3-212">T</span><span class="sxs-lookup"><span data-stu-id="4cde3-212">T</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="4cde3-213">Computer Konformitäts Berichts Laufwerk (Felder)</span><span class="sxs-lookup"><span data-stu-id="4cde3-213">Computer Compliance Report Drive fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4cde3-214">Spalten Name</span><span class="sxs-lookup"><span data-stu-id="4cde3-214">Column Name</span></span></th>
<th align="left"><span data-ttu-id="4cde3-215">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4cde3-215">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-216">Laufwerkbuchstabe</span><span class="sxs-lookup"><span data-stu-id="4cde3-216">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-217">Computer Laufwerkbuchstabe, der diesem bestimmten Laufwerk vom Benutzer zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="4cde3-217">Computer drive letter that was assigned to this particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cde3-218">Laufwerktyp</span><span class="sxs-lookup"><span data-stu-id="4cde3-218">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-219">Der Typ des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="4cde3-219">Type of drive.</span></span> <span data-ttu-id="4cde3-220">Gültige Werte sind Betriebs System Laufwerk und festes Datenlaufwerk.</span><span class="sxs-lookup"><span data-stu-id="4cde3-220">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="4cde3-221">Hierbei handelt es sich um physikalische Laufwerke anstatt um logische Volumes.</span><span class="sxs-lookup"><span data-stu-id="4cde3-221">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-222">Cypher-Stärke</span><span class="sxs-lookup"><span data-stu-id="4cde3-222">Cypher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-223">Die vom Administrator während der MBAM-Richtlinien Spezifikation ausgewählte Verschlüsselungsstärke.</span><span class="sxs-lookup"><span data-stu-id="4cde3-223">Cipher Strength selected by the Administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cde3-224">Protector-Typ</span><span class="sxs-lookup"><span data-stu-id="4cde3-224">Protector Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-225">Der Typ des Beschützers, der über eine Richtlinie zum Verschlüsseln eines Betriebssystems oder eines festen Volumes ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="4cde3-225">Type of protector selected via policy used to encrypt an operating system or Fixed volume.</span></span> <span data-ttu-id="4cde3-226">Die gültigen Schutztypen auf einem Betriebssystemlaufwerk sind TPM oder TPM + PIN.</span><span class="sxs-lookup"><span data-stu-id="4cde3-226">The valid protector types on an operating system drive are TPM or TPM+PIN.</span></span> <span data-ttu-id="4cde3-227">Der einzige gültige Protector-Typ für ein festes Datenvolumen ist ein Kennwort.</span><span class="sxs-lookup"><span data-stu-id="4cde3-227">The only valid protector type for a Fixed Data Volume is Password.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-228">Protector-Status</span><span class="sxs-lookup"><span data-stu-id="4cde3-228">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-229">Dieses Feld gibt an, ob der Computer den in der Richtlinie angegebenen Protector-Typ aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="4cde3-229">This field indicates whether the computer has enabled the protector type specified in the policy.</span></span> <span data-ttu-id="4cde3-230">Die gültigen Zustände sind ein-oder ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="4cde3-230">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cde3-231">Verschlüsselungsstatus</span><span class="sxs-lookup"><span data-stu-id="4cde3-231">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-232">Dies ist der aktuelle Verschlüsselungsstatus des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="4cde3-232">This is the current encryption state of the drive.</span></span> <span data-ttu-id="4cde3-233">Gültige Zustände sind verschlüsselt, nicht verschlüsselt und verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="4cde3-233">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-234">Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="4cde3-234">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-235">Gibt an, ob das Laufwerk der Richtlinie entspricht.</span><span class="sxs-lookup"><span data-stu-id="4cde3-235">Indicates whether the drive is in accordance with the policy.</span></span> <span data-ttu-id="4cde3-236">Status sind nicht kompatibel und kompatibel.</span><span class="sxs-lookup"><span data-stu-id="4cde3-236">States are Noncompliant and Compliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cde3-237">Details zum Kompatibilitäts Status</span><span class="sxs-lookup"><span data-stu-id="4cde3-237">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-238">Enthält Fehler-und Statusmeldungen bezüglich des Kompatibilitätszustands des Computers.</span><span class="sxs-lookup"><span data-stu-id="4cde3-238">Contains error and status messages regarding the compliance state of the computer.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="4cde3-239">Hardware Überwachungsbericht</span><span class="sxs-lookup"><span data-stu-id="4cde3-239">Hardware Audit Report</span></span>

<span data-ttu-id="4cde3-240">Dieser Bericht kann Ihnen dabei helfen, Änderungen am Hardware Kompatibilitätsstatus bestimmter Computermarken und-Modelle zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="4cde3-240">This report can help you audit changes to the Hardware Compatibility status of specific computer makes and models.</span></span> <span data-ttu-id="4cde3-241">Damit Sie die Suchergebnisse einschränken können, enthält dieser Berichtfilter für Kriterien wie Art der Änderung und Zeitpunkt des Auftretens.</span><span class="sxs-lookup"><span data-stu-id="4cde3-241">To help you narrow your search results, this report includes filtering on criteria such as type of change and time of occurrence.</span></span> <span data-ttu-id="4cde3-242">Jede Zustandsänderung wird nach Benutzer und Datum und Uhrzeit nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="4cde3-242">Each state change is tracked by user and date and time.</span></span> <span data-ttu-id="4cde3-243">Der Hardwaretyp wird automatisch vom MBAM-Agent ausgefüllt, der auf dem Clientcomputer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4cde3-243">The Hardware Type is automatically populated by the MBAM agent that runs on the client computer.</span></span> <span data-ttu-id="4cde3-244">Dieser Bericht verfolgt Benutzer Änderungen an den Informationen, die direkt vom verwalteten MBAM-Computer erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="4cde3-244">This report tracks user changes to the information collected directly from the MBAM managed computer.</span></span> <span data-ttu-id="4cde3-245">Eine typische administrative Änderung ändert sich von kompatibel zu inkompatibel.</span><span class="sxs-lookup"><span data-stu-id="4cde3-245">A typical administrative change is changing from Compatible to incompatible.</span></span> <span data-ttu-id="4cde3-246">Der Administrator kann jedoch auch ein beliebiges Feld überarbeiten.</span><span class="sxs-lookup"><span data-stu-id="4cde3-246">However, the administrator can also revise any field.</span></span>

**<span data-ttu-id="4cde3-247">Hardware Überwachungsbericht (Felder)</span><span class="sxs-lookup"><span data-stu-id="4cde3-247">Hardware Audit Report fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4cde3-248">Spalten Name</span><span class="sxs-lookup"><span data-stu-id="4cde3-248">Column Name</span></span></th>
<th align="left"><span data-ttu-id="4cde3-249">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4cde3-249">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-250">Datum und Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="4cde3-250">Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-251">Datum und Uhrzeit, an dem eine Änderung am Hardwaretyp vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="4cde3-251">Date and time that a change was made to the Hardware Type.</span></span> <span data-ttu-id="4cde3-252">Beachten Sie, dass jedem eindeutigen Hardwaretyp mindestens ein Eintrag zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="4cde3-252">Note that every unique hardware type is assigned to at least one entry.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cde3-253">Benutzer</span><span class="sxs-lookup"><span data-stu-id="4cde3-253">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-254">Administrator Benutzer, der die Änderung für den jeweiligen Eintrag vorgenommen hat.</span><span class="sxs-lookup"><span data-stu-id="4cde3-254">Administrative user that has made the change for the particular entry.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-255">Typ ändern</span><span class="sxs-lookup"><span data-stu-id="4cde3-255">Change Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-256">Der Typ der Änderung, die an den Hardwaretypen Informationen vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="4cde3-256">Type of change that was made to the hardware type information.</span></span> <span data-ttu-id="4cde3-257">Gültige Werte sind Addition (neuer Eintrag), aktualisieren (vorhandener Eintrag ändern) oder löschen (vorhandenen Eintrag entfernen).</span><span class="sxs-lookup"><span data-stu-id="4cde3-257">Valid values are Addition (new entry), Update (change existing entry), or Deletion (remove existing entry).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cde3-258">Ursprünglicher Wert</span><span class="sxs-lookup"><span data-stu-id="4cde3-258">Original Value</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-259">Der Wert der Hardwaretypen Spezifikation, bevor die Änderung vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="4cde3-259">Value of the hardware type specification before the change was made.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-260">Aktueller Wert</span><span class="sxs-lookup"><span data-stu-id="4cde3-260">Current Value</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-261">Der Wert der Hardwaretypen Spezifikation, nachdem die Änderung vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="4cde3-261">Value of the hardware type specification after the change was made.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="4cde3-262">Wiederherstellungs Überwachungsbericht</span><span class="sxs-lookup"><span data-stu-id="4cde3-262">Recovery Audit Report</span></span>

<span data-ttu-id="4cde3-263">Der Bericht zur Wiederherstellungsprüfung kann Ihnen dabei helfen, Benutzer zu überwachen, die Zugriff auf Wiederherstellungsschlüssel angefordert haben.</span><span class="sxs-lookup"><span data-stu-id="4cde3-263">The Recovery Audit Report can help you audit users who have requested access to recovery keys.</span></span> <span data-ttu-id="4cde3-264">Die Filterkriterien für diesen Bericht umfassen den Typ des Benutzers, der die Anforderung stellt, den Typ des angeforderten Schlüssels, den Zeitpunkt des Auftretens, den Erfolg oder den Fehler, den Zeitpunkt des Auftretens und den Typ des anfordernden Benutzers (Helpdesk, Endbenutzer).</span><span class="sxs-lookup"><span data-stu-id="4cde3-264">The filter criteria for this report includes type of user making the request, type of key requested, time of occurrence, success or fail, time of occurrence, and type of user requesting (help desk, end user).</span></span> <span data-ttu-id="4cde3-265">Dieser Bericht ermöglicht Administratoren, kontextbezogene Berichte zu erstellen, die auf dem Bedarf basieren.</span><span class="sxs-lookup"><span data-stu-id="4cde3-265">This report enables administrators to produce contextual reports based on need.</span></span>

**<span data-ttu-id="4cde3-266">Wiederherstellungs Überwachungsbericht (Felder)</span><span class="sxs-lookup"><span data-stu-id="4cde3-266">Recovery Audit Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4cde3-267">Spalten Name</span><span class="sxs-lookup"><span data-stu-id="4cde3-267">Column Name</span></span></th>
<th align="left"><span data-ttu-id="4cde3-268">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4cde3-268">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-269">Datum und Uhrzeit anfordern</span><span class="sxs-lookup"><span data-stu-id="4cde3-269">Request Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-270">Das Datum und die Uhrzeit, zu dem eine Schlüssel Abrufanforderung von einem Endbenutzer oder Helpdesk-Benutzer erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4cde3-270">The date and time that a key retrieval request was made by an end user or help desk user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cde3-271">Status anfordern</span><span class="sxs-lookup"><span data-stu-id="4cde3-271">Request Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-272">Der Status der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4cde3-272">Status of the request.</span></span> <span data-ttu-id="4cde3-273">Gültige Status sind entweder erfolgreich (der Schlüssel wurde abgerufen) oder Fehler (der Schlüssel wurde nicht abgerufen).</span><span class="sxs-lookup"><span data-stu-id="4cde3-273">Valid statuses are either Successful (the key was retrieved) or Failed (the key was not retrieved).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-274">Helpdesk-Nutzer</span><span class="sxs-lookup"><span data-stu-id="4cde3-274">Helpdesk User</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-275">Der Helpdesk-Benutzer, der die Anforderung zum Abrufen von Schlüsseln initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="4cde3-275">The help desk user who initiated the request for key retrieval.</span></span> <span data-ttu-id="4cde3-276">Wenn der Benutzer des Helpdesks den Schlüssel im Auftrag eines Endbenutzers abruft, ist das Feld Endbenutzer leer.</span><span class="sxs-lookup"><span data-stu-id="4cde3-276">If the help desk user retrieves the key on behalf of an end user, the End User field will be blank.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cde3-277">Benutzer</span><span class="sxs-lookup"><span data-stu-id="4cde3-277">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-278">Der Endbenutzer, der die Anforderung zum Abrufen von Schlüsseln initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="4cde3-278">The end user who initiated the request for key retrieval.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cde3-279">Schlüsseltyp</span><span class="sxs-lookup"><span data-stu-id="4cde3-279">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-280">Der Typ des Schlüssels, der angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="4cde3-280">The type of key that was requested.</span></span> <span data-ttu-id="4cde3-281">MBAM sammelt drei Schlüsseltypen: Kennwort für Wiederherstellungsschlüssel (zum Wiederherstellen eines Computers im Wiederherstellungsmodus). Wiederherstellungsschlüssel-ID (zum Wiederherstellen eines Computers im Wiederherstellungsmodus im Auftrag eines anderen Benutzers) und TPM-Kennwort-Hash (Trusted Platform Module) (zum Wiederherstellen eines Computers mit einem gesperrten TPM).</span><span class="sxs-lookup"><span data-stu-id="4cde3-281">MBAM collects three key types: Recovery Key Password (to recovery a computer in recovery mode); Recovery Key ID (to recover a computer in recovery mode on behalf of another user); and Trusted Platform Module (TPM) Password Hash (to recover a computer with a locked TPM).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cde3-282">Beschreibung des Grunds</span><span class="sxs-lookup"><span data-stu-id="4cde3-282">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cde3-283">Der Grund für die Anforderung des angegebenen Schlüsseltyps.</span><span class="sxs-lookup"><span data-stu-id="4cde3-283">The reason that the specified Key Type was requested.</span></span> <span data-ttu-id="4cde3-284">Die Gründe sind in den Features Drive Recovery und TPM-Verwaltung der administrativen Website angegeben.</span><span class="sxs-lookup"><span data-stu-id="4cde3-284">The reasons are specified in the Drive Recovery and Manage TPM features of the Administrative web site.</span></span> <span data-ttu-id="4cde3-285">Gültige Einträge sind der vom Benutzer eingegebene Text oder einer der folgenden Ursachencodes:</span><span class="sxs-lookup"><span data-stu-id="4cde3-285">Valid entries include user-entered text or one of the following reason codes:</span></span></p>
<ul>
<li><p><span data-ttu-id="4cde3-286">Betriebs System-Startreihenfolge geändert</span><span class="sxs-lookup"><span data-stu-id="4cde3-286">Operating System Boot Order changed</span></span></p></li>
<li><p><span data-ttu-id="4cde3-287">BIOS geändert</span><span class="sxs-lookup"><span data-stu-id="4cde3-287">BIOS changed</span></span></p></li>
<li><p><span data-ttu-id="4cde3-288">Geänderte Betriebs System Dateien</span><span class="sxs-lookup"><span data-stu-id="4cde3-288">Operating System files changed</span></span></p></li>
<li><p><span data-ttu-id="4cde3-289">Startschlüssel verloren</span><span class="sxs-lookup"><span data-stu-id="4cde3-289">Lost Startup key</span></span></p></li>
<li><p><span data-ttu-id="4cde3-290">PIN verloren</span><span class="sxs-lookup"><span data-stu-id="4cde3-290">Lost PIN</span></span></p></li>
<li><p><span data-ttu-id="4cde3-291">TPM-Reset</span><span class="sxs-lookup"><span data-stu-id="4cde3-291">TPM Reset</span></span></p></li>
<li><p><span data-ttu-id="4cde3-292">Passphrase verloren</span><span class="sxs-lookup"><span data-stu-id="4cde3-292">Lost Passphrase</span></span></p></li>
<li><p><span data-ttu-id="4cde3-293">Smartcard verloren</span><span class="sxs-lookup"><span data-stu-id="4cde3-293">Lost Smartcard</span></span></p></li>
<li><p><span data-ttu-id="4cde3-294">PIN-Sperrung zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="4cde3-294">Reset PIN lockout</span></span></p></li>
<li><p><span data-ttu-id="4cde3-295">Aktivieren von TPM</span><span class="sxs-lookup"><span data-stu-id="4cde3-295">Turn on TPM</span></span></p></li>
<li><p><span data-ttu-id="4cde3-296">Deaktivieren von TPM</span><span class="sxs-lookup"><span data-stu-id="4cde3-296">Turn off TPM</span></span></p></li>
<li><p><span data-ttu-id="4cde3-297">TPM-Kennwort ändern</span><span class="sxs-lookup"><span data-stu-id="4cde3-297">Change TPM password</span></span></p></li>
<li><p><span data-ttu-id="4cde3-298">TPM löschen</span><span class="sxs-lookup"><span data-stu-id="4cde3-298">Clear TPM</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="4cde3-299">**Hinweis**  Wenn Sie Berichtsergebnisse in einer Datei speichern möchten, klicken Sie auf der Menüleiste Berichte auf die Schaltfläche **exportieren** .</span><span class="sxs-lookup"><span data-stu-id="4cde3-299">**Note** To save report results to a file, click the **Export** button on the reports menu bar.</span></span>

 

## <span data-ttu-id="4cde3-300">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="4cde3-300">Related topics</span></span>


[<span data-ttu-id="4cde3-301">BitLocker-Kompatibilitätsüberwachung und -berichterstellung mit MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="4cde3-301">Monitoring and Reporting BitLocker Compliance with MBAM 1.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





