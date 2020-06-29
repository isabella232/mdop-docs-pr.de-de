---
title: Ausführen einer lokal installierten Anwendung in einer virtuellen Umgebung mit virtualisierter Anwendungen
description: Ausführen einer lokal installierten Anwendung in einer virtuellen Umgebung mit virtualisierter Anwendungen
author: dansimp
ms.assetid: a8affa46-f1f7-416c-8125-9595cfbfdbc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 10c0f3f3c8a1b88cf1a98fd64fe8f7f49b597a91
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804883"
---
# <span data-ttu-id="9f1d8-103">Ausführen einer lokal installierten Anwendung in einer virtuellen Umgebung mit virtualisierter Anwendungen</span><span class="sxs-lookup"><span data-stu-id="9f1d8-103">Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications</span></span>


<span data-ttu-id="9f1d8-104">Sie können eine lokal installierte Anwendung in einer virtuellen Umgebung neben Anwendungen ausführen, die mit Microsoft Application Virtualization (App-V) virtualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-104">You can run a locally installed application in a virtual environment, alongside applications that have been virtualized by using Microsoft Application Virtualization (App-V).</span></span> <span data-ttu-id="9f1d8-105">Möglicherweise möchten Sie dies tun, wenn Sie:</span><span class="sxs-lookup"><span data-stu-id="9f1d8-105">You might want to do this if you:</span></span>

-   <span data-ttu-id="9f1d8-106">Sie möchten eine Anwendung lokal auf Clientcomputern installieren und ausführen, möchten aber bestimmte Plug-ins, die mit dieser lokalen Anwendung funktionieren, virtualisieren und ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-106">Want to install and run an application locally on client computers, but want to virtualize and run specific plug-ins that work with that local application.</span></span>

-   <span data-ttu-id="9f1d8-107">Behandeln ein App-v-Clientpaket und möchten eine lokale Anwendung in der virtuellen App-v-Umgebung öffnen.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-107">Are troubleshooting an App-V client package and want to open a local application within the App-V virtual environment.</span></span>

<span data-ttu-id="9f1d8-108">Verwenden Sie eine der folgenden Methoden, um eine lokale Anwendung innerhalb der virtuellen App-V-Umgebung zu öffnen:</span><span class="sxs-lookup"><span data-stu-id="9f1d8-108">Use any of the following methods to open a local application inside the App-V virtual environment:</span></span>

-   [<span data-ttu-id="9f1d8-109">RunVirtual-Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="9f1d8-109">RunVirtual registry key</span></span>](#bkmk-runvirtual-regkey)

-   [<span data-ttu-id="9f1d8-110">Cmdlet "Get-AppvClientPackage PowerShell"</span><span class="sxs-lookup"><span data-stu-id="9f1d8-110">Get-AppvClientPackage PowerShell cmdlet</span></span>](#bkmk-get-appvclientpackage-posh)

-   [<span data-ttu-id="9f1d8-111">Befehlszeilen Schalter/appvpid: &lt; PID&gt;</span><span class="sxs-lookup"><span data-stu-id="9f1d8-111">Command line switch /appvpid:&lt;PID&gt;</span></span>](#bkmk-cl-switch-appvpid)

-   [<span data-ttu-id="9f1d8-112">Befehlszeilen-Hook-Schalter/appvve: &lt; GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="9f1d8-112">Command line hook switch /appvve:&lt;GUID&gt;</span></span>](#bkmk-cl-hook-switch-appvve)

<span data-ttu-id="9f1d8-113">Jede Methode erfüllt im Wesentlichen dieselbe Aufgabe, aber einige Methoden sind möglicherweise für einige Anwendungen besser geeignet als für andere, je nachdem, ob die virtualisierte Anwendung bereits ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-113">Each method accomplishes essentially the same task, but some methods may be better suited for some applications than others, depending on whether the virtualized application is already running.</span></span>

## <a href="" id="bkmk-runvirtual-regkey"></a><span data-ttu-id="9f1d8-114">RunVirtual-Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="9f1d8-114">RunVirtual registry key</span></span>


<span data-ttu-id="9f1d8-115">Wenn Sie eine lokal installierte Anwendung zu einem Paket oder zur virtuellen Umgebung einer Verbindungsgruppe hinzufügen möchten, fügen Sie dem `RunVirtual` Registrierungsschlüssel im Registrierungs-Editor einen Unterschlüssel hinzu, wie in den folgenden Abschnitten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-115">To add a locally installed application to a package or to a connection group’s virtual environment, you add a subkey to the `RunVirtual` registry key in the Registry Editor, as described in the following sections.</span></span>

<span data-ttu-id="9f1d8-116">Es ist keine Gruppenrichtlinieneinstellung verfügbar, um diesen Registrierungsschlüssel zu verwalten, daher müssen Sie System Center Configuration Manager oder ein anderes ESD-System (Electronic Software Distribution) verwenden oder die Registrierung manuell bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-116">There is no Group Policy setting available to manage this registry key, so you have to use System Center Configuration Manager or another electronic software distribution (ESD) system, or manually edit the registry.</span></span>

### <a href="" id="bkmk-"></a><span data-ttu-id="9f1d8-117">Unterstützte Methoden zum Veröffentlichen von Paketen bei Verwendung von RunVirtual</span><span class="sxs-lookup"><span data-stu-id="9f1d8-117">Supported methods of publishing packages when using RunVirtual</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9f1d8-118">App-V-Version</span><span class="sxs-lookup"><span data-stu-id="9f1d8-118">App-V version</span></span></th>
<th align="left"><span data-ttu-id="9f1d8-119">Unterstützte Veröffentlichungsmethoden</span><span class="sxs-lookup"><span data-stu-id="9f1d8-119">Supported publishing methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9f1d8-120">App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="9f1d8-120">App-V 5.0 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f1d8-121">Global oder für den Benutzer veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="9f1d8-121">Published globally or to the user</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9f1d8-122">App-v 5,0 über APP-v 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="9f1d8-122">App-V 5.0 through App-V 5.0 SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f1d8-123">Nur global veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="9f1d8-123">Published globally only</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="9f1d8-124">Schritte zum Erstellen des Unterschlüssels</span><span class="sxs-lookup"><span data-stu-id="9f1d8-124">Steps to create the subkey</span></span>

1.  <span data-ttu-id="9f1d8-125">Erstellen Sie mithilfe der Informationen in der folgenden Tabelle einen neuen Registrierungsschlüssel mit dem Namen der ausführbaren Datei, beispielsweise **MyApp.exe**.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-125">Using the information in the following table, create a new registry key using the name of the executable file, for example, **MyApp.exe**.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="9f1d8-126">Paket Veröffentlichungsmethode</span><span class="sxs-lookup"><span data-stu-id="9f1d8-126">Package publishing method</span></span></th>
    <th align="left"><span data-ttu-id="9f1d8-127">Wo soll der Registrierungsschlüssel erstellt werden?</span><span class="sxs-lookup"><span data-stu-id="9f1d8-127">Where to create the registry key</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="9f1d8-128">Global veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="9f1d8-128">Published globally</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9f1d8-129">HKEY_LOCAL_MACHINE \software\microsoft\appv\client\runvirtual</span><span class="sxs-lookup"><span data-stu-id="9f1d8-129">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual</span></span></p>
    <p><strong><span data-ttu-id="9f1d8-130">Beispiel </strong> : HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="9f1d8-130">Example</strong>: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="9f1d8-131">Für den Benutzer veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="9f1d8-131">Published to the user</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9f1d8-132">HKEY_CURRENT_USER \software\microsoft\appv\client\runvirtual</span><span class="sxs-lookup"><span data-stu-id="9f1d8-132">HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</span></span></p>
    <p><strong><span data-ttu-id="9f1d8-133">Beispiel </strong> : HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="9f1d8-133">Example</strong>: HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="9f1d8-134">Die Verbindungsgruppe kann Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="9f1d8-134">Connection group can contain:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="9f1d8-135">Pakete, die nur global oder nur für den Benutzer veröffentlicht werden</span><span class="sxs-lookup"><span data-stu-id="9f1d8-135">Packages that are published just globally or just to the user</span></span></p></li>
    <li><p><span data-ttu-id="9f1d8-136">Pakete, die Global und für den Benutzer veröffentlicht werden</span><span class="sxs-lookup"><span data-stu-id="9f1d8-136">Packages that are published globally and to the user</span></span></p></li>
    </ul></td>
    <td align="left"><p><span data-ttu-id="9f1d8-137">Entweder HKEY_LOCAL_MACHINE oder HKEY_CURRENT_USER-Taste, aber alle der folgenden Bedingungen müssen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="9f1d8-137">Either HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER key, but all of the following must be true:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="9f1d8-138">Wenn Sie mehrere Pakete in die virtuelle Umgebung einbeziehen möchten, müssen Sie Sie in eine aktivierte Verbindungsgruppe einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-138">If you want to include multiple packages in the virtual environment, you must include them in an enabled connection group.</span></span></p></li>
    <li><p><span data-ttu-id="9f1d8-139">Erstellen Sie nur einen Unterschlüssel für eines der Pakete in der Verbindungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-139">Create only one subkey for one of the packages in the connection group.</span></span> <span data-ttu-id="9f1d8-140">Wenn Sie beispielsweise ein Paket haben, das Global veröffentlicht wird, und ein weiteres Paket, das für den Benutzer veröffentlicht wird, erstellen Sie einen Unterschlüssel für eines der beiden Pakete, aber nicht für beide.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-140">If, for example, you have one package that is published globally, and another package that is published to the user, you create a subkey for either of these packages, but not both.</span></span> <span data-ttu-id="9f1d8-141">Obwohl Sie einen Unterschlüssel nur für eines der Pakete erstellen, sind alle Pakete in der Verbindungsgruppe sowie die lokale Anwendung in der virtuellen Umgebung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-141">Although you create a subkey for only one of the packages, all of the packages in the connection group, plus the local application, will be available in the virtual environment.</span></span></p></li>
    <li><p><span data-ttu-id="9f1d8-142">Der Schlüssel, unter dem Sie den Unterschlüssel erstellen, muss mit der Veröffentlichungsmethode übereinstimmen, die Sie für das Paket verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-142">The key under which you create the subkey must match the publishing method you used for the package.</span></span></p>
    <p><span data-ttu-id="9f1d8-143">Wenn Sie das Paket beispielsweise für den Benutzer veröffentlicht haben, müssen Sie den Unterschlüssel erstellen <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</code> .</span><span class="sxs-lookup"><span data-stu-id="9f1d8-143">For example, if you published the package to the user, you must create the subkey under <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</code>.</span></span></p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

     

2.  <span data-ttu-id="9f1d8-144">Setzen Sie den Wert des neuen Registrierungsunterschlüssels auf die Paket-und Versions-Nr des Pakets, wobei die Werte durch einen Unterstrich voneinander getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-144">Set the new registry subkey’s value to the PackageId and VersionId of the package, separating the values with an underscore.</span></span>

    <span data-ttu-id="9f1d8-145">**Syntax**: &lt; Paket-Nr &gt; \ _ &lt; Version-Nr&gt;</span><span class="sxs-lookup"><span data-stu-id="9f1d8-145">**Syntax**: &lt;PackageId&gt;\_&lt;VersionId&gt;</span></span>

    <span data-ttu-id="9f1d8-146">**Beispiel**: 4c909996-AFC9-4352-b606-0b74542a09c1 \ _be463724-Oct1-48f1-8604-c4bd7ca92fa</span><span class="sxs-lookup"><span data-stu-id="9f1d8-146">**Example**: 4c909996-afc9-4352-b606-0b74542a09c1\_be463724-Oct1-48f1-8604-c4bd7ca92fa</span></span>

    <span data-ttu-id="9f1d8-147">Die Anwendung im vorherigen Beispiel würde eine Registrierungsexport Datei (reg-Datei) wie die folgende erstellen:</span><span class="sxs-lookup"><span data-stu-id="9f1d8-147">The application in the previous example would produce a registry export file (.reg file) like the following:</span></span>

    ``` syntax
    Windows Registry Editor Version 5.00 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual] 
    @="" 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe] 
    @="aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-555555555
    ```

## <a href="" id="bkmk-get-appvclientpackage-posh"></a><span data-ttu-id="9f1d8-148">Cmdlet "Get-AppvClientPackage PowerShell"</span><span class="sxs-lookup"><span data-stu-id="9f1d8-148">Get-AppvClientPackage PowerShell cmdlet</span></span>


<span data-ttu-id="9f1d8-149">Sie können das Cmdlet **Start-AppVVirtualProcess** verwenden, um den Paketnamen abzurufen und einen Prozess in der virtuellen Umgebung des angegebenen Pakets zu starten.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-149">You can use the **Start-AppVVirtualProcess** cmdlet to retrieve the package name and then start a process within the specified package's virtual environment.</span></span> <span data-ttu-id="9f1d8-150">Mit dieser Methode können Sie einen beliebigen Befehl im Kontext eines App-V-Pakets starten, unabhängig davon, ob das Paket gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-150">This method lets you launch any command within the context of an App-V package, regardless of whether the package is currently running.</span></span>

<span data-ttu-id="9f1d8-151">Verwenden Sie die folgende Beispielsyntax, und ersetzen Sie den Namen Ihres Pakets für \*\* &lt; Paket &gt; \*\*:</span><span class="sxs-lookup"><span data-stu-id="9f1d8-151">Use the following example syntax, and substitute the name of your package for **&lt;Package&gt;**:</span></span>

`$AppVName = Get-AppvClientPackage <Package>`

`Start-AppvVirtualProcess -AppvClientObject $AppVName cmd.exe`

<span data-ttu-id="9f1d8-152">Wenn Sie den genauen Namen Ihres Pakets nicht kennen, können Sie die Befehlszeile **Get-AppvClientPackage \ \* executable\\**verwenden <em> , wobei \*\*Executable </em> \* der Name der Anwendung ist, beispielsweise: Get-AppvClientPackage \ \* Word \ \*.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-152">If you don’t know the exact name of your package, you can use the command line **Get-AppvClientPackage \*executable\\**<em>, where \**executable</em>* is the name of the application, for example: Get-AppvClientPackage \*Word\*.</span></span>

## <a href="" id="bkmk-cl-switch-appvpid"></a><span data-ttu-id="9f1d8-153">Befehlszeilen Schalter/appvpid: &lt; PID&gt;</span><span class="sxs-lookup"><span data-stu-id="9f1d8-153">Command line switch /appvpid:&lt;PID&gt;</span></span>


<span data-ttu-id="9f1d8-154">Sie können den \*\*/appvpid: &lt; PID &gt; \*\* -Schalter auf einen beliebigen Befehl anwenden, wodurch dieser Befehl innerhalb eines virtuellen Prozesses ausgeführt werden kann, den Sie durch Angabe der Prozess-ID (PID) auswählen.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-154">You can apply the **/appvpid:&lt;PID&gt;** switch to any command, which enables that command to run within a virtual process that you select by specifying its process ID (PID).</span></span> <span data-ttu-id="9f1d8-155">Mit dieser Methode wird die neue ausführbare Datei in derselben App-V-Umgebung wie eine ausführbare Datei gestartet, die bereits ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-155">Using this method launches the new executable in the same App-V environment as an executable that is already running.</span></span>

<span data-ttu-id="9f1d8-156">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9f1d8-156">Example:</span></span> `cmd.exe /appvpid:8108`

<span data-ttu-id="9f1d8-157">Um die Prozess-ID (PID) des App-V-Prozesses zu finden, führen Sie den Befehl **tasklist.exe** über eine Eingabeaufforderung mit erhöhten Rechten aus.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-157">To find the process ID (PID) of your App-V process, run the command **tasklist.exe** from an elevated command prompt.</span></span>

## <a href="" id="bkmk-cl-hook-switch-appvve"></a><span data-ttu-id="9f1d8-158">Befehlszeilen-Hook-Schalter/appvve: &lt; GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="9f1d8-158">Command line hook switch /appvve:&lt;GUID&gt;</span></span>


<span data-ttu-id="9f1d8-159">Mit dieser Option können Sie einen lokalen Befehl innerhalb der virtuellen Umgebung eines App-V-Pakets ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-159">This switch lets you run a local command within the virtual environment of an App-V package.</span></span> <span data-ttu-id="9f1d8-160">Im Gegensatz zum **/appvid** -Schalter, in dem die virtuelle Umgebung bereits ausgeführt werden muss, können Sie mit dieser Option die virtuelle Umgebung starten.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-160">Unlike the **/appvid** switch, where the virtual environment must already be running, this switch enables you to start the virtual environment.</span></span>

<span data-ttu-id="9f1d8-161">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f1d8-161">Syntax:</span></span> `cmd.exe /appvve:<PACKAGEGUID_VERSIONGUID>`

<span data-ttu-id="9f1d8-162">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9f1d8-162">Example:</span></span> `cmd.exe /appvve:aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-55555555`

<span data-ttu-id="9f1d8-163">Führen Sie das Cmdlet " **Get-AppvClientPackage** " aus, um die Paket-GUID und die Versions-GUID der Anwendung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-163">To get the package GUID and version GUID of your application, run the **Get-AppvClientPackage** cmdlet.</span></span> <span data-ttu-id="9f1d8-164">Verketten Sie den **/appvve** -Schalter mit folgendem:</span><span class="sxs-lookup"><span data-stu-id="9f1d8-164">Concatenate the **/appvve** switch with the following:</span></span>

-   <span data-ttu-id="9f1d8-165">Ein Doppelpunkt</span><span class="sxs-lookup"><span data-stu-id="9f1d8-165">A colon</span></span>

-   <span data-ttu-id="9f1d8-166">Paket-GUID des gewünschten Pakets</span><span class="sxs-lookup"><span data-stu-id="9f1d8-166">Package GUID of the desired package</span></span>

-   <span data-ttu-id="9f1d8-167">Ein Unterstrich</span><span class="sxs-lookup"><span data-stu-id="9f1d8-167">An underscore</span></span>

-   <span data-ttu-id="9f1d8-168">Versions-ID des gewünschten Pakets</span><span class="sxs-lookup"><span data-stu-id="9f1d8-168">Version ID of the desired package</span></span>

<span data-ttu-id="9f1d8-169">Wenn Sie den genauen Namen Ihres Pakets nicht kennen, verwenden Sie die Befehlszeile **Get-AppvClientPackage \ \* executable\\** <em> , wobei \*\*Executable </em> \* der Name der Anwendung ist, beispielsweise: Get-AppvClientPackage \ \* Word \ \*.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-169">If you don’t know the exact name of your package, use the command line **Get-AppvClientPackage \*executable\\**<em>, where \**executable</em>* is the name of the application, for example: Get-AppvClientPackage \*Word\*.</span></span>

<span data-ttu-id="9f1d8-170">Mit dieser Methode können Sie einen beliebigen Befehl im Kontext eines App-V-Pakets starten, unabhängig davon, ob das Paket gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f1d8-170">This method lets you launch any command within the context of an App-V package, regardless of whether the package is currently running.</span></span>






## <span data-ttu-id="9f1d8-171">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9f1d8-171">Related topics</span></span>


[<span data-ttu-id="9f1d8-172">Technische Referenz zu App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="9f1d8-172">Technical Reference for App-V 5.0</span></span>](technical-reference-for-app-v-50.md)

 

 





