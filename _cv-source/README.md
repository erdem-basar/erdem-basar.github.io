# Lebenslauf-Quellen

Aus diesen Vorlagen werden beide PDFs erzeugt:

| Vorlage       | PDF                     |
|---------------|-------------------------|
| `cv-de.html`  | `/Lebenslauf.pdf`       |
| `cv-en.html`  | `/Erdem_Basar_CV.pdf`   |

Gemeinsames Layout und Farben (Akzent `#2dd4bf`, Hintergrund `#0b1015`) stehen in `cv.css`.
Inhaltliche Änderungen immer in **beiden** Sprachfassungen nachziehen.

## Neu rendern (A4, 2 Seiten)

In diesem Ordner einen lokalen Server starten, damit die Inter-Webfont geladen wird:

    python -m http.server 8098 --bind 127.0.0.1

Dann aus dem Repo-Stammverzeichnis:

    "C:\Program Files\Google\Chrome\Application\chrome.exe" --headless --disable-gpu --no-pdf-header-footer --print-to-pdf="Lebenslauf.pdf" "http://127.0.0.1:8098/cv-de.html"
    "C:\Program Files\Google\Chrome\Application\chrome.exe" --headless --disable-gpu --no-pdf-header-footer --print-to-pdf="Erdem_Basar_CV.pdf" "http://127.0.0.1:8098/cv-en.html"

## Achtung: Seiten sind fest 297 mm hoch

Jede Seite ist auf A4-Höhe mit `overflow: hidden` gesetzt. Was nicht passt, wird **still
abgeschnitten**, der Text bleibt aber im PDF-Textlayer. Eine Textsuche im PDF beweist also
nicht, dass etwas sichtbar ist. Nach jeder inhaltlichen Änderung das PDF ansehen und auf
Seite 2 besonders die Hauptspalte prüfen: Die deutsche Fassung hat dort nur rund 1,5 mm Luft.

Der Ordner beginnt mit `_` und wird von GitHub Pages nicht mit ausgeliefert.
