---
description: Erstellen einer Erweiterung, die das NASA-Bild des Tages öffnet
title: Erstellen eines Erweiterungs-Lernprogramms – Teil 1
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Edge Chromium, Webentwicklung, html, css, javascript, Entwickler, Erweiterungen
ms.openlocfilehash: dfbe7893ce576c223d2b1d39ec21b6c5f46d8356
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397510"
---
# <a name="create-an-extension-tutorial---part-1"></a>Erstellen eines Erweiterungs-Lernprogramms – Teil 1  

## <a name="overview"></a>Übersicht  

Das Ziel dieses Lernprogramms ist es, eine Microsoft Edge (Chromium)-Erweiterung zu erstellen, die mit einem leeren Verzeichnis beginnt.  Sie erstellen eine Erweiterung, die das NASA-Bild des Tages öffnet. In diesem Lernprogramm erfahren Sie, wie Sie eine Erweiterung erstellen, indem Sie die folgenden Aktionen ausführen.  

*   Erstellen einer `manifest.json` Datei.  
*   Hinzufügen von Symbolen.  
*   Öffnen eines Standardmäßigen Popupdialogfelds.  

## <a name="before-you-begin"></a>Bevor Sie beginnen

Laden Sie den Quellcode herunter, um die abgeschlossene Erweiterung zu testen, die Sie in diesem Lernprogramm [erstellen.][ArchiveExtensionGettingStartedPart1]  

## <a name="step-1-create-a-manifestjson-file"></a>Schritt 1: Erstellen einer manifest.json-Datei

Jedes Erweiterungspaket muss eine `manifest.json` Datei im Stammverzeichnis haben.  Das Manifest enthält Details ihrer Erweiterung, der Erweiterungspaketversion, des Erweiterungsnamens und der Beschreibung, und so weiter.  

Der folgende Codeausschnitt beschreibt die grundlegenden Informationen, die in Ihrer Datei benötigt `manifest.json` werden.  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to display the NASA picture of the day."
}
```  

## <a name="step-2-add-icons"></a>Schritt 2: Hinzufügen von Symbolen  

Erstellen Sie zunächst das `icons` Verzeichnis in Ihrem Projekt, um die Symbolbilddateien zu speichern.  Die Symbole werden für das Hintergrundbild der Schaltfläche verwendet, die Benutzer zum Starten der Erweiterung auswählen.  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Symbol auf der Symbolleiste zum Öffnen der Erweiterung":::
   Symbol auf der Symbolleiste zum Öffnen der Erweiterung  
:::image-end:::  

Für Symbole wird die Verwendung von folgenden Symbolen empfohlen: 
*   `PNG` format for icons, but you may also use `BMP` , `GIF` , or `ICO` `JPEG` formats.  
*   Bilder mit einer Größe von 128 x 128 px, die bei Bedarf vom Browser angepasst werden.  

Die Verzeichnisse Ihres Projekts sollten der folgenden Struktur ähnlich sein.   

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

Fügen Sie als Nächstes die Symbole der Datei `manifest.json` hinzu. Aktualisieren Sie `manifest.json` Ihre Datei mit den Symbolinformationen, sodass sie mit dem folgenden Codeausschnitt entspricht. Die im folgenden Code aufgeführten Dateien sind in der oben in diesem Artikel erwähnten `png` Downloaddatei verfügbar.  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium extension to show the NASA picture of the day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    }
}
```  

## <a name="step-3-open-a-default-pop-up-dialog"></a>Schritt 3: Öffnen eines Standardmäßigen Popupdialogfelds  

Erstellen Sie nun eine Datei, die beim Starten der Erweiterung `HTML` durch den Benutzer ausgeführt werden soll.  Erstellen Sie die HTML-Datei `popup.html` namens in einem Verzeichnis namens `popup` .  Wenn Benutzer das Symbol zum Starten der Erweiterung auswählen, `popup/popup.html` wird es als modales Dialogfeld angezeigt.  

Fügen Sie den Code aus dem folgenden Codeausschnitt hinzu, `popup.html` um das Sternbild anzeigen zu können.  

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

Stellen Sie sicher, dass Sie die Bilddatei `images/stars.jpeg` dem Ordner "Bilder" hinzufügen.  Die Verzeichnisse Ihres Projekts sollten der folgenden Struktur ähnlich sein.   

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

Stellen Sie schließlich sicher, dass Sie das Popup unter `manifest.json` `browser_action` registrieren, wie im folgenden Codeausschnitt gezeigt.  

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

## <a name="next-steps"></a>Nächste Schritte
Dies ist alles, was Sie zum Entwickeln einer Arbeitserweiterung benötigen.  Fahren Sie nun mit dem Querladen fort, und testen Sie die Erweiterung. Weitere Informationen finden Sie unter [Querladen einer Erweiterung][TestExtensionSideload].  

<!-- image links -->  

<!--[ImagePart1Heirarchy]: ./media/part1-heirarchy.png "Directory Structure"  -->  
<!--[ImagePart1Badge1]: ./media/part1-badge1.png "Toolbar Badge Icon"  -->  
<!--[ImagePart1Heirarchy1]: ./media/part1-heirarchy1.png "Directory Structure for Extension"  -->  
<!--[ImagePart1Threedots]: ./media/part1-threedots.png "Choose Extensions"  -->  
<!--[ImagePart1DevelopermodeToggle]: ./media/part1-developermode-toggle.png "Enable Developer Mode"  -->  
<!--[ImagePart1InstalledExtension]: ./media/part1-installed-extension.png "Installed Extensions"  -->  

<!-- links -->  

[ArchiveExtensionGettingStartedPart1]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part1/part1 "Abgeschlossene Erweiterungspaketquelle | Microsoft Docs"

[TestExtensionSideload]: ./extension-sideloading.md "Testen der Erweiterung (Querladen) | Microsoft Docs"
