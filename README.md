# `trac`-compatible Gantt-chart template

A template to create simple gantt charts in trac using the trac-compatible subset of plain html.

Note that, while the code looks very straightforward, trac itself is very unforgiving about the subset of html it 
supports, and finding the exact subset and format that produces the expected results was not a trivial matter; hence 
this template, in the hope that it saves someone else from wasting time trying to produce trac-compatible html.

Specifically, note that css is hardcoded inside the html tags for a reason, since trac tends to break down if proper css 
style headers are attempted.

----

The enclosed template file defines an 'empty' template section, and a couple of 'prefilled' examples showing how it 
works and looks. It is intended to be edited by hand, and copy-pasted directly into a trac wiki-editor window.

If I have spare time in my hands in the near future, I may write a python script generating a template for appropriate 
dates; but in any case, it should be straightforward and painless enough to do this by hand anyway.

E.g. filling in the appropriate progress bar should be a simple case of performing a find-and-replace operation on 
"`______`" in your favourite text-editor, and replacing with an appropriate 6-digit hexadecimal colour code as 
appropriate.

Copying the resulting html script directly into a trac wiki-editor should then display a nice table with progress bars 
handled by css.

----

If you happen to open this file normally in a browser by itelf, you will note the presence of ugly `{{{#!html` and `}}}` 
trac preprocessor directives surrounding the html code. Do not remove these, they are intentional; when the code is 
copy-pasted in a trac wiki-editor, these preprocessor directives instruct trac to interpret the enclosed code as html, 
as opposed to trac-wiki syntax. They will not be visible in the resulting trac wiki page.
