---
title: Konfigurieren von erweiterten Einstellungen mit Windows PowerShell
description: Konfigurieren von erweiterten Einstellungen mit Windows PowerShell
author: dansimp
ms.assetid: 437a31cc-2a11-456f-b448-b0b869fb53f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a3ece3f76f6e982913aad2b25cfe0084542f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812328"
---
# Konfigurieren von erweiterten Einstellungen mit Windows PowerShell


Das von Ihnen erstellte Med-v-Arbeitsbereichs Paket enthält eine Windows PowerShell-Skriptdatei (ps1), die Sie bearbeiten können, bevor Sie Ihr Med-v-Arbeitsbereichs Paket testen und bereitstellen. Dieser Abschnitt enthält Informationen und Anleitungen, die Ihnen bei der Verwaltung von Med-v-Konfigurationseinstellungen mithilfe von Windows PowerShell helfen, bevor Sie die Med-v-Arbeitsbereiche bereitstellen.

## Verwenden von Windows PowerShell-Cmdlets in MED-V


Die folgenden Windows PowerShell-Cmdlets stehen in Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 zur Verfügung:

**Neu – MedvConfiguration**

**Export-MedvConfiguration**

**Neu – MedvWorkspace**

**Export-MedvWorkspace**

Wenn Sie auf Windows PowerShell-Cmdlets für med-v zugreifen möchten, öffnen Sie Windows PowerShell, und geben Sie den folgenden Befehl ein, um die Med-v-Module zu importieren.

``` syntax
Import-Module microsoft.medv
```

Nachdem die Module importiert wurden, können Sie mithilfe der Windows PowerShell-Standardhilfe Befehle **Mann** oder **Get-Help**auf die Inline Hilfe für die Cmdlets zugreifen. Wenn Sie beispielsweise auf eine Beschreibung des Cmdlets **New-MedvConfiguration** einschließlich einer vollständigen Liste der verfügbaren Parameter zugreifen möchten, geben Sie den folgenden Befehl ein.

``` syntax
get-help New-MedvConfiguration
```

Sie können auch Hilfe zu bestimmten Parametern anzeigen. Wenn Sie beispielsweise Hilfe für den Parameter VmMemory anzeigen möchten, geben Sie Folgendes ein:

``` syntax
get-help New-MedvConfiguration -parameter VmMemory
```

Um eine Liste aller MED-V-Konfigurationseinstellungen und deren Standardeinstellungen anzuzeigen, geben Sie den folgenden Befehl ein.

``` syntax
New-MedvConfiguration -ForceDefaults
```

Um eine Liste aller MED-V-Konfigurationseinstellungen und deren aktuellen Werte anzuzeigen, geben Sie den folgenden Befehl ein.

``` syntax
gwmi -Class "Setting” -Namespace "root/microsoft/medv”
```

## Erstellen eines MED-V-Arbeitsbereichs mit benutzerdefinierten Einstellungen


Nachdem Sie ein Med-v-Arbeitsbereichs Paket erfolgreich mithilfe des Med-v-Arbeitsbereichs-Packagers erstellt haben, wird ein Windows PowerShell-Skript in dem Ordner generiert, den Sie zum Speichern der Packager-Dateien angegeben haben. Der Inhalt dieses Skripts zeigt einige der verfügbaren MED-V-Konfigurationseinstellungen, die Sie bearbeiten können.

Mit den folgenden Schritten können Sie das Skript anpassen und es dann in Windows PowerShell ausführen, um einen MED-V-Arbeitsbereich mit den neuen Einstellungen zu erstellen.

**Wichtig**  Führen Sie Windows PowerShell mit administrativen Anmeldeinformationen aus, und stellen Sie sicher, dass die Windows PowerShell-Ausführungsrichtlinie die Ausführung von Skripts ermöglicht.

1.  Bearbeiten Sie das Windows PowerShell-Skript, das vom MED-V Workspace-Paket erstellt wurde, oder erstellen Sie ein neues Skript mit den gewünschten Konfigurationseinstellungen.

2.  Führen Sie Windows PowerShell mit administrativen Anmeldeinformationen aus, und geben Sie an der Eingabeaufforderung den folgenden Befehl ein.

    ``` syntax
    & “.\<workspacename>.ps1”
    ```

    Dieser Befehl führt das Windows PowerShell-Skript aus und führt das Cmdlet **New-MedvWorkspace** aus, um ein neues MED-V-Arbeitsbereichs Paket zu generieren. Die neuen Packager-Dateien werden in dem Ordner gespeichert, den Sie ursprünglich für das Speichern Ihrer MED-V Workspace-Paketdateien angegeben haben. Weitere Hilfe zu diesem Cmdlet finden Sie in der Hilfe zu Windows PowerShell.

 

## Exportieren einer MED-V-Konfiguration in eine Registrierungsdatei


Sie können die Med-v-Konfigurationseinstellungen aktualisieren, nachdem der Med-v-Arbeitsbereich installiert wurde. Verwenden Sie das Cmdlet **New-MedvConfiguration** , um die Parameter anzugeben, die Sie ändern möchten. Geben Sie beispielsweise die folgenden Befehle ein, um eine Registrierungsdatei zu erstellen, die die Speichereinstellung für den virtuellen Computer ändert.

``` syntax
New-MedvConfiguration  -VmMemory 1024 | Export-MedvConfiguration -Path c:\medvConfiguration\myConfig.reg
```

Sie können die resultierende Registrierungsdatei vom Hostcomputer in einen MED-V-Arbeitsbereich importieren, um die neuen Konfigurationseinstellungen anzuwenden.

## Verwandte Themen


[Verwalten von Konfigurationseinstellungen für MED-V-Arbeitsbereiche](managing-med-v-workspace-configuration-settings.md)

[Testen und Bereitstellen des MED-V-Arbeitsbereichspakets](test-and-deploy-the-med-v-workspace-package.md)

 

 





