---
title: Planen der Gruppen und Konten für MBAM 2.5
description: Planen der Gruppen und Konten für MBAM 2.5
author: dansimp
ms.assetid: 73bb9fe5-5900-4b6f-b271-ade62991fca1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 3431c3602685a4f96cb4c1333700107ba9c38b96
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811374"
---
# <span data-ttu-id="7e993-103">Planen der Gruppen und Konten für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="7e993-103">Planning for MBAM 2.5 Groups and Accounts</span></span>


<span data-ttu-id="7e993-104">In diesem Thema sind die Rollen und Konten aufgeführt, die Sie in Active Directory-Domänendiensten (AD DS) erstellen müssen, um Sicherheits-und Zugriffsrechte für die Microsoft BitLocker-Datenbanken,-Berichte und-Webanwendungen (MBAM) bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7e993-104">This topic lists the roles and accounts that you must create in Active Directory Domain Services (AD DS) to provide security and access rights for the Microsoft BitLocker Administration and Monitoring (MBAM) databases, reports, and web applications.</span></span> <span data-ttu-id="7e993-105">Für jede Rolle und jedes Konto wird das entsprechende Feld im MBAM-Serverkonfigurations-Assistenten bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7e993-105">For each role and account, the corresponding field in the MBAM Server Configuration wizard is provided.</span></span> <span data-ttu-id="7e993-106">Eine Liste der Windows PowerShell-Cmdlets und-Parameter, die diesen Konten entsprechen, finden Sie unter [Konfigurieren von MBAM 2,5-Server Features mithilfe von Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md#bkmk-reqd-posh-accts).</span><span class="sxs-lookup"><span data-stu-id="7e993-106">For a list of Windows PowerShell cmdlets and parameters that correspond to these accounts, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md#bkmk-reqd-posh-accts).</span></span>

**<span data-ttu-id="7e993-107">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="7e993-107">Note</span></span>**  
<span data-ttu-id="7e993-108">MBAM unterstützt nicht die Verwendung von verwalteten Dienstkonten.</span><span class="sxs-lookup"><span data-stu-id="7e993-108">MBAM does not support the use of managed service accounts.</span></span>



## <span data-ttu-id="7e993-109">Daten Bankkonten</span><span class="sxs-lookup"><span data-stu-id="7e993-109">Database accounts</span></span>


<span data-ttu-id="7e993-110">Erstellen Sie die folgenden Konten für die Compliance-und Überwachungsdatenbank sowie die Wiederherstellungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="7e993-110">Create the following accounts for the Compliance and Audit Database and the Recovery Database.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7e993-111">Name und Zweck des Kontos</span><span class="sxs-lookup"><span data-stu-id="7e993-111">Account name and purpose</span></span></th>
<th align="left"><span data-ttu-id="7e993-112">Kontotyp</span><span class="sxs-lookup"><span data-stu-id="7e993-112">Account type</span></span></th>
<th align="left"><span data-ttu-id="7e993-113">MBAM-Serverkonfigurations-Assistent-Feld, das diesem Konto entspricht</span><span class="sxs-lookup"><span data-stu-id="7e993-113">MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
<th align="left"><span data-ttu-id="7e993-114">Beschreibung des MBAM-Serverkonfigurations-Assistenten Felds, das diesem Konto entspricht</span><span class="sxs-lookup"><span data-stu-id="7e993-114">Description of the MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7e993-115">Konformitäts-und Überwachungsdatenbank-und Wiederherstellungsdatenbank, Benutzer oder Gruppe für Berichte lesen/schreiben</span><span class="sxs-lookup"><span data-stu-id="7e993-115">Compliance and Audit Database and Recovery Database read/write user or group for reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-116">Benutzer oder Gruppe</span><span class="sxs-lookup"><span data-stu-id="7e993-116">User or Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-117">Lese/Schreib-Zugriffsdomänen Benutzer oder-Gruppe</span><span class="sxs-lookup"><span data-stu-id="7e993-117">Read/write access domain user or group</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-118">Domänenbenutzer oder-Gruppe mit Lese-/Schreibzugriff auf die Datenbank für Konformitäts-und Überwachungsdaten und die Wiederherstellungsdatenbank, damit die Webanwendungen auf die Daten und Berichte in diesen Datenbanken zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="7e993-118">Domain user or group that has read/write access to the Compliance and Audit Database and the Recovery Database to enable the web applications to access the data and reports in these databases.</span></span></p>
<p><span data-ttu-id="7e993-119">Wenn Sie einen Benutzernamen in dieses Feld eingeben, muss er mit dem Wert im <strong> Feld "Domain-Konto" des Webdienst-Anwendungspools </strong> auf der <strong> Seite "Webanwendungen konfigurieren </strong> " identisch sein.</span><span class="sxs-lookup"><span data-stu-id="7e993-119">If you enter a user name in this field, it must be the same value as the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page.</span></span></p>
<p><span data-ttu-id="7e993-120">Wenn Sie einen Gruppennamen in dieses Feld eingeben, muss der Wert im <strong> Feld "Webdienst-Anwendungspool Domäne" </strong> auf der <strong> Seite "Webanwendungen konfigurieren" </strong> ein Mitglied der Gruppe sein, die Sie in dieses Feld eingeben.</span><span class="sxs-lookup"><span data-stu-id="7e993-120">If you enter a group name in this field, the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page must be a member of the group you enter in this field.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7e993-121">Konformitäts-und Überwachungsdatenbank – schreibgeschützter Benutzer oder Gruppe für Berichte</span><span class="sxs-lookup"><span data-stu-id="7e993-121">Compliance and Audit Database read-only user or group for reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-122">Benutzer oder Gruppe</span><span class="sxs-lookup"><span data-stu-id="7e993-122">User or Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-123">Schreibgeschützter Zugriffsdomänen Benutzer oder-Gruppe</span><span class="sxs-lookup"><span data-stu-id="7e993-123">Read-only access domain user or group</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-124">Der Name des Benutzers oder der Gruppe, der schreibgeschützten Zugriff auf die Compliance-und Überwachungsdatenbank hat, damit die Berichte Zugriff auf die Compliance-und Überwachungsdaten in dieser Datenbank erhalten.</span><span class="sxs-lookup"><span data-stu-id="7e993-124">Name of the user or group that will have read-only access to the Compliance and Audit Database to enable the reports to access the compliance and audit data in this database.</span></span></p>
<p><span data-ttu-id="7e993-125">Wenn Sie einen Benutzernamen in dieses Feld eingeben, muss er derselbe Benutzer sein, den Sie im <strong> Feld Compliance und Audit Database Domain Account </strong> auf der <strong> Seite "Berichte konfigurieren" angeben </strong> .</span><span class="sxs-lookup"><span data-stu-id="7e993-125">If you enter a user name in this field, it must be the same user as the one you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page.</span></span></p>
<p><span data-ttu-id="7e993-126">Wenn Sie einen Gruppennamen in dieses Feld eingeben, muss der Wert, den Sie im <strong> Feld Compliance und Audit Database Domain Account angeben, </strong> auf der <strong> Seite "Berichte konfigurieren" </strong> ein Mitglied der Gruppe sein, die Sie in diesem Feld angeben.</span><span class="sxs-lookup"><span data-stu-id="7e993-126">If you enter a group name in this field, the value that you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page must be a member of the group that you specify in this field.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="7e993-127">Berichterstellungskonten</span><span class="sxs-lookup"><span data-stu-id="7e993-127">Reporting accounts</span></span>


<span data-ttu-id="7e993-128">Erstellen Sie die folgenden Konten für das Feature Berichte.</span><span class="sxs-lookup"><span data-stu-id="7e993-128">Create the following accounts for the Reports feature.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7e993-129">Kontoname/Zweck</span><span class="sxs-lookup"><span data-stu-id="7e993-129">Account name/purpose</span></span></th>
<th align="left"><span data-ttu-id="7e993-130">Kontotyp</span><span class="sxs-lookup"><span data-stu-id="7e993-130">Account type</span></span></th>
<th align="left"><span data-ttu-id="7e993-131">MBAM-Serverkonfigurations-Assistent-Feld, das diesem Konto entspricht</span><span class="sxs-lookup"><span data-stu-id="7e993-131">MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
<th align="left"><span data-ttu-id="7e993-132">Beschreibung des MBAM-Serverkonfigurations-Assistenten Felds, das diesem Konto entspricht</span><span class="sxs-lookup"><span data-stu-id="7e993-132">Description of the MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7e993-133">Meldet schreibgeschützte Domänenzugriffs Gruppe</span><span class="sxs-lookup"><span data-stu-id="7e993-133">Reports read-only domain access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-134">Gruppe</span><span class="sxs-lookup"><span data-stu-id="7e993-134">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-135">Gruppe "Berichtsrolle-Domäne"</span><span class="sxs-lookup"><span data-stu-id="7e993-135">Reporting role domain group</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-136">Gibt die Domänenbenutzergruppe an, die schreibgeschützten Zugriff auf die Berichte auf der Website Verwaltung und Überwachung hat.</span><span class="sxs-lookup"><span data-stu-id="7e993-136">Specifies the domain user group that has read-only access to the reports in the Administration and Monitoring Website.</span></span> <span data-ttu-id="7e993-137">Die von Ihnen angegebene Gruppe muss dieselbe Gruppe sein, die Sie für den Gruppenparameter schreibgeschützter Zugriff für Berichte angegeben haben, wenn die Web-Apps aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="7e993-137">The group you specify must be the same group you specified for the Reports Read Only Access Group parameter when the web apps are enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7e993-138">Kompatibilitäts-und Überwachungsdatenbank-Domänenbenutzerkonto</span><span class="sxs-lookup"><span data-stu-id="7e993-138">Compliance and Audit Database domain user account</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-139">Benutzer</span><span class="sxs-lookup"><span data-stu-id="7e993-139">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-140">Compliance-und Audit-Daten Bank Domänenkonto</span><span class="sxs-lookup"><span data-stu-id="7e993-140">Compliance and Audit Database domain account</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-141">Domänenbenutzerkonto und Kennwort, das von der lokalen SQL Server Reporting Services-Instanz für den Zugriff auf die Compliance-und Überwachungsdatenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7e993-141">Domain user account and password that the local SQL Server Reporting Services instance uses to access the Compliance and Audit Database.</span></span> <span data-ttu-id="7e993-142">Für dieses Konto ist <strong> die Anmeldung als Batch </strong> Berechtigung für den SQL Server Reporting Services-Server erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7e993-142">This account requires <strong>Log On as Batch</strong> rights to the SQL Server Reporting Services server.</span></span></p>
<p><span data-ttu-id="7e993-143">Wenn der Wert, den Sie in das <strong> Feld "Schreibgeschützter Zugriffsdomänen Benutzer" oder "Gruppe" </strong> auf der <strong> Seite "Datenbanken konfigurieren </strong> " eingeben, ein Benutzername ist, müssen Sie diesen Wert in dieses Feld eingeben.</span><span class="sxs-lookup"><span data-stu-id="7e993-143">If the value you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a user name, you must enter that same value in this field.</span></span></p>
<p><span data-ttu-id="7e993-144">Wenn der Wert, den Sie in das <strong> Feld "Schreibgeschützter Zugriffsdomänen Benutzer" oder "Gruppe" </strong> auf der <strong> Seite "Datenbanken konfigurieren" eingeben </strong> , ein Gruppenname ist, muss der Wert, den Sie in dieses Feld eingeben, Mitglied dieser Gruppe sein.</span><span class="sxs-lookup"><span data-stu-id="7e993-144">If the value you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a group name, the value that you enter in this field must be a member of that group.</span></span></p>
<p><span data-ttu-id="7e993-145">Konfigurieren Sie das Kennwort für dieses Konto so, dass es nie abläuft.</span><span class="sxs-lookup"><span data-stu-id="7e993-145">Configure the password for this account to never expire.</span></span> <span data-ttu-id="7e993-146">Das Benutzerkonto sollte auf alle Daten zugreifen können, die für die Gruppe MBAM-Berichte Benutzer verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7e993-146">The user account should be able to access all data that is available to the MBAM Reports Users group.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-helpdesk-roles"></a><span data-ttu-id="7e993-147">Verwaltungs-und Überwachungs Website (Help Desk)-Konten</span><span class="sxs-lookup"><span data-stu-id="7e993-147">Administration and Monitoring Website (Help Desk) accounts</span></span>


<span data-ttu-id="7e993-148">Erstellen Sie die folgenden Konten für die Website Verwaltung und Überwachung.</span><span class="sxs-lookup"><span data-stu-id="7e993-148">Create the following accounts for the Administration and Monitoring Website.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7e993-149">Kontoname/Zweck</span><span class="sxs-lookup"><span data-stu-id="7e993-149">Account name/purpose</span></span></th>
<th align="left"><span data-ttu-id="7e993-150">Kontotyp</span><span class="sxs-lookup"><span data-stu-id="7e993-150">Account type</span></span></th>
<th align="left"><span data-ttu-id="7e993-151">MBAM-Serverkonfigurations-Assistent-Feld, das diesem Konto entspricht</span><span class="sxs-lookup"><span data-stu-id="7e993-151">MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
<th align="left"><span data-ttu-id="7e993-152">Beschreibung des MBAM-Serverkonfigurations-Assistenten Felds, das diesem Konto entspricht</span><span class="sxs-lookup"><span data-stu-id="7e993-152">Description of the MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7e993-153">Domänenkonto des Webdienst-Anwendungspools</span><span class="sxs-lookup"><span data-stu-id="7e993-153">Web service application pool domain account</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-154">Benutzer</span><span class="sxs-lookup"><span data-stu-id="7e993-154">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-155">Domänenkonto des Webdienst-Anwendungspools</span><span class="sxs-lookup"><span data-stu-id="7e993-155">Web service application pool domain account</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-156">Das Domänenbenutzerkonto, das vom Anwendungspool für die Webanwendungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e993-156">Domain user account to be used by the application pool for the web applications.</span></span></p>
<p><span data-ttu-id="7e993-157">Wenn Sie einen Benutzernamen in das <strong> Feld Lese/Schreibzugriff-Domänenbenutzer oder-Gruppe </strong> auf der <strong> Seite Datenbanken konfigurieren eingeben </strong> , müssen Sie diesen Wert in dieses Feld eingeben.</span><span class="sxs-lookup"><span data-stu-id="7e993-157">If you enter a user name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, you must enter that same value in this field.</span></span></p>
<p><span data-ttu-id="7e993-158">Wenn Sie einen Gruppennamen in das <strong> Feld Lese-/Schreibzugriff-Domänenbenutzer oder-Gruppe </strong> auf der <strong> Seite Datenbanken konfigurieren eingeben </strong> , muss der in dieses Feld eingegebene Wert ein Mitglied dieser Gruppe sein.</span><span class="sxs-lookup"><span data-stu-id="7e993-158">If you enter a group name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, the value you enter in this field must be a member of that group.</span></span></p>
<p><span data-ttu-id="7e993-159">Wenn Sie keine Anmeldeinformationen angeben, werden die Anmeldeinformationen verwendet, die für eine zuvor aktivierte Webanwendung angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="7e993-159">If you do not specify credentials, the credentials that were specified for any previously enabled web application will be used.</span></span> <span data-ttu-id="7e993-160">Alle Webanwendungen müssen die gleichen Anmeldeinformationen für den Anwendungspool verwenden.</span><span class="sxs-lookup"><span data-stu-id="7e993-160">All web applications must use the same application pool credentials.</span></span> <span data-ttu-id="7e993-161">Wenn Sie für verschiedene Webanwendungen unterschiedliche Anmeldeinformationen angeben, wird der zuletzt angegebene Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="7e993-161">If you specify different credentials for different web applications, the most recently specified value will be used.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="7e993-162">Wichtig</span><span class="sxs-lookup"><span data-stu-id="7e993-162">Important</span></span></strong><br/><p><span data-ttu-id="7e993-163">Um die Sicherheit zu verbessern, legen Sie das in den Anmeldeinformationen angegebene Konto auf begrenzte Benutzerrechte fest.</span><span class="sxs-lookup"><span data-stu-id="7e993-163">For improved security, set the account that is specified in the credentials to have limited user rights.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7e993-164">MBAM Advanced Helpdesk users Access Group</span><span class="sxs-lookup"><span data-stu-id="7e993-164">MBAM Advanced Helpdesk Users access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-165">Gruppe</span><span class="sxs-lookup"><span data-stu-id="7e993-165">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-166">MBAM Advanced Helpdesk-Benutzer</span><span class="sxs-lookup"><span data-stu-id="7e993-166">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-167">Domänenbenutzergruppe, deren Mitglieder Zugriff auf alle Wiederherstellungs Bereiche der Website "Verwaltung und Überwachung" haben.</span><span class="sxs-lookup"><span data-stu-id="7e993-167">Domain user group whose members have access to all recovery areas of the Administration and Monitoring Website.</span></span> <span data-ttu-id="7e993-168">Benutzer, die über diese Rolle verfügen, müssen nur den Wiederherstellungsschlüssel und nicht die Domäne und den Benutzernamen des Endbenutzers eingeben, wenn Sie den Endbenutzern helfen, Ihre Laufwerke wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="7e993-168">Users who have this role have to enter only the recovery key, and not the end user’s domain and user name, when helping end users recover their drives.</span></span> <span data-ttu-id="7e993-169">Wenn ein Benutzer ein Mitglied der Gruppe MBAM Helpdesk-Benutzer und der Gruppe der erweiterten Helpdesk-Benutzer von MBAM ist, überschreiben die Berechtigungen der Gruppe erweiterte Helpdesk-Benutzer MBAM die Berechtigungen für die MBAM-Helpdesk-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="7e993-169">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Group permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7e993-170">MBAM Helpdesk-Benutzerzugriffs Gruppe</span><span class="sxs-lookup"><span data-stu-id="7e993-170">MBAM Helpdesk Users access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-171">Gruppe</span><span class="sxs-lookup"><span data-stu-id="7e993-171">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-172">MBAM Helpdesk-Benutzer</span><span class="sxs-lookup"><span data-stu-id="7e993-172">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-173">Die Domänenbenutzergruppe, deren Mitglieder Zugriff auf die Bereiche "TPM verwalten" und "Laufwerk Wiederherstellung" der Website "MBAM-Verwaltung und-Überwachung" haben.</span><span class="sxs-lookup"><span data-stu-id="7e993-173">Domain user group whose members have access to the Manage TPM and Drive Recovery areas of the MBAM Administration and Monitoring Website.</span></span> <span data-ttu-id="7e993-174">Personen, die über diese Rolle verfügen, müssen alle Felder ausfüllen, einschließlich der Domäne und des Kontonamens des Endbenutzers, wenn beide Optionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e993-174">Individuals who have this role must fill-in all fields, including the end-user’s domain and account name, when they use either option.</span></span></p>
<p><span data-ttu-id="7e993-175">Wenn ein Benutzer ein Mitglied der Gruppe MBAM Helpdesk-Benutzer und der Gruppe der erweiterten Helpdesk-Benutzer von MBAM ist, überschreiben die Berechtigungen der Gruppe erweiterte Helpdesk-Benutzer MBAM die Berechtigungen für die MBAM-Helpdesk-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="7e993-175">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Group permissions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7e993-176">MBAM-Berichtsbenutzer (Access-Gruppe)</span><span class="sxs-lookup"><span data-stu-id="7e993-176">MBAM Report Users access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-177">Gruppe</span><span class="sxs-lookup"><span data-stu-id="7e993-177">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-178">MBAM-Berichtsbenutzer</span><span class="sxs-lookup"><span data-stu-id="7e993-178">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-179">Domänenbenutzergruppe, deren Mitglieder schreibgeschützten Zugriff auf die Berichte im Bereich "Berichte" der Website "Verwaltung und Überwachung" haben.</span><span class="sxs-lookup"><span data-stu-id="7e993-179">Domain user group whose members have read-only access to the reports in the Reports area of the Administration and Monitoring Website.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7e993-180">MBAM-Benutzergruppe für die Daten Migration</span><span class="sxs-lookup"><span data-stu-id="7e993-180">MBAM Data Migration User Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-181">Gruppe</span><span class="sxs-lookup"><span data-stu-id="7e993-181">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-182">Benutzer von MBAM-Daten Migration</span><span class="sxs-lookup"><span data-stu-id="7e993-182">MBAM Data Migration Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e993-183">Optionale Domänenbenutzergruppe, deren Mitglieder über die Berechtigungen zum Schreiben von Daten in MBAM verfügen, indem Sie den MBAM-Wiederherstellungs-und Hardware Dienst verwenden, der auf dem MBAM-Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7e993-183">Optional domain user group whose members have permissions to write data to MBAM by using the MBAM Recovery and Hardware Service running on the MBAM server.</span></span> <span data-ttu-id="7e993-184">Dieses Konto wird in der Regel für die Write-mbam \*-Cmdlets verwendet, um Wiederherstellungs-und TPM-Daten aus Active Directory in die mbam-Datenbank zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="7e993-184">This account is generally used with the Write-Mbam\* cmdlets to write recovery and TPM data from Active Directory into the MBAM database.</span></span></p>
<p><span data-ttu-id="7e993-185">Weitere Informationen finden Sie unter <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> Sicherheitsüberlegungen zu MBAM 2,5 </a> .</span><span class="sxs-lookup"><span data-stu-id="7e993-185">For more information, see <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">MBAM 2.5 Security Considerations</a>.</span></span></p></td>
</tr>
</tbody>
</table>




## <span data-ttu-id="7e993-186">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7e993-186">Related topics</span></span>


[<span data-ttu-id="7e993-187">Vorbereiten der Umgebung für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="7e993-187">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="7e993-188">Bereitstellungsvoraussetzungen für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="7e993-188">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)



## <span data-ttu-id="7e993-189">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="7e993-189">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="7e993-190">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="7e993-190">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="7e993-191">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="7e993-191">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





