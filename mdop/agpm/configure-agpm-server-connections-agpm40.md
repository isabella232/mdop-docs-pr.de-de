---
title: Konfigurieren von AGPM-Server-Verbindungen
description: Konfigurieren von AGPM-Server-Verbindungen
author: dansimp
ms.assetid: bbbb15e8-35e7-403c-b695-7a6ebeb87839
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b6b065b9855c6edf44456026baa32e8d9a4674f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807760"
---
# <span data-ttu-id="8359d-103">Konfigurieren von AGPM-Server-Verbindungen</span><span class="sxs-lookup"><span data-stu-id="8359d-103">Configure AGPM Server Connections</span></span>


<span data-ttu-id="8359d-104">Alle Versionen der einzelnen gesteuerten Gruppenrichtlinienobjekte (GPO) werden in einem zentralen Archiv gespeichert, sodass Gruppenrichtlinienadministratoren Gruppenrichtlinienobjekte offline anzeigen und ändern können, ohne dass sich dies unmittelbar auf die bereitgestellte Version jedes GPO auswirkt.</span><span class="sxs-lookup"><span data-stu-id="8359d-104">All versions of each controlled Group Policy Object (GPO) are stored in a central archive so that Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="8359d-105">Ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff), das Benutzerkonto der genehmigenden Person, die das in diesen Verfahren verwendete Gruppenrichtlinienobjekt erstellt hat, oder ein Benutzerkonto mit den erforderlichen Berechtigungen in Advanced Group Policy Management (AGPM) ist erforderlich, um diese Verfahren zum zentralen Konfigurieren von Archivierungsspeicher Orten für alle Gruppenrichtlinienadministratoren durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="8359d-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO used in these procedures, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete these procedures for centrally configuring archive locations for all Group Policy administrators.</span></span> <span data-ttu-id="8359d-106">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="8359d-106">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="8359d-107">Konfigurieren von AGPM-Server Verbindungen</span><span class="sxs-lookup"><span data-stu-id="8359d-107">Configuring AGPM Server connections</span></span>


<span data-ttu-id="8359d-108">Als AGPM-Administrator können Sie sicherstellen, dass alle Gruppenrichtlinienadministratoren eine Verbindung mit dem gleichen AGPM-Server herstellen, indem Sie die zugeordnete Einstellung zentral konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8359d-108">As an AGPM Administrator, you can ensure that all Group Policy administrators connect to the same AGPM Server by centrally configuring the associated setting.</span></span> <span data-ttu-id="8359d-109">Wenn für Ihre Umgebung separate AGPM-Server für einige oder alle Domänen erforderlich sind, konfigurieren Sie diese zusätzlichen AGPM-Server als Ausnahmen von der Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="8359d-109">If your environment requires separate AGPM Servers for some or all domains, configure those additional AGPM Servers as exceptions to the default.</span></span> <span data-ttu-id="8359d-110">Wenn Sie keine AGPM-Serververbindungen zentral konfigurieren, muss jeder Gruppenrichtlinienadministrator den AGPM-Server manuell für die Anzeige für jede Domäne konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8359d-110">If you do not centrally configure AGPM Server connections, each Group Policy administrator must manually configure the AGPM Server to be displayed for each domain.</span></span>

-   [<span data-ttu-id="8359d-111">Konfigurieren einer AGPM-Server Verbindung für alle Gruppenrichtlinienadministratoren</span><span class="sxs-lookup"><span data-stu-id="8359d-111">Configure an AGPM Server connection for all Group Policy administrators</span></span>](#bkmk-defaultarchiveloc)

-   [<span data-ttu-id="8359d-112">Konfigurieren zusätzlicher AGPM-Server Verbindungen für alle Gruppenrichtlinienadministratoren</span><span class="sxs-lookup"><span data-stu-id="8359d-112">Configure additional AGPM Server connections for all Group Policy administrators</span></span>](#bkmk-additionalarchiveloc)

-   [<span data-ttu-id="8359d-113">Manuelles Konfigurieren einer AGPM-Server Verbindung für Ihr Konto</span><span class="sxs-lookup"><span data-stu-id="8359d-113">Manually configure an AGPM Server connection for your account</span></span>](#bkmk-manuallyconfigurearchiveloc)

### <a href="" id="bkmk-defaultarchiveloc"></a>

**<span data-ttu-id="8359d-114">So konfigurieren Sie eine AGPM-Server Verbindung für alle Gruppenrichtlinienadministratoren</span><span class="sxs-lookup"><span data-stu-id="8359d-114">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="8359d-115">Bearbeiten Sie in der **Gruppenrichtlinien-Verwaltungskonsolen** Struktur ein GPO, das auf alle Gruppenrichtlinienadministratoren angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8359d-115">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="8359d-116">(Weitere Informationen finden Sie unter [Bearbeiten eines Gruppenrichtlinienobjekts](editing-a-gpo-agpm40.md).)</span><span class="sxs-lookup"><span data-stu-id="8359d-116">(For more information, see [Editing a GPO](editing-a-gpo-agpm40.md).)</span></span>

2.  <span data-ttu-id="8359d-117">Klicken Sie im Fenster **Gruppenrichtlinien-Verwaltungs-Editor** auf **Benutzerkonfiguration**, **Richtlinien**, **Administrative Vorlagen**, **Windows-Komponenten**und **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="8359d-117">In the **Group Policy Management Editor** window, click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

3.  <span data-ttu-id="8359d-118">Doppelklicken Sie im Detailbereich auf **AGPM: standardmäßiger AGPM-Server (alle Domänen) angeben**.</span><span class="sxs-lookup"><span data-stu-id="8359d-118">In the details pane, double-click **AGPM: Specify default AGPM Server (all domains)**.</span></span>

4.  <span data-ttu-id="8359d-119">Aktivieren Sie im **Eigenschaften** Fenster das Kontrollkästchen **aktiviert** , und geben Sie den vollqualifizierten Namen und Port des Computers ein (beispielsweise Server.contoso.com:4600).</span><span class="sxs-lookup"><span data-stu-id="8359d-119">In the **Properties** window, select the **Enabled** check box, and type the fully-qualified computer name and port (for example, server.contoso.com:4600).</span></span>

5.  <span data-ttu-id="8359d-120">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8359d-120">Click **OK**.</span></span> <span data-ttu-id="8359d-121">Wenn Sie keine weiteren AGPM-Server Verbindungen konfigurieren möchten, schließen Sie das **Gruppenrichtlinien-Verwaltungs-Editor** -Fenster, und stellen Sie das Gruppenrichtlinienobjekt bereit.</span><span class="sxs-lookup"><span data-stu-id="8359d-121">Unless you want to configure additional AGPM Server connections, close the **Group Policy Management Editor** window and deploy the GPO.</span></span> <span data-ttu-id="8359d-122">(Weitere Informationen finden Sie unter [Bereitstellen eines GPO](deploy-a-gpo-agpm40.md).) Wenn die Gruppenrichtlinie aktualisiert wird, ist die AGPM-Server Verbindung für alle Gruppenrichtlinienadministratoren konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="8359d-122">(For more information, see [Deploy a GPO](deploy-a-gpo-agpm40.md).) When Group Policy is updated, the AGPM Server connection is configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-additionalarchiveloc"></a>

**<span data-ttu-id="8359d-123">So konfigurieren Sie zusätzliche AGPM-Server Verbindungen für alle Gruppenrichtlinienadministratoren</span><span class="sxs-lookup"><span data-stu-id="8359d-123">To configure additional AGPM Server connections for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="8359d-124">Wenn keine AGPM-Serververbindung konfiguriert wurde, führen Sie die oben beschriebenen Schritte aus, um einen AGPM-Standardserver für alle Domänen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8359d-124">If no AGPM Server connection has been configured, follow the preceding procedure to configure a default AGPM Server for all domains.</span></span>

2.  <span data-ttu-id="8359d-125">Zum Konfigurieren separater AGPM-Server für einige oder alle Domänen (Überschreiben des standardmäßigen AGPM-Servers) bearbeiten Sie in der **Gruppenrichtlinien-Verwaltungskonsolen** Struktur ein GPO, das auf alle Gruppenrichtlinienadministratoren angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8359d-125">To configure separate AGPM Servers for some or all domains (overriding the default AGPM Server), in the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="8359d-126">(Weitere Informationen finden Sie unter [Bearbeiten eines Gruppenrichtlinienobjekts](editing-a-gpo-agpm40.md).)</span><span class="sxs-lookup"><span data-stu-id="8359d-126">(For more information, see [Editing a GPO](editing-a-gpo-agpm40.md).)</span></span>

3.  <span data-ttu-id="8359d-127">Klicken Sie im Fenster **Gruppenrichtlinien-Verwaltungs-Editor** auf **Benutzerkonfiguration**, **Richtlinien**, **Administrative Vorlagen**, **Windows-Komponenten**und dann auf **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="8359d-127">In the **Group Policy Management Editor** window, click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and then **AGPM**.</span></span>

4.  <span data-ttu-id="8359d-128">Doppelklicken Sie im Detailbereich auf **AGPM: AGPM-Server angeben**.</span><span class="sxs-lookup"><span data-stu-id="8359d-128">In the details pane, double-click **AGPM: Specify AGPM Servers**.</span></span>

5.  <span data-ttu-id="8359d-129">Aktivieren Sie im **Eigenschaften** Fenster das Kontrollkästchen **aktiviert** , und klicken Sie auf **anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="8359d-129">In the **Properties** window, select the **Enabled** check box, and click **Show**.</span></span>

6.  <span data-ttu-id="8359d-130">Im Fenster " **Inhalte anzeigen** ":</span><span class="sxs-lookup"><span data-stu-id="8359d-130">In the **Show Contents** window:</span></span>

    1.  <span data-ttu-id="8359d-131">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="8359d-131">Click **Add**.</span></span>

    2.  <span data-ttu-id="8359d-132">Geben Sie unter **Wertname**den Namen der Domäne ein (beispielsweise Server1.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="8359d-132">For **Value Name**, type the domain name (for example, server1.contoso.com).</span></span>

    3.  <span data-ttu-id="8359d-133">Geben Sie als **Wert**den Namen und den Port des AGPM-Servers ein, der für diese Domäne verwendet werden soll (beispielsweise Server2.contoso.com:4600), und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8359d-133">For **Value**, type the AGPM Server name and port to use for this domain (for example, server2.contoso.com:4600), and then click **OK**.</span></span> <span data-ttu-id="8359d-134">(Standardmäßig überwacht der AGPM-Dienst Port 4600.</span><span class="sxs-lookup"><span data-stu-id="8359d-134">(By default, the AGPM Service listens on port 4600.</span></span> <span data-ttu-id="8359d-135">Informationen zum Verwenden eines anderen Ports finden Sie unter [Ändern des AGPM-Diensts](modify-the-agpm-service-agpm40.md).)</span><span class="sxs-lookup"><span data-stu-id="8359d-135">To use a different port, see [Modify the AGPM Service](modify-the-agpm-service-agpm40.md).)</span></span>

    4.  <span data-ttu-id="8359d-136">Wiederholen Sie diese Schritte für jede Domäne, die nicht den AGPM-Standard Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="8359d-136">Repeat for each domain not using the default AGPM Server.</span></span>

7.  <span data-ttu-id="8359d-137">Klicken Sie auf **OK** , um die Fenster Inhalt und **Eigenschaften** **anzeigen** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="8359d-137">Click **OK** to close the **Show Contents** and **Properties** windows.</span></span>

8.  <span data-ttu-id="8359d-138">Schließen Sie das Fenster **Gruppenrichtlinien-Verwaltungs-Editor** .</span><span class="sxs-lookup"><span data-stu-id="8359d-138">Close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="8359d-139">(Weitere Informationen finden Sie unter [Bereitstellen eines GPO](deploy-a-gpo-agpm40.md).) Wenn die Gruppenrichtlinie aktualisiert wird, werden die neuen AGPM-Server Verbindungen für alle Gruppenrichtlinienadministratoren konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="8359d-139">(For more information, see [Deploy a GPO](deploy-a-gpo-agpm40.md).) When Group Policy is updated, the new AGPM Server connections are configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-manuallyconfigurearchiveloc"></a>

<span data-ttu-id="8359d-140">Wenn Sie die AGPM-Server Verbindung zentral konfiguriert haben, steht die Option zum manuellen Konfigurieren für alle Gruppenrichtlinienadministratoren nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="8359d-140">If you have centrally configured the AGPM Server connection, the option to manually configure it is unavailable for all Group Policy administrators.</span></span>

**<span data-ttu-id="8359d-141">So konfigurieren Sie den AGPM-Server, der für Ihr Konto angezeigt werden soll, manuell</span><span class="sxs-lookup"><span data-stu-id="8359d-141">To manually configure which AGPM Server to display for your account</span></span>**

1.  <span data-ttu-id="8359d-142">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="8359d-142">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8359d-143">Klicken Sie im Detailbereich auf die Registerkarte **AGPM-Server** .</span><span class="sxs-lookup"><span data-stu-id="8359d-143">In the details pane, click the **AGPM Server** tab.</span></span>

3.  <span data-ttu-id="8359d-144">Geben Sie den vollqualifizierten Computernamen für den AGPM-Server ein, der das Archiv verwaltet, das für diese Domäne verwendet wird (beispielsweise Server.contoso.com), und den Port, der vom AGPM-Dienst überwacht wird (standardmäßig Port 4600).</span><span class="sxs-lookup"><span data-stu-id="8359d-144">Enter the fully-qualified computer name for the AGPM Server that manages the archive used for this domain (for example, server.contoso.com) and the port on which the AGPM Service listens (by default, port 4600).</span></span>

4.  <span data-ttu-id="8359d-145">Klicken Sie auf über **nehmen**, und klicken Sie dann zum bestätigen auf **Ja** .</span><span class="sxs-lookup"><span data-stu-id="8359d-145">Click **Apply**, then click **Yes** to confirm.</span></span>

### <span data-ttu-id="8359d-146">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="8359d-146">Additional considerations</span></span>

-   <span data-ttu-id="8359d-147">Sie müssen in der Lage sein, ein GPO zu bearbeiten und bereitzustellen, um die Verfahren zum zentralen Konfigurieren von AGPM-Server Verbindungen für alle Gruppenrichtlinienadministratoren durchführen zu können.</span><span class="sxs-lookup"><span data-stu-id="8359d-147">You must be able to edit and deploy a GPO to perform the procedures for centrally configuring AGPM Server connections for all Group Policy administrators.</span></span> <span data-ttu-id="8359d-148">Weitere Informationen finden Sie unter [Bearbeiten eines GPO](editing-a-gpo-agpm40.md) und [Bereitstellen eines Gruppenrichtlinienobjekts](deploy-a-gpo-agpm40.md) .</span><span class="sxs-lookup"><span data-stu-id="8359d-148">See [Editing a GPO](editing-a-gpo-agpm40.md) and [Deploy a GPO](deploy-a-gpo-agpm40.md) for additional detail.</span></span>

-   <span data-ttu-id="8359d-149">Der ausgewählte AGPM-Server legt fest, welche GPOs auf der Registerkarte **Inhalt** angezeigt werden und an welchem Speicherort die Einstellungen für die **Domänen Delegierungs** Einstellungen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="8359d-149">The selected AGPM Server determines which GPOs are displayed on the **Contents** tab and to what location the **Domain Delegation** tab settings are applied.</span></span> <span data-ttu-id="8359d-150">Wenn Sie nicht zentral über die administrative Vorlage verwaltet werden, muss jeder Gruppenrichtlinienadministrator diese Einstellung so konfigurieren, dass er auf den AGPM-Server für die Domäne verweist.</span><span class="sxs-lookup"><span data-stu-id="8359d-150">If not centrally managed through the Administrative template, each Group Policy administrator must configure this setting to point to the AGPM Server for the domain.</span></span>

-   <span data-ttu-id="8359d-151">Die Mitgliedschaft in der Gruppe Richtlinien Ersteller-Besitzer sollte eingeschränkt sein, soit wird nicht verwendet, um die AGPM-Verwaltung des Zugriffs auf GPOs zu umgehen.</span><span class="sxs-lookup"><span data-stu-id="8359d-151">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="8359d-152">(Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gruppenrichtlinienobjekte** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, klicken Sie auf **Delegierung**, und konfigurieren Sie dann die Einstellungen, um die Anforderungen Ihrer Organisation zu erfüllen.)</span><span class="sxs-lookup"><span data-stu-id="8359d-152">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="8359d-153">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="8359d-153">Additional references</span></span>

-   [<span data-ttu-id="8359d-154">Konfigurieren von Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="8359d-154">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management-agpm40.md)

 

 





