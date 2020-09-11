---
description: Win32 C++ WebView2-API-Konventionen
title: Win32 C++ WebView2-API-Konventionen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 6c596b038e871caa5a364991351636f51ef7d685
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010684"
---
# Win32 C++ WebView2-API-Konventionen  

## Async-Methoden  

Asynchrone Methoden in der WebView2 Win32 C++-API verwenden eine Delegate-Schnittstelle, um Ihnen einen Rückruf zu senden, um anzugeben, wann die Async-Methode abgeschlossen wurde, den Erfolgs-oder Fehlercode und für einige das Ergebnis der asynchronen Methode.  Der letzte Parameter für alle asynchronen Methoden ist ein Zeiger auf eine Delegat-Schnittstelle, von der Sie eine Implementierung bereitstellen.  

Die Delegat-Schnittstelle verfügt über eine einzelne `Invoke` Methode, die als erster Parameter eine `HRESULT` des Erfolgs-oder Fehlercodes akzeptiert.  Darüber hinaus gibt es möglicherweise einen zweiten Parameter, der das Ergebnis der Methode ist, wenn die Methode ein Ergebnis hat.  Beispielsweise nimmt die [ICoreWebView2:: CapturePreview] [Webview2ReferenceWin3209538Icorewebview2CapturePreview]-Methode als letzten Parameter einen `ICoreWebView2CapturePreviewCompletedHandler` Zeiger ein.  Um eine `CapturePreview` Methoden Anforderung zu senden, geben Sie eine Instanz des `ICoreWebView2CapturePreviewCompletedHandler` Zeigers an, den Sie implementieren.  Im folgenden Codeausschnitt wird eine Methode zum Implementieren verwendet.  

```cpp
HRESULT Invoke(HRESULT result)
```  

Sie implementieren die `Invoke` Methode und `CoreWebView2` fordern Ihre `Invoke` Methode an, wenn die `CapturePreview` Anforderung abgeschlossen ist.  Der Single `HRESULT` -Parameter beschreibt den Erfolgs-oder Fehlercode der `CapturePreview` Anforderung.  

Oder für `ICoreWebView2::ExecuteScript` , stellen Sie eine Instanz von zur Verfügung, die über `ICoreWebView2ExecuteScriptCompletedHandler` eine `Invoke` Methode verfügt, die Ihnen den Erfolgs-oder Fehlercode der Anforderung sowie den zweiten Parameter bereitstellt, bei dem es sich um die `ExecuteScript` `resultObjectAsJson` JSON des Ergebnisses der Ausführung des Skripts handelt.  

Sie können die `CompleteHandler` Stell Vertretungs Schnittstellen manuell implementieren, oder Sie können die [WRL-Rückruffunktion][CppCxWrlCallbackFunction]verwenden.  Die Rückruffunktion wird im folgenden WebView2-Codeausschnitt verwendet.  

```cpp
void ScriptComponent::InjectScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Inject Script",
        L"Enter script code:",
        L"Enter the JavaScript code to run in the webview.",
        L"window.getComputedStyle(document.body).backgroundColor");
    if (dialog.confirmed)
    {
        m_webView->ExecuteScript(dialog.input.c_str(),
            Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
                [](HRESULT error, PCWSTR result) -> HRESULT
        {
            if (error != S_OK) {
                ShowFailure(error, L"ExecuteScript failed");
            }
            MessageBox(nullptr, result, L"ExecuteScript Result", MB_OK);
            return S_OK;
        }).Get());
    }
}
```  

## Veranstaltungen  

Ereignisse in der WebView2 Win32 C++-API verwenden das `add_EventName` und `remove_EventName` -Methodenpaar, um Ereignisse zu abonnieren und abzubestellen.  Die `add_EventName` Methode verwendet eine Ereignishandler-Delegat Schnittstelle und gibt einen `EventRegistrationToken` als out-Parameter zurück.  Die `remove_EventName` Methode verwendet ein `EventRegistrationToken` -und-Abonnement für das entsprechende Ereignisabonnement.  

Ereignishandler-Delegat-Schnittstellen funktionieren sehr ähnlich wie die von der Async-Methode abgeschlossenen Handler-Delegat Schnittstellen.  Sie implementieren die Ereignishandler-Delegat Schnittstelle und `CoreWebView2` senden einen Rückruf, wenn das Ereignis ausgelöst wird.  Jede Schnittstelle für einen Ereignishandler-Delegat verfügt über eine einzelne `Invoke` Methode, die über einen Sender-Parameter gefolgt von einem Event args-Parameter verfügt.  Der Absender ist die Instanz des Objekts, für das Sie Ereignisse abonniert haben.  Der Ereignis-args-Parameter ist eine Schnittstelle, die Informationen zum aktuell ausgelösten Ereignis enthält.  

Das `NavigationCompleted` Ereignis on weist Beispiels `ICoreWebView2` Weise das `ICoreWebView2::add_NavigationCompleted` und `ICoreWebView2::remove_NavigationCompleted` -Methodenpaar auf.  Wenn Sie Add anfordern, geben Sie eine Instanz an `ICoreWebView2NavigationCompletedEventHandler` , in der Sie zuvor die Methode implementiert haben `Invoke` .  Wenn das `NavigationCompleted` Ereignis ausgelöst wird, `Invoke` wird die Methode angefordert.  Der erste Parameter ist das `ICoreWebView2` Auslösen des `NavigationCompleted` Ereignisses.  Der zweite Parameter ist der `ICoreWebView2NavigationCompletedEventArgs` , der Informationen darüber enthält, ob die Navigation erfolgreich abgeschlossen wurde usw.  

Ähnlich wie bei der durch die Async-Methode abgeschlossenen Handler-Delegat-Schnittstelle können Sie Sie direkt selbst implementieren, oder Sie können die WRL-Rückruffunktion verwenden, die im folgenden WebView2-Codeausschnitt verwendet wird.  

```cpp
// Register a handler for the NavigationCompleted event.
// Check whether the navigation succeeded, and if not, do something.
// Also update the Cancel buttons.
CHECK_FAILURE(m_webView->add_NavigationCompleted(
    Callback<ICoreWebView2NavigationCompletedEventHandler>(
        [this](ICoreWebView2* sender, ICoreWebView2NavigationCompletedEventArgs* args)
            -> HRESULT {
            BOOL success;
            CHECK_FAILURE(args->get_IsSuccess(&success));
            if (!success)
            {
                COREWEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                if (webErrorStatus == COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                {
                    // Do something here if you want to handle a specific error case.
                    // In most cases it is not necessary, because the WebView
                    // displays an error page automatically.
                }
            }
            m_toolbar->SetItemEnabled(Toolbar::Item_CancelButton, false);
            m_toolbar->SetItemEnabled(Toolbar::Item_ReloadButton, true);
            return S_OK;
        })
        .Get(),
    &m_navigationCompletedToken));
```  

## Zeichenfolgen  

Zeichenfolgenparameter sind `LPWSTR` NULL-terminierte Zeichenfolgen.  Der Anforderer ordnet die Zeichenfolge mithilfe von `CoTaskMemAlloc` .  Der Besitz wird an den anfordernden übertragen, und es ist Aufgabe des anfordernden, den Speicher mit zu befreien `CoTaskMemFree` .  

Zeichenfolge in Parametern sind `LPCWSTR` NULL-terminierte Zeichenfolgen.  Der Anforderer stellt sicher, dass die Zeichenfolge für die Dauer der synchronen Funktionsanforderung gültig ist.  Wenn der Empfänger diesen Wert bis zu einem gewissen Punkt beibehalten muss, nachdem die Funktionsanforderung abgeschlossen ist, muss der Empfänger eine zugeordnete Kopie des Zeichenfolgenwerts zuweisen.  

## URI-und JSON-Analyse  

Verschiedene Methoden stellen URIs und JSON als Zeichenfolgen bereit oder akzeptieren Sie.  Verwenden Sie bitte Ihre eigene bevorzugte Bibliothek, um die Zeichenfolgen zu analysieren und zu generieren.  

Wenn WinRT für Ihre app verfügbar ist, können Sie die `RuntimeClass_Windows_Data_Json_JsonObject` Methoden und verwenden, `IJsonObjectStatics` um JSON-Zeichenfolgen oder `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` Methoden zum Analysieren und Erstellen von URIs zu analysieren oder zu erzeugen.  Beide Methoden funktionieren in Win32-apps.  

Wenn Sie `IUri` URIs verwenden und `CreateUri` analysieren, sollten Sie die folgenden URI-Erstellungs Flags verwenden, damit `CreateUri` das Verhalten der URI-Analyse in der WebView genauer entspricht.  

```json
Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO
```  

<!-- links -->  

[Webview2ReferenceWin3209622Icorewebview2CapturePreview]: ../reference/win32/0-9-622/icorewebview2.md#capturepreview "CapturePreview-Interface-ICoreWebView2 | Microsoft docs"  

[CppCxWrlCallbackFunction]: /cpp/cppcx/wrl/callback-function-wrl "Callback-Funktion (WRL) | Microsoft docs"  
