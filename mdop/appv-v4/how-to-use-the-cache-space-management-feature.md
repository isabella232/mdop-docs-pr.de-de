---
title: So verwenden Sie das Verwaltungsfeature für den Cachespeicher
description: So verwenden Sie das Verwaltungsfeature für den Cachespeicher
author: dansimp
ms.assetid: 60965660-c015-46a8-88ac-54cbc050fe33
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fcb9cc4bc076e1acf52fb1c03797384c45b82f7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806695"
---
# <span data-ttu-id="3ba05-103">So verwenden Sie das Verwaltungsfeature für den Cachespeicher</span><span class="sxs-lookup"><span data-stu-id="3ba05-103">How to Use the Cache Space Management Feature</span></span>


<span data-ttu-id="3ba05-104">Das Speicher Verwaltungsfeature für das Dateisystem-Cache verwendet einen am wenigsten zuletzt verwendeten Algorithmus (LRU) und ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3ba05-104">The FileSystem cache space management feature uses a Least Recently Used (LRU) algorithm and is enabled by default.</span></span> <span data-ttu-id="3ba05-105">Wenn der Platz, der für ein neues Paket erforderlich ist, den verfügbaren freien Speicherplatz im Cache überschreitet, verwendet der Application Virtualization (App-V)-Client dieses Feature, um zu ermitteln, welche, falls vorhanden, vorhandene Pakete aus dem Cache löschen können, um Platz für das neue Paket zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="3ba05-105">If the space that is required for a new package would exceed the available free space in the cache, the Application Virtualization (App-V) Client uses this feature to determine which, if any, existing packages it can delete from the cache to make room for the new package.</span></span> <span data-ttu-id="3ba05-106">Der Client löscht das Paket mit dem ältesten Datum des letzten Zugriffs, wenn es älter als der im Registrierungswert MinPkgAge angegebene Wert ist.</span><span class="sxs-lookup"><span data-stu-id="3ba05-106">The client deletes the package with the oldest last-accessed date if it is older than the value specified in the MinPkgAge registry value.</span></span> <span data-ttu-id="3ba05-107">Die Verwendung des Dateisystem-Cache-Speicherplatz Verwaltungsfeatures kann auch dazu beitragen, niedrige Speicherplatzprobleme zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="3ba05-107">Use of the FileSystem cache space management feature can also help to avoid low cache space problems.</span></span>

<span data-ttu-id="3ba05-108">Wenn erforderlich, werden mehr als ein Paket gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3ba05-108">More than one package is deleted if necessary.</span></span> <span data-ttu-id="3ba05-109">Gesperrte Pakete werden nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3ba05-109">Packages that are locked are not deleted.</span></span>

<span data-ttu-id="3ba05-110">**Hinweis**  Wenn Sie sicherstellen möchten, dass der Cache über genügend Speicherplatz für alle Pakete verfügt, die möglicherweise bereitgestellt werden, verwenden Sie die Einstellung Speicher **Platz für freien Speicherplatz verwenden** , wenn Sie den Client so konfigurieren, dass der Cache nach Bedarf erweitert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3ba05-110">**Note** To ensure that the cache has sufficient space allocated for all packages that might be deployed, use the **Use free disk space threshold** setting when you configure the client so that the cache can grow as needed.</span></span> <span data-ttu-id="3ba05-111">Sie können aber auch im voraus ermitteln, wie viel Speicherplatz für den App-V-Cache benötigt wird, und die Cachegröße zur Installationszeit entsprechend festlegen.</span><span class="sxs-lookup"><span data-stu-id="3ba05-111">Alternatively, determine in advance how much disk space will be needed for the App-V cache, and at installation time, set the cache size accordingly.</span></span>

 

<span data-ttu-id="3ba05-112">Das Cache-Speicherplatz Verwaltungsfeature wird vom Registrierungswert UnloadLeastRecentlyUsed gesteuert.</span><span class="sxs-lookup"><span data-stu-id="3ba05-112">The cache space management feature is controlled by the UnloadLeastRecentlyUsed registry value.</span></span> <span data-ttu-id="3ba05-113">Der Wert 1 aktiviert das Feature, und der Wert 0 (null) deaktiviert es.</span><span class="sxs-lookup"><span data-stu-id="3ba05-113">A value of 1 enables the feature, and a value of 0 (zero) disables it.</span></span>

**<span data-ttu-id="3ba05-114">So aktivieren oder deaktivieren Sie das Feature "Cachespeicherverwaltung"</span><span class="sxs-lookup"><span data-stu-id="3ba05-114">To enable or disable the cache space management feature</span></span>**

-   <span data-ttu-id="3ba05-115">Setzen Sie den folgenden Registrierungswert auf 1, um den LRU-Algorithmus zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3ba05-115">Set the following registry value to 1 to enable the LRU algorithm.</span></span> <span data-ttu-id="3ba05-116">Setzen Sie den Wert auf 0 (null), um das Feature zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="3ba05-116">Set it to 0 (zero) to disable the feature.</span></span>

    <span data-ttu-id="3ba05-117">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\appfs\\unloadleastrecentlyused</span><span class="sxs-lookup"><span data-stu-id="3ba05-117">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\UnloadLeastRecentlyUsed</span></span>

**<span data-ttu-id="3ba05-118">So steuern Sie, welche Pakete verworfen werden können</span><span class="sxs-lookup"><span data-stu-id="3ba05-118">To control which packages can be discarded</span></span>**

-   <span data-ttu-id="3ba05-119">Wenn Sie feststellen möchten, wann das Paket für verwerfen ausgewählt werden kann, legen Sie den folgenden Registrierungswert auf die minimale Anzahl von Tagen fest, die Sie verstreichen möchten, nachdem das Paket zuletzt zugegriffen wurde.</span><span class="sxs-lookup"><span data-stu-id="3ba05-119">To determine when the package can be selected for discard, set the following registry value to equal the minimum number of days you want to elapse since the package was last accessed.</span></span> <span data-ttu-id="3ba05-120">Pakete, die in letzter Zeit verwendet wurden, werden nicht verworfen.</span><span class="sxs-lookup"><span data-stu-id="3ba05-120">Packages that have been used more recently are not discarded.</span></span>

    <span data-ttu-id="3ba05-121">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\appfs\\minpkgage</span><span class="sxs-lookup"><span data-stu-id="3ba05-121">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\MinPkgAge</span></span>

    <span data-ttu-id="3ba05-122">**Vorsicht**  Der Höchstwert für diesen Registrierungsschlüssel lautet 0x00011111.</span><span class="sxs-lookup"><span data-stu-id="3ba05-122">**Caution** The maximum value for this registry key is 0x00011111.</span></span> <span data-ttu-id="3ba05-123">Durch größere Werte wird die ordnungsgemäße Funktion des Cachespeicher Verwaltungsfeatures verhindert.</span><span class="sxs-lookup"><span data-stu-id="3ba05-123">Larger values will prevent the correct operation of the cache space management feature.</span></span>

     

## <span data-ttu-id="3ba05-124">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3ba05-124">Related topics</span></span>


[<span data-ttu-id="3ba05-125">So konfigurieren Sie die App-V-Client-Registrierungseinstellungen über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="3ba05-125">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





