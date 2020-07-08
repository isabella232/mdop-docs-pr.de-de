---
title: Seite „Informationen zur Package Accelerator-Freigabe“
description: Seite „Informationen zur Package Accelerator-Freigabe“
author: dansimp
ms.assetid: 9630cde0-e2c3-476f-8fa1-58b3c9f7d3f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 34fe55d910a7532f011b239ff5b8162aa9240f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808128"
---
# Seite „Informationen zur Package Accelerator-Freigabe“


Die folgenden Informationen enthalten bewährte Methoden zum Freigeben von Paket Beschleunigern. Wenn Sie die Paket Beschleunigerdateien freigeben möchten, können Informationen wie Computernamen, Benutzerkontoinformationen und Informationen zu den in den Transformationen enthaltenen Anwendungen in der Paket Beschleunigerdatei enthalten sein. Überprüfen Sie alle Einstellungen oder Konfigurationsdateien, die dem virtuellen Anwendungspaket zugeordnet sind, um sicherzustellen, dass die Anwendungen keine persönlichen Informationen enthalten. Diese Seite enthält die folgenden Elemente.

-   **Benutzername**. Wenn Sie sich bei dem Computer anmelden, auf dem Microsoft App-V Sequencer ausgeführt wird, sollten Sie ein generisches Benutzerkonto verwenden, beispielsweise das integrierte **Administrator** Konto. Sie sollten kein Konto verwenden, das auf einem vorhandenen Benutzernamen basiert.

-   **Computer Name** Geben Sie einen allgemeinen, nicht identifizierbaren Namen des Computers an, auf dem der Sequencer ausgeführt wird.

-   **Server-URL**. Verwenden Sie in der App-V Sequencer-Konsole auf der Registerkarte **Bereitstellung** die Standardeinstellungen für die Konfigurationsinformationen der Server-URL.

-   **Anwendungen**. Wenn Sie die Liste der Anwendungen, die auf dem Computer installiert waren, auf dem der Sequencer ausgeführt wurde, beim Erstellen des Paket Beschleunigers nicht freigeben möchten, müssen Sie die **appv\_manifest.xml** -Datei löschen. Diese Datei befindet sich im Paketstammverzeichnis des virtuellen Anwendungspakets.

## Verwandte Themen


[Assistent „Package Accelerator erstellen“ (AppV 4.6 SP1)](create-package-accelerator-wizard--appv-46-sp1-.md)

[Informationen zu App-V Package Accelerators (App-V 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md)

 

 





