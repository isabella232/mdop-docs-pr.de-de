---
title: Über die Verbindungsgruppendatei
description: Über die Verbindungsgruppendatei
author: dansimp
ms.assetid: 1f4df515-f5f6-4b58-91a8-c71598cb3ea4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31ef9dc9c4465ed8f261b73518348c05ceb78d15
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806095"
---
# <span data-ttu-id="0ef98-103">Über die Verbindungsgruppendatei</span><span class="sxs-lookup"><span data-stu-id="0ef98-103">About the Connection Group File</span></span>


**<span data-ttu-id="0ef98-104">In diesem Thema:</span><span class="sxs-lookup"><span data-stu-id="0ef98-104">In this topic:</span></span>**

-   [<span data-ttu-id="0ef98-105">Zweck und Speicherort der Verbindungsgruppen Datei</span><span class="sxs-lookup"><span data-stu-id="0ef98-105">Connection group file purpose and location</span></span>](#bkmk-cg-purpose-loc)

-   [<span data-ttu-id="0ef98-106">Struktur der XML-Datei der Verbindungsgruppe</span><span class="sxs-lookup"><span data-stu-id="0ef98-106">Structure of the connection group XML file</span></span>](#bkmk-define-cg-5-0sp3)

-   [<span data-ttu-id="0ef98-107">Konfigurieren der Priorität von Paketen in einer Verbindungsgruppe</span><span class="sxs-lookup"><span data-stu-id="0ef98-107">Configuring the priority of packages in a connection group</span></span>](#bkmk-config-pkg-priority-incg)

-   [<span data-ttu-id="0ef98-108">Unterstützte Verbindungskonfigurationen für virtuelle Anwendungen</span><span class="sxs-lookup"><span data-stu-id="0ef98-108">Supported virtual application connection configurations</span></span>](#bkmk-va-conn-configs)

## <a href="" id="bkmk-cg-purpose-loc"></a><span data-ttu-id="0ef98-109">Zweck und Speicherort der Verbindungsgruppen Datei</span><span class="sxs-lookup"><span data-stu-id="0ef98-109">Connection group file purpose and location</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0ef98-110">Zweck der Verbindungsgruppe</span><span class="sxs-lookup"><span data-stu-id="0ef98-110">Connection group purpose</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ef98-111">Eine Verbindungsgruppe ist ein App-V-Feature, mit dem Sie Pakete zusammen gruppieren können, um eine virtuelle Umgebung zu erstellen, in der die Anwendungen in diesen Paketen miteinander interagieren können.</span><span class="sxs-lookup"><span data-stu-id="0ef98-111">A connection group is an App-V feature that enables you to group packages together to create a virtual environment in which the applications in those packages can interact with each other.</span></span></p>
<p><span data-ttu-id="0ef98-112">Beispiel: Sie möchten Plug-ins mit Microsoft Office verwenden.</span><span class="sxs-lookup"><span data-stu-id="0ef98-112">Example: You want to use plug-ins with Microsoft Office.</span></span> <span data-ttu-id="0ef98-113">Sie können ein Paket erstellen, das die Plug-Ins enthält, ein weiteres Paket erstellen, das Office enthält, und dann beide Pakete zu einer Verbindungsgruppe hinzufügen, um Office die Verwendung dieser Plug-ins zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0ef98-113">You can create a package that contains the plug-ins, and create another package that contains Office, and then add both packages to a connection group to enable Office to use those plug-ins.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0ef98-114">Funktionsweise der Verbindungsgruppen Datei</span><span class="sxs-lookup"><span data-stu-id="0ef98-114">How the connection group file works</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ef98-115">Wenn Sie eine App-V 5,1-Verbindungsgruppen Datei anwenden, werden die in der Datei aufgelisteten Pakete zur Laufzeit in einer einzelnen virtuellen Umgebung kombiniert.</span><span class="sxs-lookup"><span data-stu-id="0ef98-115">When you apply an App-V 5.1 connection group file, the packages that are enumerated in the file will be combined at runtime into a single virtual environment.</span></span> <span data-ttu-id="0ef98-116">Verwenden Sie die Microsoft Application Virtualization (app-v) 5,1-Verbindungsgruppen Datei, um vorhandene App-v 5,1-Verbindungsgruppen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0ef98-116">Use the Microsoft Application Virtualization (App-V) 5.1 connection group file to configure existing App-V 5.1 connection groups.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0ef98-117">Beispiel Dateipfad</span><span class="sxs-lookup"><span data-stu-id="0ef98-117">Example file path</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ef98-118">%APPDATA%\Microsoft\AppV\Client\Catalog\PackageGroups {6CCC7575-162E-4152-9407-ED411DA138F4} {4D1E16E1-8EF8-41ED-92D5-8910A8527F96}.</span><span class="sxs-lookup"><span data-stu-id="0ef98-118">%APPDATA%\Microsoft\AppV\Client\Catalog\PackageGroups{6CCC7575-162E-4152-9407-ED411DA138F4}{4D1E16E1-8EF8-41ED-92D5-8910A8527F96}.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-define-cg-5-0sp3"></a><span data-ttu-id="0ef98-119">Struktur der XML-Datei der Verbindungsgruppe</span><span class="sxs-lookup"><span data-stu-id="0ef98-119">Structure of the connection group XML file</span></span>


**<span data-ttu-id="0ef98-120">In diesem Abschnitt:</span><span class="sxs-lookup"><span data-stu-id="0ef98-120">In this section:</span></span>**

-   [<span data-ttu-id="0ef98-121">Parameter, die die Verbindungsgruppe definieren</span><span class="sxs-lookup"><span data-stu-id="0ef98-121">Parameters that define the connection group</span></span>](#bkmk-params-define-cg)

-   [<span data-ttu-id="0ef98-122">Parameter, die die Pakete in der Verbindungsgruppe definieren</span><span class="sxs-lookup"><span data-stu-id="0ef98-122">Parameters that define the packages in the connection group</span></span>](#bkmk-params-define-pkgs-incg)

-   [<span data-ttu-id="0ef98-123">App-V-Beispiel für eine Verbindungsgruppen-XML-Datei</span><span class="sxs-lookup"><span data-stu-id="0ef98-123">App-V example connection group XML file</span></span>](#bkmk-50sp3-exp-cg-xml)

-   [<span data-ttu-id="0ef98-124">App-v 5,0 durch APP-v 5,0 SP2-Beispiel einer Verbindungsgruppen-XML-Datei</span><span class="sxs-lookup"><span data-stu-id="0ef98-124">App-V 5.0 through App-V 5.0 SP2 example connection group XML file</span></span>](#bkmk-50thru50sp2-exp-cg-xm)

### <a href="" id="bkmk-params-define-cg"></a><span data-ttu-id="0ef98-125">Parameter, die die Verbindungsgruppe definieren</span><span class="sxs-lookup"><span data-stu-id="0ef98-125">Parameters that define the connection group</span></span>

<span data-ttu-id="0ef98-126">In der folgenden Tabelle werden die Parameter in der XML-Datei beschrieben, die die Verbindungsgruppe selbst und nicht die Pakete definieren.</span><span class="sxs-lookup"><span data-stu-id="0ef98-126">The following table describes the parameters in the XML file that define the connection group itself, not the packages.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0ef98-127">Feld</span><span class="sxs-lookup"><span data-stu-id="0ef98-127">Field</span></span></th>
<th align="left"><span data-ttu-id="0ef98-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ef98-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0ef98-129">Schemaname</span><span class="sxs-lookup"><span data-stu-id="0ef98-129">Schema name</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ef98-130">Der Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="0ef98-130">Name of the schema.</span></span></p>
<p><strong><span data-ttu-id="0ef98-131">Anwendbar ab App-V 5,0 SP3 </strong> : Wenn Sie die neuen Features "optionale Pakete" und "Verwenden einer beliebigen Version" verwenden möchten, die in dieser Tabelle beschrieben werden, müssen Sie das folgende Schema in der XML-Datei angeben:</span><span class="sxs-lookup"><span data-stu-id="0ef98-131">Applicable starting in App-V 5.0 SP3</strong>: If you want to use the new “optional packages” and “use any version” features that are described in this table, you must specify the following schema in the XML file:</span></span></p>
<p><code>xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0ef98-132">AppConnectionGroupId</span><span class="sxs-lookup"><span data-stu-id="0ef98-132">AppConnectionGroupId</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ef98-133">Eindeutiger GUID-Bezeichner für diese Verbindungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0ef98-133">Unique GUID identifier for this connection group.</span></span> <span data-ttu-id="0ef98-134">Der Verbindungsgruppen Status ist diesem Bezeichner zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="0ef98-134">The connection group state is associated with this identifier.</span></span> <span data-ttu-id="0ef98-135">Geben Sie diesen Bezeichner nur an, wenn Sie die Verbindungsgruppe erstellen.</span><span class="sxs-lookup"><span data-stu-id="0ef98-135">Specify this identifier only when you create the connection group.</span></span></p>
<p><span data-ttu-id="0ef98-136">Sie können eine neue GUID erstellen, indem Sie Folgendes <strong>[Guid]::NewGuid()</strong> eingeben:</span><span class="sxs-lookup"><span data-stu-id="0ef98-136">You can create a new GUID by typing: <strong>[Guid]::NewGuid()</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0ef98-137">VersionID</span><span class="sxs-lookup"><span data-stu-id="0ef98-137">VersionId</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ef98-138">Versions-GUID-Bezeichner für diese Version der Verbindungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0ef98-138">Version GUID identifier for this version of the connection group.</span></span></p>
<p><span data-ttu-id="0ef98-139">Beim Aktualisieren einer Verbindungsgruppe (beispielsweisedurch hinzufügen oder Aktualisieren eines neuen Pakets) müssen Sie die Versions-GUID so aktualisieren, dass Sie der neuen Version entspricht.</span><span class="sxs-lookup"><span data-stu-id="0ef98-139">When you update a connection group (for example, by adding or updating a new package), you must update the version GUID to reflect the new version.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0ef98-140">DisplayName</span><span class="sxs-lookup"><span data-stu-id="0ef98-140">DisplayName</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ef98-141">Anzeigename der Verbindungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0ef98-141">Display name of the connection group.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0ef98-142">Priorität</span><span class="sxs-lookup"><span data-stu-id="0ef98-142">Priority</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ef98-143">Optionales Prioritätsfeld für die Verbindungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0ef98-143">Optional priority field for the connection group.</span></span></p>
<p><strong><span data-ttu-id="0ef98-144">"0" </strong> - gibt die höchste Priorität an.</span><span class="sxs-lookup"><span data-stu-id="0ef98-144">“0”</strong> - indicates the highest priority.</span></span></p>
<p><span data-ttu-id="0ef98-145">Wenn eine Priorität erforderlich ist, aber nicht konfiguriert wurde, schlägt das Paket fehl, da die richtige zu verwendende Verbindungsgruppe nicht ermittelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0ef98-145">If a priority is required, but has not been configured, the package will fail because the correct connection group to use cannot be determined.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-params-define-pkgs-incg"></a><span data-ttu-id="0ef98-146">Parameter, die die Pakete in der Verbindungsgruppe definieren</span><span class="sxs-lookup"><span data-stu-id="0ef98-146">Parameters that define the packages in the connection group</span></span>

<span data-ttu-id="0ef98-147">Im &lt; Abschnitt Pakete &gt; der XML-Datei der Verbindungsgruppe Listen Sie die Mitglieder Pakete in der Verbindungsgruppe auf, indem Sie die einzelnen Paket Bezeichner und die Versionskennung angeben, wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0ef98-147">In the &lt;Packages&gt; section of the connection group XML file, you list the member packages in the connection group by specifying each package’s unique package identifier and version identifier, as described in the following table.</span></span> <span data-ttu-id="0ef98-148">Das erste Paket in der Liste hat die höchste Priorität.</span><span class="sxs-lookup"><span data-stu-id="0ef98-148">The first package in the list has the highest precedence.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0ef98-149">Feld</span><span class="sxs-lookup"><span data-stu-id="0ef98-149">Field</span></span></th>
<th align="left"><span data-ttu-id="0ef98-150">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ef98-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0ef98-151">PackageId</span><span class="sxs-lookup"><span data-stu-id="0ef98-151">PackageId</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ef98-152">Eindeutiger GUID-Bezeichner für dieses Paket.</span><span class="sxs-lookup"><span data-stu-id="0ef98-152">Unique GUID identifier for this package.</span></span> <span data-ttu-id="0ef98-153">Diese GUID ändert sich nicht, wenn neuere Versionen des Pakets veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="0ef98-153">This GUID doesn’t change when newer versions of the package are published.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0ef98-154">VersionID</span><span class="sxs-lookup"><span data-stu-id="0ef98-154">VersionId</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ef98-155">Eindeutiger GUID-Bezeichner für die Version des Pakets.</span><span class="sxs-lookup"><span data-stu-id="0ef98-155">Unique GUID identifier for the version of the package.</span></span></p>
<p><strong><span data-ttu-id="0ef98-156">Anwendbar ab App-V 5,0 SP3 </strong> : Wenn Sie <strong> </strong> für die Paketversion "\*" angeben, wird die GUID der neuesten verfügbaren Paketversion dynamisch eingefügt.</span><span class="sxs-lookup"><span data-stu-id="0ef98-156">Applicable starting in App-V 5.0 SP3</strong>: If you specify <strong>“\*”</strong> for the package version, the GUID of the latest available package version is dynamically inserted.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0ef98-157">IsOptional</span><span class="sxs-lookup"><span data-stu-id="0ef98-157">IsOptional</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="0ef98-158">Anwendbar ab App-V 5,0 SP3 </strong> : Parameter, mit dem Sie ein Paket in der Verbindungsgruppe optional erstellen können.</span><span class="sxs-lookup"><span data-stu-id="0ef98-158">Applicable starting in App-V 5.0 SP3</strong>: Parameter that enables you to make a package optional within the connection group.</span></span> <span data-ttu-id="0ef98-159">Gültige Einträge sind:</span><span class="sxs-lookup"><span data-stu-id="0ef98-159">Valid entries are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="0ef98-160">"wahr" </strong> – das Paket ist in der Verbindungsgruppe optional</span><span class="sxs-lookup"><span data-stu-id="0ef98-160">“true”</strong> – package is optional in the connection group</span></span></p></li>
<li><p><strong><span data-ttu-id="0ef98-161">"falsch" </strong> – das Paket ist in der Verbindungsgruppe erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0ef98-161">“false”</strong> – package is required in the connection group</span></span></p></li>
</ul>
<p><span data-ttu-id="0ef98-162">Weitere Informationen finden Sie unter <a href="how-to-use-optional-packages-in-connection-groups51.md" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups51.md)"> Verwenden optionaler Pakete in Verbindungsgruppen </a> .</span><span class="sxs-lookup"><span data-stu-id="0ef98-162">See <a href="how-to-use-optional-packages-in-connection-groups51.md" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups51.md)">How to Use Optional Packages in Connection Groups</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-50sp3-exp-cg-xml"></a><span data-ttu-id="0ef98-163">App-V-Beispiel für eine Verbindungsgruppen-XML-Datei</span><span class="sxs-lookup"><span data-stu-id="0ef98-163">App-V example connection group XML file</span></span>

<span data-ttu-id="0ef98-164">Die folgende XML-Beispieldatei der Verbindungsgruppe zeigt Beispiele für die Felder in den vorherigen Tabellen und hebt die Elemente hervor, die neu ab App-V 5,0 SP3 sind.</span><span class="sxs-lookup"><span data-stu-id="0ef98-164">The following example connection group XML file shows examples of the fields in the previous tables and highlights the items that are new starting in App-V 5.0 SP3.</span></span>

```XML
<?xml version="1.0" encoding="UTF-16">
<appv:AppConnectionGroup 
  xmlns="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"
  xmlns:appv="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"  
  AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
  VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"
  Priority="0"  
  DisplayName="Sample Connection Group">
  <appv:Packages>    
    <appv:Package
      PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
      VersionId="*"
      IsOptional="true"    
    />
    <appv:Package
      PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
      VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
      IsOptional="false"    
    />  
  </appv:Packages>
</appv:AppConnectionGroup>
```

### <a href="" id="bkmk-50thru50sp2-exp-cg-xm"></a><span data-ttu-id="0ef98-165">App-v 5,0 durch APP-v 5,0 SP2-Beispiel einer Verbindungsgruppen-XML-Datei</span><span class="sxs-lookup"><span data-stu-id="0ef98-165">App-V 5.0 through App-V 5.0 SP2 example connection group XML file</span></span>

<span data-ttu-id="0ef98-166">Die folgende XML-Beispieldatei für die Verbindungsgruppe bezieht sich auf App-v 5,0 über APP-v 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="0ef98-166">The following example connection group XML file applies to App-V 5.0 through App-V 5.0 SP2.</span></span> <span data-ttu-id="0ef98-167">Sie zeigt Beispiele für die Felder in der vorherigen Tabelle, schließt aber die oben beschriebenen Änderungen für App-V 5,0 SP3 aus.</span><span class="sxs-lookup"><span data-stu-id="0ef98-167">It shows examples of the fields in the previous table, but it excludes the changes described above for App-V 5.0 SP3.</span></span>

```XML
<?xml version="1.0" encoding="UTF-16">
<appv:AppConnectionGroup
  xmlns="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
  xmlns:appv="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
  AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
  VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"
  Priority="0"
  DisplayName="Sample Connection Group">
  <appv:Packages>
    <appv:Package
      PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
      VersionId="C7DF4F63-5288-439C-ACEF-EF06BF401EC5"
    />
    <appv:Package
     PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
     VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
   />
 </appv:Packages>
<appv:AppConnectionGroup>
```

## <a href="" id="bkmk-config-pkg-priority-incg"></a><span data-ttu-id="0ef98-168">Konfigurieren der Priorität von Paketen in einer Verbindungsgruppe</span><span class="sxs-lookup"><span data-stu-id="0ef98-168">Configuring the priority of packages in a connection group</span></span>


<span data-ttu-id="0ef98-169">Die Paket Rangfolge wird mithilfe der Paket Listenreihenfolge konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="0ef98-169">Package precedence is configured using the package list order.</span></span> <span data-ttu-id="0ef98-170">Das erste Paket im Dokument hat die höchste Priorität.</span><span class="sxs-lookup"><span data-stu-id="0ef98-170">The first package in the document has the highest precedence.</span></span> <span data-ttu-id="0ef98-171">Nachfolgende Pakete in der Liste haben eine absteigende Priorität.</span><span class="sxs-lookup"><span data-stu-id="0ef98-171">Subsequent packages in the list have descending priority.</span></span>

<span data-ttu-id="0ef98-172">Die Paket Rangfolge ist die Lösung für ansonsten unvermeidliche Ressourcenkonflikte während der Initialisierung der virtuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="0ef98-172">Package precedence is the resolution for otherwise inevitable resource collisions during virtual environment initialization.</span></span> <span data-ttu-id="0ef98-173">Wenn beispielsweise zwei Pakete, die sich in derselben virtuellen Umgebung öffnen, denselben Registrierungs-DWORD-Wert definieren, bestimmt das Paket mit der höchsten Rangfolge den festgelegten Wert.</span><span class="sxs-lookup"><span data-stu-id="0ef98-173">For example, if two packages that are opening in the same virtual environment define the same registry DWORD value, the package with the highest precedence determines the value that is set.</span></span>

<span data-ttu-id="0ef98-174">Sie können die Verbindungsgruppen Datei verwenden, um jede Verbindungsgruppe mithilfe der folgenden Methoden zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="0ef98-174">You can use the connection group file to configure each connection group by using the following methods:</span></span>

-   <span data-ttu-id="0ef98-175">Angeben von Lauf Zeit Prioritäten für Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="0ef98-175">Specify runtime priorities for connection groups.</span></span> <span data-ttu-id="0ef98-176">Wenn Sie die Priorität mithilfe der App-V-Verwaltungskonsole bearbeiten möchten, klicken Sie auf die Gruppe Verbindung, und klicken Sie dann auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="0ef98-176">To edit priority by using the App-V Management Console, click the connection group and then click **Edit**.</span></span>

    <span data-ttu-id="0ef98-177">**Hinweis**  Die Priorität ist nur erforderlich, wenn das Paket mehr als einer Verbindungsgruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0ef98-177">**Note** Priority is required only if the package is associated with more than one connection group.</span></span>

     

-   <span data-ttu-id="0ef98-178">Geben Sie die Paket Rangfolge innerhalb der Verbindungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="0ef98-178">Specify package precedence within the connection group.</span></span>

<span data-ttu-id="0ef98-179">Das Feld "Priorität" ist erforderlich, wenn eine ausgeführte virtuelle Anwendung aus einer systemeigenen Anwendungsanforderung initiiert wird, beispielsweise Microsoft Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="0ef98-179">The priority field is required when a running virtual application initiates from a native application request, for example, Microsoft Windows Explorer.</span></span> <span data-ttu-id="0ef98-180">Der App-V-Client verwendet die Priorität, um zu ermitteln, in welcher Verbindungsgruppe die virtuelle Umgebung ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0ef98-180">The App-V client uses the priority to determine which connection group virtual environment the application should run in.</span></span> <span data-ttu-id="0ef98-181">Diese Situation tritt auf, wenn eine virtuelle Anwendung Teil mehrerer Verbindungsgruppen ist.</span><span class="sxs-lookup"><span data-stu-id="0ef98-181">This situation occurs if a virtual application is part of multiple connection groups.</span></span>

<span data-ttu-id="0ef98-182">Wenn eine virtuelle Anwendung mit einer anderen virtuellen Anwendung geöffnet wird, wird die virtuelle Umgebung der ursprünglichen virtuellen Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ef98-182">If a virtual application is opened using another virtual application the virtual environment of the original virtual application will be used.</span></span> <span data-ttu-id="0ef98-183">Das Feld "Priorität" wird in diesem Fall nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ef98-183">The priority field is not used in this case.</span></span>

**<span data-ttu-id="0ef98-184">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="0ef98-184">Example:</span></span>**

<span data-ttu-id="0ef98-185">Die virtuelle Anwendung Microsoft Outlook wird in der virtuellen Umgebung **XYZ**ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ef98-185">The virtual application Microsoft Outlook is running in virtual environment **XYZ**.</span></span> <span data-ttu-id="0ef98-186">Wenn Sie ein angefügtes Microsoft Word-Dokument öffnen, wird in der virtuellen Umgebung **XYZ**eine virtualisierte Version von Microsoft Word geöffnet, unabhängig davon, welche virtuellen Microsoft Word-Verbindungsgruppen oder-Lauf Zeit Prioritäten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0ef98-186">When you open an attached Microsoft Word document, a virtualized version Microsoft Word opens in the virtual environment **XYZ**, regardless of the virtualized Microsoft Word’s associated connection groups or runtime priorities.</span></span>

## <a href="" id="bkmk-va-conn-configs"></a><span data-ttu-id="0ef98-187">Unterstützte Verbindungskonfigurationen für virtuelle Anwendungen</span><span class="sxs-lookup"><span data-stu-id="0ef98-187">Supported virtual application connection configurations</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0ef98-188">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="0ef98-188">Configuration</span></span></th>
<th align="left"><span data-ttu-id="0ef98-189">Beispielszenarien</span><span class="sxs-lookup"><span data-stu-id="0ef98-189">Example scenario</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0ef98-190">Eine.</span><span class="sxs-lookup"><span data-stu-id="0ef98-190">An.</span></span> <span data-ttu-id="0ef98-191">exe-Datei und-Plug-in (. dll)</span><span class="sxs-lookup"><span data-stu-id="0ef98-191">exe file and plug-in (.dll)</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="0ef98-192">Sie möchten Microsoft Office an alle Benutzer verteilen, aber ein Microsoft Excel-Plug-in nur an eine Teilmenge von Benutzern verteilen.</span><span class="sxs-lookup"><span data-stu-id="0ef98-192">You want to distribute Microsoft Office to all users, but distribute a Microsoft Excel plug-in to only a subset of users.</span></span></p></li>
<li><p><span data-ttu-id="0ef98-193">Aktivieren Sie die Verbindungsgruppe für die entsprechenden Benutzer.</span><span class="sxs-lookup"><span data-stu-id="0ef98-193">Enable the connection group for the appropriate users.</span></span></p></li>
<li><p><span data-ttu-id="0ef98-194">Aktualisieren Sie jedes Paket einzeln nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="0ef98-194">Update each package individually as required.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0ef98-195">Eine.</span><span class="sxs-lookup"><span data-stu-id="0ef98-195">An.</span></span> <span data-ttu-id="0ef98-196">exe-Datei und eine Middleware-Anwendung</span><span class="sxs-lookup"><span data-stu-id="0ef98-196">exe file and a middleware application</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="0ef98-197">Sie verfügen über eine Anwendung erfordert eine Middleware-Anwendung oder mehrere Anwendungen, die alle von der gleichen Middleware-Laufzeitversion abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="0ef98-197">You have an application requires a middleware application, or several applications that all depend on the same middleware runtime version.</span></span></p></li>
<li><p><span data-ttu-id="0ef98-198">Alle Computer, die eine oder mehrere Anwendungen erfordern, erhalten die Verbindungsgruppen mit der Anwendungs-und Middleware-Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="0ef98-198">All computers that require one or more of the applications receive the connection groups with the application and middleware application runtime.</span></span></p></li>
<li><p><span data-ttu-id="0ef98-199">Optional können Sie mehrere Middleware-Anwendungen in einer einzigen Verbindungsgruppe kombinieren.</span><span class="sxs-lookup"><span data-stu-id="0ef98-199">You can optionally combine multiple middleware applications into a single connection group.</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0ef98-200">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0ef98-200">Example</span></span></th>
<th align="left"><span data-ttu-id="0ef98-201">Beispiel Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ef98-201">Example description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0ef98-202">Verknüpfungsgruppe für virtuelle Anwendungen für die Finanzabteilung</span><span class="sxs-lookup"><span data-stu-id="0ef98-202">Virtual application connection group for the financial division</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="0ef98-203">Middleware-Anwendung 1</span><span class="sxs-lookup"><span data-stu-id="0ef98-203">Middleware application 1</span></span></p></li>
<li><p><span data-ttu-id="0ef98-204">Middleware-Anwendung 2</span><span class="sxs-lookup"><span data-stu-id="0ef98-204">Middleware application 2</span></span></p></li>
<li><p><span data-ttu-id="0ef98-205">Middleware-Anwendung 3</span><span class="sxs-lookup"><span data-stu-id="0ef98-205">Middleware application 3</span></span></p></li>
<li><p><span data-ttu-id="0ef98-206">Middleware-Anwendungslaufzeit</span><span class="sxs-lookup"><span data-stu-id="0ef98-206">Middleware application runtime</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0ef98-207">Gruppe für virtuelle Anwendungsverbindungen für die Abteilung HR</span><span class="sxs-lookup"><span data-stu-id="0ef98-207">Virtual application connection group for HR division</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="0ef98-208">Middleware-Anwendung 5</span><span class="sxs-lookup"><span data-stu-id="0ef98-208">Middleware application 5</span></span></p></li>
<li><p><span data-ttu-id="0ef98-209">Middleware-Anwendung 6</span><span class="sxs-lookup"><span data-stu-id="0ef98-209">Middleware application 6</span></span></p></li>
<li><p><span data-ttu-id="0ef98-210">Middleware-Anwendungslaufzeit</span><span class="sxs-lookup"><span data-stu-id="0ef98-210">Middleware application runtime</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0ef98-211">Eine.</span><span class="sxs-lookup"><span data-stu-id="0ef98-211">An.</span></span> <span data-ttu-id="0ef98-212">exe-Datei und eine exe-Datei</span><span class="sxs-lookup"><span data-stu-id="0ef98-212">exe file and an .exe file</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ef98-213">Sie verfügen über eine Anwendung, die sich auf eine andere Anwendung verlässt, und Sie möchten die Pakete für Betriebseffizienz, Lizenzierungseinschränkungen oder Rollout-Zeitpläne separat aufbewahren.</span><span class="sxs-lookup"><span data-stu-id="0ef98-213">You have an application that relies on another application, and you want to keep the packages separate for operational efficiencies, licensing restrictions, or rollout timelines.</span></span></p>
<p><strong><span data-ttu-id="0ef98-214">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="0ef98-214">Example:</span></span></strong></p>
<p><span data-ttu-id="0ef98-215">Wenn Sie Microsoft lync 2010 bereitstellen, können Sie drei Pakete verwenden:</span><span class="sxs-lookup"><span data-stu-id="0ef98-215">If you are deploying Microsoft Lync 2010, you can use three packages:</span></span></p>
<ul>
<li><p><span data-ttu-id="0ef98-216">Microsoft Office2010</span><span class="sxs-lookup"><span data-stu-id="0ef98-216">Microsoft Office2010</span></span></p></li>
<li><p><span data-ttu-id="0ef98-217">Microsoft Communicator2007</span><span class="sxs-lookup"><span data-stu-id="0ef98-217">Microsoft Communicator2007</span></span></p></li>
<li><p><span data-ttu-id="0ef98-218">Microsoft Lync2010</span><span class="sxs-lookup"><span data-stu-id="0ef98-218">Microsoft Lync2010</span></span></p></li>
</ul>
<p><span data-ttu-id="0ef98-219">Sie können die Bereitstellung mithilfe der folgenden Verbindungsgruppen verwalten:</span><span class="sxs-lookup"><span data-stu-id="0ef98-219">You can manage the deployment using the following connection groups:</span></span></p>
<ul>
<li><p><span data-ttu-id="0ef98-220">Microsoft Office2010 und Microsoft Communicator2007</span><span class="sxs-lookup"><span data-stu-id="0ef98-220">Microsoft Office2010 and Microsoft Communicator2007</span></span></p></li>
<li><p><span data-ttu-id="0ef98-221">Microsoft Office2010 und Microsoft Lync2010</span><span class="sxs-lookup"><span data-stu-id="0ef98-221">Microsoft Office2010 and Microsoft Lync2010</span></span></p></li>
</ul>
<p><span data-ttu-id="0ef98-222">Wenn die Bereitstellung abgeschlossen ist, können Sie entweder ein einzelnes neues Microsoft Office2010 + Microsoft Lync2010-Paket erstellen oder diese als separate Pakete verwalten und mit einer Verbindungsgruppe bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0ef98-222">When the deployment has completed, you can either create a single new Microsoft Office2010 + Microsoft Lync2010 package, or keep and maintain them as separate packages and deploy them by using a connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="0ef98-223">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="0ef98-223">Related topics</span></span>


[<span data-ttu-id="0ef98-224">Verwalten von Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="0ef98-224">Managing Connection Groups</span></span>](managing-connection-groups51.md)

 

 




