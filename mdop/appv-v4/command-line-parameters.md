---
title: Befehlszeilenparameter
description: Befehlszeilenparameter
author: dansimp
ms.assetid: d90a0591-f1ce-4cb8-b244-85cc70461922
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31d6ca1215648e2519e9818817ab5cc779a746d0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807892"
---
# Befehlszeilenparameter


Verwenden Sie die folgenden Application Virtualization Sequencer-Parameter, um eine Anwendung zu sequenzieren und ein sequenziertes Anwendungspaket an der Eingabeaufforderung zu aktualisieren. Im Microsoft Application Virtualization Sequencer-Verzeichnis geben Sie **SFTSequencer**und dann den entsprechenden Parameter ein.

<a href="" id="-help-or---"></a>*/Help* oder */?*  
Verwenden Sie diese Funktion, um die Liste der für die Befehlszeilen Sequenz verfügbaren Parameter anzuzeigen.

<a href="" id="-installpackage-or--i"></a>*/INSTALLPACKAGE* oder */i*  
Hiermit können Sie das Installationsprogramm oder eine Batchdatei angeben, in der die Anwendung sequenziert werden soll.

<a href="" id="-installpath-or--p"></a>*/InstallPath* oder */p*  
Hiermit geben Sie das Paketstammverzeichnis an.

<a href="" id="-outputfile-or--o"></a>*/OutputFile* oder */o*  
Hiermit geben Sie den Pfad und den Dateinamen der SPRJ-Datei an, die generiert werden soll.

**Wichtig**  Der */OutputFile* -Parameter steht beim Öffnen eines Pakets, das Sie nicht aktualisieren möchten, nicht zur Verfügung.

 

<a href="" id="-fullload-or--f"></a>*/FULLLOAD* oder */f*  
Verwenden Sie diese Option, um anzugeben, ob alles im primären Feature-Block platziert werden soll.

<a href="" id="-packagename-or--k"></a>*/PackageName* oder *k*  
Hiermit geben Sie den Paketnamen der sequenzierten Anwendung an.

<a href="" id="-blocksize"></a>*/BLOCKSIZE*  
Gibt die SFT-Datei Blockgröße an, die zum Streamen des Pakets an Clientcomputer verwendet wird. Sie können einen der folgenden Werte auswählen:

-   4 KB

-   16 KB

-   32 KB

-   64 KB

Sie sollten die Größe der SFT-Datei berücksichtigen, wenn Sie die Blockgröße angeben. Eine Datei mit einer kleineren Blockgröße dauert länger, um über das Netzwerk zu streamen, ist jedoch weniger bandbreitenintensiv. Dateien mit größeren Blockgrößen verwenden mehr Netzwerkbandbreite.

<a href="" id="-compression"></a>*/COMPRESSION*  
Verwenden Sie diese Methode, um die Methode zum Komprimieren der SFT-Datei beim Streamen an den Client anzugeben.

<a href="" id="-msi-or--m"></a>*/MSI* oder */m*  
Hiermit geben Sie an, wie ein Microsoft Windows Installer-Paket für die sequenzierte Anwendung generiert wird.

<a href="" id="-default"></a>*/DEFAULT*  
Gibt die standardmäßige SPRJ-Datei an, die beim Erstellen eines virtuellen Anwendungspakets verwendet wird. Diese Datei wird als SPRJ-Vorlage verwendet, wenn die Anwendung zum ersten Mal sequenziert wird.

<a href="" id="-upgrade"></a>*/Upgrade*  
Gibt den Pfad und den Dateinamen der SPRJ-Datei an, die aktualisiert werden soll.

<a href="" id="-decodepath"></a>*/DECODEPATH*  
Gibt das Verzeichnis auf dem Sequenzcomputer an, auf dem die Dateien installiert sind, die dem sequenzierten Anwendungspaket zugeordnet sind. Verwenden Sie bei der Angabe des Verzeichnisses eines der folgenden Formate:

-   /DECODEPATH: f:

-   /DECODEPATH: q:

-   /DECODEPATH: "q:"

-   /DECODEPATH: "f:"

## Verwandte Themen


[Informationen zum Verwenden der Sequencer-Befehlszeile](about-using-the-sequencer-command-line.md)

[So öffnen Sie eine sequenzierte Anwendung über die Befehlszeile](how-to-open-a-sequenced-application-using-the-command-line.md)

[So aktualisieren Sie ein Paket mit dem Befehl „Paket öffnen“](how-to-upgrade-a-package-using-the-open-package-command.md)

 

 





