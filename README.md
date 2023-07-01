# SIENA-001 Projekt README

Das SIENA-001 Projekt besteht aus einem Jupyter Notebook und einem Excel-File mit Interviewausschnitten. Ziel des Projekts ist es, mittels OpenAI's ChatGPT-4 Anforderungen aus Interviews abzuleiten und diese gegen eine von fachlich versierten Personen erstellte Anforderungsliste zu vergleichen, um die Güte der Anforderungsextraktion zu bewerten. Die Anforderungen werden hinsichtlich ihrer Klassifikation in funktionale und nicht-funktionale Anforderungen sowie den Inhalt der Anforderung verglichen.

## Inhalt

1. SIENA-notebook.ipynb: Jupyter Notebook zur Identifikation und Extraktion von Nutzeranforderungen
2. SIENA_data_interviews.xlsx: Excel-Datei mit Interviewausschnitten
3. SIENA-baseline.ipynb: Excel-Datei mit der manuell erstellten Baseline

## Anforderungen

- Python 3.x
- openai (Python-Paket)
- pandas (Python-Paket)

## Setup

1. Stellen Sie sicher, dass Python und die erforderlichen Pakete installiert sind.
2. Platzieren Sie Ihre OpenAI API-Schlüssel an der entsprechenden Stelle im Notebook `SIENA-001.ipynb`:

```
openai.api_key  = "YOUR_API_KEY"
```

## Verwendung

1. Öffnen Sie das `SIENA-001.ipynb` Notebook mit einem Jupyter Notebook-Server (z.B. JupyterLab oder Jupyter Notebook).
2. Führen Sie das gesamte Notebook aus, um die Anforderungsextraktion durchzuführen. Das Ergebnis der Analyse wird in einer CSV-Datei gespeichert. Der Fortschritt wird während der Ausführung in der Ausgabe angezeigt.

## Struktur der Ergebnis-CSV-Datei

Die resultierende CSV-Datei hat folgende Struktur:

- Klassifikation: Funktional / Nicht funktional / Unklar
- Anforderung: Der Anforderungstext, z.B. "Das System muss Anforderung erfüllen."
- Beschreibung: Eine detaillierte Beschreibung der Anforderung
- Zitat: Zitat aus dem Interviewausschnitt, das die Anforderung stützt

Beispiel:

```
Funktional; Das System muss Suchfunktionen bereitstellen; Bereitstellung von Suchfunktionen, um medizinisches Fachwissen schnell zu finden; "B: Ich möchte in der Lage sein, schnell Informationen zu finden, die ich benötige."
```

## Fehlermeldungen und Ausnahmebehandlung

Während der Ausführung des Notebooks werden möglicherweise Fehlermeldungen angezeigt. Diese können auf Probleme bei der Verarbeitung von Interviewausschnitten oder beim Speichern von Ergebnissen hinweisen. Der Fortschritt der Ausführung wird weiterhin in der Ausgabe angezeigt, einschließlich der Anzahl der aufgetretenen Fehler. Es wird empfohlen, auf mögliche Fehler zu achten und diese zu beheben, um die Qualität der Ergebnisse zu verbessern.
