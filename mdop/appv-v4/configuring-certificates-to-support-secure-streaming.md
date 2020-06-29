---
title: Konfigurieren von Zertifikaten zur Unterstützung von sicherem Streaming
description: Konfigurieren von Zertifikaten zur Unterstützung von sicherem Streaming
author: dansimp
ms.assetid: 88dc76d8-7745-4729-92a1-af089c921244
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9376634a1b9843f46dba4cd452e672cc9e535226
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809028"
---
# Konfigurieren von Zertifikaten zur Unterstützung von sicherem Streaming


Standardmäßig wird der App-V-Dienst unter dem Netzwerkdienstkonto ausgeführt. Sie können jedoch ein Dienstkonto in den Active Directory-Domänendiensten erstellen und das Netzwerkdienstkonto durch das Active Directory-Domänenkonto ersetzen.

Der Sicherheitskontext, in dem der Dienst ausgeführt wird, ist für die Konfiguration der erweiterten sicheren Kommunikation wichtig. Dieser Sicherheitskontext muss über Leseberechtigungen für den privaten Zertifikatschlüssel verfügen. Wenn eine PKCS \ #10 *Certificate Signing Request* (CSR) für den App-V-Server generiert wird, wird der Windows *Cryptographic Service Provider* aufgerufen und ein privater Schlüssel generiert. Der private Schlüssel ist mit den Berechtigungen geschützt, die nur den System-und Administrator Konten zugewiesen sind.

Sie müssen die Zugriffssteuerungslisten (ACLs) für den privaten Schlüssel ändern, damit der App-V-Verwaltungs-oder Streamingserver auf den privaten Schlüssel zugreifen kann, der für eine erfolgreiche TLS-gesicherte Kommunikation erforderlich ist.

## Abrufen und Installieren eines Zertifikats


Die Szenarien für das Abrufen und Installieren eines Zertifikats für App-V lauten wie folgt:

-   Interne Public Key-Infrastruktur (PKI).

-   Zertifizierungsstelle (ca) eines Drittanbieters für Zertifikate.

    **Hinweis**  Wenn Sie ein Zertifikat von einer Drittanbieter-Zertifizierungsstelle anfordern müssen, befolgen Sie die auf der Website der Zertifizierungsstelle verfügbare Dokumentation.

     

Wenn eine PKI-Infrastruktur bereitgestellt wurde, konsultieren Sie die PKI-Administratoren, um ein Zertifikat zu erwerben, das die in diesem Thema beschriebenen Anforderungen erfüllt. Wenn keine PKI-Infrastruktur verfügbar ist, verwenden Sie eine Drittanbieter-Zertifizierungsstelle, um ein gültiges Zertifikat zu erhalten.

Eine Schritt-für-Schritt-Anleitung zum Abrufen und Installieren eines Zertifikats finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=151969> .

## Verwandte Themen


Konfigurieren von Zertifikaten zur Unterstützung von sicheres Streaming so [Ändern Sie die Berechtigungen privater Schlüssel zur Unterstützung des Verwaltungsservers oder des Streaming Servers](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)

 

 





