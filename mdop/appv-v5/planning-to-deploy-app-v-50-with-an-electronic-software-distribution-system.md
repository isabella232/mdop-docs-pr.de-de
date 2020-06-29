---
title: Planen der Bereitstellung von App-V 5.0 mit einem elektronischen Softwareverteilungssystem
description: Planen der Bereitstellung von App-V 5.0 mit einem elektronischen Softwareverteilungssystem
author: dansimp
ms.assetid: 8cd3f1fb-b84e-4260-9e72-a14d01e7cadf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ca441820be7e6759e65902aea18b2db7f989e8f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804952"
---
# Planen der Bereitstellung von App-V 5.0 mit einem elektronischen Softwareverteilungssystem


Wenn Sie ein elektronisches Softwareverteilungssystem zum Bereitstellen von App-V-Paketen verwenden, überprüfen Sie die folgenden Planungsüberlegungen. Informationen zur Verwendung von System Center Configuration Manager zum Bereitstellen von App-V finden Sie unter [Einführung in die Anwendungsverwaltung in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816).

Überprüfen Sie die folgenden Komponenten-und Architektur Anforderungen, die bei der Verwendung von ESD zum Bereitstellen von App-V-Paketen gelten:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Bereitstellungsanforderung oder-Option</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Der App-V-Verwaltungsserver, die Verwaltungsdatenbank und der Veröffentlichungsserver sind nicht erforderlich.</p></td>
<td align="left"><p>Diese Funktionen werden von der implementierten ESD-Lösung gehandhabt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sie können den App-V-Berichtsserver und die Berichtsdatenbank nebeneinander mit dem ESD bereitstellen.</p></td>
<td align="left"><p>Die parallele Bereitstellung ermöglicht es Ihnen, Daten zu sammeln und Berichte zu generieren.</p>
<p>Wenn Sie den App-v-Client zum Senden von Berichtsinformationen aktivieren und nicht den App-v-Berichtsserver verwenden, werden die Berichtsdaten in zugehörigen XML-Dateien gespeichert.</p></td>
</tr>
</tbody>
</table>

 






 

 





