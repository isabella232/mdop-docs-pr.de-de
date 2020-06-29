---
title: So konfigurieren Sie Benutzerberechtigungen
description: So konfigurieren Sie Benutzerberechtigungen
author: dansimp
ms.assetid: 54e69f46-b028-4ad1-9b80-f06ef5c8f559
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3c2581a9f9dddcbc63682d356c777a24222dd62f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807224"
---
# So konfigurieren Sie Benutzerberechtigungen


Sie können einige Aktionen für Benutzer, die nicht über Administratorrechte verfügen, aktivieren und deaktivieren, indem Sie die Schlüsselwerte unter dem Registrierungsschlüssel " **Berechtigungen** " Bearbeiten (HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\permissions). Dieser Schlüssel dient in erster Linie dazu, Benutzer daran zu hindern, Fehler zu machen, anstatt besondere Sicherheit zu gewährleisten, da Benutzer mit Administratorrechten einen dieser Schlüsselwerte bearbeiten können. Die folgenden Verfahren sind Beispiele für das Ändern der Schlüsselwerte. Weitere Informationen zu den Registrierungsschlüsseln und Werten der Application Virtualization (App-V)-Client Registrierung finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=121528> .

**So ändern Sie die Benutzerberechtigungen**

1.  Damit die Benutzer den Client im Offlinemodus ausführen können, legen Sie den folgenden Schlüsselwert auf 1:

    HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\permissions\\toggleofflinemode

2.  Damit die Benutzer alle Anwendungen über die Benutzeroberfläche anzeigen können, müssen Sie den folgenden Schlüsselwert auf 1 festlegen. Wenn der Wert auf 0 (null) festgelegt wird, können die Benutzer nur die Anwendungen sehen, die Ihnen zur Verfügung stehen.

    HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\permissions\\viewallapplications

## Verwandte Themen


[So konfigurieren Sie die App-V-Client-Registrierungseinstellungen über die Befehlszeile](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

[Benutzerzugriffsberechtigungen in Application Virtualization Client](user-access-permissions-in-application-virtualization-client.md)

 

 





