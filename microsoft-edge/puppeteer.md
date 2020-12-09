---
description: Verwenden von Puppenspieler zum Automatisieren und testen in Microsoft Edge
title: Puppeteer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Web-Entwicklung, Entwickler, Tools, Automatisierung, Test
ms.openlocfilehash: e92a863f28c96157b4c7692bd88ba6884cbf8f52
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "11192233"
---
# Puppeteer  

[Marionetten][|::ref1::|Main] ist eine [Knoten][NodejsMain] Bibliothek, die eine allgemeine API zur Steuerung von Microsoft Edge (Chrom \) mithilfe des [devtools-Protokolls][GithubChromedevtoolsProtocol]bereitstellt.  Der Puppenspieler startet standardmäßig [headless-Browser][WikiHeadlessBrowser] .  Headless-Browser zeigen keine Benutzeroberfläche an, daher müssen Sie stattdessen die Befehlszeile verwenden.  Sie können auch den Puppenspieler so konfigurieren, dass er Full \ (nicht-headless \) Microsoft Edge ausführt.  

Bei der Installation von Puppenspieler downloadet das Installationsprogramm standardmäßig eine neuere Version von [Chromium][ChromiumHome], den Open-Source-Browser, [auf dem Microsoft Edge ebenfalls][MicrosoftBlogsWindowsExperience20181206]basiert.  Wenn Sie Microsoft Edge \ (Chrom \) installiert haben, können Sie die [Marionetten-Core-][PuppeteerApivscore]Version verwenden.  `puppeteer-core` ist eine vereinfachte Version von Puppenspieler, die eine vorhandene Browserinstallation wie Microsoft Edge (Chrom \) startet.  Zum Herunterladen von Microsoft Edge \ (Chrom \) navigieren Sie zu [Microsoft Edge-Insider Kanälen herunterladen][MicrosoftedgeinsiderDownload].  

## Installieren von Puppenspieler-Core  

Sie können `puppeteer-core` Ihrer Website oder App mit einem der folgenden Befehle hinzufügen.  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## Starten von Microsoft Edge mit dem Puppenspieler-Core  

> [!NOTE]
> `puppeteer-core` basiert auf Node v 8.9.0 oder höher.  Im folgenden Beispiel wird verwendet `async` / `await` , das nur in Node v 7.6.0 oder höher unterstützt wird.  Führen `node -v` Sie über die Befehlszeile aus, um sicherzustellen, dass Sie über eine kompatible Version von Node.js verfügen.  

`puppeteer-core` sollte Benutzern anderer Browsertest-Frameworks wie [WebDriver][WebDriverEdgehtmlMain]vertraut sein.  Erstellen Sie eine Instanz des Browsers, öffnen Sie eine Seite, und bearbeiten Sie Sie dann mit der Marionetten-API.  Im folgenden Codebeispiel wird `puppeteer-core` Microsoft Edge (Chrom \) gestartet, navigiert zu `https://www.microsoftedgeinsider.com` und speichert einen Screenshot als `example.png` .  

Kopieren Sie den folgenden Codeausschnitt, und speichern Sie ihn als `example.js` .  

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

Ändern `executablePath` Sie, um auf Ihre Installation von Microsoft Edge (Chrom \) zu verweisen.  So sollte beispielsweise unter macOS `executablePath` für Microsoft Edge Canary auf festgesetzt werden `/Applications/Microsoft\ Edge\ Canary.app/` .  Um das zu finden `executablePath` , navigieren Sie zu dem `edge://version` **ausführbaren Pfad** auf dieser Seite, und kopieren Sie ihn, oder installieren Sie das [Edge-Paths-][npmEdgePaths] Paket mit einem der folgenden Befehle.  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
Im folgenden Codebeispiel wird das [Edge-Paths-][npmEdgePaths] Paket verwendet, um den Pfad zu Ihrer Installation von Microsoft Edge (Chrom \) auf Ihrem Betriebssystem programmgesteuert zu finden.

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

Setzen Sie abschließend `executablePath: EDGE_PATH` ein `example.js` .  Speichern Sie Ihre Änderungen.  

> [!NOTE]
> Microsoft Edge \ (EdgeHTML \) funktioniert nicht mit `puppeteer-core` .  Sie müssen die [Microsoft Edge-Insider Kanäle][MicrosoftedgeinsiderDownload] installieren, um weiterhin diesem Beispiel folgen zu können.  

Führen Sie nun `example.js` über die Befehlszeile aus.  

```shell
node example.js
```  

`puppeteer-core` startet Microsoft Edge, navigiert zu `https://www.microsoftedgeinsider.com` und speichert einen Screenshot der Webseite.  Passen Sie die Bildschirmgröße mit [Page. setviewport ()][PuppeteerApipagesetviewport]an.  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="Die von example.js erstellte example.png-Datei" lightbox="./media/puppeteer-example.png":::
   Die `example.png` Datei, die von `example.js`  
:::image-end:::  

Im folgenden einfachen Beispiel werden Automatisierungs-und Testszenarien verwendet, die von Puppenspieler und `puppeteer-core` .  Wenn Sie weitere Informationen zu Puppenspielern und deren Funktionsweise erhalten möchten, navigieren Sie zu [Puppenspieler][|::ref2::|Main].  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

Das Microsoft Edge-Entwicklerteam freut sich, Ihr Feedback zur Verwendung von Puppenspieler `puppeteer-core` und Microsoft Edge zu hören.  Verwenden Sie das Symbol " **Feedback senden** " im Microsoft Edge devtools-oder Tweet- [@EdgeDevTools][TwitterIntentTweetEdgedevtools] , damit das Microsoft Edge-Team wissen kann, was Sie denken.  


:::image type="complex" source="./devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Das Symbol Feedback senden im Microsoft Edge-devtools"::: lightbox="./devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   Das Symbol " **Feedback senden** " im Microsoft Edge-devtools  
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

[WebdriverChromiumMain]: ./webdriver-chromium "WebDriver (Chrom) | Microsoft docs"  
[WebdriverEdgehtmlMain]: ./webdriver.md "WebDriver (EdgeHTML) | Microsoft docs"  

[GithubChromedevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Chrome devtools-Protokollanzeige | GitHub"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: verbessern des Webs durch mehr Open-Source-Zusammenarbeit | Microsoft Experience-Blog"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge-Insider Kanälen"  

[ChromiumHome]: https://www.chromium.org/Home "Chrom | Die Chrom-Projekte"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "Rand Pfade | NPM"  

[PuppeteerMain]: https://pptr.dev "Puppeteer"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "Marionetten-vs. Puppenspieler-Core | Puppeteer"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "Page. setviewport (Viewport) | Puppeteer"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools-Poste einen Tweet | Twitter"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Headless-Browser | Wikipedia"  
