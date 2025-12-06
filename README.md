# font-for-textual

The Linux console is most often used in server contexts. It does not have the same capabilities as the terminal emulators available in desktop environments. The console uses fonts in a special format (called PSF), and these can have either 256 or 512 glyphs. The 256 glyph fonts can have 16 colors, while the 512 glyph fonts are restricted to only 8 colors.

The Python Textual package is a Textual User Interface (TUI) library. It uses various Unicode drawing characters for scrollbars, button outlines and other controls. To look good you need these drawing characters, as well as enough letters, numbers and punctuation for the text you want to display. 

Textual also needs enough colors to distinguish the controls and add highlights, and eight colors are not enough. This means you cannot use a 512 glyph font, and none of the standard font files supplied have all the drawing characters needed in a 256bglyph font. This font is a solution that contains the drawing characters needed, and enough letters, numbers and punctuation to be useful.

# The font

The file textual.psf is a 256 glyph PSF font for use in the Linux console. 

It is a subset of Unifont.psf and carries the same license and copyright as the work it is derived from. See [Unifoundry site](https://unifoundry.com/unifont/index.html) for definitive details. As of Unifont version 13.0.04, the fonts are dual-licensed under the SIL Open Font License (OFL) version 1.1 and the GNU GPL 2+ with the GNU font embedding exception. The Unifoundry site contains a document that describes the copyright protections that protect Unifont, and by derivation, this work. 

The subset has been chosen to improve the appearence of applications that use the Python Textual TUI package, but might be useful elsewhere. It has a full set of block drawing glyphs, and single and double line box drawing glyphs. Heavy line box drawing glyphs are mapped to the corresponding double line shape. It contains enough letter forms for at least some Western European languages, but not all, and certainly not for Central European, Cyrillic, Arabic or Asian languages.

The psf file was constructed using John Zaitseff's [console-font-utils](https://www.zap.org.au/projects/console-fonts-utils/). The distributed Unifont.psf was converted to an editable .psftx file with the psf2psftx utility. The file was edited to produce the subset in textual.psftx, and converted back with psftx2psf. 

# Using textual.psf

This font is only relevant for the Linux VT console. It is no use in a GUI. To set it, use the setfont utility.

```shell
setfont textual.psf
```

This might be added to say .profile or similar start-up file.
