---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 8ea9437530a7f64cc045bfbaa1cc3cc55da77732
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698141"
---
# Schnittstellen ICoreWebView2SourceChangedEventArgs 

> [!NOTE]
> Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen. Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

Ereignis-args für das Sourcecode-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_IsNewDocument](#get_isnewdocument) | "True", wenn die zu navigierende Seite ein neues Dokument ist.

## Member

#### get_IsNewDocument 

"True", wenn die zu navigierende Seite ein neues Dokument ist.

> Public HRESULT [get_IsNewDocument](#get_isnewdocument)(bool * IsNewDocument)

