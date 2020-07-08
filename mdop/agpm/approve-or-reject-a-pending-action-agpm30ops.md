---
title: Genehmigen oder Ablehnen einer ausstehenden Aktion
description: Genehmigen oder Ablehnen einer ausstehenden Aktion
author: dansimp
ms.assetid: 6d78989a-b600-4876-9dd9-bc6207ff2ce7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5a787e032a441a8b33a48667afecfc98ec2a3642
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807831"
---
# Genehmigen oder Ablehnen einer ausstehenden Aktion


Die Hauptverantwortung einer genehmigenden Person besteht darin, Anforderungen für die Erstellung, Bereitstellung und Löschung von Gruppenrichtlinienobjekten (Group Policy Object, GPO) zu evaluieren und anschließend zu genehmigen oder abzulehnen. Berichte können einer genehmigenden Person beim Auswerten einer neuen Version eines Gruppenrichtlinienobjekts behilflich sein.

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle Genehmiger oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So genehmigen oder ablehnen Sie eine ausstehende Anforderung**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **Ausstehend** , um die ausstehenden GPOs anzuzeigen.

3.  Klicken Sie mit der rechten Maustaste auf ein ausstehender GPO, und klicken Sie dann entweder auf **genehmigen** oder **ablehnen**.

4.  Wenn Sie die Bereitstellung genehmigen, klicken Sie im Dialogfeld **ausstehender Vorgang genehmigen** auf **erweitert** , um Links zum Gruppenrichtlinienobjekt zu überprüfen. Zeigen Sie mit dem Mauszeiger auf ein Element in der Struktur, um Details anzuzeigen.

    -   Standardmäßig werden alle Verknüpfungen mit dem Gruppenrichtlinienobjekt wiederhergestellt.

    -   Um zu verhindern, dass eine Verknüpfung wiederhergestellt wird, deaktivieren Sie das Kontrollkästchen für diesen Link.

    -   Um zu verhindern, dass alle Verknüpfungen wiederhergestellt werden, deaktivieren Sie das Kontrollkästchen **Verknüpfungen wiederherstellen** im Dialogfeld **Gruppenrichtlinienobjekt bereitstellen** .

5.  Klicken Sie auf **Ja** oder **OK** , um die Genehmigung oder Ablehnung der ausstehenden Aktion zu bestätigen. Wenn Sie die Anforderung genehmigt haben, wird das Gruppenrichtlinienobjekt auf die entsprechende Registerkarte für die auszuführende Aktion verschoben.

    **Hinweis**  Wenn die e-Mail-Adresse einer genehmigenden Person im Feld **an e-Mail-Adresse** auf der Registerkarte **Domänen** **Delegierung** enthalten ist, empfängt die genehmigende Person e-Mail-Nachrichten aus dem AGPM-Alias, wenn ein Bearbeiter oder Bearbeiter eine Anforderung absendet.

     

### Weitere Überlegungen

-   Standardmäßig müssen Sie eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über die erforderlichen Berechtigungen verfügen, um die von Ihnen genehmigte Anforderung ausführen zu können.

### Weitere Verweise

-   [Durchführen der Aufgaben von genehmigenden Personen](performing-approver-tasks-agpm30ops.md)

 

 





