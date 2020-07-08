---
title: Versionshinweise für DaRT 7.0
description: Versionshinweise für DaRT 7.0
author: dansimp
ms.assetid: fad227d0-5c22-4efd-9187-0e5922f7250b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5114acfe5a46a2c78f722a2bb6394c0dbef55dd4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809550"
---
# Versionshinweise für DaRT 7.0


**Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.**

Lesen Sie diese Versionshinweise gründlich, bevor Sie Microsoft Diagnostics and Recovery Toolset (Dart) 7 installieren.

## Informationen zu Microsoft Diagnostics and Recovery Toolset 7,0


Diese Versionshinweise enthalten Informationen, die zur erfolgreichen Installation von DaRT7 erforderlich sind, und enthalten Informationen, die in der Produktdokumentation nicht zur Verfügung stehen. Wenn es einen Unterschied zwischen diesen Versionshinweisen und anderer Dart-Plattformdokumentation gibt, sollte die neueste Änderung als autorisierend angesehen werden. Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.

## Informationen zur Produktdokumentation


Die Dokumentation für Microsoft Diagnostics and Recovery Toolset (Dart) 7 wird mit dem Produkt und der Connect-Website ausgeliefert.

Ausführliche Informationen zur Verwendung der Tools in DaRT7 finden Sie in der Hilfedatei, die im Menü " **Diagnose-und Wiederherstellungs-Toolset** " verfügbar ist.

## Abgeben von Feedback


Wir sind an Ihrem Feedback zu DaRT7 interessiert. Sie können Ihr Feedback an dart7feedback@Microsoft.com senden. Diese e-Mail-Adresse ist kein Supportkanal, aber Ihr Feedback hilft uns bei der Planung zukünftiger Änderungen für diese Tools, damit Sie in Zukunft noch nützlicher sind.

## Schutz vor Sicherheitsrisiken und Viren


Wir empfehlen, dass Sie die neuesten verfügbaren Sicherheitsupdates für jede neue Software installieren, die installiert werden soll, um den Schutz vor Sicherheitsrisiken und Viren zu gewährleisten. Weitere Informationen finden Sie unter [Microsoft-Sicherheit](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Bekannte Probleme mit Dart 7,0


### SFC-Scan kann nicht gestartet werden, wenn Standalone-System Sweeper geöffnet ist

Wenn das Standalone-System Sweeper ausgeführt wird, kann der SFC-Scan aufgrund eines Ressourcenkonflikts zwischen den beiden Tools nicht gestartet oder ausgeführt werden.

**Problemumgehung:** Schließen Sie das Standalone-System Sweeper, bevor Sie versuchen, das SFC-Scan-Tool zu öffnen oder auszuführen.

### Unicode-Zeichen werden möglicherweise nicht in Dateinamen angezeigt

Wenn Sie eine Datei löschen, deren Dateinamen Unicode-Zeichen enthält, und versuchen Sie, die Datei mithilfe des Tools zur Datei Wiederherstellung wiederherzustellen, wird die Datei nicht gefunden. Dies tritt nur auf, wenn Sie Zeichen aus einer anderen Sprache als der Sprache der Windows-DVD verwenden, die zum Erstellen des Wiederherstellungs Bilds verwendet wurde.

**Problemumgehung:** Stellen Sie sicher, dass die von DART verwendete Sprache mit der Sprache übereinstimmt, die von dem Betriebssystem verwendet wird, aus dem Sie Dateien wiederherstellen möchten.

### Die Dart-Befehlszeileninstallation kann nicht automatisch ausgeführt werden

Die Dart-Befehlszeileninstallation schlägt im Hintergrund fehl, wenn Sie mit der Option "Ruhemodus" ausgeführt wird, es sei denn, Sie wird mithilfe von erhöhten Administratorberechtigungen ausgeführt.

**Problemumgehung:** Führen Sie die Befehlszeileninstallation mithilfe von erhöhten Administratorberechtigungen aus. Die Dart-Installation unterstützt die typischen Windows Installer-Optionen für die Befehlszeileninstallation. Weitere Informationen zu den verschiedenen verfügbaren Schaltern finden Sie unter [Befehlszeilenoptionen](https://go.microsoft.com/fwlink/?LinkId=160689) für Windows Installer.

### Dateisuche kann einen Ordner nicht auf ein anderes Volume verschieben

Das Verschieben von Ordnern zwischen Volumes wird von der Datei Suchanwendung nicht unterstützt. Wenn Sie versuchen, einen Ordner in der Dateisuche auf ein anderes Volume zu verschieben, wird der folgende Fehler zurückgegeben: "beim Schreiben des Datei * &lt; namens &gt; *ist ein Fehler aufgetreten. Stellen Sie sicher, dass das Laufwerk über genügend Speicherplatz verfügt und der Zielpfad barrierefrei ist. "

**Problemumgehung:** Verwenden Sie den Explorer, um einen Ordner auf ein anderes Volume zu verschieben.

### Einige Daten sind möglicherweise nicht auf Computern verfügbar, auf denen die Laufwerkbuchstaben neu zugeordnet werden.

Dieses Problem kann auf BitLocker-aktivierten Computern und Multiboot-Computern auftreten. Dies tritt auf, weil einige Informationen in der Offlineregistrierung fest codierte Laufwerkbuchstaben aufweisen und Dart für dieselben Volumes verschiedene Buchstaben verwendet. Typische Effekte sind, dass Sie im Registrierungs-Editor keinen Zugriff auf bestimmte lokale Benutzerkonten haben. Darüber hinaus sind einige Tools möglicherweise nicht in der Lage, Eigenschaften abzurufen, die auf das Auflösen von Dateipfaden beruhen.

**Problemumgehung:** Verwenden Sie die Option, um die Laufwerkbuchstaben beim Start von DART neu zuzuordnen. Dies richtet normalerweise die typischen Laufwerksbuchstaben an das erwartete aus.

### Hotfix-Deinstallation kann bestimmte Updates nicht deinstallieren

Einige Updates und Service Packs können nicht deinstalliert werden, da Sie als nicht installierbar gekennzeichnet sind oder aus Windows 7 heraus deinstalliert werden müssen. In diesen Fällen kann das Hotfix-Deinstallationstool darauf hindeuten, dass diese Updates deinstalliert wurden, auch wenn dies nicht der Fall war.

**Problemumgehung:** Deinstallieren Sie diese problematischen Updates von Windows 7.

### Datenträgerbereinigung: Datenträger mit übergreifenden Volumes, Stripeset-Volumes oder gespiegelten Volumes können nicht gelöscht werden.

Die Datenträgerbereinigung unterstützt nicht das Löschen von Datenträgern, die über ein oder mehrere Volumes übergreifend, gespiegelt oder gestreift sind.

**Problemumgehung:** Wählen Sie die einzelnen Datenträger im Volume separat aus, und löschen Sie Sie.

## Anmerkungen zu dieser Version Copyright-Informationen


Dieses Dokument wird "as-is" bereitgestellt. Informationen und Ansichten, die in diesem Dokument zum Ausdruck kommen, sowie URLs und andere Verweise auf Internetwebsites können ohne Vorankündigung geändert werden. Das Risiko der Nutzung dieser Informationen liegt beim Benutzer.

Einige hier dargestellte Beispiele werden nur zur Illustration bereitgestellt und sind fiktiv.Es ist keine wirkliche Zuordnung oder Verbindung vorgesehen oder sollte abgeleitet werden.

Dieses Dokument stellt Ihnen keinerlei Rechte am geistigen Eigentum eines beliebigen Microsoft-Produkts zur Verfügung. Dieses Dokument ist vertraulich und für Microsoft proprietär. Sie werden offen gelegt und können nur gemäß einer Vertraulichkeitsvereinbarung verwendet werden.



Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, Windows Server und Windows Vista sind Marken der Microsoft-Unternehmensgruppe.

Alle anderen Marken sind Eigentum ihrer jeweiligen Eigentümer.

## Verwandte Themen


[Informationen zu DaRT 7.0](about-dart-70-new-ia.md)

 

 





