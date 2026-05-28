# Chinese-To-Bilingual MSDS Rules

Use this reference when the input MSDS/SDS is Chinese-only and the user expects an optimized Chinese-English document.

## Translation Scope

- Translate headings, field labels, table headers, safety statements, emergency measures, storage/transport instructions, disposal text, regulatory text, and disclaimers.
- Keep the original Chinese text visible. Add English beside it in the same line/cell when short, or in the next paired row/paragraph when long.
- Do not translate chemical formulas, CAS numbers, UN numbers, product models, company names, addresses, dates, version numbers, percentages, LD50/LC50 values, exposure limits, or regulatory identifiers unless a standard English rendering is obvious.

## Bilingual Structure

- Section headings: `1. 产品与厂商资料 / Product and Company Identification`.
- Short labels: `产品名称 Product name:` or paired rows such as `产品名称：` followed by `Product name:`.
- Table headers: combine Chinese and English in the same cell when space allows, such as `成分名称 Ingredient`.
- Long safety statements: keep Chinese first, then English in the next paragraph or paired row to avoid dense unreadable cells.

## Translation Discipline

- Translate faithfully and conservatively. MSDS text is regulatory/safety content, not marketing copy.
- Prefer standard SDS terminology: `Hazards Identification`, `First-Aid Measures`, `Fire-Fighting Measures`, `Accidental Release Measures`, `Handling and Storage`, `Exposure Controls / Personal Protection`, `Physical and Chemical Properties`, `Stability and Reactivity`, `Toxicological Information`, `Ecological Information`, `Disposal Considerations`, `Transport Information`, `Regulatory Information`, `Other Information`.
- Preserve uncertainty markers such as `无`, `不适用`, `NA`, `--`, and blank values. Translate labels around them, but do not invent missing data.
- If a Chinese phrase is ambiguous or seems technically unsafe to translate confidently, keep the Chinese, provide the most literal safe English translation, and flag the item for user review.

## Verification

- Every Chinese section title and table label has an English counterpart.
- Every Chinese safety statement has an English counterpart.
- No product-specific values, formulas, CAS numbers, hazard categories, test data, or regulatory claims were added by inference.
- The bilingual expansion did not make tables overflow page margins.
