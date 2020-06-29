---
title: App-V 4.6 SP1 – Versionshinweise
description: App-V 4.6 SP1 – Versionshinweise
author: dansimp
ms.assetid: aeb6784a-864a-4f4e-976b-40c34dcfd8d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7081aaf4a04d52bf288d7a76b4a488e2b200c3d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808067"
---
# App-V 4.6 SP1 – Versionshinweise


Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.

**Wichtig**  Lesen Sie diese Versionshinweise gründlich, bevor Sie das Microsoft Application Virtualization (App-V)-Verwaltungs System installieren. Diese Anmerkungen zu dieser Version enthalten Informationen, die Ihnen bei der erfolgreichen Installation von Application Virtualization (App-V) 4.6 SP1 helfen. Dieses Dokument enthält Informationen, die in der Produktdokumentation nicht zur Verfügung stehen. Wenn es einen Unterschied zwischen diesen Anmerkungen zu dieser Version und einer anderen App-V-Dokumentation gibt, sollte die neueste Änderung als autorisierend angesehen werden.

 

## Schutz vor Sicherheitsrisiken und Viren


Zum Schutz vor Sicherheitsrisiken und Viren ist es wichtig, die neuesten verfügbaren Sicherheitsupdates für jede neue Software zu installieren, die installiert wird. Weitere Informationen finden Sie auf der [Microsoft-Sicherheitswebsite](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Bekannte Probleme mit Application Virtualization 4.6 SP1


In diesem Abschnitt finden Sie die neuesten Informationen zu Problemen mit Microsoft Application Virtualization (App-V) 4.6 SP1. Diese Probleme werden in der Produktdokumentation nicht angezeigt und können in einigen Fällen der vorhandenen Produktdokumentation widersprechen. Wenn dies möglich ist, werden diese Probleme in späteren Versionen behoben.

### Der Pfad von sprt geht verloren, wenn er nicht in Schrägstrich (/) endet.

Wenn der Pfad in einem href-Objekt in einer Projektvorlage nicht mit einem Schrägstrich ( **/** ) endet, enthält die generierte href den Pfad nicht. Dies tritt auf, wenn der Benutzer die **sprt-** Datei manuell bearbeitet. Wenn Sie den Sequencer verwenden, wird nach dem Pfad immer der Schrägstrich () hinzugefügt **/** .

Problemumgehung stellen Sie sicher, dass die href einen nachgestellten Schrägstrich () aufweist **/** .

### Der Name des Benutzerordners entspricht nicht dem Paketnamen.

Ordner, die Benutzer-und Global. pkg-Dateien enthalten, enthalten nicht mehr den Paketnamen. Zuvor verwendete der App-V-Client den Paketstamm Ordner 8,3 Short Name als Teil des Ordner namens. So können Sie Sie ganz einfach erkennen. Wenn Sie den App-V 4,6 SP1-Sequenzer verwenden, sind die kurz Namen des Paketstamm Ordners 8,3 nun zufällige Zeichenfolgen. Dadurch ist es schwierig, die Ordner zu identifizieren, die die **pkg** -Dateien des Pakets auf dem Computer enthalten, auf dem der App-V-Client ausgeführt wird.

Problemumgehung verwenden Sie eine der folgenden Methoden, um diese Paketordner leichter zu erkennen:

1.  Wenn Sie das Paket mithilfe des Sequencers erstellen, geben Sie einen Ordnernamen an, der der 8,3-Benennungskonvention für den primären Anwendungsordner entspricht. Dieser Name wird dann als Teil des benutzerordnernamens verwendet, wie dies in App-V 4,6 der Fall war.

2.  Die SPRJ-Datei enthält jetzt ein Tag, in dem die Zeichenfolge angezeigt wird, die als Anfang des benutzerordnernamens verwendet wird. Sie können das **Shortname** -Element des **PACKAGEROOTFOLDER** -Elements verwenden, um den Namen zu ermitteln.

### Ausführen von App-V 4,6 SP1 auf Computern mit mehr als 64 Prozessoren

Wenn Sie App-v 4,6 SP1 auf Computern ausführen, auf denen mehr als 64-Prozessoren installiert sind, schlägt der APP-v-Client fehl.

Problemumgehung keine. Diese Konfiguration wird nicht unterstützt. Sie müssen App-V 4,6 SP1on-Computer ausführen, die weniger als 64-Prozessoren aufweisen.

### Application Virtualization 4,6 SP1-Update wird nicht in allen Gebietsschemas angeboten, die Microsoft Update verwenden

Wenn Sie Microsoft Update verwenden, steht das Update für App-V 4,6 SP1 für die folgenden Sprachgebietsschemas nicht zur Verfügung:

-   Kasachisch

-   Hindi

-   Serbisch-Kyrillisch

PROBLEMUMGEHUNG Wenn Sie Microsoft Windows Server Update Services (WSUS) verwenden, verwenden Sie die englische Version des Updates, oder laden Sie das Update aus dem Microsoft Update-Katalog herunter.

### Nach dem Erweitern des übergeordneten Pakets können Sie ein Plug-in nicht mit nebeneinander angeordneten Komponenten Sequenzen

Wenn Sie ein übergeordnetes Paket erweitern **Tools**, indem Sie  /  in der App-V Sequencer-Konsole Tools**zum Erweitern des Pakets in lokales System** verwenden und ein Plug-in mit parallelen Komponenten Sequenzen, wird ein Installationsfehler zurückgegeben. Beispiel:

-   **HRESULT 0x80073712**

Dies wird verursacht, wenn der Sequencer die parallele Komponente in die Registrierung schreibt, aber den Wert für den folgenden Registrierungsschlüssel nicht löscht:

HKEY \ _LOCAL \ _MACHINE \\components\\storedirty

Problemumgehung nachdem Sie das übergeordnete Paket auf dem Computer, auf dem der Sequencer ausgeführt wird, erweitert haben, müssen Sie den Wert für den folgenden Registrierungsschlüssel löschen:

HKEY \ _LOCAL \ _MACHINE \\components\\storedirty

Nachdem Sie den Wert gelöscht haben, müssen Sie das Plug-in sequenzieren.

### Anmerkungen zu dieser Version Copyright-Informationen

Dieses Dokument wird "as-is" bereitgestellt. Informationen und Ansichten, die in diesem Dokument ausgedrückt werden, wie URL und andere Verweise auf Internet Websites, können sich ohne Vorankündigung ändern. Das Risiko der Nutzung dieser Informationen liegt beim Benutzer.

Einige hier dargestellte Beispiele werden nur zur Illustration bereitgestellt und sind fiktiv. Es ist keine wirkliche Zuordnung oder Verbindung vorgesehen oder sollte abgeleitet werden.

Dieses Dokument stellt Ihnen keinerlei Rechte am geistigen Eigentum eines beliebigen Microsoft-Produkts zur Verfügung. Dieses Dokument darf für interne Referenzzwecke kopiert und verwendet werden. Sie können dieses Dokument für Ihre internen, Referenzzwecke ändern.



Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server und Windows Vista sind Marken der Microsoft-Unternehmensgruppe.

Alle anderen Marken sind Eigentum ihrer jeweiligen Eigentümer.

 

 





