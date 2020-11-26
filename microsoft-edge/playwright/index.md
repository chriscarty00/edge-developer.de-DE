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
# Dramatiker  

[Dramatiker][|::ref1::|Main] ist eine [Node.js][NodejsMain] Bibliothek zum Automatisieren von [Chrom][ChromiumHome], [Firefox][FirefoxMain]und [WebKit][|::ref2::|Main] mit einer einzigen API.  Dramatiker wurde entwickelt, um browserübergreifende webautomatisierungen zu ermöglichen, die immer grün, fähig, zuverlässig und schnell sind.  Da [Microsoft Edge auf der Open-Source-Chrom-Webplattform][MicrosoftBlogsWindowsExperience20181206]basiert, ist Dramatiker auch in der Lage, Microsoft Edge zu automatisieren.  

Writer startet standardmäßig [headless-Browser][WikiHeadlessBrowser] .  Headless-Browser zeigen keine Benutzeroberfläche an, daher müssen Sie stattdessen die Befehlszeile verwenden.  Sie können auch Writer so konfigurieren, dass der vollständige \ (nicht-headless \) Microsoft Edge ausgeführt wird.  

Wenn Sie Writer installieren, downloadet das Installationsprogramm standardmäßig [Chrom][ChromiumHome], [Firefox][FirefoxMain]und [WebKit][|::ref3::|Main].  Wenn Sie Microsoft Edge \ (Chrom \) ebenfalls installiert haben, benötigt Dramatiker nur eine einzeilige Codeänderung, um Ihre Website oder app in Microsoft Edge zu testen.  Zum Herunterladen von Microsoft Edge \ (Chrom \) navigieren Sie zu [Microsoft Edge herunterladen][MicrosoftEdgeDownload].  

## Installieren des Dramatikers  

Installieren Sie [Dramatiker][|::ref4::|Main] , um Ihre Website oder App mit dem folgenden Befehl zu testen.  

```shell
npm i playwright
```  

## Starten von Microsoft Edge mit Dramatiker  

> [!NOTE]
> Für [Dramatiker][|::ref5::|Main] ist Node.js Version 10,17 oder höher erforderlich. Führen `node -v` Sie über die Befehlszeile aus, um sicherzustellen, dass Sie über eine kompatible Version von Node.js verfügen.  Die Browser-Binaries für Chrom, Firefox und WebKit funktionieren über Windows, macOS und Linux. Weitere Informationen finden Sie unter [System Anforderungen für Dramatiker][PlaywrightSystemRequirements].  

Dramatiker sollten Benutzern anderer Browsertest-Frameworks wie [WebDriver][WebDriverChromiumMain] oder [Puppenspieler][PuppeteerMain]vertraut sein.  Erstellen Sie eine Instanz des Browsers, öffnen Sie eine Seite, und bearbeiten Sie Sie dann mit der [Dramatiker-API][PlaywrightAPIReference].  Im folgenden Codeausschnitt startet Dramatiker Microsoft Edge \ (Chrom \), navigiert zu `https://www.microsoft.com/edge` und speichert einen Screenshot als `example.png` .  

Kopieren Sie den folgenden Codeausschnitt, und speichern Sie ihn als `example.js` .  

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

Ändern `executablePath` Sie, um auf Ihre Installation von Microsoft Edge (Chrom \) zu verweisen.  So sollte beispielsweise unter macOS `executablePath` für Microsoft Edge Canary auf festgesetzt werden `/Applications/Microsoft\ Edge\ Canary.app/` .  Um das zu finden `executablePath` , navigieren Sie zu dem `edge://version` **ausführbaren Pfad** auf dieser Seite, und kopieren Sie ihn, oder installieren Sie das [Edge-Paths-][npmEdgePaths] Paket mit dem folgenden Befehl.  

```shell
npm i edge-paths
```  

Der folgende Codeausschnitt verwendet das [Edge-Paths-][npmEdgePaths] Paket zum programmgesteuerten Auffinden des Pfads zu Ihrer Installation von Microsoft Edge \ (Chrom \) auf Ihrem Betriebssystem.  

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```  

Setzen Sie abschließend `executablePath: EDGE_PATH` ein `example.js` .  Speichern Sie Ihre Änderungen.  

> [!NOTE]
> Microsoft Edge \ (EdgeHTML \) funktioniert nicht mit Dramatiker.  Sie müssen [Microsoft Edge \ (Chrom \)][MicrosoftEdgeDownload] installieren, um weiterhin diesem Beispiel folgen zu können.  

Nun `example.js` über die Befehlszeile ausgeführt werden.  

```shell
node example.js
```  

Dramatiker startet Microsoft Edge, navigiert zu `https://www.microsoft.com/edge` und speichert einen Screenshot der Seite.  Sie können die Seitengröße mit [Page. setViewportSize ()][PlaywrightAPIPageSetViewport]anpassen.  

:::image type="complex" source="../media/playwright-example.png" alt-text="Die von example.js erstellte example.png-Datei" lightbox="../media/playwright-example.png":::
    Die `example.png` Datei, die von `example.js`  
:::image-end:::  

`example.js` ist nur eine einfache Demonstration der von Dramatiker ermöglichten Automatisierungs-und Testszenarien.  Wenn Sie Screenshots in mehreren Webbrowsern erstellen möchten, ändern Sie den folgenden Code.  

*   Chromium  `await chromium.launch()`  
*   Firefox  `await firefox.launch()`  
*   WebKit  `await webkit.launch()`  

Weitere Informationen zu Dramatiker finden Sie auf der [Dramatiker-Website][|::ref6::|Main].  Schauen Sie sich das  [Dramatiker-Repo][PlaywrightRepo] auf GitHub an.  Wenn Sie Ihr Feedback zum Automatisieren und Testen Ihrer Website oder App mit Dramatiker freigeben möchten, können Sie [ein Problem einreichen][PlaywrightRepoNewIssue].  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

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
