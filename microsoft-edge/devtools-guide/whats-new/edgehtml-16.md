---
description: Features, die dem Microsoft Edge-devtools im Windows 10 Fall Creators Update (EdgeHTML 16) hinzugefügt wurden
title: DevTools in EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, edgehtml 16
ms.custom: seodec18
ms.openlocfilehash: 78ede81e022cc8f0f623ecd33fd2303314ec9cb0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567572"
---
# <span data-ttu-id="f356f-104">DevTools im Windows 10 Fall Creators Update (EdgeHTML 16)</span><span class="sxs-lookup"><span data-stu-id="f356f-104">DevTools in the Windows 10 Fall Creators Update (EdgeHTML 16)</span></span>

<span data-ttu-id="f356f-105">Mit dieser Version haben wir einen wichtigen devtools-Umgestaltungs Aufwand für verbesserte Robustheit und Leistung eingeleitet und außerdem eine Reihe neuer Funktionen hinzugefügt, die Sie heute nutzen können!</span><span class="sxs-lookup"><span data-stu-id="f356f-105">With this release we started a major DevTools refactoring effort for improved robustness and performance, and also added a bunch of new features you can start using today!</span></span> 

<span data-ttu-id="f356f-106">Hier sind die Microsoft Edge devtools-Features, die im Lieferumfang des [Windows 10 Fall Creators Update](/windows/uwp/whats-new/windows-10-build-16299) ([EdgeHTML 16](https://aka.ms/devguide_edgehtml_16)) enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="f356f-106">Here are the Microsoft Edge DevTools features that shipped with the [Windows 10 Fall Creators Update](/windows/uwp/whats-new/windows-10-build-16299) ([EdgeHTML 16](https://aka.ms/devguide_edgehtml_16)).</span></span>

## <span data-ttu-id="f356f-107">Ahnen Ereignis-Listener</span><span class="sxs-lookup"><span data-stu-id="f356f-107">Ancestor event listeners</span></span> 

<span data-ttu-id="f356f-108">Im Bereich " **Ereignisse** " wird nun die Option zum Anzeigen von Ereignislistener hinzugefügt, die für einen Vorgänger des aktuell ausgewählten Elements (im Bereich **Elemente** ) sowie für das Element selbst registriert sind.</span><span class="sxs-lookup"><span data-stu-id="f356f-108">The **Events** pane now adds the option to view event listeners registered on any ancestor of the currently selected element (in the **Elements** panel), in addition to those on the element itself.</span></span> <span data-ttu-id="f356f-109">Darüber hinaus können Sie jetzt die Ereignis-Listener-Anzeige nach *Ereignis* oder *Element*gruppieren.</span><span class="sxs-lookup"><span data-stu-id="f356f-109">Additionally, you can now group the event listener display by either *Event* or *Element*.</span></span> 

![Überwachungsbereich für Ereignisüberwachung](../media/elements_ancestor_events.png)

## <span data-ttu-id="f356f-111">Dom-mutations Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="f356f-111">DOM mutation breakpoints</span></span>

<span data-ttu-id="f356f-112">Sie können jetzt die Breakpoints für die DOM-Mutation so festlegen, dass Sie beim Ändern des ausgewählten Element Knotens in den Debugger umbrochen werden.</span><span class="sxs-lookup"><span data-stu-id="f356f-112">You can now set DOM mutation breakpoints to break into the Debugger whenever a selected element node changes.</span></span> <span data-ttu-id="f356f-113">Klicken Sie **im Element Panel auf** ein beliebiges Element in der Dom-Strukturansicht, und wählen Sie eine oder mehrere der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="f356f-113">From the **Elements** panel, rt-click on any element in the DOM tree view and select one or more of the following:</span></span>

 - <span data-ttu-id="f356f-114">Unterbrechung beim Entfernen des Knotens</span><span class="sxs-lookup"><span data-stu-id="f356f-114">Break on Node removed</span></span>
 - <span data-ttu-id="f356f-115">Umbruch in der Unterstruktur geändert</span><span class="sxs-lookup"><span data-stu-id="f356f-115">Break on Subtree modified</span></span>
 - <span data-ttu-id="f356f-116">Unterbrechen des Attributs geändert</span><span class="sxs-lookup"><span data-stu-id="f356f-116">Break on Attribute modified</span></span>

<span data-ttu-id="f356f-117">Sie können Ihre mutations Haltepunkte im Bereich " **DOM-Haltepunkte** " in den Bereichen **Elemente** oder **Debugger** verwalten.</span><span class="sxs-lookup"><span data-stu-id="f356f-117">You can manage your mutation breakpoints from the **DOM breakpoints** pane in the **Elements** or **Debugger** panels.</span></span>

![Bereich "Dom-Haltepunkte"](../media/elements_dom_breakpoints.png)

## <span data-ttu-id="f356f-119">Unterstützung für CSS at-rule</span><span class="sxs-lookup"><span data-stu-id="f356f-119">CSS at-rule support</span></span>

<span data-ttu-id="f356f-120">CSS-Regeln für "at" (@) werden jetzt unter anderen CSS-Regel Deklarationen im Bereich " **Formatvorlagen** " dargestellt, einschließlich Animations `@keyframes` Regeln (derzeit nur schreibgeschützt), `@supports` Feature-Abfragen und `@media` Abfragen.</span><span class="sxs-lookup"><span data-stu-id="f356f-120">CSS "at" (@) rules are now represented among other CSS rule declarations on the **Styles** pane, including animation `@keyframes` rules (currently limited to read-only), `@supports` feature queries, and `@media` queries.</span></span>

![CSS at-Rules-Prüfung im devtools-Stilbereich](../media/elements_at_rules.png)

## <span data-ttu-id="f356f-122">Bereich "CSS-Schriftarten"</span><span class="sxs-lookup"><span data-stu-id="f356f-122">CSS fonts pane</span></span>

<span data-ttu-id="f356f-123">CSS `@font-face` -Regeln verfügen nun über einen eigenen Bereich für **Schriftarten** , in dem angezeigt wird, wo die Schriftart aus (*lokal* oder *Netzwerk*) geladen wird und wie viele Zeichen Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="f356f-123">CSS `@font-face` rules now have their own dedicated **Fonts** pane that displays where the font is loaded from (*Local* or *Network*) and how many characters are using it.</span></span> <span data-ttu-id="f356f-124">Wenn eine Schriftart aus dem Netzwerk geladen wird, zeigt devtools die Regel, die Sie importiert hat, zusammen mit dem Alias und dem Schriftarttyp an.</span><span class="sxs-lookup"><span data-stu-id="f356f-124">If a font is loaded from the network,  DevTools will display the rule that imported it along with its alias and font type.</span></span>

![CSS-Schriftartinformationen](../media/elements_fonts.png)

## <span data-ttu-id="f356f-126">CSS-Unterstützung für Pseudoelemente</span><span class="sxs-lookup"><span data-stu-id="f356f-126">CSS pseudo-element support</span></span>

<span data-ttu-id="f356f-127">Der Bereich " **Formatvorlagen** " gruppiert nun Pseudoelemente unter ihren eigenen Überschriften und zeigt deren Inhalt nicht mehr als durchgestrichen an.</span><span class="sxs-lookup"><span data-stu-id="f356f-127">The **Styles** pane now groups pseudo-elements under their own headings and no longer displays their content as crossed out.</span></span>

**<span data-ttu-id="f356f-128">Vorher:</span><span class="sxs-lookup"><span data-stu-id="f356f-128">Before:</span></span>**
<br>
![Der generierte Inhalt wurde zuvor durchgestrichen.](../media/gc_before.png)

**<span data-ttu-id="f356f-130">Nachher:</span><span class="sxs-lookup"><span data-stu-id="f356f-130">After:</span></span>**
<br>
![Generierter Inhalt wird nicht mehr durchgestrichen angezeigt](../media/gc_after.png)

## <span data-ttu-id="f356f-132">Verbesserungen der Konsole</span><span class="sxs-lookup"><span data-stu-id="f356f-132">Console improvements</span></span>

<span data-ttu-id="f356f-133">Der **Konsolen** Bereich hat eine UX-Überholung für verbesserte Benutzerfreundlichkeit und eine schnellere, umfassendere IntelliSense-Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="f356f-133">The **Console** panel got a UX overhaul for improved usability and a faster, richer Intellisense experience.</span></span>

<span data-ttu-id="f356f-134">**Vorher:** 
![ Vorherige Konsole</span><span class="sxs-lookup"><span data-stu-id="f356f-134">**Before:**
![Previous console</span></span>](../media/console_old.png)

<span data-ttu-id="f356f-135">**Nach:** 
![ Neue Konsole</span><span class="sxs-lookup"><span data-stu-id="f356f-135">**After:**
![New console</span></span>](../media/console_new.png)

<span data-ttu-id="f356f-136">Diese Verbesserungen wurden auch hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="f356f-136">We also added these improvements:</span></span>

 -  <span data-ttu-id="f356f-137">Verwenden Sie `Shift + Enter` Diese Funktion, um eine zusätzliche Zeile zu einem Befehl hinzuzufügen, bevor Sie Sie Ausführen `Enter` .</span><span class="sxs-lookup"><span data-stu-id="f356f-137">Use `Shift + Enter` to add an additional line to a command before executing it with `Enter`.</span></span> <span data-ttu-id="f356f-138">(Früher gab es eine Umschaltfläche *zum mehrzeiligen/einzeiligen Modus* .)</span><span class="sxs-lookup"><span data-stu-id="f356f-138">(Formerly there was a *Switch to multiline/single-line mode* toggle button.)</span></span>

 - <span data-ttu-id="f356f-139">Die folgenden neuen APIs werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="f356f-139">The following new APIs are supported:</span></span>
    - <span data-ttu-id="f356f-140">[**Console. Table (***Objekt***)**](../console/console-api.md#organizing-log-output) -Methode</span><span class="sxs-lookup"><span data-stu-id="f356f-140">[**console.table(***object***)**](../console/console-api.md#organizing-log-output) method</span></span>
    - <span data-ttu-id="f356f-141">[**getEventListeners (***Objekt***) (Befehl)**](../console/command-line.md#event-listeners)</span><span class="sxs-lookup"><span data-stu-id="f356f-141">[**getEventListeners(***object***)**](../console/command-line.md#event-listeners) command</span></span>
    - <span data-ttu-id="f356f-142">[**Schlüssel (***Objekt***) (Befehl)**](../console/command-line.md#object-inspection)</span><span class="sxs-lookup"><span data-stu-id="f356f-142">[**keys(***object***)**](../console/command-line.md#object-inspection) command</span></span>
    - <span data-ttu-id="f356f-143">Befehl " [**Werte (***Objekt***)**](../console/command-line.md#object-inspection) "</span><span class="sxs-lookup"><span data-stu-id="f356f-143">[**values(***object***)**](../console/command-line.md#object-inspection) command</span></span>
    - <span data-ttu-id="f356f-144">[**$x (***XPath-Ausdruck***)-**](../console/command-line.md#dom-selectors) Auswahl</span><span class="sxs-lookup"><span data-stu-id="f356f-144">[**$x(***xpath expression***)**](../console/command-line.md#dom-selectors) selector</span></span>

 - <span data-ttu-id="f356f-145">Der Formatierungsparameter [**% c ()**](../console/console-api.md#logging-custom-messages) wird jetzt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f356f-145">The [**%c()**](../console/console-api.md#logging-custom-messages) formatting parameter is now supported</span></span>

## <span data-ttu-id="f356f-146">Verbesserungen beim Debuggen</span><span class="sxs-lookup"><span data-stu-id="f356f-146">Debugging improvements</span></span>

<span data-ttu-id="f356f-147">Neben einer Reihe von neuen Features zum Debuggen von PWA- [Dienst Mitarbeitern und-Cache](#progressive-web-app-debugging)hat der Debugger folgende Features hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="f356f-147">In addition to a suite of new features for debugging your [PWA service workers and cache](#progressive-web-app-debugging), the Debugger added these features:</span></span>

### <span data-ttu-id="f356f-148">Konsolidiertes Debuggen für freigegebene Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f356f-148">Consolidated debugging for shared resources</span></span>

<span data-ttu-id="f356f-149">Auch wenn eine Ressource, beispielsweise eine aus CDN geladene Datei, im gesamten Code mehrmals referenziert wird, stellt devtools nun eine einzelne Debug-Instanz für diese Datei bereit, in der Sie dann allgemeine Haltepunkte festlegen können, die unabhängig davon, wo auf die Datei verwiesen wird, aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f356f-149">Even when a resource, such as a file loaded from CDN, is referenced multiple times throughout your code,  DevTools will now provide a single debugging instance for that file where you can then set common breakpoints which will be hit regardless of where that file is referenced.</span></span> <span data-ttu-id="f356f-150">(Zuvor wurde jeder Skriptverweis als eine eindeutige Ressource einer separaten Reihe von Haltepunkten zugeordnet.)</span><span class="sxs-lookup"><span data-stu-id="f356f-150">(Previously each script reference was considered a unique resource would map to a separate set of breakpoints.)</span></span>

### <span data-ttu-id="f356f-151">Live Edit JavaScript mit *edit-on-Idle*</span><span class="sxs-lookup"><span data-stu-id="f356f-151">Live edit JavaScript with *Edit-on-idle*</span></span>

<span data-ttu-id="f356f-152">Sie können jetzt Ihre JavaScript-Live-Sitzung während einer Debugsitzung bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="f356f-152">You can now edit your JavaScript live during a debugging session.</span></span> <span data-ttu-id="f356f-153">Dieses Feature war in der [vorherigen](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) Version (*Windows 10 Creators Update*) experimentell verfügbar (hinter einer Kennzeichnung) und ist jetzt ein permanentes Feature.</span><span class="sxs-lookup"><span data-stu-id="f356f-153">This feature was experimentally available (behind a flag) in the [previous](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) (*Windows 10 Creators Update*) release and now its a permanent feature.</span></span> <span data-ttu-id="f356f-154">Wählen Sie im **Debuggerfenster** einfach eine beliebige Skriptdatei aus, bearbeiten Sie, und klicken Sie dann auf **Speichern** (oder `Ctrl+S` ), um Ihre Änderungen zu testen, wenn der Codeabschnitt das nächste Mal ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f356f-154">Simply select any script file from the **Debugger** panel, edit, then click **Save** (or `Ctrl+S`) to test your changes next time that section of code runs.</span></span> 

![Mit dem Debugger können Sie ein Live-Skript bearbeiten und die Änderungen vergleichen.](../media/debugger_edit_buttons.png) 

<span data-ttu-id="f356f-156">Klicken Sie auf die Schaltfläche **Dokument mit Original vergleichen** , um den Vergleich der Änderungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f356f-156">Click the **Compare document to original** button to view the diff of what you changed.</span></span>

![Vergleichsansicht des bearbeiteten Codes im Debugger](../media/debugger_edit_code.png) 

<span data-ttu-id="f356f-158">Beachten Sie die folgenden Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="f356f-158">Please be aware of the following constraints:</span></span>

- <span data-ttu-id="f356f-159">Die Skriptbearbeitung funktioniert nur in externen *js* -Dateien (und nicht `<script>` in *HTML*eingebettet).</span><span class="sxs-lookup"><span data-stu-id="f356f-159">Script editing only works in external *.js* files (and not embedded `<script>` within *.html*)</span></span>
- <span data-ttu-id="f356f-160">Bearbeitungen werden im Arbeitsspeicher gespeichert und beim erneuten Laden des Dokuments geleert, sodass Sie nicht in der Lage sind, Bearbeitungen in einem `DOMContentLoaded` Handler auszuführen, beispielsweise</span><span class="sxs-lookup"><span data-stu-id="f356f-160">Edits are saved in memory and flushed when the document is reloaded, thus you won’t be able to run edits inside a `DOMContentLoaded` handler, for example</span></span>
- <span data-ttu-id="f356f-161">Derzeit gibt es keine Möglichkeit (wie eine Option " **Speichern** unter"), um Ihre Bearbeitungen auf dem Datenträger von devtools zu speichern.</span><span class="sxs-lookup"><span data-stu-id="f356f-161">Currently there’s no way (such as a **Save As** option) to save your edits to disk from  DevTools</span></span>

## <span data-ttu-id="f356f-162">Kombinationen</span><span class="sxs-lookup"><span data-stu-id="f356f-162">Shortcuts</span></span>

<span data-ttu-id="f356f-163">Sie können devtools nun auf den zuletzt angezeigten Bereich ( `Ctrl+Shift+I` ) oder direkt auf die Konsole () starten, `Ctrl+Shift+J` genau wie in anderen gängigen Browsern.</span><span class="sxs-lookup"><span data-stu-id="f356f-163">You can now launch DevTools to the last viewed panel (`Ctrl+Shift+I`) or directly to the Console (`Ctrl+Shift+J`) just like you would on other major browsers.</span></span>

## <span data-ttu-id="f356f-164">Debuggen von Progressive Web App</span><span class="sxs-lookup"><span data-stu-id="f356f-164">Progressive Web App debugging</span></span>

<span data-ttu-id="f356f-165">Testen Sie die experimentelle Unterstützung für Progressive Web Apps (PWAs) in Microsoft Edge und DevTools, indem Sie die Option " **Dienstmitarbeiter aktivieren** " `about:flags` (und den Neustart von Microsoft Edge) auswählen.</span><span class="sxs-lookup"><span data-stu-id="f356f-165">Test out the experimental support for Progressive Web Apps (PWAs) in Microsoft Edge and  DevTools by selecting the **Enable service workers** option from `about:flags` (and restarting Microsoft Edge).</span></span> <span data-ttu-id="f356f-166">Wenn eine Website **Dienstmitarbeiter** und/oder die **Cache** -API verwendet, werden die Einträge im **Debuggerfenster** für jeden Ursprung aufgefüllt, ähnlich wie bei der Webspeicher-und Cookie-Prüfung.</span><span class="sxs-lookup"><span data-stu-id="f356f-166">If a site makes use of **Service Workers** and/or the **Cache** API,  will populate entries in the **Debugger** panel for each origin, similar to how web storage and cookie inspection work.</span></span>

<span data-ttu-id="f356f-167">Wenn Sie auf einen bestimmten Service Worker-Eintrag klicken, wird die **Übersicht über den Dienstmitarbeiter**geöffnet, auf der Sie die Dienstmitarbeiter Registrierung für den angegebenen Bereich verwalten und eine Test-Push-Benachrichtigung erzwingen können.</span><span class="sxs-lookup"><span data-stu-id="f356f-167">Clicking on a specific service worker entry will open up the **Service Worker Overview**, where you can manage the service worker registration for the given scope and force a test push notification.</span></span> <span data-ttu-id="f356f-168">Sie können auch **Stop** / den**Start** einzelner Dienstmitarbeiter beenden und Sie über ein separates Debuggerfenster über **prüfen** :</span><span class="sxs-lookup"><span data-stu-id="f356f-168">You can also **Stop**/**Start** individual service workers and **Inspect** them from a separate debugger window:</span></span>

![Bereich ' Dienstmitarbeiter Übersicht '](../media/debugger_sw_overview.png)

<span data-ttu-id="f356f-170">Beachten Sie Folgendes zum Debuggen von Service Worker:</span><span class="sxs-lookup"><span data-stu-id="f356f-170">Please note the following about service worker debugging:</span></span>

 - <span data-ttu-id="f356f-171">Beim Debuggen eines Dienst Arbeitsthreads wird eine neue Instanz des devtools, die sich von den Tools der Seite trennt, gestartet, da Dienstmitarbeiter auf mehreren Registerkarten freigegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="f356f-171">Debugging a service worker will launch a new instance of the DevTools separate from the page's tools because service workers can be shared across multiple tabs.</span></span> 
 - <span data-ttu-id="f356f-172">Die [Elemente](../elements.md) und [Emulations](../emulation.md) Panels fehlen im Service Worker-Debugger, da Dienstmitarbeiter im Hintergrund ausgeführt werden und das Front-End Ihrer APP nicht direkt steuern.</span><span class="sxs-lookup"><span data-stu-id="f356f-172">The [Elements](../elements.md) and [Emulation](../emulation.md) panels are absent from the service worker debugger, given that service workers run in the background and do not directly control the front-end of your app.</span></span>
 - <span data-ttu-id="f356f-173">Zurzeit wird der Netzwerkdatenverkehr für einen Dienstmitarbeiter nur von der devtools-Debug-Instanz für diesen Worker und nicht von der zentralen Instanz für die Seite selbst gemeldet.</span><span class="sxs-lookup"><span data-stu-id="f356f-173">Currently network traffic for a service worker is only reported from the DevTools debugging instance for that worker, and not from the central instance for the page itself.</span></span>

<span data-ttu-id="f356f-174">Wenn Sie auf einen bestimmten Cacheeintrag klicken, wird der **Cache** -Manager geöffnet, in dem Sie Cacheeinträge prüfen und optional löschen können (*Anforderungs* -und *Antwort* Schlüssel-Wert-Paare).</span><span class="sxs-lookup"><span data-stu-id="f356f-174">Clicking on a specific cache entry will open up the **Cache** manager, where you can inspect and optionally delete cache entries (*Request* and *Response* key/value pairs).</span></span>