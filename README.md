# Studzinski Innenausbau & Modernisierung – Website

One-Pager (Wariant C „Präzision sichtbar”) für Studzinski Innenausbau & Modernisierung, 35410 Hungen.
Statische Seite, ohne Build-Schritt: HTML, CSS, JS und Three.js (r128, cdnjs).

## Struktur

```
index.html              Startseite (Hero, Leistungen, 3D-Wandaufbau, Projekte, Vorher/Nachher, Ablauf, Kontakt)
impressum.html          Impressum – Platzhalter [gelb] ausfüllen
datenschutz.html        Datenschutz – vor dem Livegang vervollständigen
legal.css               Styles für Impressum/Datenschutz
assets/img/*.webp       Bilder (aktuell 3D-Visualisierungen, durch echte Fotos ersetzen)
assets/logo/            Logo (voll), Lockup (Sygnet + Name), Favicon – SVG
netlify.toml            Hosting-Konfiguration (Cache-Header)
```

## Deploy auf Netlify

1. Netlify → *Add new site* → *Import an existing project* → dieses GitHub-Repo wählen.
2. Build command: leer lassen, Publish directory: `.`
3. Fertig. Jeder Push auf `main` aktualisiert die Seite.

## Kontaktformular

Läuft über **Netlify Forms** (Formularname `anfrage`), ohne zusätzlichen Code.
E-Mail-Benachrichtigung einrichten: Netlify → Site → *Forms* → *Form notifications* → *Email notification* → `info@studzinski-innenausbau.de`.
Anderer Hoster: in `index.html` die Konstante `FORM_ENDPOINT` auf eine Formspree-URL setzen.

## Bilder austauschen

Echte Fotos als WebP (ca. 1600 px lange Seite, Qualität 75–80) unter denselben Namen in `assets/img/` ablegen:

| Datei | Wo | Format |
|---|---|---|
| hero.webp | Hero | 4:5 hoch |
| p1.webp | Projekt Altbauwohnung | 5:4 |
| p2.webp | Projekt Flur | 3:4 hoch |
| p3.webp | Projekt Wohnzimmer | 4:5 hoch |
| p4.webp | Projekt Büroetage | 16:10 |
| team.webp | Handwerk | 4:5 hoch |
| before.webp / after.webp | Vorher/Nachher-Regler | 2:1, gleicher Blickwinkel |

Danach in `index.html` die Labels „Visualisierung” entfernen und die Bildunterschriften (Ort, Material) anpassen.

## Kontaktdaten

Telefon 0178 658 06 03 (`tel:+491786580603`), WhatsApp `wa.me/491786580603`, E-Mail info@studzinski-innenausbau.de.
Die Daten stehen in `index.html` (Kontakt, Footer, Mobil-Leiste, Visitenkarte, JSON-LD).

## Offene Punkte vor dem Livegang

- [ ] Impressum: Inhaber, Adresse, USt-IdNr./Steuernummer, Handwerkskammer
- [ ] Datenschutzerklärung vollständig
- [ ] Echte Projektfotos statt Visualisierungen
- [ ] Zahlen in „Handwerk” (Jahre, Projekte)
- [ ] Optional: Google Fonts und Three.js lokal einbinden (DSGVO)
