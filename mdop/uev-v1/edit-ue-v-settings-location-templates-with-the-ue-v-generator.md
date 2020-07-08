---
title: Bearbeiten von UE-V-Einstellungsortvorlagen mit dem UE-V-Generator
description: Bearbeiten von UE-V-Einstellungsortvorlagen mit dem UE-V-Generator
author: dansimp
ms.assetid: da78f9c8-1624-4111-8c96-79db7224bd0b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b90cd58761e6ac40c089f3afeade3c445a52ea6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812160"
---
# Bearbeiten von UE-V-Einstellungsortvorlagen mit dem UE-V-Generator


Verwenden Sie den Microsoft User Experience Virtualization (UE-V)-Generator, um Einstellungen für Standort Vorlagen zu bearbeiten. Wenn die überarbeiteten Einstellungen den Vorlagen mithilfe des UE-V-Generators hinzugefügt werden, werden die Versionsinformationen in der Vorlage automatisch aktualisiert, um sicherzustellen, dass alle im Unternehmen bereitgestellten Vorlagen ordnungsgemäß aktualisiert werden.

**So bearbeiten Sie eine Standort Vorlage für UE-v-Einstellungen mit dem UE-v-Generator**

1.  Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft User Experience Virtualization**, und klicken Sie dann auf **Microsoft User Experience Virtualization Generator**.

2.  Klicken Sie auf **Vorlage für Einstellungen bearbeiten**.

3.  Wählen Sie in der Liste der zuletzt verwendeten Vorlagen die Vorlage aus, die bearbeitet werden soll. **Wechseln Sie** Alternativ zur Einstellungs Vorlagendatei. Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

4.  Überprüfen Sie die **Eigenschaften**, die **Registrierungs** Speicherorte und die Speicherorte der **Dateien** für die Einstellungs Vorlage. Bearbeiten Sie nach Bedarf.

    -   Auf der Registerkarte **Eigenschaften** können Sie die folgenden Eigenschaften anzeigen und bearbeiten:

        -   **Anwendungsname**: der Anwendungsname, der in der Beschreibung der Programmdatei Eigenschaften geschrieben wurde.

        -   **Programmname**: der Name des Programms, das aus den Programmdatei Eigenschaften übernommen wurde. Dieser Name hat in der Regel die Erweiterung ". exe".

        -   **Produktversion**: die Produktversionsnummer der exe-Datei der Anwendung. Mit dieser Eigenschaft können Sie zusammen mit der **Dateiversion**ermitteln, welche Anwendungen von der Vorlage für die Einstellungsposition abzielen. Diese Eigenschaft akzeptiert eine Hauptversionsnummer. Wenn diese Eigenschaft leer ist, gilt die Vorlage für die Einstellungsposition für alle Versionen des Produkts.

        -   **Dateiversion**: die Dateiversionsnummer the.exe Datei der Anwendung. Mit dieser Eigenschaft können Sie zusammen mit der **Produktversion**ermitteln, welche Anwendungen von der Vorlage für die Einstellungsposition abzielen. Diese Eigenschaft akzeptiert eine Hauptversionsnummer. Wenn diese Eigenschaft leer ist, wird die Vorlage für die Einstellungsposition auf alle Versionen des Programms angewendet.

        -   **Name der Vorlagen Autorin** (optional): der Name des Autors der Einstellungs Vorlage.

        -   **E-Mail-Vorlage für Vorlagenautor** (optional): die e-Mail-Adresse der Vorlage "Speicherort für Einstellungen".

    -   Auf der Registerkarte " **Registrierung** " sind der **Schlüssel** und der **Bereich** der Registrierungsspeicherorte aufgeführt, die in der Vorlage "einstellungensort" enthalten sind. Sie können die Registrierungsspeicherorte mithilfe des Dropdownmenüs " **Aufgaben** " bearbeiten. Aufgaben umfassen das Hinzufügen neuer Schlüssel, das Bearbeiten des Namens oder des Bereichs vorhandener Schlüssel, das Löschen von Schlüsseln und das Durchsuchen der Registrierung, in der sich die Schlüssel befinden. Wenn Sie den Bereich für die Registrierung definieren, können Sie den Bereich **alle Einstellungen** verwenden, um alle Registrierungseinstellungen unter dem angegebenen Schlüssel einzubeziehen. Verwenden Sie **alle Einstellungen** und unter **Schlüssel** , um alle Registrierungseinstellungen unter den angegebenen Tasten, Unterschlüsseln und Unterschlüssel Einstellungen einzubeziehen.

    -   Auf der Registerkarte " **Dateien** " werden der Dateipfad und die Dateimaske der Dateispeicherorte aufgeführt, die in der Vorlage für die Einstellungen gespeichert sind. Sie können die Dateispeicherorte mithilfe des Dropdownmenüs " **Aufgaben** " bearbeiten. Zu den Aufgaben für Dateispeicherorte gehören das Hinzufügen neuer Dateien oder Ordnerspeicherorte, das Bearbeiten des Bereichs vorhandener Dateien oder Ordner, das Löschen von Dateien oder Ordnern sowie das Öffnen des ausgewählten Speicherorts im Windows-Explorer. Wenn Sie alle Dateien in den angegebenen Ordner einbeziehen möchten, lassen Sie die Dateimaske leer.

5.  Klicken Sie auf **Speichern** , um die Änderungen an der Vorlage Speicherort für Einstellungen zu speichern.

6.  Klicken Sie auf **Schließen** , um den Assistenten für Einstellungs Vorlagen zu schließen. Beenden Sie die UE-V-Generator Anwendung.

    Nachdem Sie die Vorlage für die Einstellungsposition für eine Anwendung bearbeitet haben, sollten Sie die Vorlage testen. Stellen Sie die überarbeiteten Einstellungen-Speicherort Vorlage in einer Lab-Umgebung bereit, bevor Sie Sie in der Produktion im Unternehmen einsetzen.

**Manuelles Bearbeiten einer Speicherort Vorlage für Einstellungen**

1.  Erstellen Sie eine lokale Kopie der Vorlage für die Einstellungsposition (XML-Datei). Standort Vorlagen für UE-V-Einstellungen sind XML-Dateien, die die Speicherorte identifizieren, an denen Anwendungseinstellungen gespeichert werden.

2.  Öffnen Sie die Datei mit einem XML-Editor für die Speicherort Vorlage für Einstellungen.

3.  Bearbeiten Sie die Vorlagendatei für die Einstellungsposition. Alle Änderungen müssen der in SettingsLocationTempate. XSD definierten UE-V-Schemadatei entsprechen. Eine Kopie der XSD-Datei befindet sich `\ProgramData\Microsoft\UEV\Templates` standardmäßig in.

4.  Speichern Sie die Vorlagendatei für die Einstellungsposition, und schließen Sie den XML-Editor.

5.  Überprüfen Sie die Speicherort Vorlagendatei für geänderte Einstellungen mit dem UE-V-Generator. Weitere Informationen zum Überprüfen mit dem UE-v-Generator finden Sie unter über [Prüfen von Standort Vorlagen für UE-v-Einstellungen mit dem UE-v-Generator](validate-ue-v-settings-location-templates-with-ue-v-generator.md).

## Verwandte Themen


[Arbeiten mit benutzerdefinierten UE-V-Vorlagen und dem UE-V-Generator](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[Vorgänge für UE-V 1.0](operations-for-ue-v-10.md)

 

 





