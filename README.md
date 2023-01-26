# Thesis Template

Intended for use by the Maravelias Group at Princeton University
(https://maravelias.princeton.edu/). Originally forked from
https://github.com/suchow/Dissertate.git and modified slightly.

## Getting started
1. Install LaTeX. For Mac OS X, we recommend MacTex (http://tug.org/mactex/); for Windows, MiKTeX
   (http://miktex.org/); and for Ubuntu, Tex Live (`sudo apt-get install texlive-full`)
2. Install the default fonts: EB Garamond, Lato, and Source Code Pro. The files are provided in
   `fonts/EB Garamond`, `fonts/Lato`, and `fonts/Source Code Pro`.
3. I've modified the original template for use with Visual Studio Code and the LaTeX-Workshop
   extension
4. Other VS-Code extensions that I use are Rewrap (to automatically wrap lines to keep .tex files
   readable) and Spell Right (for spell checking)

## The directory structure and important files

`.vscode/`
- contains a local setting file for VS-Code that does a few things:
    - Hides LaTeX auxiliary files in the file explorer
    - Sets a "recipe" for compiling `dissertation.tex` by providing the path to the makefile
      located in `scripts/`

`chapters/`
- contains files for the individual chapters of your thesis **modify these files with the content
  of your thesis** 
- you can get rid of the quotes at the top left of the page 
- follow the template for inserting figures in the chapters
- actual figure files should be in the `figures/` directory

`endmatter/`
- some credits to the template authors and an image
- you can remove this if you want

`figures/`
- a directory to hold the figures for the entire document

`fonts/` 
- holds the font files for the template
- see FAQ for how to change the font

`frontmatter/`
- holds files for the title, abstract, dedication, etc.
- modify the `personalize.tex` file with your information and it will populate through the rest of
  the document
- if certain things are not showing up and you want them to, you may need to modify the
  `Dissertate.cls` file

`scripts/`
- `build.bat` is the makefile that compiles the LaTeX code into a PDF
- If you are on a unix machine, use the `build` shell script file

`Dissertate.cls`
- the main style file that sets the theme
- see the FAQ for how to modify most things like font, margins, reference style, etc.

`dissertation.tex`
- the main file that compiles all of the frontmatter, chapters, references, etc.
- you shouldn't have to modify anything here
- the `\frontmatter` and `\backmatter` shortcut commands are defined in the `Dissertate.cls` file


`references.bib`
- put all your references here, you can either copy and paste from the reference manager or have
  your reference manager keep the .bib file synced

## FAQ

### How do I make the text justified instead of ragged right?
Remove or comment out the line `\RaggedRight` from the .cls file.

### How do I change the margins
go to the % Text layout. portion of the `.cls` file

### How do I change the font
Line 87 in the `.cls` file and change the instances of EB Garamond to Arial for example
`\setromanfont[Numbers=OldStyle, Ligatures={Common, TeX},Scale=1.0]{EB Garamond}` 

### How do I change the references style
Line 123 change the options for natbib to reflect your preferences for in-text citations. Line 294
in the backmatter definition defines the reference list style and can be changed.