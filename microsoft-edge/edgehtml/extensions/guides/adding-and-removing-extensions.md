---
description: Erfahren Sie, wie Sie Erweiterungen hinzufügen und entfernen sowie die Schaltfläche einer Erweiterung neben die Adressleiste verschieben können.
title: Hinzufügen und Entfernen von Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, HTML, CSS, JavaScript, Entwickler, Erweiterung
ms.custom: seodec18
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2ef75e76795d527935a84913528506bfa042e56f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398875"
---
# <a name="adding-moving-and-removing-extensions-for-microsoft-edge"></a>Hinzufügen, Verschieben und Entfernen von Erweiterungen für Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Die Microsoft Edge-Unterstützung für Erweiterungen wurde im **Windows 10 Anniversary Update** eingeführt.  Wenn Sie eine Microsoft Edge-Erweiterung entwickeln und sie laden möchten oder wenn Sie sie bereits verwenden und jetzt entfernen möchten, lesen Sie die folgenden Schritte.  
Außerdem finden Sie hier Einzelheiten dazu, wie Sie die Position Ihres Erweiterungssymbols im Browser ändern können.  

## <a name="adding-an-extension"></a>Hinzufügen einer Erweiterung  

1.  Öffnen Sie Microsoft Edge, und geben `about:flags` Sie die Adressleiste ein.  
1.  Aktivieren Sie das Kontrollkästchen **Entwicklerfunktionen für Erweiterungen aktivieren**.  
    
    !["about:flags" aktivieren Entwicklerfeatures](../media/sideload-aboutflags.png)  
    
    > [!NOTE]
    > Wenn Sie nicht über das Windows 10 Anniversary Update oder höher verfügen, steht diese Option nicht zur Verfügung.  
    
1.  Wählen Sie **Mehr (...)** aus, um das Menü zu öffnen.  
    
    ![Schaltfläche "Mehr"](../media/morebutton.png)  
    
1.  Wählen Sie **Erweiterungen** aus dem Menü aus.  
    
1.  Klicken Sie auf die Schaltfläche **Erweiterung laden**.  
    
    !["Erweiterung laden" auswählen](../media/sideload-load-extension.png)  
    
1.  Navigieren Sie zum Ordner Ihrer Erweiterung, und wählen Sie die Schaltfläche **Ordner auswählen** aus.  
    
    ![Zu ladenden Erweiterungsordner auswählen](../media/sideload-select-extension.png)  
    
    > [!NOTE]
    > Wird beim Laden der Erweiterung eine Fehlermeldung angezeigt, finden Sie weitere Anleitungen auf der Seite [Problembehandlung](../troubleshooting.md).  
    
**Sie sind fertig! Die Erweiterung sollte nun im Erweiterungsbereich von Microsoft Edge aufgelistet sein.**  

![Erweiterung im Erweiterungsbereich](../media/sideload-extension-installed.png)  

> [!NOTE]
> Bei nachfolgenden Starts von Microsoft Edge werden nicht signierte Erweiterungen automatisch deaktiviert.  Wenn der Browser in einen Leerlaufzustand \(nach ca. 10 Sekunden Inaktivität\) tritt, wird am unteren Rand des Fensters die folgende Benachrichtigung angezeigt.  ![riskante ](../media/riskynotification.png) Benachrichtigung Zum Aktivieren der nicht signierten Erweiterungen klicken Sie **trotzdem auf Aktivieren.**  

## <a name="moving-the-extension-button"></a>Verschieben der Schaltfläche "Erweiterung"  

Je nach den Einstellungen ihrer Erweiterung kann Sie im Menü **Mehr (...)** angezeigt werden.  

![Aktionsbereich](../media/browseraction.png)  

Wenn Sie die Schaltfläche für einen einfacheren Zugriff aus diesem Menü heraus verschieben möchten:  

1.  Klicken Sie mit der rechten Maustaste auf die Schaltfläche "Erweiterung".  
1.  Wählen Sie **Schaltfläche neben Adressleiste anzeigen** aus.  
    
    ![Kontextmenü im Menü "Aktionen"](../media/browseraction_contextmenu.png)  
    
Alternativ können Sie dies über die Seite mit den Erweiterungsdetails tun:  

1.  Klicken Sie auf die Schaltfläche "Erweiterung".  
1.  Aktivieren Sie **Schaltfläche neben Adressleiste anzeigen**.  
    
    ![Aktivierte Umschaltfläche zum Anzeigen der Schaltfläche](../media/show-button-toggle.png)  
    
> [!NOTE]
> Sie können die Schaltfläche jederzeit zurück zum Menü **Mehr (...)** bewegen, indem Sie mit der rechten Maustaste darauf klicken und die Option **Neben der Adressleiste anzeigen** deaktivieren oder die Option **Schaltfläche neben Adressleiste anzeigen** auf der Seite mit den Erweiterungsdetails deaktivieren.  

## <a name="removing-an-extension"></a>Entfernen einer Erweiterung  

1.  Öffnen Sie Microsoft Edge.  
1.  Wählen Sie **Mehr (...)** aus, um das Menü zu öffnen.  
1.  Wählen Sie **Erweiterungen** aus dem Menü aus.  
1.  Klicken Sie mit der rechten Maustaste auf die zu entfernende Erweiterung, und wählen Sie **Entfernen** aus, oder wählen Sie die Erweiterung aus, und klicken Sie auf die Schaltfläche **Entfernen**.  
    
    ![Entfernen im Menü "Aktionen"](../media/remove.png)  
    
**Die Erweiterung sollte nun nicht mehr in der Liste in Microsoft Edge angezeigt werden.**  
