---
title: So verschieben Sie die MBAM 2.5-Websites
description: So verschieben Sie die MBAM 2.5-Websites
author: dansimp
ms.assetid: 71af9a54-c27b-408f-9d75-37c0d02e730e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa5bd8156810b3dccc1588b4dfd4cadd96fd22fb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811341"
---
# So verschieben Sie die MBAM 2.5-Websites


Gehen Sie wie folgt vor, um die folgenden MBAM-Websites von einem Computer auf einen anderen zu verschieben, um die folgenden Features von Server a auf Server B zu verschieben:

-   Website "Verwaltung und Überwachung"

-   Self-Service-Portal

**Wichtig**  Während der Konfiguration beider Websites müssen Sie die gleiche Verbindungszeichenfolge, die Berichts-URL, Gruppenkonten und das Webdienst-Anwendungspool-Domänenkonto als diejenigen angeben, die Sie aktuell verwenden. Wenn Sie nicht die gleichen Werte verwenden, können Sie nicht auf einige Server zugreifen. Verwenden Sie zum Abrufen der aktuellen Werte das Windows PowerShell-Cmdlet " **Get-MbamWebApplication** ".

 

**So verschieben Sie die Website "Verwaltung und Überwachung" auf einen anderen Server**

1.  Installieren Sie auf Server B die MBAM 2,5-Server Software. Anweisungen hierzu finden Sie unter [Installieren der MBAM 2,5-Server Software](installing-the-mbam-25-server-software.md).

2.  Starten Sie auf Server B den MBAM-Serverkonfigurations-Assistenten, klicken Sie auf **neue Features hinzufügen**, und wählen Sie dann nur das Feature **Website Verwaltung und Überwachung** aus.

    Alternativ können Sie das Windows PowerShell **-Cmdlet Enable-MbamWebApplication** verwenden, um die Website Verwaltung und Überwachung zu konfigurieren.

    Anweisungen zum Konfigurieren der Website "Verwaltung und Überwachung" finden Sie unter [Konfigurieren der MBAM 2,5-Webanwendungen](how-to-configure-the-mbam-25-web-applications.md).

**So verschieben Sie das Self-Service-Portal auf einen anderen Server**

1.  Installieren Sie auf Server B die MBAM 2,5-Server Software. Anweisungen hierzu finden Sie unter [Installieren der MBAM 2,5-Server Software](installing-the-mbam-25-server-software.md).

2.  Starten Sie auf Server B den MBAM-Serverkonfigurations-Assistenten, klicken Sie auf **neue Features hinzufügen**, und wählen Sie dann nur das **Self-Service-Portal-** Feature aus.

    Alternativ können Sie das Windows PowerShell **-Cmdlet Enable-MbamWebApplication** verwenden, um das Self-Service-Portal zu konfigurieren.

    Anweisungen zum Konfigurieren der Website "Verwaltung und Überwachung" finden Sie unter [Konfigurieren der MBAM 2,5-Webanwendungen](how-to-configure-the-mbam-25-web-applications.md).

3.  Wenn die Clientcomputer in Ihrer Organisation nicht auf das Microsoft Content Delivery Network zugreifen können, müssen Sie auch die JavaScript-Dateien verschieben. Weitere Informationen finden Sie unter [Konfigurieren des Self-Service-Portals, wenn Client Computer nicht auf das Microsoft Content Delivery Network zugreifen können](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md) .

4.  Passen Sie das Self-Service-Portal für Ihre Organisation an. Verwenden Sie die Anweisungen unter [Anpassen des Self-Service-Portals für Ihre Organisation](customizing-the-self-service-portal-for-your-organization.md) , um Ihre aktuellen Anpassungen zu überprüfen und benutzerdefinierte Einstellungen im Self-Server-Portal auf Server B zu konfigurieren.



## Verwandte Themen


[So konfigurieren Sie die MBAM 2.5-Webanwendungen](how-to-configure-the-mbam-25-web-applications.md)

[Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[Verschieben von MBAM 2.5-Funktionen auf einen anderen Server](moving-mbam-25-features-to-another-server.md)

 

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





