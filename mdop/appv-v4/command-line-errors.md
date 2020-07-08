---
title: Befehlszeilenfehler
description: Befehlszeilenfehler
author: dansimp
ms.assetid: eea62568-4e90-4877-9cc7-e27ef5c05068
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ab29a77dc15a8c7bd3590b918a7ca8c1ca6e8c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807895"
---
# Befehlszeilenfehler


Ermitteln Sie anhand der folgenden Fehlerliste die Gründe, warum die Befehlszeilen-Sequenzierung nicht ordnungsgemäß funktioniert. Sie können diese Fehler auch sehen, indem Sie die Sequencer-Protokolldatei anzeigen.

**Hinweis**  Bei der Sequenzierung wird möglicherweise mehr als ein Fehler angezeigt. Darüber hinaus kann der angezeigte Fehlercode die Summe von zwei Fehlercodes sein. Wenn beispielsweise die */InstallPath* -und */OutputFile* -Parameter fehlen, gibt Microsoft System Center Application Virtualization Sequencer 96 zurück – die Summe der beiden Fehlercodes.

 

<a href="" id="01"></a>01  
Es ist ein nicht spezifizierter Fehler aufgetreten.

<a href="" id="02"></a>02  
Das angegebene Installationsverzeichnis (/INSTALLPACKAGE) ist ungültig.

<a href="" id="04"></a>04  
Das angegebene Paketstammverzeichnis (/INSTALLPATH) ist ungültig.

<a href="" id="08"></a>08  
Der angegebene */OutputFile* -Parameter ist ungültig.

<a href="" id="16"></a>16  
Das Installationsverzeichnis (/INSTALLPACKAGE) wurde nicht angegeben.

<a href="" id="32"></a>32  
Das Paketstammverzeichnis (/INSTALLPATH) wurde nicht angegeben.

<a href="" id="64"></a>64  
Der */OutputFile* -Parameter wurde nicht angegeben.

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
Die angegebene Blockgröße (/Blocksize <em> ) </em> ist ungültig.

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
Der Paketname wurde nicht angegeben.

## Verwandte Themen


[Informationen zum Verwenden der Sequencer-Befehlszeile](about-using-the-sequencer-command-line.md)

[Befehlszeilenparameter](command-line-parameters.md)

 

 





