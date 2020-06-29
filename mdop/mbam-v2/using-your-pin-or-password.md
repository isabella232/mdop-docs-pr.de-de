---
title: Verwenden Ihrer PIN oder Ihres Kennworts
description: Verwenden Ihrer PIN oder Ihres Kennworts
author: dansimp
ms.assetid: 7fe2aef4-d3e0-49c8-877d-7fee13dc5b7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b8c4b894b8f3e14d2a5cfb39e744fa43874c6753
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810168"
---
# Verwenden Ihrer PIN oder Ihres Kennworts


BitLocker hilft Ihnen, Ihren Computer zu sichern, indem Sie eine persönliche Identifikationsnummer (PIN) oder ein Kennwort zum Entsperren der auf Ihrem Computer gespeicherten Informationen benötigen. Die PIN-oder Kennwortanforderungen werden von Ihrer Organisation festgesetzt und sind von der Art des zu verschlüsselten Laufwerks abhängig. Daten auf den verschlüsselten Laufwerken können nicht angezeigt werden, ohne die PIN oder das Kennwort einzugeben. Wenn Ihre Computer Hardware ein aktiviertes Trusted Platform Module (TPM) enthält, werden Sie vom TPM-Chip aufgefordert, Ihre PIN einzugeben, bevor Windows auf Ihrem Computer gestartet wird.

## Informationen zu ihrer BitLocker-PIN und-Kennwörter


Ihr Unternehmen gibt an, welche Komplexität für Ihre PIN oder Ihr Kennwort erforderlich ist. Diese Anforderungen für Ihre PIN oder Ihr Kennwort werden während des BitLocker-Setupvorgangs erläutert.

Das Kennwort wird verwendet, um Laufwerke auf dem Computer zu entsperren, die das Betriebssystem nicht enthalten. BitLocker fragt nach Ihrem Kennwort, nachdem die PIN während des Startvorgangs angefordert wurde. Jede BitLocker-geschützte Festplatte auf Ihrem Computer verfügt über ein eigenes eindeutiges Kennwort. Sie können ein geschütztes BitLocker-Laufwerk erst entsperren, wenn Sie Ihr Kennwort angeben.

**Hinweis**  Ihr Helpdesk kann Laufwerke so einrichten, dass Sie automatisch freigegeben werden. Dadurch ist es nicht mehr notwendig, eine PIN oder ein Kennwort anzugeben, um die Informationen auf den Laufwerken anzuzeigen.

 

## Entsperren Ihres Computers, wenn Sie Ihre PIN oder Ihr Kennwort vergessen haben


Wenn Sie Ihre PIN oder Ihr Kennwort vergessen haben, kann Ihnen Ihr Helpdesk beim Entsperren von BitLocker Protected Drives helfen. Wenn Sie ein mit BitLocker geschütztes Laufwerk entsperren möchten, wenden Sie sich an den Helpdesk, wenn Sie Hilfe benötigen.

**Entsperren Ihres Computers, wenn Sie Ihre PIN oder Ihr Kennwort vergessen haben**

1.  Wenn Sie sich mit Ihrem Helpdesk in Verbindung setzen, müssen Sie ihm die folgenden Informationen zur Verfügung stellen:

    -   Ihr Benutzername

    -   Ihre Domäne

    -   Die ersten acht Ziffern Ihrer Wiederherstellungsschlüssel-ID. Hierbei handelt es sich um einen 32-stelligen Code, der von BitLocker angezeigt wird, wenn Sie Ihre PIN oder Ihr Kennwort vergessen.

        -   Wenn Sie Ihre PIN vergessen haben, müssen Sie die ersten acht Ziffern der Wiederherstellungsschlüssel-ID eingeben, die in der BitLocker-Wiederherstellungskonsole angezeigt wird. Bei der BitLocker-Wiederherstellungskonsole handelt es sich um einen Windows-Pre-Windows-Bildschirm, der angezeigt wird, wenn Sie die richtige PIN nicht eingeben.

        -   Wenn Sie Ihr Kennwort vergessen haben, suchen Sie in der Control Panel-Anwendung für BitLocker-Verschlüsselungsoptionen nach der Wiederherstellungsschlüssel-ID. Wählen Sie **Laufwerk entsperren** aus, und klicken Sie dann auf **Ich kann mich nicht mehr an mein Kennwort erinnern**. Die BitLocker-Verschlüsselungsoptionen-Anwendung zeigt dann eine Wiederherstellungsschlüssel-ID an, die Sie dem Helpdesk zur Verfügung stellen.

2.  Sobald Ihr Helpdesk die erforderlichen Informationen erhält, erhalten Sie einen Wiederherstellungsschlüssel über das Telefon oder per e-Mail.

    -   Wenn Sie Ihre PIN vergessen haben, geben Sie den Wiederherstellungsschlüssel in der BitLocker-Wiederherstellungskonsole ein, um den Computer zu entsperren.

    -   Wenn Sie Ihr Kennwort vergessen haben, geben Sie den Wiederherstellungsschlüssel in der Systemsteuerungsanwendung für BitLocker-Verschlüsselungsoptionen an demselben Speicherort ein, an dem Sie die Wiederherstellungsschlüssel-ID zuvor gefunden haben. Dadurch wird die geschützte Festplatte freigegeben.

## Ändern Ihrer PIN oder Ihres Kennworts


Bevor Sie das Kennwort auf einem BitLocker-geschützten Laufwerk ändern können, müssen Sie das Laufwerk entsperren. Wenn das Laufwerk nicht entsperrt ist, wählen Sie **Laufwerk entsperren**aus, und geben Sie dann Ihr aktuelles Kennwort ein. Sobald das Laufwerk entriegelt ist, können Sie Ihr **Kennwort verwalten** auswählen, um Ihr aktuelles Kennwort zu ändern.

**So ändern Sie Ihre PIN oder Ihr Kennwort**

1.  Klicken Sie auf **Start**und dann auf **System**Steuerung. Die Systemsteuerung wird in einem neuen Fenster geöffnet.

2.  Wählen Sie **System und Sicherheit**aus, und wählen Sie dann **BitLocker-Verschlüsselungsoptionen**aus.

    -   Wenn Sie Ihre PIN ändern möchten, wählen Sie **Pin verwalten**aus. Geben Sie Ihre neue PIN in beide Felder ein, und wählen Sie **PIN zurücksetzen**aus.

    -   Wenn Sie Ihr Kennwort ändern möchten, wählen Sie **Kennwort verwalten**aus. Geben Sie Ihr neues Kennwort in beide Felder ein, und wählen Sie **Kennwort zurücksetzen**aus.

 

 





