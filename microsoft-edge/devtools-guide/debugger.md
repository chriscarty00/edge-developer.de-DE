---
description: Verwenden Sie den Debugger, um den Code zu durchlaufen und zu behandeln.
title: Debugger-devtools (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Debugger, Debuggen, Haltepunkte, Uhren, Dienstmitarbeiter, Cache-API, Web-Speicher, Cookies
ms.custom: seodec18
ms.openlocfilehash: 722277618cd8d6d5d6dba4f2a8bd3a28b6466f77
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882919"
---
# Debugger-devtools (EdgeHTML)

Verwenden Sie den **Debugger** , um Code zu durchlaufen, Uhren und Haltepunkte einzurichten, Live den Code zu bearbeiten und ihre Caches zu überprüfen. Testen und Problembehandlung für Ihren Code durch:

- [Durch](#resource-picker) suchen und [Suchen](#file-search) von Code aus ihren geladenen Quelldateien
- [Steuern des Ausführungsflusses](#toolbar) , während Sie den Code schrittweise durchlaufen
- [Verwalten von Seiten Speicherressourcen](./storage.md#cache-manager), einschließlich [Servicemitarbeitern und Cache](./service-workers.md), [Cookies](./storage.md#cookies-list) und [Webspeicher](./storage.md#local-and-session-storage-managers)  
- [Festlegen von Haltepunkten und Live Bearbeitung](#debug-window) des Codes während der Ausführung
- [Nachverfolgen und Bearbeiten von lokalen Variablen](#watches) beim Debuggen
- [Ausblenden oder Anzeigen von asynchronem Code und Bibliothekscode](#call-stack) aus Ihrem callstack nach Bedarf
- [Hinzufügen spezieller Haltepunkte](#breakpoints) für XMLHttpRequests, Ereignisse und [DOM-Mutationen](#dom-breakpoints)

![Der Microsoft Edge devtools-Debugger](./media/debugger.png)

Es gibt drei Möglichkeiten, eine Debugsitzung zu starten.

1. **Festlegen eines Haltepunkts** Wenn die Ausführung des Codes erreicht ist, geben Sie den Debugger ein und können den Code schrittweise durchlaufen.
2. **Initiieren Sie eine Unterbrechung im Code.** Klicken Sie auf die*Symbolleisten* Schaltfläche [**Pause**](#toolbar) (Symbol) oder `Ctrl+Shift+B` . Der Debugger wird bei der nächsten Ausführungsanweisung unterbrechen.
3. **Festlegen des Ausnahme Verhaltens** Verwenden Sie das Menü zum [**Ändern des Ausnahme Verhaltens**](#toolbar) ( `Ctrl+Shift+E` ), um den Debugger zu unterbrechen, wenn der Code eine Ausnahme auslöst. Standardmäßig ist der Debugger *auf Ausnahmen nie unterbrechen*eingestellt, aber Sie werden in der Konsole protokolliert.

## Ressourcenauswahl

Häufig ist der erste Schritt beim Debuggen das Festlegen von Haltepunkten im Code, den Sie zur Problembehandlung durchsuchen. Sie können alle Codedateien finden, die aktuell von der Seite geladen sind, und zwar im Bereich *Ressourcenauswahl* , einschließlich *HTML-, CSS* -und *js* -Dateien.

 Wenn Sie auf einen Dateieintrag klicken, wird im [Debugfenster](#debug-window) eine Registerkarte für diese Datei geöffnet, und der Text des Datei namens wird fett formatiert, um dies anzugeben (als *devtools-Guide-* Dateiname in der Abbildung oben). Sie können dann die Haltepunkte innerhalb dieser Datei über das [Debug-Fenster](#debug-window)festlegen.

![Debugger-Ressourcenauswahl](./media/debugger_resource_picker.png)

Im Kontextmenü der *Ressourcenauswahl* können Sie auch eine Datei als **Bibliothekscode** () kennzeichnen `Ctrl+L` und Ihnen die Möglichkeit geben, [diesen Code im Debugger](#debug-window) zu überspringen und [ihn im **Aufruf** Listenbereich auszublenden](#call-stack). Wenn Sie erneut auf (oder `Ctrl+L` ) klicken, wird die Datei wieder zu Ihrem vorherigen Wert als *mein Code* oder *Bibliothekscode*umgeschaltet.

### Dateisuche

Verwenden Sie den Befehl *in Dateien suchen* ( `Ctrl` + `Shift` + `F` ), wenn Sie über eine bestimmte Zeichenfolge verfügen, die Sie in der Quelle finden möchten. Die Symbolleiste bietet verschiedene Suchoptionen, einschließlich regulärer Ausdrücke. Wenn Sie auf ein Suchergebnis klicken, wird das *Debug-Fenster* auf die angegebene Datei und Zeile ausgerichtet.

![Debugger-Dateisuche (Bereich)](./media/debugger_file_search.png)

## Fenster "Debuggen"

Im *Fenster "Debuggen"* können Sie die Haltepunkte festlegen, den Code schrittweise durchlaufen und das Skript beim Debuggen Live bearbeiten. Klicken Sie links neben einem beliebigen Skriptbefehl, um einen **Haltepunkt**hinzuzufügen (oder zu entfernen). Verwenden Sie den Kontextmenü-oder [**Haltepunkt**](#breakpoints) Bereich, um dem Haltepunkt *eine Bedingung hinzuzufügen* , indem Sie einen logischen Ausdruck bereitstellen, der dazu führt, dass der Debugger unterbricht, wenn er an dieser Stelle *wahr* ausgewertet wird.

![Debug-Fenster Befehle](./media/debugger_window.png)

Weitere Features des Debug-Fensters sind Steuerelemente für:

### 1. Code Bearbeitung

Sie können Ihr JavaScript Live während einer Debugsitzung bearbeiten. Nachdem Sie Ihre Änderungen vorgenommen haben, klicken Sie auf <strong> speichern </strong> ( `Ctrl+S` ), um die Änderungen zu testen, wenn der Codeabschnitt das nächste Mal ausgeführt wird. Wenn Sie nicht gespeicherte Codeänderungen haben, wird vor dem Dateinamen auf der Registerkarte *Debugfenster* ein Sternchen (\ *) angezeigt.

Klicken Sie auf die Schaltfläche **Dokument mit Original vergleichen** , um den Vergleich der Änderungen anzuzeigen.

![Vergleichsansicht des bearbeiteten Codes im Debugger](./media/debugger_edit_code.png)

Beachten Sie die folgenden Einschränkungen:

- Die Skriptbearbeitung funktioniert nur in externen *js* -Dateien (und nicht `<script>` in *HTML*eingebettet).
- Bearbeitungen werden im Arbeitsspeicher gespeichert und beim erneuten Laden des Dokuments geleert, sodass Sie nicht in der Lage sind, Bearbeitungen in einem `DOMContentLoaded` Handler auszuführen, beispielsweise
- Derzeit gibt es keine Möglichkeit (wie eine Option " **Speichern** unter"), um Ihre Bearbeitungen auf dem Datenträger aus dem devtools zu speichern.

### 2. Code Formatierung

Verwenden Sie diese Steuerelemente zum Formatieren von minimierte-Code für eine bessere Lesbarkeit beim Debuggen:

#### Pretty Print ( `Ctrl+Shift+P` ) 
Fügt Zeilenumbrüche und geschweifte Klammer Ausrichtung pro JavaScript-Konventionen hinzu. Selbst komprimierter Code, der mit dieser Option besser lesbar ist, kann Funktions-, Auswahl-und Variablennamen aufweisen, die sich wesentlich von dem ursprünglichen Quellcode unterscheiden. In diesen Fällen steht möglicherweise die Option [*Quell Karten umschalten*](#source-maps) zur Verfügung.

#### Zeilenumbruch ( `Alt+W` )
Passt Code an die aktuellen Seitenränder des Debug-Fensters an (wodurch kein horizontaler Bildlauf erforderlich ist).

### 3. Code-Scoping

Sie können den Debugger anweisen, bestimmte Dateien mit der Schaltfläche **als Bibliothekscode markieren** () zu ignorieren `Ctrl+L` . Standardmäßig ist die Schaltfläche " [**nur mein Code Debuggen**](#toolbar) " aktiviert, was bedeutet, dass der Debugger alle Dateien überspringt, die Sie als *Bibliothekscode* markieren, und diese werden im [Aufruf Stapel](#call-stack)des Debuggers nicht angezeigt. Wenn Sie die Schaltfläche (**als mein Code markieren**) drücken, `Ctrl+L` wird dieses Flag entfernt.

Zum Nachverfolgen von Bibliotheken in Debug-Sitzungen können Sie diese Dateien bearbeiten, um eine Standardliste beizubehalten oder Platzhalter für eine Domäne oder einen Dateityp hinzuzufügen:

```JavaScript
%APPDATA%\..\LocalLow\Microsoft\F12\header\MyCode.json and %APPDATA%\..\Local\Microsoft\F12\header\MyCode.json
```

#### Quell Karten

Sie sehen die Schaltfläche " **Quell Karten umschalten** " für Code, der in einer Sprache geschrieben ist, die in JavaScript oder CSS kompiliert wird und eine *Quell Karte* (eine Zwischendatei Zuordnung zur ursprünglichen Quelle) bereitstellt. Mit dieser Option wird der Debugger anweisen, die ursprüngliche Quelle zur Verwendung für das Debuggen darzustellen (und nicht die kompilierte Datei, die im Browser *tatsächlich* ausgeführt wird).

Der devtools überprüft, ob der Compiler, der die JavaScript-Datei generiert hat, einen Kommentar mit dem Namen der Zuordnungsdatei enthielt. Wenn beispielsweise ein Compiler *myfile.js* auf *myfile.min.js*komprimiert hat, wird möglicherweise auch eine Zuordnungsdatei, *myfile.min.js. map* , generiert und ein Kommentar in der komprimierten Datei wie folgt eingefügt:

```JavaScript
//# sourceMappingURL=myfile.min.js.map
```

![Kontextmenü ' Datei Debuggen '](./media/debug_file_contextmenu.png)

Wenn der devtools die Karte nicht automatisch finden kann, können Sie eine Quell Karte für diese Datei auswählen. Klicken Sie mit der rechten Maustaste auf die Registerkarte Datei, um die Option **Quell Karte auswählen** zu finden. 

## Symbolleiste

Verwenden Sie die Debugger- *Symbolleiste* , um zu steuern, wie Sie den Code schrittweise durchlaufen, und welchen Code Sie durchlaufen oder ignorieren möchten. Von hier aus können Sie auch eine Volltextsuche in ihren Codedateien nach bestimmten Zeichenfolgen durchführen.

![Debugger-Symbolleiste](./media/debugger_toolbar.png)

### 1. Continue ( `F5` )/Break ( `Ctrl+Shift+B` )
 **Continue** ( `F5` ) setzt die Codeausführung bis zum nächsten Haltepunkt fort. Wenn Sie die Taste gedrückt halten, `F5` werden vergangene Umbrüche wiederholt verschoben, bis Sie Sie freigeben. 

 **Break** ( `Ctrl+Shift+B` ) bricht in den Debugger nach Ausführung der Next-Anweisung ab.

### 2. Schritt Funktionen ( `F11` , `Ctrl+F10` , `Shift+F11` )
 **Schritt in** ( `F11` ) Schritte in der aufgerufenen Funktion. 

 **Schritt über** ( `Ctrl+F10` ) Schritte über die aufgerufene Funktion. 

 **Schritt aus** ( `Shift+F11` ) führt die Schritte aus der aktuellen Funktion und in die aufrufende Funktion aus. 

 Der Debugger führt einen Schritt zur nächsten Anweisung durch, wenn er nicht an einer Funktion teilhat, wenn diese Befehle verwendet werden.

### 3. unterbrechen auf neue Arbeitskraft ( `Ctrl+Shift+W` )
 Unterbricht die Erstellung eines neuen [Webworkers](https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers).

### 4. Ausnahmeregelung
**Ändern des Ausnahme Verhaltens** ( `Ctrl+Shift+E` ) öffnet Optionen, um zu ändern, wie der Debugger auf Ausnahmen reagiert. Standardmäßig werden Ausnahmen vom Debugger ignoriert und in der [**Konsole**](./console.md)protokolliert. Sie können auswählen, ob Sie *alle Ausnahmen unterbrechen*oder nur diejenigen, die nicht von `try...catch` Anweisungen im Code behandelt werden (*Unterbrechung bei nicht behandelten Ausnahmen*).

### 5. Anzeigen von Suchergebnissen
(Derzeit deaktiviert.) **Ergebnisse einblenden/ausblenden** schaltet die Anzeige der Suchergebnisse [*in Dateien suchen ein*](#6-find-in-files-ctrlf) .

### 6. Suchen in Dateien ( `Ctrl+F` )
 **In Dateien suchen** ( `Ctrl+F` ) wird eine Textsuche durch alle geladenen Dateien in der [*Ressourcenauswahl*](#resource-picker)ausgeführt. Wenn der Text gefunden wird, wird die erste Datei geöffnet, die mit der Suchzeichenfolge übereinstimmt. Drücken `Enter` `F3` Sie oder gelangen Sie zur nächsten Übereinstimmung.

### 7. Debuggen nur meines Codes ( `Ctrl+J` )
 **Nur mein Code Debuggen** ( `Ctrl+J` ) fungiert als Umschaltfläche zum einschließen oder Ausschließen aller Dateien, die als [Bibliothekscode](#3-code-scoping) markiert wurden, während Sie den Debugger durchlaufen.

### 8. Debugger-Verbindung
**Disconnect/Connect-Debugger** ist im Grunde der ein/aus-Schalter für den Debugger.

## Uhren

Verwenden Sie den Bereich " **Überwachungen** ", um einen Katalog aller Objekte und Variablen (**lokal**) sowohl im lokalen als auch im globalen Bereich zu durchsuchen, die für die Anweisung verfügbar sind, die den Fokus des aktuellen Umbruchs im Debugger bildet.

![Überwachungsbereich](./media/debugger_watches.png)

Sie können den Wert bestimmter Variablen nachverfolgen, während Sie an-und ablaufen, indem Sie eine Uhr hinzufügen ("**Überwachung hinzufügen**" `Ctrl+W` ) und bearbeitbare Werte ändern, indem Sie darauf doppelklicken oder im *Kontextmenü*die Option " **Wert bearbeiten** " auswählen. Deaktivieren Sie Ihre Uhren mithilfe **Delete** der `Ctrl+D` Schaltflächen Löschen ()/ **Alle löschen** oder im Kontextmenü. 

## Details

Der *Detail* Bereich umfasst die Registerkarten [**CallStack**](#call-stack), [**Haltepunkte**](#breakpoints) und [**DOM-Haltepunkte**](#dom-breakpoints) .

### Anrufliste

Die Registerkarte " **Anrufliste** " zeigt die funktionskette an, die zum aktuellen Ausführungspunkt geführt hat. Die aktuelle Funktion wird oben angezeigt, und die Anruffunktionen werden in umgekehrter Reihenfolge darunter angezeigt.

![Bereich "Anrufliste"](./media/debugger_callstack.png)

Mit der Schaltfläche " **Bibliotheks Frames einblenden/ausblenden** " ( `Ctrl+Shift+J` ) wird die Ausgabe des [Bibliothekscodes](#3-code-scoping) aus der Aufrufliste umgeschaltet. Verwenden Sie die Option " **Bibliothekscode** " ( `Ctrl+L` ) im *Kontextmenü* , um die Quelle des ausgewählten Frames als Bibliothekscode zu kennzeichnen (oder die Markierung aufzuheben). 

Die Schaltfläche " **asynchrone Frames einblenden/ausblenden** " schaltet die Anzeige von Stämmen für asynchrone Funktionsaufrufe um.

### Breakpoints

Auf der Registerkarte **Haltepunkte** können Sie Haltepunkte und Ereignisablauf Verfolgungs Punkte verwalten, einschließlich Festlegen von Bedingungen, deaktivieren und löschen.

![Registerkarte "Haltepunkte"](./media/debugger_breakpoints.png)

Nachfolgend finden Sie eine Zusammenfassung der verschiedenen Arten von Haltepunkten, die Sie für das Debuggen verwenden können.

Breakpoint-Typ | Beschreibung | So wird es gemacht
:------------ | :------------ | :--------
**Haltepunkt** | Unterbricht den Debugger, unmittelbar bevor die angegebene Codezeile ausgeführt wird. Reguläre Haltepunkte sind am einfachsten festzulegen, wenn Sie eine Anweisung pro Zeile besitzen. | Klicken Sie im [Fenster Debuggen](#debug-window)in den linken Rand neben einer beliebigen Zeile im Code. Ein roter Punkt wird angezeigt, und der Haltepunkt wird gesetzt. Sie können in die Quelle eines beliebigen Haltepunkts springen, indem Sie auf den blauen Text klicken.
**Bedingter Haltepunkt** | Unterbricht, wenn die angegebene Bedingung als *wahr*ausgewertet wird. Dies ist im Wesentlichen ein `if(condition)`  für das Eindringen in den Debugger.  | Zeigen Sie auf der Registerkarte [Haltepunkte](#breakpoints) auf einen vorhandenen Haltepunkt, und klicken Sie auf die Schaltfläche "Bleistift" (*fügen Sie eine Bedingung zu diesem Haltepunkt hinzu*), klicken Sie mit der rechten Maustaste auf einen vorhandenen Haltepunkt, und wählen Sie im Kontextmenü **Bedingung** aus. Geben Sie die "if"-Bedingung an, die an der Haltepunktposition ausgewertet werden soll. 
**XMLHttpRequest-Haltepunkt** (w/optionale Bedingung) | Breaks, wenn eine XMLHttpRequest-Anforderung (XMLHttpRequest) erfüllt wurde. Sie können das XMLHttpRequest `response` -Objekt im Bereich " [**Überwachungen**](#watches) " überprüfen. | Klicken Sie auf der Registerkarte [Haltepunkte](#breakpoints) auf die Schaltfläche " *XMLHttpRequest-Haltepunkt* " (Kreis mit aufwärts-/Abwärtspfeilen). Sie können es wie oben beschrieben in einen *bedingten Haltepunkt* umwandeln.
**Ereignis-Ablaufverfolgungspunkt** | Ruft [`console.log()`](./console/console-api.md#logging-custom-messages) mit einer angegebenen Zeichenfolge als Antwort auf ein bestimmtes Ereignis auf. Verwenden Sie diese Funktion für temporäre Konsolen Protokollierungs Anweisungen, die Sie nicht direkt im Ereignis Handlercode speichern möchten. | Klicken Sie auf der Registerkarte [Haltepunkte](#breakpoints) auf die Schaltfläche *Ereignisablauf Verfolgungs* Punkt (Diamant mit Blitz). Wählen Sie einen **Ereignistyp** für den Trigger und eine **Trace** -Anweisung für die Protokollierung aus.
**Ereignis Haltepunkt** (w/optionale Bedingung) | Unterbricht jedes Mal, wenn ein bestimmtes Ereignis ausgelöst wird. | Klicken Sie auf der Registerkarte [Haltepunkte](#breakpoints) auf die Schaltfläche *Ereignis Haltepunkt* (Kreis mit Blitz). Wählen Sie einen **Ereignistyp** für den Trigger aus, und geben Sie optional eine **Condition** -Anweisung an. 
**Dom-Haltepunkt** | Unterbricht jedes Mal, wenn ein angegebenes Element auf der Seite mutiert wird, beispielsweise wenn die Unterstruktur geändert wird, die Attribute geändert werden oder wenn Sie vom Dom getrennt werden. | Klicken Sie auf der Registerkarte [Elemente](./elements/dom-breakpoints.md) mit der rechten Maustaste auf ein Quellelement, und wählen Sie dann aus den Optionen für *DOM-Haltepunkte* aus. Verwenden Sie die Registerkarte [**DOM-Haltepunkte**](#dom-breakpoints) im *Debugger* oder in den *Elementen* Panels, um Ihre Haltepunkte zu verwalten. 

Bedingte Haltepunkte und Ablaufverfolgungspunkte haben Zugriff auf alle lokalen und globalen Variablen, die sich derzeit im Bereich befinden, wenn Sie in den Debugger einbrechen.

### DOM-Haltepunkte

Verwalten Sie Ihre Dom-mutations Haltepunkte auf der Registerkarte **DOM-Haltepunkte** , einschließlich Deaktivierung, löschen und erneute Bindung.  [DOM-Haltepunkte können](./elements/dom-breakpoints.md) über die *HTML-Strukturansicht* im **Element** Panel gesetzt werden.

![Dom-Haltepunkte (Registerkarte)](./media/debugger_dom_breakpoints.png)

Die Registerkarte *DOM-Haltepunkte* im **Debugger** bietet äquivalente Funktionen für die Registerkarte *DOM-Haltepunkte** im **Element** Panel.

Hier finden Sie weitere Informationen zu den verschiedenen Typen von [DOM-Haltepunkten](./elements/dom-breakpoints.md).

## Verknüpfungen

### Symbolleisten-Tastenkombinationen

Aktion | Tastenkombination
:------------ | :-------------
Suchen | `Ctrl` + `F`
Continue (aus Haltepunkt) | `F5` oder `F8`
Schnell weiter | Halten `F5` oder `F8`
Fortsetzen und aktualisieren | `Ctrl` + `Shift` + `F5`
Brechen | `Ctrl` + `Shift` + `B`
Schritt in | `F11`
Schritt über | `F10`
Aussteigen | `Shift` + `F11`
Unterbrechen auf neue Arbeitskraft | `Ctrl` + `Shift` + `W`
Ändern des Ausnahme Verhaltens (Menü "Öffnen") | `Ctrl` + `Shift` + `E`
Debuggen nur meines Codes | `Ctrl` + `J`

### Tastenkombinationen für die Ressourcenauswahl

Aktion | Tastenkombination
:------------ | :-------------
Als "mein Code/Bibliothekscode" markieren | `Ctrl` + `L`
Datei öffnen | `Ctrl` + `O`, `Ctrl` + `P`
Durchsuchen aller Dateien | `Ctrl` + `Shift` + `F`

### Debuggen von Fenster Tastenkombinationen

Aktion | Tastenkombination
:------------ | :-------------
Haltepunkt entfernen | `F9`
Haltepunkt deaktivieren | `Ctrl` + `F9`
Bedingter Haltepunkt... | `Alt` + `F9`
Kopieren | `Ctrl` + `C`
Speichern | `Ctrl` + `S`
Wechseln Sie zu Zeile... | `Ctrl` + `G`
Nächste Anweisung anzeigen | `Alt` + `Num` + `*`
Ausführen bis Cursor | `Ctrl` + `F10`
Nächste Anweisung setzen | `Ctrl` + `Shift` + `F10`
In Dateiauswahl anzeigen | `Ctrl` + `Alt` + `P`
Zu Definition in Datei wechseln | `Ctrl`+`D`
Suchen von Bezügen in einer Datei | `Ctrl` + `Shift` + `D`
Hübsch gedruckt | `Ctrl` + `Shift` + `P`
Zeilenumbruch | `Alt` + `W`
Als "mein Code/Bibliothekscode" markieren | `Ctrl` + `L`
Deaktivieren/Aktivieren von Registerkarten im Editor **Hinweis:** Wenn Sie die Tastatur verwenden, um im Debugger zu navigieren, können Sie die Tab-Taste erst dann verlassen, wenn Sie die Tab-Taste deaktiviert haben. | `Ctrl` + `M`

### Tastenkombinationen für den Bereich "Uhren"

Aktion | Tastenkombination
:------------ | :-------------
Uhr hinzufügen | `Ctrl` + `W`
Uhr löschen | `Ctrl` + `D`

### Tastenkombinationen für den Detailbereich

| Aktion                             | Tastenkombination                 |
|:-----------------------------------|:-------------------------|
| Anzeigen/Ausblenden von Frames aus dem Bibliothekscode | `Ctrl` + `Shift` + `J`   |
| Aktivieren aller Haltepunkte             | `Ctrl` + `Shift` + `F11` |
