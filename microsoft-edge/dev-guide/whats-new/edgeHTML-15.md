---
description: Dieser Leitfaden enthält eine Übersicht über die Entwicklerfeatures und-Standards, die in EdgeHTML 15 enthalten sind.
title: Neuerungen in EdgeHTML 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.custom: seodec18
ms.openlocfilehash: e750a9272bb8bcdb51662839a31cc303c4064ef9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566785"
---
# Neuerungen in EdgeHTML 15
Hier sind die Änderungen, die mit der aktuellen Version der Microsoft Edge-Plattform ausgeliefert wurden, wie beim [Windows 10 Creators-Update](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) (04/2017, Build 15063). Eine Übersicht über Änderungen am gesamten Microsoft Edge-Browser finden Sie unter [Neuerungen in Microsoft Edge im Windows 10 Creators-Update](https://blogs.windows.com/msedgedev/2017/04/11/introducing-edgehtml-15/#DrVEvmPU6TPq3tMK.97)

Informationen zu Änderungen in nachfolgenden Windows Insider Preview-Builds finden Sie unter [Neuerungen in EdgeHTML](../whats-new.md).

Hier ist der Permalink für die folgende Liste der **[https://aka.ms/devguide_edgehtml_15](https://aka.ms/devguide_edgehtml_15)** Änderungen:

## Neue Funktionen

### Benutzerdefinierte CSS-Eigenschaften
Microsoft Edge unterstützt jetzt [CSS-benutzerdefinierte Eigenschaften](https://drafts.csswg.org/css-variables/), a. k. a-CSS-Variablen. Mit CSS-Variablen können Sie benutzerdefinierte CSS-Eigenschaften erstellen, die in Stylesheets wieder verwendet werden können, um die Menge doppelter Daten wie wiederholte Farben zu verringern. Die Verwendung von CSS-Variablen ist einfach:

```css
/* define a custom property by using two dashes and assign it a value */
body {   
   --default-color: #3390b1
}

/* reference it in your stylesheet with the "var()" function */
h1 {
   color: var(--default-color);
}
```  

### Intersection Observer
EdgeHTML 15 führt die [Schnittstellen-API-](https://w3c.github.io/IntersectionObserver/) Spezifikation ein. Die Schnittstelle Observer-API ermöglicht es Ihnen, die Position und Sichtbarkeit von DOM-Elementen relativ zu anderen Elementen oder dem globalen Viewport asynchron abzufragen. Diese API beseitigt die Notwendigkeit benutzerdefinierter teurer Code durch Erstellen einer Methode, um Elemente effizient zu benachrichtigen, wenn Sie sich in der Ansicht befinden.

### JavaScript

Leistungsoptimierungen stehen im Mittelpunkt mit dem EdgeHTML 15 rev des Chakra JavaScript-Moduls. Mit dem Windows 10 Creators-Update spart Chakra Arbeitsspeicher, indem es Funktionen erneut verzögert und Heap Argumente optimiert und die Leistung für minimierte-Code verbessert.

Darüber hinaus werden in EdgeHTML 15 die folgenden Vorschaufunktionen vorgestellt:

#### Experimentelle JavaScript-Features (aktiviert mit *about: Flags*)

* [Webassembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) ([Demo](https://webassembly.org/demo/))
* [Shared Memory und Atomics](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)

Weitere Informationen finden Sie unter [*Verbesserte JavaScript-Leistung, Webassembly und freigegebenen Arbeitsspeicher in Microsoft Edge*](https://blogs.windows.com/msedgedev/2017/04/20/improved-javascript-performance-webassembly-shared-memory/#t4gwUKjjtdmstMbs.97) .

### API für Zahlungsanforderungen
Die [Zahlungs Anforderungs-API](https://w3.org/TR/payment-request/) wird jetzt unterstützt, was einfachere Auschecken und Zahlungen im Web auf Windows 10-PCs und-Smartphones ermöglicht. Mit dieser API kann Microsoft Edge als Vermittler zwischen Händlern, Verbrauchern und Zahlungsmethoden (beispielsweise Kreditkarten) fungieren, die von Verbrauchern in der Cloud gespeichert wurden. Weitere Informationen zur Zahlungs Anforderungs-API finden Sie unter [einfachere Web-Zahlungen: Einführung in die API für Zahlungsanforderungen](https://blogs.windows.com/msedgedev/2016/12/15/payment-request-api-edge/) und das Entwicklerhandbuch zur [Zahlungs Anforderungs-API](/microsoft-edge/dev-guide/device/payment-request-api) .

### TCP fast Open (TFO)
TCP fast Open ist eine Funktion, die die Anzahl der Roundtrips verringert, die erforderlich sind, um eine TCP-Verbindung zu öffnen, wodurch die Leistung des Browser Netzwerks verbessert wird. Weitere Informationen finden Sie unter [Erstellen eines schnelleren und sichereren Webs mit schnell geöffnetem TCP](https://blogs.windows.com/msedgedev/2016/06/15/building-a-faster-and-more-secure-web-with-tcp-fast-open-tls-false-start-and-tls-1-3/#eQMauReErmIRXYqh.97). Aufgrund von Interoperabilitäts unterschieden in verschiedenen Netzwerktopologien ist diese Funktion in Microsoft Edge standardmäßig nicht aktiviert. Um Sie zu aktivieren, geben Sie `about:flags` Ihre Adressleiste ein, und aktivieren Sie das Kontrollkästchen **TCP schnell öffnen** unter dem Abschnitt *Netzwerk* aktivieren. 

### WebRTC und interoperabler RTC-Video-Codec-Unterstützung

EdgeHTML 15 unterstützt eine Teilmenge der WebRTC 1,0-API für die Interoperabilität mit Anwendungen, die mit früheren Versionen der W3C-WebRTC-PC-API circa 2015 erstellt wurden. Details finden Sie in der [WebRTC-API-Referenz](https://msdn.microsoft.com/library/mt806139(v=vs.85).aspx) .

Zur Nutzung der fortschrittlichsten Funktionen in der Peer-to-Peer-Audio-und Videokommunikation empfehlen wir die Verwendung der [Object Real-Time Communication)-API](../realtime-communication/object-rtc-api.md). Die ORTC-API eignet sich besser für Situationen, in denen Sie Gruppen-Audio-und Videoanrufe einrichten oder einzelne Transport-, Absender-und Empfängerobjekte direkt steuern möchten.

Microsoft Edge unterstützt sowohl H. 264/AVC-als auch VP8-Video mit ORTC und WebRTC 1,0 und bietet die folgenden Features zur Unterstützung beider Codectypen: [ABS-Send-Time](https://webrtc.org/experiments/rtp-hdrext/abs-send-time/), [GOOG-remb](https://tools.ietf.org/html/draft-alvestrand-rmcat-remb-03), [Bildverlust Anzeige und generisches nackt-Feedback](https://tools.ietf.org/html/rfc4585), RTP-erneute [Übertragung](https://tools.ietf.org/html/rfc4588).

Weitere Informationen finden Sie unter [Einführung in WebRTC 1,0 und interoperabler Echtzeitkommunikation in Microsoft Edge](https://blogs.windows.com/msedgedev/2017/01/31/introducing-webrtc-microsoft-edge/#k8XMeWKyZDQDPYR4.97).

### WebVR

Microsoft Edge bietet nun Unterstützung für [WebVR](https://immersive-web.github.io/webxr/), eine experimentelle API, die Windows-Mixed-Reality-Head-Mounted-Displays und Microsoft Edge verbindet. Diese Verbindung ermöglicht es, VR-Inhalte innerhalb einer Website zu erleben, was bedeutet, dass immersive VR-Erlebnisse nicht mehr auf Desktop-Anwendungen limitiert sind.  

Virtual Reality in Microsoft Edge wird von WebGL, einer JavaScript-API zum Rendern von 3D-und 2D-Grafiken, betrieben. WebGL-Anwendungen und-Anwendungen, die mit WebGL-Bibliotheken wie BabylonJS erstellt wurden, werden unterstützt. Sobald die Verbindung hergestellt ist, sendet WebVR visuelle Elemente, die den Positions-und Sensorinformationen um das Headset entsprechen. Die WebVR-API unterstützt auch räumliche Controller dank einer Erweiterung der [Gamepad-API](../dom/gamepad-api.md). Diese API ist standardmäßig aktiviert, daher müssen Sie keine Kennzeichnung umschalten.

Weitere Informationen finden Sie unter [WebVR-API-Referenz](https://msdn.microsoft.com/library/mt806281(v=vs.85).aspx) und [Gamepad-API-Referenz](https://msdn.microsoft.com/library/dn743630(v=vs.85).aspx) .

 > [!NOTE] 
 > Da sich die WebVR-Spezifikation noch in der Entwicklung befindet, kann sich die Implementierung von Microsoft Edge später in der Zeile ändern.



## Aktualisierte Features

### Inhalts Sicherheitsrichtlinie (Ebene 2)
Websites, die bereits CSP 1 verwenden, sollten weiterhin mit der Microsoft Edge-Unterstützung für CSP 2 funktionieren, doch empfiehlt es sich, alle `frame-src` Direktiven zu wechseln, die Worker-Skripts in die neue Direktive laden, `child-src` um Ihre Website zukunftssicher zu machen. (In CSP 3 `frame-src` wird nicht mehr auf Worker angewendet.) CSP 2 fügt auch Folgendes hinzu:

1. Neue Direktiven `base-uri` : `child-src` , `form-action` , `frame-ancestors` und `plugin-types` . Weitere Informationen finden Sie unter [unterstützte CSP-Direktiven von Microsoft Edge](../security/content-security-policy.md) .

2. Worker-Unterstützung: Hintergrund Arbeitskraft Skripts werden durch ihre eigene Richtlinie geregelt, unabhängig von der Richtlinie des Dokuments, in das Sie geladen werden. Wie bei Host Dokumenten können Sie den CSP für eine Arbeitskraft im Antwortheader einrichten. Neu in CSP 2 ist auch, dass sich die `allow-scripts` `allow-same-origin` Flags der `sandbox` Direktive nun auf die Erstellung von Worker-Threads auswirken.

3. Inlineskripts und-Formatvorlagen: CSP 2 ermöglicht die Ausführung von Inlineskripts und Formatvorlagen Blöcken, indem Sie als Whitelisting-Mechanismus als Whitelisting-Mechanismus bereitgestellt wird. Bei den Stichen handelt es sich um zufällige Base-64-Werte, die bei jeder Seitenauslastung generiert werden, die sowohl in der CSP-Richtlinie als auch in den Skripttags auf der Seite angezeigt wird. Wenn die Seite dynamisch beim Laden generiert wird, generiert der Server einen Kurzwert, fügt ihn in das NonceToken auf der Seite ein und deklariert ihn auch im HTTP-Header der Inhalts Sicherheitsrichtlinie. Hashwerte sind statische Werte, die (über *SHA256*-, *SHA384* -oder *SHA512* -Algorithmen) aus dem Inhalt eines oder-Elements generiert werden `<script>` , die `<style>` dann `script-src` `style-src` in der CSP-Richtlinie (über oder Direktiven) angegeben werden.

4. Reporting zur CSP-Verletzung: ein neues Ereignis, SecurityPolicyViolationEvent wird nun bei CSP-Verstößen ausgelöst. Der frühere Mechanismus für die CSP-Berichterstellung wird `report-uri` weiterhin unterstützt. Einige neue Felder wurden zu den Verletzungs Berichten hinzugefügt, die für beide gelten, einschließlich `effectiveDirective` (die Richtlinie, die verletzt wurde), `statusCode` (der HTTP-Antwortcode), `sourceFile` (die URL der problematischen Ressource), `lineNumber` und `columnNumber` .

### Web-Authentifizierung
Die Microsoft Edge-Unterstützung für die neue [Webauthentifizierungs-API](../device/web-authentication.md) mit [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) Biometrie wurde mit den folgenden Änderungen aktualisiert:
- Die anfängliche Implementierung der experimentellen Webauthentifizierungs-API, die in [EdgeHTML 14](https://blogs.windows.com/msedgedev/2016/08/04/introducing-edgehtml-14/#TVSCzKDkG4jCI5mt.97) eingeführt wurde (Windows 10 Anniversary Update, Build 10240, 7/2016), wurde über MS-prefixes-APIs (die [MSCredentials](https://msdn.microsoft.com/library/mt697639) -Schnittstelle) verfügbar gemacht. Obwohl diese APIs in EdgeHTML 15 weiterhin verfügbar sind, sind Sie nun zu Gunsten der nicht vordefinierten, auf Standards basierenden APIs und Verhaltensweisen veraltet, die in einer [neueren Momentaufnahme](https://w3.org/TR/2016/WD-webauthn-20160928) der Spezifikation definiert sind, und werden wahrscheinlich weiterhin geändert, wenn die Spezifikation zur Standardisierung heranreift.

- Die neueste Microsoft Edge-Implementierung ist standardmäßig deaktiviert und wird hinter einer Kennzeichnung versendet (geben `about:flags` Sie Ihre Adressleiste ein, um das Feature zu aktivieren).

- Microsoft Edge unterstützt noch keine externen Anmeldeinformationen wie USB-Schlüssel oder Bluetooth-Geräte. Die aktuelle API ist auf eingebettete im TPM gespeicherte Anmeldeinformationen limitiert. Ein Software-Fallback wird verwendet, wenn TPM auf dem Gerät nicht verfügbar ist.

- Das aktuell angemeldete Windows-Benutzerkonto muss so konfiguriert sein, dass es mindestens eine PIN und vorzugsweise eine Fingerabdruck-oder Fingerabdruckbiometrie unterstützt. Dadurch wird sichergestellt, dass Windows den Zugriff auf das TPM authentifizieren kann.

- Von den [vordefinierten Erweiterungen](https://w3.org/TR/webauthn/#extension-predef) , die in der Spezifikation beschrieben sind, unterstützt Microsoft Edge zurzeit nur die [Fido](https://w3.org/TR/webauthn/#extension-appid) -Webfunktion ( `webauthn_txAuthSimple` ).

- Die `timeoutSeconds` Option wird derzeit nicht ausgewertet

### WebDriver

EdgeHTML 15 bietet eine Handvoll WebDriver-Updates, einschließlich Unterstützung für die automatische Befehlszeilen Kennzeichnung und neue Befehls Endpunkte:

Methode | URI-Vorlage | Befehl
:----- | :----------  | :--------
POST | /Session/{Session-ID}/Alert/Accept | [Benachrichtigung annehmen](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-accept-alert)
POST | /Session/{Session-ID}/Alert/Dismiss | [Benachrichtigung ablehnen](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-dismiss-alert)
GET | /Session/{Session-ID}/Alert/Text | [Abrufen von Warnungs Text](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-get-alert-text)
POST | /Session/{Session-ID}/Alert/Text | [Benachrichtigungs Text senden](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-send-alert-text)
POST | /Session/{Session-ID}/Execute/Async | [Ausführen eines asynchronen Skripts](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-execute-async-script)
POST | /Session/{Session-ID}/Execute/Sync | [Skript ausführen](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-execute-script)
GET | /Session/{Session-ID}/Window | [Fenster Handle abrufen](https://w3c.github.io/webdriver/webdriver-spec.html#get-window-handle)
GET | /Session/{Session-ID}/Window/Handles | [Abrufen von Fensterhandles](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-get-window-handles)

Weitere Informationen und den Status anderer WebDriver-Features finden Sie unter [WebDriver](../../webdriver.md).

## Neue APIs in EdgeHTML 15

Hier finden Sie die vollständige Liste der neuen APIs in EdgeHTML 15. Sie werden im Format **[Schnittstellenname] aufgeführt. [ API-Name]**.

<iframe height='582' scrolling='no' title='Neue EdgeHTML15-APIs' src='//codepen.io/MicrosoftEdgeDocumentation/embed/evRjjZ/?height=582&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Informationen zu den <a href='http://codepen.io/MicrosoftEdgeDocumentation/pen/evRjjZ/'> neuen EdgeHTML15 </a> -APIs von Microsoft Edge docs (@MicrosoftEdgeDocumentation) finden Sie unter <a href='http://codepen.io/MicrosoftEdgeDocumentation'> </a> <a href='http://codepen.io'> CodePen </a> .</iframe>  

## Vorherige EdgeHTML-Versionen
[EdgeHTML 12/Windows Build 10240 (7/2015)](https://aka.ms/devguide_edgehtml_12)

[EdgeHTML 13/Windows Build 10586 (11/2015)](https://aka.ms/devguide_edgehtml_13)

[EdgeHTML 14/Windows Build 14393 (8/2016)](https://aka.ms/devguide_edgehtml_14)
