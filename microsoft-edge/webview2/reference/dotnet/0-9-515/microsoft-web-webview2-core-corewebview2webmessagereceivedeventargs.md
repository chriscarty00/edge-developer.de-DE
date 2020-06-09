---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: b917f309194316b26ee94aa94dc8289ef4430007
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697539"
---
# Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs Klasse 

> [!NOTE]
> Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen. Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

Ereignis-args für das WebMessageReceived-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Source](#source) | Der URI des Dokuments, das diese Webnachricht gesendet hat.
[WebMessageAsJson](#webmessageasjson) | Die Nachricht, die vom WebView-Inhalt an den Host gesendet wurde, der in eine JSON-Zeichenfolge konvertiert wurde.
[TryGetWebMessageAsString](#trygetwebmessageasstring) | Wenn die vom WebView-Inhalt an den Host gesendete Nachricht ein Zeichenfolgentyp ist, gibt diese Methode den Wert dieser Zeichenfolge zurück.

## Member

#### Source 

Der URI des Dokuments, das diese Webnachricht gesendet hat.

> öffentliche Zeichenfolgen [Quelle](#source)

#### WebMessageAsJson 

Die Nachricht, die vom WebView-Inhalt an den Host gesendet wurde, der in eine JSON-Zeichenfolge konvertiert wurde.

> public String [WebMessageAsJson](#webmessageasjson)

Verwenden Sie diese, um über JavaScript-Objekte zu kommunizieren.

Beispielsweise führen die folgenden PostMessage-Aufrufe zu den folgenden WebMessageAsJson-Werten:

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### TryGetWebMessageAsString 

Wenn die vom WebView-Inhalt an den Host gesendete Nachricht ein Zeichenfolgentyp ist, gibt diese Methode den Wert dieser Zeichenfolge zurück.

> public String [TryGetWebMessageAsString](#trygetwebmessageasstring)()

Wenn die gesendete Nachricht eine andere Art von JavaScript-Typ ist, schlägt diese Methode mit E_INVALIDARG fehl. Verwenden Sie diese, um über einfache Zeichenfolgen zu kommunizieren.

Beispielsweise führen die folgenden PostMessage-Aufrufe zu den folgenden WebMessageAsString-Werten:

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

