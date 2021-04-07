---
description: Verwenden von Puppeteer zum Automatisieren und Testen in Microsoft Edge
title: Puppeteer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/06/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, web development, developer, tools, automation, test
ms.openlocfilehash: 89a4dad3319f8e61f27487973509a8ee5ac23b6a
ms.sourcegitcommit: 146072bf606b84e5145a48333abf9c6b892a12d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/07/2021
ms.locfileid: "11480167"
---
# <a name="puppeteer-overview"></a><span data-ttu-id="7bad5-104">Puppeteer – Übersicht</span><span class="sxs-lookup"><span data-stu-id="7bad5-104">Puppeteer overview</span></span>  

<span data-ttu-id="7bad5-105">[Puppeteer][|::ref1::|Main] ist eine [Knotenbibliothek,][NodejsMain] die eine high-level-API zum Steuern von Microsoft Edge \(Chromium\) mithilfe des [DevTools-Protokolls bietet.][GithubChromedevtoolsProtocol]</span><span class="sxs-lookup"><span data-stu-id="7bad5-105">[Puppeteer][|::ref1::|Main] is a [Node][NodejsMain] library that provides a high-level API to control Microsoft Edge \(Chromium\) using the [DevTools Protocol][GithubChromedevtoolsProtocol].</span></span>  <span data-ttu-id="7bad5-106">Puppeteer startet [standardmäßig browserlose][WikiHeadlessBrowser] Browser.</span><span class="sxs-lookup"><span data-stu-id="7bad5-106">Puppeteer launches [headless browsers][WikiHeadlessBrowser] by default.</span></span>  <span data-ttu-id="7bad5-107">Headless-Browser zeigen keine Benutzeroberfläche an, daher müssen Sie stattdessen die Befehlszeile verwenden.</span><span class="sxs-lookup"><span data-stu-id="7bad5-107">Headless browsers do not display a UI, so instead you must use the command line.</span></span>  <span data-ttu-id="7bad5-108">Sie können auch Puppeteer so konfigurieren, dass er auch vollständig \(nicht kopflos\) Microsoft Edge ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="7bad5-108">You may also configure Puppeteer to run full \(non-headless\) Microsoft Edge as well.</span></span>  

<span data-ttu-id="7bad5-109">Standardmäßig lädt das Installationsprogramm bei der Installation von Puppeteer eine aktuelle Version von [Chromium][ChromiumHome]herunter, den Open-Source-Browser, auf dem [Auch Microsoft Edge aufgebaut ist.][MicrosoftBlogsWindowsExperience20181206]</span><span class="sxs-lookup"><span data-stu-id="7bad5-109">By default, when you install Puppeteer, the installer downloads a recent version of [Chromium][ChromiumHome], the open-source browser that [Microsoft Edge is also built upon][MicrosoftBlogsWindowsExperience20181206].</span></span>  <span data-ttu-id="7bad5-110">Wenn Sie Microsoft Edge \(Chromium\) installiert haben, können Sie [puppeteer-core verwenden.][PuppeteerApivscore]</span><span class="sxs-lookup"><span data-stu-id="7bad5-110">If you have Microsoft Edge \(Chromium\) installed, you may use [puppeteer-core][PuppeteerApivscore].</span></span>  `puppeteer-core` <span data-ttu-id="7bad5-111">ist eine einfache Version von Puppeteer, die eine vorhandene Browserinstallation startet, z. B. Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="7bad5-111">is a lightweight version of Puppeteer that launches an existing browser installation, like Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="7bad5-112">Navigieren Sie zum Herunterladen von Microsoft Edge \(Chromium\) zu [Microsoft Edge Insider Channels herunterladen.][MicrosoftedgeinsiderDownload]</span><span class="sxs-lookup"><span data-stu-id="7bad5-112">To download Microsoft Edge \(Chromium\), navigate to [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload].</span></span>  

## <a name="installing-puppeteer-core"></a><span data-ttu-id="7bad5-113">Installieren von "puppeteer-core"</span><span class="sxs-lookup"><span data-stu-id="7bad5-113">Installing puppeteer-core</span></span>  

<span data-ttu-id="7bad5-114">Sie können Ihrer `puppeteer-core` Website oder App einen der folgenden Befehle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7bad5-114">You may add `puppeteer-core` to your website or app with one of the following commands.</span></span>  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## <a name="launch-microsoft-edge-with-puppeteer-core"></a><span data-ttu-id="7bad5-115">Starten von Microsoft Edge mit puppeteer-core</span><span class="sxs-lookup"><span data-stu-id="7bad5-115">Launch Microsoft Edge with puppeteer-core</span></span>  

> [!NOTE]
> `puppeteer-core` <span data-ttu-id="7bad5-116">verwendet Knoten v8.9.0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="7bad5-116">relies on Node v8.9.0 or later.</span></span>  <span data-ttu-id="7bad5-117">Das folgende Beispiel `async` / `await` verwendet, das nur in Knoten v7.6.0 oder höher unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="7bad5-117">The example below uses `async`/`await` which is only supported in Node v7.6.0 or later.</span></span>  <span data-ttu-id="7bad5-118">Führen `node -v` Sie die Befehlszeile aus, um sicherzustellen, dass Sie über eine kompatible Version von Node.js.</span><span class="sxs-lookup"><span data-stu-id="7bad5-118">Run `node -v` from the command-line to ensure you have a compatible version of Node.js.</span></span>  

`puppeteer-core` <span data-ttu-id="7bad5-119">benutzer anderer browser-testing-frameworks wie [WebDriver vertraut sein sollten.][WebdriverChromiumMain]</span><span class="sxs-lookup"><span data-stu-id="7bad5-119">should be familiar to users of other browser-testing-frameworks like [WebDriver][WebdriverChromiumMain].</span></span>  <span data-ttu-id="7bad5-120">Sie erstellen eine Instanz des Browsers, öffnen eine Seite und bearbeiten sie dann mit der Puppeteer-API.</span><span class="sxs-lookup"><span data-stu-id="7bad5-120">You create an instance of the browser, open a page, and then manipulate it with the Puppeteer API.</span></span>  <span data-ttu-id="7bad5-121">Im folgenden Codebeispiel startet `puppeteer-core` Microsoft Edge \(Chromium\), navigiert zu `https://www.microsoftedgeinsider.com` , und speichert einen Screenshot als `example.png` .</span><span class="sxs-lookup"><span data-stu-id="7bad5-121">In the following code sample, `puppeteer-core` launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="7bad5-122">Kopieren Sie den folgenden Codeausschnitt, und speichern Sie ihn unter `example.js` .</span><span class="sxs-lookup"><span data-stu-id="7bad5-122">Copy the following code snippet and save it as `example.js`.</span></span>  

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

<span data-ttu-id="7bad5-123">Ändern `executablePath` Sie, um auf Ihre Installation von Microsoft Edge \(Chromium\) zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="7bad5-123">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="7bad5-124">Unter macOS sollte beispielsweise für `executablePath` Microsoft Edge Canary auf festgelegt `/Applications/Microsoft\ Edge\ Canary.app/` werden.</span><span class="sxs-lookup"><span data-stu-id="7bad5-124">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="7bad5-125">Navigieren Sie zu und kopieren Sie den ausführbaren Pfad auf dieser Seite, oder installieren Sie das `executablePath` `edge://version` [Edgepfadpaket][npmEdgePaths] \*\*\*\* mit einem der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="7bad5-125">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with one of the following commands.</span></span>  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
<span data-ttu-id="7bad5-126">Im folgenden Codebeispiel wird das [Edgepfadpaket][npmEdgePaths] verwendet, um programmgesteuert den Pfad zu Ihrer Installation von Microsoft Edge \(Chromium\) auf Ihrem Betriebssystem zu finden.</span><span class="sxs-lookup"><span data-stu-id="7bad5-126">The code sample below uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

<span data-ttu-id="7bad5-127">Legen Sie schließlich `executablePath: EDGE_PATH` in . `example.js`</span><span class="sxs-lookup"><span data-stu-id="7bad5-127">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="7bad5-128">Speichern Sie Ihre Änderungen.</span><span class="sxs-lookup"><span data-stu-id="7bad5-128">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="7bad5-129">Microsoft Edge \(EdgeHTML\) funktioniert nicht mit `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="7bad5-129">Microsoft Edge \(EdgeHTML\) does not work with `puppeteer-core`.</span></span>  <span data-ttu-id="7bad5-130">Sie müssen die [Microsoft Edge-Insider-Kanäle installieren,][MicrosoftedgeinsiderDownload] um dieses Beispiel weiter zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7bad5-130">You must install the [Microsoft Edge Insider channels][MicrosoftedgeinsiderDownload] to continue following this example.</span></span>  

<span data-ttu-id="7bad5-131">Führen Sie jetzt `example.js` über die Befehlszeile aus.</span><span class="sxs-lookup"><span data-stu-id="7bad5-131">Now, run `example.js` from the command line.</span></span>  

```shell
node example.js
```  

`puppeteer-core` <span data-ttu-id="7bad5-132">startet Microsoft Edge, navigiert zu `https://www.microsoftedgeinsider.com` und speichert einen Screenshot der Webseite.</span><span class="sxs-lookup"><span data-stu-id="7bad5-132">launches Microsoft Edge, navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot of the webpage.</span></span>  <span data-ttu-id="7bad5-133">Passen Sie die Screenshotgröße mit [page.setViewport() an.][PuppeteerApipagesetviewport]</span><span class="sxs-lookup"><span data-stu-id="7bad5-133">Customize the screenshot size with [page.setViewport()][PuppeteerApipagesetviewport].</span></span>  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="Die example.png datei, die von example.js" lightbox="./media/puppeteer-example.png":::
   <span data-ttu-id="7bad5-135">Die `example.png` datei, die von</span><span class="sxs-lookup"><span data-stu-id="7bad5-135">The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

<span data-ttu-id="7bad5-136">Dies ist nur ein einfaches Beispiel für die Automatisierungs- und Testszenarien, die von Puppeteer und aktiviert `puppeteer-core` werden.</span><span class="sxs-lookup"><span data-stu-id="7bad5-136">This is just a simple example of the automation and testing scenarios enabled by Puppeteer and `puppeteer-core`.</span></span>  <span data-ttu-id="7bad5-137">Weitere Informationen zu Puppeteer und deren Funktionsweise finden Sie unter [Puppeteer][|::ref2::|Main].</span><span class="sxs-lookup"><span data-stu-id="7bad5-137">For more information about Puppeteer and how it works, navigate to [Puppeteer][|::ref2::|Main].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="7bad5-138">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="7bad5-138">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="7bad5-139">Das Microsoft Edge Developer-Team ist gespannt auf Ihr Feedback zur Verwendung von Puppeteer `puppeteer-core` und Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7bad5-139">The Microsoft Edge Developer team is eager to hear your feedback about using Puppeteer, `puppeteer-core`, and Microsoft Edge.</span></span>  <span data-ttu-id="7bad5-140">Verwenden Sie **das Symbol Feedback** senden in [][TwitterIntentTweetEdgedevtools] der Microsoft Edge DevTools- oder @EdgeDevTools, um das Microsoft Edge-Team über Ihre Meinung zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="7bad5-140">Use the **Send Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] to let the Microsoft Edge team know what you think.</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Das Symbol „Feedback senden“ in den Microsoft Edge-Entwicklungstools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="7bad5-142">Das Symbol **Feedback senden** in den Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7bad5-142">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--## See also  

*   [WebDriver (Chromium)][WebdriverChromiumMain]  
*   [WebDriver (EdgeHTML)][ArchiveMicrosoftEdgeLegacyDeveloperWebdriverIndex]  
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

[WebdriverChromiumMain]: ../webdriver-chromium/index.md "WebDriver (Chromium) | Microsoft Docs"  

<!--  [ArchiveMicrosoftEdgeLegacyDeveloperWebdriverIndex]: /archive/microsoft-edge/legacy/developer/webdriver/index "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[GithubChromedevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Chrome DevTools Protocol Viewer | GitHub"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: Verbessern des Webs durch mehr Open-Source-Zusammenarbeit | Microsoft Experience Blog"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium | Die Chromium-Projekte"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "Edgepfade | npm"  

[PuppeteerMain]: https://pptr.dev "Puppeteer"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "puppeteer vs. puppeteer-core | Puppeteer"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "page.setViewport(viewport) | Puppeteer"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools – Post a Tweet | Twitter"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Monitorlose Browser-| Wikipedia"  
