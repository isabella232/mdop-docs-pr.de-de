---
title: Informationen zu MBAM 2.5
description: Informationen zu MBAM 2.5
author: dansimp
ms.assetid: 1ce218ec-4d2e-4a75-8d1a-68d737a8f3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d4c9ff0bc5ee3f7dc51a56cc428081a7c3783694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810420"
---
# <span data-ttu-id="83668-103">Informationen zu MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="83668-103">About MBAM 2.5</span></span>


<span data-ttu-id="83668-104">Die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 bietet eine vereinfachte Verwaltungsoberfläche für die BitLocker-Laufwerkverschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="83668-104">Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 provides a simplified administrative interface for BitLocker Drive Encryption.</span></span> <span data-ttu-id="83668-105">BitLocker bietet erweiterten Schutz vor Datendiebstahl oder Datengefährdung für Computer, die verloren gehen oder gestohlen werden.</span><span class="sxs-lookup"><span data-stu-id="83668-105">BitLocker offers enhanced protection against data theft or data exposure for computers that are lost or stolen.</span></span> <span data-ttu-id="83668-106">BitLocker verschlüsselt alle Daten, die auf den Volumes und Laufwerken des Windows-Betriebssystems gespeichert sind, und konfigurierte Datenlaufwerke.</span><span class="sxs-lookup"><span data-stu-id="83668-106">BitLocker encrypts all data that is stored on the Windows operating system volumes and drives and configured data drives.</span></span>

## <span data-ttu-id="83668-107">Übersicht über MBAM</span><span class="sxs-lookup"><span data-stu-id="83668-107">Overview of MBAM</span></span>


<span data-ttu-id="83668-108">MBAM 2,5 verfügt über die folgenden Features:</span><span class="sxs-lookup"><span data-stu-id="83668-108">MBAM 2.5 has the following features:</span></span>

-   <span data-ttu-id="83668-109">Administratoren können die Verschlüsselung von Volumes auf Clientcomputern unternehmensweit automatisieren.</span><span class="sxs-lookup"><span data-stu-id="83668-109">Enables administrators to automate the process of encrypting volumes on client computers across the enterprise.</span></span>

-   <span data-ttu-id="83668-110">Sicherheitsbeauftragte können den Kompatibilitätszustand einzelner Computer oder sogar des ganzen Unternehmens schnell ermitteln.</span><span class="sxs-lookup"><span data-stu-id="83668-110">Enables security officers to quickly determine the compliance state of individual computers or even of the enterprise itself.</span></span>

-   <span data-ttu-id="83668-111">Berichterstellung und Hardwareverwaltung können zentral mit Microsoft System Center Configuration Manager erfolgen.</span><span class="sxs-lookup"><span data-stu-id="83668-111">Provides centralized reporting and hardware management with Microsoft System Center Configuration Manager.</span></span>

-   <span data-ttu-id="83668-112">Verringert die Arbeitsbelastung des Helpdesks, um Endbenutzern die BitLocker-PIN-und Wiederherstellungsschlüssel Anforderungen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="83668-112">Reduces the workload on the Help Desk to assist end users with BitLocker PIN and recovery key requests.</span></span>

-   <span data-ttu-id="83668-113">Endbenutzer können verschlüsselte Geräte mithilfe des Self-Service-Portals eigenständig wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="83668-113">Enables end users to recover encrypted devices independently by using the Self-Service Portal.</span></span>

-   <span data-ttu-id="83668-114">Ermöglicht es Sicherheitsbeauftragten, den Zugriff auf die Wiederherstellung wichtiger Informationen einfach zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="83668-114">Enables security officers to easily audit access to recover key information.</span></span>

-   <span data-ttu-id="83668-115">Windows Enterprise-Benutzer können standortunabhängig arbeiten und sich dabei darauf verlassen, dass ihre Unternehmensdaten geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="83668-115">Empowers Windows Enterprise users to continue working anywhere with the assurance that their corporate data is protected.</span></span>

<span data-ttu-id="83668-116">MBAM erzwingt die BitLocker-Verschlüsselungsrichtlinien Optionen, die Sie für Ihr Unternehmen festzulegen, überwacht die Kompatibilität von Clientcomputern mit diesen Richtlinien und meldet den Verschlüsselungsstatus der Computer des Unternehmens und der einzelnen Personen.</span><span class="sxs-lookup"><span data-stu-id="83668-116">MBAM enforces the BitLocker encryption policy options that you set for your enterprise, monitors the compliance of client computers with those policies, and reports on the encryption status of the enterprise’s and individual’s computers.</span></span> <span data-ttu-id="83668-117">Darüber hinaus können Sie mit MBAM auf die Wiederherstellungsschlüssel Informationen zugreifen, wenn Benutzer Ihre PIN oder Ihr Kennwort vergessen oder wenn sich die BIOS-oder Startdatensätze ändern.</span><span class="sxs-lookup"><span data-stu-id="83668-117">In addition, MBAM lets you access the recovery key information when users forget their PIN or password, or when their BIOS or boot records change.</span></span>

<span data-ttu-id="83668-118">Die folgenden Gruppen sind möglicherweise an der Verwendung von MBAM für die Verwaltung von BitLocker interessiert:</span><span class="sxs-lookup"><span data-stu-id="83668-118">The following groups might be interested in using MBAM to manage BitLocker:</span></span>

-   <span data-ttu-id="83668-119">Administratoren, IT-Sicherheitsexperten und Compliance Officer, die dafür verantwortlich sind, sicherzustellen, dass vertrauliche Daten nicht ohne Autorisierung freigegeben werden</span><span class="sxs-lookup"><span data-stu-id="83668-119">Administrators, IT security professionals, and compliance officers who are responsible for ensuring that confidential data is not disclosed without authorization</span></span>

-   <span data-ttu-id="83668-120">Administratoren, die für die Computersicherheit in Remote-oder Zweigstellen zuständig sind</span><span class="sxs-lookup"><span data-stu-id="83668-120">Administrators who are responsible for computer security in remote or branch offices</span></span>

-   <span data-ttu-id="83668-121">Administratoren, die für Clientcomputer mit Windows verantwortlich sind</span><span class="sxs-lookup"><span data-stu-id="83668-121">Administrators who are responsible for client computers that are running Windows</span></span>

<span data-ttu-id="83668-122">**Hinweis**  BitLocker wird in dieser MBAM-Dokumentation nicht ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="83668-122">**Note** BitLocker is not explained in detail in this MBAM documentation.</span></span> <span data-ttu-id="83668-123">Weitere Informationen finden Sie unter [Übersicht über die BitLocker-Laufwerkverschlüsselung](https://go.microsoft.com/fwlink/p/?LinkId=225013).</span><span class="sxs-lookup"><span data-stu-id="83668-123">For more information, see [BitLocker Drive Encryption Overview](https://go.microsoft.com/fwlink/p/?LinkId=225013).</span></span>

 

## <a href="" id="what-s-new-in-mbam-2-5"></a><span data-ttu-id="83668-124">Neuerungen in MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="83668-124">What’s new in MBAM 2.5</span></span>


<span data-ttu-id="83668-125">In diesem Abschnitt werden die neuen Features in MBAM 2,5 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="83668-125">This section describes the new features in MBAM 2.5.</span></span>

### <span data-ttu-id="83668-126">Unterstützung für Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="83668-126">Support for Microsoft SQL Server 2014</span></span>

<span data-ttu-id="83668-127">MBAM fügt zusätzlich zur gleichen Software, die in früheren Versionen von MBAM unterstützt wird, Unterstützung für Microsoft SQL Server 2014 hinzu.</span><span class="sxs-lookup"><span data-stu-id="83668-127">MBAM adds support for Microsoft SQL Server 2014, in addition to the same software that is supported in earlier versions of MBAM.</span></span>

### <a href="" id="-------------mbam-group-policy-templates-downloaded-separately"></a> <span data-ttu-id="83668-128">MBAM-Gruppenrichtlinienvorlagen, die separat heruntergeladen wurden</span><span class="sxs-lookup"><span data-stu-id="83668-128">MBAM Group Policy Templates downloaded separately</span></span>

<span data-ttu-id="83668-129">Die Vorlagen für MBAM-Gruppenrichtlinien müssen separat aus der MBAM-Installation heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="83668-129">The MBAM Group Policy Templates must be downloaded separately from the MBAM installation.</span></span> <span data-ttu-id="83668-130">In früheren Versionen von MBAM umfasste das MBAM-Installationsprogramm eine MBAM-Richtlinienvorlage, die die erforderlichen MBAM-spezifischen Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) enthielt, die MBAM-Implementierungs Einstellungen für die BitLocker-Laufwerkverschlüsselung definieren.</span><span class="sxs-lookup"><span data-stu-id="83668-130">In previous versions of MBAM, the MBAM installer included an MBAM Policy Template, which contained the required MBAM-specific Group Policy Objects (GPOs) that define MBAM implementation settings for BitLocker Drive Encryption.</span></span> <span data-ttu-id="83668-131">Diese GPOs wurden aus dem MBAM-Installationsprogramm entfernt.</span><span class="sxs-lookup"><span data-stu-id="83668-131">These GPOs have been removed from the MBAM installer.</span></span> <span data-ttu-id="83668-132">Sie laden die GPOs jetzt herunter, indem Sie die [MDOP-Gruppenrichtlinien (ADMX)-Vorlagen abrufen](https://go.microsoft.com/fwlink/p/?LinkId=393941) und auf einen Server oder eine Arbeitsstation kopieren, bevor Sie mit der Installation des MBAM-Clients beginnen.</span><span class="sxs-lookup"><span data-stu-id="83668-132">You now download the GPOs from [How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941) and copy them to a server or workstation before you begin the MBAM Client installation.</span></span> <span data-ttu-id="83668-133">Sie können die Vorlagen für Gruppenrichtlinien auf alle Server oder Workstations kopieren, auf denen eine unterstützte Version des Windows-Servers oder Windows-Betriebssystems ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83668-133">You can copy the Group Policy Templates to any server or workstation that is running a supported version of the Windows Server or Windows operating system.</span></span>

<span data-ttu-id="83668-134">**Wichtig**  Ändern Sie die Gruppenrichtlinieneinstellungen im **BitLocker Drive Encryption** -Knoten nicht, oder MBAM wird nicht ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="83668-134">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node, or MBAM will not work correctly.</span></span> <span data-ttu-id="83668-135">Wenn Sie die Gruppenrichtlinieneinstellungen im MDOP- **MBAM (BitLocker-Verwaltungsknoten)** konfigurieren, konfiguriert MBAM automatisch die BitLocker-Laufwerk Verschlüsselungseinstellungen für Sie.</span><span class="sxs-lookup"><span data-stu-id="83668-135">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the BitLocker Drive Encryption settings for you.</span></span>

 

<span data-ttu-id="83668-136">Die Vorlagendateien, die Sie auf einen Server oder eine Workstation kopieren müssen, sind:</span><span class="sxs-lookup"><span data-stu-id="83668-136">The template files that you need to copy to a server or workstation are:</span></span>

-   <span data-ttu-id="83668-137">BitLockerManagement. ADML</span><span class="sxs-lookup"><span data-stu-id="83668-137">BitLockerManagement.adml</span></span>

-   <span data-ttu-id="83668-138">BitLockerManagement. ADMX</span><span class="sxs-lookup"><span data-stu-id="83668-138">BitLockerManagement.admx</span></span>

-   <span data-ttu-id="83668-139">BitLockerUserManagement. ADML</span><span class="sxs-lookup"><span data-stu-id="83668-139">BitLockerUserManagement.adml</span></span>

-   <span data-ttu-id="83668-140">BitLockerUserManagement. ADMX</span><span class="sxs-lookup"><span data-stu-id="83668-140">BitLockerUserManagement.admx</span></span>

<span data-ttu-id="83668-141">Kopieren Sie die Vorlagendateien an die Stelle, die Ihren Anforderungen am besten entspricht.</span><span class="sxs-lookup"><span data-stu-id="83668-141">Copy the template files to the location that best meets your needs.</span></span> <span data-ttu-id="83668-142">Für die sprachspezifischen Dateien, die in einen sprachspezifischen Ordner kopiert werden müssen, ist die Gruppenrichtlinien-Verwaltungskonsole erforderlich, um die Dateien anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="83668-142">For the language-specific files, which must be copied to a language-specific folder, the Group Policy Management Console is required to view the files.</span></span>

- <span data-ttu-id="83668-143">Wenn Sie die Vorlagendateien lokal auf einem Server oder einer Arbeitsstation installieren möchten, kopieren Sie die Dateien an einen der folgenden Speicherorte.</span><span class="sxs-lookup"><span data-stu-id="83668-143">To install the template files locally on a server or workstation, copy the files to one of the following locations.</span></span>

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th align="left"><span data-ttu-id="83668-144">Dateityp</span><span class="sxs-lookup"><span data-stu-id="83668-144">File type</span></span></th>
  <th align="left"><span data-ttu-id="83668-145">Dateispeicherort</span><span class="sxs-lookup"><span data-stu-id="83668-145">File location</span></span></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td align="left"><p><span data-ttu-id="83668-146">sprachneutral (ADMX)</span><span class="sxs-lookup"><span data-stu-id="83668-146">language neutral (.admx)</span></span></p></td>
  <td align="left"><p><em><span data-ttu-id="83668-147">% systemroot% </em> \policyDefinitions</span><span class="sxs-lookup"><span data-stu-id="83668-147">%systemroot%</em>\policyDefinitions</span></span></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="83668-148">sprachspezifisch (. ADML)</span><span class="sxs-lookup"><span data-stu-id="83668-148">language specific (.adml)</span></span></p></td>
  <td align="left"><p><em><span data-ttu-id="83668-149">% systemroot% </em> \policyDefinitions [ <em> MUIculture </em> ] (beispielsweise wird die spezifische Datei für die US-englische Sprache in <em> % systemroot% &lt; /EM policyDefinitions\en-US gespeichert &gt; )</span><span class="sxs-lookup"><span data-stu-id="83668-149">%systemroot%</em>\policyDefinitions[<em>MUIculture</em>] (for example, the U.S. English language specific file will be stored in <em>%systemroot%&lt;/em&gt;policyDefinitions\en-us)</span></span></p></td>
  </tr>
  </tbody>
  </table>

     

- <span data-ttu-id="83668-150">Wenn Sie die Vorlagen für alle Gruppenrichtlinienadministratoren in einer Domäne verfügbar machen möchten, kopieren Sie die Dateien an einen der folgenden Speicherorte auf einem Domänencontroller.</span><span class="sxs-lookup"><span data-stu-id="83668-150">To make the templates available to all Group Policy administrators in a domain, copy the files to one of the following locations on a domain controller.</span></span>

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th align="left"><span data-ttu-id="83668-151">Dateityp</span><span class="sxs-lookup"><span data-stu-id="83668-151">File type</span></span></th>
  <th align="left"><span data-ttu-id="83668-152">Speicherort der Domänencontroller Datei</span><span class="sxs-lookup"><span data-stu-id="83668-152">Domain controller file location</span></span></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td align="left"><p><span data-ttu-id="83668-153">Sprachneutral (ADMX)</span><span class="sxs-lookup"><span data-stu-id="83668-153">Language neutral (.admx)</span></span></p></td>
  <td align="left"><p><em><span data-ttu-id="83668-154">% systemroot% </em> sysvol\domain\policies\PolicyDefinitions</span><span class="sxs-lookup"><span data-stu-id="83668-154">%systemroot%</em>sysvol\domain\policies\PolicyDefinitions</span></span></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="83668-155">Sprachspezifisch (. ADML)</span><span class="sxs-lookup"><span data-stu-id="83668-155">Language specific (.adml)</span></span></p></td>
  <td align="left"><p><em><span data-ttu-id="83668-156">% systemroot% </em> \sysvol\domain\policies\PolicyDefinitions [ <em> MUIculture </em> ] (Beispiel: die sprachspezifische US-Datei wird in <em> % systemroot% \sysvol\domain\policies\PolicyDefinitions\en-US gespeichert </em> )</span><span class="sxs-lookup"><span data-stu-id="83668-156">%systemroot%</em>\sysvol\domain\policies\PolicyDefinitions[<em>MUIculture</em>] (for example, the U.S. English language-specific file will be stored in <em>%systemroot%</em>\sysvol\domain\policies\PolicyDefinitions\en-us)</span></span></p></td>
  </tr>
  </tbody>
  </table>

     

<span data-ttu-id="83668-157">Weitere Informationen zu Vorlagendateien finden Sie unter [Verwalten von Gruppenrichtlinien-ADMX-Dateien – Schritt-für-Schritt-Anleitung](https://go.microsoft.com/fwlink/?LinkId=392818).</span><span class="sxs-lookup"><span data-stu-id="83668-157">For more information about template files, see [Managing Group Policy ADMX Files Step-by-Step Guide](https://go.microsoft.com/fwlink/?LinkId=392818).</span></span>

### <span data-ttu-id="83668-158">Möglichkeit zum Erzwingen von Verschlüsselungsrichtlinien für Betriebssystem-und fest Netzlaufwerke</span><span class="sxs-lookup"><span data-stu-id="83668-158">Ability to enforce encryption policies on operating system and fixed data drives</span></span>

<span data-ttu-id="83668-159">Mit MBAM 2.5 können Sie Verschlüsselungsrichtlinien für das Betriebssystem und feste Datenlaufwerke für Computer in Ihrer Organisation erzwingen und die Anzahl der Tage begrenzen, die Endbenutzer eine Verschiebung der Anforderung zur Einhaltung der MBAM-Verschlüsselungsrichtlinien anfordern können.</span><span class="sxs-lookup"><span data-stu-id="83668-159">MBAM2.5 enables you to enforce encryption policies on operating system and fixed data drives for computers in your organization and limit the number of days that end users can request a postponement of the requirement to comply with MBAM encryption policies.</span></span>

<span data-ttu-id="83668-160">Damit Sie die Verschlüsselungsrichtlinien Erzwingung konfigurieren können, wurde eine neue Gruppenrichtlinieneinstellung namens Verschlüsselungsrichtlinien Erzwingungseinstellungen für Betriebssystemlaufwerke und fest Netzlaufwerke hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="83668-160">To enable you to configure encryption policy enforcement, a new Group Policy setting, called Encryption Policy Enforcement Settings, has been added for operating system drives and fixed data drives.</span></span> <span data-ttu-id="83668-161">Diese Richtlinie wird in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="83668-161">This policy is described in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="83668-162">Gruppenrichtlinieneinstellung</span><span class="sxs-lookup"><span data-stu-id="83668-162">Group Policy setting</span></span></th>
<th align="left"><span data-ttu-id="83668-163">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83668-163">Description</span></span></th>
<th align="left"><span data-ttu-id="83668-164">Zum Konfigurieren dieser Einstellung verwendeter Gruppenrichtlinien Knoten</span><span class="sxs-lookup"><span data-stu-id="83668-164">Group Policy node used to configure this setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83668-165">Einstellungen für die Verschlüsselungsrichtlinien Erzwingung (Betriebs System Laufwerk)</span><span class="sxs-lookup"><span data-stu-id="83668-165">Encryption Policy Enforcement Settings (Operating System Drive)</span></span></p></td>
<td align="left"><p><span data-ttu-id="83668-166">Verwenden Sie für diese Einstellung die Option <strong> Konfigurieren der Anzahl der nicht Konformitäts kulanztage für Betriebssystemlaufwerke </strong> , um einen Kulanzzeitraum zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="83668-166">For this setting, use the option <strong>Configure the number of noncompliance grace period days for operating system drives</strong> to configure a grace period.</span></span></p>
<p><span data-ttu-id="83668-167">Der Kulanzzeitraum gibt die Anzahl der Tage an, die Endbenutzer die Einhaltung der MBAM-Richtlinien für Ihr Betriebssystemlaufwerk verschieben können, nachdem das Laufwerk zunächst als nicht kompatibel erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="83668-167">The grace period specifies the number of days that end users can postpone compliance with MBAM policies for their operating system drive after the drive is first detected as noncompliant.</span></span></p>
<p><span data-ttu-id="83668-168">Nach Ablauf der konfigurierten Kulanzzeit können Benutzer die erforderliche Aktion nicht verschieben oder eine Ausnahme von ihr anfordern.</span><span class="sxs-lookup"><span data-stu-id="83668-168">After the configured grace period expires, users cannot postpone the required action or request an exemption from it.</span></span></p>
<p><span data-ttu-id="83668-169">Wenn Benutzerinteraktionen erforderlich sind (wenn Sie beispielsweise das TPM (Trusted Platform Module) +-PIN verwenden oder einen Kennwortschutz verwenden), wird ein Dialogfeld angezeigt, und die Benutzer können es erst schließen, wenn Sie die erforderlichen Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="83668-169">If user interaction is required (for example, if you are using the Trusted Platform Module (TPM) + PIN or using a password protector), a dialog box appears, and users cannot close it until they provide the required information.</span></span> <span data-ttu-id="83668-170">Wenn es sich bei dem Protector nur um ein TPM handelt, beginnt die Verschlüsselung sofort im Hintergrund ohne Benutzereingaben.</span><span class="sxs-lookup"><span data-stu-id="83668-170">If the protector is TPM only, encryption begins immediately in the background without user input.</span></span></p>
<p><span data-ttu-id="83668-171">Benutzer können keine Ausnahmen über den BitLocker-Verschlüsselungs-Assistenten anfordern.</span><span class="sxs-lookup"><span data-stu-id="83668-171">Users cannot request exemptions through the BitLocker encryption wizard.</span></span> <span data-ttu-id="83668-172">Stattdessen müssen Sie sich an den Helpdesk wenden oder den von Ihrer Organisation verwendeten Prozess für Ausnahmeanforderungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="83668-172">Instead, they must contact their Help Desk or use whatever process their organization uses for exemption requests.</span></span></p></td>
<td align="left"><p><span data-ttu-id="83668-173">Computerkonfigurations &gt; Richtlinien &gt; Administrative Vorlagen &gt; Windows Components &gt; MDOP MBAM (BitLocker-Verwaltungs-) &gt; Betriebs System Laufwerk</span><span class="sxs-lookup"><span data-stu-id="83668-173">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; Windows Components &gt; MDOP MBAM (BitLocker Management) &gt; Operating System Drive</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83668-174">Einstellungen für die Verschlüsselungsrichtlinien Erzwingung (feste Datenlaufwerke)</span><span class="sxs-lookup"><span data-stu-id="83668-174">Encryption Policy Enforcement Settings (Fixed Data Drives)</span></span></p></td>
<td align="left"><p><span data-ttu-id="83668-175">Verwenden Sie für diese Einstellung die Option <strong> Konfigurieren Sie die Anzahl der kulanztage für Nichtkonformität für Festplatten, </strong> um einen Kulanzzeitraum zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="83668-175">For this setting, use the option <strong>Configure the number of noncompliance grace period days for fixed drives</strong> to configure a grace period.</span></span></p>
<p><span data-ttu-id="83668-176">Der Kulanzzeitraum gibt an, wie viele Tage Endbenutzer die Einhaltung der MBAM-Richtlinien für ihr festes Laufwerk verschieben können, nachdem das Laufwerk zunächst als nicht kompatibel erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="83668-176">The grace period specifies the number of days that end users can postpone compliance with MBAM policies for their fixed drive after the drive is first detected as noncompliant.</span></span></p>
<p><span data-ttu-id="83668-177">Die Nachfrist beginnt, wenn das festgelegte Laufwerk als nicht kompatibel festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="83668-177">The grace period begins when the fixed drive is determined to be noncompliant.</span></span> <span data-ttu-id="83668-178">Wenn Sie die automatische Sperrung verwenden, wird die Richtlinie erst erzwungen, wenn das Betriebssystemlaufwerk kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="83668-178">If you are using auto-unlock, the policy will not be enforced until the operating system drive is compliant.</span></span> <span data-ttu-id="83668-179">Wenn Sie die automatische Sperrung jedoch nicht verwenden, kann die Verschlüsselung des festen Datenlaufwerks beginnen, bevor das Betriebssystemlaufwerk vollständig verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="83668-179">However, if you are not using auto-unlock, encryption of the fixed data drive can begin before the operating system drive is fully encrypted.</span></span></p>
<p><span data-ttu-id="83668-180">Nach Ablauf der konfigurierten Kulanzzeit können Benutzer die erforderliche Aktion nicht verschieben oder eine Ausnahme von ihr anfordern.</span><span class="sxs-lookup"><span data-stu-id="83668-180">After the configured grace period expires, users cannot postpone the required action or request an exemption from it.</span></span> <span data-ttu-id="83668-181">Wenn Benutzerinteraktionen erforderlich sind, wird ein Dialogfeld angezeigt, und Benutzer können es erst dann schließen, wenn Sie die erforderlichen Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="83668-181">If user interaction is required, a dialog box appears and users cannot close it until they provide the required information.</span></span></p></td>
<td align="left"><p><span data-ttu-id="83668-182">Computerkonfigurations &gt; Richtlinien &gt; Administrative Vorlagen &gt; Windows Components &gt; MDOP MBAM (BitLocker-Verwaltung) &gt; festes Laufwerk</span><span class="sxs-lookup"><span data-stu-id="83668-182">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; Windows Components &gt; MDOP MBAM (BitLocker Management) &gt; Fixed Drive</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="83668-183">Möglichkeit zum Bereitstelleneiner URL im BitLocker-Laufwerk Verschlüsselungs-Assistenten, um auf Ihre Sicherheitsrichtlinie zu verweisen</span><span class="sxs-lookup"><span data-stu-id="83668-183">Ability to provide a URL in the BitLocker Drive Encryption wizard to point to your security policy</span></span>

<span data-ttu-id="83668-184">Mit einer neuen Gruppenrichtlinieneinstellung, **die die URL für den Link "Sicherheitsrichtlinie" enthält**, können Sie eine URL konfigurieren, die Endbenutzern als Link " **Unternehmenssicherheitsrichtlinie**" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="83668-184">A new Group Policy setting, **Provide the URL for the Security Policy link**, enables you to configure a URL that will be presented to end users as a link called **Company Security Policy**.</span></span> <span data-ttu-id="83668-185">Dieser Link wird angezeigt, wenn MBAM Benutzer zur Verschlüsselung eines Volumes auffordert.</span><span class="sxs-lookup"><span data-stu-id="83668-185">This link will appear when MBAM prompts users to encrypt a volume.</span></span>

<span data-ttu-id="83668-186">Wenn Sie diese Richtlinieneinstellung aktivieren, können Sie die URL für den Link für die **Sicherheitsrichtlinie für Unternehmen** konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="83668-186">If you enable this policy setting, you can configure the URL for the **Company Security Policy** link.</span></span> <span data-ttu-id="83668-187">Wenn Sie diese Richtlinieneinstellung deaktivieren oder nicht konfigurieren, wird der Link **Unternehmenssicherheitsrichtlinie** für die Benutzer nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="83668-187">If you disable or do not configure this policy setting, the **Company Security Policy** link is not displayed to users.</span></span>

<span data-ttu-id="83668-188">Die neue Gruppenrichtlinieneinstellung befindet sich im folgenden GPO-Knoten: **Computerkonfigurations** &gt; **Richtlinien** &gt; **Administrative Vorlagen** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker-Verwaltung) &gt; Client Verwaltung**.</span><span class="sxs-lookup"><span data-stu-id="83668-188">The new Group Policy setting is located in the following GPO node: **Computer Configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management) &gt; Client Management**.</span></span>

### <span data-ttu-id="83668-189">Unterstützung für FIPS-konforme Wiederherstellungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="83668-189">Support for FIPS-compliant recovery keys</span></span>

<span data-ttu-id="83668-190">Mbam 2.5 unterstützt FIPS-konforme BitLocker-Wiederherstellungsschlüssel (Federal Information Processing Standard) auf Geräten, auf denen das BetriebssystemWindows 8.1 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83668-190">MBAM2.5 supports Federal Information Processing Standard (FIPS)-compliant BitLocker recovery keys on devices that are running the Windows8.1 operating system.</span></span> <span data-ttu-id="83668-191">Der Wiederherstellungsschlüssel war in früheren Versionen von Windows nicht FIPS-kompatibel.</span><span class="sxs-lookup"><span data-stu-id="83668-191">The recovery key was not FIPS compliant in earlier versions of Windows.</span></span> <span data-ttu-id="83668-192">Diese Erweiterung verbessert den Wiederherstellungsprozess in Organisationen, die FIPS-Konformität erfordern, da Endbenutzer das Self-Service-Portal oder die Verwaltungs-und Überwachungs Website (Help Desk) verwenden können, um Ihre Laufwerke wiederherzustellen, wenn Sie Ihre PIN oder Ihr Kennwort vergessen oder aus ihren Computern ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="83668-192">This enhancement improves the drive recovery process in organizations that require FIPS compliance because it enables end users to use the Self-Service Portal or Administration and Monitoring Website (Help Desk) to recover their drives if they forget their PIN or password or get locked out of their computers.</span></span> <span data-ttu-id="83668-193">Das neue FIPS-Konformitäts Feature erstreckt sich nicht auf Kennwortschutz.</span><span class="sxs-lookup"><span data-stu-id="83668-193">The new FIPS compliance feature does not extend to password protectors.</span></span>

<span data-ttu-id="83668-194">Um die FIPS-Konformität in Ihrer Organisation zu aktivieren, müssen Sie die FIPS-Gruppenrichtlinieneinstellungen (Federal Information Processing Standard) konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="83668-194">To enable FIPS compliance in your organization, you must configure the Federal Information Processing Standard (FIPS) Group Policy settings.</span></span> <span data-ttu-id="83668-195">Konfigurationsanweisungen finden Sie unter [BitLocker-Gruppenrichtlinieneinstellungen](https://go.microsoft.com/fwlink/?LinkId=393560).</span><span class="sxs-lookup"><span data-stu-id="83668-195">For configuration instructions, see [BitLocker Group Policy Settings](https://go.microsoft.com/fwlink/?LinkId=393560).</span></span>

<span data-ttu-id="83668-196">Bei Clientcomputern, auf denen das Windows8-oder Windows7-Betriebssystem ohne den [installierten BitLocker-Hotfix](https://support.microsoft.com/kb/3015477)ausgeführt wird, verwenden IT-Administratoren weiterhin die Daten Wiederherstellungs-Agents (DRA) in FIPS-kompatiblen Umgebungen.</span><span class="sxs-lookup"><span data-stu-id="83668-196">For client computers that are running the Windows8 or Windows7 operating systems without the [installed BitLocker hotfix](https://support.microsoft.com/kb/3015477), IT administrators will continue to use the Data Recovery Agents (DRA) protector in FIPS-compliant environments.</span></span> <span data-ttu-id="83668-197">Informationen zu DRA finden Sie unter [Verwenden von Daten Wiederherstellungs-Agents mit BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).</span><span class="sxs-lookup"><span data-stu-id="83668-197">For information about DRA, see [Using Data Recovery Agents with BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).</span></span>

<span data-ttu-id="83668-198">Informationen zum herunterladen und Installieren des BitLocker-Hotfixes für Windows 7-und Windows 8-Computer finden Sie unter [Hotfix-Paket 2 für die BitLocker-Verwaltung und-Überwachung 2,5](https://support.microsoft.com/kb/3015477) .</span><span class="sxs-lookup"><span data-stu-id="83668-198">See [Hotfix Package 2 for BitLocker Administration and Monitoring 2.5](https://support.microsoft.com/kb/3015477) to download and install the BitLocker hotfix for Windows 7 and Windows 8 computers.</span></span>

### <span data-ttu-id="83668-199">Unterstützung für Bereitstellungen mit höherer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="83668-199">Support for high availability deployments</span></span>

<span data-ttu-id="83668-200">MBAM unterstützt die folgenden Szenarien mit hoher Verfügbarkeit zusätzlich zu den Standard Topologien für zwei Server und Configuration Manager-Integration:</span><span class="sxs-lookup"><span data-stu-id="83668-200">MBAM supports the following high-availability scenarios in addition to the standard two-server and Configuration Manager Integration topologies:</span></span>

-   <span data-ttu-id="83668-201">Verfügbarkeitsgruppen für SQL Server-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="83668-201">SQL Server AlwaysOn availability groups</span></span>

-   <span data-ttu-id="83668-202">SQL Server-Clustering</span><span class="sxs-lookup"><span data-stu-id="83668-202">SQL Server clustering</span></span>

-   <span data-ttu-id="83668-203">Netzwerklastenausgleich (NLB)</span><span class="sxs-lookup"><span data-stu-id="83668-203">Network load balancing (NLB)</span></span>

-   <span data-ttu-id="83668-204">SQL Server-Spiegelung</span><span class="sxs-lookup"><span data-stu-id="83668-204">SQL Server mirroring</span></span>

-   <span data-ttu-id="83668-205">VSS-Sicherung (Volume Shadow Copy Service)</span><span class="sxs-lookup"><span data-stu-id="83668-205">Volume Shadow Copy Service (VSS) Backup</span></span>

<span data-ttu-id="83668-206">Weitere Informationen zu diesen Features finden Sie unter [Planen der MBAM 2,5-Höchstverfügbarkeit](planning-for-mbam-25-high-availability.md).</span><span class="sxs-lookup"><span data-stu-id="83668-206">For more information about these features, see [Planning for MBAM 2.5 High Availability](planning-for-mbam-25-high-availability.md).</span></span>

### <a href="" id="management-of-roles-for-administration-and-monitoring-website-changed-"></a><span data-ttu-id="83668-207">Verwaltung von Rollen für die Verwaltung und Überwachung der Website geändert</span><span class="sxs-lookup"><span data-stu-id="83668-207">Management of roles for Administration and Monitoring Website changed</span></span>

<span data-ttu-id="83668-208">In mbam 2.5 müssen Sie Sicherheitsgruppen in Active Directory-Domänendiensten (Adds) erstellen, um die Rollen zu verwalten, die Zugriffsrechte für die Website Verwaltung und Überwachung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="83668-208">In MBAM2.5, you must create security groups in Active Directory Domain Services (ADDS) to manage the roles that provide access rights to the Administration and Monitoring Website.</span></span> <span data-ttu-id="83668-209">Rollen ermöglichen Benutzern, die sich in bestimmten Sicherheitsgruppen befinden, verschiedene Aufgaben auf der Website auszuführen, wie etwa das Anzeigen von Berichten oder das unterstützen der Wiederherstellung verschlüsselter Laufwerke durch Endbenutzer.</span><span class="sxs-lookup"><span data-stu-id="83668-209">Roles enable users who are in specific security groups to perform different tasks in the website such as viewing reports or helping end users recover encrypted drives.</span></span> <span data-ttu-id="83668-210">In früheren Versionen von MBAM wurden Rollen mithilfe lokaler Gruppen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="83668-210">In previous versions of MBAM, roles were managed by using local groups.</span></span>

<span data-ttu-id="83668-211">In MBAM 2.5 ersetzt der Ausdruck "Rollen" den Ausdruck "Administratorrollen", der in früheren Versionen von MBAM verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="83668-211">In MBAM2.5, the term “roles” replaces the term “administrator roles,” which was used in earlier versions of MBAM.</span></span> <span data-ttu-id="83668-212">Darüber hinaus wurde in MBAM 2.5 die Rolle "MBAM-System Administratoren" entfernt.</span><span class="sxs-lookup"><span data-stu-id="83668-212">In addition, in MBAM2.5 the “MBAM System Administrators” role has been removed.</span></span>

<span data-ttu-id="83668-213">In der folgenden Tabelle sind die Sicherheitsgruppen aufgeführt, die Sie in AD DS erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="83668-213">The following table lists the security groups that you must create in AD DS.</span></span> <span data-ttu-id="83668-214">Sie können einen beliebigen Namen für die Sicherheitsgruppen verwenden.</span><span class="sxs-lookup"><span data-stu-id="83668-214">You can use any name for the security groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="83668-215">Rolle</span><span class="sxs-lookup"><span data-stu-id="83668-215">Role</span></span></th>
<th align="left"><span data-ttu-id="83668-216">Zugriffsrechte für diese Rolle auf der Website "Verwaltung und Überwachung"</span><span class="sxs-lookup"><span data-stu-id="83668-216">Access rights for this role on the Administration and Monitoring Website</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83668-217">MBAM Helpdesk-Benutzer</span><span class="sxs-lookup"><span data-stu-id="83668-217">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="83668-218">Bietet Zugriff auf die Bereiche Manage TPM und Drive Recovery der MBAM-Verwaltungs-und-Überwachungs Website.</span><span class="sxs-lookup"><span data-stu-id="83668-218">Provides access to the Manage TPM and Drive Recovery areas of the MBAM Administration and Monitoring Website.</span></span> <span data-ttu-id="83668-219">Benutzer, die auf diese Bereiche zugreifen können, müssen alle Felder ausfüllen, wenn Sie einen Bereich verwenden.</span><span class="sxs-lookup"><span data-stu-id="83668-219">Users who have access to these areas must fill in all fields when they use either area.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83668-220">MBAM-Berichtsbenutzer</span><span class="sxs-lookup"><span data-stu-id="83668-220">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="83668-221">Bietet Zugriff auf die Berichte auf der Website Verwaltung und Überwachung.</span><span class="sxs-lookup"><span data-stu-id="83668-221">Provides access to the Reports in the Administration and Monitoring Website.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83668-222">MBAM Advanced Helpdesk-Benutzer</span><span class="sxs-lookup"><span data-stu-id="83668-222">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="83668-223">Bietet Zugriff auf alle Bereiche auf der Website Verwaltung und Überwachung.</span><span class="sxs-lookup"><span data-stu-id="83668-223">Provides access to all areas in the Administration and Monitoring Website.</span></span> <span data-ttu-id="83668-224">Benutzer in dieser Gruppe müssen nur den Wiederherstellungsschlüssel eingeben, nicht die Domäne und den Benutzernamen des Endbenutzers, wenn Sie den Endbenutzern helfen, Ihre Laufwerke wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="83668-224">Users in this group have to enter only the recovery key, not the end user’s domain and user name, when helping end users recover their drives.</span></span> <span data-ttu-id="83668-225">Wenn ein Benutzer ein Mitglied der Gruppe "MBAM Helpdesk-Benutzer" und der Gruppe "Erweiterte Helpdesk-Benutzer" von MBAM ist, überschreiben die Berechtigungen der Gruppe "Erweiterte Helpdesk-Benutzer" die Berechtigungen der Gruppe "MBAM Helpdesk-Benutzer".</span><span class="sxs-lookup"><span data-stu-id="83668-225">If a user is a member of the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Users group permissions.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="83668-226">Nachdem Sie die Sicherheitsgruppen in "hinzugefügt" erstellt haben, weisen Sie der entsprechenden Sicherheitsgruppe Benutzer und/oder Gruppen zu, um die entsprechende Zugriffsebene auf die Website Verwaltung und Überwachung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="83668-226">After you create the security groups in ADDS, assign users and/or groups to the appropriate security group to enable the corresponding level of access to the Administration and Monitoring Website.</span></span> <span data-ttu-id="83668-227">Damit Personen mit jeder Rolle auf die Verwaltungs-und Überwachungs Website zugreifen können, müssen Sie auch jede Sicherheitsgruppe angeben, wenn Sie die Verwaltungs-und Überwachungs Website konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="83668-227">To enable individuals with each role to access the Administration and Monitoring Website, you must also specify each security group when you are configuring the Administration and Monitoring Website.</span></span>

### <span data-ttu-id="83668-228">Windows PowerShell-Cmdlets zum Konfigurieren von MBAM-Server Features</span><span class="sxs-lookup"><span data-stu-id="83668-228">Windows PowerShell cmdlets for configuring MBAM Server features</span></span>

<span data-ttu-id="83668-229">Mit Windows PowerShell-Cmdlets für MBAM 2.5 können Sie die MBAM-Server Features konfigurieren und verwalten.</span><span class="sxs-lookup"><span data-stu-id="83668-229">Windows PowerShell cmdlets for MBAM2.5 enable you to configure and manage the MBAM Server features.</span></span> <span data-ttu-id="83668-230">Jedes Feature verfügt über ein entsprechendes Windows PowerShell-Cmdlet, das Sie zum Aktivieren oder Deaktivieren von Features oder zum Abrufen von Informationen über das Feature verwenden können.</span><span class="sxs-lookup"><span data-stu-id="83668-230">Each feature has a corresponding Windows PowerShell cmdlet that you can use to enable or disable features, or to get information about the feature.</span></span>

<span data-ttu-id="83668-231">Voraussetzungen und Voraussetzungen für die Verwendung von Windows PowerShell finden Sie unter [Konfigurieren von MBAM 2,5-Server Features mithilfe von Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="83668-231">For prerequisites and prerequisites for using Windows PowerShell, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span></span>

**<span data-ttu-id="83668-232">So laden Sie die MBAM 2,5-Hilfe für Windows PowerShell-Cmdlets nach der Installation der MBAM-Server Software</span><span class="sxs-lookup"><span data-stu-id="83668-232">To load the MBAM 2.5 Help for Windows PowerShell cmdlets after installing the MBAM Server software</span></span>**

1.  <span data-ttu-id="83668-233">Öffnen Sie Windows PowerShell oder Windows PowerShell Integrated Scripting Environment (ISE).</span><span class="sxs-lookup"><span data-stu-id="83668-233">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="83668-234">Geben Sie **Update-Help-Module Microsoft. MBAM**.</span><span class="sxs-lookup"><span data-stu-id="83668-234">Type **Update-Help –Module Microsoft.MBAM**.</span></span>

<span data-ttu-id="83668-235">Die Windows PowerShell-Hilfe für MBAM ist in den folgenden Formaten verfügbar:</span><span class="sxs-lookup"><span data-stu-id="83668-235">Windows PowerShell Help for MBAM is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="83668-236">Windows PowerShell-Hilfeformat</span><span class="sxs-lookup"><span data-stu-id="83668-236">Windows PowerShell Help format</span></span></th>
<th align="left"><span data-ttu-id="83668-237">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="83668-237">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83668-238">Geben Sie an einer Windows PowerShell-Eingabeaufforderung <strong> Get-Help- </strong> &lt; <em> Cmdlet ein.</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="83668-238">At a Windows PowerShell command prompt, type <strong>Get-Help</strong> &lt;<em>cmdlet</em>&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="83668-239">Wenn Sie die neuesten Windows PowerShell-Cmdlets hochladen möchten, befolgen Sie die Anweisungen im vorherigen Abschnitt zum Laden der Windows PowerShell-Hilfe für MBAM.</span><span class="sxs-lookup"><span data-stu-id="83668-239">To upload the latest Windows PowerShell cmdlets, follow the instructions in the previous section on how to load Windows PowerShell Help for MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83668-240">Auf TechNet als Webseiten</span><span class="sxs-lookup"><span data-stu-id="83668-240">On TechNet as webpages</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83668-241">Im Download Center als Word. docx-Datei</span><span class="sxs-lookup"><span data-stu-id="83668-241">On the Download Center as a Word .docx file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83668-242">Im Download Center als PDF-Datei</span><span class="sxs-lookup"><span data-stu-id="83668-242">On the Download Center as a .pdf file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="83668-243">Unterstützung für reine ASCII-und erweiterte Pins sowie die Möglichkeit, sequenzielle und wiederholte Zeichen zu verhindern</span><span class="sxs-lookup"><span data-stu-id="83668-243">Support for ASCII-only and enhanced PINs and ability to prevent sequential and repeating characters</span></span>

**<span data-ttu-id="83668-244">Erweiterte Pins für Startgruppen Richtlinieneinstellung zulassen</span><span class="sxs-lookup"><span data-stu-id="83668-244">Allow enhanced PINs for startup Group Policy setting</span></span>**

<span data-ttu-id="83668-245">Die Gruppenrichtlinieneinstellung " **Erweiterte Pins für den Start zulassen**" ermöglicht es Ihnen, zu konfigurieren, ob erweiterte Start Pins für BitLocker verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83668-245">The Group Policy setting, **Allow enhanced PINs for startup**, enables you to configure whether enhanced startup PINs are used with BitLocker.</span></span> <span data-ttu-id="83668-246">Erweiterte Start Pins ermöglichen Benutzern die Eingabe von Schlüsseln auf einer vollständigen Tastatur, einschließlich Groß-und Kleinbuchstaben, Symbolen, Zahlen und Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="83668-246">Enhanced startup PINs permit users to enter any keys on a full keyboard, including uppercase and lowercase letters, symbols, numbers, and spaces.</span></span> <span data-ttu-id="83668-247">Wenn Sie diese Richtlinieneinstellung aktivieren, werden alle neuen BitLocker-startpins, die festgelegt sind, mit erweiterten Pins ergänzt.</span><span class="sxs-lookup"><span data-stu-id="83668-247">If you enable this policy setting, all new BitLocker startup PINs that are set will be enhanced PINs.</span></span> <span data-ttu-id="83668-248">Wenn Sie diese Richtlinieneinstellung deaktivieren oder nicht konfigurieren, können erweiterte Pins nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83668-248">If you disable or do not configure this policy setting, enhanced PINs cannot be used.</span></span>

<span data-ttu-id="83668-249">Nicht alle Computer unterstützen den Eintrag verbesserter Pins in der Pre-Boot Execution Environment (PXE).</span><span class="sxs-lookup"><span data-stu-id="83668-249">Not all computers support the entry of enhanced PINs in the Pre-Boot Execution Environment (PXE).</span></span> <span data-ttu-id="83668-250">Bevor Sie diese Gruppenrichtlinieneinstellung für Ihre Organisation aktivieren, führen Sie während des BitLocker-Setupvorgangs eine Systemüberprüfung durch, um sicherzustellen, dass das BIOS des Computers die Verwendung der vollständigen Tastatur in PXE unterstützt.</span><span class="sxs-lookup"><span data-stu-id="83668-250">Before you enable this Group Policy setting for your organization, run a system check during the BitLocker setup process to ensure that the computer’s BIOS supports the use of the full keyboard in PXE.</span></span> <span data-ttu-id="83668-251">Weitere Informationen finden Sie unter [Planen von MBAM 2,5-Gruppenrichtlinienanforderungen](planning-for-mbam-25-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="83668-251">For more information, see [Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md).</span></span>

**<span data-ttu-id="83668-252">Kontrollkästchen nur ASCII-Pins erforderlich</span><span class="sxs-lookup"><span data-stu-id="83668-252">Require ASCII-only PINs check box</span></span>**

<span data-ttu-id="83668-253">Die Gruppenrichtlinieneinstellung **Erweiterte Pins für Start zulassen** enthält auch das Kontrollkästchen **nur ASCII-Pins erforderlich** .</span><span class="sxs-lookup"><span data-stu-id="83668-253">The **Allow enhanced PINs for startup** Group Policy setting also contains a **Require ASCII-only PINs** check box.</span></span> <span data-ttu-id="83668-254">Wenn die Computer in Ihrer Organisation die Verwendung der Volltastatur in PXE nicht unterstützen, können Sie die Gruppenrichtlinieneinstellung **Erweiterte Pins für Start zulassen** aktivieren, und aktivieren Sie dann das Kontrollkästchen **nur-ASCII-Pins anfordern** , um zu erzwingen, dass für erweiterte Pins nur druckbare ASCII-Zeichen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83668-254">If the computers in your organization do not support the use of the full keyboard in PXE, you can enable the **Allow enhanced PINs for startup** Group Policy setting, and then select the **Require ASCII-only PINs** check box to require that enhanced PINs use only printable ASCII characters.</span></span>

**<span data-ttu-id="83668-255">Erzwungene Verwendung von nicht sequenziellen und nicht wiederholenden Zeichen</span><span class="sxs-lookup"><span data-stu-id="83668-255">Enforced use of nonsequential and nonrepeating characters</span></span>**

<span data-ttu-id="83668-256">Mbam 2.5 verhindert, dass Endbenutzer Pins erstellen, die aus wiederholenden Zahlen (wie 1111) oder sequenziellen Zahlen (wie 1234) bestehen.</span><span class="sxs-lookup"><span data-stu-id="83668-256">MBAM2.5 prevents end users from creating PINs that consist of repeating numbers (such as 1111) or sequential numbers (such as 1234).</span></span> <span data-ttu-id="83668-257">Wenn Endbenutzer versuchen, ein Kennwort einzugeben, das drei oder mehr Wiederholungs-oder fortlaufende Nummern enthält, zeigt der BitLocker-Laufwerk Verschlüsselungs-Assistent eine Fehlermeldung an und verhindert, dass Benutzer eine PIN mit den verbotenen Zeichen eingeben.</span><span class="sxs-lookup"><span data-stu-id="83668-257">If end users try to enter a password that contains three or more repeating or sequential numbers, the Bitlocker Drive Encryption wizard displays an error message and prevents users from entering a PIN with the prohibited characters.</span></span>

### <span data-ttu-id="83668-258">Hinzufügen des DRA-Zertifikats zum BitLocker-Computer Kompatibilitätsbericht</span><span class="sxs-lookup"><span data-stu-id="83668-258">Addition of DRA Certificate to BitLocker Computer Compliance report</span></span>

<span data-ttu-id="83668-259">Ein neuer Protector-Typ, das DRA-Zertifikat (Data Recovery Agent), wurde dem BitLocker-Computer Kompatibilitätsbericht in Configuration Manager hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="83668-259">A new protector type, the Data Recovery Agent (DRA) Certificate, has been added to the BitLocker Computer Compliance Report in Configuration Manager.</span></span> <span data-ttu-id="83668-260">Dieser Protector-Typ gilt für Betriebssystemlaufwerke und wird in der Spalte " **Protector-Typen** " im Abschnitt " **Computer Lautstärke (n)** " angezeigt.</span><span class="sxs-lookup"><span data-stu-id="83668-260">This protector type applies to operating system drives, and it appears in the **Computer Volume(s)** section in the **Protector Types** column.</span></span>

### <span data-ttu-id="83668-261">Unterstützung für Multi-Forest-Support Bereitstellungen</span><span class="sxs-lookup"><span data-stu-id="83668-261">Support for multi-forest support deployments</span></span>

<span data-ttu-id="83668-262">MBAM 2,5 unterstützt die folgenden Typen von Bereitstellungen mit mehreren Gesamtstrukturen:</span><span class="sxs-lookup"><span data-stu-id="83668-262">MBAM 2.5 supports the following types of multi-forest deployments:</span></span>

-   <span data-ttu-id="83668-263">Einzelne Gesamtstruktur mit einer einzelnen Domäne</span><span class="sxs-lookup"><span data-stu-id="83668-263">Single forest with single domain</span></span>

-   <span data-ttu-id="83668-264">Einzelne Gesamtstruktur mit einer einzelnen Struktur und mehreren Domänen</span><span class="sxs-lookup"><span data-stu-id="83668-264">Single forest with a single tree and multiple domains</span></span>

-   <span data-ttu-id="83668-265">Einzelne Gesamtstruktur mit mehreren Strukturen und nicht zusammengefügten Namespaces</span><span class="sxs-lookup"><span data-stu-id="83668-265">Single forest with multiple trees and disjoint namespaces</span></span>

-   <span data-ttu-id="83668-266">Mehrere Gesamtstrukturen in einer zentralen Gesamtstrukturtopologie</span><span class="sxs-lookup"><span data-stu-id="83668-266">Multiple forests in a central forest topology</span></span>

-   <span data-ttu-id="83668-267">Mehrere Gesamtstrukturen in einer Ressourcengesamtstruktur-Topologie</span><span class="sxs-lookup"><span data-stu-id="83668-267">Multiple forests in a resource forest topology</span></span>

<span data-ttu-id="83668-268">Es gibt keine Unterstützung für die Gesamtstruktur Migration (von einer einzelnen zu mehreren, von mehreren zu einer, zu einer Ressource in der gesamten Gesamtstruktur usw.) oder zum Upgrade oder Downgrade.</span><span class="sxs-lookup"><span data-stu-id="83668-268">There is no support for forest migration (going from single to multiple, multiple to single, resource to across the forest, etc.), or upgrade or downgrade.</span></span>

<span data-ttu-id="83668-269">Die Voraussetzungen für die Bereitstellung von MBAM in Multi-Forest-Bereitstellungen sind:</span><span class="sxs-lookup"><span data-stu-id="83668-269">The prerequisites for deploying MBAM in multi-forest deployments are:</span></span>

-   <span data-ttu-id="83668-270">Die Gesamtstruktur muss unter unterstützten Versionen von Windows Server ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="83668-270">Forest must be running on supported versions of Windows Server.</span></span>

-   <span data-ttu-id="83668-271">Eine bidirektionale oder unidirektionale Vertrauensstellung ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="83668-271">A two-way or one-way trust is required.</span></span> <span data-ttu-id="83668-272">Unidirektionale Vertrauensstellungen setzen voraus, dass die Domäne des Servers der Domäne des Clients vertraut.</span><span class="sxs-lookup"><span data-stu-id="83668-272">One-way trusts require that the server’s domain trusts the client’s domain.</span></span> <span data-ttu-id="83668-273">Anders ausgedrückt: die Domäne des Servers verweist auf die Domäne des Clients.</span><span class="sxs-lookup"><span data-stu-id="83668-273">In other words, the server’s domain is pointed at the client’s domain.</span></span>

### <span data-ttu-id="83668-274">MBAM-Client Unterstützung für verschlüsselte Festplatten</span><span class="sxs-lookup"><span data-stu-id="83668-274">MBAM Client support for Encrypted Hard Drives</span></span>

<span data-ttu-id="83668-275">MBAM unterstützt BitLocker auf verschlüsselten Festplatten, die die TCG-Spezifikationsanforderungen für Opal-und IEEE-1667-Standards erfüllen.</span><span class="sxs-lookup"><span data-stu-id="83668-275">MBAM supports BitLocker on Encrypted Hard Drives that meet TCG specification requirements for Opal as well as IEEE 1667 standards.</span></span> <span data-ttu-id="83668-276">Wenn BitLocker auf diesen Geräten aktiviert ist, generiert es Schlüssel und führt Verwaltungsfunktionen auf dem verschlüsselten Laufwerk aus.</span><span class="sxs-lookup"><span data-stu-id="83668-276">When BitLocker is enabled on these devices, it will generate keys and perform management functions on the encrypted drive.</span></span> <span data-ttu-id="83668-277">Weitere Informationen finden Sie unter [verschlüsselte Festplatte](https://technet.microsoft.com/library/hh831627.aspx) .</span><span class="sxs-lookup"><span data-stu-id="83668-277">See [Encrypted Hard Drive](https://technet.microsoft.com/library/hh831627.aspx) for more information.</span></span>

## <span data-ttu-id="83668-278">So erhalten Sie MDOP-Technologien</span><span class="sxs-lookup"><span data-stu-id="83668-278">How to Get MDOP Technologies</span></span>


<span data-ttu-id="83668-279">MBAM ist ein Bestandteil des Microsoft-Desktop Optimierungs Pakets (MDOP).</span><span class="sxs-lookup"><span data-stu-id="83668-279">MBAM is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="83668-280">MDOP ist Teil des Microsoft Software Assurance-Programms.</span><span class="sxs-lookup"><span data-stu-id="83668-280">MDOP is part of the Microsoft Software Assurance program.</span></span> <span data-ttu-id="83668-281">Weitere Informationen zum Microsoft Software Assurance-Programm und zum Erwerb der MDOP finden Sie unter [wie erhalte ich MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="83668-281">For more information about the Microsoft Software Assurance program and how to acquire the MDOP, see [How Do I Get MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <a href="" id="---------mbam-2-5-release-notes"></a> <span data-ttu-id="83668-282">MBAM 2,5-Versionshinweise</span><span class="sxs-lookup"><span data-stu-id="83668-282">MBAM 2.5 Release Notes</span></span>


<span data-ttu-id="83668-283">Weitere Informationen und aktuelle Neuigkeiten, die nicht in dieser Dokumentation enthalten sind, finden Sie unter [Versionshinweise zu MBAM 2,5](release-notes-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="83668-283">For more information and late-breaking news that is not included in this documentation, see [Release Notes for MBAM 2.5](release-notes-for-mbam-25.md).</span></span>

## <span data-ttu-id="83668-284">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="83668-284">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="83668-285">Senden Sie [uns](https://support.microsoft.com/help/4021566/windows-10-send-feedback-to-microsoft-with-feedback-hub)Ihr Feedback.</span><span class="sxs-lookup"><span data-stu-id="83668-285">Send your feedback [here](https://support.microsoft.com/help/4021566/windows-10-send-feedback-to-microsoft-with-feedback-hub).</span></span> 
- <span data-ttu-id="83668-286">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="83668-286">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

## <span data-ttu-id="83668-287">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="83668-287">Related topics</span></span>


[<span data-ttu-id="83668-288">Microsoft BitLocker Administration and Monitoring 2.5</span><span class="sxs-lookup"><span data-stu-id="83668-288">Microsoft BitLocker Administration and Monitoring 2.5</span></span>](index.md)

[<span data-ttu-id="83668-289">Erste Schritte mit MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="83668-289">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

 

 





