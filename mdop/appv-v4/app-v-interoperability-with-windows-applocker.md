---
title: App-V-Interoperabilität mit Windows AppLocker
description: App-V-Interoperabilität mit Windows AppLocker
author: dansimp
ms.assetid: 9a488034-607d-411c-b495-ff184c726f49
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6f67bb87c0a4474acee3c4982b65c930e86c4917
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809280"
---
# App-V-Interoperabilität mit Windows AppLocker


Version 4,5 SP1 des Microsoft Application Virtualization (App-V)-Clients unterstützt das AppLocker-Feature von Windows 7. Mit dem AppLocker-Feature können IT-Administratoren angeben, welche Anwendungen für die Ausführung auf Computern eingeschränkt sind. In diesem Dokument wird beschrieben, wie Sie die AppLocker-Regeln für die Verwendung der virtuellen App-V-Umgebung und virtualisierten Anwendungen konfigurieren.

**Hinweis**  Windows-AppLocker muss zuerst aktiviert werden, bevor Windows-AppLocker-Regeln für virtuelle Anwendungen konfiguriert werden. Weitere Informationen zum Aktivieren von Windows AppLocker finden Sie unter [Windows AppLocker](https://go.microsoft.com/fwlink/?LinkId=156732) ( https://go.microsoft.com/fwlink/?LinkId=156732) .

 

## Konfigurieren von Windows-AppLocker-Regeln für virtuelle Anwendungen


Lokale Administratoren können Windows-AppLocker-Regeln erstellen, die die Ausführung von ausführbaren Programmen (exe-Dateien), Windows Installer-Dateien (MSI-und MSP-Dateien) und Skripts (PS-, bat-, cmd-, VBS-und JS-Dateien) einschränken. Der Administrator verwendet dazu einen Referenzcomputer, auf dem der App-V-Client installiert ist und auf dem alle relevanten virtuellen Anwendungen in den Clientcache gestreamt werden. Der Administrator verwendet dann den Windows-AppLocker-Abschnitt des lokalen Sicherheitsrichtlinien-Snap-Ins Microsoft Management Console (MMC) auf dem Referenzcomputer, um die Regeln zu erstellen.

Wenn Sie nach einem Verzeichnispfad oder einer bestimmten Datei suchen, für die Sie eine Regel erstellen möchten, können Sie auf das App-V-Laufwerk zugreifen, indem Sie den Pfad zur verborgenen Freigabe verwenden. So können Sie beispielsweise zu \\\\localhost\\Q $ wechseln, wobei das App-V-Laufwerk Laufwerk Q ist. Um die Regel zu erstellen, müssen Sie den Pfad jedoch bearbeiten, um den Verweis auf \\\\localhost\\Q $ zu entfernen und stattdessen Q:\\ zu verwenden. Sie müssen jede Anwendung auf dem Referenzcomputer starten, um auf die Dateien der Anwendung zuzugreifen, und es sind Administratorrechte erforderlich, um \\\\localhost\\Q $ zu durchsuchen.

 

 





