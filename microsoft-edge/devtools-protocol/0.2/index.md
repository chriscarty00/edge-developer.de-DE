---
description: Anmerkungen zu dieser Version von Microsoft Edge devtools Protocol, Version 0,2
title: Versionshinweise zu Microsoft Edge devtools Protocol Version 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: c4959d2905f95c2bcf98cb78ad67bb88ecfec959
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104742"
---
# <span data-ttu-id="a6211-103">Versionshinweise zu devtools-Protokoll Version 0,2</span><span class="sxs-lookup"><span data-stu-id="a6211-103">DevTools Protocol Version 0.2 Release Notes</span></span>

> [!NOTE]
> <span data-ttu-id="a6211-104">Version 0,2 des Microsoft Edge devtools-Protokolls funktioniert nur auf dem [Windows 10 October 2018-Update](/windows/uwp/whats-new/windows-10-build-17763) und später in [Windows Insider Preview](https://insider.windows.com/getting-started/) -Builds.</span><span class="sxs-lookup"><span data-stu-id="a6211-104">Version 0.2 of the Microsoft Edge DevTools Protocol works only on the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) and later [Windows Insider Preview](https://insider.windows.com/getting-started/) builds.</span></span>

<span data-ttu-id="a6211-105">Version 0,2 des Microsoft **Edge devtools-Protokolls** bietet eine Vorschau zum Testen der EdgeHTML-Instrumentation und des einfachen Remotedebuggens in der neuen eigenständigen [Microsoft Edge devtools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) -app.</span><span class="sxs-lookup"><span data-stu-id="a6211-105">Version 0.2 of the Microsoft **Edge DevTools Protocol** provides a preview for testing EdgeHTML instrumentation and basic remote debugging in the new standalone [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) app.</span></span> <span data-ttu-id="a6211-106">Daher müssen Sie das [Windows 10 October 2018-Update](/windows/uwp/whats-new/windows-10-build-17763) oder einen späteren [Windows Insider Preview](https://insider.windows.com/getting-started/) -Build ausführen.</span><span class="sxs-lookup"><span data-stu-id="a6211-106">As such, it requires you to be running the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) or a later [Windows Insider Preview](https://insider.windows.com/getting-started/) build.</span></span>

<span data-ttu-id="a6211-107">Die Ziele hinter dem devtools-Protokoll sind drei Fach:</span><span class="sxs-lookup"><span data-stu-id="a6211-107">The goals behind the DevTools Protocol are three-fold:</span></span>

 - <span data-ttu-id="a6211-108">Bereitstelleneiner öffentlichen API für unsere devtools-App zum Anfügen an Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a6211-108">Provide a public API for our DevTools app to attach to Microsoft Edge</span></span>
 - <span data-ttu-id="a6211-109">Erweitern des Zugriffs auf die devtools-Funktionalität auf externe Tooling-Clients</span><span class="sxs-lookup"><span data-stu-id="a6211-109">Expand access of DevTools functionality to external tooling clients</span></span>
 - <span data-ttu-id="a6211-110">Aktivieren des Remotedebuggens im gesamten Bereich von Windows 10-Geräten mit Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a6211-110">Enable remote debugging across the range of Windows 10 devices running Microsoft Edge</span></span> 

<span data-ttu-id="a6211-111">Version 0,2 des devtools-Protokolls enthält neue Domänen für Format-und Layoutfunktionen (schreibgeschützt) sowie Debug-und Konsolen-APIs, zusätzlich zu den Kernskript Debugging-Funktionen, die in Version 0,1 eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="a6211-111">Version 0.2 of the DevTools Protocol includes new domains for style and layout (read-only) debugging and console APIs, in addition to the core script debugging functionality introduced in Version 0.1.</span></span> <span data-ttu-id="a6211-112">In der Benutzeroberfläche von Edge devtools wird dadurch die Funktionalität übersetzt, die in den Panels [**Elemente**](../../devtools-guide/elements.md), [**Konsole**](../../devtools-guide/console.md) und [**Debugger**](../../devtools-guide/debugger.md)  zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="a6211-112">In the Edge DevTools UI, this translates to functionality available in the [**Elements**](../../devtools-guide/elements.md), [**Console**](../../devtools-guide/console.md) and [**Debugger**](../../devtools-guide/debugger.md)  panels.</span></span>
