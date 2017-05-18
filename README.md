# Visual Studio Code als zentrale Entwicklungsumgebung
Dieses Dokument dient mir als Gedächtnisstütze für die Verwendung von Microsoft Visual Studio Code (im folgenden als __VS Code__ bezeichnet) als zentrales Entwicklungswerkzeug für verschiedene Platformen.

Neben den Themen die sich direkt auf VS Code beziehen finden sich weitere Themengebiete die mittel- oder unmittelbar in Zusammenhang mit VS Code stehen.

Im wesentlichen faßt dieses Dokument bestehendes Wissen aus unterschiedlichen Quellen zusammen und wird durch eigene Erfahrungen/Ideen ergänzt.


## Bezug und Installation von Visual Studio Code
Installationspakete können direkt von der [Webseite](https://code.visualstudio.com/) herunter geladen werden. Die Webseite von Visual Studio Code findet man bequem über eine Recherche bei einer Suchmaschine, z.B. [Google](https://www.google.de/search?q=Visual+Studio+Code) oder [Bing](http://www.bing.com/search?q=Visual+Studio+Code).

Installationspakete für verschiedene Platformen stehen zum [herunterladen](https://code.visualstudio.com/Download) zur Verfügung.

* [Microsoft Windows](https://code.visualstudio.com/docs/?dv=win)
* [Apple macOS](https://code.visualstudio.com/docs/?dv=osx)
* verschiedene Linux-Derivate [(Debian, Ubuntu)](https://code.visualstudio.com/docs/?dv=linux64_deb) oder [(RedHat, Fedora, SUSE)](https://code.visualstudio.com/docs/?dv=linux64_rpm)

Die oben angegebenen Links beschreiben auch gleich wie die Installation auf der jeweiligen Platform durchgeführt wird.

## Wichtige Tastenkombinationen

|Kombination DE |Kombination EN |Kombination MAC |Funktion |
|:- |:- |:- |:- |
|STRG+UMSCH+P | | |Eingabefeld für Aktionen öffnen |
|UMSCH+ALT+F | | |Dokument formatieren |
|STRG+ö| | |Integriertes Terminal anzeigen|

## Funktionsvielfalt durch _Extensions_
VS Code läßt sich mit Hilfe von [Extensions](https://code.visualstudio.com/docs/editor/extension-gallery) um zusätzliche Funktionen bereichern. Es existieren eine Vielzahl von Erweiterungen wie Debugger, Sprachuntersützung, Workflow-Werkzeuge, ...

Das notwendige Verwaltungswerkzeug ist von Anfang an in VS Code enthalten und erleichtert die Suche, Installation und Aktualisierung dieser Erweiterungen.

## Einstellungen von Visual Studio Code
Nach der Installation präsentiert sich VS Code mit einer dunkel gehaltenen Benutzeroberfläche. Da dies für mich nicht so angenehm wie eine helle Darstellung ist, ändere ich das ``colorTheme`` in den Einstellungen ab. Dabei nehme ich noch ein paar zusätzliche Einstellungen vor

Hier die ``settings.json`` Datei die von mir verwendet wird:
```json
{
    "editor.fontSize": 12,
    "editor.tabSize": 2,
    "editor.insertSpaces": true,
    "workbench.colorTheme": "Default Light+",
    "workbench.sideBar.location": "right"
}
```

## Vorgaben für die Formatierung von C# Quelltext
Um die Formatierung des Quelltextes meinen Vorstellungen ensprechend zu erreichen lege ich in das Projektverzeichnis eine Konfigurationsdatei für [OmniSharp](http://www.omnisharp.net/).

Mit Hilfe dieser Datei ``omnisharp.json`` kann OmniSharp den Quelltext im Editor passend formatieren.

``omnisharp.json``
```json
{
    "FormattingOptions": {
            "NewLine": "\n",
            "UseTabs": false,
            "TabSize": 2,
            "IndentationSize": 2,
            "SpacingAfterMethodDeclarationName": false,
            "SpaceWithinMethodDeclarationParenthesis": false,
            "SpaceBetweenEmptyMethodDeclarationParentheses": false,
            "SpaceAfterMethodCallName": false,
            "SpaceWithinMethodCallParentheses": false,
            "SpaceBetweenEmptyMethodCallParentheses": false,
            "SpaceAfterControlFlowStatementKeyword": true,
            "SpaceWithinExpressionParentheses": false,
            "SpaceWithinCastParentheses": false,
            "SpaceWithinOtherParentheses": false,
            "SpaceAfterCast": false,
            "SpacesIgnoreAroundVariableDeclaration": false,
            "SpaceBeforeOpenSquareBracket": false,
            "SpaceBetweenEmptySquareBrackets": false,
            "SpaceWithinSquareBrackets": false,
            "SpaceAfterColonInBaseTypeDeclaration": true,
            "SpaceAfterComma": true,
            "SpaceAfterDot": false,
            "SpaceAfterSemicolonsInForStatement": true,
            "SpaceBeforeColonInBaseTypeDeclaration": true,
            "SpaceBeforeComma": false,
            "SpaceBeforeDot": false,
            "SpaceBeforeSemicolonsInForStatement": false,
            "SpacingAroundBinaryOperator": "single",
            "IndentBraces": false,
            "IndentBlock": true,
            "IndentSwitchSection": true,
            "IndentSwitchCaseSection": true,
            "LabelPositioning": "oneLess",
            "WrappingPreserveSingleLine": true,
            "WrappingKeepStatementsOnSingleLine": true,
            "NewLinesForBracesInTypes": false,
            "NewLinesForBracesInMethods": false,
            "NewLinesForBracesInProperties": false,
            "NewLinesForBracesInAccessors": false,
            "NewLinesForBracesInAnonymousMethods": false,
            "NewLinesForBracesInControlBlocks": false,
            "NewLinesForBracesInAnonymousTypes": false,
            "NewLinesForBracesInObjectCollectionArrayInitializers": false,
            "NewLinesForBracesInLambdaExpressionBody": false,
            "NewLineForElse": false,
            "NewLineForCatch": true,
            "NewLineForFinally": true,
            "NewLineForMembersInObjectInit": true,
            "NewLineForMembersInAnonymousTypes": true,
            "NewLineForClausesInQuery": true
    }
}
```

``Tip:`` Mit der Tastenkombination ``UMSCH+ALT+F`` kann die Formatierung ausgelöst werden.


## Beliebte Erweiterungen
Hier sind ein paar Erweiterungen genannt, die ich als lohnenswert erachte:

* Markdown All in One (Yu Zhang)
* C# (Microsoft)


## Markdown Dokumente bearbeiten
In VS Code lassen sich Dateien im [Markdown](https://en.wikipedia.org/wiki/Markdown)-Format einfach bearbeiten. Markdown ist eine Art den Inhalt eines Dokumentes zu formatieren ohne dabei mit Hilfe aufweniger Formatierungstechniken konfrontiert zu werden. Weiterer Vorteil ist, dass Dokumente im Markdown-Stil auch ohne die vorgesehene Formatierung _lesbar_ bleiben.

Ein sehr gutes Werkzeug für die Erstellung von Markdown-Dokumenten ist die Erweiterung __Markdown All in One__ von _Yu Zhang_

``Tip:`` Mit der Tastenkombination CTRL+SHIFT+V (Deutsch: STRG+UMSCH+V) wird ein Vorschaufenster geöffnet. In diesem Vorschaufenster wird das Markdown Dokument mit Formatierung angezeigt. 

``Tip:`` Über die Tastenkombination CTRL+^ (Deutsch: STRG+^) kann das Editorfenter in eine linke und rechte Hälfte geteilt werden. So kann das Markdown-Dokument und die Vorschau nebeneinander dargestellt werden.


# VS Code und Node.js
[Node.js](https://nodejs.org/) ist eine Platform um leistungsfähige und skalierbare Serveranwendungen in JavaScript zu erstellen. Node.js ist das Laufzwitmodul und [NP](https://www.npmjs.com/) die dazu gehörige Paketverwaltung.

VS Code besitzt eine eingebaute Unterstützung für Javascript und TypeScript sowie das Debuggen von Node.js Programmcode.

Eine sehr gute Anleitung (allerdings in englischer Sprache) wie in VS Code mit Node.js und NPM gearbeitet wird findet man unter [Node.js Tutorial in VS Code ](https://code.visualstudio.com/docs/nodejs/nodejs-tutorial).

# NPM Basiswissen

|Befehl |Erklärung |
|:- |:- |
|npm install |Installiert benötigte Abhängigkeiten in ``./node_modules`` |
|npm build |Erstell die Node.js Anwendung |
|npm start|Startet die Anwendung gemäß Festlegung im Wert ``XXXX`` der Datei ``package.json``|

