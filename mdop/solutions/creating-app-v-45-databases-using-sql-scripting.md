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
ms.openlocfilehash: c119f1d43a70cce04dd6151697318f7cf6a8d1f2
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910590"
---
# <a name="creating-app-v-45-databases-using-sql-scripting"></a>Erstellen von App-V 4.5-Datenbanken mithilfe von SQL-Skripts


**Wer ist diese Lösung vorgesehen?** It technology professionals who manage Application Virtualization (App-V) 4.5 databases.

**Wie kann Ihnen dieser Leitfaden helfen?** In dieser Lösung wird das Verfahren zum Installieren von Microsoft Application Virtualization Server erläutert und dokumentiert, wenn der Administrator nicht über "sysadmin"-Berechtigungen für die SQL Server verfügt.

## <a name="overview"></a>Übersicht


Eine der Herausforderungen bei der Installation von Microsoft Application Virtualization 4.5 (App-V) besteht darin, dass das Installationsprogramm davon ausgeht, dass der Benutzer, der die Serverfeatures installiert, nicht nur ein lokaler Computeradministrator ist, sondern auch über SQL Administratorrechte auf dem SQL Server verfügt, der die Daten Store hostet. Diese Anforderung basiert auf der Tatsache, dass die Datenbank sowie die entsprechenden Rollen und Berechtigungen als Teil der Installation erstellt werden. In den meisten Unternehmen werden SQL Server jedoch separat vom Infrastrukturteam verwaltet, das App-V installiert. Diese Sicherheitsanforderungen machen es schwierig, SQL Administratoren dazu zu bringen, dem Infrastrukturadministrator angemessene Rechte für die Installation von App-V zu erteilen. Entsprechend verfügen die SQL Administratoren nicht über die erforderlichen Berechtigungen zum Installieren des Produkts für das Infrastrukturteam.

Derzeit muss ein Administrator, der die Installation von App-V versucht, über SQL "sysadmin"-Berechtigungen verfügen. In früheren Versionen des Produkts war das Setup für die SQL Administratoren zulässig, entweder ein temporäres "sysadmin"-Konto zu erstellen oder während der Installation vorhanden zu sein, um Anmeldeinformationen mit "sysadmin"-Berechtigungen bereitzustellen. In dieser Version werden Skripts im veröffentlichten Produkt für alle Administratoren bereitgestellt, die sie bei der Implementierung ihrer Infrastruktur verwenden können.

In diesem Whitepaper wird das Szenario erläutert, in dem die Installation in zwei separate Aufgaben unterteilt werden muss: Erstellen der SQL-Datenbank und Installieren der App-V-Serverfeatures. Die SQL Administratoren könnten die SQL Skripts überprüfen und Änderungen vornehmen, um Konflikte mit anderen Datenbanken zu lösen oder die Integration mit anderen Tools zu unterstützen. Das Ergebnis der Skripts ist, dass SQL Administratoren die Datenbank so vorbereiten können, dass den Infrastrukturadministratoren keine erweiterten Rechte auf dem SQL Server gewährt werden müssen. Dies ist in Umgebungen wichtig, in denen dies durch Sicherheitsrichtlinien verhindert würde.

### <a name="sql-database-creation-process"></a>SQL-Datenbank Erstellungsprozess

Die SQL Skripts ermöglichen es SQL Administratoren, die erforderliche Datenbank zu erstellen und auch die Berechtigungen für App-V-Administratoren einzurichten, um die Umgebung erfolgreich zu installieren und zu verwalten. Die Schritte zum Abschließen dieser Aufgaben werden weiter unten in diesem Dokument aufgeführt.

Dieser Vorgang trennt die Datenbankerstellungs- und Konfigurationsaktionen von der tatsächlichen App-V-Installation.

**Informationen, die SQL Administratoren bereitgestellt werden sollen**

-   Name der AD-Gruppe, die der App-V-Administrator sein wird

-   Name des Servers, auf dem der App-V-Verwaltungsserver installiert wird

**Informationen, die an die Infrastrukturadministratoren zurückgegeben werden sollen**

-   Name des Datenbankservers oder der Instanz und Name der App-V-Datenbank

Nachdem die Datenbank vorbereitet wurde, können die App-V-Administratoren die App-V-Installation ohne SQL Administratorrechte ausführen.

### <a name="using-the-sql-setup-scripts"></a>Verwenden der SQL Setupskripts

**Anforderungen**

Es folgt eine Liste der Anforderungen für die Verwendung der Skripts, die sich im Ordner "support\\createdb" im Stammverzeichnis des ausgewählten Extraktspeicherorts befinden.

-   Skripts müssen an einen schreibbaren Speicherort auf dem Computer kopiert werden, auf dem sie ausgeführt werden (achten Sie darauf, das Schreibschutzattribut aus diesen Skripts zu entfernen, nachdem sie kopiert wurden), und SQL Clienttools müssen auf diesem Computer geladen werden (osql ist nur zum Ausführen der Beispielbatchdateien auf dem lokalen Computer erforderlich).

-   Die SQL Server muss Windows Authentifizierung unterstützen.

-   Stellen Sie sicher, dass die SQL Server Instanz und SQL-Agent-Dienst ausgeführt werden.

-   Melden Sie sich mit einem Domänenkonto an, das ein SQL-Administrator (Sysadmin) auf dem Computer ist, auf dem die Skripts ausgeführt werden.

Die Skripts werden unter den Domänenanmeldeinformationen des angemeldeten Benutzers ausgeführt.

**Datenbankerstellung mit SQL Skripts**

**Aufgaben, die von SQL Administratoren ausgeführt werden sollen:**

1.  Kopieren Sie die Im Ordner "support\\createdb" enthaltenen Skripts aus dem Stammverzeichnis des ausgewählten Extraktspeicherorts auf den Computer, auf dem die Skripts ausgeführt werden. Die folgenden Dateien sind erforderlich, damit die Skripts ordnungsgemäß ausgeführt werden können, und müssen in der unten aufgeführten Reihenfolge aufgerufen werden.

    -   database.sql

    -   roles.sql

    -   table\_CODES.sql

    -   functions\_before\_tables.sql

    -   tables.sql

    -   functions.sql

    -   views.sql

    -   procedures.sql

    -   triggers.sql

    -   data\_codes.sql

    -   data\_messages.sql

    -   data\_defaults.sql

    -   alerts\_jobs.sql

    -   dbversion.sql

2.  Überprüfen und ändern Sie `database.sql` ggf. die Datei. Die Standardeinstellungen nennen die Datenbank "APPVIRTDB".

    -   Ersetzen Sie bei Bedarf Instanzen von mit `APPVIRTDB` `database name` der, die verwendet wird.

    -   Ändern Sie die `FILENAME` Eigenschaft im Skript mit dem entsprechenden Pfad für die SQL Server, in der die Datenbank erstellt wird.

3.  Überprüfen und ändern Sie `database name [APPVIRTDB]` ggf. die Datei in der `roles.sql` Datei, die in der Datei database.sql verwendet wurde.

****

### <a name="example-of-how-to-automate-the-process-using-batch-files"></a>Beispiel für die Automatisierung des Prozesses mithilfe von Batchdateien

Bei Verwendung führen die beiden bereitgestellten Beispielbatchdateien die SQL Skripts wie folgt aus:

1.  **Create\_schema.bat (1)**

    -   database.sql

    -   roles.sql

2.  **Create\_tables.bat (2)**

    -   table\_CODES.sql

    -   functions\_before\_tables.sql

    -   tables.sql

    -   functions.sql

    -   views.sql

    -   procedures.sql

    -   triggers.sql

    -   data\_codes.sql

    -   data\_messages.sql

    -   data\_defaults.sql

    -   alerts\_jobs.sql

    -   dbversion.sql

**Hinweis:**  
Sorgfältige Überlegungen beim Ändern der Skripts müssen berücksichtigt werden und sollten nur von jemanden durchgeführt werden, der über das entsprechende Wissen verfügt. Außerdem sollten von den Beispieldateien, die angezeigt werden, nur Folgendes geändert werden: **create\_schema.bat**, **create\_tables.bat**, **database.sql**und **roles.sql**. Alle anderen Dateien sollten in keiner Weise geändert werden, da dies dazu führen kann, dass die Datenbank falsch erstellt wird, was dazu führt, dass App-V-Dienste nicht installiert werden.



Die beiden Beispielbatchdateien müssen sich im selben Verzeichnis befinden, in das die restlichen SQL Skripts auf den Computer kopiert wurden.

1.  Führen Sie die ** Beispieldateicreate\_schema.bat** aus, um die Datenbank zu erstellen. Der Abschluss dieses Skripts dauert mehrere Sekunden und sollte nicht unterbrochen werden.

    -   Führen Sie die Datei zum Erstellen schema.bat aus dem Verzeichnis aus, in das sie kopiert wurde. Die Syntax lautet: `SQLSERVERNAME` "Create\_schema.bat"

        ![AppV46SQLcreatebat.](images/appv46sqlcreatebat.bmp)

    -   Wenn dieses Skript während der Erstellung der neuen "APPVIRTDB"-Datenbank fehlschlägt, überprüfen Sie das Protokoll wie angegeben, um das Problem zu beheben. Es ist erforderlich, die Datenbank zu löschen, die mit einer teilweisen Ausführung der Skripts erstellt wurde, um sicherzustellen, dass nachfolgende Versuche ordnungsgemäß funktionieren.

2.  Führen Sie die `create_tables.bat` Datei aus, um die Tabellen in der Datenbank zu erstellen. Der Abschluss dieses Skripts dauert mehrere Sekunden und sollte nicht unterbrochen werden.

    -   Führen Sie die create\_tables.bat Datei aus dem Verzeichnis aus, in das sie kopiert wurde. Die Syntax lautet: `SQLSERVERNAME DBNAME` "create\_tables.bat"

        ![app-v 4.6 sql create\-table.bat.](images/appv46sqlcreate-tablebat.gif)

        Wenn das Skript während der Erstellung der Tabellen fehlschlägt, überprüfen Sie das Protokoll wie angegeben, um das Problem zu beheben. Es ist erforderlich, die Datenbank zu löschen und create\_schema.bat auszuführen, bevor Sie versuchen, die create\_tables.bat-Datei bei allen nachfolgenden Versuchen auszuführen.

### <a name="setting-permissions-on-the-app-v-database"></a>Festlegen von Berechtigungen für die App-V-Datenbank

Die folgenden Konten müssen auf dem SQL Server mit bestimmten Berechtigungen und Rollen für die neue Datenbank für die Installation, Bereitstellung und laufende Verwaltung der App-V-Umgebung erstellt werden.

-   Erstellen Sie eine Anmeldung für die Gruppe "App-V-Administratoren" im SQL Server und die APPVIRTDB-Datenbank für die "domäne\\App-V-Administratoren" (wobei "Domäne" und "App-V-Administratoren" geändert werden, um Ihre eigene Umgebung widerzuspiegeln), und fügen Sie sie der SFTAdmin- und SFTEveryone-Datenbankrolle hinzu.

    ![App-v 4.6 sql script set permissions and roles.](images/appv46sqlscriptsetpermsroles.gif)

-   Erteilen Sie dieser Gruppe die Berechtigung "ALLE DEFINITION ANZEIGEN" auf globaler Ebene (auf diese Weise kann der Setupprozess von Microsoft Application Virtualization Management Server überprüfen, ob die Verwaltungsserveranmeldung bereits vorhanden ist). Unter MS-SQL 2005 und höher wurden Zugriffseinschränkungen für die metadaten in master.db hinzugefügt. Der im vorherigen Schritt erstellte Benutzer verfügt standardmäßig nicht über die von der Serverinstallation benötigten Rechte. Öffnen Sie die Eigenschaften der zuvor erstellten Anmeldeinformationen, Anmeldeeigenschaften– &gt; Securables. Fügen Sie die Datenbankinstanz hinzu, und aktivieren Sie "GRANT" für "Beliebige Definition anzeigen", wie im folgenden Screenshot dargestellt.

    ![app-v 4.6 sql script grant perm for view any def.](images/appv46sqlscriptviewanydef.gif)

-   Fügen Sie der Role\_ASSIGNMENTS-Tabelle für die im vorherigen Schritt erstellte Anmeldung eine Rolle hinzu, um App-V-Administratoren den Zugriff auf die Application Virtualization Management Console zu ermöglichen, wobei die Rolle = "ADMIN" und "gruppe\_ref = "Domäne\\App-V-Administratoren" (wobei "Domäne" und "App-V-Administratoren" geändert werden, um Ihre eigene Umgebung widerzuspiegeln).

    ![App-v 4.6 SQL-Skriptrollenzuweisung.](images/appv46sqlscriptroleassign.gif)

-   Erstellen Sie die Anmeldung für SQL Server und die App-V-Datenbank für den Verwaltungsserver. Dieses Konto wird vom Microsoft Application Virtualization Management Server zum Herstellen einer Verbindung mit dem Datenspeicher verwendet und ist für die Wartung von Clientanforderungen für gestreamte Anwendungen verantwortlich. Es gibt zwei Optionen, je nachdem, wo die SQL Server und der Verwaltungsserver installiert werden sollen:

    1.  Wenn Verwaltungsserver und SQL Server auf demselben Computer installiert werden, fügen Sie eine Anmeldung für NT AUTHORITY\\NETWORK SERVICE hinzu, und fügen Sie sie den SFTUser- und SFTEveryone-Datenbankrollen hinzu.

    2.  Wenn der Verwaltungsserver und SQL Server auf verschiedenen Computern installiert werden sollen, fügen Sie eine Anmeldung für "domain\\App-V Server Name$" hinzu (wobei "App-V-Servername" der Name des Servers ist, auf dem der App-V-Verwaltungsserver installiert wird) und fügen Sie ihn den SFTUser- und SFTEveryone-Datenbankrollen hinzu.

-   Öffnen Sie das Abfragefenster im fenster SQL, und führen Sie die folgenden SQL aus:

    ``` syntax
    USE APPVIRTDB
    GRANT ALTER ON ROLE::SFTuser TO “domain\App-V Admins”
    ```

    Dabei ist APPVIRTDB der Name der App-V-Datenbank, die im vorherigen Schritt auf dem SQL Server erstellt wurde, und der Benutzer, der die Installation des App-v-Servers durchführen wird, muss Mitglied von "domäne\\App-V-Administratoren" sein (wobei "Domäne" und "App-V-Administratoren" geändert werden, um Ihre eigene Umgebung widerzuspiegeln).

### <a name="tasks-to-be-performed-by-the-infrastructure-administrators"></a>Aufgaben, die von den Infrastrukturadministratoren ausgeführt werden sollen

1.  Der Administrator in der Gruppe "App-V-Administratoren" sollte App-V installieren.

    Verwenden Sie Informationen von den SQL Administratoren, um die in den vorherigen Schritten erstellten SQL Server und die Datenbank auszuwählen.

2.  Der Administrator in der Gruppe "App-V-Administratoren" meldet sich bei der Application Virtualization Management Console an und löscht die folgenden Objekte aus der Verwaltungskonsole.

    **Warnung**  
    Dies ist erforderlich, da das herkömmliche Setup bestimmte Datensätze in der Datenbank auffüllt, die nicht aufgefüllt werden, wenn Sie die Installation für eine bereits vorhandene Datenbank ausführen. Löschen Sie die folgenden Objekte:

    -   Löschen Sie unter "Servergruppen" "Standardservergruppe" den "Application Virtualization Management Server".

    -   Löschen Sie unter "Servergruppen" "Standardservergruppe"

    -   Löschen Sie unter "Anbieterrichtlinien" "Standardanbieter"



3.  Der Administrator in der Gruppe "App-V-Administratoren" sollte dann Folgendes erstellen:

    -   Erstellen Sie unter "Anbieterrichtlinien" eine neue Anbieterrichtlinie.

    -   Erstellen einer "Standardservergruppe"

        **Hinweis:**  
        Sie müssen eine Gruppe "Standardserver" erstellen, auch wenn Sie nicht verwendet werden. Das Serverinstallationsprogramm sucht nur nach der "Standardservergruppe", wenn versucht wird, den Server hinzuzufügen.  Wenn keine "Standardservergruppe" vorhanden ist, schlägt die Installation fehl. Wenn Sie andere Servergruppen als die standardeinstellung verwenden möchten, ist es nur erforderlich, die "Standardservergruppe" beizubehalten, wenn Sie beabsichtigen, ihrer Infrastruktur nachfolgende App-V-Verwaltungsserver hinzuzufügen.



~~~
-   Assign the App-V Users Group to the New Provider Policy created above

-   Under “Server Groups,” create a New Server Group, specifying the New Provider Policy

-   Under the New Server group, create a New Application Virtualization Management Server

    **Important**  
    Do not restart the service before completing all of the above steps!



-   Administrator restarts the Application Virtualization Management Server service.
~~~

## <a name="conclusion"></a>Fazit


Abschließend können Administratoren anhand der Informationen in diesem Dokument mit den SQL Administratoren einen Bereitstellungspfad entwickeln, der für die Sicherheits- und Verwaltungsabteilungen in einer Organisation funktioniert. Nachdem Sie dieses Dokument gelesen und die dokumentierten Aufgaben getestet haben, sollte ein Administrator bereit sein, seine App-V-Infrastruktur in dieser Art von Umgebung zu implementieren.









