---
title: Seite „Package Accelerator auswählen“
description: Seite „Package Accelerator auswählen“
author: dansimp
ms.assetid: 865c2702-4dfd-41ae-8cfc-3514d5f41f76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5723f8244563539c27a3fa915c1a680905e61e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806368"
---
# Seite „Package Accelerator auswählen“


Auf der Seite **Paket Beschleuniger auswählen** können Sie den Paket Beschleuniger auswählen, der zum Erstellen des neuen virtuellen Anwendungspakets verwendet wird. Sie müssen den Paket Beschleuniger in einen Ordner auf dem Computer kopieren, auf dem der App-V-Sequencer ausgeführt wird. Weitere Informationen finden Sie unter [Informationen zu app-v-Paket Beschleunigern (app-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).

Führen Sie nur Paket Beschleuniger von Herausgebern aus, denen Sie vertrauen. Paket Beschleuniger beinhalten in der Regel eine digitale Signatur. Bei einer digitalen Signatur handelt es sich um ein elektronisches Sicherheitszeichen, das den Herausgeber der Software kennzeichnet und angibt, ob das Paket manipuliert wurde, nachdem die Transformation ursprünglich signiert wurde. Wenn Sie eine Transform-Datenbank verwenden, die von einem Verleger digital signiert wurde und der Herausgeber seine Identität bei einer Zertifizierungsstelle überprüft hat, können Sie sicher sein, dass die Transformation von diesem bestimmten Herausgeber stammt und nicht geändert wurde.

Der App-V-Sequenzer benachrichtigt Sie, wenn eine der folgenden Bedingungen zutrifft:

-   Die ausgewählte Transformation wurde nicht digital signiert.

-   Die ausgewählte Transformation wird von einem Verleger signiert, dessen Identität bei einer Zertifizierungsstelle nicht überprüft wurde.

-   Die ausgewählte Transformation wurde geändert, nachdem Sie digital signiert und freigegeben wurde.

Wenn eine dieser Nachrichten angezeigt wird, wenn Sie eine Paket Beschleuniger verwenden, besuchen Sie die Website des Paket Beschleunigers Publisher, um eine Digital signierte Version der Transformation abzurufen.

Diese Seite enthält die folgenden Elemente:

<a href="" id="browse"></a>**Durchsuchen**  
Klicken Sie auf **Durchsuchen** , um den Paket Beschleuniger anzugeben, den Sie zum Erstellen des virtuellen Anwendungspakets verwenden werden. Speichern Sie den von Ihnen festgelegten Paket Beschleuniger lokal auf dem Computer, auf dem der Sequencer ausgeführt wird.

## Verwandte Themen


[Sequencer-Assistent - Package Accelerator (AppV 4.6 SP1)](sequencer-wizard---package-accelerator--appv-46-sp1-.md)

 

 





