---
title: So installieren Sie den Client über die Befehlszeile
description: So installieren Sie den Client über die Befehlszeile
author: dansimp
ms.assetid: ed372403-64ff-48ff-a3cd-a46cad04a4d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca594e1399b4ca4f680f68efffcd011fdc5f042
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807060"
---
# So installieren Sie den Client über die Befehlszeile


Die Themen in diesem Abschnitt enthalten Verfahren zum Installieren des Application Virtualization (app-v)-Desktop Clients oder des App-v-Clients für Remote Desktop Dienste (ehemals Terminal Dienste) mithilfe von setup.exe oder setup.msi. Zum Ausführen eines der Setupprogramme sind Administratorrechte erforderlich.

Sie können optionale Befehlszeilenparameter verwenden, um während der Installation bestimmte Konfigurationseinstellungen auf den App-V-Client anzuwenden. Weitere Informationen zum Verwenden von Parametern finden Sie unter [Befehlszeilenparameter für Application Virtualization Client Installer](application-virtualization-client-installer-command-line-parameters.md). Wenn Sie die Registrierungseinstellungen auf einen Computer angewendet haben, bevor Sie einen Client bereitstellen, beispielsweise mithilfe von Gruppenrichtlinien, werden diese Einstellungen beibehalten, und es werden alle zusätzlichen Befehlszeilenparameter angewendet. Mit Befehlszeilenparametern werden alle vorhandenen Werte für die gleiche Einstellung ersetzt.

**Hinweis**  Wenn Sie den App-V-Client zur Verwendung mit einem schreibgeschützten Cache installieren, beispielsweise bei einer VDI-Server Implementierung, müssen Sie den *AUTOLOADTARGET* -Parameter auf None setzen, um zu verhindern, dass der Client versucht, Anwendungen zu aktualisieren, wenn der Cache schreibgeschützt ist.

 

Weitere Informationen zum Festlegen dieser Parameterwerte nach der Installation finden Sie unter [Konfigurieren der Einstellungen der App-V-Client Registrierung über die Befehlszeile](https://go.microsoft.com/fwlink/?LinkId=169355) ( https://go.microsoft.com/fwlink/?LinkId=169355) im Operations Handbuch für Application Virtualization (App-V).

**Hinweis**  Wenn eine Konfigurationseinstellung auf dem Computer des Benutzers vom Client Installationspfad abhängt, beachten Sie, dass der Application Virtualization (App-V) 4.5-Client seine Installationsdateien in einen anderen Ordner als in früheren Versionen kopiert. Standardmäßig werden durch eine neue Installation des App-v 4.5-Clients die Installationsdateien in den \\Program c:\\Programme\\Microsoft Application Virtualization Client-Ordner kopiert. Wenn eine frühere Version des Clients bereits installiert ist, führt das Ausführen des App-V 4,5-Clientinstallationsprogramms zu einem Upgrade des vorhandenen Clients mithilfe des vorhandenen Installationsordners.

 

\ [Vorlage-Tokenwert \]

**Hinweis**  Bei App-v, Version 4.6 und höher, wenn der APP-v-Client installiert ist, wird SFTLDR.DLL in das Windows\\system32-Verzeichnis kopiert. Wenn der App-V-Client auf einem 64-Bit-System installiert ist, wird SFTLDR\_WOW64.DLL in das Windows\\SysWOW64-Verzeichnis kopiert.

 

\ [Vorlage-Tokenwert \]

## Inhalt dieses Abschnitts


In den folgenden Themen wird beschrieben, wie Sie entweder den Application Virtualization (app-v)-Desktop Client oder den App-v-Client für Remote Desktop Dienste (ehemals Terminal Dienste) mithilfe von setup.exe oder setup.msi installieren.

<a href="" id="how-to-install-the-app-v-client-by-using-setup-exe"></a>[So installieren Sie den App-V-Client mithilfe von Setup.exe](how-to-install-the-app-v-client-by-using-setupexe-new.md)  
Bietet eine schrittweise Anleitung zum Installieren des App-V-Clients mithilfe des setup.exe-Programms.

<a href="" id="how-to-install-the-app-v-client-by-using-setup-msi"></a>[So installieren Sie App-V-Client mit Setup.msi](how-to-install-the-app-v-client-by-using-setupmsi-new.md)  
Bietet Schritt-für-Schritt-Verfahren zum Installieren aller erforderlichen Software und auch des App-V-Clients mithilfe des setup.msi-Programms.

## Verwandte Themen


[Befehlszeilenparameter von Application Virtualization Client Installer](application-virtualization-client-installer-command-line-parameters.md)

[So installieren Sie Application Virtualization Client manuell](how-to-manually-install-the-application-virtualization-client.md)

[So veröffentlichen Sie eine virtuelle Anwendung auf dem Client](how-to-publish-a-virtual-application-on-the-client.md)

[So deinstallieren Sie App-V Client](how-to-uninstall-the-app-v-client.md)

 

 





