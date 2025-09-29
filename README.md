[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)

# Veilbeam

Veilbeam ist ein kleines Browser-Tool zum lokalen Anonymisieren von Gesichtern in Bildern. Es bietet Verpixelung (Pixelate) und Blur‑Effekt, unterstützt manuelle Auswahl von Bereichen und vorbereitet Integration automatischer Gesichtserkennung.

## Hauptfunktionen
- Bild lokal öffnen per Drag & Drop oder Dateiauswahl.
- Bereiche manuell markieren: Rechteck, Kreis, Polygon.
- Effekte:
  - Verpixeln (Pixelgröße steuerbar).
  - Blur (Radius steuerbar).
- Mehrere Bereiche verwalten: anwenden, aktiv/deaktivieren, löschen.
- Vorschau mit Maskierung und Overlay.
- Export als PNG/JPG.

## Bedienung (Kurz)
- Bild laden: Ziehe ein Bild auf die Fläche oder klicke zum Auswählen.
- Bereich erstellen: Ziehen mit der Maus oder Polygon-Modus.
- Auswahl anwenden: "Anwenden (alle neuen)" → Bereich wird in die angewendeten Bereiche übernommen und gerendert.
- Effekt wählen: "Verpixeln" oder "Blur" und Regler anpassen.
- Tastatur:
  - Leertaste toggelt Aktiv/Passiv einer Auswahl (wenn markiert).
  - Pfeiltasten ändern Pixelgröße / Blur-Radius (mit Shift größere Schritte).
  - Entf löscht markierte Bereiche.

## Unterstützte Formate
PNG, JPEG, WEBP, GIF, BMP, TIFF.

## Datenschutz / Architektur
Alles läuft vollständig im Browser — keine Daten werden hochgeladen. Das Tool arbeitet mit Canvas-Rendering und temporären Object-URLs für geladene Dateien. 

## Nutzung
Öffne [index.html](index.html) im Browser (lokal) oder nutze einen einfachen lokalen Server, um CORS/Objekt-URL-Verhalten zu vermeiden.

Logo: [logo_veilbeam.png](logo_veilbeam.png)  

## Lizenz

MIT License – siehe [`LICENSE`](LICENSE).

---

## Autor

© 2025 Wolfgang Saal, Böllenborn

