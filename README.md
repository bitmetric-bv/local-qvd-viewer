# Local QVD Viewer

A fast, privacy-first QVD file viewer that runs entirely in your browser — no installation, no server, no data upload.

Open [index.html](index.html) locally or visit the hosted version at **[bitmetric-bv.github.io/local-qvd-viewer](https://bitmetric-bv.github.io/local-qvd-viewer)**.

---

## Features

### File loading
- Drag & drop a `.qvd` file onto the page, or click to browse
- Parsing runs in a background Web Worker — the UI stays responsive even for large files
- Supports QVD files from both Qlik Sense and QlikView

### Table
- **Virtual scrolling** — renders only visible rows, handles millions of rows without freezing
- **Column resizing** — drag column borders to resize
- **Sort** — click a column header to cycle through ascending / descending / unsorted
- **Global search** — filters across all visible columns simultaneously

### Filtering
- **Column filter dropdown** — open via right-click → Filter…, shows all unique values with counts
  - Search within the dropdown
  - Check / uncheck individual values
  - Select all / deselect all
- **Active filter bar** — shows all active filters as chips; click a chip to edit, click × to remove
- **Quick filters from the table**
  - **Double-click** a cell → immediately filter that column to that single value
  - **Ctrl+click** multiple cells in the same column → select values, then apply as a multi-value filter via the bar that appears

### Column management
- **Column chooser** panel — search, toggle individual columns, select/deselect all or just search results, pick first 20
- Closes automatically when clicking outside

### Statistics & formatting
- **Statistics popup** — per column: count, sum, average, min, max (numeric columns only)
  - Pin any statistic to a persistent row below the column headers
- **Number formatting** — set decimal places and thousands separator per column
- **Multi-column selection** — Ctrl+click column headers to select multiple columns at once; formatting and statistics pinning apply to all selected columns simultaneously

### Export
- Export visible data to **XLSX**, **CSV**, or **TXT**
- Respects active filters, column visibility, and sort order
- Configure delimiter, text qualifier, and line endings for CSV/TXT

---

## Privacy

**Your data never leaves your device.** The viewer is a single static HTML file with no external dependencies. All parsing and processing happens locally in your browser. No analytics, no network requests, no cookies.

---

## Usage

1. Download or clone this repository
2. Open `index.html` in any modern browser (Chrome, Edge, Firefox, Safari)
3. Drop a QVD file onto the page

No build step, no dependencies, no installation required.

---

## Browser support

Any modern browser with support for Web Workers, FileReader, and ES6. Internet Explorer is not supported.

---

## License

MIT — © 2026 [Bitmetric BV](https://bitmetric.nl)
