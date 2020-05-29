---
title: Tastenkombinationen für Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 031457d33bf3cf102380c01d9084619313612124
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601894"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->





# Tastenkombinationen für Microsoft Edge devtools   





Diese Seite ist ein Verweis auf Tastenkombinationen in Microsoft Edge devtools.

Sie können auch Tastenkombinationen in QuickInfos finden. Zeigen Sie mit der Maus auf ein UI-Element von devtools, um die QuickInfo anzuzeigen. Wenn das Element über eine Verknüpfung verfügt, wird es in der QuickInfo eingeschlossen.

## Tastenkombinationen zum Öffnen von devtools   

Um devtools zu öffnen, drücken Sie die folgenden Tastenkombinationen, während sich der Cursor auf den Viewport des Browsers konzentriert:

| Aktion | Windows | macOS |  
|:--- |:--- |:--- |  
| Öffnen eines beliebigen Panels, das Sie zuletzt verwendet haben | `F12` oder`Control`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Öffnen des **Konsolen** Panels | `Control`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Öffnen des **Elements** -Panels | `Control`+`Shift`+`C` | `Command`+`Shift`+`C`oder`Command`+`Option`+`C` |  

## Globale Tastenkombinationen   

Die folgenden Tastenkombinationen stehen in den meisten, wenn nicht allen devtools-Panels zur Verfügung.

| Aktion | Windows | macOS |  
|:--- |:--- |:--- |  
| **Einstellungen** anzeigen | `?` oder `F1` | `?` oder`Function`+`F1` |  
| Fokussieren des nächsten Panels | `Control`+`]` | `Command`+`]` |  
| Fokussieren des vorherigen Panels | `Control`+`[` | `Command`+`[` |  
| Wechseln Sie zu der zuletzt verwendeten [Docking-Position][DevtoolsCustomizeIndexPlacement] zurück.  Wenn sich devtools in der Standardposition für die gesamte Sitzung befindet, wird diese Verknüpfung devtools in einem separaten Fenster Abdocken. | `Control`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| [DeviceMode][DevtoolsDeviceModeIndex] umschalten | `Control`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Umschalten des **Element Modus prüfen** | `Control`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Öffnen des [Befehlsmenüs][DevtoolsCommandMenuIndex] | `Control`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Umschalten der [Schublade][DevtoolsCustomizeIndexDrawer] | `Escape` | `Escape` |  
| Normales Reload | `F5` oder`Control`+`R` | `Command`+`R` |  
| Hard Reload | `Control`+`F5`oder`Control`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Suchen nach Text im aktuellen Bereich  Wird in den Bereichen **Audits**, **Anwendung**und **Sicherheit** nicht unterstützt | `Control`+`F` | `Command`+`F` |  
| Öffnet die Registerkarte " **Suchen** " in der [Schublade][DevtoolsCustomizeIndexDrawer], in der Sie nach Text über alle geladenen Ressourcen suchen können. | `Control`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Öffnen einer Datei im **Quellen** Panel | `Control`+`O`oder`Control`+`P` | `Command`+`O`oder`Command`+`P` |  
| Heranzoomen | `Control`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Verkleinern | `Control`+`-` | `Command`+`-` |  
| Standardzoom Stufe wiederherstellen | `Control`+`0` | `Command`+`0` |  
| Ausführen eines Snippets | Drücken Sie `Control` + `O` zum Öffnen des [Befehlsmenüs][DevtoolsCommandMenuIndex], geben `!` Sie gefolgt vom Namen des Skripts ein, und drücken Sie dann `Enter` | Drücken Sie `Command` + `O` zum Öffnen des [Befehlsmenüs][DevtoolsCommandMenuIndex], geben `!` Sie gefolgt vom Namen des Skripts ein, und drücken Sie dann `Enter` |  

<!-- TODO: make a bug about this UIPlacement link being ambiguous.  -->  
<!-- TODO: Link "Inspect Element Mode" when a good section exists.  -->  

## Tastenkombinationen im Element Panel   

| Aktion | Windows | macOS |  
|:--- |:--- |:--- |  
| Rückgängigmachen der Änderung | `Control`+`Z` | `Command`+`Z` |  
| Änderung wiederholen | `Control`+`Y` | `Command`+`Shift`+`Z` |  
| Markieren des Elements oberhalb/unterhalb des aktuell ausgewählten Elements | `Up Arrow` / `Down Arrow` | `Up Arrow` / `Down Arrow` |  
| Erweitern des aktuell ausgewählten Knotens Wenn der Knoten bereits erweitert ist, wird mit dieser Verknüpfung das Element darunter markiert. | `Right Arrow` | `Right Arrow` |  
| Reduzieren des aktuell ausgewählten Knotens Wenn der Knoten bereits reduziert ist, wird mit dieser Verknüpfung das Element darüber markiert. | `Left Arrow` | `Left Arrow` |  
| Erweitern oder reduzieren des aktuell ausgewählten Knotens und aller untergeordneten Elemente | Halten `Control` + `Alt` Sie die Maustaste gedrückt, und klicken Sie dann auf das Pfeilsymbol neben dem Namen des Elements. | Halten `Option` Sie die Maustaste gedrückt, und klicken Sie dann auf das Pfeilsymbol neben dem Namen des Elements. |  
| Umschalten des Modus zum **Bearbeiten von Attributen** für das aktuell ausgewählte Element | `Enter` | `Enter` |  
| Auswählen des nächsten/vorherigen Attributs nach Eingabe des **Bearbeitungs** Attributmodus | `Tab` / `Shift`+`Tab` | `Tab` / `Shift`+`Tab` |  
| Ausblenden des aktuell ausgewählten Elements | `H` | `H` |  
| " **Als HTML** -Modus Bearbeiten" für das aktuell ausgewählte Element umschalten | `Function`+`F2` | `F2` |  

### Tastenkombinationen für den Bereich "Formatvorlagen"   

| Aktion | Windows | macOS |  
|:--- |:--- |:--- |  
| Wechseln zu der Zeile, in der ein Eigenschaftswert deklariert ist | Halten `Control` und dann auf den Eigenschaftswert klicken | Halten `Command` und dann auf den Eigenschaftswert klicken |  
| Durchlaufen der RBGA-, HSLA-und Hex-Darstellungen eines Color-Werts | Halten `Shift` Sie die Maustaste gedrückt, und klicken Sie dann neben dem Wert auf das Feld **Farbvorschau** . | Halten `Shift` Sie die Maustaste gedrückt, und klicken Sie dann neben dem Wert auf das Feld **Farbvorschau** . |  
| Auswählen der nächsten/vorherigen Eigenschaft oder des nächsten Werts | Klicken Sie auf einen Eigenschaftsnamen oder-Wert, und drücken Sie dann`Tab` / `Shift`+`Tab` | Klicken Sie auf einen Eigenschaftsnamen oder-Wert, und drücken Sie dann`Tab` / `Shift`+`Tab` |  
| Inkrementieren/Dekrementieren eines Eigenschaftswerts durch 0,1 | Klicken Sie auf einen Wert, und drücken Sie dann alt + nach-oben-Taste/`Alt`+`Down Arrow` | Klicken Sie auf einen Wert, und drücken Sie dann `Option` + `Up Arrow` /Wahl + nach-unten-Taste. |  
| Inkrementieren/Dekrementieren eines Eigenschaftswerts um 1 | Klicken Sie auf einen Wert, und drücken Sie dann`Up Arrow` / `Down Arrow` | Klicken Sie auf einen Wert, und drücken Sie dann`Up Arrow` / `Down Arrow` |  
| Inkrementieren/Dekrementieren eines Eigenschaftswerts um 10 | Klicken Sie auf einen Wert, und drücken Sie dann`Shift`+`Up Arrow` / `Shift`+`Down Arrow` | Klicken Sie auf einen Wert, und drücken Sie dann`Shift`+`Up Arrow` / `Shift`+`Down Arrow` |  
| Inkrementieren/Dekrementieren eines Eigenschaftswerts durch 100 | Klicken Sie auf einen Wert, und drücken Sie dann`Control`+`Up Arrow` / `Control`+`Down Arrow` | Klicken Sie auf einen Wert, und drücken Sie dann`Command`+`Up Arrow` / `Command`+`Down Arrow` |  

## Tastenkombinationen für das Quellen Panel   

| Aktion | Windows | macOS |  
|:--- |:--- |:--- |  
| Unterbrechen der Skriptlaufzeit \ (sofern zurzeit ausgeführt wird \) oder fortsetzen \ (Wenn aktuell angehalten \) | `F8` oder`Control`+`\` | `F8` oder`Command`+`\` |  
| Schritt zum nächsten Funktionsaufruf | `F10` oder`Control`+`'` | `F10` oder`Command`+`'` |  
| Schritt in den nächsten Funktionsaufruf | `F11` oder`Control`+`;` | `F11` oder`Command`+`;` |  
| Schritt aus der aktuellen Funktion | `Shift`+`F11`oder`Control`+`Shift`+`;` | `Shift`+`F11`oder`Command`+`Shift`+`;` |  
| Fortsetzen einer [bestimmten Codezeile während der Pause][DevtoolsJavascriptBreakpointsLOC] | Halten `Control` und dann auf die Codezeile klicken | Halten `Command` und dann auf die Codezeile klicken |  
| Auswählen des Anruf Rahmens unterhalb/oberhalb des aktuell ausgewählten Frames | `Control`+`.` / `Control`+`,` | `Control`+`.` / `Control`+`,` |  
| Speichern von Änderungen an lokalen Änderungen | `Control`+`S` | `Command`+`S` |  
| Alle Änderungen speichern | `Control`+`Alt`+`S` | `Command`+`Option`+`S` |  
| Zur Zeile wechseln | `Control`+`G` | `Control`+`G` |  
| Zu einer Leitungsnummer der aktuell geöffneten Datei springen | Drücken Sie `Control` + `O` zum Öffnen des [Befehlsmenüs][DevtoolsCommandMenuIndex], geben `:` Sie gefolgt von der Zeilennummer ein, und drücken Sie dann `Enter` | Drücken Sie `Command` + `O` zum Öffnen des [Befehlsmenüs][DevtoolsCommandMenuIndex], geben `:` Sie gefolgt von der Zeilennummer ein, und drücken Sie dann `Enter` |  
| Wechseln zu einer Spalte der aktuell geöffneten Datei \ (beispielsweise Zeile 5, Spalte 9 \) | Drücken Sie, `Control` + `O` um das [Befehl-Menü][DevtoolsCommandMenuIndex]zu öffnen, geben Sie `:` dann die Zeilennummer und dann eine andere `:` , dann die Spaltennummer ein, und drücken Sie dann `Enter` | Drücken Sie, `Command` + `O` um das [Befehl-Menü][DevtoolsCommandMenuIndex]zu öffnen, geben Sie `:` dann die Zeilennummer und dann eine andere `:` , dann die Spaltennummer ein, und drücken Sie dann `Enter` |  
| Wechseln Sie zu einer Funktionsdeklaration \ (wenn die aktuell geöffnete Datei HTML oder ein Skript \) ist, oder eine Regelgruppe \ (Wenn aktuell geöffnete Datei ein Stylesheet ist). | Drücken Sie `Control` + `Shift` + `O` , geben Sie den Namen der Deklaration/des Regelsatzes ein, oder wählen Sie ihn in der Liste der Optionen aus. | Drücken Sie `Command` + `Shift` + `O` , geben Sie den Namen der Deklaration/des Regelsatzes ein, oder wählen Sie ihn in der Liste der Optionen aus. |  
| Schließen der aktiven Registerkarte | `Alt`+`W` | `Option`+`W` |  

### Tastenkombinationen im Code-Editor   

| Aktion | Windows | macOS |  
|:--- |:--- |:--- |  
| Löschen aller Zeichen im letzten Wort bis zum Cursor | `Control`+`Delete` | `Option`+`Delete` |  
| Hinzufügen oder Entfernen eines [Haltepunkts für die Codezeile][DevtoolsJavascriptBreakpointsLOC] | Fokussieren Sie den Cursor auf die Linie, und drücken Sie dann`Control`+`B` | Fokussieren Sie den Cursor auf die Linie, und drücken Sie dann`Command`+`B` |  
| Zur passenden Klammer wechseln | `Control`+`M` | `Control`+`M` |  
| Einzeilen-Kommentar umschalten Wenn mehrere Zeilen markiert sind, fügt devtools am Anfang jeder Zeile einen Kommentar ein. | `Control`+`/` | `Command`+`/` |  
| Wählen/deaktivieren Sie das nächste Vorkommen des Worts, auf dem sich der Cursor befindet. Jedes Vorkommen wird gleichzeitig hervorgehoben. | `Control`+`D` / `Control`+`U` | `Command`+`D` / `Command`+`U` |  

## Tastenkombinationen im Leistungs Panel   

| Aktion | Windows | macOS |  
|:--- |:--- |:--- |  
| Aufzeichnung starten/beenden | `Control`+`E` | `Command`+`E` |  
| Speichern der Aufzeichnung | `Control`+`S` | `Command`+`S` |  
| Aufzeichnung laden | `Control`+`O` | `Command`+`O` |  

## Tastenkombinationen im Speicher Panel 

| Aktion | Windows | macOS |  
|:--- |:--- |:--- |  
| Aufzeichnung starten/beenden | `Control`+`E` | `Command`+`E` |  

## Tastenkombinationen im Konsolenfeld   

| Aktion | Windows | macOS |  
|:--- |:--- |:--- |  
| AutoVervollständigen-Vorschlag akzeptieren | `Right Arrow` oder `Tab` | `Right Arrow` oder `Tab` |  
| Vorschlag für AutoVervollständigen ablehnen | `Escape` | `Escape` |  
| Vorherige Anweisung abrufen | `Up Arrow` | `Up Arrow` |  
| Nächste Anweisung abrufen | `Down Arrow` | `Down Arrow` |  
| Fokussieren der **Konsole** | `Control`+ `` ` `` | `Control`+`` ` `` |  
| Deaktivieren der **Konsole** | `Control`+`L` | `Command`+`K`oder`Option`+`L` |  
| Erzwingen eines mehrzeiligen Eintrags Beachten Sie, dass devtools mehrzeilige Szenarien standardmäßig erkennen sollte, sodass diese Verknüpfung in der Regel nicht erforderlich ist. | `Shift`+`Enter` | `Command`+`Return` |  
| Ausführen | `Enter` | `Return` |  
| Erweitern aller untergeordneten Eigenschaften eines Objekts, das auf der Konsole protokolliert wird | Halten `Alt` Sie die Maustaste **Expand**gedrückt, und klicken Sie auf erweitern. ![][ImageExpandIcon] | Halten `Alt` Sie die Maustaste **Expand**gedrückt, und klicken Sie auf erweitern. ![][ImageExpandIcon] |  

 



<!-- image links -->  

[ImageExpandIcon]: /microsoft-edge/devtools-guide-chromium/media/expand-icon.msft.png  

<!-- links -->  

[DevtoolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Schublade – Anpassen der Microsoft Edge-devtools"  
[DevtoolsCustomizeIndexPlacement]: /microsoft-edge/devtools-guide-chromium/customize/index#change-devtools-placement "Ändern der devtools-Platzierung – Anpassen der Microsoft Edge-devtools"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Simulieren von mobilen Geräten mit dem Gerätemodus in Microsoft Edge devtools"  
[DevtoolsJavascriptBreakpointsLOC]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Code Haltepunkte – Anleitung zum Anhalten des Codes mit Haltepunkten in Microsoft Edge devtools"  

<!--[201705ReleaseNotesContinue]: whats-new/2017/05/devtools-release-notes#continue  -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/shortcuts) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
