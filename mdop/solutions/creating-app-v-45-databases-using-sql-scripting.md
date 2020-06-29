---
title: Erstellen von App-V 4.5-Datenbanken mithilfe von SQL-Skripts
description: Erstellen von App-V 4.5-Datenbanken mithilfe von SQL-Skripts
author: dansimp
ms.assetid: 6cd0b180-163e-463f-a658-939ab9a7cfa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9ab2c102a43701bfdeaac49359b4ca3c4a063fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811479"
---
# Erstellen von App-V 4.5-Datenbanken mithilfe von SQL-Skripts


**Für wen ist diese Lösung vorgesehen?** IT-Experten, die Application Virtualization (App-V) 4,5-Datenbanken verwalten.

**Wie kann Ihnen dieser Leitfaden helfen?** Diese Lösung erläutert und dokumentiert das Verfahren zum Installieren des Microsoft Application Virtualization-Servers, wenn die Installation des Administrators nicht über "sysadmin"-Berechtigungen für SQL Server verfügt.

## Übersicht


Eine der Herausforderungen bei der Installation von Microsoft Application Virtualization 4,5 (App-V) besteht darin, dass das Installationsprogramm davon ausgeht, dass der Benutzer, der die Server Features installiert, nicht nur ein lokaler Computeradministrator ist, sondern auch über SQL-Administratorrechte auf dem SQL Server verfügt, der den Datenspeicher hosten wird. Diese Anforderung basiert auf der Tatsache, dass die Datenbank sowie die entsprechenden Rollen und Berechtigungen als Teil der Installation erstellt werden. In den meisten Unternehmen werden SQL-Server jedoch separat vom Infrastrukturteam verwaltet, das App-V installieren wird. Durch diese Sicherheitsanforderungen wird es schwierig, SQL-Administratoren zu veranlassen, dem Infrastrukturadministrator zu ermöglichen, App-V adäquate Rechte zu installieren. Ebenso verfügen die SQL-Administratoren nicht über die erforderlichen Berechtigungen zum Installieren des Produkts für das Infrastrukturteam.

Zurzeit muss ein Administrator, der die Installation von App-V versucht, über SQL-"sysadmin"-Berechtigungen verfügen. In früheren Versionen des Produkts durften die SQL-Administratoren entweder ein temporäres "sysadmin"-Konto erstellen oder während der Installation anwesend sein, um Anmeldeinformationen mit "sysadmin"-Privilegien bereitzustellen. In dieser Version werden Skripts im veröffentlichten Produkt bereitgestellt, damit alle Administratoren ihre Infrastruktur implementieren können.

In diesem Whitepaper wird das Szenario erläutert, in dem die Installation in zwei getrennte Aufgaben aufgeteilt werden muss: Erstellen der SQL-Datenbank und Installieren der App-V-Server Features. Die SQL-Administratoren können die SQL-Skripts überprüfen und Änderungen vornehmen, um Konflikte mit anderen Datenbanken zu beheben oder die Integration mit anderen Tools zu unterstützen. Das Ergebnis der Skripts besteht darin, dass SQL-Administratoren die Datenbank vorbereiten können, damit den Infrastrukturadministratoren keine erweiterten Rechte auf dem SQL Server gewährt werden. Dies ist in Umgebungen wichtig, in denen dies durch Sicherheitsrichtlinien untersagt ist.

### Erstellungsprozess für SQL-Datenbanken

Die SQL-Skripts ermöglichen es SQL-Administratoren, die erforderliche Datenbank zu erstellen und auch die Privilegien für die App-V-Administratoren einzurichten, um die Umgebung erfolgreich zu installieren und zu verwalten. Die Schritte zum Abschließen dieser Aufgaben sind weiter unten in diesem Dokument aufgeführt.

Durch diesen Vorgang werden die Daten Banker stellungs-und Konfigurationsaktionen von der eigentlichen App-V-Installation getrennt.

**Informationen, die SQL-Administratoren bereitgestellt werden sollen**

-   Der Name der Anzeigengruppe, die die App-V-Administratoren sein wird

-   Name des Servers, auf dem App-V Management Server installiert wird

**Informationen, die an die Infrastrukturadministratoren zurückgegeben werden sollen**

-   Name des Datenbankservers oder der Instanz und der Name der App-V-Datenbank

Nachdem die Datenbank vorbereitet wurde, können die APP-v-Administratoren die APP-v-Installation ohne SQL-Administratorrechte ausführen.

### Verwenden der SQL-Setup Skripts

**Anforderungen**

Im folgenden finden Sie eine Liste der Anforderungen für die Verwendung der Skripts, die sich im Ordner support\\createdb im Stammverzeichnis des ausgewählten Extraktions Speicherorts befinden.

-   Skripts müssen an einen beschreibbaren Speicherort auf dem Computer kopiert werden, auf dem Sie ausgeführt werden (achten Sie darauf, das Attribut "schreibgeschützt" aus diesen Skripts zu entfernen, nachdem Sie kopiert wurden), und die SQL-Clienttools müssen auf diesem Computer geladen werden (osql ist nur für die Ausführung der Beispielbatchdateien auf dem lokalen Computer erforderlich).

-   SQL Server muss die Windows-Authentifizierung unterstützen.

-   Stellen Sie sicher, dass die SQL Server-Instanz und der SQL-Agent-Dienst ausgeführt werden.

-   Melden Sie sich mit einem Domänenkonto an, bei dem es sich um einen SQL-Administrator (sysadmin) auf dem Computer handelt, auf dem die Skripts ausgeführt werden.

Die Skripts werden unter den Domänenanmeldeinformationen des angemeldeten Benutzers ausgeführt.

**Erstellen von Datenbanken mit SQL-Skripts**

**Aufgaben, die von SQL-Administratoren ausgeführt werden sollen:**

1.  Kopieren Sie die im support\\createdb-Ordner enthaltenen Skripts aus dem Stammverzeichnis des ausgewählten Extrahierungs Speicherorts auf den Computer, auf dem die Skripts ausgeführt werden. Die folgenden Dateien sind für die ordnungsgemäße Ausführung der Skripts erforderlich und müssen in der unten aufgeführten Reihenfolge aufgerufen werden.

    -   Database. SQL

    -   Roles. SQL

    -   Tabelle \ _CODES. SQL

    -   Funktionen \ _before \ _tables. SQL

    -   Tables. SQL

    -   Functions. SQL

    -   views. SQL

    -   Procedures. SQL

    -   Triggers. SQL

    -   Data \ _codes. SQL

    -   Data \ _messages. SQL

    -   Data \ _defaults. SQL

    -   Alerts \ _Jobs. SQL

    -   dbversion. SQL

2.  Überprüfen und ändern Sie bei Bedarf die `database.sql` Datei. Die Standardeinstellungen geben der Datenbank den Namen "APPVIRTDB".

    -   Ersetzen Sie bei Bedarf Instanzen von `APPVIRTDB` mit dem `database name` , die verwendet werden.

    -   Ändern Sie die `FILENAME` Eigenschaft im Skript mit dem entsprechenden Pfad für den SQL-Server, auf dem die Datenbank erstellt wird.

3.  Überprüfen und ändern Sie bei Bedarf die `database name [APPVIRTDB]` in der `roles.sql` Datei, die in der Datenbank. SQL-Datei verwendet wurde.

****

### Beispiel für die Automatisierung des Prozesses mithilfe von Batchdateien

Wenn die beiden Beispielbatchdateien verwendet werden, führen Sie die SQL-Skripts wie folgt aus:

1.  **Create\_schema.bat (1)**

    -   Database. SQL

    -   Roles. SQL

2.  **Create\_tables.bat (2)**

    -   Tabelle \ _CODES. SQL

    -   Funktionen \ _before \ _tables. SQL

    -   Tables. SQL

    -   Functions. SQL

    -   views. SQL

    -   Procedures. SQL

    -   Triggers. SQL

    -   Data \ _codes. SQL

    -   Data \ _messages. SQL

    -   Data \ _defaults. SQL

    -   Alerts \ _Jobs. SQL

    -   dbversion. SQL

**Hinweis:**  
Sorgfältige Überlegungen beim Ändern der Skripts müssen getroffen werden und sollten nur von einer Person mit dem entsprechenden wissen durchgeführt werden. Darüber hinaus sollten nur die folgenden Beispieldateien geändert werden: **create\_schema.bat**, **create\_tables.bat**, **Database. SQL**und **Roles. SQL**. Alle anderen Dateien sollten in keiner Weise geändert werden, da dies dazu führen kann, dass die Datenbank falsch erstellt wird, was dazu führt, dass App-V-Dienste nicht installiert werden.



Die beiden Beispielbatchdateien müssen sich im gleichen Verzeichnis befinden, in dem die restlichen SQL-Skripts auf den Computer kopiert wurden.

1.  Führen Sie die Beispiel **create\_schema.bat** -Datei aus, um die Datenbank zu erstellen. Dieses Skript wird einige Sekunden dauern, bis es beendet wird und nicht unterbrochen werden sollte.

    -   Führen Sie die Create schema.bat-Datei aus dem Verzeichnis aus, in das Sie kopiert wurde. Syntax lautet: "Create\_schema.bat `SQLSERVERNAME` "

        ![AppV46SQLcreatebat](images/appv46sqlcreatebat.bmp)

    -   Wenn dieses Skript während der Erstellung der neuen "APPVIRTDB"-Datenbank fehlschlägt, überprüfen Sie das Protokoll wie angegeben, um das Problem zu beheben. Es ist notwendig, die Datenbank zu löschen, die mit einer partiellen Ausführung der Skripts erstellt wurde, um sicherzustellen, dass nachfolgende Versuche ordnungsgemäß funktionieren.

2.  Führen `create_tables.bat` Sie die Datei aus, um die Tabellen in der Datenbank zu erstellen. Dieses Skript wird einige Sekunden dauern, bis es beendet wird und nicht unterbrochen werden sollte.

    -   Führen Sie die create\_tables.bat-Datei aus dem Verzeichnis aus, in dem Sie kopiert wurde. Syntax lautet: "create\_tables.bat `SQLSERVERNAME DBNAME` "

        ![App-v 4,6 SQL create\-table.bat](images/appv46sqlcreate-tablebat.gif)

        Wenn das Skript während der Erstellung der Tabellen fehlschlägt, überprüfen Sie das Protokoll wie angegeben, um das Problem zu beheben. Es ist notwendig, die Datenbank zu löschen und create\_schema.bat auszuführen, bevor Sie versuchen, die create\_tables.bat-Datei bei allen nachfolgenden versuchen auszuführen.

### Festlegen von Berechtigungen für die App-V-Datenbank

Die folgenden Konten müssen auf dem SQL Server mit bestimmten Berechtigungen und Rollen für die neue Datenbank für die Installation, Bereitstellung und laufende Verwaltung der App-V-Umgebung erstellt werden.

-   Erstellen Sie eine Anmeldung für die APP-v-Administratorengruppe auf dem SQL Server und die APPVIRTDB-Datenbank für die "domain\\App-V-Administratoren" (wobei "Domäne" und "App-v-Administratoren" geändert werden, um Ihre eigene Umgebung zu reflektieren), und fügen Sie Sie der SFTAdmin-und SFTEveryone-Datenbankrolle hinzu.

    ![App-v 4,6 SQL-Skriptsatz Berechtigungen und Rollen](images/appv46sqlscriptsetpermsroles.gif)

-   Erteilen Sie dieser Gruppe die Berechtigung "jede Definition anzeigen" auf globaler Ebene (Dies ermöglicht es dem Microsoft Application Virtualization Management Server-Setupprozess, zu überprüfen, ob der Verwaltungsserver-Anmeldename bereits vorhanden ist). Unter MS-SQL 2005 und höher wurden Zugriffseinschränkungen für die in Master. DB enthaltenen Metadaten hinzugefügt. Der im vorherigen Schritt erstellte Benutzer verfügt standardmäßig nicht über die Rechte, die von der Server Installation benötigt werden. Öffnen Sie die Eigenschaften der zuvor erstellten Anmeldung, Anmeldeeigenschaften- &gt; sicherungsfähige Elemente. Fügen Sie die Datenbankinstanz hinzu, und aktivieren Sie "Grant" für "jede Definition anzeigen", wie im folgenden Screenshot gezeigt.

    ![App-v 4,6 SQL-Skript Grant Perm für View any DEF](images/appv46sqlscriptviewanydef.gif)

-   Fügen Sie der Rolle \ _ASSIGNMENTS Tabelle für die im vorherigen Schritt erstellte Anmeldung eine Rolle hinzu, um App-v-Administratoren den Zugriff auf die Application Virtualization Management Console zu ermöglichen, mit Role = "admin" und Group \ _ref = "domain\\App-V-Administratoren" (wobei "Domäne" und "App-v-Administratoren" entsprechend ihrer eigenen Umgebung geändert werden).

    ![App-v 4,6 SQL-Skript Rollenzuweisung](images/appv46sqlscriptroleassign.gif)

-   Erstellen Sie die Anmeldung für SQL Server und die App-V-Datenbank für den Verwaltungs Server. Dieses Konto wird vom Microsoft Application Virtualization Management Server zum Herstellen einer Verbindung mit dem Datenspeicher verwendet und ist für die Wartung von Clientanforderungen für gestreamte Anwendungen verantwortlich. Je nachdem, wo SQL Server und Verwaltungsserver installiert werden sollen, gibt es zwei Optionen:

    1.  Wenn Verwaltungs Server und SQL Server auf demselben Computer installiert werden, fügen Sie einen Anmeldenamen für den NT-AUTHORITY\\NETWORK-Dienst hinzu, und fügen Sie ihn den Datenbankrollen SFTUser und SFTEveryone hinzu.

    2.  Wenn der Verwaltungsserver und SQL Server auf unterschiedlichen Computern installiert werden sollen, fügen Sie eine Anmeldung für "domain\\App-V Servername $" hinzu (wobei "App-v Servername" der Name des Servers ist, auf dem der APP-v-Verwaltungsserver installiert wird), und fügen Sie ihn den Datenbankrollen SFTUser und SFTEveryone hinzu.

-   Öffnen Sie das Abfragefenster im SQL-Fenster, und führen Sie das folgende SQL aus:

    ``` syntax
    USE APPVIRTDB
    GRANT ALTER ON ROLE::SFTuser TO “domain\App-V Admins”
    ```

    Hierbei handelt es sich um den Namen der APP-v-Datenbank, die im vorherigen Schritt auf dem SQL Server erstellt wurde, und der Benutzer, der die Installation des App-v-Servers durchführen soll, muss ein Mitglied von "domain\\App-V-Administratoren" sein (wobei "Domäne" und "App-v-Administratoren" geändert werden, um Ihre eigene Umgebung APPVIRTDB).

### Aufgaben, die von den Infrastrukturadministratoren ausgeführt werden sollen

1.  Der Administrator in der Gruppe "App-v-Administratoren" sollte App-v installieren.

    Verwenden Sie Informationen der SQL-Administratoren zum Auswählen des SQL-Servers und der Datenbank, die in den vorherigen Schritten erstellt wurden.

2.  Der Administrator in der Gruppe "App-V-Administratoren" meldet sich bei Application Virtualization Management Console an und löscht die folgenden Objekte aus der Verwaltungskonsole.

    **Warnung**  
    Dies ist erforderlich, da das herkömmliche Setup bestimmte Datensätze in der Datenbank auffüllt, die nicht ausgefüllt werden, wenn Sie die Installation für eine bereits vorhandene Datenbank ausführen. Löschen Sie die folgenden Objekte:

    -   Löschen Sie unter "Servergruppen" "Standardserver Gruppe" "Application Virtualization Management Server".

    -   Löschen Sie unter "Servergruppen" die Standardserver Gruppe.

    -   Löschen Sie unter "Anbieterrichtlinien" den Eintrag "Standardanbieter".



3.  Der Administrator in der App-V-Administratorengruppe sollte dann Folgendes erstellen:

    -   Erstellen Sie unter "Anbieterrichtlinien" eine neue Anbieterrichtlinie

    -   Erstellen einer "Standard Server Gruppe"

        **Hinweis:**  
        Sie müssen eine "Standard Server"-Gruppe erstellen, auch wenn Sie nicht verwendet werden. Das Serverinstallationsprogramm sucht nur nach der "Standardserver Gruppe", wenn Sie versuchen, den Server hinzuzufügen.  Wenn keine "Standard Server Gruppe" vorhanden ist, tritt bei der Installation ein Fehler auf. Wenn Sie beabsichtigen, andere Servergruppen als die standardmäßige Verwendung zu verwenden, müssen Sie nur die "Standardserver Gruppe" beibehalten, wenn Sie beabsichtigen, nachfolgende App-V-Verwaltungsserver zu Ihrer Infrastruktur hinzuzufügen.



~~~
-   Assign the App-V Users Group to the New Provider Policy created above

-   Under “Server Groups,” create a New Server Group, specifying the New Provider Policy

-   Under the New Server group, create a New Application Virtualization Management Server

    **Important**  
    Do not restart the service before completing all of the above steps!



-   Administrator restarts the Application Virtualization Management Server service.
~~~

## Fazit


Abschließend können die Informationen in diesem Dokument einem Administrator helfen, mit den SQL-Administratoren zusammenzuarbeiten, um einen Bereitstellungspfad zu entwickeln, der für die Sicherheits-und Verwaltungsabteilungen in einer Organisation verwendet werden kann. Nach dem Lesen dieses Dokuments und dem Testen der dokumentierten Aufgaben sollte ein Administrator bereit sein, die App-V-Infrastruktur in dieser Art von Umgebung zu implementieren.









