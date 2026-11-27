# Importing and downloading

## Import a file

**File ▾ › Import Excel or CSV…**, or **Import Excel or CSV** on a new sheet.

| Format | Supported |
|---|---|
| Excel workbook (`.xlsx`, `.xlsm`) | Yes: all sheets, values, formulas, formatting, number formats, merged cells, column widths, row heights, frozen panes |
| CSV (`.csv`), tab-separated (`.tsv`, `.txt`) | Yes. Comma, semicolon, tab and pipe separators are detected automatically |
| Old Excel (`.xls`) | No. Open it in Excel, choose File › Save As › Excel Workbook (.xlsx), and import that |

- Files up to 50 MB.
- Importing replaces the current sheet. Cellar asks first, and the previous
  version stays in history.
- Text that looks like a formula in a CSV stays as text, so nothing runs
  unexpectedly.

## Import a table from the page

**File ▾ › Import a table from this page…** lists the Confluence tables on the
page. Pick one and it becomes a sheet, with the first row as a bold header. The
original table stays on the page.

## Download

**File ▾ › Download as Excel (.xlsx)** downloads every sheet with formulas and
formatting. **Download first sheet as CSV** downloads the first sheet's values.

Anyone who can view the page can download, including read-only viewers.

## PDF and Word export

When a page is exported to PDF or Word from Confluence's **•••** menu, each sheet
appears as a table (up to the first 500 rows and 50 columns per sheet).
