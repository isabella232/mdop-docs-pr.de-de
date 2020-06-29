---
title: Informationen zu App-V Package Accelerators (App-V 4.6 SP1)
description: Informationen zu App-V Package Accelerators (App-V 4.6 SP1)
author: manikadhiman
ms.assetid: fc2d2375-8f17-4a6d-b374-771cb947cb8c
ms.reviewer: ''
manager: dansimp
ms.author: v-madhi
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cb7b8e6fa9482838283257843caf4b291c03bf2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808168"
---
# Informationen zu App-V Package Accelerators (App-V 4.6 SP1)


Sie können App-V-Paket Beschleuniger verwenden, um große komplexe Anwendungen automatisch zu sequenzieren. Darüber hinaus müssen Sie beim Anwenden eines App-V-Paket Beschleunigers nicht immer eine Anwendung manuell installieren, um das virtuelle Anwendungspaket zu erstellen.

**Hinweis**  In einigen Fällen werden Sie aufgefordert, eine Anwendung lokal auf dem Computer zu installieren, auf dem der App-V-Sequencer ausgeführt wird, bevor Sie den Paket Beschleuniger verwenden können. Wenn Sie eine Anwendung installieren müssen, müssen Sie die Anwendung am Standardspeicherort der Anwendung installieren. Diese Installation wird nicht von App-V Sequencer überwacht. Wenn der App-V-Paket Beschleuniger erstellt wird, bestimmt der Autor des Paket Beschleunigers, ob eine Anwendung lokal installiert werden muss.

 

App-v Sequencer extrahiert die erforderlichen Dateien aus dem App-v-Paket Beschleuniger und zugehörigen Installationsmedien zum Erstellen eines virtuellen Pakets, ohne die Installation der Anwendung überwachen zu müssen.

**Wichtig**  Disclaimer: Microsoft Application Virtualization Sequencer gibt Ihnen keine Lizenzrechte für die Softwareanwendung, die Sie zum Erstellen eines Paket Beschleunigers verwenden. Sie müssen sich an alle Endnutzer-Lizenzbestimmungen für diese Anwendung halten. Sie müssen sicherstellen, dass die Lizenzbestimmungen der Softwareanwendung es Ihnen ermöglichen, mithilfe von Application Virtualization Sequencer einen Paket Beschleuniger zu erstellen.

 

App-V-Paket Beschleuniger und Projektvorlagen unterscheiden sich voneinander. Paket Beschleuniger sind anwendungsspezifisch. Projektvorlagen ermöglichen es Benutzern, häufig verwendete Einstellungen zu speichern, die für eine Organisation spezifisch sind, und Sie auf mehrere Anwendungen anzuwenden. Sie können auch an der Eingabeaufforderung Projektvorlagen erstellen, während Sie im Gegensatz dazu die App-V Sequencer-Konsole zum Erstellen von Paket Beschleunigern verwenden müssen. Darüber hinaus wird das Erstellen eines Pakets mithilfe eines Paket Beschleunigers und das Anwenden einer Projektvorlage nicht unterstützt.

## Freigeben von App-V-Paket Beschleunigern


Dieser Abschnitt enthält bewährte Methoden zum Freigeben von Paket Beschleunigern. Wenn Sie die Paket Beschleuniger freigeben möchten, können Informationen wie Computernamen, Benutzerkontoinformationen und Informationen zu den zugehörigen Anwendungen in den Paket Beschleunigern enthalten sein. in der folgenden Liste werden die Methoden beschrieben, die Sie beim Erstellen von Paket Beschleunigern berücksichtigen sollten:

-   **Benutzername**. Wenn Sie sich bei dem Computer anmelden, auf dem App-V Sequencer ausgeführt wird, sollten Sie ein generisches Benutzerkonto verwenden, beispielsweise das integrierte **Administrator** Konto für die Verwaltung des Computers/der Domäne. Sie sollten kein Konto verwenden, das auf einem vorhandenen Benutzernamen basiert.

-   **Computer Name** Geben Sie einen allgemeinen, nicht identifizierbaren Namen für den Computer an, auf dem der Sequencer ausgeführt wird.

-   **Server-URL**. Verwenden Sie in der Sequencer-Konsole auf der Registerkarte **Bereitstellung** die Standardeinstellungen für die Konfigurationsinformationen der Server-URL.

-   **Anwendungen**. Wenn Sie die Liste der Anwendungen, die auf dem Computer installiert waren, auf dem der Sequencer ausgeführt wurde, beim Erstellen des Paket Beschleunigers nicht freigeben möchten, müssen Sie die **appv\_manifest.xml** -Datei löschen. Diese Datei befindet sich im Paketstammverzeichnis des virtuellen Anwendungspakets.

Darüber hinaus sollten Sie alle Einstellungen oder Konfigurationsdateien überprüfen, die dem virtuellen Anwendungspaket zugeordnet sind, um sicherzustellen, dass die Anwendungen keine persönlichen Informationen enthalten.

## Sichern von App-V-Paket Beschleunigern


Sie können APP-v-Paket Beschleuniger und alle zugehörigen Installationsmedien immer an einem sicheren Ort im Netzwerk speichern, um die APP-v-Paket Beschleuniger und die Installationsdateien vor Manipulationen oder Beschädigungen zu schützen. Da Paket Beschleuniger auch Kennwort-und benutzerspezifische Informationen enthalten können, müssen Sie App-V-Paket Beschleuniger an einem sicheren Speicherort speichern, und Sie müssen den Paket Beschleuniger digital signieren, nachdem Sie ihn erstellt haben, damit der Herausgeber überprüft werden kann, wenn der Paket Beschleuniger angewendet wird. Weitere Informationen zu digitalen Signaturen finden Sie unter [Anwendungsrichtlinien für digitale Signatur Methoden für Common Criteria-Sicherheit](https://go.microsoft.com/fwlink/?LinkId=204705) ( https://go.microsoft.com/fwlink/?LinkId=204705) .

## Verwandte Themen


[So erstellen Sie App-V Package Accelerators (App-V 4.6 SP1)](how-to-create-app-v-package-accelerators--app-v-46-sp1-.md)

[Anwenden eines Paket Beschleunigers zum Erstellen eines virtuellen Anwendungspakets (App-V 4,6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)

 

 





