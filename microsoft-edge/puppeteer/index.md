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
# <a name="puppeteer-overview"></a>Puppeteer – Übersicht  

[Puppeteer][|::ref1::|Main] ist eine [Node-Bibliothek,][NodejsMain] die eine high-level-API zum Steuern Microsoft Edge \(Chromium\) mithilfe des [DevTools-Protokolls bietet.][GithubChromedevtoolsProtocol]  Puppeteer startet [standardmäßig browserlose][WikiHeadlessBrowser] Browser.  Headless-Browser zeigen keine Benutzeroberfläche an, daher müssen Sie stattdessen die Befehlszeile verwenden.  Sie können Auch für Puppeteer die Ausführung von vollständigen \(non-headless\) Microsoft Edge konfigurieren.  

Standardmäßig lädt das Installationsprogramm bei der Installation von Puppeteer eine aktuelle Version von [Chromium][ChromiumHome]herunter, dem Open-Source-Browser, auf [dem Microsoft Edge ist.][MicrosoftBlogsWindowsExperience20181206]  Wenn Sie Microsoft Edge \(Chromium\) installiert haben, verwenden Sie [möglicherweise puppeteer-core][PuppeteerApivscore].  `puppeteer-core` ist eine einfache Version von Puppeteer, die eine vorhandene Browserinstallation startet, z. B. Microsoft Edge \(Chromium\).  Um Microsoft Edge \(Chromium\) herunterzuladen, navigieren Sie zu [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload].  

## <a name="installing-puppeteer-core"></a>Installieren von "puppeteer-core"  

Sie können Ihrer `puppeteer-core` Website oder App einen der folgenden Befehle hinzufügen.  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## <a name="launch-microsoft-edge-with-puppeteer-core"></a>Starten Microsoft Edge mit puppeteer-core  

> [!NOTE]
> `puppeteer-core` verwendet Knoten v8.9.0 oder höher.  Das folgende Beispiel `async` / `await` verwendet, das nur in Knoten v7.6.0 oder höher unterstützt wird.  Führen `node -v` Sie die Befehlszeile aus, um sicherzustellen, dass Sie über eine kompatible Version von Node.js.  

`puppeteer-core` benutzer anderer browser-testing-frameworks wie [WebDriver vertraut sein sollten.][WebdriverChromiumMain]  Sie erstellen eine Instanz des Browsers, öffnen eine Seite und bearbeiten sie dann mit der Puppeteer-API.  Im folgenden Codebeispiel startet `puppeteer-core` Microsoft Edge \(Chromium\), navigiert zu , und speichert `https://www.microsoftedgeinsider.com` einen Screenshot als `example.png` .  

Kopieren Sie den folgenden Codeausschnitt, und speichern Sie ihn unter `example.js` .  

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

Ändern `executablePath` Sie, um auf Ihre Installation von Microsoft Edge \(Chromium\) zu verweisen.  Unter macOS sollte beispielsweise der für `executablePath` Microsoft Edge Canary auf festgelegt `/Applications/Microsoft\ Edge\ Canary.app/` werden.  Navigieren Sie zu und kopieren Sie den ausführbaren Pfad auf dieser Seite, oder installieren Sie das `executablePath` `edge://version` [Edgepfadpaket][npmEdgePaths] **** mit einem der folgenden Befehle.  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
Im folgenden Codebeispiel wird das [Edgepfadpaket][npmEdgePaths] verwendet, um programmgesteuert den Pfad zu Ihrer Installation von Microsoft Edge \(Chromium\) auf Ihrem Betriebssystem zu finden.

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

Legen Sie schließlich `executablePath: EDGE_PATH` in . `example.js`  Speichern Sie Ihre Änderungen.  

> [!NOTE]
> Microsoft Edge \(EdgeHTML\) funktioniert nicht mit `puppeteer-core` .  Sie müssen die Microsoft Edge [installieren, um][MicrosoftedgeinsiderDownload] dieses Beispiel weiter zu folgen.  

Führen Sie jetzt `example.js` über die Befehlszeile aus.  

```shell
node example.js
```  

`puppeteer-core` startet Microsoft Edge, navigiert zu `https://www.microsoftedgeinsider.com` und speichert einen Screenshot der Webseite.  Passen Sie die Screenshotgröße mit [page.setViewport() an.][PuppeteerApipagesetviewport]  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="Die example.png datei, die von example.js" lightbox="./media/puppeteer-example.png":::
   Die `example.png` datei, die von `example.js`  
:::image-end:::  

Dies ist nur ein einfaches Beispiel für die Automatisierungs- und Testszenarien, die von Puppeteer und aktiviert `puppeteer-core` werden.  Weitere Informationen zu Puppeteer und deren Funktionsweise finden Sie unter [Puppeteer][|::ref2::|Main].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

Das Microsoft Edge Entwicklerteam ist gespannt auf Ihr Feedback zur Verwendung von Puppeteer und `puppeteer-core` Microsoft Edge.  Verwenden Sie **das Symbol Feedback** senden in [][TwitterIntentTweetEdgedevtools] der Microsoft Edge DevTools- oder Tweet-@EdgeDevTools, um das Microsoft Edge wissen zu lassen, was Sie denken.  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Das Symbol Feedback senden in den Microsoft Edge-Entwicklungstools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   Das Symbol **Feedback senden** in den Microsoft Edge DevTools  
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

[ChromiumHome]: https://www.chromium.org/Home "Chromium | Die Chromium Projekte"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "Edgepfade | npm"  

[PuppeteerMain]: https://pptr.dev "Puppeteer"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "puppeteer vs. puppeteer-core | Puppeteer"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "page.setViewport(viewport) | Puppeteer"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools – Post a Tweet | Twitter"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Monitorlose Browser-| Wikipedia"  
