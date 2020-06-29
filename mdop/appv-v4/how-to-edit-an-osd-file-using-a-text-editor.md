---
title: So bearbeiten Sie eine OSD-Datei mit einem Text-Editor
description: So bearbeiten Sie eine OSD-Datei mit einem Text-Editor
author: dansimp
ms.assetid: f4263a1b-824f-49b9-8060-b8229c9d9960
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c83547b38cee7e91e8348689583e0542a88dab83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807108"
---
# So bearbeiten Sie eine OSD-Datei mit einem Text-Editor


Gehen Sie wie folgt vor, um eine OSD-Datei (Open Software Descriptor) mithilfe eines Text-Editors zu bearbeiten.

**So bearbeiten Sie eine OSD-Datei mit einem Text-Editor**

1.  Öffnen Sie die OSD-Datei mit einem beliebigen XML-oder ASCII-Text-Editor, beispielsweise mit Microsoft Editor.

    **Hinweis**  Lesen Sie vor dem Ändern der OSD-Datei das Schema, das von der XSD-Datei im Installationsverzeichnis vorgegeben wird. Wenn Sie diesem Schema nicht folgen, kann dies zu Fehlern führen, die verhindern, dass eine sequenzierte Anwendung erfolgreich gestartet wird.

     

2.  Bearbeiten Sie die OSD-Datei mit Ihrem XML-oder ASCII-Text-Editor Ihrer Wahl, wobei Sie das vorgegebene Schema und die folgenden Richtlinien beachten:

    1.  Stellen Sie sicher, dass benannte Elemente innerhalb des &lt; SOFTPKG &gt; -Stammelements geschachtelt sind.

    2.  Stellen Sie sicher, dass die Elementnamen in Großbuchstaben geschrieben sind.

    3.  Beachten Sie, dass bei Attributwerten die Groß-/Kleinschreibung berücksichtigt wird.

    4.  Geben Sie sorgfältig ein, und beachten Sie die XML-Spezifikationen.

## Verwandte Themen


[Informationen zur Registerkarte „OSD“](about-the-osd-tab.md)

[So bearbeiten Sie eine OSD-Datei](how-to-edit-an-osd-file.md)

[Elemente der OSD-Datei](osd-file-elements.md)

 

 





