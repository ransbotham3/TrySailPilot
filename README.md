# TrySail: Making Python easier for first time coders.

The **TrySail** project is a code editor, targeting Python learners with a reduced/simple set of features.

The application...

- [x] Requires no installation of Python but runs Python (currently 3.11) code.
- [x] Requires no installation of external packages.
- [x] Runs on Windows and Mac.
- [x] Avoids Terminal or Command Prompt.

# Release

Version v.0.1.33 is the latest.

## Links

Mac: https://github.com/ransbotham3/TrySailPilot/releases/download/v0.1.33/TrySail.dmg

Windows: https://github.com/ransbotham3/TrySailPilot/releases/download/v0.1.33/TrySail.exe 

## Mac instructions

1. Download and open the dmg file.
2. Drag the TrySail icon to the Application folder.
3. Double click on the TrySail application to run.

## Windows instructions

1. Download the executable file.
2. Double click on the TrySail application to run.

# Quick overview

## Interface

The top  has a code editor showing output inline between the lines of code when executed.

The bottom left side shows the current memory; the right shows help.

## Basics

Users can edit Python and Markdown.

### Python

Select "run code" to run the line of code at the current position; the output display the result of the Python.

If code execution changes the memory state, the changed memory values appear below the code in the editor window.

### Markdown

Individual lines are either markdown or code. By default, new lines are code. 

To switch a line between code and markdown, use the "Line Type" option on the Edit menu. Markdown lines show with an alternative, darker background.

Markdown changes show immediately below the markdown. To edit the raw markdown code, select "Markdown Edit" from the menu while you have the markdown line selected.

# Features so far

## Things the app will do:

The app will...

###  Read files

The app will open "ipynb" Jupyter notebook files, "py" raw Python files (including py files with Jupytext markdown encoding), and "md" markdown file. For Jupyter notebooks, it renders any existing output in the notebook.

###  Edit files

You can edit code just like a plain, uncomplicated text editor. All the usual text editing key navigation works; the app support typical editing functions like find/replace, save/save as, zoom.

The app will highlight the syntax as you type.

The app supports normal (light) mode and dark mode with multiple color themes. You can change color themes under "Preferences".

###  Demo files

The app embeds some demo files, for example...

- A Jupyter notebook with basic content.

- A Python file.

You can access the demo files from the list on the "Files" tab.

### Favorite Files

For files that you use frequently, you pin them to a list on the "Files" tab.

### Recent Files

The application will also list recent files on the "Files" tab. (You can remove files from the recent list.)

###  Automatic "cells"

When you select run with code highlighted, the app will execute the code you have highlighted. If you don't have anything highlighted, it will execute the current line.

Unlike Jupyter and other tools, users do not have to work with cells. The editor figures out "cells" so that users can work with what they know about word processors / text editors without having to learn about cells (inserting, splitting, merging, etc.) or worry about splitting cells to see the output. (There is no need for"get_ipython().ast_node_interactivity = 'all'" to see all the output.)

When necessary, the app expands the selected or current line to include other lines when executing.

Markdown: If the selection includes markdown, execution starts after the last code line above and continues until the next code line. As a result, the app executes all continuous markdown. This blocking is important so that aspects like automatic "list numbering" make sense.

Code: Code expands to include any indented lines above and below. Consider the example:

```python
for i in range( 10 ):
   print( "Test" )
   print( i )
```
Executing any of these lines requires the app to execute the other two; it does not make sense to execute one of those lines in isolation.

Code executes in a background thread. You can stop execution with the 'Stop' button. If your code is stuck (like in a loop) and 'Stop' does not work, you can use the 'Kill' button to stop Python. Using 'Kill' leaves Python in an undetermined state because it was not able to gracefully stop Python; after using 'Kill', you likely have to restart.

###  Zoom in or out

You can zoom in or out the editor.

## Development

### External packages

TrySail includes the following packages: psutil, numpy, scipy, requests, beautiful soup, glpk, pillow, nltk, pandas, matplotlib, seaborn, plotnine, plotly, scikit-learn, statsmodels.

### Developing

After the pilot settles, we will make the source code openly available.

