# SheetFlow – Vercel Starter

SheetFlow är ett **command-first kalkylbladsverktyg**. Användaren skriver vad den vill göra, SheetFlow bygger celler och visar den Excel-liknande formeln.

## Testa

Öppna `index.html` direkt i webbläsaren.

Exempel:

- `250 + 350 =`
- `25% av 800`
- `600-25%`
- `(350+250)-25%`
- `350+250=-25%` – SheetFlow ber om bekräftelse
- `summera 120 350 490 210`
- `medel 10 15 25 40`

Du kan även trycka **Σ Summera**, **Ø Medel** eller **📊 Diagram** och därefter markera befintliga celler.

## Projektstruktur

```text
sheetflow/
├── index.html
├── css/sheetflow.css
├── data/functions.js
└── js/
    ├── app.js
    ├── parser.js
    ├── spreadsheet.js
    ├── suggestions.js
    └── charts.js
```

`data/functions.js` är början på SheetFlows **lexikon i bakgrunden**.

## GitHub

Packa upp ZIP-filen och lägg **innehållet i mappen `sheetflow`** i roten av ditt GitHub-repo. `index.html` ska alltså ligga direkt i repots rot.

## Vercel

1. Add New → Project.
2. Importera ditt GitHub-repo `sheetflow`.
3. Framework Preset: **Other**.
4. Ingen Build Command behövs.
5. Ingen Output Directory behövs.
6. Deploy.

Det här är en ren statisk webbapp, så den behöver ingen server eller databas.

## Säkerhetsregel

SheetFlow ska **inte gissa befintliga cellreferenser**:

- entydigt → utför
- tvetydigt → fråga/bekräfta
- befintliga data → be användaren markera
- okänt → säg att funktionen ännu inte stöds

## Nästa steg

- större funktionslexikon
- kraftigare uttrycksparser med parenteser/operatorprioritet
- text och rubriker i arket
- OM/IF-flöde
- XLOOKUP/sökflöde
- datumfunktioner
- villkorsstyrd formatering
- bättre diagram
- riktig XLSX-export med formler
- PDF-export
- lokal projektsparning
- flera blad

> Den här versionen är en utvecklingsprototyp, inte ännu en komplett Excel-motor.
