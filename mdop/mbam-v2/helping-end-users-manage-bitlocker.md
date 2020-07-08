---
title: Unterstützung für Endbenutzer beim Verwalten von BitLocker
description: Unterstützung für Endbenutzer beim Verwalten von BitLocker
author: dansimp
ms.assetid: 47776fb3-2d94-4970-b687-c35ec3dd6c64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26ef2bc33a75ff7773b75807ab0e10e5aa67b109
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810759"
---
# Unterstützung für Endbenutzer beim Verwalten von BitLocker


Inhalte auf einem verlorenen oder gestohlenen Computer sind anfällig für unbefugten Zugriff, der sowohl für Personen als auch für Unternehmen ein Sicherheitsrisiko darstellen kann. Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) verwendet BitLocker, um unbefugten Zugriff zu verhindern, indem Sie Ihren Computer sperren, um vertrauliche Daten vor böswilligen Benutzern zu schützen.

## Was ist BitLocker?


Die BitLocker-Laufwerkverschlüsselung bietet Schutz für Betriebssystemlaufwerke, Datenlaufwerke und Wechseldatenträger (wie ein USB-Thumb-Laufwerk), indem die Laufwerke verschlüsselt werden. Je nachdem, wie BitLocker konfiguriert ist, müssen die Benutzer möglicherweise einen Schlüssel (ein Kennwort oder eine PIN) bereitstellen, um die auf den verschlüsselten Laufwerken gespeicherten Informationen freizugeben.

Wenn Sie einem mit BitLocker verschlüsselten Laufwerk neue Dateien hinzufügen, werden Sie von BitLocker automatisch verschlüsselt. Dateien bleiben nur verschlüsselt, während Sie auf dem verschlüsselten Laufwerk gespeichert sind. Dateien, die auf ein anderes Laufwerk oder einen anderen Computer kopiert werden, werden entschlüsselt. Wenn Sie Dateien für andere Benutzer freigeben, beispielsweise über ein Netzwerk, werden diese Dateien verschlüsselt, während Sie auf dem verschlüsselten Laufwerk gespeichert sind, aber Sie können normalerweise von autorisierten Benutzern aufgerufen werden.

Wenn Sie das Betriebssystemlaufwerk verschlüsseln, überprüft BitLocker den Computer während des Starts auf alle Bedingungen, die ein Sicherheitsrisiko darstellen könnten (beispielsweise eine Änderung des BIOS oder Änderungen an Startdateien). Wenn ein potenzielles Sicherheitsrisiko erkannt wird, sperrt BitLocker das Betriebssystemlaufwerk und erfordert einen speziellen BitLocker-Wiederherstellungsschlüssel, um es zu entsperren. Stellen Sie sicher, dass Sie diesen Wiederherstellungsschlüssel erstellen, wenn Sie BitLocker zum ersten Mal aktivieren. Andernfalls können Sie den Zugriff auf Ihre Dateien dauerhaft verlieren.

Wenn Sie Datenlaufwerke (behoben oder abnehmbar) verschlüsseln, können Sie ein verschlüsseltes Laufwerk mit einem Kennwort oder einer Smartcard entsperren oder das Laufwerk so einrichten, dass es automatisch entsperrt wird, wenn Sie sich am Computer anmelden.

Neben Kennwörtern und Pins kann BitLocker den TPM-Chip (Trusted Platform Module) verwenden, der auf vielen neueren Computern bereitgestellt wird. Der TPM-Chip wird verwendet, um sicherzustellen, dass Ihr Computer nicht manipuliert wurde, bevor BitLocker das Betriebssystemlaufwerk aufheben kann. Während des Verschlüsselungsprozesses müssen Sie möglicherweise den TPM-Chip aktivieren. Wenn Sie Ihren Computer starten, fragt BitLocker das TPM nach den Schlüsseln für das Laufwerk und entsperrt es. Um den TPM-Chip zu aktivieren, müssen Sie Ihren Computer neu starten und dann eine Einstellung im BIOS, einer Pre-Windows-Schicht ihrer Computer Software, ändern. Weitere Informationen zum TPM finden Sie unter Informationen zum TPM- [Chip des Computers](about-the-computer-tpm-chip.md).

Sobald Ihr Computer von BitLocker geschützt ist, müssen Sie möglicherweise jedes Mal eine PIN oder ein Kennwort eingeben, wenn der Computer aus dem Ruhezustand oder gestartet wird. Der Helpdesk für Ihr Unternehmen oder Ihre Organisation kann Ihnen helfen, wenn Sie jemals Ihre PIN oder Ihr Kennwort vergessen.

Sie können BitLocker entweder vorübergehend deaktivieren, indem Sie das Laufwerk entschlüsseln oder dauerhaft sperren.

**Hinweis**  Da BitLocker das gesamte Laufwerk und nicht nur die einzelnen Dateien selbst verschlüsselt, seien Sie vorsichtig, wenn Sie sensible Daten zwischen Laufwerken verschieben. Wenn Sie eine Datei von einem mit BitLocker geschützten Laufwerk auf ein nicht verschlüsseltes Laufwerk verschieben, wird die Datei nicht mehr verschlüsselt.

 

## Informationen zur BitLocker-Verschlüsselungsoptionen-Anwendung


Wenn Sie Festplattenlaufwerke auf dem Computer entsperren und Ihre PIN und Kennwörter verwalten möchten, verwenden Sie die BitLocker-Anwendung Verschlüsselungsoptionen in der Windows-Systemsteuerung, indem Sie das hier beschriebene Verfahren ausführen. Sie können Kennwörter zum Entsperren geschützter Laufwerke eingeben und den BitLocker-Status von angefügten Laufwerken mithilfe dieser Anwendung überprüfen.

**So öffnen Sie die BitLocker-Verschlüsselungsoptionen-Anwendung**

1.  Klicken Sie auf **Start**, und wählen Sie **System**Steuerung aus. Die Systemsteuerung wird in einem neuen Fenster geöffnet.

2.  Wählen Sie **in der** **Systemsteuerung System und Sicherheit**aus.

3.  Wählen Sie **BitLocker-Verschlüsselungsoptionen** aus, um die BitLocker-Verschlüsselungsoptionen-Anwendung zu öffnen.

    Eine Beschreibung der verfügbaren Optionen finden Sie im folgenden Abschnitt.

## Optionen für die BitLocker-Verschlüsselungsoptionen-Anwendung


Mit der BitLocker-Anwendung für Verschlüsselungsoptionen in der Systemsteuerung können Sie Ihre PIN und Kennwörter verwalten, die BitLocker zum Schutz Ihres Computers verwendet.

**BitLocker-Laufwerkverschlüsselung – feste Festplatten:**

In diesem Abschnitt können Sie Informationen zu Festplatten, die mit Ihrem Computer verbunden sind, und deren aktuellen BitLocker-Verschlüsselungsstatus anzeigen.

-   **Verwalten der PIN** – ändert die PIN, die von BitLocker zum Entsperren Ihres Betriebssystemlaufwerks verwendet wird.

-   **Verwalten Ihres Kennworts** – ändert das Kennwort, das von BitLocker zum Entsperren ihrer anderen internen Laufwerke verwendet wird.

**BitLocker-Laufwerkverschlüsselung – externe Laufwerke:**

In diesem Abschnitt können Sie Informationen zu externen Laufwerken (wie einem USB-Daumen Laufwerk) anzeigen, die mit Ihrem Computer verbunden sind, und deren aktuellen BitLocker-Verschlüsselungsstatus.

-   **Verwalten Ihres Kennworts** – ändert das Kennwort, das von BitLocker zum Entsperren ihrer anderen internen Laufwerke verwendet wird.

**Erweiterte**

-   **TPM-Administration** – öffnet das TPM-Verwaltungstool in einem separaten Fenster. Hier können Sie allgemeine TPM-Aufgaben konfigurieren und Informationen zum TPM-Chipsatz abrufen. Sie müssen über Administratorrechte auf dem Computer verfügen, um auf dieses Tool zugreifen zu können.

-   **Datenträgerverwaltung** – öffnen Sie das Datenträger Verwaltungstool. Hier können Sie die Informationen für alle an den Computer angeschlossenen Festplatten anzeigen sowie Partitionen und Laufwerksoptionen konfigurieren. Sie müssen über Administratorrechte auf dem Computer verfügen, um auf dieses Tool zugreifen zu können.

 

 





