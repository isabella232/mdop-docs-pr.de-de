---
title: CONFIGURE PACKAGE
description: CONFIGURE PACKAGE
author: dansimp
ms.assetid: acc7eaa8-6ada-47b9-a655-2ca2537605b9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc8b315b68349cc9834316786b0bf15d4ac3c5cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807871"
---
# <span data-ttu-id="2f7a8-103">CONFIGURE PACKAGE</span><span class="sxs-lookup"><span data-stu-id="2f7a8-103">CONFIGURE PACKAGE</span></span>


<span data-ttu-id="2f7a8-104">Ermöglicht dem Benutzer das Ändern einer Paket Manifestdatei, einer Paketquelle, eines Load Trigger-Typs oder eines Lade Ziels für ein Paket.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-104">Enables the user to change a package manifest file, package source, load trigger types, or load target for a package.</span></span>

`SFTMIME CONFIGURE PACKAGE:package-name [/MANIFEST manifest-path]                 [/OVERRIDEURL url] [/AUTOLOADNEVER] [/AUTOLOADONREFRESH]                 [/AUTOLOADONLOGIN] [/AUTOLOADONLAUNCH]                 [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/LOG log-pathname | /CONSOLE | /GUI]                 [/NO-UPDATE-FTA-SHORTCUT {TRUE|FALSE} {/GLOBAL}]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f7a8-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f7a8-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="2f7a8-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f7a8-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f7a8-107">Paket: &lt; Package-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="2f7a8-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f7a8-108">Benutzersicht barer und benutzerfreundlicher Name für das Paket.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-108">User-visible and user-friendly name for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f7a8-109">/Manifest &lt; -Manifest-Pfad&gt;</span><span class="sxs-lookup"><span data-stu-id="2f7a8-109">/MANIFEST &lt;manifest-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f7a8-110">Der Pfad oder die URL der Manifestdatei, in der die im Paket enthaltenen Anwendungen sowie alle Veröffentlichungsinformationen aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-110">The path or URL of the manifest file that lists the applications included in the package and all of their publishing information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f7a8-111">/OVERRIDEURL- &lt; URL&gt;</span><span class="sxs-lookup"><span data-stu-id="2f7a8-111">/OVERRIDEURL &lt;URL&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f7a8-112">Der Speicherort der SFT-Datei des Pakets.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-112">The location of the package's SFT file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f7a8-113">/AUTOLOADNEVER</span><span class="sxs-lookup"><span data-stu-id="2f7a8-113">/AUTOLOADNEVER</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f7a8-114">Das Laden des Hintergrunds ist für das Paket deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-114">Background loading is turned off for the package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f7a8-115">/AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="2f7a8-115">/AUTOLOADONREFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f7a8-116">Das Laden des Hintergrunds wird nach einer Veröffentlichungsaktualisierung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-116">Background loading is performed after a publishing refresh.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f7a8-117">/AUTOLOADONLOGIN</span><span class="sxs-lookup"><span data-stu-id="2f7a8-117">/AUTOLOADONLOGIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f7a8-118">Das Laden des Hintergrunds wird durchgeführt, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-118">Background loading is performed when a user logs in.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f7a8-119">/AUTOLOADONLAUNCH</span><span class="sxs-lookup"><span data-stu-id="2f7a8-119">/AUTOLOADONLAUNCH</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f7a8-120">Das Laden des Hintergrunds wird ausgeführt, nachdem ein Benutzer eine Anwendung aus dem Paket gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-120">Background loading is performed after a user starts an application from the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f7a8-121">/AUTOLOADTARGET- &lt; Ziel&gt;</span><span class="sxs-lookup"><span data-stu-id="2f7a8-121">/AUTOLOADTARGET &lt;target&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f7a8-122">Gibt an, welche Anwendungen aus dem Paket automatisch geladen werden.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-122">Indicates which applications from the package will be autoloaded.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f7a8-123">Keine</span><span class="sxs-lookup"><span data-stu-id="2f7a8-123">NONE</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f7a8-124">Trotz vorhanden sein von/AUTOLOADONxxx-Flags wird kein Autoloading durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-124">No autoloading will be performed despite the presence of any /AUTOLOADONxxx flags.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f7a8-125">Alle</span><span class="sxs-lookup"><span data-stu-id="2f7a8-125">ALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f7a8-126">Wenn ein automatischer Trigger aktiviert ist, werden alle Anwendungen im Paket in den Cache geladen, unabhängig davon, ob Sie jemals gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-126">If an autoload trigger is enabled, all applications in the package will be loaded into cache regardless of whether they have ever been launched.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f7a8-127">PREVUSED</span><span class="sxs-lookup"><span data-stu-id="2f7a8-127">PREVUSED</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f7a8-128">Wenn ein automatischer Trigger aktiviert ist, wird das Paket geladen, wenn Anwendungen in diesem Paket zuvor von einem Benutzer gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-128">If an autoload trigger is enabled, the package will load if any applications in this package have previously been started by a user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f7a8-129">/Log</span><span class="sxs-lookup"><span data-stu-id="2f7a8-129">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f7a8-130">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-130">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f7a8-131">/Console</span><span class="sxs-lookup"><span data-stu-id="2f7a8-131">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f7a8-132">Wenn angegeben, wird die Ausgabe im aktiven Konsolenfenster angezeigt (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="2f7a8-132">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f7a8-133">/GUI</span><span class="sxs-lookup"><span data-stu-id="2f7a8-133">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f7a8-134">Wenn angegeben, wird die Ausgabe in einem Windows-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-134">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2f7a8-135">Für Version 4.6 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-135">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f7a8-136">/LOGU</span><span class="sxs-lookup"><span data-stu-id="2f7a8-136">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f7a8-137">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-137">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2f7a8-138">Für Version 4.6 SP2 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-138">For version4.6 SP2, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f7a8-139">[/no-Update-FTA-Shortcut {true | FALSE} {/Global}]</span><span class="sxs-lookup"><span data-stu-id="2f7a8-139">[/NO-UPDATE-FTA-SHORTCUT {TRUE|FALSE} {/GLOBAL}]</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f7a8-140">Wenn der Wert auf true festgelegt ist, wird für das Paket entweder pro Benutzer oder Global ein Registrierungswert erstellt, wenn das/Global-Flag angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-140">If set to TRUE, a registry value is created for the package, either per user, or globally if the /GLOBAL flag is specified.</span></span></p>
<p><span data-ttu-id="2f7a8-141">Wenn Sie auf false festgelegt ist, wird der Registrierungswert entfernt, und die Dateitypen Zuordnungen (FTA) für das Paket werden neu installiert.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-141">If set to FALSE, the registry value is removed and the file type associations (FTA) for the package are reinstalled.</span></span></p>
<p><span data-ttu-id="2f7a8-142">Wenn keine Angabe erfolgt, tritt normales FTA-und Verknüpfungs Veröffentlichungsverhalten auf.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-142">If not specified, normal FTA and shortcut publishing behavior occurs.</span></span> <span data-ttu-id="2f7a8-143">Wenn Sie spätere Veröffentlichungs Aktualisierungsvorgänge auf dem App-V 4,6 SP2-Client ausführen, werden die Verknüpfungen und FTA für Pakete, deren Registrierungswert festgesetzt ist, nicht geändert, und die Verknüpfungen und Freihandelsabkommen werden beim Systemstart oder bei der Benutzeranmeldung nicht registriert, es sei denn, Sie setzen das Flag zurück.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-143">If you perform any subsequent publishing refresh operations on the App-V 4.6 SP2 client, the shortcuts and FTAs for packages that have this registry value set will not be changed, and the shortcuts and FTAs will not be registered at system startup or user login unless you reset the flag.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f7a8-144">/Global</span><span class="sxs-lookup"><span data-stu-id="2f7a8-144">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f7a8-145">Funktioniert in Verbindung mit dem/No-Update-FTA-Shortcut-Flag.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-145">Works in conjunction with the /NO-UPDATE-FTA-SHORTCUT flag.</span></span> <span data-ttu-id="2f7a8-146">Wenn das/Global-Flag vorhanden ist, gibt es an, dass ein Registrierungswert für dieses Paket für alle Benutzer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-146">If the /GLOBAL flag is present, it indicates that a registry value will be created for that package for all users.</span></span> <span data-ttu-id="2f7a8-147">Standardmäßig wird der Registrierungswert nur für diesen Benutzer erstellt.</span><span class="sxs-lookup"><span data-stu-id="2f7a8-147">By default, the registry value is created only for this user.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="2f7a8-148">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2f7a8-148">Related topics</span></span>


[<span data-ttu-id="2f7a8-149">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="2f7a8-149">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





