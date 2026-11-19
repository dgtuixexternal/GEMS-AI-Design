
# GEMS Design System — Components / Modal

> **MANDATORY:** All Modals MUST use official GEMS General Modal components, supported variants, and approved action color semantics. Preserve original structure, typography, colors, spacing, effects, and interaction behavior. CCM Modals and CCM-specific patterns are strictly prohibited.

## 1. Sources & Priority

**Official References**
- [GEMS Modals](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-10652)
- [GEMS General Modal Variants](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-26550)
- [GEMS Modal Header](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-29010)
- [GEMS Modal Actions](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-28918)
- [GEMS Desktop Example](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-29006)
- [GEMS Mobile Example](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-29008)
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1105-7310)

**Priority Order**
1. **Approved GEMS Modal Rules:** Mandatory action color semantics and restrictions defined in this guideline.
2. **Official General Modal:** Source of truth for Type, Breakpoint, structure, dimensions, and visual properties.
3. **Modal Header & Actions:** Source of truth for supported header and action configurations.
4. **GEMS Components & Foundation:** Source of truth for nested components and tokens.
5. **Page Samples & UX Patterns:** Reference for contextual usage and interaction.
6. **HSD/BRD:** Defines business actions, consequences, fields, and permissions.
7. **General UI/UX Principles:** Fallback only when GEMS provides no specific guidance.

If approved action semantics require a configuration unavailable in the official component, request Human Approval. Do not invent unsupported variants.

**Component Restrictions**
- MUST use General Modal at node `240:26550`.
- MUST use official `_Modal header` and `_Modal actions` when applicable.
- MUST NOT use `Modals CCM`, CCM-specific variants, or CCM design patterns.
- MUST NOT recreate CCM layouts using General colors.
- Components located in the GEMS Figma file are not automatically approved for General products.

---

## 2. Purpose & Usage

Modal is a focused interface displayed above the current page to support a specific decision, task, or interaction without leaving the current context.

Official GEMS Modals support confirmations, forms, selections, verification, uploads, and other focused workflows.

### When to Use

| Context | Recommendation |
|---|---|
| Important confirmation | Use when explicit user consent is necessary |
| Delete / Reject | Use when the approved workflow requires confirmation |
| Unsaved changes | Warn before discarding changes |
| Approval / Revision | Use when required by HSD/BRD |
| Short contextual form | Use an appropriate official Form Modal |
| Additional required input | Use a supported input-based Modal |
| User selection / invitation | Use the corresponding official Type |
| Upload / image crop | Use the corresponding official Type |
| Verification | Use the corresponding official Type |
| Routine navigation | Do not use Modal |
| Simple feedback | Prefer Notification or Alert |
| Complex multi-step workflow | Prefer an approved dedicated page or UX Pattern |
| Every Save / Edit action | Do not automatically add confirmation |

**Usage Rules**
- MUST determine whether Modal is necessary based on action impact and workflow.
- MUST select an official Type matching the intended task.
- MUST preserve the user's current page context.
- MUST follow HSD/BRD for business actions and permissions.
- MUST NOT introduce unnecessary confirmation steps.
- MUST NOT use Modal as a replacement for a full page when the workflow requires extensive content.

**Core Principle:** Use Modal when focused interaction benefits the user. Not every action requires a confirmation dialog.

---

## 3. Available Modal Types

**Official Component:** `Modals`  
**Figma Node:** `240:26550`

### Verified Properties

| Property | Available Values |
|---|---|
| `Type` | Official values defined by the GEMS component set |
| `Breakpoint` | `Desktop`, `Mobile` |

### Available Type Categories

| Category | Official Type |
|---|---|
| Confirmation | `Horizontal` |
| Confirmation | `Warning horizontal` |
| Confirmation | `Destructive horizontal` |
| Confirmation | `Stacked left aligned` |
| Confirmation | `Warning stacked left aligned` |
| Confirmation | `Destructive stacked left aligned` |
| Input / Selection | `Checkboxes`, `Toggles`, `Dropdown`, `Input field`, `Text Area`, `Labels`, `Link field` |
| Access / Invitation | `Access request`, `Email invite`, `User invite` |
| Team Management | `Stacked with team`, `Stacked with team and link`, `Stacked with team and invites` |
| Authentication | `Log in`, `Sign up 01`, `Sign up 02`, `Verification code`, `2FA code`, `Password prompt` |
| Media | `Centered photo`, `Centered photo carousel`, `Centered video carousel`, `Image crop` |
| File / Form | `File upload`, `Form 01`, `Form 02` |
| Payment / Plan | `Payment method`, `Payment details`, `Payment details with image`, `Plan 01`, `Plan 02` |
| Other | `Date picker`, `Profile settings`, `User selection` |

### Type Selection Rules

- MUST select the official Type corresponding to the task.
- MUST use a supported Desktop or Mobile variant.
- MUST preserve the original internal component structure.
- MUST use official GEMS nested components.
- MUST NOT invent new Type names or unsupported variants.
- MUST NOT assume every Type is relevant to every product.
- MUST NOT use CCM-specific Modal Types.

**Important:** Positive, Warning, and Destructive describe action semantics. Technical Type names MUST follow the actual Figma component.

---

## 4. Mandatory Modal Action Colors

**MANDATORY:** Modal Primary Button colors MUST follow the approved GEMS action semantics.

### Action Color Matrix

| Action Type | Primary Button | Usage |
|---|---|---|
| General | **Red Solid** | Save, Submit, Confirm, Continue |
| Approval | **Green Solid** | Approve, Accept |
| Revision | **Orange Solid** | Request Revision |
| Rejection | **Red Solid** | Reject |
| Destructive | **Red Solid** | Delete, Remove |
| Warning | Based on final action | Exit, Cancel, Discard Changes |

### Strict Color Rules

**MUST**
- Use Red Solid as the default Primary Button for General actions.
- Use Green Solid exclusively for Approval actions.
- Use Orange Solid exclusively for Revision Request actions.
- Use Red Solid for Rejection and Destructive actions.
- Use official GEMS Button components and color tokens.
- Preserve official Button dimensions, states, and positioning.
- Match Status Icon semantics to the action context.
- Determine action classification from HSD/BRD.

**MUST NOT**
- Use Green Solid for Save, Submit, or general confirmation.
- Use Orange Solid for general confirmation or unrelated warning actions.
- Use Green Solid for Reject or Delete.
- Assume Warning automatically requires Orange Solid.
- Change Button color solely because the Status Icon has a specific color.
- Create custom Button colors or override official GEMS tokens.
- Use CCM Button variants.

### Status Icon vs. Primary Button

Status Icons and Primary Buttons serve different purposes.

| Context | Status Icon | Primary Button |
|---|---|---|
| Positive General | Official positive semantic icon | Red Solid |
| Approval | Official positive semantic icon | Green Solid |
| Warning | Official warning semantic icon | According to final action |
| Revision | Official warning/revision semantic icon | Orange Solid |
| Rejection | Official rejection/destructive semantic icon | Red Solid |
| Delete | Official destructive semantic icon | Red Solid |

Status Icon visuals MUST follow the selected official GEMS Modal pattern.

**Fallback:** If the required color configuration is unavailable in the official component, request Human Approval before creating or modifying a variant.

---

## 5. Confirmation Modal Selection

Select the confirmation pattern according to the action's meaning and consequences.

### Confirmation Matrix

| Pattern | When to Use | Example |
|---|---|---|
| Positive General | Meaningful positive action requiring confirmation | Save, Submit |
| Approval | Approving a request or decision | Approve |
| Warning | Potential loss of changes or consequential interruption | Exit unsaved form |
| Revision | Requesting changes or correction | Request Revision |
| Rejection | Rejecting a request or report | Reject |
| Destructive | Removing or deleting data | Delete |
| Confirmation with Input | Decision requires additional information | Reject with Reason |

### Selection Rules

- MUST classify the action before selecting its visual pattern.
- MUST use the corresponding official General Modal Type.
- MUST apply the approved Primary Button color rules.
- MUST use official Status Icons and semantic colors.
- MUST explain relevant consequences.
- MUST NOT create a new Modal variant for each business action.
- MUST NOT introduce confirmation when the action does not require it.

### Confirmation Necessity

Consider:
1. Is the action reversible?
2. Does it affect important data or other users?
3. Could users lose unsaved changes?
4. Does the business workflow require explicit consent?
5. Is an official GEMS confirmation pattern available?

Routine, easily reversible actions SHOULD NOT receive unnecessary confirmation.

---

## 6. Modal Header

**Official Component:** `_Modal header`  
**Figma Node:** `240:29010`

### Available Properties

| Property | Available Values |
|---|---|
| `Type` | `Left aligned`, `Center aligned`, `Horizontal left aligned` |
| `Breakpoint` | `Desktop`, `Mobile` |

### Official Configurations

| Type | Desktop | Mobile |
|---|---|---|
| `Left aligned` | Available | Available |
| `Center aligned` | Available | Available |
| `Horizontal left aligned` | Available | Available |

### Header Anatomy

Depending on the official Type, the header may contain:

- Status / Featured Icon.
- Decorative icon background.
- Modal Title.
- Supporting Description.
- Close Button.

### Header Rules

- MUST use the Header configuration supported by the selected Modal.
- MUST preserve official icon placement, alignment, spacing, and typography.
- MUST use official GEMS Icons or Featured Icons.
- MUST use a clear title matching the intended action.
- MUST provide supporting descriptions when relevant.
- MUST preserve Close Button placement and supported behavior.
- MUST NOT manually reposition icons or decorative elements.
- MUST NOT invent custom Header layouts.
- MUST NOT assume every Header Type uses the same structure.

---

## 7. Modal Actions

**Official Component:** `_Modal actions`  
**Figma Node:** `240:28918`

### Available Properties

| Property | Available Values |
|---|---|
| `Type` | `Horizontal fill container`, `Vertical fill container`, `Horizontal right aligned (checkbox)` |
| `Destructive` | `True`, `False` |
| `Breakpoint` | `Desktop`, `Mobile` |

The component provides **12 official configurations**.

### Action Selection

| Condition | Selection |
|---|---|
| Standard action | `Destructive=False` |
| Destructive action | `Destructive=True` |
| Horizontal layout | `Horizontal fill container` |
| Vertical layout | `Vertical fill container` |
| Supported checkbox option | `Horizontal right aligned (checkbox)` |

### Action Rules

- MUST use official GEMS Buttons.
- MUST apply approved Modal Action Color Rules.
- MUST preserve official Button order, sizes, spacing, and alignment.
- MUST select `Destructive=True` only for genuinely destructive behavior.
- MUST use approved Mobile action configurations.
- MUST use action labels consistent with the Modal content.
- MUST provide appropriate Cancel or Return actions when required.

**MUST NOT**
- Invent new action arrangements.
- Reverse Button order without an approved pattern.
- Add optional checkboxes without a business requirement.
- Add "Don't show again" to consequential or destructive confirmations without approval.
- Trigger confirmation actions before the user confirms.

**Important:** Rejection uses Red Solid according to the approved color semantics, but the `Destructive` property MUST still follow the actual behavior and supported configuration of the selected Modal. Do not infer component properties from Button color alone.

---

## 8. Confirmation with Input

Use a Modal with Input when the action requires additional information.

### Input Usage Matrix

| Context | Input | Required |
|---|---|---|
| Approval with Note | Catatan Persetujuan | According to HSD/BRD |
| Rejection with Reason | Alasan Penolakan | According to HSD/BRD |
| Revision with Reason | Alasan Revisi | According to HSD/BRD |
| Additional Confirmation Data | Relevant field | According to HSD/BRD |

### Input Rules

- MUST use an official Modal Type supporting the required input.
- MUST use official GEMS Input, Textarea, Dropdown, or other supported controls.
- MUST provide clear labels and relevant helper text.
- MUST follow HSD/BRD for required indicators.
- MUST apply official validation and error states.
- MUST preserve entered values when validation fails.
- MUST prevent submission of invalid required information.
- MUST preserve official Modal layout and spacing.

**MUST NOT**
- Add input without a defined business requirement.
- Make all approval or rejection notes mandatory automatically.
- Invent unsupported field layouts.
- Submit incomplete required information.
- Create a custom Form Modal when an official component can meet the requirement.

If no supported Modal Type can accommodate the required input, request Human Approval.

---

## 9. Contextual Modal Patterns & UX Writing

These examples define contextual content and approved action colors. They are not additional Figma variants.

### Usage Matrix

| Context | Suggested Title | Secondary Action | Primary Action | Primary Color |
|---|---|---|---|---|
| Save Data | Simpan Data? | Batal | Ya, Simpan | Red Solid |
| Submit Request | Konfirmasi Pengajuan? | Kembali | Ya, Ajukan | Red Solid |
| General Confirmation | Konfirmasi Tindakan? | Batal | Ya, Konfirmasi | Red Solid |
| Approval | Konfirmasi Persetujuan | Batal | Ya, Setujui | Green Solid |
| Approval with Note | Konfirmasi Persetujuan | Batal | Ya, Setujui | Green Solid |
| Revision | Konfirmasi Revisi | Batal | Ya, Minta Revisi | Orange Solid |
| Revision with Reason | Konfirmasi Permintaan Revisi | Batal | Ya, Minta Revisi | Orange Solid |
| Rejection | Konfirmasi Penolakan | Batal | Ya, Tolak | Red Solid |
| Rejection with Reason | Konfirmasi Penolakan | Batal | Ya, Tolak | Red Solid |
| Delete Data | Konfirmasi Hapus | Batal | Ya, Hapus | Red Solid |
| Exit Unsaved Form | Keluar dari Halaman? | Kembali | Ya, Keluar | Based on approved action |
| Discard Changes | Buang Perubahan? | Kembali | Ya, Buang | Based on approved action |

### Contextual Rules

**Save / Submit**
- Confirm only when required.
- Explain the result of saving or submitting.
- Do not use Green Solid.

**Approval**
- Use Green Solid.
- Explain the approval target and consequence.
- Add approval notes only when required.

**Revision**
- Use Orange Solid.
- Distinguish revision from rejection.
- Require a reason only when specified.

**Rejection**
- Use Red Solid.
- Explain the effect of rejection.
- Use required reason fields only when specified.

**Delete**
- Use Red Solid.
- Identify the affected data when useful.
- Explain whether deletion is permanent or recoverable.
- Never delete before valid confirmation.

**Exit / Discard Changes**
- Explain potential data loss.
- Preserve data if the user chooses to continue editing.
- Select Button semantics according to the actual final action.

### UX Writing Rules

- MUST use clear, action-oriented labels.
- MUST use terminology consistent with HSD/BRD.
- MUST maintain consistency between Title, Description, and Primary Button.
- MUST explain important consequences.
- SHOULD keep wording concise.
- MUST NOT use ambiguous confirmation labels.
- MUST NOT copy sample wording if it contradicts product behavior.
- MUST NOT invent approval, rejection, or revision workflows absent from the product.

---

## 10. Modal Structure & Anatomy

A Modal may contain the following elements depending on its official Type.

| Element | Usage |
|---|---|
| Background Overlay | Separates Modal from the underlying page |
| Modal Container | Holds the official Modal composition |
| Modal Header | Icon, Title, Description, and supported Close Button |
| Content Area | Message, Form, Input, Selection, or supported content |
| Modal Actions | Primary and supporting actions |
| Validation / Feedback | Relevant errors, loading, and result feedback |

### Structure Rules

- MUST preserve the selected official Modal composition.
- MUST use official container dimensions, radius, background, and effects.
- MUST preserve original padding, spacing, and alignment.
- MUST use official GEMS nested components.
- MUST NOT rebuild internal structures manually.
- MUST NOT add unrelated decorative elements.
- MUST NOT change container dimensions outside supported properties.

### Background Overlay

- MUST use the official GEMS Background Overlay component.
- MUST follow `bg-overlay.md`.
- MUST preserve official color, opacity, and layering.
- MUST display the overlay while Modal is active.
- MUST remove the overlay after Modal closes.
- MUST NOT hardcode custom overlay styling.

---

## 11. Modal States & Interaction

Functional states MUST follow the visual behavior of official GEMS components.

| State | Expected Behavior |
|---|---|
| Closed | Modal and overlay are hidden |
| Open | Modal and overlay appear |
| Focused | Keyboard focus is visible and managed |
| Processing | Submission is in progress; repeated actions are prevented |
| Validation Error | Field errors appear; entered data is preserved |
| Request Error | Failure feedback appears without false success |
| Completed | Approved success flow is executed |

### Interaction Rules

**Open**
- Open from a valid user action or approved workflow event.
- Display official Modal and Background Overlay.
- Preserve the underlying page state.

**Close / Cancel**
- Follow the approved dismissal behavior.
- Do not allow dismissal to bypass required confirmation or cause unintended data loss.
- Preserve unsaved data when users choose to continue editing.
- Remove the overlay when Modal closes.

**Processing**
- Prevent duplicate submissions.
- Use official loading states where supported.
- Do not display success before the operation completes.

**Validation Error**
- Display official field-level feedback.
- Preserve entered values.
- Keep the Modal available for correction.

**Request Error**
- Display appropriate failure feedback.
- Preserve information needed for retry.
- Do not execute success behavior.

**Completed**
- Follow HSD/BRD for closing, navigation, data updates, and feedback.
- Use official Notification or Alert components when appropriate.
- Do not automatically create an additional Success Modal.

---

## 12. Desktop & Mobile

### Desktop

- MUST use `Breakpoint=Desktop`.
- MUST preserve official dimensions and layout.
- MUST use compatible Desktop Header and Actions variants.
- MUST maintain readable content and accessible controls.

### Mobile

- MUST use `Breakpoint=Mobile`.
- MUST preserve the official mobile composition.
- MUST use compatible Mobile Header and Actions variants.
- MUST maintain accessible controls and readable text.
- MUST follow supported scrolling behavior for longer content.

### Responsive Restrictions

- MUST NOT manually shrink Desktop variants to simulate Mobile.
- MUST NOT invent breakpoints or custom responsive layouts.
- MUST NOT remove required fields or actions.
- MUST NOT introduce unsupported fullscreen, drawer, or bottom-sheet patterns.
- Request Human Approval if the required responsive behavior is unavailable.

---

## 13. Accessibility

All Modals MUST:

- Use appropriate dialog semantics.
- Provide an accessible title and description.
- Move keyboard focus into the active dialog.
- Maintain visible focus indicators.
- Manage keyboard focus within the active Modal appropriately.
- Restore focus to the triggering control after dismissal when possible.
- Provide accessible labels for Close and icon-only actions.
- Support keyboard operation of nested controls.
- Communicate required fields and validation errors accessibly.
- Maintain adequate contrast through official GEMS tokens.
- Avoid relying solely on icon or Button colors to communicate meaning.
- Follow the project's accessibility requirements.

---

## 14. Foundation & Component Dependencies

Modal MUST follow the existing GEMS guidelines.

### Foundation

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | General brand and semantic colors |
| `Foundation/typography.md` | Official GEMS Figma Text Styles |
| `Foundation/spacing-dan-radius.md` | Spacing, dimensions, and radius |
| `Foundation/effect-styles.md` | Shadows, borders, and effects |
| `Foundation/icons.md` | Standard icons and official sizes |
| `Foundation/misc-icons.md` | Featured Icons and special-purpose visuals |
| `Foundation/design-annotations.md` | Relevant layout and implementation annotations |

### Related Components

Follow corresponding GEMS guidelines when applicable:

- `button.md`
- `input.md`
- `dropdown.md`
- `tooltip.md`
- `alert.md`
- `notification.md`
- `bg-overlay.md`
- Other official Form and Selection components

Use the repository's actual filenames if different.

### Dependency Rules

- MUST use official GEMS General and semantic color tokens.
- MUST follow the approved Modal Action Color Rules in Section 4.
- MUST preserve existing GEMS Text Styles.
- MUST use official spacing, radius, and effect tokens.
- MUST preserve original icon sizes and nested component variants.
- MUST maintain reusable component references where supported.
- MUST NOT hardcode HEX/RGB/HSL or unsupported typography, spacing, or effects.
- MUST NOT introduce CCM components, tokens, or patterns.

---

## 15. Strict Rules

### MUST

- Use official GEMS General Modal components.
- Select an existing Type matching the intended task.
- Use supported Desktop or Mobile variants.
- Use official Modal Header and Actions configurations.
- Apply approved Modal Primary Button color semantics.
- Determine whether confirmation is necessary.
- Match content and interaction to actual business requirements.
- Preserve original component structure and visual properties.
- Use official GEMS nested components and Background Overlay.
- Follow HSD/BRD, Page Samples, and UX Patterns.
- Respect user permissions, required inputs, and validation behavior.

### MUST NOT

- Use `Modals CCM` or CCM-specific patterns.
- Create custom Modal Types or unsupported variants.
- Recreate official components with manually detached frames.
- Modify original dimensions, typography, spacing, radius, or effects.
- Use Green Solid outside Approval.
- Use Orange Solid outside Revision Request.
- Use non-approved Primary Button colors.
- Invent custom icons or decorative elements.
- Automatically add confirmation to every action.
- Introduce unapproved business workflows.
- Add or require fields without business justification.
- Submit invalid data or bypass mandatory confirmation.
- Delete or discard data before valid confirmation.
- Invent unsupported responsive layouts.
- Duplicate unnecessary success or confirmation dialogs.
- Remove keyboard support or focus indicators.
- Modify business behavior solely to match a visual example.

---

## 16. AI Implementation Instructions

When generating a Modal:

1. **Identify Task:** Determine the action, its consequences, and whether Modal is necessary.
2. **Select Official Type:** Use an appropriate General Modal Type at node `240:26550`; exclude CCM.
3. **Select Breakpoint:** Use the official Desktop or Mobile variant.
4. **Configure Structure:** Preserve the matching Modal Header, Content, and Actions.
5. **Apply Action Semantics:** Use the mandatory Red/Green/Orange Solid rules.
6. **Configure Content:** Use product-specific Title, Description, Input, and Button labels from HSD/BRD.
7. **Apply Behavior:** Follow official focus, validation, processing, error, and success patterns.
8. **Apply GEMS Dependencies:** Use official Background Overlay, Foundation tokens, and nested components.

**Human Approval Required When:**
- No official Modal Type supports the required task.
- The required content cannot fit an approved composition.
- The mandatory action color is unavailable in the selected official component.
- Required responsive or interaction behavior is unsupported.
- Product requirements conflict with official GEMS specifications.

Combine related clarification questions into one confirmation whenever possible.

If an official component or property cannot be accessed or verified, request the necessary Figma access or specifications. Do not invent unsupported details.

---

## Final Instruction

**AI MUST use official GEMS General Modal components, select the correct Type and Breakpoint, preserve the original structure, and adapt content and behavior to approved product requirements.**

**Mandatory Primary Button Colors:**
- **Red Solid:** General, Save, Submit, Confirm, Reject, Delete.
- **Green Solid:** Approval only.
- **Orange Solid:** Revision Request only.

**Status Icon colors MUST follow their official semantic purpose and MUST NOT automatically determine Primary Button colors.**

**Not every action requires a Modal, and not every Modal is a Confirmation Modal.**

**CCM Modals, custom variants, unsupported visual properties, and invented business workflows are strictly prohibited.**

**GEMS Design System is the single source of truth for Modal visual specifications and supported interaction behavior.**
