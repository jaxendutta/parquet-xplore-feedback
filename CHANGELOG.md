# Changelog

All notable changes to the **Parquet Xplore** extension will be documented in this file.

## 0.1.1

- **Dedicated Date & Timestamp Inspector**:
  - Pure `DATE` columns now open a focused chronology card with full calendar view, weekday, day of year, days remaining, ISO week number, quarter, epoch days, and leap year detection without irrelevant clocks or UTC assumptions.
  - `TIMESTAMP` columns open an interactive inspector featuring a monthly calendar, dual UTC and Local analog clocks side-by-side, and an equirectangular world map with live meridian hover readouts and timezone abbreviations (e.g. `JST/KST`, `EST`, `UTC+4:00`).
  - Month navigation with target date resets and multi-date highlighting across month boundaries when UTC and local time span different calendar days.
- **Autosize Column Widths**:
  - Added **Autosize Column Widths** action in the Options menu with one-click calculation snapping all columns to fit their longest content without wrapping or truncating.
  - Double-clicking any column resize handle in the header row now autosizes that individual column.
- **Distinct Type Signifiers & Cell Badges**:
  - Replaced generic JSON tags with dedicated semantic icons: Struct (`{ }`), List (`[ ]`), Date (calendar), Timestamp (clock), and Text (`=`).
  - True/False boolean values formatted with borderless monospace tags (green for `true`, red highlight for `false`).
  - Binary/BLOB cells feature zero-border-radius hex tags with byte length counters.
- **Cell Ergonomics**:
  - Single-clicking standard cells triggers an instant copy to clipboard with a brief visual pulse animation.
  - Single-clicking complex/inspectable cells (Struct, List, Date, Timestamp, BLOB, multiline text) directly launches the inspector dialog.
- **Showcase Visual Walkthroughs**:
  - Added high-definition demo walkthrough GIFs hosted via raw CDN for instant rendering in VS Code Marketplace and Open VSX.

## 0.1.0

- **Initial Release**:
  - Ultra-fast byte-range lazy loading for Apache Parquet files—opens multi-gigabyte datasets in milliseconds without memory bloat.
  - Virtualized high-performance data grid with multi-column sorting, row pagination, and selectable row group navigation.
  - Interactive filter row with comparison operators (`>`, `>=`, `<`, `<=`, `!=`/`<>`, `NULL`, `NOT NULL`) and live substring search highlighting.
  - Multiline cell word wrap with dynamic auto-height row re-measurement.
  - Right-click cell context menu with quick filter and clipboard copying.
  - Real-time column profiler bar featuring distribution histograms for numeric columns and completeness bars for text columns.
  - Parquet File Overview diagnostics modal detailing format version, compression codecs, row group chunk breakdowns, schema types, and custom key-value metadata (including embedded `ARROW:schema`).
  - 8 export formats: CSV, TSV, JSON, JSON Lines (NDJSON), Markdown, HTML, XML, and SQL INSERT statements.
  - Seamless VS Code Dark Modern, Light, and System theme support.
  - Cross-platform web extension support (runs in desktop VS Code, vscode.dev, and github.dev).
