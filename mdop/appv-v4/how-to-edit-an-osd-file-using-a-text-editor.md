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
# <span data-ttu-id="8cb04-103">So bearbeiten Sie eine OSD-Datei mit einem Text-Editor</span><span class="sxs-lookup"><span data-stu-id="8cb04-103">How to Edit an OSD File Using a Text Editor</span></span>


<span data-ttu-id="8cb04-104">Gehen Sie wie folgt vor, um eine OSD-Datei (Open Software Descriptor) mithilfe eines Text-Editors zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="8cb04-104">Use the following procedure to edit an Open Software Descriptor (OSD) file by using a text editor.</span></span>

**<span data-ttu-id="8cb04-105">So bearbeiten Sie eine OSD-Datei mit einem Text-Editor</span><span class="sxs-lookup"><span data-stu-id="8cb04-105">To edit an OSD file by using a text editor</span></span>**

1.  <span data-ttu-id="8cb04-106">Öffnen Sie die OSD-Datei mit einem beliebigen XML-oder ASCII-Text-Editor, beispielsweise mit Microsoft Editor.</span><span class="sxs-lookup"><span data-stu-id="8cb04-106">Open the OSD file using any XML or ASCII text editor—for example, Microsoft Notepad.</span></span>

    <span data-ttu-id="8cb04-107">**Hinweis**  Lesen Sie vor dem Ändern der OSD-Datei das Schema, das von der XSD-Datei im Installationsverzeichnis vorgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8cb04-107">**Note** Before modifying the OSD file, read the schema prescribed by the XSD file in the install directory.</span></span> <span data-ttu-id="8cb04-108">Wenn Sie diesem Schema nicht folgen, kann dies zu Fehlern führen, die verhindern, dass eine sequenzierte Anwendung erfolgreich gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="8cb04-108">Failing to follow this schema might introduce errors that prevent a sequenced application from starting successfully.</span></span>

     

2.  <span data-ttu-id="8cb04-109">Bearbeiten Sie die OSD-Datei mit Ihrem XML-oder ASCII-Text-Editor Ihrer Wahl, wobei Sie das vorgegebene Schema und die folgenden Richtlinien beachten:</span><span class="sxs-lookup"><span data-stu-id="8cb04-109">Edit the OSD file using your XML or ASCII text editor of choice, adhering to the prescribed schema and the following guidelines:</span></span>

    1.  <span data-ttu-id="8cb04-110">Stellen Sie sicher, dass benannte Elemente innerhalb des &lt; SOFTPKG &gt; -Stammelements geschachtelt sind.</span><span class="sxs-lookup"><span data-stu-id="8cb04-110">Ensure that named elements are nested within the &lt;SOFTPKG&gt; root element.</span></span>

    2.  <span data-ttu-id="8cb04-111">Stellen Sie sicher, dass die Elementnamen in Großbuchstaben geschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="8cb04-111">Ensure that element names are in all uppercase letters.</span></span>

    3.  <span data-ttu-id="8cb04-112">Beachten Sie, dass bei Attributwerten die Groß-/Kleinschreibung berücksichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="8cb04-112">Be aware that attribute values are case sensitive.</span></span>

    4.  <span data-ttu-id="8cb04-113">Geben Sie sorgfältig ein, und beachten Sie die XML-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="8cb04-113">Type carefully, and observe the XML specifications.</span></span>

## <span data-ttu-id="8cb04-114">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="8cb04-114">Related topics</span></span>


[<span data-ttu-id="8cb04-115">Informationen zur Registerkarte „OSD“</span><span class="sxs-lookup"><span data-stu-id="8cb04-115">About the OSD Tab</span></span>](about-the-osd-tab.md)

[<span data-ttu-id="8cb04-116">So bearbeiten Sie eine OSD-Datei</span><span class="sxs-lookup"><span data-stu-id="8cb04-116">How to Edit an OSD File</span></span>](how-to-edit-an-osd-file.md)

[<span data-ttu-id="8cb04-117">Elemente der OSD-Datei</span><span class="sxs-lookup"><span data-stu-id="8cb04-117">OSD File Elements</span></span>](osd-file-elements.md)

 

 





