---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2EnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2EnvironmentOptions
ms.openlocfilehash: a4e51dc08e2c31664cb77e4e6ee0136bab2f261d
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012177"
---
# <span data-ttu-id="b717a-104">Schnittstellen ICoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="b717a-104">interface ICoreWebView2EnvironmentOptions</span></span> 

```
interface ICoreWebView2EnvironmentOptions
  : public IUnknown
```

<span data-ttu-id="b717a-105">Optionen zum Erstellen der WebView2-Umgebung</span><span class="sxs-lookup"><span data-stu-id="b717a-105">Options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="b717a-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b717a-106">Summary</span></span>

 <span data-ttu-id="b717a-107">Member</span><span class="sxs-lookup"><span data-stu-id="b717a-107">Members</span></span>                        | <span data-ttu-id="b717a-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b717a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b717a-109">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="b717a-109">get_AdditionalBrowserArguments</span></span>](#get_additionalbrowserarguments) | <span data-ttu-id="b717a-110">AdditionalBrowserArguments kann angegeben werden, um das Verhalten von WebView zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b717a-110">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>
[<span data-ttu-id="b717a-111">get_AllowSingleSignOnUsingOSPrimaryAccount</span><span class="sxs-lookup"><span data-stu-id="b717a-111">get_AllowSingleSignOnUsingOSPrimaryAccount</span></span>](#get_allowsinglesignonusingosprimaryaccount) | <span data-ttu-id="b717a-112">Die AllowSingleSignOnUsingOSPrimaryAccount-Eigenschaft wird verwendet, um die einmalige Anmeldung mit Azure Active Directory (AAD)-Ressourcen in WebView unter Verwendung des angemeldeten Windows-Kontos und des einmaligen Anmeldens bei Websites zu aktivieren, die das Microsoft-Konto verwenden, das mit dem Anmeldenamen im Windows-Konto verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="b717a-112">The AllowSingleSignOnUsingOSPrimaryAccount property is used to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on with web sites using Microsoft account associated with the login in Windows account.</span></span>
[<span data-ttu-id="b717a-113">get_Language</span><span class="sxs-lookup"><span data-stu-id="b717a-113">get_Language</span></span>](#get_language) | <span data-ttu-id="b717a-114">Die Standardsprache, mit der WebView ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b717a-114">The default language that WebView will run with.</span></span>
[<span data-ttu-id="b717a-115">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="b717a-115">get_TargetCompatibleBrowserVersion</span></span>](#get_targetcompatiblebrowserversion) | <span data-ttu-id="b717a-116">Die Version der Edge-WebView2-Runtime-Binärdateien, die für die Kompatibilität mit der aufrufenden Anwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b717a-116">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>
[<span data-ttu-id="b717a-117">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="b717a-117">put_AdditionalBrowserArguments</span></span>](#put_additionalbrowserarguments) | <span data-ttu-id="b717a-118">Festlegen der AdditionalBrowserArguments-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b717a-118">Set the AdditionalBrowserArguments property.</span></span>
[<span data-ttu-id="b717a-119">put_AllowSingleSignOnUsingOSPrimaryAccount</span><span class="sxs-lookup"><span data-stu-id="b717a-119">put_AllowSingleSignOnUsingOSPrimaryAccount</span></span>](#put_allowsinglesignonusingosprimaryaccount) | <span data-ttu-id="b717a-120">Festlegen der AllowSingleSignOnUsingOSPrimaryAccount-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b717a-120">Set the AllowSingleSignOnUsingOSPrimaryAccount property.</span></span>
[<span data-ttu-id="b717a-121">put_Language</span><span class="sxs-lookup"><span data-stu-id="b717a-121">put_Language</span></span>](#put_language) | <span data-ttu-id="b717a-122">Festlegen der Language-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b717a-122">Set the Language property.</span></span>
[<span data-ttu-id="b717a-123">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="b717a-123">put_TargetCompatibleBrowserVersion</span></span>](#put_targetcompatiblebrowserversion) | <span data-ttu-id="b717a-124">Festlegen der TargetCompatibleBrowserVersion-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b717a-124">Set the TargetCompatibleBrowserVersion property.</span></span>

<span data-ttu-id="b717a-125">Eine Standardimplementierung wird in WebView2EnvironmentOptions. h bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b717a-125">A default implementation is provided in WebView2EnvironmentOptions.h.</span></span>

```cpp
    auto options = Microsoft::WRL::Make<CoreWebView2EnvironmentOptions>();
    CHECK_FAILURE(options->put_AllowSingleSignOnUsingOSPrimaryAccount(
        m_AADSSOEnabled ? TRUE : FALSE));
    if (!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
```

## <span data-ttu-id="b717a-126">Member</span><span class="sxs-lookup"><span data-stu-id="b717a-126">Members</span></span>

#### <span data-ttu-id="b717a-127">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="b717a-127">get_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="b717a-128">AdditionalBrowserArguments kann angegeben werden, um das Verhalten von WebView zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b717a-128">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>

> <span data-ttu-id="b717a-129">Public HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="b717a-129">public HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \* value)</span></span>

<span data-ttu-id="b717a-130">Diese werden als Teil der Befehlszeile an den Browserprozess übergeben.</span><span class="sxs-lookup"><span data-stu-id="b717a-130">These will be passed to the browser process as part of the command line.</span></span> <span data-ttu-id="b717a-131">Weitere Informationen zu Befehlszeilen wechseln in den Browserprozess finden Sie unter [Ausführen von Chrom mit Flags](https://aka.ms/RunChromiumWithFlags) .</span><span class="sxs-lookup"><span data-stu-id="b717a-131">See [Run Chromium with Flags](https://aka.ms/RunChromiumWithFlags) for more information about command line switches to browser process.</span></span> <span data-ttu-id="b717a-132">Wenn die APP mit einem Befehlszeilen Schalter gestartet wird, `--edge-webview-switches=xxx` wird der Wert dieses Schalters (xxx im obigen Beispiel) auch an die Befehlszeile des Browser Prozesses angefügt.</span><span class="sxs-lookup"><span data-stu-id="b717a-132">If the app is launched with a command line switch `--edge-webview-switches=xxx` the value of that switch (xxx in the above example) will also be appended to the browser process command line.</span></span> <span data-ttu-id="b717a-133">Bestimmte Schalter wie `--user-data-dir` sind intern und wichtig für WebView.</span><span class="sxs-lookup"><span data-stu-id="b717a-133">Certain switches like `--user-data-dir` are internal and important to WebView.</span></span> <span data-ttu-id="b717a-134">Diese Schalter werden ignoriert, auch wenn Sie angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b717a-134">Those switches will be ignored even if specified.</span></span> <span data-ttu-id="b717a-135">Wenn dieselben Schalter mehrmals angegeben werden, gewinnt der letzte.</span><span class="sxs-lookup"><span data-stu-id="b717a-135">If the same switches are specified multiple times, the last one wins.</span></span> <span data-ttu-id="b717a-136">Es wird nicht versucht, die verschiedenen Werte desselben Schalters zusammenzuführen, mit Ausnahme von deaktivierten und aktivierten Features.</span><span class="sxs-lookup"><span data-stu-id="b717a-136">There is no attempt to merge the different values of the same switch, except for disabled and enabled features.</span></span> <span data-ttu-id="b717a-137">Die Features, die von `--enable-features` und `--disable-features` mit einfacher Logik zusammengeführt werden: die Features sind die Vereinigung der angegebenen Features und integrierten Features, und wenn ein Feature deaktiviert ist, wird es aus der Liste der aktivierten Features entfernt.</span><span class="sxs-lookup"><span data-stu-id="b717a-137">The features specified by `--enable-features` and `--disable-features` will be merged with simple logic: the features will be the union of the specified features and built-in features, and if a feature is disabled, it will be removed from the enabled features list.</span></span> <span data-ttu-id="b717a-138">Der Befehlszeilenwert des App-Prozesses `--edge-webview-switches` wird verarbeitet, nachdem der additionalBrowserArguments-Parameter verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="b717a-138">App process's command line `--edge-webview-switches` value are processed after the additionalBrowserArguments parameter is processed.</span></span> <span data-ttu-id="b717a-139">Bestimmte Features sind intern deaktiviert und können nicht aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="b717a-139">Certain features are disabled internally and can't be enabled.</span></span> <span data-ttu-id="b717a-140">Wenn die Analyse bei den angegebenen Schaltern fehlgeschlagen ist, werden Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b717a-140">If parsing failed for the specified switches, they will be ignored.</span></span> <span data-ttu-id="b717a-141">Standardmäßig wird der Browserprozess ohne zusätzliche Flags ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b717a-141">Default is to run browser process with no extra flags.</span></span>

#### <span data-ttu-id="b717a-142">get_AllowSingleSignOnUsingOSPrimaryAccount</span><span class="sxs-lookup"><span data-stu-id="b717a-142">get_AllowSingleSignOnUsingOSPrimaryAccount</span></span> 

<span data-ttu-id="b717a-143">Die AllowSingleSignOnUsingOSPrimaryAccount-Eigenschaft wird verwendet, um die einmalige Anmeldung mit Azure Active Directory (AAD)-Ressourcen in WebView unter Verwendung des angemeldeten Windows-Kontos und des einmaligen Anmeldens bei Websites zu aktivieren, die das Microsoft-Konto verwenden, das mit dem Anmeldenamen im Windows-Konto verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="b717a-143">The AllowSingleSignOnUsingOSPrimaryAccount property is used to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on with web sites using Microsoft account associated with the login in Windows account.</span></span>

> <span data-ttu-id="b717a-144">öffentliche HRESULT- [get_AllowSingleSignOnUsingOSPrimaryAccount](#get_allowsinglesignonusingosprimaryaccount)(bool \* Allow)</span><span class="sxs-lookup"><span data-stu-id="b717a-144">public HRESULT [get_AllowSingleSignOnUsingOSPrimaryAccount](#get_allowsinglesignonusingosprimaryaccount)(BOOL \* allow)</span></span>

<span data-ttu-id="b717a-145">Standard ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b717a-145">Default is disabled.</span></span> <span data-ttu-id="b717a-146">Universelle Windows-Plattform-apps müssen auch die [Eingeschränkte](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) enterpriseCloudSSO-Funktion für das einmalige Anmelden deklarieren.</span><span class="sxs-lookup"><span data-stu-id="b717a-146">Universal Windows Platform apps must also declare enterpriseCloudSSO [restricted capability](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) for the single sign on to work.</span></span>

#### <span data-ttu-id="b717a-147">get_Language</span><span class="sxs-lookup"><span data-stu-id="b717a-147">get_Language</span></span> 

<span data-ttu-id="b717a-148">Die Standardsprache, mit der WebView ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b717a-148">The default language that WebView will run with.</span></span>

> <span data-ttu-id="b717a-149">Public HRESULT [get_Language](#get_language)(LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="b717a-149">public HRESULT [get_Language](#get_language)(LPWSTR \* value)</span></span>

<span data-ttu-id="b717a-150">Sie bezieht sich auf Browser-UIs wie Kontextmenüs und Dialogfelder.</span><span class="sxs-lookup"><span data-stu-id="b717a-150">It applies to browser UIs like context menu and dialogs.</span></span> <span data-ttu-id="b717a-151">Sie gilt auch für den HTTP-Header Accept-Languages, der von WebView an Websites gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="b717a-151">It also applies to the accept-languages HTTP header that WebView sends to web sites.</span></span> <span data-ttu-id="b717a-152">Das Format von `language[-country]` Where `language` ist der 2-Buchstaben-Code von ISO 639 und `country` der 2-Buchstaben-Code von ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="b717a-152">It is in the format of `language[-country]` where `language` is the 2 letter code from ISO 639 and `country` is the 2 letter code from ISO 3166.</span></span>

#### <span data-ttu-id="b717a-153">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="b717a-153">get_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="b717a-154">Die Version der Edge-WebView2-Runtime-Binärdateien, die für die Kompatibilität mit der aufrufenden Anwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b717a-154">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>

> <span data-ttu-id="b717a-155">Public HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="b717a-155">public HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \* value)</span></span>

<span data-ttu-id="b717a-156">Dies ist standardmäßig die Edge WebView2-Laufzeitversion, die der Version des SDK entspricht, das die Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b717a-156">This defaults to the Edge WebView2 Runtime version that corresponds with the version of the SDK the application is using.</span></span> <span data-ttu-id="b717a-157">Das Format dieses Werts entspricht dem Format der BrowserVersionString-Eigenschaft und anderen Browserversion-Werten.</span><span class="sxs-lookup"><span data-stu-id="b717a-157">The format of this value is the same as the format of the BrowserVersionString property and other BrowserVersion values.</span></span> <span data-ttu-id="b717a-158">Nur der Versions Teil des Browserversion-Werts wird berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="b717a-158">Only the version part of the BrowserVersion value is respected.</span></span> <span data-ttu-id="b717a-159">Wenn es vorhanden ist, wird das Kanal Suffix ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b717a-159">The channel suffix, if it exists, is ignored.</span></span> <span data-ttu-id="b717a-160">Die Version der tatsächlich verwendeten Edge-WebView2-Runtime-Binärdateien kann sich vom angegebenen TargetCompatibleBrowserVersion unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="b717a-160">The version of the Edge WebView2 Runtime binaries actually used may be different from the specified TargetCompatibleBrowserVersion.</span></span> <span data-ttu-id="b717a-161">Sie sind nur garantiert kompatibel.</span><span class="sxs-lookup"><span data-stu-id="b717a-161">They are only guaranteed to be compatible.</span></span> <span data-ttu-id="b717a-162">Sie können die aktuelle Version auf der BrowserVersionString-Eigenschaft auf der ICoreWebView2Environment-Eigenschaft überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b717a-162">You can check the actual version on the BrowserVersionString property on the ICoreWebView2Environment.</span></span>

#### <span data-ttu-id="b717a-163">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="b717a-163">put_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="b717a-164">Festlegen der AdditionalBrowserArguments-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b717a-164">Set the AdditionalBrowserArguments property.</span></span>

> <span data-ttu-id="b717a-165">Public HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(LPCWSTR-Wert)</span><span class="sxs-lookup"><span data-stu-id="b717a-165">public HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(LPCWSTR value)</span></span>

#### <span data-ttu-id="b717a-166">put_AllowSingleSignOnUsingOSPrimaryAccount</span><span class="sxs-lookup"><span data-stu-id="b717a-166">put_AllowSingleSignOnUsingOSPrimaryAccount</span></span> 

<span data-ttu-id="b717a-167">Festlegen der AllowSingleSignOnUsingOSPrimaryAccount-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b717a-167">Set the AllowSingleSignOnUsingOSPrimaryAccount property.</span></span>

> <span data-ttu-id="b717a-168">öffentliche HRESULT- [put_AllowSingleSignOnUsingOSPrimaryAccount](#put_allowsinglesignonusingosprimaryaccount)(bool Allow)</span><span class="sxs-lookup"><span data-stu-id="b717a-168">public HRESULT [put_AllowSingleSignOnUsingOSPrimaryAccount](#put_allowsinglesignonusingosprimaryaccount)(BOOL allow)</span></span>

#### <span data-ttu-id="b717a-169">put_Language</span><span class="sxs-lookup"><span data-stu-id="b717a-169">put_Language</span></span> 

<span data-ttu-id="b717a-170">Festlegen der Language-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b717a-170">Set the Language property.</span></span>

> <span data-ttu-id="b717a-171">Public HRESULT [put_Language](#put_language)(LPCWSTR-Wert)</span><span class="sxs-lookup"><span data-stu-id="b717a-171">public HRESULT [put_Language](#put_language)(LPCWSTR value)</span></span>

#### <span data-ttu-id="b717a-172">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="b717a-172">put_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="b717a-173">Festlegen der TargetCompatibleBrowserVersion-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b717a-173">Set the TargetCompatibleBrowserVersion property.</span></span>

> <span data-ttu-id="b717a-174">Public HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(LPCWSTR-Wert)</span><span class="sxs-lookup"><span data-stu-id="b717a-174">public HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(LPCWSTR value)</span></span>

