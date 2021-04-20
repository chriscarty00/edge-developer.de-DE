---
beschreibung: Featureunterschiede zwischen Microsoft Edge und WebView2-Titel: Featureunterschiede zwischen Microsoft Edge und WebView2-Autor: MSEdgeTeam ms.author: msedgedevrel ms.date: 19.04.2021 ms.topic: konzeptionell ms.prod: microsoft-edge ms.technology: webview keywords: IWebView2, IWebView2WebView, WebView2, Webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html no-loc:
- "Autofill for Addresses"
- "Autofill for Passwords"
- "Autofill for Payments""
- "Browser Extensions""
- "Browser Task Manager"
- "Collections"
- "Continue-where-I-left-off prompt"
- "Downloads"
- "Edge Shopping"
- "Family Safety"
- "Favorites"
- "Hotkeys"
- "IE Mode"
- "Immersive Reader"
- "Intrusive Ads"
- "Read Aloud"
- "Smart Screen"
- "Translate"
- "Tracking Prevention"
- "Profile and Identity"
- "Web Payment API"
- "Windows Defender Application Guard"
- "edge:// URLs"

---
# <a name="browser-feature-differences-between-microsoft-edge-and-webview2"></a>Unterschiede zwischen Microsoft Edge und WebView2 bei Browserfeatures  

WebView2 basiert auf dem neuen Microsoft Edge-Browser.  Sie haben die Möglichkeit, Features vom Browser auf WebView2-basierte Apps zu erweitern, was nützlich ist.  Da Sich WebView2 jedoch nicht auf browser like apps beschränkt, müssen einige Browserfeatures geändert oder entfernt werden.  Dieser Artikel enthält die folgenden Informationen.  

*   Die geänderten Browserfeatures und unterstützenden Informationen.   
*   Die Möglichkeit, das Feature ein- oder auszuschalten.  
*   Anleitungen zu Tastenkombinationen.  
    
## <a name="design-guidelines"></a>Entwurfsrichtlinien  

Im Kontext von WebView2 halten sich Browserfeatures an die folgenden Entwurfsrichtlinien.  

*   Die meisten Features funktionieren in WebView2 und Microsoft Edge identisch.  Wenn ein Feature im Kontext von WebView2 oder aus anderen Gründen nicht sinnvoll ist, wird das Feature geändert oder deaktiviert. 
*   WebView2-Features enthalten kein Microsoft Edge-Branding.  
    
## <a name="features"></a>Features  

In der folgenden Tabelle werden die WebView2-Features angezeigt, die sich vom Microsoft Edge-Browser unterscheiden.   

*   **Der Standardzustand** gibt an, dass das Feature Teil der Standarderfahrung in einer neuen WebView2-Instanz ist.  
*   **Konfigurierbar gibt** an, dass Sie das Feature mithilfe von WebView2-APIs oder Befehlszeilenschaltern aktivieren oder deaktivieren können.  
    
> [!NOTE]  
> Dieser Artikel behandelt nicht das Ändern von Features mithilfe von Befehlszeilenschaltern.  Weitere Informationen zum Aktivieren und Deaktivieren von Features mit Befehlszeilenschaltern finden Sie unter [Liste der Chromium-Befehlszeilenschalter.][PeterExperimentsChromiumCommandLineSwitches]  
    
| Feature | Standardzustand | Konfigurierbar | Details |  
|:--- |:--- |:--- | :--- |  
| Autofill for Addresses | Ein | Ja | Dieses Feature ist standardmäßig aktiviert, Sie können es mit WebView2 Autofill-APIs aktivieren oder deaktivieren.  |  
| Autofill for Passwords | Ein | Ja | Dieses Feature ist standardmäßig aktiviert, Sie können es mit WebView2 Autofill-APIs aktivieren oder deaktivieren.  |  
| Automatisches Ausfüllen für Zahlungen | Deaktiviert | Nein | Dieses Feature ist deaktiviert.  |  
| Browsererweiterungen | Deaktiviert | Nein | Dieses Feature ist deaktiviert.  |  
| Browser Task Manager | Deaktiviert | Nein | Dieses Feature ist deaktiviert.  |  
| Collections | Deaktiviert | Nein | Dieses Feature ist deaktiviert.  |  
| Continue-where-I-left-off prompt | Deaktiviert | Nein | Dieses Feature ist deaktiviert.  |  
| Downloads | Ein | Ja | WebView2 bietet eine API, mit der Sie die Downloadbenutzeroberfläche anpassen können, um Downloads zu bearbeiten. Sie können beispielsweise blockieren, umleiten, speichern, anhalten und so weiter.  <!--For more information, navigate to [download API][Webview2ReferenceDownloadApi].--> |  
| Edge Shopping | Deaktiviert | Nein | Dieses Feature ist deaktiviert.  |  
| Family Safety | Deaktiviert | Nein | Dieses Feature ist deaktiviert.  |  
| Favorites | Deaktiviert | Nein | Dieses Feature ist deaktiviert.  |  
| IE Mode | Deaktiviert | Nein | Dieses Feature ist deaktiviert.  |  
| Immersive Reader | Deaktiviert | Nein | Dieses Feature hängt von der Browserbenutzeroberfläche für die Interaktion ab.  Dieses Feature ist deaktiviert.  |  
| Intrusive Ads | Deaktiviert | Nein | Dieses Feature ist deaktiviert.  |  
| Tastenkombinationen | Überprüfen von Details | Überprüfen von Details | Die tastenkombinationen, die standardmäßig deaktiviert sind, sind entweder nicht sinnvoll oder verursachen Probleme in WebView2.  Sie können diese Verknüpfungen möglicherweise nicht aktivieren oder deaktivieren.  Stattdessen können Sie mithilfe des Ereignisses auf eine Tastenkombination lauschen und bei Bedarf `AcceleratorKeyPressed` eine benutzerdefinierte Antwort erstellen.  Weitere Informationen finden Sie unter [Weitere Tastenkombinationen.](#additional-keyboard-shortcuts-information) |  
| Pushbenachrichtigungen | Deaktiviert | Nein | Dieses Feature ist in WebView2 nicht implementiert.  Weitere Informationen finden Sie unter [Add support for HTML5 Notification API (#308).][GithubMicrosoftedgeWebview2feedbackIssues308] |  
| Read Aloud | Deaktiviert | Nein | Dieses Feature ist deaktiviert.  |  
| Smart Screen | Ein`*` | Nein | `*` Die Benutzeroberfläche für dieses Feature wurde entfernt, die zugrunde liegende Funktionalität ist jedoch weiterhin verfügbar.  Darüber hinaus können Sie die Option Smart Screen über eine Befehlszeile deaktivieren.  |  
| Translate | Deaktiviert | Nein | Dieses Feature ist deaktiviert.  |  
| Tracking Prevention | Ein`*` | Nein | `*` Die Benutzeroberfläche für dieses Feature wurde entfernt, die zugrunde liegende Funktionalität ist jedoch weiterhin verfügbar.  Die Nachverfolgungsverhütung ist immer auf Ausgeglichen festgelegt.|  
| Profile and Identity | Deaktiviert | Nein | Das Feature, mit dem Ihre Favoriten, Cookies und so weiter synchronisiert werden, ist deaktiviert.  |  
| Web Payment API | Deaktiviert | Nein | Dieses Feature ist deaktiviert.  | 
| Windows Defender Application Guard | Deaktiviert | Nein | Dieses Feature ist deaktiviert.  |  
| edge:// URLs | Überprüfen von Details | Nein | Die Einstellungen für den Microsoft Edge-Browser sind auf `edge://` URLs festgelegt.  Da die meisten dieser Webseiten ein Microsoft Edge-Branding haben oder im Kontext von WebView2 keinen Sinn machen, sind einige dieser URLs deaktiviert.  Weitere Informationen finden Sie unter [Blockierte interne URLs](#blocked-internal-urls).  |  

## <a name="blocked-internal-urls"></a>Blockierte interne URLs  

Die folgenden Webseiten für Microsoft Edge- und Google Chrome-Einstellungen sind in WebView2 nicht verfügbar.  

*   `chrome-search://local-ntp/local-ntp.html`  
*   `edge://application-guard-internals`  
*   `edge://apps`  
*   `edge://compat`  
*   `edge://extensions`  
*   `edge://favorites`  
*   `edge://help`  
*   `edge://management`  
*   `edge://network-error`  
*   `edge://new-tab-page`  
*   `edge://newtab`  
*   `edge://omnibox`  
*   `edge://settings`  
*   `edge://supervised-user-internals`  
*   `edge://version`  

## <a name="additional-keyboard-shortcuts-information"></a>Zusätzliche Informationen zu Tastenkombinationen  

Tastenkombinationen oder Tastenbindungen werden in Microsoft Edge und WebView2 unterstützt.  Wenn Microsoft Edge aktualisiert wird, können sich die Standardschlüsselbindungen ändern.  Darüber hinaus kann eine standardmäßig deaktivierte Tastenkombination aktiviert werden, wenn das Feature jetzt in WebView2 unterstützt wird.  Um Änderungen an den Tastenkombinationen zu vermeiden, können Sie auf festlegen, wodurch alle Tasten, die auf Browserfunktionen zugreifen, deaktiviert werden, aber alle grundlegenden Textbearbeitungs- und Bewegungsverknüpfungen aktiviert `AreBrowserAcceleratorKeysEnabled` `FALSE` bleiben.  

In der folgenden Tabelle sind die Verknüpfungen aufgeführt, die in WebView2 immer deaktiviert sind.  Ein Sternchen \( \) gibt an, dass die Verknüpfung nicht deaktiviert ist, aber das Feature, auf das zugegriffen wird, ist deaktiviert oder gilt nicht für `*` WebView2.  

| Aktion | Windows |  
|:--- |:--- |  
| Hinzufügen zu Favorites | `Ctrl`+`D` |  
| Hinzufügen aller Registerkarten zu Favorites | `Ctrl`+`Shift`+`D` |  
| Fokusspeicherort | `Ctrl`+`L, Alt`+`D` |  
| Einfügen und Los | `Ctrl`+`Shift`+`L` |  
| Datei öffnen | `Ctrl`+`O` |  
| Read Aloud `*` | `Ctrl`+`Shift`+`U` |  
| Webaufnahme `*` | `Ctrl`+`Shift`+`S` |  
| Sidebar `*` | `Ctrl`+`Shift`+`E` |  
| Seite speichern | `Ctrl`+`S` |  
| Auswählen der Registerkarte "Letzte Registerkarte" | `Ctrl`+`9` |  
| Wählen Sie Nächste Registerkarte aus. | `Ctrl`+`Tab` |  
| Auswählen der Registerkarte "Vorherige Registerkarte" | `Ctrl`+`Shift`+`Tab` |  
| Tab auswählen \(1 - 8\) | `Ctrl`+`(1-8)` |  
| Leiste Favorites anzeigen `*` | `Ctrl`+`Shift`+`B` |  
| Hilfe | `F1` |  
| Nächster Fokusbereich `*` | `F6` |  
| Fokus vorheriger Bereich `*` | `Shift`+`F6` |  
| Caret Browsing `*` | `F7` |  
| Leseansicht `*` | `F9` |  
| Fokusmenüleiste | `F10` |  
| Menü "Identität anzeigen" `*` | `Ctrl`+`Shift`+`M` |  
| Browser Task Manager `*` | `Shift`+`Escape` |  
| Edgefeedback `*` | `Shift`+`Alt`+`I` |  
| Registerkarte "Stummschalten" `*` | `Ctrl`+`M` |  
| Neues Incognito-Fenster | `Ctrl`+`Shift`+`N` |  
| Neue Registerkarte | `Ctrl`+`T` |  
| Neues Fenster | `Ctrl`+`N` |  
| Letzte geschlossene Registerkarte wiederherstellen | `Ctrl`+`Shift`+`T` |  
| Fokus Favorites | `Alt`+`Shift`+`B` |  
| Fokus Inaktives Popup | `Alt`+`Shift`+`A` |  
| Fokussuche | `Ctrl`+`E`, `Ctrl`+`K`, `Search Key` |  
| Registerkarte "Duplikate" | `Ctrl`+`Shift`+`K` |  
| Fokussymbolleiste `*` | `Alt`+`Shift`+`T` |  
| Startseite | `Alt`+`Home`, `Browser Home Key` |  
| Menü "App anzeigen" | `Alt`+`E, Alt`+`F` |  
| Anzeigen Favorites | `Ctrl`+`Shift`+`O` |  
| Anzeigen Downloads | `Ctrl`+`J` |  
| Anzeigen des Verlaufs | `Ctrl`+`H` |  
| Anzeigen der Lesemodusleiste `*` | `Shift`+`Alt`+`R` |  
| Anzeigen Collections `*` | `Ctrl`+`Shift`+`Y` |  

Die folgenden Tastenkombinationen sind immer deaktiviert, außer in Fenstern, die angezeigt werden, wenn das Ereignis `NewWindowRequested` nicht behandelt wird.

| Aktion | Windows |  
|:--- |:--- |  
| Registerkarte Schließen | `Ctrl`+`W, Ctrl`+`F4` |  
| Fenster schließen | `Ctrl`+`Shift`+`W` |  
| Vollbild | `F11` |  

Wenn Sie auf `AreBrowserAcceleratorKeysEnabled` `FALSE` festlegen, sind die folgenden zusätzlichen Tastenkombinationen deaktiviert.  

| Aktion | Windows |  
|:--- |:--- |  
| Stop | `Escape` |  
| Auf Seite suchen | `Ctrl`+`F` |  
| Find Next | `Ctrl`+`G` |  
| Vorherige Suche | `Ctrl`+`Shift`+`G` |  
| Drucken | `Ctrl`+`P` |  
| Aktualisieren | `Ctrl`+`R`, `F5`, `Reload Key` |  
| Aktualisieren ohne Cache | `Ctrl`+`Shift`+`R`, `Ctrl`+`F5`, `Shift`+`F5`, `Ctrl`+`Refresh`, `Shift`+`Refresh` |  
| Verkleinern | `Ctrl`+`-` |  
| Vergrößern | `Ctrl`+`+` |  
| Zoom zurücksetzen | `Ctrl`+`0` |  
| Find Next | `F3` |  
| Vorherige Suche | `Shift`+`F3` |  
| Zurück | `Alt`+`Left, Browser Back Key` |  
| Vorwärts | `Alt`+`Right`, `Browser Forward Key` |  
| Drucken | `Ctrl`+`P` |  
| Öffnen /Schließen von DevTools | `Ctrl`+`Shift`+`I` |  
| Öffnen der DevTools-Konsole | `Ctrl`+`Shift`+`J` |  
| Öffnen von DevTools Inspect | `Ctrl`+`Shift`+`C` |  

> [!Note] 
> Verwenden Sie das [AcceleratorKeyPressed-Ereignis,][DotnetApiMicrosoftWebWebview2CoreCorewebview2controllerAcceleratorkeypressedViewWebview2Dotnet1077444] um einen der Schlüssel einzeln anzupassen.  

## <a name="getting-in-touch-with-the-microsoft-edge-webview2-team"></a>Kontakt mit dem Microsoft Edge WebView2-Team  

[!INCLUDE [contact WebView2 team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

<!--[Webview2ReferenceDownloadApi]: ./download-api.md "download API | Microsoft Docs"  -->  

[DotnetApiMicrosoftWebWebview2CoreCorewebview2controllerAcceleratorkeypressedViewWebview2Dotnet1077444]: /dotnet/api/microsoft.web.webview2.core.corewebview2controller.acceleratorkeypressed?view=webview2-dotnet-1.0.774.44&preserve-view=true "CoreWebView2Controller.AcceleratorKeyPressed-Ereignis | Microsoft Docs"  

[DevtoolsShortcutsIndex]: ../../devtools-guide-chromium/shortcuts/index.md "Microsoft Edge DevTools-Tastenkombinationen | Microsoft Docs"  

[GithubMicrosoftedgeWebview2feedbackIssues308]: https://github.com/MicrosoftEdge/WebView2Feedback/issues/308 "Hinzufügen von Unterstützung für html5 Notification API (#308) | GitHub"  

[PeterExperimentsChromiumCommandLineSwitches]: https://peter.sh/experiments/chromium-command-line-switches "Liste der Chromium-Befehlszeilenschalter | Peter Beverloo"  
