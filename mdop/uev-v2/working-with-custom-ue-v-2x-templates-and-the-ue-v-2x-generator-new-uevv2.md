---
title: Arbeiten mit benutzerdefinierten UE-v 2. x-Vorlagen und dem UE-v 2. x-Generator
description: Arbeiten mit benutzerdefinierten UE-v 2. x-Vorlagen und dem UE-v 2. x-Generator
author: dansimp
ms.assetid: f0bb4920-0132-472c-a564-abf06a884275
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a8d863896e4ccfa92161f8a8f5e2b8955f139872
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807848"
---
# Arbeiten mit benutzerdefinierten UE-v 2. x-Vorlagen und dem UE-v 2. x-Generator


Zum Synchronisieren von Anwendungseinstellungen zwischen Benutzercomputern verwenden Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 und 2,1 SP1 *Einstellungen für Standort Vorlagen*. Einige Einstellungen für Speicherort Vorlagen sind in der Benutzeroberflächen-Virtualisierung enthalten. Mithilfe des UE-V-Generators können Sie auch benutzerdefinierte Speicherort Vorlagen erstellen, bearbeiten oder überprüfen.

Der UE-V-Generator überwacht Windows-Desktopanwendungen, um die Speicherorte, an denen die Anwendung die Einstellungen speichert, zu ermitteln und zu erfassen. Die Anwendung, die überwacht wird, muss eine Desktopanwendung sein. Der UE-V-Generator kann für die folgenden Anwendungstypen keine Vorlage für eine Einstellungsposition erstellen:

-   Virtualisierte Anwendungen

-   Anwendungen, die über die Terminal Dienste angeboten werden

-   Java-Anwendungen

-   Windows-Apps  

In diesem Thema 

**Speicherorte für Standard-und nicht Standardeinstellungen:** Der UE-V-Generator hilft Ihnen bei der Suche nach Einstellungsdateien und Registrierungseinstellungen, die Anwendungen zum Speichern von Einstellungsinformationen verwenden. Der Generator erkennt nur Einstellungen an Speicherorten, die für einen Standardbenutzer barrierefrei sind. Einstellungen, die an anderen Speicherorten gespeichert sind, sind ausgeschlossen. Erkannte Einstellungen sind in zwei Kategorien unterteilt: **Standard** und **nicht Standard**. Standard Einstellungen werden für die Synchronisierung empfohlen, und UE-V kann Sie problemlos erfassen und anwenden. Nicht standardmäßige Einstellungen können die Einstellungen möglicherweise synchronisieren, doch aufgrund der von UE-V verwendeten Regeln werden diese Einstellungen möglicherweise nicht konsistent oder zuverlässig synchronisiert. Diese Einstellungen sind möglicherweise von temporären Dateien abhängig, führen zu einer unzuverlässigen Synchronisierung oder sind möglicherweise nicht hilfreich. Diese Einstellungen sind im UE-V-Generator dargestellt. Sie können festlegen, dass Sie von Fall zu Fall einbezogen oder ausgeschlossen werden.

Der UE-V-Generator öffnet die Anwendung im Rahmen des Ermittlungsprozesses. Der Generator kann Einstellungen an den folgenden Speicherorten aufzeichnen:

-   **Registrierungseinstellungen** – Registrierungsspeicherorte unter **HKEY \ _CURRENT \ _User**

-   **Anwendungseinstellungsdateien** – Dateien, die unter \ \ **Users** \ \ \ [Benutzername \] \ \ **AppData**  \\  **Roaming** gespeichert sind

Der UE-V-Generator schließt Speicherorte aus, die häufig Anwendungssoftware Dateien speichern, aber nicht gut zwischen Benutzercomputern oder Umgebungen synchronisiert werden. Der UE-V-Generator schließt diese Speicherorte aus. Ausgeschlossene Speicherorte sind wie folgt:

-   HKEY \ _CURRENT \ _User Registrierungsschlüssel und Dateien, für die der angemeldete Benutzer keine Werte schreiben kann

-   HKEY \ _CURRENT \ _User Registrierungsschlüssel und Dateien, die der Kernfunktionalität des Windows-Betriebssystems zugeordnet sind

-   Alle Registrierungsschlüssel, die sich im HKEY \ _LOCAL \ _MACHINE Hive befinden, für die Administratorrechte erforderlich sind und möglicherweise zum Festlegen einer Vereinbarung zur Benutzerkontensteuerung erforderlich sind

-   Dateien, die sich in Verzeichnissen von Programmdateien befinden, die Administratorrechte erfordern und möglicherweise zum Festlegen einer UAC-Vereinbarung erforderlich sind

-   Dateien, die sich unter "Benutzer \ \ \ [Benutzername \] \ \ APPDATA \ \ LocalLow" befinden

-   Windows-Betriebssystemdateien, die sich in% SystemRoot% befinden und für die Administratorrechte erforderlich sind und möglicherweise zum Festlegen einer UAC-Vereinbarung erforderlich sind

Wenn Registrierungsschlüssel und Dateien, die in diesen Speicherorten gespeichert sind, zum Synchronisieren von Anwendungseinstellungen erforderlich sind, können Sie die ausgeschlossenen Speicherorte während des Vorlagen Erstellungsprozesses manuell zur Einstellungs Speicherort Vorlage hinzufügen (mit Ausnahme der Registrierungseinträge in der HKEY \ _LOCAL \ _MACHINE Struktur).

## <a href="" id="edit"></a>Bearbeiten von Einstellungen für Standort Vorlagen mit dem UE-V-Generator


Verwenden Sie den UE-V-Generator, um Einstellungen für Standort Vorlagen zu bearbeiten. Wenn die überarbeiteten Einstellungen den Vorlagen mithilfe des UE-V-Generators hinzugefügt werden, werden die Versionsinformationen in der Vorlage automatisch aktualisiert, um sicherzustellen, dass vorhandene Vorlagen, die im Unternehmen bereitgestellt werden, ordnungsgemäß aktualisiert werden.

**Hinweis**  Wenn Sie eine UE-v 1,0-Vorlage mit dem UE-v 2-Generator bearbeiten, wird die Vorlage automatisch in eine UE-v 2-Vorlage konvertiert. UE-V 1,0-Agents können die bearbeitete Vorlage nicht mehr verwenden.

 

**So bearbeiten Sie eine Standort Vorlage für UE-v-Einstellungen mit dem UE-v-Generator**

1.  Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft User Experience Virtualization**, und klicken Sie dann auf **Microsoft User Experience Virtualization Generator**.

2.  Klicken Sie auf **Vorlage für Einstellungen bearbeiten**.

3.  Wählen Sie in der Liste der zuletzt verwendeten Vorlagen die Vorlage aus, die bearbeitet werden soll. Klicken Sie alternativ auf **Durchsuchen** , um nach der Einstellungs Vorlagendatei zu suchen. Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

4.  Überprüfen Sie die **Eigenschaften**, die **Registrierungs** Speicherorte und die Speicherorte der **Dateien** für die Einstellungs Vorlage. Bearbeiten Sie nach Bedarf.

    -   Auf der Registerkarte **Eigenschaften** können Sie die folgenden Eigenschaften anzeigen und bearbeiten:

        -   **Anwendungsname**: der Name der Anwendung, der in der Beschreibung der Programmdatei Eigenschaften geschrieben ist.

        -   **Programmname**: der Name des Programms, das aus den Programmdatei Eigenschaften übernommen wird. Dieser Name hat in der Regel die Dateinamenerweiterung exe.

        -   **Produktversion**: die Produktversionsnummer der exe-Datei der Anwendung. Mit dieser Eigenschaft können Sie zusammen mit der **Dateiversion**ermitteln, welche Anwendungen von der Vorlage für die Einstellungsposition abzielen. Diese Eigenschaft akzeptiert eine Hauptversionsnummer. Wenn diese Eigenschaft leer ist, gilt die Vorlage Speicherort für Einstellungen für alle Versionen des Produkts.

        -   **Dateiversion**: die Dateiversionsnummer der exe-Datei der Anwendung. Mit dieser Eigenschaft können Sie zusammen mit der **Produktversion**ermitteln, welche Anwendungen von der Vorlage für die Einstellungsposition abzielen. Diese Eigenschaft akzeptiert eine Hauptversionsnummer. Wenn diese Eigenschaft leer ist, gilt die Vorlage für die Einstellungsposition für alle Versionen des Programms.

        -   **Name der Vorlagen Autorin** (optional): der Name des Autors der Einstellungs Vorlage.

        -   **E-Mail-Vorlage für Vorlagenautor** (optional): die e-Mail-Adresse der Vorlage "Speicherort für Einstellungen".

    -   Auf der Registerkarte " **Registrierung** " sind der **Schlüssel** und der **Bereich** der Registrierungsspeicherorte aufgeführt, die in der Vorlage "einstellungensort" enthalten sind. Sie können die Registrierungsspeicherorte mithilfe des Dropdownmenüs **Aufgaben** bearbeiten. Im Menü Aufgaben können Sie neue Schlüssel hinzufügen, den Namen oder den Bereich vorhandener Schlüssel bearbeiten, Schlüssel löschen und die Registrierung durchsuchen, in der sich die Schlüssel befinden. Wenn Sie den Bereich für die Registrierung definieren, können Sie den Bereich **alle Einstellungen** verwenden, um alle Registrierungseinstellungen unter dem angegebenen Schlüssel einzubeziehen. Verwenden Sie **alle Einstellungen** und unter **Schlüssel** , um alle Registrierungseinstellungen unter den angegebenen Tasten, Unterschlüsseln und Unterschlüssel Einstellungen einzubeziehen.

    -   Auf der Registerkarte " **Dateien** " werden der Dateipfad und die Dateimaske der Dateispeicherorte aufgeführt, die in der Vorlage für die Einstellungsposition enthalten sind. Sie können die Dateispeicherorte mithilfe des Dropdownmenüs **Aufgaben** bearbeiten. Im Menü **Aufgaben** für Dateispeicherorte können Sie neue Dateien oder Ordnerspeicherorte hinzufügen, den Bereich vorhandener Dateien oder Ordner bearbeiten, Dateien oder Ordner löschen und den ausgewählten Speicherort in Windows-Explorer öffnen. Wenn Sie alle Dateien in den angegebenen Ordner einbeziehen möchten, lassen Sie die Dateimaske leer.

5.  Klicken Sie auf **Speichern** , um die Änderungen an der Vorlage Speicherort für Einstellungen zu speichern.

6.  Klicken Sie auf **Schließen** , um den Assistenten für Einstellungs Vorlagen zu schließen. Beenden Sie die UE-V-Generator Anwendung.

    Nachdem Sie die Vorlage für die Einstellungsposition für eine Anwendung bearbeitet haben, sollten Sie die Vorlage testen. Stellen Sie die überarbeiteten Einstellungen-Speicherort Vorlage in einer Lab-Umgebung bereit, bevor Sie Sie in der Produktion im Unternehmen einsetzen.

**Manuelles Bearbeiten einer Speicherort Vorlage für Einstellungen**

1.  Erstellen Sie eine lokale Kopie der Datei Settings Location Template. Xml. Standort Vorlagen für UE-V-Einstellungen sind XML-Dateien, die die Speicherorte identifizieren, an denen Anwendungseinstellungen gespeichert werden.

    **Hinweis**  Eine Vorlage für eine Einstellungsposition ist aufgrund der Vorlagen **-ID**eindeutig. Wenn Sie die Vorlage kopieren und die XML-Datei umbenennen, schlägt die Vorlagen Registrierung fehl, da UE-V das Vorlagen- **ID** -Tag in der XML-Datei liest, um den Namen zu ermitteln, nicht den Dateinamen der XML-Datei. UE-V liest auch die **Versions** Nummer, um zu erfahren, ob sich irgendetwas geändert hat. Wenn die Versionsnummer höher ist, aktualisiert UE-V die Vorlage.

     

2.  Öffnen Sie die Datei mit einem XML-Editor für die Speicherort Vorlage für Einstellungen.

3.  Bearbeiten Sie die Vorlagendatei für die Einstellungsposition. Alle Änderungen müssen der in [SettingsLocationTempate. xsd](https://technet.microsoft.com/library/dn763947.aspx)definierten UE-V-Schemadatei entsprechen. Standardmäßig befindet sich eine Kopie der XSD-Datei in \\ProgramData\\Microsoft\\UEV\\Templates.

4.  Erhöhen Sie die **Versions** Nummer für die Vorlage für die Einstellungsposition.

5.  Speichern Sie die Vorlagendatei für die Einstellungsposition, und schließen Sie dann den XML-Editor.

6.  Überprüfen Sie die Speicherort Vorlagendatei für geänderte Einstellungen mithilfe des UE-V-Generators.

7.  Sie müssen die bearbeitete Vorlage "UE-V Settings" registrieren, bevor die Einstellungen zwischen Clientcomputern synchronisiert werden können. Wenn Sie eine Vorlage registrieren möchten, öffnen Sie Windows PowerShell, und führen Sie dann das folgende Cmdlet `update-uevtemplate [templatefilename]` aus: Anschließend können Sie die Datei in den Speicherkatalog für Einstellungen kopieren. Der UE-V-Agent auf den Computern der Benutzer sollte dann wie geplant im geplanten Task aktualisiert werden.

## <a href="" id="validate"></a>Überprüfen von Standort Vorlagen für Einstellungen mit dem UE-V-Generator


Es ist möglich, Einstellungen für Standort Vorlagen in einem XML-Editor zu erstellen oder zu bearbeiten, ohne den UE-V-Generator zu verwenden. In diesem Fall können Sie den UE-V-Generator verwenden, um zu überprüfen, ob der neue oder überarbeitete XML-Code mit dem Schema übereinstimmt, das für die Vorlage definiert wurde.

**So überprüfen Sie eine Standort Vorlage für UE-v-Einstellungen mit dem UE-v-Generator**

1.  Klicken Sie auf **Start**, zeigen Sie auf **Alle Programme**, klicken Sie auf **Microsoft User Experience Virtualization**, und klicken Sie dann auf **Microsoft User Experience Virtualization Generator**.

2.  Klicken Sie auf **Vorlage zum Überprüfen einer Einstellungsposition**.

3.  Wählen Sie in der Liste der zuletzt verwendeten Vorlagen die Vorlage aus, die bearbeitet werden soll. Sie können aber auch zur Einstellungs Vorlagendatei **Navigieren** . Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

4.  Klicken Sie auf über **prüfen** , um fortzufahren.

5.  Klicken Sie auf **Schließen** , um den Assistenten für Einstellungs Vorlagen zu schließen. Beenden Sie die UE-V-Generator Anwendung.

    Nachdem Sie die Vorlage für die Einstellungsposition für eine Anwendung überprüft haben, sollten Sie die Vorlage testen. Stellen Sie die Vorlage in einer Lab-Umgebung bereit, bevor Sie Sie in einer Produktionsumgebung in Enterprise speichern.

## <a href="" id="share"></a>Freigeben von Einstellungen für Speicherort Vorlagen im Vorlagenkatalog


Der Microsoft User Experience Virtualization (UE-v) 2,0-Vorlagenkatalog ermöglicht Administratoren die Freigabe von Standort Vorlagen für UE-v-Einstellungen. Im Katalog können Sie Ihre Einstellungen-Speicherort Vorlagen für andere Benutzer hochladen, und Sie können Vorlagen herunterladen, die von anderen Benutzern erstellt wurden. Der UE-V-Vorlagenkatalog befindet sich [hier](https://go.microsoft.com/fwlink/p/?LinkId=246589)auf der Microsoft Technet-Version.

Vergewissern Sie sich vor dem Freigeben einer Vorlage für Einstellungen für den Vorlagenkatalog in UE-V, dass Sie keine persönlichen oder Unternehmensinformationen enthält. Sie können einen beliebigen XML-Viewer verwenden, um den Inhalt einer Einstellungs Speicherort-Vorlagendatei zu öffnen und anzuzeigen. Die folgenden vorlagenwerte sollten überprüft werden, bevor Sie eine Vorlage für Personen außerhalb Ihres Unternehmens freigeben.

-   Vorlagenautor Name – geben Sie einen allgemeinen, nicht identifizierbaren Namen für den Vorlagenautoren Namen an, oder schließen Sie diese Daten aus der Vorlage aus.

-   E-Mail-Vorlage für Vorlagenautor: Geben Sie eine allgemeine, nicht identifizierbare Vorlage für eine e-Mail-Nachricht an oder schließen Sie diese Daten aus der Vorlage

Bevor Sie eine Vorlage für eine Einstellungsposition bereitstellen, die Sie aus dem UE-V-Katalog heruntergeladen haben, sollten Sie zuerst die Vorlage testen, um sicherzustellen, dass die Einstellungen der Anwendung in einer Testumgebung richtig synchronisiert werden.






## Verwandte Themen


[Verwalten von UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

[Bereitstellen von UE-V 2. x für benutzerdefinierte Anwendungen](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

 

 





