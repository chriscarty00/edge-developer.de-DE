---
description: Erstellen einer Erweiterung, die das NASA-Bild des Tages öffnet
title: Erstellen eines Erweiterungs-Lernprogramms – Teil 1
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, web development, html, css, javascript, developer, extensions
ms.openlocfilehash: dfbe7893ce576c223d2b1d39ec21b6c5f46d8356
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397510"
---
# <a name="create-an-extension-tutorial---part-1"></a><span data-ttu-id="6abf6-104">Erstellen eines Erweiterungs-Lernprogramms – Teil 1</span><span class="sxs-lookup"><span data-stu-id="6abf6-104">Create an extension tutorial - Part 1</span></span>  

## <a name="overview"></a><span data-ttu-id="6abf6-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="6abf6-105">Overview</span></span>  

<span data-ttu-id="6abf6-106">Das Ziel dieses Lernprogramms ist es, eine Microsoft Edge (Chromium)-Erweiterung zu erstellen, die mit einem leeren Verzeichnis beginnt.</span><span class="sxs-lookup"><span data-stu-id="6abf6-106">The goal for this tutorial is to build a Microsoft Edge (Chromium) extension starting with an empty directory.</span></span>  <span data-ttu-id="6abf6-107">Sie erstellen eine Erweiterung, die das NASA-Bild des Tages öffnet.</span><span class="sxs-lookup"><span data-stu-id="6abf6-107">You are building an extension that pops up the NASA picture of the day.</span></span> <span data-ttu-id="6abf6-108">In diesem Lernprogramm erfahren Sie, wie Sie eine Erweiterung erstellen, indem Sie die folgenden Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="6abf6-108">In this tutorial, learn how to create an extension by completing the following actions.</span></span>  

*   <span data-ttu-id="6abf6-109">Erstellen einer `manifest.json` Datei.</span><span class="sxs-lookup"><span data-stu-id="6abf6-109">Creating a `manifest.json` file.</span></span>  
*   <span data-ttu-id="6abf6-110">Hinzufügen von Symbolen.</span><span class="sxs-lookup"><span data-stu-id="6abf6-110">Adding icons.</span></span>  
*   <span data-ttu-id="6abf6-111">Öffnen eines Standardmäßigen Popupdialogfelds.</span><span class="sxs-lookup"><span data-stu-id="6abf6-111">Opening a default pop-up dialog.</span></span>  

## <a name="before-you-begin"></a><span data-ttu-id="6abf6-112">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="6abf6-112">Before you Begin</span></span>

<span data-ttu-id="6abf6-113">Laden Sie den Quellcode herunter, um die abgeschlossene Erweiterung zu testen, die Sie in diesem Lernprogramm [erstellen.][ArchiveExtensionGettingStartedPart1]</span><span class="sxs-lookup"><span data-stu-id="6abf6-113">To test out the completed extension that you are building in this tutorial, download the [source code][ArchiveExtensionGettingStartedPart1].</span></span>  

## <a name="step-1-create-a-manifestjson-file"></a><span data-ttu-id="6abf6-114">Schritt 1: Erstellen einer manifest.json-Datei</span><span class="sxs-lookup"><span data-stu-id="6abf6-114">Step 1: Create a manifest.json file</span></span>

<span data-ttu-id="6abf6-115">Jedes Erweiterungspaket muss eine `manifest.json` Datei im Stammverzeichnis haben.</span><span class="sxs-lookup"><span data-stu-id="6abf6-115">Every extension package must have a `manifest.json` file at the root.</span></span>  <span data-ttu-id="6abf6-116">Das Manifest enthält Details ihrer Erweiterung, der Erweiterungspaketversion, des Erweiterungsnamens und der Beschreibung, und so weiter.</span><span class="sxs-lookup"><span data-stu-id="6abf6-116">The manifest provides details of your extension, the extension package version, the extension name and description, and so on.</span></span>  

<span data-ttu-id="6abf6-117">Der folgende Codeausschnitt beschreibt die grundlegenden Informationen, die in Ihrer Datei benötigt `manifest.json` werden.</span><span class="sxs-lookup"><span data-stu-id="6abf6-117">The following code snippet outlines the basic information needed in your `manifest.json` file.</span></span>  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to display the NASA picture of the day."
}
```  

## <a name="step-2-add-icons"></a><span data-ttu-id="6abf6-118">Schritt 2: Hinzufügen von Symbolen</span><span class="sxs-lookup"><span data-stu-id="6abf6-118">Step 2: Add icons</span></span>  

<span data-ttu-id="6abf6-119">Erstellen Sie zunächst das `icons` Verzeichnis in Ihrem Projekt, um die Symbolbilddateien zu speichern.</span><span class="sxs-lookup"><span data-stu-id="6abf6-119">Start by creating the `icons` directory in your project to store the icon image files.</span></span>  <span data-ttu-id="6abf6-120">Die Symbole werden für das Hintergrundbild der Schaltfläche verwendet, die Benutzer zum Starten der Erweiterung auswählen.</span><span class="sxs-lookup"><span data-stu-id="6abf6-120">The icons are used for the background image of the button that users select to launch the extension.</span></span>  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Symbol auf der Symbolleiste zum Öffnen der Erweiterung":::
   <span data-ttu-id="6abf6-122">Symbol auf der Symbolleiste zum Öffnen der Erweiterung</span><span class="sxs-lookup"><span data-stu-id="6abf6-122">Icon on the toolbar to open your extension</span></span>  
:::image-end:::  

<span data-ttu-id="6abf6-123">Für Symbole wird die Verwendung von folgenden Symbolen empfohlen:</span><span class="sxs-lookup"><span data-stu-id="6abf6-123">For icons, we recommend using:</span></span> 
*   `PNG` <span data-ttu-id="6abf6-124">format for icons, but you may also use `BMP` , `GIF` , or `ICO` `JPEG` formats.</span><span class="sxs-lookup"><span data-stu-id="6abf6-124">format for icons, but you may also use `BMP`, `GIF`, `ICO` or `JPEG` formats.</span></span>  
*   <span data-ttu-id="6abf6-125">Bilder mit einer Größe von 128 x 128 px, die bei Bedarf vom Browser angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="6abf6-125">Images that are 128 x 128 px, which are resized by the browser if necessary.</span></span>  

<span data-ttu-id="6abf6-126">Die Verzeichnisse Ihres Projekts sollten der folgenden Struktur ähnlich sein.</span><span class="sxs-lookup"><span data-stu-id="6abf6-126">The directories of your project should be similar to the following structure.</span></span>   

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

<span data-ttu-id="6abf6-127">Fügen Sie als Nächstes die Symbole der Datei `manifest.json` hinzu.</span><span class="sxs-lookup"><span data-stu-id="6abf6-127">Next, add the icons to the `manifest.json` file.</span></span> <span data-ttu-id="6abf6-128">Aktualisieren Sie `manifest.json` Ihre Datei mit den Symbolinformationen, sodass sie mit dem folgenden Codeausschnitt entspricht.</span><span class="sxs-lookup"><span data-stu-id="6abf6-128">Update your `manifest.json` file with the icons information so that it matches the following code snippet.</span></span> <span data-ttu-id="6abf6-129">Die im folgenden Code aufgeführten Dateien sind in der oben in diesem Artikel erwähnten `png` Downloaddatei verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6abf6-129">The `png` files listed in the following code are available in the download file mentioned earlier in this article.</span></span>  

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

## <a name="step-3-open-a-default-pop-up-dialog"></a><span data-ttu-id="6abf6-130">Schritt 3: Öffnen eines Standardmäßigen Popupdialogfelds</span><span class="sxs-lookup"><span data-stu-id="6abf6-130">Step 3: Open a default pop-up dialog</span></span>  

<span data-ttu-id="6abf6-131">Erstellen Sie nun eine Datei, die beim Starten der Erweiterung `HTML` durch den Benutzer ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6abf6-131">Now, create a `HTML` file to run when the user launches your extension.</span></span>  <span data-ttu-id="6abf6-132">Erstellen Sie die HTML-Datei `popup.html` namens in einem Verzeichnis namens `popup` .</span><span class="sxs-lookup"><span data-stu-id="6abf6-132">Create the HTML file named `popup.html` in a directory named `popup`.</span></span>  <span data-ttu-id="6abf6-133">Wenn Benutzer das Symbol zum Starten der Erweiterung auswählen, `popup/popup.html` wird es als modales Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6abf6-133">When users select the icon to launch the extension, `popup/popup.html` is displayed as a modal dialog.</span></span>  

<span data-ttu-id="6abf6-134">Fügen Sie den Code aus dem folgenden Codeausschnitt hinzu, `popup.html` um das Sternbild anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="6abf6-134">Add the code from the following code snippet to `popup.html` to display the stars image.</span></span>  

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

<span data-ttu-id="6abf6-135">Stellen Sie sicher, dass Sie die Bilddatei `images/stars.jpeg` dem Ordner "Bilder" hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6abf6-135">Ensure that you add the image file `images/stars.jpeg` to the images folder.</span></span>  <span data-ttu-id="6abf6-136">Die Verzeichnisse Ihres Projekts sollten der folgenden Struktur ähnlich sein.</span><span class="sxs-lookup"><span data-stu-id="6abf6-136">The directories of your project should be similar to the following structure.</span></span>   

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

<span data-ttu-id="6abf6-137">Stellen Sie schließlich sicher, dass Sie das Popup unter `manifest.json` `browser_action` registrieren, wie im folgenden Codeausschnitt gezeigt.</span><span class="sxs-lookup"><span data-stu-id="6abf6-137">Finally, ensure you register the pop-up in `manifest.json` under `browser_action`, as shown in the following code snippet.</span></span>  

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

## <a name="next-steps"></a><span data-ttu-id="6abf6-138">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="6abf6-138">Next steps</span></span>
<span data-ttu-id="6abf6-139">Dies ist alles, was Sie zum Entwickeln einer Arbeitserweiterung benötigen.</span><span class="sxs-lookup"><span data-stu-id="6abf6-139">That is everything you need to develop a working extension.</span></span>  <span data-ttu-id="6abf6-140">Fahren Sie nun mit dem Querladen fort, und testen Sie die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="6abf6-140">Now, continue on to sideload and test your extension.</span></span> <span data-ttu-id="6abf6-141">Weitere Informationen finden Sie unter [Querladen einer Erweiterung][TestExtensionSideload].</span><span class="sxs-lookup"><span data-stu-id="6abf6-141">For more information, navigate to [Sideload an extension][TestExtensionSideload].</span></span>  

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
