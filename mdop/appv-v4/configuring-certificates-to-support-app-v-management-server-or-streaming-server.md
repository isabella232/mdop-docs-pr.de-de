---
title: Konfigurieren von Zertifikaten zur Unterstützung von App-V Management Server oder Streaming Server
description: Konfigurieren von Zertifikaten zur Unterstützung von App-V Management Server oder Streaming Server
author: dansimp
ms.assetid: 2f24e550-585e-4b7e-b486-22a3f181f543
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e537244b24d7303af550b3ced8286ba2680009e7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809031"
---
# Konfigurieren von Zertifikaten zur Unterstützung von App-V Management Server oder Streaming Server


Nachdem Sie den Zertifikat Bereitstellungsprozess abgeschlossen und die Berechtigungen für den privaten Schlüssel zur Unterstützung der App-V-Installation geändert haben, können Sie das Setup des Verwaltungsservers oder des Streaming Servers starten. Wenn während des Setups ein Zertifikat bereitgestellt wird, bevor das Setupprogramm ausgeführt wird, zeigt der Assistent das Zertifikat im Bildschirm **Verbindungssicherheitsmodus** an, und das Kontrollkästchen **verstärkte Sicherheit verwenden** ist standardmäßig aktiviert.

**Hinweis**  Wählen Sie das Zertifikat aus, das für App-V konfiguriert wurde, wenn mehr als ein Zertifikat für diesen Server bereitgestellt wurde.

 

**Wichtig**  Beim Upgrade von Version 4,2 auf Version 4,5 verfügt das Setup über eine Option für die **Verwendung von erweiterter Sicherheit**. Wenn Sie diese Option auswählen, wird das Streaming über RTSP jedoch nicht deaktiviert. Sie müssen die Verwaltungskonsole verwenden, um RTSP nach der Installation zu deaktivieren.

 

Wählen Sie den TCP-Port aus, den der Dienst für die Clientkommunikation verwenden soll. Der Standardport ist TCP 322; Sie können den Port jedoch in einen benutzerdefinierten Port für Ihre Umgebung ändern.

Die verbleibenden Schritte des Assistenten sind identisch mit der Bereitstellungeines App-V-Verwaltungs-oder Streaming-Servers, ohne das Feature **Erweiterte Sicherheit** zu verwenden.

## Konfigurieren von Zertifikaten für NLB-Umgebungen


Um große Unternehmen zu unterstützen, wird der Verwaltungs Server häufig in einem NLB-Cluster (Network Load Balancing, Netzwerklastenausgleich) gespeichert, um die große Anzahl von Verbindungen zu unterstützen. Dazu sind mindestens zwei Verwaltungsserver erforderlich, die anscheinend ein einzelner Verwaltungsserver sind. Wenn in Ihrer Umgebung ein NLB-Cluster mit mehreren Verwaltungsservern verwendet wird, benötigen Sie eine erweiterte Konfiguration des für den NLB-Cluster verwendeten Zertifikats.

Das App-V-Zertifikat wird an eine Zertifizierungsstelle (Certification Authority, ca) übermittelt, die auf einem Computer mit Windows-Server2003 konfiguriert ist. Mit dem San können Sie eine Verbindung mit einem bestimmten Verwaltungs Server-NLB-Clusterhost Namen herstellen, indem Sie einen DNS-Namen (Domain Name System) verwenden, der möglicherweise von den tatsächlichen Computernamen abweicht, da es bis zu 32-Server geben kann, die den NLB-Cluster umfassen.

Diese Konfiguration ist nur bei Verwendung eines NLB-Clusters erforderlich. Wenn der Client eine Verbindung mit dem Server herstellt, wird er mit dem vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des NLB-Clusters und nicht mit dem FQDN eines einzelnen Servers verbunden. Wenn Sie die San-Eigenschaft nicht mit dem FQDN der Serverknoten im Cluster hinzufügen, werden alle Clientverbindungen abgelehnt, weil der allgemeine Name des Zertifikats nicht mit dem Servernamen übereinstimmt.

Ausführlichere Informationen zum Konfigurieren von Zertifikaten mit dem San-Attribut finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=133228> .

## Verwandte Themen


[Konfigurieren von Zertifikaten zur Unterstützung von sicherem Streaming](configuring-certificates-to-support-secure-streaming.md)

[So ändern Sie Berechtigungen für private Schlüssel zur Unterstützung von Management Server oder Streaming Server](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)

 

 





