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
# Befehlszeilenparameter von Application Virtualization Client Installer


In der folgenden Tabelle sind alle verfügbaren Befehlszeilenparameter für Microsoft Application Virtualization Client Installer, deren Werte und eine kurze Beschreibung der einzelnen Parameter aufgeführt. Bei Parametern wird die Groß-/Kleinschreibung beachtet und muss als Großbuchstaben eingegeben werden. Alle Parameterwerte müssen in doppelten Anführungszeichen eingeschlossen werden.

**Hinweis:**  
-   Für App-V, Version 4,6, können Befehlszeilenparameter während eines Clientupgrades nicht verwendet werden.

-   Die Parameter *SWICACHESIZE* und *MINFREESPACEMB* können nicht in der Befehlszeile kombiniert werden. Wenn beide verwendet werden, wird der *SWICACHESIZE* -Parameter ignoriert.



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parameter</th>
<th align="left">Werte</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em>ALLOWINDEPENDENTFILESTREAMING</em></p></td>
<td align="left"><p>TRUE</p>
<p>FALSE</p></td>
<td align="left"><p>Gibt an, ob das Streaming aus einer Datei unabhängig davon aktiviert wird, wie der Client mit dem <em> ApplicationSourceRoot </em> -Parameter konfiguriert wurde. Ist dieser Wert auf "false" festgelegt, wird durch den Transport kein Streaming aus Dateien möglich, auch wenn der OSD-HREF-oder der <em> ApplicationSourceRoot- </em> Parameter einen Dateipfad enthält.</p>
<p>Mögliche Werte:</p>
<ul>
<li><p>TRUE – die manuell bereitgestellte Anwendung wird möglicherweise vom Datenträger geladen.</p></li>
<li><p>Falsch: alle Anwendungen müssen vom Quell Streamingserver stammen.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em>ApplicationSourceRoot</em></p></td>
<td align="left"><p>RTSP:// <em> </em> -URL (für dynamische Paketzustellung)</p>
<p>File:// <em> URL </em> oder <em> UNC </em> (für das Laden aus der Dateipaket Zustellung)</p></td>
<td align="left"><p>Um einem Administrator oder einem elektronischen Softwareverteilungssystem zu ermöglichen, sicherzustellen, dass das Laden der Anwendung in Übereinstimmung mit dem Topologieverwaltung-Schema durchgeführt wird, ist es möglich, die OSD-CodeBase für das Application href-Element (den Quellspeicherort) zu überschreiben. Wenn der Wert "" ist, der Standardwert ist, werden die vorhandenen OSD-Datei Einstellungen verwendet.</p>
<p>Eine URL besteht aus mehreren Teilen:</p>
<p>&lt;Protokoll &gt; :// &lt; Server &gt; : &lt; Port &gt; / &lt; Pfad &gt; / &lt; ? Abfrage &gt; &lt; #Fragment&gt;</p>
<p>Ein UNC-Pfad besteht aus drei Teilen:</p>
<p>&amp;lt; Computername &gt; &amp; lt; Freigabeordner &gt; &amp; lt; Ressource&gt;</p>
<p>Wenn der <em> ApplicationSourceRoot </em> -Parameter auf einem Client angegeben wird, unterbricht der Client die URL oder den UNC-Pfad aus einer OSD-Datei in seine Bestandteile und ersetzt die OSD-Abschnitte durch die entsprechenden <em> ApplicationSourceRoot- </em> Abschnitte.</p>
<div class="alert">
<strong>Wichtig</strong><br/><p>Achten Sie darauf, das richtige Format zu verwenden, wenn Sie file://mit einem UNC-Pfad verwenden. Das richtige Format ist file:// &amp; lt; Server &gt; &amp; lt; freigeben &gt; .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em>IconSourceRoot</em></p></td>
<td align="left"><p><em>UNC</em></p>
<p>HTTP:// <em> URL- </em> oder https://- <em> URL</em></p></td>
<td align="left"><p>Ermöglicht einem Administrator die Angabe eines Quellspeicherorts für den Symbol Abruf eines sequenzierten Anwendungspakets während der Veröffentlichung. Symbol Quellen Stämme unterstützen UNC-Pfade und-URLs (http oder HTTPS). Wenn der Wert "" ist, der Standardwert ist, werden die vorhandenen OSD-Datei Einstellungen verwendet.</p>
<p>Eine URL besteht aus mehreren Teilen:</p>
<p>&lt;Protokoll &gt; :// &lt; Server &gt; : &lt; Port &gt; / &lt; Pfad &gt; / &lt; ? Abfrage &gt; &lt; #Fragment&gt;</p>
<p>Ein UNC-Pfad besteht aus drei Teilen:</p>
<p>&amp;lt; Computername &gt; &amp; lt; Freigabeordner &gt; &amp; lt; Ressource&gt;</p>
<div class="alert">
<strong>Wichtig</strong><br/><p>Achten Sie beim Verwenden eines UNC-Pfads darauf, das richtige Format zu verwenden. Zulässige Formate sind &amp; lt; Server &gt; &amp; lt; Freigabe &gt; &lt; -oder Laufwerkbuchstabe &gt; : &amp; lt; Folder &gt; .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em>OSDSourceRoot</em></p></td>
<td align="left"><p><em>UNC</em></p>
<p>HTTP:// <em> URL- </em> oder https://- <em> URL</em></p></td>
<td align="left"><p>Ermöglicht einem Administrator die Angabe eines Quellspeicherorts für den Abruf von OSD-Dateien für ein Anwendungspaket während der Veröffentlichung. OSD-Quell Stämme unterstützen UNC-Pfade und-URLs (http oder HTTPS). Wenn der Wert "" ist, der Standardwert ist, werden die vorhandenen OSD-Datei Einstellungen verwendet.</p>
<p>Eine URL besteht aus mehreren Teilen:</p>
<p>&lt;Protokoll &gt; :// &lt; Server &gt; : &lt; Port &gt; / &lt; Pfad &gt; / &lt; ? Abfrage &gt; &lt; #Fragment&gt;</p>
<p>Ein UNC-Pfad besteht aus drei Teilen:</p>
<p>&amp;lt; Computername &gt; &amp; lt; Freigabeordner &gt; &amp; lt; Ressource&gt;</p>
<div class="alert">
<strong>Wichtig</strong><br/><p>Achten Sie beim Verwenden eines UNC-Pfads darauf, das richtige Format zu verwenden. Zulässige Formate sind &amp; lt; Server &gt; &amp; lt; Freigabe &gt; &lt; -oder Laufwerkbuchstabe &gt; : &amp; lt; Folder &gt; .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em>AUTOLOADONLOGIN</em></p>
<p><em>AUTOLOADONLAUNCH</em></p>
<p><em>AUTOLOADONREFRESH</em></p></td>
<td align="left"><p>[0 | 1]</p></td>
<td align="left"><p>Die Trigger zum automatischen Laden definieren die Ereignisse, die das automatische Laden von Anwendungen initiieren. Beim Laden wird implizit Hintergrund Streaming verwendet, damit die Anwendung vollständig in den Cache geladen werden kann.</p>
<p>Der primäre Feature-Block wird so schnell wie möglich geladen. Verbleibende Funktionsbausteine werden in den Hintergrund geladen, um Vordergrund Vorgänge wie Benutzerinteraktionen mit Anwendungen zu ermöglichen, um Vorrang zu haben und eine optimale Leistung zu gewährleisten.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Der <em> AUTOLOADTARGET </em> -Parameter bestimmt, welche Anwendungen automatisch geladen werden. Standardmäßig werden Pakete, die verwendet wurden, automatisch geladen, es sei denn, <em> AUTOLOADTARGET </em> ist festzulegen.</p>
</div>
<div>

</div>
<p>Jeder Parameter wirkt sich auf das Ladeverhalten wie folgt aus:</p>
<ul>
<li><p><em>AUTOLOADONLOGIN </em> – das Laden beginnt, wenn sich der Benutzer anmeldet.</p></li>
<li><p><em>AUTOLOADONLAUNCH </em> – das Laden beginnt, wenn der Benutzer eine Anwendung startet.</p></li>
<li><p><em>AUTOLOADONREFRESH </em> – das Laden beginnt, wenn eine Veröffentlichungsaktualisierung stattfindet.</p></li>
</ul>
<p>Die drei Werte können kombiniert werden. Im folgenden Beispiel werden die Trigger für das Laden sowohl bei der Benutzeranmeldung als auch bei der Veröffentlichungsaktualisierung aktiviert:</p>
<p><em>AUTOLOADONLOGIN AUTOLOADONREFRESH</em></p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn der Client bei der ersten Installation mit diesen Werten konfiguriert ist, wird das Programm automatisch erst ausgelöst, wenn sich der Benutzer das nächste Mal anmeldet und sich wieder anmeldet.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em>AUTOLOADTARGET</em></p></td>
<td align="left"><p>Keine</p>
<p>Alle</p>
<p>PREVUSED</p></td>
<td align="left"><p>Gibt an, was automatisch geladen wird, wenn ein bestimmter Trigger für das automatische Laden eintritt.</p>
<p>Mögliche Werte:</p>
<ul>
<li><p>Keine – kein automatisches Laden, unabhängig davon, welche Trigger festzulegen sind.</p></li>
<li><p>Alle – wenn ein automatischer Trigger aktiviert ist, werden alle Pakete automatisch geladen, unabhängig davon, ob Sie jemals gestartet wurden.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Diese Einstellung ist für einzelne Pakete mithilfe der <strong> Befehle SFTMIME hinzufügen </strong> und <strong> Paket konfigurieren konfiguriert </strong> . Weitere Informationen zu diesen Befehlen finden Sie unter <a href="sftmime--command-reference.md" data-raw-source="[SFTMIME Command Reference](sftmime--command-reference.md)"> Befehlsreferenz für SFTMIME </a> .</p>
</div>
<div>

</div></li>
<li><p>PREVUSED – wenn ein automatischer Trigger aktiviert ist, laden Sie nur die Pakete, bei denen mindestens eine Anwendung im Paket zuvor verwendet wurde (also gestartet oder vorab gespeichert wurde).</p></li>
</ul>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn Sie den App-V-Client installieren, um einen schreibgeschützten Cache zu verwenden (beispielsweise als VDI-Server Implementierung), müssen Sie den AUTOLOADTARGET-Parameter auf None setzen, um zu verhindern, dass <em> </em> der Client versucht, Anwendungen im schreibgeschützten Cache zu aktualisieren.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em>DOTIMEOUTMINUTES</em></p></td>
<td align="left"><p>29600 (Standard)</p>
<p>1 – 1439998560 Minuten (Bereich)</p></td>
<td align="left"><p>Gibt an, wie viele Minuten eine Anwendung im getrennten Betrieb verwendet werden kann.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>INSTALLDIR</em></p></td>
<td align="left"><p>&lt;Pfadname&gt;</p></td>
<td align="left"><p>Gibt das Installationsverzeichnis des App-V-Clients an.</p>
<p>Beispiel: INSTALLDIR = &quot; c:\Programme\Microsoft Application Virtualization Client&quot;</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>OPTIN</em></p></td>
<td align="left"><p>TRUE</p>
<p>“”</p></td>
<td align="left"><p>Microsoft Application Virtualization-Client Komponenten werden durch Microsoft Update aktualisiert, wenn Updates für die allgemeine Öffentlichkeit zur Verfügung gestellt werden. Der auf Windows-Betriebssystemen installierte Microsoft Update-Agent setzt voraus, dass ein Benutzer sich ausdrücklich für die Nutzung des Diensts entscheidet. Dieser Opt-in ist nur einmal für alle Anwendungen auf dem Gerät erforderlich. Wenn Sie sich bereits für Microsoft Update entschieden haben, nutzen die Microsoft Application Virtualization-Komponenten auf dem Gerät automatisch die Vorteile des Diensts.</p>
<p>Bei der Befehlszeileninstallation ist die Verwendung von Microsoft Update standardmäßig deaktiviert (es sei denn, eine vorherige Anwendung hat bereits die Aktivierung des Geräts ermöglicht), da Sie die manuelle Entscheidung für Microsoft Update erforderlich machen. Daher muss die Entscheidung für Befehlszeileninstallationen explizit sein. Wenn der Befehlszeilenparameter <em> optin </em> auf true festgelegt wird, muss die Microsoft Update-Option festgelegt werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>RequireAuthorizationIfCached</em></p></td>
<td align="left"><p>TRUE</p>
<p>FALSE</p></td>
<td align="left"><p>Gibt an, ob immer eine Autorisierung erforderlich ist, unabhängig davon, ob sich eine Anwendung bereits im Cache befindet.</p>
<p>Mögliche Werte:</p>
<ul>
<li><p>TRUE – die Anwendung muss beim Start immer autorisiert werden. Für RTSP-Streaming-Anwendungen wird das Benutzerautorisierungstoken zur Autorisierung an den Server gesendet. Bei dateibasierten Anwendungen diktieren Datei-ACLs, ob ein Benutzer auf die Anwendung zugreifen kann.</p></li>
<li><p>FALSE: versuchen Sie immer, eine Verbindung mit dem Server herzustellen. Wenn keine Verbindung mit dem Server hergestellt werden kann, ermöglicht der Client dem Benutzer weiterhin, eine Anwendung zu starten, die zuvor in den Cache geladen wurde.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWICACHESIZE</em></p></td>
<td align="left"><p>Cache Größe in MB</p></td>
<td align="left"><p>Gibt die Größe des Clientcaches in Megabyte an. Die Standardgröße ist 4096 MB, und die maximale Größe beträgt 1.048.576 MB (1 TB). Das System überprüft den verfügbaren Speicherplatz zur Installationszeit, aber der Platz ist nicht reserviert.</p>
<p>Beispiel: <strong> SWICACHESIZE = &quot; 1024&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIPUBSVRDISPLAY</em></p></td>
<td align="left"><p>Anzeigename</p></td>
<td align="left"><p>Gibt den angezeigten Namen des Veröffentlichungsservers an; erforderlich <em> , wenn SWIPUBSVRHOST </em> verwendet wird.</p>
<p>Beispiel: <strong> SWIPUBSVRDISPLAY = &quot; Produktionsumgebung&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIPUBSVRTYPE</em></p></td>
<td align="left"><p>[Http | RTSP</p></td>
<td align="left"><p>Gibt den Typ des Veröffentlichungsservers an. Der Standard Servertyp ist Application Virtualization Server. <strong>Bei der/Secure </strong> -Option wird die Groß-/Kleinschreibung nicht berücksichtigt.</p>
<ul>
<li><p>Http – Standard-HTTP-Server</p></li>
<li><p>Http <strong> </strong> -/Secure – Enhanced Security http Server</p></li>
<li><p>RTSP – Application Virtualization Server</p></li>
<li><p>RTSP <strong> /Secure </strong> – Enhanced Security Application Virtualization Server</p></li>
</ul>
<p>Beispiel: <strong> SWIPUBSVRTYPE = &quot; http-/Secure&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIPUBSVRHOST</em></p></td>
<td align="left"><p>IP-Adresse | hostname</p></td>
<td align="left"><p>Gibt entweder die IP-Adresse des Application Virtualization Server oder einen Hostnamen des Servers an, der in die IP-Adresse des Servers&#39;s aufgelöst wird; erforderlich <em> , wenn SWIPUBSVRDISPLAY </em> verwendet wird.</p>
<p>Beispiel: <strong> SWIPUBSVRHOST = &quot; Server01&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIPUBSVRPORT</em></p></td>
<td align="left"><p>Port Nummer</p></td>
<td align="left"><p>Gibt den logischen Port an, der von diesem Application Virtualization Server zum Überwachen von Anforderungen vom Client verwendet wird (Standard = 554).</p>
<ul>
<li><p>Standard-HTTP-Server – Standard = 80.</p></li>
<li><p>Enhanced Security http Server – Standard = 443.</p></li>
<li><p>Application Virtualization Server – Standard = 554.</p></li>
<li><p>Enhanced Security Application Virtualization Server – Standard = 322.</p></li>
</ul>
<p>Beispiel: <strong> SWIPUBSVRPORT = &quot; 443&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIPUBSVRPATH</em></p></td>
<td align="left"><p>Pfadname</p></td>
<td align="left"><p>Gibt den Speicherort auf dem Veröffentlichungsserver der Datei an, in dem die Dateitypzuordnungen definiert werden (Standard =/); erforderlich, wenn der <em> SWIPUBSVRTYPE </em> -Parameterwert http ist.</p>
<p>Beispiel: <strong> SWIPUBSVRPATH = &quot; /AppVirt/appsntypes.xml&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIPUBSVRREFRESH</em></p></td>
<td align="left"><p>[Ein | Aus</p></td>
<td align="left"><p>Gibt an, ob der Client den Veröffentlichungsserver automatisch für Dateitypzuordnungen und Anwendungen abfragt, wenn sich ein Benutzer beim Client anmeldet (Standard = ein).</p>
<p>Beispiel: <strong> SWIPUBSVRREFRESH = &quot; aus&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIGLOBALDATA</em></p></td>
<td align="left"><p>Globales Datenverzeichnis</p></td>
<td align="left"><p>Gibt das Verzeichnis an, in dem Daten gespeichert werden, die nicht für bestimmte benutzerspezifisch sind (Standard = c:\Dokumente und Einstellungen\All Users\Documents).</p>
<p>Beispiel: <strong> SWIGLOBALDATA = &quot; D:\Microsoft Application Virtualization Client\Global&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIUSERDATA</em></p></td>
<td align="left"><p>Benutzerdatenverzeichnis</p></td>
<td align="left"><p>Gibt das Verzeichnis an, in dem Daten gespeichert werden, die für bestimmte benutzerspezifisch sind (Standard =% APPDATA%).</p>
<p>Beispiel: <strong> SWIUSERDATA = &quot; H:\WINDOWS\Microsoft Application Virtualization Client&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIFSDRIVE</em></p></td>
<td align="left"><p>Bevorzugter Laufwerkbuchstabe</p></td>
<td align="left"><p>Entspricht dem Laufwerkbuchstaben, den Sie für das virtuelle Laufwerk ausgewählt haben.</p>
<p>Beispiel: <strong> SWIFSDRIVE = &quot; S&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SYSTEMEVENTLOGLEVEL</em></p></td>
<td align="left"><p>0 – 4</p></td>
<td align="left"><p>Gibt den Protokolliergrad an, bei dem Protokollnachrichten in das NT-Ereignisprotokoll geschrieben werden. Der Wert gibt einen Schwellenwert für das protokollierte an, d. h., alles, was kleiner oder gleich dem Wert ist, wird protokolliert. Ein Wert von 0x3 (Warnung) gibt beispielsweise an, dass Warnungen (0x3), Fehler (0x2) und kritische Fehler (0x1) protokolliert werden.</p>
<p>Mögliche Werte:</p>
<ul>
<li><p>0 = = keine</p></li>
<li><p>1 = = kritisch</p></li>
<li><p>2 = = Fehler</p></li>
<li><p>3 = = Warnung</p></li>
<li><p>4 = = Informationen</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em>MINFREESPACEMB</em></p></td>
<td align="left"><p>In MB</p></td>
<td align="left"><p>Gibt die Menge des freien Speicherplatzes (in Megabyte) an, die auf dem Host verfügbar sein muss, bevor die Cachegröße zunehmen kann. Im folgenden Beispiel wird der Client so konfiguriert, dass er mindestens 5 GB freien Speicherplatz auf dem Datenträger gewährleistet, bevor die Größe des Caches erhöht werden konnte. Der Standardwert ist 5000 MB freier Speicherplatz, der zum Zeitpunkt der Installation auf dem Datenträger zur Verfügung steht.</p>
<p>Beispiel: <strong> MINFREESPACEMB = &quot; 5000 &quot; (5 GB)</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>KEEPCURRENTSETTINGS</em></p></td>
<td align="left"><p>[0 | 1]</p></td>
<td align="left"><p>Wird verwendet, wenn Sie vor der Bereitstellungeines Clients Registrierungseinstellungen angewendet haben, beispielsweise mithilfe von Gruppenrichtlinien. Wenn ein Client bereitgestellt wird, setzen Sie diesen Parameter auf den Wert 1, damit die Registrierungseinstellungen nicht überschrieben werden.</p>
<div class="alert">
<strong>Wichtig</strong><br/><p>Wenn auf den Wert 1 gesetzt, werden die folgenden Befehlszeilenparameter des Clientinstallationsprogramms ignoriert:</p>
<p><strong>SWICACHESIZE </strong> , <strong> MINFREESPACEMB </strong> , <strong> ALLOWINDEPENDENTFILESTREAMING </strong> , <strong> ApplicationSourceRoot </strong> , <strong> IconSourceRoot </strong> , <strong> OSDSourceRoot </strong> , <strong> SYSTEMEVENTLOGLEVEL </strong> , <strong> SWIGLOBALDATA </strong> , <strong> DOTIMEOUTMINUTES </strong> , <strong> SWIFSDRIVE </strong> , <strong> AUTOLOADTARGET </strong> , <strong> AUTOLOADTRIGGERS </strong> und <strong> SWIUSERDATA </strong> .</p>
<p>Weitere Informationen zum Festlegen dieser Werte nach der Installation finden Sie unter "Konfigurieren der Einstellungen der APP-v-Client Registrierung über die Befehlszeile" im Operations Leit Faden für Application Virtualization (app-v) ( <a href="https://go.microsoft.com/fwlink/?LinkId=122939" data-raw-source="[https://go.microsoft.com/fwlink/?LinkId=122939](https://go.microsoft.com/fwlink/?LinkId=122939)"> https://go.microsoft.com/fwlink/?LinkId=122939 </a> ).</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Verwandte Themen


[So installieren Sie Application Virtualization Client manuell](how-to-manually-install-the-application-virtualization-client.md)

[So aktualisieren Sie Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)

[SFTMIME-Befehlsreferenz](sftmime--command-reference.md)









