---
title: So verwalten Sie BitLocker-Verschlüsselungsoptionen für MBAM-Clients mithilfe der Systemsteuerung
description: So verwalten Sie BitLocker-Verschlüsselungsoptionen für MBAM-Clients mithilfe der Systemsteuerung
author: dansimp
ms.assetid: e2ff153e-5770-4a12-b79d-cda998b8a8ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a42901ac9d8a1a3527712f4cf342b5c0ca9ffdfd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810957"
---
# So verwalten Sie BitLocker-Verschlüsselungsoptionen für MBAM-Clients mithilfe der Systemsteuerung


Eine Microsoft BitLocker-Verwaltungs-und Überwachungsanwendung (MBAM), die so genannten BitLocker-Verschlüsselungsoptionen, wird unter **System und Sicherheit** verfügbar sein, wenn der Microsoft BitLocker-Verwaltungs-und-Überwachungs Client installiert ist. Dieses benutzerdefinierte MBAM Control Panel ist ein zusätzliches Control Panel. Die standardmäßige Windows BitLocker-Systemsteuerung wird nicht ersetzt. Über das MBAM-Control Panel können verschlüsselte fest-und Wechseldatenträger freigegeben und auch Ihre PIN oder Ihr Kennwort verwaltet werden. Weitere Informationen zum Aktivieren der MBAM-Systemsteuerung finden Sie unter [Ausblenden der BitLocker-Standardverschlüsselung in der Windows-System](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md)Steuerung.

**So verwenden Sie die MBAM-Client-Systemsteuerung**

1.  Klicken Sie zum Öffnen der BitLocker-Verschlüsselungsoptionen auf **Start** und dann auf **System**Steuerung. Wenn **die Systemsteuerung geöffnet** wird, wählen Sie **System und Sicherheit**aus.

2.  Doppelklicken Sie auf **BitLocker-Verschlüsselungsoptionen** , um die angepasste MBAM-Systemsteuerung zu öffnen. Es wird eine Liste aller Festplatten auf dem Computer und deren Verschlüsselungsstatus sowie eine Option zum Verwalten Ihrer PIN oder Kennwörter angezeigt.

    Die Liste der Festplattenlaufwerke auf dem Computer kann zum Überprüfen des Verschlüsselungsstatus, Entsperren eines Laufwerks oder zum Anfordern einer Ausnahme für den BitLocker-Schutz verwendet werden, wenn die Ausnahmerichtlinien für Benutzer und Computer bereitgestellt wurden.

    Mit der Systemsteuerung für BitLocker-Verschlüsselungsoptionen können auch Benutzer ohne Administratorrechte Ihre PIN oder Kennwörter verwalten. Durch Auswahl von " **Pin verwalten**" werden die Benutzer aufgefordert, sowohl eine aktuelle PIN als auch eine neue PIN einzugeben (zusätzlich zur Bestätigung der neuen PIN). Wenn Sie die Option " **Pin aktualisieren** " auswählen, wird die PIN auf das neue Kennwort zurückgesetzt, das die Benutzer ausgewählt haben.

    Wenn Sie Ihr Kennwort verwalten möchten, wählen Sie **Laufwerk entsperren** und geben Sie Ihr aktuelles Kennwort ein. Sobald das Laufwerk entriegelt ist, wählen Sie **Kennwort zurücksetzen** aus, um Ihr aktuelles Kennwort zu ändern.

## Verwandte Themen


[Verwalten von MBAM 2.0-Funktionen](administering-mbam-20-features-mbam-2.md)

 

 





