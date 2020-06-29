---
title: App-V-Interoperabilität mit Windows AppLocker
description: App-V-Interoperabilität mit Windows AppLocker
author: dansimp
ms.assetid: 9a488034-607d-411c-b495-ff184c726f49
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6f67bb87c0a4474acee3c4982b65c930e86c4917
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809280"
---
# <span data-ttu-id="446f6-103">App-V-Interoperabilität mit Windows AppLocker</span><span class="sxs-lookup"><span data-stu-id="446f6-103">App-V Interoperability with Windows AppLocker</span></span>


<span data-ttu-id="446f6-104">Version 4,5 SP1 des Microsoft Application Virtualization (App-V)-Clients unterstützt das AppLocker-Feature von Windows 7.</span><span class="sxs-lookup"><span data-stu-id="446f6-104">Version 4.5 SP1 of the Microsoft Application Virtualization (App-V) client supports the AppLocker feature of Windows 7.</span></span> <span data-ttu-id="446f6-105">Mit dem AppLocker-Feature können IT-Administratoren angeben, welche Anwendungen für die Ausführung auf Computern eingeschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="446f6-105">The AppLocker feature enables IT administrators to specify which applications are restricted from running on computers.</span></span> <span data-ttu-id="446f6-106">In diesem Dokument wird beschrieben, wie Sie die AppLocker-Regeln für die Verwendung der virtuellen App-V-Umgebung und virtualisierten Anwendungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="446f6-106">This document describes how to configure the AppLocker rules to work with the App-V virtual environment and virtualized applications.</span></span>

<span data-ttu-id="446f6-107">**Hinweis**  Windows-AppLocker muss zuerst aktiviert werden, bevor Windows-AppLocker-Regeln für virtuelle Anwendungen konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="446f6-107">**Note** Windows AppLocker must first be enabled before configuring Windows AppLocker rules for virtual applications.</span></span> <span data-ttu-id="446f6-108">Weitere Informationen zum Aktivieren von Windows AppLocker finden Sie unter [Windows AppLocker](https://go.microsoft.com/fwlink/?LinkId=156732) ( https://go.microsoft.com/fwlink/?LinkId=156732) .</span><span class="sxs-lookup"><span data-stu-id="446f6-108">For more information about enabling Windows AppLocker, [Windows AppLocker](https://go.microsoft.com/fwlink/?LinkId=156732) (https://go.microsoft.com/fwlink/?LinkId=156732).</span></span>

 

## <span data-ttu-id="446f6-109">Konfigurieren von Windows-AppLocker-Regeln für virtuelle Anwendungen</span><span class="sxs-lookup"><span data-stu-id="446f6-109">Configuring Windows AppLocker Rules for Virtual Applications</span></span>


<span data-ttu-id="446f6-110">Lokale Administratoren können Windows-AppLocker-Regeln erstellen, die die Ausführung von ausführbaren Programmen (exe-Dateien), Windows Installer-Dateien (MSI-und MSP-Dateien) und Skripts (PS-, bat-, cmd-, VBS-und JS-Dateien) einschränken.</span><span class="sxs-lookup"><span data-stu-id="446f6-110">Local administrators can create Windows AppLocker rules that restrict the running of program executables (.exe files), Windows Installer files (.msi and .msp files), and scripts (.ps, .bat, .cmd, .vbs and .js files).</span></span> <span data-ttu-id="446f6-111">Der Administrator verwendet dazu einen Referenzcomputer, auf dem der App-V-Client installiert ist und auf dem alle relevanten virtuellen Anwendungen in den Clientcache gestreamt werden.</span><span class="sxs-lookup"><span data-stu-id="446f6-111">The administrator does this by using a reference computer that has the App-V client installed and that has all the relevant virtual applications streamed to the client cache.</span></span> <span data-ttu-id="446f6-112">Der Administrator verwendet dann den Windows-AppLocker-Abschnitt des lokalen Sicherheitsrichtlinien-Snap-Ins Microsoft Management Console (MMC) auf dem Referenzcomputer, um die Regeln zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="446f6-112">The administrator then uses the Windows AppLocker section of the Local Security Policy Microsoft Management Console (MMC) snap-in on the reference computer to create the rules.</span></span>

<span data-ttu-id="446f6-113">Wenn Sie nach einem Verzeichnispfad oder einer bestimmten Datei suchen, für die Sie eine Regel erstellen möchten, können Sie auf das App-V-Laufwerk zugreifen, indem Sie den Pfad zur verborgenen Freigabe verwenden.</span><span class="sxs-lookup"><span data-stu-id="446f6-113">When you browse to find a directory path or specific file for which you want to create a rule, you can access the App-V drive by using the path to the hidden share.</span></span> <span data-ttu-id="446f6-114">So können Sie beispielsweise zu \\\\localhost\\Q $ wechseln, wobei das App-V-Laufwerk Laufwerk Q ist. Um die Regel zu erstellen, müssen Sie den Pfad jedoch bearbeiten, um den Verweis auf \\\\localhost\\Q $ zu entfernen und stattdessen Q:\\ zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="446f6-114">For example, you can browse to \\\\localhost\\Q$, where the App-V drive is drive Q. However, to create the rule, you must edit the path to remove the reference to \\\\localhost\\Q$ and use Q:\\ instead.</span></span> <span data-ttu-id="446f6-115">Sie müssen jede Anwendung auf dem Referenzcomputer starten, um auf die Dateien der Anwendung zuzugreifen, und es sind Administratorrechte erforderlich, um \\\\localhost\\Q $ zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="446f6-115">You must start each application on the reference computer to access the application’s files, and administrative rights are required to browse to \\\\localhost\\Q$.</span></span>

 

 





