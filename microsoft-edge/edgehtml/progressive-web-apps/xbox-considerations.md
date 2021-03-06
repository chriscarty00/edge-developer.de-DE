---
description: Stellen Sie sicher, dass Ihr PWA eine großartige Erfahrung für Xbox bietet
title: Progressive Web Apps für Xbox One
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Progressive Web Apps, PWA, Edge, Windows, UWP, Xbox, Xbox One, TVJS
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3ac4174c821f221d6d666a25880867275ca5cbd5
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397671"
---
# <a name="progressive-web-apps-for-xbox-one"></a>Progressive Web Apps für Xbox One  

Sie können eine Webanwendung erweitern und als Xbox One-App über den Microsoft Store verfügbar machen, während Sie weiterhin Vorhandene Frameworks, CDN und Server-Back-End verwenden.  Und wie alle Apps der universellen Windows-Plattform \(UWP\) können progressive Web Apps \(PWAs\), die auf Xbox One ausgeführt werden, auch systemeigene Windows 10-APIs aufrufen.  Es sind bereits eine Reihe von PWAs für die Xbox One verfügbar, insbesondere in der Kategorie der [Medienwiedergabe-Apps.](#media-pwas-on-xbox)  

Zum größten Teil können Sie PWA für Xbox One auf die gleiche Weise wie [für Windows](./windows-features.md)packen, indem Sie die [PWA Builder-Tools](https://www.pwabuilder.com) oder Visual Studio IDE verwenden, um die Datei zu generieren, die zum Ausführen Ihrer PWA als [UWP-App](https://visualstudio.microsoft.com/vs) erforderlich `appxmanifest` ist.  Dieses Handbuch führt Sie jedoch durch mehrere wichtige Unterschiede.  

## <a name="deploying-and-testing-pwas-on-xbox"></a>Bereitstellen und Testen von PWAs auf Xbox  

Führen Sie die folgenden Schritte aus, [um den Xbox One Developer Mode zu *aktivieren.*](/windows/uwp/xbox-apps/devkit-activation)  Wenn der Entwicklermodus aktiviert ist, richten Sie das [ *Geräteportal für Xbox* ](/windows/uwp/debug-test-perf/device-portal-xbox) ein, um Remotezugriff auf Ihre Xbox über den Browser in Ihrer Entwicklungsumgebung zu erhalten.  

Jetzt können Sie Ihre App zum Testen mithilfe des PWA Builders oder Visual Studio.  

### <a name="option-1--pwa-builder"></a>Option 1: PWA Builder  

[PWA Builder](https://www.pwabuilder.com) ist eine Node.js, die Sie über Node Paket-Manager \(NPM\) installieren können.  Sie verwendet die Metadaten Ihrer Website, um systemeigene gehostete Apps für Android, iOS und Windows zu generieren.  Wenn Ihre Website bereits über ein [Web-App-Manifest](https://developer.mozilla.org/docs/Web/Manifest)verfügt, verwendet der PWA-Generator es zum Generieren plattformspezifischer Installationspakete.  Andernfalls generiert der PWA Builder eine grundlegende Datei basierend `manifest.json` auf den Merkmalen Ihrer Website.  

#### <a name="requirements"></a>Anforderungen  

*   [Node.js](https://nodejs.org), das NPM enthält.  

#### <a name="setup"></a>Setup  

1.  Öffnen Sie eine Node-Eingabeaufforderung, um den PWA-Generator zu installieren:  
    
    ```shell
    npm install pwabuilder --global
    ```  
    
1.  Führen Sie den PWA Builder auf Ihrer Website-URL aus:  
    
    ```shell
    pwabuilder https://example.com/ -windows10
    ```  
    
    Das *Flag -windows10* beschränkt die Paketgenerierung auf Windows 10 \(UWP\).  Sie können es auslassen, um Pakete auf allen unterstützten Plattformen zu generieren, einschließlich iOS und Android.  Weitere Informationen finden Sie in den [Dokumenten zum PWA-Generator.](https://docs.pwabuilder.com)  
    
1.  Wechseln Sie im [Geräteportal](/windows/uwp/debug-test-perf/device-portal-xbox)für Xbox zu **Startseite**Meine Spiele & Apps Hinzufügen, wählen Sie die Option zum Hochladen loser Dateien aus, und wählen Sie den Windows  >  ****  >  **** **** 10-App-Manifestordner aus, der vom PWA Builder im aktuellen Verzeichnis generiert wird.  
1.  Führen Sie den Assistenten durch, um den Installationsvorgang abzuschließen.  Nach der Installation.  Sie können Ihr PWA über das Xbox One-Dashboard anzeigen und starten.  
    
### <a name="option-2--visual-studio"></a>Option 2: Visual Studio  

Die kostenlose, voll ausgestattete [Visual Studio Community 2017](https://visualstudio.microsoft.com/vs/community) umfasst Windows 10-Entwicklertools, universelle App-Vorlagen, einen Code-Editor, einen leistungsstarken Debugger, Windows Mobile-Emulatoren, Unterstützung für umfangreiche Sprachen und vieles mehr – alles einsatzbereit in der Produktion.  Die [Professional- und Enterprise-Versionen](https://visualstudio.microsoft.com/vs/compare) bieten noch mehr Features.  

#### <a name="requirements"></a>Anforderungen  

*   [Visual Studio 2017](https://visualstudio.microsoft.com/vs): Jede Version, einschließlich der kostenlosen Community Edition.  
*   [Windows 10 SDK](/windows/uwp/xbox-apps/development-environment-setup): Wählen Sie diese optionale Komponente im Visual Studio 2017 Installer aus.  

#### <a name="setup"></a>Setup  

1.  Führen Sie die Schritte [zum Einrichten und Ausführen Ihres PWA als universelle Windows-App aus.](./windows-features.md#set-up-and-run-your-universal-windows-app)  Damit verfügen Sie über eine voll funktionsfähige Windows 10-App, die auf universelle Windows-APIs zugreifen kann.  
1.  Sie können Jetzt Ihre PWA \(als UWP-App\) auf der Xbox One \(wie bei jedem anderen Windows 10-Remotegerät\) mithilfe des Visual Studio Debuggers bereitstellen und [debuggen.](/visualstudio/debugger/run-windows-store-apps-on-a-remote-machine?view=vs-2017&preserve-view=true
)  Alternativ können Sie Ihre PWA mithilfe des [Geräteportals für Xbox](/windows/uwp/debug-test-perf/device-portal-xbox) mithilfe der folgenden Schritte installieren.  
1.  Wechseln Sie im Geräteportal für Xbox zu **Home**  >  **My games \& apps**  >  **Add**, choose the option to upload **App Package and Dependencies**.  
1.  Navigieren Sie in Schritt 1 zu dem Paketordner, den Sie für Ihre App generiert haben, und wählen Sie die `.appx` Datei für den Upload aus.  Die [APPX-Datei](/windows/uwp/packaging/packaging-uwp-apps) ist eine UWP-App-Paketdatei, die zu Testzwecken auf jedem Gerät sidegeladen werden kann.  
1.  Tippen Sie als Nächstes **auf die** Schaltfläche Abhängigkeiten, wählen Sie den `dependencies` Unterordner für Ihre App aus, und laden Sie diese hoch.  Dieser Schritt ist nur für die Bereitstellung von Apps aus dem Geräteportal für Xbox erforderlich.  Visual Studio liefert Abhängigkeiten, wenn das Remotedebuding ausgeführt wird, und auf dem Computer des Endbenutzers werden diese bereits installiert, wenn sie aus dem Microsoft Store zugestellt werden.  
1.  Wenn das App-Paket und die **** Abhängigkeiten hochgeladen ** wurden, klicken Sie im Abschnitt Bereitstellen auf die Schaltfläche Los, und die App wird installiert.  Sie können Ihre App über Xbox starten!  

## <a name="ux-considerations-for-pwas-on-xbox"></a>Überlegungen zu UX für PWAs auf Xbox  

### <a name="design-for-the-10-foot-experience"></a>Design für die "10-Fuß-Erfahrung"  

Xbox One wird als "10-Fuß-Erfahrung" betrachtet, was bedeutet, dass Ihre Benutzer wahrscheinlich mindestens 10 Meter vom Bildschirm entfernt sitzen.  Überlegen Sie daher, wie Ihre App in dieser Entfernung verwendet werden kann, im Gegensatz zur herkömmlichen Desktopwebbrowsererfahrung mit Maus und Tastatur.  Anleitungen zu Design und UX finden Sie unter [Designing for Xbox and TV](/windows/uwp/design/devices/designing-for-tv).  

### <a name="understand-the-tv-safezone"></a>Verstehen der "TV SafeZone"  

Fernsehhersteller wenden eine [Sichere Zone um](/windows/uwp/design/devices/designing-for-tv#tv-safe-area) den Inhalt an, der Ihre App beschneiden kann.  Standardmäßig wenden wir einen sicheren Rahmen um Ihre App an, um dies zu berücksichtigen. Sie können jedoch sicherstellen, dass Ihre App die Vollbildgröße übernimmt, indem Sie [setDesiredBoundsMode](/uwp/api/windows.ui.viewmanagement.applicationview.setdesiredboundsmode) aufrufen und [useCoreWindow angeben:](/uwp/api/windows.ui.viewmanagement.applicationviewboundsmode)  

```javascript
var applicationView = Windows.UI.ViewManagement.ApplicationView.getForCurrentView();
applicationView.setDesiredBoundsMode(Windows.UI.ViewManagement.ApplicationViewBoundsMode.useCoreWindow);
```  

Weitere Informationen finden Sie in der [Windows.UI.ViewManagement-Namespacedokumentation.](/uwp/api/windows.ui.viewmanagement)  

### <a name="manage-xy-focus-and-navigation"></a>Verwalten des XY-Fokus und der Navigation  

Benutzereingabemethoden für Xbox sind Gamepads oder Fernbedienungen, die ein [XY-Navigationssystem](/windows/uwp/design/devices/designing-for-tv#xy-focus-navigation-and-interaction)verwenden und es dem Benutzer ermöglichen, den Fokus von Steuerelement zu Steuerelement zu verschieben, indem er nach oben, unten, links und rechts bewegt wird.  

Als solches sollten Sie sicherstellen, dass Ihre App gut mit der XY-Navigation funktioniert.  Achten Sie außerdem darauf, den Mausmodus [zu](/windows/uwp/xbox-apps/how-to-disable-mouse-mode)deaktivieren, der standardmäßig für UWP-Apps aktiviert ist \(und wahrscheinlich nicht auf die Xbox-Erfahrung Ihrer App anwendbar ist\).  

Der folgende Code deaktiviert den `mouse` Modus und ermöglicht die Gamepadeingabe zum Generieren von DOM-Tastaturereignissen:  

```javascript
navigator.gamepadInputEmulation = "keyboard";
```  

Alternativ können Sie angeben, dass auch die Maus deaktiviert, keine DOM-Tastaturereignisse generiert wird und Sie die standardmäßigen `gamepad` Web- und/oder WinRT-Gamepad-APIs verwenden können.  

Informationen zum Aktivieren der direktionalen Navigation finden Sie in der [TVJS-Bibliothek,](#tvjs)die als Nächstes behandelt wird.  

### <a name="tvjs"></a>TVJS  

[TVJS ist eine Sammlung von Hilfsbibliotheken,](https://github.com/Microsoft/TVHelpers) die das Erstellen von Webanwendungen für das Fernsehgerät vereinfachen.  Wenn Sie eine gehostete Web-App erstellen, die auch auf der Xbox ausgeführt wird, kann TVJS unterstützung für die direktionale Navigation hinzufügen und mehrere Steuerelemente *bereitstellen,* die die Interaktion mit Inhalten auf dem Fernseher vereinfachen.  

[Die direktionale Navigation](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) ist ein TVJS-Feature, das die automatische zweidimensionale Navigation auf den Seiten Ihrer FERNSEH-App ermöglicht.  Damit ist es nicht nötig, die Navigation auf den Seiten Ihrer App zu fangen und zu behandeln oder alle gültigen Fokusziele für jedes Element auf der Benutzeroberfläche explizit anzugeben.  Mit der automatischen Fokusbehandlung können Benutzer intuitiv und robust navigieren.  

Während Der Benutzer die App-UI mit den Steuerungsrichtungsschaltflächen navigiert, wird der automatische Fokusalgorithmus mit dem Satz potenzieller Fokusziele betrachtet, das nächste Element bestimmt, zu dem es wechseln soll, und legt dann automatisch den Fokus auf dieses Element fest.  Um das nächste Element zu bestimmen, kombiniert der Algorithmus direktionale Eingaben, den vergangenen Fokusverlauf und das physische Layout von Benutzeroberflächenelementen auf der Seite.  

Um die richtungsdirektionale Navigation zu aktivieren, fügen Sie den folgenden Skriptverweis ein:  

```html
<script src="directionalnavigation-1.0.0.0.js"></script>
```  

Standardmäßig sind nur `<a>` , , , und `<button>` `<input>` `<select>` `<textarea>` -Elemente fokussierbar.  Um den Fokus auf andere Elemente zu aktivieren, weisen Sie ihnen einen gültigen [Tabindex zu.](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex)  

```html
<div tabindex="0″>This div is eligible for focus</div>
```  

In der [DirectionalNavigation-Dokumentation](https://github.com/Microsoft/TVHelpers/wiki/DirectionalNavigation) erfahren Sie, wie Sie das Stammelement ändern, den anfänglichen Fokus festlegen, den nächsten Fokus außer Kraft setzen, Steuerelemente für den Fokus optimieren und die Eingabe anpassen.  Es gibt auch eine Reihe weiterer nützlicher Beispiele.

## <a name="media-pwas-on-xbox"></a>Medien-PWAs auf Xbox  

Wenn Sie eine Medienwiedergabe-PWA für Xbox One erstellen, beachten Sie die folgenden Überlegungen.  

### <a name="encrypted-media-extensions-eme-in-the-browser"></a>Verschlüsselte Medienerweiterungen (Encrypted Media Extensions, EME) im Browser  

Der Microsoft Edge-Browser auf Xbox One unterstützt [verschlüsselte Medienerweiterungen](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API) \(EME\) nicht.  Wenn Ihre Medien-PWA sie für die Verwaltung digitaler Rechte \(DRM\) verwendet, können Sie sie nicht über den Browser auf Ihrer Xbox ausführen.  Testen Sie stattdessen den Prototyp, und testen Sie ihn als Xbox One-App mit [PWABuilder oder Visual Studio](#deploying-and-testing-pwas-on-xbox), wie oben beschrieben.  Sie können es auch im Microsoft Edge-Browser unter Windows ausführen, wobei EME vollständig unterstützt wird.  

### <a name="integrating-with-system-media-transport-controls"></a>Integration in SystemMedientransportsteuerelemente  

Wenn Ihre App eine Medien-App ist, ist es wichtig, dass Ihre App auf [](https://support.xbox.com/xbox-one/console/cortana-voice-commands)die Mediensteuerelemente reagiert, die vom Benutzer über Bildschirmschaltflächen, Cortana-Sprachbefehle, die [Systemmedientransportsteuerelemente](/windows/uwp/audio-video-camera/system-media-transport-controls) im Navigationsbereich oder die [Xbox-](https://www.microsoft.com/p/xbox/9wzdncrfjbd8
) und [Xbox One SmartGlass-Apps](https://www.microsoft.com/p/xbox-one-smartglass/9wzdncrfhvx2) auf anderen Geräten initiiert wurden.  Sehen Sie sich das [MediaPlayer-Steuerelement](https://github.com/Microsoft/TVHelpers/wiki/MediaPlayer-Overview) aus der [TVJS-Bibliothek](#tvjs)an, das automatisch in diese Steuerelemente integriert wird.  Alternativ können Sie manuell in die Steuerelemente für den [Systemmedientransport integriert werden.](/windows/uwp/audio-video-camera/system-media-transport-controls)  

### <a name="playready-content-encryption"></a>PlayReady-Inhaltsverschlüsselung  

Zum Zeitpunkt dieses Schreibens ist die Cbcs-Codierungsunterstützung auf den PlayReady-Client für XBox One \(Version 1709 oder höher\) beschränkt. [](/playready/packaging/content-encryption-modes#support-for-the-cbcs-aes-cbc-encryption-scheme)  Wenn die Medien für Ihre PWA nur die **cbcs-Verschlüsselung** unterstützen, beachten Sie, dass die Funktionalität Ihrer App unter Windows wahrscheinlich eingeschränkt ist \(oder vollständig nicht verfügbar\).  

## <a name="see-also"></a>Weitere Informationen  

[South -Kammvideo:](https://github.com/Microsoft/uwp-experiences/tree/master/apps/video)Eine Beispielvideo-App für Xbox, die mit React.js erstellt und auf einem Webserver gehostet wird.  

[Entwerfen für Xbox und Tv:](/windows/uwp/design/devices/designing-for-tv)Entwerfen Sie Ihre App für die universelle Windows-Plattform \(UWP\) so, dass sie gut aussieht und auf Xbox One- und Fernsehbildschirmen gut funktioniert.  

[Bewährte Methoden für Xbox:](/windows/uwp/xbox-apps/tailoring-for-xbox)Befolgen Sie diese bewährten Methoden, um Ihre App für Xbox One zu anpassen.  

[PWAs im Microsoft Store](./microsoft-store.md): Hier erfahren Sie, wie \(und warum?\) Sie Ihre PWA an den Microsoft Store übermitteln.  

[UWP auf Xbox One:](/windows/uwp/xbox-apps/index)Ein vollständiger Leitfaden für die Entwicklung von UWP-Apps für Xbox One.  
