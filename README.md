# Python für Ingenieure

Repository für den TU-Berlin-Kurs **Python für Ingenieure**.

---

## Ordnerstruktur

```
PythonFuerIngenieure/
├── Arbeitsmaterial/        # Vorlesungsbegleitende Notebooks (Lernmaterial)
├── Hausaufgaben/           # Abgaben, eine pro Aufgabe
│   ├── HA0/
│   ├── HA1/
│   └── ...
└── Skripte/                # Eigenständige Python-Skripte (.py)
```

---

## Regeln für die Zusammenarbeit

### Branches
- `main` ist der stabile Hauptbranch — hier landet nur fertig bearbeitetes Material.
- Für jede Hausaufgabe wird ein eigener Branch angelegt: `HA<Nummer>_<kurzer-titel>`, z. B. `HA1_Schleifen`.
- Änderungen an `main` erfolgen ausschließlich über Pull Requests.

### Commits
- Commit-Nachrichten auf **Deutsch oder Englisch**, klar und knapp: Was wurde geändert und warum?
  - Gut: `HA1: Aufgabe 2 gelöst, Schleife optimiert`
  - Schlecht: `update`, `fix`, `asdf`
- Jeder Commit sollte genau eine logische Änderung enthalten — nicht alles auf einmal.
- Vor dem Commit sicherstellen, dass alle Notebook-Zellen einmal sauber durchgelaufen sind (`Kernel → Restart & Run All`).

### Hausaufgaben
- Jede Hausaufgabe liegt in `Hausaufgaben/HA<Nummer>/`.
- Die Abgabedatei heißt `HA<Nummer>_Gruppe<Gruppennr>.ipynb`, z. B. `HA1_Gruppe112.ipynb`.
- Keine Musterlösungen oder fremden Lösungen in den Hausaufgaben-Ordnern einchecken.
- Plausibilitätstests (`assert`-Zellen) müssen fehlerfrei durchlaufen.

### Notebooks allgemein
- Zellen-Ausgaben dürfen eingecheckt werden — sie helfen beim Reviewen.
- Keine unnötigen Kernel-Neustarts oder leere Zellen am Ende der Datei hinterlassen.
- Eigener Code immer direkt unter dem Kommentar `# Hier eigenen Code schreiben ...` eintragen.

### Arbeitsmaterial
- Der Ordner `Arbeitsmaterial/` enthält nur das vom Kurs bereitgestellte Lernmaterial.
- Eigene Notizen oder Experimente gehören **nicht** hierhin — dafür lieber einen separaten Ordner nutzen.

### Was nicht eingecheckt wird
Folgendes bleibt lokal und kommt nie ins Repository (bereits in `.gitignore` konfiguriert):
- `.venv/` – virtuelle Python-Umgebung
- `__pycache__/`, `*.pyc` – Python-Cache
- `.ipynb_checkpoints/` – Jupyter-Checkpoints
- `.DS_Store` – macOS-Metadaten

---

## Einrichtung (einmalig)

```bash
# Repository klonen
git clone <repo-url>
cd PythonFuerIngenieure

# Virtuelle Umgebung anlegen und aktivieren
python -m venv .venv
source .venv/bin/activate      # macOS/Linux
# .venv\Scripts\activate       # Windows

# Jupyter installieren
pip install jupyter numpy
```

Danach Notebooks starten mit:

```bash
jupyter notebook
```
