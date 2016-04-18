IITM Thesis Template (LyX)
==========================

An exact LyX port of the standard IIT Madras BTech/MTech/MS/PhD Thesis
format.

## Prerequisites ##

The following packages need to be installed first:

	lyx
	texlive
	texlive-latexextra
	texlive-publishers
	texlive-science

## Installation ##

The template should work on Windows as well as Linux.

#### For Linux: ####

- Download the zip file. Extract it somewhere. `cd` to the folder 
  where you extracted it.
  
- Copy the `iitmdiss` directory to the latex template directory. 
  Note that on some distributions, path may be different.
  
	- For Archlinux:
	`sudo cp -r iitmdiss /usr/share/texmf-dist/tex/latex/iitmdiss/`.
  	
	- For Ubuntu:
  	`sudo cp -r iitmdiss/ /usr/share/texlive/texmf-dist/tex/latex/iitmdiss`
  
- Run `texhash` to refresh file name database.

  `sudo texhash`

- Open LyX. Click on Tools/Reconfigure. Restart LyX when done.

##### That's it! #####
The template `thesis.lyx` should now open and compile properly. 

You may get an error saying a class is missing, but ignore it since 
the PDF is created just fine. Test it by opening `thesis.lyx` and 
pressing `Ctrl+R`.


## Usage Instructions ##

- First thing you should do is, open `Document>Settings>LaTeX Preamble`.
  Set the Thesis title, Author, Date and your Department name there.

- Set your degree in `Documents>Settings>Document class>Custom`. Values
  can be:
	- BTech
	- MTech
	- MS
	- PhD 
	
- If it's a synopsis, add `synopsis` to the end. Example: `MTech, synopsis` or simply `MTech`.

- Don't remove any of the grey chunks of text you see in the file.
  Just edit the text part.

- Figures can be inserted normally through `Insert>Float>Figure` and
  `Insert>Graphics`. Same with tables.

- This document supports all image formats (jpeg, png, eps, pdf etc).
  Set the image scaling via right-click>Settings on the image.

- References at the end of the document can be set by editing the file
  `refs.bib` found in the same folder.

## Exporting the PDF ##

Do `File>Export>PDF (pdflatex)`. `thesis.pdf` will be created in the
same folder.

Good luck! :)
