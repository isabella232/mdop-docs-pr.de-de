---
title: Planen der Verwendung der Ordnerumleitung mit App-V
description: Planen der Verwendung der Ordnerumleitung mit App-V
author: dansimp
ms.assetid: 6bea9a8f-a915-4d7d-be67-ef1cca1398ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 507aef186579da0efdb3af7b6e1088a5e725ad70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804937"
---
# Planen der Verwendung der Ordnerumleitung mit App-V


Microsoft Application Virtualization (App-V) 5,1 unterstützt die Verwendung der Ordnerumleitung, ein Feature, mit dem Benutzer und Administratoren den Pfad eines Ordners an einen neuen Speicherort umleiten können.

Dieses Thema enthält die folgenden Abschnitte:

-   [Voraussetzungen für die Verwendung der Ordnerumleitung](#bkmk-folder-redir-reqs)

-   [Konfigurieren der Ordnerumleitung zur Verwendung mit App-V](#bkmk-folder-redir-cfg)

-   [Funktionsweise der Ordnerumleitung mit App-V](#bkmk-folder-redir-works)

-   [Übersicht über die Ordnerumleitung](#bkmk-folder-redir-overview)

## <a href="" id="bkmk-folder-redir-reqs"></a>Anforderungen und nicht unterstützte Szenarien für die Verwendung der Ordnerumleitung


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Anforderungen</p></td>
<td align="left"><p>Um die Ordnerumleitung von% APPDATA% zu verwenden, müssen Sie Folgendes ausführen:</p>
<ul>
<li><p>Verfügen Sie über ein App-V-Paket mit einem VFS-Ordner (APPDATA Virtual File System).</p></li>
<li><p>Aktivieren Sie die Ordnerumleitung, und leiten Sie die Ordner der Benutzer in einen freigegebenen Ordner um, in der Regel in einem Netzwerkordner.</p></li>
<li><p>Roamen Sie beide oder keine der folgenden Optionen:</p>
<ul>
<li><p>Dateien unter%APPDATA%\Microsoft\AppV\Client\Catalog</p></li>
<li><p>Registrierungseinstellungen unter HKEY_CURRENT_USER \software\microsoft\appv\client\packages</p>
<p>Weitere Informationen finden Sie unter <a href="application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs" data-raw-source="[Application Publishing and Client Interaction](application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs)"> Anwendungsveröffentlichung und Client Interaktion </a> .</p></li>
</ul></li>
<li><p>Stellen Sie sicher, dass die folgenden Ordner für jeden Benutzer verfügbar sind, der sich bei dem Computer anmeldet, auf dem der Client App-V 5,0 SP2 oder höher ausgeführt wird:</p>
<ul>
<li><p>% APPDATA% ist für den gewünschten Netzwerkspeicherort konfiguriert (mit oder ohne <a href="https://technet.microsoft.com/library/cc780552.aspx" data-raw-source="[Offline Files](https://technet.microsoft.com/library/cc780552.aspx)"> Unterstützung für Offline Dateien </a> ).</p></li>
<li><p>% LocalAppData% ist für den gewünschten lokalen Ordner konfiguriert.</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Nicht unterstützte Szenarien</p></td>
<td align="left"><ul>
<li><p>Konfigurieren von% LocalAppData% als Netzlaufwerk.</p></li>
<li><p>Umleiten des Start Menüs an einen einzelnen Ordner für mehrere Benutzer</p></li>
<li><p>Wenn Roaming-APPDATA (% APPDATA%) an eine nicht verfügbare Netzwerkfreigabe umgeleitet wird, können App-V-Anwendungen wie folgt nicht gestartet werden:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">App-V-Version</th>
<th align="left">Beschreibung des Szenarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>In App-v 5,0 über APP-v 5,0 SP2 Plus Hotfixes</p></td>
<td align="left"><p>Dieser Fehler tritt unabhängig davon auf, ob Offline Dateien aktiviert sind.</p></td>
</tr>
<tr class="even">
<td align="left"><p>In App-V 5,0 SP3 und höher</p></td>
<td align="left"><p>Wenn die nicht verfügbare Netzwerkfreigabe für Offline Dateien aktiviert wurde, wird die App-V-Anwendung erfolgreich gestartet.</p></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-cfg"></a>Konfigurieren der Ordnerumleitung zur Verwendung mit App-V


Die Ordnerumleitung kann auf verschiedene Ordner wie Desktop, eigene Dateien, meine Bilder usw. angewendet werden. Der einzige Ordner, der sich auf die Verwendung von App-V-Anwendungen auswirkt, ist jedoch der Roaming-AppData-Ordner des Benutzers (% APPDATA%). Sie können die Ordnerumleitung auf alle anderen unterstützten Ordner anwenden, ohne Auswirkungen auf App-V zu haben.

## <a href="" id="bkmk-folder-redir-works"></a>Funktionsweise der Ordnerumleitung mit App-V


In der folgenden Tabelle wird beschrieben, wie die Ordnerumleitung funktioniert, wenn% APPDATA% an ein Netzwerk umgeleitet wird und wenn Sie die oben in diesem Artikel aufgelisteten Anforderungen erfüllt haben.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Zustand der virtuellen Umgebung</th>
<th align="left">Aktion, die Eintritt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Wenn die virtuelle Umgebung gestartet wird</p></td>
<td align="left"><p>Der AppData-Ordner des virtuellen Dateisystems (VFS) wird dem lokalen AppData-Ordner (% LocalAppData%) zugeordnet. anstelle des Roaming-APPDATA-Ordners (% APPDATA%) des Benutzers.</p>
<ul>
<li><p>LocalAppData enthält einen lokalen Cache des Roaming-APPDATA-Ordners des Benutzers für das verwendete Paket. Der lokale Cache befindet sich unter:</p>
<p><code>%LocalAppData%\Microsoft\AppV\Client\VFS\PackageGUID\AppData</code></p></li>
<li><p>Die neuesten Daten aus dem Roaming-AppData-Ordner des Benutzers werden in die Daten kopiert und ersetzt, die sich derzeit im lokalen Cache befinden.</p></li>
<li><p>Während die virtuelle Umgebung ausgeführt wird, werden die Daten weiterhin im lokalen Cache gespeichert. Daten werden nur von% LocalAppData% bereitgestellt und nicht verschoben oder mit% APPDATA% synchronisiert, bis der Endbenutzer den Computer herunterfährt.</p></li>
<li><p>Einträge im AppData-Ordner werden über den Benutzerkontext und nicht über den Systemkontext erstellt.</p></li>
</ul>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Bei der Umleitung des App-V-Client Ordners können Dateien manchmal nicht von% APPDATA% auf% LocalAppData% verschoben werden. Weitere Informationen finden Sie unter <a href="release-notes-for-app-v-50-sp2.md#bkmk-folderredirection" data-raw-source="[Release Notes for App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md#bkmk-folderredirection)"> Versionshinweise für App-V 5,0 SP2 </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Wenn die virtuelle Umgebung heruntergefahren wird</p></td>
<td align="left"><p>Die lokalen zwischengespeicherten Daten in APPDATA (Roaming) werden gezippt und in% APPDATA% in den Ordner "echte" Roaming-APPDATA kopiert. Ein Zeitstempel, der den letzten bekannten Upload angibt, wird gleichzeitig als Registrierungsschlüssel unter gespeichert:</p>
<p><code>HKCU\Software\Microsoft\AppV\Client\Packages&amp;lt;PACKAGE_GUID&gt;\AppDataTime</code></p>
<p>Zur Bereitstellung von Redundanz speichert App-V die drei letzten Kopien der komprimierten Daten unter% APPDATA%.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-overview"></a>Übersicht über die Ordnerumleitung


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Zweck</p></td>
<td align="left"><p>Ermöglicht es Endbenutzern, mit Dateien zu arbeiten, die in einen anderen Ordner umgeleitet wurden, als ob die Dateien noch auf dem lokalen Laufwerk vorhanden waren.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Beschreibung</p></td>
<td align="left"><p>Mit der Ordnerumleitung können Benutzer und Administratoren den Pfad eines Ordners an einen Netzwerkspeicherort umleiten. Die Dokumente im Ordner stehen dem Benutzer auf jedem Computer im Netzwerk zur Verfügung.</p>
<ul>
<li><p>Mit der Ordnerumleitung können Benutzer und Administratoren den Pfad eines Ordners an einen Netzwerkspeicherort umleiten. Die Dokumente im Ordner stehen dem Benutzer auf jedem Computer im Netzwerk zur Verfügung.</p></li>
<li><p>Der neue Speicherort kann ein Ordner auf dem lokalen Computer oder ein Ordner in einem freigegebenen Netzwerk sein.</p></li>
<li><p>Durch die Ordnerumleitung werden die Dateien sofort aktualisiert, während Roamingdaten in der Regel synchronisiert werden, wenn sich der Benutzer anmeldet oder abmeldet.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Verwendungsbeispiel</p></td>
<td align="left"><p>Sie können den Ordner "Dokumente", der in der Regel auf der lokalen Festplatte des Computers&#39;gespeichert ist, an einen Netzwerkspeicherort umleiten. Der Benutzer kann von jedem Computer im Netzwerk aus auf die Dokumente im Ordner zugreifen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Weitere Ressourcen</p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/cc778976.aspx" data-raw-source="[Folder redirection overview](https://technet.microsoft.com/library/cc778976.aspx)">Übersicht über Ordnerumleitung</a></p></td>
</tr>
</tbody>
</table>
















