---
description: Bieten Sie eine nahtlose Benutzeroberfläche für Websites, die Adobe Flash erfordern.
title: Dev-Leitfaden – Flash
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, Flash
ms.openlocfilehash: b3e2efe142142b7cdf233acfc4e915cd320b556d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566767"
---
# Blitz

Adobe Flash ist seit Jahrzehnten ein integraler Bestandteil des Webs und ermöglicht so Rich-Content-und-Animationen in Browsern seit der Einführung von HTML5. In modernen Browsern ermöglichen Webstandards, die von Microsoft, Adobe, Google, Apple, Mozilla und vielen anderen Pionieren entwickelt wurden, die Möglichkeit, diese Erfahrungen ohne Blitz und mit verbesserter Leistung und Sicherheit zu übertreffen. In partnerschaftlicher Zusammenarbeit mit anderen Browser Anbietern und Adobe empfehlen wir Entwicklern dringend, zu HTML5-Standards wie [verschlüsselte Medienerweiterungen](https://developer.microsoft.com/microsoft-edge/platform/status/encryptedmediaextensions), [Medien Quellen Erweiterungen](https://developer.microsoft.com/microsoft-edge/platform/status/mediasourceextensions), [Canvas](https://developer.microsoft.com/microsoft-edge/platform/status/canvas), [Web-Audio](https://developer.microsoft.com/microsoft-edge/platform/status/webaudioapi)und [Echtzeitkommunikation](https://developer.microsoft.com/microsoft-edge/platform/status/webrtcobjectrtcapi)zu migrieren.

Mit der OAT 2018-Version von Windows 10 setzt Microsoft Edge die Flash-Missbilligung fort, die wir im Rahmen der [Ankündigung von Adobes Ende des Supports](https://theblog.adobe.com/adobe-flash-update/) nach 2021 [abgedeckt](https://blogs.windows.com/msedgedev/2017/07/25/flash-on-windows-timeline/#9mCF959eQEK0poo5.97) haben. In der 2018-Version von Oct müssen die Benutzer ausdrücklich zulassen, dass Flash auf einer Website für die Lebensdauer der Registerkarte ausgeführt wird. Die Option dauerhafte immer zulassen steht nicht mehr zur Verfügung, und ein Benutzer kann keine Blitz Berechtigung pro Website verwalten, die sich auf die Tab-Sitzung erstreckt.

Beim Übergang zu HTML5-Standards gibt es einige einfache Schritte, mit denen Sie sicherstellen können, dass Ihre Benutzer beim Besuch Ihrer Website mit Microsoft Edge im Windows 10 Creators-Update weiterhin eine positive Erfahrung haben. 

Wenn Flash auf der Seite verwendet wird, der Benutzer ihn aber nicht aktiviert hat, zeigt Microsoft Edge in der Adressleiste normalerweise ein Puzzleteil Symbol an, wie es in [diesem Blog](https://blogs.windows.com/msedgedev/2016/12/14/edge-flash-click-run/#41svu6EMwKIAaigx.97)gezeigt wird. Wenn Sie das Flash-Steuerelement nach dem Laden der Seite dynamisch hinzufügen, wird möglicherweise das Symbol "Puzzle Piece" nicht angezeigt – in diesem Fall ist es am besten, das vorhanden sein von Flash zu testen und einen Link wie unten beschrieben bereitzustellen.

Um sicherzustellen, dass alle Benutzer eine gute Erfahrung haben, fahren Sie mit dem Testen auf das vorhanden sein von Flash mithilfe ihrer Standardmechanismen fort. Wenn Microsoft Edge meldet, dass Flash nicht zur Verfügung steht, präsentieren Sie den [Flash-Download-Link](http://get.adobe.com/flashplayer) und das Flash-Download- [Bild](http://www.adobe.com/legal/permissions/icons-web-logos.html#flashplayer) für den Benutzer. Wenn der Benutzer auf den Link klickt, präsentieren Microsoft Edge (sowie andere Browser) die erforderlichen Eingabeaufforderungen, um Flash Player für die Website zu aktivieren. Der Link muss in der primären Domäne angezeigt werden, in der Flash aktiviert werden soll. Es funktioniert nicht, wenn Sie Benutzer zu Seiten in anderen Domänen umleiten.  Im [folgenden finden Sie eine Demo](https://microsoftedge.github.io/MicrosoftEdge-Documentation/flashclicktorun/) der vorgeschlagenen Erfahrung und des entsprechenden [Beispielcodes](https://github.com/MicrosoftEdge/MicrosoftEdge-Documentation/tree/master/docs/flashclicktorun).
