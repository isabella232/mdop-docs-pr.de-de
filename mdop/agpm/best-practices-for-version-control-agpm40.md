---
title: Bewährte Methoden für die Versionskontrolle
description: Bewährte Methoden für die Versionskontrolle
author: dansimp
ms.assetid: 4a2a1ac7-67f3-4ba3-ab07-860d33da0efe
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d560913c4e0f49a2015f620564a9038677d65144
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807808"
---
# Bewährte Methoden für die Versionskontrolle


Microsoft Advanced Group Policy Management (AGPM) bietet Versionskontrolle für Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) ähnlich wie Microsoft Visual SourceSafe® bietet Versionskontrolle für Quellcode. Entwickler können Visual SourceSafe verwenden, um mehrere Versionen jeder Quelldatei zu verwalten. Gruppenrichtlinienadministratoren können AGPM verwenden, um dasselbe für GPOs zu tun. Bei der Verwendung von AGPM sollten Gruppenrichtlinienadministratoren bewährte Methoden berücksichtigen, die für jedes Versionsverwaltungssystem gelten:

-   **Datum und Uhrzeit:** AGPM stempelt jede Version eines GPO mit dem Datum und der Uhrzeit. Um sicherzustellen, dass der Verlauf richtig ist, insbesondere beim Bearbeiten von GPOs auf mehr als einem Computer, stellen Sie sicher, dass jeder Computer seine Uhr mit einer autorisierenden Zeitquelle synchronisiert.

-   **Überprüfen Sie GPOs, wenn Sie die Bearbeitung fertig sind:** Es ist üblich, dass die Redakteure GPOs Auschecken und vergessen, Sie wieder in das Archiv zu überprüfen. Dies kann jedoch verhindern, dass andere Gruppenrichtlinienadministratoren das Gruppenrichtlinienobjekt ändern. Überprüfen Sie GPOs immer wieder in AGPM, wenn Sie mit der Bearbeitung fertig sind.

-   **Häufiges Speichern von Änderungen:** Wenn Sie ein GPO bearbeiten, speichern Sie die Änderungen häufig. Die meisten Redakteure checken ein GPO aus, nehmen viele Änderungen vor und überprüfen das Gruppenrichtlinienobjekt dann in das Archiv. Überprüfen Sie stattdessen das Gruppenrichtlinienobjekt regelmäßig in das Archiv, und überprüfen Sie es dann erneut. Das Detail kann so klein wie das Einchecken des Gruppenrichtlinienobjekts sein, nachdem Sie alle Einstellungen geändert (nicht empfohlen) oder das Gruppenrichtlinienobjekt eingecheckt haben, nachdem Sie Gruppen verwandter Änderungen vorgenommen haben. Das Ergebnis ist ein besser dokumentierter Verlauf für jedes GPO, das bei der Behandlung von Problemen helfen kann.

-   **Häufiges Bereitstellen von GPOs:** Lassen Sie keine neuen und bearbeiteten GPOs, die noch nicht bereitgestellt wurden, in großer Zahl im Archiv sammeln. Stellen Sie stattdessen neue und bearbeitete GPOs so schnell wie möglich bereit, damit Sie eine minimale Auswirkung auf die Produktionsumgebung haben. Durch die gleichzeitige Bereitstellung vieler neuer und bearbeiteter GPOs kann die Produktionsumgebung gefährdet werden.

-   **Dokumentieren des Zwecks von Änderungen beim Einchecken von GPOs:** Jeder Bearbeiter kann Versionen eines Gruppenrichtlinienobjekts vergleichen, um bestimmte Änderungen zwischen den beiden zu sehen. Durch die Dokumentation dieser spezifischen Änderungen wird kein Wert hinzugefügt. Dokumentieren Sie stattdessen die Absicht und den Zweck einer Änderung, anstatt zu dokumentieren, was Prüfer sehen können, indem Sie Differenz Berichte anzeigen. Versionskommentare sollten dem Vergleichsbericht einen Mehrwert verleihen und einem Bearbeiter helfen, zu verstehen, warum der Editor das Gruppenrichtlinienobjekt geändert hat.

-   **Testen von GPOs in einer Testumgebung:** Das Bereitstellen von GPOs in der Produktionsumgebung, ohne Sie zu testen, ist riskant. Testen Sie Ihre GPOs stattdessen in einer Domäne in einer Testgesamtstruktur, und exportieren Sie dann die GPOs in Dateien, und importieren Sie Sie in eine Domäne in einer Produktionsgesamtstruktur. Darüber hinaus können Sie GPOs mit einer Organisationseinheit verknüpfen, die Testcomputer und-Benutzer enthält. Überprüfen Sie, ob jedes GPO in der Testumgebung ordnungsgemäß funktioniert, und stellen Sie dann die GPOs in der Produktionsumgebung bereit.

### Weitere Verweise

-   [Advanced Group Policy Management 4.0](advanced-group-policy-management-40.md)

 

 





