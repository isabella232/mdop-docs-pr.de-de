---
title: Informationen zu App-V 5.0 SP2
description: Informationen zu App-V 5.0 SP2
author: dansimp
ms.assetid: 16ca8452-cef2-464e-b4b5-c10d4630fa6a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9a476f3bf273717b5a85a4244c5796f893b0c617
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806127"
---
# Informationen zu App-V 5.0 SP2


App-V 5.0 SP2 bietet eine verbesserte integrierte Plattform, eine flexiblere Virtualisierung und ein leistungsstarkes Management für virtualisierte Anwendungen. Weitere Informationen finden Sie unter [App-V 5,0 Overview](https://go.microsoft.com/fwlink/p/?LinkId=325265) ( https://go.microsoft.com/fwlink/?LinkId=325265) .

## Änderungen in der Standard mäßigen App-V 5.0 SP2-Funktionalität


Die folgenden Abschnitte enthalten Informationen zu den Änderungen der Standardfunktionen für App-V 5.0 SP2.

### <a href="" id="bkmk-sp2-supported-cfg"></a>Unterstützung für Windows Server 2012 R2 und Windows 8,1

App-V 5,0 mit Unterstützung für Windows Server 2012 R2 und Windows 8,1

### <a href="" id="-------------app-v-5-0-sp2-now-supports-folder-redirection-for-the-user-s-roaming-appdata-directory"></a> App-V 5.0 SP2 unterstützt jetzt die Ordnerumleitung für das Roaming-AppData-Verzeichnis des Benutzers.

App-V 5.0 SP2 unterstützt Roaming-APPDATA (% APPDATA%) Ordnerumleitung. Weitere Informationen finden Sie unter [Planen der Verwendung der Ordnerumleitung mit App-V](planning-to-use-folder-redirection-with-app-v.md).

### <a href="" id="bkmk-pkg-upgr-pendg-tasks"></a>Verbesserungen des Paket Upgrades und ausstehende Aufgaben

In App-V 5.0 SP2 werden Sie nicht mehr aufgefordert, eine ausgeführte virtuelle Anwendung zu schließen, wenn eine neuere Version des Pakets oder der Verbindungsgruppe veröffentlicht wird. Wenn ein Paket oder eine Verbindungsgruppe verwendet wird, wenn Sie versuchen, eine verwandte Aufgabe auszuführen, wird eine Meldung angezeigt, die angibt, dass das Objekt verwendet wird und der Vorgang zu einem späteren Zeitpunkt versucht wird.

Aufgaben, die in einem ausstehenden Status gespeichert wurden, werden gemäß den folgenden Regeln ausgeführt:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Art der Hintergrundaufgabe</th>
<th align="left">Anwendbare Regel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Benutzerbasierte Aufgaben, beispielsweise die Veröffentlichung eines Pakets für einen Benutzer</p></td>
<td align="left"><p>Die ausstehende Aufgabe wird ausgeführt, nachdem sich der Benutzer abgemeldet hat und sich dann wieder anmeldet.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Global basierender Vorgang, beispielsweise Aktivieren einer Verbindungsgruppe Global</p></td>
<td align="left"><p>Die ausstehende Aufgabe wird ausgeführt, wenn der Computer heruntergefahren und neu gestartet wird.</p></td>
</tr>
</tbody>
</table>

 

Wenn eine Aufgabe in einem ausstehenden Zustand befindet, generiert der App-V-Client auch einen Registrierungsschlüssel für die ausstehende Aufgabe wie folgt:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Benutzerbasierter oder Global basierter Vorgang</th>
<th align="left">Ort, an dem der Registrierungsschlüssel generiert wird</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Benutzerbasierte Aufgaben</p></td>
<td align="left"><p>KEY_CURRENT_USER \software\microsoft\appv\client\pendingtasks</p></td>
</tr>
<tr class="even">
<td align="left"><p>Global basierte Aufgaben</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \software\microsoft\appv\client\pendingtasks</p></td>
</tr>
</tbody>
</table>

 

### Virtualisierung von Microsoft Office 2013 und Microsoft Office 2010 mithilfe von App-V 5,0

Verwenden Sie den folgenden Link, um weitere Informationen zu App-V 5,0 unterstützte Microsoft Office-Szenarien zu erhalten.

[Virtualisierung von Microsoft Office2013 für Application Virtualization (App-V) 5.0](../solutions/virtualizing-microsoft-office-2013-for-application-virtualization--app-v--50-solutions.md)

**Hinweis**  Dieses Dokument befasst sich mit dem Erstellen eines Microsoft Office 2013-App-V 5,0-Pakets. Sie enthält jedoch auch Informationen zu Szenarien für Microsoft Office 2010 mit App-V 5,0.

 

### <a href="" id="-------------app-v-5-0-client-management-user-interface-application"></a> App-V 5,0-Benutzeroberflächenanwendung für die Client Verwaltung

In früheren Versionen von App-v 5,0 wurde die Client Verwaltungsbenutzeroberfläche (UI) mit der APP-v 5,0-Clientinstallation bereitgestellt. Mit App-V 5.0 SP2 ist dies nicht mehr der Fall. Administratoren haben jetzt die Möglichkeit, die APP-v 5,0-Client-Benutzeroberfläche als virtuelle Anwendung (unter Verwendung aller unterstützten App-v-Bereitstellungskonfigurationen) oder als installierte Anwendung bereitzustellen.

Weitere Informationen finden Sie unter [Microsoft Application Virtualization 5,0 Client-Benutzeroberflächenanwendung](https://go.microsoft.com/fwlink/p/?LinkId=386345) ( https://go.microsoft.com/fwlink/?LinkId=386345) .

### Automatisches Verpacken und Bereitstellen von nebeneinander angeordneten (SxS) Assemblys

App-v 5.0 SP2 erkennt jetzt automatisch parallele (SxS) Assemblys und die Bereitstellung auf dem Computer, auf dem der APP-v 5.0 SP2-Client ausgeführt wird. Eine SxS-Assembly besteht in erster Linie aus VC + +-Laufzeitabhängigkeiten oder MSXML. In früheren Versionen von App-v erforderten virtuelle Anwendungen mit Abhängigkeiten von VC-Laufzeiten, dass diese Abhängigkeiten lokal auf dem Computer ausgeführt werden, auf dem der App-V 5.0 SP2-Client ausgeführt wird.

Die folgenden Funktionen werden jetzt unterstützt:

-   Der App-V 5,0-Sequenzer zeichnet die SxS-Assembly automatisch im Paket auf, unabhängig davon, ob die VC-Laufzeit bereits auf dem Computer installiert ist, auf dem der Sequencer ausgeführt wird.

-   Der App-V 5,0-Client installiert die erforderliche SxS-Assembly automatisch auf dem Computer, auf dem der Client ausgeführt wird, wie dies zum Zeitpunkt der Veröffentlichung erforderlich ist.

-   Der App-V 5,0-Sequenzer meldet die VC-Laufzeitabhängigkeit mithilfe des Sequencer-Berichterstattungsmechanismus.

-   Mit dem App-V 5,0-Sequenzer können Sie jetzt die VC-Laufzeitabhängigkeit ausschließen, falls die Abhängigkeit bereits auf dem Computer verfügbar ist, auf dem der Sequencer ausgeführt wird.

### Verbesserungen bei der Veröffentlichungsaktualisierung

App-V 5,0 unterstützt mehrere Features wurden hinzugefügt, um die allgemeine Erfahrung beim Aktualisieren einer Reihe von Anwendungen für einen bestimmten Benutzer zu verbessern.

In der folgenden Liste werden die Verbesserungen der Veröffentlichungsaktualisierung angezeigt:

In der folgenden Liste finden Sie weitere Informationen dazu, wie die Verbesserungen bei der Aktualisierung der Veröffentlichung aktiviert werden.

-   **EnablePublishingRefreshUI** – aktiviert die Statusleiste für die Veröffentlichungsaktualisierung für den Computer, auf dem der App-V 5,0-Client ausgeführt wird.

-   **HideUI** – blendet die Statusleiste der Veröffentlichungsaktualisierung während einer manuellen Synchronisierung aus.

### Einstellung für neue Client Konfiguration

Die folgende neue Client Konfigurationseinstellung ist in App-V 5,0 SP2 verfügbar:

**EnableDynamicVirtualization** – ermöglicht unterstützte Shell-Erweiterungen, Browser-helferobjekte und ActiveX-Steuerelemente, die virtualisiert und mit virtuellen Anwendungen ausgeführt werden können.

Weitere Informationen finden Sie unter [Informationen zu Client Konfigurationseinstellungen](about-client-configuration-settings.md).

### <a href="" id="-------------app-v-5-0-shell-extensions"></a> App-V 5,0-Shell-Erweiterungen

App-V 5,0 SP2 unterstützt jetzt Shell-Erweiterungen.

Weitere Informationen finden Sie im Abschnitt **Unterstützung für Shell-Erweiterungen der APP-v 5.0 SP2** unter [Erstellen und Verwalten von virtualisierten Anwendungen in App-v 5,0](creating-and-managing-app-v-50-virtualized-applications.md).

## <a href="" id="---------app-v-5-0-documentation-updates"></a> App-V 5,0-Dokumentationsupdates


App-V 5,0 SP2 bietet aktualisierte Dokumentation für die folgenden Szenarien:

-   [Migrieren von einer früheren Version](migrating-from-a-previous-version-app-v-50.md)

-   [Informationen zu App-V 5.0](about-app-v-50.md)

-   [Informationen zu App-V 5,0-Berichterstellung](about-app-v-50-reporting.md) (Abschnitt "häufig gestellte Fragen")

## So erhalten Sie MDOP-Technologien


App-V 5,0 ist Teil des Microsoft Desktop Optimization Pack (MDOP). MDOP ist Teil von Microsoft Software Assurance. Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter [wie erhalte ich MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .






## Verwandte Themen


[Versionshinweise für App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md)

 

 





