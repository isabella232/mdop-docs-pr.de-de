---
title: Erstellen eines Windows Virtual PC-Images für MED-V
description: Erstellen eines Windows Virtual PC-Images für MED-V
author: dansimp
ms.assetid: fd7c0b1a-0769-4e7b-ad1a-dad19cca081f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f947479776e84a4c54edb10d583dd21d7ccf6f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804412"
---
# Erstellen eines Windows Virtual PC-Images für MED-V


Bevor Sie einen Med-v-Arbeitsbereich für Benutzer bereitstellen können, müssen Sie zuerst eine virtuelle Festplatte vorbereiten, die Sie zum Erstellen des Med-v Workspace-Installationspakets für Microsoft Enterprise Desktop Virtualization (Med-v) 2,0 verwenden. Um die erforderliche virtuelle Festplatte vorzubereiten, müssen Sie ein Windows Virtual PC-Abbild erstellen, das das erforderliche Betriebssystem, Updates und Software enthält, damit Sie später Anwendungen und URL-Umleitungsinformationen für Benutzer bereitstellen können. Dieser Abschnitt enthält Anleitungen zum Erstellen der virtuellen Festplatte.

Zum Erstellen eines virtuellen Bilds für MED-V müssen Sie die folgenden Schritte ausführen.

1.  [Erstellen eines Windows Virtual PC-Bilds](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc)

2.  [Installieren von Windows XP auf dem Bild](#bkmk-installingwindowsxpontovpc)

3.  [Installieren von .NET Framework auf dem Bild](#bkmk-installingnet)

4.  [Anwenden von Updates auf das Bild](#bkmk-applypatchestovpc)

5.  [Installieren von Integrationskomponenten](#bkmk-installintegration)

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a>Erstellen eines Windows Virtual PC-Bilds


Informationen zum Erstellen eines Windows Virtual PC-Bilds finden Sie in der Windows Virtual PC-Dokumentation:

-   [Startseite für Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=148103) ( https://go.microsoft.com/fwlink/?LinkId=148103) .

-   [Hilfe zu Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .

Wenn Sie bereits über eine Windows Imaging-Datei (WIM) verfügen, die Sie als Grundlage für Ihr virtuelles Bild verwenden möchten, können Sie Sie alternativ in eine VHD konvertieren, die Sie zum Erstellen des MED-V-Arbeitsbereichs verwenden. Weitere Informationen zum Konvertieren einer WIM auf eine virtuelle Festplatte finden Sie unter [Unterstützung für Native VHD in Windows 7](https://go.microsoft.com/fwlink/?LinkId=195922) ( https://go.microsoft.com/fwlink/?LinkId=195922) .

**Wichtig**  MED-V unterstützt nur eine virtuelle Festplatte pro virtuellen Computer und nur eine Partition auf jedem virtuellen Laufwerk.

 

Nachdem Sie Ihre virtuelle Festplatte erstellt haben, installieren Sie Windows XP auf dem Bild.

## <a href="" id="bkmk-installingwindowsxpontovpc"></a>Installieren von Windows XP auf einem Windows Virtual PC-Abbild


Für med-v muss Windows XP SP3 auf dem Windows Virtual PC-Abbild installiert sein, bevor Sie den Med-v-Arbeitsbereich erstellen.

Weitere Informationen zum Installieren von Windows XP finden Sie unter [Erstellen eines virtuellen Computers und Installieren eines Gastbetriebssystems](https://go.microsoft.com/fwlink/?LinkId=182379) ( https://go.microsoft.com/fwlink/?LinkId=182379) .

## <a href="" id="bkmk-installingnet"></a>Installieren von .NET Framework 3,5 SP1 auf einem Windows Virtual PC-Abbild


Sie müssen .NET Framework 3,5 SP1 und das Update KB959209 manuell in das Windows Virtual PC-Abbild installieren, das Sie für die Verwendung mit MED-V vorbereiten. Das Update [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) behebt verschiedene bekannte Anwendungskompatibilitätsprobleme.

## <a href="" id="bkmk-applypatchestovpc"></a>Anwenden von Updates auf das Windows Virtual PC-Abbild


Nachdem Sie Windows XP auf dem virtuellen Computer installiert haben, installieren Sie alle erforderlichen Windows XP-Updates auf dem Bild, wie etwa SP3. Sie können auch bestimmte optionale Updates installieren, um die Leistung zu verbessern.

**Wichtig**  Für MED-V muss Windows XP SP3 auf dem Gastbetriebssystem ausgeführt werden.

 

**Warnung**  Wenn Sie Updates für Windows XP installieren, stellen Sie sicher, dass Sie die Version von Internet Explorer in dem Gast verbleiben, den Sie im MED-V-Arbeitsbereich verwenden möchten. Wenn Sie beispielsweise Internet Explorer 6 im MED-V-Arbeitsbereich ausführen möchten, stellen Sie sicher, dass alle Updates, die Sie jetzt installieren, nicht mit Internet Explorer 7 oder Internet Explorer 8 verbunden sind. Darüber hinaus empfiehlt es sich, die Registrierung zu konfigurieren, um zu verhindern, dass automatische Updates Internet Explorer aktualisieren.

 

### Installieren eines optionalen Leistungsupdates

Obwohl dies optional ist, empfehlen wir, dass Sie das folgende Update für [Hotfix KB972435](https://go.microsoft.com/fwlink/?LinkId=201077) ( https://go.microsoft.com/fwlink/?LinkId=201077) . Dieses Update verbessert die Leistung von freigegebenen Ordnern in einer Terminaldienstesitzung:

**Hinweis**  Das Update ist öffentlich verfügbar. Möglicherweise werden Sie jedoch aufgefordert, eine Vereinbarung für Microsoft-Dienste zu akzeptieren. Folgen Sie den Anweisungen auf den nachfolgenden Webseiten, um diesen Hotfix abzurufen.

 

### Konfigurieren einer Leistungs Aktualisierung für Gruppenrichtlinien

Standardmäßig wird die Gruppenrichtlinie jeweils um ein Byte auf einen Computer heruntergeladen. Dies verursacht Verzögerungen, während MED-V zur Domäne hinzugefügt wird. Wenn Sie die Leistung von Gruppenrichtlinien erhöhen möchten, setzen Sie den folgenden Registrierungsschlüsselwert auf die Registrierung:

Registrierungsunterschlüssel: HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\windows NT\\CurrentVersion\\Winlogon

Eintrag: BufferPolicyReads

Geben Sie Folgendes ein: DWORD

Wert: 1

## <a href="" id="bkmk-installintegration"></a>Installieren von Integrationskomponenten


Windows Virtual PC enthält das Integrationskomponenten-Paket. Dies bietet Funktionen, die die Interaktion zwischen der virtuellen Umgebung und dem physikalischen Computer verbessern. So können Sie beispielsweise mit dem Integrationskomponenten-Paket die Maus zwischen dem Host und den Gastcomputern bewegen.

**Wichtig**  Für MED-V ist die Installation des Integrationskomponentenpakets erforderlich.

 

Wenn Sie das virtuelle Bild für die Zusammenarbeit mit MED-V konfigurieren, müssen Sie das Integrationskomponenten-Paket manuell auf dem Gastbetriebssystem installieren, um die verfügbaren Integrationsfeatures zu nutzen.

Weitere Informationen zum Installieren und Verwenden des Integrationskomponentenpakets finden Sie unter den folgenden Themen:

-   [Installieren oder Aktualisieren des Integrationskomponentenpakets](https://go.microsoft.com/fwlink/?LinkId=195923) ( https://go.microsoft.com/fwlink/?LinkId=195923) .

-   [Informationen zu Integrations Features](https://go.microsoft.com/fwlink/?LinkId=195924) ( https://go.microsoft.com/fwlink/?LinkId=195924) .

### Installieren der RemoteApp-Aktualisierung

Nachdem Sie das Integrationskomponenten-Paket installiert haben, werden Sie aufgefordert, das folgende Update zu installieren: "Update für Windows XP SP3 zum Aktivieren von RemoteApp". Dies ist eine erforderliche Komponente für MED-V.

**Wichtig**  Wenn Sie nicht aufgefordert werden, das RemoteApp-Update zu installieren, müssen Sie es manuell herunterladen und installieren. Weitere Informationen und Anweisungen zum Herunterladen dieses Updates finden Sie unter [Update für Windows XP SP3 zum Aktivieren von RemoteApp](https://go.microsoft.com/fwlink/?LinkId=195925) ( https://go.microsoft.com/fwlink/?LinkId=195925) .

 

### Aktivieren von Remote Desktop

Standardmäßig ist der Remote Desktop nach der Installation des Integrationskomponentenpakets aktiviert. Damit MED-V funktionsfähig ist, stellen Sie sicher, dass der Remote Desktop aktiviert ist, und verteilen Sie keine Gruppenrichtlinien, die ihn deaktiviert haben.

Informationen zum Aktivieren von Remote Desktop finden Sie unter [Aktivieren oder Deaktivieren von Remote Desktop](https://go.microsoft.com/fwlink/?LinkId=201162) ( https://go.microsoft.com/fwlink/?LinkId=201162) .

## Anpassen von Internet Explorer mit dem Internet Explorer-Verwaltungskit


Wenn Sie möchten, können Sie Internet Explorer mit dem Internet Explorer-Verwaltungskit auf dem Gastbetriebssystem anpassen. Weitere Informationen finden Sie im [Internet Explorer 6-Administrations-Kit und im Bereitstellungshandbuch](https://go.microsoft.com/fwlink/?LinkId=200007) (http://go.Microsoft.com/fwlink/?linkid=200007).

**Warnung**  Bedenken Sie die Sicherheitsaspekte, die mit dem Anpassen von Internet Explorer im MED-V-Arbeitsbereich verbunden sind. Weitere Informationen finden Sie unter [bewährte Methoden für die Sicherheit von MED-V-Vorgängen](security-best-practices-for-med-v-operations.md).

 

Nachdem die virtuelle Festplatte mit einem aktuellen Gastbetriebssystem installiert wurde, können Sie Anwendungen auf dem Bild installieren.

## Verwandte Themen


[Installieren von Anwendungen auf einem virtuellen Windows-PC-Image](installing-applications-on-a-windows-virtual-pc-image.md)

[Konfigurieren eines virtuellen Windows-PC-Images für MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md)

 

 





