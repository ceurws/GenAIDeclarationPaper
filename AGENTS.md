# Content policy for AI agents

This repository holds a **technical report** about the Declaration on
Generative AI in CEUR-WS papers. It is not published via CEUR-WS, but it
follows the [CEUR-WS Policy on AI-Assisting Tools](https://ceur-ws.org/GenAI/Policy.html)
(Salatino, Fornari, Zdravkovic, CC BY 4.0), whose use outside CEUR-WS is
permitted subject to attribution.

## Hard rules

0. **NEVER build the report locally.** No `scripts/tex2pdf`, no `pdflatex`,
   no `latexmk` — the PDF is built by CI on push.
1. AI assistance is limited to **spelling/grammar**, **translation of text
   dictated by the authors**, **formatting/build tooling** and the agentic
   work that is explicitly part of the method (running scripts, collecting
   data, classifying declarations for RQ4).
2. Everything outside that scope — **research questions, hypotheses,
   conclusions, arguments, prose, the abstract, the title** — is authored by
   the human authors. Text an agent rewords is generated text and does not go
   into `main.tex`.
3. Sections in `main.tex` stay **EMPTY** until the authors write them.
4. **No AI-generated visual aids.** Charts are produced deterministically by
   scripts from the data; diagrams are drawn by the authors. An agent does
   not write diagram source (PlantUML, SVG, TikZ).
5. Only **verified** bibliographic metadata belongs in `references.bib`.
   Never fabricate references, DOIs, page numbers or claims.
6. **No CEUR-WS PDFs in this repository.** CEUR-WS forbids third-party
   mirroring. The data holds volume and paper URLs, verdicts, labels and
   extracted declaration snippets of CC BY 4.0 papers with attribution only.
7. **No third-party data without a license or a written permission**, e.g.
   the annotated dataset of aftabcau/Gen_AI has no license file.
8. **No internal sources**: no board mails, no internal host names, no numbers
   from manuscripts without a DOI.
9. AI agents are **never authors** (CEUR-WS HOWTOSUBMIT FAQ 15).
10. Every agent contribution is recorded in [PROVENANCE.md](PROVENANCE.md)
    and in the issues with the provenance notation of the README; the
    **Declaration on Generative AI** is finalized by the authors from that
    record.
11. The report must be **self-contained**: every term is defined in the text,
    links only point to further material.

## Allowed agent tasks

- Maintain the CEURART scaffold, build system and `.gitignore`.
- Fix LaTeX/build errors and formatting.
- Format author-provided bibliography entries.
- Resolve and fill **verified** author ORCIDs/affiliations (from Wikidata/ORCID).
- Run the experiment scripts and record their results as described in the
  issues.
