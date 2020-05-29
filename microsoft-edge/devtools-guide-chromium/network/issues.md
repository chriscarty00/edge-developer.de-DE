---
title: Leitfaden zu Netzwerkproblemen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 018a6ef89242d55cefaa974641be456f4501c557
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611805"
---
<!-- Copyright Kayce Basques and Jonathan Garbee

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# Leitfaden zu Netzwerkproblemen   




Dieser Leitfaden zeigt Ihnen, wie Sie Netzwerkprobleme oder Optimierungsmöglichkeiten im Netzwerk Panel von Microsoft Edge devtools erkennen.  

Informationen zu den Grundlagen der Netzwerksteuerung finden Sie unter [Erste Schritte][NetworkPerformance] .  

## Warteschlangen-oder verzögerte Anforderungen   

### Symptome  

Sechs Anforderungen werden gleichzeitig heruntergeladen.  Danach wird eine Reihe von Anforderungen in die Warteschlange gestellt oder angehalten.  Nachdem eine der ersten sechs Anforderungen beendet wurde, wird eine der Anforderungen in der Warteschlange gestartet.  

Im **Wasserfall** in [Abbildung 1](#figure-1)beginnen die ersten sechs Anforderungen für das `edge-iconx1024.msft.png` Objekt gleichzeitig.  Die nachfolgenden Anforderungen werden angehalten, bis eine der ursprünglichen sechs beendet ist.  

> ##### Abbildung1  
> Ein Beispiel für eine Reihe von Warteschlangen oder verzögerten Datenreihen im Netzwerk Panel  
> ![Ein Beispiel für eine Reihe von Warteschlangen oder verzögerten Datenreihen im Netzwerk Panel][ImageStalled]  

### Ursachen  

Es werden zu viele Anforderungen an eine einzelne Domäne gestellt.  Bei HTTP/1.0-oder http/1.1-Verbindungen können mit Microsoft Edge maximal sechs gleichzeitige TCP-Verbindungen pro Host ausgeführt werden.  

### Korrekturen  

*   Implementieren Sie Domänen Splitter, wenn Sie http/1.0 oder http/1.1 verwenden müssen.  
*   Verwenden Sie http/2.  Verwenden Sie keine Domänen Splitterung mit http/2.  
*   Entfernen oder aufschieben unnötiger Anforderungen, damit kritische Anforderungen früher heruntergeladen werden.  

## Langsame Zeit bis zum ersten Byte (TTFB)   

### Symptome  

Eine Anforderung verbringt lange Zeit darauf, das erste Byte vom Server zu empfangen.  

In [Abbildung 2](#figure-2)zeigt der lange, grüne Balken im **Wasserfall** an, dass die Anforderung lange gewartet hat.  Dies wurde mithilfe eines Profils simuliert, um die Netzwerkgeschwindigkeit zu begrenzen und eine Verzögerung hinzuzufügen.  

> ##### Abbildung2  
> Ein Beispiel für eine Anforderung mit einer langsamen Zeit bis zum ersten Byte  
> ![Ein Beispiel für eine Anforderung mit einer langsamen Zeit bis zum ersten Byte][ImageSlowTimeToFirstByte]  

### Ursachen  

*   Die Verbindung zwischen dem Client und dem Server ist langsam.  
*   Der Server reagiert langsam.  Hosten Sie den Server lokal, um festzustellen, ob es sich um eine langsame Verbindung oder einen Server handelt.  Wenn Sie beim Zugriff auf einen lokalen Server weiterhin langsam auf das erste Byte \ (TTFB \) zugreifen, ist der Server langsam.  

### Korrekturen  

*   Wenn die Verbindung langsam ist, sollten Sie das Hosten von Inhalten in einem CDN oder Ändern von Hostinganbieter in Frage stellen.  
*   Wenn der Server langsam ist, empfiehlt es sich, Datenbankabfragen zu optimieren, einen Cache zu implementieren oder Ihre Serverkonfiguration zu ändern.  

## Langsamer Download von Inhalten   

### Symptome  

Eine Anforderung dauert lange zum herunterladen.  

In [Abbildung 3](#figure-3)bedeutet der lange, blaue Balken im **Wasserfall** neben dem PNG, dass es lange dauert, bis der Download erfolgt ist.  

> ##### Abbildung 3  
> Ein Beispiel für eine Anforderung, deren Download viel Zeit in Anspruch nimmt  
> ![Ein Beispiel für eine Anforderung, deren Download viel Zeit in Anspruch nimmt][ImageSlowContentDownload]  

### Ursachen  

*   Die Verbindung zwischen dem Client und dem Server ist langsam.  
*   Viele Inhalte werden heruntergeladen.  

### Korrekturen  

*   Bedenken Sie, dass Sie Ihre Inhalte in einem CDN hosten oder Hosting-Anbieter ändern.  
*   Senden Sie weniger Bytes, indem Sie Ihre Anforderungen optimieren.  

## Wissens Spenden  

Haben Sie ein Netzwerkproblem, das diesem Leitfaden hinzugefügt werden sollte?  

*   Senden Sie einen Tweet an [@EdgeDevTools][MicrosoftEdgeTweet].  
*   Wählen **Sie Feedback senden Feedback** ![ senden ][ImageSendFeedbackIcon] im devtools aus, oder drücken Sie `Alt` + `Shift` + `I` \ (Windows \) oder `Option` + `Shift` + `I` \ (macOS \), um Feedback-oder Funktionsanforderungen bereitzustellen.  
*   [Öffnen Sie ein Problem][WebFundamentalsIssue] mit dem docs Repo.  

<!--   -->  



<!-- image links -->  

[ImageSendFeedbackIcon]: /microsoft-edge/devtools-guide-chromium/media/smile-icon.msft.png  

[ImageStalled]: /microsoft-edge/devtools-guide-chromium/media/network-network-disabled-cache-resources-queue.msft.png "Abbildung 1: Beispiel einer Reihe von Warteschlangen oder verzögerten Datenreihen im Netzwerk Panel"  
[ImageSlowTimeToFirstByte]: /microsoft-edge/devtools-guide-chromium/media/network-network-resources-using-dial-up-profile.msft.png "Abbildung 2: ein Beispiel für eine Anforderung mit einer langsamen Zeit bis zum ersten Byte"  
[ImageSlowContentDownload]: /microsoft-edge/devtools-guide-chromium/media/network-network-resources-edge-devtools.msft.png "Abbildung 3: ein Beispiel für eine Anforderung, deren Download viel Zeit in Anspruch nimmt"  

<!-- links -->  

[NetworkPerformance]: /microsoft-edge/devtools-guide-chromium/network/index "Überprüfen der Netzwerkaktivität in Microsoft Edge devtools"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Neues Problem – MicrosoftDocs/Edge – Entwickler"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/network/issues) gefunden und von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) und [Jonathan Garber][JonathanGarbee] \ (Google Developer Expert für Web Technology) verfasst.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
