# Adobe Blank

*Adobe Blank* is a special-purpose OpenType font that is based on the Adobe-Identity-0 ROS (*ROS* stands for /Registry, /Ordering, and /Supplement, and refers to the /CIDSystemInfo dictionary entries that define the glyph set name for CID-based character collections). The Adobe-Identity-0 ROS is a special-purpose character collection whose use is not tied to a specific language, and Adobe Blank 2 is a *special-purpose* OpenType font that is intended to render all Unicode code points using non-spacing and non-marking glyphs, thus the reason why the Adobe-Identity-0 ROS was chosen as the basis for this OpenType font.

Adobe Blank maps 1,111,998 Unicode code points to 2,048 non-spacing and non-marking glyphs (CIDs 1 through 2048). The 2,048 High and Low Surrogates (U+D800 through U+DFFF), the two noncharacters in the BMP and in each of the 16 Supplementary Planes (FFFE and FFFF), and the 32 noncharacters in the range U+FDD0 through U+FDEF are explicitly and intentionally excluded. As a fully-functional OpenType font, the following 10 'sfnt' tables are included: CFF, DSIG, OS/2, cmap, head, hhea, hmtx, maxp, name, and post.

In addition to a functional OpenType/CFF font, a TrueType (TTF) version, an EOT version, WOFF (for OpenType/CFF and TrueType) versions, a Base64-encoded version that can be embedded into a CSS file, and a CSS file that embeds the Base64-encoded version are included.

## Font installation instructions

* [OS X](http://support.apple.com/kb/HT2509)
* [Windows](http://windows.microsoft.com/en-us/windows-vista/install-or-uninstall-fonts)
* [Linux/Unix-based systems](https://github.com/adobe-fonts/source-code-pro/issues/17#issuecomment-8967116)

## Building the fonts from source

### Requirements

To build the binary font files from source, you need to have installed the [Adobe Font Development Kit for OpenType](http://www.adobe.com/devnet/opentype/afdko.html) (AFDKO). The AFDKO tools are widely used for font development today, and are part of most font editor applications.

### Building the font

In this repository, all necessary files are in place for building the OpenType/CFF fonts, and the COMMANDS.txt file provides the command lines that are used.

## Getting Involved

Send suggestions for changes to the Adobe Blank project maintainer, [Dr. Ken Lunde](mailto:lunde@adobe.com?subject=[GitHub] Adobe Blank), for consideration.
