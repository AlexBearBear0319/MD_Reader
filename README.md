# Marginalia

<p align="center"><img src="app/icon-1024.png" width="160" alt="Marginalia app icon"></p>

A quiet, Markdown editor for macOS. It renders your document as you type: the paragraph you are editing shows its Markdown, and everything else stays formatted. There is no split preview.

## Features

- **Live preview**, block by block, with a full **Source mode** (⌘/)
- **Focus mode** (F8) dims everything except the current paragraph
- **Typewriter mode** (F9) keeps the active line centred
- Headings, tables, task lists, footnotes, and code with syntax highlighting
- **Math** with `$…$` and `$$…$$` (MathJax), **diagrams** with ```` ```mermaid ```` blocks
- Sidebar with a **file list** and a clickable **outline** of your headings
- Drag-and-drop or paste **images**
- Themes (Auto, Paper, Sepia, Night) plus your own **custom CSS**
- Open and save real `.md` files, export **HTML** and **PDF**

## Download and install

Requires macOS 13 Ventura or later. Works on Apple Silicon and Intel Macs.

1. Go to the [Releases page](https://github.com/AlexBearBear0319/MD_Reader/releases) and download **`Marginalia.zip`** from the latest release.
2. Double-click the zip in your Downloads folder to unzip it. You get **Marginalia.app**.
3. Drag **Marginalia.app** into your **Applications** folder.
4. Open it for the first time (see below).

### First launch: "Marginalia can't be opened"

Marginalia isn't signed with a paid Apple Developer certificate, so macOS blocks it the first time. Allow it once and it opens normally after that:

1. Double-click Marginalia. When macOS says it can't verify the app, click **Done** (or **Cancel**).
2. Open **System Settings → Privacy & Security**.
3. Scroll down to the message about Marginalia and click **Open Anyway**, then confirm with your password or Touch ID.

If you prefer the Terminal, this removes the download quarantine flag instead:

```bash
xattr -dr com.apple.quarantine /Applications/Marginalia.app
```

### Open Markdown files with Marginalia

Right-click any `.md` file in Finder → **Open With → Marginalia**. To make it the default, choose **Get Info** on a `.md` file, pick Marginalia under **Open with**, and click **Change All…**.

## Keyboard shortcuts

| Action | Shortcut |
| --- | --- |
| New / Open / Save | ⌘N / ⌘O / ⌘S |
| Save As | ⇧⌘S |
| Export HTML / PDF | ⇧⌘E / ⌘P |
| Heading 1–6 / paragraph | ⌘1–⌘6 / ⌘0 |
| Bold / Italic / Link / Code | ⌘B / ⌘I / ⌘K / ⌘E |
| Source mode | ⌘/ |
| Sidebar | ⇧⌘L |
| Focus / Typewriter | F8 / F9 |
| New paragraph / line break | Enter / Shift+Enter |

## Notes

- An internet connection is needed for code highlighting, math and diagrams (the libraries load from a CDN).
- Documents you haven't saved to a file are kept inside the app between launches.

## Build from source

You need the Xcode Command Line Tools (`xcode-select --install`).

```bash
./app/build.sh
```

This produces `build/Marginalia.app` (universal) and `build/Marginalia.zip`, ready to attach to a GitHub release. The icon is drawn by `app/make_icon.swift`; delete `app/icon-1024.png` and rebuild to regenerate it.

## License

See [LICENSE](LICENSE).
