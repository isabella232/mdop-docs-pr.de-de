---
title: Konfigurieren von IIS für sicheres Streaming
description: Konfigurieren von IIS für sicheres Streaming
author: dansimp
ms.assetid: 9a80a703-4642-4bec-b7af-dc7cb6b76925
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 724fd247d98c265421cea13f4b91c97049a2b4d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809022"
---
# Konfigurieren von IIS für sicheres Streaming


Mit der Veröffentlichung von Microsoft Application Virtualization (app-v), Version 4,5, können Sie http und HTTPS als Protokolle für das Streaming von Anwendungspaketen für die APP-v-Clients verwenden. Mit dieser Option können Organisationen die zusätzliche Skalierbarkeit nutzen, die IIS in der Regel bietet. Wenn Sie IIS als Streamingserver verwenden, können Sie die Kommunikation zwischen dem Client und dem Server mithilfe von HTTPS anstelle von http sichern.

**Hinweis**  Wenn Sie Anwendungen von einem Dateiserver streamen möchten, sollten Sie die Sicherheit der Kommunikation zu den Anwendungspaketen verbessern. Dies kann mit IPSec erreicht werden. Weitere Informationen finden Sie in den folgenden Themen in der TechNet-Bibliothek:

-   Für Windows Server2003 <https://go.microsoft.com/fwlink/?LinkId=133226>

-   Für Windows Server 2008 <https://go.microsoft.com/fwlink/?LinkId=133227>

 

## MIME-Typen


Wenn Sie IIS zum Streamen virtueller Anwendungen mit http oder HTTPS verwenden, um App-V zu unterstützen, müssen die folgenden MIME-Typen dem IIS-Server hinzugefügt werden:

-   . OSD = txt

-   . SFT = Binär

Verwenden Sie die folgenden KB-Artikel als Leitfaden für das Hinzufügen von MIME-Typen:

IIS 6,0: <https://go.microsoft.com/fwlink/?LinkId=151973>

IIS 7,0: <https://go.microsoft.com/fwlink/?LinkId=151977>

## Kerberos-Authentifizierung


Wenn Sie die http-oder HTTPS-und Kerberos-Authentifizierung zum Streamen von ICO-, OSD-oder SFT-Dateien verwenden, verbessern Sie die Sicherheit Ihrer Umgebung. Damit IIS die Kerberos-Authentifizierung unterstützt, müssen Sie jedoch einen richtigen Dienstprinzipalnamen (Service Principal Name, SPN) konfigurieren. Das `setspn.exe` Tool ist für Windows Server2003 über die Support Tools auf der Installations-CD verfügbar und in Windows Server2008 integriert.

Führen Sie zum Erstellen eines SPN an `setspn.exe` einer Eingabeaufforderung aus, während Sie als Mitglied von Domänenadministratoren angemeldet sind – beispielsweise `setspn.exe –A HTTP/FQDN of Server ServerName` .

## Verwandte Themen


[Konfigurieren von Management oder Streaming Server für die sichere Kommunikation nach der Installation](configuring-management-or-streaming-server-for-secure-communications-post-installation.md)

 

 





