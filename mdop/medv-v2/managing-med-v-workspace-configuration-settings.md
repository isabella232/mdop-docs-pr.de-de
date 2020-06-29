---
title: Verwalten von Konfigurationseinstellungen für MED-V-Arbeitsbereiche
description: Verwalten von Konfigurationseinstellungen für MED-V-Arbeitsbereiche
author: dansimp
ms.assetid: 517d04de-c31f-4b50-b2b3-5f8c312ed37b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97add695f605b71547b564789cce07a1d58763f2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811587"
---
# <span data-ttu-id="fa068-103">Verwalten von Konfigurationseinstellungen für MED-V-Arbeitsbereiche</span><span class="sxs-lookup"><span data-stu-id="fa068-103">Managing MED-V Workspace Configuration Settings</span></span>


<span data-ttu-id="fa068-104">Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 speichert die Konfigurationseinstellungen in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="fa068-104">Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 stores its configuration settings in the registry.</span></span> <span data-ttu-id="fa068-105">Die Informationen, die wir hier zur Registrierung einfügen, können Ihnen helfen, ihre MED-V-Dienste besser zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="fa068-105">The information we include here about the registry may help you better manage your MED-V services.</span></span>

<span data-ttu-id="fa068-106">MED-V verwendet den folgenden Suchpfad, wenn Sie nach den resultierenden Einstellungswerten suchen:</span><span class="sxs-lookup"><span data-stu-id="fa068-106">MED-V uses the following search path when looking for the resultant settings values:</span></span>

<span data-ttu-id="fa068-107">MED-V sucht zunächst in der Computerrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="fa068-107">MED-V first looks in the machine policy.</span></span>

<span data-ttu-id="fa068-108">Wenn der Wert nicht gefunden wird, sucht MED-V in der Benutzerrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="fa068-108">If the value is not found, MED-V looks in the user policy.</span></span>

<span data-ttu-id="fa068-109">Wenn der Wert nicht gefunden wird, sucht MED-V in der HKEY \ _LOCAL \ _MACHINE \\system-Struktur.</span><span class="sxs-lookup"><span data-stu-id="fa068-109">If the value is not found, MED-V looks in the HKEY\_LOCAL\_MACHINE\\System hive.</span></span>

<span data-ttu-id="fa068-110">Wenn der Wert nicht gefunden wird, sucht MED-V in der HKEY \ _CURRENT Benutzer Registrierungsstruktur.</span><span class="sxs-lookup"><span data-stu-id="fa068-110">If the value is not found, MED-V looks in the HKEY\_CURRENT USER registry hive.</span></span>

<span data-ttu-id="fa068-111">Wenn der Wert immer noch nicht gefunden wird, verwendet MED-V den Standardwert.</span><span class="sxs-lookup"><span data-stu-id="fa068-111">If the value is still not found, MED-V uses the default.</span></span>

<span data-ttu-id="fa068-112">Eine allgemeine bewährte Vorgehensweise besteht darin, den Wert im HKEY \ _LOCAL \ _MACHINE \\system-Hive oder in der Computerrichtlinie zu definieren.</span><span class="sxs-lookup"><span data-stu-id="fa068-112">A general best practice is to set the value in the HKEY\_LOCAL\_MACHINE\\System hive or in the machine policy.</span></span> <span data-ttu-id="fa068-113">Wenn der Endbenutzer jedoch in der Lage sein soll, eine bestimmte Einstellung zu konfigurieren, sollten Sie ihn verlassen.</span><span class="sxs-lookup"><span data-stu-id="fa068-113">But if you want the end user to be able to configure a particular setting, then you should leave it out.</span></span>

**<span data-ttu-id="fa068-114">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="fa068-114">Note</span></span>**  
<span data-ttu-id="fa068-115">Bevor Sie Ihre Med-v-Arbeitsbereiche bereitstellen, können Sie ein Skript-Editor verwenden, um das Windows PowerShell-Skript (PS1-Datei) zu ändern, das vom Med-v-Arbeitsbereichs Paket erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="fa068-115">Before you deploy your MED-V workspaces, you can use a script editor to change the Windows PowerShell script (.ps1 file) that the MED-V workspace packager created.</span></span> <span data-ttu-id="fa068-116">Weitere Informationen finden Sie unter [Konfigurieren von erweiterten Einstellungen mithilfe von Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="fa068-116">For more information, see [Configuring Advanced Settings by Using Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).</span></span>

<span data-ttu-id="fa068-117">Nachdem Sie Ihre Med-v-Arbeitsbereiche bereitgestellt haben, können Sie bestimmte Med-v-Konfigurationseinstellungen ändern, indem Sie die Registrierungseinträge bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="fa068-117">After you have deployed your MED-V workspaces, you can change certain MED-V configuration settings by editing the registry entries.</span></span>



<span data-ttu-id="fa068-118">In diesem Abschnitt werden alle konfigurierbaren MED-V-Registrierungsschlüssel aufgelistet und deren Verwendung erläutert.</span><span class="sxs-lookup"><span data-stu-id="fa068-118">This section lists all the configurable MED-V registry keys and explains their uses.</span></span>

## <span data-ttu-id="fa068-119">Diagnoseschlüssel</span><span class="sxs-lookup"><span data-stu-id="fa068-119">Diagnostics Key</span></span>


<span data-ttu-id="fa068-120">Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die mit dem HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\medv\\v2\\diagnostics-Schlüssel verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="fa068-120">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\Diagnostics key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa068-121">Name</span><span class="sxs-lookup"><span data-stu-id="fa068-121">Name</span></span> </th>
<th align="left"><span data-ttu-id="fa068-122">Typ</span><span class="sxs-lookup"><span data-stu-id="fa068-122">Type</span></span> </th>
<th align="left"><span data-ttu-id="fa068-123">Daten/Standard</span><span class="sxs-lookup"><span data-stu-id="fa068-123">Data/Default</span></span> </th>
<th align="left"><span data-ttu-id="fa068-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa068-124">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-125">EventLogLevel</span><span class="sxs-lookup"><span data-stu-id="fa068-125">EventLogLevel</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-126">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-126">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-127">Standard = 3</span><span class="sxs-lookup"><span data-stu-id="fa068-127">Default=3</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-128">Der Typ der Informationen, die im Ereignisprotokoll protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="fa068-128">The type of information that is logged in the event log.</span></span> <span data-ttu-id="fa068-129">Zu den Ebenen gehören die folgenden: 0 (keine), 1 (Fehler), 2 (Warnung), 3 (Informationen), 4 (Debug).</span><span class="sxs-lookup"><span data-stu-id="fa068-129">Levels include the following: 0 (None), 1 (Error), 2 (Warning), 3 (Information), 4 (Debug).</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="fa068-130">FTS-Taste</span><span class="sxs-lookup"><span data-stu-id="fa068-130">Fts Key</span></span>


<span data-ttu-id="fa068-131">Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die mit dem HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\medv\\v2\\fts-Schlüssel verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="fa068-131">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\Fts key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa068-132">Name</span><span class="sxs-lookup"><span data-stu-id="fa068-132">Name</span></span></th>
<th align="left"><span data-ttu-id="fa068-133">Typ</span><span class="sxs-lookup"><span data-stu-id="fa068-133">Type</span></span></th>
<th align="left"><span data-ttu-id="fa068-134">Daten/Standard</span><span class="sxs-lookup"><span data-stu-id="fa068-134">Data/Default</span></span></th>
<th align="left"><span data-ttu-id="fa068-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa068-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-136">AddUserToAdminGroupEnabled</span><span class="sxs-lookup"><span data-stu-id="fa068-136">AddUserToAdminGroupEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-137">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-137">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-138">Standard = 0</span><span class="sxs-lookup"><span data-stu-id="fa068-138">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-139">Konfiguriert, ob der Endbenutzer von der erstmaligen Einrichtung automatisch zur Gruppe Administrator&#39;s hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="fa068-139">Configures whether first time setup automatically adds the end user to the administrator&#39;s group.</span></span> <span data-ttu-id="fa068-140">0 = falsch; 1 = wahr.</span><span class="sxs-lookup"><span data-stu-id="fa068-140">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-141">0 = falsch: bei der erstmaligen Einrichtung wird der Endbenutzer nicht automatisch zur Gruppe Administrator&#39;s hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fa068-141">0 = false: First time setup does not automatically add the end user to the administrator&#39;s group.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-142">1 = wahr: bei der erstmaligen Einrichtung wird der Endbenutzer automatisch zur Gruppe Administrator&#39;s hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fa068-142">1 = true: First time setup automatically adds the end user to the administrator&#39;s group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-143">ComputerNameMask</span><span class="sxs-lookup"><span data-stu-id="fa068-143">ComputerNameMask</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-144">SZ</span><span class="sxs-lookup"><span data-stu-id="fa068-144">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-145">MEDV</span><span class="sxs-lookup"><span data-stu-id="fa068-145">MEDV\*</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-146">Die Computernamen Maske, die zum Erstellen des virtuellen Gastcomputers verwendet wird&#39;s-Computername.</span><span class="sxs-lookup"><span data-stu-id="fa068-146">The computer name mask that is used to create the guest virtual machine&#39;s computer name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-147">Die Maske kann einen% username%-Tag enthalten, um den Benutzernamen als Teil des Computernamens einzufügen.</span><span class="sxs-lookup"><span data-stu-id="fa068-147">The mask can contain a %username% tag to insert the username as part of the computer name.</span></span> <span data-ttu-id="fa068-148">Ebenso fügt das Tag% Hostname% den Namen des Hostcomputers ein.</span><span class="sxs-lookup"><span data-stu-id="fa068-148">Likewise, the %hostname% tag inserts the name of the host computer.</span></span></p>
<p><span data-ttu-id="fa068-149">Jedes &quot; # &quot; Zeichen in der Maske wird durch eine Zufallszahl ersetzt.</span><span class="sxs-lookup"><span data-stu-id="fa068-149">Every &quot;#&quot; character in the mask is replaced by a random digit.</span></span> <span data-ttu-id="fa068-150">Ein Sternchen (\*)-Zeichen am Ende der Maske wird durch zufällige alphanumerische Zeichen ersetzt.</span><span class="sxs-lookup"><span data-stu-id="fa068-150">An asterisk (\*) character at the end of the mask is replaced by random alphanumeric characters.</span></span></p>
<p><span data-ttu-id="fa068-151">Eine bestimmte Anzahl von Zeichen aus% Hostname% und% username% kann mithilfe von eckigen Klammern erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="fa068-151">A specific number of characters from %hostname% and %username% can be captured by using square brackets.</span></span> <span data-ttu-id="fa068-152">Beispielsweise &quot; würden% username% [3] &quot; die ersten drei Zeichen des Nutzernamens verwenden.</span><span class="sxs-lookup"><span data-stu-id="fa068-152">For example, &quot;%username%[3]&quot; would use the first three characters of the username.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-153">DeleteVMStateTimeout</span><span class="sxs-lookup"><span data-stu-id="fa068-153">DeleteVMStateTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-154">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-154">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-155">Standard = 90</span><span class="sxs-lookup"><span data-stu-id="fa068-155">Default=90</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-156">Der Timeoutwert in Sekunden, wenn die erstmalige Einrichtung versucht, den virtuellen Computer zu löschen.</span><span class="sxs-lookup"><span data-stu-id="fa068-156">The time-out value, in seconds, when first time setup tries to delete the virtual machine.</span></span> <span data-ttu-id="fa068-157">Bereich = 0 bis 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fa068-157">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-158">DetachVfdTimeout</span><span class="sxs-lookup"><span data-stu-id="fa068-158">DetachVfdTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-159">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-159">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-160">Standard = 120</span><span class="sxs-lookup"><span data-stu-id="fa068-160">Default=120</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-161">Der Timeoutwert in Sekunden, wenn die erstmalige Einrichtung versucht, die virtuelle Diskette vom virtuellen Computer zu trennen.</span><span class="sxs-lookup"><span data-stu-id="fa068-161">The time-out value, in seconds, when first time setup tries to detach the virtual floppy disk from the virtual machine.</span></span> <span data-ttu-id="fa068-162">Bereich = 0 bis 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fa068-162">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-163">DialogUrl</span><span class="sxs-lookup"><span data-stu-id="fa068-163">DialogUrl</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-164">SZ</span><span class="sxs-lookup"><span data-stu-id="fa068-164">SZ</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-165">Anpassbare URL, die mit der internen Webseite verknüpft ist und beim erstmaligen Einrichten von Dialog Meldungen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fa068-165">Customizable URL that links to internal webpage and is displayed by first time setup dialog messages.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-166">ExplorerTimeout</span><span class="sxs-lookup"><span data-stu-id="fa068-166">ExplorerTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-167">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-167">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-168">Standard = 900</span><span class="sxs-lookup"><span data-stu-id="fa068-168">Default=900</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-169">Der Timeoutwert in Sekunden, bei dem das erstmalige Setup auf den Windows-Explorer wartet.</span><span class="sxs-lookup"><span data-stu-id="fa068-169">The time-out value, in seconds, that first time setup waits for Windows Explorer.</span></span> <span data-ttu-id="fa068-170">Bereich = 0 bis 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fa068-170">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-171">FailureDialogMsg</span><span class="sxs-lookup"><span data-stu-id="fa068-171">FailureDialogMsg</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-172">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="fa068-172">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-173">Nachricht wird in der Ressourcendatei gefunden</span><span class="sxs-lookup"><span data-stu-id="fa068-173">Message is found in resource file</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-174">Anpassbare Nachricht, die dem Endbenutzer angezeigt wird, wenn die erstmalige Einrichtung nicht abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="fa068-174">Customizable message that is displayed to the end user when first time setup cannot be completed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-175">GiveUserGroupRightsMaxRetryCount</span><span class="sxs-lookup"><span data-stu-id="fa068-175">GiveUserGroupRightsMaxRetryCount</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-176">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-176">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-177">Standard = 3</span><span class="sxs-lookup"><span data-stu-id="fa068-177">Default=3</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-178">Die maximale Anzahl von MED-V, die versucht, einer Endbenutzergruppe Rechte zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="fa068-178">The maximum number of times that MED-V tries to give an end user group rights.</span></span> <span data-ttu-id="fa068-179">Wenn der angegebene Retry-Wert überschritten wird, ohne dass die Benutzergruppenrechte erfolgreich vergeben werden können, führt dies wahrscheinlich zu einem Fehler bei der Vorbereitung einer virtuellen Maschine, der dann dem MaxRetryCount-Wert unterliegt.</span><span class="sxs-lookup"><span data-stu-id="fa068-179">Exceeding the specified retry value without being able to successfully give an end user group rights most likely causes a virtual machine preparation failure that is then subject to the MaxRetryCount value.</span></span> <span data-ttu-id="fa068-180">Bereich = 0 bis 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fa068-180">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-181">GiveUserGroupRightsTimeout</span><span class="sxs-lookup"><span data-stu-id="fa068-181">GiveUserGroupRightsTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-182">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-182">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-183">Standard = 300</span><span class="sxs-lookup"><span data-stu-id="fa068-183">Default=300</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-184">Der Timeoutwert in Sekunden, wenn einem Benutzergruppenrechte erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="fa068-184">The time-out value, in seconds, when giving a user group rights.</span></span> <span data-ttu-id="fa068-185">Bereich = 0 bis 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fa068-185">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-186">LogFilePaths</span><span class="sxs-lookup"><span data-stu-id="fa068-186">LogFilePaths</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-187">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="fa068-187">MULTI_SZ</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-188">Eine Liste der Protokolldateipfade, die von MED-V bei der erstmaligen Einrichtung erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="fa068-188">A list of the log file paths that MED-V collects during first time setup.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-189">MaxPostponeTime</span><span class="sxs-lookup"><span data-stu-id="fa068-189">MaxPostponeTime</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-190">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-190">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-191">Standard = 120</span><span class="sxs-lookup"><span data-stu-id="fa068-191">Default=120</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-192">Die maximale Anzahl von Stunden, die vom Endbenutzer zum erstmaligen Einrichten verschoben werden können.</span><span class="sxs-lookup"><span data-stu-id="fa068-192">The maximum number of hours that first time setup can be postponed by the end user.</span></span> <span data-ttu-id="fa068-193">Bereich = 0 bis 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fa068-193">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-194">MaxRetryCount</span><span class="sxs-lookup"><span data-stu-id="fa068-194">MaxRetryCount</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-195">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-195">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-196">Standard = 3</span><span class="sxs-lookup"><span data-stu-id="fa068-196">Default=3</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-197">Die maximale Anzahl von MED-V, die versucht, einen virtuellen Computer vorzubereiten, wenn jeder Versuch mit einem anderen Fehler als einem Softwarefehler endet.</span><span class="sxs-lookup"><span data-stu-id="fa068-197">The maximum number of times that MED-V tries to prepare a virtual machine if each attempt ends in a failure other than a software error.</span></span> <span data-ttu-id="fa068-198">Wenn die Vorbereitung der virtuellen Maschine fehlschlägt und die Anzahl der Neuversuche beim erstmaligen Setup überschritten wird, informiert MED-V den Endbenutzer über den Fehler und gibt keine Möglichkeit zum erneuten Versuch.</span><span class="sxs-lookup"><span data-stu-id="fa068-198">When virtual machine preparation fails and the number of first time setup retries is exceeded, then MED-V informs the end user about the failure and does not give the option to retry.</span></span> <span data-ttu-id="fa068-199">Die Anzahl wird jedes Mal neu festgesetzt, wenn MED-V gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="fa068-199">The count is re-set every time that MED-V is started.</span></span> <span data-ttu-id="fa068-200">Bereich = 0 bis 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fa068-200">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-201">Modus</span><span class="sxs-lookup"><span data-stu-id="fa068-201">Mode</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-202">SZ</span><span class="sxs-lookup"><span data-stu-id="fa068-202">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-203">Standard = unbeaufsichtigt</span><span class="sxs-lookup"><span data-stu-id="fa068-203">Default=Unattended</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-204">Konfiguriert, wie das erstmalige Setup mit dem Benutzer interagiert.</span><span class="sxs-lookup"><span data-stu-id="fa068-204">Configures how first time setup interacts with the user.</span></span> <span data-ttu-id="fa068-205">Mögliche Werte lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fa068-205">Possible values are as follows:</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="fa068-206">Teilgenommen.</span><span class="sxs-lookup"><span data-stu-id="fa068-206">Attended.</span></span></strong> <span data-ttu-id="fa068-207">Der Endbenutzer muss während der erstmaligen Einrichtung Informationen eingeben.</span><span class="sxs-lookup"><span data-stu-id="fa068-207">The end user must enter information during first time setup.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="fa068-208">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="fa068-208">Note</span></span></strong><br/><p><span data-ttu-id="fa068-209">Wenn Sie die Datei "Sysprep. inf" erstellt haben, damit für das Mini Setup eine Benutzereingabe erforderlich ist, müssen Sie den <strong> beaufsichtigten Modus auswählen, </strong> oder es können Probleme beim erstmaligen Einrichten auftreten.</span><span class="sxs-lookup"><span data-stu-id="fa068-209">If you created the Sysprep.inf file so that Mini-Setup requires user input to complete, then you must select <strong>Attended</strong> mode or problems might occur during first time setup.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="fa068-210">Unbeaufsichtigt </strong> .</span><span class="sxs-lookup"><span data-stu-id="fa068-210">Unattended</strong>.</span></span> <span data-ttu-id="fa068-211">Der virtuelle Computer wird dem Endbenutzer während der erstmaligen Einrichtung nicht angezeigt, aber der Endbenutzer wird vor dem erstmaligen Setup aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="fa068-211">The virtual machine is not shown to the end user during first time setup, but the end user is prompted before first time setup starts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="fa068-212">Stumm </strong> .</span><span class="sxs-lookup"><span data-stu-id="fa068-212">Silent</strong>.</span></span> <span data-ttu-id="fa068-213">Der virtuelle Computer wird dem Endbenutzer während der erstmaligen Einrichtung überhaupt nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fa068-213">The virtual machine is not shown to the end user at all during first time setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-214">NonInteractiveRetryTimeoutInc</span><span class="sxs-lookup"><span data-stu-id="fa068-214">NonInteractiveRetryTimeoutInc</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-215">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-215">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-216">Standard = 15</span><span class="sxs-lookup"><span data-stu-id="fa068-216">Default=15</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-217">Der Timeoutwert in Minuten, bei dem das erstmalige Einrichten im interaktiven Modus zum erstmaligen Einrichten abgeschlossen werden muss, wenn das Setup erneut versucht wird.</span><span class="sxs-lookup"><span data-stu-id="fa068-217">The time-out value, in minutes, that first time setup must be completed in first time setup interactive mode when re-attempting setup.</span></span> <span data-ttu-id="fa068-218">Bereich = 0 bis 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fa068-218">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-219">NonInteractiveTimeout</span><span class="sxs-lookup"><span data-stu-id="fa068-219">NonInteractiveTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-220">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-220">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-221">Standard = 45</span><span class="sxs-lookup"><span data-stu-id="fa068-221">Default=45</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-222">Der Timeoutwert in Minuten, bei dem das erstmalige Einrichten im interaktiven Modus für die erstmalige Einrichtung abgeschlossen sein muss.</span><span class="sxs-lookup"><span data-stu-id="fa068-222">The time-out value, in minutes, that first time setup must be completed in first time setup interactive mode.</span></span> <span data-ttu-id="fa068-223">Bereich = 0 bis 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fa068-223">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-224">PostponeUtcDateTimeLimit</span><span class="sxs-lookup"><span data-stu-id="fa068-224">PostponeUtcDateTimeLimit</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-225">SZ</span><span class="sxs-lookup"><span data-stu-id="fa068-225">SZ</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-226">Das Datum und die Uhrzeit im UTC-DateTime-Format, in dem das erstmalige Einrichten verschoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="fa068-226">The date and time, in UTC DateTime format, that first time setup can be postponed.</span></span> <span data-ttu-id="fa068-227">Geben Sie in das Format &quot; yyyy-mm-tt hh: mm ein, &quot; wobei die Stunden unter Verwendung des standardmäßigen 24-Stunden-Clock-Standards angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="fa068-227">Enter in the format &quot;yyyy-MM-dd hh:mm&quot; with hours specified by using the 24-hour clock standard.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-228">RetryDialogMsg</span><span class="sxs-lookup"><span data-stu-id="fa068-228">RetryDialogMsg</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-229">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="fa068-229">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-230">Nachricht wird in der Ressourcendatei gefunden</span><span class="sxs-lookup"><span data-stu-id="fa068-230">Message is found in resource file</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-231">Anpassbare Nachricht, die dem Endbenutzer angezeigt wird, wenn das erstmalige Setup erneut versuchen muss.</span><span class="sxs-lookup"><span data-stu-id="fa068-231">Customizable message that is displayed to the end user when first time setup must re-attempt setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-232">SetComputerNameEnabled</span><span class="sxs-lookup"><span data-stu-id="fa068-232">SetComputerNameEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-233">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-233">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-234">Standard = 0</span><span class="sxs-lookup"><span data-stu-id="fa068-234">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-235">Konfiguriert, ob der Eintrag Computername unter dem Abschnitt [UserData] der Datei "Sysprep. inf" im Gast entsprechend der angegebenen ComputerNameMask aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa068-235">Configures whether the ComputerName entry under the [UserData] section of the Sysprep.inf file in the guest should be updated according to the specified ComputerNameMask.</span></span>   <span data-ttu-id="fa068-236">0 = falsch; 1 = wahr.</span><span class="sxs-lookup"><span data-stu-id="fa068-236">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-237">0 = falsch: der Computername-Eintrag in der Datei "Sysprep. inf" wird entsprechend der ComputerNameMask nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fa068-237">0 = false: The ComputerName entry in the Sysprep.inf file is not updated according to the ComputerNameMask.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-238">1 = wahr: der Computername-Eintrag in der Datei "Sysprep. inf" wird entsprechend der ComputerNameMask aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fa068-238">1 = true: The ComputerName entry in the Sysprep.inf file is updated according to the ComputerNameMask.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-239">SetJoinDomainEnabled</span><span class="sxs-lookup"><span data-stu-id="fa068-239">SetJoinDomainEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-240">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-240">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-241">Standard = 0</span><span class="sxs-lookup"><span data-stu-id="fa068-241">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-242">Konfiguriert, ob die JoinDomain-Einstellung unter dem Abschnitt [Identification] der Datei "Sysprep. inf" im Gast so aktualisiert werden soll, dass Sie den Einstellungen auf dem Host entspricht.</span><span class="sxs-lookup"><span data-stu-id="fa068-242">Configures whether the JoinDomain setting under the [Identification] section of the Sysprep.inf file in the guest should be updated to match the settings on the host.</span></span>  <span data-ttu-id="fa068-243">0 = falsch; 1 = wahr.</span><span class="sxs-lookup"><span data-stu-id="fa068-243">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-244">0 = falsch: die JoinDomain-Einstellung in der Datei "Sysprep. inf" wird nicht so aktualisiert, dass Sie den Einstellungen auf dem Host entspricht.</span><span class="sxs-lookup"><span data-stu-id="fa068-244">0 = false: The JoinDomain setting in the Sysprep.inf file is not updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-245">1 = wahr: die JoinDomain-Einstellung in der Datei "Sysprep. inf" wird so aktualisiert, dass Sie den Einstellungen auf dem Host entspricht.</span><span class="sxs-lookup"><span data-stu-id="fa068-245">1 = true: The JoinDomain setting in the Sysprep.inf file is updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-246">SetMachineObjectOUEnabled</span><span class="sxs-lookup"><span data-stu-id="fa068-246">SetMachineObjectOUEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-247">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-247">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-248">Standard = 0</span><span class="sxs-lookup"><span data-stu-id="fa068-248">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-249">Konfiguriert, ob die MachineObjectOU-Einstellung unter dem Abschnitt [Identification] der Datei "Sysprep. inf" im Gast so aktualisiert wird, dass Sie dem Host entspricht.</span><span class="sxs-lookup"><span data-stu-id="fa068-249">Configures whether the MachineObjectOU setting under the [Identification] section of the Sysprep.inf file in the guest is updated to match the host.</span></span>  <span data-ttu-id="fa068-250">0 = falsch; 1 = wahr.</span><span class="sxs-lookup"><span data-stu-id="fa068-250">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-251">0 = falsch: die MachineObjectOU-Einstellung in der Datei "Sysprep. inf" wird nicht so aktualisiert, dass Sie den Einstellungen auf dem Host entspricht.</span><span class="sxs-lookup"><span data-stu-id="fa068-251">0 = false: The MachineObjectOU setting in the Sysprep.inf file is not updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-252">1 = wahr: die MachineObjectOU-Einstellung in der Datei "Sysprep. inf" wird so aktualisiert, dass Sie den Einstellungen auf dem Host entspricht.</span><span class="sxs-lookup"><span data-stu-id="fa068-252">1 = true: The MachineObjectOU setting in the Sysprep.inf file is updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-253">SetRegionalSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="fa068-253">SetRegionalSettingsEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-254">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-254">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-255">Standard = 0</span><span class="sxs-lookup"><span data-stu-id="fa068-255">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-256">Konfiguriert, ob die Einstellungen unter dem Abschnitt [Regional Settings] der Datei "Sysprep. inf" im Gast entsprechend dem Host aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="fa068-256">Configures whether the settings under the [RegionalSettings] section of the Sysprep.inf file in the guest are updated to match the host.</span></span>  <span data-ttu-id="fa068-257">0 = falsch; 1 = wahr.</span><span class="sxs-lookup"><span data-stu-id="fa068-257">0 = false; 1 = true.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="fa068-258">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="fa068-258">Note</span></span></strong><br/><p><span data-ttu-id="fa068-259">Standardmäßig wird die Einstellung für TimeZone im Gast immer mit der Zeitzone-Einstellung im Host synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="fa068-259">By default, the setting for TimeZone in the guest is always synchronized with the TimeZone setting in the host.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-260">0 = falsch: die Einstellungen im Abschnitt [Regional Settings] der Datei "Sysprep. inf" im Gast werden nicht aktualisiert, um dem Host zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="fa068-260">0 = false: The settings under the [RegionalSettings] section of the Sysprep.inf file in the guest are not updated to match the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-261">1 = wahr: die Einstellungen unter dem Abschnitt [Regional Settings] der Datei "Sysprep. inf" im Gast werden entsprechend dem Host aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fa068-261">1 = true: The settings under the [RegionalSettings] section of the Sysprep.inf file in the guest are updated to match the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-262">SetUserDataEnabled</span><span class="sxs-lookup"><span data-stu-id="fa068-262">SetUserDataEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-263">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-263">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-264">Standard = 0</span><span class="sxs-lookup"><span data-stu-id="fa068-264">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-265">Konfiguriert, ob die FullName-und die OrgName-Einstellungen im Abschnitt [UserData] der Datei "Sysprep. inf" des Gastes so aktualisiert werden, dass Sie den Einstellungen auf dem Host entsprechen.</span><span class="sxs-lookup"><span data-stu-id="fa068-265">Configures whether the FullName and the OrgName settings under the [UserData] section of the Sysprep.inf file in the guest are updated to match the settings on the host.</span></span>  <span data-ttu-id="fa068-266">0 = falsch; 1 = wahr.</span><span class="sxs-lookup"><span data-stu-id="fa068-266">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-267">0 = falsch: die FullName-und OrgName-Einstellungen in der Datei "Sysprep. inf" werden nicht so aktualisiert, dass Sie den Einstellungen auf dem Host entsprechen.</span><span class="sxs-lookup"><span data-stu-id="fa068-267">0 = false: The FullName and OrgName settings in the Sysprep.inf file are not updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-268">1 = wahr: die FullName-und OrgName-Einstellungen in der Datei "Sysprep. inf" werden aktualisiert, sodass Sie den Einstellungen auf dem Host entsprechen.</span><span class="sxs-lookup"><span data-stu-id="fa068-268">1 = true: The FullName and OrgName settings in the Sysprep.inf file are updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-269">StartDialogMsg</span><span class="sxs-lookup"><span data-stu-id="fa068-269">StartDialogMsg</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-270">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="fa068-270">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-271">Nachricht wird in der Ressourcendatei gefunden</span><span class="sxs-lookup"><span data-stu-id="fa068-271">Message is found in resource file</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-272">Anpassbare Nachricht, die dem Endbenutzer angezeigt wird, wenn die erstmalige Einrichtung gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fa068-272">Customizable message that is displayed to the end user when first time setup is ready to start.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-273">TaskCancelTimeout</span><span class="sxs-lookup"><span data-stu-id="fa068-273">TaskCancelTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-274">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-274">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-275">Standard = 30</span><span class="sxs-lookup"><span data-stu-id="fa068-275">Default=30</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-276">Der Timeoutwert in Sekunden, der bei der erstmaligen Einrichtung auf eine Antwort vom virtuellen Computer für einen Abbruchvorgang wartet.</span><span class="sxs-lookup"><span data-stu-id="fa068-276">The time-out value, in seconds, that first time setup waits for a response from the virtual machine for a Cancel operation.</span></span> <span data-ttu-id="fa068-277">Bereich = 0 bis 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fa068-277">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-278">TaskVMTurnOffTimeout</span><span class="sxs-lookup"><span data-stu-id="fa068-278">TaskVMTurnOffTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-279">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-279">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-280">Standard = 60</span><span class="sxs-lookup"><span data-stu-id="fa068-280">Default=60</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-281">Der Timeoutwert in Sekunden, der von der erstmaligen Einrichtung auf das Herunterfahren des virtuellen Computers wartet.</span><span class="sxs-lookup"><span data-stu-id="fa068-281">The time-out value, in seconds, that first time setup waits for the virtual machine to shut down.</span></span> <span data-ttu-id="fa068-282">Bereich = 0 bis 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fa068-282">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-283">UpgradeTimeout</span><span class="sxs-lookup"><span data-stu-id="fa068-283">UpgradeTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-284">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-284">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-285">Standard = 600</span><span class="sxs-lookup"><span data-stu-id="fa068-285">Default=600</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-286">Die Zeitdauer in Sekunden, bevor ein Versuchtes Upgrade der MED-V-Gast-Agent-Software ein Timeout hat. Bereich = 0 bis 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fa068-286">The time, in seconds, before an attempted upgrade of the MED-V Guest Agent software times out. Range = 0 to 2147483647.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="fa068-287">UserExperience-Taste</span><span class="sxs-lookup"><span data-stu-id="fa068-287">UserExperience Key</span></span>


<span data-ttu-id="fa068-288">Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die mit dem HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\medv\\v2\\userexperience-Schlüssel und dem HKEY \ _CURRENT \ _User \\software\\microsoft\\medv\\v2\\userexperience-Schlüssel verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="fa068-288">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\UserExperience key and the HKEY\_CURRENT\_USER\\Software\\Microsoft\\Medv\\v2\\UserExperience key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa068-289">Name</span><span class="sxs-lookup"><span data-stu-id="fa068-289">Name</span></span></th>
<th align="left"><span data-ttu-id="fa068-290">Typ</span><span class="sxs-lookup"><span data-stu-id="fa068-290">Type</span></span></th>
<th align="left"><span data-ttu-id="fa068-291">Daten/Standard</span><span class="sxs-lookup"><span data-stu-id="fa068-291">Data/Default</span></span></th>
<th align="left"><span data-ttu-id="fa068-292">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa068-292">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-293">AppPublishingEnabled</span><span class="sxs-lookup"><span data-stu-id="fa068-293">AppPublishingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-294">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-294">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-295">Standard = 1</span><span class="sxs-lookup"><span data-stu-id="fa068-295">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-296">Konfiguriert, ob die Anwendungs Publikation vom Gast auf den Host aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fa068-296">Configures whether application publication from the guest to the host is enabled.</span></span>  <span data-ttu-id="fa068-297">0 = falsch; 1 = wahr.</span><span class="sxs-lookup"><span data-stu-id="fa068-297">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-298">0 = falsch: deaktiviert die Anwendungsveröffentlichung vom Gast auf den Host.</span><span class="sxs-lookup"><span data-stu-id="fa068-298">0 = false: Disables application publishing from the guest to the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-299">1 = wahr: ermöglicht die Anwendungsveröffentlichung vom Gast an den Host.</span><span class="sxs-lookup"><span data-stu-id="fa068-299">1 = true: Enables application publishing from the guest to the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-300">AudioSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="fa068-300">AudioSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-301">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-301">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-302">Standard = 1</span><span class="sxs-lookup"><span data-stu-id="fa068-302">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-303">Konfiguriert, ob die Freigabe des Audio-e/a-Geräts zwischen dem Gast und dem Host aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fa068-303">Configures whether the sharing of the audio I/O device between the guest and the host is enabled.</span></span>  <span data-ttu-id="fa068-304">0 = falsch; 1 = wahr.</span><span class="sxs-lookup"><span data-stu-id="fa068-304">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-305">0 = falsch: deaktiviert die Freigabe des Audio-e/a-Geräts zwischen dem Gast und dem Host.</span><span class="sxs-lookup"><span data-stu-id="fa068-305">0 = false: Disables the sharing of the audio I/O device between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-306">1 = wahr: ermöglicht die Freigabe des Audio-I/O-Geräts zwischen dem Gast und dem Host.</span><span class="sxs-lookup"><span data-stu-id="fa068-306">1 = true: Enables the sharing of the audio I/O device between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-307">ClipboardSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="fa068-307">ClipboardSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-308">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-308">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-309">Standard = 1</span><span class="sxs-lookup"><span data-stu-id="fa068-309">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-310">Konfiguriert, ob die Freigabe der Zwischenablage zwischen dem Gast und dem Host aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fa068-310">Configures whether the sharing of the Clipboard between the guest and the host is enabled.</span></span>  <span data-ttu-id="fa068-311">0 = falsch; 1 = wahr.</span><span class="sxs-lookup"><span data-stu-id="fa068-311">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-312">0 = falsch: deaktiviert die Freigabe der Zwischenablage zwischen dem Gast und dem Host.</span><span class="sxs-lookup"><span data-stu-id="fa068-312">0 = false: Disables the sharing of the Clipboard between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-313">1 = wahr: ermöglicht die Freigabe der Zwischenablage zwischen dem Gast und dem Host.</span><span class="sxs-lookup"><span data-stu-id="fa068-313">1 = true: Enables the sharing of the Clipboard between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-314">DialogTimeout</span><span class="sxs-lookup"><span data-stu-id="fa068-314">DialogTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-315">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-315">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-316">Standard = 300</span><span class="sxs-lookup"><span data-stu-id="fa068-316">Default=300</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-317">Die Zeitdauer (in Sekunden) vor dem Timeout des ersten Start Dialogfelds für Setup. Bereich = 0 bis 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fa068-317">The time, in seconds, before the first time setup Start Dialog times out. Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-318">HideVmTimeout</span><span class="sxs-lookup"><span data-stu-id="fa068-318">HideVmTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-319">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-319">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-320">Standard = 30</span><span class="sxs-lookup"><span data-stu-id="fa068-320">Default=30</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-321">Der Timeoutwert in Minuten, in dem das Fenster des virtuellen Computers im Vollbildmodus während eines langen Anmeldeversuchs vom Endbenutzer ausgeblendet wird.</span><span class="sxs-lookup"><span data-stu-id="fa068-321">The time-out value, in minutes, that the full-screen virtual machine window is hidden from the end user during a long logon attempt.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-322">LogonStartEnabled</span><span class="sxs-lookup"><span data-stu-id="fa068-322">LogonStartEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-323">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-323">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-324">Standard = 1</span><span class="sxs-lookup"><span data-stu-id="fa068-324">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-325">Konfiguriert, ob der Gast gestartet werden soll, wenn sich der Endbenutzer beim Desktop anmeldet oder wenn die erste gastanwendung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="fa068-325">Configures whether the guest should be started when the end user logs on to the desktop or when the first guest application is started.</span></span>  <span data-ttu-id="fa068-326">0 = falsch; 1 = wahr.</span><span class="sxs-lookup"><span data-stu-id="fa068-326">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-327">0 = falsch: der Gast wird gestartet, wenn die erste gastanwendung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="fa068-327">0 = false: The guest is started when the first guest application is started.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-328">1 = wahr: der Gast wird gestartet, wenn sich der Endbenutzer beim Desktop anmeldet.</span><span class="sxs-lookup"><span data-stu-id="fa068-328">1 = true: The guest is started when the end user logs on to the desktop.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-329">PrinterSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="fa068-329">PrinterSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-330">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-330">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-331">Standard = 1</span><span class="sxs-lookup"><span data-stu-id="fa068-331">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-332">Konfiguriert, ob die Freigabe von Druckern zwischen dem Gast und dem Host aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fa068-332">Configures whether the sharing of printers between the guest and the host is enabled.</span></span>  <span data-ttu-id="fa068-333">0 = falsch; 1 = wahr.</span><span class="sxs-lookup"><span data-stu-id="fa068-333">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-334">0 = falsch: deaktiviert die Freigabe von Druckern zwischen dem Gast und dem Host.</span><span class="sxs-lookup"><span data-stu-id="fa068-334">0 = false: Disables the sharing of printers between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-335">1 = wahr: ermöglicht die Freigabe von Druckern zwischen dem Gast und dem Host.</span><span class="sxs-lookup"><span data-stu-id="fa068-335">1 = true: Enables the sharing of printers between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-336">RebootAbsoluteDelayTimeout</span><span class="sxs-lookup"><span data-stu-id="fa068-336">RebootAbsoluteDelayTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-337">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-337">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-338">Standard = 1440</span><span class="sxs-lookup"><span data-stu-id="fa068-338">Default=1440</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-339">Der Timeoutwert in Minuten, der bei der erstmaligen Einrichtung auf einen Neustart wartet.</span><span class="sxs-lookup"><span data-stu-id="fa068-339">The time-out value, in minutes, that first time setup waits for a restart.</span></span> <span data-ttu-id="fa068-340">Bereich = 0 bis 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fa068-340">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-341">RedirectUrls</span><span class="sxs-lookup"><span data-stu-id="fa068-341">RedirectUrls</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-342">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="fa068-342">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-343">Angegebene URL-Liste</span><span class="sxs-lookup"><span data-stu-id="fa068-343">Specified URL list</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-344">Gibt eine Liste der URLs an, die vom Host an den Gast weitergeleitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fa068-344">Specifies a list of URLs to be redirected from the host to the guest.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-345">SmartCardLogonEnabled</span><span class="sxs-lookup"><span data-stu-id="fa068-345">SmartCardLogonEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-346">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-346">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-347">Standard = 0</span><span class="sxs-lookup"><span data-stu-id="fa068-347">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-348">Konfiguriert, ob Smartcards zur Authentifizierung von Benutzern für MED-V verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="fa068-348">Configures whether smart cards can be used to authenticate users to MED-V.</span></span> <span data-ttu-id="fa068-349">0 = falsch; 1 = wahr.</span><span class="sxs-lookup"><span data-stu-id="fa068-349">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-350">0 = falsch: Smartcards können Endbenutzer nicht an MED-V authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="fa068-350">0 = false: Does not let Smart Cards authenticate end users to MED-V.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-351">1 = wahr: ermöglicht Smartcards die Authentifizierung von Endbenutzern für MED-V.</span><span class="sxs-lookup"><span data-stu-id="fa068-351">1 = true: Lets Smart Cards authenticate end users to MED-V.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="fa068-352">Wichtig</span><span class="sxs-lookup"><span data-stu-id="fa068-352">Important</span></span></strong><br/><p><span data-ttu-id="fa068-353">Wenn SmartCardLogonEnabled und CredentialCacheEnabled beide aktiviert sind, überschreibt SmartCardLogonEnabled CredentialCacheEnabled.</span><span class="sxs-lookup"><span data-stu-id="fa068-353">If SmartCardLogonEnabled and CredentialCacheEnabled are both enabled, SmartCardLogonEnabled overrides CredentialCacheEnabled.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-354">SmartCardSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="fa068-354">SmartCardSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-355">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-355">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-356">Standard = 1</span><span class="sxs-lookup"><span data-stu-id="fa068-356">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-357">Konfiguriert, ob die Freigabe von Smartcards zwischen dem Gast und dem Host aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fa068-357">Configures whether the sharing of Smart Cards between the guest and the host is enabled.</span></span>  <span data-ttu-id="fa068-358">0 = falsch; 1 = wahr.</span><span class="sxs-lookup"><span data-stu-id="fa068-358">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-359">0 = falsch: deaktiviert die Freigabe von Smartcards zwischen dem Gast und dem Host.</span><span class="sxs-lookup"><span data-stu-id="fa068-359">0 = false: Disables the sharing of Smart Cards between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-360">1 = wahr: ermöglicht die Freigabe von Smartcards zwischen dem Gast und dem Host.</span><span class="sxs-lookup"><span data-stu-id="fa068-360">1 = true: Enables the sharing of Smart Cards between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-361">USBDeviceSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="fa068-361">USBDeviceSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-362">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-362">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-363">Standard = 1</span><span class="sxs-lookup"><span data-stu-id="fa068-363">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-364">Konfiguriert, ob die Freigabe von USB-Geräten zwischen dem Gast und dem Host aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fa068-364">Configures whether the sharing of USB devices between the guest and the host is enabled.</span></span>  <span data-ttu-id="fa068-365">0 = falsch; 1 = wahr.</span><span class="sxs-lookup"><span data-stu-id="fa068-365">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-366">0 = falsch: deaktiviert die Freigabe von USB-Geräten zwischen dem Gast und dem Host.</span><span class="sxs-lookup"><span data-stu-id="fa068-366">0 = false: Disables the sharing of USB devices between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-367">1 = wahr: ermöglicht die Freigabe von USB-Geräten zwischen dem Gast und dem Host.</span><span class="sxs-lookup"><span data-stu-id="fa068-367">1 = true: Enables the sharing of USB devices between the guest and the host.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="fa068-368">VM-Taste</span><span class="sxs-lookup"><span data-stu-id="fa068-368">VM Key</span></span>


<span data-ttu-id="fa068-369">Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die mit dem HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\medv\\v2\\vm-Schlüssel und dem HKEY \ _CURRENT \ _User \\software\\microsoft\\medv\\v2\\vm-Schlüssel verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="fa068-369">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\VM key and the HKEY\_CURRENT\_USER\\Software\\Microsoft\\Medv\\v2\\VM key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa068-370">Name</span><span class="sxs-lookup"><span data-stu-id="fa068-370">Name</span></span></th>
<th align="left"><span data-ttu-id="fa068-371">Typ</span><span class="sxs-lookup"><span data-stu-id="fa068-371">Type</span></span></th>
<th align="left"><span data-ttu-id="fa068-372">Daten/Standard</span><span class="sxs-lookup"><span data-stu-id="fa068-372">Data/Default</span></span></th>
<th align="left"><span data-ttu-id="fa068-373">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa068-373">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-374">CloseAction</span><span class="sxs-lookup"><span data-stu-id="fa068-374">CloseAction</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-375">SZ</span><span class="sxs-lookup"><span data-stu-id="fa068-375">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-376">Standard = Ruhezustand</span><span class="sxs-lookup"><span data-stu-id="fa068-376">Default=HIBERNATE</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-377">Die Aktion, die der virtuelle Computer ausführt, nachdem die letzte ausgeführte Anwendung geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="fa068-377">The action that the virtual machine performs after the last application that is running is closed.</span></span> <span data-ttu-id="fa068-378">Diese Einstellung wird ignoriert, wenn der LogonStartEnabled-Wert aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fa068-378">This setting is ignored if the LogonStartEnabled value is enabled.</span></span> <span data-ttu-id="fa068-379">Mögliche Optionen sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fa068-379">Possible options are as follows:</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="fa068-380">Ruhezustand </strong> .</span><span class="sxs-lookup"><span data-stu-id="fa068-380">HIBERNATE</strong> .</span></span> <span data-ttu-id="fa068-381">Mit dieser Option werden alle physikalischen Ressourcen, die der virtuelle Computer verwendet, wie Speicher und CPU, freigegeben, und der Zustand aller ausgeführten Anwendungen und Vorgänge wird gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fa068-381">This option releases all physical resources that the virtual machine is using, such as memory and CPU, and saves the state of all running applications and operations.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="fa068-382">Herunterfahren </strong> .</span><span class="sxs-lookup"><span data-stu-id="fa068-382">SHUTDOWN</strong> .</span></span> <span data-ttu-id="fa068-383">Mit dieser Option wird das Gastbetriebssystem sicher heruntergefahren und dann alle physikalischen Ressourcen freigegeben, die vom virtuellen Computer verwendet werden, beispielsweise Arbeitsspeicher und CPU.</span><span class="sxs-lookup"><span data-stu-id="fa068-383">This option shuts down the guest operating system safely and then releases all physical resources that the virtual machine is using, such as memory and CPU.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="fa068-384">Deaktivieren </strong> .</span><span class="sxs-lookup"><span data-stu-id="fa068-384">TURN-OFF</strong>.</span></span> <span data-ttu-id="fa068-385">Diese Option kann zu Datenverlusten führen, weil Sie mit dem Ausschalten des Netzschalters oder dem Ziehen des Netzkabel auf einem physikalischen Computer identisch ist.</span><span class="sxs-lookup"><span data-stu-id="fa068-385">This option can cause data loss because it is the same as turning off the power button or pulling out the power cord on a physical computer.</span></span> <span data-ttu-id="fa068-386">Verwenden Sie diese Option nur, wenn Sie eine der beiden anderen Optionen nicht verwenden können.</span><span class="sxs-lookup"><span data-stu-id="fa068-386">Use this option only if you cannot use one of the other two options.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-387">GuestMemFromHostMem</span><span class="sxs-lookup"><span data-stu-id="fa068-387">GuestMemFromHostMem</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-388">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="fa068-388">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-389">378, 512, 1024, 1536, 2048</span><span class="sxs-lookup"><span data-stu-id="fa068-389">378, 512, 1024, 1536, 2048</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-390">Eine Liste der Speicherwerte (MB) für den Gast.</span><span class="sxs-lookup"><span data-stu-id="fa068-390">A list of memory (MB) values for the guest.</span></span> <span data-ttu-id="fa068-391">Dieser Wert wird verwendet, um zu ermitteln, wie viel RAM dem Gast zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="fa068-391">This value is used to determine how much RAM is available to the guest.</span></span> <span data-ttu-id="fa068-392">In Kombination mit HostMemToGuestMem wird eine Nachschlagetabelle erstellt, um zu ermitteln, wie viel RAM auf dem virtuellen Gastcomputer zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa068-392">Combined with HostMemToGuestMem, a lookup table is created to determine how much RAM to allocate on the guest virtual machine.</span></span> <span data-ttu-id="fa068-393">Mögliche Werte können von 128 bis 3712 sein.</span><span class="sxs-lookup"><span data-stu-id="fa068-393">Possible values can be from 128 to 3712.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-394">GuestUpdateDuration</span><span class="sxs-lookup"><span data-stu-id="fa068-394">GuestUpdateDuration</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-395">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-395">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-396">Standard = 240</span><span class="sxs-lookup"><span data-stu-id="fa068-396">Default=240</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-397">Die Anzahl der Minuten, die MED-V den Gast für die automatische Aktualisierung aufbewahren soll, beginnend mit der im GuestUpdateTime-Wert angegebenen Zeit.</span><span class="sxs-lookup"><span data-stu-id="fa068-397">The number of minutes that MED-V should keep the guest awake for automatic updating, starting at the time specified in the GuestUpdateTime value.</span></span> <span data-ttu-id="fa068-398">Bereich = 0 bis 1440.</span><span class="sxs-lookup"><span data-stu-id="fa068-398">Range = 0 to 1440.</span></span> <span data-ttu-id="fa068-399">Wenn dieser Wert auf 0 (null) festgelegt wird, wird die Funktion zum Patchen von Gästen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="fa068-399">Setting this value to zero (0) disables the guest patching functionality.</span></span></p>
<p><span data-ttu-id="fa068-400">Weitere Informationen zu Guest-Patches für die automatische Aktualisierung finden Sie unter <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> Verwalten von automatischen Updates für MED-V-Arbeitsbereiche </a> .</span><span class="sxs-lookup"><span data-stu-id="fa068-400">For more information about guest patching for automatic updating, see <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)">Managing Automatic Updates for MED-V Workspaces</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-401">GuestUpdateTime</span><span class="sxs-lookup"><span data-stu-id="fa068-401">GuestUpdateTime</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-402">SZ</span><span class="sxs-lookup"><span data-stu-id="fa068-402">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-403">Standard = 00:00</span><span class="sxs-lookup"><span data-stu-id="fa068-403">Default=00:00</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-404">Die Stunden und Minuten pro Tag, wenn MED-V den Gast für die automatische Aktualisierung reaktivieren soll, mithilfe des standardmäßigen 24-Stunden-Clock-Standards.</span><span class="sxs-lookup"><span data-stu-id="fa068-404">The hour and minute each day when MED-V should wake up the guest for automatic updating, by using the 24-hour clock standard.</span></span> <span data-ttu-id="fa068-405">Angeben der Uhrzeit im Format hh: mm</span><span class="sxs-lookup"><span data-stu-id="fa068-405">Specify the time in the format HH:MM</span></span>  </p>
<p><span data-ttu-id="fa068-406">Weitere Informationen zu Guest-Patches für die automatische Aktualisierung finden Sie unter <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> Verwalten von automatischen Updates für MED-V-Arbeitsbereiche </a> .</span><span class="sxs-lookup"><span data-stu-id="fa068-406">For more information about guest patching for automatic updating, see <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)">Managing Automatic Updates for MED-V Workspaces</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-407">HostMemToGuestMem</span><span class="sxs-lookup"><span data-stu-id="fa068-407">HostMemToGuestMem</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-408">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="fa068-408">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-409">1024, 2048, 4096, 8192, 16384</span><span class="sxs-lookup"><span data-stu-id="fa068-409">1024, 2048, 4096, 8192, 16384</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-410">Eine Liste der Speicherwerte (MB) für den Gast, die durch den auf dem Host verfügbaren RAM bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="fa068-410">A list of memory (MB) values for the guest, determined by the RAM available on the host.</span></span> <span data-ttu-id="fa068-411">In Kombination mit GuestMemFromHostMem wird eine Nachschlagetabelle erstellt, um zu ermitteln, wie viel RAM auf dem virtuellen Gastcomputer zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa068-411">Combined with GuestMemFromHostMem, a lookup table is created to determine how much RAM to allocate on the guest virtual machine.</span></span> <span data-ttu-id="fa068-412">Mögliche Werte können von 1024 bis 16384 sein.</span><span class="sxs-lookup"><span data-stu-id="fa068-412">Possible values can be from 1024 to 16384.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-413">HostMemToGuestMemCalcEnabled</span><span class="sxs-lookup"><span data-stu-id="fa068-413">HostMemToGuestMemCalcEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-414">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-414">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-415">Standard = 1</span><span class="sxs-lookup"><span data-stu-id="fa068-415">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-416">Konfiguriert, ob der für den Gast zugewiesene Speicher aus dem auf dem Host vorhandenen Speicher berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="fa068-416">Configures whether the memory allocated for the guest is calculated from the memory present on the host.</span></span>  <span data-ttu-id="fa068-417">0 = falsch; 1 = wahr.</span><span class="sxs-lookup"><span data-stu-id="fa068-417">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-418">0 = falsch: der für den Gast zugewiesene Arbeitsspeicher wird nicht aus dem auf dem Host vorhandenen Speicher berechnet.</span><span class="sxs-lookup"><span data-stu-id="fa068-418">0 = false: The memory allocated for the guest is not calculated from the memory present on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-419">1 = wahr: der für den Gast zugewiesene Speicher wird aus dem auf dem Host vorhandenen Speicher berechnet.</span><span class="sxs-lookup"><span data-stu-id="fa068-419">1 = true: The memory allocated for the guest is calculated from the memory present on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-420">Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="fa068-420">Memory</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-421">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-421">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-422">Standard = 512</span><span class="sxs-lookup"><span data-stu-id="fa068-422">Default=512</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-423">Der RAM (MB), der für den virtuellen Gastcomputer reserviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa068-423">The RAM (MB) that should be allocated for the guest virtual machine.</span></span> <span data-ttu-id="fa068-424">Diese Einstellung wird ignoriert, wenn die HostMemToGuestMemEnabled-Einstellung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fa068-424">This setting is ignored if the HostMemToGuestMemEnabled setting is enabled.</span></span> <span data-ttu-id="fa068-425">Bereich = 128 bis 2048.</span><span class="sxs-lookup"><span data-stu-id="fa068-425">Range=128 to 2048.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-426">MultiUserEnabled</span><span class="sxs-lookup"><span data-stu-id="fa068-426">MultiUserEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-427">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-427">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-428">Standard = 0</span><span class="sxs-lookup"><span data-stu-id="fa068-428">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-429">Konfiguriert, ob mehrere Benutzer denselben MED-V-Arbeitsbereich verwenden.</span><span class="sxs-lookup"><span data-stu-id="fa068-429">Configures whether multiple users share the same MED-V workspace.</span></span>  <span data-ttu-id="fa068-430">0 = falsch; 1 = wahr.</span><span class="sxs-lookup"><span data-stu-id="fa068-430">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-431">0 = falsch: mehrere Benutzer verwenden nicht den gleichen MED-V-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="fa068-431">0 = false: Multiple users do not share the same MED-V workspace.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-432">1 = wahr: mehrere Benutzer verwenden denselben MED-V-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="fa068-432">1 = true: Multiple users share the same MED-V workspace.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa068-433">NetworkingMode</span><span class="sxs-lookup"><span data-stu-id="fa068-433">NetworkingMode</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-434">SZ</span><span class="sxs-lookup"><span data-stu-id="fa068-434">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-435">Standard = NAT</span><span class="sxs-lookup"><span data-stu-id="fa068-435">Default=NAT</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-436">Die Art der für den Gast verwendeten Netzwerkverbindung.</span><span class="sxs-lookup"><span data-stu-id="fa068-436">The kind of network connection used on the guest.</span></span> <span data-ttu-id="fa068-437">Mögliche Werte lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fa068-437">Possible values are as follows:</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="fa068-438">Überbrückt </strong> .</span><span class="sxs-lookup"><span data-stu-id="fa068-438">Bridged</strong>.</span></span> <span data-ttu-id="fa068-439">MED-V hat eine eigene Netzwerkadresse, die normalerweise über DHCP abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fa068-439">MED-V has its own network address, typically obtained through DHCP.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="fa068-440">NAT </strong> .</span><span class="sxs-lookup"><span data-stu-id="fa068-440">NAT</strong>.</span></span> <span data-ttu-id="fa068-441">MED-V verwendet die Netzwerkadressübersetzung (Network Address Translation, NAT), um die IP-Adresse des Host-&#39;für ausgehenden Datenverkehr freizugeben.</span><span class="sxs-lookup"><span data-stu-id="fa068-441">MED-V uses Network Address Translation (NAT) to share the host&#39;s IP for outgoing traffic.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-442">TaskTimeout</span><span class="sxs-lookup"><span data-stu-id="fa068-442">TaskTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-443">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-443">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-444">Standard = 600</span><span class="sxs-lookup"><span data-stu-id="fa068-444">Default=600</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-445">Ein allgemeiner Timeoutwert in Sekunden, auf den MED-V wartet, bis eine Aufgabe abgeschlossen ist, beispielsweise ein Neustart und ein Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="fa068-445">A general time-out value, in seconds, that MED-V waits for a task to be completed, such as restarting and shutting down.</span></span> <span data-ttu-id="fa068-446">Bereich = 0 bis 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fa068-446">Range = 0 to 2147483647.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="fa068-447">Einstellungen für Gast Registrierung</span><span class="sxs-lookup"><span data-stu-id="fa068-447">Guest Registry Settings</span></span>


<span data-ttu-id="fa068-448">In diesem Abschnitt werden die konfigurierbaren MED-V Guest-Registrierungsschlüssel aufgelistet und deren Verwendung erläutert.</span><span class="sxs-lookup"><span data-stu-id="fa068-448">This section lists the configurable MED-V guest registry keys and explains their uses.</span></span>

### <span data-ttu-id="fa068-449">v2</span><span class="sxs-lookup"><span data-stu-id="fa068-449">v2</span></span>

<span data-ttu-id="fa068-450">Die folgende Tabelle enthält Informationen zum Registrierungswert Guest, der dem HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\medv\\v2\\-Schlüssel zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fa068-450">The following table provides information about the guest registry value associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\ key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa068-451">Name</span><span class="sxs-lookup"><span data-stu-id="fa068-451">Name</span></span> </th>
<th align="left"><span data-ttu-id="fa068-452">Typ</span><span class="sxs-lookup"><span data-stu-id="fa068-452">Type</span></span> </th>
<th align="left"><span data-ttu-id="fa068-453">Daten/Standard</span><span class="sxs-lookup"><span data-stu-id="fa068-453">Data/Default</span></span> </th>
<th align="left"><span data-ttu-id="fa068-454">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa068-454">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa068-455">EnableGPWorkarounds</span><span class="sxs-lookup"><span data-stu-id="fa068-455">EnableGPWorkarounds</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa068-456">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa068-456">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-457">Standard = 1</span><span class="sxs-lookup"><span data-stu-id="fa068-457">Default=1</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fa068-458">Konfiguriert, wie MED-V die Tasten BufferPolicyReads und GroupPolicyMinTransferRate behandelt.</span><span class="sxs-lookup"><span data-stu-id="fa068-458">Configures how MED-V handles the keys BufferPolicyReads and GroupPolicyMinTransferRate.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fa068-459">Standardmäßig legt MED-V diese Schlüssel wie folgt fest:</span><span class="sxs-lookup"><span data-stu-id="fa068-459">By default, MED-V sets these keys as follows:</span></span></p>
<p><span data-ttu-id="fa068-460">BufferPolicyReads = 1 und GroupPolicyMinTransferRate = 0.</span><span class="sxs-lookup"><span data-stu-id="fa068-460">BufferPolicyReads=1 and GroupPolicyMinTransferRate=0.</span></span></p>
<p><span data-ttu-id="fa068-461">Erstellen Sie den EnableGPWorkarounds-Schlüssel, falls erforderlich, und legen Sie den Schlüssel auf NULL, wenn Sie nicht möchten, dass MED-V die Standardeinstellungen von BufferPolicyReads und GroupPolicyMinTransferRate ändert.</span><span class="sxs-lookup"><span data-stu-id="fa068-461">Create the EnableGPWorkarounds  key, if it is necessary, and set the key to zero if you do not want MED-V to change the default settings of BufferPolicyReads and GroupPolicyMinTransferRate.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="fa068-462">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="fa068-462">Note</span></span></strong><br/><p><span data-ttu-id="fa068-463">Wenn Ihr MED-V-Arbeitsbereich im NAT-Modus ausgeführt wird, wirkt sich EnableGPWorkarounds auf die Registrierungsschlüssel BufferPolicyReads und GroupPolicyMinTransferRate aus.</span><span class="sxs-lookup"><span data-stu-id="fa068-463">If your MED-V workspace is running in NAT mode, EnableGPWorkarounds affects the registry keys BufferPolicyReads and GroupPolicyMinTransferRate.</span></span> <span data-ttu-id="fa068-464">Wenn Ihr MED-V-Arbeitsbereich im Bridged-Modus ausgeführt wird, wirkt sich EnableGPWorkarounds nur auf den Registrierungsschlüssel BufferPolicyReads aus.</span><span class="sxs-lookup"><span data-stu-id="fa068-464">If your MED-V workspace is running in BRIDGED mode, EnableGPWorkarounds only affects the registry key BufferPolicyReads.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="fa068-465">1 = wahr: med-V legt die Tasten BufferPolicyReads = 1 und GroupPolicyMinTransferRate = 0 (falls im NAT-Modus ausgeführt) oder nur BufferPolicyReads = 1 fest (wenn Sie im Bridge-Modus ausgeführt werden).</span><span class="sxs-lookup"><span data-stu-id="fa068-465">1=true: MED-V sets the keys BufferPolicyReads=1 and GroupPolicyMinTransferRate=0 (if running in NAT mode) or just BufferPolicyReads=1 (if running in BRIDGED mode).</span></span></p>
<p><span data-ttu-id="fa068-466">0 = falsch: med-V nimmt keine Änderungen an den Tasten BufferPolicyReads und GroupPolicyMinTransferRate vor.</span><span class="sxs-lookup"><span data-stu-id="fa068-466">0=false: MED-V does not make any changes to the keys BufferPolicyReads and GroupPolicyMinTransferRate.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="fa068-467">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="fa068-467">Related topics</span></span>


[<span data-ttu-id="fa068-468">Verwalten von MED-V-Arbeitsbereich Anwendungen</span><span class="sxs-lookup"><span data-stu-id="fa068-468">Manage MED-V Workspace Applications</span></span>](manage-med-v-workspace-applications.md)

[<span data-ttu-id="fa068-469">Verwalten von MED-V-URL-Umleitungen</span><span class="sxs-lookup"><span data-stu-id="fa068-469">Manage MED-V URL Redirection</span></span>](manage-med-v-url-redirection.md)

[<span data-ttu-id="fa068-470">Verwalten von MED-V-Arbeitsbereichseinstellungen</span><span class="sxs-lookup"><span data-stu-id="fa068-470">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)









