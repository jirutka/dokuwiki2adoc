# convtags
convtags is a converter from DokuWiki to AsciiDoc formatted text files.


What is convtags
----------------

convtags is a converter:

DokuWiki => AsciiDoc
  
Written with portability in mind, it should work on any UNIX® like operating
system.

Target use cases
----------------

* Convert a wiki powered by DokuWiki to a static website
* Ease the translation of a wiki powered by DokuWiki

Installation
------------

Manual installation:

* Download the program convtags and the md5 hash file convtags.md5
* Check the integity of convtags using convtags.md5. This command:
md5sum -c convtags
should return:
* OK
* Ensure that convtags be executable and owned by root:
chown root:root convtags; chmod 755 convtags
* move convtags in a suitable location, preferably /usr/bin:
mv convtags /usr/bin

Dependencies
------------

* [POSIX-sh](http://pubs.opengroup.org/onlinepubs/009695399/utilities/xcu_chap02.html) compatible shell (e.g. Busybox ash, dash, ZSH, Bash, ...)
* `sed` supporting GNU extensions: `\?`, `\+`, `\|`, and `^` inside subexpressions
* Python for rewriting internal links

Usage
-----

After installation, type:
convtags
to get information on usage, settings, configuration and support.

Features and limitations
------------------------

Most syntactic DokuWiki constructs can be converted to AsciiDoc.

Known limitations in the conversion from DokuWiki to AsciiDoc:
* No syntax checking is done of the input file.
* Appending a downloadable file (code snippet) to a Code block is not
available (the link to the file is silently discarded by the converter).
* The links to a location in the same page are not converted.
* The vertical spanning (over several rows) of table cells is not provided.
* Text decorations and “text not to be parsed” marks are only converted if
opening and closing marks are on the same line.
* Windows shares and Interwiki links are not converted.
* Embedding HTML and PHP is not available.
* RSS/Atom feed integration is not available.
* Text to image conversion is not available.
* External images (in DokuWiki parlance) are not displayed.

In addition to the basic DokuWiki syntax, the graphical rendering of
admonitions (through the Note plugin) is converted.

Other plugins can be needed to properly display the documents in DokuWiki
format, be it in the genuine or converted back ones. Examples are the
Keyboard Syntax plugin, Info plugin, Tag plugin and HTML Comment plugin.

For syntax highlighting to show in AsciiDoc you need a proper utility, for
instance source-highlight.

Author
------

Didier Spaier, Paris, France

This document was last updated on 19/04/2016 




