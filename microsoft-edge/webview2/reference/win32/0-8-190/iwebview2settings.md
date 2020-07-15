---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 94c6d6c424d715d3b6b57b366b71cf8e5fb8ec42
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878211"
---
# 0.8.355-Interface-IWebView2Settings 

> [!NOTE]
> Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein. Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .

```
interface IWebView2Settings
  : public IUnknown
```

Definiert Eigenschaften, die WebView-Features aktivieren, deaktivieren oder ändern.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_IsScriptEnabled](#get_isscriptenabled) | Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.
[put_IsScriptEnabled](#put_isscriptenabled) | Festlegen der IsScriptEnabled-Eigenschaft
[get_IsWebMessageEnabled](#get_iswebmessageenabled) | Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.
[put_IsWebMessageEnabled](#put_iswebmessageenabled) | Festlegen der IsWebMessageEnabled-Eigenschaft
[get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled) | AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.
[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled) | Festlegen der AreDefaultScriptDialogsEnabled-Eigenschaft
[get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated) | Diese Einstellung ist veraltet und gibt immer false zurück.
[put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated) | Diese Einstellung ist veraltet und hat keine Auswirkungen.
[get_IsStatusBarEnabled](#get_isstatusbarenabled) | IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.
[put_IsStatusBarEnabled](#put_isstatusbarenabled) | Festlegen der IsStatusBarEnabled-Eigenschaft
[get_AreDevToolsEnabled](#get_aredevtoolsenabled) | AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.
[put_AreDevToolsEnabled](#put_aredevtoolsenabled) | Festlegen der AreDevToolsEnabled-Eigenschaft

Das Festlegen von Änderungen, die nach dem NavigationStarting-Ereignis vorgenommen wurden, wird erst nach der nächsten Navigation auf oberster Ebene übernommen.

## Member

#### get_IsScriptEnabled 

Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.

> Public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool * IsScriptEnabled)

Dies wirkt sich nur auf Skripts im Dokument aus. mit executeScript injizierte Skripts werden auch dann ausgeführt, wenn das Skript deaktiviert ist. Standardmäßig ist dies der Fall.

```cpp
        // Changes to settings will apply at the next navigation, which includes the
        // navigation after a NavigationStarting event.  We can use this to change
        // settings according to what site we're visiting.
        if (ShouldBlockScriptForUri(uri.get()))
        {
            m_settings->put_IsScriptEnabled(FALSE);
        }
        else
        {
            m_settings->put_IsScriptEnabled(m_isScriptEnabled);
        }
```

#### put_IsScriptEnabled 

Festlegen der IsScriptEnabled-Eigenschaft

> Public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(bool IsScriptEnabled)

#### get_IsWebMessageEnabled 

Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.

> Public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool * IsWebMessageEnabled)

Wenn Sie auf "true" festgelegt ist, ist die Kommunikation zwischen dem Host und dem HTML-Dokument der obersten Ebene der WebView über das PostWebMessageAsJson-, PostWebMessageAsString-und Window. Chrome. WebView-Nachrichtenereignis zulässig (Weitere Informationen finden Sie in der PostWebMessageAsJson-Dokumentation). Die Kommunikation vom HTML-Dokument der WebView-obersten Ebene an den Host ist über die Funktion "PostMessage" von Window. Chrome. WebView und die SetWebMessageReceivedEventHandler-Methode möglich (Einzelheiten finden Sie in der SetWebMessageReceivedEventHandler-Dokumentation). Wenn Sie auf "false" festgelegt ist, ist die Kommunikation nicht zulässig. Bei PostWebMessageAsJson und PostWebMessageAsString tritt ein Fehler auf, wenn E_ACCESSDENIED und Window. Chrome. WebView. PostMessage fehlschlägt, indem Sie eine Instanz eines Error-Objekts auslösen. Standardmäßig ist dies der Fall.

```cpp
    ComPtr<IWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### put_IsWebMessageEnabled 

Festlegen der IsWebMessageEnabled-Eigenschaft

> Public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(bool IsWebMessageEnabled)

#### get_AreDefaultScriptDialogsEnabled 

AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.

> Public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool * AreDefaultScriptDialogsEnabled)

Wenn Sie auf "false" festgelegt ist, rendert WebView das Standarddialogfeld für JavaScript nicht (insbesondere die in den Funktionen JavaScript-Benachrichtigung, Bestätigung und Eingabeaufforderung angezeigten Funktionen). Wenn ein Ereignishandler von SetScriptDialogOpeningEventHandler festgesetzt wird, sendet WebView stattdessen ein Ereignis, das alle Informationen für das Dialogfeld enthält, und es der Host-App gestatten, eine eigene benutzerdefinierte Benutzeroberfläche anzuzeigen.

#### put_AreDefaultScriptDialogsEnabled 

Festlegen der AreDefaultScriptDialogsEnabled-Eigenschaft

> Public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(bool AreDefaultScriptDialogsEnabled)

#### get_IsFullscreenAllowed_deprecated 

Diese Einstellung ist veraltet und gibt immer false zurück.

> Public HRESULT [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)(bool * IsFullscreenAllowed)

Das bedeutet, dass Elemente in der WebView nur die WebView-Begrenzungen ausfüllen. Diese Eigenschaft wird dann vollständig entfernt. Bitte hören Sie sich stattdessen das ContainsFullScreenElementChanged-Ereignis an.

Steuert, ob Vollbild für Elemente in der WebView zulässig ist. Wenn dies zulässig ist, können Webinhalte, wie ein Video Element in der WebView, im Vollbildmodus angezeigt werden. Wenn dies nicht zulässig ist, füllt ein solches Element die WebView-Begrenzungen aus, wenn das Element den Vollbildmodus anfordert. Standardmäßig ist dies der Fall.

#### put_IsFullscreenAllowed_deprecated 

Diese Einstellung ist veraltet und hat keine Auswirkungen.

> Public HRESULT [put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)(bool IsFullscreenAllowed)

Bitte hören Sie sich stattdessen das ContainsFullScreenElementChanged-Ereignis an.

Festlegen der IsFullscreenAllowed-Eigenschaft

#### get_IsStatusBarEnabled 

IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.

> Public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool * IsStatusBarEnabled)

Die Statusleiste wird normalerweise in der unteren linken Ecke der WebView angezeigt und zeigt Elemente wie den URI eines Links an, wenn der Benutzer darüber schwebt, und weitere Informationen. Standardmäßig ist dies der Fall.

#### put_IsStatusBarEnabled 

Festlegen der IsStatusBarEnabled-Eigenschaft

> Public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(bool IsStatusBarEnabled)

#### get_AreDevToolsEnabled 

AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.

> Public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool * AreDevToolsEnabled)

Standardmäßig ist dies der Fall.

#### put_AreDevToolsEnabled 

Festlegen der AreDevToolsEnabled-Eigenschaft

> Public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(bool AreDevToolsEnabled)

