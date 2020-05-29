---
ms.assetid: 8e2f75c4-fb7f-4892-a6c2-23bac081581a
description: Informieren Sie sich über die unternehmensspezifischen Aspekte von Microsoft Edge-Erweiterungen, und schauen Sie sich an, wie Sie mit UWP-apps vergleichbar sind.
title: Erweiterungen für Enterprise
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.custom: seodec18
ms.openlocfilehash: 8f50c282fce11d2654f990bf135941e0616af3f3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567454"
---
# Erweiterungen für Enterprise  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Microsoft Edge-Erweiterungen weisen einen ähnlichen Workflow auf, wenn Sie mit anderen Enterprise-UWP-apps verglichen werden. In den nachstehenden Informationen werden unternehmensspezifische Aspekte von Microsoft Edge-Erweiterungen erläutert.

## Voraussetzungen
Die folgenden Elemente werden vorgeschlagen, um eine Microsoft Edge-Erweiterung für Unternehmen zu entwickeln, zu verpacken und bereitzustellen:

+ Windows Developer Portal-Konto, um die Erweiterung für den Enterprise private Store zu signieren und freizugeben. Weitere Informationen finden Sie unter [Öffnen eines entwicklerkontos](/windows/uwp/publish/opening-a-developer-account) .
+ Microsoft Store for Business oder Education, um die Anwendung an das Unternehmen zu verteilen. Weitere Informationen finden Sie in der [Microsoft Store for Business-und Education-Dokumentation](/microsoft-store/) .
+ Ermitteln Sie, welche Versionen von Windows 10 die Microsoft Edge-Erweiterung ausführen werden. Eine Liste der vorhandenen Windows 10-Versionen finden Sie unter [Windows 10-Versionsinformationen](https://www.microsoft.com/itpro/windows-10/release-information) .

> [!NOTE]
> Sideloading kann als Alternative zur Verwendung des Windows-Entwickler Portals angesehen werden, um das Release the extension zu signieren. Weitere Informationen finden Sie im folgenden Verhalten von Sideloading-Erweiterungen.

## Windows Information Protection
Microsoft Edge-Erweiterungen berücksichtigen derzeit keine Windows Information Protection (WIP)-Einstellungen. Wenn ein Unternehmen sich um den Datenschutz sorgt, sollte die Unterstützung für Erweiterungen nicht für Microsoft Edge aktiviert sein.

Konfigurieren Sie die Gruppenrichtlinien-und Microsoft InTune-Einstellungen, um die Erweiterungen für Mitarbeiter zu deaktivieren. Weitere Informationen zu den zu konfigurierenden Richtlinien finden Sie unter [Verfügbare Richtlinien für Microsoft Edge](https://technet.microsoft.com/itpro/microsoft-edge/available-policies).

## Verpackungs Erweiterungen
Bevor ein Unternehmen eine Durchwahl an seine Mitarbeiter verteilen kann, muss es zuerst verpackt werden. Anleitungen zu Verpackungs Erweiterungen finden Sie im Leitfaden zur [Verpackung](./guides/packaging.md) .

> [!TIP]
> Testen Sie die Installation und Ausführung ihrer Erweiterung auf allen Versionen von Windows 10, um sicherzustellen, dass Sie wie erwartet funktioniert, bevor Sie verteilt werden.

## Verteilen von Erweiterungen
Nachdem eine Erweiterung gepackt wurde, kann Sie über den Microsoft Store, Microsoft Store for Business oder Sideloading an Mitarbeiter verteilt werden.

Erweiterungen, die zwar vom Microsoft Store für Unternehmen verteilt werden, aber entweder Mitarbeitern zugewiesen oder einem privaten Speicher hinzugefügt werden, in dem alle Mitarbeiter darauf zugreifen können. Dies kann mithilfe des Leitfadens ["Branchen-Apps für Unternehmen"](https://msdn.microsoft.com/windows/uwp/publish/distribute-lob-apps-to-enterprises) durchgeführt werden.

Für querladen-Erweiterungen müssen Geräte (nicht verwaltet oder verwaltet) für Sideloading freigegeben werden. Weitere Informationen dazu, wie Sie verpackte Erweiterungen querladen, finden Sie unter [querladen Branchen-apps in Windows 10](https://technet.microsoft.com/itpro/windows/deploy/sideload-apps-in-windows-10) .

> [!IMPORTANT]
> Wenn das Unternehmen die Erweiterung sowohl intern entwickelt als auch verteilt, benötigt das Unternehmen sowohl den Microsoft Store for Business (oder Education) als auch ein Windows Developer Portal-Konto.

### Verhalten von quer geladene-Erweiterungen
Im Gegensatz zu Erweiterungen, die über den Microsoft Store (oder den Microsoft Store für Unternehmen) verteilt sind, werden quer geladene-Erweiterungen in Microsoft Edge anders behandelt.

Der erste Unterschied wirkt sich auf die Verhaltensweise von quer geladene-Erweiterungen nach der Installation aus. Im Gegensatz zu Erweiterungen aus dem Microsoft Store zeigen quer geladene-Erweiterungen nicht sofort die Benachrichtigung "Sie haben eine neue Erweiterung" an und müssen vom Benutzer manuell aktiviert werden.

Um die Erweiterung zu aktivieren, öffnen Sie das Menü **mehr (.** ..), wählen Sie **"Erweiterungen"** aus, und sehen Sie sich die quer geladene-Erweiterung in der Liste der installierten Erweiterungen an. Klicken Sie auf die Erweiterung, und aktivieren Sie Sie.

Der zweite Unterschied wirkt sich darauf aus, wie quer geladene-Erweiterungen im Browser angezeigt werden. Beispielsweise enthalten sowohl die Benachrichtigung "Sie haben eine neue Durchwahl" als auch die Liste der installierten Erweiterungen eine zusätzliche Warnung, die besagt, dass die Erweiterung aus einer unbekannten Quelle stammt.

![querladen-Warnung 1](./media/sideload-permissionflyout.PNG)

![querladen-Warnung 2](./media/sideload-l1warning.PNG)

Der dritte und letzte Unterschied wirkt sich auf die Verhaltensweise von quer geladene-Erweiterungen beim Start des Browsers aus. Quer geladene-Erweiterungen auf Geräten, die entweder mit der Domäne verbunden sind oder MDM aktiviert sind, Verhalten sich wie Erweiterungen aus dem Microsoft Store. Quer geladene-Erweiterungen auf Geräten, die nicht mit der Domäne verbunden oder MDM aktiviert sind, werden jedoch während des Browser Starts deaktiviert und erfordern, dass der Benutzer explizite Aktionen durchführt.

Kurz nach dem Start des Browsers (nach ~ 10 Sekunden Inaktivität) wird die folgende Benachrichtigung am unteren Rand des Fensters angezeigt.

![querladen-Benachrichtigung](./media/sideload-scareUI.PNG)

Jedes Mal, wenn Microsoft Edge gestartet wird, müssen Benutzer "trotzdem aktivieren" auswählen, um die Erweiterung verwenden zu können.
