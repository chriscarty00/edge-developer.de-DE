---
description: Hier erfahren Sie, wie Sie Erweiterungen hinzufügen und entfernen sowie die Schaltfläche einer Erweiterung neben der Adressleiste verschieben.
title: Hinzufügen und Entfernen von Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, Erweiterung
ms.custom: seodec18
localization_priority: Priority
ms.openlocfilehash: fdc6950962e7ce7e0a720d0bafa7e2c63ebd7098
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567431"
---
# Hinzufügen, verschieben und Entfernen von Erweiterungen für Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Microsoft Edge-Unterstützung für Erweiterungen wurde im **Windows 10 Anniversary Update**eingeführt. Wenn Sie eine Microsoft Edge-Erweiterung entwickeln und Sie laden möchten, oder wenn Sie Sie bereits haben und jetzt entfernen möchten, lesen Sie die folgenden Schritte aus.
Darüber hinaus finden Sie Informationen dazu, wie Sie die Position Ihres Erweiterungssymbols im Browser ändern können.

## Hinzufügen einer Erweiterung

1. Öffnen Sie Microsoft Edge, und geben Sie "about: Flags" in die Adressleiste ein.

2. Aktivieren Sie das Kontrollkästchen **Erweiterungsentwickler Features aktivieren** .

   ![Info: Flags aktivieren von Entwicklerfeatures](./../media/sideload-aboutflags.png)
   > [!NOTE]
   > Wenn Sie nicht über das Windows 10 Anniversary Update oder höher verfügen, ist diese Option nicht verfügbar.

3. Wählen Sie **mehr (.** ..) aus, um das Menü zu öffnen.

   ![Schaltfläche "Weitere"](./../media/morebutton.png)  

4. Wählen Sie im Menü **Erweiterungen** aus.

5. Wählen Sie die Schaltfläche **Erweiterung laden** aus.

   ![Auswählen der Lade Erweiterung](./../media/sideload-load-extension.png)

6. Navigieren Sie zum Ordner Ihrer Erweiterung, und wählen Sie die Schaltfläche **Ordner auswählen** aus.
   ![Auswählen des zu ladenden Erweiterungs Ordners](./../media/sideload-select-extension.png)
   > [!NOTE]
   > Wenn beim Laden der Erweiterung eine Fehlermeldung angezeigt wird, lesen Sie auf der Seite zur [Problembehandlung](./../troubleshooting.md) nach Anleitungen.


**Sie haben es geschafft! Die im Erweiterungsbereich von Microsoft Edge aufgelistete Erweiterung wird nun angezeigt.**

![Erweiterung im Erweiterungsbereich](./../media/sideload-extension-installed.png)

> [!NOTE]
> Nicht signierte Erweiterungen werden bei nachfolgenden Starts von Microsoft Edge automatisch deaktiviert. Wenn der Browser in einen Ruhezustand wechselt (nach ungefähr 10 Sekunden Inaktivität), wird unten im Fenster die folgende Benachrichtigung angezeigt. ![riskante Benachrichtigung](./../media/riskynotification.png) Wenn Sie die nicht signierten Erweiterungen aktivieren möchten, klicken Sie auf "trotzdem einschalten".



## Verschieben der Erweiterungsschaltfläche
Je nach den Einstellungen ihrer Erweiterung kann Sie im Menü **mehr (.** ..) angezeigt werden.

   ![Menü ' Aktionen '](./../media/browseraction.png)  


Wenn Sie die Schaltfläche für einen einfacheren Zugriff aus diesem Menü verschieben möchten, gehen Sie wie folgt vor:

1. Klicken Sie mit der rechten Maustaste auf die Erweiterungsschaltfläche.

2. Wählen Sie **neben der Adressleiste die Schaltfläche anzeigen**aus.

   ![Menü ' Aktionen '](./../media/browseraction_contextmenu.png)  

Sie können dies auch über die Seite mit den Erweiterungs Details tun:

1. Klicken Sie auf die Erweiterungsschaltfläche.
2. **Schaltfläche "anzeigen" neben Adressleiste** auf ein umschalten.

   ![Schaltfläche "Schalter anzeigen" aktiviert](./../media/show-button-toggle.png)

> [!NOTE]
> Sie können die Schaltfläche immer wieder in das Menü **mehr (...)** verschieben, indem Sie mit der rechten Maustaste darauf klicken und die Option **neben der Adressleiste anzeigen** oder auf der Seite Erweiterungs Details auf die **Schaltfläche "anzeigen" neben "Adressleiste"** und dann auf "aus" klicken.


## Entfernen einer Erweiterung

1. Öffnen Sie Microsoft Edge.

2. Wählen Sie **mehr (.** ..) aus, um das Menü zu öffnen.

3. Wählen Sie im Menü **Erweiterungen** aus.

4. Klicken Sie mit der rechten Maustaste auf die zu entfernende Erweiterung, wählen Sie **Entfernen**aus, oder wählen Sie die Erweiterung aus, und klicken Sie auf die Schaltfläche **Entfernen** .

   ![Menü ' Aktionen '](./../media/remove.png)  

**Die Erweiterung sollte aus der Liste in Microsoft Edge verschwinden.**
