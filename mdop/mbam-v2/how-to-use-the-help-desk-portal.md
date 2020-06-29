---
title: So verwenden Sie das Helpdeskportal
description: So verwenden Sie das Helpdeskportal
author: dansimp
ms.assetid: c27f7737-10c8-4164-9de8-57987292c89c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8813fbe9a7b6980b656ecc673ac4ed618c4cf7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811689"
---
# <span data-ttu-id="1302c-103">So verwenden Sie das Helpdeskportal</span><span class="sxs-lookup"><span data-stu-id="1302c-103">How to Use the Help Desk Portal</span></span>


<span data-ttu-id="1302c-104">Die Website "MBAM-Verwaltung und-Überwachung", auch als Helpdesk-Portal bezeichnet, ist eine Verwaltungsschnittstelle zur BitLocker-Laufwerkverschlüsselung, die als Teil der Microsoft BitLocker-Verwaltungs-und-Überwachungsserver-Infrastruktur (MBAM) installiert wird.</span><span class="sxs-lookup"><span data-stu-id="1302c-104">The MBAM Administration and Monitoring website, also referred to as the Help Desk Portal, is an administrative interface to BitLocker drive encryption that is installed as part of the Microsoft BitLocker Administration and Monitoring (MBAM) server infrastructure.</span></span> <span data-ttu-id="1302c-105">In den folgenden Abschnitten wird beschrieben, wie Sie diese Website verwenden können, um Berichte zu überprüfen, die Laufwerke der Endbenutzer wiederherzustellen und das TPMs der Endbenutzer zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="1302c-105">The following sections describe how you can use this website to review reports, recover end users’ drives, and manage end users’ TPMs.</span></span>

## <a href="" id="bkmk-reports"></a><span data-ttu-id="1302c-106">Berichte</span><span class="sxs-lookup"><span data-stu-id="1302c-106">Reports</span></span>


<span data-ttu-id="1302c-107">MBAM sammelt Informationen von Active Directory und Clientcomputern, wodurch Sie verschiedene Berichte ausführen können, um die BitLocker-Nutzung und-Kompatibilität zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="1302c-107">MBAM collects information from Active Directory and client computers, which enables you to run different reports to monitor BitLocker usage and compliance.</span></span> <span data-ttu-id="1302c-108">Über den Abschnitt **Berichte** der Websiteverwaltung und Überwachung können Sie Berichte zu Unternehmenskonformität, einzelnen Computern und wichtigen Wiederherstellungsaktivitäten erstellen.</span><span class="sxs-lookup"><span data-stu-id="1302c-108">Using the **Reports** section of the Administration and Monitoring website, you can generate reports on enterprise compliance, individual computers, and key recovery activity.</span></span> <span data-ttu-id="1302c-109">Eine Beschreibung der einzelnen Berichte finden Sie unter [Grundlegendes zu MBAM-Berichten](understanding-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="1302c-109">For a description of each report, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span></span>

**<span data-ttu-id="1302c-110">So greifen Sie auf Berichte zu</span><span class="sxs-lookup"><span data-stu-id="1302c-110">To access reports</span></span>**

1.  <span data-ttu-id="1302c-111">Öffnen Sie einen Webbrowser, und navigieren Sie zur Website MBAM-Verwaltung und-Überwachung.</span><span class="sxs-lookup"><span data-stu-id="1302c-111">Open a web browser and navigate to the MBAM Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="1302c-112">Wählen Sie im linken Bereich **Berichte** aus.</span><span class="sxs-lookup"><span data-stu-id="1302c-112">Select **Reports** in the left pane.</span></span>

3.  <span data-ttu-id="1302c-113">Wählen Sie in der oberen Menüleiste den zu generierenden Berichtstyp aus.</span><span class="sxs-lookup"><span data-stu-id="1302c-113">From the top menu bar, select the report type you want to generate.</span></span> <span data-ttu-id="1302c-114">Wenn Sie Berichte speichern möchten, klicken Sie auf der Menüleiste Berichte auf die Schaltfläche **exportieren** .</span><span class="sxs-lookup"><span data-stu-id="1302c-114">To save reports, click the **Export** button on the Reports menu bar.</span></span>

<span data-ttu-id="1302c-115">Weitere Informationen zum Ausführen von MBAM-Berichten finden Sie unter [so](how-to-generate-mbam-reports-mbam-2.md)wird es gemacht: Erstellen von MBAM-Berichten.</span><span class="sxs-lookup"><span data-stu-id="1302c-115">For additional information about how to run MBAM reports, see [How to Generate MBAM Reports](how-to-generate-mbam-reports-mbam-2.md).</span></span>

## <a href="" id="bkmk-drirec"></a><span data-ttu-id="1302c-116">Laufwerk Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="1302c-116">Drive Recovery</span></span>


<span data-ttu-id="1302c-117">Das **Laufwerk Wiederherstellungs** Feature der Verwaltungs-und Überwachungs Website ermöglicht Benutzern mit bestimmten Administratorrollen (beispielsweise Helpdesk-Benutzern) den Zugriff auf Wiederherstellungsschlüssel Daten, die vom MBAM-Client erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="1302c-117">The **Drive Recovery** feature of the Administration and Monitoring website allows users with specific administrator roles (for example, Help Desk Users) to access recovery key data that has been collected by the MBAM Client.</span></span> <span data-ttu-id="1302c-118">Diese Daten können verwendet werden, um auf ein durch BitLocker geschütztes Laufwerk zuzugreifen, wenn BitLocker in den Wiederherstellungsmodus wechselt.</span><span class="sxs-lookup"><span data-stu-id="1302c-118">This data can be used to access a BitLocker-protected drive when BitLocker goes into recovery mode.</span></span> <span data-ttu-id="1302c-119">Anweisungen zum Wiederherstellen eines Laufwerks, das sich im Wiederherstellungsmodus befindet, finden Sie unter [Wiederherstellen eines Laufwerks im Wiederherstellungsmodus](how-to-recover-a-drive-in-recovery-mode-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="1302c-119">For instructions on how to recover a drive that is in recovery mode, see [How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-2.md).</span></span>

<span data-ttu-id="1302c-120">Sie können auch Laufwerke wiederherstellen, die verschoben wurden oder die beschädigt sind:</span><span class="sxs-lookup"><span data-stu-id="1302c-120">You can also recover drives that have been moved or that are corrupted:</span></span>

-   [<span data-ttu-id="1302c-121">So stellen Sie ein verschobenes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="1302c-121">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-2.md)

-   [<span data-ttu-id="1302c-122">So stellen Sie ein beschädigtes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="1302c-122">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-2.md)

<span data-ttu-id="1302c-123">Weitere Informationen zum Wiederherstellen eines durch BitLocker geschützten Laufwerks finden Sie unter [Durchführen der BitLocker-Verwaltung mit MBAM](performing-bitlocker-management-with-mbam-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="1302c-123">For additional information about how to recover a BitLocker-protected drive, see [Performing BitLocker Management with MBAM](performing-bitlocker-management-with-mbam-mbam-2.md).</span></span>

## <a href="" id="bkmk-manatpm"></a><span data-ttu-id="1302c-124">TPM verwalten</span><span class="sxs-lookup"><span data-stu-id="1302c-124">Manage TPM</span></span>


<span data-ttu-id="1302c-125">Das Feature "TPM verwalten" der Website "Verwaltung und Überwachung" bietet Benutzern mit bestimmten Administratorrollen (beispielsweise "MBAM Helpdesk-Benutzer") Zugriff auf TPM-Daten, die vom MBAM-Client erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="1302c-125">The Manage TPM feature of the Administration and Monitoring website gives users with certain administrator roles (for example, “MBAM Helpdesk Users”) access to TPM data that has been collected by the MBAM Client.</span></span> <span data-ttu-id="1302c-126">Bei einer TPM-Sperrung kann ein Administrator die Websiteverwaltung und Überwachung verwenden, um die erforderliche Kennwortdatei abzurufen, um das TPM zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="1302c-126">In a TPM lockout, an administrator can use the Administration and Monitoring website to retrieve the necessary password file to unlock the TPM.</span></span> <span data-ttu-id="1302c-127">Anweisungen zum Zurücksetzen eines TPMs nach einer TPM-Sperrung finden Sie unter [Zurücksetzen einer TPM-Sperrung](how-to-reset-a-tpm-lockout-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="1302c-127">For instructions on how to reset a TPM after a TPM lockout, see [How to Reset a TPM Lockout](how-to-reset-a-tpm-lockout-mbam-2.md).</span></span>

## <a href="" id="bkmk-helpdesk"></a> <span data-ttu-id="1302c-128">MBAM Help Desk-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="1302c-128">MBAM Help Desk Tasks</span></span>


<span data-ttu-id="1302c-129">Sie können die Websiteverwaltung und Überwachung für viele administrative Aufgaben verwenden, beispielsweise für die Verwaltung von BitLocker-geschützter Hardware, das Recovery von Laufwerken und das Ausführen von Berichten.</span><span class="sxs-lookup"><span data-stu-id="1302c-129">You can use the Administration and Monitoring website for many administrative tasks, such as managing BitLocker-protected hardware, recovering drives, and running reports.</span></span> <span data-ttu-id="1302c-130">Standardmäßig ist die URL für die Websiteverwaltung und Überwachung http:// &lt; *MBAMAdministrationServername* &gt; , Sie können Sie aber während des Installationsvorgangs anpassen.</span><span class="sxs-lookup"><span data-stu-id="1302c-130">By default, the URL for the Administration and Monitoring website is http://&lt;*MBAMAdministrationServername*&gt;, although you can customize it during the installation process.</span></span>

<span data-ttu-id="1302c-131">**Hinweis**  Für den Zugriff auf die verschiedenen Features, die auf der Websiteverwaltung und Überwachung angeboten werden, müssen Sie über die entsprechenden Rollen verfügen, die Ihrem Benutzerkonto zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1302c-131">**Note** To access the various features offered by the Administration and Monitoring website, you must have the appropriate roles associated with your user account.</span></span> <span data-ttu-id="1302c-132">Weitere Informationen zum Grundlegendes zu Benutzerrollen finden Sie unter [Verwalten von MBAM-Administrator Rollen](how-to-manage-mbam-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="1302c-132">For more information about understanding user roles, see [How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md).</span></span>

 

<span data-ttu-id="1302c-133">Verwenden Sie die folgenden Links, um Informationen zu den Aufgaben zu finden, die Sie mithilfe der Websiteverwaltung und Überwachung ausführen können:</span><span class="sxs-lookup"><span data-stu-id="1302c-133">Use the following links to find information about the tasks that you can perform by using the Administration and Monitoring website:</span></span>

-   [<span data-ttu-id="1302c-134">So setzen Sie eine TPM-Sperre zurück</span><span class="sxs-lookup"><span data-stu-id="1302c-134">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-2.md)

-   [<span data-ttu-id="1302c-135">So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her</span><span class="sxs-lookup"><span data-stu-id="1302c-135">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

-   [<span data-ttu-id="1302c-136">So stellen Sie ein verschobenes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="1302c-136">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-2.md)

-   [<span data-ttu-id="1302c-137">So stellen Sie ein beschädigtes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="1302c-137">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-2.md)

-   [<span data-ttu-id="1302c-138">So ermitteln Sie den BitLocker-Verschlüsselungsstatus verloren gegangener Computer</span><span class="sxs-lookup"><span data-stu-id="1302c-138">How to Determine BitLocker Encryption State of Lost Computers</span></span>](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

 

 





