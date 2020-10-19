---
description: Erstellen einer Erweiterung, die das NASA-Bild des Tages öffnet
title: Erstellen eines Erweiterungs Lernprogramms – Teil 1
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Edge-Chromium, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, Erweiterungen
ms.openlocfilehash: 3809bfac714621cf97184127132487ed93958a2f
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104707"
---
# Erstellen eines Erweiterungs Lernprogramms – Teil 1  

## Übersicht  

Das Ziel dieses Lernprogramms besteht darin, eine Microsoft Edge-Erweiterung (Chrom) zu erstellen, die mit einem leeren Verzeichnis beginnt. Wir erstellen eine Erweiterung, die das NASA-Bild des Tages öffnet. In diesem Lernprogramm erfahren Sie, wie Sie eine Erweiterung erstellen, indem Sie:

*   Erstellen einer `manifest.json` Datei  
*   Symbole werden hinzugefügt.  
*   Öffnen eines standardmäßigen Popup Dialogfelds  

## Bevor Sie beginnen

Wenn Sie die abgeschlossene Erweiterung testen möchten, die Sie in diesem Lernprogramm erstellen, laden Sie den [Quellcode][ArchiveExtensionGettingStartedPart1]herunter.  

## Schritt 1: Erstellen einer `manifest.json` Datei

Für jedes Erweiterungspaket muss eine `manifest.json` Datei am Stamm vorhanden sein.  Das Manifest enthält Details zu ihrer Erweiterung, der Erweiterungspaket Version, dem Namen der Erweiterung und der Beschreibung usw.  

Der folgende Codeausschnitt beschreibt die grundlegenden Informationen, die in der `manifest.json` Datei benötigt werden.  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to display the NASA picture of the day."
}
```  

## Schritt 2: Hinzufügen von Symbolen  

Erstellen Sie zunächst das `icons` Verzeichnis in Ihrem Projekt, in dem die Symbolbild Dateien gespeichert werden sollen.  Die Symbole werden für das Hintergrundbild der Schaltfläche verwendet, die Benutzer zum Starten der Erweiterung auswählen.  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Symbol auf der Symbolleiste, um die Erweiterung zu öffnen":::
   Symbol auf der Symbolleiste, um die Erweiterung zu öffnen
:::image-end:::

Für Symbole empfehlen wir die Verwendung von: 
*   `PNG` Format für Symbole, Sie können aber auch `BMP` `GIF` `ICO` oder `JPEG` Formate verwenden.  
*   Bilder mit einer Größe von 128 x 128 px, die bei Bedarf vom Browser geändert werden.  

Die Verzeichnisse Ihres Projekts sollten der folgenden Struktur ähneln.   

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

Als Nächstes fügen Sie die Symbole zur `manifest.json` Datei hinzu. Aktualisieren Sie Ihre `manifest.json` Datei mit den Symbolen-Informationen, damit Sie dem folgenden Codeausschnitt entspricht. Die `png` im folgenden Code aufgelisteten Dateien sind in der oben in diesem Artikel genannten Downloaddatei verfügbar.  

```json
{
    &quot;name&quot;: &quot;NASA picture of the day viewer&quot;,
    &quot;version&quot;: &quot;0.0.0.1&quot;,
    &quot;manifest_version&quot;: 2,
    &quot;description&quot;: &quot;A chromium extension to show the NASA picture of the day.&quot;,
    &quot;icons&quot;: {
        &quot;16&quot;: &quot;icons/nasapod16x16.png&quot;,
        &quot;32&quot;: &quot;icons/nasapod32x32.png&quot;,
        &quot;48&quot;: &quot;icons/nasapod48x48.png&quot;,
        &quot;128&quot;: &quot;icons/nasapod128x128.png"
    }
}
```  

## Schritt 3: Öffnen eines standardmäßigen Popup Dialogfelds  

Erstellen Sie nun eine `HTML` Datei, die ausgeführt wird, wenn der Benutzer ihre Erweiterung startet.  Erstellen Sie die HTML-Datei `popup.html` , die in einem Verzeichnis mit dem Namen aufgerufen wird `popup` .  Wenn Benutzer das Symbol zum Starten der Erweiterung auswählen, `popup/popup.html` wird es als modales Dialogfeld angezeigt.  

Fügen Sie den Code aus dem folgenden Codeausschnitt hinzu, um `popup.html` das Sternchen-Bild anzuzeigen.  

```html
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <title>NASA picture of the day</title>
    </head>
    <body>
        <div>
            <img src="/images/stars.jpeg" alt="Display the stars image" />
        </div>
    </body>
</html>
```  

Stellen Sie sicher, dass Sie die Bilddatei `images/stars.jpeg` dem Ordner Images hinzufügen.  Die Verzeichnisse Ihres Projekts sollten der folgenden Struktur ähneln.   

```shell
└── part1
    ├── _manifest.json
    ├── icons
    │   ├── nasapod16x16.png
    │   ├── nasapod32x32.png
    │   ├── nasapod48x48.png
    │   └── nasapod128x128.png
    ├── images
    │   └── stars.jpeg
    └── popup
        └── popup.html
```  

Stellen Sie abschließend sicher, dass Sie das Popup in `manifest.json` unter Registrieren `browser_action` , wie im folgenden Codeausschnitt dargestellt.  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium extension to display the NASA picture of the day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    },
    "browser_action": {
        "default_popup": "popup/popup.html"
    }
}
```  

## Nächste Schritte
Das ist alles, was Sie brauchen, um eine Arbeits Erweiterung zu entwickeln. Fahren Sie jetzt mit querladen fort, und testen Sie Ihre Erweiterung. Weitere Informationen finden Sie unter [querladen einer Erweiterung][TestExtensionSideload].  


<!-- image links -->  

<!--[ImagePart1Heirarchy]: ./media/part1-heirarchy.png "Directory Structure"  -->  
<!--[ImagePart1Badge1]: ./media/part1-badge1.png "Toolbar Badge Icon"  -->  
<!--[ImagePart1Heirarchy1]: ./media/part1-heirarchy1.png "Directory Structure for Extension"  -->  
<!--[ImagePart1Threedots]: ./media/part1-threedots.png "Choose Extensions"  -->  
<!--[ImagePart1DevelopermodeToggle]: ./media/part1-developermode-toggle.png "Enable Developer Mode"  -->  
<!--[ImagePart1InstalledExtension]: ./media/part1-installed-extension.png "Installed Extensions"  -->  

<!-- links -->  

[ArchiveExtensionGettingStartedPart1]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part1/part1 "Abgeschlossene Erweiterungspaket Quelle | Microsoft docs"

[TestExtensionSideload]: ./extension-sideloading.md "Testen der Erweiterung (Sideloading) | Microsoft docs"
