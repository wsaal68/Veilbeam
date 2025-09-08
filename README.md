[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)

# Veilbeam

Veilbeam ist ein kleines Browser-Tool zum lokalen Anonymisieren von Gesichtern in Bildern. Es bietet Verpixelung (Pixelate) und Blur‑Effekt, unterstützt manuelle Auswahl von Bereichen und vorbereitet Integration automatischer Gesichtserkennung.

Live-Demo / Hauptdatei: [index.html](index.html)

## Hauptfunktionen
- Bild lokal öffnen per Drag & Drop oder Dateiauswahl ([`handleFile`](index.html)).
- Bereiche manuell markieren: Rechteck, Kreis, Polygon.
- Effekte:
  - Verpixeln (Pixelgröße steuerbar) — Implementierung: [`pixelateSelection`](index.html).
  - Blur (Radius steuerbar) — Implementierung: [`blurSelection`](index.html).
- Mehrere Bereiche verwalten: anwenden, aktiv/deaktivieren, löschen.
- Vorschau mit Maskierung und Overlay; Composite-Rendering: [`renderCompositePixelation`](index.html).
- Export als PNG/JPG (Download-Buttons).

## Bedienung (Kurz)
- Bild laden: Ziehe ein Bild auf die Fläche oder klicke zum Auswählen.
- Bereich erstellen: Ziehen mit der Maus (rechteck/kreis) oder Polygon-Modus.
- Auswahl anwenden: "Anwenden (alle neuen)" (`#applyAllBtn`) → Bereich wird in die angewendeten Bereiche übernommen und gerendert.
- Effekt wählen: "Verpixeln" oder "Blur" und Regler (`#blockSize`, `#blurRadius`) anpassen.
- Tastatur:
  - Leertaste toggelt Aktiv/Passiv einer Auswahl (wenn markiert).
  - Pfeiltasten ändern Pixelgröße / Blur-Radius (mit Shift größere Schritte).
  - Entf löscht markierte Bereiche.

## Unterstützte Formate
PNG, JPEG, WEBP, GIF, BMP, TIFF (siehe Dateiprüfung in [`handleFile`](index.html)).

## Datenschutz / Architektur
Alles läuft vollständig im Browser — keine Daten werden hochgeladen. Das Tool arbeitet mit Canvas-Rendering und temporären Object-URLs für geladene Dateien. App‑Metadaten: [`APP_VER`](index.html) = 2.2.0, Build = [`BUILD_TS`](index.html).

## Entwicklung
Öffne [index.html](index.html) im Browser (lokal) oder nutze einen einfachen lokalen Server (z. B. `npx http-server`), um CORS/Objekt-URL-Verhalten zu vermeiden.

Wichtige Funktionen im Code (zum schnellen Nachschlagen):
- [`handleFile`](index.html)
- [`pixelateSelection`](index.html)
- [`blurSelection`](index.html)
- [`renderCompositePixelation`](index.html)
- [`applyAll`](index.html)
- Download/Export-Logik: `download` (in [index.html](index.html))

Logo: [logo_veilbeam.png](logo_veilbeam.png)  

## Lizenz

MIT License – siehe [`LICENSE`](LICENSE).

---

## Autor

© 2025 Wolfgang Saal, Böllenborn

