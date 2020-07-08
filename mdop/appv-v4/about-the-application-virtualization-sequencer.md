---
title: Informationen über Application Virtualization Sequencer
description: Informationen über Application Virtualization Sequencer
author: dansimp
ms.assetid: bee193ca-58bd-40c9-b41a-310435633895
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 83709bcceabe3312fba34512b47d28a24b4dc52c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808131"
---
# Informationen über Application Virtualization Sequencer


Der Microsoft Application Virtualization (App-V)-Sequenzer überwacht und zeichnet alle Installations-und Einrichtungsprozesse für eine Anwendung auf und erstellt die folgenden Dateien: **ICO**, **OSD**, **SFT**und **SPRJ**. Diese Dateien enthalten alle erforderlichen Informationen zu einer Anwendung, damit die Anwendung in einer virtuellen Umgebung auf Zielcomputern ausgeführt werden kann. Sie können den Microsoft Application Virtualization (App-V)-Sequenzer verwenden, um virtuelle Anwendungen zu erstellen. Nachdem Sie eine Anwendung sequenziert haben, kann Sie auf Zielcomputer gestreamt werden, oder die virtuelle Anwendung kann von Zielcomputern ausgeführt werden, indem der Inhalt des virtuellen Anwendungspakets heruntergeladen und die Anwendung lokal ausgeführt wird.

**Wichtig**  Zum Ausführen eines virtuellen Anwendungspakets muss auf dem Zielcomputer die entsprechende Version des App-V-Clients ausgeführt werden.

 

Virtuelle Anwendungspakete werden auf Zielcomputern ausgeführt, ohne mit dem zugrunde liegenden Betriebssystem auf dem Zielcomputer zu interagieren, da jede Anwendung in einer virtuellen Umgebung ausgeführt wird und von anderen Anwendungen isoliert ist, die auf dem Zielcomputer installiert oder ausgeführt werden. Durch diese Isolierung können Anwendungskonflikte verringert und die erforderliche Anzahl von Anwendungstests vor der Bereitstellung verringert werden.

## Sequenzer-Terminologie


<a href="" id="application-virtualization-drive"></a>Application Virtualization-Laufwerk  
Das Application Virtualization Drive ist das Standardlaufwerk (Laufwerk q:\) auf dem Zielcomputer, aus dem sequenzierte Anwendungen ausgeführt werden.

<a href="" id="ico-file"></a>ICO-Datei  
Die Symboldatei auf dem Clientdesktop, die zum Starten einer sequenzierten Anwendung verwendet wird.

<a href="" id="installation-directory"></a>Installationsverzeichnis  
Das Verzeichnis, das vom Sequencer zum Platzieren von Installationsdateien während des Setups verwendet wird.

<a href="" id="open-software-descriptor--osd--file"></a>Open Software Descriptor (OSD)-Datei  
Eine XML-basierte Datei, in der der APP-v-Client angewiesen wird, wie die sequenzierte Anwendung vom APP-v-Streamingserver abgerufen und wie die sequenzierte Anwendung in der virtuellen Umgebung ausgeführt werden soll.

<a href="" id="package-root-directory"></a>Paketstammverzeichnis  
Das Verzeichnis auf dem Sequenzcomputer, auf dem die Dateien für das sequenzierte Anwendungspaket installiert sind. Dieses Verzeichnis ist auch virtuell auf dem Computer vorhanden, auf den eine sequenzierte Anwendung gestreamt wird.

<a href="" id="sequenced-application"></a>Sequenzierte Anwendung  
Eine Anwendung, die vom Sequencer überwacht wurde, aufgeteilt in primäre und sekundäre Funktionsblöcke, gestreamt auf einem Zielcomputer, auf dem der App-V-Client t ausgeführt wird, und führt eine virtuelle Umgebung aus.

<a href="" id="sequenced-application-package"></a>Sequenziertes Anwendungspaket  
Die Dateien, die eine virtuelle Anwendung enthalten und die Ausführung einer virtuellen Anwendung ermöglichen. Diese Dateien werden nach der Sequenzierung erstellt und umfassen insbesondere **OSD**-, **SFT**-, **SPRJ**-und **ICO** -Dateien.

<a href="" id="sequencing"></a>Sequenzierung  
Der Vorgang zum Erstellen eines Anwendungspakets mit dem App-V-Sequenzer. In diesem Prozess wird eine Anwendung überwacht, Ihre Tastenkombinationen konfiguriert und ein sequenziertes Anwendungspaket erstellt.

<a href="" id="sequencing-computer"></a>Sequenzcomputer  
Der Computer, mit dem eine Anwendung sequenziert wird.

<a href="" id="virtual-application"></a>Virtuelle Anwendung  
Eine vom Sequencer verpackte Anwendung, die in einer eigenständigen virtuellen Umgebung ausgeführt werden soll. Die virtuelle Umgebung enthält die Informationen, die erforderlich sind, um die Anwendung auf dem Client auszuführen, ohne die Anwendung lokal zu installieren.

<a href="" id="primary-feature-block"></a>Primärer Feature-Block  
Der minimale Inhalt eines virtuellen Anwendungspakets, das für die Ausführung einer Anwendung auf einem Zielcomputer erforderlich ist. Der Inhalt des primären Funktionsblocks wird während der Anwendungsphase der Sequenzierung identifiziert und besteht in der Regel aus dem Inhalt der am häufigsten verwendeten Anwendungsfeatures.

## <a href="" id="sequencing-applications-"></a>Sequenzierung von Anwendungen


Es gibt zwei Methoden zum Erstellen und Ändern von virtuellen Anwendungspaketen in Ihrer Umgebung. Die erste Methode ist die Verwendung des **Sequenz** -Assistenten. Mit dem **Sequenz** -Assistenten können Sie neue, vorhandene virtuelle Anwendungspakete erstellen oder ändern. Weitere Informationen zur Verwendung des **Sequenz** -Assistenten finden Sie unter [so wird es gemacht: Sequenzierung einer neuen Anwendung](how-to-sequence-a-new-application.md). Die zweite Methode ist die Verwendung der Befehlszeile. Über die Befehlszeile können Sie mit der Eingabeaufforderung neue, vorhandene virtuelle Anwendungspakete erstellen oder ändern. Weitere Informationen zur Verwendung der Befehlszeile finden Sie unter [Verwalten virtueller Anwendungen über die Befehlszeile](how-to-manage-virtual-applications-using-the-command-line.md).

Der **Sequenz** -Assistent bietet die folgenden Funktionen zum Erstellen virtueller Anwendungspakete:

1.  **Paketkonfiguration**: der **Sequenz** -Assistent fordert zum Ausführen der OSD-Datei (Open Software Descriptor) Informationen zur Paketkonfiguration auf, bei der es sich um eine erforderliche Datei zum Starten eines sequenzierten Anwendungspakets handelt.

2.  **Anwendungsinstallation**: der **Sequenz** -Assistent sammelt Informationen zu den Installations-und Startkonfigurationen einer Anwendung. Es überwacht und zeichnet die Installations-und Startinformationen auf, die mit der Anwendung verknüpft sind, um die Dateien zu erstellen, die für ein virtuelles Anwendungspaket erforderlich sind.

3.  **Anwendungsstart**: der **Sequenz** -Assistent sammelt Informationen zum Kompilieren und Sortieren der Codeblöcke, die erforderlich sind, um den ersten Start des sequenzierten Anwendungspakets auf dem Zielcomputer durchzuführen. Die Kompilierung des Codeblocks wird als primärer Feature-Block bezeichnet.

## Sicherheitsüberlegungen zu Application Virtualization Sequencer


Der App-V-Sequencer führt alle Dienste, die zur Sequenzierung erkannt werden, unter Verwendung des lokalen System Kontos aus, und es werden keine Sicherheitsbeschreibungen für Dienststeuerungsanforderungen erzwungen. Wenn der Dienst mit einem anderen Benutzerkonto installiert wurde oder wenn die Sicherheitsbeschreibungen anderen Benutzergruppen bestimmte Dienstberechtigungen erteilen sollen, sollten Sie sorgfältig überlegen, ob der Dienst virtualisiert werden soll. In einigen Fällen sollten Sie den Dienst lokal installieren, um sicherzustellen, dass die vorgesehene Dienstsicherheit erhalten bleibt.

**Wichtig**  Sie sollten virtuelle Anwendungspakete immer an einem sicheren Ort speichern.

 

## Verwandte Themen


[Application Virtualization Sequencer – Übersicht](application-virtualization-sequencer-overview.md)

 

 





