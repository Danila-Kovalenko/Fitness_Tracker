# Fitness-Tracker (Python)

Dieses Repository enthält ein kleines, objektorientiertes Beispielprojekt für einen Fitness-Tracker. 
Die Anwendung verarbeitet Trainingsdaten aus eingehenden Datenpaketen, erstellt dafür passende Trainingsobjekte und berechnet zentrale Kennzahlen wie:

- **Distanz**
- **Durchschnittsgeschwindigkeit**
- **Kalorienverbrauch**

## Projektidee

Im Mittelpunkt steht eine Basisklasse `Training`, von der konkrete Trainingsarten erben:

- `Running` (Laufen)
- `SportsWalking` (Sportliches Gehen)
- `Swimming` (Schwimmen)

Jede Trainingsart implementiert ihre eigene Logik zur Berechnung der verbrannten Kalorien. 
Über `show_training_info()` wird ein `InfoMessage`-Objekt erzeugt, das die Ergebnisse in einem einheitlichen Textformat ausgibt.

## Struktur

- `homework.py` – Hauptlogik mit Klassen, Berechnungen und Verarbeitung der Datenpakete.
- `tests/test_homework.py` – automatisierte Tests für Klassen, Methoden und Formeln.
- `tests/conftest.py` – Test-Hilfsfunktionen.
- `requirements.txt` – Abhängigkeiten.

## Ausführen

### 1) Abhängigkeiten installieren

```bash
pip install -r requirements.txt
```

### 2) Beispielstart

```bash
python homework.py
```

Die Datei enthält im `__main__`-Block ein Beispielpaket, das verarbeitet und als Trainingsbericht ausgegeben wird.

## Tests ausführen

```bash
pytest
```

## Lernfokus des Projekts

Dieses Projekt demonstriert vor allem:

- Vererbung und Polymorphie in Python
- Arbeiten mit `dataclass`
- saubere Aufteilung von gemeinsamer und trainingsspezifischer Logik
- testgetriebene Überprüfung von Berechnungen
