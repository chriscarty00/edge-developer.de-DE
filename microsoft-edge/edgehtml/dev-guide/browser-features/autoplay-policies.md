---
description: Sicherstellen, dass sich der Medieninhalt auf Ihrer Website wie vorgesehen verhält
title: Richtlinien zur automatischen Wiedergabe – dev-Leitfaden
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Medien, Video, Audio, automatische Wiedergabe
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 85b91a8b87d73d6fccc6eac2aa64513f283d7f21
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233860"
---
# Richtlinien für die automatische Wiedergabe  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Microsoft Edge bietet Kunden die Möglichkeit, Ihre Browsereinstellungen auf Websites zu personalisieren, die Medien mit Sound wiedergeben, um Ablenkungen im Internet zu minimieren und die Bandbreite zu sparen.  Darüber hinaus unterdrückt Microsoft Edge automatisch die automatische Wiedergabe von Medien in Hintergrundregisterkarten.  

Benutzer können das Medienverhalten mit den Steuerelementen für die automatische Wiedergabe auf [globaler](#global-media-autoplay-settings) und [pro Website](#per-site-media-autoplay-settings) anpassen, die die folgenden Optionen bieten:  

*   `Allow`  Die Standardeinstellung, und die Wiedergabe von Videos erfolgt weiterhin, wenn eine Registerkarte zuerst im Vordergrund angezeigt wird, nach Ermessen der Website.  

*   `Limit`  Schränkt die automatische Wiedergabe ein, wenn Videos stumm geschaltet sind, sodass die Benutzer nie von Sound überrascht werden.  Nachdem der Benutzer auf eine beliebige Stelle auf der Seite geklickt hat, ist die automatische Wiedergabe wieder aktiviert und wird weiterhin innerhalb dieser Domäne auf dieser Registerkarte zugelassen.  

*   `Block`  Verhindern Sie sautoplay auf allen Websites, bis Benutzer direkt mit dem Medieninhalt interagieren.  

## Einstellungen für die automatische Wiedergabe globaler Medien  

Benutzer können das Standardverhalten für die automatische Wiedergabe für alle Websites unter **Erweiterte Einstellung**  >  **Medien Automatik**steuern.  

:::image type="complex" source="../media/autoplay_global.png" alt-text="Einstellungen für die automatische Wiedergabe globaler Medien" lightbox="../media/autoplay_global.png":::
   Einstellungen für die automatische Wiedergabe globaler Medien  
:::image-end:::  

## Einstellungen für die automatische Wiedergabe von Medien pro Website  

Benutzer können das Verhalten der automatischen Wiedergabe pro Website unter dem Abschnitt " **Websiteberechtigungen** " im Bereich "Website Informationen" steuern.  Diese Einstellung finden Sie, indem Sie auf das Symbol "Informationen" oder das Symbol "Sperren" auf der linken Seite der Adressleiste klicken und dann auf "Einstellungen für die **Medienwiedergabe** " klicken, um zu beginnen.  

Einstellungen pro Website überschreiben die globale Einstellung.  Wenn ein Benutzer beispielsweise die globale Einstellung auf `Allow` eine Einstellung pro Website festgelegt hat `Block` , wird die automatische Wiedergabe für diese Website blockiert.  

:::image type="complex" source="../media/autoplay_per-site.png" alt-text="Einstellungen für die automatische Wiedergabe von Medien pro Website" lightbox="../media/autoplay_per-site.png":::
   Einstellungen für die automatische Wiedergabe von Medien pro Website  
:::image-end:::  

## Bewährte Methoden für Web-Entwickler  

Hier erfahren Sie, wie Sie eine gute Benutzerfreundlichkeit mit auf Ihrer Website gehosteten Medien gewährleisten:  

*   Davon ausgehen, dass für jede Verwendung eines Medienelements Wil eine Benutzergeste erforderlich ist, um die Wiedergabe zu starten \ (da Benutzer die automatische Wiedergabe zu einem beliebigen Zeitpunkt blockieren können \) und entsprechend planen.  Global-und pro-Site-AutoPlay-Richtlinien gelten für alle `<audio>` und `<video>` Elemente, unabhängig davon, wie Sie auf Ihrer Website verwendet werden.  

*   Stellen Sie sicher, dass mediensteuerelemente immer auf dem Website Medium und dem Anzeigeninhalt vorhanden sind.  Dadurch können Benutzer die Wiedergabe neu starten, wenn die automatische Wiedergabe auf der Seite blockiert ist.  

*   Bewerten Sie, wie die automatische Wiedergabe die Benutzerfreundlichkeit auf Ihrer Website beeinträchtigen kann, und verwenden Sie die automatische Wiedergabe auf eine Weise, die unerwünschte Medienwiedergabe minimiert.  Wenn die automatische Wiedergabe ein entscheidender Bestandteil ihrer Erfahrung ist, sollten Sie die Verwendung von stummgeschaltetem Inhalt verwenden, damit der Benutzer die Stummschaltung aufheben kann.  Für stummgeschaltete Inhalte muss die Audioquelle entweder explizit stumm geschaltet oder nicht eingestellt sein.  Andernfalls wird das Element nicht als stumm geschaltet angesehen.  

*   Verwenden Sie die systemeigenen Browsersteuerelemente für die Medienwiedergabe, sofern dies nicht unbedingt erforderlich ist.  Dadurch wird eine konsistente Benutzeroberfläche gewährleistet.  Wenn Sie stattdessen benutzerdefinierte Steuerelemente erstellen, stellen Sie sicher, dass die mediensteuerelemente immer vorhanden sind und dass Ihre Steuerelemente auf die Unterdrückung der automatischen Wiedergabe reagieren.  

### Iframe-Delegierung  

Die automatische Wiedergabe in einer `<iframe>` erbt die Berechtigung "AutoPlay" von der übergeordneten Seite unabhängig vom Inhalts Ursprung.  In einem Wiedergabelisten Szenario, in dem jede Mediendatei von einem separaten IFrame gehostet wird, muss der Benutzer die Wiedergabe nur einmal für die gesamte Wiedergabeliste initiieren.  

### Erkennen, wenn die automatische Wiedergabe zulässig ist  

Sie können die Wiedergabesteuerelemente so anpassen, dass der richtige Zustand angezeigt wird, wenn die automatische Wiedergabe blockiert wird, indem Sie die von der `play()` Funktion für das Medienelement zurückgegebene Versprechung untersuchen:  

```javascript
var promise = document.querySelector('video').play();

if (promise !== undefined) { 
    promise.catch(_error => { 
        // Autoplay was blocked
        // Show user media controls to manually start playback
    }).then(() => { 
        // Autoplay started
    }); 
}
```  
