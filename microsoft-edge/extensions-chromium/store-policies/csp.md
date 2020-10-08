---
description: Inhalts Sicherheitsrichtlinie für Edge (Chrom)-Erweiterungen.
title: Inhalts Sicherheitsrichtlinie (CSP)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Browser-Erweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: f3769639465d048c42ad0705f74598fbd1db8a20
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015716"
---
# Inhalts Sicherheitsrichtlinie \ (CSP \)  

Um eine große Klasse potenzieller Probleme mit Website übergreifendem Skripting zu verringern, hat das Microsoft Edge-Erweiterungssystem das allgemeine Konzept der [Inhalts Sicherheitsrichtlinie (CSP \)][W3CContentSecurityPolicy]übernommen.  Dies führt einige ziemlich strenge Richtlinien ein, die Erweiterungen standardmäßig sicherer machen, und bietet Ihnen die Möglichkeit, Regeln für die Typen von Inhalten zu erstellen und zu erzwingen, die von ihren Erweiterungen und Anwendungen geladen und ausgeführt werden können.  

Im Allgemeinen funktioniert CSP als Block-allowlisting-Mechanismus für Ressourcen, die von ihren Erweiterungen geladen oder ausgeführt werden.  Wenn Sie eine angemessene Richtlinie für Ihre Erweiterung definieren, können Sie die Ressourcen, die ihre Erweiterung erfordert, sorgfältig berücksichtigen und den Browser bitten, sicherzustellen, dass dies die einzigen Ressourcen ist, auf die ihre Erweiterung zugreifen kann.  Diese Richtlinien bieten Sicherheit über die Host Berechtigungen für Ihre Erweiterungsanforderungen. Es handelt sich um eine zusätzliche Schutzebene, die nicht ersetzt werden kann.  

Im Web wird eine solche Richtlinie über einen HTTP-Header oder- `meta` Element definiert.  Innerhalb des Microsoft Edge-Erweiterungssystems ist kein geeigneter Mechanismus.  Stattdessen wird eine Erweiterungs Richtlinie über die `manifest.json` Datei für die Erweiterung wie folgt definiert:  

```javascript
{
    ...,
    "content_security_policy": "[POLICY STRING GOES HERE]"
    ...
}
```  

> Ausführliche Informationen zur CSP-Syntax finden Sie in der [Inhalts Sicherheitsrichtlinien-Spezifikation][W3CContentSecurityPolicy] und im Artikel ["eine Einführung in die Inhaltssicherheit"][HTML5RocksIntroductionContentSecurityPolicy] auf HTML5Rocks.  

## Standardmäßige Richtlinieneinschränkungen  

Pakete, die keine definieren, `manifest_version` verfügen nicht über eine Standardrichtlinie für Inhaltssicherheit.  Für diejenigen, die `manifest_version` 2 auswählen, gibt es eine Standardrichtlinie für Inhaltssicherheit:  

```javascript
script-src 'self'; object-src 'self'
```  

Diese Richtlinie bietet Sicherheit, indem Erweiterungen und Anwendungen auf drei Arten eingeschränkt werden:  

**Eval und verwandte Funktionen sind deaktiviert**  

Code wie den folgenden funktioniert nicht:  

```javascript
alert(eval("foo.bar.baz"));
window.setTimeout("alert('hi')", 10);
window.setInterval("alert('hi')", 10);
new Function("return foo.bar.baz");
```  

Die Auswertung von Zeichenfolgen mit JavaScript wie diesem ist ein häufig verwendeter XSS-Angriffsvektor.  Stattdessen sollten Sie Code wie folgt schreiben:

```javascript
alert(foo && foo.bar && foo.bar.baz);
window.setTimeout(function() { alert('hi'); }, 10);
window.setInterval(function() { alert('hi'); }, 10);
function() { return foo && foo.bar && foo.bar.baz };
```  

**Inline-JavaScript wird nicht ausgeführt**  

Inline-JavaScript wird nicht ausgeführt.  Diese Einschränkung `<script>` verbietet sowohl Inline Blöcke als auch Inline-Ereignishandler wie `<button onclick="...">` .

Mit der ersten Einschränkung wird eine große Klasse von websiteübergreifenden Skripting-Angriffen gelöscht, da Sie das Skript, das von einem böswilligen Drittanbieter bereitgestellt wird, nicht versehentlich ausführen können.  Allerdings ist es erforderlich, dass Sie Ihren Code mit einer sauberen Trennung zwischen Inhalt und Verhalten schreiben \ (was Sie natürlich ohnehin tun sollten, oder? \).  Ein Beispiel kann dies deutlicher machen.  Sie können versuchen, ein Popup-Fenster für eine Browser Aktion zu schreiben, das `pop-up.html` Folgendes enthält:  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script>
            function awesome() {
                // do something awesome!
            }
            
            function totallyAwesome() {
                // do something TOTALLY awesome!
            }
            
            function clickHandler(element) {
                setTimeout("awesome(); totallyAwesome()", 1000);
            }
            
            function main() {
                // Initialization work goes here.
            }
        </script>
    </head>
    <body onload="main();">
        <button onclick="clickHandler(this)">
            Click for awesomeness!
        </button>
    </body>
</html>
```  

Drei Dinge müssen sich ändern, um diese Arbeit wie erwartet zu gestalten:  

*   Die `clickHandler` Definition muss in eine externe JavaScript-Datei verschoben werden \ ( `popup.js` kann ein gutes Ziel sein).  
*   Die Definitionen des Inline-Ereignishandlers müssen in Bezug auf `addEventListener` und extrahiert werden `popup.js` .  
    Wenn Sie das Programm zurzeit mithilfe von Code wie starten `<body onload="main();">` , sollten Sie es in der Weise ersetzen, indem Sie das `DOMContentLoaded` Ereignis des Dokuments oder das `load` Ereignis des Fensters abhängig von Ihren Anforderungen einbinden.  Verwenden Sie das erstere, da es in der Regel schneller auslöst.  

*   Der `setTimeout` Aufruf muss neu geschrieben werden, um zu verhindern, dass die Zeichenfolge `"awesome(); totallyAwesome()"` in JavaScript für die Ausführung konvertiert wird.  
    Diese Änderungen können etwa wie folgt aussehen:  

```javascript
function awesome() {
    // Do something awesome!
}

function totallyAwesome() {
    // do something TOTALLY awesome!
}

function awesomeTask() {
    awesome();
    totallyAwesome();
}

function clickHandler(e) {
    setTimeout(awesomeTask, 1000);
}

function main() {
    // Initialization work goes here.
}

// Add event listeners once the DOM has fully loaded by listening for the
// `DOMContentLoaded` event on the document, and adding your listeners to
// specific elements when it triggers.
document.addEventListener('DOMContentLoaded', function () {
    document.querySelector('button').addEventListener('click', clickHandler);
    main();
});
```  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="popup.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

**Es werden nur lokale Skript-und Objektressourcen geladen**  

Skript-und Objektressourcen können nur aus dem Erweiterungspaket geladen werden, nicht aus dem ganzen Web.  Dadurch wird sichergestellt, dass Ihre Erweiterung nur den von Ihnen ausdrücklich genehmigten Code ausführt, wodurch verhindert wird, dass ein aktiver Netzwerk Angreifer Ihre Anforderung für eine Ressource in böswilliger Weise umleitet.  

Anstatt Code zu schreiben, der von jQuery \ (oder einer anderen Bibliothek \) abhängig ist, die von einem externen CDN geladen werden, sollten Sie die spezifische Version von jQuery in Ihrem Erweiterungspaket einbeziehen.  Das heißt, statt:  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

Laden Sie die Datei herunter, fügen Sie Sie in Ihr Paket ein, und schreiben Sie Folgendes:  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="jquery.min.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

## Entspannen der Standardrichtlinie  

**Inline Skript**  

<!-- Up until Chrome 45, there was no mechanism for relaxing the restriction against running inline JavaScript.  In particular, setting a script policy that includes `'unsafe-inline'` has no effect.  

As of Chrome 46, -->  

Inline Skripts können durch Angabe des Base64-codierten Hashs des Quellcodes in der Richtlinie zugelassen werden.  Dieser Hash muss vom verwendeten Hashalgorithmus (SHA256, SHA384 oder SHA512 \) vorangestellt werden.  Ein Beispiel finden Sie unter [Hash Verwendung für \<script\> Elemente][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage] .  

**Remote Skript**  

Wenn Sie einige externe JavaScript-oder Objektressourcen benötigen, können Sie die Richtlinie in begrenztem Umfang lockern, indem Sie allowlisting, um sicherzustellen, woher Skripts akzeptiert werden sollen.  Überprüfen Sie, ob Laufzeitressourcen, die mit erhöhten Berechtigungen einer Erweiterung geladen werden, genau die erwarteten Ressourcen sind und nicht durch einen aktiven Netzwerk Angreifer ersetzt werden.  Da [man-in-the-Middle-Angriffe][WikiManMiddleAttacks] sowohl trivial als auch unauffindbar über HTTP sind, werden diese Ursprünge nicht akzeptiert.  

Derzeit können entwicklerlist-Ursprünge mit den folgenden Schemas zulassen: `blob` ,, `filesystem` `https` und `extension` .  Der Host-Teil des Ursprungs muss explizit für die `https` und-Schemas angegeben werden `extension` .  Generische Platzhalter wie https: `https://*` und `https://*.com` sind nicht zulässig; Platzhalter für Subdomänen wie `https://*.example.com` zulässig.  Domänen in der [Liste der öffentlichen Suffixe][PublicSuffixList] werden auch als generische Domänen auf oberster Ebene angezeigt.  Um eine Ressource aus diesen Domänen zu laden, muss die Unterdomäne explizit aufgelistet werden.  Ist beispielsweise `https://*.cloudfront.net` ungültig, kann aber `https://XXXX.cloudfront.net` `https://*.XXXX.cloudfront.net` allowlisted sein.  

Zur Vereinfachung der Entwicklung können Ressourcen, die über HTTP von Servern auf dem lokalen Computer geladen werden, allowlisted werden.  Sie könnenlist-Skript-und Objektquellen an einem beliebigen Port einer der beiden `http://127.0.0.1` oder zulassen `http://localhost` .  

> [!NOTE]
> Die Beschränkung für Ressourcen, die über HTTP geladen werden, gilt nur für die Ressourcen, die direkt ausgeführt werden.  Sie sind nach wie vor kostenlos, um beispielsweise XMLHttpRequest-Verbindungen zu beliebigen Ursprungs zu machen, die Ihnen gefallen; die Standardrichtlinie schränkt `connect-src` oder keine der anderen CSP-Direktiven in irgendeiner Weise ein.  

Eine lockere Richtliniendefinition, mit der Skriptressourcen von example.com über HTTPS geladen werden können, sieht wie folgt aus:  

```javascript
"content_security_policy": "script-src 'self' https://example.com; object-src 'self'"
```  

> [!NOTE]
> Beide `script-src` und `object-src` werden durch die Richtlinie definiert.  Microsoft Edge akzeptiert keine Richtlinie, die die einzelnen Werte nicht auf \ (mindestens \) ' `self` ' beschränkt.  

<!-- Making use of Google Analytics is the canonical example for this sort of policy definition.  It is common enough that an Analytics boilerplate of sorts is provided in the Event Tracking with Google Analytics sample Extension, and a brief tutorial that goes into more detail.  -->  

**JavaScript ausgewertet**  

Die Richtlinie für `eval()` und verwandte Funktionen wie und `setTimeout(String)` `setInterval(String)` `new Function(String)` können durch Hinzufügen `unsafe-eval` zu Ihrer Richtlinie gelockert werden:  

```javascript
"content_security_policy": "script-src 'self' 'unsafe-eval'; object-src 'self'"
```  

Wir empfehlen jedoch dringend, dies zu tun.  Diese Funktionen sind berüchtigte XSS-Angriffsvektoren.  

## Verschärfen der Standardrichtlinie  

Sie können diese Richtlinie selbstverständlich so anziehen, wie es Ihre Erweiterung zulässt, um die Sicherheit zu Lasten der Bequemlichkeit zu erhöhen.  Um anzugeben, dass Ihre Erweiterung nur Ressourcen eines beliebigen Typs \ (Bilder usw.) aus dem zugehörigen Erweiterungspaket laden kann, ist beispielsweise eine Richtlinie von `default-src 'self'` geeignet.  

<!-- The Mappy sample Extension is a good example of an Extension that is been locked down above and beyond the defaults.  -->  

## Inhalts Skripts  

Die zu diskutierende Richtlinie gilt für die Hintergrundseiten und Ereignis Seiten der Erweiterung.  Die Art und Weise, wie die Inhalts Skripts auf die Inhalts Skripts der Erweiterung angewendet werden, ist komplizierter.  

Inhalts Skripts unterliegen in der Regel nicht dem CSP der Erweiterung.  Da Inhalts Skripts keine HTML-Datei sind, ist dies hauptsächlich darauf zu verwenden, dass Sie auch dann verwendet werden können, `eval` Wenn der CSP der Erweiterung nicht angibt `unsafe-eval` , dies aber nicht empfohlen wird.  Darüber hinaus gilt der CSP der Seite nicht für Inhalts Skripts.  Komplizierter sind `<script>` Tags, die Inhalts Skripts erstellen und in das DOM der Seite einfügen, auf der Sie ausgeführt werden.  Diese werden als mit Dom-injizierte Skripts weitergeleitet.  

Dom-injizierte Skripts, die unmittelbar nach der Injektion in die Seite ausgeführt werden, werden wie erwartet ausgeführt.  Stellen Sie sich ein Inhalts Skript mit dem folgenden Code als einfaches Beispiel vor:  

```javascript
document.write("<script>alert(1);</script>");
 ```  

Dieses Inhalts Skript bewirkt `alert` unmittelbar nach dem `document.write()` .  Beachten Sie, dass dies unabhängig von der von einer Seite angegebenen Richtlinie ausgeführt werden kann.
Das Verhalten wird jedoch sowohl innerhalb des DOM-injizierten Skripts als auch bei Skripten komplizierter, die nicht unmittelbar nach der Injektion ausgeführt werden.  Stellen Sie sich vor, dass Ihre Erweiterung auf einer Seite ausgeführt wird, die einen zugeordneten CSP bereitstellt, der angibt `script-src 'self'` .  Stellen Sie sich nun vor, dass das Inhalts Skript den folgenden Code ausführt:  

```javascript
document.write("<button onclick='alert(1);'>click me</button>'");
```  

Wenn ein Benutzer auf diese Schaltfläche klickt, `onclick` wird das Skript nicht ausgeführt.  Dies liegt daran, dass das Skript nicht sofort ausgeführt wurde und Code nicht interpretiert wird, bis das Click-Ereignis nicht als Teil des Inhalts Skripts betrachtet wird, daher schränkt der CSP der Seite \ (nicht der Erweiterung \) das Verhalten ein.  Und da dieser CSP nicht angibt `unsafe-inline` , wird der Inline-Ereignishandler blockiert.  
Die richtige Methode zum Implementieren des gewünschten Verhaltens in diesem Fall ist das Hinzufügen des `onclick` Handlers als Funktion aus dem Inhalts Skript wie folgt:  

```javascript
document.write("<button id='mybutton'>click me</button>'");
var button = document.getElementById('mybutton');
button.onclick = function() {
      alert(1);
};
```  

Ein anderes ähnliches Problem tritt auf, wenn das Inhalts Skript Folgendes ausführt:  

```javascript
var script = document.createElement('script');
script.innerHTML = 'alert(1);'
document.getElementById('body').appendChild(script);
```  

In diesem Fall wird das Skript ausgeführt, und die Benachrichtigung wird angezeigt.  In diesem Fall gehen Sie jedoch wie folgt vor:  

```javascript
var script = document.createElement('script');
script.innerHTML = 'eval("alert(1);")';
=document.getElementById('body').appendChild(script);
```  

Während das anfängliche Skript ausgeführt wird, wird der Anruf an `eval` blockiert.  Das heißt, während die anfängliche Skriptlaufzeit zulässig ist, wird das Verhalten innerhalb des Skripts vom CSP der Seite reguliert.  
Je nachdem, wie Sie in ihrer Erweiterung Dom-injizierte Skripts schreiben, kann sich die Änderung des CSP der Seite auf das Verhalten der Erweiterung auswirken.  Da Inhalts Skripts nicht vom CSP der Seite betroffen sind, ist dies ein guter Grund, um das Inhalts Skript so weit wie möglich von der Erweiterung zu versetzen, anstatt von Dom-injizierten Skripts.  

<!-- image links -->  

<!-- links -->  

[HTML5RocksIntroductionContentSecurityPolicy]: https://www.html5rocks.com/en/tutorials/security/content-security-policy "Eine Einführung in die Inhalts Sicherheitsrichtlinie – HTML5 rockt"  
[PublicSuffixList]: https://publicsuffix.org/list "Anzeigen der Liste der öffentlichen Suffixe"  
[W3CContentSecurityPolicyLevel2ScriptSrcHashUsage]: https://www.w3.org/TR/CSP2#script-src-hash-usage "Hash Verwendung für \ <Skript \ > Elemente – Inhalts Sicherheitsrichtlinienebene 2"  
[W3CContentSecurityPolicy]: https://w3c.github.io/webappsec-csp "Inhalts Sicherheitsrichtlinienebene 3"  
[WikiManMiddleAttacks]: https://en.wikipedia.org/wiki/Man-in-the-middle_attack "Man-in-the-Middle-Angriff – Wikipedia"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/extensions/contentSecurityPolicy).  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
