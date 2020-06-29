---
title: So stellen Sie lokale Computer mit dem DaRT-Wiederherstellungsabbild wieder her
description: So stellen Sie lokale Computer mit dem DaRT-Wiederherstellungsabbild wieder her
author: dansimp
ms.assetid: f679d522-49ab-429c-93d0-294c3f3e5639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1b5faa0eb9ac24b33c66f1d5262a050b92e11e52
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810477"
---
# So stellen Sie lokale Computer mit dem DaRT-Wiederherstellungsabbild wieder her


Verwenden Sie diese Anweisungen zum Wiederherstellen eines Computers, wenn Sie physisch am Endbenutzercomputer anwesend sind, bei dem Probleme auftreten.

**Wiederherstellen eines lokalen Computers mithilfe des DART-Wiederherstellungs Bilds**

1.  Starten Sie den Endbenutzercomputer mithilfe des Microsoft Diagnostics and Recovery Toolset (Dart) 8,0-Wiederherstellungsabbilds.

    Wenn der Computer in das Dart 8,0-Wiederherstellungsabbild gestartet wird, wird das Dialogfeld " **netstart** " angezeigt.

2.  Wenn Sie gefragt werden, ob Sie Netzwerkdienste initialisieren möchten, wählen Sie eine der folgenden Optionen aus:

    **Ja** – es wird davon ausgegangen, dass ein DHCP-Server im Netzwerk vorhanden ist, und es wird versucht, eine IP-Adresse vom Server abzurufen. Wenn das Netzwerk statische IP-Adressen statt DHCP verwendet, können Sie später das **TCP/IP-Konfigurations** Tool in DART verwenden, um eine statische IP-Adresse anzugeben.

    **Nein** – überspringen Sie den Netzwerk Initialisierungsprozess.

3.  Geben Sie an, ob Sie die Laufwerkbuchstaben neu zuordnen möchten. Wenn Sie Windows Online ausführen, wird das System Volume in der Regel Laufwerk C zugeordnet. Wenn Sie jedoch Windows offline unter WinRE ausführen, wird das ursprüngliche System Volume möglicherweise einem anderen Laufwerk zugeordnet, was zu Verwirrung führen kann. Wenn Sie sich für die Neuzuordnung entscheiden, versucht Dart, die Offline Laufwerkbuchstaben den Online Laufwerkbuchstaben zuzuordnen. Eine Neuzuordnung wird nur ausgeführt, wenn ein Offline Betriebssystem später im Startvorgang ausgewählt wird.

4.  Wählen Sie im Dialogfeld **System Wiederherstellungsoptionen** ein Tastaturlayout aus.

5.  Überprüfen Sie das angezeigte Systemstammverzeichnis, die Art des installierten Betriebssystems und die Partitionsgröße. Wenn Ihr Betriebssystem nicht aufgeführt ist und Sie vermuten, dass das Fehlen von Treibern eine mögliche Ursache für den Fehler ist, klicken Sie auf **Treiber laden** , um die Verdächtigen Treiber zu laden, und legen Sie dann das Installationsmedium für das Gerät ein, und wählen Sie den Treiber aus.

6.  Wählen Sie die Installation aus, die Sie reparieren oder diagnostizieren möchten, und klicken Sie dann auf **weiter**.

    **Hinweis:**  
    Wenn die Windows-Wiederherstellungsumgebung (WinRE) erkennt oder vermutet, dass Windows 8 beim letzten Versuch nicht ordnungsgemäß gestartet wurde, wird die **Startreparatur** möglicherweise automatisch gestartet.



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. Klicken Sie im Fenster **System Wiederherstellungsoptionen** auf **Microsoft-Diagnose-und Wiederherstellungs-Toolset**.

   Das Fenster " **Diagnose-und Wiederherstellungs-Toolset** " wird geöffnet. Sie können nun alle einzelnen Tools oder Assistenten ausführen, die beim Erstellen des DART-Wiederherstellungs Bilds enthalten waren.

Sie können im Fenster **Diagnose-und Wiederherstellungs-Toolset** auf **Hilfe** klicken, um die Clienthilfedatei zu öffnen, die detaillierte Anweisungen und Informationen zum Ausführen der einzelnen Dart-Tools enthält. Sie können auch im Fenster **Diagnose-und Wiederherstellungs-Toolset** auf den **Lösungs-Assistenten** klicken, um das optimale Tool für die Situation zu wählen, das auf einem kurzen, vom Assistenten bereitgestellten Interview basiert.

Allgemeine Informationen zu den Dart-Tools finden Sie unter [Übersicht über die Tools in Dart 8,0](overview-of-the-tools-in-dart-80-dart-8.md).

**Ausführen von DART an der Eingabeaufforderung**

- Wenn Sie Dart an der Eingabeaufforderung ausführen möchten, geben Sie den Befehl **netstart.exe** an, und verwenden Sie dann einen der folgenden Parameter:

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <tbody>
  <tr class="odd">
  <td align="left"><p><strong>Parameter</strong></p></td>
  <td align="left"><p><strong>Beschreibung</strong></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>-Netzwerk</p></td>
  <td align="left"><p>Initialisiert die Netzwerkdienste.</p></td>
  </tr>
  <tr class="odd">
  <td align="left"><p>-Erneutes Einhängen</p></td>
  <td align="left"><p>Ordnet die Laufwerkbuchstaben erneut zu.</p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>-Aufforderung</p></td>
  <td align="left"><p>Zeigt Nachrichten an, die den Endbenutzer bitten, anzugeben, ob das Netzwerk initialisiert und die Laufwerke neu zugewiesen werden sollen.</p>
  <div class="alert">
  <strong>Warnung</strong><br/><p>Die Antwort des Endbenutzers auf die Eingabeaufforderung überschreibt die Switches – Netzwerk und – erneute Bereitstellung.</p>
  </div>
  <div>

  </div></td>
  </tr>
  </tbody>
  </table>



## Verwandte Themen


[Vorgänge für DaRT 8.0](operations-for-dart-80-dart-8.md)

[Wiederherstellen von Computern mithilfe von DaRT 8.0](recovering-computers-using-dart-80-dart-8.md)









