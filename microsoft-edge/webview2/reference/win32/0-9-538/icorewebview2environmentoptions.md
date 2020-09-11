---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2EnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2EnvironmentOptions
ms.openlocfilehash: 825ecde664ddd43ec5a28721f6da12250a632f2e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010236"
---
# <span data-ttu-id="35e54-104">0.9.579-Interface-ICoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="35e54-104">0.9.579 - interface ICoreWebView2EnvironmentOptions</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2EnvironmentOptions
  : public IUnknown
```

<span data-ttu-id="35e54-105">Optionen zum Erstellen der WebView2-Umgebung</span><span class="sxs-lookup"><span data-stu-id="35e54-105">Options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="35e54-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="35e54-106">Summary</span></span>

 <span data-ttu-id="35e54-107">Member</span><span class="sxs-lookup"><span data-stu-id="35e54-107">Members</span></span>                        | <span data-ttu-id="35e54-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="35e54-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="35e54-109">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="35e54-109">get_AdditionalBrowserArguments</span></span>](#get_additionalbrowserarguments) | <span data-ttu-id="35e54-110">AdditionalBrowserArguments kann angegeben werden, um das Verhalten von WebView zu ändern.</span><span class="sxs-lookup"><span data-stu-id="35e54-110">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>
[<span data-ttu-id="35e54-111">get_Language</span><span class="sxs-lookup"><span data-stu-id="35e54-111">get_Language</span></span>](#get_language) | <span data-ttu-id="35e54-112">Die Standardsprache, mit der WebView ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="35e54-112">The default language that WebView will run with.</span></span>
[<span data-ttu-id="35e54-113">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="35e54-113">get_TargetCompatibleBrowserVersion</span></span>](#get_targetcompatiblebrowserversion) | <span data-ttu-id="35e54-114">Die Version der Edge-WebView2-Runtime-Binärdateien, die für die Kompatibilität mit der aufrufenden Anwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="35e54-114">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>
[<span data-ttu-id="35e54-115">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="35e54-115">put_AdditionalBrowserArguments</span></span>](#put_additionalbrowserarguments) | <span data-ttu-id="35e54-116">Festlegen der AdditionalBrowserArguments-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="35e54-116">Set the AdditionalBrowserArguments property.</span></span>
[<span data-ttu-id="35e54-117">put_Language</span><span class="sxs-lookup"><span data-stu-id="35e54-117">put_Language</span></span>](#put_language) | <span data-ttu-id="35e54-118">Festlegen der Language-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="35e54-118">Set the Language property.</span></span>
[<span data-ttu-id="35e54-119">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="35e54-119">put_TargetCompatibleBrowserVersion</span></span>](#put_targetcompatiblebrowserversion) | <span data-ttu-id="35e54-120">Setzen Sie die TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="35e54-120">Set the TargetCompatibleBrowserVersion.</span></span>

<span data-ttu-id="35e54-121">Eine Standardimplementierung wird in WebView2EnvironmentOptions. h bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="35e54-121">A default implementation is provided in WebView2EnvironmentOptions.h.</span></span>

```cpp
    auto options = Microsoft::WRL::Make<CoreWebView2ExperimentalEnvironmentOptions>();
    CHECK_FAILURE(options->put_IsSingleSignOnUsingOSPrimaryAccountEnabled(
        m_AADSSOEnabled ? TRUE : FALSE));
    if (!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
```

## <span data-ttu-id="35e54-122">Member</span><span class="sxs-lookup"><span data-stu-id="35e54-122">Members</span></span>

#### <span data-ttu-id="35e54-123">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="35e54-123">get_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="35e54-124">AdditionalBrowserArguments kann angegeben werden, um das Verhalten von WebView zu ändern.</span><span class="sxs-lookup"><span data-stu-id="35e54-124">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>

> <span data-ttu-id="35e54-125">Public HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="35e54-125">public HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \* value)</span></span>

<span data-ttu-id="35e54-126">Diese werden als Teil der Befehlszeile an den Browserprozess übergeben.</span><span class="sxs-lookup"><span data-stu-id="35e54-126">These will be passed to the browser process as part of the command line.</span></span> <span data-ttu-id="35e54-127">Weitere Informationen zu Befehlszeilen wechseln in den Browserprozess finden Sie unter [Ausführen von Chrom mit Flags](https://aka.ms/RunChromiumWithFlags) .</span><span class="sxs-lookup"><span data-stu-id="35e54-127">See [Run Chromium with Flags](https://aka.ms/RunChromiumWithFlags) for more information about command line switches to browser process.</span></span> <span data-ttu-id="35e54-128">Wenn die APP mit einem Befehlszeilen Schalter gestartet wird, `--edge-webview-switches=xxx` wird der Wert dieses Schalters (xxx im obigen Beispiel) auch an die Befehlszeile des Browser Prozesses angefügt.</span><span class="sxs-lookup"><span data-stu-id="35e54-128">If the app is launched with a command line switch `--edge-webview-switches=xxx` the value of that switch (xxx in the above example) will also be appended to the browser process command line.</span></span> <span data-ttu-id="35e54-129">Bestimmte Schalter wie `--user-data-dir` sind intern und wichtig für WebView.</span><span class="sxs-lookup"><span data-stu-id="35e54-129">Certain switches like `--user-data-dir` are internal and important to WebView.</span></span> <span data-ttu-id="35e54-130">Diese Schalter werden ignoriert, auch wenn Sie angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="35e54-130">Those switches will be ignored even if specified.</span></span> <span data-ttu-id="35e54-131">Wenn dieselben Schalter mehrmals angegeben werden, gewinnt der letzte.</span><span class="sxs-lookup"><span data-stu-id="35e54-131">If the same switches are specified multiple times, the last one wins.</span></span> <span data-ttu-id="35e54-132">Es wird nicht versucht, die verschiedenen Werte desselben Schalters zusammenzuführen, mit Ausnahme von deaktivierten und aktivierten Features.</span><span class="sxs-lookup"><span data-stu-id="35e54-132">There is no attempt to merge the different values of the same switch, except for disabled and enabled features.</span></span> <span data-ttu-id="35e54-133">Die Features, die von `--enable-features` und `--disable-features` mit einfacher Logik zusammengeführt werden: die Features sind die Vereinigung der angegebenen Features und integrierten Features, und wenn ein Feature deaktiviert ist, wird es aus der Liste der aktivierten Features entfernt.</span><span class="sxs-lookup"><span data-stu-id="35e54-133">The features specified by `--enable-features` and `--disable-features` will be merged with simple logic: the features will be the union of the specified features and built-in features, and if a feature is disabled, it will be removed from the enabled features list.</span></span> <span data-ttu-id="35e54-134">Der Befehlszeilenwert des App-Prozesses `--edge-webview-switches` wird verarbeitet, nachdem der additionalBrowserArguments-Parameter verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="35e54-134">App process's command line `--edge-webview-switches` value are processed after the additionalBrowserArguments parameter is processed.</span></span> <span data-ttu-id="35e54-135">Bestimmte Features sind intern deaktiviert und können nicht aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="35e54-135">Certain features are disabled internally and can't be enabled.</span></span> <span data-ttu-id="35e54-136">Wenn die Analyse bei den angegebenen Schaltern fehlgeschlagen ist, werden Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="35e54-136">If parsing failed for the specified switches, they will be ignored.</span></span> <span data-ttu-id="35e54-137">Standardmäßig wird der Browserprozess ohne zusätzliche Flags ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="35e54-137">Default is to run browser process with no extra flags.</span></span>

#### <span data-ttu-id="35e54-138">get_Language</span><span class="sxs-lookup"><span data-stu-id="35e54-138">get_Language</span></span> 

<span data-ttu-id="35e54-139">Die Standardsprache, mit der WebView ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="35e54-139">The default language that WebView will run with.</span></span>

> <span data-ttu-id="35e54-140">Public HRESULT [get_Language](#get_language)(LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="35e54-140">public HRESULT [get_Language](#get_language)(LPWSTR \* value)</span></span>

<span data-ttu-id="35e54-141">Sie bezieht sich auf Browser-UIs wie Kontextmenüs und Dialogfelder.</span><span class="sxs-lookup"><span data-stu-id="35e54-141">It applies to browser UIs like context menu and dialogs.</span></span> <span data-ttu-id="35e54-142">Sie gilt auch für den HTTP-Header Accept-Languages, der von WebView an Websites gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="35e54-142">It also applies to the accept-languages HTTP header that WebView sends to web sites.</span></span> <span data-ttu-id="35e54-143">Das Format von `language[-country]` Where `language` ist der 2-Buchstaben-Code von ISO 639 und `country` der 2-Buchstaben-Code von ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="35e54-143">It is in the format of `language[-country]` where `language` is the 2 letter code from ISO 639 and `country` is the 2 letter code from ISO 3166.</span></span>

#### <span data-ttu-id="35e54-144">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="35e54-144">get_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="35e54-145">Die Version der Edge-WebView2-Runtime-Binärdateien, die für die Kompatibilität mit der aufrufenden Anwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="35e54-145">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>

> <span data-ttu-id="35e54-146">Public HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="35e54-146">public HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \* value)</span></span>

<span data-ttu-id="35e54-147">Dies ist standardmäßig die Edge WebView2-Laufzeitversion, die der Version des SDK entspricht, das die Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="35e54-147">This defaults to the Edge WebView2 Runtime version that corresponds with the version of the SDK the application is using.</span></span> <span data-ttu-id="35e54-148">Das Format dieses Werts entspricht dem Format der BrowserVersionString-Eigenschaft und anderen Browserversion-Werten.</span><span class="sxs-lookup"><span data-stu-id="35e54-148">The format of this value is the same as the format of the BrowserVersionString property and other BrowserVersion values.</span></span> <span data-ttu-id="35e54-149">Nur der Versions Teil des Browserversion-Werts wird berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="35e54-149">Only the version part of the BrowserVersion value is respected.</span></span> <span data-ttu-id="35e54-150">Wenn es vorhanden ist, wird das Kanal Suffix ignoriert.</span><span class="sxs-lookup"><span data-stu-id="35e54-150">The channel suffix, if it exists, is ignored.</span></span> <span data-ttu-id="35e54-151">Die Version der tatsächlich verwendeten Edge-WebView2-Runtime-Binärdateien kann sich vom angegebenen TargetCompatibleBrowserVersion unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="35e54-151">The version of the Edge WebView2 Runtime binaries actually used may be different from the specified TargetCompatibleBrowserVersion.</span></span> <span data-ttu-id="35e54-152">Sie sind nur garantiert kompatibel.</span><span class="sxs-lookup"><span data-stu-id="35e54-152">They are only guaranteed to be compatible.</span></span> <span data-ttu-id="35e54-153">Sie können die aktuelle Version auf der BrowserVersionString-Eigenschaft auf der ICoreWebView2Environment-Eigenschaft überprüfen.</span><span class="sxs-lookup"><span data-stu-id="35e54-153">You can check the actual version on the BrowserVersionString property on the ICoreWebView2Environment.</span></span>

#### <span data-ttu-id="35e54-154">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="35e54-154">put_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="35e54-155">Festlegen der AdditionalBrowserArguments-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="35e54-155">Set the AdditionalBrowserArguments property.</span></span>

> <span data-ttu-id="35e54-156">Public HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(LPCWSTR-Wert)</span><span class="sxs-lookup"><span data-stu-id="35e54-156">public HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(LPCWSTR value)</span></span>

#### <span data-ttu-id="35e54-157">put_Language</span><span class="sxs-lookup"><span data-stu-id="35e54-157">put_Language</span></span> 

<span data-ttu-id="35e54-158">Festlegen der Language-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="35e54-158">Set the Language property.</span></span>

> <span data-ttu-id="35e54-159">Public HRESULT [put_Language](#put_language)(LPCWSTR-Wert)</span><span class="sxs-lookup"><span data-stu-id="35e54-159">public HRESULT [put_Language](#put_language)(LPCWSTR value)</span></span>

#### <span data-ttu-id="35e54-160">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="35e54-160">put_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="35e54-161">Setzen Sie die TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="35e54-161">Set the TargetCompatibleBrowserVersion.</span></span>

> <span data-ttu-id="35e54-162">Public HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(LPCWSTR-Wert)</span><span class="sxs-lookup"><span data-stu-id="35e54-162">public HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(LPCWSTR value)</span></span>

