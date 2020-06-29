---
title: Informationen zur Registerkarte „Dateien“
description: Informationen zur Registerkarte „Dateien“
author: dansimp
ms.assetid: 3c20e720-4b0f-465b-b7c4-3013dae1c815
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5e71cd0b60f9722da9736fc6987100f5c7bf53ab
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808103"
---
# Informationen zur Registerkarte „Dateien“


Die Registerkarte " **Dateien** " zeigt die vollständige Liste der Dateien an, die in einem sequenzierten Anwendungspaket enthalten sind. Im linken Bereich wird in einem standardmäßigen Datei durchsuchen-Format die vollständige Liste der Dateien in dem Paket angezeigt, das während der Anwendungssequenzierung erstellt wurde. Zu diesen Dateien gehören das Paketstammverzeichnis (das Verzeichnis, das Sie während der Anwendungs Installationsphase angegeben haben), der Ordner Virtual File System (VFS) und die virtuellen Umgebungsdateien. Der Rechte Bereich zeigt den Dateinamen, die Dateiattribute und die Sequencer-Attribute an.

## Dateiname und Kurzname


<a href="" id="file-name"></a>**Dateiname**  
Der Name der Datei befindet sich im linken Bereich. Die im linken Bereich angezeigten Dateien werden während der Sequenzierung erstellt.

<a href="" id="short-name"></a>**Kurzname**  
Hierbei handelt es sich um den Namen einer im linken Bereich ausgewählten Datei, die in der 8,3-Format Benennungskonvention geschrieben wurde.

## Dateiattribute


<a href="" id="file-size"></a>**Dateigröße**  
Die Größe der Datei in Bytes.

<a href="" id="file-version"></a>**Datei Version**  
Die Version der ausgewählten Datei.

<a href="" id="date-created"></a>**Datum der Erstellung**  
Das Datum und die Uhrzeit, zu der die ausgewählte Datei erstellt wurde.

<a href="" id="date-modified"></a>**Änderungsdatum**  
Das Datum und die Uhrzeit, zu der die ausgewählte Datei zuletzt geändert wurde.

<a href="" id="file-id"></a>**Datei-ID**  
Die Datei-GUID.

## Sequencer-Attribute


<a href="" id="user-data"></a>**Benutzerdaten**  
Wählen Sie dieses Attribut aus, um anzugeben, dass eine Anwendung die Informationen eines einzelnen Benutzers beibehalten muss.

<a href="" id="application-data"></a>**Anwendungsdaten**  
Wählen Sie dieses Attribut aus, um anzugeben, dass eine Anwendung die allgemeinen Informationen einer Gruppe von Benutzern beibehalten muss.

<a href="" id="override"></a>**Außer Kraft setzen**  
Wenn diese Option ausgewählt ist, wird die entsprechende Datei vom Application Virtualization Desktop Client überschrieben, wenn das sequenzierte Anwendungspaket aktualisiert und an den Client gestreamt wird. Wenn dieses Kontrollkästchen nicht aktiviert ist, bestimmt der Client, ob die ausgewählte Datei überschrieben werden soll.

## Verwandte Themen


[So ändern Sie die in einem Paket enthaltenen Dateien](how-to-modify-the-files-included-in-a-package.md)

[Sequencer Console](sequencer-console.md)

 

 





