---
title: So ändern Sie die Serverebene für die Protokollierung und die Datenbankparameter
description: So ändern Sie die Serverebene für die Protokollierung und die Datenbankparameter
author: dansimp
ms.assetid: e3ebaee5-6c4c-4aa8-9766-c5aeb00f477a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bb35ac09c5e23f4847662171b68284f868e66dee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807344"
---
# So ändern Sie die Serverebene für die Protokollierung und die Datenbankparameter


Mit den folgenden Verfahren können Sie den Protokolliergrad und die Datenbankprotokoll Parameter aus der Application Virtualization Server-Verwaltungskonsole ändern.

Die folgenden Protokollierungsstufen stehen zur Verfügung:

-   Nur Transaktion

-   Schwerwiegende Fehler

-   Fehler

-   Warnungen/Fehler

-   Informationen/Warnungen/Fehler

-   Ausführliche

**Hinweis**  Aufgrund der Größe der Protokolldatei, die bei Verwendung des **verbose** -Modus erzeugt wird, empfehlen wir, dass Sie keine Produktionsserver mit dieser Protokollierungsstufe ausführen.

 

Die Daten Bank Protokollierungsparameter legen den Daten Bank Treibertyp, die Zugriffsanmeldeinformationen und den Speicherort der Protokollierungsdatenbank fest.

**So ändern Sie den Protokolliergrad für Verwaltungsserver**

1.  Klicken Sie auf den Knoten **Servergruppen** , um die Servergruppen anzuzeigen.

2.  Klicken Sie mit der rechten Maustaste auf die Servergruppe, und wählen Sie **Eigenschaften**aus.

3.  Wählen Sie im Dialogfeld **Eigenschaften** die Registerkarte **Protokollierung** aus.

4.  Wählen Sie im Dialogfeld **Servergruppeneigenschaften** den Server aus, und klicken Sie dann auf **Bearbeiten**.

5.  Wählen Sie im Dialogfeld **Protokollmodul hinzufügen/bearbeiten** den Protokolliergrad in der Dropdownliste **Ereignistyp** aus.

6.  Klicken Sie auf **OK**.

7.  Klicken Sie im Dialogfeld **Server Gruppeneigenschaften** auf **OK** oder auf über **nehmen**.

**So ändern Sie den Protokolliergrad für Streamingserver**

1.  Bearbeiten Sie den folgenden Registrierungsschlüsselwert, um den Protokolliergrad zu ändern:

    -   HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\distributionserver\\loglevel

2.  Wählen Sie einen der folgenden Werte aus, um den Protokolliergrad einzustellen.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Wert</th>
    <th align="left">Protokollierungsstufe</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>0</p></td>
    <td align="left"><p>Nur Transaktionen</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>1</p></td>
    <td align="left"><p>Schwerwiegende Fehler</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>2</p></td>
    <td align="left"><p>Fehler</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>3</p></td>
    <td align="left"><p>Warnungen/Fehler</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>4</p></td>
    <td align="left"><p>Informationen/Warnungen/Fehler</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>5</p></td>
    <td align="left"><p>Ausführliche</p></td>
    </tr>
    </tbody>
    </table>

     

**So ändern Sie Datenbankprotokoll Parameter**

1.  Klicken Sie auf den Knoten **Servergruppen** , um die Servergruppen anzuzeigen.

2.  Klicken Sie mit der rechten Maustaste auf die Servergruppe, und wählen Sie **Eigenschaften**aus.

3.  Wählen Sie im Dialogfeld **Eigenschaften** die Registerkarte **Protokollierung** aus.

4.  Wählen Sie im Dialogfeld **Servergruppeneigenschaften** den Server aus, und klicken Sie dann auf **Bearbeiten**.

5.  Wählen Sie im Dialogfeld **Protokollmodul hinzufügen/bearbeiten** in der Dropdownliste **Datenbanktreiber** einen Datenbanktreiber aus.

6.  Geben Sie einen **DNS-Hostnamen**ein.

7.  Klicken Sie auf das Kontrollkästchen **Port dynamisch bestimmen** , oder geben Sie eine Portnummer in das Feld **Port** ein.

8.  Geben Sie einen **Dienstnamen** in das entsprechende Feld ein.

9.  Klicken Sie auf **OK**.

10. Klicken Sie im Dialogfeld **Server Gruppeneigenschaften** auf **OK** oder auf über **nehmen**.

## Verwandte Themen


[So passen Sie ein Application Virtualization System in der Server Management Console an](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

 

 





