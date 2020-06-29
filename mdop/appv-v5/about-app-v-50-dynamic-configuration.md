---
title: Informationen zur dynamischen Konfiguration in App-V 5.0
description: Informationen zur dynamischen Konfiguration in App-V 5.0
author: dansimp
ms.assetid: 88afaca1-68c5-45c4-a074-9371c56b5804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0294a60570d6dea99193c8bd411639c4888ae6b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806144"
---
# <span data-ttu-id="ac94c-103">Informationen zur dynamischen Konfiguration in App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ac94c-103">About App-V 5.0 Dynamic Configuration</span></span>


<span data-ttu-id="ac94c-104">Sie können die dynamische Konfiguration verwenden, um ein App-V 5,0-Paket für einen Benutzer anzupassen.</span><span class="sxs-lookup"><span data-stu-id="ac94c-104">You can use the dynamic configuration to customize an App-V 5.0 package for a user.</span></span> <span data-ttu-id="ac94c-105">Verwenden Sie die folgenden Informationen, um eine vorhandene dynamische Konfigurationsdatei zu erstellen oder zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ac94c-105">Use the following information to create or edit an existing dynamic configuration file.</span></span>

<span data-ttu-id="ac94c-106">Wenn Sie die dynamische Konfigurationsdatei bearbeiten, passt Sie an, wie ein App-V 5,0-Paket für einen Benutzer oder eine Gruppe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac94c-106">When you edit the dynamic configuration file it customizes how an App-V 5.0 package will run for a user or group.</span></span> <span data-ttu-id="ac94c-107">Auf diese Weise können Sie eine bequemere Methode für die Paket Anpassung bereitstellen, indem Sie die Notwendigkeit, Pakete mithilfe der gewünschten Einstellungen neu zu sequenzieren, entfernen und eine Möglichkeit bieten, Paketinhalte und benutzerdefinierte Einstellungen unabhängig zu halten.</span><span class="sxs-lookup"><span data-stu-id="ac94c-107">This helps to provide a more convenient method for package customization by removing the need to re-sequence packages using the desired settings, and provides a way to keep package content and custom settings independent.</span></span>

## <span data-ttu-id="ac94c-108">Erweitert: dynamische Konfiguration</span><span class="sxs-lookup"><span data-stu-id="ac94c-108">Advanced: Dynamic Configuration</span></span>


<span data-ttu-id="ac94c-109">Virtuelle Anwendungspakete enthalten ein Manifest, das alle Kerninformationen für das Paket enthält.</span><span class="sxs-lookup"><span data-stu-id="ac94c-109">Virtual application packages contain a manifest that provides all the core information for the package.</span></span> <span data-ttu-id="ac94c-110">Diese Informationen enthalten die Standardeinstellungen für die Paketeinstellungen und bestimmen die Einstellungen in der grundlegendsten Form (ohne zusätzliche Anpassung).</span><span class="sxs-lookup"><span data-stu-id="ac94c-110">This information includes the defaults for the package settings and determines settings in the most basic form (with no additional customization).</span></span> <span data-ttu-id="ac94c-111">Wenn Sie diese Standardeinstellungen für einen bestimmten Benutzer oder eine bestimmte Gruppe anpassen möchten, können Sie die folgenden Dateien erstellen und bearbeiten:</span><span class="sxs-lookup"><span data-stu-id="ac94c-111">If you want to adjust these defaults for a particular user or group, you can create and edit the following files:</span></span>

-   <span data-ttu-id="ac94c-112">Benutzerkonfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="ac94c-112">User Configuration file</span></span>

-   <span data-ttu-id="ac94c-113">Konfigurationsdatei für die Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="ac94c-113">Deployment configuration file</span></span>

<span data-ttu-id="ac94c-114">Die vorherigen XML-Dateien geben Paketeinstellungen an, sodass Pakete angepasst werden können, ohne die Pakete direkt zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="ac94c-114">The previous .xml files specify package settings and allow for packages to be customized without directly affecting the packages.</span></span> <span data-ttu-id="ac94c-115">Beim Erstellen eines Pakets generiert der Sequencer automatisch Standard Bereitstellungs-und Benutzer Konfigurations XML-Dateien mit den Daten des paketmanifests.</span><span class="sxs-lookup"><span data-stu-id="ac94c-115">When a package is created, the sequencer automatically generates default deployment and user configuration .xml files using the package manifest data.</span></span> <span data-ttu-id="ac94c-116">Aus diesem Grund spiegeln diese automatisch generierten Konfigurationsdateien einfach die Standardeinstellungen wider, die das Paket von der Art der Konfiguration während der Sequenzierung abbildet.</span><span class="sxs-lookup"><span data-stu-id="ac94c-116">Therefore, these automatically generated configuration files simply reflect the default settings that the package innately as from how things were configured during sequencing.</span></span> <span data-ttu-id="ac94c-117">Wenn Sie diese Konfigurationsdateien auf ein Paket in dem vom Sequencer generierten Formular anwenden, verfügen die Pakete über die gleichen Standardeinstellungen, die aus ihrem Manifest stammen.</span><span class="sxs-lookup"><span data-stu-id="ac94c-117">If you apply these configuration files to a package in the form generated by the sequencer, the packages will have the same default settings that came from their manifest.</span></span> <span data-ttu-id="ac94c-118">Dadurch erhalten Sie eine Paket spezifische Vorlage, mit der Sie beginnen können, wenn eine der Standardeinstellungen geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="ac94c-118">This provides you with a package-specific template to get started if any of the defaults must be changed.</span></span>

<span data-ttu-id="ac94c-119">**Hinweis**  Die folgenden Informationen können nur verwendet werden, um sequenzierte Sequenzer-Konfigurationsdateien zu ändern, um Pakete anzupassen, um bestimmte Benutzer-oder Gruppenanforderungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="ac94c-119">**Note** The following information can only be used to modify sequencer generated configuration files to customize packages to meet specific user or group requirements.</span></span>

 

### <span data-ttu-id="ac94c-120">Inhalt der dynamischen Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="ac94c-120">Dynamic Configuration file contents</span></span>

<span data-ttu-id="ac94c-121">Alle Ergänzungen, Löschungen und Aktualisierungen in den Konfigurationsdateien müssen in Bezug auf die Standardwerte erfolgen, die durch die Manifestinformationen des Pakets angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ac94c-121">All of the additions, deletions, and updates in the configuration files need to be made in relation to the default values specified by the package's manifest information.</span></span> <span data-ttu-id="ac94c-122">Überprüfen Sie die folgende Tabelle:</span><span class="sxs-lookup"><span data-stu-id="ac94c-122">Review the following table:</span></span>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac94c-123">Datei "User Configuration. xml"</span><span class="sxs-lookup"><span data-stu-id="ac94c-123">User Configuration .xml file</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac94c-124">Datei "Deployment Configuration. xml"</span><span class="sxs-lookup"><span data-stu-id="ac94c-124">Deployment Configuration .xml file</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac94c-125">Paket Manifest</span><span class="sxs-lookup"><span data-stu-id="ac94c-125">Package Manifest</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ac94c-126">Die vorherige Tabelle zeigt, wie die Dateien gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="ac94c-126">The previous table represents how the files will be read.</span></span> <span data-ttu-id="ac94c-127">Der erste Eintrag stellt dar, was zuletzt gelesen wird, daher hat sein Inhalt Vorrang.</span><span class="sxs-lookup"><span data-stu-id="ac94c-127">The first entry represents what will be read last, therefore, its content takes precedence.</span></span> <span data-ttu-id="ac94c-128">Daher enthalten alle Pakete inhärente und Standardeinstellungen aus dem Paketmanifest.</span><span class="sxs-lookup"><span data-stu-id="ac94c-128">Therefore, all packages inherently contain and provide default settings from the package manifest.</span></span> <span data-ttu-id="ac94c-129">Wenn eine XML-Datei für die Bereitstellungskonfiguration mit angepassten Einstellungen angewendet wird, werden die Standardwerte des paketmanifests außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="ac94c-129">If a deployment configuration .xml file with customized settings is applied, it will override the package manifest defaults.</span></span> <span data-ttu-id="ac94c-130">Wenn zuvor eine XML-Datei vom Benutzer "Configuration. xml" mit angepassten Einstellungen angewendet wird, werden sowohl die Bereitstellungskonfiguration als auch die Standardwerte des paketmanifests außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="ac94c-130">If a user configuration .xml file with customized settings is applied prior to that, it will override both the deployment configuration and the package manifest defaults.</span></span>

<span data-ttu-id="ac94c-131">In der folgenden Liste werden weitere Informationen zu den beiden Dateitypen angezeigt:</span><span class="sxs-lookup"><span data-stu-id="ac94c-131">The following list displays more information about the two file types:</span></span>

-   <span data-ttu-id="ac94c-132">**User Configuration File (userconfig)** – ermöglicht Ihnen, benutzerdefinierte Einstellungen für ein Paket anzugeben oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ac94c-132">**User Configuration File (UserConfig)** – Allows you to specify or modify custom settings for a package.</span></span> <span data-ttu-id="ac94c-133">Diese Einstellungen werden für einen bestimmten Benutzer angewendet, wenn das Paket auf einem Computer mit dem App-V 5,0-Client bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ac94c-133">These settings will be applied for a specific user when the package is deployed to a computer running the App-V 5.0 client.</span></span>

-   <span data-ttu-id="ac94c-134">**Deployment Configuration File (DeploymentConfig)** – ermöglicht Ihnen, die Standardeinstellungen für ein Paket anzugeben oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ac94c-134">**Deployment Configuration File (DeploymentConfig)** – Allows you to specify or modify the default settings for a package.</span></span> <span data-ttu-id="ac94c-135">Diese Einstellungen werden für alle Benutzer angewendet, wenn ein Paket auf einem Computer mit dem App-V 5,0-Client bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ac94c-135">These settings will be applied for all users when a package is deployed to a computer running the App-V 5.0 client.</span></span>

<span data-ttu-id="ac94c-136">Um die Einstellungen für ein Paket für eine bestimmte Gruppe von Benutzern auf einem Computer anzupassen oder um Änderungen vorzunehmen, die auf lokale Benutzerspeicherorte wie HKCU angewendet werden, sollte die userconfig-Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac94c-136">To customize the settings for a package for a specific set of users on a computer or to make changes that will be applied to local user locations such as HKCU, the UserConfig file should be used.</span></span> <span data-ttu-id="ac94c-137">Wenn Sie die Standardeinstellungen eines Pakets für alle Benutzer auf einem Computer ändern oder Änderungen vornehmen möchten, die auf globale Speicherorte wie HKEY \ _LOCAL \ _MACHINE und den Ordner alle Benutzer angewendet werden, sollte die DeploymentConfig-Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac94c-137">To modify the default settings of a package for all users on a machine or to make changes that will be applied to global locations such as HKEY\_LOCAL\_MACHINE and the all users folder, the DeploymentConfig file should be used.</span></span>

<span data-ttu-id="ac94c-138">Die userconfig-Datei enthält Konfigurationseinstellungen, die auf einen einzelnen Benutzer angewendet werden können, ohne dass dies Auswirkungen auf andere Benutzer auf einem Client hat:</span><span class="sxs-lookup"><span data-stu-id="ac94c-138">The UserConfig file provides configuration settings that can be applied to a single user without affecting any other users on a client:</span></span>

-   <span data-ttu-id="ac94c-139">Erweiterungen, die pro Benutzer in das System System integriert werden:-Verknüpfungen, Dateitypzuordnungen, URL-Protokolle, AppPaths, Software-Clients und com</span><span class="sxs-lookup"><span data-stu-id="ac94c-139">Extensions that will be integrated into the native system per user:- shortcuts, File-Type associations, URL Protocols, AppPaths, Software Clients and COM</span></span>

-   <span data-ttu-id="ac94c-140">Virtuelle Subsysteme:-Anwendungsobjekte, Umgebungsvariablen, Registrierungsänderungen, Dienste und Schriftarten</span><span class="sxs-lookup"><span data-stu-id="ac94c-140">Virtual Subsystems:- Application Objects, Environment variables, Registry modifications, Services and Fonts</span></span>

-   <span data-ttu-id="ac94c-141">Skripts (nur Benutzerkontext)</span><span class="sxs-lookup"><span data-stu-id="ac94c-141">Scripts (User context only)</span></span>

-   <span data-ttu-id="ac94c-142">Verwaltungsautorität (zum Steuern der Koexistenz von Paketen mit App-V 4,6)</span><span class="sxs-lookup"><span data-stu-id="ac94c-142">Managing Authority (for controlling co-existence of package with App-V 4.6)</span></span>

<span data-ttu-id="ac94c-143">Die DeploymentConfig-Datei enthält Konfigurationseinstellungen in zwei Abschnitten, eine relativ zum Computerkontext und eine relativ zum Benutzerkontext, in dem die gleichen Funktionen wie in der userconfig-Liste oben aufgeführt sind:</span><span class="sxs-lookup"><span data-stu-id="ac94c-143">The DeploymentConfig file provides configuration settings in two sections, one relative to the machine context and one relative to the user context providing the same capabilities listed in the UserConfig list above:</span></span>

-   <span data-ttu-id="ac94c-144">Alle userconfig-Einstellungen oben</span><span class="sxs-lookup"><span data-stu-id="ac94c-144">All UserConfig settings above</span></span>

-   <span data-ttu-id="ac94c-145">Erweiterungen, die nur global für alle Benutzer angewendet werden können</span><span class="sxs-lookup"><span data-stu-id="ac94c-145">Extensions that can only be applied globally for all users</span></span>

-   <span data-ttu-id="ac94c-146">Virtuelle Subsysteme, die für globale Computer Standorte konfiguriert werden können, beispielsweise Registry</span><span class="sxs-lookup"><span data-stu-id="ac94c-146">Virtual Subsystems that can be configured for global machine locations e.g. registry</span></span>

-   <span data-ttu-id="ac94c-147">Produkt Quell-URL</span><span class="sxs-lookup"><span data-stu-id="ac94c-147">Product Source URL</span></span>

-   <span data-ttu-id="ac94c-148">Skripts (nur Computerkontext)</span><span class="sxs-lookup"><span data-stu-id="ac94c-148">Scripts (Machine context only)</span></span>

-   <span data-ttu-id="ac94c-149">Steuerelemente zum kündigen von untergeordneten Prozessen</span><span class="sxs-lookup"><span data-stu-id="ac94c-149">Controls to Terminate Child Processes</span></span>

### <span data-ttu-id="ac94c-150">Dateistruktur</span><span class="sxs-lookup"><span data-stu-id="ac94c-150">File structure</span></span>

<span data-ttu-id="ac94c-151">Die Struktur der Dynamic Configuration-Datei der App-V 5,0 wird im folgenden Abschnitt erläutert.</span><span class="sxs-lookup"><span data-stu-id="ac94c-151">The structure of the App-V 5.0 Dynamic Configuration file is explained in the following section.</span></span>

### <span data-ttu-id="ac94c-152">Dynamic User-Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="ac94c-152">Dynamic User Configuration file</span></span>

<span data-ttu-id="ac94c-153">**Kopfzeile** : die Kopfzeile einer dynamischen Benutzerkonfigurationsdatei lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ac94c-153">**Header** - the header of a dynamic user configuration file is as follows:</span></span>

<span data-ttu-id="ac94c-154">&lt;? XML Version = "1.0" Encoding = "UTF-8"? &gt; &lt; UserConfiguration **Packaged**= "1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reserviert" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="ac94c-154">&lt;?xml version="1.0" encoding="utf-8"?&gt;&lt;UserConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>;</span></span>

<span data-ttu-id="ac94c-155">Die **Paket** -Nr ist derselbe Wert wie in der Manifestdatei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ac94c-155">The **PackageId** is the same value as exists in the Manifest file.</span></span>

<span data-ttu-id="ac94c-156">**Body** – der Text der dynamischen Benutzerkonfigurationsdatei kann alle in der Manifestdatei definierten App-Erweiterungspunkte sowie Informationen zum Konfigurieren virtueller Anwendungen umfassen.</span><span class="sxs-lookup"><span data-stu-id="ac94c-156">**Body** - the body of the Dynamic User Configuration file can include all the app extension points that are defined in the Manifest file, as well as information to configure virtual applications.</span></span> <span data-ttu-id="ac94c-157">Im Textbereich sind vier Unterabschnitte zulässig:</span><span class="sxs-lookup"><span data-stu-id="ac94c-157">There are four subsections allowed in the body:</span></span>

1. <span data-ttu-id="ac94c-158">**Anwendungen** – alle App-Erweiterungen, die in der Manifestdatei in einem Paket enthalten sind, werden mit einer Anwendungs-ID zugewiesen, die auch in der Manifestdatei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ac94c-158">**Applications** - All app-extensions that are contained in the Manifest file within a package are assigned with an Application ID, which is also defined in the manifest file.</span></span> <span data-ttu-id="ac94c-159">Dadurch können Sie alle Erweiterungen für eine bestimmte Anwendung innerhalb eines Pakets aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="ac94c-159">This allows you to enable or disable all the extensions for a given application within a package.</span></span> <span data-ttu-id="ac94c-160">Die **Anwendungs-ID** muss in der Manifestdatei vorhanden sein, oder Sie wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ac94c-160">The **Application ID** must exist in the Manifest file or it will be ignored.</span></span>

   <span data-ttu-id="ac94c-161">&lt;UserConfiguration **Packaged**= "1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reserviert" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="ac94c-161">&lt;UserConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>;</span></span>

   <span data-ttu-id="ac94c-162">&lt;Anwendungen&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-162">&lt;Applications&gt;</span></span>

   <span data-ttu-id="ac94c-163">&lt;!--Keine neue Anwendung in der Richtlinie definiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ac94c-163">&lt;!-- No new application can be defined in policy.</span></span> <span data-ttu-id="ac94c-164">AppV-Client ignoriert jede Anwendungs-ID, die sich nicht auch in der Manifestdatei befindet--&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-164">AppV Client will ignore any application ID that is not also in the Manifest file --&gt;</span></span>

   <span data-ttu-id="ac94c-165">&lt;Application ID = "{a56fa627-c35f-4a01-9e79-7d36aed8225a}" Enabled = "false"&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-165">&lt;Application Id="{a56fa627-c35f-4a01-9e79-7d36aed8225a}" Enabled="false"&gt;</span></span>

   <span data-ttu-id="ac94c-166">&lt;/Application&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-166">&lt;/Application&gt;</span></span>

   <span data-ttu-id="ac94c-167">&lt;/Applications&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-167">&lt;/Applications&gt;</span></span>

   <span data-ttu-id="ac94c-168">…</span><span class="sxs-lookup"><span data-stu-id="ac94c-168">…</span></span>

   <span data-ttu-id="ac94c-169">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-169">&lt;/UserConfiguration&gt;</span></span>

2. <span data-ttu-id="ac94c-170">**Subsysteme** -AppExtensions und andere Subsysteme sind unter den Teilsystemen als untergeordnete Knoten angeordnet &lt; &gt; :</span><span class="sxs-lookup"><span data-stu-id="ac94c-170">**Subsystems** - AppExtensions and other subsystems are arranged as subnodes under the &lt;Subsystems&gt;:</span></span>

   <span data-ttu-id="ac94c-171">&lt;UserConfiguration **Packaged**= "1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reserviert" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="ac94c-171">&lt;UserConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>;</span></span>

   <span data-ttu-id="ac94c-172">&lt;Subsysteme&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-172">&lt;Subsystems&gt;</span></span>

   <span data-ttu-id="ac94c-173">..</span><span class="sxs-lookup"><span data-stu-id="ac94c-173">..</span></span>

   <span data-ttu-id="ac94c-174">&lt;/Subsystems&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-174">&lt;/Subsystems&gt;</span></span>

   <span data-ttu-id="ac94c-175">..</span><span class="sxs-lookup"><span data-stu-id="ac94c-175">..</span></span>

   <span data-ttu-id="ac94c-176">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-176">&lt;/UserConfiguration&gt;</span></span>

   <span data-ttu-id="ac94c-177">Jedes Subsystem kann mithilfe des Attributs "**Enabled**" aktiviert/deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="ac94c-177">Each subsystem can be enabled/disabled using the “**Enabled**” attribute.</span></span> <span data-ttu-id="ac94c-178">Nachfolgend sind die verschiedenen Subsysteme und Verwendungsbeispiele aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac94c-178">Below are the various subsystems and usage samples.</span></span>

   **<span data-ttu-id="ac94c-179">Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="ac94c-179">Extensions:</span></span>**

   <span data-ttu-id="ac94c-180">Einige Subsysteme (Erweiterungs Subsysteme)-Steuerelement Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="ac94c-180">Some subsystems (Extension Subsystems) control Extensions.</span></span> <span data-ttu-id="ac94c-181">Diese Subsysteme sind:-Verknüpfungen, Dateitypzuordnungen, URL-Protokolle, AppPaths, Software-Clients und com</span><span class="sxs-lookup"><span data-stu-id="ac94c-181">Those subsystems are:- shortcuts, File-Type associations, URL Protocols, AppPaths, Software Clients and COM</span></span>

   <span data-ttu-id="ac94c-182">Erweiterungs Subsysteme können unabhängig vom Inhalt aktiviert und deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="ac94c-182">Extension Subsystems can be enabled and disabled independently of the content.</span></span>  <span data-ttu-id="ac94c-183">Wenn Tastenkombinationen aktiviert sind, verwendet der Clientstandard mäßig die Verknüpfungen, die im Manifest enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ac94c-183">Thus if Shortcuts are enabled, The client will use the shortcuts contained within the manifest by default.</span></span> <span data-ttu-id="ac94c-184">Jedes Erweiterungs Subsystem kann einen &lt; Erweiterungsknoten enthalten &gt; .</span><span class="sxs-lookup"><span data-stu-id="ac94c-184">Each Extension Subsystem can contain an &lt;Extensions&gt; node.</span></span> <span data-ttu-id="ac94c-185">Wenn dieses untergeordnete Element vorhanden ist, wird der Client den Inhalt in der Manifestdatei für dieses Subsystem ignorieren und nur den Inhalt der Konfigurationsdatei verwenden.</span><span class="sxs-lookup"><span data-stu-id="ac94c-185">If this child element is present, the client will ignore the content in the Manifest file for that subsystem and only use the content in the configuration file.</span></span>

   <span data-ttu-id="ac94c-186">Beispiel für die Verwendung des Subsystems "Verknüpfungen":</span><span class="sxs-lookup"><span data-stu-id="ac94c-186">Example using the shortcuts subsystem:</span></span>

   1.  <span data-ttu-id="ac94c-187">Wenn der Benutzer dies in der Dynamic-oder Deployment config-Datei definiert hat:</span><span class="sxs-lookup"><span data-stu-id="ac94c-187">If the user defined this in either the dynamic or deployment config file:</span></span>

                                    **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions&gt;**

                                                 ...

                                                **&lt;/Extensions&gt;**

                                    **&lt;/Shortcuts&gt;**

                         Content in the manifest will be ignored.   

   2.  <span data-ttu-id="ac94c-188">Wenn der Benutzer nur Folgendes definiert hat:</span><span class="sxs-lookup"><span data-stu-id="ac94c-188">If the user defined only the following:</span></span>

                                   **&lt;Shortcuts  Enabled="true"/&gt;**

                         Then the content in the Manifest will be integrated during publishing.

   3.  <span data-ttu-id="ac94c-189">Wenn der Benutzer Folgendes definiert:</span><span class="sxs-lookup"><span data-stu-id="ac94c-189">If the user defines the following</span></span>

                                  **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions/&gt;**

                                    **&lt;/Shortcuts&gt;**

   <span data-ttu-id="ac94c-190">Dann werden alle Tastenkombinationen im Manifest weiterhin ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ac94c-190">Then all the shortcuts within the manifest will still be ignored.</span></span> <span data-ttu-id="ac94c-191">Es werden keine Tastenkombinationen integriert.</span><span class="sxs-lookup"><span data-stu-id="ac94c-191">There will be no shortcuts integrated.</span></span>

   <span data-ttu-id="ac94c-192">Die unterstützten Erweiterungs Subsysteme sind:</span><span class="sxs-lookup"><span data-stu-id="ac94c-192">The supported Extension Subsystems are:</span></span>

   <span data-ttu-id="ac94c-193">**Tastenkombinationen:** Damit werden Tastenkombinationen gesteuert, die in das lokale System integriert werden.</span><span class="sxs-lookup"><span data-stu-id="ac94c-193">**Shortcuts:** This controls shortcuts that will be integrated into the local system.</span></span> <span data-ttu-id="ac94c-194">Nachfolgend finden Sie ein Beispiel mit zwei Tastenkombinationen:</span><span class="sxs-lookup"><span data-stu-id="ac94c-194">Below is a sample with 2 shortcuts:</span></span>

   <span data-ttu-id="ac94c-195">&lt;Subsysteme&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-195">&lt;Subsystems&gt;</span></span>

   <span data-ttu-id="ac94c-196">&lt;Tastenkombinationen aktiviert = "wahr"&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-196">&lt;Shortcuts Enabled="true"&gt;</span></span>

     <span data-ttu-id="ac94c-197">&lt;Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-197">&lt;Extensions&gt;</span></span>

       &lt;Extension Category="AppV.Shortcut"&gt;

         &lt;Shortcut&gt;

           &lt;File&gt;\[{Common Programs}\]\\Microsoft Contoso\\Microsoft ContosoApp Filler 2010.lnk&lt;/File&gt;

           &lt;Target&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/Target&gt;

           &lt;Icon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\inficon.exe&lt;/Icon&gt;

           &lt;Arguments /&gt;

           &lt;WorkingDirectory /&gt;

           &lt;AppUserModelId&gt;ContosoApp.Filler.3&lt;/AppUserModelId&gt;

           &lt;Description&gt;Fill out dynamic forms to gather and reuse information throughout the organization using Microsoft ContosoApp.&lt;/Description&gt;

           &lt;Hotkey&gt;0&lt;/Hotkey&gt;

           &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

           &lt;ApplicationId&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/ApplicationId&gt;

         &lt;/Shortcut&gt;

     <span data-ttu-id="ac94c-198">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-198">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="ac94c-199">&lt;Erweiterungskategorie = "AppV. Verknüpfung"&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-199">&lt;Extension Category="AppV.Shortcut"&gt;</span></span>

       &lt;Shortcut&gt;

         &lt;File&gt;\[{AppData}\]\\Microsoft\\Contoso\\Recent\\Templates.LNK&lt;/File&gt;

         &lt;Target&gt;\[{AppData}\]\\Microsoft\\Templates&lt;/Target&gt;

         &lt;Icon /&gt;

         &lt;Arguments /&gt;

         &lt;WorkingDirectory /&gt;

         &lt;AppUserModelId /&gt;

         &lt;Description /&gt;

         &lt;Hotkey&gt;0&lt;/Hotkey&gt;

         &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

         &lt;!-- Note the ApplicationId is optional --&gt;

       &lt;/Shortcut&gt;

     <span data-ttu-id="ac94c-200">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-200">&lt;/Extension&gt;</span></span>

    <span data-ttu-id="ac94c-201">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-201">&lt;/Extensions&gt;</span></span>

   <span data-ttu-id="ac94c-202">&lt;/Shortcuts&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-202">&lt;/Shortcuts&gt;</span></span>

   <span data-ttu-id="ac94c-203">**Dateitypzuordnungen:** Ordnet Dateitypen mit Programmen zu, die standardmäßig geöffnet werden sollen, sowie das Kontextmenü einrichten.</span><span class="sxs-lookup"><span data-stu-id="ac94c-203">**File-Type Associations:** Associates File-types with programs to open by default as well as setup the context menu.</span></span> <span data-ttu-id="ac94c-204">(MIME-Typen können auch mit diesem susbsystem eingerichtet werden).</span><span class="sxs-lookup"><span data-stu-id="ac94c-204">(MIME types can also be setup using this susbsystem).</span></span> <span data-ttu-id="ac94c-205">Beispiel für eine Dateitypzuordnung:</span><span class="sxs-lookup"><span data-stu-id="ac94c-205">Sample File-type Association is below:</span></span>

   <span data-ttu-id="ac94c-206">&lt;FileTypeAssociations Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-206">&lt;FileTypeAssociations Enabled="true"&gt;</span></span>

   <span data-ttu-id="ac94c-207">&lt;Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-207">&lt;Extensions&gt;</span></span>

     <span data-ttu-id="ac94c-208">&lt;Erweiterungskategorie = "AppV. FileTypeAssociation"&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-208">&lt;Extension Category="AppV.FileTypeAssociation"&gt;</span></span>

       &lt;FileTypeAssociation&gt;

         &lt;FileExtension MimeAssociation="true"&gt;

         &lt;Name&gt;.docm&lt;/Name&gt;

         &lt;ProgId&gt;contosowordpad.DocumentMacroEnabled.12&lt;/ProgId&gt;

         &lt;PerceivedType&gt;document&lt;/PerceivedType&gt;

         &lt;ContentType&gt;application/vnd.ms-contosowordpad.document.macroEnabled.12&lt;/ContentType&gt;

         &lt;OpenWithList&gt;

           &lt;ApplicationName&gt;wincontosowordpad.exe&lt;/ApplicationName&gt;

         &lt;/OpenWithList&gt;

        &lt;OpenWithProgIds&gt;

           &lt;ProgId&gt;contosowordpad.8&lt;/ProgId&gt;

         &lt;/OpenWithProgIds&gt;

         &lt;ShellNew&gt;

           &lt;Command /&gt;

           &lt;DataBinary /&gt;

           &lt;DataText /&gt;

           &lt;FileName /&gt;

           &lt;NullFile&gt;true&lt;/NullFile&gt;

           &lt;ItemName /&gt;

           &lt;IconPath /&gt;

           &lt;MenuText /&gt;

           &lt;Handler /&gt;

         &lt;/ShellNew&gt;

       &lt;/FileExtension&gt;

       &lt;ProgId&gt;

          &lt;Name&gt;contosowordpad.DocumentMacroEnabled.12&lt;/Name&gt;

           &lt;DefaultIcon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\contosowordpadicon.exe,15&lt;/DefaultIcon&gt;

           &lt;Description&gt;Blah Blah Blah&lt;/Description&gt;

           &lt;FriendlyTypeName&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,9182&lt;/FriendlyTypeName&gt;

           &lt;InfoTip&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,1424&lt;/InfoTip&gt;

           &lt;EditFlags&gt;0&lt;/EditFlags&gt;

           &lt;ShellCommands&gt;

             &lt;DefaultCommand&gt;Open&lt;/DefaultCommand&gt;

             &lt;ShellCommand&gt;

                &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

                &lt;Name&gt;Edit&lt;/Name&gt;

                &lt;FriendlyName&gt;&Edit&lt;/FriendlyName&gt;

                &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /vu "%1"&lt;/CommandLine&gt;

             &lt;/ShellCommand&gt;

             &lt;/ShellCommand&gt;

               &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

               &lt;Name&gt;Open&lt;/Name&gt;

               &lt;FriendlyName&gt;&Open&lt;/FriendlyName&gt;

               &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /n "%1"&lt;/CommandLine&gt;

               &lt;DropTargetClassId /&gt;

               &lt;DdeExec&gt;

                 &lt;Application&gt;mscontosowordpad&lt;/Application&gt;

                 &lt;Topic&gt;ShellSystem&lt;/Topic&gt;

                 &lt;IfExec&gt;\[SHELLNOOP\]&lt;/IfExec&gt;

                 &lt;DdeCommand&gt;\[SetForeground\]\[ShellNewDatabase "%1"\]&lt;/DdeCommand&gt;

               &lt;/DdeExec&gt;

             &lt;/ShellCommand&gt;

           &lt;/ShellCommands&gt;

         &lt;/ProgId&gt;

        &lt;/FileTypeAssociation&gt;

      <span data-ttu-id="ac94c-209">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-209">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="ac94c-210">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-210">&lt;/Extensions&gt;</span></span>

     <span data-ttu-id="ac94c-211">&lt;/FileTypeAssociations&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-211">&lt;/FileTypeAssociations&gt;</span></span>

   <span data-ttu-id="ac94c-212">**URL-Protokolle**: dies steuert die URL-Protokolle, die in die lokale Registrierung des Clientcomputers integriert sind, beispielsweise "mailto:".</span><span class="sxs-lookup"><span data-stu-id="ac94c-212">**URL Protocols**: This controls the URL Protocols that are integrated into the local registry of the client machine e.g. “mailto:”.</span></span>

   <span data-ttu-id="ac94c-213">&lt;URLProtocols Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-213">&lt;URLProtocols Enabled="true"&gt;</span></span>

   <span data-ttu-id="ac94c-214">&lt;Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-214">&lt;Extensions&gt;</span></span>

   <span data-ttu-id="ac94c-215">&lt;Erweiterungskategorie = "AppV. URLProtocol"&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-215">&lt;Extension Category="AppV.URLProtocol"&gt;</span></span>

   <span data-ttu-id="ac94c-216">&lt;URLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-216">&lt;URLProtocol&gt;</span></span>

     <span data-ttu-id="ac94c-217">&lt;Name &gt; mailto &lt; /Name&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-217">&lt;Name&gt;mailto&lt;/Name&gt;</span></span>

     <span data-ttu-id="ac94c-218">&lt;ApplicationURLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-218">&lt;ApplicationURLProtocol&gt;</span></span>

     <span data-ttu-id="ac94c-219">&lt;DefaultIcon &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE,-9403 &lt; /DefaultIcon&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-219">&lt;DefaultIcon&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE,-9403&lt;/DefaultIcon&gt;</span></span>

     <span data-ttu-id="ac94c-220">&lt;EditFlags &gt; 2 &lt; /EditFlags&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-220">&lt;EditFlags&gt;2&lt;/EditFlags&gt;</span></span>

     <span data-ttu-id="ac94c-221">&lt;Beschreibung&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-221">&lt;Description /&gt;</span></span>

     <span data-ttu-id="ac94c-222">&lt;AppUserModelId&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-222">&lt;AppUserModelId /&gt;</span></span>

     <span data-ttu-id="ac94c-223">&lt;FriendlyTypeName /&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-223">&lt;FriendlyTypeName /&gt;</span></span>

     <span data-ttu-id="ac94c-224">&lt;Infotipp&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-224">&lt;InfoTip /&gt;</span></span>

   <span data-ttu-id="ac94c-225">&lt;SourceFilter&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-225">&lt;SourceFilter /&gt;</span></span>

     <span data-ttu-id="ac94c-226">&lt;ShellFolder /&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-226">&lt;ShellFolder /&gt;</span></span>

     <span data-ttu-id="ac94c-227">&lt;WebNavigableCLSID /&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-227">&lt;WebNavigableCLSID /&gt;</span></span>

     <span data-ttu-id="ac94c-228">&lt;ExplorerFlags &gt; 2 &lt; /ExplorerFlags&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-228">&lt;ExplorerFlags&gt;2&lt;/ExplorerFlags&gt;</span></span>

     <span data-ttu-id="ac94c-229">&lt;CLSID&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-229">&lt;CLSID /&gt;</span></span>

     <span data-ttu-id="ac94c-230">&lt;ShellCommands&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-230">&lt;ShellCommands&gt;</span></span>

     <span data-ttu-id="ac94c-231">&lt;DefaultCommand &gt; Open &lt; /DefaultCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-231">&lt;DefaultCommand&gt;open&lt;/DefaultCommand&gt;</span></span>

     <span data-ttu-id="ac94c-232">&lt;ShellCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-232">&lt;ShellCommand&gt;</span></span>

     <span data-ttu-id="ac94c-233">&lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationId&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-233">&lt;ApplicationId&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE&lt;/ApplicationId&gt;</span></span>

     <span data-ttu-id="ac94c-234">&lt;Namen &gt; Öffnen &lt; /Name&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-234">&lt;Name&gt;open&lt;/Name&gt;</span></span>

     <span data-ttu-id="ac94c-235">&lt;CommandLine &gt; \ [{ProgramFilesX86} \\Microsoft Contoso\\Contoso\\contosomail.EXE "-c OEP. Hinweis/m "%1" &lt; /CommandLine&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-235">&lt;CommandLine&gt;\[{ProgramFilesX86}\\Microsoft Contoso\\Contoso\\contosomail.EXE" -c OEP.Note /m "%1"&lt;/CommandLine&gt;</span></span>

     <span data-ttu-id="ac94c-236">&lt;DropTargetClassId /&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-236">&lt;DropTargetClassId /&gt;</span></span>

     <span data-ttu-id="ac94c-237">&lt;FriendlyName&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-237">&lt;FriendlyName /&gt;</span></span>

     <span data-ttu-id="ac94c-238">&lt;Erweiterter &gt; 0- &lt; /Extended&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-238">&lt;Extended&gt;0&lt;/Extended&gt;</span></span>

     <span data-ttu-id="ac94c-239">&lt;LegacyDisable &gt; 0 &lt; /LegacyDisable&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-239">&lt;LegacyDisable&gt;0&lt;/LegacyDisable&gt;</span></span>

     <span data-ttu-id="ac94c-240">&lt;SuppressionPolicy &gt; 2 &lt; /SuppressionPolicy&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-240">&lt;SuppressionPolicy&gt;2&lt;/SuppressionPolicy&gt;</span></span>

      <span data-ttu-id="ac94c-241">&lt;DdeExec&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-241">&lt;DdeExec&gt;</span></span>

     <span data-ttu-id="ac94c-242">&lt;NoActivateHandler /&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-242">&lt;NoActivateHandler /&gt;</span></span>

     <span data-ttu-id="ac94c-243">&lt;Application &gt; contosomail &lt; /Application&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-243">&lt;Application&gt;contosomail&lt;/Application&gt;</span></span>

     <span data-ttu-id="ac94c-244">&lt;Topic &gt; ShellSystem &lt; /Topic&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-244">&lt;Topic&gt;ShellSystem&lt;/Topic&gt;</span></span>

     <span data-ttu-id="ac94c-245">&lt;IfExec &gt; \ [SHELLNOOP \] &lt; /IfExec&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-245">&lt;IfExec&gt;\[SHELLNOOP\]&lt;/IfExec&gt;</span></span>

     <span data-ttu-id="ac94c-246">&lt;DdeCommand &gt; \ [SetForeground \] \ [ShellNewDatabase "%1" \] &lt; /DdeCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-246">&lt;DdeCommand&gt;\[SetForeground\]\[ShellNewDatabase "%1"\]&lt;/DdeCommand&gt;</span></span>

     <span data-ttu-id="ac94c-247">&lt;/DdeExec&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-247">&lt;/DdeExec&gt;</span></span>

     <span data-ttu-id="ac94c-248">&lt;/ShellCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-248">&lt;/ShellCommand&gt;</span></span>

     <span data-ttu-id="ac94c-249">&lt;/ShellCommands&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-249">&lt;/ShellCommands&gt;</span></span>

     <span data-ttu-id="ac94c-250">&lt;/ApplicationURLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-250">&lt;/ApplicationURLProtocol&gt;</span></span>

     <span data-ttu-id="ac94c-251">&lt;/URLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-251">&lt;/URLProtocol&gt;</span></span>

     <span data-ttu-id="ac94c-252">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-252">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="ac94c-253">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-253">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="ac94c-254">&lt;/URLProtocols&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-254">&lt;/URLProtocols&gt;</span></span>

   <span data-ttu-id="ac94c-255">**Software-Clients**: ermöglicht es der APP, sich als e-Mail-Client, Nachrichten Leser, Media Player zu registrieren und die app in der UI "Programm Zugriff und Computer Standards festlegen" sichtbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="ac94c-255">**Software Clients**: Allows the app to register as an Email client, news reader, media player and makes the app visible in the Set Program Access and Computer Defaults UI.</span></span> <span data-ttu-id="ac94c-256">In den meisten Fällen müssen Sie diese Funktion nur aktivieren und deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="ac94c-256">In most cases you should only need to enable and disable it.</span></span> <span data-ttu-id="ac94c-257">Darüber hinaus gibt es ein Steuerelement zum Aktivieren und Deaktivieren des e-Mail-Clients, wenn die anderen Clients mit Ausnahme des Clients weiterhin aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ac94c-257">There is also a control to enable and disable the email client specifically if you want the other clients still enabled except for that client.</span></span>

   <span data-ttu-id="ac94c-258">&lt;SoftwareClients Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-258">&lt;SoftwareClients Enabled="true"&gt;</span></span>

     <span data-ttu-id="ac94c-259">&lt;ClientConfiguration EmailEnabled = "falsch"/&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-259">&lt;ClientConfiguration EmailEnabled="false" /&gt;</span></span>

   <span data-ttu-id="ac94c-260">&lt;/SoftwareClients&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-260">&lt;/SoftwareClients&gt;</span></span>

   <span data-ttu-id="ac94c-261">AppPaths:-Wenn eine Anwendung, beispielsweise contoso.exe, mit einem AppPath-Namen von "MyApp" registriert ist, können Sie "MyApp" unter dem Menü "ausführen" eingeben, und es wird contoso.exe geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ac94c-261">AppPaths:- If an application for example contoso.exe is registered with an apppath name of “myapp”, it allows you type “myapp” under the run menu and it will open contoso.exe.</span></span>

   <span data-ttu-id="ac94c-262">&lt;AppPaths Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-262">&lt;AppPaths Enabled="true"&gt;</span></span>

   <span data-ttu-id="ac94c-263">&lt;Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-263">&lt;Extensions&gt;</span></span>

   <span data-ttu-id="ac94c-264">&lt;Erweiterungskategorie = "AppV. AppPath"&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-264">&lt;Extension Category="AppV.AppPath"&gt;</span></span>

   <span data-ttu-id="ac94c-265">&lt;AppPath&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-265">&lt;AppPath&gt;</span></span>

     <span data-ttu-id="ac94c-266">&lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationId&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-266">&lt;ApplicationId&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE&lt;/ApplicationId&gt;</span></span>

     <span data-ttu-id="ac94c-267">&lt;Name &gt;contosomail.exe&lt; /Name&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-267">&lt;Name&gt;contosomail.exe&lt;/Name&gt;</span></span>

     <span data-ttu-id="ac94c-268">&lt;ApplicationPath &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /applicationPath&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-268">&lt;ApplicationPath&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE&lt;/ApplicationPath&gt;</span></span>

     <span data-ttu-id="ac94c-269">&lt;PATHEnvironmentVariablePrefix /&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-269">&lt;PATHEnvironmentVariablePrefix /&gt;</span></span>

     <span data-ttu-id="ac94c-270">&lt;CanAcceptUrl &gt; false &lt; /CanAcceptUrl&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-270">&lt;CanAcceptUrl&gt;false&lt;/CanAcceptUrl&gt;</span></span>

     <span data-ttu-id="ac94c-271">&lt;SaveUrl&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-271">&lt;SaveUrl /&gt;</span></span>

   <span data-ttu-id="ac94c-272">&lt;/AppPath&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-272">&lt;/AppPath&gt;</span></span>

   <span data-ttu-id="ac94c-273">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-273">&lt;/Extension&gt;</span></span>

   <span data-ttu-id="ac94c-274">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-274">&lt;/Extensions&gt;</span></span>

   <span data-ttu-id="ac94c-275">&lt;/AppPaths&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-275">&lt;/AppPaths&gt;</span></span>

   <span data-ttu-id="ac94c-276">**Com**: ermöglicht einer Anwendung das Registrieren lokaler COM-Server.</span><span class="sxs-lookup"><span data-stu-id="ac94c-276">**COM**: Allows an Application register Local COM servers.</span></span> <span data-ttu-id="ac94c-277">Der Modus kann integriert, isoliert oder deaktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="ac94c-277">Mode can be Integration, Isolated or Off.</span></span> <span data-ttu-id="ac94c-278">Wenn isol.</span><span class="sxs-lookup"><span data-stu-id="ac94c-278">When Isol.</span></span>

   <span data-ttu-id="ac94c-279">&lt;COM-Modus = "isoliert"/&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-279">&lt;COM Mode="Isolated"/&gt;</span></span>

   <span data-ttu-id="ac94c-280">**Weitere Einstellungen**:</span><span class="sxs-lookup"><span data-stu-id="ac94c-280">**Other Settings**:</span></span>

   <span data-ttu-id="ac94c-281">Neben Erweiterungen können auch andere Subsysteme aktiviert/deaktiviert und bearbeitet werden:</span><span class="sxs-lookup"><span data-stu-id="ac94c-281">In addition to Extensions, other subsystems can be enabled/disabled and edited:</span></span>

   <span data-ttu-id="ac94c-282">**Virtuelle Kernel Objekte**:</span><span class="sxs-lookup"><span data-stu-id="ac94c-282">**Virtual Kernel Objects**:</span></span>

   <span data-ttu-id="ac94c-283">&lt;Objekte aktiviert = "falsch"/&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-283">&lt;Objects Enabled="false" /&gt;</span></span>

   <span data-ttu-id="ac94c-284">**Virtuelle Registrierung**: wird verwendet, wenn Sie eine Registrierung in der virtuellen Registrierung in HKCU einrichten möchten.</span><span class="sxs-lookup"><span data-stu-id="ac94c-284">**Virtual Registry**: Used if you want to set a registry in the Virtual Registry within HKCU</span></span>

   <span data-ttu-id="ac94c-285">&lt;Registry Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-285">&lt;Registry Enabled="true"&gt;</span></span>

   <span data-ttu-id="ac94c-286">&lt;Enthalten&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-286">&lt;Include&gt;</span></span>

   <span data-ttu-id="ac94c-287">&lt;Key Path = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\ABC"&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-287">&lt;Key Path="\\REGISTRY\\USER\\\[{AppVCurrentUserSID}\]\\Software\\ABC"&gt;</span></span>

   <span data-ttu-id="ac94c-288">&lt;Value Type = "reg \ _SZ" Name = "Bar" Data = "Neuwert"/&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-288">&lt;Value Type="REG\_SZ" Name="Bar" Data="NewValue" /&gt;</span></span>

    <span data-ttu-id="ac94c-289">&lt;/Key&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-289">&lt;/Key&gt;</span></span>

     <span data-ttu-id="ac94c-290">&lt;Key Path = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\EmptyKey"/&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-290">&lt;Key Path="\\REGISTRY\\USER\\\[{AppVCurrentUserSID}\]\\Software\\EmptyKey" /&gt;</span></span>

    <span data-ttu-id="ac94c-291">&lt;/Include&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-291">&lt;/Include&gt;</span></span>

   <span data-ttu-id="ac94c-292">&lt;Löschen&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-292">&lt;Delete&gt;</span></span>

     <span data-ttu-id="ac94c-293">&lt;/Registry&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-293">&lt;/Registry&gt;</span></span>

   **<span data-ttu-id="ac94c-294">Virtuelles Datei System</span><span class="sxs-lookup"><span data-stu-id="ac94c-294">Virtual File System</span></span>**

         &lt;FileSystem Enabled="true" /&gt;

   **<span data-ttu-id="ac94c-295">Virtuelle Schriftarten</span><span class="sxs-lookup"><span data-stu-id="ac94c-295">Virtual Fonts</span></span>**

         &lt;Fonts Enabled="false" /&gt;

   **<span data-ttu-id="ac94c-296">Virtuelle Umgebungsvariablen</span><span class="sxs-lookup"><span data-stu-id="ac94c-296">Virtual Environment Variables</span></span>**

   <span data-ttu-id="ac94c-297">&lt;EnvironmentVariables Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-297">&lt;EnvironmentVariables Enabled="true"&gt;</span></span>

   <span data-ttu-id="ac94c-298">&lt;Enthalten&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-298">&lt;Include&gt;</span></span>

          &lt;Variable Name="UserPath" Value="%path%;%UserProfile%" /&gt;

          &lt;Variable Name="UserLib" Value="%UserProfile%\\ABC" /&gt;

          &lt;/Include&gt;

         &lt;Delete&gt;

          &lt;Variable Name="lib" /&gt;

           &lt;/Delete&gt;

           &lt;/EnvironmentVariables&gt;

   **<span data-ttu-id="ac94c-299">Virtuelle Dienste</span><span class="sxs-lookup"><span data-stu-id="ac94c-299">Virtual services</span></span>**

         &lt;Services Enabled="false" /&gt;

3. <span data-ttu-id="ac94c-300">**Userscripts** – Skripts können verwendet werden, um die virtuelle Umgebung einzurichten oder zu ändern sowie Skripts zum Zeitpunkt der Bereitstellung oder Entfernung auszuführen, bevor eine Anwendung ausgeführt wird, oder Sie können verwendet werden, um die Umgebung zu "bereinigen", nachdem die Anwendung beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ac94c-300">**UserScripts** – Scripts can be used to setup or alter the virtual environment as well as execute scripts at time of deployment or removal, before an application executes, or they can be used to “clean up” the environment after the application terminates.</span></span> <span data-ttu-id="ac94c-301">Verweisen Sie auf eine Beispielkonfigurationsdatei, die vom Sequencer ausgegeben wird, um ein Beispielskript anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ac94c-301">Please reference a sample User configuration file that is output by the sequencer to see a sample script.</span></span> <span data-ttu-id="ac94c-302">Im Abschnitt "Skripts" unten finden Sie weitere Informationen zu den verschiedenen Triggern, die verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ac94c-302">The Scripts section below provides more information on the various triggers that can be used.</span></span>

4. <span data-ttu-id="ac94c-303">**ManagingAuthority** – kann verwendet werden, wenn zwei Versionen Ihres Pakets auf demselben Computer nebeneinander vorhanden sind, eine für App-v 4,6 und die andere auf App-v 5,0 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ac94c-303">**ManagingAuthority** – Can be used when 2 versions of your package are co-existing on the same machine, one deployed to App-V 4.6 and the other deployed on App-V 5.0.</span></span> <span data-ttu-id="ac94c-304">Damit App-v vNext erhielten App-v 4,6-Erweiterungspunkte für das benannte Paket übernehmen kann, geben Sie Folgendes in die userconfig-Datei ein (wobei Paketname die Paket-GUID in App-v 4,6 ist:</span><span class="sxs-lookup"><span data-stu-id="ac94c-304">To Allow App-V vNext to take over App-V 4.6 extension points for the named package enter the following in the UserConfig file (where PackageName is the Package GUID in App-V 4.6:</span></span>

   <span data-ttu-id="ac94c-305">&lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PACKAGENAME = "032630c0-b8e2-417c-acef-76fc5297fe81"/&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-305">&lt;ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName="032630c0-b8e2-417c-acef-76fc5297fe81" /&gt;</span></span>

### <span data-ttu-id="ac94c-306">Konfigurationsdatei für dynamische Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="ac94c-306">Dynamic Deployment Configuration file</span></span>

<span data-ttu-id="ac94c-307">**Kopfzeile** : die Kopfzeile einer Konfigurationsdatei für die Bereitstellung lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ac94c-307">**Header** - The header of a Deployment Configuration file is as follows:</span></span>

<span data-ttu-id="ac94c-308">&lt;? XML Version = "1.0" Encoding = "UTF-8"? &gt; &lt; DeploymentConfiguration **Packaged**= "1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reserviert" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="ac94c-308">&lt;?xml version="1.0" encoding="utf-8"?&gt;&lt;DeploymentConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt>;</span></span>

<span data-ttu-id="ac94c-309">Die **Paket** -Nr ist derselbe Wert wie in der Manifestdatei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ac94c-309">The **PackageId** is the same value as exists in the manifest file.</span></span>

<span data-ttu-id="ac94c-310">**Body** – der Text der Bereitstellungs Konfigurationsdatei umfasst zwei Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="ac94c-310">**Body** - The body of the deployment configuration file includes two sections:</span></span>

-   <span data-ttu-id="ac94c-311">Abschnitt "Benutzerkonfiguration" – ermöglicht denselben Inhalt wie die im vorherigen Abschnitt beschriebene Benutzerkonfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="ac94c-311">User Configuration section –allows the same content as the User Configuration file described in the previous section.</span></span> <span data-ttu-id="ac94c-312">Wenn das Paket für einen Benutzer veröffentlicht wird, überschreiben alle appextensions-Konfigurationseinstellungen in diesem Abschnitt entsprechende Einstellungen im Manifest innerhalb des Pakets, es sei denn, es wird auch eine Benutzerkonfigurationsdatei bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ac94c-312">When the package is published to a user, any appextensions configuration settings in this section will override corresponding settings in the Manifest within the package unless a user configuration file is also provided.</span></span> <span data-ttu-id="ac94c-313">Wenn auch eine userconfig-Datei bereitgestellt wird, wird Sie anstelle der Benutzereinstellungen in der Konfigurationsdatei für die Bereitstellung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac94c-313">If a UserConfig file is also provided, it will be used instead of the User settings in the deployment configuration file.</span></span> <span data-ttu-id="ac94c-314">Wenn das Paket Global veröffentlicht wird, wird nur der Inhalt der Bereitstellungs Konfigurationsdatei in Verbindung mit dem Manifest verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac94c-314">If the package is published globally, then only the contents of the deployment configuration file will be used in combination with the manifest.</span></span>

-   <span data-ttu-id="ac94c-315">Abschnitt "Computerkonfiguration" – enthält Informationen, die nur für einen ganzen Computer konfiguriert werden können, und nicht für einen bestimmten Benutzer auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="ac94c-315">Machine Configuration section–contains information that can be configured only for an entire machine, not for a specific user on the machine.</span></span> <span data-ttu-id="ac94c-316">Beispiel: HKEY \ _LOCAL \ _MACHINE Registrierungsschlüssel in VFS.</span><span class="sxs-lookup"><span data-stu-id="ac94c-316">For example, HKEY\_LOCAL\_MACHINE registry keys in the VFS.</span></span>

<span data-ttu-id="ac94c-317">&lt;DeploymentConfiguration **Packaged**= "1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reserviert" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="ac94c-317">&lt;DeploymentConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt>;</span></span>

<span data-ttu-id="ac94c-318">&lt;UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-318">&lt;UserConfiguration&gt;</span></span>

  <span data-ttu-id="ac94c-319">..</span><span class="sxs-lookup"><span data-stu-id="ac94c-319">..</span></span>

<span data-ttu-id="ac94c-320">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-320">&lt;/UserConfiguration&gt;</span></span>

<span data-ttu-id="ac94c-321">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-321">&lt;MachineConfiguration&gt;</span></span>

<span data-ttu-id="ac94c-322">..</span><span class="sxs-lookup"><span data-stu-id="ac94c-322">..</span></span>

<span data-ttu-id="ac94c-323">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-323">&lt;/MachineConfiguration&gt;</span></span>

<span data-ttu-id="ac94c-324">..</span><span class="sxs-lookup"><span data-stu-id="ac94c-324">..</span></span>

<span data-ttu-id="ac94c-325">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-325">&lt;/MachineConfiguration&gt;</span></span>

<span data-ttu-id="ac94c-326">&lt;/DeploymentConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-326">&lt;/DeploymentConfiguration&gt;</span></span>

<span data-ttu-id="ac94c-327">**Benutzerkonfiguration** – verwenden Sie den vorherigen Abschnitt der **dynamischen Benutzerkonfigurationsdatei** , um Informationen zu den Einstellungen anzuzeigen, die im Abschnitt Benutzerkonfiguration der Bereitstellungs Konfigurationsdatei bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ac94c-327">**User Configuration** - use the previous **Dynamic User Configuration file** section for information on settings that are provided in the user configuration section of the Deployment Configuration file.</span></span>

<span data-ttu-id="ac94c-328">Computerkonfiguration – der Abschnitt "Computerkonfiguration" der Bereitstellungs Konfigurationsdatei dient zum Konfigurieren von Informationen, die nur für einen ganzen Computer festgesetzt werden können, und nicht für einen bestimmten Benutzer auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="ac94c-328">Machine Configuration - the Machine configuration section of the Deployment Configuration File is used to configure information that can be set only for an entire machine, not for a specific user on the computer.</span></span> <span data-ttu-id="ac94c-329">Beispiel: HKEY \ _LOCAL \ _MACHINE Registrierungsschlüssel in der virtuellen Registrierung.</span><span class="sxs-lookup"><span data-stu-id="ac94c-329">For example, HKEY\_LOCAL\_MACHINE registry keys in the Virtual Registry.</span></span> <span data-ttu-id="ac94c-330">Unter diesem Element sind vier Unterabschnitte zulässig.</span><span class="sxs-lookup"><span data-stu-id="ac94c-330">There are four subsections allowed in under this element</span></span>

1.  <span data-ttu-id="ac94c-331">**Subsysteme** -AppExtensions und andere Subsysteme sind als untergeordnete Knoten unter &lt; Subsysteme angeordnet &gt; :</span><span class="sxs-lookup"><span data-stu-id="ac94c-331">**Subsystems** - AppExtensions and other subsystems are arranged as subnodes under &lt;Subsystems&gt;:</span></span>

    <span data-ttu-id="ac94c-332">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-332">&lt;MachineConfiguration&gt;</span></span>

      <span data-ttu-id="ac94c-333">&lt;Subsysteme&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-333">&lt;Subsystems&gt;</span></span>

      <span data-ttu-id="ac94c-334">..</span><span class="sxs-lookup"><span data-stu-id="ac94c-334">..</span></span>

      <span data-ttu-id="ac94c-335">&lt;/Subsystems&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-335">&lt;/Subsystems&gt;</span></span>

    <span data-ttu-id="ac94c-336">..</span><span class="sxs-lookup"><span data-stu-id="ac94c-336">..</span></span>

    <span data-ttu-id="ac94c-337">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-337">&lt;/MachineConfiguration&gt;</span></span>

    <span data-ttu-id="ac94c-338">Im folgenden Abschnitt werden die verschiedenen Subsysteme und Verwendungsbeispiele angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ac94c-338">The following section displays the various subsystems and usage samples.</span></span>

    <span data-ttu-id="ac94c-339">**Erweiterungen**:</span><span class="sxs-lookup"><span data-stu-id="ac94c-339">**Extensions**:</span></span>

    <span data-ttu-id="ac94c-340">Einige Subsysteme (Erweiterungs Subsysteme) Steuern Erweiterungen, die nur für alle Benutzer gelten können.</span><span class="sxs-lookup"><span data-stu-id="ac94c-340">Some subsystems (Extension Subsystems) control Extensions which can only apply to all users.</span></span> <span data-ttu-id="ac94c-341">Das Subsystem ist Anwendungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="ac94c-341">The subsystem is application capabilities.</span></span> <span data-ttu-id="ac94c-342">Da dies nur für alle Benutzer gelten kann, muss das Paket Global veröffentlicht werden, damit diese Art von Erweiterung in das lokale System integriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ac94c-342">Because this can only apply to all users, the package must be published globally in order for this type of extension to be integrated into the local system.</span></span> <span data-ttu-id="ac94c-343">Die gleichen Regeln für Steuerelemente und Einstellungen, die für die Erweiterungen in der Benutzerkonfiguration gelten, gelten auch für die im Abschnitt MachineConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ac94c-343">The same rules for controls and settings that apply to the Extensions in the User Configuration also apply to those in the MachineConfiguration section.</span></span>

    <span data-ttu-id="ac94c-344">**Anwendungsfunktionen**: wird von Standardprogrammen in der Windows-Betriebssystem Schnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac94c-344">**Application Capabilities**: Used by default programs in windows operating system Interface.</span></span> <span data-ttu-id="ac94c-345">Ermöglicht es einer Anwendung, sich selbst so zu registrieren, dass Sie bestimmte Dateierweiterungen öffnen kann, als Anwärter für den Internet Browser Steckplatz des Startmenüs, um bestimmte Windows-MIME-Typen öffnen zu können.</span><span class="sxs-lookup"><span data-stu-id="ac94c-345">Allows an application to register itself as capable of opening certain file extensions, as a contender for the start menu internet browser slot, as capable of opening certain windows MIME types.</span></span><span data-ttu-id="ac94c-346">Diese Erweiterung macht auch die virtuelle Anwendung in der Benutzeroberfläche für Standard Programme festlegen sichtbar:</span><span class="sxs-lookup"><span data-stu-id="ac94c-346"> This extension also makes the virtual application visible in the Set Default Programs UI.:</span></span>

    <span data-ttu-id="ac94c-347">&lt;ApplicationCapabilities Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-347">&lt;ApplicationCapabilities Enabled="true"&gt;</span></span>

      <span data-ttu-id="ac94c-348">&lt;Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-348">&lt;Extensions&gt;</span></span>

       <span data-ttu-id="ac94c-349">&lt;Erweiterungskategorie = "AppV. ApplicationCapabilities"&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-349">&lt;Extension Category="AppV.ApplicationCapabilities"&gt;</span></span>

        &lt;ApplicationCapabilities&gt;

         &lt;ApplicationId&gt;\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe&lt;/ApplicationId&gt;

         &lt;Reference&gt;

          &lt;Name&gt;LitView Browser&lt;/Name&gt;

          &lt;Path&gt;SOFTWARE\\LitView\\Browser\\Capabilities&lt;/Path&gt;

         &lt;/Reference&gt;

       <span data-ttu-id="ac94c-350">&lt;Capabilitygroup&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-350">&lt;CapabilityGroup&gt;</span></span>

        &lt;Capabilities&gt;

         &lt;Name&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12345&lt;/Name&gt;

         &lt;Description&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12346&lt;/Description&gt;

         &lt;Hidden&gt;0&lt;/Hidden&gt;

         &lt;EMailSoftwareClient&gt;Lit View E-Mail Client&lt;/EMailSoftwareClient&gt;

         &lt;FileAssociationList&gt;

          &lt;FileAssociation Extension=".htm" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".html" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".shtml" ProgID="LitViewHTML" /&gt;

         &lt;/FileAssociationList&gt;

         &lt;MIMEAssociationList&gt;

          &lt;MIMEAssociation Type="audio/mp3" ProgID="LitViewHTML" /&gt;

          &lt;MIMEAssociation Type="audio/mpeg" ProgID="LitViewHTML" /&gt;

         &lt;/MIMEAssociationList&gt;

        &lt;URLAssociationList&gt;

          &lt;URLAssociation Scheme="http" ProgID="LitViewHTML.URL.http" /&gt;

         &lt;/URLAssociationList&gt;

         &lt;/Capabilities&gt;

      <span data-ttu-id="ac94c-351">&lt;/CapabilityGroup&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-351">&lt;/CapabilityGroup&gt;</span></span>

       <span data-ttu-id="ac94c-352">&lt;/ApplicationCapabilities&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-352">&lt;/ApplicationCapabilities&gt;</span></span>

      <span data-ttu-id="ac94c-353">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-353">&lt;/Extension&gt;</span></span>

    <span data-ttu-id="ac94c-354">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-354">&lt;/Extensions&gt;</span></span>

    <span data-ttu-id="ac94c-355">&lt;/ApplicationCapabilities&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-355">&lt;/ApplicationCapabilities&gt;</span></span>

    <span data-ttu-id="ac94c-356">**Weitere Einstellungen**:</span><span class="sxs-lookup"><span data-stu-id="ac94c-356">**Other Settings**:</span></span>

    <span data-ttu-id="ac94c-357">Neben Erweiterungen können auch andere Subsysteme bearbeitet werden:</span><span class="sxs-lookup"><span data-stu-id="ac94c-357">In addition to Extensions, other subsystems can be edited:</span></span>

    <span data-ttu-id="ac94c-358">**Machine Wide Virtual Registry**: wird verwendet, wenn Sie einen Registrierungsschlüssel in der virtuellen Registrierung in HKEY \ _Local \ _Machine</span><span class="sxs-lookup"><span data-stu-id="ac94c-358">**Machine Wide Virtual Registry**: Used when you want to set a registry key in the virtual registry within HKEY\_Local\_Machine</span></span>

    <span data-ttu-id="ac94c-359">&lt;Registrierung&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-359">&lt;Registry&gt;</span></span>

    <span data-ttu-id="ac94c-360">&lt;Enthalten&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-360">&lt;Include&gt;</span></span>

      <span data-ttu-id="ac94c-361">&lt;Key Path = "\\REGISTRY\\Machine\\Software\\ABC"&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-361">&lt;Key Path="\\REGISTRY\\Machine\\Software\\ABC"&gt;</span></span>

        &lt;Value Type="REG\_SZ" Name="Bar" Data="Baz" /&gt;

       <span data-ttu-id="ac94c-362">&lt;/Key&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-362">&lt;/Key&gt;</span></span>

      <span data-ttu-id="ac94c-363">&lt;Key Path = "\\REGISTRY\\Machine\\Software\\EmptyKey"/&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-363">&lt;Key Path="\\REGISTRY\\Machine\\Software\\EmptyKey" /&gt;</span></span>

     <span data-ttu-id="ac94c-364">&lt;/Include&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-364">&lt;/Include&gt;</span></span>

    <span data-ttu-id="ac94c-365">&lt;Löschen&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-365">&lt;Delete&gt;</span></span>

    <span data-ttu-id="ac94c-366">&lt;/Registry&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-366">&lt;/Registry&gt;</span></span>

    **<span data-ttu-id="ac94c-367">Computerweite virtuelle Kernel Objekte</span><span class="sxs-lookup"><span data-stu-id="ac94c-367">Machine Wide Virtual Kernel Objects</span></span>**

    <span data-ttu-id="ac94c-368">&lt;Objekte&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-368">&lt;Objects&gt;</span></span>

    <span data-ttu-id="ac94c-369">&lt;NotIsolate&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-369">&lt;NotIsolate&gt;</span></span>

       <span data-ttu-id="ac94c-370">&lt;Objekt Name = "testObject"/&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-370">&lt;Object Name="testObject" /&gt;</span></span>

     <span data-ttu-id="ac94c-371">&lt;/NotIsolate&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-371">&lt;/NotIsolate&gt;</span></span>

    <span data-ttu-id="ac94c-372">&lt;/Objects&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-372">&lt;/Objects&gt;</span></span>

2.  <span data-ttu-id="ac94c-373">**ProductSourceURLOptOut**: gibt an, ob die URL für das Paket global über PackageSourceRoot (zur Unterstützung von Zweigstellenszenarien) geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ac94c-373">**ProductSourceURLOptOut**: Indicates whether the URL for the package can be modified globally through PackageSourceRoot (to support branch office scenarios).</span></span> <span data-ttu-id="ac94c-374">Standard ist falsch, und die Einstellungsänderung wird beim nächsten Start wirksam.</span><span class="sxs-lookup"><span data-stu-id="ac94c-374">Default is false and the setting change takes effect on the next launch.</span></span>  

    <span data-ttu-id="ac94c-375">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-375">&lt;MachineConfiguration&gt;</span></span>

      <span data-ttu-id="ac94c-376">..</span><span class="sxs-lookup"><span data-stu-id="ac94c-376">..</span></span> 

      <span data-ttu-id="ac94c-377">&lt;ProductSourceURLOptOut Enabled = "true"/&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-377">&lt;ProductSourceURLOptOut Enabled="true" /&gt;</span></span>

      <span data-ttu-id="ac94c-378">..</span><span class="sxs-lookup"><span data-stu-id="ac94c-378">..</span></span>

    <span data-ttu-id="ac94c-379">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-379">&lt;/MachineConfiguration&gt;</span></span>

3.  <span data-ttu-id="ac94c-380">**MachineScripts** – Paket kann so konfiguriert werden, dass Skripts zum Zeitpunkt der Bereitstellung, Veröffentlichung oder Entfernung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ac94c-380">**MachineScripts** – Package can be configured to execute scripts at time of deployment, publishing or removal.</span></span> <span data-ttu-id="ac94c-381">Verweisen Sie auf eine Beispiel Bereitstellungs Konfigurationsdatei, die vom Sequencer generiert wird, um ein Beispielskript anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ac94c-381">Please reference a sample deployment configuration file that is generated by the sequencer to see a sample script.</span></span> <span data-ttu-id="ac94c-382">Im Abschnitt "Skripte" unten finden Sie weitere Informationen zu den verschiedenen Triggern, die verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ac94c-382">The Scripts section below provides more information on the various triggers that can be used</span></span>

4.  <span data-ttu-id="ac94c-383">**TerminateChildProcess**: – Es kann eine ausführbare Datei der Anwendung angegeben werden, deren untergeordnete Prozesse beendet werden, wenn der Prozess der Anwendungs-exe beendet wird.</span><span class="sxs-lookup"><span data-stu-id="ac94c-383">**TerminateChildProcess**:- An application executable can be specified, whose child processes will be terminated when the application exe process is terminated.</span></span>

    <span data-ttu-id="ac94c-384">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-384">&lt;MachineConfiguration&gt;</span></span>

      <span data-ttu-id="ac94c-385">..</span><span class="sxs-lookup"><span data-stu-id="ac94c-385">..</span></span>   

      <span data-ttu-id="ac94c-386">&lt;TerminateChildProcesses&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-386">&lt;TerminateChildProcesses&gt;</span></span>

        &lt;Application Path="\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE" /&gt;

        &lt;Application Path="\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe" /&gt;

        &lt;Application Path="\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE" /&gt;

      <span data-ttu-id="ac94c-387">&lt;/TerminateChildProcesses&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-387">&lt;/TerminateChildProcesses&gt;</span></span>

      <span data-ttu-id="ac94c-388">..</span><span class="sxs-lookup"><span data-stu-id="ac94c-388">..</span></span>

    <span data-ttu-id="ac94c-389">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="ac94c-389">&lt;/MachineConfiguration&gt;</span></span>

### <span data-ttu-id="ac94c-390">Skripts</span><span class="sxs-lookup"><span data-stu-id="ac94c-390">Scripts</span></span>

<span data-ttu-id="ac94c-391">In der folgenden Tabelle werden die verschiedenen Skriptereignisse und der Kontext beschrieben, unter dem Sie ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="ac94c-391">The following table describes the various script events and the context under which they can be run.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ac94c-392">Skript Ausführungszeit</span><span class="sxs-lookup"><span data-stu-id="ac94c-392">Script Execution Time</span></span></th>
<th align="left"><span data-ttu-id="ac94c-393">Kann in der Bereitstellungskonfiguration angegeben werden</span><span class="sxs-lookup"><span data-stu-id="ac94c-393">Can be specified in Deployment Configuration</span></span></th>
<th align="left"><span data-ttu-id="ac94c-394">Kann in der Benutzerkonfiguration angegeben werden</span><span class="sxs-lookup"><span data-stu-id="ac94c-394">Can be specified in User Configuration</span></span></th>
<th align="left"><span data-ttu-id="ac94c-395">Kann in der virtuellen Umgebung des Pakets ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="ac94c-395">Can run in the Virtual Environment of the package</span></span></th>
<th align="left"><span data-ttu-id="ac94c-396">Kann im Kontext einer bestimmten Anwendung ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="ac94c-396">Can be run in the context of a specific application</span></span></th>
<th align="left"><span data-ttu-id="ac94c-397">Wird im System/Benutzerkontext ausgeführt: (Bereitstellungskonfiguration, Benutzerkonfiguration)</span><span class="sxs-lookup"><span data-stu-id="ac94c-397">Runs in system/user context: (Deployment Configuration, User Configuration)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac94c-398">AddPackage</span><span class="sxs-lookup"><span data-stu-id="ac94c-398">AddPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac94c-399">X</span><span class="sxs-lookup"><span data-stu-id="ac94c-399">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ac94c-400">(System, N/A)</span><span class="sxs-lookup"><span data-stu-id="ac94c-400">(SYSTEM, N/A)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac94c-401">PublishPackage</span><span class="sxs-lookup"><span data-stu-id="ac94c-401">PublishPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac94c-402">X</span><span class="sxs-lookup"><span data-stu-id="ac94c-402">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac94c-403">X</span><span class="sxs-lookup"><span data-stu-id="ac94c-403">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ac94c-404">(System, Benutzer)</span><span class="sxs-lookup"><span data-stu-id="ac94c-404">(SYSTEM, User)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac94c-405">UnpublishPackage</span><span class="sxs-lookup"><span data-stu-id="ac94c-405">UnpublishPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac94c-406">X</span><span class="sxs-lookup"><span data-stu-id="ac94c-406">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac94c-407">X</span><span class="sxs-lookup"><span data-stu-id="ac94c-407">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ac94c-408">(System, Benutzer)</span><span class="sxs-lookup"><span data-stu-id="ac94c-408">(SYSTEM, User)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac94c-409">RemovePackage</span><span class="sxs-lookup"><span data-stu-id="ac94c-409">RemovePackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac94c-410">X</span><span class="sxs-lookup"><span data-stu-id="ac94c-410">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ac94c-411">(System, N/A)</span><span class="sxs-lookup"><span data-stu-id="ac94c-411">(SYSTEM, N/A)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac94c-412">StartProcess</span><span class="sxs-lookup"><span data-stu-id="ac94c-412">StartProcess</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac94c-413">X</span><span class="sxs-lookup"><span data-stu-id="ac94c-413">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac94c-414">X</span><span class="sxs-lookup"><span data-stu-id="ac94c-414">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac94c-415">X</span><span class="sxs-lookup"><span data-stu-id="ac94c-415">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac94c-416">X</span><span class="sxs-lookup"><span data-stu-id="ac94c-416">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac94c-417">(Benutzer, Benutzer)</span><span class="sxs-lookup"><span data-stu-id="ac94c-417">(User, User)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac94c-418">ExitProcess</span><span class="sxs-lookup"><span data-stu-id="ac94c-418">ExitProcess</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac94c-419">X</span><span class="sxs-lookup"><span data-stu-id="ac94c-419">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac94c-420">X</span><span class="sxs-lookup"><span data-stu-id="ac94c-420">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ac94c-421">X</span><span class="sxs-lookup"><span data-stu-id="ac94c-421">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac94c-422">(Benutzer, Benutzer)</span><span class="sxs-lookup"><span data-stu-id="ac94c-422">(User, User)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac94c-423">StartVirtualEnvironment</span><span class="sxs-lookup"><span data-stu-id="ac94c-423">StartVirtualEnvironment</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac94c-424">X</span><span class="sxs-lookup"><span data-stu-id="ac94c-424">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac94c-425">X</span><span class="sxs-lookup"><span data-stu-id="ac94c-425">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac94c-426">X</span><span class="sxs-lookup"><span data-stu-id="ac94c-426">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ac94c-427">(Benutzer, Benutzer)</span><span class="sxs-lookup"><span data-stu-id="ac94c-427">(User, User)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac94c-428">TerminateVirtualEnvironment</span><span class="sxs-lookup"><span data-stu-id="ac94c-428">TerminateVirtualEnvironment</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac94c-429">X</span><span class="sxs-lookup"><span data-stu-id="ac94c-429">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac94c-430">X</span><span class="sxs-lookup"><span data-stu-id="ac94c-430">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ac94c-431">(Benutzer, Benutzer)</span><span class="sxs-lookup"><span data-stu-id="ac94c-431">(User, User)</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="ac94c-432">Erstellen einer dynamischen Konfigurationsdatei mit einer App-V 5,0-Manifestdatei</span><span class="sxs-lookup"><span data-stu-id="ac94c-432">Create a Dynamic Configuration file using an App-V 5.0 Manifest file</span></span>

<span data-ttu-id="ac94c-433">Sie können die dynamische Konfigurationsdatei mit einer von drei Methoden erstellen: entweder manuell, mithilfe der App-V 5,0-Verwaltungskonsole oder durch Sequenzierung eines Pakets, das mit zwei Beispieldateien generiert wird.</span><span class="sxs-lookup"><span data-stu-id="ac94c-433">You can create the Dynamic Configuration file using one of three methods: either manually, using the App-V 5.0 Management Console or sequencing a package, which will be generated with 2 sample files.</span></span>

<span data-ttu-id="ac94c-434">Weitere Informationen zum Erstellen der Datei mithilfe der APP-v 5,0-Verwaltungskonsole finden Sie unter [Erstellen einer benutzerdefinierten Konfigurationsdatei mithilfe der APP-v 5,0-Verwaltungskonsole](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md).</span><span class="sxs-lookup"><span data-stu-id="ac94c-434">For more information about how to create the file using the App-V 5.0 Management Console see, [How to Create a Custom Configuration File by Using the App-V 5.0 Management Console](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md).</span></span>

<span data-ttu-id="ac94c-435">Wenn Sie die Datei manuell erstellen möchten, können die obigen Informationen in den vorherigen Abschnitten in einer einzelnen Datei kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="ac94c-435">To create the file manually, the information above in previous sections can be combined into a single file.</span></span> <span data-ttu-id="ac94c-436">Wir empfehlen die Verwendung von Dateien, die vom Sequencer generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="ac94c-436">We recommend you use files generated by the sequencer.</span></span>






## <span data-ttu-id="ac94c-437">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ac94c-437">Related topics</span></span>


[<span data-ttu-id="ac94c-438">Sie wenden Sie die Bereitstellungskonfigurationsdatei mithilfe von PowerShell an</span><span class="sxs-lookup"><span data-stu-id="ac94c-438">How to Apply the Deployment Configuration File by Using PowerShell</span></span>](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)

[<span data-ttu-id="ac94c-439">So wenden Sie die Benutzerkonfigurationsdatei mithilfe von PowerShell an</span><span class="sxs-lookup"><span data-stu-id="ac94c-439">How to Apply the User Configuration File by Using PowerShell</span></span>](how-to-apply-the-user-configuration-file-by-using-powershell.md)

[<span data-ttu-id="ac94c-440">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ac94c-440">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





