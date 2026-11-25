# Assay Tools

Small browser-based calculators and viewers for assay work. Each tool is a single static HTML file with no install, no server and no dependencies. Everything runs in your browser; files you load are never uploaded.

Live site: https://chauh08.github.io/assay-tools/

| Tool | File | What it does |
|---|---|---|
| Dispense calculator | [`index.html`](https://chauh08.github.io/assay-tools/index.html) | Per-well dispense volumes from a stock in mM (100% DMSO), with 2.5 nL snapping, solvent backfill and intermediate-to-final plate dilution steps. |
| Stock solution calculator | [`unit-converter.html`](https://chauh08.github.io/assay-tools/unit-converter.html) | Guided flow from mass, molecular weight and target mM to the solvent volume needed. |
| Concentration converter | [`concentration-converter.html`](https://chauh08.github.io/assay-tools/concentration-converter.html) | Converts between M, mM, µM, nM, pM and mg/mL, µg/mL, ng/mL, % w/v (molecular weight needed for molar to mass). |
| Plate map viewer | [`plate-map.html`](https://chauh08.github.io/assay-tools/plate-map.html) | Heatmap of 96/384/1536-well plates from Echo transfer files, Mosaic dispatch files or any plate list (`.csv`, `.xls`, `.xlsx`). Shows volume, concentration, sample ID and batch per well. |

## Plate map viewer

- Load several files at once; remove files individually or all together.
- Header names don't have to match exactly. It finds the header row and recognises common variants (barcode, well/position, conc, sample ID, batch/lot, MW and so on).
- Colour by volume, concentration or sample/batch. Hover a well for full details.
- **Export** the selected plates/views as an Excel workbook (coloured plate map and/or well list), a CSV well list, or PNG images. You choose the views, sheets and columns. Every export lists the destination plate barcodes of the selected views.
- When embedded in a page, dropping a file opens the viewer in a new tab (falls back to showing it in place if pop-ups are blocked).

## Embedding in SharePoint

Add an Embed web part and paste an iframe, for example:

```html
<iframe src="https://chauh08.github.io/assay-tools/plate-map.html" width="100%" height="1300" style="border:0;" title="Plate Map Viewer"></iframe>
```

A SharePoint admin must first allow `chauh08.github.io` under **HTML Field Security**.

## Running locally

Open any `.html` file in a modern browser (recent Chrome or Edge; `.xlsx` reading needs `DecompressionStream`).
