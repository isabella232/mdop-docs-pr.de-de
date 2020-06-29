---
title: So ändern Sie die Betriebssysteme, die mit einer vorhandenen Windows Installer-Datei verknüpft sind
description: So ändern Sie die Betriebssysteme, die mit einer vorhandenen Windows Installer-Datei verknüpft sind
author: dansimp
ms.assetid: 0633f7e2-aebf-4e00-be02-35bc59dec420
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63184852f996cbe09b476f456f7c2b509549f4fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806912"
---
# So ändern Sie die Betriebssysteme, die mit einer vorhandenen Windows Installer-Datei verknüpft sind


Gehen Sie wie folgt vor, um die Betriebssystemversionen zu ändern, die einer vorhandenen Windows Installer-Datei (**MSI**) zugeordnet sind, die mithilfe von App-V Sequencer erstellt wurde.

**So ändern Sie die Betriebssysteme einer vorhandenen Windows Installer-Datei**

1.  Installieren Sie den App-V-Sequencer auf einem Computer in Ihrer Umgebung, auf dem nur das Betriebssystem installiert ist. Alternativ können Sie den Sequencer auf einem Computer mit einer virtuellen Umgebung installieren – beispielsweise Microsoft Virtual PC. Diese Methode ist hilfreich, da es einfacher ist, eine saubere Sequenz Umgebung beizubehalten, die Sie mit minimaler zusätzlicher Konfiguration wieder verwenden können. Weitere Informationen zum Installieren des App-V-Sequencers finden Sie unter so wird es [gemacht: Installieren des Sequencers](how-to-install-the-sequencer.md).

2.  Kopieren Sie das gesamte virtuelle Anwendungspaket, das die Windows Installer-Datei enthält, die Sie ändern möchten, auf den Computer, auf dem der Sequencer ausgeführt wird.

3.  Wenn Sie die Windows Installer-Datei ändern möchten, öffnen Sie die Sequencer-Konsole, wählen Sie **Paket**  /  **Öffnen**aus, und navigieren Sie dann zu dem Speicherort, an dem das mit der Windows Installer-Datei verknüpfte virtuelle Anwendungspaket gespeichert ist.

4.  Zum Hinzufügen oder Entfernen von Betriebssystemen wählen Sie die Registerkarte **Bereitstellung** in der Sequencer-Konsole aus. Wenn Sie zusätzliche Betriebssysteme angeben möchten, die der Windows Installer-Datei zugeordnet werden sollen, wählen Sie das gewünschte Betriebssystem aus, und klicken Sie dann auf den Pfeil, der auf das **ausgewählte** Betriebssystem Listen-Steuerelement zeigt.

    Wenn Sie eine Betriebssystem Zuordnung entfernen möchten, wählen Sie das zu entfernende Betriebssystem aus, und klicken Sie dann auf den Pfeil, der auf das **Verfügbare** Betriebssystem Listen-Steuerelement zeigt.

5.  Zum Erstellen eines neuen Windows Installers, der dem virtuellen Anwendungspaket zugeordnet wird, wählen Sie **Microsoft Windows Installer (MSI)-Paket generieren**aus. Sie können auch Tools zum **Tools**  /  **Erstellen von MSI**auswählen.

    **Hinweis**  Wenn Sie **Tools** / **Create MSI** auswählen, um eine neue Windows Installer-Datei zu erstellen, können Sie **Schritt 6** dieses Verfahrens überspringen.

     

6.  Zum Speichern des virtuellen Anwendungspakets wählen Sie **Paket**  /  **Speichern**aus.

## Verwandte Themen


[Aufgaben für den Application Virtualization Sequencer](tasks-for-the-application-virtualization-sequencer.md)

 

 





