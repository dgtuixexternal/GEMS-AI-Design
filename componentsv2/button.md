
# GEMS Design System — Components / Button

> **MANDATORY:** All buttons MUST use official GEMS General Button components from the connected Figma Design System. Preserve their original component properties, variants, sizes, states, colors, icons, and styling. **GEMS Button CCM MUST NOT be used.**

## 1. Source of Truth & Priority

**Official Figma References**

- [GEMS Button Library](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=12-1130)
- [General Button](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=294-4425)
- [Button Close X](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=310-1955)
- [Social Button](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1869-10020)
- [Social Button Groups](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1869-10291)

**Priority Order**

1. **GEMS General Button:** Official component, hierarchy, size, state, and properties.
2. **GEMS Components:** Button implementation within existing GEMS components.
3. **GEMS Page Samples & UX Patterns:** Contextual usage, hierarchy, placement, and action grouping.
4. **Product Requirements:** Business actions, terminology, permissions, and workflows.
5. **General UI/UX Principles:** Fallback only when GEMS has no specific guidance.

Use the connected GEMS Figma Design System as the source of truth. Read only the components, Page Samples, and UX Patterns relevant to the requested screen.

If references conflict, official GEMS component specifications take precedence over visual examples.

## 2. Allowed Button Components

### General Button

Use the existing GEMS General Button with these official hierarchy variants:

| Hierarchy | Purpose |
|---|---|
| `Primary` | Main or highest-priority action |
| `Secondary color` | Contextual supporting action requiring color emphasis |
| `Secondary gray` | Neutral supporting or alternative action |
| `Tertiary color` | Low-emphasis action with contextual color |
| `Tertiary gray` | Low-emphasis neutral action |
| `Link color` | Text-style action with contextual color |
| `Link gray` | Text-style neutral action |

**Official sizes:** `sm`, `md`, `lg`, `xl`, `2xl`.

**Official states:** `Default`, `Hover`, `Focused`, `Disabled`.

**Official icon configurations:** Follow available GEMS component properties, including default, leading icon/dot, and icon-only configurations where supported.

Apply the complete existing component variant. Do not recreate its appearance manually.

### Button Close X

Use the official GEMS Button Close X for dismissing or closing applicable surfaces such as dialogs, panels, and overlays.

- Follow its available size, background, and state properties.
- Respect light/dark-background configurations.
- Position it according to the relevant GEMS component or UX Pattern.
- Do not replace it with a manually drawn X or custom icon button.

### Social Button & Social Button Groups

Use official GEMS Social Button components only for applicable social authentication or integration actions.

- Select the correct supported provider, theme, supporting-text option, and state.
- Use official Social Button Groups when the relevant pattern requires grouped social actions.
- Follow existing `Brand`, `Color`, or `Gray` theme options as defined by the component.
- Social-specific brand styling is permitted only within the official Social Button component—not as permission to use CCM or invent product button colors.
- Never introduce a social provider or login method that the product does not support.

## 3. Strict CCM Exclusion

**MUST NOT**

- Use any Button component, instance, variant, or styling from **GEMS CCM**.
- Use CCM-specific button colors, effects, sizes, typography, or interaction patterns.
- Duplicate or recreate a CCM button as a custom component.
- Copy CCM styling from Page Samples or UX Patterns into General products.
- Treat CCM buttons as equivalent alternatives to GEMS General Button.

**MUST**

- Use official GEMS General Button components.
- Use GEMS Foundation Color tokens and component-defined color properties.
- Preserve original GEMS component references and available variants.

If a design reference contains CCM buttons, use it only to understand the workflow or content. Replace the button implementation with the appropriate GEMS General Button.

If no suitable General Button implementation exists, request human direction before introducing a new button design.

## 4. Button Hierarchy & Selection

Choose button hierarchy based on **action importance, user context, consequences, and the surrounding action group**—not simply the action label.

| Hierarchy | Typical Usage |
|---|---|
| Primary | Save, submit, create, confirm, or complete a main task |
| Secondary color | Contextual edit, delete, or process-control action when shown by GEMS patterns |
| Secondary gray | Cancel, back, supporting edit, export, or utility action |
| Tertiary color | Subtle colored action when supported by a relevant GEMS pattern |
| Tertiary gray | Subtle neutral or lower-priority action |
| Link color / gray | Text-based actions when the component and context support them |

### Primary

Use for the main action in a page section, form, dialog, or action group.

Examples:
- `Simpan`
- `Simpan Perubahan`
- `Buat Pesanan`
- `Kirim Pengajuan`
- `Konfirmasi`

Rules:
- **SHOULD use one Primary per action group**, unless an approved GEMS pattern explicitly requires otherwise.
- Do not apply Primary to every visible button.
- Do not assume every `Edit`, `Delete`, or `Confirm` action must be Primary.
- Use an approved contextual color variation only when supported by official GEMS specifications or patterns.

### Secondary Color

Use when an action needs contextual color emphasis but is not the main action.

Examples from GEMS contextual patterns:
- `Ubah Pesanan` in a table row.
- `Hapus` with red outline on a detail page.
- `Stop Charging` with red outline during an active process.

Rules:
- Match the exact approved GEMS styling and semantic color.
- Destructive actions do **not** automatically require solid red buttons.
- Do not use Secondary Color for every supporting action.

### Secondary Gray

Use for neutral, alternative, or supporting actions.

Examples:
- `Batal`
- `Kembali`
- `Edit`
- `Ekspor Data`
- `Unduh Kode QR`

Rules:
- Commonly pairs with Primary, but can be used alone.
- `Edit` may be Secondary Gray when it supports another action.
- Keep neutral actions visually subordinate to the main action.

### Tertiary Color & Tertiary Gray

Use for low-priority actions when supported by the relevant GEMS component, Page Sample, or UX Pattern.

- `Tertiary color`: Subtle action with contextual color.
- `Tertiary gray`: Subtle neutral action.

Do not invent specific business use cases or color meanings for these variants. If their intended application is unclear, use a clearly supported GEMS pattern or request human direction.

### Link Color & Link Gray

Use only where GEMS supports text-based button actions.

- Preserve official visual treatment and interaction behavior.
- Do not use Link variants merely to avoid button spacing constraints.
- Do not replace a required standard button with a Link button without contextual justification.
- If usage is unclear, follow the relevant GEMS component or request human direction.

## 5. Size, Color, Icons & States

### Size

Select only an existing official GEMS Button size:

`sm` / `md` / `lg` / `xl` / `2xl`

**Size selection MUST follow:**
1. Original GEMS component specification.
2. Equivalent use in the relevant Page Sample or UX Pattern.
3. Surrounding UI density, action importance, and available space.

Rules:
- Maintain consistent sizing within the same action group.
- Follow GEMS sizing for buttons inside tables, forms, dialogs, cards, and headers.
- Use the correct responsive size when GEMS specifies different breakpoint behavior.
- Never invent dimensions, padding, height, or font sizes.
- Do not manually stretch internal button properties to fit a layout; adjust the surrounding container or use an officially supported size.
- Preserve component-defined minimum interaction area and usability.

### Color

- Apply GEMS General semantic color tokens.
- Follow color values defined by the selected official Button variant.
- Use warning, success, or destructive emphasis only when an approved GEMS pattern supports it.
- Do not choose color solely from the action verb.
- Never hardcode HEX, RGB, HSL, or unsupported color values.
- Never use CCM color tokens or CCM button styling.

### Icons

- Use official GEMS icons according to `icons.md`.
- Preserve the button component's icon placement, size, spacing, and alignment.
- Use icon-only buttons only where the component and interaction context support them.
- Icon-only actions MUST remain understandable through accessible naming or tooltips where appropriate.
- Do not replace existing GEMS component icons with arbitrary alternatives.
- Do not insert an icon when the original GEMS component or pattern does not require one.

### States

| State | Rule |
|---|---|
| `Default` | Normal interactive appearance |
| `Hover` | Official pointer-hover appearance; not a selected or clicked state |
| `Focused` | Preserve official visible keyboard-focus treatment |
| `Disabled` | Official disabled appearance; action must not execute |

Additional rules:
- Implement functional interaction behavior consistent with the displayed state.
- Do not simulate Disabled using opacity alone.
- Do not use Disabled as a substitute for form validation or user feedback.
- Provide an explanation when the reason for Disabled is not obvious.
- Do not invent unsupported loading, active, pressed, or other state variants.
- If processing feedback is needed, follow an existing GEMS component or approved UX Pattern.

## 6. Contextual Button Patterns

Follow the **equivalent official GEMS Page Sample or UX Pattern** when selecting hierarchy, placement, grouping, and order.

These examples describe approved contextual usage—not universal rules for every product.

| UI Context | Button Usage |
|---|---|
| Form actions | `Batal` — Secondary Gray; `Simpan` — Primary |
| Positive confirmation | `Batal` — Secondary Gray; `Konfirmasi` — Primary Green Solid, only where supported by the official GEMS pattern |
| Negative confirmation | `Batal` — Secondary Gray; `Konfirmasi` — Primary Red Solid, only where supported by the official GEMS pattern |
| Approval decision | `Tolak` — Red Solid; `Setujui` — Green Solid, as an approved two-solid-button exception |
| Page header | `Ekspor Data` — Secondary Gray; `Ubah Data Aset` — Primary |
| Table row | `Ubah Pesanan` — Secondary Color |
| Detail page | `Hapus` — Secondary Color Red Outline; `Edit Pesanan` — Secondary Gray |
| Active process | `Edit` — Secondary Gray; `Stop Charging` — Secondary Color Red Outline |
| Standalone utility | `Unduh Kode QR` — Secondary Gray |

### Contextual Rules

- Follow the action grouping, hierarchy, placement, and ordering shown in relevant GEMS references.
- A page or group does not always need a Primary button.
- Two solid decision buttons are allowed only for an explicitly supported GEMS pattern, such as the approval example above.
- Do not interpret red/green visual styling as authorization to change the product's approval process.
- Confirmation dialogs must reflect actual action consequences.
- Destructive actions must use the relevant GEMS confirmation or UX Pattern when required.
- Do not universally apply the same button combination to every page.
- Preserve the meaning of the actions while adapting labels and available actions to the product.

## 7. Placement, Grouping & Responsive Behavior

- Place buttons according to the relevant GEMS component, Page Sample, or UX Pattern.
- Keep the main action visually prominent within its action group.
- Group related actions; separate unrelated actions appropriately.
- Maintain GEMS spacing, alignment, and responsive behavior.
- Follow `spacing-radius.md` for surrounding layout spacing where applicable.
- Maintain consistent button alignment across similar pages.
- In tables, preserve compact row-action patterns without overcrowding cells.
- In forms and dialogs, preserve the official action order and hierarchy.
- In page headers, place actions according to the GEMS header pattern.
- Avoid adding redundant buttons when the same action already exists in the relevant workflow.
- On smaller screens, adapt the container or action layout using supported GEMS patterns without changing component styling.

## 8. Button Labels & Product Context

Every button MUST represent a real action supported by the product.

**Label rules:**
- Use concise, clear, action-oriented language.
- Follow terminology from the approved product requirements, modules, and business workflows.
- Match the actual operation and its consequences.
- Keep terminology consistent across screens.
- Differentiate primary actions from alternatives through meaning and hierarchy.

Examples:
- `Simpan Perubahan`
- `Buat Pesanan`
- `Kirim Pengajuan`
- `Hapus`
- `Batal`
- `Ekspor Data`
- `Unduh Kode QR`
- `Stop Charging`

**MUST NOT**
- Copy sample labels when unrelated to the product.
- Invent actions, permissions, or business workflows.
- Use unclear labels such as `OK` when a more meaningful action is needed.
- Add actions solely to fill empty interface space.
- Assign a high-priority visual style to an action that is not actually important.

Button availability must follow user roles, permissions, workflow status, and product requirements.

When essential business behavior is unknown and cannot be inferred safely, request human clarification.

## 9. Application Rules for Claude AI

When creating or modifying GEMS interfaces:

1. Understand the product module, user role, and supported actions.
2. Identify each action's purpose, priority, context, and consequences.
3. Select the existing **GEMS General Button** hierarchy and size.
4. Follow the relevant GEMS component, Page Sample, or UX Pattern for placement and grouping.
5. Apply official component properties, semantic colors, icons, and states.
6. Adapt labels and available actions to the product requirements.

These are implementation instructions—not a separate validation report. Do not generate an additional compliance checklist unless requested.

If the exact pattern is unavailable, select the closest officially supported General Button configuration without inventing variants. Request human approval if a new component, unsupported style, or unresolved business decision would otherwise be required.

## 10. Strict Button Rules

### MUST

- Use official GEMS **General Button**, never CCM.
- Preserve component references, hierarchy, sizes, colors, states, and icon configurations.
- Follow relevant GEMS component specifications and contextual patterns.
- Choose hierarchy based on actual action importance and consequences.
- Follow official GEMS Foundations for color, typography, spacing, and effects.
- Maintain accessible focus, disabled behavior, and understandable actions.
- Use product-specific labels and respect business permissions.
- Keep consistent action grouping and placement across related screens.

### MUST NOT

- Use, duplicate, recreate, or adapt **Button CCM**.
- Create custom button variants, colors, sizes, or states.
- Hardcode styling outside official GEMS components or tokens.
- Detach official GEMS Button instances without explicit authorization.
- Make all buttons Primary.
- Automatically make every `Edit` action Primary.
- Automatically make every destructive action solid red.
- Use Secondary Color for all supporting actions.
- Introduce unsupported icon sizes or placements.
- Remove keyboard-focus visibility.
- Allow disabled actions to execute.
- Invent actions or alter business workflows based on visual examples.
- Treat example button combinations as mandatory across all products.

**Fallback:** If no exact contextual pattern exists, use the closest existing **GEMS General Button** configuration based on action hierarchy and purpose. Never use CCM or create a custom button as a fallback.

