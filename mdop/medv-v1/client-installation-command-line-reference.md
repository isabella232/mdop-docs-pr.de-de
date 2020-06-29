---
title: Befehlszeilenreferenz für die Clientinstallation
description: Befehlszeilenreferenz für die Clientinstallation
author: dansimp
ms.assetid: 122a593d-3314-4e9b-858a-08a25ed00c32
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 708daf82699c63dfaa1f99ae595911cf6bad3737
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811929"
---
# Befehlszeilenreferenz für die Clientinstallation


**So installieren Sie MED-V über die Befehlszeile**

1.  Führen Sie in der Befehlszeile das MED-V. MSI-Paket aus, gefolgt von einem der optionalen Parameter, die in der folgenden Tabelle beschrieben sind.

2.  Das MED-V. MSI-Paket heißt *MED-V\_x.msi*, wobei *x* die Versionsnummer ist.

    Beispiel: *MED-V\_1.0.65.msi*.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parameter</th>
<th align="left">Wert</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/Quiet</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Unbeaufsichtigte Installation</p></td>
</tr>
<tr class="even">
<td align="left"><p>/log &lt; Vollständiger Pfad zur Protokolldatei&gt;</p></td>
<td align="left"><p>Der vollständige Pfad zur Protokolldatei.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>INSTALLDIR</p></td>
<td align="left"><p>Der vollständige Pfad zum Installationsverzeichnis.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>VMSFOLDER</p></td>
<td align="left"><p>Der vollständige Pfad zum Ordner "virtueller Computer".</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>INSTALL_ADMIN_TOOLS</p></td>
<td align="left"><p><strong>1.0</strong></p>
<p>Standard: <strong> 0</strong></p></td>
<td align="left"><p>Installiert MED-V-Verwaltungstools.</p></td>
</tr>
<tr class="even">
<td align="left"><p>START_AUTOMATICALLY</p></td>
<td align="left"><p><strong>1.0</strong></p>
<p>Standard: <strong> 0</strong></p></td>
<td align="left"><p>Startet den MED-V-Client automatisch jedes Mal, wenn sich der Benutzer bei Windows anmeldet.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SERVER_ADDRESS</p></td>
<td align="left"><p>Hostname oder IP</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>SERVER_PORT</p></td>
<td align="left"><p>Anschluss</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>SERVER_SSL</p></td>
<td align="left"><p><strong>1.0</strong></p>
<p>für <strong> https </strong> oder <strong> http</strong></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>START_MEDV</p></td>
<td align="left"><p><strong>1.0</strong></p>
<p>Standard: <strong> 1</strong></p></td>
<td align="left"><p>Startet Med-v nach Abschluss der Med-v-Installation.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Es wird empfohlen, START_MEDV = 0 zu setzen, falls MED-V vom System installiert wird.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>DESKTOP_SHORTCUT</p></td>
<td align="left"><p><strong>1.0</strong></p>
<p>Standard: <strong> 1</strong></p></td>
<td align="left"><p>Erstellt eine Verknüpfung auf dem Desktop, auf der der MED-V-Client gestartet wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MINIMAL_RAM_REQUIRED</p></td>
<td align="left"><p>RAM in MB</p></td>
<td align="left"><p>Überprüfen Sie bei der Installation von MED-V, ob der Computer über die Mindestgröße des angegebenen Arbeitsspeichers verfügt. Wenn dies nicht der Fall ist, wird die Installation abgebrochen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SKIP_OS_CHECK</p></td>
<td align="left"><p><strong>1.0</strong></p></td>
<td align="left"><p>Unterdrückt die Validierung des Betriebssystems.</p></td>
</tr>
</tbody>
</table>











