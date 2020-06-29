---
title: Schema Referenz für Anwendungsvorlagen für UE-V 2. x
description: Schema Referenz für Anwendungsvorlagen für UE-V 2. x
author: dansimp
ms.assetid: be8735a5-6a3e-4b1f-ba14-2a3bc3e5a8b6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 03ff6eabae68f07c23d5977f901e6a90e292c6ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812337"
---
# <span data-ttu-id="605ce-103">Schema Referenz für Anwendungsvorlagen für UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="605ce-103">Application Template Schema Reference for UE-V 2.x</span></span>


<span data-ttu-id="605ce-104">Microsoft User Experience Virtualization (UE-v) 2,0, 2,1 und 2,1 SP1 verwenden Sie XML-Einstellungen, um die Einstellungen für die Desktopanwendung und die Windows-Einstellungen zu definieren, die von UE-v erfasst und angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="605ce-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 use XML settings location templates to define the desktop application settings and Windows settings that are captured and applied by UE-V.</span></span> <span data-ttu-id="605ce-105">UE-V enthält eine Reihe von Standardeinstellungen für Standort Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="605ce-105">UE-V includes a set of default settings location templates.</span></span> <span data-ttu-id="605ce-106">Sie können auch mit dem UE-V-Generator benutzerdefinierte Standort Vorlagen für Einstellungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="605ce-106">You can also create custom settings location templates with the UE-V Generator.</span></span>

<span data-ttu-id="605ce-107">Ein fortgeschrittener Benutzer kann die XML-Datei für eine Einstellungs Speicherort Vorlage anpassen.</span><span class="sxs-lookup"><span data-stu-id="605ce-107">An advanced user can customize the XML file for a settings location template.</span></span> <span data-ttu-id="605ce-108">In diesem Thema wird die XML-Struktur der Einstellungen für die Standort Vorlagen UE-V 2,1 (SP1) und 2,0 erläutert, und es werden Anleitungen zum Bearbeiten dieser Dateien bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="605ce-108">This topic details the XML structure of the UE-V 2.1 (SP1) and 2.0 settings location templates and provides guidance for editing these files.</span></span>

## <span data-ttu-id="605ce-109">UE-V 2,1 und 2,1 SP1-Schema Referenz für Anwendungsvorlagen</span><span class="sxs-lookup"><span data-stu-id="605ce-109">UE-V 2.1 and 2.1 SP1 Application Template Schema Reference</span></span>


<span data-ttu-id="605ce-110">In diesem Abschnitt wird die XML-Struktur der Standort Vorlage UE-V 2,1 und 2,1 SP1 erläutert, und es werden Anleitungen zum Bearbeiten dieser Datei bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="605ce-110">This section details the XML structure of the UE-V 2.1 and 2.1 SP1 settings location template and provides guidance for editing this file.</span></span>

### <span data-ttu-id="605ce-111">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="605ce-111">In This Section</span></span>

-   [<span data-ttu-id="605ce-112">XML-Deklaration und Codierungsattribut</span><span class="sxs-lookup"><span data-stu-id="605ce-112">XML Declaration and Encoding Attribute</span></span>](#xml21)

-   [<span data-ttu-id="605ce-113">Namespace und Stamm Element</span><span class="sxs-lookup"><span data-stu-id="605ce-113">Namespace and Root Element</span></span>](#namespace21)

-   [<span data-ttu-id="605ce-114">Datentypen</span><span class="sxs-lookup"><span data-stu-id="605ce-114">Data types</span></span>](#data21)

-   [<span data-ttu-id="605ce-115">Name-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-115">Name Element</span></span>](#name21)

-   [<span data-ttu-id="605ce-116">ID-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-116">ID Element</span></span>](#id21)

-   [<span data-ttu-id="605ce-117">Version-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-117">Version Element</span></span>](#version21)

-   [<span data-ttu-id="605ce-118">Author-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-118">Author Element</span></span>](#author21)

-   [<span data-ttu-id="605ce-119">Prozesse und Prozess Element</span><span class="sxs-lookup"><span data-stu-id="605ce-119">Processes and Process Element</span></span>](#processes21)

-   [<span data-ttu-id="605ce-120">Application-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-120">Application Element</span></span>](#application21)

-   [<span data-ttu-id="605ce-121">Common-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-121">Common Element</span></span>](#common21)

-   [<span data-ttu-id="605ce-122">SettingsLocationTemplate-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-122">SettingsLocationTemplate Element</span></span>](#settingslocationtemplate21)

-   [<span data-ttu-id="605ce-123">Anhang: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="605ce-123">Appendix: SettingsLocationTemplate.xsd</span></span>](#appendix21)

### <a href="" id="xml21"></a><span data-ttu-id="605ce-124">XML-Deklaration und Codierungsattribut</span><span class="sxs-lookup"><span data-stu-id="605ce-124">XML Declaration and Encoding Attribute</span></span>

**<span data-ttu-id="605ce-125">Obligatorisch: wahr</span><span class="sxs-lookup"><span data-stu-id="605ce-125">Mandatory: True</span></span>**

**<span data-ttu-id="605ce-126">Typ: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-126">Type: String</span></span>**

<span data-ttu-id="605ce-127">Die XML-Deklaration muss das XML-Version 1,0-Attribut ( &lt; ? XML-Version = "1.0" &gt; ) angeben.</span><span class="sxs-lookup"><span data-stu-id="605ce-127">The XML declaration must specify the XML version 1.0 attribute (&lt;?xml version="1.0"&gt;).</span></span> <span data-ttu-id="605ce-128">Vom UE-V-Generator erstellte Einstellungen für Standort Vorlagen werden in UTF-8-Codierung gespeichert, obwohl die Codierung nicht explizit angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="605ce-128">Settings location templates created by the UE-V Generator are saved in UTF-8 encoding, although the encoding is not explicitly specified.</span></span> <span data-ttu-id="605ce-129">Wir empfehlen, dass Sie das Attribut Encoding = "UTF-8" in dieses Element als bewährte Methode einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="605ce-129">We recommend that you include the encoding="UTF-8" attribute in this element as a best practice.</span></span> <span data-ttu-id="605ce-130">Alle im Lieferumfang des Produkts enthaltenen Vorlagen geben diesen Tag ebenfalls an (Informationen finden Sie in den Dokumenten in%programfiles%\\Microsoft Benutzeroberflächen-Virtualization\\Templates als Referenz).</span><span class="sxs-lookup"><span data-stu-id="605ce-130">All templates included with the product specify this tag as well (see the documents in %ProgramFiles%\\Microsoft User Experience Virtualization\\Templates for reference).</span></span> <span data-ttu-id="605ce-131">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="605ce-131">For example:</span></span>

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace21"></a><span data-ttu-id="605ce-132">Namespace und Stamm Element</span><span class="sxs-lookup"><span data-stu-id="605ce-132">Namespace and Root Element</span></span>

**<span data-ttu-id="605ce-133">Obligatorisch: wahr</span><span class="sxs-lookup"><span data-stu-id="605ce-133">Mandatory: True</span></span>**

**<span data-ttu-id="605ce-134">Typ: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-134">Type: String</span></span>**

<span data-ttu-id="605ce-135">UE-V verwendet den https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate Namespace für alle Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="605ce-135">UE-V uses the https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate namespace for all applications.</span></span> <span data-ttu-id="605ce-136">SettingsLocationTemplate ist das Stammelement und enthält alle anderen Elemente.</span><span class="sxs-lookup"><span data-stu-id="605ce-136">SettingsLocationTemplate is the root element and contains all other elements.</span></span> <span data-ttu-id="605ce-137">Verweisen Sie SettingsLocationTemplate in allen Vorlagen mit diesem Tag:</span><span class="sxs-lookup"><span data-stu-id="605ce-137">Reference SettingsLocationTemplate in all templates using this tag:</span></span>

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data21"></a><span data-ttu-id="605ce-138">Datentypen</span><span class="sxs-lookup"><span data-stu-id="605ce-138">Data types</span></span>

<span data-ttu-id="605ce-139">Hierbei handelt es sich um die Datentypen für das Anwendungsvorlagen Schema UE-V.</span><span class="sxs-lookup"><span data-stu-id="605ce-139">These are the data types for the UE-V application template schema.</span></span>

<a href="" id="guid"></a><span data-ttu-id="605ce-140">**GUID** GUID beschreibt einen standardmäßigen Standardausdruck für global eindeutigen Bezeichner in der Form "\ \ {\ [a-FA-F0-9 \] {8} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {12} \ \}".</span><span class="sxs-lookup"><span data-stu-id="605ce-140">**GUID** GUID describes a standard globally unique identifier regular expression in the form "\\{\[a-fA-F0-9\]{8}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{12}\\}".</span></span> <span data-ttu-id="605ce-141">Diese wird im Filesetting\\Root\\KnownFolder-Element verwendet, um die Formatierung bekannter Ordner zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="605ce-141">This is used in the Filesetting\\Root\\KnownFolder element to verify the formatting of well-known folders.</span></span>

<a href="" id="filenamestring"></a><span data-ttu-id="605ce-142">**Filenamed** Filenamed bezieht sich auf den Dateinamen eines zu überwachenden Prozesses.</span><span class="sxs-lookup"><span data-stu-id="605ce-142">**FilenameString** FilenameString refers to the file name of a process to be monitored.</span></span> <span data-ttu-id="605ce-143">Die Werte sind durch das Regex-Element \ [^ \ \ \ \ \ \? &lt; &gt; /: \] +, (das heißt, Sie dürfen keine umgekehrten Schrägstriche, Sternchen oder Fragezeichen-Wildcard-Zeichen, das Pipe-Zeichen, das größer-als-oder kleiner-als-Zeichen, Schrägstrich oder Doppelpunktzeichen) enthalten.</span><span class="sxs-lookup"><span data-stu-id="605ce-143">Its values are restricted by the regex \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, (that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon characters).</span></span>

<a href="" id="idstring"></a><span data-ttu-id="605ce-144">**IDString** IDString bezieht sich auf den ID-Wert von Application-Elementen, SettingsLocationTemplate und Common Elements (verwendet, um Anwendungssuiten zu beschreiben, die gemeinsame Einstellungen aufweisen).</span><span class="sxs-lookup"><span data-stu-id="605ce-144">**IDString** IDString refers to the ID value of Application elements, SettingsLocationTemplate, and Common elements (used to describe application suites that share common settings).</span></span> <span data-ttu-id="605ce-145">Sie ist durch denselben Regex-Ausdruck wie filenamed eingeschränkt (\ [^ \ \ \ \ \ \? \ \ \ \* \ \ | &lt; &gt; /:\]+).</span><span class="sxs-lookup"><span data-stu-id="605ce-145">It is restricted by the same regex as FilenameString (\[^\\\\\\?\\\*\\|&lt;&gt;/:\]+).</span></span>

<a href="" id="templateversion"></a><span data-ttu-id="605ce-146">**TemplateVersion** TemplateVersion ist ein ganzzahliger Wert, der zur Beschreibung der Überarbeitung der Vorlage für die Einstellungsposition verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="605ce-146">**TemplateVersion** TemplateVersion is an integer value used to describe the revision of the settings location template.</span></span> <span data-ttu-id="605ce-147">Der Wert kann zwischen 0 und 2147483647 liegen.</span><span class="sxs-lookup"><span data-stu-id="605ce-147">Its value may range from 0 to 2147483647.</span></span>

<a href="" id="empty"></a><span data-ttu-id="605ce-148">**Leer** Empty bezieht sich auf einen NULL-Wert.</span><span class="sxs-lookup"><span data-stu-id="605ce-148">**Empty** Empty refers to a null value.</span></span> <span data-ttu-id="605ce-149">Dieser wird in Process\\ShellProcess verwendet, um anzugeben, dass kein zu überwachenden Prozess vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="605ce-149">This is used in Process\\ShellProcess to indicate that there is no process to monitor.</span></span> <span data-ttu-id="605ce-150">Dieser Wert sollte in keiner Anwendungsvorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="605ce-150">This value should not be used in any application templates.</span></span>

<a href="" id="author"></a><span data-ttu-id="605ce-151">**Autor** Der Datentyp "Autor" ist ein komplexer Typ, der den Autor einer Vorlage identifiziert.</span><span class="sxs-lookup"><span data-stu-id="605ce-151">**Author** The Author data type is a complex type that identifies the author of a template.</span></span> <span data-ttu-id="605ce-152">Sie enthält zwei untergeordnete Elemente: **Name** und **e-Mail**.</span><span class="sxs-lookup"><span data-stu-id="605ce-152">It contains two child elements: **Name** and **Email**.</span></span> <span data-ttu-id="605ce-153">Im Datentyp "Author" ist das Name-Element obligatorisch, während das e-Mail-Element optional ist.</span><span class="sxs-lookup"><span data-stu-id="605ce-153">Within the Author data type, the Name element is mandatory while the Email element is optional.</span></span> <span data-ttu-id="605ce-154">Dieser Typ wird im SettingsLocationTemplate-Element ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="605ce-154">This type is described in more detail under the SettingsLocationTemplate element.</span></span>

<a href="" id="range"></a><span data-ttu-id="605ce-155">**Bereich** Bereich definiert eine ganzzahlige Klasse, die aus zwei untergeordneten Elementen besteht: **Mindest** -und **höchst**Wert.</span><span class="sxs-lookup"><span data-stu-id="605ce-155">**Range** Range defines an integer class consisting of two child elements: **Minimum** and **Maximum**.</span></span> <span data-ttu-id="605ce-156">Dieser Datentyp wird im Datentyp ProcessVersion implementiert.</span><span class="sxs-lookup"><span data-stu-id="605ce-156">This data type is implemented in the ProcessVersion data type.</span></span> <span data-ttu-id="605ce-157">Wenn angegeben, müssen sowohl Mindest-als auch Maximalwerte enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="605ce-157">If specified, both Minimum and Maximum values must be included.</span></span>

<a href="" id="processversion"></a><span data-ttu-id="605ce-158">**ProcessVersion** ProcessVersion definiert einen Typ mit vier untergeordneten Elementen: **Major**, **Minor**, **Build**und **Patch**.</span><span class="sxs-lookup"><span data-stu-id="605ce-158">**ProcessVersion** ProcessVersion defines a type with four child elements: **Major**, **Minor**, **Build**, and **Patch**.</span></span> <span data-ttu-id="605ce-159">Dieser Datentyp wird vom Process-Element zum Auffüllen seiner ProductVersion-und fileversion-Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="605ce-159">This data type is used by the Process element to populate its ProductVersion and FileVersion values.</span></span> <span data-ttu-id="605ce-160">Bei den Daten für diesen Typ handelt es sich um einen Bereichswert.</span><span class="sxs-lookup"><span data-stu-id="605ce-160">The data for this type is a Range value.</span></span> <span data-ttu-id="605ce-161">Das wichtigste untergeordnete Element ist obligatorisch, und die anderen sind optional.</span><span class="sxs-lookup"><span data-stu-id="605ce-161">The Major child element is mandatory and the others are optional.</span></span>

<a href="" id="architecture"></a><span data-ttu-id="605ce-162">**Architektur** Architektur listet zwei mögliche Werte auf: **Win32** und **Win64**.</span><span class="sxs-lookup"><span data-stu-id="605ce-162">**Architecture** Architecture enumerates two possible values: **Win32** and **Win64**.</span></span> <span data-ttu-id="605ce-163">Diese Werte werden verwendet, um die Prozessarchitektur festzulegen.</span><span class="sxs-lookup"><span data-stu-id="605ce-163">These values are used to specify process architecture.</span></span>

<a href="" id="process"></a><span data-ttu-id="605ce-164">**Prozess** Der Prozessdatentyp ist ein Container, der zur Beschreibung der von UE-V zu überwachenden Prozesse dient.</span><span class="sxs-lookup"><span data-stu-id="605ce-164">**Process** The Process data type is a container used to describe processes to be monitored by UE-V.</span></span> <span data-ttu-id="605ce-165">Sie enthält sechs untergeordnete Elemente: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**und **fileversion**.</span><span class="sxs-lookup"><span data-stu-id="605ce-165">It contains six child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="605ce-166">In dieser Tabelle werden die jeweiligen Datentypen der einzelnen Elemente beschrieben:</span><span class="sxs-lookup"><span data-stu-id="605ce-166">This table details each element’s respective data type:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="605ce-167">Element</span><span class="sxs-lookup"><span data-stu-id="605ce-167">Element</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="605ce-168">Datentyp</span><span class="sxs-lookup"><span data-stu-id="605ce-168">Data Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="605ce-169">Mandatory</span><span class="sxs-lookup"><span data-stu-id="605ce-169">Mandatory</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-170">Dateiname</span><span class="sxs-lookup"><span data-stu-id="605ce-170">Filename</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-171">Filenamed</span><span class="sxs-lookup"><span data-stu-id="605ce-171">FilenameString</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-172">Wahr</span><span class="sxs-lookup"><span data-stu-id="605ce-172">True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-173">Architektur</span><span class="sxs-lookup"><span data-stu-id="605ce-173">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-174">Architektur</span><span class="sxs-lookup"><span data-stu-id="605ce-174">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-175">False</span><span class="sxs-lookup"><span data-stu-id="605ce-175">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-176">ProductName</span><span class="sxs-lookup"><span data-stu-id="605ce-176">ProductName</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-177">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-177">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-178">False</span><span class="sxs-lookup"><span data-stu-id="605ce-178">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-179">FileDescription</span><span class="sxs-lookup"><span data-stu-id="605ce-179">FileDescription</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-180">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-180">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-181">False</span><span class="sxs-lookup"><span data-stu-id="605ce-181">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-182">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="605ce-182">ProductVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-183">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="605ce-183">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-184">False</span><span class="sxs-lookup"><span data-stu-id="605ce-184">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-185">File Version</span><span class="sxs-lookup"><span data-stu-id="605ce-185">FileVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-186">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="605ce-186">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-187">False</span><span class="sxs-lookup"><span data-stu-id="605ce-187">False</span></span></p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a><span data-ttu-id="605ce-188">**Prozesse** Der Datentyp "Prozesse" stellt einen Container für eine Sammlung von einem oder mehreren Process-Elementen dar.</span><span class="sxs-lookup"><span data-stu-id="605ce-188">**Processes** The Processes data type represents a container for a collection of one or more Process elements.</span></span> <span data-ttu-id="605ce-189">Im Sequence-Typ Prozesse werden zwei untergeordnete Elemente unterstützt: **Process** und **ShellProcess**.</span><span class="sxs-lookup"><span data-stu-id="605ce-189">Two child elements are supported in the Processes sequence type: **Process** and **ShellProcess**.</span></span> <span data-ttu-id="605ce-190">Process ist ein Element vom Typ Process, und ShellProcess ist vom Datentyp leer.</span><span class="sxs-lookup"><span data-stu-id="605ce-190">Process is an element of type Process and ShellProcess is of data type Empty.</span></span> <span data-ttu-id="605ce-191">Es muss mindestens ein Element in der Sequenz identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="605ce-191">At least one item must be identified in the sequence.</span></span>

<a href="" id="path"></a><span data-ttu-id="605ce-192">**Path** Path wird von RegistrySetting und filesetting verwendet, um auf Registrierungs-und Dateipfade zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="605ce-192">**Path** Path is consumed by RegistrySetting and FileSetting to refer to registry and file paths.</span></span> <span data-ttu-id="605ce-193">Dieses Element unterstützt zwei optionale Attribute: **rekursiv** und **DeleteIfNotFound**.</span><span class="sxs-lookup"><span data-stu-id="605ce-193">This element supports two optional attributes: **Recursive** and **DeleteIfNotFound**.</span></span> <span data-ttu-id="605ce-194">Beide Werte sind auf Default = "false" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="605ce-194">Both values are set to default=”False”.</span></span>

<span data-ttu-id="605ce-195">Rekursiv gibt an, dass der Pfad und alle Unterordner für Datei Einstellungen enthalten sind oder dass alle untergeordneten Registrierungsschlüssel für Registrierungseinstellungen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="605ce-195">Recursive indicates that the path and all subfolders are included for file settings or that all child registry keys are included for registry settings.</span></span> <span data-ttu-id="605ce-196">In beiden Fällen sind alle Elemente auf der aktuellen Ebene in den erfassten Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="605ce-196">In both cases, all items at the current level are included in the data captured.</span></span> <span data-ttu-id="605ce-197">Bei einem filesettings-Objekt sind alle Dateien innerhalb des angegebenen Ordners in den von UE-V erfassten Daten enthalten, aber Ordner sind nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="605ce-197">For a FileSettings object, all files within the specified folder are included in the data captured by UE-V but folders are not included.</span></span> <span data-ttu-id="605ce-198">Bei Registrierungspfaden werden alle Werte im aktuellen Pfad erfasst, aber die untergeordneten Registrierungsschlüssel werden nicht erfasst.</span><span class="sxs-lookup"><span data-stu-id="605ce-198">For registry paths, all values in the current path are captured but child registry keys are not captured.</span></span> <span data-ttu-id="605ce-199">In beiden Fällen sollte darauf geachtet werden, große Datenmengen oder eine große Anzahl von Elementen nicht zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="605ce-199">In both cases, care should be taken to avoid capturing large data sets or large numbers of items.</span></span>

<span data-ttu-id="605ce-200">Das DeleteIfNotFound-Attribut entfernt die Einstellungen aus den Speicherpfad Daten des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="605ce-200">The DeleteIfNotFound attribute removes the setting from the user’s settings storage path data.</span></span> <span data-ttu-id="605ce-201">Dies kann in den Fällen wünschenswert sein, in denen durch das Entfernen dieser Einstellungen aus dem Paket eine große Menge an Speicherplatz auf dem Dateiserver für Settings Storage Path gespart wird.</span><span class="sxs-lookup"><span data-stu-id="605ce-201">This may be desirable in cases where removing these settings from the package will save a large amount of disk space on the settings storage path file server.</span></span>

<a href="" id="filemask"></a><span data-ttu-id="605ce-202">**Filemask** Filemask gibt nur bestimmte Dateitypen für den Ordner an, der durch path definiert ist.</span><span class="sxs-lookup"><span data-stu-id="605ce-202">**FileMask** FileMask specifies only certain file types for the folder that is defined by Path.</span></span> <span data-ttu-id="605ce-203">Path könnte beispielsweise sein, `C:\users\username\files` und die Dateimaske kann `*.txt` nur Textdateien enthalten.</span><span class="sxs-lookup"><span data-stu-id="605ce-203">For example, Path might be `C:\users\username\files` and FileMask could be `*.txt` to include only text files.</span></span>

<a href="" id="registrysetting"></a><span data-ttu-id="605ce-204">**RegistrySetting** RegistrySetting stellt einen Container für Registrierungsschlüssel und-Werte und das zugeordnete gewünschte Verhalten auf Seiten des UE-V-Agents dar.</span><span class="sxs-lookup"><span data-stu-id="605ce-204">**RegistrySetting** RegistrySetting represents a container for registry keys and values and the associated desired behavior on the part of the UE-V Agent.</span></span> <span data-ttu-id="605ce-205">In diesem Typ werden vier untergeordnete Elemente definiert: **path**, **Name**, **Exclude**und eine Sequenz des Werte **Pfads** und- **namens**.</span><span class="sxs-lookup"><span data-stu-id="605ce-205">Four child elements are defined within this type: **Path**, **Name**, **Exclude**, and a sequence of the values **Path** and **Name**.</span></span>

<a href="" id="filesetting"></a><span data-ttu-id="605ce-206">**Filesetting** Filesetting enthält Parameter, die mit Dateien und Dateipfaden verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="605ce-206">**FileSetting** FileSetting contains parameters associated with files and files paths.</span></span> <span data-ttu-id="605ce-207">Es werden vier untergeordnete Elemente definiert: **root**, **path**, **filemask**und **Exclude**.</span><span class="sxs-lookup"><span data-stu-id="605ce-207">Four child elements are defined: **Root**, **Path**, **FileMask**, and **Exclude**.</span></span> <span data-ttu-id="605ce-208">Root ist obligatorisch und die anderen sind optional.</span><span class="sxs-lookup"><span data-stu-id="605ce-208">Root is mandatory and the others are optional.</span></span>

<a href="" id="settings"></a><span data-ttu-id="605ce-209">**Einstellungen** Einstellungen ist ein Container für alle Einstellungen, die für eine bestimmte Vorlage gelten.</span><span class="sxs-lookup"><span data-stu-id="605ce-209">**Settings** Settings is a container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="605ce-210">Sie enthält Instanzen der zuvor beschriebenen Registrierungs-, Datei-, Systemparameter-und benutzerdefinierten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="605ce-210">It contains instances of the Registry, File, SystemParameter, and CustomAction settings described earlier.</span></span> <span data-ttu-id="605ce-211">Darüber hinaus kann Sie auch die folgenden untergeordneten Elemente mit den beschriebenen Verhaltensweisen enthalten:</span><span class="sxs-lookup"><span data-stu-id="605ce-211">In addition, it can also contain the following child elements with behaviors described:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="605ce-212">Element</span><span class="sxs-lookup"><span data-stu-id="605ce-212">Element</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="605ce-213">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="605ce-213">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-214">Asynchrone</span><span class="sxs-lookup"><span data-stu-id="605ce-214">Asynchronous</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-215">Asynchrone Einstellungs Pakete werden angewendet, ohne den Anwendungsstart zu blockieren, damit der Anwendungsstart fortgesetzt wird, während die Einstellungen noch angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="605ce-215">Asynchronous settings packages are applied without blocking the application startup so that the application start proceeds while the settings are still being applied.</span></span> <span data-ttu-id="605ce-216">Dies ist nützlich für Einstellungen, die asynchron angewendet werden können, beispielsweise <code>get/set</code> über eine API, wie SystemParameterSetting.</span><span class="sxs-lookup"><span data-stu-id="605ce-216">This is useful for settings that can be applied asynchronously, such as those <code>get/set</code> through an API, like SystemParameterSetting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-217">PreventOverlappingSynchronization</span><span class="sxs-lookup"><span data-stu-id="605ce-217">PreventOverlappingSynchronization</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-218">Standardmäßig werden in UE-V nur Einstellungen für eine Anwendung gespeichert, wenn die letzte Instanz einer Anwendung, die die Vorlage verwendet, geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="605ce-218">By default, UE-V only saves settings for an application when the last instance of an application using the template is closed.</span></span> <span data-ttu-id="605ce-219">Wenn dieses Element auf "false" festgelegt ist, exportiert UE-V die Einstellungen selbst dann, wenn andere Instanzen einer Anwendung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="605ce-219">When this element is set to ‘false’, UE-V exports the settings even if other instances of an application are running.</span></span> <span data-ttu-id="605ce-220">Geeignete Vorlagen – diejenigen, die einen allgemeinen Element Abschnitt enthalten –, die mit UE-V ausgeliefert werden, verwenden dieses Flag, um freigegebene Einstellungen so zu aktivieren, dass Sie immer beim Schließen der Anwendung exportiert werden, während anwendungsspezifische Einstellungen vor dem Export verhindert werden, bis die letzte Instanz geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="605ce-220">Suited templates – those that include a Common element section– that are shipped with UE-V use this flag to enable shared settings to always export on application close, while preventing application-specific settings from exporting until the last instance is closed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-221">AlwaysApplySettings</span><span class="sxs-lookup"><span data-stu-id="605ce-221">AlwaysApplySettings</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-222">(eingeführt in 2,1)</span><span class="sxs-lookup"><span data-stu-id="605ce-222">(introduced in 2.1)</span></span></p>
<p><span data-ttu-id="605ce-223">Dieser Parameter erzwingt die Anwendung eines importierten Einstellungs Pakets, auch wenn es keine Unterschiede zwischen dem Paket und dem aktuellen Zustand der Anwendung gibt.</span><span class="sxs-lookup"><span data-stu-id="605ce-223">This parameter forces an imported settings package to be applied even if there are no differences between the package and the current state of the application.</span></span> <span data-ttu-id="605ce-224">Dieser Parameter sollte nur in speziellen Fällen verwendet werden, da er den Import von Einstellungen verlangsamen kann.</span><span class="sxs-lookup"><span data-stu-id="605ce-224">This parameter should be used only in special cases since it can slow down settings import.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name21"></a><span data-ttu-id="605ce-225">Name-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-225">Name Element</span></span>

**<span data-ttu-id="605ce-226">Obligatorisch: wahr</span><span class="sxs-lookup"><span data-stu-id="605ce-226">Mandatory: True</span></span>**

**<span data-ttu-id="605ce-227">Typ: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-227">Type: String</span></span>**

<span data-ttu-id="605ce-228">Name gibt einen eindeutigen Namen für die Einstellungs Speicherort Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="605ce-228">Name specifies a unique name for the settings location template.</span></span> <span data-ttu-id="605ce-229">Diese Funktion wird für Anzeigezwecke verwendet, wenn Sie in WMI, PowerShell, Ereignisanzeige und Debug-Protokollen auf die Vorlage verweisen.</span><span class="sxs-lookup"><span data-stu-id="605ce-229">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="605ce-230">Im Allgemeinen sollten Sie nicht auf Versionsinformationen verweisen, da dies vom ProductVersion-Element abweichen kann.</span><span class="sxs-lookup"><span data-stu-id="605ce-230">In general, avoid referencing version information, as this can be objected from the ProductVersion element.</span></span> <span data-ttu-id="605ce-231">Geben Sie beispielsweise `<Name>My Application</Name>` anstelle ein `<Name>My Application 1.1</Name>` .</span><span class="sxs-lookup"><span data-stu-id="605ce-231">For example, specify `<Name>My Application</Name>` rather than `<Name>My Application 1.1</Name>`.</span></span>

<span data-ttu-id="605ce-232">**Hinweis**  UE-V verweist nicht auf externe DTDs, daher ist es nicht möglich, benannte Entitäten in einer Einstellungen-Speicherort Vorlage zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="605ce-232">**Note** UE-V does not reference external DTDs, so it is not possible to use named entities in a settings location template.</span></span> <span data-ttu-id="605ce-233">Verwenden Sie beispielsweise nicht, &reg; um auf das eingetragene Markenzeichen® zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="605ce-233">For example, do not use &reg; to refer to the registered trade mark sign ®.</span></span> <span data-ttu-id="605ce-234">Verwenden Sie stattdessen kanonische nummerierte Bezüge, um diese Typen von Sonderzeichen einzubeziehen, beispielsweise & \ #174 für das® Zeichen.</span><span class="sxs-lookup"><span data-stu-id="605ce-234">Instead, use canonical numbered references to include these types of special characters, for example, &\#174 for the ® character.</span></span> <span data-ttu-id="605ce-235">Diese Regel gilt für alle Zeichenfolgenwerte in diesem Dokument.</span><span class="sxs-lookup"><span data-stu-id="605ce-235">This rule applies to all string values in this document.</span></span>

<span data-ttu-id="605ce-236"><http://www.w3.org/TR/xhtml1/dtds.html>Eine vollständige Liste der Zeichenentitäten finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="605ce-236">See <http://www.w3.org/TR/xhtml1/dtds.html> for a complete list of character entities.</span></span> <span data-ttu-id="605ce-237">UTF-8-codierte Dokumente enthalten möglicherweise die Unicode-Zeichen direkt.</span><span class="sxs-lookup"><span data-stu-id="605ce-237">UTF-8-encoded documents may include the Unicode characters directly.</span></span> <span data-ttu-id="605ce-238">Beim Speichern von Vorlagen über den UE-V-Generator werden Zeichenentitäten automatisch in ihre Unicode-Darstellungen konvertiert.</span><span class="sxs-lookup"><span data-stu-id="605ce-238">Saving templates through the UE-V Generator converts character entities to their Unicode representations automatically.</span></span>

 

### <a href="" id="id21"></a><span data-ttu-id="605ce-239">ID-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-239">ID Element</span></span>

**<span data-ttu-id="605ce-240">Obligatorisch: wahr</span><span class="sxs-lookup"><span data-stu-id="605ce-240">Mandatory: True</span></span>**

**<span data-ttu-id="605ce-241">Typ: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-241">Type: String</span></span>**

<span data-ttu-id="605ce-242">ID füllt einen eindeutigen Bezeichner für eine bestimmte Vorlage auf.</span><span class="sxs-lookup"><span data-stu-id="605ce-242">ID populates a unique identifier for a particular template.</span></span> <span data-ttu-id="605ce-243">Dieses Tag wird zur primären Kennung, mit der der UE-V-Agent zur Laufzeit auf die Vorlage verweist (Beispiel: Anzeigen der Ausgabe der PowerShell-Cmdlets "Get-UevTemplate" und "Get-UevTemplateProgram").</span><span class="sxs-lookup"><span data-stu-id="605ce-243">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime (for example, see the output of the Get-UevTemplate and Get-UevTemplateProgram PowerShell cmdlets).</span></span> <span data-ttu-id="605ce-244">Nach Konvention sollte dieses Tag keine Leerzeichen enthalten, was das Skripting vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="605ce-244">By convention, this tag should not contain any spaces, which simplifies scripting.</span></span> <span data-ttu-id="605ce-245">In diesem Element sollten Versionsnummern von Anwendungen angegeben werden, um eine einfache Identifizierung der Vorlage zu ermöglichen, beispielsweise `<ID>MicrosoftCalculator6</ID>` oder `<ID>MicrosoftOffice2010Win64</ID>` .</span><span class="sxs-lookup"><span data-stu-id="605ce-245">Version numbers of applications should be specified in this element to allow for easy identification of the template, such as `<ID>MicrosoftCalculator6</ID>` or `<ID>MicrosoftOffice2010Win64</ID>`.</span></span>

### <a href="" id="version21"></a><span data-ttu-id="605ce-246">Version-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-246">Version Element</span></span>

**<span data-ttu-id="605ce-247">Obligatorisch: wahr</span><span class="sxs-lookup"><span data-stu-id="605ce-247">Mandatory: True</span></span>**

**<span data-ttu-id="605ce-248">Typ: Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="605ce-248">Type: Integer</span></span>**

**<span data-ttu-id="605ce-249">Minimaler Wert: 0</span><span class="sxs-lookup"><span data-stu-id="605ce-249">Minimum Value: 0</span></span>**

**<span data-ttu-id="605ce-250">Maximaler Wert: 2147483647</span><span class="sxs-lookup"><span data-stu-id="605ce-250">Maximum Value: 2147483647</span></span>**

<span data-ttu-id="605ce-251">Version identifiziert die Version der Vorlage für die Einstellungsposition für die administrative Nachverfolgung von Änderungen.</span><span class="sxs-lookup"><span data-stu-id="605ce-251">Version identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="605ce-252">Der UE-V-Generator erhöht diese Zahl automatisch um eins, wenn die Vorlage gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="605ce-252">The UE-V Generator automatically increments this number by one each time the template is saved.</span></span> <span data-ttu-id="605ce-253">Beachten Sie, dass dieses Feld eine ganze Zahl Ganzzahl sein muss. Gebrochene Werte, beispielsweise `<Version>2.5</Version>` sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="605ce-253">Notice that this field must be a whole number integer; fractional values, such as `<Version>2.5</Version>` are not allowed.</span></span>

<span data-ttu-id="605ce-254">**Hinweis:** Sie können Notizen zu Versionsänderungen mithilfe von XML-Kommentar Tags speichern `<!-- -->` , beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="605ce-254">**Hint:** You can save notes about version changes using XML comment tags `<!-- -->`, for example:</span></span>

```xml
  <!--
     Version History

     Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
     Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
     Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
     Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
   -->
  <Version>4</Version>
```

<span data-ttu-id="605ce-255">**Wichtig**  Dieser Wert wird abgefragt, um zu ermitteln, ob eine neue Version einer Vorlage in diesen Fällen auf eine vorhandene Vorlage angewendet werden soll:</span><span class="sxs-lookup"><span data-stu-id="605ce-255">**Important** This value is queried to determine if a new version of a template should be applied to an existing template in these instances:</span></span>

-   <span data-ttu-id="605ce-256">Wenn der automatische Aktualisierungsvorgang der geplanten Vorlage ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="605ce-256">When the scheduled Template Auto Update task executes</span></span>

-   <span data-ttu-id="605ce-257">Wenn das PowerShell-Cmdlet "Update-UevTemplate" ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="605ce-257">When the Update-UevTemplate PowerShell cmdlet is executed</span></span>

-   <span data-ttu-id="605ce-258">Wenn die microsoft\\uev: SettingsLocationTemplate-Update Methode über WMI aufgerufen wird</span><span class="sxs-lookup"><span data-stu-id="605ce-258">When the microsoft\\uev:SettingsLocationTemplate Update method is called through WMI</span></span>

 

### <a href="" id="author21"></a><span data-ttu-id="605ce-259">Author-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-259">Author Element</span></span>

**<span data-ttu-id="605ce-260">Obligatorisch: falsch</span><span class="sxs-lookup"><span data-stu-id="605ce-260">Mandatory: False</span></span>**

**<span data-ttu-id="605ce-261">Typ: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-261">Type: String</span></span>**

<span data-ttu-id="605ce-262">Autor identifiziert den Ersteller der Vorlage für die Einstellungsposition.</span><span class="sxs-lookup"><span data-stu-id="605ce-262">Author identifies the creator of the settings location template.</span></span> <span data-ttu-id="605ce-263">Zwei optionale untergeordnete Elemente werden unterstützt: **Name** und **e-Mail**.</span><span class="sxs-lookup"><span data-stu-id="605ce-263">Two optional child elements are supported: **Name** and **Email**.</span></span> <span data-ttu-id="605ce-264">Beide Attribute sind optional, aber wenn das untergeordnete e-Mail-Element angegeben ist, muss es vom Name-Element begleitet werden.</span><span class="sxs-lookup"><span data-stu-id="605ce-264">Both attributes are optional, but, if the Email child element is specified, it must be accompanied by the Name element.</span></span> <span data-ttu-id="605ce-265">Der Autor bezieht sich auf den vollständigen Namen des Kontakts für die Vorlage "Settings Location", und e-Mail sollte auf eine e-Mail-Adresse für den Autor verweisen.</span><span class="sxs-lookup"><span data-stu-id="605ce-265">Author refers to the full name of the contact for the settings location template, and email should refer to an email address for the author.</span></span> <span data-ttu-id="605ce-266">Wir empfehlen, dass Sie diese Informationen in öffentlich veröffentlichte Vorlagen einbeziehen, beispielsweise im [Vorlagenkatalog UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span><span class="sxs-lookup"><span data-stu-id="605ce-266">We recommend that you include this information in templates published publicly, for example, on the [UE-V Template Gallery](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span></span>

### <a href="" id="processes21"></a><span data-ttu-id="605ce-267">Prozesse und Prozess Element</span><span class="sxs-lookup"><span data-stu-id="605ce-267">Processes and Process Element</span></span>

**<span data-ttu-id="605ce-268">Obligatorisch: wahr</span><span class="sxs-lookup"><span data-stu-id="605ce-268">Mandatory: True</span></span>**

**<span data-ttu-id="605ce-269">Typ: Element</span><span class="sxs-lookup"><span data-stu-id="605ce-269">Type: Element</span></span>**

<span data-ttu-id="605ce-270">Prozesse enthält mindestens ein `<Process>` Element, das wiederum die folgenden untergeordneten Elemente enthält: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**und **fileversion**.</span><span class="sxs-lookup"><span data-stu-id="605ce-270">Processes contains at least one `<Process>` element, which in turn contains the following child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="605ce-271">Das untergeordnete FileName-Element ist obligatorisch, die anderen sind optional.</span><span class="sxs-lookup"><span data-stu-id="605ce-271">The Filename child element is mandatory and the others are optional.</span></span> <span data-ttu-id="605ce-272">Ein vollständig aufgefülltes Element enthält Tags ähnlich wie in diesem Beispiel:</span><span class="sxs-lookup"><span data-stu-id="605ce-272">A fully populated element contains tags similar to this example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### <span data-ttu-id="605ce-273">Dateiname</span><span class="sxs-lookup"><span data-stu-id="605ce-273">Filename</span></span>

**<span data-ttu-id="605ce-274">Obligatorisch: wahr</span><span class="sxs-lookup"><span data-stu-id="605ce-274">Mandatory: True</span></span>**

**<span data-ttu-id="605ce-275">Typ: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-275">Type: String</span></span>**

<span data-ttu-id="605ce-276">Filename bezieht sich auf den tatsächlichen Dateinamen der ausführbaren Datei, wie Sie im Dateisystem angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="605ce-276">Filename refers to the actual file name of the executable as it appears in the file system.</span></span> <span data-ttu-id="605ce-277">Dieses Element gibt das primäre Kriterium an, mit dem UE-V auswerten soll, ob eine Vorlage für einen Prozess gilt oder nicht.</span><span class="sxs-lookup"><span data-stu-id="605ce-277">This element specifies the primary criterion that UE-V uses to evaluate whether a template applies to a process or not.</span></span> <span data-ttu-id="605ce-278">Dieses Element muss in der XML-Vorlage für die Einstellungsposition angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="605ce-278">This element must be specified in the settings location template XML.</span></span>

<span data-ttu-id="605ce-279">Gültige Dateinamen dürfen nicht mit dem regulären Ausdruck \ [^ \ \ \ \ \ \? \ \ \ \* \ \ | &lt; &gt; /: \] +, das heißt, Sie dürfen keine umgekehrten Schrägstriche, Sternchen-oder Fragezeichen-Wildcards, das Pipe-Zeichen, das größer-als-oder kleiner-als-Zeichen, den Schrägstrich oder den Doppelpunkt enthalten (\ \?</span><span class="sxs-lookup"><span data-stu-id="605ce-279">Valid filenames must not match the regular expression \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon (the \\ ?</span></span> <span data-ttu-id="605ce-280">\* | &lt; &gt; /oder: Zeichen.).</span><span class="sxs-lookup"><span data-stu-id="605ce-280">\* | &lt; &gt; / or : characters.).</span></span>

<span data-ttu-id="605ce-281">**Hinweis:** Um eine Zeichenfolge für diesen Regex zu testen, verwenden Sie ein PowerShell-Befehlsfenster, und ersetzen Sie den Namen der ausführbaren Datei für **YourFileName**:</span><span class="sxs-lookup"><span data-stu-id="605ce-281">**Hint:** To test a string against this regex, use a PowerShell command window and substitute your executable’s name for **YourFileName**:</span></span>

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

<span data-ttu-id="605ce-282">Der Wert **true** gibt an, dass die Zeichenfolge ungültige Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="605ce-282">A value of **True** indicates that the string contains illegal characters.</span></span> <span data-ttu-id="605ce-283">Im folgenden finden Sie einige Beispiele für ungültige Werte:</span><span class="sxs-lookup"><span data-stu-id="605ce-283">Here are some examples of illegal values:</span></span>

-   <span data-ttu-id="605ce-284">\\\\server\\share\\program.exe</span><span class="sxs-lookup"><span data-stu-id="605ce-284">\\\\server\\share\\program.exe</span></span>

-   <span data-ttu-id="605ce-285">Programm \ \*. exe</span><span class="sxs-lookup"><span data-stu-id="605ce-285">Program\*.exe</span></span>

-   <span data-ttu-id="605ce-286">Pro? ram.exe</span><span class="sxs-lookup"><span data-stu-id="605ce-286">Pro?ram.exe</span></span>

-   <span data-ttu-id="605ce-287">Programm &lt; 1 &gt; . exe</span><span class="sxs-lookup"><span data-stu-id="605ce-287">Program&lt;1&gt;.exe</span></span>

<span data-ttu-id="605ce-288">**Hinweis**  Der UE-V-Generator codiert das größer-als-und das kleiner-als-Zeichen &gt; &lt; .</span><span class="sxs-lookup"><span data-stu-id="605ce-288">**Note** The UE-V Generator encodes the greater than and less than characters as &gt; and &lt; respectively.</span></span>

 

<span data-ttu-id="605ce-289">In seltenen Fällen enthält der FileName-Wert nicht unbedingt die Erweiterung ". exe", sollte aber als Teil des Werts angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="605ce-289">In rare circumstances, the FileName value will not necessarily include the .exe extension, but it should be specified as part of the value.</span></span> <span data-ttu-id="605ce-290">Beispielsweise `<Filename>MyApplictication.exe</Filename>` sollte angegeben werden, anstatt `<Filename>MyApplictication</Filename>` .</span><span class="sxs-lookup"><span data-stu-id="605ce-290">For example, `<Filename>MyApplictication.exe</Filename>` should be specified instead of `<Filename>MyApplictication</Filename>`.</span></span> <span data-ttu-id="605ce-291">Im zweiten Beispiel wird die Vorlage nicht auf den Prozess angewendet, wenn der tatsächliche Name der ausführbaren Datei "MyApplication.exe" lautet.</span><span class="sxs-lookup"><span data-stu-id="605ce-291">The second example will not apply the template to the process if the actual name of the executable file is “MyApplication.exe”.</span></span>

### <span data-ttu-id="605ce-292">Architektur</span><span class="sxs-lookup"><span data-stu-id="605ce-292">Architecture</span></span>

**<span data-ttu-id="605ce-293">Obligatorisch: falsch</span><span class="sxs-lookup"><span data-stu-id="605ce-293">Mandatory: False</span></span>**

**<span data-ttu-id="605ce-294">Typ: Architektur (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="605ce-294">Type: Architecture (String)</span></span>**

<span data-ttu-id="605ce-295">Architektur bezieht sich auf die Prozessorarchitektur, für die die ausführbare Ziel Datei kompiliert wurde.</span><span class="sxs-lookup"><span data-stu-id="605ce-295">Architecture refers to the processor architecture for which the target executable was compiled.</span></span> <span data-ttu-id="605ce-296">Gültige Werte sind Win32 für 32-Bit-Anwendungen oder win64 für 64-Bit-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="605ce-296">Valid values are Win32 for 32-bit applications or Win64 for 64-bit applications.</span></span> <span data-ttu-id="605ce-297">Sofern vorhanden, schränkt dieses Tag die Anwendbarkeit der Vorlage "Settings Location" auf eine bestimmte Anwendungsarchitektur ein.</span><span class="sxs-lookup"><span data-stu-id="605ce-297">If present, this tag limits the applicability of the settings location template to a particular application architecture.</span></span> <span data-ttu-id="605ce-298">Ein Beispiel hierfür finden Sie unter Vergleich der%programfiles%\\Microsoft-Benutzeroberflächen-Virtualization\\templates\\ MicrosoftOffice2010Win32.xml und MicrosoftOffice2010Win64.xml Dateien, die in UE-V enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="605ce-298">For an example of this, compare the %ProgramFiles%\\Microsoft User Experience Virtualization\\templates\\ MicrosoftOffice2010Win32.xml and MicrosoftOffice2010Win64.xml files included with UE-V.</span></span> <span data-ttu-id="605ce-299">Dies ist hilfreich, wenn relative Pfade zwischen unterschiedlichen Versionen einer ausführbaren Datei geändert werden oder wenn Einstellungen hinzugefügt oder entfernt wurden, wenn Sie von einer Prozessorarchitektur zu einer anderen wechseln.</span><span class="sxs-lookup"><span data-stu-id="605ce-299">This is useful when relative paths change between different versions of an executable or if settings have been added or removed when moving from one processor architecture to another.</span></span>

<span data-ttu-id="605ce-300">Wenn dieses Element nicht vorhanden ist, ignoriert die Vorlage "Einstellungen" die Architektur des Prozesses und bezieht sich auf 32-und 64-Bit-Prozesse, wenn der Dateiname und andere Attribute angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="605ce-300">If this element is absent, the settings location template ignores the process’ architecture and applies to both 32 and 64-bit processes if the file name and other attributes apply.</span></span>

<span data-ttu-id="605ce-301">**Hinweis**  UE-V unterstützt keine ARM-Prozessoren in dieser Version.</span><span class="sxs-lookup"><span data-stu-id="605ce-301">**Note** UE-V does not support ARM processors in this version.</span></span>

 

### <span data-ttu-id="605ce-302">ProductName</span><span class="sxs-lookup"><span data-stu-id="605ce-302">ProductName</span></span>

**<span data-ttu-id="605ce-303">Obligatorisch: falsch</span><span class="sxs-lookup"><span data-stu-id="605ce-303">Mandatory: False</span></span>**

**<span data-ttu-id="605ce-304">Typ: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-304">Type: String</span></span>**

<span data-ttu-id="605ce-305">ProductName ist ein optionales Element, das verwendet wird, um ein Produkt für administrative Zwecke oder Berichte zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="605ce-305">ProductName is an optional element used to identify a product for administrative purposes or reporting.</span></span> <span data-ttu-id="605ce-306">ProductName unterscheidet sich von filename dadurch, dass für seinen Wert keine regulären Ausdruckseinschränkungen gelten.</span><span class="sxs-lookup"><span data-stu-id="605ce-306">ProductName differs from Filename in that there are no regular expression restrictions on its value.</span></span> <span data-ttu-id="605ce-307">Auf diese Weise können Beschreibungen eines Prozesses leichter verstanden werden, bei denen der Name der ausführbaren Datei möglicherweise nicht offensichtlich ist.</span><span class="sxs-lookup"><span data-stu-id="605ce-307">This allows for more easily understood descriptions of a process where the executable name may not be obvious.</span></span> <span data-ttu-id="605ce-308">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="605ce-308">For example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### <span data-ttu-id="605ce-309">FileDescription</span><span class="sxs-lookup"><span data-stu-id="605ce-309">FileDescription</span></span>

**<span data-ttu-id="605ce-310">Obligatorisch: falsch</span><span class="sxs-lookup"><span data-stu-id="605ce-310">Mandatory: False</span></span>**

**<span data-ttu-id="605ce-311">Typ: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-311">Type: String</span></span>**

<span data-ttu-id="605ce-312">FileDescription ist ein optionales Tag, das eine administrative Beschreibung der ausführbaren Datei ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="605ce-312">FileDescription is an optional tag that allows for an administrative description of the executable file.</span></span> <span data-ttu-id="605ce-313">Hierbei handelt es sich um ein kostenloses Textfeld, das bei der Unterscheidung mehrerer ausführbarer Dateien innerhalb eines Softwarepakets hilfreich sein kann, wenn die Funktion der ausführbaren Datei identifiziert werden muss.</span><span class="sxs-lookup"><span data-stu-id="605ce-313">This is a free text field and can be useful in distinguishing multiple executables within a software package where there is a need to identify the function of the executable.</span></span>

<span data-ttu-id="605ce-314">In einer geeigneten Anwendung kann es beispielsweise hilfreich sein, die Funktion von zwei ausführbaren Dateien (MyApplication.exe und MyApplicationHelper.exe) zu informieren, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="605ce-314">For example, in a suited application, it might be useful to provide reminders about the function of two executables (MyApplication.exe and MyApplicationHelper.exe), as shown here:</span></span>

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### <span data-ttu-id="605ce-315">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="605ce-315">ProductVersion</span></span>

**<span data-ttu-id="605ce-316">Obligatorisch: falsch</span><span class="sxs-lookup"><span data-stu-id="605ce-316">Mandatory: False</span></span>**

**<span data-ttu-id="605ce-317">Typ: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-317">Type: String</span></span>**

<span data-ttu-id="605ce-318">ProductVersion bezieht sich auf die Haupt-und Nebenversionen einer Datei sowie auf eine Build-und Patchebene.</span><span class="sxs-lookup"><span data-stu-id="605ce-318">ProductVersion refers to the major and minor product versions of a file, as well as a build and patch level.</span></span> <span data-ttu-id="605ce-319">ProductVersion ist ein optionales Element, aber wenn angegeben, muss es mindestens das wichtigste untergeordnete Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="605ce-319">ProductVersion is an optional element, but if specified, it must contain at least the Major child element.</span></span> <span data-ttu-id="605ce-320">Der Wert muss einen Bereich in der Form mindestens = "x" Maximum = "y" ausdrücken, wobei X und Y ganze Zahlen sind.</span><span class="sxs-lookup"><span data-stu-id="605ce-320">The value must express a range in the form Minimum="X" Maximum="Y" where X and Y are integers.</span></span> <span data-ttu-id="605ce-321">Die Mindest-und Höchstwerte können identisch sein.</span><span class="sxs-lookup"><span data-stu-id="605ce-321">The Minimum and Maximum values can be identical.</span></span>

<span data-ttu-id="605ce-322">Die Elemente "Produkt" und "Dateiversion" werden möglicherweise nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="605ce-322">The product and file version elements may be left unspecified.</span></span> <span data-ttu-id="605ce-323">Dadurch wird die Vorlage "versionsunabhängig", was bedeutet, dass die Vorlage auf alle Versionen der angegebenen ausführbaren Datei angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="605ce-323">Doing so makes the template “version agnostic”, meaning that the template will apply to all versions of the specified executable.</span></span>

**<span data-ttu-id="605ce-324">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="605ce-324">Example 1:</span></span>**

<span data-ttu-id="605ce-325">Produktversion: 1,0, die im UE-V-Generator angegeben wird, erzeugt den folgenden XML-Code:</span><span class="sxs-lookup"><span data-stu-id="605ce-325">Product version: 1.0 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**<span data-ttu-id="605ce-326">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="605ce-326">Example 2:</span></span>**

<span data-ttu-id="605ce-327">Dateiversion: im UE-V-Generator angegebene 5.0.2.1000 erzeugt den folgenden XML-Code:</span><span class="sxs-lookup"><span data-stu-id="605ce-327">File version: 5.0.2.1000 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**<span data-ttu-id="605ce-328">Falsches Beispiel 1 – unvollständiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="605ce-328">Incorrect Example 1 – incomplete range:</span></span>**

<span data-ttu-id="605ce-329">Es ist nur das kleinste Attribut vorhanden.</span><span class="sxs-lookup"><span data-stu-id="605ce-329">Only the Minimum attribute is present.</span></span> <span data-ttu-id="605ce-330">Maximum muss auch in einem Bereich enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="605ce-330">Maximum must be included in a range as well.</span></span>

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**<span data-ttu-id="605ce-331">Falsches Beispiel 2 – Moll ohne Hauptelement angegeben:</span><span class="sxs-lookup"><span data-stu-id="605ce-331">Incorrect Example 2 – Minor specified without Major element:</span></span>**

<span data-ttu-id="605ce-332">Nur das nebengeordnete Element ist vorhanden.</span><span class="sxs-lookup"><span data-stu-id="605ce-332">Only the Minor element is present.</span></span> <span data-ttu-id="605ce-333">Major muss ebenfalls enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="605ce-333">Major must be included as well.</span></span>

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### <span data-ttu-id="605ce-334">File Version</span><span class="sxs-lookup"><span data-stu-id="605ce-334">FileVersion</span></span>

**<span data-ttu-id="605ce-335">Obligatorisch: falsch</span><span class="sxs-lookup"><span data-stu-id="605ce-335">Mandatory: False</span></span>**

**<span data-ttu-id="605ce-336">Typ: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-336">Type: String</span></span>**

<span data-ttu-id="605ce-337">Fileversion unterscheidet zwischen der Veröffentlichungsversion einer veröffentlichten Anwendung und den internen Builddaten einer ausführbaren Komponente.</span><span class="sxs-lookup"><span data-stu-id="605ce-337">FileVersion differentiates between the release version of a published application and the internal build details of a component executable.</span></span> <span data-ttu-id="605ce-338">Bei den meisten kommerziellen Anwendungen sind diese Nummern identisch.</span><span class="sxs-lookup"><span data-stu-id="605ce-338">For the majority of commercial applications, these numbers are identical.</span></span> <span data-ttu-id="605ce-339">Wenn Sie unterschiedlich sind, gibt die Produktversion einer Datei eine generische Versionskennung einer Datei an, während die Dateiversion einen bestimmten Build einer Datei angibt (wie im Fall eines Hotfix oder Updates).</span><span class="sxs-lookup"><span data-stu-id="605ce-339">Where they vary, the product version of a file indicates a generic version identification of a file, while file version indicates a specific build of a file (as in the case of a hotfix or update).</span></span> <span data-ttu-id="605ce-340">Dadurch werden Dateien eindeutig identifiziert, ohne die Erkennungslogik zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="605ce-340">This uniquely identifies files without breaking detection logic.</span></span>

<span data-ttu-id="605ce-341">Wenn Sie die Produktversion und die Dateiversion einer bestimmten ausführbaren Datei ermitteln möchten, klicken Sie mit der rechten Maustaste auf die Datei in Windows-Explorer, wählen Sie Eigenschaften aus, und klicken Sie dann auf die Registerkarte Details.</span><span class="sxs-lookup"><span data-stu-id="605ce-341">To determine the product version and file version of a particular executable, right-click on the file in Windows Explorer, select Properties, then click on the Details tab.</span></span>

<span data-ttu-id="605ce-342">Das Einfügen eines fileversion-Elements für eine Anwendung ermöglicht eine genauere Feintuning-Erkennungslogik, ist für die meisten Anwendungen jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="605ce-342">Including a FileVersion element for an application allows for more granular fine-tuning detection logic, but is not necessary for most applications.</span></span> <span data-ttu-id="605ce-343">Die ProductVersion-Elementeinstellungen werden zuerst überprüft, und dann wird die Dateiversion aktiviert.</span><span class="sxs-lookup"><span data-stu-id="605ce-343">The ProductVersion element settings are checked first, and then FileVersion is checked.</span></span> <span data-ttu-id="605ce-344">Die restriktivere Einstellung wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="605ce-344">The more restrictive setting will apply.</span></span>

<span data-ttu-id="605ce-345">Die untergeordneten Elemente und Syntaxregeln für fileversion sind mit denen von ProductVersion identisch.</span><span class="sxs-lookup"><span data-stu-id="605ce-345">The child elements and syntax rules for FileVersion are identical to those of ProductVersion.</span></span>

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application21"></a><span data-ttu-id="605ce-346">Application-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-346">Application Element</span></span>

<span data-ttu-id="605ce-347">Application ist ein Container für Einstellungen, die für eine bestimmte Anwendung gelten.</span><span class="sxs-lookup"><span data-stu-id="605ce-347">Application is a container for settings that apply to a particular application.</span></span> <span data-ttu-id="605ce-348">Es handelt sich um eine Sammlung der folgenden Felder/Typen.</span><span class="sxs-lookup"><span data-stu-id="605ce-348">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="605ce-349">Feld/Typ</span><span class="sxs-lookup"><span data-stu-id="605ce-349">Field/Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="605ce-350">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="605ce-350">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-351">Name</span><span class="sxs-lookup"><span data-stu-id="605ce-351">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-352">Gibt einen eindeutigen Namen für die Vorlage "Settings Location" an.</span><span class="sxs-lookup"><span data-stu-id="605ce-352">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="605ce-353">Diese Funktion wird für Anzeigezwecke verwendet, wenn Sie in WMI, PowerShell, Ereignisanzeige und Debug-Protokollen auf die Vorlage verweisen.</span><span class="sxs-lookup"><span data-stu-id="605ce-353">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="605ce-354">Weitere Informationen finden Sie unter <a href="#name21" data-raw-source="[Name](#name21)"> Name </a> .</span><span class="sxs-lookup"><span data-stu-id="605ce-354">For more information, see <a href="#name21" data-raw-source="[Name](#name21)">Name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-355">ID</span><span class="sxs-lookup"><span data-stu-id="605ce-355">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-356">Füllt einen eindeutigen Bezeichner für eine bestimmte Vorlage auf.</span><span class="sxs-lookup"><span data-stu-id="605ce-356">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="605ce-357">Dieses Tag wird zur primären Kennung, mit der der UE-V-Agent zur Laufzeit auf die Vorlage verweist.</span><span class="sxs-lookup"><span data-stu-id="605ce-357">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="605ce-358">Weitere Informationen finden Sie unter <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="605ce-358">For more information, see <a href="#id21" data-raw-source="[ID](#id21)">ID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-359">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="605ce-359">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-360">Eine optionale Beschreibung der Vorlage.</span><span class="sxs-lookup"><span data-stu-id="605ce-360">An optional description of the template.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-361">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="605ce-361">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-362">Ein optionaler Name, der auf der Benutzeroberfläche angezeigt wird und von einem Gebietsschema der Sprache lokalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="605ce-362">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-363">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="605ce-363">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-364">Eine optionale Vorlagenbeschreibung, die von einem Sprachgebietsschema lokalisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="605ce-364">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-365">Version</span><span class="sxs-lookup"><span data-stu-id="605ce-365">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-366">Identifiziert die Version der Vorlage für die Einstellungsposition für die administrative Nachverfolgung von Änderungen.</span><span class="sxs-lookup"><span data-stu-id="605ce-366">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="605ce-367">Weitere Informationen finden Sie unter <a href="#version21" data-raw-source="[Version](#version21)"> Version </a> .</span><span class="sxs-lookup"><span data-stu-id="605ce-367">For more information, see <a href="#version21" data-raw-source="[Version](#version21)">Version</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-368">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="605ce-368">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-369">Steuert, ob diese Vorlage in Verbindung mit einem Microsoft-Konto aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="605ce-369">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="605ce-370">Wenn die Synchronisierung von MSA für einen Benutzer auf einem Computer aktiviert ist, wird diese Vorlage automatisch deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="605ce-370">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-371">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="605ce-371">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-372">Ähnlich wie MSA steuert dies, ob diese Vorlage in Verbindung mit Office365 aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="605ce-372">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="605ce-373">Wenn Office 365 zum Synchronisieren von Einstellungen verwendet wird, wird diese Vorlage automatisch deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="605ce-373">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-374">FixedProfile (eingeführt in 2,1)</span><span class="sxs-lookup"><span data-stu-id="605ce-374">FixedProfile (Introduced in 2.1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-375">Gibt an, dass diese Vorlage nur dem in diesem Element angegebenen Profil zugeordnet werden kann und nicht über WMI oder PowerShell geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="605ce-375">Specifies that this template can only be associated with the profile specified within this element, and cannot be changed via WMI or PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-376">Prozesse</span><span class="sxs-lookup"><span data-stu-id="605ce-376">Processes</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-377">Ein Container für eine Sammlung von einem oder mehreren Process-Elementen.</span><span class="sxs-lookup"><span data-stu-id="605ce-377">A container for a collection of one or more Process elements.</span></span> <span data-ttu-id="605ce-378">Weitere Informationen finden Sie unter <a href="#processes21" data-raw-source="[Processes](#processes21)"> Prozesse </a> .</span><span class="sxs-lookup"><span data-stu-id="605ce-378">For more information, see <a href="#processes21" data-raw-source="[Processes](#processes21)">Processes</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-379">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="605ce-379">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-380">Ein Container für alle Einstellungen, die für eine bestimmte Vorlage gelten.</span><span class="sxs-lookup"><span data-stu-id="605ce-380">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="605ce-381">Sie enthält Instanzen der Registrierungs-, Datei-, Systemparameter-und benutzerdefinierten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="605ce-381">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="605ce-382">Weitere Informationen finden Sie unter <strong> Einstellungen </strong> in <a href="#data21" data-raw-source="[Data types](#data21)"> Datentypen </a> .</span><span class="sxs-lookup"><span data-stu-id="605ce-382">For more information, see <strong>Settings</strong> in <a href="#data21" data-raw-source="[Data types](#data21)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common21"></a><span data-ttu-id="605ce-383">Common-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-383">Common Element</span></span>

<span data-ttu-id="605ce-384">Common ist mit einem Application-Element vergleichbar, wird aber immer mit zwei oder mehr Anwendungselementen verknüpft.</span><span class="sxs-lookup"><span data-stu-id="605ce-384">Common is similar to an Application element, but it is always associated with two or more Application elements.</span></span> <span data-ttu-id="605ce-385">Der allgemeine Abschnitt stellt den Satz von Einstellungen dar, die zwischen diesen Anwendungsinstanzen freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="605ce-385">The Common section represents the set of settings that are shared between those Application instances.</span></span> <span data-ttu-id="605ce-386">Es handelt sich um eine Sammlung der folgenden Felder/Typen.</span><span class="sxs-lookup"><span data-stu-id="605ce-386">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="605ce-387">Feld/Typ</span><span class="sxs-lookup"><span data-stu-id="605ce-387">Field/Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="605ce-388">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="605ce-388">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-389">Name</span><span class="sxs-lookup"><span data-stu-id="605ce-389">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-390">Gibt einen eindeutigen Namen für die Vorlage "Settings Location" an.</span><span class="sxs-lookup"><span data-stu-id="605ce-390">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="605ce-391">Diese Funktion wird für Anzeigezwecke verwendet, wenn Sie in WMI, PowerShell, Ereignisanzeige und Debug-Protokollen auf die Vorlage verweisen.</span><span class="sxs-lookup"><span data-stu-id="605ce-391">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="605ce-392">Weitere Informationen finden Sie unter <a href="#name21" data-raw-source="[Name](#name21)"> Name </a> .</span><span class="sxs-lookup"><span data-stu-id="605ce-392">For more information, see <a href="#name21" data-raw-source="[Name](#name21)">Name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-393">ID</span><span class="sxs-lookup"><span data-stu-id="605ce-393">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-394">Füllt einen eindeutigen Bezeichner für eine bestimmte Vorlage auf.</span><span class="sxs-lookup"><span data-stu-id="605ce-394">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="605ce-395">Dieses Tag wird zur primären Kennung, mit der der UE-V-Agent zur Laufzeit auf die Vorlage verweist.</span><span class="sxs-lookup"><span data-stu-id="605ce-395">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="605ce-396">Weitere Informationen finden Sie unter <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="605ce-396">For more information, see <a href="#id21" data-raw-source="[ID](#id21)">ID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-397">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="605ce-397">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-398">Eine optionale Beschreibung der Vorlage.</span><span class="sxs-lookup"><span data-stu-id="605ce-398">An optional description of the template.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-399">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="605ce-399">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-400">Ein optionaler Name, der auf der Benutzeroberfläche angezeigt wird und von einem Gebietsschema der Sprache lokalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="605ce-400">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-401">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="605ce-401">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-402">Eine optionale Vorlagenbeschreibung, die von einem Sprachgebietsschema lokalisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="605ce-402">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-403">Version</span><span class="sxs-lookup"><span data-stu-id="605ce-403">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-404">Identifiziert die Version der Vorlage für die Einstellungsposition für die administrative Nachverfolgung von Änderungen.</span><span class="sxs-lookup"><span data-stu-id="605ce-404">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="605ce-405">Weitere Informationen finden Sie unter <a href="#version21" data-raw-source="[Version](#version21)"> Version </a> .</span><span class="sxs-lookup"><span data-stu-id="605ce-405">For more information, see <a href="#version21" data-raw-source="[Version](#version21)">Version</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-406">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="605ce-406">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-407">Steuert, ob diese Vorlage in Verbindung mit einem Microsoft-Konto aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="605ce-407">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="605ce-408">Wenn die Synchronisierung von MSA für einen Benutzer auf einem Computer aktiviert ist, wird diese Vorlage automatisch deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="605ce-408">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-409">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="605ce-409">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-410">Ähnlich wie MSA steuert dies, ob diese Vorlage in Verbindung mit Office365 aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="605ce-410">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="605ce-411">Wenn Office 365 zum Synchronisieren von Einstellungen verwendet wird, wird diese Vorlage automatisch deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="605ce-411">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-412">FixedProfile (eingeführt in 2,1)</span><span class="sxs-lookup"><span data-stu-id="605ce-412">FixedProfile (Introduced in 2.1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-413">Gibt an, dass diese Vorlage nur dem in diesem Element angegebenen Profil zugeordnet werden kann und nicht über WMI oder PowerShell geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="605ce-413">Specifies that this template can only be associated with the profile specified within this element, and cannot be changed via WMI or PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-414">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="605ce-414">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-415">Ein Container für alle Einstellungen, die für eine bestimmte Vorlage gelten.</span><span class="sxs-lookup"><span data-stu-id="605ce-415">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="605ce-416">Sie enthält Instanzen der Registrierungs-, Datei-, Systemparameter-und benutzerdefinierten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="605ce-416">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="605ce-417">Weitere Informationen finden Sie unter <strong> Einstellungen </strong> in <a href="#data21" data-raw-source="[Data types](#data21)"> Datentypen </a> .</span><span class="sxs-lookup"><span data-stu-id="605ce-417">For more information, see <strong>Settings</strong> in <a href="#data21" data-raw-source="[Data types](#data21)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate21"></a><span data-ttu-id="605ce-418">SettingsLocationTemplate-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-418">SettingsLocationTemplate Element</span></span>

<span data-ttu-id="605ce-419">Dieses Element definiert die Einstellungen für eine einzelne Anwendung oder eine Suite von Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="605ce-419">This element defines the settings for a single application or a suite of applications.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="605ce-420">Feld/Typ</span><span class="sxs-lookup"><span data-stu-id="605ce-420">Field/Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="605ce-421">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="605ce-421">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-422">Name</span><span class="sxs-lookup"><span data-stu-id="605ce-422">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-423">Gibt einen eindeutigen Namen für die Vorlage "Settings Location" an.</span><span class="sxs-lookup"><span data-stu-id="605ce-423">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="605ce-424">Diese Funktion wird für Anzeigezwecke verwendet, wenn Sie in WMI, PowerShell, Ereignisanzeige und Debug-Protokollen auf die Vorlage verweisen.</span><span class="sxs-lookup"><span data-stu-id="605ce-424">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="605ce-425">Weitere Informationen finden Sie unter <a href="#name21" data-raw-source="[Name](#name21)"> Name </a> .</span><span class="sxs-lookup"><span data-stu-id="605ce-425">For more information, see <a href="#name21" data-raw-source="[Name](#name21)">Name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-426">ID</span><span class="sxs-lookup"><span data-stu-id="605ce-426">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-427">Füllt einen eindeutigen Bezeichner für eine bestimmte Vorlage auf.</span><span class="sxs-lookup"><span data-stu-id="605ce-427">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="605ce-428">Dieses Tag wird zur primären Kennung, mit der der UE-V-Agent zur Laufzeit auf die Vorlage verweist.</span><span class="sxs-lookup"><span data-stu-id="605ce-428">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="605ce-429">Weitere Informationen finden Sie unter <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="605ce-429">For more information, see <a href="#id21" data-raw-source="[ID](#id21)">ID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-430">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="605ce-430">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-431">Eine optionale Beschreibung der Vorlage.</span><span class="sxs-lookup"><span data-stu-id="605ce-431">An optional description of the template.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-432">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="605ce-432">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-433">Ein optionaler Name, der auf der Benutzeroberfläche angezeigt wird und von einem Gebietsschema der Sprache lokalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="605ce-433">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-434">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="605ce-434">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-435">Eine optionale Vorlagenbeschreibung, die von einem Sprachgebietsschema lokalisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="605ce-435">An optional template description localized by a language locale.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix21"></a><span data-ttu-id="605ce-436">Anhang: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="605ce-436">Appendix: SettingsLocationTemplate.xsd</span></span>

<span data-ttu-id="605ce-437">Hier sehen Sie die SettingsLocationTemplate. xsd-Datei mit den Elementen, untergeordneten Elementen, Attributen und Parametern:</span><span class="sxs-lookup"><span data-stu-id="605ce-437">Here is the SettingsLocationTemplate.xsd file showing its elements, child elements, attributes, and parameters:</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

    <xs:simpleType name="Guid">
        <xs:restriction base="xs:string">
            <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="FilenameString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="IDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="CompositeIDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+([.][^\\\?\*\|&lt;&gt;/:.]+)?" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="TemplateVersion">
        <xs:restriction base="xs:integer">
            <xs:minInclusive value="0" />
            <xs:maxInclusive value="2147483647" />
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Empty">
        <xs:sequence/>
    </xs:complexType>

    <xs:complexType name="LocalizedString">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Locale" type="xs:string" use="required"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="LocalizedName">
        <xs:sequence>
            <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="LocalizedDescription">
        <xs:sequence>
            <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="ReplacedTemplates">
      <xs:sequence>
        <xs:element name="ID" type="CompositeIDString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Author">
        <xs:all>
            <xs:element name="Name" type="xs:string" minOccurs="1" />
            <xs:element name="Email" type="xs:string" minOccurs="0" />
        </xs:all>
    </xs:complexType>

    <xs:complexType name="Range">
        <xs:attribute name="Minimum" type="xs:integer" use="required"/>
        <xs:attribute name="Maximum" type="xs:integer" use="required"/>
    </xs:complexType>

    <xs:complexType name="ProcessVersion">
        <xs:sequence>
            <xs:element name="Major" type="Range" minOccurs="1" />
            <xs:element name="Minor" type="Range" minOccurs="0" />
            <xs:element name="Build" type="Range" minOccurs="0" />
            <xs:element name="Patch" type="Range" minOccurs="0" />
        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="Architecture">
        <xs:restriction base="xs:string">
            <xs:enumeration value="Win32"/>
            <xs:enumeration value="Win64"/>
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Process">
        <xs:sequence>
            <xs:element name="Filename" type="FilenameString" minOccurs="1" />
            <xs:element name="Architecture" type="Architecture" minOccurs="0" />
            <xs:element name="ProductName" type="xs:string" minOccurs="0" />
            <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
            <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
            <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Processes">
        <xs:sequence>
            <xs:choice minOccurs="1">
                <xs:element name="Process" type="Process" />
                <xs:element name="ShellProcess" type="Empty" />
            </xs:choice>
            <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Path">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
                <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="RegistrySetting">
        <xs:sequence>
            <xs:element name="Path" type="Path" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="FileSetting">
        <xs:sequence>

            <xs:element name="Root">
                <xs:complexType>
                    <xs:choice>
                        <xs:element name="KnownFolder" type="Guid" />
                        <xs:element name="RegistryEntry" type="xs:string" />
                        <xs:element name="EnvironmentVariable" type="xs:string" />
                    </xs:choice>
                </xs:complexType>
            </xs:element>

            <xs:element name="Path" minOccurs="0" type="Path" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>

        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="CustomActionSetting">
        <xs:restriction base="xs:anyURI"/>
    </xs:simpleType>

    <xs:simpleType name="SystemParameterSetting">
        <xs:restriction base="xs:string">

            <!-- Accessibility parameters -->
            <xs:enumeration value="AccessTimeout"/>
            <xs:enumeration value="AudioDescription"/>
            <xs:enumeration value="ClientAreaAnimation"/>
            <xs:enumeration value="DisableOverlappedContent"/>
            <xs:enumeration value="FilterKeys"/>
            <xs:enumeration value="FocusBorderHeight"/>
            <xs:enumeration value="FocusBorderWidth"/>
            <xs:enumeration value="HighContrast"/>
            <xs:enumeration value="MessageDuration"/>
            <xs:enumeration value="MouseClickLock"/>
            <xs:enumeration value="MouseClickLockTime"/>
            <xs:enumeration value="MouseKeys"/>
            <xs:enumeration value="MouseSonar"/>
            <xs:enumeration value="MouseVanish"/>
            <xs:enumeration value="ScreenReader"/>
            <xs:enumeration value="ShowSounds"/>
            <xs:enumeration value="SoundSentry"/>
            <xs:enumeration value="StickyKeys"/>
            <xs:enumeration value="ToggleKeys"/>

            <!-- Input parameters -->
            <xs:enumeration value="Beep"/>
            <xs:enumeration value="BlockSendInputResets"/>
            <xs:enumeration value="DefaultInputLang"/>
            <xs:enumeration value="DoubleClickTime"/>
            <xs:enumeration value="DoubleClkHeight"/>
            <xs:enumeration value="DoubleClkWidth"/>
            <xs:enumeration value="KeyboardCues"/>
            <xs:enumeration value="KeyboardDelay"/>
            <xs:enumeration value="KeyboardPref"/>
            <xs:enumeration value="KeyboardSpeed"/>
            <xs:enumeration value="Mouse"/>
            <xs:enumeration value="MouseButtonSwap"/>
            <xs:enumeration value="MouseHoverHeight"/>
            <xs:enumeration value="MouseHoverTime"/>
            <xs:enumeration value="MouseHoverWidth"/>
            <xs:enumeration value="MouseSpeed"/>
            <xs:enumeration value="MouseTrails"/>
            <xs:enumeration value="SnapToDefButton"/>
            <xs:enumeration value="WheelScrollChars"/>
            <xs:enumeration value="WheelScrollLines"/>

            <!-- Desktop parameters (limited subset) -->
            <xs:enumeration value="DeskWallpaper"/>
            <xs:enumeration value="DesktopColor"/>

        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Settings">
        <xs:sequence>
            <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
            <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
            <xs:element name="AlwaysApplySettings" type="xs:boolean" minOccurs="0" />
            <xs:choice minOccurs="0" maxOccurs="unbounded">
                <xs:element name="Registry" type="RegistrySetting" />
                <xs:element name="File" type="FileSetting" />
                <xs:element name="SystemParameter" type="SystemParameterSetting" />
                <xs:element name="CustomAction" type="CustomActionSetting" />
            </xs:choice>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Common">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Application">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>


    <xs:element name="SettingsLocationTemplate">
        <xs:complexType>
            <xs:sequence>

                <xs:element name="Name" type="xs:string" />
                <xs:element name="ID" type="IDString" />
                <xs:element name="Description" type="xs:string" minOccurs="0" />
                <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
                <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

                <xs:choice>

                    <!-- Single application -->
                    <xs:sequence>
                        <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
                        <xs:element name="Version" type="TemplateVersion" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
                        <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
                        <xs:element name="Processes" type="Processes" />
                        <xs:element name="Settings" type="Settings" />
                    </xs:sequence>

                    <!-- Suite of applications -->
                    <xs:sequence>
                        <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="Common" type="Common" />
                        <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
                    </xs:sequence>

                </xs:choice>

            </xs:sequence>
        </xs:complexType>
    </xs:element>
    <!-- SettingsLocationTemplate -->

</xs:schema>
```

## <span data-ttu-id="605ce-438">UE-V 2,0-Schema Referenz für Anwendungsvorlagen</span><span class="sxs-lookup"><span data-stu-id="605ce-438">UE-V 2.0 Application Template Schema Reference</span></span>


<span data-ttu-id="605ce-439">In diesem Abschnitt wird die XML-Struktur der Standort Vorlage "UE-V 2,0 Settings" erläutert, und es werden Anleitungen zum Bearbeiten dieser Datei bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="605ce-439">This section details the XML structure of the UE-V 2.0 settings location template and provides guidance for editing this file.</span></span>

### <span data-ttu-id="605ce-440">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="605ce-440">In This Section</span></span>

-   [<span data-ttu-id="605ce-441">XML-Deklaration und Codierungsattribut</span><span class="sxs-lookup"><span data-stu-id="605ce-441">XML Declaration and Encoding Attribute</span></span>](#xml)

-   [<span data-ttu-id="605ce-442">Namespace und Stamm Element</span><span class="sxs-lookup"><span data-stu-id="605ce-442">Namespace and Root Element</span></span>](#namespace)

-   [<span data-ttu-id="605ce-443">Datentypen</span><span class="sxs-lookup"><span data-stu-id="605ce-443">Data types</span></span>](#data)

-   [<span data-ttu-id="605ce-444">Name-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-444">Name Element</span></span>](#name)

-   [<span data-ttu-id="605ce-445">ID-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-445">ID Element</span></span>](#id)

-   [<span data-ttu-id="605ce-446">Version-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-446">Version Element</span></span>](#version)

-   [<span data-ttu-id="605ce-447">Author-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-447">Author Element</span></span>](#author)

-   [<span data-ttu-id="605ce-448">Prozesse und Prozess Element</span><span class="sxs-lookup"><span data-stu-id="605ce-448">Processes and Process Element</span></span>](#processes)

-   [<span data-ttu-id="605ce-449">Application-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-449">Application Element</span></span>](#application)

-   [<span data-ttu-id="605ce-450">Common-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-450">Common Element</span></span>](#common)

-   [<span data-ttu-id="605ce-451">SettingsLocationTemplate-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-451">SettingsLocationTemplate Element</span></span>](#settingslocationtemplate)

-   [<span data-ttu-id="605ce-452">Anhang: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="605ce-452">Appendix: SettingsLocationTemplate.xsd</span></span>](#appendix)

### <a href="" id="xml"></a><span data-ttu-id="605ce-453">XML-Deklaration und Codierungsattribut</span><span class="sxs-lookup"><span data-stu-id="605ce-453">XML Declaration and Encoding Attribute</span></span>

**<span data-ttu-id="605ce-454">Obligatorisch: wahr</span><span class="sxs-lookup"><span data-stu-id="605ce-454">Mandatory: True</span></span>**

**<span data-ttu-id="605ce-455">Typ: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-455">Type: String</span></span>**

<span data-ttu-id="605ce-456">Die XML-Deklaration muss das XML-Version 1,0-Attribut ( &lt; ? XML-Version = "1.0" &gt; ) angeben.</span><span class="sxs-lookup"><span data-stu-id="605ce-456">The XML declaration must specify the XML version 1.0 attribute (&lt;?xml version="1.0"&gt;).</span></span> <span data-ttu-id="605ce-457">Vom UE-V-Generator erstellte Einstellungen für Standort Vorlagen werden in UTF-8-Codierung gespeichert, obwohl die Codierung nicht explizit angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="605ce-457">Settings location templates created by the UE-V Generator are saved in UTF-8 encoding, although the encoding is not explicitly specified.</span></span> <span data-ttu-id="605ce-458">Wir empfehlen, dass Sie das Attribut Encoding = "UTF-8" in dieses Element als bewährte Methode einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="605ce-458">We recommend that you include the encoding="UTF-8" attribute in this element as a best practice.</span></span> <span data-ttu-id="605ce-459">Alle im Lieferumfang des Produkts enthaltenen Vorlagen geben diesen Tag ebenfalls an (Informationen finden Sie in den Dokumenten in%programfiles%\\Microsoft Benutzeroberflächen-Virtualization\\Templates als Referenz).</span><span class="sxs-lookup"><span data-stu-id="605ce-459">All templates included with the product specify this tag as well (see the documents in %ProgramFiles%\\Microsoft User Experience Virtualization\\Templates for reference).</span></span> <span data-ttu-id="605ce-460">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="605ce-460">For example:</span></span>

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace"></a><span data-ttu-id="605ce-461">Namespace und Stamm Element</span><span class="sxs-lookup"><span data-stu-id="605ce-461">Namespace and Root Element</span></span>

**<span data-ttu-id="605ce-462">Obligatorisch: wahr</span><span class="sxs-lookup"><span data-stu-id="605ce-462">Mandatory: True</span></span>**

**<span data-ttu-id="605ce-463">Typ: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-463">Type: String</span></span>**

<span data-ttu-id="605ce-464">UE-V verwendet den https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate Namespace für alle Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="605ce-464">UE-V uses the https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate namespace for all applications.</span></span> <span data-ttu-id="605ce-465">SettingsLocationTemplate ist das Stammelement und enthält alle anderen Elemente.</span><span class="sxs-lookup"><span data-stu-id="605ce-465">SettingsLocationTemplate is the root element and contains all other elements.</span></span> <span data-ttu-id="605ce-466">Verweisen Sie SettingsLocationTemplate in allen Vorlagen mit diesem Tag:</span><span class="sxs-lookup"><span data-stu-id="605ce-466">Reference SettingsLocationTemplate in all templates using this tag:</span></span>

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data"></a><span data-ttu-id="605ce-467">Datentypen</span><span class="sxs-lookup"><span data-stu-id="605ce-467">Data types</span></span>

<span data-ttu-id="605ce-468">Hierbei handelt es sich um die Datentypen für das Anwendungsvorlagen Schema UE-V.</span><span class="sxs-lookup"><span data-stu-id="605ce-468">These are the data types for the UE-V application template schema.</span></span>

<a href="" id="guid"></a><span data-ttu-id="605ce-469">**GUID** GUID beschreibt einen standardmäßigen Standardausdruck für global eindeutigen Bezeichner in der Form "\ \ {\ [a-FA-F0-9 \] {8} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {12} \ \}".</span><span class="sxs-lookup"><span data-stu-id="605ce-469">**GUID** GUID describes a standard globally unique identifier regular expression in the form "\\{\[a-fA-F0-9\]{8}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{12}\\}".</span></span> <span data-ttu-id="605ce-470">Diese wird im Filesetting\\Root\\KnownFolder-Element verwendet, um die Formatierung bekannter Ordner zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="605ce-470">This is used in the Filesetting\\Root\\KnownFolder element to verify the formatting of well-known folders.</span></span>

<a href="" id="filenamestring"></a><span data-ttu-id="605ce-471">**Filenamed** Filenamed bezieht sich auf den Dateinamen eines zu überwachenden Prozesses.</span><span class="sxs-lookup"><span data-stu-id="605ce-471">**FilenameString** FilenameString refers to the file name of a process to be monitored.</span></span> <span data-ttu-id="605ce-472">Die Werte sind durch das Regex-Element \ [^ \ \ \ \ \ \? &lt; &gt; /: \] +, (das heißt, Sie dürfen keine umgekehrten Schrägstriche, Sternchen oder Fragezeichen-Wildcard-Zeichen, das Pipe-Zeichen, das größer-als-oder kleiner-als-Zeichen, Schrägstrich oder Doppelpunktzeichen) enthalten.</span><span class="sxs-lookup"><span data-stu-id="605ce-472">Its values are restricted by the regex \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, (that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon characters).</span></span>

<a href="" id="idstring"></a><span data-ttu-id="605ce-473">**IDString** IDString bezieht sich auf den ID-Wert von Application-Elementen, SettingsLocationTemplate und Common Elements (verwendet, um Anwendungssuiten zu beschreiben, die gemeinsame Einstellungen aufweisen).</span><span class="sxs-lookup"><span data-stu-id="605ce-473">**IDString** IDString refers to the ID value of Application elements, SettingsLocationTemplate, and Common elements (used to describe application suites that share common settings).</span></span> <span data-ttu-id="605ce-474">Sie ist durch denselben Regex-Ausdruck wie filenamed eingeschränkt (\ [^ \ \ \ \ \ \? \ \ \ \* \ \ | &lt; &gt; /:\]+).</span><span class="sxs-lookup"><span data-stu-id="605ce-474">It is restricted by the same regex as FilenameString (\[^\\\\\\?\\\*\\|&lt;&gt;/:\]+).</span></span>

<a href="" id="templateversion"></a><span data-ttu-id="605ce-475">**TemplateVersion** TemplateVersion ist ein ganzzahliger Wert, der zur Beschreibung der Überarbeitung der Vorlage für die Einstellungsposition verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="605ce-475">**TemplateVersion** TemplateVersion is an integer value used to describe the revision of the settings location template.</span></span> <span data-ttu-id="605ce-476">Der Wert kann zwischen 0 und 2147483647 liegen.</span><span class="sxs-lookup"><span data-stu-id="605ce-476">Its value may range from 0 to 2147483647.</span></span>

<a href="" id="empty"></a><span data-ttu-id="605ce-477">**Leer** Empty bezieht sich auf einen NULL-Wert.</span><span class="sxs-lookup"><span data-stu-id="605ce-477">**Empty** Empty refers to a null value.</span></span> <span data-ttu-id="605ce-478">Dieser wird in Process\\ShellProcess verwendet, um anzugeben, dass kein zu überwachenden Prozess vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="605ce-478">This is used in Process\\ShellProcess to indicate that there is no process to monitor.</span></span> <span data-ttu-id="605ce-479">Dieser Wert sollte in keiner Anwendungsvorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="605ce-479">This value should not be used in any application templates.</span></span>

<a href="" id="author"></a><span data-ttu-id="605ce-480">**Autor** Der Datentyp "Autor" ist ein komplexer Typ, der den Autor einer Vorlage identifiziert.</span><span class="sxs-lookup"><span data-stu-id="605ce-480">**Author** The Author data type is a complex type that identifies the author of a template.</span></span> <span data-ttu-id="605ce-481">Sie enthält zwei untergeordnete Elemente: **Name** und **e-Mail**.</span><span class="sxs-lookup"><span data-stu-id="605ce-481">It contains two child elements: **Name** and **Email**.</span></span> <span data-ttu-id="605ce-482">Im Datentyp "Author" ist das Name-Element obligatorisch, während das e-Mail-Element optional ist.</span><span class="sxs-lookup"><span data-stu-id="605ce-482">Within the Author data type, the Name element is mandatory while the Email element is optional.</span></span> <span data-ttu-id="605ce-483">Dieser Typ wird im SettingsLocationTemplate-Element ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="605ce-483">This type is described in more detail under the SettingsLocationTemplate element.</span></span>

<a href="" id="range"></a><span data-ttu-id="605ce-484">**Bereich** Bereich definiert eine ganzzahlige Klasse, die aus zwei untergeordneten Elementen besteht: **Mindest** -und **höchst**Wert.</span><span class="sxs-lookup"><span data-stu-id="605ce-484">**Range** Range defines an integer class consisting of two child elements: **Minimum** and **Maximum**.</span></span> <span data-ttu-id="605ce-485">Dieser Datentyp wird im Datentyp ProcessVersion implementiert.</span><span class="sxs-lookup"><span data-stu-id="605ce-485">This data type is implemented in the ProcessVersion data type.</span></span> <span data-ttu-id="605ce-486">Wenn angegeben, müssen sowohl Mindest-als auch Maximalwerte enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="605ce-486">If specified, both Minimum and Maximum values must be included.</span></span>

<a href="" id="processversion"></a><span data-ttu-id="605ce-487">**ProcessVersion** ProcessVersion definiert einen Typ mit vier untergeordneten Elementen: **Major**, **Minor**, **Build**und **Patch**.</span><span class="sxs-lookup"><span data-stu-id="605ce-487">**ProcessVersion** ProcessVersion defines a type with four child elements: **Major**, **Minor**, **Build**, and **Patch**.</span></span> <span data-ttu-id="605ce-488">Dieser Datentyp wird vom Process-Element zum Auffüllen seiner ProductVersion-und fileversion-Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="605ce-488">This data type is used by the Process element to populate its ProductVersion and FileVersion values.</span></span> <span data-ttu-id="605ce-489">Bei den Daten für diesen Typ handelt es sich um einen Bereichswert.</span><span class="sxs-lookup"><span data-stu-id="605ce-489">The data for this type is a Range value.</span></span> <span data-ttu-id="605ce-490">Das wichtigste untergeordnete Element ist obligatorisch, und die anderen sind optional.</span><span class="sxs-lookup"><span data-stu-id="605ce-490">The Major child element is mandatory and the others are optional.</span></span>

<a href="" id="architecture"></a><span data-ttu-id="605ce-491">**Architektur** Architektur listet zwei mögliche Werte auf: **Win32** und **Win64**.</span><span class="sxs-lookup"><span data-stu-id="605ce-491">**Architecture** Architecture enumerates two possible values: **Win32** and **Win64**.</span></span> <span data-ttu-id="605ce-492">Diese Werte werden verwendet, um die Prozessarchitektur festzulegen.</span><span class="sxs-lookup"><span data-stu-id="605ce-492">These values are used to specify process architecture.</span></span>

<a href="" id="process"></a><span data-ttu-id="605ce-493">**Prozess** Der Prozessdatentyp ist ein Container, der zur Beschreibung der von UE-V zu überwachenden Prozesse dient.</span><span class="sxs-lookup"><span data-stu-id="605ce-493">**Process** The Process data type is a container used to describe processes to be monitored by UE-V.</span></span> <span data-ttu-id="605ce-494">Sie enthält sechs untergeordnete Elemente: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**und **fileversion**.</span><span class="sxs-lookup"><span data-stu-id="605ce-494">It contains six child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="605ce-495">In dieser Tabelle werden die jeweiligen Datentypen der einzelnen Elemente beschrieben:</span><span class="sxs-lookup"><span data-stu-id="605ce-495">This table details each element’s respective data type:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="605ce-496">Element</span><span class="sxs-lookup"><span data-stu-id="605ce-496">Element</span></span></th>
<th align="left"><span data-ttu-id="605ce-497">Datentyp</span><span class="sxs-lookup"><span data-stu-id="605ce-497">Data Type</span></span></th>
<th align="left"><span data-ttu-id="605ce-498">Mandatory</span><span class="sxs-lookup"><span data-stu-id="605ce-498">Mandatory</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-499">Dateiname</span><span class="sxs-lookup"><span data-stu-id="605ce-499">Filename</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-500">Filenamed</span><span class="sxs-lookup"><span data-stu-id="605ce-500">FilenameString</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-501">Wahr</span><span class="sxs-lookup"><span data-stu-id="605ce-501">True</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-502">Architektur</span><span class="sxs-lookup"><span data-stu-id="605ce-502">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-503">Architektur</span><span class="sxs-lookup"><span data-stu-id="605ce-503">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-504">False</span><span class="sxs-lookup"><span data-stu-id="605ce-504">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-505">ProductName</span><span class="sxs-lookup"><span data-stu-id="605ce-505">ProductName</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-506">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-506">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-507">False</span><span class="sxs-lookup"><span data-stu-id="605ce-507">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-508">FileDescription</span><span class="sxs-lookup"><span data-stu-id="605ce-508">FileDescription</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-509">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-509">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-510">False</span><span class="sxs-lookup"><span data-stu-id="605ce-510">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-511">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="605ce-511">ProductVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-512">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="605ce-512">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-513">False</span><span class="sxs-lookup"><span data-stu-id="605ce-513">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-514">File Version</span><span class="sxs-lookup"><span data-stu-id="605ce-514">FileVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-515">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="605ce-515">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-516">False</span><span class="sxs-lookup"><span data-stu-id="605ce-516">False</span></span></p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a><span data-ttu-id="605ce-517">**Prozesse** Der Datentyp "Prozesse" stellt einen Container für eine Sammlung von einem oder mehreren Process-Elementen dar.</span><span class="sxs-lookup"><span data-stu-id="605ce-517">**Processes** The Processes data type represents a container for a collection of one or more Process elements.</span></span> <span data-ttu-id="605ce-518">Im Sequence-Typ Prozesse werden zwei untergeordnete Elemente unterstützt: **Process** und **ShellProcess**.</span><span class="sxs-lookup"><span data-stu-id="605ce-518">Two child elements are supported in the Processes sequence type: **Process** and **ShellProcess**.</span></span> <span data-ttu-id="605ce-519">Process ist ein Element vom Typ Process, und ShellProcess ist vom Datentyp leer.</span><span class="sxs-lookup"><span data-stu-id="605ce-519">Process is an element of type Process and ShellProcess is of data type Empty.</span></span> <span data-ttu-id="605ce-520">Es muss mindestens ein Element in der Sequenz identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="605ce-520">At least one item must be identified in the sequence.</span></span>

<a href="" id="path"></a><span data-ttu-id="605ce-521">**Path** Path wird von RegistrySetting und filesetting verwendet, um auf Registrierungs-und Dateipfade zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="605ce-521">**Path** Path is consumed by RegistrySetting and FileSetting to refer to registry and file paths.</span></span> <span data-ttu-id="605ce-522">Dieses Element unterstützt zwei optionale Attribute: **rekursiv** und **DeleteIfNotFound**.</span><span class="sxs-lookup"><span data-stu-id="605ce-522">This element supports two optional attributes: **Recursive** and **DeleteIfNotFound**.</span></span> <span data-ttu-id="605ce-523">Beide Werte sind auf Default = "false" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="605ce-523">Both values are set to default=”False”.</span></span>

<span data-ttu-id="605ce-524">Rekursiv gibt an, dass der Pfad und alle Unterordner für Datei Einstellungen enthalten sind oder dass alle untergeordneten Registrierungsschlüssel für Registrierungseinstellungen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="605ce-524">Recursive indicates that the path and all subfolders are included for file settings or that all child registry keys are included for registry settings.</span></span> <span data-ttu-id="605ce-525">In beiden Fällen sind alle Elemente auf der aktuellen Ebene in den erfassten Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="605ce-525">In both cases, all items at the current level are included in the data captured.</span></span> <span data-ttu-id="605ce-526">Bei einem filesettings-Objekt sind alle Dateien innerhalb des angegebenen Ordners in den von UE-V erfassten Daten enthalten, aber Ordner sind nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="605ce-526">For a FileSettings object, all files within the specified folder are included in the data captured by UE-V but folders are not included.</span></span> <span data-ttu-id="605ce-527">Bei Registrierungspfaden werden alle Werte im aktuellen Pfad erfasst, aber die untergeordneten Registrierungsschlüssel werden nicht erfasst.</span><span class="sxs-lookup"><span data-stu-id="605ce-527">For registry paths, all values in the current path are captured but child registry keys are not captured.</span></span> <span data-ttu-id="605ce-528">In beiden Fällen sollte darauf geachtet werden, große Datenmengen oder eine große Anzahl von Elementen nicht zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="605ce-528">In both cases, care should be taken to avoid capturing large data sets or large numbers of items.</span></span>

<span data-ttu-id="605ce-529">Das DeleteIfNotFound-Attribut entfernt die Einstellungen aus den Speicherpfad Daten des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="605ce-529">The DeleteIfNotFound attribute removes the setting from the user’s settings storage path data.</span></span> <span data-ttu-id="605ce-530">Dies kann in den Fällen wünschenswert sein, in denen durch das Entfernen dieser Einstellungen aus dem Paket eine große Menge an Speicherplatz auf dem Dateiserver für Settings Storage Path gespart wird.</span><span class="sxs-lookup"><span data-stu-id="605ce-530">This may be desirable in cases where removing these settings from the package will save a large amount of disk space on the settings storage path file server.</span></span>

<a href="" id="filemask"></a><span data-ttu-id="605ce-531">**Filemask** Filemask gibt nur bestimmte Dateitypen für den Ordner an, der durch path definiert ist.</span><span class="sxs-lookup"><span data-stu-id="605ce-531">**FileMask** FileMask specifies only certain file types for the folder that is defined by Path.</span></span> <span data-ttu-id="605ce-532">Path könnte beispielsweise sein, `C:\users\username\files` und die Dateimaske kann `*.txt` nur Textdateien enthalten.</span><span class="sxs-lookup"><span data-stu-id="605ce-532">For example, Path might be `C:\users\username\files` and FileMask could be `*.txt` to include only text files.</span></span>

<a href="" id="registrysetting"></a><span data-ttu-id="605ce-533">**RegistrySetting** RegistrySetting stellt einen Container für Registrierungsschlüssel und-Werte und das zugeordnete gewünschte Verhalten auf Seiten des UE-V-Agents dar.</span><span class="sxs-lookup"><span data-stu-id="605ce-533">**RegistrySetting** RegistrySetting represents a container for registry keys and values and the associated desired behavior on the part of the UE-V Agent.</span></span> <span data-ttu-id="605ce-534">In diesem Typ werden vier untergeordnete Elemente definiert: **path**, **Name**, **Exclude**und eine Sequenz des Werte **Pfads** und- **namens**.</span><span class="sxs-lookup"><span data-stu-id="605ce-534">Four child elements are defined within this type: **Path**, **Name**, **Exclude**, and a sequence of the values **Path** and **Name**.</span></span>

<a href="" id="filesetting"></a><span data-ttu-id="605ce-535">**Filesetting** Filesetting enthält Parameter, die mit Dateien und Dateipfaden verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="605ce-535">**FileSetting** FileSetting contains parameters associated with files and files paths.</span></span> <span data-ttu-id="605ce-536">Es werden vier untergeordnete Elemente definiert: **root**, **path**, **filemask**und **Exclude**.</span><span class="sxs-lookup"><span data-stu-id="605ce-536">Four child elements are defined: **Root**, **Path**, **FileMask**, and **Exclude**.</span></span> <span data-ttu-id="605ce-537">Root ist obligatorisch und die anderen sind optional.</span><span class="sxs-lookup"><span data-stu-id="605ce-537">Root is mandatory and the others are optional.</span></span>

<a href="" id="settings"></a><span data-ttu-id="605ce-538">**Einstellungen** Einstellungen ist ein Container für alle Einstellungen, die für eine bestimmte Vorlage gelten.</span><span class="sxs-lookup"><span data-stu-id="605ce-538">**Settings** Settings is a container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="605ce-539">Sie enthält Instanzen der zuvor beschriebenen Registrierungs-, Datei-, Systemparameter-und benutzerdefinierten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="605ce-539">It contains instances of the Registry, File, SystemParameter, and CustomAction settings described earlier.</span></span> <span data-ttu-id="605ce-540">Darüber hinaus kann Sie auch die folgenden untergeordneten Elemente mit den beschriebenen Verhaltensweisen enthalten:</span><span class="sxs-lookup"><span data-stu-id="605ce-540">In addition, it can also contain the following child elements with behaviors described:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="605ce-541">Element</span><span class="sxs-lookup"><span data-stu-id="605ce-541">Element</span></span></th>
<th align="left"><span data-ttu-id="605ce-542">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="605ce-542">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-543">Asynchrone</span><span class="sxs-lookup"><span data-stu-id="605ce-543">Asynchronous</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-544">Asynchrone Einstellungs Pakete werden angewendet, ohne den Anwendungsstart zu blockieren, damit der Anwendungsstart fortgesetzt wird, während die Einstellungen noch angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="605ce-544">Asynchronous settings packages are applied without blocking the application startup so that the application start proceeds while the settings are still being applied.</span></span> <span data-ttu-id="605ce-545">Dies ist nützlich für Einstellungen, die asynchron angewendet werden können, beispielsweise <code>get/set</code> über eine API, wie SystemParameterSetting.</span><span class="sxs-lookup"><span data-stu-id="605ce-545">This is useful for settings that can be applied asynchronously, such as those <code>get/set</code> through an API, like SystemParameterSetting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-546">PreventOverlappingSynchronization</span><span class="sxs-lookup"><span data-stu-id="605ce-546">PreventOverlappingSynchronization</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-547">Standardmäßig werden in UE-V nur Einstellungen für eine Anwendung gespeichert, wenn die letzte Instanz einer Anwendung, die die Vorlage verwendet, geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="605ce-547">By default, UE-V only saves settings for an application when the last instance of an application using the template is closed.</span></span> <span data-ttu-id="605ce-548">Wenn dieses Element auf "false" festgelegt ist, exportiert UE-V die Einstellungen selbst dann, wenn andere Instanzen einer Anwendung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="605ce-548">When this element is set to ‘false’, UE-V exports the settings even if other instances of an application are running.</span></span> <span data-ttu-id="605ce-549">Geeignete Vorlagen – diejenigen, die einen allgemeinen Element Abschnitt enthalten –, die mit UE-V ausgeliefert werden, verwenden dieses Flag, um freigegebene Einstellungen so zu aktivieren, dass Sie immer beim Schließen der Anwendung exportiert werden, während anwendungsspezifische Einstellungen vor dem Export verhindert werden, bis die letzte Instanz geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="605ce-549">Suited templates – those that include a Common element section– that are shipped with UE-V use this flag to enable shared settings to always export on application close, while preventing application-specific settings from exporting until the last instance is closed.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name"></a><span data-ttu-id="605ce-550">Name-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-550">Name Element</span></span>

**<span data-ttu-id="605ce-551">Obligatorisch: wahr</span><span class="sxs-lookup"><span data-stu-id="605ce-551">Mandatory: True</span></span>**

**<span data-ttu-id="605ce-552">Typ: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-552">Type: String</span></span>**

<span data-ttu-id="605ce-553">Name gibt einen eindeutigen Namen für die Einstellungs Speicherort Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="605ce-553">Name specifies a unique name for the settings location template.</span></span> <span data-ttu-id="605ce-554">Diese Funktion wird für Anzeigezwecke verwendet, wenn Sie in WMI, PowerShell, Ereignisanzeige und Debug-Protokollen auf die Vorlage verweisen.</span><span class="sxs-lookup"><span data-stu-id="605ce-554">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="605ce-555">Im Allgemeinen sollten Sie nicht auf Versionsinformationen verweisen, da dies vom ProductVersion-Element abweichen kann.</span><span class="sxs-lookup"><span data-stu-id="605ce-555">In general, avoid referencing version information, as this can be objected from the ProductVersion element.</span></span> <span data-ttu-id="605ce-556">Geben Sie beispielsweise `<Name>My Application</Name>` anstelle ein `<Name>My Application 1.1</Name>` .</span><span class="sxs-lookup"><span data-stu-id="605ce-556">For example, specify `<Name>My Application</Name>` rather than `<Name>My Application 1.1</Name>`.</span></span>

<span data-ttu-id="605ce-557">**Hinweis**  UE-V verweist nicht auf externe DTDs, daher ist es nicht möglich, benannte Entitäten in einer Einstellungen-Speicherort Vorlage zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="605ce-557">**Note** UE-V does not reference external DTDs, so it is not possible to use named entities in a settings location template.</span></span> <span data-ttu-id="605ce-558">Verwenden Sie beispielsweise nicht, &reg; um auf das eingetragene Markenzeichen® zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="605ce-558">For example, do not use &reg; to refer to the registered trade mark sign ®.</span></span> <span data-ttu-id="605ce-559">Verwenden Sie stattdessen kanonische nummerierte Bezüge, um diese Typen von Sonderzeichen einzubeziehen, beispielsweise & \ #174 für das® Zeichen.</span><span class="sxs-lookup"><span data-stu-id="605ce-559">Instead, use canonical numbered references to include these types of special characters, for example, &\#174 for the ® character.</span></span> <span data-ttu-id="605ce-560">Diese Regel gilt für alle Zeichenfolgenwerte in diesem Dokument.</span><span class="sxs-lookup"><span data-stu-id="605ce-560">This rule applies to all string values in this document.</span></span>

<span data-ttu-id="605ce-561"><http://www.w3.org/TR/xhtml1/dtds.html>Eine vollständige Liste der Zeichenentitäten finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="605ce-561">See <http://www.w3.org/TR/xhtml1/dtds.html> for a complete list of character entities.</span></span> <span data-ttu-id="605ce-562">UTF-8-codierte Dokumente enthalten möglicherweise die Unicode-Zeichen direkt.</span><span class="sxs-lookup"><span data-stu-id="605ce-562">UTF-8-encoded documents may include the Unicode characters directly.</span></span> <span data-ttu-id="605ce-563">Beim Speichern von Vorlagen über den UE-V-Generator werden Zeichenentitäten automatisch in ihre Unicode-Darstellungen konvertiert.</span><span class="sxs-lookup"><span data-stu-id="605ce-563">Saving templates through the UE-V Generator converts character entities to their Unicode representations automatically.</span></span>

 

### <a href="" id="id"></a><span data-ttu-id="605ce-564">ID-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-564">ID Element</span></span>

**<span data-ttu-id="605ce-565">Obligatorisch: wahr</span><span class="sxs-lookup"><span data-stu-id="605ce-565">Mandatory: True</span></span>**

**<span data-ttu-id="605ce-566">Typ: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-566">Type: String</span></span>**

<span data-ttu-id="605ce-567">ID füllt einen eindeutigen Bezeichner für eine bestimmte Vorlage auf.</span><span class="sxs-lookup"><span data-stu-id="605ce-567">ID populates a unique identifier for a particular template.</span></span> <span data-ttu-id="605ce-568">Dieses Tag wird zur primären Kennung, mit der der UE-V-Agent zur Laufzeit auf die Vorlage verweist (Beispiel: Anzeigen der Ausgabe der PowerShell-Cmdlets "Get-UevTemplate" und "Get-UevTemplateProgram").</span><span class="sxs-lookup"><span data-stu-id="605ce-568">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime (for example, see the output of the Get-UevTemplate and Get-UevTemplateProgram PowerShell cmdlets).</span></span> <span data-ttu-id="605ce-569">Nach Konvention sollte dieses Tag keine Leerzeichen enthalten, was das Skripting vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="605ce-569">By convention, this tag should not contain any spaces, which simplifies scripting.</span></span> <span data-ttu-id="605ce-570">In diesem Element sollten Versionsnummern von Anwendungen angegeben werden, um eine einfache Identifizierung der Vorlage zu ermöglichen, beispielsweise `<ID>MicrosoftCalculator6</ID>` oder `<ID>MicrosoftOffice2010Win64</ID>` .</span><span class="sxs-lookup"><span data-stu-id="605ce-570">Version numbers of applications should be specified in this element to allow for easy identification of the template, such as `<ID>MicrosoftCalculator6</ID>` or `<ID>MicrosoftOffice2010Win64</ID>`.</span></span>

### <a href="" id="version"></a><span data-ttu-id="605ce-571">Version-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-571">Version Element</span></span>

**<span data-ttu-id="605ce-572">Obligatorisch: wahr</span><span class="sxs-lookup"><span data-stu-id="605ce-572">Mandatory: True</span></span>**

**<span data-ttu-id="605ce-573">Typ: Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="605ce-573">Type: Integer</span></span>**

**<span data-ttu-id="605ce-574">Minimaler Wert: 0</span><span class="sxs-lookup"><span data-stu-id="605ce-574">Minimum Value: 0</span></span>**

**<span data-ttu-id="605ce-575">Maximaler Wert: 2147483647</span><span class="sxs-lookup"><span data-stu-id="605ce-575">Maximum Value: 2147483647</span></span>**

<span data-ttu-id="605ce-576">Version identifiziert die Version der Vorlage für die Einstellungsposition für die administrative Nachverfolgung von Änderungen.</span><span class="sxs-lookup"><span data-stu-id="605ce-576">Version identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="605ce-577">Der UE-V-Generator erhöht diese Zahl automatisch um eins, wenn die Vorlage gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="605ce-577">The UE-V Generator automatically increments this number by one each time the template is saved.</span></span> <span data-ttu-id="605ce-578">Beachten Sie, dass dieses Feld eine ganze Zahl Ganzzahl sein muss. Gebrochene Werte, beispielsweise `<Version>2.5</Version>` sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="605ce-578">Notice that this field must be a whole number integer; fractional values, such as `<Version>2.5</Version>` are not allowed.</span></span>

<span data-ttu-id="605ce-579">**Hinweis:** Sie können Notizen zu Versionsänderungen mithilfe von XML-Kommentar Tags speichern `<!-- -->` , beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="605ce-579">**Hint:** You can save notes about version changes using XML comment tags `<!-- -->`, for example:</span></span>

```xml
<!--
    Version History

    Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
    Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
    Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
    Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
  -->
<Version>4</Version>
```

<span data-ttu-id="605ce-580">**Wichtig**  Dieser Wert wird abgefragt, um zu ermitteln, ob eine neue Version einer Vorlage in diesen Fällen auf eine vorhandene Vorlage angewendet werden soll:</span><span class="sxs-lookup"><span data-stu-id="605ce-580">**Important** This value is queried to determine if a new version of a template should be applied to an existing template in these instances:</span></span>

-   <span data-ttu-id="605ce-581">Wenn der automatische Aktualisierungsvorgang der geplanten Vorlage ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="605ce-581">When the scheduled Template Auto Update task executes</span></span>

-   <span data-ttu-id="605ce-582">Wenn das PowerShell-Cmdlet "Update-UevTemplate" ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="605ce-582">When the Update-UevTemplate PowerShell cmdlet is executed</span></span>

-   <span data-ttu-id="605ce-583">Wenn die microsoft\\uev: SettingsLocationTemplate-Update Methode über WMI aufgerufen wird</span><span class="sxs-lookup"><span data-stu-id="605ce-583">When the microsoft\\uev:SettingsLocationTemplate Update method is called through WMI</span></span>

 

### <a href="" id="author"></a><span data-ttu-id="605ce-584">Author-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-584">Author Element</span></span>

**<span data-ttu-id="605ce-585">Obligatorisch: falsch</span><span class="sxs-lookup"><span data-stu-id="605ce-585">Mandatory: False</span></span>**

**<span data-ttu-id="605ce-586">Typ: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-586">Type: String</span></span>**

<span data-ttu-id="605ce-587">Autor identifiziert den Ersteller der Vorlage für die Einstellungsposition.</span><span class="sxs-lookup"><span data-stu-id="605ce-587">Author identifies the creator of the settings location template.</span></span> <span data-ttu-id="605ce-588">Zwei optionale untergeordnete Elemente werden unterstützt: **Name** und **e-Mail**.</span><span class="sxs-lookup"><span data-stu-id="605ce-588">Two optional child elements are supported: **Name** and **Email**.</span></span> <span data-ttu-id="605ce-589">Beide Attribute sind optional, aber wenn das untergeordnete e-Mail-Element angegeben ist, muss es vom Name-Element begleitet werden.</span><span class="sxs-lookup"><span data-stu-id="605ce-589">Both attributes are optional, but, if the Email child element is specified, it must be accompanied by the Name element.</span></span> <span data-ttu-id="605ce-590">Der Autor bezieht sich auf den vollständigen Namen des Kontakts für die Vorlage "Settings Location", und e-Mail sollte auf eine e-Mail-Adresse für den Autor verweisen.</span><span class="sxs-lookup"><span data-stu-id="605ce-590">Author refers to the full name of the contact for the settings location template, and email should refer to an email address for the author.</span></span> <span data-ttu-id="605ce-591">Wir empfehlen, dass Sie diese Informationen in öffentlich veröffentlichte Vorlagen einbeziehen, beispielsweise im [Vorlagenkatalog UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span><span class="sxs-lookup"><span data-stu-id="605ce-591">We recommend that you include this information in templates published publicly, for example, on the [UE-V Template Gallery](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span></span>

### <a href="" id="processes"></a><span data-ttu-id="605ce-592">Prozesse und Prozess Element</span><span class="sxs-lookup"><span data-stu-id="605ce-592">Processes and Process Element</span></span>

**<span data-ttu-id="605ce-593">Obligatorisch: wahr</span><span class="sxs-lookup"><span data-stu-id="605ce-593">Mandatory: True</span></span>**

**<span data-ttu-id="605ce-594">Typ: Element</span><span class="sxs-lookup"><span data-stu-id="605ce-594">Type: Element</span></span>**

<span data-ttu-id="605ce-595">Prozesse enthält mindestens ein `<Process>` Element, das wiederum die folgenden untergeordneten Elemente enthält: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**und **fileversion**.</span><span class="sxs-lookup"><span data-stu-id="605ce-595">Processes contains at least one `<Process>` element, which in turn contains the following child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="605ce-596">Das untergeordnete FileName-Element ist obligatorisch, die anderen sind optional.</span><span class="sxs-lookup"><span data-stu-id="605ce-596">The Filename child element is mandatory and the others are optional.</span></span> <span data-ttu-id="605ce-597">Ein vollständig aufgefülltes Element enthält Tags ähnlich wie in diesem Beispiel:</span><span class="sxs-lookup"><span data-stu-id="605ce-597">A fully populated element contains tags similar to this example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### <span data-ttu-id="605ce-598">Dateiname</span><span class="sxs-lookup"><span data-stu-id="605ce-598">Filename</span></span>

**<span data-ttu-id="605ce-599">Obligatorisch: wahr</span><span class="sxs-lookup"><span data-stu-id="605ce-599">Mandatory: True</span></span>**

**<span data-ttu-id="605ce-600">Typ: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-600">Type: String</span></span>**

<span data-ttu-id="605ce-601">Filename bezieht sich auf den tatsächlichen Dateinamen der ausführbaren Datei, wie Sie im Dateisystem angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="605ce-601">Filename refers to the actual file name of the executable as it appears in the file system.</span></span> <span data-ttu-id="605ce-602">Dieses Element gibt das primäre Kriterium an, mit dem UE-V auswerten soll, ob eine Vorlage für einen Prozess gilt oder nicht.</span><span class="sxs-lookup"><span data-stu-id="605ce-602">This element specifies the primary criterion that UE-V uses to evaluate whether a template applies to a process or not.</span></span> <span data-ttu-id="605ce-603">Dieses Element muss in der XML-Vorlage für die Einstellungsposition angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="605ce-603">This element must be specified in the settings location template XML.</span></span>

<span data-ttu-id="605ce-604">Gültige Dateinamen dürfen nicht mit dem regulären Ausdruck \ [^ \ \ \ \ \ \? \ \ \ \* \ \ | &lt; &gt; /: \] +, das heißt, Sie dürfen keine umgekehrten Schrägstriche, Sternchen-oder Fragezeichen-Wildcards, das Pipe-Zeichen, das größer-als-oder kleiner-als-Zeichen, den Schrägstrich oder den Doppelpunkt enthalten (\ \?</span><span class="sxs-lookup"><span data-stu-id="605ce-604">Valid filenames must not match the regular expression \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon (the \\ ?</span></span> <span data-ttu-id="605ce-605">\* | &lt; &gt; /oder: Zeichen.).</span><span class="sxs-lookup"><span data-stu-id="605ce-605">\* | &lt; &gt; / or : characters.).</span></span>

<span data-ttu-id="605ce-606">**Hinweis:** Um eine Zeichenfolge für diesen Regex zu testen, verwenden Sie ein PowerShell-Befehlsfenster, und ersetzen Sie den Namen der ausführbaren Datei für **YourFileName**:</span><span class="sxs-lookup"><span data-stu-id="605ce-606">**Hint:** To test a string against this regex, use a PowerShell command window and substitute your executable’s name for **YourFileName**:</span></span>

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

<span data-ttu-id="605ce-607">Der Wert **true** gibt an, dass die Zeichenfolge ungültige Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="605ce-607">A value of **True** indicates that the string contains illegal characters.</span></span> <span data-ttu-id="605ce-608">Im folgenden finden Sie einige Beispiele für ungültige Werte:</span><span class="sxs-lookup"><span data-stu-id="605ce-608">Here are some examples of illegal values:</span></span>

-   <span data-ttu-id="605ce-609">\\\\server\\share\\program.exe</span><span class="sxs-lookup"><span data-stu-id="605ce-609">\\\\server\\share\\program.exe</span></span>

-   <span data-ttu-id="605ce-610">Programm \ \*. exe</span><span class="sxs-lookup"><span data-stu-id="605ce-610">Program\*.exe</span></span>

-   <span data-ttu-id="605ce-611">Pro? ram.exe</span><span class="sxs-lookup"><span data-stu-id="605ce-611">Pro?ram.exe</span></span>

-   <span data-ttu-id="605ce-612">Programm &lt; 1 &gt; . exe</span><span class="sxs-lookup"><span data-stu-id="605ce-612">Program&lt;1&gt;.exe</span></span>

<span data-ttu-id="605ce-613">**Hinweis**  Der UE-V-Generator codiert das größer-als-und das kleiner-als-Zeichen &gt; &lt; .</span><span class="sxs-lookup"><span data-stu-id="605ce-613">**Note** The UE-V Generator encodes the greater than and less than characters as &gt; and &lt; respectively.</span></span>

 

<span data-ttu-id="605ce-614">In seltenen Fällen enthält der FileName-Wert nicht unbedingt die Erweiterung ". exe", sollte aber als Teil des Werts angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="605ce-614">In rare circumstances, the FileName value will not necessarily include the .exe extension, but it should be specified as part of the value.</span></span> <span data-ttu-id="605ce-615">Beispielsweise `<Filename>MyApplictication.exe</Filename>` sollte angegeben werden, anstatt `<Filename>MyApplictication</Filename>` .</span><span class="sxs-lookup"><span data-stu-id="605ce-615">For example, `<Filename>MyApplictication.exe</Filename>` should be specified instead of `<Filename>MyApplictication</Filename>`.</span></span> <span data-ttu-id="605ce-616">Im zweiten Beispiel wird die Vorlage nicht auf den Prozess angewendet, wenn der tatsächliche Name der ausführbaren Datei "MyApplication.exe" lautet.</span><span class="sxs-lookup"><span data-stu-id="605ce-616">The second example will not apply the template to the process if the actual name of the executable file is “MyApplication.exe”.</span></span>

### <span data-ttu-id="605ce-617">Architektur</span><span class="sxs-lookup"><span data-stu-id="605ce-617">Architecture</span></span>

**<span data-ttu-id="605ce-618">Obligatorisch: falsch</span><span class="sxs-lookup"><span data-stu-id="605ce-618">Mandatory: False</span></span>**

**<span data-ttu-id="605ce-619">Typ: Architektur (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="605ce-619">Type: Architecture (String)</span></span>**

<span data-ttu-id="605ce-620">Architektur bezieht sich auf die Prozessorarchitektur, für die die ausführbare Ziel Datei kompiliert wurde.</span><span class="sxs-lookup"><span data-stu-id="605ce-620">Architecture refers to the processor architecture for which the target executable was compiled.</span></span> <span data-ttu-id="605ce-621">Gültige Werte sind Win32 für 32-Bit-Anwendungen oder win64 für 64-Bit-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="605ce-621">Valid values are Win32 for 32-bit applications or Win64 for 64-bit applications.</span></span> <span data-ttu-id="605ce-622">Sofern vorhanden, schränkt dieses Tag die Anwendbarkeit der Vorlage "Settings Location" auf eine bestimmte Anwendungsarchitektur ein.</span><span class="sxs-lookup"><span data-stu-id="605ce-622">If present, this tag limits the applicability of the settings location template to a particular application architecture.</span></span> <span data-ttu-id="605ce-623">Ein Beispiel hierfür finden Sie unter Vergleich der%programfiles%\\Microsoft-Benutzeroberflächen-Virtualization\\templates\\ MicrosoftOffice2010Win32.xml und MicrosoftOffice2010Win64.xml Dateien, die in UE-V enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="605ce-623">For an example of this, compare the %ProgramFiles%\\Microsoft User Experience Virtualization\\templates\\ MicrosoftOffice2010Win32.xml and MicrosoftOffice2010Win64.xml files included with UE-V.</span></span> <span data-ttu-id="605ce-624">Dies ist hilfreich, wenn relative Pfade zwischen unterschiedlichen Versionen einer ausführbaren Datei geändert werden oder wenn Einstellungen hinzugefügt oder entfernt wurden, wenn Sie von einer Prozessorarchitektur zu einer anderen wechseln.</span><span class="sxs-lookup"><span data-stu-id="605ce-624">This is useful when relative paths change between different versions of an executable or if settings have been added or removed when moving from one processor architecture to another.</span></span>

<span data-ttu-id="605ce-625">Wenn dieses Element nicht vorhanden ist, ignoriert die Vorlage "Einstellungen" die Architektur des Prozesses und bezieht sich auf 32-und 64-Bit-Prozesse, wenn der Dateiname und andere Attribute angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="605ce-625">If this element is absent, the settings location template ignores the process’ architecture and applies to both 32 and 64-bit processes if the file name and other attributes apply.</span></span>

<span data-ttu-id="605ce-626">**Hinweis**  UE-V unterstützt keine ARM-Prozessoren in dieser Version.</span><span class="sxs-lookup"><span data-stu-id="605ce-626">**Note** UE-V does not support ARM processors in this version.</span></span>

 

### <span data-ttu-id="605ce-627">ProductName</span><span class="sxs-lookup"><span data-stu-id="605ce-627">ProductName</span></span>

**<span data-ttu-id="605ce-628">Obligatorisch: falsch</span><span class="sxs-lookup"><span data-stu-id="605ce-628">Mandatory: False</span></span>**

**<span data-ttu-id="605ce-629">Typ: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-629">Type: String</span></span>**

<span data-ttu-id="605ce-630">ProductName ist ein optionales Element, das verwendet wird, um ein Produkt für administrative Zwecke oder Berichte zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="605ce-630">ProductName is an optional element used to identify a product for administrative purposes or reporting.</span></span> <span data-ttu-id="605ce-631">ProductName unterscheidet sich von filename dadurch, dass für seinen Wert keine regulären Ausdruckseinschränkungen gelten.</span><span class="sxs-lookup"><span data-stu-id="605ce-631">ProductName differs from Filename in that there are no regular expression restrictions on its value.</span></span> <span data-ttu-id="605ce-632">Auf diese Weise können Beschreibungen eines Prozesses leichter verstanden werden, bei denen der Name der ausführbaren Datei möglicherweise nicht offensichtlich ist.</span><span class="sxs-lookup"><span data-stu-id="605ce-632">This allows for more easily understood descriptions of a process where the executable name may not be obvious.</span></span> <span data-ttu-id="605ce-633">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="605ce-633">For example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### <span data-ttu-id="605ce-634">FileDescription</span><span class="sxs-lookup"><span data-stu-id="605ce-634">FileDescription</span></span>

**<span data-ttu-id="605ce-635">Obligatorisch: falsch</span><span class="sxs-lookup"><span data-stu-id="605ce-635">Mandatory: False</span></span>**

**<span data-ttu-id="605ce-636">Typ: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-636">Type: String</span></span>**

<span data-ttu-id="605ce-637">FileDescription ist ein optionales Tag, das eine administrative Beschreibung der ausführbaren Datei ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="605ce-637">FileDescription is an optional tag that allows for an administrative description of the executable file.</span></span> <span data-ttu-id="605ce-638">Hierbei handelt es sich um ein kostenloses Textfeld, das bei der Unterscheidung mehrerer ausführbarer Dateien innerhalb eines Softwarepakets hilfreich sein kann, wenn die Funktion der ausführbaren Datei identifiziert werden muss.</span><span class="sxs-lookup"><span data-stu-id="605ce-638">This is a free text field and can be useful in distinguishing multiple executables within a software package where there is a need to identify the function of the executable.</span></span>

<span data-ttu-id="605ce-639">In einer geeigneten Anwendung kann es beispielsweise hilfreich sein, die Funktion von zwei ausführbaren Dateien (MyApplication.exe und MyApplicationHelper.exe) zu informieren, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="605ce-639">For example, in a suited application, it might be useful to provide reminders about the function of two executables (MyApplication.exe and MyApplicationHelper.exe), as shown here:</span></span>

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### <span data-ttu-id="605ce-640">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="605ce-640">ProductVersion</span></span>

**<span data-ttu-id="605ce-641">Obligatorisch: falsch</span><span class="sxs-lookup"><span data-stu-id="605ce-641">Mandatory: False</span></span>**

**<span data-ttu-id="605ce-642">Typ: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-642">Type: String</span></span>**

<span data-ttu-id="605ce-643">ProductVersion bezieht sich auf die Haupt-und Nebenversionen einer Datei sowie auf eine Build-und Patchebene.</span><span class="sxs-lookup"><span data-stu-id="605ce-643">ProductVersion refers to the major and minor product versions of a file, as well as a build and patch level.</span></span> <span data-ttu-id="605ce-644">ProductVersion ist ein optionales Element, aber wenn angegeben, muss es mindestens das wichtigste untergeordnete Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="605ce-644">ProductVersion is an optional element, but if specified, it must contain at least the Major child element.</span></span> <span data-ttu-id="605ce-645">Der Wert muss einen Bereich in der Form mindestens = "x" Maximum = "y" ausdrücken, wobei X und Y ganze Zahlen sind.</span><span class="sxs-lookup"><span data-stu-id="605ce-645">The value must express a range in the form Minimum="X" Maximum="Y" where X and Y are integers.</span></span> <span data-ttu-id="605ce-646">Die Mindest-und Höchstwerte können identisch sein.</span><span class="sxs-lookup"><span data-stu-id="605ce-646">The Minimum and Maximum values can be identical.</span></span>

<span data-ttu-id="605ce-647">Die Elemente "Produkt" und "Dateiversion" werden möglicherweise nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="605ce-647">The product and file version elements may be left unspecified.</span></span> <span data-ttu-id="605ce-648">Dadurch wird die Vorlage "versionsunabhängig", was bedeutet, dass die Vorlage auf alle Versionen der angegebenen ausführbaren Datei angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="605ce-648">Doing so makes the template “version agnostic”, meaning that the template will apply to all versions of the specified executable.</span></span>

**<span data-ttu-id="605ce-649">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="605ce-649">Example 1:</span></span>**

<span data-ttu-id="605ce-650">Produktversion: 1,0, die im UE-V-Generator angegeben wird, erzeugt den folgenden XML-Code:</span><span class="sxs-lookup"><span data-stu-id="605ce-650">Product version: 1.0 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**<span data-ttu-id="605ce-651">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="605ce-651">Example 2:</span></span>**

<span data-ttu-id="605ce-652">Dateiversion: im UE-V-Generator angegebene 5.0.2.1000 erzeugt den folgenden XML-Code:</span><span class="sxs-lookup"><span data-stu-id="605ce-652">File version: 5.0.2.1000 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**<span data-ttu-id="605ce-653">Falsches Beispiel 1 – unvollständiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="605ce-653">Incorrect Example 1 – incomplete range:</span></span>**

<span data-ttu-id="605ce-654">Es ist nur das kleinste Attribut vorhanden.</span><span class="sxs-lookup"><span data-stu-id="605ce-654">Only the Minimum attribute is present.</span></span> <span data-ttu-id="605ce-655">Maximum muss auch in einem Bereich enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="605ce-655">Maximum must be included in a range as well.</span></span>

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**<span data-ttu-id="605ce-656">Falsches Beispiel 2 – Moll ohne Hauptelement angegeben:</span><span class="sxs-lookup"><span data-stu-id="605ce-656">Incorrect Example 2 – Minor specified without Major element:</span></span>**

<span data-ttu-id="605ce-657">Nur das nebengeordnete Element ist vorhanden.</span><span class="sxs-lookup"><span data-stu-id="605ce-657">Only the Minor element is present.</span></span> <span data-ttu-id="605ce-658">Major muss ebenfalls enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="605ce-658">Major must be included as well.</span></span>

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### <span data-ttu-id="605ce-659">File Version</span><span class="sxs-lookup"><span data-stu-id="605ce-659">FileVersion</span></span>

**<span data-ttu-id="605ce-660">Obligatorisch: falsch</span><span class="sxs-lookup"><span data-stu-id="605ce-660">Mandatory: False</span></span>**

**<span data-ttu-id="605ce-661">Typ: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="605ce-661">Type: String</span></span>**

<span data-ttu-id="605ce-662">Fileversion unterscheidet zwischen der Veröffentlichungsversion einer veröffentlichten Anwendung und den internen Builddaten einer ausführbaren Komponente.</span><span class="sxs-lookup"><span data-stu-id="605ce-662">FileVersion differentiates between the release version of a published application and the internal build details of a component executable.</span></span> <span data-ttu-id="605ce-663">Bei den meisten kommerziellen Anwendungen sind diese Nummern identisch.</span><span class="sxs-lookup"><span data-stu-id="605ce-663">For the majority of commercial applications, these numbers are identical.</span></span> <span data-ttu-id="605ce-664">Wenn Sie unterschiedlich sind, gibt die Produktversion einer Datei eine generische Versionskennung einer Datei an, während die Dateiversion einen bestimmten Build einer Datei angibt (wie im Fall eines Hotfix oder Updates).</span><span class="sxs-lookup"><span data-stu-id="605ce-664">Where they vary, the product version of a file indicates a generic version identification of a file, while file version indicates a specific build of a file (as in the case of a hotfix or update).</span></span> <span data-ttu-id="605ce-665">Dadurch werden Dateien eindeutig identifiziert, ohne die Erkennungslogik zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="605ce-665">This uniquely identifies files without breaking detection logic.</span></span>

<span data-ttu-id="605ce-666">Wenn Sie die Produktversion und die Dateiversion einer bestimmten ausführbaren Datei ermitteln möchten, klicken Sie mit der rechten Maustaste auf die Datei in Windows-Explorer, wählen Sie Eigenschaften aus, und klicken Sie dann auf die Registerkarte Details.</span><span class="sxs-lookup"><span data-stu-id="605ce-666">To determine the product version and file version of a particular executable, right-click on the file in Windows Explorer, select Properties, then click on the Details tab.</span></span>

<span data-ttu-id="605ce-667">Das Einfügen eines fileversion-Elements für eine Anwendung ermöglicht eine genauere Feintuning-Erkennungslogik, ist für die meisten Anwendungen jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="605ce-667">Including a FileVersion element for an application allows for more granular fine-tuning detection logic, but is not necessary for most applications.</span></span> <span data-ttu-id="605ce-668">Die ProductVersion-Elementeinstellungen werden zuerst überprüft, und dann wird die Dateiversion aktiviert.</span><span class="sxs-lookup"><span data-stu-id="605ce-668">The ProductVersion element settings are checked first, and then FileVersion is checked.</span></span> <span data-ttu-id="605ce-669">Die restriktivere Einstellung wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="605ce-669">The more restrictive setting will apply.</span></span>

<span data-ttu-id="605ce-670">Die untergeordneten Elemente und Syntaxregeln für fileversion sind mit denen von ProductVersion identisch.</span><span class="sxs-lookup"><span data-stu-id="605ce-670">The child elements and syntax rules for FileVersion are identical to those of ProductVersion.</span></span>

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application"></a><span data-ttu-id="605ce-671">Application-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-671">Application Element</span></span>

<span data-ttu-id="605ce-672">Application ist ein Container für Einstellungen, die für eine bestimmte Anwendung gelten.</span><span class="sxs-lookup"><span data-stu-id="605ce-672">Application is a container for settings that apply to a particular application.</span></span> <span data-ttu-id="605ce-673">Es handelt sich um eine Sammlung der folgenden Felder/Typen.</span><span class="sxs-lookup"><span data-stu-id="605ce-673">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="605ce-674">Feld/Typ</span><span class="sxs-lookup"><span data-stu-id="605ce-674">Field/Type</span></span></th>
<th align="left"><span data-ttu-id="605ce-675">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="605ce-675">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-676">Name</span><span class="sxs-lookup"><span data-stu-id="605ce-676">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-677">Gibt einen eindeutigen Namen für die Vorlage "Settings Location" an.</span><span class="sxs-lookup"><span data-stu-id="605ce-677">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="605ce-678">Diese Funktion wird für Anzeigezwecke verwendet, wenn Sie in WMI, PowerShell, Ereignisanzeige und Debug-Protokollen auf die Vorlage verweisen.</span><span class="sxs-lookup"><span data-stu-id="605ce-678">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="605ce-679">Weitere Informationen finden Sie unter <a href="#name" data-raw-source="[Name](#name)"> Name </a> .</span><span class="sxs-lookup"><span data-stu-id="605ce-679">For more information, see <a href="#name" data-raw-source="[Name](#name)">Name</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-680">ID</span><span class="sxs-lookup"><span data-stu-id="605ce-680">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-681">Füllt einen eindeutigen Bezeichner für eine bestimmte Vorlage auf.</span><span class="sxs-lookup"><span data-stu-id="605ce-681">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="605ce-682">Dieses Tag wird zur primären Kennung, mit der der UE-V-Agent zur Laufzeit auf die Vorlage verweist.</span><span class="sxs-lookup"><span data-stu-id="605ce-682">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="605ce-683">Weitere Informationen finden Sie unter <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="605ce-683">For more information, see <a href="#id" data-raw-source="[ID](#id)">ID</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-684">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="605ce-684">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-685">Eine optionale Beschreibung der Vorlage.</span><span class="sxs-lookup"><span data-stu-id="605ce-685">An optional description of the template.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-686">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="605ce-686">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-687">Ein optionaler Name, der auf der Benutzeroberfläche angezeigt wird und von einem Gebietsschema der Sprache lokalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="605ce-687">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-688">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="605ce-688">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-689">Eine optionale Vorlagenbeschreibung, die von einem Sprachgebietsschema lokalisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="605ce-689">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-690">Version</span><span class="sxs-lookup"><span data-stu-id="605ce-690">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-691">Identifiziert die Version der Vorlage für die Einstellungsposition für die administrative Nachverfolgung von Änderungen.</span><span class="sxs-lookup"><span data-stu-id="605ce-691">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="605ce-692">Weitere Informationen finden Sie unter <a href="#version" data-raw-source="[Version](#version)"> Version </a> .</span><span class="sxs-lookup"><span data-stu-id="605ce-692">For more information, see <a href="#version" data-raw-source="[Version](#version)">Version</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-693">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="605ce-693">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-694">Steuert, ob diese Vorlage in Verbindung mit einem Microsoft-Konto aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="605ce-694">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="605ce-695">Wenn die Synchronisierung von MSA für einen Benutzer auf einem Computer aktiviert ist, wird diese Vorlage automatisch deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="605ce-695">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-696">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="605ce-696">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-697">Ähnlich wie MSA steuert dies, ob diese Vorlage in Verbindung mit Office365 aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="605ce-697">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="605ce-698">Wenn Office 365 zum Synchronisieren von Einstellungen verwendet wird, wird diese Vorlage automatisch deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="605ce-698">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-699">Prozesse</span><span class="sxs-lookup"><span data-stu-id="605ce-699">Processes</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-700">Ein Container für eine Sammlung von einem oder mehreren Process-Elementen.</span><span class="sxs-lookup"><span data-stu-id="605ce-700">A container for a collection of one or more Process elements.</span></span> <span data-ttu-id="605ce-701">Weitere Informationen finden Sie unter <a href="#processes" data-raw-source="[Processes](#processes)"> Prozesse </a> .</span><span class="sxs-lookup"><span data-stu-id="605ce-701">For more information, see <a href="#processes" data-raw-source="[Processes](#processes)">Processes</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-702">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="605ce-702">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-703">Ein Container für alle Einstellungen, die für eine bestimmte Vorlage gelten.</span><span class="sxs-lookup"><span data-stu-id="605ce-703">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="605ce-704">Sie enthält Instanzen der Registrierungs-, Datei-, Systemparameter-und benutzerdefinierten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="605ce-704">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="605ce-705">Weitere Informationen finden Sie unter <strong> Einstellungen </strong> in <a href="#data" data-raw-source="[Data types](#data)"> Datentypen </a> .</span><span class="sxs-lookup"><span data-stu-id="605ce-705">For more information, see <strong>Settings</strong> in <a href="#data" data-raw-source="[Data types](#data)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common"></a><span data-ttu-id="605ce-706">Common-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-706">Common Element</span></span>

<span data-ttu-id="605ce-707">Common ist mit einem Application-Element vergleichbar, wird aber immer mit zwei oder mehr Anwendungselementen verknüpft.</span><span class="sxs-lookup"><span data-stu-id="605ce-707">Common is similar to an Application element, but it is always associated with two or more Application elements.</span></span> <span data-ttu-id="605ce-708">Der allgemeine Abschnitt stellt den Satz von Einstellungen dar, die zwischen diesen Anwendungsinstanzen freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="605ce-708">The Common section represents the set of settings that are shared between those Application instances.</span></span> <span data-ttu-id="605ce-709">Es handelt sich um eine Sammlung der folgenden Felder/Typen.</span><span class="sxs-lookup"><span data-stu-id="605ce-709">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="605ce-710">Feld/Typ</span><span class="sxs-lookup"><span data-stu-id="605ce-710">Field/Type</span></span></th>
<th align="left"><span data-ttu-id="605ce-711">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="605ce-711">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-712">Name</span><span class="sxs-lookup"><span data-stu-id="605ce-712">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-713">Gibt einen eindeutigen Namen für die Vorlage "Settings Location" an.</span><span class="sxs-lookup"><span data-stu-id="605ce-713">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="605ce-714">Diese Funktion wird für Anzeigezwecke verwendet, wenn Sie in WMI, PowerShell, Ereignisanzeige und Debug-Protokollen auf die Vorlage verweisen.</span><span class="sxs-lookup"><span data-stu-id="605ce-714">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="605ce-715">Weitere Informationen finden Sie unter <a href="#name" data-raw-source="[Name](#name)"> Name </a> .</span><span class="sxs-lookup"><span data-stu-id="605ce-715">For more information, see <a href="#name" data-raw-source="[Name](#name)">Name</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-716">ID</span><span class="sxs-lookup"><span data-stu-id="605ce-716">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-717">Füllt einen eindeutigen Bezeichner für eine bestimmte Vorlage auf.</span><span class="sxs-lookup"><span data-stu-id="605ce-717">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="605ce-718">Dieses Tag wird zur primären Kennung, mit der der UE-V-Agent zur Laufzeit auf die Vorlage verweist.</span><span class="sxs-lookup"><span data-stu-id="605ce-718">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="605ce-719">Weitere Informationen finden Sie unter <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="605ce-719">For more information, see <a href="#id" data-raw-source="[ID](#id)">ID</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-720">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="605ce-720">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-721">Eine optionale Beschreibung der Vorlage.</span><span class="sxs-lookup"><span data-stu-id="605ce-721">An optional description of the template.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-722">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="605ce-722">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-723">Ein optionaler Name, der auf der Benutzeroberfläche angezeigt wird und von einem Gebietsschema der Sprache lokalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="605ce-723">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-724">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="605ce-724">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-725">Eine optionale Vorlagenbeschreibung, die von einem Sprachgebietsschema lokalisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="605ce-725">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-726">Version</span><span class="sxs-lookup"><span data-stu-id="605ce-726">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-727">Identifiziert die Version der Vorlage für die Einstellungsposition für die administrative Nachverfolgung von Änderungen.</span><span class="sxs-lookup"><span data-stu-id="605ce-727">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="605ce-728">Weitere Informationen finden Sie unter <a href="#version" data-raw-source="[Version](#version)"> Version </a> .</span><span class="sxs-lookup"><span data-stu-id="605ce-728">For more information, see <a href="#version" data-raw-source="[Version](#version)">Version</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-729">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="605ce-729">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-730">Steuert, ob diese Vorlage in Verbindung mit einem Microsoft-Konto aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="605ce-730">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="605ce-731">Wenn die Synchronisierung von MSA für einen Benutzer auf einem Computer aktiviert ist, wird diese Vorlage automatisch deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="605ce-731">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-732">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="605ce-732">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-733">Ähnlich wie MSA steuert dies, ob diese Vorlage in Verbindung mit Office365 aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="605ce-733">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="605ce-734">Wenn Office 365 zum Synchronisieren von Einstellungen verwendet wird, wird diese Vorlage automatisch deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="605ce-734">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-735">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="605ce-735">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-736">Ein Container für alle Einstellungen, die für eine bestimmte Vorlage gelten.</span><span class="sxs-lookup"><span data-stu-id="605ce-736">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="605ce-737">Sie enthält Instanzen der Registrierungs-, Datei-, Systemparameter-und benutzerdefinierten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="605ce-737">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="605ce-738">Weitere Informationen finden Sie unter <strong> Einstellungen </strong> in <a href="#data" data-raw-source="[Data types](#data)"> Datentypen </a> .</span><span class="sxs-lookup"><span data-stu-id="605ce-738">For more information, see <strong>Settings</strong> in <a href="#data" data-raw-source="[Data types](#data)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate"></a><span data-ttu-id="605ce-739">SettingsLocationTemplate-Element</span><span class="sxs-lookup"><span data-stu-id="605ce-739">SettingsLocationTemplate Element</span></span>

<span data-ttu-id="605ce-740">Dieses Element definiert die Einstellungen für eine einzelne Anwendung oder eine Suite von Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="605ce-740">This element defines the settings for a single application or a suite of applications.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="605ce-741">Feld/Typ</span><span class="sxs-lookup"><span data-stu-id="605ce-741">Field/Type</span></span></th>
<th align="left"><span data-ttu-id="605ce-742">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="605ce-742">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-743">Name</span><span class="sxs-lookup"><span data-stu-id="605ce-743">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-744">Gibt einen eindeutigen Namen für die Vorlage "Settings Location" an.</span><span class="sxs-lookup"><span data-stu-id="605ce-744">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="605ce-745">Diese Funktion wird für Anzeigezwecke verwendet, wenn Sie in WMI, PowerShell, Ereignisanzeige und Debug-Protokollen auf die Vorlage verweisen.</span><span class="sxs-lookup"><span data-stu-id="605ce-745">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="605ce-746">Weitere Informationen finden Sie unter <a href="#name" data-raw-source="[Name](#name)"> Name </a> .</span><span class="sxs-lookup"><span data-stu-id="605ce-746">For more information, see <a href="#name" data-raw-source="[Name](#name)">Name</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-747">ID</span><span class="sxs-lookup"><span data-stu-id="605ce-747">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-748">Füllt einen eindeutigen Bezeichner für eine bestimmte Vorlage auf.</span><span class="sxs-lookup"><span data-stu-id="605ce-748">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="605ce-749">Dieses Tag wird zur primären Kennung, mit der der UE-V-Agent zur Laufzeit auf die Vorlage verweist.</span><span class="sxs-lookup"><span data-stu-id="605ce-749">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="605ce-750">Weitere Informationen finden Sie unter <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="605ce-750">For more information, see <a href="#id" data-raw-source="[ID](#id)">ID</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-751">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="605ce-751">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-752">Eine optionale Beschreibung der Vorlage.</span><span class="sxs-lookup"><span data-stu-id="605ce-752">An optional description of the template.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="605ce-753">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="605ce-753">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-754">Ein optionaler Name, der auf der Benutzeroberfläche angezeigt wird und von einem Gebietsschema der Sprache lokalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="605ce-754">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="605ce-755">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="605ce-755">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="605ce-756">Eine optionale Vorlagenbeschreibung, die von einem Sprachgebietsschema lokalisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="605ce-756">An optional template description localized by a language locale.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix"></a><span data-ttu-id="605ce-757">Anhang: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="605ce-757">Appendix: SettingsLocationTemplate.xsd</span></span>

<span data-ttu-id="605ce-758">Hier sehen Sie die SettingsLocationTemplate. xsd-Datei mit den Elementen, untergeordneten Elementen, Attributen und Parametern:</span><span class="sxs-lookup"><span data-stu-id="605ce-758">Here is the SettingsLocationTemplate.xsd file showing its elements, child elements, attributes, and parameters:</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="Guid">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="FilenameString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="IDString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="TemplateVersion">
    <xs:restriction base="xs:integer">
      <xs:minInclusive value="0" />
      <xs:maxInclusive value="2147483647" />
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Empty">
    <xs:sequence/>
  </xs:complexType>

  <xs:complexType name="LocalizedString">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Locale" type="xs:string" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="LocalizedName">
    <xs:sequence>
      <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="LocalizedDescription">
    <xs:sequence>
      <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Author">
    <xs:all>
      <xs:element name="Name" type="xs:string" minOccurs="1" />
      <xs:element name="Email" type="xs:string" minOccurs="0" />
    </xs:all>
  </xs:complexType>

  <xs:complexType name="Range">
    <xs:attribute name="Minimum" type="xs:integer" use="required"/>
    <xs:attribute name="Maximum" type="xs:integer" use="required"/>
  </xs:complexType>

  <xs:complexType name="ProcessVersion">
    <xs:sequence>
      <xs:element name="Major" type="Range" minOccurs="1" />
      <xs:element name="Minor" type="Range" minOccurs="0" />
      <xs:element name="Build" type="Range" minOccurs="0" />
      <xs:element name="Patch" type="Range" minOccurs="0" />
    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="Architecture">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Win32"/>
      <xs:enumeration value="Win64"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Process">
    <xs:sequence>
      <xs:element name="Filename" type="FilenameString" minOccurs="1" />
      <xs:element name="Architecture" type="Architecture" minOccurs="0" />
      <xs:element name="ProductName" type="xs:string" minOccurs="0" />
      <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
      <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
      <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Processes">
    <xs:sequence>
      <xs:choice minOccurs="1">
        <xs:element name="Process" type="Process" />
        <xs:element name="ShellProcess" type="Empty" />
      </xs:choice>
      <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Path">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
        <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="RegistrySetting">
    <xs:sequence>
      <xs:element name="Path" type="Path" />
      <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="FileSetting">
    <xs:sequence>

      <xs:element name="Root">
        <xs:complexType>
          <xs:choice>
            <xs:element name="KnownFolder" type="Guid" />
            <xs:element name="RegistryEntry" type="xs:string" />
            <xs:element name="EnvironmentVariable" type="xs:string" />
          </xs:choice>
        </xs:complexType>
      </xs:element>

      <xs:element name="Path" minOccurs="0" type="Path" />
      <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>

    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="SystemParameterSetting">
    <xs:restriction base="xs:string">

      <!-- Accessibility parameters -->
      <xs:enumeration value="AccessTimeout"/>
      <xs:enumeration value="AudioDescription"/>
      <xs:enumeration value="ClientAreaAnimation"/>
      <xs:enumeration value="DisableOverlappedContent"/>
      <xs:enumeration value="FilterKeys"/>
      <xs:enumeration value="FocusBorderHeight"/>
      <xs:enumeration value="FocusBorderWidth"/>
      <xs:enumeration value="HighContrast"/>
      <xs:enumeration value="MessageDuration"/>
      <xs:enumeration value="MouseClickLock"/>
      <xs:enumeration value="MouseClickLockTime"/>
      <xs:enumeration value="MouseKeys"/>
      <xs:enumeration value="MouseSonar"/>
      <xs:enumeration value="MouseVanish"/>
      <xs:enumeration value="ScreenReader"/>
      <xs:enumeration value="ShowSounds"/>
      <xs:enumeration value="SoundSentry"/>
      <xs:enumeration value="StickyKeys"/>
      <xs:enumeration value="ToggleKeys"/>

      <!-- Input parameters -->
      <xs:enumeration value="Beep"/>
      <xs:enumeration value="BlockSendInputResets"/>
      <xs:enumeration value="DefaultInputLang"/>
      <xs:enumeration value="DoubleClickTime"/>
      <xs:enumeration value="DoubleClkHeight"/>
      <xs:enumeration value="DoubleClkWidth"/>
      <xs:enumeration value="KeyboardCues"/>
      <xs:enumeration value="KeyboardDelay"/>
      <xs:enumeration value="KeyboardPref"/>
      <xs:enumeration value="KeyboardSpeed"/>
      <xs:enumeration value="Mouse"/>
      <xs:enumeration value="MouseButtonSwap"/>
      <xs:enumeration value="MouseHoverHeight"/>
      <xs:enumeration value="MouseHoverTime"/>
      <xs:enumeration value="MouseHoverWidth"/>
      <xs:enumeration value="MouseSpeed"/>
      <xs:enumeration value="MouseTrails"/>
      <xs:enumeration value="SnapToDefButton"/>
      <xs:enumeration value="WheelScrollChars"/>
      <xs:enumeration value="WheelScrollLines"/>

      <!-- Desktop parameters (limited subset) -->
      <xs:enumeration value="DeskWallpaper"/>
      <xs:enumeration value="DesktopColor"/>

    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Settings">
    <xs:sequence>
      <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
      <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Registry" type="RegistrySetting" />
        <xs:element name="File" type="FileSetting" />
        <xs:element name="SystemParameter" type="SystemParameterSetting" />
      </xs:choice>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Common">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Application">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Processes" type="Processes" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>


  <xs:element name="SettingsLocationTemplate">
    <xs:complexType>
      <xs:sequence>

        <xs:element name="Name" type="xs:string" />
        <xs:element name="ID" type="IDString" />
        <xs:element name="Description" type="xs:string" minOccurs="0" />
        <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
        <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

        <xs:choice>

          <!-- Single application -->
          <xs:sequence>
            <xs:element name="Version" type="TemplateVersion" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
          </xs:sequence>

          <!-- Suite of applications -->
          <xs:sequence>
            <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="Common" type="Common" />
            <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
          </xs:sequence>

        </xs:choice>

      </xs:sequence>
    </xs:complexType>
  </xs:element>
  <!-- SettingsLocationTemplate -->

</xs:schema>
```






## <span data-ttu-id="605ce-759">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="605ce-759">Related topics</span></span>


[<span data-ttu-id="605ce-760">Arbeiten mit benutzerdefinierten UE-v 2. x-Vorlagen und dem UE-v 2. x-Generator</span><span class="sxs-lookup"><span data-stu-id="605ce-760">Working with Custom UE-V 2.x Templates and the UE-V 2.x Generator</span></span>](working-with-custom-ue-v-2x-templates-and-the-ue-v-2x-generator-new-uevv2.md)

[<span data-ttu-id="605ce-761">Technische Referenz für UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="605ce-761">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





