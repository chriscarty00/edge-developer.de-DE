---
description: JavaScript-Fehler werden von Entwicklertools gemeldet und debuggen jeweils in der Konsole
title: Nachverfolgen von Fehlern mithilfe der Konsole
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: ebd12f8932332b3e63162ab6952577bdb43bbccd
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483472"
---
# <a name="debug-errors-reported-in-console"></a>In der Konsole gemeldete Debugfehler  

Die erste Erfahrung, die Sie mit der **Konsole haben,** ist wahrscheinlich ein Fehler in einem Skript.  Navigieren Sie zu JavaScript-Fehler, der im [Konsolentool][GithubMicrosoftedgeDevtoolssamplesConsoleErrorHtml]gemeldet wurde.  

Wenn Sie DevTools im Browser öffnen, zeigt eine Schaltfläche oben rechts einen Fehler für die Webseite an.  
Wählen Sie die Schaltfläche aus, um Sie zur **Konsole zu führen,** und geben Sie weitere Informationen zu dem Fehler.  

:::image type="complex" source="../media/console-debug-displays-error.msft.png" alt-text="DevTools enthält detaillierte Informationen zum Fehler in der Konsole" lightbox="../media/console-debug-displays-error.msft.png":::
   DevTools enthält detaillierte Informationen zum Fehler in der **Konsole**  
:::image-end:::  

Aus den Informationen können Sie erfassen, dass sich der Fehler in Zeile 16 der Datei `error.html` befindet.  Wenn Sie den Link rechts neben der Konsole auswählen, führt er Sie zum Tool Sources und hebt die Codezeile mit `error.html:16` dem Fehler hervor. **** ****  

:::image type="complex" source="../media/console-debug-displays-in-sources.msft.png" alt-text="Das Tool Sources hebt die Codezeile hervor, die den Fehler verursacht." lightbox="../media/console-debug-displays-in-sources.msft.png":::
   Das **Tool Sources** hebt die Codezeile hervor, die den Fehler verursacht.  
:::image-end:::  

Das Skript versucht, das erste Element im Dokument zu erhalten `h2` und einen roten Rahmen um das Dokument zu zeichnen.  Es ist `h2` jedoch kein Element vorhanden, sodass das Skript fehlschlägt.  

## <a name="find-and-debug-network-issues"></a>Suchen und Debuggen von Netzwerkproblemen  

Andere Fehler, die die **Konsole** meldet, sind Netzwerkfehler.  Navigieren Sie zum Netzwerkfehler, der in der Konsole gemeldet wurde, um sie in Aktion [anzeigen zu können.][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorHtml]  

:::image type="complex" source="../media/console-debug-network-error.msft.png" alt-text="Konsole zeigt einen Netzwerk- und einen JavaScript-Fehler an" lightbox="../media/console-debug-network-error.msft.png":::
   **Konsole** zeigt einen Netzwerk- und einen JavaScript-Fehler an  
:::image-end:::  

Die Tabelle zeigt an, aber auf der Webseite ändert `loading` sich nichts, da die Daten nie abgerufen werden.  In der **Konsole**sind die folgenden beiden Fehler aufgetreten.  

*   Ein Netzwerkfehler, der mit der `GET` HTTP-Methode gefolgt von einem URI beginnt.  
*   Ein `Uncaught (in promise) TypeError: data.forEach is not a function` Fehler.  
    
Wenn Sie den Link in der Konsole `network-error.html:40` **auswählen,** führt DevTools Sie zum **Sources-Tool.**  Die problematische Codezeile wird hervorgehoben und gefolgt von einer `error` \( `x` \)-Schaltfläche.  Wählen Sie zum `Failed to load resource: the server responded with a status of 404 ()` Anzeigen der Fehlermeldung die Schaltfläche **Fehler** \( `x` \) aus.  


:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-debug-network-error-code-line.msft.png" alt-text="Wählen Sie den Link zur Webseite aus, und Code, in dem der Fehler auftritt, wird das Tool Quellen geöffnet." lightbox="../media/console-debug-network-error-code-line.msft.png":::
         Wählen Sie den Link zur Webseite aus, und Code, in dem der Fehler auftritt, wird das **Tool Quellen** geöffnet.  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-debug-network-error-sources.msft.png" alt-text="Verwenden Sie das Tool Quellen, um den Fehler in JavaScript zu finden." lightbox="../media/console-debug-network-error-sources.msft.png":::
         Verwenden Sie das Tool Quellen, um den Fehler in JavaScript **zu** finden.  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Im Beispiel informiert der Fehler Sie, dass die angeforderte URL nicht gefunden wird.  Führen Sie als Nächstes die folgenden Aktionen aus, um das **Netzwerktool zu** öffnen.  

1.  Öffnen Sie die **Konsole**.  
1.  Wählen Sie den URI aus, der dem Fehler zugeordnet ist.  
    
:::image type="complex" source="../media/console-debug-network-error-url.msft.png" alt-text="Konsole zeigt einen HTTP-Statuscode des Fehlers an, nachdem eine Ressource nicht geladen wurde" lightbox="../media/console-debug-network-error-url.msft.png":::
   **Konsole** zeigt einen HTTP-Statuscode des Fehlers an, nachdem eine Ressource nicht geladen wurde  
:::image-end:::  

:::row:::
    :::column:::
        :::image type="complex" source="../media/console-debug-network-error-network.msft.png" alt-text="Das Netzwerktool zeigt weitere Informationen zur fehlgeschlagenen Anforderung an." lightbox="../media/console-debug-network-error-network.msft.png":::
           Das **Netzwerktool** zeigt weitere Informationen zur fehlgeschlagenen Anforderung an.  
        :::image-end:::  
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/console-debug-network-error-network-detail.msft.png" alt-text="Überprüfen der Kopfzeilen im Netzwerktool kann mehr Einblick geben" lightbox="../media/console-debug-network-error-network-detail.msft.png":::
           Überprüfen der Kopfzeilen im **Netzwerktool** kann mehr Einblick geben  
        :::image-end:::  
    :::column-end:::
:::row-end:::  

Was war das Problem?  Zwei Schrägstriche \( `//` \) treten im angeforderten URI nach dem Wort `repos` auf.  Öffnen Sie das **Tool Quellen,** und überprüfen Sie Zeile 26.  Ein nachgestellter Schrägstrich \( \) tritt am Ende des `/` Basis-URI auf.  

:::image type="complex" source="../media/console-debug-network-error-code-error.msft.png" alt-text="Das Tool Quellen zeigt die Codezeile mit dem Fehler an." lightbox="../media/console-debug-network-error-code-error.msft.png":::
   Das **Tool Quellen** zeigt die Codezeile mit dem Fehler an.  
:::image-end:::  

Um keine Fehler in der Konsole zu **überprüfen,** navigieren Sie zu [Fixed network error reported in Console][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorFixedHtml].  

:::image type="complex" source="../media/console-debug-network-error-fixed.msft.png" alt-text="Das Beispiel ohne Fehler lädt Informationen aus GitHub und zeigt es an." lightbox="../media/console-debug-network-error-fixed.msft.png":::
   Das Beispiel ohne Fehler lädt Informationen aus GitHub und zeigt es an.  
:::image-end:::  

Stellen Sie sicher, dass Sie defensiv Codierungstechniken bereitstellen, um die vorherigen Benutzererfahrungen zu vermeiden.  Stellen Sie außerdem sicher, dass Ihr Code Fehler abfängt und jede in der **Konsole angezeigt wird.**  Navigieren Sie [zu Netzwerkfehlerbericht in Konsole und Benutzeroberfläche,][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorReportedHtml] und überprüfen Sie die folgenden Elemente.  

*   Stellen Sie dem Benutzer die Benutzeroberfläche zur Verfügung, dass etwas schief gelaufen ist.  
*   Geben Sie **in der Konsole**hilfreiche Informationen zum Netzwerkfehler aus Ihrem Code an.  
    
:::image type="complex" source="../media/console-debug-network-error-report.msft.png" alt-text="Ein Beispiel, das Fehler abfängt und meldet" lightbox="../media/console-debug-network-error-report.msft.png":::
   Ein Beispiel, das Fehler abfängt und meldet  
:::image-end:::  

Der folgende Codeausschnitt fängt Fehler mithilfe der Methode ab und meldet `handleErrors` sie, insbesondere die `throw Error` Zeile.  

```javascript
const handleErrors = (response) => {
    if (!response.ok) {
        let message = 'Could not load the information'
        document.querySelector('tbody').innerHTML = `
        <tr><td colspan=3>Error ${message}</td></tr>
        `;
        throw Error(response.status + ' ' + response.statusText);
    }
    return response;
};
```  

## <a name="create-errors-and-traces-in-the-console"></a>Erstellen von Fehlern und Ablaufverfolgungen in der Konsole

Neben dem Beispiel im vorherigen Abschnitt können Sie auch verschiedene Fehler und Ablaufverfolgungsprobleme `throw Error` in der **Konsole erstellen.**  
Navigieren Sie zum Anzeigen von zwei erstellten Fehlermeldungen in der **Konsole**zu [Erstellen von Fehlerberichten und -assertionen in der Konsole.][GithubMicrosoftedgeDevtoolssamplesConsoleErrorAssertHtml]  

:::image type="complex" source="../media/console-debug-error-assert.msft.png" alt-text="Von der Konsole erstellte Fehlermeldungen" lightbox="../media/console-debug-error-assert.msft.png":::
   Von der Konsole erstellte **Fehlermeldungen**  
:::image-end:::  

Der folgende Codeausschnitt wurde im vorherigen Beispiel verwendet.  

```javascript
function first(name) { second(name); }
function second(name) { third(name); }
function third(name) {
    if (!name) {
        console.error(`Name isn't defined :(`)
    } else {
        console.assert(
            name.length <= 8, 
            `"${name} is not less than eight letters"`
        );
    }
}
first();
first('Console');
first('Microsoft Edge Canary');
```  

Sie verfügen über drei Funktionen, die sich nacheinander gegenseitig anfordern.  

*   `first()`  
*   `second()`  
*   `third()`  
    
Jeder sendet ein `name` Argument an das andere.  In der Funktion überprüfen Sie, ob das Argument vorhanden ist, und wenn nicht, protokollieren Sie einen Fehler, dass der Name `third()` `name` nicht definiert ist.  Wenn definiert, verwenden Sie die -Methode, um zu überprüfen, ob das `name` Argument weniger als acht Buchstaben lang `assert()` `name` ist.  Sie fordern die `first()` Funktion dreimal mit den folgenden Parametern an.  

*   Kein Argument, das die `console.error()` Methode in der Funktion `third()` auslöst.  
*   Der Ausdruck als Parameter für die Funktion verursacht keinen Fehler, da argument vorhanden ist und kürzer `Console` `first()` als acht Buchstaben `name` ist.  
*   Der Ausdruck als zu verwendende Parameter bewirkt, dass die Methode einen Fehler gemeldet, da der Parameter länger als `Microsoft Edge Canary` `first()` acht Buchstaben `console.assert()` ist.  
    
Verwenden Sie die `console.assert()` -Methode, um bedingte Fehlerberichte zu erstellen.  Die folgenden beiden Beispiele haben dasselbe Ergebnis, aber eines benötigt eine zusätzliche `if{}` Anweisung.  

```javascript
let x = 20;
if (x < 40) { console.error(`${x} is too small`) };
console.assert(x >= 40, `${x} is too small`) 
```  

> [!IMPORTANT]
> Die zweite und dritte Codezeilen führen den gleichen Test aus.  Da die Assertion ein negatives Ergebnis aufzeichnen muss, testen Sie für den Fall `x < 40` `if` und für die `x >= 40` Assertion.  

Wenn Sie nicht sicher sind, welche Funktion eine andere Funktion anfordert, verwenden Sie die Methode, um nach zu verfolgen, welche Funktionen angefordert werden, um zu der `console.trace()` aktuellen zu kommen.  Navigieren Sie zum Anzeigen der Ablaufverfolgung in der **Konsole**zu [Erstellen von Ablaufverfolgungen in der Konsole.][GithubMicrosoftedgeDevtoolssamplesConsoleTraceHtml]  

```javascript
function here() {there()}
function there() {everywhere()}
function everywhere() {
    console.trace();
}
here();
there();
```  

Das Ergebnis ist eine Ablaufverfolgung, die mit dem Namen und dann und im zweiten Beispiel mit dem Namen angezeigt `here()` `there()` `everywhere()` `everywhere()` wird.  

:::image type="complex" source="../media/console-debug-trace.msft.png" alt-text="Eine von der Konsole erstellte Ablaufverfolgung" lightbox="../media/console-debug-trace.msft.png":::
   Eine von der Konsole erstellte **Ablaufverfolgung**  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamplesConsoleErrorHtml]: https://microsoftedge.github.io/DevToolsSamples/console/error.html "Im Konsolentool gemeldeter JavaScript-Fehler | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleErrorAssertHtml]: https://microsoftedge.github.io/DevToolsSamples/console/error-assert.html "Erstellen von Fehlerberichten und Assertionen in Konsolen| GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error.html "Netzwerkfehler in Konsolen| GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorFixedHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error-fixed.html "In Konsolenkonsolen gemeldeter Netzwerkfehler | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorReportedHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error-reported.html "Netzwerkfehlerberichte in Konsolen- und Benutzeroberflächen| GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleTraceHtml]: https://microsoftedge.github.io/DevToolsSamples/console/trace.html "Erstellen von Ablaufverfolgungen in konsolen | GitHub"  
