---
description: Verwenden von Puppenspieler zum Automatisieren und testen in Microsoft Edge
title: Puppeteer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Web-Entwicklung, Entwickler, Tools, Automatisierung, Test
ms.openlocfilehash: 99d873a9b3988cb8a2827ecc9a69d574a196b037
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233606"
---
# <span data-ttu-id="ae85f-104">Übersicht über Marionetten</span><span class="sxs-lookup"><span data-stu-id="ae85f-104">Puppeteer overview</span></span>  

<span data-ttu-id="ae85f-105">[Marionetten][|::ref1::|Main] ist eine [Knoten][NodejsMain] Bibliothek, die eine allgemeine API zur Steuerung von Microsoft Edge (Chrom \) mithilfe des [devtools-Protokolls][GithubChromedevtoolsProtocol]bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ae85f-105">[Puppeteer][|::ref1::|Main] is a [Node][NodejsMain] library that provides a high-level API to control Microsoft Edge \(Chromium\) using the [DevTools Protocol][GithubChromedevtoolsProtocol].</span></span>  <span data-ttu-id="ae85f-106">Der Puppenspieler startet standardmäßig [headless-Browser][WikiHeadlessBrowser] .</span><span class="sxs-lookup"><span data-stu-id="ae85f-106">Puppeteer launches [headless browsers][WikiHeadlessBrowser] by default.</span></span>  <span data-ttu-id="ae85f-107">Headless-Browser zeigen keine Benutzeroberfläche an, daher müssen Sie stattdessen die Befehlszeile verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae85f-107">Headless browsers do not display a UI, so instead you must use the command line.</span></span>  <span data-ttu-id="ae85f-108">Sie können auch den Puppenspieler so konfigurieren, dass er Full \ (nicht-headless \) Microsoft Edge ausführt.</span><span class="sxs-lookup"><span data-stu-id="ae85f-108">You may also configure Puppeteer to run full \(non-headless\) Microsoft Edge as well.</span></span>  

<span data-ttu-id="ae85f-109">Bei der Installation von Puppenspieler downloadet das Installationsprogramm standardmäßig eine neuere Version von [Chromium][ChromiumHome], den Open-Source-Browser, [auf dem Microsoft Edge ebenfalls][MicrosoftBlogsWindowsExperience20181206]basiert.</span><span class="sxs-lookup"><span data-stu-id="ae85f-109">By default, when you install Puppeteer, the installer downloads a recent version of [Chromium][ChromiumHome], the open-source browser that [Microsoft Edge is also built upon][MicrosoftBlogsWindowsExperience20181206].</span></span>  <span data-ttu-id="ae85f-110">Wenn Sie Microsoft Edge \ (Chrom \) installiert haben, können Sie die [Marionetten-Core-][PuppeteerApivscore]Version verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae85f-110">If you have Microsoft Edge \(Chromium\) installed, you may use [puppeteer-core][PuppeteerApivscore].</span></span>  `puppeteer-core` <span data-ttu-id="ae85f-111">ist eine vereinfachte Version von Puppenspieler, die eine vorhandene Browserinstallation wie Microsoft Edge (Chrom \) startet.</span><span class="sxs-lookup"><span data-stu-id="ae85f-111">is a lightweight version of Puppeteer that launches an existing browser installation, like Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="ae85f-112">Zum Herunterladen von Microsoft Edge \ (Chrom \) navigieren Sie zu [Microsoft Edge-Insider Kanälen herunterladen][MicrosoftedgeinsiderDownload].</span><span class="sxs-lookup"><span data-stu-id="ae85f-112">To download Microsoft Edge \(Chromium\), navigate to [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload].</span></span>  

## <span data-ttu-id="ae85f-113">Installieren von Puppenspieler-Core</span><span class="sxs-lookup"><span data-stu-id="ae85f-113">Installing puppeteer-core</span></span>  

<span data-ttu-id="ae85f-114">Sie können `puppeteer-core` Ihrer Website oder App mit einem der folgenden Befehle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ae85f-114">You may add `puppeteer-core` to your website or app with one of the following commands.</span></span>  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## <span data-ttu-id="ae85f-115">Starten von Microsoft Edge mit dem Puppenspieler-Core</span><span class="sxs-lookup"><span data-stu-id="ae85f-115">Launch Microsoft Edge with puppeteer-core</span></span>  

> [!NOTE]
> `puppeteer-core` <span data-ttu-id="ae85f-116">basiert auf Node v 8.9.0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="ae85f-116">relies on Node v8.9.0 or later.</span></span>  <span data-ttu-id="ae85f-117">Im folgenden Beispiel wird verwendet `async` / `await` , das nur in Node v 7.6.0 oder höher unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="ae85f-117">The example below uses `async`/`await` which is only supported in Node v7.6.0 or later.</span></span>  <span data-ttu-id="ae85f-118">Führen `node -v` Sie über die Befehlszeile aus, um sicherzustellen, dass Sie über eine kompatible Version von Node.js verfügen.</span><span class="sxs-lookup"><span data-stu-id="ae85f-118">Run `node -v` from the command-line to ensure you have a compatible version of Node.js.</span></span>  

`puppeteer-core` <span data-ttu-id="ae85f-119">sollte Benutzern anderer Browser-Test-Frameworks wie [WebDriver][WebdriverChromiumMain]vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="ae85f-119">should be familiar to users of other browser-testing-frameworks like [WebDriver][WebdriverChromiumMain].</span></span>  <span data-ttu-id="ae85f-120">Erstellen Sie eine Instanz des Browsers, öffnen Sie eine Seite, und bearbeiten Sie Sie dann mit der Marionetten-API.</span><span class="sxs-lookup"><span data-stu-id="ae85f-120">You create an instance of the browser, open a page, and then manipulate it with the Puppeteer API.</span></span>  <span data-ttu-id="ae85f-121">Im folgenden Codebeispiel wird `puppeteer-core` Microsoft Edge (Chrom \) gestartet, navigiert zu `https://www.microsoftedgeinsider.com` und speichert einen Screenshot als `example.png` .</span><span class="sxs-lookup"><span data-stu-id="ae85f-121">In the following code sample, `puppeteer-core` launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="ae85f-122">Kopieren Sie den folgenden Codeausschnitt, und speichern Sie ihn als `example.js` .</span><span class="sxs-lookup"><span data-stu-id="ae85f-122">Copy the following code snippet and save it as `example.js`.</span></span>  

```javascript
const puppeteer = require('puppeteer-core');

(async () => {
  const browser = await puppeteer.launch({
    executablePath: 'C:\\Program Files (x86)\\Microsoft\\Edge Dev\\Application\\msedge.exe'
  });
  const page = await browser.newPage();
  await page.goto('https://www.microsoftedgeinsider.com');
  await page.screenshot({path: 'example.png'});

  await browser.close();
})();
```  

<span data-ttu-id="ae85f-123">Ändern `executablePath` Sie, um auf Ihre Installation von Microsoft Edge (Chrom \) zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="ae85f-123">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="ae85f-124">So sollte beispielsweise unter macOS `executablePath` für Microsoft Edge Canary auf festgesetzt werden `/Applications/Microsoft\ Edge\ Canary.app/` .</span><span class="sxs-lookup"><span data-stu-id="ae85f-124">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="ae85f-125">Um das zu finden `executablePath` , navigieren Sie zu dem `edge://version` **ausführbaren Pfad** auf dieser Seite, und kopieren Sie ihn, oder installieren Sie das [Edge-Paths-][npmEdgePaths] Paket mit einem der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="ae85f-125">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with one of the following commands.</span></span>  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
<span data-ttu-id="ae85f-126">Im folgenden Codebeispiel wird das [Edge-Paths-][npmEdgePaths] Paket verwendet, um den Pfad zu Ihrer Installation von Microsoft Edge (Chrom \) auf Ihrem Betriebssystem programmgesteuert zu finden.</span><span class="sxs-lookup"><span data-stu-id="ae85f-126">The code sample below uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

<span data-ttu-id="ae85f-127">Setzen Sie abschließend `executablePath: EDGE_PATH` ein `example.js` .</span><span class="sxs-lookup"><span data-stu-id="ae85f-127">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="ae85f-128">Speichern Sie Ihre Änderungen.</span><span class="sxs-lookup"><span data-stu-id="ae85f-128">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="ae85f-129">Microsoft Edge \ (EdgeHTML \) funktioniert nicht mit `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="ae85f-129">Microsoft Edge \(EdgeHTML\) does not work with `puppeteer-core`.</span></span>  <span data-ttu-id="ae85f-130">Sie müssen die [Microsoft Edge-Insider Kanäle][MicrosoftedgeinsiderDownload] installieren, um weiterhin diesem Beispiel folgen zu können.</span><span class="sxs-lookup"><span data-stu-id="ae85f-130">You must install the [Microsoft Edge Insider channels][MicrosoftedgeinsiderDownload] to continue following this example.</span></span>  

<span data-ttu-id="ae85f-131">Führen Sie nun `example.js` über die Befehlszeile aus.</span><span class="sxs-lookup"><span data-stu-id="ae85f-131">Now, run `example.js` from the command line.</span></span>  

```shell
node example.js
```  

`puppeteer-core` <span data-ttu-id="ae85f-132">startet Microsoft Edge, navigiert zu `https://www.microsoftedgeinsider.com` und speichert einen Screenshot der Webseite.</span><span class="sxs-lookup"><span data-stu-id="ae85f-132">launches Microsoft Edge, navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot of the webpage.</span></span>  <span data-ttu-id="ae85f-133">Passen Sie die Bildschirmgröße mit [Page. setviewport ()][PuppeteerApipagesetviewport]an.</span><span class="sxs-lookup"><span data-stu-id="ae85f-133">Customize the screenshot size with [page.setViewport()][PuppeteerApipagesetviewport].</span></span>  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="Die von example.js erstellte example.png-Datei" lightbox="./media/puppeteer-example.png":::
   <span data-ttu-id="ae85f-135">Die `example.png` Datei, die von</span><span class="sxs-lookup"><span data-stu-id="ae85f-135">The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

<span data-ttu-id="ae85f-136">Dies ist nur ein einfaches Beispiel für die Automatisierungs-und Testszenarien, die von Marionetten und `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="ae85f-136">This is just a simple example of the automation and testing scenarios enabled by Puppeteer and `puppeteer-core`.</span></span>  <span data-ttu-id="ae85f-137">Weitere Informationen zu Puppenspielern und deren Funktionsweise finden Sie unter [Puppenspieler][|::ref2::|Main].</span><span class="sxs-lookup"><span data-stu-id="ae85f-137">For more information about Puppeteer and how it works, see [Puppeteer][|::ref2::|Main].</span></span>  

## <span data-ttu-id="ae85f-138">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="ae85f-138">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="ae85f-139">Das Microsoft Edge-Entwicklerteam freut sich, Ihr Feedback zur Verwendung von Puppenspieler `puppeteer-core` und Microsoft Edge zu hören.</span><span class="sxs-lookup"><span data-stu-id="ae85f-139">The Microsoft Edge Developer team is eager to hear your feedback about using Puppeteer, `puppeteer-core`, and Microsoft Edge.</span></span>  <span data-ttu-id="ae85f-140">Verwenden Sie das Symbol " **Feedback senden** " im Microsoft Edge devtools-oder Tweet- [@EdgeDevTools][TwitterIntentTweetEdgedevtools] , damit das Microsoft Edge-Team wissen kann, was Sie denken.</span><span class="sxs-lookup"><span data-stu-id="ae85f-140">Use the **Send Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] to let the Microsoft Edge team know what you think.</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Das Symbol „Feedback senden“ in den Microsoft Edge-Entwicklungstools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="ae85f-142">Das Symbol " **Feedback senden** " im Microsoft Edge-devtools</span><span class="sxs-lookup"><span data-stu-id="ae85f-142">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--## See also  

*   [WebDriver (Chromium)][WebdriverChromiumMain]  
*   [WebDriver (EdgeHTML)][WebdriverEdgehtmlMain]  
*   [Chrome DevTools Protocol Viewer on GitHub][GithubChromedevtoolsProtocol]  
*   [Microsoft Edge:  Making the web better through more open source collaboration on Microsoft Experience Blog][MicrosoftBlogsWindowsExperience20181206]  
*   [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload]  
*   [Chromium on The Chromium Projects][ChromiumHome]  
*   [Node.js][NodejsMain]  
*   [Puppeteer][PuppeteerMain]  
*   [puppeteer vs. puppeteer-core][PuppeteerApivscore]  
*   [page.setViewport() on Puppeteer][PuppeteerApipagesetviewport]  
*   [Headless browser on Wikipedia][WikiHeadlessBrowser]  -->  

<!-- links -->  

[WebdriverChromiumMain]: ../webdriver-chromium/index.md "WebDriver (Chrom) | Microsoft docs"  
<!--  [WebdriverEdgehtmlMain]: ../edgehtml/webdriver/index.md "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[GithubChromedevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Chrome devtools-Protokollanzeige | GitHub"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: verbessern des Webs durch mehr Open-Source-Zusammenarbeit | Microsoft Experience-Blog"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[ChromiumHome]: https://www.chromium.org/Home "Chrom | Die Chrom-Projekte"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "Rand Pfade | NPM"  

[PuppeteerMain]: https://pptr.dev "Puppeteer"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "Marionetten-vs. Puppenspieler-Core | Puppeteer"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "Page. setviewport (Viewport) | Puppeteer"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools-Poste einen Tweet | Twitter"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Headless-Browser | Wikipedia"  
