---
title: Über die Verbindungsgruppendatei
description: Über die Verbindungsgruppendatei
author: dansimp
ms.assetid: 1f4df515-f5f6-4b58-91a8-c71598cb3ea4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31ef9dc9c4465ed8f261b73518348c05ceb78d15
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806095"
---
# Über die Verbindungsgruppendatei


**In diesem Thema:**

-   [Zweck und Speicherort der Verbindungsgruppen Datei](#bkmk-cg-purpose-loc)

-   [Struktur der XML-Datei der Verbindungsgruppe](#bkmk-define-cg-5-0sp3)

-   [Konfigurieren der Priorität von Paketen in einer Verbindungsgruppe](#bkmk-config-pkg-priority-incg)

-   [Unterstützte Verbindungskonfigurationen für virtuelle Anwendungen](#bkmk-va-conn-configs)

## <a href="" id="bkmk-cg-purpose-loc"></a>Zweck und Speicherort der Verbindungsgruppen Datei


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Zweck der Verbindungsgruppe</p></td>
<td align="left"><p>Eine Verbindungsgruppe ist ein App-V-Feature, mit dem Sie Pakete zusammen gruppieren können, um eine virtuelle Umgebung zu erstellen, in der die Anwendungen in diesen Paketen miteinander interagieren können.</p>
<p>Beispiel: Sie möchten Plug-ins mit Microsoft Office verwenden. Sie können ein Paket erstellen, das die Plug-Ins enthält, ein weiteres Paket erstellen, das Office enthält, und dann beide Pakete zu einer Verbindungsgruppe hinzufügen, um Office die Verwendung dieser Plug-ins zu ermöglichen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Funktionsweise der Verbindungsgruppen Datei</p></td>
<td align="left"><p>Wenn Sie eine App-V 5,1-Verbindungsgruppen Datei anwenden, werden die in der Datei aufgelisteten Pakete zur Laufzeit in einer einzelnen virtuellen Umgebung kombiniert. Verwenden Sie die Microsoft Application Virtualization (app-v) 5,1-Verbindungsgruppen Datei, um vorhandene App-v 5,1-Verbindungsgruppen zu konfigurieren.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Beispiel Dateipfad</p></td>
<td align="left"><p>%APPDATA%\Microsoft\AppV\Client\Catalog\PackageGroups {6CCC7575-162E-4152-9407-ED411DA138F4} {4D1E16E1-8EF8-41ED-92D5-8910A8527F96}.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-define-cg-5-0sp3"></a>Struktur der XML-Datei der Verbindungsgruppe


**In diesem Abschnitt:**

-   [Parameter, die die Verbindungsgruppe definieren](#bkmk-params-define-cg)

-   [Parameter, die die Pakete in der Verbindungsgruppe definieren](#bkmk-params-define-pkgs-incg)

-   [App-V-Beispiel für eine Verbindungsgruppen-XML-Datei](#bkmk-50sp3-exp-cg-xml)

-   [App-v 5,0 durch APP-v 5,0 SP2-Beispiel einer Verbindungsgruppen-XML-Datei](#bkmk-50thru50sp2-exp-cg-xm)

### <a href="" id="bkmk-params-define-cg"></a>Parameter, die die Verbindungsgruppe definieren

In der folgenden Tabelle werden die Parameter in der XML-Datei beschrieben, die die Verbindungsgruppe selbst und nicht die Pakete definieren.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Feld</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Schemaname</p></td>
<td align="left"><p>Der Name des Schemas.</p>
<p><strong>Anwendbar ab App-V 5,0 SP3 </strong> : Wenn Sie die neuen Features "optionale Pakete" und "Verwenden einer beliebigen Version" verwenden möchten, die in dieser Tabelle beschrieben werden, müssen Sie das folgende Schema in der XML-Datei angeben:</p>
<p><code>xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>AppConnectionGroupId</p></td>
<td align="left"><p>Eindeutiger GUID-Bezeichner für diese Verbindungsgruppe. Der Verbindungsgruppen Status ist diesem Bezeichner zugeordnet. Geben Sie diesen Bezeichner nur an, wenn Sie die Verbindungsgruppe erstellen.</p>
<p>Sie können eine neue GUID erstellen, indem Sie Folgendes <strong>[Guid]::NewGuid()</strong> eingeben:</p></td>
</tr>
<tr class="odd">
<td align="left"><p>VersionID</p></td>
<td align="left"><p>Versions-GUID-Bezeichner für diese Version der Verbindungsgruppe.</p>
<p>Beim Aktualisieren einer Verbindungsgruppe (beispielsweisedurch hinzufügen oder Aktualisieren eines neuen Pakets) müssen Sie die Versions-GUID so aktualisieren, dass Sie der neuen Version entspricht.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DisplayName</p></td>
<td align="left"><p>Anzeigename der Verbindungsgruppe.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Priorität</p></td>
<td align="left"><p>Optionales Prioritätsfeld für die Verbindungsgruppe.</p>
<p><strong>"0" </strong> - gibt die höchste Priorität an.</p>
<p>Wenn eine Priorität erforderlich ist, aber nicht konfiguriert wurde, schlägt das Paket fehl, da die richtige zu verwendende Verbindungsgruppe nicht ermittelt werden kann.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-params-define-pkgs-incg"></a>Parameter, die die Pakete in der Verbindungsgruppe definieren

Im &lt; Abschnitt Pakete &gt; der XML-Datei der Verbindungsgruppe Listen Sie die Mitglieder Pakete in der Verbindungsgruppe auf, indem Sie die einzelnen Paket Bezeichner und die Versionskennung angeben, wie in der folgenden Tabelle beschrieben. Das erste Paket in der Liste hat die höchste Priorität.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Feld</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>PackageId</p></td>
<td align="left"><p>Eindeutiger GUID-Bezeichner für dieses Paket. Diese GUID ändert sich nicht, wenn neuere Versionen des Pakets veröffentlicht werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>VersionID</p></td>
<td align="left"><p>Eindeutiger GUID-Bezeichner für die Version des Pakets.</p>
<p><strong>Anwendbar ab App-V 5,0 SP3 </strong> : Wenn Sie <strong> </strong> für die Paketversion "*" angeben, wird die GUID der neuesten verfügbaren Paketversion dynamisch eingefügt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>IsOptional</p></td>
<td align="left"><p><strong>Anwendbar ab App-V 5,0 SP3 </strong> : Parameter, mit dem Sie ein Paket in der Verbindungsgruppe optional erstellen können. Gültige Einträge sind:</p>
<ul>
<li><p><strong>"wahr" </strong> – das Paket ist in der Verbindungsgruppe optional</p></li>
<li><p><strong>"falsch" </strong> – das Paket ist in der Verbindungsgruppe erforderlich.</p></li>
</ul>
<p>Weitere Informationen finden Sie unter <a href="how-to-use-optional-packages-in-connection-groups51.md" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups51.md)"> Verwenden optionaler Pakete in Verbindungsgruppen </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-50sp3-exp-cg-xml"></a>App-V-Beispiel für eine Verbindungsgruppen-XML-Datei

Die folgende XML-Beispieldatei der Verbindungsgruppe zeigt Beispiele für die Felder in den vorherigen Tabellen und hebt die Elemente hervor, die neu ab App-V 5,0 SP3 sind.

```XML
<?xml version="1.0" encoding="UTF-16">
<appv:AppConnectionGroup 
  xmlns="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"
  xmlns:appv="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"  
  AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
  VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"
  Priority="0"  
  DisplayName="Sample Connection Group">
  <appv:Packages>    
    <appv:Package
      PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
      VersionId="*"
      IsOptional="true"    
    />
    <appv:Package
      PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
      VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
      IsOptional="false"    
    />  
  </appv:Packages>
</appv:AppConnectionGroup>
```

### <a href="" id="bkmk-50thru50sp2-exp-cg-xm"></a>App-v 5,0 durch APP-v 5,0 SP2-Beispiel einer Verbindungsgruppen-XML-Datei

Die folgende XML-Beispieldatei für die Verbindungsgruppe bezieht sich auf App-v 5,0 über APP-v 5,0 SP2. Sie zeigt Beispiele für die Felder in der vorherigen Tabelle, schließt aber die oben beschriebenen Änderungen für App-V 5,0 SP3 aus.

```XML
<?xml version="1.0" encoding="UTF-16">
<appv:AppConnectionGroup
  xmlns="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
  xmlns:appv="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
  AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
  VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"
  Priority="0"
  DisplayName="Sample Connection Group">
  <appv:Packages>
    <appv:Package
      PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
      VersionId="C7DF4F63-5288-439C-ACEF-EF06BF401EC5"
    />
    <appv:Package
     PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
     VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
   />
 </appv:Packages>
<appv:AppConnectionGroup>
```

## <a href="" id="bkmk-config-pkg-priority-incg"></a>Konfigurieren der Priorität von Paketen in einer Verbindungsgruppe


Die Paket Rangfolge wird mithilfe der Paket Listenreihenfolge konfiguriert. Das erste Paket im Dokument hat die höchste Priorität. Nachfolgende Pakete in der Liste haben eine absteigende Priorität.

Die Paket Rangfolge ist die Lösung für ansonsten unvermeidliche Ressourcenkonflikte während der Initialisierung der virtuellen Umgebung. Wenn beispielsweise zwei Pakete, die sich in derselben virtuellen Umgebung öffnen, denselben Registrierungs-DWORD-Wert definieren, bestimmt das Paket mit der höchsten Rangfolge den festgelegten Wert.

Sie können die Verbindungsgruppen Datei verwenden, um jede Verbindungsgruppe mithilfe der folgenden Methoden zu konfigurieren:

-   Angeben von Lauf Zeit Prioritäten für Verbindungsgruppen Wenn Sie die Priorität mithilfe der App-V-Verwaltungskonsole bearbeiten möchten, klicken Sie auf die Gruppe Verbindung, und klicken Sie dann auf **Bearbeiten**.

    **Hinweis**  Die Priorität ist nur erforderlich, wenn das Paket mehr als einer Verbindungsgruppe zugeordnet ist.

     

-   Geben Sie die Paket Rangfolge innerhalb der Verbindungsgruppe an.

Das Feld "Priorität" ist erforderlich, wenn eine ausgeführte virtuelle Anwendung aus einer systemeigenen Anwendungsanforderung initiiert wird, beispielsweise Microsoft Windows Explorer. Der App-V-Client verwendet die Priorität, um zu ermitteln, in welcher Verbindungsgruppe die virtuelle Umgebung ausgeführt werden soll. Diese Situation tritt auf, wenn eine virtuelle Anwendung Teil mehrerer Verbindungsgruppen ist.

Wenn eine virtuelle Anwendung mit einer anderen virtuellen Anwendung geöffnet wird, wird die virtuelle Umgebung der ursprünglichen virtuellen Anwendung verwendet. Das Feld "Priorität" wird in diesem Fall nicht verwendet.

**Beispiel:**

Die virtuelle Anwendung Microsoft Outlook wird in der virtuellen Umgebung **XYZ**ausgeführt. Wenn Sie ein angefügtes Microsoft Word-Dokument öffnen, wird in der virtuellen Umgebung **XYZ**eine virtualisierte Version von Microsoft Word geöffnet, unabhängig davon, welche virtuellen Microsoft Word-Verbindungsgruppen oder-Lauf Zeit Prioritäten zugeordnet sind.

## <a href="" id="bkmk-va-conn-configs"></a>Unterstützte Verbindungskonfigurationen für virtuelle Anwendungen


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Konfiguration</th>
<th align="left">Beispielszenarien</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Eine. exe-Datei und-Plug-in (. dll)</p></td>
<td align="left"><ul>
<li><p>Sie möchten Microsoft Office an alle Benutzer verteilen, aber ein Microsoft Excel-Plug-in nur an eine Teilmenge von Benutzern verteilen.</p></li>
<li><p>Aktivieren Sie die Verbindungsgruppe für die entsprechenden Benutzer.</p></li>
<li><p>Aktualisieren Sie jedes Paket einzeln nach Bedarf.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Eine. exe-Datei und eine Middleware-Anwendung</p></td>
<td align="left"><ul>
<li><p>Sie verfügen über eine Anwendung erfordert eine Middleware-Anwendung oder mehrere Anwendungen, die alle von der gleichen Middleware-Laufzeitversion abhängig sind.</p></li>
<li><p>Alle Computer, die eine oder mehrere Anwendungen erfordern, erhalten die Verbindungsgruppen mit der Anwendungs-und Middleware-Laufzeit.</p></li>
<li><p>Optional können Sie mehrere Middleware-Anwendungen in einer einzigen Verbindungsgruppe kombinieren.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Beispiel</th>
<th align="left">Beispiel Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Verknüpfungsgruppe für virtuelle Anwendungen für die Finanzabteilung</p></td>
<td align="left"><ul>
<li><p>Middleware-Anwendung 1</p></li>
<li><p>Middleware-Anwendung 2</p></li>
<li><p>Middleware-Anwendung 3</p></li>
<li><p>Middleware-Anwendungslaufzeit</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Gruppe für virtuelle Anwendungsverbindungen für die Abteilung HR</p></td>
<td align="left"><ul>
<li><p>Middleware-Anwendung 5</p></li>
<li><p>Middleware-Anwendung 6</p></li>
<li><p>Middleware-Anwendungslaufzeit</p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Eine. exe-Datei und eine exe-Datei</p></td>
<td align="left"><p>Sie verfügen über eine Anwendung, die sich auf eine andere Anwendung verlässt, und Sie möchten die Pakete für Betriebseffizienz, Lizenzierungseinschränkungen oder Rollout-Zeitpläne separat aufbewahren.</p>
<p><strong>Beispiel:</strong></p>
<p>Wenn Sie Microsoft lync 2010 bereitstellen, können Sie drei Pakete verwenden:</p>
<ul>
<li><p>Microsoft Office2010</p></li>
<li><p>Microsoft Communicator2007</p></li>
<li><p>Microsoft Lync2010</p></li>
</ul>
<p>Sie können die Bereitstellung mithilfe der folgenden Verbindungsgruppen verwalten:</p>
<ul>
<li><p>Microsoft Office2010 und Microsoft Communicator2007</p></li>
<li><p>Microsoft Office2010 und Microsoft Lync2010</p></li>
</ul>
<p>Wenn die Bereitstellung abgeschlossen ist, können Sie entweder ein einzelnes neues Microsoft Office2010 + Microsoft Lync2010-Paket erstellen oder diese als separate Pakete verwalten und mit einer Verbindungsgruppe bereitstellen.</p></td>
</tr>
</tbody>
</table>

 






## Verwandte Themen


[Verwalten von Verbindungsgruppen](managing-connection-groups51.md)

 

 





