# font-for-textual

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
