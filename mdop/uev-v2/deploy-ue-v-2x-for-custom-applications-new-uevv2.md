---
title: Bereitstellen von UE-V 2. x für benutzerdefinierte Anwendungen
description: Bereitstellen von UE-V 2. x für benutzerdefinierte Anwendungen
author: dansimp
ms.assetid: f7cb089f-d764-4a93-82b6-926fe0385a23
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 07/19/2016
ms.openlocfilehash: 217f647d948df016c4a6b72736669c2b3305b705
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810534"
---
# Bereitstellen von UE-V 2. x für benutzerdefinierte Anwendungen


Microsoft User Experience Virtualization (UE-V) 2,0 2,1 und 2,1 SP1 verwenden XML-Dateien namens " **Einstellungen** ", um die Einstellungen für die Desktopanwendung und die Windows-Desktopeinstellungen zwischen den Benutzercomputern zu überwachen und zu synchronisieren. In UE-V sind standardmäßig einige Einstellungsortvorlagen enthalten. Wenn Sie jedoch die Einstellungen für Desktopanwendungen, die nicht in den Standardvorlagen enthalten sind, synchronisieren möchten, können Sie mithilfe des UE-V-Generators ihre eigenen Speicherort Vorlagen für benutzerdefinierte Einstellungen erstellen.

Nachdem Sie das Planungs Material in [Vorbereiten einer UE-v 2. x-Bereitstellung](prepare-a-ue-v-2x-deployment-new-uevv2.md) gelesen haben und entschieden haben, dass Sie die Einstellungen für benutzerdefinierte Anwendungen (Drittanbieter, Branchen usw.) synchronisieren möchten, stellen Sie die Features von UE-v bereit, wie in diesem Thema beschrieben. Um zu beginnen, müssen Sie die wichtigsten Schritte zum Synchronisieren von Einstellungen für benutzerdefinierte Anwendungen ausführen:

-   [Installieren des UEV-Generators](#uevgen)

    Verwenden Sie den UEV-Generator, um benutzerdefinierte Speicherort Vorlagen für XML-Einstellungen zu erstellen.

-   [Konfigurieren eines UE-V-Einstellungs Vorlagen Katalogs](#deploycatalogue)

    Sie können diesen Pfad definieren, in dem die Speicherort Vorlagen für benutzerdefinierte Einstellungen gespeichert werden.

-   [Erstellen von Speicherort Vorlagen für benutzerdefinierte Einstellungen](#createcustomtemplates)

    Mithilfe dieser benutzerdefinierten Vorlagen können Benutzer die Einstellungen für benutzerdefinierte Anwendungen synchronisieren.

-   [Bereitstellen der Speicherort Vorlagen für benutzerdefinierte Einstellungen](#deploycustomtemplates)

    Nachdem Sie die benutzerdefinierte Vorlage getestet haben, um sicherzustellen, dass die Einstellungen ordnungsgemäß synchronisiert werden, können Sie diese Vorlagen auf eine der folgenden Arten bereitstellen:

    -   Über Ihre vorhandene Bereitstellungsinfrastruktur wie Configuration Manager

    -   Verwenden von Gruppenrichtlinieneinstellungen

    -   [Bereitstellen eines UE-V-Einstellungs Vorlagen Katalogs](#deploycatalogue)

    **Hinweis**  Vorlagen, die mithilfe von ESD-oder Gruppenrichtlinien bereitgestellt werden, müssen bei der UE-V-Windows-Verwaltungsinstrumentation (WMI) oder Windows PowerShell registriert sein.

     

## Vorbereiten der Bereitstellung von UE-V 2. x für benutzerdefinierte Anwendungen


Bevor Sie mit der Bereitstellung der UE-V-Features beginnen, die benutzerdefinierte Anwendungen behandeln, müssen Sie nur einige Punkte überprüfen.

### Der UE-V-Generator

Der UE-V-Generator überwacht eine Anwendung, um die Speicherorte, an denen die Anwendung Ihre Einstellungen speichert, zu ermitteln und zu erfassen. Die Anwendung, die überwacht wird, muss eine herkömmliche Anwendung sein. Sie verwenden den UE-V-Generator zum Erstellen von Einstellungen für Speicherort Vorlagen, aber es kann keine Vorlage für eine Einstellungsposition aus diesen Anwendungstypen erstellen:

-   Virtualisierte Anwendungen

-   Anwendungen, die über die Terminal Dienste angeboten werden

-   Java-Anwendungen

-   Windows-Apps  

**Hinweis**  Die Standort Vorlagen für die UE-V-Einstellungen können nicht aus virtualisierten Anwendungen oder Terminal Dienste-Anwendungen erstellt werden. Einstellungen, die mithilfe der Vorlagen synchronisiert werden, können jedoch auf diese Anwendungen angewendet werden. Öffnen Sie zum Erstellen von Vorlagen zur Unterstützung von VDI-Anwendungen (Virtual Desktop Infrastructure) und von Terminal Diensten eine Version des Windows Installer-Pakets (MSI) der Anwendung mithilfe des UE-V-Generators. Weitere Informationen zum Synchronisieren von Einstellungen für virtuelle Anwendungen finden Sie unter [Verwenden von UE-V 2. x mit Application Virtualization-Anwendungen](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md).

 

**Ausgeschlossene Speicherorte:** Der Ermittlungsprozess schließt Speicherorte aus, die häufig Anwendungssoftware Dateien speichern, die die Einstellungen nicht gut zwischen Benutzercomputern oder Computerumgebungen synchronisieren. Standardmäßig sind diese ausgeschlossen:

-   HKEY \ _CURRENT \ _User Registrierungsschlüssel und Dateien, für die der angemeldete Benutzer keine Werte schreiben kann

-   HKEY \ _CURRENT \ _User Registrierungsschlüssel und Dateien, die der Kernfunktionalität des Windows-Betriebssystems zugeordnet sind

-   Alle Registrierungsschlüssel, die sich im HKEY \ _LOCAL \ _MACHINE Hive befinden

-   Dateien, die sich in Verzeichnissen von Programmdateien befinden

-   Dateien, die sich in den Benutzern befinden \ \ \ [Benutzername \] \ \ APPDATA \ \ LocalLow

-   Windows-Betriebssystemdateien, die sich in% SystemRoot% befinden

Wenn Registrierungsschlüssel und Dateien, die in ausgeschlossenen Speicherorten gespeichert sind, zum Synchronisieren von Anwendungseinstellungen erforderlich sind, können Sie die Speicherorte während des Erstellungsprozesses der Vorlage manuell zur Vorlage "Einstellungs Speicherort" hinzufügen.
Es werden jedoch nur Änderungen an der HKEY \ _CURRENT \ _User Hive synchronisiert.

### Ersetzen der standardmäßigen Microsoft-Vorlagen

Der UE-V-Agent installiert eine Standardgruppe von Einstellungen-Standort Vorlagen für allgemeine Microsoft-Anwendungen und Windows-Einstellungen. Wenn Sie diese Vorlagen anpassen oder Einstellungen für Standort Vorlagen zum Synchronisieren von Einstellungen für benutzerdefinierte Anwendungen erstellen, kann der UE-V-Agent so konfiguriert werden, dass ein Einstellungs Vorlagenkatalog zum Speichern der Vorlagen verwendet wird. In diesem Fall müssen Sie die Standardvorlagen zusammen mit den benutzerdefinierten Vorlagen im Vorlagenkatalog für Einstellungen hinzufügen.

Wenn Sie [einen UE-V-Agent bereitstellen](https://technet.microsoft.com/library/dn458891.aspx#agent), können Sie den Befehlszeilenparameter verwenden, `RegisterMSTemplates` um die Registrierung der Microsoft-Standardvorlagen zu deaktivieren.

Wenn Sie Gruppenrichtlinien zum Konfigurieren des Katalog Pfads für Einstellungs Vorlagen verwenden, können Sie auswählen, dass die standardmäßigen Microsoft-Vorlagen ersetzt werden sollen. Wenn Sie die Richtlinieneinstellungen so konfigurieren, dass die standardmäßigen Microsoft-Vorlagen ersetzt werden, werden alle Microsoft-Standardvorlagen, die vom UE-V-Agent installiert werden, gelöscht, und es werden nur die Vorlagen verwendet, die sich im Katalog der Einstellungs Vorlagen befinden. Der Parameter für die Konfigurationseinstellung des UE-V-Agents `RegisterMSTemplates` muss auf " *true* " festgelegt werden, um die standardmäßige Microsoft-Vorlage zu überschreiben.

**Hinweis**  Wenn Sie diese Richtlinieneinstellung nach der Aktivierung deaktivieren, werden die standardmäßigen Microsoft-Vorlagen vom UE-V-Agent nicht wiederhergestellt.

 

Wenn im Einstellungs Vorlagenkatalog angepasste Vorlagen vorhanden sind, die die gleiche ID wie die standardmäßigen Microsoft-Vorlagen verwenden, und der UE-V-Agent nicht so konfiguriert ist, dass die standardmäßigen Microsoft-Vorlagen ersetzt werden, werden die Microsoft-Vorlagen ignoriert.

Sie können die Standardvorlagen auch ersetzen, indem Sie die Windows PowerShell-Features von UE-V verwenden. Wenn Sie die standardmäßige Microsoft-Vorlage durch Windows PowerShell ersetzen möchten, heben Sie die Registrierung aller Microsoft-Standardvorlagen auf, und registrieren Sie dann die angepassten Vorlagen.

**Hinweis**  Alte Einstellungs Pakete verbleiben im Einstellungs Speicherort, auch wenn Sie für eine Anwendung neue Speicherort Vorlagen für Einstellungen bereitstellen. Diese Pakete werden nicht vom Agenten gelesen, aber auch nicht automatisch gelöscht.

 

## <a href="" id="uevgen"></a>Installieren des UEV 2. x-Generators


Installieren Sie den Microsoft User Experience Virtualization (UE-V) 2,0-Generator auf einem Computer, den Sie dann zum Erstellen einer benutzerdefinierten Speicherort Vorlage für Einstellungen verwenden können. Auf diesem Computer sollten die Anwendungen installiert sein, für die benutzerdefinierte Einstellungen für Standort Vorlagen generiert werden sollen.

**So installieren Sie den UE-V-Generator**

1.  Suchen Sie als Benutzer mit lokalen Administratorrechten die Installationsdatei des UE-v-Generators, **ToolSetup.exe** die mit der UE-v-Software bereitgestellt wird. Wenn Ihnen die Computerarchitektur bekannt ist, können Sie die entsprechende Windows Installer-Datei (MSI), **ToolsSetupx64.msi** oder **ToolsSetupx86.msi**ausführen.

2.  Doppelklicken Sie auf die Installationsdatei. Der Setup-Assistent von User Experience Virtualization Generator wird geöffnet. Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

3.  Akzeptieren Sie die Microsoft-Software-Lizenzbestimmungen, und klicken Sie dann auf **weiter**.

4.  Klicken Sie auf die Optionen für Microsoft Updates und das Programm zur Verbesserung der Benutzerfreundlichkeit.

5.  Wählen Sie den Zielordner aus, in dem der UE-V-Generator installiert werden soll, und klicken Sie dann auf **weiter**.

6.  Klicken Sie auf **Installieren** , um mit der Installation zu beginnen.

    **Hinweis**  Vor der Installation der Anwendung wird eine Aufforderung zur **Benutzerkontensteuerung** angezeigt. Zum Installieren des UE-V-Generators ist eine Berechtigung erforderlich.

     

7.  Klicken Sie auf **Fertig stellen** , um den Assistenten zu schließen, nachdem die Installation abgeschlossen ist. Sie müssen den Computer neu starten, bevor Sie den UE-V-Generator ausführen können.

    Um zu überprüfen, ob die Installation erfolgreich war, klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft User Experience Virtualization**, und klicken Sie dann auf **Microsoft User Experience Virtualization Generator**.

    **Hinweis**  Der UE-v 2-Generator kann nur zum Erstellen von Vorlagen für UE-v 2-Agents verwendet werden. Bei einer gemischten Bereitstellung von UE-v 1,0-Agents und UE-v 2-Agents sollten Sie den UE-v 1,0-Generator weiterhin verwenden, bis Sie alle UE-v-Agents aktualisiert haben.

     

## <a href="" id="deploycatalogue"></a>Bereitstellen eines Einstellungs Vorlagen Katalogs


Der Katalog der Benutzeroberflächen-Virtualisierungs-Einstellungen ist ein Ordnerpfad auf UE-V-Computern oder eine SMB-Netzwerkfreigabe (Server Message Block), in der alle Speicherorte für benutzerdefinierte Einstellungen gespeichert sind. Ein geplanter Task im UE-V-Agent überprüft diesen Standort einmal täglich und aktualisiert sein Synchronisierungsverhalten basierend auf den Vorlagen in diesem Ordner.

Der UE-V-Agent registriert Vorlagen, die in diesem Ordner nach dem letzten Überprüfen des Ordners hinzugefügt oder aktualisiert wurden, und hebt die Registrierung von Vorlagen auf, die entfernt werden. Standardmäßig werden Vorlagen um 3:30 Uhr einmal pro Tag registriert und nicht registriert. Ortszeit durch den Aufgabenplaner und beim Systemstart. Informationen zum Anpassen der Häufigkeit dieser geplanten Aufgabe finden Sie unter [Ändern der Häufigkeit von geplanten Aufgaben in UE-V 2. x](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).

Sie können den Katalogpfad der Einstellungs Vorlage mithilfe der Befehlszeilenoptionen für die Installation, Gruppenrichtlinie, WMI oder Windows PowerShell konfigurieren. Vorlagen, die im Katalogpfad für Einstellungs Vorlagen gespeichert sind, werden automatisch von einem geplanten Vorgang registriert und nicht registriert.

**So konfigurieren Sie den Vorlagenkatalog für die Einstellungen für UE-V 2. x**

1.  Erstellen Sie einen neuen Ordner auf dem Computer, auf dem der Vorlagenkatalog für UE-V-Einstellungen gespeichert ist.

2.  Legen Sie die folgenden SMB-Berechtigungen (Freigabeebene) für den Katalogordner "Einstellungs Vorlagen" ein.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Benutzerkonto</strong></th>
    <th align="left"><strong>Empfohlene Berechtigungen</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Jeder</p></td>
    <td align="left"><p>Keine Berechtigungen</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domänencomputer</p></td>
    <td align="left"><p>Lesen von Berechtigungsstufen</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administratoren</p></td>
    <td align="left"><p>Berechtigungsstufen für Lesen/Schreiben</p></td>
    </tr>
    </tbody>
    </table>

     

3.  Legen Sie die folgenden NTFS-Dateisystemberechtigungen für den Ordner "Einstellungs Vorlagenkatalog" ein.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Benutzerkonto</th>
    <th align="left">Empfohlene Berechtigungen</th>
    <th align="left">Anwenden auf</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Ersteller/Besitzer</p></td>
    <td align="left"><p>Vollzugriff</p></td>
    <td align="left"><p>Dieser Ordner, Unterordner und Dateien</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domänencomputer</p></td>
    <td align="left"><p>Ordnerinhalte auflisten und lesen</p></td>
    <td align="left"><p>Dieser Ordner, Unterordner und Dateien</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Jeder</p></td>
    <td align="left"><p>Keine Berechtigungen</p></td>
    <td align="left"><p>Keine Berechtigungen</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administratoren</p></td>
    <td align="left"><p>Vollzugriff</p></td>
    <td align="left"><p>Dieser Ordner, Unterordner und Dateien</p></td>
    </tr>
    </tbody>
    </table>

     

4.  Klicken Sie auf **OK** , um die Dialogfelder zu schließen.

Die Netzwerkfreigabe muss mindestens die Berechtigungen für die Gruppe "Domänencomputer" erteilen. Gewähren Sie darüber hinaus Zugriffsberechtigungen für den Netzwerkfreigabeordner für Administratoren, die die gespeicherten Vorlagen verwalten sollen.

## <a href="" id="createcustomtemplates"></a>Erstellen von Speicherort Vorlagen für benutzerdefinierte Einstellungen


Verwenden Sie den UE-V-Generator zum Erstellen von Einstellungen-Speicherort Vorlagen für Branchenanwendungen oder andere benutzerdefinierte Anwendungen. Nachdem die Vorlage für eine Anwendung erstellt wurde, können Sie Sie auf Computern bereitstellen, damit die Einstellungen für diese Anwendung synchronisiert werden.

**So erstellen Sie eine Standort Vorlage für UE-v-Einstellungen mit dem UE-v-Generator**

1.  Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft User Experience Virtualization**, und klicken Sie dann auf **Microsoft User Experience Virtualization Generator**.

2.  Klicken Sie auf **Vorlage zum Erstellen einer Einstellungsposition**.

3.  Geben Sie die Anwendung an. Navigieren Sie zum Dateipfad der Anwendung (. exe) oder der Anwendungsverknüpfung (. lnk), für die Sie eine Vorlage für eine Einstellungsposition erstellen möchten. Geben Sie die Befehlszeilenargumente (sofern vorhanden) und das Arbeitsverzeichnis an, sofern vorhanden. Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

    **Hinweis**  Bevor die Anwendung gestartet wird, zeigt das System eine Aufforderung zur **Steuerung des Benutzerkontos**an. Zum Überwachen der Registrierungs-und Dateispeicherorte, die die Anwendung zum Speichern von Einstellungen verwendet, ist eine Berechtigung erforderlich.

     

4.  Schließen Sie die Anwendung, nachdem die Anwendung gestartet wurde. Der UE-V-Generator zeichnet die Speicherorte auf, an denen die Anwendung die Einstellungen speichert.

5.  Klicken Sie nach Abschluss des Prozesses auf **weiter** , um fortzufahren.

6.  Überprüfen und aktivieren Sie die Kontrollkästchen neben den entsprechenden Speicherorten für Registrierungseinstellungen und Einstellungen für die Dateispeicherorte, die für diese Anwendung synchronisiert werden sollen. Die Liste enthält die folgenden beiden Kategorien für die Einstellungen für die Speicherorte:

    -   **Standard**: Anwendungseinstellungen, die in der Registrierung unter dem HKEY \ _CURRENT \ _User Schlüssel oder in den Dateiordnern unter \ \ **Users** \ \ \ [Benutzername \] \ \ **AppData**  \\  **Roaming**gespeichert sind. Der UE-V-Generator enthält standardmäßig diese Einstellungen.

    -   Nicht **Standard**: Anwendungseinstellungen, die außerhalb der Speicherorte gespeichert sind, werden in den bewährten Methoden für Einstellungsdaten Speicher (optional) angegeben. Dazu gehören Dateien und Ordner unter **Benutzer** \ \ \ [Benutzername \] \ \ **AppData**  \\  **local**. Überprüfen Sie diese Speicherorte, um zu bestimmen, ob Sie Sie in die Vorlage für den Einstellungs Speicherort einbeziehen möchten. Aktivieren Sie die Kontrollkästchen Speicherorte, um Sie einzubeziehen.

    Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

7.  Überprüfen und bearbeiten Sie alle **Eigenschaften**, **Registrierungs** Speicherorte und **Datei** Speicherorte für die Vorlage Speicherort für Einstellungen.

    -   Bearbeiten Sie die folgenden Eigenschaften auf der Registerkarte " **Eigenschaften** ":

        -   **Anwendungsname**: der Name der Anwendung, der in der Beschreibung der Programmdatei Eigenschaften geschrieben ist.

        -   **Programmname**: der Name des Programms, das aus den Programmdatei Eigenschaften übernommen wird. Dieser Name hat in der Regel die Dateinamenerweiterung exe.

        -   **Produktversion**: die Produktversionsnummer der exe-Datei der Anwendung. Mit dieser Eigenschaft können Sie in Verbindung mit der **Dateiversion**ermitteln, welche Anwendungen von der Vorlage für die Einstellungsposition abzielen. Diese Eigenschaft akzeptiert eine Hauptversionsnummer. Wenn diese Eigenschaft leer ist, gilt die Vorlage für die Einstellungsposition für alle Versionen des Produkts.

        -   **Dateiversion**: die Dateiversionsnummer der exe-Datei der Anwendung. Mit dieser Eigenschaft können Sie in Verbindung mit der **Produktversion**ermitteln, welche Anwendungen von der Vorlage für die Einstellungsposition abzielen. Diese Eigenschaft akzeptiert eine Hauptversionsnummer. Wenn diese Eigenschaft leer ist, gilt die Vorlage für die Einstellungsposition für alle Versionen des Programms.

        -   **Name der Vorlagen Autorin** (optional): der Name der Vorlage für den Speicherort der Einstellungen.

        -   **E-Mail-Vorlage für Vorlagenautor** (optional): die e-Mail-Adresse der Vorlage "Speicherort für Einstellungen".

    -   Auf der Registerkarte " **Registrierung** " sind der **Schlüssel** und der **Bereich** der Registrierungsspeicherorte aufgeführt, die in der Vorlage "einstellungensort" enthalten sind. Bearbeiten Sie die Registrierungsspeicherorte mithilfe des Dropdownmenüs **Aufgaben** . Mit Aufgaben können Sie neue Schlüssel hinzufügen, den Namen oder den Bereich vorhandener Schlüssel bearbeiten, Schlüssel löschen und die Registrierung durchsuchen, in der sich die Schlüssel befinden. Verwenden Sie den Bereich **alle Einstellungen** , um alle Registrierungseinstellungen unter dem angegebenen Schlüssel einzubeziehen. Verwenden Sie **alle Einstellungen und Unterschlüssel** , um alle Registrierungseinstellungen unter den angegebenen Tasten, Unterschlüsseln und Unterschlüssel Einstellungen einzubeziehen.

    -   Auf der Registerkarte " **Dateien** " werden der Dateipfad und die Dateimaske der Dateispeicherorte aufgeführt, die in der Vorlage für die Einstellungsposition enthalten sind. Bearbeiten Sie die Dateispeicherorte mithilfe des Dropdownmenüs **Aufgaben** . Mit Aufgaben für Dateispeicherorte können Sie neue Dateien oder Ordnerspeicherorte hinzufügen, den Bereich vorhandener Dateien oder Ordner bearbeiten, Dateien oder Ordner löschen und den ausgewählten Speicherort in Windows-Explorer öffnen. Lassen Sie die Dateimaske leer, um alle Dateien in den angegebenen Ordner einzubeziehen.

8.  Klicken Sie auf **Erstellen**und dann auf **Speichern** , um die Vorlage für die Einstellungsposition auf dem Computer zu speichern.

9.  Klicken Sie auf **Schließen** , um den Assistenten für Einstellungs Vorlagen zu schließen. Beenden Sie die UE-V-Generator Anwendung.

    Nachdem Sie die Vorlage für die Einstellungsposition für eine Anwendung erstellt haben, sollten Sie die Vorlage testen. Stellen Sie die Vorlage in einer Lab-Umgebung bereit, bevor Sie Sie in der Produktion im Unternehmen einsetzen.

[Anwendungsvorlagen Schema Referenz für UE-v](https://technet.microsoft.com/library/dn763947.aspx) beschreibt die XML-Struktur der Standort Vorlage für UE-v-Einstellungen und bietet Anleitungen für die Bearbeitung dieser Dateien.

## <a href="" id="deploycustomtemplates"></a>Bereitstellen der Speicherort Vorlagen für benutzerdefinierte Einstellungen


Nachdem Sie eine Vorlage für die Einstellungsposition mit dem UE-V-Generator erstellt haben, sollten Sie Sie testen, um sicherzustellen, dass die Anwendungseinstellungen ordnungsgemäß synchronisiert werden. Anschließend können Sie die Vorlage für die Einstellungsposition sicher auf Computern im Unternehmen bereitstellen.

Einstellungen Speicherort Vorlagen können mithilfe einer der folgenden Methoden bereitgestellt werden:

-   Ein ESD-System (Enterprise Software Distribution) wie System Center Configuration Manager

-   Gruppenrichtlinienvoreinstellungen

-   Ein UE-V-Einstellungs Vorlagenkatalog

Vorlagen, die mithilfe eines ESD-Systems oder von Gruppenrichtlinienobjekten bereitgestellt werden, müssen über die UE-V-Windows-Verwaltungsinstrumentation (WMI) oder Windows PowerShell registriert werden. Vorlagen, die im Katalogspeicherort für Einstellungs Vorlagen gespeichert sind, werden vom UE-V-Agent automatisch registriert.

**So verwenden Sie den Katalogpfad der Einstellungs Vorlage zum Bereitstellen von UE-V-Einstellungen Speicherort Vorlagen**

1.  Navigieren Sie zu dem Netzwerkfreigabeordner, der als Vorlagenkatalog für Einstellungen definiert ist.

2.  Hinzufügen, entfernen oder Aktualisieren von Einstellungen für Standort Vorlagen im Einstellungs Vorlagenkatalog, um die für UE-v-Computer gewünschte UE-v-Agent-Vorlagenkonfiguration wiederzugeben.

    **Hinweis**  Vorlagen auf Computern werden täglich aktualisiert. Das Update basiert auf Änderungen am Vorlagenkatalog für Einstellungen.

     

3.  Wenn Sie Vorlagen auf einem Computer, auf dem der UE-V-Agent ausgeführt wird, manuell aktualisieren möchten, öffnen Sie eine Eingabeaufforderung mit erhöhten Rechten, und navigieren Sie zu **% Program Files%\\Microsoft User Experience Virtualization \ \ Agent \ \ &lt; x86 oder x64 &gt; **, und führen Sie dann **ApplySettingsTemplateCatalog.exe**aus.

    **Hinweis**  Dieses Programm wird automatisch während des Computerstarts und täglich bei 3:30 A. M ausgeführt. , um alle neuen Vorlagen zu sammeln, die dem Katalog kürzlich hinzugefügt wurden.

     






## Verwandte Themen


[Vorbereiten einer UE-V 2. x-Bereitstellung](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Bereitstellen der erforderlichen Features für UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md)

 

 





