
# GEMS Design System — Components / Checkbox

> **MANDATORY:** All Checkbox controls MUST use official GEMS General components, supported properties, sizes, and states. Checkbox usage MUST follow the actual selection requirements and relevant GEMS UX Patterns. Custom and CCM-specific components are prohibited.

## 1. Sources & Priority

**Official References**
- [GEMS Checkbox](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=12-12021)
- [GEMS Checkbox Base](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=263-2292)
- [GEMS Checkbox with Text](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=263-2427)
- [GEMS Checkbox Group Item](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1959-40654)
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1105-7310)

**Priority Order**
1. **Official Checkbox Components:** Source of truth for component structure, properties, variants, dimensions, and states.
2. **GEMS Components:** Follow official specifications for related Data Table, Button, Modal, Input, and Selection components.
3. **Page Samples & UX Patterns:** Reference for contextual usage in forms, tables, and workflows.
4. **Product Requirements (HSD/BRD):** Determine selectable options, validation, permissions, and business behavior.
5. **General UI/UX Principles:** Fallback only when GEMS provides no specific guidance.

**Component Restrictions**
- MUST use official GEMS General Checkbox components.
- MUST NOT use CCM-specific Checkbox components or patterns.
- MUST NOT recreate Checkbox controls using custom shapes, icons, or frames.
- MUST NOT invent unsupported sizes, colors, states, or selection layouts.

---

## 2. Purpose & Usage

Checkbox is a selection control used when users can independently select or deselect one or more options.

Checkbox may also represent selection state in Data Tables or other supported selection groups.

### When to Use

| Context | Recommendation |
|---|---|
| Multiple independent options | Use Checkbox |
| Optional Form setting | Use Checkbox |
| Select multiple table rows | Use Checkbox |
| Select all available records within a defined scope | Use Checkbox with Indeterminate support |
| Select multiple items from a group | Use Checkbox or supported Checkbox Group Item |
| Select one option from mutually exclusive choices | Use Radio, not Checkbox |
| Enable/disable a setting with immediate effect | Consider official Toggle/Switch |
| Choose a value from a large option list | Consider official Dropdown/Multi-select when available |
| Confirm a destructive action | Use Modal confirmation, not Checkbox alone |
| Trigger CRUD action | Use an appropriate GEMS Button |

### Usage Rules

- MUST use Checkbox for independent selection.
- MUST use Radio for mutually exclusive single-choice selection.
- MUST follow HSD/BRD for available options and selection limits.
- MUST preserve selected values when appropriate.
- MUST maintain a clear relationship between each Checkbox and its label.
- MUST NOT use Checkbox merely as decoration.
- MUST NOT use Checkbox as a substitute for Buttons, Tabs, or status indicators.

**Core Principle:** Checkbox represents selection. Business actions require their own explicit controls and approved interaction patterns.

---

## 3. Official Checkbox Base

**Component:** `_Checkbox base`  
**Figma Node:** `263:2292`

### Available Properties

| Property | Available Values |
|---|---|
| `Checked` | `True`, `False` |
| `Indeterminate` | `True`, `False` |
| `Size` | `sm`, `md` |
| `Type` | `Checkbox`, `Radio` |
| `State` | `Default`, `Hover`, `Focused`, `Disabled` |

### Available Sizes

| Size | Checkbox Dimension |
|---|---|
| `sm` | 16 × 16px |
| `md` | 20 × 20px |

These dimensions refer to the Checkbox Base control, not the full clickable area or labeled component.

### Base Rules

- MUST use `Type=Checkbox` for Checkbox functionality.
- MUST choose `sm` or `md` according to the official component usage.
- MUST preserve the original Checkbox shape, icon, border, and colors.
- MUST use the supported visual State.
- MUST NOT resize the base control manually.
- MUST NOT use `Type=Radio` as a Checkbox substitute.
- MUST NOT invent additional sizes or states.

---

## 4. Official Checkbox with Text

**Component:** `check`  
**Figma Node:** `263:2427`

### Available Properties

| Property | Available Values |
|---|---|
| `Checked` | `True`, `False` |
| `Indeterminate` | `True`, `False` |
| `Size` | `sm`, `md` |
| `Type` | `Checkbox`, `Radio` |
| `Text` | `True`, `False` |
| `State` | `Default`, `Hover`, `Focused`, `Disabled` |

### Text Selection

| Configuration | Usage |
|---|---|
| `Text=True` | Checkbox with label and supported description |
| `Text=False` | Checkbox without visible text, when an accessible name is supplied |

### Usage Rules

- MUST use `Text=True` when visible labels or descriptions are needed.
- MUST use official GEMS Text Styles for labels and supporting text.
- MUST preserve label spacing and alignment.
- MUST use meaningful labels describing the selection.
- MUST NOT use generic placeholders as final product content.
- MUST NOT remove labels solely to reduce layout width.
- MUST provide accessible names for icon-only or unlabeled Checkbox controls.

**Important:** The visible label and helper text are part of the selectable option's meaning. They must not introduce different or contradictory instructions.

---

## 5. Checkbox States

Checkbox state reflects both its selected value and its current interaction condition.

### Selection States

| Selection | Properties | Meaning |
|---|---|---|
| Unchecked | `Checked=False`, `Indeterminate=False` | Not selected |
| Checked | `Checked=True`, `Indeterminate=False` | Selected |
| Indeterminate | `Checked=True`, `Indeterminate=True` | Partially selected |

The property combination shown for Indeterminate follows the official GEMS Figma component.

### Interaction States

| State | Usage |
|---|---|
| `Default` | Normal appearance |
| `Hover` | Pointer interaction feedback |
| `Focused` | Keyboard focus feedback |
| `Disabled` | Unavailable selection control |

### State Rules

- MUST preserve official GEMS visual appearance for each supported state.
- MUST update Checked state according to user selection.
- MUST use Indeterminate only when selection is genuinely partial.
- MUST preserve Focused indicators for keyboard users.
- MUST prevent interaction while Disabled.
- MUST NOT use Disabled as a substitute for Unchecked.
- MUST NOT use Indeterminate as an ordinary third choice.
- MUST NOT invent custom state colors or checkbox icons.

---

## 6. Indeterminate & Select All

Indeterminate is primarily used when a parent Checkbox represents multiple child selections.

### Selection Logic

| Child Selection | Parent Checkbox |
|---|---|
| No items selected | Unchecked |
| All eligible items selected | Checked |
| Some eligible items selected | Indeterminate |
| No selectable items | Disabled or omitted according to the official pattern |

### Select All Rules

- MUST define the selection scope before enabling Select All.
- MUST calculate parent selection state from eligible child items.
- MUST update parent state when child selections change.
- MUST update child selections when Select All is triggered.
- MUST respect Disabled items and user permissions.
- MUST NOT display Checked when only some eligible items are selected.
- MUST NOT include inaccessible or ineligible records in selection operations.

### Scope of Selection

For Data Tables, Select All may apply to:
- Current visible page.
- Current filtered results.
- All matching records.

The actual scope MUST follow the approved product behavior.

**MUST NOT** assume Select All automatically includes every record across all pages.

If cross-page selection is supported, clearly communicate the selected scope and count.

---

## 7. Checkbox Group Item

**Component:** `Checkbox group item`  
**Figma Node:** `1959:40654`

This component provides larger selectable items with additional content.

### Available Properties

| Property | Available Values |
|---|---|
| `Selected` | `True`, `False` |
| `Size` | `sm`, `md` |
| `Type` | `Checkbox`, `Radio button`, `Icon simple`, `Icon card`, `Avatar`, `Payment icon` |
| `State` | `Default`, `Hover`, `Focused`, `Disabled` |
| `Breakpoint` | `Desktop`, `Mobile` |

### Type Usage

| Type | Recommended Context |
|---|---|
| `Checkbox` | Selectable item with standard Checkbox |
| `Radio button` | Mutually exclusive item selection |
| `Icon simple` | Selection with a supported contextual icon |
| `Icon card` | Selection where the official card-based icon presentation is relevant |
| `Avatar` | Person-based selection |
| `Payment icon` | Payment-related selection |

### Group Item Rules

- MUST use the official component when card/item-based selection is appropriate.
- MUST select the correct Type based on actual data.
- MUST preserve original selected, hover, focus, and disabled states.
- MUST use official GEMS Icons, Avatars, and Payment Icons.
- MUST follow the supported Desktop or Mobile variant.
- MUST NOT use decorative icons unrelated to the option.
- MUST NOT replace standard Checkbox with a card layout unnecessarily.
- MUST NOT treat `Selected=True` as permission to execute an action automatically.

**Core Principle:** Use Checkbox Group Item when richer option presentation improves understanding. For simple options, prefer the standard Checkbox.

---

## 8. Checkbox in Forms

Checkbox may be used for optional settings, declarations, preferences, or multiple selections.

### Form Usage Matrix

| Context | Recommended Behavior |
|---|---|
| Optional preference | Unchecked unless product requirements specify otherwise |
| Multiple selections | Allow independent selection |
| Required acknowledgment | Clearly communicate requirement |
| Conditional fields | Reveal relevant fields when the related option is selected |
| Edit Form | Reflect the saved values |
| Read-only view | Display the saved state without enabling changes |

### Form Rules

- MUST use the official GEMS Checkbox component.
- MUST determine the initial state from HSD/BRD or saved data.
- MUST use meaningful labels.
- MUST distinguish optional and required selections.
- MUST validate required acknowledgment or minimum-selection rules.
- MUST preserve selections when unrelated validation fails.
- MUST update dependent fields according to approved conditions.
- MUST NOT preselect consent or declarations without an approved requirement.
- MUST NOT silently change saved values before submission.

### Conditional Fields

When Checkbox controls additional fields:

- Show or enable dependent fields only when required by the selected option.
- Preserve or clear dependent values according to HSD/BRD.
- Apply official GEMS field validation.
- Do not invent conditional business logic.

---

## 9. Checkbox in Data Tables

Checkbox is commonly used for row selection and bulk operations.

### Table Selection

| Element | Purpose |
|---|---|
| Header Checkbox | Select all eligible rows within a defined scope |
| Row Checkbox | Select or deselect an individual record |
| Indeterminate Header | Indicates partial selection |
| Selection Count | Shows how many records are selected when supported |
| Bulk Action Controls | Performs actions on selected records |

### Usage Rules

- MUST use official GEMS Checkbox and Data Table components.
- MUST preserve consistent Checkbox alignment across rows.
- MUST maintain selection state across supported table interactions.
- MUST apply the correct Select All scope.
- MUST respect permissions and disabled records.
- MUST update the selected count when applicable.
- MUST NOT make data selection automatically execute CRUD actions.

### Filtering & Pagination

When the table changes:

- Selection behavior MUST follow the approved product workflow.
- Filtering, sorting, and pagination MUST NOT silently alter selection in an undefined way.
- Cross-page selection MUST be explicit if supported.
- Selected records MUST be identifiable before bulk actions execute.

**Important:** Page selection, filtered-result selection, and all-record selection are different behaviors. Do not interchange them without product requirements.

---

## 10. Checkbox & CRUD Operations

Checkbox supports selecting records involved in CRUD workflows.

It does not independently create, update, or delete data.

### CRUD Usage Matrix

| Operation | Checkbox Role | Action |
|---|---|---|
| Create | Select form options or preferences | Save / Submit Button |
| Read | Display selected values or enable record selection | View / Detail action |
| Update | Modify selections in Edit Form | Save Changes Button |
| Delete | Select records for deletion | Delete Button + Confirmation |
| Bulk Update | Select multiple eligible records | Approved Bulk Update action |
| Bulk Delete | Select multiple eligible records | Delete action + Confirmation |

### Create

- MUST follow default values defined by HSD/BRD.
- MUST validate required selections.
- MUST submit selected values only through the approved form action.
- MUST NOT create records merely when Checkbox is selected.

### Read

- MUST accurately display the current selection state.
- MUST use Disabled or read-only presentation when modification is unavailable, following the approved pattern.
- MUST NOT allow unauthorized changes.

### Update

- MUST initialize Checkbox states from existing saved data.
- MUST preserve unrelated data.
- MUST submit changes through the approved action.
- MUST NOT automatically overwrite saved values on every selection change unless explicitly required.

### Delete & Bulk Delete

- MUST select eligible target records.
- MUST provide a distinct Delete action.
- MUST communicate the target count or affected records where appropriate.
- MUST follow `modal.md` for confirmation.
- MUST prevent deletion before valid confirmation.
- MUST NOT use Checkbox as the destructive trigger.

**Core Principle:** Selecting a record and executing an operation are separate user decisions.

---

## 11. Bulk Actions & Permissions

Bulk actions MUST be defined by the product requirements.

### Behavior Rules

- MUST enable bulk actions only when at least one eligible record is selected.
- MUST respect user permissions for every selected record.
- MUST prevent actions on unauthorized or ineligible items.
- MUST use official GEMS Button and Modal components.
- MUST communicate the action's consequences.
- MUST handle partial failures according to the approved workflow.
- MUST update the table after a successful operation.
- MUST NOT assume all selected records support the same action.

### Destructive Operations

Bulk Delete MUST:

1. Identify eligible selected records.
2. Use the official Delete action.
3. Display an appropriate GEMS confirmation Modal.
4. Execute deletion only after confirmation.
5. Update the affected data and selection state after completion.

Use the approved Modal action color rules:
- Red Solid for Delete and Reject.
- Green Solid only for Approval.
- Orange Solid only for Revision Request.
- Red Solid for General actions.

---

## 12. Checkbox vs. Other Controls

Select the component according to the interaction model.

| Requirement | Component |
|---|---|
| Multiple independent selections | Checkbox |
| One mutually exclusive option | Radio |
| Immediate on/off setting | Toggle/Switch when supported |
| Choose from a list | Dropdown |
| Search and select options | Supported searchable selection component |
| Navigate between views | Tabs |
| Execute an action | Button |
| Select a rich option card | Checkbox Group Item |
| Display a status | Badge |

### Selection Rules

- MUST use Checkbox when multiple independent choices are valid.
- MUST use Radio for one mutually exclusive choice.
- MUST use Toggle/Switch only when the interaction represents an appropriate on/off setting.
- MUST use the official component that best matches the user's task.
- MUST NOT select controls based solely on visual preference.

---

## 13. Responsive Behavior

### Standard Checkbox

- Preserve official `sm` and `md` sizes.
- Maintain readable labels and appropriate clickable areas.
- Preserve official spacing and alignment.
- Do not scale Checkbox icons manually for mobile.

### Checkbox Group Item

- MUST use the official `Breakpoint=Desktop/Mobile` property.
- MUST preserve supported item layout and selection states.
- MUST maintain readable content and accessible controls.
- MUST NOT shrink Desktop group items to imitate Mobile.
- MUST NOT invent unsupported responsive layouts.

If the required mobile behavior is unavailable, request Human Approval.

---

## 14. Accessibility

Checkbox implementations MUST:

- Use appropriate Checkbox semantics.
- Expose Checked, Unchecked, and Indeterminate states correctly.
- Support keyboard selection, including Space.
- Maintain visible focus indicators.
- Associate visible labels with their controls.
- Provide accessible names for unlabeled table Checkboxes.
- Communicate Disabled state appropriately.
- Maintain adequate contrast using official GEMS tokens.
- Preserve a usable interaction target.
- Avoid relying solely on color to indicate selection.
- Group related options with meaningful labels when appropriate.

For Data Tables, Checkbox accessible names SHOULD identify the corresponding record or selection scope.

---

## 15. Foundation & Component Dependencies

Checkbox MUST follow existing GEMS guidelines.

### Foundation

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | Official General and semantic colors |
| `Foundation/typography.md` | Official GEMS Text Styles |
| `Foundation/spacing-dan-radius.md` | Spacing, dimensions, and radius |
| `Foundation/effect-styles.md` | Borders, focus rings, and effects |
| `Foundation/icons.md` | Official check and supporting icons |
| `Foundation/misc-icons.md` | Special-purpose visual icons when applicable |
| `Foundation/design-annotations.md` | Relevant component and interaction annotations |

### Related Components

Follow corresponding GEMS guidelines when applicable:

- `input.md`
- `dropdown.md`
- `button.md`
- `button-group.md`
- `data-table.md`
- `modal.md`
- `badge.md`
- `avatar.md`
- `pagination.md`

Use actual repository filenames if different.

### Dependency Rules

- MUST use official GEMS General and semantic tokens.
- MUST preserve original Checkbox dimensions and selected-state styling.
- MUST apply official typography for labels and helper text.
- MUST preserve official spacing, radius, border, and focus effects.
- MUST use official nested GEMS components.
- MUST NOT hardcode HEX/RGB/HSL or unsupported layout values.
- MUST NOT introduce CCM-specific styling or components.
- MUST NOT override original component states or properties.

---

## 16. Strict Rules

### MUST

- Use official GEMS General Checkbox components.
- Select supported Size, Type, Checked, Indeterminate, Text, and State properties.
- Use Checkbox for independent selection.
- Follow official GEMS Page Samples and UX Patterns.
- Maintain accurate selection states.
- Use Indeterminate for partial group selection.
- Respect HSD/BRD, validation, and permissions.
- Use official Table, Button, and Modal components for CRUD workflows.
- Preserve original GEMS visual properties.
- Apply relevant Foundation guidelines.

### MUST NOT

- Use CCM-specific Checkbox components or patterns.
- Create custom Checkbox shapes, icons, sizes, or states.
- Replace official Checkbox instances with manually recreated controls.
- Use Checkbox for mutually exclusive choices when Radio is appropriate.
- Use Checkbox to trigger CRUD actions automatically.
- Use Indeterminate as an ordinary independent selection value.
- Include disabled or unauthorized records in bulk operations.
- Assume Select All includes records outside its defined scope.
- Invent business selection limits or default values.
- Preselect consent without an approved requirement.
- Execute Delete before valid confirmation.
- Introduce unsupported responsive or interaction behavior.
- Override official GEMS nested component specifications.

---

## 17. AI Implementation Instructions

When generating UI using GEMS:

1. **Identify Selection Purpose:** Determine whether Checkbox, Radio, Toggle, Dropdown, or another selection component is appropriate.
2. **Retrieve Official Component:** Use `_Checkbox base`, `check`, or `Checkbox group item` according to the content and interaction.
3. **Select Properties:** Choose the supported Size, Checked, Indeterminate, Text, State, Type, and Breakpoint values.
4. **Define Behavior:** Apply initial values, selection rules, validation, and permissions from HSD/BRD.
5. **Handle Group Selection:** Use correct Indeterminate and Select All behavior when applicable.
6. **Integrate CRUD:** Keep selection separate from Save, Update, Delete, and bulk action execution.
7. **Preserve GEMS:** Apply official component properties, Foundation tokens, and relevant Page Samples / UX Patterns.

**Human Approval Required When:**
- The required selection behavior is unsupported by official GEMS components.
- Selection scope or bulk-action rules cannot be determined from product requirements.
- A new selection layout or responsive behavior is necessary.
- Product requirements conflict with official GEMS specifications.

Combine related clarification questions into one confirmation whenever possible.

If official component properties cannot be accessed or verified, request the necessary Figma access or specifications. Do not invent unsupported details.

---

## Final Instruction

**AI MUST use official GEMS General Checkbox components, select supported properties, and implement selection behavior according to the actual product requirements.**

**Checkbox is a selection control—not a CRUD action trigger.**

**Indeterminate MUST represent partial selection, and Select All MUST operate within a clearly defined scope.**

**All CRUD and bulk operations MUST use official GEMS action components and approved confirmation patterns.**

**CCM components, custom variants, unsupported visual states, and invented business behavior are strictly prohibited.**

**GEMS Design System is the single source of truth for Checkbox visual specifications and supported interaction behavior.**
