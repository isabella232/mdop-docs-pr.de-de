---
title: So verwenden Sie die Administration and Monitoring-Website
description: So verwenden Sie die Administration and Monitoring-Website
author: dansimp
ms.assetid: bb96a4e8-d4f4-4e6f-b7db-82d96998bfa6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b9597e29a5a7a6236cb351d8d6d1f682edce3cf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804682"
---
# <span data-ttu-id="3d863-103">So verwenden Sie die Administration and Monitoring-Website</span><span class="sxs-lookup"><span data-stu-id="3d863-103">How to Use the Administration and Monitoring Website</span></span>


<span data-ttu-id="3d863-104">Die Verwaltungs-und Überwachungs Website, auch als "Helpdesk" bezeichnet, ist eine Verwaltungsschnittstelle für die BitLocker-Laufwerkverschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="3d863-104">The Administration and Monitoring Website, also referred to as the Help Desk, is an administrative interface for BitLocker Drive Encryption.</span></span> <span data-ttu-id="3d863-105">Verwenden Sie die Website, um Berichte zu überprüfen, die Laufwerke der Endbenutzer wiederherzustellen und das TPMs der Endbenutzer zu verwalten, wie in den folgenden Abschnitten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3d863-105">Use the website to review reports, recover end users’ drives, and manage end users’ TPMs, as described in the following sections.</span></span>

<span data-ttu-id="3d863-106">**Hinweis**  Wenn Sie MBAM in der eigenständigen Topologie verwenden, werden alle Berichte auf der Website Verwaltung und Überwachung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3d863-106">**Note** If you are using MBAM in the Stand-alone topology, you view all reports from the Administration and Monitoring Website.</span></span> <span data-ttu-id="3d863-107">Wenn Sie die Configuration Manager-Integrations Topologie verwenden, werden alle Berichte in Configuration Manager mit Ausnahme des Wiederherstellungs Überwachungsberichts angezeigt, den Sie auf der Website Verwaltung und Überwachung weiter anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3d863-107">If you are using the Configuration Manager Integration topology, you view all reports in Configuration Manager, except the Recovery Audit report, which you continue to view from the Administration and Monitoring Website.</span></span> <span data-ttu-id="3d863-108">Weitere Informationen zu Berichten finden Sie unter über [wachen und melden von BitLocker-Konformität mit MBAM 2,5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="3d863-108">For more information about reports, see [Monitoring and Reporting BitLocker Compliance with MBAM 2.5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md).</span></span>

 

## <span data-ttu-id="3d863-109">Erforderliche Rollen für die Verwendung der Website "Verwaltung und Überwachung"</span><span class="sxs-lookup"><span data-stu-id="3d863-109">Required roles for using the Administration and Monitoring Website</span></span>


<span data-ttu-id="3d863-110">Wenn Sie auf bestimmte Bereiche der Verwaltungs-und Überwachungs Website zugreifen möchten, müssen Sie über eine der folgenden Rollen verfügen, bei denen es sich um Gruppen handelt, die Sie in Active Directory erstellen.</span><span class="sxs-lookup"><span data-stu-id="3d863-110">To access specific areas of the Administration and Monitoring Website, you must have one of the following roles, which are groups that you create in Active Directory.</span></span> <span data-ttu-id="3d863-111">Sie können einen beliebigen Namen für diese Gruppen verwenden.</span><span class="sxs-lookup"><span data-stu-id="3d863-111">You can use any name for these groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3d863-112">Account</span><span class="sxs-lookup"><span data-stu-id="3d863-112">Account</span></span></th>
<th align="left"><span data-ttu-id="3d863-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d863-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d863-114">MBAM Advanced Helpdesk-Benutzer</span><span class="sxs-lookup"><span data-stu-id="3d863-114">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d863-115">Bietet Zugriff auf alle Bereiche der Verwaltungs-und Überwachungs Website.</span><span class="sxs-lookup"><span data-stu-id="3d863-115">Provides access to all areas of the Administration and Monitoring Website.</span></span> <span data-ttu-id="3d863-116">Benutzer, die über diese Rolle verfügen, geben nur den Wiederherstellungsschlüssel und nicht die Domäne und den Benutzernamen des Endbenutzers ein, wenn Sie den Endbenutzern helfen, Ihre Laufwerke wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="3d863-116">Users who have this role enter only the recovery key, and not the end user’s domain and user name, when helping end users recover their drives.</span></span> <span data-ttu-id="3d863-117">Wenn ein Benutzer ein Mitglied der Gruppe MBAM Helpdesk-Benutzer und der Gruppe der erweiterten Helpdesk-Benutzer von MBAM ist, überschreiben die Berechtigungen des erweiterten Helpdesk-Benutzers von MBAM die Berechtigungen für die MBAM Helpdesk-Benutzergruppe.</span><span class="sxs-lookup"><span data-stu-id="3d863-117">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Users Group permissions.</span></span></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d863-118">MBAM Helpdesk-Benutzer</span><span class="sxs-lookup"><span data-stu-id="3d863-118">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d863-119">Bietet Zugriff auf die Bereiche Manage TPM und Drive Recovery der Verwaltungs-und Überwachungs Website.</span><span class="sxs-lookup"><span data-stu-id="3d863-119">Provides access to the Manage TPM and Drive Recovery areas of the Administration and Monitoring Website.</span></span> <span data-ttu-id="3d863-120">Personen, die über diese Rolle verfügen, müssen alle Felder ausfüllen, einschließlich der Domäne und des Kontonamens des Endbenutzers, wenn beide Bereiche verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d863-120">Individuals who have this role must fill in all fields, including the end-user’s domain and account name, when they use either area.</span></span></p>
<p><span data-ttu-id="3d863-121">Wenn ein Benutzer ein Mitglied der Gruppe MBAM Helpdesk-Benutzer und der Gruppe der erweiterten Helpdesk-Benutzer von MBAM ist, überschreiben die Berechtigungen des erweiterten Helpdesk-Benutzers von MBAM die Berechtigungen für die MBAM Helpdesk-Benutzergruppe.</span><span class="sxs-lookup"><span data-stu-id="3d863-121">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Users Group permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d863-122">MBAM-Berichtsbenutzer</span><span class="sxs-lookup"><span data-stu-id="3d863-122">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d863-123">Bietet Zugriff auf die Berichte im Bereich "Berichte" auf <strong> </strong> der Website Verwaltung und Überwachung.</span><span class="sxs-lookup"><span data-stu-id="3d863-123">Provides access to the reports in the <strong>Reports</strong> area of the Administration and Monitoring Website.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="3d863-124">Aufgaben, die auf der Website "Verwaltung und Überwachung" ausgeführt werden können</span><span class="sxs-lookup"><span data-stu-id="3d863-124">Tasks you can perform on the Administration and Monitoring Website</span></span>


<span data-ttu-id="3d863-125">In der folgenden Tabelle sind die Aufgaben aufgeführt, die Sie auf der Website Verwaltung und Überwachung ausführen können, und es werden Links zu weiteren Informationen zu den einzelnen Aufgaben bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3d863-125">The following table summarizes the tasks you can perform on the Administration and Monitoring Website and provides links to more information about each task.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3d863-126">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="3d863-126">Task</span></span></th>
<th align="left"><span data-ttu-id="3d863-127">Bereich der Website, auf den Sie auf die Aufgabe zugreifen</span><span class="sxs-lookup"><span data-stu-id="3d863-127">Area of the Website where you access the task</span></span></th>
<th align="left"><span data-ttu-id="3d863-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d863-128">Description</span></span></th>
<th align="left"><span data-ttu-id="3d863-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3d863-129">For more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d863-130">Anzeigen von Berichten</span><span class="sxs-lookup"><span data-stu-id="3d863-130">View reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d863-131">Berichte</span><span class="sxs-lookup"><span data-stu-id="3d863-131">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d863-132">Ermöglicht Ihnen das Ausführen von Berichten zum Überwachen der BitLocker-Nutzung,-Compliance und-Wiederherstellungs Aktivität.</span><span class="sxs-lookup"><span data-stu-id="3d863-132">Enables you to run reports to monitor BitLocker usage, compliance, and key recovery activity.</span></span> <span data-ttu-id="3d863-133">Berichte liefern Daten zur Unternehmenskonformität, zu einzelnen Computern und zur Anforderung von Wiederherstellungsschlüsseln oder zum TPM-OwnerAuth-Paket für einen bestimmten Computer.</span><span class="sxs-lookup"><span data-stu-id="3d863-133">Reports provide data about enterprise compliance, individual computers, and who requested recovery keys or the TPM OwnerAuth package for a specific computer.</span></span></p></td>
<td align="left"><p><a href="viewing-mbam-25-reports-for-the-stand-alone-topology.md" data-raw-source="[Viewing MBAM 2.5 Reports for the Stand-alone Topology](viewing-mbam-25-reports-for-the-stand-alone-topology.md)"><span data-ttu-id="3d863-134">Anzeigen von MBAM 2.5-Berichten für die eigenständige Topologie</span><span class="sxs-lookup"><span data-stu-id="3d863-134">Viewing MBAM 2.5 Reports for the Stand-alone Topology</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d863-135">Ermitteln des BitLocker-Verschlüsselungsstatus von verlorenen oder gestohlenen Computern</span><span class="sxs-lookup"><span data-stu-id="3d863-135">Determine the BitLocker encryption status of lost or stolen computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d863-136">Berichte</span><span class="sxs-lookup"><span data-stu-id="3d863-136">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d863-137">Ermitteln Sie, ob ein Volume verschlüsselt wurde, wenn der Computer verloren geht oder gestohlen wurde.</span><span class="sxs-lookup"><span data-stu-id="3d863-137">Determine if a volume was encrypted if the computer is lost or stolen.</span></span></p></td>
<td align="left"><p><a href="how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md" data-raw-source="[How to Determine BitLocker Encryption State of Lost Computers](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)"><span data-ttu-id="3d863-138">So ermitteln Sie den BitLocker-Verschlüsselungsstatus verloren gegangener Computer</span><span class="sxs-lookup"><span data-stu-id="3d863-138">How to Determine BitLocker Encryption State of Lost Computers</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d863-139">Wiederherstellen verlorener Laufwerke</span><span class="sxs-lookup"><span data-stu-id="3d863-139">Recover lost drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d863-140">Laufwerk Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="3d863-140">Drive Recovery</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d863-141">Wiederherstellen von Laufwerken, die:</span><span class="sxs-lookup"><span data-stu-id="3d863-141">Recover drives that are:</span></span></p>
<ul>
<li><p><span data-ttu-id="3d863-142">Im Wiederherstellungsmodus</span><span class="sxs-lookup"><span data-stu-id="3d863-142">In recovery mode</span></span></p></li>
<li><p><span data-ttu-id="3d863-143">Wurden verschoben</span><span class="sxs-lookup"><span data-stu-id="3d863-143">Have been moved</span></span></p></li>
<li><p><span data-ttu-id="3d863-144">Sind beschädigt</span><span class="sxs-lookup"><span data-stu-id="3d863-144">Are corrupted</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><a href="how-to-recover-a-drive-in-recovery-mode-mbam-25.md" data-raw-source="[How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)"><span data-ttu-id="3d863-145">So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her</span><span class="sxs-lookup"><span data-stu-id="3d863-145">How to Recover a Drive in Recovery Mode</span></span></a></p></li>
<li><p><a href="how-to-recover-a-moved-drive-mbam-25.md" data-raw-source="[How to Recover a Moved Drive](how-to-recover-a-moved-drive-mbam-25.md)"><span data-ttu-id="3d863-146">So stellen Sie ein verschobenes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="3d863-146">How to Recover a Moved Drive</span></span></a></p></li>
<li><p><a href="how-to-recover-a-corrupted-drive-mbam-25.md" data-raw-source="[How to Recover a Corrupted Drive](how-to-recover-a-corrupted-drive-mbam-25.md)"><span data-ttu-id="3d863-147">So stellen Sie ein beschädigtes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="3d863-147">How to Recover a Corrupted Drive</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d863-148">Zurücksetzen einer TPM-Sperrung</span><span class="sxs-lookup"><span data-stu-id="3d863-148">Reset a TPM lockout</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d863-149">TPM verwalten</span><span class="sxs-lookup"><span data-stu-id="3d863-149">Manage TPM</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d863-150">Bietet Zugriff auf TPM-Daten, die vom MBAM-Client erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="3d863-150">Provides access to TPM data that has been collected by the MBAM Client.</span></span> <span data-ttu-id="3d863-151">Verwenden Sie in einer TPM-Sperrung die Website Verwaltung und überwachen, um die erforderliche Kennwortdatei zum Entsperren des TPMs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3d863-151">In a TPM lockout, use the Administration and Monitoring Website to retrieve the necessary password file to unlock the TPM.</span></span></p></td>
<td align="left"><p><a href="how-to-reset-a-tpm-lockout-mbam-25.md" data-raw-source="[How to Reset a TPM Lockout](how-to-reset-a-tpm-lockout-mbam-25.md)"><span data-ttu-id="3d863-152">So setzen Sie eine TPM-Sperre zurück</span><span class="sxs-lookup"><span data-stu-id="3d863-152">How to Reset a TPM Lockout</span></span></a></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="3d863-153">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3d863-153">Related topics</span></span>


[<span data-ttu-id="3d863-154">Durchführen der BitLocker-Verwaltung mit MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="3d863-154">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 

## <span data-ttu-id="3d863-155">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="3d863-155">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="3d863-156">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="3d863-156">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="3d863-157">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="3d863-157">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





