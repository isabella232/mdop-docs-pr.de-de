---
title: Planen der Serverbereitstellung für MBAM 2.0
description: Planen der Serverbereitstellung für MBAM 2.0
author: dansimp
ms.assetid: b57f1a42-134f-4997-8697-7fbed08e2fc4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57e6510556522dce029c958172bd89a361e06b83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804358"
---
# Planen der Serverbereitstellung für MBAM 2.0


Die Microsoft BitLocker-Serverinfrastruktur für die Verwaltungs-und Überwachungsdienste (MBAM) hängt von einer Reihe von Server Features ab, die basierend auf den Anforderungen des Unternehmens auf einem oder mehreren Server Computern installiert werden können. Wenn Sie die Microsoft BitLocker-Verwaltung und-Überwachung mit der Configuration Manager-Topologie installieren, lesen Sie [Planen der Bereitstellung von MBAM mit Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).

**Hinweis**  Installationen der Microsoft BitLocker-Verwaltung und-Überwachung auf einem einzelnen Server werden nur für Testumgebungen empfohlen.

 

## Planen der Bereitstellung von MBAM Server


Die Infrastruktur für eine MBAM-Server Bereitstellung umfasst die folgenden Features:

-   Wiederherstellungsdatenbank

-   Konformitäts-und Überwachungsdatenbank

-   Konformitäts-und Überwachungsberichte

-   Self-Service-Portal

-   Verwaltungs-und Überwachungs Server

-   MBAM-Gruppenrichtlinienvorlage

MBAM Server-Datenbanken und-Features können je nach Ihren Skalierbarkeitsanforderungen in unterschiedlichen Konfigurationen installiert werden. Alle MBAM-Server Features können auf einem einzelnen Server installiert oder auf mehrere Server verteilt werden. Es wird empfohlen, eine Konfiguration mit zwei Servern für Produktionsumgebungen zu verwenden, wobei je nach Ihren Computeranforderungen auch Konfigurationen von zwei bis vier Servern verwendet werden können.

Jedes MBAM-Feature hat bestimmte Voraussetzungen. Eine vollständige Liste der Voraussetzungen und Hardware-und Softwareanforderungen für Server Features finden Sie unter [MBAM 2,0-Bereitstellungsvoraussetzungen](mbam-20-deployment-prerequisites-mbam-2.md) und [unterstützte MBAM 2,0-Konfigurationen](mbam-20-supported-configurations-mbam-2.md).

Zusätzlich zu den serverbezogenen MBAM-Features umfasst die Server-Setup Anwendung eine MBAM-Gruppenrichtlinienvorlage. Die Vorlage enthält Gruppenrichtlinienobjekt-Einstellungen, die Sie konfigurieren, um die BitLocker-Laufwerkverschlüsselung im Unternehmen zu verwalten. Sie können diese Vorlage auf jedem Computer installieren, auf dem die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ausgeführt werden kann.

Wenn Sie die MBAM-Server Bereitstellung planen, sollten Sie Bedenken, dass die BitLocker-Wiederherstellungsschlüssel in MBAM nur zur einmaligen Verwendung vorgesehen sind, nachdem die Wiederherstellungsschlüssel ablaufen. Damit die Schlüssel nach der Verwendung ablaufen, müssen Sie über das Helpdesk-Portal oder das Self-Service-Portal abgerufen werden.

## Reihenfolge der Bereitstellung von MBAM-Server Features


Zum Bereitstellen von MBAM-Features auf mehreren Servern müssen Sie die Features in der folgenden Reihenfolge installieren:

1.  Wiederherstellungsdatenbank

2.  Konformitäts-und Überwachungsdatenbank

3.  Konformitätsprüfung und Berichte

4.  Self-Service-Portal

5.  Verwaltungs-und Überwachungs Server

6.  MBAM-Gruppenrichtlinienvorlage

**Hinweis**  Verfolgen Sie die Namen der Computer, auf denen Sie die einzelnen Features installieren. Sie müssen diese Informationen während des Installationsvorgangs verwenden. Sie können eine Bereitstellungscheckliste drucken und verwenden, um diesen Aufwand zu unterstützen. Weitere Informationen zur MBAM-Bereitstellungscheckliste finden Sie unter [MBAM 2,0 Deployment Checkliste](mbam-20-deployment-checklist-mbam-2.md).

 

## Verwandte Themen


[Planen der Bereitstellung von MBAM 2.0](planning-to-deploy-mbam-20-mbam-2.md)

[Bereitstellen der Serverinfrastruktur von MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





