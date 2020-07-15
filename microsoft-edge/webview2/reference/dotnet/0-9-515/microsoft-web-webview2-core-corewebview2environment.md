---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: a3e8a958a70820bf32bd3a76acc9ee503f568438
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877756"
---
# <span data-ttu-id="8a9cf-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Environment Klasse</span><span class="sxs-lookup"><span data-stu-id="8a9cf-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

> [!NOTE]
> <span data-ttu-id="8a9cf-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="8a9cf-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="8a9cf-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="8a9cf-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="8a9cf-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="8a9cf-108">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="8a9cf-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="8a9cf-109">Dies stellt die WebView2-Umgebung dar.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-109">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="8a9cf-110">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="8a9cf-110">Summary</span></span>

 <span data-ttu-id="8a9cf-111">Member</span><span class="sxs-lookup"><span data-stu-id="8a9cf-111">Members</span></span>                        | <span data-ttu-id="8a9cf-112">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="8a9cf-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8a9cf-113">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="8a9cf-113">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="8a9cf-114">Die Browser Versionsinformationen des aktuellen CoreWebView2Environment, einschließlich des Kanal namens, wenn es sich nicht um den stabilen Kanal handelt.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-114">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="8a9cf-115">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="8a9cf-115">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="8a9cf-116">Das NewBrowserVersionAvailable-Ereignis wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-116">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="8a9cf-117">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="8a9cf-117">CreateAsync</span></span>](#createasync) | <span data-ttu-id="8a9cf-118">Erstellt eine immergrüne WebView2-Umgebung unter Verwendung der installierten Edge-Version.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-118">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="8a9cf-119">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="8a9cf-119">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="8a9cf-120">Erstellen Sie einen neuen WebView asynchron.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-120">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="8a9cf-121">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="8a9cf-121">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="8a9cf-122">Erstellen Sie ein neues Webressourcen-Antwortobjekt.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-122">Create a new web resource response object.</span></span>

<span data-ttu-id="8a9cf-123">Webansichten, die aus einer Umgebung erstellt wurden, die im Browser Prozess ausgeführt wird, der mit Umgebungsparametern und aus einer Umgebung erstellten Objekten erstellt wurde, sollten in derselben Umgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-123">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="8a9cf-124">Die Verwendung in unterschiedlichen Umgebungen ist nicht garantiert kompatibel und kann fehlerhaft sein.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-124">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="8a9cf-125">Member</span><span class="sxs-lookup"><span data-stu-id="8a9cf-125">Members</span></span>

#### <span data-ttu-id="8a9cf-126">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="8a9cf-126">BrowserVersionString</span></span> 

<span data-ttu-id="8a9cf-127">Die Browser Versionsinformationen des aktuellen CoreWebView2Environment, einschließlich des Kanal namens, wenn es sich nicht um den stabilen Kanal handelt.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-127">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="8a9cf-128">public String [BrowserVersionString](#browserversionstring)</span><span class="sxs-lookup"><span data-stu-id="8a9cf-128">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="8a9cf-129">Dies entspricht dem Format der GetAvailableCoreWebView2BrowserVersionString-API.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-129">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="8a9cf-130">Kanalnamen sind "Beta", "dev" und "Canary".</span><span class="sxs-lookup"><span data-stu-id="8a9cf-130">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="8a9cf-131">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="8a9cf-131">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="8a9cf-132">Das NewBrowserVersionAvailable-Ereignis wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-132">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="8a9cf-133">public event EventHandler<-Objekt > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="8a9cf-133">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="8a9cf-134">Wenn Sie die neuere Version des Browsers verwenden möchten, müssen Sie eine neue Umgebung und WebView erstellen.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-134">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="8a9cf-135">Dieses Ereignis wird nur für eine neue Version aus dem gleichen Edge-Kanal ausgelöst, von dem aus der Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-135">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="8a9cf-136">Wenn Sie nicht mit installiertem Edge ausgeführt wird, wird kein Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-136">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="8a9cf-137">Da ein benutzerdatenordner nur von einem Browserprozess gleichzeitig verwendet werden kann, wenn Sie denselben benutzerdatenordner in den Webansichten mithilfe der neuen Browserversion verwenden möchten, müssen Sie die Umgebung und Webansichten schließen, die zuerst die ältere Version des Browsers verwenden.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-137">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="8a9cf-138">Oder fordern Sie den Benutzer einfach auf, die APP neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-138">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="8a9cf-139">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="8a9cf-139">CreateAsync</span></span> 

<span data-ttu-id="8a9cf-140">Erstellt eine immergrüne WebView2-Umgebung unter Verwendung der installierten Edge-Version.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-140">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

> <span data-ttu-id="8a9cf-141">public static Async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [createasync](#createasync)(String browserExecutableFolder, String userDataFolder, CoreWebView2EnvironmentOptions Optionen)</span><span class="sxs-lookup"><span data-stu-id="8a9cf-141">public static async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md) > [CreateAsync](#createasync)(string browserExecutableFolder, string userDataFolder, CoreWebView2EnvironmentOptions options)</span></span>

##### <span data-ttu-id="8a9cf-142">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a9cf-142">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="8a9cf-143">Der relative Pfad zu dem Ordner, in dem sich der eingebettete Edge befindet.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-143">The relative path to the folder that contains the embedded Edge.</span></span> 

* `userDataFolder` <span data-ttu-id="8a9cf-144">userDataFolder kann angegeben werden, um den Standardspeicherort des Benutzerdatenordners für WebView2 zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-144">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> 

* `options` <span data-ttu-id="8a9cf-145">Optionen zum Erstellen der WebView2-Umgebung</span><span class="sxs-lookup"><span data-stu-id="8a9cf-145">Options used to create WebView2 Environment.</span></span>

#### <span data-ttu-id="8a9cf-146">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="8a9cf-146">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="8a9cf-147">Erstellen Sie einen neuen WebView asynchron.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-147">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="8a9cf-148">Public Async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="8a9cf-148">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="8a9cf-149">ParentWindow ist das HWND, in dem die WebView-Ansicht angezeigt werden soll und von der die Eingabe empfangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-149">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="8a9cf-150">Die WebView fügt dem bereitgestellten Fenster während der Erstellung von WebView ein untergeordnetes Fenster hinzu.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-150">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="8a9cf-151">Die Z-Reihenfolge und andere Elemente, die von der Reihenfolge der nebengeordneten Fenster beeinflusst werden, sind dementsprechend betroffen.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-151">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="8a9cf-152">Es wird empfohlen, die Anwendungsbenutzer Modell-ID für den Prozess oder das Anwendungsfenster festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-152">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="8a9cf-153">Wenn None gesetzt ist, wird bei der Erstellung von WebView eine generierte Anwendungsbenutzer Modell-ID auf das Stammfenster von ParentWindow eingestellt.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-153">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="8a9cf-154">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="8a9cf-154">CreateWebResourceResponse</span></span> 

<span data-ttu-id="8a9cf-155">Erstellen Sie ein neues Webressourcen-Antwortobjekt.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-155">Create a new web resource response object.</span></span>

> <span data-ttu-id="8a9cf-156">Public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int Statuscode, String ReasonPhrase, String Headers)</span><span class="sxs-lookup"><span data-stu-id="8a9cf-156">public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="8a9cf-157">Die Kopfzeilen ist die unformatierte Antwortheader Zeichenfolge, die durch einen Zeilenumbruch getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-157">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="8a9cf-158">Es ist auch möglich, dieses Objekt mit einer leeren Headerzeichenfolge zu erstellen und dann die Kopfzeilen Zeile für Zeile mithilfe der CoreWebView2HttpResponseHeaders zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-158">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="8a9cf-159">Informationen zu anderen Parametern finden Sie unter CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-159">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

