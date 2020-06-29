---
title: So stellen Sie eine Verbindung mit einem Application Virtualization System her
description: So stellen Sie eine Verbindung mit einem Application Virtualization System her
author: dansimp
ms.assetid: ac38216c-5464-4c0b-a4d3-3949ba6358ac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 30d60e187e1b7595fd0dce6641fa027a1df68f3d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807216"
---
# So stellen Sie eine Verbindung mit einem Application Virtualization System her


Sie müssen die Application Virtualization Server-Verwaltungskonsole mit einem Application Virtualization System verbinden, bevor Sie die Verwaltungskonsole zum Verwalten von Anwendungen, Dateitypzuordnungen, Paketen, Anwendungslizenzen, Server Gruppen, Anbieterrichtlinien und Administratoren verwenden können. Im folgenden Verfahren werden die Schritte beschrieben, die Sie ausführen müssen, um die Konsole mit einem Application Virtualization System zu verbinden.

**So stellen Sie eine Verbindung mit einem Application Virtualization System her**

1. Klicken Sie im **Bereich** Bereich mit der rechten Maustaste auf den Knoten Application Virtualization System, und wählen Sie im Popupmenü die Option mit **Application Virtualization System verbinden** aus.

   **Hinweis:**  
   Es gibt drei Komponenten für die Application Virtualization Server-Verwaltung: die Application Virtualization-Verwaltungskonsole, den Verwaltungs-Webdienst und den SQL-Datenspeicher. Wenn diese Komponenten auf verschiedenen physischen Computern verteilt sind, müssen Sie die Sicherheit für die Komponenten für die Kommunikation über das System ordnungsgemäß konfigurieren. Weitere Informationen finden Sie in den folgenden Handbüchern und Artikeln:

   So [Konfigurieren Sie den Server für die Delegierung als vertrauenswürdig](https://go.microsoft.com/fwlink/?LinkID=166682) (https://go.microsoft.com/fwlink/?LinkID=166682)

   [Leitfaden zur Planung und Bereitstellung für das Application Virtualization System](https://go.microsoft.com/fwlink/?LinkID=122063) (https://go.microsoft.com/fwlink/?LinkID=122063)

   [Betriebshandbuch für das Application Virtualization System](https://go.microsoft.com/fwlink/?LinkID=133129) (https://go.microsoft.com/fwlink/?LinkID=133129)

   [Artikel 930472](https://go.microsoft.com/fwlink/?LinkId=114647) in der Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=114647)

   [Artikel 930565](https://go.microsoft.com/fwlink/?LinkId=114648) in der Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=114648)

     

2. Füllen Sie die Felder im Dialogfeld mit **Application Virtualization System verbinden** aus:

   1. Hostname des **Webdiensts**: Geben Sie den Namen des Application Virtualization Systems ein, mit dem Sie eine Verbindung herstellen möchten, oder geben Sie **localhost** ein, um eine Verbindung mit dem lokalen Server herzustellen.

   2. **Sichere Verbindung verwenden**– aktivieren Sie dieses Kontrollkästchen, wenn Sie eine Verbindung mit dem Server mit einer sicheren Verbindung herstellen möchten.

   3. **Port**– geben Sie die Portnummer ein, die Sie für die Verbindung verwenden möchten. **80** ist die standardmäßige Standardportnummer, und **443** ist die Secure-Port-Nummer.

   4. **Aktuelles Windows-Konto verwenden**– aktivieren Sie dieses Optionsfeld, um die aktuellen Windows-Kontoanmeldeinformationen zu verwenden.

   5. **Windows-Konto angeben**– wählen Sie dieses Optionsfeld aus, wenn Sie eine Verbindung mit dem Server als anderen Benutzer herstellen möchten.

   6. **Name**: Geben Sie den Namen des neuen Benutzers ein, indem Sie entweder das *DOMAIN\\username* -oder das <em> username@Domain-Format verwenden </em> .

   7. **Kennwort**– geben Sie das Kennwort ein, das dem neuen Benutzer entspricht.

3. Klicken Sie auf **OK**.

## Verwandte Themen


[So führen Sie Verwaltungsaufgaben in der Application Virtualization Server Management Console durch](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





