---
title: Technische Übersicht über AGPM
description: Technische Übersicht über AGPM
author: dansimp
ms.assetid: 36bc0ab5-f752-474c-8559-721ea95169c2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0cc635f46c2aabb0c9fa1f472a258a3e65a07b55
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807451"
---
# <span data-ttu-id="d3334-103">Technische Übersicht über AGPM</span><span class="sxs-lookup"><span data-stu-id="d3334-103">Technical Overview of AGPM</span></span>


<span data-ttu-id="d3334-104">Microsoft Advanced Group Policy Management (AGPM) ist eine Client/Server-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d3334-104">Microsoft Advanced Group Policy Management (AGPM) is a client/server application.</span></span> <span data-ttu-id="d3334-105">Der AGPM-Server speichert Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) offline in dem Archiv, das von AGPM im Dateisystem des Servers erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d3334-105">The AGPM Server stores Group Policy Objects (GPOs) offline in the archive that AGPM creates on the server's file system.</span></span> <span data-ttu-id="d3334-106">Gruppenrichtlinienadministratoren verwenden das AGPM-Snap-in für die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC), um mit GPOs auf dem Server zu arbeiten, der das Archiv hostet.</span><span class="sxs-lookup"><span data-stu-id="d3334-106">Group Policy administrators use the AGPM snap-in for the Group Policy Management Console (GPMC) to work with GPOs on the server that hosts the archive.</span></span> <span data-ttu-id="d3334-107">Das Verständnis der Teile von AGPM und verwandter Elemente, deren Speicherung von GPOs im Dateisystem und die Art und Weise, wie Berechtigungen die für jede Benutzerrolle verfügbaren Aktionen steuern, können die Effektivität von Gruppenrichtlinienadministratoren mit AGPM verbessern.</span><span class="sxs-lookup"><span data-stu-id="d3334-107">Understanding the parts of AGPM and related items, how they store GPOs in the file system, and how permissions control the actions available to each user role can improve Group Policy administrators' effectiveness with AGPM.</span></span>

## <span data-ttu-id="d3334-108">Terminologie</span><span class="sxs-lookup"><span data-stu-id="d3334-108">Terminology</span></span>


<span data-ttu-id="d3334-109">Im folgenden werden die grundlegenden AGPM-Ausdrücke erläutert.</span><span class="sxs-lookup"><span data-stu-id="d3334-109">The following explains the basic AGPM terms.</span></span>

-   <span data-ttu-id="d3334-110">**AGPM-Client:** Einen Computer, auf dem das AGPM-Snap-in für die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) ausgeführt wird und von dem Gruppenrichtlinienadministratoren GPOs verwalten.</span><span class="sxs-lookup"><span data-stu-id="d3334-110">**AGPM Client:** A computer that runs the AGPM snap-in for the Group Policy Management Console (GPMC) and from which Group Policy administrators manage GPOs.</span></span>

-   <span data-ttu-id="d3334-111">**AGPM-Snap-in:** Die Softwarekomponente von AGPM, die auf AGPM-Clients installiert ist, damit Sie GPOs verwalten können.</span><span class="sxs-lookup"><span data-stu-id="d3334-111">**AGPM snap-in:** The software component of AGPM installed on AGPM Clients so that they can manage GPOs.</span></span>

-   <span data-ttu-id="d3334-112">**AGPM-Server:** Ein Server, der den AGPM-Dienst ausführt und ein Archiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="d3334-112">**AGPM Server:** A server that runs the AGPM Service and manages an archive.</span></span> <span data-ttu-id="d3334-113">Jeder AGPM-Server kann nur ein Archiv verwalten, aber ein AGPM-Server kann Archivdaten für mehrere Domänen in einem Archiv verwalten.</span><span class="sxs-lookup"><span data-stu-id="d3334-113">Each AGPM Server can manage only one archive, but one AGPM Server can manage archive data for multiple domains in one archive.</span></span> <span data-ttu-id="d3334-114">Ein Archiv kann auf einem anderen Computer als einem AGPM-Server gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="d3334-114">An archive can be hosted on a computer other than an AGPM Server.</span></span>

-   <span data-ttu-id="d3334-115">**AGPM-Dienst:** Die Softwarekomponente von AGPM, die auf einem AGPM-Server als Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3334-115">**AGPM Service:** The software component of AGPM that runs on an AGPM Server as a service.</span></span> <span data-ttu-id="d3334-116">Der Dienst verwaltet GPOs im Archiv und in der Produktionsumgebung in dieser Gesamtstruktur.</span><span class="sxs-lookup"><span data-stu-id="d3334-116">The service manages GPOs in the archive and in the production environment in that forest.</span></span>

-   <span data-ttu-id="d3334-117">**Archivieren:** In AGPM handelt es sich um einen zentralen Speicher, der die gesteuerten GPOs enthält, die der zugeordnete AGPM-Server zusätzlich zum Verlauf für jedes dieser GPOs verwaltet.</span><span class="sxs-lookup"><span data-stu-id="d3334-117">**Archive:** In AGPM, a central store that contains the controlled GPOs that the associated AGPM Server manages, in addition to the history for each of those GPOs.</span></span> <span data-ttu-id="d3334-118">Dazu gehören alle vorherigen kontrollierten Versionen der einzelnen Gruppenrichtlinienobjekte.</span><span class="sxs-lookup"><span data-stu-id="d3334-118">This includes all previous controlled versions of each GPO.</span></span> <span data-ttu-id="d3334-119">Ein Archiv besteht aus einer Archivindexdatei und zugehörigen Archivdaten, die Daten für GPOs in mehreren Domänen enthalten können.</span><span class="sxs-lookup"><span data-stu-id="d3334-119">An archive consists of an archive index file and associated archive data that may include data for GPOs in multiple domains.</span></span> <span data-ttu-id="d3334-120">Ein Archiv kann auf einem anderen Computer als einem AGPM-Server gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="d3334-120">An archive can be hosted on a computer other than an AGPM Server.</span></span>

-   <span data-ttu-id="d3334-121">**Gesteuertes Gruppenrichtlinienobjekt:** Ein GPO, das von AGPM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="d3334-121">**Controlled GPO:** A GPO that is being managed by AGPM.</span></span> <span data-ttu-id="d3334-122">AGPM verwaltet das Protokoll und die Berechtigungen für gesteuerte GPOs, die im Archiv gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="d3334-122">AGPM manages the history and permissions of controlled GPOs, which it stores in the archive.</span></span>

-   <span data-ttu-id="d3334-123">**Ungesteuertes Gruppenrichtlinienobjekt:** Ein GPO in der Produktionsumgebung für eine Domäne, das nicht von AGPM verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="d3334-123">**Uncontrolled GPO:** A GPO in the production environment for a domain and not managed by AGPM.</span></span>

## <span data-ttu-id="d3334-124">Was AGPM installiert, erstellt und beeinflusst</span><span class="sxs-lookup"><span data-stu-id="d3334-124">What AGPM installs, creates, and affects</span></span>


<span data-ttu-id="d3334-125">Auf einem AGPM-Server installiert das AGPM-Setup Programm den AGPM-Dienst.</span><span class="sxs-lookup"><span data-stu-id="d3334-125">On an AGPM Server, the AGPM Setup program installs the AGPM Service.</span></span> <span data-ttu-id="d3334-126">AGPM ändert den Active Directory®-Verzeichnisdienst oder das Schema nicht.</span><span class="sxs-lookup"><span data-stu-id="d3334-126">AGPM does not alter the Active Directory® directory service or the schema.</span></span> <span data-ttu-id="d3334-127">Standardmäßig werden die AGPM-Server-Programmdateien in%ProgramFiles%\\Microsoft\\AGPM\\Server. installiert.</span><span class="sxs-lookup"><span data-stu-id="d3334-127">By default, the AGPM Server program files are installed in %ProgramFiles%\\Microsoft\\AGPM\\Server.</span></span> <span data-ttu-id="d3334-128">Sie können den AGPM-Dienst auf einem Domänencontroller installieren, wenn dies der Fall ist. Es wird jedoch empfohlen, den AGPM-Dienst auf einem Mitgliedsserver zu installieren.</span><span class="sxs-lookup"><span data-stu-id="d3334-128">You can install the AGPM Service on a domain controller if you have to; however, we recommend that you install the AGPM Service on a member server.</span></span>

<span data-ttu-id="d3334-129">Auf einem AGPM-Client installiert das AGPM-Setup Programm das AGPM-Snap-in und fügt jeder Domäne, die in der GPMC angezeigt wird, einen Ordner zum **Ändern des Steuerelements** hinzu.</span><span class="sxs-lookup"><span data-stu-id="d3334-129">On an AGPM Client, the AGPM Setup program installs the AGPM snap-in, adding a **Change Control** folder to each domain that appears in the GPMC.</span></span> <span data-ttu-id="d3334-130">Standardmäßig werden die AGPM-Client Programmdateien in%ProgramFiles%\\Microsoft\\AGPM\\Client. installiert.</span><span class="sxs-lookup"><span data-stu-id="d3334-130">By default, the AGPM Client program files are installed in %ProgramFiles%\\Microsoft\\AGPM\\Client.</span></span>

<span data-ttu-id="d3334-131">Tabelle 1 beschreibt sowohl die Elemente, die AGPM installiert oder erstellt, als auch die Teile des Betriebssystems, die sich auf den AGPM-Vorgang auswirken.</span><span class="sxs-lookup"><span data-stu-id="d3334-131">Table 1 describes both the items that AGPM installs or creates and the parts of the operating system that affect AGPM operation.</span></span>

**<span data-ttu-id="d3334-132">Tabelle 1: installierte, erstellte oder von AGPM betroffene Elemente</span><span class="sxs-lookup"><span data-stu-id="d3334-132">Table 1: Items installed, created, or affected by AGPM</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d3334-133">Element</span><span class="sxs-lookup"><span data-stu-id="d3334-133">Item</span></span></th>
<th align="left"><span data-ttu-id="d3334-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3334-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d3334-135">AGPM-Dienst</span><span class="sxs-lookup"><span data-stu-id="d3334-135">AGPM Service</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-136">Der AGPM-Dienst wird auf dem AGPM-Server ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3334-136">The AGPM Service runs on the AGPM Server.</span></span> <span data-ttu-id="d3334-137">Der Dienst verwaltet das Archiv, das Offline-GPOs enthält, und gesteuerte GPOs in der Produktionsumgebung.</span><span class="sxs-lookup"><span data-stu-id="d3334-137">The service manages the archive, which contains offline GPOs, and controlled GPOs in the production environment.</span></span> <span data-ttu-id="d3334-138">Die Standardkonfiguration des AGPM-Diensts lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d3334-138">The default configuration of the AGPM Service is as follows:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="d3334-139">Dienstname: </strong> AGPM-Dienst</span><span class="sxs-lookup"><span data-stu-id="d3334-139">Service name:</strong> AGPM Service</span></span></p></li>
<li><p><strong><span data-ttu-id="d3334-140">Anzeigename: </strong> AGPM-Dienst</span><span class="sxs-lookup"><span data-stu-id="d3334-140">Display name:</strong> AGPM Service</span></span></p></li>
<li><p><strong><span data-ttu-id="d3334-141">Pfad zur ausführbaren Datei: </strong> % Programme% \Microsoft\AGPM\Server\Agpm.exe</span><span class="sxs-lookup"><span data-stu-id="d3334-141">Path to executable:</strong> %ProgramFiles%\Microsoft\AGPM\Server\Agpm.exe</span></span></p></li>
<li><p><strong><span data-ttu-id="d3334-142">Start: </strong> automatisch</span><span class="sxs-lookup"><span data-stu-id="d3334-142">Startup:</strong> Automatic</span></span></p></li>
<li><p><strong><span data-ttu-id="d3334-143">Melden Sie sich als: </strong> AGPM-Dienstkonto an, das während der Installation von AGPM Server angegeben wurde und die mithilfe von <strong> Programmen und Funktionen </strong> in der Systemsteuerung geändert werden kann <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="d3334-143">Log on as:</strong> AGPM Service Account specified during installation of AGPM Server, which can be changed using <strong>Programs and Features</strong> in the <strong>Control Panel</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d3334-144">AGPM-Archiv</span><span class="sxs-lookup"><span data-stu-id="d3334-144">AGPM archive</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-145">Standardmäßig erstellt AGPM das Archiv in%ProgramData%\Microsoft\AGPM auf dem AGPM-Server.</span><span class="sxs-lookup"><span data-stu-id="d3334-145">By default, AGPM creates the archive in %ProgramData%\Microsoft\AGPM on the AGPM Server.</span></span> <span data-ttu-id="d3334-146">Das Archiv bietet Speicher für Offline-GPOs und kann mehrere Versionen der einzelnen Gruppenrichtlinienobjekte speichern.</span><span class="sxs-lookup"><span data-stu-id="d3334-146">The archive provides storage for offline GPOs, and it can store multiple versions of each GPO.</span></span> <span data-ttu-id="d3334-147">Änderungen, die AGPM an GPOs im Archiv vornimmt, haben keinen Einfluss auf die Produktionsumgebung, bis ein AGPM-Administrator oder eine genehmigende Person das Gruppenrichtlinienobjekt in der Produktionsumgebung bereitstellt und das Gruppenrichtlinienobjekt mit einer Organisationseinheit verknüpft.</span><span class="sxs-lookup"><span data-stu-id="d3334-147">Changes that AGPM makes to GPOs in the archive do not affect the production environment until an AGPM Administrator or Approver deploys the GPO to the production environment and links the GPO to an organizational unit (OU).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d3334-148">Windows-Firewall</span><span class="sxs-lookup"><span data-stu-id="d3334-148">Windows Firewall</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-149">Während der Installation aktiviert AGPM eine eingehende Windows-Firewall-Regel, die es dem AGPM-Client ermöglicht, mit dem AGPM-Server zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="d3334-149">During installation, AGPM enables an inbound Windows Firewall rule that allows the AGPM Client to communicate with the AGPM Server.</span></span> <span data-ttu-id="d3334-150">Die standardmäßige Windows-Firewall-Regel lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d3334-150">The default Windows Firewall rule is the following:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="d3334-151">Name: </strong> AGPM-Dienst</span><span class="sxs-lookup"><span data-stu-id="d3334-151">Name:</strong> AGPM Service</span></span></p></li>
<li><p><strong><span data-ttu-id="d3334-152">Aktion: </strong> Zulassen der Verbindung</span><span class="sxs-lookup"><span data-stu-id="d3334-152">Action:</strong> Allow the connection</span></span></p></li>
<li><p><strong><span data-ttu-id="d3334-153">Programme: </strong> Alle Programme, die den angegebenen Bedingungen entsprechen</span><span class="sxs-lookup"><span data-stu-id="d3334-153">Programs:</strong> All programs that meet the specified conditions</span></span></p></li>
<li><p><strong><span data-ttu-id="d3334-154">Protokolltyp: </strong> TCP</span><span class="sxs-lookup"><span data-stu-id="d3334-154">Protocol type:</strong> TCP</span></span></p></li>
<li><p><strong><span data-ttu-id="d3334-155">Lokaler Port: </strong> 4600</span><span class="sxs-lookup"><span data-stu-id="d3334-155">Local port:</strong> 4600</span></span></p></li>
<li><p><strong><span data-ttu-id="d3334-156">Remote-Port: </strong> alle Ports</span><span class="sxs-lookup"><span data-stu-id="d3334-156">Remote port:</strong> All ports</span></span></p></li>
<li><p><strong><span data-ttu-id="d3334-157">Lokale IP-Adresse: </strong> Any</span><span class="sxs-lookup"><span data-stu-id="d3334-157">Local IP address:</strong> Any</span></span></p></li>
<li><p><strong><span data-ttu-id="d3334-158">Remote-IP-Adresse: </strong> Any</span><span class="sxs-lookup"><span data-stu-id="d3334-158">Remote IP address:</strong> Any</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d3334-159">E-Mail-Server</span><span class="sxs-lookup"><span data-stu-id="d3334-159">E-mail server</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-160">AGPM verwendet SMTP (Simple Mail Transfer Protocol) zum Senden von e-Mail-Anforderungen an die Adressen, die auf der <strong> Registerkarte Domänendelegierung konfiguriert sind </strong> . Wenn ein Editor beispielsweise anfordert, dass ein neues Gruppenrichtlinienobjekt erstellt wird, benachrichtigt AGPM jede e-Mail-Adresse, die auf der <strong> Registerkarte "Domänendelegierung" angegeben ist </strong> .</span><span class="sxs-lookup"><span data-stu-id="d3334-160">AGPM uses Simple Mail Transfer Protocol (SMTP) to send e-mail requests to the addresses configured on the <strong>Domain Delegation</strong> tab. For example, when an Editor requests that a new GPO be created, AGPM notifies each e-mail address specified on the <strong>Domain Delegation</strong> tab.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d3334-161">AGPM-Snap-in</span><span class="sxs-lookup"><span data-stu-id="d3334-161">AGPM snap-in</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-162">Das AGPM-Snap-in für die GPMC wird auf AGPM-Clients ausgeführt und von Gruppenrichtlinienadministratoren zum Verwalten von GPOs verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3334-162">The AGPM snap-in for the GPMC runs on AGPM Clients and is used by Group Policy administrators to manage GPOs.</span></span> <span data-ttu-id="d3334-163">Das Snap-in wird in der GPMC als <strong> Ordner für die Änderungssteuerung </strong> in jeder Domäne angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d3334-163">The snap-in appears in the GPMC as a <strong>Change Control</strong> folder in each domain.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="d3334-164">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="d3334-164">Additional references</span></span>

<span data-ttu-id="d3334-165">Weitere Informationen zu den von AGPM installierten Dateien finden Sie im [Planungshandbuch für AGPM](https://go.microsoft.com/fwlink/?LinkId=160060).</span><span class="sxs-lookup"><span data-stu-id="d3334-165">For more information about the files installed by AGPM, see the [Planning Guide for AGPM](https://go.microsoft.com/fwlink/?LinkId=160060).</span></span>

## <span data-ttu-id="d3334-166">Archiv</span><span class="sxs-lookup"><span data-stu-id="d3334-166">Archive</span></span>


<span data-ttu-id="d3334-167">Standardmäßig erstellt der AGPM-Server Installationsvorgang das Archiv auf der lokalen Festplatte des AGPM-Servers unter%ProgramData%\\Microsoft\\AGPM.</span><span class="sxs-lookup"><span data-stu-id="d3334-167">By default, the AGPM Server installation process creates the archive on the local hard disk of the AGPM Server at %ProgramData%\\Microsoft\\AGPM.</span></span> <span data-ttu-id="d3334-168">Sie können den Pfad jedoch während der Installation ändern und sogar das Archiv auf einem anderen Server als dem AGPM-Server erstellen.</span><span class="sxs-lookup"><span data-stu-id="d3334-168">However, you can change the path during installation and even create the archive on a server other than the AGPM Server.</span></span>

<span data-ttu-id="d3334-169">Das Archiv enthält einen Unterordner für jede Version jedes GPO, das im Archiv enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d3334-169">The archive contains a subfolder for each version of each GPO the archive contains.</span></span> <span data-ttu-id="d3334-170">Der Name jedes Unterordners ist eine GUID, die eine Version des Gruppenrichtlinienobjekts identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d3334-170">The name of each subfolder is a GUID that identifies a version of the GPO.</span></span>

<span data-ttu-id="d3334-171">Die gpostate.xml-Datei zeichnet den Status der einzelnen Gruppenrichtlinienobjekte im Archiv auf.</span><span class="sxs-lookup"><span data-stu-id="d3334-171">The gpostate.xml file records the state of each GPO in the archive.</span></span> <span data-ttu-id="d3334-172">Die Datei ist ein Manifest, das den Inhalt des Archivs beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d3334-172">The file is a manifest that describes the contents of the archive.</span></span> <span data-ttu-id="d3334-173">Beispielsweise kann ein GPO viele Versionen aufweisen, und jede Version befindet sich in einem eigenen Unterordner im Archiv.</span><span class="sxs-lookup"><span data-stu-id="d3334-173">For example, a GPO can have many versions, and each version is in its own subfolder in the archive.</span></span> <span data-ttu-id="d3334-174">Die gpostate.xml-Datei gibt an, welche Unterordner verschiedene Versionen eines einzelnen Gruppenrichtlinienobjekts enthalten.</span><span class="sxs-lookup"><span data-stu-id="d3334-174">The gpostate.xml file indicates which subfolders contain different versions of a single GPO.</span></span> <span data-ttu-id="d3334-175">Darüber hinaus weisen GPO-Vorlagen Unterordner im Archiv auf, gpostate.xml aber darauf hinweisen, dass es sich um Vorlagen und nicht um gesteuerte GPOs handelt.</span><span class="sxs-lookup"><span data-stu-id="d3334-175">Additionally, GPO templates have subfolders in the archive, but gpostate.xml indicates that these are templates and not controlled GPOs.</span></span> <span data-ttu-id="d3334-176">Wenn Gruppenrichtlinien-Administratoren GPOs löschen, ändert AGPM ihre Status in gpostate.xml, um anzugeben, dass Sie sich im **Papierkorb** befinden, aber die Unterordner der GPOs nicht aus dem Archiv entfernen.</span><span class="sxs-lookup"><span data-stu-id="d3334-176">Similarly, when Group Policy administrators delete GPOs, AGPM changes their states in gpostate.xml to indicate that they are in the **Recycle Bin** but does not actually remove the GPOs' subfolders from the archive.</span></span>

<span data-ttu-id="d3334-177">**Vorsicht**  Bearbeiten Sie gpostate.xml oder die GPOs, die das Archiv enthält, nicht manuell.</span><span class="sxs-lookup"><span data-stu-id="d3334-177">**Caution** Do not manually edit gpostate.xml or the GPOs the archive contains.</span></span> <span data-ttu-id="d3334-178">Diese Informationen werden nur bereitgestellt, um das Verständnis des AGPM-Archivs zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="d3334-178">This information is provided only to enhance understanding of the AGPM archive.</span></span> <span data-ttu-id="d3334-179">Verwenden Sie stattdessen das AGPM-Snap-in, um GPOs zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d3334-179">Instead, use the AGPM snap-in to change GPOs.</span></span>

 

<span data-ttu-id="d3334-180">Wenn AGPM das Archiv erstellt, erhält er Vollzugriff auf System, Administratoren und das AGPM-Dienstkonto (angegeben im Setup von AGPM Server).</span><span class="sxs-lookup"><span data-stu-id="d3334-180">When AGPM creates the archive, it gives Full Control to SYSTEM, Administrators, and the AGPM Service Account (specified in the setup of AGPM Server).</span></span> <span data-ttu-id="d3334-181">Durch das Ändern von Berechtigungen mithilfe der AGPM-Benutzeroberfläche im AGPM-Snap-in werden die Berechtigungen für das Archiv nicht geändert, da das AGPM-Dienstkonto alle Vorgänge im Auftrag des angemeldeten Benutzers ausführt.</span><span class="sxs-lookup"><span data-stu-id="d3334-181">Changing permissions by using the AGPM user interface on the AGPM snap-in does not alter permissions on the archive, because the AGPM Service Account performs all operations on behalf of the logged-on user.</span></span>

### <span data-ttu-id="d3334-182">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="d3334-182">Additional references</span></span>

<span data-ttu-id="d3334-183">Informationen dazu, wie Sie das Archiv sichern, das Archiv aus einer Sicherung wiederherstellen oder sowohl den AGPM-Server als auch das Archiv verschieben, finden Sie im Abschnitt "Ausführen von AGPM-Administrator Aufgaben" im [Betriebshandbuch für AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).</span><span class="sxs-lookup"><span data-stu-id="d3334-183">For information about how to back up the archive, restore the archive from a backup, or move both the AGPM Server and the archive, see the "Performing AGPM Administrator Tasks" section in the [Operations Guide for AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).</span></span>

## <span data-ttu-id="d3334-184">Rollen und Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="d3334-184">Roles and permissions</span></span>


<span data-ttu-id="d3334-185">Rollen vereinfachen die Delegierung.</span><span class="sxs-lookup"><span data-stu-id="d3334-185">Roles simplify delegation.</span></span> <span data-ttu-id="d3334-186">Anstatt den Gruppenrichtlinienadministratoren detaillierte Berechtigungen zuzuweisen, können AGPM-Administratoren Gruppenrichtlinienadministratoren eine von vier Rollen zuweisen, damit diese Aufgaben im Zusammenhang mit dieser Rolle ausführen können:</span><span class="sxs-lookup"><span data-stu-id="d3334-186">Instead of assigning detailed permissions to Group Policy administrators, AGPM Administrators can assign one of four roles to Group Policy administrators to let them perform work related to that role:</span></span>

-   <span data-ttu-id="d3334-187">**AGPM-Administrator:** Gruppenrichtlinienadministratoren, denen die Rolle AGPM-Administrator (Vollzugriff) zugewiesen ist, können beliebige Aufgaben in AGPM ausführen.</span><span class="sxs-lookup"><span data-stu-id="d3334-187">**AGPM Administrator:** Group Policy administrators assigned the AGPM Administrator (Full Control) role can perform any task in AGPM.</span></span> <span data-ttu-id="d3334-188">AGPM-Administratoren können domänenweite Optionen konfigurieren und Berechtigungen an andere Gruppenrichtlinienadministratoren delegieren.</span><span class="sxs-lookup"><span data-stu-id="d3334-188">AGPM Administrators can configure domain-wide options and delegate permissions to other Group Policy administrators.</span></span>

-   <span data-ttu-id="d3334-189">**Genehmigende Person:** Gruppenrichtlinienadministratoren, denen die genehmigende Rolle zugewiesen ist, können GPOs für eine Domäne in der Produktionsumgebung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d3334-189">**Approver:** Group Policy administrators assigned the Approver role can deploy GPOs to the production environment for a domain.</span></span> <span data-ttu-id="d3334-190">Genehmigende Personen können auch GPOs erstellen und löschen sowie Anforderungen von Editoren genehmigen oder ablehnen.</span><span class="sxs-lookup"><span data-stu-id="d3334-190">Approvers can also create and delete GPOs and approve or reject requests from Editors.</span></span> <span data-ttu-id="d3334-191">Genehmigende Personen können die Liste der GPOs in einer Domäne anzeigen, die Richtlinieneinstellungen in GPOs anzeigen sowie Berichte zu den Richtlinieneinstellungen in einem Gruppenrichtlinienobjekt erstellen und anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d3334-191">Approvers can view the list of GPOs in a domain, view the policy settings in GPOs, and create and view reports of the policy settings in a GPO.</span></span> <span data-ttu-id="d3334-192">Sie können die Richtlinieneinstellungen nicht in GPOs bearbeiten, es sei denn, Ihnen wird auch die Rolle "Editor" zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="d3334-192">They cannot edit the policy settings in GPOs unless they are also assigned the Editor role.</span></span>

-   <span data-ttu-id="d3334-193">**Editor:** Gruppenrichtlinienadministratoren, denen die Editor Rolle zugewiesen ist, können die Liste der GPOs in einer Domäne anzeigen, die Richtlinieneinstellungen in GPOs anzeigen, die Richtlinieneinstellungen in GPOs bearbeiten sowie Berichte über die Richtlinieneinstellungen in einem Gruppenrichtlinienobjekt erstellen und anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d3334-193">**Editor:** Group Policy administrators assigned the Editor role can view the list of GPOs in a domain, view the policy settings in GPOs, edit the policy settings in GPOs, and create and view reports of the policy settings in a GPO.</span></span> <span data-ttu-id="d3334-194">Wenn Sie nicht auch der Rolle genehmigende Person zugewiesen sind, können die Bearbeiter keine GPOs erstellen, bereitstellen oder löschen.</span><span class="sxs-lookup"><span data-stu-id="d3334-194">Unless they are also assigned the Approver role, Editors cannot create, deploy, or delete GPOs.</span></span> <span data-ttu-id="d3334-195">Sie können jedoch anfordern, dass GPOs erstellt, bereitgestellt oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="d3334-195">However, they can request that GPOs be created, deployed, or deleted.</span></span>

-   <span data-ttu-id="d3334-196">**Bearbeiter:** Gruppenrichtlinienadministratoren, denen die Prüferrolle zugewiesen ist, können die Liste der GPOs in einer Domäne anzeigen und Berichte zu den Richtlinieneinstellungen in einem Gruppenrichtlinienobjekt erstellen und anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d3334-196">**Reviewer:** Group Policy administrators assigned the Reviewer role can view the list of GPOs in a domain and create and view reports of the policy settings in a GPO.</span></span> <span data-ttu-id="d3334-197">Sofern Ihnen nicht auch die Rolle des Editors zugewiesen ist, können Sie die Richtlinieneinstellungen in einem Gruppenrichtlinienobjekt nicht bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="d3334-197">Unless they are also assigned the Editor role, they cannot edit policy settings in a GPO.</span></span>

<span data-ttu-id="d3334-198">AGPM bietet AGPM-Administratoren die Flexibilität, Berechtigungen mit dem AGPM-Snap-in auf einer detaillierteren Ebene als Rollen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d3334-198">AGPM gives AGPM Administrators the flexibility to configure permissions at a more detailed level than roles by using the AGPM snap-in.</span></span> <span data-ttu-id="d3334-199">Tabelle 2 beschreibt diese Berechtigungen und gibt die Berechtigungen an, die den einzelnen Rollen standardmäßig gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="d3334-199">Table 2 describes these permissions and indicates the permissions granted to each role by default.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d3334-200">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="d3334-200">Permission</span></span></th>
<th align="left"><span data-ttu-id="d3334-201">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3334-201">Description</span></span></th>
<th align="left"><span data-ttu-id="d3334-202">AGPM-Administrator</span><span class="sxs-lookup"><span data-stu-id="d3334-202">AGPM Administrator</span></span></th>
<th align="left"><span data-ttu-id="d3334-203">Genehmiger</span><span class="sxs-lookup"><span data-stu-id="d3334-203">Approver</span></span></th>
<th align="left"><span data-ttu-id="d3334-204">Editor</span><span class="sxs-lookup"><span data-stu-id="d3334-204">Editor</span></span></th>
<th align="left"><span data-ttu-id="d3334-205">Prüfer</span><span class="sxs-lookup"><span data-stu-id="d3334-205">Reviewer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d3334-206">Vollzugriff</span><span class="sxs-lookup"><span data-stu-id="d3334-206">Full Control</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3334-207">Über alle Berechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="d3334-207">Have all permissions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-208">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-208">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d3334-209">Erstellen eines GPO</span><span class="sxs-lookup"><span data-stu-id="d3334-209">Create GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3334-210">Erstellen von GPOs in einer Domäne</span><span class="sxs-lookup"><span data-stu-id="d3334-210">Create GPOs in a domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-211">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-211">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-212">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-212">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d3334-213">Listeninhalt</span><span class="sxs-lookup"><span data-stu-id="d3334-213">List Contents</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3334-214">Listen Sie die GPOs in einer Domäne auf.</span><span class="sxs-lookup"><span data-stu-id="d3334-214">List the GPOs in a domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-215">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-215">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-216">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-216">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-217">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-217">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-218">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-218">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d3334-219">Leseeinstellungen</span><span class="sxs-lookup"><span data-stu-id="d3334-219">Read Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3334-220">Lesen Sie die Richtlinieneinstellungen in einem Gruppenrichtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="d3334-220">Read the policy settings within a GPO.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-221">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-221">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-222">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-222">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-223">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-223">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-224">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-224">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d3334-225">Bearbeiten von Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d3334-225">Edit Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3334-226">Ändern Sie die Richtlinieneinstellungen in einem Gruppenrichtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="d3334-226">Change the policy settings in a GPO.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-227">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-227">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d3334-228">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-228">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d3334-229">Gruppenrichtlinienobjekt löschen</span><span class="sxs-lookup"><span data-stu-id="d3334-229">Delete GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3334-230">Löschen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="d3334-230">Delete a GPO.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-231">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-231">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-232">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-232">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d3334-233">Ändern der Sicherheit</span><span class="sxs-lookup"><span data-stu-id="d3334-233">Modify Security</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3334-234">Delegieren Sie den Zugriff auf Domänenebene, delegieren Sie den Zugriff auf ein einzelnes GPO, und delegieren Sie den Zugriff auf die Produktionsumgebung.</span><span class="sxs-lookup"><span data-stu-id="d3334-234">Delegate domain-level access, delegate access to a single GPO, and delegate access to the production environment.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-235">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-235">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d3334-236">Bereitstellen von Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="d3334-236">Deploy GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3334-237">Stellen Sie ein GPO aus dem Archiv in der Produktionsumgebung bereit.</span><span class="sxs-lookup"><span data-stu-id="d3334-237">Deploy a GPO from the archive to the production environment.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-238">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-238">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-239">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-239">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d3334-240">Erstellen einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="d3334-240">Create Template</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3334-241">Erstellen einer GPO-Vorlage in AGPM</span><span class="sxs-lookup"><span data-stu-id="d3334-241">Create a GPO template in AGPM.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-242">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-242">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d3334-243">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-243">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d3334-244">Optionen ändern</span><span class="sxs-lookup"><span data-stu-id="d3334-244">Modify Options</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3334-245">Konfigurieren Sie die AGPM-e-Mail-Benachrichtigung, und begrenzen Sie die im Archiv gespeicherten Versionen von Gruppenrichtlinienobjekten.</span><span class="sxs-lookup"><span data-stu-id="d3334-245">Configure AGPM e-mail notification and limit the GPO versions stored in the archive.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-246">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-246">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d3334-247">Exportieren von Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="d3334-247">Export GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3334-248">Exportieren eines Gruppenrichtlinienobjekts in eine Datei</span><span class="sxs-lookup"><span data-stu-id="d3334-248">Export a GPO to a file.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-249">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-249">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d3334-250">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-250">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d3334-251">Importieren von Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="d3334-251">Import GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3334-252">Importieren Sie ein GPO aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="d3334-252">Import a GPO from a file.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3334-253">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-253">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d3334-254">Ja</span><span class="sxs-lookup"><span data-stu-id="d3334-254">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="d3334-255">**Hinweis** 
 Berechtigungen zum **Exportieren von Gruppenrichtlinienobjekten** und zum **Importieren von Gruppenrichtlinienobjekten** stehen in AGPM 3,0 oder 2,5 nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d3334-255">**Note**
**Export GPO** and **Import GPO** permissions are not available in AGPM 3.0 or 2.5.</span></span>

<span data-ttu-id="d3334-256">Die Möglichkeit, den Zugriff auf GPOs in der Produktionsumgebung für eine Domäne zu delegieren, und die Möglichkeit, die Anzahl der gespeicherten GPO-Versionen zu begrenzen, sind in AGPM 2,5 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d3334-256">The ability to delegate access to GPOs in the production environment for a domain and the ability to limit the number of GPO versions stored are not available in AGPM 2.5.</span></span>

 

### <span data-ttu-id="d3334-257">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="d3334-257">Additional references</span></span>

<span data-ttu-id="d3334-258">Informationen dazu, welche Aufgaben von Gruppenrichtlinienadministratoren ausgeführt werden können, denen eine bestimmte Rolle zugewiesen wurde oder über welche Berechtigungen zum Ausführen einer bestimmten Aufgabe erforderlich sind, finden Sie im [Betriebshandbuch für AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).</span><span class="sxs-lookup"><span data-stu-id="d3334-258">For information about what tasks can be performed by Group Policy administrators assigned a particular role or about which permissions are required to perform a specific task, see the [Operations Guide for AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).</span></span>

 

 





