# 24/7 Flood Monitoring Report

Live page: https://oplankontrabaha.github.io/247DrainageCleaning/

## How it works

- **index.html** is the report form (moved from Apps Script Index.html V27 to GitHub Pages V28).
- **config.js** holds the Apps Script `/exec` link. All saving, PDF/DOCX generation, emails and photo storage still happen in Apps Script (Code.gs V13).
- The form talks to Apps Script through a small bridge that stands in for `google.script.run`, so the form code itself is unchanged.

## Setup

1. In Apps Script, use Code.gs V13 and deploy the web app as **Execute as: Me** and **Who has access: Anyone**.
2. Copy the Web app URL (ends in `/exec`) and paste it into `config.js`.
3. Test the backend: open `<exec link>?action=ping`. You should see `"status":"ONLINE"`.
