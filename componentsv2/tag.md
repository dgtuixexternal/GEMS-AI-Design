
# GEMS Design System — Components / Tag

> **MANDATORY:** All Tags MUST use existing GEMS General Tag components and official Figma variants. AI MUST determine whether Tag is appropriate based on content meaning, interaction requirements, and relevant GEMS Page Samples & UX Patterns. CCM styling, custom Tag components, and unsupported variants are prohibited.

> **CORE PRINCIPLE:** Use Tag to represent meaningful labels, categories, attributes, or selectable/removable items. Do not use Tag as a universal replacement for Badge, Checkbox, Button, or Dropdown.

## 1. Sources & Priority

**Official Figma References**
- [GEMS Tag — Overview](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=23-1305)
- [GEMS Tag — Main Component](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=424-1114)
- [GEMS Tag Close X](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=424-1469)
- [GEMS Tag Checkbox](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=424-1491)
- [GEMS Tag Count](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=424-1482)
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1105-7310)

**Priority Order**
1. **GEMS Tag Components:** Official variants, appearance, structure, and interaction states.
2. **GEMS Foundation:** Color, typography, spacing, radius, effects, and icons.
3. **GEMS Page Samples & UX Patterns:** Contextual usage, placement, and behavior.
4. **HSD/BRD:** Available values, categories, selection limits, permissions, and business rules.
5. **General UI/UX Principles:** Fallback when GEMS has no specific guidance.

GEMS defines visual implementation. Product requirements determine data and behavior.

---

## 2. Purpose & When to Use

Tag is a compact component used to represent labels, categories, attributes, selected values, or related items.

**Use Tag for:**
- Categorizing content.
- Displaying selected filter values.
- Representing multiple selected items.
- Showing removable selections.
- Displaying compact labels or attributes.
- Supporting selectable categories when the workflow requires them.
- Associating people or entities with information.

### Tag vs Other Components

| User Need | Correct Component |
|---|---|
| Category or attribute label | Tag |
| Selected filter value | Tag with supported remove behavior |
| Multiple selected items | Tag |
| Removable selected item | Tag with `X close` |
| Selectable category option | Tag with supported Checkbox pattern |
| Record status | Badge |
| Primary or secondary action | Button |
| Binary setting | Toggle |
| Standard form selection | Checkbox / Radio Button |
| Select option from a list | Dropdown |
| Brief explanation | Tooltip |

**Selection Rules**
- Use Tag when compact labels or selected items improve understanding.
- Use Badge for semantic workflow status.
- Use Checkbox/Radio Button for standard selection controls unless Tag selection is established by the relevant pattern.
- Do not replace Button with Tag.
- Do not add Tags merely as decoration.
- Do not convert every category or attribute into a Tag when plain text is clearer.

---

## 3. Available Variants & Properties

Use the original GEMS Tag component and preserve its Figma reference.

### Official Properties

| Property | Available Values |
|---|---|
| `Size` | `sm`, `md`, `lg` |
| `Icon` | `False`, `Dot`, `Country`, `Avatar` |
| `Action` | `Text only`, `X close`, `Count` |
| `Checkbox` | `True`, `False` |

Use supported combinations from the official GEMS component.

### Component Rules

- MUST use the existing GEMS General Tag component.
- MUST preserve official dimensions, spacing, radius, typography, and colors.
- MUST select the correct properties instead of manually modifying another variant.
- MUST NOT create new Size, Icon, Action, or Checkbox values.
- MUST NOT detach or reconstruct Tag components.
- MUST NOT introduce custom CCM-derived styling.

---

## 4. Tag Size Usage

| Size | Recommended Context |
|---|---|
| `sm` | Compact layouts, dense information, table content |
| `md` | Standard labels, filters, and form selections |
| `lg` | Larger Tag presentations where supported by GEMS |

**Rules**
- Choose Size based on component context and official GEMS examples.
- Maintain consistent Tag sizes within the same component group.
- Follow the sizing used by the relevant Page Sample or UX Pattern.
- Do not enlarge Tags manually to simulate unsupported sizes.
- Do not change font size, padding, or radius independently.

---

## 5. Icon Variants & Usage

### Available Icon Variants

| Icon | Purpose | Recommended Usage |
|---|---|---|
| `False` | Text-only Tag | General categories and attributes |
| `Dot` | Compact visual indicator | Category distinction when meaningful |
| `Country` | Country-related identity | Selected country or regional value |
| `Avatar` | Person-related identity | Selected user, employee, or participant |

### Usage Rules

- Select Icon based on the actual information represented.
- Use `False` when text alone communicates the information.
- Use `Dot` only when its visual meaning is defined or helpful.
- Use `Country` only for relevant country-related values.
- Use `Avatar` only for actual people or supported identities.
- Do not add icons merely to make Tags visually attractive.
- Do not invent country flags or person identities.
- Preserve icon proportions and alignment from GEMS.
- Follow `Foundation/icons.md`, `Foundation/misc-icons.md`, and GEMS Avatar specifications where applicable.

**Important:** An icon MUST reinforce the Tag's meaning, not create an unsupported semantic interpretation.

---

## 6. Action Variants

### Available Actions

| Action | Purpose | Recommended Usage |
|---|---|---|
| `Text only` | Display label or value | Categories and read-only attributes |
| `X close` | Remove or dismiss a Tag | Selected filters or removable items |
| `Count` | Display an associated quantity | Categories or groups with counts |

### 6.1 Text Only

Use when the Tag represents information without a removal action.

**Examples**
- Department category.
- Document type.
- Assigned category.

**Rules**
- Text MUST reflect actual data.
- Do not imply click or selection behavior if none exists.
- Do not add hover or pointer behavior without a supported interaction.

### 6.2 X Close

Use when users are permitted to remove the represented selection.

**Examples**
- Removing a selected filter.
- Removing a selected participant.
- Removing a selected category.

**Rules**
- Removal MUST follow actual product behavior.
- The Close action MUST be supported by the relevant workflow.
- Removing a Tag MUST update the corresponding selected value.
- Do not assume removal automatically deletes the underlying record.
- Do not use X Close for read-only categories or statuses.
- Do not introduce destructive actions through Tag removal without the required confirmation.

### 6.3 Count

Use when a meaningful quantity is associated with a label.

**Examples**
- Category with a record count.
- Filter group with selected-item count.

**Rules**
- Count MUST reflect actual available data.
- Do not invent quantities.
- Do not treat Count as a required element for every Tag.
- Use the official GEMS Count component and supported sizes.

---

## 7. Checkbox Tag & Selection

GEMS supports Tags containing Checkbox.

### Available Checkbox Properties

| Property | Official Values |
|---|---|
| `Checked` | `True`, `False` |
| `Size` | `sm`, `md`, `lg` |
| `State` | `Default`, `Hover`, `Focused`, `Disbaled` |

**Note:** `Disbaled` is the spelling appearing in the referenced Figma component. Preserve the official property value until the component library corrects it.

### When to Use

- Selectable categories.
- Multi-selection patterns that use Tag controls.
- Choice groups explicitly designed with Tags.
- Filter selections when supported by GEMS patterns.

### Selection Rules

- Use Checkbox Tag only when selection is an actual requirement.
- Checked state MUST reflect the selected value.
- Unchecked state MUST reflect an unselected value.
- Disabled state MUST prevent interaction.
- Preserve official Hover and Focused styling.
- Do not invent additional selection states.
- Do not assume all Tags are selectable.
- Do not replace standard Checkbox controls with Tag selection unless the UX pattern supports it.

### Selection Behavior

- Selection MUST update the corresponding product data or filter state.
- Selection limits MUST follow HSD/BRD.
- Do not invent maximum selection counts.
- Do not assume multi-selection is allowed when the workflow supports only one value.
- Preserve accurate selected values after applying or clearing filters.

---

## 8. Supporting Tag Components

### 8.1 Tag Close X

Official properties:

| Property | Available Values |
|---|---|
| `Size` | `sm`, `md`, `lg` |
| `State` | `Default`, `Hover` |

**Rules**
- Use only with supported removable Tag patterns.
- Match Close size with the parent Tag.
- Preserve official icon dimensions and states.
- Provide an accessible label describing what will be removed.
- Do not treat Close as an underlying record deletion action.

### 8.2 Tag Count

Official properties:

| Property | Available Values |
|---|---|
| `Size` | `sm`, `md`, `lg` |

**Rules**
- Use Count only when a meaningful quantity exists.
- Keep Count consistent with the parent Tag.
- Use actual values.
- Preserve official typography and component sizing.

### 8.3 Tag Checkbox

- Use the official supporting Checkbox component.
- Preserve Checked and interaction states.
- Match size with the parent Tag.
- Follow the selected workflow's behavior.

---

## 9. Usage in Forms & Filters

### 9.1 Selected Filter Tags

Use Tag to represent active filters when the approved design benefits from visible selected values.

**Example**
- Department: Finance.
- Location: Jakarta.
- Category: Transportasi.

**Rules**
- Display actual active filters.
- Use `X close` only when individual removal is supported.
- Removing a filter Tag MUST update the corresponding filter state.
- Keep Filter Tags synchronized with Dropdown, Date Picker, or other filter controls.
- Do not duplicate filter information unnecessarily.
- Do not invent active filter values.

### 9.2 Multi-Select Input

Tags MAY represent selected values in supported multi-select patterns.

**Rules**
- Use the official GEMS Input/Dropdown component for selection.
- Use Tag for selected-value presentation when the pattern supports it.
- Preserve selected values and selection limits.
- Do not assume every Dropdown supports Tag-based multi-selection.
- Do not create a custom Tag input when an approved GEMS component already exists.

### 9.3 Form Content

- Use Tags when they help users understand selected or associated values.
- Use read-only Tags for values that should not be modified.
- Use removable Tags only when users have permission to change the selection.
- Maintain consistency between form values and Tags.

---

## 10. Usage in Data Table & Detail Pages

### Data Table

Use Tag for relevant categories, labels, or attributes within a table when the official GEMS cell composition supports it.

**Rules**
- Follow GEMS Table Cell specifications.
- Use Badge—not Tag—for standard workflow statuses.
- Avoid displaying excessive Tags in one cell.
- Preserve readability and row height consistency.
- Do not add Tag-based actions unless supported by the table workflow.

### Detail Page

Tags may represent:
- Related categories.
- Assigned people.
- Document attributes.
- Selected classifications.

**Rules**
- Keep Tags close to their relevant data.
- Use consistent sizes and spacing.
- Do not make read-only attributes appear removable.
- Do not duplicate information unnecessarily.

---

## 11. Content & Label Rules

- Use concise, meaningful labels.
- Follow HSD/BRD terminology.
- Use actual category names and values.
- Keep terminology consistent across Forms, Filters, Tables, and Details.
- Avoid overly long labels when a shorter approved term is available.
- Do not use ambiguous abbreviations.
- Do not invent labels, counts, categories, or identities.
- Do not use Tag colors to imply an unsupported status.

### Grouping

- Group related Tags together.
- Maintain readable spacing.
- Preserve consistent sizing.
- Avoid excessive Tag groups that reduce clarity.
- Follow the relevant GEMS Page Sample for wrapping and layout.

---

## 12. Interaction & State Behavior

| Condition | Expected Behavior |
|---|---|
| Default | Display official Tag appearance |
| Hover | Apply supported hover styling to interactive elements |
| Focused | Show official focus treatment where supported |
| Checked | Reflect selected value |
| Unchecked | Reflect unselected value |
| Disabled | Prevent unavailable interactions |
| Remove | Remove the represented selection when permitted |

**Rules**
- Interactive states MUST reflect actual user actions.
- Read-only Tags MUST NOT imply unsupported interactions.
- Do not invent loading, active, or custom semantic states.
- Do not use Close to change business status.
- Do not make Tag removal trigger unrelated operations.
- Preserve keyboard and screen-reader accessibility.

---

## 13. Responsive Behavior

- Preserve official GEMS Tag sizes and component structure.
- Follow relevant Desktop and Mobile Page Samples.
- Allow appropriate wrapping where supported by the layout.
- Maintain readable labels and sufficient interaction targets.
- Do not manually shrink Tag contents to fit narrow screens.
- Do not hide essential selected values without a supported alternative.
- Do not invent mobile-only Tag variants.

---

## 14. Foundation & Component Dependencies

All Tags MUST follow GEMS Foundation.

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | Official General colors, text, backgrounds, borders |
| `Foundation/typography.md` | Tag labels and Count typography |
| `Foundation/spacing-dan-radius.md` | Padding, gaps, radius, grouping |
| `Foundation/effect-styles.md` | Official effects where applicable |
| `Foundation/icons.md` | Close and supporting icon treatment |
| `Foundation/misc-icons.md` | Specialized icons where relevant |
| `Foundation/design-annotations.md` | Component usage specifications |

### Related Components

| Requirement | Related Guideline |
|---|---|
| Workflow status | `components/badge.md` |
| Selected values | GEMS Input / Dropdown |
| Standard selection | GEMS Checkbox / Radio Button |
| People identity | GEMS Avatar |
| Primary action | `components/button.md` |
| Category information in tables | `components/data-table.md` |
| Additional explanation | `components/tooltip.md` |

Use actual repository paths if filenames differ.

### Visual Rules

- Preserve original GEMS General Tag component references.
- Apply official Text Styles.
- Use GEMS General colors and styles.
- Preserve official spacing, padding, radius, and icon dimensions.
- Do not manually recreate Tag appearance with custom shapes.
- Do not introduce hardcoded HEX/RGB/HSL or unsupported typography.
- Do not use CCM-derived styling.

---

## 15. Accessibility

**MUST**
- Keep Tag labels understandable without relying on icons alone.
- Maintain readable color contrast.
- Provide accessible names for Close actions.
- Support keyboard access for interactive Tags.
- Preserve visible Focused states where supported.
- Communicate selected and disabled states accurately.
- Maintain consistent accessibility across relevant layouts.

**MUST NOT**
- Use color alone to communicate selection.
- Make read-only Tags appear interactive.
- Hide important information behind unsupported interactions.
- Use ambiguous icon-only actions.

---

## 16. Strict AI Rules

### MUST

1. Use existing GEMS General Tag components.
2. Determine whether Tag is appropriate for the content.
3. Select supported Size, Icon, Action, and Checkbox properties.
4. Use actual labels, categories, identities, and counts.
5. Preserve official component structure and interaction states.
6. Follow relevant GEMS Page Samples and UX Patterns.
7. Use official GEMS Foundation styles.
8. Follow HSD/BRD for selection, removal, and permissions.
9. Maintain responsive readability and accessibility.
10. Request Human Approval for unsupported interactions or variants.

### MUST NOT

1. Use CCM components or CCM-specific styling.
2. Create custom, detached, or duplicate Tag components.
3. Invent unsupported properties or variants.
4. Use Tag as a universal replacement for Badge.
5. Use Tag instead of Button for primary actions.
6. Add Close to read-only values.
7. Make Tags selectable without a selection requirement.
8. Invent categories, quantities, identities, or business values.
9. Treat Tag removal as record deletion.
10. Invent selection limits or bulk behaviors.
11. Hardcode styling outside official GEMS.
12. Introduce unsupported designs without Human Approval.

---

## 17. AI Tag Selection Decision

When designing a screen:

1. **Identify Content:** Determine whether the element represents a label, category, status, selected value, or action.
2. **Choose Component:** Select Tag, Badge, Checkbox, Button, Dropdown, or plain text based on actual purpose.
3. **Select GEMS Variant:** Choose supported Size, Icon, Action, and Checkbox properties.
4. **Define Content:** Use actual labels, identities, and counts.
5. **Define Interaction:** Apply selection or removal only when permitted.
6. **Determine Placement:** Follow relevant GEMS Page Samples and UX Patterns.
7. **Apply Foundation:** Preserve official colors, typography, spacing, radius, effects, and icons.
8. **Preserve Accessibility:** Support accurate focus, selection, and action semantics.

### Human Approval

Request Human Approval when:
- The required Tag behavior is not supported by GEMS.
- A custom selectable or removable pattern is proposed.
- The product requires unsupported Tag variants.
- A new business interaction would otherwise need to be invented.

Combine related approval questions into one confirmation to minimize Claude AI context usage.

### Fallback

If a Tag pattern is unsupported:
1. Prefer an existing GEMS component that accurately serves the need.
2. Use Badge, Checkbox, Dropdown, or another appropriate component when more suitable.
3. Request Human Approval before introducing a new interaction or design.
4. Never substitute CCM styling or fabricate behavior.

> **FINAL INSTRUCTION:** Use official **GEMS General Tag** components only when labels, categories, selected values, or removable items genuinely benefit from Tag presentation. Select supported variants, preserve accurate data and interactions, follow GEMS Foundation and contextual patterns, and never replace Badge or other components without a valid functional reason.
