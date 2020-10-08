---
description: Informationen zum Anzeigen und Ändern von IndexedDB-Daten mit dem Anwendungs Panel und Snippets.
title: Anzeigen und Ändern von IndexedDB-Daten mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 6b1209ddcbfac305535d9d61e001441dbf61b6ec
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993562"
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
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-manifest-empty.msft.png":::
       Bereich ' **Manifest** '  
    :::image-end:::  
    
1.  Erweitern Sie das **IndexedDB** -Menü, um zu sehen, welche Datenbanken verfügbar sind.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       Das **IndexedDB** -Menü  
    :::image-end:::  
    
    *   \ ( ![ Datenbanksymbol ][ImageDatabaseIcon] \) `notes - https://mdn.github.io` stellt eine Datenbank dar, wobei `notes` der Name der Datenbank und `https://mdn.github.io` der Ursprung ist, der auf die Datenbank zugreift.  
    *   \ ( ![ Objektspeicher Symbol ][ImageObjectStoreIcon] \) `notes` ist ein Objektspeicher.  
    *   **Titel** und **Text** sind [Indizes][MDNUsingIndexedDBUsingIndex].  
    
    > [!NOTE]
    > **Bekannte Einschränkung**  Datenbanken von Drittanbietern werden nicht angezeigt.  Wenn Sie beispielsweise eine Anzeige in `<iframe>` Ihre Seite einbetten und Ihr Anzeigennetzwerk IndexedDB verwendet, sind die IndexedDB-Daten für Ihr Anzeigennetzwerk nicht sichtbar.  Weitere Informationen finden Sie unter [Problem #943770][ChromiumIssue943770].  
    
1.  Wählen Sie eine Datenbank aus, um den Ursprung und die Versionsnummer anzuzeigen.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       Die **Notes** -Datenbank  
    :::image-end:::  
    
1.  Wählen Sie einen Objektspeicher aus, um die Schlüssel-Wert-Paare anzuzeigen.  
    
    > [!NOTE]
    > IndexedDB-Daten werden in Echtzeit nicht aktualisiert.  Siehe [Aktualisieren von IndexedDB-Daten](#refresh-indexeddb-data).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       Der **Notizen** Objektspeicher  
    :::image-end:::  
    
    *   **Gesamt** Anzahl der Einträge ist die Gesamtzahl der Schlüssel-Wert-Paare im Objektspeicher.  
    *   Der **Schlüsselgenerator Wert** ist der nächste verfügbare Schlüssel.  Dieses Feld wird nur angezeigt, wenn [Schlüsselgeneratoren][MDNBasicConceptsKeyGenerator]verwendet werden.  
    
1.  Wählen Sie in der Spalte **Wert** eine Zelle aus, um diesen Wert zu erweitern.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       Anzeigen eines **IndexedDB** -Werts  
    :::image-end:::  
    
1.  Wählen Sie in der folgenden Abbildung einen Index wie **Titel** oder **Text** aus, um den Objektspeicher entsprechend den Werten dieses Indexes zu sortieren.  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       Sortieren eines Objektspeichers anhand eines Indexes  
    :::image-end:::  
    
## Aktualisieren von IndexedDB-Daten   

IndexedDB-Werte im **Anwendungs** Panel werden nicht in Echtzeit aktualisiert.  Wählen Sie **Aktualisieren** \ ( ![ Aktualisieren \) aus, wenn Sie ][ImageReloadIcon] einen Objektspeicher anzeigen, um die Daten zu aktualisieren, oder zeigen Sie eine Datenbank an, und klicken Sie auf **Datenbank aktualisieren** , um alle Daten zu aktualisieren.  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   Anzeigen einer Datenbank  
:::image-end:::  

## Bearbeiten von IndexedDB-Daten   

IndexedDB-Schlüssel und-Werte können im **Anwendungs** Panel nicht bearbeitet werden.  Da devtools jedoch Zugriff auf den Seitenkontext hat, können Sie JavaScript-Code in devtools ausführen, um IndexedDB-Daten zu bearbeiten.  

### Bearbeiten von IndexedDB-Daten mit Ausschnitten   

[Snippets][DevtoolsJavascriptSnippets] sind eine Möglichkeit zum Speichern und Ausführen von JavaScript-Codeblöcken in devtools.  Wenn Sie einen Ausschnitt ausführen, wird das Ergebnis in der **Konsole**protokolliert.  Sie können einen Ausschnitt zum Ausführen von JavaScript-Code zum Bearbeiten einer IndexedDB-Datenbank verwenden.  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   Verwenden eines Snippets für die Interaktion mit IndexedDB  
:::image-end:::  

## Löschen von IndexedDB-Daten   

### Löschen eines IndexedDB-Schlüssel-Wert-Paars   

1.  [Anzeigen eines IndexedDB-Objektspeichers](#view-indexeddb-data)  
1.  Wählen Sie das Schlüssel-Wert-Paar aus, das Sie löschen möchten.  DevTools hebt die Markierung hervor, um anzugeben, dass Sie markiert ist.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       Wählen Sie ein Schlüssel-Wert-Paar aus, um es zu löschen.  
    :::image-end:::  
    
1.  Drücken Sie die Eingabe `Delete` Taste, oder klicken Sie auf **Ausgewählte löschen** \ ( ![ Auswahl löschen ][ImageDeleteIcon] \).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       Wie der Objektspeicher aussieht, nachdem das Schlüssel-Wert-Paar gelöscht wurde  
    :::image-end:::  
    
### Löschen aller Schlüssel-Wert-Paare in einem Objektspeicher   

1.  [Anzeigen eines IndexedDB-Objektspeichers](#view-indexeddb-data)  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       Anzeigen eines Objektspeichers  
    :::image-end:::  
    
1.  Wählen Sie **Objektspeicher löschen** \ ( ![ Objektspeicher löschen ][ImageClearIcon] \) aus.  
    
### Löschen einer IndexedDB-Datenbank   

1.  [Zeigen Sie die IndexedDB-Datenbank](#view-indexeddb-data) an, die Sie löschen möchten.  
1.  Wählen Sie **Datenbank löschen**aus.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       Schaltfläche " **Datenbank löschen** "  
    :::image-end:::  
    
### Löschen des gesamten IndexedDB-Speichers   

1.  Öffnen Sie den Bereich **Speicher löschen** .  
1.  Stellen Sie sicher, dass das Kontrollkästchen **IndexedDB** aktiviert ist.  
1.  Wählen Sie **Website Daten löschen**aus.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       Der Bereich " **Speicher löschen** "  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDatabaseIcon]: ../media/database-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageObjectStoreIcon]: ../media/object-store-icon.msft.png  
[ImageReloadIcon]: ../media/reload-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwicklertools | Microsoft docs"  
[DevtoolsJavascriptSnippets]: ../javascript/snippets.md "Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools | Microsoft docs"  

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
