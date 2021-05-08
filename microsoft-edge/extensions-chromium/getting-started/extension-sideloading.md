---
description: Testen Der Erweiterung durch Querladen im Browser
title: Querladen der Erweiterung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge Chromium, Webentwicklung, html, css, javascript, Entwickler, Erweiterungen
ms.openlocfilehash: 7070878b9608e6d239179078390f2315e0b289a1
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104773"
---
# Eine Erweiterung querladen

Während der Entwicklung können Sie den browser Microsoft Edge \(Chromium\) verwenden, um die Erweiterung sicher zu ausführen und zu debuggen. Indem Sie Ihre Erweiterung lokal in Ihrem Browser querladen, können Sie Ihre Erweiterung ausführen und testen. In diesem Artikel wird das Querladen von Erweiterungen in Microsoft Edge.

Führen Sie die folgenden Schritte aus, um die Erweiterung quer zu laden.

1.  Öffnen Sie die Seite, indem Sie die drei Punkte oben im Browser auswählen und dann `edge://extensions` **Erweiterungen auswählen.**

       :::image type="complex" source="./media/part1-threedots.png" alt-text="Öffnen der edge://extensions Seite":::
          Öffnen der edge://extensions Seite :::image-end:::

1.  Aktivieren Sie auf der Seite Erweiterungsverwaltung unter den Entwicklermodus mit dem Umschalter unten `edge://extensions` links auf der Seite. ****

       :::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Aktivieren des Entwicklermodus":::
          Aktivieren des Entwicklermodus :::image-end:::

1.  Wählen Sie bei der ersten Installation der Erweiterung die Option **Entpackt laden aus.**  Sie werden zur Eingabe des Verzeichnisses mit ihren Erweiterungsquellendateien aufgefordert.  Ihre Erweiterung wird in Ihrem Browser installiert, ähnlich wie erweiterungen, die aus dem Store installiert wurden.  

       :::image type="complex" source="./media/part1-installed-extension.png" alt-text="Seite "Installierte Erweiterungen" mit einer seitengeladenen Erweiterung":::
          Seite "Installierte Erweiterungen" mit einer seitengeladenen Erweiterung :::image-end:::

Während der Entwicklung müssen Sie möglicherweise auch die folgenden Aufgaben ausführen.
* Aktualisieren Sie die Erweiterung. Navigieren Sie zu `edge://extensions` , und wählen Sie dann Erneut laden **aus,** um Ihre Erweiterung zu aktualisieren.  
* Entfernen Sie die Erweiterung aus Ihrem Browser. Navigieren Sie `edge://extensions` zu , und wählen Sie dann die Erweiterung `Remove` aus.