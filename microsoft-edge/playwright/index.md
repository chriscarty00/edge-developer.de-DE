---
description: Verwenden von Playwright zum Automatisieren und Testen in Microsoft Edge
title: Dramatiker
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/24/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, web development, developer, tools, automation, test, playwright, node, javascript, npm
ms.openlocfilehash: 5ce51864177731dd1bafb845466abb00cce1e0aa
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231083"
---
# <span data-ttu-id="70bb3-104">Dramatiker</span><span class="sxs-lookup"><span data-stu-id="70bb3-104">Playwright</span></span>  

<span data-ttu-id="70bb3-105">[Playwright][|::ref1::|Main] ist [eine][NodejsMain]Node.js, um Chromium [,][ChromiumHome] [Firefox][FirefoxMain]und [WebKit][|::ref2::|Main] mit einer einzigen API zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="70bb3-105">[Playwright][|::ref1::|Main] is a [Node.js][NodejsMain] library to automate [Chromium][ChromiumHome], [Firefox][FirefoxMain], and [WebKit][|::ref2::|Main] with a single API.</span></span>  <span data-ttu-id="70bb3-106">Playwright wurde entwickelt, um browserübergreifende Webautomatisierung zu ermöglichen, die immer grün, fähig, zuverlässig und schnell ist.</span><span class="sxs-lookup"><span data-stu-id="70bb3-106">Playwright is built to enable cross-browser web automation that is ever-green, capable, reliable, and fast.</span></span>  <span data-ttu-id="70bb3-107">Da [Microsoft Edge auf der Open-Source-Chromium-Webplattform][MicrosoftBlogsWindowsExperience20181206]aufgebaut ist, kann Playwright auch Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="70bb3-107">Since [Microsoft Edge is built on the open-source Chromium web platform][MicrosoftBlogsWindowsExperience20181206], Playwright is also able to automate Microsoft Edge.</span></span>  

<span data-ttu-id="70bb3-108">Playwright startet [standardmäßig browserlose][WikiHeadlessBrowser] Browser.</span><span class="sxs-lookup"><span data-stu-id="70bb3-108">Playwright launches [headless browsers][WikiHeadlessBrowser] by default.</span></span>  <span data-ttu-id="70bb3-109">Headless-Browser zeigen keine Benutzeroberfläche an, daher müssen Sie stattdessen die Befehlszeile verwenden.</span><span class="sxs-lookup"><span data-stu-id="70bb3-109">Headless browsers do not display a UI, so instead you must use the command line.</span></span>  <span data-ttu-id="70bb3-110">Sie können Playwright auch so konfigurieren, dass vollständige \(nicht kopflose\) Microsoft Edge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="70bb3-110">You may also configure Playwright to run full \(non-headless\) Microsoft Edge as well.</span></span>  

<span data-ttu-id="70bb3-111">Bei der Installation von Playwright lädt das Installationsprogramm standardmäßig [Chromium][ChromiumHome], [Firefox][FirefoxMain]und [WebKit herunter.][|::ref3::|Main]</span><span class="sxs-lookup"><span data-stu-id="70bb3-111">By default, when you install Playwright, the installer downloads [Chromium][ChromiumHome], [Firefox][FirefoxMain], and [WebKit][|::ref3::|Main].</span></span>  <span data-ttu-id="70bb3-112">Wenn Sie auch Microsoft Edge \(Chromium\) installiert haben, benötigt Playwright nur eine einz nen Codeänderung, um Ihre Website oder App in Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="70bb3-112">If you have Microsoft Edge \(Chromium\) installed as well, Playwright just needs a one-line code change to test your website or app in Microsoft Edge.</span></span>  <span data-ttu-id="70bb3-113">Um Microsoft Edge \(Chromium\) herunterzuladen, navigieren Sie zu [Download Microsoft Edge][MicrosoftEdgeDownload].</span><span class="sxs-lookup"><span data-stu-id="70bb3-113">To download Microsoft Edge \(Chromium\), navigate to [Download Microsoft Edge][MicrosoftEdgeDownload].</span></span>  

## <span data-ttu-id="70bb3-114">Installieren von Playwright</span><span class="sxs-lookup"><span data-stu-id="70bb3-114">Installing Playwright</span></span>  

<span data-ttu-id="70bb3-115">Installieren [Sie Playwright,][|::ref4::|Main] um Ihre Website oder App mit dem folgenden Befehl zu testen.</span><span class="sxs-lookup"><span data-stu-id="70bb3-115">Install [Playwright][|::ref4::|Main] to test your website or app with the following command.</span></span>  

```shell
npm i playwright
```  

## <span data-ttu-id="70bb3-116">Starten Microsoft Edge mit Playwright</span><span class="sxs-lookup"><span data-stu-id="70bb3-116">Launch Microsoft Edge with Playwright</span></span>  

> [!NOTE]
> <span data-ttu-id="70bb3-117">[Playwright][|::ref5::|Main] erfordert Node.js Version 10.17 oder höher.</span><span class="sxs-lookup"><span data-stu-id="70bb3-117">[Playwright][|::ref5::|Main] requires Node.js version 10.17 or above.</span></span> <span data-ttu-id="70bb3-118">Führen `node -v` Sie über die Befehlszeile aus, um sicherzustellen, dass Sie über eine kompatible Version von Node.js.</span><span class="sxs-lookup"><span data-stu-id="70bb3-118">Run `node -v` from the command line to ensure you have a compatible version of Node.js.</span></span>  <span data-ttu-id="70bb3-119">Die Browser-Binärdateien für Chromium, Firefox und WebKit funktionieren Windows, macOS und Linux.</span><span class="sxs-lookup"><span data-stu-id="70bb3-119">The browser binaries for Chromium, Firefox and WebKit work across Windows, macOS, and Linux.</span></span> <span data-ttu-id="70bb3-120">Weitere Informationen finden Sie unter [Playwright System Requirements][PlaywrightSystemRequirements].</span><span class="sxs-lookup"><span data-stu-id="70bb3-120">For more information, navigate to [Playwright System Requirements][PlaywrightSystemRequirements].</span></span>  

<span data-ttu-id="70bb3-121">Playwright sollte Benutzern anderer Browsertestframeworks wie [WebDriver][WebDriverChromiumMain] oder [Puppeteer vertraut sein.][PuppeteerMain]</span><span class="sxs-lookup"><span data-stu-id="70bb3-121">Playwright should be familiar to users of other browser-testing frameworks like [WebDriver][WebDriverChromiumMain] or [Puppeteer][PuppeteerMain].</span></span>  <span data-ttu-id="70bb3-122">Sie erstellen eine Instanz des Browsers, öffnen eine Seite und bearbeiten sie dann mit der [Playwright-API.][PlaywrightAPIReference]</span><span class="sxs-lookup"><span data-stu-id="70bb3-122">You create an instance of the browser, open a page, and then manipulate it with the [Playwright API][PlaywrightAPIReference].</span></span>  <span data-ttu-id="70bb3-123">Im folgenden Codeausschnitt startet Playwright Microsoft Edge \(Chromium\), navigiert zu und speichert `https://www.microsoft.com/edge` einen Screenshot als `example.png` .</span><span class="sxs-lookup"><span data-stu-id="70bb3-123">In the following code snippet, Playwright launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoft.com/edge`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="70bb3-124">Kopieren Sie den folgenden Codeausschnitt, und speichern Sie ihn unter `example.js` .</span><span class="sxs-lookup"><span data-stu-id="70bb3-124">Copy the following code snippet and save it as `example.js`.</span></span>  

```javascript
const { chromium } = require('playwright');

(async () => {
  const browser = await chromium.launch({
    executablePath: 'C:\\Program Files (x86)\\Microsoft\\Edge Dev\\Application\\msedge.exe'
  });
  const page = await browser.newPage();
  await page.goto('https://www.microsoft.com/edge');
  await page.screenshot({path: 'example.png'});

  await browser.close();
})();
```  

<span data-ttu-id="70bb3-125">Ändern `executablePath` Sie, um auf Ihre Installation von Microsoft Edge \(Chromium\) zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="70bb3-125">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="70bb3-126">Unter macOS sollte beispielsweise der für `executablePath` Microsoft Edge Canary auf festgelegt `/Applications/Microsoft\ Edge\ Canary.app/` werden.</span><span class="sxs-lookup"><span data-stu-id="70bb3-126">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="70bb3-127">Navigieren Sie zu und kopieren Sie den ausführbaren Pfad auf dieser Seite, oder installieren Sie das `executablePath` `edge://version` [Edge-Paths-Paket][npmEdgePaths] mit dem folgenden Befehl. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="70bb3-127">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with the following command.</span></span>  

```shell
npm i edge-paths
```  

<span data-ttu-id="70bb3-128">Der folgende Codeausschnitt verwendet das [Edge-Paths-Paket,][npmEdgePaths] um programmgesteuert den Pfad zu Ihrer Installation von Microsoft Edge \(Chromium\) auf Ihrem Betriebssystem zu finden.</span><span class="sxs-lookup"><span data-stu-id="70bb3-128">The following code snippet uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>  

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```  

<span data-ttu-id="70bb3-129">Legen Sie schließlich `executablePath: EDGE_PATH` in . `example.js`</span><span class="sxs-lookup"><span data-stu-id="70bb3-129">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="70bb3-130">Speichern Sie Ihre Änderungen.</span><span class="sxs-lookup"><span data-stu-id="70bb3-130">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="70bb3-131">Microsoft Edge \(EdgeHTML\) funktioniert nicht mit Playwright.</span><span class="sxs-lookup"><span data-stu-id="70bb3-131">Microsoft Edge \(EdgeHTML\) does not work with Playwright.</span></span>  <span data-ttu-id="70bb3-132">Sie müssen die [Microsoft Edge \(Chromium\)][MicrosoftEdgeDownload] installieren, um dieses Beispiel weiter zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="70bb3-132">You must install [Microsoft Edge \(Chromium\)][MicrosoftEdgeDownload] to continue following this example.</span></span>  

<span data-ttu-id="70bb3-133">Führen Sie `example.js` jetzt über die Befehlszeile aus.</span><span class="sxs-lookup"><span data-stu-id="70bb3-133">Now run `example.js` from the command line.</span></span>  

```shell
node example.js
```  

<span data-ttu-id="70bb3-134">Playwright startet Microsoft Edge, navigiert zu `https://www.microsoft.com/edge` und speichert einen Screenshot der Seite.</span><span class="sxs-lookup"><span data-stu-id="70bb3-134">Playwright launches Microsoft Edge, navigates to `https://www.microsoft.com/edge`, and saves a screenshot of the page.</span></span>  <span data-ttu-id="70bb3-135">Sie können die Seitengröße mit [page.setViewportSize() anpassen.][PlaywrightAPIPageSetViewport]</span><span class="sxs-lookup"><span data-stu-id="70bb3-135">You may customize the page size with [page.setViewportSize()][PlaywrightAPIPageSetViewport].</span></span>  

:::image type="complex" source="../media/playwright-example.png" alt-text="Die example.png datei, die von example.js" lightbox="../media/playwright-example.png":::
    <span data-ttu-id="70bb3-137">Die `example.png` datei, die von</span><span class="sxs-lookup"><span data-stu-id="70bb3-137">The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

`example.js` <span data-ttu-id="70bb3-138">ist nur eine einfache Demonstration der von Playwright aktivierten Automatisierungs- und Testszenarien.</span><span class="sxs-lookup"><span data-stu-id="70bb3-138">is just a simple demonstration of the automation and testing scenarios enabled by Playwright.</span></span>  <span data-ttu-id="70bb3-139">Um Screenshots in mehreren Webbrowsern zu erstellen, ändern Sie den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="70bb3-139">To take screenshots in multiple web browsers, change the following code.</span></span>  

*   <span data-ttu-id="70bb3-140">Chromium</span><span class="sxs-lookup"><span data-stu-id="70bb3-140">Chromium</span></span>  `await chromium.launch()`  
*   <span data-ttu-id="70bb3-141">Firefox</span><span class="sxs-lookup"><span data-stu-id="70bb3-141">Firefox</span></span>  `await firefox.launch()`  
*   <span data-ttu-id="70bb3-142">WebKit</span><span class="sxs-lookup"><span data-stu-id="70bb3-142">WebKit</span></span>  `await webkit.launch()`  

<span data-ttu-id="70bb3-143">Weitere Informationen zu Playwright finden Sie auf der [Playwright-Website.][|::ref6::|Main]</span><span class="sxs-lookup"><span data-stu-id="70bb3-143">For more information about Playwright, navigate to the [Playwright website][|::ref6::|Main].</span></span>  <span data-ttu-id="70bb3-144">Sehen Sie sich [das Playwright-Repository auf GitHub.][PlaywrightRepo]</span><span class="sxs-lookup"><span data-stu-id="70bb3-144">Check out the  [Playwright repo][PlaywrightRepo] on GitHub.</span></span>  <span data-ttu-id="70bb3-145">Um Ihr Feedback zum Automatisieren und Testen Ihrer Website oder App mit Playwright zu teilen, geben Sie [ein Problem ein.][PlaywrightRepoNewIssue]</span><span class="sxs-lookup"><span data-stu-id="70bb3-145">To share your feedback on automating and testing your website or app with Playwright, [file an issue][PlaywrightRepoNewIssue].</span></span>  

## <span data-ttu-id="70bb3-146">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="70bb3-146">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../devtools-guide-chromium/includes/contact-devtools-team-note.md)]  

<!-- links -->  

[WebdriverChromiumMain]: ../webdriver-chromium/index.md "WebDriver (Chromium) | Microsoft Docs"  
[PuppeteerMain]: ../puppeteer/index.md "| Microsoft Docs"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: Verbessern des Webs durch mehr Open-Source-Zusammenarbeit | Microsoft Experience Blog"  

[MicrosoftEdgeDownload]: https://microsoft.com/edge "Download Microsoft Edge"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium | Die Chromium Projekte"  

[FirefoxMain]: https://www.mozilla.org/firefox "Mozilla Firefox"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "edge-paths | npm"  

[PlaywrightMain]: https://playwright.dev "Playwright"  
[PlaywrightAPIReference]: https://playwright.dev#?path=docs/api.md "Playwright-API-Referenz"  
[PlaywrightAPIPageSetViewport]: https://playwright.dev#?path=docs%2Fapi.md&q=pagesetviewportsizeviewportsize "page.setViewportSize(viewportSize) | Playwright-API-Referenz"    
[PlaywrightSystemRequirements]: https://playwright.dev#?path=docs/intro.md&q=system-requirements "Playwright System Requirements"  

[PlaywrightRepo]: https://github.com/microsoft/playwright "Playwright | GitHub"  
[PlaywrightRepoNewIssue]: https://github.com/microsoft/playwright/issues/new/choose "Neues Problem im Playwright-Repository | GitHub"  

[WebKitMain]: https://webkit.org "WebKit"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Monitorlose Browser-| Wikipedia"  
