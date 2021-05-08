---
description: Win32 C++ WebView2-API-Konventionen
title: Win32 C++ WebView2-API-Konventionen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, Webview2, Webview, wpf-Apps, Wpf, Microsoft Edge, ICoreWebView2, ICoreWebView2Host, Browsersteuerung, Edge-HTML
ms.openlocfilehash: b5a86751bfe3386058812ca166fa7cf9e0e201dc
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535643"
---
# <a name="win32-c-webview2-api-conventions"></a>Win32 C++ WebView2-API-Konventionen  

:::row:::
   :::column span="1":::
      Unterstützte Plattformen:
   :::column-end:::
   :::column span="2":::
      Win32
   :::column-end:::
:::row-end:::  

## <a name="prerequisites"></a>Voraussetzungen  

*   Erfahrung mit der Win32-API  

## <a name="async-methods"></a>Async-Methoden  

Asynchrone Methoden in der WebView2 Win32 C++-API verwenden eine Stellvertretungsschnittstelle, um Sie aus den folgenden Gründen zu kontaktieren.  

*   Die async-Methode wurde abgeschlossen.  
*   Der Erfolgs- oder Fehlercode.  
*   Das Ergebnis der asynchronen Methode.  

Der letzte Parameter für alle asynchronen Methoden ist ein Zeiger auf eine Stellvertretungsschnittstelle, von der Sie eine Implementierung bereitstellen.  

Die Stellvertretungsschnittstelle verfügt über eine einzelne Methode, die als erster Parameter einen des Erfolgs- oder `Invoke` `HRESULT` Fehlercodes verwendet.  Darüber hinaus gibt es möglicherweise einen zweiten Parameter, der das Ergebnis der Methode ist, wenn die Methode ein Ergebnis hat.  Beispielsweise verwendet die [ICoreWebView2::CapturePreview-Methode][Webview2ReferenceWin32Icorewebview2CapturePreview] als letzter Parameter einen `ICoreWebView2CapturePreviewCompletedHandler` Zeiger.  Zum Senden einer Methodenanforderung geben Sie eine Instanz des Zeigers an, `CapturePreview` `ICoreWebView2CapturePreviewCompletedHandler` den Sie implementieren.  Im folgenden Codeausschnitt wird eine Methode zum Implementieren verwendet.  

```cpp
HRESULT Invoke(HRESULT result)
```  

Sie implementieren die `Invoke` Methode und fordern ihre Methode `CoreWebView2` `Invoke` an, wenn die Anforderung abgeschlossen `CapturePreview` ist.  Der einzelne Parameter ist die Beschreibung des Erfolgs- oder `HRESULT` Fehlercodes der `CapturePreview` Anforderung.  

Alternativ stellen Sie für eine Instanz mit einer Methode zur Verfügung, die Ihnen den Erfolgs- oder `ICoreWebView2::ExecuteScript` `Invoke` Fehlercode der Anforderung `ExecuteScript` zur Verfügung stellt.  Geben Sie außerdem den zweiten Parameter an, der das JSON des Ergebnisses der Ausführung des Skripts ist.  

Sie können die Stellvertretungsschnittstellen manuell implementieren oder die `CompleteHandler` [Rückruffunktion (Callback Function, WRL) verwenden.][CppCxWrlCallbackFunction]  Die [Rückruffunktion (Callback Function, WRL)][CppCxWrlCallbackFunction] wird im folgenden WebView2-Codeausschnitt verwendet.  

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

## <a name="events"></a>Veranstaltungen  

Ereignisse in der WebView2 Win32 C++-API verwenden das `add_EventName` and-Methodenpaar, um Ereignisse zu abonnieren und `remove_EventName` zu kündigen.  Die `add_EventName` Methode verwendet eine Ereignishandlerdelegiertenschnittstelle und gibt ein Token als `EventRegistrationToken` Ausgabeparameter zurück.  Die `remove_EventName` Methode verwendet ein Token und `EventRegistrationToken` kündigen das entsprechende Ereignisabonnement ab.  

Ereignishandlerdelegiertenschnittstellen funktionieren ähnlich wie die abgeschlossenen Handlerdelegiertenschnittstellen der async-Methode.  Sie implementieren die Stellvertretungsschnittstelle des Ereignishandlers und `CoreWebView2` senden einen Rückruf, wenn das Ereignis ausgeführt wird.  Jede Ereignishandlerdelegiertenschnittstelle verfügt über eine einzelne Methode, die über einen Sender-Parameter gefolgt von `Invoke` einem Ereignis-args-Parameter verfügt.  Der Absender ist die Instanz des Objekts, für das Sie Ereignisse abonniert haben.  Der Ereignis-args-Parameter ist eine Schnittstelle, die Informationen zum aktuell abfeuernden Ereignis enthält.  

Das Ereignis on `NavigationCompleted` hat z. `ICoreWebView2` B. das `ICoreWebView2::add_NavigationCompleted` `ICoreWebView2::remove_NavigationCompleted` Und-Methodenpaar.  Wenn Sie eine Anforderung senden, stellen Sie eine Instanz zur Verfügung, `ICoreWebView2NavigationCompletedEventHandler` in der Sie zuvor eine Methode implementiert `Invoke` haben.  Wenn das `NavigationCompleted` Ereignis ausgeführt wird, wird `Invoke` Ihre Methode angefordert.  Der erste Parameter führt das Ereignis `NavigationCompleted` aus.  Der zweite Parameter enthält Informationen dazu, ob die Navigation erfolgreich abgeschlossen wurde und so weiter.  

Verwenden Sie ähnlich wie bei der async-Methode abgeschlossene Handlerdelegiertenschnittstelle eine der folgenden Aktionen, um sie zu einrichten.  

*   Implementieren Sie es direkt.  
*   Verwenden Sie [die Rückruffunktion (Callback Function, WRL),][CppCxWrlCallbackFunction] die im folgenden WebView2-Codeausschnitt verwendet wird.  

<!-- todo:  what is async method completed handler delegate interface?  Is there a shorter name for it?  -->  

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

## <a name="strings"></a>Zeichenfolgen  

Zeichenfolgenausgabeparameter sind `LPWSTR` zeichenfolgenent terminierte Zeichenfolgen.  Der Anfordernde stellt die Zeichenfolge mithilfe von `CoTaskMemAlloc` zur Verfügung.  Der Besitz wird an den Anantrager übertragen, und es liegt an dem Anantrager, den Arbeitsspeicher mithilfe von frei zu `CoTaskMemFree` stellen.  

Zeichenfolgeneingabeparameter sind `LPCWSTR` zeichenfolgenend beendete Zeichenfolgen.  Der Anser stellt sicher, dass die Zeichenfolge für die Dauer der synchronen Funktionsanforderung gültig ist.  Wenn der Empfänger den Wert bis zu einem bestimmten Punkt speichern muss, nachdem die Funktionsanforderung abgeschlossen ist, muss der Empfänger eine zugeordnete Kopie des Zeichenfolgenwerts angeben.  

## <a name="uri-and-json-parsing"></a>URI- und JSON-Analyse  

Verschiedene Methoden bieten oder akzeptieren URIs und JSON als Zeichenfolgen.  Verwenden Sie Ihre bevorzugte Bibliothek zum Analysen und Generieren der Zeichenfolgen.  

Wenn WinRT für Ihre App verfügbar ist, können Sie die und-Methoden verwenden, um JSON-Zeichenfolgen oder -Methoden zu analysieren oder zu erstellen, um `RuntimeClass_Windows_Data_Json_JsonObject` `IJsonObjectStatics` `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` URIs zu analysieren und zu erzeugen.  Beide Methoden funktionieren in Win32-Apps.  

Wenn Sie URIs verwenden und analysieren, sollten Sie die folgenden `IUri` `CreateUri` URI-Erstellungsflags verwenden, um das Verhalten besser mit der `CreateUri` URI-Analyse in der WebView zu übereinstimmen.  

```json
Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO
```  

## <a name="see-also"></a>Weitere Informationen  

*   Um mit der Verwendung von WebView2 Win32 C/C++ zu beginnen, navigieren Sie zu [Erste Schritte mit WebView2][Webview2IndexGetStarted]-Anleitungen.  
*   Weitere Informationen zu WebView2-APIs finden Sie unter [API-Referenz][DotnetApiMicrosoftWebWebview2WpfWebview2].  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Kontakt mit dem Microsoft Edge WebView-Team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2GetStartedWin32]: ../get-started/win32.md "Erste Schritte mit WebView2 | Microsoft Docs"  

[Webview2ReferenceWin32Icorewebview2CapturePreview]: /microsoft-edge/webview2/reference/win32/icorewebview2#capturepreview "CapturePreview – Schnittstelle ICoreWebView2 | Microsoft Docs"  

[CppCxWrlCallbackFunction]: /cpp/cppcx/wrl/callback-function-wrl "Rückruffunktion (Callback Function, WRL) | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "WebView2-Klasse | Microsoft Docs"  
