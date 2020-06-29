---
title: So verwenden Sie optionale Pakete in Verbindungsgruppen
description: So verwenden Sie optionale Pakete in Verbindungsgruppen
author: dansimp
ms.assetid: 67666f18-b704-4852-a1e4-d13633bd2baf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ffa29f5d62e57a60423b2041cb71787d2c96bd66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805120"
---
# So verwenden Sie optionale Pakete in Verbindungsgruppen


Ab Microsoft Application Virtualization (App-V) 5,0 SP3 können Sie Ihren Verbindungsgruppen optionale Pakete hinzufügen, um die Verwaltung der Verbindungsgruppe zu vereinfachen. In der folgenden Tabelle sind die Aufgaben, die Sie mithilfe optionaler Pakete einfacher durchführen können, zusammengefasst, und es werden Links zu den Anweisungen für die einzelnen Aufgaben bereitgestellt.

**Hinweis** 
 **Optionale Pakete werden in Versionen vor App-V 5,0 SP3 nicht unterstützt.**

 

Lesen Sie vor dem Verwenden optionaler Pakete die [Anforderungen für die Verwendung optionaler Pakete in Verbindungsgruppen](#bkmk-reqs-using-cg).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Link zu Anweisungen</th>
<th align="left">Aufgabe</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="#bkmk-apps-plugs-optional" data-raw-source="[Use one connection group, with optional packages, for multiple users who have different packages entitled to them](#bkmk-apps-plugs-optional)">Verwenden einer Verbindungsgruppe mit optionalen Paketen für mehrere Benutzer, die über verschiedene Pakete verfügen, die Ihnen zustehen</a></p></td>
<td align="left"><p>Verwenden Sie eine einzelne Verbindungsgruppe, um verschiedene Gruppen von Anwendungen und Plug-Ins für verschiedene Endbenutzer verfügbar zu machen.</p>
<p>Angenommen, Sie möchten Microsoft Office an alle Endbenutzer verteilen, aber verschiedene Plug-ins an verschiedene Teilmengen von Benutzern verteilen.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="#bkmk-unpub-del-optl-pkg" data-raw-source="[Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group](#bkmk-unpub-del-optl-pkg)">Aufheben der Veröffentlichung oder Löschen eines optionalen Pakets oder Aufheben der Veröffentlichung eines optionalen Pakets und erneutes veröffentlichen, ohne die Verbindungsgruppe zu ändern</a></p></td>
<td align="left"><p>Heben Sie die Veröffentlichung, Löschung oder erneute Veröffentlichung eines optionalen Pakets auf, ohne die Verbindungsgruppe auf dem App-V-Client zu deaktivieren, zu entfernen, zu bearbeiten, hinzuzufügen und wieder zu aktivieren.</p>
<p>Sie können die Veröffentlichung des optionalen Pakets auch aufheben und später erneut veröffentlichen, ohne die Verbindungsgruppe deaktivieren oder erneut veröffentlichen zu müssen.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-apps-plugs-optional"></a>Verwenden einer Verbindungsgruppe mit optionalen Paketen für mehrere Benutzer mit unterschiedlichen Paketen, die Ihnen zustehen


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabenbeschreibung</th>
<th align="left">Durchführen der Aufgabe</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Mit App-v 5,0 SP3 und App-v 5,1</strong></p>
<p>Sie können Verbindungsgruppen optionale Pakete hinzufügen, mit denen Sie unterschiedliche Kombinationen von Anwendungen und Plug-Ins für verschiedene Endbenutzer bereitstellen können.</p>
<p><strong>Beispiel </strong> : Sie möchten Microsoft Office an Ihre Endbenutzer verteilen, aber ein bestimmtes Plug-in nur für eine Teilmenge der Benutzer aktivieren.</p>
<p>Erstellen Sie dazu eine Verbindungsgruppe, die ein Paket mit Office und ein weiteres Paket mit Office-Plug-Ins enthält, und machen Sie dann das Plug-in-Paket optional.</p>
<p>Endbenutzer, die nicht zum Plug-in-Paket berechtigt sind, können Office weiterhin ausführen.</p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Methode</th>
<th align="left">Schritte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V Server – Verwaltungskonsole</p></td>
<td align="left"><ol>
<li><p>Wählen Sie in der Verwaltungskonsole <strong> Verbindungsgruppen aus </strong> , um die Bibliothek Verbindungsgruppen anzuzeigen.</p></li>
<li><p>Wählen Sie in der Bibliothek Verbindungsgruppen die richtige Verbindungsgruppe aus.</p></li>
<li><p>Klicken <strong> Sie </strong> im Bereich verbundene Pakete auf Bearbeiten.</p></li>
<li><p>Wählen Sie <strong> optional </strong> neben dem Paketnamen aus.</p></li>
<li><p>Aktivieren Sie das <strong> Kontrollkästchen Paketzugriff auf Gruppen Zugriff hinzufügen </strong> . Dieser erforderliche Schritt fügt der Verbindungsgruppe die Paket Berechtigungen hinzu, die Sie zuvor konfiguriert haben, als Sie den Active Directory-GRUPPENPAKETE zugewiesen haben.</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>App-V Server-PowerShell-Cmdlet</p></td>
<td align="left"><p>Verwenden Sie das folgende Cmdlet, und geben Sie den <strong> Parameter-optional an </strong> :</p>
<p><strong>Add-AppvServerConnectionGroupPackage</strong></p>
<p><strong>Syntax</strong></p>
<p><code>Add-AppvServerConnectionGroupPackage [-AppvServerConnectionGroup] &lt;SerializableConnectionGroup&gt; [[-AppvServerPackage] &lt;PackageVersion&gt;] [-Optional] [-Order &lt;int&gt;] [-UseAnyPackageVersion]</code></p>
<p><strong>Beispiel:</strong></p>
<p><code>Add-AppvServerConnectionGroupPackage -Name &quot;Connection Group 1&quot; -PackageName &quot;Package 1&quot; -Optional</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V-Client auf einem eigenständigen Computer</p></td>
<td align="left"><ol>
<li><p>Erstellen Sie das Verbindungsgruppen-XML-Dokument, und legen <strong> Sie das Package </strong> Tag-Attribut <strong> isOptional </strong> auf <strong> "true" fest.</strong></p></li>
<li><p>Verwenden Sie die folgenden Cmdlets, um die Verbindungsgruppe hinzuzufügen und zu aktivieren:</p>
<ul>
<li><p>Add-AppvClientConnectionGroup</p></li>
<li><p>Enable-AppvClientConnectionGroup</p></li>
</ul></li>
</ol>
<p><strong>Beispiel für ein Verbindungsgruppen-XML-Dokument mit optionalen Paketen:</strong></p>
<pre class="syntax" space="preserve"><code>&lt;?xml version=&quot;1.0&quot; ?&gt;
&lt;AppConnectionGroup
   xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;
   AppConnectionGroupId=&quot;8105CCD5-244B-4BA1-8888-E321E688D2CB&quot;
   VersionId=&quot;84CE3797-F1CB-4475-A223-757918929EB4&quot;
   DisplayName=&quot;Contoso Software Connection Group&quot; &gt;
&lt;Packages&gt;
&lt;Package
   PackageId=&quot;7735d1a8-5ef9-4df9-a1cf-3aa92ef54fe7&quot;
   VersionId=&quot;ec560d6f-e62e-48eb-a9e5-7c52a8c2e149&quot;
   DisplayName=&quot;Contoso Business Manager&quot;
/&gt;

&lt;Package
   PackageId=&quot;fc6fe0f7-be3d-4643-b37d-fc3f62d4dd5c&quot;
   VersionId=&quot;c67a71cd-3542-4a48-93e8-20c643c50970&quot;
   DisplayName=&quot;Contoso Forms&quot;
   IsOptional=&quot;false&quot;
/&gt;

&lt;Package
   PackageId=&quot;8f6301a5-4348-4039-9560-b27a5bb72711&quot;
   VersionId=&quot;6c694b45-3e19-46c6-a327-d159aa39e1d2&quot;
   DisplayName=&quot;Contoso Tax&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;Package
   PackageId=&quot;89d701bc-d507-4299-b6b6-000000003472&quot;
   VersionId=&quot;*&quot;
   DisplayName=&quot;Contoso Accounts&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;/Packages&gt;
&lt;/AppConnectionGroup&gt;</code></pre></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Mit älteren Versionen als App-V 5,0 SP3</strong></p></td>
<td align="left"><p>Sie mussten viele Verbindungsgruppen erstellen, um bestimmte Anwendungen und Plug-in-Kombinationen für bestimmte Benutzer verfügbar zu machen.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-unpub-del-optl-pkg"></a>Aufheben der Veröffentlichung oder Löschen eines optionalen Pakets oder Aufheben der Veröffentlichung eines optionalen Pakets und erneutes veröffentlichen, ohne die Verbindungsgruppe zu ändern


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabenbeschreibung</th>
<th align="left">Durchführen der Aufgabe</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Mit App-v 5,0 SP3 und App-v 5,1</strong></p>
<p>Sie können ein optionales Paket, das sich in einer Verbindungsgruppe befindet, unveröffentlicht, löschen oder erneut veröffentlichen, ohne die Verbindungsgruppe auf dem App-V-Client deaktivieren oder erneut aktivieren zu müssen.</p>
<p>Sie können auch die Veröffentlichung eines optionalen Pakets aufheben und es später erneut veröffentlichen, ohne die Verbindungsgruppe deaktivieren oder erneut veröffentlichen zu müssen.</p>
<p><strong>Beispiel </strong> : Wenn Sie ein optionales Paket veröffentlichen, das ein Microsoft Office-Plug-in enthält, und Sie das Plug-in entfernen möchten, können Sie die Veröffentlichung des Pakets aufheben, ohne die Verbindungsgruppe deaktivieren zu müssen.</p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Methode</th>
<th align="left">Schritte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V Server – Verwaltungskonsole</p></td>
<td align="left"><ul>
<li><p>So heben Sie die Veröffentlichung des Pakets auf: Wählen Sie in der Verwaltungskonsole die Option Pakete auswählen aus <strong> </strong> , klicken oder klicken Sie mit der rechten Maustaste auf das Paket, dessen Veröffentlichung Sie aufheben möchten, und klicken Sie auf Veröffentlichung aufheben <strong> </strong> .</p></li>
<li><p>So entfernen Sie ein optionales Paket aus einer Verbindungsgruppe: Wählen Sie auf der <strong> Seite Verbindungsgruppen das Paket aus, das </strong> Sie entfernen möchten, und klicken Sie auf den Pfeil nach rechts, um das Paket aus dem Bereich Verbindungsgruppe unten links zu entfernen.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>App-V-Client auf einem eigenständigen Computer</p></td>
<td align="left"><p>Verwenden Sie die folgenden vorhandenen Cmdlets:</p>
<ul>
<li><p>Veröffentlichung aufheben – AppvClientPackage</p></li>
<li><p>Remove-AppvClientPackage</p></li>
</ul>
<p>Weitere Informationen finden Sie unter <a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"> Verwalten von App-V 5,1-Paketen, die mit PowerShell auf einem eigenständigen Computer ausgeführt werden </a> .</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Mit älteren Versionen als App-V 5,0 SP3</strong></p></td>
<td align="left"><p>Sie mussten Folgendes tun:</p>
<ol>
<li><p>Entfernen Sie die Verbindungsgruppe von jedem App-V-Client Computer, auf dem Sie aktiviert wurde.</p></li>
<li><p>Heben Sie die Veröffentlichung des Pakets auf.</p></li>
<li><p>Entfernen Sie das Paket aus der Definition der Verbindungsgruppe.</p></li>
<li><p>Veröffentlichen Sie die Verbindungsgruppe erneut.</p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqs-using-cg"></a>Voraussetzungen für die Verwendung optionaler Pakete in Verbindungsgruppen


Überprüfen Sie die folgenden Anforderungen, bevor Sie optionale Pakete in Verbindungsgruppen verwenden:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Anforderung</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Verbindungsgruppen müssen mindestens ein nicht optionales Paket enthalten.</p></td>
<td align="left"><ul>
<li><p>Überprüfen Sie sorgfältig, ob Sie diese Anforderung erfüllen, da der App-V-Server und das PowerShell-Cmdlet nicht überprüfen, ob die Anforderung erfüllt wurde.</p></li>
<li><p>Wenn Sie versehentlich eine Verbindungsgruppe erstellen, die nicht mindestens ein nicht optionales Paket enthält, und der Endbenutzer versucht, eine verpackte Anwendung in dieser Verbindungsgruppe zu öffnen, schlägt die Verbindungsgruppe fehl.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p>Von Benutzern veröffentlichte Verbindungsgruppen können Pakete enthalten, die Global oder für den Benutzer veröffentlicht werden.</p></li>
<li><p>Global veröffentlichte Verbindungsgruppen dürfen nur global veröffentlichte Pakete enthalten.</p></li>
</ul></td>
<td align="left"><p>Global veröffentlichte Verbindungsgruppen müssen Pakete enthalten, die Global veröffentlicht werden, um sicherzustellen, dass die Pakete beim Starten der virtuellen Umgebung der Verbindungsgruppe verfügbar sind.</p>
<p>Wenn Sie versuchen, Global veröffentlichte Verbindungsgruppen hinzuzufügen oder zu aktivieren, die von Benutzern veröffentlichte Pakete enthalten, schlägt die Verbindungsgruppe fehl.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sie müssen alle nicht optionalen Pakete veröffentlichen, bevor Sie die Verbindungsgruppe veröffentlichen, die diese Pakete enthält.</p></td>
<td align="left"><p>Die virtuelle Umgebung einer Verbindungsgruppe kann nicht gestartet werden, wenn nicht optionale Pakete fehlen.</p>
<p>Der App-V-Client kann keine Verbindungsgruppe hinzufügen oder aktivieren, wenn nicht optionale Pakete nicht veröffentlicht wurden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Bevor Sie die Veröffentlichung eines Global veröffentlichten Pakets aufheben, stellen Sie sicher, dass die Verbindungsgruppen, die für alle Benutzer auf diesem Computer berechtigt sind, das Paket nicht mehr benötigen.</p></td>
<td align="left"><p>Das System überprüft nicht, ob das Paket Teil der Verbindungsgruppe eines anderen Benutzers ist. Wenn die Veröffentlichung eines globalen Pakets aufgehoben wird, ist es für jeden Benutzer auf diesem Computer nicht mehr verfügbar, stellen Sie daher sicher, dass die Verbindungsgruppen des Benutzers das Paket nicht mehr enthalten, oder machen Sie das Paket optional.</p></td>
</tr>
</tbody>
</table>

 






## Verwandte Themen


[Verwalten von Verbindungsgruppen](managing-connection-groups51.md)

 

 





