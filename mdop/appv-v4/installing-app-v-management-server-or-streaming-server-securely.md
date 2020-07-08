---
title: Sicheres Installieren von App-V Management Server oder Streaming Server
description: Sicheres Installieren von App-V Management Server oder Streaming Server
author: dansimp
ms.assetid: d2a51a81-a80f-427c-a727-611e1eb74f02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0150f4dc7f489731c4a818fed9780ebb25dbd24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806663"
---
# Sicheres Installieren von App-V Management Server oder Streaming Server


Die Themen in diesem Abschnitt enthalten Informationen zum Installieren einer erweiterten Sicherheitsversion des App-v-Verwaltungsservers oder des App-v-Streaming-Servers.

**Hinweis**  Zum Installieren oder Konfigurieren eines App-v-Verwaltungs-oder Streaming-Servers zur Verwendung der erweiterten Sicherheit (beispielsweise Transport Layer Security oder TLS) muss ein X. 509 v3-Zertifikat für den App-v-Server bereitgestellt werden.

 

Wenn Sie sich für die Installation oder Konfiguration eines sicheren Management-oder Streaming-Servers vorbereiten, sollten Sie die folgenden technischen Voraussetzungen Bedenken:

-   Das Zertifikat muss gültig sein. Wenn das Zertifikat ungültig ist, beendet der Client die Verbindung.

-   Das Zertifikat muss die korrekte *Erweiterte Schlüsselverwendung (Enhanced Key Usage* , EKU) – Server Authentifizierung (OID 1.3.6.1.5.5.7.3.1) enthalten. Wenn das Zertifikat diese EKU nicht enthält, beendet der Client die Verbindung.

-   Der vollqualifizierte Domänenname (Fully Qualified Domain Name, FQDN) des Zertifikats muss mit dem Server übereinstimmen, auf dem er installiert ist. Wenn beispielsweise der Client angerufen wird `RTSPS://Myserver.mycompany.com/content/MyApp.sft` und das **für Field ausgegebene** Zertifikat auf eingestellt ist `Server1.mycompany.com` , stellt der Client keine Verbindung mit dem Server her, und die Sitzung endet. Der Fehler wird dem Benutzer gemeldet.

    **Hinweis**  Wenn Sie App-V in einem Netzwerklastenausgleich-Cluster verwenden, müssen Sie das Zertifikat mit "Subject Alternate Names (SANs)" konfigurieren, um RTSPS zu unterstützen. Informationen zum Konfigurieren der Zertifizierungsstelle und zum Erstellen von Zertifikaten mit Sans finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=133228> .

     

-   Der Client und der Server müssen der Stammzertifizierungsstelle vertrauen – die Zertifizierungsstelle, die das Zertifikat an den App-V-Server ausgibt, muss vom Client als vertrauenswürdig eingestuft werden. Wenn dies nicht der Fall ist, beendet der Client die Verbindung.

-   Für den privaten Schlüssel des Zertifikats muss die Berechtigung geändert werden, damit das App-V-Dienstkonto auf das Zertifikat zugreifen kann. Standardmäßig verwendet App-V das Netzwerkdienstkonto, und das Netzwerkdienstkonto verfügt standardmäßig nicht über die Berechtigung für den Zugriff auf den privaten Schlüssel, wodurch sichere Verbindungen verhindert werden.

## Inhalt dieses Abschnitts


<a href="" id="configuring-certificates-to-support-secure-streaming"></a>[Konfigurieren von Zertifikaten zur Unterstützung von sicherem Streaming](configuring-certificates-to-support-secure-streaming.md)  
Enthält Informationen zum Abrufen, konfigurieren und Installieren von Zertifikaten zur Unterstützung von Secure Streaming.

<a href="" id="how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server"></a>[So ändern Sie Berechtigungen für private Schlüssel zur Unterstützung von Management Server oder Streaming Server](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)  
Stellt Prozeduren bereit, die Sie zum Ändern von Schlüsseln in Windows Server2003 und Windows Server2008 verwenden können.

<a href="" id="configuring-certificates-to-support-app-v-management-server-or-streaming-server"></a>[Konfigurieren von Zertifikaten zur Unterstützung von App-V Management Server oder Streaming Server](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)  
Enthält Informationen zum Konfigurieren von Zertifikaten für die App-V-Verwaltungs-oder Streaming-Server, einschließlich Informationen zum Konfigurieren von Zertifikaten für Netzwerklastenausgleich-Umgebungen.

 

 





