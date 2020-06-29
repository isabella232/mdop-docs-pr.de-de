---
title: Versionshinweise für MBAM 2.5
description: Versionshinweise für MBAM 2.5
author: dansimp
ms.assetid: fcaf03e6-5e39-4771-af3c-a3cd468f3961
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4bcc17d6295b14a7f3276146d5630b869b94b7f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810882"
---
# <span data-ttu-id="de42e-103">Versionshinweise für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="de42e-103">Release Notes for MBAM 2.5</span></span>


<span data-ttu-id="de42e-104">Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="de42e-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="de42e-105">Lesen Sie diese Versionshinweise gründlich, bevor Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 installieren.</span><span class="sxs-lookup"><span data-stu-id="de42e-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM) 2.5.</span></span> <span data-ttu-id="de42e-106">Diese Versionshinweise enthalten Informationen, die zur erfolgreichen Installation von MBAM erforderlich sind, und können Informationen enthalten, die in der Produktdokumentation nicht zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="de42e-106">These release notes contain information that is required to successfully install MBAM and can contain information that is not available in the product documentation.</span></span> <span data-ttu-id="de42e-107">Wenn sich diese Versionshinweise von der anderen MBAM 2,5-Dokumentation unterscheiden, sollten Sie die neueste Änderung als autorisierend ansehen.</span><span class="sxs-lookup"><span data-stu-id="de42e-107">If these release notes differ from other MBAM 2.5 documentation, consider the latest change to be authoritative.</span></span> <span data-ttu-id="de42e-108">Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="de42e-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-5-known-issues"></a> <span data-ttu-id="de42e-109">MBAM 2,5 bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="de42e-109">MBAM 2.5 known issues</span></span>


<span data-ttu-id="de42e-110">Dieser Abschnitt enthält Anmerkungen zu dieser Version von MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="de42e-110">This section contains release notes for MBAM 2.5.</span></span>

### <span data-ttu-id="de42e-111">Webbrowser wird versehentlich als Administrator ausgeführt</span><span class="sxs-lookup"><span data-stu-id="de42e-111">Web browser unintentionally run as administrator</span></span>

<span data-ttu-id="de42e-112">Hilfe Links im MBAM Server-Konfigurationstool können dazu führen, dass Browserfenster mit Administratorrechten geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="de42e-112">Help links in the MBAM Server Configuration tool can cause browser windows to open with administrator rights.</span></span>

<span data-ttu-id="de42e-113">**Problemumgehung:** Aktivieren Sie Internet Explorer Enhanced Security Configuration (IESC), oder schließen Sie den Webbrowser, bevor Sie zu anderen Websites navigieren.</span><span class="sxs-lookup"><span data-stu-id="de42e-113">**Workaround:** Enable Internet Explorer Enhanced Security Configuration (IESC) or close your web browser before navigating to other sites.</span></span>

<span data-ttu-id="de42e-114">**Hinweis**  Dies ist in MBAM 2,5 SP1 behoben.</span><span class="sxs-lookup"><span data-stu-id="de42e-114">**Note** This is fixed in MBAM 2.5 SP1.</span></span>

 

### <a href="" id="-------------mbam-reports-as-noncompliant-a-client-encrypted-with-aes-256-bit-encryption-keys-and-diffuser"></a> <span data-ttu-id="de42e-115">MBAM-Berichte als nicht kompatibel ein Client, der mit AES 256-Bit-Verschlüsselungsschlüsseln und Diffusor verschlüsselt ist</span><span class="sxs-lookup"><span data-stu-id="de42e-115">MBAM reports as noncompliant a client encrypted with AES 256-bit encryption keys and Diffuser</span></span>

<span data-ttu-id="de42e-116">Wenn auf einem Computer der MBAM 2,5-Client installiert ist und mithilfe des AES 256-Bit mit Diffusor-Verschlüsselungsstärke verschlüsselt wird, wird der MBAM-Client in den MBAM-Konformitätsberichten als nicht kompatibel gemeldet.</span><span class="sxs-lookup"><span data-stu-id="de42e-116">If a computer has the MBAM 2.5 client installed and is encrypted by using the AES 256-bit with Diffuser cipher strength, the MBAM client is reported as noncompliant in the MBAM compliance reports.</span></span>

<span data-ttu-id="de42e-117">**Problemumgehung:** Installieren Sie den Hotfix unter [KB2975636](https://go.microsoft.com/fwlink/?LinkId=511972).</span><span class="sxs-lookup"><span data-stu-id="de42e-117">**Workaround:** Install the hotfix at [KB2975636](https://go.microsoft.com/fwlink/?LinkId=511972).</span></span>

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> <span data-ttu-id="de42e-118">MBAM kann ein Volume nicht verschlüsseln und meldet einen Fehler, wenn Sie auf einem Tablet-Gerät ein TPM + PIN Protector festzulegen</span><span class="sxs-lookup"><span data-stu-id="de42e-118">MBAM fails to encrypt a volume and reports an error if you set a TPM + PIN protector on a tablet device</span></span>

<span data-ttu-id="de42e-119">Wenn Endbenutzer versuchen, eine TPM + PIN-Beschützer auf einem Tablet-Gerät festzulegen, kann MBAM nicht verschlüsselt werden, und es wird ein Fehler gemeldet.</span><span class="sxs-lookup"><span data-stu-id="de42e-119">If end users try to set a TPM + PIN protector on a tablet device, MBAM fails to encrypt, and it reports an error.</span></span> <span data-ttu-id="de42e-120">Dieses Problem tritt auf, weil Tablet-Geräte nicht über eine Pre-Boot-Umgebungs Tastatur verfügen.</span><span class="sxs-lookup"><span data-stu-id="de42e-120">This issue occurs because tablet devices do not have a pre-boot environment keyboard.</span></span>

<span data-ttu-id="de42e-121">**Problemumgehung:** Aktivieren Sie die Option **Verwendung der BitLocker-Authentifizierung aktivieren, die für die Gruppenrichtlinieneinstellung Vorstart Tastatureingabe erforderlich** ist.</span><span class="sxs-lookup"><span data-stu-id="de42e-121">**Workaround:** Enable the **Enable use of BitLocker authentication requiring preboot keyboard input on tablets** Group Policy setting.</span></span> <span data-ttu-id="de42e-122">Diese Einstellung ist eine BitLocker-Gruppenrichtlinieneinstellung und steht in den MBAM-Gruppenrichtlinienvorlagen nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="de42e-122">This setting is a BitLocker Group Policy setting and is not available in the MBAM Group Policy Templates.</span></span>

### <span data-ttu-id="de42e-123">Benutzerprinzipalname ist für alle Dienstkonten erforderlich</span><span class="sxs-lookup"><span data-stu-id="de42e-123">User principal name is required for all service accounts</span></span>

<span data-ttu-id="de42e-124">Für alle Dienstkonten in MBAM muss ein Benutzerprinzipalname (User Principal Name, UPN) eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="de42e-124">A user principal name (UPN) must be set for all service accounts in MBAM.</span></span> <span data-ttu-id="de42e-125">Wenn Sie einen UPN für ein Konto nicht erstellen, wird während des Konfigurationsprozesses eine Fehlermeldung angezeigt, die besagt, dass der Benutzer oder die Gruppe nicht in Active Directory gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="de42e-125">If you fail to create a UPN for an account, an error message appears during the configuration process to indicate that the user or group could not be found in Active Directory.</span></span>

<span data-ttu-id="de42e-126">**Problemumgehung:** Fügen Sie den UPN dem Dienstkonto hinzu.</span><span class="sxs-lookup"><span data-stu-id="de42e-126">**Workaround:** Add the UPN to the service account.</span></span>

### <span data-ttu-id="de42e-127">Self-Service-Portal erfordert zusätzliche Konfiguration, wenn Clientcomputer nicht auf das Microsoft AJAX Content Delivery Network zugreifen können</span><span class="sxs-lookup"><span data-stu-id="de42e-127">Self-Service Portal requires additional configuration if client computers cannot access Microsoft Ajax Content Delivery Network</span></span>

<span data-ttu-id="de42e-128">Wenn Ihre Clientcomputer keinen Zugriff auf das Microsoft AJAX Content Delivery Network (CDN) haben, das dem Self-Service-Portal den für bestimmte JavaScript-Dateien erforderlichen Zugriff gewährt, müssen Sie das Self-Service-Portal so konfigurieren, dass es von einer barrierefreien Quelle aus auf die JavaScript-Dateien verweist.</span><span class="sxs-lookup"><span data-stu-id="de42e-128">If your client computers do not have access to the Microsoft Ajax Content Delivery Network (CDN), which gives the Self-Service Portal the access that it requires to certain JavaScript files, you must configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span> <span data-ttu-id="de42e-129">Wenn Sie das Self-Service-Portal nicht konfigurieren, wenn Clientcomputer nicht auf CDN zugreifen können, werden nur der Firmenname und das Konto angezeigt, unter dem Sie sich angemeldet haben.</span><span class="sxs-lookup"><span data-stu-id="de42e-129">If you don’t configure the Self-Service Portal when client computers cannot access CDN, only the company name and the account under which you logged on is displayed.</span></span> <span data-ttu-id="de42e-130">Es wird keine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="de42e-130">No error message appears.</span></span>

<span data-ttu-id="de42e-131">**Problemumgehung:** Installieren Sie MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="de42e-131">**Workaround:** Install MBAM 2.5 SP1.</span></span> <span data-ttu-id="de42e-132">oder konfigurieren Sie das Self-Service-Portal, indem Sie die folgenden Anweisungen ausführen: [Konfigurieren des Self-Service-Portals, wenn Client Computer nicht auf das Microsoft Content Delivery Network zugreifen können](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span><span class="sxs-lookup"><span data-stu-id="de42e-132">or configure the Self-Service Portal by following these instructions: [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span></span>

### <span data-ttu-id="de42e-133">Self-Service-Portal und die Verwaltungs-und Überwachungs Website werden nicht geöffnet, nachdem Sie IIS auf .NET Framework 4,5 aktualisiert haben</span><span class="sxs-lookup"><span data-stu-id="de42e-133">Self-Service Portal and the Administration and Monitoring Website do not open after you upgrade IIS to .NET Framework 4.5</span></span>

<span data-ttu-id="de42e-134">Wenn Sie Internet Informationsdienste (IIS) auf das Microsoft .NET Framework 4,5 aktualisieren, werden das Self-Service-Portal und die Website Verwaltung und Überwachung nicht geöffnet.</span><span class="sxs-lookup"><span data-stu-id="de42e-134">When you upgrade Internet Information Services (IIS) to the Microsoft .NET Framework 4.5, the Self-Service Portal and the Administration and Monitoring Website do not open.</span></span>

<span data-ttu-id="de42e-135">**Problemumgehung:** Lesen Sie den Artikel [Fehlermeldung nach der Installation von .NET Framework 4,0: "der Typ konnte nicht geladen werden" System. ServiceModel. Activation. HttpModule "](https://go.microsoft.com/fwlink/?LinkId=393568).</span><span class="sxs-lookup"><span data-stu-id="de42e-135">**Workaround:** See the article [Error message after you install the .NET Framework 4.0: "Could not load type 'System.ServiceModel.Activation.HttpModule'](https://go.microsoft.com/fwlink/?LinkId=393568).</span></span>

### <span data-ttu-id="de42e-136">Website "Verwaltung und Überwachung" zeigt die Fehlermeldung "Bericht kann nicht gefunden werden" an, wenn Berichte nicht konfiguriert sind</span><span class="sxs-lookup"><span data-stu-id="de42e-136">Administration and Monitoring Website displays a "Report cannot be found" error message when Reports are not configured</span></span>

<span data-ttu-id="de42e-137">Wenn Sie die Website Verwaltung und Überwachung konfigurieren und dann versuchen, einen Bericht anzuzeigen, ohne zuerst das Feature Berichte zu konfigurieren, wird eine Fehlermeldung angezeigt, die besagt, dass der Bericht nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="de42e-137">If you configure the Administration and Monitoring Website and then try to view a report without configuring the Reports feature first, an error message indicates that the report cannot be found.</span></span>

<span data-ttu-id="de42e-138">**Problemumgehung:** Konfigurieren Sie das Feature Berichte, bevor Sie die Webanwendungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="de42e-138">**Workaround:** Configure the Reports feature before you configure the web applications.</span></span>

### <span data-ttu-id="de42e-139">Berichte auf der Website "Verwaltung und Überwachung" zeigen eine Warnung an, wenn SSL in SSRS nicht konfiguriert ist</span><span class="sxs-lookup"><span data-stu-id="de42e-139">Reports in the Administration and Monitoring Website display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="de42e-140">Wenn SQL Server Reporting Services (SSRS) nicht für die Verwendung von Secure Socket Layer (SSL) konfiguriert wurde, wird die URL für das Feature Berichte auf http anstatt auf HTTPS festgelegt, wenn Sie den MBAM-Server konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="de42e-140">If SQL Server Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the Reports feature will be set to HTTP instead of to HTTPS when you configure the MBAM Server.</span></span> <span data-ttu-id="de42e-141">Wenn Sie dann die Website Verwaltung und Überwachung öffnen und einen Bericht auswählen, wird die folgende Fehlermeldung angezeigt: "nur sicherer Inhalt wird angezeigt."</span><span class="sxs-lookup"><span data-stu-id="de42e-141">If you then open the Administration and Monitoring Website and select a report, the following error message appears: "Only Secure Content is Displayed."</span></span>

<span data-ttu-id="de42e-142">**Problemumgehung:** Klicken Sie auf **alle Inhalte anzeigen**, um den Bericht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="de42e-142">**Workaround:** To show the report, click **Show All Content**.</span></span> <span data-ttu-id="de42e-143">Um dieses Problem zu beheben, wechseln Sie zum MBAM-Computer, auf dem SQL Server Reporting Services installiert ist, führen Sie **Reporting Services-Konfigurations-Manager**aus, und klicken Sie dann auf **Webdienst-URL**.</span><span class="sxs-lookup"><span data-stu-id="de42e-143">To correct this issue, go to the MBAM computer where SQL Server Reporting Services is installed, run **Reporting Services Configuration Manager**, and then click **Web Service URL**.</span></span> <span data-ttu-id="de42e-144">Wählen Sie das entsprechende SSL-Zertifikat für den Server aus, geben Sie den entsprechenden SSL-Port ein (der Standardport ist 443), und klicken Sie dann auf über **nehmen**.</span><span class="sxs-lookup"><span data-stu-id="de42e-144">Select the appropriate SSL certificate for the server, enter the appropriate SSL port (the default port is 443), and then click **Apply**.</span></span>

### <span data-ttu-id="de42e-145">Wenn Sie im Bericht zur BitLocker-Konformitätszusammenfassung auf "zurück" klicken, wird möglicherweise ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="de42e-145">Clicking "Back" in the BitLocker Compliance Summary report might throw an error</span></span>

<span data-ttu-id="de42e-146">Wenn Sie einen Drilldown in einen BitLocker-Kompatibilitäts Zusammenfassungsbericht ausführen und dann im SSRS-Bericht auf den Link **zurück** klicken, wird möglicherweise ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="de42e-146">If you drill down into a BitLocker Compliance Summary report, and then click the **Back** link in the SSRS report, an error might be thrown.</span></span>

<span data-ttu-id="de42e-147">**Problemumgehung:** Keine.</span><span class="sxs-lookup"><span data-stu-id="de42e-147">**Workaround:** None.</span></span>

### <span data-ttu-id="de42e-148">Verwendeter Speicherplatz nur die Verschlüsselung funktioniert nicht ordnungsgemäß</span><span class="sxs-lookup"><span data-stu-id="de42e-148">Used Space Only Encryption does not work correctly</span></span>

<span data-ttu-id="de42e-149">Wenn Sie einen Computer nach der Installation des MBAM-Clients zum ersten Mal verschlüsseln und eine Gruppenrichtlinieneinstellung zum Implementieren der nur verwendeter Speicherplatz Verschlüsselung konfiguriert haben, verschlüsselt MBAM fälschlicherweise den gesamten Datenträger, anstatt nur den verwendeten Speicherplatz der Festplatte zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="de42e-149">If you encrypt a computer for the first time after you install the MBAM Client, and you have configured a Group Policy setting to implement Used Space Only encryption, MBAM erroneously encrypts the entire disk instead of encrypting only the disk’s used space.</span></span> <span data-ttu-id="de42e-150">Wenn ein Computer bereits mit verwendetem Speicherplatz verschlüsselt ist, wenn Sie den MBAM-Client installieren, und Sie dieselbe Gruppenrichtlinieneinstellung konfiguriert haben, meldet MBAM, dass das Laufwerk richtig verschlüsselt ist, und versucht nicht, das Laufwerk erneut zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="de42e-150">If a computer is already encrypted with Used Space Only when you install the MBAM Client, and you have configured the same Group Policy setting, MBAM reports that the drive is encrypted correctly, and does not try to re-encrypt the drive.</span></span>

<span data-ttu-id="de42e-151">**Problemumgehung:** Keine.</span><span class="sxs-lookup"><span data-stu-id="de42e-151">**Workaround:** None.</span></span>

### <span data-ttu-id="de42e-152">Die Verschlüsselungsstärke wird im BitLocker-Computer Kompatibilitätsbericht falsch angezeigt</span><span class="sxs-lookup"><span data-stu-id="de42e-152">Cipher strength displays incorrectly on the BitLocker Computer Compliance report</span></span>

<span data-ttu-id="de42e-153">Wenn Sie keine bestimmte Verschlüsselungsstärke in den Gruppenrichtlinienobjekten " **Laufwerksverschlüsselung auswählen" und "Verschlüsselungsstärke"** festlegen, wird im BitLocker-Computer Kompatibilitätsbericht in der Configuration Manager-Integrations Topologie immer "unbekannt" für die Verschlüsselungsstärke angezeigt, selbst wenn die Verschlüsselungsstärke den Standardwert der 128-Bit-Verschlüsselung verwendet.</span><span class="sxs-lookup"><span data-stu-id="de42e-153">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the BitLocker Computer Compliance report in the Configuration Manager Integration topology always displays "unknown" for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="de42e-154">Der Bericht zeigt die richtige Verschlüsselungsstärke an, wenn Sie eine bestimmte Verschlüsselungsstärke im Gruppenrichtlinienobjekt festlegen.</span><span class="sxs-lookup"><span data-stu-id="de42e-154">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="de42e-155">**Problemumgehung:** Legen Sie immer eine bestimmte Verschlüsselungsstärke im Gruppenrichtlinienobjekt **Auswählen von Laufwerk Verschlüsselungsmethode und Verschlüsselungsstärke** fest.</span><span class="sxs-lookup"><span data-stu-id="de42e-155">**Workaround:** Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="de42e-156">Kompatibilitäts Status Verteilung nach Laufwerks zeigt alte Daten an, nachdem Sie Konfigurationselemente aktualisiert haben</span><span class="sxs-lookup"><span data-stu-id="de42e-156">Compliance Status Distribution by Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="de42e-157">Nachdem Sie MBAM-Konfigurationselemente in SystemCenter2012 ConfigurationManager aktualisiert haben, werden auf dem BitLocker Enterprise Compliance-Dashboard Daten angezeigt, die auf Informationen aus älteren Versionen der Konfigurationselemente basieren.</span><span class="sxs-lookup"><span data-stu-id="de42e-157">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="de42e-158">**Problemumgehung:** Keine.</span><span class="sxs-lookup"><span data-stu-id="de42e-158">**Workaround:** None.</span></span> <span data-ttu-id="de42e-159">Änderungen der MBAM-Konfigurationselemente werden nicht unterstützt, und der Bericht wird möglicherweise nicht wie erwartet angezeigt.</span><span class="sxs-lookup"><span data-stu-id="de42e-159">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="de42e-160">Verbesserte Sicherheitskonfiguration kann dazu führen, dass Berichte eine Fehlermeldung falsch anzeigen</span><span class="sxs-lookup"><span data-stu-id="de42e-160">Enhanced Security Configuration might cause reports to display an error message incorrectly</span></span>

<span data-ttu-id="de42e-161">Wenn Internet Explorer Enhanced Security Configuration (ESC) aktiviert ist, wird möglicherweise eine Fehlermeldung "Zugriff verweigert" angezeigt, wenn Sie versuchen, Berichte auf dem MBAM-Server anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="de42e-161">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an "Access Denied" error message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="de42e-162">Standardmäßig ist ESC aktiviert, um den Server zu schützen, indem die Anfälligkeit des Servers für potenzielle Angriffe verringert wird, die über Webinhalte und Anwendungsskripts auftreten können.</span><span class="sxs-lookup"><span data-stu-id="de42e-162">By default, ESC is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="de42e-163">**Problemumgehung:** Wenn die Fehlermeldung "Zugriff verweigert" angezeigt wird, wenn Sie versuchen, Berichte auf dem MBAM-Server anzuzeigen, können Sie ein Gruppenrichtlinienobjekt festlegen oder den Standardwert manuell in Ihrem Bild ändern, um die erweiterte Sicherheitskonfiguration zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="de42e-163">**Workaround:** If the "Access Denied" error message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="de42e-164">Sie können auch die Berichte auf einem anderen Computer anzeigen, auf dem ESC nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="de42e-164">You can also alternatively view the reports from another computer on which ESC is not enabled.</span></span>

## <a href="" id="hotfixes-and-knowledge-base-articles-for-mbam-2-5-"></a><span data-ttu-id="de42e-165">Hotfixes und Knowledge Base-Artikel für MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="de42e-165">Hotfixes and Knowledge Base articles for MBAM 2.5</span></span>


<span data-ttu-id="de42e-166">Diese Tabelle enthält die Hotfixes und KB-Artikel für MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="de42e-166">This table lists the hotfixes and KB articles for MBAM 2.5.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="de42e-167">KB-Artikel</span><span class="sxs-lookup"><span data-stu-id="de42e-167">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="de42e-168">Title</span><span class="sxs-lookup"><span data-stu-id="de42e-168">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="de42e-169">Link</span><span class="sxs-lookup"><span data-stu-id="de42e-169">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="de42e-170">2975636</span><span class="sxs-lookup"><span data-stu-id="de42e-170">2975636</span></span></p></td>
<td align="left"><p><span data-ttu-id="de42e-171">Hotfix-Paket 1 für Microsoft BitLocker-Verwaltung und-Überwachung 2,5</span><span class="sxs-lookup"><span data-stu-id="de42e-171">Hotfix Package 1 for Microsoft BitLocker Administration and Monitoring 2.5</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975636/EN-US" data-raw-source="[support.microsoft.com/kb/2975636/EN-US](https://support.microsoft.com/kb/2975636/EN-US)"><span data-ttu-id="de42e-172">support.microsoft.com/kb/2975636/EN-US</span><span class="sxs-lookup"><span data-stu-id="de42e-172">support.microsoft.com/kb/2975636/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="de42e-173">3015477</span><span class="sxs-lookup"><span data-stu-id="de42e-173">3015477</span></span></p></td>
<td align="left"><p><span data-ttu-id="de42e-174">Hotfix-Paket 2 für die BitLocker-Verwaltung und-Überwachung 2,5</span><span class="sxs-lookup"><span data-stu-id="de42e-174">Hotfix Package 2 for BitLocker Administration and Monitoring 2.5</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3015477" data-raw-source="[support.microsoft.com/kb/3015477](https://support.microsoft.com/kb/3015477)"><span data-ttu-id="de42e-175">support.microsoft.com/kb/3015477</span><span class="sxs-lookup"><span data-stu-id="de42e-175">support.microsoft.com/kb/3015477</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="de42e-176">3011022</span><span class="sxs-lookup"><span data-stu-id="de42e-176">3011022</span></span></p></td>
<td align="left"><p><span data-ttu-id="de42e-177">MBAM 2,5-Installation oder Configuration Manager-Berichterstellung schlägt fehl, wenn der Name der SSRS-Instanz einen Unterstrich enthält</span><span class="sxs-lookup"><span data-stu-id="de42e-177">MBAM 2.5 installation or Configuration Manager reporting fails if the name of SSRS instance contains an underscore</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3011022/EN-US" data-raw-source="[support.microsoft.com/kb/3011022/EN-US](https://support.microsoft.com/kb/3011022/EN-US)"><span data-ttu-id="de42e-178">support.microsoft.com/kb/3011022/EN-US</span><span class="sxs-lookup"><span data-stu-id="de42e-178">support.microsoft.com/kb/3011022/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="de42e-179">2756402</span><span class="sxs-lookup"><span data-stu-id="de42e-179">2756402</span></span></p></td>
<td align="left"><p><span data-ttu-id="de42e-180">MBAM-Client schlägt mit Ereignis-ID 4 und Fehlercode 0x8004100E in der Ereignisbeschreibung fehl</span><span class="sxs-lookup"><span data-stu-id="de42e-180">MBAM client would fail with Event ID 4 and error code 0x8004100E in the Event description</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)"><span data-ttu-id="de42e-181">support.microsoft.com/kb/2756402/EN-US</span><span class="sxs-lookup"><span data-stu-id="de42e-181">support.microsoft.com/kb/2756402/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="de42e-182">2639518</span><span class="sxs-lookup"><span data-stu-id="de42e-182">2639518</span></span></p></td>
<td align="left"><p><span data-ttu-id="de42e-183">Fehler beim Öffnen von Enterprise-oder Computer Kompatibilitätsberichten in MBAM</span><span class="sxs-lookup"><span data-stu-id="de42e-183">Error opening Enterprise or Computer Compliance Reports in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)"><span data-ttu-id="de42e-184">support.microsoft.com/kb/2639518/EN-US</span><span class="sxs-lookup"><span data-stu-id="de42e-184">support.microsoft.com/kb/2639518/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="de42e-185">2870842</span><span class="sxs-lookup"><span data-stu-id="de42e-185">2870842</span></span></p></td>
<td align="left"><p><span data-ttu-id="de42e-186">MBAM 2,0-Setup schlägt während des Configuration Manager-Integrationsszenarios mit SQL Server 2008 fehl</span><span class="sxs-lookup"><span data-stu-id="de42e-186">MBAM 2.0 Setup fails during Configuration Manager Integration Scenario with SQL Server 2008</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)"><span data-ttu-id="de42e-187">support.microsoft.com/kb/2870842/EN-US</span><span class="sxs-lookup"><span data-stu-id="de42e-187">support.microsoft.com/kb/2870842/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="de42e-188">2975472</span><span class="sxs-lookup"><span data-stu-id="de42e-188">2975472</span></span></p></td>
<td align="left"><p><span data-ttu-id="de42e-189">SQL-Deadlocks, wenn viele MBAM-Clients eine Verbindung mit der MBAM-Wiederherstellungsdatenbank herstellen</span><span class="sxs-lookup"><span data-stu-id="de42e-189">SQL deadlocks when many MBAM clients connect to the MBAM recovery database</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975472/EN-US" data-raw-source="[support.microsoft.com/kb/2975472/EN-US](https://support.microsoft.com/kb/2975472/EN-US)"><span data-ttu-id="de42e-190">support.microsoft.com/kb/2975472/EN-US</span><span class="sxs-lookup"><span data-stu-id="de42e-190">support.microsoft.com/kb/2975472/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="de42e-191">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="de42e-191">Related topics</span></span>


[<span data-ttu-id="de42e-192">Informationen zu MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="de42e-192">About MBAM 2.5</span></span>](about-mbam-25.md)

 

## <span data-ttu-id="de42e-193">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="de42e-193">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="de42e-194">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="de42e-194">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="de42e-195">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="de42e-195">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





