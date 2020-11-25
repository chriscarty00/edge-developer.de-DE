---
description: Die kanonische Dokumentation für Microsoft Edge devtools-Tastenkombinationen.
title: Tastenkombinationen für Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: d24728f493b70db2db9cd9bbe2e7e7c1ef943885
ms.sourcegitcommit: 080759f68a0a158f10dc20d20c14e222ace1be84
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "11189963"
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

Dieser Artikel ist ein Verweis auf Tastenkombinationen in Microsoft Edge devtools.

Sie können auch Tastenkombinationen in QuickInfos finden. Zeigen Sie mit der Maus auf ein UI-Element von devtools, um die QuickInfo anzuzeigen. Wenn das Element über eine Verknüpfung verfügt, wird es in der QuickInfo eingeschlossen.

## Tastenkombinationen zum Öffnen von devtools  

Um devtools zu öffnen, wählen Sie die folgenden Tastenkombinationen aus, während sich der Cursor auf das Viewport des Browsers konzentriert.

| Aktion | Windows/Linux | macOS |  
|:--- |:--- |:--- |  
| Öffnen eines beliebigen Panels, das Sie zuletzt verwendet haben | `F12` oder `Control`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Öffnen des **Konsolen** Panels | `Control`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Öffnen des **Elements** -Panels | `Control`+`Shift`+`C` | `Command`+`Shift`+`C` oder `Command`+`Option`+`C` |  

## Globale Tastenkombinationen  

Die folgenden Tastenkombinationen stehen in den meisten, wenn nicht allen devtools-Panels zur Verfügung.

| Aktion | Windows/Linux | macOS |  
|:--- |:--- |:--- |  
| **Einstellungen** anzeigen | `?` oder `F1` | `?` oder `Function`+`F1` |  
| Fokussieren des nächsten Panels | `Control`+`]` | `Command`+`]` |  
| Fokussieren des vorherigen Panels | `Control`+`[` | `Command`+`[` |  
| Wechseln Sie zu der zuletzt verwendeten [Docking-Position][DevtoolsCustomizeIndexPlacement] zurück.  Wenn sich devtools in der Standardposition für die gesamte Sitzung befinden, wird diese Verknüpfung devtools in einem separaten Fenster Abdocken. | `Control`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| [Geräteemulation][DevtoolsDeviceModeIndex] umschalten | `Control`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Umschalten des **Element Modus prüfen** | `Control`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Öffnen des [Befehlsmenüs][DevtoolsCommandMenuIndex] | `Control`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Umschalten der [Schublade][DevtoolsCustomizeIndexDrawer] | `Escape` | `Escape` |  
| Normales Reload | `F5` oder `Control`+`R` | `Command`+`R` |  
| Hard Reload | `Control`+`F5` oder `Control`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Suchen nach Text im aktuellen Bereich  Wird in den Bereichen **Audits**, **Anwendung**und **Sicherheit** nicht unterstützt | `Control`+`F` | `Command`+`F` |  
| Öffnet die Registerkarte " **Suchen** " in der [Schublade][DevtoolsCustomizeIndexDrawer], in der Sie nach Text über alle geladenen Ressourcen suchen können. | `Control`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Öffnen einer Datei im **Quellen** Panel | `Control`+`O` oder `Control`+`P` | `Command`+`O` oder `Command`+`P` |  
| Heranzoomen | `Control`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Verkleinern | `Control`+`-` | `Command`+`-` |  
| Standardzoom Stufe wiederherstellen | `Control`+`0` | `Command`+`0` |  
| Ausführen eines Snippets | Wählen Sie aus, `Control` + `O` um das [Menübefehl][DevtoolsCommandMenuIndex]zu öffnen, geben Sie `!` gefolgt vom Namen des Skripts ein, und wählen Sie dann `Enter` | Wählen Sie aus, `Command` + `O` um das [Menübefehl][DevtoolsCommandMenuIndex]zu öffnen, geben Sie `!` gefolgt vom Namen des Skripts ein, und wählen Sie dann `Enter` |  

<!-- TODO: make a bug about this UIPlacement link being ambiguous.  -->  
<!-- TODO: Link "Inspect Element Mode" when a good section exists.  -->  

## Tastenkombinationen im Element Panel  

| Aktion | Windows/Linux | macOS |  
|:--- |:--- |:--- |  
| Rückgängigmachen der Änderung | `Control`+`Z` | `Command`+`Z` |  
| Änderung wiederholen | `Control`+`Y` | `Command`+`Shift`+`Z` |  
| Markieren des Elements oberhalb/unterhalb des aktuell ausgewählten Elements | `Up Arrow` / `Down Arrow` | `Up Arrow` / `Down Arrow` |  
| Erweitern des aktuell ausgewählten Knotens Wenn der Knoten bereits erweitert ist, wird mit dieser Verknüpfung das Element darunter markiert. | `Right Arrow` | `Right Arrow` |  
| Reduzieren des aktuell ausgewählten Knotens Wenn der Knoten bereits reduziert ist, wird mit dieser Verknüpfung das Element darüber markiert. | `Left Arrow` | `Left Arrow` |  
| Erweitern oder reduzieren des aktuell ausgewählten Knotens und aller untergeordneten Elemente | Halten `Control` + `Alt` Sie die Maustaste gedrückt, und wählen Sie dann das **Pfeil** Symbol neben dem Namen des Elements aus. | Halten `Option` Sie die Maustaste gedrückt, und wählen Sie dann das **Pfeil** Symbol neben dem Namen des Elements aus. |  
| Umschalten des Modus zum **Bearbeiten von Attributen** für das aktuell ausgewählte Element | `Enter` | `Enter` |  
| Auswählen des nächsten/vorherigen Attributs nach Eingabe des **Bearbeitungs** Attributmodus | `Tab` / `Shift`+`Tab` | `Tab` / `Shift`+`Tab` |  
| Ausblenden des aktuell ausgewählten Elements | `H` | `H` |  
| " **Als HTML-Modus Bearbeiten** " für das aktuell ausgewählte Element umschalten | `Function`+`F2` | `F2` |  

### Tastenkombinationen für den Bereich "Formatvorlagen"  

| Aktion | Windows/Linux | macOS |  
|:--- |:--- |:--- |  
| Wechseln zu der Zeile, in der ein Eigenschaftswert deklariert ist | Halten `Control` Sie den Eigenschaftswert, und wählen Sie ihn aus. | Halten `Command` Sie den Eigenschaftswert, und wählen Sie ihn aus. |  
| Durchlaufen der RBGA-, HSLA-und Hex-Darstellungen eines Color-Werts | Halten `Shift` Sie das Kontrollkästchen **Farbvorschau** neben dem Wert | Halten `Shift` Sie das Kontrollkästchen **Farbvorschau** neben dem Wert |  
| Auswählen der nächsten/vorherigen Eigenschaft oder des nächsten Werts | Wählen Sie einen Eigenschaftsnamen oder-Wert aus, und wählen Sie dann `Tab` / `Shift`+`Tab` | Wählen Sie einen Eigenschaftsnamen oder-Wert aus, und wählen Sie dann `Tab` / `Shift`+`Tab` |  
| Inkrementieren/Dekrementieren eines Eigenschaftswerts durch 0,1 | Wählen Sie einen Wert aus, und wählen Sie dann `Alt`+`Up Arrow` / `Alt`+`Down Arrow` | Wählen Sie einen Wert aus, und wählen Sie dann `Option` + `Up Arrow` /Wahl + nach-unten-Taste |  
| Inkrementieren/Dekrementieren eines Eigenschaftswerts um 1 | Wählen Sie einen Wert aus, und wählen Sie dann `Up Arrow` / `Down Arrow` | Wählen Sie einen Wert aus, und wählen Sie dann `Up Arrow` / `Down Arrow` |  
| Inkrementieren/Dekrementieren eines Eigenschaftswerts um 10 | Wählen Sie einen Wert aus, und wählen Sie dann `Shift`+`Up Arrow` / `Shift`+`Down Arrow` | Wählen Sie einen Wert aus, und wählen Sie dann `Shift`+`Up Arrow` / `Shift`+`Down Arrow` |  
| Inkrementieren/Dekrementieren eines Eigenschaftswerts durch 100 | Wählen Sie einen Wert aus, und wählen Sie dann `Control`+`Up Arrow` / `Control`+`Down Arrow` | Wählen Sie einen Wert aus, und wählen Sie dann `Command`+`Up Arrow` / `Command`+`Down Arrow` |  

## Tastenkombinationen für das Quellen Panel  

| Aktion | Windows/Linux | macOS |  
|:--- |:--- |:--- |  
| Unterbrechen der Skriptlaufzeit \ (sofern zurzeit ausgeführt wird \) oder fortsetzen \ (Wenn aktuell angehalten \) | `F8` oder `Control`+`\` | `F8` oder `Command`+`\` |  
| Schritt zum nächsten Funktionsaufruf | `F10` oder `Control`+`'` | `F10` oder `Command`+`'` |  
| Schritt in den nächsten Funktionsaufruf | `F11` oder `Control`+`;` | `F11` oder `Command`+`;` |  
| Schritt aus der aktuellen Funktion | `Shift`+`F11` oder `Control`+`Shift`+`;` | `Shift`+`F11` oder `Command`+`Shift`+`;` |  
| Fortsetzen einer [bestimmten Codezeile während der Pause][DevtoolsJavascriptBreakpointsLOC] | Halten `Control` Sie die Codezeile, und wählen Sie Sie aus. | Halten `Command` Sie die Codezeile, und wählen Sie Sie aus. |  
| Auswählen des Anruf Rahmens unterhalb/oberhalb des aktuell ausgewählten Frames | `Control`+`.` / `Control`+`,` | `Control`+`.` / `Control`+`,` |  
| Speichern von Änderungen an lokalen Änderungen | `Control`+`S` | `Command`+`S` |  
| Alle Änderungen speichern | `Control`+`Alt`+`S` | `Command`+`Option`+`S` |  
| Zur Zeile wechseln | `Control`+`G` | `Control`+`G` |  
| Zu einer Leitungsnummer der aktuell geöffneten Datei springen | Wählen Sie aus, `Control` + `O` um das [Menübefehl][DevtoolsCommandMenuIndex]zu öffnen, geben `:` Sie gefolgt von der Zeilennummer ein, und wählen Sie dann `Enter` | Wählen Sie aus, `Command` + `O` um das [Menübefehl][DevtoolsCommandMenuIndex]zu öffnen, geben `:` Sie gefolgt von der Zeilennummer ein, und wählen Sie dann `Enter` |  
| Wechseln zu einer Spalte der aktuell geöffneten Datei \ (beispielsweise Zeile 5, Spalte 9 \) | Wählen Sie aus, `Control` + `O` um das [Menübefehl][DevtoolsCommandMenuIndex]zu öffnen, geben Sie `:` dann die Zeilennummer und dann eine andere `:` , dann die Spaltennummer ein, und wählen Sie dann `Enter` | Wählen Sie aus, `Command` + `O` um das [Menübefehl][DevtoolsCommandMenuIndex]zu öffnen, geben Sie `:` dann die Zeilennummer und dann eine andere `:` , dann die Spaltennummer ein, und wählen Sie dann `Enter` |  
| Wechseln Sie zu einer Funktionsdeklaration, wenn es sich bei der aktuellen Datei um ein HTML-Dokument oder ein Skript handelt. <br /> Wechseln Sie zu einem Regelsatz, wenn es sich bei der aktuellen Datei um ein Stylesheet handelt. | Wählen Sie `Control` + `Shift` + `O` aus, geben Sie dann den Namen der Deklaration/des Regelsatzes ein, oder wählen Sie ihn in der Liste der Optionen aus. | Wählen Sie `Command` + `Shift` + `O` aus, geben Sie dann den Namen der Deklaration/des Regelsatzes ein, oder wählen Sie ihn in der Liste der Optionen aus. |  
| Schließen der aktiven Registerkarte | `Alt`+`W` | `Option`+`W` |  

### Tastenkombinationen im Code-Editor  

| Aktion | Windows/Linux | macOS |  
|:--- |:--- |:--- |  
| Löschen aller Zeichen im letzten Wort bis zum Cursor | `Control`+`Delete` | `Option`+`Delete` |  
| Hinzufügen oder Entfernen eines [Haltepunkts für die Codezeile][DevtoolsJavascriptBreakpointsLOC] | Fokussieren Sie den Cursor auf die Linie, und wählen Sie dann `Control`+`B` | Fokussieren Sie den Cursor auf die Linie, und wählen Sie dann `Command`+`B` |  
| Zur passenden Klammer wechseln | `Control`+`M` | `Control`+`M` |  
| Einzeilen-Kommentar umschalten Wenn mehrere Zeilen markiert sind, devtools fügen Sie am Anfang jeder Zeile einen Kommentar hinzu. | `Control`+`/` | `Command`+`/` |  
| Wählen/deaktivieren Sie das nächste Vorkommen des Worts, auf dem sich der Cursor befindet. Jedes Vorkommen wird gleichzeitig hervorgehoben. | `Control`+`D` / `Control`+`U` | `Command`+`D` / `Command`+`U` |  

## Tastenkombinationen im Leistungs Panel  

| Aktion | Windows/Linux | macOS |  
|:--- |:--- |:--- |  
| Aufzeichnung starten/beenden | `Control`+`E` | `Command`+`E` |  
| Speichern der Aufzeichnung | `Control`+`S` | `Command`+`S` |  
| Aufzeichnung laden | `Control`+`O` | `Command`+`O` |  

## Tastenkombinationen im Speicher Panel  

| Aktion | Windows/Linux | macOS |  
|:--- |:--- |:--- |  
| Aufzeichnung starten/beenden | `Control`+`E` | `Command`+`E` |  

## Tastenkombinationen im Konsolenfeld  

| Aktion | Windows/Linux | macOS |  
|:--- |:--- |:--- |  
| AutoVervollständigen-Vorschlag akzeptieren | `Right Arrow` oder `Tab` | `Right Arrow` oder `Tab` |  
| Vorschlag für AutoVervollständigen ablehnen | `Escape` | `Escape` |  
| Vorherige Anweisung abrufen | `Up Arrow` | `Up Arrow` |  
| Nächste Anweisung abrufen | `Down Arrow` | `Down Arrow` |  
| Fokussieren der **Konsole** | `Control`+ `` ` `` | `Control`+`` ` `` |  
| Deaktivieren der **Konsole** | `Control`+`L` | `Command`+`K` oder `Option`+`L` |  
| Erzwingen eines mehrzeiligen Eintrags  Diese Tastenkombination ist überwiegend unnötig, da devtools mehrzeilige Szenarien standardmäßig erkennen sollte. | `Shift`+`Enter` | `Command`+`Return` |  
| Ausführen | `Enter` | `Return` |  
| Erweitern aller unter Eigenschaften eines Objekts, das auf der Konsole protokolliert wird | Halten `Alt` , und wählen Sie **erweitern** \ ( ![ Erweitern ][ImageExpandIcon] \) aus. | Halten `Alt` , und wählen Sie **erweitern** \ ( ![ Erweitern ][ImageExpandIcon] \) aus. |  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExpandIcon]: ./media/expand-icon.msft.png  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ./command-menu/index.md "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools | Microsoft docs"  
[DevtoolsCustomizeIndexDrawer]: ./customize/index.md#drawer "Schublade – Anpassen von Microsoft Edge devtools | Microsoft docs"  
[DevtoolsCustomizeIndexPlacement]: ./customize/index.md#change-devtools-placement "Ändern der devtools-Platzierung – Anpassen von Microsoft Edge-devtools | Microsoft docs"  
[DevtoolsDeviceModeIndex]: ./device-mode/index.md "Emulieren von mobilen Geräten in Microsoft Edge devtools | Microsoft docs"  
[DevtoolsJavascriptBreakpointsLOC]: ./javascript/breakpoints.md#line-of-code-breakpoints "Code Haltepunkte – Anleitung zum Anhalten des Codes mit Haltepunkten in Microsoft Edge devtools | Microsoft docs"  

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