---
title: Verwalten von automatischen Updates für MED-V-Arbeitsbereiche
description: Verwalten von automatischen Updates für MED-V-Arbeitsbereiche
author: dansimp
ms.assetid: 306f28a2-d653-480d-b737-4b8b3132de5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b22d3250db806e740c1d62da4fed98d5956b0eeb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811068"
---
# Verwalten von automatischen Updates für MED-V-Arbeitsbereiche


Der MED-V-Arbeitsbereich ist ein virtueller Computer, der ein separates Betriebssystem enthält, dessen automatischer Softwareupdateprozess genauso wie die physischen Computer in Ihrem Unternehmen verwaltet werden muss. Da das Gastbetriebssystem nicht immer unbedingt ausgeführt wird, wenn das Betriebssystem des Hosts ausgeführt wird, müssen Sie sicherstellen, dass der virtuelle MED-V-Computer so konfiguriert ist, dass Softwareupdates nach Bedarf auf das Gastbetriebssystem angewendet werden können. Die Microsoft Enterprise Desktop Virtualization (Med-v) 2,0-Lösung bietet die Funktionalität, mit der Sie ermitteln können, wie automatische Softwareupdates in einem MED-V-Arbeitsbereich verarbeitet werden.

## Verwalten der Wake-up-Richtlinie für den MED-V-Arbeitsbereich


Die Wake-up-Richtlinie für med-v Workspace garantiert, dass der virtuelle Med-v-Computer für den Zeitraum, den Sie in ihren Med-v-Konfigurationseinstellungen angeben, für Updates zur Verfügung gestellt wird. Dies gilt sowohl für Updates, die von Microsoft über Windows Update veröffentlicht werden, als auch für Updates, die von nicht von Microsoft bereitgestellten Lösungen wie Antivirus-Anwendungen bereitgestellt und gesteuert werden.

**Wichtig**  Die Wake-up-Richtlinie für den MED-V-Arbeitsbereich wurde für die Microsoft Update-Infrastruktur optimiert. Wenn Sie Microsoft System Center Configuration Manager zum Bereitstellen von nicht-Microsoft-Updates verwenden, empfiehlt es sich, auch den System Center Updates Publisher zu verwenden, der die gleiche Infrastruktur wie Microsoft Update nutzt und daher von der Wake-up-Richtlinie des MED-V-Arbeitsbereichs profitiert. Weitere Informationen finden Sie unter [System Center Updates Publisher](https://go.microsoft.com/fwlink/?LinkId=200035) ( https://go.microsoft.com/fwlink/?LinkId=200035) .

 

Beim Erstellen Ihres MED-V-Arbeitsbereichs Pakets haben Sie festgelegt, wann und wie es gestartet wird, entweder, wenn sich der Endbenutzer anmeldet (**Fast Start**) oder wenn der Endbenutzer zuerst eine veröffentlichte Anwendung öffnet (**normaler Anfang**). Sie können aber auch die Option festlegen, mit der der Endbenutzer diese Einstellung steuern kann.

So oder so, wenn die Option " **schnell Start** " ausgewählt ist, wird der virtuelle Computer weiterhin ausgeführt, solange der MED-V-Host als Benutzer angemeldet ist. Da Med-v in dieser Konfiguration aktiv ist, wenn der Host aktiv ist, werden automatische Updates angewendet, ohne dass eine zusätzliche Verarbeitung von Med-v erforderlich ist.

In den Fällen, in denen " **schnell Start** " nicht angegeben ist oder der virtuelle Computer in den Ruhezustand versetzt wird oder beendet wird, garantiert Med-v über die Wake-up-Richtlinie des Med-v-Arbeitsbereichs, dass das Gastbetriebssystem regelmäßig aktualisiert wird, auch wenn Med-v nicht regelmäßig verwendet wird. MED-V führt diese Funktion aus, indem Sie den virtuellen Computerregel mäßig basierend auf den von Ihnen angegebenen Konfigurationseinstellungen aufweckt. Auf diese Weise können die Clients für automatische Updates auf dem virtuellen Computer basierend auf Ihren Konfigurationen ausgeführt werden.Nachdem der durch die Med-v-Konfigurationseinstellung definierte Zeitraum abgelaufen ist, gibt Med-v den virtuellen Computer in seinen vorherigen Zustand zurück.

**Hinweis**  Wenn der Endbenutzer während des Aktualisierungszeitraums eine veröffentlichte Anwendung öffnet, werden die erforderlichen Updates angewendet, aber MED-V wird nicht automatisch in den Ruhezustand versetzt oder nach dem Ende des Aktualisierungszeitraums beendet. Stattdessen wird MED-V weiterhin ausgeführt.

 

Die Wake-up-Richtlinie für den MED-V-Arbeitsbereich umfasst drei Hauptkomponenten:

**Gast Update-Manager**

Dieses eigenständige ausführbare Programm, das sich auf dem MED-V-Host befindet, ist für das Aufwachen des virtuellen Computers entsprechend einem vordefinierten, konfigurierbaren Zeitplan verantwortlich. Geben Sie die Konfigurationseinstellungen an, um anzugeben, zu welchem Zeitpunkt der Update-Manager jeden Tag den virtuellen Computer reaktivieren soll, und wie lange die virtuelle Maschine wach gehalten werden soll (in Minuten), damit Updates angewendet werden können. Nachdem die angegebene Anzahl von Minuten erreicht wurde, versetzt der gastupdate-Manager den virtuellen Computer in den Ruhezustand, der für die nächste Verwendung vorbereitet wurde. Sie können die Ausführung dieses ausführbaren Programms über den Windows Task-Manager planen.

**Verwaltungsdienst für Gast Neustart**

Dieser Dienst, der sich auf dem MED-V-Host befindet, hat drei Hauptaufgaben. Zusammen mit dem Guest Update Manager verwaltet er den Neustart des virtuellen Computers bei der Benutzeranmeldung, falls dies erforderlich ist. Sie erkennt, dass ein Neustart von virtuellen Maschinen erforderlich ist, wenn Updates installiert werden. Und es wird sichergestellt, dass die Aufgabe für den Guest Update Manager immer entsprechend der Konfiguration geplant wird.

**Gast Aktualisierungsdienst**

Dieser Windows-Dienst, der sich auf dem virtuellen MED-V-Computer befindet, ist dafür verantwortlich, zu überwachen, wenn für installierte Updates ein Neustart erforderlich ist. Nachdem dem Dienst mitgeteilt wird, dass ein Neustart erforderlich ist, benachrichtigt er den Guest-Neustart-Verwaltungsdienst auf dem Host.

### Konfigurationseinstellungen für die Wake-up-Richtlinie für den MED-V-Arbeitsbereich

Sie steuern, wann und wie lange der virtuelle Computer aufwacht, um automatische Updates zu erhalten, indem Sie die folgenden zwei Konfigurationswerte in der Registrierung definieren. Beide Werte befinden sich unter dem HKLM\\Software\\Microsoft\\MEDV\\v2\\VM-Schlüssel.

**GuestUpdateTime** – konfiguriert die Stunden und Minuten pro Tag, wenn MED-V den virtuellen Computer zum Aktualisieren basierend auf dem 24-Stunden-Standard der Uhr reaktivieren muss. Geben Sie die Uhrzeit im Format hh: mm ein. Der Standardwert ist 00:00 (Midnight).

**GuestUpdateDuration** – konfiguriert die Anzahl der Minuten, für die MED-V den virtuellen Computer für die Aktualisierung wach halten muss, beginnend mit der in der GuestUpdateTime-Konfigurationseinstellung angegebenen Zeit. Der Standardwert ist 240 (4 Stunden). Wenn dieser Wert auf 0 (null) festgelegt wird, wird die Wake-up-Richtlinie für den MED-V-Arbeitsbereich deaktiviert.

Weitere Informationen zum Definieren Ihrer Med-v-Konfigurationswerte finden Sie unter [Verwalten von Med-v Workspace-Konfigurationseinstellungen](managing-med-v-workspace-configuration-settings.md).

**Hinweis**  Eine optimale Methode für med-v besteht darin, das Aktivierungsintervall so einzurichten, dass es der Zeit entspricht, zu der die virtuellen Med-v-Maschinen regelmäßig aktualisiert werden sollen. Darüber hinaus empfiehlt es sich, diese Einstellungen so zu konfigurieren, dass Sie dem Verhalten des Hostcomputers ähneln.

 

### Neustart der Benachrichtigung mithilfe Ihres ESD-Systems

Sie können Ihr ESD-System so konfigurieren, dass es Med-v benachrichtigt, wenn ein Neustart für den Med-v-Arbeitsbereich erforderlich ist, nachdem automatische Updates angewendet wurden. Wenn Sie automatische Updates über Ihr ESD-System anwenden und wissen, dass ein Neustart erforderlich ist, sollten Sie ein Skript schreiben, um das folgende globale Ereignis im MED-V-Arbeitsbereich zu signalisieren:

**Wichtig**  Sie müssen das Ereignis mit nur Rechte ändern öffnen und dann signalisieren. Wenn Sie es nicht mit den richtigen Berechtigungen öffnen, funktioniert es nicht.

 

``` syntax
/// <summary>
/// The guest is required to be restarted due to an ESD update.
/// </summary>
public const string MedvGuestRebootRequiredEventName = @"Global\MedvGuestRebootRequiredEvent";
using (EventWaitHandle notificationEvent = 
EventWaitHandle.OpenExisting(eventName, EventWaitHandleRights.Modify))
{
notificationEvent.Set();
}
```

Wenn Sie dieses Ereignis signalisieren, wird es von MED-V erfasst und dem virtuellen Computer darüber informiert, dass ein Neustart erforderlich ist.

## Verwandte Themen


[Verwalten von Softwareupdates für MED-V-Arbeitsbereiche](managing-software-updates-for-med-v-workspaces.md)

 

 





