---
title: Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.0
description: Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.0
author: dansimp
ms.assetid: f17f3897-73ab-431b-a6ec-5a6cff9f279a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1ce2c2a37631d9d678d6de7c1d66b7fdafb2ade9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809988"
---
# Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.0


Zur erfolgreichen Bereitstellung von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) müssen Sie zunächst die Gruppenrichtlinien ermitteln, die Sie bei der Implementierung der Microsoft BitLocker-Verwaltung und-Überwachung verwenden werden. Weitere Informationen zu den verschiedenen verfügbaren Richtlinien finden Sie unter [Planen von MBAM 2,0-Gruppenrichtlinienanforderungen](planning-for-mbam-20-group-policy-requirements-mbam-2.md) . Nachdem Sie die Richtlinien festgelegt haben, die Sie verwenden möchten, müssen Sie ein oder mehrere Gruppenrichtlinienobjekte (Group Policy Objects, GPO) erstellen und bereitstellen, die die Richtlinieneinstellungen für MBAM enthalten, indem Sie die MBAM 2,0-Gruppenrichtlinienvorlage verwenden.

## Installieren der MBAM 2,0-Gruppenrichtlinienvorlage


Zusätzlich zu den serverbezogenen Microsoft BitLocker-Verwaltungs-und-Überwachungsfeatures umfasst die Server Setupanwendung eine MBAM-Gruppenrichtlinienvorlage. Diese Vorlage kann auf jedem Computer installiert werden, in dem die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ausgeführt werden kann.

[So installieren Sie die Gruppenrichtlinienvorlage für MBAM 2.0](how-to-install-the-mbam-20-group-policy-template-mbam-2.md)

## Bereitstellen von MBAM 2,0-Gruppenrichtlinieneinstellungen


Nachdem Sie die erforderlichen GPOs erstellt haben, müssen Sie die MBAM-Gruppenrichtlinieneinstellungen auf den Clientcomputern Ihrer Organisation bereitstellen.

[So bearbeiten Sie GPO-Einstellungen für MBAM 2.0](how-to-edit-mbam-20-gpo-settings-mbam-2.md)

## Anzeigen der MBAM-Systemsteuerung in Windows


Da MBAM ein angepasstes MBAM-Control Panel bietet, das die standardmäßige Windows BitLocker-Systemsteuerung ersetzen kann, können Sie auch die standardmäßige BitLocker-Systemsteuerung von Endbenutzern mithilfe von Gruppenrichtlinien ausblenden.

[So blenden Sie die standardmäßige BitLocker-Verschlüsselung in der Windows-Systemsteuerung aus](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md)

## Weitere Ressourcen für die Bereitstellung von MBAM 2,0-Gruppenrichtlinienobjekten


[Bereitstellen von MBAM 2.0](deploying-mbam-20-mbam-2.md)

 

 





