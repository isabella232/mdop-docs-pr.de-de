---
title: Behandeln von Problemen mit Zertifikatberechtigungen
description: Behandeln von Problemen mit Zertifikatberechtigungen
author: dansimp
ms.assetid: 06b8cbbc-93fd-44aa-af39-2d780792d3c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 728c35b9f51c8f2e18db8acd63708c70bb5d3100
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806215"
---
# Behandeln von Problemen mit Zertifikatberechtigungen


Wenn der private Schlüssel nach der Installation von App-v 4.5 nicht mit der richtigen Zugriffssteuerungsliste für den Netzwerkdienst konfiguriert wurde, wird ein Ereignis im NT-Ereignisprotokoll protokolliert, und es wird ein Eintrag in der `Sft-server.log` Datei gespeichert.

## Fehlermeldungen


### Windows Server2003

Ereignis-ID-36870 – es ist ein schwerwiegender Fehler beim Zugriff auf den privaten Schlüssel des SSL-Serveranmeldeinformationen aufgetreten. Der vom kryptografischen Modul zurückgegebene Fehlercode lautet 0x80090016.

### Windows Server2008

Ereignis-ID-36870 – es ist ein schwerwiegender Fehler beim Zugriff auf den privaten Schlüssel des SSL-Serveranmeldeinformationen aufgetreten. Der vom kryptografischen Modul zurückgegebene Fehlercode lautet 0x8009030d.

## SFT-Server. log


Die folgende Fehlermeldung befindet sich in der `sft-server.log` Datei im `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\logs` Verzeichnis:

Das Zertifikat konnte nicht geladen werden. Fehlercode \ [-2146893043 \]. Stellen Sie sicher, dass das Netzwerkdienstkonto über den richtigen Zugriff auf das Zertifikat und die zugehörige private Schlüsseldatei verfügt.

 

 





