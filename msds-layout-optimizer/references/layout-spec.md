# MSDS Layout Reference

Derived from `FS100-115M_MSDS_2.2_translation_layout_optimized_v4_toxicity_table.docx`.

## Page

- Size: Letter, 21.59 cm x 27.94 cm.
- Margins: top 1.8 cm, bottom 1.25 cm, left 2.0 cm, right 2.0 cm.
- Default body type: 10.5 pt, Arial for Latin text and Microsoft YaHei for Chinese text.

## Paragraph System

- Main title: centered, 26 pt, Microsoft YaHei, no bold required, about 10 pt space after.
- Version line: right aligned, 9 pt, tight line spacing around 1.05. Optimized outputs use `版本Version ：2.3` unless the user specifies another version.
- Numbered section heading: matches `1.` through `16.`, bold, 18 pt, blue `#1F4E79`, about 12 pt space before and 8 pt after.
- Subsection heading, such as `急性毒性 / Acute toxicity:`: bold, 10.5 pt, about 4 pt before and 2 pt after.
- Closing company/contact and disclaimer text: compact body text, 10-10.5 pt, line spacing around 1.05.
- Revision date: right aligned, 9 pt, muted gray. If the source has no revision date, use `修订日期Revision Date：03/2026`.

## Table System

- General sections use two-column label/value tables.
- Label cells should stay narrow enough to scan but wide enough for bilingual labels.
- Body tables use compact paragraph spacing: 0 pt before/after, line spacing around 1.05.
- Cell padding should be modest: about 0.08-0.12 cm left/right and 0.04-0.06 cm top/bottom.
- Borders should be visible and light, typically gray `#BFBFBF`.
- Dense multi-column tables use 8.5-9 pt text when needed.

## Composition Table

- Typical columns: `序号 No.`, `成分名称 Ingredient`, `含量 Content`, `分子式 Molecular formula`, `CAS No.`.
- Header shading: pale blue `#D9EAF7`.
- Header text: bold and centered.
- Body cells: vertically centered; formula and CAS cells can use compact text to avoid wrapping damage.
- Values must match the current source document exactly. Translate ingredient names, but do not change the source substance name or percentage range. For example, if the source says `水` and `60-70%`, use `水 Water` and `60-70%`; do not change it to `去离子水 Deionized water` or infer a different range.
- This table must be audited row by row before delivery. Compare the output against the source for ingredient name, content, formula, and CAS No.; do not trust template values.

## Toxicity Table

- Treat as the most fragile table.
- Preserve merged cells and duplicated bilingual labels.
- Prefer 8.5-9 pt text, vertical centering, and compact margins.
- LD50/LC50 values must remain visible and not collapse into narrow columns.
- If automatic formatting still causes overflow, manually adjust column widths or insert safe line breaks inside long values.

## Content Integrity Rules

- Do not invent hazard classifications, CAS numbers, formulas, exposure limits, transport data, or regulatory statements.
- Do not normalize `None`, `NA`, `--`, or blank values unless the user asks.
- Keep company names and product identifiers from the source. Normalize optimized MSDS version to `2.3`; when no source revision date is provided, use `03/2026`.
- In section 9, `外观及性状 / Appearance and properties` should describe only the physical appearance/state. Remove product model prefixes such as `FS7230-130` from this value in both Chinese and English; keep the product model only in product identification, header material number, or other explicit model fields.
- In section 9, numeric physical/chemical property fields with concrete values should use one row: put the Chinese and English label in the left cell, and put only the concrete value in the right cell. For example, use `蒸气压 Vapor pressure:` with `< 21.07mmHg (23℃)`, and `密度 Density:` with `1.0-1.05g/cm3 (20℃)`. Do not add a separate English row or duplicate the numeric value in English.
- Section 9 must be audited value by value before delivery. Compare appearance, odor, vapor pressure, vapor density, boiling point, explosive limits, solubility, and density against the source. Do not trust template values.
