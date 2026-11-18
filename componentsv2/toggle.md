
# GEMS Design System — Components / Toggle

> **MANDATORY:** All Toggle controls MUST use official GEMS General Toggle components from the connected Figma Design System. Preserve original component references, supported variants, sizes, states, colors, typography, spacing, and interaction behavior. **CCM components and CCM-derived styling are strictly prohibited.**

## 1. Purpose & Core Principles

Toggle is a binary switch used to enable or disable a setting, feature, preference, visibility condition, or supported data status.

Examples:
- Aktif / Nonaktif
- On / Off
- Tampilkan / Sembunyikan
- Enabled / Disabled as a business setting

**Core Principle:**

> Use Toggle to represent a persistent binary value—not to execute a one-time action.

### 1.1 Core Rules

- Toggle MUST represent the actual binary value.
- Usage and behavior MUST follow HSD/BRD.
- Selection MUST consider business consequences and permissions.
- Save behavior MUST follow the approved workflow.
- Visual styling MUST follow official GEMS General components.
- Not every two-option requirement should use Toggle.

### 1.2 Source Priority

1. **GEMS General Toggle:** Component properties, variants, sizes, and states.
2. **GEMS Page Samples & UX Patterns:** Contextual placement and behavior.
3. **Product HSD/BRD:** Binary values, permissions, validation, and workflows.
4. **Approved Product Designs:** Supplementary implementation examples.
5. **General UI/UX Principles:** Fallback when no specific GEMS guidance exists.

GEMS defines component design. HSD/BRD defines business behavior.

Read only relevant GEMS references for the requested screen.

## 2. When to Use Toggle

### 2.1 Recommended Usage

| Context | When to Use | Example |
|---|---|---|
| Settings | Enable/disable a preference | Aktifkan Notifikasi |
| Feature Configuration | Enable/disable a supported feature | Aktifkan Pengingat |
| Visibility Settings | Show/hide a supported element | Tampilkan Informasi Tambahan |
| System Configuration | Enable/disable a configuration | Aktifkan Integrasi |
| Form Settings | Enter a binary setting within a form | Aktifkan Pengingat Otomatis |
| Table Row Settings | Change a binary value for one record | Aktifkan Konfigurasi |
| Data Activation | Set active/inactive record status | Status Aktif |

These examples illustrate suitable patterns; actual features and permissions MUST come from product requirements.

### 2.2 When NOT to Use Toggle

| Requirement | Correct Component | Reason |
|---|---|---|
| Simpan Data | Button | One-time action |
| Hapus Data | Button | Destructive action |
| Kirim Pengajuan | Button | Submission |
| Konfirmasi | Button / Modal | Explicit confirmation |
| Pilih beberapa item | Checkbox | Multi-selection |
| Pilih satu dari beberapa opsi | Radio Button / Dropdown | Selection between options |
| Pertanyaan Ya/Tidak | Radio / approved control | Explicit answer, not necessarily a setting |
| Setujui / Tolak | Button / Approval Pattern | Workflow decision |
| Status proses bertahap | Product-defined control | Requires business transitions |

### 2.3 Selection Rules

- Use Toggle only for appropriate binary conditions.
- Ensure users understand the setting being changed.
- Use Toggle for active/inactive data status only when the product establishes that pattern.
- Do not replace Save, Delete, Submit, or Approval actions with Toggle.
- Do not convert workflow status into Toggle without approved requirements.

## 3. Toggle Component Structure

GEMS provides two related components:

| Component | Purpose |
|---|---|
| `Toggle` | Complete switch, optionally including supporting text |
| `_Toggle base` | Base switch without the `Text` property |

### 3.1 Available Properties

| Property | Official Values | Purpose |
|---|---|---|
| `Pressed` | `True`, `False` | Binary value |
| `Size` | `xs`, `sm`, `md` | Switch size |
| `Text` | `True`, `False` | Supporting text visibility |
| `State` | `Default`, `Hover`, `Focus`, `Disabled` | Interaction state |

### 3.2 Property Rules

- `Pressed` determines the On/Off value.
- `State` determines the interaction condition.
- `Size` determines the official switch dimensions.
- `Text` applies to the complete Toggle component.
- `_Toggle base` does not provide `Text`.
- The official state is named `Focus`, NOT `Focused`.
- Do not rename `Pressed` to `Checked` in Figma variant documentation.
- Use only property combinations supported by the original component.

## 4. Toggle Variants & Sizes

### 4.1 Available Sizes

| Size | Switch Dimensions | Context |
|---|---|---|
| `xs` | 32 × 16 px | Compact controls without integrated text |
| `sm` | 36 × 20 px | Compact settings or table rows |
| `md` | 44 × 24 px | Standard forms and settings |

Dimensions refer to the switch itself, not the full interactive area.

### 4.2 Text Variants

| Text | Supported Sizes | Usage |
|---|---|---|
| `False` | `xs`, `sm`, `md` | Label provided separately |
| `True` | `sm`, `md` | Supporting text within component |

`Size=xs, Text=True` is not an identified official combination.

### 4.3 Size & Variant Rules

- Use only official `xs`, `sm`, or `md` sizes.
- Preserve original switch dimensions and proportions.
- Use only supported `Size` and `Text` combinations.
- Maintain consistent size among equivalent settings.
- Follow GEMS Page Samples and UX Patterns for contextual sizing.
- Preserve adequate interaction usability for compact sizes.
- Do not invent custom sizes, spacing, or switch geometry.

## 5. Toggle Pressed Conditions

`Pressed` represents the current binary value.

### 5.1 Pressed Matrix

| Pressed | Meaning | Visual |
|---|---|---|
| `False` | Off / Nonaktif | Official GEMS Off appearance |
| `True` | On / Aktif | Official GEMS On appearance |

### 5.2 Pressed=False

- Represents the inactive binary value.
- MUST show the official GEMS Off appearance.
- MUST reflect actual product data.
- MUST NOT be interpreted as Disabled.

### 5.3 Pressed=True

- Represents the active binary value.
- MUST show the official GEMS On appearance.
- MUST reflect actual product data.
- MUST NOT be interpreted as Hover or Focus.

### 5.4 Pressed vs State

| Pressed | State | Meaning |
|---|---|---|
| False | Default | Off, interactive |
| True | Default | On, interactive |
| False | Hover | Off, hovered |
| True | Hover | On, hovered |
| False | Focus | Off, focused |
| True | Focus | On, focused |
| False | Disabled | Off, non-interactive |
| True | Disabled | On, non-interactive |

**Important:** Disabled does not change the stored binary value. A disabled Toggle may remain visually On or Off.

## 6. Toggle States & Behavior

### 6.1 State Matrix

| State | Trigger | Behavior | Editable |
|---|---|---|---|
| `Default` | Normal condition | Official default styling | Yes |
| `Hover` | Pointer hover | Official hover styling | Yes |
| `Focus` | Keyboard or equivalent focus | Visible focus indicator | Yes |
| `Disabled` | Interaction prohibited | Official disabled styling | No |

### 6.2 Default

- Display the current `Pressed` value.
- Allow supported pointer and keyboard activation.
- Do not permanently display Hover or Focus styling.

### 6.3 Hover

- Use the official GEMS Hover variant.
- Preserve `Pressed` until activation.
- Return to the appropriate state when the pointer leaves.
- Do not treat Hover as a value change.

### 6.4 Focus

- Use the official `State=Focus` variant.
- Preserve a visible focus indicator.
- Support keyboard activation.
- Do not change `Pressed` merely because focus is received.
- Do not rename the Figma state to `Focused`.

### 6.5 Disabled

Use when permissions, prerequisites, feature availability, or workflow status prevent changes.

- Use the official Disabled variant.
- Prevent pointer and keyboard changes.
- Preserve the actual `Pressed` value.
- Explain the restriction when its reason is unclear.
- Follow product access rules for whether the control is shown disabled or hidden.
- Do not use Disabled as a validation-error indicator.

## 7. Toggle Interaction Behavior

### 7.1 Basic Interaction

| User Interaction | Expected Behavior |
|---|---|
| Activate Off Toggle | Changes toward On if permitted |
| Activate On Toggle | Changes toward Off if permitted |
| Hover | Visual change only |
| Focus | Focus indicator only |
| Keyboard activation | Changes value if enabled |
| Activate Disabled Toggle | No value change |

### 7.2 Save Behavior

Two patterns are possible:

| Pattern | Behavior | Requirement |
|---|---|---|
| Immediate Update | Change is processed immediately | HSD/BRD explicitly defines immediate saving |
| Form Submission | Value is updated in the form, then saved through Button | HSD/BRD defines form submission |

**Rules**
- Follow the product's approved save mechanism.
- Do not assume all Toggles auto-save.
- Do not add a Save button to an immediate-update pattern without requirements.
- Do not remove a required Save button from a form.
- Preserve existing values if saving fails, according to the approved error-handling pattern.
- Provide appropriate feedback for unsuccessful changes.

### 7.3 Initial Value

- Use the existing stored value or an explicitly approved default.
- Do not set all Toggles to Off automatically.
- Preserve saved values across reloads when supported by the system.
- Do not change business data without an authorized user action or system rule.

### 7.4 Pending & Failure Behavior

- Follow relevant GEMS loading, notification, and error UX Patterns.
- Prevent duplicate or conflicting updates where required.
- Keep the displayed value consistent with the confirmed system state.
- If a save fails, restore or retain the appropriate value according to product behavior.
- Do not invent a Toggle loading variant or temporary state.
- Do not silently imply that an unsuccessful change was saved.

## 8. Toggle vs Other Components

| User Requirement | Correct Component |
|---|---|
| Aktifkan Notifikasi | Toggle |
| Aktifkan Status Data | Toggle, if approved |
| Pilih beberapa kategori | Checkbox |
| Pilih satu lokasi | Dropdown |
| Jawaban Ya/Tidak | Radio or approved form control |
| Simpan Perubahan | Button |
| Hapus Data | Button |
| Setujui Pengajuan | Button |
| Ubah status workflow | Control specified by HSD/BRD |

**Decision Rule:** A binary choice is not automatically a Toggle. Distinguish persistent settings from form answers, selections, and workflow actions.

## 9. Contextual Toggle Patterns

### 9.1 Notification Settings

| Property | Usage |
|---|---|
| Label | Aktifkan Notifikasi |
| Size | `sm` / `md` |
| Text | True |
| Pressed | Actual saved value |
| State | Default or applicable interaction state |

**Behavior:** Enables or disables notifications according to product requirements.

### 9.2 Feature Configuration

| Property | Usage |
|---|---|
| Label | Aktifkan Fitur |
| Size | `md` |
| Text | True |
| Pressed | Actual feature value |
| State | Default / Disabled |

**Behavior:** Changes feature availability when the user has permission.

### 9.3 Table Row Settings

| Property | Usage |
|---|---|
| Context | Per-record binary setting |
| Size | `xs` / `sm` |
| Text | False |
| Pressed | Actual record value |
| State | Default / Disabled |

**Rules**
- Follow GEMS Table layout and sizing.
- Ensure the controlled record is identifiable.
- Do not change complex workflow statuses through Toggle without explicit requirements.
- Do not replace ordinary row CRUD actions with Toggle.

### 9.4 Visibility Settings

| Property | Usage |
|---|---|
| Label | Tampilkan Informasi Tambahan |
| Size | `sm` / `md` |
| Text | True |
| Pressed | Actual visibility value |
| State | Default |

**Behavior:** Controls visibility according to the approved interaction.

### 9.5 Disabled Settings

| Property | Usage |
|---|---|
| Label | Aktifkan Integrasi |
| Size | `sm` / `md` |
| Text | True |
| Pressed | Actual value |
| State | Disabled |

**Behavior:** Displays the current value without allowing changes.

### 9.6 Data Activation Status

Use Toggle for active/inactive record status only when the product requirements or approved design establish that interaction.

**Example:** ISS Registrasi Asset — Status Aktif.

| Property | Usage |
|---|---|
| Field Label | Status |
| Toggle Label | Status Aktif |
| Pressed=True | Record is active |
| Pressed=False | Record is inactive |
| Size | Official supported variant |
| State | Applicable official state |
| Save Behavior | According to HSD/BRD |

**Rules**
- Distinguish data activation from workflow status.
- Preserve the initial value from record data.
- Follow the approved save mechanism.
- Respect user-role permissions.
- Do not assume that changing the switch immediately saves the record.
- Do not convert multi-stage workflow status into an active/inactive Toggle.

### 9.7 CRUD & Empty States

**Create**
- Toggle may define a supported binary field within a create form.
- Initial value must follow HSD/BRD.
- Saving follows the approved create workflow.

**Read / Detail**
- Show the actual setting value.
- Use the appropriate GEMS display or disabled-control pattern.
- Do not use a Disabled Toggle as the universal read-only representation.

**Update**
- Allow changes only when authorized.
- Follow immediate-update or form-submission requirements.

**Delete**
- Use GEMS Button and confirmation patterns.
- Toggle is not a substitute for Delete.

**Empty State**
- Follow the official GEMS Empty State component or UX Pattern.
- Do not add Toggles for nonexistent records.
- Do not fabricate settings or default records.

## 10. Labels & Supporting Text

### 10.1 Label Rules

- Use concise, meaningful labels.
- Identify the setting or object controlled.
- Follow approved HSD/BRD terminology.
- Maintain consistency across equivalent screens.
- Do not use ambiguous labels without supporting context.

### 10.2 Label Examples

| Context | Example |
|---|---|
| Notification | Aktifkan Notifikasi |
| Feature | Aktifkan Fitur |
| Visibility | Tampilkan Informasi Tambahan |
| Reminder | Aktifkan Pengingat |
| Integration | Aktifkan Integrasi |
| Data Activation | Status Aktif |

### 10.3 Supporting Description

Use supporting text when users need to understand the consequences of a change.

| Label | Example Description |
|---|---|
| Aktifkan Notifikasi | Terima pemberitahuan ketika terdapat pembaruan data. |
| Aktifkan Pengingat | Tampilkan pengingat untuk jadwal yang akan datang. |
| Status Aktif | Tentukan apakah data dapat digunakan sesuai aturan sistem. |

Examples are illustrative. Actual wording MUST reflect product behavior.

## 11. Accessibility & Foundation Rules

### 11.1 Accessibility

- Provide a clear label or accessible name.
- Make On/Off understandable without relying solely on color.
- Preserve visible Focus styling.
- Support appropriate keyboard activation.
- Prevent changes when Disabled.
- Maintain usable interaction areas, including for `xs`.
- Expose the binary state to assistive technology.
- Explain significant consequences when necessary.

### 11.2 Foundation Integration

All Toggle visuals MUST follow these repository guidelines:

| Foundation | Usage |
|---|---|
| `Foundation/color.md` | Official GEMS General semantic colors |
| `Foundation/typography.md` | Official Text Styles |
| `Foundation/spacing-dan-radius.md` | Spacing, layout, and radius |
| `Foundation/effect-styles.md` | Official effects when specified |
| `Foundation/icons.md` | General icons when applicable |
| `Foundation/design-annotations.md` | Additional approved design specifications |

**Rules**
- Preserve original component color, spacing, radius, and dimensions.
- Apply complete official Text Styles when using labels and descriptions.
- Do not add custom effects or decorative shadows.
- Do not hardcode HEX, RGB, HSL, unsupported typography, or spacing.
- Do not modify internal component styling to fit a layout.
- Use GEMS Page Samples and UX Patterns for contextual placement.

## 12. AI Toggle Selection Workflow

When implementing a Toggle:

1. **Read HSD/BRD:** Identify the binary value, business meaning, permissions, and save mechanism.
2. **Check Suitability:** Distinguish a persistent setting from Button, Checkbox, Radio, or Dropdown interactions.
3. **Select Component:** Use official GEMS General Toggle.
4. **Apply Properties:** Choose supported `Size`, `Text`, `Pressed`, and `State`.
5. **Apply Content:** Use the approved label and supporting description.
6. **Apply Behavior:** Follow actual values, permissions, saving, and failure handling.
7. **Follow Context:** Use relevant GEMS Components, Page Samples, and UX Patterns.
8. **Resolve Exceptions:** Request Human Approval before introducing unsupported components or business behavior.

These are implementation instructions—not a separate validation report.

## 13. Strict AI Restrictions

### MUST

- Use official GEMS General Toggle components.
- Preserve original Figma component references and supported properties.
- Use actual product data for `Pressed`.
- Apply only official `xs`, `sm`, or `md` sizes.
- Use supported `Text` combinations.
- Preserve `State=Focus` naming.
- Follow GEMS Foundation and contextual patterns.
- Respect business permissions and save behavior.
- Maintain accessible labels and interaction states.

### MUST NOT

- Use Toggle CCM or CCM-derived styling.
- Create unsupported Toggle variants or sizes.
- Use `Size=xs, Text=True` without verified component support.
- Rename `Pressed` to `Checked` in Figma property documentation.
- Rename `Focus` to `Focused`.
- Interpret `Pressed=False` as Disabled.
- Change values because of Hover or Focus.
- Assume all Toggles auto-save.
- Assume all Toggles require a Save button.
- Invent initial values.
- Use Toggle for Save, Delete, Submit, or Confirmation actions.
- Use Toggle for Approval decisions without explicit requirements.
- Convert multi-stage workflow statuses into binary settings.
- Invent colors, dimensions, typography, or effects.
- Modify business workflows or permissions.
- Treat illustrative examples as universal requirements.

## 14. Official Figma References

| Reference | Purpose | Figma |
|---|---|---|
| GEMS Toggle Overview | Toggle library | [Open](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=12-17422) |
| GEMS Toggle Base | Base switch variants | [Open](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1868-18337) |
| GEMS Toggle | Complete Toggle variants | [Open](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-6121) |
| ISS Registrasi Asset | Status Aktif example | [Open](https://www.figma.com/design/v3ggUUZOrTe6dh9wJ21Hcy/ISS-Registrasi-Asset?node-id=365-92063) |

### Related Guidelines

**Foundation**
- `Foundation/color.md`
- `Foundation/typography.md`
- `Foundation/spacing-dan-radius.md`
- `Foundation/effect-styles.md`
- `Foundation/icons.md`
- `Foundation/design-annotations.md`

**Components**
- `components/button.md`
- `components/input.md`
- `components/input-dropdown.md`

Use actual repository paths if component filenames differ.

Read GEMS Page Samples and UX Patterns only when relevant to the current screen.

## 15. Implementation Requirements

### 15.1 Source Responsibilities

| Source | Responsibility |
|---|---|
| HSD/BRD | Business meaning, initial values, permissions, validation, saving |
| GEMS Design System | Components, variants, sizes, states, and visual styling |
| Approved Product Designs | Contextual examples |
| Human Approval | Decisions outside existing requirements |

### 15.2 Human Approval

Request confirmation when:

- A required binary interaction has no suitable GEMS General component.
- Unsupported visual styling or behavior is necessary.
- Business consequences or saving behavior are essential but undefined.
- The correct choice between Toggle and another component materially affects the workflow.

Combine related questions into one confirmation.

**Fallback:** Use the closest officially supported GEMS General component appropriate to the interaction. If this requires inventing a component or business rule, request Human Approval. Never use CCM.

---

**FINAL RULE:** Every Toggle MUST represent an actual binary value using the official GEMS General component. Apply correct `Pressed`, `Size`, `Text`, and `State` properties; preserve GEMS Foundation styling; follow HSD/BRD for permissions and saving; and never introduce CCM or unsupported behavior.
