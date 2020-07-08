---
title: So verweigern Sie den Zugriff auf eine Anwendung
description: So verweigern Sie den Zugriff auf eine Anwendung
author: dansimp
ms.assetid: 14f5e201-7265-462c-b738-57938dc3fc30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 56a89669ea8c6323023b585d6d58620cd203fc00
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807139"
---
# So verweigern Sie den Zugriff auf eine Anwendung


Benutzer müssen in der Liste der **Zugriffsberechtigungen** einer Anwendung sein, um die Anwendung laden und verwenden zu können. Die Application Virtualization Server-Verwaltungskonsole unterstützt zwar nicht die explizite Verweigerung des Zugriffs einer Benutzergruppe auf eine Anwendung, aber Sie können die Benutzergruppen aus den Eigenschaften einer Anwendung entfernen, um dies zu erreichen.

**So verweigern Sie den Zugriff auf eine Anwendung**

1.  Klicken Sie für eine vorhandene Anwendung im linken Bereich auf den Knoten **Anwendungen** .

2.  Klicken Sie im rechten Bereich mit der rechten Maustaste auf eine Anwendung, und wählen Sie **Eigenschaften**aus. Wählen Sie dann die Registerkarte **Zugriffsberechtigungen** aus.

3.  Wenn Sie den Zugriff für eine Benutzergruppe entfernen möchten, markieren Sie die Benutzergruppe, und klicken Sie auf **Entfernen**.

4.  Klicken Sie auf **OK**.

    **Hinweis**  Um den Zugriff auf Anwendungen zu steuern, können Sie auch die Anwendungslizenzen einschränken. Das Einrichten der richtigen Benutzergruppen in den Active Directory-Domänendiensten bietet die einfachste Möglichkeit zum gewähren und Verweigern des Zugriffs auf bestimmte Gruppen von Benutzern.

     

## Verwandte Themen


[So gewähren Sie Zugriff auf eine Anwendung](how-to-grant-access-to-an-application.md)

[So verwalten Sie Anwendungslizenzen in der Server Management Console](how-to-manage-application-licenses-in-the-server-management-console.md)

[So verwalten Sie Anwendungen in der Server Management Console](how-to-manage-applications-in-the-server-management-console.md)

 

 





