---
title: Informationen zum Verwenden der Sequencer-Befehlszeile
description: Informationen zum Verwenden der Sequencer-Befehlszeile
author: dansimp
ms.assetid: 0fd5f81b-17f9-4065-bce2-8785e8aac7c7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: afb3fb8608c78a3b9237a80529a6c22d792661ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808092"
---
# Informationen zum Verwenden der Sequencer-Befehlszeile


Sie können die Befehlszeile verwenden, um sequenzierte Anwendungspakete zu erstellen. Die Verwendung der Befehlszeile zum Erstellen virtueller Anwendungen ist in den folgenden Szenarien hilfreich:

-   Sie müssen eine große Anzahl von sequenzierten Anwendungspaketen erstellen.

-   Sie müssen in regelmäßigen Abständen ein sequenziertes Anwendungspaket erstellen.

**Wichtig**  Die Sequenzierung an der Eingabeaufforderung ermöglicht nur die standardmäßige Sequenzierung. Wenn Sie die standardmäßigen Sequenz Parameter ändern müssen, müssen Sie entweder ein sequenziertes Anwendungspaket manuell ändern oder die Anwendung neu sequenzieren.

 

Alle nachfolgenden Änderungen an vorhandenen sequenzierten Anwendungspaketen müssen mithilfe des Sequenz-Assistenten erfolgen.

## Voraussetzungen


Um eine Anwendung mithilfe der Eingabeaufforderung zu sequenzieren, müssen die folgenden Bedingungen erfüllt sein:

-   Die zu sequenzierte Anwendung darf keine Änderungen oder Problemumgehungen erfordern, die außerhalb des Installationsprogramms oder des Windows Installer-Pakets vorgenommen wurden.

-   Vor der Sequenzierung müssen Sie eine Liste der Batchdateien zum Erstellen der sequenzierten Anwendungspakete vorbereiten.

-   Weitere Informationen zu den Befehlszeilenparametern finden Sie unter [Befehlszeilenparameter](command-line-parameters.md).

-   Überprüfen Sie die Fehler, die möglicherweise beim Erstellen eines sequenzierten Anwendungspakets über die Befehlszeile angezeigt werden. Weitere Informationen finden Sie unter diese Fehler finden Sie unter [Befehlszeilenfehler](command-line-errors.md).

## Verwandte Themen


[So verwalten Sie virtuellen Anwendungen über die Befehlszeile](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





