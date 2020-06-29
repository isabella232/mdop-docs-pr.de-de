---
title: So installieren Sie die Gruppenrichtlinienvorlage für MBAM 2.0
description: So installieren Sie die Gruppenrichtlinienvorlage für MBAM 2.0
author: dansimp
ms.assetid: bc193232-d060-4285-842e-d194a74dd3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6420fc4d499de05ed740b038b40aff6a9cd8a05f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811644"
---
# So installieren Sie die Gruppenrichtlinienvorlage für MBAM 2.0


Zusätzlich zu den serverbezogenen Features für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) umfasst die Server Setupanwendung eine Microsoft BitLocker-Verwaltungs-und-Überwachungsgruppen Richtlinienvorlage. Diese Vorlage kann auf jedem Computer installiert werden, der die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ausführt.

In den folgenden Schritten wird beschrieben, wie die MBAM-Gruppenrichtlinienvorlage installiert wird.

**Hinweis**  Stellen Sie sicher, dass Sie das 32-Bit-Setup auf 32-Bit-Servern und das 64-Bit-Setup auf 64-Bit-Servern verwenden.

 

**So installieren Sie die MBAM-Gruppenrichtlinienvorlage**

1.  Führen Sie auf dem Server, auf dem Sie MBAM installieren möchten, **MBAMSetup.exe** aus, um den MBAM-Installations-Assistenten zu starten.

2.  Wählen Sie auf der **Willkommens** Seite optional das **Programm zur Verbesserung der Benutzerfreundlichkeit**aus, und klicken Sie dann auf **Start**.

3.  Lesen und akzeptieren Sie die Microsoft-Software-Lizenzbestimmungen, und klicken Sie auf **weiter** , um die Installation fortzusetzen.

4.  Standardmäßig sind alle Microsoft BitLocker-Verwaltungs-und Überwachungsfeatures für die Installation ausgewählt. Deaktivieren Sie alle Feature-Optionen mit Ausnahme der **Richtlinienvorlage**, und klicken Sie auf **weiter** , um die Installation fortzusetzen.

    **Hinweis**  Der Installations-Assistent überprüft die Voraussetzungen für die Installation und zeigt die fehlenden Voraussetzungen an. Wenn alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt. Wenn eine fehlende Voraussetzung erkannt wird, müssen Sie die fehlenden Voraussetzungen beheben und dann **erneut auf Voraussetzungen prüfen**klicken. Sobald alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.

     

5.  Detaillierte Informationen dazu, wie und wo Sie die Vorlagen installieren, finden Sie unter [herunterladen und Bereitstellen von MDOP-Gruppenrichtlinien-Vorlagen (ADMX)](https://technet.microsoft.com/library/dn659707.aspx).

6.  Klicken Sie nach dem Setup-Assistenten für Microsoft BitLocker-Verwaltung und-Überwachung auf Installationsseiten für die ausgewählten Features, und klicken Sie auf **Fertig stellen** , um das MBAM-Setup zu schließen

## Verwandte Themen


[Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.0](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 





