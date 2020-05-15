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
# <span data-ttu-id="1e6dc-104">Schnittstellen IWebView2WebView4</span><span class="sxs-lookup"><span data-stu-id="1e6dc-104">interface IWebView2WebView4</span></span> 

> [!NOTE]
> <span data-ttu-id="1e6dc-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="1e6dc-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="1e6dc-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView4
  : public IWebView2WebView3
```

<span data-ttu-id="1e6dc-107">Zusätzliche Funktionen, die vom primären WebView-Objekt implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="1e6dc-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="1e6dc-108">Summary</span></span>

 <span data-ttu-id="1e6dc-109">Member</span><span class="sxs-lookup"><span data-stu-id="1e6dc-109">Members</span></span>                        | <span data-ttu-id="1e6dc-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="1e6dc-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1e6dc-111">Addremoteobject</span><span class="sxs-lookup"><span data-stu-id="1e6dc-111">AddRemoteObject</span></span>](#addremoteobject) | <span data-ttu-id="1e6dc-112">Fügen Sie das bereitgestellte Hostobjekt zu Skript hinzu, das in der WebView mit dem angegebenen Namen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-112">Add the provided host object to script running in the WebView with the specified name.</span></span>
[<span data-ttu-id="1e6dc-113">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="1e6dc-113">RemoveRemoteObject</span></span>](#removeremoteobject) | <span data-ttu-id="1e6dc-114">Entfernen Sie das vom Namen angegebene Hostobjekt, damit es nicht mehr über JavaScript-Code in der WebView zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-114">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>
[<span data-ttu-id="1e6dc-115">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="1e6dc-115">OpenDevToolsWindow</span></span>](#opendevtoolswindow) | <span data-ttu-id="1e6dc-116">Öffnet das devtools-Fenster für das aktuelle Dokument in der WebView.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-116">Opens the DevTools window for the current document in the WebView.</span></span>
[<span data-ttu-id="1e6dc-117">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="1e6dc-117">add_AcceleratorKeyPressed</span></span>](#add_acceleratorkeypressed) | <span data-ttu-id="1e6dc-118">Fügen Sie einen Ereignishandler für das AcceleratorKeyPressed-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-118">Add an event handler for the AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="1e6dc-119">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="1e6dc-119">remove_AcceleratorKeyPressed</span></span>](#remove_acceleratorkeypressed) | <span data-ttu-id="1e6dc-120">Entfernen Sie einen Ereignishandler, der zuvor mit add_AcceleratorKeyPressed hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-120">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>
[<span data-ttu-id="1e6dc-121">WEBVIEW2_KEY_EVENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="1e6dc-121">WEBVIEW2_KEY_EVENT_TYPE</span></span>](#webview2_key_event_type) | <span data-ttu-id="1e6dc-122">Der Typ des Schlüssel Ereignisses, das ein AcceleratorKeyPressed-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-122">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="1e6dc-123">WEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="1e6dc-123">WEBVIEW2_PHYSICAL_KEY_STATUS</span></span>](#webview2_physical_key_status) | <span data-ttu-id="1e6dc-124">Eine Struktur, die die Informationen darstellt, die in lParam verpackt sind, die einem Win32-Schlüsselereignis zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-124">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

<span data-ttu-id="1e6dc-125">Sie können QueryInterface für diese Schnittstelle aus dem Objekt, das [IWebView2WebView](IWebView2WebView.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-125">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="1e6dc-126">Weitere Informationen finden Sie auf der [IWebView2WebView](IWebView2WebView.md) -Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-126">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="1e6dc-127">Member</span><span class="sxs-lookup"><span data-stu-id="1e6dc-127">Members</span></span>

#### <span data-ttu-id="1e6dc-128">Addremoteobject</span><span class="sxs-lookup"><span data-stu-id="1e6dc-128">AddRemoteObject</span></span> 

<span data-ttu-id="1e6dc-129">Fügen Sie das bereitgestellte Hostobjekt zu Skript hinzu, das in der WebView mit dem angegebenen Namen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-129">Add the provided host object to script running in the WebView with the specified name.</span></span>

> <span data-ttu-id="1e6dc-130">Public HRESULT [addremoteobject](#addremoteobject)(LPCWSTR-Name, Variant \*-Objekt)</span><span class="sxs-lookup"><span data-stu-id="1e6dc-130">public HRESULT [AddRemoteObject](#addremoteobject)(LPCWSTR name,VARIANT \* object)</span></span>

<span data-ttu-id="1e6dc-131">Host Objekte werden als Remoteobjekt Proxys über bereitgestellt `window.chrome.webview.remoteObjects.<name>` .</span><span class="sxs-lookup"><span data-stu-id="1e6dc-131">Host objects are exposed as remote object proxies via `window.chrome.webview.remoteObjects.<name>`.</span></span> <span data-ttu-id="1e6dc-132">Remote Objektproxys sind Versprechungen und werden in ein Objekt aufgelöst, das das Hostobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-132">Remote object proxies are promises and will resolve to an object representing the host object.</span></span> <span data-ttu-id="1e6dc-133">Das Versprechen wird abgelehnt, wenn die APP kein Objekt mit dem Namen hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-133">The promise is rejected if the app has not added an object with the name.</span></span> <span data-ttu-id="1e6dc-134">Wenn JavaScript-Code auf eine Eigenschaft oder Methode des Objekts zugreift, wird eine Zusage zurückgegeben, die in den Wert aufgelöst wird, der vom Host für die Eigenschaft oder Methode zurückgegeben wird, oder im Fall eines Fehlers abgelehnt wird, beispielsweise wenn keine solche Eigenschaft oder Methode für das Objekt vorhanden ist oder Parameter ungültig sind.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-134">When JavaScript code access a property or method of the object, a promise is return, which will resolve to the value returned from the host for the property or method, or rejected in case of error such as there is no such property or method on the object or parameters are invalid.</span></span> <span data-ttu-id="1e6dc-135">Wenn der Anwendungscode beispielsweise Folgendes durchführt:</span><span class="sxs-lookup"><span data-stu-id="1e6dc-135">For example, when the application code does the following:</span></span> 

```cpp
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddRemoteObject(L"host_object", &host);
```

 <span data-ttu-id="1e6dc-136">JavaScript-Code in der WebView kann auf appObject wie folgt zugreifen und dann auf Attribute und Methoden von appObject zugreifen:</span><span class="sxs-lookup"><span data-stu-id="1e6dc-136">JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject:</span></span> 

```js
let app_object = await window.chrome.webview.remoteObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

 <span data-ttu-id="1e6dc-137">Beachten Sie, dass einfache Typen, IDispatch und Array unterstützt werden, generische IUnknown, VT_DECIMAL oder VT_RECORD Variant nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-137">Note that while simple types, IDispatch and array are supported, generic IUnknown, VT_DECIMAL, or VT_RECORD variant is not supported.</span></span> <span data-ttu-id="1e6dc-138">Remote-JavaScript-Objekte wie Rückruffunktionen werden als VT_DISPATCH Variante mit dem Object-Implementierungs-IDispatch dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-138">Remote JavaScript objects like callback functions are represented as an VT_DISPATCH VARIANT with the object implementing IDispatch.</span></span> <span data-ttu-id="1e6dc-139">Die JavaScript-Rückrufmethode kann mit DISPID_VALUE für die DISPID aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-139">The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID.</span></span> <span data-ttu-id="1e6dc-140">Geschachtelte Arrays werden bis zu einer Tiefe von 3 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-140">Nested arrays are supported up to a depth of 3.</span></span> <span data-ttu-id="1e6dc-141">Arrays von nach Verweistypen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-141">Arrays of by reference types are not supported.</span></span> <span data-ttu-id="1e6dc-142">VT_EMPTY und VT_NULL werden JavaScript als NULL zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-142">VT_EMPTY and VT_NULL are mapped into JavaScript as null.</span></span> <span data-ttu-id="1e6dc-143">In JavaScript werden NULL und undefined VT_EMPTY zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-143">In JavaScript null and undefined are mapped to VT_EMPTY.</span></span>

<span data-ttu-id="1e6dc-144">Darüber hinaus werden alle Remoteobjekte als verfügbar gemacht `window.chrome.webview.remoteObjects.sync.<name>` .</span><span class="sxs-lookup"><span data-stu-id="1e6dc-144">Additionally, all remote objects are exposed as `window.chrome.webview.remoteObjects.sync.<name>`.</span></span> <span data-ttu-id="1e6dc-145">Hier werden die Hostobjekte als synchrone Remoteobjekt Proxys verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-145">Here the host objects are exposed as synchronous remote object proxies.</span></span> <span data-ttu-id="1e6dc-146">Hierbei handelt es sich nicht um Versprechungen und Aufrufe von Funktionen oder des Eigenschafts Zugriffs, die ein synchrones Blockieren des ausgeführten Skripts warten, um die Ausführung des Host Codes zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-146">These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run.</span></span> <span data-ttu-id="1e6dc-147">Dementsprechend kann dies zu Zuverlässigkeitsproblemen führen, und es wird empfohlen, dass Sie die oben beschriebene Versprechen-basierte asynchrone `window.chrome.webview.remoteObjects.<name>` API verwenden.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-147">Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.remoteObjects.<name>` API described above.</span></span>

<span data-ttu-id="1e6dc-148">Synchrone Remoteobjekt Proxys und asynchrone Remoteobjekt Proxys können sowohl Proxys für dasselbe Remoteobjekt als auch Proxys sein.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-148">Synchronous remote object proxies and asynchronous remote object proxies can both proxy the same remote object.</span></span> <span data-ttu-id="1e6dc-149">Remote Änderungen, die von einem Proxy durchgeführt werden, werden in jedem anderen Proxy desselben Remoteobjekts widergespiegelt, unabhängig davon, ob die anderen Proxys synchron oder asynchron sind.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-149">Remote changes made by one proxy will be reflected in any other proxy of that same remote object whether the other proxies and synchronous or asynchronous.</span></span>

<span data-ttu-id="1e6dc-150">Während JavaScript bei einem synchronen Aufruf von systemeigenem Code blockiert wird, kann dieser systemeigene Code nicht mehr in JavaScript zurückrufen.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-150">While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript.</span></span> <span data-ttu-id="1e6dc-151">Der Versuch, dies zu tun, schlägt mit HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK) fehl.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-151">Attempts to do so will fail with HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK).</span></span>

<span data-ttu-id="1e6dc-152">Remote Objektproxys sind JavaScript-Proxy Objekte, die alle Eigenschaften abrufen, Eigenschaftensätze und Methodenaufrufe abfangen.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-152">Remote object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations.</span></span> <span data-ttu-id="1e6dc-153">Eigenschaften oder Methoden, die Teil des Funktions-oder Objekt Prototyps sind, werden lokal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-153">Properties or methods that are a part of the Function or Object prototype are run locally.</span></span> <span data-ttu-id="1e6dc-154">Darüber hinaus werden alle Eigenschaften oder Methoden im Array `chrome.webview.remoteObjects.options.forceLocalProperties` lokal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-154">Additionally any property or method in the array `chrome.webview.remoteObjects.options.forceLocalProperties` will also be run locally.</span></span> <span data-ttu-id="1e6dc-155">Diese Option enthält standardmäßig optionale Methoden, die in JavaScript wie und in Bedeutung sind `toJSON` `Symbol.toPrimitive` .</span><span class="sxs-lookup"><span data-stu-id="1e6dc-155">This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`.</span></span> <span data-ttu-id="1e6dc-156">Sie können diesem Array nach Bedarf weitere hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-156">You can add more to this array as required.</span></span>

<span data-ttu-id="1e6dc-157">Es gibt eine Methode `chrome.webview.remoteObjects.cleanupSome` , mit der die Garbage Collection von Remoteobjekt Proxys am besten abläuft.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-157">There's a method `chrome.webview.remoteObjects.cleanupSome` that will best effort garbage collect remote object proxies.</span></span>

<span data-ttu-id="1e6dc-158">Für Remote Objektproxys gibt es zusätzlich die folgenden Methoden, die lokal ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="1e6dc-158">Remote object proxies additionally have the following methods which run locally:</span></span>

* <span data-ttu-id="1e6dc-159">applyRemote, getRemote, setremote: Durchführen eines Methodenaufrufs, eines Eigenschaften Abstands oder eines Eigenschaftssatzes für das Remoteobjekt.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-159">applyRemote, getRemote, setRemote: Perform a method invocation, property get, or property set on the remote object.</span></span> <span data-ttu-id="1e6dc-160">Mit diesen können Sie explizit erzwingen, dass eine Methode oder Eigenschaft Remote ausgeführt wird, wenn eine in Konflikt stehende lokale Methode oder Eigenschaft vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-160">You can use these to explicitly force a method or property to run remotely if there is a conflicting local method or property.</span></span> <span data-ttu-id="1e6dc-161">Beispielsweise führt `proxy.toString()` die lokale ToString-Methode für das Proxyobjekt aus.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-161">For instance, `proxy.toString()` will run the local toString method on the proxy object.</span></span> <span data-ttu-id="1e6dc-162">`proxy.applyRemote('toString')`Wird aber `toString` stattdessen auf dem Remoteproxy Objekt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-162">But `proxy.applyRemote('toString')` runs `toString` on the remote proxied object instead.</span></span>

* <span data-ttu-id="1e6dc-163">getLocal, setlocal: führt Eigenschaften abrufen oder Eigenschaftssatz lokal aus.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-163">getLocal, setLocal: Perform property get, or property set locally.</span></span> <span data-ttu-id="1e6dc-164">Sie können diese Methoden verwenden, um das Abrufen oder Festlegen einer Eigenschaft für den Remoteobjekt Proxy selbst und nicht für das Remoteobjekt zu erzwingen, das es darstellt.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-164">You can use these methods to force getting or setting a property on the remote object proxy itself rather than on the remote object it represents.</span></span> <span data-ttu-id="1e6dc-165">Beispielsweise `proxy.unknownProperty` wird die Eigenschaft abgerufen, die `unknownProperty` aus dem Remoteproxy Objekt benannt wurde.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-165">For instance, `proxy.unknownProperty` will get the property named `unknownProperty` from the remote proxied object.</span></span> <span data-ttu-id="1e6dc-166">`proxy.getLocal('unknownProperty')`Der Wert der Eigenschaft wird jedoch `unknownProperty` für das Proxyobjekt selbst abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-166">But `proxy.getLocal('unknownProperty')` will get the value of the property `unknownProperty` on the proxy object itself.</span></span>

* <span data-ttu-id="1e6dc-167">Synchronisierung: asynchrone Remoteobjekt Proxys machen eine Synchronisierungsmethode verfügbar, die ein Versprechen für einen synchronen Remoteobjekt Proxy für das gleiche Remoteobjekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-167">sync: Asynchronous remote object proxies expose a sync method which returns a promise for a synchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="1e6dc-168">Gibt beispielsweise `chrome.webview.remoteObjects.sample.methodCall()` einen asynchronen Remoteobjekt Proxy zurück.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-168">For example, `chrome.webview.remoteObjects.sample.methodCall()` returns an asynchronous remote object proxy.</span></span> <span data-ttu-id="1e6dc-169">Sie können stattdessen die `sync` Methode zum Abrufen eines synchronen Remoteobjekt Proxys verwenden:</span><span class="sxs-lookup"><span data-stu-id="1e6dc-169">You can use the `sync` method to obtain a synchronous remote object proxy instead:</span></span> `const syncProxy = await chrome.webview.remoteObjects.sample.methodCall().sync()`

* <span data-ttu-id="1e6dc-170">Async: synchrone Remoteobjekt Proxys machen eine asynchrone Methode verfügbar, die einen asynchronen Remoteobjekt Proxy für das gleiche Remoteobjekt blockiert und zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-170">async: Synchronous remote object proxies expose an async method which blocks and returns an asynchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="1e6dc-171">Gibt beispielsweise `chrome.webview.remoteObjects.sync.sample.methodCall()` einen synchronen Remoteobjekt Proxy zurück.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-171">For example, `chrome.webview.remoteObjects.sync.sample.methodCall()` returns a synchronous remote object proxy.</span></span> <span data-ttu-id="1e6dc-172">Aufruf der `async` Methode für diesen Block und anschließendes zurückgeben eines asynchronen Remoteobjekt Proxys für dasselbe Remoteobjekt:</span><span class="sxs-lookup"><span data-stu-id="1e6dc-172">Calling the `async` method on this blocks and then returns an asynchronous remote object proxy for the same remote object:</span></span> `const asyncProxy = chrome.webview.remoteObjects.sync.sample.methodCall().async()`

* <span data-ttu-id="1e6dc-173">dann: asynchrone Remoteobjekt Proxys verfügen über eine then-Methode.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-173">then: Asynchronous remote object proxies have a then method.</span></span> <span data-ttu-id="1e6dc-174">Auf diese Weise können Sie warten.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-174">This allows them to be awaitable.</span></span> `then` <span data-ttu-id="1e6dc-175">gibt eine Verheißung zurück, die mit einer Darstellung des Remoteobjekts aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-175">will return a promise that resolves with a representation of the remote object.</span></span> <span data-ttu-id="1e6dc-176">Wenn der Proxy ein JavaScript-Literal darstellt, wird eine Kopie davon lokal zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-176">If the proxy represents a JavaScript literal then a copy of that is returned locally.</span></span> <span data-ttu-id="1e6dc-177">Wenn der Proxy eine Funktion darstellt, wird ein nicht erwarteter Proxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-177">If the proxy represents a function then a non-awaitable proxy is returned.</span></span> <span data-ttu-id="1e6dc-178">Wenn der Proxy ein JavaScript-Objekt mit einer Kombination aus Literalen Eigenschaften und Funktionseigenschaften darstellt, wird eine Kopie des Objekts mit einigen Eigenschaften als Remoteobjekt Proxys zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-178">If the proxy represents a JavaScript object with a mix of literal properties and function properties, then the a copy of the object is returned with some properties as remote object proxies.</span></span>

<span data-ttu-id="1e6dc-179">Alle anderen Eigenschaften-und Methodenaufrufe (außer den oben genannten Methoden für Remote Objektproxy, forceLocalProperties-Liste und Eigenschaften für Funktions-und Objekt Prototypen) werden Remote ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-179">All other property and method invocations (other than the above Remote object proxy methods, forceLocalProperties list, and properties on Function and Object prototypes) are run remotely.</span></span> <span data-ttu-id="1e6dc-180">Asynchrone Remoteobjekt Proxys geben eine Versprechung zurück, die den asynchronen Abschluss des Remoteaufrufs der Methode oder das Abrufen der Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-180">Asynchronous remote object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property.</span></span> <span data-ttu-id="1e6dc-181">Das Versprechen wird aufgelöst, nachdem die Remotevorgänge abgeschlossen sind und die Zusagen in den resultierenden Wert des Vorgangs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-181">The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation.</span></span> <span data-ttu-id="1e6dc-182">Synchrone Remoteobjekt Proxys funktionieren ähnlich, blockieren aber die JavaScript-Ausführung und warten, bis der Remotevorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-182">Synchronous remote object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.</span></span>

<span data-ttu-id="1e6dc-183">Das Festlegen einer Eigenschaft für einen asynchronen Remoteobjekt Proxy funktioniert etwas anders.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-183">Setting a property on an asynchronous remote object proxy works slightly differently.</span></span> <span data-ttu-id="1e6dc-184">Der Satz wird sofort zurückgegeben, und der Rückgabewert ist der Wert, der festgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-184">The set returns immediately and the return value is the value that will be set.</span></span> <span data-ttu-id="1e6dc-185">Dies ist eine Anforderung des JavaScript-Proxy Objekts.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-185">This is a requirement of the JavaScript Proxy object.</span></span> <span data-ttu-id="1e6dc-186">Wenn Sie asynchron warten müssen, bis die Eigenschaft auf Complete gesetzt ist, verwenden Sie die setremote-Methode, die eine Verheißung zurückgibt, wie oben beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-186">If you need to asynchronously wait for the property set to complete, use the setRemote method which returns a promise as described above.</span></span> <span data-ttu-id="1e6dc-187">Eigenschaft für synchrone Objekteigenschaft festlegen synchron blockiert, bis die Eigenschaft gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-187">Synchronous object property set property synchronously blocks until the property is set.</span></span>

<span data-ttu-id="1e6dc-188">Angenommen, Sie verfügen über ein COM-Objekt mit der folgenden Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-188">For example, suppose you have a COM object with the following interface</span></span>

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

 <span data-ttu-id="1e6dc-189">Wir können eine Instanz dieser Schnittstelle in unserem JavaScript mit hinzufügen `AddRemoteObject` .</span><span class="sxs-lookup"><span data-stu-id="1e6dc-189">We can add an instance of this interface into our JavaScript with `AddRemoteObject`.</span></span> <span data-ttu-id="1e6dc-190">In diesem Fall nennen wir `sample` Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1e6dc-190">In this case we name it `sample`:</span></span>

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

 <span data-ttu-id="1e6dc-191">Im HTML-Dokument können wir dieses COM-Objekt dann über `chrome.webview.remoteObjects.sample` Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="1e6dc-191">Then in the HTML document we can use this COM object via `chrome.webview.remoteObjects.sample`:</span></span>

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

#### <span data-ttu-id="1e6dc-192">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="1e6dc-192">RemoveRemoteObject</span></span> 

<span data-ttu-id="1e6dc-193">Entfernen Sie das vom Namen angegebene Hostobjekt, damit es nicht mehr über JavaScript-Code in der WebView zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-193">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>

> <span data-ttu-id="1e6dc-194">Public HRESULT [RemoveRemoteObject](#removeremoteobject)(LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="1e6dc-194">public HRESULT [RemoveRemoteObject](#removeremoteobject)(LPCWSTR name)</span></span>

<span data-ttu-id="1e6dc-195">Während neue Zugriffsversuche verweigert werden, wenn das Objekt bereits durch JavaScript-Code in der WebView abgerufen wird, hat der JavaScript-Code weiterhin Zugriff auf das Objekt.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-195">While new access attempts will be denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code will continue to have access to that object.</span></span> <span data-ttu-id="1e6dc-196">Das Aufrufen dieser Methode für einen Namen, der bereits entfernt oder nie hinzugefügt wird, schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-196">Calling this method for a name that is already removed or never added will fail.</span></span>

#### <span data-ttu-id="1e6dc-197">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="1e6dc-197">OpenDevToolsWindow</span></span> 

<span data-ttu-id="1e6dc-198">Öffnet das devtools-Fenster für das aktuelle Dokument in der WebView.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-198">Opens the DevTools window for the current document in the WebView.</span></span>

> <span data-ttu-id="1e6dc-199">Public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span><span class="sxs-lookup"><span data-stu-id="1e6dc-199">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span></span>

<span data-ttu-id="1e6dc-200">Wenn das devtools-Fenster bereits geöffnet ist, wird nichts aufgerufen</span><span class="sxs-lookup"><span data-stu-id="1e6dc-200">Does nothing if called when the DevTools window is already open</span></span>

#### <span data-ttu-id="1e6dc-201">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="1e6dc-201">add_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="1e6dc-202">Fügen Sie einen Ereignishandler für das AcceleratorKeyPressed-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-202">Add an event handler for the AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="1e6dc-203">Public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([IWebView2AcceleratorKeyPressedEventHandler](IWebView2AcceleratorKeyPressedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="1e6dc-203">public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([IWebView2AcceleratorKeyPressedEventHandler](IWebView2AcceleratorKeyPressedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="1e6dc-204">AcceleratorKeyPressed wird ausgelöst, wenn eine Zugriffstasten-oder Tastenkombination gedrückt oder freigegeben wird, während die WebView fokussiert ist.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-204">AcceleratorKeyPressed fires when an accelerator key or key combo is pressed or released while the WebView is focused.</span></span> <span data-ttu-id="1e6dc-205">Ein Schlüssel wird in folgenden Fällen als Beschleuniger betrachtet:</span><span class="sxs-lookup"><span data-stu-id="1e6dc-205">A key is considered an accelerator if either:</span></span>

1. <span data-ttu-id="1e6dc-206">STRG oder alt wird derzeit gehalten, oder</span><span class="sxs-lookup"><span data-stu-id="1e6dc-206">Ctrl or Alt is currently being held, or</span></span>

1. <span data-ttu-id="1e6dc-207">die Taste gedrückt wird einem Zeichen nicht zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-207">the pressed key does not map to a character.</span></span> <span data-ttu-id="1e6dc-208">Einige bestimmte Tasten gelten nie als Beschleuniger, wie etwa die UMSCHALTTASTE.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-208">A few specific keys are never considered accelerators, such as Shift.</span></span> <span data-ttu-id="1e6dc-209">Die Escape-Taste wird immer als Beschleuniger angesehen.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-209">The Escape key is always considered an accelerator.</span></span>

<span data-ttu-id="1e6dc-210">Durch automatisch wiederholte Tastenereignisse, die durch das Drücken der Taste nach unten verursacht werden, wird dieses Ereignis ebenfalls ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-210">Autorepeated key events caused by holding the key down will also fire this event.</span></span> <span data-ttu-id="1e6dc-211">Sie können diese filtern, indem Sie das Ereignis args ' KeyEventLParam oder PhysicalKeyStatus.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-211">You can filter these out by checking the event args' KeyEventLParam or PhysicalKeyStatus.</span></span>

<span data-ttu-id="1e6dc-212">Im Fenstermodus wird dieser Ereignishandler synchron aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-212">In windowed mode, this event handler is called synchronously.</span></span> <span data-ttu-id="1e6dc-213">Bis Sie Handle () für die Ereignis-args aufrufen oder der Ereignishandler zurückgibt, wird der Browserprozess blockiert, und ausgehende prozessübergreifende com-Aufrufe schlagen mit RPC_E_CANTCALLOUT_ININPUTSYNCCALL fehl.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-213">Until you call Handle() on the event args or the event handler returns, the browser process will be blocked and outgoing cross-process COM calls will fail with RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span></span> <span data-ttu-id="1e6dc-214">Allerdings funktionieren alle WebView2-API-Methoden.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-214">All WebView2 API methods will work, however.</span></span>

<span data-ttu-id="1e6dc-215">Im Fenstermodus wird der Ereignishandler asynchron aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-215">In windowless mode, the event handler is called asynchronously.</span></span> <span data-ttu-id="1e6dc-216">Eine weitere Eingabe erreicht den Browser erst, wenn der Ereignishandler zurückgegeben oder Handle () aufgerufen wird, der Browserprozess selbst jedoch nicht blockiert wird und ausgehende com-Aufrufe normal funktionieren.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-216">Further input will not reach the browser until the event handler returns or Handle() is called, but the browser process itself will not be blocked, and outgoing COM calls will work normally.</span></span>

<span data-ttu-id="1e6dc-217">Es wird empfohlen, handle (true) so früh wie möglich aufzurufen, wenn Sie wissen, dass Sie die Zugriffstasten Taste behandeln möchten.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-217">It is recommended to call Handle(TRUE) as early as you can know that you want to handle the accelerator key.</span></span>

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

#### <span data-ttu-id="1e6dc-218">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="1e6dc-218">remove_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="1e6dc-219">Entfernen Sie einen Ereignishandler, der zuvor mit add_AcceleratorKeyPressed hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-219">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>

> <span data-ttu-id="1e6dc-220">Public HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="1e6dc-220">public HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="1e6dc-221">WEBVIEW2_KEY_EVENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="1e6dc-221">WEBVIEW2_KEY_EVENT_TYPE</span></span> 

<span data-ttu-id="1e6dc-222">Der Typ des Schlüssel Ereignisses, das ein AcceleratorKeyPressed-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-222">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="1e6dc-223">Enum- [WEBVIEW2_KEY_EVENT_TYPE](#webview2_key_event_type)</span><span class="sxs-lookup"><span data-stu-id="1e6dc-223">enum [WEBVIEW2_KEY_EVENT_TYPE](#webview2_key_event_type)</span></span>

 <span data-ttu-id="1e6dc-224">Werte</span><span class="sxs-lookup"><span data-stu-id="1e6dc-224">Values</span></span>                         | <span data-ttu-id="1e6dc-225">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="1e6dc-225">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="1e6dc-226">WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="1e6dc-226">WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN</span></span>            | <span data-ttu-id="1e6dc-227">Dem Fenster Nachrichten WM_KEYDOWN entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-227">Correspond to window message WM_KEYDOWN.</span></span>
<span data-ttu-id="1e6dc-228">WEBVIEW2_KEY_EVENT_TYPE_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="1e6dc-228">WEBVIEW2_KEY_EVENT_TYPE_KEY_UP</span></span>            | <span data-ttu-id="1e6dc-229">Dem Fenster Nachrichten WM_KEYUP entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-229">Correspond to window message WM_KEYUP.</span></span>
<span data-ttu-id="1e6dc-230">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="1e6dc-230">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN</span></span>            | <span data-ttu-id="1e6dc-231">Dem Fenster Nachrichten WM_SYSKEYDOWN entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-231">Correspond to window message WM_SYSKEYDOWN.</span></span>
<span data-ttu-id="1e6dc-232">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="1e6dc-232">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP</span></span>            | <span data-ttu-id="1e6dc-233">Dem Fenster Nachrichten WM_SYSKEYUP entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-233">Correspond to window message WM_SYSKEYUP.</span></span>

#### <span data-ttu-id="1e6dc-234">WEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="1e6dc-234">WEBVIEW2_PHYSICAL_KEY_STATUS</span></span> 

<span data-ttu-id="1e6dc-235">Eine Struktur, die die Informationen darstellt, die in lParam verpackt sind, die einem Win32-Schlüsselereignis zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-235">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

> <span data-ttu-id="1e6dc-236">typedef [WEBVIEW2_PHYSICAL_KEY_STATUS](#webview2_physical_key_status)</span><span class="sxs-lookup"><span data-stu-id="1e6dc-236">typedef [WEBVIEW2_PHYSICAL_KEY_STATUS](#webview2_physical_key_status)</span></span>

<span data-ttu-id="1e6dc-237">Weitere Informationen finden Sie in der Dokumentation zu WM_KEYDOWN.[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span><span class="sxs-lookup"><span data-stu-id="1e6dc-237">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span></span>

