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
ms.openlocfilehash: 6ebed9e61bf7eda60e6e16b7a417306baa5d07bf
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653713"
---
# Schnittstellen IWebView2WebView4 

> [!NOTE]
> Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein. Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .

```
interface IWebView2WebView4
  : public IWebView2WebView3
```

Zusätzliche Funktionen, die vom primären WebView-Objekt implementiert werden.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Addremoteobject](#addremoteobject) | Fügen Sie das bereitgestellte Hostobjekt zu Skript hinzu, das in der WebView mit dem angegebenen Namen ausgeführt wird.
[RemoveRemoteObject](#removeremoteobject) | Entfernen Sie das vom Namen angegebene Hostobjekt, damit es nicht mehr über JavaScript-Code in der WebView zugänglich ist.
[OpenDevToolsWindow](#opendevtoolswindow) | Öffnet das devtools-Fenster für das aktuelle Dokument in der WebView.
[add_AcceleratorKeyPressed](#add_acceleratorkeypressed) | Fügen Sie einen Ereignishandler für das AcceleratorKeyPressed-Ereignis hinzu.
[remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed) | Entfernen Sie einen Ereignishandler, der zuvor mit add_AcceleratorKeyPressed hinzugefügt wurde.
[WEBVIEW2_KEY_EVENT_TYPE](#webview2_key_event_type) | Der Typ des Schlüssel Ereignisses, das ein AcceleratorKeyPressed-Ereignis ausgelöst hat.
[WEBVIEW2_PHYSICAL_KEY_STATUS](#webview2_physical_key_status) | Eine Struktur, die die Informationen darstellt, die in lParam verpackt sind, die einem Win32-Schlüsselereignis zugewiesen wurden.

Sie können QueryInterface für diese Schnittstelle aus dem Objekt, das [IWebView2WebView](IWebView2WebView.md)implementiert. Weitere Informationen finden Sie auf der [IWebView2WebView](IWebView2WebView.md) -Benutzeroberfläche.

## Member

#### Addremoteobject 

Fügen Sie das bereitgestellte Hostobjekt zu Skript hinzu, das in der WebView mit dem angegebenen Namen ausgeführt wird.

> Public HRESULT [addremoteobject](#addremoteobject)(LPCWSTR-Name, Variant *-Objekt)

Host Objekte werden als Remoteobjekt Proxys über bereitgestellt `window.chrome.webview.remoteObjects.<name>` . Remote Objektproxys sind Versprechungen und werden in ein Objekt aufgelöst, das das Hostobjekt darstellt. Das Versprechen wird abgelehnt, wenn die APP kein Objekt mit dem Namen hinzugefügt hat. Wenn JavaScript-Code auf eine Eigenschaft oder Methode des Objekts zugreift, wird eine Zusage zurückgegeben, die in den Wert aufgelöst wird, der vom Host für die Eigenschaft oder Methode zurückgegeben wird, oder im Fall eines Fehlers abgelehnt wird, beispielsweise wenn keine solche Eigenschaft oder Methode für das Objekt vorhanden ist oder Parameter ungültig sind. Wenn der Anwendungscode beispielsweise Folgendes durchführt: 

```cpp
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddRemoteObject(L"host_object", &host);
```

 JavaScript-Code in der WebView kann auf appObject wie folgt zugreifen und dann auf Attribute und Methoden von appObject zugreifen: 

```js
let app_object = await window.chrome.webview.remoteObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

 Beachten Sie, dass einfache Typen, IDispatch und Array unterstützt werden, generische IUnknown, VT_DECIMAL oder VT_RECORD Variant nicht unterstützt werden. Remote-JavaScript-Objekte wie Rückruffunktionen werden als VT_DISPATCH Variante mit dem Object-Implementierungs-IDispatch dargestellt. Die JavaScript-Rückrufmethode kann mit DISPID_VALUE für die DISPID aufgerufen werden. Geschachtelte Arrays werden bis zu einer Tiefe von 3 unterstützt. Arrays von nach Verweistypen werden nicht unterstützt. VT_EMPTY und VT_NULL werden JavaScript als NULL zugeordnet. In JavaScript werden NULL und undefined VT_EMPTY zugeordnet.

Darüber hinaus werden alle Remoteobjekte als verfügbar gemacht `window.chrome.webview.remoteObjects.sync.<name>` . Hier werden die Hostobjekte als synchrone Remoteobjekt Proxys verfügbar gemacht. Hierbei handelt es sich nicht um Versprechungen und Aufrufe von Funktionen oder des Eigenschafts Zugriffs, die ein synchrones Blockieren des ausgeführten Skripts warten, um die Ausführung des Host Codes zu kommunizieren. Dementsprechend kann dies zu Zuverlässigkeitsproblemen führen, und es wird empfohlen, dass Sie die oben beschriebene Versprechen-basierte asynchrone `window.chrome.webview.remoteObjects.<name>` API verwenden.

Synchrone Remoteobjekt Proxys und asynchrone Remoteobjekt Proxys können sowohl Proxys für dasselbe Remoteobjekt als auch Proxys sein. Remote Änderungen, die von einem Proxy durchgeführt werden, werden in jedem anderen Proxy desselben Remoteobjekts widergespiegelt, unabhängig davon, ob die anderen Proxys synchron oder asynchron sind.

Während JavaScript bei einem synchronen Aufruf von systemeigenem Code blockiert wird, kann dieser systemeigene Code nicht mehr in JavaScript zurückrufen. Der Versuch, dies zu tun, schlägt mit HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK) fehl.

Remote Objektproxys sind JavaScript-Proxy Objekte, die alle Eigenschaften abrufen, Eigenschaftensätze und Methodenaufrufe abfangen. Eigenschaften oder Methoden, die Teil des Funktions-oder Objekt Prototyps sind, werden lokal ausgeführt. Darüber hinaus werden alle Eigenschaften oder Methoden im Array `chrome.webview.remoteObjects.options.forceLocalProperties` lokal ausgeführt. Diese Option enthält standardmäßig optionale Methoden, die in JavaScript wie und in Bedeutung sind `toJSON` `Symbol.toPrimitive` . Sie können diesem Array nach Bedarf weitere hinzufügen.

Es gibt eine Methode `chrome.webview.remoteObjects.cleanupSome` , mit der die Garbage Collection von Remoteobjekt Proxys am besten abläuft.

Für Remote Objektproxys gibt es zusätzlich die folgenden Methoden, die lokal ausgeführt werden:

* applyRemote, getRemote, setremote: Durchführen eines Methodenaufrufs, eines Eigenschaften Abstands oder eines Eigenschaftssatzes für das Remoteobjekt. Mit diesen können Sie explizit erzwingen, dass eine Methode oder Eigenschaft Remote ausgeführt wird, wenn eine in Konflikt stehende lokale Methode oder Eigenschaft vorhanden ist. Beispielsweise führt `proxy.toString()` die lokale ToString-Methode für das Proxyobjekt aus. `proxy.applyRemote('toString')`Wird aber `toString` stattdessen auf dem Remoteproxy Objekt ausgeführt.

* getLocal, setlocal: führt Eigenschaften abrufen oder Eigenschaftssatz lokal aus. Sie können diese Methoden verwenden, um das Abrufen oder Festlegen einer Eigenschaft für den Remoteobjekt Proxy selbst und nicht für das Remoteobjekt zu erzwingen, das es darstellt. Beispielsweise `proxy.unknownProperty` wird die Eigenschaft abgerufen, die `unknownProperty` aus dem Remoteproxy Objekt benannt wurde. `proxy.getLocal('unknownProperty')`Der Wert der Eigenschaft wird jedoch `unknownProperty` für das Proxyobjekt selbst abgerufen.

* Synchronisierung: asynchrone Remoteobjekt Proxys machen eine Synchronisierungsmethode verfügbar, die ein Versprechen für einen synchronen Remoteobjekt Proxy für das gleiche Remoteobjekt zurückgibt. Gibt beispielsweise `chrome.webview.remoteObjects.sample.methodCall()` einen asynchronen Remoteobjekt Proxy zurück. Sie können stattdessen die `sync` Methode zum Abrufen eines synchronen Remoteobjekt Proxys verwenden: `const syncProxy = await chrome.webview.remoteObjects.sample.methodCall().sync()`

* Async: synchrone Remoteobjekt Proxys machen eine asynchrone Methode verfügbar, die einen asynchronen Remoteobjekt Proxy für das gleiche Remoteobjekt blockiert und zurückgibt. Gibt beispielsweise `chrome.webview.remoteObjects.sync.sample.methodCall()` einen synchronen Remoteobjekt Proxy zurück. Aufruf der `async` Methode für diesen Block und anschließendes zurückgeben eines asynchronen Remoteobjekt Proxys für dasselbe Remoteobjekt: `const asyncProxy = chrome.webview.remoteObjects.sync.sample.methodCall().async()`

* dann: asynchrone Remoteobjekt Proxys verfügen über eine then-Methode. Auf diese Weise können Sie warten. `then` gibt eine Verheißung zurück, die mit einer Darstellung des Remoteobjekts aufgelöst wird. Wenn der Proxy ein JavaScript-Literal darstellt, wird eine Kopie davon lokal zurückgegeben. Wenn der Proxy eine Funktion darstellt, wird ein nicht erwarteter Proxy zurückgegeben. Wenn der Proxy ein JavaScript-Objekt mit einer Kombination aus Literalen Eigenschaften und Funktionseigenschaften darstellt, wird eine Kopie des Objekts mit einigen Eigenschaften als Remoteobjekt Proxys zurückgegeben.

Alle anderen Eigenschaften-und Methodenaufrufe (außer den oben genannten Methoden für Remote Objektproxy, forceLocalProperties-Liste und Eigenschaften für Funktions-und Objekt Prototypen) werden Remote ausgeführt. Asynchrone Remoteobjekt Proxys geben eine Versprechung zurück, die den asynchronen Abschluss des Remoteaufrufs der Methode oder das Abrufen der Eigenschaft darstellt. Das Versprechen wird aufgelöst, nachdem die Remotevorgänge abgeschlossen sind und die Zusagen in den resultierenden Wert des Vorgangs aufgelöst werden. Synchrone Remoteobjekt Proxys funktionieren ähnlich, blockieren aber die JavaScript-Ausführung und warten, bis der Remotevorgang abgeschlossen ist.

Das Festlegen einer Eigenschaft für einen asynchronen Remoteobjekt Proxy funktioniert etwas anders. Der Satz wird sofort zurückgegeben, und der Rückgabewert ist der Wert, der festgesetzt wird. Dies ist eine Anforderung des JavaScript-Proxy Objekts. Wenn Sie asynchron warten müssen, bis die Eigenschaft auf Complete gesetzt ist, verwenden Sie die setremote-Methode, die eine Verheißung zurückgibt, wie oben beschrieben. Eigenschaft für synchrone Objekteigenschaft festlegen synchron blockiert, bis die Eigenschaft gesetzt ist.

Angenommen, Sie verfügen über ein COM-Objekt mit der folgenden Schnittstelle.

```idl
    [uuid(3a14c9c0-bc3e-453f-a314-4ce4a0ec81d8), object, local]
    interface IRemoteObjectSample : IUnknown
    {
        // Demonstrate basic method call with some parameters and a return value.
        HRESULT MethodWithParametersAndReturnValue([in] BSTR stringParameter, [in] INT integerParameter, [out, retval] BSTR* stringResult);

        // Demonstrate getting and setting a property.
        [propget] HRESULT Property([out, retval] BSTR* stringResult);
        [propput] HRESULT Property([in] BSTR stringValue);

        // Demonstrate native calling back into JavaScript.
        HRESULT CallCallbackAsynchronously([in] IDispatch* callbackParameter);
    };
```

 Wir können eine Instanz dieser Schnittstelle in unserem JavaScript mit hinzufügen `AddRemoteObject` . In diesem Fall nennen wir `sample` Folgendes:

```cpp
            VARIANT remoteObjectAsVariant = {};
            m_remoteObject.query_to<IDispatch>(&remoteObjectAsVariant.pdispVal);
            remoteObjectAsVariant.vt = VT_DISPATCH;

            // We can call AddRemoteObject multiple times in a row without
            // calling RemoveRemoteObject first. This will replace the previous object
            // with the new object. In our case this is the same object and everything
            // is fine.
            CHECK_FAILURE(m_webView->AddRemoteObject(L"sample", &remoteObjectAsVariant));
            remoteObjectAsVariant.pdispVal->Release();
```

 Im HTML-Dokument können wir dieses COM-Objekt dann über `chrome.webview.remoteObjects.sample` Folgendes verwenden:

```js
        document.getElementById("getPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = await chrome.webview.remoteObjects.sample.property;
            document.getElementById("getPropertyAsyncOutput").textContent = propertyValue;
        });

        document.getElementById("getPropertySyncButton").addEventListener("click", () => {
            const propertyValue = chrome.webview.remoteObjects.sync.sample.property;
            document.getElementById("getPropertySyncOutput").textContent = propertyValue;
        });

        document.getElementById("setPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyAsyncInput").value;
            // The following line will work but it will return immediately before the property value has actually been set.
            // If you need to set the property and wait for the property to change value, use the setRemote function.
            chrome.webview.remoteObjects.sample.property = propertyValue;
            document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
            // If you care about waiting until the property has actually changed value use the setRemote function.
            await chrome.webview.remoteObjects.sample.setRemote("property", propertyValue);
            document.getElementById("setPropertyExplicitAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertySyncButton").addEventListener("click", () => {
            const propertyValue = document.getElementById("setPropertySyncInput").value;
            chrome.webview.remoteObjects.sync.sample.property = propertyValue;
            document.getElementById("setPropertySyncOutput").textContent = "Set";
        });

        document.getElementById("invokeMethodAsyncButton").addEventListener("click", async () => {
            const paramValue1 = document.getElementById("invokeMethodAsyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodAsyncParam2").value);
            const resultValue = await chrome.webview.remoteObjects.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodAsyncOutput").textContent = resultValue;
        });

        document.getElementById("invokeMethodSyncButton").addEventListener("click", () => {
            const paramValue1 = document.getElementById("invokeMethodSyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodSyncParam2").value);
            const resultValue = chrome.webview.remoteObjects.sync.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodSyncOutput").textContent = resultValue;
        });

        let callbackCount = 0;
        document.getElementById("invokeCallbackButton").addEventListener("click", async () => {
            chrome.webview.remoteObjects.sample.CallCallbackAsynchronously(() => {
                document.getElementById("invokeCallbackOutput").textContent = "Native object called the callback " + (++callbackCount) + " time(s).";
            });
        });
```

#### RemoveRemoteObject 

Entfernen Sie das vom Namen angegebene Hostobjekt, damit es nicht mehr über JavaScript-Code in der WebView zugänglich ist.

> Public HRESULT [RemoveRemoteObject](#removeremoteobject)(LPCWSTR Name)

Während neue Zugriffsversuche verweigert werden, wenn das Objekt bereits durch JavaScript-Code in der WebView abgerufen wird, hat der JavaScript-Code weiterhin Zugriff auf das Objekt. Das Aufrufen dieser Methode für einen Namen, der bereits entfernt oder nie hinzugefügt wird, schlägt fehl.

#### OpenDevToolsWindow 

Öffnet das devtools-Fenster für das aktuelle Dokument in der WebView.

> Public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()

Wenn das devtools-Fenster bereits geöffnet ist, wird nichts aufgerufen

#### add_AcceleratorKeyPressed 

Fügen Sie einen Ereignishandler für das AcceleratorKeyPressed-Ereignis hinzu.

> Public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([IWebView2AcceleratorKeyPressedEventHandler](IWebView2AcceleratorKeyPressedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

AcceleratorKeyPressed wird ausgelöst, wenn eine Zugriffstasten-oder Tastenkombination gedrückt oder freigegeben wird, während die WebView fokussiert ist. Ein Schlüssel wird in folgenden Fällen als Beschleuniger betrachtet:

1. STRG oder alt wird derzeit gehalten, oder

1. die Taste gedrückt wird einem Zeichen nicht zugeordnet. Einige bestimmte Tasten gelten nie als Beschleuniger, wie etwa die UMSCHALTTASTE. Die Escape-Taste wird immer als Beschleuniger angesehen.

Durch automatisch wiederholte Tastenereignisse, die durch das Drücken der Taste nach unten verursacht werden, wird dieses Ereignis ebenfalls ausgelöst. Sie können diese filtern, indem Sie das Ereignis args ' KeyEventLParam oder PhysicalKeyStatus.

Im Fenstermodus wird dieser Ereignishandler synchron aufgerufen. Bis Sie Handle () für die Ereignis-args aufrufen oder der Ereignishandler zurückgibt, wird der Browserprozess blockiert, und ausgehende prozessübergreifende com-Aufrufe schlagen mit RPC_E_CANTCALLOUT_ININPUTSYNCCALL fehl. Allerdings funktionieren alle WebView2-API-Methoden.

Im Fenstermodus wird der Ereignishandler asynchron aufgerufen. Eine weitere Eingabe erreicht den Browser erst, wenn der Ereignishandler zurückgegeben oder Handle () aufgerufen wird, der Browserprozess selbst jedoch nicht blockiert wird und ausgehende com-Aufrufe normal funktionieren.

Es wird empfohlen, handle (true) so früh wie möglich aufzurufen, wenn Sie wissen, dass Sie die Zugriffstasten Taste behandeln möchten.

```cpp
    // Register a handler for the AcceleratorKeyPressed event.
    CHECK_FAILURE(m_webView->add_AcceleratorKeyPressed(
        Callback<IWebView2AcceleratorKeyPressedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2AcceleratorKeyPressedEventArgs* args)
                -> HRESULT {
                WEBVIEW2_KEY_EVENT_TYPE type;
                CHECK_FAILURE(args->get_KeyEventType(&type));
                // We only care about key down events.
                if (type == WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN ||
                    type == WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN)
                {
                    UINT key;
                    CHECK_FAILURE(args->get_VirtualKey(&key));
                    // Check if the key is one we want to handle.
                    if (std::function<void()> action =
                            m_appWindow->GetAcceleratorKeyFunction(key))
                    {
                        // Keep the browser from handling this key, whether it's autorepeated or
                        // not.
                        CHECK_FAILURE(args->Handle(TRUE));

                        // Filter out autorepeated keys.
                        WEBVIEW2_PHYSICAL_KEY_STATUS status;
                        CHECK_FAILURE(args->get_PhysicalKeyStatus(&status));
                        if (!status.WasKeyDown)
                        {
                            // Perform the action asynchronously to avoid blocking the
                            // browser process's event queue.
                            m_appWindow->RunAsync(action);
                        }
                    }
                }
                return S_OK;
            })
            .Get(),
        &m_acceleratorKeyPressedToken));
```

#### remove_AcceleratorKeyPressed 

Entfernen Sie einen Ereignishandler, der zuvor mit add_AcceleratorKeyPressed hinzugefügt wurde.

> Public HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(EventRegistrationToken-Token)

#### WEBVIEW2_KEY_EVENT_TYPE 

Der Typ des Schlüssel Ereignisses, das ein AcceleratorKeyPressed-Ereignis ausgelöst hat.

> Enum- [WEBVIEW2_KEY_EVENT_TYPE](#webview2_key_event_type)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN            | Dem Fenster Nachrichten WM_KEYDOWN entsprechen.
WEBVIEW2_KEY_EVENT_TYPE_KEY_UP            | Dem Fenster Nachrichten WM_KEYUP entsprechen.
WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN            | Dem Fenster Nachrichten WM_SYSKEYDOWN entsprechen.
WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP            | Dem Fenster Nachrichten WM_SYSKEYUP entsprechen.

#### WEBVIEW2_PHYSICAL_KEY_STATUS 

Eine Struktur, die die Informationen darstellt, die in lParam verpackt sind, die einem Win32-Schlüsselereignis zugewiesen wurden.

> typedef [WEBVIEW2_PHYSICAL_KEY_STATUS](#webview2_physical_key_status)

Weitere Informationen finden Sie in der Dokumentation zu WM_KEYDOWN.[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)

