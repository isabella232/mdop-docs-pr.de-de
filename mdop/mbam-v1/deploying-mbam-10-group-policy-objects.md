---
title: Bereitstellen von Gruppenrichtlinienobjekten für MBAM 1.0
description: Bereitstellen von Gruppenrichtlinienobjekten für MBAM 1.0
author: dansimp
ms.assetid: 2129291e-d2b2-41ed-b643-1e311c49fee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d14123f1d5b197146e425cba063e8ce4c180641
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808623"
---
# Bereitstellen von Gruppenrichtlinienobjekten für MBAM 1.0


Wenn Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) erfolgreich bereitstellen möchten, müssen Sie zuerst die Gruppenrichtlinien ermitteln, die Sie bei der Implementierung von MBAM verwenden werden. Weitere Informationen zu den verschiedenen verfügbaren Richtlinien finden Sie unter [Planen von MBAM 1,0-Gruppenrichtlinienanforderungen](planning-for-mbam-10-group-policy-requirements.md). Wenn Sie die Richtlinien festgelegt haben, die Sie verwenden möchten, müssen Sie die MBAM 1,0-Gruppenrichtlinienvorlage verwenden, um ein oder mehrere Gruppenrichtlinienobjekte zu erstellen und bereitzustellen, die die MBAM-Richtlinieneinstellungen enthalten.

## Installieren der MBAM 1,0-Gruppenrichtlinienvorlage


Zusätzlich zum Bereitstellen von serverbezogenen Features von MBAM umfasst die Server Setupanwendung eine MBAM-Gruppenrichtlinienvorlage. Sie können diese Vorlage auf jedem Computer installieren, auf dem die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ausgeführt werden kann.

[So installieren Sie die Gruppenrichtlinienvorlage für MBAM 1.0](how-to-install-the-mbam-10-group-policy-template.md)

## Bereitstellen von MBAM 1,0-Gruppenrichtlinieneinstellungen


Nachdem Sie die erforderlichen GPOs erstellt haben, müssen Sie die MBAM-Gruppenrichtlinieneinstellungen auf den Clientcomputern Ihrer Organisation bereitstellen.

[So bearbeiten Sie die GPO-Einstellungen für MBAM 1.0](how-to-edit-mbam-10-gpo-settings.md)

## Anzeigen der MBAM-Systemsteuerung in Windows


Da MBAM ein angepasstes MBAM-Control Panel bietet, das die standardmäßige Windows BitLocker-Systemsteuerung ersetzen kann, können Sie auch die standardmäßige BitLocker-Systemsteuerung von Endbenutzern mithilfe von Gruppenrichtlinien ausblenden.

[So blenden Sie die standardmäßige BitLocker-Verschlüsselung in der Windows-Systemsteuerung aus](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md)

## Weitere Ressourcen für die Bereitstellung von MBAM 1,0-Gruppenrichtlinienobjekten


[Bereitstellen von MBAM 1.0](deploying-mbam-10.md)

 

 





