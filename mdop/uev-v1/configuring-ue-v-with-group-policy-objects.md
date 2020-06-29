---
title: Konfigurieren von UE-V mit Gruppenrichtlinienobjekten
description: Konfigurieren von UE-V mit Gruppenrichtlinienobjekten
author: dansimp
ms.assetid: 5c9be706-a05f-4397-9a38-e6b73ebff1e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e479e6bef1a2b38cf822ffca19ed4220b0c59fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811911"
---
# <span data-ttu-id="1d2a4-103">Konfigurieren von UE-V mit Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="1d2a4-103">Configuring UE-V with Group Policy Objects</span></span>


<span data-ttu-id="1d2a4-104">Einige Gruppenrichtlinieneinstellungen für Microsoft User Experience Virtualization (UE-V) können für Computer definiert werden, andere können für benutzerdefiniert werden.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-104">Some Microsoft User Experience Virtualization (UE-V) Group Policy settings can be defined for computers and others can be defined for users.</span></span> <span data-ttu-id="1d2a4-105">Die Konfigurationsrichtlinien Einstellungen des UE-V-Agents können für Computer oder Benutzerdefiniert werden.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-105">UE-V agent configuration policy settings can be defined for computers or users.</span></span> <span data-ttu-id="1d2a4-106">Informationen zum Installieren von ADMX-Dateien für UE-v-Gruppenrichtlinien finden Sie unter [Installieren der ADMX-Vorlagen für UE-v-Gruppenrichtlinien](installing-the-ue-v-group-policy-admx-templates.md).</span><span class="sxs-lookup"><span data-stu-id="1d2a4-106">For information about how to install UE-V Group Policy ADMX files, see [Installing the UE-V Group Policy ADMX Templates](installing-the-ue-v-group-policy-admx-templates.md).</span></span>

<span data-ttu-id="1d2a4-107">Die folgenden Richtlinieneinstellungen können für UE-V konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="1d2a4-107">The following policy settings can be configured for UE-V:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1d2a4-108">Name der Richtlinieneinstellung</span><span class="sxs-lookup"><span data-stu-id="1d2a4-108">Policy setting name</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="1d2a4-109">Ziel</span><span class="sxs-lookup"><span data-stu-id="1d2a4-109">Target</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="1d2a4-110">Beschreibung der Richtlinieneinstellung</span><span class="sxs-lookup"><span data-stu-id="1d2a4-110">Policy setting description</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="1d2a4-111">Konfigurationsoptionen</span><span class="sxs-lookup"><span data-stu-id="1d2a4-111">Configuration options</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1d2a4-112">Verwenden der Benutzeroberflächen-Virtualisierung (UE-V)</span><span class="sxs-lookup"><span data-stu-id="1d2a4-112">Use User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-113">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="1d2a4-113">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-114">Mit dieser Richtlinieneinstellung können Sie die Virtualisierung der Benutzeroberfläche (UE-V) aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-114">This policy setting allows you to enable or disable User Experience Virtualization (UE-V).</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-115">Aktivieren oder deaktivieren Sie diese Richtlinieneinstellung.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-115">Enable or disable this policy setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1d2a4-116">Speicherpfad für Einstellungen</span><span class="sxs-lookup"><span data-stu-id="1d2a4-116">Settings storage path</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-117">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="1d2a4-117">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-118">Diese Richtlinieneinstellung konfiguriert, wo die Benutzereinstellungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-118">This policy setting configures where the user settings will be stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-119">Bereitstellen eines UNC-Pfads (Universal Naming Convention) und von Variablen wie \Server\SettingsShare%username%.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-119">Provide a Universal Naming Convention (UNC) path and variables such as \Server\SettingsShare%username%.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1d2a4-120">Katalogpfad für Einstellungs Vorlagen</span><span class="sxs-lookup"><span data-stu-id="1d2a4-120">Settings template catalog path</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-121">Nur Computer</span><span class="sxs-lookup"><span data-stu-id="1d2a4-121">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-122">Diese Richtlinieneinstellung konfiguriert, wo die Speicherort Vorlagen für benutzerdefinierte Einstellungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-122">This policy setting configures where custom settings location templates are stored.</span></span> <span data-ttu-id="1d2a4-123">Mit dieser Richtlinieneinstellung wird auch konfiguriert, ob der Katalog zum Ersetzen der Microsoft-Standardvorlagen verwendet wird, die mit dem UE-V-Agent installiert werden.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-123">This policy setting also configures whether the catalog will be used to replace the default Microsoft templates that are installed with the UE-V agent.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-124">Stellen Sie einen UNC-Pfad (Universal Naming Convention) wie \Server\TemplateShare oder einen Ordnerspeicherort auf dem Computer bereit.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-124">Provide a Universal Naming Convention (UNC) path such as \Server\TemplateShare or a folder location on the computer.</span></span></p>
<p></p>
<p><span data-ttu-id="1d2a4-125">Aktivieren Sie das Kontrollkästchen, um die standardmäßigen Microsoft-Vorlagen zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-125">Select the check box to replace the default Microsoft templates.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1d2a4-126">Verwenden Sie keine Offline Dateien</span><span class="sxs-lookup"><span data-stu-id="1d2a4-126">Do not use Offline Files</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-127">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="1d2a4-127">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-128">Mit dieser Richtlinieneinstellung können Sie konfigurieren, ob UE-V das Windows-Feature "Offline Dateien" verwendet.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-128">This policy setting allows you to configure whether UE-V will use the Windows Offline Files feature.</span></span> <span data-ttu-id="1d2a4-129">Mit dieser Richtlinieneinstellung können Sie auch die Benachrichtigung aktivieren, wenn der Import von Benutzereinstellungen verzögert wird.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-129">This policy setting also allows you to enable notification to occur when the import of user settings is delayed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-130">Aktivieren Sie diese Einstellung, um den UE-V-Agent so zu konfigurieren, dass keine Offlinedateien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-130">To configure the UE-V Agent to not use offline files, enable this setting.</span></span></p>
<p></p>
<p><span data-ttu-id="1d2a4-131">Geben Sie an, ob Benachrichtigungen erfolgen sollen, wenn der Import von Einstellungen verzögert wird.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-131">Specify if notifications should be given when settings import is delayed.</span></span></p>
<p></p>
<p><span data-ttu-id="1d2a4-132">Geben Sie die Dauer in Sekunden an, die gewartet werden soll, bevor die Benachrichtigung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-132">Specify the length of time in seconds to wait before the notification appears.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1d2a4-133">Synchronisierungs Timeout</span><span class="sxs-lookup"><span data-stu-id="1d2a4-133">Synchronization timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-134">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="1d2a4-134">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-135">Mit dieser Richtlinieneinstellung wird die Anzahl der Millisekunden konfiguriert, die der Computer vor einem Timeout wartet, wenn Benutzereinstellungen vom Speicherort der Remoteeinstellungen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-135">This policy setting configures the number of milliseconds that the computer waits before a timeout when retrieving user settings from the remote settings location.</span></span> <span data-ttu-id="1d2a4-136">Wenn der Remotespeicher Standort nicht verfügbar ist, wird der Anwendungsstart um diese Zahl von Millisekunden verzögert.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-136">If the remote storage location is unavailable, the application launch is delayed by this many milliseconds.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-137">Geben Sie das bevorzugte Synchronisierungs Timeout in Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-137">Specify the preferred synchronization timeout in milliseconds.</span></span> <span data-ttu-id="1d2a4-138">Der Standardwert von 2000 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-138">The default value of 2000 milliseconds.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1d2a4-139">Warnungsschwellenwert für Paketgröße</span><span class="sxs-lookup"><span data-stu-id="1d2a4-139">Package size warning threshold</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-140">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="1d2a4-140">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-141">Mit dieser Richtlinieneinstellung können Sie den UE-V-Agent so konfigurieren, dass er meldet, wenn die Dateigröße eines Einstellungen-Pakets einen definierten Schwellenwert erreicht.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-141">This policy setting allows you to configure the UE-V agent to report when a settings package file size reaches a defined threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-142">Der bevorzugte Schwellenwert für die Größe der Einstellungs Pakete in Kilobyte angegeben.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-142">Specified the preferred threshold for settings package sizes in kilobytes.</span></span></p>
<p><span data-ttu-id="1d2a4-143">Standardmäßig hat der UE-V-Agent keinen Schwellenwert für die Paketdatei Größe.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-143">By default, the UE-V agent does not have a package file size threshold.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1d2a4-144">Einstellungen für Roaming-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="1d2a4-144">Roaming Application settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-145">Nur für Benutzer</span><span class="sxs-lookup"><span data-stu-id="1d2a4-145">Users Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-146">Diese Richtlinieneinstellung konfiguriert das Roaming der Benutzereinstellungen von Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-146">This policy setting configures the roaming of user settings of applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-147">Wählen Sie aus, welche Windows-Einstellungen zwischen Computern durchlaufen sollen.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-147">Select which Windows settings will roam between computers.</span></span></p>
<p><span data-ttu-id="1d2a4-148">Standardmäßig werden die Benutzereinstellungen von Anwendungen mit der von UE-V bereitgestellten Einstellungs Vorlage zwischen Computern durchsucht.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-148">By default, the user settings of applications with settings template provided by UE-V are roamed between computers.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1d2a4-149">Roaming-Windows-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="1d2a4-149">Roaming Windows settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-150">Nur für Benutzer</span><span class="sxs-lookup"><span data-stu-id="1d2a4-150">Users Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-151">Diese Richtlinieneinstellung konfiguriert das Roaming von Windows-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-151">This policy setting configures the roaming of Windows settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1d2a4-152">Wählen Sie aus, welche Anwendungen zwischen Computern durchlaufen sollen.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-152">Select which applications will roam between computers.</span></span></p>
<p><span data-ttu-id="1d2a4-153">Standardmäßig werden Windows-Designs zwischen Computern der gleichen Betriebssystemversion durchsucht.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-153">By default, Windows themes are roamed between computers of the same operating system version.</span></span> <span data-ttu-id="1d2a4-154">Die Windows-Desktopeinstellungen und die Einstellungen für den erleichterten Zugriff werden nicht durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-154">Windows desktop settings and Ease of Access settings are not roamed.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="1d2a4-155">So konfigurieren Sie computerbezogene Richtlinien</span><span class="sxs-lookup"><span data-stu-id="1d2a4-155">To configure computer-targeted policies</span></span>**

1.  <span data-ttu-id="1d2a4-156">Verwenden Sie die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) auf dem Domänencontrollercomputer, der Gruppenrichtlinien für UE-V-Computer verwaltet.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-156">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) on the domain controller computer that manages Group Policy for UE-V computers.</span></span> <span data-ttu-id="1d2a4-157">Navigieren Sie zu **Computer Konfiguration**, wählen Sie **Richtlinien**aus, wählen Sie **Administrative Vorlagen**aus, klicken Sie auf **Windows-Komponenten**, und wählen Sie dann **Microsoft User Experience Virtualization**aus.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-157">Navigate to **Computer configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="1d2a4-158">Wählen Sie die zu bearbeitende Richtlinieneinstellung aus.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-158">Select the policy setting to be edited.</span></span>

**<span data-ttu-id="1d2a4-159">So konfigurieren Sie benutzerbezogene Richtlinien</span><span class="sxs-lookup"><span data-stu-id="1d2a4-159">To configure user-targeted policies</span></span>**

1.  <span data-ttu-id="1d2a4-160">Verwenden Sie die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder das erweiterte Tool für die Gruppenrichtlinienverwaltung (AGPM) im Microsoft Desktop Optimization Pack (MDOP) auf dem Domänencontrollercomputer, der die Gruppenrichtlinie für UE-V verwaltet.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-160">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) tool in Microsoft Desktop Optimization Pack (MDOP) on the domain controller computer that manages Group Policy for UE-V.</span></span> <span data-ttu-id="1d2a4-161">Navigieren Sie zu **Benutzerkonfiguration**, wählen Sie **Richtlinien**aus, wählen Sie **Administrative Vorlagen**aus, klicken Sie auf **Windows-Komponenten**, und wählen Sie dann **Microsoft User Experience Virtualization**aus.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-161">Navigate to **User configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="1d2a4-162">Wählen Sie die bearbeitete Richtlinieneinstellung aus.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-162">Select the policy setting edited.</span></span>

<span data-ttu-id="1d2a4-163">Der UE-V-Agent verwendet die folgende Rangfolge, um die Synchronisierung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-163">The UE-V agent uses the following order of precedence to determine synchronization.</span></span>

**<span data-ttu-id="1d2a4-164">Rangfolge der UE-V-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="1d2a4-164">Order of precedence for UE-V settings</span></span>**

1.  <span data-ttu-id="1d2a4-165">Benutzerbezogene Einstellungen, die von Gruppenrichtlinien verwaltet werden – diese Konfigurationseinstellungen werden im Registrierungsschlüssel nach Gruppenrichtlinie unter gespeichert `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="1d2a4-165">User-targeted settings managed by Group Policy - These configuration settings are stored in the registry key by Group Policy under `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="1d2a4-166">Von Gruppenrichtlinien verwaltete Computer gesteuerte Einstellungen – diese Konfigurationseinstellungen werden im Registrierungsschlüssel nach Gruppenrichtlinie unter gespeichert `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="1d2a4-166">Computer-targeted settings managed by Group Policy - These configuration settings are stored in the registry key by Group Policy under `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

3.  <span data-ttu-id="1d2a4-167">Vom aktuellen Benutzer mithilfe von PowerShell oder WMI definierte Konfigurationseinstellungen – diese Konfigurationseinstellungen werden vom UE-V-Agent unter diesem Registrierungsspeicherort gespeichert: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="1d2a4-167">Configuration settings defined by the current user using PowerShell or WMI - These configuration settings are stored by the UE-V agent under this registry location: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

4.  <span data-ttu-id="1d2a4-168">Die für den Computer mit PowerShell oder WMI definierten Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-168">Configuration settings defined for the computer using PowerShell or WMI.</span></span> <span data-ttu-id="1d2a4-169">Diese Konfigurationseinstellungen werden vom UE-V-Agent unter dem gespeichert `HKEY_LOCAL_MACHINE \Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="1d2a4-169">These configuration settings are stored by the UE-V agent under the `HKEY_LOCAL_MACHINE \Software\Microsoft\Uev\Agent\Configuration`.</span></span>

## <span data-ttu-id="1d2a4-170">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1d2a4-170">Related topics</span></span>


[<span data-ttu-id="1d2a4-171">Verwalten von UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="1d2a4-171">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="1d2a4-172">Vorgänge für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="1d2a4-172">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





