---
ms.assetid: 1b3ebc25-d023-4f23-bbba-dce066c20de8
description: Gehen Sie durch, wie bewährte Methoden und barrierefreie Rich-Internet-Anwendungen (Aria) zusammen kommen können, um eine barrierefreie Website zu erstellen.
title: Build | Zugänglichkeit
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/13/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Barrierefreiheit, Barrierefreiheit für Entwickler, barrierefreie Websites, Edge, Web-Entwicklung, Aria, Developer, UIA, UI-Automatisierung
ms.custom: seodec18
ms.openlocfilehash: 7a8ff5082132ec3270a6e01af594a5bd9fb35389
ms.sourcegitcommit: 5d3802721036dc7cd90e9e6f7ac90dc3acc24eec
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2020
ms.locfileid: "11191552"
---
# Erstellen von barrierefreien Websites
Das Web ist mit dynamischen und komplexen Websites, Anwendungen und Benutzeroberflächen gefüllt, die mit einer Kombination aus HTML, CSS und JavaScript erstellt wurden.  Wenn Sie jedoch ohne Barrierefreiheit entworfen und erstellt wurden, sind diese komplexen Websites nur schwer von Personen zu verwenden, die auf [Hilfstechnologien](https://webaim.org/articles/motor/assistive) zum Durchsuchen des Webs angewiesen sind. Das Erstellen von Websites, die für Menschen mit Behinderungen barrierefrei sind, erfordert semantische Informationen über die Benutzeroberfläche. Auf diese Weise können Hilfstechnologien wie Bildschirmsprachausgaben die erforderlichen Informationen vermitteln, um Personen mit einer Reihe von Fähigkeiten die Nutzung der Website zu ermöglichen.

Besuchen Sie [HTML5Accessibility](https://html5accessibility.com) , um Informationen darüber zu erhalten, welche neuen HTML5-Features von Microsoft Edge zugänglich unterstützt werden.

## Funktionsweise der Barrierefreiheit

Hilfstechnologien fügen Funktionen hinzu, die normalerweise von Computern nicht zur Verfügung stehen. Beispielsweise kann ein sehbehinderter Benutzer seine Tastatur in Kombination mit Hilfstechnologien wie einer Sprachausgabe verwenden, anstatt den Browser mit der Maus und dem Bildschirm direkt zu verwenden. Bei Anwendungen auf Microsoft-Plattformen und im Web interagiert die Hilfstechnologie mit der Microsoft- [Benutzeroberflächenautomatisierung](https://msdn.microsoft.com/library/windows/desktop/bb892135.aspx), einem anwendungsspezifischen Objektmodell wie dem Dokumentobjektmodell (DOM) in Microsoft Edge oder einer Kombination dieser Technologien.

Für Webentwickler werden bestimmte HTML-Elemente UI-Automatisierung-Objekten zugeordnet, sodass der Entwickler bei der Auswahl dieser HTML-Elemente die Barrierefreiheitseigenschaften und Ereignisse verwenden kann, die in diesen Elementen integriert sind. Bei der Entwicklung Ihrer Website müssen Sie in der Regel nur darauf achten, dass die API richtig geschrieben wird (oder das entsprechende Element angegeben ist), damit die Anwendung barrierefrei ist. Weitere Informationen finden Sie [unter Aria und UI-Automatisierung in Microsoft Edge](./build/ARIA-and-UI-Automation.md) .  Informationen zu barrierefreien Apps für die universelle Windows-Plattform (UWP) finden Sie im Thema [Barrierefreiheit](https://msdn.microsoft.com/windows/uwp/accessibility/accessibility) im Windows dev Center.

Viele häufige Barrierefreiheitsprobleme mit dynamischem Inhalt können durch eine gute Codierungspraxis behoben werden, und die [WCAG 2,0](https://go.microsoft.com/fwlink/p/?LinkID=24629) -Dokumentation umfasst zahlreiche Techniken und bewährte Methoden, mit denen Sie barrierefreiere dynamische Webanwendungen erstellen können. Auch wenn Sie ordnungsgemäß codiert sind, ist es nicht unbedingt möglich, dynamischen Inhalt zu erreichen. [Barrierefreie Rich-Internet-Anwendungen (Aria)](#aria) helfen, dieses Problem zu lösen.  

Weitere Informationen zur Barrierefreiheit im Web finden Sie [in der Einführung in die Barrierefreiheit](https://www.w3.org/WAI/intro/accessibility.php) des Webs durch die [Web Accessibility Initiative](https://www.w3.org/WAI/) (WAI).

## Aria
Die Aria-Spezifikation ( [barrierefreie Rich-Internet-Anwendungen](https://www.w3.org/TR/wai-aria/) ) der W3C [Web Accessibility-Initiative](https://www.w3.org/WAI/) definiert eine Syntax für die Erstellung von dynamischen Webinhalten und benutzerdefinierten Benutzeroberflächen, die für alle Personen zugänglich sind. Aria erweitert HTML mithilfe zusätzlicher Attribute (Rollen, Eigenschaften und Zustände), die für die Übertragung benutzerdefinierter Semantik entwickelt wurden. Diese Attribute werden von Browsern verwendet, um den Zustand und die Rolle des Steuerelements an die Barrierefreiheits-API weiterzugeben.

### Rollen, Eigenschaften und Zustände
Aria-Rollen werden für Elemente mit dem [`role`](https://msdn.microsoft.com/library/cc304102(v=vs.85).aspx) Attribut gesetzt, um Hilfstechnologien und Barrierefreiheits-APIs Informationen zu dem Element zu geben. So wird beispielsweise das untere `<li>` Element zugewiesen `role="menuitem"` , um zu signalisieren, dass es sich um ein Element in einem Menü handelt.

``` html
<li role="menuitem">Home</li>
```

Aria-Zustände und-Eigenschaften sind Aria-Präfix Attribute, die bestimmte Informationen zu einem Objekt bereitstellen, um die Definition der Art von Rollen zu unterstützen. Eigenschaften sind Attribute, die für die Art eines Objekts wichtig sind, wie [`aria-readonly`](https://msdn.microsoft.com/library/cc304089(v=vs.85).aspx) und [`aria-haspopup`](https://msdn.microsoft.com/library/cc304081(v=vs.85).aspx) . Das Ändern einer Eigenschaft wirkt sich auf die Bedeutung des Objekts aus. Im folgenden Beispiel wird die Eigenschaft `aria-haspopup="true"` für ein `<li>` Menüelement auf ein Popup Symbol gesetzt.

``` html
<li role="menuitem" aria-haspopup="true">Open</li>
```

Zustände ändern nicht die Art des Objekts, sondern stellen Informationen dar, die dem Objekt oder der Interaktion des Benutzers mit dem Objekt zugeordnet sind, wie [`aria-hidden`](https://msdn.microsoft.com/library/cc304083(v=vs.85).aspx) oder [`aria-checked`](https://msdn.microsoft.com/library/cc304075(v=vs.85).aspx) . Der Zustand `aria-checked="false"` im folgenden Beispiel zeigt beispielsweise, dass das Kontrollkästchen nicht aktiviert ist.

``` html
<div role="checkbox" aria-checked="false">Accept</div>
```

Wechseln Sie zum [Rollenmodell](https://www.w3.org/TR/wai-aria-1.1/#roles) des W3C, um eine vollständige Liste der Rollen, Eigenschaften und Zustände anzuzeigen.

Weitere Informationen zu Aria finden Sie in der Aria im Abschnitt [Resources](#resources) .

## Kompatibilitätstests für Hilfstechnologien  

Überprüfen, ob die Website, die Sie erstellen, mit echten Hilfstechnologien arbeitet, ist die beste Methode, um für Benutzer mit Behinderungen eine gute Benutzerfreundlichkeit zu gewährleisten.  Da viele Hilfstechnologien die Tastatur verwenden, ist das Testen der Barrierefreiheit Ihrer Website ein guter Ausgangspunkt.  Das [Testen der Tastatur Kompatibilität][W3cPerspectiveVideosKeyboard] überprüft, ob Benutzer auf alle interaktiven Steuerelemente zugreifen können, ohne dass eine Maus erforderlich ist.  Microsoft [Accessibility Insights für Web][AccessibilityinsightsWebOverview] ist eine Browser Erweiterung für Microsoft Edge und Chrome, die Sie führt und einige häufige Probleme aufdeckt.  

Wenn Sie sicher sind, dass Ihre Website gut mit einer Tastatur funktioniert, versuchen Sie es mit anderen Hilfstechnologien wie Bildschirmsprachausgaben.  Im folgenden werden Probleme aufgedeckt.

*   Ihr HTML-, Aria-und CSS-Code  
*   Die Stufe der Unterstützung einer Hilfstechnologie für ein Feature oder eine Technik.  
    
Unterschiedliche Browser können Elemente Platt Form Barrierefreiheits-APIs anders als Microsoft Edge zuordnen.  Beim Erstellen der Benutzeroberfläche ist es wichtig, die einzelnen Unterschiede zu beachten.  

WebAIM führt Umfragen mit [Sprachausgabe][WebaimProjectsScreenreadersurvey8] und [sehbehinderten][WebaimProjectsLowvisionsurvey2] Benutzern durch, die Ihnen bei der Entscheidung helfen, welche Hilfstechnologien und Browser Sie testen möchten.  

### Lernen, wie man testet  

Hilfstechnologien sind ausgeklügelte Tools.  Gehen Sie nicht davon aus, dass Sie in der Lage sind, sofort mit einer Hilfstechnologie zu testen, ohne zuvor zu erfahren, wie das funktioniert.  Das Lernen mit einer Sprachausgabe zu testen, hat eine besonders steile Lernkurve.  Ein unerfahrener Benutzer der Bildschirmsprachausgabe kann davon ausgehen, dass ein Fehler bei der Bildschirmsprachausgabe aufgetreten ist, während das Problem mit dem Missbrauch der Sprachausgabe zusammenhängt.  

Weitere Informationen zum Lernen, wie Sie mit Hilfstechnologien testen können, finden Sie unter [Testen mit Bildschirmsprachausgaben][WebaimArticlesScreenreaderTesting] auf WebAIM.  

### Lokales Testen  

Die meisten Geräte umfassen Hilfstechnologien, die für das Betriebssystem integriert sind.  Microsoft Windows umfasst die [Windows-Sprachausgabe][MicrosoftSupport22798] und die [Windows][MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198]-Bildschirmlupe.  Hilfstechnologien von Drittanbietern wie [NVDA][NvaccessAboutNvda], [FreedomscientificSoftwareJaws]und [ZoomText][FreedomscientificSoftwareZoomtext] stehen zum Download zur Verfügung.  Apple macOS enthält die [VoiceOver][AppleAccessibilityMacVision] -Sprachausgabe.  Und IOS, Android und Linux unterstützen alle eine Vielzahl von Hilfstechnologien.  

### Testen in virtuellen Computern und Emulatoren  

Wenn Sie unter macOS mit einer Hilfstechnologie testen möchten, die nur für Windows verfügbar ist, wie Windows-Sprachausgabe oder NVDA, erstellen Sie einen virtuellen Windows-Computer.  Virtuelle Computer mit Microsoft Edge \ (EdgeHTML \) und IE sind für virtualbox und VMware auf der [Download Seite für virtuelle Computer][MicrosoftDeveloperEdgeVms]verfügbar.  

[Android Studio][AndroidDeveloperSdkInstallingStudioHtml] enthält einen Emulator, mit dem Sie Hilfstechnologien in der [Android-Barrierefreiheits Suite][GooglePlayStoreAndroidAccessibilitySuite]testen können.  Befolgen Sie die Anweisungen zum [Einrichten eines virtuellen Geräts][AndroidDeveloperDevicesManagingAvdsHtml] , und [Starten Sie den Emulator][AndroidDeveloperDevicesEmulatorHtml], und installieren Sie dann die [Android-Barrierefreiheits Suite][GooglePlayStoreAndroidAccessibilitySuite] aus dem GooglePlay-Store.  

> [!NOTE]
> Der IOS-Simulator enthält derzeit keine VoiceOver-Funktion.  

### Cloud-basierte Test Tools  

Wenn keine Hilfstechnologien für Ihr Betriebssystem verfügbar sind oder wenn Sie eine auf einem virtuellen Computer oder Emulator nicht installieren können, sind Cloud-basierte Hilfstechnologie-Testtools die beste Wahl.  

*   Mit [Assistiv Labs (Commercial)][AssistivlabsMain] können Sie mit Hilfstechnologien manuell über einen beliebigen modernen Webbrowser testen.  Wählen Sie eine Hilfstechnologie und einen Browser aus, die Sie mit einem virtuellen Computer, Emulator oder realen Gerät verbindet, mit dem Sie interagieren können.  

## Ressourcen

### Grundlagen der Barrierefreiheit
#### [Das A11Y-Projekt](http://a11yproject.com/)
Das A11Y-Projekt ist eine Community-gesteuerte Anstrengung, um die Barrierefreiheit im Web zu vereinfachen. Schauen Sie sich [die A11Y-Projekt](https://a11yproject.com/) Website an, um mehr über grundlegende Barrierefreiheits Prinzipien, deren Barrierefreies Muster und die Widget- [Bibliothek](https://a11yproject.com/patterns)sowie deren [Ressourcen](http://a11yproject.com/resources.html) zu Barrierefreiheits Software, Blogs, Büchern und Tools zu erfahren.

#### [Web Accessibility Initiative (WAI)](https://w3.org/WAI/)
Die W3C Web Accessibility Initiative (WAI) stellt eine Bemühung dar, die Barrierefreiheit im Internet zu verbessern. Ihre Website bietet eine Reihe von Ressourcen für den Einstieg [in die Barrierefreiheit im Web](https://www.w3.org/WAI/gettingstarted/Overview.html), das [Entwerfen für Inklusion](https://www.w3.org/WAI/users/Overview.html), [Lernprogramme und Präsentationen](https://www.w3.org/WAI/train.html)und vieles mehr.

### Barrierefreiheits-Blogs
#### [Die der Paciello-Gruppe](https://www.paciellogroup.com/blog/)
Die der Paciello-Gruppe bietet Beratungs-und Technologielösungen für Organisationen in der ganzen Welt, um sicherzustellen, dass Ihre Kunden effektiv und effizient alle Zielgruppen erreichen, während Sie behördliche und internationale Standards erfüllen. Ihr Blog umfasst Themen wie bewährte Methoden für Web-Barrierefreiheit, Barrierefreiheits Tools und Trends für Barrierefreiheit.

#### [Einfach zugänglich](http://simplyaccessible.com/articles/)
Einfach barrierefrei ist ein Team von Spezialisten für Barrierefreiheit, das Barrierefreiheit, Beratung und mehr bietet, um die Wahrnehmung von Barrierefreiheit im Internet zu ändern. Im Abschnitt " [Artikel](http://simplyaccessible.com/articles/) " werden bewährte Methoden für Barrierefreiheit, Barrierefreies Design und vieles mehr erläutert.

#### [SSB Bart Group (SSB)](http://www.ssbbartgroup.com/blog/)
SSB Bart Group ist eine digitale Bedienungshilfe Firma, die Ihre Kunden bei der Entwicklung und Bereitstellung von barrierefreien Produkten und Diensten unterstützt. Ihr Blog behandelt Themen wie Aria-bewährte Methoden, Trends für Barrierefreiheit, Webinars und vieles mehr.

### Barrierefreie Beispiele
#### [ally.js-Lernprogramme](http://allyjs.io/tutorials/)
JavaScript-Bibliothek, um moderne Webanwendungen mit Barrierefreiheits Problemen zu unterstützen, indem die Barrierefreiheit vereinfacht wird.

#### [Heydonworks-Aria-Beispiele](http://heydonworks.com/practical_aria_examples/)
Praktische Aria-Beispiele zum Verbessern der Barrierefreiheit Ihrer Anwendung

#### [OpenAjax-Beispiele](http://oaa-accessibility.org/)
Die OpenAjax Alliance-Website ist eine hervorragende Ressource zur Überprüfung der Regeln für WAI-ARIA und bietet eine Reihe von Beispielen für WAI-ARIA-Implementierungen.

#### [Muster](http://a11yproject.com/patterns.html)
[Das A11Y-Projekt](http://a11yproject.com/) bietet eine Bibliothek mit barrierefreien Widgets und Mustern wie Menüs, Schaltflächen, QuickInfos und vieles mehr.

### Barrierefreiheits Techniken & Tools
#### [Barrierefreiheit: Erstellen barrierefreier Erweiterungssymbole für Microsoft Edge](../extensions/guides/accessibility.md)
Hier finden Sie Anleitungen zum Erstellen von Symbolen für barrierefreie Erweiterungen für Microsoft Edge.

#### [Barrierefreier Name und Beschreibung: Berechnungen und Zuordnungen 1,1](https://www.w3.org/TR/accname-1.1/)
In diesem W3C-Zuordnungsdokument wird erläutert, wie Browsernamen und Beschreibungen von barrierefreien Objekten aus Webinhalts Sprachen ermitteln und diese in Barrierefreiheits-APIs verfügbar machen.

#### [Ressourcen zur Auswertung der Barrierefreiheit](https://www.w3.org/WAI/eval/Overview.html)
Barrierefreiheits Auswertungs Ressourcen ist eine mehrseitige Ressource des W3C, in der verschiedene Ansätze für die Auswertung von Websites für Barrierefreiheit erläutert werden.

#### [Kompatibilitätstests für Hilfstechnologien](http://www.powermapper.com/tests/)
Test Ergebnisse, die zeigen, wie sich unterschiedliche Inhaltstypen und Standards in Hilfstechnologien (at) wie Bildschirmsprachausgaben Verhalten.

#### [Das Erstellen barrierefreier Websites ist jetzt noch einfacher geworden](https://blogs.msdn.microsoft.com/webdev/2016/05/02/building-accessible-websites-just-got-a-lot-easier/)
Dieser .net Web Development-und Tools-Blogbeitrag beschreibt die Visual Studio Extension [Web-barrierefreiheitsprüfung](https://go.microsoft.com/fwlink/p/?linkid=841539).

#### [Zentrale Barrierefreiheits-API-Zuordnungen 1,1](https://www.w3.org/TR/core-aam-1.1/)
In diesem W3C-Zuordnungsdokument wird erläutert, wie die Semantik von Webinhalts Sprachen für Barrierefreiheits-APIs verfügbar gemacht wird.  

#### [Einfache Überprüfungen – eine erste Überprüfung der Barrierefreiheit im Web](https://www.w3.org/WAI/eval/preliminary.html)
Eine Reihe von schnellen Überprüfungen durch Wai, die Ihnen helfen, die Barrierefreiheit einer Webseite zu beurteilen.

#### [So treffen Sie die WCAG 2,0](https://www.w3.org/WAI/WCAG20/quickref/)
Eine Kurzübersicht über Web Content Accessibility Guidelines (WCAG) 2,0-Anforderungen (Erfolgskriterien) und Techniken.

#### [HTML-Barrierefreiheits-API-Zuordnungen 1,0](https://www.w3.org/TR/html-aam-1.0/)
In diesem W3C-Zuordnungsdokument wird erläutert, wie HTML 5.1-Elemente und-Attribute den Platt Form Barrierefreiheits-APIs zugeordnet werden.


#### [Schnelle Tipps](http://a11yproject.com/#Quick-tips)
Eine Liste mit Tipps zur schnellen Webentwicklung für Barrierefreiheit [im A11Y-Projekt](http://a11yproject.com/).

#### [Website Überprüfung](https://developer.microsoft.com/microsoft-edge/tools/staticscan/)
Das Tool "Website Überprüfung" im Microsoft Edge dev Center sucht nach veralteten Bibliotheken, Layout-Problemen und Barrierefreiheits Problemen.

#### [Techniken für WCAG 2,0](https://www.w3.org/TR/WCAG20-TECHS/Overview.html)
Techniken des W3C, die Anleitungen für Web-Entwickler zur Erfüllung von [Richtlinien für die Barrierefreiheit von Webinhalten (WCAG) 2,0](https://w3.org/TR/WCAG20/) bieten.

#### [Tipps zur Entwicklung für Barrierefreiheit im Web](https://w3.org/WAI/gettingstarted/tips/developing.html)
Tipps vom W3C zur Entwicklung von Webinhalten, die für Menschen mit Behinderungen barrierefreier sind.

#### [WAI-ARIA Authoring Practices 1,1](http://w3c.github.io/aria-practices/)
Ein Dokument des W3C, in dem die Leser wissen, wie Sie WAI-ARIA 1,1 verwenden können, und empfiehlt Ansätze, Widgets, Navigation und Verhaltensweisen mithilfe von WAI-ARIA-Rollen,-Zuständen und-Eigenschaften barrierefrei zu gestalten.

#### [Wai-Richtlinien und-Techniken](https://w3.org/WAI/guid-tech.html)
Eine Reihe von Richtlinien und Standards zur Barrierefreiheit im Web, die von Wai entwickelt wurden.  

#### [Liste der Evaluierungs Tools für Web-Barrierefreiheit](https://www.w3.org/WAI/ER/tools/index.html)
Eine Liste der Tools zur Bewertung der Barrierefreiheit im Web, um festzustellen, ob Websites den Richtlinien für Barrierefreiheit entsprechen.

#### [Barrierefreie Web-Perspektiven: untersuchen Sie die Auswirkungen und Vorteile für alle](https://w3.org/WAI/perspectives/)
Eine Reihe von kurzen situations Videos des W3C über die Auswirkungen der Barrierefreiheit und die Vorteile für alle.

<!-- links -->  

<!--todo: link updates and acrolinx  -->  

[MicrosoftDeveloperEdgeVms]: https://developer.microsoft.com/microsoft-edge/tools/vms "Virtuelle Computer | Microsoft Edge-Entwickler"  

[MicrosoftSupport22798]: https://support.microsoft.com/help/22798 "Vollständige Anleitung für die Sprachausgabe | Microsoft-Support"  
[MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198]: https://support.microsoft.com/windows/414948ba-8b1c-d3bd-8615-0e5e32204198 "Verwenden der Bildschirmlupe, um die Anzeige der Dinge auf dem Bildschirm zu verbessern | Microsoft-Support"  

[AccessibilityinsightsWebOverview]: https://accessibilityinsights.io/docs/web/overview "Barrierefreiheit für Web | Einblicke in die Barrierefreiheit"  

[AndroidDeveloperDevicesManagingAvdsHtml]: https://developer.android.com/tools/devices/managing-avds.html "Erstellen und Verwalten von virtuellen Geräten | Android-Entwickler"  
[AndroidDeveloperDevicesEmulatorHtml]: https://developer.android.com/tools/devices/emulator.html "Ausführen von apps auf dem Android-Emulator | Android-Entwickler"  
[AndroidDeveloperSdkInstallingStudioHtml]: https://developer.android.com/sdk/installing/studio.html "Android Studio herunterladen | Android-Entwickler"  

[AppleAccessibilityMacVision]: https://www.apple.com/accessibility/mac/vision "Barrierefreiheit von Visionen-Mac | Apple"  

[AssistivlabsMain]: https://assistivlabs.com "Assistiv Labs"  

[FreedomscientificSoftwareJaws]: https://www.freedomscientific.com/products/software/jaws "Jaws® | Freiheit wissenschaftlich"  
[FreedomscientificSoftwareZoomtext]: https://www.freedomscientific.com/products/software/zoomtext "ZoomText | Freiheit wissenschaftlich"  

[GooglePlayStoreAndroidAccessibilitySuite]: https://play.google.com/store/apps/details?id=com.google.android.marvin.talkback "Android-Suite für Barrierefreiheit | GooglePlay-Store"  

[NvaccessAboutNvda]: https://www.nvaccess.org/about-nvda "Informationen zu NVDA | NV-Zugriff"  

[W3cPerspectiveVideosKeyboard]: https://www.w3.org/WAI/perspective-videos/keyboard "Tastatur Kompatibilität | W3C"  

[WebaimProjectsLowvisionsurvey2]: https://webaim.org/projects/lowvisionsurvey2 "Umfrage von Benutzern mit Sehbehinderungen \ #2 Ergebnisse | WebAIM"  
[WebaimProjectsScreenreadersurvey8]: https://webaim.org/projects/screenreadersurvey8 "Benutzerumfrage zur Sprachausgabe \ #8 Ergebnisse | WebAIM"  
[WebaimArticlesScreenreaderTesting]: https://webaim.org/articles/screenreader_testing "Testen mit Bildschirmsprachausgaben | WebAIM"  
