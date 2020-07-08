---
title: Informationen zu Application Virtualization-Paketen
description: Informationen zu Application Virtualization-Paketen
author: dansimp
ms.assetid: 69bd35c1-7af3-43db-931b-3074780aa926
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cfe6df90881ea4179fa8cd224609ca6d28ff5f61
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808164"
---
# Informationen zu Application Virtualization-Paketen


In Application Virtualization ist ein *Paket* die Ausgabe des Sequenz Prozesses. Sie verwenden Pakete, wenn Sie zuerst Anwendungen auf Ihren Servern bereitstellen und Anwendungen mit einer neuen Version aktualisieren. Mit Paketen können Sie virtuelle Anwendungsversionen auf Ihren Application Virtualization Management-Servern steuern. Ein einzelnes Paket kann mindestens eine Anwendung enthalten. Jedes Anwendungspaket enthält eine Reihe von Dateien als eigenständige Einheit.

## Verwalten von Paketen


Nachdem der Sequencer ein Paket aus einer oder mehreren Anwendungen als Teil des Prozesses erstellt hat, können Sie die vom Sequencer generierten Dateien auf einen Application Virtualization Management-Server kopieren und für das Streaming verfügbar machen.

Verfügbare Pakete werden unter dem Container **Pakete** im linken Bereich der Application Virtualization-Verwaltungskonsole angezeigt. Wenn Sie eine Anwendung mit einer Sequencer Project-Datei (SPRJ) oder einer Open Software Descriptor-Datei (OSD) importieren, wird im Container **Pakete** ein verwandter Eintrag angezeigt. In der Application Virtualization Server-Verwaltungskonsole können Sie Pakete und Versionen davon bereitstellen, aktualisieren oder löschen.

Jede virtuelle Anwendung verfügt über ein zugeordnetes Paket. Dieses Paket enthält die folgenden Dateien:

-   SFT – die Datei, die die Anwendung an Clients streamt.

-   OSD – die Open Software Descriptor-Datei enthält die Informationen, die zum Suchen und Starten der Anwendung erforderlich sind.

-   ICO – die Symboldatei, die die Anwendung visuell in Benutzeroberflächen und Tastenkombinationen darstellt.

-   SPRJ – die Projektdatei des Sequencers.

Wenn Sie die SPRJ-Datei importieren, stehen standardmäßig alle sequenzierten Anwendungen für die Bereitstellung zur Verfügung, die Anwendungen sind jedoch nicht für Streaming aktiviert. Sie können auswählen, ob alle oder einige der Anwendungen im Paket gestreamt werden sollen. Wenn Sie beispielsweise Microsoft Office sequenziert und importiert haben, können Sie auswählen, dass einige Anwendungen nicht bereitgestellt werden sollen, beispielsweise den Assistenten zum Speichern meiner Einstellungen. Klicken Sie in diesem Fall mit der rechten Maustaste auf jede Anwendung, die Sie bereitstellen möchten, wählen Sie **Eigenschaften**aus, und stellen Sie sicher, dass das Feld **aktiviert** (leer) deaktiviert ist. Nur die Anwendungen mit **aktiviertem aktivierten** Feld werden auf Clientcomputer gestreamt.

Nachdem Sie ein Paket neu sequenziert und eine neue SFT-Datei für das Streaming erstellt haben, können Sie das alte Paket schnell und einfach über die Application Virtualization Server-Verwaltungskonsole aktualisieren.

Das einzige operationelle Szenario, in dem Sie den Knoten **Pakete** verwenden müssen, ist, wenn Sie eine neue Version (SFT-Datei) für das Paket einführen. Wenn Sie Anwendungen importieren, Anwendungen Zugriff und Lizenzen zuweisen usw., verfolgt das Application Virtualization System diese Informationen auf Paketebene. Das bedeutet, dass Sie dem Benutzer die Berechtigung erteilen, eine Anwendung im gleichen Paket auszuführen, wenn Sie einen Benutzer zur Verwendung einer Anwendung autorisieren.

### Paket Version

Eine Paketversion wird durch eine bestimmte SFT-Datei dargestellt. Wenn Sie ein Paket aktualisieren (ein Update auf eine Anwendung anwenden oder einem Paket eine Anwendung hinzufügen), erstellen Sie eine neue SFT-Datei. Jedes Mal, wenn Sie eine neue SFT-Datei erstellen, erstellen Sie eine neue Paketversion.

Wenn Sie Anwendungen über die Application Virtualization Server-Verwaltungskonsole importieren, erstellt die Software automatisch ein Paket und eine Paketversion, wenn Sie noch nicht vorhanden sind.

## Verwandte Themen


[Informationen zu Application Virtualization-Anwendungen](about-application-virtualization-applications.md)

[Informationen zur Application Virtualization Server Management Console](about-the-application-virtualization-server-management-console.md)

[So verwalten Sie die Pakete in der Server Management Console](how-to-manage-packages-in-the-server-management-console.md)

 

 





