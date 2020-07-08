---
title: Sicherheitsüberlegungen zu DaRT 7.0
description: Sicherheitsüberlegungen zu DaRT 7.0
author: dansimp
ms.assetid: 52ad7e6c-c169-4ba4-aa76-56335a585eb8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 739c0319195aeb26e38d55ffe01d14b623de7f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809532"
---
# Sicherheitsüberlegungen zu DaRT 7.0


Microsoft Diagnostics and Recovery Toolset (Dart) 7 enthält Funktionen, mit denen ein Administrator die Dart-Tools Remote ausführen kann, um Probleme auf einem Endbenutzercomputer zu beheben. In früheren Versionen von DART musste sich ein Helpdesk-Techniker oder Administrator physisch auf einem Endbenutzercomputer befinden und mit der CD oder DVD, die das DART-Wiederherstellungsbild enthielt, in DART Booten. Nun kann der Helpdesk-Techniker oder Administrator die gleichen Verfahren Remote durchführen.

Darüber hinaus können Sie in DaRT7 neben dem Brennen einer CD oder DVD nun auch das Image der internationalen Organisation für Standardisierung (ISO) auf einem USB-Stick speichern. Sie können das ISO-Abbild auch in einem Netzwerk speichern oder seinen Inhalt als Wiederherstellungspartition auf einer Festplatte des Computers einfügen.

Mit der Funktion **Remote Verbindung** in DaRT7 können Endbenutzer auf DART zugreifen, indem Sie eine der folgenden neuen Bereitstellungsmethoden verwenden. Daher können Sie Dart einfacher starten und auf die Dart-Tools zugreifen.

Die neuen Funktionen in DaRT7 bieten viel mehr Flexibilität bei der Verwendung von Dart in Ihrem Unternehmen. Sie erstellen jedoch auch einen eigenen Satz von Sicherheitsproblemen, die behoben werden müssen. Wir empfehlen, beim Konfigurieren von DART die folgenden Sicherheitstipps zu bedenken.

## So gewährleisten Sie die Sicherheit beim Erstellen des DART-Wiederherstellungs Bilds


Wenn Sie das DART-Wiederherstellungsbild erstellen, können Sie die Tools auswählen, die Sie einbeziehen möchten. Aus Sicherheitsgründen ist es möglicherweise sinnvoll, den Endbenutzer Zugriff auf die leistungsstärkeren Dart-Tools wie Datenträger Zurücksetzung und Schlosser zu beschränken. In DaRT7 können Sie bestimmte Tools während der Konfiguration deaktivieren und diese weiterhin für Helpdesk-Agents verfügbar machen, wenn der Endbenutzer das Remote Verbindungs Feature startet.

Sie können das DART-Bild sogar so konfigurieren, dass die Option zum Starten einer Remote Verbindungssitzung das einzige Tool ist, das einem Endbenutzer zur Verfügung steht.

**Wichtig**  Nachdem die Remoteverbindung hergestellt wurde, werden alle Tools, die Sie in das Wiederherstellungsabbild aufgenommen haben, einschließlich der für den Endbenutzer nicht verfügbaren Tools, dem Helpdesk-Mitarbeiter zur Verfügung stehen, der auf dem Endbenutzercomputer arbeitet.

 

Weitere Informationen zum Einschließen von Tools in das DART-Wiederherstellungsabbild finden Sie unter [Verwenden des DART-Wiederherstellungsbild-Assistenten zum Erstellen des Wiederherstellungs](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md)Abbilds.

## So gewährleisten Sie die Sicherheit durch Verschlüsseln des DART-Wiederherstellungs Bilds


Wenn Sie eine der in DaRT7 neuen Bereitstellungsoptionen verwenden, beispielsweise das Speichern auf einem USB-Flashlaufwerk oder das Erstellen einer Remotepartition oder einer Wiederherstellungspartition, können Sie die bevorzugte Methode für die Laufwerkverschlüsselung Ihres Unternehmens auf der ISO-Datei angeben. Dadurch wird sichergestellt, dass ein Endbenutzer die Funktionalität von DART nicht verwenden kann, wenn er Zugriff auf das Wiederherstellungsabbild erhält. Außerdem wird sichergestellt, dass nicht autorisierte Benutzer in DART auf Computern booten können, die einer anderen Person gehören.

Ihre Verschlüsselungsmethode sollte auf allen Computern bereitgestellt und aktiviert sein.

**Hinweis**  DaRT7 unterstützt BitLocker nativ.

 

## So gewährleisten Sie die Sicherheit zwischen zwei Computern während der Remote Verbindung


Standardmäßig ist die Kommunikation zwischen zwei Computern, die eine **Remote Verbindungs** Sitzung eingerichtet haben, möglicherweise nicht verschlüsselt. Um die Sicherheit zwischen den beiden Computern zu gewährleisten, empfehlen wir daher, dass beide Computer Teil desselben Netzwerks sind.

## Verwandte Themen


[Vorgänge für DaRT 7.0](operations-for-dart-70-new-ia.md)

 

 





