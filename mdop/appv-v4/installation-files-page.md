---
title: Seite „Installationsdateien“
description: Seite „Installationsdateien“
author: dansimp
ms.assetid: b0aad26f-b143-4f09-87a1-9f016a23cb62
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 08a2e7318271503f072298ca137a1e65e16c0178
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806668"
---
# Seite „Installationsdateien“


Auf der Seite " **Installationsdateien** " können Sie die Installationsdateien angeben, die zum Erstellen des virtuellen Anwendungspakets verwendet wurden, das auf der Seite **"Paket auswählen** " dieses Assistenten angegeben wurde. Wenn Sie ein virtuelles Anwendungspaket erstellt haben, das mehrere Anwendungen enthält, sollten Sie alle erforderlichen Installationsdateien in einen einzelnen Ordner auf dem Computer kopieren, auf dem der Microsoft Application Virtualization Sequencer ausgeführt wird.

Diese Seite enthält die folgenden Elemente:

<a href="" id="original-installation-files"></a>**Ursprüngliche Installationsdateien**  
Klicken Sie auf **Durchsuchen** , um die Installationsdateien anzugeben, die ursprünglich zum Erstellen des virtuellen Anwendungspakets verwendet wurden. Das von Ihnen angegebene übergeordnete Verzeichnis sollte lokal auf dem Computer gespeichert werden, auf dem der Sequencer ausgeführt wird, und muss alle erforderlichen Installationsdateien oder Unterordner enthalten, die die Installationsdateien enthalten. Die Installationsdateien können im übergeordneten Ordner oder in einem der Unterordner des angegebenen übergeordneten Ordners enthalten sein.

<a href="" id="files-installed-on-local-system"></a>**Auf dem lokalen System installierte Dateien**  
Klicken Sie auf **Durchsuchen** , um die Installationsdateien anzugeben, die lokal auf dem Computer installiert wurden, auf dem der Sequencer ausgeführt wird. Sie können diese Option nur auswählen, wenn die Installationsdateien der Anwendung im Standardspeicherort der Anwendung installiert wurden.

**Hinweis**  Der von Ihnen bereitgestellte Standard Installationsspeicherort hängt von den folgenden Bedingungen ab:

 

-   Der Paketstamm, der beim ursprünglichen Erstellen des Pakets angegeben wurde.

-   Der Installationsspeicherort, der beim ursprünglichen Erstellen des Pakets im Windows Installer angegeben wurde.

-   Der Standardinstallationspfad der Anwendung.

Wenn beispielsweise der angegebene Paketstamm **Q:\\Office12** ist und während der Installation der Standard Installationsspeicherort von **c:\\Programme Files\\Office12** in **Q:\\Office12**geändert wird, muss der während der Dehydratisierung angegebene Pfad **c:\\Programme Files\\Office 12**sein.

Wenn der angegebene Paketstamm **Q:\\Microsoft** ist und während der Installation der Standard Installationsspeicherort von **c:\\Programme Files\\Office12** in **Q:\\Microsoft\\Office12**geändert wird, muss der während der Dehydratisierung angegebene Pfad **c:\\Programme Dateien**sein.

Wenn Sie ein Paket mithilfe eines Paket Beschleunigers erstellen, wird jede Datei im Paket, beispielsweise **Q:\\Office12\\file.txt** auf dem lokalen Computer gefunden, indem das Paketstamm **Q:\\Office12** durch den Standardspeicherort ersetzt wird, der beim Erstellen des Paket Beschleunigers angegeben wurde, beispielsweise **c:\\Programme Files\\Office12**. Im vorherigen Beispiel sollte sich die Datei in **c:\\Programme Files\\Office12\\file.txt**befinden.

## Verwandte Themen


[Assistent „Package Accelerator erstellen“ (AppV 4.6 SP1)](create-package-accelerator-wizard--appv-46-sp1-.md)

 

 





