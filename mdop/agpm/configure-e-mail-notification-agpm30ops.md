---
title: Konfigurieren von E-Mail-Benachrichtigungen
description: Konfigurieren von E-Mail-Benachrichtigungen
author: dansimp
ms.assetid: b32ce395-d1b9-4c5b-b765-97cdbf455f9e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0204f2bd3430fa47b785d13a73b107e311990b82
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807732"
---
# <span data-ttu-id="3f855-103">Konfigurieren von E-Mail-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="3f855-103">Configure E-Mail Notification</span></span>


<span data-ttu-id="3f855-104">Wenn ein Editor oder ein Bearbeiter versucht, ein Gruppenrichtlinienobjekt (Group Policy Object, GPO) zu erstellen, bereitzustellen oder zu löschen, wird eine Anforderung für diese Aktion an eine bestimmte e-Mail-Adresse oder Adressen gesendet, sodass eine genehmigende Person die Anforderung auswerten und implementieren oder ablehnen kann.</span><span class="sxs-lookup"><span data-stu-id="3f855-104">When an Editor or a Reviewer attempts to create, deploy, or delete a Group Policy Object (GPO), a request for this action is sent to a designated e-mail address or addresses so that an Approver can evaluate the request and implement or deny it.</span></span> <span data-ttu-id="3f855-105">Sie bestimmen die e-Mail-Adresse oder Adressen, an die Benachrichtigungen gesendet werden, sowie den Alias, aus dem Benachrichtigungen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f855-105">You determine the e-mail address or addresses to which notifications are sent, as well as the alias from which notifications are sent.</span></span>

<span data-ttu-id="3f855-106">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in Advanced Group Policy Management (AGPM) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3f855-106">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="3f855-107">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="3f855-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="3f855-108">So konfigurieren Sie die e-Mail-Benachrichtigung für AGPM</span><span class="sxs-lookup"><span data-stu-id="3f855-108">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="3f855-109">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="3f855-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="3f855-110">Klicken Sie im Detailbereich auf die Registerkarte **Domänendelegierung** .</span><span class="sxs-lookup"><span data-stu-id="3f855-110">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="3f855-111">Geben Sie im Feld **von e-Mail-Adresse** den e-Mail-Alias für AGPM ein, aus dem Benachrichtigungen gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3f855-111">In the **From e-mail address** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="3f855-112">Geben Sie im Feld **an e-Mail-Adresse** eine durch trennzeichengetrennte Liste der e-Mail-Adressen von genehmigenden Personen ein, die Genehmigungsanforderungen erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="3f855-112">In the **To e-mail address** field, type a comma-delimited list of e-mail addresses of Approvers who should receive requests for approval.</span></span>

5.  <span data-ttu-id="3f855-113">Geben Sie im Feld **SMTP-Server** einen gültigen SMTP-e-Mail-Server ein.</span><span class="sxs-lookup"><span data-stu-id="3f855-113">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="3f855-114">Geben Sie in den Feldern **Benutzername** und **Kennwort** die Anmeldeinformationen eines Benutzers mit Zugriff auf den SMTP-Dienst ein.</span><span class="sxs-lookup"><span data-stu-id="3f855-114">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span>

7.  <span data-ttu-id="3f855-115">Klicken Sie auf **Übernehmen**.</span><span class="sxs-lookup"><span data-stu-id="3f855-115">Click **Apply**.</span></span>

### <span data-ttu-id="3f855-116">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="3f855-116">Additional considerations</span></span>

-   <span data-ttu-id="3f855-117">Standardmäßig müssen Sie ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="3f855-117">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="3f855-118">Insbesondere müssen Sie über die Berechtigungen **Listeninhalt** und **Änderungsoptionen** für die Domäne verfügen.</span><span class="sxs-lookup"><span data-stu-id="3f855-118">Specifically, you must have **List Contents** and **Modify Options** permissions for the domain.</span></span>

-   <span data-ttu-id="3f855-119">E-Mail-Benachrichtigung für AGPM ist eine Einstellung auf Domänenebene.</span><span class="sxs-lookup"><span data-stu-id="3f855-119">E-mail notification for AGPM is a domain-level setting.</span></span> <span data-ttu-id="3f855-120">Sie können unterschiedliche e-Mail-Adressen oder AGPM-e-Mail-Aliase auf den Registerkarten der Domänen **Delegierung** jeder Domäne angeben oder dieselben e-Mail-Adressen in ihrer gesamten Umgebung verwenden.</span><span class="sxs-lookup"><span data-stu-id="3f855-120">You can provide different Approver e-mail addresses or AGPM e-mail aliases on each domain's **Domain Delegation** tab, or use the same e-mail addresses throughout your environment.</span></span>

-   <span data-ttu-id="3f855-121">Standardmäßig werden e-Mail-Nachrichten, die als Ergebnis von Aktionen in Advanced Group Policy Management (AGPM) gesendet wurden, nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="3f855-121">By default, e-mail messages sent as a result of actions in Advanced Group Policy Management (AGPM) are not encrypted.</span></span> <span data-ttu-id="3f855-122">Sie können jedoch die e-Mail-Sicherheit für AGPM mithilfe von Registrierungseinstellungen konfigurieren, um anzugeben, ob die SSL-Verschlüsselung (Secure Sockets Layer) und welcher SMTP-Port verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f855-122">However, you can configure e-mail security for AGPM using registry settings to specify whether to use Secure Sockets Layer (SSL) encryption and which SMTP port to use.</span></span> <span data-ttu-id="3f855-123">Weitere Informationen finden Sie unter [Konfigurieren von e-Mail-Sicherheit für AGPM](configure-e-mail-security-for-agpm-agpm30ops.md)</span><span class="sxs-lookup"><span data-stu-id="3f855-123">For more information, see [Configure E-Mail Security for AGPM](configure-e-mail-security-for-agpm-agpm30ops.md)</span></span>

### <span data-ttu-id="3f855-124">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="3f855-124">Additional references</span></span>

-   [<span data-ttu-id="3f855-125">Konfigurieren von Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="3f855-125">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management.md)

 

 





