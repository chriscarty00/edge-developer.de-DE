---
description: Überprüfen Ihres Webspeichers, IndexedDB, Cookies und Anforderungs-/Antwort-Caches mithilfe des Speicher Panels
title: DevTools-Speicher
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Web Storage, lokaler Speicher, Sitzungsspeicher, indexeddb, Cookies, Service Worker, Cache
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 90a2e2fdb0f329c3d83f52beb9eba169bdd48520
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233665"
---
# Speicher

Verwenden Sie den **Speicher** Panel, um verschiedene lokal zwischengespeicherte Daten zu überprüfen und zu verwalten, einschließlich:

 - Schlüssel-Wert-Paare für [Webspeicher](#local-and-session-storage-managers) (*lokaler* und *Sitzungs* Speicher)
 - [Indizierte DB](#indexeddb-manager) -strukturierte Daten
 - [Cookies](#cookies-list) für die Domäne
 - [Cache](#cache-manager) (Anforderung/Antwort-Paare) für das Debuggen von Service Worker

Erweitern Sie eine dieser Kategorien, und klicken Sie auf einen untergeordneten Eintrag, um die Registerkarte Ressourcen-Manager zu öffnen.

## Lokale und Sitzungsspeicher-Manager

Verwenden Sie den *lokalen Speicher-Manager* und den *Sitzungsspeicher-Manager* , um den Webspeicher für Ihre Seite zu überprüfen und zu verwalten. 

In den **lokalen Speicher** -und **Sitzungsspeicher** Ordnern in der [*Ressourcenauswahl*](./debugger.md#resource-picker) des Speicher Panels wird eine Liste der Ursprünge für die Seite angezeigt. Wenn Sie einen dieser Frames auswählen, wird eine bearbeitbare Tabelle mit den aktuellen Schlüssel-Wert-Paaren geöffnet, die über [Window. localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) oder [Window. sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage)(und/oder direkt aus der devtools- [Speicherliste](#storage-list)) gesetzt werden.

![DevTools-lokaler Speicher-Manager](./media/storage_web_storage.png)

Auf den Registerkarten *lokaler Speicher* und *Sitzungsspeicher* können Sie Folgendes ausführen:

 - **Aktualisieren** ( `Ctrl+F5` ) die [Speicherliste](#cookies-list) , um die aktuelle Gruppe von Schlüssel-Wert-Paaren für die angegebene Domäne anzuzeigen. (Die Liste wird bei Skript Aktualisierungen nicht automatisch aktualisiert.)
 - **Simulieren Sie das Erreichen der Speichergrenze** für Microsoft Edge Web Storage. Jede Domäne und Unterdomäne verfügt über einen eigenen Speicherbereich, es gibt jedoch eine kombinierte Grenze:
    - Unter **Domänen:** bis zu 5 MBS Speicherplatz
    - **Domänen:** bis zu 10 MBS Speicherplatz
    - **Gesamtzahl für alle Domänen:** bis zu 50 MBS Speicherplatz

   Der Sitzungsspeicher wird gelöscht, sobald der letzte Browser Reiter, der auf seinen Ursprung verweist, geschlossen ist. Lokale Speichereinträge bleiben unbegrenzt bestehen, bis Sie programmgesteuert von der Seite oder manuell vom Benutzer gelöscht werden:

   **Einstellungen**  >  **Löschen von Browserdaten**  >  **Cookies und gespeicherte Website Daten**

![Löschen von Daten aus dem Microsoft Edge Settings-Panel](./media/settings_clear_browsing_data.png)

### Speicherliste

In der Tabelle " *Speicherliste* " können Sie Folgendes ausführen:

 - Überprüfen Sie Ihre Schlüssel-Wert-Paare **, und Sortieren** Sie Sie, indem Sie in der Tabelle auf einen der Spaltennamen klicken.
 - **Bearbeiten** Sie den *Schlüssel* und *Wert* eines vorhandenen Eintrags, indem Sie in die Zelle klicken.
 - **Löschen** `Del` Sie einen Eintrag aus der Kontextmenüoption, und löschen Sie das *Element*.
 - **Fügen Sie** ein neues Schlüssel-Wert-Paar hinzu, indem Sie auf die leere Zeile am Ende der Tabelle klicken.


### Tastenkombinationen

| Aktion              | Tastenkombination      |
|:--------------------|:--------------|
| Aktualisieren             | `Ctrl` + `F5` |
| Element löschen         | `Del`         |
| Kopieren der markierten Elemente | `Ctrl` + `C`  |
| Alle auswählen          | `Ctrl` + `A`  |


## IndexedDB-Manager

Verwenden Sie die Registerkarte **IndexedDB** , um die strukturierten Daten, die lokal auf einem Clientcomputer gespeichert sind, zu überprüfen und zu verwalten. Insbesondere können Sie Ihre Objektspeicher und Indizes prüfen/sortieren und aktualisieren sowie einzelne Schlüssel-Wert-Einträge löschen.

> [!TIP]
> Sie können unsere [Audiomixer-](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) Demo verwenden, um den *IndexedDB-Manager* in Microsoft Edge devtools zu testen.

Wenn Sie alle IndexedDB-Daten löschen möchten, die für den aktuellen Benutzer in Microsoft Edge gespeichert sind, verwenden Sie das Menü Microsoft Edge *Settings (Einstellungen* ):

**...** >  **Einstellungen**  >  **Löschen von Browserdaten**  >  **Cookies und gespeicherte Website Daten**

Der **IndexedDB** -Ordner in der [*Ressourcenauswahl*](./debugger.md#resource-picker) des Debuggers zeigt eine Liste der Ursprünge der Ressourcen an, die von der Seite geladen werden. Alle IndexedDB-Datenbanken (IDB) werden unter dem Ursprung zusammen mit den Objekt speichern aufgelistet. 

![DevTools-IndexedDB-Manager](./media/storage_indexeddb.png)

### IndexedDB-Symbolleiste

Auf der *IndexedDB* -Symbolleiste können Sie Folgendes ausführen:

 - **Refresh** ( `Ctrl+F5` ), um die aktuellen Einträge im Objektspeicher oder Index der Datenbank anzuzeigen. Der IndexedDB-Manager wird nicht automatisch aktualisiert, wenn Änderungen an der Datenbank vorgenommen wurden.

### Liste der Objektspeicher Einträge

In der *Objektspeicher* -oder *Index* Tabelle können Sie Folgendes ausführen:

 - Überprüfen Sie Ihre Schlüssel-Wert-Paare **, und Sortieren** Sie Sie, indem Sie in der Tabelle auf einen beliebigen Spaltennamen klicken.
 - **Refresh** ( `Ctrl+F5` )
 - **Element löschen** ( `Del` ), um den ausgewählten Eintrag im Objektspeicher oder-Index zu entfernen. Sie können dies auch über die [Kontextmenü](#context-menu) Option " *Element löschen*" ausführen.
 - **Ausgewählte Elemente kopieren** ( `Ctrl+C` ), um das ausgewählte Element in die Zwischenablage zu kopieren. Sie können dies auch über die [Kontextmenü](#context-menu) Option mit der rechten Maustaste ausführen, um das *ausgewählte Element zu kopieren*.
 - **Wählen Sie alle** ( `Ctrl+A` ) aus, um alle Einträge in Ihrem Objektspeicher oder-Index auszuwählen. Sie können dies auch über die [Kontextmenü](#context-menu) Option mit der rechten Maustaste und dann auf *Alle auswählen*.

Die Spalten der *Objektspeicher* -oder *Index* Tabelle sind sortierbar:

Spalte | Beschreibung
:------------ | :-------------
Schlüssel | Name des Schlüssel-Wert-Paars (identisch mit dem *Primärschlüssel*) beim Durchlaufen eines Objektspeichers; Name des Indexschlüssels (aktuelle Taste des Cursors) beim Durchlaufen eines Indexes
Primärschlüssel | Name des Schlüssel-Wert-Paars (Weitere Informationen zu den IDB- [Schlüsseln](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)finden Sie unter *MDN Web docs* )
Wert | Wert des Schlüssel-Wert-Paars

Weitere Informationen zu [IndexedDB-Konzepten und-Verwendung](https://developer.mozilla.org/docs/Web/API/IndexedDB_API)finden Sie unter *MDN Web docs* .

### Kontextmenü

Neben der [ *IndexedDB* -Symbolleiste](#indexeddb-toolbar)können Sie auch Ihre Daten in Objekt speichern oder Indizes über das **Kontextmenü** mit der rechten Maustaste und/oder die Tasten [Kombinationen](#shortcuts)verwalten.

### Tastenkombinationen

Aktion | Tastenkombination
:------------ | :-------------
Aktualisieren | `Ctrl` + `F5`
Schlüssel-Wert-Paar löschen | `Del`
Kopieren der markierten Elemente | `Ctrl` + `C`
Alle auswählen | `Ctrl` + `A`

## Cookies-Manager

Verwenden Sie den *Cookies-Manager* , um die Cookies für die angegebene Domäne zu überprüfen und zu verwalten. 

Der Ordner " **Cookies** " in der [*Ressourcenauswahl*](./debugger.md#resource-picker) des Debuggers zeigt eine Liste der Ursprünge der Ressourcen an, die von der Seite geladen werden. Wenn Sie einen dieser Frames auswählen, wird eine Tabelle geöffnet, die die aktuellen Cookies darstellt, die entweder über den [http](https://developer.mozilla.org/docs/Web/HTTP/Cookies) -Header oder über ein Skript mit [Document. Cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie)gesetzt sind.

![DevTools-Cookies-Manager](./media/storage_cookies.png)

Über die Registerkarte " *Cookies* " können Sie Folgendes tun:

 - **Aktualisieren** `Ctrl+F5` Sie die [Liste der Cookies](#cookies-list) , um die aktuelle Gruppe von Cookies für die angegebene Domäne anzuzeigen. (Die Liste wird nicht automatisch aktualisiert.)
 - **Löschen Sie alle Cookies** ( `Ctrl+Shift+Del` ) (Session und permanent) für den Pfad der aktuellen Seite.
 - **Löschen Sie alle Sitzungscookies** ( `Ctrl+Del` ) für den Pfad der aktuellen Seite.

Um die Liste der *Cookies*vollständig zu löschen, müssen Sie möglicherweise **alle Cookies für die Domäne** über die Symbolleiste des [**Netzwerk**](./network.md#toolbar) Panels löschen.

### Liste der Cookies

In der Tabelle " *Cookies-Liste* " können Sie Folgendes ausführen:

 - Über **prüfen und Sortieren** Sie Ihre Cookies, indem Sie in der Tabelle auf einen beliebigen Spaltennamen klicken.
 - **Bearbeiten** Sie den *Namen* und den *Wert* eines vorhandenen Cookies, indem Sie in die Zelle klicken.
 - **Löschen** ( `Del` ) eines Cookies aus der [Kontextmenü](#context-menu) Option " *Cookie löschen*"
 - **Fügen Sie** ein neues Sitzungscookie für die angegebene *Domäne/* den angegebenen Pfad hinzu, indem Sie auf die leere Zeile am Ende der Tabelle klicken. Dies funktioniert nur bei Sitzungscookies; permanente Cookies (mit bestimmten Ablaufdaten) müssen mit traditionellen Methoden festgesetzt werden. Die Werte für *Domäne* und *Pfad* werden automatisch entsprechend dem Speicherort der Seite ausgefüllt.

Die Spalten der *Liste "Cookies* " sind sortierbar:

Spalte | Beschreibung
:------------ | :-------------
Name | Name des Cookies
Wert | Wert des Cookies
Domäne | Hostname des Cookies (möglicherweise leer)
Pfad | URL-Pfad für das Cookie (möglicherweise leer)
Läuft ab | Maximale Lebensdauer des Cookies als http-Datumsstempel. `Expires` `Max-Age` Ist "Nein" oder "wurde" gesetzt, gilt der Eintrag als *Sitzungs* Cookie.
Nur http | Gibt an, ob das Cookie mit Directive festgesetzt wurde `HttpOnly` , was darauf hinweist, dass von JavaScript aus kein Zugriff möglich ist.
Sicherheit | Gibt an, ob das Cookie mit der `Secure` Direktive gesetzt wurde, was angibt, dass es nur von einer Anforderung mit SSL und dem HTTPS-Protokoll an den Server gesendet wird.

Weitere Informationen zu Cookie-Eigenschaften finden Sie im **MDN Web docs** [-Satz-Cookie-](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) Referenz.

### Kontextmenü

Neben der [Symbolleiste](#cookies-manager)" *Cookies* " können Sie Ihre Cookies auch über das **Kontextmenü** der rechten Maustaste und/oder die Tasten [Kombinationen](#shortcuts)verwalten.

### Tastenkombinationen

| Aktion                     | Tastenkombination                 |
|:---------------------------|:-------------------------|
| Aktualisieren                    | `Ctrl` + `F5`            |
| Löschen eines Cookies              | `Del`                    |
| Alle Cookies löschen         | `Ctrl` + `Shift` + `Del` |
| Löschen aller Sitzungscookies | `Ctrl` + `Del`           |
| Kopieren der markierten Elemente        | `Ctrl` + `C`             |
| Alle auswählen                 | `Ctrl` + `A`             |

### Cache-Manager

Wenn Sie auf einen bestimmten Cacheeintrag klicken, wird der Service Worker- **Cache** -Manager geöffnet, in dem Sie Cacheeinträge (*Anforderungs* -und *Antwort* Schlüssel-Wert-Paare) überprüfen und optional löschen können:

![Cache-Manager](./media/storage_cache.png)

### Tastenkombinationen

#### Cache-Manager

| Aktion              | Tastenkombination      |
|:--------------------|:--------------|
| Aktualisieren             | `Ctrl` + `F5` |
| Element löschen         | `Del`         |
| Kopieren der markierten Elemente | `Ctrl` + `C`  |
| Alle auswählen          | `Ctrl` + `A`  |
