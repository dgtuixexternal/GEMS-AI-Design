
# GEMS Design System — Components / Tooltip

> **MANDATORY:** All Tooltips and Help Icons MUST use official GEMS General components from the connected Figma Design System. Preserve original component references, supported variants, colors, typography, spacing, radius, effects, and positioning. **CCM components and CCM-derived styling are strictly prohibited.**

## 1. Purpose & Source of Truth

Tooltip provides brief contextual information that helps users understand UI elements without interrupting their workflow.

This guideline covers:

- Tooltip
- Help Icon
- Supporting text
- Theme and Arrow
- Open/close behavior
- Placement and accessibility
- Contextual usage across GEMS interfaces

**Core Principle:**

> Use Tooltip to clarify an interface element—not to replace essential labels, instructions, validation, warnings, or confirmations.

### 1.1 Reference Priority

1. **Official GEMS General Components:** Tooltip properties, variants, and styling.
2. **GEMS Components:** Tooltip implementation within reusable components.
3. **GEMS Page Samples & UX Patterns:** Contextual usage and interaction.
4. **Approved Product Designs:** Real-world application examples.
5. **Product HSD/BRD:** Content, terminology, permissions, and business meaning.
6. **General UI/UX Principles:** Fallback when GEMS provides no specific guidance.

GEMS governs component design; HSD/BRD governs product information and behavior.

Read only references relevant to the current interface.

## 2. Component Selection Matrix

| Requirement | Component | Example |
|---|---|---|
| Explain a UI element briefly | Tooltip | Icon function |
| Provide contextual help through an icon | Help Icon | Field explanation |
| Clarify a metric | Tooltip / Help Icon | Dashboard calculation |
| Explain a table column | Tooltip / Help Icon | Column meaning |
| Clarify an icon-only action | Tooltip | Edit or Export icon |
| Explain unavailable functionality | Tooltip, when supported | Disabled action |
| Provide mandatory field instructions | Inline helper text | Required format |
| Display validation errors | GEMS validation component | Invalid input |
| Display important warnings | Alert / Modal | Destructive consequences |
| Confirm an action | Confirmation Modal | Delete confirmation |
| Present complex interactive content | Appropriate GEMS component | Form or interactive menu |

### 2.1 When to Use Tooltip

Use Tooltip when:

- An icon or control needs additional clarification.
- A technical term is unfamiliar.
- A dashboard metric requires a brief explanation.
- A table column needs contextual information.
- A field benefits from optional guidance.
- A disabled control needs a short explanation.
- Additional information is helpful but not essential for completing the task.

### 2.2 When NOT to Use Tooltip

**MUST NOT** use Tooltip to:

- Replace field labels.
- Hide mandatory instructions.
- Replace validation messages.
- Display critical warnings or confirmations.
- Present long explanations or complex workflows.
- Contain unsupported interactive content.
- Hide essential data behind hover.
- Repeat information that is already clear.
- Add decorative help elements without a meaningful purpose.

If the information is required to complete a task, use an appropriate visible GEMS component instead.

## 3. Tooltip Component

### 3.1 Available Properties

| Property | Official Values |
|---|---|
| `Supporting text` | `True`, `False` |
| `Theme` | `Light`, `Dark` |
| `Arrow` | `None`, `Top center`, `Bottom center`, `Bottom left`, `Bottom right`, `Left`, `Right` |

Use exact property names and supported GEMS combinations.

### 3.2 Property Usage Matrix

| Property | Usage |
|---|---|
| Supporting text=False | Short explanation without additional description |
| Supporting text=True | Main text with brief supporting explanation |
| Theme=Light | Official Light appearance |
| Theme=Dark | Official Dark appearance |
| Arrow=None | Tooltip without directional arrow |
| Arrow with direction | Indicates relationship with the triggering element |

### 3.3 Supporting Text

**Supporting text=False**
- Use for concise information.
- Avoid unnecessary descriptions.

**Supporting text=True**
- Use when the main explanation benefits from additional context.
- Keep supporting information short and relevant.
- Apply official GEMS Text Styles.

**Rules**
- Preserve official component content hierarchy.
- Do not enable supporting text merely to enlarge the Tooltip.
- Do not invent additional content properties.
- Do not use Tooltip for paragraphs requiring dedicated help content.

## 4. Theme, Arrow & Placement

### 4.1 Theme

Available themes:

- `Light`
- `Dark`

**Rules**
- Follow official GEMS component and contextual patterns.
- Preserve theme-specific text and background styling.
- Maintain readable contrast.
- Use official GEMS General semantic colors.
- Do not manually create alternative theme colors.
- Do not automatically assume every dark interface requires Dark Tooltip without checking GEMS guidance.

### 4.2 Arrow Variants

| Arrow | Position |
|---|---|
| None | No arrow |
| Top center | Top-center arrow |
| Bottom center | Bottom-center arrow |
| Bottom left | Bottom-left arrow |
| Bottom right | Bottom-right arrow |
| Left | Left-side arrow |
| Right | Right-side arrow |

### 4.3 Placement Rules

- Position Tooltip near its triggering element.
- Match Arrow direction to actual Tooltip placement.
- Preserve official arrow shape and dimensions.
- Maintain correct trigger-to-tooltip alignment.
- Avoid covering important content or controls.
- Keep Tooltip within the viewport where possible.
- Use another supported placement when available space is limited.
- Follow GEMS spacing and responsive patterns.
- Do not create custom arrow positions or manually redraw arrows.

## 5. Help Icon Component

Help Icon provides an explicit contextual-help trigger with an associated Tooltip.

### 5.1 Available Properties

| Property | Official Values |
|---|---|
| `Open` | `True`, `False` |
| `Supporting text` | `True`, `False` |
| `Tooltip` | `Top no arrow`, `Top arrow`, `Top right`, `Top left`, `Bottom`, `Right`, `Left` |

### 5.2 Open Behavior

| Open | Meaning |
|---|---|
| False | Tooltip hidden |
| True | Tooltip visible |

**Rules**
- Use the original GEMS Help Icon component.
- Keep `Open` synchronized with actual visibility.
- Preserve official Tooltip placement.
- Do not assume Tooltip must always be open.
- Do not invent Open states or interaction properties.

### 5.3 Help Icon Placement

Recommended contexts:

- Form labels
- Dashboard metrics
- Table headers
- Configuration settings
- Technical terms

**Rules**
- Place Help Icon next to the information it explains.
- Preserve official icon size, alignment, and spacing.
- Maintain consistent placement across equivalent components.
- Do not attach Help Icon to every label automatically.
- Do not recreate Help Icon using arbitrary icons.

### 5.4 Tooltip vs Help Icon

| Situation | Use |
|---|---|
| Existing control needs brief explanation | Tooltip |
| Information needs a dedicated help trigger | Help Icon |
| Icon-only button needs clarification | Tooltip attached to action |
| Form label needs optional explanation | Help Icon |
| Mandatory instructions are required | Visible helper text |
| Complex information is required | Appropriate visible GEMS component |

**Important:** Tooltip does not always require a Help Icon.

## 6. Interaction Behavior

### 6.1 Supported Triggers

Tooltip interaction MUST follow the applicable GEMS component and approved UX Pattern.

Possible contexts:

- Pointer Hover
- Keyboard Focus
- Help Icon activation
- Approved touch interaction

Do not invent trigger behavior unsupported by the component or product.

### 6.2 Hover

- Tooltip MAY appear when a supported trigger is hovered.
- Hover MUST NOT execute the underlying action.
- Tooltip content MUST remain associated with its trigger.
- Hover MUST NOT change application data.

### 6.3 Keyboard Focus

- Preserve visible focus on the triggering element.
- Make Tooltip information accessible through the applicable keyboard pattern.
- Do not remove focus indicators.
- Do not make essential guidance available only through pointer hover.

### 6.4 Touch & Mobile

- Follow official GEMS Mobile Page Samples and UX Patterns.
- Do not rely exclusively on Hover.
- Use an approved touch-accessible trigger when necessary.
- Preserve appropriate dismissal behavior.
- Keep Tooltip visible within the available screen area.
- Do not invent mobile-specific Tooltip variants.

### 6.5 Open & Close

- Open Tooltip according to the supported trigger.
- Close Tooltip according to the approved interaction.
- Preserve correct visibility.
- Avoid obstructing relevant UI controls.
- Do not change user data when Tooltip opens or closes.
- Do not create unsupported animations or interaction states.

## 7. Tooltip Content & Wording

### 7.1 Content Rules

Tooltip content MUST be:

- Short
- Clear
- Contextual
- Relevant
- Consistent with HSD/BRD terminology

**MUST NOT**
- Invent business definitions.
- Include unrelated instructions.
- Duplicate obvious labels.
- Hide critical information.
- Include unsupported interactive elements.
- Expose sensitive data without authorization.

### 7.2 Content Examples

| Context | Example |
|---|---|
| Dashboard Metric | Jumlah data yang telah diproses dalam periode terpilih. |
| Form Field | Gunakan nomor identitas yang terdaftar. |
| Disabled Action | Lengkapi data wajib sebelum melanjutkan. |
| Table Header | Menampilkan tanggal pembaruan terakhir. |
| Configuration | Aktifkan untuk menerima notifikasi pembaruan. |

Examples illustrate wording only. Actual content MUST follow product requirements.

### 7.3 Supporting Text Examples

**Main Text:** Total Pengajuan

**Supporting Text:** Jumlah seluruh pengajuan pada periode yang dipilih.

**Main Text:** Status Aktif

**Supporting Text:** Menentukan apakah data dapat digunakan dalam proses terkait.

Use supporting text only when it adds meaningful clarification.

## 8. Contextual Tooltip Patterns

### 8.1 Usage Matrix

| Context | Tooltip Usage | Restriction |
|---|---|---|
| Form / Input | Optional field explanation | Do not replace labels or validation |
| Dashboard | Metric or calculation explanation | Do not invent formulas |
| Table | Column, icon, or truncated-content clarification | Do not hide critical values |
| Button | Icon-only action explanation | Do not replace action labels unnecessarily |
| Settings | Configuration explanation | Follow actual feature behavior |
| Disabled Control | Explain unavailability | Do not replace validation |
| Navigation | Clarify supported icon navigation | Follow navigation pattern |
| Empty State | Optional additional explanation | Do not replace empty-state content |

### 8.2 Form & Input

- Use Tooltip or Help Icon when contextual explanation is useful.
- Follow `components/input.md`.
- Keep mandatory instructions appropriately visible.
- Follow official GEMS validation patterns for errors.
- Do not hide required field guidance in Tooltip.

### 8.3 Dashboard & Metrics

- Use Tooltip to explain unfamiliar metrics or calculations.
- Follow approved metric definitions and reporting logic.
- Do not invent formulas, data sources, or reporting periods.
- Do not add Tooltip to every card or chart automatically.

### 8.4 Table & Data List

- Tooltip MAY clarify headers, truncated values, or icon-only actions.
- Preserve GEMS Table layout and hierarchy.
- Keep essential data accessible without hover.
- Do not use Tooltip to replace row-action confirmation.

### 8.5 Button & Icon

- Use Tooltip when an icon-only action needs explanation.
- Follow `components/button.md` and `Foundation/icons.md`.
- Preserve the original action behavior.
- Do not execute an action when Tooltip appears.
- Do not add Tooltip to every text-labeled Button.

### 8.6 Settings & Configuration

- Use Tooltip to clarify supported settings.
- Follow relevant GEMS Toggle and Input guidelines.
- Explain consequences only when supported by requirements.
- Keep significant consequences visible when necessary.

### 8.7 CRUD & Confirmation

**Create / Edit**
- Tooltip MAY explain fields or unfamiliar actions.
- Required instructions remain visible.

**Read / Detail**
- Tooltip MAY clarify values and terminology.
- Critical information must remain accessible.

**Delete**
- Tooltip MUST NOT replace destructive confirmation.
- Use official GEMS Button and confirmation UX Patterns.

### 8.8 Empty, Loading & Error States

- Use official GEMS Empty, Loading, and Error components.
- Tooltip MAY provide supplementary clarification.
- Do not replace primary state messages with Tooltip.
- Do not invent Tooltip-specific loading or error variants.

### 8.9 Approved Product Example — Meals Management ISS

**Reference:** Meals Management ISS — Export.

This product demonstrates contextual Tooltip usage attached directly to a relevant UI element.

**Rules**
- Tooltip MAY be used without a separate Help Icon.
- Use the official GEMS General Tooltip component.
- Preserve the appropriate Arrow configuration and trigger alignment.
- Keep content concise and relevant to the interaction.
- Use Help Icon only when an explicit help trigger is appropriate.
- Follow actual product requirements and accessibility behavior.
- Do not copy Meals Management labels or content into unrelated products.
- Do not treat the example as a universal placement rule.
- Never transfer CCM or unrelated product styling.

**Reference Priority:** GEMS component specifications remain authoritative. Meals Management ISS is a contextual usage reference only.

## 9. Foundation & Component Integration

### 9.1 Foundation Guidelines

Tooltip visual styling MUST follow these GEMS repository guidelines:

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | General semantic colors and contrast |
| `Foundation/typography.md` | Official GEMS Text Styles |
| `Foundation/spacing-dan-radius.md` | Padding, spacing, and radius |
| `Foundation/effect-styles.md` | Official Tooltip effects |
| `Foundation/icons.md` | General icon usage |
| `Foundation/misc-icons.md` | Specialized icons when applicable |
| `Foundation/design-annotations.md` | Additional approved specifications |

### 9.2 Color & Theme

- Use official GEMS General semantic colors.
- Preserve Light and Dark theme styling.
- Maintain readable text contrast.
- Do not use CCM tokens.
- Do not hardcode HEX, RGB, or HSL.

### 9.3 Typography

- Apply existing official GEMS Figma Text Styles.
- Preserve component-defined typography hierarchy.
- Maintain readable text wrapping.
- Do not invent font sizes, weights, or line heights.
- Do not detach original Text Styles.

### 9.4 Spacing, Radius & Effects

- Preserve official component padding, radius, and dimensions.
- Follow GEMS spacing variables for surrounding layout.
- Apply only official GEMS effects where specified.
- Do not add arbitrary shadows, borders, or blur.
- Do not change internal styling merely to fit content.

### 9.5 Icons

- Use official GEMS Help Icon or General Icons as appropriate.
- Preserve icon size, stroke style, alignment, and color.
- Follow `Foundation/icons.md`.
- Do not recreate Help Icon manually.
- Do not use CCM icon styling.

## 10. Accessibility & Responsive Rules

### 10.1 Accessibility

**MUST**
- Make Tooltip information accessible to keyboard users.
- Preserve visible focus on triggers.
- Provide meaningful accessible names for Help Icons.
- Maintain readable text and sufficient contrast.
- Support appropriate dismissal behavior.
- Keep essential information accessible without Hover.

**MUST NOT**
- Require pointer Hover for mandatory instructions.
- Remove focus indicators.
- Trap keyboard focus in a non-interactive Tooltip.
- Use inaccessible custom interactions.
- Make Tooltip the only source of critical information.

### 10.2 Responsive

- Follow relevant GEMS Page Samples and UX Patterns.
- Use supported placements to avoid clipping.
- Keep Tooltip within available viewport space.
- Maintain readability on smaller screens.
- Use approved mobile trigger behavior.
- Do not invent responsive Tooltip variants.

## 11. AI Implementation Rules

### 11.1 Selection Workflow

When implementing Tooltip:

1. **Identify Purpose:** Determine whether additional clarification is genuinely necessary.
2. **Select Component:** Use official GEMS Tooltip or Help Icon.
3. **Apply Properties:** Select supported Theme, Supporting text, Arrow, Tooltip placement, and Open configuration.
4. **Apply Content:** Use concise, product-specific wording from HSD/BRD.
5. **Apply Foundation:** Preserve official colors, typography, spacing, radius, effects, and icons.
6. **Follow Context:** Use relevant GEMS Components, Page Samples, UX Patterns, and approved product examples.
7. **Implement Interaction:** Follow supported Hover, Focus, Touch, Open, and Close behavior.
8. **Resolve Exceptions:** Request Human Approval when unsupported styling or interaction is required.

These are implementation instructions, not a separate validation report.

### 11.2 Strict Rules

**MUST**
- Use official GEMS General Tooltip and Help Icon components.
- Preserve original Figma component references.
- Use supported variants and properties.
- Follow GEMS Foundation and related component guidelines.
- Keep Tooltip content relevant and concise.
- Maintain accessible interaction.
- Follow product requirements for actual information.

**MUST NOT**
- Use Tooltip CCM or CCM-derived styling.
- Create custom Tooltip variants, themes, arrows, or states.
- Hardcode styling outside GEMS.
- Invent unsupported placement or trigger behavior.
- Add Tooltip to every icon, Button, or label automatically.
- Replace labels, validation, warnings, or confirmation with Tooltip.
- Invent product definitions, calculations, or consequences.
- Recreate Help Icon manually.
- Add unsupported interactive content.
- Copy unrelated product-specific Tooltip content.
- Override official GEMS component specifications.

### 11.3 Human Approval

Request Human Approval when:

- No suitable GEMS General Tooltip or Help Icon exists.
- Unsupported visual styling or interaction is necessary.
- Required information is unclear and materially affects user understanding.
- Essential workflow behavior would depend on an unsupported Tooltip interaction.

Combine related questions into one confirmation.

**Fallback:** Use the closest supported GEMS General component. If information is essential or too complex for Tooltip, use an appropriate visible GEMS component. Never use CCM or invent unsupported variants.

## 12. Official Figma References & Related Guidelines

### 12.1 GEMS Components

| Component | Reference |
|---|---|
| Tooltip Library | [GEMS Tooltip Overview](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-6369) |
| Tooltip | [GEMS Tooltip Component](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-6700) |
| Help Icon | [GEMS Help Icon](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-6861) |

### 12.2 Approved Product Reference

| Product | Reference |
|---|---|
| Meals Management ISS — Export | [View Tooltip Implementation](https://www.figma.com/design/FaD6En6EYVnjGzegaxhjzy/Meals-Management-ISS?node-id=232-126387) |

### 12.3 Related Guidelines

**Foundation**
- `Foundation/color.md`
- `Foundation/typography.md`
- `Foundation/spacing-dan-radius.md`
- `Foundation/effect-styles.md`
- `Foundation/icons.md`
- `Foundation/misc-icons.md`
- `Foundation/design-annotations.md`

**Components**
- `components/button.md`
- `components/input.md`
- `components/input-dropdown.md`
- `components/toggle.md`

Use actual repository paths if component filenames differ.

### 12.4 GEMS Page Samples & UX Patterns

Read relevant references for:

- Forms and Input
- Dashboard and Metrics
- Tables and Data Lists
- Settings and Configuration
- Navigation
- CRUD and Confirmation
- Empty and Error States
- Responsive Layouts

Read only references needed for the current interface.

---

**FINAL RULE:** Tooltip MUST provide concise, contextual help using the official GEMS General component. Use the correct Theme, Supporting text, Arrow, placement, and interaction behavior. Preserve GEMS Foundation styling, accessibility, and product-specific meaning. Never use CCM or invent unsupported Tooltip variants.
