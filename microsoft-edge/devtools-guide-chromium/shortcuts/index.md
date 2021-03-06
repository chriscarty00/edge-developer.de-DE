---
description: Die kanonische Dokumentation für Microsoft Edge DevTools-Tastenkombinationen.
title: Microsoft Edge DevTools-Tastenkombinationen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: c6d51d27ce41ed8192a867cf33555b3880dd3ef9
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398350"
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
   limitations under the License.  -->

# <a name="microsoft-edge-devtools-keyboard-shortcuts"></a>Microsoft Edge DevTools-Tastenkombinationen  

Dieser Artikel ist eine Referenz zu Tastenkombinationen in Microsoft Edge DevTools.

Verknüpfungen finden Sie möglicherweise auch in QuickInfos.  Zeigen Sie auf ein Benutzeroberflächenelement von DevTools, um die QuickInfo angezeigt zu werden.  Wenn das Element über eine Verknüpfung verfügt, enthält die QuickInfo sie.

## <a name="keyboard-shortcuts-for-opening-devtools"></a>Tastenkombinationen zum Öffnen von DevTools  

Wenn Sie DevTools öffnen möchten, wählen Sie die folgenden Tastenkombinationen aus, während sich der Cursor auf den Browseransichtsfenster konzentriert.

| Aktion | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Öffnen Des zuletzt verwendeten Panels | `F12` oder `Control`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Öffnen des **Konsolentools** | `Control`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Öffnen des **Elements-Tools** | `Control`+`Shift`+`C` | `Command`+`Shift`+`C` oder `Command`+`Option`+`C` |  

## <a name="global-keyboard-shortcuts"></a>Globale Tastenkombinationen  

Die folgenden Tastenkombinationen sind in den meisten, wenn nicht in allen DevTools-Panels verfügbar.

| Aktion | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Anzeigen von **Einstellungen** | `?` or `F1` | `?` oder `Function`+`F1` |  
| Fokus auf den nächsten Bereich | `Control`+`]` | `Command`+`]` |  
| Fokussieren des vorherigen Panels | `Control`+`[` | `Command`+`[` |  
| Wechseln Sie zurück zu der [Dockingposition, die][DevtoolsCustomizeIndexPlacement] Sie zuletzt verwendet haben.  Wenn DevTools für die gesamte Sitzung an der Standardposition war, wird DevTools mit dieser Verknüpfung in einem separaten Fenster entfernt. | `Control`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| [Umschalten der Geräteemulation][DevtoolsDeviceModeIndex] | `Control`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| **Umschalten des Inspect-Elementmodus** | `Control`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Öffnen des [Befehlsmenüs][DevtoolsCommandMenuIndex] | `Control`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Umschalten der [Schublade][DevtoolsCustomizeIndexDrawer] | `Escape` | `Escape` |  
| Normale Aktualisierung | `F5` oder `Control`+`R` | `Command`+`R` |  
| Harte Aktualisierung | `Control`+`F5` oder `Control`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Im aktuellen Bereich nach Text suchen.  Nicht unterstützt in **den Überwachungs-,** **Anwendungs-** und **Sicherheitstools** | `Control`+`F` | `Command`+`F` |  
| Öffnet die **Registerkarte Suchen** in der [Drawer][DevtoolsCustomizeIndexDrawer], mit der Sie nach Text in allen geladenen Ressourcen suchen können. | `Control`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Öffnen einer Datei im **Bereich Quellen** | `Control`+`O` oder `Control`+`P` | `Command`+`O` oder `Command`+`P` |  
| Vergrößern | `Control`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Verkleinern | `Control`+`-` | `Command`+`-` |  
| Standardzoom wiederherstellen | `Control`+`0` | `Command`+`0` |  
| Ausführen eines Codeausschnitts | Select `Control` + `O` to open the [Command Menu][DevtoolsCommandMenuIndex], type `!` followed by the name of the script, then select `Enter` | Select `Command` + `O` to open the [Command Menu][DevtoolsCommandMenuIndex], type `!` followed by the name of the script, then select `Enter` |  

<!-- TODO: make a bug about this UIPlacement link being ambiguous.  -->  
<!-- TODO: Link "Inspect Element Mode" when a good section exists.  -->  

## <a name="elements-tool-keyboard-shortcuts"></a>Tastenkombinationen des Elements-Tools  

| Aktion | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Rückgängig machen | `Control`+`Z` | `Command`+`Z` |  
| Wiederholen der Änderung | `Control`+`Y` | `Command`+`Shift`+`Z` |  
| Wählen Sie das Element oben /unterhalb des aktuell ausgewählten Elements aus. | `Up Arrow` / `Down Arrow` | `Up Arrow` / `Down Arrow` |  
| Erweitern Sie den aktuell ausgewählten Knoten.  Wenn der Knoten bereits erweitert wurde, wählt diese Verknüpfung das darunter angezeigte Element aus. | `Right Arrow` | `Right Arrow` |  
| Reduzieren Sie den aktuell ausgewählten Knoten.  Wenn der Knoten bereits reduziert ist, wählt diese Verknüpfung das darüber angezeigte Element aus. | `Left Arrow` | `Left Arrow` |  
| Erweitern oder Reduzieren des aktuell ausgewählten Knotens und aller kinder | Halten `Control` + `Alt` Sie , und wählen Sie dann das **Pfeilsymbol** neben dem Namen des Elements aus. | Halten `Option` Sie , und wählen Sie dann das **Pfeilsymbol** neben dem Namen des Elements aus. |  
| **Umschalten des Bearbeitungsattributmodus** für das aktuell ausgewählte Element | `Enter` | `Enter` |  
| Wählen Sie das nächste /vorherige Attribut aus, nachdem Sie den **Bearbeitungsattributmodus aktiviert** haben. | `Tab` / `Shift`+`Tab` | `Tab` / `Shift`+`Tab` |  
| Ausblenden des aktuell ausgewählten Elements | `H` | `H` |  
| **Umschalten als HTML-Modus** bearbeiten für das aktuell ausgewählte Element | `Function`+`F2` | `F2` |  

### <a name="styles-panel-keyboard-shortcuts"></a>Formatvorlagenbereich-Tastenkombinationen  

| Aktion | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Navigieren Sie zu der Zeile, in der ein Eigenschaftswert deklariert ist | Halten `Control` Sie , und wählen Sie dann den Eigenschaftswert aus. | Halten `Command` Sie , und wählen Sie dann den Eigenschaftswert aus. |  
| Zyklus durch die RBGA-, HSLA- und Hexdarstellungen eines Farbwerts | Halten `Shift` Sie , und wählen Sie dann das Feld **Farbvorschau** neben dem Wert aus. | Halten `Shift` Sie , und wählen Sie dann das Feld **Farbvorschau** neben dem Wert aus. |  
| Wählen Sie die nächste /vorherige Eigenschaft oder den nächsten Wert aus. | Wählen Sie einen Eigenschaftennamen oder -wert aus, und wählen Sie dann aus. `Tab` / `Shift`+`Tab` | Wählen Sie einen Eigenschaftennamen oder -wert aus, und wählen Sie dann aus. `Tab` / `Shift`+`Tab` |  
| Erhöhen /Dekrement eines Eigenschaftswerts um 0,1 | Wählen Sie einen Wert aus, und wählen Sie dann `Alt`+`Up Arrow` / `Alt`+`Down Arrow` | Wählen Sie einen Wert aus, und wählen Sie `Option` + `Up Arrow` dann /Option+Pfeil nach unten aus. |  
| Erhöhen/Dekrement eines Eigenschaftswerts um 1 | Wählen Sie einen Wert aus, und wählen Sie dann `Up Arrow` / `Down Arrow` | Wählen Sie einen Wert aus, und wählen Sie dann `Up Arrow` / `Down Arrow` |  
| Erhöhen/Dekrementierung eines Eigenschaftswerts um 10 | Wählen Sie einen Wert aus, und wählen Sie dann `Shift`+`Up Arrow` / `Shift`+`Down Arrow` | Wählen Sie einen Wert aus, und wählen Sie dann `Shift`+`Up Arrow` / `Shift`+`Down Arrow` |  
| Erhöhen/Dekrementierung eines Eigenschaftswerts um 100 | Wählen Sie einen Wert aus, und wählen Sie dann `Control`+`Up Arrow` / `Control`+`Down Arrow` | Wählen Sie einen Wert aus, und wählen Sie dann `Command`+`Up Arrow` / `Command`+`Down Arrow` |  

## <a name="sources-tool-keyboard-shortcuts"></a>Tastenkombinationen des Quellentools  

| Aktion | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Skriptlaufzeit anhalten \(wenn aktuell ausgeführt\) oder fortsetzen \(wenn derzeit angehalten\) | `F8` oder `Control`+`\` | `F8` oder `Command`+`\` |  
| Schritt über nächsten Funktionsaufruf | `F10` oder `Control`+`'` | `F10` oder `Command`+`'` |  
| Schritt in den nächsten Funktionsaufruf | `F11` oder `Control`+`;` | `F11` oder `Command`+`;` |  
| Schritt aus der aktuellen Funktion | `Shift`+`F11` oder `Control`+`Shift`+`;` | `Shift`+`F11` oder `Command`+`Shift`+`;` |  
| Fahren Sie mit einer [bestimmten Codezeile fort, während sie angehalten wird.][DevtoolsJavascriptBreakpointsLOC] | Halten `Control` Sie , und wählen Sie dann die Codezeile aus. | Halten `Command` Sie , und wählen Sie dann die Codezeile aus. |  
| Wählen Sie den Anrufrahmen unter /über dem aktuell ausgewählten Frame aus. | `Control`+`.` / `Control`+`,` | `Control`+`.` / `Control`+`,` |  
| Speichern von Änderungen an lokalen Änderungen | `Control`+`S` | `Command`+`S` |  
| Speichern aller Änderungen | `Control`+`Alt`+`S` | `Command`+`Option`+`S` |  
| Navigieren zur Zeile | `Control`+`G` | `Control`+`G` |  
| Wechseln zu einer Zeilennummer der aktuell geöffneten Datei | Wählen `Control` + `O` Sie aus, um das [Befehlsmenü zu][DevtoolsCommandMenuIndex]öffnen, geben Sie gefolgt `:` von der Zeilennummer ein, und wählen Sie dann aus. `Enter` | Wählen `Command` + `O` Sie aus, um das [Befehlsmenü zu][DevtoolsCommandMenuIndex]öffnen, geben Sie gefolgt `:` von der Zeilennummer ein, und wählen Sie dann aus. `Enter` |  
| Wechseln zu einer Spalte der aktuell geöffneten Datei \(z. B. Zeile 5, Spalte 9\) | Wählen `Control` + `O` Sie aus, um das [Befehlsmenü][DevtoolsCommandMenuIndex]zu öffnen, geben Sie ein, dann die Zeilennummer, dann eine weitere , dann die `:` `:` Spaltennummer, und wählen Sie dann aus. `Enter` | Wählen `Command` + `O` Sie aus, um das [Befehlsmenü][DevtoolsCommandMenuIndex]zu öffnen, geben Sie ein, dann die Zeilennummer, dann eine weitere , dann die `:` `:` Spaltennummer, und wählen Sie dann aus. `Enter` |  
| Navigieren Sie zu einer Funktionsdeklaration, wenn die aktuelle Datei HTML oder ein Skript ist.  <br />  Navigieren Sie zu einem Regelsatz, wenn es sich bei der aktuellen Datei um ein Stylesheet handelt.  | Wählen Sie aus, und geben Sie `Control` + `Shift` + `O` dann den Namen der Deklaration/des Regelsatzs ein, oder wählen Sie ihn aus der Liste der Optionen aus. | Wählen Sie aus, und geben Sie `Command` + `Shift` + `O` dann den Namen der Deklaration/des Regelsatzs ein, oder wählen Sie ihn aus der Liste der Optionen aus. |  
| Schließen der aktiven Registerkarte | `Alt`+`W` | `Option`+`W` |  

### <a name="code-editor-keyboard-shortcuts"></a>Tastenkombinationen des Code-Editors  

| Aktion | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Löschen aller Zeichen im letzten Wort bis zum Cursor | `Control`+`Delete` | `Option`+`Delete` |  
| Hinzufügen oder Entfernen eines [Codezeile-Haltepunkts][DevtoolsJavascriptBreakpointsLOC] | Fokussieren Sie den Cursor auf die Zeile, und wählen Sie dann `Control`+`B` | Fokussieren Sie den Cursor auf die Zeile, und wählen Sie dann `Command`+`B` |  
| Navigieren zu übereinstimmender Klammer | `Control`+`M` | `Control`+`M` |  
| Einzeilerkommentar umschalten.  Wenn mehrere Zeilen ausgewählt sind, fügen DevTools am Anfang jeder Zeile einen Kommentar hinzu. | `Control`+`/` | `Command`+`/` |  
| Aktivieren oder deaktivieren Sie das nächste Vorkommen des Worts, auf dem sich der Cursor befindet.  Jedes Vorkommen wird gleichzeitig hervorgehoben | `Control`+`D` / `Control`+`U` | `Command`+`D` / `Command`+`U` |  

## <a name="performance-tool-keyboard-shortcuts"></a>Tastenkombinationen des Leistungstools  

| Aktion | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Starten/Beenden der Aufzeichnung | `Control`+`E` | `Command`+`E` |  
| Speichern der Aufzeichnung | `Control`+`S` | `Command`+`S` |  
| Laden der Aufzeichnung | `Control`+`O` | `Command`+`O` |  

## <a name="memory-tool-keyboard-shortcuts"></a>Tastenkombinationen für Speichertools  

| Aktion | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Starten/Beenden der Aufzeichnung | `Control`+`E` | `Command`+`E` |  

## <a name="console-tool-keyboard-shortcuts"></a>Tastenkombinationen für Konsolentools  

| Aktion | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Annahme des Vorschlags für die automatische Vervollständigung | `Right Arrow` or `Tab` | `Right Arrow` or `Tab` |  
| Ablehnen des Vorschlags für die automatische Vervollständigung | `Escape` | `Escape` |  
| Vorherige Anweisung erhalten | `Up Arrow` | `Up Arrow` |  
| Nächste Anweisung erhalten | `Down Arrow` | `Down Arrow` |  
| Fokussieren der **Konsole** | `Control`+ `` ` `` | `Control`+`` ` `` |  
| Löschen der **Konsole** | `Control`+`L` | `Command`+`K` oder `Option`+`L` |  
| Erzwingen eines mehrzeilerigen Eintrags.  Diese Verknüpfung ist meist nicht erforderlich, da DevTools standardmäßig mehrzeige Szenarien erkennen sollte. | `Shift`+`Enter` | `Command`+`Return` |  
| Ausführen | `Enter` | `Return` |  
| Erweitern aller Untereigenschaften eines Objekts, die bei der Konsole protokolliert werden | Halten `Alt` Sie , und wählen Sie dann **Erweitern** \( ![ Erweitern ][ImageExpandIcon] \) aus. | Halten `Alt` Sie , und wählen Sie dann **Erweitern** \( ![ Erweitern ][ImageExpandIcon] \) aus. |  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExpandIcon]: ../media/expand-icon.msft.png  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Ausführen von Befehlen mit der Microsoft Edge DevTools-Befehlsmenüleiste | Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: ../customize/index.md#drawer "Drawer – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndexPlacement]: ../customize/index.md#change-devtools-placement "DevTools-Platzierung ändern – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: ../device-mode/index.md "Emulieren von mobilen Geräten in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsJavascriptBreakpointsLOC]: ../javascript/breakpoints.md#line-of-code-breakpoints "Zeilen-von-Code-Haltepunkte – So halten Sie Ihren Code mit Haltepunkten in Microsoft Edge DevTools-| Microsoft Docs"  

<!--[201705ReleaseNotesContinue]: whats-new/2017/05/devtools-release-notes#continue  -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/shortcuts) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  