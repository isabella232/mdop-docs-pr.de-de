---
title: Problembehandlung für Application Virtualization Sequencer
description: Problembehandlung für Application Virtualization Sequencer
author: dansimp
ms.assetid: 12ea8367-0b84-44e1-a885-e0539486556b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60c47b853c74d90afc21e9ca172c0eec2a2c7a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806204"
---
# Problembehandlung für Application Virtualization Sequencer


Dieses Thema enthält Informationen, die Sie bei der Behandlung allgemeiner Probleme beim Application Virtualization (App-V)-Sequenzer verwenden können.

## Durch das Erstellen einer SFTD-Datei mithilfe von App-V Sequencer wird die Versionsnummer unerwartet erhöht


Die Versionsnummer, die einer SFTD-Datei zugeordnet ist, nimmt unerwartet zu.

**Lösung**

Verwenden Sie die Befehlszeile, um eine neue SFT-Datei zu generieren. Wenn Sie die SFT-Datei über die Befehlszeile erstellen möchten, geben Sie an der Eingabeaufforderung Folgendes ein:

**mkdiffpkg.exe &lt; Base SFT-Dateinamen &gt; &lt; diff SFT-Dateiname&gt;**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a>Der Dateiname in der OSD-Datei ist nach dem Paket Upgrade nicht richtig


Nach dem Upgrade eines vorhandenen Pakets ist der Dateiname nicht richtig.

**Lösung**

Wenn Sie ein Paket für das Upgrade öffnen, sollten Sie das Root-Q:\\-Laufwerk als Ausgabespeicherort für das Paket angeben. Geben Sie keinen zugeordneten Dateinamen mit dem Ausgabespeicherort an.

## Die Microsoft Word2003-Standardinstallation führt zu einem Fehler beim Streamen an einen Client.


Wenn Sie Microsoft Word2003 zu einem Client streamen, wird ein Fehler zurückgegeben, aber Microsoft Word wird weiterhin ausgeführt.

**Lösung**

Umsequenzieren Sie das virtuelle Anwendungspaket, und wählen Sie **vollständige Installation**aus.

## Das Paket Upgrade funktioniert nicht, wenn Sie ein abhängiges Paket erstellen.


Wenn Sie ein abhängiges Paket erstellen, indem Sie die Paketaktualisierung verwenden und neue Registrierungseinträge hinzufügen, scheint es korrekt zu funktionieren, aber die aktualisierten Registrierungseinträge sind nicht verfügbar.

**Lösung**

Registrierungseinstellungen werden immer mit der ursprünglichen Version des Pakets gespeichert, sodass Updates für das Paket nur dann verfügbar sind, wenn Sie das ursprüngliche Paket repariert haben.

## Fehler beim Sequenz Versuch. NET 2.0


Wenn Sie ein Paket sequenzieren, das erfordert. NET 2.0 erhalten Sie eine Fehlermeldung.

**Lösung**

Sequenzierung von Paketen, die erforderlich sind. NET 2.0 wird nicht unterstützt.

## Verwandte Themen


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

 

 





