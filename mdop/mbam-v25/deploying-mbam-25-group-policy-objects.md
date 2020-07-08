---
title: Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.5
description: Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.5
author: dansimp
ms.assetid: 4b835054-6846-463d-af58-8ac4639a1188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9624b94e9d4808a35e1199290f4cd90a8122f767
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810525"
---
# Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.5


Zum Bereitstellen von MBAM müssen Sie Gruppenrichtlinieneinstellungen festlegen, die MBAM-Implementierungs Einstellungen für die BitLocker-Laufwerkverschlüsselung definieren. Zum Ausführen dieser Aufgabe müssen Sie die MBAM-Gruppenrichtlinienvorlagen auf einen Server oder eine Workstation kopieren, die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ausführen können, und dann die Einstellungen bearbeiten.

**Wichtig**  Ändern Sie die Gruppenrichtlinieneinstellungen im **BitLocker Drive Encryption** -Knoten nicht, oder MBAM wird nicht ordnungsgemäß funktionieren. Wenn Sie die Gruppenrichtlinieneinstellungen im MDOP- **MBAM (BitLocker-Verwaltungsknoten)** konfigurieren, konfiguriert MBAM automatisch die **BitLocker-Laufwerk Verschlüsselungs** Einstellungen für Sie.

 

## Kopieren die Gruppenrichtlinienvorlagen für MBAM 2.5


Bevor Sie den MBAM-Client installieren, müssen Sie MBAM-spezifische Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) auf die Verwaltungsarbeitsstation kopieren. Diese GPOs definieren MBAM-Implementierungs Einstellungen für die BitLocker-Laufwerkverschlüsselung. Sie können die Gruppenrichtlinienvorlagen auf alle Server oder Workstations kopieren, die ein unterstützter Windows-Server oder-Clientcomputer sind und die in der Lage sind, die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) auszuführen.

[Kopieren die Gruppenrichtlinienvorlagen für MBAM 2.5](copying-the-mbam-25-group-policy-templates.md)

## Bearbeiten von MBAM 2,0-GPO-Einstellungen


Nachdem Sie die erforderlichen GPOs erstellt haben, müssen Sie die MBAM-Gruppenrichtlinieneinstellungen auf den Clientcomputern Ihrer Organisation bereitstellen. Um GPOs anzuzeigen und zu erstellen, müssen Sie die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder eine erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) installiert haben.

[Bearbeiten der Gruppenrichtlinieneinstellungen für MBAM 2.5](editing-the-mbam-25-group-policy-settings.md)

## Anzeigen oder Ausblenden der MBAM-Systemsteuerung in der Windows-Systemsteuerung


Da MBAM ein angepasstes MBAM-Control Panel bietet, das die standardmäßige Windows BitLocker-Systemsteuerung ersetzen kann, können Sie auch die standardmäßige BitLocker-Systemsteuerung von Endbenutzern mithilfe von Gruppenrichtlinieneinstellungen anzeigen oder ausblenden.

[Ausblenden der Standard-BitLocker-Laufwerkverschlüsselung in der Windows-Systemsteuerung](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)

## Weitere Ressourcen für die Bereitstellung von MBAM 2,0-Gruppenrichtlinienobjekten


[Bereitstellen von MBAM 2.5](deploying-mbam-25.md)

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).

 

 





