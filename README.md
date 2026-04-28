# GPS Track Analyzer & Editor 🗺️🏃‍♂️

Eine leichtgewichtige, im Browser laufende Web-App (SPA) zur Visualisierung, Analyse und Bearbeitung von GPS-Daten. Speziell optimiert für Smartphones und den Export von zugeschnittenen Trainingseinheiten (z.B. für Garmin Connect).

## ✨ Funktionen

*   **Lokale Verarbeitung (Privacy-First):** Alle Dateien werden direkt im Browser per JavaScript verarbeitet. Es werden **keine** GPS-Daten an Server gesendet.
*   **Format-Support:** Importiert `.csv`, `.gpx` und `.kml` Dateien.
*   **Aktivitäts-Erkennung:** Berechnet Distanz und Durchschnittsgeschwindigkeit und schätzt die Aktivität ab (Gehen, Joggen, Radfahren, Autofahren).
*   **Interaktiver Zuschnitt:** Durch einfaches Tippen auf die Wegstrecke auf der Karte können Start- und Endpunkt für einen Export festgelegt werden.
*   **Garmin-kompatibler Export:** Generiert saubere `.gpx`-Dateien des ausgewählten Bereichs.
*   **Open-Source Karte:** Nutzt OpenStreetMap über Leaflet.js.

## 🚀 Nutzung

1.  Öffne die Web-App auf deinem Smartphone oder PC.
2.  Klicke auf **Importieren** und wähle deine GPS-Datei aus.
3.  Die App zeichnet den Track in Blau auf die Karte und zeigt die Auswertung an.
4.  Tippe auf den Pfad, um den Startpunkt der Auswahl zu markieren.
5.  Tippe auf eine zweite Stelle, um den Endpunkt zu markieren (die Auswahl färbt sich rot).
6.  Klicke auf **Auswahl als GPX Exportieren**. Die neue Datei wird heruntergeladen.

## 🛠️ Technologien

*   [HTML5 / CSS3 / Vanilla JavaScript](https://developer.mozilla.org/de/docs/Web)
*   [Leaflet.js](https://leafletjs.com/) (Karten-Rendering)
*   [PapaParse](https://www.papaparse.com/) (CSV-Verarbeitung)

## 📝 Lizenz

Dieses Projekt ist unter der MIT-Lizenz veröffentlicht.
