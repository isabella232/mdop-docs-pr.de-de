---
title: Planen der Gruppenrichtlinienanforderungen für MBAM 1.0
description: Planen der Gruppenrichtlinienanforderungen für MBAM 1.0
author: dansimp
ms.assetid: 0fc9c509-7850-4a8e-bb82-b949025bcb02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5061748107dc1d00baa41188b8cf240ec187317
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804226"
---
# <span data-ttu-id="7c070-103">Planen der Gruppenrichtlinienanforderungen für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="7c070-103">Planning for MBAM 1.0 Group Policy Requirements</span></span>


<span data-ttu-id="7c070-104">Die Microsoft BitLocker-MBAM-Client Verwaltung erfordert die Anwendung benutzerdefinierter Gruppenrichtlinieneinstellungen.</span><span class="sxs-lookup"><span data-stu-id="7c070-104">Microsoft BitLocker Administration and Monitoring (MBAM) Client management requires custom Group Policy settings to be applied.</span></span> <span data-ttu-id="7c070-105">In diesem Thema werden die verfügbaren Richtlinienoptionen für Gruppenrichtlinienobjekte beschrieben, wenn Sie MBAM verwenden, um die BitLocker-Laufwerkverschlüsselung im Unternehmen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="7c070-105">This topic describes the available policy options for Group Policy Object (GPO) when you use MBAM to manage BitLocker Drive Encryption in the enterprise.</span></span>

**<span data-ttu-id="7c070-106">Wichtig</span><span class="sxs-lookup"><span data-stu-id="7c070-106">Important</span></span>**  
<span data-ttu-id="7c070-107">MBAM verwendet nicht die standardmäßigen GPO-Einstellungen für die Windows BitLocker Drive-Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="7c070-107">MBAM does not use the default GPO settings for Windows BitLocker drive encryption.</span></span> <span data-ttu-id="7c070-108">Wenn die Standardeinstellungen aktiviert sind, kann dies zu einem in Konflikt stehenden Verhalten führen.</span><span class="sxs-lookup"><span data-stu-id="7c070-108">If the default settings are enabled, they can cause conflicting behavior.</span></span> <span data-ttu-id="7c070-109">Wenn Sie MBAM zum Verwalten von BitLocker aktivieren möchten, müssen Sie nach der Installation der MBAM-Gruppenrichtlinienvorlage die Richtlinieneinstellungen für Gruppenrichtlinienobjekte definieren.</span><span class="sxs-lookup"><span data-stu-id="7c070-109">To enable MBAM to manage BitLocker, you must define the GPO policy settings after you install the MBAM Group Policy Template.</span></span>



<span data-ttu-id="7c070-110">Nachdem Sie die MBAM-Gruppenrichtlinienvorlage installiert haben, können Sie die verfügbaren benutzerdefinierten MBAM-GPO-Richtlinieneinstellungen anzeigen und ändern, mit denen MBAM die BitLocker-Unternehmens-Verschlüsselung verwalten kann.</span><span class="sxs-lookup"><span data-stu-id="7c070-110">After you install the MBAM Group Policy template, you can view and modify the available custom MBAM GPO policy settings that enable MBAM to manage the enterprise BitLocker encryption.</span></span> <span data-ttu-id="7c070-111">Die MBAM-Gruppenrichtlinienvorlage muss auf einem Computer installiert sein, auf dem die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (AGPM)-MDOP-Technologie ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7c070-111">The MBAM Group Policy template must be installed on a computer that is capable of running the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) MDOP technology.</span></span> <span data-ttu-id="7c070-112">Zum Bearbeiten des anwendbaren Gruppenrichtlinienobjekts öffnen Sie dann die GPMC oder AGPM, und navigieren Sie dann zum folgenden GPO-Knoten: **Computerkonfigurations**- \\ **Administrative Vorlagen** \\ **Windows Components** \\ **MDOP MBAM (BitLocker-Verwaltung)**.</span><span class="sxs-lookup"><span data-stu-id="7c070-112">Next, to edit the applicable GPO, open the GPMC or AGPM, and then navigate to the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)**.</span></span>

<span data-ttu-id="7c070-113">Der MDOP MBAM (BitLocker Management)-GPO-Knoten enthält vier globale Richtlinieneinstellungen und vier untergeordnete GPO-Einstellungs Knoten.</span><span class="sxs-lookup"><span data-stu-id="7c070-113">The MDOP MBAM (BitLocker Management) GPO node contains four global policy settings and four child GPO setting nodes, respectively.</span></span> <span data-ttu-id="7c070-114">Die vier globalen Richtlinieneinstellungen für GPO sind: Client Verwaltung, festes Laufwerk, Betriebs System Laufwerk und Wechsellaufwerk.</span><span class="sxs-lookup"><span data-stu-id="7c070-114">The four GPO global policy settings are: Client Management, Fixed Drive, Operating System Drive, and Removable Drive.</span></span> <span data-ttu-id="7c070-115">Die folgenden Abschnitte enthalten Richtlinien Definitionen und vorgeschlagene Richtlinieneinstellungen, die Ihnen bei der Planung der MBAM-Richtlinien Einstellungsanforderungen helfen.</span><span class="sxs-lookup"><span data-stu-id="7c070-115">The following sections provide policy definitions and suggested policy settings to help you plan for the MBAM GPO policy setting requirements.</span></span>

**<span data-ttu-id="7c070-116">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="7c070-116">Note</span></span>**  
<span data-ttu-id="7c070-117">Weitere Informationen zum Konfigurieren der Mindesteinstellungen für vorgeschlagene Gruppenrichtlinienobjekte, damit MBAM die BitLocker-Verschlüsselung verwalten kann, finden Sie unter [Bearbeiten von MBAM 1,0-GPO-Einstellungen](how-to-edit-mbam-10-gpo-settings.md).</span><span class="sxs-lookup"><span data-stu-id="7c070-117">For more information about configuring the minimum suggested GPO settings to enable MBAM to manage BitLocker encryption, see [How to Edit MBAM 1.0 GPO Settings](how-to-edit-mbam-10-gpo-settings.md).</span></span>



## <span data-ttu-id="7c070-118">Definitionen globaler Richtlinien</span><span class="sxs-lookup"><span data-stu-id="7c070-118">Global policy definitions</span></span>


<span data-ttu-id="7c070-119">In diesem Abschnitt werden die globalen MBAM-Definitionen beschrieben, die unter dem folgenden GPO-Knoten zu finden sind: **Computerkonfigurations**- \\ **Administrative Vorlagen** \\ **Windows Components** \\ **MDOP MBAM (BitLocker-Verwaltung)**.</span><span class="sxs-lookup"><span data-stu-id="7c070-119">This section describes the MBAM Global policy definitions, which can be found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7c070-120">Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="7c070-120">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="7c070-121">Übersicht und vorgeschlagene Richtlinieneinstellung</span><span class="sxs-lookup"><span data-stu-id="7c070-121">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7c070-122">Wählen Sie Laufwerk Verschlüsselungsmethode und Verschlüsselungsstärke aus.</span><span class="sxs-lookup"><span data-stu-id="7c070-122">Choose drive encryption method and cipher strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c070-123">Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</span><span class="sxs-lookup"><span data-stu-id="7c070-123">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="7c070-124">Konfigurieren Sie diese Richtlinie für die Verwendung einer bestimmten Verschlüsselungsmethode und Verschlüsselungsstärke.</span><span class="sxs-lookup"><span data-stu-id="7c070-124">Configure this policy to use a specific encryption method and cipher strength.</span></span></p>
<p><span data-ttu-id="7c070-125">Wenn diese Richtlinie nicht konfiguriert ist, verwendet BitLocker die Standardverschlüsselungsmethode von AES 128-Bit mit Diffusor oder die vom Setupskript angegebene Verschlüsselungsmethode.</span><span class="sxs-lookup"><span data-stu-id="7c070-125">When this policy is not configured, BitLocker uses the default encryption method of AES 128-bit with Diffuser or the encryption method specified by the setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7c070-126">Verhindern, dass beim Neustart Speicher überschrieben wird</span><span class="sxs-lookup"><span data-stu-id="7c070-126">Prevent memory overwrite on restart</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c070-127">Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</span><span class="sxs-lookup"><span data-stu-id="7c070-127">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="7c070-128">Konfigurieren Sie diese Richtlinie, um die Neustart Leistung zu verbessern, ohne BitLocker-Geheimnisse beim Neustart überschreiben zu müssen.</span><span class="sxs-lookup"><span data-stu-id="7c070-128">Configure this policy to improve restart performance without overwriting BitLocker secrets in memory on restart.</span></span></p>
<p><span data-ttu-id="7c070-129">Wenn diese Richtlinie nicht konfiguriert ist, werden BitLocker-Geheimnisse aus dem Arbeitsspeicher entfernt, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="7c070-129">When this policy is not configured, BitLocker secrets are removed from memory when the computer restarts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7c070-130">Überprüfen der Verwendungs Regel für Smartcard-Zertifikate</span><span class="sxs-lookup"><span data-stu-id="7c070-130">Validate smart card certificate usage rule</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c070-131">Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</span><span class="sxs-lookup"><span data-stu-id="7c070-131">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="7c070-132">Konfigurieren Sie diese Richtlinie für die Verwendung von Smartcard-Zertifikat basiertem BitLocker-Schutz.</span><span class="sxs-lookup"><span data-stu-id="7c070-132">Configure this policy to use smartcard certificate-based BitLocker protection.</span></span></p>
<p><span data-ttu-id="7c070-133">Wenn diese Richtlinie nicht konfiguriert ist, wird ein Standardobjekt-ID-1.3.6.1.4.1.311.67.1.1 verwendet, um ein Zertifikat anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7c070-133">When this policy is not configured, a default object identifier 1.3.6.1.4.1.311.67.1.1 is used to specify a certificate.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7c070-134">Bereitstellen der eindeutigen Bezeichner für Ihre Organisation</span><span class="sxs-lookup"><span data-stu-id="7c070-134">Provide the unique identifiers for your organization</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c070-135">Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</span><span class="sxs-lookup"><span data-stu-id="7c070-135">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="7c070-136">Konfigurieren Sie diese Richtlinie für die Verwendung eines zertifikatbasierten Daten Wiederherstellungs-Agents oder des BitLocker To Go-Readers.</span><span class="sxs-lookup"><span data-stu-id="7c070-136">Configure this policy to use a certificate-based data recovery agent or the BitLocker To Go reader.</span></span></p>
<p><span data-ttu-id="7c070-137">Wenn diese Richtlinie nicht konfiguriert ist, <strong> </strong> wird das Feld ID nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7c070-137">When this policy is not configured, the <strong>Identification</strong> field is not used.</span></span></p>
<p><span data-ttu-id="7c070-138">Wenn in Ihrem Unternehmen höhere Sicherheitsmaße erforderlich sind, können Sie das Feld "Identifikation" so konfigurieren, <strong> </strong> dass alle USB-Geräte dieses Feld festgelegt haben, und dass Sie mit dieser Gruppenrichtlinieneinstellung ausgerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="7c070-138">If your company requires higher security measurements, you may want to configure the <strong>Identification</strong> field to make sure that all USB devices have this field set and that they are aligned with this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="7c070-139">Definitionen für Client Verwaltungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="7c070-139">Client Management policy definitions</span></span>


<span data-ttu-id="7c070-140">In diesem Abschnitt werden die Definitionen der clientverwaltungsrichtlinien für MBAM beschrieben, die unter dem folgenden GPO-Knoten gefunden werden: **Computerkonfigurations**- \\ **Administrative Vorlagen** \\ **Windows Components** \\ **MDOP MBAM (BitLocker-Verwaltungs**  \\  **Clientverwaltung**).</span><span class="sxs-lookup"><span data-stu-id="7c070-140">This section describes the Client Management policy definitions for MBAM, found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Client Management**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7c070-141">Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="7c070-141">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="7c070-142">Übersicht und vorgeschlagene Richtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="7c070-142">Overview and Suggested Policy Settings</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7c070-143">Konfigurieren von MBAM-Diensten</span><span class="sxs-lookup"><span data-stu-id="7c070-143">Configure MBAM Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c070-144">Empfohlene Konfiguration: <strong> aktiviert</span><span class="sxs-lookup"><span data-stu-id="7c070-144">Suggested Configuration: <strong>Enabled</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="7c070-145">MBAM-Wiederherstellungs-und Hardware </strong> Dienstendpunkt</span><span class="sxs-lookup"><span data-stu-id="7c070-145">MBAM Recovery and Hardware service endpoint</strong>.</span></span> <span data-ttu-id="7c070-146">Dies ist die erste Richtlinieneinstellung, die Sie konfigurieren müssen, um die MBAM-Client-BitLocker-Verschlüsselungs Verwaltung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7c070-146">This is the first policy setting that you must configure to enable the MBAM Client BitLocker encryption management.</span></span> <span data-ttu-id="7c070-147">Geben Sie für diese Einstellung den Endpunkt Speicherort ein, der dem folgenden Beispiel ähnelt: <strong> http:// </strong><em> &lt; MBAM Administration and Monitoring Server Name &gt; </em><strong> : </strong><em> &lt; Port der Webdienst ist an &gt; </em><strong> /MBAMRecoveryAndHardwareService/CoreService.svc gebunden </strong> .</span><span class="sxs-lookup"><span data-stu-id="7c070-147">For this setting, enter the endpoint location similar to the following example: <strong>http://</strong><em>&lt;MBAM Administration and Monitoring Server Name&gt;</em><strong>:</strong><em>&lt;port the web service is bound to&gt;</em><strong>/MBAMRecoveryAndHardwareService/CoreService.svc</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="7c070-148">Wählen Sie die zu speichernden BitLocker-Wiederherstellungsinformationen aus </strong> .</span><span class="sxs-lookup"><span data-stu-id="7c070-148">Select BitLocker recovery information to store</strong>.</span></span> <span data-ttu-id="7c070-149">Mit dieser Richtlinieneinstellung können Sie den Schlüssel Wiederherstellungs Dienst so konfigurieren, dass die BitLocker-Wiederherstellungsinformationen gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="7c070-149">This policy setting lets you configure the key recovery service to back up the BitLocker recovery information.</span></span> <span data-ttu-id="7c070-150">Außerdem können Sie den Statusberichts Dienst für das Sammeln von Konformitäts-und Überwachungsberichten konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7c070-150">It also lets you configure the status reporting service for collecting compliance and audit reports.</span></span> <span data-ttu-id="7c070-151">Die Richtlinie stellt eine administrative Methode zur Verfügung, die von BitLocker verschlüsselte Daten zurückgibt, um Datenverluste aufgrund fehlender Schlüsselinformationen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="7c070-151">The policy provides an administrative method of recovering data encrypted by BitLocker to help prevent data loss due to the lack of key information.</span></span> <span data-ttu-id="7c070-152">Status Bericht und wichtige Wiederherstellungsaktivitäten werden automatisch an den konfigurierten Berichtsserver Speicherort gesendet.</span><span class="sxs-lookup"><span data-stu-id="7c070-152">Status report and key recovery activity will automatically and silently be sent to the configured report server location.</span></span></p>
<p><span data-ttu-id="7c070-153">Wenn Sie diese Richtlinieneinstellung nicht konfigurieren oder deaktivieren, werden die Schlüssel Wiederherstellungsinformationen nicht gespeichert, und der Statusbericht und die Schlüssel Wiederherstellungs Aktivität werden nicht an den Server gemeldet.</span><span class="sxs-lookup"><span data-stu-id="7c070-153">If you do not configure or if you disable this policy setting, the key recovery information will not be saved, and status report and key recovery activity will not be reported to server.</span></span> <span data-ttu-id="7c070-154">Wenn diese Einstellung auf <strong> Wiederherstellungskennwort und Schlüsselpaket festgelegt ist </strong> , werden das Wiederherstellungskennwort und das Schlüsselpaket automatisch und lautlos auf dem konfigurierten Speicherort des Schlüssel Wiederherstellungs Servers gesichert.</span><span class="sxs-lookup"><span data-stu-id="7c070-154">When this setting is set to <strong>Recovery Password and key package</strong>, the recovery password and key package will be automatically and silently backed up to the configured key recovery server location.</span></span></p></li>
<li><p><strong><span data-ttu-id="7c070-155">Geben Sie die Status Häufigkeit der Clientüberprüfung in Minuten ein </strong> .</span><span class="sxs-lookup"><span data-stu-id="7c070-155">Enter the client checking status frequency in minutes</strong>.</span></span> <span data-ttu-id="7c070-156">Diese Richtlinieneinstellung verwaltet, wie häufig der Client die BitLocker-Schutzrichtlinien und den Status auf dem Clientcomputer überprüft.</span><span class="sxs-lookup"><span data-stu-id="7c070-156">This policy setting manages how frequently the client checks the BitLocker protection policies and the status on the client computer.</span></span> <span data-ttu-id="7c070-157">Diese Richtlinie verwaltet auch die Häufigkeit, mit der der Client Kompatibilitätsstatus auf dem Server gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="7c070-157">This policy also manages how frequently the client compliance status is saved to the server.</span></span> <span data-ttu-id="7c070-158">Der Client überprüft die BitLocker-Schutzrichtlinien und den Status auf dem Clientcomputer, und es wird auch der Client Wiederherstellungsschlüssel unter der konfigurierten Häufigkeit gesichert.</span><span class="sxs-lookup"><span data-stu-id="7c070-158">The client checks the BitLocker protection policies and status on the client computer, and it also backs up the client recovery key at the configured frequency.</span></span></p>
<p><span data-ttu-id="7c070-159">Legen Sie diese Häufigkeit basierend auf der von Ihrem Unternehmen festgelegten Anforderung fest, wie häufig der Kompatibilitätsstatus des Computers überprüft werden soll und wie häufig der Client Wiederherstellungsschlüssel gesichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c070-159">Set this frequency based on the requirement established by your company on how frequently to check the compliance status of the computer, and how frequently to back up the client recovery key.</span></span></p></li>
<li><p><strong><span data-ttu-id="7c070-160">MBAM-Status Berichterstattungsdienst Endpunkt </strong> .</span><span class="sxs-lookup"><span data-stu-id="7c070-160">MBAM Status reporting service endpoint</strong>.</span></span> <span data-ttu-id="7c070-161">Dies ist die zweite Richtlinieneinstellung, die Sie konfigurieren müssen, um die MBAM-Client-BitLocker-Verschlüsselungs Verwaltung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7c070-161">This is the second policy setting that you must configure to enable MBAM Client BitLocker encryption management.</span></span> <span data-ttu-id="7c070-162">Geben Sie für diese Einstellung den Endpunkt Speicherort ein, indem Sie das folgende Beispiel verwenden: <strong> http:// </strong><em> &lt; MBAM Administration and Monitoring Server Name &gt; </em><strong> : </strong><em> &lt; Port der Webdienst ist an &gt; </em><strong> /MBAMComplianceStatusService/StatusReportingService. gebunden.</span><span class="sxs-lookup"><span data-stu-id="7c070-162">For this setting, enter the endpoint location by using the following example: <strong>http://</strong><em>&lt;MBAM Administration and Monitoring Server Name&gt;</em><strong>:</strong><em>&lt;port the web service is bound to&gt;</em><strong>/MBAMComplianceStatusService/StatusReportingService.</span></span> <span data-ttu-id="7c070-163">SVC </strong> .</span><span class="sxs-lookup"><span data-stu-id="7c070-163">svc</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7c070-164">Hardware Kompatibilitätsüberprüfung zulassen</span><span class="sxs-lookup"><span data-stu-id="7c070-164">Allow hardware compatibility checking</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c070-165">Empfohlene Konfiguration: <strong> aktiviert</span><span class="sxs-lookup"><span data-stu-id="7c070-165">Suggested Configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="7c070-166">Mit dieser Richtlinieneinstellung können Sie die Überprüfung der Hardwarekompatibilität verwalten, bevor Sie den BitLocker-Schutz auf Laufwerken von MBAM-Clientcomputern aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7c070-166">This policy setting lets you manage the verification of hardware compatibility before you enable BitLocker protection on drives of MBAM client computers.</span></span></p>
<p><span data-ttu-id="7c070-167">Sie sollten diese Richtlinienoption aktivieren, wenn Ihr Unternehmen über ältere Computer Hardware oder Computer verfügt, die kein Trusted Platform Module (TPM) unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7c070-167">You should enable this policy option if your enterprise has older computer hardware or computers that do not support Trusted Platform Module (TPM).</span></span> <span data-ttu-id="7c070-168">Wenn eines der beiden Kriterien wahr ist, aktivieren Sie die Hardware Kompatibilitätsüberprüfung, um sicherzustellen, dass MBAM nur auf Computermodelle angewendet wird, die BitLocker unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7c070-168">If either of these criteria is true, enable the hardware compatibility verification to make sure that MBAM is applied only to computer models that support BitLocker.</span></span> <span data-ttu-id="7c070-169">Wenn alle Computer in Ihrer Organisation BitLocker unterstützen, müssen Sie die Hardware Kompatibilität nicht bereitstellen, und Sie können diese Richtlinie auf <strong> nicht konfiguriert festlegen </strong> .</span><span class="sxs-lookup"><span data-stu-id="7c070-169">If all computers in your organization support BitLocker, you do not have to deploy the Hardware Compatibility, and you can set this policy to <strong>Not Configured</strong>.</span></span></p>
<p><span data-ttu-id="7c070-170">Wenn Sie diese Richtlinieneinstellung aktivieren, wird das Modell des Computers alle 24 Stunden anhand der Hardwarekompatibilitätsliste überprüft, bevor die Richtlinie den BitLocker-Schutz auf einem Computerlaufwerk aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7c070-170">If you enable this policy setting, the model of the computer is validated against the hardware compatibility list once every 24 hours, before the policy enables BitLocker protection on a computer drive.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="7c070-171">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="7c070-171">Note</span></span></strong><br/><p><span data-ttu-id="7c070-172">Bevor Sie diese Richtlinieneinstellung aktivieren, stellen Sie sicher, dass Sie die <strong> Einstellung MBAM-Wiederherstellungs-und Hardware Dienstendpunkt </strong> in den <strong> Optionen für MBAM-Dienst Richtlinien konfigurieren </strong> konfiguriert haben.</span><span class="sxs-lookup"><span data-stu-id="7c070-172">Before enabling this policy setting, make sure that you have configured the <strong>MBAM Recovery and Hardware service endpoint</strong> setting in the <strong>Configure MBAM Services</strong> policy options.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="7c070-173">Wenn Sie diese Richtlinieneinstellung entweder deaktivieren oder nicht konfigurieren, wird das Computermodell nicht anhand der Hardwarekompatibilitätsliste überprüft.</span><span class="sxs-lookup"><span data-stu-id="7c070-173">If you either disable or do not configure this policy setting, the computer model is not validated against the hardware compatibility list.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7c070-174">Konfigurieren von Benutzer Freistellungs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="7c070-174">Configure user exemption policy</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c070-175">Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</span><span class="sxs-lookup"><span data-stu-id="7c070-175">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="7c070-176">Mit dieser Richtlinieneinstellung können Sie eine Websiteadresse, e-Mail-Adresse oder Telefonnummer konfigurieren, mit der ein Benutzer angewiesen wird, eine Ausnahme von der BitLocker-Verschlüsselung anzufordern.</span><span class="sxs-lookup"><span data-stu-id="7c070-176">This policy setting lets you configure a web site address, email address, or phone number that will instruct a user to request an exemption from BitLocker encryption.</span></span></p>
<p><span data-ttu-id="7c070-177">Wenn Sie diese Richtlinieneinstellung aktivieren und eine Websiteadresse, e-Mail-Adresse oder Telefonnummer angeben, wird ein Dialogfeld angezeigt, in dem Benutzer eine Anleitung zum beantragen einer Ausnahme vom BitLocker-Schutz sehen.</span><span class="sxs-lookup"><span data-stu-id="7c070-177">If you enable this policy setting and provide a web site address, email address, or phone number, users will see a dialog with instructions on how to apply for an exemption from BitLocker protection.</span></span> <span data-ttu-id="7c070-178">Weitere Informationen zum Aktivieren von BitLocker-Verschlüsselungs Ausnahmen für Benutzer finden Sie unter <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)"> so wird es gemacht: Verwalten von Benutzer-BitLocker-Verschlüsselungs Ausnahmen </a> .</span><span class="sxs-lookup"><span data-stu-id="7c070-178">For more information about how to enable BitLocker encryption exemptions for users, see <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)">How to Manage User BitLocker Encryption Exemptions</a>.</span></span></p>
<p><span data-ttu-id="7c070-179">Wenn Sie diese Richtlinieneinstellung entweder deaktivieren oder nicht konfigurieren, werden die Anweisungen zum beantragen einer ausnahmeanforderung nicht für die Benutzer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7c070-179">If you either disable or do not configure this policy setting, the instructions about how to apply for an exemption request will not be presented to users.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="7c070-180">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="7c070-180">Note</span></span></strong><br/><p><span data-ttu-id="7c070-181">Die Benutzer Befreiung wird pro Benutzer und nicht pro Computer verwaltet.</span><span class="sxs-lookup"><span data-stu-id="7c070-181">User exemption is managed per user, not per computer.</span></span> <span data-ttu-id="7c070-182">Wenn sich mehrere Benutzer am gleichen Computer anmelden und ein Benutzer nicht freigestellt ist, wird der Computer verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="7c070-182">If multiple users log on to the same computer and one user is not exempt, the computer will be encrypted.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="7c070-183">Definitionen fester Laufwerk Richtlinien</span><span class="sxs-lookup"><span data-stu-id="7c070-183">Fixed Drive policy definitions</span></span>


<span data-ttu-id="7c070-184">In diesem Abschnitt werden die Definitionen fester Laufwerk Richtlinien für MBAM beschrieben, die unter dem folgenden GPO-Knoten zu finden sind: **Computerkonfigurations**- \\ **Administrative Vorlagen** \\ **Windows Components** \\ **MDOP MBAM (BitLocker-Verwaltung)**  \\  **festes Laufwerk**.</span><span class="sxs-lookup"><span data-stu-id="7c070-184">This section describes the Fixed Drive policy definitions for MBAM, which can be found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Fixed Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7c070-185">Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="7c070-185">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="7c070-186">Übersicht und vorgeschlagene Richtlinieneinstellung</span><span class="sxs-lookup"><span data-stu-id="7c070-186">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7c070-187">Einstellungen für die Verschlüsselung fester Datenlaufwerke</span><span class="sxs-lookup"><span data-stu-id="7c070-187">Fixed data drive encryption settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c070-188">Empfohlene Konfiguration: <strong> aktiviert </strong> , und aktivieren Sie das <strong> Kontrollkästchen Automatisches Entsperren eines festgelegten Datenlaufwerks, </strong> Wenn das Volume des Betriebssystems verschlüsselt werden muss.</span><span class="sxs-lookup"><span data-stu-id="7c070-188">Suggested Configuration: <strong>Enabled</strong>, and select the <strong>Enable auto-unlock fixed data drive</strong> check box if the operating system volume is required to be encrypted.</span></span></p>
<p><span data-ttu-id="7c070-189">Mit dieser Richtlinieneinstellung können Sie verwalten, ob die festen Laufwerke verschlüsselt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7c070-189">This policy setting lets you manage whether or not to encrypt the fixed drives.</span></span></p>
<p><span data-ttu-id="7c070-190">Wenn Sie diese Richtlinie aktivieren, deaktivieren Sie die <strong> Richtlinie für die Verwendung von Kennwort für feste Datenlaufwerke konfigurieren </strong> .</span><span class="sxs-lookup"><span data-stu-id="7c070-190">When you enable this policy, do not disable the <strong>Configure use of password for fixed data drives</strong> policy.</span></span></p>
<p><span data-ttu-id="7c070-191">Wenn das <strong> Kontrollkästchen automatische Sperrung von festem Datenlaufwerk aktivieren </strong> aktiviert ist, muss das Betriebssystemvolume verschlüsselt sein.</span><span class="sxs-lookup"><span data-stu-id="7c070-191">If the <strong>Enable auto-unlock fixed data drive</strong> check box is selected, the operating system volume must be encrypted.</span></span></p>
<p><span data-ttu-id="7c070-192">Wenn Sie diese Richtlinieneinstellung aktivieren, müssen die Benutzer alle Festplatten unter BitLocker-Schutz setzen, wodurch die Laufwerke verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="7c070-192">If you enable this policy setting, users are required to put all fixed drives under BitLocker protection, which will encrypt the drives.</span></span></p>
<p><span data-ttu-id="7c070-193">Wenn Sie diese Richtlinie nicht konfigurieren oder wenn Sie diese Richtlinie deaktivieren, müssen Benutzer keine festen Laufwerke unter dem BitLocker-Schutz speichern.</span><span class="sxs-lookup"><span data-stu-id="7c070-193">If you do not configure this policy or if you disable this policy, users are not required to put fixed drives under BitLocker protection.</span></span></p>
<p><span data-ttu-id="7c070-194">Wenn Sie diese Richtlinie deaktivieren, entschlüsselt der MBAM-Agent alle verschlüsselten Festplatten.</span><span class="sxs-lookup"><span data-stu-id="7c070-194">If you disable this policy, the MBAM agent decrypts any encrypted fixed drives.</span></span></p>
<p><span data-ttu-id="7c070-195">Wenn die Verschlüsselung des Betriebssystemdatenträgers nicht erforderlich ist, deaktivieren <strong> Sie das Kontrollkästchen automatische Sperrung von festem Datenlaufwerk aktivieren </strong> .</span><span class="sxs-lookup"><span data-stu-id="7c070-195">If encrypting the operating system volume is not required, clear the <strong>Enable auto-unlock fixed data drive</strong> check box.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7c070-196">Verweigern der Schreibberechtigung für feste Laufwerke, die nicht durch BitLocker geschützt sind</span><span class="sxs-lookup"><span data-stu-id="7c070-196">Deny “write” permission to fixed drives that are not protected by BitLocker</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c070-197">Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</span><span class="sxs-lookup"><span data-stu-id="7c070-197">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="7c070-198">Diese Richtlinieneinstellung bestimmt, ob der BitLocker-Schutz für feste Laufwerke auf einem Computer erforderlich ist, damit Sie beschreibbar sind.</span><span class="sxs-lookup"><span data-stu-id="7c070-198">This policy setting determines if BitLocker protection is required for fixed drives on a computer so that they are writable.</span></span> <span data-ttu-id="7c070-199">Diese Richtlinieneinstellung wird angewendet, wenn Sie BitLocker aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7c070-199">This policy setting is applied when you turn on BitLocker.</span></span></p>
<p><span data-ttu-id="7c070-200">Wenn die Richtlinie nicht konfiguriert ist, werden alle festen Laufwerke auf dem Computer mit Lese-und Schreibberechtigungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7c070-200">When the policy is not configured, all fixed drives on the computer are mounted with read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7c070-201">Gewähren des Zugriffs auf von BitLocker geschützte Festplatten aus früheren Versionen von Windows</span><span class="sxs-lookup"><span data-stu-id="7c070-201">Allow access to BitLocker-protected fixed drives from earlier versions of Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c070-202">Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</span><span class="sxs-lookup"><span data-stu-id="7c070-202">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="7c070-203">Aktivieren Sie diese Richtlinie, um die festen Laufwerke, die mit dem Dateizuordnungstabelle (FAT)-Dateisystem auf Computern mit Windows Server 2008, Windows Vista, Windows XP mit SP3 oder Windows XP mit SP2 formatiert sind, zu entsperren und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7c070-203">Enable this policy to unlock and view the fixed drives that are formatted with the file allocation table (FAT) file system on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p>
<p><span data-ttu-id="7c070-204">Diese Betriebssysteme verfügen über schreibgeschützte Berechtigungen für BitLocker-geschützte Laufwerke.</span><span class="sxs-lookup"><span data-stu-id="7c070-204">These operating systems have read-only permissions to BitLocker-protected drives.</span></span></p>
<p><span data-ttu-id="7c070-205">Wenn die Richtlinie deaktiviert ist, können Festplatten, die mit dem FAT-Dateisystem formatiert sind, nicht entsperrt werden, und der Inhalt kann nicht auf Computern angezeigt werden, auf denen Windows Server 2008, Windows Vista, Windows XP mit SP3 oder Windows XP mit SP2 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c070-205">When the policy is disabled, fixed drives formatted with the FAT file system cannot be unlocked and their content cannot be viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7c070-206">Konfigurieren der Verwendung des Kennworts für feste Laufwerke</span><span class="sxs-lookup"><span data-stu-id="7c070-206">Configure use of password for fixed drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c070-207">Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</span><span class="sxs-lookup"><span data-stu-id="7c070-207">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="7c070-208">Aktivieren Sie diese Richtlinie zum Konfigurieren des Kennwortschutzes auf Festplatten.</span><span class="sxs-lookup"><span data-stu-id="7c070-208">Enable this policy to configure password protection on fixed drives.</span></span></p>
<p><span data-ttu-id="7c070-209">Wenn die Richtlinie nicht konfiguriert ist, werden Kennwörter mit den Standardeinstellungen unterstützt, die keine Anforderungen an die Kennwortkomplexität enthalten und nur acht Zeichen erfordern.</span><span class="sxs-lookup"><span data-stu-id="7c070-209">When the policy is not configured, passwords will be supported with the default settings, which do not include password complexity requirements and require only eight characters.</span></span></p>
<p><span data-ttu-id="7c070-210">Aktivieren Sie für höhere Sicherheit diese Richtlinie, und wählen Sie <strong> Kennwort für festes Datenlaufwerk anfordern aus </strong> , wählen Sie <strong> Kennwortkomplexität anfordern aus </strong> , und legen Sie die gewünschte <strong> minimale Kennwortlänge fest </strong> .</span><span class="sxs-lookup"><span data-stu-id="7c070-210">For higher security, enable this policy and select <strong>Require password for fixed data drive</strong>, select <strong>Require password complexity</strong>, and set the desired <strong>minimum password length</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7c070-211">Auswählen, wie BitLocker-geschützte Festplatten wiederhergestellt werden können</span><span class="sxs-lookup"><span data-stu-id="7c070-211">Choose how BitLocker-protected fixed drives can be recovered</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c070-212">Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</span><span class="sxs-lookup"><span data-stu-id="7c070-212">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="7c070-213">Konfigurieren Sie diese Richtlinie, um den BitLocker-Daten Wiederherstellungs-Agent zu aktivieren oder BitLocker-Wiederherstellungsinformationen in Active Directory-Domänendiensten (AD DS) zu speichern.</span><span class="sxs-lookup"><span data-stu-id="7c070-213">Configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="7c070-214">Wenn diese Richtlinie nicht konfiguriert ist, ist der BitLocker-Daten Wiederherstellungs-Agent zulässig, und Wiederherstellungsinformationen werden nicht in AD DS gesichert.</span><span class="sxs-lookup"><span data-stu-id="7c070-214">When this policy is not configured, the BitLocker data recovery agent is allowed, and recovery information is not backed up to AD DS.</span></span> <span data-ttu-id="7c070-215">Für MBAM müssen die Wiederherstellungsinformationen nicht in AD DS gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="7c070-215">MBAM does not require the recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="7c070-216">Richtlinien Definitionen für das Betriebs System Laufwerk</span><span class="sxs-lookup"><span data-stu-id="7c070-216">Operating System Drive policy definitions</span></span>


<span data-ttu-id="7c070-217">In diesem Abschnitt werden die Richtlinien Definitionen für das Betriebssystemlaufwerk für MBAM beschrieben, die unter dem folgenden GPO-Knoten gefunden werden: **Computerkonfigurations**- \\ **Administrative Vorlagen** \\ **Windows Components** \\ **MDOP MBAM (BitLocker Management)**-  \\  **Betriebs System Laufwerk**.</span><span class="sxs-lookup"><span data-stu-id="7c070-217">This section describes the Operating System Drive policy definitions for MBAM, found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Operating System Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7c070-218">Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="7c070-218">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="7c070-219">Übersicht und vorgeschlagene Richtlinieneinstellung</span><span class="sxs-lookup"><span data-stu-id="7c070-219">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7c070-220">Verschlüsselungseinstellungen für das Betriebssystemlaufwerk</span><span class="sxs-lookup"><span data-stu-id="7c070-220">Operating system drive encryption settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c070-221">Empfohlene Konfiguration: <strong> aktiviert</span><span class="sxs-lookup"><span data-stu-id="7c070-221">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="7c070-222">Diese Richtlinieneinstellung bestimmt, ob das Betriebssystemlaufwerk verschlüsselt wird.</span><span class="sxs-lookup"><span data-stu-id="7c070-222">This policy setting determines if the operating system drive will be encrypted.</span></span></p>
<p><span data-ttu-id="7c070-223">Konfigurieren Sie diese Richtlinie für die folgenden Aktionen:</span><span class="sxs-lookup"><span data-stu-id="7c070-223">Configure this policy to do the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="7c070-224">Erzwingen des BitLocker-Schutzes für das Betriebssystemlaufwerk</span><span class="sxs-lookup"><span data-stu-id="7c070-224">Enforce BitLocker protection for the operating system drive.</span></span></p></li>
<li><p><span data-ttu-id="7c070-225">Konfigurieren Sie die PIN-Verwendung für die Verwendung einer TPM-PIN (Trusted Platform Module) für den Schutz des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="7c070-225">Configure PIN usage to use a Trusted Platform Module (TPM) PIN for operating system protection.</span></span></p></li>
<li><p><span data-ttu-id="7c070-226">Konfigurieren Sie erweiterte Start Pins, um Zeichen wie groß-und Kleinbuchstaben sowie Zahlen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7c070-226">Configure enhanced startup PINs to permit characters such as uppercase and lowercase letters, and numbers.</span></span> <span data-ttu-id="7c070-227">MBAM unterstützt nicht die Verwendung von Symbolen und Leerzeichen für erweiterte Pins, obwohl BitLocker Symbole und Leerzeichen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7c070-227">MBAM does not support the use of symbols and spaces for enhanced PINs, even though BitLocker supports symbols and spaces.</span></span></p></li>
</ul>
<p><span data-ttu-id="7c070-228">Wenn Sie diese Richtlinieneinstellung aktivieren, müssen Benutzer das Betriebssystemlaufwerk mithilfe von BitLocker sichern.</span><span class="sxs-lookup"><span data-stu-id="7c070-228">If you enable this policy setting, users are required to secure the operating system drive by using BitLocker.</span></span></p>
<p><span data-ttu-id="7c070-229">Wenn Sie die Einstellung nicht konfigurieren oder deaktivieren, müssen Benutzer das Betriebssystemlaufwerk nicht mithilfe von BitLocker sichern.</span><span class="sxs-lookup"><span data-stu-id="7c070-229">If you do not configure or if you disable the setting, users are not required to secure the operating system drive by using BitLocker.</span></span></p>
<p><span data-ttu-id="7c070-230">Wenn Sie diese Richtlinie deaktivieren, entschlüsselt der MBAM-Agent das Betriebssystemvolume, wenn es verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="7c070-230">If you disable this policy, the MBAM agent decrypts the operating system volume if it is encrypted.</span></span></p>
<p><span data-ttu-id="7c070-231">Wenn diese Option aktiviert ist, müssen die Benutzer das Betriebssystem mithilfe des BitLocker-Schutzes sichern, und das Laufwerk ist verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="7c070-231">When it is enabled, this policy setting requires users to secure the operating system by using BitLocker protection, and the drive is encrypted.</span></span> <span data-ttu-id="7c070-232">Basierend auf Ihren Verschlüsselungsanforderungen können Sie die Schutzmethode für das Betriebssystemlaufwerk auswählen.</span><span class="sxs-lookup"><span data-stu-id="7c070-232">Based on your encryption requirements, you may select the method of protection for the operating system drive.</span></span></p>
<p><span data-ttu-id="7c070-233">Verwenden Sie für höhere Sicherheitsanforderungen TPM + PIN, ermöglichen Sie erweiterte Pins, und setzen Sie die minimale PIN-Länge auf acht Zeichen.</span><span class="sxs-lookup"><span data-stu-id="7c070-233">For higher security requirements, use TPM + PIN, allow enhanced PINs, and set the minimum PIN length to eight characters.</span></span></p>
<p><span data-ttu-id="7c070-234">Wenn diese Richtlinie mit der TPM +-PIN-Schutzfunktion aktiviert ist, können Sie die folgenden Richtlinien unter <strong> </strong>  /  <strong> Energie Verwaltungs </strong>  /  <strong> Einstellungen für Energieverwaltung deaktivieren </strong> :</span><span class="sxs-lookup"><span data-stu-id="7c070-234">When this policy is enabled with the TPM + PIN protector, you can consider disabling the following policies under <strong>System</strong> / <strong>Power Management</strong> / <strong>Sleep Settings</strong>:</span></span></p>
<ul>
<li><p><span data-ttu-id="7c070-235">Standby-Status (S1-S3) beim schlafen zulassen (angeschlossen)</span><span class="sxs-lookup"><span data-stu-id="7c070-235">Allow Standby States (S1-S3) When Sleeping (Plugged In)</span></span></p></li>
<li><p><span data-ttu-id="7c070-236">Standby-Status (S1-S3) beim schlafen zulassen (auf Akku)</span><span class="sxs-lookup"><span data-stu-id="7c070-236">Allow Standby States (S1-S3) When Sleeping (On Battery)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7c070-237">Konfigurieren des TPM-Platt Form Überprüfungsprofils</span><span class="sxs-lookup"><span data-stu-id="7c070-237">Configure TPM platform validation profile</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c070-238">Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</span><span class="sxs-lookup"><span data-stu-id="7c070-238">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="7c070-239">Mit dieser Richtlinieneinstellung können Sie konfigurieren, wie die TPM-Sicherheitshardware auf einem Computer den BitLocker-Verschlüsselungsschlüssel sichert.</span><span class="sxs-lookup"><span data-stu-id="7c070-239">This policy setting lets you configure how the TPM security hardware on a computer secures the BitLocker encryption key.</span></span> <span data-ttu-id="7c070-240">Diese Richtlinieneinstellung trifft nicht zu, wenn der Computer nicht über ein kompatibles TPM verfügt oder wenn BitLocker bereits den TPM-Schutz aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="7c070-240">This policy setting does not apply if the computer does not have a compatible TPM or if BitLocker already has TPM protection enabled.</span></span></p>
<p><span data-ttu-id="7c070-241">Wenn diese Richtlinie nicht konfiguriert ist, verwendet das TPM das standardmäßige Platt Form Überprüfungsprofil oder das Platt Form Überprüfungsprofil, das vom Setupskript angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7c070-241">When this policy is not configured, the TPM uses the default platform validation profile or the platform validation profile specified by the setup script.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7c070-242">Auswählen, wie BitLocker-geschützte Betriebssystemlaufwerke wiederhergestellt werden</span><span class="sxs-lookup"><span data-stu-id="7c070-242">Choose how to recover BitLocker-protected operating system drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c070-243">Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</span><span class="sxs-lookup"><span data-stu-id="7c070-243">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="7c070-244">Konfigurieren Sie diese Richtlinie, um den BitLocker-Daten Wiederherstellungs-Agent zu aktivieren oder BitLocker-Wiederherstellungsinformationen in Active Directory-Domänendiensten (AD DS) zu speichern.</span><span class="sxs-lookup"><span data-stu-id="7c070-244">Configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="7c070-245">Wenn diese Richtlinie nicht konfiguriert ist, ist der Daten Wiederherstellungs-Agent zulässig, und die Wiederherstellungsinformationen werden nicht in AD DS gesichert.</span><span class="sxs-lookup"><span data-stu-id="7c070-245">When this policy is not configured, the data recovery agent is allowed, and the recovery information is not backed up to AD DS.</span></span></p>
<p><span data-ttu-id="7c070-246">Für den MBAM-Vorgang müssen die Wiederherstellungsinformationen nicht in AD DS gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="7c070-246">MBAM operation does not require the recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="7c070-247">Definitionen für Wechsellaufwerks Richtlinien</span><span class="sxs-lookup"><span data-stu-id="7c070-247">Removable Drive policy definitions</span></span>


<span data-ttu-id="7c070-248">In diesem Abschnitt werden die Richtlinien Definitionen für Wechseldatenträger für MBAM beschrieben, die unter dem folgenden GPO-Knoten gefunden werden: **Computerkonfigurations**- \\ **Administrative Vorlagen** \\ **Windows Components** \\ **MDOP MBAM (BitLocker Management)**-  \\  **Wechsellaufwerk**.</span><span class="sxs-lookup"><span data-stu-id="7c070-248">This section describes the Removable Drive Policy definitions for MBAM, found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Removable Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7c070-249">Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="7c070-249">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="7c070-250">Übersicht und vorgeschlagene Richtlinieneinstellung</span><span class="sxs-lookup"><span data-stu-id="7c070-250">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7c070-251">Steuern der Verwendung von BitLocker auf Wechseldatenträgern</span><span class="sxs-lookup"><span data-stu-id="7c070-251">Control the use of BitLocker on removable drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c070-252">Empfohlene Konfiguration: <strong> aktiviert</span><span class="sxs-lookup"><span data-stu-id="7c070-252">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="7c070-253">Diese Richtlinie steuert die Verwendung von BitLocker auf Wechseldaten Laufwerken.</span><span class="sxs-lookup"><span data-stu-id="7c070-253">This policy controls the use of BitLocker on removable data drives.</span></span></p>
<p><span data-ttu-id="7c070-254">Aktivieren Sie das <strong> Kontrollkästchen Benutzer können BitLocker-Schutz auf Wechseldatenträgern anwenden </strong> , damit Benutzer den BitLocker-Setup-Assistenten auf einem Wechseldatenträger ausführen können.</span><span class="sxs-lookup"><span data-stu-id="7c070-254">Enable the <strong>Allow users to apply BitLocker protection on removable data drives</strong> option, to allow users to run the BitLocker setup wizard on a removable data drive.</span></span></p>
<p><span data-ttu-id="7c070-255">Aktivieren Sie das <strong> Kontrollkästchen Benutzer können BitLocker auf Wechseldatenträgern Sperren und entschlüsseln </strong> , damit Benutzer die BitLocker-Laufwerkverschlüsselung vom Laufwerk entfernen oder die Verschlüsselung während der Wartung anhalten können.</span><span class="sxs-lookup"><span data-stu-id="7c070-255">Enable the <strong>Allow users to suspend and decrypt BitLocker on removable data drives</strong> option to allow users to remove BitLocker drive encryption from the drive or to suspend the encryption while maintenance is performed.</span></span></p>
<p><span data-ttu-id="7c070-256">Wenn diese Richtlinie aktiviert ist und die <strong> Option Benutzer können BitLocker-Schutz auf Wechseldatenträgern anwenden aktiviert </strong> ist, speichert der MBAM-Client die Wiederherstellungsinformationen zu Wechseldatenträgern auf dem MBAM-Schlüssel Wiederherstellungsserver und ermöglicht Benutzern das Wiederherstellen des Laufwerks, wenn das Kennwort verloren geht.</span><span class="sxs-lookup"><span data-stu-id="7c070-256">When this policy is enabled and the <strong>Allow users to apply BitLocker protection on removable data drives</strong> option is selected, the MBAM Client saves the recovery information about removable drives to the MBAM key recovery server, and it allows users to recover the drive if the password is lost.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7c070-257">Verweigern der Schreibberechtigungen für Wechseldatenträger, die nicht durch BitLocker geschützt sind</span><span class="sxs-lookup"><span data-stu-id="7c070-257">Deny the “write” permissions to removable drives that are not protected by BitLocker</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c070-258">Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</span><span class="sxs-lookup"><span data-stu-id="7c070-258">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="7c070-259">Aktivieren Sie diese Richtlinie, damit nur-Leseberechtigungen für BitLocker-geschützte Laufwerke zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="7c070-259">Enable this policy to allow write-only permissions to BitLocker protected drives.</span></span></p>
<p><span data-ttu-id="7c070-260">Wenn diese Richtlinie aktiviert ist, müssen alle auf dem Computer entfernbaren Datenlaufwerke verschlüsselt werden, bevor Schreibberechtigungen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="7c070-260">When this policy is enabled, all removable data drives on the computer require encryption before write permissions are allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7c070-261">Gewähren des Zugriffs auf von BitLocker geschützte Wechseldatenträger aus früheren Versionen von Windows</span><span class="sxs-lookup"><span data-stu-id="7c070-261">Allow access to BitLocker-protected removable drives from earlier versions of Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c070-262">Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</span><span class="sxs-lookup"><span data-stu-id="7c070-262">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="7c070-263">Aktivieren Sie diese Richtlinie, um die festen Laufwerke, die mit dem (FAT)-Dateisystem formatiert sind, auf Computern, auf denen Windows Server 2008, Windows Vista, Windows XP mit SP3 oder Windows XP mit SP2 ausgeführt wird, zu entsperren und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7c070-263">Enable this policy to unlock and view the fixed drives that are formatted with the (FAT) file system on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p>
<p><span data-ttu-id="7c070-264">Diese Betriebssysteme verfügen über schreibgeschützte Berechtigungen für BitLocker-geschützte Laufwerke.</span><span class="sxs-lookup"><span data-stu-id="7c070-264">These operating systems have read-only permissions to BitLocker-protected drives.</span></span></p>
<p><span data-ttu-id="7c070-265">Wenn die Richtlinie deaktiviert ist, können Wechseldatenträger, die mit dem FAT-Dateisystem formatiert sind, nicht entsperrt werden, und der Inhalt kann nicht auf Computern angezeigt werden, auf denen Windows Server 2008, Windows Vista, Windows XP mit SP3 oder Windows XP mit SP2 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c070-265">When the policy is disabled, removable drives formatted with the FAT file system cannot be unlocked and their content cannot be viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7c070-266">Konfigurieren der Verwendung des Kennworts für Wechseldaten Laufwerke</span><span class="sxs-lookup"><span data-stu-id="7c070-266">Configure the use of password for removable data drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c070-267">Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</span><span class="sxs-lookup"><span data-stu-id="7c070-267">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="7c070-268">Aktivieren Sie diese Richtlinie, um den Kennwortschutz auf Wechseldatenträgern zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7c070-268">Enable this policy to configure password protection on removable data drives.</span></span></p>
<p><span data-ttu-id="7c070-269">Wenn diese Richtlinie nicht konfiguriert ist, werden Kennwörter mit den Standardeinstellungen unterstützt, die keine Anforderungen an die Kennwortkomplexität enthalten und nur acht Zeichen erfordern.</span><span class="sxs-lookup"><span data-stu-id="7c070-269">When this policy is not configured, passwords are supported with the default settings, which do not include password complexity requirements and require only eight characters.</span></span></p>
<p><span data-ttu-id="7c070-270">Um die Sicherheit zu erhöhen, können Sie diese Richtlinie aktivieren und <strong> das Kennwort für Wechseldatenträger anfordern auswählen </strong> , <strong> die Option Kennwortkomplexität anfordern auswählen </strong> und dann die gewünschte <strong> Mindestlänge für das Kennwort festlegen </strong> .</span><span class="sxs-lookup"><span data-stu-id="7c070-270">For increased security, you can enable this policy and select <strong>Require password for removable data drive</strong>, select <strong>Require password complexity</strong>, and then set the preferred <strong>minimum password length</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7c070-271">Auswählen, wie BitLocker-geschützte Wechsellaufwerke wiederhergestellt werden können</span><span class="sxs-lookup"><span data-stu-id="7c070-271">Choose how BitLocker-protected removable drives can be recovered</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c070-272">Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</span><span class="sxs-lookup"><span data-stu-id="7c070-272">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="7c070-273">Sie können diese Richtlinie so konfigurieren, dass der BitLocker-Daten Wiederherstellungs-Agent aktiviert oder BitLocker-Wiederherstellungsinformationen in Active Directory-Domänendiensten (AD DS) gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7c070-273">You can configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="7c070-274">Wenn die Richtlinie auf "nicht konfiguriert" festgelegt ist <strong> </strong> , ist der Daten Wiederherstellungs-Agent zulässig, und die Wiederherstellungsinformationen werden nicht in AD DS gesichert.</span><span class="sxs-lookup"><span data-stu-id="7c070-274">When the policy is set to <strong>Not Configured</strong>, the data recovery agent is allowed and recovery information is not backed up to AD DS.</span></span></p>
<p><span data-ttu-id="7c070-275">Für den MBAM-Vorgang müssen die Wiederherstellungsinformationen nicht in AD DS gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="7c070-275">MBAM operation does not require the recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="7c070-276">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7c070-276">Related topics</span></span>


[<span data-ttu-id="7c070-277">Vorbereiten der Umgebung für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="7c070-277">Preparing your Environment for MBAM 1.0</span></span>](preparing-your-environment-for-mbam-10.md)









