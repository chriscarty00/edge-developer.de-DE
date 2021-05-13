---
ms.assetid: 1b3ebc25-d023-4f23-bbba-dce066c20de8
description: Erfahren Sie, wie bewährte Methoden und ARIA (Accessible Rich Internet Applications) zusammenkommen können, um eine barrierefreie Website zu erstellen.
title: Erstellen | Barrierefreiheit
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Barrierefreiheit, Barrierefreiheit für Entwickler, barrierefreie Websites, Edge, Webentwicklung, ARIA, Entwickler, UIA, Benutzeroberflächenautomatisierung
ms.custom: seodec18
ms.openlocfilehash: 99f0eb9d96bc6d53df72839c6c2f1e61cbd5494e
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564021"
---
# <a name="building-accessible-websites"></a>Erstellen barrierefreier Websites  

Das Web ist mit dynamischen und komplexen Websites, Anwendungen und Benutzeroberflächen gefüllt, die mithilfe einer Kombination aus HTML, CSS und JavaScript erstellt wurden.  Wenn diese komplexen Websites jedoch ohne Barrierefreiheit entworfen und erstellt werden, ist die Verwendung dieser komplexen Websites für Personen, die auf Hilfstechnologien zum Durchsuchen des Webs angewiesen sind, schwierig. [](https://webaim.org/articles/motor/assistive)  Das Erstellen von Websites, auf die für Personen mit Behinderungen zugegriffen werden kann, erfordert semantische Informationen über die Benutzeroberfläche.  Auf diese Weise können Hilfstechnologien, wie z. B. Bildschirmlesegeräte, die erforderlichen Informationen vermitteln, um Personen mit einer Reihe von Fähigkeiten bei der Verwendung der Website zu helfen.  

Unter [HTML5Accessibility](https://html5accessibility.com) finden Sie Informationen dazu, welche neuen HTML5-Features von der Website Microsoft Edge.  

## <a name="how-accessibility-works"></a>Funktionsweise der Barrierefreiheit  

Hilfstechnologien fügen Funktionen hinzu, die Computer normalerweise nicht haben.  Beispielsweise kann ein sehbehinderter Benutzer seine Tastatur in Kombination mit Hilfstechnologie wie z. B. einer Bildschirmlesefunktion verwenden, anstatt den Browser direkt mit der Maus und dem Bildschirm zu verwenden.  Für Anwendungen auf Microsoft-Plattformen und im Web interagiert die Hilfstechnologie mit der Microsoft [UI Automation,](/windows/win32/winauto/uiauto-specandcommunitypromise)einem anwendungsspezifischen Objektmodell wie dem Dokumentobjektmodell \(DOM\) in Microsoft Edge oder einer Kombination aus diesen.  

Für Webentwickler werden bestimmte HTML-Elemente Benutzeroberflächenautomatisierungsobjekten zugeordnet, sodass der Entwickler bei der Auswahl dieser HTML-Elemente die in diese Elemente integrierten Barrierefreiheitseigenschaften und -ereignisse verwenden kann.  Beim Entwickeln Ihrer Website müssen Sie in der Regel nur sicherstellen, dass die API ordnungsgemäß in \(oder das entsprechende Element angegeben ist\) geschrieben wird, damit auf die Anwendung zugegriffen werden kann.  Weitere Informationen [finden Sie unter ARIA and UI Automation in Microsoft Edge.](./aria-and-ui-automation.md)  Informationen zu barrierefreien Apps der universellen Windows-Plattform \(UWP\) finden Sie im Thema Barrierefreiheit im Windows Dev Center. [](/windows/uwp/design/accessibility/accessibility)  

Viele häufige Barrierefreiheitsprobleme mit dynamischen Inhalten können durch eine bewährte Codierungspraxis behoben werden, und die [WCAG 2.0-Dokumentation](https://www.w3.org/TR/WCAG20) enthält viele Techniken und bewährte Methoden, mit deren Hilfe Sie barrierefreiere dynamische Webanwendungen erstellen können.  Auch wenn sie ordnungsgemäß codiert sind, ist der Zugriff auf dynamische Inhalte jedoch nicht unbedingt möglich.  [Barrierefreie Rich Internet Applications (ARIA) hilft](#aria) bei der Bewältigung dieses Problems.  

Weitere Informationen zur Webbarrierefreiheit finden Sie in der [Einführung in web accessibility](https://www.w3.org/WAI/intro/accessibility.php) by the Web Accessibility Initiative [(WAI).](https://www.w3.org/WAI)  

## <a name="aria"></a>ARIA  

Die [ARIA(Accessible Rich Internet Applications)-Spezifikation](https://www.w3.org/TR/wai-aria) der Web [Accessibility Initiative](https://www.w3.org/WAI) von W3C definiert als Syntax, um dynamische Webinhalte und benutzerdefinierte Benutzeroberflächen für alle Benutzer zugänglich zu machen.  ARIA erweitert HTML mithilfe zusätzlicher Attribute \(Rollen, Eigenschaften und Zustände\), die benutzerdefinierte Semantik vermitteln sollen.  Diese Attribute werden von Browsern verwendet, um den Zustand und die Rolle der Steuerelemente an die Barrierefreiheits-API weiter zu übergeben.  

### <a name="roles-properties-and-states"></a>Rollen, Eigenschaften und Zustände  

ARIA-Rollen werden für Elemente festgelegt, die das [Role-Attribut](https://developer.mozilla.org/docs/Web/HTML/Reference) verwenden, um Hilfstechnologien und Barrierefreiheits-APIs Informationen über das Element zu geben.  Das folgende Element wird beispielsweise zugewiesen, um zu signalisieren, dass es sich um ein `<li>` Element in einem Menü `role="menuitem"` handelt.  

```html
<li role="menuitem">Home</li>
```  

ARIA-Zustände und -Eigenschaften sind Arienpräfixattribute, die spezifische Informationen zu einem Objekt bereitstellen, um die Definition der Art von Rollen zu bilden.  Eigenschaften sind Attribute, die für die Art eines Objekts unerlässlich sind, z. B. [ari-readonly](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) und [aria-haspopup](https://developer.mozilla.org/docs/Web/Accessibility/ARIA).  Das Ändern einer Eigenschaft wirkt sich auf die Bedeutung des Objekts aus.  Im folgenden Beispiel wird die Eigenschaft für ein Menüelement festgelegt, um anzuzeigen, `aria-haspopup="true"` dass sie über ein Popup `<li>` verfügt.  

```html
<li role="menuitem" aria-haspopup="true">Open</li>
```  

Zustände ändern nicht die Art des Objekts, sondern stellen Informationen dar, die mit dem Objekt oder der Benutzerinteraktion mit dem Objekt verknüpft sind, z. B. [ariengebte](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) oder [ariengecheckte](https://developer.mozilla.org/docs/Web/Accessibility/ARIA).  Der Status im folgenden Beispiel stellt z. B. dar, dass `aria-checked="false"` das Kontrollkästchen nicht aktiviert ist.  

```html
<div role="checkbox" aria-checked="false">Accept</div>
```  

Wechseln Sie [zum Rollenmodell](https://www.w3.org/TR/wai-aria-1.1#roles) des W3C, um eine vollständige Liste der Rollen, Eigenschaften und Zustände zu sehen.  

Weitere Informationen zu ARIA finden Sie unter ARIA im Abschnitt [Ressourcen.](#resources)  

## <a name="assistive-technology-compatibility-testing"></a>Kompatibilitätstests für Hilfstechnologien  

Die Überprüfung, ob die website, die Sie erstellen, mit echten Hilfstechnologien funktioniert, ist die beste Möglichkeit, um eine gute Erfahrung für Ihre Benutzer mit Behinderungen zu gewährleisten.  Da viele Hilfstechnologien die Tastatur nutzen, ist das Testen der Barrierefreiheit ihrer Website ein guter Einstiegsort.  [Tastaturkompatibilitätstests][W3cPerspectiveVideosKeyboard] überprüfen, ob Benutzer zugriff auf alle interaktiven Steuerelemente haben, ohne dass eine Maus erforderlich ist.  Microsoft [Accessibility Insights for Web][AccessibilityinsightsWebOverview] ist eine Browsererweiterung für Microsoft Edge Und Chrome, die Sie führt und mehrere häufige Probleme auft.  

Sobald Sie sicher sind, dass Ihre Website gut mit einer Tastatur funktioniert, versuchen Sie es mit anderen Hilfstechnologien, z. B. Bildschirmlesegeräten.  Es werden Probleme in den folgenden Themen aufgedeckt.  

*   Ihre HTML, ARIA und CSS.  
*   Die Unterstützungsebene einer Hilfstechnologie für ein Feature oder eine Technik.  
    
Verschiedene Browser ordnen Elemente plattformbarrierefreien APIs möglicherweise anders zu als Microsoft Edge.  Beim Erstellen Der Benutzeroberfläche ist es wichtig, jeden Unterschied zu berücksichtigen.  

WebAIM führt Umfragen mit [][WebaimProjectsLowvisionsurvey2] Bildschirmleser und Benutzern mit niedriger Sehkraft durch, die Ihnen bei der Entscheidung helfen, welche Hilfstechnologien und Browser Sie testen möchten. [][WebaimProjectsScreenreadersurvey8]  

### <a name="learning-how-to-test"></a>Learning How to Test  

Hilfstechnologien sind ausgefeilte Tools.  Gehen Sie nicht davon aus, dass Sie sofort mit dem Testen mit einer Hilfstechnologie beginnen können, ohne zunächst zu erfahren, wie sie funktioniert.  Das Testen mit einer Bildschirmleseausgabe hat eine besonders starke Lernkurve.  Ein benutzerfreundlicher Bildschirmlesebenutzer kann davon ausgehen, dass ein Bildschirmlesefehler aufgetreten ist, während das Problem im Zusammenhang mit dem Missbrauch der Bildschirmleseausgabe steht.  

Weitere Informationen zum Testen mit Hilfstechnologien finden Sie unter [Testen mit Bildschirmlesegeräten][WebaimArticlesScreenreaderTesting] auf WebAIM.  

### <a name="testing-locally"></a>Lokal testen  

Die meisten Geräte enthalten Hilfstechnologie, die in das Betriebssystem integrierte Ist.  Microsoft Windows enthält die [Windows Sprachausgabe][MicrosoftSupport22798] und [Windows Bildschirmlupe][MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198].  Hilfstechnologien von Drittanbietern wie [NVDA,][NvaccessAboutNvda] [FreedomscientificSoftwareJaws]und [ZoomText][FreedomscientificSoftwareZoomtext] stehen zum Herunterladen zur Verfügung.  Apple macOS enthält die [VoiceOver-Sprachausgabe.][AppleAccessibilityMacVision]  Und iOS, Android und Linux unterstützen eine Vielzahl von Hilfstechnologien.  

### <a name="testing-in-virtual-machines-and-emulators"></a>Testen in virtuellen Computern und Emulatoren  

Wenn Sie unter macOS mit einer Hilfstechnologie testen möchten, die nur für Windows verfügbar ist, z. B. Windows Sprachausgabe oder NVDA, erstellen Sie einen Windows virtuellen Computer.  Virtuelle Computer mit Microsoft Edge \(EdgeHTML\) und IE sind für VirtualBox und VMWare auf der Downloadseite für virtuelle [Computer verfügbar.][MicrosoftDeveloperEdgeVms]  

[Android Studio][AndroidDeveloperSdkInstallingStudioHtml] enthält einen Emulator, mit dem Sie Hilfstechnologien in der [Android Accessibility Suite testen können.][GooglePlayStoreAndroidAccessibilitySuite]  Befolgen Sie die Anweisungen [zum Einrichten eines][AndroidDeveloperDevicesManagingAvdsHtml] virtuellen Geräts und [starten][AndroidDeveloperDevicesEmulatorHtml]Sie den Emulator, und installieren Sie dann die Android [Accessibility Suite][GooglePlayStoreAndroidAccessibilitySuite] aus dem GooglePlay Store.  

> [!NOTE]
> Der iOS-Simulator enthält derzeit nicht VoiceOver.  

### <a name="cloud-based-testing-tools"></a>Cloudbasierte Testtools  

Wenn eine Hilfstechnologie auf Ihrem Betriebssystem nicht verfügbar ist oder Sie eine nicht auf einem virtuellen Computer oder Emulator installieren können, sind cloudbasierte Tools zum Testen von Hilfstechnologien das nächste Beste.  

*   [Assistiv Labs (kommerziell)][AssistivlabsMain] ermöglicht ihnen das manuelle Testen mit Hilfstechnologien über jeden modernen Webbrowser.  Wählen Sie eine Hilfstechnologie und einen Browser aus, und sie verbindet Sie mit einem virtuellen Computer, Emulator oder einem echten Gerät, mit dem Sie interagieren können.  

## <a name="resources"></a>Ressourcen  

### <a name="accessibility-basics"></a>Grundlagen der Barrierefreiheit  

#### <a name="the-a11y-project"></a>Die A11Y-Project  

[Die A11Y Project](http://a11yproject.com) ist eine communitygesteuerte Anstrengung, um die Barrierefreiheit des Webs zu vereinfachen.  Weitere Informationen zu grundlegenden Barrierefreiheitsprinzipien, deren barrierefreien [](https://a11yproject.com/patterns)Mustern und [](http://a11yproject.com/resources.html) der Widgetbibliothek sowie deren Ressourcen zu Barrierefreiheitssoftware, Blogs, Büchern und Tools finden Sie auf der [A11Y-Project-Website.](https://a11yproject.com)  

#### <a name="web-accessibility-initiative-wai"></a>Web Accessibility Initiative (WAI)  

Die W3C [Web Accessibility Initiative (WAI)](https://w3.org/WAI) ist ein Versuch, die Barrierefreiheit des Webs zu verbessern.  Ihre Website bietet eine Vielzahl von Ressourcen für erste Schritte mit Barrierefreiheit im [Web,](https://www.w3.org/WAI/gettingstarted/Overview.html) [Entwerfen für](https://www.w3.org/WAI/users/Overview.html)Inklusion, [Lernprogramme und Präsentationen](https://www.w3.org/WAI/train.html)und vieles mehr.  

### <a name="accessibility-blogs"></a>Barrierefreiheitsblogs  

#### <a name="tpgi-llc"></a>TPGi, LLC  

[TPGi, LLC](https://www.tpgi.com/blog) bietet Beratungs- und Technologielösungen für Organisationen auf der ganzen Welt, um sicherzustellen, dass ihre Kunden alle Zielgruppen effektiv und effizient erreichen und gleichzeitig staatliche und internationale Standards erfüllen.  Ihr Blog behandelt Themen wie bewährte Methoden für die Webbarrierefreiheit, Barrierefreiheitstools und Barrierefreiheitstrends.  

#### <a name="simply-accessible"></a>Einfach zugänglich  

[Simply Accessible](http://simplyaccessible.com/articles) ist ein Team von Barrierefreiheitsspezialisten, das Barrierefreiheitsschulungen, Beratungsleistungen und vieles mehr bietet, um die Wahrnehmung von Barrierefreiheit im Web zu ändern.  In [ihrem Abschnitt](http://simplyaccessible.com/articles) Artikel werden bewährte Methoden für Barrierefreiheit im Web, barrierefreies Design und vieles mehr erläutert.  

#### <a name="level-access"></a>Zugriff auf Ebene  

[Level Access ist](https://www.levelaccess.com/blog) eine Firma für digitale Barrierefreiheit, die ihre Kunden bei der Entwicklung und Bereitstellung barrierefreier Produkte und Dienste unterstützt.  In ihrem Blog werden Themen wie bewährte Methoden für ARIA, Barrierefreiheitstrends, Webinare und vieles mehr behandelt.  

### <a name="accessible-examples"></a>Barrierefreie Beispiele  

#### <a name="allyjs---tutorials"></a>ally.js – Lernprogramme  

JavaScript-Bibliothek, um moderne Webanwendungen mit Barrierefreiheitsbedenken zu unterstützen, indem sie die Barrierefreiheit vereinfacht.  Weitere Informationen finden Sie unter [ally.js - Tutorials](http://allyjs.io/tutorials).  

#### <a name="openajax-examples"></a>OpenAjax-Beispiele  

Die [OpenAjax Alliance-Website](http://oaa-accessibility.org) ist eine hervorragende Ressource zum Überprüfen der Regeln für WAI-ARIA und bietet eine Reihe von Beispielen für WAI-ARIA-Implementierungen.  

#### <a name="patterns"></a>Muster  

[Das A11Y Project](http://a11yproject.com) bietet eine Bibliothek mit barrierefreien Widgets und Mustern wie Menüs, Schaltflächen, QuickInfos und mehr.  Weitere Informationen finden Sie unter [Patterns](http://a11yproject.com/patterns.html).  

### <a name="accessibility-techniques--tools"></a>Barrierefreiheitstechniken & Tools

#### <a name="accessibility--creating-accessible-extension-icons-for-microsoft-edge"></a>Barrierefreiheit: Erstellen barrierefreier Erweiterungssymbole für Microsoft Edge  

Hier erhalten Sie Anleitungen zum Erstellen von Symbolen für barrierefreie Microsoft Edge.  Weitere Informationen finden Sie unter [Accessibility: Creating accessible extension icons for Microsoft Edge](/archive/microsoft-edge/legacy/developer/extensions/guides/accessibility).  

#### <a name="accessible-name-and-description-computation-and-mappings-11"></a>Barrierefreier Name und Beschreibung: Berechnung und Zuordnungen 1.1  

In diesem W3C-Zuordnungsdokument wird erläutert, wie Browser Namen und Beschreibungen barrierefreier Objekte aus Webinhaltssprachen bestimmen und diese in Barrierefreiheits-APIs verfügbar machen.  Weitere Informationen finden Sie unter [Barrierefreier Name und Beschreibung: Berechnung und Zuordnungen 1.1](https://www.w3.org/TR/accname-1.1).  

#### <a name="accessibility-evaluation-resources"></a>Ressourcen für die Barrierefreiheitsbewertung  

Ressourcen für die Barrierefreiheitsbewertung ist eine mehrseitige Ressource des W3C, die verschiedene Ansätze für die Auswertung von Websites für Barrierefreiheit beschreibt.  Weitere Informationen finden Sie unter [Accessibility Evaluation Resources](https://www.w3.org/WAI/eval/Overview.html).  

#### <a name="assistive-technology-compatibility-tests"></a>Kompatibilitätstests für Hilfstechnologien  

Testergebnisse, die zeigen, wie sich unterschiedliche Inhaltstypen und Standards in Hilfstechnologien \(AT\) wie Bildschirmlesegeräten verhalten.  Weitere Informationen finden Sie unter [Assistive technology compatibility tests](http://www.powermapper.com/tests).  

#### <a name="building-accessible-websites-just-got-a-lot-easier"></a>Das Erstellen barrierefreier Websites wurde einfach einfacher  

In diesem .NET Web Development and Tools-Blogbeitrag wird die Visual Studio [Web Accessibility Checker beschrieben.](https://marketplace.visualstudio.com/items?itemName=MadsKristensen.WebAccessibilityChecker)  Weitere Informationen finden Sie unter [Building accessible websites just got a lot easier.](https://devblogs.microsoft.com/aspnet/building-accessible-websites-just-got-a-lot-easier)  

#### <a name="core-accessibility-api-mappings-11"></a>Grundlegende Barrierefreiheits-API-Zuordnungen 1.1  

In diesem W3C-Zuordnungsdokument wird erläutert, wie die Semantik von Webinhaltssprachen für Barrierefreiheits-APIs verfügbar gemacht wird.  Weitere Informationen finden Sie unter [Core Accessibility API Mappings 1.1](https://www.w3.org/TR/core-aam-1.1).  

#### <a name="easy-checks--a-first-review-of-web-accessibility"></a>Einfache Überprüfungen – Eine erste Überprüfung der Webbarrierefreiheit  

Eine Reihe von schnell überprüfungen durch die WAI, die Ihnen helfen, die Barrierefreiheit einer Webseite zu überprüfen.  Weitere Informationen finden Sie unter [Easy Checks – A First Review of Web Accessibility](https://www.w3.org/WAI/eval/preliminary.html).  

#### <a name="how-to-meet-wcag-20"></a>So treffen Sie WCAG 2.0  

Ein Kurzverweis auf Web Content Accessibility Guidelines \(WCAG\) 2.0 requirements \(success criteria\) and techniques.  Weitere Informationen finden Sie unter [How to Meet WCAG 2.0](https://www.w3.org/WAI/WCAG20/quickref).  

#### <a name="html-accessibility-api-mappings-10"></a>HTML Accessibility API Mappings 1.0  

In diesem W3C-Zuordnungsdokument wird erläutert, wie HTML5.1-Elemente und -Attribute plattformbarrierefreien APIs zugeordnet werden.  Weitere Informationen finden Sie unter [HTML Accessibility API Mappings 1.0](https://www.w3.org/TR/html-aam-1.0).  

#### <a name="quick-tips"></a>Schnell Tipps

Eine Liste der Tipps zur Schnellwebentwicklung für die Barrierefreiheit von [The A11Y Project](http://a11yproject.com).  Weitere Informationen finden Sie unter [Schnellstart Tipps](http://a11yproject.com#Quick-tips).  

#### <a name="site-scan"></a>Websitescan  

Das Tool "Websitescan" Microsoft Edge Dev Center prüft auf veraltete Bibliotheken, Layoutprobleme und Barrierefreiheitsprobleme.  Weitere Informationen finden Sie unter [Websitescan](https://developer.microsoft.com/microsoft-edge/tools).  

#### <a name="techniques-for-wcag-20"></a>Techniken für WCAG 2.0  

Techniken aus dem W3C, die Anleitungen für Webentwickler zum Erfüllen von [Web Content Accessibility Guidelines (WCAG) 2.0-Erfolgskriterien](https://w3.org/TR/WCAG20) bieten.  Weitere Informationen finden Sie unter [Techniken für WCAG 2.0](https://www.w3.org/TR/WCAG20-TECHS/Overview.html).  

#### <a name="tips-on-developing-for-web-accessibility"></a>Tipps auf Developing for Web Accessibility  

Tipps W3C zur Entwicklung von Webinhalten, die für Personen mit Behinderungen zugänglicher sind.  Weitere Informationen finden Sie unter [Tipps Entwickeln für Webbarrierefreiheit](https://w3.org/WAI/gettingstarted/tips/developing.html).  

#### <a name="wai-aria-authoring-practices-11"></a>WAI-ARIA Authoring Practices 1.1  

Ein Dokument des W3C, das Lesern ein Verständnis der Verwendung von WAI-ARIA 1.1 vermittelt und Ansätze zum Zugriff auf Widgets, Navigation und Verhaltensweisen mithilfe von WAI-ARIA-Rollen, -Zuständen und -Eigenschaften empfiehlt.  Weitere Informationen finden Sie unter [WAI-ARIA Authoring Practices 1.1](http://w3c.github.io/aria-practices).  

#### <a name="wai-guidelines-and-techniques"></a>WAI-Richtlinien und -Techniken  

Eine Reihe von Richtlinien und Standards für die Webbarrierefreiheit, die vom WAI entwickelt wurden.  Weitere Informationen finden Sie unter [WAI Guidelines and Techniques](https://w3.org/WAI/guid-tech.html).  

#### <a name="web-accessibility-evaluation-tools-list"></a>Web Accessibility Evaluation Tools List  

Eine Liste der Tools zur Bewertung der Webbarrierefreiheit, um festzustellen, ob Websites Barrierefreiheitsrichtlinien erfüllen.  Weitere Informationen finden Sie unter [Web Accessibility Evaluation Tools List](https://www.w3.org/WAI/ER/tools/index.html).  

#### <a name="web-accessibility-perspectives-explore-the-impact-and-benefits-for-everyone"></a>Web Accessibility Perspectives: Explore the Impact and Benefits for Everyone  

Eine Reihe kurzer Situationalvideos des W3C über die Auswirkungen der Barrierefreiheit und die Vorteile für alle.  Weitere Informationen finden Sie unter [Web Accessibility Perspectives: Explore the Impact and Benefits for Everyone](https://w3.org/WAI/perspectives).  

<!-- links -->  

<!--todo: link updates and acrolinx  -->  

[MicrosoftDeveloperEdgeVms]: https://developer.microsoft.com/microsoft-edge/tools/vms "Virtuelle Computer | Microsoft Edge Entwickler"  

[MicrosoftSupport22798]: https://support.microsoft.com/help/22798 "Vollständige Anleitung für Sprachausgabe | Microsoft Support"  
[MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198]: https://support.microsoft.com/windows/414948ba-8b1c-d3bd-8615-0e5e32204198 "Verwenden Sie Die Bildschirmlupe, um Die Dinge auf dem Bildschirm einfacher zu | Microsoft Support"  

[AccessibilityinsightsWebOverview]: https://accessibilityinsights.io/docs/web/overview "Accessibility Insights for Web | Einblicke in die Barrierefreiheit"  

[AndroidDeveloperDevicesManagingAvdsHtml]: https://developer.android.com/tools/devices/managing-avds.html "Erstellen und Verwalten von virtuellen | Android-Entwickler"  
[AndroidDeveloperDevicesEmulatorHtml]: https://developer.android.com/tools/devices/emulator.html "Ausführen von Apps auf dem Android-Emulator | Android-Entwickler"  
[AndroidDeveloperSdkInstallingStudioHtml]: https://developer.android.com/sdk/installing/studio.html "Herunterladen von Android Studio | Android-Entwickler"  

[AppleAccessibilityMacVision]: https://www.apple.com/accessibility/mac/vision "Barrierefreiheit – Mac | Apple"  

[AssistivlabsMain]: https://assistivlabs.com "Assistiv Labs"  

[FreedomscientificSoftwareJaws]: https://www.freedomscientific.com/products/software/jaws "JAWS® | Freiheit wissenschaftlich"  
[FreedomscientificSoftwareZoomtext]: https://www.freedomscientific.com/products/software/zoomtext "ZoomText-| Freiheit wissenschaftlich"  

[GooglePlayStoreAndroidAccessibilitySuite]: https://play.google.com/store/apps/details?id=com.google.android.marvin.talkback "Android Accessibility Suite | GooglePlay Store"  

[NvaccessAboutNvda]: https://www.nvaccess.org/about-nvda "Informationen zu NVDA-| NV Access"  

[W3cPerspectiveVideosKeyboard]: https://www.w3.org/WAI/perspective-videos/keyboard "Tastaturkompatibilität | W3C"  

[WebaimProjectsLowvisionsurvey2]: https://webaim.org/projects/lowvisionsurvey2 "Umfrage unter Benutzern mit geringer Sehkraft \#2 Ergebnisse | WebAIM"  
[WebaimProjectsScreenreadersurvey8]: https://webaim.org/projects/screenreadersurvey8 "Screen Reader User Survey \#8 Results | WebAIM"  
[WebaimArticlesScreenreaderTesting]: https://webaim.org/articles/screenreader_testing "Testen mit Bildschirmlesegeräten | WebAIM"  
