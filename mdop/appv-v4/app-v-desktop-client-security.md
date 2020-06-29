---
title: App-V Desktop Client-Sicherheit
description: App-V Desktop Client-Sicherheit
author: dansimp
ms.assetid: 216b9c16-7bb4-4f94-b9d8-810501285008
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 26add6f855780113613cf1591c41722643954477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809283"
---
# <span data-ttu-id="f3b16-103">App-V Desktop Client-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="f3b16-103">App-V Desktop Client Security</span></span>


<span data-ttu-id="f3b16-104">Der App-V-Desktop Client bietet zahlreiche Sicherheitsverbesserungen, die in früheren Versionen des Produkts nicht zur Verfügung standen.</span><span class="sxs-lookup"><span data-stu-id="f3b16-104">The App-V Desktop Client provides many security enhancements that were not available in previous versions of the product.</span></span> <span data-ttu-id="f3b16-105">Diese Änderungen bieten standardmäßig höhere Sicherheitsstufen und über die Konfiguration der Clienteinstellungen.</span><span class="sxs-lookup"><span data-stu-id="f3b16-105">These changes provide higher levels of security by default and through configuration of the client settings.</span></span>

<span data-ttu-id="f3b16-106">**Hinweis**  Wenn Sie den App-V-Desktop Client auf einem Computer installieren, ist die Software standardmäßig die sichersten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="f3b16-106">**Note** When you install the App-V Desktop Client on a computer, the software defaults to the most secure settings.</span></span> <span data-ttu-id="f3b16-107">Beim Upgrade werden die vorherigen Einstellungen des Clients jedoch beibehalten.</span><span class="sxs-lookup"><span data-stu-id="f3b16-107">However, when upgrading, the previous settings of the client persist.</span></span>

 

<span data-ttu-id="f3b16-108">Standardmäßig ist der App-V-Desktop Client nur mit den erforderlichen Berechtigungen konfiguriert, damit ein Benutzer ohne Administratorrechte eine Veröffentlichungsaktualisierung und Datenstrom Anwendungen ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="f3b16-108">By default, the App-V Desktop Client is configured only with the permissions required to allow a non-administrative user to perform a publishing refresh and stream applications.</span></span> <span data-ttu-id="f3b16-109">Zu den weiteren im App-V-Desktop Client bereitgestellten Sicherheitsverbesserungen gehören die folgenden:</span><span class="sxs-lookup"><span data-stu-id="f3b16-109">Additional security enhancements provided in the App-V Desktop Client include the following:</span></span>

-   <span data-ttu-id="f3b16-110">Standardmäßig ist eine OSD-Cacheaktualisierung nur durch den Veröffentlichungs Aktualisierungsvorgang zulässig.</span><span class="sxs-lookup"><span data-stu-id="f3b16-110">By default, an OSD cache update is allowed only by the publishing refresh process.</span></span>

-   <span data-ttu-id="f3b16-111">Auf die Protokolldatei ( `sftlog.txt` ) kann nur von Konten mit lokalem Administratorzugriff auf den Client zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="f3b16-111">The log file (`sftlog.txt`) is accessible only by accounts with local administrative access to the client.</span></span>

-   <span data-ttu-id="f3b16-112">Die Protokolldatei hat nun eine maximale Größe.</span><span class="sxs-lookup"><span data-stu-id="f3b16-112">The log file now has a maximum size.</span></span>

-   <span data-ttu-id="f3b16-113">Die Protokolldateien werden über die Archivierungseinstellungen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="f3b16-113">The log files are managed through archive settings.</span></span>

-   <span data-ttu-id="f3b16-114">Die System Ereignisprotokollierung wird nun ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f3b16-114">System Event logging is now performed.</span></span>

## <span data-ttu-id="f3b16-115">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="f3b16-115">Permissions</span></span>


<span data-ttu-id="f3b16-116">Nachdem Sie den Desktop Client installiert haben, können Sie mithilfe der Registrierung oder der von Microsoft bereitgestellten ADM-Vorlage andere Sicherheitseinstellungen über die MMC oder auf einem einzelnen Client konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f3b16-116">After you install the Desktop Client, you can configure other security settings through the MMC, or on an individual client by using the registry or the ADM Template provided by Microsoft.</span></span> <span data-ttu-id="f3b16-117">Der App-V-Desktop Client verfügt über Berechtigungen, die Sie festlegen können, um zu verhindern, dass nicht administrative Benutzer auf alle Features des Desktop Clients zugreifen.</span><span class="sxs-lookup"><span data-stu-id="f3b16-117">The App-V Desktop Client has permissions that you can set to restrict non-administrative users from accessing all the features of the Desktop Client.</span></span> <span data-ttu-id="f3b16-118">Eine vollständige Liste der Berechtigungen finden Sie in der APP-v-Client-Hilfedatei oder im App-v-Betriebshandbuch.</span><span class="sxs-lookup"><span data-stu-id="f3b16-118">For a full list of permissions, please see the App-V Client Help file or App-V Operations Guide.</span></span>

<span data-ttu-id="f3b16-119">**Wichtig**  Berücksichtigen Sie die Auswirkungen der Änderung der Zugriffsrechte, insbesondere auf Systemen, die von mehreren Benutzern wie Terminal Servern freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f3b16-119">**Important** Carefully consider the consequences of changing access rights, especially on systems that are shared by multiple users, such as Terminal Servers.</span></span>

 

<span data-ttu-id="f3b16-120">**Hinweis**  Wenn Benutzer in der Umgebung über lokale Administratorrechte für Ihre Computer verfügen, werden die Berechtigungen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f3b16-120">**Note** If users in the environment have local administrator privileges for their computers, the permissions are ignored.</span></span>

 

### <span data-ttu-id="f3b16-121">ADM-Vorlage</span><span class="sxs-lookup"><span data-stu-id="f3b16-121">ADM Template</span></span>

<span data-ttu-id="f3b16-122">Microsoft Application Virtualization (App-V) führt eine ADM-Vorlage ein, mit der Sie die am häufigsten verwendeten Clienteinstellungen mithilfe von Gruppenrichtlinien konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="f3b16-122">Microsoft Application Virtualization (App-V) introduces an ADM Template that you can use to configure the most common client settings through Group Policies.</span></span> <span data-ttu-id="f3b16-123">Mit dieser Vorlage können Administratoren viele Clienteinstellungen mithilfe eines zentralisierten Verwaltungsmodells implementieren und ändern.</span><span class="sxs-lookup"><span data-stu-id="f3b16-123">This template enables administrators to implement and change many of the client settings through a centralized administration model.</span></span> <span data-ttu-id="f3b16-124">Einige der in der ADM-Vorlage verfügbaren Einstellungen sind Sicherheitseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="f3b16-124">Some of the settings available in the ADM Template are security settings.</span></span>

<span data-ttu-id="f3b16-125">**Wichtig**  Beachten Sie bei der Verwendung der ADM-Vorlage, dass es sich bei den Einstellungen um Gruppenrichtlinien-Einstellungs Einstellungen und nicht um vollständig verwaltete Gruppenrichtlinien handelt.</span><span class="sxs-lookup"><span data-stu-id="f3b16-125">**Important** When using the ADM Template, remember that the settings are Group Policy preference settings and not fully managed Group Policies.</span></span>

 

<span data-ttu-id="f3b16-126">Eine vollständige Beschreibung der ADM-Vorlage, der spezifischen Einstellungen und Anleitungen zum erfolgreichen Bereitstellen von Clients in Ihrer Umgebung finden Sie in der App-V ADM-Vorlage Whitepaper unter [https://go.microsoft.com/fwlink/LinkId=122063](https://go.microsoft.com/fwlink/?LinkId=122063) .</span><span class="sxs-lookup"><span data-stu-id="f3b16-126">For a full description of the ADM Template, the specific settings, and guidance to successfully deploy clients in your environment, see the App-V ADM Template white paper at [https://go.microsoft.com/fwlink/LinkId=122063](https://go.microsoft.com/fwlink/?LinkId=122063).</span></span>

## <span data-ttu-id="f3b16-127">Entfernen von OSD-Dateitypzuordnungen</span><span class="sxs-lookup"><span data-stu-id="f3b16-127">Removing OSD File Type Associations</span></span>


<span data-ttu-id="f3b16-128">Wenn Ihre Organisation nicht von Benutzern verlangt, Anwendungen direkt aus einer OSD-Datei zu öffnen, können Sie die Sicherheit erhöhen, indem Sie die Dateitypzuordnungen auf dem Client entfernen.</span><span class="sxs-lookup"><span data-stu-id="f3b16-128">If your organization does not require users to open applications directly from an OSD file, you can enhance security by removing the file type associations on the client.</span></span> <span data-ttu-id="f3b16-129">Entfernen Sie die `HKEY_CURRENT_USERS` Tasten für OSD und `Softgird.osd.file` verwenden Sie den Registrierungs-Editor.</span><span class="sxs-lookup"><span data-stu-id="f3b16-129">Remove the `HKEY_CURRENT_USERS` keys for OSD and `Softgird.osd.file` by using the registry editor.</span></span> <span data-ttu-id="f3b16-130">Sie können diesen Prozess in ein Anmeldeskript oder in ein Skript nach der Installation einfügen, um diese Änderungen zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="f3b16-130">You can put this process into a logon script or into a post-installation script to automate these changes.</span></span>

 

 





