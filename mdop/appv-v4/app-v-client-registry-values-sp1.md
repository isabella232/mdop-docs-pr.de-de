---
title: Registrierungswerte für App-V Client
description: Registrierungswerte für App-V Client
author: dansimp
ms.assetid: 46af5209-9762-47b9-afdb-9a2947e013f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 05cd807ff9882bc478aca07abc4a28cdea83086a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808055"
---
# <span data-ttu-id="f1da9-103">Registrierungswerte für App-V Client</span><span class="sxs-lookup"><span data-stu-id="f1da9-103">App-V Client Registry Values</span></span>


<span data-ttu-id="f1da9-104">Der Microsoft Application Virtualization (App-V)-Client speichert seine Konfiguration in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="f1da9-104">The Microsoft Application Virtualization (App-V) client stores its configuration in the registry.</span></span> <span data-ttu-id="f1da9-105">Sie können einige nützliche Informationen zu dem Client sammeln, wenn Sie das Format der Daten in der Registrierung verstehen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-105">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="f1da9-106">Sie können auch viele Clientaktionen konfigurieren, indem Sie Registrierungseinträge ändern.</span><span class="sxs-lookup"><span data-stu-id="f1da9-106">You can also configure many client actions by changing registry entries.</span></span> <span data-ttu-id="f1da9-107">In diesem Thema werden alle Application Virtualization (App-V)-Client Registrierungsschlüssel aufgelistet und deren Verwendung erläutert.</span><span class="sxs-lookup"><span data-stu-id="f1da9-107">This topic lists all the Application Virtualization (App-V) client registry keys and explains their uses.</span></span>

**<span data-ttu-id="f1da9-108">Wichtig</span><span class="sxs-lookup"><span data-stu-id="f1da9-108">Important</span></span>**  
<span data-ttu-id="f1da9-109">Auf einem Computer, auf dem ein 64-Bit-Betriebssystem ausgeführt wird, werden die in den folgenden Abschnitten beschriebenen Schlüssel und Werte unter HKEY \ _LOCAL \ _MACHINE \\software\\wow6432node\\microsoft\\softgrid\\4.5\\client.</span><span class="sxs-lookup"><span data-stu-id="f1da9-109">On a computer running a 64-bit operating system, the keys and values described in the following sections will be under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span></span>



## <span data-ttu-id="f1da9-110">Konfigurationsschlüssel</span><span class="sxs-lookup"><span data-stu-id="f1da9-110">Configuration Key</span></span>


<span data-ttu-id="f1da9-111">Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die mit dem HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\configuration-Schlüssel verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="f1da9-111">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f1da9-112">Name</span><span class="sxs-lookup"><span data-stu-id="f1da9-112">Name</span></span></th>
<th align="left"><span data-ttu-id="f1da9-113">Typ</span><span class="sxs-lookup"><span data-stu-id="f1da9-113">Type</span></span></th>
<th align="left"><span data-ttu-id="f1da9-114">Daten (Beispiele)</span><span class="sxs-lookup"><span data-stu-id="f1da9-114">Data (Examples)</span></span></th>
<th align="left"><span data-ttu-id="f1da9-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1da9-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-116">ProductName</span><span class="sxs-lookup"><span data-stu-id="f1da9-116">ProductName</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-117">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f1da9-117">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-118">Microsoft Application Virtualization-Desktop Client</span><span class="sxs-lookup"><span data-stu-id="f1da9-118">Microsoft Application Virtualization Desktop Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-119">Nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="f1da9-119">Do not modify.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-120">Version</span><span class="sxs-lookup"><span data-stu-id="f1da9-120">Version</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-121">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f1da9-121">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-122">4.5.0.xxx</span><span class="sxs-lookup"><span data-stu-id="f1da9-122">4.5.0.xxx</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-123">Nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="f1da9-123">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-124">Treiber</span><span class="sxs-lookup"><span data-stu-id="f1da9-124">Drivers</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-125">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f1da9-125">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-126">Sftfs.sys</span><span class="sxs-lookup"><span data-stu-id="f1da9-126">Sftfs.sys</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-127">Wenn dieser Schlüsselwert vorhanden ist, enthält er den Namen des Treibers, der beim letzten Start des Kerns einen Abbruchfehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="f1da9-127">If this key value is present, it contains the name of the driver that caused a stop error the last time the core was starting.</span></span> <span data-ttu-id="f1da9-128">Nachdem Sie den Abbruchfehler behoben haben, müssen Sie diesen Schlüsselwert löschen, damit sftlist beginnen kann.</span><span class="sxs-lookup"><span data-stu-id="f1da9-128">After you have fixed the stop error, you must delete this key value so that sftlist can start.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-129">Entspricht InstallPath</span><span class="sxs-lookup"><span data-stu-id="f1da9-129">InstallPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f1da9-130">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-131">Standard = c:\Programme\Microsoft Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="f1da9-131">Default=C:\Program Files\Microsoft Application Virtualization Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-132">Der Speicherort, an dem der Client installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f1da9-132">The location where the client is installed.</span></span> <span data-ttu-id="f1da9-133">Nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="f1da9-133">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-134">Protokolldateiname</span><span class="sxs-lookup"><span data-stu-id="f1da9-134">LogFileName</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f1da9-135">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-136">Standard = CSIDL_COMMON_APPDATA \microsoft\application Virtualization Client\sftlog.txt</span><span class="sxs-lookup"><span data-stu-id="f1da9-136">Default=CSIDL_COMMON_APPDATA\Microsoft\Application Virtualization Client\sftlog.txt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-137">Der Pfad und Name für die Clientprotokolldatei.</span><span class="sxs-lookup"><span data-stu-id="f1da9-137">The path and name for the client log file.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="f1da9-138">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="f1da9-138">Note</span></span></strong><br/><p><span data-ttu-id="f1da9-139">Wenn Sie eine frühere Version als App-V 4,6, SP1 und den Namen oder Speicherort der Protokolldatei ändern, müssen Sie den sftlist-Dienst neu starten, damit die Änderung wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="f1da9-139">If you are running an earlier version than App-V 4.6, SP1 and you modify the log file name or location, you must restart the sftlist service for the change to take effect.</span></span></p>
</div>
<div>

</div>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-140">LogMinSeverity</span><span class="sxs-lookup"><span data-stu-id="f1da9-140">LogMinSeverity</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-141">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-141">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-142">Standard = 4, Informations</span><span class="sxs-lookup"><span data-stu-id="f1da9-142">Default=4, Informational</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-143">Steuert, welche Nachrichten in das Protokoll geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-143">Controls which messages are written to the log.</span></span> <span data-ttu-id="f1da9-144">Der Wert gibt einen Schwellenwert für das protokollierte an – alles, was kleiner oder gleich dem Wert ist, wird protokolliert.</span><span class="sxs-lookup"><span data-stu-id="f1da9-144">The value indicates a threshold of what is logged—everything less than or equal to that value is logged.</span></span> <span data-ttu-id="f1da9-145">Ein Wert von 0x3 (Warnung) gibt beispielsweise an, dass Warnungen (0x3), Fehler (0x2) und kritische Fehler (0x1) protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-145">For example, a value of 0x3 (Warning) indicates that Warnings (0x3), Errors (0x2), and Critical Errors (0x1) are logged.</span></span></p>
<p><span data-ttu-id="f1da9-146">Wertbereich: 0x0 = keine, 0x1 = kritisch, 0x2 = Fehler, 0x3 = Warnung, 0x4 = Informationen (Standard), 0x5 = Verbose.</span><span class="sxs-lookup"><span data-stu-id="f1da9-146">Value Range: 0x0 = None, 0x1 = Critical, 0x2 = Error, 0x3 = Warning, 0x4 = Information (Default), 0x5 = Verbose.</span></span></p>
<p><span data-ttu-id="f1da9-147">Die Protokollebene kann über die Application Virtualization (App-V)-Clientkonsole und über die Eingabeaufforderung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-147">The log level is configurable from the Application Virtualization (App-V) client console and from the command prompt.</span></span> <span data-ttu-id="f1da9-148">An einer Eingabeaufforderung wird mit dem Befehl sftlist.exe/Verboselog die Protokollebene auf Verbose erhöht.</span><span class="sxs-lookup"><span data-stu-id="f1da9-148">At a command prompt, the command sftlist.exe /verboselog will increase the log level to verbose.</span></span> <span data-ttu-id="f1da9-149">Weitere Informationen zu Befehlszeilen Details finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="f1da9-149">For more information on command-line details see</span></span></p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467">https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467</a></p>
<p><span data-ttu-id="f1da9-150">.</span><span class="sxs-lookup"><span data-stu-id="f1da9-150">.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-151">LogRolloverCount</span><span class="sxs-lookup"><span data-stu-id="f1da9-151">LogRolloverCount</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-152">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-152">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-153">Standard = 4</span><span class="sxs-lookup"><span data-stu-id="f1da9-153">Default=4</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-154">Definiert die Anzahl von Sicherungskopien der Protokolldatei, die beim Zurücksetzen beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-154">Defines the number of backup copies of the log file that are kept when it is reset.</span></span> <span data-ttu-id="f1da9-155">Der gültige Bereich ist 0 – 9999.</span><span class="sxs-lookup"><span data-stu-id="f1da9-155">The valid range is 0–9999.</span></span> <span data-ttu-id="f1da9-156">Der Standardwert ist 4.</span><span class="sxs-lookup"><span data-stu-id="f1da9-156">The default is 4.</span></span> <span data-ttu-id="f1da9-157">Der Wert 0 bedeutet, dass keine Kopien aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-157">A value of 0 means no copies will be kept.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-158">LogMaxSize</span><span class="sxs-lookup"><span data-stu-id="f1da9-158">LogMaxSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-159">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-159">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-160">Standard = 256</span><span class="sxs-lookup"><span data-stu-id="f1da9-160">Default=256</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-161">Definiert die maximale Größe in Megabytes (MB), die die Protokolldatei vergrößert werden kann, bevor Sie zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="f1da9-161">Defines the maximum size in megabytes (MB) that the log file can grow before being reset.</span></span> <span data-ttu-id="f1da9-162">Die Standardgröße ist 256 MB.</span><span class="sxs-lookup"><span data-stu-id="f1da9-162">The default size is 256 MB.</span></span> <span data-ttu-id="f1da9-163">Wenn diese Größe erreicht ist, wird beim nächsten Schreibversuch eine Protokoll Zurücksetzung erzwungen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-163">When this size is reached, a log reset will be forced on the next write attempt.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-164">SystemEventLogLevel</span><span class="sxs-lookup"><span data-stu-id="f1da9-164">SystemEventLogLevel</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-165">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-165">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-166">Standard = 0x4 (App-V 4,5)</span><span class="sxs-lookup"><span data-stu-id="f1da9-166">Default=0x4 (App-V 4.5)</span></span></p>
<p><span data-ttu-id="f1da9-167">Standard = 0x3 (App-V 4,6)</span><span class="sxs-lookup"><span data-stu-id="f1da9-167">Default=0x3 (App-V 4.6)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-168">Gibt den Protokolliergrad an, bei dem Protokollnachrichten in das NT-Ereignisprotokoll geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-168">Indicates the logging level at which log messages are written to the NT event log.</span></span> <span data-ttu-id="f1da9-169">Der Wert gibt einen Schwellenwert für das protokollierte an, d. h., alles, was kleiner oder gleich dem Wert ist, wird protokolliert.</span><span class="sxs-lookup"><span data-stu-id="f1da9-169">The value indicates a threshold of what is logged—that is, everything equal to or less than that value is logged.</span></span> <span data-ttu-id="f1da9-170">Ein Wert von 0x3 (Warnung) gibt beispielsweise an, dass Warnungen (0x3), Fehler (0x2) und kritische Fehler (0x1) protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-170">For example, a value of 0x3 (Warning) indicates that Warnings (0x3), Errors (0x2), and Critical Errors (0x1) are logged.</span></span></p>
<p><span data-ttu-id="f1da9-171">Wertebereich</span><span class="sxs-lookup"><span data-stu-id="f1da9-171">Value Range</span></span></p>
<p><span data-ttu-id="f1da9-172">0x0 = keine</span><span class="sxs-lookup"><span data-stu-id="f1da9-172">0x0 = None</span></span></p>
<p><span data-ttu-id="f1da9-173">0x1 = kritisch</span><span class="sxs-lookup"><span data-stu-id="f1da9-173">0x1 = Critical</span></span></p>
<p><span data-ttu-id="f1da9-174">0x2 = Fehler</span><span class="sxs-lookup"><span data-stu-id="f1da9-174">0x2 = Error</span></span></p>
<p><span data-ttu-id="f1da9-175">0x3 = Warnung</span><span class="sxs-lookup"><span data-stu-id="f1da9-175">0x3 = Warning</span></span></p>
<p><span data-ttu-id="f1da9-176">0x4 = Informationen (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1da9-176">0x4 = Information (Default)</span></span></p>
<p><span data-ttu-id="f1da9-177">0x5 = Verbose</span><span class="sxs-lookup"><span data-stu-id="f1da9-177">0x5 = Verbose</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-178">AllowIndependentFileStreaming</span><span class="sxs-lookup"><span data-stu-id="f1da9-178">AllowIndependentFileStreaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-179">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-179">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-180">Standard = 0</span><span class="sxs-lookup"><span data-stu-id="f1da9-180">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-181">Gibt an, ob das Streaming aus einer Datei unabhängig davon aktiviert wird, wie der Client mit dem ApplicationSourceRoot-Parameter konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="f1da9-181">Indicates whether streaming from file will be enabled regardless of how the client has been configured with the APPLICATIONSOURCEROOT parameter.</span></span> <span data-ttu-id="f1da9-182">Ist dieser Wert auf "false" festgelegt, wird durch den Transport kein Streaming aus Dateien möglich, auch wenn der OSD-HREF-oder der ApplicationSourceRoot-Parameter einen Dateipfad enthält.</span><span class="sxs-lookup"><span data-stu-id="f1da9-182">If set to FALSE, the transport will not enable streaming from files even if the OSD HREF or the APPLICATIONSOURCEROOT parameter contains a file path.</span></span></p>
<p><span data-ttu-id="f1da9-183">0x0 = false (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1da9-183">0x0=False (default)</span></span></p>
<p><span data-ttu-id="f1da9-184">0x1 = wahr</span><span class="sxs-lookup"><span data-stu-id="f1da9-184">0x1=True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-185">ApplicationSourceRoot</span><span class="sxs-lookup"><span data-stu-id="f1da9-185">ApplicationSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-186">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f1da9-186">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-187">rtsps://mainserver:322/prodapps</span><span class="sxs-lookup"><span data-stu-id="f1da9-187">rtsps://mainserver:322/prodapps</span></span></p>
<p><a href="https://mainserver:443/prodapps" data-raw-source="https://mainserver:443/prodapps">https://mainserver:443/prodapps</a></p>
<p><span data-ttu-id="f1da9-188">Datei://\uncserver\share\prodapps</span><span class="sxs-lookup"><span data-stu-id="f1da9-188">file://\uncserver\share\prodapps</span></span></p>
<p><span data-ttu-id="f1da9-189">Datei://\uncserver\share</span><span class="sxs-lookup"><span data-stu-id="f1da9-189">file://\uncserver\share</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-190">Ermöglicht einem Administrator oder einem ESD-System (Electronic Software Distribution), sicherzustellen, dass das Laden der Anwendung entsprechend dem Topologieverwaltung-Schema durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1da9-190">Enables an administrator or electronic software distribution (ESD) system to ensure application loading is performed according to the topology management scheme.</span></span> <span data-ttu-id="f1da9-191">Verwenden Sie diesen Schlüsselwert, um die OSD-CodeBase für das href-Element (beispielsweise den Quellspeicherort) für eine Anwendung zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="f1da9-191">Use this key value to override the OSD CODEBASE for the HREF element (for example, the source location) for an application.</span></span> <span data-ttu-id="f1da9-192">Der Anwendungsquellen Stamm unterstützt URLs und UNC-Pfad Formate (Universal Naming Convention).</span><span class="sxs-lookup"><span data-stu-id="f1da9-192">Application Source Root supports URLs and Universal Naming Convention (UNC) path formats.</span></span></p>
<p><span data-ttu-id="f1da9-193">Das richtige Format für den URL-Pfad ist Protocol://Servername: [Port] [/path] [/], wobei Port und Path optional sind.</span><span class="sxs-lookup"><span data-stu-id="f1da9-193">The correct format for the URL path is protocol://servername:[port][/path][/], where port and path are optional.</span></span> <span data-ttu-id="f1da9-194">Wenn kein Port angegeben wird, wird der Standardport für das Protokoll verwendet.</span><span class="sxs-lookup"><span data-stu-id="f1da9-194">If a port is not specified, the default port for the protocol is used.</span></span> <span data-ttu-id="f1da9-195">Nur der Abschnitt Protocol://Server: Port der OSD-URL wird ersetzt.</span><span class="sxs-lookup"><span data-stu-id="f1da9-195">Only the protocol://server:port portion of the OSD URL is replaced.</span></span> </p>
<p><span data-ttu-id="f1da9-196">Das richtige Format für den UNC-Pfad lautet \computername\sharefolder [Folder] [], wobei Folder optional ist.</span><span class="sxs-lookup"><span data-stu-id="f1da9-196">The correct format for the UNC path is \computername\sharefolder[folder][], where folder is optional.</span></span> <span data-ttu-id="f1da9-197">Der Computername kann ein vollständig qualifizierter Domänenname (Fully Qualified Domain Name, FQDN) oder eine IP-Adresse sein, und sharefolder kann ein Laufwerkbuchstabe sein.</span><span class="sxs-lookup"><span data-stu-id="f1da9-197">The computer name can be a fully qualified domain name (FQDN) or an IP address, and sharefolder can be a drive letter.</span></span> <span data-ttu-id="f1da9-198">Es wird nur der \computername\sharefolder-oder Laufwerkbuchstaben Bereich des OSD-Pfads ersetzt.</span><span class="sxs-lookup"><span data-stu-id="f1da9-198">Only the \computername\sharefolder or drive letter portion of the OSD path is replaced.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-199">OSDSourceRoot</span><span class="sxs-lookup"><span data-stu-id="f1da9-199">OSDSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-200">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f1da9-200">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-201">\computername\sharefolder\resource</span><span class="sxs-lookup"><span data-stu-id="f1da9-201">\computername\sharefolder\resource</span></span></p>
<p><span data-ttu-id="f1da9-202">\computername\content</span><span class="sxs-lookup"><span data-stu-id="f1da9-202">\computername\content</span></span></p>
<p><span data-ttu-id="f1da9-203">C:\foldername</span><span class="sxs-lookup"><span data-stu-id="f1da9-203">C:\foldername</span></span></p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p><span data-ttu-id="f1da9-204">Ermöglicht einem Administrator die Angabe eines Quellspeicherorts für den Abruf von OSD-Dateien für ein sequenziertes Anwendungspaket während der Veröffentlichung.</span><span class="sxs-lookup"><span data-stu-id="f1da9-204">Enables an administrator to specify a source location for OSD file retrieval for a sequenced application package during publication.</span></span> <span data-ttu-id="f1da9-205">Zulässige Formate für die OSDSourceRoot sind UNC-Pfade und URLs (http oder HTTPS).</span><span class="sxs-lookup"><span data-stu-id="f1da9-205">Acceptable formats for the OSDSourceRoot include UNC paths and URLs (http or https).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-206">IconSourceRoot</span><span class="sxs-lookup"><span data-stu-id="f1da9-206">IconSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-207">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f1da9-207">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-208">\computername\sharefolder\resource</span><span class="sxs-lookup"><span data-stu-id="f1da9-208">\computername\sharefolder\resource</span></span></p>
<p><span data-ttu-id="f1da9-209">\computername\content</span><span class="sxs-lookup"><span data-stu-id="f1da9-209">\computername\content</span></span></p>
<p><span data-ttu-id="f1da9-210">C:\foldername</span><span class="sxs-lookup"><span data-stu-id="f1da9-210">C:\foldername</span></span></p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p><span data-ttu-id="f1da9-211">Ermöglicht einem Administrator, einen Quellspeicherort für das Abrufen von Symboldateien für ein sequenziertes Anwendungspaket während der Veröffentlichung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f1da9-211">Enables an administrator to specify a source location for icon file retrieval for a sequenced application package during publication.</span></span> <span data-ttu-id="f1da9-212">Zulässige Formate für die IconSourceRoot sind UNC-Pfade und URLs (http oder HTTPS).</span><span class="sxs-lookup"><span data-stu-id="f1da9-212">Acceptable formats for the IconSourceRoot include UNC paths and URLs (http or https).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-213">AutoLoadTriggers</span><span class="sxs-lookup"><span data-stu-id="f1da9-213">AutoLoadTriggers</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-214">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-214">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-215">Standard = 5</span><span class="sxs-lookup"><span data-stu-id="f1da9-215">Default=5</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-216">Beim automatischen Lademodus handelt es sich um einen Client Laufzeitrichtlinien-Konfigurationsparameter, mit dem der sekundäre Funktionsbaustein einer virtualisierten Anwendung automatisch im Hintergrund an den Client gestreamt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f1da9-216">AutoLoad is a client runtime policy configuration parameter that enables the secondary feature block of a virtualized application to be streamed to the client automatically in the background.</span></span> <span data-ttu-id="f1da9-217">Die Trigger für das automatische Laden sind Flags, die Ereignisse angeben, die das automatische Laden von Anwendungen initiieren.</span><span class="sxs-lookup"><span data-stu-id="f1da9-217">The AutoLoad triggers are flags to indicate events that initiate auto-loading of applications.</span></span> <span data-ttu-id="f1da9-218">Beim Laden wird implizit Hintergrund Streaming verwendet, damit die Anwendung vollständig in den Cache geladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="f1da9-218">AutoLoad implicitly uses background streaming to enable the application to be fully loaded into cache.</span></span> <span data-ttu-id="f1da9-219">Der primäre Feature-Block wird zuerst geladen, und die restlichen Funktionsbausteine werden in den Hintergrund geladen, damit Vordergrund Vorgänge wie Benutzerinteraktionen mit Anwendungen ausgeführt werden und eine optimale Leistung erzielt wird.</span><span class="sxs-lookup"><span data-stu-id="f1da9-219">The primary feature block will be loaded first, and the remaining feature blocks will be loaded in the background to enable foreground operations, such as user interaction with applications, to take place and provide optimal perceived performance.</span></span></p>
<p><span data-ttu-id="f1da9-220">Bitmaskenwerte:</span><span class="sxs-lookup"><span data-stu-id="f1da9-220">Bit mask values:</span></span></p>
<p><span data-ttu-id="f1da9-221">(0) Never: keine Bits sind gesetzt (Wert ist 0), es wird kein automatisches Laden durchgeführt, da keine Trigger gesetzt sind.</span><span class="sxs-lookup"><span data-stu-id="f1da9-221">(0) Never: No bits are set (value is 0), no auto loading will be performed, because there are no triggers set.</span></span></p>
<p><span data-ttu-id="f1da9-222">(1) onlaunch: das Laden beginnt, wenn ein Benutzer eine Anwendung startet.</span><span class="sxs-lookup"><span data-stu-id="f1da9-222">(1) OnLaunch: Loading starts when a user starts an application.</span></span></p>
<p><span data-ttu-id="f1da9-223">(2) OnRefresh: das Laden beginnt, wenn die Anwendung veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="f1da9-223">(2) OnRefresh: Loading starts when the application is published.</span></span> <span data-ttu-id="f1da9-224">Dies tritt auf, wenn der paketdatensatz hinzugefügt oder aktualisiert wird, beispielsweise, wenn eine Veröffentlichungsaktualisierung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="f1da9-224">This occurs whenever the package record is added or updated—for example, when a publishing refresh occurs.</span></span></p>
<p><span data-ttu-id="f1da9-225">(4) onlogin: das Laden beginnt, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="f1da9-225">(4) OnLogin: Loading starts when a user logs in.</span></span></p>
<p><span data-ttu-id="f1da9-226">(5) onlaunch und onlogin: Standard.</span><span class="sxs-lookup"><span data-stu-id="f1da9-226">(5) OnLaunch and OnLogin: Default.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-227">AutoLoadTarget</span><span class="sxs-lookup"><span data-stu-id="f1da9-227">AutoLoadTarget</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-228">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-228">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-229">Standard = 1</span><span class="sxs-lookup"><span data-stu-id="f1da9-229">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-230">Gibt an, was automatisch geladen wird, wenn ein bestimmter Trigger für das automatische Laden eintritt.</span><span class="sxs-lookup"><span data-stu-id="f1da9-230">Indicates what will be auto-loaded when any given AutoLoad triggers occur.</span></span> <span data-ttu-id="f1da9-231">Bitmaskenwerte:</span><span class="sxs-lookup"><span data-stu-id="f1da9-231">Bit mask values:</span></span></p>
<p><span data-ttu-id="f1da9-232">(0) None: kein automatisches Laden, unabhängig davon, welche Trigger eingestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="f1da9-232">(0) None: No auto-loading, regardless of what triggers may be set.</span></span></p>
<p><span data-ttu-id="f1da9-233">(1) PreviouslyUsed (Standard): Wenn ein automatischer Trigger aktiviert ist, laden Sie nur die Pakete, bei denen mindestens eine Anwendung im Paket zuvor verwendet wurde – also gestartet oder vorab gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="f1da9-233">(1) PreviouslyUsed (default): If any AutoLoad trigger is enabled, load only the packages where at least one application in the package has been previously used—that is, started or precached.</span></span></p>
<p><span data-ttu-id="f1da9-234">(2) alle: Wenn ein automatischer Trigger aktiviert ist, werden alle Anwendungen im Paket (pro Paket) oder alle Pakete (für Client festgesetzt) automatisch geladen, unabhängig davon, ob Sie jemals gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-234">(2) All: If any AutoLoad trigger is enabled, all applications in the package (per package) or all packages (set for client) will be automatically loaded, whether or not they have ever been started.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-235">RequireAuthorizationIfCached</span><span class="sxs-lookup"><span data-stu-id="f1da9-235">RequireAuthorizationIfCached</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-236">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-236">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-237">Standard = 1</span><span class="sxs-lookup"><span data-stu-id="f1da9-237">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-238">Gibt an, dass immer eine Autorisierung erforderlich ist, unabhängig davon, ob sich eine Anwendung bereits im Cache befindet.</span><span class="sxs-lookup"><span data-stu-id="f1da9-238">Indicates that authorization is always required, whether or not an application is already in cache.</span></span> <span data-ttu-id="f1da9-239">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="f1da9-239">Possible values:</span></span></p>
<p><span data-ttu-id="f1da9-240">0 = falsch: versuchen Sie immer, eine Verbindung mit dem Server herzustellen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-240">0=False: Always try to connect to the server.</span></span> <span data-ttu-id="f1da9-241">Wenn keine Verbindung mit dem Server hergestellt werden kann, ermöglicht der Client dem Benutzer weiterhin, eine Anwendung zu starten, die zuvor in den Cache geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="f1da9-241">If a connection to the server cannot be established, the client still allows the user to launch an application that has previously been loaded into cache.</span></span></p>
<p><span data-ttu-id="f1da9-242">1 = wahr (Standard): die Anwendung muss beim Start immer autorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-242">1=True (default): Application always must be authorized at startup.</span></span> <span data-ttu-id="f1da9-243">Für RTSP-Streaming-Anwendungen wird das Benutzerautorisierungstoken zur Autorisierung an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="f1da9-243">For RTSP streamed applications, the user authorization token is sent to the server for authorization.</span></span> <span data-ttu-id="f1da9-244">Bei dateibasierten Anwendungen steuern Datei-ACLs, ob ein Benutzer auf die Anwendung zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="f1da9-244">For file-based applications, file ACLs control whether a user may access the application.</span></span></p>
<p><span data-ttu-id="f1da9-245">Starten Sie den sftlist-Dienst neu, damit die Änderung wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="f1da9-245">Restart the sftlist service for the change to take effect.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-246">UserDataDirectory</span><span class="sxs-lookup"><span data-stu-id="f1da9-246">UserDataDirectory</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-247">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f1da9-247">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-248">APPDATA</span><span class="sxs-lookup"><span data-stu-id="f1da9-248">%APPDATA%</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-249">Der Speicherort, an dem der Symbolcache und die Benutzereinstellungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-249">Location where the icon cache and user settings are stored.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-250">GlobalDataDirectory</span><span class="sxs-lookup"><span data-stu-id="f1da9-250">GlobalDataDirectory</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-251">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f1da9-251">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-252">C:\Users\Public\Documents</span><span class="sxs-lookup"><span data-stu-id="f1da9-252">C:\Users\Public\Documents</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-253">Verzeichnis, das für globale App-V-Daten verwendet werden soll, einschließlich Caches für OSD-Dateien, Symboldateien, Verknüpfungsinformationen und SystemGuard-Ressourcen wie INI-Dateien.</span><span class="sxs-lookup"><span data-stu-id="f1da9-253">Directory to use for global App-V data, including caches for OSD files, icon files, shortcut information, and SystemGuard resources such as .ini files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-254">AllowCrashes</span><span class="sxs-lookup"><span data-stu-id="f1da9-254">AllowCrashes</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-255">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-255">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-256">0 oder 1</span><span class="sxs-lookup"><span data-stu-id="f1da9-256">0 or 1</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-257">Standard = 0: ein Wert von "0" bedeutet, dass der Client versucht, interne Programmausnahmen abzufangen, damit andere Benutzer Anwendungen wiederhergestellt und fortfahren können, wenn ein Absturz eintritt.</span><span class="sxs-lookup"><span data-stu-id="f1da9-257">Default=0: A value of 0 means that the client tries to catch internal program exceptions so that other user applications can recover and continue when a crash happens.</span></span> <span data-ttu-id="f1da9-258">Der Wert 1 bedeutet, dass der Client die internen Programmausnahmen eintreten lässt, damit Sie in einem Debugger erfasst werden können.</span><span class="sxs-lookup"><span data-stu-id="f1da9-258">A value of 1 means that the client allows the internal program exceptions to occur so that they can be captured in a debugger.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-259">CoreInternalTimeout</span><span class="sxs-lookup"><span data-stu-id="f1da9-259">CoreInternalTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-260">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-260">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-261">60</span><span class="sxs-lookup"><span data-stu-id="f1da9-261">60</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-262">Timeout in Sekunden für interne IPC-Anforderungen zwischen Core und Front-End.</span><span class="sxs-lookup"><span data-stu-id="f1da9-262">Time-out in seconds for internal IPC requests between core and front-end.</span></span> <span data-ttu-id="f1da9-263">Nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="f1da9-263">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-264">DefaultSuiteCombineTime</span><span class="sxs-lookup"><span data-stu-id="f1da9-264">DefaultSuiteCombineTime</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-265">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-265">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-266">10</span><span class="sxs-lookup"><span data-stu-id="f1da9-266">10</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-267">Dieser Wert wird verwendet, um anzugeben, wie schnell nach dem Start ein Programm beendet werden kann, und es werden keine Fehlermeldungen generiert, wenn eine andere Anwendung in derselben Suite ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1da9-267">This value is used to indicate how soon after being started that a program can shut down and not generate any error messages when another application in the same suite is running.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-268">SerializedSuiteLaunchTimeout</span><span class="sxs-lookup"><span data-stu-id="f1da9-268">SerializedSuiteLaunchTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-269">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-269">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-270">Standard = 60000</span><span class="sxs-lookup"><span data-stu-id="f1da9-270">Default=60000</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-271">Definiert, wie lange der Client in Millisekunden warten wird, während er versucht, Programmstarts in der gleichen Suite zu serialisieren.</span><span class="sxs-lookup"><span data-stu-id="f1da9-271">Defines how long in milliseconds the client will wait as it tries to serialize program starts in the same suite.</span></span> <span data-ttu-id="f1da9-272">Bei einem Timeout des Clients wird der Programmstart fortgesetzt, aber nicht serialisiert.</span><span class="sxs-lookup"><span data-stu-id="f1da9-272">If the client times out, the program start will continue but it will not be serialized.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-273">ScriptTimeout</span><span class="sxs-lookup"><span data-stu-id="f1da9-273">ScriptTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-274">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-274">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-275">300</span><span class="sxs-lookup"><span data-stu-id="f1da9-275">300</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-276">Standardtimeout in Sekunden für Skripts in der OSD-Datei, wenn Wait = true.</span><span class="sxs-lookup"><span data-stu-id="f1da9-276">Default time-out in seconds for scripts in OSD file if WAIT=TRUE.</span></span> <span data-ttu-id="f1da9-277">Sie können pro-Skript-Timeouts mit Timeout anstelle von Wait angeben.</span><span class="sxs-lookup"><span data-stu-id="f1da9-277">You can specify per-script time-outs with TIMEOUT instead of WAIT.</span></span> <span data-ttu-id="f1da9-278">Der Wert 0 bedeutet keine Wartezeit, und 0xFFFFFFFF bedeutet, dass Sie für immer warten.</span><span class="sxs-lookup"><span data-stu-id="f1da9-278">A value of 0 means no wait, and 0xFFFFFFFF means wait forever.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-279">LaunchRecordLogPath</span><span class="sxs-lookup"><span data-stu-id="f1da9-279">LaunchRecordLogPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-280">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f1da9-280">String</span></span> </p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f1da9-281">Wenn dieser Wert unter HKLM oder HKCU einen gültigen Pfad zu einer Protokolldatei enthält, schreibt SFTTray in dieses Protokoll, wenn Programme gestartet, heruntergefahren, nicht gestartet werden und der getrennte Modus beendet oder beendet wird.</span><span class="sxs-lookup"><span data-stu-id="f1da9-281">If, under either HKLM or HKCU, this value contains a valid path to a log file, SFTTray will write to this log when programs start, shut down, fail to launch, and enter or exit disconnected mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-282">LaunchRecordMask</span><span class="sxs-lookup"><span data-stu-id="f1da9-282">LaunchRecordMask</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-283">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-283">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-284">0x1A (26) log-Startfehler und die Eingabe-und Ausgangs Aktivität für den Offlinemodus.</span><span class="sxs-lookup"><span data-stu-id="f1da9-284">0x1A (26) log launch errors and disconnected mode entry and exit activity.</span></span></p>
<p><span data-ttu-id="f1da9-285">0x1F (31) protokolliert alles.</span><span class="sxs-lookup"><span data-stu-id="f1da9-285">0x1F (31) logs everything.</span></span></p>
<p><span data-ttu-id="f1da9-286">0x0 (0) protokolliert nichts.</span><span class="sxs-lookup"><span data-stu-id="f1da9-286">0x0 (0) logs nothing.</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-287">Gibt an, welches der fünf Ereignisse protokolliert wird (Bitmaskenwerte):</span><span class="sxs-lookup"><span data-stu-id="f1da9-287">Specifies which of the five events are logged (bitmask values):</span></span></p>
<p><span data-ttu-id="f1da9-288">1 für Programmstarts</span><span class="sxs-lookup"><span data-stu-id="f1da9-288">1 for program starts</span></span></p>
<p><span data-ttu-id="f1da9-289">2 für Fehler beim Startfehler</span><span class="sxs-lookup"><span data-stu-id="f1da9-289">2 for launch failure errors</span></span></p>
<p><span data-ttu-id="f1da9-290">4 für Shutdowns</span><span class="sxs-lookup"><span data-stu-id="f1da9-290">4 for shutdowns</span></span></p>
<p><span data-ttu-id="f1da9-291">8 für die Eingabe des getrennten Modus</span><span class="sxs-lookup"><span data-stu-id="f1da9-291">8 for entering disconnected mode</span></span></p>
<p><span data-ttu-id="f1da9-292">16 für das Beenden des getrennten Modus, um die Verbindung zu einem Server wiederherzustellen</span><span class="sxs-lookup"><span data-stu-id="f1da9-292">16 for exiting disconnected mode to reconnect to a server</span></span></p>
<p><span data-ttu-id="f1da9-293">Fügen Sie eine beliebige Kombination dieser Nummern hinzu, um die jeweiligen Nachrichten zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f1da9-293">Add any combination of those numbers to turn on the respective messages.</span></span> <span data-ttu-id="f1da9-294">Standardmäßig ist 0x1F, wenn nicht in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="f1da9-294">Defaults to 0x1F if not in registry.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-295">LaunchRecordWriteTimeout</span><span class="sxs-lookup"><span data-stu-id="f1da9-295">LaunchRecordWriteTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-296">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-296">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-297">Standard = 3000</span><span class="sxs-lookup"><span data-stu-id="f1da9-297">Default=3000</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-298">Gibt in Millisekunden an, wie lange das Tablett wartet, wenn es versucht, in das Startdatensatz Protokoll zu schreiben, wenn es von einem anderen Prozess verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f1da9-298">Specifies in milliseconds how long the tray will wait when trying to write to the launch record log if another process is using it.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-299">ImportSearchPath</span><span class="sxs-lookup"><span data-stu-id="f1da9-299">ImportSearchPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-300">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f1da9-300">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-301">d:\files; C:\Dokumente und settings\user1\SFTs</span><span class="sxs-lookup"><span data-stu-id="f1da9-301">d:\files;C:\documents and settings\user1\SFTs</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-302">Eine durch Semikolons getrennte Liste mit bis zu fünf Verzeichnissen für die Suche nach tragbaren SFT-Dateien, bevor der Benutzer aufgefordert wird, ein Verzeichnis auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-302">A semicolon delimited list of up to five directories to search for portable SFT files before prompting the user to select a directory.</span></span> <span data-ttu-id="f1da9-303">Der nachfolgende umgekehrte Schrägstrich in Paths ist optional.</span><span class="sxs-lookup"><span data-stu-id="f1da9-303">Trailing backslash in paths is optional.</span></span> <span data-ttu-id="f1da9-304">Dieser Wert ist standardmäßig nicht vorhanden und muss manuell eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-304">This value is not present by default and must be set manually.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-305">UserImportPath</span><span class="sxs-lookup"><span data-stu-id="f1da9-305">UserImportPath</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-306">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f1da9-306">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-307">D:\SFTs</span><span class="sxs-lookup"><span data-stu-id="f1da9-307">D:\SFTs</span></span>\ </p></td>
<td align="left"><p><span data-ttu-id="f1da9-308">Gültig nur unter HKCU.</span><span class="sxs-lookup"><span data-stu-id="f1da9-308">Valid only under HKCU.</span></span> <span data-ttu-id="f1da9-309">Der letzte Speicherort, zu dem der Benutzer beim Suchen einer SFT-Datei für den Paketimport gesucht hat.</span><span class="sxs-lookup"><span data-stu-id="f1da9-309">The last location the user browsed to while finding a SFT file for package import.</span></span> <span data-ttu-id="f1da9-310">Wird automatisch festgesetzt, wenn SFT erfolgreich gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="f1da9-310">Set automatically if the SFT is found successfully.</span></span> <span data-ttu-id="f1da9-311">Diese wird für aufeinanderfolgende Importe verwendet, wenn Sie versuchen, SFT-Dateien automatisch zu finden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-311">This is used on successive imports when trying to automatically locate SFT files.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f1da9-312">Freigegebener Schlüssel</span><span class="sxs-lookup"><span data-stu-id="f1da9-312">Shared Key</span></span>


<span data-ttu-id="f1da9-313">Der HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\shared-Schlüssel steuert Werte, die für App-V-Komponenten freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-313">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Shared key controls values that are shared across App-V components.</span></span> <span data-ttu-id="f1da9-314">Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die mit dem freigegebenen Schlüssel verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="f1da9-314">The following table provides information about the registry values associated with the Shared key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f1da9-315">Name</span><span class="sxs-lookup"><span data-stu-id="f1da9-315">Name</span></span> </th>
<th align="left"><span data-ttu-id="f1da9-316">Typ</span><span class="sxs-lookup"><span data-stu-id="f1da9-316">Type</span></span> </th>
<th align="left"><span data-ttu-id="f1da9-317">Daten (Beispiele)</span><span class="sxs-lookup"><span data-stu-id="f1da9-317">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="f1da9-318">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1da9-318">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-319">DumpPath</span><span class="sxs-lookup"><span data-stu-id="f1da9-319">DumpPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-320">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f1da9-320">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-321">Standard = c-c</span><span class="sxs-lookup"><span data-stu-id="f1da9-321">Default=C:\</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-322">Standardpfad zum Erstellen von Speicherabbilddateien beim Generieren eines Mini Abbilds für eine Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="f1da9-322">Default path to create dump files when generating a minidump on an exception.</span></span> <span data-ttu-id="f1da9-323">Dieser Standardwert ist "c". Wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="f1da9-323">This defaults to C:\ if not specified.</span></span> <span data-ttu-id="f1da9-324">Der Client Installer legt diesen Schlüssel auf das &lt; globale Datenverzeichnis der APP-Virtualisierung fest &gt; \Dumps.</span><span class="sxs-lookup"><span data-stu-id="f1da9-324">The Client installer sets this key to the &lt;App Virtualization global data directory&gt;\Dumps.</span></span> <span data-ttu-id="f1da9-325">Der Sequencer-Installer legt diesen Schlüssel auf das Installationsverzeichnis fest.</span><span class="sxs-lookup"><span data-stu-id="f1da9-325">The Sequencer installer sets this key to the installation directory.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-326">DumpPathSizeLimit</span><span class="sxs-lookup"><span data-stu-id="f1da9-326">DumpPathSizeLimit</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-327">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-327">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-328">1000</span><span class="sxs-lookup"><span data-stu-id="f1da9-328">1000</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-329">Gibt die maximale Gesamtmenge an Speicherplatz in Megabyte an, die zum Speichern von Mini Abbildern verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f1da9-329">Specifies the maximum total amount of disk space in megabytes that can be used to store minidumps.</span></span> <span data-ttu-id="f1da9-330">Standard = 1000 MB.</span><span class="sxs-lookup"><span data-stu-id="f1da9-330">Default = 1000 MB.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f1da9-331">Netzwerkschlüssel</span><span class="sxs-lookup"><span data-stu-id="f1da9-331">Network Key</span></span>


<span data-ttu-id="f1da9-332">Der HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\network-Schlüssel steuert eine Vielzahl von netzwerkbezogenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="f1da9-332">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network key controls a variety of network-related parameters.</span></span> <span data-ttu-id="f1da9-333">Dieser Schlüssel wird in erster Linie vom Netzwerktransport-Agent verwendet.</span><span class="sxs-lookup"><span data-stu-id="f1da9-333">This key is primarily used by the network transport agent.</span></span> <span data-ttu-id="f1da9-334">Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die dem Netzwerkschlüssel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f1da9-334">The following table provides information about the registry values associated with the Network key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f1da9-335">Name</span><span class="sxs-lookup"><span data-stu-id="f1da9-335">Name</span></span> </th>
<th align="left"><span data-ttu-id="f1da9-336">Typ</span><span class="sxs-lookup"><span data-stu-id="f1da9-336">Type</span></span> </th>
<th align="left"><span data-ttu-id="f1da9-337">Daten (Beispiele)</span><span class="sxs-lookup"><span data-stu-id="f1da9-337">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="f1da9-338">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1da9-338">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-339">Online</span><span class="sxs-lookup"><span data-stu-id="f1da9-339">Online</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-340">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-340">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-341">Standard = 1</span><span class="sxs-lookup"><span data-stu-id="f1da9-341">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-342">Aktiviert oder deaktiviert den Offlinemodus.</span><span class="sxs-lookup"><span data-stu-id="f1da9-342">Enables or disables offline mode.</span></span> <span data-ttu-id="f1da9-343">Wenn der Wert auf 0 gesetzt ist, kommuniziert der Client nicht mit App-V-Verwaltungsservern oder Veröffentlichungsservern.</span><span class="sxs-lookup"><span data-stu-id="f1da9-343">If set to 0, the client will not communicate with App-V Management Servers or publishing servers.</span></span> <span data-ttu-id="f1da9-344">Bei getrennten Vorgängen kann der Client eine geladene Anwendung starten, auch wenn Sie nicht mit einem App-V-Verwaltungs Server verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="f1da9-344">In disconnected operations, the client can start a loaded application even when it is not connected to an App-V Management Server.</span></span> <span data-ttu-id="f1da9-345">Im Offlinemodus versucht der Client nicht, eine Verbindung zu einem App-V-Verwaltungsserver oder Veröffentlichungsserver herzustellen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-345">In offline mode, the client does not attempt to connect to an App-V Management Server or publishing server.</span></span> <span data-ttu-id="f1da9-346">Sie müssen getrennte Vorgänge zulassen, um offline arbeiten zu können.</span><span class="sxs-lookup"><span data-stu-id="f1da9-346">You must allow disconnected operations to be able to work offline.</span></span> <span data-ttu-id="f1da9-347">Der Standardwert ist 1 aktiviert (Online) und 0 ist deaktiviert (offline).</span><span class="sxs-lookup"><span data-stu-id="f1da9-347">Default value is 1 enabled (online), and 0 is disabled (offline).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-348">AllowDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="f1da9-348">AllowDisconnectedOperation</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-349">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-349">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-350">Standard = 1</span><span class="sxs-lookup"><span data-stu-id="f1da9-350">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-351">Aktiviert oder deaktiviert den getrennten Betrieb.</span><span class="sxs-lookup"><span data-stu-id="f1da9-351">Enables or disables disconnected operation.</span></span> <span data-ttu-id="f1da9-352">Der Standardwert ist 1 aktiviert, und 0 ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f1da9-352">Default value is 1 enabled, and 0 is disabled.</span></span> <span data-ttu-id="f1da9-353">Wenn getrennte Vorgänge aktiviert sind, kann der APP-v-Client eine geladene Anwendung starten, auch wenn Sie nicht mit einem App-v-Verwaltungs Server verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="f1da9-353">When disconnected operations are enabled, the App-V client can start a loaded application even when it is not connected to an App-V Management Server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-354">FastConnectTimeout</span><span class="sxs-lookup"><span data-stu-id="f1da9-354">FastConnectTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-355">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-355">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-356">Standard = 1000</span><span class="sxs-lookup"><span data-stu-id="f1da9-356">Default=1000</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-357">Dieser Wert gibt das Timeout für TCP-Verbindungen in Millisekunden an, um zu bestimmen, wann der Modus für den getrennten Betrieb wechselt.</span><span class="sxs-lookup"><span data-stu-id="f1da9-357">This value specifies the TCP connect time-out in milliseconds to determine when to go into disconnected operations mode.</span></span> <span data-ttu-id="f1da9-358">Dieser Wert kann verwendet werden, um den standardmäßigen ConnectTimeout von 20 Sekunden (App-V Connect-Timeout für Netzwerktransaktionen) oder das TCP-Timeout des Systems von ca. 25 Sekunden zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="f1da9-358">This value can be used to override the default ConnectTimeout of 20 seconds (App-V connect time-out for network transactions) or the system’s TCP time-out of approximately 25 seconds.</span></span> <span data-ttu-id="f1da9-359">Dadurch wird der Client schnell in den getrennten Betriebsmodus versetzt.</span><span class="sxs-lookup"><span data-stu-id="f1da9-359">This brings the client into disconnected operations mode quickly.</span></span> <span data-ttu-id="f1da9-360">Auf die nächste Verbindung angewendet.</span><span class="sxs-lookup"><span data-stu-id="f1da9-360">Applied on the next connect.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-361">LimitDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="f1da9-361">LimitDisconnectedOperation</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-362">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-362">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-363">Standard = 1</span><span class="sxs-lookup"><span data-stu-id="f1da9-363">Default=1</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-364">Nur anwendbar, wenn AllowDisconnectedOperation 1 ist, aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f1da9-364">Applicable only if AllowDisconnectedOperation is 1, enabled.</span></span> <span data-ttu-id="f1da9-365">Dieser Wert bestimmt, ob es ein Zeitlimit für die Dauer des Client-Betriebs in getrennten Vorgängen geben wird.</span><span class="sxs-lookup"><span data-stu-id="f1da9-365">This value determines whether there will be a time limit for how long the client will be allowed to operate in disconnected operations.</span></span> <span data-ttu-id="f1da9-366">1 = limitiert.</span><span class="sxs-lookup"><span data-stu-id="f1da9-366">1=limited.</span></span> <span data-ttu-id="f1da9-367">0 = unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="f1da9-367">0=unlimited.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-368">DOTimeoutMinutes</span><span class="sxs-lookup"><span data-stu-id="f1da9-368">DOTimeoutMinutes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-369">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-369">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-370">Standard = 129600</span><span class="sxs-lookup"><span data-stu-id="f1da9-370">Default=129,600</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-371">Gibt an, wie viele Minuten eine Anwendung im getrennten Betriebsmodus verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f1da9-371">Indicates how many minutes an application may be used in disconnected operation mode.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f1da9-372">Die gültigen Werte sind 1 – 999999 in Tagen, ausgedrückt in Minuten (1 – 1439998560 Minuten).</span><span class="sxs-lookup"><span data-stu-id="f1da9-372">The valid values are 1–999,999 in days expressed in minutes (1–1,439,998,560 minutes).</span></span> <span data-ttu-id="f1da9-373">Der Standardwert ist 90 Tage oder 129.600 Minuten.</span><span class="sxs-lookup"><span data-stu-id="f1da9-373">The default value is 90 days or 129,600 minutes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-374">Protokoll</span><span class="sxs-lookup"><span data-stu-id="f1da9-374">Protocol</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-375">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-375">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-376">Standard = 8</span><span class="sxs-lookup"><span data-stu-id="f1da9-376">Default=8</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-377">Standardprotokoll für die Verwendung (TCP vs SSL).</span><span class="sxs-lookup"><span data-stu-id="f1da9-377">Default protocol to use (TCP vs SSL).</span></span> <span data-ttu-id="f1da9-378">Im Dialog Feld "Optionen" konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f1da9-378">Configure in Options Dialog.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-379">ReadTimeout</span><span class="sxs-lookup"><span data-stu-id="f1da9-379">ReadTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-380">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-380">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-381">20</span><span class="sxs-lookup"><span data-stu-id="f1da9-381">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-382">Lesen des Timeouts für Netzwerktransaktionen in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-382">Read time-out for network transactions, in seconds.</span></span> <span data-ttu-id="f1da9-383">Nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="f1da9-383">Do not modify.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-384">WriteTimeout</span><span class="sxs-lookup"><span data-stu-id="f1da9-384">WriteTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-385">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-385">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-386">20</span><span class="sxs-lookup"><span data-stu-id="f1da9-386">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-387">Schreiben Sie Timeout für Netzwerktransaktionen in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-387">Write time-out for network transactions, in seconds.</span></span> <span data-ttu-id="f1da9-388">Nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="f1da9-388">Do not modify.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-389">ConnectTimeout</span><span class="sxs-lookup"><span data-stu-id="f1da9-389">ConnectTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-390">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-390">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-391">20</span><span class="sxs-lookup"><span data-stu-id="f1da9-391">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-392">Verbinden Sie das Timeout für Netzwerktransaktionen in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-392">Connect time-out for network transactions, in seconds.</span></span> <span data-ttu-id="f1da9-393">Nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="f1da9-393">Do not modify.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-394">ReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="f1da9-394">ReestablishmentRetries</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-395">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-395">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-396">3</span><span class="sxs-lookup"><span data-stu-id="f1da9-396">3</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-397">Die Anzahl der Versuche, eine gelöschte Sitzung wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-397">The number of times to try to reestablish a dropped session.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-398">ReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="f1da9-398">ReestablishmentInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-399">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-399">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-400">15</span><span class="sxs-lookup"><span data-stu-id="f1da9-400">15</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-401">Die Anzahl der Sekunden, zwischen denen versucht wird, eine gelöschte Sitzung wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-401">The number of seconds to wait between tries to reestablish a dropped session.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f1da9-402">Http-Taste</span><span class="sxs-lookup"><span data-stu-id="f1da9-402">Http Key</span></span>


<span data-ttu-id="f1da9-403">Der HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\network\\http-Schlüssel steuert die Parameter, die sich auf HTTP-Streaming beziehen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-403">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\Http key controls the parameters that are related to Http streaming.</span></span> <span data-ttu-id="f1da9-404">Dieser Schlüssel wird hauptsächlich vom Netzwerktransport-Agent verwendet.</span><span class="sxs-lookup"><span data-stu-id="f1da9-404">This key is used primarily by the network transport agent.</span></span> <span data-ttu-id="f1da9-405">Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die dem http-Schlüssel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f1da9-405">The following table provides information about the registry values that are associated with the Http key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f1da9-406">Name</span><span class="sxs-lookup"><span data-stu-id="f1da9-406">Name</span></span> </th>
<th align="left"><span data-ttu-id="f1da9-407">Typ</span><span class="sxs-lookup"><span data-stu-id="f1da9-407">Type</span></span> </th>
<th align="left"><span data-ttu-id="f1da9-408">Daten (Beispiele)</span><span class="sxs-lookup"><span data-stu-id="f1da9-408">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="f1da9-409">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1da9-409">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-410">LaunchIfNotFound</span><span class="sxs-lookup"><span data-stu-id="f1da9-410">LaunchIfNotFound</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-411">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-411">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-412">Standard = 0</span><span class="sxs-lookup"><span data-stu-id="f1da9-412">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-413">Steuert das Verhalten des HTTP-Streaming, wenn eine Verbindung mit dem HTTP-Server hergestellt werden kann und die Paketdatei auf dem HTTP-Server nicht mehr vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f1da9-413">Controls the behavior of HTTP streaming when a connection to the HTTP server can be established and the package file no longer exists on the HTTP server.</span></span> <span data-ttu-id="f1da9-414">Wenn der Wert nicht vorhanden ist oder nicht auf 1 festgesetzt ist, können Sie mit dem App-V-Client keine Anwendung starten, die zuvor in den Cache geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="f1da9-414">If the value does not exist or if it is not set to 1, the App-V client does not let you launch an application that has previously been loaded into cache.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f1da9-415">1</span><span class="sxs-lookup"><span data-stu-id="f1da9-415">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-416">Wenn dieser Wert auf 1 festgesetzt ist, können Sie mit dem App-V-Client eine Anwendung starten, die zuvor in den Cache geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="f1da9-416">If this value is set to 1, the App-V client lets you launch an application that has previously been loaded into cache.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f1da9-417">Datei System Schlüssel</span><span class="sxs-lookup"><span data-stu-id="f1da9-417">File System Key</span></span>


<span data-ttu-id="f1da9-418">Die Werte, die unter dem HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\appfs-Schlüssel enthalten sind, steuern die Dateisystemparameter für App-V.</span><span class="sxs-lookup"><span data-stu-id="f1da9-418">The values that are contained under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS key control the file system parameters for App-V.</span></span> <span data-ttu-id="f1da9-419">Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die mit dem AppFS-Schlüssel verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="f1da9-419">The following table provides information about the registry values associated with the AppFS key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f1da9-420">Name</span><span class="sxs-lookup"><span data-stu-id="f1da9-420">Name</span></span> </th>
<th align="left"><span data-ttu-id="f1da9-421">Typ</span><span class="sxs-lookup"><span data-stu-id="f1da9-421">Type</span></span> </th>
<th align="left"><span data-ttu-id="f1da9-422">Daten (Beispiele)</span><span class="sxs-lookup"><span data-stu-id="f1da9-422">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="f1da9-423">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1da9-423">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-424">FileSize</span><span class="sxs-lookup"><span data-stu-id="f1da9-424">FileSize</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-425">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-425">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-426">4096</span><span class="sxs-lookup"><span data-stu-id="f1da9-426">4096</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-427">Maximale Größe in Megabytes der Dateisystemcache-Datei.</span><span class="sxs-lookup"><span data-stu-id="f1da9-427">Maximum size in megabytes of file system cache file.</span></span> <span data-ttu-id="f1da9-428">Wenn Sie diesen Wert in der Registrierung ändern, müssen Sie den Zustand auf 0 festlegen und einen Neustart durchführen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-428">If you change this value in the registry, you must set State to 0 and reboot.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-429">FileName</span><span class="sxs-lookup"><span data-stu-id="f1da9-429">FileName</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-430">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f1da9-430">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-431">C:\Users\Public\Documents\SoftGrid Client\sftfs.fsd</span><span class="sxs-lookup"><span data-stu-id="f1da9-431">C:\Users\Public\Documents\SoftGrid Client\sftfs.fsd</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-432">Speicherort der Dateisystem-Cache-Datei.</span><span class="sxs-lookup"><span data-stu-id="f1da9-432">Location of file system cache file.</span></span> <span data-ttu-id="f1da9-433">Wenn Sie diesen Wert in der Registrierung ändern, müssen Sie entweder die Dateigröße beibehalten und den Neustart durchführen oder den Status auf 0 festlegen und neu starten.</span><span class="sxs-lookup"><span data-stu-id="f1da9-433">If you change this value in the registry, you must either leave FileSize the same and reboot or set State to 0 and reboot.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-434">DriveLetter</span><span class="sxs-lookup"><span data-stu-id="f1da9-434">DriveLetter</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-435">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f1da9-435">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-436">F:</span><span class="sxs-lookup"><span data-stu-id="f1da9-436">Q:</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-437">Laufwerk, auf dem das App-V-Dateisystem bereitgestellt wird, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f1da9-437">Drive where App-V file system will be mounted, if it is available.</span></span> <span data-ttu-id="f1da9-438">Dieser Wert wird entweder vom Listener oder vom Installationsprogramm gesetzt und vom Dateisystem gelesen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-438">This value is set either by the listener or the installer, and it is read by the file system.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-439">Status</span><span class="sxs-lookup"><span data-stu-id="f1da9-439">State</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-440">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-440">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-441">0x100</span><span class="sxs-lookup"><span data-stu-id="f1da9-441">0x100</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-442">Status des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="f1da9-442">State of file system.</span></span> <span data-ttu-id="f1da9-443">Legen Sie den Wert 0 fest, und starten Sie den Dateisystemcache vollständig.</span><span class="sxs-lookup"><span data-stu-id="f1da9-443">Set to 0 and reboot to completely clear the file system cache.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-444">FileSystemStorage</span><span class="sxs-lookup"><span data-stu-id="f1da9-444">FileSystemStorage</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-445">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f1da9-445">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-446">C:\Profiles\Joe\SG</span><span class="sxs-lookup"><span data-stu-id="f1da9-446">C:\Profiles\Joe\SG</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-447">Pfad für Symlinks, die unter HKCU.</span><span class="sxs-lookup"><span data-stu-id="f1da9-447">Path for symlinks, set under HKCU.</span></span> <span data-ttu-id="f1da9-448">Ändern Sie nicht (verwenden Sie das Datenverzeichnis unter Konfiguration, um es zu ändern).</span><span class="sxs-lookup"><span data-stu-id="f1da9-448">Do not modify (use data directory under Configuration to change).</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-449">GlobalFileSystemStorage</span><span class="sxs-lookup"><span data-stu-id="f1da9-449">GlobalFileSystemStorage</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-450">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f1da9-450">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-451">C:\Users\Public\Documents\SoftGrid Client\AppFS-Speicher</span><span class="sxs-lookup"><span data-stu-id="f1da9-451">C:\Users\Public\Documents\SoftGrid Client\AppFS Storage</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-452">Pfad für globale Dateisystem Daten.</span><span class="sxs-lookup"><span data-stu-id="f1da9-452">Path for global file system data.</span></span> <span data-ttu-id="f1da9-453">Nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="f1da9-453">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-454">MaxPercentToLockInCache</span><span class="sxs-lookup"><span data-stu-id="f1da9-454">MaxPercentToLockInCache</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-455">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-455">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-456">Standard = 90</span><span class="sxs-lookup"><span data-stu-id="f1da9-456">Default=90</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-457">Gibt den maximalen Prozentsatz der Dateisystem-Cachedatei an, die gesperrt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f1da9-457">Specifies the maximum percentage of the file system cache file that can be locked.</span></span> <span data-ttu-id="f1da9-458">Nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="f1da9-458">Do not modify.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-459">UnloadLeastRecentlyUsed</span><span class="sxs-lookup"><span data-stu-id="f1da9-459">UnloadLeastRecentlyUsed</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-460">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-460">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-461">Standard = 1</span><span class="sxs-lookup"><span data-stu-id="f1da9-461">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-462">Das Speicher Verwaltungsfeature "Dateisystem-Cache" verwendet einen am wenigsten zuletzt verwendeten Algorithmus (LRU) und ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f1da9-462">The file system cache space management feature uses a Least Recently Used (LRU) algorithm and is enabled by default.</span></span> <span data-ttu-id="f1da9-463">Wenn der Platz, der für ein neues Paket erforderlich ist, den verfügbaren freien Speicherplatz im Cache überschreitet, verwendet der App-V-Client dieses Feature, um zu ermitteln, welche, falls vorhanden, vorhandene Pakete aus dem Cache löschen können, um Platz für das neue Paket zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-463">If the space that is required for a new package would exceed the available free space in the cache, the App-V Client uses this feature to determine which, if any, existing packages it can delete from the cache to make room for the new package.</span></span> <span data-ttu-id="f1da9-464">Der Client löscht das Paket mit dem ältesten Datum des letzten Zugriffs, wenn es älter als der im Registrierungswert MinPkgAge angegebene Wert ist.</span><span class="sxs-lookup"><span data-stu-id="f1da9-464">The client deletes the package with the oldest last-accessed date if it is older than the value specified in the MinPkgAge registry value.</span></span> <span data-ttu-id="f1da9-465">Werte sind 0 (deaktiviert) und 1 (Standard, aktiviert).</span><span class="sxs-lookup"><span data-stu-id="f1da9-465">Values are 0 (disabled) and 1 (default, enabled).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-466">MinPackageAge</span><span class="sxs-lookup"><span data-stu-id="f1da9-466">MinPackageAge</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-467">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-467">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-468">1</span><span class="sxs-lookup"><span data-stu-id="f1da9-468">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-469">Wenn Sie feststellen möchten, wann das Paket für verwerfen ausgewählt werden kann, legen Sie diesen Registrierungswert auf die minimale Anzahl von Tagen fest, die Sie verstreichen möchten, nachdem das Paket zuletzt zugegriffen wurde.</span><span class="sxs-lookup"><span data-stu-id="f1da9-469">To determine when the package can be selected for discard, set this registry value to equal the minimum number of days you want to elapse since the package was last accessed.</span></span> <span data-ttu-id="f1da9-470">Pakete, die in letzter Zeit verwendet wurden, werden nicht verworfen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-470">Packages that have been used more recently are not discarded.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f1da9-471">Berechtigungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="f1da9-471">Permissions Key</span></span>


<span data-ttu-id="f1da9-472">Um zu verhindern, dass Benutzer Fehler machen, können Administratoren den HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\permissions-Schlüssel verwenden, um den Zugriff auf einige Aktionen für nicht administrative Benutzer zu steuern, beispielsweise um zu verhindern, dass Benutzer versehentlich Programme entladen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-472">To help to prevent users from making mistakes, administrators can use the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions key to control access to some actions for non-administrative users—for example, to prevent users from accidentally unloading programs.</span></span> <span data-ttu-id="f1da9-473">Benutzer mit Administratorrechten können sich eine dieser Berechtigungen erteilen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-473">Users with administrative rights can give themselves any of these permissions.</span></span> <span data-ttu-id="f1da9-474">Achten Sie bei freigegebenen Systemen wie einem Host für Remotedesktopsitzungen-Server (ehemals Terminal Server) auf die Verwendung von zusätzlichen Berechtigungen für Benutzer, da einige dieser Berechtigungen es Benutzern ermöglichen, die Anwendungen zu steuern, die von allen Benutzern im System verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-474">On shared systems, such as a Remote Desktop Session Host (RD Session Host) server (formerly Terminal Server) system, be careful when granting additional permissions to users because some of these permissions would enable users to control the applications used by all users on the system.</span></span> <span data-ttu-id="f1da9-475">Mögliche Werte für diese Einstellungen sind 1 (Allow) und 0 (Disallow).</span><span class="sxs-lookup"><span data-stu-id="f1da9-475">Possible values for these settings are 1 (allow) and 0 (disallow).</span></span>

<span data-ttu-id="f1da9-476">Die Einstellungen für den Berechtigungsschlüssel Steuern alle Schnittstellen, die die benannten Aktionen ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-476">The Permissions key settings control all interfaces that enable the named actions.</span></span> <span data-ttu-id="f1da9-477">Dazu gehören das Dialog Feld Optionen, SFTTray und SFTMime.</span><span class="sxs-lookup"><span data-stu-id="f1da9-477">This includes the Options Dialog, SFTTray, and SFTMime.</span></span> <span data-ttu-id="f1da9-478">Diese Einstellungen wirken sich nicht auf Administratoren aus.</span><span class="sxs-lookup"><span data-stu-id="f1da9-478">These settings do not affect administrators.</span></span> <span data-ttu-id="f1da9-479">Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die mit dem Berechtigungsschlüssel verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="f1da9-479">The following table provides information about the registry values associated with the Permissions key.</span></span>

<span data-ttu-id="f1da9-480">Name Type Data (Beispiele) Beschreibung ChangeFSDrive</span><span class="sxs-lookup"><span data-stu-id="f1da9-480">Name Type Data (Examples) Description ChangeFSDrive</span></span>

<span data-ttu-id="f1da9-481">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-481">DWORD</span></span>

<span data-ttu-id="f1da9-482">Standard = 0</span><span class="sxs-lookup"><span data-stu-id="f1da9-482">Default=0</span></span>

<span data-ttu-id="f1da9-483">Der Wert 1 ermöglicht es Benutzern, einen anderen Laufwerkbuchstaben auszuwählen, der als Dateisystemlaufwerk verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1da9-483">A value of 1 allows users to pick a different drive letter to be used as the file system drive.</span></span>

<span data-ttu-id="f1da9-484">ChangeCacheSize</span><span class="sxs-lookup"><span data-stu-id="f1da9-484">ChangeCacheSize</span></span>

<span data-ttu-id="f1da9-485">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-485">DWORD</span></span>

<span data-ttu-id="f1da9-486">Standard = 0</span><span class="sxs-lookup"><span data-stu-id="f1da9-486">Default=0</span></span>

<span data-ttu-id="f1da9-487">Der Wert 1 ermöglicht Benutzern, die Cachegröße zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f1da9-487">A value of 1 allows users to change the cache size.</span></span>

<span data-ttu-id="f1da9-488">ChangeLogSettings</span><span class="sxs-lookup"><span data-stu-id="f1da9-488">ChangeLogSettings</span></span>

<span data-ttu-id="f1da9-489">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-489">DWORD</span></span>

<span data-ttu-id="f1da9-490">Standard = 0</span><span class="sxs-lookup"><span data-stu-id="f1da9-490">Default=0</span></span>

<span data-ttu-id="f1da9-491">Der Wert 1 ermöglicht Benutzern, die Protokollebene zu ändern, deren Speicherort zu ändern und Sie über die Benutzeroberfläche zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-491">A value of 1 allows users to modify the log level, change its location, and reset it through the user interface.</span></span>

<span data-ttu-id="f1da9-492">AddApp</span><span class="sxs-lookup"><span data-stu-id="f1da9-492">AddApp</span></span>

<span data-ttu-id="f1da9-493">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-493">DWORD</span></span>

<span data-ttu-id="f1da9-494">Standard = 0</span><span class="sxs-lookup"><span data-stu-id="f1da9-494">Default=0</span></span>

<span data-ttu-id="f1da9-495">Mit dem Wert 1 können Benutzer Anwendungen explizit hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-495">A value of 1 allows users to add applications explicitly.</span></span> <span data-ttu-id="f1da9-496">Dies wirkt sich nicht auf Anwendungen aus, die über die Veröffentlichungsaktualisierung hinzugefügt werden, und es wird verhindert, dass Benutzer Anwendungen starten (und dadurch implizit hinzufügen), die noch nicht hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-496">This does not affect applications that are added through publishing refresh nor does it prevent users from starting (and thereby implicitly adding) applications that have not already been added.</span></span> <span data-ttu-id="f1da9-497">Werte sind 0 oder 1.</span><span class="sxs-lookup"><span data-stu-id="f1da9-497">Values are 0 or 1.</span></span>

<span data-ttu-id="f1da9-498">LoadApp</span><span class="sxs-lookup"><span data-stu-id="f1da9-498">LoadApp</span></span> 

<span data-ttu-id="f1da9-499">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-499">DWORD</span></span> 

<span data-ttu-id="f1da9-500">0</span><span class="sxs-lookup"><span data-stu-id="f1da9-500">0</span></span>

<span data-ttu-id="f1da9-501">Ermöglicht es einem Benutzer nicht, eine Anwendung zu laden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-501">Does not allow a user to load an application.</span></span> <span data-ttu-id="f1da9-502">Dies ist die Standardeinstellung für Host für Remotedesktopsitzungen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-502">This is the default for RD Session Hosts.</span></span> <span data-ttu-id="f1da9-503">Wenn Sie ein mobiler Benutzer sind, möchten Sie möglicherweise Ihre Anwendungen im Cache vollständig laden, um Sie während des getrennten Betriebs oder Offlinemodus zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-503">If you are a mobile user, you might want to fully load your applications in the cache to use them during disconnected operation or offline mode.</span></span> <span data-ttu-id="f1da9-504">Damit Anwendungen vom APP-v-Verwaltungsserver oder vom APP-v-Streamingserver gestreamt werden können, müssen Sie mit einem Server verbunden sein, um Anwendungen zu laden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-504">To stream applications from the App-V Management Server or the App-V Streaming Server, you must be connected to a server to load applications.</span></span>

<span data-ttu-id="f1da9-505">1</span><span class="sxs-lookup"><span data-stu-id="f1da9-505">1</span></span>

<span data-ttu-id="f1da9-506">Ermöglicht einem Benutzer das Laden einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="f1da9-506">Allows a user to load an application.</span></span> <span data-ttu-id="f1da9-507">Dies ist die Standardeinstellung für Windows-Desktops.</span><span class="sxs-lookup"><span data-stu-id="f1da9-507">This is the default for Windows desktops.</span></span> 

<span data-ttu-id="f1da9-508">UnloadApp</span><span class="sxs-lookup"><span data-stu-id="f1da9-508">UnloadApp</span></span> 

<span data-ttu-id="f1da9-509">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-509">DWORD</span></span> 

<span data-ttu-id="f1da9-510">0</span><span class="sxs-lookup"><span data-stu-id="f1da9-510">0</span></span>

<span data-ttu-id="f1da9-511">Ermöglicht es einem Benutzer nicht, eine Anwendung zu entladen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-511">Does not allow a user to unload an application.</span></span> <span data-ttu-id="f1da9-512">Beim Laden oder Entladen eines Pakets werden alle Anwendungen im Paket in den Cache geladen oder daraus entfernt.</span><span class="sxs-lookup"><span data-stu-id="f1da9-512">When you load or unload a package, all the applications in the package are loaded into or removed from cache.</span></span>

<span data-ttu-id="f1da9-513">1</span><span class="sxs-lookup"><span data-stu-id="f1da9-513">1</span></span>

<span data-ttu-id="f1da9-514">Ermöglicht es einem Benutzer, eine Anwendung zu entladen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-514">Allows a user to unload an application.</span></span> 

<span data-ttu-id="f1da9-515">LockApp</span><span class="sxs-lookup"><span data-stu-id="f1da9-515">LockApp</span></span> 

<span data-ttu-id="f1da9-516">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-516">DWORD</span></span> 

<span data-ttu-id="f1da9-517">0</span><span class="sxs-lookup"><span data-stu-id="f1da9-517">0</span></span>

<span data-ttu-id="f1da9-518">Der Benutzer kann keine Anwendung sperren und entsperren.</span><span class="sxs-lookup"><span data-stu-id="f1da9-518">Does not allow a user to lock and unlock an application.</span></span> <span data-ttu-id="f1da9-519">Dies ist die Standardeinstellung für Host für Remotedesktopsitzungen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-519">This is the default for RD Session Hosts.</span></span> <span data-ttu-id="f1da9-520">Eine gesperrte Anwendung kann nicht aus dem Cache entfernt werden, um Platz für neue Anwendungen zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-520">A locked application cannot be removed from the cache to make room for new applications.</span></span> <span data-ttu-id="f1da9-521">Wenn Sie eine gesperrte Anwendung vom App-V-Desktop oder-Client für Remote Desktop Dienste (ehemals Terminal Dienste)-Cache entfernen möchten, müssen Sie die Sperre aufheben.</span><span class="sxs-lookup"><span data-stu-id="f1da9-521">To remove a locked application from the App-V Desktop or Client for Remote Desktop Services (formerly Terminal Services) cache, you must unlock it.</span></span>

<span data-ttu-id="f1da9-522">1</span><span class="sxs-lookup"><span data-stu-id="f1da9-522">1</span></span>

<span data-ttu-id="f1da9-523">Ermöglicht einem Benutzer das Sperren und Entsperren einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="f1da9-523">Allows a user to lock and unlock an application.</span></span> <span data-ttu-id="f1da9-524">Dies ist die Standardeinstellung für Windows-Desktops.</span><span class="sxs-lookup"><span data-stu-id="f1da9-524">This is the default for Windows Desktops.</span></span> 

<span data-ttu-id="f1da9-525">ManageTypes</span><span class="sxs-lookup"><span data-stu-id="f1da9-525">ManageTypes</span></span> 

<span data-ttu-id="f1da9-526">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-526">DWORD</span></span> 

<span data-ttu-id="f1da9-527">0</span><span class="sxs-lookup"><span data-stu-id="f1da9-527">0</span></span>

<span data-ttu-id="f1da9-528">Ermöglicht es einem Benutzer nicht, nur Dateitypzuordnungen für diesen Benutzer hinzuzufügen, zu bearbeiten oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-528">Does not allow a user to add, edit, or remove file type associations for that User alone.</span></span> <span data-ttu-id="f1da9-529">Dies ist die Standardeinstellung für Host für Remotedesktopsitzungen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-529">This is the default for RD Session Hosts.</span></span> 

<span data-ttu-id="f1da9-530">1</span><span class="sxs-lookup"><span data-stu-id="f1da9-530">1</span></span>

<span data-ttu-id="f1da9-531">Ermöglicht einem Benutzer das Hinzufügen, bearbeiten und Entfernen von Dateitypzuordnungen für diesen Benutzer und nicht global.</span><span class="sxs-lookup"><span data-stu-id="f1da9-531">Allows a user to add, edit, and remove file type associations for that user only and not globally.</span></span> <span data-ttu-id="f1da9-532">Dies ist die Standardeinstellung für Windows-Desktops.</span><span class="sxs-lookup"><span data-stu-id="f1da9-532">This is the default for Windows Desktops.</span></span> 

<span data-ttu-id="f1da9-533">RefreshServer</span><span class="sxs-lookup"><span data-stu-id="f1da9-533">RefreshServer</span></span> 

<span data-ttu-id="f1da9-534">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-534">DWORD</span></span> 

<span data-ttu-id="f1da9-535">0</span><span class="sxs-lookup"><span data-stu-id="f1da9-535">0</span></span>

<span data-ttu-id="f1da9-536">Ermöglicht es einem Benutzer nicht, eine Aktualisierung der MIME-Einstellungen auszulösen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-536">Does not allow a user to trigger a refresh of MIME settings.</span></span> <span data-ttu-id="f1da9-537">Dies ist die Standardeinstellung für Host für Remotedesktopsitzungen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-537">This is the default for RD Session Hosts.</span></span> 

<span data-ttu-id="f1da9-538">1</span><span class="sxs-lookup"><span data-stu-id="f1da9-538">1</span></span>

<span data-ttu-id="f1da9-539">Ermöglicht einem Benutzer das Auslösen einer Aktualisierung der MIME-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-539">Enables a user to trigger a refresh of MIME settings.</span></span> <span data-ttu-id="f1da9-540">Dies ist die Standardeinstellung für Windows-Desktops.</span><span class="sxs-lookup"><span data-stu-id="f1da9-540">This is the default for Windows Desktops.</span></span> 

<span data-ttu-id="f1da9-541">UpdateOSDFile</span><span class="sxs-lookup"><span data-stu-id="f1da9-541">UpdateOSDFile</span></span>

<span data-ttu-id="f1da9-542">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-542">DWORD</span></span>

<span data-ttu-id="f1da9-543">Standard = 0</span><span class="sxs-lookup"><span data-stu-id="f1da9-543">Default= 0</span></span>

<span data-ttu-id="f1da9-544">Der Wert 1 ermöglicht einem Benutzer die Verwendung einer geänderten OSD-Datei.</span><span class="sxs-lookup"><span data-stu-id="f1da9-544">A value of 1 enables a user to use a modified OSD file.</span></span>

<span data-ttu-id="f1da9-545">ImportApp</span><span class="sxs-lookup"><span data-stu-id="f1da9-545">ImportApp</span></span> 

<span data-ttu-id="f1da9-546">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-546">DWORD</span></span> 

<span data-ttu-id="f1da9-547">0</span><span class="sxs-lookup"><span data-stu-id="f1da9-547">0</span></span>

<span data-ttu-id="f1da9-548">Der Benutzer kann Anwendungen nicht in den Cache importieren.</span><span class="sxs-lookup"><span data-stu-id="f1da9-548">Does not allow a user to import applications into cache.</span></span> <span data-ttu-id="f1da9-549">Der Unterschied zwischen laden und importieren besteht darin, dass der Client beim Auslösen einer Last das Paket von dem aktuell konfigurierten Speicherort erhält, der in der OSD-, ASR-oder override-URL enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="f1da9-549">The difference between Load and Import is that when a Load is triggered, the client gets the package from the currently configured location contained in the OSD, ASR, or Override URL.</span></span> <span data-ttu-id="f1da9-550">Bei Verwendung von Import muss ein Speicherort angegeben werden, von dem das Paket abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1da9-550">When using Import, a location to get the package from must be specified.</span></span> 

<span data-ttu-id="f1da9-551">1</span><span class="sxs-lookup"><span data-stu-id="f1da9-551">1</span></span>

<span data-ttu-id="f1da9-552">Ermöglicht es einem Benutzer, Anwendungen in den Cache zu importieren.</span><span class="sxs-lookup"><span data-stu-id="f1da9-552">Allows a user to import applications into cache.</span></span> 

<span data-ttu-id="f1da9-553">ChangeRefreshSettings</span><span class="sxs-lookup"><span data-stu-id="f1da9-553">ChangeRefreshSettings</span></span>

<span data-ttu-id="f1da9-554">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-554">DWORD</span></span>

<span data-ttu-id="f1da9-555">Standard = 0</span><span class="sxs-lookup"><span data-stu-id="f1da9-555">Default=0</span></span>

<span data-ttu-id="f1da9-556">Der Wert 1 ermöglicht Benutzern, die Aktualisierungseinstellungen für Server zu ändern (Aktualisierung bei der Anmeldung und periodische Aktualisierung).</span><span class="sxs-lookup"><span data-stu-id="f1da9-556">A value of 1 allows users to modify the refresh settings for servers (refresh on login and periodic refresh).</span></span> <span data-ttu-id="f1da9-557">Dies bedeutet nicht, dass der Benutzer andere Servereinstellungen (Pfad, Host usw.) ändern kann.</span><span class="sxs-lookup"><span data-stu-id="f1da9-557">This does not imply that the user can modify other server settings (path, host, and so on).</span></span>

<span data-ttu-id="f1da9-558">ManageServers</span><span class="sxs-lookup"><span data-stu-id="f1da9-558">ManageServers</span></span>

<span data-ttu-id="f1da9-559">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-559">DWORD</span></span>

<span data-ttu-id="f1da9-560">Standard = 0</span><span class="sxs-lookup"><span data-stu-id="f1da9-560">Default=0</span></span>

<span data-ttu-id="f1da9-561">Der Wert 1 ermöglicht dem Benutzer das Hinzufügen, bearbeiten und Entfernen von Servern, mit Ausnahme der Bearbeitung der Aktualisierungseinstellungen, die durch die ChangeRefreshSettings-Berechtigung gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-561">A value of 1 allows the user to add, edit, and remove servers, except for editing the refresh settings, which is controlled by the ChangeRefreshSettings permission.</span></span>

<span data-ttu-id="f1da9-562">PublishShortcut</span><span class="sxs-lookup"><span data-stu-id="f1da9-562">PublishShortcut</span></span>

<span data-ttu-id="f1da9-563">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-563">DWORD</span></span>

<span data-ttu-id="f1da9-564">Standard = 0</span><span class="sxs-lookup"><span data-stu-id="f1da9-564">Default=0</span></span>

<span data-ttu-id="f1da9-565">Der Wert 1 ermöglicht Benutzern das Veröffentlichen von Verknüpfungen über die Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="f1da9-565">A value of 1 allows users to publish shortcuts through the user interface.</span></span> <span data-ttu-id="f1da9-566">Dies wirkt sich nicht auf Tastenkombinationen aus, die während einer Veröffentlichungsaktualisierung veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-566">This does not affect shortcuts that are published during a publishing refresh.</span></span>

<span data-ttu-id="f1da9-567">ViewAllApplications</span><span class="sxs-lookup"><span data-stu-id="f1da9-567">ViewAllApplications</span></span>

<span data-ttu-id="f1da9-568">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-568">DWORD</span></span>

<span data-ttu-id="f1da9-569">Standard = 0</span><span class="sxs-lookup"><span data-stu-id="f1da9-569">Default=0</span></span>

<span data-ttu-id="f1da9-570">Der Wert 1 zeigt alle Anwendungen über die Benutzeroberfläche an; Andernfalls werden nur die Anwendungen des Benutzers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f1da9-570">A value of 1 displays all applications through the user interface; otherwise, only the user’s applications are displayed.</span></span>

<span data-ttu-id="f1da9-571">RepairApp</span><span class="sxs-lookup"><span data-stu-id="f1da9-571">RepairApp</span></span>

<span data-ttu-id="f1da9-572">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-572">DWORD</span></span>

<span data-ttu-id="f1da9-573">Standard = 1</span><span class="sxs-lookup"><span data-stu-id="f1da9-573">Default=1</span></span>

<span data-ttu-id="f1da9-574">Der Wert 1 ermöglicht es dem Benutzer, die Reparaturaktion für Anwendungen in SFTMime oder der Client Verwaltungskonsole zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-574">A value of 1 allows the user to use the Repair action on applications in SFTMime or the Client Management Console.</span></span> <span data-ttu-id="f1da9-575">Wenn Sie eine Anwendung reparieren, werden alle benutzerdefinierten Benutzereinstellungen entfernt und die Standardeinstellungen wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="f1da9-575">When you repair an application, you remove any custom user settings and restore the default settings.</span></span> <span data-ttu-id="f1da9-576">Mit dieser Aktion werden keine Verknüpfungen oder Dateitypzuordnungen geändert oder gelöscht, und die Anwendung wird nicht aus dem Cache entfernt.</span><span class="sxs-lookup"><span data-stu-id="f1da9-576">This action does not change or delete shortcuts or file type associations, and it does not remove the application from cache.</span></span>

<span data-ttu-id="f1da9-577">ClearApp</span><span class="sxs-lookup"><span data-stu-id="f1da9-577">ClearApp</span></span>

<span data-ttu-id="f1da9-578">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-578">DWORD</span></span>

<span data-ttu-id="f1da9-579">Standard = 1</span><span class="sxs-lookup"><span data-stu-id="f1da9-579">Default=1</span></span>

<span data-ttu-id="f1da9-580">Der Wert 1 ermöglicht es dem Benutzer, die klare Aktion für Anwendungen in SFTMime oder der Client Verwaltungskonsole zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-580">A value of 1 allows the user to use the Clear action on applications in SFTMime or the Client Management Console.</span></span> <span data-ttu-id="f1da9-581">Wenn Sie eine Anwendung von der Konsole löschen, können Sie diese Anwendung nicht mehr verwenden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-581">When you clear an application from the console, you can no longer use that application.</span></span> <span data-ttu-id="f1da9-582">Die Anwendung verbleibt jedoch im Cache und steht weiterhin anderen Benutzern im gleichen System zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="f1da9-582">However, the application remains in cache and is still available to other users on the same system.</span></span> <span data-ttu-id="f1da9-583">Nach einer Veröffentlichungsaktualisierung werden die gelöschten Anwendungen wieder zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="f1da9-583">After a publishing refresh, the cleared applications will again become available to you.</span></span>

<span data-ttu-id="f1da9-584">DeleteApp</span><span class="sxs-lookup"><span data-stu-id="f1da9-584">DeleteApp</span></span>

<span data-ttu-id="f1da9-585">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-585">DWORD</span></span>

<span data-ttu-id="f1da9-586">Standard = 0</span><span class="sxs-lookup"><span data-stu-id="f1da9-586">Default=0</span></span>

<span data-ttu-id="f1da9-587">Der Wert 1 ermöglicht es dem Benutzer, die Löschaktion für Anwendungen in SFTMime oder der Client Verwaltungskonsole zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-587">A value of 1 allows the user to use the Delete action on applications in SFTMime or the Client Management Console.</span></span> <span data-ttu-id="f1da9-588">Wenn Sie eine Anwendung löschen, steht die ausgewählte Anwendung nicht mehr für alle Benutzer dieses Clients zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="f1da9-588">When you delete an application, the selected application will no longer be available to any users on that client.</span></span> <span data-ttu-id="f1da9-589">Verknüpfungen und Dateitypzuordnungen werden gelöscht, und die Anwendung wird aus dem Cache gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f1da9-589">Shortcuts and file type associations are deleted and the application is deleted from cache.</span></span> <span data-ttu-id="f1da9-590">Wenn sich eine andere Anwendung jedoch auf Daten im Dateisystem-Cache oder auf Einstellungsdaten für die ausgewählte Anwendung bezieht, werden diese Elemente nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f1da9-590">However, if another application refers to data in the file system cache or settings data for the selected application, these items will not be deleted.</span></span>

<span data-ttu-id="f1da9-591">Nach einer Veröffentlichungsaktualisierung werden die gelöschten Anwendungen wieder zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="f1da9-591">After a publishing refresh, the deleted applications will again become available to you.</span></span>

<span data-ttu-id="f1da9-592">ToggleOfflineMode</span><span class="sxs-lookup"><span data-stu-id="f1da9-592">ToggleOfflineMode</span></span>

<span data-ttu-id="f1da9-593">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-593">DWORD</span></span>

<span data-ttu-id="f1da9-594">Mit dem Wert 1 können die Benutzer auswählen, dass der Client im Offline Modus ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1da9-594">A value of 1 allows the users to select to run the client in Offline Mode.</span></span> <span data-ttu-id="f1da9-595">Im Offline Modus kann der Application Virtualization-Client eine geladene Anwendung starten, auch wenn Sie nicht mit einem Application Virtualization Server verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="f1da9-595">In Offline Mode, the Application Virtualization client can start a loaded application even when it is not connected to an Application Virtualization Server.</span></span>



## <span data-ttu-id="f1da9-596">Benutzerdefinierte Einstellungen</span><span class="sxs-lookup"><span data-stu-id="f1da9-596">Custom Settings</span></span>


<span data-ttu-id="f1da9-597">Der HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\customsettings-Schlüssel enthält Werte, die für Front-End-Komponenten spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="f1da9-597">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\CustomSettings key contains values specific to front-end components.</span></span> <span data-ttu-id="f1da9-598">Alle benutzerdefinierten Einstellungen werden als Zeichenfolgen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f1da9-598">All custom settings are stored as strings.</span></span> <span data-ttu-id="f1da9-599">Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die mit dem CustomSettings-Schlüssel verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="f1da9-599">The following table provides information about the registry values associated with the CustomSettings key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f1da9-600">Name</span><span class="sxs-lookup"><span data-stu-id="f1da9-600">Name</span></span> </th>
<th align="left"><span data-ttu-id="f1da9-601">Typ</span><span class="sxs-lookup"><span data-stu-id="f1da9-601">Type</span></span> </th>
<th align="left"><span data-ttu-id="f1da9-602">Daten (Beispiele)</span><span class="sxs-lookup"><span data-stu-id="f1da9-602">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="f1da9-603">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1da9-603">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-604">TrayErrorDelay</span><span class="sxs-lookup"><span data-stu-id="f1da9-604">TrayErrorDelay</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-605">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-605">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-606">Standard = 30</span><span class="sxs-lookup"><span data-stu-id="f1da9-606">Default=30</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-607">Zeit in Sekunden, in der der Application Virtualization-Benachrichtigungsbereich Fehlermeldungen wie "starten" nicht angezeigt wird &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="f1da9-607">Time in seconds that the Application Virtualization notification area will display error messages like &quot;Launch failed&quot;.</span></span> <span data-ttu-id="f1da9-608">Minimaler Wert von 1.</span><span class="sxs-lookup"><span data-stu-id="f1da9-608">Minimum value of 1.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-609">TraySuccessDelay</span><span class="sxs-lookup"><span data-stu-id="f1da9-609">TraySuccessDelay</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-610">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-610">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-611">Standard = 10</span><span class="sxs-lookup"><span data-stu-id="f1da9-611">Default=10</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f1da9-612">Zeit in Sekunden, in der im appvmed-Benachrichtigungsbereich Erfolgsmeldungen wie &quot; Word gestartet &quot; oder &quot; Excel heruntergefahren angezeigt werden &quot; .</span><span class="sxs-lookup"><span data-stu-id="f1da9-612">Time in seconds that the appvmed notification area will display success messages like &quot;Word launched&quot; or &quot;Excel shut down&quot;.</span></span> <span data-ttu-id="f1da9-613">Wenn 0, werden diese Nachrichten unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="f1da9-613">If 0, those messages will be suppressed.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-614">TrayVisibility</span><span class="sxs-lookup"><span data-stu-id="f1da9-614">TrayVisibility</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-615">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-615">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-616">Standard = 0</span><span class="sxs-lookup"><span data-stu-id="f1da9-616">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-617">0 = Anzeige Fach, wenn virtualisierte Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1da9-617">0=Show Tray when virtualized applications are in use.</span></span></p>
<p><span data-ttu-id="f1da9-618">1 = Anzeige Fach immer anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-618">1=Show Tray always.</span></span></p>
<p><span data-ttu-id="f1da9-619">2 = niemals Fach anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-619">2=Never show Tray.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-620">TrayShowRefresh</span><span class="sxs-lookup"><span data-stu-id="f1da9-620">TrayShowRefresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-621">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-621">DWORD</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f1da9-622">Wenn präsentieren und auf einen Wert von 1 gesetzt ist, kann die Aktualisierung von Menüelement Anwendungen im Menü "Taskleiste" angezeigt werden, und der Benutzer kann darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-622">When present and set to a value of 1, allows menu item Refresh Applications to be displayed on the Tray menu and is accessible by the user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-623">TrayShowLoad</span><span class="sxs-lookup"><span data-stu-id="f1da9-623">TrayShowLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-624">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-624">DWORD</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f1da9-625">Wenn Present und auf einen Wert von 1 gesetzt ist, können Menüelement Lade Anwendungen im Menü "Taskleiste" angezeigt werden, und der Benutzer kann darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-625">When present and set to a value of 1, allows menu item Load Applications to be displayed on the Tray menu and is accessible by the user.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f1da9-626">Berichterstellungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="f1da9-626">Reporting Settings</span></span>


<span data-ttu-id="f1da9-627">Der HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\reporting-Schlüssel enthält Werte, die für die Berichterstellung an einen App-V-Verwaltungs Server spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="f1da9-627">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Reporting key contains values specific to reporting to an App-V Management Server.</span></span> <span data-ttu-id="f1da9-628">Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die dem Berichterstattungs Schlüssel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f1da9-628">The following table provides information about the registry values associated with the Reporting key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f1da9-629">Name</span><span class="sxs-lookup"><span data-stu-id="f1da9-629">Name</span></span> </th>
<th align="left"><span data-ttu-id="f1da9-630">Typ</span><span class="sxs-lookup"><span data-stu-id="f1da9-630">Type</span></span> </th>
<th align="left"><span data-ttu-id="f1da9-631">Daten (Beispiele)</span><span class="sxs-lookup"><span data-stu-id="f1da9-631">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="f1da9-632">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1da9-632">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1da9-633">DataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="f1da9-633">DataCacheLimit</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-634">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-634">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-635">Standard = 20</span><span class="sxs-lookup"><span data-stu-id="f1da9-635">Default=20</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-636">Dieser Wert gibt die maximale Größe in Megabyte (MB) des XML-Caches zum Speichern von Berichtsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="f1da9-636">This value specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="f1da9-637">Die Größe bezieht sich auf den Cache im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="f1da9-637">The size applies to the cache in memory.</span></span> <span data-ttu-id="f1da9-638">Wenn das Limit erreicht ist, wird die Protokolldatei überschrieben.</span><span class="sxs-lookup"><span data-stu-id="f1da9-638">When the limit is reached, the log file will roll over.</span></span> <span data-ttu-id="f1da9-639">Wenn ein neuer Eintrag hinzugefügt wird (unten in der Liste), werden mindestens einer der ältesten Datensätze (oben in der Liste) gelöscht, um Platz zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="f1da9-639">When a new record is added (bottom of the list), one or more of the oldest records (top of the list) will be deleted to make room.</span></span> <span data-ttu-id="f1da9-640">Beim ersten auftreten wird eine Warnung in das Client Protokoll und das Ereignisprotokoll protokolliert, und es wird erst wieder protokolliert, nachdem der Cache bei der Übertragung erfolgreich gelöscht wurde und das Protokoll erneut gefüllt wurde.</span><span class="sxs-lookup"><span data-stu-id="f1da9-640">A warning will be logged to the Client log and the event log the first time this occurs, and it will not be logged again until after the cache has been successfully cleared on transmission and the log has filled up again.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1da9-641">Datablocking</span><span class="sxs-lookup"><span data-stu-id="f1da9-641">DataBlockSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-642">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1da9-642">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-643">Standard = 65536</span><span class="sxs-lookup"><span data-stu-id="f1da9-643">Default=65536</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1da9-644">Dieser Wert gibt die maximale Größe in Bytes an, die bei der Veröffentlichungsaktualisierung an den Server gesendet werden soll, um permanente Übertragungsfehler zu vermeiden, wenn das Protokoll eine signifikante Größe erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="f1da9-644">This value specifies the maximum size in bytes to transmit to the server at once on publishing refresh, to avoid permanent transmission failures when the log has reached a significant size.</span></span> <span data-ttu-id="f1da9-645">Der Standardwert ist 65536.</span><span class="sxs-lookup"><span data-stu-id="f1da9-645">The default value is 65536.</span></span> <span data-ttu-id="f1da9-646">Wenn Berichtsdaten an den Server übertragen werden, wird ein Block von Anwendungsdatensätzen, die kleiner oder gleich der Blockgröße in Bytes von XML-Daten sind, aus dem Cache entfernt und an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="f1da9-646">When transmitting report data to the server, one block of application records—less than or equal to the block size in bytes of XML data—will be removed from the cache and sent to the server.</span></span> <span data-ttu-id="f1da9-647">Jedem Block werden die allgemeinen Client Daten und die globalen Paket Listendaten vorangestellt, und diese werden nicht in die Berechnung der Blockgröße einbezogen; Es besteht die Möglichkeit, dass eine extrem große Paketliste zu Übertragungsfehlern bei geringer Bandbreite oder unzuverlässigen Verbindungen führt.</span><span class="sxs-lookup"><span data-stu-id="f1da9-647">Each block will have the general Client data and global package list data prepended, and these will not factor into the block size calculations; the potential exists for an extremely large package list to result in transmission failures over low bandwidth or unreliable connections.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f1da9-648">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="f1da9-648">Related topics</span></span>


[<span data-ttu-id="f1da9-649">Application Virtualization Client-Referenz</span><span class="sxs-lookup"><span data-stu-id="f1da9-649">Application Virtualization Client Reference</span></span>](application-virtualization-client-reference.md)









