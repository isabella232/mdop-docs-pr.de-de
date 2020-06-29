---
title: Authentifizierung von MED-V-Endbenutzern
description: Authentifizierung von MED-V-Endbenutzern
author: dansimp
ms.assetid: aaf96eb6-91d1-4f4d-9854-5fc73c7ae7ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14c1e95a94f2da76b6b6c5ebd9d4cf14dcf839a7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810825"
---
# <span data-ttu-id="75dd4-103">Authentifizierung von MED-V-Endbenutzern</span><span class="sxs-lookup"><span data-stu-id="75dd4-103">Authentication of MED-V End Users</span></span>


<span data-ttu-id="75dd4-104">Die Authentifizierung von Microsoft Enterprise Desktop Virtualization (MED-V) 2,0-Endbenutzern ist ein sehr wichtiges Sicherheitsproblem.</span><span class="sxs-lookup"><span data-stu-id="75dd4-104">The authentication of Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 end users is a very important security issue.</span></span> <span data-ttu-id="75dd4-105">In diesem Kontext bezieht sich die Authentifizierung auf die Überprüfung der Identität des MED-V-Endbenutzers.</span><span class="sxs-lookup"><span data-stu-id="75dd4-105">In this context, authentication refers to verifying the identity of the MED-V end user.</span></span>

<span data-ttu-id="75dd4-106">Der folgende Abschnitt enthält Informationen und Anleitungen zur Endbenutzer Authentifizierung in MED-V.</span><span class="sxs-lookup"><span data-stu-id="75dd4-106">The following section provides information and guidance about end-user authentication in MED-V.</span></span>

## <span data-ttu-id="75dd4-107">Benutzerauthentifizierung in MED-V</span><span class="sxs-lookup"><span data-stu-id="75dd4-107">User Authentication in MED-V</span></span>


<span data-ttu-id="75dd4-108">Die Authentifizierung in Med-v erfolgt in der Regel auf zwei Ebenen: Wenn ein Benutzer zuerst auf Med-v und jedes Mal, wenn er sein Kennwort ändert, zugreift.</span><span class="sxs-lookup"><span data-stu-id="75dd4-108">Authentication in MED-V generally occurs at two levels: when a user first accesses MED-V and every time that they change their password.</span></span>

<span data-ttu-id="75dd4-109">Je nachdem, wie Sie die Med-v-Einstellungen für die Authentifizierung konfiguriert haben, wird der Endbenutzer in der Regel irgendwann aufgefordert, sein Kennwort einzugeben, entweder beim ersten Start von Med-v oder beim ersten Versuch, eine veröffentlichte Anwendung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="75dd4-109">Depending on how you have configured MED-V settings for authentication, the end user is typically prompted at some point to enter their password, either the first time MED-V is started or the first time that they try to open a published application.</span></span>

<span data-ttu-id="75dd4-110">Es gibt verschiedene Aspekte der Endbenutzer Authentifizierung, die Sie steuern können, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="75dd4-110">There are several aspects of end-user authentication that you can control, including the following:</span></span>

<span data-ttu-id="75dd4-111">Ob die Anmeldeinformationen, die der Endbenutzer eingibt, im Anmelde Informations-Manager gespeichert werden</span><span class="sxs-lookup"><span data-stu-id="75dd4-111">Whether the credentials the end user enters are stored in Credential Manager</span></span>

<span data-ttu-id="75dd4-112">In welcher Weise wird dem Endnutzer die Möglichkeit geboten, sein Kennwort einzugeben und zu speichern</span><span class="sxs-lookup"><span data-stu-id="75dd4-112">In what manner the end user is presented with the option of entering and saving their password</span></span>

<span data-ttu-id="75dd4-113">Je nach dem bevorzugten Prozess des Unternehmens für die Verwaltung der Endbenutzer Authentifizierung können Sie angeben, ob die Zwischenspeicherung von Anmeldeinformationen für einen bestimmten MED-V-Arbeitsbereich erfolgt.</span><span class="sxs-lookup"><span data-stu-id="75dd4-113">Depending on your company’s preferred process for managing end-user authentication, you can specify whether credential caching occurs for a particular MED-V workspace.</span></span> <span data-ttu-id="75dd4-114">Das Zwischenspeichern der Anmeldeinformationen eines Endbenutzers ist hilfreich, da er nur einmal für sein Kennwort aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="75dd4-114">Caching the credentials of an end user is helpful because they are only prompted one time for their password.</span></span> <span data-ttu-id="75dd4-115">Wenn es dem Endbenutzer nicht gestattet ist, sein Kennwort zu speichern oder nicht, jedes Mal, wenn Sie eine neue MED-V-Sitzung starten, müssen Sie es erneut eingeben.</span><span class="sxs-lookup"><span data-stu-id="75dd4-115">If the end user is not allowed to save their password or they decide not to, every time that they start a new MED-V session, they must enter it again.</span></span> <span data-ttu-id="75dd4-116">Wenn beispielsweise MED-V so konfiguriert ist, dass er gestartet wird, wenn sich der Endbenutzer beim Host anmeldet, die Authentifizierung aber deaktiviert ist, wird der Endbenutzer nur einmal während der Anmeldung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="75dd4-116">For example, if MED-V is configured to start when the end user logs on to the host but Authentication is disabled, the end user is only prompted one time during logon.</span></span> <span data-ttu-id="75dd4-117">In diesem Fall sind Anmeldeinformationen gültig, bis sich der Endbenutzer vom Host abmeldet.</span><span class="sxs-lookup"><span data-stu-id="75dd4-117">In this case, credentials are valid until the end user logs off from the host.</span></span>

<span data-ttu-id="75dd4-118">Wenn dies erforderlich ist, können Sie mithilfe des Anmelde Informations-Managers alle gespeicherten Endbenutzeranmeldeinformationen entfernen.</span><span class="sxs-lookup"><span data-stu-id="75dd4-118">If it is necessary, you can use Credential Manager to remove any stored end-user credentials.</span></span>

<span data-ttu-id="75dd4-119">Standardmäßig ist die Speicherung von Anmeldeinformationen deaktiviert, doch Sie können diese Einstellung mithilfe einer der folgenden Methoden ändern:</span><span class="sxs-lookup"><span data-stu-id="75dd4-119">By default, credential storing is disabled, but you can change this setting through one of the following methods:</span></span>

<span data-ttu-id="75dd4-120">**Während des Erstellens des MED-V-Arbeitsbereichs Pakets**.</span><span class="sxs-lookup"><span data-stu-id="75dd4-120">**While you are creating the MED-V workspace package**.</span></span> <span data-ttu-id="75dd4-121">Weitere Informationen finden Sie unter [Erstellen eines MED-V-Arbeitsbereichs Pakets](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="75dd4-121">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

<span data-ttu-id="75dd4-122">**Nachdem Sie den MED-V-Arbeitsbereich bereitgestellt haben**.</span><span class="sxs-lookup"><span data-stu-id="75dd4-122">**After you have deployed the MED-V workspace**.</span></span> <span data-ttu-id="75dd4-123">Bearbeiten Sie den Parameter UxCredentialCacheEnabled des MED-V-Cmdlets, um den Registrierungsschlüssel für die Terminal Dienste einzurichten.</span><span class="sxs-lookup"><span data-stu-id="75dd4-123">Edit the MED-V cmdlet parameter UxCredentialCacheEnabled to set the Terminal Services registry key.</span></span> <span data-ttu-id="75dd4-124">Weitere Informationen finden Sie in der Hilfe zu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="75dd4-124">For more information, see Windows PowerShell Help.</span></span>

<span data-ttu-id="75dd4-125">Nach der Bereitstellung von MED-V Workspace können Sie Ihre Präferenz für die Endbenutzer Authentifizierung festlegen, indem Sie die Terminal Dienste-Richtlinie mit dem Namen DisablePasswordSaving ändern.</span><span class="sxs-lookup"><span data-stu-id="75dd4-125">After MED-V workspace deployment, you can set your preference for end-user authentication by modifying the Terminal Services policy named DisablePasswordSaving.</span></span> <span data-ttu-id="75dd4-126">DisablePasswordSaving steuert, ob das Kontrollkästchen Kennwort speichern im Dialogfenster des RDP-Clients angezeigt wird und ob die Eingabeaufforderung MED-V-Anmeldeinformationen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="75dd4-126">DisablePasswordSaving controls whether the password saving check box appears on the RDP client dialog window and whether the MED-V credential prompt is displayed.</span></span>

<span data-ttu-id="75dd4-127">Im folgenden wird der Richtlinienpfad für die Terminal Dienste-Richtlinie mit dem Namen DisablePasswordSaving.</span><span class="sxs-lookup"><span data-stu-id="75dd4-127">Following is the policy path for the Terminal Services policy named DisablePasswordSaving.</span></span>

**<span data-ttu-id="75dd4-128">Regedit</span><span class="sxs-lookup"><span data-stu-id="75dd4-128">Regedit:</span></span>**

<span data-ttu-id="75dd4-129">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\virtual Machine\\Policies\\DisablePasswordSaving</span><span class="sxs-lookup"><span data-stu-id="75dd4-129">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Policies\\DisablePasswordSaving</span></span>

**<span data-ttu-id="75dd4-130">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="75dd4-130">Note</span></span>**  
<span data-ttu-id="75dd4-131">Die Änderungen, die Sie an DisablePasswordSaving vornehmen, wirken sich nur auf die RDP-Eingabeaufforderung für einen virtuellen Computer aus.</span><span class="sxs-lookup"><span data-stu-id="75dd4-131">The changes that you make to DisablePasswordSaving only affect the RDP prompt to a virtual machine.</span></span>



<span data-ttu-id="75dd4-132">In der folgenden Tabelle sind die verschiedenen Möglichkeiten für die Konfiguration Ihrer Einstellungen für die Speicherung von Anmeldeinformationen und die Auswirkungen der verschiedenen Konfigurationen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="75dd4-132">The following table lists the different ways you can configure your settings for credential storing and the effects of the different configurations:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="75dd4-133">Wert</span><span class="sxs-lookup"><span data-stu-id="75dd4-133">Value</span></span></th>
<th align="left"><span data-ttu-id="75dd4-134">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="75dd4-134">Configuration</span></span></th>
<th align="left"><span data-ttu-id="75dd4-135">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="75dd4-135">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="75dd4-136">DisablePasswordSaving</span><span class="sxs-lookup"><span data-stu-id="75dd4-136">DisablePasswordSaving</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="75dd4-137">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="75dd4-137">Disabled</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="75dd4-138">Die MED-V-Eingabeaufforderung wird angezeigt, und ein Kontrollkästchen zum annehmen ist verfügbar und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="75dd4-138">The MED-V prompt is presented and a check box to accept is available and cleared.</span></span> <span data-ttu-id="75dd4-139">Wenn der Endbenutzer das Kontrollkästchen aktiviert, werden die Anmeldeinformationen für die spätere Verwendung zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="75dd4-139">If the end user selects the check box, credentials are cached for subsequent use.</span></span> <span data-ttu-id="75dd4-140">Der Endbenutzer hat außerdem den Vorteil, dass nur eine Aufforderung angezeigt wird, wenn das Kennwort abläuft.</span><span class="sxs-lookup"><span data-stu-id="75dd4-140">The end user also has the benefit of only being prompted when the password expires.</span></span></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="75dd4-141">Wenn der Endbenutzer das Kontrollkästchen nicht aktiviert, wird anstelle der MED-V-Eingabeaufforderung die RDC-Client Aufforderung (Remote Desktop Connection) angezeigt, und das Kontrollkästchen zum annehmen wird deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="75dd4-141">If the end user does not select the check box, the Remote Desktop Connection (RDC) Client prompt is presented instead of the MED-V prompt, and the check box to accept is cleared.</span></span> <span data-ttu-id="75dd4-142">Wenn der Endbenutzer das Kontrollkästchen aktiviert, werden die RDC-Client Anmeldeinformationen für die spätere Verwendung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="75dd4-142">If the end user selects the check box, the RDC Client credential is stored for later use.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="75dd4-143">Wichtig</span><span class="sxs-lookup"><span data-stu-id="75dd4-143">Important</span></span></strong><br/><p><span data-ttu-id="75dd4-144">RDC überprüft keine Anmeldeinformationen, wenn der Endbenutzer Sie eingibt.</span><span class="sxs-lookup"><span data-stu-id="75dd4-144">RDC does not validate credentials when the end user enters them.</span></span> <span data-ttu-id="75dd4-145">Wenn der Endbenutzer die Anmeldeinformationen über die RDC-Eingabeaufforderung zwischenspeichert, besteht das Risiko, dass falsche Anmeldeinformationen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="75dd4-145">If the end user caches the credentials through the RDC prompt, there is a risk that incorrect credentials might be stored.</span></span> <span data-ttu-id="75dd4-146">In diesem Fall müssen die falschen Anmeldeinformationen im Windows-Anmelde Informations-Manager gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="75dd4-146">In this case, the incorrect credentials must be deleted in the Windows Credential Manager.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="75dd4-147">DisablePasswordSaving</span><span class="sxs-lookup"><span data-stu-id="75dd4-147">DisablePasswordSaving</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="75dd4-148">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="75dd4-148">Enabled</span></span></strong></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="75dd4-149">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="75dd4-149">Note</span></span></strong><br/><p><span data-ttu-id="75dd4-150">Diese Konfiguration ist sicherer, da Sie die Zwischenspeicherung von Endbenutzeranmeldeinformationen nicht zulässt.</span><span class="sxs-lookup"><span data-stu-id="75dd4-150">This configuration is more secure because it does not allow end user credentials to be cached.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="75dd4-151">Standardmäßig legt die MED-V-Installation einen Registrierungsschlüssel im Gast fest, um die Eingabeaufforderung "Kennwort läuft ab" zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="75dd4-151">By default, the MED-V installation sets a registry key in the guest to suppress the "password about to expire" prompt.</span></span> <span data-ttu-id="75dd4-152">Der Endbenutzer wird nur zur Eingabe einer Kennwortänderung auf dem Host aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="75dd4-152">The end user is only prompted for a password change on the host.</span></span> <span data-ttu-id="75dd4-153">Die auf dem Host aktualisierten Anmeldeinformationen werden an den Gast weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="75dd4-153">Credentials that are updated on the host are passed to the guest.</span></span>

**<span data-ttu-id="75dd4-154">Achtung</span><span class="sxs-lookup"><span data-stu-id="75dd4-154">Caution</span></span>**  
<span data-ttu-id="75dd4-155">Wenn Sie Gruppenrichtlinien in Ihrer Umgebung verwenden, wissen Sie, dass der Registrierungsschlüssel außer Kraft gesetzt werden kann, wodurch die Kennworteingabeaufforderung des Gasts wieder angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="75dd4-155">If you use Group Policy in your environment, know that it can override the registry key causing the password prompts from the guest to reappear.</span></span>



### <span data-ttu-id="75dd4-156">Sicherheitsaspekte bei der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="75dd4-156">Security Concerns with Authentication</span></span>

<span data-ttu-id="75dd4-157">Auch wenn die Zwischenspeicherung der Anmeldeinformationen des Endbenutzers die beste Benutzererfahrung bietet, müssen Sie sich mit den damit verbundenen Risiken vertraut machen.</span><span class="sxs-lookup"><span data-stu-id="75dd4-157">Even though caching the end user’s credentials provides the best user experience, you must be aware of the risks involved.</span></span>

<span data-ttu-id="75dd4-158">Wenn die Zwischenspeicherung von Anmeldeinformationen aktiviert ist, werden die Domänenanmeldeinformationen des Endbenutzers in einem reversiblen Format innerhalb des Windows-Anmelde Informations-Managers gespeichert.</span><span class="sxs-lookup"><span data-stu-id="75dd4-158">When credential caching is enabled, the end user’s domain credential is stored in a reversible format within the Windows Credential Manager.</span></span> <span data-ttu-id="75dd4-159">Infolgedessen kann ein Angreifer ein Tool schreiben, das entweder als Prozess auf Systemebene oder als Endbenutzer Prozess ausgeführt wird und die Anmeldeinformationen des Endbenutzers abruft.</span><span class="sxs-lookup"><span data-stu-id="75dd4-159">As a result, an attacker could write a tool that runs as either a system level process or an end user process and that retrieves the end user's credentials.</span></span> <span data-ttu-id="75dd4-160">Sie können dieses Risiko nur verringern, indem Sie DisablePasswordSaving auf **Enabled**festlegen.</span><span class="sxs-lookup"><span data-stu-id="75dd4-160">You can only lessen this risk by setting DisablePasswordSaving to **Enabled**.</span></span>

<span data-ttu-id="75dd4-161">Das gleiche Problem tritt auf, wenn die MED-V-Authentifizierung deaktiviert ist, die Einstellung für die Terminal Dienste-Richtlinie jedoch aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="75dd4-161">This same concern exists when MED-V authentication is disabled but the Terminal Services policy setting is enabled.</span></span>

## <span data-ttu-id="75dd4-162">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="75dd4-162">Related topics</span></span>


[<span data-ttu-id="75dd4-163">Bewährte Sicherheitsmethoden für MED-V-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="75dd4-163">Security Best Practices for MED-V Operations</span></span>](security-best-practices-for-med-v-operations.md)









