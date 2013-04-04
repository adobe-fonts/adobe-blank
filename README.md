Adobe Blank
====

Overview
----
Adobe Blank is a special-purpose OpenType font. This open source project provides all of the source files that were used to build this OpenType font by using the AFDKO *makeotf* tool.

Getting Involved
----
Send suggestions for changes to the Adobe Blank OpenType Font project maintainer, lunde@adobe.com, for consideration.

Building
====

Pre-built font binaries
----
The font binaries are not part of the source files. They are available on [Open@Adobe](https://sourceforge.net/projects/adobe-blank.adobe/files/).


Requirements
----

For building binary font files from source, installation of the [Adobe Font Development Kit for OpenType](http://www.adobe.com/devnet/opentype/afdko.html) (AFDKO) is necessary. The AFDKO tools are widely used for font development today, and are part of most font editor applications.

Building the font
----

Key to building OTF or TTF fonts is *makeotf*, which is part of AFDKO. Information and usage instructions can be found by executing *makeotf -h*.

In this repository, all necessary files are in place for building the OpenType font. For example, build a binary OTF font for the Regular style like this, which also includes post-processes for inserting a "stub" 'DSIG' table, removing the 'VORG', 'vhea', and 'vmtx' tables, and recalculating the 'sfnt' checksum:

    % makeotf -f cidfont.ps -r -ch UnicodeAll-UTF32-H
    % sfntedit -a DSIG=DSIG.bin AdobeBlank.otf
    % sfntedit -d VORG,vhea,vmtx AdobeBlank.otf
    % sfntedit -f AdobeBlank.otf

That is all.
