---
title: Microsoft User Experience Virtualization (UE-V) 2. x
description: Microsoft User Experience Virtualization (UE-V) 2. x
author: dansimp
ms.assetid: b860fed0-b846-415d-bdd6-ba60231a64be
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 573b8bb2027e5c7f117a8254005a43c656f047a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795814"
---
# <span data-ttu-id="98418-103">Microsoft User Experience Virtualization (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="98418-103">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>

>[!NOTE]
><span data-ttu-id="98418-104">Diese Dokumentation ist eine für die Version von UE-V, die im Microsoft-Desktop Optimierungspaket (MDOP) enthalten war.</span><span class="sxs-lookup"><span data-stu-id="98418-104">This documentation is a for version of UE-V that was included in the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="98418-105">Informationen zur neuesten Version von UE-v, die in Windows 10 Enterprise enthalten ist, finden Sie unter [Erste Schritte mit UE-v](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).</span><span class="sxs-lookup"><span data-stu-id="98418-105">For information about the latest version of UE-V which is included in Windows 10 Enterprise, see [Get Started with UE-V](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).</span></span>


<span data-ttu-id="98418-106">Erfassen und zentralisieren Sie die Anwendungseinstellungen und Windows-Betriebssystem Einstellungen Ihrer Benutzer, indem Sie die Microsoft User Experience Virtualization (UE-V) 2,0 oder 2,1 implementieren.</span><span class="sxs-lookup"><span data-stu-id="98418-106">Capture and centralize your users’ application settings and Windows OS settings by implementing Microsoft User Experience Virtualization (UE-V) 2.0 or 2.1.</span></span> <span data-ttu-id="98418-107">Wenden Sie diese Einstellungen dann auf die Geräte an, auf die Benutzer in Ihrem Unternehmen zugreifen, wie Desktopcomputer, Laptops oder VDI-Sitzungen (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="98418-107">Then, apply these settings to the devices users access in your enterprise, like desktop computers, laptops, or virtual desktop infrastructure (VDI) sessions.</span></span>

**<span data-ttu-id="98418-108">Mit UE-V können Sie...</span><span class="sxs-lookup"><span data-stu-id="98418-108">With UE-V you can…</span></span>**

-   <span data-ttu-id="98418-109">Angeben, welche Anwendungs-und Desktopeinstellungen synchronisiert werden sollen</span><span class="sxs-lookup"><span data-stu-id="98418-109">Specify which application and desktop settings synchronize</span></span>

-   <span data-ttu-id="98418-110">Orts- und zeitunabhängige Bereitstellung der Einstellungen im Unternehmen</span><span class="sxs-lookup"><span data-stu-id="98418-110">Deliver the settings anytime and anywhere users work throughout the enterprise</span></span>

-   <span data-ttu-id="98418-111">Erstellen benutzerdefinierter Vorlagen für Drittanbieter- oder Branchenanwendungen</span><span class="sxs-lookup"><span data-stu-id="98418-111">Create custom templates for your third-party or line-of-business applications</span></span>

-   <span data-ttu-id="98418-112">Wiederherstellen von Einstellungen nach dem Hardwareaustausch oder-Upgrade oder nach dem erneuten Imaging einer virtuellen Maschine in Ihrem ursprünglichen Zustand</span><span class="sxs-lookup"><span data-stu-id="98418-112">Recover settings after hardware replacement or upgrade, or after reimaging a virtual machine to its initial state</span></span>

## <span data-ttu-id="98418-113">Komponenten von UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="98418-113">Components of UE-V 2.x</span></span>


<span data-ttu-id="98418-114">Dieses Diagramm zeigt, wie die bereitgestellten UE-V-Komponenten zum Synchronisieren von Einstellungen zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="98418-114">This diagram shows how deployed UE-V components work together to synchronize settings.</span></span>

![uev2-Architekturdiagramm](images/uev2archdiagram.gif)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="98418-116">Komponente</span><span class="sxs-lookup"><span data-stu-id="98418-116">Component</span></span></th>
<th align="left"><span data-ttu-id="98418-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="98418-117">Function</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="98418-118">UE-V-Agent</span><span class="sxs-lookup"><span data-stu-id="98418-118">UE-V Agent</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="98418-119">Auf jedem Computer, auf dem die Einstellungen synchronisiert werden müssen, <strong> überwacht der UE-V-Agent </strong> registrierte Anwendungen und das Betriebssystem für alle Einstellungen und synchronisiert dann diese Einstellungen zwischen Computern.</span><span class="sxs-lookup"><span data-stu-id="98418-119">Installed on every computer that needs to synchronize settings, the <strong>UE-V Agent</strong> monitors registered applications and the operating system for any settings changes, then synchronizes those settings between computers.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="98418-120">Einstellungen-Pakete</span><span class="sxs-lookup"><span data-stu-id="98418-120">Settings packages</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="98418-121">Anwendungseinstellungen und Windows-Einstellungen werden in <strong> </strong> den vom UE-V-Agent erstellten Einstellungspaketen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="98418-121">Application settings and Windows settings are stored in <strong>settings packages</strong> created by the UE-V Agent.</span></span> <span data-ttu-id="98418-122">Einstellungspakete werden erstellt, lokal gespeichert und an den Speicherort für die Einstellungen kopiert.</span><span class="sxs-lookup"><span data-stu-id="98418-122">Settings packages are built, locally stored, and copied to the settings storage location.</span></span></p>
<ul>
<li><p><span data-ttu-id="98418-123">Die Einstellungswerte für <strong> Desktopanwendungen </strong> werden gespeichert, wenn der Benutzer die Anwendung schließt.</span><span class="sxs-lookup"><span data-stu-id="98418-123">The setting values for <strong>desktop applications</strong> are stored when the user closes the application.</span></span></p></li>
<li><p><span data-ttu-id="98418-124">Werte für <strong> Windows </strong> -Einstellungen werden gespeichert, wenn sich der Benutzer abmeldet, wenn der Computer gesperrt ist oder wenn der Benutzer die Verbindung von einem Computer entfernt trennt.</span><span class="sxs-lookup"><span data-stu-id="98418-124">Values for <strong>Windows settings</strong> are stored when the user logs off, when the computer is locked, or when the user disconnects remotely from a computer.</span></span></p></li>
</ul>
<p><span data-ttu-id="98418-125">Der Synchronisierungsanbieter bestimmt, wann die Anwendungs-oder Betriebssystemeinstellungen aus den <strong> Einstellungspaketen gelesen </strong> und synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="98418-125">The sync provider determines when the application or operating system settings are read from the <strong>Settings Packages</strong> and synchronized.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="98418-126">Speicherort des Einstellungs Speichers</span><span class="sxs-lookup"><span data-stu-id="98418-126">Settings storage location</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="98418-127">Hierbei handelt es sich um eine standardmäßige Netzwerkfreigabe, auf die Ihre Benutzer zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="98418-127">This is a standard network share that your users can access.</span></span> <span data-ttu-id="98418-128">Der UE-V-Agent überprüft den Standort und erstellt einen versteckten Systemordner, in dem Benutzereinstellungen gespeichert und abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="98418-128">The UE-V Agent verifies the location and creates a hidden system folder in which to store and retrieve user settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="98418-129">Einstellungen-Speicherort Vorlagen</span><span class="sxs-lookup"><span data-stu-id="98418-129">Settings location templates</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="98418-130">UE-V verwendet XML-Dateien als Speicherort Vorlagen für Einstellungen, um die Einstellungen für die Desktopanwendung und die Windows-Desktopeinstellungen zwischen den Benutzercomputern zu überwachen und zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="98418-130">UE-V uses XML files as settings location templates to monitor and synchronize desktop application settings and Windows desktop settings between user computers.</span></span> <span data-ttu-id="98418-131">Standardmäßig sind einige Einstellungen für Speicherort Vorlagen in UE-V enthalten.</span><span class="sxs-lookup"><span data-stu-id="98418-131">By default, some settings location templates are included in UE-V .</span></span> <span data-ttu-id="98418-132">Sie können auch Standort Vorlagen für benutzerdefinierte Einstellungen erstellen, bearbeiten oder überprüfen, indem Sie die <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)"> Synchronisierung von Einstellungen für benutzerdefinierte Anwendungen verwalten </a> .</span><span class="sxs-lookup"><span data-stu-id="98418-132">You can also create, edit, or validate custom settings location templates by <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)">managing settings synchronization for custom applications</a>.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="98418-133">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="98418-133">Note</span></span></strong><br/><p><span data-ttu-id="98418-134">Für Windows-apps sind keine Speicherort Vorlagen für Einstellungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="98418-134">Settings location templates are not required for Windows apps.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="98418-135">Windows-App-Liste</span><span class="sxs-lookup"><span data-stu-id="98418-135">Windows app list</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="98418-136">Einstellungen für Windows-apps werden erfasst und dynamisch angewendet.</span><span class="sxs-lookup"><span data-stu-id="98418-136">Settings for Windows apps are captured and applied dynamically.</span></span> <span data-ttu-id="98418-137">Der App-Entwickler gibt die Einstellungen an, die für jede APP synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="98418-137">The app developer specifies the settings that are synchronized for each app.</span></span> <span data-ttu-id="98418-138">UE-V legt fest, welche Windows-Apps für die Synchronisierung von Einstellungen unter Verwendung einer verwalteten Liste von apps aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="98418-138">UE-V determines which Windows apps are enabled for settings synchronization using a managed list of apps.</span></span> <span data-ttu-id="98418-139">Diese Liste enthält standardmäßig die meisten Windows-apps.</span><span class="sxs-lookup"><span data-stu-id="98418-139">By default, this list includes most Windows apps.</span></span></p>
<p><span data-ttu-id="98418-140">Sie können Anwendungen in der Windows-App-Liste hinzufügen oder entfernen, indem Sie die hier gezeigten Verfahren befolgen <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)"> </a> .</span><span class="sxs-lookup"><span data-stu-id="98418-140">You can add or remove applications in the Windows app list by following the procedures shown <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)">here</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="customapps"></a><span data-ttu-id="98418-141">Verwalten der Synchronisierung von Einstellungen für benutzerdefinierte Anwendungen</span><span class="sxs-lookup"><span data-stu-id="98418-141">Managing Settings Synchronization for Custom Applications</span></span>

<span data-ttu-id="98418-142">Verwenden Sie diese UE-V-Komponenten, um benutzerdefinierte Vorlagen für Ihre Drittanbieter-oder Branchenanwendungen zu erstellen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="98418-142">Use these UE-V components to create and manage custom templates for your third-party or line-of-business applications.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="98418-143">UE-V-Generator</span><span class="sxs-lookup"><span data-stu-id="98418-143">UE-V Generator</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="98418-144">Verwenden <strong> Sie den UE-V-Generator </strong> , um benutzerdefinierte Standort Vorlagen für Einstellungen zu erstellen, die Sie dann an Benutzer Computer verteilen können.</span><span class="sxs-lookup"><span data-stu-id="98418-144">Use the <strong>UE-V Generator</strong> to create custom settings location templates that you can then distribute to user computers.</span></span> <span data-ttu-id="98418-145">Mit dem UE-V-Generator können Sie auch eine vorhandene Vorlage bearbeiten oder eine Vorlage überprüfen, die mit einem anderen XML-Editor erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="98418-145">The UE-V Generator also lets you edit an existing template or validate a template that was created by using another XML editor.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="98418-146">Vorlagenkatalog für Einstellungen</span><span class="sxs-lookup"><span data-stu-id="98418-146">Settings template catalog</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="98418-147">Der <strong> Einstellungs Vorlagenkatalog </strong> ist ein Ordnerpfad auf UE-V-Computern oder eine SMB-Netzwerkfreigabe (Server Message Block), in der die Speicherort Vorlagen für benutzerdefinierte Einstellungen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="98418-147">The <strong>settings template catalog</strong> is a folder path on UE-V computers or a Server Message Block (SMB) network share that stores the custom settings location templates.</span></span> <span data-ttu-id="98418-148">Der UE-V-Agent überprüft diesen Speicherort einmal täglich, ruft neue oder aktualisierte Vorlagen ab und aktualisiert das Synchronisierungsverhalten.</span><span class="sxs-lookup"><span data-stu-id="98418-148">The UE-V Agent checks this location once a day, retrieves new or updated templates, and updates its synchronization behavior.</span></span></p>
<p><span data-ttu-id="98418-149">Wenn Sie nur die Standort Vorlagen für die UE-V-Standardeinstellungen verwenden, ist ein Einstellungs Vorlagenkatalog nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="98418-149">If you use only the UE-V default settings location templates, then a settings template catalog is unnecessary.</span></span> <span data-ttu-id="98418-150">Weitere Informationen zu Einstellungen für die Bereitstellungs Kataloge finden Sie unter <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)"> Konfigurieren eines UE-V-Einstellungs Vorlagen Katalogs </a> .</span><span class="sxs-lookup"><span data-stu-id="98418-150">For more information about settings deployment catalogs, see <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)">Configure a UE-V settings template catalog</a>.</span></span></p></td>
</tr>
</tbody>
</table>



![UE-v-Generator Prozess](images/ue-vgeneratorprocess.gif)

## <span data-ttu-id="98418-152">Standardmäßige Synchronisierung von Einstellungen</span><span class="sxs-lookup"><span data-stu-id="98418-152">Settings Synchronized by Default</span></span>


<span data-ttu-id="98418-153">UE-V synchronisiert die Einstellungen für diese Anwendungen standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="98418-153">UE-V synchronizes settings for these applications by default.</span></span> <span data-ttu-id="98418-154">Eine vollständige Liste und ausführlichere Informationen finden Sie unter [Einstellungen, die in einer UE-V-Bereitstellung automatisch synchronisiert werden](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="98418-154">For a complete list and more detailed information, see [Settings that are automatically synchronized in a UE-V deployment](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span></span>

<span data-ttu-id="98418-155">Microsoft Office 2013-Anwendungen (UE-V 2,1 SP1 und 2,1)</span><span class="sxs-lookup"><span data-stu-id="98418-155">Microsoft Office 2013 applications (UE-V 2.1 SP1 and 2.1)</span></span>

<span data-ttu-id="98418-156">Microsoft Office 2010-Anwendungen (UE-V 2,1 SP1, 2,1 und 2,0)</span><span class="sxs-lookup"><span data-stu-id="98418-156">Microsoft Office 2010 applications (UE-V 2.1 SP1, 2.1, and 2.0)</span></span>

<span data-ttu-id="98418-157">Microsoft Office 2007-Anwendungen (nur UE-V 2,0)</span><span class="sxs-lookup"><span data-stu-id="98418-157">Microsoft Office 2007 applications (UE-V 2.0 only)</span></span>

<span data-ttu-id="98418-158">Internet Explorer 8, 9 und 10</span><span class="sxs-lookup"><span data-stu-id="98418-158">Internet Explorer 8, 9, and 10</span></span>

<span data-ttu-id="98418-159">Internet Explorer 11 in UE-V 2,1 SP1 und 2,1</span><span class="sxs-lookup"><span data-stu-id="98418-159">Internet Explorer 11 in UE-V 2.1 SP1 and 2.1</span></span>

<span data-ttu-id="98418-160">Viele Windows-Anwendungen wie Xbox</span><span class="sxs-lookup"><span data-stu-id="98418-160">Many Windows applications, such as Xbox</span></span>

<span data-ttu-id="98418-161">Viele Windows-Desktopanwendungen wie Notepad</span><span class="sxs-lookup"><span data-stu-id="98418-161">Many Windows desktop applications, such as Notepad</span></span>

<span data-ttu-id="98418-162">Viele Windows-Einstellungen wie Desktop Hintergrund oder Hintergrund</span><span class="sxs-lookup"><span data-stu-id="98418-162">Many Windows settings, such as desktop background or wallpaper</span></span>

**<span data-ttu-id="98418-163">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="98418-163">Note</span></span>**  
<span data-ttu-id="98418-164">Sie können [UE-V auch so anpassen, dass Einstellungen](https://technet.microsoft.com/library/dn458942.aspx) für Anwendungen synchronisiert werden, die nicht standardmäßig synchronisiert sind.</span><span class="sxs-lookup"><span data-stu-id="98418-164">You can also [customize UE-V to synchronize settings](https://technet.microsoft.com/library/dn458942.aspx) for applications other than those synchronized by default.</span></span>



## <span data-ttu-id="98418-165">Vergleich von UE-V mit anderen Microsoft-Produkten</span><span class="sxs-lookup"><span data-stu-id="98418-165">Compare UE-V to other Microsoft products</span></span>


<span data-ttu-id="98418-166">Verwenden Sie diese Tabelle, um UE-V zu vergleichen, um Profile in Windows 7 zu synchronisieren, Profile in Windows 8 zu synchronisieren und das Feature Synchronisierungs-PC-Einstellungen von Microsoft-Konto zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="98418-166">Use this table to compare UE-V to Synchronize Profiles in Windows 7, Synchronize Profiles in Windows 8, and the Sync PC Settings feature of Microsoft account.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="98418-167">Feature</span><span class="sxs-lookup"><span data-stu-id="98418-167">Feature</span></span></th>
<th align="left"><span data-ttu-id="98418-168">Synchronisieren von Profilen mit Windows 7</span><span class="sxs-lookup"><span data-stu-id="98418-168">Synchronize Profiles using Windows 7</span></span></th>
<th align="left"><span data-ttu-id="98418-169">Synchronisieren von Profilen mit Windows 8</span><span class="sxs-lookup"><span data-stu-id="98418-169">Synchronize Profiles using Windows 8</span></span></th>
<th align="left"><span data-ttu-id="98418-170">Synchronisieren von Profilen mithilfe von Windows 10</span><span class="sxs-lookup"><span data-stu-id="98418-170">Synchronize Profiles using Windows 10</span></span></th>
<th align="left"><span data-ttu-id="98418-171">Microsoft-Konto</span><span class="sxs-lookup"><span data-stu-id="98418-171">Microsoft account</span></span></th>
<th align="left"><span data-ttu-id="98418-172">UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="98418-172">UE-V 2.0</span></span></th>
<th align="left"><span data-ttu-id="98418-173">UE-V 2,1 und 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="98418-173">UE-V 2.1 and 2.1 SP1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="98418-174">Synchronisieren von Einstellungen zwischen mehreren Computern</span><span class="sxs-lookup"><span data-stu-id="98418-174">Synchronize settings between multiple computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-175">●</span><span class="sxs-lookup"><span data-stu-id="98418-175">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-176">●</span><span class="sxs-lookup"><span data-stu-id="98418-176">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-177">●</span><span class="sxs-lookup"><span data-stu-id="98418-177">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-178">●</span><span class="sxs-lookup"><span data-stu-id="98418-178">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-179">●</span><span class="sxs-lookup"><span data-stu-id="98418-179">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-180">●</span><span class="sxs-lookup"><span data-stu-id="98418-180">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="98418-181">Synchronisieren von Einstellungen zwischen physischen und virtuellen apps</span><span class="sxs-lookup"><span data-stu-id="98418-181">Synchronize settings between physical and virtual apps</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="98418-182">●</span><span class="sxs-lookup"><span data-stu-id="98418-182">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-183">●</span><span class="sxs-lookup"><span data-stu-id="98418-183">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="98418-184">Synchronisieren von Windows-App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="98418-184">Synchronize Windows app settings</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="98418-185">●</span><span class="sxs-lookup"><span data-stu-id="98418-185">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-186">●</span><span class="sxs-lookup"><span data-stu-id="98418-186">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-187">●</span><span class="sxs-lookup"><span data-stu-id="98418-187">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="98418-188">Verwalten über WMI</span><span class="sxs-lookup"><span data-stu-id="98418-188">Manage via WMI</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="98418-189">●</span><span class="sxs-lookup"><span data-stu-id="98418-189">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-190">●</span><span class="sxs-lookup"><span data-stu-id="98418-190">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="98418-191">●</span><span class="sxs-lookup"><span data-stu-id="98418-191">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-192">●</span><span class="sxs-lookup"><span data-stu-id="98418-192">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="98418-193">Regelmäßige Synchronisierung von Einstellungsänderungen</span><span class="sxs-lookup"><span data-stu-id="98418-193">Synchronize settings changes on a regular basis</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="98418-194">●</span><span class="sxs-lookup"><span data-stu-id="98418-194">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-195">●</span><span class="sxs-lookup"><span data-stu-id="98418-195">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-196">●</span><span class="sxs-lookup"><span data-stu-id="98418-196">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="98418-197">Minimale Konfiguration für Setup</span><span class="sxs-lookup"><span data-stu-id="98418-197">Minimal configuration for Setup</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-198">●</span><span class="sxs-lookup"><span data-stu-id="98418-198">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-199">●</span><span class="sxs-lookup"><span data-stu-id="98418-199">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-200">●</span><span class="sxs-lookup"><span data-stu-id="98418-200">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-201">●</span><span class="sxs-lookup"><span data-stu-id="98418-201">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-202">●</span><span class="sxs-lookup"><span data-stu-id="98418-202">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-203">●</span><span class="sxs-lookup"><span data-stu-id="98418-203">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="98418-204">Unterstützt auf Computern, die nicht mit der Domäne verbunden sind</span><span class="sxs-lookup"><span data-stu-id="98418-204">Supported on non-domain joined computers</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="98418-205">●</span><span class="sxs-lookup"><span data-stu-id="98418-205">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="98418-206">Active Directory-Attribut für primären Computer unterstützt</span><span class="sxs-lookup"><span data-stu-id="98418-206">Supports Primary Computer Active Directory attribute</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="98418-207">●</span><span class="sxs-lookup"><span data-stu-id="98418-207">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-208">●</span><span class="sxs-lookup"><span data-stu-id="98418-208">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="98418-209">Synchronisiert die Einstellungen zwischen Virtual Desktop Infrastructure (VDI)/Remote-Desktop Diensten (RDS) und Rich-Desktops</span><span class="sxs-lookup"><span data-stu-id="98418-209">Synchronizes settings between virtual desktop infrastructure (VDI)/Remote Desktop Services (RDS) and rich desktops</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="98418-210">●</span><span class="sxs-lookup"><span data-stu-id="98418-210">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-211">●</span><span class="sxs-lookup"><span data-stu-id="98418-211">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="98418-212">Unbegrenzter Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="98418-212">Unlimited setting storage space</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-213">●</span><span class="sxs-lookup"><span data-stu-id="98418-213">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-214">●</span><span class="sxs-lookup"><span data-stu-id="98418-214">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-215">●</span><span class="sxs-lookup"><span data-stu-id="98418-215">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="98418-216">●</span><span class="sxs-lookup"><span data-stu-id="98418-216">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-217">●</span><span class="sxs-lookup"><span data-stu-id="98418-217">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="98418-218">Auswahl der zu synchronisierenden App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="98418-218">Choice in which app settings to synchronize</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="98418-219">●</span><span class="sxs-lookup"><span data-stu-id="98418-219">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-220">●</span><span class="sxs-lookup"><span data-stu-id="98418-220">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="98418-221">Backup/Restore für IT-Experten</span><span class="sxs-lookup"><span data-stu-id="98418-221">Backup/Restore for IT Pro</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="98418-222">●</span><span class="sxs-lookup"><span data-stu-id="98418-222">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-223">Teilweise</span><span class="sxs-lookup"><span data-stu-id="98418-223">Partial</span></span></p></td>
<td align="left"><p><span data-ttu-id="98418-224">●</span><span class="sxs-lookup"><span data-stu-id="98418-224">●</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="98418-225">UE-V 2. x – Anmerkungen zu dieser Version</span><span class="sxs-lookup"><span data-stu-id="98418-225">UE-V 2.x Release Notes</span></span>


<span data-ttu-id="98418-226">Weitere Informationen und aktuelle Nachrichten, die nicht in die Dokumentation eingehen, finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="98418-226">For more information, and for late-breaking news that did not make it into the documentation, see</span></span>

-   [<span data-ttu-id="98418-227">Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.1 SP1</span><span class="sxs-lookup"><span data-stu-id="98418-227">Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

-   [<span data-ttu-id="98418-228">Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.1</span><span class="sxs-lookup"><span data-stu-id="98418-228">Microsoft User Experience Virtualization (UE-V) 2.1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

-   [<span data-ttu-id="98418-229">Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.0</span><span class="sxs-lookup"><span data-stu-id="98418-229">Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

## <span data-ttu-id="98418-230">Weitere Ressourcen für dieses Produkt</span><span class="sxs-lookup"><span data-stu-id="98418-230">Other resources for this product</span></span>


-   [<span data-ttu-id="98418-231">Erste Schritte mit UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="98418-231">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="98418-232">Vorbereiten einer UE-V 2. x-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="98418-232">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [<span data-ttu-id="98418-233">Verwalten von UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="98418-233">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="98418-234">Problembehandlung bei UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="98418-234">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="98418-235">Technische Referenz für UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="98418-235">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

### <span data-ttu-id="98418-236">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="98418-236">More information</span></span>

<a href="" id="mdop-techcenter-page"></a><span data-ttu-id="98418-237">[MDOP-TechCenter-Seite](https://go.microsoft.com/fwlink/p/?LinkId=225286) Informieren Sie sich über die neuesten MDOP-Informationen und-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="98418-237">[MDOP TechCenter Page](https://go.microsoft.com/fwlink/p/?LinkId=225286) Learn about the latest MDOP information and resources.</span></span>

<a href="" id="mdop-information-experience"></a><span data-ttu-id="98418-238">[MDOP-Informations Erfahrung](https://go.microsoft.com/fwlink/p/?LinkId=236032) Finden Sie Dokumentation, Videos und andere Ressourcen für MDOP-Technologien.</span><span class="sxs-lookup"><span data-stu-id="98418-238">[MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) Find documentation, videos, and other resources for MDOP technologies.</span></span> <span data-ttu-id="98418-239">Sie können [uns auch Feedback senden](mailto:MDOPDocs@microsoft.com) oder Informationen zu Updates erhalten, indem Sie uns auf [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) oder [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447)folgen.</span><span class="sxs-lookup"><span data-stu-id="98418-239">You can also [send us feedback](mailto:MDOPDocs@microsoft.com) or learn about updates by following us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>














