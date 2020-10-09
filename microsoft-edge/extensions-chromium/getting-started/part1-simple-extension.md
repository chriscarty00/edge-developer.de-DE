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
# <span data-ttu-id="27242-104">Erstellen eines Erweiterungs Lernprogramms – Teil 1</span><span class="sxs-lookup"><span data-stu-id="27242-104">Create an extension tutorial - Part 1</span></span>  

## <span data-ttu-id="27242-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="27242-105">Overview</span></span>  

<span data-ttu-id="27242-106">Das Ziel dieses Lernprogramms besteht darin, eine Microsoft Edge-Erweiterung (Chrom) zu erstellen, die mit einem leeren Verzeichnis beginnt.</span><span class="sxs-lookup"><span data-stu-id="27242-106">The goal for this tutorial is to build a Microsoft Edge (Chromium) extension starting with an empty directory.</span></span> <span data-ttu-id="27242-107">Wir erstellen eine Erweiterung, die das NASA-Bild des Tages öffnet.</span><span class="sxs-lookup"><span data-stu-id="27242-107">We'll build an extension that pops up the NASA picture of the day.</span></span> <span data-ttu-id="27242-108">In diesem Lernprogramm erfahren Sie, wie Sie eine Erweiterung erstellen, indem Sie:</span><span class="sxs-lookup"><span data-stu-id="27242-108">In this tutorial, you'll learn how to create an extension by:</span></span>

*   <span data-ttu-id="27242-109">Erstellen einer `manifest.json` Datei</span><span class="sxs-lookup"><span data-stu-id="27242-109">Creating a `manifest.json` file.</span></span>  
*   <span data-ttu-id="27242-110">Symbole werden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="27242-110">Adding icons.</span></span>  
*   <span data-ttu-id="27242-111">Öffnen eines standardmäßigen Popup Dialogfelds</span><span class="sxs-lookup"><span data-stu-id="27242-111">Opening a default pop-up dialog.</span></span>  

## <span data-ttu-id="27242-112">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="27242-112">Before you Begin</span></span>

<span data-ttu-id="27242-113">Wenn Sie die abgeschlossene Erweiterung testen möchten, die Sie in diesem Lernprogramm erstellen, laden Sie den [Quellcode][ArchiveExtensionGettingStartedPart1]herunter.</span><span class="sxs-lookup"><span data-stu-id="27242-113">If you'd like to test out the completed extension that you'll build in this tutorial, download the [source code][ArchiveExtensionGettingStartedPart1].</span></span>  

## <span data-ttu-id="27242-114">Schritt 1: Erstellen einer `manifest.json` Datei</span><span class="sxs-lookup"><span data-stu-id="27242-114">Step 1: Create a `manifest.json` file</span></span>

<span data-ttu-id="27242-115">Für jedes Erweiterungspaket muss eine `manifest.json` Datei am Stamm vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="27242-115">Every extension package must have a `manifest.json` file at the root.</span></span>  <span data-ttu-id="27242-116">Das Manifest enthält Details zu ihrer Erweiterung, der Erweiterungspaket Version, dem Namen der Erweiterung und der Beschreibung usw.</span><span class="sxs-lookup"><span data-stu-id="27242-116">The manifest provides details of your extension, the extension package version, the extension name and description, and so on.</span></span>  

<span data-ttu-id="27242-117">Der folgende Codeausschnitt beschreibt die grundlegenden Informationen, die in der `manifest.json` Datei benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="27242-117">The following code snippet outlines the basic information needed in your `manifest.json` file.</span></span>  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to display the NASA picture of the day."
}
```  

## <span data-ttu-id="27242-118">Schritt 2: Hinzufügen von Symbolen</span><span class="sxs-lookup"><span data-stu-id="27242-118">Step 2: Add icons</span></span>  

<span data-ttu-id="27242-119">Erstellen Sie zunächst das `icons` Verzeichnis in Ihrem Projekt, in dem die Symbolbild Dateien gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="27242-119">Start by creating the `icons` directory in your project to store the icon image files.</span></span>  <span data-ttu-id="27242-120">Die Symbole werden für das Hintergrundbild der Schaltfläche verwendet, die Benutzer zum Starten der Erweiterung auswählen.</span><span class="sxs-lookup"><span data-stu-id="27242-120">The icons are used for the background image of the button that users select to launch the extension.</span></span>  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Symbol auf der Symbolleiste, um die Erweiterung zu öffnen":::
   <span data-ttu-id="27242-122">Symbol auf der Symbolleiste, um die Erweiterung zu öffnen</span><span class="sxs-lookup"><span data-stu-id="27242-122">Icon on the toolbar to open your extension</span></span>
:::image-end:::

<span data-ttu-id="27242-123">Für Symbole empfehlen wir die Verwendung von:</span><span class="sxs-lookup"><span data-stu-id="27242-123">For icons, we recommend using:</span></span> 
*   `PNG` <span data-ttu-id="27242-124">Format für Symbole, Sie können aber auch `BMP` `GIF` `ICO` oder `JPEG` Formate verwenden.</span><span class="sxs-lookup"><span data-stu-id="27242-124">format for icons, but you may also use `BMP`, `GIF`, `ICO` or `JPEG` formats.</span></span>  
*   <span data-ttu-id="27242-125">Bilder mit einer Größe von 128 x 128 px, die bei Bedarf vom Browser geändert werden.</span><span class="sxs-lookup"><span data-stu-id="27242-125">Images that are 128 x 128 px, which are resized by the browser if necessary.</span></span>  

<span data-ttu-id="27242-126">Die Verzeichnisse Ihres Projekts sollten der folgenden Struktur ähneln.</span><span class="sxs-lookup"><span data-stu-id="27242-126">The directories of your project should be similar to the following structure.</span></span>   

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

<span data-ttu-id="27242-127">Als Nächstes fügen Sie die Symbole zur `manifest.json` Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="27242-127">Next, add the icons to the `manifest.json` file.</span></span> <span data-ttu-id="27242-128">Aktualisieren Sie Ihre `manifest.json` Datei mit den Symbolen-Informationen, damit Sie dem folgenden Codeausschnitt entspricht.</span><span class="sxs-lookup"><span data-stu-id="27242-128">Update your `manifest.json` file with the icons information so that it matches the following code snippet.</span></span> <span data-ttu-id="27242-129">Die `png` im folgenden Code aufgelisteten Dateien sind in der oben in diesem Artikel genannten Downloaddatei verfügbar.</span><span class="sxs-lookup"><span data-stu-id="27242-129">The `png` files listed in the following code are available in the download file mentioned earlier in this article.</span></span>  

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

## <span data-ttu-id="27242-130">Schritt 3: Öffnen eines standardmäßigen Popup Dialogfelds</span><span class="sxs-lookup"><span data-stu-id="27242-130">Step 3: Open a default pop-up dialog</span></span>  

<span data-ttu-id="27242-131">Erstellen Sie nun eine `HTML` Datei, die ausgeführt wird, wenn der Benutzer ihre Erweiterung startet.</span><span class="sxs-lookup"><span data-stu-id="27242-131">Now, create a `HTML` file that's run when the user launches your extension.</span></span>  <span data-ttu-id="27242-132">Erstellen Sie die HTML-Datei `popup.html` , die in einem Verzeichnis mit dem Namen aufgerufen wird `popup` .</span><span class="sxs-lookup"><span data-stu-id="27242-132">Create the HTML file called `popup.html` in a directory called `popup`.</span></span>  <span data-ttu-id="27242-133">Wenn Benutzer das Symbol zum Starten der Erweiterung auswählen, `popup/popup.html` wird es als modales Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="27242-133">When users select the icon to launch the extension, `popup/popup.html` is displayed as a modal dialog.</span></span>  

<span data-ttu-id="27242-134">Fügen Sie den Code aus dem folgenden Codeausschnitt hinzu, um `popup.html` das Sternchen-Bild anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="27242-134">Add the code from the following code snippet to `popup.html` to display the stars image.</span></span>  

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

<span data-ttu-id="27242-135">Stellen Sie sicher, dass Sie die Bilddatei `images/stars.jpeg` dem Ordner Images hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="27242-135">Ensure that you add the image file `images/stars.jpeg` to the images folder.</span></span>  <span data-ttu-id="27242-136">Die Verzeichnisse Ihres Projekts sollten der folgenden Struktur ähneln.</span><span class="sxs-lookup"><span data-stu-id="27242-136">The directories of your project should be similar to the following structure.</span></span>   

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

<span data-ttu-id="27242-137">Stellen Sie abschließend sicher, dass Sie das Popup in `manifest.json` unter Registrieren `browser_action` , wie im folgenden Codeausschnitt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="27242-137">Finally, ensure you register the pop-up in `manifest.json` under `browser_action`, as shown in the following code snippet.</span></span>  

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

## <span data-ttu-id="27242-138">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="27242-138">Next steps</span></span>
<span data-ttu-id="27242-139">Das ist alles, was Sie brauchen, um eine Arbeits Erweiterung zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="27242-139">That's everything you need to develop a working extension.</span></span> <span data-ttu-id="27242-140">Fahren Sie jetzt mit querladen fort, und testen Sie Ihre Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="27242-140">Now, continue on to sideload and test your extension.</span></span> <span data-ttu-id="27242-141">Weitere Informationen finden Sie unter [querladen einer Erweiterung][TestExtensionSideload].</span><span class="sxs-lookup"><span data-stu-id="27242-141">For more information, see [Sideload an extension][TestExtensionSideload].</span></span>  


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
