---
title: Bereitstellen der Serverinfrastruktur von MBAM 1.0
description: Bereitstellen der Serverinfrastruktur von MBAM 1.0
author: dansimp
ms.assetid: 90529379-b70e-4c92-b188-3d7aaf1844af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: de136db557233a097d95f47ef0a1bba5996798c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810999"
---
# Bereitstellen der Serverinfrastruktur von MBAM 1.0


Sie können die Microsoft BitLocker-Verwaltungs-und-Überwachungs Server Features (MBAM) in verschiedenen Konfigurationen mithilfe von einem bis fünf Servern installieren. Im Allgemeinen sollten Sie je nach Ihren Skalierbarkeitsanforderungen eine Konfiguration mit drei bis fünf Servern für Produktionsumgebungen verwenden. Weitere Informationen zur Leistungsskalierbarkeit von MBAM und empfohlenen Bereitstellungs Topologien finden Sie unter [Whitepaper zur Skalierbarkeit von MBAM und Leitfaden für die höchst Verfügbarkeit](https://go.microsoft.com/fwlink/p/?LinkId=258314).

## Bereitstellen aller MBAM 1,0 auf einem einzelnen Server


In dieser Konfiguration sind alle MBAM-Features auf einem einzelnen Server installiert. Diese Bereitstellungstopologie für die MBAM-Serverinfrastruktur unterstützt bis zu 21.000-MBAM-Clientcomputer.

**Wichtig**  Diese Konfiguration wird unterstützt, aber wir empfehlen Sie nur zum Testen.

 

Die Verfahren in diesem Abschnitt beschreiben die vollständige Installation der MBAM-Features auf einem einzelnen Server.

[So installieren und Konfigurieren von MBAM auf einem Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)

## Bereitstellen von MBAM 1,0 auf verteilten Servern


MBAM-Features können je nach Ihren Skalierbarkeitsanforderungen in verschiedenen Konfigurationen installiert werden. Weitere Informationen zum Planen der Bereitstellung von MBAM Server Features finden Sie unter [Planen der MBAM 1,0-Server Bereitstellung](planning-for-mbam-10-server-deployment.md).

Die Verfahren in diesem Abschnitt beschreiben die vollständige Installation der MBAM-Features auf verteilten Servern.

### Konfiguration mit drei Computern

Das folgende Diagramm zeigt die Bereitstellungstopologie mit drei Computern für MBAM. Wir empfehlen diese Topologie für Produktionsumgebungen, die bis zu 55.000 MBAM-Clients unterstützen.

![mbam drei Computer Bereitstellungstopologie](images/mbam-3-server.jpg)

In dieser Konfiguration werden die MBAM-Features in der folgenden Konfiguration installiert:

1.  Wiederherstellungs-und Hardware Datenbank, Konformitäts-und Überwachungsdatenbank sowie Compliance-und Überwachungsberichte sind auf einem Server installiert.

2.  Die Verwaltungs-und Überwachungsserver Funktion ist auf einem Server installiert.

3.  Die MBAM-Gruppenrichtlinienvorlage ist auf einem Computer installiert, auf dem Gruppenrichtlinienobjekte (GPO) geändert werden können.

### Konfiguration mit vier Computern

Das folgende Diagramm zeigt die Bereitstellungstopologie mit vier Computern für MBAM. Wir empfehlen diese Topologie für Produktionsumgebungen, die bis zu 110.000 MBAM-Clients unterstützen.

![mbam vier Computer Bereitstellungstopologie.](images/mbam-4-computer.jpg)

In dieser Konfiguration werden die MBAM-Features in der folgenden Konfiguration installiert:

1.  Wiederherstellungs-und Hardware Datenbank, Konformitäts-und Überwachungsdatenbank sowie Compliance-und Überwachungsberichte sind auf einem Server installiert.

2.  Die Verwaltungs-und Überwachungsserver Funktion ist auf einem Server installiert, der in einem NLB-Server Cluster (Network Load Balancing) konfiguriert ist.

3.  Die MBAM-Gruppenrichtlinienvorlage ist auf einem Computer installiert, auf dem die Gruppenrichtlinienobjekte geändert werden können.

### Konfiguration mit fünf Computern

Das folgende Diagramm zeigt die fünf Computer Bereitstellungstopologie für MBAM. Wir empfehlen diese Topologie für Produktionsumgebungen, die bis zu 135.000 MBAM-Clients unterstützen.

![mbam fünf Computer Bereitstellungstopologie.](images/mbam-5-computer.jpg)

In dieser Konfiguration werden die MBAM-Features in der folgenden Konfiguration installiert:

1.  Die Wiederherstellungs-und Hardware Datenbank ist auf einem Server installiert.

2.  Die Compliance-und Audit-Datenbank sowie Compliance-und Überwachungsberichte sind auf einem Server installiert.

3.  Die Verwaltungs-und Überwachungsserver Funktion ist auf einem Server installiert, der in einem NLB-Server Cluster (Network Load Balancing) konfiguriert ist.

4.  Die MBAM-Gruppenrichtlinienvorlage ist auf einem Computer installiert, auf dem Gruppenrichtlinienobjekte geändert werden können.

[Installieren und Konfigurieren von MBAM auf verteilten Servern](how-to-install-and-configure-mbam-on-distributed-servers-mbam-1.md)

[So konfigurieren Sie den Netzwerklastenausgleich für MBAM](how-to-configure-network-load-balancing-for-mbam.md)

## Weitere Ressourcen für die Bereitstellung von MBAM 1,0 Server Features


[Bereitstellen von MBAM 1.0](deploying-mbam-10.md)

 

 





