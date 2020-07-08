---
title: App-V 4.6 - Versionshinweise
description: App-V 4.6 - Versionshinweise
author: dansimp
ms.assetid: a3eba129-edac-48bf-a933-3bf43a9873e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9eee3c309a927a72155dec707d8dd95f43e90fb9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809313"
---
# App-V 4.6 - Versionshinweise


Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.

**Wichtig**  Lesen Sie diese Versionshinweise gründlich, bevor Sie das Microsoft Application Virtualization (App-V)-Verwaltungs System installieren. Diese Anmerkungen zu dieser Version enthalten Informationen, die Sie benötigen, um Application Virtualization (App-V) 4.6 erfolgreich zu installieren. Dieses Dokument enthält Informationen, die in der Produktdokumentation nicht zur Verfügung stehen. Wenn zwischen diesen Versionshinweisen und der anderen App-V-Dokumentation Diskrepanzen bestehen, sollte die neueste Änderung als autorisierend angesehen werden.

 

## Schutz vor Sicherheitsrisiken und Viren


Zum Schutz vor Sicherheitsrisiken und Viren ist es wichtig, die neuesten verfügbaren Sicherheitsupdates für jede neue Software zu installieren, die installiert wird. Weitere Informationen finden Sie auf der [Microsoft-](https://go.microsoft.com/fwlink/?LinkId=3482) Website für Sicherheit ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Bekannte Probleme mit Application Virtualization 4.6


In diesem Abschnitt finden Sie die neuesten Informationen zu Problemen mit Microsoft Application Virtualization (App-V) 4.6. Diese Probleme werden in der Produktdokumentation nicht angezeigt und können in einigen Fällen der vorhandenen Produktdokumentation widersprechen. Wenn möglich, werden diese Probleme in späteren Versionen behoben.

### Fehler beim Laden/installieren beim Ausführen einer vom APP-v 4.5-Sequenzer generierten Windows Installer-Datei

Beim Ausführen einer vom APP-v 4.5-Sequenzer generierten Windows Installer-Datei entsteht beim Versuch, Sie auf einem App-v 4,6-Client auszuführen, ein Fehler beim Laden/installieren. Es wird die folgende Meldung angezeigt: "für dieses Paket ist Microsoft Application Virtualization Client 4.5 oder höher erforderlich." Verwenden Sie die folgende Problemumgehung.

WORKAROUNDOpen Sie das alte Paket entweder mit dem App-v 4,5 SP1-Sequenzer oder dem App-v 4,6-Sequenzer ab, und generieren Sie eine neue MSI-Datei für das Paket.

**Hinweis**  Alternativ kann der App-V-Sequenzer an der Eingabeaufforderung die neue MSI-Datei mit den Parametern */Open* und */MSI* generieren, beispielsweise `SFTSequencer /Open:”package.sprj” /MSI` . Weitere Informationen finden Sie unter [Aktualisieren einer virtuellen Anwendung mithilfe der Befehlszeile](how-to-upgrade-a-virtual-application-by-using-the-command-line.md).

 

### Anmerkungen zu dieser Version Copyright-Informationen

Dieses Dokument wird "as-is" bereitgestellt. Die in diesem Dokument enthaltenen Informationen und Ansichten, einschließlich URLs und andere Verweise auf Internetwebsites, können ohne vorherige Ankündigung geändert werden. Das Risiko der Nutzung dieser Informationen liegt beim Benutzer.

Einige hier dargestellte Beispiele werden nur zur Illustration bereitgestellt und sind fiktiv.Es ist keine wirkliche Zuordnung oder Verbindung vorgesehen oder sollte abgeleitet werden.

Dieses Dokument stellt Ihnen keinerlei Rechte am geistigen Eigentum eines beliebigen Microsoft-Produkts zur Verfügung. Dieses Dokument darf für interne Referenzzwecke kopiert und verwendet werden. Sie können dieses Dokument für Ihre internen, Referenzzwecke ändern.



Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server und Windows Vista sind Marken der Microsoft-Unternehmensgruppe.

Alle anderen Marken sind Eigentum ihrer jeweiligen Eigentümer.

 

 





