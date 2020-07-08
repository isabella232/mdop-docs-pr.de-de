---
title: Verwenden einer Testumgebung
description: Verwenden einer Testumgebung
author: dansimp
ms.assetid: b8d7b3ee-030a-4b5b-8223-4a3276fd47a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2299fb6eaf7c75f6841056f67a05fe025ea19bb7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807424"
---
# Verwenden einer Testumgebung


Wenn Sie eine Testorganisationseinheit (Organizational Unit, OU) zum Testen von Gruppenrichtlinienobjekten (GPOs) vor der Bereitstellung in der Produktionsumgebung verwenden, müssen Sie über die erforderlichen Berechtigungen für den Zugriff auf die Testorganisationseinheit verfügen. Die Verwendung einer Testorganisationseinheit ist optional.

**So verwenden Sie eine Testorganisationseinheit**

1.  Wenn Sie das Gruppenrichtlinienobjekt zur Bearbeitung ausgecheckt haben, klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gruppenrichtlinienobjekte** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten.

2.  Klicken Sie auf die ausgecheckte Kopie des zu testenden Gruppenrichtlinienobjekts. Dem Namen wird **\ [AGPM \]** vorangestellt. (Wenn Sie nicht aufgeführt ist, klicken Sie auf **Aktion**und dann auf **Aktualisieren**. Sortieren Sie die Namen alphabetisch, und **\ [AGPM \]** GPOs werden in der Regel oben in der Liste angezeigt.)

3.  Ziehen Sie das Gruppenrichtlinienobjekt in die Testorganisationseinheit, und legen Sie es ab.

4.  Klicken Sie im Dialogfeld, in dem Sie gefragt werden, ob Sie einen Link zu einem GPO in der Testorganisationseinheit erstellen möchten, auf **OK** .

### Weitere Überlegungen

-   Nach Abschluss der Prüfung löscht das Einchecken des Gruppenrichtlinienobjekts automatisch den Link zu der ausgecheckten Kopie des Gruppenrichtlinienobjekts.

### Weitere Verweise

-   [Bearbeiten eines Gruppenrichtlinienobjekts](editing-a-gpo.md)

 

 





