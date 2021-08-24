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
ms.openlocfilehash: c95fab4b2b4f402df4ff0f82f2f346c9bd226e00
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910480"
---
# <a name="configuring-app-v-for-secure-administration"></a>Konfigurieren von App-V für die sichere Verwaltung


In einer Umgebung, in der das Sichern administrativer Vorgänge wichtig ist, ermöglicht App-V eine sichere Kommunikation zwischen dem App-V-Webverwaltungsdienst und der App-V-Verwaltungskonsole. Da der Verwaltungsdienst eine webbasierte Anwendung ist, muss die App-V-Verwaltungsserveranwendung auf dem Webserver gesichert werden, auf dem der Verwaltungsdienst gehostet wird. Wie in der folgenden Abbildung dargestellt, umfasst dieser Prozess die Verwendung von HTTPS für die Kommunikation und die Konfiguration des IIS-Servers, um nur Windows integrierte Authentifizierung zuzulassen.

![App-v-Webdienst-Netzwerkkonfiguration.](images/appvmgmtwebservice.gif)

Der App-V-Webverwaltungsdienst wird als webbasierte Anwendung auf IIS installiert. Damit der Webverwaltungsdienst sichere (SSL)-Verbindungen zwischen der App-V-Verwaltungskonsole und dem Webverwaltungsdienst unterstützt, müssen Sie den IIS-Server konfigurieren, auf dem der Webverwaltungsdienst installiert ist, und die App-V-Verwaltungskonsole konfigurieren.

## <a name="in-this-section"></a>Inhalt dieses Abschnitts


<a href="" id="configuring-certificates-to-support-the-app-v-web-management-service"></a>[Konfigurieren von Zertifikaten zur Unterstützung des App-V Web Management Service](configuring-certificates-to-support-the-app-v-web-management-service.md)  
Enthält hilfreiche Informationen zum Konfigurieren von Zertifikaten zur Unterstützung SSL-basierter Verbindungen, um die sichere Kommunikation für den App-V-Webverwaltungsdienst zu unterstützen.

<a href="" id="how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment"></a>[So installieren und konfigurieren Sie die App-V Management Console für eine sicherere Umgebung](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)  
Stellt ein schrittweises Verfahren zum Herstellen einer Verbindung mit einem App-V-Webverwaltungsdienst mithilfe einer sicheren Verbindung bereit.

 

 





