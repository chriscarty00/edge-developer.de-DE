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
# Dramatiker  

[Playwright][|::ref1::|Main] ist [eine][NodejsMain]Node.js, um Chromium [,][ChromiumHome] [Firefox][FirefoxMain]und [WebKit][|::ref2::|Main] mit einer einzigen API zu automatisieren.  Playwright wurde entwickelt, um browserübergreifende Webautomatisierung zu ermöglichen, die immer grün, fähig, zuverlässig und schnell ist.  Da [Microsoft Edge auf der Open-Source-Chromium-Webplattform][MicrosoftBlogsWindowsExperience20181206]aufgebaut ist, kann Playwright auch Microsoft Edge.  

Playwright startet [standardmäßig browserlose][WikiHeadlessBrowser] Browser.  Headless-Browser zeigen keine Benutzeroberfläche an, daher müssen Sie stattdessen die Befehlszeile verwenden.  Sie können Playwright auch so konfigurieren, dass vollständige \(nicht kopflose\) Microsoft Edge ausgeführt werden.  

Bei der Installation von Playwright lädt das Installationsprogramm standardmäßig [Chromium][ChromiumHome], [Firefox][FirefoxMain]und [WebKit herunter.][|::ref3::|Main]  Wenn Sie auch Microsoft Edge \(Chromium\) installiert haben, benötigt Playwright nur eine einz nen Codeänderung, um Ihre Website oder App in Microsoft Edge.  Um Microsoft Edge \(Chromium\) herunterzuladen, navigieren Sie zu [Download Microsoft Edge][MicrosoftEdgeDownload].  

## Installieren von Playwright  

Installieren [Sie Playwright,][|::ref4::|Main] um Ihre Website oder App mit dem folgenden Befehl zu testen.  

```shell
npm i playwright
```  

## Starten Microsoft Edge mit Playwright  

> [!NOTE]
> [Playwright][|::ref5::|Main] erfordert Node.js Version 10.17 oder höher. Führen `node -v` Sie über die Befehlszeile aus, um sicherzustellen, dass Sie über eine kompatible Version von Node.js.  Die Browser-Binärdateien für Chromium, Firefox und WebKit funktionieren Windows, macOS und Linux. Weitere Informationen finden Sie unter [Playwright System Requirements][PlaywrightSystemRequirements].  

Playwright sollte Benutzern anderer Browsertestframeworks wie [WebDriver][WebDriverChromiumMain] oder [Puppeteer vertraut sein.][PuppeteerMain]  Sie erstellen eine Instanz des Browsers, öffnen eine Seite und bearbeiten sie dann mit der [Playwright-API.][PlaywrightAPIReference]  Im folgenden Codeausschnitt startet Playwright Microsoft Edge \(Chromium\), navigiert zu und speichert `https://www.microsoft.com/edge` einen Screenshot als `example.png` .  

Kopieren Sie den folgenden Codeausschnitt, und speichern Sie ihn unter `example.js` .  

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

Ändern `executablePath` Sie, um auf Ihre Installation von Microsoft Edge \(Chromium\) zu verweisen.  Unter macOS sollte beispielsweise der für `executablePath` Microsoft Edge Canary auf festgelegt `/Applications/Microsoft\ Edge\ Canary.app/` werden.  Navigieren Sie zu und kopieren Sie den ausführbaren Pfad auf dieser Seite, oder installieren Sie das `executablePath` `edge://version` [Edge-Paths-Paket][npmEdgePaths] mit dem folgenden Befehl. ****  

```shell
npm i edge-paths
```  

Der folgende Codeausschnitt verwendet das [Edge-Paths-Paket,][npmEdgePaths] um programmgesteuert den Pfad zu Ihrer Installation von Microsoft Edge \(Chromium\) auf Ihrem Betriebssystem zu finden.  

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```  

Legen Sie schließlich `executablePath: EDGE_PATH` in . `example.js`  Speichern Sie Ihre Änderungen.  

> [!NOTE]
> Microsoft Edge \(EdgeHTML\) funktioniert nicht mit Playwright.  Sie müssen die [Microsoft Edge \(Chromium\)][MicrosoftEdgeDownload] installieren, um dieses Beispiel weiter zu verwenden.  

Führen Sie `example.js` jetzt über die Befehlszeile aus.  

```shell
node example.js
```  

Playwright startet Microsoft Edge, navigiert zu `https://www.microsoft.com/edge` und speichert einen Screenshot der Seite.  Sie können die Seitengröße mit [page.setViewportSize() anpassen.][PlaywrightAPIPageSetViewport]  

:::image type="complex" source="../media/playwright-example.png" alt-text="Die example.png datei, die von example.js" lightbox="../media/playwright-example.png":::
    Die `example.png` datei, die von `example.js`  
:::image-end:::  

`example.js` ist nur eine einfache Demonstration der von Playwright aktivierten Automatisierungs- und Testszenarien.  Um Screenshots in mehreren Webbrowsern zu erstellen, ändern Sie den folgenden Code.  

*   Chromium  `await chromium.launch()`  
*   Firefox  `await firefox.launch()`  
*   WebKit  `await webkit.launch()`  

Weitere Informationen zu Playwright finden Sie auf der [Playwright-Website.][|::ref6::|Main]  Sehen Sie sich [das Playwright-Repository auf GitHub.][PlaywrightRepo]  Um Ihr Feedback zum Automatisieren und Testen Ihrer Website oder App mit Playwright zu teilen, geben Sie [ein Problem ein.][PlaywrightRepoNewIssue]  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

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
