---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: cc3cf67a03f81acc546ab17fded5d7430496033f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653849"
---
# <span data-ttu-id="97578-104">Schnittstellen ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="97578-104">interface ICoreWebView2HttpHeadersCollectionIterator</span></span> 

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="97578-105">Iterator für eine Sammlung von HTTP-Headern.</span><span class="sxs-lookup"><span data-stu-id="97578-105">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="97578-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="97578-106">Summary</span></span>

 <span data-ttu-id="97578-107">Member</span><span class="sxs-lookup"><span data-stu-id="97578-107">Members</span></span>                        | <span data-ttu-id="97578-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="97578-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="97578-109">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="97578-109">get_HasCurrentHeader</span></span>](#get_hascurrentheader) | <span data-ttu-id="97578-110">"True", wenn der Iterator keine Überschriften mehr ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="97578-110">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="97578-111">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="97578-111">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="97578-112">Rufen Sie den Namen und den Wert des aktuellen HTTP-Headers des Iterators ab.</span><span class="sxs-lookup"><span data-stu-id="97578-112">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="97578-113">MoveNext</span><span class="sxs-lookup"><span data-stu-id="97578-113">MoveNext</span></span>](#movenext) | <span data-ttu-id="97578-114">Verschieben Sie den Iterator in den nächsten HTTP-Header in der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="97578-114">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="97578-115">Siehe [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) und [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span><span class="sxs-lookup"><span data-stu-id="97578-115">See [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) and [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span></span> 
```cpp
std::wstring RequestHeadersToJsonString(ICoreWebView2HttpRequestHeaders* requestHeaders)
{
    wil::com_ptr<ICoreWebView2HttpHeadersCollectionIterator> iterator;
    CHECK_FAILURE(requestHeaders->GetIterator(&iterator));
    BOOL hasCurrent = FALSE;
    std::wstring result = L"[";

    while (SUCCEEDED(iterator->get_HasCurrentHeader(&hasCurrent)) && hasCurrent)
    {
        wil::unique_cotaskmem_string name;
        wil::unique_cotaskmem_string value;

        CHECK_FAILURE(iterator->GetCurrentHeader(&name, &value));
        result += L"{\"name\": " + EncodeQuote(name.get())
            + L", \"value\": " + EncodeQuote(value.get()) + L"}";

        BOOL hasNext = FALSE;
        CHECK_FAILURE(iterator->MoveNext(&hasNext));
        if (hasNext)
        {
            result += L", ";
        }
    }

    return result + L"]";
}
```

## <span data-ttu-id="97578-116">Member</span><span class="sxs-lookup"><span data-stu-id="97578-116">Members</span></span>

#### <span data-ttu-id="97578-117">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="97578-117">get_HasCurrentHeader</span></span> 

<span data-ttu-id="97578-118">"True", wenn der Iterator keine Überschriften mehr ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="97578-118">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="97578-119">Public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(bool \* hasCurrent)</span><span class="sxs-lookup"><span data-stu-id="97578-119">public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(BOOL \* hasCurrent)</span></span>

<span data-ttu-id="97578-120">Wenn die Sammlung, über die der Iterator durchlaufen wird, leer ist oder der Iterator über das Ende der Auflistung hinausgegangen ist, ist dies false.</span><span class="sxs-lookup"><span data-stu-id="97578-120">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="97578-121">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="97578-121">GetCurrentHeader</span></span> 

<span data-ttu-id="97578-122">Rufen Sie den Namen und den Wert des aktuellen HTTP-Headers des Iterators ab.</span><span class="sxs-lookup"><span data-stu-id="97578-122">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="97578-123">Public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* Name, LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="97578-123">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name, LPWSTR \* value)</span></span>

<span data-ttu-id="97578-124">Diese Methode schlägt fehl, wenn der letzte Aufruf von MoveNext has_next auf "false" festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="97578-124">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="97578-125">MoveNext</span><span class="sxs-lookup"><span data-stu-id="97578-125">MoveNext</span></span> 

<span data-ttu-id="97578-126">Verschieben Sie den Iterator in den nächsten HTTP-Header in der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="97578-126">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="97578-127">Public HRESULT [MoveNext](#movenext)(bool \* hasNext ")</span><span class="sxs-lookup"><span data-stu-id="97578-127">public HRESULT [MoveNext](#movenext)(BOOL \* hasNext)</span></span>

<span data-ttu-id="97578-128">Der hasNext "-Parameter wird auf" false "festgelegt, wenn keine weiteren HTTP-Header vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="97578-128">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="97578-129">Nachdem dies erfolgt ist, schlägt die GetCurrentHeader-Methode fehl, wenn Sie aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="97578-129">After this occurs the GetCurrentHeader method will fail if called.</span></span>

