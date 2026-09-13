# AutoMotor documentation

## `BSR_AutoMotor_UserManual.pdf`

The public user manual — Edition 2. It covers the current production feature
set, including the built-in web control panel, and is written for customers and
installers. It deliberately describes **behaviour only**: no source, no internal
endpoints, no credentials, no part numbers.

## Rebuilding it

The PDF is generated, not hand-edited. The source is:

```
manual/manual.html      the whole document — edit this
manual/images/*.png     screenshots of the web control panel
```

`manual.html` is a single self-contained file with print CSS (A4, running
heads, page breaks). To rebuild, print it to PDF in two passes and join them —
the cover is rendered edge-to-edge with no running heads, the body with them,
so the cover is unnumbered and the body starts at page 1.

## Refreshing the screenshots

The images are captures of `web/automotor.html` from the firmware repository,
served locally against mock device data so every card shows realistic values.
Re-capture them the same way whenever the panel's design changes, then rebuild
the PDF.
