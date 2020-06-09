---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 212e515c07446fefefc91292595f15fe655b46e5
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698043"
---
# <span data-ttu-id="ccdd1-104">Schnittstellen ICoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="ccdd1-104">interface ICoreWebView2EnvironmentOptions</span></span> 

> [!NOTE]
> <span data-ttu-id="ccdd1-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="ccdd1-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="ccdd1-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2EnvironmentOptions
  : public IUnknown
```

<span data-ttu-id="ccdd1-107">Optionen zum Erstellen der WebView2-Umgebung</span><span class="sxs-lookup"><span data-stu-id="ccdd1-107">Options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="ccdd1-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ccdd1-108">Summary</span></span>

 <span data-ttu-id="ccdd1-109">Member</span><span class="sxs-lookup"><span data-stu-id="ccdd1-109">Members</span></span>                        | <span data-ttu-id="ccdd1-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ccdd1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ccdd1-111">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="ccdd1-111">get_AdditionalBrowserArguments</span></span>](#get_additionalbrowserarguments) | <span data-ttu-id="ccdd1-112">AdditionalBrowserArguments kann angegeben werden, um das Verhalten von WebView zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-112">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>
[<span data-ttu-id="ccdd1-113">get_Language</span><span class="sxs-lookup"><span data-stu-id="ccdd1-113">get_Language</span></span>](#get_language) | <span data-ttu-id="ccdd1-114">Die Standardsprache, mit der WebView ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-114">The default language that WebView will run with.</span></span>
[<span data-ttu-id="ccdd1-115">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="ccdd1-115">get_TargetCompatibleBrowserVersion</span></span>](#get_targetcompatiblebrowserversion) | <span data-ttu-id="ccdd1-116">Die Version der Edge-WebView2-Runtime-Binärdateien, die für die Kompatibilität mit der aufrufenden Anwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-116">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>
[<span data-ttu-id="ccdd1-117">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="ccdd1-117">put_AdditionalBrowserArguments</span></span>](#put_additionalbrowserarguments) | <span data-ttu-id="ccdd1-118">Festlegen der AdditionalBrowserArguments-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ccdd1-118">Set the AdditionalBrowserArguments property.</span></span>
[<span data-ttu-id="ccdd1-119">put_Language</span><span class="sxs-lookup"><span data-stu-id="ccdd1-119">put_Language</span></span>](#put_language) | <span data-ttu-id="ccdd1-120">Festlegen der Language-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ccdd1-120">Set the Language property.</span></span>
[<span data-ttu-id="ccdd1-121">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="ccdd1-121">put_TargetCompatibleBrowserVersion</span></span>](#put_targetcompatiblebrowserversion) | <span data-ttu-id="ccdd1-122">Setzen Sie die TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-122">Set the TargetCompatibleBrowserVersion.</span></span>

<span data-ttu-id="ccdd1-123">Eine Standardimplementierung wird in WebView2EnvironmentOptions. h bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-123">A default implementation is provided in WebView2EnvironmentOptions.h.</span></span>

```cpp
    auto options = Microsoft::WRL::Make<CoreWebView2EnvironmentOptions>();
    if(!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
```

## <span data-ttu-id="ccdd1-124">Member</span><span class="sxs-lookup"><span data-stu-id="ccdd1-124">Members</span></span>

#### <span data-ttu-id="ccdd1-125">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="ccdd1-125">get_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="ccdd1-126">AdditionalBrowserArguments kann angegeben werden, um das Verhalten von WebView zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-126">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>

> <span data-ttu-id="ccdd1-127">Public HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="ccdd1-127">public HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \* value)</span></span>

<span data-ttu-id="ccdd1-128">Diese werden als Teil der Befehlszeile an den Browserprozess übergeben.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-128">These will be passed to the browser process as part of the command line.</span></span> <span data-ttu-id="ccdd1-129">Weitere Informationen zu Befehlszeilen wechseln in den Browserprozess finden Sie unter [Ausführen von Chrom mit Flags](https://aka.ms/RunChromiumWithFlags) .</span><span class="sxs-lookup"><span data-stu-id="ccdd1-129">See [Run Chromium with Flags](https://aka.ms/RunChromiumWithFlags) for more information about command line switches to browser process.</span></span> <span data-ttu-id="ccdd1-130">Wenn die APP mit einem Befehlszeilen Schalter gestartet wird, `--edge-webview-switches=xxx` wird der Wert dieses Schalters (xxx im obigen Beispiel) auch an die Befehlszeile des Browser Prozesses angefügt.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-130">If the app is launched with a command line switch `--edge-webview-switches=xxx` the value of that switch (xxx in the above example) will also be appended to the browser process command line.</span></span> <span data-ttu-id="ccdd1-131">Bestimmte Schalter wie `--user-data-dir` sind intern und wichtig für WebView.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-131">Certain switches like `--user-data-dir` are internal and important to WebView.</span></span> <span data-ttu-id="ccdd1-132">Diese Schalter werden ignoriert, auch wenn Sie angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-132">Those switches will be ignored even if specified.</span></span> <span data-ttu-id="ccdd1-133">Wenn dieselben Schalter mehrmals angegeben werden, gewinnt der letzte.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-133">If the same switches are specified multiple times, the last one wins.</span></span> <span data-ttu-id="ccdd1-134">Es wird nicht versucht, die verschiedenen Werte desselben Schalters zusammenzuführen, mit Ausnahme von deaktivierten und aktivierten Features.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-134">There is no attempt to merge the different values of the same switch, except for disabled and enabled features.</span></span> <span data-ttu-id="ccdd1-135">Die Features, die von `--enable-features` und `--disable-features` mit einfacher Logik zusammengeführt werden: die Features sind die Vereinigung der angegebenen Features und integrierten Features, und wenn ein Feature deaktiviert ist, wird es aus der Liste der aktivierten Features entfernt.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-135">The features specified by `--enable-features` and `--disable-features` will be merged with simple logic: the features will be the union of the specified features and built-in features, and if a feature is disabled, it will be removed from the enabled features list.</span></span> <span data-ttu-id="ccdd1-136">Der Befehlszeilenwert des App-Prozesses `--edge-webview-switches` wird verarbeitet, nachdem der additionalBrowserArguments-Parameter verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-136">App process's command line `--edge-webview-switches` value are processed after the additionalBrowserArguments parameter is processed.</span></span> <span data-ttu-id="ccdd1-137">Bestimmte Features sind intern deaktiviert und können nicht aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-137">Certain features are disabled internally and can't be enabled.</span></span> <span data-ttu-id="ccdd1-138">Wenn die Analyse bei den angegebenen Schaltern fehlgeschlagen ist, werden Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-138">If parsing failed for the specified switches, they will be ignored.</span></span> <span data-ttu-id="ccdd1-139">Standardmäßig wird der Browserprozess ohne zusätzliche Flags ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-139">Default is to run browser process with no extra flags.</span></span>

#### <span data-ttu-id="ccdd1-140">get_Language</span><span class="sxs-lookup"><span data-stu-id="ccdd1-140">get_Language</span></span> 

<span data-ttu-id="ccdd1-141">Die Standardsprache, mit der WebView ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-141">The default language that WebView will run with.</span></span>

> <span data-ttu-id="ccdd1-142">Public HRESULT [get_Language](#get_language)(LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="ccdd1-142">public HRESULT [get_Language](#get_language)(LPWSTR \* value)</span></span>

<span data-ttu-id="ccdd1-143">Sie bezieht sich auf Browser-UIs wie Kontextmenüs und Dialogfelder.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-143">It applies to browser UIs like context menu and dialogs.</span></span> <span data-ttu-id="ccdd1-144">Sie gilt auch für den HTTP-Header Accept-Languages, der von WebView an Websites gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-144">It also applies to the accept-languages HTTP header that WebView sends to web sites.</span></span> <span data-ttu-id="ccdd1-145">Das Format von `language[-country]` Where `language` ist der 2-Buchstaben-Code von ISO 639 und `country` der 2-Buchstaben-Code von ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-145">It is in the format of `language[-country]` where `language` is the 2 letter code from ISO 639 and `country` is the 2 letter code from ISO 3166.</span></span>

#### <span data-ttu-id="ccdd1-146">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="ccdd1-146">get_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="ccdd1-147">Die Version der Edge-WebView2-Runtime-Binärdateien, die für die Kompatibilität mit der aufrufenden Anwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-147">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>

> <span data-ttu-id="ccdd1-148">Public HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="ccdd1-148">public HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \* value)</span></span>

<span data-ttu-id="ccdd1-149">Dies ist standardmäßig die Edge WebView2-Laufzeitversion, die der Version des SDK entspricht, das die Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-149">This defaults to the Edge WebView2 Runtime version that corresponds with the version of the SDK the application is using.</span></span> <span data-ttu-id="ccdd1-150">Das Format dieses Werts entspricht dem Format der BrowserVersionString-Eigenschaft und anderen Browserversion-Werten.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-150">The format of this value is the same as the format of the BrowserVersionString property and other BrowserVersion values.</span></span> <span data-ttu-id="ccdd1-151">Nur der Versions Teil des Browserversion-Werts wird berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-151">Only the version part of the BrowserVersion value is respected.</span></span> <span data-ttu-id="ccdd1-152">Wenn es vorhanden ist, wird das Kanal Suffix ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-152">The channel suffix, if it exists, is ignored.</span></span> <span data-ttu-id="ccdd1-153">Die Version der tatsächlich verwendeten Edge-WebView2-Runtime-Binärdateien kann sich vom angegebenen TargetCompatibleBrowserVersion unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-153">The version of the Edge WebView2 Runtime binaries actually used may be different from the specified TargetCompatibleBrowserVersion.</span></span> <span data-ttu-id="ccdd1-154">Sie sind nur garantiert kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-154">They are only guaranteed to be compatible.</span></span> <span data-ttu-id="ccdd1-155">Sie können die aktuelle Version auf der BrowserVersionString-Eigenschaft auf der ICoreWebView2Environment-Eigenschaft überprüfen.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-155">You can check the actual version on the BrowserVersionString property on the ICoreWebView2Environment.</span></span>

#### <span data-ttu-id="ccdd1-156">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="ccdd1-156">put_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="ccdd1-157">Festlegen der AdditionalBrowserArguments-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ccdd1-157">Set the AdditionalBrowserArguments property.</span></span>

> <span data-ttu-id="ccdd1-158">Public HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(LPCWSTR-Wert)</span><span class="sxs-lookup"><span data-stu-id="ccdd1-158">public HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(LPCWSTR value)</span></span>

#### <span data-ttu-id="ccdd1-159">put_Language</span><span class="sxs-lookup"><span data-stu-id="ccdd1-159">put_Language</span></span> 

<span data-ttu-id="ccdd1-160">Festlegen der Language-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ccdd1-160">Set the Language property.</span></span>

> <span data-ttu-id="ccdd1-161">Public HRESULT [put_Language](#put_language)(LPCWSTR-Wert)</span><span class="sxs-lookup"><span data-stu-id="ccdd1-161">public HRESULT [put_Language](#put_language)(LPCWSTR value)</span></span>

#### <span data-ttu-id="ccdd1-162">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="ccdd1-162">put_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="ccdd1-163">Setzen Sie die TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-163">Set the TargetCompatibleBrowserVersion.</span></span>

> <span data-ttu-id="ccdd1-164">Public HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(LPCWSTR-Wert)</span><span class="sxs-lookup"><span data-stu-id="ccdd1-164">public HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(LPCWSTR value)</span></span>

