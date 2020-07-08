---
title: Konfigurieren von App-V für die sichere Verwaltung
description: Konfigurieren von App-V für die sichere Verwaltung
author: dansimp
ms.assetid: 4543fa81-c8cc-4b10-83b7-060778eb1349
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de70c1df734bbf1168fd7dacf9410d3451a8a3c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809034"
---
# Konfigurieren von App-V für die sichere Verwaltung


In einer Umgebung, in der es wichtig ist, administrative Vorgänge zu sichern, ermöglicht App-v die sichere Kommunikation zwischen dem App-v-Webverwaltungs Dienst und der APP-v-Verwaltungskonsole. Da es sich bei dem Verwaltungsdienst um eine webbasierte Anwendung handelt, muss die App-V-Verwaltungs Server Anwendung auf dem Webserver gesichert werden, der den Verwaltungsdienst hostet. Wie in der folgenden Abbildung dargestellt, umfasst dieser Prozess die Verwendung von HTTPS für die Kommunikation und die Konfiguration des IIS-Servers, um nur die integrierte Windows-Authentifizierung zu ermöglichen.

![App-v Web Service-Netzwerkkonfiguration](images/appvmgmtwebservice.gif)

Der App-V-Webverwaltungs Dienst wird als webbasierte Anwendung unter IIS installiert. Damit der Webverwaltungs Dienst sichere (SSL-) Verbindungen zwischen der APP-v-Verwaltungskonsole und dem Webverwaltungs Dienst unterstützt, müssen Sie den IIS-Server konfigurieren, auf dem der Webverwaltungs Dienst installiert ist, und die APP-v-Verwaltungskonsole konfigurieren.

## Inhalt dieses Abschnitts


<a href="" id="configuring-certificates-to-support-the-app-v-web-management-service"></a>[Konfigurieren von Zertifikaten zur Unterstützung des App-V Web Management Service](configuring-certificates-to-support-the-app-v-web-management-service.md)  
Bietet hilfreiche Informationen zum Konfigurieren von Zertifikaten zur Unterstützung von SSL-basierten Verbindungen, um die Kommunikation für den App-V Web Management Service zu sichern.

<a href="" id="how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment"></a>[So installieren und konfigurieren Sie die App-V Management Console für eine sicherere Umgebung](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)  
Bietet eine schrittweise Anleitung zum Herstellen einer Verbindung mit einem App-V-Webverwaltungs Dienst mithilfe einer sicheren Verbindung.

 

 





