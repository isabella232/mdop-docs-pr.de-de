---
title: Konfigurieren von E-Mail-Benachrichtigungen
description: Konfigurieren von E-Mail-Benachrichtigungen
author: dansimp
ms.assetid: 6e152de0-4376-4963-8d1a-3e7f5866d30f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 46e8d00c2446a0185de30bbd1f39a7e3eaf90080
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807723"
---
# <span data-ttu-id="51b8d-103">Konfigurieren von E-Mail-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="51b8d-103">Configure E-Mail Notification</span></span>


<span data-ttu-id="51b8d-104">Wenn ein Editor oder ein Bearbeiter versucht, ein Gruppenrichtlinienobjekt (Group Policy Object, GPO) zu erstellen, bereitzustellen oder zu löschen, wird eine Anforderung für diese Aktion an eine bestimmte e-Mail-Adresse oder Adressen gesendet, sodass eine genehmigende Person die Anforderung auswerten und implementieren oder ablehnen kann.</span><span class="sxs-lookup"><span data-stu-id="51b8d-104">When an Editor or a Reviewer attempts to create, deploy, or delete a Group Policy object (GPO), a request for this action is sent to a designated e-mail address or addresses so that an Approver can evaluate the request and implement or deny it.</span></span> <span data-ttu-id="51b8d-105">Sie bestimmen die e-Mail-Adresse oder Adressen, an die Benachrichtigungen gesendet werden, sowie den Alias, aus dem Benachrichtigungen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="51b8d-105">You determine the e-mail address or addresses to which notifications are sent, as well as the alias from which notifications are sent.</span></span>

<span data-ttu-id="51b8d-106">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="51b8d-106">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="51b8d-107">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="51b8d-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="51b8d-108">So konfigurieren Sie die e-Mail-Benachrichtigung für AGPM</span><span class="sxs-lookup"><span data-stu-id="51b8d-108">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="51b8d-109">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="51b8d-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="51b8d-110">Klicken Sie im Detailbereich auf die Registerkarte **Domänendelegierung** .</span><span class="sxs-lookup"><span data-stu-id="51b8d-110">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="51b8d-111">Geben Sie im Feld **von** den e-Mail-Alias für AGPM ein, aus dem Benachrichtigungen gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="51b8d-111">In the **From** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="51b8d-112">Geben Sie im Feld **an** eine durch trennzeichengetrennte Liste der e-Mail-Adressen von genehmigenden Personen ein, die Genehmigungsanforderungen erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="51b8d-112">In the **To** field, type a comma-delimited list of e-mail addresses of Approvers who should receive requests for approval.</span></span>

5.  <span data-ttu-id="51b8d-113">Geben Sie im Feld **SMTP-Server** einen gültigen SMTP-e-Mail-Server ein.</span><span class="sxs-lookup"><span data-stu-id="51b8d-113">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="51b8d-114">Geben Sie in den Feldern **Benutzername** und **Kennwort** die Anmeldeinformationen eines Benutzers mit Zugriff auf den SMTP-Dienst ein.</span><span class="sxs-lookup"><span data-stu-id="51b8d-114">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span>

7.  <span data-ttu-id="51b8d-115">Klicken Sie auf **Übernehmen**.</span><span class="sxs-lookup"><span data-stu-id="51b8d-115">Click **Apply**.</span></span>

### <span data-ttu-id="51b8d-116">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="51b8d-116">Additional considerations</span></span>

-   <span data-ttu-id="51b8d-117">Standardmäßig müssen Sie ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="51b8d-117">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="51b8d-118">Insbesondere müssen Sie über die Berechtigungen **Listeninhalt** und **Änderungsoptionen** für die Domäne verfügen.</span><span class="sxs-lookup"><span data-stu-id="51b8d-118">Specifically, you must have **List Contents** and **Modify Options** permissions for the domain.</span></span>

-   <span data-ttu-id="51b8d-119">E-Mail-Benachrichtigung für AGPM ist eine Einstellung auf Domänenebene.</span><span class="sxs-lookup"><span data-stu-id="51b8d-119">E-mail notification for AGPM is a domain-level setting.</span></span> <span data-ttu-id="51b8d-120">Sie können unterschiedliche e-Mail-Adressen oder AGPM-e-Mail-Aliase auf den Registerkarten der Domänen **Delegierung** jeder Domäne angeben oder dieselben e-Mail-Adressen in ihrer gesamten Umgebung verwenden.</span><span class="sxs-lookup"><span data-stu-id="51b8d-120">You can provide different Approver e-mail addresses or AGPM e-mail aliases on each domain's **Domain Delegation** tab, or use the same e-mail addresses throughout your environment.</span></span>

### <span data-ttu-id="51b8d-121">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="51b8d-121">Additional references</span></span>

-   [<span data-ttu-id="51b8d-122">Durchführen von AGPM-Administratoraufgaben</span><span class="sxs-lookup"><span data-stu-id="51b8d-122">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





