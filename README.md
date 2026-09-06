# testing

Staging repo for the next version of [Building Designer](https://github.com/City-of-Stonks/building-designer) — kept separate on purpose while it's in progress, not a branch of the real repo. Once this is settled it gets folded into `building-designer`'s `main`.

What's new here versus the current live version:
- **Import** — load a previously exported `.json` back into the editor (round-trips width/height/band/metadata, and drops any role ids it doesn't recognize instead of failing, so older/newer exports still load).
- **Toolbar-first layout** — Import/Export moved into a top app bar instead of buried in a form panel.
- **Tooltips instead of block text** — shortcuts, the repeating-floors explanation, the resize note, and the local-only export disclaimer are now `?` tooltips (click or hover) instead of permanent paragraphs, so the actual editor gets more of the screen.

No build step — open `index.html` directly, or use the GitHub Pages link once it's live.
