---
title: High-Level-Architektur für UE-V 1.0
description: High-Level-Architektur für UE-V 1.0
author: dansimp
ms.assetid: d54f9f10-1a4d-4e56-802d-22d51646e1cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b54a9a207f9b74ad3d028cf4ab1f9842d59b0b3a
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910450"
---
# <a name="high-level-architecture-for-ue-v-10"></a>High-Level-Architektur für UE-V 1.0


In diesem Thema werden allgemeine Architekturelemente der Microsoft User Experience Virtualization (UE-V)-Roaminglösung beschrieben. Die folgenden Elemente sind Teil einer Standardbereitstellung UE-V.

![Architekturdiagramm des ue-v-Agents.](images/ue-vagentarchitecturaldiagram.gif)

Der UE-V-Agent überwacht die Anwendungen und Die Betriebssystemprozesse, wie sie in den Speicherortvorlagen für die UE-V-Einstellungen identifiziert werden. Wenn die Anwendung oder das Betriebssystem gestartet wird, werden die Einstellungen aus dem Einstellungspaket gelesen und auf den Computer angewendet. Wenn die Anwendung geschlossen wird oder das Betriebssystem gesperrt oder heruntergefahren wird, werden die Einstellungen in einem UE-V Einstellungspaket am Speicherort der Einstellungen gespeichert.

## <a name="settings-storage-location"></a>Einstellungen Speicherort


Der Speicherort der Einstellungen ist eine Dateifreigabe, auf die der User Experience Virtualization-Agent zugreift, um Einstellungen zu lesen und zu schreiben. Dieser Speicherort ist entweder das Active Directory-Startverzeichnis oder wird während der UE-V Installation definiert. Sie können den Speicherort während der Installation des UE-V-Agents oder später mit gruppenrichtlinien, WMI oder PowerShell festlegen. Der Speicherort kann sich auf einer beliebigen gemeinsamen Dateifreigabe befinden, auf die Benutzer zugreifen können. Wenn während der Installation kein Einstellungsspeicherort festgelegt ist, verwendet UE-V das Startverzeichnis in Active Directory. Der UE-V-Agent überprüft den Speicherort und erstellt einen Systemordner, der für den Benutzer ausgeblendet ist, in dem die Benutzereinstellungen gespeichert und darauf zugegriffen werden soll. Weitere Informationen zum Speicher von Einstellungen finden Sie unter [Vorbereiten der Umgebung für UE-V.](preparing-your-environment-for-ue-v.md)

## <a name="ue-v-agent"></a>UE-V Agent


Der UE-V-Agent wird auf jedem Computer mit Einstellungen installiert, die von user Experience Virtualization synchronisiert werden. Der Agent überwacht die registrierten Anwendungen und das Betriebssystem auf alle Änderungen, die an den Einstellungen vorgenommen werden, und synchronisiert diese Einstellungen zwischen Computern. Einstellungen werden vom Speicherort der Einstellungen auf die Anwendung angewendet, wenn die Anwendung gestartet wird. Die Einstellungen werden dann wieder am Speicherort der Einstellungen gespeichert, wenn die Anwendung geschlossen wird. Die Betriebssystemeinstellungen werden angewendet, wenn sich der Benutzer anmeldet, wenn der Computer entsperrt ist oder wenn der Benutzer mithilfe des Remotedesktopprotokolls (RDP) eine Remoteverbindung mit dem Computer herstellt. Der Agent speichert Einstellungen, wenn sich der Benutzer abmeldet, wenn der Computer gesperrt ist oder wenn eine Remoteverbindung getrennt wird. Weitere Informationen zum UE-V-Agent finden Sie unter [Vorbereiten Der Umgebung für UE-V](preparing-your-environment-for-ue-v.md).

## <a name="settings-location-templates"></a><a href="" id="bkmk-settingslocationtemplate"></a>Einstellungen Standortvorlagen


Die Einstellungsspeicherortvorlage ist eine XML-Datei, die die Von User Experience Virtualization zu überwachenden Einstellungsspeicherorte definiert. Nur die in diesen Einstellungsvorlagen definierten Einstellungsspeicherorte werden auf Computern erfasst oder angewendet, auf denen der UE-V-Agent ausgeführt wird. Die Einstellungsspeicherortvorlage enthält keine Einstellungswerte, nur die Speicherorte, an denen Werte auf dem Computer gespeichert sind.

UE-V enthält eine Reihe von Einstellungsspeicherortvorlagen, die Einstellungsspeicherorte für einige Microsoft-Anwendungen und Windows Einstellungen angeben. Ein Administrator kann benutzerdefinierte Einstellungsspeicherortvorlagen mithilfe des UE-V-Generators erstellen.

[Planen der Verwendung von Anwendungen zum Synchronisieren mit UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md)

[Planen der Bereitstellung von benutzerdefinierten Vorlagen für UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md)

[Arbeiten mit benutzerdefinierten UE-V-Vorlagen und dem UE-V-Generator](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

## <a name="settings-packages"></a>Einstellungen Pakete


Anwendungseinstellungen und Windows Einstellungen werden in Einstellungspaketen gespeichert, die vom UE-V-Agent erstellt werden. Ein Einstellungspaket ist eine Auflistung der Einstellungen, die in den Einstellungsspeicherortvorlagen dargestellt werden. Diese Einstellungspakete werden erstellt, lokal gespeichert und dann an den Speicherort der Einstellungen kopiert. "Letzter Schreibvorgang hat Vorrang" bestimmt, welche Einstellungen beibehalten werden, wenn ein einzelner Benutzer mehrere Computer mit einem Speicherort synchronisiert. Der Agent, der auf einem Computer ausgeführt wird, liest und schreibt unabhängig von Agents, die auf anderen Computern ausgeführt werden, in den Einstellungsspeicherort. Die zuletzt geschriebenen Einstellungen und Werte werden angewendet, wenn der nächste Agent vom Speicherort der Einstellungen liest.

![ue-v-Generatorprozess.](images/ue-vgeneratorprocess.gif)

## <a name="settings-template-catalog"></a>Einstellungen Vorlagenkatalog


Der Einstellungsvorlagenkatalog ist ein Ordnerpfad auf UE-V Computern oder eine SMB-Netzwerkfreigabe (Server Message Block), in der alle benutzerdefinierten Einstellungsspeicherortvorlagen gespeichert sind. Der UE-V-Agent ruft neue oder aktualisierte Vorlagen von diesem Speicherort ab. Der UE-V-Agent überprüft diesen Speicherort einmal täglich und aktualisiert sein Synchronisierungsverhalten basierend auf den Vorlagen in diesem Ordner. Die Vorlagen, die seit der letzten Überprüfung in diesem Ordner hinzugefügt oder aktualisiert wurden, werden vom UE-V-Agent registriert. Der UE-V-Agent deregistrierungsiert die Vorlagen, die aus diesem Ordner entfernt wurden. Vorlagen werden vom Aufgabenplaner einmal pro Tag registriert und nicht registriert. Wenn Sie nur die Standardeinstellungsspeicherortvorlagen verwenden, die in UE-V enthalten sind, ist kein Einstellungsvorlagenkatalog erforderlich. Weitere Informationen zu Einstellungsbereitstellungskatalogen finden Sie unter [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).

## <a name="user-experience-virtualization-generator"></a>User Experience Virtualization Generator


Mit dem User Experience Virtualization Generator können Sie benutzerdefinierte Einstellungsspeicherortvorlagen erstellen, in denen die Einstellungsspeicherorte der Anwendungen gespeichert werden, die im Unternehmen verwendet werden und die Sie in die Roamingeinstellungslösung einschließen möchten. Der UE-V-Generator sucht nach den Speicherorten von Registrierungswerten und den Einstellungsdateien für Anwendungen und zeichnet diese Speicherorte dann in einer XML-Datei mit Einstellungsspeicherortvorlagen auf. Sie können diese Einstellungsspeicherortvorlagen dann an die Benutzercomputer verteilen. Der UE-V-Generator ermöglicht es einem Administrator auch, eine vorhandene Vorlage zu bearbeiten oder eine Vorlage zu überprüfen, die mit einem anderen XML-Editor erstellt wurde.

Der UE-V-Generator überwacht eine Anwendung, um zu ermitteln und zu erfassen, wo sie ihre Einstellungen speichert. Zu diesem Zweck wird überwacht, wo die Anwendung in der Registrierung HKEY\_CURRENT\_USER oder in den Dateiordnern unter **"Benutzer** \\ \[Benutzername\] \\ **AppData**  \\  **Roaming und Benutzer** \\ \[Benutzername\] \\ **AppData**  \\  **Local"** liest oder schreibt.

Der Ermittlungsprozess schließt Registrierungsschlüssel und Dateien aus, in die der angemeldete Benutzer keine Werte schreiben kann. Keine dieser Dateien wird in der XML-Datei enthalten sein. Der Ermittlungsprozess schließt auch Registrierungsschlüssel und Dateien aus, die der Kernfunktionalität des Windows Betriebssystems zugeordnet sind.

Weitere Informationen zum UE-V-Generator finden Sie unter [Installing the UE-V Generator](installing-the-ue-v-generator.md).

## <a name="related-topics"></a>Verwandte Themen


[Microsoft-User Experience Virtualization (UE-V) 1.0](index.md)

[Erste Schritte mit User Experience Virtualization 1.0](getting-started-with-user-experience-virtualization-10.md)

[Informationen zu User Experience Virtualization 1.0](about-user-experience-virtualization-10.md)

[Arbeiten mit benutzerdefinierten UE-V-Vorlagen und dem UE-V-Generator](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

 

 





