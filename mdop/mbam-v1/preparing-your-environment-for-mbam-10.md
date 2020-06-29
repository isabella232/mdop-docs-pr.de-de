---
title: Vorbereiten der Umgebung für MBAM 1.0
description: Vorbereiten der Umgebung für MBAM 1.0
author: dansimp
ms.assetid: 915f7c3c-70ad-4a90-a434-73e7fba97ecb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a2de4e825d5c89aeabcf57d78dc856bacb03e11
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809808"
---
# Vorbereiten der Umgebung für MBAM 1.0


Bevor Sie mit dem Setup für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) beginnen, stellen Sie sicher, dass Sie die erforderlichen Voraussetzungen für die Installation des Produkts erfüllt haben. Wenn Sie die Voraussetzungen im Voraus kennen, können Sie das Produkt effizient bereitstellen und seine Features aktivieren, die die geschäftlichen Ziele Ihrer Organisation effektiver unterstützen können.

## Überprüfen der MBAM 1,0-Bereitstellungsvoraussetzungen


Der MBAM-Client und alle MBAM-Server Features verfügen über bestimmte Voraussetzungen, die erfüllt sein müssen, bevor Sie erfolgreich installiert werden können.

Um eine erfolgreiche Installation von MBAM-Clients und MBAM-Server Features zu gewährleisten, sollten Sie sicherstellen, dass Computer, die für die Installation von MBAM Client oder MBAM Server festgelegt wurden, ordnungsgemäß für MBAM Setup vorbereitet sind.

**Hinweis**  MBAM-Setup überprüft, ob alle Voraussetzungen erfüllt sind, bevor die Installation gestartet wird. Wenn Sie nicht erfüllt sind, schlägt Setup fehl.

 

[Bereitstellungsvoraussetzungen für MBAM 1.0](mbam-10-deployment-prerequisites.md)

## Planen der MBAM 1,0-Gruppenrichtlinienanforderungen


Bevor MBAM Clients im Unternehmen verwalten kann, müssen Sie die Gruppenrichtlinie für die Verschlüsselungsanforderungen Ihrer Umgebung definieren.

**Wichtig**  MBAM wird nicht mit Richtlinien für eigenständige BitLocker-Laufwerkverschlüsselung funktionieren. Für MBAM muss eine Gruppenrichtlinie definiert werden. Andernfalls treten bei der BitLocker-Verschlüsselung und-Erzwingung Fehler auf.

 

[Planen der Gruppenrichtlinienanforderungen für MBAM 1.0](planning-for-mbam-10-group-policy-requirements.md)

## Planen von MBAM 1,0-Administratorrollen


MBAM-Administratorrollen werden von lokalen Gruppen verwaltet, die von MBAM Setup erstellt werden, wenn Sie Folgendes installieren: BitLocker-Verwaltungs-und Überwachungs Server, das Feature Konformitäts-und Überwachungsberichte sowie die Datenbank für Konformitäts-und Überwachungs Status.

Die Mitgliedschaft in MBAM-Rollen kann effektiver verwaltet werden, wenn Sie in ActiveDirectoryDomainServices Sicherheitsgruppen erstellen, diesen Gruppen die entsprechenden Administratorkonten hinzufügen und diese Sicherheitsgruppen dann den lokalen MBAM-Gruppen hinzufügen. Weitere Informationen finden Sie unter [Verwalten von MBAM-Administrator Rollen](how-to-manage-mbam-administrator-roles-mbam-1.md).

[Planen der Administratorrollen für MBAM 1.0](planning-for-mbam-10-administrator-roles.md)

## Weitere Ressourcen für die Planung von MBAM


[Planen von MBAM 1.0](planning-for-mbam-10.md)

 

 





