---
title: Testen eines Gruppenrichtlinienobjekts in einer separaten Organisationseinheit
description: Testen eines Gruppenrichtlinienobjekts in einer separaten Organisationseinheit
author: dansimp
ms.assetid: 9a9e6d22-74e6-41d8-ac2f-12a1b76ad5a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 509721fdd775c8669399549f6dcc29cb9ebaea2f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807435"
---
# Testen eines Gruppenrichtlinienobjekts in einer separaten Organisationseinheit


Wenn Sie eine Testorganisationseinheit (Organizational Unit, OU) zum Testen von Gruppenrichtlinienobjekten (GPOs) innerhalb der gleichen Domäne vor der Bereitstellung in der Produktionsumgebung verwenden, müssen Sie über die erforderlichen Berechtigungen für den Zugriff auf die Testorganisationseinheit verfügen. Die Verwendung einer Test-ou ist optional.

**So verwenden Sie eine Testorganisationseinheit**

1.  Obwohl Sie das Gruppenrichtlinienobjekt zur Bearbeitung ausgecheckt haben, klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gruppenrichtlinienobjekte** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten.

2.  Klicken Sie auf die ausgecheckte Kopie des zu testenden Gruppenrichtlinienobjekts. Dem Namen wird **\ [AGPM \]** vorangestellt. (Wenn Sie nicht aufgeführt ist, klicken Sie auf **Aktion**und dann auf **Aktualisieren**. Sortieren Sie die Namen alphabetisch, und **\ [AGPM \]** GPOs werden in der Regel oben in der Liste angezeigt.)

3.  Ziehen Sie das Gruppenrichtlinienobjekt in die OU Test.

4.  Klicken Sie im Dialogfeld, in dem Sie gefragt werden, ob Sie einen Link zu einem GPO in der Testorganisationseinheit erstellen möchten, auf **OK** .

### Weitere Überlegungen

-   Nach Abschluss der Prüfung löscht das Einchecken des Gruppenrichtlinienobjekts automatisch den Link zu der ausgecheckten Kopie des Gruppenrichtlinienobjekts.

### Weitere Verweise

-   [Verwenden einer Testumgebung](using-a-test-environment.md)

 

 





