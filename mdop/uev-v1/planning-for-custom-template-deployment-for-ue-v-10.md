---
title: Planen der Bereitstellung von benutzerdefinierten Vorlagen für UE-V 1.0
description: Planen der Bereitstellung von benutzerdefinierten Vorlagen für UE-V 1.0
author: dansimp
ms.assetid: be76fc9a-31ca-4290-af11-7640dcb87d50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d17f058bff452f88003ab4488daa7afa846f688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808608"
---
# Planen der Bereitstellung von benutzerdefinierten Vorlagen für UE-V 1.0


Microsoft User Experience Virtualization (UE-v) verwendet Einstellungen-Standort Vorlagen (XML-Dateien), die die Einstellungen definieren, die von UE-v erfasst und angewendet werden. Sie können den UE-v-Generator verwenden, um benutzerdefinierte Standort Vorlagen für Einstellungen zu erstellen, mit denen Benutzer die Einstellungen anderer Anwendungen als die in den Standard-UE-V-Vorlagen enthaltenen Einstellungen durchlaufen können. Nachdem Sie die benutzerdefinierte Vorlage getestet haben, um sicherzustellen, dass die Anwendungseinstellungen in einer Testumgebung ordnungsgemäß durchlaufen, können Sie diese Einstellungen Speicherort Vorlagen auf Computern im Unternehmen bereitstellen.

Sie können die Speicherort Vorlagen für benutzerdefinierte Einstellungen mit einer vorhandenen Bereitstellungsinfrastruktur wie Enterprise Software Distribution (ESD), Gruppenrichtlinieneinstellungen oder durch Konfigurieren eines UE-V-Einstellungs Vorlagen Katalogs bereitstellen. Vorlagen, die mithilfe von ESD-oder Gruppenrichtlinien bereitgestellt werden, müssen bei UE-V WMI oder PowerShell registriert sein.

## Vorlagenkatalog für Einstellungen


Der Katalog der Benutzeroberflächen-Virtualisierungs-Einstellungen ist ein Ordnerpfad auf UE-V-Computern oder eine SMB-Netzwerkfreigabe (Server Message Block), in der alle Speicherorte für benutzerdefinierte Einstellungen gespeichert sind. Der UE-V-Agent ruft neue oder aktualisierte Vorlagen von diesem Speicherort ab. Der UE-V-Agent überprüft diesen Speicherort einmal täglich und aktualisiert sein Synchronisierungsverhalten basierend auf den Vorlagen in diesem Ordner. Vorlagen, die seit dem letzten Überprüfen des Ordners in diesem Ordner hinzugefügt oder aktualisiert wurden, werden vom UE-V-Agent registriert. Der UE-V-Agent hebt die Registrierung von Vorlagen auf, die aus diesem Ordner entfernt wurden. Standardmäßig werden Vorlagen um 3:30 Uhr einmal pro Tag registriert und nicht registriert. Ortszeit durch den Aufgabenplaner. Weitere Informationen zu den UE-v-Aufgaben finden Sie unter [Ändern der Häufigkeit von geplanten UE-v-Aufgaben](changing-the-frequency-of-ue-v-scheduled-tasks.md).

Sie können den Katalogpfad der Einstellungs Vorlage mithilfe der Befehlszeilenoptionen "installieren", "Gruppenrichtlinie", "WMI" oder "PowerShell" konfigurieren. Vorlagen, die im Katalogpfad für Einstellungs Vorlagen gespeichert sind, werden automatisch von einem geplanten Vorgang registriert und nicht registriert. Sie können diesen geplanten Task nach Bedarf anpassen.

## Ersetzen der standardmäßigen Microsoft-Vorlagen


Der UE-V-Agent installiert eine Standardgruppe von Einstellungen-Standort Vorlagen für allgemeine Microsoft-Anwendungen und Windows-Einstellungen. Wenn Ihr Unternehmen angepasste Versionen dieser Vorlagen benötigt, kann der UE-V-Agent so konfiguriert werden, dass ein Einstellungs Vorlagenkatalog verwendet wird, und Sie sollten die standardmäßigen Microsoft-Vorlagen ersetzen.

Während der Installation des UE-V-Agents kann der Befehlszeilenparameter `RegisterMSTemplates` verwendet werden, um die Registrierung der Microsoft-Standardvorlagen zu deaktivieren. Weitere Informationen zum Einrichten der UE-v-Parameter finden Sie unter [Planen der UE-v-Konfigurationsmethoden](planning-for-ue-v-configuration-methods.md).

Wenn Sie Gruppenrichtlinien zum Konfigurieren des Katalog Pfads für Einstellungs Vorlagen verwenden, können Sie auswählen, dass die standardmäßigen Microsoft-Vorlagen ersetzt werden sollen. Wenn Sie die Richtlinieneinstellungen so konfigurieren, dass die standardmäßigen Microsoft-Vorlagen ersetzt werden, werden alle Microsoft-Standardvorlagen, die vom UE-V-Agent installiert werden, auf dem Computer gelöscht, und es werden nur die Vorlagen verwendet, die sich im Katalog der Einstellungs Vorlagen befinden. Um die standardmäßige Microsoft-Vorlage außer Kraft setzen zu können, muss die Konfigurationseinstellung UE-V-Agent `RegisterMSTemplates` auf true festgelegt sein.

**Hinweis**  Wenn Sie diese Richtlinieneinstellung nach der Aktivierung deaktivieren, wird der UE-V-Agent die standardmäßigen Microsoft-Vorlagen nicht wiederherstellen.

 

Wenn im Einstellungs Vorlagenkatalog angepasste Vorlagen vorhanden sind, die die gleiche ID wie die standardmäßigen Microsoft-Vorlagen verwenden und der UE-V-Agent nicht so konfiguriert ist, dass die standardmäßigen Microsoft-Vorlagen ersetzt werden, werden die Microsoft-Vorlagen im Katalog ignoriert.

Sie können die Standardvorlagen auch mithilfe der Features UE-V PowerShell ersetzen. Wenn Sie die standardmäßige Microsoft-Vorlage durch PowerShell ersetzen möchten, heben Sie die Registrierung aller Microsoft-Standardvorlagen auf, und registrieren Sie dann die angepassten Vorlagen.

**Hinweis**  Alte Einstellungs Pakete verbleiben im Einstellungs Speicherort, auch wenn neue Einstellungs Vorlagen für eine Anwendung bereitgestellt werden. Diese Pakete werden nicht vom Agenten gelesen, aber auch nicht automatisch gelöscht.

 

## Verwandte Themen


[Planen für UE-V 1.0](planning-for-ue-v-10.md)

[Planen der Verwendung von Anwendungen zum Synchronisieren mit UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md)

[Planen für UE-V-Konfigurationsmethoden](planning-for-ue-v-configuration-methods.md)

Planen der Bereitstellung von benutzerdefinierten Vorlagen
 

 





