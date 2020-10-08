---
ms.assetid: 1319a070-c6e3-4592-9f4b-40ce1575851f
description: Hier erfahren Sie, wie Sie Ihre Chrome-Erweiterung mithilfe des Microsoft Edge Extension Toolkit zu Microsoft Edge portieren.
title: Portieren von Chrome-Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.custom: seodec18
ms.openlocfilehash: 38bf1324c2e7e6f7754912177ce0e53d6c15a276
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567371"
---
# <span data-ttu-id="1f424-104">Portieren einer Erweiterung von Chrome zu Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1f424-104">Porting an extension from Chrome to Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="1f424-105">Das Portieren einer Erweiterung von Chrome zu Microsoft Edge wird mithilfe des [Microsoft Edge Extension Toolkit](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb)vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="1f424-105">Porting an extension from Chrome to Microsoft Edge is made easy with the help of the [Microsoft Edge Extension Toolkit](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).</span></span> <span data-ttu-id="1f424-106">Dieses Entwicklertool wandelt eine ungepackte Chrome-Erweiterung in eine ungepackte Microsoft-Edge-Erweiterung um, indem Sie APIs überbrückt und Fehler in Ihrer Datei aufweist `manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="1f424-106">This developer tool converts an unpacked Chrome extension to an unpacked Microsoft Edge extension by bridging APIs and surfacing any errors in your `manifest.json` file.</span></span>


### <span data-ttu-id="1f424-107">API-Bridges</span><span class="sxs-lookup"><span data-stu-id="1f424-107">API bridges</span></span>
<span data-ttu-id="1f424-108">Um eine nahtlose Portierung von Chrome-APIs auf unterstützte Microsoft Edge-APIs zu ermöglichen, werden dem Ordner Ihrer Erweiterung zwei Skripts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1f424-108">In order to allow for seamless porting of Chrome APIs to supported Microsoft Edge APIs, two scripts are added to your extension's folder.</span></span> <span data-ttu-id="1f424-109">Diese Skripts überbrücken APIs (bei Bedarf polyfiling), was bedeutet, dass Sie sich keine Gedanken über das Ändern von Chrome-spezifischem Code in Ihrem Hintergrundskript oder in Inhalts Skripts machen müssen.</span><span class="sxs-lookup"><span data-stu-id="1f424-109">These scripts bridge APIs (polyfiling where necessary), meaning you won't have to worry about changing any Chrome specific code in your background script or content scripts.</span></span>

<span data-ttu-id="1f424-110">Nach der Konvertierung werden die Dateien in der Manifestdatei ihrer Erweiterung mit dem folgenden Schlüssel angezeigt `"-ms-preload"` :</span><span class="sxs-lookup"><span data-stu-id="1f424-110">After conversion, you will see them included in the manifest file of your extension with the `"-ms-preload"` key:</span></span>

```json
"-ms-preload": {
  "backgroundScript": "backgroundScriptsAPIBridge.js",
  "contentScript": "contentScriptsAPIBridge.js"
}
```

## <span data-ttu-id="1f424-111">Verwenden des Microsoft Edge Extension Toolkit</span><span class="sxs-lookup"><span data-stu-id="1f424-111">Using the Microsoft Edge Extension Toolkit</span></span>

<span data-ttu-id="1f424-112">Die folgenden Anweisungen erläutern, wie Sie Ihre Chrome-Erweiterung in Windows 10 Anniversary Update Edition auf Microsoft Edge konvertieren:</span><span class="sxs-lookup"><span data-stu-id="1f424-112">The following instructions detail how to convert your Chrome extension to run on Microsoft Edge in the Windows 10 Anniversary Update edition:</span></span>

1. <span data-ttu-id="1f424-113">Installieren Sie das [Microsoft Edge Extension Toolkit](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).</span><span class="sxs-lookup"><span data-stu-id="1f424-113">Install the [Microsoft Edge Extension Toolkit](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).</span></span>
2. <span data-ttu-id="1f424-114">Erstellen Sie eine Kopie des Ordners ihrer Chrome-Erweiterung, um eine sichere Aufbewahrung zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="1f424-114">Make a copy of your Chrome extension's folder for safe keeping.</span></span> <span data-ttu-id="1f424-115">Durch den Konvertierungsprozess wird der Code überschrieben.</span><span class="sxs-lookup"><span data-stu-id="1f424-115">The conversion process will overwrite the code.</span></span> 
3. <span data-ttu-id="1f424-116">Führen Sie das Microsoft Edge Extension Toolkit aus, und laden Sie die Kopie der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="1f424-116">Run the Microsoft Edge Extension Toolkit and load the copy of your extension.</span></span>  
 ![Schaltfläche ' Erweiterung laden '](./../media/save-folder.png)
4. <span data-ttu-id="1f424-118">Korrigieren Sie alle Fehler, die im Text-Editor des Tools gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="1f424-118">Correct all the errors that are reported within the tool's text editor.</span></span> <span data-ttu-id="1f424-119">Wählen Sie "erneut überprüfen" aus, um nach dem korrigieren auf Fehler zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1f424-119">Select "Re-validate" to check for errors after making corrections.</span></span>  
 ![Erweiterungen-Toolkitfehler finden](./../media/extension-toolkit.png)
5. <span data-ttu-id="1f424-121">Wählen Sie "Dateien speichern".</span><span class="sxs-lookup"><span data-stu-id="1f424-121">Select "Save files".</span></span>

<span data-ttu-id="1f424-122">Sie können jetzt das Toolkit verlassen und ihre Erweiterung in Microsoft Edge laden!</span><span class="sxs-lookup"><span data-stu-id="1f424-122">You can now exit out of the toolkit and load your extension in Microsoft Edge!</span></span> 

<span data-ttu-id="1f424-123">Sie können mit dem [EdgeHTML Issue Tracker](http://issues.microsoftedge.com)nach bekannten Platt Form Problemen suchen.</span><span class="sxs-lookup"><span data-stu-id="1f424-123">You can search for known platform issues with the [EdgeHTML issue tracker](http://issues.microsoftedge.com).</span></span> <span data-ttu-id="1f424-124">Wenn Sie der Meinung sind, dass Sie etwas neues gefunden haben, [Öffnen Sie ein Problem](https://developer.microsoft.com/microsoft-edge/platform/issues/new/)!</span><span class="sxs-lookup"><span data-stu-id="1f424-124">If you think you've found something new, [open an issue](https://developer.microsoft.com/microsoft-edge/platform/issues/new/)!</span></span>
