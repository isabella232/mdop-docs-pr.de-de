---
title: Aktualisieren von MBAM 2.5 oder MBAM 2.5 SP1 von früheren Versionen
description: Aktualisieren von MBAM 2.5 oder MBAM 2.5 SP1 von früheren Versionen
author: dansimp
ms.assetid: a9edb4b8-5d5e-42ab-8db6-619db2878e50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 07a03ebbbfce45f7f69a85000e18ddf1a58e53ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804463"
---
# Aktualisieren von MBAM 2.5 oder MBAM 2.5 SP1 von früheren Versionen


In diesem Thema wird der Vorgang zum Aktualisieren des Microsoft BitLocker-Verwaltungs-und Überwachungsservers (MBAM) und des MBAM-Clients aus früheren Versionen von MBAM beschrieben.

**Hinweis**  Sie können ein Upgrade direkt auf MBAM 2,5 oder MBAM 2,5 SP1 aus einer beliebigen vorherigen Version von MBAM durchführen.

 

## Vor dem Starten des Upgrades


Überprüfen Sie die folgenden Informationen, bevor Sie mit dem Upgrade beginnen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Was Sie wissen sollten, bevor Sie beginnen</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Wenn Sie die MBAM-Websites auf einem Server und die Webdienste auf einem anderen Server installieren, müssen Sie Windows PowerShell-Cmdlets verwenden, um Sie zu konfigurieren.</p></td>
<td align="left"><p>Der MBAM-Serverkonfigurations-Assistent unterstützt nicht die Konfiguration der Websites auf einem Server und die Webdienste auf einem anderen Server.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Wenn Sie ein Upgrade auf mbam 2.5 oder 2,5 SP1 von mbam 2.0 oder 2,0 SP1 in Windows Server2008 R2 ausführen:</p>
<p>Die Verwaltungs-und Überwachungs Website und das Self-Service-Portal funktionieren nicht, wenn Sie die erforderliche .NET Framework 4.5-Software installieren, nachdem Internet Informationsdienste (IIS) bereits installiert ist.</p>
<p>Dieses Problem tritt auf, weil ASP.net bei IIS nicht ordnungsgemäß registriert werden kann, wenn .NET Framework installiert ist, nachdem IIS bereits installiert wurde.</p></td>
<td align="left"><p><strong>So beheben Sie dieses Problem:</strong></p>
<p>Führen Sie <strong> aspnet_regiis – i </strong> von folgendem Speicherort aus:</p>
<p>C:\windows\microsoft.net\Framework\v4.0.30319</p>
<p>Weitere Informationen finden Sie unter: <a href="https://go.microsoft.com/fwlink/?LinkId=393272" data-raw-source="[ASP.NET IIS Registration Tool](https://go.microsoft.com/fwlink/?LinkId=393272)"> ASP.NET IIS-Registrierungs Tool </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registrieren Sie einen SPN für das Anwendungspoolkonto, wenn alle folgenden Bedingungen erfüllt sind:</p>
<ul>
<li><p>Sie aktualisieren eine frühere Version von MBAM.</p></li>
<li><p>Zurzeit führen Sie die MBAM-Websites nicht in einer Lastenausgleichs-oder verteilten Konfiguration aus, aber Sie möchten dies beim Upgrade auf MBAM 2.5 oder 2,5 SP1 tun.</p></li>
</ul></td>
<td align="left"><p>Anweisungen hierzu finden Sie unter <a href="planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn)"> Planen der Sicherung der MBAM-Websites </a> .</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Was wir empfehlen</strong></p></td>
<td align="left"><p>Registrieren Sie einen Dienstprinzipalnamen (Service Principal Name, SPN) für das Anwendungspoolkonto, obwohl Sie möglicherweise bereits über registrierte SPNs für das Computerkonto verfügen.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Warum wir es empfehlen</strong></p></td>
<td align="left"><p>Das Registrieren eines SPN für das Anwendungspoolkonto ist erforderlich, um die Websites in einer Lastenausgleich-oder verteilten Konfiguration zu konfigurieren.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Was geschieht, wenn SPNs bereits für ein Computerkonto konfiguriert sind?</strong></p></td>
<td align="left"><p>MBAM verwendet die SPNs, die Sie bereits registriert haben, und Sie müssen keine zusätzlichen SPNs konfigurieren, aber Sie können die Websites nicht in einer Lastenausgleich-oder verteilten Konfiguration konfigurieren.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## Schritte zum Upgrade der MBAM-Server Infrastruktur


Führen Sie die Schritte in den folgenden Abschnitten aus, um MBAM für die eigenständige Topologie oder die System Center Configuration Manager-Integrations Topologie zu aktualisieren.

**So aktualisieren Sie die MBAM-Server Infrastruktur für eigenständige Topologie**

1.  Deinstallieren Sie frühere Versionen von MBAM aus **Programmen und Funktionen** sowie von Webservern, um sicherzustellen, dass Informationen nicht von MBAM-Clients in die MBAM-Infrastruktur geschrieben werden. Anweisungen hierzu finden Sie unter [Entfernen von MBAM-Server Features oder Software](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).

2.  Sichern Sie Ihre Datenbanken.

3.  Deinstallieren Sie frühere Versionen von MBAM von SQL Server mithilfe von **Programmen und Features**, einschließlich SQL-Servern, die die MBAM-Berichte über SQL Server Reporting Services hosten. Entfernen Sie alle verbleibenden temporären MBAM Server-Dateien oder-Ordner aus dem Datenbankserver und Reporting Services.

    **Hinweis**  Die Datenbankenwerden nicht entfernt, und alle Kompatibilitäts-und Wiederherstellungsdaten werden in der Datenbank verwaltet.

     

4.  Installieren und konfigurieren Sie die mbam 2.5-oder 2,5 SP1-Datenbanken,-Berichte und-Webanwendungen in dieser Reihenfolge. Die Datenbankenwerden direkt aktualisiert.

5.  Aktualisieren Sie die Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) mithilfe der MBAM 2,5-Vorlagen, um die neuen Features in MBAM, wie erzwungene Verschlüsselung, zu nutzen. Wenn Sie die GPOs und den MBAM-Client nicht auf MBAM 2,5 aktualisieren, werden frühere Versionen von MBAM-Clients weiterhin mit eingeschränkter Funktionalität gegen ihre aktuellen GPOs gemeldet. Informationen zum Herunterladen der neuesten ADMX-Vorlagen finden Sie unter [Abrufen von MDOP-Gruppenrichtlinien (ADMX)](https://www.microsoft.com/download/details.aspx?id=41183) .

    Nachdem Sie die MBAM-Serverinfrastruktur aktualisiert haben, werden die vorhandenen Clientcomputer weiterhin erfolgreich an den MBAM 2.5-oder 2,5 SP1-Server gemeldet, und die Wiederherstellungsdaten werden weiterhin gespeichert.

6.  Installieren Sie den neuesten mbam 2.5-oder 2,5 SP1-Client. Client Computer müssen nach der Bereitstellung nicht neu gestartet werden.

**So aktualisieren Sie die MBAM-Infrastruktur für die System Center Configuration Manager-Integrations Topologie**

1.  Deinstallieren Sie frühere Versionen von MBAM aus **Programmen und Funktionen** sowie von Webservern, um sicherzustellen, dass Informationen nicht von MBAM-Clients in die MBAM-Infrastruktur geschrieben werden. Anweisungen hierzu finden Sie unter [Entfernen von MBAM-Server Features oder Software](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).

2.  Sichern Sie Ihre Datenbanken.

3.  Deinstallieren Sie frühere Versionen von MBAM von SQL Server mithilfe von **Programmen und Features**, einschließlich SQL-Servern, die die MBAM-Berichte über SQL Server Reporting Services hosten. Entfernen Sie alle verbleibenden temporären MBAM Server-Dateien oder-Ordner aus dem Datenbankserver und Reporting Services.

4.  Deinstallieren Sie MBAM vom Configuration Manager-Server.

    **Hinweis**  Die Datenbanken und die Configuration Manager-Objekte (Baseline, MBAM unterstützte Computersammlung und Berichte) werden nicht entfernt, und alle Kompatibilitäts-und Wiederherstellungsdaten werden in der Datenbank verwaltet.

     

5.  Aktualisieren Sie die MOF-Dateien.

6.  Installieren und konfigurieren Sie die mbam 2.5-oder 2,5 SP1-Datenbanken,-Berichte,-Webanwendungen und die Configuration Manager-Integration in dieser Reihenfolge. Die Datenbanken und Configuration Manager-Objekte werden direkt aktualisiert.

7.  Aktualisieren Sie optional die Gruppenrichtlinienobjekte (Group Policy Objects, GPOs), und bearbeiten Sie die Einstellungen, wenn Sie neue Features in MBAM implementieren möchten, beispielsweise erzwungene Verschlüsselung. Wenn Sie die GPOs nicht aktualisieren, wird MBAM weiterhin für Ihre aktuellen GPOs gemeldet. Informationen zum Herunterladen der neuesten ADMX-Vorlagen finden Sie unter [Abrufen von MDOP-Gruppenrichtlinien (ADMX)](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates) .

    Nachdem Sie die MBAM-Serverinfrastruktur aktualisiert haben, werden die vorhandenen Clientcomputer weiterhin erfolgreich an den MBAM 2.5-oder 2,5 SP1-Server gemeldet, und die Wiederherstellungsdaten werden weiterhin gespeichert.

8.  Installieren Sie den neuesten mbam 2.5-oder 2,5 SP1-Client. Client Computer müssen nach der Bereitstellung nicht neu gestartet werden.

## Upgrade-Unterstützung für den MBAM-Client


MBAM unterstützt Upgrades auf den MBAM 2.5-Client aus einer früheren Version des MBAM-Clients.

**Möglichkeiten zum Installieren des MBAM-Clients:**

-   Aktualisieren Sie die Computer, auf denen der MBAM-Client ausgeführt wird, alle auf einmal oder schrittweise nach der Installation der MBAM 2.5-Server Infrastruktur.

-   Installieren Sie den MBAM-Client über ein elektronisches Softwareverteilungssystem oder über Tools wie Active Directory-Domänendienste oder System Center Configuration Manager.



## Verwandte Themen


[Bereitstellen von MBAM 2.5](deploying-mbam-25.md)

[Bereitstellen des MBAM 2.5-Clients](deploying-the-mbam-25-client.md)

[Konfigurieren der MBAM 2.5-Serverfunktionen](configuring-the-mbam-25-server-features.md)

 

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





