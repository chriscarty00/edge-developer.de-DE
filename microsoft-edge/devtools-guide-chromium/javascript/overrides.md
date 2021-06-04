---
description: Das Außerkraftsetzungsfeature ist ein Feature im Sources-Tool von Microsoft Edge DevTools, mit dem Sie Webseitenressourcen auf Ihre Festplatte kopieren können.  Wenn Sie die Webseite aktualisieren, laden DevTools die Ressource nicht, sondern ersetzen sie durch Ihre lokale Kopie.
title: Überschreiben von Webseitenressourcen mit lokalen Kopien mithilfe Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 66c0686c166163f1640384d096288af0b530f135
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519436"
---
# <a name="override-webpage-resources-with-local-copies-using-microsoft-edge-devtools"></a>Überschreiben von Webseitenressourcen mit lokalen Kopien mithilfe Microsoft Edge DevTools  

Manchmal müssen Sie einige mögliche Korrekturen für eine Webseite ausprobieren, aber Sie haben keinen Zugriff auf die Quelldateien, oder das Ändern der Seite erfordert einen langsamen und komplexen Buildprozess.  Sie können alle Arten von Problemen in DevTools debuggen und beheben.  Die Änderungen bleiben jedoch nicht erhalten. Nachdem Sie die lokale Datei aktualisiert haben, sind alle Ihre Arbeit weg.  Das Überschreibungsfeature im [Tool Quellen][DevToolsSourcesTool] hilft Ihnen bei der Lösung dieses Problems.  

Sie können nun eine Ressource der aktuellen Webseite verwenden und lokal speichern.  Wenn Sie die Webseite aktualisieren, wird die Ressource vom Browser nicht vom Server geladen.  Stattdessen ersetzt der Browser sie durch Ihre lokale Kopie der Ressource.  

## <a name="setting-up-your-local-folder-to-store-overrides"></a>Einrichten des lokalen Ordners zum Speichern von Außerkraftsetzungen  

1.  Navigieren Sie zum **Tool Quellen.**  
1.  Wählen Sie **im Bereich Navigator** (links) die Registerkarte **Außerkraftsetzungen** aus.  Wenn die **Registerkarte** Außerkraftsetzungen nicht angezeigt wird, wählen Sie die Option <code>&#x0226B;</code><!--`≫`-->  aus.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-overflow-menu.msft.png" alt-text="Quellentool mit nicht genügend Platz zum Anzeigen der Option Außerkraftsetzungen" lightbox="../media/javascript-overrides-overflow-menu.msft.png":::
             **Quellentool** mit nicht genügend Platz zum Anzeigen der Option "Außerkraftsetzungen"  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-menu.msft.png" alt-text="Auswählen der Option Außerkraftsetzungen" lightbox="../media/javascript-overrides-menu.msft.png":::
             Auswählen der Option Außerkraftsetzungen  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Wählen Sie einen Ordner auf dem lokalen Computer aus, um die Ressourcendateien zu speichern, die Sie ersetzen möchten.  
     *   Wenn Sie nach einem Ordner suchen möchten, wählen Sie **+ Ordner für Außerkraftsetzungen auswählen aus.**  
    
    :::image type="complex" source="../media/javascript-overrides-select-folder.msft.png" alt-text="Auswählen eines Ordners, der für Außerkraftsetzungen verwendet werden soll" lightbox="../media/javascript-overrides-select-folder.msft.png":::
       Auswählen eines Ordners, der für Außerkraftsetzungen verwendet werden soll  
    :::image-end:::  
    
1.  DevTools warnt Sie, dass Sie voll auf den Ordner zugreifen müssen und keine vertraulichen Informationen preis geben sollten.  Wählen Sie auf der Warnleiste Die Option **Zugriff** gewähren zulassen aus.  
    
    :::image type="complex" source="../media/javascript-overrides-give-access-to-folder.msft.png" alt-text="Gewähren von DevTools-Zugriff auf Ordner" lightbox="../media/javascript-overrides-give-access-to-folder.msft.png":::
       Gewähren von DevTools-Zugriff auf Ordner  
    :::image-end:::  
    
1.  Auf der **Registerkarte Außerkraftsetzungen** wird neben Lokale Außerkraftsetzungen aktivieren ein **Kontrollkästchen angezeigt.**  Rechts neben **Lokale** Außerkraftsetzungen aktivieren befindet sich ein **Clear-Konfigurationssymbol,** mit dem Sie Ihre einstellungen für lokale Außerkraftsetzungen löschen können.  Sie sind nun mit dem Einrichten Ihres Ordners fertig und können Liveressourcen durch lokale ersetzen.
    
    :::image type="complex" source="../media/javascript-overrides-folder-setup-complete.msft.png" alt-text="Erfolgreiches Einrichten eines Außerkraftsetzungsordners" lightbox="../media/javascript-overrides-folder-setup-complete.msft.png":::
       Erfolgreiches Einrichten eines Außerkraftsetzungsordners  
    :::image-end:::  
    
## <a name="adding-files-to-your-overrides-folder"></a>Hinzufügen von Dateien zum Ordner Außerkraftsetzungen  
  
Öffnen Sie das Elementtool, und **** überprüfen Sie die Webseite, um Dem Ordner "Außerkraftsetzungen" Dateien hinzuzufügen.  Wählen Sie zum Bearbeiten den Namen der CSS-Datei im **Formatvorlageninspektor** aus.  

:::image type="complex" source="../media/javascript-overrides-select-css-file.msft.png" alt-text="Auswählen einer Datei im Formatvorlageninspektor" lightbox="../media/javascript-overrides-select-css-file.msft.png":::
   Auswählen einer Datei im **Formatvorlageninspektor**  
:::image-end:::  

Zeigen Sie **im Editor** Quellen auf den Dateinamen der ausgewählten Datei, öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie Speichern für **Außerkraftsetzungen aus.**  

:::image type="complex" source="../media/javascript-overrides-file-name.msft.png" alt-text="Fügen Sie im Quellen-Editor den Namen der Datei zu Außerkraftsetzungen hinzu." lightbox="../media/javascript-overrides-file-name.msft.png":::
   Fügen Sie **im Quellen-Editor** den Namen der Datei zu Außerkraftsetzungen hinzu.  
:::image-end:::  

:::image type="complex" source="../media/javascript-overrides-save-for-overrides.msft.png" alt-text="Wählen Sie im Kontextmenü Speichern für Außerkraftsetzungen aus." lightbox="../media/javascript-overrides-save-for-overrides.msft.png":::
   Wählen Sie im Kontextmenü Speichern **für Außerkraftsetzungen aus.**  
:::image-end:::  

Die Datei wird in Ihrem Überschreibungsordner gespeichert.  Stellen Sie sicher, dass DevTools einen Ordner mit dem Namen mithilfe der URL der Datei mit der richtigen Verzeichnisstruktur erstellt.  Die Datei wird darin gespeichert.  Der Dateiname im Editor zeigt nun auch einen lila Punkt an, der angibt, dass die Datei lokal und nicht live ist.  

:::image type="complex" source="../media/javascript-overrides-file-stored.msft.png" alt-text="Die Datei wurde erfolgreich im Ordner "Außerkraftsetzungen" gespeichert." lightbox="../media/javascript-overrides-file-stored.msft.png":::
   Die Datei wurde erfolgreich im Ordner "Außerkraftsetzungen" gespeichert.  
:::image-end:::  

:::row:::
   :::column span="":::
      Im folgenden Beispiel können Sie nun die Formatvorlagen der Webseite ändern.  Wenn Sie einen roten Rahmen um **** die Datei hinzufügen möchten, kopieren Sie im Formatvorlagen-Editor die folgende Formatvorlage, und fügen Sie sie dem body-Element hinzu.  
      
      ```css
      border: 10px solid firebrick
      ```  
   :::column-end:::
   :::column span="":::
      Die Datei wird automatisch auf Ihrem Computer gespeichert.  Wenn Sie die Datei aktualisieren, wird der Rahmen angezeigt, und ihre Arbeit geht nicht verloren.  
      
      :::image type="complex" source="../media/javascript-overrides-changing-styles.msft.png" alt-text="Webseitenformatvorlagen dauerhaft ändern, indem Sie eine Datei im Ordner "Außerkraftsetzungen" bearbeiten" lightbox="../media/javascript-overrides-changing-styles.msft.png":::
         Webseitenformatvorlagen dauerhaft ändern, indem Sie eine Datei im Ordner "Außerkraftsetzungen" bearbeiten  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

:::row:::
   :::column span="":::
      Zeigen Sie **im Tool** Quellen im Abschnitt **Seite** auf eine beliebige Datei, öffnen Sie das Kontextmenü \(mit der rechten Maustaste auf\), und fügen Sie es außer Kraft.  Auch hier haben Dateien, die sich bereits im Ordner "Außerkraftsetzungen" befinden, einen lila Punkt auf dem Symbol.  
      
      :::image type="complex" source="../media/javascript-overrides-safe-from-sources.msft.png" alt-text="Auswählen einer Datei aus dem Tool "Quellen" für Außerkraftsetzungen" lightbox="../media/javascript-overrides-safe-from-sources.msft.png":::
         Auswählen einer Datei aus dem **Tool "Quellen"** für Außerkraftsetzungen  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Alternativ zeigen Sie im **Netzwerktool** auf eine beliebige Datei, öffnen Sie das Kontextmenü \(rechtsklicken\), und fügen Sie es außer Kraft.  Wenn Außerkraftsetzungen wirksam sind, dateien, die sich auf Ihrem Computer befinden und nicht von der Livewebseite.  Wenn Außerkraftsetzungen wirksam sind, suchen Sie im **Netzwerktool** ein Warnsymbol neben dem Dateinamen.  
      
      :::image type="complex" source="../media/javascript-overrides-network.msft.png" alt-text="Auswählen einer Datei aus dem Netzwerktool für Außerkraftsetzungen" lightbox="../media/javascript-overrides-network.msft.png":::
         Auswählen einer Datei aus dem **Netzwerktool** für Außerkraftsetzungen  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="two-way-interaction-of-overrides"></a>Zwei-Wege-Interaktion von Außerkraftsetzungen  

Verwenden Sie den Editor, der mit dem **Sources-Tool** von DevTools oder einem beliebigen Editor bereitgestellt wird, den Sie ändern möchten.  Änderungen werden für alle Produkte synchronisiert, die auf die Dateien im Ordner "Außerkraftsetzungen" zugreifen.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsSourcesTool]: ../sources/index.md "Übersicht über das | Microsoft Docs"  
