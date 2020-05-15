---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 0314c796865d3d745b831d050498f59868e38e8f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654048"
---
# Schnittstellen IWebView2NewVersionAvailableEventArgs 

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

