# ICPC Programming Contest's Problems LaTeX Template

A professional LaTeX template for programming contest problem sets, designed for ICPC-style competitions with multi-problem booklets.

## Features

- **Professional Layout**: Clean header with logo placement and color-coded sections  
- **Multi-problem Support**: Easy organization of multiple contest problems  
- **Custom Header**: Includes space for contest series name and title  
- **Logo Integration**: Pre-configured slots for multiple organizational logos  
- **Page Numbering**: Automatic problem-specific page numbering (Page X of Y)  
- **Sample I/O Tables**: Pre-formatted tables for input/output examples  
- **Responsive Design**: Adjusts to different problem lengths and page counts  

## File Structure
```plaintext
project/
├── template.tex            # Main template file
├── cover-page.tex          # Cover page (optional)
├── problems/
│   ├── A.tex               # Problem A content
│   └── B.tex               # Problem B content
└── logo/                   # Directory for logo files
    ├── icpc-logo.*         # ICPC foundation logo
    ├── university-logo.*   # University logo
    ├── scientific-logo.*   # Scientific sponsor logo
    └── cultural-logo.*     # Cultural sponsor logo
```

## Required Packages

Make sure these LaTeX packages are installed:

- `geometry`
- `graphicx`
- `fancyhdr`
- `amsmath`, `amssymb`
- `parskip`
- `array`
- `xcolor` (with `table` option)
- `hyperref`
- `colortbl`

## Customization

### Contest Information

Edit these lines in `template.tex`:

```latex
\newcommand{\ContestSeriesName}{Programming Contest League}
\newcommand{\ContestTitle}{Sample University Programming League 2025}
```
### Adding Problems
Use the problem environment:

```latex
\begin{problem}{A}{Problem Name}{2}  % {Label}{Name}{Total Pages}
% Problem content here
\end{problem}
```
You can separate the problem text file from the template.tex and input it to the template.tex

> ⚠️ **Important:** You must manually specify the total number of pages as the third parameter in the problem instruction. While page numbering is dynamic, the total page count needs to be initialized by the user.

### Sample Input/Output
Use the provided command:

```latex
\sampleio{Input content}{Output content}
```
### Logos
Place your logo files in the logo/ directory with these exact names:

- `icpc-logo (any image format)`
- `university-logo`
- `scientific-logo`
- `cultural-logo`

## Compilation
Compile with standard LaTeX engines:

```bash
pdflatex template.tex
```

## Page Styles

- **First Page**: Cover page with header only (optional)  
- **Problem Pages**: Header with contest info + footer with problem-specific page numbers  

## Color Scheme

- **Header Blue**: RGB(0, 90, 170)  
- **Header Gray**: 90% gray  

Customizable via `\definecolor` commands.

## Notes

- Adjust `geometry` parameters for different margin requirements  
- Modify `\setlength` commands for spacing adjustments  
- The template automatically handles problem page numbering  
- Remove first page by commenting `\input{first-page.tex}` if not needed  


## License

Feel free to use, modify, and distribute this template for any programming contest or academic purpose.  
If you spot an issue or have an improvement, please open an issue or send a pull request! 🙌 

