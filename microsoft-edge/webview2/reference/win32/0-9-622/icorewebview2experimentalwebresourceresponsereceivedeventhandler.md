---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler
ms.openlocfilehash: 4111c13756783779a1ef3d223c992defadf43d66
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012113"
---
# <span data-ttu-id="2c78a-104">Schnittstellen ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2c78a-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="2c78a-105">Wird ausgelöst, wenn eine Antwort für eine Anforderung für eine Webressource in der WebView empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="2c78a-105">Fires when a response for a request is received for a Web resource in the webview.</span></span>

## <span data-ttu-id="2c78a-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2c78a-106">Summary</span></span>

 <span data-ttu-id="2c78a-107">Member</span><span class="sxs-lookup"><span data-stu-id="2c78a-107">Members</span></span>                        | <span data-ttu-id="2c78a-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="2c78a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2c78a-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="2c78a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="2c78a-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2c78a-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="2c78a-111">Host kann dieses Ereignis verwenden, um die tatsächliche Anforderung und Antwort für eine Webressource anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2c78a-111">Host can use this event to view the actual request and response for a Web resource.</span></span> <span data-ttu-id="2c78a-112">Dazu gehören alle Anforderungs-oder Antwort Änderungen, die vom Netzwerkstapel (wie das Hinzufügen von Autorisierungs Kopfzeilen) vorgenommen wurden, nachdem das WebResourceRequested-Ereignis für die zugeordnete Anforderung ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="2c78a-112">This includes any request or response modifications made by the network stack (such as adding of Authorization headers) after the WebResourceRequested event for the associated request has fired.</span></span> <span data-ttu-id="2c78a-113">Änderungen, die an den Anforderungs-oder Antwort Objekten vorgenommen wurden, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2c78a-113">Modifications made to the request or response objects are ignored.</span></span>

## <span data-ttu-id="2c78a-114">Member</span><span class="sxs-lookup"><span data-stu-id="2c78a-114">Members</span></span>

#### <span data-ttu-id="2c78a-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="2c78a-115">Invoke</span></span> 

<span data-ttu-id="2c78a-116">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2c78a-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="2c78a-117">Public HRESULT [Invoke](#invoke)([ICoreWebView2Experimental](icorewebview2experimental.md) \* Sender; [ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs](icorewebview2experimentalwebresourceresponsereceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="2c78a-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Experimental](icorewebview2experimental.md) \* sender, [ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs](icorewebview2experimentalwebresourceresponsereceivedeventargs.md) \* args)</span></span>

