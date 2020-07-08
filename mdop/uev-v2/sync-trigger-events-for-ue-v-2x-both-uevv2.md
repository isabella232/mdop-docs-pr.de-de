---
title: Synchronisieren von Triggerereignissen für UE-V 2.x
description: Synchronisieren von Triggerereignissen für UE-V 2.x
author: dansimp
ms.assetid: 4ed71a13-6a4f-4376-996f-74b126536bbc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f3e89a0370790e7f462b2f469792128dba033460
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811971"
---
# Synchronisieren von Triggerereignissen für UE-V 2.x


Mit Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 und 2,1 SP1 können Sie Ihre Anwendungs-und Windows-Einstellungen auf allen Ihren Domänen verbundenen Geräten synchronisieren. *Synchronisierungstrigger-Ereignisse* definieren, wann der UE-V-Agent diese Einstellungen mit dem Speicherort der Einstellungen synchronisiert. UE-V 2 führt eine neue *Synchronisierungsmethode* mit dem Namen " *SyncProvider*" ein. Weitere Informationen zur Konfiguration der Synchronisierungsmethoden finden Sie unter [Synchronisierungsmethoden für UE-V 2. x](sync-methods-for-ue-v-2x-both-uevv2.md).

## UE-V 2-Synchronisierungs Trigger-Ereignisse


In der folgenden Tabelle werden die Trigger-Ereignisse für klassische Anwendungen und Windows-Einstellungen erläutert.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>UE-V 2-Trigger-Ereignis</strong></p></td>
<td align="left"><p><strong>SyncMethod = SyncProvider</strong></p></td>
<td align="left"><p><strong>SyncMethod = keine</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Windows-Anmeldung</strong></p></td>
<td align="left"><ul>
<li><p>Anwendungs-und Windows-Einstellungen werden aus dem Speicherort für Einstellungen in den lokalen Cache importiert.</p></li>
<li><p><a href="https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2" data-raw-source="[Asynchronous Windows settings](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2)">Asynchrone Windows </a> -Einstellungen werden angewendet.</p></li>
<li><p>Synchrone Windows-Einstellungen werden während der nächsten Windows-Anmeldung übernommen.</p></li>
<li><p>Anwendungseinstellungen werden angewendet, wenn die Anwendung gestartet wird.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Anwendungs-und Windows-Einstellungen werden direkt vom Speicherort der Einstellungen gelesen.</p></li>
<li><p>Asynchrone und synchrone Windows-Einstellungen werden angewendet.</p></li>
<li><p>Anwendungseinstellungen werden angewendet, wenn die Anwendung gestartet wird.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Windows-Abmeldung</strong></p></td>
<td align="left"><p>Lokale Änderungen lokal speichern und asynchrone und synchrone Windows-Einstellungen auf den Einstellungen-Speicherort Server kopieren, falls verfügbar</p></td>
<td align="left"><p>Speichern von Änderungen an einem asynchronen und synchronen Windows-Einstellungs Speicherort</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Windows Connect (RDP)/entsperren</strong></p></td>
<td align="left"><p>Synchronisieren Sie alle asynchronen Windows-Einstellungen vom Speicherort der Einstellungen zum lokalen Cache, sofern verfügbar.</p>
<p>Anwenden von zwischengespeicherten Windows-Einstellungen</p></td>
<td align="left"><p>Herunterladen und Anwenden von asynchronen Windows-Einstellungen vom Speicherort des Einstellungs Speichers</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Windows-Trennung (RDP)/Sperre</strong></p></td>
<td align="left"><p>Speichern Sie die Änderungen an den asynchronen Windows-Einstellungen im lokalen Cache.</p>
<p>Synchronisieren Sie alle asynchronen Windows-Einstellungen aus dem lokalen Cache mit dem Speicherort der Einstellungen, falls verfügbar</p></td>
<td align="left"><p>Speichern von Änderungen an den asynchronen Windows-Einstellungen am Speicherort der Einstellungen</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Anwendungsstart</strong></p></td>
<td align="left"><p>Anwenden von Anwendungseinstellungen aus dem lokalen Cache beim Starten der Anwendung</p></td>
<td align="left"><p>Anwenden von Anwendungseinstellungen vom Speicherort der Einstellungen beim Starten der Anwendung</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Anwendung wird geschlossen</strong></p></td>
<td align="left"><p>Speichern von Änderungen an den Anwendungseinstellungen im lokalen Cache und Kopieren von Einstellungen in den Speicherort der Einstellungen, sofern verfügbar</p></td>
<td align="left"><p>Speichern der Änderungen an den Einstellungen des Einstellungsspeicher Orts</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Der geplante Synchronisierungs Controller-Task oder "Jetzt synchronisieren" wird über das Unternehmenseinstellungen-Center ausgeführt.</strong></p>
<p></p></td>
<td align="left"><p>Anwendungs-und Windows-Einstellungen werden zwischen dem Speicherort der Einstellungen und dem lokalen Cache synchronisiert.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Änderungen an Einstellungen werden erst lokal zwischengespeichert, nachdem eine Anwendung geschlossen wurde. Dieser Trigger exportiert keine Änderungen, die an einer aktuell ausgeführten Anwendung vorgenommen wurden.</p>
<p>Für Windows-Einstellungen bedeutet dies, dass alle Änderungen nicht lokal zwischengespeichert und bis zur nächsten Sperre (asynchron) oder Abmeldung (asynchron und synchron) exportiert werden.</p>
</div>
<div>

</div>
<p>In diesen Fällen werden Einstellungen angewendet:</p>
<ul>
<li><p>Asynchrone Windows-Einstellungen werden direkt angewendet.</p></li>
<li><p>Anwendungseinstellungen werden angewendet, wenn die Anwendung gestartet wird.</p></li>
<li><p>Während der nächsten Windows-Anmeldung werden sowohl asynchrone als auch synchrone Windows-Einstellungen angewendet.</p></li>
<li><p>Bei der nächsten Aktualisierung werden die Windows-App-Einstellungen (AppX) angewendet. Weitere Informationen finden Sie unter <a href="https://technet.microsoft.com/library/dn458944.aspx" data-raw-source="[Monitor Application Settings](https://technet.microsoft.com/library/dn458944.aspx)"> Überwachen von Anwendungseinstellungen </a> .</p></li>
</ul></td>
<td align="left"><p>Nicht verfügbar</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Asynchrone Einstellungen, die im Remotespeicher aktualisiert wurden *</strong></p></td>
<td align="left"><p>Laden und Anwenden neuer asynchroner Einstellungen aus dem Cache.</p></td>
<td align="left"><p>Laden und Anwenden von Einstellungen vom zentralen Server</p></td>
</tr>
</tbody>
</table>








## Verwandte Themen


[Technische Referenz für UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

[Ändern der Häufigkeit von geplanten Aufgaben in UE-V 2. x](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

[Wählen Sie die Konfigurationsmethode für UE-V 2. x aus.](https://technet.microsoft.com/library/dn458891.aspx#config)









