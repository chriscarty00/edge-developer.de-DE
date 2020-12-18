---
ms.assetid: 961ca575-6b93-4367-a72b-f3f02e5b9568
description: Verweis auf gängige Codes und empfohlene Problemlösungen der Konsole
title: DevTools – Fehler- und Statuscodes der Konsole
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools, Konsolencodes
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: da9facaa65b2bd2403d454c2041e2ad30dfcd112
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234290"
---
# Fehler- und Statuscodes der Konsole  

Dieser Verweis hilft Ihnen bei der Interpretation von Fehler- und Statusmeldungen von der DevTools-[Konsole](../console.md).  Verwenden Sie die folgende Tabelle, um Codes anhand ihres Präfixes \ nachzuschlagen (wobei "x" für eine 0&ndash;9-stellige Zahl steht\):

| Codepräfix | Bereich | Beschreibung |  
|:--- | :--- |:--- |  
| [CSP143xx](#csp-codes) | Sicherheitsrichtlinie für Inhalte | Ressourcen, die durch die Verwendung eines `Content-Security-Policy` HTTP-Headers blockiert werden.  |  
| [CSS31xx](#css-codes) | Stylesheets | Fehler im Zusammenhang mit *Web Open Font Format* \(WOFF\) und *Embedded OpenType* \(EOT\) Schriftart- und Hostserver-Probleme.  |  
| [HTML1112-1300](#html-codes) | HTML | Die meisten davon sind Legacy-Codes, die spezifisch für Microsoft Internet Explorer-Konzepte wie *Dokumentmodus* und *Kompatibilitätsansicht* sind.  |  
| [HTML1400-1532](#html5-parser-warnings) | HTML5-Analyse | Vom HTML5-Parser ausgelöste Validierungswarnungen.  |  
| [HTTP](#http-codes) | Serverfehler und Status | Codes, die von Remoteservern als Antwort auf HTTP-Anforderungen zurückgegeben wurden.  |  
| [SCRIPT10xx](#javascript-syntax-errors) | JavaScript-Syntaxfehler | Tritt auf, wenn die Struktur einer Ihrer JavaScript-Anweisungen gegen eine oder mehrere syntaktische Regeln verstößt.  |  
| [SCRIPT50xx](#javascript-run-time-errors) | JavaScript-Laufzeitfehler | Tritt auf, wenn Ihr Skript versucht, eine Aktion auszuführen, die das System nicht ausführen kann.  |  
| [SEC71xx](#security-codes) | Sicherheit | Spiegelt Sicherheitsbedingungen wider, die von Microsoft Edge erzwungen werden, wie z.B. *Gemischte Inhalte* und *Tracking-Schutz*.  |  
| [SVG560x](#svg-codes) | Skalierbare Vektorgrafiken |  Umfangreiches SVG-Debugging wird derzeit nicht unterstützt, aber einige Konsolenmeldungen werden zu Debugging-Zwecken bereitgestellt.  |  
| WebGL11_xxx | WebGL | Fehlermeldungen aus dem WebGL-Kontext.  Siehe auch [GLSL-Fehler](https://msdn.microsoft.com/library/dn611835.aspx).  |  
| [XML5xxx](#xml-codes) | XML | Fehler beim Analysieren und Überprüfung von XML.  |  

## CSP-Codes  

Ressourcen, die durch die Verwendung eines `Content-Security-Policy` HTTP-Headers blockiert wurden, werden über die DevTools-Konsole und optional als Bericht zurück an den Server gemeldet.

| Code | Meldung | Beschreibung | Empfohlene Problemlösung |
|:--- |:--- |:--- |:--- |
| CSP14301 | "Fehler beim Analysieren von \[Richtlinientyp\] aufgrund von \<the reason for canceling the operation\> -- Die Richtlinie wird ignoriert." | Der angegebene Sicherheitsrichtlinientyp \(z.B. script-src, base-uri\) ist aus dem angegebenen Grund fehlgeschlagen und wird ignoriert.  | Stellen Sie sicher, dass Sie alle erforderlichen Ressourcen eines bestimmten Typs in einer einzigen Richtlinie auflisten.  Zum Beispiel wird in `script-src https://host1.com; script-src https://host2.com` die zweite Direktive ignoriert.  Im Folgenden werden beide Ursprünge korrekt als gültig angegeben: `script-src https://host1.com https://host2.com`.  |
| CSP14302 | "Fehler beim Analysieren der Quelle in \[Richtlinientyp\] für die Direktive \[Direktiventyp\] bei \[Quell-URL\] -- Die Quelle wird ignoriert."                                                         | Die meisten CSP-Direktiven erfordern eine oder mehrere Inhaltsquellen \(Angabe einer URL, von der Inhalte geladen werden können\).  Dieser Fehler weist auf eine Richtlinie mit einer Direktive hin, die eine Quell-URL enthält, die beim Analysieren fehlgeschlagen ist.  | Prüfen Sie die Inhaltsquelle \(meistens eine URL\), die in der angegebenen Direktive definiert ist, die Sie im angegebenen Richtlinientyp finden.  Korrigieren oder ersetzen Sie die Quell-URL oder entfernen Sie die Direktive.  <br /> *\*Ihre Richtlinie sollte eine Direktive für eine default-src-Richtlinie enthalten, die ein Fallback für andere Ressourcentypen darstellt, wenn diese keine eigenen Richtlinien haben.* |
| CSP14303 | "Die Richtlinie [Richtlinientyp] war leer." | Der Richtlinientyp \(z. B. Inhaltssicherheitsrichtlinie im HTTP-Header\) ist leer.  | Eine Kurzübersicht zum Einrichten einer Inhaltssicherheitsrichtlinie finden Sie unter [http://content-security-policy.com](http://content-security-policy.com).  |
| CSP14304 | "Unbekannte Quelle \[Quell-URL\] für die Direktive \[Direktiventyp\] in \[Richtlinientyp\]. Die Quelle wird ignoriert." | Die in der Richtlinie genannten Quellen für genehmigte \(sichere\) Inhalte sind unbekannt und werden ignoriert.  | Überprüfen Sie die identifizierte Inhaltsquelle \(oft ist dies eine URL\), um sicherzustellen, dass sie korrekt ist.  |
| CSP14305 | "Nicht unterstützte Quelle \[Quell-URL\] für die Direktive [Direktiventyp] in \[Richtlinientyp\]. Die Quelle wird ignoriert." | Die in dieser Direktive aufgeführte Quelle \(URL, Schlüsselwort oder Daten) wird nicht unterstützt und ignoriert.  | Die Adresse der Quellseite kann einen optionalen führenden Platzhalter \(das Sternzeichen `*`\) enthalten.  Zum Beispiel http://`*`.foo.com oder mail.foo.com:*.  Die Hosts sind durch Leerzeichen getrennt.  Quellen können auch Schlüsselwörter \(keine, selbst, unsafe-inline und unsafe-eval werden alle unterstützt\) oder Daten \(Daten:URIs, Mediastream:URIs\) sein.  |
| CSP14306 | "Es wurden keine Quellen für die Direktive \[Direktiventyp\] für \[Ressourcen\] angegeben -- Dies entspricht der Verwendung von 'none' und verhindert, dass alle Ressourcen dieses Typs heruntergeladen werden." | Eine Direktive zu geben und keine Quellen für den Zugriff auf sichere Inhalte aufzulisten, ist dasselbe wie das Herunterladen von Ressourcen des in der Direktive angegebenen Typs nicht zu erlauben.  | Bei einer Quelle kann es sich um einen oder mehrere Internet-Hostnamen oder IP-Adressen sowie um ein optionales URL-Schema und/oder eine Portnummer handeln.  |
| CSP14307 | "Die Quelle [Quell-URL] wurde bereits für die Direktive \[Direktiventyp\] für \[Richtlinientyp\] bereitgestellt." | Eine doppelte Quelle \(URL, Schlüsselwort oder Daten\) wurde in dieser Direktive aufgeführt und wird ignoriert.  | Entfernen Sie die angegebene doppelte Quelle.  |
| CSP14308 | "Fehler beim Analysieren der Direktive in \[Richtlinientyp\] bei [Direktivename]". | Die identifizierte Richtlinie ist fehlgeschlagen.  Eine Anleitung zum Schreiben unterstützter Direktiven finden Sie unter [http://content-security-policy.com](http://content-security-policy.com/).  | Die Direktiven müssen durch Semikolons voneinander getrennt werden.  Wenn Sie z. B. eine Anwendung haben, die alle ihre Ressourcen aus einem Content Delivery Network \(z.B. `https://cdn.example.net`\) lädt, und Sie wissen, dass Sie keine gerahmten Inhalte oder Plug-Ins benötigen, könnte Ihre Richtlinie so aussehen: `Content-Security-Policy: default-src https://cdn.example.net; child-src 'none'; object-src 'none'.` *\*Während Direktiven durch Semikolons voneinander getrennt werden, sollten Quellen innerhalb einer Direktive nur durch ein Leerzeichen voneinander getrennt werden.* |
| CSP14309 | "Unbekannte Direktive in \[Direktivename\] in \[Richtlinientyp\] -- Die Direktive wird ignoriert." | Die in der CSP-Richtlinie festgelegte Direktive ist unbekannt und wird ignoriert.  | Eine Liste der unterstützten Direktiven finden Sie unter [http://content-security-policy.com](http://content-security-policy.com/).  |
| CSP14310 | "Nicht unterstützte Direktive [Direktivename] in \[Richtlinientyp] -- Die Direktive wird ignoriert." | Beim Analysieren wurde eine Direktive im Richtlinientyp \(z.B. das Header-Feld `Content-Security-policy-Report-Only`\) gefunden, die nicht unterstützt ist und ignoriert wird.  Unterstützte Direktiven finden Sie unter [http://content-security-policy.com](http://content-security-policy.com/).  | Entfernen Sie die nicht unterstützte Direktive.  **HINWEIS**: Einige Direktiven werden weder im Element \<meta\> noch im Header-Feld `Content-Security-policy-Report-Only` unterstützt.  |
| CSP14311 | "Die Direktive \[Direktivename\] wurde bereits in \[Richtlinientyp\] bereitgestellt -- Die doppelte Direktive wird ignoriert." | Beim Analysieren wurde eine doppelte Direktive gefunden. Die zweite Direktive und ihre Quell-Ausdrücke werden ignoriert.  | Entfernen Sie das doppelte Skript.  |
| CSP14312 | "Die Direktive [Direktivename] in [Richtlinientyp] wurde durch eine Ressource verletzt: [Ziel-URI].  Die Ressource wird blockiert." | In diesem Beispiel: "Ressource verletzte die Direktive 'script-src ms-appx: data: 'unsafe-eval' in der host-definierten Richtlinie: Inlineskript.  Die Ressource wird blockiert." | Ein Inlineskript \(Ziel-URI\) wurde aufgrund der Direktive `'script-src ms-appx: data: 'unsafe-eval'` in der Richtlinie "hostdefiniert" blockiert.  <br /> Autoren müssen alle Inlineskripts und Formatvorlagen aus der Reihe verschieben, da der Benutzer-Agent nicht feststellen kann, ob ein Inlineskript von einem Angreifer eingefügt wurde.  Entfernen Sie das Inlineskript, und platzieren Sie es in einer externen Datei.  |
| CSP14313 | "Die Direktive [Direktivename] in [Richtlinientyp] wurde durch eine Ressource verletzt: [Ziel-URI].  Die Ressource wird nicht blockiert, weil die Richtlinie "Nur-Bericht" ist." | Es wurde eine Ressource identifiziert, die gegen die im Header-Feld `Content-Security-policy-Report-Only` angegebene Richtlinie verstößt.  Da es sich um einen `Report-Only`-Richtlinientyp handelt, wird die Ressource nicht blockiert.  | Verschieben Sie die Direktive in ein Header-Feld für die Inhaltssicherheitsrichtlinie, wenn diese Ressource zum Schutz Ihrer Website blockiert werden soll.  |
| CSP14314 | "Fehler beim Senden des Berichts über die Richtlinienverletzung an [Ziel-URI]. Ursache: [Grund für den Abbruch des Vorgangs]." | Es gab ein Problem bei der Meldung einer Richtlinienverletzung, das Ziel, an das der Bericht geschickt werden soll, und der Grund für die Nichtübermittlung sollte ermittelt werden.  | Die Direktive `report-uri` gibt eine URL an, in der ein Browser Berichte sendet, wenn eine Inhaltssicherheitsrichtlinie verletzt wird.  *\*Es kann nicht in \<meta\>-Tags verwendet werden.* |
| CSP14315 | "Fehler beim Durchsetzen der Sandkastendirektive in [Richtlinientyp]. Ursache: [Grund für den Abbruch des Vorgangs]." | Die Sandkastendirektive ist aus den angegebenen Gründen fehlgeschlagen.  Diese Direktive legt Beschränkungen für Aktionen fest, die die Seite ausführen kann, anstatt für Ressourcen, die die Seite laden kann.  Wenn die Sandkastendirektive vorhanden ist, wird die Seite so behandelt, als wäre sie innerhalb eines iFrame geladen worden.  Sie kann Popups und Plug-Ins verhindern und die Skriptausführung blockieren.  | Halten Sie den Sandbox-Wert leer, um alle Beschränkungen aufrechtzuerhalten oder Werte hinzuzufügen: `allow-forms`, `allow-same-origin`, `allow-scripts` und `allow-top-navigation`.  *\*Die Sandkastendirektive wird weder im Element \<meta\> noch im Header-Feld `Content-Security-policy-Report-Only` unterstützt.* |
| CSP14316 | "Die Skriptauswertung ist aufgrund einer Hostüberschreibung zulässig." | Wenn entweder die Direktive `script-src` oder `default-src` enthalten ist, werden Inlineskript und `eval()` deaktiviert, es sei denn, Sie geben `unsafe-inline` und `unsafe-eval` an.  | `'unsafe-eval'` Ermöglicht die Verwendung von `eval()` und ähnliche Methoden zum Erstellen von Code aus Zeichenfolgen.  Sie müssen die einfachen Anführungszeichen ebenfalls angeben.  ***HINWEIS**: Dies ist unsicher und kann Ihre Website für websiteübergreifende Skripting-Schwachstellen öffnen.* |
| CSP14317 | "Frame [Quellname] ist aufgrund einer Hostüberschreibung zulässig." | Der identifizierte Quell-Frame wurde aufgrund einer in der Host-CSP-Richtlinie festgelegten Außerkraftsetzung zugelassen.  | Eine Richtlinie kann einen Ausdruck enthalten, der keine Quelle ist, was bedeutet, dass die Quelle nur einmal verwendet werden kann und der Server bei jeder Übertragung einer Richtlinie einen neuen Wert für die Richtlinie generieren muss.  In diesem Fall werden die Einschränkungen in der Direktive, in der Sie anwesend sind, außer Kraft gesetzt.  |

> [!NOTE]
> Bei Websites in der vertrauenswürdigen Sicherheitszone eines Benutzers prüft Microsoft Edge nicht den MIME-Typ eines Stylesheets.  

## CSS-Codes  

Diese Fehler liegen im CSS31xx-Format vor und stehen im Zusammenhang mit *Web Open Font Format* \(WOFF\) und *Embedded OpenType* \(EOT\) Schriftart- und Hostserver-Probleme.  

| Code | Meldung | Beschreibung | Empfohlene Problemlösung |
|:--- |:--- |:--- |:--- |
| CSS3111 | "Unbekannter Fehler in "@font-face"." | Ein unbekanntes Problem wurde mit dem "Web Open Font Format \(WOFF\)" und der "Embedded OpenType-Schriftart \(EOT\)" der Cascading Stylesheets \(CSS\) Schriftart festgestellt.  | Überprüfen Sie die Quelle der WOFF-Schriftarten.  Versuchen Sie eine alternative Schriftart oder Quelle, um zu sehen, ob Sie das Problem reproduzieren können.  |
| CSS3112 | "Fehler bei der WOFF-Integritätsprüfung in "@font-face"." | Die Schriftart "Web Open Font Format \(WOFF\)" könnte beschädigt, unvollständig oder nicht das richtige Format sein.  | Überprüfen Sie die Quelle der Schriftarten.  Versuchen Sie eine bekannte gute Schriftart oder Quelle, um zu sehen, ob Sie das Problem reproduzieren können.  |
| CSS3113 | "Nichtübereinstimmung zwischen Dokumentursprung und EOT-Stammzeichenfolge in "@font-face"." | Die Schriftart kann nicht verwendet werden, weil die URL\(Stammzeichenfolge\) in der Schriftart Embedded OpenType \(EOT\) nicht mit der Domäne des Dokuments übereinstimmt, das die Schriftart verwendet.  | Die URL-Prüfsumme in der EOT-Stammzeichenfolge ist möglicherweise falsch, was auf eine beschädigte oder geänderte URL für die Schriftart hinweist.  Stellen Sie sicher, dass die Schriftart für die Website, auf der sie verwendet wird, lizenziert ist oder über entsprechende Genehmigungen verfügt.  |
| CSS3114 | "Fehler bei der Berechtigungsprüfung für die OpenType-Einbettung in "@font-face".  Die Berechtigung muss "Installable" sein." | Die Schriftart hat keine Berechtigungen zur Installation mit der aktuellen Webseite.  | Besorgen Sie sich die richtige(n) Berechtigung(en) für die Einbettung der Schriftart.  |
| CSS3115 | "Ungültige OpenType-Schriftart kann in "@font-face" nicht geladen werden." | Die Schriftart ist für diese Verwendung ungültig.  | Besorgen Sie sich die Berechtigung oder Lizenzen für die aktuelle und gültige Schriftart.  |
| CSS3116 | "Fehler bei der ursprungsübergreifenden Anforderung in "@font-face".  Kein Header vom Typ "Access-Control-Allow-Origin"." | Die Schriftart ist möglicherweise nicht für den domänenübergreifenden Zugriff konfiguriert.  | Die Schriftart wird nicht vom gleichen Ursprung wie das Dokument bereitgestellt.  Stellen Sie sicher, dass der Host, der die Schriftart bereitstellt, die Verwendung dieser Schriftart durch Verwendung des HTTP-Headers "Access-Control-Allow-Origin" zulässt.                        |
| CSS3117 | "Fehler bei der ursprungsübergreifenden Anforderung in "@font-face".  Der Ressourcenzugriff ist eingeschränkt." | Der Header "Access-Control-Allow-Origin" ist möglicherweise nicht korrekt konfiguriert, oder der Schriftart-Host erlaubt möglicherweise nicht, dass diese Schriftart von Ihrer Seite verwendet wird.  | Stellen Sie sicher, dass die Ressource über die richtigen Berechtigungen und einen korrekt konfigurierten HTTP-Antwortheader verfügt, der den domänenübergreifenden Zugriffsursprung auf dem Host hat, der die Schriften bereitstellt.  |
| CSS3118 | "Fehler beim Erstellen eines neuen Stylesheets.  Das Dokument enthält mehr als \[Maximum\] Stylesheets." | Microsoft Edge hat beim Rendering Ihrer Seite mehr als 4095 Stylesheet-Objekte erstellt.  | Dies kann ein außer Kontrolle geratener JavaScript-Prozess oder ein Build-Systemfehler sein.  Verringern Sie die Anzahl von Stylesheet-Objekten, die generiert werden.  |
| CSS3119 | "Die Medienabfrage "-ms-view-state" ist veraltet.  Medienabfragen vom Typ "-ms-view-state" werden in Versionen nach Windows 8.1 ggf. geändert oder sind nicht mehr verfügbar.  Verwenden Sie stattdessen Abfragen vom Typ "max-width" und "min-width"." | Ihr CSS enthält eine `-ms-view-state`-Medienabfrage.  | Verwenden Sie "max-width" und "min-width".  |

## HTML-Codes

Diese Codes liegen im Format HTML1xxx vor, wie z. B. HTML1115.  Die meisten davon sind Legacy-Codes, die spezifisch für Internet Explorer-Konzepte wie *Dokumentmodus* und *Kompatibilitätsansicht* sind.  

| Code | Meldung | Beschreibung | Empfohlene Problemlösung |  
| :--- |:--- |:--- |:--- |  
| HTML1112 | "Neustart der Codepage von \[Codierung\] zu \[Codierung\]" | Es wurde eine Codepage angegeben, die sich von der Codepage des Servers unterscheidet.  | Verwenden Sie die gleiche Codepage wie der Server, um diesen Fehler zu vermeiden.  |  
| HTML1113 | "Neustart des Dokumentmodus von \[Modus\] zu \[Modus\]" | Die Webseite erfordert einen anderen Dokumentmodus als den, auf den der Browser derzeit eingestellt ist.  | Diese Meldung kann auftreten, wenn der Benutzer von einer anderen Seite aus browst, so dass es außerhalb der Kontrolle des Entwicklers liegt.  |  
| HTML1114 | "Die Codepage \[Codierung\] von \[Domäne\] überschreibt die Konflikte verursachende Codepage \[Codierung\] von \[Domäne\]." | Die in den Headern HTTP \(from server\) und HTML \(in-page\) angegebenen Codepages unterscheiden sich voneinander.  | Ändern Sie eins, damit Sie übereinstimmen.  |  
| HTML1115 | "Das X-UA-kompatible META-Tag \(`[META tag]`\) wurde ignoriert, weil der Dokumentmodus bereits fertig gestellt ist." | Normalerweise wurde das META-Tag nach einer "Script"- oder "Style"-Deklaration platziert, wodurch der Dokumentenmodus für die Seite festgelegt wurde.  | Verschieben Sie das X-UA-kompatible META-Tag so früh wie möglich in den Header.  Es ist eine gute Praxis, es unmittelbar nach dem \<title\> und dem Zeichensatz-Wert zu setzen.  |  
| HTML1116 | "Das X-UA-kompatible META-Tag \(`[META tag]`\) wurde aufgrund eines früheren X-UA-kompatiblen META-Tags \(`[META tag]`\) ignoriert." | Es gibt mehr als einen "X-UA-kompatiblen" "META"-Tag im Abschnitt \<head\> des Quellcodes.  | Entfernen Sie alle bis auf ein "X-UA-kompatibles META"-Tag und stellen Sie sicher, dass es so früh wie möglich in den Header eingefügt wird.  Es ist eine gute Praxis, es unmittelbar nach dem \<title\> und dem Zeichensatz-Wert zu setzen.  |  
| HTML1121 | "Codepage \[Codierung\] ist nicht zulässig, nur Codepage \[Codierung\] ist zulässig." | Der Inhalt der Webseite rief eine Zeichencodierung hervor, die in diesem Zusammenhang nicht zulässig ist.  | Stellen Sie sicher, dass alle Inhalte die erlaubte Codierung verwenden, die in der Nachricht angegeben ist.  |  
| HTML1122 | "Internet Explorer wird im Unternehmensmodus mit der Emulation von IE8 ausgeführt" | Die Seite wird derzeit im Unternehmensmodus gerendert, der eine Emulation von Windows Internet Explorer 8 ist.  | Dieser Modus wird vom IT-Management für bestimmte Websites konfiguriert.  Wenn ein einzelner Benutzer sie auf einer Webseite ausschalten muss, deaktivieren Sie die Option "Unternehmensmodus" im Menü "Extras".  Weitere Informationen zum Verwalten des Unternehmensmodus finden Sie unter [IT-Dokumentation](https://technet.microsoft.com/library/dn640687.aspx).  |  
| HTML1201 | "`[domain]` ist eine Website, die zur Kompatibilitätsansicht hinzugefügt haben." | Der Benutzer hat die Schaltfläche **Kompatibilitätsansicht** für die aktuelle Website ausgewählt oder sie über die Einstellungen der **Kompatibilitätsansicht** hinzugefügt.  | Vom Benutzer initiiert.  |  
| HTML1202 | "`[domain]` wird in der Kompatibilitätsansicht ausgeführt, weil "Alle Websites in Kompatibilitätsansicht anzeigen" aktiviert ist." | Der Benutzer hat das Kontrollkästchen **Intranet-Websites in Kompatibilitätsansicht anzeigen** in den Einstellungen der **Kompatibilitätsansicht**.  | Der Benutzer muss Alt+T drücken, Einstellungen der **Kompatibilitätsansicht** wählen und dann das Kontrollkästchen **Intranet-Websites in Kompatibilitätsansicht anzeigen** deaktivieren.  |  
| HTML1203 | "`[domain]` wurde über eine Gruppenrichtlinie für die Ausführung in der Kompatibilitätsansicht konfiguriert." | Der Netzwerkadministrator hat festgelegt, dass die Webseite in der Kompatibilitätsansicht ausgeführt wird.  | Wenden Sie sich an den Netzwerkadministrator.  |  
| HTML1204 | "`[domain]` wird in der Kompatibilitätsansicht ausgeführt, weil "Alle Websites in Kompatibilitätsansicht anzeigen" aktiviert ist." | Der Benutzer hat das Kontrollkästchen **Alle Websites in Kompatibilitätsansicht anzeigen** in den Einstellungen der **Kompatibilitätsansicht**.  | Der Benutzer muss Alt+T drücken, Einstellungen der **Kompatibilitätsansicht** wählen und dann das Kontrollkästchen **Alle Websites in Kompatibilitätsansicht anzeigen** deaktivieren.  |  
| HTML1300 | "Navigation wurde ausgeführt" | Es wurde zu einer neuen Seite navigiert, oder die aktuelle Seite wurde aktualisiert.  | Dies ist eine informative Meldung, keine Fehlermeldung.  |  

## HTML5-Parser-Warnungen  

Die folgenden Warnungen können als Teil der Validierung auftreten, die während der HTML-Analyse durchgeführt wird.  Diese Warnungen bedeuten nicht unbedingt, dass eine Seite fehlerhaft ist, sondern dass das bereitgestellte HTML nach dem HTML5-Standard ungültig ist.  Inhalte, die in Übereinstimmung mit früheren Versionen der HTML- oder XHTML-Spezifikationen erstellt wurden, sind möglicherweise in HTML5 nicht gültig, insbesondere im Hinblick auf die Verwendung von DOCTYPEs.

Diese Warnungen weisen häufig auf fehlende oder zusätzliche Zeichen und nicht übereinstimmende Tags hin.  Wenn Sie diese Warnungen beheben, sollte sich die Kompatibilität mit älteren Browsern und die Übereinstimmung einer Webseite mit dem HTML5-Standard verbessern.  Um die Quelle einer Warnung leichter identifizieren zu können, enthält sie Zeilen- und Zeichenversatzinformationen sowie einen Link, der zum Speicherort des Problems verweist.

| Code     | Meldung |  
| :--- |:--- |  
| HTML1400 | "Unerwartetes Zeichen am Start der numerischen Zeichenreferenz.  Erwartet [0-9]." |  
| HTML1401 | "Unerwartetes Zeichen am Start der hexadezimalen numerischen Zeichenreferenz.  Erwartet [0-9], [a-f] oder [A-F]." |  
| HTML1402 | "In der Zeichenreferenz fehlt ein Endsemikolon ";"." |  
| HTML1403 | "Die numerische Zeichenreferenz wurde nicht in ein gültiges Zeichen aufgelöst." |  
| HTML1404 | "Unbekannte benannte Zeichenreferenz." |  
| HTML1405 | "Ungültiges Zeichen: U+0000 NULL.  NULL-Zeichen sollten nicht verwendet werden." |  
| HTML1406 | "Ungültiger Markierungsanfang: \<\?.  Fragezeichen sollten nicht den Anfang von Markierungen bilden." |  
| HTML1407 | "Ungültiger Markierungsname.  Das erste Zeichen sollte der Zeichenfolge [a-zA-Z] entsprechen." |  
| HTML1408 | "Ungültige Endmarkierung\</\>.  Endmarkierungen sollten nicht leer sein." |  
| HTML1409 | "Ungültiges Attributnamenzeichen.  Attributnamen sollten nicht \(\"\), \(\'\), \(\<\), oder \(=\) enthalten." |  
| HTML1410 | "Ungültiger Attributwert ohne Anführungszeichen.  Die Attributwerte ohne Anführungszeichen sollten nicht \(\"\), \(\'\), \(\<\), \(=\), oder \(\`\) enthalten. |  
| HTML1411 | "Unerwartetes Dateiende." |  
| HTML1412 | "Falsch formatierter Kommentar.  Kommentare sollten mit \<\!-- \> beginnen." |  
| HTML1413 | "Unerwartetes Zeichen: U+003E GRÖSSER-ALS-ZEICHEN \(\>\)" |  
| HTML1414 | "Unerwartetes Zeichen: U+0021 AUSRUFEZEICHEN \(\!\)" |  
| HTML1415 | "Unerwartetes Zeichen: U+002D BINDESTRICH-MINUS \(-\)" |  
| HTML1416 | "Unerwartetes Zeichen im Kommentarende.  Erwartet "--\>"." |  
| HTML1417 | "Leerer DOCTYPE.  Der kürzeste gültige Dokumenttyp (doctype) ist \<\!DOCTYPE html\>." |  
| HTML1418 | "Unerwartetes Zeichen in DOCTYPE." |  
| HTML1419 | "Unerwartetes Schlüsselwort in DOCTYPE.  Erwartet: "PUBLIC" oder "SYSTEM"." |  
| HTML1420 | "Unerwartetes Anführungszeichen nach dem Schlüsselwort "PUBLIC" oder "SYSTEM".  Ein Leerzeichen wurde erwartet." |  
| HTML1421 | "Falsch formatierte Endmarkierung.  Endmarkierungen sollten keine Attribute enthalten." |  
| HTML1422 | "Falsch formatierte Startmarkierung.  Auf einen selbstschließenden Schrägstrich sollte ein U+003E GRÖSSER-ALS-ZEICHEN (>) folgen." |  
| HTML1423 | "Falsch formatierte Startmarkierung.  Attribute sollten durch Leerzeichen voneinander getrennt werden." |  
| HTML1424 | "Ungültiges Zeichen   " |  
| HTML1500 | "Die Markierung kann nicht selbstschließend sein.  Verwenden Sie eine explizite schließende Markierung." |  
| HTML1501 | "Unerwartetes Dateiende." |  
| HTML1502 | "Unerwarteter DOCTYPE.  Nur ein DOCTYPE ist zulässig, und er muss vor allen Elementen stehen." |  
| HTML1503 | "Unerwartete Startmarkierung." |  
| HTML1504 | "Unerwartete Endmarkierung." |  
| HTML1505 | "Unerwartetes Zeichentoken." |  
| HTML1506 | "Unerwartetes Token." |  
| HTML1507 | "Unerwartetes Zeichen: U+0000 NULL.  NULL-Zeichen sollten nicht verwendet werden." |  
| HTML1508 | "Endmarkierung ohne Entsprechung." |  
| HTML1509 | "Endmarkierung ohne Entsprechung." |  
| HTML1510 | "Die erforderlichen Knoten sind nicht im Bereich enthalten." |  
| HTML1511 | "Unerwartetes Element auf Kopfebene außerhalb von \<head\> gefunden." |  
| HTML1512 | "Endmarkierung ohne Entsprechung." |  
| HTML1513 | "Zusätzliche \<html\>-Markierung gefunden.  Pro Dokument sollte nur eine \<html\>-Markierung vorhanden sein." |  
| HTML1514 | "Zusätzliche \<body\>-Markierung gefunden.  Pro Dokument sollte nur eine \<body\>-Markierung vorhanden sein." |  
| HTML1515 | "\<frameset\> wurde zu weit unten im Dokument gefunden.  Diese Markierung sollte sich an einer Stelle befinden, die vor einer neu zu erstellenden \<body\>-Markierung liegt." |  
| HTML1516 | "Ungültige Schachtelung.  Eine Kopfzeilenmarkierung wie \<h1\> oder \<h2\> sollte nicht in einer anderen Kopfzeilenmarkierung platziert werden." |  
| HTML1517 | "Ungültige Schachtelung.  Eine \<form\>-Markierung sollte nicht in einer anderen \<form\>-Markierung platziert werden." |  
| HTML1518 | "Ungültige Schachtelung.  Eine \<button\>-Markierung sollte nicht in einer anderen \<button\>-Markierung platziert werden." |  
| HTML1519 | "Ungültige Schachtelung.  Eine \<a\>-Markierung sollte nicht in einer anderen \<a\>-Markierung platziert werden." |  
| HTML1520 | "Unerwartete Startmarkierung: Das \<isindex\>-Element ist veraltet und sollte nicht verwendet werden." |  
| HTML1521 | "Unerwartete \</body\>-Markierung oder Dateiende.  Alle geöffneten Elemente sollten vor dem Ende des Dokuments geschlossen werden. " |  
| HTML1522 | "Ungültige Endmarkierung: \</br\>.  Verwenden Sie stattdessen \<br\> oder \<br /\>." |  
| HTML1523 | "Überlappende Endmarkierung.  Markierungen sollten im Format \<b\>\<i\>\</i\>\</b\> anstatt im Format \<b\>\<i\>\</b\>\</i\> strukturiert werden." |  
| HTML1524 | "Ungültiger DOCTYPE.  Der kürzeste gültige Dokumenttyp (doctype) ist \<\!DOCTYPE html\>." |  
| HTML1525 | "Unerwartete HTML-Markierung wurde in Fremdinhalt \(MathML/SVG\) gefunden." |  
| HTML1526 | "Ungültige Schachtelung.  Eine \<nobr\>-Markierung sollte nicht in einer anderen \<nobr\>-Markierung platziert werden." |  
| HTML1527 | "DOCTYPE erwartet.  Der kürzeste gültige Dokumenttyp (doctype) ist \<\!DOCTYPE html\>." |  
| HTML1528 | "Unerwartetes Element \<image\> in HTML-Inhalt.  Verwenden Sie stattdessen \<img\>." |  
| HTML1529 | "Ungültiger xmlns:xlink-Attributwert.  Der Wert muss "\<https://w3.org/1999/xlink\>" sein." |  
| HTML1530 | "Text in einem Strukturtabellenelement gefunden.  Tabellentext darf nur in die Elemente \<caption\>, \<td\> oder \<th\> gesetzt werden." |  
| HTML1531 | "Ungültiger xmlns-Attributwert.  Für SVG-Elemente muss der Wert "\<https://w3.org/2000/svg/\>" sein." |  
| HTML1532 | "Ungültiger xmlns-Attributwert.  Für MathML-Elemente muss der Wert "\<https://w3.org/1998/Math/MathML/\>" sein."  |  

## HTTP-Codes  

HTTP-Fehlercodes werden als Antwort auf Anfragen von entfernten Servern zurückgegeben.  Die wohl bekannteste ist HTTP404, die immer dann zurückgegeben wird, wenn der Server die im Uniform Resource Identifier \(URI\) angegebene Seite oder das Dokument nicht finden kann.


| Code | Meldung | Beschreibung |  
| :--- |:--- |:--- |  
| HTTP400 | UNGÜLTIGE ANFORDERUNG | Die Anforderung konnte vom Server aufgrund einer ungültigen Syntax nicht verarbeitet werden.  |  
| HTTP401 | VERWEIGERT | Für die angeforderte Ressource ist eine Benutzerauthentifizierung erforderlich.  |  
| HTTP402 | ZAHLUNG IST ERFORDERLICH | Derzeit nicht im HTTP-Protokoll implementiert.  |  
| HTTP403 | VERBOTEN | Die Anforderung wurde vom Server gelesen, ihre Verarbeitung ist jedoch nicht zulässig.  |  
| HTTP404 | NICHT GEFUNDEN | Der Server hat keine Übereinstimmungen für den angeforderten URI (Uniform Resource Identifier) gefunden.  |  
| HTTP405 | UNGÜLTIGE METHODE | Das verwendete HTTP-Verb ist nicht zulässig.  |  
| HTTP406 | ALLE UNZULÄSSIG | Es wurden keine für den Client zulässigen Antworten gefunden.  |  
| HTTP407 | PROXYAUTHENTIFIZIERUNG IST ERFORDERLICH | Proxyauthentifizierung ist erforderlich.  |  
| HTTP408 | ANFORDERUNGSTIMEOUT | Das Zeitlimit wurde beim Warten auf die Anforderung vom Server überschritten.  |  
| HTTP409 | KONFLIKT | Die Anforderung konnte aufgrund eines Konflikts mit dem aktuellen Status der Ressource nicht erfüllt werden. Die Anforderung muss erneut mit weiteren Informationen gestellt werden.  |  
| HTTP410 | NICHT VORHANDEN | Die angeforderte Ressource ist auf dem Server nicht mehr verfügbar. Ein Weiterleitungsziel ist nicht bekannt.  |  
| HTTP411 | LÄNGE IST ERFORDERLICH | Der Server verweigert die Annahme von Anforderungen, für die keine Inhaltslänge definiert wurde.  |  
| HTTP412 | FEHLER BEI VORBEDINGUNG | Die in mindestens einem Anforderungsheaderfeld angegebene Vorbedingung wurde vom Server als falsch bewertet.  |  
| HTTP413 | NUTZLAST ZU GROSS | Der Server verarbeitet eine Anforderung nicht, weil die Anforderungsentität größer ist als auf dem Server zulässig oder unterstützt.  |  
| HTTP414 | URI ZU LANG | Der Server verarbeitet die Anforderung nicht, weil der Anforderungs-URI (Uniform Resource Identifier) größer ist als auf dem Server zulässig.  |  
| HTTP415 | NICHT UNTERSTÜTZTER MEDIENTYP | Der Server verarbeitet die Anforderung nicht, da das Format der Anforderungsentität von der angeforderten Ressource mit der angeforderten Methode nicht unterstützt wird.  |  
| HTTP416 | ANGEFORDERTER BEREICH KANN NICHT ERFÜLLT WERDEN | Der vom Client angeforderte Teil der Datei kann vom Server nicht bereitgestellt werden.  Der Bereich erstreckt sich möglicherweise über das Dateiende hinaus.  |  
| HTTP417 | FEHLER BEI ERWARTUNG | Die im Erwartungsheaderfeld angegebene Erwartung konnte vom Server nicht erfüllt werden.  |  
| HTTP418 | TEEKANNE | Der Server ist eine Teekanne und kann keinen Kaffee bereiten.  |  
| HTTP419 | AUTHENTIFIZIERUNGSTIMEOUT | Die zuvor gültige Authentifizierung ist abgelaufen.  |  
| HTTP422 | ENTITÄT KANN NICHT VERARBEITET WERDEN | Die Anforderung war wohlgeformt, konnte aufgrund semantischer Fehler jedoch nicht verarbeitet werden.  |  
| HTTP423 | GESPERRT | Die Ressource, auf die zugegriffen wird, ist gesperrt.  |  
| HTTP424 | ABHÄNGIGKEITSFEHLER | Anforderungsfehler aufgrund eines Fehlers bei einer früheren Anforderung.  |  
| HTTP426 | UPGRADE ERFORDERLICH | Der Client muss zu einem anderen Protokoll wechseln.  |  
| HTTP428 | VORBEDINGUNG ERFORDERLICH | Der Ursprungsserver erfordert eine bedingte Anforderung.  |  
| HTTP429 | ZU VIELE ANFORDERUNGEN | Der Server verweigert die Verarbeitung der Anforderung, weil der Client zu viele Anforderungen gesendet hat.  |  
| HTTP431 | ANFORDERUNGSHEADER ZU GROSS | Der Server verweigert die Verarbeitung der Anforderung, weil ein Headerfeld oder alle Headerfelder zusammen größer sind als vom Server verarbeitet werden können.  |  
| HTTP449 | ERNEUT VERSUCHEN MIT | Die Anforderung sollte nach dem Ausführen der entsprechenden Aktion erneut versucht werden.  |  
| HTTP500 | SERVERFEHLER | Es ist ein unerwarteter Zustand aufgetreten, sodass der Server die Anforderung nicht erfüllen kann.  |  
| HTTP501 | NICHT UNTERSTÜTZT | Die Funktion, die zum Erfüllen der Anforderung erforderlich ist, wird vom Server nicht unterstützt.  |  
| HTTP502 | UNGÜLTIGES GATEWAY | Beim Fungieren als Gateway oder Proxyserver hat der Server bei der Anforderungsverarbeitung vom Upstreamserver eine ungültige Antwort erhalten.  |  
| HTTP503 | DIENST NICHT VERFÜGBAR | Der Dienst ist zurzeit überlastet.  |  
| HTTP504 | GATEWAYTIMEOUT | Beim Warten auf ein Gateway ist ein Anforderungstimeout aufgetreten.  |  
| HTTP505 | NICHT UNTERSTÜTZTE VERSION | Der Server unterstützt die in der Anforderungsnachricht verwendete HTTP-Protokollversion nicht, oder sie ist für ihn nicht zulässig.  |  
| HTTP506 | VARIANTE HANDELT AUCH AUS | Die transparente Inhaltsaushandlung für die Anforderung hat Zirkelbezüge verursacht.  |  
| HTTP507 | UNZUREICHENDER SPEICHER | Der Server kann die zum Abschließen der Anforderung erforderliche Darstellung nicht speichern.  |  
| HTTP508 | SCHLEIFE FESTGESTELLT | Der Server hat beim Verarbeiten der Anforderung eine Endlosschleife erkannt.  |  
| HTTP510 | NICHT ERWEITERT | Damit der Server die Anforderung erfüllen kann, sind zusätzliche Erweiterungen erforderlich.  |  
| HTTP511 | NETZWERKAUTHENTIFIZIERUNG ERFORDERLICH | Der Client muss sich authentifizieren, um Netzwerkzugriff zu erhalten.  |  

## JavaScript-Syntaxfehler  

JavaScript-Syntaxfehler treten auf, wenn die Struktur einer Ihrer Anweisungen gegen eine oder mehrere syntaktische Regeln verstößt.  

| Fehlernummer | Beschreibung |  
| --- | --- |  
| 1019 | ['break' außerhalb einer Schleife nicht möglich](/scripting/javascript/misc/can-t-have-break-outside-of-loop) |  
| 1020 | ['continue' außerhalb einer Schleife nicht möglich](/scripting/javascript/misc/can-t-have-continue-outside-of-loop) |  
| 1030 | [Bedingte Kompilierung ist ausgeschaltet](/scripting/javascript/misc/conditional-compilation-is-turned-off) |  
| 1027 | ['default' kann nur einmal in einer 'switch'-Anweisung auftreten](/scripting/javascript/misc/default-can-only-appear-once-in-a-switch-statement) |  
| 1005 | ['\(' erwartet](/scripting/javascript/misc/expected-left-parenthesis-javascript) |  
| 1006 | ['\)' erwartet](/scripting/javascript/misc/expected-right-parenthesis-javascript) |  
| 1012 | ['/' erwartet](/scripting/javascript/misc/expected-minus) |  
| 1003 | [':' erwartet](/scripting/javascript/misc/expected-colon) |  
| 1004 | [';' erwartet](/scripting/javascript/misc/expected-semicolon) |  
| 1032 | ['@' erwartet](/scripting/javascript/misc/expected-at) |  
| 1029 | ['@end' erwartet](/scripting/javascript/misc/expected-at-end) |  
| 1007 | ['\]' erwartet](/scripting/javascript/misc/expected-right-square-bracket) |  
| 1008 | ['{' erwartet](/scripting/javascript/misc/expected-left-curly-brace) |  
| 1009 | ['}' erwartet](/scripting/javascript/misc/expected-right-curly-brace) |  
| 1011 | ['=' erwartet](/scripting/javascript/misc/expected-equal-javascript) |  
| 1033 | ['catch' erwartet](/scripting/javascript/misc/expected-catch) |  
| 1031 | [Konstante erwartet](/scripting/javascript/misc/expected-constant) |  
| 1023 | [Hexadezimalziffer erwartet](/scripting/javascript/misc/expected-hexadecimal-digit) |  
| 1010 | [Bezeichner erwartet](/scripting/javascript/misc/expected-identifier-javascript) |  
| 1028 | [Bezeichner, Zeichenfolge oder Zahl erwartet](/scripting/javascript/misc/expected-identifier-string-or-number) |  
| 1024 | ['while' erwartet](/scripting/javascript/misc/expected-while) |  
| 1014 | [Ungültiges Zeichen](/scripting/javascript/misc/invalid-character-javascript) |  
| 1026 | [Marke nicht gefunden](/scripting/javascript/misc/label-not-found) |  
| 1025 | [Marke neu definiert](/scripting/javascript/misc/label-redefined) |  
| 1018 | ['return'-Anweisung außerhalb einer Funktion](/scripting/javascript/misc/return-statement-outside-of-function) |  
| 1002 | [Syntaxfehler](/scripting/javascript/misc/syntax-error-javascript) |  
| 1035 | ["Throw" muss gefolgt sein von einem Ausdruck auf derselben Quellzeile](/scripting/javascript/misc/throw-must-be-followed-by-an-expression-on-the-same-source-line) |  
| 1016 | [Nicht abgeschlossener Kommentar](/scripting/javascript/misc/unterminated-comment) |  
| 1015 | [Nicht abgeschlossene Zeichenfolgenkonstante](/scripting/javascript/misc/unterminated-string-constant-javascript) |  
  
### Script Host-Fehler  

Die folgenden Fehler beziehen sich auf den Script Host, aber sie können gelegentlich auftreten:  
  
| Fehler | HRESULT | Beschreibung |  
| ---| --- | --- |  
| SCRIPT_E_RECORDED | 0x86664004 | Es wurde ein Fehler aufgezeichnet und zwischen Skriptmodul und Host weitergegeben.  Der Host muss den Fehlercode an den Aufrufer übergeben.  |  
| SCRIPT_E_REPORTED | 0x80020101 | Das Skriptmodul hat dem Host über IActiveScriptSite::OnScriptError einen Ausnahmefehler gemeldet, der nicht behandelt wurde.  Der Host kann diesen Fehler ignorieren.  |  
| SCRIPT_E_PROPAGATE | 0x8002010 | Ein Skriptfehler, der an den Aufrufer weitergegeben wird, befindet sich möglicherweise in einem anderen Thread.  Der Host sollte den Fehlercode an den Aufrufer übergeben.  |  

## JavaScript-Laufzeitfehler

JavaScript-Laufzeitfehler treten auf, wenn Ihr Skript versucht, eine Aktion auszuführen, die das System nicht ausführen kann.  Möglicherweise treten Laufzeitfehler auf, wenn variable Ausdrücke ausgewertet werden oder wenn Arbeitsspeicher belegt wird.

| Fehlernummer | Beschreibung |  
| --- | --- |  
| 5 | [Zugriff verweigert](/scripting/javascript/misc/access-is-denied) |  
| 438 | [Das Objekt unterstützt diese Eigenschaft oder Methode nicht.](/scripting/javascript/misc/object-doesn-t-support-this-property-or-method) |  
| 1001 | Nicht genügend Arbeitsspeicher. |  

### Windows-Runtime-Fehler  

 Wenn Sie APIs von Windows-Runtime \(WinRT\) verwenden, werden möglicherweise JavaScript-Fehler angezeigt, die aus Windows-Runtime-HRESULTs konvertiert wurden.  Windows-Runtime-HRESULTs im Bereich von über 0x80070000 werden in JavaScript-Fehler umgewandelt, indem der hexadezimale Wert der niedrigen Bits genommen und in einen Dezimalwert umgewandelt wird.  Beispielsweise wird das HRESULT 0x80070032 in den Dezimalwert 50 umgewandelt, und der JavaScript-Fehler lautet SCRIPT50.  Das HRESULT 0x80074005 wird in den Dezimalwert 16389 umgewandelt, und der JavaScript-Fehler lautet SCRIPT16389.

| Fehlernummer | Beschreibung |  
| --- | --- |  
| 5029 | [Die Arraylänge muss eine finite positive Ganzzahl sein](/scripting/javascript/misc/array-length-must-be-a-finite-positive-integer) |  
| 5030 | [Der Arraylänge muss eine finite positive Zahl zugewiesen sein](/scripting/javascript/misc/array-length-must-be-assigned-a-finite-positive-number) |  
| 5028 | [Array- oder Arguments-Objekt erwartet](/scripting/javascript/misc/array-or-arguments-object-expected) |  
| 5010 | [Boolesch erwartet](/scripting/javascript/misc/boolean-expected) |  
| 5003 | [Kann dem Ergebnis einer Funktion nicht zugewiesen werden](/scripting/javascript/misc/cannot-assign-to-a-function-result) |  
| 5000 | [Zuweisung an 'this' nicht möglich](/scripting/javascript/misc/cannot-assign-to-this) |  
| 5034 | [Zirkelverweis wird im Wertargument nicht unterstützt](/scripting/javascript/misc/circular-reference-in-value-argument-not-supported) |  
| 5006 | [Datumsobjekt erwartet](/scripting/javascript/misc/date-object-expected) |  
| 5015 | [Enumeratorobjekt erwartet](/scripting/javascript/misc/enumerator-object-expected) |  
| 5022 | [Annahme ausgelöst und nicht aufgefangen](/scripting/javascript/misc/exception-thrown-and-not-caught) |  
| 5020 | [Erwartet ')' in regulärem Ausdruck](/scripting/javascript/misc/expected-right-parenthesis-in-regular-expression-javascript) |  
| 5019 | [Erwartet '&#93;' in regulärem Ausdruck](/scripting/javascript/misc/expected-right-square-bracket-in-regular-expression-javascript) |  
| 5023 | [Die Funktion hat kein gültiges Prototyp-Objekt](/scripting/javascript/misc/function-does-not-have-a-valid-prototype-object) |  
| 5002 | [Funktion erwartet](/scripting/javascript/misc/function-expected) |  
| 5008 | [Ungültige Zuweisung](/scripting/javascript/misc/illegal-assignment-javascript) |  
| 5021 | [Ungültiger Bereich im Zeichensatz](/scripting/javascript/misc/invalid-range-in-character-set-javascript) |  
| 5035 | [Ungültiges Ersetzungsargument](/scripting/javascript/misc/invalid-replacer-argument) |  
| 5014 | [JavaScript-Objekt erwartet](/scripting/javascript/misc/javascript-object-expected) |  
| 5001 | [Zahl erwartet](/scripting/javascript/misc/number-expected) |  
| 5007 | [Objekt erwartet](/scripting/javascript/misc/object-expected) |  
| 5012 | [Objektmitglied erwartet](/scripting/javascript/misc/object-member-expected) |  
| 5016 | [Regulärer Ausdruck als Objekt erwartet](/scripting/javascript/misc/regular-expression-object-expected) |  
| 5005 | [Zeichenfolge erwartet](/scripting/javascript/misc/string-expected) |  
| 5017 | [Syntaxfehler in regulärem Ausdruck](/scripting/javascript/misc/syntax-error-in-regular-expression-javascript) |  
| 5026 | [Die Anzahl der Bruchstellen befindet sich außerhalb des gültigen Bereichs.](/scripting/javascript/misc/the-number-of-fractional-digits-is-out-of-range) |  
| 5027 | [Die Präzision befindet sich außerhalb des gültigen Bereichs.](/scripting/javascript/misc/the-precision-is-out-of-range) |  
| 5025 | [Der zu entschlüsselnde URI hat keine gültige Verschlüsselung](/scripting/javascript/misc/the-uri-to-be-decoded-is-not-a-valid-encoding) |  
| 5024 | [Der zu verschlüsselnde URI enthält ein ungültiges Zeichen](/scripting/javascript/misc/the-uri-to-be-encoded-contains-an-invalid-character) |  
| 5009 | [Nicht definierter Bezeichner](/scripting/javascript/misc/undefined-identifier) |  
| 5018 | [Unerwarteter Quantifizierer](/scripting/javascript/misc/unexpected-quantifier-javascript) |  
| 5013 | [VBArray erwartet](/scripting/javascript/misc/vbarray-expected) |  

## Sicherheitscodes

Sicherheitsfehlercodes sind im Format `SEC7xxx`, wie z.B. `SEC7113`.  Diese Fehler spiegeln Sicherheitsbedingungen wider, die von Microsoft Edge erzwungen werden, wie z.B. „Gemischte Inhalte“ und „Tracking-Schutz“.

| Code | Meldung | Beschreibung | Empfohlene Problemlösung |  
| :--- |:--- |:--- |:--- |  
| SEC7111 | "HTTPS-Sicherheit beeinträchtigt durch [Name der Ressource]" | Eine Secure Hypertext Transfer-Protokoll \(HTTPS\)-Seite enthält Inhalte aus einer nicht sicheren Quelle.  | Stellen Sie sicher, dass der gesamte Inhalt der Seite, einschließlich der Skripte, Stylesheet-Objekte und Bilder, aus HTTPS-Quellen stammt.  |  
| SEC7112 | "Skript von [URL] wurde aufgrund eines MIME-Typenkonflikts blockiert" | Der HTTP-Antwortheader für die durch die URL angegebene JavaScript-Datei hat einen "X-Content-Type-Options: nosniff"-Header und verfügt nicht über eine erkannte Inhaltstyp-Deklaration.  | Aktualisieren Sie den Server, um den korrekten Inhaltstyp für die JavaScript-Datei \(wie z. B. text/javascript, application/javascript", zum Beispiel\) im HTTP-Antwortheader zu senden.  Weitere Informationen und eine vollständige Liste der Inhaltstypen finden Sie unter [Änderungen der MIME-Verarbeitung in Internet Explorer](https://blogs.msdn.microsoft.com/ie/2010/10/26/mime-handling-changes-in-internet-explorer/).  |  
| SEC7113 | "Das CSS wurde aufgrund eines MIME-Typenkonflikts ignoriert" | Ein importiertes Stylesheet wurde nicht verwendet, weil der falsche MIME-Typ im HTTP-Header stand.  | Stellen Sie sicher, dass die Stylesheet-Datei mit dem korrekten HTTP-Antwortheader geliefert wird, der den Inhaltstyp "Text/CSS" enthält.  Weitere Informationen finden Sie unter [Änderungen der MIME-Verarbeitung in Internet Explorer](https://blogs.msdn.microsoft.com/ie/2010/10/26/mime-handling-changes-in-internet-explorer/).  |  
| SEC7114 | "Ein Download auf dieser Seite wurde durch den Tracking-Schutz geblockt. [Hier angegebene URL]" | Der Benutzer hat ein Skript oder einen Inhalt mithilfe des Tracking-Schutzes geblockt.  | Keine – benutzerinitiiert.  |  
| SEC7115 | "Die Formate ":visited" und ":link" können nur farblich voneinander abweichen.  Manche Formate wurden nicht auf ":visited" angewendet." | Mehr als ein Attribut, wie z.B. Schriftart oder Größe, wurde durch die Verwendung der Formate "visited" und "link" geändert.  | Ändern Sie nur das Attribut "Farbe".  |  
| SEC7116 | "Zugriff verweigert.  Fehler beim Sperren der ursprungsübergreifenden URL: [URL]." | Ein Skript, das eine andere Herkunftsseite als den BLOB hat, hat versucht, eine BLOB-URL zu widerrufen.  Aufgrund von Richtlinien für den BLOB-Ursprung ist der Versuch fehlgeschlagen.  | Stellen Sie sicher, dass alle BLOB-URLs widerrufen werden, indem Sie Skripts aus derselben Website wie das Dokument verwenden, mit dem die BLOB-URL erstellt wurde.  |  
| SEC7120 | "Der Ursprung [Domäne] wurde im Access-Control-Allow-Origin-Header nicht gefunden." | In der Antwort auf Ihre XMLHttpRequest wurde der Access-Control-Allow-Origin-Header mit einem Wert zurückgegeben, der nicht den Ursprungswert Ihrer Website enthält oder mit diesem übereinstimmt.  | Die Ressource gibt die richtige Art von Header-Codes zurück, lässt die Website aber nicht zu.  Wenden Sie sich an den Entwickler, der die Ressource leitet, und bitten Sie ihn, den Access-Control-Allow-Origin-Header zu aktualisieren, damit Ihre Website zulässig ist.  Sie können sie auf [CORS für XHR im IE10](https://blogs.msdn.microsoft.com/ie/2012/02/09/cors-for-xhr-in-ie10/) verweisen, um weitere Informationen über CORS in Antwortheadern zu erhalten.  |  
| SEC7121 | "Platzhalter in "Access-Control-Allow-Origin" nicht zulässig, wenn das Anmeldeinformationskennzeichen auf "true" festgelegt ist." | Der Server gibt "Access-Control-Allow-Origin: *" in den Headern zurück, aber dies ist nicht erlaubt, wenn die Kennzeichnung `withCredentials` im XMLHttpRequest auf **true** gesetzt ist.  | Der serverseitige Handler muss so modifiziert werden, dass er einen Access-Control-Allow-Origin-Header zurückgibt, der speziell Ihren Ursprungspunkt bei diesem Typ von Anforderung erlaubt.  Wenn Sie den serverseitigen Handler nicht steuern, müssen Sie sich an den Entwickler wenden, der dies tut.  |  
| SEC7122 | "Anmeldeinformationskennzeichen wurde auf "true" festgelegt, aber "Access-Control-Allow-Credentials" war nicht vorhanden oder nicht "true"." | Ein XMLHttpRequest wurde mithilfe der Kennzeichnung `withCredentials` vorgenommen.  Entweder wurde ein Access-Control-Allow-Credentials-Header nicht zurückgegeben oder er wurde mit einem anderen Wert als **true** zurückgegeben.  | Möglicherweise gibt es ein Problem mit Ihren Anmeldeinformationen oder der Antwort des Servers.  Informationen zu den Anforderungen für Anmeldeinformationen finden Sie in der [XMLHttpRequest-Spezifikation der Ebene 2](https://w3.org/TR/XMLHttpRequest2/).  |  
| SEC7123 | "Anforderungsheader [Header] war nicht in der Liste "Access-Control-Allow-Headers" vorhanden." | Die Anforderung enthielt einen benutzerdefinierten Header-Typ, der jedoch in der Liste "Access-Control-Allow-Headers" der Antwort nicht enthalten war.  | Stellen Sie sicher, dass der Server benutzerdefinierte Header zulässt und insbesondere den in der Anforderung gesendeten Header zulässt.  |  
| SEC7124 | "Anforderungsmethode [Methode] war nicht in der Liste "Access-Control-Allow-Methods" vorhanden." | Eine Anforderungsmethode wie POST wurde in der XMLHttpRequest verwendet, aber die Antwort gab einen Header "Access-Control-Allow-Methods" zurück, der sie nicht enthielt.  | Stellen Sie sicher, dass der Server diese Art von Anforderungsmethode zulässt und dass Sie korrekt `withCredentials` verwenden, wenn diese Methode den Zugriff eingeschränkt hat.  |  
| SEC7125 | "XMLHttpRequest für [URL] hat beim Analysieren der Antwortheader einen Fehler verursacht." | Die Antwortheader vom Server konnten nicht analysiert werden, wodurch die Anforderung fehlgeschlagen ist.  | Verwenden Sie das Tool [Netzwerk](https://msdn.microsoft.com/library/dn255004.aspx), um die Antwortheadern zu erfassen und zu überprüfen, um sicherzustellen, dass Sie [CORS-Spezifikationen](https://w3.org/TR/cors/) entsprechen.  |  
| SEC7126 | "Umleitungen sind für CORS Preflight-Anforderungen nicht zulässig." | Im Header "Ursprung" wurde eine Umleitung entdeckt, und der Benutzer-Agent wird während eines Preflights keine Umleitungen folgen.  | Verwenden Sie das Tool [Netzwerk](https://msdn.microsoft.com/library/dn255004.aspx), um die Anforderungsheader zu erfassen und zu überprüfen und sicherzustellen, dass es einen einzigen direkten Ursprung gibt.  |  
| SEC7127 | "Umleitung wurde blockiert für CORS-Anforderung." | Der Pfad zu der CORS-Ressource enthält eine Umleitung, die Sicherheitsregeln verletzt hat.  | Stellen Sie sicher, dass Sie in Ihrem XMLHttpRequest den direktesten Pfad zur CORS-Ressource haben.  |  
| SEC7128 | "Mehrere Access-Control-Allow-Origin-Header sind nicht zulässig für die CORS-Antwort." | Der Antwortheader enthielt mehrere Access-Control-Allow-Origin-Header.  | Dies ist ein serverseitiger Fehler.  Der Server sollte einen einzigen Access-Control-Allow-Origin-Header zurückgeben.  Melden Sie diesen Fehler an den für die serverseitige Ressource zuständigen Entwickler.
| SEC7129 | "Mehrere Access-Control-Allow-Credentials-Header sind nicht zulässig für die CORS-Antwort." | Der Antwortheader enthielt mehrere Access-Control-Allow-Credentials-Header.  | Dies ist ein serverseitiger Fehler.  Der Server muss einen einzigen Access-Control-Allow-Credentials-Header zurückgeben.  Melden Sie diesen Fehler an den für die serverseitige Ressource zuständigen Entwickler.  |  
| SEC7130 | "Potenzielles websiteübergreifendes Skripting in [URL] ermittelt.  Der Inhalt wurde vom XSS-Filter geändert." | Der [XSS-Filter](https://msdn.microsoft.com/library/dd565647.aspx) hat potenziell bösartige Inhalte in der Antwort der Ressource erkannt und die anstößigen Inhalte entfernt.  | Weitere Informationen über den [XSS-Filter](https://msdn.microsoft.com/library/dd565647.aspx).   |  
| SEC7131 | "Die Sicherheit eines Sandkasten-iFrames ist möglicherweise durch das Zulassen eines Skripts und des Zugriffs mit demselben Ursprung gefährdet." | Wenn der Inhalt in einem Sandkasten-iFrame aus einer nicht vertrauenswürdigen oder ungesicherten Quelle stammt, könnte er dem Sandkasten entgehen, wenn sowohl Skript- als auch Ursprungszugriff erlaubt sind.  | Hierbei handelt es sich um eine informative Warnmeldung, die sich nicht auf die Funktionalität auswirkt.  Wir haben empfohlen, diese Berechtigungen nicht zu kombinieren, wenn Sie nicht sicher sind, was im iFrame ausgeführt wird.  |  
| SEC7132 | "Das Zertifikat zum Schutz dieser Website verwendet eine schwache SHA1-Kryptografie." | Das von dieser Website verwendete TLS-Sicherheitszertifikat verwendet eine schwache Kryptografie | Aktualisieren Sie das TLS-Zertifikat des Servers |  

> [!NOTE]
> Bei Websites in der vertrauenswürdigen Sicherheitszone eines Benutzers prüft Microsoft Edge nicht den MIME-Typ eines Stylesheets.

## SVG-Codes  

DevTools unterstützt derzeit kein umfangreiches Debugging für die skalierbare Vektorgrafiken \(SVG\), aber einige Konsolenmeldungen helfen beim Debugging.

| Code | Meldung | Beschreibung | Empfohlene Problemlösung |  
| :--- |:--- |:--- |:--- |  
| SVG5601 | "Die SVG-Pfaddaten haben ein falsches Format und konnten nicht vollständig analysiert werden." | Der SVG-[Pfadzeichenfolge](https://msdn.microsoft.com/library/ff972086.aspx) ist nicht richtig formatiert oder enthält nicht erkannte Befehle.  | Überprüfen Sie das Format der Befehle.  |  
| SVG5602 | "Die SVG-Punkteliste hat ein falsches Format und konnte nicht vollständig analysiert werden." | Die Liste der für ein Element, z.B. einen [Polyline](https://msdn.microsoft.com/library/ff972113.aspx), verwendeten Punkte ist nicht ordnungsgemäß formatiert.  | Stellen Sie sicher, dass die Punkte vollständig und korrekt formatiert für das Koordinatensystem des Benutzers sind.  |  

## XML-Codes  

XML-Codes liegen in der Form von XML5xxx vor, wie z. B. XML5603.  

| Code | Meldung |  
|:--- |:--- |  
| XML5001 | "Die integrierte XSLT-Verarbeitung wird angewendet." |  
| XML5601 | "MX_E_MX" |  
| XML5602 | "Unerwartetes Eingabeende." |  
| XML5603 | "Codierung wurde nicht erkannt." |  
| XML5604 | "Es kann nicht zu einer anderen Codierung gewechselt werden." |  
| XML5605 | "Signatur für die Eingabecodierung wurde nicht erkannt." |  
| XML5606 | "WC_E_WC" |  
| XML5607 | "Ein Leerzeichen wurde erwartet." |  
| XML5608 | "Ein Semikolon wurde erwartet." |  
| XML5609 | "">" erwartet." |  
| XML5610 | "Ein Anführungszeichen wird erwartet." |  
| XML5611 | ""=" erwartet." |  
| XML5612 | "Das Zeichen "<" ist in Attributwerten unzulässig." |  
| XML5613 | "Eine Hexadezimalzahl wird erwartet." |  
| XML5614 | "Eine Dezimalzahl wird erwartet." |  
| XML5615 | ""[" erwartet." |  
| XML5616 | ""(" erwartet." |  
| XML5617 | "Ungültiges XML-Zeichen." |  
| XML5618 | "Ungültiges Namenszeichen." |  
| XML5619 | "Ungültige Dokumentsyntax." |  
| XML5620 | "Ungültige Syntax des CDATA-Abschnitts." |  
| XML5621 | "Ungültige Kommentarsyntax." |  
| XML5622 | "Ungültige Syntax des Bedingungsabschnitts." |  
| XML5623 | "Ungültige Syntax der ATTLIST-Deklaration." |  
| XML5624 | "Ungültige Syntax der DOCTYPE-Deklaration." |  
| XML5625 | "Ungültige Syntax der ELEMENT-Deklaration." |  
| XML5626 | Ungültige Syntax der ENTITY-Deklaration." |  
| XML5627 | "Ungültige Syntax der NOTATION-Deklaration." |  
| XML5628 | ""NDATA " erwartet." |  
| XML5629 | ""PUBLIC" erwartet." |  
| XML5630 | ""System" erwartet." |  
| XML5631 | "Ungültiger Name." |  
| XML5632 | "Es ist nur ein Stammelement zulässig." |  
| XML5633 | "Der Name des Endtags entspricht nicht dem Namen des zugehörigen Starttags." |  
| XML5634 | "Es ist bereits ein Attribut mit diesem Namen für dieses Element vorhanden." |  
| XML5635 | "Eine XML-Deklaration ist nur am Beginn der Datei zulässig." |  
| XML5636 | "Führendes "xml"." |  
| XML5637 | "Ungültige Syntax der Textdeklaration." |  
| XML5638 | "Ungültige Syntax der XML-Deklaration." |  
| XML5639 | "Ungültige Syntax des Codierungsnamens." |  
| XML5640 | "Ungültige Syntax des öffentlichen Bezeichners." |  
| XML5641 | "In einer internen DTD-Teilmenge können Verweise auf Parameterentitäten in Markup-Deklarationen nicht vorkommen." |  
| XML5642 | "Der Ersetzungstext für Verweise auf Parameterentitäten zwischen Markup-Deklarationen muss eine Reihe vollständiger Markup-Deklarationen enthalten." |  
| XML5643 | "Eine analysierte Entität kann keinen direkten oder indirekten Verweis auf sich selbst enthalten." |  
| XML5644 | "Der Inhalt der angegebenen Entität ist nicht wohlgeformt." |  
| XML5645 | "Die angegebene Entität wurde nicht deklariert." |  
| XML5646 | "Entitätsverweise können nicht den Namen einer nicht analysierten Entität enthalten." |  
| XML5647 | "Attributwerte können keine direkten oder indirekten Verweise auf externe Entitäten enthalten." |  
| XML5648 | "Ungültige Syntax der Verarbeitungsanweisung." |  
| XML5649 | Ungültige Syntax des Systembezeichners." |  
| XML5650 | "Ein Fragezeichen \(\?\) wird erwartet." |  
| XML5651 | "Das Zeichen für das CDATA-Abschnittsende "]]>" darf nicht in Elementinhalt verwendet werden." |  
| XML5652 | "Es wurden nicht alle Datenabschnitte gelesen." |  
| XML5653 | "DTD gefunden, ist jedoch unzulässig." |  
| XML5654 | "Es wurde ein xml:space-Attribut mit ungültigem Wert gefunden.  Gültige Werte sind "preserve" und "default"." |  
| XML5655 | "NC_E_NC" |  
| XML5656 | "Ungültiges Zeichen für qualifizierten Namen." |  
| XML5657 | "Mehrfache Doppelpunkte (":") sind in einem qualifizierten Namen nicht zulässig." |  
| XML5658 | "Ein Doppelpunkt (":") ist in einem Namen nicht zulässig." |  
| XML5659 | "Deklariertes Präfix." |  
| XML5660 | "Das angegebene Präfix wurde nicht deklariert." |  
| XML5661 | "Nicht standardmäßige Namespacedeklarationen können keinen leeren URI haben." |  
| XML5662 | "Das Präfix "xml" ist reserviert und muss den URI "<https://w3.org/XML/1998/namespace/>" aufweisen." |  
| XML5663 | "Das Präfix "xmlns" ist für die Verwendung durch XML reserviert." |  
| XML5664 | "Der XML-Namespace-URI \(\<https://w3.org/XML/1998/namespace/\>\) darf nur dem Präfix "xml" zugewiesen werden." |  
| XML5665 | "Der XMLNS-Namespace-URI \(\<https://w3.org/2000/xmlns/\>\) ist reserviert und darf nicht verwendet werden." |  
| XML5666 | "SC_E_SC" |  
| XML5667 | "Die maximale Tiefe für geschachtelte Elemente wurde überschritten." |  
| XML5668 | "Die maximale Anzahl von Entitätserweiterungen wurde überschritten." |  
| XML5669 | "WR_E_WR" |  
| XML5670 | "WR_E_NONWHITESPACE: writer: Die angegebene Zeichenfolge ist kein Leerzeichen." |  
| XML5671 | "WR_E_NSPREFIXDECLARED: Writer: Das Namespacepräfix wurde bereits mit einem anderen Namespace deklariert." |  
| XML5672 | "WR_E_NSPREFIXWITHEMPTYNSURI: Writer: Das Präfix kann nicht mit einem leeren Namespace-URI verwendet werden." |  
| XML5673 | "WR_E_DUPLICATEATTRIBUTE: Writer: Doppeltes Attribut." |  
| XML5674 | "WR_E_XMLNSPREFIXDECLARATION: Writer: Das Präfix "xmlns" kann nicht umdefiniert werden." |  
| XML5675 | "WR_E_XMLPREFIXDECLARATION: Writer: Das Präfix "xml" muss den URI \<https://w3.org/XML/1998/namespace/\> aufweisen." |  
| XML5676 | "WR_E_XMLURIDECLARATION: Writer: Der XML-Namespace-URI \(\<https://w3.org/XML/1998/namespace/\>\) darf nur dem Präfix "xml" zugewiesen werden." |  
| XML5677 | "WR_E_XMLNSURIDECLARATION: Writer: Der XMLNS-Namespace-URI \(\<https://w3.org/2000/xmlns/\>\) ist reserviert und darf nicht verwendet werden." |  
| XML5678 | "WR_E_NAMESPACEUNDECLARED: Writer: Der Namespace ist nicht deklariert." |  
| XML5679 | "WR_E_INVALIDXMLSPACE: Writer: Ungültiger Wert für das xml:space-Attribut \(zulässige Werte sind "default" und "preserve"\)." |  
| XML5680 | "WR_E_INVALIDACTION: Writer: Ungültiges XML-Dokument beim Ausführen der angeforderten Aktion." |  
| XML5681 | "WR_E_INVALIDSURROGATEPAIR: Writer: Die Eingabe enthält ein ungültiges oder unvollständiges Ersatzzeichenpaar." |  
| XML5682 | "Unerwartetes Zeichen in der Zeichenentität.  Erwartet wurde eine Dezimalzahl." |  
| XML5683 | "Unerwartetes Zeichen in der Zeichenentität.  Erwartet wurde eine Hexadezimalziffer." |  
| XML5684 | "Der Unicode-Wert der angegebenen Zeichenentität ist ungültig." |  
| XML5685 | "Ungültige Codierung." |  
| XML5686 | "Nicht angegebener XML-Fehler." |  
