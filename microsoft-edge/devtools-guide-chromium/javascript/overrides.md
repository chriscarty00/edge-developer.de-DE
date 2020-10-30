---
description: Das Feature "Außerkraftsetzungen" ist ein Feature im Quellen Tool von Microsoft Edge devtools, mit dem Sie Webseiten Ressourcen auf Ihre Festplatte kopieren können.  Wenn Sie die Webseite aktualisieren, wird die Ressource von devtools nicht geladen, sondern stattdessen durch Ihre lokale Kopie ersetzt.
title: Überschreiben von Webseiten Ressourcen mit lokalen Kopien mithilfe von Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 579ebe92dc50571837e7e3caf8fb7c1a9989bc59
ms.sourcegitcommit: 9dcaf598f3930bcfab9f93ff63463beb98274de0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/30/2020
ms.locfileid: "11145169"
---
# Überschreiben von Webseiten Ressourcen mit lokalen Kopien mithilfe von Microsoft Edge devtools  

Manchmal müssen Sie ein Problem auf einer Webseite beheben, auf die Sie keinen Zugriff haben, oder Fehlerbehebungen beinhalten einen langsamen und komplexen Buildprozess.  Sie können alle Arten von Problemen in devtools Debuggen und beheben. Das Problem besteht aber darin, dass die Änderungen nicht fortbestehen.  Nachdem Sie die Datei aktualisiert haben, ist Ihre Arbeit nicht mehr vorhanden.  

Das Feature "Außerkraftsetzungen" im [Quellen][DevToolsSourcesTool] Tool hilft Ihnen bei der Lösung dieses Problems.  

Sie können nun eine Ressource der aktuellen Webseite aufnehmen und lokal speichern.  Wenn Sie die Webseite aktualisieren, lädt der Browser die Ressource nicht vom Server.  Stattdessen ersetzt der Browser ihn durch Ihre lokale Kopie der Ressource.  

## Einrichten Ihres lokalen Ordners zum Speichern von Außerkraftsetzungen  

1.  Suchen Sie im **Quellen** Tool auf der linken Seite mehrere Abschnitte.  Wenn die Option " **Außerkraftsetzungen** " nicht angezeigt wird, wählen Sie die <code>&#x0226B;</code><!--`≫`--> Symbol, um dorthin zu gelangen.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-overflow-menu.msft.png" alt-text="Quellen Tool mit nicht genügend Speicherplatz, um die Option &quot;Außerkraftsetzungen&quot; anzuzeigen" lightbox="../media/javascript-overrides-overflow-menu.msft.png":::
             **Quellen** Tool mit nicht genügend Speicherplatz, um die Option "Außerkraftsetzungen" anzuzeigen  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-menu.msft.png" alt-text="Quellen Tool mit nicht genügend Speicherplatz, um die Option &quot;Außerkraftsetzungen&quot; anzuzeigen" lightbox="../media/javascript-overrides-menu.msft.png":::
             Auswählen der Option "Außerkraftsetzungen"  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Nachdem Sie die Option **Overrides** ausgewählt haben, müssen Sie einen Ordner auf dem lokalen Computer auswählen, um die Ressourcendateien zu speichern, die Sie ersetzen möchten.  Wählen Sie den **Ordner + SELECT für Außerkraftsetzungen** aus, um nach einem Ordner zu suchen.  
    
    :::image type="complex" source="../media/javascript-overrides-select-folder.msft.png" alt-text="Quellen Tool mit nicht genügend Speicherplatz, um die Option &quot;Außerkraftsetzungen&quot; anzuzeigen" lightbox="../media/javascript-overrides-select-folder.msft.png":::
       Auswählen eines Ordners, der für Außerkraftsetzungen verwendet werden soll  
    :::image-end:::  
    
1.  DevTools warnt Sie, dass der Vollzugriff auf den Ordner vorhanden sein muss und dass Sie keine vertraulichen Informationen offen legen sollten.  Wählen Sie auf der warnungsleiste **zulassen** aus, um Zugriff zu gewähren.  
    
    :::image type="complex" source="../media/javascript-overrides-give-access-to-folder.msft.png" alt-text="Quellen Tool mit nicht genügend Speicherplatz, um die Option &quot;Außerkraftsetzungen&quot; anzuzeigen" lightbox="../media/javascript-overrides-give-access-to-folder.msft.png":::
       Gewähren von devtools Zugriff auf Ordner  
    :::image-end:::  
    
1.  Im Bereich " **Außerkraftsetzungen** " sollte ein Kontrollkästchen neben `Enable Local Overrides` dem Ordner "Überschreibungen" angezeigt werden.  Daneben wird ein Symbol angezeigt, in dem Sie Ihre lokalen Außerkraftsetzungseinstellungen löschen können.  Sie haben nun die Einrichtung Ihres Ordners abgeschlossen und sind bereit, Live-Ressourcen durch lokale zu ersetzen.
    
    :::image type="complex" source="../media/javascript-overrides-folder-setup-complete.msft.png" alt-text="Quellen Tool mit nicht genügend Speicherplatz, um die Option &quot;Außerkraftsetzungen&quot; anzuzeigen" lightbox="../media/javascript-overrides-folder-setup-complete.msft.png":::
       Erfolgreiche Einrichtung eines Overrides-Ordners  
    :::image-end:::  
    
## Hinzufügen von Dateien zu Ihrem Overrides-Ordner  
  
Zum Hinzufügen von Dateien zu Ihrem Überschreibungen-Ordner öffnen Sie das **Element** Tool, und überprüfen Sie die Webseite.  Wählen Sie zum Bearbeiten im **Formatvorlagen** -Inspektor den Namen der CSS-Datei aus.  

:::image type="complex" source="../media/javascript-overrides-select-css-file.msft.png" alt-text="Quellen Tool mit nicht genügend Speicherplatz, um die Option &quot;Außerkraftsetzungen&quot; anzuzeigen" lightbox="../media/javascript-overrides-select-css-file.msft.png":::
   Auswählen einer Datei im **Formatvorlagen** -Inspektor  
:::image-end:::  

Zeigen Sie im **Quellen** -Editor auf den Dateinamen der ausgewählten Datei, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **für Außerkraftsetzungen speichern**aus.  

:::image type="complex" source="../media/javascript-overrides-file-name.msft.png" alt-text="Quellen Tool mit nicht genügend Speicherplatz, um die Option &quot;Außerkraftsetzungen&quot; anzuzeigen" lightbox="../media/javascript-overrides-file-name.msft.png":::
   Fügen Sie im **Quellen** -Editor den Namen der Datei hinzu, die überschrieben werden soll.  
:::image-end:::  

:::image type="complex" source="../media/javascript-overrides-save-for-overrides.msft.png" alt-text="Quellen Tool mit nicht genügend Speicherplatz, um die Option &quot;Außerkraftsetzungen&quot; anzuzeigen" lightbox="../media/javascript-overrides-save-for-overrides.msft.png":::
   Wählen Sie im Kontextmenü die Option **für Außerkraftsetzungen speichern** aus.  
:::image-end:::  

Die Datei wird im Ordner Overrides gespeichert.  Überprüfen Sie, ob devtools einen Ordner mit dem Namen der URL der Datei mit der richtigen Verzeichnisstruktur erstellt.  Die Datei wird in gespeichert.  Der Dateiname im Editor zeigt nun auch einen lila Punkt an, der angibt, dass die Datei lokal und nicht Live ist.  

:::image type="complex" source="../media/javascript-overrides-file-stored.msft.png" alt-text="Quellen Tool mit nicht genügend Speicherplatz, um die Option &quot;Außerkraftsetzungen&quot; anzuzeigen" lightbox="../media/javascript-overrides-file-stored.msft.png":::
   Die Datei wurde erfolgreich im Ordner "Overrides" gespeichert  
:::image-end:::  

:::row:::
   :::column span="":::
      Im folgenden Beispiel können Sie nun die Formatvorlagen der Webseite ändern.  Wenn Sie einen roten Rahmen um die Datei hinzufügen möchten, kopieren Sie den folgenden Stil im **Formatvorlagen** -Editor, und fügen Sie ihn dem Body-Element hinzu.  
      
      ```css
      border: 10px solid firebrick
      ```  
   :::column-end:::
   :::column span="":::
      Die Datei wird automatisch auf Ihrem Computer gespeichert.  Wenn Sie die Datei aktualisieren, wird der Rahmen angezeigt, und keine ihrer Arbeit geht verloren.  
      
      :::image type="complex" source="../media/javascript-overrides-changing-styles.msft.png" alt-text="Quellen Tool mit nicht genügend Speicherplatz, um die Option &quot;Außerkraftsetzungen&quot; anzuzeigen" lightbox="../media/javascript-overrides-changing-styles.msft.png":::
         Dauerhaftes ändern von Webseitenformat Vorlagen durch Bearbeiten einer Datei im Ordner "Außerkraftsetzungen"  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

:::row:::
   :::column span="":::
      Zeigen Sie im Bereich " **Quellen** " im Abschnitt " **Seite** " auf eine beliebige Datei, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und fügen Sie es zu Außerkraftsetzungen hinzu.  Auch die Dateien, die sich bereits im Ordner "Außerkraftsetzungen" befinden, haben einen lila Punkt auf dem Symbol.  
      
      :::image type="complex" source="../media/javascript-overrides-safe-from-sources.msft.png" alt-text="Quellen Tool mit nicht genügend Speicherplatz, um die Option &quot;Außerkraftsetzungen&quot; anzuzeigen" lightbox="../media/javascript-overrides-safe-from-sources.msft.png":::
         Auswählen einer Datei aus dem **Quellen** Tool für Außerkraftsetzungen  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Sie können aber auch im **Netzwerk** Tool auf eine beliebige Datei zeigen, das Kontextmenü öffnen \ (mit der rechten Maustaste auf \) klicken und es zu Außerkraftsetzungen hinzufügen.  Wenn Außerkraftsetzungen aktiviert sind, finden Sie Dateien, die sich auf Ihrem Computer und nicht auf der Live-Webseite befinden.  Wenn Außerkraftsetzungen aktiviert sind, suchen Sie im Tool **Netzwerk** nach einem Warnungssymbol neben dem Dateinamen.  
      
      :::image type="complex" source="../media/javascript-overrides-network.msft.png" alt-text="Quellen Tool mit nicht genügend Speicherplatz, um die Option &quot;Außerkraftsetzungen&quot; anzuzeigen" lightbox="../media/javascript-overrides-network.msft.png":::
         Auswählen einer Datei aus dem **Netzwerk** Tool für Außerkraftsetzungen  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Bidirektionale Interaktion von Außerkraftsetzungen  

Verwenden Sie den mit dem **Sources** -Tool von devtools bereitgestellten Editor oder einen beliebigen Editor, in dem Sie die Dateien ändern möchten.  Änderungen werden über alle Produkte synchronisiert, die auf die Dateien im Ordner "Außerkraftsetzungen" zugreifen.  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsSourcesTool]: ../sources.md "Übersicht über das Quellen Tool | Microsoft docs"  
