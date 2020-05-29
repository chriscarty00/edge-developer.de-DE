---
description: Erfahren Sie, was eine Chrom-Erweiterung ist, und erstellen Sie eine vollständige Bildanzeige Erweiterung, die Optionen, Inhalts Injektion, hintergrundskripts, Speicher und vieles mehr umfasst.
title: Erste Schritte mit Microsoft Edge (Chrom)-Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/05/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, Erweiterungen
ms.openlocfilehash: a271514f39ed8bbe379116c33e23c973d3eb6adb
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567509"
---
# Erste Schritte mit Microsoft Edge \ (Chrom \)-Erweiterungen  

Wenn Sie direkt zum Erstellen Ihrer ersten Erweiterung springen möchten, wechseln Sie zu Teil 1, um ein NASA-Bild der Tages Erweiterung zu erstellen.  

Wenn Sie mit den Erweiterungs Konzepten und der Architektur nicht vertraut sind, lesen Sie weiter, und erfahren Sie, was Erweiterungen sind.  Mithilfe dieser Informationen können Sie Erweiterungen viel einfacher erstellen, da Sie die Beweggründe und die Architektur dahinter verstehen.  

## Erstellen eines NASA-Bilds der Tages Erweiterung  

In jedem Abschnitt befindet sich das abgeschlossene Erweiterungs Quellen-Installationspaket, auf das verwiesen wird.  

*   [Erstellen einer einfachen Erweiterung, die das NASA-Bild des Tages öffnet](part1-simple-extension.md)  
    *   Erstellen eines Manifests  
    *   Zuweisen von Erweiterungssymbolen  
    *   Anzeigen eines Popupfensters  
    *   Führen Sie Ihre Erweiterung lokal in Ihrem Browser aus \ (Side-Loading \)  

*   [Dynamisches Einfügen eines NASA-Bilds unterhalb des Body-Tags der Seite](part2-content-scripts.md)  
    *   Erstellen von JavaScript zum Einfügen eines dynamischen Inhalts Skripts  
    *   Im Manifest definieren, welche Seiteninhalts Skript erhalten  
    *   Deklaratives Einfügen eines Inhalts Skripts  
    *   Hinzufügen einer Schaltfläche in Popup, um eine Nachricht an ein Inhalts Skript zu senden  
    *   Empfangen einer Nachricht in einem Inhalts Skript  

## Grundlegendes zum Browser, bevor Erweiterungen eingeführt werden  

### Jede Registerkarte des Browsers ist von jeder anderen Registerkarte isoliert  

Um zu verstehen, was eine Microsoft Edge \ (Chromium \)-Erweiterung ist, müssen wir zunächst vollständig verstehen, was ein Multi Tab-Browser, wie Microsoft Edge, in erster Linie tut.  Um zu beginnen, wird jede Browserregister Karte in einem einzelnen Thread ausgeführt, der Sie effektiv von anderen Browser Registern \ (oder Threads \) isoliert.  

![Ein Thread pro Browser-Registerkarte](media/index-image1-browsertabs.png)  

### Jede Registerkarte verarbeitet eine GET-Anforderung.  

Auf jeder Registerkarte wird im Wesentlichen die URL \ (auch als Uniform Resource Locator bezeichnet) verwendet, um einen einzelnen Datenstrom zu erhalten, der in der Regel ein HTML-Dokument ist.  Dieser einzelne Datenstrom \ (oder die Seite \) enthält häufig Anweisungen (wie beispielsweise JavaScript-Tags, Bild Bezüge, CSS-Bezüge usw.).  Letztendlich werden alle benötigten Ressourcen auf eine Registerkartenseite heruntergeladen, und in der Regel wird eine Visualisierung angezeigt, die auf der Registerkarte Browser vollständig gerendert wird.  

### Die gesamte Kommunikation von jeder Registerkarte erfolgt an Remoteserver.  

Wenn Sie wissen, dass jede Registerkarte in einer isolierten Umgebung ausgeführt wird, bedeutet dies, dass diese Registerkarten voneinander isoliert sind, nicht aber das größere Internet.  In der Regel werden diese Registerkarten, auf denen JavaScript als Programmiersprache ausgeführt wird, an den Server zurückgegeben, der als Ursprungsserver für die erste Get-Anforderung gedacht ist, die in die URL-Leiste oben auf der Registerkarte Browser eingegeben wurde.  

## Das Erweiterungsmodell dreht alles auf den Kopf  

Eine Erweiterung, genau wie Registerkarten, wird in einem einzelnen Thread ausgeführt, der vollständig von allen besprochenen Registerkarten Threads isoliert ist.  Im Gegensatz zu den Registerkarten, deren Aufgabe darin besteht, in der Regel eine einzelne Get-Anforderung an einen Remoteserver auszugeben, wird eine Visualisierung dieser Daten im Browser angezeigt, wobei es sich um den Server handelt, der sich zuvor auf dem anderen Ende der Internetverbindung befand, die auf einer Browserregister Karte ausgeführt wurde.  

![Erweiterungsmodell wandelt das Servermodell auf den Kopf](media/index-image3-upsidedown.png)  

Das ist wirklich wichtig, um es zu verstehen.  Nachdem Sie eine Erweiterung erstellt und in Ihrem Browser installiert haben, haben Sie einen eigenständigen Webserver erstellt, der in Ihrem Browser lebt und atmet, aber immer noch von jeder Registerkarte isoliert ist, die in diesem Browser ausgeführt wird.  

### Das Extension Web Server-Bundle  

Was ist eine Erweiterung? Hierbei handelt es sich um ein Bündel \ (oder als ZIP-Datei bezeichnet) von Webressourcen, die sich nicht von dem unterscheiden, was ein Web Developer auf einem Webserver veröffentlicht.  

Diese ZIP-Datei enthält HTML, CSS, JavaScript, Bilder und alle erforderlichen Ressourcen, um eine Webseite zu erstellen.  Es gibt jedoch eine zusätzliche Datei, die im Stammverzeichnis dieser zip-Datei erforderlich ist, und diese Datei hat den Namen `manifest.json` .  Es handelt sich um die Blaupause für Ihre Erweiterung, die Dinge wie die Version ihrer Erweiterung, was ist der Titel, welche Privilegien benötigt Sie für die Ausführung und vieles mehr umfasst.  

![Anzeigen von Dateien in ZIP](media/index-image5-filemanager-view.png)  

### Starten des Erweiterungs Servers  

Wenn Sie die Bereitstellung auf einem Webserver vornehmen, enthält dieser Webserver, ob Apache, IIS, NGINX oder andere, Ihr Webpaket.  Wenn ein Browser zu einer URL auf einem Server navigiert, `index.html` wird die Datei auf dem Webserver heruntergeladen.  Der Browser navigiert mithilfe von Zertifikaten, Konfigurationsdateien und mehr.  Die `index.html` Datei, die an einem bestimmten Speicherort auf dem Webserver gespeichert ist.   Wie funktioniert Ihre Erweiterung?  Wie können die Registerkarten Ihres Browsers insbesondere auf diese ZIP-Datei \ (Ihre Erweiterung \) zugreifen?  So funktioniert die Erweiterungs Laufzeit für Sie.  

Die Erweiterung dient für alle Dateien aus der URL \ (Uniform Resource Locator \) unter dem Namen `extension://{some-long-unique-identifier}/index.html` .  Der Name, den ich in eckige Klammern gesetzt habe, `{some-long-unique-identifier}` ist eine eindeutige Kennung, die der von Ihnen installierten Erweiterung zugewiesen ist.  Das bedeutet: Wenn in Ihrem Browser 10 eindeutige Erweiterungen installiert sind, weist jede Erweiterung einen eindeutigen Bezeichner auf, der auf die ZIP-Datei \ (oder das Erweiterungspaket \) verweist, die innerhalb Ihres Browsers installiert ist.  

<!--![Unique URLS for Extensions](media/index-image4-uniqueurls.png)  -->  

<!--todo: add image for unique URLs  -->  

### Erweiterungen verwalten und kommunizieren mit Registerkarten und der Browsersymbolleiste  

Erweiterungen interagieren mit der Browsersymbolleiste, jeder kann alle anderen ausgeführten Registerkarten auf sichere Weise verwalten sowie das DOM aller Registerkartenseiten manipulieren.  Integriert in den Chromium-Browser ist eine Nachrichten-API, die die Kommunikation zwischen den Erweiterungen und den Registerkarten ermöglicht, damit dies problemlos erfolgen kann.  Diese API, auch als Erweiterungen-API bekannt, bietet zahlreiche Funktionen wie Benachrichtigungsverwaltung, Speicherverwaltung und vieles mehr.  

Wie bei Webservern können Erweiterungen kontinuierlich \ (oder Sleep Waiting for Notifications \) ausgeführt werden, wenn der Browser ausgeführt wird.  Sie können sich eine Erweiterung als Orchestrator für den Browser vorstellen.  Auch hier wird die Erweiterung vollständig von den Registerkartenseiten isoliert, aber durch die Erweiterungen-API und die der Erweiterung gewährten Opt-in-Berechtigungen kann jede Erweiterung alle Registerkarten, die im Browser ausgeführt werden, virtuell steuern.  

### Erweiterungen bieten ein Opt-in-Sicherheitsmodell für die Installationszeit.  

Jede Erweiterung kann durch eine Deklaration in der `manifest.json` Datei der Person, die die Erweiterung installiert, unterschiedliche Autoritätsebenen zuweisen.  Diese Berechtigung ermöglicht Erweiterungen, wenn Sie von einem Benutzer installiert werden, um sich anzumelden, damit die Erweiterung alle Informationen extrahieren und diese Daten über die Erweiterung verarbeiten kann.  

<!-- image links -->  

<!-- links -->  
