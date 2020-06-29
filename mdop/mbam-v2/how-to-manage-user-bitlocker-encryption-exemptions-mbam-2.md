---
title: So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Benutzer
description: So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Benutzer
author: dansimp
ms.assetid: 1bfd9d66-6a9a-4d0e-b54a-e5a6627f5ada
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d5530701fd208d42dc1f6774fac11ee9ca2036b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810936"
---
# <span data-ttu-id="f2c25-103">So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Benutzer</span><span class="sxs-lookup"><span data-stu-id="f2c25-103">How to Manage User BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="f2c25-104">Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) kann zum Verwalten des BitLocker-Schutzes verwendet werden, indem Benutzer freigestellt werden, wenn Benutzer vorhanden sind, die Ihre Laufwerke nicht verschlüsseln müssen oder möchten.</span><span class="sxs-lookup"><span data-stu-id="f2c25-104">Microsoft BitLocker Administration and Monitoring (MBAM) can be used to manage BitLocker protection by exempting users if there are users who do not need or want their drives encrypted.</span></span>

<span data-ttu-id="f2c25-105">Um Benutzer vom BitLocker-Schutz zu befreien, muss eine Organisation eine Infrastruktur zur Unterstützung von ausgenommenen Benutzern erstellen, beispielsweise indem Sie dem Benutzer eine Telefonnummer, eine Webseite oder eine Postanschrift zur Verfügung stellt, um eine Ausnahme zu beantragen.</span><span class="sxs-lookup"><span data-stu-id="f2c25-105">To exempt users from BitLocker protection, an organization will have to create an infrastructure to support exempted users, such as giving the user a contact telephone number, webpage, or mailing address to use to request an exemption.</span></span> <span data-ttu-id="f2c25-106">Darüber hinaus muss ein freigestellter Benutzer einer Sicherheitsgruppe für ein Gruppenrichtlinienobjekt hinzugefügt werden, das speziell für befreite Benutzer erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f2c25-106">Also, an exempt user will have to be added to a security group for a Group Policy Object that was created specifically for exempted users.</span></span> <span data-ttu-id="f2c25-107">Wenn sich Mitglieder dieser Sicherheitsgruppe an einem Computer anmelden, zeigt die Gruppenrichtlinieneinstellung des Benutzers an, dass der Benutzer vom BitLocker-Schutz ausgenommen ist.</span><span class="sxs-lookup"><span data-stu-id="f2c25-107">When members of this security group log on to a computer, the user’s Group Policy setting shows that the user is exempted from BitLocker protection.</span></span> <span data-ttu-id="f2c25-108">Die Gruppenrichtlinieneinstellung des Benutzers überschreibt die Computerrichtlinie, und der Computer bleibt von der BitLocker-Verschlüsselung ausgenommen.</span><span class="sxs-lookup"><span data-stu-id="f2c25-108">The user’s Group Policy setting overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span>

<span data-ttu-id="f2c25-109">**Hinweis**  Wenn der Computer bereits mit BitLocker geschützt ist, hat die Richtlinie für die Benutzer Befreiung keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="f2c25-109">**Note** If the computer is already BitLocker-protected, the user exemption policy has no effect.</span></span>

 

<span data-ttu-id="f2c25-110">In der folgenden Tabelle wird gezeigt, wie der BitLocker-Schutz angewendet wird, je nachdem, wie Ausnahmen eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f2c25-110">The following table shows how BitLocker protection is applied based on how exemptions are set.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f2c25-111">Benutzer Status</span><span class="sxs-lookup"><span data-stu-id="f2c25-111">User Status</span></span></th>
<th align="left"><span data-ttu-id="f2c25-112">Computer nicht freigestellt</span><span class="sxs-lookup"><span data-stu-id="f2c25-112">Computer Not Exempt</span></span></th>
<th align="left"><span data-ttu-id="f2c25-113">Computer ausgenommen</span><span class="sxs-lookup"><span data-stu-id="f2c25-113">Computer Exempt</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f2c25-114">Benutzer nicht freigestellt</span><span class="sxs-lookup"><span data-stu-id="f2c25-114">User not exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f2c25-115">Der BitLocker-Schutz wird auf einem Computer erzwungen</span><span class="sxs-lookup"><span data-stu-id="f2c25-115">BitLocker protection is enforced on computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="f2c25-116">Der BitLocker-Schutz wird auf dem Computer nicht erzwungen</span><span class="sxs-lookup"><span data-stu-id="f2c25-116">BitLocker protection is not enforced on computer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f2c25-117">Benutzer freigestellt</span><span class="sxs-lookup"><span data-stu-id="f2c25-117">User exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f2c25-118">Der BitLocker-Schutz wird auf dem Computer nicht erzwungen</span><span class="sxs-lookup"><span data-stu-id="f2c25-118">BitLocker protection is not enforced on computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="f2c25-119">Der BitLocker-Schutz wird auf dem Computer nicht erzwungen</span><span class="sxs-lookup"><span data-stu-id="f2c25-119">BitLocker protection is not enforced on computer</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="f2c25-120">So nehmen Sie einen Benutzer von der BitLocker-Verschlüsselung frei</span><span class="sxs-lookup"><span data-stu-id="f2c25-120">To exempt a user from BitLocker encryption</span></span>**

1.  <span data-ttu-id="f2c25-121">Erstellen Sie eine ActiveDirectoryDomainServices-Sicherheitsgruppe, die verwendet wird, um Benutzer Ausnahmen von BitLocker-Verschlüsselungsanforderungen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="f2c25-121">Create an ActiveDirectoryDomainServices security group that will be used to manage user exemptions from BitLocker encryption requirements.</span></span>

2.  <span data-ttu-id="f2c25-122">Erstellen Sie eine Gruppenrichtlinienobjekteinstellung mithilfe der Gruppenrichtlinienvorlage Microsoft BitLocker-Verwaltung und-Überwachung, und ordnen Sie Sie der Active Directory-Gruppe zu, die Sie im vorherigen Schritt erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="f2c25-122">Create a Group Policy Object setting by using the Microsoft BitLocker Administration and Monitoring Group Policy template and associate it with the Active Directory group that you created in the previous step.</span></span> <span data-ttu-id="f2c25-123">Die Richtlinieneinstellungen zum Ausschließen von Benutzern finden Sie unter **UserConfiguration\\Administrative Templates\\Windows Components\\MDOP MBAM (BitLocker-Verwaltung)**.</span><span class="sxs-lookup"><span data-stu-id="f2c25-123">The policy settings to exempt users can be found under **UserConfiguration\\Administrative Templates\\Windows Components\\MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="f2c25-124">Nachdem Sie eine Sicherheitsgruppe für von BitLocker freigestellten Benutzern erstellt haben, fügen Sie dieser Gruppe die Namen der Benutzer hinzu, die eine Ausnahmegenehmigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="f2c25-124">After creating a security group for BitLocker-exempted users, add to this group the names of the users who are requesting an exemption.</span></span> <span data-ttu-id="f2c25-125">Wenn sich Benutzer an einem Computer anmelden, der von BitLocker gesteuert wird, überprüft der MBAM-Client die Einstellung für die Benutzer Freistellungs Richtlinie und unterbricht den Schutz, je nachdem, ob der Benutzer Teil der BitLocker-Ausnahme Sicherheitsgruppe ist.</span><span class="sxs-lookup"><span data-stu-id="f2c25-125">When users log on to a computer controlled by BitLocker, the MBAM client will check the User Exemption Policy setting and will suspend protection based on whether the user is part of the BitLocker exemption security group.</span></span>

    <span data-ttu-id="f2c25-126">**Wichtig**  Szenarien mit freigegebenen Computern erfordern besondere Berücksichtigung bei der Verwendung von Ausnahmen für Benutzer.</span><span class="sxs-lookup"><span data-stu-id="f2c25-126">**Important** Shared computer scenarios require special consideration when using user exemptions.</span></span> <span data-ttu-id="f2c25-127">Wenn sich ein nicht ausgenommener Benutzer an einem Computer anmeldet, der für einen ausgenommenen Benutzer freigegeben wurde, kann der Computer verschlüsselt sein.</span><span class="sxs-lookup"><span data-stu-id="f2c25-127">If a non-exempt user logs on to a computer shared with an exempt user, the computer may be encrypted.</span></span>

     

**<span data-ttu-id="f2c25-128">So ermöglichen Sie Benutzern das Anfordern einer Ausnahme von der BitLocker-Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="f2c25-128">To enable users to request an exemption from BitLocker encryption</span></span>**

1.  <span data-ttu-id="f2c25-129">Wenn Sie Benutzer Freistellungs Richtlinien mithilfe der MBAM-Richtlinienvorlage konfiguriert haben, kann ein Benutzer eine Ausnahme vom BitLocker-Schutz über den MBAM-Client anfordern.</span><span class="sxs-lookup"><span data-stu-id="f2c25-129">If you have configured user exemption policies by using the MBAM policy template, a user can request an exemption from BitLocker protection through the MBAM client.</span></span>

2.  <span data-ttu-id="f2c25-130">Wenn sich Benutzer an einem Computer anmelden, der verschlüsselt werden muss, erhalten Sie eine Benachrichtigung, dass Ihr Computer verschlüsselt wird.</span><span class="sxs-lookup"><span data-stu-id="f2c25-130">When users log on to a computer that is required to be encrypted, they receive a notification that their computer is going to be encrypted.</span></span> <span data-ttu-id="f2c25-131">Sie können die **Anforderungs Befreiung** auswählen und die Verschlüsselung verschieben, indem Sie **später**auswählen, oder " **Start** " auswählen, um die BitLocker-Verschlüsselung zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="f2c25-131">They can select **Request Exemption** and postpone the encryption by selecting **Later**, or select **Start** to accept the BitLocker encryption.</span></span>

    <span data-ttu-id="f2c25-132">**Hinweis**  Wenn Sie die **ausnahmeanforderung** auswählen, wird der BitLocker-Schutz so lange verschoben, bis die maximale Zeitdauer in der Benutzer Freistellungs Richtlinie festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="f2c25-132">**Note** Selecting **Request Exemption** postpones the BitLocker protection until the maximum time that is set in the User Exemption Policy.</span></span>

     

3.  <span data-ttu-id="f2c25-133">Wenn Benutzer die Option **Befreiung anfordern**auswählen, erhalten Sie eine Benachrichtigung, in der Sie aufgefordert werden, sich an die BitLocker-Verwaltungsgruppe Ihrer Organisation zu wenden.</span><span class="sxs-lookup"><span data-stu-id="f2c25-133">If users select **Request Exemption**, they receive a notification telling them to contact your organization’s BitLocker administration group.</span></span> <span data-ttu-id="f2c25-134">Je nachdem, wie die Richtlinie für die Benutzer Freistellung konfigurieren konfiguriert ist, werden Benutzern mindestens eine der folgenden Kontaktmethoden zur Verfügung gestellt:</span><span class="sxs-lookup"><span data-stu-id="f2c25-134">Depending on how the Configure User Exemption Policy is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="f2c25-135">Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="f2c25-135">Phone Number</span></span>

    -   <span data-ttu-id="f2c25-136">URL der Webseite</span><span class="sxs-lookup"><span data-stu-id="f2c25-136">Webpage URL</span></span>

    -   <span data-ttu-id="f2c25-137">Postanschrift</span><span class="sxs-lookup"><span data-stu-id="f2c25-137">Mailing Address</span></span>

    <span data-ttu-id="f2c25-138">Nachdem die ausnahmeanforderung eingegangen ist, kann der MBAM-Administrator entscheiden, ob der Benutzer zur BitLocker-Ausnahme Active Directory-Gruppe hinzugefügt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="f2c25-138">After the exemption request is received, the MBAM Administrator can take decide if it is appropriate to add the user to the BitLocker Exemption Active Directory group.</span></span>

    <span data-ttu-id="f2c25-139">**Hinweis**  Sobald ein Benutzer eine ausnahmeanforderung übermittelt hat, meldet der MBAM-Agent den Benutzer als "vorübergehend ausgenommen" und wartet dann eine konfigurierbare Anzahl von Tagen, bevor er die Konformität des Computers erneut überprüft.</span><span class="sxs-lookup"><span data-stu-id="f2c25-139">**Note** Once a user submits an exemption request, the MBAM agent reports the user as “temporarily exempt” and then waits a configurable number of days before it checks the computer’s compliance again.</span></span> <span data-ttu-id="f2c25-140">Wenn der MBAM-Administrator die ausnahmeanforderung ablehnt, wird die Option "ausnahmeanforderung" deaktiviert, wodurch verhindert wird, dass der Benutzer die Ausnahme erneut anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="f2c25-140">If the MBAM administrator rejects the exemption request, the exemption request option is deactivated, which prevents the user from being able to request the exemption again.</span></span>

     

## <span data-ttu-id="f2c25-141">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="f2c25-141">Related topics</span></span>


[<span data-ttu-id="f2c25-142">Verwalten von MBAM 2.0-Funktionen</span><span class="sxs-lookup"><span data-stu-id="f2c25-142">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)

 

 





