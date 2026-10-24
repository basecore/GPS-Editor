# 🗺️ GPS Track Editor Pro

[![Version](https://img.shields.io/badge/version-1.9.0-blue.svg)](https://basecore.github.io/GPS-Editor/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PWA](https://img.shields.io/badge/PWA-Ready-success.svg)](https://basecore.github.io/GPS-Editor/)
[![AI](https://img.shields.io/badge/AI_Generated-Gemini_3.1-8A2BE2.svg)](#)

Eine professionelle, komplett lokal im Browser laufende und Smartphone-optimierte Web-App (PWA) zur Visualisierung, detaillierten Analyse, Bereinigung, Zusammenführung und zum präzisen Zuschneiden von GPS-Daten.

Besonders optimiert für den **Import von fortlaufenden GPS-Logs (z. B. aus der App *GPSLogger*)** sowie für das Zusammenführen mehrerer unvollständiger GPX-Tracks. So lassen sich spezifische Aktivitäten – etwa Jogging-Runden oder Radtouren – aus einem ganzen Tages-Track extrahieren und als saubere GPX-Datei für **Garmin Connect, Strava oder Komoot** exportieren.

🚀 **[Live-Demo öffnen (App direkt im Browser starten)](https://basecore.github.io/GPS-Editor/)**

---

## ✨ Key Features

* 🔒 **Privacy-First (100% Lokal):** Alle Berechnungen, Analysen und Dateiexporte finden ausschließlich im Speicher deines Browsers statt. Es werden keine Standortdaten an externe Server gesendet.
* 📂 **Multi-File-Import:** Mehrere `.csv`-, `.gpx`- und `.kml`-Dateien können gleichzeitig geladen werden. Die App führt alle Trackpunkte zu einer gemeinsamen, zeitlich sortierten Aufzeichnung zusammen.
* 🔗 **Intelligenter Track-Merge:** Überlappende Bereiche mehrerer Tracker werden erkannt. Punkte, die zeitlich und örtlich zusammengehören, werden zusammengeführt; Position und Höhe werden dabei gemittelt.
* 🧹 **GPS-Sprungfilter:** Unrealistische Geschwindigkeits- oder Positionssprünge – etwa durch GPS-Drift oder einen Tracker-Fehler – werden automatisch erkannt und entfernt.
* ⛰️ **Höhen-Glättung:** Die Höhe wird per Median-Filter geglättet. Verbleibende Höhen-Sprünge, insbesondere an Schnittstellen zusammengeführter Tracks, werden korrigiert.
* ⚠️ **Lückenerkennung:** Pausen oder fehlende Aufzeichnungen werden erkannt und im GPX-Export als separate `<trkseg>`-Segmente behandelt. Es entstehen keine falschen Verbindungslinien über Lücken.
* 🏃 **Manueller Aktivitätstyp:** Die Aktivität kann pro Tag manuell auf **Gehen**, **Joggen**, **Radfahren** oder **Auto** gesetzt werden. Ohne manuelle Auswahl erfolgt eine automatische Geschwindigkeitsklassifizierung.
* 📅 **Automatische Tagesauswahl:** Nach dem Import wird automatisch der zeitlich letzte vorhandene Tag ausgewählt.
* 🎨 **Farbige Geschwindigkeits-Voranalyse:** Der Track wird automatisch nach Geschwindigkeit eingefärbt auf der Karte gezeichnet (Gehen 🟩, Joggen 🟧, Radfahren 🟪, Auto 🟥).
* ✂️ **Präzises Zuschneiden (Clipping):**
  * Klick auf die Karte, um den nächstgelegenen Punkt als Start/Ende festzulegen.
  * Hover/Klick im Diagramm für eine visuelle Auswahl.
  * Minutengenaue, manuelle Zeiteingabe mit **+1 Min / -1 Min** Buttons zur Feinjustierung.
* 📈 **Interaktives Dual-Axis Chart:** Chart.js-Diagramm für Höhen- und Geschwindigkeitsprofil. Beim Überfahren des Diagramms wandert ein Cursor synchron auf der Karte mit.
* ⏱️ **Umfangreiche Live-Statistiken:** Distanz, Dauer, Ø Geschwindigkeit, Maximalgeschwindigkeit, Aufstieg, Abstieg und Durchschnittshöhe für den ausgewählten Abschnitt.
* 💾 **Garmin-Ready GPX Export:** Standardisierte GPX-1.1-Dateien inklusive Zeit- und Höhendaten, mit getrennten Segmenten an erkannten Lücken.

---

## 💡 Typischer Workflow: Mehrere unvollständige Tracks zusammenführen

Wenn während einer Aufzeichnung ein Tracker abgestürzt ist oder du zwei Geräte parallel verwendet hast:

1. **Dateien auswählen:** Wähle alle beteiligten GPX-, CSV- oder KML-Dateien gleichzeitig aus.
2. **Merge starten:** Die App sortiert alle Punkte nach Zeit, entfernt Duplikate und führt überlappende Bereiche zusammen.
3. **Bereinigung prüfen:** Der Analyse-Report zeigt entfernte GPS-Sprünge, geglättete Höhenwerte, erkannte Lücken sowie die Anzahl zusammengeführter Overlaps.
4. **Aktivität wählen:** Stelle bei Bedarf den Aktivitätstyp manuell auf Gehen, Joggen, Radfahren oder Auto.
5. **Bereich auswählen:** Lege Start und Ende über Karte, Diagramm oder Zeitsteuerung fest.
6. **GPX exportieren:** Lücken werden als getrennte Track-Segmente exportiert; die Datei kann direkt in Garmin Connect, Strava oder Komoot importiert werden.

---

## 💡 Typischer Workflow: GPSLogger zu Garmin

Wenn deine Laufuhr das Training nicht aufgezeichnet hat oder du Akku sparen willst:

1. **Tracking:** Lass *GPSLogger* den ganzen Tag im Hintergrund als CSV mitlaufen.
2. **Import:** Lade die CSV-Datei in den *GPS Track Editor Pro*. Die App öffnet automatisch den letzten vorhandenen Tag.
3. **Identifikation:** Suche auf der Karte den passenden, farblich markierten Abschnitt.
4. **Auswahl:** Klicke auf den Beginn und wähle **Als Start**, dann auf das Ende und wähle **Als Ende**. Feinjustierung ist über die Zeit-Buttons möglich.
5. **Export:** Klicke auf **GPX Export**.
6. **Upload:** Importiere die generierte Datei in Garmin Connect, Strava oder Komoot.

---

## 🛠️ Technologien & Architektur

Diese Single-Page-Application (SPA) ist als Progressive Web App (PWA) konzipiert. Sie kann über die Browser-Funktion **Zum Startbildschirm hinzufügen** wie eine native App installiert und im Vollbildmodus auf Smartphones genutzt werden.

* **UI/UX:** HTML5, CSS3, Vanilla JavaScript – ohne schwere Frameworks für maximale Performance.
* **Karten-Rendering:** [Leaflet.js](https://leafletjs.com/) mit OpenStreetMap-Tiles.
* **Datenverarbeitung:** [PapaParse](https://www.papaparse.com/) für CSV, DOMParser für GPX/KML sowie geodätische Haversine-Berechnung für Distanzen.
* **Datenbereinigung:** Geschwindigkeits- und Position-Outlier-Filter, Median-basierte Höhenglättung, Overlap-Merging und Lückensegmentierung.
* **Datenvisualisierung:** [Chart.js](https://www.chartjs.org/) mit Dual-Axis-Konfiguration.

---

## 🤖 Entwicklung & Credits

Entwickelt von **Basecore**.
Die App-Logik, das User-Interface und die Algorithmen zur Geodaten-Analyse wurden mit Unterstützung von **Gemini 3.1 KI** (via Perplexity) entworfen und optimiert.

---

## 📝 Lizenz

Dieses Projekt ist Open-Source und unter der **MIT-Lizenz** veröffentlicht. Du kannst den Code frei verwenden, anpassen und weiterverbreiten.
