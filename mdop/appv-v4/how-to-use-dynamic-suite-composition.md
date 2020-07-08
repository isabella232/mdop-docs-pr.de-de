---
title: So verwenden Sie Dynamic Suite Composition
description: So verwenden Sie Dynamic Suite Composition
author: dansimp
ms.assetid: 24147feb-a0a8-4791-a8e5-cbe5fe13c762
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bff4c9721352785cf6db5c497234ceaa3c5e448
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806699"
---
# So verwenden Sie Dynamic Suite Composition


Mit der Dynamic Suite-Komposition in Application Virtualization können Sie eine Anwendung als von einer anderen Anwendung abhängig definieren, beispielsweise von Middleware oder einem Plug-in. Dadurch kann die Anwendung mit der Middleware oder dem Plug-in in der virtuellen Umgebung interagieren, wobei dies in der Regel verhindert wird. Dies ist hilfreich, da ein sekundäres Anwendungspaket mit mehreren anderen Anwendungen verwendet werden kann, die als *primäre Anwendungen*bezeichnet werden, sodass jede primäre Anwendung auf dasselbe sekundäre Paket verweisen kann.

Sie können die Dynamic Suite-Komposition verwenden, wenn Sie Anwendungen sequenzieren, die von Plug-ins wie ActiveX-Steuerelementen oder Anwendungen abhängen, die von Middleware wie OLE DB oder Java Runtime Environment (JRE) abhängen. Wenn für jede Anwendung, die diese abhängigen Komponenten verwendet hat, sequenzielle Sequenzierung erforderlich war, einschließlich der Komponenten, müssten Updates für diese Komponenten eine erneute Sequenzierung aller primären Anwendungen erfordern. Wenn Sie die primären Anwendungen ohne die Komponenten sequenzieren und dann die Middleware oder das Plug-in als sekundäres Paket sequenzieren, muss nur das sekundäre Paket aktualisiert werden.

Ein Vorteil dieses Ansatzes besteht darin, dass die Größe der primären Pakete verringert wird. Ein weiterer Vorteil besteht darin, dass Sie die Zugriffsberechtigungen für sekundäre Anwendungen besser steuern können. Beachten Sie, dass die sekundäre Anwendung in regelmäßigen Abständen gestreamt werden kann und nicht vollständig zwischengespeichert werden muss, um ausgeführt zu werden.

Ein primäres Paket kann mehr als ein sekundäres Paket aufweisen. Es wird jedoch nur eine Abhängigkeitsstufe unterstützt, sodass Sie ein sekundäres Paket nicht als abhängig von einem anderen sekundären Paket definieren können. Auch die sekundäre Anwendung kann nur Middleware oder ein Plug-in sein und kann kein weiteres vollständiges Softwareprodukt sein.

Wenn Sie beabsichtigen, mehrere primäre Anwendungen von einem einzelnen Middleware-Produkt abhängig zu machen, stellen Sie sicher, dass Sie diese Konfiguration testen, um die potenziellen Auswirkungen auf die Systemleistung zu ermitteln, bevor Sie Sie bereitstellen.

**Wichtig**  Paketabhängigkeiten können als obligatorisch für eine primäre Anwendung angegeben werden. Wenn ein sekundäres Paket als obligatorisch gekennzeichnet ist und während des Ladens nicht zugegriffen werden kann, tritt beim Laden des sekundären Pakets ein Fehler auf. Außerdem schlägt die primäre Anwendung fehl, wenn der Benutzer versucht, Sie zu starten.

 

Sie können die folgenden Verfahren zum Erstellen eines sekundären Pakets für ein Plug-in oder eine Middleware-Komponente verwenden, und dann können Sie das letzte Verfahren verwenden, um die Abhängigkeit in der OSD-Datei des sekundären Pakets zu definieren.

**So erstellen Sie ein sekundäres Paket für ein Plug-in mithilfe der Dynamic Suite-Komposition**

1.  Installieren Sie Application Virtualization Sequencer auf einem Sequenzcomputer, der mit einem sauberen Bild eingerichtet ist, und speichern Sie den Computerzustand.

2.  Sequenzieren Sie die primäre Anwendung, und speichern Sie das Paket im Inhaltsordner auf dem Server.

3.  Wiederherstellen des Sequenz Computers in seinem gespeicherten Zustand aus Schritt 1.

4.  Installieren und konfigurieren Sie die primäre Anwendung lokal auf dem Sequenzcomputer.

    **Wichtig**  Sie müssen einen neuen Paketstamm für das sekundäre Paket angeben.

     

5.  Starten Sie die Sequencer-Überwachungsphase.

6.  Installieren Sie das Plug-in auf dem Sequenzcomputer, und konfigurieren Sie es nach Bedarf.

7.  Öffnen Sie die primäre Anwendung, und stellen Sie sicher, dass das Plug-in ordnungsgemäß funktioniert.

8.  Erstellen Sie in der Sequencer-Konsole eine Dummy-Anwendung zur Darstellung des sekundären Pakets, das das Plug-in enthalten soll, und wählen Sie ein Symbol aus.

9.  Speichern Sie das Paket im Inhaltsordner auf dem Server.

    **Hinweis**  Um die Verwaltung sekundärer Pakete zu unterstützen, wird empfohlen, dass der Paketname den Begriff "sekundäres Paket" enthält, um hervorzuheben, dass es sich um ein Paket handelt, das nicht als eigenständige Anwendung verwendet werden kann, beispielsweise **\ [Plug in Name \]-sekundäres Paket**.

     

**So erstellen Sie ein sekundäres Paket für Middleware mithilfe der Dynamic Suite-Komposition**

1.  Installieren Sie Application Virtualization Sequencer auf einem Sequenzcomputer, der mit einem sauberen Bild eingerichtet ist, und speichern Sie den Computerzustand.

2.  Installieren Sie die Middleware lokal auf dem Sequenzcomputer, und konfigurieren Sie Sie.

3.  Sequenzieren Sie die primäre Anwendung, und speichern Sie das Paket im Inhaltsordner auf dem Server.

4.  Wiederherstellen des Sequenz Computers in seinem gespeicherten Zustand aus Schritt 1.

5.  Starten Sie den Sequencer, um ein neues Paket zu erstellen.

6.  Starten Sie die Sequencer-Überwachungsphase.

7.  Installieren Sie die Middleware-Anwendung auf dem Sequenzcomputer, und konfigurieren Sie Sie wie in einer typischen Installation.

8.  Durchführen des Sequenz Prozesses

9.  Speichern Sie das Paket im Inhaltsordner auf dem Server.

    **Hinweis**  Um die Verwaltung sekundärer Pakete zu unterstützen, wird empfohlen, dass der Paketname den Begriff "sekundäres Paket" enthält, um hervorzuheben, dass es sich um ein Paket handelt, das nicht als eigenständige Anwendung verwendet werden kann, beispielsweise " **\ [Middleware Name \]"-sekundäres Paket**.

     

**So definieren Sie die Abhängigkeit im primären Paket**

1. Öffnen Sie auf dem Server die OSD-Datei des sekundären Pakets zur Bearbeitung. (Es empfiehlt sich, einen XML-Editor zu verwenden, um Änderungen an der OSD-Datei vorzunehmen; Sie können jedoch auch Notepad als Alternative verwenden.)

2. Kopieren Sie die **CODEBASE-HREF** -Zeile aus der Datei.

3. Öffnen Sie die OSD-Datei des primären Pakets zur Bearbeitung.

4. Fügen Sie das Tag <strong> &lt; Dependencies &gt; </strong> nach dem Schließen des ** &lt; /ENVLIST &gt; ** -Tags am Ende des ** &lt; VIRTUALENV &gt; ** -Abschnitts direkt vor dem ** &lt; &gt; /VIRTUALENV** -Tag ein.

5. Fügen Sie die **CODEBASE-HREF** -Zeile aus dem sekundären Paket nach dem soeben erstellten ** &lt; Dependencies &gt; ** -Tag ein.

6. Wenn das sekundäre Paket ein obligatorisches Paket ist, was bedeutet, dass es gestartet werden muss, bevor das primäre Paket gestartet wird, fügen Sie die Eigenschaft **Mandatory = "true"** innerhalb des **CodeBase** -Tags hinzu. Wenn dies nicht zwingend erforderlich ist, kann die Eigenschaft ausgelassen werden.

7. Schließen Sie das ** &lt; Dependencies &gt; ** -Tag, indem Sie Folgendes einfügen:

   **&lt;/DEPENDENCIES&gt;**

8. Überprüfen Sie die Änderungen, die Sie an der OSD-Datei vorgenommen haben, und speichern Sie die Datei, und schließen Sie Sie. Im folgenden Beispiel wird gezeigt, wie der hinzugefügte Abschnitt angezeigt werden sollte. Die hier gezeigten Tag-Werte sind beispielsweise nur.

   **&lt;VIRTUALENV&gt;**

        **&lt;ENVLIST&gt;**

   **…**

        **&lt;/ENVLIST&gt;**

        **&lt;DEPENDENCIES&gt;**

             **&lt;CODEBASE HREF="rtsp://virt\_apps/package.1/package.1.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.1\\osguard.cp"/&gt;**

             **&lt;CODEBASE HREF="rtsp://sample\_apps/package.2/sample.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.2\\osguard.cp" MANDATORY="TRUE" /&gt;**

        **&lt;/DEPENDENCIES&gt;**

   **&lt;/VIRTUALENV&gt;**

9. Wenn das sekundäre Paket Einträge im ** &lt; ENVLIST &gt; ** -Abschnitt der OSD-Datei enthält, müssen Sie diese Einträge in denselben Abschnitt im primären Paket kopieren.

## Verwandte Themen


[Erstellen oder Aktualisieren virtueller Anwendungen mit dem App-V-Sequenzer](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





