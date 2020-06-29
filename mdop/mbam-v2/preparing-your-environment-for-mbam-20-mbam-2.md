---
title: Vorbereiten der Umgebung für MBAM 2.0
description: Vorbereiten der Umgebung für MBAM 2.0
author: dansimp
ms.assetid: 5fb01da9-620e-4992-9e54-2ed3fb69e6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f1be989112d456064db302952d50159d00b5597a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811257"
---
# Vorbereiten der Umgebung für MBAM 2.0


Bevor Sie mit der Einrichtung von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) beginnen, sollten Sie sicherstellen, dass Sie die Voraussetzungen für die Installation des Produkts erfüllt haben. Wenn Sie wissen, welche Voraussetzungen Voraussetzungen sind, können Sie das Produkt effizient bereitstellen und seine Features aktivieren, damit es die geschäftlichen Ziele Ihrer Organisation am effektivsten unterstützt.

Wenn Sie die Microsoft BitLocker-Verwaltung und-Überwachung mit Microsoft System Center Configuration Manager 2007 oder MicrosoftSystemCenter2012 ConfigurationManager bereitstellen, lesen Sie [Planen der Bereitstellung von MBAM mit Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).

## Überprüfen der MBAM 2,0-Bereitstellungsvoraussetzungen


Der MBAM-Client und alle MBAM-Server Features verfügen über bestimmte Voraussetzungen, die erfüllt sein müssen, bevor Sie erfolgreich installiert werden können.

Um eine erfolgreiche Installation von MBAM-Clients und MBAM-Server Features sicherzustellen, müssen Sie sicherstellen, dass die für die Installation von MBAM Client-oder MBAM-Servern angegebenen Computer ordnungsgemäß für die MBAM Einrichtung vorbereitet sind

**Hinweis**  MBAM-Setup überprüft, ob alle Voraussetzungen erfüllt sind, bevor die Installation gestartet wird. Wenn alle Voraussetzungen nicht erfüllt sind, schlägt Setup fehl.

 

[Bereitstellungsvoraussetzungen für MBAM 2.0](mbam-20-deployment-prerequisites-mbam-2.md)

## Planen der MBAM 2,0-Gruppenrichtlinienanforderungen


Bevor MBAM Clients im Unternehmen verwalten kann, müssen Sie Gruppenrichtlinien für die Verschlüsselungsanforderungen Ihrer Umgebung definieren.

**Wichtig**  MBAM wird nicht mit Richtlinien für eigenständige BitLocker-Laufwerkverschlüsselung funktionieren. Für MBAM müssen Gruppenrichtlinieneinstellungen definiert sein, oder die BitLocker-Verschlüsselung und-Erzwingung schlägt fehl.

 

[Planen der Gruppenrichtlinienanforderungen für MBAM 2.0](planning-for-mbam-20-group-policy-requirements-mbam-2.md)

## Planen von MBAM 2,0-Administrator Rollen


MBAM-Administratorrollen werden von lokalen Gruppen verwaltet, die von MBAM Setup beim Installieren des BitLocker-Verwaltungs-und Überwachungsservers, des Features Konformitäts-und Überwachungsberichte sowie der Kompatibilitäts-und Überwachungs Status Datenbank erstellt werden.

Die Mitgliedschaft in den Microsoft BitLocker-Verwaltungs-und Überwachungs Rollen kann am besten durch Erstellen von Sicherheitsgruppen in ActiveDirectoryDomainServices, Hinzufügen der entsprechenden Administratorkonten zu diesen Gruppen und anschließendes Hinzufügen dieser Sicherheitsgruppen zur BitLocker-Verwaltung und zum Überwachen lokaler Gruppen verwaltet werden. Weitere Informationen finden Sie unter [Verwalten von MBAM-Administrator Rollen](how-to-manage-mbam-administrator-roles-mbam-2.md).

## Weitere Ressourcen für die Planung von MBAM


[Planen von MBAM 2.0](planning-for-mbam-20-mbam-2.md)

[Von MBAM 2.0 unterstützte Konfigurationen](mbam-20-supported-configurations-mbam-2.md)

 

 





