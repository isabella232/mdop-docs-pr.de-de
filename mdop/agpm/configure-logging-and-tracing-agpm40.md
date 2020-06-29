---
title: Konfigurieren von Protokollierung und Ablaufverfolgung
description: Konfigurieren von Protokollierung und Ablaufverfolgung
author: dansimp
ms.assetid: 2418cb6a-7189-4080-8fe2-9c8d47dec62c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bfc56d418ae83cbc5db24246bfac057305629df7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807719"
---
# Konfigurieren von Protokollierung und Ablaufverfolgung


Sie können die optionale Protokollierung und Ablaufverfolgung mithilfe administrativer Vorlagen zentral konfigurieren. Dies kann beim Diagnostizieren von Problemen im Zusammenhang mit der erweiterten Gruppenrichtlinienverwaltung (AGPM) hilfreich sein.

Ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff), dem Benutzerkonto der genehmigenden Person, die das in diesen Verfahren verwendete Gruppenrichtlinienobjekt (Group Policy Object, GPO) erstellt hat, oder ein Benutzerkonto mit den erforderlichen Berechtigungen in AGPM ist erforderlich, um diese Verfahren ausführen zu können. Darüber hinaus ist ein Benutzerkonto mit Zugriff auf den AGPM-Server erforderlich, um die Protokollierung auf dem AGPM-Server zu initiieren. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So konfigurieren Sie die Protokollierung und Ablaufverfolgung für AGPM**

1.  Bearbeiten Sie in der **Gruppenrichtlinien-Verwaltungskonsolen** Struktur ein GPO, das auf alle Gruppenrichtlinienadministratoren angewendet wird, für die Sie die Protokollierung und Ablaufverfolgung aktivieren möchten. (Weitere Informationen finden Sie unter [Bearbeiten eines Gruppenrichtlinienobjekts](editing-a-gpo-agpm40.md).)

2.  Klicken Sie im Fenster **Gruppenrichtlinien-Verwaltungs-Editor** auf **Computer Konfiguration**, **Richtlinien**, **Administrative Vorlagen**, **Windows-Komponenten**und **AGPM**.

3.  Doppelklicken Sie im Detailbereich auf **AGPM: Protokollierung konfigurieren**.

4.  Klicken Sie im **Eigenschaften** Fenster auf **aktiviert**, und konfigurieren Sie die Detailebene, die Sie in den Protokollen aufzeichnen möchten.

5.  Klicken Sie auf **OK**.

6.  Schließen Sie das Fenster **Gruppenrichtlinien-Verwaltungs-Editor** . (Weitere Informationen finden Sie unter [Bereitstellen eines GPO](deploy-a-gpo-agpm40.md).) Nachdem die Gruppenrichtlinien aktualisiert wurden, müssen Sie den AGPM-Dienst neu starten, um die Protokollierung auf dem AGPM-Server zu starten, zu ändern oder zu beenden. Gruppenrichtlinienadministratoren müssen die GPMC schließen und neu starten, um die Protokollierung auf ihren Computern zu starten, zu ändern oder zu beenden.

    **Speicherort der Ablaufverfolgungsdatei**:

    -   Client:%localappdata%\\Microsoft\\AGPM\\agpm.log

    -   Server:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log

### Weitere Überlegungen

-   Sie müssen in der Lage sein, ein GPO zu bearbeiten und bereitzustellen, um die AGPM-Protokollierung und-Ablaufverfolgung konfigurieren zu können. Weitere Informationen finden Sie unter [Bearbeiten eines GPO](editing-a-gpo-agpm40.md) und [Bereitstellen eines Gruppenrichtlinienobjekts](deploy-a-gpo-agpm40.md) .

### Weitere Verweise

-   [Konfigurieren von Advanced Group Policy Management](configuring-advanced-group-policy-management-agpm40.md)

 

 





