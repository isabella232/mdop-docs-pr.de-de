---
title: Spalten des Bereichs „Ergebnisse“ von „Anwendungen“
description: Spalten des Bereichs „Ergebnisse“ von „Anwendungen“
author: dansimp
ms.assetid: abae5ce2-40df-4f47-8062-f5eb6295c88c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c0138e40647a6a7d131a08aa03a9c9c1fcb071b3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807931"
---
# Spalten des Bereichs „Ergebnisse“ von „Anwendungen“


Im Bereich **Ergebnisse** des Knotens **Anwendungen** in der Application Virtualization Client Management Console können verschiedene Spalten angezeigt werden. Standardmäßig werden **Anwendungs**-, **Ausführungs**-, **Sperr**-und **Paket Status** angezeigt.

**Hinweis**  Sie können Spalten hinzufügen oder entfernen, indem Sie mit der rechten Maustaste auf den **Ergebnis** Bereich klicken, **Ansicht**auswählen und dann **Spalten hinzufügen/entfernen**auswählen.

 

Die Liste kann nach jeder beliebigen Spalte sortiert werden. Spalten, die Datums-und Uhrzeitangaben enthalten, werden in chronologischer Reihenfolge und nicht alphabetisch sortiert. Für Spalten, die eine Kombination aus Datums-und Uhrzeitangaben sowie Text enthalten, gelten Datums-und Uhrzeitangaben als vor allen anderen Text.

Die folgenden Spalten stehen zur Verfügung.

<a href="" id="application"></a>**Application**  
Der Name und die Version der Anwendung, getrennt durch ein Leerzeichen.

<a href="" id="application-in-use"></a>**Anwendung wird verwendet**  
Zeigt " **Ja** " oder " **Nein** " an, je nachdem, ob ein Benutzer die Anwendung verwendet (das heißt, Sie wird ausgeführt oder geladen).

<a href="" id="app-virt-server"></a>**App virt-Server**  
Der Application Virtualization-Server, von dem das Paket gestreamt wurde.

<a href="" id="cached-icon-file"></a>**Zwischengespeicherte Symboldatei**  
Der Name der Symboldateien im Cache (eine GUID in der aktuellen Implementierung).

<a href="" id="cached-icon-path"></a>**Zwischengespeicherter Symbolpfad**  
Der vollständige Pfad zu den Symboldateien im Cache.

<a href="" id="cached-launch-percent"></a>**Zwischengespeicherte Start Prozent**  
Der Prozentsatz der Startdaten der Anwendung, die sich derzeit im Cache befinden.

<a href="" id="cached-launch-size--mb-"></a>**Zwischengespeicherte Startgröße (MB)**  
Die Menge der Startdaten der Anwendung, die sich derzeit im Cache befinden.

<a href="" id="cached-osd-file"></a>**Zwischengespeicherte OSD-Datei**  
Der Name der OSD-Datei im Cache (bei der es sich um eine GUID in der aktuellen Implementierung handelt).

<a href="" id="cached-osd-path"></a>**Zwischengespeicherter OSD-Pfad**  
Der vollständige Pfad zur OSD-Datei im Cache.

<a href="" id="cached-package-percent"></a>**Zwischengespeichertes Paket Prozent**  
Der Prozentsatz des derzeit im Cache befindlichen Pakets.

<a href="" id="cached-package-size--mb-"></a>**Zwischengespeicherte Paketgröße (MB)**  
Die Größe des Teils des Pakets, das sich derzeit im Cache befindet.

<a href="" id="icon-file"></a>**Symboldatei**  
Der ursprüngliche Name der Symboldatei.

<a href="" id="icon-path"></a>**Symbolpfad**  
Der ursprüngliche Pfad oder die URL für die Symboldatei.

<a href="" id="last-system-launch"></a>**Letzter System Start**  
Der letzte Zeitpunkt, zu dem die Anwendung vom System gestartet wurde.

<a href="" id="last-user-launch"></a>**Letzter Start des Benutzers**  
Der letzte Zeitpunkt, zu dem die Anwendung vom Benutzer gestartet wurde.

<a href="" id="launch-size--mb-"></a>**Startgröße (MB)**  
Die unkomprimierte Größe der Paketdaten, die zum Starten der Anwendung erforderlich sind.

<a href="" id="locked"></a>**Gesperrt**  
Zeigt " **Ja** " oder " **Nein** " an, je nachdem, ob das Paket der Anwendung im Cache gesperrt ist.

<a href="" id="name"></a>**Name**  
Der Name der Anwendung.

<a href="" id="osd-file"></a>**OSD-Datei**  
Der ursprüngliche Name der OSD-Datei (Open Software Descriptor).

<a href="" id="osd-path"></a>**OSD-Pfad**  
Der vollständige ursprüngliche Pfad oder die URL der OSD-Datei.

<a href="" id="package-name"></a>**Paket Name**  
Der Name des Pakets.

<a href="" id="package-guid"></a>**Paket-GUID**  
Die GUID für das Paket.

<a href="" id="package-size--mb-"></a>**Paketgröße (MB)**  
Die Gesamtgröße der unkomprimierten Daten im Paket.

<a href="" id="package-status"></a>**Paket Status**  
Der aktuelle Betriebsstatus des Pakets.

<a href="" id="package-url"></a>**Paket-URL**  
Die URL für das Paket.

<a href="" id="package-version"></a>**Paket Version**  
Die Version für das Paket.

<a href="" id="package-version-guid"></a>**Paketversions-GUID**  
Die GUID für die Paketversion.

<a href="" id="running"></a>**Running**  
Zeigt " **Ja** " oder " **Nein** " an, je nachdem, ob der aktuelle Benutzer die Anwendung ausführt.

<a href="" id="source"></a>**Source**  
Woher die Anwendung kam – entweder der Name eines Anwendungs Publishing Servers oder "local" für Anwendungen, die direkt aus OSD-Dateien hinzugefügt wurden.

<a href="" id="version"></a>**Version**  
Die Anwendungsversion.

## Verwandte Themen


[Anwendungsknoten](applications-node.md)

[Bereich „Ergebnisse“ von „Anwendungen“](applications-results-pane.md)

[Referenz zur Application Virtualization Client Management Console](application-virtualization-client-management-console-reference.md)

 

 





