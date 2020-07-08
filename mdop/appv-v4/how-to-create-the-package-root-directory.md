---
title: So erstellen Sie das Stammverzeichnis des Pakets
description: So erstellen Sie das Stammverzeichnis des Pakets
author: dansimp
ms.assetid: bcfe3bd4-6c60-409a-8ffa-cc22f27194b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c9e1e7be71627d4e55eff7a4e2582a21b834876d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807183"
---
# So erstellen Sie das Stammverzeichnis des Pakets


Das Paketstammverzeichnis ist das Verzeichnis auf dem Computer, auf dem der App-V-Sequencer ausgeführt wird, in dem Dateien für die sequenzierte Anwendung installiert sind. Dieses Verzeichnis ist auch virtuell auf dem Computer vorhanden, auf den eine sequenzierte Anwendung gestreamt wird. Sie sollten das Paketstammverzeichnis erstellen, bevor Sie die Installation einer neuen Anwendung überwachen.

Nachdem Sie das Paketstammverzeichnis erstellt haben, können Sie mit der Sequenzierung von Anwendungen beginnen. Weitere Informationen zum Sequenzieren einer neuen Anwendung finden Sie unter [so wird es gemacht: Installieren des Sequencers](how-to-install-the-sequencer.md).

**So erstellen Sie das Paketstammverzeichnis**

1.  Zum Erstellen des Paketstammverzeichnisses ordnen Sie auf dem Computer, auf dem der App-V-Sequencer ausgeführt wird, das Q:\\-Laufwerk dem angegebenen Netzwerkspeicherort zu. Der von Ihnen angegebene Speicherort sollte über genügend Speicherplatz verfügen, um die Anwendung zu speichern, die Sie sequenzieren.

2.  Wenn Sie ein Verzeichnis erstellen möchten, das Sie für eine neue virtuelle Anwendung verwenden können, erstellen Sie einen Ordner auf dem Q:\\-Laufwerk, und weisen Sie ihm einen Namen zu.

    **Wichtig**  Der Name, den Sie virtuellen Anwendungsdateien zuweisen, die im Paketstammverzeichnis gespeichert werden, sollte das 8,3-Benennungsformat verwenden. Die Dateinamen dürfen nicht mehr als 8 Zeichen mit einer Dateinamenerweiterung mit drei Zeichen sein.

     

## Verwandte Themen


[Aufgaben für den Application Virtualization Sequencer](tasks-for-the-application-virtualization-sequencer.md)

 

 





