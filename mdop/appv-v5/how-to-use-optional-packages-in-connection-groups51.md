---
title: So verwenden Sie optionale Pakete in Verbindungsgruppen
description: So verwenden Sie optionale Pakete in Verbindungsgruppen
author: dansimp
ms.assetid: 67666f18-b704-4852-a1e4-d13633bd2baf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ffa29f5d62e57a60423b2041cb71787d2c96bd66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805120"
---
# <span data-ttu-id="6b55d-103">So verwenden Sie optionale Pakete in Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="6b55d-103">How to Use Optional Packages in Connection Groups</span></span>


<span data-ttu-id="6b55d-104">Ab Microsoft Application Virtualization (App-V) 5,0 SP3 können Sie Ihren Verbindungsgruppen optionale Pakete hinzufügen, um die Verwaltung der Verbindungsgruppe zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="6b55d-104">Starting in Microsoft Application Virtualization (App-V) 5.0 SP3, you can add optional packages to your connection groups to simplify connection group management.</span></span> <span data-ttu-id="6b55d-105">In der folgenden Tabelle sind die Aufgaben, die Sie mithilfe optionaler Pakete einfacher durchführen können, zusammengefasst, und es werden Links zu den Anweisungen für die einzelnen Aufgaben bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6b55d-105">The following table summarizes the tasks that you can complete more easily by using optional packages, and provides links to instructions for each task.</span></span>

<span data-ttu-id="6b55d-106">**Hinweis** 
 **Optionale Pakete werden in Versionen vor App-V 5,0 SP3 nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="6b55d-106">**Note**
**Optional packages are not supported in releases prior to App-V 5.0 SP3.**</span></span>

 

<span data-ttu-id="6b55d-107">Lesen Sie vor dem Verwenden optionaler Pakete die [Anforderungen für die Verwendung optionaler Pakete in Verbindungsgruppen](#bkmk-reqs-using-cg).</span><span class="sxs-lookup"><span data-stu-id="6b55d-107">Before using optional packages, see [Requirements for using optional packages in connection groups](#bkmk-reqs-using-cg).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6b55d-108">Link zu Anweisungen</span><span class="sxs-lookup"><span data-stu-id="6b55d-108">Link to instructions</span></span></th>
<th align="left"><span data-ttu-id="6b55d-109">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="6b55d-109">Task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="#bkmk-apps-plugs-optional" data-raw-source="[Use one connection group, with optional packages, for multiple users who have different packages entitled to them](#bkmk-apps-plugs-optional)"><span data-ttu-id="6b55d-110">Verwenden einer Verbindungsgruppe mit optionalen Paketen für mehrere Benutzer, die über verschiedene Pakete verfügen, die Ihnen zustehen</span><span class="sxs-lookup"><span data-stu-id="6b55d-110">Use one connection group, with optional packages, for multiple users who have different packages entitled to them</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="6b55d-111">Verwenden Sie eine einzelne Verbindungsgruppe, um verschiedene Gruppen von Anwendungen und Plug-Ins für verschiedene Endbenutzer verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="6b55d-111">Use a single connection group to make different groups of applications and plug-ins available to different end users.</span></span></p>
<p><span data-ttu-id="6b55d-112">Angenommen, Sie möchten Microsoft Office an alle Endbenutzer verteilen, aber verschiedene Plug-ins an verschiedene Teilmengen von Benutzern verteilen.</span><span class="sxs-lookup"><span data-stu-id="6b55d-112">For example, you want to distribute Microsoft Office to all end users, but distribute different plug-ins to different subsets of users.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="#bkmk-unpub-del-optl-pkg" data-raw-source="[Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group](#bkmk-unpub-del-optl-pkg)"><span data-ttu-id="6b55d-113">Aufheben der Veröffentlichung oder Löschen eines optionalen Pakets oder Aufheben der Veröffentlichung eines optionalen Pakets und erneutes veröffentlichen, ohne die Verbindungsgruppe zu ändern</span><span class="sxs-lookup"><span data-stu-id="6b55d-113">Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="6b55d-114">Heben Sie die Veröffentlichung, Löschung oder erneute Veröffentlichung eines optionalen Pakets auf, ohne die Verbindungsgruppe auf dem App-V-Client zu deaktivieren, zu entfernen, zu bearbeiten, hinzuzufügen und wieder zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6b55d-114">Unpublish, delete, or republish an optional package without having to disable, remove, edit, add, and re-enable the connection group on the App-V Client.</span></span></p>
<p><span data-ttu-id="6b55d-115">Sie können die Veröffentlichung des optionalen Pakets auch aufheben und später erneut veröffentlichen, ohne die Verbindungsgruppe deaktivieren oder erneut veröffentlichen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="6b55d-115">You can also unpublish the optional package and republish it later without having to disable or republish the connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-apps-plugs-optional"></a><span data-ttu-id="6b55d-116">Verwenden einer Verbindungsgruppe mit optionalen Paketen für mehrere Benutzer mit unterschiedlichen Paketen, die Ihnen zustehen</span><span class="sxs-lookup"><span data-stu-id="6b55d-116">Use one connection group, with optional packages, for multiple users with different packages entitled to them</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6b55d-117">Aufgabenbeschreibung</span><span class="sxs-lookup"><span data-stu-id="6b55d-117">Task description</span></span></th>
<th align="left"><span data-ttu-id="6b55d-118">Durchführen der Aufgabe</span><span class="sxs-lookup"><span data-stu-id="6b55d-118">How to perform the task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6b55d-119">Mit App-v 5,0 SP3 und App-v 5,1</span><span class="sxs-lookup"><span data-stu-id="6b55d-119">With App-V 5.0 SP3 and App-V 5.1</span></span></strong></p>
<p><span data-ttu-id="6b55d-120">Sie können Verbindungsgruppen optionale Pakete hinzufügen, mit denen Sie unterschiedliche Kombinationen von Anwendungen und Plug-Ins für verschiedene Endbenutzer bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="6b55d-120">You can add optional packages to connection groups, which enables you to provide different combinations of applications and plug-ins to different end users.</span></span></p>
<p><strong><span data-ttu-id="6b55d-121">Beispiel </strong> : Sie möchten Microsoft Office an Ihre Endbenutzer verteilen, aber ein bestimmtes Plug-in nur für eine Teilmenge der Benutzer aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6b55d-121">Example</strong>: You want to distribute Microsoft Office to your end users, but enable a certain plug-in for only a subset of users.</span></span></p>
<p><span data-ttu-id="6b55d-122">Erstellen Sie dazu eine Verbindungsgruppe, die ein Paket mit Office und ein weiteres Paket mit Office-Plug-Ins enthält, und machen Sie dann das Plug-in-Paket optional.</span><span class="sxs-lookup"><span data-stu-id="6b55d-122">To do this, create a connection group that contains a package with Office, and another package with Office plug-ins, and then make the plug-ins package optional.</span></span></p>
<p><span data-ttu-id="6b55d-123">Endbenutzer, die nicht zum Plug-in-Paket berechtigt sind, können Office weiterhin ausführen.</span><span class="sxs-lookup"><span data-stu-id="6b55d-123">End users who are not entitled to the plug-in package will still be able to run Office.</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6b55d-124">Methode</span><span class="sxs-lookup"><span data-stu-id="6b55d-124">Method</span></span></th>
<th align="left"><span data-ttu-id="6b55d-125">Schritte</span><span class="sxs-lookup"><span data-stu-id="6b55d-125">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b55d-126">App-V Server – Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="6b55d-126">App-V Server – Management Console</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="6b55d-127">Wählen Sie in der Verwaltungskonsole <strong> Verbindungsgruppen aus </strong> , um die Bibliothek Verbindungsgruppen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6b55d-127">In the Management Console, select <strong>CONNECTION GROUPS</strong> to display the Connection Groups library.</span></span></p></li>
<li><p><span data-ttu-id="6b55d-128">Wählen Sie in der Bibliothek Verbindungsgruppen die richtige Verbindungsgruppe aus.</span><span class="sxs-lookup"><span data-stu-id="6b55d-128">Select the correct connection group from the Connection Groups library.</span></span></p></li>
<li><p><span data-ttu-id="6b55d-129">Klicken <strong> Sie </strong> im Bereich verbundene Pakete auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="6b55d-129">Click <strong>EDIT</strong> in the CONNECTED PACKAGES pane.</span></span></p></li>
<li><p><span data-ttu-id="6b55d-130">Wählen Sie <strong> optional </strong> neben dem Paketnamen aus.</span><span class="sxs-lookup"><span data-stu-id="6b55d-130">Select <strong>Optional</strong> next to the package name.</span></span></p></li>
<li><p><span data-ttu-id="6b55d-131">Aktivieren Sie das <strong> Kontrollkästchen Paketzugriff auf Gruppen Zugriff hinzufügen </strong> .</span><span class="sxs-lookup"><span data-stu-id="6b55d-131">Select the <strong>ADD PACKAGE ACCESS TO GROUP ACCESS</strong> check box.</span></span> <span data-ttu-id="6b55d-132">Dieser erforderliche Schritt fügt der Verbindungsgruppe die Paket Berechtigungen hinzu, die Sie zuvor konfiguriert haben, als Sie den Active Directory-GRUPPENPAKETE zugewiesen haben.</span><span class="sxs-lookup"><span data-stu-id="6b55d-132">This required step adds to the connection group the package entitlements that you configured earlier when you assigned packages to Active Directory groups.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b55d-133">App-V Server-PowerShell-Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6b55d-133">App-V Server - PowerShell cmdlet</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b55d-134">Verwenden Sie das folgende Cmdlet, und geben Sie den <strong> Parameter-optional an </strong> :</span><span class="sxs-lookup"><span data-stu-id="6b55d-134">Use the following cmdlet, and specify the <strong>-Optional</strong> parameter:</span></span></p>
<p><strong><span data-ttu-id="6b55d-135">Add-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="6b55d-135">Add-AppvServerConnectionGroupPackage</span></span></strong></p>
<p><strong><span data-ttu-id="6b55d-136">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b55d-136">Syntax:</span></span></strong></p>
<p><code>Add-AppvServerConnectionGroupPackage [-AppvServerConnectionGroup] &lt;SerializableConnectionGroup&gt; [[-AppvServerPackage] &lt;PackageVersion&gt;] [-Optional] [-Order &lt;int&gt;] [-UseAnyPackageVersion]</code></p>
<p><strong><span data-ttu-id="6b55d-137">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6b55d-137">Example:</span></span></strong></p>
<p><code>Add-AppvServerConnectionGroupPackage -Name &quot;Connection Group 1&quot; -PackageName &quot;Package 1&quot; -Optional</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b55d-138">App-V-Client auf einem eigenständigen Computer</span><span class="sxs-lookup"><span data-stu-id="6b55d-138">App-V Client on a Stand-alone computer</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="6b55d-139">Erstellen Sie das Verbindungsgruppen-XML-Dokument, und legen <strong> Sie das Package </strong> Tag-Attribut <strong> isOptional </strong> auf <strong> "true" fest.</span><span class="sxs-lookup"><span data-stu-id="6b55d-139">Create the connection group XML document, and set the <strong>Package</strong> tag attribute <strong>IsOptional</strong> to <strong>“true”.</span></span></strong></p></li>
<li><p><span data-ttu-id="6b55d-140">Verwenden Sie die folgenden Cmdlets, um die Verbindungsgruppe hinzuzufügen und zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="6b55d-140">Use the following cmdlets to add and enable the connection group:</span></span></p>
<ul>
<li><p><span data-ttu-id="6b55d-141">Add-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="6b55d-141">Add-AppvClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="6b55d-142">Enable-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="6b55d-142">Enable-AppvClientConnectionGroup</span></span></p></li>
</ul></li>
</ol>
<p><strong><span data-ttu-id="6b55d-143">Beispiel für ein Verbindungsgruppen-XML-Dokument mit optionalen Paketen:</span><span class="sxs-lookup"><span data-stu-id="6b55d-143">Example connection group XML document with optional packages:</span></span></strong></p>
<pre class="syntax" space="preserve"><code>&lt;?xml version=&quot;1.0&quot; ?&gt;
&lt;AppConnectionGroup
   xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;
   AppConnectionGroupId=&quot;8105CCD5-244B-4BA1-8888-E321E688D2CB&quot;
   VersionId=&quot;84CE3797-F1CB-4475-A223-757918929EB4&quot;
   DisplayName=&quot;Contoso Software Connection Group&quot; &gt;
&lt;Packages&gt;
&lt;Package
   PackageId=&quot;7735d1a8-5ef9-4df9-a1cf-3aa92ef54fe7&quot;
   VersionId=&quot;ec560d6f-e62e-48eb-a9e5-7c52a8c2e149&quot;
   DisplayName=&quot;Contoso Business Manager&quot;
/&gt;

&lt;Package
   PackageId=&quot;fc6fe0f7-be3d-4643-b37d-fc3f62d4dd5c&quot;
   VersionId=&quot;c67a71cd-3542-4a48-93e8-20c643c50970&quot;
   DisplayName=&quot;Contoso Forms&quot;
   IsOptional=&quot;false&quot;
/&gt;

&lt;Package
   PackageId=&quot;8f6301a5-4348-4039-9560-b27a5bb72711&quot;
   VersionId=&quot;6c694b45-3e19-46c6-a327-d159aa39e1d2&quot;
   DisplayName=&quot;Contoso Tax&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;Package
   PackageId=&quot;89d701bc-d507-4299-b6b6-000000003472&quot;
   VersionId=&quot;*&quot;
   DisplayName=&quot;Contoso Accounts&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;/Packages&gt;
&lt;/AppConnectionGroup&gt;</code></pre></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6b55d-144">Mit älteren Versionen als App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="6b55d-144">With versions earlier than App-V 5.0 SP3</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6b55d-145">Sie mussten viele Verbindungsgruppen erstellen, um bestimmte Anwendungen und Plug-in-Kombinationen für bestimmte Benutzer verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="6b55d-145">You had to create many connection groups to make specific application and plug-in combinations available to specific users.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-unpub-del-optl-pkg"></a><span data-ttu-id="6b55d-146">Aufheben der Veröffentlichung oder Löschen eines optionalen Pakets oder Aufheben der Veröffentlichung eines optionalen Pakets und erneutes veröffentlichen, ohne die Verbindungsgruppe zu ändern</span><span class="sxs-lookup"><span data-stu-id="6b55d-146">Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6b55d-147">Aufgabenbeschreibung</span><span class="sxs-lookup"><span data-stu-id="6b55d-147">Task description</span></span></th>
<th align="left"><span data-ttu-id="6b55d-148">Durchführen der Aufgabe</span><span class="sxs-lookup"><span data-stu-id="6b55d-148">How to perform the task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6b55d-149">Mit App-v 5,0 SP3 und App-v 5,1</span><span class="sxs-lookup"><span data-stu-id="6b55d-149">With App-V 5.0 SP3 and App-V 5.1</span></span></strong></p>
<p><span data-ttu-id="6b55d-150">Sie können ein optionales Paket, das sich in einer Verbindungsgruppe befindet, unveröffentlicht, löschen oder erneut veröffentlichen, ohne die Verbindungsgruppe auf dem App-V-Client deaktivieren oder erneut aktivieren zu müssen.</span><span class="sxs-lookup"><span data-stu-id="6b55d-150">You can unpublish, delete, or republish an optional package, which is in a connection group, without having to disable or re-enable the connection group on the App-V Client.</span></span></p>
<p><span data-ttu-id="6b55d-151">Sie können auch die Veröffentlichung eines optionalen Pakets aufheben und es später erneut veröffentlichen, ohne die Verbindungsgruppe deaktivieren oder erneut veröffentlichen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="6b55d-151">You can also unpublish an optional package and republish it later without having to disable or republish the connection group.</span></span></p>
<p><strong><span data-ttu-id="6b55d-152">Beispiel </strong> : Wenn Sie ein optionales Paket veröffentlichen, das ein Microsoft Office-Plug-in enthält, und Sie das Plug-in entfernen möchten, können Sie die Veröffentlichung des Pakets aufheben, ohne die Verbindungsgruppe deaktivieren zu müssen.</span><span class="sxs-lookup"><span data-stu-id="6b55d-152">Example</strong>: If you publish an optional package that contains a Microsoft Office plug-in, and you want to remove the plug-in, you can unpublish the package without having to disable the connection group.</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6b55d-153">Methode</span><span class="sxs-lookup"><span data-stu-id="6b55d-153">Method</span></span></th>
<th align="left"><span data-ttu-id="6b55d-154">Schritte</span><span class="sxs-lookup"><span data-stu-id="6b55d-154">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b55d-155">App-V Server – Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="6b55d-155">App-V Server – Management Console</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="6b55d-156">So heben Sie die Veröffentlichung des Pakets auf: Wählen Sie in der Verwaltungskonsole die Option Pakete auswählen aus <strong> </strong> , klicken oder klicken Sie mit der rechten Maustaste auf das Paket, dessen Veröffentlichung Sie aufheben möchten, und klicken Sie auf Veröffentlichung aufheben <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="6b55d-156">To unpublish the package: In the Management Console, select elect the <strong>PACKAGES</strong> page, click or right-click the package that you want to unpublish, and click <strong>Unpublish</strong>.</span></span></p></li>
<li><p><span data-ttu-id="6b55d-157">So entfernen Sie ein optionales Paket aus einer Verbindungsgruppe: Wählen Sie auf der <strong> Seite Verbindungsgruppen das Paket aus, das </strong> Sie entfernen möchten, und klicken Sie auf den Pfeil nach rechts, um das Paket aus dem Bereich Verbindungsgruppe unten links zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="6b55d-157">To remove an optional package from a connection group: On the <strong>CONNECTION GROUPS</strong> page, select the package that you want to remove, and click the right arrow to remove the package from the connection group pane on the bottom left.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b55d-158">App-V-Client auf einem eigenständigen Computer</span><span class="sxs-lookup"><span data-stu-id="6b55d-158">App-V Client on a Stand-alone computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b55d-159">Verwenden Sie die folgenden vorhandenen Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6b55d-159">Use the following existing cmdlets:</span></span></p>
<ul>
<li><p><span data-ttu-id="6b55d-160">Veröffentlichung aufheben – AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="6b55d-160">Unpublish-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="6b55d-161">Remove-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="6b55d-161">Remove-AppvClientPackage</span></span></p></li>
</ul>
<p><span data-ttu-id="6b55d-162">Weitere Informationen finden Sie unter <a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"> Verwalten von App-V 5,1-Paketen, die mit PowerShell auf einem eigenständigen Computer ausgeführt werden </a> .</span><span class="sxs-lookup"><span data-stu-id="6b55d-162">For more information, see <a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6b55d-163">Mit älteren Versionen als App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="6b55d-163">With versions earlier than App-V 5.0 SP3</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6b55d-164">Sie mussten Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="6b55d-164">You had to:</span></span></p>
<ol>
<li><p><span data-ttu-id="6b55d-165">Entfernen Sie die Verbindungsgruppe von jedem App-V-Client Computer, auf dem Sie aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="6b55d-165">Remove the connection group from each App-V Client computer where it was enabled.</span></span></p></li>
<li><p><span data-ttu-id="6b55d-166">Heben Sie die Veröffentlichung des Pakets auf.</span><span class="sxs-lookup"><span data-stu-id="6b55d-166">Unpublish the package.</span></span></p></li>
<li><p><span data-ttu-id="6b55d-167">Entfernen Sie das Paket aus der Definition der Verbindungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="6b55d-167">Remove the package from the connection group’s definition.</span></span></p></li>
<li><p><span data-ttu-id="6b55d-168">Veröffentlichen Sie die Verbindungsgruppe erneut.</span><span class="sxs-lookup"><span data-stu-id="6b55d-168">Republish the connection group.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqs-using-cg"></a><span data-ttu-id="6b55d-169">Voraussetzungen für die Verwendung optionaler Pakete in Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="6b55d-169">Requirements for using optional packages in connection groups</span></span>


<span data-ttu-id="6b55d-170">Überprüfen Sie die folgenden Anforderungen, bevor Sie optionale Pakete in Verbindungsgruppen verwenden:</span><span class="sxs-lookup"><span data-stu-id="6b55d-170">Review the following requirements before using optional packages in connection groups:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6b55d-171">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b55d-171">Requirement</span></span></th>
<th align="left"><span data-ttu-id="6b55d-172">Details</span><span class="sxs-lookup"><span data-stu-id="6b55d-172">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b55d-173">Verbindungsgruppen müssen mindestens ein nicht optionales Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="6b55d-173">Connection groups must contain at least one non-optional package.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="6b55d-174">Überprüfen Sie sorgfältig, ob Sie diese Anforderung erfüllen, da der App-V-Server und das PowerShell-Cmdlet nicht überprüfen, ob die Anforderung erfüllt wurde.</span><span class="sxs-lookup"><span data-stu-id="6b55d-174">Check carefully that you meet this requirement, as the App-V Server and the PowerShell cmdlet don’t validate that the requirement has been met.</span></span></p></li>
<li><p><span data-ttu-id="6b55d-175">Wenn Sie versehentlich eine Verbindungsgruppe erstellen, die nicht mindestens ein nicht optionales Paket enthält, und der Endbenutzer versucht, eine verpackte Anwendung in dieser Verbindungsgruppe zu öffnen, schlägt die Verbindungsgruppe fehl.</span><span class="sxs-lookup"><span data-stu-id="6b55d-175">If you accidentally create a connection group that does not contain at least one non-optional package, and the end user tries to open a packaged application in that connection group, the connection group will fail.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p><span data-ttu-id="6b55d-176">Von Benutzern veröffentlichte Verbindungsgruppen können Pakete enthalten, die Global oder für den Benutzer veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="6b55d-176">User-published connection groups can contain packages that are published globally or to the user.</span></span></p></li>
<li><p><span data-ttu-id="6b55d-177">Global veröffentlichte Verbindungsgruppen dürfen nur global veröffentlichte Pakete enthalten.</span><span class="sxs-lookup"><span data-stu-id="6b55d-177">Globally published connection groups must contain only globally published packages.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="6b55d-178">Global veröffentlichte Verbindungsgruppen müssen Pakete enthalten, die Global veröffentlicht werden, um sicherzustellen, dass die Pakete beim Starten der virtuellen Umgebung der Verbindungsgruppe verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="6b55d-178">Globally published connection groups must contain packages that are published globally to ensure that the packages will be available when starting the connection group’s virtual environment.</span></span></p>
<p><span data-ttu-id="6b55d-179">Wenn Sie versuchen, Global veröffentlichte Verbindungsgruppen hinzuzufügen oder zu aktivieren, die von Benutzern veröffentlichte Pakete enthalten, schlägt die Verbindungsgruppe fehl.</span><span class="sxs-lookup"><span data-stu-id="6b55d-179">If you try to add or enable globally published connection groups that contain user-published packages, the connection group will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b55d-180">Sie müssen alle nicht optionalen Pakete veröffentlichen, bevor Sie die Verbindungsgruppe veröffentlichen, die diese Pakete enthält.</span><span class="sxs-lookup"><span data-stu-id="6b55d-180">You must publish all non-optional packages before publishing the connection group that contains those packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b55d-181">Die virtuelle Umgebung einer Verbindungsgruppe kann nicht gestartet werden, wenn nicht optionale Pakete fehlen.</span><span class="sxs-lookup"><span data-stu-id="6b55d-181">A connection group’s virtual environment cannot start if any non-optional packages are missing.</span></span></p>
<p><span data-ttu-id="6b55d-182">Der App-V-Client kann keine Verbindungsgruppe hinzufügen oder aktivieren, wenn nicht optionale Pakete nicht veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="6b55d-182">The App-V Client fails to add or enable a connection group if any non-optional packages have not been published.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b55d-183">Bevor Sie die Veröffentlichung eines Global veröffentlichten Pakets aufheben, stellen Sie sicher, dass die Verbindungsgruppen, die für alle Benutzer auf diesem Computer berechtigt sind, das Paket nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="6b55d-183">Before you unpublish a globally published package, ensure that the connection groups that are entitled to all the users on that computer no longer require the package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b55d-184">Das System überprüft nicht, ob das Paket Teil der Verbindungsgruppe eines anderen Benutzers ist.</span><span class="sxs-lookup"><span data-stu-id="6b55d-184">The system does not check whether the package is part of another user’s connection group.</span></span> <span data-ttu-id="6b55d-185">Wenn die Veröffentlichung eines globalen Pakets aufgehoben wird, ist es für jeden Benutzer auf diesem Computer nicht mehr verfügbar, stellen Sie daher sicher, dass die Verbindungsgruppen des Benutzers das Paket nicht mehr enthalten, oder machen Sie das Paket optional.</span><span class="sxs-lookup"><span data-stu-id="6b55d-185">Unpublishing a global package will make it unavailable to every user on that computer, so make sure that each user’s connection groups no longer contain the package, or alternatively make the package optional.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="6b55d-186">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="6b55d-186">Related topics</span></span>


[<span data-ttu-id="6b55d-187">Verwalten von Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="6b55d-187">Managing Connection Groups</span></span>](managing-connection-groups51.md)

 

 




