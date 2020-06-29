---
title: Informationen zu virtuellen Umgebungen
description: Informationen zu virtuellen Umgebungen
author: dansimp
ms.assetid: e03a8c72-56c1-4ae9-aa45-0283c50a154c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 15f3ae29ae8d5586f83baa98ea6821e09ae5c305
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809328"
---
# Informationen zu virtuellen Umgebungen


Virtuelle Anwendungen werden in virtuellen Umgebungen ausgeführt. In virtuellen Umgebungen kann jede Anwendung auf einem Desktop-, Laptop-oder Remote Desktop-Sitzungshost Server (RDSession-Host) ohne Installation und Änderung des Hostbetriebssystems ausgeführt werden. Jede Anwendung enthält eigene Konfigurationsinformationen in der virtuellen Umgebung. Daher laufen viele Anwendungen parallel mit anderen Anwendungen auf demselben Computer ohne Konflikte.

Virtuelle Anwendungen werden lokal ausgeführt, sodass Sie mit der vollständigen Leistung, Funktionalität und dem Zugriff auf lokale Dienste ausgeführt werden, die Sie von einer lokal installierten Anwendung erwarten.

Da jede Anwendung in einer virtuellen Umgebung ausgeführt wird, werden die folgenden Probleme reduziert:

-   Anwendungskonflikte – in Umgebungen, die keine Anwendungsvirtualisierung verwenden, müssen Sie jede Anwendung gründlich testen, um sicherzustellen, dass Sie keine anderen installierten Anwendungen stört.

-   Regressionstests – da die Anwendung das zugrunde liegende Betriebssystem nicht ändert, werden langwierige Regressionstests eliminiert.

-   Versionsinkompatibilitäten – verschiedene Versionen der gleichen Anwendung können gleichzeitig auf demselben Computer ausgeführt werden.

-   Mehrbenutzerzugriff – Anwendungen, die nicht im Mehrbenutzermodus ausgeführt werden und daher nicht in einem RDSession-Host ausgeführt werden können, können dies nun tun und für mehrere Benutzer auf einem einzelnen RDSession-Host ordnungsgemäß funktionieren.

-   Probleme mit mehreren Instanzen: zwei Instanzen der gleichen Anwendung, die unterschiedliche Konfigurationen verwenden, können gleichzeitig auf demselben Computer ausgeführt werden.

-   Server-siloing – die Notwendigkeit für viele getrennte Serverfarmen wird eliminiert.

Virtuelle Umgebungen umfassen eine virtuelle Registrierung für jede Anwendung. Von einer Anwendung erstellte Registrierungseinstellungen können von anderen Anwendungen oder Dienstprogrammen wie "regedit" nicht angezeigt werden. Anstatt die gesamte Registrierung zu kopieren, verwendet die virtuelle Registrierung eine *Overlay* -Methode. Elemente in der Clientregistrierung können von der Anwendung gelesen werden, solange eine virtuelle Kopie dieses Registrierungselements nicht in der virtuellen Registrierung enthalten ist. Alle Anwendungs Schreibvorgänge in der Registrierung sind in der virtuellen Registrierung enthalten.

Zu den virtuellen Umgebungen gehören auch ein virtuelles Dateisystem und andere virtuelle Komponenten, einschließlich virtueller Dienste und virtueller com.

## Verwandte Themen


[Application Virtualization Client Management Console – Übersicht](application-virtualization-client-management-console-overview.md)

 

 





