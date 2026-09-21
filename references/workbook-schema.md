# Workbook schema and mapping reference

## Expected activity table

| Field | Required | Use |
|---|---:|---|
| Week | yes | Week number and weekly theme; a week header may be inherited by following rows. |
| Number | yes | Stable item identifier such as `3.5`. |
| Type | yes | Usually `Topic` or `Activity`; the title often carries the subtype. |
| Time (hrs) | yes for generated items | Numeric duration, normally `0.5`, `1`, or a multiple of 0.5. |
| Title / Topic | yes | Source title and basis for the filename. |
| Purpose | yes | Purpose statement to place in the template. |
| Suggested Topic Outline | optional | Populates the topic template's `Content:` bullet list when nonempty. |
| CLOs, readings, notes | optional | Preserve or add only when requested and a suitable template location exists. |

If there is one worksheet, use it after checking that it contains the expected table. If there are multiple worksheets or versions, ask the user to identify the authoritative sheet. Do not infer authority from names such as `New`, `Archive`, or `Example` alone.

## Activity mapping

- `Topic` → topic template
- title beginning `Quiz:` → quiz template
- title beginning `Scenario:` → scenario template
- title beginning `Guided discussion:` → guided-discussion template
- title beginning `Hands-on:`, `Hand-on:`, or `Hands-on/Reflection:` → hands-on template
- title beginning `Reflection:` or type `Reflection` → reflection template

`Activity` alone is insufficient to choose a template. Ask when its subtype is not explicit. A hands-on item may map to a reflection template only when the user confirms that mapping.

## Week and filename rules

For `3.5 | Activity | 0.5 | Quiz: Measuring AI value and performance`, create `3.5 Measuring AI value and performance.xlsx`. The internal title may remain `3.5 Quiz: Measuring AI value and performance`.

Use the workbook's week theme after light whitespace cleanup. The default folder is `<course code> Week 3 Template`. Do not infer a course code from a filename if the user supplied a different code.

## Duration and topic content

For topic templates, update the word-count guidance already present in the template:

- 60 minutes / 1 hour: approximately 2,500–4,500 words
- 30 minutes / 0.5 hours: approximately 1,500–2,500 words

Ask for guidance for other durations. If `Suggested Topic Outline` is nonempty, replace or populate the template's `Content:` bullet list with the row's outline. Preserve original template bullets when the outline is empty. Split clear multiline bullets into separate bullets and retain the user's wording.

## Referencing

Ask whether the course uses Harvard, APA, or another style before adding or adapting references. Do not assume Harvard from a previous course.

## Clarification checklist

Ask before authoring if a type has no template, multiple plausible templates, a new subtype appears, duration is blank/negative/nonnumeric/not a half-hour increment, title or purpose is blank, referencing style is unspecified where references are needed, overwrite behavior is unclear, or extra fields have no clear destination.

Do not ask about harmless spelling, capitalization, or trailing-space differences when mapping is unambiguous.
