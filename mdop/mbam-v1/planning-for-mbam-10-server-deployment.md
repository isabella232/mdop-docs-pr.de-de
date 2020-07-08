---
title: Planen der Serverbereitstellung für MBAM 1.0
description: Planen der Serverbereitstellung für MBAM 1.0
author: dansimp
ms.assetid: 3cbef284-3092-4c42-9234-2826b18ddef1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 76ff9c444ce3f9c39161341610fb0cd9a763dc6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804220"
---
# Planen der Serverbereitstellung für MBAM 1.0


Die Microsoft BitLocker-Serverinfrastruktur für die Verwaltungs-und Überwachungsdienste (MBAM) hängt von einer Reihe von Server Features ab, die basierend auf den Anforderungen Ihres Unternehmens auf einem oder mehreren Server Computern installiert werden können.

## Planen der Bereitstellung von MBAM Server


Die folgenden MBAM-Features stellen die Serverinfrastruktur für eine MBAM-Server Bereitstellung dar:

-   Wiederherstellungs-und Hardware Datenbank

-   Konformitäts-und Überwachungsdatenbank

-   Konformitäts-und Überwachungsberichte

-   Verwaltungs-und Überwachungs Server

MBAM Server-Datenbanken und-Features können je nach Ihren Skalierbarkeitsanforderungen in unterschiedlichen Konfigurationen installiert werden. Alle MBAM-Server Features können auf einem einzelnen Server installiert oder auf mehrere Server verteilt werden. Im Allgemeinen empfiehlt es sich, eine Konfiguration mit drei Servern oder fünf Servern für Produktionsumgebungen zu verwenden, auch wenn Konfigurationen von zwei oder vier Servern je nach Ihren Computeranforderungen ebenfalls verwendet werden können.

**Hinweis**  Weitere Informationen zur Leistungsskalierbarkeit von MBAM und empfohlenen Bereitstellungs Topologien finden Sie unter Whitepaper zur Skalierbarkeit von MBAM und Leitfaden für die höchst Verfügbarkeit <https://go.microsoft.com/fwlink/p/?LinkId=258314> .

 

Jedes MBAM-Feature hat bestimmte Voraussetzungen. Eine vollständige Liste der Voraussetzungen und Hardware-und Softwareanforderungen für Server Features finden Sie unter [MBAM 1,0-Bereitstellungsvoraussetzungen](mbam-10-deployment-prerequisites.md) und [unterstützte MBAM 1,0-Konfigurationen](mbam-10-supported-configurations.md).

Zusätzlich zu den serverbezogenen MBAM-Features umfasst die Server-Setup Anwendung eine MBAM-Gruppenrichtlinienvorlage. Diese Vorlage kann auf jedem Computer installiert werden, auf dem die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ausgeführt werden kann.

## Reihenfolge der Bereitstellung von MBAM-Server Features


Wenn Sie die MBAM-Server Features bereitstellen, installieren Sie die Features in der folgenden Reihenfolge:

1.  Wiederherstellungs-und Hardware Datenbank

2.  Konformitäts-und Überwachungsdatenbank

3.  Konformitätsprüfung und Berichte

4.  Verwaltungs-und Überwachungs Server

5.  Richtlinienvorlage

**Hinweis**  Verfolgen Sie die Namen der Computer, auf denen Sie die einzelnen Features installieren. Sie werden diese Informationen während des Installationsvorgangs verwenden. Sie können eine Bereitstellungscheckliste drucken und verwenden, um Sie beim Installationsvorgang zu unterstützen. Weitere Informationen zur MBAM-Bereitstellungscheckliste finden Sie unter [MBAM 1,0 Deployment Checkliste](mbam-10-deployment-checklist.md).

 

## Verwandte Themen


[Planen der Bereitstellung von MBAM 1.0](planning-to-deploy-mbam-10.md)

[Bereitstellen der Serverinfrastruktur von MBAM 1.0](deploying-the-mbam-10-server-infrastructure.md)

 

 





