---
description: Überprüfen Sie mithilfe des Speicherbereichs Ihren Webspeicher, IndexedDB, Cookies und Anforderungs-/Antwortcaches.
title: Speicher | DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, web storage, local storage, session storage, indexeddb, cookies, service worker, cache
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3e970ae0d8ca3a43a309eff7b77400aa3ced5b21
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398896"
---
# <a name="storage"></a>Speicher

Verwenden Sie **den Speicherbereich,** um verschiedene lokal zwischengespeicherte Daten zu überprüfen und zu verwalten, einschließlich:  

*   [Webspeicher](#local-and-session-storage-managers) \(Lokaler und Sitzungsspeicher\) Schlüssel-/Wertepaare  
*   [Indizierte strukturierte DB-Daten](#indexeddb-manager)  
*   [Cookies](#cookies-list) für die Domäne  
*   [Cache](#cache-manager) \(Anforderungs-/Antwortpaare\) für das Debuggen von Dienstmitarbeitern  

Erweitern Sie eine dieser Kategorien, und klicken Sie auf einen untergeordneten Eintrag, um die Registerkarte Ressourcen-Manager zu öffnen.  

## <a name="local-and-session-storage-managers"></a>Lokale und Sitzungsspeichermanager  

Verwenden Sie den lokalen Speicher-Manager und den Sitzungsspeicher-Manager, um den Webspeicher für Ihre Seite zu überprüfen und zu verwalten.  

In den **** **Ordnern** Lokaler Speicher und Sitzungsspeicher in der Ressourcenauswahl des Speicherbereichs wird eine Liste der Ursprünge für die Seite angezeigt. [](./debugger.md#resource-picker)  Wenn Sie einen dieser Frames auswählen, wird eine bearbeitbare Tabelle der aktuellen Schlüssel-Wert-Paare geöffnet, die über [Window.localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) oder [Window.sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage)festgelegt wurden, bzw. \(bzw. direkt aus der DevTools [Storage-Liste](#storage-list)\).  

![DevTools Storage Manager](./media/storage_web_storage.png)  

Auf den Registerkarten Lokaler Speicher und Sitzungsspeicher können Sie:  

*   **Aktualisieren** Sie `Ctrl+F5` \( \) die [Speicherliste,](#cookies-list) um die aktuellen Schlüssel-Werte-Paare für die angegebene Domäne zu sehen.  \(Die Liste wird bei Skriptupdates nicht automatisch aktualisiert.\)  
*   **Simulieren Sie das Erreichen des Speichergrenzwerts**  für Microsoft Edge-Webspeicher.  Jede Domäne und Unterdomäne verfügt über einen eigenen Speicherbereich, es gibt jedoch einen kombinierten Grenzwert:  
    *   **Unterdomänen**: bis zu 5 MBs Speicherplatz  
    *   **Domänen:** bis zu 10 MBs Speicherplatz  
    *   **Gesamt für alle Domänen:** bis zu 50 MBs Speicherplatz  

   Der Sitzungsspeicher wird gelöscht, sobald die letzte Browserregisterkarte, die auf den Ursprung des Browsers verweisen, geschlossen wird.  Lokale Speichereinträge bleiben auf unbestimmte Zeit bestehen, bis sie programmgesteuert von der Seite oder manuell vom Benutzer gelöscht werden:  

   **Einstellungen**  >  **Löschen von Browserdaten**  >  **Cookies und gespeicherte Websitedaten**  

![Löschen von Browserdaten aus dem Bereich "Microsoft Edge-Einstellungen"](./media/settings_clear_browsing_data.png)  

### <a name="storage-list"></a>Speicherliste  

In der Tabelle Speicherliste können Sie:  

*   **Überprüfen und sortieren Sie Ihre** Paare, indem Sie in der Tabelle auf einen der `key/value` Spaltennamen klicken.  
*   **Bearbeiten** Sie `Key` das und eines `Value` vorhandenen Eintrags, indem Sie in die Zelle klicken.  
*   **Löschen** Sie `Del` \( \) einen Eintrag aus der Kontextmenüoption mit der rechten Maustaste, **Element löschen**.  
*   **Fügen** Sie ein neues Paar hinzu, indem Sie auf die leere Zeile am `key/value` unteren Rand der Tabelle klicken.  

### <a name="shortcuts"></a>Tastenkombinationen

| Aktion | Tastenkombination |  
|:--- |:--- |  
| Aktualisieren | `Ctrl`+`F5` |  
| Element löschen | `Del` |  
| Kopieren ausgewählter Elemente | `Ctrl`+`C` |  
| Alle auswählen | `Ctrl`+`A` |  

## <a name="indexeddb-manager"></a>IndexedDB Manager  

Verwenden Sie **die Registerkarte IndexedDB,** um die lokal auf einem Clientcomputer gespeicherten strukturierten Daten zu überprüfen und zu verwalten.  Insbesondere können Sie Ihre Objektspeicher und -indizes überprüfen/sortieren und aktualisieren sowie einzelne Schlüsselwerteinträge löschen.  

> [!TIP]
> Sie können unsere [Audiomixerdemo](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) verwenden, um den *IndexedDB-Manager* in Microsoft Edge DevTools zu testen.  

Verwenden Sie das Menü Microsoft **Edge-Einstellungen,** um alle indexedDB-Daten zu löschen, die für den aktuellen Benutzer in Microsoft Edge gespeichert sind:  

**...** >  **Einstellungen**  >  **Löschen von Browserdaten**  >  **Cookies und gespeicherte Websitedaten**  

Der Ordner in der Ressourcenauswahl des Debuggers zeigt eine Liste der Ursprünge der von der `IndexedDB` Seite geladenen Ressourcen an. [](./debugger.md#resource-picker)  Alle IndexedDB \(IDB\)-Datenbanken werden zusammen mit ihren Objektspeichern unter dem Ursprung aufgelistet.  

![DevTools IndexedDB Manager](./media/storage_indexeddb.png)  

### <a name="indexeddb-toolbar"></a>IndexedDB Toolbar  

Über die IndexedDB-Symbolleiste können Sie:  

*   **Aktualisieren** Sie \( \), um die aktuellen Einträge im Objektspeicher oder `Ctrl` + `F5` -index Ihrer Datenbank zu sehen.  Der IndexedDB-Manager aktualisiert die Datenbank nicht automatisch, wenn Änderungen an der Datenbank vorgenommen werden.  

### <a name="object-store-entries-list"></a>Liste der Objektspeichereinträge  

Im Objektspeicher oder in der Indextabelle können Sie:  

*   **Überprüfen und sortieren Sie** Ihre Schlüssel-Wert-Paare, indem Sie auf einen beliebigen Spaltennamen in der Tabelle klicken.  
*   **Refresh** \( `Ctrl` + `F5` \)  
*   **Löschen Sie das** Element \( `Del` \), um den ausgewählten Eintrag im Objektspeicher oder -index zu entfernen.  Sie können dies auch über [](#context-menu) die Kontextmenüoption Löschen mit der rechten Maustaste **tun.**  
*   **Kopieren Sie ausgewählte Elemente** \( `Ctrl` + `C` \), um das ausgewählte Element in die Zwischenablage zu kopieren.  Sie können dies auch über [](#context-menu) die Kontextmenüoption "Ausgewähltes **Element kopieren" mit der rechten**Maustaste tun.  
*   **Wählen Sie** alle \( `Ctrl` + `A` \) aus, um alle Einträge im Objektspeicher oder -index auszuwählen.  Sie können dies auch über [](#context-menu) die Kontextmenüoption **"Alle auswählen" mit**der rechten Maustaste tun.  

Die Spalten des Objektspeichers oder der Indextabelle sind sortierbar:  

| Spalte | Beschreibung |  
|:--- |:--- |  
| Schlüssel | Name des Schlüssel-Wert-Paars \(identisch mit **Primärschlüssel**\) beim Iterieren über einen Objektspeicher; Name des Indexschlüssels \(aktueller Schlüssel des Cursors\) beim Iterieren eines Indexes |  
| Primärschlüssel | Name des Schlüssel-Wert-Paars \(Weitere Informationen zu IDB-Schlüsseln finden Sie unter **MDN-Web-Dokumente** \) [](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database) |  
| Wert | Wert des Schlüssel-Wert-Paares |  

Weitere Informationen zu [IndexedDB-Konzepten](https://developer.mozilla.org/docs/Web/API/IndexedDB_API)und -Verwendung finden Sie in DEN MDN-Web-Dokumenten. **  

### <a name="context-menu"></a>Kontextmenü  

Zusätzlich zur [ *IndexedDB-Symbolleiste* ](#indexeddb-toolbar)können Sie Ihre Daten auch in Objektspeichern **** oder Indizes über das Kontextmenü und/oder die Tastenkombinationen [verwalten.](#shortcuts)  

### <a name="shortcuts"></a>Tastenkombinationen

| Aktion | Tastenkombination |  
|:--- |:--- |  
| Aktualisieren | `Ctrl`+`F5` |  
| Schlüssel-Wert-Paar löschen | `Del` |  
| Kopieren ausgewählter Elemente | `Ctrl`+`C` |  
| Alle auswählen | `Ctrl +`A' |  

## <a name="cookies-manager"></a>Cookies-Manager  

Verwenden Sie den Cookies-Manager, um die Cookies für die angegebene Domäne zu überprüfen und zu verwalten.  

Der Ordner in der Ressourcenauswahl des Debuggers zeigt eine Liste der Ursprünge der von der `Cookies` Seite geladenen Ressourcen an. [](./debugger.md#resource-picker)  Wenn Sie einen dieser Frames auswählen, wird eine Tabelle geöffnet, die die aktuellen Cookies darstellt, die entweder vom [HTTP-Header](https://developer.mozilla.org/docs/Web/HTTP/Cookies) oder über ein Skript mit [Document.cookie festgelegt werden.](https://developer.mozilla.org/docs/Web/API/Document/cookie)  

![DevTools Cookies Manager](./media/storage_cookies.png)  

Auf der Registerkartensymbolleiste Cookies können Sie:  

*   **Aktualisieren** Sie `Ctrl` + `F5` \( \) die [Liste Cookies,](#cookies-list) um den aktuellen Satz von Cookies für die angegebene Domäne zu sehen.  \(Die Liste wird nicht automatisch aktualisiert.\)  
*   **Löschen Sie alle** Cookies \( `Ctrl` + `Shift` + `Del` \) \(session and permanent\) für den Pfad der aktuellen Seite.  
*   **Löschen Sie alle Sitzungscookies** \( `Ctrl` + `Del` \) für den Pfad der aktuellen Seite.  

Um Ihre Cookiesliste vollständig zu löschen, müssen Sie möglicherweise alle Cookies für **die** Domäne über die Symbolleiste [des](./network.md#toolbar) Netzwerkpanels löschen.  

### <a name="cookies-list"></a>Liste der Cookies  

In der Listentabelle Cookies können Sie:  

*   **Überprüfen und sortieren Sie** Ihre Cookies, indem Sie auf einen beliebigen Spaltennamen in der Tabelle klicken.  
*   **Bearbeiten** Sie `Name` das und eines `Value` vorhandenen Cookies, indem Sie in die Zelle klicken.  
*   **Löschen** Sie `Del` \( \) ein Cookie aus der Kontextmenüoption mit [der](#context-menu) rechten Maustaste, `Delete cookie` .  
*   **Fügen** Sie ein neues Sitzungscookie für die angegebene hinzu, indem Sie unten in der Tabelle auf die leere `Domain/Path` Zeile klicken.  Dies funktioniert nur für Sitzungscookies. Dauerhafte Cookies \(mit bestimmten Ablaufdatum\) müssen mit herkömmlichen Methoden festgelegt werden.  Die Werte und werden automatisch entsprechend der Position `Domain` `Path` der Seite gefüllt.  

Die Spalten der Liste Cookies können sortiert werden:

| Spalte | Beschreibung |  
| :--- | :--- |  
| Name | Name des Cookies |  
| Wert | Wert des Cookies |  
| Domäne | Hostname des Cookies \(kann leer sein\) |  
| Pfad | URL-Pfad für das Cookie \(kann leer sein\) |  
| Läuft ab | Maximale Lebensdauer des Cookies als HTTP-Datumsstempel.  Wenn nein `Expires` oder `Max-Age` festgelegt wurde, wird der Eintrag als Sitzungscookie betrachtet.  |  
| Nur HTTP | Gibt an, ob das Cookie mit Direktive festgelegt wurde, was angibt, dass von JavaScript nicht auf das Cookie `HttpOnly` zugegriffen werden kann. |  
| Sicherheit | Gibt an, ob das Cookie mit der Direktive festgelegt wurde, und gibt an, dass es nur über eine Anforderung mit SSL und dem HTTPS-Protokoll an den `Secure` Server gesendet wird.  |  

Weitere Informationen zu Cookieeigenschaften finden Sie in der [Set-Cookie-Referenz](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) für MDN-Webdoks. ****  

### <a name="context-menu"></a>Kontextmenü  

Zusätzlich zur Registerkartensymbolleiste Cookies [können](#cookies-manager)Sie Ihre Cookies **** auch über das Kontextmenü und/oder die Tastenkombinationen [verwalten.](#shortcuts)  

### <a name="shortcuts"></a>Tastenkombinationen  

| Aktion | Tastenkombination |  
|:--- |:--- |  
| Aktualisieren | `Ctrl`+`F5` |  
| Löschen des Cookies | `Del` |  
| Löschen aller Cookies | `Ctrl`+`Shift`+`Del` |  
| Löschen aller Sitzungscookies | `Ctrl`+`Del` |  
| Kopieren ausgewählter Elemente | `Ctrl`+`C` |  
| Alle auswählen | `Ctrl`+`A` |  

### <a name="cache-manager"></a>Cache-Manager  

Wenn Sie auf einen bestimmten Cacheeintrag **** klicken, wird der Cache-Manager des Dienstmitarbeiters geöffnet, in dem Sie Cacheeinträge \( und `Request` Schlüssel-/Wertpaare\ überprüfen und optional `Response` löschen können):  

![Cache-Manager](./media/storage_cache.png)  

### <a name="shortcuts"></a>Tastenkombinationen  

#### <a name="cache-manager"></a>Cache-Manager  

| Aktion | Tastenkombination |  
|:--- |:--- |  
| Aktualisieren | `Ctrl`+`F5` |  
| Element löschen | `Del` |  
| Kopieren ausgewählter Elemente | `Ctrl`+`C` |  
| Alle auswählen | `Ctrl`+`A` |  
