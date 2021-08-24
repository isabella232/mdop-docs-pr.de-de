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
ms.openlocfilehash: 63099d425b51bfde52eac59771007b1c765acf05
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910420"
---
# <a name="deploying-the-mbam-10-server-infrastructure"></a>Bereitstellen der Serverinfrastruktur von MBAM 1.0


Sie können Microsoft BitLocker Administration and Monitoring (MBAM)-Serverfeatures in unterschiedlichen Konfigurationen mit einem bis fünf Servern installieren. Im Allgemeinen sollten Sie eine Konfiguration von drei bis fünf Servern für Produktionsumgebungen verwenden, je nach Ihren Skalierbarkeitsanforderungen. Weitere Informationen zur Leistungsskalierbarkeit von MBAM und empfohlenen Bereitstellungstopologien finden Sie im [Whitepaper "MBAM-Skalierbarkeit und High-Availability Handbuch".](https://go.microsoft.com/fwlink/p/?LinkId=258314)

## <a name="deploy-all-mbam-10-on-a-single-server"></a>Bereitstellen aller MBAM 1.0 auf einem einzelnen Server


In dieser Konfiguration werden alle MBAM-Features auf einem einzelnen Server installiert. Diese Bereitstellungstopologie für die MBAM-Serverinfrastruktur unterstützt bis zu 21.000 MBAM-Clientcomputer.

**Wichtig**  
Diese Konfiguration wird unterstützt, wird jedoch nur zu Testzwecken empfohlen.

 

Die Verfahren in diesem Abschnitt beschreiben die vollständige Installation der MBAM-Features auf einem einzelnen Server.

[So installieren und Konfigurieren von MBAM auf einem Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)

## <a name="deploy-mbam-10-on-distributed-servers"></a>Bereitstellen von MBAM 1.0 auf verteilten Servern


MBAM-Features können je nach Ihren Skalierbarkeitsanforderungen in unterschiedlichen Konfigurationen installiert werden. Weitere Informationen zum Planen der Bereitstellung von MBAM-Serverfeatures finden Sie unter [Planning for MBAM 1.0 Server Deployment.](planning-for-mbam-10-server-deployment.md)

Die Verfahren in diesem Abschnitt beschreiben die vollständige Installation der MBAM-Features auf verteilten Servern.

### <a name="three-computer-configuration"></a>Konfiguration mit drei Computern

Das folgende Diagramm zeigt die Drei-Computer-Bereitstellungstopologie für MBAM. Wir empfehlen diese Topologie für Produktionsumgebungen, die bis zu 55.000 MBAM-Clients unterstützen.

![drei Computerbereitstellungstopologie für mbam.](images/mbam-3-server.jpg)

In dieser Konfiguration werden MBAM-Features in der folgenden Konfiguration installiert:

1.  Wiederherstellungs- und Hardwaredatenbank, Compliance- und Überwachungsdatenbank sowie Compliance- und Überwachungsberichte werden auf einem Server installiert.

2.  Das Verwaltungs- und Monitoring Server-Feature ist auf einem Server installiert.

3.  Die MBAM-Gruppenrichtlinienvorlage wird auf einem Computer installiert, der Gruppenrichtlinienobjekte (Group Policy Objects, GPO) ändern kann.

### <a name="four-computer-configuration"></a>Konfiguration mit vier Computern

Das folgende Diagramm zeigt die Bereitstellungstopologie mit vier Computern für MBAM. Wir empfehlen diese Topologie für Produktionsumgebungen, die bis zu 110.000 MBAM-Clients unterstützen.

![mbam four computer deployment topology.](images/mbam-4-computer.jpg)

In dieser Konfiguration werden MBAM-Features in der folgenden Konfiguration installiert:

1.  Wiederherstellungs- und Hardwaredatenbank, Compliance- und Überwachungsdatenbank sowie Compliance- und Überwachungsberichte werden auf einem Server installiert.

2.  Die Verwaltungs- und Überwachungsserverfunktion wird auf einem Server installiert, der in einem Netzwerklastenausgleichs-Servercluster (Network Load Balancing, NLB) konfiguriert ist.

3.  Die MBAM-Gruppenrichtlinienvorlage wird auf einem Computer installiert, der die Gruppenrichtlinienobjekte ändern kann.

### <a name="five-computer-configuration"></a>Konfiguration mit fünf Computern

Das folgende Diagramm zeigt die Bereitstellungstopologie mit fünf Computern für MBAM. Wir empfehlen diese Topologie für Produktionsumgebungen, die bis zu 135.000 MBAM-Clients unterstützen.

![mbam five computer deployment topology.](images/mbam-5-computer.jpg)

In dieser Konfiguration werden MBAM-Features in der folgenden Konfiguration installiert:

1.  Die Wiederherstellungs- und Hardwaredatenbank wird auf einem Server installiert.

2.  Die Compliance- und Überwachungsdatenbank sowie Die Konformitäts- und Überwachungsberichte werden auf einem Server installiert.

3.  Die Verwaltungs- und Überwachungsserverfunktion wird auf einem Server installiert, der in einem Netzwerklastenausgleichs-Servercluster (Network Load Balancing, NLB) konfiguriert ist.

4.  Die MBAM-Gruppenrichtlinienvorlage wird auf einem Computer installiert, der Gruppenrichtlinienobjekte ändern kann.

[Installieren und Konfigurieren von MBAM auf verteilten Servern](how-to-install-and-configure-mbam-on-distributed-servers-mbam-1.md)

[So konfigurieren Sie den Netzwerklastenausgleich für MBAM](how-to-configure-network-load-balancing-for-mbam.md)

## <a name="other-resources-for-mbam-10-server-features-deployment"></a>Weitere Ressourcen für die Bereitstellung von MBAM 1.0-Serverfeatures


[Bereitstellen von MBAM 1.0](deploying-mbam-10.md)

 

 





