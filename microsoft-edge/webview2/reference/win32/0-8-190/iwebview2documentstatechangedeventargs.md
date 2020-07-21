---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2DocumentStateChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 75741c1ba1d835d1c26c7d1db0845071216e0705
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886122"
---
# 0.8.355-Interface-IWebView2DocumentStateChangedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2DocumentStateChangedEventArgs
  : public IUnknown
```

Ereignis-args für das DocumentStateChanged-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_IsNewDocument](#get_isnewdocument) | "True", wenn die zu navigierende Seite ein neues Dokument ist.
[get_IsErrorPage](#get_iserrorpage) | "True", wenn der geladene Inhalt eine Fehlerseite ist.

## Member

#### get_IsNewDocument 

"True", wenn die zu navigierende Seite ein neues Dokument ist.

> Public HRESULT [get_IsNewDocument](#get_isnewdocument)(bool * IsNewDocument)

#### get_IsErrorPage 

"True", wenn der geladene Inhalt eine Fehlerseite ist.

> Public HRESULT [get_IsErrorPage](#get_iserrorpage)(bool * IsErrorPage)

