---
description: Anmerkungen zu dieser Version von Microsoft Edge devtools Protocol, Version 0,1
title: Versionshinweise zu devtools-Protokoll Version 0,1
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 60e92cb3afa9b10b15c8ebdd520c0061fbb3b366
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234019"
---
# <span data-ttu-id="4e77f-103">Versionshinweise zu devtools-Protokoll Version 0,1</span><span class="sxs-lookup"><span data-stu-id="4e77f-103">DevTools Protocol Version 0.1 Release Notes</span></span>

> [!NOTE]
> <span data-ttu-id="4e77f-104">Das Microsoft Edge devtools-Protokoll funktioniert nur unter [Windows 10 April 2018-Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) und später [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) -Builds.</span><span class="sxs-lookup"><span data-stu-id="4e77f-104">The Microsoft Edge DevTools Protocol works only on [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>

<span data-ttu-id="4e77f-105">Version 0,1 des Microsoft **Edge devtools-Protokolls** bietet eine frühe Vorschau zum Testen der EdgeHTML-Instrumentation und des einfachen Remotedebuggens in der neuen eigenständigen [Microsoft Edge devtools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) -app.</span><span class="sxs-lookup"><span data-stu-id="4e77f-105">Version 0.1 of the Microsoft **Edge DevTools Protocol** provides an early preview for testing EdgeHTML instrumentation and basic remote debugging in the new standalone [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) app.</span></span> <span data-ttu-id="4e77f-106">Daher ist es erforderlich, dass Sie [Windows 10 April 2018-Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) oder einen späteren [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) -Build ausführen.</span><span class="sxs-lookup"><span data-stu-id="4e77f-106">As such, it requires you to be running [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) or a later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) build.</span></span>

<span data-ttu-id="4e77f-107">Die Ziele hinter dem devtools-Protokoll sind drei Fach:</span><span class="sxs-lookup"><span data-stu-id="4e77f-107">The goals behind the DevTools Protocol are three-fold:</span></span>

 - <span data-ttu-id="4e77f-108">Bereitstelleneiner öffentlichen API für unsere devtools-App zum Anfügen an Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4e77f-108">Provide a public API for our DevTools app to attach to Microsoft Edge</span></span>
 - <span data-ttu-id="4e77f-109">Erweitern des Zugriffs auf die devtools-Funktionalität auf externe Tooling-Clients</span><span class="sxs-lookup"><span data-stu-id="4e77f-109">Expand access of DevTools functionality to external tooling clients</span></span>
 - <span data-ttu-id="4e77f-110">Aktivieren des Remotedebuggens im gesamten Bereich von Windows 10-Geräten mit Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4e77f-110">Enable remote debugging across the range of Windows 10 devices running Microsoft Edge</span></span> 

<span data-ttu-id="4e77f-111">Diese vorläufige Version bietet Kernfunktionen zum Debuggen, wie das Festlegen von Haltepunkten, das Durchlaufen von Code und das Untersuchen von Stapelablaufverfolgungen.</span><span class="sxs-lookup"><span data-stu-id="4e77f-111">This preliminary release provides core debugging functionality, such as setting breakpoints, stepping through code, and exploring stack traces.</span></span> <span data-ttu-id="4e77f-112">In der Benutzeroberfläche von Edge devtools wird dadurch die Funktionalität übersetzt, die im [**Debuggerfenster**](../../devtools-guide/debugger.md) zur Verfügung steht, minus Cache Überprüfung (für Web Storage, Service Worker, Cache-API und IndexedDB).</span><span class="sxs-lookup"><span data-stu-id="4e77f-112">In the Edge DevTools UI, this translates to functionality available in the [**Debugger**](../../devtools-guide/debugger.md) panel, minus cache inspection (for Web storage, Service worker, Cache API, and IndexedDB).</span></span> 

<span data-ttu-id="4e77f-113">Weitere Debuggerfunktionen werden in bevorstehenden Versionen hinzugefügt, gefolgt von der Instrumentation, die andere [devtools](../index.md) -Panels anbietet.</span><span class="sxs-lookup"><span data-stu-id="4e77f-113">Further debugger functionality will be added in upcoming releases, followed by the instrumentation powering other [DevTools](../index.md) panels.</span></span>
