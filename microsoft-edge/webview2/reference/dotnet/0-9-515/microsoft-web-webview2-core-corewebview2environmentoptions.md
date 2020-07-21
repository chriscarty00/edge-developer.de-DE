---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 8378c6388f0bc7cda26ef4a34b8ef5e8d5c95f4d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885044"
---
# <span data-ttu-id="07f55-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions Klasse</span><span class="sxs-lookup"><span data-stu-id="07f55-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2EnvironmentOptions class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="07f55-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="07f55-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="07f55-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="07f55-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="07f55-107">Optionen zum Erstellen der WebView2-Umgebung</span><span class="sxs-lookup"><span data-stu-id="07f55-107">Options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="07f55-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="07f55-108">Summary</span></span>

 <span data-ttu-id="07f55-109">Member</span><span class="sxs-lookup"><span data-stu-id="07f55-109">Members</span></span>                        | <span data-ttu-id="07f55-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="07f55-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="07f55-111">AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="07f55-111">AdditionalBrowserArguments</span></span>](#additionalbrowserarguments) | <span data-ttu-id="07f55-112">AdditionalBrowserArguments kann angegeben werden, um das Verhalten von WebView zu ändern.</span><span class="sxs-lookup"><span data-stu-id="07f55-112">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>
[<span data-ttu-id="07f55-113">Sprache</span><span class="sxs-lookup"><span data-stu-id="07f55-113">Language</span></span>](#language) | <span data-ttu-id="07f55-114">Die Standardsprache, mit der WebView ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07f55-114">The default language that WebView will run with.</span></span>
[<span data-ttu-id="07f55-115">TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="07f55-115">TargetCompatibleBrowserVersion</span></span>](#targetcompatiblebrowserversion) | <span data-ttu-id="07f55-116">Die Version der Edge-WebView2-Runtime-Binärdateien, die für die Kompatibilität mit der aufrufenden Anwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="07f55-116">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>
[<span data-ttu-id="07f55-117">CoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="07f55-117">CoreWebView2EnvironmentOptions</span></span>](#corewebview2environmentoptions) | <span data-ttu-id="07f55-118">Initialisiert eine neue Instanz der CoreWebView2EnvironmentOptions-Klasse.</span><span class="sxs-lookup"><span data-stu-id="07f55-118">Initializes a new instance of the CoreWebView2EnvironmentOptions class.</span></span>

<span data-ttu-id="07f55-119">Eine Standardimplementierung wird in WebView2EnvironmentOptions. h bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="07f55-119">A default implementation is provided in WebView2EnvironmentOptions.h.</span></span>

## <span data-ttu-id="07f55-120">Member</span><span class="sxs-lookup"><span data-stu-id="07f55-120">Members</span></span>

#### <span data-ttu-id="07f55-121">AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="07f55-121">AdditionalBrowserArguments</span></span> 

<span data-ttu-id="07f55-122">AdditionalBrowserArguments kann angegeben werden, um das Verhalten von WebView zu ändern.</span><span class="sxs-lookup"><span data-stu-id="07f55-122">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>

> <span data-ttu-id="07f55-123">public String [AdditionalBrowserArguments](#additionalbrowserarguments)</span><span class="sxs-lookup"><span data-stu-id="07f55-123">public string [AdditionalBrowserArguments](#additionalbrowserarguments)</span></span>

<span data-ttu-id="07f55-124">Diese werden als Teil der Befehlszeile an den Browserprozess übergeben.</span><span class="sxs-lookup"><span data-stu-id="07f55-124">These will be passed to the browser process as part of the command line.</span></span> <span data-ttu-id="07f55-125">Weitere Informationen zu Befehlszeilen wechseln in den Browserprozess finden Sie unter [Ausführen von Chrom mit Flags](https://aka.ms/RunChromiumWithFlags) .</span><span class="sxs-lookup"><span data-stu-id="07f55-125">See [Run Chromium with Flags](https://aka.ms/RunChromiumWithFlags) for more information about command line switches to browser process.</span></span> <span data-ttu-id="07f55-126">Wenn die APP mit einem Befehlszeilen Schalter gestartet wird, `--edge-webview-switches=xxx` wird der Wert dieses Schalters (xxx im obigen Beispiel) auch an die Befehlszeile des Browser Prozesses angefügt.</span><span class="sxs-lookup"><span data-stu-id="07f55-126">If the app is launched with a command line switch `--edge-webview-switches=xxx` the value of that switch (xxx in the above example) will also be appended to the browser process command line.</span></span> <span data-ttu-id="07f55-127">Bestimmte Schalter wie `--user-data-dir` sind intern und wichtig für WebView.</span><span class="sxs-lookup"><span data-stu-id="07f55-127">Certain switches like `--user-data-dir` are internal and important to WebView.</span></span> <span data-ttu-id="07f55-128">Diese Schalter werden ignoriert, auch wenn Sie angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="07f55-128">Those switches will be ignored even if specified.</span></span> <span data-ttu-id="07f55-129">Wenn dieselben Schalter mehrmals angegeben werden, gewinnt der letzte.</span><span class="sxs-lookup"><span data-stu-id="07f55-129">If the same switches are specified multiple times, the last one wins.</span></span> <span data-ttu-id="07f55-130">Es wird nicht versucht, die verschiedenen Werte desselben Schalters zusammenzuführen, mit Ausnahme von deaktivierten und aktivierten Features.</span><span class="sxs-lookup"><span data-stu-id="07f55-130">There is no attempt to merge the different values of the same switch, except for disabled and enabled features.</span></span> <span data-ttu-id="07f55-131">Die Features, die von `--enable-features` und `--disable-features` mit einfacher Logik zusammengeführt werden: die Features sind die Vereinigung der angegebenen Features und integrierten Features, und wenn ein Feature deaktiviert ist, wird es aus der Liste der aktivierten Features entfernt.</span><span class="sxs-lookup"><span data-stu-id="07f55-131">The features specified by `--enable-features` and `--disable-features` will be merged with simple logic: the features will be the union of the specified features and built-in features, and if a feature is disabled, it will be removed from the enabled features list.</span></span> <span data-ttu-id="07f55-132">Der Befehlszeilenwert des App-Prozesses `--edge-webview-switches` wird verarbeitet, nachdem der additionalBrowserArguments-Parameter verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="07f55-132">App process's command line `--edge-webview-switches` value are processed after the additionalBrowserArguments parameter is processed.</span></span> <span data-ttu-id="07f55-133">Bestimmte Features sind intern deaktiviert und können nicht aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="07f55-133">Certain features are disabled internally and can't be enabled.</span></span> <span data-ttu-id="07f55-134">Wenn die Analyse bei den angegebenen Schaltern fehlgeschlagen ist, werden Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="07f55-134">If parsing failed for the specified switches, they will be ignored.</span></span> <span data-ttu-id="07f55-135">Standardmäßig wird der Browserprozess ohne zusätzliche Flags ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07f55-135">Default is to run browser process with no extra flags.</span></span>

#### <span data-ttu-id="07f55-136">Sprache</span><span class="sxs-lookup"><span data-stu-id="07f55-136">Language</span></span> 

<span data-ttu-id="07f55-137">Die Standardsprache, mit der WebView ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07f55-137">The default language that WebView will run with.</span></span>

> <span data-ttu-id="07f55-138">öffentliche Zeichenfolgen [Sprache](#language)</span><span class="sxs-lookup"><span data-stu-id="07f55-138">public string [Language](#language)</span></span>

<span data-ttu-id="07f55-139">Sie bezieht sich auf Browser-UIs wie Kontextmenüs und Dialogfelder.</span><span class="sxs-lookup"><span data-stu-id="07f55-139">It applies to browser UIs like context menu and dialogs.</span></span> <span data-ttu-id="07f55-140">Sie gilt auch für den HTTP-Header Accept-Languages, der von WebView an Websites gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="07f55-140">It also applies to the accept-languages HTTP header that WebView sends to web sites.</span></span> <span data-ttu-id="07f55-141">Das Format von `language[-country]` Where `language` ist der 2-Buchstaben-Code von ISO 639 und `country` der 2-Buchstaben-Code von ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="07f55-141">It is in the format of `language[-country]` where `language` is the 2 letter code from ISO 639 and `country` is the 2 letter code from ISO 3166.</span></span>

#### <span data-ttu-id="07f55-142">TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="07f55-142">TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="07f55-143">Die Version der Edge-WebView2-Runtime-Binärdateien, die für die Kompatibilität mit der aufrufenden Anwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="07f55-143">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>

> <span data-ttu-id="07f55-144">public String [TargetCompatibleBrowserVersion](#targetcompatiblebrowserversion)</span><span class="sxs-lookup"><span data-stu-id="07f55-144">public string [TargetCompatibleBrowserVersion](#targetcompatiblebrowserversion)</span></span>

<span data-ttu-id="07f55-145">Dies ist standardmäßig die Edge WebView2-Laufzeitversion, die der Version des SDK entspricht, das die Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="07f55-145">This defaults to the Edge WebView2 Runtime version that corresponds with the version of the SDK the application is using.</span></span> <span data-ttu-id="07f55-146">Das Format dieses Werts entspricht dem Format der BrowserVersionString-Eigenschaft und anderen Browserversion-Werten.</span><span class="sxs-lookup"><span data-stu-id="07f55-146">The format of this value is the same as the format of the BrowserVersionString property and other BrowserVersion values.</span></span> <span data-ttu-id="07f55-147">Nur der Versions Teil des Browserversion-Werts wird berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="07f55-147">Only the version part of the BrowserVersion value is respected.</span></span> <span data-ttu-id="07f55-148">Wenn es vorhanden ist, wird das Kanal Suffix ignoriert.</span><span class="sxs-lookup"><span data-stu-id="07f55-148">The channel suffix, if it exists, is ignored.</span></span> <span data-ttu-id="07f55-149">Die Version der tatsächlich verwendeten Edge-WebView2-Runtime-Binärdateien kann sich vom angegebenen TargetCompatibleBrowserVersion unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="07f55-149">The version of the Edge WebView2 Runtime binaries actually used may be different from the specified TargetCompatibleBrowserVersion.</span></span> <span data-ttu-id="07f55-150">Sie sind nur garantiert kompatibel.</span><span class="sxs-lookup"><span data-stu-id="07f55-150">They are only guaranteed to be compatible.</span></span> <span data-ttu-id="07f55-151">Sie können die aktuelle Version auf der BrowserVersionString-Eigenschaft auf der CoreWebView2Environment-Eigenschaft überprüfen.</span><span class="sxs-lookup"><span data-stu-id="07f55-151">You can check the actual version on the BrowserVersionString property on the CoreWebView2Environment.</span></span>

#### <span data-ttu-id="07f55-152">CoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="07f55-152">CoreWebView2EnvironmentOptions</span></span> 

<span data-ttu-id="07f55-153">Initialisiert eine neue Instanz der CoreWebView2EnvironmentOptions-Klasse.</span><span class="sxs-lookup"><span data-stu-id="07f55-153">Initializes a new instance of the CoreWebView2EnvironmentOptions class.</span></span>

> <span data-ttu-id="07f55-154">Public [CoreWebView2EnvironmentOptions](#corewebview2environmentoptions)(String additionalBrowserArguments, String Language, String targetCompatibleBrowserVersion)</span><span class="sxs-lookup"><span data-stu-id="07f55-154">public  [CoreWebView2EnvironmentOptions](#corewebview2environmentoptions)(string additionalBrowserArguments, string language, string targetCompatibleBrowserVersion)</span></span>

##### <span data-ttu-id="07f55-155">Parameter</span><span class="sxs-lookup"><span data-stu-id="07f55-155">Parameters</span></span>
* `additionalBrowserArguments` <span data-ttu-id="07f55-156">AdditionalBrowserArguments kann angegeben werden, um das Verhalten von WebView zu ändern.</span><span class="sxs-lookup"><span data-stu-id="07f55-156">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span> 

* `language` <span data-ttu-id="07f55-157">Die Standardsprache, mit der WebView ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07f55-157">The default language that WebView will run with.</span></span> 

* `targetCompatibleBrowserVersion` <span data-ttu-id="07f55-158">Die Version der Edge-WebView2-Runtime-Binärdateien, die für die Kompatibilität mit der aufrufenden Anwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="07f55-158">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>

