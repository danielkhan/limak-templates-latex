# CLAUDE.md - Arbeiten mit Claude an LIMAK-Arbeiten

Diese Datei hilft dir dabei, **Claude Code** (claude.ai/code) effektiv beim Bearbeiten deiner LIMAK Master Thesis oder Transferarbeit einzusetzen.

> **⚠️ WICHTIG**: Claude soll dich beim **Bearbeiten, Formatieren und Strukturieren** deiner Arbeit unterstützen - NICHT beim Verfassen der wissenschaftlichen Inhalte. Die fachlichen Inhalte, Argumente und Analysen müssen von dir stammen!

---

## 📚 Repository-Übersicht

Dieses Repository enthält LaTeX-Vorlagen für akademische Arbeiten an der LIMAK Austrian Business School (Johannes Kepler Universität Linz):

- **limak-thesis-latex/**: Master Thesis Vorlage (60+ Seiten, 9 Kapitel)
- **limak-transferarbeit-latex/**: Transferarbeit Vorlage (10-20 Seiten, 5 Abschnitte)

---

## 🎯 Wie Claude dir helfen kann

### ✅ Claude KANN helfen bei:

1. **LaTeX-Formatierung**
   - Tabellen erstellen und formatieren
   - Abbildungen einbinden (TikZ-Diagramme, PNG/PDF)
   - Literaturverzeichnis korrekt formatieren (Harvard-Stil)
   - LaTeX-Fehler beheben

2. **Strukturierung**
   - Kapitel-Struktur überprüfen
   - Inhaltsverzeichnis aktualisieren
   - Querverweise (`\ref`, `\label`) korrekt setzen
   - Nummerierung von Abbildungen/Tabellen prüfen

3. **LIMAK-Formatierungsvorgaben**
   - Arial 11pt, 1.5 Zeilenabstand prüfen
   - Seitenränder (3/3/3/2.5 cm) kontrollieren
   - Harvard-Zitierstil (`\parencite`) korrekt anwenden
   - Zwei-Autoren-Separator `/` überprüfen

4. **Technische Probleme**
   - Kompilierungsfehler beheben
   - Biber/BibLaTeX Probleme lösen
   - Umlaute und Sonderzeichen korrigieren
   - PDF-Generierung debuggen

5. **Vorlagen-Anpassung**
   - Titelseite anpassen
   - Metadaten aktualisieren
   - Kapitel hinzufügen/entfernen
   - Layout-Anpassungen vornehmen

### ❌ Claude SOLLTE NICHT helfen bei:

1. **Wissenschaftliche Inhalte verfassen**
   - Forschungsfragen formulieren
   - Argumentationen entwickeln
   - Literatur analysieren
   - Fallstudien schreiben
   - Empirische Analysen durchführen

2. **Fachliche Bewertungen**
   - Theorien bewerten
   - Methodenwahl begründen
   - Ergebnisse interpretieren
   - Schlussfolgerungen ziehen

> **💡 Faustregel**: Claude hilft beim "Wie" (Formatierung, Struktur), nicht beim "Was" (Inhalt, Argumente)

---

## 🛠️ Praktische Beispiele für Claude-Nutzung

### Beispiel 1: Tabelle formatieren

**Du schreibst:**
> "Ich habe diese Daten, kannst du eine LaTeX-Tabelle daraus machen?"
>
> ```
> Kennzahl | 2022 | 2023 | 2024
> Umsatz | 100 | 120 | 145
> Gewinn | 10 | 15 | 20
> ```

**Claude erstellt:**
```latex
\begin{table}[htbp]
\centering
\caption{Unternehmenskennzahlen 2022-2024 (in Mio. EUR)}
\label{tab:kennzahlen}
\begin{tabular}{lrrr}
\toprule
Kennzahl & 2022 & 2023 & 2024 \\
\midrule
Umsatz & 100 & 120 & 145 \\
Gewinn & 10 & 15 & 20 \\
\bottomrule
\end{tabular}
\end{table}
```

### Beispiel 2: Literaturverzeichnis-Fehler beheben

**Du fragst:**
> "Meine Zitation zeigt 'undefined reference', was ist falsch?"

**Claude prüft:**
- Ist der Biber-Lauf durchgeführt?
- Stimmt der BibTeX-Key in `\parencite{}`?
- Ist die Quelle in `references.bib` vorhanden?
- Ist die Harvard-Syntax korrekt?

### Beispiel 3: TikZ-Diagramm aus Daten erstellen

**Du schreibst:**
> "Kannst du ein Balkendiagramm für diese Werte erstellen?"

**Claude erstellt ein TikZ-Diagramm** basierend auf deinen Daten (nicht basierend auf erfundenen Daten!)

### Beispiel 4: LaTeX-Fehler debuggen

**Du zeigst:**
> "Beim Kompilieren erscheint dieser Fehler: `! Missing } inserted`"

**Claude hilft:**
- Log-Datei analysieren
- Fehlerhafte Zeile finden
- Syntaxfehler korrigieren
- Kompilierung testen

---

## 🔧 Build-Kommandos

### LaTeX kompilieren

Die Vorlagen verwenden **XeLaTeX** mit **Biber** für die Bibliographie.

#### Transferarbeit:
```bash
cd limak-transferarbeit-latex
xelatex main-transferarbeit.tex
biber main-transferarbeit
xelatex main-transferarbeit.tex
xelatex main-transferarbeit.tex
```

#### Master Thesis:
```bash
cd limak-thesis-latex
xelatex main-limak-thesis.tex
biber main-limak-thesis
xelatex main-limak-thesis.tex
xelatex main-limak-thesis.tex
```

#### Schnellkompilierung (während der Bearbeitung):
```bash
xelatex main-limak-thesis.tex  # oder main-transferarbeit.tex
```

---

## 📝 Template-Struktur

### Master Thesis Template

**Hauptdatei**: `limak-thesis-latex/main-limak-thesis.tex`

**Kapitel-Dateien**:
- `00-abstract.tex` - Abstract (DE/EN)
- `01-einleitung.tex` - Einleitung
- `02-theoretische-grundlagen.tex` - Theoretische Grundlagen
- `03-methodik.tex` - Methodik
- `04-ist-analyse.tex` - Ist-Analyse
- `05-soll-konzept.tex` - Soll-Konzept
- `06-implementierung.tex` - Implementierung
- `07-evaluation.tex` - Evaluation
- `08-diskussion.tex` - Diskussion
- `09-zusammenfassung.tex` - Zusammenfassung
- `91-anhang.tex` - Anhang

**Wichtige Dateien**:
- `references.bib` - Literaturverzeichnis
- `jkureport.sty` - LIMAK-Styling
- `logos/` - LIMAK/JKU Logos

### Transferarbeit Template

**Hauptdatei**: `limak-transferarbeit-latex/main-transferarbeit.tex`

**Abschnitts-Dateien** (gemäß LIMAK Leitfaden):
- `01-ausgangssituation.tex` - Ausgangssituation
- `02-fragestellung.tex` - Fragestellung
- `03-zielsetzung.tex` - Zielsetzung
- `04-inhaltliche-bearbeitung.tex` - Inhaltliche Bearbeitung
- `05-schlussfolgerungen.tex` - Schlussfolgerungen mit Handlungsempfehlungen

---

## 📖 LIMAK-spezifische Anforderungen

### Formatierung

| Element | Vorgabe | LaTeX |
|---------|---------|-------|
| Schriftart | Arial 11pt | `\setmainfont{Arial}` (Systemfont) |
| Zeilenabstand | 1.5 | `\onehalfspacing` |
| Seitenränder | 3/3/3/2.5 cm | Vorkonfiguriert in `geometry` |
| Zitierstil | Harvard (Author-Year) | `\parencite{key}` |

### Harvard-Zitierstil Beispiele

**Im Text**:
```latex
\parencite{Porter2008}                    % → (Porter 2008)
\parencite[S.~123]{Porter2008}            % → (Porter 2008, S. 123)
Müller und Schmidt \parencite{key}        % → Müller und Schmidt (2024)
```

**Zwei Autoren** (mit `/`):
```latex
% In references.bib:
@article{Mueller2020,
    author = {Müller, Anna and Schmidt, Peter},
    ...
}

% Wird zu: (Müller / Schmidt 2020)
```

**Drei+ Autoren** (automatisch "et al."):
```latex
% In references.bib:
@article{Mueller2020,
    author = {Müller, Anna and Schmidt, Peter and Wagner, Thomas},
    ...
}

% Wird zu: (Müller et al. 2020)
```

### Bibliographie (`references.bib`)

**Buch**:
```bibtex
@book{Porter2008,
    author = {Porter, Michael E.},
    title = {Competitive Advantage},
    year = {2008},
    publisher = {Free Press},
    address = {New York}
}
```

**Journal-Artikel**:
```bibtex
@article{Barney1991,
    author = {Barney, Jay},
    title = {Firm Resources and Sustained Competitive Advantage},
    journal = {Journal of Management},
    year = {1991},
    volume = {17},
    number = {1},
    pages = {99--120},
    doi = {10.1177/014920639101700108}
}
```

**Online-Quelle**:
```bibtex
@online{McKinsey2023,
    author = {{McKinsey \& Company}},
    title = {The State of Organizations 2023},
    year = {2023},
    url = {https://www.mckinsey.com/...},
    urldate = {2024-01-15},
    note = {Zugriff am 15.01.2024}
}
```

---

## 🚀 VS Code Integration

Das Repository enthält vorkonfigurierte VS Code Settings:

**`.vscode/settings.json`**:
- XeLaTeX als Standard-Compiler
- Biber für Bibliographie
- Automatische Kompilierung beim Speichern

**`.vscode/extensions.json`**:
- Empfiehlt "LaTeX Workshop" Extension

### Erste Schritte mit VS Code

1. Öffne den Projekt-Ordner in VS Code
2. Installiere die empfohlene Extension (Popup erscheint automatisch)
3. Öffne `main-limak-thesis.tex` oder `main-transferarbeit.tex`
4. Speichere mit `Strg+S` (Windows) oder `Cmd+S` (macOS)
5. PDF wird automatisch kompiliert und angezeigt

---

## 💡 Tipps für die Arbeit mit Claude

### 1. Zeige Claude konkrete Beispiele
❌ Schlecht: "Formatiere das"
✅ Gut: "Kannst du diese Tabelle als LaTeX-Tabelle mit `booktabs` formatieren?" + Dateneingabe

### 2. Beschreibe LaTeX-Fehler präzise
❌ Schlecht: "Es kompiliert nicht"
✅ Gut: "Beim Kompilieren erscheint Fehler X in Zeile Y" + Log-Auszug

### 3. Gib Claude deine eigenen Inhalte
❌ Schlecht: "Schreibe ein Kapitel über Digitalisierung"
✅ Gut: "Ich habe diesen Text geschrieben, kannst du ihn als LaTeX formatieren?" + dein Text

### 4. Lass Claude technische Aufgaben erledigen
✅ "Erstelle ein TikZ-Diagramm aus diesen Daten"
✅ "Behebe diesen LaTeX-Kompilierfehler"
✅ "Formatiere diese Quelle für references.bib"
✅ "Prüfe, ob alle Querverweise funktionieren"

### 5. Behalte die Kontrolle über Inhalte
❌ "Analysiere diese Theorie"
❌ "Schreibe eine Fallstudie"
❌ "Formuliere Forschungsfragen"

---

## 🎓 Wissenschaftliche Integrität

### Eigenleistung

Deine Master Thesis oder Transferarbeit ist eine **wissenschaftliche Eigenleistung**. Claude kann:
- ✅ Beim Formatieren helfen
- ✅ LaTeX-Probleme lösen
- ✅ Strukturierung unterstützen

Claude darf **NICHT**:
- ❌ Wissenschaftliche Inhalte verfassen
- ❌ Argumentationen entwickeln
- ❌ Forschungsergebnisse interpretieren

### Eidesstattliche Erklärung

In deiner Arbeit erklärst du, dass du die Arbeit selbstständig verfasst hast. Die Nutzung von Claude für:
- ✅ LaTeX-Formatierung ist OK (technisches Hilfsmittel)
- ❌ Inhaltserstellung ist NICHT OK (Plagiat/Täuschung)

### Im Zweifel

Frage deine Betreuungsperson bei LIMAK, wenn du unsicher bist, ob eine bestimmte Nutzung von Claude zulässig ist.

---

## 📚 Weitere Ressourcen

- **README.md**: Ausführliche Installations- und Nutzungsanleitung
- **LIMAK Leitfaden**: Offizielle Anforderungen (im `instructions/` Ordner)
- **LaTeX Workshop Dokumentation**: https://github.com/James-Yu/LaTeX-Workshop/wiki
- **TeX Stack Exchange**: https://tex.stackexchange.com/ (LaTeX-Community)

---

**Viel Erfolg bei deiner wissenschaftlichen Arbeit!** 🎓
