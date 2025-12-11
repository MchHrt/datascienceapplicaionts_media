# Text Mining als Datenanalyse-Strategie
## Kursportfolio – Management, Communication & IT

Willkommen im offiziellen GitHub-Repository für den Kurs *Text Mining als Datenanalyse-Strategie*.
Hier dokumentieren wir gemeinsam die Inhalte, Übungen und das finale Portfolio-Projekt.
Der Kurs richtet sich an Studierende mit Schwerpunkt auf Medien- und Managementfragen im digitalen Raum.

---

## 🧭 Kursstruktur (6 Termine)

### 1. Einführung & Use Cases
- Impulsvortrag: Überblick über Text Mining in Management & Kommunikation
- Gruppenarbeit: Anwendungsbereiche
- Mega Tutorial: Web-Scraping mit `BeautifulSoup`

### 2. Datenquellen & Vorverarbeitung
- Sammeln und Importieren von Textdaten (z. B. GitHub, Social Media, PDFs)
- Tokenisierung, Stopword-Handling, Normalisierung
- Erste Explorationsschritte mit Pandas & spaCy

### 3. Feature Engineering & Visualisierung
- Frequenzanalysen, N-Gramme, Named Entity Recognition
- Visualisierung mit Wordclouds, Barplots, Netzwerken
- Diskussion: Was sagen uns die Texte wirklich?

### 4. LLMs & semantische Analyse
- Einführung in Large Language Models (LLMs)
- Prompt Engineering & semantische Textklassifikation
- Ollama lokal nutzen: Setup & erste Experimente

### 5. Anwendungsszenarien & Prototyping
- Gruppenarbeit: Entwicklung eines Mini-Prototyps
- Textbasierte Entscheidungsunterstützung, Trendanalyse, Stimmungsmodelle
- Feedback & Iteration

### 6. Portfolio-Projekt & Reflexion
- Präsentation der Projekte
- Reflexion: Was funktioniert, was nicht?
- Dokumentation & Upload ins Repository

## 📁 Ordnerstruktur

```plaintext
├── data/              # Beispiel- und Übungsdaten
├── notebooks/         # Jupyter Notebooks zu den einzelnen Terminen
├── portfolio/         # Ergebnisse der Gruppenprojekte
├── resources/         # Zusatzmaterialien, Links, PDFs
└── README.md          # Kursübersicht
```

## ⚙️ Vorbereitung

* Erstellt einen Fork dieses Repositories - das ist eine Kopie des Repos in der ihr selbst experimentieren könnt, ohne das Original zu verändern.
* Öffnet euren Fork mit Github Desktop (oder nutzt `git clone` im Terminal)
* Erstellt eine virtuelle Umgebung mit VSCode (oder nutzt `python -m virtualenv .venv` im Terminal)
* Installiert die Bibliotheken in der `requirements.txt`

## Local LLMs

* Ollama-Client installieren ([Websie](https://ollama.com))
* Modell herunterladen (im Terminal)

```shell
ollama pull llama3.1:8b
```

* Modelfile erzeugen (im Text Editor)

```txt
FROM llama3.1:8b
PARAMETER temperature 0.7
PARAMETER num_ctx 5000
SYSTEM """Du bist Spiderman...."""
```

* Customized Modell erstellen (im Termin)

```shell
ollama create spiderman -f Modelfile
```

* Modell verwenden

```python
from ollama import generate

response = generate(
    "llama3.1:8b",
    "Was ist der Sinn des Lebens"
)

print(response["response"])
```
