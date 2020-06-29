---
title: So konfigurieren Sie Benutzerberechtigungen
description: So konfigurieren Sie Benutzerberechtigungen
author: dansimp
ms.assetid: 54e69f46-b028-4ad1-9b80-f06ef5c8f559
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3c2581a9f9dddcbc63682d356c777a24222dd62f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807224"
---
# <span data-ttu-id="7adb3-103">So konfigurieren Sie Benutzerberechtigungen</span><span class="sxs-lookup"><span data-stu-id="7adb3-103">How to Configure User Permissions</span></span>


<span data-ttu-id="7adb3-104">Sie können einige Aktionen für Benutzer, die nicht über Administratorrechte verfügen, aktivieren und deaktivieren, indem Sie die Schlüsselwerte unter dem Registrierungsschlüssel " **Berechtigungen** " Bearbeiten (HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\permissions).</span><span class="sxs-lookup"><span data-stu-id="7adb3-104">You can enable and disable some actions for users who do not have administrative rights by editing the key values under the **Permissions** registry key (HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions).</span></span> <span data-ttu-id="7adb3-105">Dieser Schlüssel dient in erster Linie dazu, Benutzer daran zu hindern, Fehler zu machen, anstatt besondere Sicherheit zu gewährleisten, da Benutzer mit Administratorrechten einen dieser Schlüsselwerte bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="7adb3-105">This key is primarily designed to help prevent users from making mistakes rather than to provide any special security, because users with administrative rights can edit any of these key values.</span></span> <span data-ttu-id="7adb3-106">Die folgenden Verfahren sind Beispiele für das Ändern der Schlüsselwerte.</span><span class="sxs-lookup"><span data-stu-id="7adb3-106">The following procedures are examples of how to change the key values.</span></span> <span data-ttu-id="7adb3-107">Weitere Informationen zu den Registrierungsschlüsseln und Werten der Application Virtualization (App-V)-Client Registrierung finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=121528> .</span><span class="sxs-lookup"><span data-stu-id="7adb3-107">For more information about the Application Virtualization (App-V) Client registry keys and values, see <https://go.microsoft.com/fwlink/?LinkId=121528>.</span></span>

**<span data-ttu-id="7adb3-108">So ändern Sie die Benutzerberechtigungen</span><span class="sxs-lookup"><span data-stu-id="7adb3-108">To change user permissions</span></span>**

1.  <span data-ttu-id="7adb3-109">Damit die Benutzer den Client im Offlinemodus ausführen können, legen Sie den folgenden Schlüsselwert auf 1:</span><span class="sxs-lookup"><span data-stu-id="7adb3-109">To enable the users to choose to run the client in offline mode, set the following key value to 1:</span></span>

    <span data-ttu-id="7adb3-110">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\permissions\\toggleofflinemode</span><span class="sxs-lookup"><span data-stu-id="7adb3-110">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ToggleOfflineMode</span></span>

2.  <span data-ttu-id="7adb3-111">Damit die Benutzer alle Anwendungen über die Benutzeroberfläche anzeigen können, müssen Sie den folgenden Schlüsselwert auf 1 festlegen.</span><span class="sxs-lookup"><span data-stu-id="7adb3-111">To enable the users to view all applications through the user interface, set the following key value to 1.</span></span> <span data-ttu-id="7adb3-112">Wenn der Wert auf 0 (null) festgelegt wird, können die Benutzer nur die Anwendungen sehen, die Ihnen zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="7adb3-112">Setting the value to 0 (zero) allows the users to see only the applications that are available to them.</span></span>

    <span data-ttu-id="7adb3-113">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\permissions\\viewallapplications</span><span class="sxs-lookup"><span data-stu-id="7adb3-113">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ViewAllApplications</span></span>

## <span data-ttu-id="7adb3-114">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7adb3-114">Related topics</span></span>


[<span data-ttu-id="7adb3-115">So konfigurieren Sie die App-V-Client-Registrierungseinstellungen über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="7adb3-115">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

[<span data-ttu-id="7adb3-116">Benutzerzugriffsberechtigungen in Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="7adb3-116">User Access Permissions in Application Virtualization Client</span></span>](user-access-permissions-in-application-virtualization-client.md)

 

 





