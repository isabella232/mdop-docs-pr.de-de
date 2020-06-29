---
title: So verwalten Sie BitLocker-Verschlüsselungsoptionen für MBAM-Clients mithilfe der Systemsteuerung
description: So verwalten Sie BitLocker-Verschlüsselungsoptionen für MBAM-Clients mithilfe der Systemsteuerung
author: dansimp
ms.assetid: c08077e1-5529-468f-9370-c3b33fc258f3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 271147d0e5581f6ce49fe0b46aa83dae6ae4556b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804616"
---
# So verwalten Sie BitLocker-Verschlüsselungsoptionen für MBAM-Clients mithilfe der Systemsteuerung


Eine Microsoft BitLocker-Verwaltungs-und Überwachungsanwendung (MBAM), die so genannten BitLocker-Verschlüsselungsoptionen, ist unter **System und Sicherheit** verfügbar, wenn der MBAM-Client installiert ist. Diese angepasste MBAM-Systemsteuerung ersetzt die standardmäßige Windows BitLocker-Systemsteuerung. Das MBAM Control Panel ermöglicht Ihnen, verschlüsselte Laufwerke (behoben und abnehmbar) zu entsperren, und hilft Ihnen auch bei der Verwaltung Ihrer PIN oder Ihres Kennworts. Weitere Informationen zum Aktivieren der MBAM-Systemsteuerung finden Sie unter [Ausblenden der BitLocker-Standardverschlüsselung in der Windows-System](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md)Steuerung.

**Hinweis**  Für den BitLocker-Client befinden sich die Administrator-und Betriebsprotokoll Dateien in der Ereignisanzeige unter **Anwendungs-und Dienstprotokolle**  /  **Microsoft**  /  **Windows**-  /  **BitLockerManagement**.

 

**So verwenden Sie die MBAM-Client-Systemsteuerung**

1.  Um die BitLocker-Verschlüsselungsoptionen zu öffnen, klicken Sie auf **Start**, und wählen Sie **System**Steuerung aus. Wenn **die Systemsteuerung geöffnet** wird, wählen Sie **System und Sicherheit**aus.

2.  Doppelklicken Sie auf **BitLocker-Verschlüsselungsoptionen** , um die angepasste MBAM-Systemsteuerung zu öffnen. Es wird eine Liste aller Festplatten auf dem Computer und deren Verschlüsselungsstatus angezeigt. Außerdem wird eine Option zum Verwalten Ihrer PIN oder Kennwörter angezeigt.

3.  Verwenden Sie die Liste der Festplattenlaufwerke auf dem Computer, um den Verschlüsselungsstatus zu überprüfen, ein Laufwerk zu entsperren oder eine Ausnahme für den BitLocker-Schutz zu fordern, wenn die Richtlinien für Benutzer-und Computer Ausnahmen bereitgestellt wurden.

4.  Nicht Administratoren können Pins oder Kennwörter mithilfe der Systemsteuerung für BitLocker-Verschlüsselungsoptionen verwalten. Ein Benutzer kann " **Pin verwalten** " auswählen und dann sowohl eine aktuelle PIN als auch eine neue PIN eingeben. Benutzer können auch Ihre neue PIN bestätigen. Mit der Funktion " **Pin aktualisieren** " wird die PIN auf das neue zurückgesetzt, das der Benutzer auswählt.

5.  Wenn Sie Ihr Kennwort verwalten möchten, wählen Sie **Laufwerk entsperren** und geben Sie Ihr aktuelles Kennwort ein. Sobald das Laufwerk entriegelt ist, wählen Sie **Kennwort zurücksetzen** aus, um Ihr aktuelles Kennwort zu ändern.

## Verwandte Themen


[Verwalten von MBAM 1.0-Funktionen](administering-mbam-10-features.md)

 

 





