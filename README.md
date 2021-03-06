# JBAstroXSL

XSL file to be used in Microsoft Word as a reference format style. The bibliography will look like what you typically see at the end of an astronomy article (e.g. in ApJ or MNRAS). References within the text are numerical.

This should work in most cases for entries downloaded from ADS as BibTeX and then exported as Word XML format, for example using BibDesk.

Installation:
Copy into "the appropriate place", which appears to change every version of Word, and then quit Word and restart it. For Office 365 on Mac, as of June 14, 2021, it needs to be in ``/Applications/Microsoft\ Word.app/Contents/Resources/Style/``, be owned by root, and have all read and user write permissions. In other words, the following should install it:
```
sudo cp JBAstro.xsl /Applications/Microsoft\ Word.app/Contents/Resources/Style/ ; sudo chmod 644 /Applications/Microsoft\ Word.app/Contents/Resources/Style/JBAstro.xsl ; sudo chown root:wheel /Applications/Microsoft\ Word.app/Contents/Resources/Style/JBAstro.xsl
```
You will need to have administrator access and enter your password. I don't know why you can't put it in a user-accessible area.

Caveats:
 - If the authors have LaTeX commands in their name for special letters, you will need to fix those up. I recommend fixing them up in the BibTeX file.
 - Currently lists all authors, even for very long author lists.
 - Punctuation around the year for single authors and multiple authors looks very slightly different (multiple authors has a comma before the year, single authors don't).

Based very heavily on the IEEE2006OfficeOnline.xsl file that comes with Word by default that specifies the IEEE style. I made some hacks to journal article entries and report entries (used for theses) -- don't expect any other type of entry to look even vaguely correct.
