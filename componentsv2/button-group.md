
# GEMS Design System — Components / Button Group

> **MANDATORY:** Use official GEMS General Button Group components for supported grouped selections and view-switching controls. Preserve original component properties, selected states, icons, spacing, colors, and interaction behavior. Never use CCM variants or recreate Button Groups manually.

## 1. Purpose & Source of Truth

Button Group is a set of related, visually connected controls used to switch between options, modes, or views within the same context.

**Core Principle:**

> Use Button Group for related selectable options with a visible current selection—not as a replacement for ordinary action buttons.

### Official Figma References

- [GEMS Button Group Library](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=403-3601)
- [Button Group Base](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=403-5462)
- [Button Group Component](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=403-5543)

**Additional Contextual Reference**

- [ISS Transportasi App](https://www.figma.com/design/mN91DNF9bSz4H8CnXuXPW4/ISS-Mess-Mangement?node-id=108-148613)

### Reference Priority

1. **GEMS Button Group:** Official component structure, properties, and states.
2. **GEMS Components:** Button Group usage within reusable components.
3. **GEMS Page Samples & UX Patterns:** Contextual application, placement, and behavior.
4. **Product HSD/BRD:** Available options, data, workflows, and permissions.
5. **General UI/UX Principles:** Fallback only when GEMS provides no specific guidance.

Use relevant GEMS Page Samples and UX Patterns to determine where Button Groups belong.

Product-specific designs, including ISS, provide usage context but MUST NOT override GEMS General component specifications.

## 2. Available Components & Properties

### 2.1 Button Group Base

The official GEMS Button Group Base includes these properties:

| Property | Available Values | Purpose |
|---|---|---|
| `Current` | `True`, `False` | Indicates whether an option is currently selected |
| `Icon` | `False`, `Leading`, `Only`, `Dot` | Configures icon presentation |
| `State` | `Default`, `Hover`, `Focused`, `Disabled` | Represents interaction status |

The base component defines the individual selectable segments and their interaction states.

### 2.2 Button Group Component

The official grouped component includes these configurations:

| Configuration | Usage |
|---|---|
| `Icon=False` | Text-based options |
| `Icon=Leading` | Options containing text and a leading icon |
| `Icon=Only` | Icon-only options |

Select the configuration provided by the relevant GEMS component or UX Pattern.

`Icon=Dot` exists in the base component but MUST NOT be introduced into a composed Button Group unless the official implementation supports that configuration.

### 2.3 Component Rules

**MUST**
- Use the official GEMS General Button Group.
- Preserve original component references and properties.
- Use supported Current, Icon, and State values.
- Maintain the original connected-segment structure.
- Follow existing GEMS styling for borders, radius, spacing, typography, and colors.

**MUST NOT**
- Recreate the group using separate standard Buttons.
- Invent custom component variants.
- Mix unsupported icon configurations.
- Apply CCM styling.
- Manually adjust selected-state styling outside official component properties.

## 3. Button Group Usage & Selection

### 3.1 When to Use

Use Button Group when users need to select between related options within the same interface context.

Typical applicable scenarios include:

- Switching between alternative data views.
- Switching display modes.
- Selecting a supported presentation mode.
- Switching between related, mutually exclusive options.
- Changing how the same information is displayed.

Use a scenario only when supported by the relevant GEMS pattern and product requirements.

### 3.2 Usage Matrix

| Context | Button Group Usage | Requirement |
|---|---|---|
| List / Grid View | Switch between list and grid presentation | Both views must exist |
| Display Mode | Switch between supported visualization modes | Each mode must work |
| Data Presentation | Switch how the same data is displayed | Preserve data scope |
| Exclusive Option | Select one option from a related group | Selection behavior must be defined |
| CRUD Actions | Not the default control | Use actions from `button.md` |
| Page Navigation | Not the default navigation component | Follow GEMS Navigation guidelines |
| Form Submission | Not appropriate | Use a standard GEMS Button |
| Destructive Action | Not appropriate | Follow Button and confirmation patterns |

The examples above describe possible use cases, not proof that every scenario has an approved GEMS implementation.

### 3.3 When NOT to Use

**MUST NOT** use Button Group for:

- `Simpan` + `Batal`
- `Edit` + `Hapus`
- `Tambah` + `Ekspor`
- `Setujui` + `Tolak`
- Unrelated actions grouped solely for visual convenience.
- Primary page navigation when GEMS provides a dedicated navigation component.
- Workflow steps requiring separate submit, confirm, or destructive operations.

Use standard GEMS Buttons for independent actions.

## 4. Current Selection & Interaction States

### 4.1 Current Property

`Current=True` represents the selected option.

`Current=False` represents an unselected option.

**MUST**
- Clearly indicate the currently active option.
- Keep the visual state synchronized with the actual displayed content or mode.
- Apply the official GEMS selected-state styling.
- Update the current selection when the user successfully switches options.

**For mutually exclusive groups**
- SHOULD have one current option.
- MUST NOT show multiple current options simultaneously unless the approved component and product behavior explicitly support multi-selection.

A group may have no current option only when an approved interaction pattern explicitly requires it.

### 4.2 Default State

Use when an option is available and not hovered or focused.

- MUST preserve official GEMS appearance.
- MUST distinguish Current and non-Current options.
- MUST respond according to its intended action.

### 4.3 Hover State

Use when the pointer is over an enabled option.

- MUST use the official Hover state.
- MUST NOT change the Current value simply because the user hovers.
- MUST NOT treat Hover as a selected state.

### 4.4 Focused State

Use when an option receives keyboard or equivalent focus.

- MUST use the official Focused state.
- MUST preserve visible focus indication.
- MUST support keyboard interaction.

Keyboard behavior MUST follow the implemented GEMS component and applicable accessibility pattern.

### 4.5 Disabled State

Use when an option is unavailable according to product conditions or permissions.

- MUST use the official Disabled state.
- MUST prevent activation.
- SHOULD explain unavailability when the reason is unclear.
- MUST NOT use Disabled to conceal missing functionality.

An option unavailable to the user's role may need to be hidden instead of disabled, depending on approved product requirements.

## 5. Icon, Size & Visual Rules

### 5.1 Icon Usage

**Icon=False**
- Use for text-based grouped options.
- Keep labels short and understandable.

**Icon=Leading**
- Use when an icon supports a textual option.
- Follow official icon alignment and spacing.

**Icon=Only**
- Use when icon meaning is recognizable.
- MUST provide accessible names or tooltips where appropriate.
- MUST preserve the original icon size and interaction area.

**Icon=Dot**
- Available in the base component.
- Use only where an approved GEMS configuration explicitly supports it.

### 5.2 Icon Rules

- MUST follow `icons.md`.
- MUST use official GEMS icons.
- MUST maintain consistent icon style within the same group.
- MUST preserve component-defined dimensions, alignment, and spacing.
- MUST NOT invent icon sizes or positions.
- MUST NOT mix line and filled icons inconsistently with GEMS guidelines.

### 5.3 Size & Layout

- MUST follow the exact dimensions defined by the official Button Group component.
- MUST preserve segment height, internal padding, spacing, and connected borders.
- MUST follow GEMS typography and radius tokens.
- MUST maintain consistent segment alignment.
- MUST adapt the surrounding layout when space is limited.
- MUST NOT manually resize individual segments in ways unsupported by the component.
- MUST NOT introduce a new size variant without Human Approval.

### 5.4 Color

- MUST use official GEMS General semantic colors.
- MUST preserve the selected and unselected visual treatments.
- MUST maintain distinguishable Hover, Focused, and Disabled states.
- MUST follow `foundation/color.md`.
- MUST NOT hardcode HEX, RGB, HSL, or CCM colors.

## 6. Contextual UI Application

### 6.1 Page Header & Toolbar

Button Group MAY appear in a header or toolbar when it controls a supported view or presentation mode.

**Rules**
- Place it near the content it controls.
- Follow the relevant GEMS Page Header or toolbar pattern.
- Keep it visually distinct from independent page actions.
- Do not replace the main Primary action with a Button Group.

**Example:**

A data page supports both List View and Grid View.

- Button Group controls the active view.
- `Tambah Data` remains a standard Primary Button.
- `Ekspor Data` remains a standard supporting Button.

### 6.2 List & Data Table

Use Button Group only when the page supports multiple related display modes.

**Rules**
- Switching modes MUST update the appropriate content view.
- Preserve applicable search, filter, and data context.
- Follow GEMS Table, Input, Filter, and Pagination guidelines.
- Do not use Button Group as a replacement for filters when GEMS specifies an Input or Select component.
- Do not introduce Grid View unless it is supported by product requirements.

### 6.3 Dashboard

Button Group MAY control supported dashboard presentation modes.

**Rules**
- Use only when the dashboard genuinely provides multiple modes.
- Keep the current mode synchronized with the displayed data.
- Follow the official GEMS Dashboard, Chart, and related component guidelines.
- Do not invent additional charts or display modes solely to justify a Button Group.
- Do not replace period filters or date-range inputs unless the relevant GEMS pattern explicitly uses Button Group.

### 6.4 Detail Page

Button Group MAY switch between supported representations of the same content.

**Rules**
- Preserve the current record and context.
- Do not use it to combine unrelated CRUD actions.
- Follow the relevant GEMS Detail Page pattern.
- Keep the selected option consistent with visible content.

### 6.5 Mobile & Responsive Layout

- Follow the relevant GEMS mobile Page Samples and UX Patterns.
- Preserve touch-target usability and readable labels.
- Use icon-only configurations only when meaning remains clear.
- Do not invent responsive variants absent from GEMS.
- If the group does not fit, adapt its surrounding layout or use an officially supported alternative.

## 7. CRUD & Data Behavior

Button Group is a **selection or view-control component**, not a CRUD action component.

### 7.1 Create

- Use a standard GEMS Button for creating records.
- Button Group MAY control an existing supported view, but MUST NOT replace `Tambah` or `Simpan`.
- Newly created data MUST appear according to product workflow and current view behavior.

### 7.2 Read

- Button Group MAY switch between supported reading or presentation modes.
- The current selection MUST match the displayed content.
- Preserve relevant search, filter, and pagination context where applicable.

### 7.3 Update

- Use a standard GEMS Button for editing or saving records.
- Do not treat switching Button Group options as editing business data unless requirements explicitly define that behavior.
- If selection changes user data, follow the approved save or confirmation workflow.

### 7.4 Delete

- Use standard GEMS destructive-action components and confirmation patterns.
- MUST NOT use Button Group as a substitute for a Delete action.
- Removing a record MUST follow product authorization and confirmation requirements.

### 7.5 CRUD Rules

- MUST follow `button.md` for independent CRUD actions.
- MUST follow the product's business permissions and status rules.
- MUST NOT invent CRUD operations because a sample contains them.
- MUST NOT imply data has been saved merely because a Button Group option changed.

## 8. Empty, Loading & Error States

Button Group selection and content availability are separate concerns.

### 8.1 Empty State

When the selected mode contains no data:

- Display the appropriate GEMS Empty State component or UX Pattern.
- Keep the selected Button Group option visually accurate.
- Provide contextual empty-state wording.
- Show a relevant action only when supported by product requirements.
- Do not automatically disable the entire group simply because data is empty.

**Example:**

A page offers List View and Grid View but currently has no records.

- The selected view remains current.
- The content area displays the official Empty State.
- An optional `Tambah Data` action follows the regular Button guideline.

### 8.2 Loading State

When switching modes requires data loading:

- Follow the relevant GEMS loading or skeleton pattern.
- Keep Current selection synchronized with the defined transition behavior.
- Prevent conflicting repeated actions when necessary.
- Do not invent custom Button Group loading states.

### 8.3 Error State

When the selected content cannot be loaded:

- Follow the official GEMS Error State pattern.
- Preserve a meaningful view selection.
- Provide an approved retry action where applicable.
- Use a standard GEMS Button for retry if specified.
- Do not use Disabled as a replacement for error feedback.

### 8.4 No Access / Unavailable Mode

When a mode is unavailable because of role permissions or business status:

- Apply product authorization rules.
- Hide or disable the option according to the approved UX Pattern.
- Do not expose inaccessible data by switching views.
- Do not fabricate placeholder content to simulate unavailable functionality.

## 9. Product Context & Content Rules

### 9.1 Product-Specific Options

Button Group labels and options MUST reflect actual product capabilities.

**MUST**
- Read the relevant HSD/BRD and product module.
- Use approved terminology.
- Include only supported options.
- Keep labels consistent across equivalent screens.
- Match selection behavior with the displayed content.

**MUST NOT**
- Copy unrelated option labels from Page Samples.
- Invent display modes.
- Add options solely to make the group visually balanced.
- Use Button Group when only one meaningful option exists without an approved reason.

### 9.2 ISS Reference

Use the provided ISS Transportasi App design as supplementary product-context reference.

**Rules**
- Follow GEMS for Button Group component styling.
- Follow ISS only for applicable workflow or content context.
- Do not assume all controls in the ISS design are Button Groups.
- Do not transfer ISS-specific business actions to unrelated products.
- Do not copy non-GEMS component styling.

### 9.3 Human Approval

Request Human Approval when:

- The product does not specify which views or modes exist.
- Multiple interaction behaviors are plausible and materially affect the product.
- No official GEMS component supports a required configuration.
- A new visual variant or unsupported selection behavior is required.

Combine related questions into one confirmation whenever possible.

## 10. Strict AI Implementation Rules

### MUST

- Use the official GEMS General Button Group.
- Preserve original component references.
- Apply valid Current, Icon, and State properties.
- Match the active selection with the displayed content.
- Use official GEMS colors, typography, spacing, radius, and icons.
- Follow relevant Page Samples and UX Patterns.
- Preserve appropriate Empty, Loading, Error, and Disabled behavior.
- Use standard GEMS Buttons for independent CRUD actions.
- Respect product roles, permissions, and supported functionality.
- Maintain consistent visual behavior across equivalent screens.

### MUST NOT

- Use Button Group CCM.
- Recreate Button Group using manually connected Buttons.
- Create custom Button Group variants or states.
- Hardcode styling outside official GEMS components.
- Use Button Group for unrelated actions.
- Replace standard Primary, Secondary, or destructive buttons with Button Group.
- Invent unsupported views or modes.
- Show a Current selection inconsistent with actual content.
- Enable unavailable options without permission.
- Invent custom icon sizes, borders, colors, or spacing.
- Treat Empty State as a reason to automatically disable the entire group.
- Assume Button Group selection automatically saves business data.
- Copy product-specific labels from unrelated GEMS or ISS examples.
- Override official GEMS component specifications.

### Fallback

If the required interaction matches an existing official Button Group pattern, use it directly.

If the task requires independent actions, use standard GEMS Buttons according to `button.md`.

If the interaction cannot be represented using existing GEMS components without inventing new behavior or styling, request Human Approval.

---

**FINAL RULE:** Button Group MUST represent a valid grouped selection or view-control interaction, using the official GEMS General component. Its Current state, icon configuration, behavior, placement, and displayed content MUST remain consistent. Never use CCM or invent unsupported variants.
