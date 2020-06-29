---
title: Konfigurieren von UE-V 2. x mit System Center Configuration Manager 2012
description: Konfigurieren von UE-V 2. x mit System Center Configuration Manager 2012
author: dansimp
ms.assetid: 9a4e2a74-7646-4a77-b58f-2b4456487295
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 2ff9ccc1a17db31471549ece37461558768c3a2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810537"
---
# Konfigurieren von UE-V 2. x mit System Center Configuration Manager 2012


Nachdem Sie die Microsoft User Experience Virtualization (UE-v) 2,0, 2,1 oder 2,1 SP1 und die erforderlichen Features installiert haben, muss UE-v konfiguriert sein. Das UE-v-Konfigurationspaket bietet Administratoren die Möglichkeit, das Feature "Konformitäts Einstellungen" von System Center Configuration Manager 2012 SP1 oder höher zu verwenden, um konsistente Konfigurationen auf Websites anzuwenden, auf denen UE-v und Configuration Manager installiert sind.

## Unterstützte Features des UE-V-Konfigurationspakets


Das UE-V-Konfigurationspaket enthält Tools, mit denen Sie die folgenden Aufgaben ausführen können:

-   Erstellen oder Aktualisieren von Basislinien für die Verteilung von Standort Vorlagen für UE-V-Einstellungen

    -   Definieren von UE-V-Vorlagen für die Registrierung oder Nichtregistrierung

    -   Aktualisieren von Konfigurationselementen und Basisplänen für UE-V-Vorlagen, wenn Vorlagen hinzugefügt oder aktualisiert werden

    -   Verteilen und Registrieren von UE-V-Vorlagen mithilfe der standardmäßigen Konfigurationselement Bereinigung

-   Erstellen oder aktualisieren Sie ein UE-V-Agent-Richtlinien Konfigurationselement, um diese Einstellungen festzulegen oder zu löschen.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Maximale Paketgröße</p></td>
    <td align="left"><p>Aktivieren/Deaktivieren der Windows-App-Synchronisierung</p></td>
    <td align="left"><p>Auf Synchronisierung beim Anwendungsstart warten</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Festlegen der Import Verzögerung</p></td>
    <td align="left"><p>Synchronisieren nicht aufgelisteter Windows-apps</p></td>
    <td align="left"><p>Auf die Synchronisierung bei der Anmeldung warten</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Benachrichtigung zum Importieren von Einstellungen</p></td>
    <td align="left"><p>IT-Kontakt-URL</p></td>
    <td align="left"><p>Auf Synchronisierungs Timeout warten</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Speicherpfad für Einstellungen</p></td>
    <td align="left"><p>Sie wenden sich an einen beschreibenden Text</p></td>
    <td align="left"><p>Katalogpfad für Einstellungs Vorlagen</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Synchronisierungs Aktivierung</p></td>
    <td align="left"><p>Taskleistensymbol aktiviert</p></td>
    <td align="left"><p>Starten/Beenden des UE-V-Agent-Diensts</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Sync-Methode</p></td>
    <td align="left"><p>Benachrichtigung zur ersten Verwendung</p></td>
    <td align="left"><p>Definieren, welche Windows-apps Roaming-Einstellungen durchführen</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Synchronisierungs Timeout</p></td>
    <td align="left"><p></p></td>
    <td align="left"><p></p></td>
    </tr>
    </tbody>
    </table>

     

-   Überprüfen Sie die Kompatibilität, indem Sie bestätigen, dass UE-V ausgeführt wird.

## Generieren eines UE-V-Agentenrichtlinien-Konfigurationselements


Alle UE-V-Agentenrichtlinien und-Konfigurationen werden über ein einzelnes Konfigurationselement verteilt, das mit dem UevAgentPolicyGenerator.exe-Tool generiert wird. Dieses Tool liest die gewünschte Konfiguration aus einer XML-Konfigurationsdatei und erstellt eine CI, die die Einstellungen für Ermittlung und Behebung enthält, die erforderlich sind, um den Computer in die Konformität zu bringen.

Die CAB-Datei für das UE-V-Agent-Richtlinien Konfigurationselement wird mithilfe des Befehlszeilentools UevTemplateBaselineGenerator.exe erstellt, das die folgenden Parameter aufweist:

-   Website-Website &lt; Code&gt;

-   Richtlinien &lt; Name &gt; -Name optional: standardmäßig "UE-V-Agent-Richtlinie", wenn nicht vorhanden

-   PolicyDescription &lt; Beschreibung &gt; Optional: eine Beschreibung wird bereitgestellt, wenn Sie nicht vorhanden ist.

-   CabFilePath &lt; Vollständiger Pfad zum Konfigurationselement. CAB-Datei&gt;

-   Konfigurations &lt; Datei, vollständiger Pfad zur XML-Konfigurationsdatei für Agents&gt;

**Hinweis**  Es kann erforderlich sein, die PowerShell-Ausführungsrichtlinie so zu ändern, dass diese Skripts in Ihrer Umgebung ausgeführt werden können. Führen Sie die folgenden Schritte in der Configuration Manager-Konsole aus:

1.  Auswählen von Einstellungen für den **Administrations &gt; Client &gt; **

2.  Setzen Sie auf der Registerkarte **Benutzer-Agent** die **PowerShell-Ausführungsrichtlinie** auf **Bypass**

<a href="" id="create"></a>**Erstellen des ersten UE-V-Richtlinien Konfigurationselements**

1.  Kopieren Sie die Konfigurationsdatei für die Standardeinstellungen aus dem Installationsverzeichnis des UE-V config Packs an einen Speicherort, der für Ihre ConfigMgr-Verwaltungskonsole sichtbar ist:

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\AgentConfiguration.xml c:\<target path>
    ```

    Die Standardkonfigurationsdatei enthält fünf Abschnitte:

    <a href="" id="computer-policy"></a>**Computer Richtlinie**  
    Alle UE-V-Einstellungen auf Computerebene. Das DesiredState-Attribut kann

    -   So **eingestellt** , dass der Wert in der Registrierung zugewiesen ist

    -   **Löschen** , um die Einstellung zu entfernen

    -   **Nicht verwaltet** , damit das Konfigurationselement in seinem aktuellen Zustand bleibt

    Entfernen Sie keine Zeilen aus diesem Abschnitt. Legen Sie die DesiredState stattdessen auf "nicht verwaltet", wenn Sie nicht möchten, dass der Configuration Manager aktuelle oder Standardwerte ändert.

    <a href="" id="currentcomputeruserpolicy"></a>**CurrentComputerUserPolicy**  
    Alle UE-V-Einstellungen auf Benutzerebene Diese Einträge überschreiben die Computereinstellungen für einen Benutzer. Das DesiredState-Attribut kann

    -   So **eingestellt** , dass der Wert in der Registrierung zugewiesen ist

    -   **Löschen** , um die Einstellung zu entfernen

    -   **Nicht verwaltet** , damit das Konfigurationselement in seinem aktuellen Zustand bleibt

    Entfernen Sie keine Zeilen aus diesem Abschnitt. Legen Sie die DesiredState stattdessen auf "nicht verwaltet", wenn Sie nicht möchten, dass der Configuration Manager aktuelle oder Standardwerte ändert.

    <a href="" id="services"></a>**Dienste**  
    Einträge in diesem Abschnitt Steuern des Dienstvorgangs. Die Standardkonfigurationsdatei enthält einen einzelnen Eintrag für die UevAgentService-Datei. Das DesiredState-Attribut kann auf **Running** oder **Stopped**eingestellt werden.

    <a href="" id="windows8appscomputerpolicy"></a>**Windows8AppsComputerPolicy**  
    Alle Synchronisierungseinstellungen für Windows-App auf Computerebene. Jedem in diesem Abschnitt aufgelisteten PackageFamilyName kann eine DesiredState von zugewiesen werden.

    -   **Aktiviert** , um die Einstellungen zu durchlaufen

    -   **Deaktiviert** , um zu verhindern, dass Roaming-Einstellungen durchlaufen werden

    -   **Gelöscht** , damit der Eintrag aus dem UE-V-Steuerelement entfernt wird

    In diesem Abschnitt können zusätzliche Zeilen basierend auf der Liste der installierten Windows-apps hinzugefügt werden, die mit dem PowerShell-Cmdlet GetAppxPackage angezeigt werden können.

    <a href="" id="windows8appscurrentcomputeruserpolicy"></a>**Windows8AppsCurrentComputerUserPolicy**  
    Identisch mit dem Windows8AppsComputerPolicy mit Einstellungen, die die Computereinstellungen für einen einzelnen Benutzer außer Kraft setzen.

2.  Bearbeiten Sie die Konfigurationsdatei, indem Sie die Felder für den gewünschten Zustand und die Werte ändern.

3.  Führen Sie diesen Befehl auf einem Computer aus, auf dem die ConfigMgr-Verwaltungskonsole ausgeführt wird:

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevAgentPolicyGenerator.exe –Site ABC –CabFilePath "C:\MyCabFiles\UevPolicyItem.cab" –ConfigurationFile "c:\AgentConfiguration.xml"
    ```

4.  Importieren der CAB-Datei mithilfe der ConfigMgr-Konsole oder des PowerShell-Import-CMConfigurationItem

**Aktualisieren eines UE-V-Richtlinien Konfigurationselements**

1.  Bearbeiten Sie die Konfigurationsdatei, indem Sie die Felder für den gewünschten Zustand und die Werte ändern.

2.  Führen Sie den Befehl aus Schritt 3 in [Erstellen des ersten UE-V-Richtlinien Konfigurationselements](#create)aus. Wenn Sie den Namen mit dem Parameter PolicyName geändert haben, stellen Sie sicher, dass Sie denselben Namen eingeben.

3.  Importieren Sie die CAB-Datei erneut. Die Version in ConfigMgr wird aktualisiert.

## Erstellen einer UE-V-Vorlagen Basislinie
UE-V-Vorlagen werden mithilfe einer Baseline verteilt, die mehrere Konfigurationselemente enthält. Jedes Konfigurationselement enthält die Ermittlungs-und Korrekturskripts, die zum Installieren einer UE-V-Vorlage erforderlich sind. Die tatsächliche UE-V-Vorlage wird in das Behebungs Skript für die Verteilung unter Verwendung der Standardfunktionalität für Konfigurationselemente eingebettet.

Der Basisplan der UE-V-Vorlage wird mithilfe des Befehlszeilentools UevTemplateBaselineGenerator.exe erstellt, das die folgenden Parameter aufweist:

-   Website-Website &lt; Code&gt;

-   Baselinename &lt; &gt; -Name (optional: standardmäßig "UE-V-Vorlagen Verteilungs Basisplan", wenn nicht vorhanden)

-   BaselineDescription &lt; Beschreibung &gt; (optional: eine Beschreibung wird bereitgestellt, wenn nicht vorhanden)

-   TemplateFolder &lt; UE-V-Vorlagenordner&gt;

-   Registrieren einer durch &lt; Kommas getrennten Vorlagendatei Liste&gt;

-   Aufheben der Registrierung der Liste der durch &lt; Kommas getrennten Vorlagen&gt;

-   CabFilePath &lt; Vollständiger Pfad zur zu Generier-Baseline-CAB-Datei&gt;

Das Ergebnis ist eine Baseline-CAB-Datei, die in Configuration Manager importiert werden kann. Wenn Sie zu einem späteren Zeitpunkt eine Vorlage aktualisieren oder hinzufügen, können Sie den Befehl mit dem gleichen Basisplan erneut ausführen. Beim Importieren der CAB-Version werden die geänderten Vorlagen in CI-Versionsupdates angezeigt.

### <a href="" id="create2"></a>Erstellen des ersten Basisplans für die UE-V-Vorlage

1.  Erstellen Sie einen "Master"-Satz von UE-V-Vorlagen in einem stabilen Ordnerspeicherort, der auf dem Computer sichtbar ist, auf dem Ihre ConfigMgr-Verwaltungskonsole ausgeführt wird. Wenn Vorlagen hinzugefügt oder aktualisiert werden, wird dieser Ordner für die Verteilung abgerufen. Die erste Liste der Vorlagen kann von einem Computer kopiert werden, auf dem UE-V installiert ist. Der Standardspeicherort für Vorlagen ist c:\\Programme c:\\Programme\\Microsoft-Benutzeroberfläche Virtualization\\Templates.

2.  Erstellen Sie eine text.bat-Datei, in der Sie den Befehl Vorlagen Generator hinzufügen können. Dies ist optional, bewirkt aber eine einfachere Regenerierung, wenn Sie die Befehlsparameter speichern.

3.  Fügen Sie der bat-Datei den Befehl und die Parameter hinzu, die den Basisplan generieren soll. Im folgenden Beispiel wird ein Basisplan erstellt, der Notepad und Calculator verteilt:

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevTemplateBaselineGenerator.exe –Site "ABC" –TemplateFolder "C:\ProductionUevTemplates" –Register "MicrosoftNotepad.xml, MicrosoftCalculator.xml" –CabFilePath "C:\MyCabFiles\UevTemplateBaseline.cab"
    ```

4.  Führen Sie die bat-Datei aus, um UevTemplateBaseline.cab bereit für den Import in Configuration Manager zu erstellen.

### Aktualisieren einer UE-V-Vorlagen Basislinie

Der Vorlagen Generator verwendet die Vorlagenversion, um zu ermitteln, ob eine Vorlage aktualisiert werden soll. Wenn Sie eine Vorlage ändern und die Version aktualisieren, vergleicht der Baseline-Generator die Vorlage im Masterordner mit der Vorlage, die in der CI auf dem ConfigMgr-Server enthalten ist. Wenn ein Unterschied gefunden wird, werden die generierten Baseline-und modified-CI-Versionen aktualisiert.

Wenn Sie eine neue Notizblock Vorlage verteilen möchten, führen Sie die folgenden Schritte aus:

1.  Aktualisieren Sie die Vorlage und die Vorlagenversion, die sich im &lt; Version- &gt; Element der Vorlage befindet.

2.  Kopieren Sie die Vorlage in das Mastervorlagen Verzeichnis.

3.  Führen Sie den Befehl in der bat-Datei aus, die Sie in Schritt 3 unter [Erstellen der ersten UE-V-Vorlagen Basislinie](#create2)erstellt haben.

4.  Importieren Sie die generierte CAB-Datei mithilfe der Konsole oder PowerShell-Import-CMBaseline in ConfigMgr.

## Abrufen des UE-V-Konfigurationspakets


Das UE-V-Konfigurationspaket für Configuration Manager 2012 SP1 oder höher kann [hier](https://go.microsoft.com/fwlink/?LinkId=317263)heruntergeladen werden.






## Verwandte Themen


[Verwalten von Konfigurationen für UE-V 2.x](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





