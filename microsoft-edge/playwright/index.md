---
description: Verwenden von Dramatiker zum Automatisieren und testen in Microsoft Edge
title: Dramatiker
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/24/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Web-Entwicklung, Entwickler, Tools, Automatisierung, Test, Dramatiker, Knoten, JavaScript, NPM
ms.openlocfilehash: ac03923fb25da00f07cb70e81ac06b106a6e1452
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "11192212"
---
# <span data-ttu-id="e0e2b-104">Dramatiker</span><span class="sxs-lookup"><span data-stu-id="e0e2b-104">Playwright</span></span>  

<span data-ttu-id="e0e2b-105">[Dramatiker][|::ref1::|Main] ist eine [Node.js][NodejsMain] Bibliothek zum Automatisieren von [Chrom][ChromiumHome], [Firefox][FirefoxMain]und [WebKit][|::ref2::|Main] mit einer einzigen API.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-105">[Playwright][|::ref1::|Main] is a [Node.js][NodejsMain] library to automate [Chromium][ChromiumHome], [Firefox][FirefoxMain], and [WebKit][|::ref2::|Main] with a single API.</span></span>  <span data-ttu-id="e0e2b-106">Dramatiker wurde entwickelt, um browserübergreifende webautomatisierungen zu ermöglichen, die immer grün, fähig, zuverlässig und schnell sind.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-106">Playwright is built to enable cross-browser web automation that is ever-green, capable, reliable, and fast.</span></span>  <span data-ttu-id="e0e2b-107">Da [Microsoft Edge auf der Open-Source-Chrom-Webplattform][MicrosoftBlogsWindowsExperience20181206]basiert, ist Dramatiker auch in der Lage, Microsoft Edge zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-107">Since [Microsoft Edge is built on the open-source Chromium web platform][MicrosoftBlogsWindowsExperience20181206], Playwright is also able to automate Microsoft Edge.</span></span>  

<span data-ttu-id="e0e2b-108">Writer startet standardmäßig [headless-Browser][WikiHeadlessBrowser] .</span><span class="sxs-lookup"><span data-stu-id="e0e2b-108">Playwright launches [headless browsers][WikiHeadlessBrowser] by default.</span></span>  <span data-ttu-id="e0e2b-109">Headless-Browser zeigen keine Benutzeroberfläche an, daher müssen Sie stattdessen die Befehlszeile verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-109">Headless browsers do not display a UI, so instead you must use the command line.</span></span>  <span data-ttu-id="e0e2b-110">Sie können auch Writer so konfigurieren, dass der vollständige \ (nicht-headless \) Microsoft Edge ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-110">You may also configure Playwright to run full \(non-headless\) Microsoft Edge as well.</span></span>  

<span data-ttu-id="e0e2b-111">Wenn Sie Writer installieren, downloadet das Installationsprogramm standardmäßig [Chrom][ChromiumHome], [Firefox][FirefoxMain]und [WebKit][|::ref3::|Main].</span><span class="sxs-lookup"><span data-stu-id="e0e2b-111">By default, when you install Playwright, the installer downloads [Chromium][ChromiumHome], [Firefox][FirefoxMain], and [WebKit][|::ref3::|Main].</span></span>  <span data-ttu-id="e0e2b-112">Wenn Sie Microsoft Edge \ (Chrom \) ebenfalls installiert haben, benötigt Dramatiker nur eine einzeilige Codeänderung, um Ihre Website oder app in Microsoft Edge zu testen.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-112">If you have Microsoft Edge \(Chromium\) installed as well, Playwright just needs a one-line code change to test your website or app in Microsoft Edge.</span></span>  <span data-ttu-id="e0e2b-113">Zum Herunterladen von Microsoft Edge \ (Chrom \) navigieren Sie zu [Microsoft Edge herunterladen][MicrosoftEdgeDownload].</span><span class="sxs-lookup"><span data-stu-id="e0e2b-113">To download Microsoft Edge \(Chromium\), navigate to [Download Microsoft Edge][MicrosoftEdgeDownload].</span></span>  

## <span data-ttu-id="e0e2b-114">Installieren des Dramatikers</span><span class="sxs-lookup"><span data-stu-id="e0e2b-114">Installing Playwright</span></span>  

<span data-ttu-id="e0e2b-115">Installieren Sie [Dramatiker][|::ref4::|Main] , um Ihre Website oder App mit dem folgenden Befehl zu testen.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-115">Install [Playwright][|::ref4::|Main] to test your website or app with the following command.</span></span>  

```shell
npm i playwright
```  

## <span data-ttu-id="e0e2b-116">Starten von Microsoft Edge mit Dramatiker</span><span class="sxs-lookup"><span data-stu-id="e0e2b-116">Launch Microsoft Edge with Playwright</span></span>  

> [!NOTE]
> <span data-ttu-id="e0e2b-117">Für [Dramatiker][|::ref5::|Main] ist Node.js Version 10,17 oder höher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-117">[Playwright][|::ref5::|Main] requires Node.js version 10.17 or above.</span></span> <span data-ttu-id="e0e2b-118">Führen `node -v` Sie über die Befehlszeile aus, um sicherzustellen, dass Sie über eine kompatible Version von Node.js verfügen.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-118">Run `node -v` from the command line to ensure you have a compatible version of Node.js.</span></span>  <span data-ttu-id="e0e2b-119">Die Browser-Binaries für Chrom, Firefox und WebKit funktionieren über Windows, macOS und Linux.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-119">The browser binaries for Chromium, Firefox and WebKit work across Windows, macOS, and Linux.</span></span> <span data-ttu-id="e0e2b-120">Weitere Informationen finden Sie unter [System Anforderungen für Dramatiker][PlaywrightSystemRequirements].</span><span class="sxs-lookup"><span data-stu-id="e0e2b-120">For more information, navigate to [Playwright System Requirements][PlaywrightSystemRequirements].</span></span>  

<span data-ttu-id="e0e2b-121">Dramatiker sollten Benutzern anderer Browsertest-Frameworks wie [WebDriver][WebDriverChromiumMain] oder [Puppenspieler][PuppeteerMain]vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-121">Playwright should be familiar to users of other browser-testing frameworks like [WebDriver][WebDriverChromiumMain] or [Puppeteer][PuppeteerMain].</span></span>  <span data-ttu-id="e0e2b-122">Erstellen Sie eine Instanz des Browsers, öffnen Sie eine Seite, und bearbeiten Sie Sie dann mit der [Dramatiker-API][PlaywrightAPIReference].</span><span class="sxs-lookup"><span data-stu-id="e0e2b-122">You create an instance of the browser, open a page, and then manipulate it with the [Playwright API][PlaywrightAPIReference].</span></span>  <span data-ttu-id="e0e2b-123">Im folgenden Codeausschnitt startet Dramatiker Microsoft Edge \ (Chrom \), navigiert zu `https://www.microsoft.com/edge` und speichert einen Screenshot als `example.png` .</span><span class="sxs-lookup"><span data-stu-id="e0e2b-123">In the following code snippet, Playwright launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoft.com/edge`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="e0e2b-124">Kopieren Sie den folgenden Codeausschnitt, und speichern Sie ihn als `example.js` .</span><span class="sxs-lookup"><span data-stu-id="e0e2b-124">Copy the following code snippet and save it as `example.js`.</span></span>  

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

<span data-ttu-id="e0e2b-125">Ändern `executablePath` Sie, um auf Ihre Installation von Microsoft Edge (Chrom \) zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-125">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="e0e2b-126">So sollte beispielsweise unter macOS `executablePath` für Microsoft Edge Canary auf festgesetzt werden `/Applications/Microsoft\ Edge\ Canary.app/` .</span><span class="sxs-lookup"><span data-stu-id="e0e2b-126">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="e0e2b-127">Um das zu finden `executablePath` , navigieren Sie zu dem `edge://version` **ausführbaren Pfad** auf dieser Seite, und kopieren Sie ihn, oder installieren Sie das [Edge-Paths-][npmEdgePaths] Paket mit dem folgenden Befehl.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-127">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with the following command.</span></span>  

```shell
npm i edge-paths
```  

<span data-ttu-id="e0e2b-128">Der folgende Codeausschnitt verwendet das [Edge-Paths-][npmEdgePaths] Paket zum programmgesteuerten Auffinden des Pfads zu Ihrer Installation von Microsoft Edge \ (Chrom \) auf Ihrem Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-128">The following code snippet uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>  

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```  

<span data-ttu-id="e0e2b-129">Setzen Sie abschließend `executablePath: EDGE_PATH` ein `example.js` .</span><span class="sxs-lookup"><span data-stu-id="e0e2b-129">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="e0e2b-130">Speichern Sie Ihre Änderungen.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-130">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="e0e2b-131">Microsoft Edge \ (EdgeHTML \) funktioniert nicht mit Dramatiker.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-131">Microsoft Edge \(EdgeHTML\) does not work with Playwright.</span></span>  <span data-ttu-id="e0e2b-132">Sie müssen [Microsoft Edge \ (Chrom \)][MicrosoftEdgeDownload] installieren, um weiterhin diesem Beispiel folgen zu können.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-132">You must install [Microsoft Edge \(Chromium\)][MicrosoftEdgeDownload] to continue following this example.</span></span>  

<span data-ttu-id="e0e2b-133">Nun `example.js` über die Befehlszeile ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-133">Now run `example.js` from the command line.</span></span>  

```shell
node example.js
```  

<span data-ttu-id="e0e2b-134">Dramatiker startet Microsoft Edge, navigiert zu `https://www.microsoft.com/edge` und speichert einen Screenshot der Seite.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-134">Playwright launches Microsoft Edge, navigates to `https://www.microsoft.com/edge`, and saves a screenshot of the page.</span></span>  <span data-ttu-id="e0e2b-135">Sie können die Seitengröße mit [Page. setViewportSize ()][PlaywrightAPIPageSetViewport]anpassen.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-135">You may customize the page size with [page.setViewportSize()][PlaywrightAPIPageSetViewport].</span></span>  

:::image type="complex" source="../media/playwright-example.png" alt-text="Die von example.js erstellte example.png-Datei" lightbox="../media/playwright-example.png":::
    <span data-ttu-id="e0e2b-137">Die `example.png` Datei, die von</span><span class="sxs-lookup"><span data-stu-id="e0e2b-137">The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

`example.js` <span data-ttu-id="e0e2b-138">ist nur eine einfache Demonstration der von Dramatiker ermöglichten Automatisierungs-und Testszenarien.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-138">is just a simple demonstration of the automation and testing scenarios enabled by Playwright.</span></span>  <span data-ttu-id="e0e2b-139">Wenn Sie Screenshots in mehreren Webbrowsern erstellen möchten, ändern Sie den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-139">To take screenshots in multiple web browsers, change the following code.</span></span>  

*   <span data-ttu-id="e0e2b-140">Chromium</span><span class="sxs-lookup"><span data-stu-id="e0e2b-140">Chromium</span></span>  `await chromium.launch()`  
*   <span data-ttu-id="e0e2b-141">Firefox</span><span class="sxs-lookup"><span data-stu-id="e0e2b-141">Firefox</span></span>  `await firefox.launch()`  
*   <span data-ttu-id="e0e2b-142">WebKit</span><span class="sxs-lookup"><span data-stu-id="e0e2b-142">WebKit</span></span>  `await webkit.launch()`  

<span data-ttu-id="e0e2b-143">Weitere Informationen zu Dramatiker finden Sie auf der [Dramatiker-Website][|::ref6::|Main].</span><span class="sxs-lookup"><span data-stu-id="e0e2b-143">For more information about Playwright, navigate to the [Playwright website][|::ref6::|Main].</span></span>  <span data-ttu-id="e0e2b-144">Schauen Sie sich das  [Dramatiker-Repo][PlaywrightRepo] auf GitHub an.</span><span class="sxs-lookup"><span data-stu-id="e0e2b-144">Check out the  [Playwright repo][PlaywrightRepo] on GitHub.</span></span>  <span data-ttu-id="e0e2b-145">Wenn Sie Ihr Feedback zum Automatisieren und Testen Ihrer Website oder App mit Dramatiker freigeben möchten, können Sie [ein Problem einreichen][PlaywrightRepoNewIssue].</span><span class="sxs-lookup"><span data-stu-id="e0e2b-145">To share your feedback on automating and testing your website or app with Playwright, [file an issue][PlaywrightRepoNewIssue].</span></span>  

## <span data-ttu-id="e0e2b-146">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="e0e2b-146">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../devtools-guide-chromium/includes/contact-devtools-team-note.md)]  

<!-- links -->  

[WebdriverChromiumMain]: ../webdriver-chromium/index.md "WebDriver (Chrom) | Microsoft docs"  
[PuppeteerMain]: ../puppeteer.md "Puppenspieler | Microsoft docs"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: verbessern des Webs durch mehr Open-Source-Zusammenarbeit | Microsoft Experience-Blog"  

[MicrosoftEdgeDownload]: https://microsoft.com/edge "Herunterladen von Microsoft Edge"  

[ChromiumHome]: https://www.chromium.org/Home "Chrom | Die Chrom-Projekte"  

[FirefoxMain]: https://www.mozilla.org/firefox "Mozilla Firefox"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "Edge-Pfade | NPM"  

[PlaywrightMain]: https://playwright.dev "Dramatiker"  
[PlaywrightAPIReference]: https://playwright.dev#?path=docs/api.md "Dramatiker-API-Referenz"  
[PlaywrightAPIPageSetViewport]: https://playwright.dev#?path=docs%2Fapi.md&q=pagesetviewportsizeviewportsize "Page. setViewportSize (ViewportSize) | Dramatiker-API-Referenz"    
[PlaywrightSystemRequirements]: https://playwright.dev#?path=docs/intro.md&q=system-requirements "System Anforderungen für Dramatiker"  

[PlaywrightRepo]: https://github.com/microsoft/playwright "Dramatiker | GitHub"  
[PlaywrightRepoNewIssue]: https://github.com/microsoft/playwright/issues/new/choose "Neues Problem in Dramatiker-Repo | GitHub"  

[WebKitMain]: https://webkit.org "WebKit"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Headless-Browser | Wikipedia"  
