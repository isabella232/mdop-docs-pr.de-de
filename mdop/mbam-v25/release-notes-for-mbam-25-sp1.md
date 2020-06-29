---
title: Versionshinweise für MBAM 2.5SP1
description: Versionshinweise für MBAM 2.5SP1
author: dansimp
ms.assetid: 3ac424c8-c490-4d62-aba4-1b462c02e962
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/06/2017
ms.openlocfilehash: 837892897aeca341433de54aca1228c0faeee124
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810885"
---
# <span data-ttu-id="13c0a-103">Versionshinweise für MBAM 2.5SP1</span><span class="sxs-lookup"><span data-stu-id="13c0a-103">Release Notes for MBAM 2.5 SP1</span></span>


<span data-ttu-id="13c0a-104">Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="13c0a-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="13c0a-105">Lesen Sie diese Versionshinweise gründlich, bevor Sie Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 SP1 installieren.</span><span class="sxs-lookup"><span data-stu-id="13c0a-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1.</span></span> <span data-ttu-id="13c0a-106">Diese Versionshinweise enthalten Informationen, die zur erfolgreichen Installation von MBAM erforderlich sind, und können Informationen enthalten, die in der Produktdokumentation nicht zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="13c0a-106">These release notes contain information that is required to successfully install MBAM and can contain information that is not available in the product documentation.</span></span> <span data-ttu-id="13c0a-107">Wenn sich diese Versionshinweise von der anderen MBAM 2,5 SP1-Dokumentation unterscheiden, sollten Sie die neueste Änderung als autorisierend ansehen.</span><span class="sxs-lookup"><span data-stu-id="13c0a-107">If these release notes differ from other MBAM 2.5 SP1 documentation, consider the latest change to be authoritative.</span></span> <span data-ttu-id="13c0a-108">Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="13c0a-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-5-sp1-known-issues"></a> <span data-ttu-id="13c0a-109">Bekannte Probleme mit MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="13c0a-109">MBAM 2.5 SP1 known issues</span></span>


<span data-ttu-id="13c0a-110">Dieser Abschnitt enthält Anmerkungen zu dieser Version von MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="13c0a-110">This section contains release notes for MBAM 2.5 SP1.</span></span>

### <a href="" id="powershell-read-ad--cmdlets-do-not-provide-feedback-if-user-does-not-have-sufficient-rights"></a><span data-ttu-id="13c0a-111">PowerShell Read-AD \ \*-Cmdlets geben kein Feedback, wenn der Benutzer nicht über ausreichende Rechte verfügt</span><span class="sxs-lookup"><span data-stu-id="13c0a-111">PowerShell Read-AD\* cmdlets do not provide feedback if user does not have sufficient rights</span></span>

<span data-ttu-id="13c0a-112">Wenn ein Benutzer, der versucht, die PowerShell-Cmdlets "Read-AD \ \*" für den MBAM-Server zu verwenden, nicht über Benutzerrechte zum Lesen der Active Directory-Wiederherstellungsinformationen oder zum Lesen der TPM-Informationen verfügt, werden die Cmdlets dem Benutzer keinen Fehler oder keine Warnung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="13c0a-112">If a user trying to use the PowerShell Read-AD\* cmdlets for the MBAM Server does not have user rights to read the Active Directory recovery information or to read the TPM information, the cmdlets will not provide the user with any error or warning.</span></span>

<span data-ttu-id="13c0a-113">**Problemumgehung:** Verwenden Sie nur die PowerShell Read-AD \ \*-Cmdlets, wenn Sie über die erforderlichen Benutzerrechte verfügen.</span><span class="sxs-lookup"><span data-stu-id="13c0a-113">**Workaround:** Only use the PowerShell Read-AD\* cmdlets if you have the required user rights.</span></span>

### <span data-ttu-id="13c0a-114">MBAM Active Directory (AD)-Migrations-Cmdlets rufen keine Datenträger Wiederherstellungsinformationen ab</span><span class="sxs-lookup"><span data-stu-id="13c0a-114">MBAM Active Directory (AD) Migration cmdlets do not retrieve volume recovery information</span></span>

<span data-ttu-id="13c0a-115">Bei MBAM Active Directory (AD)-Migrations Cmdlets können keine Datenträger Wiederherstellungsinformationen für Computer in Organisationseinheiten abgerufen werden, wenn der Schrägstrich (/) Teil des ou-namens ist.</span><span class="sxs-lookup"><span data-stu-id="13c0a-115">MBAM Active Directory (AD) Migration cmdlets fail to retrieve volume recovery information for computers in organizational units (OUs) if the forward slash character (/) is part of the OU name.</span></span> <span data-ttu-id="13c0a-116">Wiederholte AD-Pulls schlagen fehl, wenn bei diesem Fehler ein Pipeline Abbruchfehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="13c0a-116">Repeated AD pulls will fail with a pipeline terminating error when this error is encountered.</span></span>

<span data-ttu-id="13c0a-117">**Technische Informationen:** Dieser Fehler wird angezeigt, wenn Sie den Befehl ausführen:</span><span class="sxs-lookup"><span data-stu-id="13c0a-117">**Technical Details:** You will see this error when running the command:</span></span>

``` syntax
Read-ADRecoveryInformation : Unknown error (0x80005000)
At line:1 char:1
+ Read-ADRecoveryInformation -Server "…" -SearchBase " ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : NotSpecified: (:) [Read-ADRecoveryInformation], COMException
    + FullyQualifiedErrorId : System.Runtime.InteropServices.COMException,Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADRecoveryInformationCommand
```

<span data-ttu-id="13c0a-118">Darüber hinaus sieht die Ausnahmestapelüberwachung `Error[0].Exception.StackTrace` wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="13c0a-118">In addition, the Exception stack trace `Error[0].Exception.StackTrace` will look like this:</span></span>

``` syntax
   at System.DirectoryServices.DirectoryEntry.Bind(Boolean throwIfFail)
   at System.DirectoryServices.DirectoryEntry.Bind()
   at System.DirectoryServices.DirectoryEntry.get_AdsObject()
   at System.DirectoryServices.PropertyValueCollection.PopulateList()
   at System.DirectoryServices.PropertyValueCollection..ctor(DirectoryEntry entry, String propertyName)
   at System.DirectoryServices.PropertyCollection.get_Item(String propertyName)
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.VerifySettingsConnectivity()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.ExecuteRead()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADInformationBase.ProcessRecord()
   at System.Management.Automation.CommandProcessor.ProcessRecord()
```

<span data-ttu-id="13c0a-119">**Problemumgehung:** Führen Sie eine der folgenden Aufgaben aus, um dieses Problem zu beheben:</span><span class="sxs-lookup"><span data-stu-id="13c0a-119">**Workaround:** Perform one of these tasks to resolve this situation:</span></span>

-   <span data-ttu-id="13c0a-120">Benennen Sie die OU um, um den Schrägstrich zu entfernen, und führen Sie dann das Skript aus.</span><span class="sxs-lookup"><span data-stu-id="13c0a-120">Rename the OU to remove the forward slash character and then run the script.</span></span>

-   <span data-ttu-id="13c0a-121">Wenn Sie eine problematische ou aus dem Sicherungsprozess ausschließen möchten, suchen Sie nach einer Liste von OUs, deren Namen nicht das Schrägstrichzeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="13c0a-121">To exclude any problematic OU from the backup process, find a list of OUs whose names do not contain the forward slash character.</span></span> <span data-ttu-id="13c0a-122">Führen Sie das Skript in diesen OUs, jeweils eine OU, aus.</span><span class="sxs-lookup"><span data-stu-id="13c0a-122">Run the script on these OUs, one OU at a time.</span></span>

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> <span data-ttu-id="13c0a-123">MBAM kann ein Volume nicht verschlüsseln und meldet einen Fehler, wenn Sie auf einem Tablet-Gerät ein TPM + PIN Protector festzulegen</span><span class="sxs-lookup"><span data-stu-id="13c0a-123">MBAM fails to encrypt a volume and reports an error if you set a TPM + PIN protector on a tablet device</span></span>

<span data-ttu-id="13c0a-124">Wenn Endbenutzer versuchen, eine TPM + PIN-Beschützer auf einem Tablet-Gerät festzulegen, kann MBAM nicht verschlüsselt werden, und es wird ein Fehler gemeldet.</span><span class="sxs-lookup"><span data-stu-id="13c0a-124">If end users try to set a TPM + PIN protector on a tablet device, MBAM fails to encrypt, and it reports an error.</span></span> <span data-ttu-id="13c0a-125">Dieses Problem tritt auf, weil Tablet-Geräte nicht über eine Pre-Boot-Umgebungs Tastatur verfügen.</span><span class="sxs-lookup"><span data-stu-id="13c0a-125">This issue occurs because tablet devices do not have a pre-boot environment keyboard.</span></span>

<span data-ttu-id="13c0a-126">**Problemumgehung:** Aktivieren Sie die Option **Verwendung der BitLocker-Authentifizierung aktivieren, die für die Gruppenrichtlinieneinstellung Vorstart Tastatureingabe erforderlich** ist.</span><span class="sxs-lookup"><span data-stu-id="13c0a-126">**Workaround:** Enable the **Enable use of BitLocker authentication requiring preboot keyboard input on tablets** Group Policy setting.</span></span> <span data-ttu-id="13c0a-127">Diese Einstellung ist eine BitLocker-Gruppenrichtlinieneinstellung und steht in den MBAM-Gruppenrichtlinienvorlagen nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="13c0a-127">This setting is a BitLocker Group Policy setting and is not available in the MBAM Group Policy Templates.</span></span>

### <span data-ttu-id="13c0a-128">Benutzerprinzipalname ist für alle Dienstkonten erforderlich</span><span class="sxs-lookup"><span data-stu-id="13c0a-128">User principal name is required for all service accounts</span></span>

<span data-ttu-id="13c0a-129">Für alle Dienstkonten in MBAM muss ein Benutzerprinzipalname (User Principal Name, UPN) eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="13c0a-129">A user principal name (UPN) must be set for all service accounts in MBAM.</span></span> <span data-ttu-id="13c0a-130">Wenn Sie einen UPN für ein Konto nicht erstellen, wird während des Konfigurationsprozesses eine Fehlermeldung angezeigt, die besagt, dass der Benutzer oder die Gruppe nicht in Active Directory gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="13c0a-130">If you fail to create a UPN for an account, an error message appears during the configuration process to indicate that the user or group could not be found in Active Directory.</span></span>

<span data-ttu-id="13c0a-131">**Problemumgehung:** Fügen Sie den UPN dem Dienstkonto hinzu.</span><span class="sxs-lookup"><span data-stu-id="13c0a-131">**Workaround:** Add the UPN to the service account.</span></span>

### <span data-ttu-id="13c0a-132">Self-Service-Portal und die Verwaltungs-und Überwachungs Website werden nicht geöffnet, nachdem Sie IIS auf .NET Framework 4,5 aktualisiert haben</span><span class="sxs-lookup"><span data-stu-id="13c0a-132">Self-Service Portal and the Administration and Monitoring Website do not open after you upgrade IIS to .NET Framework 4.5</span></span>

<span data-ttu-id="13c0a-133">Wenn Sie Internet Informationsdienste (IIS) auf das Microsoft .NET Framework 4,5 aktualisieren, werden das Self-Service-Portal und die Website Verwaltung und Überwachung nicht geöffnet.</span><span class="sxs-lookup"><span data-stu-id="13c0a-133">When you upgrade Internet Information Services (IIS) to the Microsoft .NET Framework 4.5, the Self-Service Portal and the Administration and Monitoring Website do not open.</span></span>

<span data-ttu-id="13c0a-134">**Problemumgehung:** Lesen Sie den Artikel [Fehlermeldung nach der Installation von .NET Framework 4,0: "der Typ konnte nicht geladen werden" System. ServiceModel. Activation. HttpModule "](https://go.microsoft.com/fwlink/?LinkId=393568).</span><span class="sxs-lookup"><span data-stu-id="13c0a-134">**Workaround:** See the article [Error message after you install the .NET Framework 4.0: "Could not load type 'System.ServiceModel.Activation.HttpModule'](https://go.microsoft.com/fwlink/?LinkId=393568).</span></span>

### <span data-ttu-id="13c0a-135">Website "Verwaltung und Überwachung" zeigt die Fehlermeldung "Bericht kann nicht gefunden werden" an, wenn Berichte nicht konfiguriert sind</span><span class="sxs-lookup"><span data-stu-id="13c0a-135">Administration and Monitoring Website displays a "Report cannot be found" error message when Reports are not configured</span></span>

<span data-ttu-id="13c0a-136">Wenn Sie die Website Verwaltung und Überwachung konfigurieren und dann versuchen, einen Bericht anzuzeigen, ohne zuerst das Feature Berichte zu konfigurieren, wird eine Fehlermeldung angezeigt, die besagt, dass der Bericht nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="13c0a-136">If you configure the Administration and Monitoring Website and then try to view a report without configuring the Reports feature first, an error message indicates that the report cannot be found.</span></span>

<span data-ttu-id="13c0a-137">**Problemumgehung:** Konfigurieren Sie das Feature Berichte, bevor Sie die Webanwendungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="13c0a-137">**Workaround:** Configure the Reports feature before you configure the web applications.</span></span>

### <span data-ttu-id="13c0a-138">Berichte auf der Website "Verwaltung und Überwachung" zeigen eine Warnung an, wenn SSL in SSRS nicht konfiguriert ist</span><span class="sxs-lookup"><span data-stu-id="13c0a-138">Reports in the Administration and Monitoring Website display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="13c0a-139">Wenn SQL Server Reporting Services (SSRS) nicht für die Verwendung von Secure Socket Layer (SSL) konfiguriert wurde, wird die URL für das Feature Berichte auf http anstatt auf HTTPS festgelegt, wenn Sie den MBAM-Server konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="13c0a-139">If SQL Server Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the Reports feature will be set to HTTP instead of to HTTPS when you configure the MBAM Server.</span></span> <span data-ttu-id="13c0a-140">Wenn Sie dann die Website Verwaltung und Überwachung öffnen und einen Bericht auswählen, wird die folgende Fehlermeldung angezeigt: "nur sicherer Inhalt wird angezeigt."</span><span class="sxs-lookup"><span data-stu-id="13c0a-140">If you then open the Administration and Monitoring Website and select a report, the following error message appears: "Only Secure Content is Displayed."</span></span>

<span data-ttu-id="13c0a-141">**Problemumgehung:** Klicken Sie auf **alle Inhalte anzeigen**, um den Bericht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="13c0a-141">**Workaround:** To show the report, click **Show All Content**.</span></span> <span data-ttu-id="13c0a-142">Um dieses Problem zu beheben, wechseln Sie zum MBAM-Computer, auf dem SQL Server Reporting Services installiert ist, führen Sie **Reporting Services-Konfigurations-Manager**aus, und klicken Sie dann auf **Webdienst-URL**.</span><span class="sxs-lookup"><span data-stu-id="13c0a-142">To correct this issue, go to the MBAM computer where SQL Server Reporting Services is installed, run **Reporting Services Configuration Manager**, and then click **Web Service URL**.</span></span> <span data-ttu-id="13c0a-143">Wählen Sie das entsprechende SSL-Zertifikat für den Server aus, geben Sie den entsprechenden SSL-Port ein (der Standardport ist 443), und klicken Sie dann auf über **nehmen**.</span><span class="sxs-lookup"><span data-stu-id="13c0a-143">Select the appropriate SSL certificate for the server, enter the appropriate SSL port (the default port is 443), and then click **Apply**.</span></span>

### <span data-ttu-id="13c0a-144">Wenn Sie im Bericht zur BitLocker-Konformitätszusammenfassung auf "zurück" klicken, wird möglicherweise ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="13c0a-144">Clicking "Back" in the BitLocker Compliance Summary report might throw an error</span></span>

<span data-ttu-id="13c0a-145">Wenn Sie einen Drilldown in einen BitLocker-Kompatibilitäts Zusammenfassungsbericht ausführen und dann im SSRS-Bericht auf den Link **zurück** klicken, wird möglicherweise ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="13c0a-145">If you drill down into a BitLocker Compliance Summary report, and then click the **Back** link in the SSRS report, an error might be thrown.</span></span>

<span data-ttu-id="13c0a-146">**Problemumgehung:** Keine.</span><span class="sxs-lookup"><span data-stu-id="13c0a-146">**Workaround:** None.</span></span>

### <span data-ttu-id="13c0a-147">Die Verschlüsselungsstärke wird im BitLocker-Computer Kompatibilitätsbericht falsch angezeigt</span><span class="sxs-lookup"><span data-stu-id="13c0a-147">Cipher strength displays incorrectly on the BitLocker Computer Compliance report</span></span>

<span data-ttu-id="13c0a-148">Wenn Sie keine bestimmte Verschlüsselungsstärke in den Gruppenrichtlinienobjekten " **Laufwerksverschlüsselung auswählen" und "Verschlüsselungsstärke"** festlegen, wird im BitLocker-Computer Kompatibilitätsbericht in der Configuration Manager-Integrations Topologie immer "unbekannt" für die Verschlüsselungsstärke angezeigt, selbst wenn die Verschlüsselungsstärke den Standardwert der 128-Bit-Verschlüsselung verwendet.</span><span class="sxs-lookup"><span data-stu-id="13c0a-148">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the BitLocker Computer Compliance report in the Configuration Manager Integration topology always displays "unknown" for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="13c0a-149">Der Bericht zeigt die richtige Verschlüsselungsstärke an, wenn Sie eine bestimmte Verschlüsselungsstärke im Gruppenrichtlinienobjekt festlegen.</span><span class="sxs-lookup"><span data-stu-id="13c0a-149">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="13c0a-150">**Problemumgehung:** Legen Sie immer eine bestimmte Verschlüsselungsstärke im Gruppenrichtlinienobjekt **Auswählen von Laufwerk Verschlüsselungsmethode und Verschlüsselungsstärke** fest.</span><span class="sxs-lookup"><span data-stu-id="13c0a-150">**Workaround:** Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="13c0a-151">Kompatibilitäts Status Verteilung nach Laufwerks zeigt alte Daten an, nachdem Sie Konfigurationselemente aktualisiert haben</span><span class="sxs-lookup"><span data-stu-id="13c0a-151">Compliance Status Distribution By Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="13c0a-152">Nachdem Sie MBAM-Konfigurationselemente in SystemCenter2012 ConfigurationManager aktualisiert haben, werden auf dem BitLocker Enterprise Compliance-Dashboard Daten angezeigt, die auf Informationen aus älteren Versionen der Konfigurationselemente basieren.</span><span class="sxs-lookup"><span data-stu-id="13c0a-152">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="13c0a-153">**Problemumgehung:** Keine.</span><span class="sxs-lookup"><span data-stu-id="13c0a-153">**Workaround:** None.</span></span> <span data-ttu-id="13c0a-154">Änderungen der MBAM-Konfigurationselemente werden nicht unterstützt, und der Bericht wird möglicherweise nicht wie erwartet angezeigt.</span><span class="sxs-lookup"><span data-stu-id="13c0a-154">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="13c0a-155">Verbesserte Sicherheitskonfiguration kann dazu führen, dass Berichte eine Fehlermeldung falsch anzeigen</span><span class="sxs-lookup"><span data-stu-id="13c0a-155">Enhanced Security Configuration might cause reports to display an error message incorrectly</span></span>

<span data-ttu-id="13c0a-156">Wenn Internet Explorer Enhanced Security Configuration (ESC) aktiviert ist, wird möglicherweise eine Fehlermeldung "Zugriff verweigert" angezeigt, wenn Sie versuchen, Berichte auf dem MBAM-Server anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="13c0a-156">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an "Access Denied" error message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="13c0a-157">Standardmäßig ist ESC aktiviert, um den Server zu schützen, indem die Anfälligkeit des Servers für potenzielle Angriffe verringert wird, die über Webinhalte und Anwendungsskripts auftreten können.</span><span class="sxs-lookup"><span data-stu-id="13c0a-157">By default, ESC is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="13c0a-158">**Problemumgehung:** Wenn die Fehlermeldung "Zugriff verweigert" angezeigt wird, wenn Sie versuchen, Berichte auf dem MBAM-Server anzuzeigen, können Sie ein Gruppenrichtlinienobjekt festlegen oder den Standardwert manuell in Ihrem Bild ändern, um die erweiterte Sicherheitskonfiguration zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="13c0a-158">**Workaround:** If the "Access Denied" error message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="13c0a-159">Sie können auch die Berichte auf einem anderen Computer anzeigen, auf dem ESC nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="13c0a-159">You can also alternatively view the reports from another computer on which ESC is not enabled.</span></span>

### <span data-ttu-id="13c0a-160">Unterstützung für den BitLocker-XTS-AES-Verschlüsselungsalgorithmus</span><span class="sxs-lookup"><span data-stu-id="13c0a-160">Support for Bitlocker XTS-AES encryption algorithm</span></span>
<span data-ttu-id="13c0a-161">BitLocker hat Unterstützung für den XTS-AES-Verschlüsselungsalgorithmus in Windows 10, Version 1511, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="13c0a-161">Bitlocker added support for the XTS-AES encryption algorithm in Windows 10, version 1511.</span></span> <span data-ttu-id="13c0a-162">Mit HF02 hat MBAM Clientunterstützung für diese BitLocker-Option hinzugefügt, und in HF04 wurde die serverseitige Unterstützung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="13c0a-162">With HF02, MBAM added client support for this Bitlocker option and in HF04, the server-side support was added.</span></span> <span data-ttu-id="13c0a-163">Es gibt jedoch eine bekannte Einschränkung:</span><span class="sxs-lookup"><span data-stu-id="13c0a-163">However, there is one known limitation:</span></span>

* <span data-ttu-id="13c0a-164">Kunden müssen dieselbe Verschlüsselungsstärke für Betriebssystem-und Daten-Volumes auf demselben Computer verwenden.</span><span class="sxs-lookup"><span data-stu-id="13c0a-164">Customers must use the same encryption strength for OS and data volumes on the same machine.</span></span>
<span data-ttu-id="13c0a-165">Bei Verwendung unterschiedlicher Verschlüsselungsstärken meldet MBAM den Computer als **nicht kompatibel**.</span><span class="sxs-lookup"><span data-stu-id="13c0a-165">If different encryption strengths are used, MBAM will report the machine as **non-compliant**.</span></span>

### <span data-ttu-id="13c0a-166">Self-Service-Portal fügt automatisch "-" bei Schlüssel-ID-Eintrag hinzu</span><span class="sxs-lookup"><span data-stu-id="13c0a-166">Self-Service Portal automatically adds "-" on Key ID entry</span></span>
<span data-ttu-id="13c0a-167">Ab HF02 fügt das MBAM Self-Service-Portal automatisch den Schlüssel-ID-Eintrag "-" hinzu.</span><span class="sxs-lookup"><span data-stu-id="13c0a-167">As of HF02, the MBAM Self-Service Portal automatically adds the '-' on Key ID entry.</span></span>  
<span data-ttu-id="13c0a-168">**Hinweis:** Der Server muss neu konfiguriert werden, damit das JavaScript wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="13c0a-168">**Note:** The Server has to be reconfigured for the Javascript to take effect.</span></span>

### <span data-ttu-id="13c0a-169">MBAM 2,5 SP1-Berichte funktionieren/werden nicht ordnungsgemäß gerendert</span><span class="sxs-lookup"><span data-stu-id="13c0a-169">MBAM 2.5 Sp1 Reports does not work / render properly</span></span>
<span data-ttu-id="13c0a-170">Die Seite "Berichte" wird nicht ordnungsgemäß gerendert, wenn SSRS in SQL Server 2016 Edition gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="13c0a-170">Reports Page does not render properly when SSRS is hosted on SQL Server 2016 edition.</span></span> 
<span data-ttu-id="13c0a-171">Zum Beispiel: Durchsuchen des Helpdesks – klicken auf Berichte – (hervorgehobener Anteil hat "x"), der dies mit Fiddler weiter ausgräbt – es sieht so aus, als ob wir auf Berichte klicken – er ruft die Seite SSRS mit dem HTML 4,0-Rendering-Format auf.</span><span class="sxs-lookup"><span data-stu-id="13c0a-171">For example – Browsing to Helpdesk – Clicking on Reports – ( Highlighted portion have “x” on it ) Digging this further with Fiddler – it does look like once we click on Reports – it calls the SSRS page with HTML 4.0 rendering format.</span></span>

<span data-ttu-id="13c0a-172">**Problemumgehung:** Sehen Sie sich den Website-Master-Code an und beachten Sie, dass der X-UA-Modus als IE8 diktiert wurde.</span><span class="sxs-lookup"><span data-stu-id="13c0a-172">**Workaround:** Looking at the site.master code and noticed the X-UA mode was dictated as IE8.</span></span> <span data-ttu-id="13c0a-173">Da IE8 weit hinter dem Ende des Lebens liegt und der Kunde IE11 verwendet.</span><span class="sxs-lookup"><span data-stu-id="13c0a-173">As IE8 is WAY past the end of life, and customer is using IE11.</span></span> <span data-ttu-id="13c0a-174">Aktualisieren Sie die Einstellung auf den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="13c0a-174">Update the setting to the below code.</span></span> <span data-ttu-id="13c0a-175">Auf diese Weise kann die Website IE11-Rendering-Technologien verwenden</span><span class="sxs-lookup"><span data-stu-id="13c0a-175">This allows the site to utilize IE11 rendering technologies</span></span>

    <meta http-equiv="X-UA-Compatible" content="IE=Edge" />

<span data-ttu-id="13c0a-176">Die ursprüngliche Einstellung lautet:</span><span class="sxs-lookup"><span data-stu-id="13c0a-176">Original setting is:</span></span> 

    <meta http-equiv="X-UA-Compatible" content="IE=8" />


<span data-ttu-id="13c0a-177">Aus diesem Grund wurde das Problem bei anderen Browsern wie Chrome, Firefox usw. nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="13c0a-177">This is the reason why the issue was not seen with other browsers like Chrome, Firefox etc.</span></span>



## <span data-ttu-id="13c0a-178">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="13c0a-178">Related topics</span></span>


[<span data-ttu-id="13c0a-179">Informationen zu MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="13c0a-179">About MBAM 2.5</span></span>](about-mbam-25.md)

 

## <span data-ttu-id="13c0a-180">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="13c0a-180">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="13c0a-181">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="13c0a-181">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="13c0a-182">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="13c0a-182">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





