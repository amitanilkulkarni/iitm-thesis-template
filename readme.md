IITM Thesis Template (LyX)
==========================

An exact LyX port of the standard IIT Madras BTech/MTech/MS/PhD Thesis
format.

## Prerequisites ##

For Linux, the following packages need to be installed first:

	lyx
	texlive
	texlive-latexextra
	texlive-publishers
	texlive-science

For Windows, download and install the latest LyX bundle from this website: http://www.lyx.org/Download
The same installer will also install MiKTeX on your computer.


## Installation ##

The template should work on Windows as well as Linux. However, I recommend 
using Linux for this since it's much easier to configure there.

#### For Linux: ####

1. Download the zip file. Extract it somewhere. `cd` to the folder 
  where you extracted it.
  
2. Copy the `iitmdiss` directory to the latex template directory. 
  Note that on some distributions, path may be different.
  
	- For Archlinux:
	`sudo cp -r iitmdiss /usr/share/texmf-dist/tex/latex/iitmdiss/`.
  	
	- For Ubuntu:
  	`sudo cp -r iitmdiss/ /usr/share/texlive/texmf-dist/tex/latex/iitmdiss`

3. Copy `iitmdiss.layout` file to LyX layouts directory.
	
	`sudo cp iitmdiss.layout /usr/share/lyx/layouts/`
  
4. Run `texhash` to refresh file name database.

  `sudo texhash`

5. Open LyX. Click on `Tools > Reconfigure`. Restart LyX when done.


#### For Windows: ####

1. Download the zip file and extract its contents somewhere.

2. Now copy the directory `iitmdiss` to `%AppData%\MiKTeX\2.9\tex\latex`. You may first need to create the `latex` directory inside `%AppData%\MiKTeX\2.9\tex\` manually.

3. Now copy the file `iitmdiss.layout` inside `C:\Program Files (x86)\LyX 2.1\Resources\layouts`.

4. Now open `MiKTeX Package Manager (Admin)` from start menu. We need to install three packages, `caption`, `natbib` and `threeparttable` from there. You can search using the Name field on the top bar. Then right click and choose Install on the shown package.

(NOTE: If you get download errors, go to `Repository>Change Repository`. Choose any of the available ones. That should fix it.)

5. After this is done, open `cmd.exe` and type: `texhash`

6. Open LyX as administrator, and click on `Tools>Reconfigure`. Now restart Lyx, again as an admin.

##### That's it! #####
The template `thesis.lyx` should now open and compile properly. 

You may get an error saying a class is missing, but ignore it since 
the PDF is created just fine. Test it by opening `thesis.lyx` and 
pressing `Ctrl+R`.


## Usage Instructions ##

- First thing you should do is, open `Document > Settings > LaTeX Preamble`.
  Set the Thesis title, Author, Date and your Department name there.

- Set your degree in `Documents > Settings > Document class > Custom`. Values
  can be:
	- BTech
	- MTech
	- MS
	- PhD 
	
- If it's a synopsis, add `synopsis` to the end. 
  (Examples: `MTech, synopsis` or simply `MTech`)

- Don't remove any of the grey chunks of text you see in the file.
  Just edit the text part.

- Figures can be inserted normally through first `Insert > Float > Figure` and
  then `Insert>Graphics` inside it. Same with tables.

- This document supports all image formats (jpeg, png, eps, pdf etc).
  Set the image scaling via `Right-click > Settings` on the image.

- References at the end of the document can be set by editing the file
  `refs.bib` found in the same folder.

## Exporting the PDF ##

Do `File > Export > PDF (pdflatex)`. `thesis.pdf` will be created in the
same folder.

Good luck! :)
