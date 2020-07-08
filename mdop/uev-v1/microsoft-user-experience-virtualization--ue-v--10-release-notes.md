---
title: Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 1.0
description: Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 1.0
author: dansimp
ms.assetid: 920f3fae-e9b5-4b94-beda-32c19d31e94b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9f9942eef7ea84cf7010a0c0173427827a512216
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804265"
---
# Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 1.0


Drücken Sie STRG + F, um Microsoft User Experience Virtualization (UE-V)-Versionshinweise zu durchsuchen.

Lesen Sie diese Versionshinweise gründlich, bevor Sie UE-V installieren. Die Anmerkungen zu dieser Version enthalten Informationen, die erforderlich sind, um die Virtualisierung der Benutzeroberfläche erfolgreich zu installieren, und zusätzliche Informationen enthalten, die in der Produktdokumentation nicht zur Verfügung stehen. Wenn es Unterschiede zwischen diesen Versionshinweisen und anderen UE-V-Dokumentationen gibt, sollte die neueste Änderung als autorisierend angesehen werden. Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.

## Abgeben von Feedback


Teilen Sie uns Ihre Meinung zu unserer Dokumentation zu MDOP mit, indem Sie uns Feedback und Kommentare geben. Senden Sie Ihr Feedback zur Dokumentation an [mdopdocs@Microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).

## Bekannte Probleme in UE-V


Dieser Abschnitt enthält Anmerkungen zu dieser Version für die Virtualisierung der Benutzeroberfläche.

### Registrierungseinstellungen können nicht zwischen App-V und systemeigenen Anwendungen auf demselben Computer synchronisiert werden.

Wenn ein Computer über eine Anwendung verfügt, die sowohl über die Application Virtualization (App-V)-Anwendung als auch über eine systemeigene Installationsanwendung (mit einer MSI-Datei installiert) verfügbar ist, werden die registrierungsbasierten Einstellungen nicht zwischen den Technologien synchronisiert.

Problemumgehung: um dieses Problem zu beheben, führen Sie die Anwendung aus, indem Sie eine der beiden Technologien auswählen, aber nicht beide.

### Bei der Synchronisierung von Windows 8-Einstellungen tritt ein Fehler auf: "Boost:: Dateisystem:: EXISTS:: Falscher Benutzername oder Kennwort"

Die Synchronisierung der Betriebssystem Einstellungen für Windows® 8 schlägt mit der folgenden Fehlermeldung fehl: **Boost:: File System:: EXISTS:: Falscher Benutzername oder Kennwort**. Wenn Sie nach Betriebsprotokoll Ereignissen suchen möchten, öffnen Sie die **Ereignisanzeige** , und navigieren Sie zu **Anwendungen und Dienstprotokolle**, die  /  **Microsoft**  /  **User Experience Virtualization**-  /  **Protokollierung**in  /  **Betrieb**sind. Netzwerkfreigaben, die für die Speicherorte der UE-V-Einstellungen verwendet werden, sollten sich in derselben Active Directory-Domäne wie der Benutzer befinden. Andernfalls kann der folgende Fehler auftreten: "Falscher Benutzername oder Kennwort".

Problemumgehung: Verwenden Sie Netzwerkfreigaben aus der gleichen Active Directory-Domäne wie der Benutzer. .

### E-Mail-Signatur-Roaming für Outlook 2010

UE-V durchstreift die Outlook 2010-Signaturdateien zwischen Geräten. Die standardmäßigen Signaturoptionen für neue Nachrichten und Antworten/Weiterleitungen sind jedoch nicht.Diese beiden Einstellungen werden im Outlook-Profil gespeichert, das UE-Vdoes nicht durchwandert.

Problemumgehung: keine.

### Synchronisierungseinstellungen werden nicht im erwarteten Intervall synchronisiert, wenn Sie im Slow-Link-Modus ausgeführt werden.

Unter normalen Bedingungen sollten Einstellungen Speicherorte über eine fast Link-Netzwerkverbindung zur Verfügung stehen. Im Modus für langsame Verbindungen erfolgt die Synchronisierung nur regelmäßig. Standardmäßig ist der Synchronisierungszeitplan für den Slow-Link-Modus auf alle 360 Minuten eingestellt.

Problemumgehung: Wenn Sie die Häufigkeit der Hintergrundsynchronisierung für Computer im Slow-Link-Modus ändern möchten, können Sie die Gruppenrichtlinie für die Hintergrund Synchronisierungs Richtlinie für **Offline Dateien**konfigurieren.

### Sonderzeichen werden nicht synchronisiert

Bestimmte Zeichen wie Währungssymbole können nicht zwischen Windows 7-und Windows 8-Computern synchronisiert werden, auf denen der UE-V-Agent ausgeführt wird.

Problemumgehung: keine.

### UE-V unterstützt keine Roamingeinstellungen zwischen 32-Bit-und 64-Bit-Versionen von Microsoft Office.

Wir empfehlen, die 32-Bit-Version von Microsoft Office sowohl für 32-Bit-als auch für 64-Bit-Betriebssysteme zu installieren. Wenn Sie die von Ihnen benötigte Microsoft Office-Version auswählen möchten, klicken Sie hier. ([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)). UE-V unterstützt Roamingeinstellungen zwischen identischen Architekturversionen von Office. Beispielsweise werden die Office-Einstellungen für 32-Bit zwischen allen 32-Bit-Office-Instanzen durchlaufen. UE-V unterstützt keine Roamingeinstellungen zwischen 32-Bit-und 64-Bit-Versionen von Office.

Problemumgehung: keine

### Andere Ordner auf der Freigabe mit dem Einstellungs Speicherort sind im Modus für langsame Verbindung nicht verfügbar.

Einstellungen Speicherfreigaben sollten sich nicht auf einer Netzwerkfreigabe befinden, die für andere Ordner verwendet wird, die immer verfügbar sein müssen. Wenn die Netzwerkfreigabe, die den festgelegten Speicherplatz hostet, in den Modus für langsame Verbindung wechselt, ist der einzige verfügbare Ordner der Ordner Einstellungen-Speicherort. Andere Ordner auf der Freigabe stehen im Modus für langsame Verbindung nicht zur Verfügung.

Problemumgehung: keine

### Favicons, die mit Internet Explorer 9-Favoriten verknüpft sind, werden nicht durchwandert

Die Favicons, die mit Internet Explorer 9-Favoriten verknüpft sind, werden nicht von der Benutzeroberflächen-Virtualisierung durchlaufen und nicht angezeigt, wenn die Favoriten auf einem neuen Computer erstmalig angezeigt werden.

Problemumgehung: Favicons werden mit den zugehörigen Favoriten angezeigt, sobald die Textmarke verwendet und im Internet Explorer 9-Browser zwischengespeichert wurde.

### Datei Einstellungs Pfade werden in der Registrierung gespeichert

In einigen Anwendungseinstellungen werden die Pfade Ihrer Konfigurations-und Einstellungsdateien als Werte in der Registrierung gespeichert. Die Dateien, die als Pfade in der Registrierung referenziert werden, müssen synchronisiert werden, wenn die Einstellungen zwischen Computern durchlaufen werden.

Problemumgehung: Verwenden Sie die Ordnerumleitung oder eine andere Technologie, um sicherzustellen, dass alle Dateien, auf die als Pfad für Datei Einstellungen verwiesen wird, vorhanden sind und auf allen Computern, auf denen die Einstellungen durchlaufen werden, an derselben Stelle abgelegt werden.

### Pfade, die länger als 260 Zeichen sind, werden nicht unterstützt.

Einstellungen Speicherpfade, die länger als 260 Zeichen sind, werden nicht unterstützt. Das Kopieren der UE-v-Einstellungs Pakete in Einstellungen Speicherpfade, die länger als 260 Zeichen sind, schlägt fehl, und die folgende Ausnahmemeldung wird im operationellen UE-v-Ereignisprotokoll generiert: **\ [Boost:: Dateisystem:: Kopieren \ _File: das System kann den angegebenen Pfad nicht finden \]**. Wenn Sie nach Betriebsprotokoll Ereignissen suchen möchten, öffnen Sie die **Ereignisanzeige** , und navigieren Sie zu **Anwendungen und Dienstprotokolle**, die  /  **Microsoft**  /  **User Experience Virtualization**-  /  **Protokollierung**in  /  **Betrieb**sind.

Datei Einstellungs Pfade, die länger als 260 Zeichen sind, werden zurzeit nicht unterstützt. Datei Einstellungen, auf die in UE-V-Einstellungen verwiesen wird, können sich nicht in einem Verzeichnispfad befinden, der mehr als 260 Zeichen enthält.

Problemumgehung: keine.

### UE-V-Agenten Verzögerungen beim Abmelden oder anmelden

Wenn eine Anmeldung oder Abmeldung stattfindet, bevor Offline Dateien festgestellt haben, dass eine langsame Verbindung vorhanden ist, kann sich das Abmelden oder anmelden verzögert werden. Das Feature "Offline Dateien" kann bis zu drei Minuten dauern, um den aktuellen Netzwerkzustand zu erkennen. Wenn die Anmeldung oder das Herunterfahren eintritt, bevor Offline Dateien festgestellt haben, dass der Computer mit einer langsamen Verbindung verbunden ist, wird das UE-V-Einstellungspaket an den Server anstelle des lokalen Caches gesendet.

Problemumgehung: keine.

### Konflikte beim Versuch, die Einstellungen des Betriebssystems unter Windows 8 zu durchlaufen

Unter Windows 8, wenn die Microsoft-Konto Synchronisierung zusammen mit UE-V für Betriebssystemeinstellungen aktiviert ist, sind die angewendeten Einstellungen möglicherweise inkonsistent.

Problemumgehung: führen Sie eine der folgenden Aktionen aus:

-   Deaktivieren der Microsoft-Konto Synchronisierung, wenn Sie UE-V für die Roaming-Einstellungen des Betriebssystems verwenden

-   Deaktivieren von UE-V für Betriebssystemeinstellungen

### Einige Betriebssystemeinstellungen wechseln nur zwischen Betriebssystemversionen

Die Betriebssystemeinstellungen für Sprachausgaben und Währungszeichen, die für das gebietsschemaspezifisch sind, werden nur wie Betriebssystemversionen von Windows durchlaufen. Währungszeichen können beispielsweise nur von Windows 7 zu Windows 7 gewechselt werden.

Problemumgehung: keine

### Internet Explorer-Lesezeichen werden in der SmartBar von Internet Explorer nicht angezeigt

Wenn Internet Explorer-Lesezeichen von einem Computer auf einen anderen Computer übertragen werden, kann der Index auf dem zweiten Computer nicht aktualisiert werden, sodass der Favorit beim eingeben in der Adressleiste nicht als mögliches Suchergebnis auf Computer 2 angezeigt wird.

Problemumgehung: keine

 

 





