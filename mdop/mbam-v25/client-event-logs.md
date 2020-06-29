---
title: Client-Ereignisprotokolle
description: Client-Ereignisprotokolle
author: dansimp
ms.assetid: d5c2f270-db6a-45f1-8557-8c6fb28fd568
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7324d07bf018944fcbe24168bba2e9abea9cea41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810408"
---
# Client-Ereignisprotokolle

MBAM-Client Ereignisprotokolle befinden sich in der Ereignisanzeige – Anwendungen und Dienstprotokolle – Microsoft – Windows – MBAM-operativer Pfad.
Die folgende Tabelle enthält Ereignis-IDs, die auf dem MBAM-Client auftreten können.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Ereignis-ID</th>
<th align="left">Kanal</th>
<th align="left">Ereignissymbol</th>
<th align="left">Meldung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>1</p></td>
<td align="left"><p>Betriebs</p></td>
<td align="left"><p>VolumeEnactmentSuccessful</p></td>
<td align="left"><p>Die MBAM-Richtlinien wurden erfolgreich angewendet.</p></td>
</tr>
<tr class="even">
<td align="left"><p>2</p></td>
<td align="left"><p>Administrator</p></td>
<td align="left"><p>VolumeEnactmentFailed</p></td>
<td align="left"><p>Beim Anwenden von MBAM-Richtlinien ist ein Fehler aufgetreten.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>3</p></td>
<td align="left"><p>Betriebs</p></td>
<td align="left"><p>TransferStatusDataSuccessful</p></td>
<td align="left"><p>Die Daten für den Verschlüsselungsstatus wurden erfolgreich gesendet.</p></td>
</tr>
<tr class="even">
<td align="left"><p>4</p></td>
<td align="left"><p>Administrator</p></td>
<td align="left"><p>TransferStatusDataFailed</p></td>
<td align="left"><p>Beim Senden von Verschlüsselungsstatus Daten ist ein Fehler aufgetreten.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>8</p></td>
<td align="left"><p>Administrator</p></td>
<td align="left"><p>SystemVolumeNotFound</p></td>
<td align="left"><p>Das System Volume fehlt. Systemvolume ist erforderlich, um das Betriebssystemlaufwerk zu verschlüsseln.</p></td>
</tr>
<tr class="even">
<td align="left"><p>9</p></td>
<td align="left"><p>Administrator</p></td>
<td align="left"><p>TPMNotFound</p></td>
<td align="left"><p>Die TPM-Hardware fehlt. Zum Verschlüsseln des Betriebssystemlaufwerks mit jeder TPM-Schutzkomponente ist TPM erforderlich.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>10</p></td>
<td align="left"><p>Administrator</p></td>
<td align="left"><p>MachineHWExempted</p></td>
<td align="left"><p>Der Computer ist von der Verschlüsselung ausgenommen. Hardwarestatus des Computers: ausgenommen</p></td>
</tr>
<tr class="even">
<td align="left"><p>11</p></td>
<td align="left"><p>Administrator</p></td>
<td align="left"><p>MachineHWUnknown</p></td>
<td align="left"><p>Der Computer ist von der Verschlüsselung ausgenommen. Hardwarestatus des Computers: unbekannt</p></td>
</tr>
<tr class="odd">
<td align="left"><p>12</p></td>
<td align="left"><p>Administrator</p></td>
<td align="left"><p>HWCheckFailed</p></td>
<td align="left"><p>Fehler bei der Hardware Befreiungs Prüfung.</p></td>
</tr>
<tr class="even">
<td align="left"><p>13</p></td>
<td align="left"><p>Administrator</p></td>
<td align="left"><p>UserIsExempted</p></td>
<td align="left"><p>Der Benutzer ist von der Verschlüsselung ausgenommen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>14</p></td>
<td align="left"><p>Administrator</p></td>
<td align="left"><p>UserIsWaiting</p></td>
<td align="left"><p>Der Benutzer hat eine Ausnahme beantragt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>15</p></td>
<td align="left"><p>Administrator</p></td>
<td align="left"><p>UserExemptionCheckFailed</p></td>
<td align="left"><p>Fehler bei der Benutzer Befreiungs Prüfung.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>16</p></td>
<td align="left"><p>Administrator</p></td>
<td align="left"><p>UserPostponed</p></td>
<td align="left"><p>Der Benutzer hat den Verschlüsselungsprozess verschoben.</p></td>
</tr>
<tr class="even">
<td align="left"><p>17</p></td>
<td align="left"><p>Administrator</p></td>
<td align="left"><p>TPMInitializationFailed</p></td>
<td align="left"><p>Fehler bei der TPM-Initialisierung. Der Benutzer hat die BIOS-Änderungen abgelehnt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>18</p></td>
<td align="left"><p>Administrator</p></td>
<td align="left"><p>CoreServiceDown</p></td>
<td align="left"><p>Es konnte keine Verbindung mit dem MBAM-Wiederherstellungs-und-Hardware Dienst hergestellt werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>19</p></td>
<td align="left"><p>Betriebs</p></td>
<td align="left"><p>CoreServiceUp</p></td>
<td align="left"><p>Erfolgreich mit dem MBAM-Wiederherstellungs-und-Hardware Dienst verbunden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>20</p></td>
<td align="left"><p>Administrator</p></td>
<td align="left"><p>PolicyMismatch</p></td>
<td align="left"><p>Die MBAM-Richtlinie ist in Konflikt oder fehlerhaft.</p></td>
</tr>
<tr class="even">
<td align="left"><p>21</p></td>
<td align="left"><p>Administrator</p></td>
<td align="left"><p>ConflictingOSVolumePolicies</p></td>
<td align="left"><p>Erkannte System-Volume-Verschlüsselungsrichtlinien Konflikte. Überprüfen Sie die BitLocker-und MBAM-Richtlinien in Bezug auf Betriebssystemlaufwerks Schutz.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>22</p></td>
<td align="left"><p>Administrator</p></td>
<td align="left"><p>ConflictingFDDVolumePolicies</p></td>
<td align="left"><p>Die Datenträger-Verschlüsselungsrichtlinien für festgelegte Daten sind Konflikt. Überprüfen Sie die BitLocker-und MBAM-Richtlinien für Diskettenlaufwerks Schutz.</p></td>
</tr>
<tr class="even">
<td align="left"><p>27</p></td>
<td align="left"><p>Administrator</p></td>
<td align="left"><p>EncryptionFailedNoDra</p></td>
<td align="left"><p>Beim Verschlüsseln ist ein Fehler aufgetreten. Eine DRA-Beschützer (Data Recovery Agent) ist im FIPS-Modus für Pre-Windows 8,1-Computer erforderlich.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>28</p></td>
<td align="left"><p>Betriebs</p></td>
<td align="left"><p>TpmOwnerAuthEscrowed</p></td>
<td align="left"><p>Das TPM-OwnerAuth wurde gesperrt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>29</p></td>
<td align="left"><p>Betriebs</p></td>
<td align="left"><p>RecoveryKeyEscrowed</p></td>
<td align="left"><p>Der BitLocker-Wiederherstellungsschlüssel für das Volume wurde gesperrt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>30</p></td>
<td align="left"><p>Betriebs</p></td>
<td align="left"><p>RecoveryKeyReset</p></td>
<td align="left"><p>Der BitLocker-Wiederherstellungsschlüssel für das Volume wurde aktualisiert.</p></td>
</tr>
<tr class="even">
<td align="left"><p>31</p></td>
<td align="left"><p>Betriebs</p></td>
<td align="left"><p>EnforcePolicyDateSet</p></td>
<td align="left"><p>Das Datum der Richtlinienerzwingung <em> &lt; &gt; </em> wurde für die Lautstärke eingestellt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>32</p></td>
<td align="left"><p>Betriebs</p></td>
<td align="left"><p>EnforcePolicyDateCleared</p></td>
<td align="left"><p>Das Datum der Richtlinie erzwingen wurde <em> &lt; &gt; </em> für das Volume gelöscht.</p></td>
</tr>
<tr class="even">
<td align="left"><p>33</p></td>
<td align="left"><p>Betriebs</p></td>
<td align="left"><p>TpmLockOutResetSucceeded</p></td>
<td align="left"><p>TPM-Sperrung erfolgreich zurückgesetzt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>34</p></td>
<td align="left"><p>Administrator</p></td>
<td align="left"><p>TpmLockOutResetFailed</p></td>
<td align="left"><p>Fehler beim Zurücksetzen der TPM-Sperrung.</p></td>
</tr>
<tr class="even">
<td align="left"><p>35</p></td>
<td align="left"><p>Betriebs</p></td>
<td align="left"><p>TpmOwnerAuthRetrievalSucceeded</p></td>
<td align="left"><p>TPM-OwnerAuth von MBAM-Diensten erfolgreich abgerufen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>36</p></td>
<td align="left"><p>Administrator</p></td>
<td align="left"><p>TpmOwnerAuthRetrievalFailed</p></td>
<td align="left"><p>Fehler beim Abrufen der TPM-OwnerAuth von MBAM-Diensten.</p></td>
</tr>
<tr class="even">
<td align="left"><p>37</p></td>
<td align="left"><p>Administrator</p></td>
<td align="left"><p>WmiProviderDllSearchPathUpdateFailed</p></td>
<td align="left"><p>Fehler beim Aktualisieren des dll-Such Pfads für den WMI-Anbieter.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>38</p></td>
<td align="left"><p>Administrator</p></td>
<td align="left"><p>TimedOutWaitingForWmiProvider</p></td>
<td align="left"><p>Agent-Stopp-Timeout beim Warten auf die MBAM-WMI-Anbieterinstanz.</p></td>
</tr>
<tr class="even">
<td align="left"><p>39</p></td>
<td align="left"><p>Betriebs</p></td>
<td align="left"><p>RemovableDriveMounted</p></td>
<td align="left"><p>Das Wechsellaufwerk wurde bereitgestellt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>40</p></td>
<td align="left"><p>Betriebs</p></td>
<td align="left"><p>RemovableDriveDismounted</p></td>
<td align="left"><p>Das Wechsellaufwerk wurde nicht bereitgestellt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>41</p></td>
<td align="left"><p>Betriebs</p></td>
<td align="left"><p>FailedToEnactEndpointUnreachable</p></td>
<td align="left"><p>Beim Herstellen einer Verbindung mit dem MBAM-Wiederherstellungs-und-Hardware Dienst wurde verhindert, dass MBAM-Richtlinien erfolgreich auf das Volume angewendet wurden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>42</p></td>
<td align="left"><p>Betriebs</p></td>
<td align="left"><p>FailedToEnactLockedVolume</p></td>
<td align="left"><p>Gesperrter Lautstärke Status hat verhindert, dass MBAM-Richtlinien erfolgreich auf das Volume angewendet werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>43</p></td>
<td align="left"><p>Betriebs</p></td>
<td align="left"><p>TransferStatusDataFailedEndpointUnreachable</p></td>
<td align="left"><p>Wenn keine Verbindung mit dem MBAM-Compliance-und-Statusdienst hergestellt wurde, wurde die Übertragung von Verschlüsselungsstatus Daten verhindert.</p></td>
</tr>
</tbody>
</table>

 


## Verwandte Themen
[Technische Referenz für MBAM2.5](technical-reference-for-mbam-25.md)

[Serverereignisprotokolle](server-event-logs.md)

 


## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





