---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: b361148f52ed86cbe94d96e9dbf9bd646eb8beb8
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885480"
---
# <span data-ttu-id="5ab76-104">0.9.515-Interface-ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="5ab76-104">0.9.515 - interface ICoreWebView2HttpHeadersCollectionIterator</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="5ab76-105">Iterator für eine Sammlung von HTTP-Headern.</span><span class="sxs-lookup"><span data-stu-id="5ab76-105">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="5ab76-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5ab76-106">Summary</span></span>

 <span data-ttu-id="5ab76-107">Member</span><span class="sxs-lookup"><span data-stu-id="5ab76-107">Members</span></span>                        | <span data-ttu-id="5ab76-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="5ab76-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5ab76-109">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="5ab76-109">get_HasCurrentHeader</span></span>](#get_hascurrentheader) | <span data-ttu-id="5ab76-110">"True", wenn der Iterator keine Überschriften mehr ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="5ab76-110">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="5ab76-111">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="5ab76-111">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="5ab76-112">Rufen Sie den Namen und den Wert des aktuellen HTTP-Headers des Iterators ab.</span><span class="sxs-lookup"><span data-stu-id="5ab76-112">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="5ab76-113">MoveNext</span><span class="sxs-lookup"><span data-stu-id="5ab76-113">MoveNext</span></span>](#movenext) | <span data-ttu-id="5ab76-114">Verschieben Sie den Iterator in den nächsten HTTP-Header in der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="5ab76-114">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="5ab76-115">Siehe [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) und [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span><span class="sxs-lookup"><span data-stu-id="5ab76-115">See [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) and [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span></span> 
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

## <span data-ttu-id="5ab76-116">Member</span><span class="sxs-lookup"><span data-stu-id="5ab76-116">Members</span></span>

#### <span data-ttu-id="5ab76-117">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="5ab76-117">get_HasCurrentHeader</span></span> 

<span data-ttu-id="5ab76-118">"True", wenn der Iterator keine Überschriften mehr ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="5ab76-118">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="5ab76-119">Public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(bool \* hasCurrent)</span><span class="sxs-lookup"><span data-stu-id="5ab76-119">public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(BOOL \* hasCurrent)</span></span>

<span data-ttu-id="5ab76-120">Wenn die Sammlung, über die der Iterator durchlaufen wird, leer ist oder der Iterator über das Ende der Auflistung hinausgegangen ist, ist dies false.</span><span class="sxs-lookup"><span data-stu-id="5ab76-120">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="5ab76-121">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="5ab76-121">GetCurrentHeader</span></span> 

<span data-ttu-id="5ab76-122">Rufen Sie den Namen und den Wert des aktuellen HTTP-Headers des Iterators ab.</span><span class="sxs-lookup"><span data-stu-id="5ab76-122">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="5ab76-123">Public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* Name, LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="5ab76-123">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name, LPWSTR \* value)</span></span>

<span data-ttu-id="5ab76-124">Diese Methode schlägt fehl, wenn der letzte Aufruf von MoveNext has_next auf "false" festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="5ab76-124">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="5ab76-125">MoveNext</span><span class="sxs-lookup"><span data-stu-id="5ab76-125">MoveNext</span></span> 

<span data-ttu-id="5ab76-126">Verschieben Sie den Iterator in den nächsten HTTP-Header in der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="5ab76-126">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="5ab76-127">Public HRESULT [MoveNext](#movenext)(bool \* hasNext ")</span><span class="sxs-lookup"><span data-stu-id="5ab76-127">public HRESULT [MoveNext](#movenext)(BOOL \* hasNext)</span></span>

<span data-ttu-id="5ab76-128">Der hasNext "-Parameter wird auf" false "festgelegt, wenn keine weiteren HTTP-Header vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="5ab76-128">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="5ab76-129">Nachdem dies erfolgt ist, schlägt die GetCurrentHeader-Methode fehl, wenn Sie aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5ab76-129">After this occurs the GetCurrentHeader method will fail if called.</span></span>

