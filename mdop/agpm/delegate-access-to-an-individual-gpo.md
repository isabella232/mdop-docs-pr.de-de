---
title: Delegieren des Zugriffs auf eine einzelne Gruppenrichtlinienobjekte
description: Delegieren des Zugriffs auf eine einzelne Gruppenrichtlinienobjekte
author: dansimp
ms.assetid: b2a7d550-14bf-4b41-b6e4-2cc091eedd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e5d2ae8c6ef52eae39feb67b9df42e84f523300
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807624"
---
# <span data-ttu-id="13301-103">Delegieren des Zugriffs auf eine einzelne Gruppenrichtlinienobjekte</span><span class="sxs-lookup"><span data-stu-id="13301-103">Delegate Access to an Individual GPO</span></span>


<span data-ttu-id="13301-104">Als AGPM-Administrator (Vollzugriff) können Sie die Verwaltung eines kontrollierten Gruppenrichtlinienobjekts (GPO) delegieren, damit ausgewählte Gruppen und Bearbeiter es bearbeiten können, Prüfer Sie überprüfen können, und Genehmiger können es genehmigen.</span><span class="sxs-lookup"><span data-stu-id="13301-104">As an AGPM Administrator (Full Control), you can delegate the management of a controlled Group Policy object (GPO), so selected groups and Editors can edit it, Reviewers can review it, and Approvers can approve it.</span></span>

<span data-ttu-id="13301-105">Ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff), dem Benutzerkonto der genehmigenden Person, die das Gruppenrichtlinienobjekt erstellt hat, oder ein Benutzerkonto mit den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung ist erforderlich, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="13301-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="13301-106">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="13301-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="13301-107">So delegieren Sie die Verwaltung eines kontrollierten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="13301-107">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="13301-108">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="13301-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="13301-109">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um gesteuerte GPOs anzuzeigen, und klicken Sie dann auf das zu delegierende Gruppenrichtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="13301-109">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate.</span></span>

3.  <span data-ttu-id="13301-110">Klicken Sie auf die Schaltfläche **Hinzufügen** , wählen Sie die Benutzer oder Gruppen aus, denen Sie Zugriff gewähren möchten, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="13301-110">Click the **Add** button, select the users or groups to be permitted access, and then click **OK**.</span></span>

4.  <span data-ttu-id="13301-111">Um die Berechtigungen für die einzelnen Benutzer oder Gruppen anzupassen, klicken Sie auf der Registerkarte **Inhalt** auf die Schaltfläche **erweitert** , und überprüfen Sie die Rollen Berechtigungen auf zulassen oder ablehnen.</span><span class="sxs-lookup"><span data-stu-id="13301-111">To customize the permissions for each user or group, click the **Advanced** button on the **Contents** tab and check role permissions to allow or deny.</span></span> <span data-ttu-id="13301-112">(Wenn Sie eine genauere Steuerung haben, klicken Sie im Dialogfeld **Berechtigungen** auf **erweitert** .)</span><span class="sxs-lookup"><span data-stu-id="13301-112">(For more detailed control, click **Advanced** in the **Permissions** dialog box.)</span></span>

5.  <span data-ttu-id="13301-113">Klicken Sie auf über **nehmen**, und klicken Sie dann im Dialogfeld **Berechtigungen** auf **OK** .</span><span class="sxs-lookup"><span data-stu-id="13301-113">Click **Apply**, and then click **OK** in the **Permissions** dialog box.</span></span>

### <span data-ttu-id="13301-114">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="13301-114">Additional considerations</span></span>

-   <span data-ttu-id="13301-115">Standardmäßig müssen Sie die genehmigende Person sein, die das Gruppenrichtlinienobjekt erstellt oder kontrolliert hat, oder einen AGPM-Administrator (Vollzugriff), um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="13301-115">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="13301-116">Insbesondere müssen Sie über die Berechtigung **Listeninhalt** für die Domäne und die Berechtigung zum **Ändern der Sicherheit** für das Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="13301-116">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

-   <span data-ttu-id="13301-117">Wenn Sie den Lesezugriff an Gruppenrichtlinienadministratoren delegieren möchten, die AGPM verwenden, müssen Sie Ihnen **Listeninhalte** und Berechtigungen zum **Lesen von Einstellungen** erteilen.</span><span class="sxs-lookup"><span data-stu-id="13301-117">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="13301-118">Dadurch können Sie GPOs auf der Registerkarte **Inhalt** von AGPM anzeigen.</span><span class="sxs-lookup"><span data-stu-id="13301-118">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="13301-119">Legen Sie die Berechtigung für **dieses Objekt und verschachtelte Objekte**auf.</span><span class="sxs-lookup"><span data-stu-id="13301-119">Set the permission to apply to **This object and nested objects**.</span></span> <span data-ttu-id="13301-120">Andere Berechtigungen müssen explizit delegiert werden.</span><span class="sxs-lookup"><span data-stu-id="13301-120">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="13301-121">Redakteure müssen über die Berechtigung " **Lesen** " für die bereitgestellte Kopie eines Gruppenrichtlinienobjekts verfügen, um die Gruppenrichtlinien-Software Installation vollständig nutzen zu können.</span><span class="sxs-lookup"><span data-stu-id="13301-121">Editors must have **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="13301-122">Die Mitgliedschaft in der Gruppe Richtlinien Ersteller-Besitzer sollte eingeschränkt sein, damit Sie nicht zur Umgehung der AGPM-Verwaltung des Zugriffs auf GPOs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="13301-122">Membership in the Group Policy Creator Owners group should be restricted so that it is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="13301-123">(Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gruppenrichtlinienobjekte** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, klicken Sie auf **Delegierung**, und konfigurieren Sie dann die Einstellungen, um die Anforderungen Ihrer Organisation zu erfüllen.)</span><span class="sxs-lookup"><span data-stu-id="13301-123">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="13301-124">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="13301-124">Additional references</span></span>

-   [<span data-ttu-id="13301-125">Durchführen von AGPM-Administratoraufgaben</span><span class="sxs-lookup"><span data-stu-id="13301-125">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





