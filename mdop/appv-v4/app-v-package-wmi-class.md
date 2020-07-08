---
title: WMI-Klasse für APP-V-Pakete
description: WMI-Klasse für APP-V-Pakete
author: dansimp
ms.assetid: 0fc26c3b-9706-4804-be2d-645771dc33ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa452afaaeb2f490c179a928b24de47207d6dc63
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808051"
---
# WMI-Klasse für APP-V-Pakete


Im Application Virtualization-Client (App-V) ist die **Package** -Klasse eine WMI-Klasse (Windows Management Instrumentation), die alle virtuellen Pakete auf dem Client darstellt. Die virtuellen Pakete können viele virtuelle Anwendungen enthalten.

## Syntax


``` syntax
class Package
{
      string Name;
      string Version;
      string PackageGUID;
      string SftPath;
      uint64 TotalSize;
      uint64 CachedSize;
      uint64 LaunchSize;
      uint64 CachedLaunchSize;
      boolean InUse;
      boolean Locked;
      uint16 CachedPercentage;
      string VersionGUID;
 };
```

## Eigenschaften


<a href="" id="name"></a>**Name**  
Datentyp: **Zeichenfolge**

Access-Typ: schreibgeschützt

Qualifizierer: keine

Der benutzerfreundliche Name des virtuellen Pakets.

<a href="" id="version"></a>**Version**  
Datentyp: **Zeichenfolge**

Access-Typ: schreibgeschützt

Qualifizierer: keine

Die Version des virtuellen Pakets.

<a href="" id="packageguid"></a>**PackageGUID**  
Datentyp: **Zeichenfolge**

Access-Typ: schreibgeschützt

Qualifizierer: Schlüssel

Der GUID-Bezeichner der Paketkonfiguration und der Quelldateien.

<a href="" id="sftpath"></a>**SftPath**  
Datentyp: **Zeichenfolge**

Access-Typ: schreibgeschützt

Qualifizierer: keine

Der Dateipfad der SFT-Datei.

<a href="" id="totalsize"></a>**TotalSize**  
Datentyp: **UInt64**

Access-Typ: schreibgeschützt

Qualifizierer: keine

Die Gesamtgröße des virtuellen Pakets in Kilobytes.

<a href="" id="cachedsize"></a>**CachedSize**  
Datentyp: **UInt64**

Access-Typ: schreibgeschützt

Qualifizierer: keine

Die Gesamtgröße des Caches für das virtuelle Paket in Kilobytes.

<a href="" id="launchsize"></a>**LaunchSize**  
Datentyp: **UInt64**

Access-Typ: schreibgeschützt

Qualifizierer: keine

Die Gesamtgröße des primären Funktionsblocks des virtuellen Pakets in Kilobytes.

<a href="" id="cachedlaunchsize"></a>**CachedLaunchSize**  
Datentyp: **UInt64**

Access-Typ: schreibgeschützt

Qualifizierer: keine

Die Gesamtgröße des primären Feature Blocks des virtuellen Pakets, der zwischengespeichert wurde, in Kilobytes.

<a href="" id="inuse"></a>**InUse**  
Datentyp: **boolescher Wert**

Access-Typ: schreibgeschützt

Qualifizierer: keine

" **true** ", wenn eine virtuelle Anwendung im virtuellen Paket ausgeführt wird; andernfalls **false**.

<a href="" id="locked"></a>**Gesperrt**  
Datentyp: **boolescher Wert**

Access-Typ: schreibgeschützt

Qualifizierer: keine

**true** , wenn das virtuelle Paket gesperrt ist, andernfalls false. andernfalls **false**.

<a href="" id="cachedpercentage"></a>**CachedPercentage**  
Datentyp: **UInt16**

Access-Typ: schreibgeschützt

Qualifizierer: keine

Der Prozentsatz der Cachedateien. Basierend auf der folgenden Formel: CachedSize/TotalSize × 100.

<a href="" id="versionguid"></a>**VersionGUID**  
Datentyp: **Zeichenfolge**

Access-Typ: schreibgeschützt

Qualifizierer: keine

Der GUID-Bezeichner der Paketversion.

 

 





