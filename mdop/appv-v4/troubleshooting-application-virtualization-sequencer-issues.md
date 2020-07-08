---
title: Behandeln von Problemen mit Application Virtualization Sequencer
description: Behandeln von Problemen mit Application Virtualization Sequencer
author: dansimp
ms.assetid: 2712094b-a0bc-4643-aced-5415535f3fec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8b84f37217f29ff2c08a2254d7f54ce74348d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806228"
---
# Behandeln von Problemen mit Application Virtualization Sequencer


Dieses Thema enthält Informationen, die Sie bei der Behandlung allgemeiner Probleme beim Application Virtualization (App-V)-Sequenzer verwenden können.

## Durch das Erstellen einer SFTD-Datei mithilfe von App-V Sequencer wird die Versionsnummer unerwartet erhöht


Verwenden Sie die Befehlszeile, um eine neue SFT-Datei zu generieren. Wenn Sie die SFT-Datei über die Befehlszeile erstellen möchten, geben Sie an der Eingabeaufforderung Folgendes ein:

**mkdiffpkg.exe &lt; Base SFT-Dateinamen &gt; &lt; diff SFT-Dateiname&gt;**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a>Der Dateiname in der OSD-Datei ist nach dem Paket Upgrade nicht richtig


Wenn Sie ein Paket für das Upgrade öffnen, sollten Sie das Root-Q:\\-Laufwerk als Ausgabespeicherort für das Paket angeben. Geben Sie keinen zugeordneten Dateinamen mit dem Ausgabespeicherort an.

## Die Microsoft Word2003-Standardinstallation führt zu einem Fehler beim Streamen an einen Client.


Wenn Sie Microsoft Word2003 zu einem Client streamen, wird ein Fehler zurückgegeben, aber Microsoft Word wird weiterhin ausgeführt.

**Lösung**

Umsequenzieren Sie das virtuelle Anwendungspaket, und wählen Sie **vollständige Installation**aus.

## Das aktive Upgrade funktioniert nicht, wenn Sie ein abhängiges Paket erstellen.


Wenn Sie ein abhängiges Paket erstellen, indem Sie das aktive Upgrade verwenden und neue Registrierungseinträge hinzufügen, scheint es korrekt zu funktionieren, aber die aktualisierten Registrierungseinträge sind nicht verfügbar.

**Lösung**

Registrierungseinstellungen werden immer mit der ursprünglichen Version des Pakets gespeichert, sodass Updates für das Paket nur dann verfügbar sind, wenn Sie das ursprüngliche Paket repariert haben.

## Detaillierte Informationen sind für Microsoft office2007-Dokumente auf der Seite "Eigenschaften" nicht sichtbar


Wenn Sie versuchen, detaillierte Informationen zu einem Microsoft office2007-Dokument mithilfe der Eigenschaftenseite anzuzeigen, werden die detaillierten Informationen nicht angezeigt.

**Lösung**

App-V unterstützt nicht die erforderlichen Shell-Erweiterungen für diese Eigenschaftenseiten.

## Einige Registrierungsschlüssel werden nicht erfasst, wenn Sie 16-Bit-Anwendungen abgleichen


In App-V 4,5 wurde das Registrierungs-Hooking vom Kernelmodus in den Benutzermodus verschoben. Wenn Sie eine 16-Bit-Anwendung oder eine Anwendung, die ein 16-Bit-Installationsprogramm verwendet, abgleichen möchten, müssen Sie zuerst den Sequencer-Computer so konfigurieren, dass der Prozess in einer eigenen Kopie des Windows NT Virtual DOS Machine (NTVDM) ausgeführt wird.

**Lösung**

Bevor Sie die Anwendung sequenzieren, setzen Sie den folgenden globalen REGSZ-Registrierungsschlüsselwert auf "Ja" auf dem Sequenzcomputer:

HKLM\\SYSTEM\\CurrentControlSet\\Control\\WOW\\DefaultSeparateVDM

Sie müssen den Computer neu starten, bevor dies wirksam wird.

## Verwandte Themen


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

 

 





