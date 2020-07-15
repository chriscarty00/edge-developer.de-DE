---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: f59b5acac510b66eae0e1ada51e28b6dd9363ca8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877854"
---
# 0.9.430-Interface-ICoreWebView2NewBrowserVersionAvailableEventArgs 

> [!NOTE]
> Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein. Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .

```
interface ICoreWebView2NewBrowserVersionAvailableEventArgs
  : public IUnknown
```

Ereignis-args für das NewBrowserVersionAvailable-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_NewVersion](#get_newversion) | Die Browser Versionsinformationen des aktuellen [ICoreWebView2Environment](ICoreWebView2Environment.md).

## Member

#### get_NewVersion 

Die Browser Versionsinformationen des aktuellen [ICoreWebView2Environment](ICoreWebView2Environment.md).

> Public HRESULT [get_NewVersion](#get_newversion)(LPWSTR *-Version)

