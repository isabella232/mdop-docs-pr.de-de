---
title: So konfigurieren Sie das App-V System für das Paketupgrade
description: So konfigurieren Sie das App-V System für das Paketupgrade
author: dansimp
ms.assetid: de133898-f887-46c1-9bc9-fbb03feac66a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5e5056f923c61aff39d9bd6e1d26f071177f7c12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807271"
---
# So konfigurieren Sie das App-V System für das Paketupgrade


Wenn Sie eine neue Version eines vorhandenen Anwendungspakets bereitstellen, das im App-v-Sequencer aktualisiert wurde, können Sie es bereitstellen, damit die APP-v-Clients die neue Version automatisch in den lokalen Cache streamen. Je nach verwendeter Streaming-Lösung gibt es verschiedene Verfahren zum Konfigurieren des Paket Upgrades. In den folgenden Abschnitten werden die am häufigsten auftretenden Szenarien für die Veröffentlichung und das Streaming beschrieben, und es werden die erforderlichen Verfahren für die Konfiguration des Paket Upgrades für jedes Szenario aufgeführt.

## Verwenden eines Verwaltungsservers für Veröffentlichung und Streaming


In diesem Szenario wird ein einzelner App-V-Verwaltungs Server für die Veröffentlichung und das Streaming von Paketen und Anwendungen verwendet, und das RTSP (S)-Protokoll ist erforderlich. Wenn das ursprüngliche Paket in den App-V-Verwaltungs Server importiert wird, kopiert der Administrator den Paketordner, der die vom Sequencer erstellten Dateien enthält, in den Inhaltsordner, beispielsweise in \\\\server\\CONTENT\\packagename. Der Administrator bearbeitet auch den Eintrag href in der OSD-Datei so, dass er auf die SFT-Datei im Paketordner verweist, und importiert dann das Paket auf den Server.

Wenn ein Benutzer vom Verwaltungsserver authentifiziert wird, veröffentlicht der Server die Anwendungen des Benutzers, indem die applist.xml Datei an den Client gesendet wird. Der Client ruft dann die OSD-Dateien und-Symbole für die Anwendungen vom Verwaltungs Server ab. Wenn der Benutzer auf ein Anwendungssymbol doppelklickt, wird der Anwendungsinhalt aus dem in der OSD-Datei angegebenen Pfad an den Clientcache gestreamt, und die Anwendung wird gestartet.

### So aktualisieren Sie das Paket

Um eine neue Version einer Anwendung hinzuzufügen, die im App-V-Sequencer aktualisiert wurde, muss der Administrator die neue SFT-Datei und alle anderen geänderten Dateien in denselben Ordner wie die ursprüngliche Version der Anwendung kopieren. Der Administrator verwendet dann in der Serververwaltungskonsole die **Add-Version** , um die neue Version des Pakets hinzuzufügen.

Wenn der Benutzer die Anwendung als nächstes startet, strömt der Server die neue Version automatisch an den Client aus. Diese spezifische Methode zum Aktualisieren eines Pakets war früher als aktives Upgrade bekannt.

## Verwenden eines Verwaltungsservers für die Veröffentlichung und eines Streaming Servers für Streaming


In diesem Szenario wird der App-V-Verwaltungs Server für die Veröffentlichung der Pakete verwendet, und der Streamingserver wird für Streaming-Pakete und-Anwendungen verwendet. Das RTSP (S)-Protokoll ist erforderlich. Wenn das ursprüngliche Paket auf den Verwaltungs Server importiert wird, kopiert der Administrator den Paketordner, der die vom Sequencer erstellten Dateien enthält, in den Inhaltsordner, beispielsweise in \\\\server\\CONTENT\\packagename. Der Administrator bearbeitet den Eintrag href in der OSD-Datei so, dass er auf die SFT-Datei auf dem Streamingserver verweist, und importiert dann das Paket auf den Verwaltungs Server.

Zum Einrichten des Streamingserver kopiert der Administrator den Paketordner aus dem Verwaltungs Server in den Inhaltsordner auf dem Streamingserver. Dieser Ordner muss denselben Namen und relativen Pfad unter dem Inhaltsordner des Streaming Servers wie auf dem Verwaltungs Server aufweisen, beispielsweise \\\\streamingserver\\CONTENT\\packagename.

Wenn die Einstellung des Client-Anwendungs Quell Stamms (ASR) so konfiguriert ist, dass er auf den Streamingserver verweist, verwendet der Client diese Einstellung anstelle des Server namens im href-Eintrag in der OSD-Datei. Die Felder ISR und ASR auf dem Client können optional so konfiguriert werden, dass Sie je nach verwendeter Systemarchitektur entweder auf den Verwaltungsserver oder den Streamingserver verweisen.

Wenn ein Benutzer vom Verwaltungsserver authentifiziert wird, veröffentlicht der Server die Anwendungen des Benutzers, indem die applist.xml Datei an den Client gesendet wird. Je nach den Einstellungen in den Feldern ASR und ISR ruft der Client die OSD-Dateien und-Symbole für die Anwendungen entweder vom Streamingserver oder vom Verwaltungsserver ab.

Wenn der Benutzer auf ein Anwendungssymbol doppelklickt, verwendet der Client den Pfad zur Paketinhalts Datei (SFT), die im OSD-Datei href-Element enthalten ist. Bei Verwendung der ASR ersetzt der Client den Servernamen (und Port und Protokoll, falls verwendet) im href-Element durch den Pfad zu dem in der ASR-Datei angegebenen Streamingserver. Die Anwendung wird dann vom Streaming Server an den Clientcache gestreamt und gestartet.

### So aktualisieren Sie das Paket

Um eine neue Version einer Anwendung hinzuzufügen, die im App-V-Sequencer aktualisiert wurde, muss der Administrator die neue Version der SFT-Datei und alle anderen geänderten Dateien in denselben Ordner wie die ursprüngliche Version der Anwendung auf dem Streamingserver kopieren.

Aus Gründen der Konsistenz empfehlen wir, dass Sie auch neue Dateien in den Ordner auf dem Verwaltungs Server kopieren. Insbesondere wenn Sie die Felder ASR oder ISR des Clients verwenden, kopieren Sie die aktualisierte OSD-Datei und die aktualisierten Symbole auf den Server, der in den Feldern ASR und ISR angegeben ist.

Nachdem der Streamingserver die neue Version erkannt hat, strömt der Server die neue Version beim nächsten Start der Anwendung automatisch an den Client.

## Verwenden eines Verwaltungsservers für die Veröffentlichung und eines IIS-Servers für Streaming


In diesem Szenario wird der App-V-Verwaltungs Server für die Veröffentlichung der Pakete verwendet, und der IIS-Server wird für Streaming-Pakete und-Anwendungen verwendet. Wenn das ursprüngliche Paket auf den Verwaltungs Server importiert wird, kopiert der Administrator den Paketordner, der die vom Sequencer erstellten Dateien enthält, in den Inhaltsordner, beispielsweise in \\\\server\\CONTENT\\packagename. Der Administrator bearbeitet den Eintrag href in der OSD-Datei, sodass er auf die SFT-Datei auf dem IIS-Server verweist, und importiert dann das Paket auf den Verwaltungsserver.

Zum Einrichten des IIS-Servers für Streaming kopiert der Administrator den Paketordner aus dem Verwaltungsserver in den Inhaltsordner auf dem IIS-Server. Dieser Ordner muss denselben Namen und relativen Pfad unter dem Webinhalts Ordner des IIS-Servers wie auf dem Verwaltungsserver aufweisen. Beispielsweise kann auf die URL auf dem IIS-Server mithilfe von oder zugegriffen werden http://IISserver/CONTENT/packagename https://IISserver/CONTENT/packagename .

Wenn die Einstellung für den Anwendungs Quellstamm (ASR) des Clients so konfiguriert ist, dass Sie auf den IIS-Server verweist, verwendet der Client die ASR anstelle des Server namens im href-Eintrag in der OSD-Datei. Sie können die Felder ISR und ASR auf dem Client optional so konfigurieren, dass Sie je nach verwendeter Systemarchitektur entweder auf den Verwaltungsserver oder den IIS-Server verweisen.

Wenn der Verwaltungsserver den Benutzer authentifiziert, veröffentlicht der Server die Anwendungen des Benutzers, indem die applist.xml Datei an den Client gesendet wird. Je nach den Einstellungen in den Feldern ISR und ASR ruft der Client die OSD-Dateien und-Symbole für die Anwendungen vom IIS-Server oder vom Verwaltungsserver ab.

Wenn der Benutzer auf ein Anwendungssymbol doppelklickt, verwendet der Client den Pfad zur Paketinhalts Datei (SFT), die im OSD-Datei href-Element enthalten ist. Bei Verwendung der ASR ersetzt der Client den Servernamen (und Port und Protokoll, falls verwendet) im href-Element mit dem Pfad zu dem IIS-Server, der in der ASR-Datei angegeben ist. Die Anwendung wird dann mithilfe des HTTP (S)-Protokolls vom IIS-Server an den Clientcache gestreamt und gestartet.

### So aktualisieren Sie das Paket

Die Vorgehensweise zum Upgrade des Pakets lautet wie folgt:

-   Kopieren Sie die neue Version der OSD-Datei in den Ordner der ursprünglichen Version unter dem Inhaltsordner des Verwaltungsservers, beispielsweise \\\\server\\CONTENT\\packagename, und ersetzen Sie die vorhandene OSD-Datei. Kopieren Sie aus Gründen der Konsistenz auch alle anderen geänderten Dateien. Wenn die ASR-oder ISR-Felder des Clients verwendet werden, kopieren Sie auch die aktualisierte OSD-Datei und die aktualisierten Symbole auf den Server, der in den Feldern ASR und ISR angegeben ist.

-   Kopieren Sie die neue Version der SFT-Datei in den Ordner "Paket" unter dem Ordner "Webinhalt" auf dem IIS-Server. Beispielsweise kann auf die URL auf dem IIS-Server mithilfe von oder zugegriffen werden http://IISserver/CONTENT/packagename https://IISserver/CONTENT/packagename .

Bei der nächsten Veröffentlichungsaktualisierung wird der Client mit der neuen Version der OSD-Datei aktualisiert. Diese Datei verweist nun auf die neue Version der SFT-Datei. Wenn der Benutzer dann auf ein Anwendungssymbol doppelklickt, wird daher die neue Version gestartet.

## Verwenden eines Verwaltungsservers für die Veröffentlichung und eine Dateifreigabe für Streaming


In diesem Szenario wird der App-V-Verwaltungs Server für die Veröffentlichung der Pakete verwendet, und der Datei Server wird für Streaming-Pakete und-Anwendungen verwendet. Wenn das ursprüngliche Paket auf den Verwaltungs Server importiert wird, kopiert der Administrator den Paketordner, der die vom Sequencer erstellten Dateien enthält, in den Inhaltsordner, beispielsweise in \\\\server\\CONTENT\\packagename. Der Administrator bearbeitet den href-Eintrag in der OSD-Datei so, dass er auf die SFT-Datei auf dem Dateiserver verweist, und importiert das Paket auf den Verwaltungsserver.

Um den Dateiserver für Streaming einzurichten, kopiert der Administrator den Paketordner aus dem Verwaltungsserver in den Inhaltsordner auf dem Dateiserver. Dieser Ordner muss denselben Namen und relativen Pfad unter dem Inhaltsordner des Dateiservers wie auf dem Verwaltungsserver aufweisen, beispielsweise \\\\fileserver\\CONTENT\\packagename.

Wenn die Einstellung für die Anwendung Source Root (ASR) des Clients so konfiguriert ist, dass Sie mithilfe eines UNC-Pfads, beispielsweise \\\\fileserver\\content, auf den Dateiserver verweist, verwendet der Client diese Einstellung anstelle des Server namens im href-Eintrag in der OSD-Datei. Der Administrator kann die Felder ISR und ASR auf dem Client optional so konfigurieren, dass Sie je nach verwendeter Systemarchitektur entweder auf den Verwaltungs Server oder den Datei Server verweisen.

Wenn der Verwaltungsserver den Benutzer authentifiziert, veröffentlicht der Server die Anwendungen des Benutzers, indem die applist.xml Datei an den Client gesendet wird. Der Client ruft die OSD-Dateien und-Symbole für die Anwendungen entweder vom Dateiserver oder vom Verwaltungsserver ab, abhängig von den Einstellungen in den Feldern ISR und ASR.

Wenn der Benutzer auf ein Anwendungssymbol doppelklickt, verwendet der Client den Pfad zur Paketinhalts Datei (SFT), die im OSD-Datei href-Element enthalten ist. Wenn die ASR verwendet wird, ersetzt der Client den Servernamen (und Port und Protokoll, falls verwendet) im href-Element mit dem Pfad zu dem Dateiserver, der in der ASR-Datei angegeben ist. Die Anwendung wird dann vom Dateiserver in den Clientcache gestreamt und gestartet.

### So aktualisieren Sie das Paket

Die Vorgehensweise zum Upgrade des Pakets lautet wie folgt:

-   Kopieren Sie die neue Version der OSD-Datei in den Ordner der ursprünglichen Version unter dem Inhaltsordner des Verwaltungsservers, beispielsweise \\\\server\\CONTENT\\packagename, und ersetzen Sie die vorhandene OSD-Datei. Alle anderen geänderten Dateien sollten ebenfalls aus Konsistenzgründen kopiert werden. Wenn die ASR-oder ISR-Felder des Clients verwendet werden, kopieren Sie auch die aktualisierte OSD-Datei und die aktualisierten Symbole auf den Server, der in den Feldern ASR und ISR angegeben ist.

-   Kopieren Sie die neue Version der SFT-Datei in den Paketordner unter dem Inhaltsordner auf dem Dateiserver, beispielsweise \\\\fileserver\\CONTENT\\packagename. Kopieren Sie die V2 SFT-Datei in den Ordner unter der Inhaltsfreigabe auf dem Dateiserver, beispielsweise \\\\fileserver\\CONTENT\\packagename\\V1.

Bei der nächsten Veröffentlichungsaktualisierung wird der Client mit der neuen Version der OSD-Datei aktualisiert. Diese Datei verweist nun auf die neue Version der SFT-Datei, sodass die neue Version gestartet wird, wenn der Benutzer als nächstes auf ein Anwendungssymbol doppelklickt.

## Aktualisieren des Pakets mit dem MSI-Streamingmodus


Wenn Sie während der Sequenzierung eines Pakets eine Windows Installer-Datei (MSI) generieren, erstellt der Sequencer eine. MSI-Datei, die alle erforderlichen Veröffentlichungsinformationen enthält. Der Administrator muss das Kopieren. MSI-Datei an den Client und die. SFT-Datei mit dem Paketinhalt einer Netzwerkfreigabe, auf die der Clientcomputer zugreifen kann.

Führen Sie den folgenden Befehl auf dem Clientcomputer aus, um die Anwendung auf dem Client zu veröffentlichen:

   **Msiexec.exe/i \\\\PathToMsi\\packagename.msi Mode = Streaming OVERRIDEURL = \\\\\\\\server\\share\\package.SFT**

Die. MSI-Datei veröffentlicht die Anwendungen auf dem Client und streamt dann die. SFT-Datei im Clientcache.

### So aktualisieren Sie das Paket

Um eine neue Version hinzuzufügen, muss ein Administrator eine neue Version bereitstellen. MSI-Datei für den Client und eine neue. SFT-Datei auf die Netzwerkfreigabe. Der Administrator muss dann denselben Befehl ausführen, der zum Bereitstellen des Pakets verwendet wird, aber die neue verwenden. MSI-Datei und die neue. SFT-Datei, beispielsweise:

   **Msiexec.exe/i \\\\PathToMsi\\packagename\_2.msi Mode = Streaming OVERRIDEURL = \\\\\\\\server\\share\\package\_2.SFT**

 

 





