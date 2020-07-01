---
description: Verwenden von Puppenspieler zum Automatisieren und testen in Microsoft Edge
title: Puppeteer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Web-Entwicklung, Entwickler, Tools, Automatisierung, Test
ms.openlocfilehash: ccca46426a006651a417a22e54c8b528834b5f81
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "10844012"
---
# <span data-ttu-id="6d591-104">Puppeteer</span><span class="sxs-lookup"><span data-stu-id="6d591-104">Puppeteer</span></span>  

<span data-ttu-id="6d591-105">[Marionetten][|::ref1::|Main] ist eine [Knoten][NodejsMain] Bibliothek, die eine allgemeine API zur Steuerung von Microsoft Edge (Chrom \) über das [devtools-Protokoll][GithubChromedevtoolsProtocol]bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6d591-105">[Puppeteer][|::ref1::|Main] is a [Node][NodejsMain] library which provides a high-level API to control Microsoft Edge \(Chromium\) over the [DevTools Protocol][GithubChromedevtoolsProtocol].</span></span>  <span data-ttu-id="6d591-106">Puppenspieler läuft standardmäßig [headless][WikiHeadlessBrowser] , was bedeutet, dass Sie keine Benutzeroberfläche sehen und stattdessen die Befehlszeile verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="6d591-106">Puppeteer runs [headless][WikiHeadlessBrowser] by default, which means that you do not see a UI, and instead must use the command-line.</span></span>  <span data-ttu-id="6d591-107">Sie können auch den Puppenspieler so konfigurieren, dass er "Full \" (nicht-headless \) Microsoft Edge oder Chromium ausführt.</span><span class="sxs-lookup"><span data-stu-id="6d591-107">You may also configure Puppeteer to run full \(non-headless\) Microsoft Edge or Chromium as well.</span></span>  

<span data-ttu-id="6d591-108">Bei der Installation von Puppenspieler downloadet das Installationsprogramm standardmäßig eine neuere Version von [Chromium][ChromiumHome], den Open-Source-Browser, [auf dem Microsoft Edge ebenfalls][MicrosoftBlogsWindowsExperience20181206]basiert.</span><span class="sxs-lookup"><span data-stu-id="6d591-108">By default, when you install Puppeteer, the installer downloads a recent version of [Chromium][ChromiumHome], the open-source browser that [Microsoft Edge is also built upon][MicrosoftBlogsWindowsExperience20181206].</span></span>  <span data-ttu-id="6d591-109">Wenn Sie Microsoft Edge \ (Chrom \) installiert haben, können Sie die [Marionetten-Core-][PuppeteerApivscore]Version verwenden.</span><span class="sxs-lookup"><span data-stu-id="6d591-109">If you have Microsoft Edge \(Chromium\) installed, you may use [puppeteer-core][PuppeteerApivscore].</span></span>  `puppeteer-core` <span data-ttu-id="6d591-110">ist eine vereinfachte Version von Puppenspieler, die eine vorhandene Browserinstallation wie Microsoft Edge (Chrom \) startet.</span><span class="sxs-lookup"><span data-stu-id="6d591-110">is a lightweight version of Puppeteer that launches an existing browser installation, like Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="6d591-111">Informationen zum Herunterladen von Microsoft Edge \ (Chrom \) finden Sie unter [Herunterladen von Microsoft Edge-Insider Kanälen][MicrosoftedgeinsiderDownload].</span><span class="sxs-lookup"><span data-stu-id="6d591-111">To download Microsoft Edge \(Chromium\), see [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload].</span></span>

## <span data-ttu-id="6d591-112">Installieren von Puppenspieler-Core</span><span class="sxs-lookup"><span data-stu-id="6d591-112">Installing puppeteer-core</span></span>  

<span data-ttu-id="6d591-113">Sie können `puppeteer-core` Ihrer Website oder App mit einem der folgenden Befehle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6d591-113">You may add `puppeteer-core` to your website or app with one of the following commands.</span></span>  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## <span data-ttu-id="6d591-114">Starten von Microsoft Edge mit dem Puppenspieler-Core</span><span class="sxs-lookup"><span data-stu-id="6d591-114">Launch Microsoft Edge with puppeteer-core</span></span>  

> [!NOTE]
> `puppeteer-core` <span data-ttu-id="6d591-115">basiert auf Node v 8.9.0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="6d591-115">relies on Node v8.9.0 or later.</span></span>  <span data-ttu-id="6d591-116">Im folgenden Beispiel wird verwendet `async` / `await` , das nur in Node v 7.6.0 oder höher unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="6d591-116">The example below uses `async`/`await` which is only supported in Node v7.6.0 or later.</span></span>  <span data-ttu-id="6d591-117">Führen `node -v` Sie über die Befehlszeile aus, um sicherzustellen, dass Sie über eine kompatible Version von Node.js verfügen.</span><span class="sxs-lookup"><span data-stu-id="6d591-117">Run `node -v` from the command-line to ensure you have a compatible version of Node.js.</span></span>  

`puppeteer-core` <span data-ttu-id="6d591-118">sollte Benutzern anderer Browser-Test-Frameworks wie [WebDriver][WebDriverEdgehtmlMain]vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="6d591-118">should be familiar to users of other browser-testing-frameworks like [WebDriver][WebDriverEdgehtmlMain].</span></span>  <span data-ttu-id="6d591-119">Erstellen Sie eine Instanz des Browsers, öffnen Sie eine Seite, und bearbeiten Sie Sie dann mit der Marionetten-API.</span><span class="sxs-lookup"><span data-stu-id="6d591-119">You create an instance of the browser, open a page, and then manipulate it with the Puppeteer API.</span></span>  <span data-ttu-id="6d591-120">Im folgenden Codebeispiel wird `puppeteer-core` Microsoft Edge (Chrom \) gestartet, navigiert zu `https://www.microsoftedgeinsider.com` und speichert einen Screenshot als `example.png` .</span><span class="sxs-lookup"><span data-stu-id="6d591-120">In the following code sample, `puppeteer-core` launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="6d591-121">Kopieren Sie das folgende Codebeispiel, und speichern Sie es als `example.js` .</span><span class="sxs-lookup"><span data-stu-id="6d591-121">Copy the code sample below and save it as `example.js`.</span></span>  

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

<span data-ttu-id="6d591-122">Ändern `executablePath` Sie, um auf Ihre Installation von Microsoft Edge (Chrom \) zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="6d591-122">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="6d591-123">So sollte beispielsweise unter macOS `executablePath` für Microsoft Edge Canary auf festgesetzt werden `/Applications/Microsoft\ Edge\ Canary.app/` .</span><span class="sxs-lookup"><span data-stu-id="6d591-123">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="6d591-124">Um das zu finden `executablePath` , navigieren Sie zu dem `edge://version` **ausführbaren Pfad** auf dieser Seite, und kopieren Sie ihn, oder installieren Sie das [Edge-Paths-][npmEdgePaths] Paket mit einem der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="6d591-124">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with one of the following commands.</span></span>  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
<span data-ttu-id="6d591-125">Im folgenden Codebeispiel wird das [Edge-Paths-][npmEdgePaths] Paket verwendet, um den Pfad zu Ihrer Installation von Microsoft Edge (Chrom \) auf Ihrem Betriebssystem programmgesteuert zu finden.</span><span class="sxs-lookup"><span data-stu-id="6d591-125">The code sample below uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

<span data-ttu-id="6d591-126">Setzen Sie abschließend `executablePath: EDGE_PATH` ein `example.js` .</span><span class="sxs-lookup"><span data-stu-id="6d591-126">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="6d591-127">Speichern Sie Ihre Änderungen.</span><span class="sxs-lookup"><span data-stu-id="6d591-127">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="6d591-128">Microsoft Edge \ (EdgeHTML \) funktioniert nicht mit `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="6d591-128">Microsoft Edge \(EdgeHTML\) does not work with `puppeteer-core`.</span></span>  <span data-ttu-id="6d591-129">Sie müssen die [Microsoft Edge-Insider Kanäle][MicrosoftedgeinsiderDownload] installieren, um weiterhin diesem Beispiel folgen zu können.</span><span class="sxs-lookup"><span data-stu-id="6d591-129">You must install the [Microsoft Edge Insider channels][MicrosoftedgeinsiderDownload] to continue following this example.</span></span>  

<span data-ttu-id="6d591-130">Nun `example.js` über die Befehlszeile ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6d591-130">Now run `example.js` from the command-line.</span></span>  

```shell
node example.js
```  

`puppeteer-core` <span data-ttu-id="6d591-131">startet Microsoft Edge, navigiert zu `https://www.microsoftedgeinsider.com` und speichert einen Screenshot der Seite 800px x 600px.</span><span class="sxs-lookup"><span data-stu-id="6d591-131">launches Microsoft Edge, navigates to `https://www.microsoftedgeinsider.com` and saves an 800px x 600px screenshot of the page.</span></span>  <span data-ttu-id="6d591-132">Sie können die Seitengröße mit [Page. setviewport ()][PuppeteerApipagesetviewport]anpassen.</span><span class="sxs-lookup"><span data-stu-id="6d591-132">You are able to customize the page size with [page.setViewport()][PuppeteerApipagesetviewport].</span></span>  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="Die von example.js erstellte example.png-Datei":::
   <span data-ttu-id="6d591-134">Abbildung 1: die `example.png` Datei, die von erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="6d591-134">Figure 1:  The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

<!--  
> ##### Figure 1  
> The `example.png` file produced by `example.js`  
> ![The example.png file produced by example.js](./media/puppeteer-example.png)  
-->  

<span data-ttu-id="6d591-135">Dies ist nur ein einfaches Beispiel für die Automatisierungs-und Testszenarien, die von Marionetten und `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="6d591-135">This is just a simple example of the automation and testing scenarios enabled by Puppeteer and `puppeteer-core`.</span></span>  <span data-ttu-id="6d591-136">Weitere Informationen zu Puppenspielern und deren Funktionsweise finden Sie unter [Puppenspieler][|::ref2::|Main].</span><span class="sxs-lookup"><span data-stu-id="6d591-136">For more information about Puppeteer and how it works, see [Puppeteer][|::ref2::|Main].</span></span>  

## <span data-ttu-id="6d591-137">Feedback senden</span><span class="sxs-lookup"><span data-stu-id="6d591-137">Send Feedback</span></span>  

<span data-ttu-id="6d591-138">Das Edge-Entwicklerteam ist begierig, Ihr Feedback zur Verwendung von Puppenspieler `puppeteer-core` und Microsoft Edge zu hören.</span><span class="sxs-lookup"><span data-stu-id="6d591-138">The Edge Developer team is eager to hear your feedback about using Puppeteer, `puppeteer-core`, and Microsoft Edge.</span></span>  <span data-ttu-id="6d591-139">Verwenden Sie das Symbol " **Feedback senden** " im Microsoft Edge devtools-oder Tweet- [@EdgeDevTools][TwitterIntentTweetEdgedevtools] , damit das Microsoft Edge-Team wissen kann, was Sie denken.</span><span class="sxs-lookup"><span data-stu-id="6d591-139">Use the **Send Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] to let the Microsoft Edge team know what you think.</span></span>  


:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="Das Feedback Symbol in der Microsoft Edge-devtools":::
   <span data-ttu-id="6d591-141">Abbildung 2: das Symbol " **Feedback** " in der Microsoft Edge-devtools</span><span class="sxs-lookup"><span data-stu-id="6d591-141">Figure 2:  The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
> ##### Figure 2  
> The **Feedback** icon in the Microsoft Edge DevTools  
> ![The Feedback icon in the Microsoft Edge DevTools](./devtools-guide-chromium/media/devtools-feedback.png)  
-->  

<!--## See also  

*   [WebDriver (Chromium)][WebdriverChromiumMain]  
*   [WebDriver (EdgeHTML)][WebdriverEdgehtmlMain]  
*   [Chrome DevTools Protocol Viewer on GitHub][GithubChromedevtoolsProtocol]  
*   [Microsoft Edge: Making the web better through more open source collaboration on Microsoft Experience Blog][MicrosoftBlogsWindowsExperience20181206]  
*   [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload]  
*   [Chromium on The Chromium Projects][ChromiumHome]  
*   [Node.js][NodejsMain]  
*   [Puppeteer][PuppeteerMain]  
*   [puppeteer vs. puppeteer-core][PuppeteerApivscore]  
*   [page.setViewport() on Puppeteer][PuppeteerApipagesetviewport]  
*   [Headless browser on Wikipedia][WikiHeadlessBrowser]  -->  

<!-- image links -->  

<!-- links -->  

[WebdriverChromiumMain]: ./webdriver-chromium.md "WebDriver (Chrom)"  
[WebdriverEdgehtmlMain]: ./webdriver.md "WebDriver (EdgeHTML)"  

[GithubChromedevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Chrome devtools-Protokollanzeige | GitHub"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: verbessern des Webs durch mehr Open-Source-Zusammenarbeit | Microsoft Experience-Blog"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge-Insider Kanälen"  

[ChromiumHome]: https://www.chromium.org/Home "Chrom | Die Chrom-Projekte"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "NPM | Rand Pfade"

[PuppeteerMain]: https://pptr.dev "Puppeteer"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "Marionetten-vs. Puppenspieler-Core | Puppeteer"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "Page. setviewport (Viewport) | Puppeteer"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools-Poste einen Tweet | Twitter"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Headless-Browser | Wikipedia"  
