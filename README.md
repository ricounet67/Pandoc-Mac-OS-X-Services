# Pandoc Mac OS X Services

Invoke [pandoc](http://johnmacfarlane.net/pandoc/) from any text editor with the opened file as input.

This is achieved using [Mac OS X services](http://arstechnica.com/apple/2011/03/howto-build-mac-os-x-services-with-automator-and-shell-scripting/).


## Go!

1. Copy the files to your `~/Library/Services` folder
2. Restart your editor, open and save a file containing some [markdown](http://johnmacfarlane.net/pandoc/README.html#pandocs-markdown)
3. Go to the `Services` menu (for example if you're using Sublime: `Sublime > Services`) and choose a service like `Pandoc PDF`.
4. After a few seconds, the PDF file will appear in the same folder as your markdown file
5. Finally, you can assign a keyboard shortcut to invoke a service in `System Preferences > Keyboard > Keyboard Shortcuts > Services (on the left)`.


## Templates

`Pandoc PDF with Template` and `Pandoc ConTeXt PDF with Template` look for a `template.tex` or `contextTemplate.tex` file respectively in the same directory as the input file.

To get a copy of the default [pandoc template](http://johnmacfarlane.net/pandoc/README.html#templates) to customize, use `pandoc -D latex > template.tex` or `pandoc -D context > contextTemplate.tex` respectively.