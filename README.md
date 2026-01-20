Bruno Campera's CV in LaTeX format.


## Environment setup:

OS: Windows 11 with WSL2 Ubuntu 22.04.4 LTS
Latex environment installed on Linux side with the following command:

`sudo apt install texlive latexmk texlive-xetex texlive-fonts-extra texlive-lang-greek`

Visual Studio Code on Windows side with [LaTeX](https://marketplace.visualstudio.com/items?itemName=mathematic.vscode-latex) and [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) plugins.

The current CV packages used require `xelatex` compiler command being used instead of the usual `pdflatex`. PDF may be compiled in bash with `xelatex file.tex`.
In order for the LaTeX Workshop extension to automatically compile and update the PDF preview, the following has to be added to the VSCode settings, which sets xelatex as the compiler.
```
{
    "latex-workshop.latex.tools": [{
        "name": "latexmk",
        "command": "latexmk",
        "args": [
            "-xelatex",
            "-synctex=1",
            "-interaction=nonstopmode",
            "-file-line-error",
            "%DOC%"
        ]
    }]
}
```

The PDF will be updated automatically every time you update and save .tex files.