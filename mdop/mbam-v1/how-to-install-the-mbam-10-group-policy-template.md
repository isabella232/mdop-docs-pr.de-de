---
title: So installieren Sie die Gruppenrichtlinienvorlage für MBAM 1.0
description: So installieren Sie die Gruppenrichtlinienvorlage für MBAM 1.0
author: dansimp
ms.assetid: 451a50b0-939c-47ad-9248-a138deade550
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a055c84fb6b1645592b53d957daf157a6055880
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811095"
---
# So installieren Sie die Gruppenrichtlinienvorlage für MBAM 1.0


Zusätzlich zu den serverbezogenen Features der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) enthält die Server Setupanwendung eine MBAM-Gruppenrichtlinienvorlage. Sie können diese Vorlage auf jedem Computer installieren, auf dem die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ausgeführt werden kann.

In den folgenden Schritten wird beschrieben, wie die MBAM-Gruppenrichtlinienvorlage installiert wird.

**Hinweis**  Stellen Sie sicher, dass Sie das 32-Bit-Setup auf 32-Bit-Servern und das 64-Bit-Setup auf 64-Bit-Servern verwenden.

 

**So installieren Sie die MBAM-Gruppenrichtlinienvorlage**

1.  Starten Sie den MBAM-Installations-Assistenten. Klicken Sie dann auf der Seite Willkommen auf **Installieren** .

2.  Lesen und akzeptieren Sie die Microsoft-Software-Lizenzbestimmungen, und klicken Sie auf **weiter** , um die Installation fortzusetzen.

3.  Standardmäßig sind alle MBAM-Features für die Installation ausgewählt. Deaktivieren Sie alle Feature-Optionen mit Ausnahme der **Richtlinienvorlage**, und klicken Sie auf **weiter** , um die Installation fortzusetzen.

    **Hinweis**  Der Installations-Assistent überprüft die Voraussetzungen für die Installation und zeigt die fehlenden Voraussetzungen an. Wenn alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt. Wenn eine fehlende Voraussetzung erkannt wird, müssen Sie die fehlende Voraussetzungen beheben und dann **erneut auf Voraussetzungen prüfen**klicken. Sobald alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.

     

4.  Nachdem der MBAM-Setup-Assistent Installationsseiten für die ausgewählten Features angezeigt hat, klicken Sie auf **Fertig stellen** , um das MBAM-Setup zu schließen.

## Verwandte Themen


[Bereitstellen von Gruppenrichtlinienobjekten für MBAM 1.0](deploying-mbam-10-group-policy-objects.md)

 

 





