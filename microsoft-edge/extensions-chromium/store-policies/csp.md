---
description: Inhaltssicherheitsrichtlinie für Edgeerweiterungen (Chromium).
title: Inhaltssicherheitsrichtlinie (Content Security Policy, CSP)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, Erweiterungenentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 8307482e780b4d631edffd976cca7ba724e2ad40
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397517"
---
# <a name="content-security-policy-csp"></a>Inhaltssicherheitsrichtlinie \(CSP\)  

Um eine große Klasse potenzieller websiteübergreifender Skriptingprobleme zu beheben, hat das Microsoft Edge Extension-System das allgemeine Konzept der Inhaltssicherheitsrichtlinie [\(CSP\) integriert.][W3CContentSecurityPolicy]  Dies führt einige ziemlich strenge Richtlinien ein, die Erweiterungen standardmäßig sicherer machen, und bietet Ihnen die Möglichkeit, Regeln für die Inhaltstypen zu erstellen und zu erzwingen, die von Ihren Erweiterungen und Anwendungen geladen und ausgeführt werden können.  

Im Allgemeinen funktioniert CSP als Block-/Allowlisting-Mechanismus für Ressourcen, die von Ihren Erweiterungen geladen oder ausgeführt werden.  Wenn Sie eine angemessene Richtlinie für Ihre Erweiterung definieren, können Sie die Für ihre Erweiterung benötigten Ressourcen sorgfältig berücksichtigen und den Browser bitten, sicherzustellen, dass diese Ressourcen die einzigen Ressourcen sind, auf die Ihre Erweiterung Zugriff hat.  Die Richtlinien bieten Sicherheit über die Hostberechtigungen, die Ihre Erweiterung anfordert. Sie sind eine zusätzliche Schutzebene, keine Ersetzung.  

Im Web wird eine solche Richtlinie über einen HTTP-Header oder -Element `meta` definiert.  Innerhalb des Microsoft Edge Extension-Systems ist keine der beiden Mechanismen geeignet.  Stattdessen wird eine Erweiterungsrichtlinie mithilfe der Datei für die `manifest.json` Erweiterung wie folgt definiert:  

```javascript
{
    ...,
    "content_security_policy": "[POLICY STRING GOES HERE]"
    ...
}
```  

> Ausführliche Informationen zur #A0 finden Sie in [][W3CContentSecurityPolicy] der Spezifikation für Inhaltssicherheitsrichtlinien und im Artikel ["An Introduction to Content Security Policy"][HTML5RocksIntroductionContentSecurityPolicy] auf HTML5Rocks.  

## <a name="default-policy-restrictions"></a>Standardrichtlinieneinschränkungen  

Pakete, die keine `manifest_version` definieren, verfügen nicht über eine Standardrichtlinie für die Inhaltssicherheit.  Pakete, die `manifest_version` 2 auswählen, verfügen über die folgende Standardrichtlinie für die Inhaltssicherheit.  

```javascript
script-src 'self'; object-src 'self'
```  

Die Richtlinie erhöht die Sicherheit, indem Erweiterungen und Anwendungen auf drei Arten eingeschränkt werden:  

**Eval und zugehörige Funktionen sind deaktiviert**  

Code wie der folgende funktioniert nicht:  

```javascript
alert(eval("foo.bar.baz"));
window.setTimeout("alert('hi')", 10);
window.setInterval("alert('hi')", 10);
new Function("return foo.bar.baz");
```  

Die Auswertung von Zeichenfolgen von JavaScript wie dieser ist ein gängiger XSS-Angriffsvektor.  Stattdessen sollten Sie Code wie:

```javascript
alert(foo && foo.bar && foo.bar.baz);
window.setTimeout(function() { alert('hi'); }, 10);
window.setInterval(function() { alert('hi'); }, 10);
function() { return foo && foo.bar && foo.bar.baz };
```  

**Inline-JavaScript wird nicht ausgeführt**  

Inline-JavaScript wird nicht ausgeführt.  Diese Einschränkung verbietet sowohl Inlineblöcke als auch `<script>` Inlineereignishandler, z. B. `<button onclick="...">` .

Mit der ersten Einschränkung wird eine große Klasse von websiteübergreifenden Skriptangriffen gelöscht, da es Ihnen nicht möglich ist, das skript versehentlich auszuführen, das von einem böswilligen Drittanbieter bereitgestellt wurde.  Es ist jedoch erforderlich, dass Sie Ihren Code mit einer sauberen Trennung zwischen Inhalt und Verhalten \(was Sie natürlich trotzdem tun sollten, richtig?\) schreiben.  Ein Beispiel kann dies deutlicher machen.  Sie können versuchen, ein Browseraktion-Popup als einzelnes Popup zu schreiben, `pop-up.html` das:  

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

Drei Dinge müssen sich ändern, damit dies so funktioniert, wie Sie es erwarten:  

*   Die `clickHandler` Definition muss in eine externe JavaScript-Datei \( verschoben werden. `popup.js`  
*   Die Inlineereignishandlerdefinitionen müssen im Sinne von umgeschrieben und in `addEventListener` extrahiert `popup.js` werden.  
    Wenn Sie Ihr Programm derzeit mit Code wie starten, sollten Sie es ersetzen, indem Sie es je nach Ihren Anforderungen in das Dokumentereignis oder das Ereignis des `<body onload="main();">` `DOMContentLoaded` `load` Fensters einhaken.  Verwenden Sie erstere, da sie im Allgemeinen schneller ausgelöst wird.  

*   Der `setTimeout` Aufruf muss umgeschrieben werden, um zu vermeiden, dass die Zeichenfolge zur Ausführung in `"awesome(); totallyAwesome()"` JavaScript konvertiert wird.  
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

**Nur lokale Skript- und Objektressourcen werden geladen**  

Skript- und Objektressourcen können nur aus dem Erweiterungspaket geladen werden, nicht aus dem Web.  Dadurch wird sichergestellt, dass ihre Erweiterung nur den speziell genehmigten Code ausgeführt, um zu verhindern, dass ein aktiver Netzwerkangreifer Ihre Anforderung für eine Ressource böswillig umleiten kann.  

Anstatt Code zu schreiben, der vom Laden von jQuery \(oder einer anderen Bibliothek\) aus einem externen CDN abhängt, sollten Sie erwägen, die spezifische Version von jQuery in Das Erweiterungspaket zu verwenden.  Das heißt, anstatt:  

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

Laden Sie die Datei herunter, fügen Sie sie in Ihr Paket ein, und schreiben Sie:  

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

## <a name="relaxing-the-default-policy"></a>Lockern der Standardrichtlinie  

**Inlineskript**  

<!-- Up until Chrome 45, there was no mechanism for relaxing the restriction against running inline JavaScript.  In particular, setting a script policy that includes `'unsafe-inline'` has no effect.  

As of Chrome 46, -->  

Inlineskripts können zulässig sein, indem der base64-codierte Hash des Quellcodes in der Richtlinie angegeben wird.  Diesem Hash muss der verwendete Hashalgorithmus \(sha256, sha384 oder sha512\) vorangestellt werden.  Navigieren Sie beispielsweise zu [Hashverwendung für \<script\> Elemente][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage].  

**Remoteskript**  

Wenn Sie externe JavaScript- oder Objektressourcen benötigen, können Sie die Richtlinie in begrenztem Umfang lockern, indem Sie sichere Ursprünge zulassen, von denen Skripts akzeptiert werden sollen.  Stellen Sie sicher, dass Laufzeitressourcen, die mit erhöhten Berechtigungen einer Erweiterung geladen werden, genau die Ressourcen sind, die Sie erwarten, und nicht durch einen aktiven Netzwerkangreifer ersetzt werden.  Da [Man-in-the-Middle-Angriffe][WikiManMiddleAttacks] sowohl trivial als auch über HTTP nicht nachweisbar sind, werden diese Ursprünge nicht akzeptiert.  

Derzeit können Entwickler Die Ursprünge der Liste mit den folgenden Schemas zulassen: `blob` , , , und `filesystem` `https` `extension` .  Der Hostteil des Ursprungs muss explizit für die `https` Und-Schemas angegeben `extension` werden.  Generische Platzhalter wie https:, und sind nicht `https://*` `https://*.com` zulässig. Unterdomänen-Platzhalter wie `https://*.example.com` sind zulässig.  Domänen in der [Liste öffentliches Suffix][PublicSuffixList] werden auch als generische Domänen auf oberster Ebene angezeigt.  Zum Laden einer Ressource aus diesen Domänen muss die Unterdomäne explizit aufgelistet werden.  Ist z. `https://*.cloudfront.net` B. nicht gültig, `https://XXXX.cloudfront.net` kann aber auch `https://*.XXXX.cloudfront.net` `allowlisted` sein.  

Zur Erleichterung der Entwicklung können Ressourcen, die über HTTP von Servern auf Ihrem lokalen Computer geladen werden, `allowlisted` sein.  Sie können Skript- und Objektquellen für einen beliebigen Port von oder `http://127.0.0.1` `http://localhost` zulassen.  

> [!NOTE]
> Die Einschränkung für über HTTP geladene Ressourcen gilt nur für die Ressourcen, die direkt ausgeführt werden.  Beispielsweise können Sie weiterhin Verbindungen zu beliebigen Ursprüngen herstellen. Die Standardrichtlinie schränkt keine oder keine der anderen `XMLHTTPRequest` `connect-src` #A0 ein.  

Eine lockere Richtliniendefinition, die das Laden von Skriptressourcen von `example.com` über HTTPS ermöglicht, kann wie dies aussehen:  

```javascript
"content_security_policy": "script-src 'self' https://example.com; object-src 'self'"
```  

> [!NOTE]
> Beide `script-src` und werden durch die Richtlinie `object-src` definiert.  Microsoft Edge akzeptiert keine Richtlinie, die nicht jeden dieser Werte auf \(mindestens\) ' ' `self` eingrenzt.  

<!-- Making use of Google Analytics is the canonical example for this sort of policy definition.  It is common enough that an Analytics boilerplate of sorts is provided in the Event Tracking with Google Analytics sample Extension, and a brief tutorial that goes into more detail.  -->  

**Ausgewertetes JavaScript**  

Die Richtlinie für und zugehörige Funktionen wie , und können durch Hinzufügen zu `eval()` `setTimeout(String)` Ihrer Richtlinie `setInterval(String)` `new Function(String)` `unsafe-eval` gelockert werden:  

```javascript
"content_security_policy": "script-src 'self' 'unsafe-eval'; object-src 'self'"
```  

Sie sollten jedoch lockere Richtlinien vermeiden.  Die Funktionen sind berüchtigte XSS-Angriffsvektoren.  

## <a name="tightening-the-default-policy"></a>Straffen der Standardrichtlinie  

Sie können diese Richtlinie natürlich in dem Umfang festziehen, den Ihre Erweiterung zulässt, um die Sicherheit auf Kosten der Benutzerfreundlichkeit zu erhöhen.  Um anzugeben, dass Ihre Erweiterung nur Ressourcen eines beliebigen Typs \(Bilder und so weiter\) aus dem zugeordneten Erweiterungspaket laden kann, kann beispielsweise eine Richtlinie von `default-src 'self'` geeignet sein.  

<!-- The Mappy sample Extension is a good example of an Extension that is been locked down above and beyond the defaults.  -->  

## <a name="content-scripts"></a>Inhaltsskripts  

Die zu besprechende Richtlinie gilt für die Hintergrund- und Ereignisseiten der Erweiterung.  Die Anwendung der Inhaltsskripts auf die Inhaltsskripts der Erweiterung ist komplizierter.  

Inhaltsskripts unterliegen im Allgemeinen nicht dem CSP der Erweiterung.  Da Inhaltsskripts keine HTML sind, besteht der Hauptauswirkungen davon, dass sie auch dann verwendet werden können, wenn der CSP der Erweiterung nicht angegeben wird, obwohl dies `eval` `unsafe-eval` nicht empfohlen wird.  Darüber hinaus gilt der CSP der Seite nicht für Inhaltsskripts.  Komplizierter sind Tags, die Inhaltsskripts erstellen und in das DOM der Seite setzen, `<script>` auf der sie ausgeführt werden.  Diese werden in Zukunft als DOM-injizierte Skripts referenziert.  

DOM-injizierte Skripts, die unmittelbar nach dem Einspritzen in die Seite ausgeführt werden, werden erwartungsgleich ausgeführt.  Stellen Sie sich ein Inhaltsskript mit dem folgenden Code als einfaches Beispiel vor:  

```javascript
document.write("<script>alert(1);</script>");
 ```  

Dieses Inhaltsskript bewirkt eine `alert` unmittelbar nach dem `document.write()` .  Beachten Sie, dass dies unabhängig von der Richtlinie ausgeführt wird, die von einer Seite angegeben werden kann.
Das Verhalten wird jedoch sowohl innerhalb dieses DOM-injizierten Skripts als auch für alle Skripts, die nicht sofort nach der Einspritzung ausgeführt werden, komplizierter.  Stellen Sie sich vor, Ihre Erweiterung wird auf einer Seite ausgeführt, die einen zugeordneten CSP enthält, der `script-src 'self'` angibt.  Stellen Sie sich nun vor, das Inhaltsskript führt den folgenden Code aus:  

```javascript
document.write("<button onclick='alert(1);'>click me</button>'");
```  

Wenn ein Benutzer diese Schaltfläche aus wählt, wird das `onclick` Skript nicht ausgeführt.  Dies liegt daran, dass das Skript nicht sofort ausgeführt wurde und Code erst interpretiert wird, wenn das Ereignis als Teil des Inhaltsskripts betrachtet wird, sodass der CSP der Seite \(nicht der Erweiterung\) das Verhalten `click` einschränkt.  Und da dieser CSP keine Angabe macht, wird der `unsafe-inline` Inlineereignishandler blockiert.  
Die richtige Möglichkeit, das gewünschte Verhalten in diesem Fall zu implementieren, kann sein, den Handler wie eine Funktion aus dem `onclick` Inhaltsskript wie folgt hinzuzufügen:  

```javascript
document.write("<button id='mybutton'>click me</button>'");
var button = document.getElementById('mybutton');
button.onclick = function() {
      alert(1);
};
```  

Ein weiteres ähnliches Problem tritt auf, wenn das Inhaltsskript Folgendes ausgeführt wird:  

```javascript
var script = document.createElement('script');
script.innerHTML = 'alert(1);'
document.getElementById('body').appendChild(script);
```  

In diesem Fall wird das Skript ausgeführt und die Warnung angezeigt.  Gehen Sie jedoch wie in diesem Fall vor:  

```javascript
var script = document.createElement('script');
script.innerHTML = 'eval("alert(1);")';
=document.getElementById('body').appendChild(script);
```  

Während das erste Skript ausgeführt wird, wird der `eval` Aufruf von blockiert.  Das heißt, während die anfängliche Skriptlaufzeit zulässig ist, wird das Verhalten innerhalb des Skripts durch den CSP der Seite reguliert.  
Je nachdem, wie Sie dominjizierte Skripts in Ihre Erweiterung schreiben, können Änderungen am CSP der Seite das Verhalten Ihrer Erweiterung beeinflussen.  Da Inhaltsskripts nicht vom CSP der Seite betroffen sind, ist dies ein guter Grund, um so viel Verhalten wie möglich ihrer Erweiterung in das Inhaltsskript anstelle von DOM-injizierten Skripts zu verwenden.  

<!-- image links -->  

<!-- links -->  

[HTML5RocksIntroductionContentSecurityPolicy]: https://www.html5rocks.com/en/tutorials/security/content-security-policy "Eine Einführung in die Inhaltssicherheitsrichtlinie | HTML5-Rock"  
[PublicSuffixList]: https://publicsuffix.org/list "ANZEIGEN DER ÖFFENTLICHEN SUFFIXLISTE"  
[W3CContentSecurityPolicyLevel2ScriptSrcHashUsage]: https://www.w3.org/TR/CSP2#script-src-hash-usage "Hashverwendung für \<Script\>-Elemente – Inhaltssicherheitsrichtlinie Ebene 2 | W3C"  
[W3CContentSecurityPolicy]: https://w3c.github.io/webappsec-csp "Inhaltssicherheitsrichtlinie Ebene 3 | W3C"  
[WikiManMiddleAttacks]: https://en.wikipedia.org/wiki/Man-in-the-middle_attack "Man-in-the-Middle-| Wikipedia"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/extensions/contentSecurityPolicy).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
