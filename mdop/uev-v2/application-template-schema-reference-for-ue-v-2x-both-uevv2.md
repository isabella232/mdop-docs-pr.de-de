---
title: Schema Referenz für Anwendungsvorlagen für UE-V 2. x
description: Schema Referenz für Anwendungsvorlagen für UE-V 2. x
author: dansimp
ms.assetid: be8735a5-6a3e-4b1f-ba14-2a3bc3e5a8b6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 03ff6eabae68f07c23d5977f901e6a90e292c6ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812337"
---
# Schema Referenz für Anwendungsvorlagen für UE-V 2. x


Microsoft User Experience Virtualization (UE-v) 2,0, 2,1 und 2,1 SP1 verwenden Sie XML-Einstellungen, um die Einstellungen für die Desktopanwendung und die Windows-Einstellungen zu definieren, die von UE-v erfasst und angewendet werden. UE-V enthält eine Reihe von Standardeinstellungen für Standort Vorlagen. Sie können auch mit dem UE-V-Generator benutzerdefinierte Standort Vorlagen für Einstellungen erstellen.

Ein fortgeschrittener Benutzer kann die XML-Datei für eine Einstellungs Speicherort Vorlage anpassen. In diesem Thema wird die XML-Struktur der Einstellungen für die Standort Vorlagen UE-V 2,1 (SP1) und 2,0 erläutert, und es werden Anleitungen zum Bearbeiten dieser Dateien bereitgestellt.

## UE-V 2,1 und 2,1 SP1-Schema Referenz für Anwendungsvorlagen


In diesem Abschnitt wird die XML-Struktur der Standort Vorlage UE-V 2,1 und 2,1 SP1 erläutert, und es werden Anleitungen zum Bearbeiten dieser Datei bereitgestellt.

### Inhalt dieses Abschnitts

-   [XML-Deklaration und Codierungsattribut](#xml21)

-   [Namespace und Stamm Element](#namespace21)

-   [Datentypen](#data21)

-   [Name-Element](#name21)

-   [ID-Element](#id21)

-   [Version-Element](#version21)

-   [Author-Element](#author21)

-   [Prozesse und Prozess Element](#processes21)

-   [Application-Element](#application21)

-   [Common-Element](#common21)

-   [SettingsLocationTemplate-Element](#settingslocationtemplate21)

-   [Anhang: SettingsLocationTemplate. xsd](#appendix21)

### <a href="" id="xml21"></a>XML-Deklaration und Codierungsattribut

**Obligatorisch: wahr**

**Typ: Zeichenfolge**

Die XML-Deklaration muss das XML-Version 1,0-Attribut ( &lt; ? XML-Version = "1.0" &gt; ) angeben. Vom UE-V-Generator erstellte Einstellungen für Standort Vorlagen werden in UTF-8-Codierung gespeichert, obwohl die Codierung nicht explizit angegeben wird. Wir empfehlen, dass Sie das Attribut Encoding = "UTF-8" in dieses Element als bewährte Methode einbeziehen. Alle im Lieferumfang des Produkts enthaltenen Vorlagen geben diesen Tag ebenfalls an (Informationen finden Sie in den Dokumenten in%programfiles%\\Microsoft Benutzeroberflächen-Virtualization\\Templates als Referenz). Beispiel:

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace21"></a>Namespace und Stamm Element

**Obligatorisch: wahr**

**Typ: Zeichenfolge**

UE-V verwendet den https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate Namespace für alle Anwendungen. SettingsLocationTemplate ist das Stammelement und enthält alle anderen Elemente. Verweisen Sie SettingsLocationTemplate in allen Vorlagen mit diesem Tag:

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data21"></a>Datentypen

Hierbei handelt es sich um die Datentypen für das Anwendungsvorlagen Schema UE-V.

<a href="" id="guid"></a>**GUID** GUID beschreibt einen standardmäßigen Standardausdruck für global eindeutigen Bezeichner in der Form "\ \ {\ [a-FA-F0-9 \] {8} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {12} \ \}". Diese wird im Filesetting\\Root\\KnownFolder-Element verwendet, um die Formatierung bekannter Ordner zu überprüfen.

<a href="" id="filenamestring"></a>**Filenamed** Filenamed bezieht sich auf den Dateinamen eines zu überwachenden Prozesses. Die Werte sind durch das Regex-Element \ [^ \ \ \ \ \ \? &lt; &gt; /: \] +, (das heißt, Sie dürfen keine umgekehrten Schrägstriche, Sternchen oder Fragezeichen-Wildcard-Zeichen, das Pipe-Zeichen, das größer-als-oder kleiner-als-Zeichen, Schrägstrich oder Doppelpunktzeichen) enthalten.

<a href="" id="idstring"></a>**IDString** IDString bezieht sich auf den ID-Wert von Application-Elementen, SettingsLocationTemplate und Common Elements (verwendet, um Anwendungssuiten zu beschreiben, die gemeinsame Einstellungen aufweisen). Sie ist durch denselben Regex-Ausdruck wie filenamed eingeschränkt (\ [^ \ \ \ \ \ \? \ \ \ * \ \ | &lt; &gt; /:\]+).

<a href="" id="templateversion"></a>**TemplateVersion** TemplateVersion ist ein ganzzahliger Wert, der zur Beschreibung der Überarbeitung der Vorlage für die Einstellungsposition verwendet wird. Der Wert kann zwischen 0 und 2147483647 liegen.

<a href="" id="empty"></a>**Leer** Empty bezieht sich auf einen NULL-Wert. Dieser wird in Process\\ShellProcess verwendet, um anzugeben, dass kein zu überwachenden Prozess vorhanden ist. Dieser Wert sollte in keiner Anwendungsvorlage verwendet werden.

<a href="" id="author"></a>**Autor** Der Datentyp "Autor" ist ein komplexer Typ, der den Autor einer Vorlage identifiziert. Sie enthält zwei untergeordnete Elemente: **Name** und **e-Mail**. Im Datentyp "Author" ist das Name-Element obligatorisch, während das e-Mail-Element optional ist. Dieser Typ wird im SettingsLocationTemplate-Element ausführlicher beschrieben.

<a href="" id="range"></a>**Bereich** Bereich definiert eine ganzzahlige Klasse, die aus zwei untergeordneten Elementen besteht: **Mindest** -und **höchst**Wert. Dieser Datentyp wird im Datentyp ProcessVersion implementiert. Wenn angegeben, müssen sowohl Mindest-als auch Maximalwerte enthalten sein.

<a href="" id="processversion"></a>**ProcessVersion** ProcessVersion definiert einen Typ mit vier untergeordneten Elementen: **Major**, **Minor**, **Build**und **Patch**. Dieser Datentyp wird vom Process-Element zum Auffüllen seiner ProductVersion-und fileversion-Werte verwendet. Bei den Daten für diesen Typ handelt es sich um einen Bereichswert. Das wichtigste untergeordnete Element ist obligatorisch, und die anderen sind optional.

<a href="" id="architecture"></a>**Architektur** Architektur listet zwei mögliche Werte auf: **Win32** und **Win64**. Diese Werte werden verwendet, um die Prozessarchitektur festzulegen.

<a href="" id="process"></a>**Prozess** Der Prozessdatentyp ist ein Container, der zur Beschreibung der von UE-V zu überwachenden Prozesse dient. Sie enthält sechs untergeordnete Elemente: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**und **fileversion**. In dieser Tabelle werden die jeweiligen Datentypen der einzelnen Elemente beschrieben:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Element</strong></p></td>
<td align="left"><p><strong>Datentyp</strong></p></td>
<td align="left"><p><strong>Mandatory</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Dateiname</p></td>
<td align="left"><p>Filenamed</p></td>
<td align="left"><p>Wahr</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Architektur</p></td>
<td align="left"><p>Architektur</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>ProductName</p></td>
<td align="left"><p>Zeichenfolge</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FileDescription</p></td>
<td align="left"><p>Zeichenfolge</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>ProductVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>File Version</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>False</p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a>**Prozesse** Der Datentyp "Prozesse" stellt einen Container für eine Sammlung von einem oder mehreren Process-Elementen dar. Im Sequence-Typ Prozesse werden zwei untergeordnete Elemente unterstützt: **Process** und **ShellProcess**. Process ist ein Element vom Typ Process, und ShellProcess ist vom Datentyp leer. Es muss mindestens ein Element in der Sequenz identifiziert werden.

<a href="" id="path"></a>**Path** Path wird von RegistrySetting und filesetting verwendet, um auf Registrierungs-und Dateipfade zu verweisen. Dieses Element unterstützt zwei optionale Attribute: **rekursiv** und **DeleteIfNotFound**. Beide Werte sind auf Default = "false" festgelegt.

Rekursiv gibt an, dass der Pfad und alle Unterordner für Datei Einstellungen enthalten sind oder dass alle untergeordneten Registrierungsschlüssel für Registrierungseinstellungen enthalten sind. In beiden Fällen sind alle Elemente auf der aktuellen Ebene in den erfassten Daten enthalten. Bei einem filesettings-Objekt sind alle Dateien innerhalb des angegebenen Ordners in den von UE-V erfassten Daten enthalten, aber Ordner sind nicht enthalten. Bei Registrierungspfaden werden alle Werte im aktuellen Pfad erfasst, aber die untergeordneten Registrierungsschlüssel werden nicht erfasst. In beiden Fällen sollte darauf geachtet werden, große Datenmengen oder eine große Anzahl von Elementen nicht zu erfassen.

Das DeleteIfNotFound-Attribut entfernt die Einstellungen aus den Speicherpfad Daten des Benutzers. Dies kann in den Fällen wünschenswert sein, in denen durch das Entfernen dieser Einstellungen aus dem Paket eine große Menge an Speicherplatz auf dem Dateiserver für Settings Storage Path gespart wird.

<a href="" id="filemask"></a>**Filemask** Filemask gibt nur bestimmte Dateitypen für den Ordner an, der durch path definiert ist. Path könnte beispielsweise sein, `C:\users\username\files` und die Dateimaske kann `*.txt` nur Textdateien enthalten.

<a href="" id="registrysetting"></a>**RegistrySetting** RegistrySetting stellt einen Container für Registrierungsschlüssel und-Werte und das zugeordnete gewünschte Verhalten auf Seiten des UE-V-Agents dar. In diesem Typ werden vier untergeordnete Elemente definiert: **path**, **Name**, **Exclude**und eine Sequenz des Werte **Pfads** und- **namens**.

<a href="" id="filesetting"></a>**Filesetting** Filesetting enthält Parameter, die mit Dateien und Dateipfaden verknüpft sind. Es werden vier untergeordnete Elemente definiert: **root**, **path**, **filemask**und **Exclude**. Root ist obligatorisch und die anderen sind optional.

<a href="" id="settings"></a>**Einstellungen** Einstellungen ist ein Container für alle Einstellungen, die für eine bestimmte Vorlage gelten. Sie enthält Instanzen der zuvor beschriebenen Registrierungs-, Datei-, Systemparameter-und benutzerdefinierten Einstellungen. Darüber hinaus kann Sie auch die folgenden untergeordneten Elemente mit den beschriebenen Verhaltensweisen enthalten:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Element</strong></p></td>
<td align="left"><p><strong>Beschreibung</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Asynchrone</p></td>
<td align="left"><p>Asynchrone Einstellungs Pakete werden angewendet, ohne den Anwendungsstart zu blockieren, damit der Anwendungsstart fortgesetzt wird, während die Einstellungen noch angewendet werden. Dies ist nützlich für Einstellungen, die asynchron angewendet werden können, beispielsweise <code>get/set</code> über eine API, wie SystemParameterSetting.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PreventOverlappingSynchronization</p></td>
<td align="left"><p>Standardmäßig werden in UE-V nur Einstellungen für eine Anwendung gespeichert, wenn die letzte Instanz einer Anwendung, die die Vorlage verwendet, geschlossen ist. Wenn dieses Element auf "false" festgelegt ist, exportiert UE-V die Einstellungen selbst dann, wenn andere Instanzen einer Anwendung ausgeführt werden. Geeignete Vorlagen – diejenigen, die einen allgemeinen Element Abschnitt enthalten –, die mit UE-V ausgeliefert werden, verwenden dieses Flag, um freigegebene Einstellungen so zu aktivieren, dass Sie immer beim Schließen der Anwendung exportiert werden, während anwendungsspezifische Einstellungen vor dem Export verhindert werden, bis die letzte Instanz geschlossen ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AlwaysApplySettings</p></td>
<td align="left"><p>(eingeführt in 2,1)</p>
<p>Dieser Parameter erzwingt die Anwendung eines importierten Einstellungs Pakets, auch wenn es keine Unterschiede zwischen dem Paket und dem aktuellen Zustand der Anwendung gibt. Dieser Parameter sollte nur in speziellen Fällen verwendet werden, da er den Import von Einstellungen verlangsamen kann.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name21"></a>Name-Element

**Obligatorisch: wahr**

**Typ: Zeichenfolge**

Name gibt einen eindeutigen Namen für die Einstellungs Speicherort Vorlage an. Diese Funktion wird für Anzeigezwecke verwendet, wenn Sie in WMI, PowerShell, Ereignisanzeige und Debug-Protokollen auf die Vorlage verweisen. Im Allgemeinen sollten Sie nicht auf Versionsinformationen verweisen, da dies vom ProductVersion-Element abweichen kann. Geben Sie beispielsweise `<Name>My Application</Name>` anstelle ein `<Name>My Application 1.1</Name>` .

**Hinweis**  UE-V verweist nicht auf externe DTDs, daher ist es nicht möglich, benannte Entitäten in einer Einstellungen-Speicherort Vorlage zu verwenden. Verwenden Sie beispielsweise nicht, &reg; um auf das eingetragene Markenzeichen® zu verweisen. Verwenden Sie stattdessen kanonische nummerierte Bezüge, um diese Typen von Sonderzeichen einzubeziehen, beispielsweise & \ #174 für das® Zeichen. Diese Regel gilt für alle Zeichenfolgenwerte in diesem Dokument.

<http://www.w3.org/TR/xhtml1/dtds.html>Eine vollständige Liste der Zeichenentitäten finden Sie unter. UTF-8-codierte Dokumente enthalten möglicherweise die Unicode-Zeichen direkt. Beim Speichern von Vorlagen über den UE-V-Generator werden Zeichenentitäten automatisch in ihre Unicode-Darstellungen konvertiert.

 

### <a href="" id="id21"></a>ID-Element

**Obligatorisch: wahr**

**Typ: Zeichenfolge**

ID füllt einen eindeutigen Bezeichner für eine bestimmte Vorlage auf. Dieses Tag wird zur primären Kennung, mit der der UE-V-Agent zur Laufzeit auf die Vorlage verweist (Beispiel: Anzeigen der Ausgabe der PowerShell-Cmdlets "Get-UevTemplate" und "Get-UevTemplateProgram"). Nach Konvention sollte dieses Tag keine Leerzeichen enthalten, was das Skripting vereinfacht. In diesem Element sollten Versionsnummern von Anwendungen angegeben werden, um eine einfache Identifizierung der Vorlage zu ermöglichen, beispielsweise `<ID>MicrosoftCalculator6</ID>` oder `<ID>MicrosoftOffice2010Win64</ID>` .

### <a href="" id="version21"></a>Version-Element

**Obligatorisch: wahr**

**Typ: Ganzzahl**

**Minimaler Wert: 0**

**Maximaler Wert: 2147483647**

Version identifiziert die Version der Vorlage für die Einstellungsposition für die administrative Nachverfolgung von Änderungen. Der UE-V-Generator erhöht diese Zahl automatisch um eins, wenn die Vorlage gespeichert wird. Beachten Sie, dass dieses Feld eine ganze Zahl Ganzzahl sein muss. Gebrochene Werte, beispielsweise `<Version>2.5</Version>` sind nicht zulässig.

**Hinweis:** Sie können Notizen zu Versionsänderungen mithilfe von XML-Kommentar Tags speichern `<!-- -->` , beispielsweise:

```xml
  <!--
     Version History

     Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
     Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
     Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
     Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
   -->
  <Version>4</Version>
```

**Wichtig**  Dieser Wert wird abgefragt, um zu ermitteln, ob eine neue Version einer Vorlage in diesen Fällen auf eine vorhandene Vorlage angewendet werden soll:

-   Wenn der automatische Aktualisierungsvorgang der geplanten Vorlage ausgeführt wird

-   Wenn das PowerShell-Cmdlet "Update-UevTemplate" ausgeführt wird

-   Wenn die microsoft\\uev: SettingsLocationTemplate-Update Methode über WMI aufgerufen wird

 

### <a href="" id="author21"></a>Author-Element

**Obligatorisch: falsch**

**Typ: Zeichenfolge**

Autor identifiziert den Ersteller der Vorlage für die Einstellungsposition. Zwei optionale untergeordnete Elemente werden unterstützt: **Name** und **e-Mail**. Beide Attribute sind optional, aber wenn das untergeordnete e-Mail-Element angegeben ist, muss es vom Name-Element begleitet werden. Der Autor bezieht sich auf den vollständigen Namen des Kontakts für die Vorlage "Settings Location", und e-Mail sollte auf eine e-Mail-Adresse für den Autor verweisen. Wir empfehlen, dass Sie diese Informationen in öffentlich veröffentlichte Vorlagen einbeziehen, beispielsweise im [Vorlagenkatalog UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).

### <a href="" id="processes21"></a>Prozesse und Prozess Element

**Obligatorisch: wahr**

**Typ: Element**

Prozesse enthält mindestens ein `<Process>` Element, das wiederum die folgenden untergeordneten Elemente enthält: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**und **fileversion**. Das untergeordnete FileName-Element ist obligatorisch, die anderen sind optional. Ein vollständig aufgefülltes Element enthält Tags ähnlich wie in diesem Beispiel:

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### Dateiname

**Obligatorisch: wahr**

**Typ: Zeichenfolge**

Filename bezieht sich auf den tatsächlichen Dateinamen der ausführbaren Datei, wie Sie im Dateisystem angezeigt wird. Dieses Element gibt das primäre Kriterium an, mit dem UE-V auswerten soll, ob eine Vorlage für einen Prozess gilt oder nicht. Dieses Element muss in der XML-Vorlage für die Einstellungsposition angegeben werden.

Gültige Dateinamen dürfen nicht mit dem regulären Ausdruck \ [^ \ \ \ \ \ \? \ \ \ * \ \ | &lt; &gt; /: \] +, das heißt, Sie dürfen keine umgekehrten Schrägstriche, Sternchen-oder Fragezeichen-Wildcards, das Pipe-Zeichen, das größer-als-oder kleiner-als-Zeichen, den Schrägstrich oder den Doppelpunkt enthalten (\ \? \* | &lt; &gt; /oder: Zeichen.).

**Hinweis:** Um eine Zeichenfolge für diesen Regex zu testen, verwenden Sie ein PowerShell-Befehlsfenster, und ersetzen Sie den Namen der ausführbaren Datei für **YourFileName**:

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

Der Wert **true** gibt an, dass die Zeichenfolge ungültige Zeichen enthält. Im folgenden finden Sie einige Beispiele für ungültige Werte:

-   \\\\server\\share\\program.exe

-   Programm \ *. exe

-   Pro? ram.exe

-   Programm &lt; 1 &gt; . exe

**Hinweis**  Der UE-V-Generator codiert das größer-als-und das kleiner-als-Zeichen &gt; &lt; .

 

In seltenen Fällen enthält der FileName-Wert nicht unbedingt die Erweiterung ". exe", sollte aber als Teil des Werts angegeben werden. Beispielsweise `<Filename>MyApplictication.exe</Filename>` sollte angegeben werden, anstatt `<Filename>MyApplictication</Filename>` . Im zweiten Beispiel wird die Vorlage nicht auf den Prozess angewendet, wenn der tatsächliche Name der ausführbaren Datei "MyApplication.exe" lautet.

### Architektur

**Obligatorisch: falsch**

**Typ: Architektur (Zeichenfolge)**

Architektur bezieht sich auf die Prozessorarchitektur, für die die ausführbare Ziel Datei kompiliert wurde. Gültige Werte sind Win32 für 32-Bit-Anwendungen oder win64 für 64-Bit-Anwendungen. Sofern vorhanden, schränkt dieses Tag die Anwendbarkeit der Vorlage "Settings Location" auf eine bestimmte Anwendungsarchitektur ein. Ein Beispiel hierfür finden Sie unter Vergleich der%programfiles%\\Microsoft-Benutzeroberflächen-Virtualization\\templates\\ MicrosoftOffice2010Win32.xml und MicrosoftOffice2010Win64.xml Dateien, die in UE-V enthalten sind. Dies ist hilfreich, wenn relative Pfade zwischen unterschiedlichen Versionen einer ausführbaren Datei geändert werden oder wenn Einstellungen hinzugefügt oder entfernt wurden, wenn Sie von einer Prozessorarchitektur zu einer anderen wechseln.

Wenn dieses Element nicht vorhanden ist, ignoriert die Vorlage "Einstellungen" die Architektur des Prozesses und bezieht sich auf 32-und 64-Bit-Prozesse, wenn der Dateiname und andere Attribute angewendet werden.

**Hinweis**  UE-V unterstützt keine ARM-Prozessoren in dieser Version.

 

### ProductName

**Obligatorisch: falsch**

**Typ: Zeichenfolge**

ProductName ist ein optionales Element, das verwendet wird, um ein Produkt für administrative Zwecke oder Berichte zu identifizieren. ProductName unterscheidet sich von filename dadurch, dass für seinen Wert keine regulären Ausdruckseinschränkungen gelten. Auf diese Weise können Beschreibungen eines Prozesses leichter verstanden werden, bei denen der Name der ausführbaren Datei möglicherweise nicht offensichtlich ist. Beispiel:

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### FileDescription

**Obligatorisch: falsch**

**Typ: Zeichenfolge**

FileDescription ist ein optionales Tag, das eine administrative Beschreibung der ausführbaren Datei ermöglicht. Hierbei handelt es sich um ein kostenloses Textfeld, das bei der Unterscheidung mehrerer ausführbarer Dateien innerhalb eines Softwarepakets hilfreich sein kann, wenn die Funktion der ausführbaren Datei identifiziert werden muss.

In einer geeigneten Anwendung kann es beispielsweise hilfreich sein, die Funktion von zwei ausführbaren Dateien (MyApplication.exe und MyApplicationHelper.exe) zu informieren, wie hier gezeigt:

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### ProductVersion

**Obligatorisch: falsch**

**Typ: Zeichenfolge**

ProductVersion bezieht sich auf die Haupt-und Nebenversionen einer Datei sowie auf eine Build-und Patchebene. ProductVersion ist ein optionales Element, aber wenn angegeben, muss es mindestens das wichtigste untergeordnete Element enthalten. Der Wert muss einen Bereich in der Form mindestens = "x" Maximum = "y" ausdrücken, wobei X und Y ganze Zahlen sind. Die Mindest-und Höchstwerte können identisch sein.

Die Elemente "Produkt" und "Dateiversion" werden möglicherweise nicht angegeben. Dadurch wird die Vorlage "versionsunabhängig", was bedeutet, dass die Vorlage auf alle Versionen der angegebenen ausführbaren Datei angewendet wird.

**Beispiel 1:**

Produktversion: 1,0, die im UE-V-Generator angegeben wird, erzeugt den folgenden XML-Code:

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**Beispiel 2:**

Dateiversion: im UE-V-Generator angegebene 5.0.2.1000 erzeugt den folgenden XML-Code:

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**Falsches Beispiel 1 – unvollständiger Bereich:**

Es ist nur das kleinste Attribut vorhanden. Maximum muss auch in einem Bereich enthalten sein.

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**Falsches Beispiel 2 – Moll ohne Hauptelement angegeben:**

Nur das nebengeordnete Element ist vorhanden. Major muss ebenfalls enthalten sein.

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### File Version

**Obligatorisch: falsch**

**Typ: Zeichenfolge**

Fileversion unterscheidet zwischen der Veröffentlichungsversion einer veröffentlichten Anwendung und den internen Builddaten einer ausführbaren Komponente. Bei den meisten kommerziellen Anwendungen sind diese Nummern identisch. Wenn Sie unterschiedlich sind, gibt die Produktversion einer Datei eine generische Versionskennung einer Datei an, während die Dateiversion einen bestimmten Build einer Datei angibt (wie im Fall eines Hotfix oder Updates). Dadurch werden Dateien eindeutig identifiziert, ohne die Erkennungslogik zu unterbrechen.

Wenn Sie die Produktversion und die Dateiversion einer bestimmten ausführbaren Datei ermitteln möchten, klicken Sie mit der rechten Maustaste auf die Datei in Windows-Explorer, wählen Sie Eigenschaften aus, und klicken Sie dann auf die Registerkarte Details.

Das Einfügen eines fileversion-Elements für eine Anwendung ermöglicht eine genauere Feintuning-Erkennungslogik, ist für die meisten Anwendungen jedoch nicht erforderlich. Die ProductVersion-Elementeinstellungen werden zuerst überprüft, und dann wird die Dateiversion aktiviert. Die restriktivere Einstellung wird angewendet.

Die untergeordneten Elemente und Syntaxregeln für fileversion sind mit denen von ProductVersion identisch.

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application21"></a>Application-Element

Application ist ein Container für Einstellungen, die für eine bestimmte Anwendung gelten. Es handelt sich um eine Sammlung der folgenden Felder/Typen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Feld/Typ</strong></p></td>
<td align="left"><p><strong>Beschreibung</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Name</p></td>
<td align="left"><p>Gibt einen eindeutigen Namen für die Vorlage "Settings Location" an. Diese Funktion wird für Anzeigezwecke verwendet, wenn Sie in WMI, PowerShell, Ereignisanzeige und Debug-Protokollen auf die Vorlage verweisen. Weitere Informationen finden Sie unter <a href="#name21" data-raw-source="[Name](#name21)"> Name </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ID</p></td>
<td align="left"><p>Füllt einen eindeutigen Bezeichner für eine bestimmte Vorlage auf. Dieses Tag wird zur primären Kennung, mit der der UE-V-Agent zur Laufzeit auf die Vorlage verweist. Weitere Informationen finden Sie unter <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Beschreibung</p></td>
<td align="left"><p>Eine optionale Beschreibung der Vorlage.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Ein optionaler Name, der auf der Benutzeroberfläche angezeigt wird und von einem Gebietsschema der Sprache lokalisiert wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Eine optionale Vorlagenbeschreibung, die von einem Sprachgebietsschema lokalisiert wurde.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Version</p></td>
<td align="left"><p>Identifiziert die Version der Vorlage für die Einstellungsposition für die administrative Nachverfolgung von Änderungen. Weitere Informationen finden Sie unter <a href="#version21" data-raw-source="[Version](#version21)"> Version </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Steuert, ob diese Vorlage in Verbindung mit einem Microsoft-Konto aktiviert ist oder nicht. Wenn die Synchronisierung von MSA für einen Benutzer auf einem Computer aktiviert ist, wird diese Vorlage automatisch deaktiviert.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>Ähnlich wie MSA steuert dies, ob diese Vorlage in Verbindung mit Office365 aktiviert ist. Wenn Office 365 zum Synchronisieren von Einstellungen verwendet wird, wird diese Vorlage automatisch deaktiviert.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FixedProfile (eingeführt in 2,1)</p></td>
<td align="left"><p>Gibt an, dass diese Vorlage nur dem in diesem Element angegebenen Profil zugeordnet werden kann und nicht über WMI oder PowerShell geändert werden kann.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Prozesse</p></td>
<td align="left"><p>Ein Container für eine Sammlung von einem oder mehreren Process-Elementen. Weitere Informationen finden Sie unter <a href="#processes21" data-raw-source="[Processes](#processes21)"> Prozesse </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Einstellungen</p></td>
<td align="left"><p>Ein Container für alle Einstellungen, die für eine bestimmte Vorlage gelten. Sie enthält Instanzen der Registrierungs-, Datei-, Systemparameter-und benutzerdefinierten Einstellungen. Weitere Informationen finden Sie unter <strong> Einstellungen </strong> in <a href="#data21" data-raw-source="[Data types](#data21)"> Datentypen </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common21"></a>Common-Element

Common ist mit einem Application-Element vergleichbar, wird aber immer mit zwei oder mehr Anwendungselementen verknüpft. Der allgemeine Abschnitt stellt den Satz von Einstellungen dar, die zwischen diesen Anwendungsinstanzen freigegeben werden. Es handelt sich um eine Sammlung der folgenden Felder/Typen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Feld/Typ</strong></p></td>
<td align="left"><p><strong>Beschreibung</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Name</p></td>
<td align="left"><p>Gibt einen eindeutigen Namen für die Vorlage "Settings Location" an. Diese Funktion wird für Anzeigezwecke verwendet, wenn Sie in WMI, PowerShell, Ereignisanzeige und Debug-Protokollen auf die Vorlage verweisen. Weitere Informationen finden Sie unter <a href="#name21" data-raw-source="[Name](#name21)"> Name </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ID</p></td>
<td align="left"><p>Füllt einen eindeutigen Bezeichner für eine bestimmte Vorlage auf. Dieses Tag wird zur primären Kennung, mit der der UE-V-Agent zur Laufzeit auf die Vorlage verweist. Weitere Informationen finden Sie unter <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Beschreibung</p></td>
<td align="left"><p>Eine optionale Beschreibung der Vorlage.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Ein optionaler Name, der auf der Benutzeroberfläche angezeigt wird und von einem Gebietsschema der Sprache lokalisiert wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Eine optionale Vorlagenbeschreibung, die von einem Sprachgebietsschema lokalisiert wurde.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Version</p></td>
<td align="left"><p>Identifiziert die Version der Vorlage für die Einstellungsposition für die administrative Nachverfolgung von Änderungen. Weitere Informationen finden Sie unter <a href="#version21" data-raw-source="[Version](#version21)"> Version </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Steuert, ob diese Vorlage in Verbindung mit einem Microsoft-Konto aktiviert ist oder nicht. Wenn die Synchronisierung von MSA für einen Benutzer auf einem Computer aktiviert ist, wird diese Vorlage automatisch deaktiviert.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>Ähnlich wie MSA steuert dies, ob diese Vorlage in Verbindung mit Office365 aktiviert ist. Wenn Office 365 zum Synchronisieren von Einstellungen verwendet wird, wird diese Vorlage automatisch deaktiviert.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FixedProfile (eingeführt in 2,1)</p></td>
<td align="left"><p>Gibt an, dass diese Vorlage nur dem in diesem Element angegebenen Profil zugeordnet werden kann und nicht über WMI oder PowerShell geändert werden kann.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Einstellungen</p></td>
<td align="left"><p>Ein Container für alle Einstellungen, die für eine bestimmte Vorlage gelten. Sie enthält Instanzen der Registrierungs-, Datei-, Systemparameter-und benutzerdefinierten Einstellungen. Weitere Informationen finden Sie unter <strong> Einstellungen </strong> in <a href="#data21" data-raw-source="[Data types](#data21)"> Datentypen </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate21"></a>SettingsLocationTemplate-Element

Dieses Element definiert die Einstellungen für eine einzelne Anwendung oder eine Suite von Anwendungen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Feld/Typ</strong></p></td>
<td align="left"><p><strong>Beschreibung</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Name</p></td>
<td align="left"><p>Gibt einen eindeutigen Namen für die Vorlage "Settings Location" an. Diese Funktion wird für Anzeigezwecke verwendet, wenn Sie in WMI, PowerShell, Ereignisanzeige und Debug-Protokollen auf die Vorlage verweisen. Weitere Informationen finden Sie unter <a href="#name21" data-raw-source="[Name](#name21)"> Name </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ID</p></td>
<td align="left"><p>Füllt einen eindeutigen Bezeichner für eine bestimmte Vorlage auf. Dieses Tag wird zur primären Kennung, mit der der UE-V-Agent zur Laufzeit auf die Vorlage verweist. Weitere Informationen finden Sie unter <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Beschreibung</p></td>
<td align="left"><p>Eine optionale Beschreibung der Vorlage.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Ein optionaler Name, der auf der Benutzeroberfläche angezeigt wird und von einem Gebietsschema der Sprache lokalisiert wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Eine optionale Vorlagenbeschreibung, die von einem Sprachgebietsschema lokalisiert wurde.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix21"></a>Anhang: SettingsLocationTemplate. xsd

Hier sehen Sie die SettingsLocationTemplate. xsd-Datei mit den Elementen, untergeordneten Elementen, Attributen und Parametern:

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

    <xs:simpleType name="Guid">
        <xs:restriction base="xs:string">
            <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="FilenameString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="IDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="CompositeIDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+([.][^\\\?\*\|&lt;&gt;/:.]+)?" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="TemplateVersion">
        <xs:restriction base="xs:integer">
            <xs:minInclusive value="0" />
            <xs:maxInclusive value="2147483647" />
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Empty">
        <xs:sequence/>
    </xs:complexType>

    <xs:complexType name="LocalizedString">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Locale" type="xs:string" use="required"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="LocalizedName">
        <xs:sequence>
            <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="LocalizedDescription">
        <xs:sequence>
            <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="ReplacedTemplates">
      <xs:sequence>
        <xs:element name="ID" type="CompositeIDString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Author">
        <xs:all>
            <xs:element name="Name" type="xs:string" minOccurs="1" />
            <xs:element name="Email" type="xs:string" minOccurs="0" />
        </xs:all>
    </xs:complexType>

    <xs:complexType name="Range">
        <xs:attribute name="Minimum" type="xs:integer" use="required"/>
        <xs:attribute name="Maximum" type="xs:integer" use="required"/>
    </xs:complexType>

    <xs:complexType name="ProcessVersion">
        <xs:sequence>
            <xs:element name="Major" type="Range" minOccurs="1" />
            <xs:element name="Minor" type="Range" minOccurs="0" />
            <xs:element name="Build" type="Range" minOccurs="0" />
            <xs:element name="Patch" type="Range" minOccurs="0" />
        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="Architecture">
        <xs:restriction base="xs:string">
            <xs:enumeration value="Win32"/>
            <xs:enumeration value="Win64"/>
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Process">
        <xs:sequence>
            <xs:element name="Filename" type="FilenameString" minOccurs="1" />
            <xs:element name="Architecture" type="Architecture" minOccurs="0" />
            <xs:element name="ProductName" type="xs:string" minOccurs="0" />
            <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
            <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
            <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Processes">
        <xs:sequence>
            <xs:choice minOccurs="1">
                <xs:element name="Process" type="Process" />
                <xs:element name="ShellProcess" type="Empty" />
            </xs:choice>
            <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Path">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
                <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="RegistrySetting">
        <xs:sequence>
            <xs:element name="Path" type="Path" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="FileSetting">
        <xs:sequence>

            <xs:element name="Root">
                <xs:complexType>
                    <xs:choice>
                        <xs:element name="KnownFolder" type="Guid" />
                        <xs:element name="RegistryEntry" type="xs:string" />
                        <xs:element name="EnvironmentVariable" type="xs:string" />
                    </xs:choice>
                </xs:complexType>
            </xs:element>

            <xs:element name="Path" minOccurs="0" type="Path" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>

        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="CustomActionSetting">
        <xs:restriction base="xs:anyURI"/>
    </xs:simpleType>

    <xs:simpleType name="SystemParameterSetting">
        <xs:restriction base="xs:string">

            <!-- Accessibility parameters -->
            <xs:enumeration value="AccessTimeout"/>
            <xs:enumeration value="AudioDescription"/>
            <xs:enumeration value="ClientAreaAnimation"/>
            <xs:enumeration value="DisableOverlappedContent"/>
            <xs:enumeration value="FilterKeys"/>
            <xs:enumeration value="FocusBorderHeight"/>
            <xs:enumeration value="FocusBorderWidth"/>
            <xs:enumeration value="HighContrast"/>
            <xs:enumeration value="MessageDuration"/>
            <xs:enumeration value="MouseClickLock"/>
            <xs:enumeration value="MouseClickLockTime"/>
            <xs:enumeration value="MouseKeys"/>
            <xs:enumeration value="MouseSonar"/>
            <xs:enumeration value="MouseVanish"/>
            <xs:enumeration value="ScreenReader"/>
            <xs:enumeration value="ShowSounds"/>
            <xs:enumeration value="SoundSentry"/>
            <xs:enumeration value="StickyKeys"/>
            <xs:enumeration value="ToggleKeys"/>

            <!-- Input parameters -->
            <xs:enumeration value="Beep"/>
            <xs:enumeration value="BlockSendInputResets"/>
            <xs:enumeration value="DefaultInputLang"/>
            <xs:enumeration value="DoubleClickTime"/>
            <xs:enumeration value="DoubleClkHeight"/>
            <xs:enumeration value="DoubleClkWidth"/>
            <xs:enumeration value="KeyboardCues"/>
            <xs:enumeration value="KeyboardDelay"/>
            <xs:enumeration value="KeyboardPref"/>
            <xs:enumeration value="KeyboardSpeed"/>
            <xs:enumeration value="Mouse"/>
            <xs:enumeration value="MouseButtonSwap"/>
            <xs:enumeration value="MouseHoverHeight"/>
            <xs:enumeration value="MouseHoverTime"/>
            <xs:enumeration value="MouseHoverWidth"/>
            <xs:enumeration value="MouseSpeed"/>
            <xs:enumeration value="MouseTrails"/>
            <xs:enumeration value="SnapToDefButton"/>
            <xs:enumeration value="WheelScrollChars"/>
            <xs:enumeration value="WheelScrollLines"/>

            <!-- Desktop parameters (limited subset) -->
            <xs:enumeration value="DeskWallpaper"/>
            <xs:enumeration value="DesktopColor"/>

        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Settings">
        <xs:sequence>
            <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
            <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
            <xs:element name="AlwaysApplySettings" type="xs:boolean" minOccurs="0" />
            <xs:choice minOccurs="0" maxOccurs="unbounded">
                <xs:element name="Registry" type="RegistrySetting" />
                <xs:element name="File" type="FileSetting" />
                <xs:element name="SystemParameter" type="SystemParameterSetting" />
                <xs:element name="CustomAction" type="CustomActionSetting" />
            </xs:choice>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Common">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Application">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>


    <xs:element name="SettingsLocationTemplate">
        <xs:complexType>
            <xs:sequence>

                <xs:element name="Name" type="xs:string" />
                <xs:element name="ID" type="IDString" />
                <xs:element name="Description" type="xs:string" minOccurs="0" />
                <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
                <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

                <xs:choice>

                    <!-- Single application -->
                    <xs:sequence>
                        <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
                        <xs:element name="Version" type="TemplateVersion" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
                        <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
                        <xs:element name="Processes" type="Processes" />
                        <xs:element name="Settings" type="Settings" />
                    </xs:sequence>

                    <!-- Suite of applications -->
                    <xs:sequence>
                        <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="Common" type="Common" />
                        <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
                    </xs:sequence>

                </xs:choice>

            </xs:sequence>
        </xs:complexType>
    </xs:element>
    <!-- SettingsLocationTemplate -->

</xs:schema>
```

## UE-V 2,0-Schema Referenz für Anwendungsvorlagen


In diesem Abschnitt wird die XML-Struktur der Standort Vorlage "UE-V 2,0 Settings" erläutert, und es werden Anleitungen zum Bearbeiten dieser Datei bereitgestellt.

### Inhalt dieses Abschnitts

-   [XML-Deklaration und Codierungsattribut](#xml)

-   [Namespace und Stamm Element](#namespace)

-   [Datentypen](#data)

-   [Name-Element](#name)

-   [ID-Element](#id)

-   [Version-Element](#version)

-   [Author-Element](#author)

-   [Prozesse und Prozess Element](#processes)

-   [Application-Element](#application)

-   [Common-Element](#common)

-   [SettingsLocationTemplate-Element](#settingslocationtemplate)

-   [Anhang: SettingsLocationTemplate. xsd](#appendix)

### <a href="" id="xml"></a>XML-Deklaration und Codierungsattribut

**Obligatorisch: wahr**

**Typ: Zeichenfolge**

Die XML-Deklaration muss das XML-Version 1,0-Attribut ( &lt; ? XML-Version = "1.0" &gt; ) angeben. Vom UE-V-Generator erstellte Einstellungen für Standort Vorlagen werden in UTF-8-Codierung gespeichert, obwohl die Codierung nicht explizit angegeben wird. Wir empfehlen, dass Sie das Attribut Encoding = "UTF-8" in dieses Element als bewährte Methode einbeziehen. Alle im Lieferumfang des Produkts enthaltenen Vorlagen geben diesen Tag ebenfalls an (Informationen finden Sie in den Dokumenten in%programfiles%\\Microsoft Benutzeroberflächen-Virtualization\\Templates als Referenz). Beispiel:

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace"></a>Namespace und Stamm Element

**Obligatorisch: wahr**

**Typ: Zeichenfolge**

UE-V verwendet den https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate Namespace für alle Anwendungen. SettingsLocationTemplate ist das Stammelement und enthält alle anderen Elemente. Verweisen Sie SettingsLocationTemplate in allen Vorlagen mit diesem Tag:

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data"></a>Datentypen

Hierbei handelt es sich um die Datentypen für das Anwendungsvorlagen Schema UE-V.

<a href="" id="guid"></a>**GUID** GUID beschreibt einen standardmäßigen Standardausdruck für global eindeutigen Bezeichner in der Form "\ \ {\ [a-FA-F0-9 \] {8} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {12} \ \}". Diese wird im Filesetting\\Root\\KnownFolder-Element verwendet, um die Formatierung bekannter Ordner zu überprüfen.

<a href="" id="filenamestring"></a>**Filenamed** Filenamed bezieht sich auf den Dateinamen eines zu überwachenden Prozesses. Die Werte sind durch das Regex-Element \ [^ \ \ \ \ \ \? &lt; &gt; /: \] +, (das heißt, Sie dürfen keine umgekehrten Schrägstriche, Sternchen oder Fragezeichen-Wildcard-Zeichen, das Pipe-Zeichen, das größer-als-oder kleiner-als-Zeichen, Schrägstrich oder Doppelpunktzeichen) enthalten.

<a href="" id="idstring"></a>**IDString** IDString bezieht sich auf den ID-Wert von Application-Elementen, SettingsLocationTemplate und Common Elements (verwendet, um Anwendungssuiten zu beschreiben, die gemeinsame Einstellungen aufweisen). Sie ist durch denselben Regex-Ausdruck wie filenamed eingeschränkt (\ [^ \ \ \ \ \ \? \ \ \ * \ \ | &lt; &gt; /:\]+).

<a href="" id="templateversion"></a>**TemplateVersion** TemplateVersion ist ein ganzzahliger Wert, der zur Beschreibung der Überarbeitung der Vorlage für die Einstellungsposition verwendet wird. Der Wert kann zwischen 0 und 2147483647 liegen.

<a href="" id="empty"></a>**Leer** Empty bezieht sich auf einen NULL-Wert. Dieser wird in Process\\ShellProcess verwendet, um anzugeben, dass kein zu überwachenden Prozess vorhanden ist. Dieser Wert sollte in keiner Anwendungsvorlage verwendet werden.

<a href="" id="author"></a>**Autor** Der Datentyp "Autor" ist ein komplexer Typ, der den Autor einer Vorlage identifiziert. Sie enthält zwei untergeordnete Elemente: **Name** und **e-Mail**. Im Datentyp "Author" ist das Name-Element obligatorisch, während das e-Mail-Element optional ist. Dieser Typ wird im SettingsLocationTemplate-Element ausführlicher beschrieben.

<a href="" id="range"></a>**Bereich** Bereich definiert eine ganzzahlige Klasse, die aus zwei untergeordneten Elementen besteht: **Mindest** -und **höchst**Wert. Dieser Datentyp wird im Datentyp ProcessVersion implementiert. Wenn angegeben, müssen sowohl Mindest-als auch Maximalwerte enthalten sein.

<a href="" id="processversion"></a>**ProcessVersion** ProcessVersion definiert einen Typ mit vier untergeordneten Elementen: **Major**, **Minor**, **Build**und **Patch**. Dieser Datentyp wird vom Process-Element zum Auffüllen seiner ProductVersion-und fileversion-Werte verwendet. Bei den Daten für diesen Typ handelt es sich um einen Bereichswert. Das wichtigste untergeordnete Element ist obligatorisch, und die anderen sind optional.

<a href="" id="architecture"></a>**Architektur** Architektur listet zwei mögliche Werte auf: **Win32** und **Win64**. Diese Werte werden verwendet, um die Prozessarchitektur festzulegen.

<a href="" id="process"></a>**Prozess** Der Prozessdatentyp ist ein Container, der zur Beschreibung der von UE-V zu überwachenden Prozesse dient. Sie enthält sechs untergeordnete Elemente: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**und **fileversion**. In dieser Tabelle werden die jeweiligen Datentypen der einzelnen Elemente beschrieben:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Element</th>
<th align="left">Datentyp</th>
<th align="left">Mandatory</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Dateiname</p></td>
<td align="left"><p>Filenamed</p></td>
<td align="left"><p>Wahr</p></td>
</tr>
<tr class="even">
<td align="left"><p>Architektur</p></td>
<td align="left"><p>Architektur</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ProductName</p></td>
<td align="left"><p>Zeichenfolge</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>FileDescription</p></td>
<td align="left"><p>Zeichenfolge</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ProductVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>File Version</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>False</p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a>**Prozesse** Der Datentyp "Prozesse" stellt einen Container für eine Sammlung von einem oder mehreren Process-Elementen dar. Im Sequence-Typ Prozesse werden zwei untergeordnete Elemente unterstützt: **Process** und **ShellProcess**. Process ist ein Element vom Typ Process, und ShellProcess ist vom Datentyp leer. Es muss mindestens ein Element in der Sequenz identifiziert werden.

<a href="" id="path"></a>**Path** Path wird von RegistrySetting und filesetting verwendet, um auf Registrierungs-und Dateipfade zu verweisen. Dieses Element unterstützt zwei optionale Attribute: **rekursiv** und **DeleteIfNotFound**. Beide Werte sind auf Default = "false" festgelegt.

Rekursiv gibt an, dass der Pfad und alle Unterordner für Datei Einstellungen enthalten sind oder dass alle untergeordneten Registrierungsschlüssel für Registrierungseinstellungen enthalten sind. In beiden Fällen sind alle Elemente auf der aktuellen Ebene in den erfassten Daten enthalten. Bei einem filesettings-Objekt sind alle Dateien innerhalb des angegebenen Ordners in den von UE-V erfassten Daten enthalten, aber Ordner sind nicht enthalten. Bei Registrierungspfaden werden alle Werte im aktuellen Pfad erfasst, aber die untergeordneten Registrierungsschlüssel werden nicht erfasst. In beiden Fällen sollte darauf geachtet werden, große Datenmengen oder eine große Anzahl von Elementen nicht zu erfassen.

Das DeleteIfNotFound-Attribut entfernt die Einstellungen aus den Speicherpfad Daten des Benutzers. Dies kann in den Fällen wünschenswert sein, in denen durch das Entfernen dieser Einstellungen aus dem Paket eine große Menge an Speicherplatz auf dem Dateiserver für Settings Storage Path gespart wird.

<a href="" id="filemask"></a>**Filemask** Filemask gibt nur bestimmte Dateitypen für den Ordner an, der durch path definiert ist. Path könnte beispielsweise sein, `C:\users\username\files` und die Dateimaske kann `*.txt` nur Textdateien enthalten.

<a href="" id="registrysetting"></a>**RegistrySetting** RegistrySetting stellt einen Container für Registrierungsschlüssel und-Werte und das zugeordnete gewünschte Verhalten auf Seiten des UE-V-Agents dar. In diesem Typ werden vier untergeordnete Elemente definiert: **path**, **Name**, **Exclude**und eine Sequenz des Werte **Pfads** und- **namens**.

<a href="" id="filesetting"></a>**Filesetting** Filesetting enthält Parameter, die mit Dateien und Dateipfaden verknüpft sind. Es werden vier untergeordnete Elemente definiert: **root**, **path**, **filemask**und **Exclude**. Root ist obligatorisch und die anderen sind optional.

<a href="" id="settings"></a>**Einstellungen** Einstellungen ist ein Container für alle Einstellungen, die für eine bestimmte Vorlage gelten. Sie enthält Instanzen der zuvor beschriebenen Registrierungs-, Datei-, Systemparameter-und benutzerdefinierten Einstellungen. Darüber hinaus kann Sie auch die folgenden untergeordneten Elemente mit den beschriebenen Verhaltensweisen enthalten:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Element</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Asynchrone</p></td>
<td align="left"><p>Asynchrone Einstellungs Pakete werden angewendet, ohne den Anwendungsstart zu blockieren, damit der Anwendungsstart fortgesetzt wird, während die Einstellungen noch angewendet werden. Dies ist nützlich für Einstellungen, die asynchron angewendet werden können, beispielsweise <code>get/set</code> über eine API, wie SystemParameterSetting.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PreventOverlappingSynchronization</p></td>
<td align="left"><p>Standardmäßig werden in UE-V nur Einstellungen für eine Anwendung gespeichert, wenn die letzte Instanz einer Anwendung, die die Vorlage verwendet, geschlossen ist. Wenn dieses Element auf "false" festgelegt ist, exportiert UE-V die Einstellungen selbst dann, wenn andere Instanzen einer Anwendung ausgeführt werden. Geeignete Vorlagen – diejenigen, die einen allgemeinen Element Abschnitt enthalten –, die mit UE-V ausgeliefert werden, verwenden dieses Flag, um freigegebene Einstellungen so zu aktivieren, dass Sie immer beim Schließen der Anwendung exportiert werden, während anwendungsspezifische Einstellungen vor dem Export verhindert werden, bis die letzte Instanz geschlossen ist.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name"></a>Name-Element

**Obligatorisch: wahr**

**Typ: Zeichenfolge**

Name gibt einen eindeutigen Namen für die Einstellungs Speicherort Vorlage an. Diese Funktion wird für Anzeigezwecke verwendet, wenn Sie in WMI, PowerShell, Ereignisanzeige und Debug-Protokollen auf die Vorlage verweisen. Im Allgemeinen sollten Sie nicht auf Versionsinformationen verweisen, da dies vom ProductVersion-Element abweichen kann. Geben Sie beispielsweise `<Name>My Application</Name>` anstelle ein `<Name>My Application 1.1</Name>` .

**Hinweis**  UE-V verweist nicht auf externe DTDs, daher ist es nicht möglich, benannte Entitäten in einer Einstellungen-Speicherort Vorlage zu verwenden. Verwenden Sie beispielsweise nicht, &reg; um auf das eingetragene Markenzeichen® zu verweisen. Verwenden Sie stattdessen kanonische nummerierte Bezüge, um diese Typen von Sonderzeichen einzubeziehen, beispielsweise & \ #174 für das® Zeichen. Diese Regel gilt für alle Zeichenfolgenwerte in diesem Dokument.

<http://www.w3.org/TR/xhtml1/dtds.html>Eine vollständige Liste der Zeichenentitäten finden Sie unter. UTF-8-codierte Dokumente enthalten möglicherweise die Unicode-Zeichen direkt. Beim Speichern von Vorlagen über den UE-V-Generator werden Zeichenentitäten automatisch in ihre Unicode-Darstellungen konvertiert.

 

### <a href="" id="id"></a>ID-Element

**Obligatorisch: wahr**

**Typ: Zeichenfolge**

ID füllt einen eindeutigen Bezeichner für eine bestimmte Vorlage auf. Dieses Tag wird zur primären Kennung, mit der der UE-V-Agent zur Laufzeit auf die Vorlage verweist (Beispiel: Anzeigen der Ausgabe der PowerShell-Cmdlets "Get-UevTemplate" und "Get-UevTemplateProgram"). Nach Konvention sollte dieses Tag keine Leerzeichen enthalten, was das Skripting vereinfacht. In diesem Element sollten Versionsnummern von Anwendungen angegeben werden, um eine einfache Identifizierung der Vorlage zu ermöglichen, beispielsweise `<ID>MicrosoftCalculator6</ID>` oder `<ID>MicrosoftOffice2010Win64</ID>` .

### <a href="" id="version"></a>Version-Element

**Obligatorisch: wahr**

**Typ: Ganzzahl**

**Minimaler Wert: 0**

**Maximaler Wert: 2147483647**

Version identifiziert die Version der Vorlage für die Einstellungsposition für die administrative Nachverfolgung von Änderungen. Der UE-V-Generator erhöht diese Zahl automatisch um eins, wenn die Vorlage gespeichert wird. Beachten Sie, dass dieses Feld eine ganze Zahl Ganzzahl sein muss. Gebrochene Werte, beispielsweise `<Version>2.5</Version>` sind nicht zulässig.

**Hinweis:** Sie können Notizen zu Versionsänderungen mithilfe von XML-Kommentar Tags speichern `<!-- -->` , beispielsweise:

```xml
<!--
    Version History

    Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
    Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
    Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
    Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
  -->
<Version>4</Version>
```

**Wichtig**  Dieser Wert wird abgefragt, um zu ermitteln, ob eine neue Version einer Vorlage in diesen Fällen auf eine vorhandene Vorlage angewendet werden soll:

-   Wenn der automatische Aktualisierungsvorgang der geplanten Vorlage ausgeführt wird

-   Wenn das PowerShell-Cmdlet "Update-UevTemplate" ausgeführt wird

-   Wenn die microsoft\\uev: SettingsLocationTemplate-Update Methode über WMI aufgerufen wird

 

### <a href="" id="author"></a>Author-Element

**Obligatorisch: falsch**

**Typ: Zeichenfolge**

Autor identifiziert den Ersteller der Vorlage für die Einstellungsposition. Zwei optionale untergeordnete Elemente werden unterstützt: **Name** und **e-Mail**. Beide Attribute sind optional, aber wenn das untergeordnete e-Mail-Element angegeben ist, muss es vom Name-Element begleitet werden. Der Autor bezieht sich auf den vollständigen Namen des Kontakts für die Vorlage "Settings Location", und e-Mail sollte auf eine e-Mail-Adresse für den Autor verweisen. Wir empfehlen, dass Sie diese Informationen in öffentlich veröffentlichte Vorlagen einbeziehen, beispielsweise im [Vorlagenkatalog UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).

### <a href="" id="processes"></a>Prozesse und Prozess Element

**Obligatorisch: wahr**

**Typ: Element**

Prozesse enthält mindestens ein `<Process>` Element, das wiederum die folgenden untergeordneten Elemente enthält: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**und **fileversion**. Das untergeordnete FileName-Element ist obligatorisch, die anderen sind optional. Ein vollständig aufgefülltes Element enthält Tags ähnlich wie in diesem Beispiel:

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### Dateiname

**Obligatorisch: wahr**

**Typ: Zeichenfolge**

Filename bezieht sich auf den tatsächlichen Dateinamen der ausführbaren Datei, wie Sie im Dateisystem angezeigt wird. Dieses Element gibt das primäre Kriterium an, mit dem UE-V auswerten soll, ob eine Vorlage für einen Prozess gilt oder nicht. Dieses Element muss in der XML-Vorlage für die Einstellungsposition angegeben werden.

Gültige Dateinamen dürfen nicht mit dem regulären Ausdruck \ [^ \ \ \ \ \ \? \ \ \ * \ \ | &lt; &gt; /: \] +, das heißt, Sie dürfen keine umgekehrten Schrägstriche, Sternchen-oder Fragezeichen-Wildcards, das Pipe-Zeichen, das größer-als-oder kleiner-als-Zeichen, den Schrägstrich oder den Doppelpunkt enthalten (\ \? \* | &lt; &gt; /oder: Zeichen.).

**Hinweis:** Um eine Zeichenfolge für diesen Regex zu testen, verwenden Sie ein PowerShell-Befehlsfenster, und ersetzen Sie den Namen der ausführbaren Datei für **YourFileName**:

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

Der Wert **true** gibt an, dass die Zeichenfolge ungültige Zeichen enthält. Im folgenden finden Sie einige Beispiele für ungültige Werte:

-   \\\\server\\share\\program.exe

-   Programm \ *. exe

-   Pro? ram.exe

-   Programm &lt; 1 &gt; . exe

**Hinweis**  Der UE-V-Generator codiert das größer-als-und das kleiner-als-Zeichen &gt; &lt; .

 

In seltenen Fällen enthält der FileName-Wert nicht unbedingt die Erweiterung ". exe", sollte aber als Teil des Werts angegeben werden. Beispielsweise `<Filename>MyApplictication.exe</Filename>` sollte angegeben werden, anstatt `<Filename>MyApplictication</Filename>` . Im zweiten Beispiel wird die Vorlage nicht auf den Prozess angewendet, wenn der tatsächliche Name der ausführbaren Datei "MyApplication.exe" lautet.

### Architektur

**Obligatorisch: falsch**

**Typ: Architektur (Zeichenfolge)**

Architektur bezieht sich auf die Prozessorarchitektur, für die die ausführbare Ziel Datei kompiliert wurde. Gültige Werte sind Win32 für 32-Bit-Anwendungen oder win64 für 64-Bit-Anwendungen. Sofern vorhanden, schränkt dieses Tag die Anwendbarkeit der Vorlage "Settings Location" auf eine bestimmte Anwendungsarchitektur ein. Ein Beispiel hierfür finden Sie unter Vergleich der%programfiles%\\Microsoft-Benutzeroberflächen-Virtualization\\templates\\ MicrosoftOffice2010Win32.xml und MicrosoftOffice2010Win64.xml Dateien, die in UE-V enthalten sind. Dies ist hilfreich, wenn relative Pfade zwischen unterschiedlichen Versionen einer ausführbaren Datei geändert werden oder wenn Einstellungen hinzugefügt oder entfernt wurden, wenn Sie von einer Prozessorarchitektur zu einer anderen wechseln.

Wenn dieses Element nicht vorhanden ist, ignoriert die Vorlage "Einstellungen" die Architektur des Prozesses und bezieht sich auf 32-und 64-Bit-Prozesse, wenn der Dateiname und andere Attribute angewendet werden.

**Hinweis**  UE-V unterstützt keine ARM-Prozessoren in dieser Version.

 

### ProductName

**Obligatorisch: falsch**

**Typ: Zeichenfolge**

ProductName ist ein optionales Element, das verwendet wird, um ein Produkt für administrative Zwecke oder Berichte zu identifizieren. ProductName unterscheidet sich von filename dadurch, dass für seinen Wert keine regulären Ausdruckseinschränkungen gelten. Auf diese Weise können Beschreibungen eines Prozesses leichter verstanden werden, bei denen der Name der ausführbaren Datei möglicherweise nicht offensichtlich ist. Beispiel:

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### FileDescription

**Obligatorisch: falsch**

**Typ: Zeichenfolge**

FileDescription ist ein optionales Tag, das eine administrative Beschreibung der ausführbaren Datei ermöglicht. Hierbei handelt es sich um ein kostenloses Textfeld, das bei der Unterscheidung mehrerer ausführbarer Dateien innerhalb eines Softwarepakets hilfreich sein kann, wenn die Funktion der ausführbaren Datei identifiziert werden muss.

In einer geeigneten Anwendung kann es beispielsweise hilfreich sein, die Funktion von zwei ausführbaren Dateien (MyApplication.exe und MyApplicationHelper.exe) zu informieren, wie hier gezeigt:

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### ProductVersion

**Obligatorisch: falsch**

**Typ: Zeichenfolge**

ProductVersion bezieht sich auf die Haupt-und Nebenversionen einer Datei sowie auf eine Build-und Patchebene. ProductVersion ist ein optionales Element, aber wenn angegeben, muss es mindestens das wichtigste untergeordnete Element enthalten. Der Wert muss einen Bereich in der Form mindestens = "x" Maximum = "y" ausdrücken, wobei X und Y ganze Zahlen sind. Die Mindest-und Höchstwerte können identisch sein.

Die Elemente "Produkt" und "Dateiversion" werden möglicherweise nicht angegeben. Dadurch wird die Vorlage "versionsunabhängig", was bedeutet, dass die Vorlage auf alle Versionen der angegebenen ausführbaren Datei angewendet wird.

**Beispiel 1:**

Produktversion: 1,0, die im UE-V-Generator angegeben wird, erzeugt den folgenden XML-Code:

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**Beispiel 2:**

Dateiversion: im UE-V-Generator angegebene 5.0.2.1000 erzeugt den folgenden XML-Code:

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**Falsches Beispiel 1 – unvollständiger Bereich:**

Es ist nur das kleinste Attribut vorhanden. Maximum muss auch in einem Bereich enthalten sein.

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**Falsches Beispiel 2 – Moll ohne Hauptelement angegeben:**

Nur das nebengeordnete Element ist vorhanden. Major muss ebenfalls enthalten sein.

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### File Version

**Obligatorisch: falsch**

**Typ: Zeichenfolge**

Fileversion unterscheidet zwischen der Veröffentlichungsversion einer veröffentlichten Anwendung und den internen Builddaten einer ausführbaren Komponente. Bei den meisten kommerziellen Anwendungen sind diese Nummern identisch. Wenn Sie unterschiedlich sind, gibt die Produktversion einer Datei eine generische Versionskennung einer Datei an, während die Dateiversion einen bestimmten Build einer Datei angibt (wie im Fall eines Hotfix oder Updates). Dadurch werden Dateien eindeutig identifiziert, ohne die Erkennungslogik zu unterbrechen.

Wenn Sie die Produktversion und die Dateiversion einer bestimmten ausführbaren Datei ermitteln möchten, klicken Sie mit der rechten Maustaste auf die Datei in Windows-Explorer, wählen Sie Eigenschaften aus, und klicken Sie dann auf die Registerkarte Details.

Das Einfügen eines fileversion-Elements für eine Anwendung ermöglicht eine genauere Feintuning-Erkennungslogik, ist für die meisten Anwendungen jedoch nicht erforderlich. Die ProductVersion-Elementeinstellungen werden zuerst überprüft, und dann wird die Dateiversion aktiviert. Die restriktivere Einstellung wird angewendet.

Die untergeordneten Elemente und Syntaxregeln für fileversion sind mit denen von ProductVersion identisch.

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application"></a>Application-Element

Application ist ein Container für Einstellungen, die für eine bestimmte Anwendung gelten. Es handelt sich um eine Sammlung der folgenden Felder/Typen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Feld/Typ</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Name</p></td>
<td align="left"><p>Gibt einen eindeutigen Namen für die Vorlage "Settings Location" an. Diese Funktion wird für Anzeigezwecke verwendet, wenn Sie in WMI, PowerShell, Ereignisanzeige und Debug-Protokollen auf die Vorlage verweisen. Weitere Informationen finden Sie unter <a href="#name" data-raw-source="[Name](#name)"> Name </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>ID</p></td>
<td align="left"><p>Füllt einen eindeutigen Bezeichner für eine bestimmte Vorlage auf. Dieses Tag wird zur primären Kennung, mit der der UE-V-Agent zur Laufzeit auf die Vorlage verweist. Weitere Informationen finden Sie unter <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Beschreibung</p></td>
<td align="left"><p>Eine optionale Beschreibung der Vorlage.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Ein optionaler Name, der auf der Benutzeroberfläche angezeigt wird und von einem Gebietsschema der Sprache lokalisiert wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Eine optionale Vorlagenbeschreibung, die von einem Sprachgebietsschema lokalisiert wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Version</p></td>
<td align="left"><p>Identifiziert die Version der Vorlage für die Einstellungsposition für die administrative Nachverfolgung von Änderungen. Weitere Informationen finden Sie unter <a href="#version" data-raw-source="[Version](#version)"> Version </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Steuert, ob diese Vorlage in Verbindung mit einem Microsoft-Konto aktiviert ist oder nicht. Wenn die Synchronisierung von MSA für einen Benutzer auf einem Computer aktiviert ist, wird diese Vorlage automatisch deaktiviert.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>Ähnlich wie MSA steuert dies, ob diese Vorlage in Verbindung mit Office365 aktiviert ist. Wenn Office 365 zum Synchronisieren von Einstellungen verwendet wird, wird diese Vorlage automatisch deaktiviert.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Prozesse</p></td>
<td align="left"><p>Ein Container für eine Sammlung von einem oder mehreren Process-Elementen. Weitere Informationen finden Sie unter <a href="#processes" data-raw-source="[Processes](#processes)"> Prozesse </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Einstellungen</p></td>
<td align="left"><p>Ein Container für alle Einstellungen, die für eine bestimmte Vorlage gelten. Sie enthält Instanzen der Registrierungs-, Datei-, Systemparameter-und benutzerdefinierten Einstellungen. Weitere Informationen finden Sie unter <strong> Einstellungen </strong> in <a href="#data" data-raw-source="[Data types](#data)"> Datentypen </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common"></a>Common-Element

Common ist mit einem Application-Element vergleichbar, wird aber immer mit zwei oder mehr Anwendungselementen verknüpft. Der allgemeine Abschnitt stellt den Satz von Einstellungen dar, die zwischen diesen Anwendungsinstanzen freigegeben werden. Es handelt sich um eine Sammlung der folgenden Felder/Typen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Feld/Typ</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Name</p></td>
<td align="left"><p>Gibt einen eindeutigen Namen für die Vorlage "Settings Location" an. Diese Funktion wird für Anzeigezwecke verwendet, wenn Sie in WMI, PowerShell, Ereignisanzeige und Debug-Protokollen auf die Vorlage verweisen. Weitere Informationen finden Sie unter <a href="#name" data-raw-source="[Name](#name)"> Name </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>ID</p></td>
<td align="left"><p>Füllt einen eindeutigen Bezeichner für eine bestimmte Vorlage auf. Dieses Tag wird zur primären Kennung, mit der der UE-V-Agent zur Laufzeit auf die Vorlage verweist. Weitere Informationen finden Sie unter <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Beschreibung</p></td>
<td align="left"><p>Eine optionale Beschreibung der Vorlage.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Ein optionaler Name, der auf der Benutzeroberfläche angezeigt wird und von einem Gebietsschema der Sprache lokalisiert wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Eine optionale Vorlagenbeschreibung, die von einem Sprachgebietsschema lokalisiert wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Version</p></td>
<td align="left"><p>Identifiziert die Version der Vorlage für die Einstellungsposition für die administrative Nachverfolgung von Änderungen. Weitere Informationen finden Sie unter <a href="#version" data-raw-source="[Version](#version)"> Version </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Steuert, ob diese Vorlage in Verbindung mit einem Microsoft-Konto aktiviert ist oder nicht. Wenn die Synchronisierung von MSA für einen Benutzer auf einem Computer aktiviert ist, wird diese Vorlage automatisch deaktiviert.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>Ähnlich wie MSA steuert dies, ob diese Vorlage in Verbindung mit Office365 aktiviert ist. Wenn Office 365 zum Synchronisieren von Einstellungen verwendet wird, wird diese Vorlage automatisch deaktiviert.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Einstellungen</p></td>
<td align="left"><p>Ein Container für alle Einstellungen, die für eine bestimmte Vorlage gelten. Sie enthält Instanzen der Registrierungs-, Datei-, Systemparameter-und benutzerdefinierten Einstellungen. Weitere Informationen finden Sie unter <strong> Einstellungen </strong> in <a href="#data" data-raw-source="[Data types](#data)"> Datentypen </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate"></a>SettingsLocationTemplate-Element

Dieses Element definiert die Einstellungen für eine einzelne Anwendung oder eine Suite von Anwendungen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Feld/Typ</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Name</p></td>
<td align="left"><p>Gibt einen eindeutigen Namen für die Vorlage "Settings Location" an. Diese Funktion wird für Anzeigezwecke verwendet, wenn Sie in WMI, PowerShell, Ereignisanzeige und Debug-Protokollen auf die Vorlage verweisen. Weitere Informationen finden Sie unter <a href="#name" data-raw-source="[Name](#name)"> Name </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>ID</p></td>
<td align="left"><p>Füllt einen eindeutigen Bezeichner für eine bestimmte Vorlage auf. Dieses Tag wird zur primären Kennung, mit der der UE-V-Agent zur Laufzeit auf die Vorlage verweist. Weitere Informationen finden Sie unter <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Beschreibung</p></td>
<td align="left"><p>Eine optionale Beschreibung der Vorlage.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Ein optionaler Name, der auf der Benutzeroberfläche angezeigt wird und von einem Gebietsschema der Sprache lokalisiert wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Eine optionale Vorlagenbeschreibung, die von einem Sprachgebietsschema lokalisiert wurde.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix"></a>Anhang: SettingsLocationTemplate. xsd

Hier sehen Sie die SettingsLocationTemplate. xsd-Datei mit den Elementen, untergeordneten Elementen, Attributen und Parametern:

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="Guid">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="FilenameString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="IDString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="TemplateVersion">
    <xs:restriction base="xs:integer">
      <xs:minInclusive value="0" />
      <xs:maxInclusive value="2147483647" />
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Empty">
    <xs:sequence/>
  </xs:complexType>

  <xs:complexType name="LocalizedString">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Locale" type="xs:string" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="LocalizedName">
    <xs:sequence>
      <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="LocalizedDescription">
    <xs:sequence>
      <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Author">
    <xs:all>
      <xs:element name="Name" type="xs:string" minOccurs="1" />
      <xs:element name="Email" type="xs:string" minOccurs="0" />
    </xs:all>
  </xs:complexType>

  <xs:complexType name="Range">
    <xs:attribute name="Minimum" type="xs:integer" use="required"/>
    <xs:attribute name="Maximum" type="xs:integer" use="required"/>
  </xs:complexType>

  <xs:complexType name="ProcessVersion">
    <xs:sequence>
      <xs:element name="Major" type="Range" minOccurs="1" />
      <xs:element name="Minor" type="Range" minOccurs="0" />
      <xs:element name="Build" type="Range" minOccurs="0" />
      <xs:element name="Patch" type="Range" minOccurs="0" />
    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="Architecture">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Win32"/>
      <xs:enumeration value="Win64"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Process">
    <xs:sequence>
      <xs:element name="Filename" type="FilenameString" minOccurs="1" />
      <xs:element name="Architecture" type="Architecture" minOccurs="0" />
      <xs:element name="ProductName" type="xs:string" minOccurs="0" />
      <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
      <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
      <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Processes">
    <xs:sequence>
      <xs:choice minOccurs="1">
        <xs:element name="Process" type="Process" />
        <xs:element name="ShellProcess" type="Empty" />
      </xs:choice>
      <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Path">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
        <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="RegistrySetting">
    <xs:sequence>
      <xs:element name="Path" type="Path" />
      <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="FileSetting">
    <xs:sequence>

      <xs:element name="Root">
        <xs:complexType>
          <xs:choice>
            <xs:element name="KnownFolder" type="Guid" />
            <xs:element name="RegistryEntry" type="xs:string" />
            <xs:element name="EnvironmentVariable" type="xs:string" />
          </xs:choice>
        </xs:complexType>
      </xs:element>

      <xs:element name="Path" minOccurs="0" type="Path" />
      <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>

    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="SystemParameterSetting">
    <xs:restriction base="xs:string">

      <!-- Accessibility parameters -->
      <xs:enumeration value="AccessTimeout"/>
      <xs:enumeration value="AudioDescription"/>
      <xs:enumeration value="ClientAreaAnimation"/>
      <xs:enumeration value="DisableOverlappedContent"/>
      <xs:enumeration value="FilterKeys"/>
      <xs:enumeration value="FocusBorderHeight"/>
      <xs:enumeration value="FocusBorderWidth"/>
      <xs:enumeration value="HighContrast"/>
      <xs:enumeration value="MessageDuration"/>
      <xs:enumeration value="MouseClickLock"/>
      <xs:enumeration value="MouseClickLockTime"/>
      <xs:enumeration value="MouseKeys"/>
      <xs:enumeration value="MouseSonar"/>
      <xs:enumeration value="MouseVanish"/>
      <xs:enumeration value="ScreenReader"/>
      <xs:enumeration value="ShowSounds"/>
      <xs:enumeration value="SoundSentry"/>
      <xs:enumeration value="StickyKeys"/>
      <xs:enumeration value="ToggleKeys"/>

      <!-- Input parameters -->
      <xs:enumeration value="Beep"/>
      <xs:enumeration value="BlockSendInputResets"/>
      <xs:enumeration value="DefaultInputLang"/>
      <xs:enumeration value="DoubleClickTime"/>
      <xs:enumeration value="DoubleClkHeight"/>
      <xs:enumeration value="DoubleClkWidth"/>
      <xs:enumeration value="KeyboardCues"/>
      <xs:enumeration value="KeyboardDelay"/>
      <xs:enumeration value="KeyboardPref"/>
      <xs:enumeration value="KeyboardSpeed"/>
      <xs:enumeration value="Mouse"/>
      <xs:enumeration value="MouseButtonSwap"/>
      <xs:enumeration value="MouseHoverHeight"/>
      <xs:enumeration value="MouseHoverTime"/>
      <xs:enumeration value="MouseHoverWidth"/>
      <xs:enumeration value="MouseSpeed"/>
      <xs:enumeration value="MouseTrails"/>
      <xs:enumeration value="SnapToDefButton"/>
      <xs:enumeration value="WheelScrollChars"/>
      <xs:enumeration value="WheelScrollLines"/>

      <!-- Desktop parameters (limited subset) -->
      <xs:enumeration value="DeskWallpaper"/>
      <xs:enumeration value="DesktopColor"/>

    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Settings">
    <xs:sequence>
      <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
      <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Registry" type="RegistrySetting" />
        <xs:element name="File" type="FileSetting" />
        <xs:element name="SystemParameter" type="SystemParameterSetting" />
      </xs:choice>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Common">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Application">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Processes" type="Processes" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>


  <xs:element name="SettingsLocationTemplate">
    <xs:complexType>
      <xs:sequence>

        <xs:element name="Name" type="xs:string" />
        <xs:element name="ID" type="IDString" />
        <xs:element name="Description" type="xs:string" minOccurs="0" />
        <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
        <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

        <xs:choice>

          <!-- Single application -->
          <xs:sequence>
            <xs:element name="Version" type="TemplateVersion" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
          </xs:sequence>

          <!-- Suite of applications -->
          <xs:sequence>
            <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="Common" type="Common" />
            <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
          </xs:sequence>

        </xs:choice>

      </xs:sequence>
    </xs:complexType>
  </xs:element>
  <!-- SettingsLocationTemplate -->

</xs:schema>
```






## Verwandte Themen


[Arbeiten mit benutzerdefinierten UE-v 2. x-Vorlagen und dem UE-v 2. x-Generator](working-with-custom-ue-v-2x-templates-and-the-ue-v-2x-generator-new-uevv2.md)

[Technische Referenz für UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





