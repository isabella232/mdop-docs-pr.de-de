---
title: Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 1.0 SP1
description: Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 1.0 SP1
author: dansimp
ms.assetid: 447fae0c-fe87-4d1c-b616-6f92fbdaf6d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8584999d9fdbdfccc3e9b2b1486cb97635475747
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804262"
---
# Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 1.0 SP1


Drücken Sie STRG + F, um die Microsoft User Experience Virtualization (UE-V) 1,0 Service Pack 1-Versionshinweise zu durchsuchen.

Lesen Sie diese Versionshinweise gründlich, bevor Sie UE-V installieren. Die Anmerkungen zu dieser Version enthalten Informationen, die erforderlich sind, um die Virtualisierung der Benutzeroberfläche erfolgreich zu installieren, und zusätzliche Informationen enthalten, die in der Produktdokumentation nicht zur Verfügung stehen. Wenn es Unterschiede zwischen diesen Versionshinweisen und anderen UE-V-Dokumentationen gibt, sollte die neueste Änderung als autorisierend angesehen werden. Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.

## Bekannte Probleme in UE-V


Dieser Abschnitt enthält Anmerkungen zu dieser Version von User Experience Virtualization 1,0 SP1.

### Registrierungseinstellungen können nicht zwischen App-V und systemeigenen Anwendungen auf demselben Computer synchronisiert werden.

Wenn ein Computer über eine Anwendung verfügt, die sowohl über die Application Virtualization (App-V)-Anwendung als auch über eine systemeigene Installationsanwendung verfügt, die mit einer Windows Installer-Datei (MSI-Datei) installiert ist, werden die registrierungsbasierten Einstellungen nicht zwischen den Technologien synchronisiert.

Problemumgehung: um dieses Problem zu beheben, führen Sie die Anwendung aus, indem Sie eine der beiden Technologien auswählen, aber nicht beide.

### <a href="" id="windows-8-setting-synchronization-fails-when-network-share-is-outside-user-s-domain"></a>Die Synchronisierung von Windows 8-Einstellungen schlägt fehl, wenn die Netzwerkfreigabe außerhalb der Domäne des Benutzers liegt

Wenn Windows® 8 die Synchronisierung der Betriebssystem Einstellungen versucht, schlägt die synchrnization mit der folgenden Fehlermeldung fehl: **Boost:: File System:: EXISTS:: Falscher Benutzername oder Kennwort**. Dieser Fehler kann darauf hindeuten, dass sich die Netzwerkfreigabe außerhalb der Domäne des Benutzers befindet. Wenn Sie nach Betriebsprotokoll Ereignissen suchen möchten, öffnen Sie die **Ereignisanzeige** , und navigieren Sie zu **Anwendungen und Dienstprotokolle**, die  /  **Microsoft**  /  **User Experience Virtualization**-  /  **Protokollierung**in  /  **Betrieb**sind. Netzwerkfreigaben, die für die Speicherorte der UE-V-Einstellungen verwendet werden, sollten sich in derselben Active Directory-Domäne wie der Benutzer befinden.

Problemumgehung: Verwenden Sie Netzwerkfreigaben aus der gleichen Active Directory-Domäne wie der Benutzer. .

### E-Mail-Signatur-Roaming für Outlook 2010

UE-V durchstreift die Outlook 2010-Signaturdateien zwischen Geräten. Die standardmäßigen Signaturoptionen für neue Nachrichten und Antworten/Weiterleitungen werden jedoch nicht durchstreift. Diese beiden Einstellungen werden im Outlook-Profil gespeichert, das UE-V nicht durchwandert.

Problemumgehung: keine.

### Synchronisierungseinstellungen werden nicht im erwarteten Intervall synchronisiert, wenn Sie im Slow-Link-Modus ausgeführt werden.

Unter normalen Bedingungen sollten Einstellungen Speicherorte über eine fast Link-Netzwerkverbindung zur Verfügung stehen. Im Modus für langsame Verbindungen erfolgt die Synchronisierung nur regelmäßig. Standardmäßig ist der Synchronisierungszeitplan für den Slow-Link-Modus auf alle 360 Minuten eingestellt.

Problemumgehung: Wenn Sie die Häufigkeit der Hintergrundsynchronisierung für Computer im Slow-Link-Modus ändern möchten, können Sie die Gruppenrichtlinie für die Hintergrund Synchronisierungs Richtlinie für **Offline Dateien**konfigurieren.

### Sonderzeichen werden nicht synchronisiert

Bestimmte Zeichen wie Währungssymbole können nicht zwischen Windows 7-und Windows 8-Computern synchronisiert werden, auf denen der UE-V-Agent ausgeführt wird.

Problemumgehung: keine.

### UE-V unterstützt keine Roamingeinstellungen zwischen 32-Bit-und 64-Bit-Versionen von Microsoft Office.

Wir empfehlen, die 32-Bit-Version von Microsoft Office sowohl für 32-Bit-als auch für 64-Bit-Betriebssysteme zu installieren. Wenn Sie die von Ihnen benötigte Microsoft Office-Version auswählen möchten, klicken Sie hier ( [http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623) ). UE-V unterstützt Roamingeinstellungen zwischen identischen Architekturversionen von Office. Beispielsweise werden die Office-Einstellungen für 32-Bit zwischen allen 32-Bit-Office-Instanzen durchlaufen. UE-V unterstützt keine Roamingeinstellungen zwischen 32-Bit-und 64-Bit-Versionen von Office.

Problemumgehung: keine

### <a href="" id="msi-s-are-not-localized"></a>MSI-Versionen sind nicht lokalisiert

UE-v 1,0 SP1 umfasst ein lokalisiertes Setupprogramm für den UE-v-Agent und den UE-v-Generator. Diese MSI-Dateien sind weiterhin verfügbar, die Benutzeroberfläche wird jedoch minimiert, und die MSI-Datei wird nur in Englisch angezeigt. Obwohl die Datei in Englisch ist, werden alle unterstützten Sprachen während der Installation von dem Setup-Programm installiert.

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

### Lange Einstellungen Speicherpfade können einen Fehler verursachen

Behalten Sie die Einstellungen für den Speicherpfad so kurz wie möglich. Lange Pfade können die Auflösung oder Synchronisierung verhindern. UE-V verwendet den Einstellungsspeicher Pfad als Teil des berechneten Pfads zum Speichern von Einstellungen. Dieser Pfad wird folgendermaßen berechnet: Einstellungsspeicher Pfad + "settingspackages" + Paket dir (Vorlagen-ID) + Paketname (Vorlagen-ID). Wenn der berechnete Pfad 260 Zeichen überschreitet, schlägt der Paketspeicher fehl, und es wird die folgende Fehlermeldung im operationellen UE-V-Ereignisprotokoll generiert:

`[boost::filesystem::copy_file: The system cannot find the path specified]`

Zum Überprüfen der Betriebsprotokoll Ereignisse öffnen Sie die Ereignisanzeige, und navigieren Sie zu Anwendungen und Dienstprotokolle/Microsoft/User Experience Virtualization/Logging/Operational.

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

 

 





