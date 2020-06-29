---
title: So stellen Sie sicher, dass Crash Analyzer auf Symboldateien zugreifen kann
description: So stellen Sie sicher, dass Crash Analyzer auf Symboldateien zugreifen kann
author: dansimp
ms.assetid: 150a2f88-68a5-40eb-8471-e5008488ab6e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: db56bb21ad885d1e3aa73bcbd922a7e8bde77080
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809574"
---
# So stellen Sie sicher, dass Crash Analyzer auf Symboldateien zugreifen kann


In der Regel werden Debuginformationen in einer Symboldatei gespeichert, die von der ausführbaren Datei getrennt ist. Sie müssen Zugriff auf die Symbol Informationen haben, wenn Sie eine Anwendung debuggen, die nicht mehr reagiert, beispielsweise wenn Sie abgestürzt ist.

Symbol Dateien werden beim Ausführen des Microsoft Diagnostics and Recovery Toolset (Dart) 7 Crash Analyzer automatisch heruntergeladen. Wenn der Computer nicht über eine Internet Verbindung verfügt oder das Netzwerk den Computer für den Zugriff auf einen HTTP-Proxy Server benötigt, können die Symboldateien nicht heruntergeladen werden.

## Sicherstellen des Zugriffs auf Symboldateien


In der Regel werden Debuginformationen in einer Symboldatei gespeichert, die von der ausführbaren Datei getrennt ist. Sie müssen Zugriff auf die Symbol Informationen haben, wenn Sie eine Anwendung debuggen, die nicht mehr reagiert, beispielsweise wenn Sie abgestürzt ist.

Symbol Dateien werden beim Ausführen von **Crash Analyzer**automatisch heruntergeladen. Wenn der Computer nicht über eine Internet Verbindung verfügt oder das Netzwerk den Computer für den Zugriff auf einen HTTP-Proxy Server benötigt, können die Symboldateien nicht heruntergeladen werden.

Im folgenden finden Sie eine Liste der Optionen, die verfügbar sind, um den Zugriff auf Symboldateien zu gewährleisten:

-   **Kopieren Sie die Speicherabbilddatei auf einen anderen Computer.** Wenn die Symbole wegen fehlender Internetverbindung nicht heruntergeladen werden können, kopieren Sie die Absturz Speicherdatei auf einen Computer, auf dem eine Internetverbindung besteht, und führen Sie den eigenständigen **Absturzanalyse-Assistenten** auf diesem Computer aus.

-   **Greifen Sie auf die Symboldateien von einem anderen Computer zu.** Wenn die Symbole nicht heruntergeladen werden können, weil keine Internetverbindung besteht, können Sie die Symbole von einem Computer herunterladen, der über eine Internetverbindung verfügt, und Sie dann auf den Computer kopieren, auf dem keine Internetverbindung besteht, oder Sie können ein Netzlaufwerk an einem Speicherort zuordnen, an dem die Symbole im lokalen Netzwerk verfügbar sind. Wenn Sie den **Crash Analyzer** in einer Windows-Wiederherstellungsumgebung (WindowsRE) ausführen, können Sie die Symboldateien in das DART-Wiederherstellungsabbild aufnehmen. Weitere Informationen zum Erstellen eines Wiederherstellungsabbilds finden Sie unter [Erstellen des DART 7,0-Wiederherstellungs](creating-the-dart-70-recovery-image-dart-7.md)Abbilds.

-   **Zugriff auf Symboldateien über einen HTTP-Proxy Server.** Wenn die Symbole nicht heruntergeladen werden können, weil auf einen HTTP-Proxy Server zugegriffen werden muss, führen Sie die folgenden Schritte aus, um auf einen HTTP-Proxy Server zuzugreifen. In DaRT7 hat der **Absturzanalyse-Assistent** eine Einstellung auf der Dialogseite **Symbol Dateien angeben** , die mit dem Label- **Proxy Server gekennzeichnet ist (optional mit dem Format "Server: Port")**. Sie können in diesem Textfeld einen Proxy Server angeben. Geben Sie die Proxyadresse in das Format ** &lt; Hostname &gt; : &lt; Port &gt; **ein, wobei der &lt; **Hostname** &gt; ein DNS-Name oder eine IP-Adresse und der &lt; **Port** &gt; eine TCP-Portnummer ist, in der Regel 80. Es gibt zwei Modi, in denen der **Absturzanalyse-Analyzer** ausgeführt werden kann. Im folgenden wird beschrieben, wie Sie die Proxyeinstellung in jedem dieser Modi verwenden:

    -   **Online Modus:** Wenn in diesem Modus das Feld Proxy Server leer bleibt, verwendet der Assistent in der Systemsteuerung die Proxyeinstellungen in den Internet Optionen. Wenn Sie eine Proxyadresse in das bereitgestellte Textfeld eingeben, wird diese Adresse verwendet, und die Einstellung in den Internet Optionen wird außer Kraft gesetzt.

    -   **Windows-Wiederherstellungsumgebung (WindowsRE):** Wenn Sie **Crash Analyzer** im Fenster **Diagnose-und Wiederherstellungs-Toolset** ausführen, gibt es keine Standardproxy Adresse. Wenn der Computer direkt mit dem Internet verbunden ist, ist keine Proxyadresse erforderlich. Daher können Sie dieses Feld in der Assistenten Einstellung leer lassen. Wenn der Computer nicht direkt mit dem Internet verbunden ist und sich in einer Netzwerkumgebung mit einem Proxy Server befindet, müssen Sie das Feld Proxy im Assistenten für den Zugriff auf den Symbolspeicher fest legen. Die Proxyadresse kann vom Netzwerkadministrator abgerufen werden. Das Festlegen des Proxyservers ist nur dann wichtig, wenn der öffentliche Symbolspeicher mit dem Internet verbunden ist. Wenn sich die Symbole bereits im Dart-Wiederherstellungsabbild befinden oder wenn Sie lokal verfügbar sind, ist das Festlegen des Proxyservers nicht erforderlich.

## Verwandte Themen


[Diagnostizieren von Systemfehlern mit Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





