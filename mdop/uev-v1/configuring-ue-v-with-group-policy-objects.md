---
title: Konfigurieren von UE-V mit Gruppenrichtlinienobjekten
description: Konfigurieren von UE-V mit Gruppenrichtlinienobjekten
author: dansimp
ms.assetid: 5c9be706-a05f-4397-9a38-e6b73ebff1e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e479e6bef1a2b38cf822ffca19ed4220b0c59fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811911"
---
# Konfigurieren von UE-V mit Gruppenrichtlinienobjekten


Einige Gruppenrichtlinieneinstellungen für Microsoft User Experience Virtualization (UE-V) können für Computer definiert werden, andere können für benutzerdefiniert werden. Die Konfigurationsrichtlinien Einstellungen des UE-V-Agents können für Computer oder Benutzerdefiniert werden. Informationen zum Installieren von ADMX-Dateien für UE-v-Gruppenrichtlinien finden Sie unter [Installieren der ADMX-Vorlagen für UE-v-Gruppenrichtlinien](installing-the-ue-v-group-policy-admx-templates.md).

Die folgenden Richtlinieneinstellungen können für UE-V konfiguriert werden:

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Name der Richtlinieneinstellung</strong></p></td>
<td align="left"><p><strong>Ziel</strong></p></td>
<td align="left"><p><strong>Beschreibung der Richtlinieneinstellung</strong></p></td>
<td align="left"><p><strong>Konfigurationsoptionen</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Verwenden der Benutzeroberflächen-Virtualisierung (UE-V)</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Mit dieser Richtlinieneinstellung können Sie die Virtualisierung der Benutzeroberfläche (UE-V) aktivieren oder deaktivieren.</p></td>
<td align="left"><p>Aktivieren oder deaktivieren Sie diese Richtlinieneinstellung.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Speicherpfad für Einstellungen</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Diese Richtlinieneinstellung konfiguriert, wo die Benutzereinstellungen gespeichert werden.</p></td>
<td align="left"><p>Bereitstellen eines UNC-Pfads (Universal Naming Convention) und von Variablen wie \Server\SettingsShare%username%.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Katalogpfad für Einstellungs Vorlagen</p></td>
<td align="left"><p>Nur Computer</p></td>
<td align="left"><p>Diese Richtlinieneinstellung konfiguriert, wo die Speicherort Vorlagen für benutzerdefinierte Einstellungen gespeichert werden. Mit dieser Richtlinieneinstellung wird auch konfiguriert, ob der Katalog zum Ersetzen der Microsoft-Standardvorlagen verwendet wird, die mit dem UE-V-Agent installiert werden.</p></td>
<td align="left"><p>Stellen Sie einen UNC-Pfad (Universal Naming Convention) wie \Server\TemplateShare oder einen Ordnerspeicherort auf dem Computer bereit.</p>
<p></p>
<p>Aktivieren Sie das Kontrollkästchen, um die standardmäßigen Microsoft-Vorlagen zu ersetzen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Verwenden Sie keine Offline Dateien</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Mit dieser Richtlinieneinstellung können Sie konfigurieren, ob UE-V das Windows-Feature "Offline Dateien" verwendet. Mit dieser Richtlinieneinstellung können Sie auch die Benachrichtigung aktivieren, wenn der Import von Benutzereinstellungen verzögert wird.</p></td>
<td align="left"><p>Aktivieren Sie diese Einstellung, um den UE-V-Agent so zu konfigurieren, dass keine Offlinedateien verwendet werden.</p>
<p></p>
<p>Geben Sie an, ob Benachrichtigungen erfolgen sollen, wenn der Import von Einstellungen verzögert wird.</p>
<p></p>
<p>Geben Sie die Dauer in Sekunden an, die gewartet werden soll, bevor die Benachrichtigung angezeigt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Synchronisierungs Timeout</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Mit dieser Richtlinieneinstellung wird die Anzahl der Millisekunden konfiguriert, die der Computer vor einem Timeout wartet, wenn Benutzereinstellungen vom Speicherort der Remoteeinstellungen abgerufen werden. Wenn der Remotespeicher Standort nicht verfügbar ist, wird der Anwendungsstart um diese Zahl von Millisekunden verzögert.</p></td>
<td align="left"><p>Geben Sie das bevorzugte Synchronisierungs Timeout in Millisekunden an. Der Standardwert von 2000 Millisekunden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Warnungsschwellenwert für Paketgröße</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Mit dieser Richtlinieneinstellung können Sie den UE-V-Agent so konfigurieren, dass er meldet, wenn die Dateigröße eines Einstellungen-Pakets einen definierten Schwellenwert erreicht.</p></td>
<td align="left"><p>Der bevorzugte Schwellenwert für die Größe der Einstellungs Pakete in Kilobyte angegeben.</p>
<p>Standardmäßig hat der UE-V-Agent keinen Schwellenwert für die Paketdatei Größe.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Einstellungen für Roaming-Anwendungen</p></td>
<td align="left"><p>Nur für Benutzer</p></td>
<td align="left"><p>Diese Richtlinieneinstellung konfiguriert das Roaming der Benutzereinstellungen von Anwendungen.</p></td>
<td align="left"><p>Wählen Sie aus, welche Windows-Einstellungen zwischen Computern durchlaufen sollen.</p>
<p>Standardmäßig werden die Benutzereinstellungen von Anwendungen mit der von UE-V bereitgestellten Einstellungs Vorlage zwischen Computern durchsucht.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Roaming-Windows-Einstellungen</p></td>
<td align="left"><p>Nur für Benutzer</p></td>
<td align="left"><p>Diese Richtlinieneinstellung konfiguriert das Roaming von Windows-Einstellungen.</p></td>
<td align="left"><p>Wählen Sie aus, welche Anwendungen zwischen Computern durchlaufen sollen.</p>
<p>Standardmäßig werden Windows-Designs zwischen Computern der gleichen Betriebssystemversion durchsucht. Die Windows-Desktopeinstellungen und die Einstellungen für den erleichterten Zugriff werden nicht durchlaufen.</p></td>
</tr>
</tbody>
</table>

 

**So konfigurieren Sie computerbezogene Richtlinien**

1.  Verwenden Sie die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) auf dem Domänencontrollercomputer, der Gruppenrichtlinien für UE-V-Computer verwaltet. Navigieren Sie zu **Computer Konfiguration**, wählen Sie **Richtlinien**aus, wählen Sie **Administrative Vorlagen**aus, klicken Sie auf **Windows-Komponenten**, und wählen Sie dann **Microsoft User Experience Virtualization**aus.

2.  Wählen Sie die zu bearbeitende Richtlinieneinstellung aus.

**So konfigurieren Sie benutzerbezogene Richtlinien**

1.  Verwenden Sie die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder das erweiterte Tool für die Gruppenrichtlinienverwaltung (AGPM) im Microsoft Desktop Optimization Pack (MDOP) auf dem Domänencontrollercomputer, der die Gruppenrichtlinie für UE-V verwaltet. Navigieren Sie zu **Benutzerkonfiguration**, wählen Sie **Richtlinien**aus, wählen Sie **Administrative Vorlagen**aus, klicken Sie auf **Windows-Komponenten**, und wählen Sie dann **Microsoft User Experience Virtualization**aus.

2.  Wählen Sie die bearbeitete Richtlinieneinstellung aus.

Der UE-V-Agent verwendet die folgende Rangfolge, um die Synchronisierung zu ermitteln.

**Rangfolge der UE-V-Einstellungen**

1.  Benutzerbezogene Einstellungen, die von Gruppenrichtlinien verwaltet werden – diese Konfigurationseinstellungen werden im Registrierungsschlüssel nach Gruppenrichtlinie unter gespeichert `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .

2.  Von Gruppenrichtlinien verwaltete Computer gesteuerte Einstellungen – diese Konfigurationseinstellungen werden im Registrierungsschlüssel nach Gruppenrichtlinie unter gespeichert `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .

3.  Vom aktuellen Benutzer mithilfe von PowerShell oder WMI definierte Konfigurationseinstellungen – diese Konfigurationseinstellungen werden vom UE-V-Agent unter diesem Registrierungsspeicherort gespeichert: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .

4.  Die für den Computer mit PowerShell oder WMI definierten Konfigurationseinstellungen. Diese Konfigurationseinstellungen werden vom UE-V-Agent unter dem gespeichert `HKEY_LOCAL_MACHINE \Software\Microsoft\Uev\Agent\Configuration` .

## Verwandte Themen


[Verwalten von UE-V 1.0](administering-ue-v-10.md)

[Vorgänge für UE-V 1.0](operations-for-ue-v-10.md)

 

 





