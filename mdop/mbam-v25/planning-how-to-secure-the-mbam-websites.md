---
title: Planen der Sicherung von MBAM-Websites
description: Planen der Sicherung von MBAM-Websites
author: dansimp
ms.assetid: aea1d137-62cf-4da4-9989-541e0b5ad8d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 223c9397ad7933e11051c289c3dbcab63940fbc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810906"
---
# Planen der Sicherung von MBAM-Websites


In diesem Thema werden die folgenden Methoden zum Sichern der Microsoft BitLocker-Verwaltungs-und-Überwachungs Website (MBAM) 2,5-Website und des Self-Service-Portals beschrieben:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Methode</th>
<th align="left">Erforderlich oder optional?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Verwenden von Zertifikaten zum Sichern von MBAM-Websites</p></td>
<td align="left"><p>Optional, aber sehr empfehlenswert</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registrieren von Dienstprinzipalnamen (Service Principal Names, SPN) für das Anwendungspoolkonto</p></td>
<td align="left"><p>Erforderlich</p></td>
</tr>
</tbody>
</table>



Weitere Informationen zum Sichern Ihrer MBAM-Bereitstellung finden Sie unter [Sicherheitsüberlegungen zu MBAM 2,5](mbam-25-security-considerations.md).

## Verwenden von Zertifikaten zum Sichern von MBAM-Websites


Wir empfehlen, dass Sie ein Zertifikat verwenden, um die Kommunikation zwischen den folgenden zu sichern:

-   MBAM-Client und die Webdienste

-   Browser und die Website "Verwaltung und Überwachung" sowie die Websites des Self-Service-Portals

Informationen zum Anfordern und Installieren eines Zertifikats finden Sie unter [Konfigurieren von Internet Server Zertifikaten](https://technet.microsoft.com/library/cc731977.aspx).

**Hinweis:**  
Sie können die Websites und Webdienste auf unterschiedlichen Servern nur konfigurieren, wenn Sie Windows PowerShell verwenden. Wenn Sie den MBAM-Serverkonfigurations-Assistenten zum Konfigurieren der Websites verwenden, müssen Sie die Websites und die Webdienste auf demselben Server konfigurieren.



Um die Kommunikation zwischen den Webdiensten und den Datenbanken zu sichern, sollten Sie auch die Verschlüsselung in SQL Server erzwingen. Informationen zum Sichern aller Verbindungen mit SQL Server, einschließlich der Kommunikation zwischen den Webdiensten und SQL Server, finden Sie unter [MBAM 2,5-Sicherheitsüberlegungen](mbam-25-security-considerations.md#bkmk-secure-databases).

## Registrieren von SPNs für das Anwendungspoolkonto


Damit die MBAM-Server die Kommunikation über die Verwaltungs-und Überwachungs Website und das Self-Service-Portal authentifizieren können, müssen Sie einen Dienstprinzipalnamen (Service Principal Name, SPN) für den Hostnamen unter dem Domänenkonto registrieren, das Sie für den Webanwendungspool verwenden.

In diesem Thema finden Sie Anweisungen zum Registrieren von SPNs für die folgenden Typen von Host Namen:

-   Vollständig qualifizierter Domänenname

-   NetBIOS-Name

-   Virtueller Name

### Vor dem Erstellen von SPNs für eine anfängliche MBAM-Installation

Überprüfen Sie die Informationen in der folgenden Tabelle, bevor Sie mit dem Erstellen von SPNs beginnen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabe oder Element</th>
<th align="left">Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Erstellen Sie ein Dienstkonto in Active Directory-Domänendienste (AD DS).</p></td>
<td align="left"><p>Das Dienstkonto ist ein Benutzerkonto, das Sie in AD DS erstellen, um Sicherheit für die MBAM-Websites bereitzustellen. Die MBAM-Websites werden unter einem Anwendungspool ausgeführt, dessen Identität der Name des Dienstkontos ist. Die SPNs werden dann im Anwendungspoolkonto registriert.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Sie müssen dasselbe Anwendungspoolkonto für alle Webserver verwenden.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Vergewissern Sie sich, dass entweder das IIS-IUSRS-Gruppenkonto oder das Anwendungspoolkonto über die erforderlichen Rechte verfügen.</p></td>
<td align="left"><p>Führen Sie die folgenden Schritte aus, um dies zu überprüfen:</p>
<ol>
<li><p>Öffnen Sie den <strong> lokalen Sicherheitsrichtlinien-Editor </strong> , und erweitern Sie den <strong> Knoten Lokale Richtlinien </strong> .</p></li>
<li><p>Wählen Sie den <strong> Knoten Benutzerrechtezuweisung aus </strong> , und doppelklicken Sie <strong> im rechten Bereich auf die Gruppenrichtlinieneinstellungen für den Identitätswechsel eines Clients nach Authentifizierung </strong> und <strong> Anmeldung als Stapelverarbeitungsauftrag </strong> .</p></li>
</ol></td>
</tr>
<tr class="odd">
<td align="left"><p>Wenn Sie die MBAM-Websites mithilfe eines Domänenadministratorkontos konfigurieren, erstellt MBAM die SPNs für Sie.</p></td>
<td align="left"><p>Wenn Sie die MBAM-Websites mithilfe eines Domänenadministratorkontos konfigurieren, führen Sie die Schritte in diesem Thema aus, um SPNs für den Typ des verwendeten Hostnamens manuell zu registrieren.</p></td>
</tr>
</tbody>
</table>



### Registrieren von SPNs, wenn Sie einen vollqualifizierten Domänenhost Namen verwenden

Wenn Sie bei der Konfiguration von MBAM einen vollqualifizierten Domänenhost Namen verwenden, müssen Sie nur einen SPN registrieren, wie im folgenden Beispiel gezeigt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Was Sie tun müssen</th>
<th align="left">Beispiele und weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Registrieren Sie einen SPN für den vollqualifizierten Domänennamen.</p></td>
<td align="left"><p><code>Setspn -s http/mybitlockerrecovery.contoso.com contoso\mbamapppooluser</code></p>
<p>Der vollqualifizierte Hostname lautet <strong> mybitlockerrecovery.contoso.com </strong> , und das für den Webanwendungspool verwendete Domänenkonto ist <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Konfigurieren Sie die beschränkte Delegierung für den SPN, den Sie für das Anwendungspoolkonto registrieren.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)">Konfigurieren der beschränkten Delegierung</a></p>
<p>Diese Anforderung gilt nur für MBAM 2,5; in MBAM 2,5 SP1 ist dies nicht erforderlich.</p></td>
</tr>
</tbody>
</table>



### Registrieren von SPNs bei Verwendung eines NetBIOS-Hostnamens

Wenn Sie bei der Konfiguration von MBAM einen NetBIOS-Hostnamen verwenden, registrieren Sie einen SPN für den NetBIOS-Namen und einen weiteren SPN für den vollqualifizierten Domänennamen, wie in den folgenden Beispielen dargestellt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Was Sie tun müssen</th>
<th align="left">Beispiele und weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Registrieren Sie einen SPN für den NetBIOS-Host Namen.</p></td>
<td align="left"><p><code>Setspn -s http/nbname01 contoso\mbamapppooluser</code></p>
<p>Der NetBIOS-Hostname lautet <strong> nbname01 </strong> , und das für den Webanwendungspool verwendete Domänenkonto ist <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registrieren Sie einen SPN für den vollqualifizierten Domänennamen.</p></td>
<td align="left"><p><code>Setspn –s http/nbname01.corp.contoso.com contoso\mbamapppooluser</code></p>
<p>Der vollqualifizierte Domänenname lautet <strong> nbname01.contoso.com </strong> , und das für den Webanwendungspool verwendete Domänenkonto ist <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Konfigurieren Sie die beschränkte Delegierung für die SPNs, die Sie für das Anwendungspoolkonto registrieren.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)">Konfigurieren der beschränkten Delegierung</a></p>
<p>Diese Anforderung gilt nur für MBAM 2,5; in MBAM 2,5 SP1 ist dies nicht erforderlich.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-regvirtualspn"></a>Registrieren von SPNs bei Verwendung eines virtuellen Hostnamens

Wenn Sie MBAM mit einem virtuellen Hostnamen konfigurieren, bei dem es sich um einen vollqualifizierten Domänennamen handelt, registrieren Sie nur einen SPN für den virtuellen Host Namen. Wenn es sich bei dem von Ihnen konfigurierten virtuellen Host Namen nicht um einen vollqualifizierten Domänennamen handelt, müssen Sie einen zweiten SPN erstellen, der den vollqualifizierten Domänennamen angibt, wie in den folgenden Beispielen beschrieben.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Was Sie tun müssen</th>
<th align="left">Beispiele und weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Wenn der Name Ihres virtuellen Hosts ein vollständig qualifizierter Domänenname ist, wie in diesem Beispiel, registrieren Sie nur einen SPN.</p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p>Im Beispiel lautet der Name des virtuellen Hosts <strong> mbamvirtual.contoso.com </strong> , und das für den Webanwendungspool verwendete Domänenkonto ist <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registrieren Sie diesen zusätzlichen SPN, wenn der Name Ihres virtuellen Hosts kein vollqualifizierter Domänenname ist.</p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser</code></p>
<p>Im Beispiel lautet der Name des virtuellen Hosts <strong> mbamvirtual </strong> , und das für den Webanwendungspool verwendete Domänenkonto ist <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registrieren Sie diesen zusätzlichen SPN, wenn der Name Ihres virtuellen Hosts kein vollqualifizierter Domänenname ist.</p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p>Im Beispiel lautet der Name des virtuellen Hosts <strong> mbamvirtual.contoso.com </strong> , und das für den Webanwendungspool verwendete Domänenkonto ist <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Erstellen Sie auf dem Domain Nameserver (DNS)-Server einen "A Record" für den benutzerdefinierten Hostnamen, und verweisen Sie auf einen Webserver oder ein Lastenausgleichsmodul.</p></td>
<td align="left"><p>Weitere Informationen finden Sie im Abschnitt "so konfigurieren Sie einen DNS-Host für Datensätze" unter <a href="https://go.microsoft.com/fwlink/?LinkId=394337" data-raw-source="[Configure DNS Host Records](https://go.microsoft.com/fwlink/?LinkId=394337)"> Konfigurieren von DNS-Hosteinträgen </a> .</p>
<p>Wir empfehlen, anstelle von CNAMEs Datensätze zu verwenden. Wenn Sie CNAMEs verwenden, um auf die Domänenadresse zu verweisen, müssen Sie auch SPNs für den Webservernamen im Anwendungspoolkonto registrieren.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Konfigurieren Sie die beschränkte Delegierung für die SPNs, die Sie für das Anwendungspoolkonto registrieren.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)">Konfigurieren der beschränkten Delegierung</a></p>
<p>Diese Anforderung gilt nur für MBAM 2,5; in MBAM 2,5 SP1 ist dies nicht erforderlich.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-registerspn"></a>Registrieren eines SPN beim Upgrade von vorherigen Versionen von MBAM

Führen Sie die Schritte in diesem Abschnitt nur aus, wenn Sie Folgendes tun möchten:

-   Upgrade von einer früheren Version von MBAM.

-   Führen Sie die Websites in MBAM 2,5 in einer Lastenausgleichs-oder verteilten Konfiguration aus, und Sie werden derzeit in einer Konfiguration ausgeführt, die nicht Lastenausgleich ist.

Wenn Sie SPNs bereits auf dem Computerkonto und nicht in einem Anwendungspoolkonto registriert haben, verwendet MBAM die vorhandenen SPNs, und Sie können die Websites nicht in einer Lastenausgleich-oder verteilten Konfiguration konfigurieren.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Was Sie tun müssen</th>
<th align="left">Beispiele und weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Erstellen Sie ein Anwendungspoolkonto in Active Directory-Domänendienste (AD DS).</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Entfernen Sie die aktuell installierten Websites und Webdienste.</p></td>
<td align="left"><p><a href="removing-mbam-server-features-or-software.md" data-raw-source="[Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md)">Entfernen von MBAM-Serverfunktionen oder -software</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Entfernen Sie SPNs aus dem Computerkonto.</p></td>
<td align="left"><p><code>Setspn –d http/mbamwebserver mbamwebserver</code></p>
<p><code>Setspn –d http/mbamwebserver.contoso.com mbamwebserver</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>Registrieren Sie SPNs im Anwendungspoolkonto.</p></td>
<td align="left"><p>Führen Sie die Schritte zum <a href="#bkmk-regvirtualspn" data-raw-source="[Registering SPNs when you use a virtual host name](#bkmk-regvirtualspn)"> Registrieren von SPNs aus, wenn Sie einen virtuellen Hostnamen verwenden </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Konfigurieren Sie die Web Applications und Web Services neu.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">So konfigurieren Sie die MBAM 2.5-Webanwendungen</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Führen Sie je nach der für die Konfiguration verwendeten Methode eine der folgenden Aktionen aus:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Methode</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>MBAM-Serverkonfigurations-Assistent</strong></p></td>
<td align="left"><p>Geben Sie das Anwendungspoolkonto im <strong> Feld "Domänenkonto" des Webdienst-Anwendungspools ein </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><code>Enable-MbamWebApplication</code> Windows PowerShell-Cmdlet</p></td>
<td align="left"><p>Geben Sie das Konto in den <code>WebServiceApplicationPoolCredential</code> Parameter ein.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
<td align="left"><div class="alert">
<strong>Wichtig</strong><br/><p>Der eingegebene Hostname muss mit dem Namen des virtuellen Hosts identisch sein, für den Sie die SPNs erstellen. Außerdem müssen die Hostnamen und die Anmeldeinformationen des Anwendungspools in Ihrer Webfarm auf jedem Server identisch sein, den Sie konfigurieren.</p>
</div>
<div>

</div>
<p>Wenn MBAM die Webanwendungen konfiguriert, versucht Sie, die SPNs für Sie zu registrieren, kann dies aber nur tun, wenn Sie über Domänenadministratorrechte auf dem Server verfügen, auf dem Sie MBAM installieren. Wenn Sie nicht über diese Rechte verfügen, können Sie die Konfiguration abschließen, aber Sie müssen die SPNs vor oder nach dem Konfigurieren von MBAM festlegen.</p></td>
</tr>
</tbody>
</table>

## Erforderliche Filtereinstellungen für Anforderungen

 "Nicht aufgelistete Dateinamenerweiterungen zulassen" ist erforderlich, damit die Anwendung wie erwartet funktioniert.  Diese finden Sie unter "Microsoft BitLocker-Verwaltung und-Überwachung" – > Anforderungsfilterung – > Featureeinstellungen bearbeiten.


## Verwandte Themen


[Vorbereiten der Umgebung für MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Bereitstellungsvoraussetzungen für MBAM 2.5](mbam-25-deployment-prerequisites.md)





## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).



