# PDF Kompressor (Auslieferung)

Fertig gebaute Browser-Version des PDF Kompressors von Halbstark. Macht Figma-PDF-Exporte
versandfertig: Seiten zusammenführen und sortieren, Bilder auf ihre tatsächliche
Darstellungsgröße bringen, doppelte Inhalte nur einmal speichern.

Die Verarbeitung läuft vollständig im Browser. PDFs werden nirgendwohin hochgeladen.

## Einbinden

An einen Commit gebunden (unveränderlich) und mit Prüfsumme. Die aktuelle Prüfsumme steht in
`integrity.json`, die Worker-Dateien prüft `pdfk.js` beim Laden selbst.

```html
<script type="module" crossorigin="anonymous"
  src="https://cdn.jsdelivr.net/gh/Flozilla97/pdf-kompressor@COMMIT/pdfk.js?mount"
  integrity="sha384-…"></script>
```

Die drei Dateien `pdfk.js`, `pdfk-worker.js` und `pdf.worker.min.mjs` müssen im selben Ordner
liegen. Mitgelieferte Bibliotheken und ihre Lizenzen: siehe `THIRD_PARTY_LICENSES.txt`.
