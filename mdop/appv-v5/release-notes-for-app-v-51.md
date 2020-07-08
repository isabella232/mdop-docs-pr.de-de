---
title: Versionshinweise für App-V 5.1
description: Versionshinweise für App-V 5.1
author: dansimp
ms.assetid: 62c5be3b-0a46-4512-93ed-97c23184f343
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/26/2016
ms.openlocfilehash: 7437a16bc10b21bb15b0f8307c2711177e78cb72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804880"
---
# Versionshinweise für App-V 5.1


Im folgenden werden bekannte Probleme in Microsoft Application Virtualization (App-V) 5,1.

## Beim Aktualisieren der Veröffentlichung zwischen App-v 5,0 SP3-Verwaltungs Server und App-v 5,1-Client unter Windows 10 tritt ein Fehler auf.


Beim Synchronisieren von Paketen vom APP-v 5,0 SP3-Verwaltungsserver zu einem App-v 5,1-Client unter Windows 10 wird ein Fehler während der Veröffentlichungsaktualisierung generiert. Dieser Fehler tritt auf, weil der App-V 5,0 SP3-Server das Windows 10-Betriebssystem nicht versteht, das in der Veröffentlichungs-URL angegeben ist. Das Problem wurde für den App-v 5,1-Veröffentlichungsserver behoben, wird jedoch nicht in Versionen von App-v 5,0 SP3 oder früher portiert.

**Problemumgehung**: Aktualisieren Sie den App-v 5,0-Verwaltungsserver auf den App-v 5,1-Verwaltungsserver für Windows 10-Clients.

## Benutzerdefinierte Konfigurationen werden nicht auf Pakete angewendet, die Global veröffentlicht werden, wenn Sie mit dem App-V 5,1-Server festgesetzt werden.


Wenn Sie einer Anzeigengruppe, die Computerkonten enthält, ein Paket zuweisen und eine benutzerdefinierte Konfiguration mit dem App-V-Server auf diese Gruppe anwenden, wird die benutzerdefinierte Konfiguration nicht auf diese Computer angewendet. Der App-V 5,1-Client veröffentlicht Pakete, die einem Computerkonto Global zugewiesen sind. Es werden jedoch benutzerdefinierte Konfigurationsdateien pro Benutzer im Profil jedes Benutzers gespeichert. Global veröffentlichte Pakete haben keinen Zugriff auf diese benutzerdefinierte Konfiguration.

**Problemumgehung**: führen Sie eine der folgenden Aktionen aus:

-   Weisen Sie das Paketgruppen zu, die nur Benutzerkonten enthalten. Dadurch wird sichergestellt, dass die benutzerdefinierte Konfiguration des Pakets in den Profilen jedes Benutzers gespeichert wird und ordnungsgemäß angewendet wird.

-   Erstellen Sie eine benutzerdefinierte Konfigurationsdatei für die Bereitstellung, und wenden Sie Sie auf das Paket auf dem Client mithilfe des Cmdlets "Add-AppvClientPackage" mit dem Parameter "– DynamicDeploymentConfiguration" an. Weitere Informationen finden Sie unter Informationen [zur dynamischen Konfiguration von App-V 5,1](about-app-v-51-dynamic-configuration.md) .

-   Erstellen Sie ein neues Paket mit der benutzerdefinierten Konfiguration mit dem App-V 5,1-Sequenzer.

## Server Dateien werden nach der Installation der neuen App-V 5,1-Server nicht gelöscht


Wenn Sie den App-v 5,0 SP1-Server deinstallieren und dann den App-v 5,1-Server installieren, schlägt die Installation fehl, die falsche Version des Verwaltungsservers wird installiert, und es wird eine Fehlermeldung zurückgegeben. Das Problem tritt auf, weil die Server Dateien nicht gelöscht werden, wenn Sie App-V 5,0 SP1 deinstallieren, sodass der Installationsvorgang anstelle einer neuen Installation ein Upgrade durchführt.

**Problemumgehung**: Löschen Sie diesen Registrierungsschlüssel, bevor Sie mit der Installation von App-V 5,1 beginnen:

Suchen und löschen Sie unter HKEY \ _LOCAL \ _MACHINE \\software\\wow6432node\\microsoft\\windows\\currentversion\\uninstall den Installations-GUID-Schlüssel, der den DWORD-Wert "DisplayName" mit dem Wert "Microsoft Application Virtualization (App-V) Server" enthält. Dies ist der einzige Schlüssel, der gelöscht werden soll.

## Manuell hinzugefügte Dateitypen Zuordnungen werden nicht ordnungsgemäß gespeichert


Dateitypzuordnungen, die einem Anwendungspaket manuell mithilfe der Registerkarte Verknüpfungen und FTA am Ende des Anwendungs Aktualisierungs-Assistenten hinzugefügt wurden, werden nicht ordnungsgemäß gespeichert. Sie stehen dem App-V-Client oder dem Sequencer beim erneuten Aktualisieren des gespeicherten Pakets nicht zur Verfügung.

**Problemumgehung**: Wenn Sie eine Dateitypzuordnung hinzufügen möchten, öffnen Sie das Paket zur Änderung, und führen Sie den Update-Assistenten aus. Fügen Sie während des Installationsschritts die neue Dateitypzuordnung über das Betriebssystem hinzu. Der Sequencer erkennt die neue Zuordnung in der Systemregistrierung und fügt Sie der virtuellen Registrierung des Pakets hinzu, wo Sie für den Client verfügbar ist.

## Beim Streaming von Paketen im freigegebenen Inhaltsspeicher (SCS)-Modus zu einem Client, der auch mit AppLocker verwaltet wird, werden zusätzliche Daten auf den lokalen Datenträger geschrieben.


Um die Menge der auf den lokalen Datenträger des Clients geschriebenen Daten zu verringern, können Sie den SCS-Modus auf dem App-V 5,1-Client aktivieren, um den Inhalt eines Pakets bei Bedarf zu streamen. Wenn AppLocker jedoch eine Anwendung innerhalb des Pakets verwaltet, werden möglicherweise einige Daten auf den lokalen Datenträger des Clients geschrieben, die sonst nicht geschrieben werden.

**Problemumgehung**: keine

## Im Dialogfeld "Management Console-Paket hinzufügen" steht die Schaltfläche "Durchsuchen" bei Verwendung von Chrome oder Firefox nicht zur Verfügung.


Wenn Sie auf der Seite Pakete der Verwaltungskonsole in der unteren rechten Ecke auf **Hinzufügen oder aktualisieren** klicken, wird das Dialogfeld **Paket hinzufügen** angezeigt. Wenn Sie mit Chrome oder Firefox als Browser auf die Verwaltungskonsole zugreifen, können Sie nicht zum Speicherort des Pakets navigieren.

**Problemumgehung**: Geben Sie den Pfad des Pakets in das Eingabefeld **Paket hinzufügen** ein, oder kopieren Sie ihn, und fügen Sie ihn ein. Wenn die Verwaltungskonsole Zugriff auf diesen Pfad hat, können Sie das Paket hinzufügen. Wenn sich das Paket auf einer Netzwerkfreigabe befindet, können Sie mit dem Datei-Explorer zu dem Speicherort navigieren, indem Sie die folgenden Schritte ausführen:

1.  Klicken Sie bei gedrückter **UMSCHALTTASTE**mit der rechten Maustaste auf die Paketdatei.

2.  Wählen Sie **als Pfad kopieren** aus.

3.  Einfügen des Pfads in das Eingabefeld des Dialogfelds " **Paket hinzufügen** "

## <a href="" id="upgrading-app-v-management-server-to-5-1-sometimes-fails-with-the-message--a-database-error-occurred-"></a>Das Upgrade von App-V Management Server auf 5,1 schlägt manchmal mit der Meldung "ein Datenbankfehler ist aufgetreten" fehl


Wenn Sie den App-v 5,0 SP1-Verwaltungsserver installieren und dann versuchen, auf App-v 5,1-Server zu aktualisieren, wenn mehrere Verbindungsgruppen konfiguriert und aktiviert sind, wird der folgende Fehler angezeigt: "ein Datenbankfehler ist aufgetreten. Ursache: ' Ungültiger Spaltenname ' PackageOptional '. Ungültiger Spaltenname ' VersionOptional '. "

**Problemumgehung**: führen Sie diesen Befehl für Ihre SQL-Datenbank aus:

`ALTER TABLE AppVManagement.dbo.PackageGroupMembers ADD PackageOptional bit NOT NULL DEFAULT 0, VersionOptional bit NOT NULL DEFAULT 0`

Dabei ist "AppVManagement" der Name der Datenbank.

## Benutzer können ein Paket nicht in einer vom Benutzer veröffentlichten Verbindungsgruppe öffnen, wenn Sie ein optionales Paket hinzufügen oder entfernen.


In Umgebungen, in denen der RDS-Client ausgeführt wird oder die mehrere gleichzeitige Benutzer pro Computer aufweisen, können angemeldete Benutzer keine Anwendungen in Paketen öffnen, die sich in einer vom Benutzer veröffentlichten Verbindungsgruppe befinden, wenn ein optionales Paket zur Verbindungsgruppe hinzugefügt oder daraus entfernt wird.

**Problemumgehung**: lassen Sie die Benutzer sich abmelden und melden Sie sich dann wieder an.

## Fehlermeldung wird fälschlicherweise angezeigt, wenn die Verbindungsgruppe nur für den Benutzer veröffentlicht wird


Wenn Sie Repair-AppvClientConnectionGroup ausführen, wird der folgende Fehler angezeigt, auch wenn die Verbindungsgruppe nur für den Benutzer veröffentlicht wird: "interner App-V-Integrations Fehler: das Paket wurde nicht für den Benutzer integriert. Stellen Sie sicher, dass das Paket dem Computer hinzugefügt und für den Benutzer veröffentlicht wird. "

**Problemumgehung**: führen Sie eine der folgenden Aktionen aus:

-   Alle Pakete in einer Verbindungsgruppe veröffentlichen

    Das Problem tritt auf, wenn die zu reparierende Verbindungsgruppe Pakete enthält, die für den Benutzer nicht verfügbar sind oder nicht zur Verfügung stehen (also nicht global oder für den Benutzer veröffentlicht werden). Die Reparatur funktioniert jedoch, wenn alle Pakete der Verbindungsgruppe verfügbar sind, um sicherzustellen, dass alle Pakete veröffentlicht werden.

-   Reparieren Sie Pakete einzeln mit dem Befehl reparieren-AppvClientPackage statt mit dem Befehl Repair-AppvClientConnectionGroup.

    Ermitteln Sie, welche Pakete für die Benutzer verfügbar sind, und führen Sie dann den Befehl Repair-AppvClientPackage einmal für jedes Paket aus. Verwenden Sie PowerShell-Cmdlets, um folgende Aktionen auszuführen:

    1.  Rufen Sie alle Pakete in einer Verbindungsgruppe ab.

    2.  Überprüfen Sie, ob die einzelnen Pakete aktuell veröffentlicht sind.

    3.  Wenn das Paket aktuell veröffentlicht wird, führen Sie AppvClientPackage für dieses Paket aus.

## Symbole werden in Sequencer nicht richtig angezeigt


Symbole auf der Registerkarte Verknüpfungen und Dateitypzuordnungen werden beim Ändern eines Pakets im App-V-Sequenzer nicht richtig angezeigt. Dieses Problem tritt auf, wenn die Größe der Symbole nicht 16x16 oder 32 x 32 ist.

**Problemumgehung**: Verwenden Sie nur Symbole, die 16x16 oder 32 x 32 sind.

## InsertVersionInfo. SQL-Skript ist für die Verwaltungsdatenbank nicht mehr erforderlich


Das InsertVersionInfo. SQL-Skript ist für Versionen der APP-v-Verwaltungsdatenbank später als App-v 5,0 SP3 nicht erforderlich.

Das Skript "Permissions. SQL" sollte gemäß **Schritt 2** im [KB-Artikel 3031340](https://support.microsoft.com/kb/3031340)aktualisiert werden.

**Wichtig** 
 **Schritt 1** ist für Versionen von App-v später als App-v 5,0 SP3 nicht erforderlich.

 

## Microsoft Visual Studio 2012 nicht unterstützt


App-V 5,1 unterstützt Visual Studio 2012 nicht.

**Problemumgehung**: keine

## Einschränkungen für Anwendungsdatei Namen für App-V 5. x-Sequenzer


App-V 5. x Sequencer kann keine Anwendungen mit Dateinamen abgleichen, die "CO_ &lt; x &gt; " entsprechen, wobei x eine beliebige Zahl ist. Fehler 0x8007139F wird generiert.

**Problemumgehung**: Verwenden Sie einen anderen Dateinamen

## Zeitweilige Fehlermeldung "Datei nicht gefunden" beim Bereitstellen eines Pakets


Gelegentlich wird beim Bereitstellen eines Pakets ein Fehler "Datei nicht gefunden" (0x80070002) generiert. In der Regel tritt dies auf, wenn ein Ordner in einem App-V-Paket viele Dateien enthält (also 20K oder mehr). Dies kann dazu führen, dass Streaming länger als erwartet dauert und zu einem Timeout führt, das die Fehlermeldung "Datei nicht gefunden" generiert.

**Problemumgehung**: ab HF06 wurde ein neuer Registrierungsschlüssel eingeführt, um die Verlängerung dieses Timeoutzeitraums zu ermöglichen.

<table>
<colgroup>
<col width="20%" />
<col width="80%" />
</colgroup>
<tbody>
<tr>
<td align="left">Pfad</td>
<td align="left">HKEY_LOCAL_MACHINE \software\microsoft\appv\client\streaming</td>
</tr>
<tr>
<td align="left">Einstellung</td>
<td align="left">StreamResponseWaitTimeout</td>
</tr>
<tr>
<td align="left">Datentyp</td>
<td align="left">DWORD</td>
</tr>
<tr>
<td align="left">Einheiten</td>
<td align="left">Sekunden</td>
</tr>
<tr>
<td align="left">Standard</td>
<td align="left">5<br />
<strong>Hinweis </strong> : dieser Wert ist der Standardwert, wenn der Registrierungsschlüssel nicht definiert ist oder ein Wert &lt; = 5 angegeben ist.
</td>
</tr>
</tbody>
</table>






## Verwandte Themen


[Informationen zu App-V 5.1](about-app-v-51.md)

 

 





