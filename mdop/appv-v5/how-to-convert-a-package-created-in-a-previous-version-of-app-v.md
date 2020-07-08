---
title: So konvertieren Sie ein Paket, das in einer früheren Version von App-V erstellt wurde
description: So konvertieren Sie ein Paket, das in einer früheren Version von App-V erstellt wurde
author: dansimp
ms.assetid: b092a5f8-cc5f-4df8-a5a2-0a68fd7bd5b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bd0d5db7cb406a5a7fe67c69ff77461cce2b0a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805669"
---
# So konvertieren Sie ein Paket, das in einer früheren Version von App-V erstellt wurde


Sie können das Paket Konverter-Dienstprogrammverwenden, um virtuelle Anwendungspakete zu aktualisieren, die mit früheren Versionen von App-V erstellt wurden.

**Hinweis:**  
Wenn Sie einen Computer mit einer 64-Bit-Architektur ausführen, müssen Sie die x86-Version von PowerShell verwenden.



Der Paket Konverter kann nur Pakete direkt konvertieren, die mit dem App-V 4,5-Sequenzer oder einer nachfolgenden Version erstellt wurden. Pakete, die mit einer Version vor App-v 4,5 erstellt wurden, müssen vor der Konvertierung auf das App-v 4,5-oder App-v 4,6-Format aktualisiert werden.

Die folgenden Informationen enthalten eine Anleitung zum Konvertieren vorhandener virtueller Anwendungspakete.

**Wichtig**  
Sie müssen den Paket Konverter so konfigurieren, dass die Paketinhalts Datei immer an einem sicheren Speicherort und Verzeichnis gespeichert wird. Auf einen sicheren Speicherort kann nur von einem Administrator zugegriffen werden. Wenn Sie das Paket bereitstellen, sollten Sie darüber hinaus das Paket an einem sicheren Speicherort speichern, oder Sie müssen sicherstellen, dass kein anderer Benutzer während des Konvertierungsvorgangs angemeldet werden darf.



**Erste Schritte**

1.  Installieren Sie den App-V-Sequencer auf einem Computer in Ihrer Umgebung. Informationen zum Installieren des Sequencers finden Sie unter so wird es [gemacht: Installieren des Sequencers](how-to-install-the-sequencer-beta-gb18030.md).

2. Importieren des erforderlichen PowerShell-Moduls

```powershell
Import-Module AppVPkgConverter
```

3. Die folgenden Cmdlets stehen zur Verfügung:

   -   Test-AppvLegacyPackage – dieses Cmdlet dient zum Überprüfen von Paketen. Es werden Informationen zu Fehlern mit dem Paket wie fehlenden **SFT** -Dateien, einer ungültigen Quelle, **OSD** -Dateifehlern oder einer ungültigen Paketversion zurückgegeben. Dieses Cmdlet analysiert die **SFT-** Datei nicht oder führt eine eingehende Überprüfung durch. Informationen zu Optionen und Grundfunktionen für dieses Cmdlet finden Sie unter Verwenden des PowerShell-cmdline `Test-AppvLegacyPackage -?` .

   -   ConvertFrom-AppvLegacyPackage – geben Sie zum Konvertieren eines vorhandenen Pakets `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages` . In diesem Befehl `c:\contentStore` stellt den Speicherort des vorhandenen Pakets dar und `c:\convertedPackages` ist das Ausgabeverzeichnis, in das die resultierende App-V 5,0-Paketdatei für virtuelle Anwendungen gespeichert wird. Wenn Sie keinen neuen Namen angeben, wird standardmäßig der alte Paketname für den App-V 5,0-Dateinamen verwendet.

       Darüber hinaus optimiert der Paket Konverter die Leistung von Paketen in App-v 5,0, indem das Paket so festgelegt wird, dass das App-v-Paket den Fehler streamt.  Dies ist leistungsstärker als der primäre Feature-Block und der vollständige Download des Pakets. Mit dem Flag **DownloadFullPackageOnFirstLaunch** können Sie das Paket konvertieren und festlegen, dass das Paket standardmäßig vollständig heruntergeladen werden soll.

       **Hinweis:**  
       Bevor Sie das Ausgabeverzeichnis angeben, müssen Sie das Ausgabeverzeichnis erstellen.



~~~
**Advanced Conversion Tips**

-   Piping - PowerShell supports piping. Piping allows you to call `dir c:\contentStore\myPackage | Test-AppvLegacyPackage`. In this example, the directory object that represents `myPackage` will be given as input to the `Test-AppvLegacyPackage` command and bound to the `-Source` parameter. Piping like this is especially useful when you want to batch commands together; for example, `dir .\ | Test-AppvLegacyPackage | ConvertFrom-AppvLegacyAppvPackage -Target .\ConvertedPackages`. This piped command would test the packages and then pass those objects on to actually be converted. You can also apply a filter on packages without errors or only specify a directory which contains an **.sprj** file or pipe them to another cmdlet that adds the filtered package to the server or publishes them to the App-V 5.0 client.

-   Batching - The PowerShell command enables batching. More specifically, the cmdlets support taking a string\[\] object for the `-Source` parameter which represents a list of directory paths. This allows you to enter `$packages = dir c:\contentStore` and then call `ConvertFrom-AppvLegacyAppvPackage-Source $packages -Target c:\ConvertedPackages` or to use piping and call `dir c:\ContentStore | ConvertFrom-AppvLegacyAppvPackage -Target C:\ConvertedPackages`.

-   Other functionality - PowerShell has other built-in functionality for features such as aliases, piping, lazy-binding, .NET object, and many others. All of these are usable in PowerShell and can help you create advanced scenarios for the Package Converter.

**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Verwandte Themen


[Vorgänge für App-V 5.0](operations-for-app-v-50.md)









