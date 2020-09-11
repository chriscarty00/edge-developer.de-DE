---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2WebResourceRequestedEventHandler
ms.openlocfilehash: 6aa36c8b28a3e47a796324987687ab23179aae10
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012009"
---
# <span data-ttu-id="c53c2-104">Schnittstellen ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c53c2-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="c53c2-105">Wird ausgelöst, wenn eine URL-Anforderung (über Netzwerk, Datei usw.) in der WebView für einen Ressourcenkontext Filter und eine in AddWebResourceRequestedFilter angegebene URL für die Webressource erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c53c2-105">Fires when a URL request (through network, file etc.) is made in the webview for a Web resource matching resource context filter and URL specified in AddWebResourceRequestedFilter.</span></span>

## <span data-ttu-id="c53c2-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c53c2-106">Summary</span></span>

 <span data-ttu-id="c53c2-107">Member</span><span class="sxs-lookup"><span data-stu-id="c53c2-107">Members</span></span>                        | <span data-ttu-id="c53c2-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="c53c2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c53c2-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="c53c2-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c53c2-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c53c2-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="c53c2-111">Der Host kann die Anforderung anzeigen und ändern oder eine Antwort in einem ähnlichen Muster wie http bereitstellen, in diesem Fall ist die Anforderung sofort abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c53c2-111">The host can view and modify the request or provide a response in a similar pattern to HTTP, in which case the request immediately completed.</span></span> <span data-ttu-id="c53c2-112">Dieser enthält möglicherweise keine Anforderungs Kopfzeilen, die vom Netzwerkstapel hinzugefügt werden, wie Autorisierungs Kopfzeilen.</span><span class="sxs-lookup"><span data-stu-id="c53c2-112">This may not contain any request headers that are added by the network stack, such as Authorization headers.</span></span>

## <span data-ttu-id="c53c2-113">Member</span><span class="sxs-lookup"><span data-stu-id="c53c2-113">Members</span></span>

#### <span data-ttu-id="c53c2-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="c53c2-114">Invoke</span></span> 

<span data-ttu-id="c53c2-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c53c2-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c53c2-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="c53c2-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>

