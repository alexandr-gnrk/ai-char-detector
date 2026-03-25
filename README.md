# AI Character Detector

A browser-based tool to detect AI-generated text by scanning for Unicode characters commonly produced by LLMs — em dashes, smart quotes, guillemets, ellipsis, and invisible glyphs.

**[Try it live →](https://alexandr-gnrk.github.io/ai-char-detector/)**

## How it works

Large language models tend to reproduce typographic Unicode characters from their training data — em dashes (`—`), curly quotes (`" "`), guillemets (`« »`), horizontal ellipsis (`…`), and various invisible zero-width characters. This tool scans pasted text for those characters, highlights them by type, and lets you replace them all with plain ASCII equivalents in one click.

## Features

- Detects 20 Unicode characters across 6 categories
- Color-coded highlights in the scanned text
- Verdict with signal level (none / low / medium / high)
- One-click fix — replaces all flagged chars with keyboard equivalents
- Copy fixed text to clipboard
- 100% local — no text is ever sent anywhere

## Detected characters

| Category | Characters |
|---|---|
| Em dash | `—` U+2014 |
| En dash | `–` U+2013 |
| Smart quotes | `" " ' '` U+201C/D, U+2018/9 |
| Guillemets | `« » ‹ ›` U+00AB/BB, U+2039/3A |
| Ellipsis | `…` U+2026 |
| Non-breaking space | U+00A0 |
| Invisible chars | U+200B, U+200C, U+200D, U+2060, U+FEFF |
| Figure/horizontal dash | `‒ ―` U+2012, U+2015 |

## Limitations

This is a heuristic, not a classifier. A human writer using a Mac or a word processor will also produce these characters. Conversely, AI text with no special characters won't be flagged. Use results as one signal among many.

## Built by

[alexandr-gnrk](https://github.com/alexandr-gnrk) & Claude
