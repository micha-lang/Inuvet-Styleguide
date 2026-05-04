# inuvet Styleguide — Arbeitsregeln für Claude

## Grundprinzip

Vor jeder neuen Komponente oder Klasse: `inuvet.css` lesen und prüfen, ob das Muster bereits existiert. Nichts neu erfinden, was schon definiert ist.

## Klassen und Tokens

- Keine neuen CSS-Klassen für Dinge, die bereits existieren (z.B. `.section-label`, `.label-caps`, `.btn.--full`, `.form-field`, `.form-grid`, `.form-check`, `.form-upload`)
- Keine neuen Design-Tokens — nur die in `:root` definierten verwenden (`--module`, `--half-module`, `--base`, `--text-xs/base/m/l/xl`, `--fg`, `--green`, etc.)
- Kein `!important`
- Kein `text-align: center` — im gesamten Styleguide nicht definiert und nicht verwendet
- Kein `border-radius` — überall `0`, keine Ausnahmen
- Keine Inline-Styles für Spacing, Farben oder Typografie — immer Tokens und Klassen

## Formulare

- Zwischenüberschriften: `<h3 class="section-label">` — wie im Demo "Komplexes Formular (mit Zwischenrubriken)"
- Felder: `.form-field` mit Floating Label (Input vor Label im DOM)
- Mehrspaltig: `.form-grid` (2 Spalten); volles Feld: `style="grid-column: span 2"`
- Checkboxen/Radios: `.form-check`
- Datei-Upload: `.form-upload`
- Button Absenden: `.btn.--primary.--full`

## Typografie

- Schriftgrößen ausschließlich über Tokens: `--text-xs`, `--text-base`, `--text-m`, `--text-l`, `--text-xl`
- Token `--text-h1`, `--text-h2` existieren NICHT
- Headline einer Seite: `--text-l` oder `--text-xl`, Farbe `--fg`, linksbündig

## Abstände

- Abstände immer als Vielfache von `--module` (3rem) oder `--half-module` (1.5rem)
- Pixel-Werte für Abstände vermeiden

## Neue Dateien

- Formular-spezifische Styles kommen in `formulare.css` (gilt für alle `Formular-*.html`)
- Styles, die potenziell global nützlich sind, am Ende der Session als Kandidaten für `inuvet.css` vorschlagen

## Preview-Server

- Läuft auf `http://localhost:3456`
- Nach Änderungen, die im Browser sichtbar sind: Verifikation via Preview-Tools durchführen

## Assets

- Lokale Pfade: `assets/images/`, `assets/lotties/`, `assets/graphics/`, `assets/videos/`
- Kein CDN für Produktbilder — lokale Dateien verwenden
- Logo: Inline-SVG aus dem Styleguide-Nav verwenden (nicht als `<img src="...">`)
