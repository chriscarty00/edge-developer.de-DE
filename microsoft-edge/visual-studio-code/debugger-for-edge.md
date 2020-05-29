---
description: Debuggen von Microsoft Edge (Chrom) und Microsoft Edge (EdgeHTML) aus vs-Code
title: Debuggen von Microsoft Edge (Chrom) aus vs-Code
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/10/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, vs-Code, Visual Studio-Code, Debugger
ms.openlocfilehash: 7d8d2f87500b3e81866b49de32db91c0a525baf2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568670"
---
# Debugger für Microsoft Edge-vs-Code Erweiterung

Mit dem [Debugger für Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs Code Extension können Sie den Front-End-JavaScript-Code Zeile für Zeile Debuggen und `console.log()` alle Anweisungen direkt aus [Visual Studio-Code](https://code.visualstudio.com/)anzeigen!

![GIF des Debuggers für Edge-vs-Code Erweiterung am Arbeitsplatz](./media/debugger-for-edge.gif)

## Starten von Microsoft Edge

Navigieren Sie `Ctrl`  +  `Shift`  +  `D` `Command`  +  `Shift`  +  `D` in der **Aktivitäts Leiste**zur Ansicht Debuggen (unter Windows oder Mac). Wenn Sie keine Konfigurationen im vs-Code haben, drücken Sie `F5` Windows oder Mac, oder klicken Sie auf die grüne Schaltfläche " **Wiedergabe** ". Wählen Sie in der Dropdownliste "Edge" aus. Nun wird eine **JSON-Start** Datei mit der folgenden Konfiguration angezeigt:

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "type": "edge",
            "request": "launch",
            "name": "Launch Edge against localhost",
            "url": "http://localhost:8080",
            "webRoot": "${workspaceFolder}"
        }
    ]
}
```

Wenn Sie nun `F5` auf Windows oder Mac drücken oder erneut auf die grüne **Wiedergabe** -Schaltfläche klicken, wird mit dem vs-Code Microsoft Edge (EdgeHTML) gestartet, und Sie können jedes Webprojekt, das Sie auf Port **8080** ausführen, direkt aus dem vs-Code heraus Debuggen!

### Microsoft Edge (Chromium)

Wenn Sie Microsoft Edge (Chrom), die nächste Version von Microsoft Edge, anstatt Microsoft Edge (EdgeHTML) starten möchten, fügen `version` Sie Ihrer vorhandenen Konfiguration einfach ein Attribut mit der Version von Microsoft Edge (Chrom) hinzu, die Sie starten möchten ( `dev` , `beta` oder `canary` ). In der folgenden Konfiguration wird die Canary-Version von Microsoft Edge (Chrom) gestartet:

```json
{
    "type": "edge",
    "request": "launch",
    "version": "canary",
    "name": "Launch Edge against localhost",
    "url": "http://localhost:8080",
    "webRoot": "${workspaceFolder}"
}
```

## Anfügen an Microsoft Edge

Sie können auch vs-Code an Microsoft Edge (Chrom) anfügen. Führen Sie auf Ihrem Terminal den folgenden Befehl aus:

`start msedge --remote-debugging-port=9222`

Fügen Sie die folgende Konfiguration zu Ihrer **Start. JSON-** Datei hinzu:

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```

Wenn Sie diese Konfiguration jetzt ausführen, wird vs-Code an Microsoft Edge (Chrom) angefügt, und Sie können mit dem Debuggen beginnen!

## Feedback senden

Senden Sie uns Ihr Feedback, indem Sie [ein Problem](https://github.com/Microsoft/vscode-edge-debug2/issues/new) mit dem [GitHub-Repo](https://github.com/Microsoft/vscode-edge-debug2)dieser Erweiterung einreichen. Fügen Sie die Debug-Adapter Protokolldatei ein, die für jeden Testlauf im Verzeichnis% Temp% mit dem Namen erstellt wird `vscode-edge-debug2.txt` . Sie können diese Datei in einen Problem Kommentar ziehen, um Sie in GitHub hochzuladen.

Wenn Sie uns helfen möchten, diese Erweiterung besser zu gestalten, freuen wir uns über Ihre Beiträge! Sie finden alles, was Sie für den Einstieg in [unser GitHub-Repo](https://github.com/Microsoft/vscode-edge-debug2)benötigen.