---
description: Beginnen Sie mit Remote debugging WebViews in Ihren systemeigenen Android-Apps mithilfe Microsoft Edge Entwicklertools.
title: Erste Schritte mit Remotedebugging von Android-WebViews
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/25/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 4d389473673791d91c38e252c919378c4725db6b
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461522"
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
# <a name="get-started-with-remote-debugging-android-webviews"></a>Erste Schritte mit Remotedebugging von Android-WebViews  

Debuggen Sie Android WebViews in Ihren nativen Android-Apps mit Microsoft Edge Entwicklertools.  

Verwenden Sie devTools unter Android 4.4 \(KitKat\) oder höher, um WebView-Inhalte in systemeigenen Android-Apps zu debuggen.  

### <a name="summary"></a>Zusammenfassung  

*   Aktivieren des Android WebView-Debuggings in Ihrer nativen #A0 Debuggen von Android WebViews in Microsoft Edge DevTools.  
*   Navigieren Sie zu, um die Liste der Android WebViews mit aktivierten Debuggen anzeigen zu `edge://inspect` .  
*   Debuggen Sie Android WebViews auf die gleiche Weise, wie Sie eine Webseite durch [Remotedebuggern debuggen.][RemoteDebuggingGettingStarted]  

## <a name="configure-android-webviews-to-debug"></a>Konfigurieren von Android WebViews zum Debuggen  

Das Debuggen von Android WebView muss in Ihrer App aktiviert sein.  Führen Sie zum Aktivieren des Android WebView-Debuggings die [statische Methode setWebContentsDebuggingEnabled][AndroidDeveloperWebViewsSetWebContentsDebuggingEnabled] für die Klasse `WebView` aus.  

```java
if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.KITKAT) {
    WebView.setWebContentsDebuggingEnabled(true);
}
```  

Die Einstellung gilt für alle Android WebViews der App.  

> [!TIP]
> Das Debuggen von Android WebView wird vom Zustand des Flags im Manifest der `debuggable` App nicht beeinflusst.  Wenn Sie das Android WebView-Debuggen nur aktivieren möchten, wenn das Flag `debuggable` `true` ist, testen Sie das Flag zur Laufzeit.  
> 
> ```java
> if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.KITKAT) {
>     if (0 != (getApplicationInfo().flags & ApplicationInfo.FLAG_DEBUGGABLE))
>    { WebView.setWebContentsDebuggingEnabled(true); }
> }
> ```  

## <a name="open-an-android-webview-in-devtools"></a>Öffnen eines Android WebView in DevTools  

Navigieren Sie zu, um eine Liste der Android WebViews mit aktivierten Debuggen zu zeigen, die auf Ihrem Gerät ausgeführt `edge://inspect` werden.  

Zum Starten des Debuggens wählen Sie unter Android WebView, das Sie debuggen möchten, **inspect aus.**  Verwenden Sie DevTools auf die gleiche Weise wie eine Remotebrowserregisterkarte.  

<!--
:::image type="complex" source=".images/webview-debugging.msft.png" alt-text="Inspecting elements in an Android WebView" lightbox=".images/webview-debugging.msft.png":::
   Inspecting elements in an Android WebView  
:::image-end:::  

The gray graphics listed with the Android WebView represent its size and position relative to the screen of the device.  If your Android WebViews have titles set, the titles are listed as well.  
-->  

## <a name="troubleshoot"></a>Problembehandlung  

Ihre Android WebViews werden nicht auf der Seite `edge://inspect` angezeigt?  

*   Stellen Sie sicher, dass das Android WebView-Debuggen für Ihre App aktiviert ist.  
*   Öffnen Sie auf Ihrem Gerät die App mit der Android WebView, die Sie debuggen möchten.  Aktualisieren Sie dann `edge://inspect` .  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Erste Schritte remote debugging android devices | Microsoft Docs"  

[AndroidDeveloperWebViewsSetWebContentsDebuggingEnabled]: https://developer.android.com/reference/android/webkit/WebView.html#setWebContentsDebuggingEnabled(boolean) "setWebContentsDebuggingEnabled – WebView | Android-Entwickler"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier und](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/webviews) wird von [Meggin Kearney][MegginKearney] \(Tech Writer\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: http://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
