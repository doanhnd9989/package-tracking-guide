# Your Spreadsheet Is Quietly Breaking Your Tracking Numbers

**Short answer:** a spreadsheet treats a long run of digits as a *quantity*, and quantities get
rounded and reformatted. A tracking number is a *label* — every character matters. Paste a 20- or
22-digit number into a default-formatted column and the cell can come back as
`9.2144904245500004E+21`, or, far worse, as the same length with the final digit turned into a
zero. Format the column as **Text before you paste**, and nothing is lost.

---

## The two failure modes

There are two, and the second one is the dangerous one because nothing on screen looks wrong.

**1. Scientific notation — visible.**

```
you typed   9214490424550000386431
cell holds  9.2144904245500004E+21
```

This is ugly but at least obvious. You can see something happened and go fix it.

**2. Silent truncation — invisible.**

```
you typed   9400150206217912
cell holds  9400150206217910
```

Same length. No exponent. No warning triangle. The last digit has simply become a zero. If you
copy that column into a tracking site you will get "not found" for a parcel that is perfectly
fine, and you will spend the afternoon blaming the carrier.

## Why it happens

Most spreadsheets store numbers as IEEE-754 double-precision floating point, which holds about 15–17
significant decimal digits. Common tracking formats are longer than that:

| Format | Digits | Fits in a float? |
|---|---|---|
| USPS IMpb | 22 | no |
| FedEx Ground | 15 | borderline |
| DPD parcel number (many countries) | 14 | yes, but still reformatted |
| UPS `1Z` + 16 | 18 characters, has letters | safe — letters force text |
| S10 international postal (`AA999999999CC`) | 13 characters, has letters | safe |

Notice the pattern: **the formats that survive are the ones containing letters**, because a letter
forces the cell to be text. The all-digit formats are the ones at risk — and they include the most
common one in the world, the 22-digit USPS barcode.

This is also why the problem seems to come and go. A column of UPS numbers behaves perfectly, so
people conclude spreadsheets are fine, and then the first USPS batch of the month is silently
mangled.

## The fix, in order of reliability

1. **Format the column as Text before the first paste.** In Excel: select the column →
   Format Cells → Text. In Google Sheets: Format → Number → Plain text. Do this on an *empty*
   column. Formatting a column that already holds broken values does not bring the digits back —
   the information is gone, not hidden.
2. **Import from CSV with the column typed as Text** rather than double-clicking the file. Excel's
   "Get Data / From Text" flow lets you set the column type during import; double-clicking applies
   the defaults, which is what breaks it.
3. **Use a template that already has the column set to Text.** If a tracking tool offers an import
   template, download it rather than building your own sheet. 24hTrack's import template ships with
   the tracking-number column pre-set to Text for exactly this reason.
4. **Never retype by hand.** Every manual retype is a chance to transpose two digits, and a
   transposed digit fails in the same silent way.

## How to check a column you already have

Three quick tests, cheapest first:

- **Look for `E+`.** Any cell showing scientific notation is broken.
- **Check the lengths.** In a spare column put `=LEN(A2)` and fill down. USPS numbers should all be
  22; a column that is mostly 22 with a few 21s or 23s has a problem. A column where everything is
  the right length can still be broken by rounding, which is why the next test matters.
- **Check the endings.** `=RIGHT(A2,1)` filled down. If an implausible share of your numbers end in
  `0`, you are looking at rounding, not coincidence.

If a column is already damaged, the only real fix is to re-export it from wherever it came from —
the shop's order system, the carrier's portal, the marketplace — into a Text-formatted column.

## If you are moving lists around regularly

Round-tripping a list through a spreadsheet by hand is where these numbers get damaged. If you do
it often, move the list without retyping it:

- Import the file directly into a tracker and let it read the file, rather than copying cells between
  windows. 24hTrack accepts .xlsx and .csv up to 50,000 rows, reads the file in the browser, and
  shows you a count of rows found, rows ready and rows skipped — with the reason for each skip —
  before anything is added.
- Export the statuses back out as a sheet instead of pasting results in by hand. You keep your own
  formulas and filters, on values nobody retyped.
- For a list that changes continuously, sync a Google Sheet so the status column updates itself.
  On 24hTrack that sync is free.

## Related

- [How to track several packages at once](track-multiple-packages-at-once.md)
- [Track packages in Google Sheets](track-packages-in-google-sheets.md)
- [Tracking number formats by carrier](tracking-number-formats.md)
- [Order number vs tracking number](order-number-vs-tracking-number.md)

---

*Part of the [package-tracking-guide](../README.md) reference set, maintained by the team behind
[24hTrack](https://www.24htrack.com) — a free package tracker covering 3,200+ carriers, where you
paste any tracking number and the carrier is detected automatically, no sign-up. CC BY 4.0.*
