---
title: Planen der Bereitstellung von App-V 5.1 mittels eines elektronischen Softwareverteilungssystems
description: Planen der Bereitstellung von App-V 5.1 mittels eines elektronischen Softwareverteilungssystems
author: dansimp
ms.assetid: c26602c2-5e8d-44e6-90df-adacc593607e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fde3f0ea4f1dec72b97143b4b27dd0b32a503b15
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804949"
---
# <span data-ttu-id="78aba-103">Planen der Bereitstellung von App-V 5.1 mittels eines elektronischen Softwareverteilungssystems</span><span class="sxs-lookup"><span data-stu-id="78aba-103">Planning to Deploy App-V 5.1 with an Electronic Software Distribution System</span></span>


<span data-ttu-id="78aba-104">Wenn Sie ein elektronisches Softwareverteilungssystem zum Bereitstellen von App-V-Paketen verwenden, überprüfen Sie die folgenden Planungsüberlegungen.</span><span class="sxs-lookup"><span data-stu-id="78aba-104">If you are using an electronic software distribution system to deploy App-V packages, review the following planning considerations.</span></span> <span data-ttu-id="78aba-105">Informationen zur Verwendung von System Center Configuration Manager zum Bereitstellen von App-V finden Sie unter [Einführung in die Anwendungsverwaltung in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816).</span><span class="sxs-lookup"><span data-stu-id="78aba-105">For information about using System Center Configuration Manager to deploy App-V, see [Introduction to Application Management in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816).</span></span>

<span data-ttu-id="78aba-106">Überprüfen Sie die folgenden Komponenten-und Architektur Anforderungen, die bei der Verwendung von ESD zum Bereitstellen von App-V-Paketen gelten:</span><span class="sxs-lookup"><span data-stu-id="78aba-106">Review the following component and architecture requirements options that apply when you use an ESD to deploy App-V packages:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="78aba-107">Bereitstellungsanforderung oder-Option</span><span class="sxs-lookup"><span data-stu-id="78aba-107">Deployment requirement or option</span></span></th>
<th align="left"><span data-ttu-id="78aba-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78aba-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="78aba-109">Der App-V-Verwaltungsserver, die Verwaltungsdatenbank und der Veröffentlichungsserver sind nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="78aba-109">The App-V Management server, Management database, and Publishing server are not required.</span></span></p></td>
<td align="left"><p><span data-ttu-id="78aba-110">Diese Funktionen werden von der implementierten ESD-Lösung gehandhabt.</span><span class="sxs-lookup"><span data-stu-id="78aba-110">These functions are handled by the implemented ESD solution.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="78aba-111">Sie können den App-V-Berichtsserver und die Berichtsdatenbank nebeneinander mit dem ESD bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="78aba-111">You can deploy the App-V Reporting server and Reporting database side by side with the ESD.</span></span></p></td>
<td align="left"><p><span data-ttu-id="78aba-112">Die parallele Bereitstellung ermöglicht es Ihnen, Daten zu sammeln und Berichte zu generieren.</span><span class="sxs-lookup"><span data-stu-id="78aba-112">The side-by-side deployment lets you to collect data and generate reports.</span></span></p>
<p><span data-ttu-id="78aba-113">Wenn Sie den App-v-Client zum Senden von Berichtsinformationen aktivieren und nicht den App-v-Berichtsserver verwenden, werden die Berichtsdaten in zugehörigen XML-Dateien gespeichert.</span><span class="sxs-lookup"><span data-stu-id="78aba-113">If you enable the App-V client to send report information, and you are not using the App-V Reporting server, the reporting data is stored in associated .xml files.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="78aba-114">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="78aba-114">Related topics</span></span>


[<span data-ttu-id="78aba-115">Planen der Bereitstellung von App-V</span><span class="sxs-lookup"><span data-stu-id="78aba-115">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

 

 





