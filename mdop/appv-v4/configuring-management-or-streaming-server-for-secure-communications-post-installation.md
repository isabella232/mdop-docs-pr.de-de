---
title: Konfigurieren von Management oder Streaming Server für die sichere Kommunikation nach der Installation
description: Konfigurieren von Management oder Streaming Server für die sichere Kommunikation nach der Installation
author: dansimp
ms.assetid: 1062a213-470b-4ae2-b12f-b3e28a6ab745
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a2713f130809c431b7444f3e928a523838597a6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809019"
---
# Konfigurieren von Management oder Streaming Server für die sichere Kommunikation nach der Installation


Wenn das richtige Zertifikat vor der Installation des App-v-Verwaltungsservers oder des App-v-Streaming-Servers nicht bereitgestellt wurde, kann App-v nach der ersten Installation für erhöhte Sicherheit konfiguriert werden. Sie können den App-v-Verwaltungs Server über die APP-v-Verwaltungskonsole konfigurieren. Der App-V-Streamingserver wird jedoch über die Registrierung verwaltet. In beiden Fällen muss das Zertifikat die richtige *Erweiterte Schlüsselverwendung* (EKU) für die Server Authentifizierung enthalten, und der Netzwerkdienst muss über Lesezugriff auf den privaten Schlüssel verfügen.

## Inhalt dieses Abschnitts


<a href="" id="how-to-configure-management-server-security-post-installation"></a>[So konfigurieren Sie Management Server Security-Nachinstallation](how-to-configure-management-server-security-post-installation.md)  
Bietet eine Prozedur, die nach der Installation mithilfe der APP-v-Verwaltungskonsole durchgeführt werden kann, um das Zertifikat hinzuzufügen und den App-v-Verwaltungs Server für erhöhte Sicherheit zu konfigurieren.

<a href="" id="how-to-configure-streaming-server-security-post-installation"></a>[So konfigurieren Sie die Streaming Server Security-Nachinstallation](how-to-configure-streaming-server-security-post-installation.md)  
Bietet eine Prozedur, die nach der Installation durchgeführt werden kann, um das Zertifikat hinzuzufügen und den App-V-Streamingserver für erhöhte Sicherheit zu konfigurieren.

<a href="" id="troubleshooting-certificate-permission-issues"></a>[Behandeln von Problemen mit Zertifikatberechtigungen](troubleshooting-certificate-permission-issues.md)  
Bietet Anleitungen zur Problembehandlung, wenn der private Schlüssel nicht mit der richtigen ACL für den Netzwerkdienst konfiguriert wurde.

 

 





