# <a name="microsoft-edge-documentation"></a>Dokumentation für Microsoft Edge  

## <a name="microsoft-open-source-code-of-conduct"></a>Microsoft Open Source Code of Conduct  

Dieses Projekt hat den [Microsoft Open Source Code of Conduct übernommen.](https://opensource.microsoft.com/codeofconduct)  
Weitere Informationen finden Sie unter [Häufig gestellte](https://opensource.microsoft.com/codeofconduct/faq) Fragen zum Code of Conduct [oder](mailto:opencode@microsoft.com) opencode@microsoft.com mit weiteren Fragen oder Kommentaren.  

## <a name="legal-notices"></a>Rechtliche Hinweise  

Microsoft und alle Mitwirkenden gewähren Ihnen eine Lizenz für die Microsoft-Dokumentation und andere Inhalte in diesem Repository unter der [Creative Commons Attribution 4.0 International Public License,](https://creativecommons.org/licenses/by/4.0/legalcode)navigieren Sie zur [LIZENZdatei,](./LICENSE) und erteilen Sie Ihnen eine Lizenz für jeden Code im Repository unter der [MIT-Lizenz,](https://opensource.org/licenses/MIT)navigieren Sie zur [LIZENZ-CODE-Datei.](./LICENSE-CODE)  

Microsoft, Windows, Microsoft Azure und/oder andere Microsoft-Produkte und -Dienste, auf die in der Dokumentation verwiesen wird, sind möglicherweise Marken oder eingetragene Marken von Microsoft in den USA und/oder anderen Ländern.  
Die Lizenzen für dieses Projekt berechtigen Sie nicht dazu, Microsoft-Namen, -Logos oder -Marken zu verwenden.  
Allgemeine Markenrichtlinien von Microsoft finden Sie unter [https://go.microsoft.com/fwlink/?LinkID=254653](https://go.microsoft.com/fwlink/?LinkID=254653) .  

Datenschutzinformationen finden Sie unter [https://privacy.microsoft.com](https://privacy.microsoft.com) .  

Microsoft und die Beitragenden behalten sich alle weiteren Rechte vor, ob gemäß den jeweiligen Urheber-, Patent- oder Markenrechten oder ob implizit, durch rechtshemmenden Einwand oder anderweitig.  

## <a name="contributing"></a>Mitwirken  

Dies ist das Repository für Microsoft **Edge-Dokumentation, das** unter gehostet [https://docs.microsoft.com/microsoft-edge/](https://docs.microsoft.com/microsoft-edge/index) wird.  

Wenn Sie eine neue Abdeckung enthalten möchten oder Feedback haben möchten, sollten Sie einen [Beitrag leisten.](./CONTRIBUTING.md)  Sie können den vorhandenen Inhalt bearbeiten, neue Inhalte hinzufügen oder neue Probleme [erstellen.](https://github.com/MicrosoftDocs/edge-developer/issues)  Das Microsoft Edge-Team überprüft Ihre Vorschläge und arbeitet an der Integration der Vorschläge in die Dokumente.  

Suchen Sie die Daten für die [Seite Status](https://developer.microsoft.com/microsoft-edge/status) unter:  [https://github.com/MicrosoftEdge/Status](https://github.com/MicrosoftEdge/Status) .  Die `Status` Seite enthält den neuesten Implementierungsstatus und zukünftige Pläne für Webplattformfeatures in Microsoft Edge.

### <a name="conventions"></a>Konventionen  

*   Wenn Sie eine Seite hinzufügen, müssen Sie einen Eintrag für sie [in](./microsoft-edge/toc.yml) toc.md hinzufügen, damit sie angezeigt wird.
*   Ein Verzeichnis kann mehr Verzeichnisse oder `readme.md` s enthalten
*   Ordner-/Verzeichnisnamen sind durch Strich getrennt \(z. B. `f12-tools` \) und Kleinbuchstaben.  Verzeichnisse werden in URLs auf der Website `docs.microsoft.com` verwendet.  Vermeiden Sie die Verwendung von Unterstrichen, PascalCase oder camelCase.  

### <a name="other-text-elements"></a>Andere Textelemente  

Für diese anderen Textelemente ist eine Formatierung verfügbar:  

*   Ungeordnete Listen  
*   Regelmäßige Aufzählungszeichen haben  
    *   Sie können auch Aufzählungszeichen schachteln.  
    *   Aufzählungslisten sollten mehr als einen Eintrag enthalten.  
*   Standardanordnung 

1.  Geordnete Listen.  
1.  Verwenden Sie die reguläre Nummerierung im westlichen Stil.  
1.  Sollte nur verwendet werden, wenn eine Liste wirklich über Eine Reihenfolge verfügt.  

---  

Horizontale Regeln sind verfügbar.  Verwenden Sie horizontale Regeln sparsam, um Unübersichtlichkeit zu reduzieren.  
Vermeiden Sie die Verwendung horizontaler Regeln mit Überschriftentags. Einige Überschriften verwenden bereits Linienformatvorlagen für die visuelle Hierarchie.  

### <a name="displaying-code"></a>Anzeigen von Code  

Sie können die `code` Inline-Markdown-Syntax \(mit den Backticks\) verwenden.  

Oder Sie können Codeblöcke anzeigen.  Der folgende Codeausschnitt ist ein CSS-Beispiel.  

```css
body {
    background: #fff;
}
```  

### <a name="tables"></a>Tabellen  

| Sie können sich bei Ihrem Konto | Verwenden von Kopfzeilen | in Tabellen |  
|:--- |:--- |:--- |  
| Linksbündig ausgerichtet | Es sei denn, ein # | 456 |  
| Textwert | Mehr Text | $0.00 |  

### <a name="notes"></a>Anmerkungen  

Verwenden Sie Notizen sparsam.  Die Blöcke sind so konzipiert, dass sie "Don't-miss-it"-Informationen hervorheben.  

Vier verschiedene Versionen von Notizen werden derzeit gestylt.  

*   HINWEIS  
*   WARNUNG  
*   TIPP  
*   WICHTIG  

Die Notizen sehen jeweils wie die folgenden Codeausschnitte aus.  

```md
> [!NOTE]
> This is a NOTE  
```  

```md
> [!WARNING]
> This is a WARNING  
```  

```md
> [!TIP]
> This is a TIP  
```  

```md
> [!IMPORTANT]
> This is IMPORTANT  
```  

![Notizmuster](./media/notes.png)

Verwenden Sie für mehrzeilerige Blockquotenotizen ein Größer-als\( \)-Zeichen vor jeder Zeile der Notizen, wie im folgenden `>` Beispiel dargestellt.  

```md
> This is a line in a blockquote.  
> My text may wrap to more than one line when the Markdown is parsed, but I must include all my information within a single \(sometimes very long line\) in the Markdown.  
> This is another line in a blockquote.  
```

### <a name="images"></a>Images  

Bilder sollten in einem Verzeichnis gespeichert und mithilfe eines `media` Bildskripts mit einem relativen Pfad referenziert werden.  

<!--  `![Note patterns](media/notes.png)`  -->  

```md
:::image type="complex" source="./media/notes.png" alt-text="Note patterns" lightbox="./media/notes.png":::
   Note patterns  
:::image-end:::  
```  
