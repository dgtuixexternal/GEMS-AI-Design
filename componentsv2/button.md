
# GEMS Design System — Components / Button

> **MANDATORY:** All buttons MUST use official GEMS General Button components from the connected Figma Design System. Follow existing variants, sizes, colors, typography, icons, states, and component properties. **Button CCM is strictly prohibited.**

## 1. Purpose & Source of Truth

Button digunakan untuk tindakan pengguna seperti membuat, menyimpan, mengubah, menghapus, mengirim, membatalkan, mengonfirmasi, dan menghentikan proses.

**Core Principle:** Button hierarchy is determined by action priority, UI context, and consequences—not by the button label alone.

### Official Figma References

- [GEMS Button Library](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=12-1130)
- [GEMS General Button](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=294-4425)
- [Button Close X](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=310-1955)
- [Social Button](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1869-10020)
- [Social Button Groups](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1869-10291)

### Reference Priority

1. **Official GEMS General Button:** Component properties, hierarchy, sizes, states, and styling.
2. **GEMS Components:** Button usage within existing reusable components.
3. **GEMS Page Samples & UX Patterns:** Contextual hierarchy, grouping, placement, and responsive behavior.
4. **Product HSD/BRD:** Supported actions, user permissions, labels, and business workflows.
5. **General UI/UX Principles:** Fallback when no specific GEMS guidance exists.

Read only the GEMS components, Page Samples, and UX Patterns relevant to the requested interface.

**GEMS component specifications take precedence over sample visuals.**

## 2. Button Variants & Hierarchy

### 2.1 Available Variants

Use the exact hierarchy variants available in the official GEMS General Button component.

| Variant | Visual Hierarchy | Purpose |
|---|---|---|
| `Primary` | Highest | Main action with strongest visual emphasis |
| `Secondary color` | Medium | Contextual action requiring color emphasis |
| `Secondary gray` | Medium | Neutral supporting or utility action |
| `Tertiary color` | Low | Additional action with subtle color emphasis |
| `Tertiary gray` | Low | Additional neutral action |
| `Link color` | Text-based | Colored text-style action |
| `Link gray` | Text-based | Neutral text-style action |

**Implementation Scope**

- Primary, Secondary Color, Secondary Gray, and Tertiary Gray have defined contextual guidance below.
- Tertiary Color has general principles, but no universal product-specific example has been established.
- Link Color and Link Gray exist in GEMS, but their contextual use MUST follow official GEMS references.
- Do not invent business usage rules for variants whose application is not specified.

### 2.2 Button Usage Matrix

| Variant | When to Use | When NOT to Use | Example |
|---|---|---|---|
| Primary | Highest-priority action within an action group | Low-priority supporting actions | Simpan, Buat Pesanan, Konfirmasi |
| Secondary Color | Contextual action requiring color emphasis without dominant solid styling | Neutral actions suited to Secondary Gray | Ubah Pesanan, Hapus, Stop Charging |
| Secondary Gray | Supporting, cancel, back, edit, export, or utility action | Main action requiring strongest emphasis | Batal, Kembali, Edit, Ekspor Data |
| Tertiary Color | Additional low-priority action requiring subtle color | Main actions or important confirmations | Follow approved GEMS context |
| Tertiary Gray | Additional low-priority neutral action | Actions requiring high emphasis | Neutral additional action |
| Link Color | Text-style action when specified by GEMS | Replacing a required standard Button without justification | Follow official GEMS pattern |
| Link Gray | Neutral text-style action when specified by GEMS | Replacing important primary or confirmation actions | Follow official GEMS pattern |

### 2.3 General Hierarchy Rules

- MUST determine hierarchy from action importance, page context, consequences, and related actions.
- MUST use existing GEMS Button variants.
- SHOULD have one visually dominant Primary action per action group.
- MAY use approved exceptions defined by GEMS contextual patterns.
- MUST maintain consistent hierarchy for equivalent actions across screens.
- MUST NOT make every button Primary.
- MUST NOT select a variant only because its label contains `Edit`, `Delete`, `Save`, or `Confirm`.
- MUST NOT force a Primary button into an action group that does not require one.

## 3. Primary Button

### 3.1 Definition

Primary is the highest-priority action within a specific page, section, form, dialog, or action group.

### 3.2 When to Use

- Save data or changes.
- Create new records.
- Submit requests or reports.
- Confirm the main action.
- Execute the primary purpose of the current workflow.

### 3.3 Examples

| Context | Button Label | Variant |
|---|---|---|
| Create form | Simpan | Primary |
| Order form | Buat Pesanan | Primary |
| Submission | Kirim Pengajuan | Primary |
| Confirmation modal | Konfirmasi | Primary |
| Page Header | Ubah Data Aset | Primary |

### 3.4 Rules

**MUST**
- Use Primary for the most important action within its group.
- Preserve official GEMS component styling.
- Apply the approved semantic color and state.
- Make its visual priority consistent with its actual purpose.

**SHOULD**
- Limit Primary to one per action group.
- Pair Primary with Secondary Gray when a neutral alternative is needed.

**MAY**
- Use approved positive or negative solid styling for specific GEMS confirmation patterns.

**MUST NOT**
- Use Primary for all visible actions.
- Use Primary merely because an action changes data.
- Invent custom Primary colors or variants.
- Apply a red/green Primary outside officially supported contexts.

## 4. Secondary Color Button

### 4.1 Definition

Secondary Color provides contextual color emphasis with the official GEMS visual treatment, including the outline appearance used in approved patterns.

It is less visually dominant than Primary.

### 4.2 When to Use

- An action needs contextual color emphasis.
- A table or detail action requires stronger distinction than a neutral button.
- An action's consequence needs visual differentiation.
- A solid Primary appearance would be too dominant.

### 4.3 Examples

| Context | Button Label | Visual |
|---|---|---|
| Table Row | Ubah Pesanan | Colored Outline |
| Detail Page | Hapus | Red Outline |
| Live Charging Session | Stop Charging | Red Outline |

### 4.4 Rules

**MUST**
- Use the official Secondary Color component variant.
- Follow approved GEMS semantic colors.
- Preserve the exact color and visual treatment of the relevant pattern.

**SHOULD**
- Use Secondary Gray for neutral supporting actions.

**MUST NOT**
- Make every negative action solid red.
- Use Secondary Color for all supporting actions.
- Create custom outline colors or borders.
- Treat every Edit action as requiring colored emphasis.

## 5. Secondary Gray Button

### 5.1 Definition

Secondary Gray is a neutral supporting button used for alternatives, cancellation, navigation, editing, and utility actions.

### 5.2 When to Use

- Cancel an operation.
- Return to a previous screen.
- Edit data when editing is not the main action.
- Export or download data.
- Perform a standalone utility action.

### 5.3 Examples

| Context | Button Label | Variant |
|---|---|---|
| Modal | Batal | Secondary Gray |
| Navigation | Kembali | Secondary Gray |
| Page Header | Ekspor Data | Secondary Gray |
| Detail Page | Edit Pesanan | Secondary Gray |
| Live Charging Session | Edit | Secondary Gray |
| Utility | Unduh Kode QR | Secondary Gray |

### 5.4 Rules

**MUST**
- Preserve official neutral GEMS styling.
- Maintain lower visual priority than the main action when grouped with Primary.

**SHOULD**
- Be the default supporting choice alongside Primary where the relevant pattern supports it.

**MAY**
- Be used without a Primary button.
- Serve as a standalone utility action.

**MUST NOT**
- Automatically become Secondary Color because the action edits data.
- Become Primary merely because it is the only button.
- Introduce unsupported neutral color values.

## 6. Tertiary Color Button

### 6.1 Definition

Tertiary Color is used for low-priority additional actions that require subtle contextual color emphasis.

### 6.2 When to Use

- The action is additional rather than primary.
- Color communicates a relevant distinction.
- Primary or Secondary emphasis would be excessive.
- An official GEMS component or contextual pattern supports its use.

### 6.3 Rules

**MUST**
- Use the official Tertiary Color variant.
- Preserve hierarchy below Primary and Secondary.
- Follow the relevant GEMS reference for contextual usage.

**MUST NOT**
- Use Tertiary Color for the main action.
- Replace an important confirmation action without an approved pattern.
- Invent unsupported product-specific usage examples.

**Human Direction:** If no suitable GEMS reference establishes its intended use, request human guidance before introducing a new usage convention.

## 7. Tertiary Gray & Link Buttons

### 7.1 Tertiary Gray — Definition

Tertiary Gray is a neutral, low-emphasis button for additional actions.

### 7.2 Tertiary Gray — When to Use

- The action is not the main priority.
- The action does not require color emphasis.
- Secondary Gray would be too visually dominant.
- The placement follows a relevant GEMS pattern.

### 7.3 Tertiary Gray — Rules

**MUST**
- Use the official Tertiary Gray variant.
- Maintain low visual emphasis.
- Follow contextual GEMS hierarchy.

**MUST NOT**
- Use it for important primary actions.
- Use it when consequences require higher emphasis.
- Invent custom text or background styling.

### 7.4 Link Color & Link Gray

These variants are official GEMS text-style buttons.

**Link Color:** Colored text-based action.

**Link Gray:** Neutral text-based action.

**Rules**
- MUST use their original GEMS component variants.
- MUST follow existing GEMS component and UX Pattern usage.
- MUST preserve official typography, color, spacing, and interaction states.
- MUST NOT replace standard action buttons solely to save space.
- MUST NOT invent detailed usage conventions absent from GEMS references.
- If the appropriate Link variant cannot be determined, use a clearly supported button pattern or request human direction.

## 8. Button Sizes, States & Properties

### 8.1 Available Sizes

Official GEMS General Button sizes:

| Size | Usage Rule |
|---|---|
| `sm` | Use where the relevant GEMS component or compact pattern specifies it |
| `md` | Use where the relevant GEMS component or pattern specifies it |
| `lg` | Use where the relevant GEMS component or pattern specifies it |
| `xl` | Use where the relevant GEMS component or pattern specifies it |
| `2xl` | Use where the relevant GEMS component or pattern specifies it |

**Important:** These descriptions do not establish fixed use cases. The official GEMS component and contextual samples determine the appropriate size.

**Size Rules**
- MUST use only existing GEMS sizes.
- MUST preserve the selected size's exact dimensions, padding, typography, and icon properties.
- MUST keep equivalent buttons consistently sized within the same action group.
- MUST follow original component sizing inside tables, forms, dialogs, headers, and other components.
- MUST adapt surrounding layout for responsive behavior without manually changing internal button styling.
- MUST NOT invent custom width, height, padding, or typography values.
- MAY use supported width and layout behavior when available through official component properties.

### 8.2 Available States

| State | Trigger | Visual Behavior | Interaction |
|---|---|---|---|
| Default | Button is enabled and idle | Official default appearance | Interactive |
| Hover | Pointer enters button | Official hover appearance | Interactive |
| Focused | Button receives focus | Official visible focus treatment | Interactive |
| Disabled | Action unavailable | Official disabled appearance | Not interactive |

### 8.3 Default State

**When to Use:** The action is available.

**MUST**
- Use the official Default state.
- Display the correct label and optional icon.
- Execute the action represented by the label.

**MUST NOT**
- Keep Hover or Focused styling permanently.

### 8.4 Hover State

**When to Use:** A pointing device hovers over the button.

**MUST**
- Use the official GEMS Hover state.
- Preserve the label and intended action.
- Return to the appropriate non-hover state when the pointer leaves.

**MUST NOT**
- Create a custom hover color.
- Treat Hover as a click or selected state.

### 8.5 Focused State

**When to Use:** A button receives keyboard or equivalent focus.

**MUST**
- Use the official GEMS Focused state.
- Preserve visible focus indication.
- Support keyboard interaction.

**MUST NOT**
- Remove the focus indicator without an approved accessible replacement.

### 8.6 Disabled State

**When to Use**
- Required conditions are incomplete.
- The action is unavailable in the current process status.
- Business rules restrict the action.
- User permissions prohibit the action and the approved UI pattern displays it as disabled.

**MUST**
- Use the official Disabled state.
- Prevent the action from executing.
- Explain unavailable actions when the reason is not obvious.

**MUST NOT**
- Use visual opacity alone as a substitute for official Disabled styling.
- Allow interaction as if enabled.
- Use Disabled instead of proper form validation and feedback.
- Display a disabled control when product authorization rules require hiding the action entirely.

### 8.7 Button Colors

- MUST use official GEMS General semantic colors and component properties.
- MUST follow the GEMS Foundation Color Guidelines.
- MUST preserve approved positive, negative, and neutral styling.
- MUST NOT invent HEX, RGB, HSL, or unsupported color combinations.
- MUST NOT use CCM-specific color tokens or styles.
- MUST NOT choose red or green solely from the action label without checking its context.

### 8.8 Button Icons

- MUST use official GEMS icons according to `icons.md`.
- MUST match the Button component's supported icon configuration.
- MUST preserve icon size, alignment, spacing, and color.
- MAY use icon-only configurations when supported by the official component and UX context.
- MUST provide an understandable accessible name for icon-only actions.
- MUST NOT replace official component icons with arbitrary alternatives.
- MUST NOT add decorative icons when unnecessary or inconsistent with GEMS patterns.

### 8.9 Unsupported States

Do not invent new visual variants for loading, active, pressed, success, or error states.

When such behavior is required, use an existing GEMS component or approved UX Pattern that explicitly supports it.

## 9. Contextual Button Patterns

The following examples define approved contextual usage. They are **not universal layouts** for every product.

### 9.1 Form Actions

**Case:** `Batal` + `Simpan`

| Button | Variant | Priority |
|---|---|---|
| Batal | Secondary Gray | Supporting |
| Simpan | Primary | Main |

**Rules**
- SHOULD use Secondary Gray + Primary when this combination fits the GEMS form pattern.
- MUST give the save action higher visual priority.
- MUST preserve the relevant GEMS form-action placement and order.

### 9.2 Positive Confirmation

**Case:** `Batal` + `Konfirmasi`

| Button | Variant |
|---|---|
| Batal | Secondary Gray |
| Konfirmasi | Primary — Green Solid |

**Rules**
- MUST use approved positive styling only when the official GEMS pattern supports it.
- MUST maintain clear hierarchy between cancel and confirm.
- MUST NOT introduce green confirmation styling as a universal default.

### 9.3 Negative Confirmation

**Case:** `Batal` + `Konfirmasi`

| Button | Variant |
|---|---|
| Batal | Secondary Gray |
| Konfirmasi | Primary — Red Solid |

**Rules**
- MUST follow the approved negative confirmation pattern.
- MUST NOT use positive styling for a destructive or negative confirmation.
- MUST NOT make every destructive action solid red outside its specific context.

### 9.4 Approval Decision

**Case:** `Tolak` + `Setujui`

| Button | Visual |
|---|---|
| Tolak | Red Solid |
| Setujui | Green Solid |

**Rules**
- MAY use two solid buttons only when an approved GEMS decision pattern explicitly supports them.
- MUST preserve their distinct meanings.
- MUST NOT apply the two-solid-button combination to ordinary forms.

**Scope:** This section defines Button appearance only. Approval permissions, transitions, and workflows MUST come from product requirements or the relevant UX Pattern.

### 9.5 Page Header Actions

**Case:** `Ekspor Data` + `Ubah Data Aset`

| Button | Variant |
|---|---|
| Ekspor Data | Secondary Gray |
| Ubah Data Aset | Primary |

**Rules**
- SHOULD use Primary for the main page action.
- SHOULD use Secondary Gray for supporting export or utility actions.
- MUST follow the relevant GEMS Page Header layout and action order.
- MUST adapt available actions to the actual product module.

### 9.6 Table Row Actions

**Case:** `Ubah Pesanan`

| Button | Variant |
|---|---|
| Ubah Pesanan | Secondary Color |

**Rules**
- MAY use Secondary Color for contextual table-row actions when supported by GEMS.
- MUST preserve button size and placement defined by the table pattern.
- MUST NOT assume every Edit action should be Primary.
- MUST NOT overcrowd table cells with unnecessary actions.

### 9.7 Detail Page Actions

**Case:** `Hapus` + `Edit Pesanan`

| Button | Variant |
|---|---|
| Hapus | Secondary Color — Red Outline |
| Edit Pesanan | Secondary Gray |

**Rules**
- MAY combine Secondary Color and Secondary Gray.
- MUST preserve the distinction between destructive and neutral actions.
- MUST NOT force a Primary button when no action requires that hierarchy.
- MUST follow approved destructive-action confirmation behavior when applicable.

### 9.8 Active Process Actions

**Case:** Live Charging Session

| Button | Variant | Purpose |
|---|---|---|
| Edit | Secondary Gray | Modify session information |
| Stop Charging | Secondary Color — Red Outline | Stop an active charging process |

**Rules**
- MAY use Secondary Gray for supporting edits.
- MAY use Secondary Color Red Outline for approved process-stopping actions.
- MUST preserve the actual business consequence of each action.
- MUST NOT automatically apply solid red to every process-stopping action.

### 9.9 Standalone Utility Actions

**Case:** `Unduh Kode QR`

| Button | Variant |
|---|---|
| Unduh Kode QR | Secondary Gray |

**Rules**
- MAY use Secondary Gray independently.
- MUST NOT force a Primary variant for standalone utility actions.
- MUST preserve the correct label, icon, and interaction behavior.

### 9.10 General Contextual Rules

- MUST select patterns according to the actual page and workflow.
- MUST use GEMS Page Samples and UX Patterns for hierarchy, placement, grouping, and responsiveness.
- MUST preserve official component styling even when sample layouts are adapted.
- MUST NOT copy sample button labels unrelated to the product.
- MUST NOT assume every page or action group requires a Primary button.
- MUST NOT change business workflows solely because a visual example contains an action.

## 10. Button Labels, Placement & Grouping

### 10.1 General Label Rules

Button labels MUST:
- Clearly describe the resulting action.
- Use terminology from the approved HSD/BRD or product requirements.
- Be concise and understandable.
- Remain consistent across equivalent workflows.
- Match the actual operation and user permissions.

**MUST NOT**
- Use vague labels where a specific action is needed.
- Copy sample content that does not apply to the product.
- Invent unsupported actions.
- Add redundant buttons solely to fill layout space.

### 10.2 Label Examples

| Action | Recommended Label |
|---|---|
| Save changes | Simpan Perubahan |
| Create order | Buat Pesanan |
| Submit request | Kirim Pengajuan |
| Delete record | Hapus |
| Cancel action | Batal |
| Export records | Ekspor Data |
| Download QR | Unduh Kode QR |
| Stop charging | Stop Charging |

These are contextual examples, not fixed labels for all products.

### 10.3 Button Placement

**MUST**
- Follow the relevant GEMS component, Page Sample, or UX Pattern.
- Preserve clear visual distinction between main and supporting actions.
- Group related actions consistently.
- Use official GEMS spacing and alignment.
- Follow `spacing-radius.md` for surrounding layout spacing.
- Keep equivalent action groups consistent across screens.
- Adapt layout responsively using existing GEMS patterns.

**Context Rules**
- **Forms:** Follow the official form-action group.
- **Dialogs:** Follow the relevant confirmation-action pattern.
- **Page Headers:** Follow GEMS Page Header action positioning.
- **Tables:** Follow the relevant row-action size and placement.
- **Detail Pages:** Group actions based on priority and consequence.
- **Active Processes:** Distinguish supporting actions from process-control actions.
- **Utilities:** Avoid excessive visual emphasis.

**MUST NOT**
- Change button hierarchy just to fit available space.
- Invent custom internal padding or dimensions.
- Place unrelated actions in one group without contextual justification.
- Reorder actions contrary to an applicable GEMS pattern.
- Create unnecessary duplicate actions.

## 11. Specialized Button Components

### 11.1 Button Close X

**Source:** [GEMS Button Close X](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=310-1955)

Use the official GEMS Button Close X for dismissing or closing supported UI surfaces.

**Available component properties include:**
- Supported sizes.
- Light/dark background configuration.
- Official interaction states.

**Rules**
- MUST use the original Button Close X component.
- MUST select the correct size and background configuration.
- MUST follow the relevant GEMS dialog, panel, or overlay placement.
- MUST preserve accessible close behavior.
- MUST NOT manually recreate an X icon button.
- MUST NOT use a regular Button as a visual substitute when GEMS specifies Button Close X.

### 11.2 Social Button

**Source:** [GEMS Social Button](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1869-10020)

Use only for supported social authentication or integration actions.

**Official component options include:**
- Social provider.
- Supporting text.
- Theme.
- Interaction state.

**Rules**
- MUST use the official Social Button component.
- MUST select an available provider and theme.
- MUST preserve existing logos, typography, spacing, and state properties.
- MUST NOT invent unsupported providers.
- MUST NOT add authentication methods absent from product requirements.
- MUST NOT treat social-provider brand themes as permission to use CCM styling.

### 11.3 Social Button Groups

**Source:** [GEMS Social Button Groups](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1869-10291)

Use the official grouping component when a relevant GEMS pattern requires multiple social actions.

**Rules**
- MUST preserve official group layout and supported themes.
- MUST follow available button/icon group styles.
- MUST include only product-supported providers.
- MUST coordinate authentication content with `authentication.md`.
- MUST NOT create custom social-button arrangements when an official component exists.

## 12. AI Implementation Rules & Restrictions

### 12.1 Button Selection Rules

When creating or modifying an interface:

1. **Identify Action:** Read the product requirements and determine what the user can do.
2. **Identify Context:** Determine whether the action belongs to a Form, Dialog, Page Header, Table, Detail Page, Card, Active Process, or Utility Area.
3. **Determine Priority:** Classify it as Main, Supporting, Contextual, or Additional.
4. **Select Component & Variant:** Use the official GEMS General Button and Button Usage Matrix.
5. **Apply Properties:** Select the official size, color, icon configuration, and interaction state.
6. **Follow Contextual Pattern:** Match the relevant GEMS component, Page Sample, or UX Pattern for placement and grouping.
7. **Resolve Exceptions:** If an unsupported design or business decision is necessary, request Human Approval before introducing it.

These steps are implementation instructions. Do not generate a separate AI-validation report unless requested.

### 12.2 Strict CCM Exclusion

**MUST NOT**
- Use Button CCM components, instances, variants, or styling.
- Copy CCM-specific Button colors, typography, effects, spacing, or states.
- Duplicate CCM buttons into General components.
- Recreate CCM buttons manually.
- Use CCM buttons as a fallback.
- Transfer CCM Button styling from Page Samples into General products.

If a referenced screen contains CCM Button styling, follow its relevant content or workflow only. Implement the action using an appropriate official GEMS General Button.

### 12.3 Strict Button Rules

**MUST**
- Use existing official GEMS General Button components.
- Preserve original Figma component references and supported properties.
- Follow official hierarchy, size, color, typography, icons, and states.
- Follow GEMS Foundation Guidelines and relevant component guidelines.
- Preserve consistent grouping, placement, and visual priority.
- Follow product permissions, terminology, and business workflows.
- Maintain accessible Focused and Disabled behavior.

**MUST NOT**
- Create new or duplicate Button variants.
- Introduce custom Button styling or hardcoded colors.
- Modify official component properties outside supported variants.
- Detach official component instances without authorization.
- Use Primary for every action.
- Assume every Edit action requires Primary.
- Assume every Hapus action requires Red Solid.
- Use Secondary Color for every supporting action.
- Replace a required standard Button with a Link variant merely to save space.
- Remove visible focus treatment.
- Allow Disabled actions to execute.
- Invent unsupported visual states.
- Add arbitrary icons or unsupported dimensions.
- Treat contextual examples as universal rules.
- Invent business actions, permissions, or workflow transitions.
- Use CCM Button under any circumstances.

### 12.4 Human Approval

Request Human Approval only when:
- A required Button component or variant does not exist in GEMS.
- A new visual treatment or unsupported state is necessary.
- The intended use of an undocumented variant cannot be established from GEMS.
- A business action, permission, or workflow cannot be determined from the supplied product requirements.

Consolidate related questions into one confirmation whenever possible.

**Fallback:** Use the closest officially supported GEMS General Button configuration according to action purpose, priority, and context. If that would require inventing a design or business rule, stop and request human direction. Never use CCM as a fallback.

## 13. Figma Reference & Related Guidelines

### Primary Reference

[GEMS General Button](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=294-4425)

### Contextual References

Use the connected GEMS Design System:

- **GEMS Components:** Official button application inside reusable components.
- **GEMS Page Samples:** Hierarchy, size, grouping, and placement in complete pages.
- **GEMS UX Patterns:** Button behavior and action combinations within user workflows.

Read only references relevant to the task.

### Related GEMS Guidelines

Apply the existing project guidelines when relevant:

- `foundation/color.md` — Semantic color usage.
- `foundation/typography.md` — Official Text Styles.
- `foundation/spacing-radius.md` — Layout spacing and radius.
- `foundation/effects.md` — Official effect styles.
- `components/icons.md` — Icon usage and sizing.
- `components/authentication.md` — Authentication and social actions.
- Other relevant GEMS component guidelines for the current page.

Use the actual repository paths if filenames differ.

---

**FINAL RULE:** Every Button MUST use an official **GEMS General component**, with the correct hierarchy, size, state, color, icon, placement, and product-specific action. **Never use CCM Button. Never invent unsupported Button styling or behavior.**
