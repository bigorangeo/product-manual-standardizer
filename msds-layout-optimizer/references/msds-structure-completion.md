# MSDS Structure Completion

Use this reference when the input MSDS/SDS is structurally incomplete, poorly ordered, missing common sections, or written as loose notes rather than a complete MSDS document.

## Standard 16-Section Framework

Use this order unless the user provides a different required standard:

1. 产品与厂商资料 / Product and Company Identification
2. 成分辨识资料 / Composition / Information on Ingredients
3. 危害辨识资料 / Hazards Identification
4. 急救措施 / First-Aid Measures
5. 灭火措施 / Fire-Fighting Measures
6. 意外泄漏处理方法 / Accidental Release Measures
7. 操作与储存方法 / Handling and Storage
8. 接触控制/个体防护 / Exposure Controls / Personal Protection
9. 物理及化学性质 / Physical and Chemical Properties
10. 稳定性及反应活性 / Stability and Reactivity
11. 毒性资料 / Toxicological Information
12. 生态资料 / Ecological Information
13. 废弃处置方法 / Disposal Considerations
14. 储存、运输资料 / Storage and Transport Information
15. 法规资料 / Regulatory Information
16. 其他资料 / Other Information

## Completion Rules

- Add any missing section heading from the 16-section framework.
- Move existing content into the best matching section when the source order is messy.
- Preserve all provided values exactly: product names, models, company data, formulas, CAS numbers, percentages, LD50/LC50 values, hazard statements, storage requirements, dates, and version numbers.
- Do not invent missing safety, chemical, toxicity, ecological, regulatory, or transport data.
- For missing fields, use `未提供 / Not provided` when the source simply lacks the data.
- Use `待确认 / To be confirmed` when a value is implied but not reliable enough to state.
- Use `不适用 / Not applicable` only when the source clearly says the item does not apply.

## Minimum Useful Fields

When rebuilding a sparse document, include these fields where possible:

- Product/company: product name, model, recommended use, manufacturer, address, emergency contact.
- Composition: ingredient name, content, molecular formula if provided, CAS No.
- Hazards: health hazards, physical/chemical hazards, environmental hazards, GHS or label elements if provided.
- First aid: skin, eye, inhalation, ingestion, medical advice.
- Fire fighting: combustion products, extinguishing media, special hazards, firefighter protection.
- Accidental release: personal precautions, environmental precautions, cleanup method.
- Handling/storage: handling precautions, storage precautions.
- Exposure/PPE: engineering controls, respiratory protection, eye protection, hand protection, skin/body protection.
- Physical/chemical: appearance, odor, pH, boiling point, flash point, density, solubility, viscosity if provided.
- Stability/reactivity: stability, conditions to avoid, incompatible materials, hazardous decomposition products.
- Toxicology: acute toxicity, chronic toxicity, irritation, sensitization, carcinogenicity if provided.
- Ecology: ecotoxicity, biodegradability, persistence, bioaccumulation if provided.
- Disposal: waste classification and disposal method.
- Transport: dangerous goods number, UN number, packing group, transport precautions.
- Regulatory: applicable local laws and regulatory notes.
- Other: prepared/revised by, disclaimer, revision date.

## Verification

- The final document has all 16 section headings in order.
- Existing content is not lost during reorganization.
- Missing information is explicitly marked without making unsupported claims.
- Added placeholder text is bilingual when the output is bilingual.
