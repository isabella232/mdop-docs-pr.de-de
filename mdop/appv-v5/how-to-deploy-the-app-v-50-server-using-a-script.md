---
title: So stellen Sie den App-V 5.0-Server mithilfe eines Skripts bereit
description: So stellen Sie den App-V 5.0-Server mithilfe eines Skripts bereit
author: dansimp
ms.assetid: b91a35c8-df9e-4065-9187-abafbe565b84
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: aeb16d166fe7b1c4bb418c212024c49f6b151b94
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805525"
---
# So stellen Sie den App-V 5.0-Server mithilfe eines Skripts bereit


Um das Setup des **appv\_server\_setup.exe** Servers erfolgreich über die Befehlszeile abzuschließen, müssen Sie mehrere Parameter angeben und kombinieren.

Verwenden Sie die folgenden Tabellen, um weitere Informationen zum Installieren des App-V 5,0-Servers über die Befehlszeile zu erhalten.

>[!NOTE]
> Die Informationen in den folgenden Tabellen können auch über die Befehlszeile aufgerufen werden, indem Sie den folgenden Befehl eingeben:
>```
> appv\_server\_setup.exe /?
>```

## Allgemeine Parameter und Beispiele

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>So installieren Sie den Verwaltungsserver und die Verwaltungsdatenbank auf einem lokalen Computer</p></td>
    <td align="left"><p>Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Verwenden Sie die folgenden Parameter, um eine benutzerdefinierte Instanz von Microsoft SQL Server zu verwenden:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server-Beispiel:</p>
    <p>/appv_server_setup.exe/quiet</p>
    <p>/MANAGEMENT_SERVER</p>
    <p>/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</p>
    <p>/MANAGEMENT_WEBSITE_NAME = "Microsoft AppV-Verwaltungsdienst"</p>
    <p>/MANAGEMENT_WEBSITE_PORT = "8080"</p>
    <p>/DB_PREDEPLOY_MANAGEMENT</p>
    <p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/MANAGEMENT_DB_NAME = "AppVManagement"</p></td>
    </tr>
    </tbody>
    </table>
     
<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>So installieren Sie den Verwaltungsserver mithilfe einer vorhandenen Verwaltungsdatenbank auf einem lokalen Computer</p></td>
    <td align="left"><p>Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Verwenden Sie die folgenden Parameter, um eine benutzerdefinierte Instanz von Microsoft SQL Server zu verwenden:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server-Beispiel:</p>
    <p>/appv_server_setup.exe/quiet</p>
    <p>/MANAGEMENT_SERVER</p>
    <p>/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</p>
    <p>/MANAGEMENT_WEBSITE_NAME = "Microsoft AppV-Verwaltungsdienst"</p>
    <p>/MANAGEMENT_WEBSITE_PORT = "8080"</p>
    <p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p>
    <p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</p></td>
    </tr>
    </tbody>
    </table>  

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>So installieren Sie den Verwaltungsserver mithilfe einer vorhandenen Verwaltungsdatenbank auf einem Remotecomputer</p></td>
    <td align="left"><p>Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Verwenden Sie die folgenden Parameter, um eine benutzerdefinierte Instanz von Microsoft SQL Server zu verwenden:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server-Beispiel:</p>
    <p>/appv_server_setup.exe/quiet</p>
    <p>/MANAGEMENT_SERVER</p>
    <p>/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</p>
    <p>/MANAGEMENT_WEBSITE_NAME = "Microsoft AppV-Verwaltungsdienst"</p>
    <p>/MANAGEMENT_WEBSITE_PORT = "8080"</p>
    <p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME = "Sie SQLSERVERMACHINE. Domain Name"</p>
    <p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</p></td>
    </tr>
    </tbody>
    </table>
    
<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>So installieren Sie die Verwaltungsdatenbank und den Verwaltungs Server auf demselben Computer</p></td>
    <td align="left"><p>Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Verwenden Sie die folgenden Parameter, um eine benutzerdefinierte Instanz von Microsoft SQL Server zu verwenden:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server-Beispiel:</p>
    <p>/appv_server_setup.exe/quiet</p>
    <p>/DB_PREDEPLOY_MANAGEMENT</p>
    <p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/MANAGEMENT_DB_NAME = "AppVManagement"</p>
    <p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p>
    <p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>So installieren Sie die Verwaltungsdatenbank auf einem anderen Computer als der Verwaltungsserver</p></td>
    <td align="left"><p>Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Verwenden Sie die folgenden Parameter, um eine benutzerdefinierte Instanz von Microsoft SQL Server zu verwenden:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server-Beispiel:</p>
    <p>/appv_server_setup.exe/quiet</p>
    <p>/DB_PREDEPLOY_MANAGEMENT</p>
    <p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/MANAGEMENT_DB_NAME = "AppVManagement"</p>
    <p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</p>
    <p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>So installieren Sie den Veröffentlichungsserver</p></td>
    <td align="left"><p>Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</p>
    <ul>
    <li><p>/PUBLISHING_SERVER</p></li>
    <li><p>/PUBLISHING_MGT_SERVER</p></li>
    <li><p>/PUBLISHING_WEBSITE_NAME</p></li>
    <li><p>/PUBLISHING_WEBSITE_PORT</p></li>
    </ul>
    <p>Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server-Beispiel:</p>
    <p>/appv_server_setup.exe/quiet</p>
    <p>/PUBLISHING_SERVER</p>
    <p>/PUBLISHING_MGT_SERVER = " http://ManagementServerName:ManagementPort "</p>
    <p>/PUBLISHING_WEBSITE_NAME = "Microsoft AppV Publishing Service"</p>
    <p>/PUBLISHING_WEBSITE_PORT = "8081"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>So installieren Sie den Berichtsserver und die Berichtsdatenbank auf einem lokalen Computer</p></td>
    <td align="left"><p>Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</p>
    <ul>
    <li><p>/Reporting _SERVER</p></li>
    <li><p>/Reporting _WEBSITE_NAME</p></li>
    <li><p>/Reporting _WEBSITE_PORT</p></li>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/Reporting _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/Reporting _DB_NAME</p></li>
    </ul>
    <p>Verwenden Sie die folgenden Parameter, um eine benutzerdefinierte Instanz von Microsoft SQL Server zu verwenden:</p>
    <ul>
    <li><p>/Reporting _SERVER</p></li>
    <li><p>/Reporting _ADMINACCOUNT</p></li>
    <li><p>/Reporting _WEBSITE_NAME</p></li>
    <li><p>/Reporting _WEBSITE_PORT</p></li>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/Reporting _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/Reporting _DB_NAME</p></li>
    </ul>
    <p>Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server-Beispiel:</p>
    <ul>
    <li><p>/appv_server_setup.exe/quiet</p></li>
    <li><p>/REPORTING_SERVER</p></li>
    <li><p>/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</p></li>
    <li><p>/REPORTING_WEBSITE_PORT = "8082"</p></li>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p></li>
    <li><p>/REPORTING_DB_NAME = "AppVReporting"</p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>So installieren Sie den Berichtsserver und verwenden eine vorhandene Berichtsdatenbank auf einem lokalen Computer</p></td>
    <td align="left"><p>Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</p>
    <ul>
    <li><p>/Reporting _SERVER</p></li>
    <li><p>/Reporting _WEBSITE_NAME</p></li>
    <li><p>/Reporting _WEBSITE_PORT</p></li>
    <li><p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Verwenden Sie die folgenden Parameter, um eine benutzerdefinierte Instanz von Microsoft SQL Server zu verwenden:</p>
    <ul>
    <li><p>/Reporting _SERVER</p></li>
    <li><p>/Reporting _ADMINACCOUNT</p></li>
    <li><p>/Reporting _WEBSITE_NAME</p></li>
    <li><p>/Reporting _WEBSITE_PORT</p></li>
    <li><p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server-Beispiel:</p>
    <p>/appv_server_setup.exe/quiet</p>
    <p>/REPORTING_SERVER</p>
    <p>/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</p>
    <p>/REPORTING_WEBSITE_PORT = "8082"</p>
    <p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p>
    <p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/EXITING_REPORTING_DB_NAME = "AppVReporting"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>So installieren Sie den Berichtsserver mithilfe einer vorhandenen Berichtsdatenbank auf einem Remotecomputer</p></td>
    <td align="left"><p>Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</p>
    <ul>
    <li><p>/Reporting _SERVER</p></li>
    <li><p>/Reporting _WEBSITE_NAME</p></li>
    <li><p>/Reporting _WEBSITE_PORT</p></li>
    <li><p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Verwenden Sie die folgenden Parameter, um eine benutzerdefinierte Instanz von Microsoft SQL Server zu verwenden:</p>
    <ul>
    <li><p>/Reporting _SERVER</p></li>
    <li><p>/Reporting _ADMINACCOUNT</p></li>
    <li><p>/Reporting _WEBSITE_NAME</p></li>
    <li><p>/Reporting _WEBSITE_PORT</p></li>
    <li><p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server-Beispiel:</p>
    <p>/appv_server_setup.exe/quiet</p>
    <p>/REPORTING_SERVER</p>
    <p>/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</p>
    <p>/REPORTING_WEBSITE_PORT = "8082"</p>
    <p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME = "Sie SQLSERVERMACHINE. Domain Name"</p>
    <p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/EXITING_REPORTING_DB_NAME = "AppVReporting"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>So installieren Sie die Berichtsdatenbank auf demselben Computer wie der Berichtsserver</p></td>
    <td align="left"><p>Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/Reporting _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/Reporting _DB_NAME</p></li>
    <li><p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Verwenden Sie die folgenden Parameter, um eine benutzerdefinierte Instanz von Microsoft SQL Server zu verwenden:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/Reporting _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/Reporting _DB_NAME</p></li>
    <li><p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server-Beispiel:</p>
    <p>/appv_server_setup.exe/quiet</p>
    <p>/DB_PREDEPLOY_REPORTING</p>
    <p>/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/REPORTING_DB_NAME = "AppVReporting"</p>
    <p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p>
    <p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>So installieren Sie die Berichtsdatenbank auf einem anderen Computer als der Berichtsserver</p></td>
    <td align="left"><p>Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/Reporting _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/Reporting _DB_NAME</p></li>
    <li><p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Verwenden Sie die folgenden Parameter, um eine benutzerdefinierte Instanz von Microsoft SQL Server zu verwenden:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/Reporting _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/Reporting _DB_NAME</p></li>
    <li><p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server-Beispiel:</p>
    <p>/appv_server_setup.exe/quiet</p>
    <p>/DB_PREDEPLOY_REPORTING</p>
    <p>/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/REPORTING_DB_NAME = "AppVReporting"</p>
    <p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</p>
    <p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
    </tr>
    </tbody>
    </table>

## Parameter Definitionen

### Allgemeine Parameter

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parameter</th>
    <th align="left">Information</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/Quiet</p></td>
    <td align="left"><p>Gibt die unbeaufsichtigte Installation an.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/Uninstall</p></td>
    <td align="left"><p>Gibt eine Deinstallation an.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/LAYOUT</p></td>
    <td align="left"><p>Gibt die Layout-Aktion an. Dadurch werden die MSIs-und Skriptdateien in einen Ordner extrahiert, ohne das Produkt tatsächlich zu installieren. Es wird kein Wert erwartet.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/LAYOUTDIR</p></td>
    <td align="left"><p>Gibt das layoutverzeichnis an. Nimmt eine Zeichenfolge an. Beispiel:/LAYOUTDIR = "C:\Application Virtualization Server"</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/INSTALLDIR</p></td>
    <td align="left"><p>Gibt das Installationsverzeichnis an. Nimmt eine Zeichenfolge an. z.B. /INSTALLDIR = "C:\Program Files\Application Virtualization\Server"</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MUOPTIN</p></td>
    <td align="left"><p>Aktiviert Microsoft Update. Kein Wert erwartet</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/ACCEPTEULA</p></td>
    <td align="left"><p>Akzeptiert den Lizenzvertrag. Dies ist für eine unbeaufsichtigte Installation erforderlich. Beispiel Verwendung: <strong> /ACCEPTEULA </strong> oder <strong> /ACCEPTEULA = 1 </strong> .</p></td>
    </tr>
    </tbody>
    </table>

### Verwaltungs Server-Installationsparameter

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parameter</th>
    <th align="left">Information</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_SERVER</p></td>
    <td align="left"><p>Gibt an, dass der Verwaltungsserver installiert wird. Kein Wert erwartet</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_ADMINACCOUNT</p></td>
    <td align="left"><p>Gibt das Konto an, das dem Administrator Zugriff auf den Verwaltungsserver gewährt wird. dieses Konto kann ein einzelnes Benutzerkonto oder eine Gruppe sein. Beispiel Verwendung: <strong> /MANAGEMENT_ADMINACCOUNT = "mydomain\admin" </strong> . Wenn <strong> /MANAGEMENT_SERVER </strong> nicht angegeben ist, wird diese ignoriert. Gibt das Konto an, das dem Administrator Zugriff auf den Verwaltungsserver gewährt wird. Dies kann ein Benutzerkonto oder eine Gruppe sein. Beispiel: <strong> /MANAGEMENT_ADMINACCOUNT = &quot; mydomain\admin &quot; </strong> .</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_WEBSITE_NAME</p></td>
    <td align="left"><p>Gibt den Namen der Website an, die für den Verwaltungsdienst erstellt wird. Beispiel:/MANAGEMENT_WEBSITE_NAME = "Microsoft App-V-Verwaltungsdienst"</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>MANAGEMENT_WEBSITE_PORT</p></td>
    <td align="left"><p>Gibt die Portnummer an, die vom Verwaltungsdienst verwendet wird. Beispiel:/MANAGEMENT_WEBSITE_PORT = 82.</p></td>
    </tr>
    </tbody>
    </table>

### Parameter für die Verwaltungs Server-Datenbank

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parameter</th>
    <th align="left">Information</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/DB_PREDEPLOY_MANAGEMENT</p></td>
    <td align="left"><p>Gibt an, dass die Verwaltungsdatenbank installiert wird. Sie müssen über ausreichende Datenbankberechtigungen verfügen, um diese Installation abzuschließen. Kein Wert erwartet</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></td>
    <td align="left"><p>Gibt an, dass die SQL-Standardinstanz verwendet werden soll. Es wird kein Wert erwartet.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</p></td>
    <td align="left"><p>Gibt den Namen der benutzerdefinierten SQL-Instanz an, die zum Erstellen einer neuen Datenbank verwendet werden soll. Beispiel Verwendung: <strong> /MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "MySqlServer" </strong> . Wenn/DB_PREDEPLOY_MANAGEMENT nicht angegeben ist, wird diese ignoriert.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_DB_NAME</p></td>
    <td align="left"><p>Gibt den Namen der neuen Verwaltungsdatenbank an, die erstellt werden soll. Beispiel Verwendung: <strong> /MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> . Wenn/DB_PREDEPLOY_MANAGEMENT nicht angegeben ist, wird diese ignoriert.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></td>
    <td align="left"><p>Gibt an, ob der Verwaltungsserver, der auf die Datenbank zugreifen soll, auf dem lokalen Server installiert ist. Parameter wechseln, damit kein Wert erwartet wird.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
    <td align="left"><p>Gibt das Computerkonto des Remotecomputers an, auf dem der Verwaltungsserver installiert wird. Verwendungsbeispiel: <strong> /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\ComputerName"</strong></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
    <td align="left"><p>Gibt das Administrator Konto an, das zum Installieren des Verwaltungsservers verwendet wird. Verwendungsbeispiel: <strong> /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "DOMAIN\alias"</strong></p></td>
    </tr>
    </tbody>
    </table>

### Parameter für die Installation des Veröffentlichungsservers

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parameter</th>
    <th align="left">Information</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/PUBLISHING_SERVER</p></td>
    <td align="left"><p>Gibt an, dass der Veröffentlichungs Server installiert wird. Kein Wert erwartet</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/PUBLISHING_MGT_SERVER</p></td>
    <td align="left"><p>Gibt die URL des Verwaltungsdiensts an, mit dem der Veröffentlichungsserver eine Verbindung herstellen soll. Verwendungsbeispiel: <strong> http:// &lt; -Verwaltungsservername &gt; : &lt; Verwaltungsserver-Portnummer &gt; </strong> . Wenn/PUBLISHING_SERVER nicht verwendet wird, wird dieser Parameter ignoriert.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/PUBLISHING_WEBSITE_NAME</p></td>
    <td align="left"><p>Gibt den Namen der Website an, die für den Veröffentlichungsdienst erstellt wird. Beispiel:/PUBLISHING_WEBSITE_NAME = "Microsoft App-V Publishing Service"</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/PUBLISHING_WEBSITE_PORT</p></td>
    <td align="left"><p>Gibt die vom Veröffentlichungsdienst verwendete Portnummer an. Beispiel:/PUBLISHING_WEBSITE_PORT = 83</p></td>
    </tr>
    </tbody>
    </table>

### Parameter für Reporting Server

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parameter</th>
    <th align="left">Information</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/REPORTING_SERVER</p></td>
    <td align="left"><p>Gibt an, dass der Berichts Server installiert wird. Kein Wert erwartet</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_WEBSITE_NAME</p></td>
    <td align="left"><p>Gibt den Namen der Website an, die für den Berichterstellungsdienst erstellt wird. z.B. /REPORTING_WEBSITE_NAME = &quot; Microsoft App-V ReportingService&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/REPORTING_WEBSITE_PORT</p></td>
    <td align="left"><p>Gibt die Portnummer an, die vom Berichterstattungsdienst verwendet wird. z.B. /REPORTING_WEBSITE_PORT = 82</p></td>
    </tr>
    </tbody>
    </table>

     

### Parameter für die Verwendung einer vorhandenen Berichts Server-Datenbank

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parameter</th>
    <th align="left">Information</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p></td>
    <td align="left"><p>Gibt an, dass Microsoft SQL Server auf dem lokalen Server installiert ist. Parameter wechseln, damit kein Wert erwartet wird.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</p></td>
    <td align="left"><p>Gibt den Namen des Remotecomputers an, auf dem SQL Server installiert ist. Nimmt eine Zeichenfolge an. z.B. /EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/EXISTING_ Berichterstellung <em> DB_SQLINSTANCE_USE_DEFAULT</p></td>
    <td align="left"><p>Gibt an, dass die SQL-Standardinstanz verwendet werden soll. Parameter wechseln, damit kein Wert erwartet wird.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING </em> REPORTING_DB_CUSTOM_SQLINSTANCE</p></td>
    <td align="left"><p>Gibt den Namen der benutzerdefinierten SQL-Instanz an, die verwendet werden soll. Nimmt eine Zeichenfolge an. z.B. /EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = &quot; MySQLServer&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/EXISTING_ Berichterstellung _DB_NAME</p></td>
    <td align="left"><p>Gibt den Namen der vorhandenen Berichtsdatenbank an, die verwendet werden soll. Nimmt eine Zeichenfolge an. z.B. /EXISTING_REPORTING_DB_NAME = &quot; AppVReporting&quot;</p></td>
    </tr>
    </tbody>
    </table>

### Parameter für die Installation der Berichts Server-Datenbank

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parameter</th>
    <th align="left">Information</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/DB_PREDEPLOY_REPORTING</p></td>
    <td align="left"><p>Gibt an, dass die Berichtsdatenbank installiert wird. Für diese Installation sind DBA-Berechtigungen erforderlich. Kein Wert erwartet</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</p></td>
    <td align="left"><p>Gibt den Namen der benutzerdefinierten SQL-Instanz an, die verwendet werden soll. Nimmt eine Zeichenfolge an. z.B. /REPORTING_DB_ CUSTOM_SQLINSTANCE = &quot; MySQLServer&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/REPORTING_DB_NAME</p></td>
    <td align="left"><p>Gibt den Namen der neuen Berichtsdatenbank an, die erstellt werden soll. Nimmt eine Zeichenfolge an. z.B. /REPORTING_DB_NAME = &quot; AppVMgmtDB&quot;</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p></td>
    <td align="left"><p>Gibt an, dass der Berichtsserver, auf den die Datenbank zugreifen soll, auf dem lokalen Server installiert ist. Parameter wechseln, damit kein Wert erwartet wird.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
    <td align="left"><p>Gibt das Computerkonto des Remotecomputers an, auf dem der Berichtsserver installiert wird. Nimmt eine Zeichenfolge an. z.B. /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = &quot; Domain\ComputerName&quot;</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
    <td align="left"><p>Gibt das Administrator Konto an, das zum Installieren des App-V-Berichtsservers verwendet wird. Nimmt eine Zeichenfolge an. z.B. /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = &quot; DOMAIN\alias&quot;</p></td>
    </tr>
    </tbody>
    </table>

### Parameter für die Verwendung einer vorhandenen Verwaltungs Server-Datenbank

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parameter</th>
    <th align="left">Information</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p></td>
    <td align="left"><p>Gibt an, dass SQL Server auf dem lokalen Server installiert ist. Parameter wechseln, damit kein Wert erwartet wird. Wenn/DB_PREDEPLOY_MANAGEMENT angegeben ist, wird diese ignoriert.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</p></td>
    <td align="left"><p>Gibt den Namen des Remotecomputers an, auf dem SQL Server installiert ist. Nimmt eine Zeichenfolge an. z.B. /EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></td>
    <td align="left"><p>Gibt an, dass die SQL-Standardinstanz verwendet werden soll. Parameter wechseln, damit kein Wert erwartet wird. Wenn/DB_PREDEPLOY_MANAGEMENT angegeben ist, wird diese ignoriert.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</p></td>
    <td align="left"><p>Gibt den Namen der benutzerdefinierten SQL-Instanz an, die verwendet werden soll. Beispiel Verwendung <strong> /EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement" </strong> . Wenn/DB_PREDEPLOY_MANAGEMENT angegeben ist, wird diese ignoriert.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_NAME</p></td>
    <td align="left"><p>Gibt den Namen der vorhandenen Verwaltungsdatenbank an, die verwendet werden soll. Beispiel Verwendung: <strong> /EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> . Wenn/DB_PREDEPLOY_MANAGEMENT angegeben ist, wird diese ignoriert.</p>
    <p></p>
    <p><strong>Sie haben einen Vorschlag für App-V </strong> ? Hier können Sie Vorschläge hinzufügen oder abstimmen <a href="http://appv.uservoice.com/forums/280448-microsoft-application-virtualization" data-raw-source="[here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)"> </a> . <strong>Haben Sie eine App-V Issu </strong> e? Verwenden Sie das <a href="https://social.technet.microsoft.com/Forums/home?forum=mdopappv" data-raw-source="[App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)"> App-V TechNet-Forum </a> .</p></td>
</tr>
</tbody>
</table>
  

## Verwandte Themen

[Bereitstellen des App-V 5.0-Servers](deploying-the-app-v-50-server.md)

 

 





