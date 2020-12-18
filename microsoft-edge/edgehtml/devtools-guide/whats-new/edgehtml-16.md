---
description: Features, die dem Microsoft Edge-devtools im Windows 10 Fall Creators Update (EdgeHTML 16) hinzugefügt wurden
title: DevTools in EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, edgehtml 16
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2d24b6851e843f491e470b18ccc18d559ed5533d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233654"
---
# DevTools im Windows 10 Fall Creators Update (EdgeHTML 16)

Mit dieser Version haben wir einen wichtigen devtools-Umgestaltungs Aufwand für verbesserte Robustheit und Leistung eingeleitet und außerdem eine Reihe neuer Funktionen hinzugefügt, die Sie heute nutzen können! 

Hier sind die Microsoft Edge devtools-Features, die im Lieferumfang des [Windows 10 Fall Creators Update](/windows/uwp/whats-new/windows-10-build-16299) ([EdgeHTML 16](https://aka.ms/devguide_edgehtml_16)) enthalten sind.

## Ahnen Ereignis-Listener 

Im Bereich " **Ereignisse** " wird nun die Option zum Anzeigen von Ereignislistener hinzugefügt, die für einen Vorgänger des aktuell ausgewählten Elements (im Bereich **Elemente** ) sowie für das Element selbst registriert sind. Darüber hinaus können Sie jetzt die Ereignis-Listener-Anzeige nach *Ereignis* oder *Element*gruppieren. 

![Überwachungsbereich für Ereignisüberwachung](../media/elements_ancestor_events.png)

## Dom-mutations Haltepunkte

Sie können jetzt die Breakpoints für die DOM-Mutation so festlegen, dass Sie beim Ändern des ausgewählten Element Knotens in den Debugger umbrochen werden. Klicken Sie **im Element Panel auf** ein beliebiges Element in der Dom-Strukturansicht, und wählen Sie eine oder mehrere der folgenden Optionen aus:

 - Unterbrechung beim Entfernen des Knotens
 - Umbruch in der Unterstruktur geändert
 - Unterbrechen des Attributs geändert

Sie können Ihre mutations Haltepunkte im Bereich " **DOM-Haltepunkte** " in den Bereichen **Elemente** oder **Debugger** verwalten.

![Bereich "Dom-Haltepunkte"](../media/elements_dom_breakpoints.png)

## Unterstützung für CSS at-rule

CSS-Regeln für "at" (@) werden jetzt unter anderen CSS-Regel Deklarationen im Bereich " **Formatvorlagen** " dargestellt, einschließlich Animations `@keyframes` Regeln (derzeit nur schreibgeschützt), `@supports` Feature-Abfragen und `@media` Abfragen.

![CSS at-Rules-Prüfung im devtools-Stilbereich](../media/elements_at_rules.png)

## Bereich "CSS-Schriftarten"

CSS `@font-face` -Regeln verfügen nun über einen eigenen Bereich für **Schriftarten** , in dem angezeigt wird, wo die Schriftart aus (*lokal* oder *Netzwerk*) geladen wird und wie viele Zeichen Sie verwenden. Wenn eine Schriftart aus dem Netzwerk geladen wird, zeigt devtools die Regel, die Sie importiert hat, zusammen mit dem Alias und dem Schriftarttyp an.

![CSS-Schriftartinformationen](../media/elements_fonts.png)

## CSS-Unterstützung für Pseudoelemente

Der Bereich " **Formatvorlagen** " gruppiert nun Pseudoelemente unter ihren eigenen Überschriften und zeigt deren Inhalt nicht mehr als durchgestrichen an.

**Vorher:**
<br>
![Der generierte Inhalt wurde zuvor durchgestrichen.](../media/gc_before.png)

**Nachher:**
<br>
![Generierter Inhalt wird nicht mehr durchgestrichen angezeigt](../media/gc_after.png)

## Verbesserungen der Konsole

Der **Konsolen** Bereich hat eine UX-Überholung für verbesserte Benutzerfreundlichkeit und eine schnellere, umfassendere IntelliSense-Funktionalität.

**Vorher:** 
![ Vorherige Konsole](../media/console_old.png)

**Nach:** 
![ Neue Konsole](../media/console_new.png)

Diese Verbesserungen wurden auch hinzugefügt:

 -  Verwenden Sie `Shift + Enter` Diese Funktion, um eine zusätzliche Zeile zu einem Befehl hinzuzufügen, bevor Sie Sie Ausführen `Enter` . (Früher gab es eine Umschaltfläche *zum mehrzeiligen/einzeiligen Modus* .)

 - Die folgenden neuen APIs werden unterstützt:
    - [ **Console. Table (**_Objekt_*_)_* ](../console/console-api.md#organizing-log-output) -Methode
    - [ **getEventListeners (**_Objekt_*_)_* (Befehl)](../console/command-line.md#event-listeners)
    - [ **Schlüssel (**_Objekt_*_)_* (Befehl)](../console/command-line.md#object-inspection)
    - Befehl " [ **Werte (**_Objekt_*_)_* ](../console/command-line.md#object-inspection) "
    - [ **$x (**_XPath-Ausdruck_*_)-_* ](../console/command-line.md#dom-selectors) Auswahl

 - Der Formatierungsparameter [**% c ()**](../console/console-api.md#logging-custom-messages) wird jetzt unterstützt.

## Verbesserungen beim Debuggen

Neben einer Reihe von neuen Features zum Debuggen von PWA- [Dienst Mitarbeitern und-Cache](#progressive-web-app-debugging)hat der Debugger folgende Features hinzugefügt:

### Konsolidiertes Debuggen für freigegebene Ressourcen

Auch wenn eine Ressource, beispielsweise eine aus CDN geladene Datei, im gesamten Code mehrmals referenziert wird, stellt devtools nun eine einzelne Debug-Instanz für diese Datei bereit, in der Sie dann allgemeine Haltepunkte festlegen können, die unabhängig davon, wo auf die Datei verwiesen wird, aufgerufen werden. (Zuvor wurde jeder Skriptverweis als eine eindeutige Ressource einer separaten Reihe von Haltepunkten zugeordnet.)

### Live Edit JavaScript mit *edit-on-Idle*

Sie können jetzt Ihre JavaScript-Live-Sitzung während einer Debugsitzung bearbeiten. Dieses Feature war in der [vorherigen](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) Version (*Windows 10 Creators Update*) experimentell verfügbar (hinter einer Kennzeichnung) und ist jetzt ein permanentes Feature. Wählen Sie im **Debuggerfenster** einfach eine beliebige Skriptdatei aus, bearbeiten Sie, und klicken Sie dann auf **Speichern** (oder `Ctrl+S` ), um Ihre Änderungen zu testen, wenn der Codeabschnitt das nächste Mal ausgeführt wird. 

![Mit dem Debugger können Sie ein Live-Skript bearbeiten und die Änderungen vergleichen.](../media/debugger_edit_buttons.png) 

Klicken Sie auf die Schaltfläche **Dokument mit Original vergleichen** , um den Vergleich der Änderungen anzuzeigen.

![Vergleichsansicht des bearbeiteten Codes im Debugger](../media/debugger_edit_code.png) 

Beachten Sie die folgenden Einschränkungen:

- Die Skriptbearbeitung funktioniert nur in externen *js* -Dateien (und nicht `<script>` in *HTML*eingebettet).
- Bearbeitungen werden im Arbeitsspeicher gespeichert und beim erneuten Laden des Dokuments geleert, sodass Sie nicht in der Lage sind, Bearbeitungen in einem `DOMContentLoaded` Handler auszuführen, beispielsweise
- Derzeit gibt es keine Möglichkeit (wie eine Option " **Speichern** unter"), um Ihre Bearbeitungen auf dem Datenträger von devtools zu speichern.

## Tastenkombinationen

Sie können devtools nun auf den zuletzt angezeigten Bereich ( `Ctrl+Shift+I` ) oder direkt auf die Konsole () starten, `Ctrl+Shift+J` genau wie in anderen gängigen Browsern.

## Debuggen von Progressive Web App

Testen Sie die experimentelle Unterstützung für Progressive Web Apps (PWAs) in Microsoft Edge und DevTools, indem Sie die Option " **Dienstmitarbeiter aktivieren** " `about:flags` (und den Neustart von Microsoft Edge) auswählen. Wenn eine Website **Dienstmitarbeiter** und/oder die **Cache** -API verwendet, werden die Einträge im **Debuggerfenster** für jeden Ursprung aufgefüllt, ähnlich wie bei der Webspeicher-und Cookie-Prüfung.

Wenn Sie auf einen bestimmten Service Worker-Eintrag klicken, wird die **Übersicht über den Dienstmitarbeiter**geöffnet, auf der Sie die Dienstmitarbeiter Registrierung für den angegebenen Bereich verwalten und eine Test-Push-Benachrichtigung erzwingen können. Sie können auch **** / den**Start** einzelner Dienstmitarbeiter beenden und Sie über ein separates Debuggerfenster über **prüfen** :

![Bereich ' Dienstmitarbeiter Übersicht '](../media/debugger_sw_overview.png)

Beachten Sie Folgendes zum Debuggen von Service Worker:

 - Beim Debuggen eines Dienst Arbeitsthreads wird eine neue Instanz des devtools, die sich von den Tools der Seite trennt, gestartet, da Dienstmitarbeiter auf mehreren Registerkarten freigegeben werden können. 
 - Die [Elemente](../elements.md) und [Emulations](../emulation.md) Panels fehlen im Service Worker-Debugger, da Dienstmitarbeiter im Hintergrund ausgeführt werden und das Front-End Ihrer APP nicht direkt steuern.
 - Zurzeit wird der Netzwerkdatenverkehr für einen Dienstmitarbeiter nur von der devtools-Debug-Instanz für diesen Worker und nicht von der zentralen Instanz für die Seite selbst gemeldet.

Wenn Sie auf einen bestimmten Cacheeintrag klicken, wird der **Cache** -Manager geöffnet, in dem Sie Cacheeinträge prüfen und optional löschen können (*Anforderungs* -und *Antwort* Schlüssel-Wert-Paare).
