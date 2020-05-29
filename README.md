# Dokumentation für Microsoft Edge

## Microsoft Open-Source-Code of Conduct

Dieses Projekt hat den [Microsoft Open-Source-Code of Conduct](https://opensource.microsoft.com/codeofconduct/)übernommen.
Weitere Informationen finden Sie im [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) oder Kontakt [opencode@Microsoft.com](mailto:opencode@microsoft.com) mit weiteren Fragen oder Kommentaren.

## Rechtliche Hinweise
Microsoft und alle Mitwirkenden gewähren Ihnen eine Lizenz für die Microsoft-Dokumentation und andere Inhalte in diesem Repository im Rahmen der [Creative Commons Namensgebung 4.0 International Public License](https://creativecommons.org/licenses/by/4.0/legalcode), siehe Datei [LIZENZ](LICENSE), sowie eine Lizenz für den gesamten Code in dem Repository im Rahmen der [MIT-Lizenz](https://opensource.org/licenses/MIT), siehe Datei [LIZENZCODE](LICENSE-CODE).

Microsoft, Windows, Microsoft Azure und/oder andere Microsoft-Produkte und -Dienste, auf die in der Dokumentation verwiesen wird, sind möglicherweise Marken oder eingetragene Marken von Microsoft in den USA und/oder anderen Ländern.
Die Lizenzen für dieses Projekt berechtigen Sie nicht dazu, Microsoft-Namen, -Logos oder -Marken zu verwenden.
Die allgemeinen Markenrichtlinien von Microsoft finden Sie unter https://go.microsoft.com/fwlink/?LinkID=254653 .

Datenschutzinformationen finden Sie unterhttps://privacy.microsoft.com

Microsoft und die Beitragenden behalten sich alle weiteren Rechte vor, ob gemäß den jeweiligen Urheber-, Patent- oder Markenrechten oder ob implizit, durch rechtshemmenden Einwand oder anderweitig.

## Beitragen

Dies ist das Repository für Microsoft Edge- **Dokumentation** , die unter gehostet wird [https://docs.microsoft.com/microsoft-edge/](https://docs.microsoft.com/microsoft-edge/) .

Wenn Sie eine neue Berichterstattung sehen oder Feedback haben möchten, sollten Sie [**einen Beitrag**](/CONTRIBUTING.md)leisten.  Sie können die vorhandenen Inhalte bearbeiten, neue Inhalte hinzufügen oder einfach neue [Probleme](https://github.com/MicrosoftDocs/edge-developer/issues)erstellen. Wir werden uns mit ihren Vorschlägen befassen und zusammenarbeiten, um Sie in die Dokumente einzubeziehen.

Suchen Sie die Daten für die [`Status`](https://dev.windows.com/microsoft-edge/platform/status/) Seite unter: https://github.com/MicrosoftEdge/Status . Die `Status` Seite bietet den neuesten Implementierungsstatus und zukünftige Pläne für Features für Webplattformen in Microsoft Edge.

### Konventionen

- Wenn Sie eine Seite hinzufügen, müssen Sie in [TOC.MD](microsoft-edge/toc.md) einen Eintrag hinzufügen, damit Sie angezeigt wird.
- Ein Ordner kann mehr Ordner oder `readme.md` s enthalten
- Ordner-oder Verzeichnisnamen sind Bindestrich getrennte (z.b. `f12-tools` ) und Kleinbuchstaben. Sie werden in URLs auf der docs.Microsoft.com-Website verwendet. Verwenden Sie keine Unterstriche oder PascalCase/CamelCase.

### Andere Textelemente

Für diese anderen Textelemente steht das Design zur Verfügung:

* Ungeordnete Listen
* Haben Sie regelmäßige Aufzählungszeichen
   * Sie können auch Aufzählungszeichen verschachteln.
   * Aufzählungslisten sollten mehr als einen Eintrag aufweisen.
* Ziemlich Standard

1. Geordnete Listen.
2. Verwenden Sie die normale OL-Nummerierung in westlicher Formatvorlage.
3. Sollte nur verwendet werden, wenn eine Liste wirklich Ordnung aufweist.

_________________________

Es stehen horizontale Regeln zur Verfügung. Wir empfehlen, Sie sparsam zu verwenden, um das Chaos zu verringern.
Kombinieren Sie keine horizontalen Regeln mit Überschriften-Tags; einige bereits verwendete Linienarten für die visuelle Hierarchie.

### Anzeigen von Code

Sie können die Inline `code` -Abzugs Syntax (mit den Backticks) verwenden.

Oder Sie können Codeblöcke wie folgt anzeigen:

```css
body {
    background: #fff;
}
```

### Tabellen

| Sie können     | Verwenden von Überschriften | in Tabellen    |
|-------------|-------------|-------------:|
| Linksbündig| Es sei denn, ein #  | 456          |
| Textwert  | Mehr Text   | $0,00        |

### Anmerkungen

Verwenden Sie Notizen sparsam. Es handelt sich um Blöcke, die dazu dienen, "nicht verpassen"-Informationen hervorzuheben.

Es gibt vier verschiedene Versionen von Notizen, die derzeit formatiert sind:
- HINWEIS
- Warnung
- Tipp
- WICHTIG

Diese sehen wie folgt aus:

![Notiz Muster](./media/notes.png)

```
> [!WARNING]
> Hello. Yes. I am a warning note that has been automagically created. My text may wrap to more than one line when the Markdown is parsed, but I must include all my information within a single (sometimes very long line) in the Markdown itself.```

For multi-line blockquote notes, use a > in front of each line of the notes as seen in the example below.

```


### Images

Bilder sollten in einem Ordner gespeichert `media` und mit einem relativen Pfad referenziert werden:

`![Note patterns](media/notes.png)`
