
# GEMS Design System — Components / Input

> **MANDATORY:** Use official GEMS General Input components from the connected Figma Design System. Preserve original component references, supported properties, styling, and interaction behavior. **CCM components are strictly prohibited.**

## 1. Purpose & Source of Truth

This guideline governs text-entry components in GEMS interfaces:

- Input Field
- Textarea Input Field
- Supporting Form components
- Input states, validation, content, and contextual usage

**Excluded:** Standalone Dropdown and Date & Time Picker. Follow their respective component guidelines.

**Core Principle:** Select components according to data type, interaction, and business requirements—not visual similarity.

### Priority Order

1. **Official GEMS Components:** Variants, properties, sizes, states, and visual specifications.
2. **GEMS Page Samples & UX Patterns:** Contextual usage, grouping, layout, and interaction.
3. **HSD/BRD:** Data requirements, validation, permissions, and workflows.
4. **General UI/UX Principles:** Fallback when GEMS provides no specific guidance.

GEMS governs component design; HSD/BRD governs business behavior.

Read only the relevant GEMS components, Page Samples, and UX Patterns.

## 2. Component Selection Matrix

| Requirement | Component | Usage |
|---|---|---|
| Single-line text or number | Input Field — Default | Nama, nomor identitas |
| Text with contextual icon | Input Field — Icon leading | Pencarian |
| Value with preceding selection | Input Field — Leading dropdown | Kode negara + nomor |
| Value with trailing selection | Input Field — Trailing dropdown | Nilai + satuan |
| Value with fixed prefix | Input Field — Leading text | Rp + nominal |
| Payment information | Input Field — Payment input | Official payment pattern |
| Multiple entered values | Input Field — Tags | Kata kunci |
| Value with attached action | Input Field — Trailing button | Kode + aksi terkait |
| Multiline text | Textarea — Default | Catatan, deskripsi |
| Supported tag-oriented multiline input | Textarea — Tags | Tag content |
| Selection from predefined options | Input Dropdown | Follow `input-dropdown.md` |
| Date or time selection | Date & Time Picker | Follow `date-time-picker.md` |

**Rules**
- Select the component matching the actual data and interaction.
- Do not replace structured selection with free-text Input.
- Do not force multiline content into single-line Input.
- Do not invent component capabilities or business requirements.

## 3. Input Field

### 3.1 Available Properties

| Property | Official Values |
|---|---|
| `Size` | `sm`, `md` |
| `Type` | `Default`, `Icon leading`, `Leading dropdown`, `Trailing dropdown`, `Leading text`, `Payment input`, `Tags`, `Trailing button` |
| `State` | `Placeholder`, `Filled`, `Focused`, `Disabled` |
| `Destructive` | `False`, `True` |

Use only combinations available in the official GEMS component.

### 3.2 Type Usage Matrix

| Type | When to Use | Restriction |
|---|---|---|
| Default | Standard single-line text/number | Apply requirement-defined formatting |
| Icon leading | Icon clarifies input purpose | No decorative icons |
| Leading dropdown | Selection precedes and relates to value | Not for unrelated selections |
| Trailing dropdown | Selection follows and relates to value | Not for standalone selections |
| Leading text | Fixed prefix accompanies editable value | Prefix must not replace editable content |
| Payment input | Official payment interaction | Not for ordinary numeric input |
| Tags | Multiple user-entered values | Multi-value behavior must be supported |
| Trailing button | Action operates on the field value | Not for full-form submission |

### 3.3 Size Rules

| Size | Usage |
|---|---|
| `sm` | Compact contexts supported by GEMS |
| `md` | Standard contexts supported by GEMS |

- Use official component sizing, padding, typography, and icon dimensions.
- Keep equivalent fields consistently sized within a form.
- Follow relevant GEMS component and Page Sample layouts.
- Do not infer production measurements from documentation frames.
- Do not invent additional Input Field sizes.

### 3.4 Type-Specific Rules

**Icon leading**
- Use official GEMS icons and `icons.md`.
- Preserve icon size, color, and alignment.
- Keep field labels understandable without relying on icons alone.

**Leading/Trailing dropdown**
- Use the original combined Input variant.
- Preserve the relationship between selection and entered value.
- Follow `input-dropdown.md` for selection behavior.
- Do not manually assemble unsupported combinations.

**Leading text**
- Use for a fixed, non-editable prefix.
- Follow product requirements for currency, unit, or format.

**Payment input**
- Use only when the product requires a supported payment interaction.
- Do not invent payment methods, masking, or formatting rules.

**Tags**
- Follow HSD/BRD for allowed values, entry limits, and duplicate handling.
- Preserve entered tags during validation.
- Distinguish free-text tags from selection-based Dropdown Tags.

**Trailing button**
- Use only for actions directly related to the field.
- Follow `button.md` for its action and interaction.
- Do not use as a replacement for the main form action.

## 4. Input Field States & Validation

### 4.1 State Matrix

| State | Condition | Behavior |
|---|---|---|
| `Placeholder` | No entered value | Editable placeholder |
| `Filled` | Value exists, not focused | Display entered value |
| `Focused` | Input receives focus | Official visible focus |
| `Disabled` | Interaction unavailable | Non-editable |

**Rules**
- Preserve user-entered values when focus changes.
- Use official GEMS state styling.
- Maintain visible keyboard focus.
- Disabled inputs must not accept edits.
- Do not use Disabled to represent validation errors.
- Do not create a `Success` state.

### 4.2 Destructive & Error Matrix

`Destructive` is a component property, **not a State**.

| Condition | State | Destructive |
|---|---|---|
| Empty, valid | Placeholder | False |
| Filled, valid | Filled | False |
| Focused, valid | Focused | False |
| Empty, invalid | Placeholder | True |
| Filled, invalid | Filled | True |
| Focused, invalid | Focused | True |
| Error resolved | Appropriate normal state | False |
| Disabled | Disabled | False |

**Rules**
- Use `Destructive=True` only for officially supported error variants.
- Display a specific error message when validation fails.
- Preserve entered values and restore normal styling after correction.
- Do not create success borders, green check icons, or custom error styles.
- Do not assume every property combination is supported.

## 5. Textarea Input Field

### 5.1 Available Properties

| Property | Official Values |
|---|---|
| `Type` | `Default`, `Tags` |
| `State` | `Placeholder`, `Default`, `Focused`, `Disabled` |
| `Destructive` | `False`, `True` |

**Important:** Textarea uses `State=Default`, not `Filled`.

No `Size=sm/md` property has been established for this referenced component.

### 5.2 Type Usage

| Type | When to Use | Example |
|---|---|---|
| Default | Multiline text entry | Catatan, Deskripsi |
| Tags | Supported tag-oriented content | Daftar Tag |

### 5.3 States & Validation

| State | Normal | Error |
|---|---|---|
| Placeholder | Empty placeholder | Official destructive appearance |
| Default | Normal unfocused textarea | Official destructive appearance |
| Focused | Editing with focus | Official focused-error appearance |
| Disabled | Non-editable | Do not assume Destructive=True is available |

**Rules**
- Preserve line breaks, text wrapping, and entered values.
- Use `Default` for normal, unfocused Textarea.
- Use `Focused` while editing.
- Use supported `Destructive=True` variants for errors.
- Do not invent `Filled`, `Success`, or custom sizes.
- Do not assume unsupported Disabled + Destructive combinations exist.
- Follow HSD/BRD for character limits and required status.

## 6. Supporting Form Components

These components support Input composition. They do not replace the primary Input Field or Textarea specifications.

### 6.1 Form

Official states:

- `Default`
- `Focus`
- `Filled`

**Rule:** Preserve exact component naming. Form uses `Focus`, while Input Field uses `Focused`.

Do not transfer Form states to Input Field or Textarea.

### 6.2 Mega Input Field Base

| Property | Available Values |
|---|---|
| Size | `sm`, `md`, `lg` |
| State | `Placeholder`, `Filled`, `Focused`, `Disabled` |

- Use only where official GEMS composition requires this base component.
- Preserve original supported properties.
- Do not transfer its `lg` size to the standard Input Field.
- Do not treat internal/base components as interchangeable with regular Input components.

### 6.3 Text Editor

Available configurations:

- `Property 1=Default`
- `Property 1=Filled`

Use only when the product requires the corresponding GEMS text-editing interaction.

Do not replace ordinary Textarea or invent editing tools without support.

### 6.4 Form Section

Official layouts:

- `Layout = Stacked`
- `Layout = Side Label`

Use the relevant official layout for field grouping, alignment, and responsive presentation.

Do not recreate supported Form Section layouts manually.

### 6.5 Field Repeater

Use when users need multiple entries of the same supported field structure.

**Rules**
- Follow the official Field Repeater component and relevant UX Pattern.
- Use GEMS components for repeated fields and associated actions.
- Preserve existing values when rows are added or removed.
- Follow HSD/BRD for add/remove permissions and limits.
- Do not invent repeated fields, minimum/maximum counts, or business behavior.

## 7. Shared Validation & Error Handling

### 7.1 Validation Matrix

| Condition | Behavior |
|---|---|
| Required field empty | Show a specific required-field message |
| Invalid format | Explain expected format |
| Invalid length | Explain allowed length |
| Value outside allowed range | Explain valid boundaries |
| Cross-field conflict | Explain the conflicting values |
| Validation corrected | Restore normal component styling |

### 7.2 Validation Rules

**MUST**
- Follow HSD/BRD for required fields, formats, limits, and dependencies.
- Preserve user-entered values after validation errors.
- Use official GEMS destructive styling.
- Associate messages with the correct field.
- Follow approved validation timing and interaction patterns.

**MUST NOT**
- Invent validation requirements.
- Clear or silently modify user input.
- Use Disabled as error feedback.
- Add unsupported success states.
- Display errors unnecessarily before users can reasonably complete entry.

### 7.3 Error Message Examples

| Scenario | Example |
|---|---|
| Required name | Nama lengkap wajib diisi. |
| Invalid phone | Format nomor telepon tidak sesuai. |
| Required description | Deskripsi wajib diisi. |
| Character limit | Maksimal karakter telah terlampaui. |

Examples illustrate wording only. Actual rules come from product requirements.

## 8. Labels, Placeholder & Helper Text

### 8.1 Labels

- Use specific labels matching HSD/BRD terminology.
- Associate labels with the corresponding fields.
- Maintain consistent wording across related screens.
- Follow GEMS Typography and Form patterns.
- Do not use placeholder as the only label for important fields.

### 8.2 Placeholder

- Keep text short and contextual.
- Use examples or expected formats when helpful.
- Do not treat placeholders as entered values.
- Do not copy unrelated sample content.

### 8.3 Helper Text

Use for instructions, accepted formats, constraints, or consequences that need explanation.

- Follow official GEMS styling.
- Show only relevant information.
- Do not invent business restrictions.

### 8.4 Required & Optional

- Required/optional status MUST come from HSD/BRD.
- Follow GEMS required-indicator conventions.
- Do not mark every field required by default.
- Do not submit incomplete required values when product rules prohibit it.

## 9. Contextual Usage — Forms, CRUD & States

### 9.1 Usage Matrix

| Context | Component | Key Rule |
|---|---|---|
| Registration | Input Field — Default | Fields follow HSD/BRD |
| Free-text Search | Input Field — Icon leading | Follow Search UX Pattern |
| Notes | Textarea — Default | Preserve multiline content |
| Currency | Input Field — Leading text | Prefix follows requirements |
| Phone number | Input Field — Leading dropdown | Only if country selection is needed |
| Payment | Input Field — Payment input | Official payment pattern |
| Keywords | Input Field — Tags | Multi-value must be supported |
| Field-specific action | Input Field — Trailing button | Action applies to field |
| Repeated entries | Field Repeater | Repetition must be supported |
| Grouped form | Form Section | Use official layout |

### 9.2 Create

- Use only fields required by the product workflow.
- Apply appropriate Type, Size, State, and validation.
- Follow GEMS Form Section and relevant Add New Data UX Pattern.
- Use `button.md` for Save, Submit, and Cancel actions.
- Do not invent additional fields or default values.

### 9.3 Edit

- Display existing values accurately.
- Preserve unchanged data.
- Respect field-level permissions.
- Follow relevant GEMS Edit Data UX Pattern.
- Do not clear values, overwrite data silently, or allow unauthorized editing.

### 9.4 Read / Detail

- Use appropriate GEMS display components for non-editable information.
- Use Disabled Input only when the official pattern requires a disabled form control.
- Do not universally represent read-only data with disabled inputs.

### 9.5 Search & Filter

- Use Input Field for free-text search when supported.
- Use official Dropdown for structured selections.
- Preserve search values according to the product interaction.
- Do not invent search criteria or filters.
- Follow relevant GEMS Search, Filter, and Input guidelines.

### 9.6 Delete

- Delete is an action governed by `button.md` and applicable confirmation patterns.
- Use Input or Textarea for deletion reasons only when required by the product.
- Do not invent mandatory reason fields.

### 9.7 Empty State

- Use the official GEMS Empty State component or relevant UX Pattern.
- Show contextual wording and approved recovery/create actions.
- Do not add unnecessary editable fields to empty states.
- Do not invent records to avoid displaying an empty state.

### 9.8 Loading & Error State

- Follow official GEMS loading and error patterns.
- Preserve entered values during recoverable failures.
- Distinguish field-validation errors from page-level errors.
- Do not create custom Input loading states.

## 10. Layout, Responsive & Accessibility

### 10.1 Layout

- Follow official GEMS Form, Form Section, Page Samples, and UX Patterns.
- Preserve label, field, helper text, and error-message relationships.
- Use official spacing, radius, typography, and effects.
- Maintain consistent field widths and alignment where appropriate.
- Do not invent input dimensions or internal spacing.

### 10.2 Responsive

- Follow GEMS responsive component behavior.
- Adapt surrounding containers rather than modifying official Input styling.
- Preserve readability, touch usability, and field grouping.
- Do not invent mobile-specific variants.

### 10.3 Accessibility

- Maintain visible keyboard focus.
- Associate labels and validation messages with their fields.
- Preserve logical focus order.
- Distinguish editable, disabled, and invalid states.
- Do not rely on color alone to communicate errors.
- Do not make disabled controls interactive.

## 11. AI Implementation Rules

When implementing Input components:

1. **Understand Requirements:** Identify data type, field purpose, required status, formatting, permissions, and validation.
2. **Choose Component:** Select the matching official GEMS Input Field, Textarea, or supporting component.
3. **Apply Properties:** Use only supported Type, Size, State, and Destructive combinations.
4. **Apply Content:** Use approved labels, placeholders, helper text, and initial values.
5. **Apply Behavior:** Preserve input, validation, focus, disabled rules, and product-specific workflow.
6. **Follow GEMS Context:** Reference relevant Components, Page Samples, and UX Patterns.
7. **Resolve Exceptions:** Request Human Approval if an unsupported component or essential business decision is required.

These are implementation instructions—not an additional validation report.

## 12. Strict Restrictions & Human Approval

### 12.1 Strict Rules

**MUST**
- Use original GEMS General components and supported properties.
- Follow Foundation and relevant component guidelines.
- Preserve component references, states, values, and accessibility.
- Match content and behavior to approved product requirements.

**MUST NOT**
- Use CCM Input components or CCM styling.
- Create custom Input variants, sizes, states, or colors.
- Hardcode styling outside official GEMS components.
- Transfer component properties between unrelated families.
- Invent validation rules, required fields, or data formats.
- Create Success styling absent from GEMS.
- Replace Dropdown or Date/Time Picker with free-text Input without approval.
- Recreate existing GEMS component compositions manually.
- Modify user data silently.
- Invent permissions, workflows, or product functionality.
- Treat illustrative examples as universal requirements.

### 12.2 Human Approval

Request Human Approval when:

- No official GEMS component supports the required interaction.
- An unsupported visual variant or behavior is necessary.
- Essential validation or business requirements are unclear.
- Implementation would otherwise require inventing product functionality.

Combine related clarification questions into one confirmation.

**Fallback:** Use the closest supported GEMS General Input component based on data type and interaction. Never use CCM or invent unsupported design and business rules.

## 13. Official Figma References

### 13.1 Main Components

| Component | Figma Reference |
|---|---|
| Input Library | [GEMS Input](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=12-6891) |
| Input Field | [GEMS Input Field](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=219-5292) |
| Textarea | [GEMS Textarea](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-4425) |

### 13.2 Supporting Components

| Component | Figma Reference |
|---|---|
| Text Editor | [GEMS Text Editor](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=12-6972) |
| Form | [GEMS Form](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=195-1595) |
| Mega Input Field Base | [GEMS Mega Input Field Base](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1870-13817) |
| Field Repeater | [GEMS Field Repeater](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2819-67577) |
| Form Section | [GEMS Form Section](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2825-25548) |

### 13.3 Related Guidelines

Apply relevant guidelines from the GEMS repository:

- `foundation/color.md`
- `foundation/typography.md`
- `foundation/spacing-radius.md`
- `foundation/effects.md`
- `components/button.md`
- `components/icons.md`
- `components/input-dropdown.md`
- `components/date-time-picker.md`

Use actual repository paths if filenames differ.

**Contextual References:** Read GEMS Components, Page Samples, and UX Patterns only when relevant to the requested interface.

---

**FINAL RULE:** Every Input MUST use an official GEMS General component with correct Type, Size, State, Destructive property, content, and behavior. Preserve original Figma styling, follow product requirements, and never use CCM or invent unsupported configurations.
