---
description: Informationen zum Erstellen einer Microsoft Edge-Erweiterung
title: Erstellen einer Erweiterung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.custom: seodec18
ms.openlocfilehash: a08fc6bd604ce810895e7103f7f6384dbedc9f78
ms.sourcegitcommit: 0bc1312a1e6a0ac37cf385201db4361fc05184fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2020
ms.locfileid: "10683651"
---
# <span data-ttu-id="036e2-104">Erstellen einer Microsoft Edge-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="036e2-104">Creating A Microsoft Edge Extension</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="036e2-105">In diesem Leitfaden erfahren Sie, wie Sie eine Erweiterung für Microsoft Edge erstellen.</span><span class="sxs-lookup"><span data-stu-id="036e2-105">In this guide, learn to create an extension for Microsoft Edge.</span></span>  <span data-ttu-id="036e2-106">Mit dieser Beispielerweiterung können Sie bestimmte CSS für [docs.Microsoft.com][MicrosoftDocs] -Seiten manipulieren, einschließlich der Erstellung einer Manifestdatei, der Benutzeroberfläche sowie von Hintergrund-und Inhalts Skripts.</span><span class="sxs-lookup"><span data-stu-id="036e2-106">This example extension allows you to manipulate specific CSS for [docs.microsoft.com][MicrosoftDocs] pages including walking you through creation of a manifest file, the user interface, and background and content scripts.</span></span>  

:::image type="complex" source="../media/color-changer_header.png" alt-text="Docs.Microsoft.com Body in blau geändert":::
   <span data-ttu-id="036e2-108">Docs.Microsoft.com Body in blau geändert</span><span class="sxs-lookup"><span data-stu-id="036e2-108">Docs.microsoft.com body changed to blue</span></span>
:::image-end:::

<!--![Docs.microsoft.com body changed to blue][ImageColorChangerHeader]  -->  

<span data-ttu-id="036e2-109">In diesem Lernprogramm wird davon ausgegangen, dass Sie grundlegende Kenntnisse darüber haben, was eine Browser Erweiterung ist und wie Sie funktioniert.</span><span class="sxs-lookup"><span data-stu-id="036e2-109">This tutorial assumes you have basic understanding of what a browser extension is and how it work.</span></span>  <span data-ttu-id="036e2-110">Weitere Informationen zu den Bausteinen für Erweiterungen finden Sie unter [Anatomie einer Erweiterung][MDNAnatomyExtension].</span><span class="sxs-lookup"><span data-stu-id="036e2-110">For more imformation about the building blocks for extensions, see [Anatomy of an extension][MDNAnatomyExtension].</span></span>  

<span data-ttu-id="036e2-111">Laden Sie den Code für das [vollständige Beispiel auf GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger]herunter.</span><span class="sxs-lookup"><span data-stu-id="036e2-111">Download the code for the [full sample on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span></span>  

## <span data-ttu-id="036e2-112">Erstellen der Manifestdatei</span><span class="sxs-lookup"><span data-stu-id="036e2-112">Building the manifest file</span></span>  

<span data-ttu-id="036e2-113">Erstellen Sie zunächst ein Verzeichnis für Ihre Erweiterung, und geben Sie Ihr einen Namen `color-changer` .</span><span class="sxs-lookup"><span data-stu-id="036e2-113">To begin, create a directory for your extension and name it `color-changer`.</span></span>  

<span data-ttu-id="036e2-114">Erstellen Sie innerhalb des `color-changer` Ordners eine Datei mit dem Namen `manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="036e2-114">Inside the `color-changer` folder, create a file named `manifest.json`.</span></span>  <span data-ttu-id="036e2-115">Die `manifest.json` Datei ist für alle Erweiterungen erforderlich und enthält wichtige Informationen für die Erweiterung, die vom Namen der Erweiterung bis zu den Berechtigungen reichen.</span><span class="sxs-lookup"><span data-stu-id="036e2-115">The `manifest.json` file is required for all extensions and provides important information for the extension, ranging from the extension name to the permissions.</span></span>  

> [!NOTE] 
> <span data-ttu-id="036e2-116">Dieser Leitfaden führt Sie durch alle manifestschlüssel, die Sie in diesem Leitfaden verwenden müssen, aber eine Liste aller unterstützten und empfohlenen manifestschlüssel finden Sie unter [unterstützte Manifest-Schlüssel][ExtensionsApisupportManifestKeys].</span><span class="sxs-lookup"><span data-stu-id="036e2-116">This guide walks you through all the manifest keys you must use in this guide, but for a list of all supported and recommended manifest keys, see [Supported manifest keys][ExtensionsApisupportManifestKeys].</span></span>  

<span data-ttu-id="036e2-117">`manifest.json`Fügen Sie im Inneren den folgenden Code hinzu.</span><span class="sxs-lookup"><span data-stu-id="036e2-117">Inside `manifest.json`, add the following code.</span></span>  

```json
{
  "name": "Color Changer",
  "author": "Microsoft Edge Extension Developer",
  "version": "1.0",
  "description": "Change the color of the body on docs.microsoft.com",
  "permissions": [
    "*://docs.microsoft.com/*",
    "tabs"
  ], 
  "browser_action": {
    "default_icon": {
      "20": "images/color-changer20.png",
      "40": "images/color-changer40.png"
    },
    "default_title": "Color Changer",
    "default_popup": "popup.html"
  }
}
```  

### <span data-ttu-id="036e2-118">Definitionen für manifestschlüssel</span><span class="sxs-lookup"><span data-stu-id="036e2-118">Manifest key definitions</span></span>  

| <span data-ttu-id="036e2-119">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="036e2-119">Key</span></span> | <span data-ttu-id="036e2-120">Details</span><span class="sxs-lookup"><span data-stu-id="036e2-120">Details</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="036e2-121">name</span><span class="sxs-lookup"><span data-stu-id="036e2-121">name</span></span>][MDNManifestjsonName] | <span data-ttu-id="036e2-122">Der Name der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="036e2-122">The name of the extension.</span></span>  |  
| [<span data-ttu-id="036e2-123">Autor</span><span class="sxs-lookup"><span data-stu-id="036e2-123">author</span></span>][MDNManifestjsonAuthor] | <span data-ttu-id="036e2-124">Der Autor der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="036e2-124">The author of the extension.</span></span>  |  
| [<span data-ttu-id="036e2-125">version</span><span class="sxs-lookup"><span data-stu-id="036e2-125">version</span></span>][MDNManifestjsonVersion] | <span data-ttu-id="036e2-126">Die Versionsnummer der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="036e2-126">The extension version number.</span></span>  |  
| [<span data-ttu-id="036e2-127">description</span><span class="sxs-lookup"><span data-stu-id="036e2-127">description</span></span>][MDNManifestjsonDescription] | <span data-ttu-id="036e2-128">Die Beschreibung der Erweiterung, die im Abschnitt "Info" des Menüs "Erweiterung" in Microsoft Edge angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="036e2-128">The description of the extension displayed in the About section of the extension menu in Microsoft Edge.</span></span>  |  
| [<span data-ttu-id="036e2-129">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="036e2-129">permissions</span></span>][MDNManifestjsonPermissions] | <span data-ttu-id="036e2-130">Ein Array von Zeichenfolgen, die Berechtigungen für die Erweiterung anfordern.</span><span class="sxs-lookup"><span data-stu-id="036e2-130">An array of strings requesting permissions for the extension.</span></span>  <span data-ttu-id="036e2-131">Für Ihre Erweiterung fordern Sie Berechtigungen an, um die besuchten Websites anzuzeigen \ ("Registerkarten" \), und um den Inhalt der URLs zu aktualisieren, die " `*://docs.microsoft.com/*` " entsprechen.</span><span class="sxs-lookup"><span data-stu-id="036e2-131">For your extension, you are requesting permissions to see the websites visited \("tabs"\) and to update content on URLs matching "`*://docs.microsoft.com/*`".</span></span>  |  
| [<span data-ttu-id="036e2-132">browser_action</span><span class="sxs-lookup"><span data-stu-id="036e2-132">browser_action</span></span>][MDNManifestjsonBrowserAction] | <span data-ttu-id="036e2-133">Enthält die Informationen für ein Symbol.</span><span class="sxs-lookup"><span data-stu-id="036e2-133">Contains the information for an icon.</span></span> <span data-ttu-id="036e2-134">Das Symbol befindet sich auf der Microsoft Edge-Symbolleiste rechts neben der Adressleiste.</span><span class="sxs-lookup"><span data-stu-id="036e2-134">The icon is placed on the Microsoft Edge toolbar, to the right of the address bar.</span></span>  |  

#### <span data-ttu-id="036e2-135">browser_action Schlüsseldefinitionen</span><span class="sxs-lookup"><span data-stu-id="036e2-135">browser_action Key definitions</span></span>  

| <span data-ttu-id="036e2-136">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="036e2-136">Key</span></span> | <span data-ttu-id="036e2-137">Details</span><span class="sxs-lookup"><span data-stu-id="036e2-137">Details</span></span> |  
|:--- |:--- |  
| `default_icon` | <span data-ttu-id="036e2-138">Das Symbol, das auf der Symbolleiste verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="036e2-138">The icon that is used in the toolbar.</span></span>  |  
| `default_title` | <span data-ttu-id="036e2-139">Der Text, der angezeigt wird, wenn ein Benutzer auf das Symbol in der Symbolleiste zeigt.</span><span class="sxs-lookup"><span data-stu-id="036e2-139">The text that is displayed when a user hovers over the icon in the toolbar.</span></span>  |  
| `default_popup` | <span data-ttu-id="036e2-140">Der Pfad zur HTML-Datei für das Popupfenster.</span><span class="sxs-lookup"><span data-stu-id="036e2-140">The path to the HTML file for the pop-up window.</span></span>  |  

<span data-ttu-id="036e2-141">Nachdem Sie die Manifestdatei erstellt haben, benötigen Sie eine Benutzeroberfläche für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="036e2-141">Now that you have created the manifest file, you need a user interface for the extension.</span></span>  

## <span data-ttu-id="036e2-142">Erstellen des Popups</span><span class="sxs-lookup"><span data-stu-id="036e2-142">Creating the pop-up</span></span>  

<span data-ttu-id="036e2-143">Erstellen Sie für Ihre Erweiterung ein Popup für die Benutzeroberfläche, wie unten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="036e2-143">For your extension, create a pop-up for the user interface, like below.</span></span>  

:::image type="complex" source="../media/color-changer_popup.png" alt-text="Docs.Microsoft.com Body in blau geändert":::
   <span data-ttu-id="036e2-145">Die Popup Schnittstelle der Erweiterung</span><span class="sxs-lookup"><span data-stu-id="036e2-145">The pop-up interface of the extension</span></span>
:::image-end:::

<!--![The pop-up interface of the extension][ImageColorChangerPopup]  -->  

<span data-ttu-id="036e2-146">Erstellen Sie eine Datei mit dem Namen `popup.html` im Stammverzeichnis Ihres `color-changer` Ordners.</span><span class="sxs-lookup"><span data-stu-id="036e2-146">Create a file named `popup.html` in the root of your `color-changer` folder.</span></span>  <span data-ttu-id="036e2-147">Fügen Sie den folgenden Code in ein `popup.html` .</span><span class="sxs-lookup"><span data-stu-id="036e2-147">Paste the following code into `popup.html`.</span></span>  

```html
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" type="text/css" href="css/styles.css" />
    </head>
    <body>
        <h1>Creating a Microsoft Edge Extension</h1>
        <p>Color Changer</p>
        <input id="aliceblue" type="button" value="Aliceblue" />
        <input id="cornsilk" type="button" value="Cornsilk" />
        <input id="reset" type="button" value="Reset" />
        <script src="js/popup.js"></script>
    </body>
</html>
```  

<span data-ttu-id="036e2-148">In `popup.html` können Sie einen Titel, einen Absatz und drei Schaltflächen (AliceBlue, Cornsilk und Reset \) erstellen.</span><span class="sxs-lookup"><span data-stu-id="036e2-148">In `popup.html`, you create a title, a paragraph, and three buttons \(Aliceblue, Cornsilk, and Reset\).</span></span>  

<span data-ttu-id="036e2-149">Erstellen Sie nun einen Ordner mit dem Namen `css` und in Erstellen einer Datei mit dem Namen `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="036e2-149">Now create a folder named `css` and inside create a file named `styles.css`.</span></span>  <span data-ttu-id="036e2-150">Fügen Sie die folgenden Formatvorlagen hinzu.</span><span class="sxs-lookup"><span data-stu-id="036e2-150">Add the styles below.</span></span>  

```css
/* main styles */
* {
    font-family: 'Segoe UI';
}

h1 {
    font-weight: 600;
    font-size: .9em;
}

p {
    font-weight: 500;
    font-size: .8em;
    margin-bottom: 10px;  
}
```  

<span data-ttu-id="036e2-151">Dieses CSS gibt unserer Erweiterung einige einfache Formatvorlagen.</span><span class="sxs-lookup"><span data-stu-id="036e2-151">This CSS gives our extension some basic styles.</span></span>  <span data-ttu-id="036e2-152">Sie können weitere Formatvorlagen hinzufügen, um Ihre Erweiterung anzupassen.</span><span class="sxs-lookup"><span data-stu-id="036e2-152">Feel free to add more styles to customize your extension.</span></span>  

<span data-ttu-id="036e2-153">Als nächstes müssen Sie die JavaScript-Datei erstellen, die mit dem Popup interagiert.</span><span class="sxs-lookup"><span data-stu-id="036e2-153">Next, you must create the JavaScript file that interacts with the pop-up.</span></span>  <span data-ttu-id="036e2-154">Erstellen Sie einen `js` Ordner und eine Datei mit dem Namen `popup.js` innen.</span><span class="sxs-lookup"><span data-stu-id="036e2-154">Create a `js` folder and a file named `popup.js` inside.</span></span>  <span data-ttu-id="036e2-155">Aktualisieren Sie `popup.js` mit dem folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="036e2-155">Update `popup.js` with the following code.</span></span>  

```JavaScript
// get the buttons by id
let aliceblue = document.getElementById('aliceblue');
let cornsilk = document.getElementById('cornsilk');
let reset = document.getElementById('reset');

// use tabs.insertCSS to change header color on button click

// aliceblue
aliceblue.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: aliceblue !important; }"});
};

// cornsilk
cornsilk.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: cornsilk !important; }"});
};

// back to original
reset.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: none !important; }"});
};
```  

<span data-ttu-id="036e2-156">In bietet `popup.js` die [Registerkarten][MDNApiTabs] -API die Möglichkeit, mit den Registerkarten des Browsers zu interagieren und Skripts und Formatvorlagen in den Seiteninhalt einzufügen.</span><span class="sxs-lookup"><span data-stu-id="036e2-156">In `popup.js`, the [tabs][MDNApiTabs] API allows you to interact with the tabs of the browser and inject script and styles into the page content.</span></span>  <span data-ttu-id="036e2-157">Mit der [Tab. insertCSS ()][MDNApiTabsInsertcss] -Methode fügen Sie das angegebene CSS in die Seite ein, wodurch die Kopfzeile von [docs.Microsoft.com][MicrosoftDocs] in eine andere Farbe geändert wird, wenn auf die angegebene Schaltfläche geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="036e2-157">Using the [tabs.insertCSS()][MDNApiTabsInsertcss] method, you inject the specified CSS into the page which changes the header on [docs.microsoft.com][MicrosoftDocs] to a different color when the specified button is clicked.</span></span>  

<span data-ttu-id="036e2-158">Nachdem Sie nun über die grundlegenden Popup Funktionen verfügen, fügen Sie der Erweiterung Symbole hinzu.</span><span class="sxs-lookup"><span data-stu-id="036e2-158">Now that you have the basic pop-up functionality, add icons to the extension.</span></span>  

## <span data-ttu-id="036e2-159">Hinzufügen von Symbolen</span><span class="sxs-lookup"><span data-stu-id="036e2-159">Adding icons</span></span>  

<span data-ttu-id="036e2-160">Symbole werden verwendet, um die Erweiterung in der Symbolleiste des Browsers, im Menüerweiterungen und an anderen Stellen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="036e2-160">Icons are used to represent the extension in the browser toolbar, the extensions menu, and other places.</span></span>  <span data-ttu-id="036e2-161">Laden [Sie die Symbole für Ihre Erweiterung auf GitHub][GithubMicrosoftEdgeExtensionsDemosColorChangerImages]herunter.</span><span class="sxs-lookup"><span data-stu-id="036e2-161">Download the [icons for your extension on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChangerImages].</span></span> <span data-ttu-id="036e2-162">Weitere Informationen zu Erweiterungssymbolen in Microsoft Edge finden Sie unter [Entwurfshandbuch][ExtensionsGuidesDesignIcons].</span><span class="sxs-lookup"><span data-stu-id="036e2-162">For more information about extension icons in Microsoft Edge, see [Design Guide][ExtensionsGuidesDesignIcons].</span></span>  

<span data-ttu-id="036e2-163">Nachdem Sie die Erweiterungssymbole heruntergeladen haben, speichern Sie die Symbole in einem `images` Ordner in `color-changer` .</span><span class="sxs-lookup"><span data-stu-id="036e2-163">After you download the extension icons, save the icons in an `images` folder inside `color-changer`.</span></span>  

<span data-ttu-id="036e2-164">Das Symbol, das auf der Symbolleiste angezeigt wird `default_icon` , wird innerhalb des [browser_action][MDNManifestjsonBrowserAction] Schlüssels festgesetzt, den Sie bereits zu Ihrer Manifestdatei in einem früheren Abschnitt hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="036e2-164">The icon that appears in the toolbar is set using `default_icon` inside of the [browser_action][MDNManifestjsonBrowserAction] key, which you already added to your manifest file in an earlier section.</span></span>  

<span data-ttu-id="036e2-165">Der `icons` Schlüssel definiert, welche Symbole in den Menüs für die Erweiterungseinstellungen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="036e2-165">The `icons` key defines which icons should be used in the Extensions settings menus.</span></span>  <span data-ttu-id="036e2-166">Im folgenden geben Sie mehrere Symbole mit unterschiedlichen Größen an, die für unterschiedliche Bildschirmauflösungen berücksichtigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="036e2-166">Below, you are specifying multiple icons with different sizes to account for different screen resolutions.</span></span>  <span data-ttu-id="036e2-167">Der Name der Symbole `25` und `48` die Höhe der Symbole in Pixeln.</span><span class="sxs-lookup"><span data-stu-id="036e2-167">The name of the icons, `25` and `48` are the heights in pixels of the icons.</span></span>  

<span data-ttu-id="036e2-168">Schließen Sie im [manifest.jsauf][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] Datei einen Schlüssel auf oberster Ebene für ein `icons` .</span><span class="sxs-lookup"><span data-stu-id="036e2-168">In the [manifest.json][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] file, include a top-level key for `icons`.</span></span>  

```json
  "icons": {
    "25": "images/color-changer25.png",
    "48": "images/color-changer48.png"
  }
```  

### <span data-ttu-id="036e2-169">Definitionen für manifestschlüssel</span><span class="sxs-lookup"><span data-stu-id="036e2-169">Manifest Key definitions</span></span>  

| <span data-ttu-id="036e2-170">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="036e2-170">Key</span></span> | <span data-ttu-id="036e2-171">Details</span><span class="sxs-lookup"><span data-stu-id="036e2-171">Details</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="036e2-172">Symbole</span><span class="sxs-lookup"><span data-stu-id="036e2-172">icons</span></span>][MDNManifestjsonIcons] | <span data-ttu-id="036e2-173">Die Symbole für Ihre Erweiterung mit Schlüssel-Wert-Paaren der Bildgröße in `px` und Bild Pfad relativ zum Stammverzeichnis der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="036e2-173">The icons for your extension with key-value pairs of image size in `px` and image path relative to the root directory of the extension.</span></span> |  

> [!NOTE]
> <span data-ttu-id="036e2-174">Verwenden Sie die Symbole `inactive##.png` , die sich im Ordner "Bilder" befinden, später in diesem Leitfaden.</span><span class="sxs-lookup"><span data-stu-id="036e2-174">Use the icons named `inactive##.png` located in the images folder later in this guide.</span></span>  

## <span data-ttu-id="036e2-175">Testen der Erweiterung</span><span class="sxs-lookup"><span data-stu-id="036e2-175">Testing the extension</span></span>  

<span data-ttu-id="036e2-176">Nachdem Sie nun die Benutzeroberfläche und die erstellten Symbole hinzugefügt haben, testen Sie Ihre Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="036e2-176">Now that you have added the user interface and created icons, test your extension.</span></span>  <span data-ttu-id="036e2-177">Führen Sie die Schritte zum [Hinzufügen einer Erweiterung][ExtensionsGuidesAddingRemovingExtensionsAdding] zu Microsoft Edge durch.</span><span class="sxs-lookup"><span data-stu-id="036e2-177">Walk through the steps for [Adding an extension][ExtensionsGuidesAddingRemovingExtensionsAdding] to Microsoft Edge.</span></span>  <span data-ttu-id="036e2-178">Kehren Sie anschließend zu diesem Leitfaden zurück.</span><span class="sxs-lookup"><span data-stu-id="036e2-178">Afterwards, return to this guide.</span></span>  

<span data-ttu-id="036e2-179">Navigieren Sie nach dem Hinzufügen der Erweiterung zu einer beliebigen [docs.Microsoft.com][MicrosoftDocs] -Seite.</span><span class="sxs-lookup"><span data-stu-id="036e2-179">After you add your extension, navigate to any [docs.microsoft.com][MicrosoftDocs] page.</span></span>  <span data-ttu-id="036e2-180">Nachdem Sie auf die Browser Aktion geklickt haben, sollte das folgende Popup angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="036e2-180">You should see the following pop-up after clicking on the browser action.</span></span>  <span data-ttu-id="036e2-181">Die Farbe des [docs.Microsoft.com][MicrosoftDocs] -Texts sollte auch die Farbe ändern.</span><span class="sxs-lookup"><span data-stu-id="036e2-181">The color of the [docs.microsoft.com][MicrosoftDocs] body should also change color.</span></span>  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_aliceblue.png" alt-text="Docs.Microsoft.com Body in blau geändert":::
         <span data-ttu-id="036e2-183">Docs.Microsoft.com-Kopfzeile geändert in AliceBlue</span><span class="sxs-lookup"><span data-stu-id="036e2-183">Docs.microsoft.com header changed to Aliceblue</span></span> :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Aliceblue][ImageColorChangerHeaderAliceblue]  -->
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_cornsilk.png" alt-text="Docs.Microsoft.com Body in blau geändert":::
         <span data-ttu-id="036e2-185">Docs.Microsoft.com-Kopfzeile geändert in Cornsilk</span><span class="sxs-lookup"><span data-stu-id="036e2-185">Docs.microsoft.com header changed to Cornsilk</span></span> :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Cornsilk][ImageColorChangerHeaderCornsilk]  -->
   :::column-end:::
:::row-end:::

<span data-ttu-id="036e2-186">Wenn Fehler oder Funktionen auftreten, die nicht funktionieren, lesen Sie den Leitfaden zum [Debuggen von Erweiterungen][ExtensionsGuidesDebuggingExtensions] , oder laden Sie das [vollständige Beispiel auf GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger]herunter.</span><span class="sxs-lookup"><span data-stu-id="036e2-186">If you encounter any errors or functionality that does not work, see the [Debugging extensions][ExtensionsGuidesDebuggingExtensions] guide or download the [full sample on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span></span>  

## <span data-ttu-id="036e2-187">Hinzufügen von Inhalten und hintergrundskripts</span><span class="sxs-lookup"><span data-stu-id="036e2-187">Adding content and background scripts</span></span>  

<span data-ttu-id="036e2-188">Gehen Sie einen Schritt weiter und fügen Sie Logik hinzu, um die Erweiterung von der Arbeit an Seiten außerhalb der [docs.Microsoft.com][MicrosoftDocs] -Domäne zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="036e2-188">Go one step further and add logic to disable the extension from working on pages outside the [docs.microsoft.com][MicrosoftDocs] domain.</span></span>  

<span data-ttu-id="036e2-189">Sie müssen zuerst ein [Inhalts Skript][MDNContentScripts]erstellen.</span><span class="sxs-lookup"><span data-stu-id="036e2-189">You must first create a [content script][MDNContentScripts].</span></span>  <span data-ttu-id="036e2-190">Als nächstes müssen Sie Inhalts Skripts erstellen, die im Kontext einer bestimmten Webseite ausgeführt werden, in der Lage sind, auf den Inhalt einer Webseite zuzugreifen, und die in der Lage sind, mit hintergrundskripts zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="036e2-190">Next, you must create content scripts that run in the context of a particular web page, are able to access the content of a web page, and are able to communicate with background scripts.</span></span>  <span data-ttu-id="036e2-191">Erstellen Sie in Ihrem `js` Verzeichnis eine Datei mit dem Namen, `content.js` und fügen Sie den folgenden Code hinzu.</span><span class="sxs-lookup"><span data-stu-id="036e2-191">Inside of your `js` directory, create a file named `content.js` and add the following code.</span></span>  

```javascript
// get the URL of the page
var url = document.location.href;

// if not on a docs.microsoft.com domain
if (url.indexOf("//docs.microsoft.com") === -1) {
    // send inactive icons
    browser.runtime.sendMessage({
        "iconPath20": "images/inactive20.png",
        "iconPath40": "images/inactive40.png"
    });
}
```  

<span data-ttu-id="036e2-192">Dieses Skript ruft die URL der aktuellen Seite ab `document.location.href` und überprüft, ob sich die aktuelle Seite in der [docs.Microsoft.com][MicrosoftDocs] -Domäne befindet.</span><span class="sxs-lookup"><span data-stu-id="036e2-192">This script gets the URL of the current page through `document.location.href` and verifies whether the current page is on the [docs.microsoft.com][MicrosoftDocs] domain.</span></span>  <span data-ttu-id="036e2-193">Wenn sich die Seite nicht in der [docs.Microsoft.com][MicrosoftDocs] -Domäne befindet \ (beispielsweise  [https://www.bing.com/][|::ref1::|] \), werden die Pfade zu den inaktiven Symbolen \ (abgeblendete Symbole \) mithilfe von [Runtime. SendMessage ()][MDNApiRuntimeSendmessage]an das Hintergrundskript gesendet.</span><span class="sxs-lookup"><span data-stu-id="036e2-193">If the page is not on the [docs.microsoft.com][MicrosoftDocs] domain \(for example  [https://www.bing.com/][|::ref1::|]\), the paths to the inactive icons \(grayed out icons\) are sent to the background script using [runtime.sendMessage()][MDNApiRuntimeSendmessage].</span></span>  

<span data-ttu-id="036e2-194">Sie müssen die [manifest.jsauf][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] Datei aktualisieren, um den folgenden `content_scripts` Schlüssel einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="036e2-194">You must update the [manifest.json][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] file to include the following `content_scripts` key.</span></span>  

```json
  "content_scripts": [{
    "matches": [
        "<all_urls>"
    ],
    "js": ["js/content.js"],
    "run_at": "document_end"
}]
```  

### <span data-ttu-id="036e2-195">Definitionen für manifestschlüssel</span><span class="sxs-lookup"><span data-stu-id="036e2-195">Manifest Key definitions</span></span>  

| <span data-ttu-id="036e2-196">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="036e2-196">Key</span></span> | <span data-ttu-id="036e2-197">Details</span><span class="sxs-lookup"><span data-stu-id="036e2-197">Details</span></span> |  
|:--- |:---- |  
| [<span data-ttu-id="036e2-198">content_scripts</span><span class="sxs-lookup"><span data-stu-id="036e2-198">content_scripts</span></span>][MDNManifestjsonContentScripts] | <span data-ttu-id="036e2-199">Enthält die Informationen dazu, welche Inhalts Skripts vom Browser geladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="036e2-199">Contains the information about which content scripts the browser should load.</span></span> |  

#### <span data-ttu-id="036e2-200">content_scripts Schlüsseldefinitionen</span><span class="sxs-lookup"><span data-stu-id="036e2-200">content_scripts Key definitions</span></span>  

| <span data-ttu-id="036e2-201">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="036e2-201">Key</span></span> | <span data-ttu-id="036e2-202">Details</span><span class="sxs-lookup"><span data-stu-id="036e2-202">Details</span></span> |  
|:--- |:---- |  
| `matches` <span data-ttu-id="036e2-203">\ (erforderlich \)</span><span class="sxs-lookup"><span data-stu-id="036e2-203">\(required\)</span></span> | <span data-ttu-id="036e2-204">Das URL-Muster, das vor dem Laden des Inhalts Skripts übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="036e2-204">The URL pattern to match prior to loading the content script.</span></span> |  
| `js` | <span data-ttu-id="036e2-205">Das Skript, das auf übereinstimmende URLs geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="036e2-205">The script that should be loaded on matching URLs.</span></span> |  
| `run_at` | <span data-ttu-id="036e2-206">Gibt an, wo die JavaScript-Dateien aus dem `js` Schlüssel eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="036e2-206">Specifies where the JavaScript files from the `js` key are injected.</span></span> |  

<span data-ttu-id="036e2-207">Als nächstes müssen Sie ein [Hintergrundskript][MDNAnatomyExtensionBackgroundScripts]erstellen.</span><span class="sxs-lookup"><span data-stu-id="036e2-207">Next, you must create a [background script][MDNAnatomyExtensionBackgroundScripts].</span></span>  <span data-ttu-id="036e2-208">Hintergrundskripts werden im Hintergrund des Browsers ausgeführt, unabhängig von der Lebensdauer einer Webseite oder eines Browserfensters ausgeführt und können mit Inhalts Skripts kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="036e2-208">Background scripts run in the background of the browser, run independently of the lifetime of a web page or browser window, and are able to communicate with content scripts.</span></span>  

<span data-ttu-id="036e2-209">Erstellen Sie innerhalb Ihres `js` Ordners eine Datei mit dem Namen, `background.js` und fügen Sie den folgenden Code hinzu.</span><span class="sxs-lookup"><span data-stu-id="036e2-209">Inside of your `js` folder, create a file named `background.js` and add the following code.</span></span>  

```javascript
// listen for sendMessage() from content script
browser.runtime.onMessage.addListener(
    function (request, sender, sendResponse) {
        // set the icon for the browser action from sendMessage() in content script
        browser.browserAction.setIcon({
            path: {
                "20": request.iconPath20,
                "40": request.iconPath40
            },
            tabId: sender.tab.id
        });
        // disable browser action for the current tab
        browser.browserAction.disable(sender.tab.id);
    });
```  

<span data-ttu-id="036e2-210">Die [Runtime. onMessage][MDNApiRuntimeOnmessage] -Methode wartet auf [Runtime. SendMessage ()][MDNApiRuntimeSendmessage] aus dem Inhalts Skript.</span><span class="sxs-lookup"><span data-stu-id="036e2-210">The [runtime.onMessage][MDNApiRuntimeOnmessage] method listens for [runtime.sendMessage()][MDNApiRuntimeSendmessage] from the content script.</span></span>  <span data-ttu-id="036e2-211">Wenn die Domäne der Seite nicht [docs.Microsoft.com][MicrosoftDocs]ist, legt die [Browser-Methode. SetIcon ()][MDNApiBrowseractionSeticon] -Methode die Symbolpfade auf die inaktiven Bilder fest.</span><span class="sxs-lookup"><span data-stu-id="036e2-211">If the domain of the page is not [docs.microsoft.com][MicrosoftDocs], then [browserAction.setIcon()][MDNApiBrowseractionSeticon] method sets the icon paths to the inactive images.</span></span>  

<span data-ttu-id="036e2-212">Das Skript deaktiviert auch die Browser Aktion \ (BrowserAction[. Disable][MDApiBrowseractionDisable]\), damit Benutzer nicht in der Lage sind, auf die Browser Aktion außerhalb einer [docs.Microsoft.com][MicrosoftDocs] -Seite zu klicken.</span><span class="sxs-lookup"><span data-stu-id="036e2-212">The script also disables the browser action \([browserAction.disable][MDApiBrowseractionDisable]\), so that users are not able to click on the browser action outside of a [docs.microsoft.com][MicrosoftDocs] page.</span></span>  

<span data-ttu-id="036e2-213">Sie müssen das Hintergrundskript zur Datei [manifest.js][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="036e2-213">You must add the background script to the [manifest.json][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] file.</span></span>  <span data-ttu-id="036e2-214">Fügen Sie dem `background` Manifest den folgenden Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="036e2-214">Add the following `background` key to your manifest.</span></span>  

```json
"background": {
    "scripts": ["js/background.js"],
    "persistent": true
  }
```  

### <span data-ttu-id="036e2-215">Definitionen für manifestschlüssel</span><span class="sxs-lookup"><span data-stu-id="036e2-215">Manifest Key definitions</span></span>  

| <span data-ttu-id="036e2-216">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="036e2-216">Key</span></span> | <span data-ttu-id="036e2-217">Details</span><span class="sxs-lookup"><span data-stu-id="036e2-217">Details</span></span>|  
|:--- |:--- |  
| [<span data-ttu-id="036e2-218">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="036e2-218">background</span></span>][MDNManifestjsonBackground] | <span data-ttu-id="036e2-219">Enthält die hintergrundskripts.</span><span class="sxs-lookup"><span data-stu-id="036e2-219">Contains the background scripts.</span></span> |  

#### <span data-ttu-id="036e2-220">Definitionen für den Hintergrund Schlüssel</span><span class="sxs-lookup"><span data-stu-id="036e2-220">background Key definitions</span></span>  

| <span data-ttu-id="036e2-221">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="036e2-221">Key</span></span> | <span data-ttu-id="036e2-222">Details</span><span class="sxs-lookup"><span data-stu-id="036e2-222">Details</span></span> |  
|:--- |:--- |  
| `scripts` | <span data-ttu-id="036e2-223">Der Pfad zu einer JavaScript-Datei.</span><span class="sxs-lookup"><span data-stu-id="036e2-223">The path to a JavaScript file.</span></span> |  
| `persistent` <span data-ttu-id="036e2-224">(erforderlich)</span><span class="sxs-lookup"><span data-stu-id="036e2-224">(required)</span></span> | <span data-ttu-id="036e2-225">Dieser muss auf oder eingestellt `true` sein `false` .</span><span class="sxs-lookup"><span data-stu-id="036e2-225">This must be set to `true` or `false`.</span></span>  <span data-ttu-id="036e2-226">Wenn Sie auf gesetzt `true` ist, wird das Hintergrundskript geladen und für den gesamten Browsing-Abschnitt beibehalten.</span><span class="sxs-lookup"><span data-stu-id="036e2-226">If set to `true`, the background script is loaded and persists for the entire browsing section.</span></span>  <span data-ttu-id="036e2-227">Wenn Sie auf gesetzt `false` ist, wird das Hintergrundskript mit einer Verzögerung geladen und für die Browsersitzung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="036e2-227">If set to `false`, the background script is loaded with a delay and persists for the browsing session.</span></span> |  

<span data-ttu-id="036e2-228">Laden Sie Ihre Erweiterung erneut, und testen Sie Sie erneut.</span><span class="sxs-lookup"><span data-stu-id="036e2-228">Reload your extension and test again.</span></span>  <span data-ttu-id="036e2-229">So laden Sie Ihre Erweiterung erneut: Klicken Sie auf die **Optionen für Einstellungen** und mehr in Microsoft Edge, klicken Sie auf **Erweiterungen**, klicken Sie auf Ihre Durchwahl \ (**Farbwechsler**\), und klicken Sie auf **Erweiterung erneut laden**.</span><span class="sxs-lookup"><span data-stu-id="036e2-229">To reload your extension: click the **...** for settings and more in Microsoft Edge, click **Extensions**, click on your extension \(**Color Changer**\), and click **Reload extension**.</span></span>  

<span data-ttu-id="036e2-230">Öffnen Sie nun eine neue Registerkarte, oder aktualisieren Sie eine vorhandene Registerkarte, bei der es sich nicht um eine [docs.Microsoft.com][MicrosoftDocs] -Seite handelt.</span><span class="sxs-lookup"><span data-stu-id="036e2-230">Now, open a new tab or refresh an existing tab that is not a [docs.microsoft.com][MicrosoftDocs] page.</span></span>  <span data-ttu-id="036e2-231">Sie sollten das Symbol inaktiv sehen und nicht auf die Browser Aktion klicken können.</span><span class="sxs-lookup"><span data-stu-id="036e2-231">You should see the inactive icon and not be able to click on the browser action.</span></span>  

<span data-ttu-id="036e2-232">Herzlichen Glückwunsch!</span><span class="sxs-lookup"><span data-stu-id="036e2-232">Congratulations!</span></span>  <span data-ttu-id="036e2-233">Sie haben eine Erweiterung für Microsoft Edge erstellt!</span><span class="sxs-lookup"><span data-stu-id="036e2-233">You created an extension for Microsoft Edge!</span></span>  <span data-ttu-id="036e2-234">Sehen Sie [sich das vollständige Beispiel auf GitHub an][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span><span class="sxs-lookup"><span data-stu-id="036e2-234">View the [full sample on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span></span>  <span data-ttu-id="036e2-235">Lesen Sie weiter, um mehr über Erweiterungen zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="036e2-235">Continue reading to learn more about extensions.</span></span>  

## <span data-ttu-id="036e2-236">Schreiben einer komplexeren Erweiterung</span><span class="sxs-lookup"><span data-stu-id="036e2-236">Writing a more complex extension</span></span>  

<span data-ttu-id="036e2-237">Möchten Sie eine komplexere Erweiterung erstellen?</span><span class="sxs-lookup"><span data-stu-id="036e2-237">Want to write a more complex extension?</span></span>  <span data-ttu-id="036e2-238">Sehen Sie sich die Beastify-Erweiterung auf MDN im Artikel, [ihrer zweiten Erweiterung][MDNYourSecondWebextension], an.</span><span class="sxs-lookup"><span data-stu-id="036e2-238">Take a look at the Beastify extension on MDN in the article, [Your second extension][MDNYourSecondWebextension].</span></span>  <span data-ttu-id="036e2-239">Das Erweiterungsmodell für Microsoft Edge weicht etwas vom Erweiterungsmodell für Firefox ab, die in [ihrer zweiten Erweiterung][MDNYourSecondWebextension] erstellte Beastify-Erweiterung wurde an die Funktion in Microsoft Edge angepasst.</span><span class="sxs-lookup"><span data-stu-id="036e2-239">The extension model for Microsoft Edge differs slightly from the extension model for Firefox, the Beastify extension created in [Your second extension][MDNYourSecondWebextension] was adapted to function in Microsoft Edge.</span></span>  <span data-ttu-id="036e2-240">Überprüfen Sie es auf [GitHub][GithubMicrosoftEdgeExtensionsDemosBeastify].</span><span class="sxs-lookup"><span data-stu-id="036e2-240">Check it out on [GitHub][GithubMicrosoftEdgeExtensionsDemosBeastify].</span></span>  

<span data-ttu-id="036e2-241">Beachten Sie beim Durchlaufen des Artikels zu MDN, [ihrer zweiten Erweiterung][MDNYourSecondWebextension], die folgenden Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="036e2-241">While walking through the article on MDN, [Your second extension][MDNYourSecondWebextension], keep in mind the following sections.</span></span>  

### <span data-ttu-id="036e2-242">APIs</span><span class="sxs-lookup"><span data-stu-id="036e2-242">APIs</span></span>  

<span data-ttu-id="036e2-243">Eine Liste der unterstützten Erweiterungen-APIs in Microsoft Edge finden Sie auf der Seite [unterstützte APIs][ExtensionsAPIsupportApis] .</span><span class="sxs-lookup"><span data-stu-id="036e2-243">See the [Supported APIs][ExtensionsAPIsupportApis] page for a list of supported extensions APIs in Microsoft Edge.</span></span>  

### <span data-ttu-id="036e2-244">Symbolgrößen</span><span class="sxs-lookup"><span data-stu-id="036e2-244">Icon sizes</span></span>  

<span data-ttu-id="036e2-245">Die bevorzugten Erweiterungssymbol Größen für Microsoft Edge sind,, `20px` `25px` `30px` und `40px` .</span><span class="sxs-lookup"><span data-stu-id="036e2-245">Preferred extension icon sizes for Microsoft Edge are `20px`, `25px`, `30px`, and `40px`.</span></span>  <span data-ttu-id="036e2-246">Weitere unterstützte Größen sind `19px` , `35px` und `38px` .</span><span class="sxs-lookup"><span data-stu-id="036e2-246">Other supported sizes are `19px`, `35px`, and `38px`.</span></span>  <span data-ttu-id="036e2-247">Weitere Informationen zu Symbolgrößen und bewährten Methoden finden Sie im [Design][ExtensionsGuidesDesign] Handbuch.</span><span class="sxs-lookup"><span data-stu-id="036e2-247">For more info on icon sizes and best practices, see the [Design][ExtensionsGuidesDesign] guide.</span></span>  

### <span data-ttu-id="036e2-248">JavaScript</span><span class="sxs-lookup"><span data-stu-id="036e2-248">JavaScript</span></span>  

<span data-ttu-id="036e2-249">Das Erweiterungsmodell für Microsoft Edge unterstützt keine JavaScript-Versprechungen.</span><span class="sxs-lookup"><span data-stu-id="036e2-249">The extension model for Microsoft Edge does not support JavaScript Promises.</span></span>  <span data-ttu-id="036e2-250">Verwenden Sie stattdessen Rückrufe.</span><span class="sxs-lookup"><span data-stu-id="036e2-250">Instead, use callbacks.</span></span>  <span data-ttu-id="036e2-251">Weitere Beispiele für die Verwendung von Rückrufen in einer Erweiterung finden Sie in den Demos zu  [Schnelldruck][GithubMicrosoftEdgeExtensionsDemosQuickPrint] und [Text Austausch][GithubMicrosoftEdgeExtensionsDemosTextSwap] .</span><span class="sxs-lookup"><span data-stu-id="036e2-251">For more examples of using callbacks in an extension, take a look at the  [Quick Print][GithubMicrosoftEdgeExtensionsDemosQuickPrint] and [Text Swap][GithubMicrosoftEdgeExtensionsDemosTextSwap] demos.</span></span>  

<span data-ttu-id="036e2-252">Navigieren Sie im folgenden Video zum [Schnelldruck][GithubMicrosoftEdgeExtensionsDemosQuickPrint] -Beispiel.</span><span class="sxs-lookup"><span data-stu-id="036e2-252">Walk through the [Quick Print][GithubMicrosoftEdgeExtensionsDemosQuickPrint] example in the following video.</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Adding-a-Background-Script-to-you-Edge-Extension/player]  

### <span data-ttu-id="036e2-253">Manifest.jsein</span><span class="sxs-lookup"><span data-stu-id="036e2-253">Manifest.json</span></span>  

*   <span data-ttu-id="036e2-254">Der `author` Schlüssel ist in Microsoft Edge erforderlich.</span><span class="sxs-lookup"><span data-stu-id="036e2-254">The `author` key is required in Microsoft Edge</span></span>  
*   <span data-ttu-id="036e2-255">Der `activeTab` Schlüssel wird in Microsoft Edge nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="036e2-255">The `activeTab` key is not supported in Microsoft Edge</span></span>  

<span data-ttu-id="036e2-256">Weitere Informationen zu [Browser Erweiterungen][MDNBrowserExtensions]finden Sie unter [MDN Web docs][MDNWebDocs].</span><span class="sxs-lookup"><span data-stu-id="036e2-256">For more information on [Browser Extensions][MDNBrowserExtensions], see [MDN web docs][MDNWebDocs].</span></span>  

<!-- image links -->  

<!--[ImageColorChangerHeader]: ../media/color-changer_header.png "Docs.microsoft.com body changed to blue"  -->  
<!--[ImageColorChangerPopup]: ../media/color-changer_popup.png "The pop-up interface of the extension"  -->  
<!--[ImageColorChangerHeaderAliceblue]: ../media/color-changer_header_aliceblue.png "[Docs.microsoft.com header changed to Aliceblue"  -->  
<!--[ImageColorChangerHeaderCornsilk]: ../media/color-changer_header_cornsilk.png "Docs.microsoft.com header changed to Cornsilk"  -->  

<!-- links -->  

[ExtensionsGuidesAddingRemovingExtensionsAdding]: ./adding-and-removing-extensions.md#adding-an-extension "Hinzufügen einer Erweiterung – hinzufügen, verschieben und Entfernen von Erweiterungen für Microsoft Edge | Microsoft docs"  
[ExtensionsGuidesDebuggingExtensions]: ./debugging-extensions.md "Debugging-Erweiterungen | Microsoft docs"  
[ExtensionsGuidesDesign]: ./design.md "Entwurfsrichtlinien für Microsoft Edge-Erweiterungen | Microsoft docs"  
[ExtensionsGuidesDesignIcons]: ./design.md#icons "Symbole – Entwurfsrichtlinien für Microsoft Edge-Erweiterungen | Microsoft docs"  
[ExtensionsAPIsupportApis]: ../api-support/supported-apis.md " Unterstützte APIs | Microsoft docs"  
[ExtensionsApisupportManifestKeys]: ../api-support/supported-manifest-keys.md "Unterstützte manifestschlüssel | Microsoft docs"  

[MicrosoftDocs]: https://docs.microsoft.com "Microsoft docs"  

[MDNWebDocs]: https://developer.mozilla.org "MDN Web docs"  
[MDNBrowserExtensions]: https://developer.mozilla.org/Add-ons/WebExtensions "Browser-Erweiterungen | MDN"  
[MDNAnatomyExtension]: https://developer.mozilla.org/Add-ons/WebExtensions/Anatomy_of_a_WebExtension "Anatomie einer Erweiterung | MDN"  
[MDNAnatomyExtensionBackgroundScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Anatomy_of_a_WebExtension#Background_scripts "Hintergrundskripts – Anatomie einer Erweiterung | MDN"  
[MDApiBrowseractionDisable]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/disable "Browser-Funktion. Disable ()-API | MDN" 
[MDNApiBrowseractionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setIcon "BrowserControl. SetIcon ()-API | MDN"  
[MDNApiRuntimeOnmessage]: https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/onmessage "Runtime. onMessage-API | MDN"  
[MDNApiRuntimeSendmessage]: https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendMessage "Runtime. SendMessage ()-API | MDN"  
[MDNApiTabs]: https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs "Registerkarten-API | MDN"  
[MDNApiTabsInsertcss]: https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs/insertCSS "Tabs. insertCSS ()-API | MDN"  
[MDNContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Content_scripts "Inhalts Skripts | MDN"  
[MDNManifestjsonAuthor]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/author "Autor-manifest.jsauf | MDN"  
[MDNManifestjsonBackground]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/background "Background-manifest.jsauf | MDN"  
[MDNManifestjsonBrowserAction]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/browser_action "browser_action-manifest.js| MDN"  
[MDNManifestjsonContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/content_scripts "content_scripts-manifest.js| MDN"  
[MDNManifestjsonDescription]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/description "Beschreibung-manifest.jsauf | MDN"  
[MDNManifestjsonIcons]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/icons "Symbole – manifest.jsauf | MDN"  
[MDNManifestjsonName]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/name "Name-manifest.jsauf | MDN"  
[MDNManifestjsonPermissions]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/permissions "Berechtigungen – manifest.jsauf | MDN"  
[MDNManifestjsonVersion]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/version "Version-manifest.jsauf | MDN"  
[MDNYourSecondWebextension]: https://developer.mozilla.org/Add-ons/WebExtensions/Your_second_WebExtension "Ihre zweite Durchwahl | MDN"  

[Bing]: https://www.bing.com "Bing"  

[GithubMicrosoftEdgeExtensionsDemosBeastify]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/beastify_edge "Beastify-MicrosoftEdge/MicrosoftEdge-Extensions-Demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChanger]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/color_changer "Farbwechsler-MicrosoftEdge/MicrosoftEdge-Extensions-Demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChangerImages]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/color_changer/images "Bilder-Farbwechsler-MicrosoftEdge/MicrosoftEdge-Extensions-Demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/color_changer/manifest.json "Manifest.json-Color Changer-MicrosoftEdge/MicrosoftEdge-Extensions-Demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosQuickPrint]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/quick_print "Schnelldruck-MicrosoftEdge/MicrosoftEdge-Erweiterungen-Demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosTextSwap]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/text_swap "Text Austausch-MicrosoftEdge/MicrosoftEdge-Extensions-Demos | GitHub"  
