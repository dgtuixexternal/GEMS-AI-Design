
# GEMS Design System — Components / Background Overlay

> **MANDATORY:** All modal backdrops in GEMS UI MUST use the existing GEMS General Background Overlay component. This applies to Confirmation Modals, Form Modals, Dialogs, and other modal-based interactions requiring a backdrop. Never create custom overlays, manually apply opacity or blur, or use CCM-specific styling.

## 1. Sources & Priority

**Official Figma References**
- [GEMS Background Overlay](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3339-63265)
- [GEMS Components](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=12-1129)
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1105-7310)

**Priority Order**
1. **GEMS Background Overlay:** Official properties, variants, appearance, and component structure.
2. **GEMS Modal/Popup Components:** Determine the correct overlay usage and composition.
3. **GEMS Foundation:** Official colors, effects, spacing, and related styles.
4. **GEMS Page Samples & UX Patterns:** Reference for actual overlay usage in UI workflows.
5. **HSD/BRD:** Defines modal purpose, confirmation requirements, and interaction behavior.

Official GEMS components are the visual source of truth. Business behavior MUST follow HSD/BRD.

---

## 2. Purpose & Core Principles

Background Overlay is a visual layer placed between the underlying interface and modal content to establish focus, visual separation, and interaction context.

**Primary Purposes**
- Dim or visually separate background content.
- Direct attention toward the active Modal or Dialog.
- Support confirmation and form-based modal workflows.
- Establish consistent modal layering.
- Prevent unintended interaction with underlying content when modal behavior requires it.

**Core Rules**
- MUST use official GEMS Background Overlay for modal backdrops.
- MUST preserve the existing Figma component reference.
- MUST follow the overlay variant used by the relevant GEMS Modal or UX Pattern.
- MUST NOT manually create darkened rectangles, custom opacity layers, or blur effects.
- MUST NOT use overlay solely for decoration.
- MUST NOT use CCM-specific components, tokens, or effects.

---

## 3. Available Variants & Properties

### Official Properties

| Property | Available Values |
|---|---|
| `Type` | `Default`, `Gradient`, `Transparent` |
| `Background` | `True`, `False` |
| `Background blur` | `True`, `False` |

### Official Variant Combinations

| Type | Background | Background Blur |
|---|---|---|
| `Default` | `True` | `True` |
| `Default` | `True` | `False` |
| `Gradient` | `True` | `True` |
| `Gradient` | `True` | `False` |
| `Transparent` | `False` | `True` |
| `Transparent` | `False` | `False` |

Only these combinations are available in the referenced GEMS component.

**Rules**
- Select the existing variant directly from GEMS.
- Preserve its official opacity, gradient, fill, and blur properties.
- Do not manually substitute colors or effects.
- Do not create unsupported property combinations.
- Do not interpret `Background=False` as permission to remove required modal interaction behavior.
- Do not detach instances or recreate overlays using primitive shapes.

---

## 4. When to Use Background Overlay

Use Background Overlay whenever the selected GEMS modal pattern requires a backdrop.

### Required Usage

| UI Context | Overlay Usage |
|---|---|
| Confirmation Modal | Required according to GEMS modal pattern |
| Delete Confirmation | Required |
| Submit Confirmation | Required |
| Cancel / Discard Confirmation | Required |
| Form Modal | Required |
| Add Data Modal | Required |
| Edit Data Modal | Required |
| Detail Dialog | Required when modal-based |
| Warning / Decision Dialog | Required when modal-based |
| Other Modal Popup | Required when the official pattern uses a backdrop |

**Important:** The requirement is based on modal behavior, not the word "popup" alone.

### When NOT to Use

| UI Context | Rule |
|---|---|
| Tooltip | Do not add modal overlay |
| Dropdown Menu | Do not add modal overlay by default |
| Notification / Toast | Do not add modal overlay |
| Standard Alert | Do not add modal overlay |
| Badge | Do not add modal overlay |
| Standard Input | Do not add modal overlay |
| Ordinary Card | Do not add modal overlay |
| Nonmodal Popover | Follow its own GEMS component pattern |
| Full Page Form | No modal overlay unless another modal opens |

Do not turn ordinary interactive components into modal experiences by introducing Background Overlay.

---

## 5. Overlay Type Selection

### Default

Use `Type=Default` for standard modal backdrops when the relevant GEMS pattern specifies it.

**Typical Context**
- Confirmation Modal.
- Form Modal.
- Standard Dialog.
- Common modal interactions.

**Rules**
- Prefer the existing Default variant for standard modal patterns when supported by GEMS examples.
- Preserve the official visual appearance.
- Do not independently adjust darkness or opacity.

### Gradient

Use `Type=Gradient` only when the official GEMS component or relevant pattern requires gradient treatment.

**Rules**
- Follow the existing gradient definition.
- Do not create custom gradient colors, directions, or stops.
- Do not choose Gradient purely for visual decoration.

### Transparent

Use `Type=Transparent` only when the selected GEMS pattern specifically requires a transparent overlay treatment.

**Rules**
- Preserve the official Transparent variant.
- Do not assume Transparent is appropriate for all modal interactions.
- Do not replace Default with Transparent for aesthetic reasons.

---

## 6. Background Blur Usage

| Property | Meaning | Usage |
|---|---|---|
| `Background blur=True` | Applies official GEMS background blur treatment | When the selected overlay variant requires blur |
| `Background blur=False` | Uses the official variant without background blur | When the selected overlay variant does not require blur |

**Rules**
- Blur MUST follow the official GEMS variant.
- Do not independently add CSS blur, backdrop filters, or custom effects.
- Do not change blur strength to achieve a preferred visual appearance.
- Do not assume every modal requires blur.
- Follow the same overlay treatment for equivalent modal patterns.

---

## 7. Modal Composition & Layering

The modal composition MUST preserve the intended visual and interaction hierarchy.

**Layer Order**
1. Underlying page content.
2. Official GEMS Background Overlay.
3. Active Modal or Dialog content.

**Rules**
- Overlay MUST be visually behind the active modal.
- Overlay MUST cover the background region required by the modal pattern.
- Modal content MUST remain readable and interactive.
- Overlay MUST NOT obscure the active modal.
- Underlying page content MUST NOT remain unintentionally interactive during a blocking modal.
- Avoid multiple overlapping overlays for one active modal.
- Do not introduce arbitrary z-index values or custom layering behavior when existing GEMS patterns provide the composition.

### Multiple or Nested Modals

- Follow existing GEMS UX Patterns and product requirements.
- Do not automatically create an additional overlay for each nested layer.
- Do not invent modal stacking behavior.
- Request Human Approval when the required composition is not defined.

---

## 8. Usage in CRUD & UX Workflows

| Workflow | Modal Purpose | Overlay |
|---|---|---|
| Add Data | Show modal form | Use official GEMS overlay |
| Edit Data | Show modal form | Use official GEMS overlay |
| Delete Data | Confirm destructive action | Use official GEMS overlay |
| Submit Data | Confirm submission | Use official GEMS overlay |
| Cancel Changes | Confirm unsaved changes | Use official GEMS overlay |
| Discard Draft | Confirm discarding data | Use official GEMS overlay |
| Approve / Reject | Confirm decision when required | Use official GEMS overlay |
| View Detail | Show details in modal | Use official GEMS overlay |
| Full Page CRUD | No modal involved | Overlay not required |

**Usage Rules**
- Determine whether the workflow uses a modal or full page.
- When the workflow uses a GEMS modal with a backdrop, apply the official overlay.
- Do not invent a modal solely to introduce Background Overlay.
- Do not invent confirmation steps absent from HSD/BRD or product requirements.
- Follow the relevant GEMS Page Sample or UX Pattern for placement and composition.

---

## 9. Interaction & Dismiss Behavior

Background Overlay is a visual layer. It does not independently define the modal's business behavior.

### Opening

When a modal opens:
- Display the appropriate official Background Overlay.
- Keep the modal above the overlay.
- Apply focus behavior defined by the GEMS modal pattern.
- Restrict background interaction when the modal is blocking.

### Closing

When a modal closes:
- Remove or hide its associated overlay.
- Restore the underlying page's normal interaction state.
- Preserve relevant form data and workflow state according to requirements.

### Clicking Outside the Modal

- Do not assume clicking the overlay closes the modal.
- Follow the official modal behavior and HSD/BRD.
- For destructive confirmations, avoid accidental dismissal when explicit confirmation is required.
- For unsaved forms, follow the product's discard/close behavior.
- Overlay interaction MUST NOT independently execute actions or change business status.

### Escape & Keyboard

- Follow the official modal's keyboard behavior.
- Restore focus appropriately after closing.
- Do not allow background controls to receive focus when the active modal is blocking.
- Do not make the overlay itself an unnecessary keyboard-focusable element.

---

## 10. Responsive Behavior

- Use the GEMS overlay composition appropriate to the target screen.
- Preserve proper backdrop coverage on Desktop and Mobile.
- Follow responsive Modal components and Page Samples.
- Do not leave uncovered background areas when the selected pattern requires full backdrop coverage.
- Preserve modal visibility and accessibility across screen sizes.
- Do not create custom mobile overlay variants without GEMS support or Human Approval.

---

## 11. Foundation & Component Dependencies

Background Overlay MUST remain consistent with GEMS Foundation and modal component guidelines.

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | Official General color tokens and background treatment |
| `Foundation/effect-styles.md` | Official blur and effects |
| `Foundation/spacing-dan-radius.md` | Related modal layout, spacing, and radius |
| `Foundation/typography.md` | Typography of modal content |
| `Foundation/icons.md` | Modal controls and action icons |
| `Foundation/design-annotations.md` | Component specifications and annotations |

### Related Components

- **Modal / Dialog:** Defines modal structure and behavior.
- **Button:** Defines confirmation, cancel, and action controls.
- **Input / Dropdown:** Defines form controls within modal content.
- **Alert:** Used for relevant contextual information inside a modal when needed.
- **Notification:** Reports outcomes after actions, without automatically introducing another overlay.

**Cross-Component Rules**
- Overlay styling MUST come from the original GEMS Background Overlay instance.
- Modal styling MUST come from its own official GEMS component.
- Do not apply modal shadows, corner radii, or padding to the overlay itself unless specified.
- Do not manually combine multiple background fills or effects to imitate GEMS.

---

## 12. Strict AI Rules

### MUST

1. Use official **GEMS General Background Overlay** for modal backdrops.
2. Preserve the original Figma component reference.
3. Select supported Type, Background, and Background Blur combinations.
4. Follow the related GEMS Modal/Dialog component and UX Pattern.
5. Maintain correct layering between background, overlay, and active modal.
6. Preserve modal readability, interaction, and responsive behavior.
7. Follow HSD/BRD for opening, closing, confirmation, and dismissal behavior.
8. Request Human Approval for unsupported overlay compositions or interactions.

### MUST NOT

1. **Use CCM overlays, CCM variants, or CCM styling.**
2. Create custom overlay rectangles or duplicate overlay components.
3. Hardcode opacity, HEX/RGB/HSL, blur strength, or gradient values.
4. Invent unsupported variant combinations.
5. Add overlay to Tooltip, Dropdown, Notification, or standard nonmodal components.
6. Change official overlay colors or effects for visual preference.
7. Place overlay above active modal content.
8. Allow unintended interaction with blocked background content.
9. Assume overlay clicks always dismiss modals.
10. Make overlay dismissal execute destructive actions or alter business status.
11. Create unnecessary nested overlays.
12. Introduce unsupported responsive or interaction behavior without Human Approval.

---

## 13. AI Usage Decision

When designing a UI flow:

1. **Identify Interaction:** Determine whether the UI requires a modal, dialog, or nonmodal component.
2. **Determine Backdrop Need:** Check the selected official GEMS pattern.
3. **Use GEMS Overlay:** Apply the existing Background Overlay component when a backdrop is required.
4. **Select Variant:** Choose supported Type, Background, and Background Blur properties.
5. **Build Composition:** Place overlay between background content and active modal.
6. **Apply Behavior:** Follow modal interaction, dismissal, and focus requirements.
7. **Preserve Foundation:** Use original GEMS General styling without manual overrides.

**Fallback:** If the required backdrop type, composition, or interaction is not defined in GEMS, request Human Approval before introducing a new pattern.

> **FINAL INSTRUCTION:** Every GEMS modal-based Confirmation, Form Popup, or Dialog requiring a backdrop MUST use the original **GEMS General Background Overlay** component. Never recreate overlays manually, never use CCM, and never apply overlay to ordinary nonmodal components.
