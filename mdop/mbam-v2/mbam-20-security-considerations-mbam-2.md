---
title: Sicherheitsüberlegungen zu MBAM2.0
description: Sicherheitsüberlegungen zu MBAM2.0
author: dansimp
ms.assetid: 0aa5c6e2-d92c-4e30-9f6a-b48abb667ae5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 04dc9b667faddecab629b50f4c5d909fd7b2829e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810240"
---
# <span data-ttu-id="6df88-103">Sicherheitsüberlegungen zu MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="6df88-103">MBAM 2.0 Security Considerations</span></span>


<span data-ttu-id="6df88-104">Dieses Thema enthält eine kurze Übersicht über die Konten und Gruppen, Protokolldateien und andere sicherheitsbezogene Überlegungen für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM).</span><span class="sxs-lookup"><span data-stu-id="6df88-104">This topic contains a brief overview about the accounts and groups, log files, and other security-related considerations for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="6df88-105">Weitere Informationen finden Sie unter den Links in diesem Artikel.</span><span class="sxs-lookup"><span data-stu-id="6df88-105">For more information, follow the links within this article.</span></span>

## <span data-ttu-id="6df88-106">Allgemeine Sicherheitsüberlegungen</span><span class="sxs-lookup"><span data-stu-id="6df88-106">General Security Considerations</span></span>


**<span data-ttu-id="6df88-107">Grundlegendes zu den Sicherheitsrisiken</span><span class="sxs-lookup"><span data-stu-id="6df88-107">Understand the security risks.</span></span>** <span data-ttu-id="6df88-108">Das schwerwiegendste Risiko aus der Microsoft BitLocker-Verwaltung und-Überwachung besteht darin, dass die Funktionalität von einem nicht autorisierten Benutzer übernommen werden kann, der dann die BitLocker-Verschlüsselung neu konfigurieren und BitLocker-Verschlüsselungsschlüssel Daten auf MBAM-Clients erhalten kann.</span><span class="sxs-lookup"><span data-stu-id="6df88-108">The most serious risk from Microsoft BitLocker Administration and Monitoring is that its functionality could be hijacked by an unauthorized user who could then reconfigure BitLocker encryption and gain BitLocker encryption key data on MBAM Clients.</span></span> <span data-ttu-id="6df88-109">Der Verlust von MBAM-Funktionen für kurze Zeit aufgrund eines Denial-of-Service-Angriffs hat jedoch im Allgemeinen keine katastrophalen Auswirkungen, wie beispielsweise e-Mail, Netzwerkkommunikation, Licht und Strom.</span><span class="sxs-lookup"><span data-stu-id="6df88-109">However, the loss of MBAM functionality for a short period of time, due to a denial-of-service attack, does not generally have a catastrophic impact, unlike, for example, e-mail, network communications, light, and power.</span></span>

<span data-ttu-id="6df88-110">**Physisches sichern ihrer Computer**.</span><span class="sxs-lookup"><span data-stu-id="6df88-110">**Physically secure your computers**.</span></span> <span data-ttu-id="6df88-111">Es gibt keine Sicherheit ohne physische Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="6df88-111">There is no security without physical security.</span></span> <span data-ttu-id="6df88-112">Ein Angreifer, der physischen Zugriff auf einen MBAM-Server erhält, kann ihn potenziell zum Angriff auf die gesamte Clientbasis verwenden.</span><span class="sxs-lookup"><span data-stu-id="6df88-112">An attacker who gets physical access to an MBAM Server could potentially use it to attack the entire client base.</span></span> <span data-ttu-id="6df88-113">Alle potenziellen körperlichen Angriffe müssen als Risiko behaftet und entsprechend verringert werden.</span><span class="sxs-lookup"><span data-stu-id="6df88-113">All potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="6df88-114">MBAM-Server sollten in einem sicheren Serverraum mit kontrolliertem Zugriff gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="6df88-114">MBAM servers should be stored in a secure server room with controlled access.</span></span> <span data-ttu-id="6df88-115">Sichern Sie diese Computer, wenn Administratoren physisch nicht anwesend sind, indem Sie das Betriebssystem sperren oder einen sicheren Bildschirmschoner verwenden.</span><span class="sxs-lookup"><span data-stu-id="6df88-115">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="6df88-116">**Wenden Sie die neuesten Sicherheitsupdates auf alle Computer an**.</span><span class="sxs-lookup"><span data-stu-id="6df88-116">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="6df88-117">Informieren Sie sich über neue Updates für Betriebssysteme, Microsoft SQL Server und MBAM, indem Sie den Security Notification Service ( <https://go.microsoft.com/fwlink/?LinkId=28819> ) abonnieren.</span><span class="sxs-lookup"><span data-stu-id="6df88-117">Stay informed about new updates for operating systems, Microsoft SQL Server, and MBAM by subscribing to the Security Notification service (<https://go.microsoft.com/fwlink/?LinkId=28819>).</span></span>

<span data-ttu-id="6df88-118">**Verwenden Sie sichere Kennwörter oder Passphrasen**.</span><span class="sxs-lookup"><span data-stu-id="6df88-118">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="6df88-119">Verwenden Sie immer starke Kennwörter mit 15 oder mehr Zeichen für alle MBAM-und MBAM-Administratorkonten.</span><span class="sxs-lookup"><span data-stu-id="6df88-119">Always use strong passwords with 15 or more characters for all MBAM and MBAM administrator accounts.</span></span> <span data-ttu-id="6df88-120">Verwenden Sie niemals leere Kennwörter.</span><span class="sxs-lookup"><span data-stu-id="6df88-120">Never use blank passwords.</span></span> <span data-ttu-id="6df88-121">Weitere Informationen zu Kenn Wort Konzepten finden Sie im Whitepaper "Kontokennwörter und-Richtlinien" auf TechNet ( <https://go.microsoft.com/fwlink/?LinkId=30009> ).</span><span class="sxs-lookup"><span data-stu-id="6df88-121">For more information about password concepts, see the “Account Passwords and Policies” white paper on TechNet (<https://go.microsoft.com/fwlink/?LinkId=30009>).</span></span>

## <span data-ttu-id="6df88-122">Konten und Gruppen in MBAM</span><span class="sxs-lookup"><span data-stu-id="6df88-122">Accounts and Groups in MBAM</span></span>


<span data-ttu-id="6df88-123">Die bewährte Methode zum Verwalten von Benutzerkonten ist das Erstellen globaler Domänengruppen und das Hinzufügen von Benutzerkonten.</span><span class="sxs-lookup"><span data-stu-id="6df88-123">The best practice for managing user accounts is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="6df88-124">Fügen Sie dann die globalen Domänenkonten den erforderlichen lokalen MBAM-Gruppen auf den MBAM-Servern hinzu.</span><span class="sxs-lookup"><span data-stu-id="6df88-124">Then, add the domain global accounts to the necessary MBAM local groups on the MBAM Servers.</span></span>

### <span data-ttu-id="6df88-125">ActiveDirectoryDomainServices-Gruppen</span><span class="sxs-lookup"><span data-stu-id="6df88-125">ActiveDirectoryDomainServices Groups</span></span>

<span data-ttu-id="6df88-126">Während des MBAM-Setupprozesses werden keine Active Directory-Gruppen automatisch erstellt.</span><span class="sxs-lookup"><span data-stu-id="6df88-126">No Active Directory groups are created automatically during the MBAM setup process.</span></span> <span data-ttu-id="6df88-127">Es wird jedoch empfohlen, dass Sie die folgenden globalen ActiveDirectoryDomainServices-Gruppen erstellen, um MBAM-Vorgänge zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="6df88-127">However, it is recommended that you create the following ActiveDirectoryDomainServices global groups to manage MBAM operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6df88-128">Gruppenname</span><span class="sxs-lookup"><span data-stu-id="6df88-128">Group Name</span></span></th>
<th align="left"><span data-ttu-id="6df88-129">Details</span><span class="sxs-lookup"><span data-stu-id="6df88-129">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6df88-130">MBAM Advanced Helpdesk-Benutzer</span><span class="sxs-lookup"><span data-stu-id="6df88-130">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6df88-131">Diese Gruppe erstellen, um Mitglieder der lokalen Gruppe MBAM Advanced Helpdesk-Benutzer zu verwalten, die während des MBAM-Setups erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6df88-131">Create this group to manage members of the MBAM Advanced Helpdesk Users local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6df88-132">MBAM Compliance Auditing DB Access</span><span class="sxs-lookup"><span data-stu-id="6df88-132">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="6df88-133">Diese Gruppe erstellen, um die Mitglieder der MBAM-Konformitätsprüfung zu verwalten, die beim MBAM-Setup erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6df88-133">Create this group to manage members of the MBAM Compliance Auditing DB Access local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6df88-134">MBAM Helpdesk-Benutzer</span><span class="sxs-lookup"><span data-stu-id="6df88-134">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6df88-135">Diese Gruppe erstellen, um Mitglieder der lokalen Gruppe MBAM Helpdesk-Benutzer zu verwalten, die während des MBAM-Setups erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6df88-135">Create this group to manage members of the MBAM Helpdesk Users local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6df88-136">MBAM Recovery-und Hardware-DB-Zugriff</span><span class="sxs-lookup"><span data-stu-id="6df88-136">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="6df88-137">Diese Gruppe erstellen, um die Mitglieder der lokalen Gruppe MBAM Recovery and Hardware DB Access zu verwalten, die während des MBAM-Setups erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6df88-137">Create this group to manage members of the MBAM Recovery and Hardware DB Access local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6df88-138">MBAM-Berichtsbenutzer</span><span class="sxs-lookup"><span data-stu-id="6df88-138">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6df88-139">Diese Gruppe erstellen, um Mitglieder der lokalen Gruppe MBAM-Berichtsbenutzer zu verwalten, die während des MBAM-Setups erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6df88-139">Create this group to manage members of the MBAM Report Users local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6df88-140">MBAM-System Administratoren</span><span class="sxs-lookup"><span data-stu-id="6df88-140">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="6df88-141">Diese Gruppe erstellen, um Mitglieder der lokalen Gruppe MBAM-System Administratoren zu verwalten, die während des MBAM-Setups erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6df88-141">Create this group to manage members of the MBAM System Administrators local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6df88-142">Ausnahmen für BitLocker-Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="6df88-142">BitLocker Encryption Exemptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="6df88-143">Erstellen Sie diese Gruppe zum Verwalten von Benutzerkonten, die von der BitLocker-Verschlüsselung ab Computern, bei denen Sie sich anmelden, ausgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6df88-143">Create this group to manage user accounts that should be exempted from BitLocker encryption starting on computers that they log on to.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------mbam-server-local-groups"></a> <span data-ttu-id="6df88-144">Lokale MBAM-Server Gruppen</span><span class="sxs-lookup"><span data-stu-id="6df88-144">MBAM Server Local Groups</span></span>

<span data-ttu-id="6df88-145">MBAM Setup erstellt lokale Gruppen, um MBAM-Vorgänge zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6df88-145">MBAM Setup creates local groups to support MBAM operations.</span></span> <span data-ttu-id="6df88-146">Sie sollten die globalen ActiveDirectoryDomainServices-Gruppen den entsprechenden lokalen MBAM-Gruppen hinzufügen, um MBAM-Sicherheits-und Datenzugriffsberechtigungen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="6df88-146">You should add the ActiveDirectoryDomainServices global groups to the appropriate MBAM local groups to configure MBAM security and data access permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6df88-147">Gruppenname</span><span class="sxs-lookup"><span data-stu-id="6df88-147">Group Name</span></span></th>
<th align="left"><span data-ttu-id="6df88-148">Details</span><span class="sxs-lookup"><span data-stu-id="6df88-148">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6df88-149">MBAM Advanced Helpdesk-Benutzer</span><span class="sxs-lookup"><span data-stu-id="6df88-149">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6df88-150">Mitglieder dieser Gruppe haben erhöhten Zugriff auf die Helpdesk-Features von MBAM.</span><span class="sxs-lookup"><span data-stu-id="6df88-150">Members of this group have increased access to the Help Desk features from MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6df88-151">MBAM Compliance Auditing DB Access</span><span class="sxs-lookup"><span data-stu-id="6df88-151">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="6df88-152">Enthält die Computer, die Zugriff auf die MBAM-Konformitäts-und Überwachungsdatenbank haben.</span><span class="sxs-lookup"><span data-stu-id="6df88-152">Contains the machines that have access to the MBAM Compliance and Auditing Database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6df88-153">MBAM Helpdesk-Benutzer</span><span class="sxs-lookup"><span data-stu-id="6df88-153">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6df88-154">Mitglieder dieser Gruppe können auf einige der Helpdesk-Features von MBAM zugreifen.</span><span class="sxs-lookup"><span data-stu-id="6df88-154">Members of this group have access to some of the Help Desk features from MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6df88-155">MBAM Recovery-und Hardware-DB-Zugriff</span><span class="sxs-lookup"><span data-stu-id="6df88-155">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="6df88-156">Enthält die Computer, die Zugriff auf die MBAM-Wiederherstellungsdatenbank haben.</span><span class="sxs-lookup"><span data-stu-id="6df88-156">Contains the machines that have access to the MBAM Recovery Database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6df88-157">MBAM-Berichtsbenutzer</span><span class="sxs-lookup"><span data-stu-id="6df88-157">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6df88-158">Mitglieder dieser Gruppe haben Zugriff auf die Konformitäts-und Überwachungsberichte von MBAM.</span><span class="sxs-lookup"><span data-stu-id="6df88-158">Members of this group have access to the Compliance and Audit reports from MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6df88-159">MBAM-System Administratoren</span><span class="sxs-lookup"><span data-stu-id="6df88-159">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="6df88-160">Mitglieder dieser Gruppe haben Zugriff auf alle MBAM-Features.</span><span class="sxs-lookup"><span data-stu-id="6df88-160">Members of this group have access to all MBAM features.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="6df88-161">SSRS-Berichtsdienst Konto</span><span class="sxs-lookup"><span data-stu-id="6df88-161">SSRS Reports Service Account</span></span>

<span data-ttu-id="6df88-162">Das SSRS-Berichtsdienst Konto bietet den Sicherheitskontext zum Ausführen der MBAM-Berichte, die über SSRS zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="6df88-162">The SSRS Reports service account provides the security context to run the MBAM reports available through SSRS.</span></span> <span data-ttu-id="6df88-163">Sie wird während des MBAM-Setups konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="6df88-163">It is configured during MBAM Setup.</span></span>

<span data-ttu-id="6df88-164">Wenn Sie das SSRS-Berichtsdienst Konto konfigurieren, geben Sie ein Domänenbenutzerkonto an, und konfigurieren Sie das Kennwort so, dass es nie abläuft.</span><span class="sxs-lookup"><span data-stu-id="6df88-164">When you configure the SSRS Reports service account, specify a domain user account, and configure the password to never expire.</span></span>

<span data-ttu-id="6df88-165">**Hinweis**  Wenn Sie den Namen des Dienstkontos ändern, nachdem Sie MBAM bereitgestellt haben, müssen Sie die Berichterstellungsdaten Quelle neu konfigurieren, um die neuen Dienstkontoanmeldeinformationen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6df88-165">**Note** If you change the name of the service account after you deploy MBAM, you must reconfigure the reporting data source to use the new service account credentials.</span></span> <span data-ttu-id="6df88-166">Andernfalls können Sie nicht auf das Helpdesk-Portal zugreifen.</span><span class="sxs-lookup"><span data-stu-id="6df88-166">Otherwise, you will not be able to access the Help Desk Portal.</span></span>

 

## <a href="" id="---------mbam-log-files"></a> <span data-ttu-id="6df88-167">MBAM-Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="6df88-167">MBAM Log Files</span></span>


<span data-ttu-id="6df88-168">Die folgenden MBAM-Setupprotokolldateien werden im Ordner "% Temp%" des Installations Benutzers während des MBAM-Setups erstellt:</span><span class="sxs-lookup"><span data-stu-id="6df88-168">The following MBAM Setup log files are created in the installing user’s %temp% folder during MBAM Setup:</span></span>

**<span data-ttu-id="6df88-169">MBAM Server Setup-Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="6df88-169">MBAM Server Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="6df88-170">MSI <em> &lt; fünf zufällige Zeichen &gt; </em> . log</span><span class="sxs-lookup"><span data-stu-id="6df88-170">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="6df88-171">Protokolliert die Aktionen, die während der Installation von MBAM-Setup und der MBAM-Server Funktion ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="6df88-171">Logs the actions taken during MBAM Setup and MBAM Server Feature installation.</span></span>

<a href="" id="installcompliancedatabase-log"></a><span data-ttu-id="6df88-172">InstallComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="6df88-172">InstallComplianceDatabase.log</span></span>  
<span data-ttu-id="6df88-173">Protokolliert Aktionen, die zum Erstellen der MBAM-Konformitäts-und Überwachungsdatenbank-Einrichtung ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="6df88-173">Logs actions taken to create the MBAM Compliance and Audit Database setup.</span></span>

<a href="" id="installkeycompliancedatabase-log"></a><span data-ttu-id="6df88-174">InstallKeyComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="6df88-174">InstallKeyComplianceDatabase.log</span></span>  
<span data-ttu-id="6df88-175">Protokolliert Aktionen, die zum Erstellen der MBAM-Wiederherstellungsdatenbank ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="6df88-175">Logs actions taken to create the MBAM Recovery Database.</span></span>

<a href="" id="addhelpdeskdbauditusers-log"></a><span data-ttu-id="6df88-176">AddHelpDeskDbAuditUsers. log</span><span class="sxs-lookup"><span data-stu-id="6df88-176">AddHelpDeskDbAuditUsers.log</span></span>  
<span data-ttu-id="6df88-177">Protokolliert Aktionen zum Erstellen der SQL Server-Anmeldungen in der MBAM-Konformitäts-und Überwachungsdatenbank und Autorisieren des Helpdesk-Webdiensts für Berichte in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="6df88-177">Logs actions taken to create the SQL Server logins on the MBAM Compliance and Audit database and authorize the HelpDesk web service to the database for reports.</span></span>

<a href="" id="addhelpdeskdbusers-log"></a><span data-ttu-id="6df88-178">AddHelpDeskDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="6df88-178">AddHelpDeskDbUsers.log</span></span>  
<span data-ttu-id="6df88-179">Protokolliert Aktionen, die zum Autorisieren von Webdiensten zur Datenbank für die Schlüsselwiederherstellung und zum Erstellen von Anmeldungen in der MBAM-Wiederherstellungsdatenbank ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6df88-179">Logs actions taken to authorize web services to database for key recovery and create logins to the MBAM Recovery Database.</span></span>

<a href="" id="addkeycompliancedbusers-log"></a><span data-ttu-id="6df88-180">AddKeyComplianceDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="6df88-180">AddKeyComplianceDbUsers.log</span></span>  
<span data-ttu-id="6df88-181">Protokolliert Aktionen zum Autorisieren von Webdiensten für MBAM Compliance-und Audit-Datenbank für Compliance-Berichte.</span><span class="sxs-lookup"><span data-stu-id="6df88-181">Logs actions taken to authorize web services to MBAM Compliance and Audit Database for compliance reporting.</span></span>

<a href="" id="addrecoveryandhardwaredbusers-log"></a><span data-ttu-id="6df88-182">AddRecoveryAndHardwareDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="6df88-182">AddRecoveryAndHardwareDbUsers.log</span></span>  
<span data-ttu-id="6df88-183">Protokolliert Aktionen, die zum Autorisieren von Webdiensten zur MBAM-Wiederherstellungsdatenbank für die Schlüsselwiederherstellung ergriffen wurden.</span><span class="sxs-lookup"><span data-stu-id="6df88-183">Logs actions taken to authorize web services to the MBAM Recovery database for key recovery.</span></span>

<span data-ttu-id="6df88-184">**Hinweis**  Um zusätzliche MBAM-Setup Protokolldateien zu erhalten, müssen Sie MBAM mithilfe des msiexec-Pakets und der Option "/l &lt; Location &gt; " installieren.</span><span class="sxs-lookup"><span data-stu-id="6df88-184">**Note** In order to obtain additional MBAM Setup log files, you have to install MBAM by using the msiexec package and the /L &lt;location&gt; option.</span></span> <span data-ttu-id="6df88-185">Protokolldateien werden an dem angegebenen Speicherort erstellt.</span><span class="sxs-lookup"><span data-stu-id="6df88-185">Log files are created in the location specified.</span></span>

 

**<span data-ttu-id="6df88-186">MBAM-Client Setup-Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="6df88-186">MBAM Client Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="6df88-187">MSI <em> &lt; fünf zufällige Zeichen &gt; </em> . log</span><span class="sxs-lookup"><span data-stu-id="6df88-187">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="6df88-188">Protokolliert die während der MBAM-Client Installation ausgeführten Aktionen.</span><span class="sxs-lookup"><span data-stu-id="6df88-188">Logs the actions taken during MBAM Client installation.</span></span>

## <a href="" id="---------mbam-database-tde-considerations"></a> <span data-ttu-id="6df88-189">Überlegungen zu MBAM-Daten Bank DSA</span><span class="sxs-lookup"><span data-stu-id="6df88-189">MBAM Database TDE Considerations</span></span>


<span data-ttu-id="6df88-190">Das in SQL Server verfügbare Feature "transparente Datenverschlüsselung (DSA)" ist eine optionale Installation für die Datenbankinstanzen, in denen MBAM-Datenbankfeatures gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="6df88-190">The transparent data encryption (TDE) feature that is available in SQL Server is an optional installation for the database instances that will host MBAM database features.</span></span>

<span data-ttu-id="6df88-191">Mit DSA können Sie die vollständige Verschlüsselung auf Datenbankebene in Echtzeit durchführen.</span><span class="sxs-lookup"><span data-stu-id="6df88-191">With TDE, you can perform real-time, full database-level encryption.</span></span> <span data-ttu-id="6df88-192">DSA ist die optimale Lösung für die Massenverschlüsselung, um behördliche Compliance-oder Unternehmensdaten Sicherheitsstandards zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="6df88-192">TDE is the optimal choice for bulk encryption to meet regulatory compliance or corporate data security standards.</span></span> <span data-ttu-id="6df88-193">DSA funktioniert auf der Dateiebene, die zwei Windows-Features ähnelt: EFS (Encrypting File System) und BitLocker-Laufwerkverschlüsselung, die beide auch Daten auf der Festplatte verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="6df88-193">TDE works at the file level, which is similar to two Windows features: the Encrypting File System (EFS) and BitLocker Drive Encryption, both of which also encrypt data on the hard drive.</span></span> <span data-ttu-id="6df88-194">DSA ersetzt nicht die Verschlüsselung auf Zellenebene, EFS oder BitLocker.</span><span class="sxs-lookup"><span data-stu-id="6df88-194">TDE does not replace cell-level encryption, EFS, or BitLocker.</span></span>

<span data-ttu-id="6df88-195">Wenn DSA für eine Datenbank aktiviert ist, werden alle Sicherungen verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="6df88-195">When TDE is enabled on a database, all backups are encrypted.</span></span> <span data-ttu-id="6df88-196">Daher muss besonders darauf geachtet werden, dass das zum Schützen des Datenbank-Verschlüsselungsschlüssels verwendete Zertifikat mit der Datenbanksicherung gesichert und verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="6df88-196">Thus, special care must be taken to ensure that the certificate that was used to protect the database encryption key is backed up and maintained with the database backup.</span></span> <span data-ttu-id="6df88-197">Wenn dieses Zertifikat (oder Zertifikate) verloren geht, sind die Daten nicht lesbar.</span><span class="sxs-lookup"><span data-stu-id="6df88-197">If this certificate (or certificates) is lost, the data will be unreadable.</span></span> <span data-ttu-id="6df88-198">Sichern Sie das Zertifikat zusammen mit der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="6df88-198">Back up the certificate along with the database.</span></span> <span data-ttu-id="6df88-199">Für jede Zertifikat Sicherung sollten zwei Dateien vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="6df88-199">Each certificate backup should have two files.</span></span> <span data-ttu-id="6df88-200">Beide Dateien sollten archiviert werden (idealerweise getrennt von der Datenbanksicherungsdatei zur Sicherheit).</span><span class="sxs-lookup"><span data-stu-id="6df88-200">Both of these files should be archived (ideally separately from the database backup file for security).</span></span> <span data-ttu-id="6df88-201">Alternativ können Sie die erweiterbare Schlüssel Verwaltungsfunktion (Extensible Key Management, erweiterbare Schlüsselverwaltung) für die Speicherung und Wartung von Schlüsseln verwenden, die für DSA verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6df88-201">You can alternatively consider using the extensible key management (EKM) feature (see Extensible Key Management) for storage and maintenance of keys used for TDE.</span></span>

<span data-ttu-id="6df88-202">Ein Beispiel für die Aktivierung von DSA für MBAM-Datenbankinstanzen finden Sie unter [Auswerten von MBAM 2,0](evaluating-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="6df88-202">For an example of how to enable TDE for MBAM database instances, see [Evaluating MBAM 2.0](evaluating-mbam-20-mbam-2.md).</span></span>

<span data-ttu-id="6df88-203">Weitere Informationen zu DSA in SQLServer 2008 finden Sie unter [SQL Server-Verschlüsselung]( https://go.microsoft.com/fwlink/?LinkId=299883).</span><span class="sxs-lookup"><span data-stu-id="6df88-203">For more information about TDE in SQLServer 2008, see [SQL Server Encryption]( https://go.microsoft.com/fwlink/?LinkId=299883).</span></span>

## <span data-ttu-id="6df88-204">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="6df88-204">Related topics</span></span>


[<span data-ttu-id="6df88-205">Sicherheit und Datenschutz für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="6df88-205">Security and Privacy for MBAM 2.0</span></span>](security-and-privacy-for-mbam-20-mbam-2.md)

 

 





