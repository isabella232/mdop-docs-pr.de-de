---
title: Planen der Verwendung von Anwendungen zum Synchronisieren mit UE-V 1.0
description: Planen der Verwendung von Anwendungen zum Synchronisieren mit UE-V 1.0
author: dansimp
ms.assetid: c718274f-87b4-47f3-8ef7-5e1bd5557a9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f2b04942588d0f6efad03d5e0249534cd325c09
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804211"
---
# <span data-ttu-id="97455-103">Planen der Verwendung von Anwendungen zum Synchronisieren mit UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="97455-103">Planning Which Applications to Synchronize with UE-V 1.0</span></span>


<span data-ttu-id="97455-104">Microsoft User Experience Virtualization (UE-v) verwendet Einstellungen-Standort Vorlagen (XML-Dateien), die die Einstellungen definieren, die von UE-v erfasst und angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="97455-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings that are captured and applied by UE-V.</span></span> <span data-ttu-id="97455-105">UE-V enthält eine Reihe vordefinierter Einstellungen für Standort Vorlagen und ermöglicht es Administratoren auch, benutzerdefinierte Einstellungen für Standort Vorlagen für Drittanbieter-oder Branchenanwendungen zu erstellen, die im Unternehmen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97455-105">UE-V includes a set of predefined settings location templates and also allows administrators to create custom settings location templates for third-party or line-of-business applications that are used in the enterprise.</span></span>

<span data-ttu-id="97455-106">Wenn Sie als Administrator berücksichtigen, welche Anwendungen in Ihre UE-V-Lösung einbezogen werden sollen, sollten Sie berücksichtigen, welche Einstellungen von Benutzern angepasst werden können und wie und wo die Anwendung die Einstellungen speichert.</span><span class="sxs-lookup"><span data-stu-id="97455-106">As an administrator, when you consider which applications to include in your UE-V solution, consider which settings can be customized by users, and how and where the application stores its settings.</span></span> <span data-ttu-id="97455-107">Nicht alle Anwendungen verfügen über Einstellungen, die angepasst oder regelmäßig von Benutzern angepasst werden können.</span><span class="sxs-lookup"><span data-stu-id="97455-107">Not all applications have settings that can be customized or that are routinely customized by users.</span></span> <span data-ttu-id="97455-108">Darüber hinaus können nicht alle Anwendungseinstellungen über mehrere Computer oder Umgebungen sicher durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="97455-108">In addition, not all applications settings can safely roam across multiple computers or environments.</span></span> <span data-ttu-id="97455-109">Synchronisieren Sie die Einstellungen, die die folgenden Kriterien erfüllen:</span><span class="sxs-lookup"><span data-stu-id="97455-109">Synchronize settings that meet the following criteria:</span></span>

-   <span data-ttu-id="97455-110">Einstellungen, die in Benutzer zugänglichen Speicherorten gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="97455-110">Settings that are stored in user-accessible locations.</span></span> <span data-ttu-id="97455-111">Synchronisieren Sie beispielsweise nicht die Einstellungen, die im System32-oder outside HKCU-Abschnitt der Registrierung gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="97455-111">For example, do not synchronize settings that are stored in system32 or outside HKCU section of the registry.</span></span>

-   <span data-ttu-id="97455-112">Einstellungen, die nicht für den jeweiligen Computer spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="97455-112">Settings that are not specific to the particular computer.</span></span> <span data-ttu-id="97455-113">Schließen Sie beispielsweise Netzwerk-oder Hardwarekonfigurationen aus.</span><span class="sxs-lookup"><span data-stu-id="97455-113">For example, exclude network or hardware configurations.</span></span>

-   <span data-ttu-id="97455-114">Einstellungen, die zwischen Computern synchronisiert werden können, ohne dass ein Risiko für beschädigte Daten besteht.</span><span class="sxs-lookup"><span data-stu-id="97455-114">Settings that can be synchronized between computers without risk of corrupted data.</span></span> <span data-ttu-id="97455-115">Verwenden Sie beispielsweise keine Einstellungen, die in einer Datenbankdatei gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="97455-115">For example, do not use settings that are stored in a database file.</span></span>

## <span data-ttu-id="97455-116">In UE-V enthaltene Positions Vorlagen für Einstellungen</span><span class="sxs-lookup"><span data-stu-id="97455-116">Settings location templates that are included in UE-V</span></span>


**<span data-ttu-id="97455-117">Standort Vorlagen für UE-V-Anwendungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="97455-117">UE-V application settings location templates</span></span>**

<span data-ttu-id="97455-118">Die Installationssoftware des UE-V-Agents installiert den Agenten und registriert eine Standardgruppe von Einstellungen-Standort Vorlagen für gängige Microsoft-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="97455-118">The UE-V agent installation software installs the agent and registers a default group of settings location templates for common Microsoft applications.</span></span> <span data-ttu-id="97455-119">Mit den Einstellungen für die Positions Vorlagen werden die Einstellungswerte für die folgenden Anwendungen erfasst:</span><span class="sxs-lookup"><span data-stu-id="97455-119">These settings location templates capture settings values for the following applications:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="97455-120">Anwendungskategorie</span><span class="sxs-lookup"><span data-stu-id="97455-120">Application category</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="97455-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97455-121">Description</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="97455-122">Microsoft Office 2010-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="97455-122">Microsoft Office 2010 applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="97455-123">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="97455-123">Microsoft Word 2010</span></span></p>
<p><span data-ttu-id="97455-124">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="97455-124">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="97455-125">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="97455-125">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="97455-126">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="97455-126">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="97455-127">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="97455-127">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="97455-128">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="97455-128">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="97455-129">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="97455-129">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="97455-130">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="97455-130">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="97455-131">Microsoft SharePoint Workspace 2010</span><span class="sxs-lookup"><span data-stu-id="97455-131">Microsoft SharePoint Workspace 2010</span></span></p>
<p><span data-ttu-id="97455-132">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="97455-132">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="97455-133">Microsoft lync 2010</span><span class="sxs-lookup"><span data-stu-id="97455-133">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="97455-134">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="97455-134">Microsoft OneNote 2010</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="97455-135">Browser Optionen (Internet Explorer 8, Internet Explorer 9 und Internet Explorer 10)</span><span class="sxs-lookup"><span data-stu-id="97455-135">Browser options (Internet Explorer 8, Internet Explorer 9, and Internet Explorer 10)</span></span></p></td>
<td align="left"><p><span data-ttu-id="97455-136">Favoriten, Startseite, Tabstopps und Symbolleisten.</span><span class="sxs-lookup"><span data-stu-id="97455-136">Favorites, home page, tabs, and toolbars.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="97455-137">Windows-Zubehör</span><span class="sxs-lookup"><span data-stu-id="97455-137">Windows accessories</span></span></p></td>
<td align="left"><p><span data-ttu-id="97455-138">Rechner, Notepad, WordPad.</span><span class="sxs-lookup"><span data-stu-id="97455-138">Calculator, Notepad, WordPad.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="97455-139">Anwendungseinstellungen werden auf die Anwendung angewendet, wenn die Anwendung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="97455-139">Application settings are applied to the application when the application is started.</span></span> <span data-ttu-id="97455-140">Sie werden beim Schließen der Anwendung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="97455-140">They are saved when the application closes.</span></span>

**<span data-ttu-id="97455-141">Standort Vorlagen für UE-V-Windows-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="97455-141">UE-V Windows settings location templates</span></span>**

<span data-ttu-id="97455-142">Die Virtualisierung der Benutzeroberfläche umfasst Einstellungen-Speicherort Vorlagen, mit denen Einstellungswerte für die folgenden Windows-Einstellungen erfasst werden:</span><span class="sxs-lookup"><span data-stu-id="97455-142">User Experience Virtualization includes settings location templates that capture settings values for the following Windows settings:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="97455-143">Windows-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="97455-143">Windows settings</span></span></th>
<th align="left"><span data-ttu-id="97455-144">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97455-144">Description</span></span></th>
<th align="left"><span data-ttu-id="97455-145">Anwenden auf</span><span class="sxs-lookup"><span data-stu-id="97455-145">Apply on</span></span></th>
<th align="left"><span data-ttu-id="97455-146">Standardzustand</span><span class="sxs-lookup"><span data-stu-id="97455-146">Default state</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="97455-147">Desktophintergrund</span><span class="sxs-lookup"><span data-stu-id="97455-147">Desktop background</span></span></p></td>
<td align="left"><p><span data-ttu-id="97455-148">Derzeit aktiver Desktop Hintergrund</span><span class="sxs-lookup"><span data-stu-id="97455-148">Currently active desktop background.</span></span></p></td>
<td align="left"><p><span data-ttu-id="97455-149">Anmelden, entsperren, Remoteverbindung.</span><span class="sxs-lookup"><span data-stu-id="97455-149">Logon, unlock, remote connect.</span></span></p></td>
<td align="left"><p><span data-ttu-id="97455-150">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="97455-150">Enabled</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="97455-151">Erleichterte Bedienung</span><span class="sxs-lookup"><span data-stu-id="97455-151">Ease of Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="97455-152">Bedienungshilfen und Eingabeeinstellungen, Bildschirmlupe, Sprachausgabe und Bildschirmtastatur.</span><span class="sxs-lookup"><span data-stu-id="97455-152">Accessibility and input settings, magnifier, Narrator, and on-Screen keyboard.</span></span></p></td>
<td align="left"><p><span data-ttu-id="97455-153">Anmelden, entsperren, Remoteverbindung.</span><span class="sxs-lookup"><span data-stu-id="97455-153">Logon, unlock, remote connect.</span></span></p></td>
<td align="left"><p><span data-ttu-id="97455-154">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="97455-154">Disabled</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="97455-155">Desktop Einstellungen</span><span class="sxs-lookup"><span data-stu-id="97455-155">Desktop settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="97455-156">Startmenü-und Taskleisteneinstellungen, Ordneroptionen, Standard Desktopsymbole, zusätzliche Uhren sowie Regions-und Spracheinstellungen.</span><span class="sxs-lookup"><span data-stu-id="97455-156">Start menu and Taskbar settings, Folder options, default desktop icons, additional clocks, and region and Language settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="97455-157">Nur Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="97455-157">Logon only.</span></span></p></td>
<td align="left"><p><span data-ttu-id="97455-158">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="97455-158">Disabled</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="97455-159">Der Windows-Desktop Hintergrund und die Einstellungen für die erleichterte Bedienung werden angewendet, wenn sich der Benutzer anmeldet, wenn der Computer entriegelt wird, oder wenn eine Remoteverbindung mit einem anderen Computer besteht.</span><span class="sxs-lookup"><span data-stu-id="97455-159">The Windows desktop background and Ease of Access settings are applied when the user logs on, when the computer is unlocked, or upon remote connection to another computer.</span></span> <span data-ttu-id="97455-160">Der Agent speichert diese Einstellungen, wenn sich der Benutzer abmeldet, wenn der Computer gesperrt ist oder wenn eine Remoteverbindung getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="97455-160">The agent saves these settings when the user logs off, when the computer is locked, or when a remote connection is disconnected.</span></span> <span data-ttu-id="97455-161">Standardmäßig werden die Windows-Desktop Hintergrundeinstellungen zwischen Computern der gleichen Betriebssystemversion durchsucht.</span><span class="sxs-lookup"><span data-stu-id="97455-161">By default, Windows desktop background settings are roamed between computers of the same operating system version.</span></span>

<span data-ttu-id="97455-162">Windows-Desktop und Einstellungen für die erleichterte Bedienung werden bei der Anmeldung angewendet, bevor der Desktop dem Benutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="97455-162">Windows desktop and Ease of Access settings are applied at logon before the desktop is presented to the user.</span></span> <span data-ttu-id="97455-163">Um die Anmelde Erfahrung zu optimieren, werden diese Einstellungen nicht standardmäßig durchsucht.</span><span class="sxs-lookup"><span data-stu-id="97455-163">To optimize the logon experience, these settings are not roamed by default.</span></span> <span data-ttu-id="97455-164">Die Einstellungen für Desktop und erleichterte Bedienung können mithilfe von Gruppenrichtlinien, PowerShell und WMI aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="97455-164">Desktop and Ease of Access settings can be enabled by using Group Policy, PowerShell, and WMI.</span></span>

<span data-ttu-id="97455-165">UE-V unterstützt nicht das Roaming von Einstellungen zwischen Betriebssystemen mit unterschiedlichen Sprachen.</span><span class="sxs-lookup"><span data-stu-id="97455-165">UE-V does not support the roaming of settings between operating systems with different languages.</span></span> <span data-ttu-id="97455-166">Beispielsweise wird die Synchronisierung zwischen Englisch und Deutsch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="97455-166">For example, synchronization between English and German is not supported.</span></span> <span data-ttu-id="97455-167">Die Sprache aller Computer, auf die UE-V die Benutzereinstellungen durchstreift, müssen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="97455-167">The language of all computers to which UE-V roams the user settings must match.</span></span>

<span data-ttu-id="97455-168">**Hinweis**  Wenn Sie die von Microsoft bereitgestellten Einstellungen für Standort Vorlagen ändern, funktioniert die Virtualisierung der Benutzeroberfläche möglicherweise nicht ordnungsgemäß für die vorgesehene Anwendung oder Windows-Einstellungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="97455-168">**Note** If you change the settings location templates that are provided by Microsoft, User Experience Virtualization might not work properly for the designated application or Windows settings group.</span></span>

 

## <a href="" id="prevent-unintentional-user-settings-configuration-"></a><span data-ttu-id="97455-169">Verhindern der unbeabsichtigten Konfiguration von Benutzereinstellungen</span><span class="sxs-lookup"><span data-stu-id="97455-169">Prevent unintentional user Settings configuration</span></span>


<span data-ttu-id="97455-170">Virtualisierung der Benutzeroberfläche überprüft, ob neue Informationen zu den Benutzereinstellungen verwendet werden, und downloadet diese Informationen entsprechend von einem Speicherort für Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="97455-170">User Experience Virtualization checks for new user settings information, and downloads that information accordingly from a settings storage location.</span></span> <span data-ttu-id="97455-171">Anschließend werden die Einstellungen in den folgenden Fällen auf den lokalen Computer angewendet:</span><span class="sxs-lookup"><span data-stu-id="97455-171">Then, it applies the settings to the local computer in the following cases:</span></span>

-   <span data-ttu-id="97455-172">Jedes Mal, wenn eine Anwendung gestartet wird, die über eine registrierte UE-V-Vorlage verfügt.</span><span class="sxs-lookup"><span data-stu-id="97455-172">Every time an application is launched that has a registered UE-V template.</span></span>

-   <span data-ttu-id="97455-173">Wenn sich ein Benutzer bei seinem Computer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="97455-173">When a user logs on to their computer.</span></span>

-   <span data-ttu-id="97455-174">Wenn ein Benutzer seinen Computer entsperrt.</span><span class="sxs-lookup"><span data-stu-id="97455-174">When a user unlocks their computer.</span></span>

-   <span data-ttu-id="97455-175">Wenn eine Verbindung mit einem Remote Desktopcomputer hergestellt wird, auf dem UE-V installiert ist.</span><span class="sxs-lookup"><span data-stu-id="97455-175">When a connection is made to a remote desktop computer that has UE-V installed.</span></span>

<span data-ttu-id="97455-176">Wenn UE-V auf Computer a und Computer B installiert ist und die gewünschten Einstellungen für die Anwendung auf Computer a liegen, muss Computer a die Anwendung zuerst öffnen und schließen.</span><span class="sxs-lookup"><span data-stu-id="97455-176">If UE-V is installed on computer A and computer B, and the desired settings for the application are on computer A, then computer A must open and close the application first.</span></span> <span data-ttu-id="97455-177">Wenn eine Anwendung zuerst auf Computer b geöffnet und geschlossen wird, werden die Anwendungseinstellungen auf Computer A so konfiguriert, dass Sie mit den Anwendungseinstellungen auf Computer b identisch sind.</span><span class="sxs-lookup"><span data-stu-id="97455-177">If an application is opened and closed on computer B first, then the application settings on computer A will be configured to be the same as the application settings on computer B.</span></span>

<span data-ttu-id="97455-178">Dieses Szenario gilt auch für Windows-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="97455-178">This scenario also applies to Windows settings.</span></span> <span data-ttu-id="97455-179">Wenn die Windows-Einstellungen auf Computer B mit den Windows-Einstellungen auf Computer a identisch sein sollten, sollte sich der Benutzer zuerst anmelden und den Computer abmelden.</span><span class="sxs-lookup"><span data-stu-id="97455-179">If the Windows settings on computer B should be the same as the Windows settings on computer A, then the user should logon and logoff computer A first.</span></span>

<span data-ttu-id="97455-180">Wenn die gewünschten Benutzereinstellungen in der falschen Reihenfolge angewendet werden, können Sie wiederhergestellt werden, indem Sie einen Wiederherstellungsvorgang für die jeweilige Anwendung oder Windows-Konfiguration auf dem Computer ausführen, auf dem die Einstellungen überschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="97455-180">If the desired user settings are applied in the wrong order, they can be recovered by performing a restore operation for the specific application or Windows configuration on the computer on which the settings were overwritten.</span></span> <span data-ttu-id="97455-181">Weitere Informationen finden Sie unter [Wiederherstellen von Anwendungs-und Windows-Einstellungen, die mit UE-V 1,0 synchronisiert](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md)wurden.</span><span class="sxs-lookup"><span data-stu-id="97455-181">For more information, see [Restoring Application and Windows Settings Synchronized with UE-V 1.0](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md).</span></span>

## <span data-ttu-id="97455-182">Benutzerdefinierte Standort Vorlagen für UE-V-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="97455-182">Custom UE-V settings location templates</span></span>


<span data-ttu-id="97455-183">Mithilfe des UE-V-Generators können Sie benutzerdefinierte Standort Vorlagen für Einstellungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="97455-183">You can create custom settings location templates by using the UE-V Generator.</span></span> <span data-ttu-id="97455-184">Nachdem Sie eine Standort Vorlage für benutzerdefinierte Einstellungen in einer Testumgebung erstellt und getestet haben, können Sie die Einstellungen-Speicherort Vorlagen auf Computern im Unternehmen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="97455-184">After you create and test a custom settings location template in a test environment, you can deploy the settings location templates to computers in the enterprise.</span></span> <span data-ttu-id="97455-185">Speicherort Vorlagen für benutzerdefinierte Einstellungen müssen mit einer vorhandenen Bereitstellungsinfrastruktur bereitgestellt werden, beispielsweise mit der Enterprise Software Distribution (ESD)-Methode, mit Einstellungen oder durch Konfigurieren eines UE-V-Einstellungs Vorlagen Katalogs.</span><span class="sxs-lookup"><span data-stu-id="97455-185">Custom settings location templates must be deployed with an existing deployment infrastructure, such as enterprise software distribution (ESD) method, with preferences, or by configuring an UE-V settings template catalog.</span></span> <span data-ttu-id="97455-186">Vorlagen, die mit ESD-oder Gruppenrichtlinien bereitgestellt werden, müssen mit UE-V WMI oder PowerShell registriert werden.</span><span class="sxs-lookup"><span data-stu-id="97455-186">Templates that are deployed with ESD or Group Policy must be registered by using UE-V WMI or PowerShell.</span></span> <span data-ttu-id="97455-187">Weitere Informationen zu den Standort Vorlagen für benutzerdefinierte Einstellungen finden Sie unter [Planen der Bereitstellung von benutzerdefinierten Vorlagen für UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="97455-187">For more information about custom settings location templates, see [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).</span></span>

<span data-ttu-id="97455-188">Anleitungen dazu, ob eine Branchenanwendung synchronisiert werden soll, finden Sie unter [Checkliste für die Evaluierung von Branchenanwendungen für UE-V 1,0](checklist-for-evaluating-line-of-business-applications-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="97455-188">For guidance on whether a line-of-business application should be synchronized, see [Checklist for Evaluating Line-of-Business Applications for UE-V 1.0](checklist-for-evaluating-line-of-business-applications-for-ue-v-10.md).</span></span>

## <span data-ttu-id="97455-189">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="97455-189">Related topics</span></span>


[<span data-ttu-id="97455-190">Planen für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="97455-190">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="97455-191">Planen der Bereitstellung von benutzerdefinierten Vorlagen für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="97455-191">Planning for Custom Template Deployment for UE-V 1.0</span></span>](planning-for-custom-template-deployment-for-ue-v-10.md)

[<span data-ttu-id="97455-192">Bereitstellen von UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="97455-192">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

 

 





