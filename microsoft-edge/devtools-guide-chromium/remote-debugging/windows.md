---
description: Erste Schritte mit remote debuggen von Windows 10-Geräten
title: Erste Schritte mit remote debuggen von Windows 10-Geräten
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/23/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, remote, debugging, windows 10, windows, device portal
ms.openlocfilehash: e3f60f07ba96aaed8cd9d7348eee1b0a846faecf
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519255"
---
# <a name="get-started-with-remote-debugging-windows-10-devices"></a>Erste Schritte mit remote debuggen von Windows 10-Geräten  

Remotedebuggern von Liveinhalten auf einem Windows 10-Gerät von Ihrem Windows- oder macOS-Computer.  In diesem Lernprogramm werden die folgenden Aufgaben erläutert.  

*   Richten Sie Ihr Windows 10-Gerät für das Remotedebubugen ein, und stellen Sie eine Verbindung mit dem Gerät von Ihrem Entwicklungscomputer aus.  
*   Überprüfen und Debuggen von Liveinhalten auf Ihrem Windows 10-Gerät auf Ihrem Entwicklungscomputer.  
*   Screencastinhalt von Ihrem Windows 10-Gerät auf eine DevTools-Instanz auf Ihrem Entwicklungscomputer.  
    
## <a name="step-1-set-up-the-host-debuggee-machine"></a>Schritt 1: Einrichten des Hosts (Debuggecomputer)  

Der Host- oder Debuggecomputer ist das Windows 10-Gerät, das Sie debuggen möchten.  Es kann ein Remotegerät sein, auf das Sie nur schwer physisch zugreifen können, oder es hat keine Tastatur- und Mausperipheriegeräte, was die Interaktion mit den Microsoft Edge DevTools auf diesem Gerät erschwert.  Zum Einrichten des Hostcomputers \(debuggee\) müssen Sie die folgenden Aktionen ausführen.  

*   Installieren und Konfigurieren [von Microsoft Edge (Chromium)][MicrosoftEdgeMain]  
*   Installieren der [Remotetools für Microsoft Edge (Beta)][MicrosoftStoreApps9p6cmfv44zlt] aus dem [Microsoft Store][MicrosoftStoreAppsWindows]  
*   Aktivieren [des Entwicklermodus][WindowsAppsGetStartedEnableYourDeviceForDevelopment] und Aktivieren des [Geräteportals][WindowsUwpDebugTestPerfDevicePortal]  
    
### <a name="install-and-configure-microsoft-edge-chromium"></a>Installieren und Konfigurieren von Microsoft Edge (Chromium)  

Falls noch nicht, installieren Sie Microsoft Edge \(Chromium\) auf [dieser Seite.][MicrosoftEdgeMain]  Wenn Sie eine vorinstallierte Version von Microsoft Edge auf dem Hostcomputer \(debuggee\) verwenden, vergewissern Sie sich, dass Microsoft Edge \(Chromium\) und nicht Microsoft Edge \(EdgeHTML\) vorhanden ist.  Eine schnelle Möglichkeit zum Überprüfen ist das Laden im Browser und bestätigen, dass die Versionsnummer `edge://settings/help` 75 oder höher ist.  

Navigieren Sie nun `edge://flags` in Microsoft Edge \(Chromium\) zu.  Geben **Sie unter Suchflags**die Option **Remotedebuggen über das Windows Device Portal aktivieren ein.**  Legen Sie dieses Flag auf **Aktiviert fest.**  Wählen Sie dann die Schaltfläche **Neustart aus,** um Microsoft Edge \(Chromium\) neu zu starten.  

:::image type="complex" source="../media/remote-debugging-windows-media-edge-flags-on-host.msft.png" alt-text="Festlegen des Kennzeichens Remotedebuggen über Windows Device Portal aktivieren auf Aktiviert" lightbox="../media/remote-debugging-windows-media-edge-flags-on-host.msft.png":::
   Festlegen des **Kennzeichens Remotedebuggen über Windows Device Portal** aktivieren auf **Aktiviert**  
:::image-end:::  

### <a name="install-the-remote-tools-for-microsoft-edge-beta"></a>Installieren der Remotetools für Microsoft Edge (Beta)  

Installieren Sie [die Remotetools für Microsoft Edge (Beta)][MicrosoftStoreApps9p6cmfv44zlt] aus dem [Microsoft Store][MicrosoftStoreAppsWindows].  

> [!NOTE]
> Die **Schaltfläche** Get für [die Remotetools für Microsoft Edge (Beta)][MicrosoftStoreApps9p6cmfv44zlt] ist möglicherweise deaktiviert, wenn Sie sich unter Windows 10, Version 1809 oder früher, befinden.  Zum Einrichten des Hostcomputers \(debuggee\) muss Windows 10, Version 1903 oder höher, ausgeführt werden.  Aktualisieren Sie den Hostcomputer \(debuggee\), um die [Remotetools für Microsoft Edge (Beta) zu erwerben.][MicrosoftStoreApps9p6cmfv44zlt]  

:::image type="complex" source="../media/remote-debugging-windows-media-remote-tools-in-store.msft.png" alt-text="Die Remotetools für Microsoft Edge \(Beta\) im Microsoft Store" lightbox="../media/remote-debugging-windows-media-remote-tools-in-store.msft.png":::
   Die [Remotetools für Microsoft Edge (Beta)][MicrosoftStoreApps9p6cmfv44zlt] im [Microsoft Store][MicrosoftStoreAppsWindows]  
:::image-end:::  

Starten Sie [die Remotetools für Microsoft Edge (Beta)][MicrosoftStoreApps9p6cmfv44zlt] und akzeptieren Sie bei Aufforderung das Dialogfeld Berechtigungen in der App.  Sie können nun die Remotetools für [Microsoft Edge (Beta)][MicrosoftStoreApps9p6cmfv44zlt] schließen, und sie müssen nicht für zukünftige Remotedebubusitzungen geöffnet sein.

### <a name="activate-developer-mode-and-enable-device-portal"></a>Aktivieren des Entwicklermodus und Aktivieren des Geräteportals  

Wenn Sie sich in einem WLAN-Netzwerk befinden, stellen Sie sicher, dass das Netzwerk entweder **als Domäne** oder als Privat **gekennzeichnet ist.**  Sie können den Status überprüfen, indem Sie die **Windows Security-App** öffnen, firewall **&** Netzwerkschutz **** auswählen und überprüfen, ob Ihr Netzwerk als Domänennetzwerk oder privates Netzwerk **aufgeführt** ist.  

Wenn sie als Öffentlich aufgeführt **** **ist,** navigieren Sie zu Einstellungen Netzwerk  >  **&**  >  **Internet-WLAN,** **** wählen Sie in Ihrem Netzwerk aus, und schalten Sie die Schaltfläche Netzwerkprofil auf **Privat um.**  

Öffnen Sie nun die **App Einstellungen.**  Geben **Sie unter Suchen einer Einstellung**ein, und wählen Sie sie `Developer settings` aus.  Umschalten im **Entwicklermodus**.  Sie können nun das Geräteportal **aktivieren,** indem Sie **Remotediagnosen** über lokale Netzwerkverbindungen auf **Ein aktivieren festlegen.**  Anschließend können Sie die **** Authentifizierung optional aktivieren, damit das Clientgerät \(Debugger\) die richtigen Anmeldeinformationen für die Verbindung mit diesem Gerät bereitstellen muss.  

> [!NOTE]
> Wenn **Remotediagnosen über Lokale Netzwerkverbindungen aktivieren.** zuvor aktiviert war, müssen Sie es deaktivieren und **** erneut aktivieren, damit das Geräteportal mit den [Remotetools für Microsoft Edge (Beta) funktioniert.][MicrosoftStoreApps9p6cmfv44zlt]  Wenn unter **Einstellungen kein** Abschnitt für Entwickler **** angezeigt **wird,** ist das Geräteportal möglicherweise bereits aktiviert, versuchen Sie stattdessen, das Windows 10-Gerät neu zu starten.

:::image type="complex" source="../media/remote-debugging-windows-media-host-settings.msft.png" alt-text="Die Einstellungs-App mit dem Entwicklermodus und dem Geräteportal konfiguriert" lightbox="../media/remote-debugging-windows-media-host-settings.msft.png":::
   Die **Einstellungs-App** **mit dem Entwicklermodus** und dem **Geräteportal** konfiguriert  
:::image-end:::  

Notieren Sie sich die COMPUTER-IP-Adresse und den Verbindungsport, die unter **Verbinden mit angezeigt werden:**.  Die IP-Adresse in der abbildung unten `192.168.86.78` ist und der Verbindungsport ist `50080` .  

:::image type="complex" source="../media/remote-debugging-windows-media-host-settings-ip-address.msft.png" alt-text="Notieren Sie sich die IP-Adresse und den Verbindungsport in den Einstellungen." lightbox="../media/remote-debugging-windows-media-host-settings-ip-address.msft.png":::
   Notieren Sie sich die IP-Adresse und den Verbindungsport in den **Einstellungen.**  
:::image-end:::  

Sie geben die Informationen auf dem Clientgerät \(Debugger\) im nächsten [Abschnitt ein.](#step-2-set-up-the-client-debugger-machine)  Öffnen Sie Registerkarten in Microsoft Edge und [Progressive Web Apps (PWAs)][DevtoolsProgressiveWebApps] auf dem Hostcomputer \(debuggee\), den Sie auf dem Clientcomputer debuggen möchten.  

## <a name="step-2-set-up-the-client-debugger-machine"></a>Schritt 2: Einrichten des Clients (Debuggercomputer)  

Der Client- oder Debuggercomputer ist das Gerät, von dem Sie debuggen möchten.  Dieses Gerät kann Ihr täglicher Entwicklungscomputer sein, oder es kann nur Ihr PC oder MacBook sein, wenn Sie von zu Hause aus arbeiten.  

Wenn Sie den Clientcomputer \(debugger\) einrichten möchten, installieren [][MicrosoftEdgeMain] Sie Microsoft Edge \(Chromium\) auf dieser Seite, falls noch nicht vorhanden.  Wenn Sie eine vorinstallierte Version von Microsoft Edge auf dem Hostcomputer \(debuggee\) verwenden, vergewissern Sie sich, dass Microsoft Edge \(Chromium\) und nicht Microsoft Edge \(EdgeHTML\) vorhanden ist.  Eine schnelle Möglichkeit zum Überprüfen ist das Laden im Browser und bestätigen, dass die Versionsnummer `edge://settings/help` 75 oder höher ist.  

Navigieren Sie nun `edge://flags` in Microsoft Edge \(Chromium\) zu.  Geben **Sie unter Suchkennzeichen**die Option **Remote-Windows-Gerätedebuggen aktivieren in edge://inspect.**  Legen Sie dieses Flag auf **Aktiviert fest.**  Wählen Sie dann die Schaltfläche **Neustart aus,** um Microsoft Edge \(Chromium\) neu zu starten.  

:::image type="complex" source="../media/remote-debugging-windows-media-edge-flags-on-client.msft.png" alt-text="Festlegen der Option Remote-Windows-Gerätedebuggen über edge://inspect aktivieren auf Aktiviert" lightbox="../media/remote-debugging-windows-media-edge-flags-on-client.msft.png":::
   Festlegen der **Option Remote-Windows-Gerätedebuggen** über edge://inspect aktivieren auf **Aktiviert**  
:::image-end:::  

Navigieren Sie nun zu `edge://inspect` der Seite in Microsoft Edge \(Chromium\).  Standardmäßig sollten Sie im Abschnitt Geräte **angezeigt** werden.  Geben Sie unter Verbinden mit einem **Remote-Windows-Gerät**die IP-Adresse und den Verbindungsport des Hostcomputers \(debuggee\) in das Textfeld ein, das folgende Muster enthält: http:// `IP address` : `connection port` .  Wählen Sie jetzt **Verbinden mit Gerät aus.**  

:::image type="complex" source="../media/remote-debugging-windows-media-edge-inspect.msft.png" alt-text="Die edge://inspect auf dem Client" lightbox="../media/remote-debugging-windows-media-edge-inspect.msft.png":::
   Die `edge://inspect` Seite auf dem Client  
:::image-end:::  

Wenn Sie die Authentifizierung für den Hostcomputer \(debuggee\) **** einrichten, **** werden Sie aufgefordert, den Benutzernamen und das Kennwort für den Clientcomputer \(Debugger\) einzugeben, um eine erfolgreiche Verbindung herzustellen.  

### <a name="using-https-instead-of-http"></a>Verwenden von https anstelle von http  

Wenn Sie eine Verbindung mit dem Hostcomputer \(debuggee\) herstellen möchten, müssen Sie in Microsoft Edge auf dem Clientcomputer `https` `http` `http://IP address:50080/config/rootcertificate` \(Debugger\) zu navigieren.  Dadurch wird automatisch ein Sicherheitszertifikat mit dem Namen `rootcertificate.cer` heruntergeladen.

Wählen Sie `rootcertificate.cer` aus.  Dadurch wird das [Windows Certificate Manager-Tool geöffnet.][DotnetFrameworkWcfFeatureDetailsHowToViewCertificatesWithMmcSnapInViewCertificatesWithCertificateManagerTool]

Wählen **Sie Zertifikat installieren...** aus, stellen Sie sicher, **dass der** aktuelle Benutzer aktiviert ist, und wählen Sie **Weiter aus.**  Wählen Sie **jetzt Alle Zertifikate im folgenden Speicher platzieren aus,** und wählen Sie **Durchsuchen...** aus.  Wählen Sie den **Speicher der vertrauenswürdigen Stammzertifizierungsstellen** aus, und wählen Sie **OK aus.**  Wählen **Sie Weiter** und dann Fertig stellen **aus.**  Wenn Sie dazu aufgefordert werden, bestätigen Sie, dass Sie dieses Zertifikat im Speicher der vertrauenswürdigen **Stammzertifizierungsstellen** installieren möchten.

Wenn Sie nun über die Seite eine Verbindung mit dem Hostcomputer \(debuggee\) vom Clientcomputer \(Debugger\) herstellen, müssen Sie einen `edge://inspect` anderen Wert `connection port` verwenden.  Standardmäßig wird für Desktop-Windows das Geräteportal `50080` als für `connection port` `http` verwendet.  Für `https` verwendet das Geräteportal dieses `50043` Muster: https:// : auf der `IP address` `50043` `edge://inspect` Seite.  [Weitere Informationen zu den standardports, die vom Geräteportal verwendet werden.][WindowsUwpDebugTestPerfDevicePortalSetup]  

> [!NOTE]
> Der Standardport für ist und der Standardport für ist, aber dies ist nicht immer der Fall als Geräteportal auf Desktop-Anspruchsports im kurzlebigen Bereich `http` `50080` `https` \(\>50.000\), um Kollisionen mit vorhandenen Portansprüchen auf dem Gerät zu `50043` verhindern.  Weitere Informationen finden Sie im Abschnitt  [Porteinstellungen][WindowsUwpDebugTestPerfDevicePortalDesktopRegistryBasedConfigurationForDevicePortal] für das Geräteportal auf Dem Windows-Desktop.  

## <a name="step-3-debug-content-on-the-host-from-the-client"></a>Schritt 3: Debuggen von Inhalten auf dem Host über den Client  

Wenn der Clientcomputer \(Debugger\) erfolgreich eine Verbindung mit dem Hostcomputer \(debuggee\) herstellt, zeigt die Seite auf dem Client nun eine Liste der Registerkarten in Microsoft Edge und aller geöffneten PWAs auf dem Host `edge://inspect` an.  

:::image type="complex" source="../media/remote-debugging-windows-media-edge-inspect-connected.msft.png" alt-text="Die edge://inspect auf dem Client zeigt die Registerkarten in Microsoft Edge und PWAs auf dem Host an." lightbox="../media/remote-debugging-windows-media-edge-inspect-connected.msft.png":::
   Auf `edge://inspect` der Seite auf dem Client werden die Registerkarten in Microsoft Edge und PWAs auf dem Host angezeigt.  
:::image-end:::  

Bestimmen Sie den Inhalt, den Sie debuggen möchten, und wählen Sie **überprüfen aus.**  Die Microsoft Edge DevTools werden auf einer neuen Registerkarte geöffnet und den Inhalt vom Hostcomputer \(debuggee\) auf den Clientcomputer \(Debugger\) übertragen.  Sie können jetzt die volle Leistung der Microsoft Edge DevTools auf dem Client für Inhalte nutzen, die auf dem Host ausgeführt werden.  Weitere Informationen zur Verwendung der Microsoft Edge DevTools finden Sie [hier][DevtoolsIndex].  

:::image type="complex" source="../media/remote-debugging-windows-media-devtools-client.msft.png" alt-text="Die Microsoft Edge DevTools auf dem Client debuggen eine Registerkarte in Microsoft Edge auf dem Host" lightbox="../media/remote-debugging-windows-media-devtools-client.msft.png":::
   Die [Microsoft Edge DevTools auf][DevtoolsIndex] dem Client debuggen eine Registerkarte in Microsoft Edge auf dem Host  
:::image-end:::  

### <a name="inspect-elements"></a>Überprüfen von Elementen  

Versuchen Sie beispielsweise, ein Element zu überprüfen.  Navigieren Sie zum **Elementtool** Ihrer DevTools-Instanz auf dem Client, und zeigen Sie auf ein Element, um es im Viewport des Hostgeräts zu markieren.  

Sie können auch auf ein Element auf dem Bildschirm des Hostgeräts tippen, um es im **Elementtool zu** wählen.  Wählen **Sie Element auswählen** auf Ihrer DevTools-Instanz auf dem Client aus, und tippen Sie dann auf das Element auf dem Hostgerätbildschirm.  

> [!NOTE]
> **Select Element** ist nach dem ersten Touch deaktiviert, daher müssen Sie es jedes Mal wieder aktivieren, wenn Sie dieses Feature verwenden möchten.  

> [!IMPORTANT]
> Der **Bereich Ereignislistener** im **Tool Elemente** ist unter Windows 10, Version 1903, leer.  Dies ist ein **bekanntes** Problem, und das Team plant, den Bereich Ereignislistener in einem Wartungsupdate auf Windows 10, Version 1903, zu beheben.  

## <a name="step-4-screencast-your-host-screen-to-your-client-device"></a>Schritt 4: Screencast your host screen to your client device  

Standardmäßig ist für die DevTools-Instanz auf dem Client die Screencasting aktiviert, mit der Sie die Inhalte auf dem Hostgerät in Ihrer DevTools-Instanz auf Ihrem Clientgerät anzeigen können.  Wählen **Sie Screencast umschalten** aus, um dieses Feature zu deaktivieren oder zu aktivieren.  

:::image type="complex" source="../media/remote-debugging-windows-media-toggle-screencast.msft.png" alt-text="Die Schaltfläche Screencast umschalten in den Microsoft Edge DevTools auf dem Client" lightbox="../media/remote-debugging-windows-media-toggle-screencast.msft.png":::
   Die **Schaltfläche Screencast umschalten** in den Microsoft Edge DevTools auf dem Client  
:::image-end:::  

Sie können auf verschiedene Weise mit dem Screencast interagieren:  
*   Auswahlen werden in Tipptasten übersetzt, die richtige Touchereignisse auf dem Gerät abfeuern.  
*   Tastaturanschläge auf Ihrem Computer werden an das Gerät gesendet.  
*   Halten Sie beim Ziehen gedrückt, um eine `Shift` Prisegeste zu simulieren.  
*   Wenn Sie einen Bildlauf durchführen möchten, verwenden Sie das Trackpad oder mausrad oder bewegen Sie sich mit dem Mauszeiger.  

Einige Hinweise zu Screencasts:  
*   Screencasts zeigen nur Seiteninhalte an.  Transparente Teile des Screencasts stellen Geräteschnittstellen dar, z. B. die Microsoft Edge-Adressleiste, die Windows 10-Taskleiste oder die Windows 10-Tastatur.  
*   Screencasts wirken sich negativ auf die Frameraten aus.  Deaktivieren Sie das Screencasting, während Sie Bildlauf oder Animationen messen, um ein genaueres Bild der Leistung Ihrer Seite zu erhalten.  
*   Wenn der Bildschirm des Hostgeräts gesperrt wird, wird der Inhalt des Screencasts ausgeblendet.  Entsperren Sie den Bildschirm Des Hostgeräts, um den Screencast automatisch fortsetzen zu können.  

## <a name="known-issues"></a>Bekannte Probleme  

Der **Bereich Ereignislistener** im **Tool Elemente** ist unter Windows 10, Version 1903, leer.  Das Team plant, den Bereich **Ereignislistener** in einem Wartungsupdate auf Windows 10, Version 1903, zu beheben.  

Der **Bereich** Cookies im **Bereich Anwendung** ist unter Windows 10, Version 1903, leer.  Das Team plant, den **Bereich Cookies** in einem Dienstupdate auf Windows 10, Version 1903, zu beheben.  

Das **Überwachungstool,** **** das **3D-Ansichtstool,** der Abschnitt **** **Emulierte** Geräte unter **Einstellungen**und der Barrierefreiheitsstrukturbereich im Elementtool funktionieren derzeit nicht wie erwartet.  Das Team plant, die aufgeführten Tools in einem zukünftigen Update von Microsoft Edge zu beheben.  

Der Datei-Explorer wird beim Remotedebugger nicht **** über die DevTools im **Tool Quellen** oder im Sicherheitsbereich gestartet.  Das Team plant, die Tools in einem zukünftigen Update von Microsoft Edge zu beheben.  

<!-- links -->

[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) Entwickler Tools Übersicht | Microsoft-Dokumentation"  
[DevtoolsProgressiveWebApps]: ../progressive-web-apps/index.md "Debuggen von Progressive Web Apps | Microsoft Docs"  

[DotnetFrameworkWcfFeatureDetailsHowToViewCertificatesWithMmcSnapInViewCertificatesWithCertificateManagerTool]: /dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in#view-certificates-with-the-certificate-manager-tool "Anzeigen von Zertifikaten mit dem Zertifikat-Manager-Tool – How to: View certificates with the MMC snap-in | Microsoft Docs"  

[WindowsAppsGetStartedEnableYourDeviceForDevelopment]: /windows/apps/get-started/enable-your-device-for-development "Aktivieren Sie Ihr Gerät für | Microsoft Docs"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Übersicht über das Windows Device Portal | Microsoft Docs"  
[WindowsUwpDebugTestPerfDevicePortalSetup]: /windows/uwp/debug-test-perf/device-portal#setup "Setup – Übersicht über das Windows Device Portal | Microsoft Docs"  
[WindowsUwpDebugTestPerfDevicePortalDesktopRegistryBasedConfigurationForDevicePortal]: /windows/uwp/debug-test-perf/device-portal-desktop#registry-based-configuration-for-device-portal "Registrierungsbasierte Konfiguration für das Geräteportal – Geräteportal für Windows Desktop | Microsoft Docs"  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Den neuen Microsoft Edge-Browser herunterladen"  

[MicrosoftStoreAppsWindows]: https://www.microsoft.com/store/apps/windows "Windows Apps | Microsoft Store"  

[MicrosoftStoreApps9p6cmfv44zlt]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Remotetools für Microsoft Edge (Beta) | Microsoft Store"  
