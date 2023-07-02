# Enso Font

The Enso font was specifically designed for the [Enso application](https://enso.org). It is based on the [MPlus1 font family](https://github.com/coz-m/MPLUS_FONTS), with certain modifications to enhance its suitability for both the Enso code and regular text displayed within the application. The font was designed in such a way that it provides good code readability by default and implements alternative characters that can be used to properly display written text. All these rules were implemented within a single font to allow the application to use only one font instead of different ones for different parts of the application, allowing the Enso rendering engine to work faster by caching common glyphs across these use cases. Refer to the below image to see an example usage of the font:

<img width="656" alt="image" src="https://github.com/enso-org/font/assets/1623053/9a2ca1f7-be02-4676-86ae-8ed8f7026e9f">

<br/>

## Changes to MPlus1

In order to improve code readability, the following changes have been implemented:

- [The Full Stop Glyph (`.`, U+002E)](https://www.compart.com/en/unicode/U+002E) has been adjusted with additional side spacing to improve its appearance in Enso code, such as `data.read`.
- [The Low Line Glyph (`_`, U+005F)](https://www.compart.com/en/unicode/U+005F) spacing and vertical alignment has been modified to ensure greater consistency when used to surround words.
- [The Apostrophe Glyph (`'`, U+0027)](https://www.compart.com/en/unicode/U+0027), [the Quotation Mark Glyph (`"`, U+0022)](https://www.compart.com/en/unicode/U+0022), and their left and right variants have been modified to not use italics style when using inside of a text.
- The mathematical operators (`+`, `-`, `*`, `<`, `>`) have been modified to have the same spacing and vertical alignment.
- [The Space Glyph (' ', U+0020)](https://www.compart.com/en/unicode/U+0020) has been adjusted to have the same width as mathematical operators.
- Ligatures for `<|`, `|>`, and `->` have been added.

<br/>

## Using Enso Font in regular sentences

In order to use the font in regular sentences, several new glyphs have been implemented. If you want to use this font to display regular sentences, you have to apply the following transformations to your text:

- Instead of [the One Dot Leader Glyph (`․`, U+2024)](https://www.compart.com/en/unicode/U+2024) use the [the One Dot Leader Glyph (`․`, U+2024)](https://www.compart.com/en/unicode/U+2024).
- Instead of [the Space Glyph (` `, U+0020)](https://www.compart.com/en/unicode/U+0020) use [the Four-Per-Em Space Glyph (` `, U+2005)](https://www.compart.com/en/unicode/U+2005).
- Instead of [the Hyphen Glyph (`-`, U+2010)](https://www.compart.com/en/unicode/U+2010), use [the En Dash Glyph (`–`, U+2013)](https://www.compart.com/en/unicode/U+2013).

<br/>

## Installation

To install the Enso font, please follow these steps:

1. Download the font files from the [release page](https://github.com/enso-org/font/releases).
2. Use your system's font manager to install the downloaded files.

<br/>

## Contributing

If you wish to contribute and make edits to the Enso font, you can use the [MacOS Glyphs App](https://glyphsapp.com). Simply open the `src/Enso.glyphs` file in the Glyphs App and make the desired modifications. To build the fonts, use the `File -> export` command. Currently, the `build.py` script is not supported and is kept only for future reference.
