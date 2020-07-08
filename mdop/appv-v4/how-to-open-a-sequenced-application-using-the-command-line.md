---
title: So öffnen Sie eine sequenzierte Anwendung über die Befehlszeile
description: So öffnen Sie eine sequenzierte Anwendung über die Befehlszeile
author: dansimp
ms.assetid: dc23ee65-8aea-470e-bb3f-a2f2b06cb241
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c99ab6b41947fc255afa9cad5b3ed2e22e672c3e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806899"
---
# So öffnen Sie eine sequenzierte Anwendung über die Befehlszeile


Sie können virtuelle Anwendungspakete über die Befehlszeile öffnen. Sie müssen die **cmd** -Eingabeaufforderung als Administrator ausführen.

Gehen Sie wie folgt vor, um sequenzierte Anwendungspakete über die Befehlszeile zu öffnen.

**So öffnen Sie eine sequenzierte Anwendung über die Befehlszeile**

1.  Um die Eingabeaufforderung zu öffnen, klicken Sie auf **Start**, wählen Sie **Ausführen**aus, geben Sie **cmd**ein, und klicken Sie auf **OK**.

2.  Geben Sie an der Eingabeaufforderung **cd\\** ein, und geben Sie den Pfad zu dem Verzeichnis an, in dem der Sequencer installiert ist, und drücken Sie dann die **EINGABETASTE.**

3.  Geben Sie an der Eingabeaufforderung den folgenden Befehl ein, und ersetzen Sie den kursiv formatierten Text durch ihre Werte:

    SFTSequencer/Open:*"gibt die zu öffnende SPRJ-Datei an"*

    Drücken **Sie die Eingabe**Taste.

4.  Sie können auch die folgenden optionalen Parameter angeben. Geben Sie an der Eingabeaufforderung die folgenden Befehle ein, und ersetzen Sie den kursiv formatierten Text durch ihre Werte:

    /PackageName: "*gibt den Paketnamen an"*

    /MSI – gibt an, dass ein zugeordneter Microsoft Windows Installer generiert wird.

    /COMPRESS – gibt an, ob das Paket komprimiert werden soll. Standardmäßig werden Pakete nicht komprimiert.

    Drücken **Sie die Eingabe**Taste.

    **Hinweis**  Wenn das Installationsprogramm oder das Windows Installer-Paket über eine grafische Benutzeroberfläche verfügt, wird es angezeigt, nachdem Sie die Befehlszeilenparameter angegeben haben.

     

## Verwandte Themen


[So verwalten Sie virtuellen Anwendungen über die Befehlszeile](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





