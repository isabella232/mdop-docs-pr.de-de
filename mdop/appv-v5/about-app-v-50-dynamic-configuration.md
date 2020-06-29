---
title: Informationen zur dynamischen Konfiguration in App-V 5.0
description: Informationen zur dynamischen Konfiguration in App-V 5.0
author: dansimp
ms.assetid: 88afaca1-68c5-45c4-a074-9371c56b5804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0294a60570d6dea99193c8bd411639c4888ae6b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806144"
---
# Informationen zur dynamischen Konfiguration in App-V 5.0


Sie können die dynamische Konfiguration verwenden, um ein App-V 5,0-Paket für einen Benutzer anzupassen. Verwenden Sie die folgenden Informationen, um eine vorhandene dynamische Konfigurationsdatei zu erstellen oder zu bearbeiten.

Wenn Sie die dynamische Konfigurationsdatei bearbeiten, passt Sie an, wie ein App-V 5,0-Paket für einen Benutzer oder eine Gruppe ausgeführt wird. Auf diese Weise können Sie eine bequemere Methode für die Paket Anpassung bereitstellen, indem Sie die Notwendigkeit, Pakete mithilfe der gewünschten Einstellungen neu zu sequenzieren, entfernen und eine Möglichkeit bieten, Paketinhalte und benutzerdefinierte Einstellungen unabhängig zu halten.

## Erweitert: dynamische Konfiguration


Virtuelle Anwendungspakete enthalten ein Manifest, das alle Kerninformationen für das Paket enthält. Diese Informationen enthalten die Standardeinstellungen für die Paketeinstellungen und bestimmen die Einstellungen in der grundlegendsten Form (ohne zusätzliche Anpassung). Wenn Sie diese Standardeinstellungen für einen bestimmten Benutzer oder eine bestimmte Gruppe anpassen möchten, können Sie die folgenden Dateien erstellen und bearbeiten:

-   Benutzerkonfigurationsdatei

-   Konfigurationsdatei für die Bereitstellung

Die vorherigen XML-Dateien geben Paketeinstellungen an, sodass Pakete angepasst werden können, ohne die Pakete direkt zu beeinflussen. Beim Erstellen eines Pakets generiert der Sequencer automatisch Standard Bereitstellungs-und Benutzer Konfigurations XML-Dateien mit den Daten des paketmanifests. Aus diesem Grund spiegeln diese automatisch generierten Konfigurationsdateien einfach die Standardeinstellungen wider, die das Paket von der Art der Konfiguration während der Sequenzierung abbildet. Wenn Sie diese Konfigurationsdateien auf ein Paket in dem vom Sequencer generierten Formular anwenden, verfügen die Pakete über die gleichen Standardeinstellungen, die aus ihrem Manifest stammen. Dadurch erhalten Sie eine Paket spezifische Vorlage, mit der Sie beginnen können, wenn eine der Standardeinstellungen geändert werden muss.

**Hinweis**  Die folgenden Informationen können nur verwendet werden, um sequenzierte Sequenzer-Konfigurationsdateien zu ändern, um Pakete anzupassen, um bestimmte Benutzer-oder Gruppenanforderungen zu erfüllen.

 

### Inhalt der dynamischen Konfigurationsdatei

Alle Ergänzungen, Löschungen und Aktualisierungen in den Konfigurationsdateien müssen in Bezug auf die Standardwerte erfolgen, die durch die Manifestinformationen des Pakets angegeben werden. Überprüfen Sie die folgende Tabelle:

<table>
<colgroup>
<col width="100%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Datei "User Configuration. xml"</p></td>
</tr>
<tr class="even">
<td align="left"><p>Datei "Deployment Configuration. xml"</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Paket Manifest</p></td>
</tr>
</tbody>
</table>

 

Die vorherige Tabelle zeigt, wie die Dateien gelesen werden. Der erste Eintrag stellt dar, was zuletzt gelesen wird, daher hat sein Inhalt Vorrang. Daher enthalten alle Pakete inhärente und Standardeinstellungen aus dem Paketmanifest. Wenn eine XML-Datei für die Bereitstellungskonfiguration mit angepassten Einstellungen angewendet wird, werden die Standardwerte des paketmanifests außer Kraft gesetzt. Wenn zuvor eine XML-Datei vom Benutzer "Configuration. xml" mit angepassten Einstellungen angewendet wird, werden sowohl die Bereitstellungskonfiguration als auch die Standardwerte des paketmanifests außer Kraft gesetzt.

In der folgenden Liste werden weitere Informationen zu den beiden Dateitypen angezeigt:

-   **User Configuration File (userconfig)** – ermöglicht Ihnen, benutzerdefinierte Einstellungen für ein Paket anzugeben oder zu ändern. Diese Einstellungen werden für einen bestimmten Benutzer angewendet, wenn das Paket auf einem Computer mit dem App-V 5,0-Client bereitgestellt wird.

-   **Deployment Configuration File (DeploymentConfig)** – ermöglicht Ihnen, die Standardeinstellungen für ein Paket anzugeben oder zu ändern. Diese Einstellungen werden für alle Benutzer angewendet, wenn ein Paket auf einem Computer mit dem App-V 5,0-Client bereitgestellt wird.

Um die Einstellungen für ein Paket für eine bestimmte Gruppe von Benutzern auf einem Computer anzupassen oder um Änderungen vorzunehmen, die auf lokale Benutzerspeicherorte wie HKCU angewendet werden, sollte die userconfig-Datei verwendet werden. Wenn Sie die Standardeinstellungen eines Pakets für alle Benutzer auf einem Computer ändern oder Änderungen vornehmen möchten, die auf globale Speicherorte wie HKEY \ _LOCAL \ _MACHINE und den Ordner alle Benutzer angewendet werden, sollte die DeploymentConfig-Datei verwendet werden.

Die userconfig-Datei enthält Konfigurationseinstellungen, die auf einen einzelnen Benutzer angewendet werden können, ohne dass dies Auswirkungen auf andere Benutzer auf einem Client hat:

-   Erweiterungen, die pro Benutzer in das System System integriert werden:-Verknüpfungen, Dateitypzuordnungen, URL-Protokolle, AppPaths, Software-Clients und com

-   Virtuelle Subsysteme:-Anwendungsobjekte, Umgebungsvariablen, Registrierungsänderungen, Dienste und Schriftarten

-   Skripts (nur Benutzerkontext)

-   Verwaltungsautorität (zum Steuern der Koexistenz von Paketen mit App-V 4,6)

Die DeploymentConfig-Datei enthält Konfigurationseinstellungen in zwei Abschnitten, eine relativ zum Computerkontext und eine relativ zum Benutzerkontext, in dem die gleichen Funktionen wie in der userconfig-Liste oben aufgeführt sind:

-   Alle userconfig-Einstellungen oben

-   Erweiterungen, die nur global für alle Benutzer angewendet werden können

-   Virtuelle Subsysteme, die für globale Computer Standorte konfiguriert werden können, beispielsweise Registry

-   Produkt Quell-URL

-   Skripts (nur Computerkontext)

-   Steuerelemente zum kündigen von untergeordneten Prozessen

### Dateistruktur

Die Struktur der Dynamic Configuration-Datei der App-V 5,0 wird im folgenden Abschnitt erläutert.

### Dynamic User-Konfigurationsdatei

**Kopfzeile** : die Kopfzeile einer dynamischen Benutzerkonfigurationsdatei lautet wie folgt:

&lt;? XML Version = "1.0" Encoding = "UTF-8"? &gt; &lt; UserConfiguration **Packaged**= "1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reserviert" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;

Die **Paket** -Nr ist derselbe Wert wie in der Manifestdatei vorhanden.

**Body** – der Text der dynamischen Benutzerkonfigurationsdatei kann alle in der Manifestdatei definierten App-Erweiterungspunkte sowie Informationen zum Konfigurieren virtueller Anwendungen umfassen. Im Textbereich sind vier Unterabschnitte zulässig:

1. **Anwendungen** – alle App-Erweiterungen, die in der Manifestdatei in einem Paket enthalten sind, werden mit einer Anwendungs-ID zugewiesen, die auch in der Manifestdatei definiert ist. Dadurch können Sie alle Erweiterungen für eine bestimmte Anwendung innerhalb eines Pakets aktivieren oder deaktivieren. Die **Anwendungs-ID** muss in der Manifestdatei vorhanden sein, oder Sie wird ignoriert.

   &lt;UserConfiguration **Packaged**= "1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reserviert" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;

   &lt;Anwendungen&gt;

   &lt;!--Keine neue Anwendung in der Richtlinie definiert werden kann. AppV-Client ignoriert jede Anwendungs-ID, die sich nicht auch in der Manifestdatei befindet--&gt;

   &lt;Application ID = "{a56fa627-c35f-4a01-9e79-7d36aed8225a}" Enabled = "false"&gt;

   &lt;/Application&gt;

   &lt;/Applications&gt;

   …

   &lt;/UserConfiguration&gt;

2. **Subsysteme** -AppExtensions und andere Subsysteme sind unter den Teilsystemen als untergeordnete Knoten angeordnet &lt; &gt; :

   &lt;UserConfiguration **Packaged**= "1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reserviert" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;

   &lt;Subsysteme&gt;

   ..

   &lt;/Subsystems&gt;

   ..

   &lt;/UserConfiguration&gt;

   Jedes Subsystem kann mithilfe des Attributs "**Enabled**" aktiviert/deaktiviert werden. Nachfolgend sind die verschiedenen Subsysteme und Verwendungsbeispiele aufgeführt.

   **Erweiterungen**

   Einige Subsysteme (Erweiterungs Subsysteme)-Steuerelement Erweiterungen. Diese Subsysteme sind:-Verknüpfungen, Dateitypzuordnungen, URL-Protokolle, AppPaths, Software-Clients und com

   Erweiterungs Subsysteme können unabhängig vom Inhalt aktiviert und deaktiviert werden.  Wenn Tastenkombinationen aktiviert sind, verwendet der Clientstandard mäßig die Verknüpfungen, die im Manifest enthalten sind. Jedes Erweiterungs Subsystem kann einen &lt; Erweiterungsknoten enthalten &gt; . Wenn dieses untergeordnete Element vorhanden ist, wird der Client den Inhalt in der Manifestdatei für dieses Subsystem ignorieren und nur den Inhalt der Konfigurationsdatei verwenden.

   Beispiel für die Verwendung des Subsystems "Verknüpfungen":

   1.  Wenn der Benutzer dies in der Dynamic-oder Deployment config-Datei definiert hat:

                                    **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions&gt;**

                                                 ...

                                                **&lt;/Extensions&gt;**

                                    **&lt;/Shortcuts&gt;**

                         Content in the manifest will be ignored.   

   2.  Wenn der Benutzer nur Folgendes definiert hat:

                                   **&lt;Shortcuts  Enabled="true"/&gt;**

                         Then the content in the Manifest will be integrated during publishing.

   3.  Wenn der Benutzer Folgendes definiert:

                                  **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions/&gt;**

                                    **&lt;/Shortcuts&gt;**

   Dann werden alle Tastenkombinationen im Manifest weiterhin ignoriert. Es werden keine Tastenkombinationen integriert.

   Die unterstützten Erweiterungs Subsysteme sind:

   **Tastenkombinationen:** Damit werden Tastenkombinationen gesteuert, die in das lokale System integriert werden. Nachfolgend finden Sie ein Beispiel mit zwei Tastenkombinationen:

   &lt;Subsysteme&gt;

   &lt;Tastenkombinationen aktiviert = "wahr"&gt;

     &lt;Extensions&gt;

       &lt;Extension Category="AppV.Shortcut"&gt;

         &lt;Shortcut&gt;

           &lt;File&gt;\[{Common Programs}\]\\Microsoft Contoso\\Microsoft ContosoApp Filler 2010.lnk&lt;/File&gt;

           &lt;Target&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/Target&gt;

           &lt;Icon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\inficon.exe&lt;/Icon&gt;

           &lt;Arguments /&gt;

           &lt;WorkingDirectory /&gt;

           &lt;AppUserModelId&gt;ContosoApp.Filler.3&lt;/AppUserModelId&gt;

           &lt;Description&gt;Fill out dynamic forms to gather and reuse information throughout the organization using Microsoft ContosoApp.&lt;/Description&gt;

           &lt;Hotkey&gt;0&lt;/Hotkey&gt;

           &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

           &lt;ApplicationId&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/ApplicationId&gt;

         &lt;/Shortcut&gt;

     &lt;/Extension&gt;

     &lt;Erweiterungskategorie = "AppV. Verknüpfung"&gt;

       &lt;Shortcut&gt;

         &lt;File&gt;\[{AppData}\]\\Microsoft\\Contoso\\Recent\\Templates.LNK&lt;/File&gt;

         &lt;Target&gt;\[{AppData}\]\\Microsoft\\Templates&lt;/Target&gt;

         &lt;Icon /&gt;

         &lt;Arguments /&gt;

         &lt;WorkingDirectory /&gt;

         &lt;AppUserModelId /&gt;

         &lt;Description /&gt;

         &lt;Hotkey&gt;0&lt;/Hotkey&gt;

         &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

         &lt;!-- Note the ApplicationId is optional --&gt;

       &lt;/Shortcut&gt;

     &lt;/Extension&gt;

    &lt;/Extensions&gt;

   &lt;/Shortcuts&gt;

   **Dateitypzuordnungen:** Ordnet Dateitypen mit Programmen zu, die standardmäßig geöffnet werden sollen, sowie das Kontextmenü einrichten. (MIME-Typen können auch mit diesem susbsystem eingerichtet werden). Beispiel für eine Dateitypzuordnung:

   &lt;FileTypeAssociations Enabled = "true"&gt;

   &lt;Extensions&gt;

     &lt;Erweiterungskategorie = "AppV. FileTypeAssociation"&gt;

       &lt;FileTypeAssociation&gt;

         &lt;FileExtension MimeAssociation="true"&gt;

         &lt;Name&gt;.docm&lt;/Name&gt;

         &lt;ProgId&gt;contosowordpad.DocumentMacroEnabled.12&lt;/ProgId&gt;

         &lt;PerceivedType&gt;document&lt;/PerceivedType&gt;

         &lt;ContentType&gt;application/vnd.ms-contosowordpad.document.macroEnabled.12&lt;/ContentType&gt;

         &lt;OpenWithList&gt;

           &lt;ApplicationName&gt;wincontosowordpad.exe&lt;/ApplicationName&gt;

         &lt;/OpenWithList&gt;

        &lt;OpenWithProgIds&gt;

           &lt;ProgId&gt;contosowordpad.8&lt;/ProgId&gt;

         &lt;/OpenWithProgIds&gt;

         &lt;ShellNew&gt;

           &lt;Command /&gt;

           &lt;DataBinary /&gt;

           &lt;DataText /&gt;

           &lt;FileName /&gt;

           &lt;NullFile&gt;true&lt;/NullFile&gt;

           &lt;ItemName /&gt;

           &lt;IconPath /&gt;

           &lt;MenuText /&gt;

           &lt;Handler /&gt;

         &lt;/ShellNew&gt;

       &lt;/FileExtension&gt;

       &lt;ProgId&gt;

          &lt;Name&gt;contosowordpad.DocumentMacroEnabled.12&lt;/Name&gt;

           &lt;DefaultIcon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\contosowordpadicon.exe,15&lt;/DefaultIcon&gt;

           &lt;Description&gt;Blah Blah Blah&lt;/Description&gt;

           &lt;FriendlyTypeName&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,9182&lt;/FriendlyTypeName&gt;

           &lt;InfoTip&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,1424&lt;/InfoTip&gt;

           &lt;EditFlags&gt;0&lt;/EditFlags&gt;

           &lt;ShellCommands&gt;

             &lt;DefaultCommand&gt;Open&lt;/DefaultCommand&gt;

             &lt;ShellCommand&gt;

                &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

                &lt;Name&gt;Edit&lt;/Name&gt;

                &lt;FriendlyName&gt;&Edit&lt;/FriendlyName&gt;

                &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /vu "%1"&lt;/CommandLine&gt;

             &lt;/ShellCommand&gt;

             &lt;/ShellCommand&gt;

               &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

               &lt;Name&gt;Open&lt;/Name&gt;

               &lt;FriendlyName&gt;&Open&lt;/FriendlyName&gt;

               &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /n "%1"&lt;/CommandLine&gt;

               &lt;DropTargetClassId /&gt;

               &lt;DdeExec&gt;

                 &lt;Application&gt;mscontosowordpad&lt;/Application&gt;

                 &lt;Topic&gt;ShellSystem&lt;/Topic&gt;

                 &lt;IfExec&gt;\[SHELLNOOP\]&lt;/IfExec&gt;

                 &lt;DdeCommand&gt;\[SetForeground\]\[ShellNewDatabase "%1"\]&lt;/DdeCommand&gt;

               &lt;/DdeExec&gt;

             &lt;/ShellCommand&gt;

           &lt;/ShellCommands&gt;

         &lt;/ProgId&gt;

        &lt;/FileTypeAssociation&gt;

      &lt;/Extension&gt;

     &lt;/Extensions&gt;

     &lt;/FileTypeAssociations&gt;

   **URL-Protokolle**: dies steuert die URL-Protokolle, die in die lokale Registrierung des Clientcomputers integriert sind, beispielsweise "mailto:".

   &lt;URLProtocols Enabled = "true"&gt;

   &lt;Extensions&gt;

   &lt;Erweiterungskategorie = "AppV. URLProtocol"&gt;

   &lt;URLProtocol&gt;

     &lt;Name &gt; mailto &lt; /Name&gt;

     &lt;ApplicationURLProtocol&gt;

     &lt;DefaultIcon &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE,-9403 &lt; /DefaultIcon&gt;

     &lt;EditFlags &gt; 2 &lt; /EditFlags&gt;

     &lt;Beschreibung&gt;

     &lt;AppUserModelId&gt;

     &lt;FriendlyTypeName /&gt;

     &lt;Infotipp&gt;

   &lt;SourceFilter&gt;

     &lt;ShellFolder /&gt;

     &lt;WebNavigableCLSID /&gt;

     &lt;ExplorerFlags &gt; 2 &lt; /ExplorerFlags&gt;

     &lt;CLSID&gt;

     &lt;ShellCommands&gt;

     &lt;DefaultCommand &gt; Open &lt; /DefaultCommand&gt;

     &lt;ShellCommand&gt;

     &lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationId&gt;

     &lt;Namen &gt; Öffnen &lt; /Name&gt;

     &lt;CommandLine &gt; \ [{ProgramFilesX86} \\Microsoft Contoso\\Contoso\\contosomail.EXE "-c OEP. Hinweis/m "%1" &lt; /CommandLine&gt;

     &lt;DropTargetClassId /&gt;

     &lt;FriendlyName&gt;

     &lt;Erweiterter &gt; 0- &lt; /Extended&gt;

     &lt;LegacyDisable &gt; 0 &lt; /LegacyDisable&gt;

     &lt;SuppressionPolicy &gt; 2 &lt; /SuppressionPolicy&gt;

      &lt;DdeExec&gt;

     &lt;NoActivateHandler /&gt;

     &lt;Application &gt; contosomail &lt; /Application&gt;

     &lt;Topic &gt; ShellSystem &lt; /Topic&gt;

     &lt;IfExec &gt; \ [SHELLNOOP \] &lt; /IfExec&gt;

     &lt;DdeCommand &gt; \ [SetForeground \] \ [ShellNewDatabase "%1" \] &lt; /DdeCommand&gt;

     &lt;/DdeExec&gt;

     &lt;/ShellCommand&gt;

     &lt;/ShellCommands&gt;

     &lt;/ApplicationURLProtocol&gt;

     &lt;/URLProtocol&gt;

     &lt;/Extension&gt;

     &lt;/Extension&gt;

     &lt;/URLProtocols&gt;

   **Software-Clients**: ermöglicht es der APP, sich als e-Mail-Client, Nachrichten Leser, Media Player zu registrieren und die app in der UI "Programm Zugriff und Computer Standards festlegen" sichtbar zu machen. In den meisten Fällen müssen Sie diese Funktion nur aktivieren und deaktivieren. Darüber hinaus gibt es ein Steuerelement zum Aktivieren und Deaktivieren des e-Mail-Clients, wenn die anderen Clients mit Ausnahme des Clients weiterhin aktiviert werden sollen.

   &lt;SoftwareClients Enabled = "true"&gt;

     &lt;ClientConfiguration EmailEnabled = "falsch"/&gt;

   &lt;/SoftwareClients&gt;

   AppPaths:-Wenn eine Anwendung, beispielsweise contoso.exe, mit einem AppPath-Namen von "MyApp" registriert ist, können Sie "MyApp" unter dem Menü "ausführen" eingeben, und es wird contoso.exe geöffnet.

   &lt;AppPaths Enabled = "true"&gt;

   &lt;Extensions&gt;

   &lt;Erweiterungskategorie = "AppV. AppPath"&gt;

   &lt;AppPath&gt;

     &lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationId&gt;

     &lt;Name &gt;contosomail.exe&lt; /Name&gt;

     &lt;ApplicationPath &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /applicationPath&gt;

     &lt;PATHEnvironmentVariablePrefix /&gt;

     &lt;CanAcceptUrl &gt; false &lt; /CanAcceptUrl&gt;

     &lt;SaveUrl&gt;

   &lt;/AppPath&gt;

   &lt;/Extension&gt;

   &lt;/Extensions&gt;

   &lt;/AppPaths&gt;

   **Com**: ermöglicht einer Anwendung das Registrieren lokaler COM-Server. Der Modus kann integriert, isoliert oder deaktiviert sein. Wenn isol.

   &lt;COM-Modus = "isoliert"/&gt;

   **Weitere Einstellungen**:

   Neben Erweiterungen können auch andere Subsysteme aktiviert/deaktiviert und bearbeitet werden:

   **Virtuelle Kernel Objekte**:

   &lt;Objekte aktiviert = "falsch"/&gt;

   **Virtuelle Registrierung**: wird verwendet, wenn Sie eine Registrierung in der virtuellen Registrierung in HKCU einrichten möchten.

   &lt;Registry Enabled = "true"&gt;

   &lt;Enthalten&gt;

   &lt;Key Path = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\ABC"&gt;

   &lt;Value Type = "reg \ _SZ" Name = "Bar" Data = "Neuwert"/&gt;

    &lt;/Key&gt;

     &lt;Key Path = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\EmptyKey"/&gt;

    &lt;/Include&gt;

   &lt;Löschen&gt;

     &lt;/Registry&gt;

   **Virtuelles Datei System**

         &lt;FileSystem Enabled="true" /&gt;

   **Virtuelle Schriftarten**

         &lt;Fonts Enabled="false" /&gt;

   **Virtuelle Umgebungsvariablen**

   &lt;EnvironmentVariables Enabled = "true"&gt;

   &lt;Enthalten&gt;

          &lt;Variable Name="UserPath" Value="%path%;%UserProfile%" /&gt;

          &lt;Variable Name="UserLib" Value="%UserProfile%\\ABC" /&gt;

          &lt;/Include&gt;

         &lt;Delete&gt;

          &lt;Variable Name="lib" /&gt;

           &lt;/Delete&gt;

           &lt;/EnvironmentVariables&gt;

   **Virtuelle Dienste**

         &lt;Services Enabled="false" /&gt;

3. **Userscripts** – Skripts können verwendet werden, um die virtuelle Umgebung einzurichten oder zu ändern sowie Skripts zum Zeitpunkt der Bereitstellung oder Entfernung auszuführen, bevor eine Anwendung ausgeführt wird, oder Sie können verwendet werden, um die Umgebung zu "bereinigen", nachdem die Anwendung beendet wurde. Verweisen Sie auf eine Beispielkonfigurationsdatei, die vom Sequencer ausgegeben wird, um ein Beispielskript anzuzeigen. Im Abschnitt "Skripts" unten finden Sie weitere Informationen zu den verschiedenen Triggern, die verwendet werden können.

4. **ManagingAuthority** – kann verwendet werden, wenn zwei Versionen Ihres Pakets auf demselben Computer nebeneinander vorhanden sind, eine für App-v 4,6 und die andere auf App-v 5,0 bereitgestellt. Damit App-v vNext erhielten App-v 4,6-Erweiterungspunkte für das benannte Paket übernehmen kann, geben Sie Folgendes in die userconfig-Datei ein (wobei Paketname die Paket-GUID in App-v 4,6 ist:

   &lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PACKAGENAME = "032630c0-b8e2-417c-acef-76fc5297fe81"/&gt;

### Konfigurationsdatei für dynamische Bereitstellung

**Kopfzeile** : die Kopfzeile einer Konfigurationsdatei für die Bereitstellung lautet wie folgt:

&lt;? XML Version = "1.0" Encoding = "UTF-8"? &gt; &lt; DeploymentConfiguration **Packaged**= "1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reserviert" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;

Die **Paket** -Nr ist derselbe Wert wie in der Manifestdatei vorhanden.

**Body** – der Text der Bereitstellungs Konfigurationsdatei umfasst zwei Abschnitte:

-   Abschnitt "Benutzerkonfiguration" – ermöglicht denselben Inhalt wie die im vorherigen Abschnitt beschriebene Benutzerkonfigurationsdatei. Wenn das Paket für einen Benutzer veröffentlicht wird, überschreiben alle appextensions-Konfigurationseinstellungen in diesem Abschnitt entsprechende Einstellungen im Manifest innerhalb des Pakets, es sei denn, es wird auch eine Benutzerkonfigurationsdatei bereitgestellt. Wenn auch eine userconfig-Datei bereitgestellt wird, wird Sie anstelle der Benutzereinstellungen in der Konfigurationsdatei für die Bereitstellung verwendet. Wenn das Paket Global veröffentlicht wird, wird nur der Inhalt der Bereitstellungs Konfigurationsdatei in Verbindung mit dem Manifest verwendet.

-   Abschnitt "Computerkonfiguration" – enthält Informationen, die nur für einen ganzen Computer konfiguriert werden können, und nicht für einen bestimmten Benutzer auf dem Computer. Beispiel: HKEY \ _LOCAL \ _MACHINE Registrierungsschlüssel in VFS.

&lt;DeploymentConfiguration **Packaged**= "1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reserviert" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;

&lt;UserConfiguration&gt;

  ..

&lt;/UserConfiguration&gt;

&lt;MachineConfiguration&gt;

..

&lt;/MachineConfiguration&gt;

..

&lt;/MachineConfiguration&gt;

&lt;/DeploymentConfiguration&gt;

**Benutzerkonfiguration** – verwenden Sie den vorherigen Abschnitt der **dynamischen Benutzerkonfigurationsdatei** , um Informationen zu den Einstellungen anzuzeigen, die im Abschnitt Benutzerkonfiguration der Bereitstellungs Konfigurationsdatei bereitgestellt werden.

Computerkonfiguration – der Abschnitt "Computerkonfiguration" der Bereitstellungs Konfigurationsdatei dient zum Konfigurieren von Informationen, die nur für einen ganzen Computer festgesetzt werden können, und nicht für einen bestimmten Benutzer auf dem Computer. Beispiel: HKEY \ _LOCAL \ _MACHINE Registrierungsschlüssel in der virtuellen Registrierung. Unter diesem Element sind vier Unterabschnitte zulässig.

1.  **Subsysteme** -AppExtensions und andere Subsysteme sind als untergeordnete Knoten unter &lt; Subsysteme angeordnet &gt; :

    &lt;MachineConfiguration&gt;

      &lt;Subsysteme&gt;

      ..

      &lt;/Subsystems&gt;

    ..

    &lt;/MachineConfiguration&gt;

    Im folgenden Abschnitt werden die verschiedenen Subsysteme und Verwendungsbeispiele angezeigt.

    **Erweiterungen**:

    Einige Subsysteme (Erweiterungs Subsysteme) Steuern Erweiterungen, die nur für alle Benutzer gelten können. Das Subsystem ist Anwendungsfunktionen. Da dies nur für alle Benutzer gelten kann, muss das Paket Global veröffentlicht werden, damit diese Art von Erweiterung in das lokale System integriert werden kann. Die gleichen Regeln für Steuerelemente und Einstellungen, die für die Erweiterungen in der Benutzerkonfiguration gelten, gelten auch für die im Abschnitt MachineConfiguration.

    **Anwendungsfunktionen**: wird von Standardprogrammen in der Windows-Betriebssystem Schnittstelle verwendet. Ermöglicht es einer Anwendung, sich selbst so zu registrieren, dass Sie bestimmte Dateierweiterungen öffnen kann, als Anwärter für den Internet Browser Steckplatz des Startmenüs, um bestimmte Windows-MIME-Typen öffnen zu können.Diese Erweiterung macht auch die virtuelle Anwendung in der Benutzeroberfläche für Standard Programme festlegen sichtbar:

    &lt;ApplicationCapabilities Enabled = "true"&gt;

      &lt;Extensions&gt;

       &lt;Erweiterungskategorie = "AppV. ApplicationCapabilities"&gt;

        &lt;ApplicationCapabilities&gt;

         &lt;ApplicationId&gt;\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe&lt;/ApplicationId&gt;

         &lt;Reference&gt;

          &lt;Name&gt;LitView Browser&lt;/Name&gt;

          &lt;Path&gt;SOFTWARE\\LitView\\Browser\\Capabilities&lt;/Path&gt;

         &lt;/Reference&gt;

       &lt;Capabilitygroup&gt;

        &lt;Capabilities&gt;

         &lt;Name&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12345&lt;/Name&gt;

         &lt;Description&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12346&lt;/Description&gt;

         &lt;Hidden&gt;0&lt;/Hidden&gt;

         &lt;EMailSoftwareClient&gt;Lit View E-Mail Client&lt;/EMailSoftwareClient&gt;

         &lt;FileAssociationList&gt;

          &lt;FileAssociation Extension=".htm" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".html" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".shtml" ProgID="LitViewHTML" /&gt;

         &lt;/FileAssociationList&gt;

         &lt;MIMEAssociationList&gt;

          &lt;MIMEAssociation Type="audio/mp3" ProgID="LitViewHTML" /&gt;

          &lt;MIMEAssociation Type="audio/mpeg" ProgID="LitViewHTML" /&gt;

         &lt;/MIMEAssociationList&gt;

        &lt;URLAssociationList&gt;

          &lt;URLAssociation Scheme="http" ProgID="LitViewHTML.URL.http" /&gt;

         &lt;/URLAssociationList&gt;

         &lt;/Capabilities&gt;

      &lt;/CapabilityGroup&gt;

       &lt;/ApplicationCapabilities&gt;

      &lt;/Extension&gt;

    &lt;/Extensions&gt;

    &lt;/ApplicationCapabilities&gt;

    **Weitere Einstellungen**:

    Neben Erweiterungen können auch andere Subsysteme bearbeitet werden:

    **Machine Wide Virtual Registry**: wird verwendet, wenn Sie einen Registrierungsschlüssel in der virtuellen Registrierung in HKEY \ _Local \ _Machine

    &lt;Registrierung&gt;

    &lt;Enthalten&gt;

      &lt;Key Path = "\\REGISTRY\\Machine\\Software\\ABC"&gt;

        &lt;Value Type="REG\_SZ" Name="Bar" Data="Baz" /&gt;

       &lt;/Key&gt;

      &lt;Key Path = "\\REGISTRY\\Machine\\Software\\EmptyKey"/&gt;

     &lt;/Include&gt;

    &lt;Löschen&gt;

    &lt;/Registry&gt;

    **Computerweite virtuelle Kernel Objekte**

    &lt;Objekte&gt;

    &lt;NotIsolate&gt;

       &lt;Objekt Name = "testObject"/&gt;

     &lt;/NotIsolate&gt;

    &lt;/Objects&gt;

2.  **ProductSourceURLOptOut**: gibt an, ob die URL für das Paket global über PackageSourceRoot (zur Unterstützung von Zweigstellenszenarien) geändert werden kann. Standard ist falsch, und die Einstellungsänderung wird beim nächsten Start wirksam.  

    &lt;MachineConfiguration&gt;

      .. 

      &lt;ProductSourceURLOptOut Enabled = "true"/&gt;

      ..

    &lt;/MachineConfiguration&gt;

3.  **MachineScripts** – Paket kann so konfiguriert werden, dass Skripts zum Zeitpunkt der Bereitstellung, Veröffentlichung oder Entfernung ausgeführt werden. Verweisen Sie auf eine Beispiel Bereitstellungs Konfigurationsdatei, die vom Sequencer generiert wird, um ein Beispielskript anzuzeigen. Im Abschnitt "Skripte" unten finden Sie weitere Informationen zu den verschiedenen Triggern, die verwendet werden können.

4.  **TerminateChildProcess**: – Es kann eine ausführbare Datei der Anwendung angegeben werden, deren untergeordnete Prozesse beendet werden, wenn der Prozess der Anwendungs-exe beendet wird.

    &lt;MachineConfiguration&gt;

      ..   

      &lt;TerminateChildProcesses&gt;

        &lt;Application Path="\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE" /&gt;

        &lt;Application Path="\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe" /&gt;

        &lt;Application Path="\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE" /&gt;

      &lt;/TerminateChildProcesses&gt;

      ..

    &lt;/MachineConfiguration&gt;

### Skripts

In der folgenden Tabelle werden die verschiedenen Skriptereignisse und der Kontext beschrieben, unter dem Sie ausgeführt werden können.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Skript Ausführungszeit</th>
<th align="left">Kann in der Bereitstellungskonfiguration angegeben werden</th>
<th align="left">Kann in der Benutzerkonfiguration angegeben werden</th>
<th align="left">Kann in der virtuellen Umgebung des Pakets ausgeführt werden</th>
<th align="left">Kann im Kontext einer bestimmten Anwendung ausgeführt werden</th>
<th align="left">Wird im System/Benutzerkontext ausgeführt: (Bereitstellungskonfiguration, Benutzerkonfiguration)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AddPackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(System, N/A)</p></td>
</tr>
<tr class="even">
<td align="left"><p>PublishPackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(System, Benutzer)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UnpublishPackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(System, Benutzer)</p></td>
</tr>
<tr class="even">
<td align="left"><p>RemovePackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(System, N/A)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>StartProcess</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>(Benutzer, Benutzer)</p></td>
</tr>
<tr class="even">
<td align="left"><p>ExitProcess</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>(Benutzer, Benutzer)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>StartVirtualEnvironment</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p>(Benutzer, Benutzer)</p></td>
</tr>
<tr class="even">
<td align="left"><p>TerminateVirtualEnvironment</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(Benutzer, Benutzer)</p></td>
</tr>
</tbody>
</table>

 

### Erstellen einer dynamischen Konfigurationsdatei mit einer App-V 5,0-Manifestdatei

Sie können die dynamische Konfigurationsdatei mit einer von drei Methoden erstellen: entweder manuell, mithilfe der App-V 5,0-Verwaltungskonsole oder durch Sequenzierung eines Pakets, das mit zwei Beispieldateien generiert wird.

Weitere Informationen zum Erstellen der Datei mithilfe der APP-v 5,0-Verwaltungskonsole finden Sie unter [Erstellen einer benutzerdefinierten Konfigurationsdatei mithilfe der APP-v 5,0-Verwaltungskonsole](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md).

Wenn Sie die Datei manuell erstellen möchten, können die obigen Informationen in den vorherigen Abschnitten in einer einzelnen Datei kombiniert werden. Wir empfehlen die Verwendung von Dateien, die vom Sequencer generiert wurden.






## Verwandte Themen


[Sie wenden Sie die Bereitstellungskonfigurationsdatei mithilfe von PowerShell an](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)

[So wenden Sie die Benutzerkonfigurationsdatei mithilfe von PowerShell an](how-to-apply-the-user-configuration-file-by-using-powershell.md)

[Vorgänge für App-V 5.0](operations-for-app-v-50.md)

 

 





