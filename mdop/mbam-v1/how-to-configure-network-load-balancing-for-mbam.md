---
title: So konfigurieren Sie den Netzwerklastenausgleich für MBAM
description: So konfigurieren Sie den Netzwerklastenausgleich für MBAM
author: dansimp
ms.assetid: df2208c3-352b-4a48-9722-237b0c8cd6a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a04bc74a9dab7bfe18eed8e5a3c1b6ca64d88b5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811200"
---
# So konfigurieren Sie den Netzwerklastenausgleich für MBAM


Wenn Sie sicherstellen möchten, dass Sie die Voraussetzungen und Hardware-und Softwareanforderungen für die Installation des Features Verwaltung und Monitoring Server erfüllt haben, lesen Sie [MBAM 1,0-Bereitstellungsvoraussetzungen](mbam-10-deployment-prerequisites.md) und [MBAM 1,0-unterstützte Konfigurationen](mbam-10-supported-configurations.md).

**Hinweis**  Um die Setupprotokolldateien zu erhalten, müssen Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mithilfe des **msiexec** -Pakets und der Option " **/l** &lt; Location &gt; " installieren. Die Protokolldateien werden an dem von Ihnen angegebenen Speicherort erstellt.

Zusätzliche Setupprotokolldateien werden im Ordner "% Temp%" des Benutzers erstellt, der MBAM installiert.

 

Die Netzwerklastenausgleich-Cluster (NLB) für das Verwaltungs-und Überwachungs Server Feature bieten Skalierbarkeit in MBAM und sollten mehr als 55.000 MBAM-Clientcomputer unterstützen.

**Hinweis**  Der Windows Server-Netzwerklastenausgleich verteilt Clientanforderungen auf eine Reihe von Servern, die in einem einzelnen Servercluster konfiguriert sind. Wenn der Netzwerklastenausgleich auf den einzelnen Servern (Hosts) eines Clusters installiert ist, stellt der Cluster eine virtuelle IP-Adresse oder einen vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) für Clientanforderungen dar. Die anfänglichen Clientanforderungen gehen an alle Hosts im Cluster, aber nur ein Host akzeptiert und verarbeitet die Anforderung.

Alle Computer, die zu einem NLB-Cluster gehören, weisen die folgenden Voraussetzungen auf:

-   Alle Computer im NLB-Cluster müssen sich in derselben Domäne befinden.

-   Jeder Computer im NLB-Cluster muss eine statische IP-Adresse verwenden.

-   Auf jedem Computer im NLB-Cluster muss der Netzwerklastenausgleich aktiviert sein.

-   Der NLB-Cluster erfordert eine statische IP-Adresse, und ein Hosteintrag muss manuell im DNS (Domain Name System) erstellt werden.

 

## Konfigurieren des Netzwerklastenausgleichs für MBAM-Verwaltungs-und-Überwachungsserver


In den folgenden Schritten wird beschrieben, wie Sie einen virtuellen NLB-Clusternamen und eine IP-Adresse für zwei MBAM-Verwaltungs-und-Überwachungsserver konfigurieren und wie Sie MBAM-Clients für die Verwendung des NLB-Clusters konfigurieren.

Bevor Sie mit den in diesem Thema beschriebenen Verfahren beginnen, müssen Sie das MBAM-Verwaltungs-und Überwachungs Server Feature erfolgreich installieren, indem Sie dieselbe IIS-Portbindung auf zwei separaten Server Computern verwenden, die die Voraussetzungen für die Installation von MBAM-Server Features und die NLB-Cluster Konfiguration erfüllen.

**Hinweis**  In diesem Thema wird der grundlegende Prozess der Verwendung des Netzwerklastenausgleich-Managers zum Erstellen eines NLB-Clusters beschrieben. Die genauen Schritte zum Konfigurieren eines Windows-Servers als Teil eines NLB-Clusters hängen von der verwendeten Windows Server-Version ab. Weitere Informationen zum Erstellen von NLBS auf WindowsServer2008 finden Sie unter [Erstellen von Netzwerklastenausgleich-Clustern](https://go.microsoft.com/fwlink/?LinkId=197176) in der Windows Server2008 TechNet-Bibliothek.

 

**So konfigurieren Sie einen virtuellen NLB-Cluster Namen und eine IP-Adresse für zwei MBAM-Verwaltungs-und-Überwachungsserver**

1.  Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **Netzwerklastenausgleich-Manager**.

    **Hinweis**  Wenn der NLB-Manager nicht vorhanden ist, können Sie ihn als Windows Server-Feature installieren. Sie müssen dieses Feature auf beiden MBAM-Verwaltungs-und-Überwachungs Servern installieren, wenn Sie es in den NLB-Cluster konfigurieren möchten.

     

2.  Klicken Sie auf der Menüleiste auf **Cluster**, und klicken Sie dann auf **neu** , um das Dialogfeld **Clusterparameter** zu öffnen.

3.  Geben Sie im Dialogfeld **Clusterparameter** die Informationen für die IP-Konfiguration des NLB-Clusters ein:

    -   **IP-Adresse:** In DNS registrierte IP-Adresse des NLB-Clusters

    -   **Subnetzmaske:** NLB-Cluster-IP-Adressen-Subnetzmaske in DNS registriert

    -   **Vollständiger Internet Name:** FQDN des in DNS registrierten NLB-Clusternamens

4.  Stellen Sie sicher, dass **Unicast** im **Cluster Betriebsmodus**ausgewählt ist, und klicken Sie dann auf **weiter**.

5.  Klicken Sie auf der Seite **Cluster-IP-Adressen** auf **weiter**.

6.  Klicken Sie auf der Seite **Port Regeln** auf **Bearbeiten** , um die Ports zu definieren, auf die der NLB-Cluster antwortet, und konfigurieren Sie die Ports, die für die Client-zu-Standort-Systemkommunikation verwendet werden, wie Sie für die Website definiert sind, oder klicken Sie auf **weiter** , um die IP-Adresse des NLB-Clusters zu aktivieren, um auf alle TCP/IP-Ports

    **Hinweis**  Stellen Sie sicher, dass **Affinität** auf **Single**festgesetzt ist.

     

7.  Geben Sie auf der Seite **verbinden** einen Hostnamen für die MBAM-Verwaltungs-und-Überwachungsserverinstanz ein, der Teil des NLB-Clusters in **Host**sein soll, und klicken Sie dann auf **verbinden**.

8.  Wählen Sie unter **für die Konfiguration eines neuen Clusters verfügbare Schnittstellen**die Netzwerkschnittstelle aus, die für die Reaktion auf die NLB-Clusterkommunikation konfiguriert wird, und klicken Sie dann auf **weiter**.

9.  Überprüfen Sie auf der Seite **Host Parameter** die angezeigten Informationen, um sicherzustellen, dass die dedizierten **IP-Konfigurations** Einstellungen die dedizierte Host-IP-Konfiguration für den richtigen NLB-Clusterhost anzeigen, überprüfen Sie, ob der ursprüngliche **Standardzustand** des Hoststatus: **gestartet**ist, und klicken Sie dann auf **Fertig stellen**.

    **Hinweis**  Auf der Seite " **Hostparameter** " wird auch die NLB-Cluster Host Priorität (1 bis 32) angezeigt. Wenn dem NLB-Cluster neue Hosts hinzugefügt werden, muss sich die Hostpriorität von den zuvor hinzugefügten Hosts unterscheiden. Die Priorität wird bei Verwendung des Netzwerklastenausgleich-Managers automatisch erhöht.

     

10. Klicken Sie auf ** &lt; NLB &gt; -Clustername** , und stellen Sie sicher, dass der NLB-Hostschnittstellen **Status** **konvergiert** angezeigt wird, bevor Sie fortfahren. Für diesen Schritt müssen Sie möglicherweise die Anzeige des NLB-Clusters als Host-TCP/IP-Konfiguration aktualisieren, die vom NLB-Manager geändert wird.

11. Wenn Sie dem NLB-Cluster weitere Hosts hinzufügen möchten, klicken Sie mit der rechten Maustaste auf ** &lt; NLB-Cluster &gt; Name**, klicken Sie auf **Host zu Cluster hinzufügen,** und wiederholen Sie dann die Schritte 7 bis 10 für jedes Website System, das Teil des NLB-Clusters sein wird.

12. Ändern Sie auf einem Computer, auf dem die MBAM-Gruppenrichtlinienvorlage installiert ist, die MBAM-Gruppenrichtlinieneinstellungen, um die MBAM-Dienstendpunkte so zu konfigurieren, dass der NLB-Clustername und die entsprechende IIS-Portbindung für den Zugriff auf die auf den NLB-Clustercomputern installierten MBAM-Verwaltungs-und Überwachungs Server Features verwendet werden. Weitere Informationen zum Bearbeiten von MBAM-GPO-Einstellungen finden Sie unter [Bearbeiten von MBAM 1,0-GPO-Einstellungen](how-to-edit-mbam-10-gpo-settings.md). Wenn die MBAM-Verwaltungs-und-Überwachungsserver für Ihre Umgebung neu sind, stellen Sie sicher, dass die erforderlichen Mitgliedschaften der lokalen Sicherheitsgruppe ordnungsgemäß konfiguriert wurden. Weitere Informationen zu Sicherheitsgruppen Anforderungen finden Sie unter [Planen von MBAM 1,0-Administrator Rollen](planning-for-mbam-10-administrator-roles.md).

13. Wenn die NLB-Cluster Konfiguration abgeschlossen ist, empfehlen wir, dass Sie überprüfen, ob der NLB-Cluster MBAM-Verwaltung und-Überwachung funktionsfähig ist. Öffnen Sie dazu einen Webbrowser auf einem anderen Computer als den Servern, die im NLB konfiguriert sind, und stellen Sie sicher, dass Sie mithilfe des NLB-FQDN auf die Website MBAM-Verwaltung und-Überwachung zugreifen können.

## Verwandte Themen


[Bereitstellen der Serverinfrastruktur von MBAM 1.0](deploying-the-mbam-10-server-infrastructure.md)

 

 





