# trutovik-site

Statische Info-Seite auf **Russisch** über den Zunderschwamm (*Fomes fomentarius*).
Erste Fassung für den Aufbau in Kasachstan.

## Seiten
| Datei | Inhalt |
|---|---|
| `index.html` | Einstieg — „Вы наверняка знаете чагу" + Übersicht |
| `grib.html` | O грибе — Botanik, Herkunft des Namens, Ötzi |
| `sostav.html` | Состав — β-Glucane, Chitin, Melanine, Glucuronsäure |
| `nauka.html` | Наука — Kiewer Schule Gorovoj, „Mycoton", Quellen |
| `bezopasnost.html` | Статус — Novel Food EU, 5 g/Tag, Grenzen |
| `primenenie.html` | Применение — Einnahme, Erfahrungen, FAQ |
| `partneram.html` | Партнёрам — Mini-Landingpage für Partnerinnen |

Dazu: `Trutovik_Fomes_fomentarius_obzor_RU.pdf` (6 Seiten, 13 Quellen) als Download.

## Farben
Übernommen aus dem Markenmaterial des Herstellers:

| Rolle | Wert |
|---|---|
| Hintergrund (creme) | `#F7F1E9` |
| Signaturgrün (Blatt) | `#9CC63C` |
| Grün dunkel (Hover/Links) | `#74A028` |
| Waldgrün (Überschriften) | `#2E4A22` |
| Text | `#23261F` |

Schriften: Montserrat (Überschriften) + Manrope (Fließtext) — beide mit vollem Kyrillisch-Satz.

---

## 🔴 Vor dem Umzug auf eine eigene Domain

**1. `noindex` entfernen.** In **jeder** HTML-Datei steht im `<head>`:

```html
<meta name="robots" content="noindex, nofollow">
```

Das ist Absicht, solange die Seite unter `github.io` liegt — sonst indexiert Google den
Entwurf statt der späteren echten Domain. **Beim Umzug auf `trutovik.com` diese Zeile
in allen sieben Dateien löschen** und eine `sitemap.xml` ergänzen.

Ein Einzeiler dafür:
```bash
sed -i '' '/name="robots"/d' *.html
```

**2. Platzhalter ersetzen**
- `partneram.html`: `wa.me/XXXXXXXXXXX` und `t.me/XXXXXXXX`
- `index.html`: PDF-Block hat noch kein Formular — Kit anbinden
- Bilder fehlen komplett (Wald, Licht, Hände, Tee)

## Was auf dieser Seite bewusst NICHT steht
Keine Krankheitsnamen, keine Heilaussagen, keine Vorher-Nachher-Bilder, keine Preise,
keine Fristen. Der Erfahrungsblock in `primenenie.html` ist auf Alltag begrenzt —
die Regel steht als Kommentar direkt im Quelltext.

## Lokal ansehen
```bash
python3 -m http.server 8000
```
