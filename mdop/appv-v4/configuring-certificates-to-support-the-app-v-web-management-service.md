---
title: Konfigurieren von Zertifikaten zur Unterstützung des App-V Web Management Service
description: Konfigurieren von Zertifikaten zur Unterstützung des App-V Web Management Service
author: dansimp
ms.assetid: b7960161-2c19-4cbf-a98a-d4b06f547dce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 23839e6fad79c1f10eb2416941396ad3c6f04d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809025"
---
# Konfigurieren von Zertifikaten zur Unterstützung des App-V Web Management Service


Der App-V-Webverwaltungs Dienst muss so konfiguriert sein, dass SSL-basierte Verbindungen unterstützt werden, um die Kommunikation zu gewährleisten. Dieser Vorgang setzt voraus, dass der Webserver oder der Computer, auf dem der Verwaltungsdienst installiert ist, über ein Zertifikat verfügt, das für den Dienst oder Computer ausgestellt wurde.

Die folgenden Szenarien veranschaulichen, wie Sie ein Zertifikat für diesen Zweck erhalten:

1.  Die Infrastruktur des Unternehmens verfügt bereits über eine Public Key-Infrastruktur (PKI), die automatisch Zertifikate für Computer ausgibt.

2.  Die Infrastruktur des Unternehmens verfügt bereits über eine PKI, die jedoch nicht automatisch Zertifikate für Computer ausstellt.

3.  In der Unternehmensinfrastruktur ist keine PKI vorhanden.

In jedem der vorhergehenden Szenarien ist die Methode zum Abrufen eines Zertifikats anders, das Endergebnis ist jedoch identisch. Der Administrator muss der IIS-Standardwebsite ein Zertifikat zuweisen und den App-V Web-Verwaltungsdienst so konfigurieren, dass eine sichere Kommunikation erforderlich ist.

**Wichtig**  Der Name des Zertifikats muss dem Namen des Servers entsprechen. Es empfiehlt sich, vollständig qualifizierte Domänennamen (FQDNs) für den allgemeinen Namen des Zertifikats zu verwenden.

 

App-V kann IIS-Server verwenden, um unterschiedliche Infrastrukturkonfigurationen zu unterstützen. Weitere Informationen zum Konfigurieren von IIS-Servern zur Unterstützung von HTTPS finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=151972> .

## Verwandte Themen


[So installieren und konfigurieren Sie die App-V Management Console für eine sicherere Umgebung](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)

 

 





