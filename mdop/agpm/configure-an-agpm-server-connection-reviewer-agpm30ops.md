---
title: Konfigurieren einer AGPM-Server-Verbindung
description: Konfigurieren einer AGPM-Server-Verbindung
author: dansimp
ms.assetid: ae78dc74-111d-4509-b0a6-e8b8b451c22a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 50968d8b1b1eb5d464c6dbdb251354a9dc691d62
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807735"
---
# Konfigurieren einer AGPM-Server-Verbindung


Wenn Sie sicherstellen möchten, dass Sie mit dem richtigen zentralen Archiv verbunden sind, überprüfen Sie die Konfiguration der AGPM-Server Verbindung. Wenn ein AGPM-Administrator (Vollzugriff) für Sie keine AGPM-Server Verbindung konfiguriert hat, müssen Sie ihn manuell konfigurieren.

**So wählen Sie einen AGPM-Server aus**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie im Detailbereich auf die Registerkarte **AGPM-Server** :

    -   Wenn die Optionen auf der Registerkarte **AGPM-Server** nicht verfügbar sind, wurden Sie von einem AGPM-Administrator zentral konfiguriert.

    -   Wenn die Optionen auf der Registerkarte **AGPM-Server** verfügbar sind, geben Sie den vollqualifizierten Computernamen für den AGPM-Server (beispielsweise Server.contoso.com) und den Port ein, den der AGPM-Dienst überwacht (standardmäßig Port 4600). Klicken Sie auf über **nehmen**, und klicken Sie dann zum bestätigen auf **Ja** .

### Weitere Überlegungen

-   Die ausgewählten AGPM-Server legen fest, welche GPOs auf der Registerkarte **Inhalt** angezeigt werden und an welchem Speicherort die Einstellungen für die **Domänen Delegierungs** Einstellungen angewendet werden. Wenn Sie nicht zentral über die administrative Vorlage verwaltet werden, muss jeder Gruppenrichtlinienadministrator diese Einstellung so konfigurieren, dass er auf den AGPM-Server für die Domäne verweist.

### Weitere Verweise

-   [Durchführen von Editor-Aufgaben](performing-editor-tasks-agpm30ops.md)

-   [Durchführen der Aufgaben von genehmigenden Personen](performing-approver-tasks-agpm30ops.md)

-   [Durchführen von Prüferaufgaben](performing-reviewer-tasks-agpm30ops.md)

 

 





