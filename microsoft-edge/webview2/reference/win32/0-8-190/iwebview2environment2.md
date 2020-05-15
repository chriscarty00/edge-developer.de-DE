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
ms.openlocfilehash: 00b19d1174a5d5ac643a04038ecdd60c82211194
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653966"
---
# Schnittstellen IWebView2Environment2 

> [!NOTE]
> Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein. Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .

```
interface IWebView2Environment2
  : public IWebView2Environment
```

Zusätzliche vom Environment-Objekt implementierte Funktionalität.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_BrowserVersionInfo](#get_browserversioninfo) | Die Browser Versionsinformationen des aktuellen [IWebView2Environment](IWebView2Environment.md), einschließlich des Kanal namens, wenn es sich nicht um den stabilen Kanal handelt.

Weitere Informationen finden Sie auf der [IWebView2Environment](IWebView2Environment.md) -Benutzeroberfläche. Sie können QueryInterface für diese Schnittstelle aus dem Objekt, das [IWebView2Environment](IWebView2Environment.md)implementiert.

## Member

#### get_BrowserVersionInfo 

Die Browser Versionsinformationen des aktuellen [IWebView2Environment](IWebView2Environment.md), einschließlich des Kanal namens, wenn es sich nicht um den stabilen Kanal handelt.

> Public HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR * VERSIONINFO)

Dies entspricht dem Format der GetWebView2BrowserVersionInfo-API. Kanalnamen sind "Beta", "dev" und "Canary".

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

