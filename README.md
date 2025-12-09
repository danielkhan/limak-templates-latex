# LIMAK LaTeX Templates

> **ℹ️ Hinweis**: Dies ist **kein offizielles Repository** der Johannes Kepler Universität Linz oder der LIMAK Austrian Business School. Diese Vorlagen basieren auf dem [JKU Templates Report LaTeX](https://github.com/michaelroland/jku-templates-report-latex) Repository und wurden für LIMAK-spezifische Anforderungen angepasst.

Professionelle LaTeX-Vorlagen für wissenschaftliche Arbeiten an der **LIMAK Austrian Business School** (Johannes Kepler Universität Linz).

Diese Vorlagen entsprechen den offiziellen LIMAK-Richtlinien und ermöglichen die Erstellung wissenschaftlicher Arbeiten mit professionellem Layout.

## 📚 Enthaltene Vorlagen

| Vorlage | Verwendung | Umfang | Struktur |
|---------|------------|--------|----------|
| **limak-thesis-latex/** | Master Thesis (Masterarbeit) | 60+ Seiten | 9 Kapitel |
| **limak-transferarbeit-latex/** | Transferarbeit (Praxistransfer) | 10-20 Seiten | 5 Abschnitte |

---

## 🚀 Schnellstart

> **💡 Hinweis**: Dieser Schnellstart ist für Nutzer, die bereits mit **LaTeX und VS Code** vertraut sind. Wenn du LaTeX zum ersten Mal verwendest, springe direkt zu [💻 Installation](#-installation) für eine ausführliche Anleitung.

### Vorlage herunterladen

**Option 1: Download als ZIP**
1. Klicke auf den grünen "Code"-Button oben rechts
2. Wähle "Download ZIP"
3. Entpacke das ZIP-Archiv an einem geeigneten Ort

**Option 2: Git Clone** (für fortgeschrittene Benutzer)
```bash
git clone https://github.com/danielkhan/limak-templates-latex
cd limak-templates-latex
```

### Erste Schritte (für erfahrene LaTeX-Nutzer)

1. **Wähle die passende Vorlage:**
   - **Master Thesis**: Ordner `limak-thesis-latex/`
   - **Transferarbeit**: Ordner `limak-transferarbeit-latex/`

2. **Öffne die Hauptdatei in VS Code:**
   - Öffne VS Code → `Datei` → `Ordner öffnen...`
   - Wähle den Template-Ordner (z.B. `limak-thesis-latex/`)
   - Klicke auf die Hauptdatei:
     - Master Thesis: `main-limak-thesis.tex`
     - Transferarbeit: `main-transferarbeit.tex`

3. **Kompiliere das Dokument:**
   - Mit XeLaTeX kompilieren (bereits konfiguriert in `.vscode/settings.json`)
   - In VS Code: Speichern (`Strg+S` / `Cmd+S`) oder Play-Icon (▶) klicken
   - Detaillierte Anleitung: [📝 Kompilierung](#-kompilierung)

4. **Passe die Vorlage an:**
   - Metadaten in der Hauptdatei anpassen (Titel, Name, etc.)
   - Kapitel-Dateien bearbeiten
   - Literaturverzeichnis in `references.bib` pflegen

---

## 💻 Installation

### Windows

#### Schritt 1: LaTeX-Distribution installieren

**Empfohlen: MiKTeX** (einfacher für Einsteiger)

1. **Download**: Gehe auf [miktex.org/download](https://miktex.org/download)
2. **Installation**:
   - Lade den "Basic MiKTeX Installer" herunter
   - Führe die .exe-Datei aus
   - Wähle "Install MiKTeX for all users" (empfohlen) oder "Install MiKTeX for me only"
   - Installationspfad: Standard beibehalten (z.B. `C:\Program Files\MiKTeX`)
   - Package Installation: Wähle "Yes" für automatische Installation fehlender Pakete

3. **Nach Installation**:
   - Öffne die MiKTeX Console (Windows-Suche: "MiKTeX Console")
   - Klicke unter "Updates" auf "Check for updates"
   - Installiere alle verfügbaren Updates

**Alternative: TeX Live**

1. **Download**: [tug.org/texlive/acquire-netinstall.html](https://www.tug.org/texlive/acquire-netinstall.html)
2. **Installation**:
   - Lade `install-tl-windows.exe` herunter
   - Führe die Datei als Administrator aus
   - Wähle "Full installation" (ca. 7 GB)
   - Installation dauert 30-60 Minuten

#### Schritt 2: VS Code installieren und konfigurieren

**Visual Studio Code** mit LaTeX Workshop Extension:

1. **VS Code installieren**:
   - Download: [code.visualstudio.com](https://code.visualstudio.com/)
   - Führe den Installer aus (Standard-Installation)

2. **Projekt in VS Code öffnen**:
   - Öffne VS Code
   - Wähle `Datei` → `Ordner öffnen...`
   - Wähle den `LIMAK-Masterthesis-Template` Ordner aus
   - VS Code schlägt automatisch vor, die empfohlene Extension zu installieren

3. **LaTeX Workshop Extension installieren**:
   - Wenn du das Projekt öffnest, erscheint eine Meldung: "Dieses Repository empfiehlt Extensions"
   - Klicke auf "Installieren" oder "Alle anzeigen und installieren"
   - **Alternativ manuell**: Extensions-Icon (linke Seitenleiste) → Suche "LaTeX Workshop" → Installieren

4. **Kompilieren** (ohne weitere Konfiguration nötig!):
   - Öffne `main-limak-thesis.tex` oder `main-transferarbeit.tex`
   - Speichere die Datei (Strg+S) - LaTeX Workshop kompiliert automatisch
   - Oder klicke auf das grüne Play-Icon (▶) oben rechts
   - Das PDF wird automatisch im VS Code Tab angezeigt

> **💡 Hinweis**: Die XeLaTeX-Konfiguration ist bereits im Projekt enthalten (`.vscode/settings.json`). Du musst nichts manuell konfigurieren!

#### Schritt 3: Claude Code installieren (optional, aber empfohlen)

**Claude Code** ([claude.code](https://claude.ai/code)) ist ein KI-Assistent, der dir beim Bearbeiten deiner Arbeit helfen kann.

1. **VS Code Extension installieren**:
   - Öffne VS Code
   - Gehe zu Extensions (linke Seitenleiste oder `Strg+Shift+X`)
   - Suche nach "Claude Code"
   - Klicke auf "Install"

2. **Mit Claude.ai verbinden**:
   - Nach Installation: Klicke auf das Claude-Icon in der Seitenleiste
   - Folge den Anweisungen zur Anmeldung
   - Wähle deinen Plan (kostenlos oder Pro)

3. **Claude starten**:
   - Drücke `Strg+Shift+P` und wähle "Claude Code: Start Chat"
   - Oder klicke auf das Claude-Icon in der Seitenleiste

> **⚠️ Wichtig**: Claude Code ist für **technische LaTeX-Unterstützung** - nicht für wissenschaftliche Inhalte! Siehe [KI-NUTZUNG.md](KI-NUTZUNG.md) für Richtlinien.

#### Schritt 4: Arial-Schriftart prüfen

Arial ist unter Windows standardmäßig installiert. Zur Sicherheit prüfen:

1. Öffne die Windows-Systemsteuerung
2. Gehe zu `Darstellung und Anpassung` → `Schriftarten`
3. Suche nach "Arial"
4. Falls nicht vorhanden: Arial ist in Microsoft Office enthalten

---

### macOS

#### Schritt 1: LaTeX-Distribution installieren

**MacTeX** (empfohlen für macOS)

1. **Download**: Gehe auf [tug.org/mactex](https://www.tug.org/mactex/)
2. **Installation**:
   - Lade `MacTeX.pkg` herunter (ca. 5 GB)
   - Doppelklicke auf die .pkg-Datei
   - Folge dem Installationsassistenten
   - Installation dauert 10-20 Minuten
   - **Wichtig**: Nach Installation öffne das Terminal und gib ein:
     ```bash
     sudo tlmgr update --self
     sudo tlmgr update --all
     ```

#### Schritt 2: VS Code installieren und konfigurieren

**Visual Studio Code** mit LaTeX Workshop Extension:

1. **VS Code installieren**:
   - Download: [code.visualstudio.com](https://code.visualstudio.com/)
   - Lade die macOS .dmg-Datei herunter
   - Öffne die .dmg und ziehe VS Code in den Programme-Ordner

2. **Projekt in VS Code öffnen**:
   - Öffne VS Code
   - Wähle `Datei` → `Ordner öffnen...`
   - Wähle den `LIMAK-Masterthesis-Template` Ordner aus
   - VS Code schlägt automatisch vor, die empfohlene Extension zu installieren

3. **LaTeX Workshop Extension installieren**:
   - Wenn du das Projekt öffnest, erscheint eine Meldung: "Dieses Repository empfiehlt Extensions"
   - Klicke auf "Installieren" oder "Alle anzeigen und installieren"
   - **Alternativ manuell**: Extensions-Icon (linke Seitenleiste) → Suche "LaTeX Workshop" → Installieren

4. **Kompilieren** (ohne weitere Konfiguration nötig!):
   - Öffne `main-limak-thesis.tex` oder `main-transferarbeit.tex`
   - Speichere die Datei (Cmd+S) - LaTeX Workshop kompiliert automatisch
   - Oder klicke auf das grüne Play-Icon (▶) oben rechts
   - Das PDF wird automatisch im VS Code Tab angezeigt

> **💡 Hinweis**: Die XeLaTeX-Konfiguration ist bereits im Projekt enthalten (`.vscode/settings.json`). Du musst nichts manuell konfigurieren!

#### Schritt 3: Claude Code installieren (optional, aber empfohlen)

**Claude Code** ([claude.code](https://claude.ai/code)) ist ein KI-Assistent, der dir beim Bearbeiten deiner Arbeit helfen kann.

1. **VS Code Extension installieren**:
   - Öffne VS Code
   - Gehe zu Extensions (linke Seitenleiste oder `Cmd+Shift+X`)
   - Suche nach "Claude Code"
   - Klicke auf "Install"

2. **Mit Claude.ai verbinden**:
   - Nach Installation: Klicke auf das Claude-Icon in der Seitenleiste
   - Folge den Anweisungen zur Anmeldung
   - Wähle deinen Plan (kostenlos oder Pro)

3. **Claude starten**:
   - Drücke `Cmd+Shift+P` und wähle "Claude Code: Start Chat"
   - Oder klicke auf das Claude-Icon in der Seitenleiste

> **⚠️ Wichtig**: Claude Code ist für **technische LaTeX-Unterstützung** - nicht für wissenschaftliche Inhalte! Siehe [KI-NUTZUNG.md](KI-NUTZUNG.md) für Richtlinien.

#### Schritt 4: Arial-Schriftart prüfen

Arial ist unter macOS standardmäßig installiert. Zur Sicherheit prüfen:

```bash
fc-list | grep -i arial
```

Falls Arial nicht gefunden wird:
- Arial ist in Microsoft Office für Mac enthalten
- Oder lade Arial aus dem macOS Font Book herunter

---

## 📝 Kompilierung

### Automatische Kompilierung in VS Code

Mit der LaTeX Workshop Extension kompiliert VS Code automatisch:

1. **Öffne die Hauptdatei**:
   - `main-limak-thesis.tex` (Master Thesis)
   - `main-transferarbeit.tex` (Transferarbeit)

2. **Kompilierung starten**:
   - **Automatisch beim Speichern**: Drücke `Strg+S` (Windows) oder `Cmd+S` (macOS)
   - **Manuell**: Klicke auf das grüne Play-Icon (▶) oben rechts
   - Oder nutze die Command Palette (`Strg+Shift+P`): "LaTeX Workshop: Build LaTeX project"

3. **PDF anzeigen**:
   - Das PDF öffnet sich automatisch in einem VS Code Tab
   - Oder mache einen Rechtsklick auf die .tex-Datei → "View LaTeX PDF"
   - Live-Update: Das PDF aktualisiert sich bei jeder Kompilierung automatisch

### Manuelle Kompilierung (Kommandozeile)

Falls du manuell kompilieren möchtest oder musst:

#### Master Thesis

```bash
cd limak-thesis-latex
xelatex main-limak-thesis.tex
biber main-limak-thesis
xelatex main-limak-thesis.tex
xelatex main-limak-thesis.tex
```

#### Transferarbeit

```bash
cd limak-transferarbeit-latex
xelatex main-transferarbeit.tex
biber main-transferarbeit
xelatex main-transferarbeit.tex
xelatex main-transferarbeit.tex
```

**Warum mehrmals kompilieren?**
1. **Erster Durchlauf**: Erstellt das Dokument, sammelt Referenzen
2. **Biber**: Verarbeitet die Bibliographie-Datenbank
3. **Zweiter Durchlauf**: Fügt Literaturverzeichnis ein
4. **Dritter Durchlauf**: Aktualisiert alle Querverweise und Seitenzahlen

### Windows: Kommandozeile öffnen

- **PowerShell**: Windows-Taste + X → "Windows PowerShell"
- **Cmd**: Windows-Taste + R → "cmd" eingeben → Enter
- Navigiere zum Ordner:
  ```powershell
  cd "C:\Pfad\zur\Vorlage\limak-thesis-latex"
  ```

### macOS: Terminal öffnen

- **Terminal**: Spotlight (Cmd+Space) → "Terminal" eingeben
- Navigiere zum Ordner:
  ```bash
  cd ~/Downloads/LIMAK-Masterthesis-Template/limak-thesis-latex
  ```

---

## 🛠️ Anpassung der Vorlagen

### Master Thesis anpassen

1. **Titelseite** (`main-limak-thesis.tex`, Zeilen 171-210):
   ```latex
   \title{Dein Titel der Masterarbeit}
   \author{Dein Name}{Deine Matrikelnummer}
   \supervisor{Titel Vorname Nachname}
   \degree{Master of Business Administration}{Programmname}
   ```

2. **Kapitel bearbeiten**: Öffne die Dateien `01-einleitung.tex` bis `09-zusammenfassung.tex`

3. **Literatur**: Füge deine Quellen in `references.bib` hinzu

### Transferarbeit anpassen

1. **Titelseite** (`main-transferarbeit.tex`, Zeilen 188-218):
   - Ersetze alle `[Platzhalter]` mit deinen Angaben

2. **Abschnitte bearbeiten**: Öffne die Dateien `01-ausgangssituation.tex` bis `05-schlussfolgerungen.tex`

3. **Literatur**: Füge deine Quellen in `references.bib` hinzu

### Sprache umschalten

**Für deutsche Arbeiten** (Standard):
```latex
\documentclass[a4paper,oneside,11pt,english,ngerman]{scrbook}
```

**Für englische Arbeiten**:
```latex
\documentclass[a4paper,oneside,11pt,ngerman,english]{scrbook}
```

Die **letzte** Sprache wird zur Hauptsprache (bestimmt "Kapitel" vs. "Chapter").

---

## 📋 LIMAK-Formatierung

Beide Vorlagen entsprechen den offiziellen LIMAK-Anforderungen:

| Merkmal | Einstellung | Hinweis |
|---------|-------------|---------|
| **Schriftart** | Arial 11pt | Systemschrift (vorinstalliert) |
| **Zeilenabstand** | 1.5 | Gemäß Leitfaden |
| **Seitenränder** | 3/3/3/2.5 cm (oben/unten/links/rechts) | DIN A4 |
| **Zitierstil** | Harvard (Author-Year) | BibLaTeX mit authoryear |
| **Zwei-Autoren-Separator** | `/` (Schrägstrich) | Beispiel: (Müller / Schmidt 2024) |
| **Drei+ Autoren** | et al. | Beispiel: (Müller et al. 2024) |

### Harvard-Zitierstil Beispiele

**Im Text**:
```latex
\parencite{Porter2008}              % → (Porter 2008)
\parencite[S.~123]{Porter2008}      % → (Porter 2008, S. 123)
Müller und Schmidt \parencite{key}  % → Müller und Schmidt (2024)
```

**In der Bibliographie** (`references.bib`):
```bibtex
@book{Porter2008,
    author = {Porter, Michael E.},
    title = {Competitive Advantage},
    year = {2008},
    publisher = {Free Press},
    address = {New York}
}
```

---

## 📊 Abbildungen und Tabellen

Beide Vorlagen enthalten Beispiele für:

- **TikZ-Diagramme**: Professionelle Prozessdiagramme, Balkendiagramme
- **Tabellen**: Formatierte Tabellen mit booktabs
- **Beschriftungen**: Korrekte Nummerierung und Referenzierung

**Beispiel aus der Vorlage** (siehe `02-theoretische-grundlagen.tex`):

```latex
\begin{figure}[htbp]
\centering
\begin{tikzpicture}
  % Dein Diagramm hier
\end{tikzpicture}
\caption{Beschreibung der Abbildung}
\label{fig:mein-diagramm}
\end{figure}
```

**Referenzierung im Text**:
```latex
Wie in Abbildung~\ref{fig:mein-diagramm} dargestellt...
```

---

## 🎓 Curriculum-Versionen

Die Master Thesis unterstützt beide aktuellen Curricula:

**Curriculum ab 2025S**:
```latex
\degree{Master of Business Administration}{Executive MBA Management \& Leadership}
```

**Curriculum ab 2023W**:
```latex
\degree{Executive Master of Business Administration}{Executive MBA Management \& Leadership}
```

Anpassen in `main-limak-thesis.tex` (Zeile 203).

---

## 📁 Projektstruktur

```
LIMAK-Masterthesis-Template/
├── .vscode/                         # VS Code Konfiguration (automatisch!)
│   ├── settings.json                # XeLaTeX + Biber Konfiguration
│   └── extensions.json              # Empfohlene Extensions
│
├── limak-thesis-latex/              # Master Thesis Vorlage
│   ├── main-limak-thesis.tex        # Hauptdatei
│   ├── 00-abstract.tex              # Abstract (DE/EN)
│   ├── 01-einleitung.tex            # Einleitung
│   ├── 02-theoretische-grundlagen.tex
│   ├── ...                          # Weitere Kapitel (03-09)
│   ├── 91-anhang.tex                # Anhang
│   ├── references.bib               # Literaturverzeichnis
│   ├── jkureport.sty                # LIMAK-Styling
│   └── logos/                       # LIMAK/JKU Logos
│
├── limak-transferarbeit-latex/      # Transferarbeit Vorlage
│   ├── main-transferarbeit.tex      # Hauptdatei
│   ├── 01-ausgangssituation.tex     # 5 Abschnitte gemäß
│   ├── 02-fragestellung.tex         # LIMAK Leitfaden
│   ├── 03-zielsetzung.tex
│   ├── 04-inhaltliche-bearbeitung.tex
│   ├── 05-schlussfolgerungen.tex
│   └── references.bib               # Literaturverzeichnis
│
├── instructions/                    # Offizielle LIMAK-Dokumente
│   ├── Leitfaden_Transferarbeit_2024.pdf
│   └── Vorlage_*.doc                # Word-Vorlagen
│
└── README.md                        # Diese Datei
```

---

## ❓ Häufige Probleme (Troubleshooting)

### Problem: "XeLaTeX nicht gefunden"

**Lösung Windows**:
1. Überprüfe, ob MiKTeX/TeX Live installiert ist
2. Starte den Editor neu
3. Prüfe die PATH-Variable (sollte automatisch gesetzt werden)

**Lösung macOS**:
```bash
which xelatex
# Sollte ausgeben: /Library/TeX/texbin/xelatex
```
Falls nicht gefunden:
```bash
sudo tlmgr update --self
```

### Problem: "Arial.ttf not found"

**Lösung Windows**:
- Arial ist standardmäßig installiert
- Überprüfe unter C:\Windows\Fonts
- Neuinstallation: Über Microsoft Office oder Windows-Updates

**Lösung macOS**:
```bash
fc-cache -fv
```

### Problem: "Undefined citations"

**Ursache**: Biber wurde nicht ausgeführt

**Lösung**:
1. Kompiliere in dieser Reihenfolge:
   ```bash
   xelatex main-limak-thesis.tex
   biber main-limak-thesis
   xelatex main-limak-thesis.tex
   ```
2. In VS Code: Die LaTeX Workshop Extension macht das automatisch

### Problem: "Package not found"

**MiKTeX (Windows)**:
- MiKTeX installiert Pakete automatisch beim ersten Gebrauch
- Oder öffne die MiKTeX Console → Packages → Suchen und installieren

**MacTeX (macOS)**:
```bash
sudo tlmgr install <paketname>
```

### Problem: "Compilation takes too long"

**Ursache**: Möglicherweise ist die Kompilierung hängengeblieben (z.B. durch Fehler in Platzhaltern)

**Lösung**:
1. Beende den Kompiliervorgang (Strg+C oder Stop-Button)
2. Überprüfe die .log-Datei auf Fehlermeldungen
3. Stelle sicher, dass alle `[Platzhalter]` in geschweiften Klammern stehen: `{[Text]}`

---

## 📚 Offizielle LIMAK-Dokumente

Der Ordner `instructions/` enthält:

- **Leitfaden_Transferarbeit_2024.pdf**: Offizieller LIMAK-Leitfaden
- **Word-Vorlagen**: Für Studierende, die kein LaTeX verwenden

Diese Vorlagen implementieren die Anforderungen aus diesen offiziellen Dokumenten.

---

## 🤖 Arbeiten mit Claude Code

Dieses Repository ist optimiert für die Nutzung mit **Claude Code** (claude.ai/code) - einem KI-Assistenten, der dir beim Bearbeiten deiner Arbeit helfen kann.

### Claude Code installieren

1. **Installiere die VS Code Extension**:
   - Öffne VS Code
   - Gehe zu Extensions (linke Seitenleiste oder `Strg+Shift+X`)
   - Suche nach "Claude Code"
   - Klicke auf "Install"

2. **Mit Claude.ai verbinden**:
   - Nach Installation: Klicke auf das Claude-Icon in der Seitenleiste
   - Folge den Anweisungen zur Anmeldung bei Claude.ai
   - Wähle deinen Plan (kostenlos oder Pro)

3. **Claude in diesem Projekt starten**:
   - Öffne das LIMAK Template Projekt in VS Code
   - Drücke `Strg+Shift+P` (Windows) oder `Cmd+Shift+P` (macOS)
   - Tippe "Claude" und wähle "Claude Code: Start Chat"
   - Oder klicke einfach auf das Claude-Icon in der Seitenleiste

### Was Claude für dich tun kann

✅ **Claude Code ist ideal für technische Aufgaben:**
- LaTeX-Formatierung (Tabellen, Abbildungen, TikZ-Diagramme)
- Literaturverzeichnis korrekt formatieren (Harvard-Stil)
- LaTeX-Fehler beheben und debuggen
- Querverweise und Nummerierung prüfen
- Titelseite und Metadaten anpassen

❌ **Für andere Aufgaben gibt es bessere Tools:**
- **Literaturrecherche**: Perplexity, Elicit
- **Übersetzung**: DeepL
- **Inhaltliche Arbeit**: Deine eigene Leistung!

> **⚠️ Wichtig**: Claude Code ist optimiert für **technische LaTeX-Unterstützung**. Für wissenschaftliche Inhalte nutze andere Tools oder arbeite selbst. Siehe [KI-NUTZUNG.md](KI-NUTZUNG.md) für vollständige Richtlinien.

### Praktische Beispiele

**✅ Gute Nutzung:**
- "Erstelle eine LaTeX-Tabelle aus diesen Daten: [deine Daten]"
- "Behebe diesen LaTeX-Fehler: [Fehlermeldung]"
- "Formatiere diese Grafik als TikZ-Diagramm"

**❌ Schlechte Nutzung:**
- "Schreibe ein Kapitel über Digitalisierung"
- "Analysiere diese Theorie für mich"
- "Formuliere meine Forschungsfragen"

### Mehr Informationen

- **[KI-NUTZUNG.md](KI-NUTZUNG.md)** - Vollständige Richtlinien für KI-Einsatz bei wissenschaftlichen Arbeiten
- **[CLAUDE.md](CLAUDE.md)** - Technische Details zu Claude Code und LaTeX-Formatierung

---

## 🔗 Weiterführende Ressourcen

### LaTeX lernen

- [Overleaf LaTeX Tutorial](https://www.overleaf.com/learn) (Deutsch/English)
- [LaTeX Wikibook](https://en.wikibooks.org/wiki/LaTeX) (umfassend)
- [VS Code LaTeX Workshop Dokumentation](https://github.com/James-Yu/LaTeX-Workshop/wiki)

### LaTeX-Hilfe

- [TeX Stack Exchange](https://tex.stackexchange.com/) (Q&A Community)
- [LaTeX Community Forum](https://latex.org/forum/)

### Literaturverwaltung

- **Zotero** + BetterBibTeX Plugin (empfohlen)
- **JabRef** (für .bib-Dateien)
- **Mendeley** (mit BibTeX-Export)

---

## 📄 Lizenz

Dieses Projekt steht unter der **Mozilla Public License 2.0** (MPL-2.0).

### Ursprung und Anpassungen

Diese Vorlagen basieren auf der **JKU LaTeX Technical Report Template** von Michael Roland:
- Copyright (c) 2021-2025 Michael Roland
- Original: [github.com/michaelroland/jku-templates-report-latex](https://github.com/michaelroland/jku-templates-report-latex)

Die LIMAK-spezifischen Anpassungen (Farben, Logos, Struktur, Richtlinien) wurden hinzugefügt und stehen ebenfalls unter MPL-2.0.

### Was bedeutet das?

✅ **Du darfst:**
- Die Vorlagen frei verwenden, auch für deine Masterarbeit
- Die Vorlagen anpassen und modifizieren
- Die Vorlagen mit anderen teilen

⚠️ **Bedingung:**
- Änderungen an den `.tex`/`.sty`-Dateien müssen unter MPL-2.0 bleiben
- Deine wissenschaftlichen Inhalte gehören natürlich dir!

📄 Vollständiger Lizenztext: [LICENSE](LICENSE)

---

## 🎯 Support

- **LaTeX-spezifische Fragen**: [TeX Stack Exchange](https://tex.stackexchange.com/)
- **LIMAK-Anforderungen**: Kontaktiere deine Betreuungsperson
- **Template-Probleme**: Erstelle ein Issue auf GitHub (falls Repository verfügbar)

---

**Viel Erfolg bei deiner wissenschaftlichen Arbeit!** 🎓
