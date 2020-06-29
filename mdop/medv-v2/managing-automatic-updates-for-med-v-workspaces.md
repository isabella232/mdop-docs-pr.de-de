---
title: Verwalten von automatischen Updates für MED-V-Arbeitsbereiche
description: Verwalten von automatischen Updates für MED-V-Arbeitsbereiche
author: dansimp
ms.assetid: 306f28a2-d653-480d-b737-4b8b3132de5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b22d3250db806e740c1d62da4fed98d5956b0eeb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811068"
---
# <span data-ttu-id="a7ecb-103">Verwalten von automatischen Updates für MED-V-Arbeitsbereiche</span><span class="sxs-lookup"><span data-stu-id="a7ecb-103">Managing Automatic Updates for MED-V Workspaces</span></span>


<span data-ttu-id="a7ecb-104">Der MED-V-Arbeitsbereich ist ein virtueller Computer, der ein separates Betriebssystem enthält, dessen automatischer Softwareupdateprozess genauso wie die physischen Computer in Ihrem Unternehmen verwaltet werden muss.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-104">The MED-V workspace is a virtual machine that contains a separate operating system, whose automatic software update process must be managed just like the physical computers in your enterprise.</span></span> <span data-ttu-id="a7ecb-105">Da das Gastbetriebssystem nicht immer unbedingt ausgeführt wird, wenn das Betriebssystem des Hosts ausgeführt wird, müssen Sie sicherstellen, dass der virtuelle MED-V-Computer so konfiguriert ist, dass Softwareupdates nach Bedarf auf das Gastbetriebssystem angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-105">Because the guest operating system is not always necessarily running when the host operating system is running, you must ensure that the MED-V virtual machine is configured in such a way that software updates can be applied to the guest operating system as required.</span></span> <span data-ttu-id="a7ecb-106">Die Microsoft Enterprise Desktop Virtualization (Med-v) 2,0-Lösung bietet die Funktionalität, mit der Sie ermitteln können, wie automatische Softwareupdates in einem MED-V-Arbeitsbereich verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-106">The Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 solution provides the functionality that lets you determine how automatic software updates are processed in a MED-V workspace.</span></span>

## <span data-ttu-id="a7ecb-107">Verwalten der Wake-up-Richtlinie für den MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="a7ecb-107">Managing MED-V Workspace Wake-Up Policy</span></span>


<span data-ttu-id="a7ecb-108">Die Wake-up-Richtlinie für med-v Workspace garantiert, dass der virtuelle Med-v-Computer für den Zeitraum, den Sie in ihren Med-v-Konfigurationseinstellungen angeben, für Updates zur Verfügung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-108">The MED-V workspace wake-up policy guarantees that the MED-V virtual machine is made available for updates for the time that you specify in your MED-V configuration settings.</span></span> <span data-ttu-id="a7ecb-109">Dies gilt sowohl für Updates, die von Microsoft über Windows Update veröffentlicht werden, als auch für Updates, die von nicht von Microsoft bereitgestellten Lösungen wie Antivirus-Anwendungen bereitgestellt und gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-109">This applies to both updates that are published from Microsoft through Windows Update and updates deployed and controlled by non-Microsoft solutions, such as antivirus applications.</span></span>

<span data-ttu-id="a7ecb-110">**Wichtig**  Die Wake-up-Richtlinie für den MED-V-Arbeitsbereich wurde für die Microsoft Update-Infrastruktur optimiert.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-110">**Important** The MED-V workspace wake-up policy is optimized for the Microsoft Update infrastructure.</span></span> <span data-ttu-id="a7ecb-111">Wenn Sie Microsoft System Center Configuration Manager zum Bereitstellen von nicht-Microsoft-Updates verwenden, empfiehlt es sich, auch den System Center Updates Publisher zu verwenden, der die gleiche Infrastruktur wie Microsoft Update nutzt und daher von der Wake-up-Richtlinie des MED-V-Arbeitsbereichs profitiert.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-111">If you are using Microsoft System Center Configuration Manager to deploy non-Microsoft updates, we recommend that you also use the System Center Updates Publisher, which takes advantage of the same infrastructure as Microsoft Update and therefore benefits from the MED-V workspace wake-up policy.</span></span> <span data-ttu-id="a7ecb-112">Weitere Informationen finden Sie unter [System Center Updates Publisher](https://go.microsoft.com/fwlink/?LinkId=200035) ( https://go.microsoft.com/fwlink/?LinkId=200035) .</span><span class="sxs-lookup"><span data-stu-id="a7ecb-112">For more information, see [System Center Updates Publisher](https://go.microsoft.com/fwlink/?LinkId=200035) (https://go.microsoft.com/fwlink/?LinkId=200035).</span></span>

 

<span data-ttu-id="a7ecb-113">Beim Erstellen Ihres MED-V-Arbeitsbereichs Pakets haben Sie festgelegt, wann und wie es gestartet wird, entweder, wenn sich der Endbenutzer anmeldet (**Fast Start**) oder wenn der Endbenutzer zuerst eine veröffentlichte Anwendung öffnet (**normaler Anfang**).</span><span class="sxs-lookup"><span data-stu-id="a7ecb-113">When you created your MED-V workspace package, you configured when and how it starts, either when the end user logs on (**Fast Start**) or when the end user first opens a published application (**Normal Start**).</span></span> <span data-ttu-id="a7ecb-114">Sie können aber auch die Option festlegen, mit der der Endbenutzer diese Einstellung steuern kann.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-114">Or you set the option to let the end user control this setting.</span></span>

<span data-ttu-id="a7ecb-115">So oder so, wenn die Option " **schnell Start** " ausgewählt ist, wird der virtuelle Computer weiterhin ausgeführt, solange der MED-V-Host als Benutzer angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-115">Either way, whenever the **Fast Start** option is selected, the virtual machine continues to run as long as the MED-V host is logged on as User.</span></span> <span data-ttu-id="a7ecb-116">Da Med-v in dieser Konfiguration aktiv ist, wenn der Host aktiv ist, werden automatische Updates angewendet, ohne dass eine zusätzliche Verarbeitung von Med-v erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-116">In this configuration, because MED-V is active when the host is active, automatic updates are applied without requiring any extra processing from MED-V.</span></span>

<span data-ttu-id="a7ecb-117">In den Fällen, in denen " **schnell Start** " nicht angegeben ist oder der virtuelle Computer in den Ruhezustand versetzt wird oder beendet wird, garantiert Med-v über die Wake-up-Richtlinie des Med-v-Arbeitsbereichs, dass das Gastbetriebssystem regelmäßig aktualisiert wird, auch wenn Med-v nicht regelmäßig verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-117">However, for those cases in which **Fast Start** is not specified or the virtual machine hibernates or stops, MED-V guarantees through its MED-V workspace wake-up policy that the guest operating system is being regularly updated even when MED-V is not used regularly.</span></span> <span data-ttu-id="a7ecb-118">MED-V führt diese Funktion aus, indem Sie den virtuellen Computerregel mäßig basierend auf den von Ihnen angegebenen Konfigurationseinstellungen aufweckt.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-118">MED-V performs this function by regularly waking up the virtual machine based on the configuration settings that you specify.</span></span> <span data-ttu-id="a7ecb-119">Auf diese Weise können die Clients für automatische Updates auf dem virtuellen Computer basierend auf Ihren Konfigurationen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-119">This enables the automatic update clients in the virtual machine to execute based on their configurations.</span></span><span data-ttu-id="a7ecb-120">Nachdem der durch die Med-v-Konfigurationseinstellung definierte Zeitraum abgelaufen ist, gibt Med-v den virtuellen Computer in seinen vorherigen Zustand zurück.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-120">After the time period defined by the MED-V configuration setting elapses, MED-V returns the virtual machine to its previous state.</span></span>

<span data-ttu-id="a7ecb-121">**Hinweis**  Wenn der Endbenutzer während des Aktualisierungszeitraums eine veröffentlichte Anwendung öffnet, werden die erforderlichen Updates angewendet, aber MED-V wird nicht automatisch in den Ruhezustand versetzt oder nach dem Ende des Aktualisierungszeitraums beendet.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-121">**Note** If the end user opens a published application during the update period, the required updates are applied, but MED-V is not automatically hibernated or shut down after the update period ends.</span></span> <span data-ttu-id="a7ecb-122">Stattdessen wird MED-V weiterhin ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-122">Instead, MED-V continues running.</span></span>

 

<span data-ttu-id="a7ecb-123">Die Wake-up-Richtlinie für den MED-V-Arbeitsbereich umfasst drei Hauptkomponenten:</span><span class="sxs-lookup"><span data-stu-id="a7ecb-123">The MED-V workspace wake-up policy includes three main components:</span></span>

**<span data-ttu-id="a7ecb-124">Gast Update-Manager</span><span class="sxs-lookup"><span data-stu-id="a7ecb-124">Guest Update Manager</span></span>**

<span data-ttu-id="a7ecb-125">Dieses eigenständige ausführbare Programm, das sich auf dem MED-V-Host befindet, ist für das Aufwachen des virtuellen Computers entsprechend einem vordefinierten, konfigurierbaren Zeitplan verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-125">Residing on the MED-V host, this stand-alone executable program is responsible for waking up the virtual machine according to a predefined, configurable schedule.</span></span> <span data-ttu-id="a7ecb-126">Geben Sie die Konfigurationseinstellungen an, um anzugeben, zu welchem Zeitpunkt der Update-Manager jeden Tag den virtuellen Computer reaktivieren soll, und wie lange die virtuelle Maschine wach gehalten werden soll (in Minuten), damit Updates angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-126">Specify the configuration settings to indicate at what time the update manager should wake up the virtual machine every day, and how long the virtual machine should be kept awake (in minutes) to allow for updates to be applied.</span></span> <span data-ttu-id="a7ecb-127">Nachdem die angegebene Anzahl von Minuten erreicht wurde, versetzt der gastupdate-Manager den virtuellen Computer in den Ruhezustand, der für die nächste Verwendung vorbereitet wurde.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-127">After the number of minutes specified has been reached, the guest update manager puts the virtual machine into hibernation, prepared for the next use.</span></span> <span data-ttu-id="a7ecb-128">Sie können die Ausführung dieses ausführbaren Programms über den Windows Task-Manager planen.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-128">You can schedule the execution of this executable program through the Windows Task Manager.</span></span>

**<span data-ttu-id="a7ecb-129">Verwaltungsdienst für Gast Neustart</span><span class="sxs-lookup"><span data-stu-id="a7ecb-129">Guest Restart Management Service</span></span>**

<span data-ttu-id="a7ecb-130">Dieser Dienst, der sich auf dem MED-V-Host befindet, hat drei Hauptaufgaben.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-130">Residing on the MED-V host, this service has three primary responsibilities.</span></span> <span data-ttu-id="a7ecb-131">Zusammen mit dem Guest Update Manager verwaltet er den Neustart des virtuellen Computers bei der Benutzeranmeldung, falls dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-131">Along with the Guest Update Manager, it manages the restart of the virtual machine at user logon, if it is required.</span></span> <span data-ttu-id="a7ecb-132">Sie erkennt, dass ein Neustart von virtuellen Maschinen erforderlich ist, wenn Updates installiert werden.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-132">It detects when virtual machine restarts are required caused by updates being installed.</span></span> <span data-ttu-id="a7ecb-133">Und es wird sichergestellt, dass die Aufgabe für den Guest Update Manager immer entsprechend der Konfiguration geplant wird.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-133">And it ensures that the task for the Guest Update Manager is always scheduled according to configuration.</span></span>

**<span data-ttu-id="a7ecb-134">Gast Aktualisierungsdienst</span><span class="sxs-lookup"><span data-stu-id="a7ecb-134">Guest Update Service</span></span>**

<span data-ttu-id="a7ecb-135">Dieser Windows-Dienst, der sich auf dem virtuellen MED-V-Computer befindet, ist dafür verantwortlich, zu überwachen, wenn für installierte Updates ein Neustart erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-135">Residing on the MED-V virtual machine, this Windows service has the responsibility of monitoring when installed updates require a restart.</span></span> <span data-ttu-id="a7ecb-136">Nachdem dem Dienst mitgeteilt wird, dass ein Neustart erforderlich ist, benachrichtigt er den Guest-Neustart-Verwaltungsdienst auf dem Host.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-136">After the service becomes aware of the need for a restart, it notifies the guest restart management service on the host.</span></span>

### <span data-ttu-id="a7ecb-137">Konfigurationseinstellungen für die Wake-up-Richtlinie für den MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="a7ecb-137">Configuration Settings for MED-V Workspace Wake-Up Policy</span></span>

<span data-ttu-id="a7ecb-138">Sie steuern, wann und wie lange der virtuelle Computer aufwacht, um automatische Updates zu erhalten, indem Sie die folgenden zwei Konfigurationswerte in der Registrierung definieren.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-138">You control when and for how long the virtual machine awakens to receive automatic updates by defining the following two configuration values in the registry.</span></span> <span data-ttu-id="a7ecb-139">Beide Werte befinden sich unter dem HKLM\\Software\\Microsoft\\MEDV\\v2\\VM-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-139">Both of these values are located under the HKLM\\Software\\Microsoft\\MEDV\\v2\\VM key.</span></span>

<span data-ttu-id="a7ecb-140">**GuestUpdateTime** – konfiguriert die Stunden und Minuten pro Tag, wenn MED-V den virtuellen Computer zum Aktualisieren basierend auf dem 24-Stunden-Standard der Uhr reaktivieren muss.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-140">**GuestUpdateTime** – Configures the hour and minute each day when MED-V must wake up the virtual machine for updating, based on the 24-hour clock standard.</span></span> <span data-ttu-id="a7ecb-141">Geben Sie die Uhrzeit im Format hh: mm ein.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-141">Specify the time in the format HH:MM.</span></span> <span data-ttu-id="a7ecb-142">Der Standardwert ist 00:00 (Midnight).</span><span class="sxs-lookup"><span data-stu-id="a7ecb-142">The default value is 00:00 (midnight).</span></span>

<span data-ttu-id="a7ecb-143">**GuestUpdateDuration** – konfiguriert die Anzahl der Minuten, für die MED-V den virtuellen Computer für die Aktualisierung wach halten muss, beginnend mit der in der GuestUpdateTime-Konfigurationseinstellung angegebenen Zeit.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-143">**GuestUpdateDuration** – Configures the number of minutes that MED-V must keep the virtual machine awake for updating, starting at the time specified in the GuestUpdateTime configuration setting.</span></span> <span data-ttu-id="a7ecb-144">Der Standardwert ist 240 (4 Stunden).</span><span class="sxs-lookup"><span data-stu-id="a7ecb-144">The default value is 240 (4 hours).</span></span> <span data-ttu-id="a7ecb-145">Wenn dieser Wert auf 0 (null) festgelegt wird, wird die Wake-up-Richtlinie für den MED-V-Arbeitsbereich deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-145">Setting this value to zero (0) disables the MED-V workspace wake-up policy.</span></span>

<span data-ttu-id="a7ecb-146">Weitere Informationen zum Definieren Ihrer Med-v-Konfigurationswerte finden Sie unter [Verwalten von Med-v Workspace-Konfigurationseinstellungen](managing-med-v-workspace-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="a7ecb-146">For more information about how to define your MED-V configuration values, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).</span></span>

<span data-ttu-id="a7ecb-147">**Hinweis**  Eine optimale Methode für med-v besteht darin, das Aktivierungsintervall so einzurichten, dass es der Zeit entspricht, zu der die virtuellen Med-v-Maschinen regelmäßig aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-147">**Note** A MED-V best practice is to set your wake up interval to match the time when MED-V virtual machines are planned to be updated regularly.</span></span> <span data-ttu-id="a7ecb-148">Darüber hinaus empfiehlt es sich, diese Einstellungen so zu konfigurieren, dass Sie dem Verhalten des Hostcomputers ähneln.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-148">In addition, we recommend that you configure these settings to resemble the host computer’s behavior.</span></span>

 

### <span data-ttu-id="a7ecb-149">Neustart der Benachrichtigung mithilfe Ihres ESD-Systems</span><span class="sxs-lookup"><span data-stu-id="a7ecb-149">Reboot Notification Using your ESD System</span></span>

<span data-ttu-id="a7ecb-150">Sie können Ihr ESD-System so konfigurieren, dass es Med-v benachrichtigt, wenn ein Neustart für den Med-v-Arbeitsbereich erforderlich ist, nachdem automatische Updates angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-150">You can configure your ESD system to notify MED-V whenever a restart is required for the MED-V workspace after automatic updates have been applied.</span></span> <span data-ttu-id="a7ecb-151">Wenn Sie automatische Updates über Ihr ESD-System anwenden und wissen, dass ein Neustart erforderlich ist, sollten Sie ein Skript schreiben, um das folgende globale Ereignis im MED-V-Arbeitsbereich zu signalisieren:</span><span class="sxs-lookup"><span data-stu-id="a7ecb-151">When you apply automatic updates through your ESD system that you know require a restart, you should write a script to signal the following global event on the MED-V workspace:</span></span>

<span data-ttu-id="a7ecb-152">**Wichtig**  Sie müssen das Ereignis mit nur Rechte ändern öffnen und dann signalisieren.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-152">**Important** You must open the event with Modify Only rights and then signal it.</span></span> <span data-ttu-id="a7ecb-153">Wenn Sie es nicht mit den richtigen Berechtigungen öffnen, funktioniert es nicht.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-153">If you do not open it with the correct permissions, it does not work.</span></span>

 

``` syntax
/// <summary>
/// The guest is required to be restarted due to an ESD update.
/// </summary>
public const string MedvGuestRebootRequiredEventName = @"Global\MedvGuestRebootRequiredEvent";
using (EventWaitHandle notificationEvent = 
EventWaitHandle.OpenExisting(eventName, EventWaitHandleRights.Modify))
{
notificationEvent.Set();
}
```

<span data-ttu-id="a7ecb-154">Wenn Sie dieses Ereignis signalisieren, wird es von MED-V erfasst und dem virtuellen Computer darüber informiert, dass ein Neustart erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-154">When you signal this event, MED-V captures it and informs the virtual machine that a restart is required.</span></span>

## <span data-ttu-id="a7ecb-155">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a7ecb-155">Related topics</span></span>


[<span data-ttu-id="a7ecb-156">Verwalten von Softwareupdates für MED-V-Arbeitsbereiche</span><span class="sxs-lookup"><span data-stu-id="a7ecb-156">Managing Software Updates for MED-V Workspaces</span></span>](managing-software-updates-for-med-v-workspaces.md)

 

 





