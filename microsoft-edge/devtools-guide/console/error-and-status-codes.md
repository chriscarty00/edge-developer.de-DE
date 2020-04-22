---
ms.assetid: 961ca575-6b93-4367-a72b-f3f02e5b9568
description: Verweis auf häufige Konsolen Codes und vorgeschlagene Korrekturen
title: DevTools-Konsolenfehler und Statuscodes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Konsolen Codes
ms.custom: seodec18
localization_priority: Priority
ms.openlocfilehash: aa667941f619dcc0eac2411a087dbdfcf2fda613
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568444"
---
# Konsolenfehler und Statuscodes  

Dieser Verweis hilft Ihnen bei der Interpretation von Fehler-und Statusmeldungen über die devtools- [Konsole](../console.md).  Verwenden Sie die folgende Tabelle, um Codes nach deren Präfix zu suchen \ (wobei "x" eine&ndash;0 9-stellige Zahl darstellt \):

| Code Präfix | Bereich | Beschreibung |  
|:--- | :--- |:--- |  
| [CSP143xx](#csp-codes) | Inhalts Sicherheitsrichtlinie | Durch die Verwendung eines `Content-Security-Policy` HTTP-Headers blockierte Ressourcen.  |  
| [CSS31xx](#css-codes) | Stylesheets | Fehler im Zusammenhang mit dem *Web Open Font Format* \ (WOFF \) und *Embedded OpenType* \ (EOT \) Font Source-und Hostserver Probleme.  |  
| [HTML1112-1300](#html-codes) | HTML | Die meisten dieser Beispiele sind Legacycodes für Microsoft Internet Explorer-Konzepte wie *Dokumentmodus* und *Kompatibilitätsansicht*.  |  
| [HTML1400-1532](#html5-parser-warnings) | HTML5-Analyse | Vom HTML5-Parser ausgelöste Validierungswarnungen.  |  
| [HTTP](#http-codes) | Server Fehler und-Status | Von Remoteservern als Antwort auf HTTP-Anforderungen zurückgegebene Codes.  |  
| [SCRIPT10xx](#javascript-syntax-errors) | JavaScript-Syntaxfehler | Tritt auf, wenn die Struktur einer ihrer JavaScript-Anweisungen gegen eine oder mehrere syntaktische Regeln verstößt.  |  
| [SCRIPT50xx](#javascript-run-time-errors) | JavaScript-Runtime-Fehler | Tritt auf, wenn das Skript versucht, eine Aktion auszuführen, die das System nicht ausführen kann.  |  
| [SEC71xx](#security-codes) | Sicherheit | Spiegelt die Sicherheitsbedingungen wider, die von Microsoft Edge erzwungen werden, wie beispielsweise *gemischter Inhalt* und *nach Verfolgungs Schutz*.  |  
| [SVG560x](#svg-codes) | Skalierbare Vektorgrafiken |  Umfangreiches SVG-Debugging wird derzeit nicht unterstützt, aber einige Konsolen Nachrichten werden für Debugging-Zwecke bereitgestellt.  |  
| WebGL11_xxx | WebGL | Fehlermeldungen aus dem WebGL-Kontext.  Siehe auch [GLSL-Fehler](https://msdn.microsoft.com/library/dn611835.aspx).  |  
| [XML5xxx](#xml-codes) | XML | Fehler bei der XML-Analyse und-Validierung.  |  

## CSP-Codes  

Durch die Verwendung eines `Content-Security-Policy` HTTP-Headers blockierte Ressourcen werden über die devtools-Konsole und optional als Bericht zurück an den Server gemeldet.

| Code | Meldung | Beschreibung | Vorgeschlagene Lösung |
|:--- |:--- |:--- |:--- |
| CSP14301 | "Fehler beim Analysieren des \ [Richtlinientyps \], weil \ <der Grund für den Abbruch des Vorgangs \ >--Richtlinie ignoriert wird." | Der angegebene Sicherheits Richtlinientyp \ (beispielsweise Script-src, Base-URI \) konnte aus dem angegebenen Grund nicht erkannt werden und wird ignoriert.  | Stellen Sie sicher, dass Sie alle erforderlichen Ressourcen eines bestimmten Typs in einer einzelnen Direktive auflisten.  In `script-src https://host1.com; script-src https://host2.com`wird beispielsweise die zweite Direktive ignoriert.  Im folgenden werden beide Ursprünge richtig als gültig `script-src https://host1.com https://host2.com`angegeben:  |
| CSP14302 | "Fehler beim Analysieren der Quelle in \ [Richtlinientyp \]" für Direktive \ [Direktive Type \] at \ [Quell-URL \]--Source wird ignoriert. "                                                         | Für die meisten CSP-Direktiven ist mindestens eine Inhaltsquelle erforderlich \ (die eine URL angibt, von der Inhalte geladen werden können).  Dieser Fehler verweist auf eine Richtlinie mit einer Direktive, die eine Quell-URL enthält, die bei der Analyse fehlschlug.  | Überprüfen Sie die Inhaltsquelle \ (meistens eine URL \), die in der angegebenen Direktive definiert ist, die Sie im angegebenen Richtlinientyp finden können.  Korrigieren oder ersetzen Sie die Quell-URL, oder entfernen Sie die Direktive.  <br /> *\ * Ihre Richtlinie sollte eine default-src-Richtlinien Direktive enthalten, die ein Fallback für andere Ressourcentypen ist, wenn Sie keine eigenen Richtlinien besitzen.* |
| CSP14303 | "[Richtlinientyp]-Richtlinie war leer." | Der Richtlinientyp \ (beispielsweise Content-Security-Policy im HTTP-Header \) ist leer.  | Eine Kurzübersicht zum Einrichten einer Inhalts Sicherheitsrichtlinie finden Sie unter [http://content-security-policy.com](http://content-security-policy.com).  |
| CSP14304 | "Unbekannte Quelle \ [Quell-URL \]" für Direktive \ [Directive Type \] in \ [Richtlinientyp \] Source wird ignoriert. " | Die Quellen für genehmigte \ (Safe \)-Inhalte in der angegebenen Direktive sind unbekannt und werden ignoriert.  | Überprüfen Sie die gefundene Inhaltsquelle \ (häufig handelt es sich um eine URL \), um sicherzustellen, dass Sie richtig ist.  |
| CSP14305 | "Nicht unterstützte Quelle \ [Quell-URL \] für Direktive [Directive-Typ] in \ [Richtlinientyp \] Source wird ignoriert." | Die in dieser Direktive aufgelistete Quelle \ (URL, Schlüsselwort oder Daten) wird nicht unterstützt und ignoriert.  | Die Adresse der Quellwebsite enthält möglicherweise einen optionalen führenden Platzhalter \ (das `*`Sternchenzeichen \).  Beispiel: http://`*`. foo.com oder Mail.foo.com: *.  Die Hosts sind durch Leerzeichengetrennt.  Quellen können auch Stichwörter sein (keine, selbst, unsichere Inline-und unsafe-eval werden unterstützt \) oder Daten \ (Data: URIs, MediaStream: URIs \).  |
| CSP14306 | "Es wurden keine Quellen für die Direktive \ [Directive Type \] für \ [Richtlinientyp \] angegeben, was der Verwendung von" None "entspricht und den Download aller Ressourcen dieses Typs verhindert." | Wenn Sie eine Direktive angeben und keine Quellen für den Zugriff auf sichere Inhalte auflisten, ist dies identisch mit der Möglichkeit, keine Ressourcen des in der Direktive angegebenen Typs herunterzuladen.  | Eine Quelle kann einen oder mehrere Internethostnamen oder IP-Adressen sowie ein optionales URL-Schema und/oder eine Portnummer sein.  |
| CSP14307 | "Quelle [Quell-URL]" wurde bereits für die Direktive \ [Directive Type \] für \ [Richtlinientyp \] bereitgestellt. " | Eine doppelte Quelle \ (URL, Schlüsselwort oder Daten \) wurde in dieser Direktive aufgeführt und wird ignoriert.  | Entfernen Sie die erkannte doppelte Quelle.  |
| CSP14308 | "Fehler beim Analysieren der Direktive in \ [Richtlinientyp \] unter [Direktive Name]." | Fehler bei der angegebenen Richtlinie.  Anleitungen zum Schreiben von unterstützten Direktiven finden [http://content-security-policy.com](http://content-security-policy.com/)Sie unter.  | Direktiven müssen durch Semikolons getrennt werden.  Wenn Sie beispielsweise über eine Anwendung verfügen, die alle Ihre Ressourcen aus einem Content Delivery Network (beispielsweise `https://cdn.example.net`\) lädt, und Sie wissen, dass Sie keine gerahmten Inhalte oder Plug-Ins benötigen, sieht Ihre Richtlinie wie folgt aus: `Content-Security-Policy: default-src https://cdn.example.net; child-src 'none'; object-src 'none'.` *\ * während Direktiven durch Semikolons getrennt sind, sollten Quellen innerhalb einer Direktive nur durch ein Leerzeichengetrennt werden.* |
| CSP14309 | "Unbekannte Direktive in \ [Direktive Name \] in \ [Richtlinientyp \]--Direktive wird ignoriert." | Die in der CSP-Richtlinie gesetzte Direktive ist unbekannt und wird ignoriert.  | Eine Liste der unterstützten Direktiven [http://content-security-policy.com](http://content-security-policy.com/)finden Sie unter.  |
| CSP14310 | "Nicht unterstützte Direktive [Direktive Name] in \ [Policy Type]--Direktive wird ignoriert." | Eine Direktive wurde während der Analyse im Richtlinientyp gefunden \ (beispielsweise das `Content-Security-policy-Report-Only` Headerfeld \), das nicht unterstützt wird, und wird ignoriert.  Informationen zu unterstützten [http://content-security-policy.com](http://content-security-policy.com/)Direktiven finden Sie unter.  | Entfernen Sie die nicht unterstützte Direktive.  **Hinweis**: einige Direktiven werden im \ <Meta \ >-Element oder im `Content-Security-policy-Report-Only` Headerfeld nicht unterstützt.  |
| CSP14311 | "Direktive \ [Direktive Name \] wurde bereits in \ [Richtlinientyp \] bereitgestellt--doppelte Direktive wird ignoriert." | Während der Analyse wurde eine doppelte Direktive gefunden, die zweite Direktive und ihre quellausdrücke werden ignoriert.  | Entfernen Sie das doppelte Skript.  |
| CSP14312 | "Ressource verletzt Direktive [Direktive Name] in [Richtlinientyp]: [Ziel-URI].  Die Ressource wird blockiert. " | In diesem Beispiel: "Ressourcen Verletzungs Direktive"-Skript-src MS-AppX: Data: "unsafe-eval" in der Host definierten Richtlinie: Inlineskript.  Die Ressource wird blockiert. " | Ein Inlineskript \ (Ziel-URI \) wurde aufgrund der Direktive in `'script-src ms-appx: data: 'unsafe-eval'` der Richtlinie "Host definiert" blockiert.  <br /> Autoren müssen alle Inlineskripts und Formatvorlagen außerhalb der Zeile verschieben, da der Benutzer-Agent nicht ermitteln kann, ob ein Inlineskript von einem Angreifer injiziert wurde.  Entfernen Sie Inlineskripts, und fügen Sie Sie in einer externen Datei ein.  |
| CSP14313 | "Ressource verletzt Direktive [Direktive Name] in [Richtlinientyp]: [Ziel-URI].  Die Ressource wird aufgrund einer nur Berichts basierten Richtlinie nicht blockiert. " | Es wurde eine Ressource identifiziert, die gegen die im `Content-Security-policy-Report-Only` Headerfeld angegebene Direktive verstößt.  Da es sich um einen `Report-Only` Richtlinientyp handelt, wird die Ressource nicht blockiert.  | Verschieben Sie die Direktive in ein Headerfeld für Inhaltssicherheit – Richtlinie, wenn diese Ressource blockiert werden soll, um Ihre Website zu schützen.  |
| CSP14314 | "Fehler beim Senden einer Richtlinien Verletzungs Meldung an [Ziel-Ziel-URI], weil [Grund für den Abbruch des Vorgangs]." | Es gab ein Problem mit dem Melden einer Richtlinienverletzung, dem Ziel Ziel, in dem der Bericht gesendet werden soll, und der Grund für das nicht senden sollte identifiziert werden.  | Die `report-uri` Direktive gibt eine URL an, in der ein Browser Berichte sendet, wenn eine Inhalts Sicherheitsrichtlinie verletzt wird.  *\ * Es kann nicht in \ <Meta \ > Tags verwendet werden.* |
| CSP14315 | "Fehler beim Erzwingen der Sandbox-Direktive in [Richtlinientyp], weil [Grund für den Abbruch des Vorgangs]." | Die Sandbox-Direktive konnte aus den angegebenen Gründen nicht ausgeführt werden.  Diese Direktive legt Einschränkungen für Aktionen fest, die von der Seite ausgeführt werden können, statt auf Ressourcen, die von der Seite geladen werden können.  Wenn die Sandbox-Direktive vorhanden ist, wird die Seite so behandelt, als ob Sie in einem IFRAME geladen wurde.  Damit können Popups und Plug-ins verhindert und die Skriptausführung blockiert werden.  | Halten Sie den Sandkasten Wert leer, damit alle Einschränkungen vorhanden sind, oder fügen `allow-forms`Sie `allow-same-origin`Werte `allow-scripts`hinzu: `allow-top-navigation`,, und.  *\ * Die Sandbox-Direktive wird im \ <Meta \ >-Element oder im `Content-Security-policy-Report-Only` Headerfeld nicht unterstützt.* |
| CSP14316 | "Skript-eval wird aufgrund einer Host-Überschreibung zugelassen." | Wenn entweder die `script-src` or `default-src` -Direktive enthalten ist, werden Inline `eval()` Skripts und deaktiviert, es `unsafe-inline` sei `unsafe-eval`denn, Sie geben bzw.  | `'unsafe-eval'` ermöglicht die Verwendung `eval()` und ähnliche Methoden zum Erstellen von Code aus Zeichenfolgen.  Sie müssen die einfachen Anführungszeichen angeben.  ***Hinweis**: Dies ist unsicher und kann Ihre Website für websiteübergreifende Skripting-Sicherheitsanfälligkeiten öffnen. * |
| CSP14317 | "Frame [Source Name] wird aufgrund einer Host Überschreibung zugelassen." | Der erkannte Quellframe wurde aufgrund eines override-Satzes in der Host-CSP-Richtlinie zugelassen.  | Eine Richtlinie enthält möglicherweise einen aus der Quelle hervorgehenden Ausdruck, was bedeutet, dass die Quelle nur einmal verwendet werden kann und der Server bei jeder Übertragung einer Richtlinie einen neuen Wert für die Direktive generieren muss.  Die Einschränkungen in der Direktive, in der Sie vorhanden sind, werden von den Vorfahren überschrieben.  |

> [!NOTE]
> Für Websites in der vertrauenswürdigen Sicherheitszone eines Benutzers überprüft Microsoft Edge nicht den MIME-Typ eines Stylesheets.  

## CSS-Codes  

Diese Fehler sind im CSS31xx-Format und beziehen sich auf *Web Open Font Format* \ (WOFF \) und *eingebettete OpenType* \ (EOT \) Font Source-und Hostserver Probleme.  

| Code | Meldung | Beschreibung | Vorgeschlagene Lösung |
|:--- |:--- |:--- |:--- |
| CSS3111 | Unbekannter Fehler "@font-face" | Ein unbekanntes Problem mit dem "Web Open Font Format \ (WOFF \)" und "Embedded OpenType Font \ (EOT \)" der Cascading Style Sheets \ (CSS \)-Schriftart ist aufgetreten.  | Überprüfen Sie die Quelle der WOFF-Schriftarten.  Versuchen Sie es mit einer alternativen Schriftart oder-Quelle, um festzustellen, ob das Problem reproduziert werden kann.  |
| CSS3112 | "@font-face-Fehler bei der WOFF-Integritätsprüfung" | Die Schriftart "Web Open Font Format \ (WOFF \)" ist möglicherweise beschädigt, unvollständig oder nicht das richtige Format.  | Überprüfen Sie die Quelle der Schriftarten.  Testen Sie eine bekannte Schriftart oder Quelle, um festzustellen, ob Sie das Problem reproduzieren können.  |
| CSS3113 | "@font-face-Konflikt zwischen Dokumentursprung und EOT-Stamm Zeichenfolge" | Die Schriftart kann nicht verwendet werden, da die URL \ (rootName \) in der eingebetteten OpenType \ (EOT \)-Schriftart nicht der Domäne des Dokuments mit der Schriftart entspricht.  | Die URL-Prüfsumme im EOT-Wortstamm ist möglicherweise falsch, was auf eine beschädigte oder geänderte URL für die Schriftart hindeutet.  Stellen Sie sicher, dass die Schriftart lizenziert ist oder über die Berechtigungen für die Website verfügt, auf der Sie verwendet wird.  |
| CSS3114 | "@font-face-Fehler bei OpenType-Einbettungs Überprüfung.  Die Berechtigung muss installiert sein. " | Die Font-Face-Anwendung verfügt nicht über die erforderlichen Berechtigungen, um die aktuelle Webseite zu installieren.  | Abrufen der richtigen Berechtigung oder Lizenzen zum Einbetten der Schriftart  |
| CSS3115 | "@font-face kann keine ungültige OpenType-Schriftart laden." | Die Schriftart ist für diese Verwendung ungültig.  | Besorgen Sie sich die Berechtigung oder Lizenzen für die aktuelle und gültige Schriftart.  |
| CSS3116 | "@font-face-Fehler-Cross-Origin-Anfrage.  Keine Zugriffssteuerung-Allow-Origin-Kopfzeile. " | Die Schriftart ist möglicherweise nicht für den domänenübergreifenden Zugriff konfiguriert.  | Die Schriftart wird nicht vom gleichen Ursprung wie das Dokument bereitgestellt.  Stellen Sie sicher, dass der Host, der die Schriftart verwendet, die Verwendung dieser Schriftart mithilfe des HTTP-Headers "Access-Control-Allow-Origin" ermöglicht.                        |
| CSS3117 | "@font-face-Fehler-Cross-Origin-Anfrage.  Der Ressourcenzugriff ist eingeschränkt. " | Die Kopfzeile "Zugriff-Steuerelement-Allow-Origin" ist möglicherweise nicht ordnungsgemäß konfiguriert, oder der Font-Host lässt nicht zu, dass diese Schriftart von der Seite verwendet wird.  | Stellen Sie sicher, dass die Ressource über die richtigen Berechtigungen und einen ordnungsgemäß konfigurierten HTTP-Antwortheader verfügt, der über einen domänenübergreifenden Zugriffs Ursprung auf dem Host für die Schriftarten verfügt.  |
| CSS3118 | "Fehler beim Erstellen eines neuen Stylesheets.  Das Dokument enthält mehr als \ [Maximum \]-Stylesheets. " | Microsoft Edge hat während des Renderns Ihrer Seite mehr als 4095-Stylesheet-Objekte erstellt.  | Hierbei kann es sich um einen Out-of-Control-JavaScript-Prozess oder einen Buildsystem-Fehler handeln.  Verringern Sie die Anzahl der zu generierende Stylesheet-Objekte.  |
| CSS3119 | "Der medienabfrage-MS-View-Zustand wurde als veraltet markiert.  -MS-View-State-medienabfragen werden nach Windows 8,1 möglicherweise geändert oder sind für Versionen nicht verfügbar.  Verwenden Sie stattdessen Abfragen mit maximaler Breite und minimaler Breite. " | Ihr CSS enthält eine `-ms-view-state` medienabfrage.  | Verwenden Sie max-width und min-width.  |

## HTML-Codes

Diese Codes sind im HTML1xxx-Format, wie etwa HTML1115.  Viele dieser Legacycodes sind für Internet Explorer-Konzepte wie *Dokumentmodus* und *Kompatibilitätsansicht* spezifisch.  

| Code | Meldung | Beschreibung | Vorgeschlagene Lösung |  
| :--- |:--- |:--- |:--- |  
| HTML1112 | "Codepage-Neustart von \ [Codierung \] to \ [Codierung \]" | Es wurde eine Codepage angegeben, die von der Codepage des Servers abweicht.  | Verwenden Sie dieselbe Codepage wie der Server, um diesen Fehler zu vermeiden.  |  
| HTML1113 | "Neustart des Dokumentmodus von \ [Modus \] to \ [Modus \]" | Die Webseite erfordert einen anderen Dokumentmodus als für den Browser aktuell eingestellt ist.  | Diese Meldung kann auftreten, wenn der Benutzer von einer anderen Seite aus durchsucht, wodurch er aus dem Steuerelement des Entwicklers hervorgeht.  |  
| HTML1114 | "Codepage \ [Codierung \] from \ [Domäne \] überschreibt die in Konflikt stehende Codepage \ [Encoding \] from \ [Domäne \]" | Die in den Headern http \ (from Server \) und HTML \ (in-Page \) angegebenen Codepages unterscheiden sich voneinander.  | Ändern Sie eine Übereinstimmung.  |  
| HTML1115 | "X-UA-kompatibles Meta-Tag`[META tag]`\ (\) wird ignoriert, da der Dokumentmodus bereits finalisiert ist" | In der Regel wurde das Meta-Tag nach der Deklaration "Script" oder "Style" gesetzt, wodurch der Dokumentmodus für die Seite behoben wurde.  | Verschieben Sie das X-UA-kompatible Meta-Tag so früh wie möglich in die Kopfzeile.  Es empfiehlt sich, die Datei direkt hinter dem \ <Title \ > und dem charset-Wert zu platzieren.  |  
| HTML1116 | "X-UA-kompatibles Meta-Tag`[META tag]`\ (\)" wurde aufgrund eines früheren x-UA-kompatiblen Meta`[META tag]`-Tags \ (\) ignoriert. " | Es gibt mehr als ein "X-UA-kompatibles" Meta-Tag im Abschnitt \ <Head \ > des Quellcodes.  | Entfernen Sie alle bis auf eine "X-UA-Compatible Meta"-Kategorie, und stellen Sie sicher, dass Sie so früh wie möglich in der Kopfzeile ist.  Es empfiehlt sich, die Datei direkt hinter dem \ <Title \ > und dem charset-Wert zu platzieren.  |  
| HTML1121 | "Codepage \ [Codierung \] ist nicht zulässig, nur Codepage \ [Codierung \] ist zulässig." | Inhalt auf der Webseite hat eine Zeichencodierung aufgerufen, die in diesem Kontext nicht zulässig ist.  | Stellen Sie sicher, dass alle Inhalte die zulässige Codierung verwenden, die in der Nachricht angegeben ist.  |  
| HTML1122 | "Internet Explorer wird im Enterprise-Modus ausgeführt, der IE8 emuliert" | Die Seite wird derzeit im Enterprise-Modus gerendert, einer Emulation von Windows Internet Explorer 8.  | Dieser Modus wird von der IT-Verwaltung für bestimmte Websites konfiguriert.  Wenn ein einzelner Benutzer ihn auf einer Webseite deaktivieren muss, deaktivieren Sie im Menü Extras die Option Enterprise-Modus.  Weitere Informationen zur Verwaltung des Enterprise-Modus finden Sie in der [IT-Dokumentation](https://technet.microsoft.com/library/dn640687.aspx).  |  
| HTML1201 | "`[domain]` ist eine Website, die Sie der Kompatibilitätsansicht hinzugefügt haben." | Der Benutzer hat die Schaltfläche **Kompatibilitätsansicht** für die aktuelle Website ausgewählt oder ihn über die **Einstellungen für die Kompatibilitätsansicht**hinzugefügt.  | Vom Benutzer initiiert.  |  
| HTML1202 | "`[domain]` wird in der Kompatibilitätsansicht ausgeführt, da" Intranet-Websites in der Kompatibilitätsansicht anzeigen "aktiviert ist." | Der Benutzer hat das Kontrollkästchen **Intranet-Websites in Kompatibilitätsansicht anzeigen** in den **Einstellungen der Kompatibilitätsansicht**ausgewählt.  | Der Benutzer muss Alt + T drücken, die **Einstellungen für die Kompatibilitätsansicht**auswählen und dann das Kontrollkästchen **Intranet-Websites in Kompatibilitätsansicht anzeigen** deaktivieren.  |  
| HTML1203 | "`[domain]` wurde für die Ausführung in der Kompatibilitätsansicht über Gruppenrichtlinien konfiguriert." | Der Netzwerkadministrator hat angegeben, dass die Webseite in der Kompatibilitätsansicht ausgeführt werden soll.  | Sie müssen sich an den Netzwerkadministrator wenden.  |  
| HTML1204 | "`[domain]` wird in der Kompatibilitätsansicht ausgeführt, da" alle Websites in der Kompatibilitätsansicht anzeigen "aktiviert ist." | Der Benutzer hat in den **Einstellungen der Kompatibilitätsansicht**das Kontrollkästchen **alle Websites in Kompatibilitätsansicht anzeigen** aktiviert.  | Der Benutzer muss Alt + T drücken, die **Einstellungen für die Kompatibilitätsansicht**auswählen und dann das Kontrollkästchen **alle Websites in der Kompatibilitätsansicht anzeigen** deaktivieren.  |  
| HTML1300 | "Navigation ist aufgetreten" | Es wurde eine neue Seite navigiert, oder die aktuelle Seite wurde aktualisiert.  | Hierbei handelt es sich um eine Informationsmeldung, nicht um einen Fehler.  |  

## HTML5-Parser-Warnungen  

Die folgenden Warnungen können als Teil der Validierung auftreten, die während der HTML-Analyse durchgeführt wird.  Diese Warnungen bedeuten nicht unbedingt, dass eine Seite beschädigt ist, dass der bereitgestellte HTML-Code pro HTML5-Standard ungültig ist.  Inhalte, die in Übereinstimmung mit früheren Versionen der HTML-oder XHTML-Spezifikationen erstellt wurden, sind in HTML5 möglicherweise nicht gültig, insbesondere im Hinblick auf die Verwendung von doctypes.

In diesen Warnungen werden häufig fehlende oder zusätzliche Zeichen und nicht übereinstimmende Tags angezeigt.  Wenn Sie diese Warnungen beheben, sollte die Kompatibilität mit älteren Browsern und der Kompatibilität einer Webseite mit dem HTML5-Standard verbessert werden.  Um die Quelle einer Warnung zu identifizieren, enthält Sie Informationen zur Zeile und zum Zeichenabstand sowie einen Link, der auf den Speicherort zeigt, an dem das Problem gefunden wurde.

| Code     | Meldung |  
| :--- |:--- |  
| HTML1400 | "Unerwartetes Zeichen am Anfang des numerischen Zeichen Bezugs.  Erwartet [0-9]. " |  
| HTML1401 | "Unerwartetes Zeichen beim Anfang des hexadezimalen numerischen Zeichen Bezugs.  Erwarten Sie ED [0-9], [a-f] oder [a-f]. " |  
| HTML1402 | "Zeichen Bezug fehlt ein endsemikolon"; "." |  
| HTML1403 | "Numerischer Zeichen Bezug wird nicht in ein gültiges Zeichen aufgelöst." |  
| HTML1404 | "Unbekannter Named Character-Verweis." |  
| HTML1405 | "Ungültiges Zeichen: U + 0000 NULL.  NULL-Zeichen sollten nicht verwendet werden. " |  
| HTML1406 | "Ungültiger Tag-Anfang: \ < \?.  Fragezeichen sollten keine Tags starten. " |  
| HTML1407 | "Ungültiger Tag-Name.  Das erste Zeichen sollte mit [a-zA-Z] übereinstimmen. " |  
| HTML1408 | "Ungültiges Endtag \ </\ >.  End-Tags sollten nicht leer sein. " |  
| HTML1409 | "Ungültiges Attributnamen Zeichen.  Attributnamen dürfen keine \ (\ "\), \ (\ ' \), \ (\ < \) oder \ (= \) enthalten." |  
| HTML1410 | "Ungültiger Attributwert für nicht Anführungszeichen.  Nicht Anführungszeichen-Attributwerte dürfen keine \ (\ "\), \ (\ ' \), \ (\ < \), \ (= \) oder \ (\ ' \) enthalten." |  
| HTML1411 | "Unerwartetes Ende der Datei." |  
| HTML1412 | "Fehlerhafter Kommentar.  Kommentare sollten mit \ < \!--\ > beginnen. " |  
| HTML1413 | "Unerwartetes Zeichen: U + 003E größer-als-Zeichen \ (\ > \)" |  
| HTML1414 | "Unerwartetes Zeichen: U + 0021-Ausrufezeichen \ (\! \)" |  
| HTML1415 | "Unerwartetes Zeichen: U + 002D Bindestrich-minus \ (-\)" |  
| HTML1416 | "Unerwartetes Zeichen im Kommentarende.  Erwartet "--\ >". " |  
| HTML1417 | "Leeres DOCTYPE.  Der kürzeste gültige DOCTYPE ist \ < \! DOCTYPE HTML \ >. " |  
| HTML1418 | "Unerwartetes Zeichen in DOCTYPE." |  
| HTML1419 | "Unerwartetes Schlüsselwort in DOCTYPE.  "Öffentlich" oder "System" erwartet. " |  
| HTML1420 | "Unerwartetes Zitat nach" öffentliches "oder" System "-Schlüsselwort.  Erwartetes Leerzeichen. " |  
| HTML1421 | "Fehlerhafte End-Tag.  End-Tags sollten keine Attribute enthalten. " |  
| HTML1422 | "Fehlerhafte Start Kategorie.  Auf einen selbstschließenden Schrägstrich sollte ein U + 003E größer-als-Zeichen \ (\ > \) folgen. " |  
| HTML1423 | "Fehlerhafte Start Kategorie.  Attribute sollten durch Leerzeichengetrennt werden. " |  
| HTML1424 | "Ungültiges Zeichen" |  
| HTML1500 | "Tag kann nicht automatisch geschlossen werden.  Verwenden Sie ein explizites schließendes Tag. " |  
| HTML1501 | "Unerwartetes Ende der Datei." |  
| HTML1502 | "Unerwarteter DOCTYPE.  Nur ein DOCTYPE ist zulässig und muss vor allen Elementen auftreten. " |  
| HTML1503 | "Unerwartetes Starttag" |  
| HTML1504 | "Unerwartetes Endtag." |  
| HTML1505 | "Unerwartetes Zeichen Token" |  
| HTML1506 | "Unerwartetes Token" |  
| HTML1507 | "Unerwartetes Zeichen: U + 0000 NULL.  NULL-Zeichen sollten nicht verwendet werden. " |  
| HTML1508 | "Nicht übereinstimmende Endtag." |  
| HTML1509 | "Nicht übereinstimmende Endtag." |  
| HTML1510 | "Erforderliche Knoten nicht im Bereich." |  
| HTML1511 | "Unerwartetes Head-Level-Element außerhalb von \ <Head \ >." |  
| HTML1512 | "Nicht übereinstimmende Endtag." |  
| HTML1513 | "Extra \ <HTML \ > Tag-lieb.  Pro Dokument sollte nur ein \ <HTML \ >-Tag vorhanden sein. " |  
| HTML1514 | "Extra \ <Body \ > Tag gefunden.  Pro Dokument sollte nur ein \ <Body \ >-Tag vorhanden sein. " |  
| HTML1515 | "Gefunden \ <Frameset \ > zu weit unten im Dokument.  Dieses Tag sollte auftreten, bevor ein \ <Body \ > erstellt wird. " |  
| HTML1516 | "Ungültige Schachtelung.  Ein Kopf zeilentag, beispielsweise \ <H1 \ > oder \ <H2 \ >, sollte nicht in einem anderen Header-Tag plaziert werden. " |  
| HTML1517 | "Ungültige Schachtelung.  Ein \ <Formular \ >-Tag sollte nicht in einem anderen \ <-Formular \ > gespeichert werden. " |  
| HTML1518 | "Ungültige Schachtelung.  Eine \ <-Schaltfläche \ >-Tag sollte nicht in einer anderen \ <-Schaltfläche \ > gespeichert werden. " |  
| HTML1519 | "Ungültige Schachtelung.  Ein \ <a \ >-Tag sollte nicht in einem anderen \ <a \ > gespeichert werden. " |  
| HTML1520 | "Unerwartetes Starttag: das \ <ISINDEX \ >-Element ist veraltet und sollte nicht verwendet werden." |  
| HTML1521 | "Unerwarteter \ </body\ > oder Ende der Datei.  Alle geöffneten Elemente sollten vor dem Ende des Dokuments geschlossen werden. " |  
| HTML1522 | "Ungültiges Endtag: \ </br\ >.  Verwenden Sie stattdessen \ <BR \ > oder \ <BR/\ >. " |  
| HTML1523 | "Überlappendes Endtag.  Tags sollten so strukturiert sein, wie \ <b \ > \ <i \ > \ </i\ > \ </b\ > statt \ <b \ > \ <i \ > \ </b\ > \ </i\ >. " |  
| HTML1524 | "Ungültiger DOCTYPE.  Der kürzeste gültige DOCTYPE ist \ < \! DOCTYPE HTML \ >. " |  
| HTML1525 | "Unerwartetes HTML-Tag innerhalb fremder Inhalte gefunden \ (MathML/SVG \)." |  
| HTML1526 | "Ungültige Schachtelung.  Ein \ <nobr \ >-Tag sollte nicht in einem anderen \ <nobr \ > gespeichert werden. " |  
| HTML1527 | "DOCTYPE erwartet.  Der kürzeste gültige DOCTYPE ist \ < \! DOCTYPE HTML \ >. " |  
| HTML1528 | "Unerwartetes \ <Bild \ > in HTML-Inhalt.  Verwenden Sie stattdessen \ <IMG \ >. " |  
| HTML1529 | "Ungültiger xmlns: XLink-Attributwert.  Der Wert muss "\ <https://w3.org/1999/xlink\>" sein. " |  
| HTML1530 | "Text, der in einem strukturellen Tabellenelement gefunden wurde.  Der Tabellentext darf nur in \ <Beschriftung \ >, \ <TD \ > oder \ <Th \ > Elemente angeordnet sein. " |  
| HTML1531 | "Ungültiger xmlns-Attributwert.  Bei SVG-Elementen muss der Wert "\ <https://w3.org/2000/svg/\>" sein. " |  
| HTML1532 | "Ungültiger xmlns-Attributwert.  Für MathML-Elemente muss der Wert "\ <https://w3.org/1998/Math/MathML/\>" sein.  |  

## HTTP-Codes  

HTTP-Fehlercodes werden von Remoteservern als Antwort auf Anforderungen zurückgegeben.  Der wahrscheinlich bekannteste ist HTTP404, der zurückgegeben wird, wenn der Server die Seite oder das Dokument nicht finden kann, die im Uniform Resource Identifier \ (URI \) angegeben ist.

| Code | Meldung | Beschreibung |  
| :--- |:--- |:--- |  
| HTTP400 | Ungültige Anforderung | Die Anforderung konnte aufgrund einer ungültigen Syntax nicht vom Server verarbeitet werden.  |  
| HTTP401 | Verweigert | Für die angeforderte Ressource ist eine Benutzerauthentifizierung erforderlich.  |  
| HTTP402 | Zahlung erforderlich | Derzeit nicht im HTTP-Protokoll implementiert.  |  
| HTTP403 | Verboten | Der Server hat die Anfrage verstanden, weigert sich jedoch, ihn zu erfüllen.  |  
| HTTP404 | nicht gefunden | Der Server hat nichts gefunden, das dem angeforderten URI entspricht.  |  
| HTTP405 | Ungültige Methode | Das verwendete HTTP-Verb ist nicht zulässig.  |  
| HTTP406 | keine akzeptabel | Keine für den Client akzeptablen Antworten wurden gefunden.  |  
| HTTP407 | Proxy-Authentifizierung erforderlich | Proxy-Authentifizierung erforderlich.  |  
| HTTP408 | Anforderungs Timeout | Timeout des Servers beim Warten auf die Anforderung.  |  
| HTTP409 | Konflikt | Die Anforderung konnte aufgrund eines Konflikts mit dem aktuellen Zustand der Ressource nicht abgeschlossen werden.  |  
| HTTP410 | Gegangen | Die angeforderte Ressource steht auf dem Server nicht mehr zur Verfügung, und es ist keine Weiterleitungsadresse bekannt.  |  
| HTTP411 | Länge erforderlich | Der Server weigert sich, die Anforderung ohne definierte Inhaltslänge zu akzeptieren.  |  
| HTTP412 | Vorbedingung fehlgeschlagen | Die Vorbedingung, die in einem oder mehreren der Anforderungsheaderfelder angegeben wurde, die beim Testen auf dem Server auf "false" ausgewertet wurden.  |  
| HTTP413 | Nutzlast zu groß | Der Server weigert sich, eine Anforderung zu verarbeiten, da die Anforderungsentität größer ist als der Server bereit oder in der Lage ist, zu verarbeiten.  |  
| HTTP414 | URI zu lang | Der Server weigert sich, die Anforderung zu bedienen, da der Anforderungs-URI länger ist, als der Server interpretieren will.  |  
| HTTP415 | nicht unterstützter Medientyp | Der Server weigert sich, die Anforderung zu warten, da sich die Entität der Anforderung in einem Format befindet, das von der angeforderten Ressource für die angeforderte Methode nicht unterstützt wird.  |  
| HTTP416 | Angeforderter Bereich nicht erfüllbar | Der Server kann den Teil der Datei, den der Client angefordert hat, nicht bereitstellen.  Der Teil kann sich über das Ende der Datei erstrecken.  |  
| HTTP417 | Erwartung fehlgeschlagen | Der Server kann die Anforderungen des Felds "expect Request-Header" nicht erfüllen.  |  
| HTTP418 | IM eine Teekanne | Der Server ist eine Teekanne; Kaffee kann nicht gebraut werden.  |  
| HTTP419 | Authentifizierungs Timeout | Die zuvor gültige Authentifizierung ist abgelaufen.  |  
| HTTP422 | nicht verarbeitende Entität | Die Anforderung war wohlgeformt, konnte aber aufgrund von semantischen Fehlern nicht verarbeitet werden.  |  
| HTTP423 | Gesperrt | Die Ressource, auf die zugegriffen wird, ist gesperrt.  |  
| HTTP424 | fehlerhafte Abhängigkeit | Die Anforderung konnte aufgrund des Fehlers einer vorherigen Anforderung nicht ausgeführt werden.  |  
| HTTP426 | Upgrade erforderlich | Der Client muss zu einem anderen Protokoll wechseln.  |  
| HTTP428 | Voraussetzung erforderlich | Der Ursprungsserver setzt voraus, dass die Anforderung abhängig ist.  |  
| HTTP429 | zu viele Anforderungen | Der Server weigert sich, die Anforderung zu bedienen, da zu viele Anforderungen vom Client übermittelt wurden.  |  
| HTTP431 | zu große Anforderungs Kopffelder | Der Server weigert sich, die Anforderung zu bearbeiten, da ein Kopfzeilenfeld oder alle Kopfzeilenfelder insgesamt größer sind, als der Server bereit oder in der Lage ist, zu verarbeiten.  |  
| HTTP449 | Wiederholen mit | Die Anforderung sollte nach der entsprechenden Aktion wiederholt werden.  |  
| HTTP500 | Server Fehler | Auf dem Server ist eine unerwartete Bedingung aufgetreten, die verhindert, dass die Anforderung erfüllt wird.  |  
| HTTP501 | Nicht unterstützt | Der Server unterstützt nicht die Funktionalität, die erforderlich ist, um die Anforderung zu erfüllen.  |  
| HTTP502 | Fehlerhaftes Gateway | Der Server, der als Gateway oder Proxy fungiert, hat eine ungültige Antwort vom Upstream-Server erhalten, auf den er beim Versuch, die Anforderung zu erfüllen, zugegriffen hat.  |  
| HTTP503 | Dienst nicht verfügbar | Der Dienst ist vorübergehend überlastet.  |  
| HTTP504 | Gateway-Timeout | Timeout der Anforderung beim Warten auf ein Gateway.  |  
| HTTP505 | Version wird nicht unterstützt | Der Server unterstützt oder weigert sich, die HTTP-Protokollversion zu unterstützen, die in der Anforderungsnachricht verwendet wurde.  |  
| HTTP506 | Variante verhandelt auch | Die transparente Inhalts Verhandlung für die Anforderung führte zu Zirkelverweisen.  |  
| HTTP507 | unzureichender Speicherplatz | Der Server kann die zum Ausführen der Anforderung erforderliche Darstellung nicht speichern.  |  
| HTTP508 | Schleife erkannt | Der Server hat eine Endlosschleife beim Warten der Anforderung erkannt.  |  
| HTTP510 | nicht verlängert | Weitere Erweiterungen der Anforderung sind erforderlich, damit der Server Sie erfüllen kann.  |  
| HTTP511 | Netzwerkauthentifizierung erforderlich | Der Client muss sich authentifizieren, um Netzwerkzugriff zu erhalten.  |  

## JavaScript-Syntaxfehler  

JavaScript-Syntaxfehler treten auf, wenn die Struktur einer ihrer Anweisungen gegen eine oder mehrere syntaktische Regeln verstößt.  

| Fehlernummer | Beschreibung |  
| --- | --- |  
| 1019 | [' Umbruch ' außerhalb der Schleife ist nicht möglich](/scripting/javascript/misc/can-t-have-break-outside-of-loop) |  
| 1020 | ["Continue" kann nicht außerhalb der Schleife vorhanden sein](/scripting/javascript/misc/can-t-have-continue-outside-of-loop) |  
| 1030 | [Bedingte Kompilierung ist deaktiviert](/scripting/javascript/misc/conditional-compilation-is-turned-off) |  
| 1027 | ["Standard" kann nur einmal in einer "Switch"-Anweisung angezeigt werden.](/scripting/javascript/misc/default-can-only-appear-once-in-a-switch-statement) |  
| 1005 | [Erwartet ' \ ('](/scripting/javascript/misc/expected-left-parenthesis-javascript) |  
| 1006 | [Erwartet ' \) '](/scripting/javascript/misc/expected-right-parenthesis-javascript) |  
| 1012 | [Erwartet '/'](/scripting/javascript/misc/expected-minus) |  
| 1003 | [Erwartet ":"](/scripting/javascript/misc/expected-colon) |  
| 1004 | [Erwartet ";"](/scripting/javascript/misc/expected-semicolon) |  
| 1032 | ["@" Erwartet](/scripting/javascript/misc/expected-at) |  
| 1029 | ["@End" erwartet](/scripting/javascript/misc/expected-at-end) |  
| 1007 | ["\]" Erwartet](/scripting/javascript/misc/expected-right-square-bracket) |  
| 1008 | ["{" Erwartet](/scripting/javascript/misc/expected-left-curly-brace) |  
| 1009 | ["}" Erwartet](/scripting/javascript/misc/expected-right-curly-brace) |  
| 1011 | [Erwartet ' = '](/scripting/javascript/misc/expected-equal-javascript) |  
| 1033 | ["Catch" erwartet](/scripting/javascript/misc/expected-catch) |  
| 1031 | [Erwartete Konstante](/scripting/javascript/misc/expected-constant) |  
| 1023 | [Erwartete hexadezimale Ziffer](/scripting/javascript/misc/expected-hexadecimal-digit) |  
| 1010 | [Erwarteter Bezeichner](/scripting/javascript/misc/expected-identifier-javascript) |  
| 1028 | [Erwarteter Bezeichner, Zeichenfolge oder Zahl](/scripting/javascript/misc/expected-identifier-string-or-number) |  
| 1024 | ["While" erwartet](/scripting/javascript/misc/expected-while) |  
| 1014 | [Ungültiges Zeichen](/scripting/javascript/misc/invalid-character-javascript) |  
| 1026 | [Beschriftung nicht gefunden](/scripting/javascript/misc/label-not-found) |  
| 1025 | [Beschriftung neu definiert](/scripting/javascript/misc/label-redefined) |  
| 1018 | ["Return"-Anweisung außerhalb der Funktion](/scripting/javascript/misc/return-statement-outside-of-function) |  
| 1002 | [Syntax Fehler](/scripting/javascript/misc/syntax-error-javascript) |  
| 1035 | [Auf throw muss ein Ausdruck in derselben Quellzeile folgen](/scripting/javascript/misc/throw-must-be-followed-by-an-expression-on-the-same-source-line) |  
| 1016 | [Nicht terminierter Kommentar](/scripting/javascript/misc/unterminated-comment) |  
| 1015 | [Nicht terminierte Zeichenfolgenkonstante](/scripting/javascript/misc/unterminated-string-constant-javascript) |  
  
### Skripthost Fehler  

Die folgenden Fehler beziehen sich auf den Skripthost, Sie können Sie jedoch gelegentlich sehen:  
  
| Fehler | HRESULT | Beschreibung |  
| ---| --- | --- |  
| SCRIPT_E_RECORDED | 0x86664004 | Es wurde ein Fehler aufgezeichnet, der zwischen dem Skriptmodul und dem Host übergeben wurde.  Der Host muss den Fehlercode an den Aufrufer übergeben.  |  
| SCRIPT_E_REPORTED | 0x80020101 | Das Skriptmodul hat über IActiveScriptSite:: OnScriptError eine nicht behandelte Ausnahme für den Host gemeldet.  Der Host kann diesen Fehler ignorieren.  |  
| SCRIPT_E_PROPAGATE | 0x8002010 | Ein Skriptfehler, der an den Aufrufer weitergegeben wird, befindet sich möglicherweise in einem anderen Thread.  Der Host sollte den Fehlercode an den Aufrufer übergeben.  |  

## JavaScript-Laufzeitfehler

JavaScript-Laufzeitfehler treten auf, wenn das Skript versucht, eine Aktion auszuführen, die das System nicht ausführen kann.  Möglicherweise werden Laufzeitfehler angezeigt, wenn Variablen Ausdrücke ausgewertet werden oder wenn Speicher zugewiesen wird.

| Fehlernummer | Beschreibung |  
| --- | --- |  
| 5 | [Zugriff verweigert](/scripting/javascript/misc/access-is-denied) |  
| 438 | [Das Objekt unterstützt diese Eigenschaft oder Methode nicht.](/scripting/javascript/misc/object-doesn-t-support-this-property-or-method) |  
| 1001 | Nicht genügend Arbeitsspeicher |  

### Windows-Runtime-Fehler  

 Wenn Sie Windows-Runtime \ (WinRT \)-APIs verwenden, werden möglicherweise JavaScript-Fehler angezeigt, die aus Windows-Runtime-HRESULTs konvertiert wurden.  Die Windows-Runtime-HRESULTs im Bereich von mehr als 0x80070000 werden in JavaScript-Fehler konvertiert, indem der hexadezimale Wert der unteren Bits und die Konvertierung in eine Dezimalzahl übernommen werden.  Beispielsweise wird der HRESULT-0x80070032 in den Dezimalwert 50 konvertiert, und der JavaScript-Fehler ist SCRIPT50.  Der HRESULT-0x80074005 wird in den Dezimalwert 16389 konvertiert, und der JavaScript-Fehler ist SCRIPT16389.

| Fehlernummer | Beschreibung |  
| --- | --- |  
| 5029 | [Die Array Länge muss eine endliche positive Ganzzahl sein.](/scripting/javascript/misc/array-length-must-be-a-finite-positive-integer) |  
| 5030 | [Der Array Länge muss eine endliche positive Zahl zugewiesen werden.](/scripting/javascript/misc/array-length-must-be-assigned-a-finite-positive-number) |  
| 5028 | [Array-oder Arguments-Objekt erwartet](/scripting/javascript/misc/array-or-arguments-object-expected) |  
| 5010 | [Boolescher Wert erwartet](/scripting/javascript/misc/boolean-expected) |  
| 5003 | [Zuweisen eines Funktionsergebnisses nicht möglich](/scripting/javascript/misc/cannot-assign-to-a-function-result) |  
| 5000 | ["This" kann nicht zugewiesen werden.](/scripting/javascript/misc/cannot-assign-to-this) |  
| 5034 | [Zirkelbezug im Wert Argument wird nicht unterstützt](/scripting/javascript/misc/circular-reference-in-value-argument-not-supported) |  
| 5006 | [Date-Objekt erwartet](/scripting/javascript/misc/date-object-expected) |  
| 5015 | [Enumeratorobjekt erwartet](/scripting/javascript/misc/enumerator-object-expected) |  
| 5022 | [Ausnahme ausgelöst und nicht abgefangen](/scripting/javascript/misc/exception-thrown-and-not-caught) |  
| 5020 | [Erwartet ') ' im regulären Ausdruck](/scripting/javascript/misc/expected-right-parenthesis-in-regular-expression-javascript) |  
| 5019 | ["&#93;" in regulärem Ausdruck erwartet](/scripting/javascript/misc/expected-right-square-bracket-in-regular-expression-javascript) |  
| 5023 | [Funktion hat kein gültiges prototype-Objekt](/scripting/javascript/misc/function-does-not-have-a-valid-prototype-object) |  
| 5002 | [Funktion erwartet](/scripting/javascript/misc/function-expected) |  
| 5008 | [Ungültige Zuordnung](/scripting/javascript/misc/illegal-assignment-javascript) |  
| 5021 | [Ungültiger Bereich im Zeichensatz](/scripting/javascript/misc/invalid-range-in-character-set-javascript) |  
| 5035 | [Ungültiges Austausch Argument](/scripting/javascript/misc/invalid-replacer-argument) |  
| 5014 | [JavaScript-Objekt erwartet](/scripting/javascript/misc/javascript-object-expected) |  
| 5001 | [Erwartete Zahl](/scripting/javascript/misc/number-expected) |  
| 5007 | [Objekt erwartet](/scripting/javascript/misc/object-expected) |  
| 5012 | [Objekt Mitglied erwartet](/scripting/javascript/misc/object-member-expected) |  
| 5016 | [Reguläres Ausdrucksobjekt erwartet](/scripting/javascript/misc/regular-expression-object-expected) |  
| 5005 | [Zeichenfolge erwartet](/scripting/javascript/misc/string-expected) |  
| 5017 | [Syntax Fehler in regulärem Ausdruck](/scripting/javascript/misc/syntax-error-in-regular-expression-javascript) |  
| 5026 | [Die Anzahl der Dezimalstellen liegt außerhalb des gültigen Bereichs](/scripting/javascript/misc/the-number-of-fractional-digits-is-out-of-range) |  
| 5027 | [Die Genauigkeit liegt außerhalb des gültigen Bereichs](/scripting/javascript/misc/the-precision-is-out-of-range) |  
| 5025 | [Der zu decodierende URI ist keine gültige Codierung](/scripting/javascript/misc/the-uri-to-be-decoded-is-not-a-valid-encoding) |  
| 5024 | [Der zu codierende URI enthält ein ungültiges Zeichen](/scripting/javascript/misc/the-uri-to-be-encoded-contains-an-invalid-character) |  
| 5009 | [Undefined Identifier](/scripting/javascript/misc/undefined-identifier) |  
| 5018 | [Unerwarteter Quantifizierer](/scripting/javascript/misc/unexpected-quantifier-javascript) |  
| 5013 | [VBArray erwartet](/scripting/javascript/misc/vbarray-expected) |  

## Sicherheitscodes

Sicherheitsfehler Codes sind im `SEC7xxx` Format wie. `SEC7113`  Diese Fehler entsprechen den Sicherheitsbedingungen, die von Microsoft Edge erzwungen werden, wie beispielsweise gemischter Inhalt und nach Verfolgungs Schutz.

| Code | Meldung | Beschreibung | Vorgeschlagene Lösung |  
| :--- |:--- |:--- |:--- |  
| SEC7111 | "Https-Sicherheit wird durch [Name der Ressource] beeinträchtigt" | Eine Secure Hypertext Transfer Protocol \ (HTTPS \)-Seite enthält Inhalte aus einer nicht sicheren Quelle.  | Stellen Sie sicher, dass alle Inhalte auf der Seite, einschließlich Skripts, Stylesheet-Objekten und Bildern, aus HTTPS-Quellen stammen.  |  
| SEC7112 | "Skript von [URL] wurde aufgrund eines fehlenden MIME-Typs blockiert" | Der HTTP-Antwortheader für die JavaScript-Datei, die durch die URL angegeben wird, verfügt über eine "X-Content-Type-Optionen: nosniff"-Kopfzeile und hat keine erkannte Inhaltstyp Deklaration.  | Aktualisieren Sie den Server, um den richtigen Inhaltstyp für die JavaScript-Datei (wie Text/JavaScript, Anwendung/JavaScript ", beispielsweise \) im HTTP-Antwortheader zu senden.  Weitere Informationen und eine vollständige Liste der Inhaltstypen finden Sie unter [Änderungen der MIME-Behandlung in Internet Explorer](https://blogs.msdn.microsoft.com/ie/2010/10/26/mime-handling-changes-in-internet-explorer/).  |  
| SEC7113 | "CSS wurde aufgrund einer Nichtübereinstimmung des MIME-Typs ignoriert" | Ein importiertes Stylesheet wurde nicht verwendet, da sich der falsche MIME-Typ im HTTP-Header befand.  | Stellen Sie sicher, dass die Stylesheetdatei mit dem richtigen HTTP-Antwortheader geliefert wird, der den Inhaltstyp Text/CSS enthält.  Weitere Informationen finden Sie unter [Änderungen der MIME-Behandlung in Internet Explorer](https://blogs.msdn.microsoft.com/ie/2010/10/26/mime-handling-changes-in-internet-explorer/).  |  
| SEC7114 | "Ein Download auf dieser Seite wurde durch den Tracking-Schutz blockiert. [Hier angegebene URL] " | Der Benutzer hat ein Skript oder einen Inhalt mithilfe des nach Verfolgungs Schutzes blockiert.  | Keine – Benutzer initiiert.  |  
| SEC7115 | ": besuchte und: Verknüpfungs Formate können nur nach Farbe abweichen.  Einige Formatvorlagen wurden nicht angewendet auf: besucht. " | Es wurden mehrere Attribute, wie Schriftart oder Schriftgrad, mithilfe der Stile "besucht" und "Link" geändert.  | Ändern Sie nur das Color-Attribut.  |  
| SEC7116 | "Zugriff verweigert.  Fehler beim widerrufen der Ursprungs-URL: [URL]. " | Ein Skript, das eine andere Ursprungssite als das BLOB hat, hat versucht, eine BLOB-URL zu widerrufen.  Aufgrund von BLOB-Ursprungs Richtlinien ist der Versuch fehlgeschlagen.  | Stellen Sie sicher, dass alle BLOB-URLs mithilfe von Skripts aus derselben Ursprungssite wie dem Dokument, das die BLOB-URL erstellt hat, widerrufen werden.  |  
| SEC7120 | "Origin [Domäne] wurde in der Kopfzeile" Access-Control-Allow-Origin "nicht gefunden. | In der Antwort auf Ihr XMLHttpRequest-Element wurde der Header "Access-Control-Allow-Origin" mit einem Wert zurückgegeben, der den Ursprungswert Ihrer Website nicht enthält oder entspricht.  | Die Ressource gibt die richtige Art von Kopfzeilen Codes zurück, lässt Ihre Website jedoch nicht zu.  Wenden Sie sich an den für die Ressource zuständigen Entwickler, und bitten Sie ihn, seine Zugriffssteuerung-Allow-Origin-Kopfzeile so zu aktualisieren, dass Ihre Website zulässig ist.  Sie können Sie auf [CORS for XMLHttpRequest in IE10](https://blogs.msdn.microsoft.com/ie/2012/02/09/cors-for-xhr-in-ie10/) verweisen, um weitere Informationen zu CORS in den Antwortheadern zu erhalten.  |  
| SEC7121 | "Platzhalter in Access-Control-Allow-Origin ist nicht zulässig, wenn das Anmeldeinformationen-Flag auf" true "festgelegt ist. | Der Server gibt "Access-Control-Allow-Origin: *" in den Kopfzeilen zurück, dies ist jedoch nicht zulässig, `withCredentials` wenn das Flag im XMLHttpRequest auf " **true** " festgelegt ist.  | Der serverseitige Handler muss so geändert werden, dass ein Access-Control-Allow-Origin-Header zurückgegeben wird, der Ihren Ursprungspunkt speziell für diesen Typ von Anforderung zulässt.  Wenn Sie den serverseitigen Handler nicht steuern, müssen Sie sich mit dem Entwickler unterhalten, der dies tut.  |  
| SEC7122 | "Das Flag für Anmeldeinformationen wurde auf true festgelegt, aber die Zugriffssteuerung-Allow-Credentials war nicht vorhanden oder wurde nicht auf" true "festgelegt. | Ein XMLHttpRequest wurde mit dem `withCredentials` Flag erstellt.  Entweder wurde eine Zugriffssteuerung-Allow-Credentials-Kopfzeile nicht zurückgegeben oder mit einem anderen Wert als " **true**" zurückgegeben.  | Möglicherweise liegt ein Problem mit Ihren Anmeldeinformationen oder der Antwort des Servers vor.  Informationen zu Anforderungen mit Anmeldeinformationen finden Sie in der [XMLHttpRequest-Spezifikation für Ebene 2](https://w3.org/TR/XMLHttpRequest2/) .  |  
| SEC7123 | "Request-Kopfzeile [Kopfzeile] war in der Liste" Zugriffssteuerung-Allow-Header "nicht vorhanden." | Ein benutzerdefinierter Kopfzeilentyp war in der Anforderung enthalten, aber die Liste der Access-Control-Allow-Headers der Antwort wurde nicht berücksichtigt.  | Stellen Sie sicher, dass der Server benutzerdefinierte Kopfzeilen zulässt und die Person, die in der Anforderung gesendet wird, ausdrücklich zulässt.  |  
| SEC7124 | "Die Request-Methode [Methode] war in der Liste der Zugriffssteuerung-Allow-Methoden nicht vorhanden." | Eine Anforderungsmethode wie "Post" wurde im XMLHttpRequest verwendet, aber die Antwort hat einen Header der Zugriffssteuerung-Allow-Methoden zurückgegeben, der Sie nicht enthalten hat.  | Stellen Sie sicher, dass der Server diese Art von Anforderungsmethode zulässt und `withCredentials` dass Sie ordnungsgemäß verwenden, wenn diese Methode eingeschränkten Zugriff hat.  |  
| SEC7125 | "XMLHttpRequest für [URL] hat einen Fehler bei der Analyse der Antwortheader verursacht." | Die Antwortheader vom Server konnten nicht analysiert werden, sodass die Anforderung fehlschlug.  | Verwenden Sie das [Tool Netzwerk](https://msdn.microsoft.com/library/dn255004.aspx) , um die Antwortheader zu erfassen und zu überprüfen, um sicherzustellen, dass Sie die [CORS-Spezifikationen](https://w3.org/TR/cors/)erfüllen.  |  
| SEC7126 | "Umleitungen sind für CORS-Preflight-Anfragen nicht zulässig." | Im Origin-Header wurde eine Umleitung erkannt, und der Benutzer-Agent folgt nicht den Umleitungen während eines Preflights.  | Verwenden Sie das [Tool Netzwerk](https://msdn.microsoft.com/library/dn255004.aspx) , um die Anforderungs Kopfzeilen zu erfassen und zu überprüfen und sicherzustellen, dass ein einzelner direkter Ursprung vorhanden ist.  |  
| SEC7127 | "Umleitung wurde für CORS-Anforderung blockiert" | Der Pfad zur CORS-Ressource enthielt eine Umleitung, die gegen Sicherheitsregeln verstoßen hat.  | Stellen Sie sicher, dass Sie den direktsten Pfad zur CORS-Ressource in Ihrem XMLHttpRequest-Objekt haben.  |  
| SEC7128 | "Für CORS-Antwort sind mehrere Header für die Zugriffssteuerung-Allow-Origins nicht zulässig." | Der Antwortheader enthielt mehrere Header für die Zugriffssteuerung-Allow-Origins.  | Dies ist ein serverseitiger Fehler.  Der Server sollte einen einzelnen Zugriffssteuerung-Allow-Origin-Header zurückgeben.  Melden Sie diesen Fehler dem Entwickler, der für die serverseitige Ressource zuständig ist.
| SEC7129 | "Mehrere Header für die Zugriffssteuerung-Allow-Credentials sind für CORS-Antwort nicht zulässig." | Der Antwortheader enthielt mehrere Header für die Zugriffssteuerung-Allow-Credentials.  | Dies ist ein serverseitiger Fehler.  Der Server sollte einen einzigen Header für die Zugriffssteuerung-Allow-Credentials zurückgeben.  Melden Sie diesen Fehler dem Entwickler, der für die serverseitige Ressource zuständig ist.  |  
| SEC7130 | "Potenzielle websiteübergreifende Skripterstellung in [URL].  Der Inhalt wurde vom XSS-Filter geändert. " | Der [XSS-Filter](https://msdn.microsoft.com/library/dd565647.aspx) hat in der Antwort der Ressource potenziell schädliche Inhalte erkannt und den beanstandeten Inhalt entfernt.  | Weitere Informationen zum XSS- [Filter](https://msdn.microsoft.com/library/dd565647.aspx)finden Sie hier.  |  
| SEC7131 | "Die Sicherheit eines IFRAME in einer Sandbox ist potenziell gefährdet, da der Zugriff auf Skripts und denselben Ursprung möglich ist." | Wenn der Inhalt in einem Sandbox-IFRAME aus einer nicht vertrauenswürdigen oder ungesicherten Quelle stammt, kann er der Sandbox entkommen, wenn sowohl Skript Zugriff als auch derselbe Ursprungs Zugriff zulässig sind.  | Hierbei handelt es sich um eine Informationswarnung, die keine Auswirkungen auf die Funktionalität hat.  Wir empfehlen, diese Berechtigungen zu kombinieren, wenn Sie sich nicht sicher sind, was im IFRAME ausgeführt werden soll.  |  
| SEC7132 | "Das Zertifikat, das diese Website schützt, verwendet eine schwache Kryptographie" | Das von dieser Website verwendete TLS-Sicherheitszertifikat verwendet eine schwache Kryptographie | Aktualisieren des TLS-Zertifikats des Servers |  

> [!NOTE]
> Für Websites in der vertrauenswürdigen Sicherheitszone eines Benutzers überprüft Microsoft Edge nicht den MIME-Typ eines Stylesheets.

## SVG-Codes  

DevTools unterstützt derzeit keine umfangreichen skalierbaren Vektorgrafiken \ (SVG \)-Debuggen, aber einige Konsolen Nachrichten werden zur Unterstützung beim Debuggen bereitgestellt.

| Code | Meldung | Beschreibung | Vorgeschlagene Lösung |  
| :--- |:--- |:--- |:--- |  
| SVG5601 | "SVG-Pfaddaten haben ein falsches Format und konnten nicht vollständig analysiert werden." | Die SVG- [Pfad](https://msdn.microsoft.com/library/ff972086.aspx) Zeichenfolge ist nicht richtig formatiert oder enthält nicht erkannte Befehle.  | Überprüfen Sie das Format der Befehle.  |  
| SVG5602 | "SVG-Punktliste hat ein falsches Format und konnte nicht vollständig analysiert werden." | Die Liste der für ein Element verwendeten Punkte, beispielsweise eine [Polylinie](https://msdn.microsoft.com/library/ff972113.aspx), ist falsch formatiert.  | Stellen Sie sicher, dass die Punkte vollständig und für das Koordinatensystem des Benutzers richtig formatiert sind.  |  

## XML-Codes  

XML-Codes sind in Form von XML5xxx wie XML5603.  

| Code | Meldung |  
|:--- |:--- |  
| Xml5001 | "Anwenden der integrierten XSLT-Behandlung" |  
| XML5601 | "MX_E_MX" |  
| XML5602 | "Unerwartetes Ende der Eingabe." |  
| XML5603 | "Unbekannte Codierung." |  
| XML5604 | "Die Codierung kann nicht gewechselt werden." |  
| XML5605 | "Unbekannte Eingabe Codierungs Signatur" |  
| XML5606 | "WC_E_WC" |  
| XML5607 | "Leerzeichen erwartet." |  
| XML5608 | "Semikolon erwartet." |  
| XML5609 | "Erwartet" > "." |  
| XML5610 | "Anführungszeichen erwartet." |  
| XML5611 | "Expected" = "." |  
| XML5612 | "Das < Zeichen ist in Attributwerten nicht zulässig." |  
| XML5613 | "Hexadezimalzahl erwartet." |  
| XML5614 | "Dezimalzahl erwartet." |  
| XML5615 | "Erwartet" ["." |  
| Xml5616 | "Erwartet" ("." |  
| XML5617 | "Ungültiges XML-Zeichen" |  
| XML5618 | "Ungültiges Namenszeichen." |  
| XML5619 | "Falsche Dokument Syntax." |  
| XML5620 | "Falsche CDATA-Abschnitts Syntax." |  
| XML5621 | "Falsche Kommentarsyntax." |  
| XML5622 | "Fehlerhafte bedingte Abschnitts Syntax." |  
| XML5623 | "Fehlerhafte ATTLIST-Deklarationssyntax." |  
| XML5624 | "Fehlerhafte DOCTYPE-Deklarationssyntax." |  
| XML5625 | "Fehlerhafte Element Deklarationssyntax." |  
| XML5626 | "Fehlerhafte Entitäts Deklarationssyntax." |  
| XML5627 | "Falsche Notations Deklarationssyntax." |  
| XML5628 | "Erwartet" NDATA "." |  
| XML5629 | "Erwartet" öffentlich "." |  
| XML5630 | "Erwartetes" System "." |  
| XML5631 | "Ungültiger Name" |  
| XML5632 | "Nur ein Stammelement ist zulässig." |  
| XML5633 | "Endtag-Name stimmt nicht mit dem entsprechenden Start-Tag-Namen überein." |  
| XML5634 | "Es ist bereits ein Attribut mit dem gleichen Namen für dieses Element vorhanden." |  
| XML5635 | "Eine XML-Deklaration ist nur am Anfang der Datei zulässig." |  
| XML5636 | "Leading" XML "." |  
| XML5637 | "Fehlerhafte Text Deklarationssyntax." |  
| XML5638 | "Fehlerhafte XML-Deklarationssyntax." |  
| XML5639 | "Falsche Syntax für Codierungsnamen" |  
| XML5640 | "Falsche Public Identifier-Syntax." |  
| XML5641 | "Parameter-Entitäts Bezüge sind in Markupdeklarationen in einer internen DTD-Teilmenge nicht zulässig." |  
| XML5642 | "Der Ersetzungstext für Parameter Entitäts Bezüge, die zwischen Markupdeklarationen verwendet werden, muss selbst eine Reihe von vollständigen Markupdeklarationen enthalten." |  
| XML5643 | "Eine analysierte Entität darf keinen direkten oder indirekten Verweis auf sich selbst enthalten." |  
| XML5644 | "Der Inhalt der angegebenen Entität ist nicht wohlgeformt." |  
| XML5645 | "Die angegebene Entität wurde nicht deklariert." |  
| XML5646 | "Entitätsverweis darf nicht den Namen einer nicht analysierten Entität enthalten." |  
| XML5647 | "Attributwerte dürfen keine direkten oder indirekten Bezüge auf externe Entitäten enthalten." |  
| XML5648 | "Fehlerhafte Verarbeitungsanweisungssyntax." |  
| XML5649 | "Falsche System-ID-Syntax." |  
| XML5650 | "Ein Fragezeichen erwartet \ (\? \)". |  
| XML5651 | "Der CDATA-Abschnitt-close-Trennzeichen"]] > "darf nicht in Elementinhalten verwendet werden." |  
| XML5652 | "Nicht alle Datenabschnitte wurden gelesen." |  
| XML5653 | "DTD wurde gefunden, ist aber verboten." |  
| XML5654 | "Gefundenes XML: Leerzeichen Attribut mit ungültigem Wert.  Gültige Werte sind "preserve" oder "Default". " |  
| XML5655 | "NC_E_NC" |  
| XML5656 | "Ungültiger qualifizierter Name (Zeichen)." |  
| XML5657 | "Mehrere Doppelpunkte": "darf nicht mit einem qualifizierten Namen erfolgen." |  
| XML5658 | "Ein Doppelpunkt": "darf nicht in einem Namen vorkommen." |  
| XML5659 | "Deklariertes Präfix" |  
| XML5660 | "Das angegebene Präfix wurde nicht deklariert." |  
| XML5661 | "Nicht standardmäßige Namespacedeklarationen dürfen keinen leeren URI aufweisen." |  
| XML5662 | "Das Präfix" XML "ist reserviert und muss den URI"<https://w3.org/XML/1998/namespace/>"aufweisen." |  
| XML5663 | "Das Präfix" xmlns "ist für die Verwendung durch XML reserviert." |  
| XML5664 | "Der XML-Namespace-URI \ ( https://w3.org/XML/1998/namespace/\>\) \ <darf nur dem Präfix" XML "zugewiesen werden." |  
| XML5665 | "Der xmlns-Namespace-URI \ ( https://w3.org/2000/xmlns/\>\) \ <ist reserviert und darf nicht verwendet werden." |  
| XML5666 | "SC_E_SC" |  
| XML5667 | "Die maximale Tiefe verschachtelter Elemente wurde überschritten." |  
| XML5668 | "Maximale Anzahl von Entitäts Erweiterungen wurde überschritten." |  
| XML5669 | "WR_E_WR" |  
| XML5670 | "WR_E_NONWHITESPACE: Writer: angegebene Zeichenfolge ist kein Leerzeichen." |  
| XML5671 | "WR_E_NSPREFIXDECLARED: Writer: Namespace Prefix ist bereits mit einem anderen Namespace deklariert." |  
| XML5672 | "WR_E_NSPREFIXWITHEMPTYNSURI: Writer: kann Prefix nicht mit einem leeren Namespace-URI verwenden." |  
| XML5673 | "WR_E_DUPLICATEATTRIBUTE: Writer: Duplicate-Attribut." |  
| XML5674 | "WR_E_XMLNSPREFIXDECLARATION: Writer: kann das xmlns-Präfix nicht neu definieren." |  
| XML5675 | "WR_E_XMLPREFIXDECLARATION: Writer: XML-Präfix muss über den \ https://w3.org/XML/1998/namespace/\> <-URI verfügen." |  
| XML5676 | "WR_E_XMLURIDECLARATION: Writer: XML-Namespace-URI \ ( https://w3.org/XML/1998/namespace/\>\) \ <muss nur dem Präfix" XML "zugewiesen sein." |  
| XML5677 | "WR_E_XMLNSURIDECLARATION: Writer: xmlns-Namespace-URI \ ( https://w3.org/2000/xmlns/\>\) \ <ist reserviert und darf nicht verwendet werden." |  
| XML5678 | "WR_E_NAMESPACEUNDECLARED: Writer: Namespace ist nicht deklariert." |  
| XML5679 | "WR_E_INVALIDXMLSPACE: Writer: Ungültiger Wert von XML: space-Attribut \ (zulässige Werte sind" Standard "und" preserve "\)." |  
| XML5680 | "WR_E_INVALIDACTION: Writer: Durchführen der angeforderten Aktion würde ein ungültiges XML-Dokument entstehen." |  
| XML5681 | "WR_E_INVALIDSURROGATEPAIR: Writer: input enthält ein ungültiges oder unvollständiges Ersatzzeichenpaar." |  
| XML5682 | "Unerwartetes Zeichen in der Zeichenentität.  Eine Dezimalzahl erwartet. " |  
| XML5683 | "Unerwartetes Zeichen in der Zeichenentität.  Eine hexadezimale Ziffer erwartet. " |  
| XML5684 | "Der Unicode-Wert der angegebenen Zeichenentität ist ungültig." |  
| XML5685 | "Ungültige Codierung." |  
| XML5686 | "Nicht spezifizierter XML-Fehler". |  
