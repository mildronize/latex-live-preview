# Latex Live Preview
Latex Live Preview with watchdog

> Here is a first beta. It may be some bug.

## Feature
- Live Preview, when you save `.tex` or `.bib`
- Support only `evince` (pdf viewer).
- Show only `Error` and `Warning` message, for easily to debug. [Source
  is adapted from Here](http://tex.stackexchange.com/questions/27878/pdflatex-bash-script-to-supress-all-output-except-error-messages)
- Automatic convert to pdf & clean junk files

## Prerequisite

```bash
$ sudo pip3 install watchdog
```

## Install
1. Clone this project.

    ```bash
    git clone https://github.com/mildronize/latex-live-preview.git /tmp/latex-live-preview
    ```

1. copy `bin/watchdog_latex` and `bin/.merge` into your latex project:

    ```bash
    $ cp /tmp/latex-live-preview/bin/{watchdog_latex, .merge} /path/to/your/project
    ```

## Usage

- Run `./watchdog_latex [LATEX FILE NAME w/o extension]`
- Save `.tex` or `.bib` when file is changed, the program will compile
  latex to pdf
- If `.pdf` is exist, run `evince [LATE FILE NAME].pdf&` into background
- Enjoy! your writing with latex when you save, the pdf viewer will be
  reload automatically

## Example usage

If I have `report.tex` , `ref.bib`, and `report.tex` import bib from
`ref.bib`.

- `./watchdog_latex report`
- Open pdf `evince report.pdf&`
