# Abdelrahman O. Sawy — LaTeX Resume

**Generated:** 2026-03-27
**Target:** 2-page ATS-optimized academic/industry hybrid resume, US market

---

## Files

| File | Purpose |
|------|---------|
| `main.tex` | Complete resume document |
| `preamble.sty` | Style file: fonts, colors, spacing, section formatting |
| `README.md` | This file |
| `NOTES.md` | All enhancements and additions beyond the original resume (verify accuracy) |

---

## Compiling on Overleaf

1. Go to [overleaf.com](https://overleaf.com) and create a new project → **Upload Project**
2. Zip both `main.tex` and `preamble.sty` together and upload the zip
3. Set the compiler to **pdfLaTeX** (Project Settings → Compiler)
4. Click **Compile** — compile **twice** to resolve hyperref cross-references
5. Download the PDF

---

## Required Packages (all available on Overleaf / TeX Live)

All packages are standard TeX Live 2023+ / Overleaf packages — no special installs needed:

| Package | Purpose |
|---------|---------|
| `geometry` | Page margins |
| `fontenc` + `inputenc` | Encoding |
| `charter` | Body font (Bitstream Charter — professional serif) |
| `microtype` | Improved kerning and hyphenation |
| `xcolor` | Accent color (navy `#1F3A5F`) |
| `titlesec` | Section heading formatting |
| `enumitem` | Bullet list customization |
| `hyperref` | Clickable hyperlinks + PDF metadata |

---

## Local Compilation (if you have TeX Live or MiKTeX)

```bash
pdflatex main.tex
pdflatex main.tex   # run twice for hyperref
```

---

## Customization Notes

- **Accent color:** Change `navyblue` hex in `preamble.sty` line 24
- **Margins:** Adjust `top`, `bottom`, `left`, `right` in `preamble.sty` lines 15–20
- **Font size:** Change `10pt` in `\documentclass[10pt, letterpaper]{article}` to `10.5pt` or `11pt`
- **LinkedIn/GitHub URLs:** Update the two `\href` entries in `main.tex` header section
- **Page count:** Currently tuned for exactly 2 pages at 10pt/charter. Increasing font size will push to 3 pages; decrease margins or reduce content if needed.

---

## ATS Compatibility Notes

This resume is designed for ATS (Applicant Tracking System) parsing:

- No tables used for layout (dates use `\hfill`, not `tabular`)
- No graphics, icons, or images
- All text is embedded and extractable
- Standard section names: Profile, Education, Technical Skills, Research Experience, Teaching Experience, Professional Experience, Projects & Competitions, Leadership & Entrepreneurship, Relevant Coursework
- Hyperlinks are plain text that ATS can read even if hyperref colors don't render
- Font (Charter) embeds cleanly in PDF — no character mapping issues
