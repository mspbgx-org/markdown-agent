# 📝 Markdown Agent

Ein intelligenter Agent zur Verwaltung von Markdown-Dateien mit KI-Unterstützung.

## 🚀 Features

Der Markdown Agent bietet folgende Funktionen und arbeitet ausschließlich im `files` Verzeichnis:

### 📖 Markdown-Dateien lesen
- Liest den Inhalt bestehender Markdown-Dateien aus dem `files` Verzeichnis
- Überprüft automatisch das Dateiformat (.md, .markdown)
- Zeigt den vollständigen Dateiinhalt an
- **Verwendung**: Nur Dateiname angeben (z.B. `readme.md`)

### ✏️ Markdown-Dateien erstellen
- Erstellt neue Markdown-Dateien mit strukturiertem Inhalt im `files` Verzeichnis
- Fügt automatisch die .md-Erweiterung hinzu, wenn nicht vorhanden
- Erstellt das `files` Verzeichnis automatisch, falls es nicht existiert
- Verhindert das versehentliche Überschreiben bestehender Dateien

### 🔧 Markdown-Dateien bearbeiten
- **Replace-Modus**: Ersetzt den gesamten Dateiinhalt
- **Append-Modus**: Fügt Inhalt am Ende der Datei hinzu
- **Prepend-Modus**: Fügt Inhalt am Anfang der Datei hinzu
- Arbeitet nur mit Dateien im `files` Verzeichnis

### 📁 Markdown-Dateien auflisten
- Listet alle Markdown-Dateien im `files` Verzeichnis auf
- Zeigt sowohl .md als auch .markdown Dateien an
- Erstellt das Verzeichnis automatisch, falls es nicht existiert

### 🤖 KI-gestützte Strukturierung
- Nutzt AWS Bedrock (Claude Sonnet) für intelligente Inhaltsstrukturierung
- Schlägt Verbesserungen für bessere Lesbarkeit vor
- Befolgt Markdown Best Practices automatisch
- Erstellt professionell strukturierte Inhalte

## 🛠️ Installation

```bash
# Abhängigkeiten installieren
pip install strands
```

## 💻 Verwendung

```bash
python markdown_agent.py
```

### Beispiele

**Neue Markdown-Datei erstellen:**
```
You > Erstelle mir eine README.md für ein Python-Projekt namens "Calculator"
```

**Markdown-Datei lesen:**
```
You > Lies den Inhalt der Datei README.md
```

**Datei bearbeiten:**
```
You > Füge am Ende der README.md eine Lizenz-Sektion hinzu
```

**Dateien auflisten:**
```
You > Liste alle Markdown-Dateien auf
```

**Hinweis**: Alle Operationen finden im `files` Verzeichnis statt. Sie müssen nur den Dateinamen angeben, nicht den vollständigen Pfad.

## 🏗️ Technische Details

### Dependencies
- `strands`: Framework für KI-Agenten
- `pathlib`: Dateipfad-Verwaltung
- AWS Bedrock Model: `eu.anthropic.claude-sonnet-4-20250514-v1:0`

### Tools
1. `read_markdown_file`: Liest Markdown-Dateien aus dem files Verzeichnis
2. `create_markdown_file`: Erstellt neue Markdown-Dateien im files Verzeichnis
3. `edit_markdown_file`: Bearbeitet bestehende Dateien im files Verzeichnis
4. `list_markdown_files`: Listet alle Markdown-Dateien im files Verzeichnis auf

### Dateiorganisation
- Alle Markdown-Dateien werden im `files/` Verzeichnis verwaltet
- Das Verzeichnis wird automatisch erstellt, falls es nicht existiert
- Benutzer müssen nur Dateinamen angeben, keine Pfade
- Unterstützte Dateierweiterungen: `.md` und `.markdown`

### Sicherheitsfeatures
- Dateiformatvalidierung
- Überschreibungsschutz
- Automatische Verzeichniserstellung
- Fehlerbehandlung und aussagekräftige Fehlermeldungen

## 📋 Unterstützte Modi für Bearbeitung

| Modus | Beschreibung |
|-------|-------------|
| `replace` | Ersetzt den gesamten Dateiinhalt |
| `append` | Fügt neuen Inhalt am Ende hinzu |
| `prepend` | Fügt neuen Inhalt am Anfang hinzu |

## 🎯 Best Practices

Der Agent befolgt automatisch Markdown Best Practices:
- Verwendung korrekter Markdown-Syntax
- Logische Strukturierung mit angemessenen Überschriften  
- Professionelle Formatierung
- Verbesserungsvorschläge für bessere Lesbarkeit

## 🔧 Anpassung

Um das Verhalten des Agenten anzupassen, können Sie:
- Das System-Prompt in der `markdown_agent.py` ändern
- Zusätzliche Tools hinzufügen
- Das verwendete LLM-Modell austauschen

## 🤝 Beitragen

Contributions sind willkommen! Bitte erstellen Sie einen Pull Request oder öffnen Sie ein Issue.

## 📄 Lizenz

Dieses Projekt steht unter der MIT-Lizenz.