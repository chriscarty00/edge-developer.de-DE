---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 798c3ce0a3eeddad651668124d6a263d0672a391
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877840"
---
# 0.9.430-Interface-ICoreWebView2NewWindowRequestedEventArgs 

> [!NOTE]
> Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein. Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

Ereignis-args für das mswebviewnewwindowrequested-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | Der Ziel-URI des NewWindowRequest.
[put_NewWindow](#put_newwindow) | Legt eine WebView als Ergebnis des NewWindowRequest fest.
[get_NewWindow](#get_newwindow) | Ruft das neue Fenster ab.
[put_Handled](#put_handled) | Legt fest, ob die NewWindowRequestedEvent vom Host verarbeitet wird.
[get_Handled](#get_handled) | Ruft ab, ob die NewWindowRequestedEvent vom Host verarbeitet wird.
[get_IsUserInitiated](#get_isuserinitiated) | IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.
[GetDeferral](#getdeferral) | Rufen Sie ein [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.

Das Ereignis wird ausgelöst, wenn Inhalt in WebView zum Öffnen eines neuen Fensters angefordert wird (durch Window. Open () usw.).

## Member

#### get_Uri 

Der Ziel-URI des NewWindowRequest.

> Public HRESULT [get_Uri](#get_uri)(LPWSTR * URI)

#### put_NewWindow 

Legt eine WebView als Ergebnis des NewWindowRequest fest.

> öffentliche HRESULT- [put_NewWindow](#put_newwindow)([ICoreWebView2](ICoreWebView2.md) *-Fenster)

Die Ziel-WebView sollte nicht navigiert werden. Wenn das Fenster "Fenster" eingestellt ist, wird das Fenster der obersten Ebene als geöffnetes WindowProxy zurückgegeben.

#### get_NewWindow 

Ruft das neue Fenster ab.

> öffentliche HRESULT- [get_NewWindow](#get_newwindow)([ICoreWebView2](ICoreWebView2.md) * *-Fenster)

#### put_Handled 

Legt fest, ob die NewWindowRequestedEvent vom Host verarbeitet wird.

> öffentliche HRESULT- [put_Handled](#put_handled)(bool Handled)

Wenn dies falsch ist und kein Fenster festgelegt ist, wird die WebView ein Popupfenster geöffnet und als geöffnetes WindowProxy zurückgegeben. Wenn Sie auf "true" festgelegt ist und kein Fenster für einen Window. Open-Aufruf festgelegt ist, wird das geöffnete WindowProxy-Objekt für ein Dummy Window-Objekt und es wird kein Fenster geladen. Der Standardwert ist false.

#### get_Handled 

Ruft ab, ob die NewWindowRequestedEvent vom Host verarbeitet wird.

> öffentliche HRESULT- [get_Handled](#get_handled)(bool * Handled)

#### get_IsUserInitiated 

IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.

> Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool * IsUserInitiated)

#### GetDeferral 

Rufen Sie ein [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.

> öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) * * Stundung)

Sie können das [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt verwenden, um die geöffnete Fenster Anforderung zu einem späteren Zeitpunkt abzuschließen. Während dieses Ereignis verzögert wird, wird das Opener-Fenster eine WindowProxy zu einem unnavigierten Fenster zurückgegeben, das nach Abschluss der Verzögerungszeit navigiert.

