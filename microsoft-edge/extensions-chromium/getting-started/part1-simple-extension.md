---
description: Erweiterungen erste Schritte Teil 1
title: Erstellen einer einfachen Erweiterung, die das NASA-Bild des Tages öffnet
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/08/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, Erweiterungen
ms.openlocfilehash: dd5c1dab0cb9b54b79be7d2728cb9bfde0945185
ms.sourcegitcommit: 0bc1312a1e6a0ac37cf385201db4361fc05184fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2020
ms.locfileid: "10683623"
---
# Erstellen einer einfachen Erweiterung, die das NASA-Bild des Tages öffnet  

[Abgeschlossene Erweiterungspaket Quelle für diesen Teil][ArchiveExtensionGettingStartedPart1]  

## Übersicht  

In Teil 1 besteht das Ziel darin, eine sehr einfache Edge Chrom-Erweiterung zu erstellen, beginnend mit einem leeren Verzeichnis.  Das Ziel für diese Erweiterung besteht darin, die folgenden Aufgaben auszuführen:  

*   Erstellen von Symbolen für die Erweiterung, die an mehreren Stellen und in unterschiedlichen Größen verwendet werden können  
*   Erstellen einer einfachen `manifest.json` Datei  
*   Anzeigen eines Start Symbols, das bei Auswahl ein Popupfenster mit dem NASA-Bild des Tages anzeigt  

## Grundlagen der Manifestdatei  

Für jedes Erweiterungspaket muss eine `manifest.json` Datei am Stamm vorhanden sein.  Sie sollten sich dies als den Entwurf für die Erweiterung vorstellen.  Sie teilt dem Browsermodul mit, welche Version der Erweiterungs-API, die die Erweiterung erwartet, den Namen und die Beschreibung der Erweiterung sowie viele weitere Details, von denen viele in dieser mehrteiligen Erweiterung "erste Schritte" erläutert werden.  

Unten ist die einfache  `manifest.json`  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium Extension to show the NASA Picture of the Day."
}
```  

## Setup für Erweiterungssymbole  

Fügen Sie als nächstes einige Symbole zu `manifest.json` Datei \ hinzu, und erstellen Sie ein neues `/icons` Verzeichnis mit den Symboldateien \).  Die Symbole werden für das Hintergrundbild der Schaltfläche verwendet, die der Benutzer auswählt, um die Erweiterung zu starten \ (sofern vorhanden), und an anderen geeigneten Stellen.  

`PNG` Das empfohlene Format, Sie können aber auch `BMP` , und verwenden `GIF` `ICO` `JPEG` .  Es wird empfohlen, immer mindestens ein Symbol für die 128x128 Pixelgröße zu haben, und der Browser passt die Größe automatisch an.  

Ihre Verzeichnisstruktur sollte wie im folgenden Diagramm aussehen.  

<!--  
:::image type="complex" source="./media/part1-heirarchy.png" alt-text="Directory Structure":::
   Directory Structure
:::image-end:::
-->  

<!--![Directory Structure][ImagePart1Heirarchy]  -->  

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

Ihre aktualisierte `manifest.json` Datei sollte wie folgt angezeigt werden.  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium extension to show the NASA Picture of the Day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    }
}
```  

> [!NOTE]
> Die oben auf `png` dieser Seite erwähnten Symboldateien sind im ZIP-Download enthalten.  

## Hinzufügen eines standardmäßigen Popup Dialogfelds  

Erstellen Sie nun eine `HTML` Datei, die automatisch ausgeführt wird, wenn der Benutzer das Erweiterungssymbol auswählt.  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Symbol für Symbolleiste":::
   Symbol für Symbolleiste
:::image-end:::

<!--![Toolbar Badge Icon][ImagePart1Badge1]  -->  

Die HTML-Datei hat den Namen `popup/popup.html` .  Die Auswahl des Erweiterungssymbols wird `popup/popup.html` als modales Dialogfeld angezeigt, das bis zur Auswahl außerhalb des Dialogfelds bleibt.  

Registrieren Sie dazu die Datei als Standard Popup im `manifest.json` `browser_action` folgenden Code.  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium Extension to show the NASA Picture of the Day.",
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

Fügen Sie die Datei in das `popup` Verzeichnis ein, `popup.html` und Rendern Sie das Sternchen-Bild.  Hier ist die `popup.html` Datei.  

```html
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <title>NASA Picture of the Day</title>
    </head>
    <body>
        <div>
            <img src="/images/stars.jpeg" alt="stars" />
        </div>
    </body>
</html>
```  

 Fügen Sie außerdem eine Image-Datei hinzu, `images/stars.jpeg` auf die in der Datei verwiesen wird `popup.html` .  

Die Verzeichnisstruktur für die Beispielerweiterung wird im folgenden Diagramm angezeigt.  

<!--  
:::image type="complex" source="./media/part1-heirarchy1.png" alt-text="Directory Structure for Extension":::
   Directory Structure for Extension
:::image-end:::
-->  

<!--![Directory Structure for Extension][ImagePart1Heirarchy1]  -->  

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

> [!NOTE]
> Die `images/stars.jpeg` im vorherigen Bild aufgelistete Datei steht im [ZIP-Download][ArchiveExtensionGettingStartedPart1]zur Verfügung.  

Das ist alles, was Sie zum Erstellen einer Arbeits Erweiterung benötigen.  Alles, was übrig bleibt, ist es zu testen.  

Im nächsten Abschnitt wird erläutert, wie Sie die Erweiterung \ (manchmal auch als Seite ladend bezeichnet) in den Microsoft Edge \ (Chromium \)-Browser laden, um Sie zu testen.  

## Führen Sie Ihre Erweiterung lokal in Ihrem Browser aus, während Sie Sie entwickeln \ (Seiten laden \)  

Der Microsoft Edge \ (Chrom \)-Browser bietet eine sichere und einfache Möglichkeit zum Ausführen sowie zum Debuggen Ihrer Erweiterungen während der Entwicklung.  

Der Vorgang ist recht einfach.  Sie müssen zuerst die drei Punkte oben im Browser auswählen.  Wählen Sie `Extensions` als nächstes aus dem Kontextmenü aus, wie in der folgenden Abbildung dargestellt.  

:::image type="complex" source="./media/part1-threedots.png" alt-text="Auswählen von Erweiterungen":::
   Auswählen von Erweiterungen
:::image-end:::

<!--![Choose Extensions][ImagePart1Threedots]  -->  

Wenn Sie sich auf der Seite **Erweiterungen** befinden, wie in der folgenden Abbildung gezeigt, aktivieren Sie den **Entwicklermodus** , indem Sie die Umschaltfläche unten links auf der Seite aktivieren, wie in der folgenden Abbildung dargestellt.  

:::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Aktivieren des Entwicklermodus":::
   Aktivieren des Entwicklermodus
:::image-end:::

<!--![Enable Developer Mode][ImagePart1DevelopermodeToggle]  -->  

## Installieren und Aktualisieren von Seiten geladenen Erweiterungen  

Wenn Sie die Erweiterung zum ersten Mal installieren möchten, wählen Sie die `Load Unpacked` Option aus, wie in der folgenden Abbildung dargestellt.  Dadurch werden Sie aufgefordert, ein Verzeichnis zu speichern, in dem die Datei für die Erweiterungsobjekte nach Datei gespeichert ist.  Dadurch wird die Erweiterung so installiert, als ob Sie Sie aus einem Store heruntergeladen hätten.  

:::image type="complex" source="./media/part1-installed-extension.png" alt-text="Installierte Erweiterungen":::
   Installierte Erweiterungen
:::image-end:::

<!--![Installed Extensions][ImagePart1InstalledExtension]  -->  

Nachdem Sie Ihre Erweiterung installiert haben, können Sie Sie aktualisieren, indem Sie die `Reload` Schaltfläche unter Ihrem Erweiterungs Eintrag auswählen.  

Um die Erweiterung aus Ihrem Browser zu entfernen, klicken Sie `Remove` auf die Schaltfläche auf der Unterseite des Erweiterungs Eintrags.  

## Debuggen von Erweiterungen  

Das Debuggen von Erweiterungen ist recht einfach und unterstützt alle Features von Edge Chromium devtools.  Diese Details werden in diesem Leitfaden für erste Schritte jedoch nicht behandelt, sind aber sehr wichtig, um Erweiterungen erfolgreich zu erstellen.  

<!-- image links -->  

<!--[ImagePart1Heirarchy]: ./media/part1-heirarchy.png "Directory Structure"  -->  
<!--[ImagePart1Badge1]: ./media/part1-badge1.png "Toolbar Badge Icon"  -->  
<!--[ImagePart1Heirarchy1]: ./media/part1-heirarchy1.png "Directory Structure for Extension"  -->  
<!--[ImagePart1Threedots]: ./media/part1-threedots.png "Choose Extensions"  -->  
<!--[ImagePart1DevelopermodeToggle]: ./media/part1-developermode-toggle.png "Enable Developer Mode"  -->  
<!--[ImagePart1InstalledExtension]: ./media/part1-installed-extension.png "Installed Extensions"  -->  

<!-- links -->  

[ArchiveExtensionGettingStartedPart1]: ./extension-source/extension-getting-started-part1.zip "Abgeschlossene Erweiterungspaket Quelle für diesen Teil | Microsoft docs"  
