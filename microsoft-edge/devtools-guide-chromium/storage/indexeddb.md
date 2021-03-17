---
description: Anzeigen und Ändern von IndexedDB-Daten mit dem Anwendungsbereich und Codeausschnitten.
title: Anzeigen und Ändern von IndexedDB-Daten mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 719348067b1343ca3d7781737fa6441f92ad7ba1
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439710"
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

# <a name="view-and-change-indexeddb-data-with-microsoft-edge-devtools"></a>Anzeigen und Ändern von IndexedDB-Daten mit Microsoft Edge DevTools  

In diesem Handbuch erfahren Sie, wie [Sie Microsoft Edge DevTools zum Anzeigen][MicrosoftEdgeDevTools] und Ändern von [IndexedDB-Daten][MDNIndexedDBAPI] verwenden.  Es wird davon ausgegangen, dass Sie mit DevTools vertraut sind.  Außerdem wird davon ausgegangen, dass Sie mit IndexedDB vertraut sind.  Wenn nicht, navigieren Sie zu [Verwenden von IndexedDB][MDNUsingIndexedDB].  

## <a name="view-indexeddb-data"></a>Anzeigen von IndexedDB-Daten  

1.  Wählen Sie die **Registerkarte Anwendung** aus, um das **Anwendungstool zu** öffnen.  Der **Manifestbereich** wird in der Regel standardmäßig geöffnet.  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Der Manifestbereich" lightbox="../media/storage-application-manifest-empty.msft.png":::
       Der **Manifestbereich**  
    :::image-end:::  
    
1.  Erweitern Sie **das Menü IndexedDB,** um zu überprüfen, welche Datenbanken verfügbar sind.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="Das Menü IndexedDB" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       Das **Menü IndexedDB**  
    :::image-end:::  
    
    *   \( ![ Database icon ](../media/database-icon.msft.png) \) represents a `notes - https://mdn.github.io` database, where is the name of the `notes` database and is the origin that `https://mdn.github.io` accesses the database.  
    *   \( ![ Objektspeichersymbol ](../media/object-store-icon.msft.png) \) `notes` ist ein Objektspeicher.  
    *   **title** und **body** sind [Indizes][MDNUsingIndexedDBUsingIndex].  
    
    > [!NOTE]
    > **Bekannte Einschränkung**  Drittanbieterdatenbanken sind nicht sichtbar.  Wenn Sie beispielsweise eine zum Einbetten einer Anzeige auf Ihrer Seite verwenden und Ihr Anzeigennetzwerk IndexedDB verwendet, sind die IndexedDB-Daten für Ihr Anzeigennetzwerk `<iframe>` nicht sichtbar.  Navigieren Sie zum [Problem #943770][ChromiumIssue943770].  
    
1.  Wählen Sie eine Datenbank aus, um den Ursprung und die Versionsnummer zu überprüfen.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="Die Notizendatenbank" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       Die **Notizendatenbank**  
    :::image-end:::  
    
1.  Wählen Sie einen Objektspeicher aus, um die Schlüssel-Wert-Paare zu überprüfen.  
    
    > [!NOTE]
    > IndexedDB-Daten werden nicht in Echtzeit aktualisiert.  Navigieren Sie zu [IndexedDB-Daten aktualisieren.](#refresh-indexeddb-data)  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="Der Notes-Objektspeicher" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       Der **Notes-Objektspeicher**  
    :::image-end:::  
    
    *   **Total entries** is the total number of key-value pairs in the object store.  
    *   **Der Schlüsselgeneratorwert** ist der nächste verfügbare Schlüssel.  Das Feld wird nur angezeigt, wenn [Schlüsselgeneratoren verwendet werden.][MDNBasicConceptsKeyGenerator]  
    
1.  Wählen Sie eine Zelle in der **Spalte Wert** aus, um den Wert zu erweitern.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="Anzeigen eines IndexedDB-Werts" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       Anzeigen eines **IndexedDB-Werts**  
    :::image-end:::  
    
1.  Wählen Sie in **** der **** folgenden Abbildung einen Index aus, z. B. Titel oder Textkörper, um den Objektspeicher nach den Werten dieses Indexes zu sortieren.  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="Sortieren eines Objektspeichers nach einem Index" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       Sortieren eines Objektspeichers nach einem Index  
    :::image-end:::  
    
## <a name="refresh-indexeddb-data"></a>Aktualisieren von IndexedDB-Daten  

IndexedDB-Werte im **Anwendungstool** werden nicht in Echtzeit aktualisiert.  Wählen **Sie Aktualisieren** \( Aktualisieren ![ \) aus, wenn Sie einen Objektspeicher anzeigen, um die Daten zu aktualisieren, oder zeigen Sie eine Datenbank an, und wählen Sie Datenbank aktualisieren aus, um ](../media/reload-icon.msft.png) alle Daten zu aktualisieren. ****  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="Anzeigen einer Datenbank" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   Anzeigen einer Datenbank  
:::image-end:::  

## <a name="edit-indexeddb-data"></a>Bearbeiten von IndexedDB-Daten  

IndexedDB-Schlüssel und -Werte können nicht über das **Anwendungstool bearbeitet** werden.  Da DevTools jedoch Zugriff auf den Seitenkontext hat, können Sie JavaScript-Code in DevTools ausführen, um IndexedDB-Daten zu bearbeiten.  

### <a name="edit-indexeddb-data-with-snippets"></a>Bearbeiten von IndexedDB-Daten mit Codeausschnitten  

[Codeausschnitte][DevtoolsJavascriptSnippets] sind eine Möglichkeit zum Speichern und Ausführen von Blöcken von JavaScript-Code in DevTools.  Wenn Sie einen Codeausschnitt ausführen, wird das Ergebnis bei der **Konsole protokolliert.**  Sie können einen Codeausschnitt zum Ausführen von JavaScript-Code verwenden, um eine IndexedDB-Datenbank zu bearbeiten.  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="Verwenden eines Codeausschnitts für die Interaktion mit IndexedDB" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   Verwenden eines Codeausschnitts für die Interaktion mit IndexedDB  
:::image-end:::  

## <a name="delete-indexeddb-data"></a>Löschen von IndexedDB-Daten  

### <a name="delete-an-indexeddb-key-value-pair"></a>Löschen eines IndexedDB-Schlüssel-Wert-Paars  

1.  [Anzeigen eines IndexedDB-Objektspeichers](#view-indexeddb-data).  
1.  Wählen Sie das Schlüssel-Wert-Paar aus, das Sie löschen möchten.  DevTools hebt es hervor, um anzugeben, dass es ausgewählt ist.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="Wählen Sie ein Schlüssel-Wert-Paar aus, um es zu löschen" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       Wählen Sie ein Schlüssel-Wert-Paar aus, um es zu löschen  
    :::image-end:::  
    
1.  Wählen Sie `Delete` den Schlüssel aus, oder wählen **Sie Ausgewählte \(** ![ Ausgewählte Option löschen ](../media/delete-icon.msft.png) \) aus.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="Aussehen des Objektspeichers nach dem Löschen des Schlüssel-Wert-Paars" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       Aussehen des Objektspeichers nach dem Löschen des Schlüssel-Wert-Paars  
    :::image-end:::  
    
### <a name="delete-all-key-value-pairs-in-an-object-store"></a>Löschen aller Schlüssel-Wert-Paare in einem Objektspeicher  

1.  [Anzeigen eines IndexedDB-Objektspeichers](#view-indexeddb-data).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="Anzeigen eines Objektspeichers" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       Anzeigen eines Objektspeichers  
    :::image-end:::  
    
1.  Wählen **Sie Clear object store** \( Clear object store ![ ](../media/clear-icon.msft.png) \).  
    
### <a name="delete-an-indexeddb-database"></a>Löschen einer IndexedDB-Datenbank  

1.  [Zeigen Sie die IndexedDB-Datenbank an,](#view-indexeddb-data) die Sie löschen möchten.  
1.  Wählen **Sie Datenbank löschen**aus.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="Die Schaltfläche Datenbank löschen" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       Die **Schaltfläche Datenbank löschen**  
    :::image-end:::  
    
### <a name="delete-all-indexeddb-storage"></a>Löschen des ganzen IndexedDB-Speichers  

1.  Öffnen Sie den **Speicherbereich** löschen.  
1.  Stellen Sie sicher, dass das **Kontrollkästchen IndexedDB** aktiviert ist.  
1.  Wählen **Sie Websitedaten löschen aus.**  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="Der Speicherbereich löschen" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       Der **Speicherbereich löschen**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Entwicklertools | Microsoft Docs"  
[DevtoolsJavascriptSnippets]: ../javascript/snippets.md "Ausführen von Codeausschnitten von JavaScript auf jeder Seite mit Microsoft Edge DevTools | Microsoft Docs"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770 - DevTools: iframe IndexedDB-Datenbanken anzeigen - Chromium - Monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Key Generator – Grundlegende Konzepte | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "IndexedDB-API-| MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Verwenden von IndexedDB-| MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Verwenden eines Indexes – Verwenden von IndexedDB-| MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
