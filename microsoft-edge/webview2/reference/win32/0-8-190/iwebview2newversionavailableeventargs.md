---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2NewVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: e8965ebe2e0434d83b4d6e8eabe74466adb7cec6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878344"
---
# 0.8.355-Interface-IWebView2NewVersionAvailableEventArgs 

> [!NOTE]
> Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein. Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .

```
interface IWebView2NewVersionAvailableEventArgs
  : public IUnknown
```

Ereignis-args für das NewVersionAvailable-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_NewVersion](#get_newversion) | Die Browser Versionsinformationen des aktuellen [IWebView2Environment](IWebView2Environment.md).

## Member

#### get_NewVersion 

Die Browser Versionsinformationen des aktuellen [IWebView2Environment](IWebView2Environment.md).

> Public HRESULT [get_NewVersion](#get_newversion)(LPWSTR *-Version)

