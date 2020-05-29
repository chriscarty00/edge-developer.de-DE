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
# <span data-ttu-id="4de27-104">Debugger für Microsoft Edge-vs-Code Erweiterung</span><span class="sxs-lookup"><span data-stu-id="4de27-104">Debugger for Microsoft Edge VS Code extension</span></span>

<span data-ttu-id="4de27-105">Mit dem [Debugger für Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs Code Extension können Sie den Front-End-JavaScript-Code Zeile für Zeile Debuggen und `console.log()` alle Anweisungen direkt aus [Visual Studio-Code](https://code.visualstudio.com/)anzeigen!</span><span class="sxs-lookup"><span data-stu-id="4de27-105">With the [Debugger for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension, you can debug your front-end JavaScript code line by line and see `console.log()` statements all directly from [Visual Studio Code](https://code.visualstudio.com/)!</span></span>

![GIF des Debuggers für Edge-vs-Code Erweiterung am Arbeitsplatz](./media/debugger-for-edge.gif)

## <span data-ttu-id="4de27-107">Starten von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4de27-107">Launching Microsoft Edge</span></span>

<span data-ttu-id="4de27-108">Navigieren Sie `Ctrl`  +  `Shift`  +  `D` `Command`  +  `Shift`  +  `D` in der **Aktivitäts Leiste**zur Ansicht Debuggen (unter Windows oder Mac).</span><span class="sxs-lookup"><span data-stu-id="4de27-108">Navigate to the Debug view (`Ctrl` + `Shift` + `D` on Windows or `Command` + `Shift` + `D` on Mac) in the **Activity Bar**.</span></span> <span data-ttu-id="4de27-109">Wenn Sie keine Konfigurationen im vs-Code haben, drücken Sie `F5` Windows oder Mac, oder klicken Sie auf die grüne Schaltfläche " **Wiedergabe** ".</span><span class="sxs-lookup"><span data-stu-id="4de27-109">If you do not have any configurations in VS Code, press `F5` on Windows or Mac or click the green **Play** button.</span></span> <span data-ttu-id="4de27-110">Wählen Sie in der Dropdownliste "Edge" aus.</span><span class="sxs-lookup"><span data-stu-id="4de27-110">Select "Edge" in the dropdown.</span></span> <span data-ttu-id="4de27-111">Nun wird eine **JSON-Start** Datei mit der folgenden Konfiguration angezeigt:</span><span class="sxs-lookup"><span data-stu-id="4de27-111">You will now see a **launch.json** file with the following configuration:</span></span>

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

<span data-ttu-id="4de27-112">Wenn Sie nun `F5` auf Windows oder Mac drücken oder erneut auf die grüne **Wiedergabe** -Schaltfläche klicken, wird mit dem vs-Code Microsoft Edge (EdgeHTML) gestartet, und Sie können jedes Webprojekt, das Sie auf Port **8080** ausführen, direkt aus dem vs-Code heraus Debuggen!</span><span class="sxs-lookup"><span data-stu-id="4de27-112">If you now press `F5` on Windows or Mac or click the green **Play** button again, VS Code will launch Microsoft Edge (EdgeHTML) and you will be able to debug any web project you have running on port **8080** directly from VS Code!</span></span>

### <span data-ttu-id="4de27-113">Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="4de27-113">Microsoft Edge (Chromium)</span></span>

<span data-ttu-id="4de27-114">Wenn Sie Microsoft Edge (Chrom), die nächste Version von Microsoft Edge, anstatt Microsoft Edge (EdgeHTML) starten möchten, fügen `version` Sie Ihrer vorhandenen Konfiguration einfach ein Attribut mit der Version von Microsoft Edge (Chrom) hinzu, die Sie starten möchten ( `dev` , `beta` oder `canary` ).</span><span class="sxs-lookup"><span data-stu-id="4de27-114">If you want to launch Microsoft Edge (Chromium), the next version of Microsoft Edge, instead of Microsoft Edge (EdgeHTML), simply add a `version` attribute to your existing configuration with the version of Microsoft Edge (Chromium) you want to launch (`dev`, `beta`, or `canary`).</span></span> <span data-ttu-id="4de27-115">In der folgenden Konfiguration wird die Canary-Version von Microsoft Edge (Chrom) gestartet:</span><span class="sxs-lookup"><span data-stu-id="4de27-115">The configuration below will launch the Canary version of Microsoft Edge (Chromium):</span></span>

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

## <span data-ttu-id="4de27-116">Anfügen an Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4de27-116">Attaching to Microsoft Edge</span></span>

<span data-ttu-id="4de27-117">Sie können auch vs-Code an Microsoft Edge (Chrom) anfügen.</span><span class="sxs-lookup"><span data-stu-id="4de27-117">You can also attach VS Code to Microsoft Edge (Chromium).</span></span> <span data-ttu-id="4de27-118">Führen Sie auf Ihrem Terminal den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="4de27-118">From your terminal, run the following command:</span></span>

`start msedge --remote-debugging-port=9222`

<span data-ttu-id="4de27-119">Fügen Sie die folgende Konfiguration zu Ihrer **Start. JSON-** Datei hinzu:</span><span class="sxs-lookup"><span data-stu-id="4de27-119">Add the configuration below to your **launch.json** file:</span></span>

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```

<span data-ttu-id="4de27-120">Wenn Sie diese Konfiguration jetzt ausführen, wird vs-Code an Microsoft Edge (Chrom) angefügt, und Sie können mit dem Debuggen beginnen!</span><span class="sxs-lookup"><span data-stu-id="4de27-120">If you now run this configuration, VS Code will attach to Microsoft Edge (Chromium) and you can start debugging!</span></span>

## <span data-ttu-id="4de27-121">Feedback senden</span><span class="sxs-lookup"><span data-stu-id="4de27-121">Feedback</span></span>

<span data-ttu-id="4de27-122">Senden Sie uns Ihr Feedback, indem Sie [ein Problem](https://github.com/Microsoft/vscode-edge-debug2/issues/new) mit dem [GitHub-Repo](https://github.com/Microsoft/vscode-edge-debug2)dieser Erweiterung einreichen.</span><span class="sxs-lookup"><span data-stu-id="4de27-122">Send us your feedback by [filing an issue](https://github.com/Microsoft/vscode-edge-debug2/issues/new) against this extension's [GitHub repo](https://github.com/Microsoft/vscode-edge-debug2).</span></span> <span data-ttu-id="4de27-123">Fügen Sie die Debug-Adapter Protokolldatei ein, die für jeden Testlauf im Verzeichnis% Temp% mit dem Namen erstellt wird `vscode-edge-debug2.txt` .</span><span class="sxs-lookup"><span data-stu-id="4de27-123">Please include the debug adapter log file, which is created for each run in the %temp% directory with the name `vscode-edge-debug2.txt`.</span></span> <span data-ttu-id="4de27-124">Sie können diese Datei in einen Problem Kommentar ziehen, um Sie in GitHub hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="4de27-124">You can drag this file into an issue comment to upload it to GitHub.</span></span>

<span data-ttu-id="4de27-125">Wenn Sie uns helfen möchten, diese Erweiterung besser zu gestalten, freuen wir uns über Ihre Beiträge!</span><span class="sxs-lookup"><span data-stu-id="4de27-125">If you want to help us make this extension better, we welcome your contributions!</span></span> <span data-ttu-id="4de27-126">Sie finden alles, was Sie für den Einstieg in [unser GitHub-Repo](https://github.com/Microsoft/vscode-edge-debug2)benötigen.</span><span class="sxs-lookup"><span data-stu-id="4de27-126">You can find everything you need to get started in [our GitHub repo](https://github.com/Microsoft/vscode-edge-debug2).</span></span>