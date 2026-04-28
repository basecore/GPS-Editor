# 🗺️ GPS Track Editor Pro

[![Version](https://img.shields.io/badge/version-1.3.0-blue.svg)](https://basecore.github.io/GPS-Editor/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PWA](https://img.shields.io/badge/PWA-Ready-success.svg)](https://basecore.github.io/GPS-Editor/)
[![AI](https://img.shields.io/badge/AI_Generated-Gemini_3.1-8A2BE2.svg)](#)

Eine professionelle, komplett lokal im Browser laufende und Smartphone-optimierte Web-App (PWA) zur Visualisierung, detaillierten Analyse und zum präzisen Zuschneiden von GPS-Daten. 

Besonders optimiert für den **Import von fortlaufenden GPS-Logs (z. B. aus der App *GPSLogger*)**, um spezifische Aktivitäten (wie Jogging-Runden oder Radtouren) aus einem ganzen Tages-Track zu extrahieren und als saubere GPX-Datei für Sportplattformen wie **Garmin Connect, Strava oder Komoot** zu exportieren.

🚀 **[Live-Demo öffnen (App direkt im Browser starten)](https://basecore.github.io/GPS-Editor/)**

---

## ✨ Key Features

*   🔒 **Privacy-First (100% Lokal):** Alle Berechnungen, Analysen und Dateiexporte finden ausschließlich im Speicher deines Browsers statt. Es werden keine Standortdaten an externe Server gesendet.
*   📊 **Multiformat-Import:** Unterstützt `.csv` (perfekt für *GPSLogger*), `.gpx` und `.kml` Dateien inkl. Lade-Indikator bei großen Dateien.
*   🎨 **Farbige Geschwindigkeits-Voranalyse:** Der Track wird automatisch nach Geschwindigkeit eingefärbt auf der Karte gezeichnet (Gehen 🟩, Joggen 🟧, Radfahren 🟪, Auto 🟥). Aktivitäten sind so auf einen Blick erkennbar.
*   ✂️ **Präzises Zuschneiden (Clipping):**
    *   Klick auf die Karte, um den nächstgelegenen Punkt als Start/Ende festzulegen.
    *   Hover/Klick im Diagramm für eine visuelle Auswahl.
    *   Minutengenaue, manuelle Zeiteingabe mit komfortablen **+1 Min / -1 Min** Buttons zur Feinjustierung.
*   📈 **Interaktives Dual-Axis Chart:** Ein professionelles Chart.js-Diagramm, das sowohl das Höhen- als auch das Geschwindigkeitsprofil des ausgewählten Ausschnitts zeigt. Fährst du über das Diagramm, wandert ein Cursor synchron auf der Karte mit!
*   ⏱️ **Umfangreiche Live-Statistiken:** Berechnet sofort Distanz, Dauer, Ø Geschwindigkeit, Maximalgeschwindigkeit, Aufstieg, Abstieg und Durchschnittshöhe für den ausgewählten Abschnitt.
*   💾 **Garmin-Ready GPX Export:** Generiert auf Knopfdruck saubere, standardisierte GPX 1.1 Dateien inkl. Zeit- und Höhendaten zum direkten Upload in dein Sport-Ökosystem.

---

## 💡 Typischer Workflow (Der GPSLogger -> Garmin Use-Case)

Wenn deine Laufuhr das Training nicht aufgezeichnet hat oder du schlicht Akku sparen willst:

1.  **Tracking:** Lass die App *GPSLogger* ressourcenschonend im Hintergrund deines Smartphones den ganzen Tag als CSV mitlaufen.
2.  **Import:** Lade die CSV-Datei am Abend in den *GPS Track Editor Pro*. Die App zoomt automatisch auf den gesamten Tages-Track.
3.  **Identifikation:** Suche auf der Karte nach dem orangefarbenen Abschnitt (Joggen, 7-15 km/h).
4.  **Auswahl:** Klicke auf den Beginn der orangenen Linie und wähle "Als Start". Klicke auf das Ende und wähle "Als Ende". Nutze ggf. die Zeit-Buttons für die Sekunden-genaue Justierung.
5.  **Export:** Klicke auf "Auswahl als GPX Exportieren".
6.  **Upload:** Importiere die generierte Datei nahtlos in **Garmin Connect**. Alle Zeiten, Höhenmeter und Geschwindigkeiten werden perfekt übernommen!

---

## 🛠️ Technologien & Architektur

Diese Single-Page-Application (SPA) ist als Progressive Web App (PWA) konzipiert. Sie kann über die Browser-Funktion "Zum Startbildschirm hinzufügen" wie eine native App installiert und im Vollbildmodus auf Smartphones genutzt werden.

*   **UI/UX:** HTML5, CSS3, Vanilla JavaScript (keine schweren Frameworks wie React/Angular für maximale Performance).
*   **Karten-Rendering:** [Leaflet.js](https://leafletjs.com/) mit OpenStreetMap-Tiles.
*   **Datenverarbeitung:** [PapaParse](https://www.papaparse.com/) (für schnelle CSV-Analysen) und Geodätische Haversine-Formel für Distanzberechnungen.
*   **Datenvisualisierung:** [Chart.js](https://www.chartjs.org/) (Dual-Axis Konfiguration).

---

## 🤖 Entwicklung & Credits

Entwickelt von **Basecore**.  
Die App-Logik, das User-Interface und die Algorithmen zur Geodaten-Analyse wurden mit Unterstützung von **Gemini 3.1 KI** (via Perplexity) am 28. April 2026 entworfen und optimiert.

---

## 📝 Lizenz

Dieses Projekt ist Open-Source und unter der **MIT-Lizenz** veröffentlicht. Du kannst den Code frei verwenden, anpassen und weiterverbreiten.
