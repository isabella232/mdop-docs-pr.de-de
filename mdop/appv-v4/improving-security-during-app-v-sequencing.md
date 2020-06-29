---
title: Verbessern der Sicherheit während der App-V-Sequenzierung
description: Verbessern der Sicherheit während der App-V-Sequenzierung
author: dansimp
ms.assetid: f30206dd-5749-4a27-bbaf-61fc21b9c663
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ba97c334c4ac9a928fee3d69c265c12e82e43619
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806675"
---
# <span data-ttu-id="6571d-103">Verbessern der Sicherheit während der App-V-Sequenzierung</span><span class="sxs-lookup"><span data-stu-id="6571d-103">Improving Security During App-V Sequencing</span></span>


<span data-ttu-id="6571d-104">Verpackungsanwendungen für die Sequenzierung sind die größte fortlaufende Aufgabe in einer App-V-Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="6571d-104">Packaging applications for sequencing is the largest ongoing task in an App-V infrastructure.</span></span> <span data-ttu-id="6571d-105">Da es sich um eine laufende Aufgabe handelt, sollten Sie sorgfältig die Erstellung von Richtlinien und Verfahren für die Sequenzierung von Anwendungen in Frage stellen.</span><span class="sxs-lookup"><span data-stu-id="6571d-105">Because this task is ongoing, you should carefully consider creating policies and procedures to follow when sequencing applications.</span></span> <span data-ttu-id="6571d-106">In App-v 4.5 können Sie während der Sequenzierung Zugriffssteuerungslisten (ACLs) für die Dateiressourcen der virtualisierten Anwendung aufzeichnen.</span><span class="sxs-lookup"><span data-stu-id="6571d-106">In App-V4.5, during sequencing, you can capture Access Control Lists (ACLs) on the file assets of the virtualized application.</span></span>

## <span data-ttu-id="6571d-107">Virenscan auf dem Sequenzer</span><span class="sxs-lookup"><span data-stu-id="6571d-107">Virus Scanning on the Sequencer</span></span>


<span data-ttu-id="6571d-108">Es wird empfohlen, die Scansoftware auf dem Sequenzcomputer zu installieren und den Computer dann auf Viren und Malware zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="6571d-108">It is a best practice to install the scanning software on the sequencing computer and then scan the computer for viruses and malware.</span></span> <span data-ttu-id="6571d-109">Deaktivieren Sie die Scansoftware, einschließlich aller Antivirus-und Malware Erkennungssoftware, auf dem Sequenzcomputer, bevor Sie alle Anwendungen sequenzieren, nachdem der Sequenzcomputer gescannt und virenfrei oder Malware freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="6571d-109">After the sequencing computer is scanned and free of any viruses or malware, disable the scanning software, including all antivirus and malware detection software, on the sequencing computer before sequencing any applications.</span></span> <span data-ttu-id="6571d-110">Dies beschleunigt den Sequenzierungsprozess und verhindert, dass die Scansoftware Komponenten während der Sequenzierung erkannt und im virtuellen Anwendungspaket enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6571d-110">This speeds the sequencing process and prevents the scanning software components from being detected during sequencing and included in the virtual application package.</span></span>

## <span data-ttu-id="6571d-111">Aufzeichnen von ACLs für Dateien (NTFS)</span><span class="sxs-lookup"><span data-stu-id="6571d-111">Capturing ACLs on Files (NTFS)</span></span>


<span data-ttu-id="6571d-112">Der Sequencer zeichnet NTFS-Berechtigungen (ACLs) für die Dateien auf, die während der Installationsphase der Sequenz Überwachung überwacht werden.</span><span class="sxs-lookup"><span data-stu-id="6571d-112">The Sequencer captures NTFS permissions (the ACLs) for the files that are monitored during the sequencing installation phase.</span></span> <span data-ttu-id="6571d-113">(Vor der Veröffentlichung von App-v 4.5 wurden ACLs nicht als Teil des Sequenz Prozesses erfasst.) Mit diesem neuen Feature können bestimmte Anwendungen für Benutzer mit einer geringen Berechtigungsstufe ausgeführt werden, für die normalerweise Administratorrechte erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="6571d-113">(Before the release of App-V4.5, ACLs were not captured as part of the sequencing process.) This new feature enables certain applications to run for users with a low level of permission that would normally require Administrative privileges.</span></span>

<span data-ttu-id="6571d-114">Dieses Feature ermöglicht es dem Sequenz Ingenieur auch, die vom Hersteller identifizierten Sicherheitseinstellungen zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="6571d-114">This feature also enables the sequencing engineer to capture the security settings identified by the vendor.</span></span> <span data-ttu-id="6571d-115">Wenn die vom Hersteller empfohlenen Einstellungen nicht angewendet werden, kann die Anwendung für Angriffe oder Missbrauch durch die Benutzer geöffnet bleiben.</span><span class="sxs-lookup"><span data-stu-id="6571d-115">Failing to apply the settings recommended by the vendor could leave the application open to attack or misuse by users.</span></span> <span data-ttu-id="6571d-116">Informationen dazu, ob Sie eine Anwendung mit geöffneten ACLs bereitstellen sollten, finden Sie unter Anwendungssupport Gruppe oder Softwarehersteller.</span><span class="sxs-lookup"><span data-stu-id="6571d-116">For information about whether or not you should deploy an application with open ACLs, refer to your application support group or the software vendor.</span></span>

<span data-ttu-id="6571d-117">**Wichtig**  Obwohl der Sequencer die NTFS-ACLs erfasst, während die Installationsphase der Sequenzierung überwacht wird, werden die ACLs für die Registrierung nicht erfasst.</span><span class="sxs-lookup"><span data-stu-id="6571d-117">**Important** Although the sequencer captures the NTFS ACLs while monitoring the installation phase of sequencing, it does not capture the ACLs for the registry.</span></span> <span data-ttu-id="6571d-118">Benutzer haben vollständigen Zugriff auf alle Registrierungsschlüssel für virtuelle Anwendungen mit Ausnahme der Dienste.</span><span class="sxs-lookup"><span data-stu-id="6571d-118">Users have full access to all registry keys for virtual applications except for services.</span></span> <span data-ttu-id="6571d-119">Wenn ein Benutzer jedoch die Registrierung einer virtuellen Anwendung ändert, wird diese Änderung an einem bestimmten Speicherort ( `uservol_sftfs_v1.pkg` ) gespeichert und wirkt sich nicht auf andere Benutzer aus.</span><span class="sxs-lookup"><span data-stu-id="6571d-119">However, if a user modifies the registry of a virtual application, that change is stored in a specific location (`uservol_sftfs_v1.pkg`) and won’t affect other users.</span></span>

 

<span data-ttu-id="6571d-120">Während der Installationsphase kann ein Sequenz Ingenieur die Standardberechtigungen der Dateien bei Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="6571d-120">During the installation phase, a sequencing engineer can modify the default permissions of the files if necessary.</span></span> <span data-ttu-id="6571d-121">Nach Abschluss des Sequenz Prozesses, aber vor dem Speichern des Pakets, kann der Sequenz Ingenieur dann Sicherheitsdeskriptoren erzwingen, die während der Installationsphase aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="6571d-121">After the sequencing process is complete, but before saving the package, the sequencing engineer can then choose to enforce security descriptors that were captured during the installation phase.</span></span> <span data-ttu-id="6571d-122">Es ist eine bewährte Methode, Sicherheitsbeschreibungen zu erzwingen, wenn keine andere Lösung die ordnungsgemäße Ausführung der Anwendung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="6571d-122">It is a best practice to enforce security descriptors if no other solution allows the application to run properly once virtualized.</span></span>

 

 





