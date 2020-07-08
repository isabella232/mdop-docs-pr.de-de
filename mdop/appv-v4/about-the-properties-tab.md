---
title: Informationen zur Registerkarte „Eigenschaften“
description: Informationen zur Registerkarte „Eigenschaften“
author: dansimp
ms.assetid: a6cf6f51-3778-4c8d-9632-3af4005775d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b2d6c3e01dde48fdd6701984f66610ea0333b74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808100"
---
# Informationen zur Registerkarte „Eigenschaften“


Verwenden Sie die Registerkarte **Eigenschaften** , um grundlegende statistische Informationen zu einem sequenzierten Anwendungspaket anzuzeigen. Sofern nicht anders angegeben, werden die Informationen automatisch generiert. Diese Registerkarte enthält die folgenden Elemente.

## Paketinformationen


<a href="" id="package-name"></a>**Paket Name**  
Der einzelne Name für ein sequenziertes Anwendungspaket, das möglicherweise eine oder mehrere Anwendungen enthält – beispielsweise kann Microsoft Office verwendet werden, um ein sequenziertes Anwendungspaket zu beschriften, das Microsoft Word-und Microsoft Excel-Anwendungen enthält, die in derselben virtuellen Umgebung ausgeführt werden.

<a href="" id="comments"></a>**Anmerkungen**  
Zeigt eine kurze Beschreibung des Softwarepakets an, das im abstrakten Element "Open Software Descriptor (OSD)-Datei" angezeigt wird. Dieses Element ist optional.

<a href="" id="package-version"></a>**Paket Version**  
Die Version des sequenzierten Anwendungspakets.

<a href="" id="package-guid"></a>**Paket-GUID**  
Die GUID (Globally Unique Identifier), die dem sequenzierten Anwendungspaket automatisch zugewiesen wird, um Sie von anderen sequenzierten Anwendungspaketen zu unterscheiden, die möglicherweise auf dem Computer ausgeführt werden, auf dem ein sequenziertes Anwendungspaket gestreamt wird.

<a href="" id="package-version-guid"></a>**Paketversions-GUID**  
Die Versions-GUID des sequenzierten Anwendungspakets.

<a href="" id="root-directory"></a>**Stammverzeichnis**  
Das Verzeichnis auf dem Sequenzcomputer, in dem Dateien für das sequenzierte Anwendungspaket installiert sind. Dieses Verzeichnis wird auch auf dem Computer erstellt, auf dem ein sequenziertes Anwendungspaket gestreamt wird. Es wird empfohlen, für die Abwärtskompatibilität zu sorgen, dass es sich um einen 8,3-Format Verzeichnisnamen am Stamm des Q-Laufwerks handelt, beispielsweise Q:\\MyApp.1\\.

<a href="" id="created"></a>**Erstellt**  
Das Datum und die Uhrzeit der Erstellung des sequenzierten Anwendungspakets.

<a href="" id="modified"></a>**Geändert**  
Das Datum und die Uhrzeit, zu der das sequenzierte Anwendungspaket zuletzt geändert wurde.

<a href="" id="package-size"></a>**Paketgröße**  
Die Größe des Pakets in Megabytes.

<a href="" id="launch-size"></a>**Startgröße**  
Die Größe in Megabyte des Teils der SFT-Datei, die zum Starten der Anwendung erforderlich ist.

## Sequenz Parameter


<a href="" id="block-size"></a>**Block Größe**  
Gibt die Größe des primären und des sekundären Funktionsblocks an, in die die SFT-Datei für das Streaming in einem Netzwerk aufgeteilt wird. Alle Blöcke entsprechen der angegebenen Größe; Allerdings kann der letzte Block kleiner als angegeben sein. Es wird einer der folgenden Werte angezeigt:

-   4 KB

-   16 KB

-   32 KB

-   64 KB

**Hinweis**  Nachdem das ursprüngliche Paket erstellt wurde, kann der Block Size-Wert nicht geändert werden.

 

## Verwandte Themen


[So ändern Sie die Paketeigenschaften](how-to-change-package-properties.md)

[Sequencer Console](sequencer-console.md)

 

 





