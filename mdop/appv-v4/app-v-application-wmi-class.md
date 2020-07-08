---
title: WMI-Klasse für App-V-Anwendungen
description: WMI-Klasse für App-V-Anwendungen
author: dansimp
ms.assetid: b79b0d5a-ba57-442f-8bb4-d7154fc056f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a4e1e49e35b231ddb2a480a06c46e364121ac2d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809286"
---
# WMI-Klasse für App-V-Anwendungen


Beim Application Virtualization-Client (App-V) handelt es sich bei der **Anwendungs** Klasse um eine WMI-Klasse (Windows Management Instrumentation), die alle virtuellen Anwendungen auf dem Client darstellt.

Die folgende Syntax ist vom MOF-Code (Managed Object Format) vereinfacht. Der Code enthält alle geerbten Eigenschaften.

## Syntax


``` syntax
class Application
{
      string Name;
      string Version;
      string PackageGUID;
      datetime LastLaunchOnSystem;
      uint32 GlobalRunningCount;
      boolean Loading;
      string OriginalOsdPath;
      string CachedOsdPath;
};
```

## Anforderungen


## Eigenschaften


<a href="" id="name"></a>**Name**  
Datentyp: **Zeichenfolge**

Access-Typ: schreibgeschützt

Qualifizierer: Schlüssel

Der Anzeigename der virtuellen Anwendung.

<a href="" id="version"></a>**Version**  
Datentyp: **Zeichenfolge**

Access-Typ: schreibgeschützt

Qualifizierer: Schlüssel

Die Version der virtuellen Anwendung.

<a href="" id="packageguid"></a>**PackageGUID**  
Datentyp: **Zeichenfolge**

Access-Typ: schreibgeschützt

Qualifizierer: keine

Die GUID des Pakets, dem die virtuelle Anwendung zugeordnet ist.

<a href="" id="lastlaunchonsystem"></a>**LastLaunchOnSystem**  
Datentyp: **DateTime**

Access-Typ: schreibgeschützt

Qualifizierer: keine

Das Datum und die Uhrzeit des letzten Starts der virtuellen Anwendung.

<a href="" id="globalrunningcount"></a>**GlobalRunningCount**  
Datentyp: **UInt32**

Access-Typ: schreibgeschützt

Qualifizierer: keine

Die Anzahl der ausgeführten Instanzen der virtuellen Anwendung, die direkt gestartet wurden.

<a href="" id="loading"></a>**Laden**  
Datentyp: **boolescher Wert**

Access-Typ: schreibgeschützt

Qualifizierer: keine

" **true** ", wenn die virtuelle Anwendung gestartet wird; andernfalls **false**.

<a href="" id="originalosdpath"></a>**OriginalOsdPath**  
Datentyp: **Zeichenfolge**

Access-Typ: schreibgeschützt

Qualifizierer: keine

Der ursprüngliche Dateipfad der OSD-Datei, die beim App-V-Client registriert wurde.

<a href="" id="cachedosdpath"></a>**CachedOsdPath**  
Datentyp: **Zeichenfolge**

Access-Typ: schreibgeschützt

Qualifizierer: keine

Der Dateipfad der OSD-Datei, wenn der App-V-Client die OSD-Datei lokal zwischengespeichert hat.

 

 





