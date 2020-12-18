---
description: Schauen Sie sich die Neuerungen in der Microsoft Edge-devtools im Windows 10 Oktober 2018-Update an
title: Neuerungen im Microsoft Edge-devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, edgehtml 18
ms.custom: RS5, seodec18
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2f1d3c6fe5bf061186d5c6593a115a8b6794c0dd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234035"
---
# <span data-ttu-id="66a4c-104">DevTools im neuesten Windows 10-Update (EdgeHTML 18)</span><span class="sxs-lookup"><span data-stu-id="66a4c-104">DevTools in the latest Windows 10 update (EdgeHTML 18)</span></span>

<span data-ttu-id="66a4c-105">Das neueste Update für Microsoft Edge devtools bietet eine Reihe von Vorteilen sowohl für die Benutzeroberfläche als auch unter der Haube, einschließlich neuer dedizierter Panels für [*Dienstmitarbeiter*](#service-workers-panel) und [*Speicher*](#storage-panel), Quell [Datei-Such](#source-file-search-tools) Tools im Debugger und neuen Edge- [devtools-Protokoll Domänen](#edge-devtools-protocol-updates) für das Debuggen von Stilen und Layouts sowie für Konsolen-APIs.</span><span class="sxs-lookup"><span data-stu-id="66a4c-105">The latest update to Microsoft Edge DevTools adds a number of conveniences both to the UI and under the hood, including new dedicated panels for [*Service Workers*](#service-workers-panel) and [*Storage*](#storage-panel), source [file search](#source-file-search-tools) tools in the Debugger, and new [Edge DevTools Protocol domains](#edge-devtools-protocol-updates) for style/layout debugging and console APIs.</span></span>

<span data-ttu-id="66a4c-106">Hier sind die neuesten Microsoft Edge devtools-Funktionen, die jetzt im [Windows 10 October 2018-Update](/windows/uwp/whats-new/windows-10-build-17763) ([EdgeHTML 18](https://aka.ms/devguide_edgehtml_18)) zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="66a4c-106">Here are the latest Microsoft Edge DevTools features available now in the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) ([EdgeHTML 18](https://aka.ms/devguide_edgehtml_18)).</span></span> <span data-ttu-id="66a4c-107">Darüber hinaus haben wir auch eine Reihe von Fehlern bei der Barrierefreiheit, Zuverlässigkeit und Leistung behoben, um die Grundlagen zu verbessern!</span><span class="sxs-lookup"><span data-stu-id="66a4c-107">In addition to all this, we’ve also fixed a number of accessibility, reliability, and performance bugs to improve fundamentals!</span></span>

## <span data-ttu-id="66a4c-108">DevTools-App</span><span class="sxs-lookup"><span data-stu-id="66a4c-108">DevTools app</span></span>

<span data-ttu-id="66a4c-109">Wir haben die eigenständige [Microsoft Edge devtools Preview-App](./index.md#microsoft-store-app)aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="66a4c-109">We've updated the standalone [Microsoft Edge DevTools Preview app](./index.md#microsoft-store-app).</span></span> <span data-ttu-id="66a4c-110">Die neueste Version umfasst den Remotedebuggen Zugriff auf Kernfunktionalität im [**Debugger**](./debugger.md), [**Elemente**](./elements.md) (für schreibgeschützte Vorgänge) und [**Konsolen**](./console.md) Panels.</span><span class="sxs-lookup"><span data-stu-id="66a4c-110">The latest release includes remote debugging access to core funtionality in the [**Debugger**](./debugger.md), [**Elements**](./elements.md) (for read-only operations), and [**Console**](./console.md) panels.</span></span>

## <span data-ttu-id="66a4c-111">Dienstmitarbeiter-Panel</span><span class="sxs-lookup"><span data-stu-id="66a4c-111">Service Workers panel</span></span>

<span data-ttu-id="66a4c-112">Es gibt jetzt ein dediziertes [**Service Worker**](./service-workers.md) -Panel zum Überprüfen, verwalten und Debuggen der Servicemitarbeiter Ihrer Website.</span><span class="sxs-lookup"><span data-stu-id="66a4c-112">There's now a dedicated [**Service Workers**](./service-workers.md) panel for inspecting, managing, and debugging your site's service workers.</span></span> <span data-ttu-id="66a4c-113">Dies bietet die gleiche Funktionalität wie zuvor im *Debugger* -Panel (jetzt mit einer nicht überfüllten UI!).</span><span class="sxs-lookup"><span data-stu-id="66a4c-113">This provides the same functionality as was previously in the *Debugger* panel (now with a less-crowded UI!).</span></span>

![Dienstmitarbeiter-Panel](./media/service_worker.png)

## <span data-ttu-id="66a4c-115">Speicher Panel</span><span class="sxs-lookup"><span data-stu-id="66a4c-115">Storage panel</span></span>

<span data-ttu-id="66a4c-116">Darüber hinaus haben wir alle lokalen Speicher Inspektoren (*lokaler Speicher, IndexedDB, Cookies, Cache*), die sich zuvor im *Debugger* befanden, in Ihre eigene dedizierte [**Speicher**](./storage.md) Konsole verschoben.</span><span class="sxs-lookup"><span data-stu-id="66a4c-116">We've also moved all the local storage inspectors (*Local and Sesion Storage, IndexedDB, Cookies, Cache*) previously in the *Debugger* to their own dedicated [**Storage**](./storage.md) panel.</span></span>

![Speicher Panel](./media/storage_cache.png)

## <span data-ttu-id="66a4c-118">Such Tools für Quelldateien</span><span class="sxs-lookup"><span data-stu-id="66a4c-118">Source file search tools</span></span>

<span data-ttu-id="66a4c-119">Der [**Debugger**](./debugger.md) verfügt nun über einen Bereich für die [Quelldatei Suche](./debugger.md#file-search) .</span><span class="sxs-lookup"><span data-stu-id="66a4c-119">The [**Debugger**](./debugger.md) now has a [source file search](./debugger.md#file-search) pane.</span></span> <span data-ttu-id="66a4c-120">Öffnen Sie die Datei mit dem Befehl *in Dateien suchen* ( `Ctrl` + `Shift` + `F` ), wenn Sie über eine bestimmte Zeichenfolge verfügen, die Sie in der Quelle finden möchten.</span><span class="sxs-lookup"><span data-stu-id="66a4c-120">Open it with the *Find in files* command (`Ctrl`+`Shift`+`F`) when you have a specific string of code you're trying to find in the source.</span></span> <span data-ttu-id="66a4c-121">Die Symbolleiste bietet verschiedene Suchoptionen, einschließlich regulärer Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="66a4c-121">The toolbar provides different search options, including regular expressions.</span></span> 

![Debugger-Dateisuche](./media/debugger_file_search.png)

<span data-ttu-id="66a4c-123">Sie können auch eine beliebige geladene Quelldatei mit dem Befehl *Open File* () schnell öffnen `Ctrl` + `P` .</span><span class="sxs-lookup"><span data-stu-id="66a4c-123">You can also quickly open any loaded source file with the *Open file* (`Ctrl`+`P`) command.</span></span>

![Debugger-Datei öffnen](./media/debugger_open_file.png)

## <span data-ttu-id="66a4c-125">Edge-devtools-Protokoll Updates</span><span class="sxs-lookup"><span data-stu-id="66a4c-125">Edge DevTools Protocol updates</span></span>

<span data-ttu-id="66a4c-126">[Version 0,2](../devtools-protocol/0.2/index.md) des devtools-Protokolls bietet neue Domänen für Stil-und Layoutfunktionen (schreibgeschützt) sowie Debug-und Konsolen-APIs sowie die Kernskript Debugging-Funktionen, die in [Version 0,1](../devtools-protocol/0.1/index.md)eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="66a4c-126">[Version 0.2](../devtools-protocol/0.2/index.md) of the DevTools Protocol provides new domains for style and layout (read-only) debugging and console APIs, in addition to the core script debugging functionality introduced in [Version 0.1](../devtools-protocol/0.1/index.md).</span></span> <span data-ttu-id="66a4c-127">In der Benutzeroberfläche von Edge devtools wird dadurch die Funktionalität übersetzt, die in den [**Elementen**](../devtools-guide/elements.md) (für schreibgeschützte Vorgänge), [**Konsolen**](../devtools-guide/console.md) -und [**Debuggerfenster**](../devtools-guide/debugger.md) zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="66a4c-127">In the Edge DevTools UI, this translates to functionality available in the [**Elements**](../devtools-guide/elements.md) (for read-only operations), [**Console**](../devtools-guide/console.md) and [**Debugger**](../devtools-guide/debugger.md) panels.</span></span>
