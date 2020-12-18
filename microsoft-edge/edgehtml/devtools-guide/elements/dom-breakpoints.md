---
description: Verwenden von Dom-Haltepunkten zum visuellen Debuggen von Layout-Pannen auf Ihrer Seite
title: DevTools-Elemente-Dom-Haltepunkte
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Elemente, Dom-Haltepunkte, Dom-Mutation
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cb60fa0497c98c152ca2c5adf28e9dee5d7c9f98
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233850"
---
# <span data-ttu-id="287a5-104">DOM-Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="287a5-104">DOM breakpoints</span></span>

<span data-ttu-id="287a5-105">Verwalten Sie Ihre Dom-mutations Haltepunkte in diesem Bereich, einschließlich Deaktivierung, löschen und erneute Bindung.</span><span class="sxs-lookup"><span data-stu-id="287a5-105">Manage your DOM mutation breakpoints from this pane, including disabling, deleting and rebinding them.</span></span>

<span data-ttu-id="287a5-106">Sie können Dom-mutations Haltepunkte verwenden, um in den Debugger einzubrechen, wenn sich ein ausgewählter Elementknoten ändert.</span><span class="sxs-lookup"><span data-stu-id="287a5-106">You can use DOM mutation breakpoints to break into the debugger whenever a selected element node changes.</span></span> <span data-ttu-id="287a5-107">Dies ist hilfreich bei der Nachverfolgung des Codes, der für das Auslösen von visuellen Problemen mit der Benutzeroberfläche verantwortlich ist, ohne einzelne Haltepunkte für jede der 450 + DOM-APIs in *EdgeHTML* festzulegen, die solche Änderungen auslösen können.</span><span class="sxs-lookup"><span data-stu-id="287a5-107">This is helpful for tracking down the code responsible for causing visual glitches with your UI without having to set individual breakpoints on each of the 450+ DOM APIs in *EdgeHTML* that can trigger such changes.</span></span> 

<span data-ttu-id="287a5-108">Zum Festlegen eines DOM-Haltepunkts klicken Sie mit der rechten Maustaste auf ein beliebiges Element in der *HTML-Strukturansicht* des **Elements** Panels, um das Kontextmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="287a5-108">To set a DOM breakpoint, right-click on any element in the **Elements** panel *HTML tree view* to open the context menu.</span></span>

![Dom-Haltepunkte-Kontextmenü](../media/elements_dom_breakpoints_contextmenu.png)

<span data-ttu-id="287a5-110">Sie können einen der folgenden Haltepunkte festlegen:</span><span class="sxs-lookup"><span data-stu-id="287a5-110">You can set any of the following breakpoints:</span></span>

 - <span data-ttu-id="287a5-111">**Unterbrechung beim Entfernen des Knotens**: unterbrechen Sie den Debugger, wenn das ausgewählte Element aus dem Dokument entfernt wird (DOM-Struktur).</span><span class="sxs-lookup"><span data-stu-id="287a5-111">**Break on Node removed**: Break into the debugger when the selected element is removed from the document (DOM tree).</span></span>

 - <span data-ttu-id="287a5-112">**Unterbrechung**in der Teilstruktur geändert: unterbrechen Sie den Debugger, wenn eines der Nachfolgerelemente des ausgewählten Elements geändert (hinzugefügt, entfernt oder deren unter Strukturen geändert wurden).</span><span class="sxs-lookup"><span data-stu-id="287a5-112">**Break on Subtree modified**: Break into the debugger when any of the descendants of the selected element are changed (added, removed, or their subtrees are modified).</span></span> <span data-ttu-id="287a5-113">Dies wird nicht unterbrechen, wenn Attribute geändert werden (siehe die nächste Option dafür).</span><span class="sxs-lookup"><span data-stu-id="287a5-113">This will not break when attributes are modified (see the next option for that).</span></span>

 - <span data-ttu-id="287a5-114">**Break-on-Attribut geändert**: unterbrechen Sie den Debugger, wenn ein Attribut des ausgewählten Elements hinzugefügt, entfernt oder in Value geändert wird.</span><span class="sxs-lookup"><span data-stu-id="287a5-114">**Break on Attribute modified**: Break into the debugger when an attribute of the selected element is added, removed or changed in value.</span></span>

<span data-ttu-id="287a5-115">Der Bereich " **DOM-Haltepunkte** " listet dann das ausgewählte Element auf (durch Generieren einer Auswahl, die seine Position im Dom beschreibt) und die Typen von Haltepunkten, die Sie festlegen (*Knoten entfernt, Struktur geändert, Attribut geändert*).</span><span class="sxs-lookup"><span data-stu-id="287a5-115">The **DOM breakpoints** pane will then list the selected element (by generating a selector describing its location in the DOM) and the types of breakpoints you have set (*Node removed, Subtree modified, Attribute modified*).</span></span> <span data-ttu-id="287a5-116">Von hier aus können Sie Ihre Haltepunkte auch einzeln (über das RT-Click-Kontextmenü) oder alle gleichzeitig (mithilfe der Schaltflächen) erneut *binden*, *Deaktivieren*oder *Löschen* .</span><span class="sxs-lookup"><span data-stu-id="287a5-116">From here, you can also *rebind*, *disable*, or *delete* your breakpoints, individually (from the rt-click context menu) or all at once (using the buttons).</span></span>

![Bereich "Dom-Haltepunkte"](../media/elements_dom_breakpoints.png)

## <span data-ttu-id="287a5-118">Haltepunkt Persistenz</span><span class="sxs-lookup"><span data-stu-id="287a5-118">Breakpoint persistence</span></span>

<span data-ttu-id="287a5-119">Haltepunkte werden im Rahmen ihrer devtools-Einstellungen gespeichert (und sind auf die URL der Seite beschränkt, in der Sie sich befinden).</span><span class="sxs-lookup"><span data-stu-id="287a5-119">Breakpoints are stored (and scoped to the URL of the page they're set within) as part of your DevTools settings.</span></span> <span data-ttu-id="287a5-120">Wenn die Seite neu geladen wird oder die Tools geschlossen und erneut geöffnet werden, versucht devtools, die Haltepunkte erneut an die zugehörigen Elemente zu binden.</span><span class="sxs-lookup"><span data-stu-id="287a5-120">When the page is reloaded or the tools are closed and reopened, DevTools will attempt to rebind your breakpoints to their associated elements.</span></span>

<span data-ttu-id="287a5-121">Haltepunkte, die nicht automatisch erneut gebunden werden konnten, werden mit einem Warnungssymbol im Kreis des Haltepunkts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="287a5-121">Breakpoints that couldn't be automatically rebinded are indicated with a warning icon on the breakpoint circle.</span></span> <span data-ttu-id="287a5-122">Für diese können Sie warten, bis das Element manuell (mithilfe der Schaltfläche " **Haltepunkt erneut binden** " und/oder der Kontextmenüoption) erneut gebunden wird, sobald ein entsprechendes Element im DOM angezeigt wird (und das Symbol "Haltepunkt" nicht mehr die Warnanzeige zeigt) oder den Haltepunkt ganz **Löschen** .</span><span class="sxs-lookup"><span data-stu-id="287a5-122">For these, you can wait to rebind the element manually (using the **Rebind breakpoint** button and/or context menu option) once a corresponding element appears in the DOM (and the breakpoint icon no longer shows the warning indicator), or **Delete** the breakpoint altogether.</span></span>

![Indikator für ungebundenen Haltepunkt](../media/elements_dom_breakpoint_unbound.png)

<span data-ttu-id="287a5-124">Zusätzlich zu diesem Bereich des *DOM-Haltepunkts* können Sie auch Ihre [DOM-Haltepunkte](../debugger.md#dom-breakpoints) im **Debugger**verwalten.</span><span class="sxs-lookup"><span data-stu-id="287a5-124">In addition to this *DOM breakpoints* pane, you can also manage your [DOM breakpoints](../debugger.md#dom-breakpoints) from within the **Debugger**.</span></span>

## <span data-ttu-id="287a5-125">Aktuelle Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="287a5-125">Current limitations</span></span>

<span data-ttu-id="287a5-126">Beachten Sie die folgenden Einschränkungen des Debuggens von Dom-Haltepunkten in Edge-devtools:</span><span class="sxs-lookup"><span data-stu-id="287a5-126">Please be aware of the following limitations of DOM breakpoint debugging in Edge DevTools:</span></span>

- <span data-ttu-id="287a5-127">Edge-devtools unterstützen derzeit keine rebindungs Haltepunkte innerhalb von [ `<iframe>` s](https://developer.mozilla.org/docs/Web/HTML/Element/iframe).</span><span class="sxs-lookup"><span data-stu-id="287a5-127">Edge DevTools don't currently support rebinding breakpoints inside of [`<iframe>`s](https://developer.mozilla.org/docs/Web/HTML/Element/iframe).</span></span> <span data-ttu-id="287a5-128">Wenn Sie einen Haltepunkt in einem IFRAME festlegen und den Edge-devtools schließen oder die Seite aktualisieren, geht der Haltepunkt verloren.</span><span class="sxs-lookup"><span data-stu-id="287a5-128">If you set a breakpoint in an iframe and close Edge DevTools or refresh the page, the breakpoint will be lost.</span></span>

- <span data-ttu-id="287a5-129">Wenn Ihr Skript vor Abschluss des DOM einen synchron ausgeführten Haltepunkt findet [`readyState`](https://developer.mozilla.org/docs/Web/API/Document/readyState) , können Sie keinen DOM-Haltepunkt festlegen, während der Debugger angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="287a5-129">If your script encounters a synchronously-executed breakpoint before the DOM [`readyState`](https://developer.mozilla.org/docs/Web/API/Document/readyState) is completed, you won't be able to set a DOM breakpoint while the debugger is paused.</span></span> <span data-ttu-id="287a5-130">Sie können diese Situation in der Regel beheben, indem Sie die [`defer`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) oder [`async`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) Skript Attribute festlegen.</span><span class="sxs-lookup"><span data-stu-id="287a5-130">You can typically remedy this situation by setting the [`defer`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) or [`async`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) script attributes.</span></span>

- <span data-ttu-id="287a5-131">Für synchrone Skripts wird die automatische erneute Bindung von Haltepunkten ausgelöst, wenn das [`window.onload`](https://developer.mozilla.org/docs/Web/API/GlobalEventHandlers/onload) Ereignis aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="287a5-131">For synchronous scripts, we trigger automatic rebinding of breakpoints when the [`window.onload`](https://developer.mozilla.org/docs/Web/API/GlobalEventHandlers/onload) event is called.</span></span> <span data-ttu-id="287a5-132">In diesem Fall verpassen wir möglicherweise Bindungs Haltepunkte, die während des anfänglichen skriptgesteuerten Aufbaus des DOM ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="287a5-132">In this case, we may miss binding breakpoints that would trigger during initial script-driven build-up of the DOM.</span></span> <span data-ttu-id="287a5-133">Bei asynchronen Skripts wird ein erneuter Binde Versuch ausgelöst, bevor das erste Skript ausgeführt wird, sodass Ihre Haltepunkte ggf. erneut gebunden und ausgelöst werden können.</span><span class="sxs-lookup"><span data-stu-id="287a5-133">For asynchronous scripts, we trigger a rebind attempt before the first script executes, so your breakpoints may rebind and trigger as desired.</span></span>
