---
description: Features, die dem Microsoft Edge (Chrom)-devtools im März 2019 hinzugefügt wurden
title: Neuerungen in der Microsoft Edge-devtools (Chrom) im März 2019
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: bf1919b0ab46df378880d664dd4e59aee96605e5
ms.sourcegitcommit: 24430258f363b7dd85f7067afd4565bf102b4a1f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2020
ms.locfileid: "10645322"
---
# Neuerungen in Microsoft Edge (Chrom) devtools

Vielen Dank, dass Sie eine Vorschau der nächsten Version von Microsoft Edge ausprobiert haben! Mit dieser Version haben wir eine wichtige Schicht in der zugrunde liegenden Webplattform von Microsoft Edge durch die Übernahme des Open-Source-Projekts Chromium übernommen. Mit dieser Änderung ist es einfacher für Sie, ihre Websites in Microsoft Edge zu erstellen und zu testen und sicherzustellen, dass diese weiterhin wie erwartet funktionieren, auch wenn Ihre Benutzer in einem anderen Chrom basierten Browser wie Google Chrome, Vivaldi, Opera oder Brave Surfen.

## Das neue Microsoft Edge (Chrom)-devtools

Wenn Sie Microsoft Edge Auschecken und sich hauptsächlich in einem Chrom basierten Browser entwickeln, sollten Sie sich wie zu Hause fühlen. Die Microsoft Edge (Chrom)-Entwicklertools sind genau wie die Entwicklertools, die Sie bereits kennen und verwenden!

![Microsoft Edge (Chrom) devtools](./media/devtools.png)

Wenn Sie die nächste Version von Microsoft Edge Auschecken und Sie hauptsächlich in Microsoft Edge (EdgeHTML) entwickelt haben, haben wir einige hervorragende neue Tools, mit denen wir hoffen, dass es Ihnen einfacher und schneller fällt, ihre Websites in Microsoft Edge zu erstellen und zu testen! Weitere Informationen zu diesen neuen Tools finden Sie [im devtools-Leitfaden zu Microsoft Edge (Chrom)](../devtools-guide-chromium.md).

## Neue dunkle und helle Designs für das devtools

Wir haben einige neue düstere und helle Designs für die devtools entwickelt, die Ihnen gefallen werden. Standardmäßig verwendet die Microsoft Edge-devtools (Chrom) das dunkle Design. Wenn Sie das Design des devtools ändern möchten, drücken Sie `Fn`  +  `F1` Windows oder Mac, oder navigieren Sie mithilfe der `...` Schaltfläche in der oberen rechten Ecke des devtools zu Einstellungen.

![Hauptmenü von Microsoft Edge (Chrom) devtools](./media/devtools-main-menu.png)

In den Einstellungen können Sie das Design des devtools ändern. Wenn Ihnen die Darstellung des devtools in Ihrem Chrom basierten Browser gefallen hat, können Sie die Microsoft Edge (Chrom)-devtools genauso aussehen lassen, indem Sie die Designs " **dunkel (Chrom)** " oder " **hell (Chrom** )" auswählen. 

## Debuggen von Microsoft Edge (Chrom) aus vs-Code

Mit dem [Debugger für Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs Code Extension können Sie jetzt sowohl Microsoft Edge (EdgeHTML) als auch Microsoft Edge (Chrom) direkt aus vs-Code Debuggen!

![Debugger für Edge-vs-Code Erweiterung](./media/vscode-debugger.png)

Um Microsoft Edge (Chrom) anstelle von Microsoft Edge (EdgeHTML) aus vs-Code zu starten, müssen Sie `version` Ihrem vorhandenen **launch.jsauf** Konfiguration mit der Version von Microsoft Edge (Chrom), die Sie starten möchten ( `dev` , `beta` oder), ein Attribut hinzufügen `canary` . Im folgenden finden Sie ein Beispiel **launch.jszur** Konfiguration, mit der die Canary-Version von Microsoft Edge (Chrom) auf [Bing.com](https://www.bing.com/)gestartet wird:

```json
{
    "type": "edge",
    "request": "launch",
    "version": "canary",
    "name": "Launch Microsoft Edge (Chromium) Canary against Bing",
    "url": "https://bing.com"
}
```

Weitere Informationen finden Sie unter [Debuggen von Microsoft Edge (Chrom) aus vs-Code](../visual-studio-code/debugger-for-edge.md).

## Aktualisierung des Edge devtools-Protokolls

Mit der Verschiebung in der zugrunde liegenden Webplattform von Microsoft Edge erhält das Edge devtools-Protokoll keine weiteren Updates. Die Microsoft Edge-devtools (Chrom) verwendet das Chrom-devtools-Protokoll oder CDP. Informationen zum Verweisen auf die Dokumentation zu den Domänen und Methoden in CDP finden Sie [im CDP-Viewer](https://chromedevtools.github.io/devtools-protocol/tot/Accessibility).

In der nächsten Version von Microsoft Edge werden alle Methoden, mit denen das Präfix vorangestellt wurde, `ms` nicht unterstützt. Weitere Informationen zur Verwendung von CDP in Microsoft Edge (Chrom) finden Sie unter [devtools-Protokoll (Chrom)](../devtools-protocol-chromium.md).

## Bekannte Probleme

Viele Links vom Microsoft Edge (Chrom)-devtools zu Inhalten, die auf Websites von Drittanbietern gehostet werden, wurden vorübergehend entfernt. Sobald wir diese Links ersetzen können, werden wir Sie wieder zum devtools hinzufügen.


Beim Debuggen von Webinhalten auf einem Android-Gerät von Microsoft Edge (Chrom) ist die Version des devtools, die beim Klicken auf die Schaltfläche "über **prüfen** " vom Tool " **Remote Geräte** " gestartet wird, möglicherweise nicht mit der Version des Browsers auf Ihrem Android-Gerät identisch. Infolgedessen werden möglicherweise neue Features im devtools angezeigt, die nicht für den Browser auf Ihrem Android-Gerät funktionieren. Wenn Ihnen das auffallen sollte, würden wir uns freuen, darüber zu hören, bitte geben Sie uns [Feedback](../devtools-guide-chromium.md#getting-in-touch-with-the-microsoft-edge-devtools-team)!

Schließlich unterstützt Visual Studio unter Windows und Mac noch nicht Microsoft Edge (Chrom). Melden Sie sich [hier](https://visualstudio.microsoft.com/vs/preview/) an, um als erster zu erfahren, wann wir eine Preview-Version von Visual Studio haben, die JavaScript-Debugging in Microsoft Edge (Chrom) für ASP.net-Projekte unterstützt.  
