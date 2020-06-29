---
title: Erkennen von Netzwerkänderungen, die MED-V beeinflussen
description: Erkennen von Netzwerkänderungen, die MED-V beeinflussen
author: dansimp
ms.assetid: fd29b95a-cda2-464d-b86d-50b6bd64b4ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5f43c30dee9ef8e06a7ae226849a4f21e83257c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809916"
---
# Erkennen von Netzwerkänderungen, die MED-V beeinflussen


Mit der Microsoft Enterprise Desktop Virtualization (Med-v) 2,0-Lösung können Sie Ihre Umgebung so konfigurieren, dass bestimmte Netzwerkänderungen erkannt werden, die möglicherweise nach der Bereitstellung von Med-v-Arbeitsbereichen auftreten und sich auf Med-v auswirken können.

Das Feature umfasst eine im Gastbetriebssystem ausgeführte Komponente, die über Änderungen an der Netzwerkkonfiguration auf dem Hostcomputer benachrichtigt wird. Damit kann eine nicht von Microsoft ausgeführte ESD-oder andere Anwendung, die im Gast ausgeführt wird, zu denselben Netzwerkendpunkten aufgelöst werden, zu denen die Host-ESD oder-Anwendung aufgelöst wird.

**Hinweis**  Dieses Feature ist nur verfügbar, wenn der virtuelle Computer für den NAT-Modus (Network Address Translation) konfiguriert ist. Wenn der virtuelle Computer für den Überbrückungsmodus konfiguriert ist, werden keine Änderungshinweise generiert.

 

Dieser Abschnitt enthält Informationen und Anweisungen zur Unterstützung bei der Überwachung dieser Netzwerkänderungen, die sich auf MED-V auswirken können.

## So erkennen Sie Netzwerkänderungen für MED-V


Nachdem Sie Ihre MED-V-Arbeitsbereiche bereitgestellt haben, können Sie Änderungen an bestimmten Netzwerkkonfigurationen überwachen, indem Sie die folgenden Aufgaben Vorformen:

1. Erstellen Sie eine MOF-Datei (Managed Object Format), die nach den Netzwerkkonfigurationsänderungen sucht, die überwacht werden sollen. Der folgende Code zeigt ein Beispiel für die MOF-Datei, die Sie erstellen können.

   ``` syntax
   #pragma namespace ("\\\\.\\root\\ccm\\NetworkConfig")

   class CCM_IPConfig
   {
       [NotNull: ToInstance ToSubClass] uint32 AddressFamily; // AF_INET, AF_INET6
       [Key, NotNull: ToInstance ToSubClass] string IPAddress; // IPv4 or IPv6 address
       [NotNull: ToInstance ToSubClass] string SubnetMask; // IPv4 subnet mask
   };

   class CCM_NetworkAdapter
   {
       [Key, NotNull: ToInstance ToSubClass] string Name;
       [NotNull: ToInstance ToSubClass] uint32 DHCPEnabled = 0; 
       [NotNull: ToInstance ToSubClass] uint32 Quarantined = 0; // To check if it is quarantined.
       CCM_IPConfig IPConfigInfo[];
   };

   [singleton]
   class CCM_NetworkAdapters
   {
       [NotNull: ToInstance ToSubClass] String ProviderName; // MED-V or other provider
       CCM_NetworkAdapter AdaptersInfo[];
   };
   ```

2. Kompilieren Sie die MOF-Datei.

3. Installieren Sie die MOF-Datei im Gast.

Nachdem Sie die MOF-Datei installiert haben, können Sie ein Ereignisabonnement erstellen, das Windows Management Instrumentation (WMI)-Erstellungs-, Änderungs-oder Löschereignisse für die **ccm \ _NetworkAdapters** Klasse abonniert. Damit werden die folgenden Änderungen am Host erkannt:

Gibt es Konfigurationsänderungen am Netzwerk, beispielsweise Änderungen an der IP-Adresse oder am Netzwerkadapter?

Ist das Netzwerk verfügbar oder nicht verfügbar?

Wurde das Netzwerk Setup vom Brückenmodus in den NAT-Modus geändert?

Wurde das Netzwerk Setup vom NAT-Modus in den Überbrückungsmodus geändert?

Eine MED-V-Komponente auf dem Host überwacht das Netzwerk für diese Änderungen und signalisiert dem Gast dann die Änderung. Eine Komponente im Gast erstellt eine WMI-Instanz, um den MED-V-Arbeitsbereich für diese Änderungen zu überwachen.

Das von Ihnen erstellte Ereignisabonnement bietet eine Benachrichtigung über das WMI-System, wenn mindestens eine dieser Netzwerkänderungen – erstellen, ändern oder löschen – eintritt.

## Verwandte Themen


[Überwachen von MED-V-Arbeitsbereichen](monitor-med-v-workspaces.md)

[Verwalten von MED-V-Arbeitsbereichseinstellungen](manage-med-v-workspace-settings.md)

 

 





