---
title: So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Benutzer
description: So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Benutzer
author: dansimp
ms.assetid: 48d69721-504f-4524-8a04-b9ce213ac9b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c3d70558a65c3288174413d6c36cc9c77bc9eaa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804622"
---
# <span data-ttu-id="2c1b5-103">So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Benutzer</span><span class="sxs-lookup"><span data-stu-id="2c1b5-103">How to Manage User BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="2c1b5-104">Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) kann zum Verwalten des BitLocker-Schutzes verwendet werden, indem Benutzer freigestellt werden, die Ihre Laufwerke nicht verschlüsseln müssen oder möchten.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-104">Microsoft BitLocker Administration and Monitoring (MBAM) can be used to manage BitLocker protection by exempting users who do not need or want their drives encrypted.</span></span>

<span data-ttu-id="2c1b5-105">Um Benutzer vom BitLocker-Schutz zu befreien, muss eine Organisation zunächst eine Infrastruktur zur Unterstützung derartiger Ausnahmen erstellen.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-105">To exempt users from BitLocker protection, an organization must first create an infrastructure to support such exemptions.</span></span> <span data-ttu-id="2c1b5-106">Die unterstützende Infrastruktur kann eine Kontakt Telefonnummer, eine Webseite oder eine Postanschrift enthalten, um eine Befreiung zu beantragen.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-106">The supporting infrastructure might include a contact telephone number, webpage, or mailing address to request exemption.</span></span> <span data-ttu-id="2c1b5-107">Darüber hinaus muss jeder befreite Benutzer einer Sicherheitsgruppe für Gruppenrichtlinien hinzugefügt werden, die speziell für befreite Benutzer erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-107">Also, any exempt user will have to be added to a security group for Group Policy created specifically for exempted users.</span></span> <span data-ttu-id="2c1b5-108">Wenn sich Mitglieder dieser Sicherheitsgruppe an einem Computer anmelden, zeigt die Benutzergruppenrichtlinie an, dass der Benutzer vom BitLocker-Schutz ausgenommen ist.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-108">When members of this security group log on to a computer, the user Group Policy shows that the user is exempted from BitLocker protection.</span></span> <span data-ttu-id="2c1b5-109">Die Benutzerrichtlinie überschreibt die Computerrichtlinie, und der Computer bleibt von der BitLocker-Verschlüsselung ausgenommen.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-109">The user policy overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span>

<span data-ttu-id="2c1b5-110">**Hinweis**  Wenn der Computer bereits mit BitLocker geschützt ist, hat die Richtlinie für die Benutzer Befreiung keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-110">**Note** If the computer is already BitLocker-protected, the user exemption policy has no effect.</span></span>

 

<span data-ttu-id="2c1b5-111">In der folgenden Tabelle wird gezeigt, wie der BitLocker-Schutz angewendet wird, je nachdem, wie Ausnahmen eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-111">The following table shows how BitLocker protection is applied based on how exemptions are set.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2c1b5-112">Benutzer Status</span><span class="sxs-lookup"><span data-stu-id="2c1b5-112">User Status</span></span></th>
<th align="left"><span data-ttu-id="2c1b5-113">Computer nicht freigestellt</span><span class="sxs-lookup"><span data-stu-id="2c1b5-113">Computer Not Exempt</span></span></th>
<th align="left"><span data-ttu-id="2c1b5-114">Computer ausgenommen</span><span class="sxs-lookup"><span data-stu-id="2c1b5-114">Computer Exempt</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2c1b5-115">Benutzer nicht freigestellt</span><span class="sxs-lookup"><span data-stu-id="2c1b5-115">User not exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2c1b5-116">Der BitLocker-Schutz wird auf dem Computer erzwungen.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-116">BitLocker protection is enforced on the computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c1b5-117">Der BitLocker-Schutz wird auf dem Computer nicht erzwungen.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-117">BitLocker protection is not enforced on the computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2c1b5-118">Benutzer freigestellt</span><span class="sxs-lookup"><span data-stu-id="2c1b5-118">User exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2c1b5-119">Der BitLocker-Schutz wird auf dem Computer nicht erzwungen.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-119">BitLocker protection is not enforced on the computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c1b5-120">Der BitLocker-Schutz wird auf dem Computer nicht erzwungen.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-120">BitLocker protection is not enforced on the computer.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="2c1b5-121">So nehmen Sie einen Benutzer von der BitLocker-Verschlüsselung frei</span><span class="sxs-lookup"><span data-stu-id="2c1b5-121">To exempt a user from BitLocker Encryption</span></span>**

1.  <span data-ttu-id="2c1b5-122">Erstellen Sie eine ActiveDirectoryDomainServices-Sicherheitsgruppe, die verwendet wird, um Benutzer Ausnahmen von der BitLocker-Verschlüsselung zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-122">Create an ActiveDirectoryDomainServices security group that will be used to manage user exemptions from BitLocker encryption.</span></span>

2.  <span data-ttu-id="2c1b5-123">Erstellen Sie eine Gruppenrichtlinienobjekteinstellung mithilfe der MBAM-Gruppenrichtlinienvorlage.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-123">Create a Group Policy Object setting by using the MBAM Group Policy template.</span></span> <span data-ttu-id="2c1b5-124">Ordnen Sie das Gruppenrichtlinienobjekt der Active Directory-Gruppe zu, die Sie im vorherigen Schritt erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-124">Associate the Group Policy Object with the Active Directory group that you created in the previous step.</span></span> <span data-ttu-id="2c1b5-125">Weitere Informationen zu den erforderlichen Richtlinieneinstellungen, mit denen Benutzer die Befreiung von der BitLocker-Verschlüsselung anfordern können, finden Sie im Abschnitt Konfigurieren von Benutzer Freistellungs Richtlinien unter [Planen der MBAM 1,0-Gruppenrichtlinienanforderungen](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2c1b5-125">For more information about the necessary policy settings to enable users to request exemption from BitLocker encryption, see the Configure User Exemption Policy section in [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span>

3.  <span data-ttu-id="2c1b5-126">Nachdem Sie eine Sicherheitsgruppe für von BitLocker freigestellten Benutzern erstellt haben, fügen Sie dieser Gruppe die Namen der Benutzer hinzu, die eine Befreiung anfordern.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-126">After creating a security group for BitLocker-exempted users, add to this group the names of the users who are requesting exemption.</span></span> <span data-ttu-id="2c1b5-127">Wenn sich ein Benutzer bei einem von BitLocker gesteuerten Computer anmeldet, überprüft der MBAM-Client die Richtlinieneinstellung für die Benutzer Befreiung und unterbricht den Schutz, je nachdem, ob der Benutzer Teil der BitLocker-Ausnahme Sicherheitsgruppe ist.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-127">When a user logs on to a computer controlled by BitLocker, the MBAM client will check the User Exemption Policy setting and will suspend protection based on whether the user is part of the BitLocker exemption security group.</span></span>

    <span data-ttu-id="2c1b5-128">**Hinweis**  Szenarien für gemeinsam genutzte Computer erfordern besondere Rücksicht auf die Benutzer Befreiung.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-128">**Note** Shared computer scenarios require special consideration regarding user exemption.</span></span> <span data-ttu-id="2c1b5-129">Wenn sich ein nicht ausgenommener Benutzer an einem Computer anmeldet, der für einen ausgenommenen Benutzer freigegeben wurde, kann der Computer verschlüsselt sein.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-129">If a non-exempt user logs on to a computer shared with an exempt user, the computer may be encrypted.</span></span>

     

**<span data-ttu-id="2c1b5-130">So ermöglichen Sie Benutzern das Anfordern einer Ausnahme von der BitLocker-Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="2c1b5-130">To enable users to request exemption from BitLocker Encryption</span></span>**

1.  <span data-ttu-id="2c1b5-131">Nachdem Sie die Richtlinien für die Benutzer Befreiung durch usingwith der MBAM-Richtlinienvorlage konfiguriert haben, kann ein Benutzer eine Befreiung vom BitLocker-Schutz über den MBAM-Client anfordern.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-131">After you have configured user-exemption policies by usingwith the MBAM Policy template, a user can request exemption from BitLocker protection through the MBAM client.</span></span>

2.  <span data-ttu-id="2c1b5-132">Wenn sich ein Benutzer an einem Computer anmeldet, der in der MBAM-Hardware Kompatibilitätsliste als **kompatibel** gekennzeichnet ist, zeigt das System dem Benutzer eine Benachrichtigung an, dass der Computer verschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-132">When a user logs on to a computer that is marked as **Compatible** in the MBAM Hardware Compatibility list, the system presents the user with a notification that the computer is going to be encrypted.</span></span> <span data-ttu-id="2c1b5-133">Der Benutzer kann **Anforderungs Befreiung** auswählen und die Verschlüsselung verschieben, indem er **später**auswählt, oder wählen Sie **Start** aus, um die BitLocker-Verschlüsselung zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-133">The user can select **Request Exemption** and postpone the encryption by selecting **Later**, or select **Start** to accept the BitLocker encryption.</span></span>

    <span data-ttu-id="2c1b5-134">**Hinweis**  Wenn Sie die Option **Befreiung anfordern** auswählen, wird der BitLocker-Schutz so lange verschoben, bis die maximale Zeit in der Benutzer Freistellungs Richtlinie gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-134">**Note** Selecting **Request Exemption** will postpone the BitLocker protection until the maximum time set in the User Exemption Policy.</span></span>

     

3.  <span data-ttu-id="2c1b5-135">Wenn ein Benutzer die **Anforderungs Befreiung**auswählt, wird der Benutzer benachrichtigt, wenn er sich an die BitLocker-Verwaltungsgruppe der Organisation wenden möchte.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-135">When a user selects **Request Exemption**, the user is notified to contact the organization's BitLocker administration group.</span></span> <span data-ttu-id="2c1b5-136">Je nachdem, wie die Richtlinie für die Benutzer Freistellung konfigurieren konfiguriert ist, werden Benutzern mindestens eine der folgenden Kontaktmethoden zur Verfügung gestellt:</span><span class="sxs-lookup"><span data-stu-id="2c1b5-136">Depending on how the Configure User Exemption Policy is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="2c1b5-137">Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="2c1b5-137">Phone Number</span></span>

    -   <span data-ttu-id="2c1b5-138">URL der Webseite</span><span class="sxs-lookup"><span data-stu-id="2c1b5-138">Webpage URL</span></span>

    -   <span data-ttu-id="2c1b5-139">Postanschrift</span><span class="sxs-lookup"><span data-stu-id="2c1b5-139">Mailing Address</span></span>

    <span data-ttu-id="2c1b5-140">Nach der Übermittlung der Anforderung kann der MBAM-Administrator entscheiden, ob der Benutzer zur BitLocker-Ausnahmegruppe Active Directory hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-140">After submittal of the request, the MBAM Administrator can decide if it is appropriate to add the user to the BitLocker Exemption Active Directory group.</span></span>

    <span data-ttu-id="2c1b5-141">**Hinweis**  Nachdem die Beschränkungs Frist für die Benutzer Freistellungs Richtlinie abgelaufen ist, wird den Benutzern die Option zum Anfordern einer Ausnahme von der Verschlüsselungsrichtlinie nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-141">**Note** Once the postpone time limit from the User Exemption Policy has expired, users will not see the option to request exemption to the encryption policy.</span></span> <span data-ttu-id="2c1b5-142">An diesem Punkt müssen Benutzer sich direkt mit dem MBAM-Administrator in Verbindung setzen, um eine Ausnahme vom BitLocker-Schutz zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-142">At this point, users must contact the MBAM administrator directly in order to receive exemption from BitLocker Protection.</span></span>

     

## <span data-ttu-id="2c1b5-143">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2c1b5-143">Related topics</span></span>


[<span data-ttu-id="2c1b5-144">Verwalten von MBAM 1.0-Funktionen</span><span class="sxs-lookup"><span data-stu-id="2c1b5-144">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





