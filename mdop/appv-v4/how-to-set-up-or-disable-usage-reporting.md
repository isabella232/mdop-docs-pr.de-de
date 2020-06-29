---
title: So richten Sie die Verwendungsberichterstellung ein oder deaktivieren Sie sie
description: So richten Sie die Verwendungsberichterstellung ein oder deaktivieren Sie sie
author: dansimp
ms.assetid: 8587003a-128d-4b5d-ac70-5b9eddddd3dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f8f6c44d4060581f1ebe435875bc2f105cb93d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806751"
---
# So richten Sie die Verwendungsberichterstellung ein oder deaktivieren Sie sie


Sie können die folgenden Verfahren in der Application Virtualization Server-Verwaltungskonsole verwenden, um die Dauer (in Monaten) der Nutzungsinformationen für Application Virtualization System anzugeben, die Sie in der Datenbank speichern möchten.

**Hinweis**  Zum Speichern von Nutzungsinformationen müssen Sie auf der Registerkarte **Anbieter Pipeline** das Kontrollkästchen **Verwendungsinformationen protokollieren** aktivieren. Wenn Sie diese Registerkarte anzeigen möchten, klicken Sie im Ergebnisbereich **Anbieterrichtlinien** mit der rechten Maustaste auf die Anbieterrichtlinie, und wählen Sie **Eigenschaften**aus.

 

**So richten Sie Verwendungsberichte ein**

1.  Klicken Sie im linken Bereich mit der rechten Maustaste auf den Knoten Application Virtualization System, und wählen Sie **Systemoptionen**aus.

2.  Wählen Sie die Registerkarte **Datenbank** aus.

3.  Aktivieren Sie das Optionsfeld **Nutzung für (Monate)** oder **alle Verwendung** beibehalten.

4.  Wenn Sie die Nutzungsdauer in Monaten angeben möchten, geben Sie eine Zahl von 1 bis 120 ein (Standardwert ist 6 Monate). Wenn Sie **alle Verwendung beibehalten**auswählen, wird die Datenbank so lange vergrößert, bis Sie die angegebene Größenbeschränkung erreicht hat.

5.  Klicken Sie auf über **nehmen** oder **OK**.

**So deaktivieren Sie die Verwendungsberichterstattung**

1.  Klicken Sie auf den Knoten **Anbieterrichtlinien** .

2.  Klicken Sie mit der rechten Maustaste auf **Anbieterrichtlinie** , und wählen Sie **Eigenschaften**aus.

3.  Wählen Sie die Registerkarte **Anbieter Pipeline** aus.

4.  Deaktivieren Sie das Kontrollkästchen **Verwendungsinformationen protokollieren** .

5.  Klicken Sie auf über **nehmen** oder **OK**.

## Verwandte Themen


[So passen Sie ein Application Virtualization System in der Server Management Console an](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[So richten Sie die Datenbankgröße ein oder deaktivieren Sie sie](how-to-set-up-or-disable-database-size.md)

 

 





