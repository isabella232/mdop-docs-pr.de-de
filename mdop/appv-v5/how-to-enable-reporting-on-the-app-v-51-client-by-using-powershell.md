---
title: So aktivieren Sie die Berichterstellung auf dem App-V 5.1-Client mithilfe von PowerShell
description: So aktivieren Sie die Berichterstellung auf dem App-V 5.1-Client mithilfe von PowerShell
author: dansimp
ms.assetid: c4c58be6-cc50-44f6-bf4f-8346fc5d0c0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1d8c0d5e1930020ed1ce354f806f8917a9644e02
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805453"
---
# So aktivieren Sie die Berichterstellung auf dem App-V 5.1-Client mithilfe von PowerShell


Gehen Sie wie folgt vor, um die App-V 5,1 für die Berichterstellung zu konfigurieren.

**So konfigurieren Sie den Computer mit dem App-V 5,1-Client für Berichte**

1. Installieren Sie den App-V 5,1-Client. Weitere Informationen zum Installieren des Clients finden Sie unter [Bereitstellen des App-V-Clients](how-to-deploy-the-app-v-client-51gb18030.md).

2. Nachdem Sie den App-V 5,1-Client installiert haben, verwenden Sie die PowerShell " **AppvClientConfiguration** ", um die entsprechenden Konfigurationseinstellungen für Berichte zu konfigurieren:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Einstellung</th>
   <th align="left">Beschreibung</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>ReportingEnabled</p></td>
   <td align="left"><p>Ermöglicht es dem Client, Informationen an einen Berichtsserver zurückzugeben. Diese Einstellung ist erforderlich, damit der Client die Berichtsdaten auf dem Client sammelt.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReportingServerURL</p></td>
   <td align="left"><p>Gibt den Speicherort auf dem Berichtsserver an, auf dem Clientinformationen gespeichert werden. Beispiel &lt; : http://reportingservername &gt; : &lt; reportingportnumber &gt; .</p>
   <div class="alert">
   <strong>Hinweis:</strong><br/><p>Hierbei handelt es sich um die Portnummer, die während des Berichts Server-Setups zugewiesen wurde.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Anfangszeit für Berichte</p></td>
   <td align="left"><p>Dies ist so eingestellt, dass der Client automatisch die Daten an den Server sendet. Diese Einstellung zeigt die Stunde an, zu der die Berichtsdaten gesendet werden. Es ist im 24-Stunden-Format und nimmt eine Zahl zwischen 0-23.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReportingRandomDelay</p></td>
   <td align="left"><p>Gibt die maximale Verzögerung (in Minuten) für Daten an, die an den Berichtsserver gesendet werden sollen. Wenn der geplante Task gestartet wird, generiert der Client eine zufällige Verzögerung zwischen 0 und ReportingRandomDelay und wartet die angegebene Dauer vor dem Senden von Daten.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ReportingInterval</p></td>
   <td align="left"><p>Gibt das Wiederholungsintervall an, das vom Client zum erneuten Senden von Daten an den Berichtsserver verwendet wird.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReportingDataCacheLimit</p></td>
   <td align="left"><p>Gibt die maximale Größe in Megabyte (MB) des XML-Caches zum Speichern von Berichtsinformationen an. Die Größe bezieht sich auf den Cache im Arbeitsspeicher. Wenn das Limit erreicht ist, wird die Protokolldatei überschrieben.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ReportingDataBlockSize</p></td>
   <td align="left"><p>Gibt die maximale Größe in Megabyte (MB) des XML-Caches zum Speichern von Berichtsinformationen an. Die Größe bezieht sich auf den Cache im Arbeitsspeicher. Wenn das Limit erreicht ist, wird die Protokolldatei überschrieben.</p></td>
   </tr>
   </tbody>
   </table>



3. Nachdem die entsprechenden Einstellungen konfiguriert wurden, sammelt der Computer, auf dem der App-V 5,1-Client ausgeführt wird, automatisch Daten, und die Daten werden an den Berichtsserver zurückgesendet.

   Darüber hinaus können Administratoren die Daten mithilfe des PowerShell-Cmdlets " **Send-AppvClientReport** " manuell zurücksenden.

   Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Verwalten von App-V 5.1 mithilfe von PowerShell](administering-app-v-51-by-using-powershell.md)









