---
title: Sicherheitsüberlegungen zu MBAM 1.0
description: Sicherheitsüberlegungen zu MBAM 1.0
author: dansimp
ms.assetid: 5e1c8b8c-235b-4a92-8b0b-da50dca17353
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b06c343c8193293dde91bc7af2541f35f332d261
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811608"
---
# <span data-ttu-id="5934c-103">Sicherheitsüberlegungen zu MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="5934c-103">Security Considerations for MBAM 1.0</span></span>


<span data-ttu-id="5934c-104">Dieses Thema enthält eine kurze Übersicht über die Konten und Gruppen, Protokolldateien und andere sicherheitsbezogene Überlegungen für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM).</span><span class="sxs-lookup"><span data-stu-id="5934c-104">This topic contains a brief overview of the accounts and groups, log files, and other security-related considerations for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="5934c-105">Weitere Informationen finden Sie unter den Links in diesem Artikel.</span><span class="sxs-lookup"><span data-stu-id="5934c-105">For more information, follow the links in this article.</span></span>

## <span data-ttu-id="5934c-106">Allgemeine Sicherheitsüberlegungen</span><span class="sxs-lookup"><span data-stu-id="5934c-106">General security considerations</span></span>


**<span data-ttu-id="5934c-107">Grundlegendes zu den Sicherheitsrisiken</span><span class="sxs-lookup"><span data-stu-id="5934c-107">Understand the security risks.</span></span>** <span data-ttu-id="5934c-108">Das schwerwiegendste Risiko für MBAM besteht darin, dass seine Funktionalität von einem nicht autorisierten Benutzer gekapert werden kann, der dann die BitLocker-Verschlüsselung neu konfigurieren und BitLocker-Verschlüsselungsschlüssel Daten auf MBAM-Clients erhalten kann.</span><span class="sxs-lookup"><span data-stu-id="5934c-108">The most serious risk to MBAM is that its functionality could be hijacked by an unauthorized user who could then reconfigure BitLocker encryption and gain BitLocker encryption key data on MBAM Clients.</span></span> <span data-ttu-id="5934c-109">Der Verlust von MBAM-Funktionen für einen kurzen Zeitraum aufgrund eines Denial-of-Service-Angriffs würde jedoch im Allgemeinen keine katastrophalen Auswirkungen haben.</span><span class="sxs-lookup"><span data-stu-id="5934c-109">However, the loss of MBAM functionality for a short period of time due to a denial-of-service attack would not generally have a catastrophic impact.</span></span>

<span data-ttu-id="5934c-110">**Physisches sichern ihrer Computer**.</span><span class="sxs-lookup"><span data-stu-id="5934c-110">**Physically secure your computers**.</span></span> <span data-ttu-id="5934c-111">Sicherheit ist ohne physische Sicherheit unvollständig.</span><span class="sxs-lookup"><span data-stu-id="5934c-111">Security is incomplete without physical security.</span></span> <span data-ttu-id="5934c-112">Jeder, der über einen physischen Zugriff auf einen MBAM-Server verfügt, kann möglicherweise die gesamte Clientbasis angreifen.</span><span class="sxs-lookup"><span data-stu-id="5934c-112">Anyone with physical access to an MBAM Server could potentially attack the entire client base.</span></span> <span data-ttu-id="5934c-113">Mögliche physische Angriffe müssen als Risiko behaftet und entsprechend verringert werden.</span><span class="sxs-lookup"><span data-stu-id="5934c-113">Any potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="5934c-114">MBAM-Server sollten in einem physisch sicheren Serverraum mit kontrolliertem Zugriff gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="5934c-114">MBAM servers should be stored in a physically secure server room with controlled access.</span></span> <span data-ttu-id="5934c-115">Sichern Sie diese Computer, wenn Administratoren physisch nicht anwesend sind, indem Sie das Betriebssystem sperren oder einen sicheren Bildschirmschoner verwenden.</span><span class="sxs-lookup"><span data-stu-id="5934c-115">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="5934c-116">**Wenden Sie die neuesten Sicherheitsupdates auf alle Computer an**.</span><span class="sxs-lookup"><span data-stu-id="5934c-116">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="5934c-117">Informieren Sie sich über neue Updates für Betriebssysteme, Microsoft SQL Server und MBAM, indem Sie den Security Notification Service ( <https://go.microsoft.com/fwlink/p/?LinkId=28819> ) abonnieren.</span><span class="sxs-lookup"><span data-stu-id="5934c-117">Stay informed about new updates for operating systems, Microsoft SQL Server, and MBAM by subscribing to the Security Notification service (<https://go.microsoft.com/fwlink/p/?LinkId=28819>).</span></span>

<span data-ttu-id="5934c-118">**Verwenden Sie sichere Kennwörter oder Passphrasen**.</span><span class="sxs-lookup"><span data-stu-id="5934c-118">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="5934c-119">Verwenden Sie immer starke Kennwörter mit 15 oder mehr Zeichen für alle MBAM-und MBAM-Administratorkonten.</span><span class="sxs-lookup"><span data-stu-id="5934c-119">Always use strong passwords with 15 or more characters for all MBAM and MBAM administrator accounts.</span></span> <span data-ttu-id="5934c-120">Verwenden Sie niemals leere Kennwörter.</span><span class="sxs-lookup"><span data-stu-id="5934c-120">Never use blank passwords.</span></span> <span data-ttu-id="5934c-121">Weitere Informationen zu Kenn Wort Konzepten finden Sie im Whitepaper "Kontokennwörter und-Richtlinien" auf TechNet ( <https://go.microsoft.com/fwlink/p/?LinkId=30009> ).</span><span class="sxs-lookup"><span data-stu-id="5934c-121">For more information about password concepts, see the “Account Passwords and Policies” white paper on TechNet (<https://go.microsoft.com/fwlink/p/?LinkId=30009>).</span></span>

## <span data-ttu-id="5934c-122">Konten und Gruppen in MBAM</span><span class="sxs-lookup"><span data-stu-id="5934c-122">Accounts and Groups in MBAM</span></span>


<span data-ttu-id="5934c-123">Eine bewährte Methode für die Verwaltung von Benutzerkonten ist das Erstellen globaler Domänengruppen und das Hinzufügen von Benutzerkonten.</span><span class="sxs-lookup"><span data-stu-id="5934c-123">A best practice for user account management is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="5934c-124">Fügen Sie dann die globalen Domänenkonten den erforderlichen lokalen MBAM-Gruppen auf den MBAM-Servern hinzu.</span><span class="sxs-lookup"><span data-stu-id="5934c-124">Then, add the domain global accounts to the necessary MBAM local groups on the MBAM Servers.</span></span>

### <span data-ttu-id="5934c-125">ActiveDirectoryDomainServices-Gruppen</span><span class="sxs-lookup"><span data-stu-id="5934c-125">ActiveDirectoryDomainServices Groups</span></span>

<span data-ttu-id="5934c-126">Während der MBAM-Einrichtung werden keine Gruppen automatisch erstellt.</span><span class="sxs-lookup"><span data-stu-id="5934c-126">No groups are created automatically during MBAM Setup.</span></span> <span data-ttu-id="5934c-127">Sie sollten jedoch die folgenden globalen ActiveDirectoryDomainServices-Gruppen erstellen, um MBAM-Vorgänge zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="5934c-127">However, you should create the following ActiveDirectoryDomainServices global groups to manage MBAM operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5934c-128">Gruppenname</span><span class="sxs-lookup"><span data-stu-id="5934c-128">Group Name</span></span></th>
<th align="left"><span data-ttu-id="5934c-129">Details</span><span class="sxs-lookup"><span data-stu-id="5934c-129">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5934c-130">MBAM Advanced Helpdesk-Benutzer</span><span class="sxs-lookup"><span data-stu-id="5934c-130">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="5934c-131">Erstellen Sie diese Gruppe zum Verwalten von Mitgliedern der lokalen Gruppe MBAM Advanced Helpdesk-Benutzer, die während des MBAM-Setups erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5934c-131">Create this group to manage members of the MBAM Advanced Helpdesk Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5934c-132">MBAM Compliance Auditing DB Access</span><span class="sxs-lookup"><span data-stu-id="5934c-132">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="5934c-133">Erstellen Sie diese Gruppe zum Verwalten von Mitgliedern der lokalen Gruppe MBAM Compliance Auditing DB Access, die während des MBAM-Setups erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5934c-133">Create this group to manage members of the MBAM Compliance Auditing DB Access local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5934c-134">MBAM-Hardware Benutzer</span><span class="sxs-lookup"><span data-stu-id="5934c-134">MBAM Hardware Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="5934c-135">Erstellen Sie diese Gruppe, um die Mitglieder der lokalen Gruppe MBAM-Hardware Benutzer zu verwalten, die während des MBAM-Setups erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5934c-135">Create this group to manage members of the MBAM Hardware Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5934c-136">MBAM Helpdesk-Benutzer</span><span class="sxs-lookup"><span data-stu-id="5934c-136">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="5934c-137">Erstellen Sie diese Gruppe, um Mitglieder der lokalen Gruppe MBAM Helpdesk-Benutzer zu verwalten, die während des MBAM-Setups erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5934c-137">Create this group to manage members of the MBAM Helpdesk Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5934c-138">MBAM Recovery-und Hardware-DB-Zugriff</span><span class="sxs-lookup"><span data-stu-id="5934c-138">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="5934c-139">Erstellen Sie diese Gruppe, um die Mitglieder der lokalen Gruppe MBAM Recovery and Hardware DB Access zu verwalten, die während des MBAM-Setups erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5934c-139">Create this group to manage members of the MBAM Recovery and Hardware DB Access local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5934c-140">MBAM-Berichtsbenutzer</span><span class="sxs-lookup"><span data-stu-id="5934c-140">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="5934c-141">Erstellen Sie diese Gruppe, um Mitglieder der lokalen Gruppe MBAM-Berichtsbenutzer zu verwalten, die während des MBAM-Setups erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5934c-141">Create this group to manage members of the MBAM Report Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5934c-142">MBAM-System Administratoren</span><span class="sxs-lookup"><span data-stu-id="5934c-142">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="5934c-143">Erstellen Sie diese Gruppe, um die Mitglieder der lokalen Gruppe MBAM-System Administratoren zu verwalten, die während des MBAM-Setups erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5934c-143">Create this group to manage members of the MBAM System Administrators local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5934c-144">Ausnahmen für BitLocker-Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="5934c-144">BitLocker Encryption Exemptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="5934c-145">Erstellen Sie diese Gruppe zum Verwalten von Benutzerkonten, die von der BitLocker-Verschlüsselung ab Computern, bei denen Sie sich anmelden, ausgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5934c-145">Create this group to manage user accounts that should be exempted from BitLocker encryption starting on computers that they log on to.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="5934c-146">Lokale MBAM-Server Gruppen</span><span class="sxs-lookup"><span data-stu-id="5934c-146">MBAM Server Local Groups</span></span>

<span data-ttu-id="5934c-147">MBAM Setup erstellt lokale Gruppen, um MBAM-Vorgänge zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5934c-147">MBAM Setup creates local groups to support MBAM operations.</span></span> <span data-ttu-id="5934c-148">Sie sollten die globalen ActiveDirectoryDomainServices-Gruppen den entsprechenden lokalen MBAM-Gruppen hinzufügen, um MBAM-Sicherheits-und Datenzugriffsberechtigungen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="5934c-148">You should add the ActiveDirectoryDomainServices Global Groups to the appropriate MBAM local groups to configure MBAM security and data access permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5934c-149">Gruppenname</span><span class="sxs-lookup"><span data-stu-id="5934c-149">Group Name</span></span></th>
<th align="left"><span data-ttu-id="5934c-150">Details</span><span class="sxs-lookup"><span data-stu-id="5934c-150">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5934c-151">MBAM Advanced Helpdesk-Benutzer</span><span class="sxs-lookup"><span data-stu-id="5934c-151">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="5934c-152">Mitglieder dieser Gruppe haben erweiterten Zugriff auf die Helpdesk-Features der Microsoft BitLocker-Verwaltung und-Überwachung.</span><span class="sxs-lookup"><span data-stu-id="5934c-152">Members of this group have expanded access to the Helpdesk features of Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5934c-153">MBAM Compliance Auditing DB Access</span><span class="sxs-lookup"><span data-stu-id="5934c-153">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="5934c-154">Diese Gruppe enthält die Computer, die Zugriff auf die MBAM-Konformitäts Überwachungsdatenbank haben.</span><span class="sxs-lookup"><span data-stu-id="5934c-154">This group contains the machines that have access to the MBAM Compliance Auditing Database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5934c-155">MBAM-Hardware Benutzer</span><span class="sxs-lookup"><span data-stu-id="5934c-155">MBAM Hardware Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="5934c-156">Mitglieder dieser Gruppe haben Zugriff auf einige der Hardware Funktionen von Microsoft BitLocker-Verwaltung und-Überwachung.</span><span class="sxs-lookup"><span data-stu-id="5934c-156">Members of this group have access to some of the Hardware Capability features from Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5934c-157">MBAM Helpdesk-Benutzer</span><span class="sxs-lookup"><span data-stu-id="5934c-157">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="5934c-158">Mitglieder dieser Gruppe können über die Microsoft BitLocker-Verwaltung und-Überwachung auf einige der Helpdesk-Features zugreifen.</span><span class="sxs-lookup"><span data-stu-id="5934c-158">Members of this group have access to some of the Helpdesk features from Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5934c-159">MBAM Recovery-und Hardware-DB-Zugriff</span><span class="sxs-lookup"><span data-stu-id="5934c-159">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="5934c-160">Diese Gruppe enthält die Computer, die Zugriff auf die MBAM-Wiederherstellungs-und-Hardware Datenbank haben.</span><span class="sxs-lookup"><span data-stu-id="5934c-160">This group contains the computers that have access to the MBAM Recovery and Hardware Database.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5934c-161">MBAM-Berichtsbenutzer</span><span class="sxs-lookup"><span data-stu-id="5934c-161">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="5934c-162">Mitglieder dieser Gruppe haben Zugriff auf die Konformitäts-und Überwachungsberichte aus der Microsoft BitLocker-Verwaltung und-Überwachung.</span><span class="sxs-lookup"><span data-stu-id="5934c-162">Members of this group have access to the Compliance and Audit reports from Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5934c-163">MBAM-System Administratoren</span><span class="sxs-lookup"><span data-stu-id="5934c-163">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="5934c-164">Mitglieder dieser Gruppe haben Zugriff auf alle Features der Microsoft BitLocker-Verwaltung und-Überwachung.</span><span class="sxs-lookup"><span data-stu-id="5934c-164">Members of this group have access to all the features of Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="5934c-165">Zugriffskonto für SSRS-Berichte</span><span class="sxs-lookup"><span data-stu-id="5934c-165">SSRS Reports Access Account</span></span>

<span data-ttu-id="5934c-166">Das SQL Server Reporting Services (SSRS)-Berichtsdienst Konto bietet den Sicherheitskontext zum Ausführen der MBAM-Berichte, die über SSRS zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="5934c-166">The SQL Server Reporting Services (SSRS) Reports Service Account provides the security context to run the MBAM reports available through SSRS.</span></span> <span data-ttu-id="5934c-167">Dieses Konto wird während des MBAM-Setups konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="5934c-167">This account is configured during MBAM Setup.</span></span>

## <span data-ttu-id="5934c-168">MBAM-Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="5934c-168">MBAM Log Files</span></span>


<span data-ttu-id="5934c-169">Während des MBAM-Setups werden die folgenden MBAM-Setupprotokolldateien im Ordner "% Temp%" des Benutzers erstellt, der den</span><span class="sxs-lookup"><span data-stu-id="5934c-169">During MBAM Setup, the following MBAM Setup log files are created in the %temp% folder of the user who installs the</span></span>

**<span data-ttu-id="5934c-170">MBAM Server Setup-Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="5934c-170">MBAM Server Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="5934c-171">MSI <em> &lt; fünf zufällige Zeichen &gt; </em> . log</span><span class="sxs-lookup"><span data-stu-id="5934c-171">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="5934c-172">Protokolliert die Aktionen, die während der Installation von MBAM-Setup und der MBAM-Server Funktion ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="5934c-172">Logs the actions taken during MBAM Setup and MBAM Server Feature installation.</span></span>

<a href="" id="installcompliancedatabase-log"></a><span data-ttu-id="5934c-173">InstallComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="5934c-173">InstallComplianceDatabase.log</span></span>  
<span data-ttu-id="5934c-174">Protokolliert die Aktionen, die zum Erstellen der MBAM-Konformitäts Status Datenbank ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="5934c-174">Logs the actions taken to create the MBAM Compliance Status database setup.</span></span>

<a href="" id="installkeycompliancedatabase-log"></a><span data-ttu-id="5934c-175">InstallKeyComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="5934c-175">InstallKeyComplianceDatabase.log</span></span>  
<span data-ttu-id="5934c-176">Protokolliert die Aktionen, die zum Erstellen der MBAM-Wiederherstellungs-und-Hardware Datenbank ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="5934c-176">Logs the actions taken to create the MBAM Recovery and Hardware database.</span></span>

<a href="" id="addhelpdeskdbauditusers-log"></a><span data-ttu-id="5934c-177">AddHelpDeskDbAuditUsers. log</span><span class="sxs-lookup"><span data-stu-id="5934c-177">AddHelpDeskDbAuditUsers.log</span></span>  
<span data-ttu-id="5934c-178">Protokolliert die Aktionen, die zum Erstellen der SQL Server-Anmeldungen in der MBAM-Konformitäts Status Datenbank ergriffen wurden, und Autorisieren des Helpdesk-Webdiensts zur Datenbank für Berichte.</span><span class="sxs-lookup"><span data-stu-id="5934c-178">Logs the actions taken to create the SQL Server logins on the MBAM Compliance Status database and authorize helpdesk web service to the database for reports.</span></span>

<a href="" id="addhelpdeskdbusers-log"></a><span data-ttu-id="5934c-179">AddHelpDeskDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="5934c-179">AddHelpDeskDbUsers.log</span></span>  
<span data-ttu-id="5934c-180">Protokolliert die Aktionen, die zum Autorisieren von Webdiensten zur Datenbank für die Schlüsselwiederherstellung und zum Erstellen von Anmeldungen in der MBAM-Wiederherstellungs-und-Hardware Datenbank ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="5934c-180">Logs the actions taken to authorize web services to database for key recovery and create logins to the MBAM Recovery and Hardware database.</span></span>

<a href="" id="addkeycompliancedbusers-log"></a><span data-ttu-id="5934c-181">AddKeyComplianceDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="5934c-181">AddKeyComplianceDbUsers.log</span></span>  
<span data-ttu-id="5934c-182">Protokolliert die Aktionen, die zum Autorisieren von Webdiensten zur MBAM-Konformitäts Status Datenbank für Konformitätsberichte ergriffen wurden.</span><span class="sxs-lookup"><span data-stu-id="5934c-182">Logs the actions taken to authorize web services to MBAM Compliance Status database for compliance reporting.</span></span>

<a href="" id="addrecoveryandhardwaredbusers-log"></a><span data-ttu-id="5934c-183">AddRecoveryAndHardwareDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="5934c-183">AddRecoveryAndHardwareDbUsers.log</span></span>  
<span data-ttu-id="5934c-184">Protokolliert die Aktionen, die zum Autorisieren von Webdiensten zur MBAM-Wiederherstellung und Hardware Datenbank für die Schlüsselwiederherstellung ergriffen wurden.</span><span class="sxs-lookup"><span data-stu-id="5934c-184">Logs the actions taken to authorize web services to MBAM Recovery and Hardware database for key recovery.</span></span>

<span data-ttu-id="5934c-185">**Hinweis**  Um weitere MBAM-Setup Protokolldateien zu erhalten, müssen Sie die Microsoft BitLocker-Verwaltung und-Überwachung mithilfe des **msiexec** -Pakets und der Option " **/l** &lt; Location &gt; " installieren.</span><span class="sxs-lookup"><span data-stu-id="5934c-185">**Note** In order to obtain additional MBAM Setup log files, you must install Microsoft BitLocker Administration and Monitoring by using the **msiexec** package and the **/l** &lt;location&gt; option.</span></span> <span data-ttu-id="5934c-186">Protokolldateien werden an dem angegebenen Speicherort erstellt.</span><span class="sxs-lookup"><span data-stu-id="5934c-186">Log files are created in the location specified.</span></span>

 

**<span data-ttu-id="5934c-187">MBAM-Client Setup-Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="5934c-187">MBAM Client Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="5934c-188">MSI <em> &lt; fünf zufällige Zeichen &gt; </em> . log</span><span class="sxs-lookup"><span data-stu-id="5934c-188">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="5934c-189">Protokolliert die während der MBAM-Client Installation ausgeführten Aktionen.</span><span class="sxs-lookup"><span data-stu-id="5934c-189">Logs the actions taken during MBAM Client installation.</span></span>

## <span data-ttu-id="5934c-190">Überlegungen zu MBAM-Daten Bank DSA</span><span class="sxs-lookup"><span data-stu-id="5934c-190">MBAM Database TDE considerations</span></span>


<span data-ttu-id="5934c-191">Das in SQL Server 2008 verfügbare Feature "transparente Datenverschlüsselung (DSA)" ist eine erforderliche Installationsvoraussetzung für die Datenbankinstanzen, in denen MBAM-Datenbankfeatures gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="5934c-191">The Transparent Data Encryption (TDE) feature available in SQL Server 2008 is a required installation prerequisite for the database instances that will host MBAM database features.</span></span>

<span data-ttu-id="5934c-192">Mit DSA können Sie die vollständige Verschlüsselung auf Datenbankebene in Echtzeit durchführen.</span><span class="sxs-lookup"><span data-stu-id="5934c-192">With TDE, you can perform real-time, full database-level encryption.</span></span> <span data-ttu-id="5934c-193">DSA eignet sich hervorragend für die Massenverschlüsselung, um behördliche Compliance-oder Unternehmensdaten Sicherheitsstandards zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="5934c-193">TDE is a well-suited choice for bulk encryption to meet regulatory compliance or corporate data security standards.</span></span> <span data-ttu-id="5934c-194">DSA funktioniert auf der Dateiebene, die zwei Windows-Features ähnelt: EFS (Encrypting File System) und BitLocker-Laufwerkverschlüsselung, die beide auch Daten auf der Festplatte verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="5934c-194">TDE works at the file level, which is similar to two Windows features: the Encrypting File System (EFS) and BitLocker Drive Encryption, both of which also encrypt data on the hard drive.</span></span> <span data-ttu-id="5934c-195">DSA ersetzt nicht die Verschlüsselung auf Zellenebene, EFS oder BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5934c-195">TDE does not replace cell-level encryption, EFS, or BitLocker.</span></span>

<span data-ttu-id="5934c-196">Wenn DSA für eine Datenbank aktiviert ist, werden alle Sicherungen verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="5934c-196">When TDE is enabled on a database, all backups are encrypted.</span></span> <span data-ttu-id="5934c-197">Daher muss besonders darauf geachtet werden, dass das zum Schützen des Daten Bank Verschlüsselungsschlüssels (DEK) verwendete Zertifikat mit der Datenbanksicherung gesichert und verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="5934c-197">Thus, special care must be taken to ensure that the certificate that was used to protect the Database Encryption Key (DEK) is backed up and maintained with the database backup.</span></span> <span data-ttu-id="5934c-198">Ohne ein Zertifikat sind die Daten nicht lesbar.</span><span class="sxs-lookup"><span data-stu-id="5934c-198">Without a certificate, the data will be unreadable.</span></span> <span data-ttu-id="5934c-199">Sichern Sie das Zertifikat zusammen mit der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5934c-199">Back up the certificate along with the database.</span></span> <span data-ttu-id="5934c-200">Für jede Zertifikat Sicherung sollten zwei Dateien vorhanden sein. Beide Dateien sollten archiviert werden. Es empfiehlt sich, die Daten aus der Datenbank-Sicherungsdatei für die Sicherheit separat zu archivieren.</span><span class="sxs-lookup"><span data-stu-id="5934c-200">Each certificate backup should have two files; both of these files should be archived .It is best to archive them separately from the database backup file for security.</span></span>

<span data-ttu-id="5934c-201">Ein Beispiel für die Aktivierung von DSA für MBAM-Datenbankinstanzen finden Sie unter [Auswerten von MBAM 1,0](evaluating-mbam-10.md).</span><span class="sxs-lookup"><span data-stu-id="5934c-201">For an example of how to enable TDE for MBAM database instances, see [Evaluating MBAM 1.0](evaluating-mbam-10.md).</span></span>

<span data-ttu-id="5934c-202">Weitere Informationen zu DSA in SQLServer 2008 finden Sie unter [Datenbankverschlüsselung in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703).</span><span class="sxs-lookup"><span data-stu-id="5934c-202">For more information about TDE in SQLServer 2008, see [Database Encryption in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703).</span></span>

## <span data-ttu-id="5934c-203">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5934c-203">Related topics</span></span>


[<span data-ttu-id="5934c-204">Sicherheit und Datenschutz für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="5934c-204">Security and Privacy for MBAM 1.0</span></span>](security-and-privacy-for-mbam-10.md)

 

 





