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
ms.openlocfilehash: 6d4c5e7893f9be78baca25e8976ca889ef9826c0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654057"
---
# Schnittstellen ICoreWebView2SourceChangedEventArgs 

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

