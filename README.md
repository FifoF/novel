*** LuaLaTeX Document Class: novel

IMPORTANT:
**********
This is now in version 1.81, uploaded to CTAN on March 13, 2023.
Earlier version 1.80, from February 2023, had a bug affecting image floats.
Although it is fixed in 1.81, TeXlive 2022 "froze" before the fix. So if
your system has TeXlive 2022, you may be unable to automatically install
`novel` version 1.81, at least for awhile.

The fix is easy. In your documents, just prior to `\begin{document}`, add this
line of code:
```
\makeatletter\def\@TMratio{1}\makeatother
```
That fixes the problem of 1.80. And, it will not hurt if you have 1.81.

Alternatively, you can permanently fix the code, without the need to
add the above line to any document. This assumes you have read/write
permission to `/tex/lualatex/novel` directory in your `texmf-dist` tree.
Edit the file `novel-Images.sty`. Find the line containing `TMratio`.
Delete the characters `[scale=\@TMratio]` so that the edited line is:
```
\gdef\@mygraphic{\novel@sub@inclgr{#3}}%
```
Do not forget the ending percent, without space before it.
**********



The 'novel' document class was added to TeXlive in early 2018. By the end
of that year, it appeared that there would be no further need for updates.
So I, its original author, removed its GitHub page (obsolete user name).

But during 2020-2022 it became clear that some tweaks need to be applied.
Version 1.80, uploaded to CTAN in early 2023, does that.

I have re-established this GitHub repository, with a new user name, in case users detect the
need for further tweaks. I may tweak it myself (particularly the documentation)
but do not expect any major changes. Use only the CTAN code for documents.

There will be no added features. Please use the 'issues' only if geniune bugs
are discovered.

Sometime in March 2023, I expect to upload a newer document class, 'novelette'.
This will be much simpler (and more accurate) than 'novel'.

Remember that 'novel' is for writing popular fiction to paper print books.
It is not just another way to format your academic papers, and has no support
for Ebooks.

GitHub user Daniel_J https://github.com/daniel-j has a fork of the older
repository, with some changes. Have a look.

