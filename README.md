# Tickr

**Your CSV, as a checklist.**

🔗 **[gettickr.vercel.app](https://gettickr.vercel.app)**

## Why this exists

I had a CSV I wanted to work through, and I didn't want to import it into a todo app or wrestle with checkboxes in a spreadsheet. So I built Tickr: open a CSV, check items off, and your progress saves straight back to the file. Small tool, one job.

## How it works

1. Go to [gettickr.vercel.app](https://gettickr.vercel.app) in **Chrome** or **Edge**.
2. Click **Open a CSV file** (or drag a file onto the page) and allow write access.
3. Choose what to show:
   - **Main text**: the column used as the todo title
   - **Link** (optional): makes the title a clickable link
   - **Extra columns**: shown as small chips next to each item
4. Tick items off. Each tick is written back to the same file.

A `Completed` column is added to your CSV the first time you open it: `1` means done, `0` means not done. If the column already exists, it is reused. Your other columns, delimiter and quoting are left unchanged.

## Features

- Works with any CSV (comma, tab or semicolon separated). No fixed column names.
- Search, filter by a column's value, and sort by any column (numbers sort numerically).
- All / To do / Done views and a progress bar.
- Light and dark theme, with your choice remembered.
- Remembers your column choices per file layout, and **Resume last file** reopens the previous file in one click.

## Browser support

| Browser | Auto-save to file |
| --- | --- |
| Chrome, Edge, other Chromium | Yes |
| Firefox, Safari | No. Use **Download CSV** after ticking items |

Saving to a local file relies on the [File System Access API](https://developer.mozilla.org/docs/Web/API/File_System_API), which only Chromium browsers support.

## Privacy

No server, no tracking, no uploads. Your file is read and saved by your browser only. The only things stored in your browser are your theme, your column choices, a backup copy of the last file, and a handle to the last opened file (used by **Resume last file**).

## Run it yourself

Tickr is a single static file, `index.html`. Open it directly in Chrome or Edge, or deploy it to any static host (Vercel, GitHub Pages, Netlify, Cloudflare Pages). There's no build step and no dependencies.
