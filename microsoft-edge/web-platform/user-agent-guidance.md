---
description: Dieser Artikel enthält Eine Dokumentation zu den Microsoft Edge-Clienthinweisen und der Benutzer-Agent-Zeichenfolge
title: Erkennen von Microsoft Edge in Ihrer Website
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibility, web platform, user agent string, ua string, ua overrides, user-agent client hints, user agent client hints, ua client hints, ua ch
ms.openlocfilehash: 1957bb5bd33d9d921d8a12e16a4a52a23836027b
ms.sourcegitcommit: e90bbc210b5d510004bbc2145d49e14fe72ed54b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/20/2021
ms.locfileid: "11578779"
---
# <a name="how-to-detect-microsoft-edge-in-your-website"></a>Erkennen von Microsoft Edge in Ihrer Website  

Browser bieten Mechanismen für Websites zum Erkennen von Browserinformationen wie Marke und Versionsnummer.  Die Mechanismen erkennen auch andere Gerätemerkmale wie das Hostbetriebssystem.  Zwei solche Mechanismen, die auf Microsoft Edge unterstützt werden, sind [User-Agent-Clienthinweise](#user-agent-client-hints) und [User-Agent-Zeichenfolgen.](#user-agent-string)  Nach einer jahrzehntelangen Verwendung User-Agent Zeichenfolgen veraltet und haben eine lange Vorgeschichte als Ursache für Probleme mit der Websitekompatibilität.  Stattdessen empfiehlt das Microsoft Edge, einen verbesserten Mechanismus zum Abrufen von Browserinformationen namens [User-Agent Client Hints zu verwenden.](#user-agent-client-hints)  In diesem Artikel werden die beiden Mechanismen beschrieben, die Microsoft Edge zum Abrufen von Benutzer-Agent-Informationen unterstützt werden.  

|  | Serverseitig | Clientseitig |  
|:--- |:--- |:--- | 
| **User-Agent-Clienthinweise** \(empfohlen\) | `Sec-CH-UA` HTTPS-Header | `navigator.userAgentData` JavaScript-Methode |  
| **User-Agent-Zeichenfolge** \(legacy\) | `User-Agent` HTTPS-Header | `navigator.userAgent` JavaScript-Methode |  

Microsoft empfiehlt, die [Featureerkennung nach][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] Möglichkeit aus den folgenden Gründen zu verwenden.  

*   Verbessern Sie die Code-Wartbarkeit.  
*   Reduzieren Sie die Anfälligkeit von Code.  
*   Reduzieren Sie den Codebruch durch Änderungen an der User-Agent Zeichenfolge.  
    
Wenn [die Featureerkennung][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] nicht anwendbar ist und Sie die Benutzer-Agent-Erkennung verwenden müssen, verwenden Sie das folgende Format, um Microsoft Edge-Agent auf Windows und Android zu erkennen.  

## <a name="user-agent-client-hints"></a>User-Agent Clienthinweise  

Ab Microsoft Edge Version 90 können Sie auf eine sauberere und datenschutzerhaltende Weise auf Browserinformationen zugreifen.  

### <a name="user-agent-client-hints-https-header"></a>User-Agent Client hints HTTPS Header  

Standardmäßig senden Chromium browser einschließlich Microsoft Edge den `Accept-CH-UA` Antwortheader im folgenden Format.  

```https
Sec-CH-UA: "Chromium";v="91", "Microsoft Edge";v="91","Dummy;Browser Brand";v="99"
Sec-CH-UA-Mobile: ?0
```  

> [!NOTE]
> Clienthinweise werden nur über sichere Verbindungen mit `HTTPS` gesendet.  

Die folgenden Hinweise zur niedrigen Entropie werden standardmäßig gesendet.  Wenn Sie auf weitere Informationen zugreifen müssen, senden Sie einen der folgenden Anforderungsheader.  

#### <a name="user-agent-request-and-response-headers"></a>User-Agent- und Antwortheader  

| Anforderungsheader | Beispielantwortwert |  
|:--- |:--- |  
| `Sec-CH-UA` | `"Chromium";v="91", "Microsoft Edge";v="91","GREASE";v="99"` |  
| `Sec-CH-UA-Mobile` | `false` |  
| `Sec-CH-UA-Full-Version` | `91.0.866.0` |  
| `Sec-CH-UA-Platform` | `Windows` |  
| `Sec-CH-UA Platform-Version` | `10.0` |  
| `Sec-CH-UA-Arch` | `x86` |  
| `Sec-CH-UA-Model` |  |  

### <a name="user-agent-client-hints-javascript-api"></a>User-Agent Client hints JavaScript API  

Der Standardwert für die Antwort von `navigator.userAgentData` verwendet das folgende Format.  

```javascript
{ brands: [ {brand: "Chromium","version":"91"}, {brand: "Microsoft Edge","version":"91"}, {brand: "GREASE","version":"99"}, ]
mobile: false }
```  

Wenn Sie auf ausführlichere Informationen zugreifen müssen, verwenden Sie die [getHighEntropyValues()-Methode.][GithubWicgUaClientHintsGethighentropyvalues]  

:::row:::
   :::column span="":::
      Der folgende Codeausschnitt sendet eine Anforderung.  
   :::column-end:::
   :::column span="":::
      So erhalten Sie die folgende Antwort.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      ```javascript
         navigator.userAgentData.getHighEntropyValues(
             ["architecture", "model", "platform", "platformVersion", "uaFullVersion"])
             .then(ua => { console.log(ua) });
      ```  
   :::column-end:::
   :::column span="":::
      ```javascript
      {architecture: "x86", 
      model: "", 
      platform: "Windows", 
      platformVersion: "10.0", 
      uaFullVersion: "92.0.866.0"}
      ```  
   :::column-end:::
:::row-end:::  

## <a name="recommended-uses-of-user-agent-client-hints"></a>Empfohlene Verwendung von User-Agent Clienthinweisen  

Der Satz von Marken und die zugeordnete Anzeigereihenfolge ändern sich im Laufe der Zeit, sodass Sie niemals Indizes in das Array der zurückgegebenen Marken hart coden sollten.  Damit Sie ähnliche Probleme frühzeitig auf Ihrer Website erkennen können, enthält der Browser einen Markenwert, der sich im Laufe der Zeit ändert und aufgrund von häufigen Problemen bei der Analyse von Zeichenfolgen als Unterbrechung `GREASE` formatiert ist.  

Wenn Sie die Featureerkennung nicht verwenden [können,][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection]verwenden Sie keine hartcodierte Liste bekannter Chromium Browser für die Überprüfung.  Beispiele für hartcodierte Browsernamen sind `Microsoft Edge` und `Google Chrome` .  Gründe, [warum die][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] Featureerkennung nicht anwendbar ist, können die folgende Situation sein.  

*   Eine Behebung eines Chromium in einer späteren Version muss vermieden werden, und die betroffenen Browser sind außerhalb einer Überprüfung der Marke und Version schwer zu erkennen.  
    
Stattdessen sollten Sie die Marke überprüfen, um sicherzustellen, dass Ihre Erkennung für alle betroffenen `Chromium` browserbasierten Chromium gilt.  


```javascript
function isChromium() {
    for (brand_version_pair in navigator.userAgentData.brands) {
        if (brand_version_pair.brand == "Chromium") {
            return true;
        }
    }
    return false;
}
```  

## <a name="user-agent-string"></a>Zeichenfolge des Benutzer-Agents  

Nach Möglichkeit empfiehlt Microsoft, die Verwendung Microsoft Edge Browsererkennungslogik basierend auf der Zeichenfolge des Benutzer-Agents zu minimieren.  Wenn Sie einen guten Grund haben, den Benutzer-Agent zu erkennen, empfiehlt das Microsoft Edge-Team, dass Sie [Benutzer-Agent-Clienthinweise](#user-agent-client-hints) als primäre Erkennungslogik verwenden.  [Benutzer-Agent-Clienthinweise reduzieren](#user-agent-client-hints) auch die erforderliche Anzahl analysierter Zeichenfolgen.  Für den Legacyverweis wird jedoch das folgende Format für die Zeichenfolge User-Agent verwendet.  

:::row:::
   :::column span="":::
      Bei Windows verwendet der `User-Agent` HTTP-Anforderungsheader das folgende Format.  
   :::column-end:::
   :::column span="":::
      Unter Android verwendet der `User-Agent` HTTP-Anforderungsheader das folgende Format.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      ```https
      User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.85 Safari/537.36 Edg/90.0.818.46
      ```  
   :::column-end:::
   :::column span="":::
      ```https
      User-Agent: Mozilla/5.0 (Linux; Android 6.0; Nexus 5 Build/MRA58N) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.85 Mobile Safari/537.36 Edg/90.0.818.46
      ```  
   :::column-end:::
:::row-end:::  

Der Antwortwert der `navigator.userAgent` Methode verwendet das folgende Format.  

```javascript
"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4501.0 Safari/537.36 Edg/91.0.866.0"
```  

Plattformbezeichner ändern sich basierend auf dem verwendeten Betriebssystem, und die Versionsnummern werden ebenfalls erhöht, sobald die Zeit vergeht.  Das Format ist identisch mit dem Chromium Benutzer-Agent, der am Ende ein neues Token `Edg` hinzube kommt.  Microsoft hat das Token ausgewählt, um Kompatibilitätsprobleme zu vermeiden, die durch eine Zeichenfolge verursacht wurden, die Microsoft Edge EdgeHTML verwendet `Edg` `Edge` wurde.  Das `Edg` Token entspricht auch vorhandenen [Token,][WindowsBlogsMsedgedev20171005MicrosoftEdgeIosAndroidDeveloper] die unter iOS und Android verwendet werden.

## <a name="map-the-user-agent-string-to-browser-name"></a>Ordnen Sie die Zeichenfolge des Benutzer-Agents dem Browsernamen zu.  

Ordnen Sie die Zeichenfolgentoken des Benutzer-Agents einem besser lesbaren Browsernamen zu, der im Code verwendet werden soll.  Es ist heute ein gängiges Muster im Web.  Wenn Sie das neue Token einem Browsernamen zuordnungen, empfiehlt Microsoft, einen anderen Namen als den für den älteren Microsoft Edge-Browser verwendeten Namen zu verwenden, um zu vermeiden, dass versehentlich ältere Problemumgehungen angewendet werden, die für Chromium-basierte Browser nicht anwendbar `Edg` sind.

## <a name="user-agent-overrides"></a>Außerkraftsetzungen des Benutzer-Agents  

Manchmal erkennt eine Website den neuen Microsoft Edge-Agent nicht.  Dies führt dazu, dass eine Reihe von Features der Website möglicherweise nicht ordnungsgemäß funktioniert.  Wenn Microsoft über die Arten von Problemen benachrichtigt wird, kontaktiert Microsoft Sie \(ein Websitebesitzer\) und informiert Sie über den aktualisierten Benutzer-Agent.  

Möglicherweise benötigen Sie mehr Zeit, um die Erkennungslogik des Benutzer-Agents für Ihre Website zu aktualisieren und zu testen, um die von Microsoft gemeldeten Probleme zu beheben.  Um die Kompatibilität für Ihre Benutzer zu maximieren, verwenden Microsoft Edge Beta und Stable eine Liste von Außerkraftsetzungen des Benutzer-Agents.  Verwenden Sie die Außerkraftsetzungen des Benutzer-Agents, während Sie Ihre Website aktualisieren.  Die Liste der von Microsoft bereitgestellten Außerkraftsetzungen des Benutzer-Agents.  

Die Außerkraftsetzungen geben neue Benutzer-Agent-Werte an, die Microsoft Edge anstelle des Standardbenutzer-Agents für bestimmte Websites senden.  Führen Sie die folgenden Aktionen aus, um die Liste der derzeit angewendeten Benutzer-Agent-Überschreibungen anzeigen zu können.  

1.  Öffnen Sie Microsoft Edge Beta oder Stable-Kanal.  
1.  Navigieren Sie zu `edge://compat/useragent`.  
    
Die Microsoft Edge Canary- und Dev-Kanäle empfangen derzeit keine Außerkraftsetzungen des Benutzer-Agents.  Die Microsoft Edge Canary- und Dev-Kanäle stellen Umgebungen bereit, die den Standardbenutzer-agent Microsoft Edge verwenden.  Verwenden Sie Microsoft Edge Canary- und Dev-Kanäle, um Probleme auf Ihrer Website zu reproduzieren, die durch den Standardbenutzer-Agent Microsoft Edge werden.  Führen Sie die folgenden Aktionen aus, um Außerkraftsetzungen des Benutzer-Agents in Microsoft Edge Beta oder Stable-Kanälen zu deaktivieren.  

1.  Öffnen Sie Ihre Befehlszeilen-App.  
1.  Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn ein.  
    
    ```shell
    --disable-domain-action-user-agent-override
    ```  
    
1.  Führen Sie die Microsoft Edge-App mithilfe des Codeausschnitts aus.  
    
    ```shell
    {path/to/microsoft/edge.ext} --disable-domain-action-user-agent-override
    ```  
    
<!-- links -->  

[WindowsBlogsMsedgedev20171005MicrosoftEdgeIosAndroidDeveloper]: https://blogs.windows.com/msedgedev/2017/10/05/microsoft-edge-ios-android-developer "Microsoft Edge für iOS und Android: Was Entwickler über ihre | Microsoft Windows Blogs"  

[GithubWicgUaClientHintsGethighentropyvalues]: https://wicg.github.io/ua-client-hints#getHighEntropyValues "4.1.5. getHighEntropyValues-Methode – User-Agent Clienthinweise | GitHub"  

[MdnLearnToolsTestingCrossBrowserTestingFeatureDetection]: https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing/Feature_detection "Implementieren von Featureerkennungs| MDN"  
