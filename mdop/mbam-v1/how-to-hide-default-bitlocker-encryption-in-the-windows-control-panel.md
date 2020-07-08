---
title: So blenden Sie die standardmäßige BitLocker-Verschlüsselung in der Windows-Systemsteuerung aus
description: So blenden Sie die standardmäßige BitLocker-Verschlüsselung in der Windows-Systemsteuerung aus
author: dansimp
ms.assetid: c8503743-220c-497c-9785-e2feeca484d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67a61763e556f8c3b93825220dbbd61a14b7d6f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810597"
---
# So blenden Sie die standardmäßige BitLocker-Verschlüsselung in der Windows-Systemsteuerung aus


Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) bietet ein angepasstes Control Panel für MBAM-Clientcomputer mit dem Namen "BitLocker-Verschlüsselungsoptionen". Dieses angepasste Control Panel kann die standardmäßige Windows BitLocker-Systemsteuerung mit dem Namen BitLocker Drive Encryption ersetzen. Mit der Systemsteuerung für BitLocker-Verschlüsselungsoptionen, die sich unter System und Sicherheit in der Windows-Systemsteuerung befindet, können Benutzer Ihre PIN und Kennwörter verwalten, Laufwerke entsperren und die Oberfläche ausblenden, mit der Administratoren ein Laufwerk entschlüsseln oder die BitLocker-Verschlüsselung anhalten oder fortsetzen können.

**So blenden Sie die BitLocker-Standardverschlüsselung in der Windows-Systemsteuerung aus**

1.  Navigieren Sie mithilfe der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC), der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) oder des Editors für lokale Gruppenrichtlinien auf dem BitLocker-Gruppenrichtlinien Computer zu **Benutzerkonfiguration** .

2.  Klicken Sie auf **Richtlinien**, wählen Sie **Administrative Vorlagen**aus, und klicken Sie dann auf **System**Steuerung.

3.  Doppelklicken Sie im **Detail** Bereich auf **angegebene Control Panel-Elemente ausblenden**, und wählen Sie dann **aktiviert**aus.

4.  Klicken Sie auf **anzeigen**, **Klicken Sie auf hinzufügen...**, und geben Sie dann Microsoft. BitLockerDriveEncryption ein. Mit dieser Richtlinie wird das standardmäßige Windows BitLocker-Verwaltungstool aus der Windows-Systemsteuerung ausgeblendet, und der Benutzer kann das aktualisierte MBAM BitLocker-Verschlüsselungsoptionen Tool in der Windows-Systemsteuerung öffnen.

## Verwandte Themen


[Bereitstellen von Gruppenrichtlinienobjekten für MBAM 1.0](deploying-mbam-10-group-policy-objects.md)

 

 





