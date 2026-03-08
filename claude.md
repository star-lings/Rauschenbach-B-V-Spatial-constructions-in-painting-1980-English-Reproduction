> **Task:** Translate and typeset the scanned Russian-language PDF `"Rauschenbach, B. (1980) Spatial Composition in Painting (cyrillic).pdf"` into a new English-language LaTeX document.
> 
> **Goal:** A compilable LaTeX project that faithfully represents the source book's structure and content in English, with source pagination preserved as reference markers.
> 
> ---
> 
> **Phase 1 — OCR & Verification (pause for review before proceeding)**
> 
> 1. OCR the PDF using the best available tool for Cyrillic text (e.g. `tesseract` with `rus` language data, or `ocrmypdf`). Save the raw output.
> 2. Perform a brief quality check: sample several pages from different parts of the book and display them. Flag any systematic OCR errors (e.g. character confusion, broken hyphenation, page-header noise). **Pause here and report findings before proceeding.**
> 
> ---
> 
> **Phase 2 — Structure identification**
> 
> 3. Identify the book's structure: front matter, chapters/sections, bibliography, index (if present), and their source page ranges. Report this outline.
> 
> ---
> 
> **Phase 3 — LaTeX project setup**
> 
> 4. Create a `main.tex` with appropriate preamble (use `babel` or `polyglossia` for any retained Greek; `fontenc`/`inputenc` or LuaLaTeX/XeLaTeX as appropriate). Do not use `\tableofcontents` — the TOC will be typeset manually to reflect **source** page numbers.
> 5. Organize the project as `main.tex` + one `\include`d `.tex` file per chapter/major section.
> 
> ---
> 
> **Phase 4 — Translation & typesetting conventions**
> 
> Translate each section to English directly into the target `.tex` file as you typeset it. No intermediate translation files are needed. 
> Apply the following typesetting conventions:
> 
> - **Source page breaks:** mark with `\hrulefill` followed by the source page number in a small centered label (e.g. `{\small\centering [p.\,47]\par}`).
> - **Figures** (inline and full-page): replace with a centered block giving the source figure number and caption text. No image files needed.
> - **Tables:** replace with a centered block giving the source table number and a brief description of table contents.
> - **Inline Greek:** preserve as-is, typeset in Greek script.
> - **Inline math:** typeset as LaTeX inline math.
> - **Block/display equations:** replace with a centered block stating the source equation number and source page number (redundantly), similar to figures.
> - **Footnotes:** capture the source footnote marker and corresponding note text; render using `\footnote{}` at the appropriate location.
> - **Manual TOC:** typeset a table of contents reflecting the source page numbers for each chapter/section.
> 
> ---
> 
> **Phase 5 — First deliverable**
> 
> Complete front matter and **Chapter 1 only**, then pause. Present the `.tex` output for review before continuing.

---