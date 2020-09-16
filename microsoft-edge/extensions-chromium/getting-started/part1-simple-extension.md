---
description: Erweiterungen erste Schritte Teil 1
title: Erstellen einer einfachen Erweiterung, die das NASA-Bild des Tages öffnet
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, Erweiterungen
ms.openlocfilehash: 826401869b98d339e9b156a3727d94bd1182063d
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015765"
---
# <span data-ttu-id="ba0b9-104">Erstellen einer einfachen Erweiterung, die das NASA-Bild des Tages öffnet</span><span class="sxs-lookup"><span data-stu-id="ba0b9-104">Build A Simple Extension That Pops Up NASA Picture Of The Day</span></span> 
 
<!--  
[Completed Extension Package Source for This Part][ArchiveExtensionGettingStartedPart1]  
-->  

## <span data-ttu-id="ba0b9-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="ba0b9-105">Overview</span></span>  

<span data-ttu-id="ba0b9-106">In Teil 1 besteht das Ziel darin, eine sehr einfache Edge Chrom-Erweiterung zu erstellen, beginnend mit einem leeren Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-106">In part 1, the goal is to build a very simple Edge Chromium Extension starting with an empty directory.</span></span>  <span data-ttu-id="ba0b9-107">Das Ziel für diese Erweiterung besteht darin, die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="ba0b9-107">The goal for this Extension is to complete the following tasks.</span></span>  

*   <span data-ttu-id="ba0b9-108">Erstellen von Symbolen für die Erweiterung, die an mehreren Stellen und in unterschiedlichen Größen verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="ba0b9-108">Create icons for the Extension that may be used in multiple places and in different sizes</span></span>  
*   <span data-ttu-id="ba0b9-109">Erstellen einer einfachen `manifest.json` Datei</span><span class="sxs-lookup"><span data-stu-id="ba0b9-109">Create a simple `manifest.json` file</span></span>  
*   <span data-ttu-id="ba0b9-110">Anzeigen eines Start Symbols, das bei Auswahl ein Popupfenster mit dem NASA-Bild des Tages anzeigt</span><span class="sxs-lookup"><span data-stu-id="ba0b9-110">Display a launch icon that when selected displays a pop-up window containing the NASA picture of the day</span></span>  

## <span data-ttu-id="ba0b9-111">Grundlagen der Manifestdatei</span><span class="sxs-lookup"><span data-stu-id="ba0b9-111">The manifest file basics</span></span>  

<span data-ttu-id="ba0b9-112">Für jedes Erweiterungspaket muss eine `manifest.json` Datei am Stamm vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-112">Every Extension package must have a `manifest.json` file at the root.</span></span>  <span data-ttu-id="ba0b9-113">Sie sollten sich dies als den Entwurf für die Erweiterung vorstellen.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-113">You should think of this as the blueprint for the Extension.</span></span>  <span data-ttu-id="ba0b9-114">Sie teilt dem Browsermodul mit, welche Version der Erweiterungs-API, die die Erweiterung erwartet, den Namen und die Beschreibung der Erweiterung sowie viele weitere Details, von denen viele in dieser mehrteiligen Erweiterung "erste Schritte" erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-114">It tells the browser engine what version of the Extension API the Extension expects, the name and description of the Extension, and lots of other details, many of which are discussed in this multi-part Extension Getting Started guide.</span></span>  

<span data-ttu-id="ba0b9-115">Unten ist die einfache</span><span class="sxs-lookup"><span data-stu-id="ba0b9-115">Below is the simple</span></span>  `manifest.json`  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium Extension to show the NASA Picture of the Day."
}
```  

## <span data-ttu-id="ba0b9-116">Setup für Erweiterungssymbole</span><span class="sxs-lookup"><span data-stu-id="ba0b9-116">Extension icons setup</span></span>  

<span data-ttu-id="ba0b9-117">Fügen Sie als nächstes einige Symbole zu `manifest.json` Datei \ hinzu, und erstellen Sie ein neues `/icons` Verzeichnis mit den Symboldateien \).</span><span class="sxs-lookup"><span data-stu-id="ba0b9-117">Next add some icons to `manifest.json` file \(and create a new `/icons` directory with the icons files\).</span></span>  <span data-ttu-id="ba0b9-118">Die Symbole werden für das Hintergrundbild der Schaltfläche verwendet, die der Benutzer auswählt, um die Erweiterung zu starten \ (sofern vorhanden), und an anderen geeigneten Stellen.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-118">The icons are used for the background image of the button the user selects to launch the extension \(if there is one\), and other places that are appropriate.</span></span>  

`PNG` <span data-ttu-id="ba0b9-119">Das empfohlene Format, Sie können aber auch `BMP` , und verwenden `GIF` `ICO` `JPEG` .</span><span class="sxs-lookup"><span data-stu-id="ba0b9-119">is the recommended format, but you may also use `BMP`, `GIF`, `ICO` and `JPEG`.</span></span>  <span data-ttu-id="ba0b9-120">Es wird empfohlen, immer mindestens ein Symbol für die 128x128 Pixelgröße zu haben, und der Browser passt die Größe automatisch an.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-120">It is recommended to always have at least a 128x128 pixels size icon and the browser automatically resizes it as necessary.</span></span>  

<span data-ttu-id="ba0b9-121">Ihre Verzeichnisstruktur sollte wie im folgenden Diagramm aussehen.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-121">Your directory structure should look like the following diagram.</span></span>  

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

<span data-ttu-id="ba0b9-122">Ihre aktualisierte `manifest.json` Datei sollte wie folgt angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-122">Your updated `manifest.json` file should appear as follows.</span></span>  

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
> <span data-ttu-id="ba0b9-123">Die oben auf `png` dieser Seite erwähnten Symboldateien sind im ZIP-Download enthalten.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-123">The icon `png` files listed previous code are available in the zip download mentioned at the top of this page.</span></span>  

## <span data-ttu-id="ba0b9-124">Hinzufügen eines standardmäßigen Popup Dialogfelds</span><span class="sxs-lookup"><span data-stu-id="ba0b9-124">Adding a default pop-up dialog</span></span>  

<span data-ttu-id="ba0b9-125">Erstellen Sie nun eine `HTML` Datei, die automatisch ausgeführt wird, wenn der Benutzer das Erweiterungssymbol auswählt.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-125">Now, create an `HTML` file that is automatically run when the user selects on the extension icon.</span></span>  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Symbol für Symbolleiste":::
   <span data-ttu-id="ba0b9-127">Symbol für Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="ba0b9-127">Toolbar Badge Icon</span></span>
:::image-end:::

<!--![Toolbar Badge Icon][ImagePart1Badge1]  -->  

<span data-ttu-id="ba0b9-128">Die HTML-Datei hat den Namen `popup/popup.html` .</span><span class="sxs-lookup"><span data-stu-id="ba0b9-128">The HTML file is named `popup/popup.html`.</span></span>  <span data-ttu-id="ba0b9-129">Die Auswahl des Erweiterungssymbols wird `popup/popup.html` als modales Dialogfeld angezeigt, das bis zur Auswahl außerhalb des Dialogfelds bleibt.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-129">Selecting the Extension icon launches `popup/popup.html` as modal dialog that stays up until you select outside the dialog.</span></span>  

<span data-ttu-id="ba0b9-130">Registrieren Sie dazu die Datei als Standard Popup im `manifest.json` `browser_action` folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-130">For this, register the file as a default pop-up in the `manifest.json` under `browser_action` in the following code.</span></span>  

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

<span data-ttu-id="ba0b9-131">Fügen Sie die Datei in das `popup` Verzeichnis ein, `popup.html` und Rendern Sie das Sternchen-Bild.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-131">In the `popup` directory , add the file `popup.html` and have it render the stars image.</span></span>  <span data-ttu-id="ba0b9-132">Hier ist die `popup.html` Datei.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-132">Here is the `popup.html` file.</span></span>  

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

 <span data-ttu-id="ba0b9-133">Fügen Sie außerdem eine Image-Datei hinzu, `images/stars.jpeg` auf die in der Datei verwiesen wird `popup.html` .</span><span class="sxs-lookup"><span data-stu-id="ba0b9-133">Also, add an image file `images/stars.jpeg` that is referenced in the `popup.html` file.</span></span>  

<span data-ttu-id="ba0b9-134">Die Verzeichnisstruktur für die Beispielerweiterung wird im folgenden Diagramm angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-134">The directory structure for the example Extension is displayed in the following diagram.</span></span>  

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

<!--  
> [!NOTE]
> The `images/stars.jpeg` file listed in the previous image is available in the [zip download][ArchiveExtensionGettingStartedPart1].  
-->  

<span data-ttu-id="ba0b9-135">Das ist alles, was Sie zum Erstellen einer Arbeits Erweiterung benötigen.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-135">That is everything you need to build a working Extension.</span></span>  <span data-ttu-id="ba0b9-136">Alles, was noch zu tun ist, ist es zu testen.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-136">All that is left to do is test it.</span></span>  

<span data-ttu-id="ba0b9-137">Im nächsten Abschnitt wird erläutert, wie Sie die Erweiterung \ (manchmal auch als Seite ladend bezeichnet) in den Microsoft Edge \ (Chromium \)-Browser laden, um Sie zu testen.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-137">The next section explains how to load the Extension \(sometimes called side loading\) into the Microsoft Edge \(Chromium\) browser to test it.</span></span>  

## <span data-ttu-id="ba0b9-138">Führen Sie Ihre Erweiterung lokal in Ihrem Browser aus, während Sie Sie entwickeln \ (Seiten laden \)</span><span class="sxs-lookup"><span data-stu-id="ba0b9-138">Run your Extension locally in your browser while developing it \(side-loading\)</span></span>  

<span data-ttu-id="ba0b9-139">Der Microsoft Edge \ (Chrom \)-Browser bietet eine sichere und einfache Möglichkeit zum Ausführen sowie zum Debuggen Ihrer Erweiterungen während der Entwicklung.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-139">The Microsoft Edge \(Chromium\) browser provides a safe and simple way for you to run as well as debug your Extensions while you are developing.</span></span>  

<span data-ttu-id="ba0b9-140">Der Vorgang ist recht einfach.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-140">The process is quite simple.</span></span>  <span data-ttu-id="ba0b9-141">Sie müssen zuerst die drei Punkte oben im Browser auswählen.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-141">You must first select the three dots at the top of your browser.</span></span>  <span data-ttu-id="ba0b9-142">Wählen Sie `Extensions` als nächstes aus dem Kontextmenü aus, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-142">Next, choose `Extensions` from the context menu as shown in the following image.</span></span>  

:::image type="complex" source="./media/part1-threedots.png" alt-text="Auswählen von Erweiterungen":::
   <span data-ttu-id="ba0b9-144">Auswählen von Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="ba0b9-144">Choose Extensions</span></span>
:::image-end:::

<!--![Choose Extensions][ImagePart1Threedots]  -->  

<span data-ttu-id="ba0b9-145">Wenn Sie sich auf der Seite **Erweiterungen** befinden, wie in der folgenden Abbildung gezeigt, aktivieren Sie den **Entwicklermodus** , indem Sie die Umschaltfläche unten links auf der Seite aktivieren, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-145">When you are on the **Extensions** page as shown in the following image, enable the **Developer mode** by enabling the toggle at the bottom left of the page as shown in the following image.</span></span>  

:::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Aktivieren des Entwicklermodus":::
   <span data-ttu-id="ba0b9-147">Aktivieren des Entwicklermodus</span><span class="sxs-lookup"><span data-stu-id="ba0b9-147">Enable Developer Mode</span></span>
:::image-end:::

<!--![Enable Developer Mode][ImagePart1DevelopermodeToggle]  -->  

## <span data-ttu-id="ba0b9-148">Installieren und Aktualisieren von Seiten geladenen Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="ba0b9-148">Installing and updating side-loaded Extensions</span></span>  

<span data-ttu-id="ba0b9-149">Wenn Sie die Erweiterung zum ersten Mal installieren möchten, wählen Sie die `Load Unpacked` Option aus, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-149">The first time you want to install your Extension, you choose the `Load Unpacked` option as shown in the following image.</span></span>  <span data-ttu-id="ba0b9-150">Dadurch werden Sie aufgefordert, ein Verzeichnis zu speichern, in dem die Datei für die Erweiterungsobjekte nach Datei gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-150">This prompts you for a directory where you have your Extension assets file by file.</span></span>  <span data-ttu-id="ba0b9-151">Dadurch wird die Erweiterung so installiert, als ob Sie Sie aus einem Store heruntergeladen hätten.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-151">This installs the Extension as if you had downloaded it from a store.</span></span>  

:::image type="complex" source="./media/part1-installed-extension.png" alt-text="Installierte Erweiterungen":::
   <span data-ttu-id="ba0b9-153">Installierte Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="ba0b9-153">Installed Extensions</span></span>
:::image-end:::

<!--![Installed Extensions][ImagePart1InstalledExtension]  -->  

<span data-ttu-id="ba0b9-154">Nachdem Sie Ihre Erweiterung installiert haben, können Sie Sie aktualisieren, indem Sie die `Reload` Schaltfläche unter Ihrem Erweiterungs Eintrag auswählen.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-154">After you install your Extension, you may update it by selecting the `Reload` button under your Extension listing.</span></span>  

<span data-ttu-id="ba0b9-155">Um die Erweiterung aus Ihrem Browser zu entfernen, klicken Sie `Remove` auf die Schaltfläche auf der Unterseite des Erweiterungs Eintrags.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-155">To remove the Extension from your browser, click the `Remove` button on the bottom of the Extension listing.</span></span>  

## <span data-ttu-id="ba0b9-156">Debuggen von Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="ba0b9-156">Debugging Extensions</span></span>  

<span data-ttu-id="ba0b9-157">Das Debuggen von Erweiterungen ist recht einfach und unterstützt alle Features von Edge Chromium devtools.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-157">Debugging Extensions is quite easy and supports all of the features in Edge Chromium DevTools.</span></span>  <span data-ttu-id="ba0b9-158">Diese Details werden in diesem Leitfaden für erste Schritte jedoch nicht behandelt, sind aber sehr wichtig, um Erweiterungen erfolgreich zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ba0b9-158">Those details however are not covered in this getting started guide but are very important to successfully build Extensions.</span></span>  

<!-- image links -->  

<!--[ImagePart1Heirarchy]: ./media/part1-heirarchy.png "Directory Structure"  -->  
<!--[ImagePart1Badge1]: ./media/part1-badge1.png "Toolbar Badge Icon"  -->  
<!--[ImagePart1Heirarchy1]: ./media/part1-heirarchy1.png "Directory Structure for Extension"  -->  
<!--[ImagePart1Threedots]: ./media/part1-threedots.png "Choose Extensions"  -->  
<!--[ImagePart1DevelopermodeToggle]: ./media/part1-developermode-toggle.png "Enable Developer Mode"  -->  
<!--[ImagePart1InstalledExtension]: ./media/part1-installed-extension.png "Installed Extensions"  -->  

<!-- links -->  

[ArchiveExtensionGettingStartedPart1]: ./extension-source/extension-getting-started-part1.zip "Abgeschlossene Erweiterungspaket Quelle für diesen Teil | Microsoft docs"  
