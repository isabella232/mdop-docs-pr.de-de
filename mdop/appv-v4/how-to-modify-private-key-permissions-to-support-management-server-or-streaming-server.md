---
title: So ändern Sie Berechtigungen für private Schlüssel zur Unterstützung von Management Server oder Streaming Server
description: So ändern Sie Berechtigungen für private Schlüssel zur Unterstützung von Management Server oder Streaming Server
author: dansimp
ms.assetid: 1ebe86fa-0fbc-4512-aebc-0a5da991cd43
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e35c2df518f22ba81a070d2c40ad3862f376a6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806943"
---
# So ändern Sie Berechtigungen für private Schlüssel zur Unterstützung von Management Server oder Streaming Server


Um eine sicherere App-V-Installation zu unterstützen, können Sie die folgenden Verfahren verwenden, um private Schlüssel in Windows Server2003 oder Windows Server2008 zu ändern. Wenn Sie die Berechtigungen für den privaten Schlüssel ändern möchten, können Sie das Windows Server2003 Resource Kit-Tool verwenden `WinHttpCertCfg.exe` .

Für Windows Server2003 erfordert das Verfahren, dass ein Zertifikat, das die in diesem Dokument aufgeführten Voraussetzungen erfüllt, auf dem Computer installiert ist, auf dem Sie das App-V-Verwaltungs-oder Streamingserver installieren werden. Weitere Informationen zur Verwendung des `WinHttpCertCfg.exe` Tools finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=151981> .

In Windows Server2008 ist der Vorgang zum Ändern der ACLs für den privaten Schlüssel wesentlich einfacher. Die Benutzeroberfläche des Zertifikats kann zum Verwalten von Berechtigungen für den privaten Schlüssel verwendet werden.

**Hinweis**  Der Standardsicherheitskontext ist Netzwerkdienst; Stattdessen kann jedoch ein Domänenkonto verwendet werden.

 

**So verwalten Sie private Schlüssel in Windows Server2003**

1.  Geben Sie auf dem Computer, der zum App-V-Verwaltungs-oder Streamingserver wird, in der Eingabeaufforderung den folgenden Befehl ein, um die aktuellen Berechtigungen aufzulisten, die einem bestimmten Zertifikat zugewiesen sind:

    `winhttpcertcfg -l -c LOCAL_MACHINE\My -s Name_of_cert`

2.  Ändern Sie bei Bedarf die Berechtigungen des Zertifikats, um Lesezugriff auf den Sicherheitskontext zur Verfügung zu stellen, der für den Verwaltungs-oder Streamingdienst verwendet wird:

    `winhttpcertcfg -g -c LOCAL_MACHINE\My -s Name_of_cert -a NetworkService`

3.  Überprüfen Sie, ob der Sicherheitskontext ordnungsgemäß hinzugefügt wurde, indem Sie die Berechtigungen für das Zertifikat auflisten:

    `winhttpcertcfg –l –c LOCAL_MACHINE\My –s Name_of_cert`

**So verwalten Sie private Schlüssel in Windows Server2008**

1.  Erstellen Sie eine Microsoft Management Console (MMC) mit dem *Zertifikate* -Snap-in, das auf den Zertifikatspeicher des *lokalen Computers* ausgerichtet ist.

2.  Erweitern Sie die MMC, und wählen Sie **private Schlüssel verwalten**aus.

3.  Fügen Sie auf der Registerkarte **Sicherheit** das **Netzwerkdienst** Konto mit **Lese** Zugriff hinzu.

## Verwandte Themen


[Konfigurieren von Zertifikaten zur Unterstützung von App-V Management Server oder Streaming Server](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)

[Konfigurieren von Zertifikaten zur Unterstützung von sicherem Streaming](configuring-certificates-to-support-secure-streaming.md)

 

 





