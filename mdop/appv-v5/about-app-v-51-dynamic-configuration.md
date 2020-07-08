---
title: Informationen zur dynamischen Konfiguration von App-V 5,1
description: Sie können die dynamische Konfiguration verwenden, um ein App-V 5,1-Paket für einen Benutzer anzupassen. Verwenden Sie die folgenden Informationen, um eine vorhandene dynamische Konfigurationsdatei zu erstellen oder zu bearbeiten.
author: dansimp
ms.assetid: 35bc9908-d502-4a9c-873f-8ee17b6d9d74
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/28/2018
ms.author: dansimp
ms.openlocfilehash: ec8a25da6e139ac329810b1e04f7097cadaa6ab4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806116"
---
# Informationen zur dynamischen Konfiguration von App-V 5,1 
Mit der dynamischen Konfiguration können Sie die dynamische Konfigurationsdatei bearbeiten, um die Ausführung eines App-V 5,1-Pakets für einen Benutzer oder eine Gruppe anzupassen. Die Paket Anpassung entfernt die Notwendigkeit, Pakete mithilfe der gewünschten Einstellungen erneut zu sequenzieren.  Darüber hinaus bietet es eine Möglichkeit, Paketinhalte und benutzerdefinierte Einstellungen unabhängig zu halten.

Virtuelle Anwendungspakete enthalten ein Manifest, das alle Kerninformationen für das Paket enthält. Diese Informationen enthalten die Standardeinstellungen für die Paketeinstellungen und bestimmen die Einstellungen in der grundlegendsten Form (ohne zusätzliche Anpassung). 

Wenn ein Paket erstellt wird, generiert der Sequencer automatisch Standard Bereitstellungs-und Benutzer Konfigurations-XML-Dateien mit den Daten des paketmanifests. Daher spiegeln diese generierten Dateien die Standardeinstellungen wider, die während der Sequenzierung konfiguriert sind. Wenn Sie diese Dateien auf ein Paket in dem vom Sequencer generierten Formular anwenden, weisen die Pakete die gleichen Standardeinstellungen auf, die aus ihrem Manifest stammen. 

Verwenden Sie diese generierten Dateien, um bei Bedarf Änderungen vorzunehmen, die sich nicht direkt auf das Paket auswirken. Wenn Sie die Konfigurationsdateien hinzufügen, löschen oder aktualisieren möchten, nehmen Sie Ihre Änderungen an den Standardwerten in den Manifestinformationen vor.

>[!TIP]
>Die Reihenfolge, in der die Dateien gelesen werden, lautet:<ul><li>UserConfig.xml</li><li>DeploymentConfig.xml</li><li>Manifest</li></ul><p>Der erste Eintrag steht für das, was zuletzt gelesen wird. Daher hat der Inhalt Vorrang, und alle Pakete enthalten Standardeinstellungen aus dem Paketmanifest.<ol><li> Wenn Sie die DeploymentConfig.xml Datei anpassen und die angepassten Einstellungen anwenden, werden die Standardeinstellungen im Paketmanifest überschrieben. </li><li> Wenn Sie die UserConfig.xml anpassen und die angepassten Einstellungen anwenden, werden die Standardeinstellungen für die Bereitstellungskonfiguration und das Paketmanifest überschrieben. </li></ol>

## Inhalt der Benutzer Konfigurationsdatei (UserConfig.xml)
Die userconfig-Datei enthält Konfigurationseinstellungen, die für einen bestimmten Benutzer angewendet werden, wenn das Paket auf einem Computer mit dem App-V 5,1-Client bereitgestellt wird.  Diese Einstellungen wirken sich nicht auf andere Benutzer auf dem Client aus.

Verwenden Sie die userconfig-Datei, um benutzerdefinierte Einstellungen für ein Paket anzugeben oder zu ändern:

-   In das System System integrierte Erweiterungen pro Benutzer: Verknüpfungen, Dateitypzuordnungen, URL-Protokolle, AppPaths, Software-Clients und com
-   Virtuelle Subsysteme: Anwendungsobjekte, Umgebungsvariablen, Registrierungsänderungen, Dienste und Schriftarten
-   Skripts (nur Benutzerkontext)
-   Verwaltungsautorität (zum Steuern der Koexistenz von Paketen mit App-V 4,6)

### Kopfzeile

Die Kopfzeile einer Dynamic User-Konfigurationsdatei sieht wie folgt aus:

```xml
<?xml version="1.0" encoding="utf-8"?><UserConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/userconfiguration">
```

Die **Paket** -Nr ist derselbe Wert wie in der Manifestdatei vorhanden.


### Textkörper

Der Text der Dynamic User-Konfigurationsdatei kann alle in der Manifestdatei definierten App-Erweiterungspunkte sowie Informationen zum Konfigurieren virtueller Anwendungen umfassen. Im Textbereich sind vier Unterabschnitte zulässig:

1.  **[Anwendungen](#applications)** 
2.  **[Subsysteme](#subsystems)**
3.  **[UserScripts](#userscripts)**
4.  **[ManagingAuthority](#managingauthority)**

#### Anwendungen

Für alle App-Erweiterungen, die in der Manifestdatei in einem Paket enthalten sind, ist eine Anwendungs-ID zugewiesen, die Sie in der Manifestdatei finden. Mit der Anwendungs-ID können Sie alle Erweiterungen für eine bestimmte Anwendung innerhalb eines Pakets aktivieren oder deaktivieren. Die Anwendungs-ID muss in der Manifestdatei vorhanden sein, oder Sie wird ignoriert.

```XML
<UserConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved"  xmlns="http://schemas.microsoft.com/appv/2010/userconfiguration">

<Applications>

<!--No new application can be defined in policy. AppV Client will ignore any application ID that is not also in the Manifest file-->

<Application Id="{a56fa627-c35f-4a01-9e79-7d36aed8225a}" Enabled="false">

</Application>

</Applications>

..

</UserConfiguration>
```

#### Subsysteme

AppExtensions und andere Subsysteme, die als untergeordnete Knoten angeordnet sind.

```XML
<UserConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/userconfiguration">

<Subsystems>

..

</Subsystems>

..

</UserConfiguration>
```

Sie können jedes Subsystem mithilfe des **Enabled** -Attributs aktivieren oder deaktivieren.

**Extensions** 

Einige Subsysteme (Erweiterungs Subsysteme)-Steuerelement Erweiterungen. Diese Subsysteme sind Tastenkombinationen, Dateitypzuordnungen, URL-Protokolle, AppPaths, Software Clients und com.

Erweiterungs Subsysteme können unabhängig vom Inhalt aktiviert und deaktiviert werden. Wenn Sie beispielsweise Tastenkombinationen aktivieren, verwendet der Clientstandard mäßig die Verknüpfungen, die im Manifest enthalten sind. Jedes Erweiterungs Subsystem kann einen Knoten enthalten \<Extensions\> . Wenn dieses untergeordnete Element vorhanden ist, ignoriert der Client den Inhalt in der Manifestdatei für dieses Subsystem und verwendet nur den Inhalt in der Konfigurationsdatei. 

_**Beispiele:**_ 

- Wenn Sie dies in der Benutzer-oder Bereitstellungs Konfigurationsdatei definieren, wird der Inhalt des Manifests ignoriert.

  ```XML

  <Shortcuts  Enabled="true"\>

  <Extensions>

  ...

  </Extensions>

  </Shortcuts>
  ```
- Wenn Sie nur Folgendes definieren, wird der Inhalt des Manifests während der Veröffentlichung integriert.

  ```XML

  <Shortcuts  Enabled="true"/>
  ```

- Wenn Sie Folgendes definieren, werden alle Verknüpfungen im Manifest weiterhin ignoriert. Anders ausgedrückt: keine Tastenkombinationen werden integriert.

  ```XML

  <Shortcuts  Enabled="true">

     <Extensions/>

  </Shortcuts>
  ```

_**Unterstützte Erweiterungs Subsysteme:**_ 

Das Erweiterungs Subsystem für **Verknüpfungen** steuert, welche Tastenkombinationen in das lokale System integriert werden.  

```XML

<Subsystems>

<Shortcuts Enabled="true">

  <Extensions>

    <Extension Category="AppV.Shortcut">

      <Shortcut>

        <File>[{Common Programs}]\Microsoft Contoso\Microsoft ContosoApp Filler 2010.lnk</File>

        <Target>[{PackageRoot}]\Contoso\ContosoApp.EXE</Target>


      <Icon>[{Windows}]\Installer\{90140000-0011-0000-0000-0000000FF1CE}\inficon.exe</Icon>

        <Arguments />

        <WorkingDirectory />

        <AppUserModelId>ContosoApp.Filler.3</AppUserModelId>

        <Description>Fill out dynamic forms to gather and reuse information throughout the organization using Microsoft ContosoApp.</Description>

        <Hotkey>0</Hotkey>

        <ShowCommand>1</ShowCommand>

      <ApplicationId>[{PackageRoot}]\Contoso\ContosoApp.EXE</ApplicationId>

      </Shortcut>

  </Extension>

  <Extension Category="AppV.Shortcut">

    <Shortcut>

    <File>[{AppData}]\Microsoft\Contoso\Recent\Templates.LNK</File>

      <Target>[{AppData}]\Microsoft\Templates</Target>

      <Icon />

      <Arguments />

      <WorkingDirectory />

      <AppUserModelId />

      <Description />

      <Hotkey>0</Hotkey>

      <ShowCommand>1</ShowCommand>

      <!-- Note the ApplicationId is optional -->

    </Shortcut>

  </Extension>

 </Extensions>

</Shortcuts>
```

**File-Type Associates** Extension Subsystem ordnet Dateitypen zu, die Programme standardmäßig öffnen und das Kontextmenü einrichten. 

>[!TIP]
>Sie können das Subsystem mit MIME-Typen einrichten.

```XML

<FileTypeAssociations Enabled="true">

<Extensions>

  <Extension Category="AppV.FileTypeAssociation">

    <FileTypeAssociation>

      <FileExtension MimeAssociation="true">

      <Name>.docm</Name>

      <ProgId>contosowordpad.DocumentMacroEnabled.12</ProgId>

      <PerceivedType>document</PerceivedType>

    <ContentType>application/vnd.ms-contosowordpad.document.macroEnabled.12</ContentType>

      <OpenWithList>

        <ApplicationName>wincontosowordpad.exe</ApplicationName>

      </OpenWithList>

     <OpenWithProgIds>

        <ProgId>contosowordpad.8</ProgId>

      </OpenWithProgIds>

      <ShellNew>

        <Command />

        <DataBinary />

        <DataText />

        <FileName />

        <NullFile>true</NullFile>

        <ItemName />

        <IconPath />

        <MenuText />

        <Handler />

      </ShellNew>

    </FileExtension>

    <ProgId>

       <Name>contosowordpad.DocumentMacroEnabled.12</Name>

      <DefaultIcon\>[{Windows}]\Installer\{90140000-0011-0000-0000-000000FF1CE}\contosowordpadicon.exe,15</DefaultIcon>

        <Description>Blah Blah Blah</Description>

        <FriendlyTypeName>[{FOLDERID_ProgramFilesX86}]\Microsoft Contoso 14\res.dll,9182</FriendlyTypeName>

        <InfoTip>[{FOLDERID_ProgramFilesX86}]\Microsoft Contoso 14\res.dll,1424</InfoTip>

        <EditFlags>0</EditFlags>

        <ShellCommands>

          <DefaultCommand>Open</DefaultCommand>

          <ShellCommand>

           <ApplicationId>{e56fa627-c35f-4a01-9e79-7d36aed8225a}</ApplicationId>

             <Name>Edit</Name>

             <FriendlyName>&Edit</FriendlyName>

           <CommandLine>"[{PackageRoot}]\Contoso\WINcontosowordpad.EXE" /vu "%1"</CommandLine>

          </ShellCommand>

          </ShellCommand>

          <ApplicationId>{e56fa627-c35f-4a01-9e79-7d36aed8225a}</ApplicationId>

            <Name>Open</Name>

            <FriendlyName>&Open</FriendlyName>

            <CommandLine>"[{PackageRoot}]\Contoso\WINcontosowordpad.EXE" /n "%1"</CommandLine>

            <DropTargetClassId />

            <DdeExec>

              <Application>mscontosowordpad</Application>

              <Topic>ShellSystem</Topic>

              <IfExec>[SHELLNOOP]</IfExec>

              <DdeCommand>[SetForeground][ShellNewDatabase"%1"]</DdeCommand>

            </DdeExec>

          </ShellCommand>

        </ShellCommands>

      </ProgId>

     </FileTypeAssociation>

   </Extension>

  </Extensions>

  </FileTypeAssociations>
```

Das Subsystem für **URL-Protokoll** Erweiterungen steuert die URL-Protokolle, die in die lokale Registrierung des Clientcomputers integriert sind, beispielsweise _mailto:_. 

```XML

<URLProtocols Enabled="true">

<Extensions>

<Extension Category="AppV.URLProtocol">

<URLProtocol>

  <Name>mailto</Name>

  <ApplicationURLProtocol>

  <DefaultIcon>[{ProgramFilesX86}]\MicrosoftContoso\Contoso\contosomail.EXE,-9403</DefaultIcon>

  <EditFlags>2</EditFlags>

  <Description />

  <AppUserModelId />

  <FriendlyTypeName />

  <InfoTip />

<SourceFilter />

  <ShellFolder />

  <WebNavigableCLSID />

  <ExplorerFlags>2</ExplorerFlags>

  <CLSID />

  <ShellCommands>

  <DefaultCommand>open</DefaultCommand>

  <ShellCommand>

  <ApplicationId>[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE</ApplicationId>

  <Name>open</Name>

  <CommandLine>[{ProgramFilesX86}\Microsoft Contoso\Contoso\contosomail.EXE" -c OEP.Note /m "%1"</CommandLine>

  <DropTargetClassId />

  <FriendlyName />

  <Extended>0</Extended>

  <LegacyDisable>0</LegacyDisable>

  <SuppressionPolicy>2</SuppressionPolicy>

   <DdeExec>

  <NoActivateHandler />

  <Application>contosomail</Application>

  <Topic>ShellSystem</Topic>

  <IfExec>[SHELLNOOP]</IfExec>

  <DdeCommand>[SetForeground][ShellNewDatabase "%1"]</DdeCommand>

  </DdeExec>

  </ShellCommand>

  </ShellCommands>

  </ApplicationURLProtocol>

  </URLProtocol>

  </Extension>

  </Extension>

  </URLProtocols>
```

Das Subsystem für **Software-Clients** -Erweiterungen ermöglicht es der APP, sich als e-Mail-Client, Nachrichten Leser, Media Player zu registrieren und die app in der UI "Programm Zugriff und Computer Standardeinstellungen" sichtbar zu machen. In den meisten Fällen müssen Sie Sie nur aktivieren und deaktivieren. Darüber hinaus gibt es ein Steuerelement zum Aktivieren und Deaktivieren des e-Mail-Clients, wenn die anderen Clients mit Ausnahme des Clients weiterhin aktiviert werden sollen.

```XML

<SoftwareClients Enabled="true">

  <ClientConfiguration EmailEnabled="false" />

</SoftwareClients>
```

Das **AppPaths** -Erweiterungs Subsystem öffnet apps, die mit einem Anwendungspfad registriert sind. Wenn contoso.exe beispielsweise über einen AppPath-Namen von _myapp_verfügt, können Benutzer _myapp_ aus dem Menü "ausführen" eingeben, indem Sie contoso.exe öffnen.

```XML

<AppPaths Enabled="true">

<Extensions>

<Extension Category="AppV.AppPath">

<AppPath>

  <ApplicationId>[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE</ApplicationId>

  <Name>contosomail.exe</Name>

  <ApplicationPath>[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE</ApplicationPath>

  <PATHEnvironmentVariablePrefix />

  <CanAcceptUrl>false</CanAcceptUrl>

  <SaveUrl />

</AppPath>

</Extension>

</Extensions>

</AppPaths>
```

Das **com** -Erweiterungs Subsystem ermöglicht eine Anwendung, die auf lokalen com-Servern registriert ist. Der Modus kann wie folgt lauten:

-   Integration
-   Isolierten 
-   Deaktiviert

```XML

<COM Mode="Isolated"/>
```

**Virtuelle Kernel Objekte**

```XML

<Objects Enabled="false" />
```

Mit der **virtuellen Registrierung** wird eine Registrierung in der virtuellen Registrierung in HKCU festgelegt.

```XML

<Registry Enabled="true">

<Include>

<Key Path="\REGISTRY\USER\[{AppVCurrentUserSID}]\Software\ABC">

<Value Type="REG_SZ" Name="Bar" Data="NewValue" />

 </Key>

  <Key Path="\REGISTRY\USER\[{AppVCurrentUserSID}]\Software\EmptyKey" />

 </Include>

<Delete>

</Registry>
```

**Virtuelles Datei System**

```XML

    <FileSystem Enabled="true" />
```

**Virtuelle Schriftarten**

```XML

      <Fonts Enabled="false" />
```

**Virtuelle Umgebungsvariablen**

```XML

<EnvironmentVariables Enabled="true">

<Include>

       <Variable Name="UserPath" Value="%path%;%UserProfile%" />

       <Variable Name="UserLib" Value="%UserProfile%\ABC" />

       </Include>

      <Delete>

       <Variable Name="lib" />

        </Delete>

        </EnvironmentVariables>
```

**Virtuelle Dienste**

```XML

      <Services Enabled="false" />
```

#### UserScripts

Verwenden Sie userscripts, um die virtuelle Umgebung einzurichten oder zu ändern.  Sie können Skripts auch zum Zeitpunkt der Bereitstellung ausführen oder die Umgebung bereinigen, nachdem die Anwendung beendet wurde. Ein Beispielskript finden Sie in der vom Sequencer generierten Benutzerkonfigurationsdatei. Im Abschnitt "Skripts" unten finden Sie weitere Informationen zu den verschiedenen Triggern, die verwendet werden können.

#### ManagingAuthority

Verwenden Sie ManagingAuthority, wenn zwei Versionen Ihres Pakets auf dem gleichen Computer koexistieren, einer für App-v 4,6 und ein anderer auf App-v 5,0 bereitgestellt. Damit App-v vNext erhielten App-v 4,6-Erweiterungspunkte für das benannte Paket übernehmen kann, geben Sie Folgendes in die userconfig-Datei ein (wobei Paketname die Paket-GUID in App-v 4,6 ist:

```XML

<ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName="032630c0-b8e2-417c-acef-76fc5297fe81" />
```

## Konfigurationsdatei für die Bereitstellung (DeploymentConfig.xml)

Die DeploymentConfig-Datei enthält die Konfigurationseinstellungen für den Computerkontext und den Benutzerkontext und bietet dieselben Funktionen, die in der userconfig-Datei aufgeführt sind. Die Einstellungen werden angewendet, wenn das Paket auf einem Computer mit dem App-V 5,1-Client bereitgestellt wird.

Verwenden Sie die DeploymentConfig-Datei, um benutzerdefinierte Einstellungen für ein Paket anzugeben oder zu ändern:

- Alle userconfig-Einstellungen
- Erweiterungen, die nur global für alle Benutzer angewendet werden können
- Virtuelle Subsysteme für globale Computerspeicher Orte, beispielsweise Registrierung
- Produkt Quell-URL
- Skripts (nur Computerkontext)
- Steuerelemente zum kündigen von untergeordneten Prozessen

### Kopfzeile

Die Kopfzeile einer Dynamic Deployment-Konfigurationsdatei sieht wie folgt aus:

```XML
<?xml version="1.0" encoding="utf-8"?><DeploymentConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/deploymentconfiguration">
```

Die **Paket** -Nr ist derselbe Wert wie in der Manifestdatei vorhanden.

### Textkörper

Der Text der Dynamic Deployment-Konfigurationsdatei umfasst zwei Abschnitte:

- **UserConfiguration:** ermöglicht denselben Inhalt wie die im vorherigen Abschnitt beschriebene Benutzerkonfigurationsdatei.  Wenn Sie das Paket für einen Benutzer veröffentlichen, überschreiben alle appextensions-Konfigurationseinstellungen in diesem Abschnitt die entsprechenden Einstellungen im Manifest innerhalb des Pakets, es sei denn, Sie geben eine Benutzerkonfigurationsdatei an. Wenn auch eine userconfig-Datei bereitgestellt wird, wird Sie anstelle der Benutzereinstellungen in der Konfigurationsdatei für die Bereitstellung verwendet. Wenn Sie das Paket Global veröffentlichen, wird nur der Inhalt der Bereitstellungs Konfigurationsdatei in Verbindung mit dem Manifest verwendet. Weitere Informationen finden Sie unter [Inhalt der Benutzer Konfigurationsdatei (UserConfig.xml)](#user-configuration-file-contents-userconfigxml).

- **MachineConfiguration:** enthält Informationen, die nur für einen ganzen Computer konfiguriert werden können, nicht für einen bestimmten Benutzer auf dem Computer. HKEY_LOCAL_MACHINE Sie beispielsweise die Registrierungsschlüssel in VFS.

```XML

<DeploymentConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/deploymentconfiguration">

<UserConfiguration>

...

</UserConfiguration>

<MachineConfiguration>

...

</MachineConfiguration>

...

</MachineConfiguration>

</DeploymentConfiguration>
```

### UserConfiguration

Informationen zu den für diesen Abschnitt bereitgestellten Einstellungen finden Sie unter [Inhalt der Benutzer Konfigurationsdatei (UserConfig.xml)](#user-configuration-file-contents-userconfigxml) . 

### MachineConfiguration

Verwenden Sie den Abschnitt MachineConfiguration, um Informationen für einen ganzen Computer zu konfigurieren. nicht für einen bestimmten Benutzer auf dem Computer. HKEY_LOCAL_MACHINE Sie beispielsweise Registrierungsschlüssel in der virtuellen Registrierung. Unter diesem Element sind vier Unterabschnitte zulässig:

1.  **[Subsysteme](#subsystems-1)**
2.  **[ProductSourceURLOptOut](#productsourceurloptout)**
3.  **[MachineScripts](#machinescripts)**
4.  **[TerminateChildProcess](#terminatechildprocess)**

#### Subsysteme

AppExtensions und andere Subsysteme, die als untergeordnete Knoten angeordnet sind.

```XML

<MachineConfiguration>

  <Subsystems>

  …

  </Subsystems>

…

</MachineConfiguration>
```

Sie können jedes Subsystem mithilfe des **Enabled** -Attributs aktivieren oder deaktivieren.

**Extensions** 

Einige Subsysteme (Erweiterungs Subsysteme)-Steuerelement Erweiterungen. Das Subsystem ist Anwendungsfunktionen, die von Standardprogrammen verwendet werden. Für diese Art von Erweiterung muss das Paket global für die Integration in das lokale System veröffentlicht werden. Die gleichen Regeln für Steuerelemente und Einstellungen, die für die Erweiterungen in der Benutzerkonfiguration gelten, gelten auch für die im Abschnitt MachineConfiguration.

**Anwendungsfunktionen**: wird von Standardprogrammen verwendet, mit denen sich eine Anwendung wie folgt registrieren kann:

- Kann bestimmte Dateierweiterungen öffnen
- Ein Anwärter für den Internet Browser Steckplatz des Startmenüs
- Kann bestimmte Windows-MIME-Typen öffnen

Diese Erweiterung macht auch die virtuelle Anwendung in der Benutzeroberfläche für Standard Programme festlegen sichtbar.

```XML

<ApplicationCapabilities Enabled="true">

  <Extensions>

   <Extension Category="AppV.ApplicationCapabilities">

    <ApplicationCapabilities>


   <ApplicationId>[{PackageRoot}]\LitView\LitViewBrowser.exe</ApplicationId>

     <Reference>

      <Name>LitView Browser</Name>

      <Path>SOFTWARE\LitView\Browser\Capabilities</Path>

     </Reference>

   <CapabilityGroup>

    <Capabilities>


   <Name>@[{ProgramFilesX86}]\LitView\LitViewBrowser.exe,-12345</Name>


   <Description>@[{ProgramFilesX86}]\LitView\LitViewBrowser.exe,-12346</Description>

     <Hidden>0</Hidden>

     <EMailSoftwareClient>Lit View E-Mail Client</EMailSoftwareClient>

     <FileAssociationList>

      <FileAssociation Extension=".htm" ProgID="LitViewHTML" />

      <FileAssociation Extension=".html" ProgID="LitViewHTML" />

      <FileAssociation Extension=".shtml" ProgID="LitViewHTML" />

     </FileAssociationList>

     <MIMEAssociationList>

      <MIMEAssociation Type="audio/mp3" ProgID="LitViewHTML" />

      <MIMEAssociation Type="audio/mpeg" ProgID="LitViewHTML" />

     </MIMEAssociationList>

    <URLAssociationList>

      <URLAssociation Scheme="http" ProgID="LitViewHTML.URL.http" />

     </URLAssociationList>

     </Capabilities>

  </CapabilityGroup>

   </ApplicationCapabilities>

  </Extension>

</Extensions>

</ApplicationCapabilities>
```

_**Unterstützte Erweiterungs Subsysteme:**_ 

**Machine Wide Virtual Registry** Extension Subsystem legt einen Registrierungsschlüssel in der virtuellen Registrierung innerhalb HKEY_LOCAL_MACHINE fest.

```XML

<Registry>

<Include>

  <Key Path="\REGISTRY\\Machine\Software\ABC">

    <Value Type="REG_SZ" Name="Bar" Data="Baz" />

   </Key>

  <Key Path="\REGISTRY\Machine\Software\EmptyKey" />

 </Include>

<Delete>

</Registry>
```

**Computerweite virtuelle Kernel Objekte**

```XML

<Objects>

<NotIsolate>

   <Object Name="testObject" />

 </NotIsolate>

</Objects>
```

#### ProductSourceURLOptOut

Verwenden Sie ProductSourceURLOptOut, um anzugeben, dass die URL für das Paket global über _PackageSourceRoot_ (zur Unterstützung von Zweigstellenszenarien) geändert werden kann. Änderungen werden beim nächsten Start wirksam. 

```XML

<MachineConfiguration>

  ... 

  <ProductSourceURLOptOut Enabled="true" />

  ...

</MachineConfiguration>
```

#### MachineScripts

Das Paket kann so konfiguriert werden, dass Skripts zum Zeitpunkt der Bereitstellung, Veröffentlichung oder Entfernung ausgeführt werden. Wenn Sie ein Beispielskript anzeigen möchten, lesen Sie die vom Sequencer generierte Konfigurationsdatei für die Bereitstellung. 

Im Abschnitt "Skripts" unten finden Sie weitere Informationen zu den verschiedenen Triggern, die verwendet werden können.

#### TerminateChildProcess

Eine ausführbare Datei der Anwendung kann angegeben werden, deren untergeordnete Prozesse beendet werden, wenn der exe-Prozess der Anwendung beendet wird.

```XML

<MachineConfiguration>

  ...   

  <TerminateChildProcesses>

    <Application Path="[{PackageRoot}]\Contoso\ContosoApp.EXE" />

    <Application Path="[{PackageRoot}]\LitView\LitViewBrowser.exe" />

    <Application Path="[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE" />

  </TerminateChildProcesses>

  ...

</MachineConfiguration>
```



## Skripts

In der folgenden Tabelle werden die verschiedenen Skriptereignisse und der Kontext beschrieben, unter dem Sie ausgeführt werden können.

| Skript Ausführungszeit       | Kann in der Bereitstellungskonfiguration angegeben werden | Kann in der Benutzerkonfiguration angegeben werden | Kann in der virtuellen Umgebung des Pakets ausgeführt werden | Kann im Kontext einer bestimmten Anwendung ausgeführt werden | Wird im System/Benutzerkontext ausgeführt: (Bereitstellungskonfiguration, Benutzerkonfiguration) |
|-----------------------------|----------------------------------------------|----------------------------------------|---------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------|
| AddPackage                  | X                                            |                                        |                                                   |                                                     | (System, N/A)                                                               |
| PublishPackage              | X                                            | X                                      |                                                   |                                                     | (System, Benutzer)                                                              |
| UnpublishPackage            | X                                            | X                                      |                                                   |                                                     | (System, Benutzer)                                                              |
| RemovePackage               | X                                            |                                        |                                                   |                                                     | (System, N/A)                                                               |
| StartProcess                | X                                            | X                                      | X                                                 | X                                                   | (Benutzer, Benutzer)                                                                |
| ExitProcess                 | X                                            | X                                      |                                                   | X                                                   | (Benutzer, Benutzer)                                                                |
| StartVirtualEnvironment     | X                                            | X                                      | X                                                 |                                                     | (Benutzer, Benutzer)                                                                |
| TerminateVirtualEnvironment | X                                            | X                                      |                                                   |                                                     | (Benutzer, Benutzer)                                                                |

### Verwenden mehrerer Skripts für einen einzelnen Ereignisauslöser

App-v 5,1 unterstützt die Verwendung mehrerer Skripts für einen einzelnen Ereignisauslöser für App-v-Pakete, einschließlich Pakete, die Sie von App-v 4,6 in App-v 5,0 oder höher konvertieren. Um die Verwendung mehrerer Skripts zu ermöglichen, verwendet App-v 5,1 eine Skript Startanwendung mit dem Namen ScriptRunner.exe, die als Teil der APP-v-Clientinstallation installiert wird.

### Verwenden mehrerer Skripts für einen einzelnen Ereignisauslöser

Übergeben Sie das Skript für jedes Skript, das Sie ausführen möchten, als Argument an die ScriptRunner.exe-Anwendung. Die Anwendung führt dann jedes Skript separat zusammen mit den Argumenten aus, die Sie für jedes Skript angeben. Verwenden Sie pro Trigger nur ein Skript (ScriptRunner.exe).

> [!NOTE]
> 
> Wir empfehlen, dass Sie zuerst die mehr Skript Zeile an einer Eingabeaufforderung ausführen, um sicherzustellen, dass alle Argumente ordnungsgemäß erstellt wurden, bevor Sie Sie zur Bereitstellungs Konfigurationsdatei hinzufügen.

### Beispielskript-und Parameterbeschreibungen

Verwenden Sie die folgende Beispieldatei und-Tabelle, und ändern Sie die Bereitstellungs-oder Benutzerkonfigurationsdatei, um die Skripts hinzuzufügen, die ausgeführt werden sollen.

```XML
<MachineScripts>
 <AddPackage>
   <Path>ScriptRunner.exe</Path>
   <Arguments>
   -appvscript script1.exe arg1 arg2 –appvscriptrunnerparameters –wait –timeout=10
   -appvscript script2.vbs arg1 arg2
   -appvscript script3.bat arg1 arg2 –appvscriptrunnerparameters –wait –timeout=30 –rollbackonerror
   </Arguments>
   <Wait timeout=”40” RollbackOnError=”true”/>
 </AddPackage>
</MachineScripts>
```


**Zu den Parametern in der Beispieldatei gehören:**

#### \<AddPackage\>

Name des Ereignisauslösers, für den Sie ein Skript ausführen, beispielsweise das Hinzufügen eines Pakets oder das Veröffentlichen eines Pakets.

#### \<Path\>ScriptRunner.exe\</Path\>

Die Skript Startanwendung, die als Teil der App-V-Clientinstallation installiert wird.

> [!NOTE]
> 
> Obwohl ScriptRunner.exe als Teil des App-v-Clients installiert wird, muss sich der Speicherort des App-v-Clients in% path% befinden, oder ScriptRunner wird nicht ausgeführt. ScriptRunner.exe befindet sich normalerweise im C:FilesApplication-Virtualizationfolder.

#### \<Arguments\>

`-appvscript` -Token, das das eigentliche Skript darstellt, das Sie ausführen möchten.

`script1.exe` – Name des Skripts, das Sie ausführen möchten.

`arg1 arg2` – Argumente für das Skript, das Sie ausführen möchten.

`-appvscriptrunnerparameters` – Token, das die Ausführungsoptionen für script1.exe darstellt.

`-wait` – Token, das ScriptRunner informiert, dass die Ausführung von script1.exe abgewartet werden soll, bevor Sie mit dem nächsten Skript fortfahren.

`-timeout=x` – Token, das ScriptRunner informiert, dass das aktuelle Skript nach x Sekunden nicht mehr ausgeführt werden soll. Alle anderen angegebenen Skripts werden weiterhin ausgeführt.

`-rollbackonerror` – Token, das ScriptRunner informiert, dass die Ausführung aller noch nicht ausgeführten Skripts beendet werden soll, und ein Rollback für einen Fehler beim App-V-Client ausgeführt werden soll.

#### \<Wait timeout=”40” RollbackOnError=”true”/\>

Wartet auf die allgemeine Fertigstellung von ScriptRunner.exe.

Setzen Sie den Timeoutwert für den gesamten Runner auf größer als oder gleich der Summe der Timeoutwerte für die einzelnen Skripts.

Wenn ein einzelnes Skript einen Fehler gemeldet hat und rollbackonerror auf "true" festgelegt wurde, meldet ScriptRunner den Fehler dem App-V-Client.

ScriptRunner führt alle Skripts aus, deren Dateityp einer auf dem Computer installierten Anwendung zugeordnet ist. Wenn die zugeordnete Anwendung nicht vorhanden ist oder der Dateityp des Skripts keiner Anwendung auf dem Computer zugeordnet ist, wird das Skript nicht ausgeführt.

### Erstellen einer dynamischen Konfigurationsdatei mit einer App-V 5,1-Manifestdatei

Sie können die dynamische Konfigurationsdatei mit einer von drei Methoden erstellen: entweder manuell mithilfe der App-V 5,1-Verwaltungskonsole oder durch Sequenzierung eines Pakets, das zwei Beispieldateien generiert. Weitere Informationen zum Erstellen der Datei mithilfe der APP-v 5,1-Verwaltungskonsole finden Sie unter [Erstellen einer benutzerdefinierten Konfigurationsdatei mithilfe der APP-v 5,1-Verwaltungskonsole](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md).

Wenn Sie die Datei manuell erstellen möchten, können die obigen Informationen in den vorherigen Abschnitten in einer einzelnen Datei kombiniert werden. Wir empfehlen die Verwendung von Dateien, die vom Sequencer generiert wurden.



- [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.
- Verwenden Sie für App-v-Probleme das [App-v TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen

- [Sie wenden Sie die Bereitstellungskonfigurationsdatei mithilfe von PowerShell an](how-to-apply-the-deployment-configuration-file-by-using-powershell51.md)

- [So wenden Sie die Benutzerkonfigurationsdatei mithilfe von PowerShell an](how-to-apply-the-user-configuration-file-by-using-powershell51.md)

- [Vorgänge für App-V 5.1](operations-for-app-v-51.md)

---
