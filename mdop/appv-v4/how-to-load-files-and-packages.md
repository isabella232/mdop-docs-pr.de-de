---
title: So laden Sie Dateien und Pakete
description: So laden Sie Dateien und Pakete
author: dansimp
ms.assetid: f86f5bf1-99a4-44d7-ae2f-e6049c482f68
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9427fd8089ec9c22d7d379b15ae94bf421ca2d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807027"
---
# So laden Sie Dateien und Pakete


Mit dem folgenden Verfahren können Sie Dateien und Pakete auf Application Virtualization-Servern laden.

**Hinweis**  Während des Installationsvorgangs haben Sie den Speicherort des \\Content-Verzeichnisses auf der Seite " **Inhaltspfad** " angegeben. Dieses Verzeichnis sollte als Standarddateifreigabe erstellt und konfiguriert werden, bevor Sie auf den Speicherort verweisen.

 

**So laden Sie Dateien und Pakete**

1.  Navigieren Sie auf dem Computer, von dem aus Anwendungen gestreamt werden sollen, zu dem Speicherort, den Sie für das \\Content-Verzeichnis angegeben haben. Erstellen Sie bei Bedarf das Verzeichnis, und konfigurieren Sie es als Standarddateifreigabe.

2.  Verschieben Sie die SFT-Dateien für die virtuellen Anwendungen und Pakete in das \\Content-Verzeichnis. Um die SFT-Dateien zu organisieren und Verwirrung zu vermeiden, fügen Sie Anwendungen und Pakete in dedizierte Unterordner ein.

3.  Laden Sie die Anwendungen und Pakete entsprechend den Anforderungen Ihres Szenarios und ihrer Konfiguration unter Berücksichtigung der folgenden Bedingungen:

    -   Wenn Ihre Anwendungen und Pakete auf einem Application Virtualization (App-V)-Verwaltungs Server gespeichert sind, laden Sie Sie über die Verwaltungskonsole. Weitere Informationen finden Sie unter [so wird es gemacht: Laden oder Entladen einer Anwendung](how-to-load-or-unload-an-application.md) oder [Laden virtueller Anwendungen aus dem Desktop Benachrichtigungsbereich](how-to-load-virtual-applications-from-the-desktop-notification-area.md).

    -   Wenn Ihre Anwendungen auf einem App-V-Streamingserver, einem Webserver oder einem Computer gespeichert sind, der als Datei Server konfiguriert ist, können die Anwendungen automatisch geladen werden.

        **Hinweis**  Der App-V-Streamingserver Ruft das \\Content-Verzeichnis automatisch auf Anwendungen und Pakete ab und fügt diese Informationen in den Arbeitsspeicher für Dienst Anwendungsanforderungen ein.

        Die App-V-Clients müssen ordnungsgemäß konfiguriert sein, damit Anwendungen und Pakete von Webservern und Dateiservern abgerufen werden können. Weitere Informationen finden Sie unter [Konfigurieren des Clients für das Abrufen von Anwendungspaketen](how-to-configure-the-client-for-application-package-retrieval.md).

         

## Verwandte Themen


[Application Virtualization Server](application-virtualization-server.md)

 

 





