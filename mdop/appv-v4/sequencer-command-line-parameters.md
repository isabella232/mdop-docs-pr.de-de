---
title: Sequencer Befehlszeilenparameter
description: Sequencer Befehlszeilenparameter
author: dansimp
ms.assetid: 28fb875a-c302-4d95-b2e0-8dc0c5dbb0f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ecfa269de04cf3dcba30cbb4a40f9176f03f6571
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806352"
---
# Sequencer Befehlszeilenparameter


Sie können die folgenden Application Virtualization (App-V)-Sequenzer-Parameter verwenden, um eine Anwendung zu sequenzieren und eine vorhandene virtuelle Anwendung mithilfe einer Befehlszeile zu aktualisieren. Weitere Informationen zum Sequenzieren einer Anwendung mithilfe einer Befehlszeile finden Sie unter so wird es [gemacht: Sequenzierung einer neuen Anwendung mithilfe der Befehlszeile](how-to-sequence-a-new-application-by-using-the-command-line.md).

## Sequencer Befehlszeilenparameter


<a href="" id="-help-or---"></a>**/Help oder/?**  
Zeigt Informationen zu Parametern an, die für die Verwendung einer Befehlszeile zur Sequenzierung von Anwendungen verfügbar sind.

<a href="" id="-installpackage-or--i"></a>**/INSTALLPACKAGE oder/i**  
Gibt den Windows Installer oder eine Batchdatei an, die zum Installieren einer Anwendung verwendet wird, damit Sie sequenziert werden kann.

<a href="" id="-installpath-or--p"></a>**/InstallPath oder/p**  
Gibt das Paketstammverzeichnis für eine Anwendung an.

<a href="" id="-outputfile-or--o"></a>**/OutputFile oder/o**  
Gibt den Pfad und den Dateinamen der SPRJ-Datei an, die generiert wird.

<a href="" id="-fullload-or--f"></a>**/FULLLOAD oder/f**  
Gibt an, ob alle Dateien im primären Feature-Block enthalten sein sollen. Wenn der Parameter **/FULLLOAD** in der Befehlszeile angegeben wird, werden alle zugeordneten Anwendungsdaten dem primären Feature-Block hinzugefügt. Wenn der **/FULLLOAD** -Parameter nicht in der Befehlszeile angegeben ist, wird dem primären Feature-Block keine der zugeordneten Anwendungsdaten hinzugefügt.

<a href="" id="-packagename-or--k"></a>**/PackageName oder k**  
Gibt den Paketnamen an, der der sequenzierten Anwendung zugewiesen wird.

<a href="" id="-blocksize"></a>**/BLOCKSIZE**  
Gibt die SFT-Datei Blockgröße an, die zum Streamen des Pakets an Clientcomputer verwendet wird. Sie können einen der folgenden Werte auswählen:

-   4 KB

-   16 KB

-   32 KB

-   64 KB

Sie sollten die Größe der SFT-Datei berücksichtigen, wenn Sie die Blockgröße angeben. Eine Datei mit einer kleineren Blockgröße dauert länger, um über das Netzwerk zu streamen, ist jedoch weniger bandbreitenintensiv. Dateien mit größeren Blockgrößen verwenden mehr Netzwerkbandbreite.

<a href="" id="-compression"></a>**/COMPRESSION**  
Gibt die Methode zum Komprimieren der SFT-Datei an, die an den Client gestreamt wird.

<a href="" id="-msi-or--m"></a>**/MSI oder/m**  
Gibt an, ob ein Windows Installer für die sequenzierte Anwendung erstellt werden soll.

<a href="" id="-default"></a>**/DEFAULT**  
Gibt die standardmäßige SPRJ-Datei an, die beim Erstellen eines virtuellen Anwendungspakets verwendet wird. Diese Datei wird als SPRJ-Vorlage verwendet, wenn die Anwendung zum ersten Mal sequenziert wird.

<a href="" id="-upgrade"></a>**/Upgrade**  
Gibt den Pfad und den Dateinamen der SPRJ-Datei an, die aktualisiert werden soll.

<a href="" id="-decodepath"></a>**/DECODEPATH**  
Gibt das Verzeichnis auf dem Sequenzcomputer an, auf dem die Dateien installiert sind, die dem sequenzierten Anwendungspaket zugeordnet sind. Verwenden Sie bei der Angabe des Verzeichnisses eines der folgenden Formate:

-   /DECODEPATH: f:

-   /DECODEPATH: q:

-   /DECODEPATH: "q:"

-   /DECODEPATH: "f:"

## Verwandte Themen


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

[Sequencer-Befehlszeilenfehlercodes](sequencer-command-line-error-codes.md)

 

 





