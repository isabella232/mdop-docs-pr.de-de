---
title: Identifizieren der Anzahl und Typen von MED-V-Arbeitsbereichen
description: Identifizieren der Anzahl und Typen von MED-V-Arbeitsbereichen
author: dansimp
ms.assetid: 11642253-6b1f-4c4a-a11e-48d8a360e1ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e0c9ed4b0ce92d0ca752525b847405bbce90a270
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812250"
---
# Identifizieren der Anzahl und Typen von MED-V-Arbeitsbereichen


MED-V erstellt eine virtuelle Umgebung zum Ausführen von Anwendungen, die Windows XP erfordern oder für die eine Version von Internet Explorer erforderlich ist, die von der Version auf dem Hostcomputer abweicht. Diese virtuelle Umgebung wird als MED-V-Arbeitsbereich bezeichnet.

Je nach den Anwendungs Kompatibilitätsanforderungen, die Ihre Organisation bei der Migration zu Windows 7 hat, können nur bestimmte Benutzer oder Abteilungen MED-V-Arbeitsbereiche benötigen. Bei der Planung der Bereitstellung müssen Sie die Anzahl der MED-V-Arbeitsbereiche ermitteln, die für Ihr Unternehmen erforderlich sind. Darüber hinaus müssen Sie die Anforderungen für jeden MED-V-Arbeitsbereich definieren.

## Ermitteln der Anzahl und Typen von MED-V-Arbeitsbereichen


Identifizieren Sie die Computer und Gruppen in Ihrem Unternehmen, für die Sie MED-V-Arbeitsbereiche erstellen werden. In der Regel sind dies die Benutzer, die Zugriff auf die Anwendungen benötigen, die nicht zu Windows 7 migriert werden können. Identifizieren Sie die Anwendungen, die nicht migriert werden können, und die Benutzer, die einen MED-V-Arbeitsbereich zum Ausführen dieser Anwendungen benötigen.

Möglicherweise haben Sie auch Intranet-Adressen, die noch nicht für Windows 7 optimiert wurden. Der MED-V-Arbeitsbereich bietet einen Internet Explorer-Browser, über den Endbenutzer besser auf diese Webadressen zugreifen können, die noch nicht für die Migration zu Windows 7 bereit sind. Während Sie Ihre Med-v-Bereitstellung vorbereiten und planen, müssen Sie eine Liste der URL-Adressen identifizieren und kompilieren, die von Internet Explorer auf dem Hostcomputer an Internet Explorer im Med-v-Arbeitsbereich umgeleitet werden sollen.

Schließlich müssen Sie Ihre Speicherplatzanforderungen auswerten. Die meisten MED-V-Arbeitsbereiche sind 2 Gigabyte (GB) oder größer. Je nach Anzahl der Benutzer und der Konfiguration von MED-V kann der verfügbare Speicherplatz auf einem System schnell genutzt werden. Außerdem kann die bevorzugte Verteilungsmethode Ihres Unternehmens zusätzlichen Speicherplatz benötigen. Im Allgemeinen sollten Sie eine Mindestmenge von 10 GB Speicherplatz für einen MED-V-Arbeitsbereich freigeben, doch variiert dies je nach Größe des Bilds erheblich.

### Berechnen der Speicherplatzanforderungen für MED-V-Arbeitsbereiche

Ein MED-V-Arbeitsbereich erfordert Arbeitsspeicher und Speicherplatz auf dem Hostcomputer, auf dem er installiert ist. Auf dem Host sind mindestens 2 GB Speicherplatz erforderlich. Der Speicherplatz ist variabel und hängt von der Anzahl der Anwendungen und den Daten im MED-V-Arbeitsbereich eines Benutzers ab.

Wir empfehlen einen Mindestspeicher von 10 GB Speicherplatz für MED-V. Dieser Betrag ermöglicht einen einfachen Windows XP-Arbeitsbereich und einige grundlegende installierte Anwendungen und die webumleitung. Darüber hinaus steht der Speicherplatz für das Host-Swap-Laufwerk zur Verfügung. In einer einfachen Konfiguration verbraucht Med-v und ein einzelner bereitgestellter Med-v-Arbeitsbereich so viel wie 6 bis 8 GB. Wenn Sie viele Anwendungen in den Med-v-Arbeitsbereich einbeziehen oder mehr als einen Benutzer pro Computer haben, können Sie die folgende Berechnung verwenden, um den von Ihrem Med-v-Arbeitsbereich benötigten Speicherplatz genauer zu ermitteln:

*Basis-VHD + (Benutzer pro Computer x (Differenzdaten Träger + gespeicherter Zustand))*

Um den erforderlichen Speicherplatz zu berechnen, müssen Sie Folgendes ermitteln:

-   **Größe der Basis-VHD** – die virtuelle Festplatte, die zum Erstellen des MED-V-Arbeitsbereichs verwendet wurde.

    **Wichtig**  Verwenden Sie die medv-Dateigröße für Ihre Berechnung nicht, da die medv-Datei komprimiert ist.

     

-   **Benutzer pro Computer** – Med-v erstellt einen Med-v-Arbeitsbereich für jeden Benutzer auf einem Computer; der Med-v-Arbeitsbereich beansprucht Speicherplatz, während sich jeder Benutzer anmeldet und der Med-v-Arbeitsbereich erstellt wird.

-   **Die Größe des differenzierenden Datenträgers** – wird verwendet, um den Unterschied zur Basisfestplatte zu überwachen. Diese Größe variiert beim Hinzufügen von Anwendungen und Softwareupdates zur virtuellen Festplatte. Für jeden Med-v-Benutzer wird ein differenzierender Datenträger erstellt, wenn Sie Med-v zum ersten Mal starten.

-   **Die Größe der gespeicherten Zustandsdatei** – wird verwendet, um den Zustand auf dem virtuellen Computer beizubehalten. In der Regel ist dies nur ein bisschen größer als der zugewiesene Arbeitsspeicher für den virtuellen Computer. Beispielsweise erstellt 1 GB Arbeitsspeicher eine Datei über 1.081.000 KB.

Das folgende Beispiel zeigt eine Berechnung auf der Grundlage von drei Benutzern eines MED-V-Arbeitsbereichs mit einer virtuellen 2,6 GB-Festplatte:

*2.6 GB + (3 x (1,5 GB + 1GB)) = 10,1 GB*

**Hinweis**  Eine optimale Methode für MED-V besteht darin, den erforderlichen Speicherplatz mithilfe einer Lab-Bereitstellung zu berechnen, um die Anforderungen zu überprüfen.

 

### Suchen der Dateien zum Ermitteln der Dateigröße

Die folgenden Speicherorte enthalten die Dateien für die Computer-und Benutzereinstellungen:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Typ</th>
<th align="left">Pfad</th>
<th align="left">Dateien</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Basis-VHD</p></td>
<td align="left"><p>%ProgramData%\Microsoft\Medv\Workspace</p></td>
<td align="left"><p><em>InternalName </em> . VHD – wobei <em> internalname </em> der Name der virtuellen Festplatte ist, die Sie im MED-V Workspace-Paketer ausgewählt haben.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Differenzierender Datenträger</p></td>
<td align="left"><p>%LocalAppData%\Microsoft\MEDV\v2\Virtual-Maschinen</p></td>
<td align="left"><p><em>WorkspaceName </em> . VHD</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gespeicherte Statusdatei</p></td>
<td align="left"><p>%LocalAppData%\Microsoft\MEDV\v2\Virtual-Maschinen</p></td>
<td align="left"><p><em>WorkspaceName </em> . VSV</p></td>
</tr>
</tbody>
</table>

 

### Berechnen der Speicherplatzanforderungen für freigegebene MED-V-Arbeitsbereiche

Wenn Sie für eine freigegebene Med-v Workspace-Bereitstellung auf einem einzelnen Computer berechnen, ist die Anzahl der Benutzer pro Computer in ihrer Berechnung immer "1", da Med-v nur einen einzelnen differenzierenden Datenträger für alle Benutzer konfiguriert.

Sie können den differenzierenden Datenträger und die gespeicherte Zustandsdatei für freigegebene MED-V-Arbeitsbereiche in%ProgramData%\\Microsoft\\Medv\\AllUsers. finden.

## Verwandte Themen


[Definieren und Planen der MED-V-Bereitstellung](define-and-plan-your-med-v-deployment.md)

[Planen für MED-V](planning-for-med-v.md)

 

 





