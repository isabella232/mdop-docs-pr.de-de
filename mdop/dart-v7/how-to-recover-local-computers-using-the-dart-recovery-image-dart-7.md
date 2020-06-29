---
title: So stellen Sie lokale Computer mithilfe des DaRT-Wiederherstellungsabbilds wieder her
description: So stellen Sie lokale Computer mithilfe des DaRT-Wiederherstellungsabbilds wieder her
author: dansimp
ms.assetid: be29b5a8-be08-4cf2-822e-77a51d3f3b65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c605db895b5ea812d90db51d3c2de9653e2dd2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810150"
---
# So stellen Sie lokale Computer mithilfe des DaRT-Wiederherstellungsabbilds wieder her


Wenn Sie einen lokalen Computer mithilfe von Microsoft Diagnostics and Recovery Toolset (Dart) 7 wiederherstellen möchten, müssen Sie physisch auf dem Computer des Endbenutzers anwesend sein, bei dem Probleme auftreten, bei denen Dart erforderlich ist. Sie können Dart auch remote ausführen, indem Sie die Anweisungen zum [Wiederherstellen von Remotecomputern mithilfe des DART-Wiederherstellungs Bilds](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md)befolgen.

**So stellen Sie einen lokalen Computer mithilfe von DART wieder her**

1.  Wenn der Computer in das DART-Wiederherstellungsabbild gestartet wird, wird das Dialogfeld " **netstart** " angezeigt. Sie werden gefragt, ob Sie Netzwerkdienste initialisieren möchten. Wenn Sie auf **Ja**klicken, wird davon ausgegangen, dass ein DHCP-Server im Netzwerk vorhanden ist, und es wird versucht, eine IP-Adresse vom Server abzurufen. Wenn das Netzwerk statische IP-Adressen statt DHCP verwendet, können Sie später das **TCP/IP-Konfigurations** Tool in DART verwenden, um eine statische IP-Adresse anzugeben.

    Wenn Sie den Netzwerk Initialisierungsprozess überspringen möchten, klicken Sie auf **Nein**.

2.  Nachdem Sie das Dialogfeld Netzwerk Initialisierung aufgerufen haben, werden Sie gefragt, ob Sie die Laufwerkbuchstaben neu zuordnen möchten. Wenn Sie Windows Online ausführen, wird das System Volume in der Regel Laufwerk C zugeordnet. Wenn Sie jedoch Windows offline unter WinRE ausführen, wird das ursprüngliche System Volume möglicherweise einem anderen Laufwerk zugeordnet, was zu Verwirrung führen kann. Wenn Sie sich für die Neuzuordnung entscheiden, versucht Dart, die Offline Laufwerkbuchstaben den Online Laufwerkbuchstaben zuzuordnen. Eine Neuzuordnung wird nur ausgeführt, wenn ein Offline Betriebssystem später im Startvorgang ausgewählt wird.

3.  Nach dem Dialogfeld erneute Zuordnung wird ein Dialogfeld **System Wiederherstellungsoptionen** angezeigt, in dem Sie aufgefordert werden, ein Tastaturlayout auszuwählen. Anschließend werden das Systemstammverzeichnis, die Art des installierten Betriebssystems und die Partitionsgröße angezeigt. Wenn Ihr Betriebssystem nicht aufgeführt ist und Sie vermuten, dass das Fehlen von Treibern eine mögliche Ursache für den Fehler ist, klicken Sie auf **Treiber laden** , um die Verdächtigen Treiber zu laden. Sie werden aufgefordert, das Installationsmedium für das Gerät einzufügen und den Treiber auszuwählen. Wählen Sie die Installation aus, die Sie reparieren oder diagnostizieren möchten, und klicken Sie dann auf **weiter**.

    **Hinweis:**  
    Wenn die Windows-Wiederherstellungsumgebung (WinRE) erkennt oder vermutet, dass Windows 7 beim letzten Versuch nicht ordnungsgemäß gestartet wurde, wird die **Startreparatur** möglicherweise automatisch gestartet.



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

4. Klicken Sie im Fenster **System Wiederherstellungsoptionen** auf **Microsoft-Diagnose-und Wiederherstellungs-Toolset**.

   Das Fenster " **Diagnose-und Wiederherstellungs-Toolset** " wird geöffnet. Sie können nun alle einzelnen Tools oder Assistenten ausführen, die beim Erstellen des DART-Wiederherstellungs Bilds enthalten waren.

Sie können im Fenster **Diagnose-und Wiederherstellungs-Toolset** auf **Hilfe** klicken, um die Clienthilfedatei zu öffnen, die detaillierte Anweisungen und Informationen zum Ausführen der einzelnen Dart-Tools enthält. Sie können auch im Fenster **Diagnose-und Wiederherstellungs-Toolset** auf den **Lösungs-Assistenten** klicken, um das optimale Tool für die Situation zu wählen, das auf einem kurzen, vom Assistenten bereitgestellten Interview basiert.

Allgemeine Informationen zu den Dart-Tools finden Sie unter [Übersicht über die Tools in DART 7,0](overview-of-the-tools-in-dart-70-new-ia.md).

**So führen Sie Dart an der Eingabeaufforderung aus**

1. Sie können Dart an der Eingabeaufforderung ausführen, indem Sie den Befehl **netstart.exe** angeben und einen der folgenden Parameter verwenden:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Parameter</th>
   <th align="left">Beschreibung</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>-Netzwerk</p></td>
   <td align="left"><p>Initialisiert die Netzwerkdienste.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>-Erneutes Einhängen</p></td>
   <td align="left"><p>Ordnet die Laufwerkbuchstaben erneut zu.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>-Aufforderung</p></td>
   <td align="left"><p>Zeigt Nachrichten an, in denen der Endbenutzer angeben soll, ob das Netzwerk initialisiert und die Laufwerke neu zugewiesen werden sollen.</p>
   <div class="alert">
   <strong>Wichtig</strong><br/><p>Die Antwort des Endbenutzers auf die Eingabeaufforderungen überschreibt die Switches-Netzwerk und-erneute Bereitstellung.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. Sie können Dart so anpassen, dass ein Computer, der in DART bootet, automatisch das **Remote Verbindungs** Tool öffnet, das zum Einrichten einer Remoteverbindung mit dem Helpdesk verwendet wird.

## Verwandte Themen


[Wiederherstellen von Computern mithilfe von DaRT 7.0](recovering-computers-using-dart-70-dart-7.md)









