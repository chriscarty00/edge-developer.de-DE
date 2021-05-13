---
description: Beginnen Sie mit Remote debugging WebViews in Ihren systemeigenen Android-Apps mithilfe Microsoft Edge Entwicklertools.
title: Erste Schritte mit Remotedebugging von Android-WebViews
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 75d948465c62c63c9ccbe0fcd46616819a04e79d
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565078"
---
<!-- Copyright Meggin Kearney 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="get-started-with-remote-debugging-android-webviews"></a><span data-ttu-id="675e3-104">Erste Schritte mit Remotedebugging von Android-WebViews</span><span class="sxs-lookup"><span data-stu-id="675e3-104">Get started with remote debugging Android WebViews</span></span>  

<span data-ttu-id="675e3-105">Debuggen Sie Android WebViews in Ihren nativen Android-Apps mit Microsoft Edge Entwicklertools.</span><span class="sxs-lookup"><span data-stu-id="675e3-105">Debug Android WebViews in your native Android apps using Microsoft Edge Developer Tools.</span></span>  

<span data-ttu-id="675e3-106">Verwenden Sie devTools unter Android 4.4 \(KitKat\) oder höher, um WebView-Inhalte in systemeigenen Android-Apps zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="675e3-106">On Android 4.4 \(KitKat\) or later, use DevTools to debug WebView content in native Android apps.</span></span>  

### <a name="summary"></a><span data-ttu-id="675e3-107">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="675e3-107">Summary</span></span>  

*   <span data-ttu-id="675e3-108">Aktivieren des Android WebView-Debuggings in Ihrer nativen #A0 Debuggen von Android WebViews in Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="675e3-108">Turn on Android WebView debugging in your native Android app; debug Android WebViews in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="675e3-109">Navigieren Sie zu, um die Liste der Android WebViews mit aktivierten Debuggen anzeigen zu `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="675e3-109">To display the list of the Android WebViews with debugging turned on, navigate to `edge://inspect`.</span></span>  
*   <span data-ttu-id="675e3-110">Debuggen Sie Android WebViews auf die gleiche Weise, wie Sie eine Webseite durch [Remotedebuggern debuggen.][RemoteDebuggingGettingStarted]</span><span class="sxs-lookup"><span data-stu-id="675e3-110">Debug Android WebViews in the same way you debug a webpage through [remote debugging][RemoteDebuggingGettingStarted].</span></span>  

## <a name="configure-android-webviews-to-debug"></a><span data-ttu-id="675e3-111">Konfigurieren von Android WebViews zum Debuggen</span><span class="sxs-lookup"><span data-stu-id="675e3-111">Configure Android WebViews to debug</span></span>  

<span data-ttu-id="675e3-112">Das Debuggen von Android WebView muss in Ihrer App aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="675e3-112">Android WebView debugging must be turned on within your app.</span></span>  <span data-ttu-id="675e3-113">Führen Sie zum Aktivieren des Android WebView-Debuggings die [statische Methode setWebContentsDebuggingEnabled][AndroidDeveloperWebViewsSetWebContentsDebuggingEnabled] für die Klasse `WebView` aus.</span><span class="sxs-lookup"><span data-stu-id="675e3-113">To turn on Android WebView debugging, run the [setWebContentsDebuggingEnabled][AndroidDeveloperWebViewsSetWebContentsDebuggingEnabled] static method on the `WebView` class.</span></span>  

```java
if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.KITKAT) {
    WebView.setWebContentsDebuggingEnabled(true);
}
```  

<span data-ttu-id="675e3-114">Die Einstellung gilt für alle Android WebViews der App.</span><span class="sxs-lookup"><span data-stu-id="675e3-114">The setting applies to all of the Android WebViews of the app.</span></span>  

> [!TIP]
> <span data-ttu-id="675e3-115">Das Debuggen von Android WebView wird vom Zustand des Flags im Manifest der `debuggable` App nicht beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="675e3-115">Android WebView debugging is not affected by the state of the `debuggable` flag in the manifest of the app.</span></span>  <span data-ttu-id="675e3-116">Wenn Sie das Android WebView-Debuggen nur aktivieren möchten, wenn das Flag `debuggable` `true` ist, testen Sie das Flag zur Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="675e3-116">If you want to turn on Android WebView debugging only when the `debuggable` flag is `true`, test the flag at runtime.</span></span>  
> 
> ```java
> if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.KITKAT) {
>     if (0 != (getApplicationInfo().flags & ApplicationInfo.FLAG_DEBUGGABLE))
>    { WebView.setWebContentsDebuggingEnabled(true); }
> }
> ```  

## <a name="open-an-android-webview-in-devtools"></a><span data-ttu-id="675e3-117">Öffnen eines Android WebView in DevTools</span><span class="sxs-lookup"><span data-stu-id="675e3-117">Open an Android WebView in DevTools</span></span>  

<span data-ttu-id="675e3-118">Navigieren Sie zu, um eine Liste der Android WebViews mit aktivierten Debuggen zu zeigen, die auf Ihrem Gerät ausgeführt `edge://inspect` werden.</span><span class="sxs-lookup"><span data-stu-id="675e3-118">To display a list of the Android WebViews with debugging turned on that run on your device, navigate to `edge://inspect`.</span></span>  

<span data-ttu-id="675e3-119">Zum Starten des Debuggens wählen Sie unter Android WebView, das Sie debuggen möchten, **inspect aus.**</span><span class="sxs-lookup"><span data-stu-id="675e3-119">To start debugging, under the Android WebView you want to debug, choose **inspect**.</span></span>  <span data-ttu-id="675e3-120">Verwenden Sie DevTools auf die gleiche Weise wie eine Remotebrowserregisterkarte.</span><span class="sxs-lookup"><span data-stu-id="675e3-120">Use DevTools in the same way that you do a remote browser tab.</span></span>  

<!--
:::image type="complex" source=".images/webview-debugging.msft.png" alt-text="Inspecting elements in an Android WebView" lightbox=".images/webview-debugging.msft.png":::
   Inspecting elements in an Android WebView  
:::image-end:::  

The gray graphics listed with the Android WebView represent its size and position relative to the screen of the device.  If your Android WebViews have titles set, the titles are listed as well.  
-->  

## <a name="troubleshoot"></a><span data-ttu-id="675e3-121">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="675e3-121">Troubleshoot</span></span>  

<span data-ttu-id="675e3-122">Ihre Android WebViews werden nicht auf der Seite `edge://inspect` angezeigt?</span><span class="sxs-lookup"><span data-stu-id="675e3-122">Your Android WebViews aren't displayed on the `edge://inspect` page?</span></span>  

*   <span data-ttu-id="675e3-123">Stellen Sie sicher, dass das Android WebView-Debuggen für Ihre App aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="675e3-123">Verify that Android WebView debugging is turned on for your app.</span></span>  
*   <span data-ttu-id="675e3-124">Öffnen Sie auf Ihrem Gerät die App mit der Android WebView, die Sie debuggen möchten.</span><span class="sxs-lookup"><span data-stu-id="675e3-124">On your device, open the app with the Android WebView you want to debug.</span></span>  <span data-ttu-id="675e3-125">Aktualisieren Sie dann `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="675e3-125">Then, refresh `edge://inspect`.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="675e3-126">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="675e3-126">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Erste Schritte remote debugging android devices | Microsoft Docs"  

[AndroidDeveloperWebViewsSetWebContentsDebuggingEnabled]: https://developer.android.com/reference/android/webkit/WebView.html#setWebContentsDebuggingEnabled(boolean) "setWebContentsDebuggingEnabled – WebView | Android-Entwickler"  

> [!NOTE]
> <span data-ttu-id="675e3-129">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="675e3-129">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="675e3-130">Die ursprüngliche Seite befindet sich [hier und](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/webviews) wird von [Meggin Kearney][MegginKearney] \(Tech Writer\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="675e3-130">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/webviews) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="675e3-132">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="675e3-132">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: http://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
