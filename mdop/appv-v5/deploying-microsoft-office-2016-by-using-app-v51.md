---
title: Bereitstellen von Microsoft Office2016 mit App-V
description: Bereitstellen von Microsoft Office2016 mit App-V
author: dansimp
ms.assetid: e0f4876-da99-4b89-977e-2fb6e89ea3d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: b47fd46c8dc368bbce819b24f18fa30328fbbaf0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805855"
---
# Bereitstellen von Microsoft Office2016 mit App-V


Verwenden Sie die Informationen in diesem Artikel, um Microsoft Application Virtualization (App-V) 5,1 oder höhere Versionen zu verwenden, um Microsoft Office 2016 als virtualisierte Anwendung an Computer in Ihrer Organisation zu übermitteln. Informationen zum Verwenden von App-v für die Bereitstellung von Office 2013 finden Sie unter [Bereitstellen von Microsoft Office 2013 mithilfe von App-v](deploying-microsoft-office-2013-by-using-app-v51.md). Informationen zum Verwenden von App-v für die Bereitstellung von Office 2010 finden Sie unter [Bereitstellen von Microsoft Office 2010 mithilfe von App-v](deploying-microsoft-office-2010-by-using-app-v51.md).

Dieses Thema enthält die folgenden Abschnitte:

-   [Was Sie wissen sollten, bevor Sie beginnen](#bkmk-before-you-start)

-   [Erstellen eines Office 2016-Pakets für App-V mit dem Office-Bereitstellungs Tool](#bkmk-create-office-pkg)

-   [Veröffentlichen des Office-Pakets für App-V 5,1](#bkmk-pub-pkg-office)

-   [Anpassen und Verwalten von Office App-V-Paketen](#bkmk-custmz-manage-office-pkgs)

## <a href="" id="bkmk-before-you-start"></a>Was Sie wissen sollten, bevor Sie beginnen


Bevor Sie Office 2016 mithilfe von App-V bereitstellen, sollten Sie die folgenden Planungsinformationen überprüfen.

### <a href="" id="bkmk-supp-vers-coexist"></a>Unterstützte Office-Versionen und Office-Koexistenz

Verwenden Sie die folgende Tabelle, um Informationen zu unterstützten Versionen von Office und zum Ausführen von nebeneinander vorhandenen Versionen von Office zu erhalten.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Zu überprüfende Informationen</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv" data-raw-source="[Supported versions of Microsoft Office](planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv)">Unterstützte Versionen von Microsoft Office</a></p></td>
<td align="left"><ul>
<li><p>Unterstützte Office-Versionen</p></li>
<li><p>Unterstützte Bereitstellungstypen (beispielsweise Desktop, Personal Virtual Desktop Infrastructure (VDI), gebündelter VDI)</p></li>
<li><p>Office-Lizenzierungsoptionen</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-plan-coexisting" data-raw-source="[Planning for Using App-V with coexisting versions of Office](planning-for-using-app-v-with-office.md#bkmk-plan-coexisting)">Planen der Verwendung von App-V mit vorhandenen Office-Versionen</a></p></td>
<td align="left"><p>Überlegungen zum Installieren verschiedener Office-Versionen auf demselben Computer</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pkg-pub-reqs"></a>Anforderungen für das Verpacken, veröffentlichen und bereitstellen

Bevor Sie Office mithilfe von App-V bereitstellen, überprüfen Sie die folgenden Anforderungen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabe</th>
<th align="left">Anforderung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Verpacken</p></td>
<td align="left">
<ul>
<li><p>Alle Office-Anwendungen, die Sie für Benutzer bereitstellen möchten, müssen sich in einem einzigen Paket befinden.</p></li>
<li><p>In App-V 5,1 und höher müssen Sie das Office-Bereitstellungs Tool verwenden, um Pakete zu erstellen. Sie können den Sequencer nicht verwenden.</p></li>
<li><p>Wenn Sie Microsoft Visio 2016 und Microsoft Project 2016 zusammen mit Office bereitstellen, müssen Sie diese in das gleiche Paket mit Office einbeziehen. Weitere Informationen finden Sie unter <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2016 and Project 2016 with Office](#bkmk-deploy-visio-project)"> Bereitstellen von Visio 2016 und Project 2016 mit Office </a> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Publishing</p></td>
<td align="left"><ul>
<li><p>Sie können auf jedem Clientcomputer nur ein Office-Paket veröffentlichen.</p></li>
<li><p>Sie müssen das Office-Paket Global veröffentlichen. Sie können nicht für den Benutzer veröffentlichen.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Bereitstellen eines der folgenden Produkte auf einem freigegebenen Computer, beispielsweise mithilfe von Remote Desktop Diensten:</p>
<ul>
<li><p>Microsoft 365-Apps für Unternehmen</p></li>
<li><p>Visio pro für Office 365</p></li>
<li><p>Project pro für Office 365</p></li>
</ul></td>
<td align="left"><p>Sie müssen die <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)"> Aktivierung gemeinsam genutzter Computer aktivieren </a> .</p>
</td>
</tr>
</tbody>
</table>



### Ausschließen von Office-Anwendungen aus einem Paket

In der folgenden Tabelle werden die empfohlenen Methoden zum Ausschließen bestimmter Office-Anwendungen aus einem Paket beschrieben.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabe</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Verwenden <strong> Sie die ExcludeApp </strong> -Einstellung, wenn Sie das Paket mithilfe des Office-Bereitstellungstools erstellen.</p></td>
<td align="left"><ul>
<li><p>Ermöglicht das Ausschließen bestimmter Office-Anwendungen aus dem Paket, wenn das Office-Bereitstellungs Tool das Paket erstellt. Mit dieser Einstellung können Sie beispielsweise ein Paket erstellen, das nur Microsoft Word enthält.</p></li>
<li><p>Weitere Informationen finden Sie unter <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)"> ExcludeApp-Element </a> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Ändern der DeploymentConfig.xml Datei</p></td>
<td align="left"><ul>
<li><p>Ändern Sie die DeploymentConfig.xml-Datei, nachdem das Paket erstellt wurde. Diese Datei enthält die Standardpaket Einstellungen für alle Benutzer auf einem Computer, auf dem der App-V-Client ausgeführt wird.</p></li>
<li><p>Weitere Informationen finden Sie unter <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2016 applications](#bkmk-disable-office-apps)"> Deaktivieren von Office 2016-Anwendungen </a> .</p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-create-office-pkg"></a>Erstellen eines Office 2016-Pakets für App-V mit dem Office-Bereitstellungs Tool


Führen Sie die folgenden Schritte aus, um ein Office 2016-Paket für App-V 5,1 oder höher zu erstellen.

>**Important** &nbsp; Wichtig &nbsp; In App-V 5,1 und höher müssen Sie das Office-Bereitstellungs Tool verwenden, um ein Paket zu erstellen. Sie können den Sequencer nicht zum Erstellen von Paketen verwenden.

### Überprüfen der Voraussetzungen für die Verwendung des Office-Bereitstellungstools

Der Computer, auf dem Sie das Office-Bereitstellungs Tool installieren, muss Folgendes aufweisen:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Voraussetzung</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Erforderliche Software</p></td>
<td align="left"><p>.NET Framework 4</p></td>
</tr>
<tr class="even">
<td align="left"><p>Unterstützte Betriebssysteme</p></td>
<td align="left"><ul>
<li><p>64-Bit-Version von Windows 10</p></li>
<li><p>64-Bit-Version von Windows 8 oder 8,1</p></li>
<li><p>64-Bit-Version von Windows 7</p></li>
</ul></td>
</tr>
</tbody>
</table>


>**Hinweis**  In diesem Thema bezieht sich der Begriff "Office 2016 App-V-Paket" auf die Abonnementlizenzierung.


### Erstellen von Office 2016-App-V-Paketen mithilfe des Office-Bereitstellungstools

Sie erstellen Office 2016-App-V-Pakete mithilfe des Office-Bereitstellungstools. Die folgenden Anweisungen erläutern, wie Sie ein Office 2016-App-V-Paket mit Abonnementlizenzierung erstellen.

Erstellen Sie Office 2016-App-V-Pakete auf 64-Bit-Windows-Computern. Nach der Erstellung wird das Office 2016-App-V-Paket auf Computern mit 32-Bit und 64-Bit Windows 7, Windows 8,1 und Windows 10 ausgeführt.

### Herunterladen des Office-Bereitstellungstools

Office 2016-App-v-Pakete werden mit dem Office-Bereitstellungs Tool erstellt, das ein Office 2016-App-v-Paket generiert. Das Paket kann nicht über den App-V-Sequenzer erstellt oder geändert werden. So beginnen Sie die Paketerstellung:

1.  Laden [Sie das Office 2016-Bereitstellungs Tool für Klick-und-Los](https://www.microsoft.com/download/details.aspx?id=49117)herunter.

> **Wichtig** Sie müssen das Office 2016-Bereitstellungs Tool verwenden, um Office 2016-App-V-Pakete zu erstellen.
> 2. Führen Sie die exe-Datei aus, und extrahieren Sie die zugehörigen Features an den gewünschten Speicherort. Um diesen Vorgang zu vereinfachen, können Sie einen freigegebenen Netzwerkordner erstellen, in dem die Features gespeichert werden.

    Example: \\\\Server\\Office2016

3. Überprüfen Sie, ob eine setup.exe und eine configuration.xml Datei vorhanden sind und sich an dem von Ihnen angegebenen Speicherort befinden.

### Herunterladen von Office 2016-Anwendungen

Nachdem Sie das Office-Bereitstellungs Tool heruntergeladen haben, können Sie es verwenden, um die neuesten Office 2016-Anwendungen zu erhalten. Nachdem Sie die Office-Anwendungen erhalten haben, erstellen Sie das Office 2016-App-V-Paket.

Die im Office-Bereitstellungs Tool enthaltene XML-Datei gibt die Produkt Details an, beispielsweise die enthaltenen Sprachen und Office-Anwendungen.

1. **Passen Sie die Beispiel-XML-Konfigurationsdatei an:** Verwenden Sie die Beispiel-XML-Konfigurationsdatei, die Sie mit dem Office-Bereitstellungs Tool heruntergeladen haben, um die Office-Anwendungen anzupassen:

   1. Öffnen Sie die XML-Beispieldatei im Editor oder in Ihrem bevorzugten Text-Editor.

   2. Wenn die Beispiel configuration.xml-Datei geöffnet und zur Bearbeitung bereit ist, können Sie Produkte, Sprachen und den Pfad angeben, in dem Sie die Office 2016-Anwendungen speichern. Der folgende Code ist ein einfaches Beispiel für die configuration.xml-Datei:

      ```xml
      <Configuration>
         <Add SourcePath= ”\\Server\Office2016” OfficeClientEdition="32" >
          <Product ID="O365ProPlusRetail ">
            <Language ID="en-us" />
          </Product>
          <Product ID="VisioProRetail">
            <Language ID="en-us" />
          </Product>
        </Add>
      </Configuration>
      ```

      >**Hinweis**  Das Konfigurations-XML ist eine XML-Beispieldatei. Die Datei enthält Zeilen, die auskommentiert werden. Sie können diese Zeilen "kommentieren", um zusätzliche Einstellungen für die Datei anzupassen. Wenn Sie diese Zeilen "kommentieren" möchten, entfernen Sie die "<! --"vom Anfang der Zeile und der"--> "vom Ende der Zeile aus.

      In der obigen XML-Konfigurationsdatei wird angegeben, dass die Office 2016 ProPlus 32-Bit-Edition, einschließlich Visio ProPlus, in Englisch auf das \\\\server\\Office 2016 heruntergeladen wird, dem Speicherort, in dem Office-Anwendungen gespeichert werden. Beachten Sie, dass sich die Produkt-ID der Anwendungen nicht auf die endgültige Lizenzierung von Office auswirkt. Office 2016-App-V-Pakete mit unterschiedlicher Lizenzierung können über die gleichen Anwendungen erstellt werden, indem die Lizenzierung in einem späteren Schritt angegeben wird. In der folgenden Tabelle sind die anpassbaren Attribute und Elemente der XML-Datei zusammengefasst:

      <table>
      <colgroup>
      <col width="33%" />
      <col width="33%" />
      <col width="33%" />
      </colgroup>
      <thead>
      <tr class="header">
      <th align="left">Eingabe</th>
      <th align="left">Beschreibung</th>
      <th align="left">Beispiel</th>
      </tr>
      </thead>
      <tbody>
      <tr class="odd">
      <td align="left"><p>Element hinzufügen</p></td>
      <td align="left"><p>Gibt die Produkte und Sprachen an, die in das Paket eingeschlossen werden sollen.</p></td>
      <td align="left"><p>n.v.</p></td>
      </tr>
      <tr class="even">
      <td align="left"><p>OfficeClientEdition (Attribut des Add-Elements)</p></td>
      <td align="left"><p>Gibt die Edition des zu verwendenden Office 2016-Produkts an: 32-Bit oder 64-Bit. Der Vorgang schlägt fehl <strong> , wenn OfficeClientEdition </strong> nicht auf einen gültigen Wert gesetzt ist.</p></td>
      <td align="left"><p><strong>OfficeClientEdition </strong> = &quot; 32&quot;</p>
      <p><strong>OfficeClientEdition </strong> = &quot; 64&quot;</p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p>Product-Element</p></td>
      <td align="left"><p>Gibt die Anwendung an. Project 2016 und Visio 2016 müssen hier als hinzugefügtes Produkt angegeben werden, das in die Anwendungen aufgenommen werden soll.

      Weitere Informationen zu den Produkt-IDs finden Sie unter vom <a href="https://support.microsoft.com/kb/2842297" data-raw-source="[Product IDs that are supported by the Office Deployment Tool for Click-to-Run](https://support.microsoft.com/kb/2842297)"> Office-Bereitstellungs Tool unterstützte Produkt-IDs für Klick-und-los.</a>
      </p></td>
      <td align="left"><p><code>Product ID =&quot;O365ProPlusRetail &quot;</code></p>
      <p><code>Product ID =&quot;VisioProRetail&quot;</code></p>
      <p><code>Product ID =&quot;ProjectProRetail&quot;</code></p>
      </td>
      </tr>
      <tr class="even">
      <td align="left"><p>Language-Element</p></td>
      <td align="left"><p>Gibt die Sprache an, die in den Anwendungen unterstützt wird.</p></td>
      <td align="left"><p><code>Language ID=&quot;en-us&quot;</code></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p>Version (Attribut des Add-Elements)</p></td>
      <td align="left"><p>Optional. Gibt einen Build an, der für das Paket verwendet werden soll.</p>
      <p>Standardwert für den neuesten angekündigten Build (wie in v32.CAB in der Office-Quelle definiert).</p></td>
      <td align="left"><p><code>16.1.2.3</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p>SourcePath (Attribut des Add-Elements)</p></td>
      <td align="left"><p>Gibt den Speicherort an, in dem die Anwendungen gespeichert werden.</p></td>
      <td align="left"><p><code>Sourcepath = &quot;\Server\Office2016”</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p>Verzweigung (Attribut des Add-Elements)</p></td>
      <td align="left"><p>Optional. Gibt den Aktualisierungszweig für das Produkt an, das heruntergeladen oder installiert werden soll. </p><p>Weitere Informationen zu Update Verzweigungen finden Sie unter Übersicht über Update Verzweigungen für Microsoft 365-Apps für Unternehmen.</p></td>
      <td align="left"><p><code>Branch = &quot;Business&quot;</code></p></td>
      </tr>
      </tbody>
      </table>

      Nachdem Sie die configuration.xml-Datei bearbeitet haben, um das gewünschte Produkt, die Sprachen und auch den Speicherort anzugeben, auf dem die Office 2016-Anwendungen gespeichert werden, können Sie beispielsweise die Konfigurationsdatei als Customconfig.xml speichern.

2. **Laden Sie die Anwendungen in den angegebenen Speicherort herunter:** Verwenden Sie eine Eingabeaufforderung mit erhöhten Rechten und ein 64-Bit-Betriebssystem, um die Office 2016-Anwendungen herunterzuladen, die später in ein App-V-Paket konvertiert werden. Im folgenden finden Sie einen Beispielbefehl mit einer Beschreibung der Details:

   ``` syntax
   \\server\Office2016\setup.exe /download \\server\Office2016\Customconfig.xml
   ```

   Im Beispiel:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>\server\Office2016</strong></p></td>
   <td align="left"><p>der Speicherort des Netzwerkspeichers, der das Office-Bereitstellungs Tool und die benutzerdefinierte Configuration.xml Datei enthält, Customconfig.xml.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Setup.exe</strong></p></td>
   <td align="left"><p>ist das Office-Bereitstellungs Tool.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>/Download</strong></p></td>
   <td align="left"><p>downloadet die Office 2016-Anwendungen, die Sie in der customConfig.xml-Datei angeben. Diese Bits können später in einem Office 2016-App-V-Paket mit Volumenlizenzierung konvertiert werden.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>\server\Office2016\Customconfig.xml</strong></p></td>
   <td align="left"><p>übergibt die XML-Konfigurationsdatei, die zum Abschließen des Downloadprozesses erforderlich ist, in diesem Beispiel customconfig.xml. Nach Verwendung des Befehls "Download" sollten sich die Office-Anwendungen an dem Speicherort befinden, der in der XML-Konfigurationsdatei angegeben ist, in diesem Beispiel \Server\Office2016.</p></td>
   </tr>
   </tbody>
   </table>



### Konvertieren der Office-Anwendungen in ein App-V-Paket

Nachdem Sie die Office 2016-Anwendungen über das Office-Bereitstellungstool heruntergeladen haben, verwenden Sie das Office-Bereitstellungstool, um Sie in ein Office 2016 App-V-Paket umzuwandeln. Führen Sie die Schritte aus, die Ihrem Lizenzierungsmodell entsprechen.

**Zusammenfassung der erforderlichen Schritte:**

-   Erstellen Sie die Office 2016-App-V-Pakete auf 64-Bit-Windows-Computern. Das Paket wird jedoch auf 32-Bit-und 64-Bit-Computern unter Windows 7, Windows 8 oder 8,1 und Windows 10 ausgeführt.

-   Erstellen Sie mithilfe des Office-Bereitstellungstools ein Office App-V-Paket für das Abonnement Lizenzierungs Paket, und ändern Sie dann die CustomConfig.xml-Konfigurationsdatei.

    In der folgenden Tabelle sind die Werte zusammengefasst, die Sie in die CustomConfig.xml-Datei für das verwendete Lizenzierungsmodell eingeben müssen. Die Schritte in den Abschnitten, die der Tabelle folgen, geben die genauen Einträge an, die Sie vornehmen müssen.

>**Note** &nbsp; Hinweis &nbsp; Sie können das Office-Bereitstellungs Tool verwenden, um App-V-Pakete für Microsoft 365-Apps für Unternehmen zu erstellen. Das Erstellen von Paketen für die Volumen lizenzierten Versionen von Office Professional Plus oder Office Standard wird nicht unterstützt.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Produkt-ID</th>
<th align="left">Abonnementlizenzierung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Office2016</strong></p></td>
<td align="left"><p>O365ProPlusRetail</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Office 2016 mit Visio 2016</strong></p></td>
<td align="left"><p>O365ProPlusRetail</p>
<p>VisioProRetail</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Office 2016 mit Visio 2016 und Project 2016</strong></p></td>
<td align="left"><p>O365ProPlusRetail</p>
<p>VisioProRetail</p>
<p>ProjectProRetail</p></td>
</tr>
</tbody>
</table>



**Konvertieren der Office-Anwendungen in ein App-V-Paket**

1. Öffnen Sie die CustomConfig.xml Datei in Editor erneut, und nehmen Sie die folgenden Änderungen an der Datei vor:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Parameter</th>
   <th align="left">So ändern Sie den Wert</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>SourcePath</p></td>
   <td align="left"><p>Zeigen Sie auf die zuvor heruntergeladenen Office-Anwendungen.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ProductID</p></td>
   <td align="left"><p>Geben Sie die Abonnementlizenzierung an, wie im folgenden Beispiel gezeigt:</p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\server\Office 2016&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;O365ProPlusRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt; </code></pre>
   <p>In diesem Beispiel wurden die folgenden Änderungen zum Erstellen eines Pakets mit Abonnementlizenzierung vorgenommen:</p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>SourcePath</strong></p></td>
   <td align="left"><p>ist der Pfad, der geändert wurde, um auf die Office-Anwendungen zu verweisen, die zuvor heruntergeladen wurden.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Produkt-ID</strong></p></td>
   <td align="left"><p>für Office wurde geändert in <code>O365ProPlusRetail</code> .</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Produkt-ID</strong></p></td>
   <td align="left"><p>für Visio wurde geändert in <code>VisioProRetail</code> .</p></td>
   </tr>
   </tbody>
   </table>
   <p></p>
   <tr class="odd">
   <td align="left"><p>ExcludeApp (optional)</p></td>
   <td align="left"><p>Mit dieser Option können Sie Office-Programme angeben, die nicht im App-V-Paket enthalten sein sollen, das vom Office-Bereitstellungs Tool erstellt wird. So können Sie beispielsweise Access und InfoPath ausschließen.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>PACKAGEGUID (optional)</p></td>
   <td align="left"><p>Standardmäßig verwenden alle App-v-Pakete, die vom Office-Bereitstellungs Tool erstellt wurden, dieselbe App-v-Paket-ID. Sie können PACKAGEGUID verwenden, um eine andere Paket-ID für jedes Paket anzugeben, mit der Sie mehrere App-v-Pakete, die vom Office-Bereitstellungs Tool erstellt wurden, veröffentlichen und mithilfe des App-v-Servers verwalten können.</p>
   <p>Ein Beispiel für die Verwendung dieses Parameters ist, wenn Sie unterschiedliche Pakete für verschiedene Benutzer erstellen. So können Sie beispielsweise ein Paket mit Office 2016 für einige Benutzer erstellen und ein weiteres Paket mit Office 2016 und Visio 2016 für eine andere Gruppe von Benutzern erstellen.</p>

   &gt;<strong>Hinweis </strong> auch wenn Sie eindeutige Paket-IDs verwenden, können Sie weiterhin nur ein App-V-Paket auf einem einzelnen Gerät bereitstellen.
   </td>
   </tr>
   </tbody>
   </table>


2. Verwenden Sie den Befehl/Packager, um die Office-Anwendungen in ein Office 2016-App-V-Paket umzuwandeln.

   Beispiel:

   ``` syntax
   \\server\Office2016\setup.exe /packager \\server\Office2016\Customconfig.xml  \\server\share\Office2016AppV
   ```

   Im Beispiel:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>\server\Office2016</strong></p></td>
   <td align="left"><p>der Speicherort des Netzwerkspeichers, der das Office-Bereitstellungs Tool und die benutzerdefinierte Configuration.xml Datei enthält, Customconfig.xml.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Setup.exe</strong></p></td>
   <td align="left"><p>ist das Office-Bereitstellungs Tool.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>/packager</strong></p></td>
   <td align="left"><p>erstellt das Office 2016-App-V-Paket mit der Art der Lizenzierung, die in der customConfig.xml-Datei angegeben ist.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>\server\Office2016\Customconfig.xml</strong></p></td>
   <td align="left"><p>übergibt die Konfigurations-XML-Datei (in diesem Fall customConfig), die für die Paket Phase vorbereitet wurde.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>\server\share\Office 2016AppV</strong></p></td>
   <td align="left"><p>Gibt den Speicherort des neu erstellten Office App-V-Pakets an.</p></td>
   </tr>
   </tbody>
   </table>



~~~
After you run the **/packager** command, the following folders appear up in the directory where you specified the package should be saved:

-   **App-V Packages** – contains an Office 2016 App-V package and two deployment configuration files.

-   **WorkingDir**

**Note** To troubleshoot any issues, see the log files in the %temp% directory (default).
~~~



3. Überprüfen Sie, ob das Office 2016-App-V-Paket ordnungsgemäß funktioniert:

   1.  Veröffentlichen Sie das von Ihnen Global erstellte Office 2016 App-V-Paket auf einem Testcomputer, und überprüfen Sie, ob die Office 2016-Verknüpfungen angezeigt werden.

   2.  Starten Sie einige Office 2016-Anwendungen wie Excel oder Word, um sicherzustellen, dass Ihr Paket wie erwartet funktioniert.

## <a href="" id="bkmk-pub-pkg-office"></a>Veröffentlichen des Office-Pakets für App-V


Verwenden Sie die folgenden Informationen zum Veröffentlichen eines Office-Pakets.

### Methoden zum Veröffentlichen von Office App-V-Paketen

Stellen Sie das App-V-Paket für Office 2016 mithilfe der gleichen Methoden bereit, die Sie für jedes andere Paket verwenden:

-   System Center Konfigurations-Manager

-   App-V-Server

-   Eigenständige über PowerShell-Befehle

### Voraussetzungen und Anforderungen für die Veröffentlichung

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Voraussetzungen oder Anforderungen</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aktivieren von PowerShell-Skripts für die App-V-Clients</p></td>
<td align="left"><p>Zum Veröffentlichen von Office 2016-Paketen müssen Sie ein Skript ausführen.</p>
<p>Paket Skripts sind auf App-V-Clients standardmäßig deaktiviert. Führen Sie zum Aktivieren der Skripterstellung den folgenden PowerShell-Befehl aus:</p>
<pre class="syntax" space="preserve"><code>Set-AppvClientConfiguration –EnablePackageScripts 1</code></pre></td>
</tr>
<tr class="even">
<td align="left"><p>Veröffentlichen des Office 2016-Pakets auf globaler Ebene</p></td>
<td align="left"><p>Erweiterungspunkte im Office App-V-Paket erfordern die Installation auf Computerebene.</p>
<p>Wenn Sie auf Computerebene veröffentlichen, werden keine Voraussetzungen oder verteilbaren Aktionen benötigt, und das Office 2016-Paket ermöglicht es, dass seine Anwendungen wie nativ installierte Office funktionieren, sodass Administratoren keine Pakete anpassen müssen.</p></td>
</tr>
</tbody>
</table>



### Veröffentlichen eines Office-Pakets

Führen Sie den folgenden Befehl aus, um ein Office-Paket global zu veröffentlichen:

-   `Add-AppvClientPackage <Path_to_AppV_Package> | Publish-AppvClientPackage –global`

-   Über die Web-Verwaltungskonsole auf dem App-V-Server können Sie einer Gruppe von Computern Berechtigungen hinzufügen, anstatt einer Benutzergruppe, um zu ermöglichen, dass Pakete Global auf den Computern in der entsprechenden Gruppe veröffentlicht werden.

## <a href="" id="bkmk-custmz-manage-office-pkgs"></a>Anpassen und Verwalten von Office App-V-Paketen


Zum Verwalten Ihrer Office-App-V-Pakete verwenden Sie die gleichen Vorgänge wie für jedes andere Paket, doch es gibt ein paar Ausnahmen, wie in den folgenden Abschnitten beschrieben.

-   [Aktivieren von Office-Plug-Ins mithilfe von Verbindungsgruppen](#bkmk-enable-office-plugins)

-   [Deaktivieren von Office 2016-Anwendungen](#bkmk-disable-office-apps)

-   [Deaktivieren von Office 2016-Tastenkombinationen](#bkmk-disable-shortcuts)

-   [Verwalten von Office 2016-Paket Upgrades](#bkmk-manage-office-pkg-upgrd)

-   [Bereitstellen von Visio 2016 und Project 2016 mit Office](#bkmk-deploy-visio-project)

### <a href="" id="bkmk-enable-office-plugins"></a>Aktivieren von Office-Plug-Ins mithilfe von Verbindungsgruppen

Führen Sie die Schritte in diesem Abschnitt aus, um Office-Plug-ins mit Ihrem Office-Paket zu aktivieren. Um Office-Plug-ins zu verwenden, müssen Sie den App-V-Sequenzer verwenden, um ein separates Paket zu erstellen, das nur die Plug-Ins enthält. Sie können das Office-Bereitstellungs Tool nicht verwenden, um das Plug-in-Paket zu erstellen. Sie erstellen dann eine Verbindungsgruppe, die das Office-Paket und das Plug-in-Paket enthält, wie in den folgenden Schritten beschrieben.

**So aktivieren Sie Plug-Ins für Office App-V-Pakete**

1.  Fügen Sie mithilfe von App-V Server, System Center Configuration Manager oder einem PowerShell-Cmdlet eine Verbindungsgruppe hinzu.

2.  Sequenzieren Sie Ihre Plug-Ins mithilfe des App-V-Sequencers. Stellen Sie sicher, dass Office 2016 auf dem Computer installiert ist, der zur Sequenzierung des Plug-ins verwendet wird. Es wird empfohlen, Microsoft 365-Apps für Enterprise (nicht-virtuell) auf dem Sequenzcomputer zu verwenden, wenn Sie Office 2016-Plug-ins abgleichen.

3.  Erstellen Sie ein App-V-Paket, das die gewünschten Plug-Ins enthält.

4.  Fügen Sie mithilfe von App-V Server, System Center Configuration Manager oder einem PowerShell-Cmdlet eine Verbindungsgruppe hinzu.

5.  Fügen Sie das Office 2016-App-V-Paket und das Plug-in-Paket, das Sie sequenziert haben, zu der von Ihnen erstellten Verbindungsgruppe hinzu.

    >**Wichtig** Die Reihenfolge der Pakete in der Verbindungsgruppe bestimmt die Reihenfolge, in der die Paketinhalte zusammengeführt werden. Fügen Sie in ihrer Beschreibungsdatei für die Verbindungsgruppe zuerst das Office 2016-App-v-Paket hinzu, und fügen Sie dann das Plug-in-App-v-Paket hinzu.



6.  Stellen Sie sicher, dass beide Pakete auf dem Zielcomputer veröffentlicht werden und dass das Plug-in-Paket Global veröffentlicht wird, um die globalen Einstellungen des veröffentlichten Office 2016-App-V-Pakets zu erfüllen.

7.  Überprüfen Sie, ob die Bereitstellungs Konfigurationsdatei des Plug-in-Pakets die gleichen Einstellungen wie das Office 2016-App-V-Paket aufweist.

    Da das Office 2016-App-V-Paket in das Betriebssystem integriert ist, sollten die Einstellungen für das Plug-in-Paket übereinstimmen. Sie können die Konfigurationsdatei für die Bereitstellung nach "com-Modus" Durchsuchen und sicherstellen, dass Ihr Plug-in-Paket diesen Wert als "integriert" festgesetzt hat und sowohl "InProcessEnabled" als auch "OutOfProcessEnabled" den Einstellungen des veröffentlichten Office 2016-App-V-Pakets entsprechen.

8.  Öffnen Sie die Konfigurationsdatei für die Bereitstellung, und legen Sie den Wert für **Objekte** auf **false**fest.

9.  Wenn Sie nach der Sequenzierung Änderungen an der Konfigurationsdatei für die Bereitstellung vorgenommen haben, stellen Sie sicher, dass das Plug-in-Paket mit der Datei veröffentlicht wird.

10. Stellen Sie sicher, dass die von Ihnen erstellte Verbindungsgruppe auf dem gewünschten Computer aktiviert ist. Die erstellte Verbindungsgruppe wird wahrscheinlich "aussetzen", wenn das Office 2016-App-V-Paket verwendet wird, wenn die Verbindungsgruppe aktiviert ist. In diesem Fall müssen Sie den Neustart durchführen, um die Verbindungsgruppe erfolgreich zu aktivieren.

11. Nachdem Sie beide Pakete erfolgreich veröffentlicht und die Verbindungsgruppe aktiviert haben, starten Sie die Office 2016-Zielanwendung, und stellen Sie sicher, dass das von Ihnen veröffentlichte und der Verbindungsgruppe hinzugefügte Plug-in wie erwartet funktioniert.

### <a href="" id="bkmk-disable-office-apps"></a>Deaktivieren von Office 2016-Anwendungen

Möglicherweise möchten Sie bestimmte Anwendungen in Ihrem Office App-V-Paket deaktivieren. So können Sie beispielsweise den Zugriff deaktivieren, aber alle anderen Office-Anwendungen Main verfügbar lassen. Wenn Sie eine Anwendung deaktivieren, wird dem Endbenutzer die Verknüpfung für diese Anwendung nicht mehr angezeigt. Sie müssen die Anwendung nicht neu sequenzieren. Wenn Sie die Konfigurationsdatei für die Bereitstellung nach dem Veröffentlichen des Office 2016-App-v-Pakets ändern, speichern Sie die Änderungen, fügen das Office 2016-App-v-Paket hinzu und veröffentlichen es dann erneut mit der neuen Bereitstellungs Konfigurationsdatei, um die neuen Einstellungen auf Office 2016 App-v-Paketanwendungen anzuwenden.

>**Hinweis** Wenn Sie bestimmte Office-Anwendungen (beispielsweise Access und InfoPath) beim Erstellen des App-V-Pakets mit dem Office-Bereitstellungs Tool ausschließen möchten, verwenden Sie die Einstellung **ExcludeApp** .


**So deaktivieren Sie eine Office 2016-Anwendung**

1.  Öffnen Sie eine Konfigurationsdatei für die Bereitstellung mit einem Text-Editor wie **Editor** , und suchen Sie nach "Anwendungen".

2.  Suchen Sie nach der Office-Anwendung, die Sie deaktivieren möchten, beispielsweise Access 2016.

3.  Ändern Sie den Wert von "Enabled" von "true" in "false".

4.  Speichern Sie die Konfigurationsdatei für die Bereitstellung.

5.  Fügen Sie das Office 2016-App-V-Paket mit der neuen Bereitstellungs Konfigurationsdatei hinzu.

    ```xml
    <Application Id="[{AppVPackageRoot}]\office16\lync.exe" Enabled="true">
      <VisualElements>
        <Name>Lync 2016</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[(AppVPackageRoot}]\office16\MSACCESS.EXE" Enabled="true">
      <VisualElements>
        <Name>Access 2016</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    ```

6.  Fügen Sie das Office 2016-App-v-Paket erneut hinzu, und veröffentlichen Sie es erneut mit der neuen Bereitstellungs Konfigurationsdatei, um die neuen Einstellungen auf Office 2016 App-v-Paketanwendungen anzuwenden.

### <a href="" id="bkmk-disable-shortcuts"></a>Deaktivieren von Office 2016-Tastenkombinationen

Möglicherweise möchten Sie die Tastenkombinationen für bestimmte Office-Anwendungen deaktivieren, anstatt das Paket zu veröffentlichen oder zu entfernen. Im folgenden Beispiel wird gezeigt, wie Sie Tastenkombinationen für Microsoft Access deaktivieren.

**So deaktivieren Sie Tastenkombinationen für Office 2016-Anwendungen**

1.  Öffnen Sie eine Konfigurationsdatei für die Bereitstellung in Editor, und suchen Sie nach "Tastenkombinationen".

2.  Wenn Sie bestimmte Tastenkombinationen deaktivieren möchten, löschen oder kommentieren Sie die gewünschten Tastenkombinationen aus. Sie müssen das Subsystem vorhanden und aktiviert lassen. Löschen Sie beispielsweise im folgenden Beispiel die Microsoft Access-Tastenkombinationen, während &lt; Sie die Tastenkombination &gt; &lt; /Shortcut intakt halten, &gt; um die Microsoft Access-Verknüpfung zu deaktivieren.

    ``` syntax
    Shortcuts

    -->
     <Shortcuts Enabled="true">
      <Extensions>
        <Extension Category="AppV.Shortcut">
          <Shortcut>
           <File>[{Common Programs}]\Microsoft Office 2016\Access 2016.lnk</File>
           <Target>[{AppvPackageRoot}])office16\MSACCESS.EXE</Target>
           <Icon>[{Windows}]\Installer\{90150000-000F-0000-0000-000000FF1CE)\accicons.exe.Ø.ico</Icon>
           <Arguments />
           <WorkingDirectory />
           <AppuserModelId>Microsoft.Office.MSACCESS.EXE.15</AppUserModelId>
           <AppUserModelExcludeFromShowInNewInstall>true</AppUserModelExcludeFromShowInNewInstall>
           <Description>Build a professional app quickly to manage data.</Description>
           <ShowCommand>l</ShowCommand>
           <ApplicationId>[{AppVPackageRoot}]\office16\MSACCESS.EXE</ApplicationId>
        </Shortcut>
    ```

3.  Speichern Sie die Konfigurationsdatei für die Bereitstellung.

4.  Veröffentlichen Sie das Office 2016 App-V-Paket erneut mit der neuen Bereitstellungs Konfigurationsdatei.

Viele zusätzliche Einstellungen können durch Ändern der Bereitstellungskonfiguration für App-V-Pakete geändert werden, beispielsweise Dateitypen Zuordnungen, virtuelles Datei System und vieles mehr. Weitere Informationen zur Verwendung von Bereitstellungskonfigurationsdateien zum Ändern von App-V-Paketeinstellungen finden Sie im Abschnitt zusätzliche Ressourcen am Ende dieses Dokuments.

### <a href="" id="bkmk-manage-office-pkg-upgrd"></a>Verwalten von Office 2016-Paket Upgrades

Verwenden Sie das Office-Bereitstellungs Tool, um ein Office 2016-Paket zu aktualisieren. Führen Sie die folgenden Schritte aus, um ein zuvor bereitgestelltes Office 2016-Paket zu aktualisieren.

**Aktualisieren eines zuvor bereitgestellten Office 2016-Pakets**

1. Erstellen Sie ein neues Office 2016-Paket über das Office-Bereitstellungs Tool, das die neueste Office 2016-Anwendungssoftware verwendet. Die neuesten Office 2016-Bits können immer über die Downloadphase des Erstellens eines Office 2016-App-V-Pakets abgerufen werden. Das neu erstellte Office 2016-Paket verfügt über die neuesten Updates und eine neue Versions-ID. Alle Pakete, die mit dem Office-Bereitstellungs Tool erstellt wurden, haben dieselbe Linie.

   > **Hinweis** Office App-V-Pakete weisen zwei Versions-IDs auf:
   > <ul>
   > <li>Eine Office 2016-App-V-paketversions-ID, die für alle mit dem Office-Bereitstellungs Tool erstellten Pakete eindeutig ist.</li>
   > <li>Eine zweite App-V-Paket-Versions-ID, x. x. x. x, beispielsweise im AppX-Manifest, das nur dann geändert wird, wenn eine neue Version von Office selbst vorhanden ist. Wenn beispielsweise eine neue Office 2016-Version mit Upgrades verfügbar ist und ein Paket über das Office-Bereitstellungs Tool erstellt wird, um diese Upgrades zu integrieren, ändert sich die x. x. x. x-Version, um zu reflektieren, dass sich die Office-Version selbst geändert hat. Der App-V-Server verwendet die x. x. x. x. x-Versions-ID, um dieses Paket zu unterscheiden und zu erkennen, dass es neue Upgrades für das zuvor veröffentlichte Paket enthält, und als Ergebnis es als Upgrade auf das vorhandene Office 2016-Paket veröffentlichen.</li>
   > </ul>


2. Veröffentlichen Sie die neu erstellten Office 2016-App-V-Pakete Global auf Computern, auf denen Sie die neuen Updates anwenden möchten. Da das neue Paket dieselbe Abstammungslinie des älteren Office 2016-App-V-Pakets aufweist, werden durch das Veröffentlichen des neuen Pakets mit den Updates nur die neuen Änderungen auf das alte Paket angewendet, und es wird schnell so sein.

3. Upgrades werden auf die gleiche Weise wie alle Global veröffentlichten App-V-Pakete angewendet. Da Anwendungen wahrscheinlich verwendet werden, können Upgrades verzögert werden, bis der Computer neu gestartet wird.


### <a href="" id="bkmk-deploy-visio-project"></a>Bereitstellen von Visio 2016 und Project 2016 mit Office

In der folgenden Tabelle werden die Anforderungen und Optionen für die Bereitstellung von Visio 2016 und Project 2016 mit Office beschrieben.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabe</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Wie kann ich Visio 2016 und Project 2016 mit Office Verpacken und veröffentlichen?</p></td>
<td align="left"><p>Sie müssen Visio 2016 und Project 2016 in das gleiche Paket mit Office einbeziehen.</p>
<p>Wenn Sie Office nicht bereitstellen, können Sie ein Paket erstellen, das Visio und/oder Project enthält, sofern Sie die in diesem Thema beschriebenen Verpackungs-, Veröffentlichungs-und Bereitstellungsanforderungen befolgen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Wie kann ich Visio 2016 und Project 2016 für bestimmte Benutzer bereitstellen?</p></td>
<td align="left"><p>Verwenden Sie eine der folgenden Methoden:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Wenn Sie möchten...</th>
<th align="left">... Verwenden Sie dann diese Methode</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Erstellen von zwei unterschiedlichen Paketen und Bereitstellen jeder Person für eine andere Gruppe von Benutzern</p></td>
<td align="left"><p>Erstellen und Bereitstellen der folgenden Pakete:</p>
<ul>
<li><p>Ein Paket, das nur Office-deploy auf Computern enthält, deren Benutzer nur Office benötigen.</p></li>
<li><p>Ein Paket mit Office, Visio und Project – deploy auf Computern, deren Benutzer alle drei Anwendungen benötigen.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Wenn Sie nur ein Paket für die gesamte Organisation verwenden möchten oder wenn Sie über Benutzer verfügen, die Computer freigeben:</p></td>
<td align="left"><p>Führen Sie die folgenden Schritte aus:</p>
<ol>
<li><p>Erstellen Sie ein Paket, das Office, Visio und Project enthält.</p></li>
<li><p>Bereitstellen des Pakets für alle Benutzer</p></li>
<li><p>Verwenden Sie <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)"> Microsoft AppLocker </a> , um zu verhindern, dass bestimmte Benutzer Visio und Project verwenden.</p></li>
</ol></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>


## Zusätzliche Ressourcen


[Bereitstellen von Microsoft Office2013 mit App-V](deploying-microsoft-office-2013-by-using-app-v.md)

[Bereitstellen von Microsoft Office2010 mit App-V](deploying-microsoft-office-2010-by-using-app-v.md)

[Office 2016-Bereitstellungs Tool für Klick-und-Los](https://www.microsoft.com/download/details.aspx?id=49117)

**Verbindungsgruppen**

[Bereitstellen von Verbindungsgruppen in Microsoft App-V V5](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[Verwalten von Verbindungsgruppen](managing-connection-groups.md)

**Dynamische Konfiguration**

[Informationen zur dynamischen Konfiguration in App-V 5.1](about-app-v-51-dynamic-configuration.md)





