---
title: Planen der Gruppen und Konten für MBAM 2.5
description: Planen der Gruppen und Konten für MBAM 2.5
author: dansimp
ms.assetid: 73bb9fe5-5900-4b6f-b271-ade62991fca1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 3431c3602685a4f96cb4c1333700107ba9c38b96
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811374"
---
# Planen der Gruppen und Konten für MBAM 2.5


In diesem Thema sind die Rollen und Konten aufgeführt, die Sie in Active Directory-Domänendiensten (AD DS) erstellen müssen, um Sicherheits-und Zugriffsrechte für die Microsoft BitLocker-Datenbanken,-Berichte und-Webanwendungen (MBAM) bereitzustellen. Für jede Rolle und jedes Konto wird das entsprechende Feld im MBAM-Serverkonfigurations-Assistenten bereitgestellt. Eine Liste der Windows PowerShell-Cmdlets und-Parameter, die diesen Konten entsprechen, finden Sie unter [Konfigurieren von MBAM 2,5-Server Features mithilfe von Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md#bkmk-reqd-posh-accts).

**Hinweis:**  
MBAM unterstützt nicht die Verwendung von verwalteten Dienstkonten.



## Daten Bankkonten


Erstellen Sie die folgenden Konten für die Compliance-und Überwachungsdatenbank sowie die Wiederherstellungsdatenbank.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name und Zweck des Kontos</th>
<th align="left">Kontotyp</th>
<th align="left">MBAM-Serverkonfigurations-Assistent-Feld, das diesem Konto entspricht</th>
<th align="left">Beschreibung des MBAM-Serverkonfigurations-Assistenten Felds, das diesem Konto entspricht</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Konformitäts-und Überwachungsdatenbank-und Wiederherstellungsdatenbank, Benutzer oder Gruppe für Berichte lesen/schreiben</p></td>
<td align="left"><p>Benutzer oder Gruppe</p></td>
<td align="left"><p>Lese/Schreib-Zugriffsdomänen Benutzer oder-Gruppe</p></td>
<td align="left"><p>Domänenbenutzer oder-Gruppe mit Lese-/Schreibzugriff auf die Datenbank für Konformitäts-und Überwachungsdaten und die Wiederherstellungsdatenbank, damit die Webanwendungen auf die Daten und Berichte in diesen Datenbanken zugreifen können.</p>
<p>Wenn Sie einen Benutzernamen in dieses Feld eingeben, muss er mit dem Wert im <strong> Feld "Domain-Konto" des Webdienst-Anwendungspools </strong> auf der <strong> Seite "Webanwendungen konfigurieren </strong> " identisch sein.</p>
<p>Wenn Sie einen Gruppennamen in dieses Feld eingeben, muss der Wert im <strong> Feld "Webdienst-Anwendungspool Domäne" </strong> auf der <strong> Seite "Webanwendungen konfigurieren" </strong> ein Mitglied der Gruppe sein, die Sie in dieses Feld eingeben.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Konformitäts-und Überwachungsdatenbank – schreibgeschützter Benutzer oder Gruppe für Berichte</p></td>
<td align="left"><p>Benutzer oder Gruppe</p></td>
<td align="left"><p>Schreibgeschützter Zugriffsdomänen Benutzer oder-Gruppe</p></td>
<td align="left"><p>Der Name des Benutzers oder der Gruppe, der schreibgeschützten Zugriff auf die Compliance-und Überwachungsdatenbank hat, damit die Berichte Zugriff auf die Compliance-und Überwachungsdaten in dieser Datenbank erhalten.</p>
<p>Wenn Sie einen Benutzernamen in dieses Feld eingeben, muss er derselbe Benutzer sein, den Sie im <strong> Feld Compliance und Audit Database Domain Account </strong> auf der <strong> Seite "Berichte konfigurieren" angeben </strong> .</p>
<p>Wenn Sie einen Gruppennamen in dieses Feld eingeben, muss der Wert, den Sie im <strong> Feld Compliance und Audit Database Domain Account angeben, </strong> auf der <strong> Seite "Berichte konfigurieren" </strong> ein Mitglied der Gruppe sein, die Sie in diesem Feld angeben.</p></td>
</tr>
</tbody>
</table>



## Berichterstellungskonten


Erstellen Sie die folgenden Konten für das Feature Berichte.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Kontoname/Zweck</th>
<th align="left">Kontotyp</th>
<th align="left">MBAM-Serverkonfigurations-Assistent-Feld, das diesem Konto entspricht</th>
<th align="left">Beschreibung des MBAM-Serverkonfigurations-Assistenten Felds, das diesem Konto entspricht</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Meldet schreibgeschützte Domänenzugriffs Gruppe</p></td>
<td align="left"><p>Gruppe</p></td>
<td align="left"><p>Gruppe "Berichtsrolle-Domäne"</p></td>
<td align="left"><p>Gibt die Domänenbenutzergruppe an, die schreibgeschützten Zugriff auf die Berichte auf der Website Verwaltung und Überwachung hat. Die von Ihnen angegebene Gruppe muss dieselbe Gruppe sein, die Sie für den Gruppenparameter schreibgeschützter Zugriff für Berichte angegeben haben, wenn die Web-Apps aktiviert sind.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Kompatibilitäts-und Überwachungsdatenbank-Domänenbenutzerkonto</p></td>
<td align="left"><p>Benutzer</p></td>
<td align="left"><p>Compliance-und Audit-Daten Bank Domänenkonto</p></td>
<td align="left"><p>Domänenbenutzerkonto und Kennwort, das von der lokalen SQL Server Reporting Services-Instanz für den Zugriff auf die Compliance-und Überwachungsdatenbank verwendet wird. Für dieses Konto ist <strong> die Anmeldung als Batch </strong> Berechtigung für den SQL Server Reporting Services-Server erforderlich.</p>
<p>Wenn der Wert, den Sie in das <strong> Feld "Schreibgeschützter Zugriffsdomänen Benutzer" oder "Gruppe" </strong> auf der <strong> Seite "Datenbanken konfigurieren </strong> " eingeben, ein Benutzername ist, müssen Sie diesen Wert in dieses Feld eingeben.</p>
<p>Wenn der Wert, den Sie in das <strong> Feld "Schreibgeschützter Zugriffsdomänen Benutzer" oder "Gruppe" </strong> auf der <strong> Seite "Datenbanken konfigurieren" eingeben </strong> , ein Gruppenname ist, muss der Wert, den Sie in dieses Feld eingeben, Mitglied dieser Gruppe sein.</p>
<p>Konfigurieren Sie das Kennwort für dieses Konto so, dass es nie abläuft. Das Benutzerkonto sollte auf alle Daten zugreifen können, die für die Gruppe MBAM-Berichte Benutzer verfügbar sind.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-helpdesk-roles"></a>Verwaltungs-und Überwachungs Website (Help Desk)-Konten


Erstellen Sie die folgenden Konten für die Website Verwaltung und Überwachung.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Kontoname/Zweck</th>
<th align="left">Kontotyp</th>
<th align="left">MBAM-Serverkonfigurations-Assistent-Feld, das diesem Konto entspricht</th>
<th align="left">Beschreibung des MBAM-Serverkonfigurations-Assistenten Felds, das diesem Konto entspricht</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Domänenkonto des Webdienst-Anwendungspools</p></td>
<td align="left"><p>Benutzer</p></td>
<td align="left"><p>Domänenkonto des Webdienst-Anwendungspools</p></td>
<td align="left"><p>Das Domänenbenutzerkonto, das vom Anwendungspool für die Webanwendungen verwendet werden soll.</p>
<p>Wenn Sie einen Benutzernamen in das <strong> Feld Lese/Schreibzugriff-Domänenbenutzer oder-Gruppe </strong> auf der <strong> Seite Datenbanken konfigurieren eingeben </strong> , müssen Sie diesen Wert in dieses Feld eingeben.</p>
<p>Wenn Sie einen Gruppennamen in das <strong> Feld Lese-/Schreibzugriff-Domänenbenutzer oder-Gruppe </strong> auf der <strong> Seite Datenbanken konfigurieren eingeben </strong> , muss der in dieses Feld eingegebene Wert ein Mitglied dieser Gruppe sein.</p>
<p>Wenn Sie keine Anmeldeinformationen angeben, werden die Anmeldeinformationen verwendet, die für eine zuvor aktivierte Webanwendung angegeben wurden. Alle Webanwendungen müssen die gleichen Anmeldeinformationen für den Anwendungspool verwenden. Wenn Sie für verschiedene Webanwendungen unterschiedliche Anmeldeinformationen angeben, wird der zuletzt angegebene Wert verwendet.</p>
<div class="alert">
<strong>Wichtig</strong><br/><p>Um die Sicherheit zu verbessern, legen Sie das in den Anmeldeinformationen angegebene Konto auf begrenzte Benutzerrechte fest.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM Advanced Helpdesk users Access Group</p></td>
<td align="left"><p>Gruppe</p></td>
<td align="left"><p>MBAM Advanced Helpdesk-Benutzer</p></td>
<td align="left"><p>Domänenbenutzergruppe, deren Mitglieder Zugriff auf alle Wiederherstellungs Bereiche der Website "Verwaltung und Überwachung" haben. Benutzer, die über diese Rolle verfügen, müssen nur den Wiederherstellungsschlüssel und nicht die Domäne und den Benutzernamen des Endbenutzers eingeben, wenn Sie den Endbenutzern helfen, Ihre Laufwerke wiederherzustellen. Wenn ein Benutzer ein Mitglied der Gruppe MBAM Helpdesk-Benutzer und der Gruppe der erweiterten Helpdesk-Benutzer von MBAM ist, überschreiben die Berechtigungen der Gruppe erweiterte Helpdesk-Benutzer MBAM die Berechtigungen für die MBAM-Helpdesk-Gruppe.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM Helpdesk-Benutzerzugriffs Gruppe</p></td>
<td align="left"><p>Gruppe</p></td>
<td align="left"><p>MBAM Helpdesk-Benutzer</p></td>
<td align="left"><p>Die Domänenbenutzergruppe, deren Mitglieder Zugriff auf die Bereiche "TPM verwalten" und "Laufwerk Wiederherstellung" der Website "MBAM-Verwaltung und-Überwachung" haben. Personen, die über diese Rolle verfügen, müssen alle Felder ausfüllen, einschließlich der Domäne und des Kontonamens des Endbenutzers, wenn beide Optionen verwendet werden.</p>
<p>Wenn ein Benutzer ein Mitglied der Gruppe MBAM Helpdesk-Benutzer und der Gruppe der erweiterten Helpdesk-Benutzer von MBAM ist, überschreiben die Berechtigungen der Gruppe erweiterte Helpdesk-Benutzer MBAM die Berechtigungen für die MBAM-Helpdesk-Gruppe.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM-Berichtsbenutzer (Access-Gruppe)</p></td>
<td align="left"><p>Gruppe</p></td>
<td align="left"><p>MBAM-Berichtsbenutzer</p></td>
<td align="left"><p>Domänenbenutzergruppe, deren Mitglieder schreibgeschützten Zugriff auf die Berichte im Bereich "Berichte" der Website "Verwaltung und Überwachung" haben.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM-Benutzergruppe für die Daten Migration</p></td>
<td align="left"><p>Gruppe</p></td>
<td align="left"><p>Benutzer von MBAM-Daten Migration</p></td>
<td align="left"><p>Optionale Domänenbenutzergruppe, deren Mitglieder über die Berechtigungen zum Schreiben von Daten in MBAM verfügen, indem Sie den MBAM-Wiederherstellungs-und Hardware Dienst verwenden, der auf dem MBAM-Server ausgeführt wird. Dieses Konto wird in der Regel für die Write-mbam *-Cmdlets verwendet, um Wiederherstellungs-und TPM-Daten aus Active Directory in die mbam-Datenbank zu schreiben.</p>
<p>Weitere Informationen finden Sie unter <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> Sicherheitsüberlegungen zu MBAM 2,5 </a> .</p></td>
</tr>
</tbody>
</table>




## Verwandte Themen


[Vorbereiten der Umgebung für MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Bereitstellungsvoraussetzungen für MBAM 2.5](mbam-25-deployment-prerequisites.md)



## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





