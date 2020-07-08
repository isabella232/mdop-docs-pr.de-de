---
title: Erstellen von UE-V-Einstellungsortvorlagen mit UE-V-Generator
description: Erstellen von UE-V-Einstellungsortvorlagen mit UE-V-Generator
author: dansimp
ms.assetid: b8e50e2f-0cc6-4f74-bb48-c471fefdc7d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ef7e3e5d00a95b9fcfc426207ce04f928cc0ebbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811878"
---
# Erstellen von UE-V-Einstellungsortvorlagen mit UE-V-Generator


Microsoft User Experience Virtualization (UE-V) verwendet *Einstellungen für Standort Vorlagen* , um Anwendungseinstellungen zwischen Benutzercomputern zu durchlaufen. Einige Standardeinstellungen für Standort Vorlagen sind in der Virtualisierung der Benutzeroberfläche enthalten. Sie können mit dem UE-V-Generator auch benutzerdefinierte Standort Vorlagen erstellen, bearbeiten oder überprüfen.

Der UE-V-Generator überwacht eine Anwendung, um die Speicherorte, an denen die Anwendung Ihre Einstellungen speichert, zu ermitteln und zu erfassen. Die Anwendung, die überwacht wird, muss eine herkömmliche Anwendung sein. Der UE-V-Generator kann keine Vorlage für eine Einstellungsposition aus den folgenden Anwendungstypen erstellen:

-   Virtualisierte Anwendungen

-   Über die Terminaldienste angebotene Anwendung

-   Java-Anwendungen

-   Windows 8-Anwendungen

**Hinweis**  UE-V-Vorlagen können nicht aus virtualisierten Anwendungen oder Terminaldienste-Anwendungen erstellt werden. Einstellungen, die mithilfe der Vorlagen synchronisiert werden, können jedoch auf diese Anwendungen angewendet werden. Öffnen Sie zum Erstellen von Vorlagen, die die Virtual Desktop Infrastructure (VDI)-und Terminaldienste-Anwendungen unterstützen, eine Windows Installer-Datei (MSI)-Version der Anwendung mit dem UE-V-Generator.

 

**Ausgeschlossene Speicherorte**

Der Ermittlungsprozess schließt Speicherorte aus, die häufig Anwendungssoftware Dateien speichern, die nicht gut zwischen Benutzercomputern oder Umgebungen gespeichert sind. Folgende Punkte sind ausgeschlossen:

-   HKEY \ _CURRENT \ _User Registrierungsschlüssel und Dateien, für die der angemeldete Benutzer keine Werte schreiben kann

-   HKEY \ _CURRENT \ _User Registrierungsschlüssel und Dateien, die der Kernfunktionalität des Windows-Betriebssystems zugeordnet sind

-   Alle Registrierungsschlüssel, die sich im HKEY \ _LOCAL \ _MACHINE Hive befinden

-   Dateien, die sich in Verzeichnissen von Programmdateien befinden

-   Dateien, die sich in den Benutzern befinden \ \ \ [Benutzername \] \ \ APPDATA \ \ LocalLow

-   Windows-Betriebssystemdateien in% SystemRoot%

Wenn Registrierungsschlüssel und Dateien, die in diesen ausgeschlossenen Speicherorten gespeichert sind, benötigt werden, um die Anwendungseinstellungen zu durchlaufen, können Administratoren die Speicherorte während des Vorlagen Erstellungsprozesses manuell zur Einstellungs Speicherort Vorlage hinzufügen.

## Erstellen von UE-V-Vorlagen


Verwenden Sie den UE-V-Generator zum Erstellen von Einstellungen-Speicherort Vorlagen für Branchenanwendungen oder andere Anwendungen. Nachdem die Vorlage für eine Anwendung erstellt wurde, können Sie die Vorlage auf Computern bereitstellen, damit Benutzer die Einstellungen für diese Anwendung durchlaufen können.

**So erstellen Sie eine Standort Vorlage für UE-v-Einstellungen mit dem UE-v-Generator**

1.  Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft User Experience Virtualization**, und klicken Sie dann auf **Microsoft User Experience Virtualization Generator**.

2.  Klicken Sie auf **Vorlage zum Erstellen einer Einstellungsposition**.

3.  Geben Sie die Anwendung an. Navigieren Sie zum Dateipfad der Anwendung (. exe) oder der Anwendungsverknüpfung (. lnk), für die Sie eine Vorlage für eine Einstellungsposition erstellen möchten. Geben Sie die Befehlszeilenargumente (sofern vorhanden) und das Arbeitsverzeichnis an, sofern vorhanden. Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

    **Hinweis**  Bevor die Anwendung gestartet wird, zeigt das System eine Aufforderung zur **Steuerung des Benutzerkontos**an. Zum Überwachen der Registrierungs-und Dateispeicherorte, die die Anwendung zum Speichern von Einstellungen verwendet, ist eine Berechtigung erforderlich.

     

4.  Schließen Sie die Anwendung, nachdem die Anwendung gestartet wurde. Der UE-V-Generator zeichnet die Speicherorte auf, an denen die Anwendung die Einstellungen speichert.

5.  Klicken Sie nach Abschluss des Prozesses auf **weiter** , um fortzufahren.

6.  Überprüfen Sie, und aktivieren Sie die Kontrollkästchen neben den entsprechenden Registrierungseinstellungen für Speicherorte und Einstellungen für die Dateispeicherorte für diese Anwendung. Die Liste enthält die folgenden beiden Kategorien für die Einstellungen für die Speicherorte:

    -   **Standard**: Anwendungseinstellungen, die in der Registrierung unter dem HKEY \ _CURRENT \ _User Schlüssel oder in den Dateiordnern unter \ \ **Users** \ \ \ [Benutzername \] \ \ **AppData**  \\  **Roaming**gespeichert sind. Der UE-V-Generator enthält standardmäßig diese Einstellungen.

    -   Nicht **Standard**: Anwendungseinstellungen, die außerhalb der Speicherorte gespeichert sind, die in den bewährten Methoden für Einstellungsdaten Speicher angegeben sind (optional). Dazu gehören Dateien und Ordner unter **Benutzer** \ \ \ [Benutzername \] \ \ **AppData**  \\  **local**. Überprüfen Sie diese Speicherorte, um zu bestimmen, ob Sie Sie in die Vorlage für den Einstellungs Speicherort einbeziehen möchten. Aktivieren Sie die Kontrollkästchen Speicherorte, um Sie einzubeziehen.

    Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

7.  Überprüfen und bearbeiten Sie alle **Eigenschaften**, **Registrierungs** Speicherorte und **Datei** Speicherorte für die Vorlage Speicherort für Einstellungen.

    -   Bearbeiten Sie die folgenden Eigenschaften auf der Registerkarte " **Eigenschaften** ":

        -   **Anwendungsname**: der Anwendungsname, der in der Beschreibung der Programmdatei Eigenschaften geschrieben wurde.

        -   **Programmname**: der Name des Programms, das aus den Programmdatei Eigenschaften übernommen wurde. Dieser Name hat in der Regel die Erweiterung ". exe".

        -   **Produktversion**: die Produktversionsnummer der exe-Datei der Anwendung. Mit dieser Eigenschaft können Sie in Verbindung mit der Dateiversion ermitteln, welche Anwendungen von der Vorlage für die Einstellungsposition abzielen. Diese Eigenschaft akzeptiert eine Hauptversionsnummer. Wenn diese Eigenschaft leer ist, wird die Vorlage für die Einstellungsposition auf alle Versionen des Produkts angewendet.

        -   **Dateiversion**: die Dateiversionsnummer the.exe Datei der Anwendung. Mit dieser Eigenschaft können Sie in Verbindung mit der Produktversion ermitteln, welche Anwendungen von der Vorlage für die Einstellungsposition abzielen. Diese Eigenschaft akzeptiert eine Hauptversionsnummer. Wenn diese Eigenschaft leer ist, wird die Vorlage für die Einstellungsposition auf alle Versionen des Programms angewendet.

        -   **Name der Vorlagen Autorin** (optional): der Name der Vorlage für den Speicherort der Einstellungen.

        -   **E-Mail-Vorlage für Vorlagenautor** (optional): die e-Mail-Adresse der Vorlage "Speicherort für Einstellungen".

    -   Auf der Registerkarte " **Registrierung** " sind der **Schlüssel** und der **Bereich** der Registrierungsspeicherorte aufgeführt, die in der Vorlage "einstellungensort" enthalten sind. Bearbeiten Sie die Registrierungsspeicherorte mithilfe des Dropdownmenüs **Aufgaben** . Aufgaben umfassen das Hinzufügen neuer Schlüssel, das Bearbeiten des Namens oder des Bereichs vorhandener Schlüssel, das Löschen von Schlüsseln und das Durchsuchen der Registrierung, in der sich die Schlüssel befinden. Verwenden Sie den Bereich **alle Einstellungen** , um alle Registrierungseinstellungen unter dem angegebenen Schlüssel einzubeziehen. Verwenden Sie **alle Einstellungen und Unterschlüssel** , um alle Registrierungseinstellungen unter den angegebenen Tasten, Unterschlüsseln und Unterschlüssel Einstellungen einzubeziehen.

    -   Auf der Registerkarte " **Dateien** " werden der Dateipfad und die Dateimaske der Dateispeicherorte aufgeführt, die in der Vorlage für die Einstellungen gespeichert sind. Bearbeiten Sie die Dateispeicherorte mithilfe des Dropdownmenüs **Aufgaben** . Zu den Aufgaben für Dateispeicherorte gehören das Hinzufügen neuer Dateien oder Ordnerspeicherorte, das Bearbeiten des Bereichs vorhandener Dateien oder Ordner, das Löschen von Dateien oder Ordnern sowie das Öffnen des ausgewählten Speicherorts im Windows-Explorer. Lassen Sie die Dateimaske leer, um alle Dateien in den angegebenen Ordner einzubeziehen.

8.  Klicken Sie auf dem Computer auf die Vorlage Speicherort für Einstellungen **Erstellen** und speichern.

9.  Klicken Sie auf **Schließen** , um den Assistenten für Einstellungs Vorlagen zu schließen. Beenden Sie die UE-V-Generator Anwendung.

    Nachdem Sie die Vorlage für die Einstellungsposition für eine Anwendung erstellt haben, sollten Sie die Vorlage testen. Stellen Sie die Vorlage in einer Lab-Umgebung bereit, bevor Sie Sie in der Produktion im Unternehmen einsetzen.

## Verwandte Themen


[Arbeiten mit benutzerdefinierten UE-V-Vorlagen und dem UE-V-Generator](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[Vorgänge für UE-V 1.0](operations-for-ue-v-10.md)

 

 





