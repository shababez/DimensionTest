# Dimension Measurement Form

A single-file web page (`index.html`) for dimension measurement sheets.

- Take a photo of a handwritten sheet. A vision model reads the column names, printed spec limits, header fields and the 30 sample rows into a table.
- Out-of-spec values turn red. Digits the reader is unsure about turn yellow. Every cell can be edited.
- Avg, Max and Min are calculated automatically.
- Export to Excel (with live formulas) or PDF.
- You can also key values in by hand: type the column names and tap "Apply columns".

## How to run

1. Open `index.html` in a browser (double-click it), or host it with GitHub Pages or any static web server.
2. To read photos, open "Reader settings" and enter an API key, the model name and the API address.
3. Choose a photo, tap "Read the paper", check the red and yellow cells against the paper, then download.

## Privacy and security

- Photos are sent to the API address in the settings. Use only a key and an address approved by your organisation.
- The API key is stored in the browser tab only (`sessionStorage`) and is cleared when the tab closes. **Never write a key into the code or commit it.**
- Because the key is entered in the browser, this page is meant for personal or internal use. For wider use, put the API call behind your own server and change the API address.
- Entered data is saved in the browser (`localStorage`) on that device. Use "Clear measurements" after each report.
- The repository contains no company names, document numbers or specification limits. Keep it that way if your sheets are confidential, and use a private repository.

## Notes

- Handwriting reading is not perfect. Always compare the highlighted cells with the paper.
- Excel, PDF libraries are loaded from cdnjs when the page opens, so internet access is needed.
