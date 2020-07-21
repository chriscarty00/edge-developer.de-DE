---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: e0812d463005a4ff3fb834c91412eeb07d837362
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883968"
---
# 0.9.430-Interface-ICoreWebView2WebMessageReceivedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

Ereignis-args für das WebMessageReceived-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_Source](#get_source) | Der URI des Dokuments, das diese Webnachricht gesendet hat.
[get_WebMessageAsJson](#get_webmessageasjson) | Die Nachricht, die vom WebView-Inhalt an den Host gesendet wurde, der in eine JSON-Zeichenfolge konvertiert wurde.
[TryGetWebMessageAsString](#trygetwebmessageasstring) | Wenn die vom WebView-Inhalt an den Host gesendete Nachricht ein Zeichenfolgentyp ist, gibt diese Methode den Wert dieser Zeichenfolge zurück.

## Member

#### get_Source 

Der URI des Dokuments, das diese Webnachricht gesendet hat.

> öffentliche HRESULT- [get_Source](#get_source)(LPWSTR * Source)

#### get_WebMessageAsJson 

Die Nachricht, die vom WebView-Inhalt an den Host gesendet wurde, der in eine JSON-Zeichenfolge konvertiert wurde.

> Public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR * WebMessageAsJson)

Verwenden Sie diese, um über JavaScript-Objekte zu kommunizieren.

Beispielsweise führen die folgenden PostMessage-Aufrufe zu den folgenden WebMessageAsJson-Werten:

```cpp
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### TryGetWebMessageAsString 

Wenn die vom WebView-Inhalt an den Host gesendete Nachricht ein Zeichenfolgentyp ist, gibt diese Methode den Wert dieser Zeichenfolge zurück.

> Public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR * webMessageAsString)

Wenn die gesendete Nachricht eine andere Art von JavaScript-Typ ist, schlägt diese Methode mit E_INVALIDARG fehl. Verwenden Sie diese, um über einfache Zeichenfolgen zu kommunizieren.

Beispielsweise führen die folgenden PostMessage-Aufrufe zu den folgenden WebMessageAsString-Werten:

```cpp
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

