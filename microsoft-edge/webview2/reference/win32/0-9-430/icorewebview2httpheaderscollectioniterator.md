---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 29f4a09af459e80f8c299a66b24d061e79a96f92
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881025"
---
# 0.9.430-Interface-ICoreWebView2HttpHeadersCollectionIterator 

> [!NOTE]
> Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein. Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

Iterator für eine Sammlung von HTTP-Headern.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[GetCurrentHeader](#getcurrentheader) | Rufen Sie den Namen und den Wert des aktuellen HTTP-Headers des Iterators ab.
[get_HasCurrentHeader](#get_hascurrentheader) | "True", wenn der Iterator keine Überschriften mehr ausgeführt hat.
[MoveNext](#movenext) | Verschieben Sie den Iterator in den nächsten HTTP-Header in der Sammlung.

Siehe [ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) und [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md). 

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

## Member

#### GetCurrentHeader 

Rufen Sie den Namen und den Wert des aktuellen HTTP-Headers des Iterators ab.

> Public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR * Name, LPWSTR *-Wert)

Diese Methode schlägt fehl, wenn der letzte Aufruf von MoveNext has_next auf "false" festgelegt hat.

#### get_HasCurrentHeader 

"True", wenn der Iterator keine Überschriften mehr ausgeführt hat.

> Public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(bool * hasCurrent)

Wenn die Sammlung, über die der Iterator durchlaufen wird, leer ist oder der Iterator über das Ende der Auflistung hinausgegangen ist, ist dies false.

#### MoveNext 

Verschieben Sie den Iterator in den nächsten HTTP-Header in der Sammlung.

> Public HRESULT [MoveNext](#movenext)(bool * hasNext ")

Der hasNext "-Parameter wird auf" false "festgelegt, wenn keine weiteren HTTP-Header vorhanden sind. Nachdem dies erfolgt ist, schlägt die GetCurrentHeader-Methode fehl, wenn Sie aufgerufen wird.

