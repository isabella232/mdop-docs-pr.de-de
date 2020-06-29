---
title: So blenden Sie die standardmäßige BitLocker-Verschlüsselung in der Windows-Systemsteuerung aus
description: So blenden Sie die standardmäßige BitLocker-Verschlüsselung in der Windows-Systemsteuerung aus
author: dansimp
ms.assetid: 6674aa51-2b5d-4e4a-8b43-2cc18d008285
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eda8fafbd7b3ebf414520354eba6def2e97f6237
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810342"
---
# So blenden Sie die standardmäßige BitLocker-Verschlüsselung in der Windows-Systemsteuerung aus


Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) bietet ein angepasstes Control Panel für Microsoft BitLocker-Verwaltung und-Überwachung von Clientcomputern, so genannte BitLocker-Verschlüsselungsoptionen. Dieses angepasste Control Panel kann die standardmäßige Windows BitLocker-Systemsteuerung ersetzen, die als BitLocker-Laufwerkverschlüsselung bezeichnet wird. Das angepasste Control Panel, das sich in der Systemsteuerung unter System und Sicherheit befindet, ermöglicht Benutzern, Ihre PIN und Kennwörter zu verwalten sowie Laufwerke zu entsperren, und blendet die Benutzeroberfläche aus, mit der Administratoren ein Laufwerk entschlüsseln oder die BitLocker-Laufwerkverschlüsselung anhalten oder fortsetzen können.

**So blenden Sie die standardmäßige BitLocker-Laufwerkverschlüsselung in der Windows-Systemsteuerung aus**

1.  Navigieren Sie in der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC), der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) oder dem Editor für lokale Gruppenrichtlinien auf dem BitLocker-Computer für Gruppenrichtlinien zur **Benutzerkonfiguration**.

2.  Klicken Sie als nächstes auf **Richtlinien**, wählen Sie **Administrative Vorlagen**aus, und klicken Sie dann auf **System**Steuerung.

3.  Doppelklicken Sie im **Detail** Bereich auf **angegebene Control Panel-Elemente ausblenden** , und wählen Sie dann **aktiviert**aus.

4.  Klicken Sie auf **anzeigen**, klicken Sie auf **Hinzufügen**, und geben Sie dann **Microsoft. BitLockerDriveEncryption**ein. Mit dieser Richtlinie wird das standardmäßige Windows BitLocker-Verwaltungstool aus der Windows-Systemsteuerung ausgeblendet, und der Benutzer kann in der Systemsteuerung das aktualisierte MBAM BitLocker-Verschlüsselungsoptionen-Tool unter System und Sicherheit öffnen.

## Verwandte Themen


[Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.0](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 





