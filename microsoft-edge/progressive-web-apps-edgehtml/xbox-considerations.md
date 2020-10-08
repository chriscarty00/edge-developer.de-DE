---
description: Sicherstellen, dass Ihre PWA eine hervorragende Funktionalität für Xbox bietet
title: Progressive Web-Apps für Xbox One
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Progressive Web-Apps, PWA, Edge, Windows, UWP, Xbox, Xbox One, TVJS
ms.openlocfilehash: dfa2b2d252bb788c0010017de57ab147d407c5f7
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882853"
---
# Progressive Web-Apps für Xbox One  

Sie können eine Webanwendung erweitern und als Xbox One-App über den Microsoft Store verfügbar machen, während Sie weiterhin Ihre vorhandenen Frameworks, CDN und das Server-Back-End verwenden.  Und wie alle apps für die universelle Windows-Plattform (UWP) können Progressive Web Apps (PWAs), die auf Xbox One ausgeführt werden, auch Native Windows 10-APIs aufrufen.  Es gibt bereits eine Reihe von PWAs, die für die Xbox One verfügbar sind, insbesondere in der Kategorie der [Medienwiedergabe-apps](#media-pwas-on-xbox).  

In den meisten Teilen können Sie Ihre PWA für Xbox One auf die [gleiche Weise verpacken wie für Windows](./windows-features.md), indem Sie die [PWA-Generator](https://www.pwabuilder.com/) Tools oder die [Visual Studio](https://visualstudio.microsoft.com/vs/) -IDE verwenden, um die *appxmanifest* -Datei zu generieren, die zum Ausführen ihrer PWA-Anwendung als UWP-App erforderlich ist. Es gibt jedoch einige wichtige Unterschiede, die in diesem Leitfaden zu finden sind.

## Bereitstellen und Testen von PWAs auf Xbox

Führen Sie zunächst die folgenden [Schritte aus, um den *Xbox One-Entwicklermodus* zu aktivieren](/windows/uwp/xbox-apps/devkit-activation) . Wenn der Entwicklermodus aktiviert ist, [richten Sie *Device Portal für Xbox* ](/windows/uwp/debug-test-perf/device-portal-xbox) ein, um über den Browser in ihrer dev-Umgebung Remotezugriff auf Ihre Xbox zu erhalten.

Nun können Sie Ihre APP für Tests mit *PWA Builder* oder *Visual Studio*bereitstellen.

### Option 1: PWA-Generator

Der [PWA-Generator](https://www.pwabuilder.com/) ist eine Node.js-APP, die Sie über den Knoten Paket-Manager (NPM) installieren können. Sie verwendet die Metadaten Ihrer Website, um systemeigene gehostete Apps für Android, IOS und Windows zu generieren. Wenn Ihre Website bereits über ein [Web App-Manifest](https://developer.mozilla.org/docs/Web/Manifest)verfügt, wird Sie von PWA Builder zum Generieren plattformspezifischer Installationspakete verwendet. Andernfalls generiert PWA Builder basierend auf den Eigenschaften Ihrer Website eine grundlegende *manifest.jsfür* die Datei.

#### Anforderungen
 - [Node.js](https://nodejs.org/en/), das NPM umfasst.

#### Setup

1. Öffnen Sie eine Eingabeaufforderung des Knotens, um den PWA-Generator zu installieren:

    ```
    npm install pwabuilder --global
    ```

2. Führen Sie PWA Builder auf Ihrer Website-URL aus:

    ```
    pwabuilder https://example.com/ -windows10
    ```

    Das *-windows10-* Flag begrenzt die Paket Generierung auf Windows 10 (UWP). Sie können es auslassen, um Pakete über alle unterstützten Plattformen wie IOS und Android zu generieren. Weitere Informationen finden Sie in der [PWA-Builder-Dokumentation](https://docs.pwabuilder.com/) .

3. Wechseln Sie im [Geräte Portal für Xbox](/windows/uwp/debug-test-perf/device-portal-xbox)zu **Startseite**  >  **Meine Spiele & apps**  >  **Hinzufügen**, wählen Sie die Option zum *Hochladen von losen Dateien*aus, und wählen Sie den Windows 10-App-Manifest-Ordner aus, der vom PWA-Generator im aktuellen Verzeichnis generiert wird.

4. Führen Sie die Schritte im Assistenten aus, um den Installationsvorgang abzuschließen. Nach der Installation. Sie können Ihre PWA über das Xbox One-Dashboard anzeigen und starten.


### Option 2: Visual Studio

Das ﻿kostenlose, voll funktionsfähige [Visual Studio Community 2017](https://visualstudio.microsoft.com/vs/community/) umfasst Windows 10-Entwicklertools, universelle App-Vorlagen, einen Code-Editor, einen leistungsfähigen Debugger, Windows Mobile-Emulatoren, Rich-Language-Unterstützung und vieles mehr, die alle in der Produktion einsatzbereit sind. Die Versionen [ *Professional* und *Enterprise* ](https://visualstudio.microsoft.com/vs/compare/) bieten noch mehr Funktionen.

#### Anforderungen

 - [**Visual Studio 2017**](https://visualstudio.microsoft.com/vs/
): eine beliebige Version, einschließlich der kostenlosen *Community* Edition.
 - [**Windows 10 SDK**](/windows/uwp/xbox-apps/development-environment-setup): Wählen Sie diese optionale Komponente im *Visual Studio 2017-Installationsprogramm*aus.

#### Setup

1. Führen Sie die Schritte zum [Einrichten und Ausführen ihrer PWA als universelle Windows-App](/microsoft-edge/progressive-web-apps-edgehtml/windows-features#set-up-and-run-your-universal-windows-app)aus. Damit haben Sie eine voll funktionsfähige Windows 10-APP, die in der Lage ist, auf universelle Windows-APIs zuzugreifen.

2. Sie können jetzt mithilfe des [Visual Studio-Remotedebuggers](/visualstudio/debugger/run-windows-store-apps-on-a-remote-machine?view=vs-2017
)ihre PWA-(als UWP-APP) auf der Xbox One (wie bei allen anderen Windows 10-Remotegeräten) bereitstellen und Debuggen. Alternativ können Sie Ihre PWA mithilfe des [Geräte Portals für Xbox](/windows/uwp/debug-test-perf/device-portal-xbox) mithilfe der folgenden Schritte installieren.

3. Wechseln Sie im Geräte Portal für Xbox zu Start > meine Spiele & apps > hinzufügen, und wählen Sie die Option zum Hochladen von *App-Paketen und Abhängigkeiten*aus.

4. Navigieren Sie in Schritt 1 zu dem Paketordner, den Sie für Ihre APP generiert haben, und wählen Sie die *AppX* -Datei für den Upload aus. Die [ *AppX-* Datei](/windows/uwp/packaging/packaging-uwp-apps) ist eine UWP-App-Paketdatei, die für Testzwecke auf jedem Gerät quer geladene werden kann.

5. Tippen Sie als nächstes auf die Schaltfläche **Abhängigkeiten** , und wählen Sie den Unterordner *Abhängigkeiten* für Ihre APP aus, und laden Sie Sie hoch. Dieser Schritt ist nur für die Bereitstellung von Apps aus dem Geräte Portal für Xbox erforderlich. Visual Studio bietet Abhängigkeiten, wenn das Remotedebuggen und der Computer des Endbenutzers diese bereits installiert haben, wenn Sie aus dem Microsoft Store bereitgestellt werden.

6. Klicken Sie mit dem App-Paket und den hochgeladenen Abhängigkeiten auf die Schaltfläche **wechseln** unter dem Abschnitt *Bereitstellen* , und die APP wird installiert. Sie sind bereit, Ihre APP von Xbox aus zu starten!

## UX-Überlegungen für PWAs auf Xbox

### Design für "10-Fuß-Erfahrung"

Xbox One gilt als "10-Fuß-Erfahrung", was bedeutet, dass Ihre Benutzer wahrscheinlich mindestens 10 Fuß vom Bildschirm entfernt sitzen werden. Berücksichtigen Sie daher, wie Ihre APP in diesem Abstand verwendet werden kann, anstatt die herkömmliche Desktop-Webbrowseroberfläche mit einer Maus und einer Tastatur zu verwenden. Informationen zur Entwurfs-und UX-Anleitung finden Sie unter [Entwerfen für Xbox und Fernseh](/windows/uwp/design/devices/designing-for-tv)Geräte.

### Grundlegendes zur "TV-SafeZone"

Fernsehhersteller wenden eine ["sichere Zone"](/windows/uwp/design/devices/designing-for-tv#tv-safe-area) um den Inhalt an, der Ihre APP beschneiden kann. Standardmäßig wenden wir einen sicheren Rahmen um Ihre APP an, um dies zu berücksichtigen, jedoch können Sie sicherstellen, dass Ihre APP die vollständige Bildschirmgröße aufnimmt, indem Sie [`setDesiredBoundsMode`](/uwp/api/windows.ui.viewmanagement.applicationview.setdesiredboundsmode) Folgendes aufrufen und angeben [`useCoreWindow`](/uwp/api/windows.ui.viewmanagement.applicationviewboundsmode) :

```JavaScript
var applicationView = Windows.UI.ViewManagement.ApplicationView.getForCurrentView();
applicationView.setDesiredBoundsMode(Windows.UI.ViewManagement.ApplicationViewBoundsMode.useCoreWindow);
```

Weitere Informationen finden Sie in der [`Windows.UI.ViewManagement`](/uwp/api/windows.ui.viewmanagement) Namespace-Dokumentation.

### Verwalten des XY-Fokus und der Navigation

Benutzereingabemethoden für Xbox sind Gamepad oder Remotesteuerung, die ein [XY-Navigationssystem](/windows/uwp/design/devices/designing-for-tv#xy-focus-navigation-and-interaction)verwenden, das es dem Benutzer ermöglicht, den Fokus vom Steuerelement auf das Steuerelement zu verschieben, indem Sie nach oben, unten, Links und rechts navigieren.

Daher sollten Sie sicherstellen, dass Ihre APP mit der XY-Navigation gut funktioniert. Stellen Sie außerdem sicher, dass Sie den [ *Mausmodus*deaktivieren](/windows/uwp/xbox-apps/how-to-disable-mouse-mode), der standardmäßig für UWP-apps aktiviert ist (und wahrscheinlich nicht auf die Xbox-Umgebung Ihrer APP anwendbar ist).

Mit dem folgenden Code wird der `mouse` Modus deaktiviert, und die Gamepad-Eingabe ermöglicht das Generieren von Dom-Tastaturereignissen:

```JavaScript
navigator.gamepadInputEmulation = "keyboard";
```

Alternativ können Sie angeben `gamepad` , was auch die Maus deaktiviert, keine Dom-Tastaturereignisse generiert, und Sie können die standardmäßigen Web-und/oder WinRT-Gamepad-APIs verwenden.

Wenn Sie die Richtungsnavigation aktivieren möchten, lesen Sie die [TVJS-Bibliothek](#tvjs), die als nächstes erläutert wird.

### TVJS

[TVJS ist eine Sammlung von Hilfsbibliotheken](https://github.com/Microsoft/TVHelpers) , die das Erstellen von Webanwendungen für Fernsehgeräte vereinfachen. Wenn Sie eine gehostete Web-App erstellen, die auch auf der Xbox ausgeführt wird, kann TVJS dazu beitragen, die Unterstützung für die *direktionale Navigation*hinzuzufügen, und mehrere Steuerelemente bereitstellen, die die Interaktion mit Inhalten auf dem Fernsehgerät vereinfachen.

Bei der [direktionalen Navigation](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) handelt es sich um eine TVJS-Funktion, die eine automatische zweidimensionale Navigation auf den Seiten Ihrer TV-App ermöglicht. Damit ist es nicht erforderlich, die Navigation auf den Seiten der APP zu überspringen und zu behandeln oder alle gültigen Fokus Ziele für jedes Element in der Benutzeroberfläche explizit anzugeben. Mithilfe der automatischen Fokus Behandlung können Benutzer auf intuitive und robuste Weise navigieren.

Wenn der Benutzer die App-Benutzeroberfläche mit den Schaltflächen für die Controller Richtung navigiert, überprüft der automatische Fokus Algorithmus die Gruppe potenzieller Fokus Ziele, bestimmt das nächste Element, zu dem Sie wechseln möchten, und legt den Fokus dann automatisch auf dieses Element fest. Um das nächste Element zu ermitteln, kombiniert der Algorithmus die richtungseingabe, das vergangene Fokus Protokoll und das physikalische Layout der UI-Elemente auf der Seite.

Wenn Sie die Richtungsnavigation aktivieren möchten, schließen Sie den folgenden Skriptverweis ein:

```HTML
<script src="directionalnavigation-1.0.0.0.js"></script>
```

Standardmäßig sind nur `<a>` , `<button>` , `<input>` , `<select>` und `<textarea>` Elemente fokussierbar. Um den Fokus auf andere Elemente zu aktivieren, weisen Sie ihm einen gültigen [TabIndex](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex)zu.

```HTML
<div tabindex="0″>This div is eligible for focus</div>
```

Schauen Sie sich die [DirectionalNavigation](https://github.com/Microsoft/TVHelpers/wiki/DirectionalNavigation) -Dokumentation an, um zu erfahren, wie Sie das Stammelement ändern, den anfänglichen Fokus festlegen, den nächsten Fokus überschreiben, die Steuerelemente für den Fokus optimieren, die Eingabe anpassen. Es gibt auch eine Reihe weiterer nützlicher Beispiele.

## Medien PWAs auf Xbox

Wenn Sie eine Medienwiedergabe-PWA für Xbox One erstellen, sollten Sie sich mit den folgenden Aspekten vertraut machen.

### Verschlüsselte Medienerweiterungen (EME) im Browser

Der Microsoft Edge-Browser auf Xbox One unterstützt keine [verschlüsselten Medienerweiterungen](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API) (EME). Wenn Ihre Medien-PWA Sie für die Verwaltung digitaler Rechte (Digital Rights Management, DRM) verwendet, können Sie Sie nicht über den Browser auf der Xbox ausführen. Testen Sie Sie stattdessen als [Xbox One-App mit PWABuilder oder Visual Studio](#deploying-and-testing-pwas-on-xbox), wie oben beschrieben. Sie können es auch im Microsoft Edge-Browser unter Windows ausführen, wobei eme vollständig unterstützt wird.

### Integration in die Steuerelemente für den System Medien Transport

Wenn es sich bei ihrer App um eine Medien-App handelt, ist es wichtig, dass Ihre APP auf die vom Benutzer initiierten mediensteuerelemente über die Bildschirmschaltflächen, die [Cortana-Sprachbefehle](https://support.xbox.com/xbox-one/console/cortana-voice-commands), die [Steuerelemente für den System Medien Transport](/windows/uwp/audio-video-camera/system-media-transport-controls) im Navigationsbereich oder auf die [Xbox](https://www.microsoft.com/p/xbox/9wzdncrfjbd8
) -und [Xbox One-SmartGlass](https://www.microsoft.com/p/xbox-one-smartglass/9wzdncrfhvx2) -apps auf anderen Geräten reagiert. Sehen Sie sich das [Media Player](https://github.com/Microsoft/TVHelpers/wiki/MediaPlayer-Overview) -Steuerelement aus der [TVJS-Bibliothek](#tvjs)an, das automatisch in diese Steuerelemente integriert wird. Alternativ können Sie [die Steuerelemente für den System Medien Transport manuell integrieren](https://msdn.microsoft.com/windows/uwp/audio-video-camera/system-media-transport-controls).

### PlayReady-Inhalts Verschlüsselung

Zum Zeitpunkt der Erstellung dieses Artikels [ `cbcs` ist die Codierungsunterstützung](/playready/packaging/content-encryption-modes#support-for-the-cbcs-aes-cbc-encryption-scheme) auf den PlayReady-Client für Xbox One (Version 1709 oder höher) limitiert. Wenn die Medien für Ihre PWA- *CBCs* -Verschlüsselung nur unterstützt werden, beachten Sie, dass die Funktionalität Ihrer APP unter Windows wahrscheinlich limitiert (oder vollständig nicht verfügbar) sein wird.



## Weitere Informationen
[South Ridge Video](https://github.com/Microsoft/uwp-experiences/tree/master/apps/video): eine Beispiel-Video-App für Xbox, die mit React.js erstellt und auf einem Webserver gehostet wird.

[Entwerfen für Xbox und TV](/windows/uwp/design/devices/designing-for-tv): Entwerfen Sie Ihre APP für die universelle Windows-Plattform (UWP) so, dass Sie gut aussieht und auf Xbox One-und Fernsehbildschirmen gut funktioniert.

Bewährte [Methoden für Xbox](/windows/uwp/xbox-apps/tailoring-for-xbox): Befolgen Sie diese bewährten Methoden zum Anpassen Ihrer APP für Xbox One.

[PWAs im Microsoft Store](/microsoft-edge/progressive-web-apps-edgehtml/microsoft-store): gehen Sie wie folgt vor, um Ihre PWA an den Microsoft Store zu übermitteln.

[UWP auf Xbox One](/windows/uwp/xbox-apps/): eine vollständige Anleitung zur UWP-App-Entwicklung für Xbox One.
