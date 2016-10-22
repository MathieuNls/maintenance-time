# maintenance-time

## Collaborate

Edit the bianca.md file using whichever text editor you want (Vim, Sublime, Word). 
You can even edit it online, directly on github: https://github.com/MathieuNls/maintenance-time/edit/master/nier.md

The only thing that matters is to save it in text format.

## Build the pdf

The pdf generation is based on [Pandoc](http://pandoc.org/). Pandoc transforms the markdown to latex and then, to pdf. 
Here's the command, assuming pandoc is installed on your system and that you are on the right directory :

```bash
pandoc -s -S --latex-engine=xelatex --filter pandoc-citeproc --number-sections --listings --csl="config/ieee.csl" --template="config/default.latex" -o nier.md.pdf nier.md
```