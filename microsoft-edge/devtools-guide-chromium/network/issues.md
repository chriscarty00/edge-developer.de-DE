---
description: Erfahren Sie, wie Sie Netzwerkprobleme im Netzwerkbereich von devTools Microsoft Edge erkennen.
title: Leitfaden zu Netzwerkproblemen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: c99f43872abe04800880c63ee4126bfcdd633edb
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564980"
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
# <a name="network-issues-guide"></a>Leitfaden zu Netzwerkproblemen  

In diesem Handbuch erfahren Sie, wie Sie Netzwerkprobleme oder Optimierungsmöglichkeiten im Netzwerkbereich von devTools Microsoft Edge erkennen.  

Um die Grundlagen des Netzwerktools **zu** erlernen, navigieren Sie zu [Erste Schritte][NetworkPerformance].  

## <a name="queued-or-stalled-requests"></a>Anforderungen in der Warteschlange oder in der Warteschlange  

**Symptome**  

Sechs Anforderungen werden gleichzeitig heruntergeladen.  Anschließend wird eine Reihe von Anforderungen in die Warteschlange gestellt oder ins Stocken geraten.  Sobald eine der ersten sechs Anforderungen abgeschlossen ist, wird eine der Anforderungen in der Warteschlange gestartet.  

Im **Wasserfall** in der folgenden Abbildung beginnen die ersten sechs Anforderungen für die `edge-iconx1024.msft.png` Ressource gleichzeitig.  Die nachfolgenden Anforderungen werden bis zum Ende einer der ursprünglichen sechs Beendete beendet.  

:::image type="complex" source="../media/network-network-disabled-cache-resources-queue.msft.png" alt-text="Ein Beispiel für eine in die Warteschlange eingereihte oder in die Warteschlange geplatzte Datenreihe im Netzwerkbereich" lightbox="../media/network-network-disabled-cache-resources-queue.msft.png":::
   Ein Beispiel für eine in der Warteschlange oder in der Warteschlange geplatzte Datenreihe im **Netzwerktool**  
:::image-end:::  

**Ursachen**  

Es werden zu viele Anforderungen für eine einzelne Domäne vorgenommen.  Bei HTTP/1.0- oder HTTP/1.1-Verbindungen ermöglicht Microsoft Edge maximal sechs gleichzeitige TCP-Verbindungen pro Host.  

**Fixes**  

*   Implementieren Sie die Domänensharding, wenn Sie HTTP/1.0 oder HTTP/1.1 verwenden müssen.  
*   Verwenden Sie HTTP/2.  Verwenden Sie keine Domänensharding mit HTTP/2.  
*   Entfernen oder Aufschub unnötiger Anforderungen, sodass kritische Anforderungen früher heruntergeladen werden.  
    
## <a name="slow-time-to-first-byte-ttfb"></a>Slow Time To First Byte (TTFB)  

**Symptome**  

Eine Anforderung wartet lange darauf, das erste Byte vom Server zu erhalten.  

In der folgenden Abbildung gibt die lange grüne Leiste im **Wasserfall** an, dass die Anforderung lange gewartet hat.  Dies wurde mithilfe eines Profils simuliert, um die Netzwerkgeschwindigkeit einzuschränken und eine Verzögerung hinzuzufügen.  

:::image type="complex" source="../media/network-network-resources-using-dial-up-profile.msft.png" alt-text="Ein Beispiel für eine Anforderung mit einem langsamen Time To First Byte" lightbox="../media/network-network-resources-using-dial-up-profile.msft.png":::
   Ein Beispiel für eine Anforderung mit einem langsamen Time To First Byte  
:::image-end:::  

**Ursachen**  

*   Die Verbindung zwischen dem Client und dem Server ist langsam.  
*   Der Server reagiert langsam.  Hosten Sie den Server lokal, um festzustellen, ob die Verbindung oder der Server langsam ist.  Wenn Sie beim Zugriff auf einen lokalen Server immer noch ein langsames Time To First Byte \(TTFB\) erhalten, ist der Server langsam.  
    
**Fixes**  

*   Wenn die Verbindung langsam ist, erwägen Sie, Ihre Inhalte auf einem CDN zu hosten oder Hostinganbieter zu ändern.  
*   Wenn der Server langsam ist, sollten Sie datenbankabfragen optimieren, einen Cache implementieren oder Ihre Serverkonfiguration ändern.  
    
## <a name="slow-content-download"></a>Langsamer Inhaltsdownload  

**Symptome**  

Das Herunterladen einer Anforderung dauert sehr lange.  

In der folgenden Abbildung bedeutet die lange, blaue Leiste im **Wasserfall** neben dem Png, dass der Download lange gezeitet hat.  

:::image type="complex" source="../media/network-network-resources-edge-devtools.msft.png" alt-text="Ein Beispiel für eine Anforderung, die lange dauert, bis sie heruntergeladen wird" lightbox="../media/network-network-resources-edge-devtools.msft.png":::
   Ein Beispiel für eine Anforderung, die lange dauert, bis sie heruntergeladen wird  
:::image-end:::  

**Ursachen**  

*   Die Verbindung zwischen dem Client und dem Server ist langsam.  
*   Viele Inhalte werden heruntergeladen.  
    
**Fixes**  

*   Erwägen Sie, Ihre Inhalte auf einem CDN oder sich ändernden Hostinganbietern zu hosten.  
*   Senden Sie weniger Bytes, indem Sie Ihre Anforderungen optimieren.  
    
<!--   ## Contribute knowledge  

Do you have a network issue that should be added to this guide?  

*   Send a tweet to [@EdgeDevTools][MicrosoftEdgeTweet].  
*   Choose **Send Feedback** \(![Send Feedback](../media/smile-icon.msft.png)\) in the DevTools or select `Alt`+`Shift`+`I` \(Windows, Linux\) or `Option`+`Shift`+`I` \(macOS\) to provide feedback or feature requests.  
*   [Open an issue][WebFundamentalsIssue] on the docs repo.  -->  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[NetworkPerformance]: ./index.md "Überprüfen der Netzwerkaktivität in Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Neues Problem – MicrosoftDocs/edge-developer"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite [](https://developers.google.com/web/tools/chrome-devtools/network/issues) befindet sich hier und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) und [Jonathan Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors#jonathan-garbee
