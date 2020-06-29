---
title: Authentifizierung von MED-V-Endbenutzern
description: Authentifizierung von MED-V-Endbenutzern
author: dansimp
ms.assetid: aaf96eb6-91d1-4f4d-9854-5fc73c7ae7ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14c1e95a94f2da76b6b6c5ebd9d4cf14dcf839a7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810825"
---
# Authentifizierung von MED-V-Endbenutzern


Die Authentifizierung von Microsoft Enterprise Desktop Virtualization (MED-V) 2,0-Endbenutzern ist ein sehr wichtiges Sicherheitsproblem. In diesem Kontext bezieht sich die Authentifizierung auf die Überprüfung der Identität des MED-V-Endbenutzers.

Der folgende Abschnitt enthält Informationen und Anleitungen zur Endbenutzer Authentifizierung in MED-V.

## Benutzerauthentifizierung in MED-V


Die Authentifizierung in Med-v erfolgt in der Regel auf zwei Ebenen: Wenn ein Benutzer zuerst auf Med-v und jedes Mal, wenn er sein Kennwort ändert, zugreift.

Je nachdem, wie Sie die Med-v-Einstellungen für die Authentifizierung konfiguriert haben, wird der Endbenutzer in der Regel irgendwann aufgefordert, sein Kennwort einzugeben, entweder beim ersten Start von Med-v oder beim ersten Versuch, eine veröffentlichte Anwendung zu öffnen.

Es gibt verschiedene Aspekte der Endbenutzer Authentifizierung, die Sie steuern können, einschließlich der folgenden:

Ob die Anmeldeinformationen, die der Endbenutzer eingibt, im Anmelde Informations-Manager gespeichert werden

In welcher Weise wird dem Endnutzer die Möglichkeit geboten, sein Kennwort einzugeben und zu speichern

Je nach dem bevorzugten Prozess des Unternehmens für die Verwaltung der Endbenutzer Authentifizierung können Sie angeben, ob die Zwischenspeicherung von Anmeldeinformationen für einen bestimmten MED-V-Arbeitsbereich erfolgt. Das Zwischenspeichern der Anmeldeinformationen eines Endbenutzers ist hilfreich, da er nur einmal für sein Kennwort aufgefordert wird. Wenn es dem Endbenutzer nicht gestattet ist, sein Kennwort zu speichern oder nicht, jedes Mal, wenn Sie eine neue MED-V-Sitzung starten, müssen Sie es erneut eingeben. Wenn beispielsweise MED-V so konfiguriert ist, dass er gestartet wird, wenn sich der Endbenutzer beim Host anmeldet, die Authentifizierung aber deaktiviert ist, wird der Endbenutzer nur einmal während der Anmeldung aufgefordert. In diesem Fall sind Anmeldeinformationen gültig, bis sich der Endbenutzer vom Host abmeldet.

Wenn dies erforderlich ist, können Sie mithilfe des Anmelde Informations-Managers alle gespeicherten Endbenutzeranmeldeinformationen entfernen.

Standardmäßig ist die Speicherung von Anmeldeinformationen deaktiviert, doch Sie können diese Einstellung mithilfe einer der folgenden Methoden ändern:

**Während des Erstellens des MED-V-Arbeitsbereichs Pakets**. Weitere Informationen finden Sie unter [Erstellen eines MED-V-Arbeitsbereichs Pakets](create-a-med-v-workspace-package.md).

**Nachdem Sie den MED-V-Arbeitsbereich bereitgestellt haben**. Bearbeiten Sie den Parameter UxCredentialCacheEnabled des MED-V-Cmdlets, um den Registrierungsschlüssel für die Terminal Dienste einzurichten. Weitere Informationen finden Sie in der Hilfe zu Windows PowerShell.

Nach der Bereitstellung von MED-V Workspace können Sie Ihre Präferenz für die Endbenutzer Authentifizierung festlegen, indem Sie die Terminal Dienste-Richtlinie mit dem Namen DisablePasswordSaving ändern. DisablePasswordSaving steuert, ob das Kontrollkästchen Kennwort speichern im Dialogfenster des RDP-Clients angezeigt wird und ob die Eingabeaufforderung MED-V-Anmeldeinformationen angezeigt wird.

Im folgenden wird der Richtlinienpfad für die Terminal Dienste-Richtlinie mit dem Namen DisablePasswordSaving.

**Regedit**

HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\virtual Machine\\Policies\\DisablePasswordSaving

**Hinweis:**  
Die Änderungen, die Sie an DisablePasswordSaving vornehmen, wirken sich nur auf die RDP-Eingabeaufforderung für einen virtuellen Computer aus.



In der folgenden Tabelle sind die verschiedenen Möglichkeiten für die Konfiguration Ihrer Einstellungen für die Speicherung von Anmeldeinformationen und die Auswirkungen der verschiedenen Konfigurationen aufgeführt:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Wert</th>
<th align="left">Konfiguration</th>
<th align="left">Ergebnis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>DisablePasswordSaving</p></td>
<td align="left"><p><strong>Deaktiviert</strong></p></td>
<td align="left"><p>Die MED-V-Eingabeaufforderung wird angezeigt, und ein Kontrollkästchen zum annehmen ist verfügbar und deaktiviert. Wenn der Endbenutzer das Kontrollkästchen aktiviert, werden die Anmeldeinformationen für die spätere Verwendung zwischengespeichert. Der Endbenutzer hat außerdem den Vorteil, dass nur eine Aufforderung angezeigt wird, wenn das Kennwort abläuft.</p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>Wenn der Endbenutzer das Kontrollkästchen nicht aktiviert, wird anstelle der MED-V-Eingabeaufforderung die RDC-Client Aufforderung (Remote Desktop Connection) angezeigt, und das Kontrollkästchen zum annehmen wird deaktiviert. Wenn der Endbenutzer das Kontrollkästchen aktiviert, werden die RDC-Client Anmeldeinformationen für die spätere Verwendung gespeichert.</p>
<div class="alert">
<strong>Wichtig</strong><br/><p>RDC überprüft keine Anmeldeinformationen, wenn der Endbenutzer Sie eingibt. Wenn der Endbenutzer die Anmeldeinformationen über die RDC-Eingabeaufforderung zwischenspeichert, besteht das Risiko, dass falsche Anmeldeinformationen gespeichert werden. In diesem Fall müssen die falschen Anmeldeinformationen im Windows-Anmelde Informations-Manager gelöscht werden.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>DisablePasswordSaving</p></td>
<td align="left"><p><strong>Aktiviert</strong></p></td>
<td align="left"><div class="alert">
<strong>Hinweis:</strong><br/><p>Diese Konfiguration ist sicherer, da Sie die Zwischenspeicherung von Endbenutzeranmeldeinformationen nicht zulässt.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



Standardmäßig legt die MED-V-Installation einen Registrierungsschlüssel im Gast fest, um die Eingabeaufforderung "Kennwort läuft ab" zu unterdrücken. Der Endbenutzer wird nur zur Eingabe einer Kennwortänderung auf dem Host aufgefordert. Die auf dem Host aktualisierten Anmeldeinformationen werden an den Gast weitergegeben.

**Achtung**  
Wenn Sie Gruppenrichtlinien in Ihrer Umgebung verwenden, wissen Sie, dass der Registrierungsschlüssel außer Kraft gesetzt werden kann, wodurch die Kennworteingabeaufforderung des Gasts wieder angezeigt wird.



### Sicherheitsaspekte bei der Authentifizierung

Auch wenn die Zwischenspeicherung der Anmeldeinformationen des Endbenutzers die beste Benutzererfahrung bietet, müssen Sie sich mit den damit verbundenen Risiken vertraut machen.

Wenn die Zwischenspeicherung von Anmeldeinformationen aktiviert ist, werden die Domänenanmeldeinformationen des Endbenutzers in einem reversiblen Format innerhalb des Windows-Anmelde Informations-Managers gespeichert. Infolgedessen kann ein Angreifer ein Tool schreiben, das entweder als Prozess auf Systemebene oder als Endbenutzer Prozess ausgeführt wird und die Anmeldeinformationen des Endbenutzers abruft. Sie können dieses Risiko nur verringern, indem Sie DisablePasswordSaving auf **Enabled**festlegen.

Das gleiche Problem tritt auf, wenn die MED-V-Authentifizierung deaktiviert ist, die Einstellung für die Terminal Dienste-Richtlinie jedoch aktiviert ist.

## Verwandte Themen


[Bewährte Sicherheitsmethoden für MED-V-Vorgänge](security-best-practices-for-med-v-operations.md)









