# Increment Ledger — GGHL

A self-contained PWA that reads `data.xlsx` (monthly gross salary with breakup)
and shows each employee's last increment, full increment history, and
previous-vs-current salary breakup.

## Files
- index.html      — the whole app (HTML + CSS + JS, uses SheetJS from CDN)
- data.xlsx       — payroll data (replace this file to update the app)
- manifest.json   — PWA manifest (install on iPhone / Windows)
- sw.js           — service worker (offline shell, always-fresh data)
- icon-*.png      — app icons

## Update the data
Just replace data.xlsx with a new export that keeps the same columns:
Personnel Number | Name of employee or applicant | Company | Payment date |
Basic-D | Allw-D | Car Allw-D | Home Allw-D | Total Salary

Commit → app refreshes automatically (data is fetched network-first with a
cache-buster on every open).

## Company names
Edit the COMPANY_NAMES map near the top of the script in index.html to show
real company names instead of codes.
