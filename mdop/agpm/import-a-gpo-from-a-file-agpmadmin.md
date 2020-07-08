---
title: Importieren eines Gruppenrichtlinienobjekts aus einer Datei
description: Importieren eines Gruppenrichtlinienobjekts aus einer Datei
author: dansimp
ms.assetid: 2cbcda72-4de3-47ad-aaf8-4fc7341d5a00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 04819dacac8df73f0a61cace0dab8b9fa79b7307
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808432"
---
# Importieren eines Gruppenrichtlinienobjekts aus einer Datei


Wenn Sie ein AGPM-Administrator (Vollzugriff) sind und ein Gruppenrichtlinienobjekt (GPO) in eine CAB-Datei exportiert haben, können Sie in der erweiterten Gruppenrichtlinienverwaltung (AGPM) die Richtlinieneinstellungen aus diesem Gruppenrichtlinienobjekt in ein neues Gruppenrichtlinienobjekt oder in ein vorhandenes GPO in einer Domäne in einer anderen Gesamtstruktur importieren. Informationen zum Exportieren von GPO-Einstellungen in eine CAB-Datei finden Sie unter [Exportieren eines Gruppenrichtlinienobjekts in eine Datei](export-a-gpo-to-a-file.md).

Ein Benutzerkonto mit der Rolle "AGPM-Administrator" oder die erforderlichen Berechtigungen in AGPM sind erforderlich, um Richtlinieneinstellungen in ein neues gesteuertes Gruppenrichtlinienobjekt zu importieren. Ein Benutzerkonto mit der Rolle "Editor" oder "AGPM-Administrator" oder die erforderlichen Berechtigungen in AGPM sind erforderlich, um Richtlinieneinstellungen in ein vorhandenes Gruppenrichtlinienobjekt zu importieren. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

## Importieren von Richtlinieneinstellungen aus einer Datei


Wenn Sie Richtlinieneinstellungen aus einer Datei importieren, können Sie Sie in ein neues GPO oder ein vorhandenes Gruppenrichtlinienobjekt importieren. Wenn Sie jedoch Richtlinieneinstellungen in ein vorhandenes GPO importieren, werden alle darin enthaltenen Richtlinieneinstellungen ersetzt.

-   [Importieren von Richtlinieneinstellungen in ein neues gesteuertes Gruppenrichtlinienobjekt](#bkmk-new)

-   [Importieren von Richtlinieneinstellungen in ein vorhandenes Gruppenrichtlinienobjekt](#bkmk-existing)

### <a href="" id="bkmk-new"></a>

**So importieren Sie Richtlinieneinstellungen in ein neues gesteuertes Gruppenrichtlinienobjekt**

1.  Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsolen** Struktur in der Domäne, für die Sie Richtlinieneinstellungen importieren möchten, auf **Steuerelement ändern** .

2.  Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.

3.  Erstellen eines neuen kontrollierten Gruppenrichtlinienobjekts Klicken Sie im Dialogfeld **Neues gesteuertes GPO** auf **importieren** und dann auf **Start-Assistent**. Weitere Informationen zum Erstellen eines Gruppenrichtlinienobjekts finden Sie unter [Erstellen eines neuen kontrollierten Gruppenrichtlinienobjekts](create-a-new-controlled-gpo-agpm40.md).

4.  Befolgen Sie die Anweisungen im **Assistenten zum Importieren von Einstellungen** , um eine GPO-Sicherung auszuwählen, die Richtlinieneinstellungen für das neue GPO zu importieren, und geben Sie einen Kommentar für den Überwachungspfad des neuen Gruppenrichtlinienobjekts ein.

### <a href="" id="bkmk-existing"></a>

**So importieren Sie Richtlinieneinstellungen in ein vorhandenes Gruppenrichtlinienobjekt**

1.  Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsolen** Struktur in der Domäne, für die Sie Richtlinieneinstellungen importieren möchten, auf **Steuerelement ändern** .

2.  Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.

3.  Überprüfen Sie das Ziel-GPO, in das Sie Richtlinieneinstellungen importieren möchten.

4.  Klicken Sie mit der rechten Maustaste auf das Ziel-GPO, zeigen Sie auf **Importieren von**, und klicken Sie dann auf **Datei**.

5.  Befolgen Sie die Anweisungen im **Assistenten zum Importieren von Einstellungen** , um eine GPO-Sicherung auszuwählen, importieren Sie deren Richtlinieneinstellungen, um diese im Zielgruppen Richtlinienobjekt zu ersetzen, und geben Sie einen Kommentar für den Überwachungspfad des Zielgruppen Richtlinienobjekts ein. Standardmäßig ist das Ziel-GPO nach Abschluss des Assistenten eingecheckt.

### Weitere Überlegungen

-   Wenn Sie Richtlinieneinstellungen in ein neues gesteuertes Gruppenrichtlinienobjekt importieren möchten, müssen Sie über **Listeninhalt**, **Gruppenrichtlinienobjekt importieren**und Berechtigungen zum **Erstellen von Gruppenrichtlinienobjekten** für die Domäne verfügen. Standardmäßig müssen Sie ein AGPM-Administrator sein, um dieses Verfahren ausführen zu können.

-   Wenn Sie Richtlinieneinstellungen in ein vorhandenes Gruppenrichtlinienobjekt importieren möchten, müssen Sie über **Listeninhalt**, **Einstellungen zum Bearbeiten**und **Importieren von GPO** -Berechtigungen für die Domäne verfügen, und das Gruppenrichtlinienobjekt muss von Ihnen ausgecheckt werden. Standardmäßig müssen Sie ein Editor oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.

### Weitere Verweise

-   [Verwalten des Archivs](managing-the-archive-agpm40.md)

 

 





