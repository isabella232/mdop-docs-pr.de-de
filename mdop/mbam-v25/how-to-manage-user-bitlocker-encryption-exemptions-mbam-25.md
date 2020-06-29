---
title: So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Benutzer
description: So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Benutzer
author: dansimp
ms.assetid: f582ab82-5bb5-4cd3-ad7c-483240533cf9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4224a0fb6d905c2362659efe7cf05e16756f7c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811968"
---
# <span data-ttu-id="8b797-103">So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Benutzer</span><span class="sxs-lookup"><span data-stu-id="8b797-103">How to Manage User BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="8b797-104">Mit Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) können Sie Benutzer von den BitLocker-Laufwerk Verschlüsselungsanforderungen ausschließen.</span><span class="sxs-lookup"><span data-stu-id="8b797-104">Microsoft BitLocker Administration and Monitoring (MBAM) enables you to exempt users from BitLocker Drive Encryption requirements.</span></span>

<span data-ttu-id="8b797-105">Um Benutzer vom BitLocker-Schutz zu befreien, müssen Sie Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="8b797-105">To exempt users from BitLocker protection, you have to:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8b797-106">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="8b797-106">Task</span></span></th>
<th align="left"><span data-ttu-id="8b797-107">Details</span><span class="sxs-lookup"><span data-stu-id="8b797-107">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8b797-108">Erstellen einer Infrastruktur zur Unterstützung von befreiten Benutzern</span><span class="sxs-lookup"><span data-stu-id="8b797-108">Create an infrastructure to support exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b797-109">Beispiele für diese Infrastruktur sind die Bereitstellung von Benutzern mit einer Kontakt Telefonnummer, einer Webseite oder einer Postanschrift, die Sie verwenden können, um eine Ausnahme zu beantragen.</span><span class="sxs-lookup"><span data-stu-id="8b797-109">Examples of this infrastructure include providing users with a contact telephone number, webpage, or mailing address that they can use to request an exemption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8b797-110">Hinzufügen des befreiten Benutzers zu einer Sicherheitsgruppe für ein Gruppenrichtlinienobjekt, das speziell für befreite Benutzer konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="8b797-110">Add the exempted user to a security group for a Group Policy Object that is configured specifically for exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b797-111">Wenn sich Mitglieder dieser Sicherheitsgruppe bei einem Computer anmelden, wird der Benutzer durch die Gruppenrichtlinieneinstellung des Benutzers vom BitLocker-Schutz ausgenommen.</span><span class="sxs-lookup"><span data-stu-id="8b797-111">When members of this security group sign in to a computer, the user’s Group Policy setting exempts the user from BitLocker protection.</span></span> <span data-ttu-id="8b797-112">Die Gruppenrichtlinieneinstellung des Benutzers überschreibt die Computerrichtlinie, und der Computer bleibt von der BitLocker-Verschlüsselung ausgenommen.</span><span class="sxs-lookup"><span data-stu-id="8b797-112">The user’s Group Policy setting overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="8b797-113">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="8b797-113">Note</span></span></strong><br/><p><span data-ttu-id="8b797-114">MBAM erlässt die Verschlüsselungsrichtlinie nicht, wenn der Computer bereits BitLocker-geschützt ist und der Benutzer freigestellt ist.</span><span class="sxs-lookup"><span data-stu-id="8b797-114">MBAM does not enact the encryption policy if the computer is already BitLocker-protected and the user is exempted.</span></span> <span data-ttu-id="8b797-115">Wenn ein anderer Benutzer, der nicht von der Verschlüsselungsrichtlinie ausgenommen ist, sich auf dem Computer anmeldet, wird jedoch die Verschlüsselung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b797-115">However, if another user who is not exempt from the encryption policy signs in to the computer, encryption will take place.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="8b797-116">In den folgenden Schritten wird beschrieben, was geschieht, wenn Endbenutzer eine Ausnahme vom BitLocker-Laufwerk-Verschlüsselungs Befreiungsprozess über den MBAM-Client oder über den von Ihrer Organisation verwendeten Prozess anfordern.</span><span class="sxs-lookup"><span data-stu-id="8b797-116">The following steps describe what occurs when end users request an exemption from the BitLocker Drive Encryption exemption process through the MBAM Client or through whatever process your organization uses.</span></span> <span data-ttu-id="8b797-117">Sie müssen die MBAM-Gruppenrichtlinieneinstellungen so konfigurieren, dass Endbenutzer eine Ausnahme von der BitLocker-Laufwerkverschlüsselung anfordern können.</span><span class="sxs-lookup"><span data-stu-id="8b797-117">You must configure MBAM Group Policy settings to allow end users to request an exemption from BitLocker Drive Encryption.</span></span>

1.  <span data-ttu-id="8b797-118">Wenn sich Endbenutzer bei einem Computer anmelden, der verschlüsselt werden muss, erhalten Sie eine Benachrichtigung, dass Ihr Computer verschlüsselt wird.</span><span class="sxs-lookup"><span data-stu-id="8b797-118">When end users sign in to a computer that is required to be encrypted, they receive a notification that their computer is going to be encrypted.</span></span> <span data-ttu-id="8b797-119">Sie können die **Anforderungs Befreiung** auswählen und die Verschlüsselung verschieben, indem Sie **verschieben**auswählen, oder Sie können **Verschlüsselung starten** auswählen, um die BitLocker-Verschlüsselung zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="8b797-119">They can select **Request Exemption** and postpone the encryption by selecting **Postpone**, or they can select **Start Encryption** to accept the BitLocker encryption.</span></span>

    **<span data-ttu-id="8b797-120">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="8b797-120">Note</span></span>**  
    <span data-ttu-id="8b797-121">Wenn Sie die **ausnahmeanforderung** auswählen, wird der BitLocker-Schutz so lange verschoben, bis die maximale Zeitdauer in der Benutzer Freistellungs Richtlinie festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="8b797-121">Selecting **Request Exemption** postpones the BitLocker protection until the maximum time that is set in the User Exemption Policy.</span></span>



2.  <span data-ttu-id="8b797-122">Wenn Endbenutzer die Option **Befreiung anfordern**auswählen, erhalten Sie eine Benachrichtigung, in der Sie aufgefordert werden, sich an die BitLocker-Verwaltungsgruppe der Organisation zu wenden.</span><span class="sxs-lookup"><span data-stu-id="8b797-122">If end users select **Request Exemption**, they receive a notification telling them to contact the organization’s BitLocker administration group.</span></span> <span data-ttu-id="8b797-123">Je nachdem, wie die **Richtlinie für die Benutzer Freistellung konfigurieren** konfiguriert ist, werden Benutzern mindestens eine der folgenden Kontaktmethoden zur Verfügung gestellt:</span><span class="sxs-lookup"><span data-stu-id="8b797-123">Depending on how the **Configure User Exemption Policy** is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="8b797-124">Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="8b797-124">Phone number</span></span>

    -   <span data-ttu-id="8b797-125">URL der Webseite</span><span class="sxs-lookup"><span data-stu-id="8b797-125">Webpage URL</span></span>

    -   <span data-ttu-id="8b797-126">Postanschrift</span><span class="sxs-lookup"><span data-stu-id="8b797-126">Mailing address</span></span>

3.  <span data-ttu-id="8b797-127">Nachdem die ausnahmeanforderung eingegangen ist, entscheidet der MBAM-Administrator, ob der Benutzer der BitLocker-Ausnahmegruppe Active Directory-Domänendienste (AD DS) hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b797-127">After the exemption request is received, the MBAM administrator decides whether to add the user to the BitLocker Exemption Active Directory Domain Services (AD DS) group.</span></span>

4.  <span data-ttu-id="8b797-128">Nachdem ein Endbenutzer eine ausnahmeanforderung eingereicht hat, meldet der MBAM-Client den Benutzer als "vorübergehend ausgenommen".</span><span class="sxs-lookup"><span data-stu-id="8b797-128">After an end user submits an exemption request, the MBAM Client reports the user as “Temporarily exempt.”</span></span> <span data-ttu-id="8b797-129">Der Client wartet dann eine festgelegte Anzahl von Tagen, die von den IT-Administratoren konfiguriert werden, bevor er die Konformität des Computers erneut überprüft.</span><span class="sxs-lookup"><span data-stu-id="8b797-129">The Client then waits a specified number of days, which IT administrators configure, before it checks the computer’s compliance again.</span></span> <span data-ttu-id="8b797-130">Wenn der MBAM-Administrator die ausnahmeanforderung ablehnt, wird die Option "ausnahmeanforderung" deaktiviert, wodurch verhindert wird, dass der Benutzer die Befreiung erneut anfordert.</span><span class="sxs-lookup"><span data-stu-id="8b797-130">If the MBAM administrator rejects the exemption request, the exemption request option is deactivated, which prevents the user from requesting the exemption again.</span></span>

<span data-ttu-id="8b797-131">Mit Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) können Sie Benutzer von den BitLocker-Laufwerk Verschlüsselungsanforderungen ausschließen.</span><span class="sxs-lookup"><span data-stu-id="8b797-131">Microsoft BitLocker Administration and Monitoring (MBAM) enables you to exempt users from BitLocker Drive Encryption requirements.</span></span>

<span data-ttu-id="8b797-132">Um Benutzer vom BitLocker-Schutz zu befreien, müssen Sie Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="8b797-132">To exempt users from BitLocker protection, you have to:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8b797-133">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="8b797-133">Task</span></span></th>
<th align="left"><span data-ttu-id="8b797-134">Details</span><span class="sxs-lookup"><span data-stu-id="8b797-134">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8b797-135">Erstellen einer Infrastruktur zur Unterstützung von befreiten Benutzern</span><span class="sxs-lookup"><span data-stu-id="8b797-135">Create an infrastructure to support exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b797-136">Beispiele für diese Infrastruktur sind die Bereitstellung von Benutzern mit einer Kontakt Telefonnummer, einer Webseite oder einer Postanschrift, die Sie verwenden können, um eine Ausnahme zu beantragen.</span><span class="sxs-lookup"><span data-stu-id="8b797-136">Examples of this infrastructure include providing users with a contact telephone number, webpage, or mailing address that they can use to request an exemption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8b797-137">Hinzufügen des befreiten Benutzers zu einer Sicherheitsgruppe für ein Gruppenrichtlinienobjekt, das speziell für befreite Benutzer konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="8b797-137">Add the exempted user to a security group for a Group Policy Object that is configured specifically for exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b797-138">Wenn sich Mitglieder dieser Sicherheitsgruppe bei einem Computer anmelden, wird der Benutzer durch die Gruppenrichtlinieneinstellung des Benutzers vom BitLocker-Schutz ausgenommen.</span><span class="sxs-lookup"><span data-stu-id="8b797-138">When members of this security group sign in to a computer, the user’s Group Policy setting exempts the user from BitLocker protection.</span></span> <span data-ttu-id="8b797-139">Die Gruppenrichtlinieneinstellung des Benutzers überschreibt die Computerrichtlinie, und der Computer bleibt von der BitLocker-Verschlüsselung ausgenommen.</span><span class="sxs-lookup"><span data-stu-id="8b797-139">The user’s Group Policy setting overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="8b797-140">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="8b797-140">Note</span></span></strong><br/><p><span data-ttu-id="8b797-141">Wenn der Computer bereits mit BitLocker geschützt ist, hat die Richtlinie für die Benutzer Befreiung keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="8b797-141">If the computer is already BitLocker-protected, the User Exemption Policy has no effect.</span></span> <span data-ttu-id="8b797-142">Darüber hinaus erfolgt die Verschlüsselung, wenn sich ein anderer Benutzer an einem Computer anmeldet, der nicht von der Verschlüsselungsrichtlinie ausgenommen ist.</span><span class="sxs-lookup"><span data-stu-id="8b797-142">In addition, if another user signs in to a computer that is not exempt from the encryption policy, encryption will take place.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="8b797-143">In den folgenden Schritten wird beschrieben, was geschieht, wenn Endbenutzer eine Ausnahme vom BitLocker-Laufwerk-Verschlüsselungs Befreiungsprozess über den MBAM-Client oder über den von Ihrer Organisation verwendeten Prozess anfordern.</span><span class="sxs-lookup"><span data-stu-id="8b797-143">The following steps describe what occurs when end users request an exemption from the BitLocker Drive Encryption exemption process through the MBAM Client or through whatever process your organization uses.</span></span> <span data-ttu-id="8b797-144">Sie müssen die MBAM-Gruppenrichtlinieneinstellungen so konfigurieren, dass Endbenutzer eine Ausnahme von der BitLocker-Laufwerkverschlüsselung anfordern können.</span><span class="sxs-lookup"><span data-stu-id="8b797-144">You must configure MBAM Group Policy settings to allow end users to request an exemption from BitLocker Drive Encryption.</span></span>

1.  <span data-ttu-id="8b797-145">Wenn sich Endbenutzer bei einem Computer anmelden, der verschlüsselt werden muss, erhalten Sie eine Benachrichtigung, dass Ihr Computer verschlüsselt wird.</span><span class="sxs-lookup"><span data-stu-id="8b797-145">When end users sign in to a computer that is required to be encrypted, they receive a notification that their computer is going to be encrypted.</span></span> <span data-ttu-id="8b797-146">Sie können die **Anforderungs Befreiung** auswählen und die Verschlüsselung verschieben, indem Sie **verschieben**auswählen, oder Sie können **Verschlüsselung starten** auswählen, um die BitLocker-Verschlüsselung zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="8b797-146">They can select **Request Exemption** and postpone the encryption by selecting **Postpone**, or they can select **Start Encryption** to accept the BitLocker encryption.</span></span>

    **<span data-ttu-id="8b797-147">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="8b797-147">Note</span></span>**  
    <span data-ttu-id="8b797-148">Wenn Sie die **ausnahmeanforderung** auswählen, wird der BitLocker-Schutz so lange verschoben, bis die maximale Zeitdauer in der Benutzer Freistellungs Richtlinie festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="8b797-148">Selecting **Request Exemption** postpones the BitLocker protection until the maximum time that is set in the User Exemption Policy.</span></span>



2.  <span data-ttu-id="8b797-149">Wenn Endbenutzer die Option **Befreiung anfordern**auswählen, erhalten Sie eine Benachrichtigung, in der Sie aufgefordert werden, sich an die BitLocker-Verwaltungsgruppe der Organisation zu wenden.</span><span class="sxs-lookup"><span data-stu-id="8b797-149">If end users select **Request Exemption**, they receive a notification telling them to contact the organization’s BitLocker administration group.</span></span> <span data-ttu-id="8b797-150">Je nachdem, wie die **Richtlinie für die Benutzer Freistellung konfigurieren** konfiguriert ist, werden Benutzern mindestens eine der folgenden Kontaktmethoden zur Verfügung gestellt:</span><span class="sxs-lookup"><span data-stu-id="8b797-150">Depending on how the **Configure User Exemption Policy** is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="8b797-151">Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="8b797-151">Phone number</span></span>

    -   <span data-ttu-id="8b797-152">URL der Webseite</span><span class="sxs-lookup"><span data-stu-id="8b797-152">Webpage URL</span></span>

    -   <span data-ttu-id="8b797-153">Postanschrift</span><span class="sxs-lookup"><span data-stu-id="8b797-153">Mailing address</span></span>

3.  <span data-ttu-id="8b797-154">Nachdem die ausnahmeanforderung eingegangen ist, entscheidet der MBAM-Administrator, ob der Benutzer der BitLocker-Ausnahmegruppe Active Directory-Domänendienste (AD DS) hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b797-154">After the exemption request is received, the MBAM administrator decides whether to add the user to the BitLocker Exemption Active Directory Domain Services (AD DS) group.</span></span>

4.  <span data-ttu-id="8b797-155">Nachdem ein Endbenutzer eine ausnahmeanforderung eingereicht hat, meldet der MBAM-Client den Benutzer als "vorübergehend ausgenommen".</span><span class="sxs-lookup"><span data-stu-id="8b797-155">After an end user submits an exemption request, the MBAM Client reports the user as “Temporarily exempt.”</span></span> <span data-ttu-id="8b797-156">Der Client wartet dann eine festgelegte Anzahl von Tagen, die von den IT-Administratoren konfiguriert werden, bevor er die Konformität des Computers erneut überprüft.</span><span class="sxs-lookup"><span data-stu-id="8b797-156">The Client then waits a specified number of days, which IT administrators configure, before it checks the computer’s compliance again.</span></span> <span data-ttu-id="8b797-157">Wenn der MBAM-Administrator die ausnahmeanforderung ablehnt, wird die Option "ausnahmeanforderung" deaktiviert, wodurch verhindert wird, dass der Benutzer die Befreiung erneut anfordert.</span><span class="sxs-lookup"><span data-stu-id="8b797-157">If the MBAM administrator rejects the exemption request, the exemption request option is deactivated, which prevents the user from requesting the exemption again.</span></span>

**<span data-ttu-id="8b797-158">So nehmen Sie einen Benutzer von der BitLocker-Laufwerkverschlüsselung frei</span><span class="sxs-lookup"><span data-stu-id="8b797-158">To exempt a user from BitLocker Drive Encryption</span></span>**

1.  <span data-ttu-id="8b797-159">Erstellen Sie eine AD DS-Sicherheitsgruppe, die verwendet wird, um Benutzer Ausnahmen von BitLocker-Verschlüsselungsanforderungen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="8b797-159">Create an AD DS security group that will be used to manage user exemptions from BitLocker encryption requirements.</span></span>

2.  <span data-ttu-id="8b797-160">Erstellen Sie ein Gruppenrichtlinienobjekt mithilfe der Gruppenrichtlinienvorlagen für Microsoft BitLocker-Verwaltung und-Überwachung.</span><span class="sxs-lookup"><span data-stu-id="8b797-160">Create a Group Policy Object by using the Microsoft BitLocker Administration and Monitoring Group Policy Templates.</span></span>

3.  <span data-ttu-id="8b797-161">Ordnen Sie das Gruppenrichtlinienobjekt der AD DS-Gruppe zu, die Sie im vorherigen Schritt erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="8b797-161">Associate the Group Policy Object with the AD DS group that you created in the previous step.</span></span> <span data-ttu-id="8b797-162">Die Richtlinieneinstellungen, um Benutzer zu befreien, finden Sie unter: **UserConfiguration** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker-Verwaltung)**.</span><span class="sxs-lookup"><span data-stu-id="8b797-162">The policy settings to exempt users are located at: **UserConfiguration** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)**.</span></span>

4.  <span data-ttu-id="8b797-163">Fügen Sie der Sicherheitsgruppe, die Sie für BitLocker-Ausgeschlossene Benutzer erstellt haben, die Namen der Benutzer hinzu, die eine Befreiung anfordern.</span><span class="sxs-lookup"><span data-stu-id="8b797-163">To the security group you created for BitLocker exempted users, add the names of the users who are requesting an exemption.</span></span>

    <span data-ttu-id="8b797-164">Wenn sich ein Benutzer bei einem von BitLocker kontrollierten Computer anmeldet, überprüft der MBAM-Client die Einstellung für die Benutzer Freistellungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="8b797-164">When a user signs in to a computer controlled by BitLocker, the MBAM Client checks the User Exemption Policy setting.</span></span> <span data-ttu-id="8b797-165">Wenn der Computer bereits verschlüsselt ist, wird der BitLocker-Schutz nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="8b797-165">If the computer is already encrypted, BitLocker protection is not suspended.</span></span> <span data-ttu-id="8b797-166">Wenn der Computer nicht verschlüsselt ist, fordert MBAM den Benutzer nicht auf zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="8b797-166">If the computer is not encrypted, MBAM does not prompt the user to encrypt.</span></span>

    **<span data-ttu-id="8b797-167">Wichtig</span><span class="sxs-lookup"><span data-stu-id="8b797-167">Important</span></span>**  
    <span data-ttu-id="8b797-168">Szenarien mit freigegebenen Computern erfordern besondere Berücksichtigung, wenn Sie BitLocker-Benutzer Ausnahmen verwenden.</span><span class="sxs-lookup"><span data-stu-id="8b797-168">Shared computer scenarios require special consideration when you are using BitLocker user exemptions.</span></span> <span data-ttu-id="8b797-169">Wenn sich ein nicht ausgenommener Benutzer an einem Computer anmeldet, der für einen ausgenommenen Benutzer freigegeben wurde, kann der Computer verschlüsselt sein.</span><span class="sxs-lookup"><span data-stu-id="8b797-169">If a non-exempt user signs in to a computer that is shared with an exempt user, the computer may be encrypted.</span></span>




## <span data-ttu-id="8b797-170">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="8b797-170">Related topics</span></span>


[<span data-ttu-id="8b797-171">Verwalten von MBAM 2.5-Funktionen</span><span class="sxs-lookup"><span data-stu-id="8b797-171">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)

[<span data-ttu-id="8b797-172">Planen der Gruppenrichtlinienanforderungen für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8b797-172">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)




## <span data-ttu-id="8b797-173">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="8b797-173">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8b797-174">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="8b797-174">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="8b797-175">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8b797-175">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




