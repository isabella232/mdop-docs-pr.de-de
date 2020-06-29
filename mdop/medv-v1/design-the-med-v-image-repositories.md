---
title: Entwerfen Sie die MED-V-Image-Repositorys
description: Entwerfen Sie die MED-V-Image-Repositorys
author: dansimp
ms.assetid: e153154d-2751-4990-b94d-a2d76242c15f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0c59a0dd2d1b3a78bd211c6a6353a86c77d8fc2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810060"
---
# <span data-ttu-id="2d48f-103">Entwerfen Sie die MED-V-Image-Repositorys</span><span class="sxs-lookup"><span data-stu-id="2d48f-103">Design the MED-V Image Repositories</span></span>


<span data-ttu-id="2d48f-104">Nachdem MED-V-Bilder erstellt und gepackt wurden, können Sie an einem beliebigen Speicherort auf einem Dateiserver gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2d48f-104">After MED-V images are created and packed, they can be stored on a file server in any location.</span></span> <span data-ttu-id="2d48f-105">Die Dateien werden möglicherweise über HTTP oder HTTPS von einem oder mehreren IIS-Servern gesendet.</span><span class="sxs-lookup"><span data-stu-id="2d48f-105">The files may be sent over HTTP or HTTPS by one or more IIS servers.</span></span> <span data-ttu-id="2d48f-106">Das Bild-Repository kann von mehreren MED-V-Instanzen freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2d48f-106">The image repository can be shared by multiple MED-V instances.</span></span>

<span data-ttu-id="2d48f-107">Um die Bild Depots zu entwerfen, müssen Sie zunächst entscheiden, wie die Bilder für jeden Client bereitgestellt werden sollen, und dann, ob dieser Client ein lokales Image-Repository benötigt.</span><span class="sxs-lookup"><span data-stu-id="2d48f-107">To design the image repositories, you must first decide how the images will be deployed to each client and then whether that client requires a local image repository.</span></span> <span data-ttu-id="2d48f-108">Alle Repositories werden dann zusammen mit dem zugehörigen IIS-Server entworfen und abgelegt.</span><span class="sxs-lookup"><span data-stu-id="2d48f-108">Each repository is then designed and placed, along with its accompanying IIS server.</span></span>

## <span data-ttu-id="2d48f-109">Bestimmen, wie Bilder bereitgestellt werden</span><span class="sxs-lookup"><span data-stu-id="2d48f-109">Determine How Images Will Be Deployed</span></span>


<span data-ttu-id="2d48f-110">Entscheiden Sie für jeden Med-v-Arbeitsbereich, wie Sie Med-v-Bilder für den Client bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="2d48f-110">For each MED-V workspace, decide how you plan to deploy MED-V images to the client.</span></span> <span data-ttu-id="2d48f-111">Dies ist wichtig, wenn Sie ermitteln möchten, wie viele Repositories benötigt werden, um die gepackten Bilder zu speichern, wo diese Repositories abgelegt werden, und dann diese Repositories zu entwerfen.</span><span class="sxs-lookup"><span data-stu-id="2d48f-111">This is important in determining how many repositories are necessary to store the packed images, where those repositories will be placed, and then to design those repositories.</span></span>

<span data-ttu-id="2d48f-112">Verpackte Bilder können wie folgt bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="2d48f-112">Packed images can be deployed in the following ways:</span></span>

-   <span data-ttu-id="2d48f-113">Über das Netzwerk von einem Bildverteilungsserver heruntergeladen, der einen Dateiserver und einen IIS-Server umfasst.</span><span class="sxs-lookup"><span data-stu-id="2d48f-113">Downloaded over the network from an image distribution server, which comprises a file server and IIS server.</span></span>

-   <span data-ttu-id="2d48f-114">Auf Wechselmedien wie einem USB-Laufwerk oder einer DVD.</span><span class="sxs-lookup"><span data-stu-id="2d48f-114">On removable media, such as a USB drive or DVD.</span></span>

-   <span data-ttu-id="2d48f-115">Mit einem Unternehmenssoftware-Distributionscenter in einem Bildspeicher Verzeichnis auf dem Clientcomputer vorab bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2d48f-115">Pre-staged to an image store directory on the client computer using an enterprise software distribution center.</span></span>

<span data-ttu-id="2d48f-116">Entscheiden Sie, welche Methode oder Methoden für die Bereitstellung von MED-V-Bildern für die einzelnen Clients verwendet werden sollen und ob für den Speicherort ein Bild-Repository erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2d48f-116">Decide which method, or methods, will be used to deploy MED-V images to each of the clients and whether the location will require an image repository.</span></span>

## <span data-ttu-id="2d48f-117">Ermitteln der Anzahl von Bild Repositories</span><span class="sxs-lookup"><span data-stu-id="2d48f-117">Determine the Number of Image Repositories</span></span>


<span data-ttu-id="2d48f-118">Nachdem Sie nun die Mindestanzahl der benötigten Repositories ermittelt haben, fügen Sie weitere hinzu, wenn eines der folgenden Kriterien zutrifft:</span><span class="sxs-lookup"><span data-stu-id="2d48f-118">Now that you have determined the minimum number of repositories you need, add more if any of the following criteria apply:</span></span>

-   <span data-ttu-id="2d48f-119">Organisatorische oder regulatorische Gründe, die Med-v-Bilder voneinander zu trennen – einige Med-v-Bilder können möglicherweise nicht im gleichen Repository koexistieren.</span><span class="sxs-lookup"><span data-stu-id="2d48f-119">Organizational or regulatory reasons to separate the MED-V images—some MED-V images may not be able to coexist in the same repository.</span></span> <span data-ttu-id="2d48f-120">Vertrauliche persönliche Daten können beispielsweise Speicher auf einem Server erfordern, der nur für eine begrenzte Anzahl von Mitarbeitern verfügbar ist, die auf die Daten zugreifen müssen.</span><span class="sxs-lookup"><span data-stu-id="2d48f-120">For example, sensitive personal data may require storage on a server that is only available to a limited set of employees who need access to the data.</span></span>

-   <span data-ttu-id="2d48f-121">Clients in isolierten Netzwerken – wenn Bilder über das Netzwerk bereitgestellt werden, ermitteln Sie, ob Netzwerke isoliert sind und ein separates Repository erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2d48f-121">Clients in isolated networks—if images will be deployed over the network, determine whether any networks are isolated and require a separate repository.</span></span> <span data-ttu-id="2d48f-122">Beispielsweise isolieren Organisationen häufig Lab-Netzwerke aus Produktionsnetzwerken.</span><span class="sxs-lookup"><span data-stu-id="2d48f-122">For example, organizations often isolate lab networks from production networks.</span></span>

-   <span data-ttu-id="2d48f-123">Clients in Remotenetzwerken: Wenn Bilder über das Netzwerk bereitgestellt werden, werden einige Clientcomputer möglicherweise durch Netzwerk Links vom Repository getrennt, die nicht genügend Bandbreite aufweisen, um eine angemessene Benutzerfreundlichkeit zu gewährleisten, wenn ein Client einen MED-V-Arbeitsbereich lädt.</span><span class="sxs-lookup"><span data-stu-id="2d48f-123">Clients in remote networks—if images will be deployed over the network, some client machines may be separated from the repository by network links that have insufficient bandwidth to provide an adequate experience when a client loads a MED-V workspace.</span></span> <span data-ttu-id="2d48f-124">Falls erforderlich, entwerfen Sie zusätzliche MED-V-Instanzen, um diesen Bedarf zu beheben.</span><span class="sxs-lookup"><span data-stu-id="2d48f-124">If necessary, design additional MED-V instances to address this need.</span></span>

<span data-ttu-id="2d48f-125">Fügen Sie diese Repositories zum Entwurf hinzu.</span><span class="sxs-lookup"><span data-stu-id="2d48f-125">Add these repositories to the design.</span></span> <span data-ttu-id="2d48f-126">Entscheiden Sie sich für einen Namen für jedes Repository und den Grund für dessen Entwurf.</span><span class="sxs-lookup"><span data-stu-id="2d48f-126">Decide on a name for each repository and the reason for designing it.</span></span> <span data-ttu-id="2d48f-127">Entscheiden Sie, welche Med-v-Bilder in den Repositories gespeichert werden und welche Med-v-Clients Med-v-Arbeitsbereiche mit Bildern aus dem Repository laden werden.</span><span class="sxs-lookup"><span data-stu-id="2d48f-127">Decide which MED-V images the repositories will hold and which MED-V clients will load MED-V workspaces with images from the repository.</span></span>

## <span data-ttu-id="2d48f-128">Entwerfen und Platzieren der Bild Depots</span><span class="sxs-lookup"><span data-stu-id="2d48f-128">Design and Place the Image Repositories</span></span>


<span data-ttu-id="2d48f-129">Wenn ein neues Bild für Clients verfügbar ist, beginnt der Download des Bilds möglicherweise gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="2d48f-129">When a new image is available to clients, clients begin downloading the image, possibly simultaneously.</span></span> <span data-ttu-id="2d48f-130">Dies führt zu einer großen Nachfrage im Repository und muss beim Entwerfen des Image-Repositorys berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="2d48f-130">This creates a high demand on the repository and must be taken into account when designing the image repository.</span></span>

<span data-ttu-id="2d48f-131">Ermitteln Sie für jedes Repository die Menge der Daten, die gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2d48f-131">For each repository, determine the amount of data it will store.</span></span> <span data-ttu-id="2d48f-132">Summieren Sie die Größe von Bildern, die im Repository gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2d48f-132">Sum the sizes of images that will be stored in the repository.</span></span> <span data-ttu-id="2d48f-133">Dies ist der Wert des auf dem Dateiserver erforderlichen Speicherplatzes.</span><span class="sxs-lookup"><span data-stu-id="2d48f-133">This is the value of the disk space required on the file server.</span></span>

<span data-ttu-id="2d48f-134">Als nächstes addieren Sie die Anzahl der Clients, die MED-V-Bilder aus dem Repository herunterladen können.</span><span class="sxs-lookup"><span data-stu-id="2d48f-134">Next, add up the number of clients that may download MED-V images from the repository.</span></span> <span data-ttu-id="2d48f-135">Hierbei handelt es sich um die maximale Anzahl gleichzeitiger Downloads, die auftreten können, wenn ein neues MED-V-Abbild in das Repository geladen wird.</span><span class="sxs-lookup"><span data-stu-id="2d48f-135">This is the maximum number of concurrent downloads that can occur when a new MED-V image is loaded into the repository.</span></span> <span data-ttu-id="2d48f-136">Der Dateiserver muss mit einem Datenträgersubsystem entworfen werden, das die IO-Anforderungen erfüllen kann, die dadurch entstehen.</span><span class="sxs-lookup"><span data-stu-id="2d48f-136">The file server must be designed with a disk subsystem that can meet the IO demands this will create.</span></span>

<span data-ttu-id="2d48f-137">Das Image-Repository kann sich auf dem gleichen System wie der MED-V-Server und dem Server befinden, auf dem SQL Server ausgeführt wird, oder auf einer Remotedateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="2d48f-137">The image repository can reside on the same system as the MED-V server and the server running SQL Server, or on a remote file share.</span></span> <span data-ttu-id="2d48f-138">Sie können es auch in einer Windows Server2008 Hyper-V-VM ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d48f-138">You can also run it in a Windows Server2008 Hyper-V VM.</span></span> <span data-ttu-id="2d48f-139">Überprüfen Sie den Netzwerkstandort der Clients, die vom Image-Repository bereitgestellt werden, und platzieren Sie das Repository an einem Netzwerkspeicherort, an dem es über genügend Bandbreite verfügt, um die Erwartungen der Kunden an den Service Level zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="2d48f-139">Check the network location of the clients that the image repository will service, and place the repository in a network location where it will have sufficient bandwidth to meet the service level expectations of those clients.</span></span>

### <span data-ttu-id="2d48f-140">Fehlertoleranz</span><span class="sxs-lookup"><span data-stu-id="2d48f-140">Fault Tolerance</span></span>

<span data-ttu-id="2d48f-141">Wenn das Bild-Repository nicht verfügbar ist, können Clients keine neuen oder aktualisierten MED-V-Bilder herunterladen.</span><span class="sxs-lookup"><span data-stu-id="2d48f-141">If the image repository is unavailable, clients will not be able to download new or updated MED-V images.</span></span> <span data-ttu-id="2d48f-142">Informationen zum Entwerfen von Fehlertoleranzoptionen für den Dateiserver und fehlertolerante Datenträger finden Sie im Leitfaden zur [Infrastrukturplanung und-Entwurf von Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) .</span><span class="sxs-lookup"><span data-stu-id="2d48f-142">To design fault-tolerance options for the file server and fault-tolerant disks, see the [Infrastructure Planning and Design Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) guide.</span></span>

## <span data-ttu-id="2d48f-143">Entwerfen und Platzieren der IIS-Server</span><span class="sxs-lookup"><span data-stu-id="2d48f-143">Design and Place the IIS Servers</span></span>


<span data-ttu-id="2d48f-144">Dieser Abschnitt ist nur relevant, wenn Clients Bilddateien über das Netzwerk über HTTP oder https herunterladen.</span><span class="sxs-lookup"><span data-stu-id="2d48f-144">This section is only relevant if clients will download image files over the network using HTTP or HTTPS.</span></span>

<span data-ttu-id="2d48f-145">Der IIS-Server kann auf demselben System wie dem MED-V-Server und dem Server koexistieren, auf dem SQL Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d48f-145">The IIS server can coexist on the same system as the MED-V server and the server running SQL Server.</span></span> <span data-ttu-id="2d48f-146">Sie kann auch in einer Windows Server2008 Hyper-V-VM ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2d48f-146">It can also run in a Windows Server2008 Hyper-V VM.</span></span> <span data-ttu-id="2d48f-147">Die IIS-Serverinfrastruktur muss über einen ausreichenden Durchsatz verfügen, um Bilder an Clients innerhalb der Service Level-Erwartungen der Organisation zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="2d48f-147">The IIS server infrastructure must have sufficient throughput to deliver images to clients within the service level expectations of the organization.</span></span> <span data-ttu-id="2d48f-148">Sie muss mit einem Datenträgersubsystem entworfen werden, das die IO-Anforderungen erfüllen kann, die dadurch entstehen.</span><span class="sxs-lookup"><span data-stu-id="2d48f-148">It must be designed with a disk subsystem that can meet the IO demands this creates.</span></span>

<span data-ttu-id="2d48f-149">Addieren Sie für jedes Bild-Repository die Anzahl der Clients, die MED-V-Bilder mit IIS herunterladen können.</span><span class="sxs-lookup"><span data-stu-id="2d48f-149">For each image repository, sum the number of clients that may download MED-V images using IIS.</span></span> <span data-ttu-id="2d48f-150">Hierbei handelt es sich um die maximale Anzahl gleichzeitiger Downloads, die beim Laden eines Bilds in das Repository auftreten können.</span><span class="sxs-lookup"><span data-stu-id="2d48f-150">This is the maximum number of concurrent downloads that can occur when an image is loaded into the repository.</span></span> <span data-ttu-id="2d48f-151">Verwenden Sie die in [Definieren des Projektumfangs](define-the-project-scope.md) festgelegte Durchsatz Summe und die erwarteten Service Level, um den Entwurf der IIS-Serverinfrastruktur zu planen und die für das Repository zuzuweisende geeignete Bandbreite festzulegen.</span><span class="sxs-lookup"><span data-stu-id="2d48f-151">Use the throughput sum and the service level expectations determined in [Define the Project Scope](define-the-project-scope.md) to plan the design of the IIS server infrastructure and to determine the appropriate amount of bandwidth to allocate for the repository.</span></span>

<span data-ttu-id="2d48f-152">Informationen zum Entwerfen der IIS-Infrastruktur finden Sie im Leitfaden zur [Infrastrukturplanung und-Entwurf für Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) .</span><span class="sxs-lookup"><span data-stu-id="2d48f-152">To design the IIS infrastructure, see the [Infrastructure Planning and Design Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) guide.</span></span>

### <span data-ttu-id="2d48f-153">Fehlertoleranz</span><span class="sxs-lookup"><span data-stu-id="2d48f-153">Fault Tolerance</span></span>

<span data-ttu-id="2d48f-154">Wenn die IIS-Serverinfrastruktur nicht verfügbar ist, können Clients keine neuen oder aktualisierten Bilder herunterladen.</span><span class="sxs-lookup"><span data-stu-id="2d48f-154">If the IIS server infrastructure is unavailable, clients will not be able to download new or updated images.</span></span> <span data-ttu-id="2d48f-155">Um die Fehlertoleranz zu konfigurieren, kann der Windows Server2008-basierte IIS-Server in einem Failovercluster gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2d48f-155">To configure fault tolerance, the Windows Server2008-based IIS server can be placed in a failover cluster.</span></span> <span data-ttu-id="2d48f-156">Informationen zum Entwerfen der Fehlertoleranz für die IIS-Serverinfrastruktur finden Sie im Leitfaden zur [Infrastrukturplanung und-Entwurf für Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) .</span><span class="sxs-lookup"><span data-stu-id="2d48f-156">To design the fault tolerance for the IIS server infrastructure, see the [Infrastructure Planning and Design Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) guide.</span></span>

## <span data-ttu-id="2d48f-157">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2d48f-157">Related topics</span></span>


[<span data-ttu-id="2d48f-158">Bereitstellen eines MED-V-Arbeitsbereichs über ein Enterprise Software Distribution-System</span><span class="sxs-lookup"><span data-stu-id="2d48f-158">Deploying a MED-V Workspace Using an Enterprise Software Distribution System</span></span>](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md)

[<span data-ttu-id="2d48f-159">Bereitstellen eines MED-V-Arbeitsbereichs mit einem Bereitstellungspaket</span><span class="sxs-lookup"><span data-stu-id="2d48f-159">Deploying a MED-V Workspace Using a Deployment Package</span></span>](deploying-a-med-v-workspace-using-a-deployment-package.md)

 

 





