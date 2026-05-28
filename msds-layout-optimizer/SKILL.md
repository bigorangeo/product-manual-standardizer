---
name: msds-layout-optimizer
description: Optimize and complete MSDS/SDS Word documents (.docx) into a clean Chinese-English bilingual Guangzhou Faith-style layout. Use when the user asks to format, polish, standardize, complete missing structure, translate-and-format, or improve material safety data sheets, safety data sheets, hazard documents, chemical documents, Chinese-only MSDS files that must become bilingual, incomplete MSDS drafts, bilingual Chinese-English MSDS files, toxicity tables, ingredient tables, or Word MSDS templates.
---

# MSDS Layout Optimizer

## Core Workflow

1. Inspect the source `.docx` structure first: sections, title/version/revision lines, numbered MSDS sections, tables, merged cells, and any overflow-prone toxicity or composition tables.
2. Check whether the MSDS structure is complete and in the expected 16-section order. If it is incomplete, actively reorganize and complete the structure using `references/msds-structure-completion.md`.
3. Decide whether the file is Chinese-only or already bilingual.
4. If the file is Chinese-only, convert it into Chinese-English bilingual MSDS content while preserving the original Chinese meaning and all provided technical data. Follow `references/bilingual-msds-translation.md`.
5. If the file is already bilingual, preserve safety content exactly unless the user explicitly asks for translation or rewriting.
6. Apply the reference layout from `references/layout-spec.md`.
7. For routine formatting after the structure and bilingual content are present, run `scripts/optimize_msds_docx.py <input.docx> <output.docx>`.
8. Open or inspect the output document and verify that table text remains visible, section order is intact, merged cells are not flattened, and the toxicity table is readable.

## Layout Rules

- Use Letter page size with top 1.8 cm, bottom 1.25 cm, left/right 2.0 cm margins unless the user asks for A4.
- Keep the document bilingual and compact: Chinese and English labels may share lines or paired rows, but do not merge unrelated safety fields.
- For incomplete MSDS inputs, add missing standard section headings and organize available content under the best matching section. Mark missing unknown data as `未提供 / Not provided` or `待确认 / To be confirmed`; do not invent safety values.
- For Chinese-only inputs, add English beside each heading, field label, and safety statement. Keep the original Chinese visible.
- Format the main title as centered, large Microsoft YaHei/Arial text.
- Format numbered section headings as bold blue bilingual headings, with visible spacing before and after.
- Use tables for structured fields. Prefer two-column label/value tables for general MSDS sections.
- Use a shaded header row for ingredient/composition tables and any dense multi-column hazard tables.
- Treat toxicity tables as high-risk layout elements: use smaller text, centered headers, adequate cell margins, and check that LD50/LC50 data does not disappear or overlap.

## Using The Script

Run:

```bash
python scripts/optimize_msds_docx.py input.docx output.docx
```

The script performs conservative formatting only. It does not translate, delete, reorder, or synthesize safety content.

For Chinese-only inputs, create or update the bilingual text first, then run the script on the bilingual `.docx`.

For structurally incomplete inputs, complete the 16-section MSDS framework before running the script.

Use manual `python-docx` edits after the script only for document-specific issues such as:

- long chemical formulas requiring narrower font or line breaks
- regulatory sections with unusually long bilingual paragraphs
- toxicity tables with merged cells that need custom widths
- user-specified company logo, header, footer, or page size changes
- adding English rows/cell text when the source document is Chinese-only
- adding missing MSDS sections and moving misplaced content into the proper section

## Assets

`assets/reference-msds-layout.docx` is the source layout sample. Use it as a visual/layout reference only; do not copy product-specific facts, formulas, dates, or company details into another MSDS unless the user provides them.

## Verification Checklist

- Title, version, 16 numbered MSDS sections, technical contact block, disclaimer, and revision date are still present when provided.
- Incomplete source files have been reorganized into the standard 16-section MSDS structure.
- Missing data is marked clearly instead of invented.
- Tables stay inside page margins.
- Ingredient tables retain CAS numbers, formulas, and percentages.
- Chinese-only source content has been converted into Chinese-English bilingual content, with original Chinese retained.
- Toxicity tables keep LD50/LC50 values readable.
- No provided safety statement or technical value is changed as a formatting side effect.
