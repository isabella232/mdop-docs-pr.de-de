---
title: Kopieren die Gruppenrichtlinienvorlagen für MBAM 2.5
description: Kopieren die Gruppenrichtlinienvorlagen für MBAM 2.5
author: dansimp
ms.assetid: e526ecec-07ff-435e-bc90-3084b617b84b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/28/2017
ms.openlocfilehash: a3436552256b1632a11037dc94751207cde89d5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811026"
---
# Kopieren die Gruppenrichtlinienvorlagen für MBAM 2.5


Bevor Sie die MBAM-Client Installation bereitstellen, müssen Sie die MBAM-Gruppenrichtlinienvorlagen, die Gruppenrichtlinieneinstellungen enthalten, die MBAM-Implementierungs Einstellungen für die BitLocker-Laufwerkverschlüsselung definieren, herunterladen. Nachdem Sie die Vorlagen heruntergeladen haben, können Sie die Gruppenrichtlinieneinstellungen so festlegen, dass Sie im gesamten Unternehmen implementiert werden.

## Herunterladen und Bereitstellen der MDOP-Gruppenrichtlinienvorlagen


MDOP-Gruppenrichtlinienvorlagen stehen in einer selbstextrahierenden, komprimierten Datei, gruppiert nach Technologie und Version, zum Download zur Verfügung.

**Herunterladen und Bereitstellen der MDOP-Gruppenrichtlinienvorlagen**

1. Laden Sie die MDOP-Gruppenrichtlinienvorlagen aus den [Microsoft Desktop Optimization Pack-Gruppenrichtlinien-Verwaltungsvorlagen](https://www.microsoft.com/download/details.aspx?id=55531)herunter.

2. Führen Sie die heruntergeladene Datei aus, um die Vorlagenordner zu extrahieren.

   **Warnung**  
   Extrahieren Sie die Vorlagen nicht direkt in das Bereitstellungsverzeichnis für Gruppenrichtlinien. In dieser Datei sind mehrere Technologien und Versionen gebündelt.



3. Suchen Sie im extrahierten Ordner nach der Datei "Technology-Version. ADMX". Bestimmte MDOP-Technologien verfügen über mehrere Gruppenrichtlinienobjekte (Group Policy Objects, GPOs). MBAM enthält beispielsweise MBAM-Verwaltungseinstellungen und MBAM-Benutzereinstellungen.

4. Suchen Sie die entsprechende ADML-Datei nach sprach Kultur (d. *en* für Englisch – USA).

5. Kopieren Sie die ADMX-und ADML-Dateien in einen Richtlinien Definitions Ordner. Je nachdem, wo Sie die Vorlagen speichern, können Sie die Gruppenrichtlinieneinstellungen auf dem lokalen Gerät oder auf einem beliebigen Computer in der Domäne konfigurieren.

   **Lokale Dateien.** Wenn Sie die Gruppenrichtlinieneinstellungen auf dem lokalen Gerät konfigurieren möchten, kopieren Sie die Vorlagendateien an die folgenden Speicherorte:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Dateityp</th>
   <th align="left">Dateispeicherort</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Gruppenrichtlinienvorlage (ADMX)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;starke &gt; PolicyDefinitions</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Gruppenrichtlinien-Sprachdatei (ADML)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;starke &gt; PolicyDefinitions</strong><code>[MUIculture]</code></p></td>
   </tr>
   </tbody>
   </table>



~~~
**Domain central store.** To enable Group Policy settings configuration by a Group Policy administrator from any computer on the domain, copy files to the following locations on the domain controller:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">File type</th>
<th align="left">File location</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Group Policy template (.admx)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Group Policy language file (.adml)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions\[MUIculture]</strong><code>\[MUIculture]</code></p>
<p>For example, the U.S. English ADML language-specific file will be stored in %systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</p></td>
</tr>
</tbody>
</table>
~~~



6. Bearbeiten Sie die Gruppenrichtlinieneinstellungen mithilfe von Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM), um Gruppenrichtlinieneinstellungen für die MDOP-Technologie zu konfigurieren Weitere Informationen finden Sie unter [Bearbeiten der MBAM 2,5-Gruppenrichtlinieneinstellungen](editing-the-mbam-25-group-policy-settings.md) .

   Beschreibungen der Gruppenrichtlinieneinstellungen finden Sie unter [Planen von MBAM 2,5-Gruppenrichtlinienanforderungen](planning-for-mbam-25-group-policy-requirements.md).


## Verwandte Themen


[Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.5](deploying-mbam-25-group-policy-objects.md)


## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






