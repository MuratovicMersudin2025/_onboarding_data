# Day 1 - Antworten

## Aufgabe: Datenbereinigung in Google Sheets

### Link zum bereinigten Google Sheet
[Google Sheet - Bereinigte Daten](https://docs.google.com/spreadsheets/d/e/2PACX-1vQiva34qA-iKN6doMORtHPnBkvQEQkqls8gWLubG3PPsIREMcadOH7A-YDappbgZ8sXJMQNcmcmRWie/pub?gid=1263977315&single=true&output=csv)

### Durchgeführte Bereinigungsschritte

1. **Duplikate entfernt**: Überprüfung der Datensätze auf doppelte Einträge anhand der ID-Spalte. Insgesamt 12 Duplikate identifiziert und entfernt.

2. **NULL-Werte behandelt**: 
   - Leere Zellen in der Spalte "Email" identifiziert (8 Fälle)
   - Leere Zellen in der Spalte "Phone" identifiziert (5 Fälle)
   - Strategie: Zeilen mit fehlenden Pflichtfeldern (Email) wurden entfernt, optionale Felder (Phone) mit "N/A" gefüllt

3. **Formatierung standardisiert**:
   - Datumsformat vereinheitlicht auf DD.MM.YYYY
   - Email-Adressen auf Kleinschreibung konvertiert
   - Telefonnummern in einheitliches Format gebracht (+49...)
   - Leerzeichen am Anfang/Ende von Textfeldern entfernt (TRIM-Funktion)

4. **Datenvalidierung durchgeführt**:
   - Email-Format mit Regex geprüft (muss @ und Domain enthalten)
   - Numerische Felder auf gültige Werte getestet (keine negativen Werte bei Alter)
   - 3 ungültige Email-Adressen korrigiert

5. **Spalten umbenannt und strukturiert**:
   - Spaltenüberschriften auf Englisch und konsistente Benennung geändert
   - Unnötige Spalten entfernt (z.B. leere Spalte F)

### Erkenntnisse und Learnings

- **Systematisches Vorgehen ist entscheidend**: Habe gelernt, dass man zuerst eine Datenübersicht erstellen sollte (Duplikate zählen, NULL-Werte identifizieren) bevor man mit der Bereinigung beginnt.

- **Dokumentation während der Arbeit**: Während der Bereinigung habe ich direkt Notizen gemacht, welche Änderungen ich vorgenommen habe - das hat die Dokumentation später deutlich erleichtert.

- **Google Sheets Funktionen**: Habe neue Funktionen kennengelernt:
  - `UNIQUE()` zum Finden von Duplikaten
  - `TRIM()` zum Entfernen von Leerzeichen
  - `LOWER()` für Kleinschreibung
  - Bedingte Formatierung zur Visualisierung von Problemen

- **Entscheidungen bei fehlenden Daten**: Musste abwägen, wann Zeilen gelöscht vs. mit Platzhaltern gefüllt werden. Habe gelernt: Pflichtfelder (Email) erfordern Löschung, optionale Felder können mit "N/A" oder "Unknown" gefüllt werden.

- **Herausforderungen mit Formaten**: Datumsformate waren inkonsistent (mix aus DD/MM/YYYY und MM/DD/YYYY), musste manuell prüfen und korrigieren.

- **Nächstes Mal anders**: Würde direkt am Anfang ein separates Sheet für "Problematic Rows" erstellen, um später nachvollziehen zu können, welche Daten entfernt oder angepasst wurden.

### Freigabe-Status

- [x] Google Sheet ist bereinigt
- [x] Sheet ist korrekt geteilt (Zugriff für Reviewer)
- [x] Alle Antworten sind dokumentiert

### Statistik der Bereinigung

- **Ursprüngliche Zeilen**: 250
- **Nach Bereinigung**: 229
- **Entfernte Duplikate**: 12
- **Entfernte Zeilen (fehlende Pflichtdaten)**: 9
- **Korrigierte Werte**: 15
- **Bereinigte Spalten**: 8
- **Entfernte Spalten**: 2
