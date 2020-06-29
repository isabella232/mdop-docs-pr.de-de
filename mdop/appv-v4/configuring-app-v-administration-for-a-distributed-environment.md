---
title: Konfigurieren von App-V-Verwaltung für eine verteilte Umgebung
description: Konfigurieren von App-V-Verwaltung für eine verteilte Umgebung
author: dansimp
ms.assetid: 53971fa9-8319-435c-be74-c37feb9af1da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c1a638d6afde9270859c8aa98fc9f421c39cfc72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809040"
---
# Konfigurieren von App-V-Verwaltung für eine verteilte Umgebung


Wenn Sie die Infrastruktur für Ihre spezifische Organisation entwerfen, können Sie den App-v Management Web Service auf einem anderen Computer als dem Computer installieren, auf dem Sie den App-v-Verwaltungs Server installieren. Häufige Gründe für die Trennung dieser App-V-Komponenten sind die folgenden:

-   Leistung

-   Zuverlässigkeit

-   Verfügbarkeit

-   Skalierbarkeit

Das Trennen des Verwaltungsservers und des Verwaltungs-Webdiensts erfordert eine zusätzliche Konfiguration für die ordnungsgemäße Funktionsweise der Infrastruktur. Wenn Sie diese beiden Features trennen, aber die in diesem Thema beschriebenen Verfahren nicht ausführen, stellt die Verwaltungskonsole eine Verbindung mit dem Verwaltungs-Webdienst her, kann sich aber nicht ordnungsgemäß mit dem Datenspeicher authentifizieren. Die Verwaltungskonsole wird nicht ordnungsgemäß geladen, und der Administrator kann keine administrativen Aufgaben ausführen.

Dieses Verhalten tritt auf, weil der Verwaltungs Webdienst die Anmeldeinformationen, die an ihn über die Verwaltungskonsole übergeben werden, nicht verwenden kann, um auf den Datenspeicher zuzugreifen. Die Lösung besteht darin, den Management Web Service-Server so zu konfigurieren, dass er "für Delegierungszwecke vertraut" ist.

## Konfigurieren von Active Directory-Domänendiensten


Darüber hinaus ist es erforderlich, die Active Directory-Domänendienste ordnungsgemäß für die Arbeit in einer verteilten Umgebung zu konfigurieren. Dieser Abschnitt enthält die Informationen, die Sie benötigen, um die Active Directory-Domänendienste zu konfigurieren.

### Wenn der SQL-Dienst lokales System Konto verwendet

Wenn Sie die Umgebung einrichten möchten, in der der SQL-Dienst das lokale Systemkonto verwendet, ändern Sie die Eigenschaften des Computerkontos des Verwaltungs-Webdiensts, damit es für die Delegierung als vertrauenswürdig eingestuft wird. Detaillierte Verfahren zur Vorgehensweise finden Sie unter [so wird es gemacht: Konfigurieren des Servers für die Delegierung als vertrauenswürdig](how-to-configure-the-server-to-be-trusted-for-delegation.md)

### Wenn der SQL-Dienstdomänen basiertes Konto verwendet

Zum Einrichten der Umgebung, in der SQL-Server domänenbasierte Dienstkonten verwenden, müssen Sie berücksichtigen, ob eine Vielzahl von Faktoren gelten soll, einschließlich der folgenden:

-   Clustering von SQL Server

-   Replikation

-   Automatisierte Aufgaben

-   Verknüpfte Server

Informationen zum Konfigurieren von Active Directory-Domänendiensten, wenn der SQL-Dienst ein domänenbasiertes Konto verwendet, finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=151968> .

 

 





