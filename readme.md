# LaTeX code to produce PhD thesis in the Utrecht University format (17x24cm) using VS Code

## Why running LaTeX locally
Latex needs to be installed locally, as online resources just like Overleaf cannot compile the full thesis (a thesis with ~ 300 pages takes about 2 min to compile (depending your machine of course), while Overleaf (with the University account) crashes after ~ 1 min).

## Requirements
* VS Code e.g. via the Software Center
* LaTeX; use TeX Live and install as described in [Requirements](https://github.com/James-Yu/LaTeX-Workshop/wiki/Install#requirements).
* Optional: Git; install as described in [Getting Started with Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git). With this you can keep track of the changes over time and easily revert back if something is broken.

## VS Code Installation of LaTeX and other helpful addons
Open the folder containing the LaTeX code in VScode as follows:
* File --> Open Folder --> Choose the correct folder.
* When opening the folder for the first time, VScode will give you recommendations what to install via a pop-up window in the lowe right corner. If this is not the case, you can find the needed packages in [.vscode/extensions.json](.vscode/extensions.json).

## Languages
In order to write in a specific language, a language needs to be loaded (see [main line 3](main.tex)). This code includes german, french, dutch, english language packages, with english being the primary language. Whenever you switch the a language other than english, e.g. for the Dutch Summary this needs to be switched, otherwise the text is not properly compiled (for an example see [Chapter 6 line 62-74](Chapter.6\content.tex)). 

## Overview of the project structure
The structure of the whole project is defined in the [main](main.tex). It contains information about used packages, styles, and what text to compile. If you do not want to compile the whole project, you can comment out Chapters by adding `%` at the beginning of the line. E.g. if you do not want to compile Chapter 2 do the following:
```latex
\include{Chapter.1/content}
%\include{Chapter.2/content}
\include{Chapter.3/content}
```  
Each Thesis chapter has its own folder containing the text (.tex), figures (folder) and references (.bib). The bib file format is needed in order to properly cite your references in LaTeX. Check your Citation software (e.g. Endnote or Mendeley) how to generate bib files. In the provided template, each Chapter has its own bib file and bibliography.

Additionally:
* The Preamble as requested from the UU, including the Titlepage (that needs to be personalized) is found in [Title_Page](Title_Page\content.tex).
* Chapter covers, meaning the pdf's (having the correct size measurements) which will be placed on the left page of a new chapter can be found in [Chapter_covers](Chapter_covers).
* More style settings are defined in [definitions](Style_settings/definitions.tex). Likewise, you find information about the Author and Supervisor in the file, which also needs to be adjusted accordingly. 
* The Bibliography style (meaning how references are cited and how the reference list is build) can be found [here](Style_settings\bibstyle_pnas.bst).



