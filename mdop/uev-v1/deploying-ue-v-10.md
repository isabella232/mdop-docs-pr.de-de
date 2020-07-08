---
title: Bereitstellen von UE-V 1.0
description: Bereitstellen von UE-V 1.0
author: dansimp
ms.assetid: 519598bb-8c81-4af7-bee7-357696bff880
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a1c515f9be950d8ca7b0a199344d34f7852073d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812181"
---
# Bereitstellen von UE-V 1.0


Es gibt eine Reihe unterschiedlicher Bereitstellungskonfigurationen, die von Microsoft User Experience Virtualization (UE-V) unterstützt werden. Dieser Abschnitt enthält allgemeine Informationen und schrittweise Anleitungen, die Ihnen bei der erfolgreichen Durchführung der Aufgaben helfen, die Sie in verschiedenen Phasen Ihrer Bereitstellung ausführen müssen.

## Bereitstellungsinformationen für UE-V


Eine UE-v-Bereitstellung erfordert einen Speicherort für Einstellungen auf einer Netzwerkfreigabe und einen UE-v-Agent, der auf jedem Computer installiert ist, auf dem die Einstellungen synchronisiert werden. Die UE-v-Gruppenrichtlinienvorlagen können verwendet werden, um UE-v-Einstellungen zu verwalten. In den folgenden Themen wird beschrieben, wie diese Features bereitgestellt werden.

[Bereitstellen des Speicherorts für die Einstellungen für UE-V 1.0](deploying-the-settings-storage-location-for-ue-v-10.md)

Alle UE-V-Bereitstellungen erfordern einen Speicherort für Einstellungen, in dem sich die Einstellungs Pakete befinden, die die synchronisierten Einstellungswerte enthalten.

[Bereitstellen von UE-V-Agent](deploying-the-ue-v-agent.md)

Damit die Einstellungen mithilfe von UE-v synchronisiert werden können, muss der UE-v-Agent auf einem Computer installiert sein und ausgeführt werden.

[Installieren der ADMX-Vorlagen für UE-V-Gruppenrichtlinien](installing-the-ue-v-group-policy-admx-templates.md)

Sie können Gruppenrichtlinien verwenden, um die UE-v-Einstellungen vorab zu konfigurieren, bevor Sie den UE-v-Agent sowie die standardmäßige UE-v-Konfiguration bereitstellen.

## Bereitstellungsinformationen für die benutzerdefinierte Vorlagenbereitstellung


Wenn Sie beabsichtigen, benutzerdefinierte Speicherort Vorlagen für Anwendungen zu erstellen, die nicht die Microsoft-Anwendungen sind, die in UE-v enthalten sind, beispielsweise Branchenanwendungen, können Sie einen Vorlagenkatalog für die Einstellungen bereitstellen und den UE-v-Generator installieren, um diese Vorlagen zu erstellen. Weitere Informationen finden Sie unter [Planen der Bereitstellung von benutzerdefinierten Vorlagen für UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

[Installieren von UE-V-Generator](installing-the-ue-v-generator.md)

Verwenden Sie den UE-V-Generator zum Erstellen, bearbeiten und Überprüfen von Speicherort Vorlagen für benutzerdefinierte Einstellungen, mit denen die Einstellungen anderer Anwendungen als der Standardanwendungen synchronisiert werden.

[Bereitstellen des Katalogs für Einstellungsvorlagen für UE-V 1.0](deploying-the-settings-template-catalog-for-ue-v-10.md)

Wenn Sie benutzerdefinierte Einstellungen für Standort Vorlagen bereitstellen müssen, um andere Anwendungen als die Standardanwendungen des UE-V-Agents zu unterstützen, müssen Sie einen Einstellungs Vorlagenkatalog konfigurieren, um Sie zu speichern.

[Bereitstellen von UE-V-Speicherortvorlagen für UE-V 1.0](deploying-ue-v-settings-location-templates-for-ue-v-10.md)

Wenn Sie andere Anwendungen als die Standardanwendungen des UE-v-Agents synchronisieren müssen, können die mit dem UE-v-Generator erstellten benutzerdefinierten Einstellungen für den Speicherort an den Vorlagenkatalog für UE-v-Einstellungen verteilt werden.

**Hinweis**  Das Bereitstellen von benutzerdefinierten Vorlagen erfordert einen Vorlagenkatalog für Einstellungen. Die Standardvorlagen für Microsoft-Anwendungen werden mit dem UE-V-Agent bereitgestellt.

 

## Themen für dieses Produkt


[Microsoft-User Experience Virtualization (UE-V) 1.0](index.md)

[Erste Schritte mit User Experience Virtualization 1.0](getting-started-with-user-experience-virtualization-10.md)

[Planen für UE-V 1.0](planning-for-ue-v-10.md)

[Vorgänge für UE-V 1.0](operations-for-ue-v-10.md)

[Problembehandlung für UE-V 1.0](troubleshooting-ue-v-10.md)

 

 





