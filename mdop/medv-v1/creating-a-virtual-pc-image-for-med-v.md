---
title: Erstellen eines virtuellen PC-Images für MED-V
description: Erstellen eines virtuellen PC-Images für MED-V
author: dansimp
ms.assetid: 5e02ea07-25b9-41a5-a803-d70c55eef586
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 84e45f9ff7213abdd6288bcd750238436d3ab68c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810090"
---
# Erstellen eines virtuellen PC-Images für MED-V


Zum Erstellen eines virtuellen PC-Images (VPC) für MED-V müssen Sie die folgenden Schritte ausführen:

1.  [Erstellen Sie ein VPC-Bild](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc).

2.  [Installieren Sie das MED-V Workspace. MSI-Paket auf dem VPC-Abbild](#bkmk-howtoinstallthemedvworkspacemsipackage).

3.  [Führen Sie das Tool MED-V Virtual Machine Voraussetzungen für das VPC-Abbild aus](#bkmk-howtorunthevirtualmachineprerequisitestool).

4.  [Manuelle Konfiguration von Voraussetzungen für virtuelle Maschinen auf dem VPC-Abbild](#bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites)

5.  [Konfigurieren von Sysprep für MED-V-Bilder](#bkmk-howtoconfiguresysprepformedvimages) (optional).

6.  [Deaktivieren Sie Microsoft Virtual PC](#bkmk-turningoffmicrosoftvirtualpc).

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a>Erstellen eines virtuellen PC-Images mithilfe von Microsoft Virtual PC


Informationen zum Erstellen eines virtuellen PC-Images mit Microsoft Virtual PC finden Sie in der Virtual PC-Dokumentation.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Hilfe zu Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=182378)

-   [Erstellen eines virtuellen Computers und Installieren eines Gastbetriebssystems](https://go.microsoft.com/fwlink/?LinkId=182379)

## <a href="" id="bkmk-howtoinstallthemedvworkspacemsipackage"></a>Installieren des MED-V Workspace. msi-Pakets


Installieren Sie nach dem Erstellen des Virtual PC-Bilds das MED-V Workspace. MSI-Paket auf dem Bild.

**So installieren Sie das MED-V Workspace-Bild**

1.  Starten Sie den virtuellen Computer, und kopieren Sie das MED-V Workspace. MSI-Paket nach innen.

    Das MED-V Workspace. MSI-Paket heißt *MED-V\_workspace\_x.msi*, wobei *x* die Versionsnummer ist.

    Beispiel: *MED-V\_workspace\_1.0.65.msi*.

2.  Doppelklicken Sie auf das MED-V Workspace. MSI-Paket, und folgen Sie den Anweisungen des Installations-Assistenten.

    **Hinweis:**  
    Wenn eine neue Med-v-Version veröffentlicht wird und ein vorhandenes Virtual PC-Abbild aktualisiert wird, deinstallieren Sie das vorhandene Med-v Workspace. MSI-Paket, starten Sie den Computer neu, und installieren Sie das neue Med-v Workspace. MSI-Paket.



~~~
**Note**  
After the MED-V workspace .msi package is installed, other products that replace GINA cannot be installed.
~~~



## <a href="" id="bkmk-howtorunthevirtualmachineprerequisitestool"></a>Ausführen des Tools für Voraussetzungen für virtuelle Maschinen


Das Tool für die Voraussetzungen für virtuelle Maschinen (VM) ist ein Assistent, der mehrere Voraussetzungen automatisiert.

**Hinweis:**  
Obwohl im Assistenten viele Parameter konfigurierbar sind, können die für die ordnungsgemäße Funktion von MED-V erforderlichen Eigenschaften nicht konfiguriert werden.



**So führen Sie das Tool für Voraussetzungen für virtuelle Maschinen aus**

1.  Nachdem das Med-v Workspace. MSI-Paket installiert wurde, wählen Sie **Start** im Windows-Startmenü **Alle Programme &gt; Med-v &gt; VM-Voraussetzungen-Tool**aus.

    **Hinweis:**  
    Der Benutzer, der das Tool für Voraussetzungen für virtuelle Maschinen ausführt, muss über lokale Administratorrechte verfügen und muss der einzige Benutzer sein, der angemeldet ist.



~~~
The **MED-V VM Prerequisite Wizard Welcome** page appears.
~~~

2. Klicken Sie auf **Weiter**.

3. Wählen Sie auf der Seite **Windows-Einstellungen** in den folgenden konfigurierbaren Eigenschaften die zu konfigurierenden Eigenschaften aus:

   -   **Löschen der persönlichen Verlaufsinformationen der Benutzer**

   -   **Temporäres Verzeichnis für lokales Profil löschen**

   -   **Deaktivieren von Sounds für folgende Windows-Ereignisse: Start, Anmeldung, Abmelden**

   **Hinweis:**  
   Aktivieren Sie den Windows-Seiten Speicher in einer Gruppenrichtlinie nicht.



4. Klicken Sie auf **Weiter**.

5. Wählen Sie auf der Seite **Internet Explorer-Einstellungen** in den folgenden konfigurierbaren Eigenschaften die zu konfigurierenden Eigenschaften aus:

   -   **Verwenden Sie keine AutoVervollständigen-Features**

   -   **Deaktivieren der Wiederverwendung von Windows zum Starten von Tastenkombinationen**

   -   **Browserverlauf löschen**

   -   **Aktivieren von Tabbed-Browsing in Internet Explorer 7**

6. Klicken Sie auf **Weiter**.

7. Wählen Sie auf der Seite **Windows-Dienste** in den folgenden konfigurierbaren Eigenschaften die zu konfigurierenden Eigenschaften aus:

   -   **Security Center-Dienst**

   -   **Aufgabenplanungsdienst**

   -   **Dienst für automatische Updates**

   -   **System Wiederherstellungs Dienst**

   -   **Indizierungsdienst**

   -   **Drahtlose Nullkonfiguration**

   -   **Schnelle Benutzerwechsel Kompatibilität**

8. Klicken Sie auf **Weiter**.

9. Gehen Sie auf der Windows-Seite für die **automatische Anmeldung** wie folgt vor:

   1.  Aktivieren Sie das Kontrollkästchen **Automatische Windows-Anmeldung aktivieren** .

   2.  Weisen Sie einen **Benutzernamen** und ein **Kennwort**zu.

10. Klicken Sie auf über **nehmen**, und klicken Sie im daraufhin angezeigten Bestätigungsdialogfeld auf **Ja**.

11. Klicken Sie auf der **Zusammenfassungs** Seite auf **Fertig stellen** , um den Assistenten zu beenden.

**Hinweis:**  
Überprüfen Sie, ob die Gruppenrichtlinien die im Tool Voraussetzungen festgelegten obligatorischen Einstellungen nicht überschreiben.



## <a href="" id="bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites"></a>So konfigurieren Sie die Voraussetzungen für die manuelle Installation von MED-V Virtual Machine


Einige Konfigurationen können nicht über das Voraussetzungen-Tool für virtuelle Maschinen konfiguriert werden und müssen manuell ausgeführt werden.

-   Einstellungen für den virtuellen Computer

    Es wird empfohlen, die folgenden Einstellungen für den virtuellen Computer in der Microsoft Virtual PC-Konsole zu konfigurieren:

    -   Deaktivieren von Diskettenlaufwerken

    -   Deaktivieren Sie Undo-Disks (**Einstellungen &gt; Undo-Disks**).

    -   Stellen Sie sicher, dass das Bild nur einen virtuellen Prozessor aufweist.

    -   Sie können die Interaktionen zwischen dem virtuellen Computer und dem Benutzer eliminieren, wenn diese nicht mit veröffentlichten Anwendungen verknüpft sind (beispielsweise Nachrichten, die Benutzereingaben erfordern).

-   Bildeinstellungen

    Konfigurieren Sie die folgenden manuellen Einstellungen innerhalb des Bilds:

    1.  Deaktivieren Sie im Fenster **Eigenschaften von Energieoptionen** den Ruhezustand und den Ruhezustand.

    2.  Wenden Sie die neuesten Windows-Updates an.

    3.  Deaktivieren Sie im Dialogfeld **Windows-Start und-Wiederherstellung** im Abschnitt **System Fehler** das Kontrollkästchen **automatisch neu starten** .

    4.  Stellen Sie sicher, dass das Bild einen VLK-Lizenzschlüssel verwendet.

-   Installieren von VPC-Ergänzungen

    Klicken Sie im Menü **Aktion** auf **Virtual Machine Additions installieren oder aktualisieren**.

-   Konfigurieren des Drucks

    Sie können den Druck aus dem MED-V-Arbeitsbereich auf eine der folgenden Arten konfigurieren:

    -   Fügen Sie dem virtuellen Computer einen Drucker hinzu.

    -   Drucken mit Druckern zulassen, die auf dem Hostcomputer konfiguriert sind.

## <a href="" id="bkmk-howtoconfiguresysprepformedvimages"></a>Konfigurieren von Sysprep für MED-V-Bilder


In einem Med-v-Arbeitsbereich kann Sysprep so konfiguriert werden, dass eine eindeutige Sicherheits-ID (SID) zugewiesen wird, insbesondere dann, wenn mehrere med-v-Arbeitsbereiche auf einem einzelnen Computer ausgeführt werden. Es wird nicht empfohlen, Sysprep für die Teilnahme an einer Domäne zu verwenden. Verwenden Sie stattdessen die Aktion MED-V Join-Domänen Skript, wie unter [so wird es gemacht: Einrichten von Skriptaktionen](how-to-set-up-script-actions.md)beschrieben.

**Hinweis:**  
Sysprep ist das Microsoft-System Vorbereitungs Dienstprogramm für das Windows-Betriebssystem.



**So konfigurieren Sie Sysprep in einem MED-V-Arbeitsbereich**

1.  Erstellen Sie ein Verzeichnis im Stammverzeichnis des Systemlaufwerks mit dem Namen *Sysprep*.

2.  Extrahieren Sie auf der Windows-Installations-CD *deploy.cab* auf das Stammverzeichnis des Systemlaufwerks, oder laden Sie das neueste Update zur Bereitstellungs Tools von der Microsoft-Website herunter.

    -   Informationen zu Windows 2000 finden Sie unter [Bereitstellungs Tools-Update für Windows 2000](https://go.microsoft.com/fwlink/?LinkId=143001).

    -   Unter Windows XP finden Sie unter [Bereitstellungs Tools-Update für Windows XP](https://go.microsoft.com/fwlink/?LinkId=143000).

3.  Führen Sie den **Setup-Manager** (setupmgr.exe) aus.

4.  Folgen Sie dem Setup-Manager-Assistenten.

Nachdem Sysprep konfiguriert und der MED-V-Arbeitsbereich erstellt wurde, muss Sysprep ausgeführt werden.

**So führen Sie Sysprep aus**

1.  Führen Sie aus dem Ordner "Sysprep", der sich im Stammverzeichnis des Systemlaufwerks befindet, das System Vorbereitungs Tool (Sysprep.exe) aus.

2.  Klicken Sie im daraufhin angezeigten warnmeldungsfeld auf **OK**.

3.  Aktivieren Sie im Dialogfeld **Sysprep-Eigenschaften** die Kontrollkästchen **Kulanzzeitraum nicht zurücksetzen für Aktivierung** und **Mini-Setup verwenden** .

4.  Klicken Sie auf erneut **versiegeln**.

5.  Wenn Sie mit den Informationen, die im angezeigten Bestätigungsdialogfeld aufgeführt sind, nicht zufrieden sind, klicken Sie auf **Abbrechen** , und ändern Sie die Auswahl.

6.  Klicken Sie auf **OK** , um den System Vorbereitungsvorgang abzuschließen.

## <a href="" id="bkmk-turningoffmicrosoftvirtualpc"></a>Deaktivieren von Microsoft Virtual PC


Nachdem alle Komponenten installiert und konfiguriert sind, schließen Sie Microsoft Virtual PC, und wählen Sie **Deaktivieren aus**.

## Verwandte Themen


Erstellen eines MED-V-Bilds [so wird es gemacht: Einrichten von Skriptaktionen](how-to-set-up-script-actions.md)









