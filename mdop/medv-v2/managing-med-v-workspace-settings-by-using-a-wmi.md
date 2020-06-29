---
title: Verwalten von MED-V-Arbeitsbereichseinstellungen mit einer WMI
description: Verwalten von MED-V-Arbeitsbereichseinstellungen mit einer WMI
author: dansimp
ms.assetid: 05a665a3-2309-46c1-babb-a3e3bbb0b1f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e74e6fa4944ce0dacd5503baec73044b231abe83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811572"
---
# <span data-ttu-id="65b9b-103">Verwalten von MED-V-Arbeitsbereichseinstellungen mit einer WMI</span><span class="sxs-lookup"><span data-stu-id="65b9b-103">Managing MED-V Workspace Settings by Using a WMI</span></span>


<span data-ttu-id="65b9b-104">Sie können die Windows-Verwaltungsinstrumentation (WMI) in Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 verwenden, um Ihre aktuellen Konfigurationseinstellungen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="65b9b-104">You can use Windows Management Instrumentation (WMI) in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 to manage your current configuration settings.</span></span>

## <span data-ttu-id="65b9b-105">So verwalten Sie MED-V-Arbeitsbereichseinstellungen mit einer WMI</span><span class="sxs-lookup"><span data-stu-id="65b9b-105">To manage MED-V workspace settings with a WMI</span></span>


<span data-ttu-id="65b9b-106">Mit einem WMI-Browser Tool können Sie die Einstellungen in einem MED-V-Arbeitsbereich anzeigen und bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="65b9b-106">A WMI browsing tool lets you view and edit the settings in a MED-V workspace.</span></span> <span data-ttu-id="65b9b-107">Der WMI-Anbieter wird mithilfe des WMI-Anbieter Erweiterungs Frameworks von Microsoft .NET Framework 3,5 implementiert.</span><span class="sxs-lookup"><span data-stu-id="65b9b-107">The WMI provider is implemented by using the WMI Provider Extension framework from the Microsoft .Net Framework 3.5.</span></span>

<span data-ttu-id="65b9b-108">Der WMI-Anbieter wird im **root\\microsoft\\medv** -Namespace implementiert und implementiert die Klassen **Einstellung**.</span><span class="sxs-lookup"><span data-stu-id="65b9b-108">The WMI provider is implemented in the **root\\microsoft\\medv** namespace and implements the class **Setting**.</span></span> <span data-ttu-id="65b9b-109">Die Kurs **Einstellung** enthält Eigenschaften, die den Einstellungen in der Systemregistrierung unter dem Registrierungsschlüssel HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\medv entsprechen.</span><span class="sxs-lookup"><span data-stu-id="65b9b-109">The class **Setting** contains properties that correspond to the settings in the system registry under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv registry key.</span></span>

<span data-ttu-id="65b9b-110">**Vorsicht**  Mithilfe der WMI-Browser Tools können Klassen und Instanzen gelöscht oder geändert werden.</span><span class="sxs-lookup"><span data-stu-id="65b9b-110">**Caution** WMI browsing tools can be used to delete or modify classes and instances.</span></span> <span data-ttu-id="65b9b-111">Das Löschen oder Ändern bestimmter Klassen und Instanzen kann zu einem Verlustwert voller Daten führen und dazu führen, dass MED-V unvorhersehbar funktioniert.</span><span class="sxs-lookup"><span data-stu-id="65b9b-111">Deleting or modifying certain classes and instances can result in the loss of valuable data and cause MED-V to function unpredictably.</span></span>

 

<span data-ttu-id="65b9b-112">Sie können Ihr bevorzugtes WMI-Browser Tool verwenden, um MED-V-Konfigurationseinstellungen anzuzeigen und zu bearbeiten, indem Sie die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="65b9b-112">You can use your preferred WMI browsing tool to view and edit MED-V configuration settings by following these steps.</span></span>

1.  <span data-ttu-id="65b9b-113">Öffnen Sie das bevorzugte WMI-Browser Tool mit Administratorberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="65b9b-113">Open your preferred WMI browsing tool with administrator permissions.</span></span>

2.  <span data-ttu-id="65b9b-114">Stellen Sie eine Verbindung mit dem Namespace **root\\microsoft\\medv**.</span><span class="sxs-lookup"><span data-stu-id="65b9b-114">Connect to the namespace **root\\microsoft\\medv**.</span></span>

3.  <span data-ttu-id="65b9b-115">Auflisten der Instanzen, um eine Verbindung mit der ausgeführten Instanz herzustellen</span><span class="sxs-lookup"><span data-stu-id="65b9b-115">Enumerate the instances to connect to the running instance.</span></span> <span data-ttu-id="65b9b-116">Sie möchten eine Verbindung mit der Instanz der Klassen **Einstellung**herstellen.</span><span class="sxs-lookup"><span data-stu-id="65b9b-116">You want to connect to the instance of the class **Setting**.</span></span>

    <span data-ttu-id="65b9b-117">Ein **Objekt-Editor-** Fenster wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="65b9b-117">An **Object Editor** window opens.</span></span> <span data-ttu-id="65b9b-118">Die MED-V-Konfigurationseinstellungen werden als **Eigenschaften**aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="65b9b-118">The MED-V configuration settings are listed as **Properties**.</span></span>

<span data-ttu-id="65b9b-119">Führen Sie die folgenden Schritte aus, um eine MED-V-Konfigurationseinstellung in der WMI zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="65b9b-119">Perform the following steps to edit a MED-V configuration setting in the WMI.</span></span>

1.  <span data-ttu-id="65b9b-120">Doppelklicken Sie in der Liste der **Eigenschaften** im **Objekt-Editor** -Fenster auf den Namen der Konfigurationseinstellung, die Sie bearbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="65b9b-120">In the list of **Properties** on the **Object Editor** window, double-click the name of the configuration setting you want to edit.</span></span> <span data-ttu-id="65b9b-121">Um beispielsweise MED-V-URL-Umleitungsinformationen zu bearbeiten, doppelklicken Sie auf die Eigenschaft **UxRedirectUrls**.</span><span class="sxs-lookup"><span data-stu-id="65b9b-121">For example, to edit MED-V URL redirection information, double-click the property **UxRedirectUrls**.</span></span>

    <span data-ttu-id="65b9b-122">Ein **Eigenschaften-Editor-** Fenster wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="65b9b-122">A **Property Editor** window opens.</span></span>

2.  <span data-ttu-id="65b9b-123">Bearbeiten Sie den Wert, um die Konfigurationsinformationen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="65b9b-123">Edit the value to update the configuration information.</span></span> <span data-ttu-id="65b9b-124">Wenn Sie beispielsweise MED-V-URL-Umleitungsinformationen bearbeiten möchten, fügen Sie eine Webadresse in der Liste hinzu, oder entfernen Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="65b9b-124">For example, to edit MED-V URL redirection information, add or remove a web address in the list.</span></span>

3.  <span data-ttu-id="65b9b-125">Speichern Sie die aktualisierten Eigenschafteneinstellungen.</span><span class="sxs-lookup"><span data-stu-id="65b9b-125">Save the updated property settings.</span></span>

<span data-ttu-id="65b9b-126">Nachdem Sie die MED-V-Konfigurationseinstellungen angezeigt oder bearbeitet haben, schließen Sie das WMI-Browser Tool.</span><span class="sxs-lookup"><span data-stu-id="65b9b-126">After you have finished viewing or editing MED-V configuration settings, close the WMI browsing tool.</span></span>

<span data-ttu-id="65b9b-127">**Wichtig**  In einigen Fällen ist ein Neustart des Med-v-Arbeitsbereichs erforderlich, damit Änderungen an den Med-v-Konfigurationseinstellungen wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="65b9b-127">**Important** In some cases, a restart of the MED-V workspace is required for changes to MED-V configuration settings to take effect.</span></span>

 

<span data-ttu-id="65b9b-128">Der folgende Code zeigt die MOF-Datei (Managed Object Format), die die **Setting** -Klasse definiert.</span><span class="sxs-lookup"><span data-stu-id="65b9b-128">The following code shows the Managed Object Format (MOF) file that defines the **Setting** class.</span></span>

``` syntax
[dynamic: ToInstance, provider("TroubleShooting, Version=2.0.392.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"), singleton: DisableOverride ToInstance ToSubClass]
class Setting : ConfigValueProvider
{
                boolean UxSmartCardLogonEnabled = TRUE;
                [read] string User;
                [implemented] void Clear([in] string propertyName);
};
```

<span data-ttu-id="65b9b-129">Die **Setting** -Klasse erbt von der **ConfigValueProvider** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="65b9b-129">The **Setting** class inherits from the **ConfigValueProvider** class.</span></span> <span data-ttu-id="65b9b-130">Der folgende Code zeigt die MOF-Datei (Managed Object Format), die die **ConfigValueProvider** -Klasse definiert.</span><span class="sxs-lookup"><span data-stu-id="65b9b-130">The following code shows the Managed Object Format (MOF) file that defines the **ConfigValueProvider** class.</span></span>

``` syntax
[abstract]
class ConfigValueProvider
{
                [write] string DiagEventLogLevel;
                [write] boolean FtsAddUserToAdminGroupEnabled;
                [write] string FtsComputerNameMask;
                [write] sint32 FtsDeleteVMStateTimeout;
                [write] sint32 FtsDetachVfdTimeout;
                [write] string FtsDialogUrl;
                [write] sint32 FtsExplorerTimeout;
                [write] string FtsFailureDialogMsg;
                [write] string FtsLogFilePaths[];
                [write] sint32 FtsMaxPostponeTime;
                [write] sint32 FtsMaxRetryCount;
                [write] string FtsMode;
                [write] sint32 FtsNonInteractiveRetryTimeoutInc;
                [write] sint32 FtsNonInteractiveTimeout;
                [write] string FtsPostponeUtcDateTimeLimit;
                [write] string FtsRetryDialogMsg;
                [write] boolean FtsSetComputerNameEnabled;
                [write] boolean FtsSetJoinDomainEnabled;
                [write] boolean FtsSetMachineObjectOUEnabled;
                [write] boolean FtsSetRegionalSettingsEnabled;
                [write] boolean FtsSetUserDataEnabled;
                [write] string FtsStartDialogMsg;
                [write] sint32 FtsTaskCancelTimeout;
                [write] sint32 FtsTaskVMTurnOffTimeout;
                [write] sint32 FtsUpgradeTimeout;
                [write] boolean UxAppPublishingEnabled;
                [write] boolean UxAudioSharingEnabled;
                [write] boolean UxClipboardSharingEnabled;
                [write] boolean UxCredentialCacheEnabled;
                [write] sint32 UxDialogTimeout;
                [write] sint32 UxHideVmTimeout;
                [write] boolean UxLogonStartEnabled;
                [write] boolean UxPrinterSharingEnabled;
                [write] sint32 UxRebootAbsoluteDelayTimeout;
                [write] string UxRedirectUrls[];
                [write] boolean UxShowExit;
                [write] boolean UxSmartCardLogonEnabled;
                [write] boolean UxSmartCardSharingEnabled;
                [write] boolean UxUSBDeviceSharingEnabled;
                [write] string VmCloseAction;
                [write] sint32 VmGuestMemFromHostMem[];
                [write] sint32 VmGuestUpdateDuration;
                [write] string VmGuestUpdateTime;
                [write] sint32 VmHostMemToGuestMem[];
                [write] boolean VmHostMemToGuestMemCalcEnabled;
                [write] sint32 VmMemory;
                [write] boolean VmMultiUserEnabled;
                [write] string VmNetworkingMode;
                [write] sint32 VmTaskTimeout;
};
```

## <span data-ttu-id="65b9b-131">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="65b9b-131">Related topics</span></span>


[<span data-ttu-id="65b9b-132">Verwalten von Konfigurationseinstellungen für MED-V-Arbeitsbereiche</span><span class="sxs-lookup"><span data-stu-id="65b9b-132">Managing MED-V Workspace Configuration Settings</span></span>](managing-med-v-workspace-configuration-settings.md)

[<span data-ttu-id="65b9b-133">Verwalten von MED-V-Arbeitsbereichseinstellungen</span><span class="sxs-lookup"><span data-stu-id="65b9b-133">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





