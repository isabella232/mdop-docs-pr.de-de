---
title: QUERY OBJ
description: QUERY OBJ
author: dansimp
ms.assetid: 55abf0d1-c779-4172-8357-552ab010933b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328e9feb96c70080531cbbc666d8ff1b86045ba5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806427"
---
# <span data-ttu-id="3d300-103">QUERY OBJ</span><span class="sxs-lookup"><span data-stu-id="3d300-103">QUERY OBJ</span></span>


<span data-ttu-id="3d300-104">Gibt eine durch Tabstopps getrennte Liste der aktuellen Anwendungen, Pakete, Dateitypzuordnungen oder Veröffentlichungsserver zurück.</span><span class="sxs-lookup"><span data-stu-id="3d300-104">Returns a tab-delimited list of current applications, packages, file type associations, or publishing servers.</span></span>

`SFTMIME QUERY OBJ:{APP|PACKAGE|TYPE|SERVER} [/SHORT] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE ]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3d300-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d300-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="3d300-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d300-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d300-107">App</span><span class="sxs-lookup"><span data-stu-id="3d300-107">APP</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d300-108">Gibt eine Liste der Anwendungen zurück.</span><span class="sxs-lookup"><span data-stu-id="3d300-108">Returns a list of applications.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d300-109">Paket</span><span class="sxs-lookup"><span data-stu-id="3d300-109">PACKAGE</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d300-110">Gibt eine Liste der Pakete zurück.</span><span class="sxs-lookup"><span data-stu-id="3d300-110">Returns a list of packages.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d300-111">TYPE</span><span class="sxs-lookup"><span data-stu-id="3d300-111">TYPE</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d300-112">Gibt eine Liste der Dateitypzuordnungen zurück.</span><span class="sxs-lookup"><span data-stu-id="3d300-112">Returns a list of file type associations.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d300-113">Server</span><span class="sxs-lookup"><span data-stu-id="3d300-113">SERVER</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d300-114">Gibt eine Liste der Veröffentlichungsserver zurück.</span><span class="sxs-lookup"><span data-stu-id="3d300-114">Returns a list of publishing servers.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d300-115">/SHORT</span><span class="sxs-lookup"><span data-stu-id="3d300-115">/SHORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d300-116">Gibt eine Liste der Anwendungsnamen, Pakete, Assoziationen oder Servernamen zurück, ohne die vollständigen Eigenschaften der einzelnen anzeigen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3d300-116">Without displaying the full properties of each, returns a list of application names, packages, associations, or server names.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d300-117">/Global</span><span class="sxs-lookup"><span data-stu-id="3d300-117">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d300-118">Gibt für Anwendungen alle bekannten Anwendungen zurück, nicht nur diejenigen, auf die der aktuelle Benutzer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="3d300-118">For applications, returns all known applications instead of only the ones the current user has access to.</span></span> <span data-ttu-id="3d300-119">Gibt für Pakete alle bekannten Pakete anstatt nur diejenigen zurück, auf die der aktuelle Benutzer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="3d300-119">For packages, returns all known packages instead of only the ones the current user has access to.</span></span> <span data-ttu-id="3d300-120">Gibt für Zuordnungen nur Zuordnungen zurück, die für alle Benutzer gelten, nicht für benutzerspezifische.</span><span class="sxs-lookup"><span data-stu-id="3d300-120">For associations, returns only associations that apply to all users, not user-specific ones.</span></span> <span data-ttu-id="3d300-121">Nicht gültig für Server.</span><span class="sxs-lookup"><span data-stu-id="3d300-121">Not valid for servers.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d300-122">/Log</span><span class="sxs-lookup"><span data-stu-id="3d300-122">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d300-123">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="3d300-123">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d300-124">/Console</span><span class="sxs-lookup"><span data-stu-id="3d300-124">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d300-125">Wenn angegeben, wird die Ausgabe im aktiven Konsolenfenster angezeigt (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="3d300-125">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3d300-126">Für Version 4.6 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3d300-126">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d300-127">/LOGU</span><span class="sxs-lookup"><span data-stu-id="3d300-127">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d300-128">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</span><span class="sxs-lookup"><span data-stu-id="3d300-128">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3d300-129">**Hinweis**  In Version 4,6 wurde der Ausgabe von SFTMIME Query obj: App \ [/GLOBAL\] eine neue Spalte hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3d300-129">**Note** In version 4.6, a new column has been added to the output of SFTMIME QUERY OBJ:APP \[/GLOBAL\].</span></span> <span data-ttu-id="3d300-130">Die letzte Spalte der Ausgabe ist ein numerischer Wert, der angibt, ob eine Anwendung veröffentlicht wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="3d300-130">The last column of the output is a numeric value that indicates whether an application is published or not.</span></span>

<span data-ttu-id="3d300-131">Veröffentlicht = 1 bedeutet, dass die Anwendung durch eine Veröffentlichungs Server Aktualisierung veröffentlicht wurde, indem Sie die Anwendung mithilfe einer Windows Installer-Datei (. MSI) oder durch Ausführen eines SFTMIME-Pakets zum Hinzufügen, Konfigurieren des Pakets oder Veröffentlichen eines Pakets mithilfe eines paketmanifests.</span><span class="sxs-lookup"><span data-stu-id="3d300-131">PUBLISHED=1 means the application was published by a Publishing Server refresh, by installing the application by using a Windows Installer file (.MSI), or by running an SFTMIME ADD PACKAGE, CONFIGURE PACKAGE or PUBLISH PACKAGE command by using a package manifest.</span></span>

<span data-ttu-id="3d300-132">Published = 0 bedeutet, dass die Anwendung nicht veröffentlicht wurde oder dass Sie nicht mehr als Ergebnis der Durchführung eines Clear-Vorgangs oder durch Ausführen eines SFTMIME-Befehls "UNPUBLISH" veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="3d300-132">PUBLISHED=0 means the application has not been published or it is no longer published as a result of performing a Clear operation or running an SFTMIME UNPUBLISH command.</span></span>

<span data-ttu-id="3d300-133">Wenn Sie den/Global-Parameter verwenden, ist der veröffentlichte Zustand 1 für Anwendungen, die Global veröffentlicht wurden, und 0 für die Anwendungen, die unter Benutzerkontexten veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="3d300-133">If you use the /GLOBAL parameter, the PUBLISHED state will be 1 for applications that were published globally and 0 for those applications that were published under user contexts.</span></span> <span data-ttu-id="3d300-134">Ohne den/Global-Parameter wird ein veröffentlichter Zustand von 1 für Anwendungen zurückgegeben, die im Kontext des Benutzers veröffentlicht werden, der den Befehl ausführt, und für die Global veröffentlichten Anwendungen wird ein Zustand von 0 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3d300-134">Without the /GLOBAL parameter, a PUBLISHED state of 1 is returned for applications published in the context of the user running the command, and a state of 0 is returned for those applications that are published globally.</span></span>

 

<span data-ttu-id="3d300-135">Mithilfe des SFTMIME-Abfrage-obj-Befehls können Sie Informationen zu allen oben gezeigten Objekten Abfragen – Anwendungen, Pakete, Dateitypzuordnungen und Server.</span><span class="sxs-lookup"><span data-stu-id="3d300-135">The SFTMIME QUERY OBJ command can be used to query for information on all of the objects shown above—applications, packages, file type associations, and servers.</span></span><span data-ttu-id="3d300-136">Im folgenden Beispiel wird gezeigt, wie Sie den SFTMIME-Abfrage-obj-Befehl in ihren normalen Vorgangs Aufgaben verwenden können, indem Sie den Prozess, dem Sie folgen, wenn Sie den OVERRIDEURL-Parameterwert für ein bestimmtes Paket festlegen möchten, um einen neuen Pfad für den Paketinhalt anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3d300-136">To show how you might use the SFTMIME QUERY OBJ command in your normal operations tasks, the following example demonstrates the process you would follow if you wanted to set the OVERRIDEURL parameter value for a specific package to specify a new path to the package content.</span></span> 

1.  <span data-ttu-id="3d300-137">Führen Sie den folgenden Befehl aus, um das Paket zu finden, das Sie konfigurieren möchten:</span><span class="sxs-lookup"><span data-stu-id="3d300-137">To find the package that you want to configure, run the following command:</span></span>

    `SFTMIME QUERY OBJ:PACKAGE`

    <span data-ttu-id="3d300-138">Dieser Befehl gibt jeden gefundenen Paketnamen als GUID in der ersten Ausgabespalte zurück, beispielsweise {AF78ABE1-57D4-4297-89DE-C308684AEDD6}.</span><span class="sxs-lookup"><span data-stu-id="3d300-138">This command returns each discovered package name as a GUID in the first column of output—for example, {AF78ABE1-57D4-4297-89DE-C308684AEDD6}.</span></span>

2.  <span data-ttu-id="3d300-139">Zum Festlegen des OVERRIDEURL-Parameterwerts verwenden Sie den Befehl SFTMIME- [Paket konfigurieren](configure-package.md) .</span><span class="sxs-lookup"><span data-stu-id="3d300-139">To set the OVERRIDEURL parameter value, you use the SFTMIME [CONFIGURE PACKAGE](configure-package.md) command.</span></span> <span data-ttu-id="3d300-140">Wenn Sie beispielsweise den OVERRIDEURL-Wert für dieses Paket auf einen Wert von *\\\\server\\share\\mypackage.SFT*festlegen möchten, verwenden Sie den Befehl SFTMIME-Paket konfigurieren, und geben Sie ihm die ausgewählte Paket-GUID aus der Ausgabe des Befehls SFTMIME Query obj in Schritt 1, gefolgt vom OVERRIDEURL-Parameter und dem neuen Wert, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3d300-140">For example, to set the OVERRIDEURL value for this package to a value of *\\\\server\\share\\mypackage.sft*, use the SFTMIME CONFIGURE PACKAGE command and give it the selected package GUID from the output of the SFTMIME QUERY OBJ command in step 1, followed by the OVERRIDEURL parameter and its new value, as follows:</span></span>

    `SFTMIME CONFIGURE PACKAGE:"{AF78ABE1-57D4-4297-89DE-C308684AEDD6}" /OVERRIDEURL "\\\\server\\share\\mypackage.sft "`

<span data-ttu-id="3d300-141">Für Version 4.6 SP2 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3d300-141">For version4.6 SP2, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d300-142">/NO-UPDATE-FTA-SHORTCUT</span><span class="sxs-lookup"><span data-stu-id="3d300-142">/NO-UPDATE-FTA-SHORTCUT</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d300-143">Gibt den aktuellen Zustand des/no-Update-FTA-Shortcut-Flags an.</span><span class="sxs-lookup"><span data-stu-id="3d300-143">Indicates the current state of the /NO-UPDATE-FTA-SHORTCUT flag.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="3d300-144">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3d300-144">Related topics</span></span>


[<span data-ttu-id="3d300-145">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="3d300-145">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





