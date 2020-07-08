---
title: Informationen zur Problembehandlung für Application Virtualization Client
description: Informationen zur Problembehandlung für Application Virtualization Client
author: dansimp
ms.assetid: 260a8dad-847f-4ec0-b7dd-6e6bc52017ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2ab332f5f3b7f8cdc40f6d35e8712d55028a60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806208"
---
# Informationen zur Problembehandlung für Application Virtualization Client


Dieses Thema enthält Informationen, die Sie zur Behebung verschiedener Probleme auf dem Application Virtualization (App-V)-Client verwenden können.

## Die Veröffentlichungsaktualisierung ist sehr langsam


Wenn die Veröffentlichungsaktualisierung auf einem bestimmten Computer viel länger als erwartet dauert und der Client für die Verwendung der **IconSourceRoot** -Einstellung konfiguriert ist, ermitteln Sie, ob **IconSourceRoot** eine ungültige URL enthält. Eine nicht gültige URL führt zu sehr langen Verzögerungen während der Veröffentlichungsaktualisierung.

## Benutzer können keine Verbindung mit dem Server herstellen und in den Modus für getrennte Vorgänge wechseln


Wenn Sie einen App-V-Verwaltungs Server verwenden, der mit dem RTSPS-Protokoll konfiguriert ist, können Sie ermitteln, ob das auf dem Server verwendete Zertifikat gültig ist, wenn die Benutzer keine Verbindung herstellen können und Sie in den Modus für getrennte Vorgänge wechseln. Ein nicht gültiges Zertifikat verhindert, dass Benutzer eine Verbindung herstellen können, und führt dazu, dass Sie in den Modus für getrennte Vorgänge wechseln.

## <a href="" id="users-experience-slow-performance-when-applications-are-not-fully-cached-"></a>Benutzer verlangsamen die Leistung, wenn Anwendungen nicht vollständig zwischengespeichert werden


Wenn Anwendungen nicht vollständig zwischengespeichert werden, kann es vorkommen, dass Benutzer beim Starten oder verwenden der Anwendung gelegentlich vorübergehende langsame oder zeitweilige Leistung erfahren. Dies kann mehrere mögliche Gründe haben, beispielsweise, wenn der App-V-Client gerade eine Anwendung automatisch lädt oder wenn eine außer Sequenz-Anforderung verarbeitet wird. Wenn die Anwendungen vollständig zwischengespeichert sind, treten diese Probleme nicht mehr auf.

## <a href="" id="error-displayed-after-an-update-is-removed-"></a>Fehler angezeigt, nachdem eine Aktualisierung entfernt wurde


Sie müssen das richtige Windows Installer 3,1-Befehls Format verwenden, um ein Update vom App-V-Client wie folgt zu entfernen:

`Msiexec /I {F82584A0-D706-4D2D-9BC1-7E6D8BE3BB0F} MSIPATCHREMOVE={BE3DD018-9A1F-40FD-9538-C0A995CBD254} /qb /l*v "Uninstall.log"`

Die Verwendung des älteren Befehlsformats `msiexec /package <GUID> /uninstall <GUID>` führt zu einem Fehler 6003 "Application Virtualization Client konnte nicht gestartet werden".

## Fehler Code 0A-0000E01E tritt auf, wenn Sie versuchen, eine Anwendung zu starten


Fehlercode 0A-0000E01E gibt an, dass das sequenzierte Anwendungspaket möglicherweise beschädigt ist. Die Lösung ist die Neusequenzierung des Pakets.

## Benutzer können nicht auf Dateien zugreifen, die Sie auf dem Laufwerk "f:" erstellt haben


Wenn Benutzer Dateien auf dem Laufwerk **Q:** speichern, können Sie Sie nicht abrufen, da Sie keine Lese Rechte für das Laufwerk besitzen. Benutzer sollten Dateien nicht auf dem Laufwerk **Q:** speichern.

## Der Benutzer wird mit einem 1D1-Fehler aufgefordert


Wenn die Datei-Streaming-URL fälschlicherweise in der OSD-Datei (Open Software Descriptor) festgesetzt ist, gibt der App-V-Client einen 1D1-Fehler zurück, anstatt einen Fehler "Datei nicht gefunden" zu finden. Dieser Fehler zeigt an, dass der Anwendungsstart fehlgeschlagen ist und der Benutzer in den Modus für getrennte Vorgänge gezwungen wurde. Korrigieren Sie die Datei-Streaming-URL.

## Mit einigen Anwendungen verknüpfte falsche Symbole


Wenn ein Symbol in einem Veröffentlichungsvorgang verwendet werden soll, ermittelt der App-V-Client zunächst, ob bereits eine zwischengespeicherte Kopie des Symbols vorhanden ist, indem im Symbolcache nach einem Element gesucht wird, dessen ursprünglicher Quellpfad dem Pfad des Symbols entspricht, das dem Veröffentlichungsvorgang zugewiesen ist. Wenn der App-V-Client eine Übereinstimmung findet, wird das bereits zwischengespeicherte Symbol verwendet. Andernfalls wird das neue Symbol in den Cache heruntergeladen. Wenn es sich bei dem Pfad zu dem Symbol um ein Scratch-Verzeichnis handelt oder wenn es für neue Symbole oder Pakete wieder verwendet wird, kann das Nachschlagen im Cache das falsche Symbol aus einem vorherigen Vorgang auswählen.

## Benutzer werden beim Starten einer Anwendung zur Eingabe von Anmeldeinformationen aufgefordert


Wenn ein Benutzer versucht, eine virtuelle Anwendung zu starten, auf die der System Administrator eingeschränkten Zugriff hat, wird der Benutzer möglicherweise zur Eingabe von Anmeldeinformationen aufgefordert. Der Benutzer sollte den Benutzernamen und das Kennwort für ein Konto eingeben, das über die Berechtigung zum Starten der Anwendung verfügt, und dann die EINGABETASTE drücken.

## Die Veröffentlichungsaktualisierung schlägt nach dem Upgrade des App-V-Clients auf Version 4,5 fehl


Wenn das Benutzerdatenverzeichnis zuvor an einem nicht standardmäßigen Speicherort (%*ALLUSERSPROFILE*%\\Documents\\SoftGrid Client\\Users\\%*username*%) gespeichert wurde, finden Benutzer, die nicht über Administratorrechte auf dem Computer verfügen, die Veröffentlichungsaktualisierung nach dem Upgrade des App-V-Clients fehlschlägt. Während des Upgrades werden das globale App-V-Client-Datenverzeichnis und alle zugehörigen Unterverzeichnisse mit eingeschränkten Zugriffsrechten für Administratoren konfiguriert. Sie können dieses Problem vermeiden, indem Sie das Benutzerdatenverzeichnis vor dem Upgrade ändern, sodass es sich nicht um ein Unterverzeichnis des globalen Datenverzeichnisses handelt.

## Neustart nach Installationsfehler erforderlich


Wenn die Clientinstallation aus irgendeinem Grund fehlschlägt und bei nachfolgenden versuchen, den Client zu installieren, ebenfalls fehlschlägt, überprüfen Sie das Windows Installer-Protokoll, um festzustellen, ob ein Fehler "sftplay Fehler, Fehler = 1072" angezeigt wird. Wenn dies der Fall ist, starten Sie den Computer neu, bevor Sie versuchen, den Client erneut zu installieren.

## Reparieren einer beschädigten virtuellen Anwendung


Wenn ein virtuelles Anwendungspaket, das mit einer MSI-Datei (Windows Installer-Paket) installiert wurde, beschädigt wird, installieren Sie es erneut. Mit der im Windows Installer verfügbaren Funktion reparieren werden die Benutzer-Volumes nicht aktualisiert.

## Verwandte Themen


[Application Virtualization Client-Referenz](application-virtualization-client-reference.md)

 

 





