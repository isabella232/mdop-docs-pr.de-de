---
title: Definieren Sie den Projektumfang
description: Definieren Sie den Projektumfang
author: dansimp
ms.assetid: 84637d2a-2e30-417d-b150-dc81f414b3a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4f33562452327bba9036f56d9f6f96650f00c1f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810078"
---
# Definieren Sie den Projektumfang


Legen Sie beim Definieren des Projektumfangs Folgendes fest:

1.  Die Med-v-Endbenutzer – der Speicherort und die Anzahl der Endbenutzer werden verwendet, um den Standort der Med-v-Clientinstallationen und die Anzahl der Med-v-Instanzen sowie die Anzahl und die Platzierung von Med-v-Bild Depots zu ermitteln.

2.  Die VM-Bilder (Virtual Machine), die von MED-V verwaltet werden sollen, um die Methode zum Verteilen von Bildern und zur Platzierung von Bild-Repositories zu ermitteln.

3.  Die Erwartungen des Unternehmens an den Service Level: Ermitteln der Leistungs-und Fehlertoleranzanforderungen für den MED-V-Server und die Datenbank sowie das Bild-Repository.

4.  Überprüfen Sie mit dem Unternehmen – stellen Sie sicher, dass Sie wissen, wie sich die geplante Infrastruktur auf das Unternehmen auswirkt.

## Definieren der MED-V-Endbenutzer


Ermitteln Sie zunächst, wo sich die Endbenutzer befinden, sowie die Anzahl der Benutzer an jedem Standort. Rufen Sie als nächstes ein Netzwerkinfrastruktur Diagramm ab, in dem die Benutzerspeicherorte und die verfügbare Bandbreite an diesen Speicherorten angezeigt werden. Drittens: finden Sie heraus, ob Benutzerzwischenspeicher Orten reisen. Wenn Benutzer Reisen, ist möglicherweise zusätzliche Kapazität beim Entwurf der Serverinfrastruktur und der Bild Depots erforderlich.

## Ermitteln der Med-v-Bilder, die von Med-v verwaltet werden sollen


Nachdem die Med-v-Endbenutzer definiert wurden, ermitteln Sie, welche VMS von Med-v für die Benutzer an den einzelnen Speicherorten verwaltet werden.

Wenn eines der VMs in einer zentralisierten Bibliothek gespeichert ist, ermitteln Sie den Speicherort der Bibliothek, damit Sie für die Verwendung als MED-V-Repository ausgewertet werden kann.

## <a href="" id="determine-the-organization-s-service-level-expectations"></a>Ermitteln der Service-Level-Erwartungen des Unternehmens


Notieren Sie sich für jeden MED-V-Arbeitsbereich die akzeptable Zeit, zu der ein neues Bild geladen werden soll, und den Zeitrahmen für die Bereitstellung kritischer Updates.

Notieren Sie sich ggf. die Erwartungen des Service Levels für MED-V-Berichte, die beim Entwurf der Serverinfrastruktur zu verwenden sind.

## Überprüfen mit dem Unternehmen


Bitten Sie Unternehmen und Anwendungsbesitzer, die folgenden Fragen zu beantworten:

-   Gibt es vorhandene Bilder, die kombiniert werden können? Wenn beispielsweise die Anwendung a unter WindowsXP ein VPC-Bild und die Anwendung B unter WindowsXP ein weiteres VPC-Abbild ist, kann ein einzelnes Bild möglicherweise beide Anwendungen enthalten und dadurch den Speicherplatz und die Bandbreite reduzieren, die für den Download von Bildern erforderlich sind.

-   Sind die in-Scope-Anwendungen lizenziert und unterstützt, wenn Sie von MED-V in einem VM bereitgestellt werden? Wenden Sie sich an den Anbieter der Anwendung, um sicherzustellen, dass die Lizenz-und Support Bestimmungen nicht verletzt werden, indem Sie die Anwendung über MED-V bereitstellen.

 

 





