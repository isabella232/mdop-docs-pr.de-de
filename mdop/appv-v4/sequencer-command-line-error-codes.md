---
title: Sequencer-Befehlszeilenfehlercodes
description: Sequencer-Befehlszeilenfehlercodes
author: dansimp
ms.assetid: 3d491314-4923-45fd-9839-c541c5e620bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 74f5bd0c1b66656ac6891dcc1c019254fa36fdac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806355"
---
# Sequencer-Befehlszeilenfehlercodes


Verwenden Sie die folgende Liste, um Fehler zu identifizieren, die sich auf die Sequenzierung von Anwendungen beziehen, indem Sie die Befehlszeile verwenden. Sie können diese Informationen auch anzeigen, indem Sie die zugehörige App-V Sequencer-Protokolldatei anzeigen.

**Hinweis**  Während der Sequenzierung können mehrere Fehler auftreten, und wenn dies der Fall ist, kann der angezeigte Fehlercode die Summe von zwei Fehlercodes sein. Wenn beispielsweise die */InstallPath* -und */OutputFile* -Parameter fehlen, gibt der App-V-Sequenzer **96**zurück – die Summe der beiden Fehlercodes.

 

<a href="" id="01"></a>01  
Es ist ein nicht spezifizierter Fehler aufgetreten.

<a href="" id="02"></a>02  
Das angegebene Installationsverzeichnis (/INSTALLPACKAGE) ist ungültig.

<a href="" id="04"></a>04  
Das angegebene Paketstammverzeichnis (/INSTALLPATH) ist ungültig.

<a href="" id="08"></a>08  
Der angegebene */OutputFile* -Parameter ist ungültig.

<a href="" id="16"></a>16  
Das Installationsverzeichnis (/INSTALLPACKAGE) ist nicht angegeben.

<a href="" id="32"></a>32  
Das Paketstammverzeichnis (/INSTALLPATH) ist nicht angegeben.

<a href="" id="64"></a>64  
Der */OutputFile* -Parameter ist nicht angegeben.

<a href="" id="128"></a>128  
Das angegebene Application Virtualization-Laufwerk ist ungültig.

<a href="" id="256"></a>256  
Fehler beim Installationsprogramm.

<a href="" id="512"></a>512  
Fehler beim Sequenzieren der Anwendung.

<a href="" id="1024"></a>1024  
Fehler beim Auswerten installierter Verknüpfungen.

<a href="" id="2048"></a>2048  
Das sequenzierte Anwendungspaket kann nicht gespeichert werden.

<a href="" id="4096"></a>4096  
Der angegebene Paket Name (/PACKAGENAME) ist ungültig.

<a href="" id="8192"></a>8192  
Die angegebene Blockgröße (/Blocksize) ist ungültig.

<a href="" id="16384"></a>16384  
Der angegebene Komprimierungstyp (/Compression) ist ungültig.

<a href="" id="32768"></a>32768  
Der angegebene Projektpfad ist ungültig.

<a href="" id="65536"></a>65536  
Der angegebene Aktualisierungsparameter ist ungültig.

<a href="" id="131072"></a>131072  
Der angegebene Aktualisierungsprojekt Parameter ist ungültig.

<a href="" id="262144"></a>262144  
Der angegebene Decode path-Parameter ist ungültig.

<a href="" id="525288"></a>525288  
Der Paket Name ist nicht angegeben.

## Verwandte Themen


[Referenz zu Application Virtualization Sequencer](application-virtualization-sequencer-reference.md)

[Sequencer Befehlszeilenparameter](sequencer-command-line-parameters.md)

 

 





