# Copilot Instructions for AI Agents

## Project Overview
This repository is for a technical report in LaTeX, used in the Instrumentación y Control / Robótica course at Instituto Tecnológico de Hermosillo. The workspace is structured for collaborative editing and version control using GitHub Classroom.

## Key Structure
- All report source files are in `plantilla/`:
  - `reporte.tex`: Main LaTeX file, imports sections from `secciones/` and other subfolders.
  - `secciones/`: Contains individual section files (e.g., `introduccion.tex`, `ecuaciones.tex`, etc.).
  - `portada/portada.tex`: Custom cover page, includes team info and images.
  - `img/`: Store all images referenced in the report.
  - `fuentes.bib`: Bibliography for references.
- Top-level files:
  - `Instrucciones.md`: Assignment instructions.
  - `readme.md`: Setup and workflow guidance for students.

## Build & Workflow
- **Compilation:** Use TeXstudio or MiKTeX to compile `plantilla/reporte.tex`. Ensure all images and section files are present.
- **Images:** Place all images in `plantilla/img/` and reference them with relative paths in LaTeX (`\includegraphics{img/filename}`).
- **Bibliography:** Use BibTeX with `fuentes.bib` for references. Compile with sequence: LaTeX → BibTeX → LaTeX (twice).
- **Cover Page:** Edit `plantilla/portada/portada.tex` for team details and member photos. Photos should be placed in `img/` and referenced accordingly.

## Conventions & Patterns
- **Section Inclusion:** Each section is a separate `.tex` file in `secciones/` and included in `reporte.tex` via `\input{secciones/filename}`.
- **Team Info:** Update `portada.tex` for each team member, following the tabular format for photos and contact info.
- **File Naming:** Use lowercase, descriptive names for images and section files.
- **No custom build scripts:** Compilation is manual via TeXstudio/MiKTeX; no Makefile or CI pipeline is present.

## External Dependencies
- MiKTeX (LaTeX distribution)
- TeXstudio (LaTeX editor)
- Git/GitHub for version control

## Example: Adding a New Section
1. Create `plantilla/secciones/nueva_seccion.tex`.
2. Add content in LaTeX format.
3. Reference in `reporte.tex` with `\input{secciones/nueva_seccion}`.

## Example: Adding a Team Member
1. Place photo in `plantilla/img/`.
2. Add a new tabular entry in `portada/portada.tex` with name, email, and photo reference.

## Troubleshooting
- If images or sections do not appear, check file paths and ensure files are present in the correct folders.
- For bibliography issues, ensure `fuentes.bib` is updated and compilation sequence is followed.

---
For questions about unclear conventions or missing instructions, ask for clarification or review `readme.md` and `Instrucciones.md` for assignment-specific details.