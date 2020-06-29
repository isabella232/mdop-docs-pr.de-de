---
title: Sicherheitsüberlegungen zu DaRT 10
description: Sicherheitsüberlegungen zu DaRT 10
author: dansimp
ms.assetid: c653daf1-f12a-4667-98cc-f0c89fa38e3f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f10ecf81021d41fbc08b288573c05a8d64c47d7c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809724"
---
# Sicherheitsüberlegungen zu DaRT 10


Dieses Thema enthält eine kurze Übersicht über die Konten und Gruppen, Protokolldateien und andere sicherheitsrelevante Überlegungen für Microsoft Diagnostics and Recovery Toolset (Dart) 10. Weitere Informationen finden Sie unter den Links in diesem Artikel.

## Allgemeine Sicherheitsüberlegungen


Grund **Legendes zu den Sicherheitsrisiken** Dart 10 enthält Funktionen, mit denen ein Administrator oder ein Helpdesk-Mitarbeiter die Dart-Tools Remote ausführen kann, um Probleme auf einem Endbenutzercomputer zu beheben. Darüber hinaus können Sie das Image der internationalen Organisation für Standardisierung (ISO) auf einem USB-Flashlaufwerk speichern oder das ISO-Abbild in ein Netzwerk setzen, um dessen Inhalt als Wiederherstellungspartition auf der Festplatte eines Computers einzuschließen. Diese Funktionen bieten Flexibilität, aber auch potenzielle Sicherheitsrisiken, die bei der Konfiguration von DART berücksichtigt werden sollten.

**Physisches sichern ihrer Computer**. Wenn Administratoren und Helpdesk-Mitarbeiter nicht physisch an ihren Computern sind, sollten Sie Ihre Computer sperren und einen sicheren Bildschirmschoner verwenden.

**Wenden Sie die neuesten Sicherheitsupdates auf alle Computer an**. Bleiben Sie über neue Updates für Betriebssysteme auf dem laufenden, indem Sie den Security Notification Service ( <https://go.microsoft.com/fwlink/?LinkId=28819> ) abonnieren.

## Einschränken des Endbenutzerzugriffs auf DART-Tools


Wenn Sie das DART-Wiederherstellungsbild erstellen, können Sie die Tools auswählen, die Sie einbeziehen möchten. Aus Sicherheitsgründen ist es möglicherweise sinnvoll, den Endbenutzer Zugriff auf die leistungsstärkeren Dart-Tools wie Datenträger Zurücksetzung und Schlosser zu beschränken. In DART 10 können Sie bestimmte Tools während der Konfiguration deaktivieren und diese weiterhin den Helpdesk-Mitarbeitern zur Verfügung stellen, wenn der Endbenutzer das Remote Verbindungs Feature startet.

Sie können das DART-Bild sogar so konfigurieren, dass die Option zum Starten einer Remote Verbindungssitzung das einzige Tool ist, das einem Endbenutzer zur Verfügung steht.

**Wichtig**  Nachdem die Remoteverbindung hergestellt wurde, werden alle Tools, die Sie in das Wiederherstellungsabbild aufgenommen haben, einschließlich der für den Endbenutzer nicht verfügbaren Tools, für alle Helpdesk-Mitarbeiter zur Verfügung gestellt, die am Endbenutzercomputer arbeiten.

 

Weitere Informationen zum Einbeziehen von Tools in das DART-Wiederherstellungsbild finden Sie unter [Übersicht über die Tools in DART 10](overview-of-the-tools-in-dart-10.md).

## Sichern des DART-Wiederherstellungs Bilds


Wenn Sie das DART-Wiederherstellungsabbild bereitstellen, indem Sie es auf einem USB-Stick oder durch Erstellen einer Remotepartition oder einer Wiederherstellungspartition speichern, möchten Sie möglicherweise die bevorzugte Methode für die Laufwerkverschlüsselung Ihres Unternehmens auf der ISO-Datei angeben. Das Verschlüsseln der ISO-Datei hilft, sicherzustellen, dass Endbenutzer DART-Funktionen nicht verwenden können, wenn Sie Zugriff auf das Wiederherstellungsabbild erhalten, und es wird sichergestellt, dass nicht autorisierte Benutzer in DART auf Computern booten können, die einer anderen Person angehören. Wenn Sie eine Verschlüsselungsmethode verwenden, stellen Sie sicher, dass Sie auf allen Computern bereitgestellt und aktiviert ist.

**Hinweis**  Dart 10 unterstützt BitLocker nativ.

 

Wenn Sie die Laufwerkverschlüsselung einbeziehen möchten, fügen Sie die Verschlüsselungs Projektmappendateien hinzu, wenn Sie das Wiederherstellungsabbild erstellen. Ihre Verschlüsselungslösung muss auf WinPE ausgeführt werden können. Endbenutzer, die von der ISO-Datei booten, können dann auf diese Verschlüsselungslösung zugreifen und das Laufwerk freigeben.

## Verwalten der Sicherheit zwischen zwei Computern, wenn Sie eine Remote Verbindung verwenden


Standardmäßig ist die Kommunikation zwischen zwei Computern, die eine **Remote Verbindungs** Sitzung eingerichtet haben, möglicherweise nicht verschlüsselt. Um die Sicherheit zwischen den beiden Computern zu gewährleisten, empfehlen wir daher, dass beide Computer Teil desselben Netzwerks sind.

## Verwandte Themen


[Sicherheit und Datenschutz für DaRT 10](security-and-privacy-for-dart-10.md)

 

 





