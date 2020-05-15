---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 9e94291c55680e03c48a5fbf1b48f9d79a790cb6
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653866"
---
# <span data-ttu-id="8fd1d-104">Schnittstellen ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="8fd1d-104">interface ICoreWebView2HttpHeadersCollectionIterator</span></span> 

> [!NOTE]
> <span data-ttu-id="8fd1d-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="8fd1d-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="8fd1d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="8fd1d-107">Iterator für eine Sammlung von HTTP-Headern.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-107">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="8fd1d-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="8fd1d-108">Summary</span></span>

 <span data-ttu-id="8fd1d-109">Member</span><span class="sxs-lookup"><span data-stu-id="8fd1d-109">Members</span></span>                        | <span data-ttu-id="8fd1d-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="8fd1d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8fd1d-111">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="8fd1d-111">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="8fd1d-112">Rufen Sie den Namen und den Wert des aktuellen HTTP-Headers des Iterators ab.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-112">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="8fd1d-113">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="8fd1d-113">get_HasCurrentHeader</span></span>](#get_hascurrentheader) | <span data-ttu-id="8fd1d-114">"True", wenn der Iterator keine Überschriften mehr ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-114">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="8fd1d-115">MoveNext</span><span class="sxs-lookup"><span data-stu-id="8fd1d-115">MoveNext</span></span>](#movenext) | <span data-ttu-id="8fd1d-116">Verschieben Sie den Iterator in den nächsten HTTP-Header in der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-116">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="8fd1d-117">Siehe [ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) und [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md).</span><span class="sxs-lookup"><span data-stu-id="8fd1d-117">See [ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) and [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md).</span></span> 

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

## <span data-ttu-id="8fd1d-118">Member</span><span class="sxs-lookup"><span data-stu-id="8fd1d-118">Members</span></span>

#### <span data-ttu-id="8fd1d-119">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="8fd1d-119">GetCurrentHeader</span></span> 

<span data-ttu-id="8fd1d-120">Rufen Sie den Namen und den Wert des aktuellen HTTP-Headers des Iterators ab.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-120">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="8fd1d-121">Public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* Name, LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="8fd1d-121">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name,LPWSTR \* value)</span></span>

<span data-ttu-id="8fd1d-122">Diese Methode schlägt fehl, wenn der letzte Aufruf von MoveNext has_next auf "false" festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-122">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="8fd1d-123">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="8fd1d-123">get_HasCurrentHeader</span></span> 

<span data-ttu-id="8fd1d-124">"True", wenn der Iterator keine Überschriften mehr ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-124">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="8fd1d-125">Public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(bool \* hasCurrent)</span><span class="sxs-lookup"><span data-stu-id="8fd1d-125">public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(BOOL \* hasCurrent)</span></span>

<span data-ttu-id="8fd1d-126">Wenn die Sammlung, über die der Iterator durchlaufen wird, leer ist oder der Iterator über das Ende der Auflistung hinausgegangen ist, ist dies false.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-126">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="8fd1d-127">MoveNext</span><span class="sxs-lookup"><span data-stu-id="8fd1d-127">MoveNext</span></span> 

<span data-ttu-id="8fd1d-128">Verschieben Sie den Iterator in den nächsten HTTP-Header in der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-128">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="8fd1d-129">Public HRESULT [MoveNext](#movenext)(bool \* hasNext ")</span><span class="sxs-lookup"><span data-stu-id="8fd1d-129">public HRESULT [MoveNext](#movenext)(BOOL \* hasNext)</span></span>

<span data-ttu-id="8fd1d-130">Der hasNext "-Parameter wird auf" false "festgelegt, wenn keine weiteren HTTP-Header vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-130">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="8fd1d-131">Nachdem dies erfolgt ist, schlägt die GetCurrentHeader-Methode fehl, wenn Sie aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-131">After this occurs the GetCurrentHeader method will fail if called.</span></span>

