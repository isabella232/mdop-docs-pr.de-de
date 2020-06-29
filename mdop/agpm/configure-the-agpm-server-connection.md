---
title: Konfigurieren der AGPM-Server-Verbindung
description: Konfigurieren der AGPM-Server-Verbindung
author: dansimp
ms.assetid: 9a42b5bc-41be-44ef-a6e2-6f56e2cf1996
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 88182f0e79f1a8bcce53e0d50c014e8d4aa29286
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807696"
---
# <span data-ttu-id="38c2f-103">Konfigurieren der AGPM-Server-Verbindung</span><span class="sxs-lookup"><span data-stu-id="38c2f-103">Configure the AGPM Server Connection</span></span>


<span data-ttu-id="38c2f-104">Bei der erweiterten Gruppenrichtlinienverwaltung (AGPM) werden alle Versionen der einzelnen gesteuerten Gruppenrichtlinienobjekte in einem zentralen Archiv gespeichert, sodass Gruppenrichtlinienadministratoren Gruppenrichtlinienobjekte offline anzeigen und ändern können, ohne dass sich dies unmittelbar auf die bereitgestellte Version jedes GPO auswirkt.</span><span class="sxs-lookup"><span data-stu-id="38c2f-104">Advanced Group Policy Management (AGPM) stores all versions of each controlled Group Policy object (GPO) in a central archive, so Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="38c2f-105">Ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff), dem Benutzerkonto der genehmigenden Person, die das in diesen Verfahren verwendete Gruppenrichtlinienobjekt erstellt hat, oder ein Benutzerkonto mit den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung ist erforderlich, um diese Verfahren zum zentralen Konfigurieren von Archivierungsspeicher Orten für alle Gruppenrichtlinienadministratoren durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="38c2f-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO used in these procedures, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete these procedures for centrally configuring archive locations for all Group Policy administrators.</span></span> <span data-ttu-id="38c2f-106">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="38c2f-106">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="38c2f-107">Konfigurieren der AGPM-Server Verbindung</span><span class="sxs-lookup"><span data-stu-id="38c2f-107">Configuring the AGPM Server connection</span></span>


<span data-ttu-id="38c2f-108">Als AGPM-Administrator (Vollzugriff) können Sie sicherstellen, dass alle Gruppenrichtlinienadministratoren eine Verbindung mit dem gleichen AGPM-Server herstellen, indem Sie die Einstellung zentral konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="38c2f-108">As an AGPM Administrator (Full Control), you can ensure that all Group Policy administrators connect to the same AGPM Server by centrally configuring the setting.</span></span> <span data-ttu-id="38c2f-109">Wenn für Ihre Umgebung separate AGPM-Server für einige oder alle Domänen erforderlich sind, konfigurieren Sie diese zusätzlichen AGPM-Server als Ausnahmen von der Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="38c2f-109">If your environment requires separate AGPM Servers for some or all domains, configure those additional AGPM Servers as exceptions to the default.</span></span> <span data-ttu-id="38c2f-110">Wenn Sie keine AGPM-Serververbindungen zentral konfigurieren, muss jeder Gruppenrichtlinienadministrator den AGPM-Server manuell für die Anzeige für jede Domäne konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="38c2f-110">If you do not centrally configure AGPM Server connections, each Group Policy administrator must manually configure the AGPM Server to be displayed for each domain.</span></span>

-   [<span data-ttu-id="38c2f-111">Konfigurieren eines AGPM-Servers für alle Gruppenrichtlinienadministratoren</span><span class="sxs-lookup"><span data-stu-id="38c2f-111">Configure an AGPM Server for all Group Policy administrators</span></span>](#bkmk-defaultarchiveloc)

-   [<span data-ttu-id="38c2f-112">Konfigurieren zusätzlicher AGPM-Server für alle Gruppenrichtlinienadministratoren</span><span class="sxs-lookup"><span data-stu-id="38c2f-112">Configure additional AGPM Servers for all Group Policy administrators</span></span>](#bkmk-additionalarchiveloc)

-   [<span data-ttu-id="38c2f-113">Manuelles Konfigurieren eines AGPM-Servers für Ihr Konto</span><span class="sxs-lookup"><span data-stu-id="38c2f-113">Manually configure an AGPM Server for your account</span></span>](#bkmk-manuallyconfigurearchiveloc)

### <a href="" id="bkmk-defaultarchiveloc"></a>

**<span data-ttu-id="38c2f-114">So konfigurieren Sie einen AGPM-Server für alle Gruppenrichtlinienadministratoren</span><span class="sxs-lookup"><span data-stu-id="38c2f-114">To configure an AGPM Server for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="38c2f-115">Bearbeiten Sie in der **Gruppenrichtlinien-Verwaltungskonsolen** Struktur ein GPO, das auf alle Gruppenrichtlinienadministratoren angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="38c2f-115">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="38c2f-116">(Weitere Informationen finden Sie unter [Bearbeiten eines Gruppenrichtlinienobjekts](editing-a-gpo.md).)</span><span class="sxs-lookup"><span data-stu-id="38c2f-116">(For more information, see [Editing a GPO](editing-a-gpo.md).)</span></span>

2.  <span data-ttu-id="38c2f-117">Klicken Sie im **Gruppenrichtlinienobjekt-Editor**auf **Benutzerkonfiguration**, **Administrative Vorlagen**und **Windows-Komponenten**.</span><span class="sxs-lookup"><span data-stu-id="38c2f-117">In the **Group Policy Object Editor**, click **User Configuration**, **Administrative Templates**, and **Windows Components**.</span></span>

3.  <span data-ttu-id="38c2f-118">Wenn **AGPM** nicht unter Windows- **Komponenten**aufgeführt ist:</span><span class="sxs-lookup"><span data-stu-id="38c2f-118">If **AGPM** is not listed under **Windows Components**:</span></span>

    1.  <span data-ttu-id="38c2f-119">Klicken Sie mit der rechten Maustaste auf **Administrative Vorlagen** , und klicken Sie auf **Vorlagen hinzufügen/entfernen**.</span><span class="sxs-lookup"><span data-stu-id="38c2f-119">Right-click **Administrative Templates** and click **Add/Remove Templates**.</span></span>

    2.  <span data-ttu-id="38c2f-120">Klicken Sie auf **Hinzufügen**, wählen Sie **AGPM. ADMX** oder **AGPM. adm**aus, klicken Sie auf **Öffnen**und dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="38c2f-120">Click **Add**, select **agpm.admx** or **agpm.adm**, click **Open**, and then click **Close**.</span></span>

4.  <span data-ttu-id="38c2f-121">Doppelklicken Sie unter **Windows-Komponenten**auf **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="38c2f-121">Under **Windows Components**, double-click **AGPM**.</span></span>

5.  <span data-ttu-id="38c2f-122">Doppelklicken Sie im Detailbereich auf **AGPM-Server (alle Domänen)**.</span><span class="sxs-lookup"><span data-stu-id="38c2f-122">In the details pane, double-click **AGPM Server (all domains)**.</span></span>

6.  <span data-ttu-id="38c2f-123">Aktivieren Sie im **Eigenschaftenfenster AGPM-Server (alle Domänen)** das Kontrollkästchen **aktiviert** , und geben Sie den vollqualifizierten Computernamen und-Port ein (beispielsweise Server.contoso.com:4600).</span><span class="sxs-lookup"><span data-stu-id="38c2f-123">In the **AGPM Server (all domains) Properties** window, select the **Enabled** check box, and type the fully-qualified computer name and port (for example, server.contoso.com:4600).</span></span>

7.  <span data-ttu-id="38c2f-124">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="38c2f-124">Click **OK**.</span></span> <span data-ttu-id="38c2f-125">Wenn Sie keine weiteren AGPM-Server Verbindungen konfigurieren möchten, schließen Sie den **Gruppenrichtlinienobjekt-Editor** , und stellen Sie das Gruppenrichtlinienobjekt bereit.</span><span class="sxs-lookup"><span data-stu-id="38c2f-125">Unless you want to configure additional AGPM Server connections, close the **Group Policy Object Editor** and deploy the GPO.</span></span> <span data-ttu-id="38c2f-126">(Weitere Informationen finden Sie unter [Bereitstellen eines GPO](deploy-a-gpo.md).) Wenn die Gruppenrichtlinie aktualisiert wird, ist die AGPM-Server Verbindung für alle Gruppenrichtlinienadministratoren konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="38c2f-126">(For more information, see [Deploy a GPO](deploy-a-gpo.md).) When Group Policy is updated, the AGPM Server connection is configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-additionalarchiveloc"></a>

**<span data-ttu-id="38c2f-127">So konfigurieren Sie zusätzliche AGPM-Server für alle Gruppenrichtlinienadministratoren</span><span class="sxs-lookup"><span data-stu-id="38c2f-127">To configure additional AGPM Servers for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="38c2f-128">Wenn keine AGPM-Serververbindung konfiguriert wurde, führen Sie die oben beschriebenen Schritte aus, um einen AGPM-Standardserver für alle Domänen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="38c2f-128">If no AGPM Server connection has been configured, follow the preceding procedure to configure a default AGPM Server for all domains.</span></span>

2.  <span data-ttu-id="38c2f-129">Zum Konfigurieren separater AGPM-Server für einige oder alle Domänen (Überschreiben des standardmäßigen AGPM-Servers) bearbeiten Sie in der **Gruppenrichtlinien-Verwaltungskonsolen** Struktur ein GPO, das auf alle Gruppenrichtlinienadministratoren angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="38c2f-129">To configure separate AGPM Servers for some or all domains (overriding the default AGPM Server), in the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="38c2f-130">(Weitere Informationen finden Sie unter [Bearbeiten eines Gruppenrichtlinienobjekts](editing-a-gpo.md).)</span><span class="sxs-lookup"><span data-stu-id="38c2f-130">(For more information, see [Editing a GPO](editing-a-gpo.md).)</span></span>

3.  <span data-ttu-id="38c2f-131">Doppelklicken Sie im **Gruppenrichtlinienobjekt-Editor**unter **Benutzerkonfiguration** auf **Administrative Vorlagen**, **Windows-Komponenten**und dann auf **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="38c2f-131">Under **User Configuration** in the **Group Policy Object Editor**, double-click **Administrative Templates**, **Windows Components**, and then **AGPM**.</span></span>

4.  <span data-ttu-id="38c2f-132">Doppelklicken Sie im Detailbereich auf **AGPM-Server**.</span><span class="sxs-lookup"><span data-stu-id="38c2f-132">In the details pane, double-click **AGPM Server**.</span></span>

5.  <span data-ttu-id="38c2f-133">Aktivieren Sie im Fenster **AGPM-Server Eigenschaften** das Kontrollkästchen **aktiviert** , und klicken Sie auf **anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="38c2f-133">In the **AGPM Server Properties** window, select the **Enabled** check box, and click **Show**.</span></span>

6.  <span data-ttu-id="38c2f-134">Im Fenster " **Inhalte anzeigen** ":</span><span class="sxs-lookup"><span data-stu-id="38c2f-134">In the **Show Contents** window:</span></span>

    1.  <span data-ttu-id="38c2f-135">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="38c2f-135">Click **Add**.</span></span>

    2.  <span data-ttu-id="38c2f-136">Geben Sie unter **Wertname**den Namen der Domäne ein (beispielsweise Server1.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="38c2f-136">For **Value Name**, type the domain name (for example, server1.contoso.com).</span></span>

    3.  <span data-ttu-id="38c2f-137">Geben Sie als **Wert**den Namen und den Port des AGPM-Servers ein, der für diese Domäne verwendet werden soll (beispielsweise Server2.contoso.com:4600), und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="38c2f-137">For **Value**, type the AGPM Server name and port to use for this domain (for example, server2.contoso.com:4600), and then click **OK**.</span></span> <span data-ttu-id="38c2f-138">(Standardmäßig überwacht der AGPM-Dienst Port 4600.</span><span class="sxs-lookup"><span data-stu-id="38c2f-138">(By default, the AGPM Service listens on port 4600.</span></span> <span data-ttu-id="38c2f-139">Informationen zum Verwenden eines anderen Ports finden Sie unter [Ändern des Ports, auf den der AGPM-Dienst lauscht](modify-the-port-on-which-the-agpm-service-listens.md).)</span><span class="sxs-lookup"><span data-stu-id="38c2f-139">To use a different port, see [Modify the Port on Which the AGPM Service Listens](modify-the-port-on-which-the-agpm-service-listens.md).)</span></span>

    4.  <span data-ttu-id="38c2f-140">Wiederholen Sie diese Schritte für jede Domäne, die nicht den AGPM-Standard Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="38c2f-140">Repeat for each domain not using the default AGPM Server.</span></span>

7.  <span data-ttu-id="38c2f-141">Klicken Sie auf **OK** , um die Fenster **Inhalte anzeigen** und **AGPM-Server Eigenschaften** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="38c2f-141">Click **OK** to close the **Show Contents** and **AGPM Server Properties** windows.</span></span>

8.  <span data-ttu-id="38c2f-142">Schließen Sie den **Gruppenrichtlinienobjekt-Editor**.</span><span class="sxs-lookup"><span data-stu-id="38c2f-142">Close the **Group Policy Object Editor**.</span></span> <span data-ttu-id="38c2f-143">(Weitere Informationen finden Sie unter [Bereitstellen eines GPO](deploy-a-gpo.md).) Wenn die Gruppenrichtlinie aktualisiert wird, werden die neuen AGPM-Server Verbindungen für alle Gruppenrichtlinienadministratoren konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="38c2f-143">(For more information, see [Deploy a GPO](deploy-a-gpo.md).) When Group Policy is updated, the new AGPM Server connections are configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-manuallyconfigurearchiveloc"></a>

<span data-ttu-id="38c2f-144">Wenn Sie die AGPM-Server Verbindung zentral konfiguriert haben, steht die Option manuell für alle Gruppenrichtlinienadministratoren nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="38c2f-144">If you have centrally configured the AGPM Server connection, the option to manually it is unavailable for all Group Policy administrators.</span></span>

**<span data-ttu-id="38c2f-145">So konfigurieren Sie den AGPM-Server für die Anzeige für Ihr Konto manuell</span><span class="sxs-lookup"><span data-stu-id="38c2f-145">To manually configure the AGPM Server to display for your account</span></span>**

1.  <span data-ttu-id="38c2f-146">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="38c2f-146">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="38c2f-147">Klicken Sie im Detailbereich auf die Registerkarte **AGPM-Server** .</span><span class="sxs-lookup"><span data-stu-id="38c2f-147">In the details pane, click the **AGPM Server** tab.</span></span>

3.  <span data-ttu-id="38c2f-148">Geben Sie den vollqualifizierten Computernamen für den AGPM-Server ein, der das Archiv verwaltet, das für diese Domäne verwendet wird (beispielsweise Server.contoso.com), und den Port, der vom AGPM-Dienst überwacht wird (standardmäßig Port 4600).</span><span class="sxs-lookup"><span data-stu-id="38c2f-148">Enter the fully-qualified computer name for the AGPM Server that manages the archive used for this domain (for example, server.contoso.com) and the port on which the AGPM Service listens (by default, port 4600).</span></span>

4.  <span data-ttu-id="38c2f-149">Klicken Sie auf über **nehmen**, und klicken Sie dann zum bestätigen auf **Ja** .</span><span class="sxs-lookup"><span data-stu-id="38c2f-149">Click **Apply**, then click **Yes** to confirm.</span></span>

### <span data-ttu-id="38c2f-150">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="38c2f-150">Additional considerations</span></span>

-   <span data-ttu-id="38c2f-151">Sie müssen in der Lage sein, ein GPO zu bearbeiten und bereitzustellen, um die Verfahren zum zentralen Konfigurieren von AGPM-Server Verbindungen für alle Gruppenrichtlinienadministratoren durchführen zu können.</span><span class="sxs-lookup"><span data-stu-id="38c2f-151">You must be able to edit and deploy a GPO to perform the procedures for centrally configuring AGPM Server connections for all Group Policy administrators.</span></span> <span data-ttu-id="38c2f-152">Weitere Informationen finden Sie unter [Bearbeiten eines GPO](editing-a-gpo.md) und [Bereitstellen eines Gruppenrichtlinienobjekts](deploy-a-gpo.md) .</span><span class="sxs-lookup"><span data-stu-id="38c2f-152">See [Editing a GPO](editing-a-gpo.md) and [Deploy a GPO](deploy-a-gpo.md) for additional detail.</span></span>

-   <span data-ttu-id="38c2f-153">Der ausgewählte AGPM-Server bestimmt, welche GPOs auf der Registerkarte **Inhalt** angezeigt werden und an welchem Speicherort die Einstellungen für die **Domänen Delegierungs** Einstellungen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="38c2f-153">The AGPM Server selected determines which GPOs are displayed on the **Contents** tab and to what location the **Domain Delegation** tab settings are applied.</span></span> <span data-ttu-id="38c2f-154">Wenn Sie nicht zentral über die administrative Vorlage verwaltet werden, muss jeder Gruppenrichtlinienadministrator diese Einstellung so konfigurieren, dass er auf den AGPM-Server für die Domäne verweist.</span><span class="sxs-lookup"><span data-stu-id="38c2f-154">If not centrally managed through the Administrative Template, each Group Policy administrator must configure this setting to point to the AGPM Server for the domain.</span></span>

-   <span data-ttu-id="38c2f-155">Die Mitgliedschaft in der Gruppe Richtlinien-Ersteller-Besitzer sollte eingeschränkt sein, damit Sie nicht dazu verwendet wird, die Verwaltung des Zugriffs auf GPOs durch AGPM zu umgehen.</span><span class="sxs-lookup"><span data-stu-id="38c2f-155">Membership in the Group Policy Creator Owners group should be restricted so that it is not used to circumvent the management of access to GPOs by AGPM.</span></span> <span data-ttu-id="38c2f-156">(Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gruppenrichtlinienobjekte** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, klicken Sie auf **Delegierung**, und konfigurieren Sie dann die Einstellungen, um die Anforderungen Ihrer Organisation zu erfüllen.)</span><span class="sxs-lookup"><span data-stu-id="38c2f-156">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="38c2f-157">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="38c2f-157">Additional references</span></span>

-   [<span data-ttu-id="38c2f-158">Durchführen von AGPM-Administratoraufgaben</span><span class="sxs-lookup"><span data-stu-id="38c2f-158">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





