---
title: Veröffentlichen von virtuellen Anwendungen mit Electronic Software Distribution
description: Veröffentlichen von virtuellen Anwendungen mit Electronic Software Distribution
author: dansimp
ms.assetid: 295fbc1d-ed1c-43b4-aeee-0df384d4e630
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0354fc1226aa78d947dd764a0ab6157b563a321
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806428"
---
# Veröffentlichen von virtuellen Anwendungen mit Electronic Software Distribution


Ein ESD-System (Electronic Software Distribution) wurde entwickelt, um Software effizient auf viele verschiedene Computer über langsame oder schnelle Netzwerkverbindungen zu verschieben. Mit Application Virtualization mithilfe eines ESD-Systems können Sie eine der folgenden Methoden verwenden, um Ihre virtuellen Anwendungspakete zu verteilen:

-   Konfigurieren Sie Ihr ESD-System, um die Pakete direkt an jeden Clientcomputer zu verteilen, indem Sie die Windows Installer-Version des Pakets verwenden, das vom Application Virtualization Sequencer generiert wird. Die Windows Installer-Datei enthält die Symbole, Paketdefinitionsinformationen und den Inhalt, und wenn Sie Windows Installer verwenden, werden die Symbole auf dem Windows-Desktop und im Startmenü veröffentlicht, und der Inhalt des Pakets wird in den Application Virtualization Client-Cache geladen. Der Benutzer kann die Anwendungen sofort ohne weitere Einrichtungsanforderungen verwenden. Das Upgrade eines Pakets auf eine neuere Version erfolgt mithilfe von Windows Installer, um die package.msi Datei zu deinstallieren und dann die neue Version zu installieren.

-   Platzieren Sie den Paketinhalt auf einem Softwareverteilungspunkt oder Application Virtualization Streaming Server, der für die Clientcomputer über eine Netzwerkverbindung mit guter Bandbreite wie einem LAN problemlos zugänglich ist. So können Sie beispielsweise die vorhandenen ESD-System Verteilungspunkt-Computer in jeder Zweigstelle verwenden. Mithilfe von Befehlszeilenparametern zum Definieren der Streaming-Quelle, aus der Clients das virtuelle Anwendungspaket streamen, wird das ESD-System die Windows Installer-Version des Pakets für jeden Client bereitstellen. Das ESD-System kann auch verwendet werden, um die SFT-Datei, die den Paketinhalt enthält, in die Dateifreigabe auf allen Streaming Servern zu kopieren. Das Upgrade eines Pakets auf eine neuere Version erfolgt mithilfe von Windows Installer, um die package.msi Datei zu deinstallieren und dann die neue Version zu installieren.

-   Als Alternative zur Verwendung der eigenständigen Windows Installer-Datei in einem der vorstehenden Modi zum Bereitstellen der Pakete können Sie die Bereitstellung auf eine viel detailliertere Weise steuern, indem Sie die Befehlszeilensprache Application Virtualization SFTMIME verwenden. Dies bietet zahlreiche Befehle, mit denen alle Aspekte der Verwaltung der Pakete gesteuert werden. Obwohl SFTMIME leistungsstark ist, ist es auch komplex, daher sollten Administratoren planen, alle Befehle als Skripts zu erstellen und diese in einer Testumgebung vor der Produktions Verwendung gründlich zu testen. Weitere Informationen zu den verfügbaren SFTMIME-Befehlen finden Sie unter [SFTMIME-Befehlsreferenz](sftmime--command-reference.md).

## Verwandte Themen


[Electronic Software Distribution-basiertes Szenario](electronic-software-distribution-based-scenario.md)

[Planen der Bereitstellung von Application Virtualization System](planning-for-application-virtualization-system-deployment.md)

[Planen einer Streaminglösung in einer ESD-Implementierung (Electronic Software Distribution)](planning-your-streaming-solution-in-an-electronic-software-distribution-implementation.md)

[SFTMIME-Befehlsreferenz](sftmime--command-reference.md)

 

 





