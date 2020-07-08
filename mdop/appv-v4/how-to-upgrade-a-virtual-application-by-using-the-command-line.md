---
title: So aktualisieren Sie eine virtuelle Anwendung über die Befehlszeile
description: So aktualisieren Sie eine virtuelle Anwendung über die Befehlszeile
author: dansimp
ms.assetid: 83c97767-6ea1-42aa-b411-ccc9fa61cf81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8612deb31a1692dd85cfee88ca4b18cbc5ac2ab2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806716"
---
# So aktualisieren Sie eine virtuelle Anwendung über die Befehlszeile


Gehen Sie wie folgt vor, um eine virtuelle Anwendung mithilfe einer Befehlszeile zu aktualisieren.

**So aktualisieren Sie eine virtuelle Anwendung**

1.  Klicken Sie auf dem Computer, auf dem Application Virtualization (App-V) Sequencer ausgeführt wird, zum Öffnen der Eingabeaufforderung auf **Start**, **Ausführen**und geben Sie **cmd**ein. Klicken Sie auf **OK**.

2.  Geben Sie an der Eingabeaufforderung den Ort an, an dem der App-V-Sequencer installiert ist. Geben Sie beispielsweise an der Eingabeaufforderung Folgendes ein: **CD c:\\Programme c:\\Programme\\Microsoft Application Virtualization Sequencer**.

3.  Geben Sie an der Eingabeaufforderung den folgenden Befehl ein, und ersetzen Sie den Text in Anführungszeichen durch ihre Werte:

    `SFTSequencer /UPGRADE:"pathtosourceSPRJ" /INSTALLPACKAGE:"pathtoUpgradeInstaller" /DECODEPATH:"pathtodecodefolder" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **Hinweis:**  
    Sie können zusätzliche Parameter über die Befehlszeile angeben, abhängig von der Komplexität der Anwendung, die Sie aktualisieren. Eine vollständige Liste der Parameter, die für die Verwendung mit dem App-V-Sequenzer verfügbar sind, finden Sie unter [Befehlszeilenparameter für Sequencer](sequencer-command-line-parameters.md).



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
<td align="left"><p><em>pathtosourceSPRJ</em></p></td>
<td align="left"><p>Specifies the directory location of the virtual application to be upgraded.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtoUpgradeInstaller</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an upgrade to the application.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodecodefolder</em></p></td>
<td align="left"><p>Specify the directory in which to unpack the SFT file.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. Drücken **Sie die Eingabe**Taste.

## Verwandte Themen


[Erstellen oder Aktualisieren virtueller Anwendungen mit dem App-V-Sequenzer](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

[Sequencer-Befehlszeilenfehlercodes](sequencer-command-line-error-codes.md)

[Sequencer Befehlszeilenparameter](sequencer-command-line-parameters.md)









