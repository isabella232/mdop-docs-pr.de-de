---
title: So sequenzieren Sie ein neues Anwendungspaket über die Befehlszeile
description: So sequenzieren Sie ein neues Anwendungspaket über die Befehlszeile
author: dansimp
ms.assetid: de72912b-d9e7-45b5-a601-12528f1a4cac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2dd638a7e4765cedbf1d8050626fb8cc54b2ce8b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806803"
---
# So sequenzieren Sie ein neues Anwendungspaket über die Befehlszeile


Sie können eine Befehlszeile verwenden, um eine neue Anwendung zu sequenzieren. Die Verwendung einer Befehlszeile ist hilfreich, wenn Sie eine große Anzahl von virtuellen Anwendungen erstellen müssen oder wenn Sie sequenzierte Anwendungen regelmäßig erstellen müssen.

**Wichtig**  
Die Befehlszeilen-Sequenzierung ermöglicht nur die standardmäßige Sequenzierung. Wenn Sie die Standardinstallationseinstellungen für die von Ihnen sequenzierte Anwendung ändern müssen, müssen Sie entweder die virtuelle Anwendung manuell ändern oder die virtuelle Anwendung mithilfe von Application Virtualization (App-V) Sequencer aktualisieren. Weitere Informationen zum Aktualisieren einer virtuellen Anwendung mithilfe von App-V Sequencer finden Sie unter [Aktualisieren einer vorhandenen virtuellen Anwendung](how-to-upgrade-an-existing-virtual-application.md).



Gehen Sie wie folgt vor, um eine virtuelle Anwendung mithilfe der Befehlszeile zu erstellen.

**So Sequenzieren Sie eine Anwendung mithilfe der Befehlszeile**

1.  Öffnen Sie auf dem Computer, auf dem der App-V-Sequencer ausgeführt wird, die Eingabeaufforderung, indem Sie **Start**, **Ausführen**und dann **cmd**eingeben. Klicken Sie auf **OK**.

2.  Verwenden Sie die Eingabeaufforderung, um den Speicherort anzugeben, an dem der App-V-Sequencer installiert ist. Geben Sie beispielsweise an der Eingabeaufforderung Folgendes ein: **CD c:\\Programme c:\\Programme\\Microsoft Application Virtualization Sequencer**.

3.  Geben Sie an der Eingabeaufforderung den folgenden Befehl ein, und ersetzen Sie den Text in Anführungszeichen durch ihre Werte:

    `SFTSequencer /INSTALLPACKAGE:"pathtoMSI" /INSTALLPATH:"pathtopackageroot" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **Hinweis:**  
    Sie können zusätzliche Parameter mithilfe der Befehlszeile angeben, abhängig von der Komplexität der Anwendung, die Sie sequenzieren. Eine vollständige Liste der Parameter, die für die Verwendung mit dem App-V-Sequenzer verfügbar sind, finden Sie unter [Befehlszeile für Application Virtualization Sequencer](application-virtualization-sequencer-command-line.md).



~~~
Use the value descriptions in the following table to help you determine the actual text you will use in the preceding command.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Value</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em>pathtoMSI</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an application so that it can be sequenced.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtopackageroot</em></p></td>
<td align="left"><p>Specifies the package root directory.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. Drücken **Sie die Eingabe**Taste.

## Verwandte Themen


[So verwalten Sie virtuellen Anwendungen über die Befehlszeile](how-to-manage-virtual-applications-using-the-command-line.md)









