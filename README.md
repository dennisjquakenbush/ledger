# Ledger

A personal **envelope-budgeting** app, built from Henry's spreadsheet. Every paycheck is
automatically split across your *funds* by percentage; spending draws down a fund's balance;
funds with a target double as savings goals. 100% free, no login, works offline — your data
is stored privately on your own device.

## Your funds (defaults, fully editable)

| Fund | Allocation | Goal target |
|------|-----------:|------------:|
| Tithe | 10% | — |
| Emergency | 18% | $750 |
| Investments | 30% | — |
| Car Fund | 15% | $1,000 |
| Spending | 14% | — |
| Gifts | 5% | — |
| Getting Married | 8% | $7,500 |

Allocations total 100%. The **Funds** tab shows a badge if they ever drift off 100%.

## How it works
- **+ → Income** — enter a paycheck; it splits across every fund by its % (you see the split live before saving).
- **+ → Spending** — pick the fund it comes out of; that fund's balance goes down.
- **Overview** — total balance, income vs. spending (all-time / month / week), and every fund's running balance. A fund turns clay-red if you overspend it.
- **Goals** — any fund with a target shows progress toward it.
- **Funds** — edit names, allocation %, icon, color, and goal targets; add new funds.
- **More** — backup / restore, reset funds to defaults, erase all.

## Run it

Plain web app, no build step.

**On your computer:** open `index.html`, or serve the folder:
```
cd budget-app
python3 -m http.server 4173      # then open http://localhost:4173
```

## Get it on your phone (free, no accounts)
Host the folder somewhere with a URL — easiest free options:
1. **GitHub Pages** — push this folder to a repo, enable Pages → permanent `https://…` link.
2. **Netlify Drop / Cloudflare Pages** — drag the folder onto their uploader → instant link.

Then on the phone: open the link → **Share → Add to Home Screen**. It launches full-screen and works offline.
Move your data over with **More → Download backup** on one device and **Restore from backup** on the other.

## Files
- `index.html` — the entire app (HTML, CSS, JS, line-icon set)
- `manifest.webmanifest` — makes it installable
- `sw.js` — offline service worker (bump `CACHE` when you change the app)
- `icon-*.png` — app icons
