---
title: So generieren Sie MBAM-Berichte
description: So generieren Sie MBAM-Berichte
author: dansimp
ms.assetid: 083550cb-8c3f-49b3-a30e-97d85374d2f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ccdc1a2cd69d8cc2e2c2823827f5ea43ad867a78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810348"
---
# <span data-ttu-id="9541d-103">So generieren Sie MBAM-Berichte</span><span class="sxs-lookup"><span data-stu-id="9541d-103">How to Generate MBAM Reports</span></span>


<span data-ttu-id="9541d-104">Wenn Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mit der eigenständigen Topologie installieren, können Sie unterschiedliche Berichte erstellen, um die BitLocker-Verschlüsselungs Nutzung und-Kompatibilität zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="9541d-104">When you install Microsoft BitLocker Administration and Monitoring (MBAM) with the Stand-alone topology, you can generate different reports to monitor BitLocker encryption usage and compliance.</span></span> <span data-ttu-id="9541d-105">In den Verfahren in diesem Thema wird beschrieben, wie Sie die Website "Verwaltung und Überwachung" und die erforderlichen Schritte zum Generieren von Microsoft BitLocker-Verwaltungs-und-Überwachungsberichten zu Unternehmenskonformität, einzelnen Computern und wichtigen Wiederherstellungsaktivitäten öffnen.</span><span class="sxs-lookup"><span data-stu-id="9541d-105">The procedures in this topic describe how to open the Administration and Monitoring website and the steps that are needed to generate Microsoft BitLocker Administration and Monitoring reports on enterprise compliance, individual computers, and key recovery activity.</span></span> <span data-ttu-id="9541d-106">Detaillierte Informationen zum Verständnis von MBAM-Berichten finden Sie unter [Grundlegendes zu MBAM-Berichten](understanding-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="9541d-106">For detailed information to help understand MBAM reports, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span></span>

<span data-ttu-id="9541d-107">**Hinweis**  Um die Berichte ausführen zu können, müssen Sie Mitglied der **Rolle "Berichtsbenutzer** " auf den Computern sein, auf denen die Verwaltungs-und Überwachungs Server Features, die Kompatibilitäts-und Überwachungsdatenbank sowie die Kompatibilitäts-und Überwachungsberichte installiert sind.</span><span class="sxs-lookup"><span data-stu-id="9541d-107">**Note** To run the reports, you must be a member of the **Report Users Role** on the computers where the Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports are installed.</span></span>

 

**<span data-ttu-id="9541d-108">So öffnen Sie die Website "Verwaltung und Überwachung"</span><span class="sxs-lookup"><span data-stu-id="9541d-108">To open the Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="9541d-109">Öffnen Sie einen Webbrowser, und navigieren Sie zur Websiteverwaltung und Überwachung.</span><span class="sxs-lookup"><span data-stu-id="9541d-109">Open a web browser and navigate to the Administration and Monitoring website.</span></span> <span data-ttu-id="9541d-110">Die Standard-URL für die Websiteverwaltung und Überwachung lautet *http:// &lt; Computer &gt; Name*.</span><span class="sxs-lookup"><span data-stu-id="9541d-110">The default URL for the Administration and Monitoring website is *http://&lt;computername&gt;*.</span></span>

    <span data-ttu-id="9541d-111">**Hinweis**  Wenn Lebensarbeitszeit und die Überwachungs Website auf einem anderen Port als 80 installiert wurden, müssen Sie den Port in der URL angeben (beispielsweise \*http:// &lt; Computername &gt; : &lt; Port &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="9541d-111">**Note** If theAdministration and Monitoring website was installed on a port other than 80, you have to specify the port in the URL (for example, *http://&lt;computername&gt;:&lt;port&gt;*.</span></span> <span data-ttu-id="9541d-112">Wenn Sie während der Installation einen Hostnamen für Lebensarbeitszeit-und Überwachungs Website angegeben haben, lautet die URL \*http:// &lt; Hostname &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="9541d-112">If you specified a host name for theAdministration and Monitoring website during the installation, the URL is *http://&lt;hostname&gt;*.</span></span>

     

2.  <span data-ttu-id="9541d-113">Klicken Sie im linken Bereich auf **Berichte** , und wählen Sie dann in der oberen Menüleiste den Bericht aus, den Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="9541d-113">In the left pane, click **Reports** and then select the report you want to run from the top menu bar.</span></span>

    <span data-ttu-id="9541d-114">Historische MBAM-Client Daten werden in der Kompatibilitätsdatenbank für historische Bezüge aufbewahrt, falls ein Computer verloren geht oder gestohlen wird.</span><span class="sxs-lookup"><span data-stu-id="9541d-114">Historical MBAM client data is retained in the compliance database for historical reference in case a computer is lost or stolen.</span></span> <span data-ttu-id="9541d-115">Wenn Sie Unternehmensberichte ausführen, empfehlen wir, dass Sie geeignete Anfangs-und Endtermine verwenden, um die Zeiträume für die Berichte von ein bis zwei Wochen zu bereichern, um die Genauigkeit der Berichtsdaten zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="9541d-115">When running enterprise reports, we recommend that you use appropriate start and end dates to scope the time frames for the reports from one to two weeks to increase reporting data accuracy.</span></span>

    <span data-ttu-id="9541d-116">**Hinweis**  Wenn SSRS nicht für die Verwendung von Secure Socket Layer konfiguriert wurde, wird die URL für die Berichte bei der Installation des MBAM-Servers auf http anstatt auf HTTPS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9541d-116">**Note** If SSRS was not configured to use Secure Socket Layer, the URL for the reports will be set to HTTP instead of to HTTPS when you install the MBAM Server.</span></span> <span data-ttu-id="9541d-117">Wenn Sie dann zum Helpdesk-Portal wechseln und einen Bericht auswählen, wird die folgende Meldung angezeigt: "nur sicherer Inhalt wird angezeigt."</span><span class="sxs-lookup"><span data-stu-id="9541d-117">If you then go to the Help Desk portal and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span> <span data-ttu-id="9541d-118">Klicken Sie auf **alle Inhalte anzeigen**, um den Bericht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9541d-118">To show the report, click **Show All Content**.</span></span>

     

**<span data-ttu-id="9541d-119">So erstellen Sie einen Enterprise-Konformitätsbericht</span><span class="sxs-lookup"><span data-stu-id="9541d-119">To generate an Enterprise Compliance Report</span></span>**

1.  <span data-ttu-id="9541d-120">Wählen Sie auf der Websiteverwaltung und Überwachung im linken Navigationsbereich den Knoten **Berichte** aus, wählen Sie **Enterprise-Konformitätsbericht**aus, und wählen Sie die Filter aus, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="9541d-120">From the Administration and Monitoring website, select the **Reports** node from the left navigation pane, select **Enterprise Compliance Report**, and select the filters that you want to use.</span></span> <span data-ttu-id="9541d-121">Die verfügbaren Filter für den Enterprise Compliance-Bericht lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9541d-121">The available filters for the Enterprise Compliance Report are the following:</span></span>

    -   <span data-ttu-id="9541d-122">**Kompatibilitäts Status**</span><span class="sxs-lookup"><span data-stu-id="9541d-122">**Compliance Status**.</span></span> <span data-ttu-id="9541d-123">Verwenden Sie diesen Filter, um die Kompatibilitätsstatus Typen (beispielsweise kompatibel oder nicht kompatibel) des Berichts anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9541d-123">Use this filter to specify the compliance status types (for example, Compliant, or Noncompliant) of the report.</span></span>

    -   <span data-ttu-id="9541d-124">**Fehlerzustand**.</span><span class="sxs-lookup"><span data-stu-id="9541d-124">**Error State**.</span></span> <span data-ttu-id="9541d-125">Verwenden Sie diesen Filter, um die Fehlerzustands Typen (beispielsweise kein Fehler oder Fehler) des Berichts anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9541d-125">Use this filter to specify the error state types (for example, No Error, or Error) of the report.</span></span>

2.  <span data-ttu-id="9541d-126">Klicken Sie auf **Bericht anzeigen** , um den ausgewählten Bericht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9541d-126">Click **View Report** to display the selected report.</span></span>

    <span data-ttu-id="9541d-127">Ergebnisse können in unterschiedlichen Formaten wie HTML, Microsoft Word und Microsoft Excel gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="9541d-127">Results can be saved in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

    <span data-ttu-id="9541d-128">**Hinweis**  Der Enterprise-Konformitätsbericht wird von einem SQL-Auftrag generiert, der alle sechs Stunden ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9541d-128">**Note** The Enterprise Compliance report is generated by a SQL job that runs every six hours.</span></span> <span data-ttu-id="9541d-129">Wenn Sie den Bericht zum ersten Mal anzeigen, stellen Sie möglicherweise fest, dass einige Daten fehlen.</span><span class="sxs-lookup"><span data-stu-id="9541d-129">Therefore, the first time you view the report, you may find that some data is missing.</span></span> <span data-ttu-id="9541d-130">Sie können aktualisierte Berichtsdaten mithilfe von SQL Management Studio manuell generieren.</span><span class="sxs-lookup"><span data-stu-id="9541d-130">You can generate updated report data manually by using SQL Management Studio.</span></span> <span data-ttu-id="9541d-131">Erweitern Sie im Fenster **Objekt-Explorer** den Eintrag **SQL Server-Agent**, erweitern Sie **Aufträge**, klicken Sie mit der rechten Maustaste auf den **createcache** -Auftrag, und wählen Sie **Job bei Schritt starten** aus.</span><span class="sxs-lookup"><span data-stu-id="9541d-131">From the **Object Explorer** window, expand **SQL Server Agent**, expand **Jobs**, right-click the **CreateCache** job, and select **Start Job at Step….**</span></span>

     

3.  <span data-ttu-id="9541d-132">Wählen Sie einen Computernamen aus, um Informationen zum Computer im Bericht zur Computer Konformität anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9541d-132">Select a computer name to view information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="9541d-133">Wählen Sie das Pluszeichen (+) neben dem Computernamen aus, um Informationen zu den Volumes auf dem Computer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9541d-133">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

**<span data-ttu-id="9541d-134">So generieren Sie den Bericht zur Computer Konformität</span><span class="sxs-lookup"><span data-stu-id="9541d-134">To generate the Computer Compliance Report</span></span>**

1.  <span data-ttu-id="9541d-135">Wählen Sie auf der Websiteverwaltung und Überwachung im linken Navigationsbereich den Knoten **Bericht** aus, und wählen Sie dann den **Bericht Computer Compliance**aus.</span><span class="sxs-lookup"><span data-stu-id="9541d-135">In the Administration and Monitoring website, select the **Report** node from the left navigation pane, and then select the **Computer Compliance Report**.</span></span> <span data-ttu-id="9541d-136">Verwenden Sie den Bericht zur Computer Konformität, um nach **Benutzername** oder **Computername**zu suchen.</span><span class="sxs-lookup"><span data-stu-id="9541d-136">Use the Computer Compliance report to search for **user name** or **computer name**.</span></span>

2.  <span data-ttu-id="9541d-137">Klicken Sie auf **Bericht anzeigen** , um den computerbericht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9541d-137">Click **View Report** to view the computer report.</span></span>

    <span data-ttu-id="9541d-138">Ergebnisse können in unterschiedlichen Formaten wie HTML, Microsoft Word und Microsoft Excel gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="9541d-138">Results can be saved in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

3.  <span data-ttu-id="9541d-139">Wählen Sie einen Computernamen aus, um weitere Informationen zum Computer im Bericht zur Computer Konformität anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9541d-139">Select a computer name to display more information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="9541d-140">Wählen Sie das Pluszeichen (+) neben dem Computernamen aus, um Informationen zu den Volumes auf dem Computer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9541d-140">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

    <span data-ttu-id="9541d-141">**Hinweis**  Ein MBAM-Clientcomputer gilt als kompatibel, wenn der Computer den Anforderungen der MBAM-Richtlinieneinstellungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="9541d-141">**Note** An MBAM client computer is considered compliant if the computer matches the requirements of the MBAM policy settings.</span></span>

     

**<span data-ttu-id="9541d-142">So generieren Sie den Wiederherstellungsschlüssel-Überwachungsbericht</span><span class="sxs-lookup"><span data-stu-id="9541d-142">To generate the Recovery Key Audit Report</span></span>**

1.  <span data-ttu-id="9541d-143">Wählen Sie auf der Websiteverwaltung und Überwachung im linken Navigationsbereich den Knoten **Bericht** aus, und wählen Sie dann den **Bericht Wiederherstellungs**Überwachung aus.</span><span class="sxs-lookup"><span data-stu-id="9541d-143">From the Administration and Monitoring website, select the **Report** node in the left navigation pane, and then select the **Recovery Audit Report**.</span></span> <span data-ttu-id="9541d-144">Wählen Sie die Filter für Ihren Wiederherstellungsschlüssel-Überwachungsbericht aus.</span><span class="sxs-lookup"><span data-stu-id="9541d-144">Select the filters for your Recovery Key Audit report.</span></span> <span data-ttu-id="9541d-145">Die verfügbaren Filter für Wiederherstellungsschlüssel Audits lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9541d-145">The available filters for Recovery Key audits are as follows:</span></span>

    -   <span data-ttu-id="9541d-146">**Requestor**.</span><span class="sxs-lookup"><span data-stu-id="9541d-146">**Requestor**.</span></span> <span data-ttu-id="9541d-147">Dieser Filter ermöglicht Benutzern, den Benutzernamen des anfordernden Benutzers anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9541d-147">This filter enables users to specify the user name of the requester.</span></span> <span data-ttu-id="9541d-148">Der anfordernde ist die Person im Helpdesk, die im Auftrag eines Benutzers auf den Schlüssel zugegriffen hat.</span><span class="sxs-lookup"><span data-stu-id="9541d-148">The requester is the person in the Help Desk who accessed the key on behalf of a user.</span></span>

    -   <span data-ttu-id="9541d-149">**Anfordernder**.</span><span class="sxs-lookup"><span data-stu-id="9541d-149">**Requestee**.</span></span> <span data-ttu-id="9541d-150">Mit diesem Filter können Benutzer den Benutzernamen des anfordernden angeben.</span><span class="sxs-lookup"><span data-stu-id="9541d-150">This filter enables users to specify the user name of the requestee.</span></span> <span data-ttu-id="9541d-151">Der Antragsteller ist die Person, die den Helpdesk aufgerufen hat, um einen Wiederherstellungsschlüssel zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9541d-151">The requestee is the person who called the Help Desk to obtain a recovery key.</span></span>

    -   <span data-ttu-id="9541d-152">**Ergebnis anfordern**.</span><span class="sxs-lookup"><span data-stu-id="9541d-152">**Request Result**.</span></span> <span data-ttu-id="9541d-153">Dieser Filter ermöglicht Benutzern, die anforderungsergebnis Typen (beispielsweise Erfolg oder Fehler) anzugeben, auf denen der Bericht basieren soll.</span><span class="sxs-lookup"><span data-stu-id="9541d-153">This filter enables users to specify the request result types (for example, Success or Failed) that they want to base the report on.</span></span> <span data-ttu-id="9541d-154">Beispielsweise können Benutzer fehlgeschlagene Zugriffsversuche auf Schlüssel anzeigen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="9541d-154">For example, users may want to view failed key access attempts.</span></span>

    -   <span data-ttu-id="9541d-155">**Key-Typ**.</span><span class="sxs-lookup"><span data-stu-id="9541d-155">**Key Type**.</span></span> <span data-ttu-id="9541d-156">Dieser Filter ermöglicht Benutzern die Angabe des Schlüsseltyps (beispielsweise: Wiederherstellungsschlüssel Kennwort oder TPM-Kenn Wort Hash), auf dem der Bericht basieren soll.</span><span class="sxs-lookup"><span data-stu-id="9541d-156">This filter enables users to specify the Key Type (for example: Recovery Key Password or TPM Password Hash) that they want to base the report on.</span></span>

    -   <span data-ttu-id="9541d-157">**Anfangstermin**.</span><span class="sxs-lookup"><span data-stu-id="9541d-157">**Start Date**.</span></span> <span data-ttu-id="9541d-158">Dieser Filter wird verwendet, um den Anfangstermin Teil des Datumsbereichs zu definieren, über den der Benutzerbericht erstatten möchte.</span><span class="sxs-lookup"><span data-stu-id="9541d-158">This filter is used to define the Start Date part of the date range that the user wants to report on.</span></span>

    -   <span data-ttu-id="9541d-159">**Enddatum**.</span><span class="sxs-lookup"><span data-stu-id="9541d-159">**End Date**.</span></span> <span data-ttu-id="9541d-160">Dieser Filter wird verwendet, um den Enddatums Teil des Datumsbereichs zu definieren, über den die Benutzer Berichte erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="9541d-160">This filter is used to define the End Date part of the date range that the users want to report on.</span></span>

2.  <span data-ttu-id="9541d-161">Klicken Sie auf **Bericht anzeigen** , um den Bericht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9541d-161">Click **View Report** to view the report.</span></span>

    <span data-ttu-id="9541d-162">Ergebnisse können in unterschiedlichen Formaten wie HTML, Microsoft Word und Microsoft Excel gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="9541d-162">Results can be saved in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

## <span data-ttu-id="9541d-163">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9541d-163">Related topics</span></span>


[<span data-ttu-id="9541d-164">BitLocker-Kompatibilitätsüberwachung und -berichterstellung mit MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="9541d-164">Monitoring and Reporting BitLocker Compliance with MBAM 2.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





