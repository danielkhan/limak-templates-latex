# LIMAK Transferarbeits-Vorlage für LaTeX

Diese LaTeX-Vorlage ist speziell für **Transferarbeiten** an der **LIMAK Austrian Business School** (Johannes Kepler Universität Linz) im Studiengang **Master in Management** konzipiert.

## Was ist eine Transferarbeit?

Eine Transferarbeit ist eine **praxisorientierte, nach wissenschaftlichen Kriterien formulierte, schriftliche Arbeit**. Sie verbindet:
- Inhalte, Konzepte und Modelle aus den Lehrveranstaltungen
- Wissenschaftliche Literatur
- Aktuelle Fragestellungen aus dem beruflichen Umfeld

## Über diese Vorlage

### Hauptmerkmale

- **Dokumentklasse**: KOMA-Script scrartcl (für kürzere wissenschaftliche Arbeiten)
- **Schriftgröße**: 11pt Arial (gemäß LIMAK-Standards)
- **Sprache**: Deutsch (ngerman)
- **Zeilenabstand**: 1.5
- **Kompilierung**: XeLaTeX + Biber (empfohlen)

### Struktur gemäß LIMAK-Leitfaden

Die Vorlage folgt der im [Leitfaden Transferarbeit 2024](../instructions/Leitfaden_Transferarbeit_2024.pdf) vorgegebenen Standardstruktur:

1. **Ausgangssituation** - Kontext und Rahmenbedingungen
2. **Fragestellung** - Zentrale Forschungsfrage
3. **Zielsetzung** - Theoretische und praktische Ziele
4. **Inhaltliche Bearbeitung** - Hauptteil mit Theorie-Praxis-Transfer
5. **Schlussfolgerungen** - Erkenntnisse und Handlungsempfehlungen

## Installation und Nutzung

### Voraussetzungen

Sie benötigen eine vollständige LaTeX-Installation mit XeLaTeX-Unterstützung:

- **Windows**: [MiKTeX](https://miktex.org/) oder [TeX Live](https://www.tug.org/texlive/)
- **macOS**: [MacTeX](https://www.tug.org/mactex/)
- **Linux**: TeX Live (über Package Manager)

**Wichtig**: Arial muss auf Ihrem System installiert sein.

**Empfohlener Editor**: [TeXstudio](https://www.texstudio.org/) oder [VS Code mit LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)

### Erste Schritte

1. **Öffnen** Sie `main-transferarbeit.tex` in Ihrem LaTeX-Editor
2. **Anpassen** der Titelseite (Zeilen 105-150):
   - Titel der Transferarbeit
   - Name der Lehrveranstaltung
   - Fakultätsmitglied (Betreuer*in)
   - Ihr Name und Matrikelnummer
3. **Kompilieren** mit XeLaTeX + Biber

### Kompilierungsreihenfolge

Für vollständige Referenzen und Literaturverzeichnis:

```bash
xelatex main-transferarbeit.tex
biber main-transferarbeit
xelatex main-transferarbeit.tex
xelatex main-transferarbeit.tex
```

Die meisten LaTeX-Editoren machen dies automatisch.

## Struktur der Vorlage

```
limak-transferarbeit-latex/
├── main-transferarbeit.tex        # Hauptdatei
├── 01-ausgangssituation.tex       # Kapitel 1
├── 02-fragestellung.tex           # Kapitel 2
├── 03-zielsetzung.tex             # Kapitel 3
├── 04-inhaltliche-bearbeitung.tex # Kapitel 4 (Hauptteil)
├── 05-schlussfolgerungen.tex      # Kapitel 5
├── references.bib                 # Literaturverzeichnis
├── 09-anhang.tex                  # Anhang (optional)
├── fonts/                         # Schriftarten (optional)
└── logos/                         # LIMAK/JKU-Logos (optional)
```

## Wichtige Formale Anforderungen

### Formatierung (gemäß Leitfaden)

- **Schriftart**: Arial 11pt ✓
- **Zeilenabstand**: 1.5 ✓
- **Papier**: DIN A4 ✓
- **Umfang**: Siehe Syllabus der Lehrveranstaltung (±10% Toleranz)

### Titelseite muss enthalten:

- Programmname (Master in Management)
- Titel der Lehrveranstaltung
- Fakultätsmitglied (Betreuer*in)
- Name der Autorin/des Autors

### Dateiname für Abgabe:

Format: `Nachname_FakultaetsmitgliedNachname.pdf`
- Beispiel: `Mueller_Schmidt.pdf`
- Bei Gruppenarbeit: `Group1_Schmidt.pdf`

### Gliederung:

- Hauptkapitel: Arabische Ziffern (1, 2, 3...)
- Unterkapitel müssen **mindestens 2 Unterpunkte** haben (z.B. 1.1, 1.2)
- Absätze müssen **mehr als einen Satz** enthalten

## Wissenschaftliches Arbeiten

### Sprache

**Vermeiden Sie persönliche Meinungen**:
- ❌ "Ich bin der Meinung, dass..."
- ✓ "Daraus lässt sich schließen, dass..."
- ✓ "Die Analyse zeigt, dass..."
- ✓ "Es kann abgeleitet werden, dass..."

**Genderneutrale Sprache ist verpflichtend**. Die Generalklausel ("aus Gründen der Lesbarkeit nur männliche Form") ist **nicht gestattet**.

### Zitieren

Die Vorlage nutzt den **Harvard-Zitierstil** (author-year) gemäß LIMAK-Leitfaden.

**Im Text**:
```latex
Daraus ergibt sich \parencite{Mueller2023}...  % Ergebnis: (Müller 2023)
\textcite{Schmidt2024} zeigen, dass...         % Ergebnis: Schmidt (2024) zeigen...
```

**In references.bib**:
```bibtex
@book{Mueller2023,
  author = {Müller, Max},
  title = {Buchtitel},
  year = {2023},
  publisher = {Verlag}
}
```

**Internet-Quellen**:
```bibtex
@online{Webseite2024,
  author = {Autor, Vorname},
  title = {Titel der Webseite},
  url = {https://example.com},
  urldate = {2024-01-15}
}
```

### Plagiatsvermeidung

**Führt zu automatischer negativer Beurteilung**:
- Ungekennzeichnete Übernahme fremder Texte
- Arbeit einer anderen Person als eigene ausgeben
- Verwendung von KI (ChatGPT, etc.) zum Schreiben der Arbeit

## Kapitel bearbeiten

### Kapitel hinzufügen/entfernen

In `main-transferarbeit.tex` (Zeilen 175-179):

```latex
\import{./}{01-ausgangssituation}
\import{./}{02-fragestellung}
% Weitere Kapitel hier einfügen
```

### Literatur hinzufügen

In `references.bib`:

```bibtex
@article{Beispiel2024,
  author = {Nachname, Vorname},
  title = {Titel des Artikels},
  journal = {Zeitschrift},
  year = {2024},
  volume = {10},
  pages = {123--145}
}
```

## Troubleshooting

### Fehler: Arial nicht gefunden

**Option 1**: Installieren Sie Arial auf Ihrem System

**Option 2**: Verwenden Sie eine alternative Schriftart in `main-transferarbeit.tex`:
```latex
\setmainfont{Liberation Sans}  % oder Helvetica
```

### Literaturverzeichnis wird nicht angezeigt

- Stellen Sie sicher, dass Sie **Biber** verwenden (nicht BibTeX)
- Kompilieren Sie in der richtigen Reihenfolge: XeLaTeX → Biber → XeLaTeX → XeLaTeX

### PDF ist geschützt / nicht druckfähig

Exportieren Sie das PDF ohne Passwortschutz. LIMAK akzeptiert nur druckfähige PDFs.

## Support

- **Formale Anforderungen**: Siehe [Leitfaden_Transferarbeit_2024.pdf](../instructions/Leitfaden_Transferarbeit_2024.pdf)
- **LaTeX-Hilfe**: [LaTeX Wikibook (Deutsch)](https://de.wikibooks.org/wiki/LaTeX-Kompendium)
- **LIMAK-spezifische Fragen**: Wenden Sie sich an Ihre*n Betreuer*in

## Lizenz

Diese Vorlage basiert auf der JKU LaTeX Template:
- Copyright (c) 2021-2025 Michael Roland
- License: Mozilla Public License v2.0

---

**Viel Erfolg bei Ihrer Transferarbeit!**
