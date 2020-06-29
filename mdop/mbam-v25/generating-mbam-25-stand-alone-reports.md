---
title: Generieren von eigenständigen MBAM 2.5-Berichten
description: Generieren von eigenständigen MBAM 2.5-Berichten
author: dansimp
ms.assetid: 0ec623ff-5155-4906-aef2-20cdc0f84667
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: e1c6b33de26cce5d9ad8d20461dbe0ea0f138c78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809766"
---
# <span data-ttu-id="ef4d1-103">Generieren von eigenständigen MBAM 2.5-Berichten</span><span class="sxs-lookup"><span data-stu-id="ef4d1-103">Generating MBAM 2.5 Stand-alone Reports</span></span>


<span data-ttu-id="ef4d1-104">Wenn Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mit der eigenständigen Topologie konfigurieren, können Sie Berichte zum Überwachen der BitLocker-Laufwerk Verschlüsselungs Nutzung und-Kompatibilität generieren.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-104">When you configure Microsoft BitLocker Administration and Monitoring (MBAM) with the Stand-alone topology, you can generate reports to monitor BitLocker drive encryption usage and compliance.</span></span> <span data-ttu-id="ef4d1-105">Dieses Thema enthält die folgenden Verfahren:</span><span class="sxs-lookup"><span data-stu-id="ef4d1-105">This topic contains the following procedures:</span></span>

-   [<span data-ttu-id="ef4d1-106">So öffnen Sie die Website "Verwaltung und Überwachung"</span><span class="sxs-lookup"><span data-stu-id="ef4d1-106">To open the Administration and Monitoring Website</span></span>](#bkmk-openadmin)

-   [<span data-ttu-id="ef4d1-107">So erstellen Sie einen Enterprise-Konformitätsbericht</span><span class="sxs-lookup"><span data-stu-id="ef4d1-107">To generate an Enterprise Compliance Report</span></span>](#bkmk-enterprise)

-   [<span data-ttu-id="ef4d1-108">So erstellen Sie einen Computer Kompatibilitätsbericht</span><span class="sxs-lookup"><span data-stu-id="ef4d1-108">To generate a Computer Compliance Report</span></span>](#bkmk-computercomp)

-   [<span data-ttu-id="ef4d1-109">So generieren Sie einen Wiederherstellungsschlüssel-Überwachungsbericht</span><span class="sxs-lookup"><span data-stu-id="ef4d1-109">To generate a Recovery Key Audit Report</span></span>](#bkmk-recoverykey)

<span data-ttu-id="ef4d1-110">Beschreibungen der eigenständigen Berichte finden Sie unter [Grundlegendes zu MBAM 2,5 eigenständige Berichte](understanding-mbam-25-stand-alone-reports.md).</span><span class="sxs-lookup"><span data-stu-id="ef4d1-110">For descriptions of the Stand-alone reports, see [Understanding MBAM 2.5 Stand-alone Reports](understanding-mbam-25-stand-alone-reports.md).</span></span>

<span data-ttu-id="ef4d1-111">**Hinweis**  Damit Sie die Berichte ausführen können, müssen Sie Mitglied der Gruppe **MBAM-Berichtsbenutzer** sein, die Sie in den Active Directory-Domänendiensten konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-111">**Note** To run the reports, you must be a member of the **MBAM Report Users** group, which you configure in Active Directory Domain Services.</span></span> <span data-ttu-id="ef4d1-112">Weitere Informationen finden Sie unter [Planen von MBAM 2,5-Gruppen und-Konten](planning-for-mbam-25-groups-and-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="ef4d1-112">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md).</span></span>

 

<a href="" id="bkmk-openadmin"></a>**<span data-ttu-id="ef4d1-113">So öffnen Sie die Website "Verwaltung und Überwachung"</span><span class="sxs-lookup"><span data-stu-id="ef4d1-113">To open the Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="ef4d1-114">Öffnen Sie einen Webbrowser, und navigieren Sie zur Website Verwaltung und Überwachung.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-114">Open a web browser and navigate to the Administration and Monitoring Website.</span></span> <span data-ttu-id="ef4d1-115">Die Standard-URL für die Website Verwaltung und Überwachung lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ef4d1-115">The default URL for the Administration and Monitoring Website is:</span></span>

    *<span data-ttu-id="ef4d1-116">http (s):// &lt; MBAMAdministrationServerName &gt; : &lt; Port &gt; /Helpdesk</span><span class="sxs-lookup"><span data-stu-id="ef4d1-116">http(s)://&lt;MBAMAdministrationServerName&gt;:&lt;port&gt;/Helpdesk</span></span>*

2.  <span data-ttu-id="ef4d1-117">Klicken Sie im linken Bereich auf **Berichte**.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-117">In the left pane, click **Reports**.</span></span> <span data-ttu-id="ef4d1-118">Wählen Sie in der oberen Menüleiste den Bericht aus, den Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-118">From the top menu bar, select the report you want to run.</span></span>

    <span data-ttu-id="ef4d1-119">MBAM-Client Daten werden in der Compliance-und Audit-Datenbank für historische Bezüge aufbewahrt, falls ein Computer verloren geht oder gestohlen wird.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-119">MBAM client data is retained in the Compliance and Audit Database for historical reference in case a computer is lost or stolen.</span></span> <span data-ttu-id="ef4d1-120">Wenn Sie Unternehmensberichte ausführen, empfehlen wir, dass Sie geeignete Anfangs-und Endtermine verwenden, um die Zeiträume für die Berichte von ein bis zwei Wochen zu bereichern, um die Genauigkeit der Berichtsdaten zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-120">When running enterprise reports, we recommend that you use appropriate start and end dates to scope the time frames for the reports from one to two weeks to increase reporting data accuracy.</span></span>

    <span data-ttu-id="ef4d1-121">Nachdem Sie einen Bericht erstellt haben, können Sie die Ergebnisse in verschiedenen Formaten wie HTML, Microsoft Word und Microsoft Excel speichern.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-121">After you generate a report, you can save the results in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

    <span data-ttu-id="ef4d1-122">**Hinweis**  Konfigurieren Sie SQL Server Reporting Services (SSRS) so, dass Secure Sockets Layer (SSL) verwendet wird, bevor Sie die Website Verwaltung und Überwachung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-122">**Note** Configure SQL Server Reporting Services (SSRS) to use Secure Sockets Layer (SSL) before configuring the Administration and Monitoring Website.</span></span> <span data-ttu-id="ef4d1-123">Wenn SSRS aus irgendeinem Grund nicht für die Verwendung von SSL konfiguriert ist, wird die URL für die Berichte bei der Konfiguration der Website Verwaltung und Überwachung auf http anstatt auf HTTPS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-123">If, for any reason, SSRS is not configured to use SSL, the URL for the Reports will be set to HTTP instead of to HTTPS when you configure the Administration and Monitoring Website.</span></span> <span data-ttu-id="ef4d1-124">Wenn Sie dann zur Website Verwaltung und Überwachung wechseln und einen Bericht auswählen, wird die folgende Meldung angezeigt: "nur sicherer Inhalt wird angezeigt."</span><span class="sxs-lookup"><span data-stu-id="ef4d1-124">If you then go to the Administration and Monitoring Website and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span> <span data-ttu-id="ef4d1-125">Klicken Sie auf **alle Inhalte anzeigen**, um den Bericht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-125">To show the report, click **Show All Content**.</span></span>

     

<a href="" id="bkmk-enterprise"></a>**<span data-ttu-id="ef4d1-126">So erstellen Sie einen Enterprise-Konformitätsbericht</span><span class="sxs-lookup"><span data-stu-id="ef4d1-126">To generate an Enterprise Compliance Report</span></span>**

1.  <span data-ttu-id="ef4d1-127">Wählen Sie auf der Website Verwaltung und Überwachung im linken Navigationsbereich den Knoten **Berichte** aus, wählen Sie **Enterprise-Konformitätsbericht**aus, und wählen Sie die Filter aus, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-127">From the Administration and Monitoring Website, select the **Reports** node from the left navigation pane, select **Enterprise Compliance Report**, and select the filters that you want to use.</span></span> <span data-ttu-id="ef4d1-128">Die verfügbaren Filter für den Enterprise Compliance-Bericht lauten:</span><span class="sxs-lookup"><span data-stu-id="ef4d1-128">The available filters for the Enterprise Compliance Report are:</span></span>

    -   <span data-ttu-id="ef4d1-129">**Kompatibilitäts Status**</span><span class="sxs-lookup"><span data-stu-id="ef4d1-129">**Compliance Status**.</span></span> <span data-ttu-id="ef4d1-130">Verwenden Sie diesen Filter, um die Kompatibilitätsstatus Typen des Berichts anzugeben (beispielsweise kompatibel oder nicht kompatibel).</span><span class="sxs-lookup"><span data-stu-id="ef4d1-130">Use this filter to specify the compliance status types of the report (for example, Compliant or Noncompliant).</span></span>

    -   <span data-ttu-id="ef4d1-131">**Fehlerzustand**.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-131">**Error State**.</span></span> <span data-ttu-id="ef4d1-132">Verwenden Sie diesen Filter, um die Fehlerzustands Typen des Berichts anzugeben (beispielsweise kein Fehler oder Fehler).</span><span class="sxs-lookup"><span data-stu-id="ef4d1-132">Use this filter to specify the error state types of the report (for example, No Error or Error).</span></span>

2.  <span data-ttu-id="ef4d1-133">Klicken Sie auf **Bericht anzeigen** , um den ausgewählten Bericht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-133">Click **View Report** to display the selected report.</span></span>

3.  <span data-ttu-id="ef4d1-134">Wählen Sie einen Computernamen aus, um Informationen zum Computer im Bericht zur Computer Konformität anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-134">Select a computer name to view information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="ef4d1-135">Wählen Sie das Pluszeichen (+) neben dem Computernamen aus, um Informationen zu den Volumes auf dem Computer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-135">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

<a href="" id="bkmk-computercomp"></a>**<span data-ttu-id="ef4d1-136">So erstellen Sie einen Computer Kompatibilitätsbericht</span><span class="sxs-lookup"><span data-stu-id="ef4d1-136">To generate a Computer Compliance Report</span></span>**

1.  <span data-ttu-id="ef4d1-137">Wählen Sie auf der Website Verwaltung und Überwachung im linken Navigationsbereich den Knoten **Bericht** aus, und wählen Sie dann **Computer Kompatibilitätsbericht**aus.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-137">From the Administration and Monitoring Website, select the **Report** node from the left navigation pane, and then select **Computer Compliance Report**.</span></span> <span data-ttu-id="ef4d1-138">Verwenden Sie den Bericht zur Computer Konformität, um nach **Benutzername** oder **Computername**zu suchen.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-138">Use the Computer Compliance Report to search for **User name** or **Computer name**.</span></span>

2.  <span data-ttu-id="ef4d1-139">Klicken Sie auf **Bericht anzeigen** , um den Bericht zur Computer Konformität anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-139">Click **View Report** to view the Computer Compliance Report.</span></span>

3.  <span data-ttu-id="ef4d1-140">Wählen Sie einen Computernamen aus, um weitere Informationen zum Computer im Bericht zur Computer Konformität anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-140">Select a computer name to display more information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="ef4d1-141">Wählen Sie das Pluszeichen (+) neben dem Computernamen aus, um Informationen zu den Volumes auf dem Computer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-141">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

    <span data-ttu-id="ef4d1-142">**Hinweis**  Ein MBAM-Clientcomputer gilt als kompatibel, wenn der Computer die Anforderungen der MBAM-Gruppenrichtlinieneinstellungen erfüllt oder überschreitet.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-142">**Note** An MBAM client computer is considered compliant if the computer matches or exceeds the requirements of the MBAM Group Policy settings.</span></span>

<a href="" id="bkmk-recoverykey"></a>**<span data-ttu-id="ef4d1-143">So generieren Sie einen Wiederherstellungsschlüssel-Überwachungsbericht</span><span class="sxs-lookup"><span data-stu-id="ef4d1-143">To generate a Recovery Key Audit Report</span></span>**

1.  <span data-ttu-id="ef4d1-144">Wählen Sie auf der Website Verwaltung und Überwachung im linken Navigationsbereich den Knoten **Bericht** aus, und wählen Sie dann **Wiederherstellungs Überwachungsbericht**aus.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-144">From the Administration and Monitoring Website, select the **Report** node in the left navigation pane, and then select **Recovery Audit Report**.</span></span> <span data-ttu-id="ef4d1-145">Wählen Sie die Filter für Ihren Wiederherstellungsschlüssel-Überwachungsbericht aus.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-145">Select the filters for your Recovery Key Audit Report.</span></span> <span data-ttu-id="ef4d1-146">Die verfügbaren Filter für Wiederherstellungsschlüssel Audits lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ef4d1-146">The available filters for recovery key audits are as follows:</span></span>

    -   <span data-ttu-id="ef4d1-147">**Helpdesk-Nutzer**.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-147">**Helpdesk User**.</span></span> <span data-ttu-id="ef4d1-148">Dieser Filter ermöglicht Benutzern, den Benutzernamen des anfordernden Benutzers anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-148">This filter enables users to specify the user name of the requester.</span></span> <span data-ttu-id="ef4d1-149">Der Anforderer ist die Person im Helpdesk, die im Auftrag eines Endbenutzers auf den Schlüssel zugegriffen hat.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-149">The requester is the person in the Help Desk who accessed the key on behalf of an end user.</span></span>

    -   <span data-ttu-id="ef4d1-150">**Endbenutzer**.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-150">**End User**.</span></span> <span data-ttu-id="ef4d1-151">Mit diesem Filter können Benutzer den Benutzernamen des anfordernden angeben.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-151">This filter enables users to specify the user name of the requestee.</span></span> <span data-ttu-id="ef4d1-152">Der anfordernde ist der Endbenutzer, der den Helpdesk aufgerufen hat, um einen Wiederherstellungsschlüssel zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-152">The requestee is the end user who called the Help Desk to obtain a recovery key.</span></span>

    -   <span data-ttu-id="ef4d1-153">**Ergebnis anfordern**.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-153">**Request Result**.</span></span> <span data-ttu-id="ef4d1-154">Dieser Filter ermöglicht Benutzern, die anforderungsergebnis Typen (beispielsweise Erfolg oder Fehler) anzugeben, auf denen der Bericht basieren soll.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-154">This filter enables users to specify the request result types (for example, Success or Failed) that they want to base the report on.</span></span> <span data-ttu-id="ef4d1-155">Beispielsweise können Benutzer fehlgeschlagene Zugriffsversuche auf Schlüssel anzeigen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-155">For example, users may want to view failed key access attempts.</span></span>

    -   <span data-ttu-id="ef4d1-156">**Key-Typ**.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-156">**Key Type**.</span></span> <span data-ttu-id="ef4d1-157">Dieser Filter ermöglicht Benutzern die Angabe des Schlüsseltyps (beispielsweise des Wiederherstellungsschlüssel Kennworts oder des TPM-Kennworthashs), auf dem der Bericht basieren soll.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-157">This filter enables users to specify the key type (for example, Recovery Key Password or TPM Password Hash) that they want to base the report on.</span></span>

    -   <span data-ttu-id="ef4d1-158">**Anfangstermin**.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-158">**Start Date**.</span></span> <span data-ttu-id="ef4d1-159">Dieser Filter wird verwendet, um den Anfangstermin Teil des Datumsbereichs zu definieren, über den der Benutzerbericht erstatten möchte.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-159">This filter is used to define the Start Date part of the date range that the user wants to report on.</span></span>

    -   <span data-ttu-id="ef4d1-160">**Enddatum**.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-160">**End Date**.</span></span> <span data-ttu-id="ef4d1-161">Dieser Filter wird verwendet, um den Enddatums Teil des Datumsbereichs zu definieren, über den die Benutzer Berichte erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-161">This filter is used to define the End Date part of the date range that the users want to report on.</span></span>

2.  <span data-ttu-id="ef4d1-162">Klicken Sie auf **Bericht anzeigen** , um den Bericht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-162">Click **View Report** to view the report.</span></span>



## <span data-ttu-id="ef4d1-163">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ef4d1-163">Related topics</span></span>


[<span data-ttu-id="ef4d1-164">BitLocker-Kompatibilitätsüberwachung und -berichterstellung mit MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ef4d1-164">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[<span data-ttu-id="ef4d1-165">Grundlegende Informationen zu eigenständigen MBAM 2.5-Berichten</span><span class="sxs-lookup"><span data-stu-id="ef4d1-165">Understanding MBAM 2.5 Stand-alone Reports</span></span>](understanding-mbam-25-stand-alone-reports.md)

 

## <span data-ttu-id="ef4d1-166">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="ef4d1-166">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="ef4d1-167">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="ef4d1-167">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="ef4d1-168">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="ef4d1-168">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





