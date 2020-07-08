---
title: Konfigurieren der AGPM-Server-Verbindung
description: Konfigurieren der AGPM-Server-Verbindung
author: dansimp
ms.assetid: 9a42b5bc-41be-44ef-a6e2-6f56e2cf1996
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 88182f0e79f1a8bcce53e0d50c014e8d4aa29286
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807696"
---
# Konfigurieren der AGPM-Server-Verbindung


Bei der erweiterten Gruppenrichtlinienverwaltung (AGPM) werden alle Versionen der einzelnen gesteuerten Gruppenrichtlinienobjekte in einem zentralen Archiv gespeichert, sodass Gruppenrichtlinienadministratoren Gruppenrichtlinienobjekte offline anzeigen und ändern können, ohne dass sich dies unmittelbar auf die bereitgestellte Version jedes GPO auswirkt.

Ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff), dem Benutzerkonto der genehmigenden Person, die das in diesen Verfahren verwendete Gruppenrichtlinienobjekt erstellt hat, oder ein Benutzerkonto mit den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung ist erforderlich, um diese Verfahren zum zentralen Konfigurieren von Archivierungsspeicher Orten für alle Gruppenrichtlinienadministratoren durchzuführen. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

## Konfigurieren der AGPM-Server Verbindung


Als AGPM-Administrator (Vollzugriff) können Sie sicherstellen, dass alle Gruppenrichtlinienadministratoren eine Verbindung mit dem gleichen AGPM-Server herstellen, indem Sie die Einstellung zentral konfigurieren. Wenn für Ihre Umgebung separate AGPM-Server für einige oder alle Domänen erforderlich sind, konfigurieren Sie diese zusätzlichen AGPM-Server als Ausnahmen von der Standardeinstellung. Wenn Sie keine AGPM-Serververbindungen zentral konfigurieren, muss jeder Gruppenrichtlinienadministrator den AGPM-Server manuell für die Anzeige für jede Domäne konfigurieren.

-   [Konfigurieren eines AGPM-Servers für alle Gruppenrichtlinienadministratoren](#bkmk-defaultarchiveloc)

-   [Konfigurieren zusätzlicher AGPM-Server für alle Gruppenrichtlinienadministratoren](#bkmk-additionalarchiveloc)

-   [Manuelles Konfigurieren eines AGPM-Servers für Ihr Konto](#bkmk-manuallyconfigurearchiveloc)

### <a href="" id="bkmk-defaultarchiveloc"></a>

**So konfigurieren Sie einen AGPM-Server für alle Gruppenrichtlinienadministratoren**

1.  Bearbeiten Sie in der **Gruppenrichtlinien-Verwaltungskonsolen** Struktur ein GPO, das auf alle Gruppenrichtlinienadministratoren angewendet wird. (Weitere Informationen finden Sie unter [Bearbeiten eines Gruppenrichtlinienobjekts](editing-a-gpo.md).)

2.  Klicken Sie im **Gruppenrichtlinienobjekt-Editor**auf **Benutzerkonfiguration**, **Administrative Vorlagen**und **Windows-Komponenten**.

3.  Wenn **AGPM** nicht unter Windows- **Komponenten**aufgeführt ist:

    1.  Klicken Sie mit der rechten Maustaste auf **Administrative Vorlagen** , und klicken Sie auf **Vorlagen hinzufügen/entfernen**.

    2.  Klicken Sie auf **Hinzufügen**, wählen Sie **AGPM. ADMX** oder **AGPM. adm**aus, klicken Sie auf **Öffnen**und dann auf **Schließen**.

4.  Doppelklicken Sie unter **Windows-Komponenten**auf **AGPM**.

5.  Doppelklicken Sie im Detailbereich auf **AGPM-Server (alle Domänen)**.

6.  Aktivieren Sie im **Eigenschaftenfenster AGPM-Server (alle Domänen)** das Kontrollkästchen **aktiviert** , und geben Sie den vollqualifizierten Computernamen und-Port ein (beispielsweise Server.contoso.com:4600).

7.  Klicken Sie auf **OK**. Wenn Sie keine weiteren AGPM-Server Verbindungen konfigurieren möchten, schließen Sie den **Gruppenrichtlinienobjekt-Editor** , und stellen Sie das Gruppenrichtlinienobjekt bereit. (Weitere Informationen finden Sie unter [Bereitstellen eines GPO](deploy-a-gpo.md).) Wenn die Gruppenrichtlinie aktualisiert wird, ist die AGPM-Server Verbindung für alle Gruppenrichtlinienadministratoren konfiguriert.

### <a href="" id="bkmk-additionalarchiveloc"></a>

**So konfigurieren Sie zusätzliche AGPM-Server für alle Gruppenrichtlinienadministratoren**

1.  Wenn keine AGPM-Serververbindung konfiguriert wurde, führen Sie die oben beschriebenen Schritte aus, um einen AGPM-Standardserver für alle Domänen zu konfigurieren.

2.  Zum Konfigurieren separater AGPM-Server für einige oder alle Domänen (Überschreiben des standardmäßigen AGPM-Servers) bearbeiten Sie in der **Gruppenrichtlinien-Verwaltungskonsolen** Struktur ein GPO, das auf alle Gruppenrichtlinienadministratoren angewendet wird. (Weitere Informationen finden Sie unter [Bearbeiten eines Gruppenrichtlinienobjekts](editing-a-gpo.md).)

3.  Doppelklicken Sie im **Gruppenrichtlinienobjekt-Editor**unter **Benutzerkonfiguration** auf **Administrative Vorlagen**, **Windows-Komponenten**und dann auf **AGPM**.

4.  Doppelklicken Sie im Detailbereich auf **AGPM-Server**.

5.  Aktivieren Sie im Fenster **AGPM-Server Eigenschaften** das Kontrollkästchen **aktiviert** , und klicken Sie auf **anzeigen**.

6.  Im Fenster " **Inhalte anzeigen** ":

    1.  Klicken Sie auf **Hinzufügen**.

    2.  Geben Sie unter **Wertname**den Namen der Domäne ein (beispielsweise Server1.contoso.com).

    3.  Geben Sie als **Wert**den Namen und den Port des AGPM-Servers ein, der für diese Domäne verwendet werden soll (beispielsweise Server2.contoso.com:4600), und klicken Sie dann auf **OK**. (Standardmäßig überwacht der AGPM-Dienst Port 4600. Informationen zum Verwenden eines anderen Ports finden Sie unter [Ändern des Ports, auf den der AGPM-Dienst lauscht](modify-the-port-on-which-the-agpm-service-listens.md).)

    4.  Wiederholen Sie diese Schritte für jede Domäne, die nicht den AGPM-Standard Server verwendet.

7.  Klicken Sie auf **OK** , um die Fenster **Inhalte anzeigen** und **AGPM-Server Eigenschaften** zu schließen.

8.  Schließen Sie den **Gruppenrichtlinienobjekt-Editor**. (Weitere Informationen finden Sie unter [Bereitstellen eines GPO](deploy-a-gpo.md).) Wenn die Gruppenrichtlinie aktualisiert wird, werden die neuen AGPM-Server Verbindungen für alle Gruppenrichtlinienadministratoren konfiguriert.

### <a href="" id="bkmk-manuallyconfigurearchiveloc"></a>

Wenn Sie die AGPM-Server Verbindung zentral konfiguriert haben, steht die Option manuell für alle Gruppenrichtlinienadministratoren nicht zur Verfügung.

**So konfigurieren Sie den AGPM-Server für die Anzeige für Ihr Konto manuell**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie im Detailbereich auf die Registerkarte **AGPM-Server** .

3.  Geben Sie den vollqualifizierten Computernamen für den AGPM-Server ein, der das Archiv verwaltet, das für diese Domäne verwendet wird (beispielsweise Server.contoso.com), und den Port, der vom AGPM-Dienst überwacht wird (standardmäßig Port 4600).

4.  Klicken Sie auf über **nehmen**, und klicken Sie dann zum bestätigen auf **Ja** .

### Weitere Überlegungen

-   Sie müssen in der Lage sein, ein GPO zu bearbeiten und bereitzustellen, um die Verfahren zum zentralen Konfigurieren von AGPM-Server Verbindungen für alle Gruppenrichtlinienadministratoren durchführen zu können. Weitere Informationen finden Sie unter [Bearbeiten eines GPO](editing-a-gpo.md) und [Bereitstellen eines Gruppenrichtlinienobjekts](deploy-a-gpo.md) .

-   Der ausgewählte AGPM-Server bestimmt, welche GPOs auf der Registerkarte **Inhalt** angezeigt werden und an welchem Speicherort die Einstellungen für die **Domänen Delegierungs** Einstellungen angewendet werden. Wenn Sie nicht zentral über die administrative Vorlage verwaltet werden, muss jeder Gruppenrichtlinienadministrator diese Einstellung so konfigurieren, dass er auf den AGPM-Server für die Domäne verweist.

-   Die Mitgliedschaft in der Gruppe Richtlinien-Ersteller-Besitzer sollte eingeschränkt sein, damit Sie nicht dazu verwendet wird, die Verwaltung des Zugriffs auf GPOs durch AGPM zu umgehen. (Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gruppenrichtlinienobjekte** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, klicken Sie auf **Delegierung**, und konfigurieren Sie dann die Einstellungen, um die Anforderungen Ihrer Organisation zu erfüllen.)

### Weitere Verweise

-   [Durchführen von AGPM-Administratoraufgaben](performing-agpm-administrator-tasks.md)

 

 





