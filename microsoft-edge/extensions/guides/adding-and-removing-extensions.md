---
description: Erfahren Sie, wie Sie Erweiterungen hinzufügen und entfernen sowie die Schaltfläche einer Erweiterung neben die Adressleiste verschieben können.
title: Hinzufügen und Entfernen von Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, HTML, CSS, JavaScript, Entwickler, Erweiterung
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: aeebc0f18d6b4a743c790571b8287a209233e73f
ms.sourcegitcommit: 1e33cd41e5afb2e6dbdc19353011ff6c2b019f9c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2020
ms.locfileid: "10866078"
---
# Hinzufügen, Verschieben und Entfernen von Erweiterungen für Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Die Microsoft Edge-Unterstützung für Erweiterungen wurde im **Windows 10 Anniversary Update** eingeführt. Wenn Sie eine Microsoft Edge-Erweiterung entwickeln und sie laden möchten oder wenn Sie sie bereits verwenden und jetzt entfernen möchten, lesen Sie die folgenden Schritte.
Außerdem finden Sie hier Einzelheiten dazu, wie Sie die Position Ihres Erweiterungssymbols im Browser ändern können.

## Hinzufügen einer Erweiterung

1. Öffnen Sie Microsoft Edge, und geben Sie "about:flags" in die Adressleiste ein.

2. Aktivieren Sie das Kontrollkästchen **Entwicklerfunktionen für Erweiterungen aktivieren**.

   !["about:flags" aktivieren Entwicklerfeatures](./../media/sideload-aboutflags.png)
   > [!NOTE]
   > Wenn Sie nicht über das Windows 10 Anniversary Update oder höher verfügen, steht diese Option nicht zur Verfügung.

3. Wählen Sie **Mehr (...)** aus, um das Menü zu öffnen.

   ![Schaltfläche "Mehr"](./../media/morebutton.png)  

4. Wählen Sie **Erweiterungen** aus dem Menü aus.

5. Klicken Sie auf die Schaltfläche **Erweiterung laden**.

   !["Erweiterung laden" auswählen](./../media/sideload-load-extension.png)

6. Navigieren Sie zum Ordner Ihrer Erweiterung, und wählen Sie die Schaltfläche **Ordner auswählen** aus.
   ![Zu ladenden Erweiterungsordner auswählen](./../media/sideload-select-extension.png)
   > [!NOTE]
   > Wird beim Laden der Erweiterung eine Fehlermeldung angezeigt, finden Sie weitere Anleitungen auf der Seite [Problembehandlung](./../troubleshooting.md).


**Sie sind fertig! Die Erweiterung sollte nun im Erweiterungsbereich von Microsoft Edge aufgelistet sein.**

![Erweiterung im Erweiterungsbereich](./../media/sideload-extension-installed.png)

> [!NOTE]
> Bei nachfolgenden Starts von Microsoft Edge werden nicht signierte Erweiterungen automatisch deaktiviert. Wenn der Browser in einen Ruhezustand übergeht (nach etwa 10 Sekunden Inaktivität), wird unten im Fenster die folgende Benachrichtigung angezeigt. ![Riskikobenachrichtigung](./../media/riskynotification.png) Um die unsignierten Erweiterungen zu aktivieren, klicken Sie auf "Trotzdem aktivieren".



## Verschieben der Schaltfläche "Erweiterung"
Je nach den Einstellungen ihrer Erweiterung kann Sie im Menü **Mehr (...)** angezeigt werden.

   ![Aktionsbereich](./../media/browseraction.png)  


Wenn Sie die Schaltfläche für einen einfacheren Zugriff aus diesem Menü heraus verschieben möchten:

1. Klicken Sie mit der rechten Maustaste auf die Schaltfläche "Erweiterung".

2. Wählen Sie **Schaltfläche neben Adressleiste anzeigen** aus.

   ![Aktionsbereich](./../media/browseraction_contextmenu.png)  

Alternativ können Sie dies über die Seite mit den Erweiterungsdetails tun:

1. Klicken Sie auf die Schaltfläche "Erweiterung".
2. Aktivieren Sie **Schaltfläche neben Adressleiste anzeigen**.

   ![Aktivierte Umschaltfläche zum Anzeigen der Schaltfläche](./../media/show-button-toggle.png)

> [!NOTE]
> Sie können die Schaltfläche jederzeit zurück zum Menü **Mehr (...)** bewegen, indem Sie mit der rechten Maustaste darauf klicken und die Option **Neben der Adressleiste anzeigen** deaktivieren oder die Option **Schaltfläche neben Adressleiste anzeigen** auf der Seite mit den Erweiterungsdetails deaktivieren.


## Entfernen einer Erweiterung

1. Öffnen Sie Microsoft Edge.

2. Wählen Sie **Mehr (...)** aus, um das Menü zu öffnen.

3. Wählen Sie **Erweiterungen** aus dem Menü aus.

4. Klicken Sie mit der rechten Maustaste auf die zu entfernende Erweiterung, und wählen Sie **Entfernen** aus, oder wählen Sie die Erweiterung aus, und klicken Sie auf die Schaltfläche **Entfernen**.

   ![Aktionsbereich](./../media/remove.png)  

**Die Erweiterung sollte nun nicht mehr in der Liste in Microsoft Edge angezeigt werden.**
