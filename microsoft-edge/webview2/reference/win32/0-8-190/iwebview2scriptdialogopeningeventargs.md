---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: de8c8cc2c6c6f857a2889ad167061d2834c30c02
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885793"
---
# 0.8.355-Interface-IWebView2ScriptDialogOpeningEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

Ereignis-args für das [IWebView2WebView:: add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) -Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | Der URI der Seite, die das Dialogfeld angefordert hat.
[get_Kind](#get_kind) | Das Dialogfeld "JavaScript-Art"
[get_Message](#get_message) | Die Meldung des Dialogfelds.
[Annehmen](#accept) | Der Host kann dies aufrufen, um mit OK zu antworten, um Dialogfelder zu bestätigen und anzufordern, oder diese Methode nicht aufrufen, um "Cancel" anzugeben.
[get_DefaultText](#get_defaulttext) | Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.
[get_ResultText](#get_resulttext) | Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.
[put_ResultText](#put_resulttext) | Festlegen der ResultText-Eigenschaft
[GetDeferral](#getdeferral) | Getstundung kann aufgerufen werden, um ein [IWebView2Deferral](IWebView2Deferral.md) -Objekt zurückzugeben.

## Member

#### get_Uri 

Der URI der Seite, die das Dialogfeld angefordert hat.

> Public HRESULT [get_Uri](#get_uri)(LPWSTR * URI)

#### get_Kind 

Das Dialogfeld "JavaScript-Art"

> öffentliche HRESULT- [get_Kind](#get_kind)(WEBVIEW2_SCRIPT_DIALOG_KIND * Art)

#### get_Message 

Die Meldung des Dialogfelds.

> öffentliche HRESULT- [get_Message](#get_message)(LPWSTR *-Meldung)

Von JavaScript Dies ist der erste Parameter, der an Alert, Confirm und prompt übergeben wird.

#### Annehmen 

Der Host kann dies aufrufen, um mit OK zu antworten, um Dialogfelder zu bestätigen und anzufordern, oder diese Methode nicht aufrufen, um "Cancel" anzugeben.

> öffentliche HRESULT- [Annahme](#accept)()

Aus JavaScript bedeutet dies, dass die Confirm-Funktion true zurückgibt, wenn Accept aufgerufen wird. Und für die prompt-Funktion gibt Sie den Wert von ResultText zurück, wenn Accept aufgerufen wird, und gibt andernfalls false zurück.

#### get_DefaultText 

Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.

> Public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR * DefaultText)

Dies ist der Standardwert, der für das Ergebnis der Eingabeaufforderung JavaScript-Funktion verwendet wird.

#### get_ResultText 

Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.

> Public HRESULT [get_ResultText](#get_resulttext)(LPWSTR * ResultText)

Dies wird für Dialog Arten außer Eingabeaufforderung ignoriert. Wenn Accept nicht aufgerufen wird, wird dieser Wert ignoriert, und von der Eingabeaufforderung wird false zurückgegeben.

#### put_ResultText 

Festlegen der ResultText-Eigenschaft

> Public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)

#### GetDeferral 

Getstundung kann aufgerufen werden, um ein [IWebView2Deferral](IWebView2Deferral.md) -Objekt zurückzugeben.

> öffentliche HRESULT [getstundung](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) * * Stundung)

Sie können dies verwenden, um das Ereignis zu einem späteren Zeitpunkt abzuschließen.

