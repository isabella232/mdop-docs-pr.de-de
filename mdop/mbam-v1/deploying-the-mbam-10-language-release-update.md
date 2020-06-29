---
title: Bereitstellen des Sprachrelease-Updates für MBAM 1.0
description: Bereitstellen des Sprachrelease-Updates für MBAM 1.0
author: dansimp
ms.assetid: 9dbd85c3-e470-4752-a90f-25754dd46dab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a819be81594efd9349e3f6c0f6559c2b810bdc9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804517"
---
# Bereitstellen des Sprachrelease-Updates für MBAM 1.0


Die Microsoft BitLocker-Verwaltungs-und-Überwachungs Version (MBAM) 1.0 ist ein Update für MBAM und umfasst die Unterstützung neuer Sprachen. Die neuen Sprachen sind:

-   Englisch (en-US)

-   Französisch (FR)

-   Italienisch (IT)

-   Deutsch (de)

-   Spanisch (es)

-   Koreanisch (Ko)

-   Japanisch (ja)

-   Brasilianisches Portugiesisch (PT-BR)

-   Russisch (ru)

-   Chinesisch (traditionell) (ZH-TW)

-   Chinesisch (vereinfacht) (ZH-CN)

Mit dem MBAM 1.0-sprach Update wird die Versionsnummer von MBAM 1.0.1237.1 in MBAM 1.0.2001 geändert.

Sie müssen nicht alle MBAM-Features erneut installieren, um diese zusätzlichen Sprachen hinzuzufügen. In diesem Thema werden die erforderlichen Schritte zum Hinzufügen der neu unterstützten Sprachen definiert.

## Bereitstellen der MBAM International-Version für MBAM-Server Features


Zunächst müssen Sie die folgenden MBAM-Server Features aktualisieren:

-   Konformitäts-und Überwachungsbericht

-   Verwaltungs-und Überwachungs Server

-   Richtlinienvorlagen

Anschließend müssen Sie **MbamSetup.exe** ausführen, um die MBAM-Features zu aktualisieren, die gleichzeitig auf dem gleichen Server ausgeführt werden.

[So installieren Sie das MBAM-Sprachupdate auf einem einzelnen Server](how-to-install-the-mbam-language-update-on-a-single-server-mbam-1.md)

[So installieren Sie das MBAM-Sprachupdate auf verteilten Servern](how-to-install-the-mbam-language-update-on-distributed-servers-mbam-1.md)

## Installieren des MBAM-sprach Updates für Gruppenrichtlinien


Die MBAM-Gruppenrichtlinienvorlagen können auf jeder Verwaltungsarbeitsstation installiert werden, oder Sie können in den zentralen Gruppenrichtlinien-Informationsspeicher kopiert werden, um die Vorlagen für alle Gruppenrichtlinienadministratoren verfügbar zu machen. Die Richtlinienvorlagen können nicht direkt auf einem Domänencontroller installiert werden. Wenn Sie keinen zentralen Gruppenrichtlinien Speicher verwenden, müssen Sie die Richtlinien manuell auf jeden Domänencontroller kopieren, der MBAM-Gruppenrichtlinien verwaltet.

Wenn Sie die Vorlagen für MBAM-Sprachrichtlinien hinzufügen möchten, kopieren Sie die Gruppenrichtlinien-Sprachdateien von%systemroot%\\PolicyDefinitions auf dem Computer, auf dem die Rolle "Richtlinienvorlagen" an demselben Speicherort auf dem Arbeitsstationscomputer installiert wurde. Im folgenden finden Sie einige Beispiele für Gruppenrichtliniendateien:

-   BitLockerManagement. ADMX

-   BitLockerUserManagement. ADMX

-   en-us\\BitLockerManagement.adml

-   en-us\\BitLockerUserManagement.adml

-   Fr-fr\\ BitLockerManagement. ADML

-   Fr-fr\\ BitLockerUserManagement. ADML

-   (und ebenso für jede unterstützte Sprache)

## Bekannte Probleme in der MBAM International-Version


Dieses Thema enthält bekannte Probleme bei der Microsoft BitLocker-Verwaltung und-Überwachung in der internationalen Version.

[Bekannte Probleme beim internationalen Release für MBAM](known-issues-in-the-mbam-international-release-mbam-1.md)

## Weitere Ressourcen für die Bereitstellung des MBAM 1,0-Sprach Updates


[Bereitstellen von MBAM 1.0](deploying-mbam-10.md)

 

 





