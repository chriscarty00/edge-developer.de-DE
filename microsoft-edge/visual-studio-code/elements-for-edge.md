---
description: Verwenden von Elementen für Microsoft Edge (Chrom) aus vs-Code
title: Elemente für Microsoft Edge (Chrom) aus vs-Code
author: erdraud
ms.author: erdraud
ms.date: 08/08/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, vs-Code, Visual Studio-Code, Elemente
ms.openlocfilehash: 4875a4665fe1561ecf587a050bbd44e116d9ce5e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568674"
---
# <span data-ttu-id="c1e92-104">Elemente für Microsoft Edge vs Code Extension</span><span class="sxs-lookup"><span data-stu-id="c1e92-104">Elements for Microsoft Edge VS Code extension</span></span>

<span data-ttu-id="c1e92-105">Indem Sie die [Elemente für Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) vs Code Extension hinzufügen, können Sie das Tool Elemente des Browsers in [Visual Studio-Code](https://code.visualstudio.com/)verwenden.</span><span class="sxs-lookup"><span data-stu-id="c1e92-105">By adding the [Elements for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) VS Code extension, you can use the browser's Elements tool from within [Visual Studio Code](https://code.visualstudio.com/).</span></span> <span data-ttu-id="c1e92-106">Durch Starten oder Anfügen stellt das elementtool eine Verbindung mit einer Instanz von Microsoft Edge her, zeigt die HTML-Laufzeitstruktur an und ermöglicht Ihnen, das Layout zu ändern oder Formatierungsprobleme zu beheben.</span><span class="sxs-lookup"><span data-stu-id="c1e92-106">By either launching or attaching, the Elements tool will connect to an instance of Microsoft Edge, display the runtime HTML structure, and allow you to alter the layout or fix styling issues.</span></span>

![GIF der Elemente für Edge-vs-Code Erweiterung am Arbeitsplatz](./media/elements-for-edge.gif)

## <span data-ttu-id="c1e92-108">Starten von Microsoft Edge aus der Elements-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="c1e92-108">Launching Microsoft Edge From the Elements extension</span></span> 

<span data-ttu-id="c1e92-109">Navigieren Sie zu Elementen in der **Aktivitäts Leiste**.</span><span class="sxs-lookup"><span data-stu-id="c1e92-109">Navigate to Elements in the **Activity Bar**.</span></span> <span data-ttu-id="c1e92-110">Neben der Schaltfläche "Elemente für Microsoft Edge: Ziele" gibt es ein Pluszeichen, mit dem der Browser für Ihre APP geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="c1e92-110">Next to where it says "Elements for Microsoft Edge: Targets," there is a plus sign that will open the browser for your app.</span></span> <span data-ttu-id="c1e92-111">Wenn Sie die Option *about: blank* ausgewählt haben, müssen Sie im Browser zu Ihrer Web-App navigieren, damit Sie im vs-Code im Bedienfeld "Elemente" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c1e92-111">If you selected the *about:blank* option, you will have to navigate to your web app in the browser for it to appear in the Elements panel in VS Code.</span></span>

## <span data-ttu-id="c1e92-112">Starten von Microsoft Edge aus der Ansicht "Debuggen"</span><span class="sxs-lookup"><span data-stu-id="c1e92-112">Launching Microsoft Edge from the Debug view</span></span>

<span data-ttu-id="c1e92-113">Wenn Sie mit der Debugansicht in Visual Studio-Code vertraut sind, können Sie über dieses Tool auf Elemente zugreifen.</span><span class="sxs-lookup"><span data-stu-id="c1e92-113">If you are accustomed to using the Debug view in Visual Studio Code, you can access Elements from that tool.</span></span> <span data-ttu-id="c1e92-114">Navigieren Sie zur Ansicht Debuggen ( `Ctrl`  +  `Shift`  +  `D` unter Windows oder `Command`  +  `Shift`  +  `D` Mac).</span><span class="sxs-lookup"><span data-stu-id="c1e92-114">Navigate to the Debug view (`Ctrl` + `Shift` + `D` on Windows or `Command` + `Shift` + `D` on Mac).</span></span> 

<span data-ttu-id="c1e92-115">Wenn Sie keine Konfigurationen im vs-Code haben, drücken Sie `F5` Windows oder Mac, oder klicken Sie auf die grüne Schaltfläche " **Wiedergabe** ".</span><span class="sxs-lookup"><span data-stu-id="c1e92-115">If you do not have any configurations in VS Code, press `F5` on Windows or Mac or click the green **Play** button.</span></span> <span data-ttu-id="c1e92-116">Wählen Sie in der Dropdownliste "Edge" aus.</span><span class="sxs-lookup"><span data-stu-id="c1e92-116">Select "Edge" in the dropdown.</span></span> <span data-ttu-id="c1e92-117">Nun wird eine **JSON-Start** Datei mit der folgenden Konfiguration angezeigt:</span><span class="sxs-lookup"><span data-stu-id="c1e92-117">You will now see a **launch.json** file with the following configuration:</span></span>

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            
            "name": "Launch Microsoft Edge and open the Elements tool",
            "request": "launch",
            "type": "vscode-edge-devtools.debug",
            "url": "http://localhost:3000"
        
        }
    ]
}
```

<span data-ttu-id="c1e92-118">Nachdem Sie nun die richtige Konfiguration geladen haben, drücken Sie entweder `F5` auf Windows oder Mac, oder klicken Sie auf die grüne **Wiedergabe** Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="c1e92-118">Now that you have loaded the correct configuration, either press `F5` on Windows or Mac or click the green **Play** button.</span></span> <span data-ttu-id="c1e92-119">Das elementtool, mit dem Sie über den Microsoft Edge-Browser vertraut sind, wird nun im vs-Code gestartet, sodass Sie auf einen Screencast Ihres Browsers zugreifen und die Komponenten Ihrer Seite untersuchen können.</span><span class="sxs-lookup"><span data-stu-id="c1e92-119">The Elements tool you are familiar with from the Microsoft Edge browser will now launch in VS Code, allowing you to access a screencast of your browser and examine the components of your page.</span></span>

## <span data-ttu-id="c1e92-120">Anfügen an Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c1e92-120">Attaching to Microsoft Edge</span></span>
<span data-ttu-id="c1e92-121">Wenn Sie einen vs-Code an eine Instanz von Microsoft Edge (Chrom) anfügen möchten, müssen Sie den Browser starten, indem Sie den folgenden Befehl in Ihrem Terminal ausführen:</span><span class="sxs-lookup"><span data-stu-id="c1e92-121">If you'd like to attach VS Code to an instance of Microsoft Edge (Chromium), you must start the browser by running the following command from your teminal:</span></span>

`start msedge --remote-debugging-port=9222`

<span data-ttu-id="c1e92-122">Nachdem die APP gestartet wurde, fügen Sie die folgende Konfiguration zu Ihrer **Start. JSON** -Datei hinzu:</span><span class="sxs-lookup"><span data-stu-id="c1e92-122">Once the app has launched, add the configuration below to your **launch.json** file:</span></span>

```json
{
    "type": "vscode-edge-devtools.debug",
    "request": "attach",
    "name": "Attach to Microsoft Edge and open the Elements tool",
    "url": "http://localhost:3000/",
    "webRoot": "${workspaceFolder}/out",
    "port": 9222
}
```

<span data-ttu-id="c1e92-123">Wählen Sie "an Microsoft Edge anfügen aus, und öffnen Sie das elementtool" aus dem Dropdownmenü des Debuggers.</span><span class="sxs-lookup"><span data-stu-id="c1e92-123">Select "Attach to Microsoft Edge and open the Elements tool" from the Debugger drop-down menu.</span></span> <span data-ttu-id="c1e92-124">Klicken Sie als nächstes entweder `F5` auf Windows oder Mac oder auf die grüne Schaltfläche " **Wiedergabe** ".</span><span class="sxs-lookup"><span data-stu-id="c1e92-124">Next, either press `F5` on Windows or Mac or click the green **Play** button.</span></span> <span data-ttu-id="c1e92-125">Mit dem vs-Code wird das elementtool gestartet, sodass Sie auf einen Screencast Ihres Browsers zugreifen, das DOM und die Formatierung der Komponenten auf der Seite überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="c1e92-125">VS Code will launch the Elements tool, allowing you to access a screencast of your browser, inspect the DOM, and the styling of the components on your page.</span></span>

## <span data-ttu-id="c1e92-126">Feedback senden</span><span class="sxs-lookup"><span data-stu-id="c1e92-126">Feedback</span></span>
<span data-ttu-id="c1e92-127">Senden Sie uns Ihr Feedback, indem Sie [ein Problem](https://github.com/microsoft/vscode-edge-devtools/issues/new) mit dem [GitHub-Repo](https://github.com/microsoft/vscode-edge-devtools)dieser Erweiterung einreichen.</span><span class="sxs-lookup"><span data-stu-id="c1e92-127">Send us your feedback by [filing an issue](https://github.com/microsoft/vscode-edge-devtools/issues/new) against this extension's [GitHub repo](https://github.com/microsoft/vscode-edge-devtools).</span></span> 

<span data-ttu-id="c1e92-128">Wenn Sie uns helfen möchten, diese Erweiterung besser zu gestalten, freuen wir uns über Ihre Beiträge!</span><span class="sxs-lookup"><span data-stu-id="c1e92-128">If you want to help us make this extension better, we welcome your contributions!</span></span> <span data-ttu-id="c1e92-129">Sie finden alles, was Sie für den Einstieg in [unser GitHub-Repo](https://github.com/microsoft/vscode-edge-devtools)benötigen.</span><span class="sxs-lookup"><span data-stu-id="c1e92-129">You can find everything you need to get started in [our GitHub repo](https://github.com/microsoft/vscode-edge-devtools).</span></span>