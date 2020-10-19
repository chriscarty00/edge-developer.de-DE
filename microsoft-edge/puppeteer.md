---
description: Verwenden von Puppenspieler zum Automatisieren und testen in Microsoft Edge
title: Puppeteer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Web-Entwicklung, Entwickler, Tools, Automatisierung, Test
ms.openlocfilehash: bef3f0d7472f7bc595998829546fb540041f20fc
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986157"
---
# Puppeteer  

[Marionetten][|::ref1::|Main] ist eine [Knoten][NodejsMain] Bibliothek, die eine allgemeine API zur Steuerung von Microsoft Edge (Chrom \) über das [devtools-Protokoll][GithubChromedevtoolsProtocol]bereitstellt.  Puppenspieler läuft standardmäßig [headless][WikiHeadlessBrowser] , was bedeutet, dass Sie keine Benutzeroberfläche sehen und stattdessen die Befehlszeile verwenden müssen.  Sie können auch den Puppenspieler so konfigurieren, dass er "Full \" (nicht-headless \) Microsoft Edge oder Chromium ausführt.  

Bei der Installation von Puppenspieler downloadet das Installationsprogramm standardmäßig eine neuere Version von [Chromium][ChromiumHome], den Open-Source-Browser, [auf dem Microsoft Edge ebenfalls][MicrosoftBlogsWindowsExperience20181206]basiert.  Wenn Sie Microsoft Edge \ (Chrom \) installiert haben, können Sie die [Marionetten-Core-][PuppeteerApivscore]Version verwenden.  `puppeteer-core` ist eine vereinfachte Version von Puppenspieler, die eine vorhandene Browserinstallation wie Microsoft Edge (Chrom \) startet.  Informationen zum Herunterladen von Microsoft Edge \ (Chrom \) finden Sie unter [Herunterladen von Microsoft Edge-Insider Kanälen][MicrosoftedgeinsiderDownload].

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

`puppeteer-core` sollte Benutzern anderer Browser-Test-Frameworks wie [WebDriver][WebDriverEdgehtmlMain]vertraut sein.  Erstellen Sie eine Instanz des Browsers, öffnen Sie eine Seite, und bearbeiten Sie Sie dann mit der Marionetten-API.  Im folgenden Codebeispiel wird `puppeteer-core` Microsoft Edge (Chrom \) gestartet, navigiert zu `https://www.microsoftedgeinsider.com` und speichert einen Screenshot als `example.png` .  

Kopieren Sie das folgende Codebeispiel, und speichern Sie es als `example.js` .  

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

Nun `example.js` über die Befehlszeile ausgeführt werden.  

```shell
node example.js
```  

`puppeteer-core` startet Microsoft Edge, navigiert zu `https://www.microsoftedgeinsider.com` und speichert einen Screenshot der Seite 800px x 600px.  Sie können die Seitengröße mit [Page. setviewport ()][PuppeteerApipagesetviewport]anpassen.  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="Die von example.js erstellte example.png-Datei":::
   Abbildung 1: die `example.png` Datei, die von erstellt wurde `example.js`  
:::image-end:::  

<!--  
> ##### Figure 1  
> The `example.png` file produced by `example.js`  
> ![The example.png file produced by example.js](./media/puppeteer-example.png)  
-->  

Dies ist nur ein einfaches Beispiel für die Automatisierungs-und Testszenarien, die von Marionetten und `puppeteer-core` .  Weitere Informationen zu Puppenspielern und deren Funktionsweise finden Sie unter [Puppenspieler][|::ref2::|Main].  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

Das Microsoft Edge-Entwicklerteam freut sich, Ihr Feedback zur Verwendung von Puppenspieler `puppeteer-core` und Microsoft Edge zu hören.  Verwenden Sie das Symbol &quot; **Feedback senden** " im Microsoft Edge devtools-oder Tweet- [@EdgeDevTools][TwitterIntentTweetEdgedevtools] , damit das Microsoft Edge-Team wissen kann, was Sie denken.  


:::image type="complex" source="./devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Die von example.js erstellte example.png-Datei":::
   Abbildung 1: die `example.png` Datei, die von erstellt wurde `example.js`  
:::image-end:::  

<!--  
> ##### Figure 1  
> The `example.png` file produced by `example.js`  
> ![The example.png file produced by example.js](./media/puppeteer-example.png)  
-->  

Dies ist nur ein einfaches Beispiel für die Automatisierungs-und Testszenarien, die von Marionetten und `puppeteer-core` .  Weitere Informationen zu Puppenspielern und deren Funktionsweise finden Sie unter [Puppenspieler][|::ref2::|Main].  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

Das Microsoft Edge-Entwicklerteam freut sich, Ihr Feedback zur Verwendung von Puppenspieler `puppeteer-core` und Microsoft Edge zu hören.  Verwenden Sie das Symbol &quot; **Feedback senden** "  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "Marionetten-vs. Puppenspieler-Core | Puppeteer"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "Page. setviewport (Viewport) | Puppeteer"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools-Poste einen Tweet | Twitter"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Headless-Browser | Wikipedia"  
