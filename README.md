# PDF Kompressor (Auslieferung)

Fertig gebaute Browser-Version des PDF Kompressors von Halbstark. Macht Figma-PDF-Exporte
versandfertig: Seiten zusammenführen und sortieren, Bilder auf ihre tatsächliche
Darstellungsgröße bringen, doppelte Inhalte nur einmal speichern.

Druckmodus: Farben nach CMYK (ISO Coated v2 300 %), Text in reinem Schwarz, Farbauftrag
höchstens 300 %, gespiegelter Beschnitt, PDF/X-4 mit Output-Intent.

Die Verarbeitung läuft vollständig im Browser. PDFs werden nirgendwohin hochgeladen.

## Einbinden

An einen Commit gebunden (unveränderlich) und mit Prüfsumme. Die aktuelle Prüfsumme steht in
`integrity.json`, die Worker-Dateien prüft `pdfk.js` beim Laden selbst.

```html
<script type="module" crossorigin="anonymous"
  src="https://cdn.jsdelivr.net/gh/Flozilla97/pdf-kompressor@COMMIT/pdfk.js?mount"
  integrity="sha384-…"></script>
```

Alle Dateien müssen im selben Ordner liegen: `pdfk.js`, `pdfk-worker.js`, `pdf.worker.min.mjs`
und für den Druckmodus `print-isocoated-v2-300.bin` (Farbtabellen) und `isocoated-v2-300.icc`
(Ausgabeprofil). Beide werden erst geladen, wenn jemand auf Druck stellt, und wie die Worker
gegen ihre Prüfsumme geprüft. Mitgelieferte Bibliotheken und ihre Lizenzen: siehe `THIRD_PARTY_LICENSES.txt`.
