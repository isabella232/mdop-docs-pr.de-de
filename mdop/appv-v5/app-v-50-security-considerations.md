---
title: Sicherheitsüberlegungen zu App-V 5.0
description: Sicherheitsüberlegungen zu App-V 5.0
author: dansimp
ms.assetid: 1e7292a0-7972-4b4f-85a9-eaf33f6c563a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fcd740345be7f532502b8996d8d2b1f4437ed6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806005"
---
# <span data-ttu-id="e9093-103">Sicherheitsüberlegungen zu App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="e9093-103">App-V 5.0 Security Considerations</span></span>


<span data-ttu-id="e9093-104">Dieses Thema enthält eine kurze Übersicht über die Konten und Gruppen, Protokolldateien und andere sicherheitsbezogene Überlegungen für App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="e9093-104">This topic contains a brief overview of the accounts and groups, log files, and other security-related considerations for App-V 5.0.</span></span>

**<span data-ttu-id="e9093-105">Wichtig</span><span class="sxs-lookup"><span data-stu-id="e9093-105">Important</span></span>**  
<span data-ttu-id="e9093-106">App-V 5,0 ist kein Sicherheitsprodukt und bietet keine Garantien für eine sichere Umgebung.</span><span class="sxs-lookup"><span data-stu-id="e9093-106">App-V 5.0 is not a security product and does not provide any guarantees for a secure environment.</span></span>



## <span data-ttu-id="e9093-107">PackageStoreAccessControl (PSAC erklärte)-Feature wurde als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="e9093-107">PackageStoreAccessControl (PSAC) feature has been deprecated</span></span>


<span data-ttu-id="e9093-108">Ab Juni 2014 wurde das PackageStoreAccessControl (PSAC erklärte)-Feature, das in Microsoft Application Virtualization (App-V) 5,0 Service Pack 2 (SP2) eingeführt wurde, in Umgebungen mit einzelnen Benutzern und mehreren Benutzern als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="e9093-108">Effective as of June, 2014, the PackageStoreAccessControl (PSAC) feature that was introduced in Microsoft Application Virtualization (App-V) 5.0 Service Pack 2 (SP2) has been deprecated in both single-user and multi-user environments.</span></span>

## <span data-ttu-id="e9093-109">Allgemeine Sicherheitsüberlegungen</span><span class="sxs-lookup"><span data-stu-id="e9093-109">General security considerations</span></span>


**<span data-ttu-id="e9093-110">Grundlegendes zu den Sicherheitsrisiken</span><span class="sxs-lookup"><span data-stu-id="e9093-110">Understand the security risks.</span></span>** <span data-ttu-id="e9093-111">Das schwerwiegendste Risiko für App-v 5,0 besteht darin, dass die Funktionalität von einem nicht autorisierten Benutzer übernommen werden kann, der dann die wichtigsten Daten auf App-v 5,0-Clients neu konfigurieren kann.</span><span class="sxs-lookup"><span data-stu-id="e9093-111">The most serious risk to App-V 5.0 is that its functionality could be hijacked by an unauthorized user who could then reconfigure key data on App-V 5.0 clients.</span></span> <span data-ttu-id="e9093-112">Der Verlust der App-V 5,0-Funktionalität für kurze Zeit aufgrund eines Denial-of-Service-Angriffs hätte in der Regel keine katastrophalen Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="e9093-112">The loss of App-V 5.0 functionality for a short period of time due to a denial-of-service attack would not generally have a catastrophic impact.</span></span>

<span data-ttu-id="e9093-113">**Physisches sichern ihrer Computer**.</span><span class="sxs-lookup"><span data-stu-id="e9093-113">**Physically secure your computers**.</span></span> <span data-ttu-id="e9093-114">Sicherheit ist ohne physische Sicherheit unvollständig.</span><span class="sxs-lookup"><span data-stu-id="e9093-114">Security is incomplete without physical security.</span></span> <span data-ttu-id="e9093-115">Jeder mit physischem Zugriff auf einen App-V 5,0-Server kann potenziell die gesamte Clientbasis angreifen.</span><span class="sxs-lookup"><span data-stu-id="e9093-115">Anyone with physical access to an App-V 5.0 server could potentially attack the entire client base.</span></span> <span data-ttu-id="e9093-116">Mögliche physische Angriffe müssen als Risiko behaftet und entsprechend verringert werden.</span><span class="sxs-lookup"><span data-stu-id="e9093-116">Any potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="e9093-117">App-V 5,0-Server sollten in einem physisch sicheren Serverraum mit kontrolliertem Zugriff gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e9093-117">App-V 5.0 servers should be stored in a physically secure server room with controlled access.</span></span> <span data-ttu-id="e9093-118">Sichern Sie diese Computer, wenn Administratoren physisch nicht anwesend sind, indem Sie das Betriebssystem sperren oder einen sicheren Bildschirmschoner verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9093-118">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="e9093-119">**Wenden Sie die neuesten Sicherheitsupdates auf alle Computer an**.</span><span class="sxs-lookup"><span data-stu-id="e9093-119">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="e9093-120">Wenn Sie über die neuesten Updates für Betriebssysteme, Microsoft SQL Server und App-V 5,0 auf dem Laufenden bleiben möchten, abonnieren Sie den Sicherheitsbenachrichtigungsdienst ( <https://go.microsoft.com/fwlink/p/?LinkId=28819> ).</span><span class="sxs-lookup"><span data-stu-id="e9093-120">To stay informed about the latest updates for operating systems, Microsoft SQL Server, and App-V 5.0, subscribe to the Security Notification service (<https://go.microsoft.com/fwlink/p/?LinkId=28819>).</span></span>

<span data-ttu-id="e9093-121">**Verwenden Sie sichere Kennwörter oder Passphrasen**.</span><span class="sxs-lookup"><span data-stu-id="e9093-121">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="e9093-122">Verwenden Sie immer starke Kennwörter mit 15 oder mehr Zeichen für alle App-v 5,0-und App-v 5,0-Administratorkonten.</span><span class="sxs-lookup"><span data-stu-id="e9093-122">Always use strong passwords with 15 or more characters for all App-V 5.0 and App-V 5.0 administrator accounts.</span></span> <span data-ttu-id="e9093-123">Verwenden Sie niemals leere Kennwörter.</span><span class="sxs-lookup"><span data-stu-id="e9093-123">Never use blank passwords.</span></span> <span data-ttu-id="e9093-124">Weitere Informationen zu Kenn Wort Konzepten finden Sie im Whitepaper "Kontokennwörter und-Richtlinien" auf TechNet ( <https://go.microsoft.com/fwlink/p/?LinkId=30009> ).</span><span class="sxs-lookup"><span data-stu-id="e9093-124">For more information about password concepts, see the “Account Passwords and Policies” white paper on TechNet (<https://go.microsoft.com/fwlink/p/?LinkId=30009>).</span></span>

## <span data-ttu-id="e9093-125">Konten und Gruppen in App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="e9093-125">Accounts and groups in App-V 5.0</span></span>


<span data-ttu-id="e9093-126">Eine bewährte Methode für die Verwaltung von Benutzerkonten ist das Erstellen globaler Domänengruppen und das Hinzufügen von Benutzerkonten.</span><span class="sxs-lookup"><span data-stu-id="e9093-126">A best practice for user account management is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="e9093-127">Fügen Sie dann die globalen Domänenkonten den erforderlichen App-v 5,0-lokalen Gruppen auf den App-v 5,0-Servern hinzu.</span><span class="sxs-lookup"><span data-stu-id="e9093-127">Then, add the domain global accounts to the necessary App-V 5.0 local groups on the App-V 5.0 servers.</span></span>

**<span data-ttu-id="e9093-128">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="e9093-128">Note</span></span>**  
<span data-ttu-id="e9093-129">App-V-Clientcomputerkonten, die eine Verbindung mit dem Veröffentlichungsserver herstellen müssen, müssen Teil der lokalen Gruppe **Benutzer** des Veröffentlichungsservers sein.</span><span class="sxs-lookup"><span data-stu-id="e9093-129">App-V client computer accounts that need to connect to the publishing server must be part of the publishing server’s **Users** local group.</span></span> <span data-ttu-id="e9093-130">Standardmäßig sind alle Computer in der Domäne Teil der Gruppe **autorisierte Benutzer** , die Teil der lokalen Gruppe **Benutzer** ist.</span><span class="sxs-lookup"><span data-stu-id="e9093-130">By default, all computers in the domain are part of the **Authorized Users** group, which is part of the **Users** local group.</span></span>



### <a href="" id="-------------app-v-5-0-server-security"></a> <span data-ttu-id="e9093-131">App-V 5,0-Server Sicherheit</span><span class="sxs-lookup"><span data-stu-id="e9093-131">App-V 5.0 server security</span></span>

<span data-ttu-id="e9093-132">Während der App-V 5,0-Einrichtung werden keine Gruppen automatisch erstellt.</span><span class="sxs-lookup"><span data-stu-id="e9093-132">No groups are created automatically during App-V 5.0 Setup.</span></span> <span data-ttu-id="e9093-133">Sie sollten die folgenden globalen Active Directory-Domänendienste-Gruppen erstellen, um die App-V 5,0-Server Vorgänge zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="e9093-133">You should create the following Active Directory Domain Services global groups to manage App-V 5.0 server operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e9093-134">Gruppenname</span><span class="sxs-lookup"><span data-stu-id="e9093-134">Group name</span></span></th>
<th align="left"><span data-ttu-id="e9093-135">Details</span><span class="sxs-lookup"><span data-stu-id="e9093-135">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e9093-136">App-V-Verwaltungs Administratorgruppe</span><span class="sxs-lookup"><span data-stu-id="e9093-136">App-V Management Admin group</span></span></p></td>
<td align="left"><p><span data-ttu-id="e9093-137">Wird verwendet, um den App-V 5,0-Verwaltungsserver zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="e9093-137">Used to manage the App-V 5.0 management server.</span></span> <span data-ttu-id="e9093-138">Diese Gruppe wird während der Installation des App-V 5,0-Verwaltungsservers erstellt.</span><span class="sxs-lookup"><span data-stu-id="e9093-138">This group is created during the App-V 5.0 Management Server installation.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e9093-139">Wichtig</span><span class="sxs-lookup"><span data-stu-id="e9093-139">Important</span></span></strong><br/><p><span data-ttu-id="e9093-140">Nachdem Sie die Installation abgeschlossen haben, gibt es keine Methode zum Erstellen der Gruppe mithilfe der Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="e9093-140">There is no method to create the group using the management console after you have completed the installation.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e9093-141">Datenbank-Lese-/Schreibzugriff für Verwaltungsdienst Konto</span><span class="sxs-lookup"><span data-stu-id="e9093-141">Database read/write for Management Service account</span></span></p></td>
<td align="left"><p><span data-ttu-id="e9093-142">Bietet Lese-und Schreibzugriff auf die Verwaltungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="e9093-142">Provides read/write access to the management database.</span></span> <span data-ttu-id="e9093-143">Dieses Konto sollte während der Installation der App-V 5,0-Verwaltungsdatenbank erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e9093-143">This account should be created during the App-V 5.0 management database installation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e9093-144">App-V-Verwaltungsdienst: Administratorkonto installieren</span><span class="sxs-lookup"><span data-stu-id="e9093-144">App-V Management Service install admin account</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e9093-145">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="e9093-145">Note</span></span></strong><br/><p><span data-ttu-id="e9093-146">Dies ist nur erforderlich, wenn die Verwaltungsdatenbank separat vom Dienst installiert wird.</span><span class="sxs-lookup"><span data-stu-id="e9093-146">This is only required if management database is being installed separately from the service.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="e9093-147">Bietet öffentlichen Zugriff auf die Tabelle "Schemaversion" in der Verwaltungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="e9093-147">Provides public access to schema-version table in management database.</span></span> <span data-ttu-id="e9093-148">Dieses Konto sollte während der Installation der App-V 5,0-Verwaltungsdatenbank erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e9093-148">This account should be created during the App-V 5.0 management database installation.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e9093-149">App-V Reporting Service-Administratorkonto installieren</span><span class="sxs-lookup"><span data-stu-id="e9093-149">App-V Reporting Service install admin account</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e9093-150">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="e9093-150">Note</span></span></strong><br/><p><span data-ttu-id="e9093-151">Dies ist nur erforderlich, wenn die Berichtsdatenbank separat vom Dienst installiert wird.</span><span class="sxs-lookup"><span data-stu-id="e9093-151">This is only required if reporting database is being installed separately from the service.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="e9093-152">Öffentlicher Zugriff auf die Tabelle "Schemaversion" in der Berichtsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="e9093-152">Public access to schema-version table in reporting database.</span></span> <span data-ttu-id="e9093-153">Dieses Konto sollte während der Installation der App-V 5,0-Berichtsdatenbank erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e9093-153">This account should be created during the App-V 5.0 reporting database installation.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="e9093-154">Bedenken Sie die folgenden zusätzlichen Informationen:</span><span class="sxs-lookup"><span data-stu-id="e9093-154">Consider the following additional information:</span></span>

-   <span data-ttu-id="e9093-155">Zugriff auf die Paketfreigaben – wenn eine Freigabe auf demselben Computer wie der Verwaltungs Server vorhanden ist, erfordert der **Netzwerk** Dienst Lesezugriff auf die Freigabe.</span><span class="sxs-lookup"><span data-stu-id="e9093-155">Access to the package shares - If a share exists on the same computer as the management Server, the **Network** service requires read access to the share.</span></span> <span data-ttu-id="e9093-156">Darüber hinaus muss jeder App-V-Clientcomputer über Lesezugriff auf die Paketfreigabe verfügen.</span><span class="sxs-lookup"><span data-stu-id="e9093-156">In addition, each App-V client computer must have read access to the package share.</span></span>

    **<span data-ttu-id="e9093-157">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="e9093-157">Note</span></span>**  
    <span data-ttu-id="e9093-158">In früheren Versionen von App-V wurde die Paketfreigabe als Inhaltsfreigabe bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e9093-158">In previous versions of App-V, package share was referred to as content share.</span></span>



-   <span data-ttu-id="e9093-159">Registrieren von Veröffentlichungsservern mit dem Verwaltungsserver – ein Veröffentlichungsserver muss beim Verwaltungsserver registriert sein.</span><span class="sxs-lookup"><span data-stu-id="e9093-159">Registering publishing servers with Management Server - A publishing server must be registered with the Management server.</span></span> <span data-ttu-id="e9093-160">Beispielsweise muss Sie der Datenbank hinzugefügt werden, damit die Computerkonten des Publishing Servers in die Verwaltungsdienst-API aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="e9093-160">For example, it must be added to the database, so that the Publishing server machine accounts are able to call into the Management service API.</span></span>

### <a href="" id="-------------app-v-5-0-package-security"></a> <span data-ttu-id="e9093-161">App-V 5,0-Paketsicherheit</span><span class="sxs-lookup"><span data-stu-id="e9093-161">App-V 5.0 package security</span></span>

<span data-ttu-id="e9093-162">Im folgenden wird erläutert, wie Sie sicherstellen können, dass virtualisierte Pakete sicher sind.</span><span class="sxs-lookup"><span data-stu-id="e9093-162">The following will help you plan how to ensure that virtualized packages are secure.</span></span>

-   <span data-ttu-id="e9093-163">Wenn ein Anwendungs Installationsprogramm eine Zugriffssteuerungsliste (ACL) auf eine Datei oder ein Verzeichnis anwendet, wird diese ACL nicht im Paket beibehalten.</span><span class="sxs-lookup"><span data-stu-id="e9093-163">If an application installer applies an access control list (ACL) to a file or directory, then that ACL is not persisted in the package.</span></span> <span data-ttu-id="e9093-164">Wenn das Paket bereitgestellt wird und die Datei oder das Verzeichnis von einem Benutzer geändert wird, erbt es entweder die ACL in **% User Profile%** oder erbt die ACL des Verzeichnisses des Zielcomputers.</span><span class="sxs-lookup"><span data-stu-id="e9093-164">When the package is deployed, if the file or directory is modified by a user it will either inherit the ACL in the **%userprofile%** or inherit the ACL of the target computer’s directory.</span></span> <span data-ttu-id="e9093-165">Der erste Fall tritt auf, wenn die Datei oder das Verzeichnis nicht an einem Speicherort des virtuellen Dateisystems vorhanden ist. der letzte Fall tritt auf, wenn die Datei oder das Verzeichnis an einem virtuellen Dateisystemspeicherort vorhanden ist, beispielsweise **% windir%**.</span><span class="sxs-lookup"><span data-stu-id="e9093-165">The former case occurs if the file or directory does not exist in a virtual file system location; the latter case occurs if the file or directory exists in a virtual file system location, for example **%windir%**.</span></span>

## <a href="" id="---------app-v-5-0-log-files"></a> <span data-ttu-id="e9093-166">App-V 5,0-Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="e9093-166">App-V 5.0 log files</span></span>


<span data-ttu-id="e9093-167">Während der Installation von App-V 5,0 werden Setupprotokolldateien im Ordner **% Temp%** des Installations Benutzers erstellt.</span><span class="sxs-lookup"><span data-stu-id="e9093-167">During App-V 5.0 Setup, setup log files are created in the **%temp%** folder of the installing user.</span></span>
