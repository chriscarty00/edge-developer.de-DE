---
description: Microsoft Edge (Chrom) und Visual Studio-Code
title: Visual Studio Code
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/12/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, vs-Code, Visual Studio-Code, Debugger, webhint
ms.openlocfilehash: 94148864edbd43adbe2dc9f3d0c2fa0c1f7f0b43
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568673"
---
# Visual Studio Code

[Visual Studio-Code](https://code.visualstudio.com/Docs) ist ein leichter, aber leistungsstarker Quellcode-Editor, der auf dem Desktop ausgeführt wird und für Windows, macOS und Linux verfügbar ist. Es bietet integrierte Unterstützung für JavaScript, Script und Node. js, damit es ein tolles Tool für Web-Entwickler ist! Wechseln Sie zu [dieser Seite](https://code.visualstudio.com/) , um Visual Studio-Code herunterzuladen, wenn Sie ihn noch nicht verwenden.

## Extensions

<!-- We want to put something like the tiles for extensions VS Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page. I think it's a web page. I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->

Wenn Sie eine der unten hervorgehobenen Erweiterungen erwerben möchten, navigieren Sie in vs-Code zu Erweiterungen ( `Ctrl`  +  `Shift`  +  `X` unter Windows oder `Command`  +  `Shift`  +  `X` Mac).

Durchsuchen Sie den Marktplatz nach der jeweiligen Erweiterung, und wählen Sie **Installieren**aus.

![Installieren des Debuggers für Microsoft Edge vs Code Extension](./media/vscode-debugger-install.png)

## Debugger für Microsoft Edge

Debuggen Sie Ihre Front-End-JavaScript-Code Zeile für Zeile, und zeigen Sie `console.log()` Anweisungen direkt in [Visual Studio-Code](https://code.visualstudio.com/) mit der Erweiterung [Debugger für Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs-Code an!

Verwenden Sie den [Debugger für Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs Code Extension zum Starten oder Anfügen an Microsoft Edge (EdgeHTML) und Microsoft Edge (Chrom). Schauen Sie sich [Diese Seite](./debugger-for-edge.md) an, um eine exemplarische Vorgehensweise zum Debuggen von Microsoft Edge aus vs-Code und Beispiel **Start. JSON** -Konfigurationen zu finden.

![GIF des Debuggers für Edge-vs-Code Erweiterung in Aktion!](./media/debugger-for-edge.gif)

## Elemente für Microsoft Edge

Indem Sie die [Elemente für Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) vs Code Extension hinzufügen, können Sie das Tool Elemente des Browsers in Visual Studio-Code verwenden. Durch Starten oder Anfügen stellt das elementtool eine Verbindung mit einer Instanz von Microsoft Edge her, zeigt die HTML-Laufzeitstruktur an und ermöglicht Ihnen, das Layout zu ändern oder Formatierungsprobleme zu beheben.

Weitere Informationen finden Sie auf [dieser Seite](./elements-for-edge.md).

![GIF der Elemente für Edge-vs-Code Erweiterung in Aktion!](./media/elements-for-edge.gif)

## webhint

Verwenden Sie [webhint](https://webhint.io), ein anpassbares linting-Tool, um die Barrierefreiheit, die Leistung, die browserübergreifende Kompatibilität, die PWA-Kompatibilität und die Sicherheit Ihrer Website zu verbessern. Sie überprüft Ihren Code auf bewährte Methoden und häufige Fehler. Dieses Open-Source-Projekt, das ursprünglich vom Microsoft Edge-Team entwickelt wurde, ist jetzt Teil der [OpenJS-Foundation](https://openjsf.org/). Das Microsoft Edge-Team trägt weiterhin zu webhint neben Webentwicklern in der Community bei.

![Screenshot der webhint vs-Code Erweiterung](./media/webhint-extension.png)

Identifizieren und beheben Sie Probleme in HTML, CSS, JavaScript, Manuskript und mehr, indem Sie die [webhint-Erweiterung für vs-Code](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint)hinzufügen. Hinweise werden als Inline Unterstriche angezeigt und im Problembereich zusammengefasst.

Weitere Informationen finden Sie unter [so wird es gemacht: Verwenden von webhint in Visual Studio-Code](./webhint.md).
