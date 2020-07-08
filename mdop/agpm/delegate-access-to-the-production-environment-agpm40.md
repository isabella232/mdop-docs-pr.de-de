---
title: Delegieren des Zugriffs auf die Produktionsumgebung
description: Delegieren des Zugriffs auf die Produktionsumgebung
author: dansimp
ms.assetid: 4c670581-8c47-41ea-80eb-02846ff1ec1f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a3920a8ba5835cbbcb8a74f0af4e3ca1e1c5f43f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807623"
---
# Delegieren des Zugriffs auf die Produktionsumgebung


In Advanced Group Policy Management (AGPM) können Sie den Zugriff auf Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) in der Produktionsumgebung der Domäne ändern und vorhandene Berechtigungen für diese GPOs ersetzen. Sie können Berechtigungen auf Domänenebene so konfigurieren, dass Benutzer das Bearbeiten, löschen oder Ändern der Sicherheit von GPOs in der Produktionsumgebung zulassen oder verhindern, wenn Sie den Ordner **Change Control** nicht in der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) verwenden.

**Hinweis:**  
-   Das Ändern der Delegierten Funktion des Zugriffs auf die Produktionsumgebung hat keinen Einfluss auf die Möglichkeit der Benutzer, GPOs zu verknüpfen.

-   Wenn GPOs kontrolliert oder bereitgestellt werden, wird der Zugriff auf alle anderen Konten, mit Ausnahme der Berechtigungen **Lesen** und **anwenden** , entfernt.

 

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto erforderlich, das entweder über die Rolle des AGPM-Administrators (Vollzugriff) oder über die erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) verfügt. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So ändern Sie den Zugriff auf GPOs in der Produktionsumgebung der Domäne**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie auf die Registerkarte **Produktions Delegierung** .

3.  So fügen Sie Berechtigungen für einen Benutzer oder eine Gruppe hinzu, die keinen Zugriff auf die Produktionsumgebung haben, oder um die Berechtigungen für einen Benutzer oder eine Gruppe zu ersetzen, der Zugriff hat:

    1.  Klicken Sie auf **Hinzufügen**, wählen Sie einen Benutzer oder eine Gruppe aus, und klicken Sie dann auf **OK**.

    2.  Wählen Sie Berechtigungen aus, die an diesen Benutzer oder die Gruppe für die Produktionsumgebung delegiert werden sollen, und klicken Sie dann auf **OK**.

4.  Wenn Sie alle Berechtigungen für die Produktionsumgebung für einen Benutzer oder eine Gruppe entfernen möchten, wählen Sie den Benutzer oder die Gruppe aus, klicken Sie auf **Entfernen**, und klicken Sie dann auf **OK**.

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie die Berechtigung zum **Ändern der Sicherheit** für die Domäne besitzen.

-   Berechtigungen für das AGPM-Dienstkonto können auf der Registerkarte **Produktions Delegierung** nicht geändert werden.

-   Die folgenden Konten verfügen standardmäßig über Berechtigungen für GPOs in der Produktionsumgebung:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Account</th>
    <th align="left">Standardberechtigungen für GPOs</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>&lt;AGPM-Dienstkonto&gt;</p></td>
    <td align="left"><p>Bearbeiten von Einstellungen, löschen, Ändern der Sicherheit</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Authentifizierte Benutzer</p></td>
    <td align="left"><p>Lesen, anwenden</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Domänenadministratoren</p></td>
    <td align="left"><p>Bearbeiten von Einstellungen, löschen, Ändern der Sicherheit</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Unternehmensadministratoren</p></td>
    <td align="left"><p>Bearbeiten von Einstellungen, löschen, Ändern der Sicherheit</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Unternehmensdomänencontroller</p></td>
    <td align="left"><p>Lesen</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>System</p></td>
    <td align="left"><p>Bearbeiten von Einstellungen, löschen, Ändern der Sicherheit</p></td>
    </tr>
    </tbody>
    </table>

     

-   Die Mitgliedschaft in der Gruppe Richtlinien Ersteller-Besitzer sollte eingeschränkt sein, soit wird nicht verwendet, um die AGPM-Verwaltung des Zugriffs auf GPOs zu umgehen. (Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gruppenrichtlinienobjekte** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, klicken Sie auf **Delegierung**, und konfigurieren Sie dann die Einstellungen, um die Anforderungen Ihrer Organisation zu erfüllen.)

### Weitere Verweise

-   [Konfigurieren von Advanced Group Policy Management](configuring-advanced-group-policy-management-agpm40.md)

 

 





