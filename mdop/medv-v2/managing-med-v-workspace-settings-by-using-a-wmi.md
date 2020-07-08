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
# Verwalten von MED-V-Arbeitsbereichseinstellungen mit einer WMI


Sie können die Windows-Verwaltungsinstrumentation (WMI) in Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 verwenden, um Ihre aktuellen Konfigurationseinstellungen zu verwalten.

## So verwalten Sie MED-V-Arbeitsbereichseinstellungen mit einer WMI


Mit einem WMI-Browser Tool können Sie die Einstellungen in einem MED-V-Arbeitsbereich anzeigen und bearbeiten. Der WMI-Anbieter wird mithilfe des WMI-Anbieter Erweiterungs Frameworks von Microsoft .NET Framework 3,5 implementiert.

Der WMI-Anbieter wird im **root\\microsoft\\medv** -Namespace implementiert und implementiert die Klassen **Einstellung**. Die Kurs **Einstellung** enthält Eigenschaften, die den Einstellungen in der Systemregistrierung unter dem Registrierungsschlüssel HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\medv entsprechen.

**Vorsicht**  Mithilfe der WMI-Browser Tools können Klassen und Instanzen gelöscht oder geändert werden. Das Löschen oder Ändern bestimmter Klassen und Instanzen kann zu einem Verlustwert voller Daten führen und dazu führen, dass MED-V unvorhersehbar funktioniert.

 

Sie können Ihr bevorzugtes WMI-Browser Tool verwenden, um MED-V-Konfigurationseinstellungen anzuzeigen und zu bearbeiten, indem Sie die folgenden Schritte ausführen.

1.  Öffnen Sie das bevorzugte WMI-Browser Tool mit Administratorberechtigungen.

2.  Stellen Sie eine Verbindung mit dem Namespace **root\\microsoft\\medv**.

3.  Auflisten der Instanzen, um eine Verbindung mit der ausgeführten Instanz herzustellen Sie möchten eine Verbindung mit der Instanz der Klassen **Einstellung**herstellen.

    Ein **Objekt-Editor-** Fenster wird geöffnet. Die MED-V-Konfigurationseinstellungen werden als **Eigenschaften**aufgelistet.

Führen Sie die folgenden Schritte aus, um eine MED-V-Konfigurationseinstellung in der WMI zu bearbeiten.

1.  Doppelklicken Sie in der Liste der **Eigenschaften** im **Objekt-Editor** -Fenster auf den Namen der Konfigurationseinstellung, die Sie bearbeiten möchten. Um beispielsweise MED-V-URL-Umleitungsinformationen zu bearbeiten, doppelklicken Sie auf die Eigenschaft **UxRedirectUrls**.

    Ein **Eigenschaften-Editor-** Fenster wird geöffnet.

2.  Bearbeiten Sie den Wert, um die Konfigurationsinformationen zu aktualisieren. Wenn Sie beispielsweise MED-V-URL-Umleitungsinformationen bearbeiten möchten, fügen Sie eine Webadresse in der Liste hinzu, oder entfernen Sie Sie.

3.  Speichern Sie die aktualisierten Eigenschafteneinstellungen.

Nachdem Sie die MED-V-Konfigurationseinstellungen angezeigt oder bearbeitet haben, schließen Sie das WMI-Browser Tool.

**Wichtig**  In einigen Fällen ist ein Neustart des Med-v-Arbeitsbereichs erforderlich, damit Änderungen an den Med-v-Konfigurationseinstellungen wirksam werden.

 

Der folgende Code zeigt die MOF-Datei (Managed Object Format), die die **Setting** -Klasse definiert.

``` syntax
[dynamic: ToInstance, provider("TroubleShooting, Version=2.0.392.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"), singleton: DisableOverride ToInstance ToSubClass]
class Setting : ConfigValueProvider
{
                boolean UxSmartCardLogonEnabled = TRUE;
                [read] string User;
                [implemented] void Clear([in] string propertyName);
};
```

Die **Setting** -Klasse erbt von der **ConfigValueProvider** -Klasse. Der folgende Code zeigt die MOF-Datei (Managed Object Format), die die **ConfigValueProvider** -Klasse definiert.

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

## Verwandte Themen


[Verwalten von Konfigurationseinstellungen für MED-V-Arbeitsbereiche](managing-med-v-workspace-configuration-settings.md)

[Verwalten von MED-V-Arbeitsbereichseinstellungen](manage-med-v-workspace-settings.md)

 

 





