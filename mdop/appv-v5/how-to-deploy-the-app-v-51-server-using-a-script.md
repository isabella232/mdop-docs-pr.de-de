---
title: So stellen Sie den App-V 5.1-Server mithilfe eines Skripts bereit
description: So stellen Sie den App-V 5.1-Server mithilfe eines Skripts bereit
author: dansimp
ms.assetid: 15c33d7b-9b61-4dbc-8674-399bb33e5f7e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/20/2020
ms.openlocfilehash: 579ca685f677aaaa4f5ebb6ac8d2969fdcbe2cd2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805495"
---
# So stellen Sie den App-V 5.1-Server mithilfe eines Skripts bereit

Um das Setup des **appv\_server\_setup.exe** Servers erfolgreich über die Befehlszeile abzuschließen, müssen Sie mehrere Parameter angeben und kombinieren.

## Installieren des App-V 5,1-Servers mithilfe eines Skripts

- Verwenden Sie die folgenden Informationen zum Installieren des App-V 5,1-Servers über die Befehlszeile.

    > [!NOTE]
    > Die Informationen in den folgenden Tabellen können auch über die Befehlszeile aufgerufen werden, indem Sie den folgenden Befehl eingeben: **appv\_server\_setup.exe/?**.

### Installieren des Verwaltungsservers und der Verwaltungsdatenbank auf einem lokalen Computer

Die folgenden Parameter sind sowohl für die standardmäßige als auch für die benutzerdefinierte Instanz von Microsoft SQL Server gültig:

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /DB_PREDEPLOY_MANAGEMENT
- /MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT
- /MANAGEMENT_DB_NAME

**Beispiel: Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement"
```

### Installieren des Verwaltungsservers mithilfe einer vorhandenen Verwaltungsdatenbank auf einem lokalen Computer

Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden (Unterschied zu benutzerdefinierter Instanz in *kursiv*Schrift):

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_MANAGEMENT_DB_NAME

Wenn Sie eine benutzerdefinierte Instanz von Microsoft SQL Server verwenden möchten, verwenden Sie die folgenden Parameter (Unterschied zur Standardinstanz in *Kursivformatierung*):

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /EXISTING_MANAGEMENT_DB_NAME

**Beispiel: Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### Installieren des Verwaltungsservers mithilfe einer vorhandenen Verwaltungsdatenbank auf einem Remotecomputer

Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden (Unterschied zu benutzerdefinierter Instanz in *kursiv*Schrift):

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_MANAGEMENT_DB_NAME

Wenn Sie eine benutzerdefinierte Instanz von Microsoft SQL Server verwenden möchten, verwenden Sie diese Parameter (Unterschied zur Standardinstanz in *kursiv*Schrift):

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /EXISTING_MANAGEMENT_DB_NAME

**Beispiel: Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME="SqlServermachine.domainName" /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### Installieren der Verwaltungsdatenbank und des Verwaltungsservers auf demselben Computer

Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden (Unterschied zu benutzerdefinierter Instanz in *kursiv*Schrift):

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_SERVER_MACHINE_USE_LOCAL
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

Wenn Sie eine benutzerdefinierte Instanz von Microsoft SQL Server verwenden möchten, verwenden Sie diese Parameter (Unterschied zur Standardinstanz in *kursiv*Schrift):

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_SERVER_MACHINE_USE_LOCAL
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

**Beispiel: Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_SERVER_MACHINE_USE_LOCAL /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Installieren der Verwaltungsdatenbank auf einem anderen Computer als dem Verwaltungsserver

Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden (Unterschied zu benutzerdefinierter Instanz in *kursiv*Schrift):

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

Wenn Sie eine benutzerdefinierte Instanz von Microsoft SQL Server verwenden möchten, verwenden Sie diese Parameter (Unterschied zur Standardinstanz in *kursiv*Schrift):

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

**Beispiel: Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Installieren des Veröffentlichungsservers

Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:

- /PUBLISHING_SERVER
- /PUBLISHING_MGT_SERVER
- /PUBLISHING_WEBSITE_NAME
- /PUBLISHING_WEBSITE_PORT

**Beispiel: Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /PUBLISHING_SERVER /PUBLISHING_MGT_SERVER="http://ManagementServerName:ManagementPort" /PUBLISHING_WEBSITE_NAME="Microsoft AppV Publishing Service" /PUBLISHING_WEBSITE_PORT="8081"
```

### Installieren des Berichtsservers und der Berichtsdatenbank auf einem lokalen Computer

Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden (Unterschied zu benutzerdefinierter Instanz in *kursiv*Schrift):

- /Reporting _SERVER
- /Reporting _WEBSITE_NAME
- /Reporting _WEBSITE_PORT
- /DB_PREDEPLOY_REPORTING
- */Reporting _DB_SQLINSTANCE_USE_DEFAULT*
- /Reporting _DB_NAME

Wenn Sie eine benutzerdefinierte Instanz von Microsoft SQL Server verwenden möchten, verwenden Sie diese Parameter (Unterschied zur Standardinstanz in *kursiv*Schrift):

- /Reporting _SERVER
- */Reporting _ADMINACCOUNT*
- /Reporting _WEBSITE_NAME
- /Reporting _WEBSITE_PORT
- /DB_PREDEPLOY_REPORTING
- */Reporting _DB_CUSTOM_SQLINSTANCE*
- /Reporting _DB_NAME

**Beispiel: Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting"
```

### Installieren des Berichtsservers und Verwenden einer vorhandenen Berichtsdatenbank auf einem lokalen Computer

Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden (Unterschied zu benutzerdefinierter Instanz in *kursiv*Schrift):

- /Reporting _SERVER
- /Reporting _WEBSITE_NAME
- /Reporting _WEBSITE_PORT
- /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_REPORTING _DB_NAME

Wenn Sie eine benutzerdefinierte Instanz von Microsoft SQL Server verwenden möchten, verwenden Sie diese Parameter (Unterschied zur Standardinstanz in *kursiv*Schrift):

- /Reporting _SERVER
- */Reporting _ADMINACCOUNT*
- /Reporting _WEBSITE_NAME
- /Reporting _WEBSITE_PORT
- /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE*
- /EXISTING_REPORTING _DB_NAME

**Beispiel: Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### Installieren des Berichtsservers mithilfe einer vorhandenen Berichtsdatenbank auf einem Remotecomputer

Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden (Unterschied zu benutzerdefinierter Instanz in *kursiv*Schrift):

- /Reporting _SERVER
- /Reporting _WEBSITE_NAME
- /Reporting _WEBSITE_PORT
- /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_REPORTING _DB_NAME

Wenn Sie eine benutzerdefinierte Instanz von Microsoft SQL Server verwenden möchten, verwenden Sie diese Parameter (Unterschied zur Standardinstanz in *kursiv*Schrift):

- /Reporting _SERVER
- */Reporting _ADMINACCOUNT*
- /Reporting _WEBSITE_NAME
- /Reporting _WEBSITE_PORT
- /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE*
- /EXISTING_REPORTING _DB_NAME

**Beispiel: Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME="SqlServerMachine.DomainName" /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### Installieren der Berichtsdatenbank auf demselben Computer wie der Berichtsserver

Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden (Unterschied zu benutzerdefinierter Instanz in *kursiv*Schrift):

- /DB_PREDEPLOY_REPORTING
- */Reporting _DB_SQLINSTANCE_USE_DEFAULT*
- /Reporting _DB_NAME
- /REPORTING_SERVER_MACHINE_USE_LOCAL
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

Wenn Sie eine benutzerdefinierte Instanz von Microsoft SQL Server verwenden möchten, verwenden Sie diese Parameter (Unterschied zur Standardinstanz in *kursiv*Schrift):

- /DB_PREDEPLOY_REPORTING
- */Reporting _DB_CUSTOM_SQLINSTANCE*
- /Reporting _DB_NAME
- /REPORTING_SERVER_MACHINE_USE_LOCAL
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

**Beispiel: Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_SERVER_MACHINE_USE_LOCAL /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Installieren der Berichtsdatenbank auf einem anderen Computer als dem Berichtsserver

Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden (Unterschied zu benutzerdefinierter Instanz in *kursiv*Schrift):

- /DB_PREDEPLOY_REPORTING
- /Reporting _DB_SQLINSTANCE_USE_DEFAULT
- /Reporting _DB_NAME
- /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

Wenn Sie eine benutzerdefinierte Instanz von Microsoft SQL Server verwenden möchten, verwenden Sie diese Parameter (Unterschied zur Standardinstanz in *kursiv*Schrift):

- /DB_PREDEPLOY_REPORTING
- /Reporting _DB_CUSTOM_SQLINSTANCE
- /Reporting _DB_NAME
- /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

**Beispiel: Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server:**

```dos
 appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Parameter Definitionen

#### Allgemeine Parameter

| Parameter | Information |
|--|--|
| /Quiet | Gibt die unbeaufsichtigte Installation an. |
| /Uninstall | Gibt eine Deinstallation an. |
| /LAYOUT | Gibt die Layout-Aktion an. Dadurch werden die MSIs-und Skriptdateien in einen Ordner extrahiert, ohne das Produkt tatsächlich zu installieren. Es wird kein Wert erwartet. |
| /LAYOUTDIR | Gibt das layoutverzeichnis an. Nimmt eine Zeichenfolge an. Verwendungsbeispiel: **/LAYOUTDIR = "C:\\Application Virtualization Server"** |
| /INSTALLDIR | Gibt das Installationsverzeichnis an. Nimmt eine Zeichenfolge an. Beispiel Verwendung: **/INSTALLDIR = "c:\\Programme Files\\Application Virtualization\\Server"** |
| /MUOPTIN | Aktiviert Microsoft Update. Es wird kein Wert erwartet. |
| /ACCEPTEULA | Akzeptiert den Lizenzvertrag. Dies ist für eine unbeaufsichtigte Installation erforderlich. Verwendungsbeispiel: **/ACCEPTEULA** oder **/ACCEPTEULA = 1** |

#### Verwaltungs Server-Installationsparameter

|Parameter |Information |
|--|--|
| /MANAGEMENT_SERVER | Gibt an, dass der Verwaltungsserver installiert wird. Kein Wert erwartet |
| /MANAGEMENT_ADMINACCOUNT | Gibt das Konto an, dem Administrator Zugriff auf den Verwaltungsserver gewährt wird. Dies kann ein Benutzerkonto oder eine Gruppe sein. Beispiel Verwendung: **/MANAGEMENT_ADMINACCOUNT = "mydomain\\admin"**. Wenn **/MANAGEMENT_SERVER** nicht angegeben ist, wird diese ignoriert. |
| /MANAGEMENT_WEBSITE_NAME | Gibt den Namen der Website an, die für den Verwaltungsdienst erstellt wird. Beispiel Verwendung: **/MANAGEMENT_WEBSITE_NAME = "Microsoft App-V-Verwaltungsdienst"** |
| MANAGEMENT_WEBSITE_PORT | Gibt die Portnummer an, die vom Verwaltungsdienst verwendet wird. Verwendungsbeispiel: **/MANAGEMENT_WEBSITE_PORT = 82** |

#### Parameter für die Verwaltungs Server-Datenbank

| Parameter | Information |
|--|--|
| /DB_PREDEPLOY_MANAGEMENT | Gibt an, dass die Verwaltungsdatenbank installiert wird. Sie müssen über ausreichende Datenbankberechtigungen verfügen, um diese Installation abzuschließen. Es wird kein Wert erwartet. |
| /MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT | Gibt an, dass die SQL-Standardinstanz verwendet werden soll. Es wird kein Wert erwartet. |
| /MANAGEMENT_DB_ CUSTOM_SQLINSTANCE | Gibt den Namen der benutzerdefinierten SQL-Instanz an, die zum Erstellen einer neuen Datenbank verwendet werden soll. Beispiel Verwendung: **/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "MySqlServer"**. Wenn **/DB_PREDEPLOY_MANAGEMENT** nicht angegeben ist, wird diese ignoriert. |
| /MANAGEMENT_DB_NAME | Gibt den Namen der neuen Verwaltungsdatenbank an, die erstellt werden soll. Beispiel Verwendung: **/MANAGEMENT_DB_NAME = "AppVMgmtDB"**. Wenn **/DB_PREDEPLOY_MANAGEMENT** nicht angegeben ist, wird diese ignoriert. |
| /MANAGEMENT_SERVER_MACHINE_USE_LOCAL | Gibt an, ob der Verwaltungsserver, der auf die Datenbank zugreifen soll, auf dem lokalen Server installiert ist. Parameter wechseln, damit kein Wert erwartet wird. |
| /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT | Gibt das Computerkonto des Remotecomputers an, auf dem der Verwaltungsserver installiert wird. Verwendungsbeispiel: **/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\\computername"** |
| /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT | Gibt das Administrator Konto an, das zum Installieren des Verwaltungsservers verwendet wird. Verwendungsbeispiel: **/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"** |

#### Parameter für die Installation des Veröffentlichungsservers

| Parameter | Information |
|--|--|
| /PUBLISHING_SERVER | Gibt an, dass der Veröffentlichungs Server installiert wird. Es wird kein Wert erwartet. |
| /PUBLISHING_MGT_SERVER | Gibt die URL des Verwaltungsdiensts an, mit dem der Veröffentlichungsserver eine Verbindung herstellen soll. Verwendungsbeispiel: **http://- &lt; Verwaltungsservername &gt; : &lt; Verwaltungsserver- &gt; Portnummer**. Wenn **/PUBLISHING_SERVER** nicht verwendet wird, wird dieser Parameter ignoriert. |
| /PUBLISHING_WEBSITE_NAME | Gibt den Namen der Website an, die für den Veröffentlichungsdienst erstellt wird. Beispiel Verwendung: **/PUBLISHING_WEBSITE_NAME = "Microsoft App-V Publishing Service"** |
| /PUBLISHING_WEBSITE_PORT | Gibt die vom Veröffentlichungsdienst verwendete Portnummer an. Verwendungsbeispiel: **/PUBLISHING_WEBSITE_PORT = 83** |

#### Parameter für Reporting Server

| Parameter | Information |
|--|--|
| /REPORTING_SERVER | Gibt an, dass der Berichts Server installiert wird. Es wird kein Wert erwartet. |
| /REPORTING_WEBSITE_NAME | Gibt den Namen der Website an, die für den Berichterstellungsdienst erstellt wird. Beispiel Verwendung: **/REPORTING_WEBSITE_NAME = "Microsoft App-V ReportingService"** |
| /REPORTING_WEBSITE_PORT | Gibt die Portnummer an, die vom Berichterstattungsdienst verwendet wird. Verwendungsbeispiel: **/REPORTING_WEBSITE_PORT = 82** |

#### Parameter für die Verwendung einer vorhandenen Berichts Server-Datenbank

| Parameter | Information |
|--|--|
| /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL | Gibt an, dass Microsoft SQL Server auf dem lokalen Server installiert ist. Parameter wechseln, damit kein Wert erwartet wird. |
| /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME | Gibt den Namen des Remotecomputers an, auf dem SQL Server installiert ist. Nimmt eine Zeichenfolge an. Verwendungsbeispiel: **/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"** |
| /EXISTING_ Berichterstellung _DB_SQLINSTANCE_USE_DEFAULT | Gibt an, dass die SQL-Standardinstanz verwendet werden soll. Parameter wechseln, damit kein Wert erwartet wird. |
| /EXISTING_ REPORTING_DB_CUSTOM_SQLINSTANCE | Gibt den Namen der benutzerdefinierten SQL-Instanz an, die verwendet werden soll. Nimmt eine Zeichenfolge an. Beispiel Verwendung: **/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = "MySqlServer"** |
| /EXISTING_ Berichterstellung _DB_NAME | Gibt den Namen der vorhandenen Berichtsdatenbank an, die verwendet werden soll. Nimmt eine Zeichenfolge an. Verwendungsbeispiel: **/EXISTING_REPORTING_DB_NAME = "AppVReporting"** |

#### Parameter für die Installation der Berichts Server-Datenbank

| Parameter | Information |
|--|--|
| /DB_PREDEPLOY_REPORTING | Gibt an, dass die Berichtsdatenbank installiert wird. Für diese Installation sind DBA-Berechtigungen erforderlich. Es wird kein Wert erwartet. |
| /REPORTING_DB_SQLINSTANCE_USE_DEFAULT | Gibt den Namen der benutzerdefinierten SQL-Instanz an, die verwendet werden soll. Nimmt eine Zeichenfolge an. Beispiel Verwendung: **/REPORTING_DB_ CUSTOM_SQLINSTANCE = "MySqlServer"** |
| /REPORTING_DB_NAME | Gibt den Namen der neuen Berichtsdatenbank an, die erstellt werden soll. Nimmt eine Zeichenfolge an. Verwendungsbeispiel: **/REPORTING_DB_NAME = "AppVMgmtDB"** |
| /REPORTING_SERVER_MACHINE_USE_LOCAL | Gibt an, dass der Berichtsserver, auf den die Datenbank zugreifen soll, auf dem lokalen Server installiert ist. Parameter wechseln, damit kein Wert erwartet wird. |
| /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT | Gibt das Computerkonto des Remotecomputers an, auf dem der Berichtsserver installiert wird. Nimmt eine Zeichenfolge an. Verwendungsbeispiel: **/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\ComputerName"** |
| /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT | Gibt das Administrator Konto an, das zum Installieren des App-V-Berichtsservers verwendet wird. Nimmt eine Zeichenfolge an. Verwendungsbeispiel: **/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"** |

#### Parameter für die Verwendung einer vorhandenen Verwaltungs Server-Datenbank

| Parameter | Information |
|--|--|
| /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL | Gibt an, dass SQL Server auf dem lokalen Server installiert ist. Parameter wechseln, damit kein Wert erwartet wird. Wenn **/DB_PREDEPLOY_MANAGEMENT** angegeben ist, wird diese ignoriert. |
| /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME | Gibt den Namen des Remotecomputers an, auf dem SQL Server installiert ist. Nimmt eine Zeichenfolge an. Verwendungsbeispiel: **/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"** |
| /EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT | Gibt an, dass die SQL-Standardinstanz verwendet werden soll. Parameter wechseln, damit kein Wert erwartet wird. Wenn **/DB_PREDEPLOY_MANAGEMENT** angegeben ist, wird diese ignoriert. |
| /EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE | Gibt den Namen der benutzerdefinierten SQL-Instanz an, die verwendet werden soll. Beispiel Verwendung **/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement"**. Wenn **/DB_PREDEPLOY_MANAGEMENT** angegeben ist, wird diese ignoriert. |
| /EXISTING_MANAGEMENT_DB_NAME | Gibt den Namen der vorhandenen Verwaltungsdatenbank an, die verwendet werden soll. Beispiel Verwendung: **/EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB"**. Wenn **/DB_PREDEPLOY_MANAGEMENT** angegeben ist, wird diese ignoriert. |

Sie haben ein App-V-Problem? Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen

[Bereitstellen des App-V 5.1-Servers](deploying-the-app-v-51-server.md)
