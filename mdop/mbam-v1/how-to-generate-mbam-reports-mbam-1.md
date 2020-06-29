---
title: So generieren Sie MBAM-Berichte
description: So generieren Sie MBAM-Berichte
author: dansimp
ms.assetid: cdf4ae76-040c-447c-8736-c9e57068d221
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f0b5a4e984d7a609eab7204e67f46042992f586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810609"
---
# <span data-ttu-id="e105d-103">So generieren Sie MBAM-Berichte</span><span class="sxs-lookup"><span data-stu-id="e105d-103">How to Generate MBAM Reports</span></span>


<span data-ttu-id="e105d-104">Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) generiert verschiedene Berichte, um die BitLocker-Verschlüsselungs Nutzung und-Kompatibilität zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="e105d-104">Microsoft BitLocker Administration and Monitoring (MBAM) generates various reports to monitor BitLocker encryption usage and compliance.</span></span> <span data-ttu-id="e105d-105">In diesem Thema wird beschrieben, wie Sie die MBAM-Verwaltungswebsite öffnen und wie Sie MBAM-Berichte zu Unternehmenskonformität, einzelnen Computern, Hardwarekompatibilität und wichtigen Wiederherstellungsaktivitäten generieren.</span><span class="sxs-lookup"><span data-stu-id="e105d-105">This topic describes how to open the MBAM administration website and how to generate MBAM reports on enterprise compliance, individual computers, hardware compatibility, and key recovery activity.</span></span> <span data-ttu-id="e105d-106">Weitere Informationen zu MBAM-Berichten finden Sie unter [Grundlegendes zu MBAM-Berichten](understanding-mbam-reports-mbam-1.md).</span><span class="sxs-lookup"><span data-stu-id="e105d-106">For more information about MBAM reports, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-1.md).</span></span>

<span data-ttu-id="e105d-107">**Hinweis**  Damit Sie die Berichte ausführen können, müssen Sie Mitglied der Rolle " **Berichtsbenutzer** " auf den Computern sein, auf denen Sie die Verwaltungs-und Überwachungs Server Features, die Kompatibilitäts-und Überwachungsdatenbank sowie Compliance-und Überwachungsberichte installiert haben.</span><span class="sxs-lookup"><span data-stu-id="e105d-107">**Note** To run the reports, you must be a member of the **Report Users** role on the computers where you have installed the Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports.</span></span>

 

**<span data-ttu-id="e105d-108">So öffnen Sie die MBAM-Verwaltungswebsite</span><span class="sxs-lookup"><span data-stu-id="e105d-108">To open the MBAM Administration website</span></span>**

1.  <span data-ttu-id="e105d-109">Öffnen Sie einen Webbrowser, und navigieren Sie zur MBAM-Website.</span><span class="sxs-lookup"><span data-stu-id="e105d-109">Open a web browser and navigate to the MBAM website.</span></span> <span data-ttu-id="e105d-110">Die Standard-URL für die Website lautet *http:// &lt; Computer &gt; Name* des Microsoft BitLocker-Verwaltungs-und-Überwachungsservers.</span><span class="sxs-lookup"><span data-stu-id="e105d-110">The default URL for the website is *http://&lt;computername&gt;* of the Microsoft BitLocker Administration and Monitoring server.</span></span>

    <span data-ttu-id="e105d-111">**Hinweis**  Wenn die MBAMadministration-Website auf einem anderen Port als Port 80 installiert wurde, müssen Sie diese Portnummer in der URL angeben.</span><span class="sxs-lookup"><span data-stu-id="e105d-111">**Note** If the MBAMadministration website was installed on a port other than port 80, you must specify that port number in the URL.</span></span> <span data-ttu-id="e105d-112">Beispiel \* &lt; : http://Computername &gt; : &lt; Port &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="e105d-112">For example, *http://&lt;computername&gt;:&lt;port&gt;*.</span></span> <span data-ttu-id="e105d-113">Wenn Sie während der Installation einen Hostnamen für die MBAMadministration-Website angegeben haben, lautet die *URL &lt; http:// &gt; Hostname*.</span><span class="sxs-lookup"><span data-stu-id="e105d-113">If you specified a Host Name for the MBAMadministration website during the installation, the URL would be *http://&lt;hostname&gt;*.</span></span>

     

2.  <span data-ttu-id="e105d-114">Klicken Sie im Navigationsbereich auf **Berichte**.</span><span class="sxs-lookup"><span data-stu-id="e105d-114">In the navigation pane, click **Reports**.</span></span> <span data-ttu-id="e105d-115">Klicken Sie im Hauptbereich auf die Registerkarte für Ihren Berichtstyp: **Enterprise-Konformitätsbericht**, **Computer Kompatibilitätsbericht**, **Hardware Überwachungsbericht**oder **Wiederherstellungs Überwachungsbericht**.</span><span class="sxs-lookup"><span data-stu-id="e105d-115">In the main pane, click the tab for your report type: **Enterprise Compliance Report**, **Computer Compliance Report**, **Hardware Audit Report**, or **Recovery Audit Report**.</span></span>

    <span data-ttu-id="e105d-116">**Hinweis**  Historische MBAM-Client Daten werden in der Kompatibilitätsdatenbank aufbewahrt.</span><span class="sxs-lookup"><span data-stu-id="e105d-116">**Note** Historical MBAM Client data is retained in the compliance database.</span></span> <span data-ttu-id="e105d-117">Diese aufbewahrten Daten sind möglicherweise erforderlich, wenn ein Computer verloren geht oder gestohlen wird.</span><span class="sxs-lookup"><span data-stu-id="e105d-117">This retained data may be needed in case a computer is lost or stolen.</span></span> <span data-ttu-id="e105d-118">Wenn Sie Unternehmensberichte ausführen, sollten Sie geeignete Anfangs-und Endtermine verwenden, um die Zeiträume für die Berichte von ein bis zwei Wochen zu bereichern, um die Genauigkeit der Berichtsdaten zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="e105d-118">When running enterprise reports, you should use appropriate start and end dates to scope the time frames for the reports from one to two weeks to increase the reporting data accuracy.</span></span>

     

**<span data-ttu-id="e105d-119">So erstellen Sie einen Enterprise-Konformitätsbericht</span><span class="sxs-lookup"><span data-stu-id="e105d-119">To generate an enterprise Compliance Report</span></span>**

1.  <span data-ttu-id="e105d-120">Klicken Sie auf der MBAMadministration-Website im Navigationsbereich auf **Berichte** , und klicken Sie dann auf die Registerkarte **Enterprise-Konformitätsbericht** , und wählen Sie die entsprechenden Filter für den Bericht aus.</span><span class="sxs-lookup"><span data-stu-id="e105d-120">On the MBAMadministration website, click **Reports** in the navigation pane, then click the **Enterprise Compliance Report** tab and select the appropriate filters for your report.</span></span> <span data-ttu-id="e105d-121">Für den Enterprise-Konformitätsbericht können Sie die folgenden Filter einrichten.</span><span class="sxs-lookup"><span data-stu-id="e105d-121">For the Enterprise Compliance Report, you can set the following filters.</span></span>

    -   <span data-ttu-id="e105d-122">**Kompatibilitäts Status**</span><span class="sxs-lookup"><span data-stu-id="e105d-122">**Compliance Status**.</span></span> <span data-ttu-id="e105d-123">Verwenden Sie diesen Filter, um die Kompatibilitätsstatus Typen (beispielsweise kompatibel oder nicht kompatibel) anzugeben, die in den Bericht aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e105d-123">Use this filter to specify the compliance status types (for example, Compliant or Noncompliant) to include in the report.</span></span>

    -   <span data-ttu-id="e105d-124">**Fehlerzustand**.</span><span class="sxs-lookup"><span data-stu-id="e105d-124">**Error State**.</span></span> <span data-ttu-id="e105d-125">Verwenden Sie diesen Filter, um die Fehlerzustands Typen wie keinen Fehler oder Fehler anzugeben, die in den Bericht aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e105d-125">Use this filter to specify the Error State types, such as No Error or Error, to include in the report.</span></span>

2.  <span data-ttu-id="e105d-126">Klicken Sie auf **Bericht anzeigen** , um den angegebenen Bericht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e105d-126">Click **View Report** to display the specified report.</span></span>

    <span data-ttu-id="e105d-127">Die Berichtsergebnisse können in einem der verschiedenen verfügbaren Dateiformate wie HTML, Microsoft Word und Microsoft Excel gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e105d-127">The report results can be saved in any of several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

    <span data-ttu-id="e105d-128">**Hinweis**  Der Enterprise-Konformitätsbericht wird von einem SQL-Auftrag generiert, der alle sechs Stunden ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e105d-128">**Note** The Enterprise Compliance report is generated by a SQL job that runs every six hours.</span></span> <span data-ttu-id="e105d-129">Wenn Sie den Bericht zum ersten Mal anzeigen, stellen Sie möglicherweise fest, dass einige Daten fehlen.</span><span class="sxs-lookup"><span data-stu-id="e105d-129">Therefore, the first time you try to view the report you may find that some data is missing.</span></span>

     

3.  <span data-ttu-id="e105d-130">Wenn Sie Informationen zu einem Computer im Computer Kompatibilitätsbericht anzeigen möchten, wählen Sie den Computernamen aus.</span><span class="sxs-lookup"><span data-stu-id="e105d-130">To view information about a computer in the Computer Compliance Report, select the computer name.</span></span>

4.  <span data-ttu-id="e105d-131">Wählen Sie das Pluszeichen (+) neben dem Computernamen aus, um Informationen zu den Volumes auf dem Computer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e105d-131">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

**<span data-ttu-id="e105d-132">So generieren Sie den Bericht zur Computer Konformität</span><span class="sxs-lookup"><span data-stu-id="e105d-132">To generate the Computer Compliance Report</span></span>**

1.  <span data-ttu-id="e105d-133">Wählen Sie auf der MBAMadministration-Website im Navigationsbereich den Knoten **Bericht** aus, und wählen Sie dann den **Bericht Computer Compliance**aus.</span><span class="sxs-lookup"><span data-stu-id="e105d-133">In the MBAMadministration website, select the **Report** node in the navigation pane, and then select the **Computer Compliance Report**.</span></span> <span data-ttu-id="e105d-134">Verwenden Sie den Bericht zur Computer Konformität, um nach **Benutzername** oder **Computername**zu suchen.</span><span class="sxs-lookup"><span data-stu-id="e105d-134">Use the Computer Compliance report to search for **user name** or **computer name**.</span></span>

2.  <span data-ttu-id="e105d-135">Klicken Sie auf **Bericht anzeigen** , um den computerbericht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e105d-135">Click **View Report** to view the computer report.</span></span>

    <span data-ttu-id="e105d-136">Ergebnisse können in einem der verschiedenen verfügbaren Dateiformate wie HTML, Microsoft Word und Microsoft Excel gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e105d-136">Results can be saved in any of several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

3.  <span data-ttu-id="e105d-137">Wenn Sie weitere Informationen zu einem Computer im Computer Kompatibilitätsbericht anzeigen möchten, wählen Sie den Computernamen aus.</span><span class="sxs-lookup"><span data-stu-id="e105d-137">To display more information about a computer in the Computer Compliance Report, select the computer name.</span></span>

4.  <span data-ttu-id="e105d-138">Wählen Sie das Pluszeichen (+) neben dem Computernamen aus, um Informationen zu den Volumes auf dem Computer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e105d-138">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

    <span data-ttu-id="e105d-139">**Hinweis**  Ein MBAM-Client Computer gilt als kompatibel, wenn der Computer den Anforderungen der MBAM-Richtlinieneinstellungen entspricht oder das Hardwaremodell des Computers auf inkompatibel eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="e105d-139">**Note** An MBAM Client computer is considered compliant if the computer matches the requirements of the MBAM policy settings or the computer’s hardware model is set to incompatible.</span></span> <span data-ttu-id="e105d-140">Wenn Sie detaillierte Informationen zu den mit dem Computer verknüpften Datenträger-Volumes anzeigen, können Computer, die aufgrund der Hardwarekompatibilität von der BitLocker-Verschlüsselung ausgenommen sind, als kompatibel angezeigt werden, obwohl der Verschlüsselungsstatus für den Laufwerk Datenträger als nicht kompatibel angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e105d-140">Therefore, when you are viewing detailed information about the disk volumes associated with the computer, computers that are exempt from BitLocker encryption due to hardware compatibility can be displayed as compliant even though their drive volume encryption status is displayed as noncompliant.</span></span>

     

**<span data-ttu-id="e105d-141">So generieren Sie den Hardware Kompatibilitäts Überwachungsbericht</span><span class="sxs-lookup"><span data-stu-id="e105d-141">To generate the Hardware Compatibility Audit Report</span></span>**

1.  <span data-ttu-id="e105d-142">Wählen Sie auf der MBAMadministration-Website im Navigationsbereich den Knoten **Bericht** aus, und wählen Sie dann den **Hardware Überwachungsbericht**aus.</span><span class="sxs-lookup"><span data-stu-id="e105d-142">From the MBAMadministration website, select the **Report** node from the navigation pane, and then select the **Hardware Audit Report**.</span></span> <span data-ttu-id="e105d-143">Wählen Sie die entsprechenden Filter für Ihren Hardware Überwachungsbericht aus.</span><span class="sxs-lookup"><span data-stu-id="e105d-143">Select the appropriate filters for your Hardware Audit report.</span></span> <span data-ttu-id="e105d-144">Der Hardware Überwachungsbericht bietet die folgenden verfügbaren Filter:</span><span class="sxs-lookup"><span data-stu-id="e105d-144">The Hardware Audit report offers the following available filters:</span></span>

    -   <span data-ttu-id="e105d-145">**Benutzer (Domain\\User)**.</span><span class="sxs-lookup"><span data-stu-id="e105d-145">**User (Domain\\User)**.</span></span> <span data-ttu-id="e105d-146">Gibt den Namen des Benutzers an, der eine Änderung vorgenommen hat.</span><span class="sxs-lookup"><span data-stu-id="e105d-146">Specifies the name of the user who made a change.</span></span>

    -   <span data-ttu-id="e105d-147">**Ändern**Sie den Typ.</span><span class="sxs-lookup"><span data-stu-id="e105d-147">**Change Type**.</span></span> <span data-ttu-id="e105d-148">Gibt den Typ der gesuchten Änderungen an.</span><span class="sxs-lookup"><span data-stu-id="e105d-148">Specifies the type of changes you are looking for.</span></span>

    -   <span data-ttu-id="e105d-149">**Anfangstermin**.</span><span class="sxs-lookup"><span data-stu-id="e105d-149">**Start Date**.</span></span> <span data-ttu-id="e105d-150">Gibt den Anfangstermin Teil des Datumsbereichs an, für den Sie einen Bericht erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="e105d-150">Specifies the Start Date part of the date range that you want to report on.</span></span>

    -   <span data-ttu-id="e105d-151">**Enddatum**.</span><span class="sxs-lookup"><span data-stu-id="e105d-151">**End Date**.</span></span> <span data-ttu-id="e105d-152">Gibt den Endtermin des Datumsbereichs an, zu dem Sie einen Bericht erstatten möchten.</span><span class="sxs-lookup"><span data-stu-id="e105d-152">Specifies the End Date part of the date range that you want to report on.</span></span>

2.  <span data-ttu-id="e105d-153">Klicken Sie auf **Bericht anzeigen** , um den Bericht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e105d-153">Click **View Report** to view the report.</span></span>

    <span data-ttu-id="e105d-154">Ergebnisse können in verschiedenen verfügbaren Dateiformaten wie HTML, Microsoft Word und Microsoft Excel gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e105d-154">Results can be saved in several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

**<span data-ttu-id="e105d-155">So generieren Sie den Wiederherstellungsschlüssel-Überwachungsbericht</span><span class="sxs-lookup"><span data-stu-id="e105d-155">To generate the Recovery Key Audit Report</span></span>**

1.  <span data-ttu-id="e105d-156">Wählen Sie auf der MBAMadministration-Website den Knoten **Bericht** im Navigationsbereich aus, und wählen Sie dann den **Wiederherstellungs Überwachungsbericht**aus.</span><span class="sxs-lookup"><span data-stu-id="e105d-156">From the MBAMadministration website, select the **Report** node in the navigation pane, and then select the **Recovery Audit Report**.</span></span> <span data-ttu-id="e105d-157">Wählen Sie die Filter für Ihren Wiederherstellungsschlüssel-Überwachungsbericht aus.</span><span class="sxs-lookup"><span data-stu-id="e105d-157">Select the filters for your Recovery Key Audit report.</span></span> <span data-ttu-id="e105d-158">Die verfügbaren Filter für Wiederherstellungsschlüssel Audits lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e105d-158">The available filters for Recovery Key audits are as follows:</span></span>

    -   <span data-ttu-id="e105d-159">**Requestor**.</span><span class="sxs-lookup"><span data-stu-id="e105d-159">**Requestor**.</span></span> <span data-ttu-id="e105d-160">Gibt den Benutzernamen des Requestors an.</span><span class="sxs-lookup"><span data-stu-id="e105d-160">Specifies the user name of the requestor.</span></span> <span data-ttu-id="e105d-161">Der Anforderer ist die Person im Helpdesk, die im Auftrag eines Benutzers auf den Schlüssel zugegriffen hat.</span><span class="sxs-lookup"><span data-stu-id="e105d-161">The requestor is the person in the help desk who accessed the key on behalf of a user.</span></span>

    -   <span data-ttu-id="e105d-162">**Anfordernder**.</span><span class="sxs-lookup"><span data-stu-id="e105d-162">**Requestee**.</span></span> <span data-ttu-id="e105d-163">Gibt den Benutzernamen des Antragstellers an.</span><span class="sxs-lookup"><span data-stu-id="e105d-163">Specifies the user name of the requestee.</span></span> <span data-ttu-id="e105d-164">Der Antragsteller ist die Person, die den Helpdesk aufgerufen hat, um einen Wiederherstellungsschlüssel zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e105d-164">The requestee is the person who called the help desk to obtain a recovery key.</span></span>

    -   <span data-ttu-id="e105d-165">**Ergebnis anfordern** Gibt die Abfrageergebnistypen an, beispielsweise: Erfolg oder Fehler.</span><span class="sxs-lookup"><span data-stu-id="e105d-165">**Request Result** Specifies the request result types, such as: Success or Failed.</span></span> <span data-ttu-id="e105d-166">So können Sie beispielsweise versuchen, fehlgeschlagene Zugriffsversuche auf Schlüssel anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e105d-166">For example, you may want to view failed key access attempts.</span></span>

    -   <span data-ttu-id="e105d-167">**Key-Typ**.</span><span class="sxs-lookup"><span data-stu-id="e105d-167">**Key Type**.</span></span> <span data-ttu-id="e105d-168">Gibt den Schlüsseltyp an, beispielsweise: Kennwort für Wiederherstellungsschlüssel oder TPM-Kenn Wort Hash.</span><span class="sxs-lookup"><span data-stu-id="e105d-168">Specifies the Key Type, such as: Recovery Key Password or TPM Password Hash.</span></span>

    -   <span data-ttu-id="e105d-169">**Anfangstermin**.</span><span class="sxs-lookup"><span data-stu-id="e105d-169">**Start Date**.</span></span> <span data-ttu-id="e105d-170">Gibt den Anfangstermin Teil des Datumsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="e105d-170">Specifies the Start Date part of the date range.</span></span>

    -   <span data-ttu-id="e105d-171">**Enddatum**.</span><span class="sxs-lookup"><span data-stu-id="e105d-171">**End Date**.</span></span> <span data-ttu-id="e105d-172">Gibt den Endtermin des Datumsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="e105d-172">Specifies the End Date part of the date range.</span></span>

2.  <span data-ttu-id="e105d-173">Klicken Sie auf **Bericht anzeigen** , um den Bericht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e105d-173">Click **View Report** to display the report.</span></span>

    <span data-ttu-id="e105d-174">Ergebnisse können in verschiedenen verfügbaren Dateiformaten wie HTML, Microsoft Word und Microsoft Excel gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e105d-174">Results can be saved in several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

## <span data-ttu-id="e105d-175">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="e105d-175">Related topics</span></span>


[<span data-ttu-id="e105d-176">BitLocker-Kompatibilitätsüberwachung und -berichterstellung mit MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e105d-176">Monitoring and Reporting BitLocker Compliance with MBAM 1.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





