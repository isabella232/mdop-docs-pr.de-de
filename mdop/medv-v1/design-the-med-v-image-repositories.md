---
title: Entwerfen Sie die MED-V-Image-Repositorys
description: Entwerfen Sie die MED-V-Image-Repositorys
author: dansimp
ms.assetid: e153154d-2751-4990-b94d-a2d76242c15f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0c59a0dd2d1b3a78bd211c6a6353a86c77d8fc2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810060"
---
# Entwerfen Sie die MED-V-Image-Repositorys


Nachdem MED-V-Bilder erstellt und gepackt wurden, können Sie an einem beliebigen Speicherort auf einem Dateiserver gespeichert werden. Die Dateien werden möglicherweise über HTTP oder HTTPS von einem oder mehreren IIS-Servern gesendet. Das Bild-Repository kann von mehreren MED-V-Instanzen freigegeben werden.

Um die Bild Depots zu entwerfen, müssen Sie zunächst entscheiden, wie die Bilder für jeden Client bereitgestellt werden sollen, und dann, ob dieser Client ein lokales Image-Repository benötigt. Alle Repositories werden dann zusammen mit dem zugehörigen IIS-Server entworfen und abgelegt.

## Bestimmen, wie Bilder bereitgestellt werden


Entscheiden Sie für jeden Med-v-Arbeitsbereich, wie Sie Med-v-Bilder für den Client bereitstellen möchten. Dies ist wichtig, wenn Sie ermitteln möchten, wie viele Repositories benötigt werden, um die gepackten Bilder zu speichern, wo diese Repositories abgelegt werden, und dann diese Repositories zu entwerfen.

Verpackte Bilder können wie folgt bereitgestellt werden:

-   Über das Netzwerk von einem Bildverteilungsserver heruntergeladen, der einen Dateiserver und einen IIS-Server umfasst.

-   Auf Wechselmedien wie einem USB-Laufwerk oder einer DVD.

-   Mit einem Unternehmenssoftware-Distributionscenter in einem Bildspeicher Verzeichnis auf dem Clientcomputer vorab bereitgestellt.

Entscheiden Sie, welche Methode oder Methoden für die Bereitstellung von MED-V-Bildern für die einzelnen Clients verwendet werden sollen und ob für den Speicherort ein Bild-Repository erforderlich ist.

## Ermitteln der Anzahl von Bild Repositories


Nachdem Sie nun die Mindestanzahl der benötigten Repositories ermittelt haben, fügen Sie weitere hinzu, wenn eines der folgenden Kriterien zutrifft:

-   Organisatorische oder regulatorische Gründe, die Med-v-Bilder voneinander zu trennen – einige Med-v-Bilder können möglicherweise nicht im gleichen Repository koexistieren. Vertrauliche persönliche Daten können beispielsweise Speicher auf einem Server erfordern, der nur für eine begrenzte Anzahl von Mitarbeitern verfügbar ist, die auf die Daten zugreifen müssen.

-   Clients in isolierten Netzwerken – wenn Bilder über das Netzwerk bereitgestellt werden, ermitteln Sie, ob Netzwerke isoliert sind und ein separates Repository erforderlich ist. Beispielsweise isolieren Organisationen häufig Lab-Netzwerke aus Produktionsnetzwerken.

-   Clients in Remotenetzwerken: Wenn Bilder über das Netzwerk bereitgestellt werden, werden einige Clientcomputer möglicherweise durch Netzwerk Links vom Repository getrennt, die nicht genügend Bandbreite aufweisen, um eine angemessene Benutzerfreundlichkeit zu gewährleisten, wenn ein Client einen MED-V-Arbeitsbereich lädt. Falls erforderlich, entwerfen Sie zusätzliche MED-V-Instanzen, um diesen Bedarf zu beheben.

Fügen Sie diese Repositories zum Entwurf hinzu. Entscheiden Sie sich für einen Namen für jedes Repository und den Grund für dessen Entwurf. Entscheiden Sie, welche Med-v-Bilder in den Repositories gespeichert werden und welche Med-v-Clients Med-v-Arbeitsbereiche mit Bildern aus dem Repository laden werden.

## Entwerfen und Platzieren der Bild Depots


Wenn ein neues Bild für Clients verfügbar ist, beginnt der Download des Bilds möglicherweise gleichzeitig. Dies führt zu einer großen Nachfrage im Repository und muss beim Entwerfen des Image-Repositorys berücksichtigt werden.

Ermitteln Sie für jedes Repository die Menge der Daten, die gespeichert werden sollen. Summieren Sie die Größe von Bildern, die im Repository gespeichert werden. Dies ist der Wert des auf dem Dateiserver erforderlichen Speicherplatzes.

Als nächstes addieren Sie die Anzahl der Clients, die MED-V-Bilder aus dem Repository herunterladen können. Hierbei handelt es sich um die maximale Anzahl gleichzeitiger Downloads, die auftreten können, wenn ein neues MED-V-Abbild in das Repository geladen wird. Der Dateiserver muss mit einem Datenträgersubsystem entworfen werden, das die IO-Anforderungen erfüllen kann, die dadurch entstehen.

Das Image-Repository kann sich auf dem gleichen System wie der MED-V-Server und dem Server befinden, auf dem SQL Server ausgeführt wird, oder auf einer Remotedateifreigabe. Sie können es auch in einer Windows Server2008 Hyper-V-VM ausführen. Überprüfen Sie den Netzwerkstandort der Clients, die vom Image-Repository bereitgestellt werden, und platzieren Sie das Repository an einem Netzwerkspeicherort, an dem es über genügend Bandbreite verfügt, um die Erwartungen der Kunden an den Service Level zu erfüllen.

### Fehlertoleranz

Wenn das Bild-Repository nicht verfügbar ist, können Clients keine neuen oder aktualisierten MED-V-Bilder herunterladen. Informationen zum Entwerfen von Fehlertoleranzoptionen für den Dateiserver und fehlertolerante Datenträger finden Sie im Leitfaden zur [Infrastrukturplanung und-Entwurf von Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) .

## Entwerfen und Platzieren der IIS-Server


Dieser Abschnitt ist nur relevant, wenn Clients Bilddateien über das Netzwerk über HTTP oder https herunterladen.

Der IIS-Server kann auf demselben System wie dem MED-V-Server und dem Server koexistieren, auf dem SQL Server ausgeführt wird. Sie kann auch in einer Windows Server2008 Hyper-V-VM ausgeführt werden. Die IIS-Serverinfrastruktur muss über einen ausreichenden Durchsatz verfügen, um Bilder an Clients innerhalb der Service Level-Erwartungen der Organisation zu übermitteln. Sie muss mit einem Datenträgersubsystem entworfen werden, das die IO-Anforderungen erfüllen kann, die dadurch entstehen.

Addieren Sie für jedes Bild-Repository die Anzahl der Clients, die MED-V-Bilder mit IIS herunterladen können. Hierbei handelt es sich um die maximale Anzahl gleichzeitiger Downloads, die beim Laden eines Bilds in das Repository auftreten können. Verwenden Sie die in [Definieren des Projektumfangs](define-the-project-scope.md) festgelegte Durchsatz Summe und die erwarteten Service Level, um den Entwurf der IIS-Serverinfrastruktur zu planen und die für das Repository zuzuweisende geeignete Bandbreite festzulegen.

Informationen zum Entwerfen der IIS-Infrastruktur finden Sie im Leitfaden zur [Infrastrukturplanung und-Entwurf für Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) .

### Fehlertoleranz

Wenn die IIS-Serverinfrastruktur nicht verfügbar ist, können Clients keine neuen oder aktualisierten Bilder herunterladen. Um die Fehlertoleranz zu konfigurieren, kann der Windows Server2008-basierte IIS-Server in einem Failovercluster gespeichert werden. Informationen zum Entwerfen der Fehlertoleranz für die IIS-Serverinfrastruktur finden Sie im Leitfaden zur [Infrastrukturplanung und-Entwurf für Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) .

## Verwandte Themen


[Bereitstellen eines MED-V-Arbeitsbereichs über ein Enterprise Software Distribution-System](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md)

[Bereitstellen eines MED-V-Arbeitsbereichs mit einem Bereitstellungspaket](deploying-a-med-v-workspace-using-a-deployment-package.md)

 

 





