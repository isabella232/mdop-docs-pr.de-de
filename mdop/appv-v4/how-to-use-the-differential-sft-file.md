---
title: So verwenden Sie die differenzielle SFT-Datei
description: So verwenden Sie die differenzielle SFT-Datei
author: dansimp
ms.assetid: 607e30fd-2f0e-4e2f-b669-0b3f010aebb0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 85cc45f9665569d77fcf275db6dbc080eb919229
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806687"
---
# So verwenden Sie die differenzielle SFT-Datei


Beim Sequenzieren einer Anwendung erstellt der Microsoft Application Virtualization (App-V)-Sequenzer SFT-Dateien (. SFT), um alle Dateien der virtuellen Anwendung und die Konfigurationsinformationen zu speichern. In Version 4.5 von App-V wurde die differenzielle SFT-Datei (. dsft) eingeführt. Nachdem Sie den Sequencer zum Erstellen eines Upgrades für ein vorhandenes Paket verwendet haben, können Sie diese Datei generieren, um nur die Unterschiede zwischen dem ursprünglichen sequenzierten Anwendungspaket und der neuen Version zu speichern. Sie ist daher deutlich kleiner als die vollständige SFT-Datei für die neue Version der Anwendung und reduziert die Auswirkungen des Sendens von Paket Updates über Netzwerkverbindungen mit niedriger Bandbreite. Die Verwendung wird jedoch nur in bestimmten eingeschränkten Situationen unterstützt. Dieses Feature sollte speziell verwendet werden, wenn Sie ein ESD-System (Electronic Software Distribution) verwenden, um eine Gruppe von Benutzern mit einem lokalen Dateiserver über eine Verbindung mit niedriger Bandbreite zu verwalten, und Sie keine App-V-Streaming-Server verwenden.

Sie müssen die differenzielle SFT-Datei nicht verwenden, wenn Sie die Konfigurations Manager2007 verwenden, um die Benutzer zu verwalten, da Configuration Manager Unterstützung für Bereitstellungen mit niedriger Bandbreite bietet, die bereits integriert sind. Darüber hinaus ist es nicht erforderlich, wenn Sie Application Virtualization (App-V)-Verwaltungs-oder Streamingserver mit aktivem Upgrade verwenden, da der Client nur die Unterschiede zwischen den alten und den neuen Paketversionen abruft.

Das folgende Verfahren zeigt, wie Sie die mkdiffpkg.exe verwenden, die in der Sequencer-Installation enthalten ist, um die differenzielle SFT-Datei nach Abschluss des Upgrades des virtuellen Anwendungspakets zu erstellen und die differenzielle SFT-Datei bereitzustellen. Wenn Sie dieses Verfahren durchführen, können Sie sicherstellen, dass der Client, wenn das Paket auf dem Clientcomputer irgendwie entladen wird, beim nächsten Versuch des Benutzers, die Anwendung auszuführen, auf die Außerkraftsetzungs-URL zurückgreift, die für das Streamen des vollständigen Pakets v2. SFT aus der lokalen Dateifreigabe festgesetzt ist. Dadurch wird verhindert, dass der Benutzer beim Starten der Anwendung fehlerhaft ist. Wenn der gesamte Client beschädigt wird oder deinstalliert wird, empfiehlt es sich, das ESD-System so zu konfigurieren, dass die Vollversion des aktualisierten Pakets, v2. SFT, für den Client bereitgestellt wird.

Weitere Informationen zum Aktualisieren eines Pakets finden Sie unter "Aktualisieren einer vorhandenen virtuellen Anwendung" im App-v 4.5-Betriebshandbuch unter <https://go.microsoft.com/fwlink/?LinkId=133129>

**Hinweis**  Voraussetzung ist, dass alle Benutzer Computer, für die das ESD-Ziel vorgesehen ist, die v1. SFT-Datei vollständig in den lokalen Cache geladen haben und das Dateistreaming auf allen Computern aktiviert sein muss.

 

**So verwenden Sie die differenzielle SFT-Datei**

1.  Melden Sie sich mit einem Konto mit Administratorrechten beim Sequencer-Computer an. Öffnen Sie das ursprüngliche Paket (v1) für das Upgrade im Sequencer, und aktualisieren Sie dann das Paket auf die neue Version (v2), und speichern Sie es als neues v2. SFT.

2.  Öffnen Sie ein Befehlsfenster im App-v 4.5 Sequencer-Installationsordner, und führen Sie den folgenden Befehl aus:

    `“mkdiffpkg.exe V2.sft V2.dsft”`

3.  Kopieren Sie mithilfe des ESD-Systems oder eines anderen Dateikopiervorgangs die vollständige v2-Paketinhalts Datei v2. SFT in eine lokale Dateifreigabe, auf die die Benutzer Computer in einer gut verbundenen Netzwerkverbindung zugreifen können.

4.  Legen Sie mithilfe des ESD-Systems eine Kopie der differenziellen SFT-Datei v2. dsft auf jedem Benutzer Computer ab.

5.  Führen Sie zum Importieren der Datei v2. dsft den folgenden SFTMIME-Befehl auf jedem Benutzer Computer aus:

    `“SFTMIME load package:<package name> /SFTPATH <path to V2.dsft>”`

6.  Führen Sie auf jedem Benutzer Computer den folgenden SFTMIME-Befehl aus, um die override-URL so festzulegen, dass Sie auf die v2. SFT-Datei verweist:

    `“SFTMIME configure package:<package name> /OverrideURL FILE://<network path to V2.sft>”`

**Hinweis:**  
-   Differenzielle SFT-Dateien müssen auf Clients in der richtigen Reihenfolge angewendet werden. Beispielsweise muss v2. dsft auf eine v1-Anwendung angewendet werden, bevor v3. dsft angewendet wird.

-   Die **Microsoft Windows Installer-Paketfunktion (MSI)** im Sequencer kann nicht mit der differenziellen SFT-Datei verwendet werden.

 

## Verwandte Themen


[Erstellen oder Aktualisieren virtueller Anwendungen mit dem App-V-Sequenzer](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





