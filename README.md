# vutil
Personal utility package for LaTeX PDF documents

## Usage
### Setup
- Download `vutil.sty` into your LaTeX TDS as appropriate for your installed distribution.
- This package uses `minted` for syntax highlighting and formatting of code blocks. Ensure the Python package `Pygments` is installed.
- Include the package in a `.tex` file with `\usepackage{vutil}`.

### Code Environments
Any environment listed below may be used by wrapping raw code text with `\begin` followed by the environment signature above the text, and `\end` with the environment name below. Example:
```latex
\begin{snippet}[py]
def foo(n: int) -> int:
    return n ** 2 + 5 * n + 2
\end{snippet}
```
- `{snippet}[<language>]`: a code block with no title/label. Generally used for short snippets of code (hence the name).
- `{code}[<language>]{<ref>}`: a code block with a title/label.

### Commands
#### Code Commands
- `\codet[<language>]{<text>}`: in-line code text with optional syntax highlighting.
- `\codefile[<language>]{<path>}{<caption>}{<ref>}[<first_line>][<last_line>]`: a code block directly from a file. The optional `<first_line>` and `<last_line>` arguments may be used to only include a particular section of the file.

#### Image Commands
- `\lfig{<path>}{<width>}{<caption>}{<ref>}`: a figure with a caption/label.
- `\fig{<path>}{<width>}`: an uncaptioned figure.

#### Formatting Commands
- `\vtitle{<text>}`: simple centered title in Large text.
- `\hdr{<left>}{<right>}`: creates a header on the current page with supplied text.
- `\mhdr{<left>}{<right>}`: creates a header on every page with supplied text.
- `\ans`: sets text color to green.

#### Math Commands
- `\p`: dynamically-sized parentheses.
- `\b`: dynamically-sized square brackets.
- `\c`: dynamically-sized curly braces.
- `\abs`: absolute value.
- `\norm`: vector norm.
- `\f{<numerator>}{<denominator>}`: fraction shortcut.
- `\Im`, `\Re`: imaginary/real components in math Roman.
