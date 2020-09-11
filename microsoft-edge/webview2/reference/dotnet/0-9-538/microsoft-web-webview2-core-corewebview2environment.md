---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2Environment
ms.openlocfilehash: d1e30c17239eb1b609eb3f2c63e48a3a59616131
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011027"
---
# <span data-ttu-id="ef580-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Environment Klasse</span><span class="sxs-lookup"><span data-stu-id="ef580-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="ef580-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="ef580-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="ef580-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="ef580-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="ef580-107">Dies stellt die WebView2-Umgebung dar.</span><span class="sxs-lookup"><span data-stu-id="ef580-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="ef580-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ef580-108">Summary</span></span>

 <span data-ttu-id="ef580-109">Member</span><span class="sxs-lookup"><span data-stu-id="ef580-109">Members</span></span>                        | <span data-ttu-id="ef580-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ef580-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ef580-111">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="ef580-111">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="ef580-112">Die Browser Versionsinformationen des aktuellen CoreWebView2Environment, einschließlich des Kanal namens, wenn es sich nicht um den stabilen Kanal handelt.</span><span class="sxs-lookup"><span data-stu-id="ef580-112">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="ef580-113">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="ef580-113">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="ef580-114">Das NewBrowserVersionAvailable-Ereignis wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="ef580-114">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="ef580-115">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="ef580-115">CompareBrowserVersions</span></span>](#comparebrowserversions) | <span data-ttu-id="ef580-116">Vergleichen Sie die Browserversionen korrekt, um zu ermitteln, welche Version neuer, älter oder gleich ist.</span><span class="sxs-lookup"><span data-stu-id="ef580-116">Compare browser versions correctly to determine which version is newer, older or same.</span></span>
[<span data-ttu-id="ef580-117">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="ef580-117">CreateAsync</span></span>](#createasync) | <span data-ttu-id="ef580-118">Erstellt eine immergrüne WebView2-Umgebung unter Verwendung der installierten Edge-Version.</span><span class="sxs-lookup"><span data-stu-id="ef580-118">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="ef580-119">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="ef580-119">CreateCoreWebView2CompositionControllerAsync</span></span>](#createcorewebview2compositioncontrollerasync) | <span data-ttu-id="ef580-120">Erstellen Sie ein neues WebView-Element für die Verwendung mit Visual Hosting asynchron.</span><span class="sxs-lookup"><span data-stu-id="ef580-120">Asynchronously create a new WebView for use with visual hosting.</span></span>
[<span data-ttu-id="ef580-121">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="ef580-121">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="ef580-122">Erstellen Sie einen neuen WebView asynchron.</span><span class="sxs-lookup"><span data-stu-id="ef580-122">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="ef580-123">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="ef580-123">CreateCoreWebView2PointerInfo</span></span>](#createcorewebview2pointerinfo) | <span data-ttu-id="ef580-124">Erstellen Sie ein leeres CoreWebView2PointerInfo.</span><span class="sxs-lookup"><span data-stu-id="ef580-124">Create an empty CoreWebView2PointerInfo.</span></span>
[<span data-ttu-id="ef580-125">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="ef580-125">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="ef580-126">Erstellen Sie ein neues Webressourcen-Antwortobjekt.</span><span class="sxs-lookup"><span data-stu-id="ef580-126">Create a new web resource response object.</span></span>
[<span data-ttu-id="ef580-127">GetAvailableBrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="ef580-127">GetAvailableBrowserVersionString</span></span>](#getavailablebrowserversionstring) | <span data-ttu-id="ef580-128">Rufen Sie die Browser Versionsinformationen einschließlich des Kanal namens ab, wenn es sich nicht um den stabilen Kanal oder den eingebetteten Edge handelt.</span><span class="sxs-lookup"><span data-stu-id="ef580-128">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>
[<span data-ttu-id="ef580-129">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="ef580-129">GetProviderForHwnd</span></span>](#getproviderforhwnd) | <span data-ttu-id="ef580-130">Gibt den Benutzeroberflächenautomatisierungs-Anbieter für die CoreWebView2CompositionController zurück, die dem angegebenen HWND entspricht.</span><span class="sxs-lookup"><span data-stu-id="ef580-130">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

<span data-ttu-id="ef580-131">Webansichten, die aus einer Umgebung erstellt wurden, die im Browser Prozess ausgeführt wird, der mit Umgebungsparametern und aus einer Umgebung erstellten Objekten erstellt wurde, sollten in derselben Umgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef580-131">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="ef580-132">Die Verwendung in unterschiedlichen Umgebungen ist nicht garantiert kompatibel und kann fehlerhaft sein.</span><span class="sxs-lookup"><span data-stu-id="ef580-132">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="ef580-133">Member</span><span class="sxs-lookup"><span data-stu-id="ef580-133">Members</span></span>

#### <span data-ttu-id="ef580-134">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="ef580-134">BrowserVersionString</span></span> 

<span data-ttu-id="ef580-135">Die Browser Versionsinformationen des aktuellen CoreWebView2Environment, einschließlich des Kanal namens, wenn es sich nicht um den stabilen Kanal handelt.</span><span class="sxs-lookup"><span data-stu-id="ef580-135">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="ef580-136">public String [BrowserVersionString](#browserversionstring)</span><span class="sxs-lookup"><span data-stu-id="ef580-136">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="ef580-137">Dies entspricht dem Format der GetAvailableCoreWebView2BrowserVersionString-API.</span><span class="sxs-lookup"><span data-stu-id="ef580-137">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="ef580-138">Kanalnamen sind "Beta", "dev" und "Canary".</span><span class="sxs-lookup"><span data-stu-id="ef580-138">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="ef580-139">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="ef580-139">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="ef580-140">Das NewBrowserVersionAvailable-Ereignis wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="ef580-140">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="ef580-141">public event EventHandler<-Objekt > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="ef580-141">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="ef580-142">Wenn Sie die neuere Version des Browsers verwenden möchten, müssen Sie eine neue Umgebung und WebView erstellen.</span><span class="sxs-lookup"><span data-stu-id="ef580-142">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="ef580-143">Dieses Ereignis wird nur für eine neue Version aus dem gleichen Edge-Kanal ausgelöst, von dem aus der Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef580-143">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="ef580-144">Wenn Sie nicht mit installiertem Edge ausgeführt wird, wird kein Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ef580-144">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="ef580-145">Da ein benutzerdatenordner nur von einem Browserprozess gleichzeitig verwendet werden kann, wenn Sie denselben benutzerdatenordner in den Webansichten mithilfe der neuen Browserversion verwenden möchten, müssen Sie die Umgebung und Webansichten schließen, die zuerst die ältere Version des Browsers verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef580-145">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="ef580-146">Oder fordern Sie den Benutzer einfach auf, die APP neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="ef580-146">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="ef580-147">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="ef580-147">CompareBrowserVersions</span></span> 

<span data-ttu-id="ef580-148">Vergleichen Sie die Browserversionen korrekt, um zu ermitteln, welche Version neuer, älter oder gleich ist.</span><span class="sxs-lookup"><span data-stu-id="ef580-148">Compare browser versions correctly to determine which version is newer, older or same.</span></span>

> <span data-ttu-id="ef580-149">public static int [CompareBrowserVersions](#comparebrowserversions)(String Version1, String Version2)</span><span class="sxs-lookup"><span data-stu-id="ef580-149">public static int [CompareBrowserVersions](#comparebrowserversions)(string version1, string version2)</span></span>

<span data-ttu-id="ef580-150">Gibt-1, 0 oder 1 zurück, je nachdem, ob Version1 kleiner als, gleich oder größer als Version2 ist.</span><span class="sxs-lookup"><span data-stu-id="ef580-150">Returns -1, 0 or 1 depending on whether version1 is less than, equal to or greater than version2, respectively.</span></span>

##### <span data-ttu-id="ef580-151">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef580-151">Parameters</span></span>
* `version1` <span data-ttu-id="ef580-152">Eine der zu vergleichenden Versionszeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="ef580-152">One of the version strings to compare.</span></span> 

* `version2` <span data-ttu-id="ef580-153">Die andere zu vergleichende Versionszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ef580-153">The other version string to compare.</span></span>

#### <span data-ttu-id="ef580-154">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="ef580-154">CreateAsync</span></span> 

<span data-ttu-id="ef580-155">Erstellt eine immergrüne WebView2-Umgebung unter Verwendung der installierten Edge-Version.</span><span class="sxs-lookup"><span data-stu-id="ef580-155">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

> <span data-ttu-id="ef580-156">public static Async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [createasync](#createasync)(String browserExecutableFolder, String userDataFolder, CoreWebView2EnvironmentOptions Optionen)</span><span class="sxs-lookup"><span data-stu-id="ef580-156">public static async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md) > [CreateAsync](#createasync)(string browserExecutableFolder, string userDataFolder, CoreWebView2EnvironmentOptions options)</span></span>

##### <span data-ttu-id="ef580-157">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef580-157">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="ef580-158">Der relative Pfad zu dem Ordner, in dem sich der eingebettete Edge befindet.</span><span class="sxs-lookup"><span data-stu-id="ef580-158">The relative path to the folder that contains the embedded Edge.</span></span> 

* `userDataFolder` <span data-ttu-id="ef580-159">userDataFolder kann angegeben werden, um den Standardspeicherort des Benutzerdatenordners für WebView2 zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ef580-159">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> 

* `options` <span data-ttu-id="ef580-160">Optionen zum Erstellen der WebView2-Umgebung</span><span class="sxs-lookup"><span data-stu-id="ef580-160">Options used to create WebView2 Environment.</span></span>

#### <span data-ttu-id="ef580-161">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="ef580-161">CreateCoreWebView2CompositionControllerAsync</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="ef580-162">Erstellen Sie ein neues WebView-Element für die Verwendung mit Visual Hosting asynchron.</span><span class="sxs-lookup"><span data-stu-id="ef580-162">Asynchronously create a new WebView for use with visual hosting.</span></span>

> <span data-ttu-id="ef580-163">Public Async Task< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md)  >  [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="ef580-163">public async Task< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md) > [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="ef580-164">ParentWindow ist das HWND, in dem die APP die visuelle Struktur von WebView verbindet.</span><span class="sxs-lookup"><span data-stu-id="ef580-164">parentWindow is the HWND in which the app will connect the visual tree of the WebView.</span></span> <span data-ttu-id="ef580-165">Hierbei handelt es sich um das HWND, in dem die APP Zeiger-und Mauseingaben für die WebView erhält (und SendMouseInput/SendPointerInput für Forward verwenden muss).</span><span class="sxs-lookup"><span data-stu-id="ef580-165">This will be the HWND that the app will receive pointer/ mouse input meant for the WebView (and will need to use SendMouseInput/ SendPointerInput to forward).</span></span> <span data-ttu-id="ef580-166">Wenn die APP die visuelle WebView-Struktur unter einem anderen Fenster verschiebt, muss CoreWebView2CompositionController. ParentWindow so eingestellt werden, dass das neue übergeordnete HWND der visuellen Struktur aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ef580-166">If the app moves the WebView visual tree to underneath a different window, then it needs to set CoreWebView2CompositionController.ParentWindow to update the new parent HWND of the visual tree.</span></span>

<span data-ttu-id="ef580-167">Legen Sie die RootVisualTarget-Eigenschaft für das erstellte CoreWebView2CompositionController-Objekt so ein, dass es eine visuelle Struktur bereitstellt</span><span class="sxs-lookup"><span data-stu-id="ef580-167">Set RootVisualTarget property on the created CoreWebView2CompositionController to provide a visual to host the browser's visual tree.</span></span>

<span data-ttu-id="ef580-168">Es wird empfohlen, die Anwendungsbenutzer Modell-ID für den Prozess oder das Anwendungsfenster festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ef580-168">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="ef580-169">Wenn None gesetzt ist, wird bei der Erstellung von WebView eine generierte Anwendungsbenutzer Modell-ID auf das Stammfenster von ParentWindow eingestellt.</span><span class="sxs-lookup"><span data-stu-id="ef580-169">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="ef580-170">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="ef580-170">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="ef580-171">Erstellen Sie einen neuen WebView asynchron.</span><span class="sxs-lookup"><span data-stu-id="ef580-171">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="ef580-172">Public Async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="ef580-172">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="ef580-173">ParentWindow ist das HWND, in dem die WebView-Ansicht angezeigt werden soll und von der die Eingabe empfangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef580-173">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="ef580-174">Die WebView fügt dem bereitgestellten Fenster während der Erstellung von WebView ein untergeordnetes Fenster hinzu.</span><span class="sxs-lookup"><span data-stu-id="ef580-174">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="ef580-175">Die Z-Reihenfolge und andere Elemente, die von der Reihenfolge der nebengeordneten Fenster beeinflusst werden, sind dementsprechend betroffen.</span><span class="sxs-lookup"><span data-stu-id="ef580-175">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="ef580-176">Es wird empfohlen, die Anwendungsbenutzer Modell-ID für den Prozess oder das Anwendungsfenster festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ef580-176">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="ef580-177">Wenn None gesetzt ist, wird bei der Erstellung von WebView eine generierte Anwendungsbenutzer Modell-ID auf das Stammfenster von ParentWindow eingestellt.</span><span class="sxs-lookup"><span data-stu-id="ef580-177">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="ef580-178">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="ef580-178">CreateCoreWebView2PointerInfo</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="ef580-179">Erstellen Sie ein leeres CoreWebView2PointerInfo.</span><span class="sxs-lookup"><span data-stu-id="ef580-179">Create an empty CoreWebView2PointerInfo.</span></span>

> <span data-ttu-id="ef580-180">Public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span><span class="sxs-lookup"><span data-stu-id="ef580-180">public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span></span>

<span data-ttu-id="ef580-181">Der zurückgegebene CoreWebView2PointerInfo muss mit allen relevanten Informationen gefüllt werden, bevor SendPointerInput aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ef580-181">The returned CoreWebView2PointerInfo needs to be populated with all of the relevant info before calling SendPointerInput.</span></span>

#### <span data-ttu-id="ef580-182">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="ef580-182">CreateWebResourceResponse</span></span> 

<span data-ttu-id="ef580-183">Erstellen Sie ein neues Webressourcen-Antwortobjekt.</span><span class="sxs-lookup"><span data-stu-id="ef580-183">Create a new web resource response object.</span></span>

> <span data-ttu-id="ef580-184">Public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int Statuscode, String ReasonPhrase, String Headers)</span><span class="sxs-lookup"><span data-stu-id="ef580-184">public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="ef580-185">Die Kopfzeilen ist die unformatierte Antwortheader Zeichenfolge, die durch einen Zeilenumbruch getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="ef580-185">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="ef580-186">Es ist auch möglich, dieses Objekt mit einer leeren Headerzeichenfolge zu erstellen und dann die Kopfzeilen Zeile für Zeile mithilfe der CoreWebView2HttpResponseHeaders zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ef580-186">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="ef580-187">Informationen zu anderen Parametern finden Sie unter CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="ef580-187">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

#### <span data-ttu-id="ef580-188">GetAvailableBrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="ef580-188">GetAvailableBrowserVersionString</span></span> 

<span data-ttu-id="ef580-189">Rufen Sie die Browser Versionsinformationen einschließlich des Kanal namens ab, wenn es sich nicht um den stabilen Kanal oder den eingebetteten Edge handelt.</span><span class="sxs-lookup"><span data-stu-id="ef580-189">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

> <span data-ttu-id="ef580-190">public static String [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(String browserExecutableFolder)</span><span class="sxs-lookup"><span data-stu-id="ef580-190">public static string [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(string browserExecutableFolder)</span></span>

##### <span data-ttu-id="ef580-191">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef580-191">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="ef580-192">Der relative Pfad zu dem Ordner, in dem sich der eingebettete Edge befindet.</span><span class="sxs-lookup"><span data-stu-id="ef580-192">The relative path to the folder that contains the embedded Edge.</span></span>

#### <span data-ttu-id="ef580-193">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="ef580-193">GetProviderForHwnd</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="ef580-194">Gibt den Benutzeroberflächenautomatisierungs-Anbieter für die CoreWebView2CompositionController zurück, die dem angegebenen HWND entspricht.</span><span class="sxs-lookup"><span data-stu-id="ef580-194">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

> <span data-ttu-id="ef580-195">public Object [GetProviderForHwnd](#getproviderforhwnd)(IntPtr hwnd)</span><span class="sxs-lookup"><span data-stu-id="ef580-195">public object [GetProviderForHwnd](#getproviderforhwnd)(IntPtr hwnd)</span></span>

