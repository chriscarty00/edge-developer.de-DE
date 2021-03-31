---
description: Testen Sie Ihre Erweiterung, indem Sie Sie im Browser Sideloading
title: Querladen ihrer Durchwahl
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, Erweiterungen
ms.openlocfilehash: 7070878b9608e6d239179078390f2315e0b289a1
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104773"
---
# Querladen einer Erweiterung

Während der Entwicklung können Sie den Microsoft Edge \(Chrom \)-Browser verwenden, um Ihre Erweiterung sicher auszuführen und zu debuggen. Indem Sie Ihre Erweiterung lokal in Ihrem Browser Sideloading, können Sie Ihre Erweiterung ausführen und testen. In diesem Artikel wird erläutert, wie Sie Erweiterungen in Microsoft Edge querladen.

Führen Sie die folgenden Schritte aus, um die Erweiterung zu querladen.

1.  Öffnen `edge://extensions` Sie die Seite, indem Sie die drei Punkte oben im Browser auswählen und dann **Erweiterungen**auswählen.

       :::image type="complex" source="./media/part1-threedots.png" alt-text="Öffnen der Seite &quot;Edge://Extensions&quot;":::
          Öffnen der Seite &quot;Edge://Extensions" :::image-end:::

1.  Aktivieren Sie auf der Seite Erweiterungsverwaltung unter `edge://extensions` den **Entwicklermodus** mithilfe der Umschaltfläche unten links auf der Seite.

       :::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Öffnen der Seite &quot;Edge://Extensions&quot;":::
          Öffnen der Seite &quot;Edge://Extensions":::
          Aktivieren des Entwicklermodus :::image-end:::

1.  Wenn Sie Ihre Erweiterung zum ersten Mal installieren, wählen Sie **Laden entpackt**aus.  Sie werden aufgefordert, das Verzeichnis mit den Quelldateien für die Erweiterung einzugeben.  Ihre Erweiterung wird in Ihrem Browser installiert, ähnlich wie im Store installierte Erweiterungen.  

       :::image type="complex" source="./media/part1-installed-extension.png" alt-text="Öffnen der Seite &quot;Edge://Extensions&quot;":::
          Öffnen der Seite &quot;Edge://Extensions" mit einer quer geladene-Erweiterung :::image-end:::

Während der Entwicklung müssen Sie möglicherweise auch die folgenden Aufgaben ausführen.
* Aktualisieren Sie die Erweiterung. Navigieren `edge://extensions` Sie zu, und wählen Sie dann **Reload** aus, um Ihre Erweiterung zu aktualisieren.  
* Entfernen Sie die Erweiterung aus Ihrem Browser. Navigieren Sie zu `edge://extensions` , und wählen Sie dann `Remove` Ihre Erweiterung aus.
