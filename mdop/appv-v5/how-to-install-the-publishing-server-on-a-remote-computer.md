---
title: So installieren Sie den Veröffentlichungsserver auf einem Remotecomputer
description: So installieren Sie den Veröffentlichungsserver auf einem Remotecomputer
author: dansimp
ms.assetid: 37970706-54ff-4799-9485-b9b49fd50f37
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d711fa51ade856b3ac5880ba60a19315c358734
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805396"
---
# So installieren Sie den Veröffentlichungsserver auf einem Remotecomputer


Gehen Sie wie folgt vor, um den Veröffentlichungsserver auf einem separaten Computer zu installieren. Bevor Sie die folgenden Schritte ausführen, stellen Sie sicher, dass die Datenbank und der Verwaltungsserver verfügbar sind.

**So installieren Sie den Veröffentlichungsserver auf einem separaten Computer**

1. Kopieren Sie die App-V 5,0 Server-Installationsdateien auf den Computer, auf dem Sie Sie installieren möchten. Um die App-V 5,0 Server-Installation zu starten, klicken Sie mit der rechten Maustaste, und führen Sie **appv\_server\_setup.exe** als Administrator aus. Klicken Sie auf **Installieren**.

2. Überprüfen und akzeptieren Sie auf der Seite **Erste Schritte** die Lizenzbestimmungen, und klicken Sie auf **weiter**.

3. Aktivieren Sie auf der Seite **Microsoft Update verwenden, um die Sicherheit Ihres Computers zu gewährleisten und auf dem neuesten Stand zu bleiben** , um Microsoft Updates zu aktivieren, die Option **Microsoft Update verwenden, wenn ich auf Updates Suche (empfohlen).** Wenn Sie Microsoft-Updates deaktivieren möchten, wählen Sie **Ich möchte Microsoft Update nicht verwenden**aus. Klicken Sie auf **Weiter**.

4. Aktivieren Sie auf der Seite **Featureauswahl** das Kontrollkästchen **Veröffentlichungs Server** , und klicken Sie auf **weiter**.

5. Übernehmen Sie auf der Seite **Installationsspeicherort** den Standardspeicherort, und klicken Sie auf **weiter**.

6. Geben Sie auf der Seite **Configure Publishing Server Configuration** die folgenden Elemente an:

   -   Die URL für den Verwaltungsdienst, mit dem der Veröffentlichungsserver eine Verbindung herstellen soll. Beispiel: **http://ManagementServerName:12345** .

   -   Geben Sie den Websitenamen an, den Sie für den Veröffentlichungsdienst verwenden möchten. Übernehmen Sie die Standardeinstellung, wenn Sie keinen benutzerdefinierten Namen haben.

   -   Geben Sie für die **Portbindung**eine eindeutige Portnummer an, die von App-V 5,0, beispielsweise **54321**, verwendet wird.

7. Klicken Sie auf der Seite **bereit zur Installation** auf **Installieren**.

8. Nachdem die Installation abgeschlossen ist, muss der Veröffentlichungsserver beim Verwaltungsserver registriert sein. Führen Sie in der App-V 5,0-Verwaltungskonsole die folgenden Schritte aus, um den Server zu registrieren:

   1.  Öffnen Sie die App-V 5,0 Management Server-Konsole.

   2.  Wählen Sie im linken Bereich **Server**aus, und wählen Sie dann **neuen Server registrieren**aus.

   3.  Geben Sie den Namen dieses Servers und eine Beschreibung (falls erforderlich) ein, und klicken Sie auf **Hinzufügen**.

9. Um zu überprüfen, ob der Veröffentlichungsserver ordnungsgemäß ausgeführt wird, sollten Sie ein Paket auf den Verwaltungsserver importieren, das Paket zu einer Anzeigengruppe berechtigen und das Paket veröffentlichen. Öffnen Sie die folgende URL über einen Internet Browser: <strong> http://publishingserver:pubport </strong> Wenn der Server ordnungsgemäß ausgeführt wird, werden Informationen ähnlich der folgenden angezeigt:

   ```xml
   <Publishing Protocol="1.0">
     <Packages>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" VersionId="5d03c08f-51dc-4026-8cf9-15ebe3d65a72" PackageUrl="\\server\share\file.appv" />
     </Packages>
     <NoGroup>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" />
     </NoGroup>
   </Publishing>
   ```

   Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Bereitstellen von App-V 5.0](deploying-app-v-50.md)

 

 





