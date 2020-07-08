---
title: Versionshinweise für App-V 5.0
description: Versionshinweise für App-V 5.0
author: dansimp
ms.assetid: 68a6a5a1-4b3c-4c09-b00c-9ca4237695d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e49f6072d738b45afe25de24f2ee9a2d09d64a2e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804889"
---
# Versionshinweise für App-V 5.0


**Drücken Sie STRG + F, um nach einem bestimmten Problem in diesen Versionshinweisen zu suchen.**

Lesen Sie diese Versionshinweise gründlich, bevor Sie App-V 5,0 installieren.

Diese Versionshinweise enthalten Informationen, die erforderlich sind, um App-V 5,0 erfolgreich zu installieren. Die Anmerkungen zu dieser Version enthalten auch Informationen, die in der Produktdokumentation nicht zur Verfügung stehen. Wenn es einen Unterschied zwischen diesen Anmerkungen zu dieser Version und einer anderen App-V 5,0-Dokumentation gibt, sollte die neueste Änderung als autorisierend angesehen werden. Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.

## Informationen zur Produktdokumentation


Informationen zur APP-v 5,0-Dokumentation finden Sie auf der APP-v 5,0-Startseite auf der Microsoft TechNet-Website.

## Feedback geben


Wir sind an Ihrem Feedback zu App-V 5,0 interessiert. Sie können Ihr Feedback an senden <mdopdocs@microsoft.com> .

**Hinweis**  Diese e-Mail-Adresse ist kein Supportkanal, aber Ihr Feedback wird uns helfen, zukünftige Änderungen in unseren Dokumentations-und Produktversionen zu planen.

 

Die neuesten Informationen zu MDOP und weiteren Lernressourcen finden Sie auf der Seite [MDOP-Informationen](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Wenn Sie weitere Informationen zu neuen Updates oder Feedback geben möchten, folgen Sie uns auf [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) oder [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## Bekannte Probleme mit App-V 5,0


Dieser Abschnitt enthält Versionshinweise zu den bekannten Problemen mit App-V 5,0.

### Beim Verwenden von Server-PowerShell-Cmdlets kann das Hinzufügen von Paketen nicht beendet werden

Wenn Sie ein Paket mit PowerShell hinzufügen, gibt es keine Methode, um das Hinzufügen neuer Pakete zu beenden.

Problemumgehung: um das Hinzufügen von Paketen zu beenden, drücken Sie die **EINGABETASTE** , nachdem Sie das endgültige Paket hinzugefügt haben.

### <a href="" id="-------------app-v-5-0-client-rejects-packages-from-servers-whose-ssl-certificate-has-been-revoked"></a> App-V 5,0-Client lehnt Pakete von Servern ab, deren SSL-Zertifikat gesperrt wurde

Wenn das HTTPS-Protokoll verwendet wird, lehnt der App-V 5,0-Clientstandard mäßig Pakete von Servern ab, deren SSL-Zertifikat widerrufen wurde. Dieses Verhalten kann durch die Konfiguration deaktiviert werden, indem Sie die **VerifyCertificateRevocationList** -Einstellung ändern. Das Anwenden einer neuen Konfiguration für diese Einstellung wird erst wirksam, nachdem der App-V 5,0-Dienst neu gestartet wurde.

Problemumgehung: Starten Sie den App-V 5,0-Dienst erneut.

## Anmerkungen zu dieser Version Copyright-Informationen


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune und WindowsPowerShell sind Marken der Microsoft-Unternehmensgruppe. Alle anderen Marken sind Eigentum ihrer jeweiligen Eigentümer.








## Verwandte Themen


[Informationen zu App-V 5.0](about-app-v-50.md)

 

 





