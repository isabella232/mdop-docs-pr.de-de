---
title: So konfigurieren Sie das Self-Service-Portal, wenn Clientcomputer nicht auf das Microsoft Content Delivery Network zugreifen können
description: So konfigurieren Sie das Self-Service-Portal, wenn Clientcomputer nicht auf das Microsoft Content Delivery Network zugreifen können
author: dansimp
ms.assetid: 90ee76db-9876-41b5-994a-118556d5ed3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ffce3dd023cb6ff9bd5cdb13ea789b348661de24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810588"
---
# So konfigurieren Sie das Self-Service-Portal, wenn Clientcomputer nicht auf das Microsoft Content Delivery Network zugreifen können


Befolgen Sie diese Anweisungen, wenn die Clientcomputer in Ihrer Organisation nicht auf das Microsoft AJAX Content Delivery Network (CDN) zugreifen können.

**Gründe für die Konfiguration:**

Ihre Clientcomputer benötigen Zugriff auf das CDN, wodurch dem Self-Service-Portal der erforderliche Zugriff auf bestimmte JavaScript-Dateien gewährt wird. Wenn Sie das Self-Service-Portal nicht konfigurieren, wenn Clientcomputer nicht auf CDN zugreifen können, werden nur der Firmenname und das Konto angezeigt, unter dem sich der Endbenutzer anmeldet. Es wird keine Fehlermeldung angezeigt.

**Hinweis**  In MBAM 2,5 SP1 sind die JavaScript-Dateien im Produkt enthalten, und Sie müssen die Anweisungen in diesem Abschnitt nicht befolgen, um den SSP so zu konfigurieren, dass Clients unterstützt werden, die nicht auf das Internet zugreifen können.

 

**Konfigurieren des Self-Service-Portals, wenn Clientcomputer nicht auf das CDN zugreifen können**

1. Laden Sie die folgenden JavaScript-Dateien aus dem CDN herunter:

   -   [jQuery-1.10.2.min.js](https://go.microsoft.com/fwlink/?LinkID=390515)

   -   [jQuery.validate.min.js](https://go.microsoft.com/fwlink/?LinkID=390516)

   -   [jQuery.validate.unobtrusive.min.js](https://go.microsoft.com/fwlink/?LinkID=390517)

2. Kopieren Sie die JavaScript-Dateien in das Verzeichnis **Skripts** des Self-Service-Portals. Dieses Verzeichnis befindet sich in <em> &lt; MBAM Self-Service-Installationsverzeichnis &gt; \\ </em> Self-Service Website\\Scripts.

3. Öffnen Sie Internet Informationsdienste (IIS)-Manager.

4. Erweitern Sie **Sites** &gt; **Microsoft BitLocker-Verwaltung und-Überwachung**, und markieren Sie **Selfservice**.

   **Hinweis:**  
   *Selfservice* ist der Name des virtuellen Standardverzeichnisses. Wenn Sie während der Konfiguration einen anderen Namen für dieses Verzeichnis gewählt haben, denken Sie daran, *Selfservice* in diesen Anweisungen durch den von Ihnen gewählten Namen zu ersetzen.

     

5. Doppelklicken Sie im mittleren Bereich auf **Anwendungseinstellungen**.

6. Bearbeiten Sie für jedes Element in der folgenden Liste die Anwendungseinstellungen, um auf den neuen Speicherort zu verweisen, indem Sie/ &lt; *virtuelles Verzeichnis* &gt; /durch/Selfservice/(oder einen beliebigen Namen, den Sie während der Konfiguration ausgewählt haben) ersetzen. Beispielsweise ist der Pfad des virtuellen Verzeichnisses mit/Selfservice/Scripts/jQuery-1.10.2.min.js vergleichbar.

   -   jQueryPath:/ &lt; *virtuelles Verzeichnis* &gt; /Scripts/jQuery-1.10.2.min.js

   -   jQueryValidatePath:/ &lt; *virtuelles Verzeichnis* &gt; /Scripts/jQuery.validate.min.js

   -   jQueryValidateUnobtrusivePath:/ &lt; *virtuelles Verzeichnis* &gt; /Scripts/jQuery.validate.unobtrusive.min.js



## Verwandte Themen


[So konfigurieren Sie die MBAM 2.5-Webanwendungen](how-to-configure-the-mbam-25-web-applications.md)

 

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





