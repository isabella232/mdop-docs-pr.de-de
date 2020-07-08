---
title: So stellen Sie den MBAM-Client über eine Befehlszeile bereit
description: So stellen Sie den MBAM-Client über eine Befehlszeile bereit
author: dansimp
ms.assetid: ac1d4ffe-c26d-41c9-9737-a4f2b37fde24
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 416d76ad876c5114e3a8764111b6a15c879b13b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810585"
---
# So stellen Sie den MBAM-Client über eine Befehlszeile bereit


Sie können eine Befehlszeile zum Bereitstellen der Microsoft BitLocker-Client Software für die Verwaltung und Überwachung (MBAM) verwenden.

## Befehlszeile zum Bereitstellen der MBAM-Client Software


Geben Sie an der Eingabeaufforderung den folgenden Befehl ein, um den Endbenutzer-Lizenzvertrag beim Bereitstellen der MBAM-Client Software automatisch zu akzeptieren.

**MBAMClientSetup.exe/acceptEula = ja**

**Hinweis**  Die Befehlszeilenoptionen **/Ju** und **/JM** werden nicht unterstützt und können nicht zum Installieren der MBAM-Client Software verwendet werden.

 

Geben Sie an der Eingabeaufforderung den folgenden Befehl ein, um das MSP zu extrahieren und zu installieren:

**MBAMClientSetup.exe/Extract- &lt; Pfad zum Extrahieren von MSI &gt; /acceptEula = Yes**

Installieren Sie dann die MSI-Installation im Hintergrund, indem Sie den folgenden Befehl ausführen:

**msiexec/i- &lt; Pfad zu extrahierten MSI- &gt; /qb ALLUSERS = 1 REBOOT = ReallySuppress**

**Hinweis**  Ab MBAM 2,5 SP1 ist eine separate MSI-Version nicht mehr im MBAM-Produkt enthalten. Sie können jedoch die MSI-Datei aus der ausführbaren Datei (. exe) extrahieren, die im Lieferumfang des Produkts enthalten ist, nachdem Sie den EULA angenommen haben.

 

## <a href="" id="optin-for-microsoft-updates-1-command-line-option"></a>Optin \ _FOR \ _MICROSOFT \ _UPDATES = 1 Befehlszeilenoption


Sie können bei der Clientsoftwareinstallation optional die Befehlszeilenoption angeben `OPTIN_FOR_MICROSOFT_UPDATES=1` , um Microsoft-Updates auf Clientcomputern automatisch zu installieren. Wenn Sie diese Option angeben, wird Microsoft Update automatisch gestartet, und Sie suchen nach verfügbaren Updates, die nach Abschluss der Client Software Installation installiert werden.

Sie können diese Befehlszeilenoption mit einer der folgenden Installationsmethoden verwenden.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Installieren der MBAM-Client Software mithilfe von</th>
<th align="left">Beispiel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>MBAMClientSetup.exe</strong></p></td>
<td align="left"><p><strong>MbamClientSetup.exe OPTIN_FOR_MICROSOFT_UPDATES = 1</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>msiexec/i MBAMClient.msi</strong></p></td>
<td align="left"><p><strong>msiexec/i MBAMClient.msi OPTIN_FOR_MICROSOFT_UPDATES = 1</strong></p></td>
</tr>
</tbody>
</table>

 


## Verwandte Themen


[Bereitstellen des MBAM 2.5-Clients](deploying-the-mbam-25-client.md)

 

 
## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




