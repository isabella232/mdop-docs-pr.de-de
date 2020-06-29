---
title: So veröffentlichen Sie eine virtuelle Anwendung auf dem Client
description: So veröffentlichen Sie eine virtuelle Anwendung auf dem Client
author: dansimp
ms.assetid: 90af843e-b5b3-4a71-a3a1-fa5f4c087f28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5585f82150db69929ccedbee3aecab969c5e7dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806880"
---
# So veröffentlichen Sie eine virtuelle Anwendung auf dem Client


Wenn Sie Application Virtualization mithilfe eines elektronischen Softwareverteilungssystems bereitstellen, können Sie eines der folgenden Verfahren zum Veröffentlichen eines Anwendungspakets für Ihre Benutzer verwenden.

**So veröffentlichen Sie ein Paket mit einer eigenständigen Windows Installer-Datei**

1.  Der Client sollte mit dem *RequireAuthorizationIfCached* -Parameter auf 0 (null) festgelegten installiert werden. Weitere Informationen zum Festlegen dieses Parameters finden Sie unter [Befehlszeilenparameter für Application Virtualization Client Installer](application-virtualization-client-installer-command-line-parameters.md)

2.  Kopieren Sie die Windows Installer-Datei und die SFT-Datei in denselben Ordner auf dem Zielcomputer.

3.  Führen Sie den folgenden Befehl auf dem Computer aus:

    `Msiexec.exe /I "packagename.msi" /q`

**So veröffentlichen Sie ein Paket mit Windows Installer und dem Paketmanifest**

1.  Kopieren Sie die Windows Installer-Datei auf den Zielcomputer und die SFT-Datei auf die Inhaltsfreigabe auf dem Streamingserver.

2.  Führen Sie den folgenden Befehl auf dem Computer der einzelnen Benutzer aus:

    `Msiexec.exe /I "\\pathtomsi\packagename.msi" MODE=STREAMING  OVERRIDEURL="\\\\server\\share\\package.sft" LOAD=TRUE /q`

    **Wichtig**  Bei OVERRIDEURL müssen alle umgekehrten Schrägstriche mit einem vorangehenden umgekehrten Schrägstrich maskiert werden, oder der OVERRIDEURL-Pfad wird nicht richtig analysiert. Außerdem müssen Eigenschaften und Werte als Großbuchstaben eingegeben werden, es sei denn, der Wert ist ein Pfad zu einer Datei.

     

**So veröffentlichen Sie ein Paket mit SFTMIME**

-   Führen Sie den folgenden Befehl auf dem Computer des Benutzers aus, um ein Beispiel für das Veröffentlichen einer Anwendung für alle Benutzer auf einem Computer zu finden:

    `SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

    Weitere Informationen zu diesen und anderen SFTMIME-Befehlen finden Sie unter [Befehlsreferenz für SFTMIME](sftmime--command-reference.md).

## Verwandte Themen


[Bestimmen der Veröffentlichungsmethode](determine-your-publishing-method.md)

[Electronic Software Distribution-basiertes Szenario](electronic-software-distribution-based-scenario.md)

[SFTMIME-Befehlsreferenz](sftmime--command-reference.md)

[Szenario für die eigenständige Bereitstellung für Application Virtualization Clients](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





