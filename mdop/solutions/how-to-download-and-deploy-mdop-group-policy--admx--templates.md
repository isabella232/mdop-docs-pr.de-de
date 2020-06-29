---
title: Herunterladen und Bereitstellen von MDOP-Gruppenrichtlinienvorlagen (ADMX-Dateien)
description: Herunterladen und Bereitstellen von MDOP-Gruppenrichtlinienvorlagen (ADMX-Dateien)
author: dansimp
ms.assetid: fdb64505-6c66-4fdf-ad74-a6a161191e3f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 5bc5f8d536c113ccbc0a1931e6c7e4ed3c7a9a37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812043"
---
# Herunterladen und Bereitstellen von MDOP-Gruppenrichtlinienvorlagen (ADMX-Dateien)


Sie können die Funktionseinstellungen bestimmter Microsoft Desktop Optimization Pack (MDOP)-Technologien (beispielsweise App-v, UE-v oder MBAM) mithilfe von Gruppenrichtlinienvorlagen, den ADMX-und ADML-Dateien verwalten. MDOP-Gruppenrichtlinienvorlagen stehen in einer selbstextrahierenden, komprimierten Datei, gruppiert nach Technologie und Version, zum Download zur Verfügung.

## MDOP-Gruppenrichtlinienvorlagen

**Herunterladen und Bereitstellen der MDOP-Gruppenrichtlinienvorlagen**

1. Herunterladen der neuesten [Vorlagen für MDOP-Gruppenrichtlinien](https://www.microsoft.com/download/details.aspx?id=55531) 

2. Erweitern Sie die heruntergeladene CAB-Datei, indem Sie `expand <download_folder>\MDOP_ADMX_Templates.cab -F:* <destination_folder>`

   **Warnung**  
   Extrahieren Sie die Vorlagen nicht direkt in das Bereitstellungsverzeichnis für Gruppenrichtlinien. In dieser Datei sind mehrere Technologien und Versionen gebündelt.

3. Suchen Sie im extrahierten Ordner nach der Datei "Technology-Version. ADMX". Bestimmte MDOP-Technologien verfügen über mehrere Gruppenrichtlinienobjekte (Group Policy Objects, GPOs). MBAM enthält beispielsweise MBAM-Verwaltungseinstellungen und MBAM-Benutzereinstellungen.

4. Suchen Sie die entsprechende ADML-Datei nach Sprache-Kultur (d *-US* für Englisch-Vereinigte Staaten).

5. Kopieren Sie die ADMX-und ADML-Dateien in einen Richtlinien Definitions Ordner. Je nachdem, wo Sie die Vorlagen speichern, können Sie die Gruppenrichtlinieneinstellungen auf dem lokalen Gerät oder auf einem beliebigen Computer in der Domäne konfigurieren.

   - **Lokale Dateien:** Wenn Sie die Gruppenrichtlinieneinstellungen auf dem lokalen Gerät konfigurieren möchten, kopieren Sie die Vorlagendateien an die folgenden Speicherorte:

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

   - **Zentraler Domänenspeicher:** Wenn Sie die Konfiguration der Gruppenrichtlinieneinstellungen durch einen Gruppenrichtlinienadministrator von einem beliebigen Computer in der Domäne aus aktivieren möchten, kopieren Sie Dateien an die folgenden Speicherorte auf dem Domänencontroller:

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
   <td align="left"><p><code>%systemroot%</code>&lt;starke &gt; sysvol\domain\policies\PolicyDefinitions</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Gruppenrichtlinien-Sprachdatei (ADML)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;starke &gt; sysvol\domain\policies\PolicyDefinitions [MUIculture]</strong><code>[MUIculture]</code></p>
   <p>Beispielsweise wird die sprachspezifische ADML-Datei in US-Englisch in%SystemRoot%\sysvol\domain\policies\PolicyDefinitions\en-US. gespeichert.</p></td>
   </tr>
   </tbody>
   </table>

6. Bearbeiten Sie die Gruppenrichtlinieneinstellungen mithilfe von Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM), um Gruppenrichtlinieneinstellungen für die MDOP-Technologie zu konfigurieren

### MDOP-Gruppenrichtlinien nach Technologie

Weitere Informationen zu unterstützten MDOP-Gruppenrichtlinien finden Sie in der jeweiligen Dokumentation zur Technologie.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">MDOP-Technologie</th>
<th align="left">Versions Pakete</th>
<th align="left">Anmerkungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Application Virtualization (App-V)</strong></p></td>
<td align="left"><p>App-v 5,0 und App-v 5,0-Service Packs</p></td>
<td align="left"><p><a href="../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md" data-raw-source="[How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy](../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)">So ändern Sie die App-V 5.0-Clientkonfiguration mithilfe der ADMX-Vorlage und -Gruppenrichtlinie</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>User Experience Virtualization (UE-V)</strong></p></td>
<td align="left"><p>UE-v 2,0 und UE-v 2,1</p></td>
<td align="left"><p><a href="../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md" data-raw-source="[Configuring UE-V 2.x with Group Policy Objects](../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md)">Konfigurieren von UE-V 2. x mit Gruppenrichtlinienobjekten</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>UE-V 1,0 einschließlich 1,0 SP1</p></td>
<td align="left"><p><a href="../uev-v1/configuring-ue-v-with-group-policy-objects.md" data-raw-source="[Configuring UE-V with Group Policy Objects](../uev-v1/configuring-ue-v-with-group-policy-objects.md)">Konfigurieren von UE-V mit Gruppenrichtlinienobjekten</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Microsoft BitLocker Administration and Monitoring (MBAM)</strong></p></td>
<td align="left"><p>MBAM 2,5</p></td>
<td align="left"><p><a href="../mbam-v25/planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](../mbam-v25/planning-for-mbam-25-group-policy-requirements.md)">Planen der Gruppenrichtlinienanforderungen für MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>MBAM 2,0 einschließlich 2,0 SP1</p></td>
<td align="left"><p><a href="../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md)">Planen der Gruppenrichtlinienanforderungen für MBAM 2.0</a></p>
<p><a href="../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md)">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.0</a></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>MBAM 1,0</p></td>
<td align="left"><p><a href="../mbam-v1/how-to-edit-mbam-10-gpo-settings.md" data-raw-source="[How to Edit MBAM 1.0 GPO Settings](../mbam-v1/how-to-edit-mbam-10-gpo-settings.md)">So bearbeiten Sie die GPO-Einstellungen für MBAM 1.0</a></p></td>
</tr>
</tbody>
</table>

 

 

 





