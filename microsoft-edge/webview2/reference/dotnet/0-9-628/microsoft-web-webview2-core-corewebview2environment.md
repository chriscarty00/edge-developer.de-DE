---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2Environment
ms.openlocfilehash: c6b1f1c62da5aa5ef64693575abb9cb46ac13851
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012092"
---
# <span data-ttu-id="2de65-104">Microsoft. Web. WebView2. Core. CoreWebView2Environment Klasse</span><span class="sxs-lookup"><span data-stu-id="2de65-104">Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

<span data-ttu-id="2de65-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="2de65-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="2de65-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="2de65-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="2de65-107">Dies stellt die WebView2-Umgebung dar.</span><span class="sxs-lookup"><span data-stu-id="2de65-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="2de65-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2de65-108">Summary</span></span>

 <span data-ttu-id="2de65-109">Member</span><span class="sxs-lookup"><span data-stu-id="2de65-109">Members</span></span>                        | <span data-ttu-id="2de65-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="2de65-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2de65-111">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="2de65-111">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="2de65-112">Die Browser Versionsinformationen des aktuellen CoreWebView2Environment, einschließlich des Kanal namens, wenn es sich nicht um den stabilen Kanal handelt.</span><span class="sxs-lookup"><span data-stu-id="2de65-112">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="2de65-113">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="2de65-113">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="2de65-114">NewBrowserVersionAvailable wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="2de65-114">NewBrowserVersionAvailable fires when a newer version of the Edge browser is installed and available for use via WebView2.</span></span>
[<span data-ttu-id="2de65-115">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="2de65-115">CreateCoreWebView2CompositionControllerAsync</span></span>](#createcorewebview2compositioncontrollerasync) | <span data-ttu-id="2de65-116">Erstellen Sie ein neues WebView-Element für die Verwendung mit Visual Hosting asynchron.</span><span class="sxs-lookup"><span data-stu-id="2de65-116">Asynchronously create a new WebView for use with visual hosting.</span></span>
[<span data-ttu-id="2de65-117">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="2de65-117">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="2de65-118">Erstellen Sie einen neuen WebView asynchron.</span><span class="sxs-lookup"><span data-stu-id="2de65-118">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="2de65-119">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="2de65-119">CreateCoreWebView2PointerInfo</span></span>](#createcorewebview2pointerinfo) | <span data-ttu-id="2de65-120">Erstellen Sie ein leeres CoreWebView2PointerInfo.</span><span class="sxs-lookup"><span data-stu-id="2de65-120">Create an empty CoreWebView2PointerInfo.</span></span>
[<span data-ttu-id="2de65-121">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="2de65-121">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="2de65-122">Erstellen Sie ein neues Webressourcen-Antwortobjekt.</span><span class="sxs-lookup"><span data-stu-id="2de65-122">Create a new web resource response object.</span></span>
[<span data-ttu-id="2de65-123">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="2de65-123">GetProviderForHwnd</span></span>](#getproviderforhwnd) | <span data-ttu-id="2de65-124">Gibt den Benutzeroberflächenautomatisierungs-Anbieter für die CoreWebView2CompositionController zurück, die dem angegebenen HWND entspricht.</span><span class="sxs-lookup"><span data-stu-id="2de65-124">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

<span data-ttu-id="2de65-125">Webansichten, die aus einer Umgebung erstellt wurden, die im Browser Prozess ausgeführt wird, der mit Umgebungsparametern und aus einer Umgebung erstellten Objekten erstellt wurde, sollten in derselben Umgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2de65-125">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="2de65-126">Die Verwendung in unterschiedlichen Umgebungen ist nicht garantiert kompatibel und kann fehlerhaft sein.</span><span class="sxs-lookup"><span data-stu-id="2de65-126">Using it in different environments are not guaranteed to be compatible and may fail.</span></span> 

<span data-ttu-id="2de65-127">Webansichten, die aus einer Umgebung erstellt wurden, die im Browserprozess ausgeführt wird, der mit Umgebungsparametern und aus einer Umgebung erstellten Objekten erstellt wurde, sollten in derselben Umgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2de65-127">WebViews created from an environment run on the browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="2de65-128">Die Verwendung in unterschiedlichen Umgebungen ist nicht garantiert kompatibel und kann fehlerhaft sein.</span><span class="sxs-lookup"><span data-stu-id="2de65-128">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="2de65-129">Member</span><span class="sxs-lookup"><span data-stu-id="2de65-129">Members</span></span>

#### <span data-ttu-id="2de65-130">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="2de65-130">BrowserVersionString</span></span> 

<span data-ttu-id="2de65-131">Die Browser Versionsinformationen des aktuellen CoreWebView2Environment, einschließlich des Kanal namens, wenn es sich nicht um den stabilen Kanal handelt.</span><span class="sxs-lookup"><span data-stu-id="2de65-131">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="2de65-132">public String [BrowserVersionString](#browserversionstring)</span><span class="sxs-lookup"><span data-stu-id="2de65-132">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="2de65-133">Dies entspricht dem Format der GetAvailableCoreWebView2BrowserVersionString-API.</span><span class="sxs-lookup"><span data-stu-id="2de65-133">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="2de65-134">Kanalnamen sind "Beta", "dev" und "Canary".</span><span class="sxs-lookup"><span data-stu-id="2de65-134">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="2de65-135">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="2de65-135">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="2de65-136">NewBrowserVersionAvailable wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="2de65-136">NewBrowserVersionAvailable fires when a newer version of the Edge browser is installed and available for use via WebView2.</span></span>

> <span data-ttu-id="2de65-137">public event EventHandler<-Objekt > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="2de65-137">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="2de65-138">Wenn Sie die neuere Version des Browsers verwenden möchten, müssen Sie eine neue Umgebung und WebView erstellen.</span><span class="sxs-lookup"><span data-stu-id="2de65-138">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="2de65-139">Dieses Ereignis wird nur für eine neue Version aus dem gleichen Edge-Kanal ausgelöst, von dem aus der Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2de65-139">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="2de65-140">Wenn Sie nicht mit installiertem Edge ausgeführt wird, wird kein Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="2de65-140">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="2de65-141">Da ein benutzerdatenordner nur von einem Browserprozess gleichzeitig verwendet werden kann, wenn Sie denselben benutzerdatenordner in den Webansichten mithilfe der neuen Browserversion verwenden möchten, müssen Sie die Umgebung und Webansichten schließen, die zuerst die ältere Version des Browsers verwenden.</span><span class="sxs-lookup"><span data-stu-id="2de65-141">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="2de65-142">Oder fordern Sie den Benutzer einfach auf, die APP neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="2de65-142">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="2de65-143">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="2de65-143">CreateCoreWebView2CompositionControllerAsync</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="2de65-144">Erstellen Sie ein neues WebView-Element für die Verwendung mit Visual Hosting asynchron.</span><span class="sxs-lookup"><span data-stu-id="2de65-144">Asynchronously create a new WebView for use with visual hosting.</span></span>

> <span data-ttu-id="2de65-145">Public Async Task< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md)  >  [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="2de65-145">public async Task< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md) > [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="2de65-146">ParentWindow ist das HWND, in dem die APP die visuelle Struktur von WebView verbindet.</span><span class="sxs-lookup"><span data-stu-id="2de65-146">parentWindow is the HWND in which the app will connect the visual tree of the WebView.</span></span> <span data-ttu-id="2de65-147">Hierbei handelt es sich um das HWND, in dem die APP Zeiger-und Mauseingaben für die WebView erhält (und SendMouseInput/SendPointerInput für Forward verwenden muss).</span><span class="sxs-lookup"><span data-stu-id="2de65-147">This will be the HWND that the app will receive pointer/ mouse input meant for the WebView (and will need to use SendMouseInput/ SendPointerInput to forward).</span></span> <span data-ttu-id="2de65-148">Wenn die APP die visuelle WebView-Struktur unter einem anderen Fenster verschiebt, muss CoreWebView2CompositionController. ParentWindow so eingestellt werden, dass das neue übergeordnete HWND der visuellen Struktur aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="2de65-148">If the app moves the WebView visual tree to underneath a different window, then it needs to set CoreWebView2CompositionController.ParentWindow to update the new parent HWND of the visual tree.</span></span>

<span data-ttu-id="2de65-149">Legen Sie die RootVisualTarget-Eigenschaft für das erstellte CoreWebView2CompositionController-Objekt so ein, dass es eine visuelle Struktur bereitstellt</span><span class="sxs-lookup"><span data-stu-id="2de65-149">Set RootVisualTarget property on the created CoreWebView2CompositionController to provide a visual to host the browser's visual tree.</span></span>

<span data-ttu-id="2de65-150">Es wird empfohlen, die Anwendungsbenutzer Modell-ID für den Prozess oder das Anwendungsfenster festzulegen.</span><span class="sxs-lookup"><span data-stu-id="2de65-150">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="2de65-151">Wenn None gesetzt ist, wird bei der Erstellung von WebView eine generierte Anwendungsbenutzer Modell-ID auf das Stammfenster von ParentWindow eingestellt.</span><span class="sxs-lookup"><span data-stu-id="2de65-151">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="2de65-152">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="2de65-152">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="2de65-153">Erstellen Sie einen neuen WebView asynchron.</span><span class="sxs-lookup"><span data-stu-id="2de65-153">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="2de65-154">Public Async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="2de65-154">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="2de65-155">ParentWindow ist das HWND, in dem die WebView-Ansicht angezeigt werden soll und von der die Eingabe empfangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2de65-155">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="2de65-156">Die WebView fügt dem bereitgestellten Fenster während der Erstellung von WebView ein untergeordnetes Fenster hinzu.</span><span class="sxs-lookup"><span data-stu-id="2de65-156">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="2de65-157">Die Z-Reihenfolge und andere Elemente, die von der Reihenfolge der nebengeordneten Fenster beeinflusst werden, sind dementsprechend betroffen.</span><span class="sxs-lookup"><span data-stu-id="2de65-157">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="2de65-158">Es wird empfohlen, die Anwendungsbenutzer Modell-ID für den Prozess oder das Anwendungsfenster festzulegen.</span><span class="sxs-lookup"><span data-stu-id="2de65-158">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="2de65-159">Wenn None gesetzt ist, wird bei der Erstellung von WebView eine generierte Anwendungsbenutzer Modell-ID auf das Stammfenster von ParentWindow eingestellt.</span><span class="sxs-lookup"><span data-stu-id="2de65-159">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="2de65-160">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="2de65-160">CreateCoreWebView2PointerInfo</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="2de65-161">Erstellen Sie ein leeres CoreWebView2PointerInfo.</span><span class="sxs-lookup"><span data-stu-id="2de65-161">Create an empty CoreWebView2PointerInfo.</span></span>

> <span data-ttu-id="2de65-162">Public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span><span class="sxs-lookup"><span data-stu-id="2de65-162">public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span></span>

<span data-ttu-id="2de65-163">Der zurückgegebene CoreWebView2PointerInfo muss mit allen relevanten Informationen gefüllt werden, bevor SendPointerInput aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2de65-163">The returned CoreWebView2PointerInfo needs to be populated with all of the relevant info before calling SendPointerInput.</span></span>

#### <span data-ttu-id="2de65-164">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="2de65-164">CreateWebResourceResponse</span></span> 

<span data-ttu-id="2de65-165">Erstellen Sie ein neues Webressourcen-Antwortobjekt.</span><span class="sxs-lookup"><span data-stu-id="2de65-165">Create a new web resource response object.</span></span>

> <span data-ttu-id="2de65-166">Public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int Statuscode, String ReasonPhrase, String Headers)</span><span class="sxs-lookup"><span data-stu-id="2de65-166">public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="2de65-167">Die Kopfzeilen ist die unformatierte Antwortheader Zeichenfolge, die durch einen Zeilenumbruch getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="2de65-167">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="2de65-168">Es ist auch möglich, dieses Objekt mit einer leeren Headerzeichenfolge zu erstellen und dann die Kopfzeilen Zeile für Zeile mithilfe der CoreWebView2HttpResponseHeaders zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2de65-168">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="2de65-169">Informationen zu anderen Parametern finden Sie unter CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="2de65-169">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

#### <span data-ttu-id="2de65-170">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="2de65-170">GetProviderForHwnd</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="2de65-171">Gibt den Benutzeroberflächenautomatisierungs-Anbieter für die CoreWebView2CompositionController zurück, die dem angegebenen HWND entspricht.</span><span class="sxs-lookup"><span data-stu-id="2de65-171">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

> <span data-ttu-id="2de65-172">public Object [GetProviderForHwnd](#getproviderforhwnd)(IntPtr hwnd)</span><span class="sxs-lookup"><span data-stu-id="2de65-172">public object [GetProviderForHwnd](#getproviderforhwnd)(IntPtr hwnd)</span></span>

