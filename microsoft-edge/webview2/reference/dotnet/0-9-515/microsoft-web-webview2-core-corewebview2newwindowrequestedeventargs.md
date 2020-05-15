---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: cca15ccc5292f5eaf6f317ffb657f46fcd84b4a9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654084"
---
# Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs Klasse 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

Ereignis-args für das mswebviewnewwindowrequested-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Handled](#handled) | Gibt an, ob der NewWindowRequestedEvent vom Host verarbeitet wird.
[IsUserInitiated](#isuserinitiated) | IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.
[NewWindow](#newwindow) | Ruft das neue Fenster ab.
[URI](#uri) | Der Ziel-URI des NewWindowRequest.
[GetDeferral](#getdeferral) | Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.

Das Ereignis wird ausgelöst, wenn Inhalt in WebView zum Öffnen eines neuen Fensters angefordert wird (über Window. Open () usw.).

## Member

#### Handled 

Gibt an, ob der NewWindowRequestedEvent vom Host verarbeitet wird.

> öffentliche bool- [Behandlung](#handled)

Wenn dies falsch ist und kein Fenster festgelegt ist, wird die WebView ein Popupfenster geöffnet und als geöffnetes WindowProxy zurückgegeben. Wenn Sie auf "true" festgelegt ist und kein Fenster für einen Window. Open-Aufruf festgelegt ist, wird das geöffnete WindowProxy-Objekt für ein Dummy Window-Objekt und es wird kein Fenster geladen. Der Standardwert ist false.

#### IsUserInitiated 

IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.

> public bool [IsUserInitiated](#isuserinitiated)

#### NewWindow 

Ruft das neue Fenster ab.

> öffentliches CoreWebView2- [Fenster](#newwindow)

#### URI 

Der Ziel-URI des NewWindowRequest.

> öffentlicher Zeichenfolgen- [URI](#uri)

Die Ziel-WebView sollte nicht navigiert werden. Wenn das Fenster "Fenster" eingestellt ist, wird das Fenster der obersten Ebene als geöffnetes WindowProxy zurückgegeben.

#### GetDeferral 

Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.

> Public CoreWebView2Deferral [getstundungal](#getdeferral)()

Sie können das CoreWebView2Deferral-Objekt verwenden, um die geöffnete Fenster Anforderung zu einem späteren Zeitpunkt abzuschließen. Während dieses Ereignis verzögert wird, wird das Opener-Fenster eine WindowProxy zu einem unnavigierten Fenster zurückgegeben, das nach Abschluss der Verzögerungszeit navigiert.

