---
title: Versionshinweise für DaRT 8.0
description: Versionshinweise für DaRT 8.0
author: dansimp
ms.assetid: e8b373c8-7aa5-4930-a8f9-743d26145dad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 894708585ff4006c37085e71f365690b8424d43e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810765"
---
# Versionshinweise für DaRT 8.0


**Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.**

Lesen Sie diese Versionshinweise gründlich, bevor Sie Microsoft Diagnostics and Recovery Toolset (Dart) 8,0 installieren.

Diese Versionshinweise enthalten Informationen, die erforderlich sind, um Dart 8,0 erfolgreich zu installieren. Die Anmerkungen zu dieser Version enthalten auch Informationen, die in der Produktdokumentation nicht zur Verfügung stehen. Wenn es einen Unterschied zwischen diesen Versionshinweisen und anderer Dart-Dokumentation gibt, sollte die neueste Änderung als autorisierend angesehen werden. Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.

Informationen zum Abrufen der Dart-Software finden Sie unter [Abrufen von MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).

## Informationen zur Produktdokumentation


Informationen zur Dokumentation für Dart finden Sie auf der [Dart-Startseite](https://go.microsoft.com/fwlink/?LinkID=252096) auf Microsoft TechNet.

Eine herunterladbare Kopie der Dart-Dokumentation finden Sie <https://go.microsoft.com/fwlink/?LinkID=267420> im Microsoft Download Center.

## Abgeben von Feedback


Wir sind an Ihrem Feedback zu Dart 8,0 interessiert. Sie können Ihr Feedback an senden <mdopdocs@microsoft.com> .

**Hinweis**  Diese e-Mail-Adresse ist kein Supportkanal, aber Ihr Feedback wird uns helfen, zukünftige Änderungen für unsere Dokumentation und Produktversionen zu planen.

 

Die neuesten Informationen zu MDOP und weiteren Lernressourcen finden Sie auf der Seite [MDOP-Informationen](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Wenn Sie weitere Informationen zu neuen Updates oder Feedback geben möchten, folgen Sie uns auf [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) oder [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## Bekannte Probleme mit Dart 8,0


### System Wiederherstellung schlägt fehl, wenn Sie den Schlosser-oder Registrierungs-Editor ausführen

Wenn Sie Schlosser, Registrierungs-Editor und möglicherweise andere Tools ausführen, schlägt die System Wiederherstellung fehl.

**Problemumgehung:** Schließen Sie Dart, und starten Sie es erneut, und starten Sie dann die System Wiederherstellung.

### Der SFC-Scan läuft nach dem Starten und Schließen der Schlosser-oder Computer Verwaltung nicht.

Wenn Sie die Schlosser-oder Computer Verwaltungstools starten und dann schließen, kann die System Dateiprüfung nicht ausgeführt werden.

**Problemumgehung:** Schließen Sie Dart, und starten Sie dann den SFC.

### <a href="" id="-------------dart-installer-does-not-fail-when-adk-has-not-been-installed"></a> Dart-Installationsprogramm schlägt nicht fehl, wenn ADK nicht installiert wurde

Wenn Sie Dart 8,0 über die Befehlszeile zum Ausführen der MSI-Version installieren und das ADK nicht installiert wurde, sollte die Dart-Installation fehlschlagen. Derzeit installiert das Dart 8,0-Installationsprogramm alle Komponenten mit Ausnahme des Dart 8,0-Wiederherstellungsabbilds.

**Problemumgehung:** Keine.

### Defender kann nicht gestartet werden, nachdem Schlosser, regedit, Crash Analyzer und Computer Verwaltung gestartet wurden

Defender startet nicht, wenn Sie bereits Schlosser, regedit, Crash Analyzer und Computer Verwaltung gestartet haben.

**Problemumgehung:** Schließen und starten Sie Dart neu, und starten Sie dann Defender.

### Defender kann langsam starten

Defender benötigt manchmal einige Minuten, um zu starten. Auf der Statusleiste wird der aktuelle Ladestatus angezeigt.

**Problemumgehung:** Keine.

## Anmerkungen zu dieser Version Copyright-Informationen


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune und WindowsPowerShell sind Marken der Microsoft-Unternehmensgruppe. Alle anderen Marken sind Eigentum ihrer jeweiligen Eigentümer.



## Verwandte Themen


[Informationen zu DaRT 8.0](about-dart-80-dart-8.md)

 

 





