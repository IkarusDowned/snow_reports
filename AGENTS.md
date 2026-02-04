# Snow Report Agent Guide

This repository contains public snow reports. Write reports in a consistent OGRS-aligned observation style and match the existing Myoko report format.

## Scope
- Follow the Canadian Avalanche Association OGRS (2024) principles: objective observations, clear structure, standardized test/result notation, and explicit uncertainty.
- Follow repository rules in `README.md` and mimic language/style used in existing reports under `docs/reports/myoko/`.

## File and path rules
1. Add reports under `docs/reports/<location>/`.
2. Use filename format: `<location>_<type>_report_YYYY-MM-DD.md`.
   - Example: `myoko_snowpack_report_2026-01-05.md`
3. If media is referenced, place files under `media/` and link from report.

## Report format (required)
Use this exact high-level structure and ordering:

1. YAML lines:
   - `---`
   - `---`
2. H1 title:
   - `# <LOCATION> SNOWPACK OBSERVATIONS REPORT`
3. Metadata block (bold labels, one per line):
   - Date
   - Location
   - Coordinates
   - Elevation
   - Aspect
   - Activity
   - Observers
4. Horizontal rule: `---`
5. Section sequence (H2):
   - Concerning results observed: ...
   - QUICK SUMMARY - ...
   - AVALANCHE SUMMARY - ...
   - SNOWPACK SUMMARY - ...
   - WEATHER SUMMARY - ...
   - TRAVEL CONDITIONS - ...
   - ASSESSMENT - ...
6. Final horizontal rule: `---`

Keep the section-heading pattern consistent with existing reports:
- `## <SECTION NAME> - <compact technical takeaway>`

## OGRS-aligned content rules
- Record core context clearly: date/time, location, elevation band, aspect, weather, and observer names.
- Use standardized snow and test notation where relevant (e.g., `CTE/CTM/CTH/CTN`, fracture character like `SP`, hardness `F/4F/1F/P/K`, grain/form shorthand, layer depth in cm).
- Report observations first, then interpretation.
- Distinguish measured values from estimates/inference.
- If data is missing or uncertain, state that explicitly (do not imply certainty).
- Include key stability evidence in snowpack sections:
  - total snow depth (HS)
  - critical layer depth and interface description
  - hardness progression
  - grain type/bonding notes
  - temperature profile summary
  - stability test outcomes
- Include avalanche observations (or explicit no-activity statement) and note visibility/coverage limitations.

## Style rules
- Use concise, technical, field-report language.
- Prefer concrete numbers with units (`cm`, `m`, `°C`, `km/h`).
- Keep narrative grounded in that day’s field data and direct comparisons to prior reports when available.
- Avoid speculative claims; use cautious phrasing for unconfirmed spatial extent.
- Keep formatting, capitalization, spacing, and separator lines consistent with existing repository reports.

## Quality checklist before finalizing
- Filename and location follow `README.md`.
- Section order and heading style match existing reports.
- All key metadata fields are present.
- Stability tests and layer information are internally consistent (depths, units, hardness/test codes).
- Assessment is supported by evidence presented earlier in the report.
