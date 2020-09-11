---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2HttpHeadersCollectionIterator
ms.openlocfilehash: da1b9f3dbf9ba0ebd309e1017fe4e7f7e6526941
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011328"
---
# <span data-ttu-id="ec4ca-104">0.9.579-Interface-ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="ec4ca-104">0.9.579 - interface ICoreWebView2HttpHeadersCollectionIterator</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="ec4ca-105">Iterator für eine Sammlung von HTTP-Headern.</span><span class="sxs-lookup"><span data-stu-id="ec4ca-105">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="ec4ca-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ec4ca-106">Summary</span></span>

 <span data-ttu-id="ec4ca-107">Member</span><span class="sxs-lookup"><span data-stu-id="ec4ca-107">Members</span></span>                        | <span data-ttu-id="ec4ca-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ec4ca-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ec4ca-109">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="ec4ca-109">get_HasCurrentHeader</span></span>](#get_hascurrentheader) | <span data-ttu-id="ec4ca-110">"True", wenn der Iterator keine Überschriften mehr ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="ec4ca-110">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="ec4ca-111">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="ec4ca-111">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="ec4ca-112">Rufen Sie den Namen und den Wert des aktuellen HTTP-Headers des Iterators ab.</span><span class="sxs-lookup"><span data-stu-id="ec4ca-112">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="ec4ca-113">MoveNext</span><span class="sxs-lookup"><span data-stu-id="ec4ca-113">MoveNext</span></span>](#movenext) | <span data-ttu-id="ec4ca-114">Verschieben Sie den Iterator in den nächsten HTTP-Header in der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="ec4ca-114">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="ec4ca-115">Siehe [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) und [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span><span class="sxs-lookup"><span data-stu-id="ec4ca-115">See [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) and [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span></span> 
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

## <span data-ttu-id="ec4ca-116">Member</span><span class="sxs-lookup"><span data-stu-id="ec4ca-116">Members</span></span>

#### <span data-ttu-id="ec4ca-117">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="ec4ca-117">get_HasCurrentHeader</span></span> 

<span data-ttu-id="ec4ca-118">"True", wenn der Iterator keine Überschriften mehr ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="ec4ca-118">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="ec4ca-119">Public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(bool \* hasCurrent)</span><span class="sxs-lookup"><span data-stu-id="ec4ca-119">public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(BOOL \* hasCurrent)</span></span>

<span data-ttu-id="ec4ca-120">Wenn die Sammlung, über die der Iterator durchlaufen wird, leer ist oder der Iterator über das Ende der Auflistung hinausgegangen ist, ist dies false.</span><span class="sxs-lookup"><span data-stu-id="ec4ca-120">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="ec4ca-121">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="ec4ca-121">GetCurrentHeader</span></span> 

<span data-ttu-id="ec4ca-122">Rufen Sie den Namen und den Wert des aktuellen HTTP-Headers des Iterators ab.</span><span class="sxs-lookup"><span data-stu-id="ec4ca-122">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="ec4ca-123">Public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* Name, LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="ec4ca-123">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name, LPWSTR \* value)</span></span>

<span data-ttu-id="ec4ca-124">Diese Methode schlägt fehl, wenn der letzte Aufruf von MoveNext has_next auf "false" festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="ec4ca-124">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="ec4ca-125">MoveNext</span><span class="sxs-lookup"><span data-stu-id="ec4ca-125">MoveNext</span></span> 

<span data-ttu-id="ec4ca-126">Verschieben Sie den Iterator in den nächsten HTTP-Header in der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="ec4ca-126">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="ec4ca-127">Public HRESULT [MoveNext](#movenext)(bool \* hasNext ")</span><span class="sxs-lookup"><span data-stu-id="ec4ca-127">public HRESULT [MoveNext](#movenext)(BOOL \* hasNext)</span></span>

<span data-ttu-id="ec4ca-128">Der hasNext "-Parameter wird auf" false "festgelegt, wenn keine weiteren HTTP-Header vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ec4ca-128">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="ec4ca-129">Nachdem dies erfolgt ist, schlägt die GetCurrentHeader-Methode fehl, wenn Sie aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ec4ca-129">After this occurs the GetCurrentHeader method will fail if called.</span></span>

