---
title: Anzeigen und Ändern von IndexedDB-Daten mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 4eca78dcd92048d75f8488fddc7b210da68690df
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612088"
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





# Anzeigen und Ändern von IndexedDB-Daten mit Microsoft Edge devtools   

  

Dieser Leitfaden zeigt, wie Sie [Microsoft Edge devtools][MicrosoftEdgeDevTools] verwenden, um [IndexedDB][MDNIndexedDBAPI] -Daten anzuzeigen und zu ändern.  Es wird davon ausgegangen, dass Sie mit devtools vertraut sind.  Außerdem wird davon ausgegangen, dass Sie mit IndexedDB vertraut sind.  Wenn dies nicht der Fall ist, lesen Sie [Verwenden von IndexedDB][MDNUsingIndexedDB].  

## Anzeigen von IndexedDB-Daten   

1.  Wählen Sie die Registerkarte **Anwendung** aus, um den **Anwendungs** Panel zu öffnen.  Der Bereich **Manifest** wird normalerweise standardmäßig geöffnet.  
    
    > ##### Abbildung1  
    > Bereich ' Manifest '  
    > ![Bereich ' Manifest '][ImageManifest]  

1.  Erweitern Sie das **IndexedDB** -Menü, um zu sehen, welche Datenbanken verfügbar sind.  
    
    > ##### Abbildung2  
    > Das **IndexedDB** -Menü  
    > ![Das IndexedDB-Menü][ImageIndexedDBMenu]  
    
    *   ![Das Datenbanksymbol ][ImageDatabaseIcon] `notes - https://mdn.github.io` stellt eine Datenbank dar, wobei `notes` der Name der Datenbank und `https://mdn.github.io` der Ursprung für den Zugriff auf die Datenbank ist.  
    *   ![Das Objektspeicher Symbol ][ImageObjectStoreIcon] `notes` ist ein Objektspeicher.  
    *   **Titel** und **Text** sind [Indizes][MDNUsingIndexedDBUsingIndex].  
    
    > [!NOTE]
    > **Bekannte Einschränkung**  Datenbanken von Drittanbietern werden nicht angezeigt.  Wenn Sie beispielsweise eine Anzeige in `<iframe>` Ihre Seite einbetten und Ihr Anzeigennetzwerk IndexedDB verwendet, sind die IndexedDB-Daten für Ihr Anzeigennetzwerk nicht sichtbar.  Weitere Informationen finden Sie unter [Problem #943770][ChromiumIssue943770].  
    
1.  Wählen Sie eine Datenbank aus, um den Ursprung und die Versionsnummer anzuzeigen.  
    
    > ##### Abbildung 3  
    > Die **Notes** -Datenbank  
    > ![Die Notes-Datenbank][ImageIndexedDBDatabase]  
    
1.  Wählen Sie einen Objektspeicher aus, um die Schlüssel-Wert-Paare anzuzeigen.  
    
    > [!NOTE]
    > IndexedDB-Daten werden in Echtzeit nicht aktualisiert.  Siehe [Aktualisieren von IndexedDB-Daten](#refresh-indexeddb-data).  
    
    > ##### Abbildung4  
    > Der **Notizen** Objektspeicher  
    > ![Der Notizen Objektspeicher][ImageIndexedDBObjectStore]  

    *   **Gesamt** Anzahl der Einträge ist die Gesamtzahl der Schlüssel-Wert-Paare im Objektspeicher.  
    *   Der **Schlüsselgenerator Wert** ist der nächste verfügbare Schlüssel.  Dieses Feld wird nur angezeigt, wenn [Schlüsselgeneratoren][MDNBasicConceptsKeyGenerator]verwendet werden.  

1.  Wählen Sie in der Spalte **Wert** eine Zelle aus, um diesen Wert zu erweitern.  
    
    > ##### Abbildung5  
    > Anzeigen eines IndexedDB-Werts  
    > ![Anzeigen eines IndexedDB-Werts][ImageIndexedBDValue]  
    
1.  Wählen Sie einen Index wie **Titel** oder **Textkörper** in [Abbildung 6](#figure-6)aus, um den Objektspeicher entsprechend den Werten dieses Indexes zu sortieren.  
   
    > ##### Abbildung6  
    > Ein Objektspeicher, der alphabetisch nach dem **Titel** Schlüssel sortiert ist  
    > ![Sortieren eines Objektspeichers anhand eines Indexes][ImageIndexedDBIndex]  

## Aktualisieren von IndexedDB-Daten   

IndexedDB-Werte im **Anwendungs** Panel werden nicht in Echtzeit aktualisiert.  Wählen **Sie Aktualisierung aktualisieren** aus, ![ Wenn Sie ][ImageReloadIcon] einen Objektspeicher anzeigen, um die Daten zu aktualisieren, oder zeigen Sie eine Datenbank an, und klicken Sie auf **Datenbank aktualisieren** , um alle Daten zu aktualisieren.  

> ##### Abbildung7  
> Anzeigen einer Datenbank  
> ![Anzeigen einer Datenbank][ImageIndexedDBDatabase2]  

## Bearbeiten von IndexedDB-Daten   

IndexedDB-Schlüssel und-Werte können im **Anwendungs** Panel nicht bearbeitet werden.  Da devtools jedoch Zugriff auf den Seitenkontext hat, können Sie JavaScript-Code in devtools ausführen, um IndexedDB-Daten zu bearbeiten.  

### Bearbeiten von IndexedDB-Daten mit Ausschnitten   

[Snippets][DevtoolsJavascriptSnippets] sind eine Möglichkeit zum Speichern und Ausführen von JavaScript-Codeblöcken in devtools.  Wenn Sie einen Ausschnitt ausführen, wird das Ergebnis in der **Konsole**protokolliert.  Sie können einen Ausschnitt zum Ausführen von JavaScript-Code zum Bearbeiten einer IndexedDB-Datenbank verwenden.  

> ##### Abbildung8  
> Verwenden eines Snippets für die Interaktion mit IndexedDB  
> ![Verwenden eines Snippets für die Interaktion mit IndexedDB][ImageIndexedDBSnippet]  

## Löschen von IndexedDB-Daten   

### Löschen eines IndexedDB-Schlüssel-Wert-Paars   

1.  [Anzeigen eines IndexedDB-Objektspeichers](#view-indexeddb-data)  
1.  Wählen Sie das Schlüssel-Wert-Paar aus, das Sie löschen möchten.  DevTools hebt die Markierung hervor, um anzugeben, dass Sie markiert ist.  
    
    > ##### Abbildung 9  
    > Auswählen eines Schlüssel-Wert-Paars, um es zu löschen  
    > ![Auswählen eines Schlüssel-Wert-Paars, um es zu löschen][ImageIndexedDBKeyValuePair]  

1.  Drücken Sie die Eingabe `Delete` Taste, oder klicken Sie auf **Ausgewählte löschen Löschen** ![ ][ImageDeleteIcon] .  
    
    > ##### Abbildung 10  
    > Wie der Objektspeicher aussieht, nachdem das Schlüssel-Wert-Paar gelöscht wurde  
    > ![Wie der Objektspeicher aussieht, nachdem das Schlüssel-Wert-Paar gelöscht wurde][ImageIndexedDBKeyValuePairDeleted]  

### Löschen aller Schlüssel-Wert-Paare in einem Objektspeicher   

1.  [Anzeigen eines IndexedDB-Objektspeichers](#view-indexeddb-data)  
    
    > ##### Abbildung 11  
    > Anzeigen eines Objektspeichers  
    > ![Anzeigen eines Objektspeichers][ImageIndexedDBObjectStore]  

1.  Wählen Sie **Objektspeicher löschen** ![ , Objektspeicher löschen aus ][ImageClearIcon] .  

### Löschen einer IndexedDB-Datenbank   

1.  [Zeigen Sie die IndexedDB-Datenbank](#view-indexeddb-data) an, die Sie löschen möchten.  
1.  Wählen Sie **Datenbank löschen**aus.  
    
    > ##### Abbildung 12  
    > Schaltfläche " **Datenbank löschen** "  
    > ![Schaltfläche "Datenbank löschen"][ImageIndexedDBDatabase]  

### Löschen des gesamten IndexedDB-Speichers   

1.  Öffnen Sie den Bereich **Speicher löschen** .  

1.  Stellen Sie sicher, dass das Kontrollkästchen **IndexedDB** aktiviert ist.  

1.  Wählen Sie **Website Daten löschen**aus.  
    
    > ##### Abbildung 13  
    > Der Bereich " **Speicher löschen** " ![ im Bereich "Speicher löschen"][ImageIndexedDBClearStorage]  

 



<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDatabaseIcon]: /microsoft-edge/devtools-guide-chromium/media/database-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  
[ImageObjectStoreIcon]: /microsoft-edge/devtools-guide-chromium/media/object-store-icon.msft.png  
[ImageReloadIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest-empty.msft.png "Abbildung 1: der Bereich "Manifest""  
[ImageIndexedDBMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb.msft.png "Abbildung 2: das IndexedDB-Menü"  
[ImageIndexedDBDatabase]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db.msft.png "Abbildung 3: die notes_db-Datenbank"  
[ImageIndexedDBObjectStore]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png "Abbildung 4: der notes_os Objektspeicher"  
[ImageIndexedBDValue]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png "Abbildung 5: Anzeigen eines IndexedDB-Werts"  
[ImageIndexedDBIndex]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png "Abbildung 6: Sortieren eines Objektspeichers anhand eines Indexes"  
[ImageIndexedDBDatabase2]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png "Abbildung 7: Anzeigen einer Datenbank"  
[ImageIndexedDBSnippet]: /microsoft-edge/devtools-guide-chromium/media/storage-sources-snippets-indexeddb-output.msft.png "Abbildung 8: Verwenden eines Ausschnitts für die Interaktion mit IndexedDB"  
[ImageIndexedDBKeyValuePair]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png "Abbildung 9: Auswählen eines Schlüssel-Wert-Paars, um es zu löschen"  
[ImageIndexedDBKeyValuePairDeleted]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png "Abbildung 10: Aussehen des Objektspeichers, nachdem das Schlüssel-Wert-Paar gelöscht wurde"  
[ImageIndexedDBObjectStore]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png "Abbildung 11: Anzeigen eines Objektspeichers"  
[ImageIndexedDBDatabase]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png "Abbildung 12: die Schaltfläche "Datenbank löschen""  
[ImageIndexedDBClearStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png "Abbildung 13: der Bereich "Speicher löschen""  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  
[DevtoolsJavascriptSnippets]: /microsoft-edge/devtools-guide-chromium/javascript/snippets "Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770-devtools: Anzeigen von IFRAME-IndexedDB-Datenbanken – Chrom-Monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Schlüssel Generator – grundlegende Konzepte | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "IndexedDB-API | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Verwenden von IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Verwenden eines Index-using IndexedDB | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
