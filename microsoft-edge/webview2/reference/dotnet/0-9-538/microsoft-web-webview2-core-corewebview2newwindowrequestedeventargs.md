---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 54e2c06ef65f64560fbd5687148eace253352203
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698777"
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
[WindowFeatures](#windowfeatures) | Fenster Features, die vom Window. Open-Anruf angegeben werden.
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

#### WindowFeatures 

> [!NOTE]
> Hierbei handelt es sich um eine [experimentelle API](../../../concepts/versioning.md#experimental-apis) , die mit unserer SDK [-Version 0.9.538-Prerelease](../../../releasenotes.md#09538)ausgeliefert wurde.

Fenster Features, die vom Window. Open-Anruf angegeben werden.

> öffentliche CoreWebView2WindowFeatures- [WindowFeatures](#windowfeatures)

Diese Features können beim Positionieren und Ändern der Größe von neuen WebView-Fenstern berücksichtigt werden.

#### GetDeferral 

Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.

> Public CoreWebView2Deferral [getstundungal](#getdeferral)()

Sie können das CoreWebView2Deferral-Objekt verwenden, um die geöffnete Fenster Anforderung zu einem späteren Zeitpunkt abzuschließen. Während dieses Ereignis verzögert wird, wird das Opener-Fenster eine WindowProxy zu einem unnavigierten Fenster zurückgegeben, das nach Abschluss der Verzögerungszeit navigiert.

