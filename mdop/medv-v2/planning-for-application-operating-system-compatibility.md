---
title: Planen der Betriebssystemkompatibilität der Anwendung
description: Planen der Betriebssystemkompatibilität der Anwendung
author: dansimp
ms.assetid: cdb0a7f0-9da4-4562-8277-12972eb0fea8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b10da2c870e5ddc32098136225515cdd0523809
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811173"
---
# Planen der Betriebssystemkompatibilität der Anwendung


In diesem Thema wird erläutert, wie Kompatibilitätsprobleme mit Anwendungs Betriebssystemen behoben werden können, und es wird erläutert, wie Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 als Lösung für Ihre Organisation funktioniert.

In diesem Thema werden die geschäftlichen Anforderungen für med-v erläutert und der Vergleich zwischen Med-v und Windows XP-Modus und Microsoft Application Virtualization (app-v) beschrieben:

-   [Geschäftsanforderungen für MED-V](#bkmk-whenmedv)

-   [Vorteile von MED-V versus Windows XP-Modus](#bkmk-medvvsxp)

-   [Vorteile von Med-v versus App-v](#bkmk-medvvsappv)

## <a href="" id="bkmk-whenmedv"></a>Geschäftsanforderungen für MED-V


Wenn die IT-Abteilung Ihres Unternehmens feststellt, ob ein Upgrade auf Windows 7 durchgeführt werden soll, muss Sie auf Ihre Branchenanwendungen und webbasierten Branchenanwendungen achten, um sicherzustellen, dass diese unter dem neuen Betriebssystem ausgeführt werden können. Häufig wurden diese Anwendungen und URLs erstellt, um speziell mit einer älteren Version von Windows oder Internet Explorer zu arbeiten, und Probleme können auftreten, wenn Sie versuchen, Sie im neuen Betriebssystem zu verwenden. Microsoft bietet viele verschiedene Methoden zur Behandlung der verschiedenen Kompatibilitätsprobleme, die beim Upgrade auftreten können, beispielsweise das Application Compatibility Toolkit (Act) und der Windows 7-Programmkompatibilitäts-Assistent. Auch nachdem alle Anwendungen auf Kompatibilität getestet wurden und Korrekturen festgelegt wurden, funktionieren einige Anwendungen unter Windows 7 immer noch nicht richtig oder sind zu kostspielig, um Sie zu beheben.

Mithilfe von MED-V können Sie diese Legacyanwendungen über eine Windows Virtual PC-Umgebung ausführen, auf der Windows XP ausgeführt wird. Da Sie diese problemanwendungen nicht mehr vor dem Upgrade auf dem neuen Betriebssystem testen und überprüfen müssen, ist die Migration zu Windows 7 viel reibungsloser und schneller.

### Verwenden der MED-V-Checkliste

Bedenken Sie MED-V, wenn eines der folgenden Szenarien auf Sie zutrifft:

-   Sie eine große Organisation sind (beispielsweise 500-Benutzer und mehr), über einen Enterprise-Vertrag mit Microsoft verfügen und planen, ein Upgrade auf Windows 7 durchzuführen.

-   Sie haben Ihre Branchenanwendungen getestet und einige gefunden, die mit Windows 7 nicht kompatibel sind.

-   Sie haben die Kompatibilitätsprobleme für einige dieser problemanwendungen behoben, indem Sie die Anwendung aktualisieren oder ein von Microsoft bereitgestelltes Shim verwenden, beispielsweise das Application Compatibility Toolkit (Act), aber Kompatibilitätsprobleme bleiben für einige Anwendungen bestehen.

-   Sie haben App-v als eine Option für die Bereitstellung der nicht kompatiblen Anwendungen betrachtet und festgestellt, dass Sie auch nach der Implementierung von App-v weiterhin Kompatibilitätsprobleme mit dem Anwendungs Betriebssystem haben, die Sie berücksichtigen müssen.

-   Sie haben den Windows XP-Modus als Lösung betrachtet und festgestellt, dass es sich nicht um eine effiziente Option handelt, weil:

    -   Sie möchten in der Lage sein, virtuelle Bilder, die die problemanwendungen enthalten, für alle Endbenutzer gleichzeitig bereitzustellen, anstatt einzeln, und die virtuellen Bilder automatisch der Domäne hinzugefügt zu haben.

    -   Sie haben entschieden, dass es weitaus kostengünstiger ist, diese Legacyanwendungen (die praktisch geliefert werden) zu verwalten und die Windows Virtual PC-Einstellungen von einem zentralen Speicherort aus zu steuern, anstatt auf dem Desktop jedes Endbenutzers.

    -   Sie möchten in der Lage sein, die virtuellen Computer in Scale anstatt pro Desktop zu aktualisieren und zu unterstützen.

    -   Sie möchten, dass URLs, die in einer älteren Version von Internet Explorer besser ausgeführt werden, auf die virtuellen Computer umleiten und die URL-Umleitung später einfach verwalten können.

-   Sie haben festgestellt, dass es kostengünstiger und hilfreich wäre, so schnell wie möglich auf Windows 7 zu aktualisieren, und haben beschlossen, die Lösung ihrer verbleibenden Anwendungskompatibilitätsprobleme bis zu einem späteren Zeitpunkt zu verschieben, da Sie wissen, dass Sie über eine Lösung in MED-V verfügen.

## <a href="" id="bkmk-medvvsxp"></a> Vorteile von MED-V versus Windows XP-Modus


Mit Windows Virtual PC für Windows 7 können Sie unterschiedliche Versionen eines Betriebssystems gleichzeitig auf einem einzigen Gerät ausführen und sind in Windows 7 Professional Edition und höher verfügbar.

Die Funktionalität von Windows XP-Modus nutzt Windows Virtual PC, indem ein vorkonfiguriertes Windows XP-Abbild bereitgestellt wird, mit dem Sie eine virtuelle Windows XP-Umgebung erstellen können. In dieser virtuellen Umgebung können Sie Anwendungen manuell installieren, die mit Windows 7 nicht kompatibel sind und von Ihrem Desktop aus über den Windows Virtual PC nahtlos ausgeführt werden.

**Mithilfe des Windows XP-Modus können Sie die folgenden Aktionen ausführen:**

-   Ausführen von Anwendungen, die mit Windows XP kompatibel sind, in einem virtuellen Computer, der in Windows Virtual PC ausgeführt wird.

-   Veröffentlichen Sie diese Anwendungen im Desktop-oder Programmmenü des Hosts.

Wenn Sie diese virtuellen Computer im Rahmen einer Unternehmens Migration zu Windows 7 im großen Maßstab bereitstellen möchten, müssen Sie in der Lage sein, die virtuellen Computer schnell bereitzustellen, effizient bereitzustellen und anzupassen, Ihre Einstellungen zu steuern und Sie einfach zu unterstützen.

MED-V baut auf dem Windows XP-Modus auf, um unternehmensweite Anwendungskompatibilität zu bieten. Während sich der Windows XP-Modus auf die Bereitstellung virtueller Anwendungsfunktionen für Einzelpersonen und kleine Unternehmen ausrichtet, ermöglicht MED-V die Bereitstellung von vorkonfigurierten Windows XP-Images in großem Umfang im gesamten Unternehmensnetzwerk. Es bietet Ihnen eine Unternehmens bereite Verwaltungslösung für die Konfiguration, Bereitstellung und Wartung dieser virtuellen MED-V-Arbeitsbereiche. MED-V bietet enterpriseadministrators außerdem eine Reihe von Richtlinien zur Steuerung der Bild Verwendung. Dies beinhaltet, welche Benutzer Zugriff auf welche spezifischen Anwendungen innerhalb dieser Bilder haben werden.

**Mithilfe von MED-V können Sie die folgenden Aktionen ausführen:**

-   Aktualisieren Sie auf Ihr neues Betriebssystem, ohne jede inkompatible Anwendung und URL testen und beheben zu müssen.

-   Stellen Sie virtuelle Windows XP-Bilder bereit, die automatisch mit der Domäne verbunden und pro Benutzer angepasst werden.

-   Bereitstellen von Anwendungen und URL-Umleitungsinformationen für Benutzer

-   Steuern der Windows Virtual PC-Einstellungen

-   Verwalten und unterstützen von Endpunkten durch Überwachung und Problembehandlung

-   Stellen Sie sicher, dass die Gastcomputer gepatcht werden, auch wenn Sie in einem angehalten-Zustand sind.

-   Automatisieren Sie die Erstellung virtueller Computer pro Benutzer und die Sysprep-Initialisierung.

-   Einfache Diagnose von Problemen auf den Host-und Gastcomputern

-   Nahtloses Verwalten von Gastcomputern, die über den Windows Virtual PC-NAT-Modus verbunden sind.

## <a href="" id="bkmk-medvvsappv"></a>Vorteile von Med-v versus App-v


Med-v und App-v sind zwei sehr unterschiedliche Technologien, die problemlos zusammenarbeiten können, um Kompatibilitätsprobleme mit dem Anwendungs Betriebssystem zu lösen. Mithilfe von App-V erstellen Sie für jede Anwendung ein individualisiertes Paket, das jeweils getrennt von den anderen Anwendungen aufbewahrt wird. Jede virtuelle Anwendung kann dann sofort an den Endbenutzer übermittelt werden, was sehr hilfreich für eine Windows 7-Bereitstellungsstrategie ist.

MED-V behandelt Anwendungen nicht einzeln. Stattdessen wird eine weitere Instanz von Windows XP auf dem Desktop erstellt, auf dem Windows 7 ausgeführt wird. Sie können in diesem virtuellen Bild so viele Anwendungen wie nötig installieren und das Bild genauso wie jeden anderen Desktop in Ihrer Organisation verwalten.

Darüber hinaus können Sie Med-v zusammen mit App-v verwenden, damit virtuelle Anwendungen, die über APP-v sequenziert sind, mithilfe von Med-v installiert, veröffentlicht und verwaltet werden.

## Verwandte Themen


[Definieren und Planen der MED-V-Bereitstellung](define-and-plan-your-med-v-deployment.md)

 

 





