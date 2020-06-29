---
title: Konfigurieren von E-Mail-Benachrichtigungen
description: Konfigurieren von E-Mail-Benachrichtigungen
author: dansimp
ms.assetid: 6e152de0-4376-4963-8d1a-3e7f5866d30f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 46e8d00c2446a0185de30bbd1f39a7e3eaf90080
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807723"
---
# Konfigurieren von E-Mail-Benachrichtigungen


Wenn ein Editor oder ein Bearbeiter versucht, ein Gruppenrichtlinienobjekt (Group Policy Object, GPO) zu erstellen, bereitzustellen oder zu löschen, wird eine Anforderung für diese Aktion an eine bestimmte e-Mail-Adresse oder Adressen gesendet, sodass eine genehmigende Person die Anforderung auswerten und implementieren oder ablehnen kann. Sie bestimmen die e-Mail-Adresse oder Adressen, an die Benachrichtigungen gesendet werden, sowie den Alias, aus dem Benachrichtigungen gesendet werden.

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So konfigurieren Sie die e-Mail-Benachrichtigung für AGPM**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie im Detailbereich auf die Registerkarte **Domänendelegierung** .

3.  Geben Sie im Feld **von** den e-Mail-Alias für AGPM ein, aus dem Benachrichtigungen gesendet werden sollen.

4.  Geben Sie im Feld **an** eine durch trennzeichengetrennte Liste der e-Mail-Adressen von genehmigenden Personen ein, die Genehmigungsanforderungen erhalten sollen.

5.  Geben Sie im Feld **SMTP-Server** einen gültigen SMTP-e-Mail-Server ein.

6.  Geben Sie in den Feldern **Benutzername** und **Kennwort** die Anmeldeinformationen eines Benutzers mit Zugriff auf den SMTP-Dienst ein.

7.  Klicken Sie auf **Übernehmen**.

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über die Berechtigungen **Listeninhalt** und **Änderungsoptionen** für die Domäne verfügen.

-   E-Mail-Benachrichtigung für AGPM ist eine Einstellung auf Domänenebene. Sie können unterschiedliche e-Mail-Adressen oder AGPM-e-Mail-Aliase auf den Registerkarten der Domänen **Delegierung** jeder Domäne angeben oder dieselben e-Mail-Adressen in ihrer gesamten Umgebung verwenden.

### Weitere Verweise

-   [Durchführen von AGPM-Administratoraufgaben](performing-agpm-administrator-tasks.md)

 

 





