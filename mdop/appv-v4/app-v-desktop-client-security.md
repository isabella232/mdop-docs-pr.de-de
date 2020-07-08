---
title: App-V Desktop Client-Sicherheit
description: App-V Desktop Client-Sicherheit
author: dansimp
ms.assetid: 216b9c16-7bb4-4f94-b9d8-810501285008
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 26add6f855780113613cf1591c41722643954477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809283"
---
# App-V Desktop Client-Sicherheit


Der App-V-Desktop Client bietet zahlreiche Sicherheitsverbesserungen, die in früheren Versionen des Produkts nicht zur Verfügung standen. Diese Änderungen bieten standardmäßig höhere Sicherheitsstufen und über die Konfiguration der Clienteinstellungen.

**Hinweis**  Wenn Sie den App-V-Desktop Client auf einem Computer installieren, ist die Software standardmäßig die sichersten Einstellungen. Beim Upgrade werden die vorherigen Einstellungen des Clients jedoch beibehalten.

 

Standardmäßig ist der App-V-Desktop Client nur mit den erforderlichen Berechtigungen konfiguriert, damit ein Benutzer ohne Administratorrechte eine Veröffentlichungsaktualisierung und Datenstrom Anwendungen ausführen kann. Zu den weiteren im App-V-Desktop Client bereitgestellten Sicherheitsverbesserungen gehören die folgenden:

-   Standardmäßig ist eine OSD-Cacheaktualisierung nur durch den Veröffentlichungs Aktualisierungsvorgang zulässig.

-   Auf die Protokolldatei ( `sftlog.txt` ) kann nur von Konten mit lokalem Administratorzugriff auf den Client zugegriffen werden.

-   Die Protokolldatei hat nun eine maximale Größe.

-   Die Protokolldateien werden über die Archivierungseinstellungen verwaltet.

-   Die System Ereignisprotokollierung wird nun ausgeführt.

## Berechtigungen


Nachdem Sie den Desktop Client installiert haben, können Sie mithilfe der Registrierung oder der von Microsoft bereitgestellten ADM-Vorlage andere Sicherheitseinstellungen über die MMC oder auf einem einzelnen Client konfigurieren. Der App-V-Desktop Client verfügt über Berechtigungen, die Sie festlegen können, um zu verhindern, dass nicht administrative Benutzer auf alle Features des Desktop Clients zugreifen. Eine vollständige Liste der Berechtigungen finden Sie in der APP-v-Client-Hilfedatei oder im App-v-Betriebshandbuch.

**Wichtig**  Berücksichtigen Sie die Auswirkungen der Änderung der Zugriffsrechte, insbesondere auf Systemen, die von mehreren Benutzern wie Terminal Servern freigegeben werden.

 

**Hinweis**  Wenn Benutzer in der Umgebung über lokale Administratorrechte für Ihre Computer verfügen, werden die Berechtigungen ignoriert.

 

### ADM-Vorlage

Microsoft Application Virtualization (App-V) führt eine ADM-Vorlage ein, mit der Sie die am häufigsten verwendeten Clienteinstellungen mithilfe von Gruppenrichtlinien konfigurieren können. Mit dieser Vorlage können Administratoren viele Clienteinstellungen mithilfe eines zentralisierten Verwaltungsmodells implementieren und ändern. Einige der in der ADM-Vorlage verfügbaren Einstellungen sind Sicherheitseinstellungen.

**Wichtig**  Beachten Sie bei der Verwendung der ADM-Vorlage, dass es sich bei den Einstellungen um Gruppenrichtlinien-Einstellungs Einstellungen und nicht um vollständig verwaltete Gruppenrichtlinien handelt.

 

Eine vollständige Beschreibung der ADM-Vorlage, der spezifischen Einstellungen und Anleitungen zum erfolgreichen Bereitstellen von Clients in Ihrer Umgebung finden Sie in der App-V ADM-Vorlage Whitepaper unter [https://go.microsoft.com/fwlink/LinkId=122063](https://go.microsoft.com/fwlink/?LinkId=122063) .

## Entfernen von OSD-Dateitypzuordnungen


Wenn Ihre Organisation nicht von Benutzern verlangt, Anwendungen direkt aus einer OSD-Datei zu öffnen, können Sie die Sicherheit erhöhen, indem Sie die Dateitypzuordnungen auf dem Client entfernen. Entfernen Sie die `HKEY_CURRENT_USERS` Tasten für OSD und `Softgird.osd.file` verwenden Sie den Registrierungs-Editor. Sie können diesen Prozess in ein Anmeldeskript oder in ein Skript nach der Installation einfügen, um diese Änderungen zu automatisieren.

 

 





