---
title: So stellen Sie die App-V-Datenbanken mithilfe von SQL-Skripts bereit
description: So stellen Sie die App-V-Datenbanken mithilfe von SQL-Skripts bereit
author: dansimp
ms.assetid: 23637936-475f-4ca5-adde-76bb27d2372b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 511d1020571eead25af9e9591fe1834a9f97f068
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805483"
---
# So stellen Sie die App-V-Datenbanken mithilfe von SQL-Skripts bereit


Verwenden Sie die folgenden Anweisungen, um SQL-Skripts anstelle des Windows Installers zu verwenden:

-   Installieren der App-V 5,0-Datenbanken

-   Aktualisieren der 5,0-Datenbanken auf eine neuere Version

**Installieren der App-V-Datenbanken mithilfe von SQL-Skripts**

1. Bevor Sie die Datenbankskripts installieren, überprüfen und belassen Sie eine Kopie der App-V-Lizenzbestimmungen. Durch Ausführen der Datenbankskripts erklären Sie sich mit den Lizenzbedingungen einverstanden. Wenn Sie diese nicht akzeptieren, sollten Sie diese Software nicht verwenden.

2. Kopieren Sie die **appv\_server\_setup.exe** aus dem App-V-Veröffentlichungsmedium an einen temporären Speicherort.

3. Führen Sie an einer Eingabeaufforderung **appv\_server\_setup.exe** aus, und geben Sie einen temporären Speicherort zum Extrahieren der Datenbankskripts an.

   Beispiel: appv\_server\_setup.exe/Layout c:\\ &lt; temporären Standort Pfad&gt;

4. Navigieren Sie zu dem temporären Speicherort, den Sie erstellt haben, öffnen Sie den extrahierten **DatabaseScripts** -Ordner, und überprüfen Sie die entsprechende Readme.txt Datei, um Anweisungen zu erhalten:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Datenbank</th>
   <th align="left">Speicherort der Readme.txt zu verwendenden Datei</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Verwaltungsdatenbank</p></td>
   <td align="left"><p>ManagementDatabase-Unterordner</p>
   <div class="alert">
   <strong>Wichtig</strong><br/><p>Wenn Sie die APP-v 5,0 SP3-Verwaltungsdatenbank aktualisieren oder installieren, finden Sie weitere Informationen unter <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> SQL-Skripts zum Installieren oder Aktualisieren der APP-v 5,0 SP3-Verwaltungs Server-Datenbank Fehler </a> .</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Berichtsdatenbank</p></td>
   <td align="left"><p>ReportingDatabase-Unterordner</p></td>
   </tr>
   </tbody>
   </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Verwandte Themen


[Bereitstellen des App-V 5.0-Servers](deploying-the-app-v-50-server.md)

[So stellen Sie den App-V 5.0-Server bereit](how-to-deploy-the-app-v-50-server-50sp3.md)









