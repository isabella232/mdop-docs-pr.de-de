---
title: Konfigurieren von Protokollierung und Ablaufverfolgung
description: Konfigurieren von Protokollierung und Ablaufverfolgung
author: dansimp
ms.assetid: 419231f9-e9db-4f91-a7cf-a0a73db25256
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa3dfa71edb25f6641ade595cd4469e846410ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807720"
---
# Konfigurieren von Protokollierung und Ablaufverfolgung


Sie können die optionale Protokollierung und Ablaufverfolgung für erweiterte Gruppenrichtlinienverwaltung (AGPM) mithilfe administrativer Vorlagen zentral konfigurieren.

Ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff), dem Benutzerkonto der genehmigenden Person, die das in diesen Verfahren verwendete Gruppenrichtlinienobjekt erstellt hat, oder ein Benutzerkonto mit den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung ist erforderlich, um diese Verfahren ausführen zu können. Darüber hinaus ist ein Benutzerkonto mit Zugriff auf den AGPM-Server erforderlich, um die Protokollierung auf dem AGPM-Server zu initiieren. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So konfigurieren Sie die Protokollierung und Ablaufverfolgung für AGPM**

1.  Bearbeiten Sie in der **Gruppenrichtlinien-Verwaltungskonsolen** Struktur ein GPO, das auf alle Gruppenrichtlinienadministratoren angewendet wird, für die Sie die Protokollierung und Ablaufverfolgung aktivieren möchten. (Weitere Informationen finden Sie unter [Bearbeiten eines Gruppenrichtlinienobjekts](editing-a-gpo.md).)

2.  Klicken Sie im **Gruppenrichtlinienobjekt-Editor**auf **Computer Konfiguration**, **Administrative Vorlagen**und **Windows-Komponenten**.

3.  Wenn **AGPM** nicht unter Windows- **Komponenten**aufgeführt ist:

    1.  Klicken Sie mit der rechten Maustaste auf **Administrative Vorlagen** , und klicken Sie auf **Vorlagen hinzufügen/entfernen**.

    2.  Klicken Sie auf **Hinzufügen**, wählen Sie **AGPM. ADMX** oder **AGPM. adm**aus, klicken Sie auf **Öffnen**und dann auf **Schließen**.

4.  Doppelklicken Sie unter **Windows-Komponenten**auf **AGPM**.

5.  Doppelklicken Sie im Detailbereich auf **AGPM-Protokollierung**.

6.  Klicken Sie im Fenster **AGPM-Protokollierungseigenschaften** auf **aktiviert**, und konfigurieren Sie die Detailebene, die in den Protokollen aufgezeichnet werden soll.

7.  Klicken Sie auf **OK**.

8.  Schließen Sie den **Gruppenrichtlinienobjekt-Editor**. (Weitere Informationen finden Sie unter [Bereitstellen eines GPO](deploy-a-gpo.md).) Nachdem die Gruppenrichtlinie aktualisiert wurde, müssen Sie den AGPM-Dienst neu starten, um mit der Protokollierung auf dem AGPM-Server zu beginnen. Gruppenrichtlinienadministratoren müssen die GPMC schließen und neu starten, um mit der Protokollierung auf ihren Computern zu beginnen.

    **Speicherort der Ablaufverfolgungsdatei**:

    -   Client:%localappdata%\\Microsoft\\AGPM\\agpm.log

    -   Server:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log

### Weitere Überlegungen

-   Sie müssen in der Lage sein, ein GPO zu bearbeiten und bereitzustellen, um die AGPM-Protokollierung und-Ablaufverfolgung konfigurieren zu können. Weitere Informationen finden Sie unter [Bearbeiten eines GPO](editing-a-gpo.md) und [Bereitstellen eines Gruppenrichtlinienobjekts](deploy-a-gpo.md) .

### Weitere Verweise

-   [Durchführen von AGPM-Administratoraufgaben](performing-agpm-administrator-tasks.md)

 

 





