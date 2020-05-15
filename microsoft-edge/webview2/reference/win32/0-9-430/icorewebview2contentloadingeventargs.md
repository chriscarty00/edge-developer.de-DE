---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: c3ba6ac3a2478861abb7b26e726a9cbd606b0eb9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653883"
---
# Schnittstellen ICoreWebView2ContentLoadingEventArgs 

> [!NOTE]
> Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein. Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

Ereignis-args für das ContentLoading-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_IsErrorPage](#get_iserrorpage) | "True", wenn der geladene Inhalt eine Fehlerseite ist.
[get_NavigationId](#get_navigationid) | Die ID der Navigation.

## Member

#### get_IsErrorPage 

"True", wenn der geladene Inhalt eine Fehlerseite ist.

> Public HRESULT [get_IsErrorPage](#get_iserrorpage)(bool * IsErrorPage)

#### get_NavigationId 

Die ID der Navigation.

> Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 * navigation_id)

