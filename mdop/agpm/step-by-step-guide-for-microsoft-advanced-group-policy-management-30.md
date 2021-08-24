---
title: Schrittweise Anleitung für Microsoft Advanced Group Policy Management 3.0
description: Schrittweise Anleitung für Microsoft Advanced Group Policy Management 3.0
author: dansimp
ms.assetid: d067f465-d7c8-4f6d-b311-66b9b06874f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f3f31808be82ec07d63bd0a9a2a402c9d7b693ea
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910490"
---
# <a name="step-by-step-guide-for-microsoft-advanced-group-policy-management-30"></a>Schrittweise Anleitung für Microsoft Advanced Group Policy Management 3.0


In diesem schrittweisen Leitfaden werden erweiterte Techniken für die Gruppenrichtlinienverwaltung mithilfe der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) und der Microsoft Advanced Group Policy Management (AGPM) veranschaulicht. AGPM erhöht die Funktionen der Gruppenrichtlinien-Verwaltungskonsole und bietet Folgendes:

-   Standardrollen zum Delegieren von Berechtigungen zum Verwalten von Gruppenrichtlinienobjekten (Group Policy Objects, GPOs) an mehrere Gruppenrichtlinienadministratoren sowie die Möglichkeit, den Zugriff auf GRUPPENRICHTLINIENobjekte in der Produktionsumgebung zu delegieren.

-   Ein Archiv, mit dem Gruppenrichtlinienadministratoren Gruppenrichtlinienobjekte offline erstellen und ändern können, bevor sie in einer Produktionsumgebung bereitgestellt werden.

-   Die Möglichkeit, ein Rollback auf eine frühere Version eines Gruppenrichtlinienobjekts im Archiv durchzuführen und die Anzahl der im Archiv gespeicherten Versionen zu begrenzen.

-   Eincheck-/Auscheckfunktion für Gruppenrichtlinienobjekte, um sicherzustellen, dass Gruppenrichtlinienadministratoren die Arbeit der anderen nicht versehentlich überschreiben.

## <a name="agpm-scenario-overview"></a>Übersicht über das AGPM-Szenario


In diesem Szenario verwenden Sie ein separates Benutzerkonto für jede Rolle in AGPM, um zu veranschaulichen, wie Gruppenrichtlinien in einer Umgebung mit mehreren Gruppenrichtlinienadministratoren verwaltet werden können, die über unterschiedliche Berechtigungsstufen verfügen. Insbesondere führen Sie die folgenden Aufgaben aus:

-   Installieren Sie mithilfe eines Kontos, das Mitglied der Gruppe "Domänenadministratoren" ist, AGPM Server, und weisen Sie die AGPM-Administratorrolle einem Konto oder einer Gruppe zu.

-   Installieren Sie den AGPM-Client mithilfe von Konten, denen Sie AGPM-Rollen zuweisen.

-   Konfigurieren Sie mithilfe eines Kontos mit der AGPM-Administratorrolle AGPM, und delegieren Sie den Zugriff auf Gruppenrichtlinienobjekte, indem Sie anderen Konten Rollen zuweisen.

-   Fordern Sie unter Verwendung eines Kontos mit der Editorrolle die Erstellung eines Gruppenrichtlinienobjekts an, das Sie dann mithilfe eines Kontos mit der Rolle "Genehmigende Person" genehmigen. Überprüfen Sie mit dem Editor-Konto das Gruppenrichtlinienobjekt aus dem Archiv, bearbeiten Sie das Gruppenrichtlinienobjekt, checken Sie das Gruppenrichtlinienobjekt in das Archiv ein, und fordern Sie die Bereitstellung an.

-   Überprüfen Sie unter Verwendung eines Kontos mit der Rolle "Genehmigende Person" das Gruppenrichtlinienobjekt, und stellen Sie es in Ihrer Produktionsumgebung bereit.

-   Erstellen Sie unter Verwendung eines Kontos mit der Editorrolle eine Gruppenrichtlinienobjektvorlage, und verwenden Sie sie als Ausgangspunkt, um ein neues Gruppenrichtlinienobjekt zu erstellen.

-   Löschen und Wiederherstellen eines Gruppenrichtlinienobjekts mithilfe eines Kontos mit der Rolle "Genehmigende Person".

![Gruppenrichtlinienobjektentwicklungsprozess.](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <a name="requirements"></a>Anforderungen


Computer, auf denen Sie AGPM installieren möchten, müssen die folgenden Anforderungen erfüllen, und Sie müssen Konten für die Verwendung in diesem Szenario erstellen.

**Hinweis:**  
Wenn Sie AGPM 2.5 installiert haben und ein Upgrade von Windows Server® 2003 auf Windows Server 2008 oder Windows Vista durchführen® ohne installierte Service Packs auf Windows Vista mit Service Pack 1, müssen Sie das Betriebssystem aktualisieren, bevor Sie auf AGPM 3.0 aktualisieren können.

 

### <a name="agpm-server-requirements"></a>AGPM-Serveranforderungen

AGPM Server 3.0 erfordert Windows Server 2008 oder Windows Vista mit Service Pack 1 und der GPMC von Remote Server Administration Tools (RSAT) installiert. Sowohl 32-Bit- als auch 64-Bit-Versionen werden unterstützt.

Bevor Sie AGPM Server installieren, müssen Sie Mitglied der Gruppe "Domänenadministratoren" sein, und die folgenden Windows Features müssen vorhanden sein, sofern nicht anders angegeben:

-   GPMC

    -   Windows Server 2008: Die Gruppenrichtlinien-Verwaltungskonsole wird automatisch von AGPM installiert, wenn sie nicht vorhanden ist.

    -   Windows Vista: Sie müssen die GPMC von RSAT installieren, bevor Sie AGPM installieren. Weitere Informationen finden Sie unter <https://go.microsoft.com/fwlink/?LinkID=116179>.

-   .NET Framework 3.5

Die folgenden Windows Features sind für AGPM Server erforderlich und werden automatisch installiert, wenn sie nicht vorhanden sind:

-   WCF-Aktivierung; Nicht-HTTP-Aktivierung

-   Windows-Prozessaktivierungsdienst

    -   Prozessmodell

    -   .NET-Umgebung

    -   Konfigurations-APIs

### <a name="agpm-client-requirements"></a>AGPM-Clientanforderungen

AGPM Client 3.0 erfordert Windows Server 2008 oder Windows Vista mit Service Pack 1 und der GPMC von Remote Server Administration Tools (RSAT) installiert. Sowohl 32-Bit- als auch 64-Bit-Versionen werden unterstützt. AGPM-Client kann auf einem Computer mit AGPM-Server installiert werden.

Die folgenden Windows Features sind vom AGPM-Client erforderlich und werden automatisch installiert, wenn sie nicht vorhanden sind, sofern nicht anders angegeben:

-   GPMC

    -   Windows Server 2008: Die Gruppenrichtlinien-Verwaltungskonsole wird automatisch von AGPM installiert, wenn sie nicht vorhanden ist.

    -   Windows Vista: Sie müssen die GPMC von RSAT installieren, bevor Sie AGPM installieren. Weitere Informationen finden Sie unter <https://go.microsoft.com/fwlink/?LinkID=116179>.

-   .NET Framework 3.0

### <a name="scenario-requirements"></a>Szenarioanforderungen

Bevor Sie mit diesem Szenario beginnen, erstellen Sie vier Benutzerkonten. Während des Szenarios weisen Sie jedem dieser Konten eine der folgenden AGPM-Rollen zu: AGPM-Administrator (Vollzugriff), Genehmiger, Editor und Prüfer. Diese Konten müssen in der Lage sein, E-Mail-Nachrichten zu senden und zu empfangen. Weisen Sie den Konten mit den Rollen "AGPM-Administrator", "Genehmigende Person" und (optional) "Editor" die Berechtigung **"Verknüpfungs-GPOs"** zu.

**Hinweis:**  
**Die Berechtigung "Gruppenrichtlinienobjekte** verknüpfen" ist standardmäßig Mitgliedern von Domänenadministratoren und Enterprise Administratoren zugewiesen. Um zusätzlichen Benutzern oder Gruppen (z. B. Konten mit den Rollen AGPM-Administrator oder Genehmiger) die Berechtigung **"Verknüpfungs-GPOs"** zuzuweisen, klicken Sie auf den Knoten für die Domäne und dann auf die Registerkarte **"Delegierung",** wählen Sie **"Gruppenrichtlinienobjekte verknüpfen"** aus, klicken Sie auf **"Hinzufügen"** und wählen Sie Benutzer oder Gruppen aus, denen die Berechtigung zugewiesen werden soll.

 

## <a name="steps-for-installing-and-configuring-agpm"></a>Schritte zum Installieren und Konfigurieren von AGPM


Sie müssen die folgenden Schritte ausführen, um AGPM zu installieren und zu konfigurieren.

[Schritt 1: Installieren von AGPM Server](#bkmk-config1)

[Schritt 2: Installieren des AGPM-Clients](#bkmk-config2)

[Schritt 3: Konfigurieren einer AGPM-Serververbindung](#bkmk-config3)

[Schritt 4: Konfigurieren von E-Mail-Benachrichtigungen](#bkmk-config4)

[Schritt 5: Stellvertretungszugriff](#bkmk-config5)

### <a name="step-1-install-agpm-server"></a><a href="" id="bkmk-config1"></a>Schritt 1: Installieren von AGPM Server

In diesem Schritt installieren Sie AGPM Server auf dem Mitgliedsserver oder Domänencontroller, der den AGPM-Dienst ausführt, und konfigurieren das Archiv. Alle AGPM-Vorgänge werden über diesen Windows Dienst verwaltet und mit den Anmeldeinformationen des Diensts ausgeführt. Das von einem AGPM-Server verwaltete Archiv kann auf diesem Server oder auf einem anderen Server in derselben Gesamtstruktur gehostet werden.

**So installieren Sie AGPM-Server auf dem Computer, der den AGPM-Dienst hosten soll**

1.  Melden Sie sich mit einem Konto an, das Mitglied der Gruppe "Domänenadministratoren" ist.

2.  Starten Sie die Microsoft Desktop Optimization Pack-CD, und folgen Sie den Anweisungen auf dem Bildschirm, um **erweiterte Gruppenrichtlinienverwaltung – Server**auszuwählen.

3.  Klicken Sie im Dialogfeld **"Willkommen"** auf **"Weiter".**

4.  Akzeptieren Sie im Dialogfeld **Microsoft-Softwarelizenzbedingungen** die Bedingungen, und klicken Sie auf **"Weiter".**

5.  Wählen Sie im Dialogfeld **Anwendungspfad** einen Speicherort aus, an dem AGPM Server installiert werden soll. Der Computer, auf dem AGPM Server installiert ist, hostet den AGPM-Dienst und verwaltet das Archiv. Klicken Sie auf **Weiter**.

6.  Wählen Sie im Dialogfeld **Archivpfad** einen Speicherort für das Archiv relativ zum AGPM-Server aus. Der Archivpfad kann auf einen Ordner auf dem AGPM-Server oder an anderer Stelle verweisen. Sie sollten jedoch einen Speicherort mit genügend Speicherplatz auswählen, um alle gpOs und Verlaufsdaten zu speichern, die von diesem AGPM-Server verwaltet werden. Klicken Sie auf **Weiter**.

7.  Wählen Sie im Dialogfeld **AGPM-Dienstkonto** ein Dienstkonto aus, unter dem der AGPM-Dienst ausgeführt wird, und klicken Sie dann auf **"Weiter".**

8.  Wählen Sie im Dialogfeld **"Archivbesitzer"** ein Konto oder eine Gruppe aus, dem bzw. der die ROLLE AGPM-Administrator (Vollzugriff) anfänglich zugewiesen werden soll. Dieser AGPM-Administrator kann anderen Gruppenrichtlinienadministratoren AGPM-Rollen und -Berechtigungen zuweisen (einschließlich der Rolle des AGPM-Administrators). Wählen Sie für dieses Szenario das Konto aus, das in der ROLLE "AGPM-Administrator" verwendet werden soll. Klicken Sie auf **Weiter**.

9.  Geben Sie im Dialogfeld **"Portkonfiguration"** einen Port ein, auf den der AGPM-Dienst lauschen soll. Deaktivieren Sie das Kontrollkästchen **"Portausnahme zur Firewall hinzufügen"** nur dann, wenn Sie Portausnahmen manuell konfigurieren oder Regeln zum Konfigurieren von Portausnahmen verwenden. Klicken Sie auf **Weiter**.

10. Wählen Sie im Dialogfeld **"Sprachen"** eine oder mehrere Anzeigesprachen aus, die für AGPM Server installiert werden sollen.

11. Klicken Sie auf **"Installieren",** und klicken Sie dann auf **"Fertig stellen",** um den Setup-Assistenten zu beenden.

    **Achtung**  
    Ändern Sie die Einstellungen für den AGPM-Dienst nicht über **Administrative Tools** und **Dienste** im Betriebssystem. Dadurch kann verhindert werden, dass der AGPM-Dienst gestartet wird. Informationen zum Ändern von Einstellungen für den Dienst finden Sie in der Hilfe zur erweiterten Gruppenrichtlinienverwaltung.

     

### <a name="step-2-install-agpm-client"></a><a href="" id="bkmk-config2"></a>Schritt 2: Installieren des AGPM-Clients

Jeder Gruppenrichtlinienadministrator – jeder, der GPOs erstellt, bearbeitet, bereitstellt, überprüft oder löscht – muss den AGPM-Client auf Computern installiert haben, die zum Verwalten von Gruppenrichtlinienobjekten verwendet werden. Für dieses Szenario installieren Sie den AGPM-Client auf mindestens einem Computer. Sie müssen den AGPM-Client nicht auf den Computern von Endbenutzern installieren, die keine Gruppenrichtlinienverwaltung ausführen.

**So installieren Sie den AGPM-Client auf dem Computer eines Gruppenrichtlinienadministrators**

1.  Starten Sie die Microsoft Desktop Optimization Pack-CD, und folgen Sie den Anweisungen auf dem Bildschirm, um **erweiterte Gruppenrichtlinienverwaltung – Client**auszuwählen.

2.  Klicken Sie im Dialogfeld **"Willkommen"** auf **"Weiter".**

3.  Akzeptieren Sie im Dialogfeld **Microsoft-Softwarelizenzbedingungen** die Bedingungen, und klicken Sie auf **"Weiter".**

4.  Wählen Sie im Dialogfeld **Anwendungspfad** einen Speicherort aus, an dem AGPM-Client installiert werden soll. Klicken Sie auf **Weiter**.

5.  Geben Sie im Dialogfeld **AGPM Server** den vollqualifizierten Computernamen für den AGPM-Server und den Port ein, mit dem eine Verbindung hergestellt werden soll. Der Standardport für den AGPM-Dienst ist 4600. Deaktivieren Sie das Kontrollkästchen **"Microsoft Management Console zulassen"** nicht über die Firewall, es sei denn, Sie konfigurieren Portausnahmen manuell oder verwenden Regeln zum Konfigurieren von Portausnahmen. Klicken Sie auf **Weiter**.

6.  Wählen Sie im Dialogfeld **"Sprachen"** eine oder mehrere Anzeigesprachen aus, die für den AGPM-Client installiert werden sollen.

7.  Klicken Sie auf **"Installieren",** und klicken Sie dann auf **"Fertig stellen",** um den Setup-Assistenten zu beenden.

### <a name="step-3-configure-an-agpm-server-connection"></a><a href="" id="bkmk-config3"></a>Schritt 3: Konfigurieren einer AGPM-Serververbindung

AGPM speichert alle Versionen jedes gesteuerten Gruppenrichtlinienobjekts (GPO) – ein Gruppenrichtlinienobjekt, für das AGPM die Änderungskontrolle bereitstellt – in einem zentralen Archiv, sodass Gruppenrichtlinienadministratoren Gruppenrichtlinienobjekte offline anzeigen und ändern können, ohne sofort die bereitgestellte Version jedes Gruppenrichtlinienobjekts zu beeinträchtigen.

In diesem Schritt konfigurieren Sie eine AGPM-Serververbindung und stellen sicher, dass alle Gruppenrichtlinienadministratoren eine Verbindung mit demselben AGPM-Server herstellen. (Informationen zum Konfigurieren mehrerer AGPM-Server finden Sie in der Hilfe zur erweiterten Gruppenrichtlinienverwaltung.)

**So konfigurieren Sie eine AGPM-Serververbindung für alle Gruppenrichtlinienadministratoren**

1.  Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit dem Benutzerkonto an, das Sie als Archivbesitzer ausgewählt haben. Dieser Benutzer hat die Rolle des AGPM-Administrators (Vollzugriff).

2.  Klicken Sie auf **"Start",** zeigen Sie auf **"Verwaltungstools",** und klicken Sie auf **"Gruppenrichtlinienverwaltung",** um die Gruppenrichtlinien-Verwaltungskonsole zu öffnen.

3.  Bearbeiten Sie ein Gruppenrichtlinienobjekt, das auf alle Gruppenrichtlinienadministratoren angewendet wird.

4.  Doppelklicken Sie im Fenster **"Gruppenrichtlinienverwaltungs-Editor"** auf **"Benutzerkonfiguration",** **"Richtlinien",** **"Administrative** **Vorlagen", "Windows Komponenten"** und **"AGPM".**

5.  Doppelklicken Sie im Detailbereich auf **AGPM: Geben Sie den Standard-AGPM-Server (alle Domänen) an.**

6.  Wählen Sie **im** Eigenschaftenfenster **"Aktiviert"** aus, und geben Sie den vollqualifizierten Computernamen und Port (z. **B. server.contoso.com:4600)** für den Server ein, auf dem das Archiv gehostet wird. Standardmäßig verwendet der AGPM-Dienst Port 4600.

7.  Klicken Sie auf **"OK",** und schließen Sie dann das Fenster **"Gruppenrichtlinienverwaltungs-Editor".** Wenn die Gruppenrichtlinie aktualisiert wird, wird die AGPM-Serververbindung für jeden Gruppenrichtlinienadministrator konfiguriert.

### <a name="step-4-configure-e-mail-notification"></a><a href="" id="bkmk-config4"></a>Schritt 4: Konfigurieren von E-Mail-Benachrichtigungen

Als AGPM-Administrator (Vollzugriff) bestimmen Sie die E-Mail-Adressen von Genehmigern und AGPM-Administratoren, an die eine E-Mail-Nachricht mit einer Anforderung gesendet wird, wenn ein Editor versucht, ein Gruppenrichtlinienobjekt zu erstellen, bereitzustellen oder zu löschen. Außerdem bestimmen Sie den Alias, von dem diese Nachrichten gesendet werden.

**So konfigurieren Sie E-Mail-Benachrichtigungen für AGPM**

1.  Klicken Sie im Detailbereich auf die Registerkarte **"Domänendelegierung".**

2.  Geben Sie im Feld **"Von"-E-Mail-Adresse** den E-Mail-Alias für AGPM ein, von dem Benachrichtigungen gesendet werden sollen.

3.  Geben Sie im Feld **"An E-Mail-Adresse"** die E-Mail-Adresse für das Benutzerkonto ein, dem Sie die Rolle "Genehmigende Person" zuweisen möchten.

4.  Geben Sie im **SMTP-Serverfeld** einen gültigen SMTP-E-Mail-Server ein.

5.  Geben Sie in die Felder **"Benutzername"** und **"Kennwort"** die Anmeldeinformationen eines Benutzers mit Zugriff auf den SMTP-Dienst ein. Klicken Sie auf **Übernehmen**.

### <a name="step-5-delegate-access"></a><a href="" id="bkmk-config5"></a>Schritt 5: Stellvertretungszugriff

Als AGPM-Administrator (Vollzugriff) delegieren Sie den Zugriff auf Domänenebene an GPOs und weisen dem Konto jedes Gruppenrichtlinienadministrators Rollen zu.

**Hinweis:**  
Sie können den Zugriff auch auf GPO-Ebene und nicht auf Domänenebene delegieren. Ausführliche Informationen finden Sie in der Hilfe zur erweiterten Gruppenrichtlinienverwaltung.

 

**Wichtig**  
Sie sollten die Mitgliedschaft in der Gruppe "Ersteller von Gruppenrichtlinienbesitzern" einschränken, damit sie nicht verwendet werden kann, um die AGPM-Verwaltung des Zugriffs auf Gruppenrichtlinienobjekte zu umgehen. (Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **"Gruppenrichtlinienobjekte"** in der Gesamtstruktur und Domäne, in der Gruppenrichtlinienobjekte verwaltet werden sollen, klicken Sie auf **"Delegierung",** und konfigurieren Sie dann die Einstellungen, um die Anforderungen Ihrer Organisation zu erfüllen.)

 

**So delegieren Sie den Zugriff auf alle GRUPPENrichtlinienobjekte in einer Domäne**

1.  Klicken Sie auf der Registerkarte **"Domänendelegierung"** auf die Schaltfläche **"Hinzufügen",** wählen Sie das Benutzerkonto des Gruppenrichtlinienadministrators aus, der als Genehmiger fungiert, und klicken Sie dann auf **"OK".**

2.  Wählen Sie im Dialogfeld **"Gruppe oder Benutzer hinzufügen"** die Rolle **"Genehmigende Person"** aus, um diese Rolle dem Konto zuzuweisen, und klicken Sie dann auf **"OK".** (Diese Rolle umfasst die Rolle "Prüfer".)

3.  Klicken Sie auf die Schaltfläche **"Hinzufügen",** wählen Sie das Benutzerkonto des Gruppenrichtlinienadministrators aus, der als Editor dienen soll, und klicken Sie dann auf **"OK".**

4.  Wählen Sie im Dialogfeld **"Gruppe oder Benutzer hinzufügen"** die **Editorrolle** aus, um diese Rolle dem Konto zuzuweisen, und klicken Sie dann auf **"OK".** (Diese Rolle umfasst die Rolle "Prüfer".)

5.  Klicken Sie auf die Schaltfläche **"Hinzufügen",** wählen Sie das Benutzerkonto des Gruppenrichtlinienadministrators aus, der als Prüfer fungieren soll, und klicken Sie dann auf **"OK".**

6.  Wählen Sie im Dialogfeld **"Gruppe oder Benutzer hinzufügen"** die Rolle **"Prüfer"** aus, um dem Konto nur diese Rolle zuzuweisen.

## <a name="steps-for-managing-gpos"></a>Schritte zum Verwalten von Gruppenrichtlinienobjekten


Sie müssen die folgenden Schritte ausführen, um GRUPPENrichtlinienobjekte mit AGPM zu erstellen, zu bearbeiten, zu überprüfen und bereitzustellen. Darüber hinaus erstellen Sie eine Vorlage, löschen ein Gruppenrichtlinienobjekt und stellen ein gelöschtes Gruppenrichtlinienobjekt wieder her.

[Schritt 1: Erstellen eines Gruppenrichtlinienobjekts](#bkmk-manage1)

[Schritt 2: Bearbeiten eines Gruppenrichtlinienobjekts](#bkmk-manage2)

[Schritt 3: Überprüfen und Bereitstellen eines Gruppenrichtlinienobjekts](#bkmk-manage3)

[Schritt 4: Verwenden einer Vorlage zum Erstellen eines Gruppenrichtlinienobjekts](#bkmk-manage4)

[Schritt 5: Löschen und Wiederherstellen eines Gruppenrichtlinienobjekts](#bkmk-manage5)

### <a name="step-1-create-a-gpo"></a><a href="" id="bkmk-manage1"></a>Schritt 1: Erstellen eines Gruppenrichtlinienobjekts

In einer Umgebung mit mehreren Gruppenrichtlinienadministratoren können Diejenigen mit der Editorrolle die Erstellung neuer Gruppenrichtlinienobjekte anfordern, aber eine solche Anforderung muss von einer Person mit der Rolle "Genehmigende Person" genehmigt werden, da sich die Erstellung eines neuen Gruppenrichtlinienobjekts auf die Produktionsumgebung auswirkt.

In diesem Schritt verwenden Sie ein Konto mit der Editorrolle, um die Erstellung eines neuen Gruppenrichtlinienobjekts anzufordern. Mithilfe eines Kontos mit der Rolle "Genehmigende Person" genehmigen Sie diese Anforderung und schließen die Erstellung eines Gruppenrichtlinienobjekts ab.

**So fordern Sie die Erstellung eines neuen gruppenrichtlinienobjekts an, das über AGPM verwaltet wird**

1.  Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Editorrolle in AGPM zugewiesen wurde.

2.  Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsolenstruktur** in der Gesamtstruktur und Domäne, in der Gruppenrichtlinienobjekte verwaltet werden sollen, auf **"Steuerelement ändern".**

3.  Klicken Sie mit der rechten Maustaste auf den Knoten **"Änderungssteuerung",** und klicken Sie dann auf **"Neues kontrolliertes Gruppenrichtlinienobjekt".**

4.  Im Dialogfeld **"Neues kontrolliertes** Gruppenrichtlinienobjekt":

    1.  Um eine Kopie der Anforderung zu erhalten, geben Sie Ihre E-Mail-Adresse in das **Feld "Cc"** ein.

    2.  Geben Sie **"MyGPO"** als Namen für das neue Gruppenrichtlinienobjekt ein.

    3.  Geben Sie einen Kommentar für das neue Gruppenrichtlinienobjekt ein.

    4.  Klicken Sie auf **"Live erstellen",** damit das neue Gruppenrichtlinienobjekt unmittelbar nach der Genehmigung in der Produktionsumgebung bereitgestellt wird. Klicken Sie auf **Übermitteln**.

5.  Wenn das **Fenster "AGPM-Fortschritt"** angibt, dass der gesamtfortschritt abgeschlossen ist, klicken Sie auf **"Schließen".** Das neue Gruppenrichtlinienobjekt wird auf der Registerkarte **"Ausstehend"** angezeigt.

**So genehmigen Sie die ausstehende Anforderung zum Erstellen eines Gruppenrichtlinienobjekts**

1.  Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle des Genehmigers in AGPM zugewiesen wurde.

2.  Öffnen Sie den E-Mail-Posteingang für das Konto, und beachten Sie, dass Sie eine E-Mail-Nachricht vom AGPM-Alias mit der Anforderung des Editors zum Erstellen eines Gruppenrichtlinienobjekts erhalten haben.

3.  Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsolenstruktur** in der Gesamtstruktur und Domäne, in der Gruppenrichtlinienobjekte verwaltet werden sollen, auf **"Steuerelement ändern".**

4.  Klicken Sie auf der Registerkarte **"Inhalt"** auf die Registerkarte **"Ausstehend",** um die ausstehenden Gruppenrichtlinienobjekte anzuzeigen.

5.  Klicken Sie mit der rechten Maustaste auf **"MyGPO",** und klicken Sie dann auf **"Genehmigen".**

6.  Klicken Sie auf **"Ja",** um die Genehmigung der Erstellung des Gruppenrichtlinienobjekts zu bestätigen. Das Gruppenrichtlinienobjekt wird auf die Registerkarte **"Kontrolliert"** verschoben.

### <a name="step-2-edit-a-gpo"></a><a href="" id="bkmk-manage2"></a>Schritt 2: Bearbeiten eines Gruppenrichtlinienobjekts

Sie können Gruppenrichtlinienobjekte verwenden, um Computer- oder Benutzereinstellungen zu konfigurieren und sie auf vielen Computern oder Benutzern bereitzustellen. In diesem Schritt verwenden Sie ein Konto mit der Editorrolle, um ein Gruppenrichtlinienobjekt aus dem Archiv auszuchecken, das Gruppenrichtlinienobjekt offline zu bearbeiten, das bearbeitete Gruppenrichtlinienobjekt im Archiv zu überprüfen und die Bereitstellung des Gruppenrichtlinienobjekts in der Produktionsumgebung anzufordern. Für dieses Szenario konfigurieren Sie eine Einstellung im Gruppenrichtlinienobjekt so, dass das Kennwort mindestens acht Zeichen lang sein muss.

**So checken Sie das Gruppenrichtlinienobjekt aus dem Archiv zur Bearbeitung aus**

1.  Melden Sie sich auf einem Computer, auf dem Sie agpm-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle des Editors in AGPM zugewiesen wurde.

2.  Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsolenstruktur** in der Gesamtstruktur und Domäne, in der Gruppenrichtlinienobjekte verwaltet werden sollen, auf **"Steuerelement ändern".**

3.  Klicken Sie auf der Registerkarte **"Inhalt"** im Detailbereich auf die Registerkarte **"Gesteuert",** um die gesteuerten Gruppenrichtlinienobjekte anzuzeigen.

4.  Klicken Sie mit der rechten Maustaste auf **"MyGPO",** und klicken Sie dann auf **"Auschecken".**

5.  Geben Sie einen Kommentar ein, der während des Auscheckens im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **OK.**

6.  Wenn das **Fenster "AGPM-Fortschritt"** angibt, dass der gesamtfortschritt abgeschlossen ist, klicken Sie auf **"Schließen".** Auf der Registerkarte **"Kontrolliert"** wird der Status des Gruppenrichtlinienobjekts als **ausgecheckt**identifiziert.

**So bearbeiten Sie das Gruppenrichtlinienobjekt offline und konfigurieren die minimale Kennwortlänge**

1.  Klicken Sie auf der Registerkarte **"Kontrolliert"** mit der rechten Maustaste auf **"MyGPO",** und klicken Sie dann auf **"Bearbeiten",** um das Fenster **"Gruppenrichtlinienverwaltungs-Editor"** zu öffnen und Änderungen an einer Offlinekopie des Gruppenrichtlinienobjekts vorzunehmen. Konfigurieren Sie für dieses Szenario die mindeste Kennwortlänge:

    1.  Doppelklicken Sie unter **"Computerkonfiguration"** auf **"Richtlinien",** **"Windows Einstellungen",** **"Sicherheit Einstellungen",** **"Kontorichtlinien"** und **"Kennwortrichtlinie".**

    2.  Doppelklicken Sie im Detailbereich auf **die Mindestlänge des Kennworts.**

    3.  Aktivieren Sie im Eigenschaftenfenster das Kontrollkästchen **"Diese Richtlinieneinstellung definieren",** legen Sie die Anzahl der Zeichen auf **8**fest, und klicken Sie dann auf **"OK".**

2.  Schließen Sie das Fenster **"Gruppenrichtlinienverwaltungs-Editor".**

**So checken Sie das Gruppenrichtlinienobjekt in das Archiv ein**

1.  Klicken Sie auf der Registerkarte **"Kontrolliert"** mit der rechten Maustaste auf **"MyGPO",** und klicken Sie dann auf **"Einchecken".**

2.  Geben Sie einen Kommentar ein, und klicken Sie dann auf **"OK".**

3.  Wenn das **Fenster "AGPM-Fortschritt"** angibt, dass der gesamtfortschritt abgeschlossen ist, klicken Sie auf **"Schließen".** Auf der Registerkarte **"Kontrolliert"** wird der Status des Gruppenrichtlinienobjekts als **eingecheckt**identifiziert.

**So fordern Sie die Bereitstellung des Gruppenrichtlinienobjekts in der Produktionsumgebung an**

1.  Klicken Sie auf der Registerkarte **"Kontrolliert"** mit der rechten Maustaste auf **"MyGPO",** und klicken Sie dann auf **"Bereitstellen".**

2.  Da dieses Konto kein Genehmiger oder AGPM-Administrator ist, müssen Sie eine Bereitstellungsanforderung senden. Um eine Kopie der Anforderung zu erhalten, geben Sie Ihre E-Mail-Adresse in das **Feld "Cc"** ein. Geben Sie einen Kommentar ein, der im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **"Absenden".**

3.  Wenn das **Fenster "AGPM-Fortschritt"** angibt, dass der gesamtfortschritt abgeschlossen ist, klicken Sie auf **"Schließen".** **MyGPO** wird in der Liste der GPOs auf der Registerkarte **"Ausstehend"** angezeigt.

### <a name="step-3-review-and-deploy-a-gpo"></a><a href="" id="bkmk-manage3"></a>Schritt 3: Überprüfen und Bereitstellen eines Gruppenrichtlinienobjekts

In diesem Schritt fungieren Sie als Genehmiger, erstellen Berichte und analysieren die Einstellungen und Änderungen an Den Einstellungen im Gruppenrichtlinienobjekt, um zu bestimmen, ob Sie sie genehmigen sollten. Nach der Auswertung des Gruppenrichtlinienobjekts stellen Sie es in der Produktionsumgebung bereit und verknüpfen es mit einer Domäne oder einer Organisationseinheit(OU), damit es wirksam wird, wenn die Gruppenrichtlinie für Computer in dieser Domäne oder ORGANISATIONSEINHEIT aktualisiert wird.

**So überprüfen Sie die Einstellungen im Gruppenrichtlinienobjekt**

1. Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle des Genehmigers in AGPM zugewiesen wurde. (Jeder Gruppenrichtlinienadministrator mit der Rolle "Prüfer", der in allen anderen Rollen enthalten ist, kann die Einstellungen in einem Gruppenrichtlinienobjekt überprüfen.)

2. Öffnen Sie den E-Mail-Posteingang für das Konto, und beachten Sie, dass Sie eine E-Mail-Nachricht vom AGPM-Alias mit der Anforderung eines Editors zur Bereitstellung eines Gruppenrichtlinienobjekts erhalten haben.

3. Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsolenstruktur** in der Gesamtstruktur und Domäne, in der Gruppenrichtlinienobjekte verwaltet werden sollen, auf **"Steuerelement ändern".**

4. Klicken Sie auf der Registerkarte **"Inhalt"** im Detailbereich auf die Registerkarte **"Ausstehend".**

5. Doppelklicken Sie auf **MyGPO,** um den Verlauf anzuzeigen.

6. Überprüfen Sie die Einstellungen in der neuesten Version von MyGPO:

   1.  Klicken Sie im **Verlaufsfenster** mit der rechten Maustaste auf die GPO-Version mit dem neuesten Zeitstempel, klicken Sie auf **Einstellungen,** und klicken Sie dann auf **HTML-Bericht,** um eine Zusammenfassung der Einstellungen des Gruppenrichtlinienobjekts anzuzeigen.

   2.  Klicken Sie im Webbrowser auf **"Alle anzeigen",** um alle Einstellungen im Gruppenrichtlinienobjekt anzuzeigen. Schließen Sie den Browser.

7. Vergleichen Sie die neueste Version von MyGPO mit der ersten im Archiv eingecheckten Version:

   1. Klicken Sie im **Verlaufsfenster** auf die GPO-Version mit dem neuesten Zeitstempel. Drücken Sie STRG, und klicken Sie auf die älteste GPO-Version, für die die **Computerversion** nicht **\\\ ist.

   2. Klicken Sie auf die Schaltfläche **"Unterschiede".** Der Abschnitt **"Kontorichtlinien/Kennwortrichtlinie"** ist grün hervorgehoben und wird von **\[+\]** vorangestellt, was darauf hinweist, dass diese Einstellung nur in der zweiten Version des Gruppenrichtlinienobjekts konfiguriert ist.

   3. Klicken Sie auf **"Kontorichtlinien/Kennwortrichtlinie".** Die Einstellung für die Mindestlänge des **Kennworts** wird ebenfalls grün hervorgehoben und mit **\[+\]** vorangestellt, was bedeutet, dass sie nur in der zweiten Version des Gruppenrichtlinienobjekts konfiguriert ist.

   4. Schließen Sie den Webbrowser.

**So stellen Sie das Gruppenrichtlinienobjekt in der Produktionsumgebung bereit**

1.  Klicken Sie auf der Registerkarte **"Ausstehend"** mit der rechten Maustaste auf **"MyGPO",** und klicken Sie dann auf **"Genehmigen".**

2.  Geben Sie einen Kommentar ein, der in den Verlauf des Gruppenrichtlinienobjekts aufgenommen werden soll.

3.  Klicken Sie auf **Ja**. Wenn das **Fenster "AGPM-Fortschritt"** angibt, dass der gesamtfortschritt abgeschlossen ist, klicken Sie auf **"Schließen".** Das Gruppenrichtlinienobjekt wird in der Produktionsumgebung bereitgestellt.

**So verknüpfen Sie das Gruppenrichtlinienobjekt mit einer Domäne oder Organisationseinheit**

1.  Klicken Sie in der Gruppenrichtlinien-Verwaltungskonsole mit der rechten Maustaste auf die Domäne oder eine ORGANISATIONSeinheit, auf die das von Ihnen konfigurierte Gruppenrichtlinienobjekt angewendet werden soll, und klicken Sie dann auf **"Vorhandenes Gruppenrichtlinienobjekt verknüpfen".**

2.  Klicken **Sie** im Dialogfeld Gruppenrichtlinienobjekt auswählen auf **"MyGPO"** und dann auf **"OK".**

### <a name="step-4-use-a-template-to-create-a-gpo"></a><a href="" id="bkmk-manage4"></a>Schritt 4: Verwenden einer Vorlage zum Erstellen eines Gruppenrichtlinienobjekts

In diesem Schritt verwenden Sie ein Konto mit der Editorrolle, um eine Vorlage zu erstellen – eine unbearbeitbare, statische Version eines Gruppenrichtlinienobjekts, die als Ausgangspunkt zum Erstellen neuer Gruppenrichtlinienobjekte verwendet werden kann – und erstellen dann ein neues Gruppenrichtlinienobjekt basierend auf dieser Vorlage. Vorlagen sind nützlich, um schnell mehrere Gruppenrichtlinienobjekte zu erstellen, die viele der gleichen Einstellungen enthalten.

**So erstellen Sie eine Vorlage basierend auf einem vorhandenen Gruppenrichtlinienobjekt**

1.  Melden Sie sich auf einem Computer, auf dem Sie agpm-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle des Editors in AGPM zugewiesen wurde.

2.  Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsolenstruktur** in der Gesamtstruktur und Domäne, in der Gruppenrichtlinienobjekte verwaltet werden sollen, auf **"Steuerelement ändern".**

3.  Klicken Sie auf der Registerkarte **"Inhalt"** im Detailbereich auf die Registerkarte **"Gesteuert".**

4.  Klicken Sie mit der rechten Maustaste auf **"MyGPO",** und klicken Sie dann auf **"Als Vorlage speichern",** um eine Vorlage zu erstellen, die alle derzeit in "MyGPO" enthaltenen Einstellungen enthält.

5.  Geben Sie **"MyTemplate"** als Namen für die Vorlage und einen Kommentar ein, und klicken Sie dann auf **"OK".**

6.  Wenn das **Fenster "AGPM-Fortschritt"** angibt, dass der gesamtfortschritt abgeschlossen ist, klicken Sie auf **"Schließen".** Die neue Vorlage wird auf der Registerkarte **"Vorlagen"** angezeigt.

**So fordern Sie die Erstellung eines neuen gruppenrichtlinienobjekts an, das über AGPM verwaltet wird**

1.  Klicken Sie auf die Registerkarte **"Kontrolliert".**

2.  Klicken Sie mit der rechten Maustaste auf den Knoten **"Änderungssteuerung",** und klicken Sie dann auf **"Neues kontrolliertes Gruppenrichtlinienobjekt".**

3.  Im Dialogfeld **"Neues kontrolliertes** Gruppenrichtlinienobjekt":

    1.  Um eine Kopie der Anforderung zu erhalten, geben Sie Ihre E-Mail-Adresse in das **Feld "Cc"** ein.

    2.  Geben Sie **MyOtherGPO** als Namen für das neue Gruppenrichtlinienobjekt ein.

    3.  Geben Sie einen Kommentar für das neue Gruppenrichtlinienobjekt ein.

    4.  Klicken Sie auf **"Live erstellen",** damit das neue Gruppenrichtlinienobjekt sofort nach der Genehmigung in der Produktionsumgebung bereitgestellt wird.

    5.  For **From GPO template**, select **MyTemplate**. Klicken Sie auf **Übermitteln**.

4.  Wenn das **Fenster "AGPM-Fortschritt"** angibt, dass der gesamtfortschritt abgeschlossen ist, klicken Sie auf **"Schließen".** Das neue Gruppenrichtlinienobjekt wird auf der Registerkarte **"Ausstehend"** angezeigt.

Verwenden Sie ein Konto, dem die Rolle "Genehmigende Person" zugewiesen wurde, um die ausstehende Anforderung zum Erstellen des Gruppenrichtlinienobjekts zu genehmigen, wie Sie dies in [Schritt 1: Erstellen eines Gruppenrichtlinienobjekts](#bkmk-manage1)getan haben. MyTemplate enthält alle Einstellungen, die Sie in MyGPO konfiguriert haben. Da MyOtherGPO mit MyTemplate erstellt wurde, enthält es zunächst alle Einstellungen, die MyGPO zum Zeitpunkt der Erstellung von MyTemplate enthielt. Sie können dies bestätigen, indem Sie einen Differenzbericht generieren, um MyOtherGPO mit MyTemplate zu vergleichen.

**So checken Sie das Gruppenrichtlinienobjekt aus dem Archiv zur Bearbeitung aus**

1.  Melden Sie sich auf einem Computer, auf dem Sie agpm-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle des Editors in AGPM zugewiesen wurde.

2.  Klicken Sie mit der rechten Maustaste auf **"MyOtherGPO",** und klicken Sie dann auf **"Auschecken".**

3.  Geben Sie einen Kommentar ein, der während des Auscheckens im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **OK.**

4.  Wenn das **Fenster "AGPM-Fortschritt"** angibt, dass der gesamtfortschritt abgeschlossen ist, klicken Sie auf **"Schließen".** Auf der Registerkarte **"Kontrolliert"** wird der Status des Gruppenrichtlinienobjekts als **ausgecheckt**identifiziert.

**So bearbeiten Sie das Gruppenrichtlinienobjekt offline und konfigurieren die Sperrdauer des Kontos**

1.  Klicken Sie auf der Registerkarte **"Kontrolliert"** mit der rechten Maustaste auf **"MyOtherGPO",** und klicken Sie dann auf **"Bearbeiten",** um das Fenster **"Gruppenrichtlinienverwaltungs-Editor"** zu öffnen und Änderungen an einer Offlinekopie des Gruppenrichtlinienobjekts vorzunehmen. Konfigurieren Sie für dieses Szenario die mindeste Kennwortlänge:

    1.  Doppelklicken Sie unter **"Computerkonfiguration"** auf **"Richtlinien",** **"Windows Einstellungen",** **"Sicherheits-Einstellungen",** **"Kontorichtlinien"** und **"Kontosperrungsrichtlinie".**

    2.  Doppelklicken Sie im Detailbereich auf die Dauer der **Kontosperrung.**

    3.  Aktivieren Sie im Eigenschaftenfenster **diese Richtlinieneinstellung definieren,** legen Sie die Dauer auf **30** Minuten fest, und klicken Sie dann auf **OK.**

2.  Schließen Sie das Fenster **"Gruppenrichtlinienverwaltungs-Editor".**

Überprüfen Sie MyOtherGPO in das Archiv und fordern Sie die Bereitstellung an, wie Sie dies für MyGPO in [Schritt 2: Bearbeiten eines Gruppenrichtlinienobjekts](#bkmk-manage2)getan haben. Sie können MyOtherGPO mit "MyGPO" oder "MyTemplate" mit Differenzberichten vergleichen. Jedes Konto, das die Rolle "Prüfer" (AGPM-Administrator \[Vollzugriff\], Genehmiger, Editor oder Prüfer) enthält, kann Berichte generieren.

**So vergleichen Sie ein Gruppenrichtlinienobjekt mit einem anderen Gruppenrichtlinienobjekt und einer Vorlage**

1.  So vergleichen Sie MyGPO und MyOtherGPO:

    1.  Klicken Sie auf der Registerkarte **"Kontrolliert"** auf **"MyGPO".** Drücken Sie STRG, und klicken Sie dann auf **"MyOtherGPO".**

    2.  Klicken Sie mit der rechten Maustaste auf **"MyOtherGPO",** zeigen Sie auf **"Unterschiede",** und klicken Sie auf **"HTML-Bericht".**

2.  So vergleichen Sie MyOtherGPO und MyTemplate:

    1.  Klicken Sie auf der Registerkarte **"Kontrolliert"** auf **"MyOtherGPO".**

    2.  Klicken Sie mit der rechten Maustaste auf **"MyOtherGPO",** zeigen Sie auf **"Unterschiede",** und klicken Sie auf **"Vorlage".**

    3.  Wählen Sie **"MyTemplate"** und **"HTML-Bericht"** aus, und klicken Sie dann auf **"OK".**

### <a name="step-5-delete-and-restore-a-gpo"></a><a href="" id="bkmk-manage5"></a>Schritt 5: Löschen und Wiederherstellen eines Gruppenrichtlinienobjekts

In diesem Schritt fungieren Sie als Genehmiger, um ein Gruppenrichtlinienobjekt zu löschen.

**So löschen Sie ein Gruppenrichtlinienobjekt**

1.  Melden Sie sich auf einem Computer, auf dem Sie AGPM-Client installiert haben, mit einem Benutzerkonto an, dem die Rolle "Genehmigende Person" zugewiesen wurde.

2.  Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsolenstruktur** in der Gesamtstruktur und Domäne, in der Gruppenrichtlinienobjekte verwaltet werden sollen, auf **"Steuerelement ändern".**

3.  Klicken Sie auf der Registerkarte **"Inhalt"** auf die Registerkarte **"Gesteuert",** um die gesteuerten Gruppenrichtlinienobjekte anzuzeigen.

4.  Klicken Sie mit der rechten Maustaste auf **"MyGPO",** und klicken Sie dann auf **"Löschen".** Klicken Sie auf **Gruppenrichtlinienobjekt aus Archiv und Produktion löschen,** um sowohl die Version im Archiv als auch die bereitgestellte Version des Gruppenrichtlinienobjekts in der Produktionsumgebung zu löschen.

5.  Geben Sie einen Kommentar ein, der im Überwachungspfad für das Gruppenrichtlinienobjekt angezeigt werden soll, und klicken Sie dann auf **OK.**

6.  Wenn das **Fenster "AGPM-Fortschritt"** angibt, dass der gesamtfortschritt abgeschlossen ist, klicken Sie auf **"Schließen".** Das Gruppenrichtlinienobjekt wird von der Registerkarte **"Kontrolliert"** entfernt und auf der Registerkarte **"Papierkorb"** angezeigt, wo es wiederhergestellt oder zerstört werden kann.

Gelegentlich können Sie nach dem Löschen eines Gruppenrichtlinienobjekts feststellen, dass es noch benötigt wird. In diesem Schritt fungieren Sie als Genehmiger, um ein gelöschtes Gruppenrichtlinienobjekt wiederherzustellen.

**So stellen Sie ein gelöschtes Gruppenrichtlinienobjekt wieder her**

1.  Klicken Sie auf der Registerkarte **"Inhalt"** auf die Registerkarte **"Papierkorb",** um gelöschte Gruppenrichtlinienobjekte anzuzeigen.

2.  Klicken Sie mit der rechten Maustaste auf **"MyGPO",** und klicken Sie dann auf **"Wiederherstellen".**

3.  Geben Sie einen Kommentar ein, der im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **OK.**

4.  Wenn das **Fenster "AGPM-Fortschritt"** angibt, dass der gesamtfortschritt abgeschlossen ist, klicken Sie auf **"Schließen".** Das Gruppenrichtlinienobjekt wird aus der Registerkarte **"Papierkorb"** entfernt und auf der Registerkarte **"Kontrolliert"** angezeigt.

    **Hinweis:**  
    Durch Wiederherstellen eines Gruppenrichtlinienobjekts im Archiv wird es nicht automatisch erneut in der Produktionsumgebung bereitgestellt. Um das Gruppenrichtlinienobjekt an die Produktionsumgebung zurückzugeben, stellen Sie das Gruppenrichtlinienobjekt wie in [Schritt 3: Überprüfen und Bereitstellen eines Gruppenrichtlinienobjekts bereit.](#bkmk-manage3)

     

Nach der Bearbeitung und Bereitstellung eines Gruppenrichtlinienobjekts stellen Sie möglicherweise fest, dass die letzten Änderungen am Gruppenrichtlinienobjekt ein Problem verursachen. In diesem Schritt fungieren Sie als Genehmiger, um ein Rollback auf eine frühere Version des Gruppenrichtlinienobjekts auszuführen. Sie können ein Rollback auf eine beliebige Version im Verlauf des Gruppenrichtlinienobjekts ausführen. Sie können Kommentare und Bezeichnungen verwenden, um bekannte gute Versionen zu identifizieren und zu bestimmen, wann bestimmte Änderungen vorgenommen wurden.

**So führen Sie ein Rollback zu einer früheren Version eines Gruppenrichtlinienobjekts aus**

1.  Klicken Sie auf der Registerkarte **"Inhalt"** auf die Registerkarte **"Gesteuert",** um die gesteuerten Gruppenrichtlinienobjekte anzuzeigen.

2.  Doppelklicken Sie auf **MyGPO,** um den Verlauf anzuzeigen.

3.  Klicken Sie mit der rechten Maustaste auf die bereitzustellende Version, klicken Sie auf **"Bereitstellen"** und dann auf **"Ja".**

4.  Wenn das **Statusfenster** angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **"Schließen".** Klicken Sie im **Verlaufsfenster** auf **"Schließen".**

    **Hinweis:**  
    Um zu überprüfen, ob es sich bei der neu bereitgestellten Version um die beabsichtigte Version handelt, überprüfen Sie einen Differenzbericht für die beiden Versionen. Wählen Sie im **Verlaufsfenster** für das Gruppenrichtlinienobjekt die beiden Versionen aus, klicken Sie mit der rechten Maustaste darauf, zeigen Sie auf **Differenz,** und klicken Sie dann entweder auf **HTML-Bericht** oder **XML-Bericht.**

     

 

 





