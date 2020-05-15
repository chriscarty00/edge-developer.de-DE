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
ms.openlocfilehash: 62daeaab702b431f787bc800ab79664fc183c4ce
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653706"
---
# Schnittstellen IWebView2WebView2 

> [!NOTE]
> Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein. Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .

```
interface IWebView2WebView2
  : public IUnknown
```

Zusätzliche Funktionen, die vom primären WebView-Objekt implementiert werden.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Stop](#stop) | Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.

Sie können QueryInterface für diese Schnittstelle aus dem Objekt, das [IWebView2WebView](IWebView2WebView.md)implementiert. Weitere Informationen finden Sie auf der [IWebView2WebView](IWebView2WebView.md) -Benutzeroberfläche.

## Member

#### Stop 

Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.

> öffentlicher HRESULT- [Stopp](#stop)()

