---
title: Ausblenden der Standard-BitLocker-Laufwerkverschlüsselung in der Windows-Systemsteuerung
description: Ausblenden der Standard-BitLocker-Laufwerkverschlüsselung in der Windows-Systemsteuerung
author: dansimp
ms.assetid: 6e2a9a02-a809-43a1-80a3-1b03c7192c89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af395928ca8934bfea4eeb848bbd4ee377987293
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809751"
---
# Ausblenden der Standard-BitLocker-Laufwerkverschlüsselung in der Windows-Systemsteuerung


In diesem Thema wird beschrieben, wie Sie das Control Panel-Element für die **BitLocker-Laufwerkverschlüsselung** ausblenden, das standardmäßig in der Systemsteuerung als Teil des Windows-Betriebssystems angezeigt wird.

**Hinweis**  Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) erstellt ein zusätzliches, benutzerdefiniertes Control Panel-Element mit dem Namen **BitLocker-Verschlüsselungsoptionen**, mit dem Endbenutzer Ihre PIN und Ihr Kennwort verwalten, BitLocker für ein Laufwerk aktivieren und die Verschlüsselung überprüfen können.

 

Weitere Informationen finden Sie unter [Grundlegendes zu den BitLocker-Verschlüsselungsoptionen und Elementen der BitLocker-Laufwerkverschlüsselung in der System](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md) Steuerung:

-   Unterschiede zwischen der MBAM und den Standardelementen der Systemsteuerung

-   Kontextmenü " **BitLocker verwalten** ", das angezeigt wird, wenn Sie in Windows-Explorer mit der rechten Maustaste auf ein Laufwerk klicken

**Wichtig**  Ändern Sie nicht die Gruppenrichtlinieneinstellungen im **BitLocker Drive Encryption** -Knoten. In diesem Fall funktioniert MBAM nicht ordnungsgemäß. Wenn Sie die Gruppenrichtlinieneinstellungen im MDOP- **MBAM (BitLocker-Verwaltungsknoten)** konfigurieren, konfiguriert MBAM automatisch die **BitLocker-Laufwerk Verschlüsselungs** Einstellungen für Sie.

 

**So blenden Sie das standardmäßige BitLocker-Laufwerk Verschlüsselungselement in der Systemsteuerung aus**

1.  Navigieren Sie in der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder in der erweiterten Gruppenrichtlinienverwaltung zu **Benutzer Konfigurations** &gt; **Richtlinien** für &gt; **Administrative Vorlagen** in der &gt; **System**Steuerung.

2.  Doppelklicken Sie im **Detail** Bereich auf **angegebene Control Panel-Elemente ausblenden**, und klicken Sie dann auf **aktiviert**.

3.  Klicken Sie auf **anzeigen**, klicken Sie auf **Hinzufügen**, und geben Sie dann **Microsoft. BitLockerDriveEncryption**ein.



## Verwandte Themen


[Grundlegende Informationen zu BitLocker-Verschlüsselungsoptionen und BitLocker-Laufwerkverschlüsselungselementen in der Systemsteuerung](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md)

[Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.5](deploying-mbam-25-group-policy-objects.md)

 

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





