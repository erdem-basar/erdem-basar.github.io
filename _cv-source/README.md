# CV-Quelle (englisch)

`cv-en.html` ist die Vorlage, aus der `/Erdem_Basar_CV.pdf` erzeugt wird.
Layout, Farben (Akzent `#2dd4bf`, Hintergrund `#0b1015`) und Satzspiegel sind dem
deutschen `Lebenslauf.pdf` nachgebaut.

Neu rendern (A4, 2 Seiten):

    "C:\Program Files\Google\Chrome\Application\chrome.exe" ^
      --headless --disable-gpu --no-pdf-header-footer ^
      --print-to-pdf="...\Erdem_Basar_CV.pdf" "http://127.0.0.1:8098/cv-en.html"

Die Datei muss ueber HTTP ausgeliefert werden (z. B. `python -m http.server 8098`
in diesem Ordner), damit die Inter-Webfont geladen wird.

Beide Seiten sind auf feste 297 mm Hoehe gesetzt und `overflow: hidden` — nach
inhaltlichen Aenderungen also pruefen, ob unten nichts abgeschnitten wird.

Der Ordner beginnt mit `_` und wird von GitHub Pages nicht mit ausgeliefert.
