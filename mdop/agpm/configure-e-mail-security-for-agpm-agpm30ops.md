---
title: Konfigurieren von E-Mail-Sicherheit für AGPM
description: Konfigurieren von E-Mail-Sicherheit für AGPM
author: dansimp
ms.assetid: 4850ed8e-a1c6-43f0-95c5-853aa66a94ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3694662fd0ed81edacd16cf55ac9760b1be2ba97
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807727"
---
# <span data-ttu-id="a2167-103">Konfigurieren von E-Mail-Sicherheit für AGPM</span><span class="sxs-lookup"><span data-stu-id="a2167-103">Configure E-Mail Security for AGPM</span></span>


<span data-ttu-id="a2167-104">E-Mail-Benachrichtigungen, die aufgrund von Aktionen in Advanced Group Policy Management (AGPM) gesendet wurden, werden standardmäßig nicht verschlüsselt und über den SMTP-Port 25 gesendet.</span><span class="sxs-lookup"><span data-stu-id="a2167-104">By default, e-mail notifications sent because of actions in Advanced Group Policy Management (AGPM) are not encrypted and are sent through SMTP port 25.</span></span> <span data-ttu-id="a2167-105">Sie können die e-Mail-Sicherheit für AGPM jedoch mithilfe von Registrierungseinstellungen konfigurieren, um anzugeben, ob SSL-Verschlüsselung (Secure Sockets Layer) und welcher SMTP-Port verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2167-105">However, you can configure e-mail security for AGPM by using registry settings to specify whether to use Secure Sockets Layer (SSL) encryption and which SMTP port to use.</span></span>

<span data-ttu-id="a2167-106">Durch Verschlüsseln von AGPM-e-Mail-Benachrichtigungen können Sie die Personen, die vertrauliche Informationen über die Sicherheit Ihrer Organisation offen legen, besser schützen.</span><span class="sxs-lookup"><span data-stu-id="a2167-106">By encrypting AGPM e-mail notifications, you can better protect those that could reveal sensitive information about your organization’s security.</span></span> <span data-ttu-id="a2167-107">Das Verschlüsseln von e-Mail-Benachrichtigungen wird empfohlen, wenn Sie über Remote-e-Mail-Server weitergeleitet werden und möglicherweise durch einige Konformitätsrichtlinien erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a2167-107">Encrypting e-mail notifications is recommended when they are being relayed through remote mail servers, and may be required by some compliance regulations.</span></span>

<span data-ttu-id="a2167-108">**Vorsicht**  Durch unsachgemäßes Bearbeiten der Registrierung kann Ihr System schwer beschädigt werden.</span><span class="sxs-lookup"><span data-stu-id="a2167-108">**Caution** Incorrectly editing the registry may severely damage your system.</span></span> <span data-ttu-id="a2167-109">Bevor Sie Änderungen an der Registrierung vornehmen, sollten Sie alle wichtigen Daten auf dem Computer sichern.</span><span class="sxs-lookup"><span data-stu-id="a2167-109">Before making changes to the registry, you should back up any valued data on the computer.</span></span>

 

<span data-ttu-id="a2167-110">Ein Benutzerkonto, das über die Rolle AGPM-Administrator (Vollzugriff) verfügt, das Benutzerkonto der genehmigenden Person, die das in diesen Verfahren verwendete Gruppenrichtlinienobjekt (Group Policy Object, GPO) erstellt hat, oder ein Benutzerkonto, das über die erforderlichen Berechtigungen in AGPM verfügt, ist erforderlich, um diese Verfahren auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a2167-110">A user account that has the AGPM Administrator (Full Control) role, the user account of the Approver who created the Group Policy Object (GPO) used in these procedures, or a user account that has the necessary permissions in AGPM is required to complete these procedures.</span></span> <span data-ttu-id="a2167-111">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="a2167-111">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="a2167-112">So konfigurieren Sie die e-Mail-Sicherheit für AGPM mithilfe von Gruppenrichtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="a2167-112">To configure e-mail security for AGPM by using Group Policy preferences</span></span>**

1.  <span data-ttu-id="a2167-113">Bearbeiten Sie in der **Gruppenrichtlinien-Verwaltungskonsolen** Struktur ein GPO, das auf alle AGPM-Server angewendet wird, für die Sie die e-Mail-Sicherheit konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="a2167-113">In the **Group Policy Management Console** tree, edit a GPO that is applied to all AGPM Servers for which you want to configure e-mail security.</span></span> <span data-ttu-id="a2167-114">(Weitere Informationen finden Sie unter [Bearbeiten eines Gruppenrichtlinienobjekts](editing-a-gpo-agpm30ops.md).)</span><span class="sxs-lookup"><span data-stu-id="a2167-114">(For more information, see [Editing a GPO](editing-a-gpo-agpm30ops.md).)</span></span>

2.  <span data-ttu-id="a2167-115">Erweitern Sie im Fenster **Gruppenrichtlinien-Verwaltungs-Editor** die Ordner **Computer Konfiguration**, **Einstellungen**, **Windows-Einstellungen**und **Registrierung** .</span><span class="sxs-lookup"><span data-stu-id="a2167-115">In the **Group Policy Management Editor** window, expand the **Computer Configuration**, **Preferences**, **Windows Settings**, and **Registry** folders.</span></span>

3.  <span data-ttu-id="a2167-116">Klicken Sie in der Konsolenstruktur mit der rechten Maustaste auf **Registrierung**, zeigen Sie auf **neu**, klicken Sie auf **Sammlungselement**, und geben Sie **AGPM-e-Mail-Sicherheit**ein.</span><span class="sxs-lookup"><span data-stu-id="a2167-116">In the console tree, right-click **Registry**, point to **New**, click **Collection Item**, and type **AGPM e-mail security**.</span></span>

4.  <span data-ttu-id="a2167-117">Erstellen Sie ein Registrierungs Einstellungselement, um die Verschlüsselung zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="a2167-117">Create a Registry preference item to turn on encryption:</span></span>

    1.  <span data-ttu-id="a2167-118">Klicken Sie in der Konsolenstruktur mit der rechten Maustaste auf **AGPM-e-Mail-Sicherheit**, zeigen Sie auf **neu**, und klicken Sie dann auf **Registrierungselement**.</span><span class="sxs-lookup"><span data-stu-id="a2167-118">In the console tree, right-click **AGPM e-mail security**, point to **New**, and then click **Registry Item**.</span></span>

    2.  <span data-ttu-id="a2167-119">Wählen Sie im Dialogfeld **neue Registrierungseigenschaften** die Aktion **Aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="a2167-119">In the **New Registry Properties** dialog box, select the **Update** action.</span></span>

    3.  <span data-ttu-id="a2167-120">Wählen **Hive**Sie für Hive **HKEY \ _LOCAL \ _MACHINE**aus.</span><span class="sxs-lookup"><span data-stu-id="a2167-120">For **Hive**, select **HKEY\_LOCAL\_MACHINE**.</span></span>

    4.  <span data-ttu-id="a2167-121">Geben Sie für **Schlüsselpfad** **SOFTWARE\\Microsoft\\AGPM**.</span><span class="sxs-lookup"><span data-stu-id="a2167-121">For **Key Path**, type **SOFTWARE\\Microsoft\\AGPM**.</span></span>

    5.  <span data-ttu-id="a2167-122">Geben Sie für **Wertname** **EncryptSmtp**.</span><span class="sxs-lookup"><span data-stu-id="a2167-122">For **Value name**, type **EncryptSmtp**.</span></span>

    6.  <span data-ttu-id="a2167-123">Wählen Sie unter **Werttyp**die Option **reg \ _DWORD**aus.</span><span class="sxs-lookup"><span data-stu-id="a2167-123">For **Value type**, select **REG\_DWORD**.</span></span>

    7.  <span data-ttu-id="a2167-124">Wählen Sie für **Base**die Option **Decimal**aus, und geben Sie für **Wertdaten den Wert** **1 ein** , um die SSL-Verschlüsselung zu verwenden, oder **0** , damit e-Mails ohne Verschlüsselung gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a2167-124">For **Base**, select **Decimal**, and for **Value data**, type **1** to use SSL encryption, or **0** to let e-mail to be sent without encryption.</span></span> <span data-ttu-id="a2167-125">Standardmäßig werden e-Mail-Nachrichten ohne Verschlüsselung gesendet.</span><span class="sxs-lookup"><span data-stu-id="a2167-125">By default, e-mail is sent without encryption.</span></span>

    8.  <span data-ttu-id="a2167-126">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2167-126">Click **OK**.</span></span>

5.  <span data-ttu-id="a2167-127">Erstellen Sie ein Registrierungs Einstellungselement, um den SMTP-Port anzugeben:</span><span class="sxs-lookup"><span data-stu-id="a2167-127">Create a Registry preference item to specify the SMTP port:</span></span>

    1.  <span data-ttu-id="a2167-128">Klicken Sie in der Konsolenstruktur mit der rechten Maustaste auf **AGPM-e-Mail-Sicherheit**, zeigen Sie auf **neu**, und klicken Sie dann auf **Registrierungselement**.</span><span class="sxs-lookup"><span data-stu-id="a2167-128">In the console tree, right-click **AGPM E-mail security**, point to **New**, and then click **Registry Item**.</span></span>

    2.  <span data-ttu-id="a2167-129">Wählen Sie im Dialogfeld **neue Registrierungseigenschaften** die Aktion **Aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="a2167-129">In the **New Registry Properties** dialog box, select the **Update** action.</span></span>

    3.  <span data-ttu-id="a2167-130">Wählen **Hive**Sie für Hive **HKEY \ _LOCAL \ _MACHINE**aus.</span><span class="sxs-lookup"><span data-stu-id="a2167-130">For **Hive**, select **HKEY\_LOCAL\_MACHINE**.</span></span>

    4.  <span data-ttu-id="a2167-131">Geben Sie im Dialogfeld **Schlüsselpfad** den Namen **SOFTWARE\\Microsoft\\AGPM**ein.</span><span class="sxs-lookup"><span data-stu-id="a2167-131">For **Key Path** dialog box, type **SOFTWARE\\Microsoft\\AGPM**.</span></span>

    5.  <span data-ttu-id="a2167-132">Geben Sie für **Wertname** **SmtpPort**.</span><span class="sxs-lookup"><span data-stu-id="a2167-132">For **Value name**, type **SmtpPort**.</span></span>

    6.  <span data-ttu-id="a2167-133">Wählen Sie unter **Werttyp**die Option **reg \ _DWORD**aus.</span><span class="sxs-lookup"><span data-stu-id="a2167-133">For **Value type**, select **REG\_DWORD**.</span></span>

    7.  <span data-ttu-id="a2167-134">Wählen Sie für **Base**den Wert **Decimal**aus, und geben Sie für **Wertdaten**eine Portnummer für den SMTP-Port ein.</span><span class="sxs-lookup"><span data-stu-id="a2167-134">For **Base**, select **Decimal**, and for **Value data**, type a port number for the SMTP port.</span></span> <span data-ttu-id="a2167-135">Standardmäßig ist der SMTP-Port Port 25, wenn die Verschlüsselung nicht aktiviert ist, oder Port 587, wenn die SSL-Verschlüsselung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a2167-135">By default, the SMTP port is port 25 if encryption is not enabled or port 587 if SSL encryption is enabled.</span></span>

    8.  <span data-ttu-id="a2167-136">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2167-136">Click **OK**.</span></span>

6.  <span data-ttu-id="a2167-137">Schließen Sie das Fenster **Gruppenrichtlinien-Verwaltungs-Editor** , und aktivieren Sie das Gruppenrichtlinienobjekt, und stellen Sie es bereit.</span><span class="sxs-lookup"><span data-stu-id="a2167-137">Close the **Group Policy Management Editor** window, and then check in and deploy the GPO.</span></span> <span data-ttu-id="a2167-138">Weitere Informationen finden Sie unter [Bereitstellen eines Gruppenrichtlinienobjekts](deploy-a-gpo-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="a2167-138">For more information, see [Deploy a GPO](deploy-a-gpo-agpm30ops.md).</span></span>

### <span data-ttu-id="a2167-139">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="a2167-139">Additional considerations</span></span>

-   <span data-ttu-id="a2167-140">Sie müssen in der Lage sein, ein GPO zu bearbeiten und bereitzustellen, um Registrierungseinstellungen mithilfe von Gruppenrichtlinieneinstellungen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a2167-140">You must be able to edit and deploy a GPO to configure registry settings by using Group Policy Preferences.</span></span> <span data-ttu-id="a2167-141">Weitere Informationen finden Sie unter [Bearbeiten eines GPO](editing-a-gpo-agpm30ops.md) und [Bereitstellen eines Gruppenrichtlinienobjekts](deploy-a-gpo-agpm30ops.md) .</span><span class="sxs-lookup"><span data-stu-id="a2167-141">See [Editing a GPO](editing-a-gpo-agpm30ops.md) and [Deploy a GPO](deploy-a-gpo-agpm30ops.md) for additional detail.</span></span>

### <span data-ttu-id="a2167-142">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="a2167-142">Additional references</span></span>

-   [<span data-ttu-id="a2167-143">Konfigurieren von Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="a2167-143">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management.md)

 

 





