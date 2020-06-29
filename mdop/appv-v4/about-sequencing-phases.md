---
title: Informationen zum Sequenzierungsphasen
description: Informationen zum Sequenzierungsphasen
author: dansimp
ms.assetid: c1cb7b6c-204c-48f2-848c-4bd5a3d5ecb6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e3d1504f0af82f3d21806b38bb4640b6f7ebc45
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808132"
---
# Informationen zum Sequenzierungsphasen


Sequenzierung ist der Vorgang, mit dem Sie ein sequenziertes Anwendungspaket mithilfe von Microsoft Application Virtualization (App-V) Sequencer erstellen. Während der Sequenzierung überwacht und zeichnet der Sequencer alle Installations-und Einrichtungsprozesse für eine Anwendung auf und erstellt die folgenden Dateien: ico, OSD, SFT und SPRJ. Diese Dateien enthalten alle erforderlichen Informationen zu einer Anwendung und ermöglichen die Ausführung dieser Anwendung in einer virtuellen Umgebung.

Die vier Phasen zur Sequenzierung einer Anwendung und zum Erstellen eines virtuellen Anwendungspakets sind Installation, Start, Anpassung und speichern. In der folgenden Liste finden Sie Informationen zu den einzelnen Phasen:

1.  **Installationsphase**: Sie geben während der Installationsphase den Paketnamen und einen optionalen zugehörigen Kommentar an, der dem Paket zugeordnet wird. In dieser Phase können Sie auch erweiterte Überwachungsoptionen konfigurieren. Zu den erweiterten Überwachungsoptionen zählen die Angabe der Blockgröße und die Frage, ob automatische Updates während der Überwachung installiert werden. Der Sequencer zeichnet alle erforderlichen Informationen und Konfigurationen auf, die zum Erstellen eines virtuellen Anwendungspakets und der zugehörigen Datei-und Registrierungseinstellungen erforderlich sind.

    **Wichtig**  Wenn Sie die erweiterten Optionen anzeigen möchten, wählen Sie auf der Seite **Paketinformationen** die Option **erweiterte Überwachungsoptionen anzeigen** aus.

     

2.  **Startphase**: Sie können während der Startphase alle erforderlichen Dateizuordnungen und Sicherheitsbeschreibungen angeben, die mit dem Paket konfiguriert werden sollen. Sie sollten die Anwendung so oft wie erforderlich öffnen, um die Funktionalität und Stabilität der Anwendung sicherzustellen.

3.  **Anpassungsphase**: Sie können das Paket während der Anpassungsphase mithilfe der zugehörigen OSD-Dateien konfigurieren. Sie können angeben, ob zugeordnete Skripts innerhalb oder außerhalb der virtuellen Umgebung ausgeführt werden sollen, zusätzliche Aktionen angeben, die ausgeführt werden sollen, angeben, wie zugeordnete Skripts (synchron oder asynchron) ausgeführt werden sollen, und zusätzliche Skripts angeben, die im Benutzerkontext ausgeführt werden sollen.

4.  **Phase speichern**– während der speicherphase werden alle erforderlichen Dateien für das virtuelle Anwendungspaket erstellt. Die erstellten Dateien sind SPRJ, SFT, OSD, ICO, XML-Manifest und die Windows Installer-Datei (MSI).

## Verwandte Themen


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

 

 





