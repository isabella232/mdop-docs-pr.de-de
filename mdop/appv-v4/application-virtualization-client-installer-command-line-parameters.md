---
title: Befehlszeilenparameter von Application Virtualization Client Installer
description: Befehlszeilenparameter von Application Virtualization Client Installer
author: dansimp
ms.assetid: 508fa404-52a5-4919-8788-2a3dfb00639b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 911d333c80060c1881c96430c1d2d0516b6a4855
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808019"
---
# <span data-ttu-id="60444-103">Befehlszeilenparameter von Application Virtualization Client Installer</span><span class="sxs-lookup"><span data-stu-id="60444-103">Application Virtualization Client Installer Command-Line Parameters</span></span>


<span data-ttu-id="60444-104">In der folgenden Tabelle sind alle verfügbaren Befehlszeilenparameter für Microsoft Application Virtualization Client Installer, deren Werte und eine kurze Beschreibung der einzelnen Parameter aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="60444-104">The following table lists all available Microsoft Application Virtualization Client installer command-line parameters, their values, and a brief description of each parameter.</span></span> <span data-ttu-id="60444-105">Bei Parametern wird die Groß-/Kleinschreibung beachtet und muss als Großbuchstaben eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="60444-105">Parameters are case-sensitive and must be entered as all-uppercase letters.</span></span> <span data-ttu-id="60444-106">Alle Parameterwerte müssen in doppelten Anführungszeichen eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="60444-106">All parameter values must be enclosed in double quotes.</span></span>

**<span data-ttu-id="60444-107">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="60444-107">Note</span></span>**  
-   <span data-ttu-id="60444-108">Für App-V, Version 4,6, können Befehlszeilenparameter während eines Clientupgrades nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60444-108">For App-V version 4.6, command-line parameters cannot be used during a client upgrade.</span></span>

-   <span data-ttu-id="60444-109">Die Parameter *SWICACHESIZE* und *MINFREESPACEMB* können nicht in der Befehlszeile kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="60444-109">The *SWICACHESIZE* and *MINFREESPACEMB* parameters cannot be combined on the command line.</span></span> <span data-ttu-id="60444-110">Wenn beide verwendet werden, wird der *SWICACHESIZE* -Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="60444-110">If both are used, the *SWICACHESIZE* parameter will be ignored.</span></span>



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="60444-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="60444-111">Parameter</span></span></th>
<th align="left"><span data-ttu-id="60444-112">Werte</span><span class="sxs-lookup"><span data-stu-id="60444-112">Values</span></span></th>
<th align="left"><span data-ttu-id="60444-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60444-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="60444-114">ALLOWINDEPENDENTFILESTREAMING</span><span class="sxs-lookup"><span data-stu-id="60444-114">ALLOWINDEPENDENTFILESTREAMING</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-115">TRUE</span><span class="sxs-lookup"><span data-stu-id="60444-115">TRUE</span></span></p>
<p><span data-ttu-id="60444-116">FALSE</span><span class="sxs-lookup"><span data-stu-id="60444-116">FALSE</span></span></p></td>
<td align="left"><p><span data-ttu-id="60444-117">Gibt an, ob das Streaming aus einer Datei unabhängig davon aktiviert wird, wie der Client mit dem <em> ApplicationSourceRoot </em> -Parameter konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="60444-117">Indicates whether streaming from file will be enabled regardless of how the client has been configured with the <em>APPLICATIONSOURCEROOT</em> parameter.</span></span> <span data-ttu-id="60444-118">Ist dieser Wert auf "false" festgelegt, wird durch den Transport kein Streaming aus Dateien möglich, auch wenn der OSD-HREF-oder der <em> ApplicationSourceRoot- </em> Parameter einen Dateipfad enthält.</span><span class="sxs-lookup"><span data-stu-id="60444-118">If set to FALSE, the transport will not enable streaming from files even if the OSD HREF or the <em>APPLICATIONSOURCEROOT</em> parameter contains a file path.</span></span></p>
<p><span data-ttu-id="60444-119">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="60444-119">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="60444-120">TRUE – die manuell bereitgestellte Anwendung wird möglicherweise vom Datenträger geladen.</span><span class="sxs-lookup"><span data-stu-id="60444-120">TRUE—Manually deployed application may be loaded from disk.</span></span></p></li>
<li><p><span data-ttu-id="60444-121">Falsch: alle Anwendungen müssen vom Quell Streamingserver stammen.</span><span class="sxs-lookup"><span data-stu-id="60444-121">FALSE—All applications must come from source streaming server.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="60444-122">ApplicationSourceRoot</span><span class="sxs-lookup"><span data-stu-id="60444-122">APPLICATIONSOURCEROOT</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-123">RTSP:// <em> </em> -URL (für dynamische Paketzustellung)</span><span class="sxs-lookup"><span data-stu-id="60444-123">RTSP:// <em>URL</em> (for dynamic package delivery)</span></span></p>
<p><span data-ttu-id="60444-124">File:// <em> URL </em> oder <em> UNC </em> (für das Laden aus der Dateipaket Zustellung)</span><span class="sxs-lookup"><span data-stu-id="60444-124">File:// <em>URL</em> or <em>UNC</em> (for load from file package delivery)</span></span></p></td>
<td align="left"><p><span data-ttu-id="60444-125">Um einem Administrator oder einem elektronischen Softwareverteilungssystem zu ermöglichen, sicherzustellen, dass das Laden der Anwendung in Übereinstimmung mit dem Topologieverwaltung-Schema durchgeführt wird, ist es möglich, die OSD-CodeBase für das Application href-Element (den Quellspeicherort) zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="60444-125">To enable an administrator or an electronic software distribution system to ensure that application loading is performed in compliance with the topology management scheme, allows an override of the OSD CODEBASE for the application HREF element (the source location).</span></span> <span data-ttu-id="60444-126">Wenn der Wert "" ist, der Standardwert ist, werden die vorhandenen OSD-Datei Einstellungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="60444-126">If the value is “”, which is the default value, the existing OSD file settings are used.</span></span></p>
<p><span data-ttu-id="60444-127">Eine URL besteht aus mehreren Teilen:</span><span class="sxs-lookup"><span data-stu-id="60444-127">A URL has several parts:</span></span></p>
<p><span data-ttu-id="60444-128">&lt;Protokoll &gt; :// &lt; Server &gt; : &lt; Port &gt; / &lt; Pfad &gt; / &lt; ? Abfrage &gt; &lt; #Fragment&gt;</span><span class="sxs-lookup"><span data-stu-id="60444-128">&lt;protocol&gt;://&lt;server&gt;:&lt;port&gt;/&lt;path&gt;/&lt;?query&gt;&lt;#fragment&gt;</span></span></p>
<p><span data-ttu-id="60444-129">Ein UNC-Pfad besteht aus drei Teilen:</span><span class="sxs-lookup"><span data-stu-id="60444-129">A UNC path has three parts:</span></span></p>
<p><span data-ttu-id="60444-130">&amp;lt; Computername &gt; &amp; lt; Freigabeordner &gt; &amp; lt; Ressource&gt;</span><span class="sxs-lookup"><span data-stu-id="60444-130">&amp;lt;computername&gt;&amp;lt;share folder&gt;&amp;lt;resource&gt;</span></span></p>
<p><span data-ttu-id="60444-131">Wenn der <em> ApplicationSourceRoot </em> -Parameter auf einem Client angegeben wird, unterbricht der Client die URL oder den UNC-Pfad aus einer OSD-Datei in seine Bestandteile und ersetzt die OSD-Abschnitte durch die entsprechenden <em> ApplicationSourceRoot- </em> Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="60444-131">If the <em>APPLICATIONSOURCEROOT</em> parameter is specified on a client, the client will break the URL or UNC path from an OSD file into its constituent parts and replace the OSD sections with the corresponding <em>APPLICATIONSOURCEROOT</em> sections.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="60444-132">Wichtig</span><span class="sxs-lookup"><span data-stu-id="60444-132">Important</span></span></strong><br/><p><span data-ttu-id="60444-133">Achten Sie darauf, das richtige Format zu verwenden, wenn Sie file://mit einem UNC-Pfad verwenden.</span><span class="sxs-lookup"><span data-stu-id="60444-133">Be sure to use the correct format when using file:// with a UNC path.</span></span> <span data-ttu-id="60444-134">Das richtige Format ist file:// &amp; lt; Server &gt; &amp; lt; freigeben &gt; .</span><span class="sxs-lookup"><span data-stu-id="60444-134">The correct format is file://&amp;lt;server&gt;&amp;lt;share&gt;.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="60444-135">IconSourceRoot</span><span class="sxs-lookup"><span data-stu-id="60444-135">ICONSOURCEROOT</span></span></em></p></td>
<td align="left"><p><em><span data-ttu-id="60444-136">UNC</span><span class="sxs-lookup"><span data-stu-id="60444-136">UNC</span></span></em></p>
<p><span data-ttu-id="60444-137">HTTP:// <em> URL- </em> oder https://- <em> URL</span><span class="sxs-lookup"><span data-stu-id="60444-137">HTTP://<em>URL</em> or HTTPS://<em>URL</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-138">Ermöglicht einem Administrator die Angabe eines Quellspeicherorts für den Symbol Abruf eines sequenzierten Anwendungspakets während der Veröffentlichung.</span><span class="sxs-lookup"><span data-stu-id="60444-138">Enables an administrator to specify a source location for icon retrieval for a sequenced application package during publication.</span></span> <span data-ttu-id="60444-139">Symbol Quellen Stämme unterstützen UNC-Pfade und-URLs (http oder HTTPS).</span><span class="sxs-lookup"><span data-stu-id="60444-139">Icon source roots support UNC paths and URLs (HTTP or HTTPS).</span></span> <span data-ttu-id="60444-140">Wenn der Wert "" ist, der Standardwert ist, werden die vorhandenen OSD-Datei Einstellungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="60444-140">If the value is “”, which is the default value, the existing OSD file settings are used.</span></span></p>
<p><span data-ttu-id="60444-141">Eine URL besteht aus mehreren Teilen:</span><span class="sxs-lookup"><span data-stu-id="60444-141">A URL has several parts:</span></span></p>
<p><span data-ttu-id="60444-142">&lt;Protokoll &gt; :// &lt; Server &gt; : &lt; Port &gt; / &lt; Pfad &gt; / &lt; ? Abfrage &gt; &lt; #Fragment&gt;</span><span class="sxs-lookup"><span data-stu-id="60444-142">&lt;protocol&gt;://&lt;server&gt;:&lt;port&gt;/&lt;path&gt;/&lt;?query&gt;&lt;#fragment&gt;</span></span></p>
<p><span data-ttu-id="60444-143">Ein UNC-Pfad besteht aus drei Teilen:</span><span class="sxs-lookup"><span data-stu-id="60444-143">A UNC path has three parts:</span></span></p>
<p><span data-ttu-id="60444-144">&amp;lt; Computername &gt; &amp; lt; Freigabeordner &gt; &amp; lt; Ressource&gt;</span><span class="sxs-lookup"><span data-stu-id="60444-144">&amp;lt;computername&gt;&amp;lt;share folder&gt;&amp;lt;resource&gt;</span></span></p>
<div class="alert">
<strong><span data-ttu-id="60444-145">Wichtig</span><span class="sxs-lookup"><span data-stu-id="60444-145">Important</span></span></strong><br/><p><span data-ttu-id="60444-146">Achten Sie beim Verwenden eines UNC-Pfads darauf, das richtige Format zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="60444-146">Be sure to use the correct format when using a UNC path.</span></span> <span data-ttu-id="60444-147">Zulässige Formate sind &amp; lt; Server &gt; &amp; lt; Freigabe &gt; &lt; -oder Laufwerkbuchstabe &gt; : &amp; lt; Folder &gt; .</span><span class="sxs-lookup"><span data-stu-id="60444-147">Acceptable formats are &amp;lt;server&gt;&amp;lt;share&gt; or &lt;drive letter&gt;:&amp;lt;folder&gt;.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="60444-148">OSDSourceRoot</span><span class="sxs-lookup"><span data-stu-id="60444-148">OSDSOURCEROOT</span></span></em></p></td>
<td align="left"><p><em><span data-ttu-id="60444-149">UNC</span><span class="sxs-lookup"><span data-stu-id="60444-149">UNC</span></span></em></p>
<p><span data-ttu-id="60444-150">HTTP:// <em> URL- </em> oder https://- <em> URL</span><span class="sxs-lookup"><span data-stu-id="60444-150">HTTP://<em>URL</em> or HTTPS://<em>URL</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-151">Ermöglicht einem Administrator die Angabe eines Quellspeicherorts für den Abruf von OSD-Dateien für ein Anwendungspaket während der Veröffentlichung.</span><span class="sxs-lookup"><span data-stu-id="60444-151">Enables an administrator to specify a source location for OSD file retrieval for an application package during publication.</span></span> <span data-ttu-id="60444-152">OSD-Quell Stämme unterstützen UNC-Pfade und-URLs (http oder HTTPS).</span><span class="sxs-lookup"><span data-stu-id="60444-152">OSD source roots support UNC paths and URLs (HTTP or HTTPS).</span></span> <span data-ttu-id="60444-153">Wenn der Wert "" ist, der Standardwert ist, werden die vorhandenen OSD-Datei Einstellungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="60444-153">If the value is “”, which is the default value, the existing OSD file settings are used.</span></span></p>
<p><span data-ttu-id="60444-154">Eine URL besteht aus mehreren Teilen:</span><span class="sxs-lookup"><span data-stu-id="60444-154">A URL has several parts:</span></span></p>
<p><span data-ttu-id="60444-155">&lt;Protokoll &gt; :// &lt; Server &gt; : &lt; Port &gt; / &lt; Pfad &gt; / &lt; ? Abfrage &gt; &lt; #Fragment&gt;</span><span class="sxs-lookup"><span data-stu-id="60444-155">&lt;protocol&gt;://&lt;server&gt;:&lt;port&gt;/&lt;path&gt;/&lt;?query&gt;&lt;#fragment&gt;</span></span></p>
<p><span data-ttu-id="60444-156">Ein UNC-Pfad besteht aus drei Teilen:</span><span class="sxs-lookup"><span data-stu-id="60444-156">A UNC path has three parts:</span></span></p>
<p><span data-ttu-id="60444-157">&amp;lt; Computername &gt; &amp; lt; Freigabeordner &gt; &amp; lt; Ressource&gt;</span><span class="sxs-lookup"><span data-stu-id="60444-157">&amp;lt;computername&gt;&amp;lt;share folder&gt;&amp;lt;resource&gt;</span></span></p>
<div class="alert">
<strong><span data-ttu-id="60444-158">Wichtig</span><span class="sxs-lookup"><span data-stu-id="60444-158">Important</span></span></strong><br/><p><span data-ttu-id="60444-159">Achten Sie beim Verwenden eines UNC-Pfads darauf, das richtige Format zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="60444-159">Be sure to use the correct format when using a UNC path.</span></span> <span data-ttu-id="60444-160">Zulässige Formate sind &amp; lt; Server &gt; &amp; lt; Freigabe &gt; &lt; -oder Laufwerkbuchstabe &gt; : &amp; lt; Folder &gt; .</span><span class="sxs-lookup"><span data-stu-id="60444-160">Acceptable formats are &amp;lt;server&gt;&amp;lt;share&gt; or &lt;drive letter&gt;:&amp;lt;folder&gt;.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="60444-161">AUTOLOADONLOGIN</span><span class="sxs-lookup"><span data-stu-id="60444-161">AUTOLOADONLOGIN</span></span></em></p>
<p><em><span data-ttu-id="60444-162">AUTOLOADONLAUNCH</span><span class="sxs-lookup"><span data-stu-id="60444-162">AUTOLOADONLAUNCH</span></span></em></p>
<p><em><span data-ttu-id="60444-163">AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="60444-163">AUTOLOADONREFRESH</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-164">[0 | 1]</span><span class="sxs-lookup"><span data-stu-id="60444-164">[0|1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="60444-165">Die Trigger zum automatischen Laden definieren die Ereignisse, die das automatische Laden von Anwendungen initiieren.</span><span class="sxs-lookup"><span data-stu-id="60444-165">The AutoLoad triggers that define the events that initiate auto-loading of applications.</span></span> <span data-ttu-id="60444-166">Beim Laden wird implizit Hintergrund Streaming verwendet, damit die Anwendung vollständig in den Cache geladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="60444-166">AutoLoad implicitly uses background streaming to enable the application to be fully loaded into cache.</span></span></p>
<p><span data-ttu-id="60444-167">Der primäre Feature-Block wird so schnell wie möglich geladen.</span><span class="sxs-lookup"><span data-stu-id="60444-167">The primary feature block will be loaded as quickly as possible.</span></span> <span data-ttu-id="60444-168">Verbleibende Funktionsbausteine werden in den Hintergrund geladen, um Vordergrund Vorgänge wie Benutzerinteraktionen mit Anwendungen zu ermöglichen, um Vorrang zu haben und eine optimale Leistung zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="60444-168">Remaining feature blocks will be loaded in the background to enable foreground operations, such as user interaction with applications, to take priority and provide optimal performance.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="60444-169">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="60444-169">Note</span></span></strong><br/><p><span data-ttu-id="60444-170">Der <em> AUTOLOADTARGET </em> -Parameter bestimmt, welche Anwendungen automatisch geladen werden.</span><span class="sxs-lookup"><span data-stu-id="60444-170">The <em>AUTOLOADTARGET</em> parameter determines which applications are auto-loaded.</span></span> <span data-ttu-id="60444-171">Standardmäßig werden Pakete, die verwendet wurden, automatisch geladen, es sei denn, <em> AUTOLOADTARGET </em> ist festzulegen.</span><span class="sxs-lookup"><span data-stu-id="60444-171">By default, packages that have been used are auto-loaded unless <em>AUTOLOADTARGET</em> is set.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="60444-172">Jeder Parameter wirkt sich auf das Ladeverhalten wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="60444-172">Each parameter affects loading behavior as follows:</span></span></p>
<ul>
<li><p><em><span data-ttu-id="60444-173">AUTOLOADONLOGIN </em> – das Laden beginnt, wenn sich der Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="60444-173">AUTOLOADONLOGIN</em>—Loading starts when the user logs in.</span></span></p></li>
<li><p><em><span data-ttu-id="60444-174">AUTOLOADONLAUNCH </em> – das Laden beginnt, wenn der Benutzer eine Anwendung startet.</span><span class="sxs-lookup"><span data-stu-id="60444-174">AUTOLOADONLAUNCH</em>—Loading starts when the user starts an application.</span></span></p></li>
<li><p><em><span data-ttu-id="60444-175">AUTOLOADONREFRESH </em> – das Laden beginnt, wenn eine Veröffentlichungsaktualisierung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="60444-175">AUTOLOADONREFRESH</em>—Loading starts when a publishing refresh occurs.</span></span></p></li>
</ul>
<p><span data-ttu-id="60444-176">Die drei Werte können kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="60444-176">The three values can be combined.</span></span> <span data-ttu-id="60444-177">Im folgenden Beispiel werden die Trigger für das Laden sowohl bei der Benutzeranmeldung als auch bei der Veröffentlichungsaktualisierung aktiviert:</span><span class="sxs-lookup"><span data-stu-id="60444-177">In the following example, AutoLoad triggers are enabled both at user login and when publishing refresh occurs:</span></span></p>
<p><em><span data-ttu-id="60444-178">AUTOLOADONLOGIN AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="60444-178">AUTOLOADONLOGIN AUTOLOADONREFRESH</span></span></em></p>
<div class="alert">
<strong><span data-ttu-id="60444-179">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="60444-179">Note</span></span></strong><br/><p><span data-ttu-id="60444-180">Wenn der Client bei der ersten Installation mit diesen Werten konfiguriert ist, wird das Programm automatisch erst ausgelöst, wenn sich der Benutzer das nächste Mal anmeldet und sich wieder anmeldet.</span><span class="sxs-lookup"><span data-stu-id="60444-180">If the client is configured with these values at first install, Autoload will not be triggered until the next time the user logs off and logs back on.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="60444-181">AUTOLOADTARGET</span><span class="sxs-lookup"><span data-stu-id="60444-181">AUTOLOADTARGET</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-182">Keine</span><span class="sxs-lookup"><span data-stu-id="60444-182">NONE</span></span></p>
<p><span data-ttu-id="60444-183">Alle</span><span class="sxs-lookup"><span data-stu-id="60444-183">ALL</span></span></p>
<p><span data-ttu-id="60444-184">PREVUSED</span><span class="sxs-lookup"><span data-stu-id="60444-184">PREVUSED</span></span></p></td>
<td align="left"><p><span data-ttu-id="60444-185">Gibt an, was automatisch geladen wird, wenn ein bestimmter Trigger für das automatische Laden eintritt.</span><span class="sxs-lookup"><span data-stu-id="60444-185">Indicates what will be auto-loaded when any given AutoLoad triggers occur.</span></span></p>
<p><span data-ttu-id="60444-186">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="60444-186">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="60444-187">Keine – kein automatisches Laden, unabhängig davon, welche Trigger festzulegen sind.</span><span class="sxs-lookup"><span data-stu-id="60444-187">NONE—No auto-loading, regardless of what triggers might be set.</span></span></p></li>
<li><p><span data-ttu-id="60444-188">Alle – wenn ein automatischer Trigger aktiviert ist, werden alle Pakete automatisch geladen, unabhängig davon, ob Sie jemals gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="60444-188">ALL—If any AutoLoad trigger is enabled, all packages are automatically loaded, whether or not they have ever been launched.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="60444-189">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="60444-189">Note</span></span></strong><br/><p><span data-ttu-id="60444-190">Diese Einstellung ist für einzelne Pakete mithilfe der <strong> Befehle SFTMIME hinzufügen </strong> und <strong> Paket konfigurieren konfiguriert </strong> .</span><span class="sxs-lookup"><span data-stu-id="60444-190">This setting is configured for individual packages by using the SFTMIME <strong>ADD PACKAGE</strong> and <strong>CONFIGURE PACKAGE</strong> commands.</span></span> <span data-ttu-id="60444-191">Weitere Informationen zu diesen Befehlen finden Sie unter <a href="sftmime--command-reference.md" data-raw-source="[SFTMIME Command Reference](sftmime--command-reference.md)"> Befehlsreferenz für SFTMIME </a> .</span><span class="sxs-lookup"><span data-stu-id="60444-191">For more information about these commands, see <a href="sftmime--command-reference.md" data-raw-source="[SFTMIME Command Reference](sftmime--command-reference.md)">SFTMIME Command Reference</a>.</span></span></p>
</div>
<div>

</div></li>
<li><p><span data-ttu-id="60444-192">PREVUSED – wenn ein automatischer Trigger aktiviert ist, laden Sie nur die Pakete, bei denen mindestens eine Anwendung im Paket zuvor verwendet wurde (also gestartet oder vorab gespeichert wurde).</span><span class="sxs-lookup"><span data-stu-id="60444-192">PREVUSED—If any AutoLoad trigger is enabled, load only the packages where at least one application in the package has been previously used (that is, launched or precached).</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="60444-193">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="60444-193">Note</span></span></strong><br/><p><span data-ttu-id="60444-194">Wenn Sie den App-V-Client installieren, um einen schreibgeschützten Cache zu verwenden (beispielsweise als VDI-Server Implementierung), müssen Sie den AUTOLOADTARGET-Parameter auf None setzen, um zu verhindern, dass <em> </em> der Client versucht, Anwendungen im schreibgeschützten Cache zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="60444-194">When you install the App-V client to use a read-only cache, (for example, as a VDI server implementation), you must set the <em>AUTOLOADTARGET</em> parameter to NONE to prevent the client from trying to update applications in the read-only cache.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="60444-195">DOTIMEOUTMINUTES</span><span class="sxs-lookup"><span data-stu-id="60444-195">DOTIMEOUTMINUTES</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-196">29600 (Standard)</span><span class="sxs-lookup"><span data-stu-id="60444-196">29600 (default)</span></span></p>
<p><span data-ttu-id="60444-197">1 – 1439998560 Minuten (Bereich)</span><span class="sxs-lookup"><span data-stu-id="60444-197">1–1439998560 minutes (range)</span></span></p></td>
<td align="left"><p><span data-ttu-id="60444-198">Gibt an, wie viele Minuten eine Anwendung im getrennten Betrieb verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="60444-198">Indicates how many minutes an application may be used in disconnected operation.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="60444-199">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="60444-199">INSTALLDIR</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-200">&lt;Pfadname&gt;</span><span class="sxs-lookup"><span data-stu-id="60444-200">&lt;pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="60444-201">Gibt das Installationsverzeichnis des App-V-Clients an.</span><span class="sxs-lookup"><span data-stu-id="60444-201">Specifies the installation directory of the App-V Client.</span></span></p>
<p><span data-ttu-id="60444-202">Beispiel: INSTALLDIR = &quot; c:\Programme\Microsoft Application Virtualization Client&quot;</span><span class="sxs-lookup"><span data-stu-id="60444-202">Example: INSTALLDIR=&quot;C:\Program Files\Microsoft Application Virtualization Client&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="60444-203">OPTIN</span><span class="sxs-lookup"><span data-stu-id="60444-203">OPTIN</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-204">TRUE</span><span class="sxs-lookup"><span data-stu-id="60444-204">“TRUE”</span></span></p>
<p><span data-ttu-id="60444-205">“”</span><span class="sxs-lookup"><span data-stu-id="60444-205">“”</span></span></p></td>
<td align="left"><p><span data-ttu-id="60444-206">Microsoft Application Virtualization-Client Komponenten werden durch Microsoft Update aktualisiert, wenn Updates für die allgemeine Öffentlichkeit zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="60444-206">Microsoft Application Virtualization Client components will be upgradable through Microsoft Update when updates are made available to the general public.</span></span> <span data-ttu-id="60444-207">Der auf Windows-Betriebssystemen installierte Microsoft Update-Agent setzt voraus, dass ein Benutzer sich ausdrücklich für die Nutzung des Diensts entscheidet.</span><span class="sxs-lookup"><span data-stu-id="60444-207">The Microsoft Update Agent installed on Windows operating systems requires a user to explicitly opt-in to use the service.</span></span> <span data-ttu-id="60444-208">Dieser Opt-in ist nur einmal für alle Anwendungen auf dem Gerät erforderlich.</span><span class="sxs-lookup"><span data-stu-id="60444-208">This opt-in is required only one time for all applications on the device.</span></span> <span data-ttu-id="60444-209">Wenn Sie sich bereits für Microsoft Update entschieden haben, nutzen die Microsoft Application Virtualization-Komponenten auf dem Gerät automatisch die Vorteile des Diensts.</span><span class="sxs-lookup"><span data-stu-id="60444-209">If you have already opted into Microsoft Update, the Microsoft Application Virtualization components on the device will automatically take advantage of the service.</span></span></p>
<p><span data-ttu-id="60444-210">Bei der Befehlszeileninstallation ist die Verwendung von Microsoft Update standardmäßig deaktiviert (es sei denn, eine vorherige Anwendung hat bereits die Aktivierung des Geräts ermöglicht), da Sie die manuelle Entscheidung für Microsoft Update erforderlich machen.</span><span class="sxs-lookup"><span data-stu-id="60444-210">For command-line installation, use of Microsoft Update is by default opt-out (unless a previous application already enabled the device to be opted in) due to the requirement for manually opting into Microsoft Update.</span></span> <span data-ttu-id="60444-211">Daher muss die Entscheidung für Befehlszeileninstallationen explizit sein.</span><span class="sxs-lookup"><span data-stu-id="60444-211">Therefore, opting in must be explicit for command-line installations.</span></span> <span data-ttu-id="60444-212">Wenn der Befehlszeilenparameter <em> optin </em> auf true festgelegt wird, muss die Microsoft Update-Option festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="60444-212">Setting the command-line parameter <em>OPTIN</em> to TRUE forces the Microsoft Update opt-in to be set.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="60444-213">RequireAuthorizationIfCached</span><span class="sxs-lookup"><span data-stu-id="60444-213">REQUIREAUTHORIZATIONIFCACHED</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-214">TRUE</span><span class="sxs-lookup"><span data-stu-id="60444-214">TRUE</span></span></p>
<p><span data-ttu-id="60444-215">FALSE</span><span class="sxs-lookup"><span data-stu-id="60444-215">FALSE</span></span></p></td>
<td align="left"><p><span data-ttu-id="60444-216">Gibt an, ob immer eine Autorisierung erforderlich ist, unabhängig davon, ob sich eine Anwendung bereits im Cache befindet.</span><span class="sxs-lookup"><span data-stu-id="60444-216">Indicates whether authorization is always required, whether or not an application is already in cache.</span></span></p>
<p><span data-ttu-id="60444-217">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="60444-217">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="60444-218">TRUE – die Anwendung muss beim Start immer autorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="60444-218">TRUE—Application always must be authorized at startup.</span></span> <span data-ttu-id="60444-219">Für RTSP-Streaming-Anwendungen wird das Benutzerautorisierungstoken zur Autorisierung an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="60444-219">For RTSP streamed applications, the user authorization token is sent to the server for authorization.</span></span> <span data-ttu-id="60444-220">Bei dateibasierten Anwendungen diktieren Datei-ACLs, ob ein Benutzer auf die Anwendung zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="60444-220">For file-based applications, file ACLs dictate whether a user may access the application.</span></span></p></li>
<li><p><span data-ttu-id="60444-221">FALSE: versuchen Sie immer, eine Verbindung mit dem Server herzustellen.</span><span class="sxs-lookup"><span data-stu-id="60444-221">FALSE—Always try to connect to the server.</span></span> <span data-ttu-id="60444-222">Wenn keine Verbindung mit dem Server hergestellt werden kann, ermöglicht der Client dem Benutzer weiterhin, eine Anwendung zu starten, die zuvor in den Cache geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="60444-222">If a connection to the server cannot be established, the client still allows the user to launch an application that has previously been loaded into cache.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="60444-223">SWICACHESIZE</span><span class="sxs-lookup"><span data-stu-id="60444-223">SWICACHESIZE</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-224">Cache Größe in MB</span><span class="sxs-lookup"><span data-stu-id="60444-224">Cache size in MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="60444-225">Gibt die Größe des Clientcaches in Megabyte an.</span><span class="sxs-lookup"><span data-stu-id="60444-225">Specifies the size in megabytes of the client cache.</span></span> <span data-ttu-id="60444-226">Die Standardgröße ist 4096 MB, und die maximale Größe beträgt 1.048.576 MB (1 TB).</span><span class="sxs-lookup"><span data-stu-id="60444-226">The default size is 4096 MB, and the maximum size is 1,048,576 MB (1 TB).</span></span> <span data-ttu-id="60444-227">Das System überprüft den verfügbaren Speicherplatz zur Installationszeit, aber der Platz ist nicht reserviert.</span><span class="sxs-lookup"><span data-stu-id="60444-227">The system checks for the available space at installation time, but the space is not reserved.</span></span></p>
<p><span data-ttu-id="60444-228">Beispiel: <strong> SWICACHESIZE = &quot; 1024&quot;</span><span class="sxs-lookup"><span data-stu-id="60444-228">Example: <strong>SWICACHESIZE=&quot;1024&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="60444-229">SWIPUBSVRDISPLAY</span><span class="sxs-lookup"><span data-stu-id="60444-229">SWIPUBSVRDISPLAY</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-230">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="60444-230">Display name</span></span></p></td>
<td align="left"><p><span data-ttu-id="60444-231">Gibt den angezeigten Namen des Veröffentlichungsservers an; erforderlich <em> , wenn SWIPUBSVRHOST </em> verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="60444-231">Specifies the displayed name of the publishing server; required when <em>SWIPUBSVRHOST</em> is used.</span></span></p>
<p><span data-ttu-id="60444-232">Beispiel: <strong> SWIPUBSVRDISPLAY = &quot; Produktionsumgebung&quot;</span><span class="sxs-lookup"><span data-stu-id="60444-232">Example: <strong>SWIPUBSVRDISPLAY=&quot;PRODUCTION ENVIRONMENT&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="60444-233">SWIPUBSVRTYPE</span><span class="sxs-lookup"><span data-stu-id="60444-233">SWIPUBSVRTYPE</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-234">[Http | RTSP</span><span class="sxs-lookup"><span data-stu-id="60444-234">[HTTP|RTSP]</span></span></p></td>
<td align="left"><p><span data-ttu-id="60444-235">Gibt den Typ des Veröffentlichungsservers an.</span><span class="sxs-lookup"><span data-stu-id="60444-235">Specifies the publishing server type.</span></span> <span data-ttu-id="60444-236">Der Standard Servertyp ist Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="60444-236">The default server type is Application Virtualization Server.</span></span> <span data-ttu-id="60444-237"><strong>Bei der/Secure </strong> -Option wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="60444-237">The <strong>/secure</strong> switch is not case sensitive.</span></span></p>
<ul>
<li><p><span data-ttu-id="60444-238">Http – Standard-HTTP-Server</span><span class="sxs-lookup"><span data-stu-id="60444-238">HTTP—Standard HTTP Server</span></span></p></li>
<li><p><span data-ttu-id="60444-239">Http <strong> </strong> -/Secure – Enhanced Security http Server</span><span class="sxs-lookup"><span data-stu-id="60444-239">HTTP <strong>/secure</strong>—Enhanced Security HTTP Server</span></span></p></li>
<li><p><span data-ttu-id="60444-240">RTSP – Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="60444-240">RTSP—Application Virtualization Server</span></span></p></li>
<li><p><span data-ttu-id="60444-241">RTSP <strong> /Secure </strong> – Enhanced Security Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="60444-241">RTSP <strong>/secure</strong>—Enhanced Security Application Virtualization Server</span></span></p></li>
</ul>
<p><span data-ttu-id="60444-242">Beispiel: <strong> SWIPUBSVRTYPE = &quot; http-/Secure&quot;</span><span class="sxs-lookup"><span data-stu-id="60444-242">Example: <strong>SWIPUBSVRTYPE=&quot;HTTP /secure&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="60444-243">SWIPUBSVRHOST</span><span class="sxs-lookup"><span data-stu-id="60444-243">SWIPUBSVRHOST</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-244">IP-Adresse | hostname</span><span class="sxs-lookup"><span data-stu-id="60444-244">IP address|host name</span></span></p></td>
<td align="left"><p><span data-ttu-id="60444-245">Gibt entweder die IP-Adresse des Application Virtualization Server oder einen Hostnamen des Servers an, der in die IP-Adresse des Servers&#39;s aufgelöst wird; erforderlich <em> , wenn SWIPUBSVRDISPLAY </em> verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="60444-245">Specifies either the IP address of the Application Virtualization Server or a host name of the server that resolves into the server&#39;s IP address; required when <em>SWIPUBSVRDISPLAY</em> is used.</span></span></p>
<p><span data-ttu-id="60444-246">Beispiel: <strong> SWIPUBSVRHOST = &quot; Server01&quot;</span><span class="sxs-lookup"><span data-stu-id="60444-246">Example: <strong>SWIPUBSVRHOST=&quot;SERVER01&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="60444-247">SWIPUBSVRPORT</span><span class="sxs-lookup"><span data-stu-id="60444-247">SWIPUBSVRPORT</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-248">Port Nummer</span><span class="sxs-lookup"><span data-stu-id="60444-248">Port number</span></span></p></td>
<td align="left"><p><span data-ttu-id="60444-249">Gibt den logischen Port an, der von diesem Application Virtualization Server zum Überwachen von Anforderungen vom Client verwendet wird (Standard = 554).</span><span class="sxs-lookup"><span data-stu-id="60444-249">Specifies the logical port that is used by this Application Virtualization Server to listen for requests from the client (default = 554).</span></span></p>
<ul>
<li><p><span data-ttu-id="60444-250">Standard-HTTP-Server – Standard = 80.</span><span class="sxs-lookup"><span data-stu-id="60444-250">Standard HTTP server—Default = 80.</span></span></p></li>
<li><p><span data-ttu-id="60444-251">Enhanced Security http Server – Standard = 443.</span><span class="sxs-lookup"><span data-stu-id="60444-251">Enhanced Security HTTP Server—Default = 443.</span></span></p></li>
<li><p><span data-ttu-id="60444-252">Application Virtualization Server – Standard = 554.</span><span class="sxs-lookup"><span data-stu-id="60444-252">Application Virtualization Server—Default = 554.</span></span></p></li>
<li><p><span data-ttu-id="60444-253">Enhanced Security Application Virtualization Server – Standard = 322.</span><span class="sxs-lookup"><span data-stu-id="60444-253">Enhanced Security Application Virtualization Server—Default = 322.</span></span></p></li>
</ul>
<p><span data-ttu-id="60444-254">Beispiel: <strong> SWIPUBSVRPORT = &quot; 443&quot;</span><span class="sxs-lookup"><span data-stu-id="60444-254">Example: <strong>SWIPUBSVRPORT=&quot;443&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="60444-255">SWIPUBSVRPATH</span><span class="sxs-lookup"><span data-stu-id="60444-255">SWIPUBSVRPATH</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-256">Pfadname</span><span class="sxs-lookup"><span data-stu-id="60444-256">Path name</span></span></p></td>
<td align="left"><p><span data-ttu-id="60444-257">Gibt den Speicherort auf dem Veröffentlichungsserver der Datei an, in dem die Dateitypzuordnungen definiert werden (Standard =/); erforderlich, wenn der <em> SWIPUBSVRTYPE </em> -Parameterwert http ist.</span><span class="sxs-lookup"><span data-stu-id="60444-257">Specifies the location on the publishing server of the file that defines file type associations (default = /); required when the <em>SWIPUBSVRTYPE</em> parameter value is HTTP.</span></span></p>
<p><span data-ttu-id="60444-258">Beispiel: <strong> SWIPUBSVRPATH = &quot; /AppVirt/appsntypes.xml&quot;</span><span class="sxs-lookup"><span data-stu-id="60444-258">Example: <strong>SWIPUBSVRPATH=&quot;/AppVirt/appsntypes.xml&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="60444-259">SWIPUBSVRREFRESH</span><span class="sxs-lookup"><span data-stu-id="60444-259">SWIPUBSVRREFRESH</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-260">[Ein | Aus</span><span class="sxs-lookup"><span data-stu-id="60444-260">[ON|OFF]</span></span></p></td>
<td align="left"><p><span data-ttu-id="60444-261">Gibt an, ob der Client den Veröffentlichungsserver automatisch für Dateitypzuordnungen und Anwendungen abfragt, wenn sich ein Benutzer beim Client anmeldet (Standard = ein).</span><span class="sxs-lookup"><span data-stu-id="60444-261">Specifies whether the client automatically queries the publishing server for file type associations and applications when a user logs in to the client (default = ON).</span></span></p>
<p><span data-ttu-id="60444-262">Beispiel: <strong> SWIPUBSVRREFRESH = &quot; aus&quot;</span><span class="sxs-lookup"><span data-stu-id="60444-262">Example: <strong>SWIPUBSVRREFRESH=&quot;off&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="60444-263">SWIGLOBALDATA</span><span class="sxs-lookup"><span data-stu-id="60444-263">SWIGLOBALDATA</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-264">Globales Datenverzeichnis</span><span class="sxs-lookup"><span data-stu-id="60444-264">Global data directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="60444-265">Gibt das Verzeichnis an, in dem Daten gespeichert werden, die nicht für bestimmte benutzerspezifisch sind (Standard = c:\Dokumente und Einstellungen\All Users\Documents).</span><span class="sxs-lookup"><span data-stu-id="60444-265">Specifies the directory where data will be stored that is not specific to particular users (default = C:\Documents and Settings\All Users\Documents).</span></span></p>
<p><span data-ttu-id="60444-266">Beispiel: <strong> SWIGLOBALDATA = &quot; D:\Microsoft Application Virtualization Client\Global&quot;</span><span class="sxs-lookup"><span data-stu-id="60444-266">Example: <strong>SWIGLOBALDATA=&quot;D:\Microsoft Application Virtualization Client\Global&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="60444-267">SWIUSERDATA</span><span class="sxs-lookup"><span data-stu-id="60444-267">SWIUSERDATA</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-268">Benutzerdatenverzeichnis</span><span class="sxs-lookup"><span data-stu-id="60444-268">User data directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="60444-269">Gibt das Verzeichnis an, in dem Daten gespeichert werden, die für bestimmte benutzerspezifisch sind (Standard =% APPDATA%).</span><span class="sxs-lookup"><span data-stu-id="60444-269">Specifies the directory where data will be stored that is specific to particular users (default = %APPDATA%).</span></span></p>
<p><span data-ttu-id="60444-270">Beispiel: <strong> SWIUSERDATA = &quot; H:\WINDOWS\Microsoft Application Virtualization Client&quot;</span><span class="sxs-lookup"><span data-stu-id="60444-270">Example: <strong>SWIUSERDATA=&quot;H:\Windows\Microsoft Application Virtualization Client&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="60444-271">SWIFSDRIVE</span><span class="sxs-lookup"><span data-stu-id="60444-271">SWIFSDRIVE</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-272">Bevorzugter Laufwerkbuchstabe</span><span class="sxs-lookup"><span data-stu-id="60444-272">Preferred drive letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="60444-273">Entspricht dem Laufwerkbuchstaben, den Sie für das virtuelle Laufwerk ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="60444-273">Corresponds to the drive letter that you selected for the virtual drive.</span></span></p>
<p><span data-ttu-id="60444-274">Beispiel: <strong> SWIFSDRIVE = &quot; S&quot;</span><span class="sxs-lookup"><span data-stu-id="60444-274">Example: <strong>SWIFSDRIVE=&quot;S&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="60444-275">SYSTEMEVENTLOGLEVEL</span><span class="sxs-lookup"><span data-stu-id="60444-275">SYSTEMEVENTLOGLEVEL</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-276">0 – 4</span><span class="sxs-lookup"><span data-stu-id="60444-276">0–4</span></span></p></td>
<td align="left"><p><span data-ttu-id="60444-277">Gibt den Protokolliergrad an, bei dem Protokollnachrichten in das NT-Ereignisprotokoll geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="60444-277">Indicates the logging level at which log messages are written to the NT event Log.</span></span> <span data-ttu-id="60444-278">Der Wert gibt einen Schwellenwert für das protokollierte an, d. h., alles, was kleiner oder gleich dem Wert ist, wird protokolliert.</span><span class="sxs-lookup"><span data-stu-id="60444-278">The value indicates a threshold of what is logged—that is, everything equal to or less than that value is logged.</span></span> <span data-ttu-id="60444-279">Ein Wert von 0x3 (Warnung) gibt beispielsweise an, dass Warnungen (0x3), Fehler (0x2) und kritische Fehler (0x1) protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="60444-279">For example, a value of 0x3 (Warning) indicates that Warnings (0x3), Errors (0x2), and Critical Errors (0x1) are logged.</span></span></p>
<p><span data-ttu-id="60444-280">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="60444-280">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="60444-281">0 = = keine</span><span class="sxs-lookup"><span data-stu-id="60444-281">0 == None</span></span></p></li>
<li><p><span data-ttu-id="60444-282">1 = = kritisch</span><span class="sxs-lookup"><span data-stu-id="60444-282">1 == Critical</span></span></p></li>
<li><p><span data-ttu-id="60444-283">2 = = Fehler</span><span class="sxs-lookup"><span data-stu-id="60444-283">2 == Error</span></span></p></li>
<li><p><span data-ttu-id="60444-284">3 = = Warnung</span><span class="sxs-lookup"><span data-stu-id="60444-284">3 == Warning</span></span></p></li>
<li><p><span data-ttu-id="60444-285">4 = = Informationen</span><span class="sxs-lookup"><span data-stu-id="60444-285">4 == Information</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="60444-286">MINFREESPACEMB</span><span class="sxs-lookup"><span data-stu-id="60444-286">MINFREESPACEMB</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-287">In MB</span><span class="sxs-lookup"><span data-stu-id="60444-287">In MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="60444-288">Gibt die Menge des freien Speicherplatzes (in Megabyte) an, die auf dem Host verfügbar sein muss, bevor die Cachegröße zunehmen kann.</span><span class="sxs-lookup"><span data-stu-id="60444-288">Specifies the amount of free space (in megabytes) that must be available on the host before the cache size can increase.</span></span> <span data-ttu-id="60444-289">Im folgenden Beispiel wird der Client so konfiguriert, dass er mindestens 5 GB freien Speicherplatz auf dem Datenträger gewährleistet, bevor die Größe des Caches erhöht werden konnte.</span><span class="sxs-lookup"><span data-stu-id="60444-289">The following example would configure the client to ensure at least 5 GB of free space on the disk before allowing the size of the cache to increase.</span></span> <span data-ttu-id="60444-290">Der Standardwert ist 5000 MB freier Speicherplatz, der zum Zeitpunkt der Installation auf dem Datenträger zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="60444-290">The default is 5000 MB of free space available on disk at installation time.</span></span></p>
<p><span data-ttu-id="60444-291">Beispiel: <strong> MINFREESPACEMB = &quot; 5000 &quot; (5 GB)</span><span class="sxs-lookup"><span data-stu-id="60444-291">Example: <strong>MINFREESPACEMB =&quot;5000&quot; (5 GB)</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="60444-292">KEEPCURRENTSETTINGS</span><span class="sxs-lookup"><span data-stu-id="60444-292">KEEPCURRENTSETTINGS</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="60444-293">[0 | 1]</span><span class="sxs-lookup"><span data-stu-id="60444-293">[0|1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="60444-294">Wird verwendet, wenn Sie vor der Bereitstellungeines Clients Registrierungseinstellungen angewendet haben, beispielsweise mithilfe von Gruppenrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="60444-294">Used when you have applied registry settings prior to deploying a client—for example, by using Group Policy.</span></span> <span data-ttu-id="60444-295">Wenn ein Client bereitgestellt wird, setzen Sie diesen Parameter auf den Wert 1, damit die Registrierungseinstellungen nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="60444-295">When a client is deployed, set this parameter to a value of 1 so that it will not overwrite the registry settings.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="60444-296">Wichtig</span><span class="sxs-lookup"><span data-stu-id="60444-296">Important</span></span></strong><br/><p><span data-ttu-id="60444-297">Wenn auf den Wert 1 gesetzt, werden die folgenden Befehlszeilenparameter des Clientinstallationsprogramms ignoriert:</span><span class="sxs-lookup"><span data-stu-id="60444-297">If set to a value of 1, the following client installer command-line parameters are ignored:</span></span></p>
<p><strong><span data-ttu-id="60444-298">SWICACHESIZE </strong> , <strong> MINFREESPACEMB </strong> , <strong> ALLOWINDEPENDENTFILESTREAMING </strong> , <strong> ApplicationSourceRoot </strong> , <strong> IconSourceRoot </strong> , <strong> OSDSourceRoot </strong> , <strong> SYSTEMEVENTLOGLEVEL </strong> , <strong> SWIGLOBALDATA </strong> , <strong> DOTIMEOUTMINUTES </strong> , <strong> SWIFSDRIVE </strong> , <strong> AUTOLOADTARGET </strong> , <strong> AUTOLOADTRIGGERS </strong> und <strong> SWIUSERDATA </strong> .</span><span class="sxs-lookup"><span data-stu-id="60444-298">SWICACHESIZE</strong>, <strong>MINFREESPACEMB</strong>, <strong>ALLOWINDEPENDENTFILESTREAMING</strong>, <strong>APPLICATIONSOURCEROOT</strong>, <strong>ICONSOURCEROOT</strong>, <strong>OSDSOURCEROOT</strong>, <strong>SYSTEMEVENTLOGLEVEL</strong>, <strong>SWIGLOBALDATA</strong>, <strong>DOTIMEOUTMINUTES</strong>, <strong>SWIFSDRIVE</strong>, <strong>AUTOLOADTARGET</strong>, <strong>AUTOLOADTRIGGERS</strong>, and <strong>SWIUSERDATA</strong>.</span></span></p>
<p><span data-ttu-id="60444-299">Weitere Informationen zum Festlegen dieser Werte nach der Installation finden Sie unter "Konfigurieren der Einstellungen der APP-v-Client Registrierung über die Befehlszeile" im Operations Leit Faden für Application Virtualization (app-v) ( <a href="https://go.microsoft.com/fwlink/?LinkId=122939" data-raw-source="[https://go.microsoft.com/fwlink/?LinkId=122939](https://go.microsoft.com/fwlink/?LinkId=122939)"> https://go.microsoft.com/fwlink/?LinkId=122939 </a> ).</span><span class="sxs-lookup"><span data-stu-id="60444-299">For further information about setting these values after installation, see “How to Configure the App-V Client Registry Settings by Using the Command Line” in the Application Virtualization (App-V) Operations Guide (<a href="https://go.microsoft.com/fwlink/?LinkId=122939" data-raw-source="[https://go.microsoft.com/fwlink/?LinkId=122939](https://go.microsoft.com/fwlink/?LinkId=122939)">https://go.microsoft.com/fwlink/?LinkId=122939</a>).</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="60444-300">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="60444-300">Related topics</span></span>


[<span data-ttu-id="60444-301">So installieren Sie Application Virtualization Client manuell</span><span class="sxs-lookup"><span data-stu-id="60444-301">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="60444-302">So aktualisieren Sie Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="60444-302">How to Upgrade the Application Virtualization Client</span></span>](how-to-upgrade-the-application-virtualization-client.md)

[<span data-ttu-id="60444-303">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="60444-303">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)









