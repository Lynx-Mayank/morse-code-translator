# Signal // Morse Code Translator

## website link - https://lynx-mayank.github.io/morse-code-translator/

A fast, single-file Morse code translator that runs entirely in the browser. Type plain text to get Morse, or paste Morse to get text, and play it back as audio.

## Features

- **Bidirectional translation:** input is auto-detected as text or Morse (`.`, `-`, `/` and spaces)
- **Live output:** updates as you type, without touching your input or cursor
- **Audio playback:** plays the Morse using the Web Audio API with standard timing (dot = 1 unit, dash = 3, letter gap = 3, word gap = 7), with a stop button
- **Copy to clipboard:** one click, with a fallback for older browsers
- **Reference guide:** collapsible chart grouped into Letters, Numbers and Special Characters
- **Extra pages:** History of Morse code and a How-to-Learn guide
- **Responsive dark UI:** works on desktop and mobile

## Usage

No build step or dependencies to install. Just open `index.html` in a browser, or host it on any static host (GitHub Pages, Netlify, Vercel, Cloudflare Pages).

```bash
# Optional: serve locally
npx serve .
# or
python -m http.server 8000
```

### Input formats

| You type | Result |
| --- | --- |
| `SOS` | `... --- ...` |
| `... --- ...` | `SOS` |
| `HELLO WORLD` | `.... . .-.. .-.. --- / .-- --- .-. .-.. -..` |

For Morse input, separate letters with a single space and words with `/` or two or more spaces. Unsupported characters show as `?`.

## Supported Characters

- Letters A-Z
- Digits 0-9
- Punctuation: `. , ? ' ! / ( ) & : ; = + - _ " $ @`

## Tech Stack

- HTML, vanilla JavaScript
- [Tailwind CSS](https://tailwindcss.com/) (CDN)
- [Lucide](https://lucide.dev/) icons
- Google Fonts: JetBrains Mono and Inter
- Web Audio API for sound

## Project Structure

```
.
├── index.html   # the whole app (markup, styles, scripts)
├── img.png      # favicon
└── README.md
```

## Notes

- Ligatures are disabled on the monospace font so sequences like `....` render as separate dots.
- Google AdSense placeholders are included but commented out. To use them, add your publisher ID and uncomment the ad blocks in `index.html`.
- Audio requires a user interaction (pressing play) before browsers allow sound.

## Customization

- **Playback speed:** change `DOT_TIME` (milliseconds per dot) in the script. Lower is faster.
- **Pitch:** change `FREQUENCY` (Hz).
- **Characters:** add entries to the `MORSE_CODE` object; they appear in the reference guide automatically.

## License

MIT
