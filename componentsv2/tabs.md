
# GEMS Design System — Components / Tabs

> **MANDATORY:** All tab-based navigation MUST use official GEMS Tabs components and supported variants. AI MUST determine tab necessity, type, content, states, and placement based on product requirements, official GEMS components, Page Samples, and UX Patterns. CCM components and styling are strictly prohibited.

## 1. Sources & Priority

**Official References**
- [GEMS Tabs](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=361-4030)
- [Tab Button Base](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=361-4475)
- [Horizontal Tabs](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=361-5496)
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1105-7310)

**Priority Order**
1. **Official GEMS Tabs:** Source of truth for component structure, variants, sizes, and states.
2. **GEMS Foundation:** Source of truth for colors, typography, icons, spacing, radius, and effects.
3. **GEMS Page Samples & UX Patterns:** Reference for layout, hierarchy, interaction, and contextual implementation.
4. **HSD/BRD:** Source of truth for tab labels, grouping, content, permissions, and business logic.
5. **General UI/UX Principles:** Fallback only when no specific GEMS guidance exists.

Official component specifications take visual priority. Product functionality MUST follow approved HSD/BRD requirements.

**CCM Restriction:** Never use CCM Tabs, CCM variants, or CCM-specific visual properties.

---

## 2. Component Anatomy & Available Variants

AI MUST retrieve and reuse the official GEMS Tabs components and their supported properties.

### 2.1 Tab Button Base

**Component:** `_Tab button base`

| Property | Available Values |
|---|---|
| `Current` | `True`, `False` |
| `Size` | `sm`, `md` |
| `Type` | `Button brand`, `Button gray`, `Button white`, `Button minimal`, `Underline`, `Line (vertical tabs)` |
| `State` | `Default`, `Hover`, `Focus` |

**Property Rules**
- `Current=True`: Indicates the active tab.
- `Current=False`: Indicates an inactive tab.
- `sm` / `md`: Select according to the official GEMS component and interface density.
- `Type`: Select according to the appropriate horizontal or vertical tab pattern.
- `State`: Follow actual interaction conditions.

**Important:** `Current` represents selection status, while `State` represents interaction status. They are separate properties and MUST NOT be treated as interchangeable.

### 2.2 Horizontal Tabs

**Component:** `Horizontal tabs`

| Property | Available Values |
|---|---|
| `Type` | `Button brand`, `Button gray`, `Button border`, `Button minimal`, `Underline` |
| `Size` | `sm`, `md` |
| `Full width` | `True`, `False` |
| `Breakpoint` | `Desktop`, `Mobile` |

**Rules**
- Use only the available `Type` values.
- Select `sm` or `md` according to page hierarchy and component context.
- `Full width=True` uses the official full-width presentation.
- `Full width=False` uses the official non-full-width presentation.
- Use the corresponding `Desktop` or `Mobile` variant.
- Preserve the layout, dimensions, spacing, and active indicator defined by GEMS.
- Do not create custom combinations outside the official component properties.

**Vertical Tabs:** Use the official `Line (vertical tabs)` base and corresponding GEMS vertical-tab pattern when vertical navigation is required. Do not reconstruct vertical tabs by rotating or manually rearranging horizontal tabs.

---

## 3. When to Use Tabs

Tabs organize related content into distinct views within the same page or contextual workspace.

**Core Principle:**

> Use Tabs when users need to switch between related content groups without leaving the primary page context. Do not use Tabs merely to divide content visually.

### Usage Matrix

| Context | Recommended Usage |
|---|---|
| Detail Page | Separate related information, history, attachments, or activity |
| Dashboard | Switch between related analytical views when necessary |
| Data Management | Organize distinct datasets or views within one module |
| Settings | Separate related configuration categories |
| User Profile | Organize profile information and associated records |
| Monitoring | Switch between related operational views |
| Report Detail | Separate summary, evidence, and history when appropriate |
| Complex Forms | Separate contextual sections only when the approved workflow supports tabs |

### Example: Detail Page

A product detail page might contain:

- Informasi Umum
- Dokumen
- Riwayat Aktivitas

Tabs are appropriate when these represent distinct but related views of the same record.

### Example: Monitoring

A monitoring page might contain:

- Semua
- Berlangsung
- Selesai

These tabs are appropriate only if the approved workflow defines them as meaningful dataset views.

**Tab labels are examples, not mandatory GEMS labels.**

AI MUST derive actual tab names and content from the product's HSD/BRD.

### When NOT to Use

Do not introduce Tabs when:
- The content is sufficiently clear in one section.
- Users must review all content simultaneously.
- Sections should appear together in a continuous form.
- The items represent unrelated application modules.
- The interface needs sequential steps rather than independent views.
- Simple filtering is better handled by GEMS Filter, Dropdown, or Button Group.
- Tabs add navigation complexity without improving usability.

For sequential multi-step processes, use the official GEMS Progress Steps pattern instead of Tabs.

---

## 4. Tab Type Selection

AI MUST select tab types according to their intended GEMS usage and page context.

| Type | Selection Guidance |
|---|---|
| `Button brand` | Use when the relevant GEMS pattern calls for stronger branded tab emphasis |
| `Button gray` | Use for the supported neutral button-style tab pattern |
| `Button white` | Use only where supported by the Tab Button Base and relevant pattern |
| `Button border` | Use for the official bordered Horizontal Tabs presentation |
| `Button minimal` | Use when a compact, visually minimal tab presentation is appropriate |
| `Underline` | Use when the official pattern communicates selection through an underline |
| `Line (vertical tabs)` | Use for supported vertical-tab navigation |

**Selection Rules**
- Follow GEMS Page Samples or UX Patterns for the same interface context.
- Keep one consistent tab type within a single tab group.
- Do not mix different visual tab types within the same navigation group.
- Do not choose a type solely because it looks more decorative.
- Do not substitute ordinary Button components for the official Tabs component.

**Brand Rule:** `Button brand` MUST use the GEMS General brand styling. Never substitute CCM brand colors or components.

---

## 5. Active, Interaction & Content States

### 5.1 Selection & Interaction

| Condition | Component Property | Expected Behavior |
|---|---|---|
| Active | `Current=True` | Identifies the selected tab |
| Inactive | `Current=False` | Identifies tabs not currently selected |
| Default | `State=Default` | Normal interaction appearance |
| Hover | `State=Hover` | Pointer interaction appearance |
| Focus | `State=Focus` | Keyboard focus appearance |

**Rules**
- Only one tab within a standard single-selection tab group should be active at a time.
- The active indicator MUST follow the selected GEMS variant.
- Changing tabs MUST update the corresponding content panel.
- Inactive tabs MUST remain distinguishable from active tabs.
- Focus MUST remain visible during keyboard interaction.
- Never manually replace the official active indicator with a custom color, line, or border.

### 5.2 Content States

Tab content may contain:
- Data tables.
- Forms.
- Cards.
- Charts.
- Information sections.
- File attachments.
- Activity history.
- Empty states.

Each content area MUST use the appropriate GEMS components.

**Empty State**
- Display the appropriate empty-state pattern inside the selected tab.
- Keep tab navigation available unless the business workflow requires otherwise.
- Do not hide an entire tab merely because its dataset is empty, unless permitted by HSD/BRD.

**Loading State**
- Use the official GEMS Loading Indicator or the supported loading pattern for the content.
- Do not display fake data while content is loading.
- Preserve tab context during loading.

**Error State**
- Use official GEMS feedback components.
- Explain the failure and provide recovery behavior when relevant.
- Do not falsely indicate successful data retrieval.

---

## 6. Tab Content & Product Context

AI MUST determine tab labels, number of tabs, and content according to actual product requirements.

### Tab Structure Rules

- Group information by meaning and user task.
- Use concise, clear, mutually distinguishable labels.
- Keep related data in the same tab.
- Avoid overlapping or duplicate content across tabs.
- Preserve consistent terminology throughout the product.
- Follow role-based access rules.
- Display the appropriate default active tab based on the user's primary task or documented workflow.

### Number of Tabs

- Do not invent a fixed number of tabs.
- Use only the tabs needed for the actual content.
- Do not create empty or redundant tabs to fill the layout.
- If many tabs are required, use the official responsive behavior and consult GEMS patterns.
- Do not invent custom scrolling, overflow menus, or wrapping behavior unsupported by the component.

### Content Consistency

When switching tabs:
- Display only the content corresponding to the selected tab.
- Preserve relevant user state when required by the workflow.
- Avoid unexpected data loss.
- Do not trigger destructive actions.
- Keep the surrounding page context stable.

---

## 7. Tabs in CRUD & UX Patterns

### Create

- Tabs may organize related form content when the approved UX pattern supports them.
- Required fields MUST remain validated according to form requirements.
- Switching tabs MUST NOT silently discard entered values.
- Do not replace a sequential creation process with Tabs when Progress Steps is more appropriate.

### Read / Detail

- Use Tabs to separate meaningful detail views such as information, attachments, and history.
- Keep the record identity and page context consistent.
- Each tab MUST use official GEMS data-display components.
- Do not create separate tabs for trivial amounts of information.

### Update

- Preserve unsaved changes when switching tabs according to the approved workflow.
- If switching causes data loss, follow the official confirmation pattern when required.
- Validation errors MUST identify the affected field or section.
- Do not save or discard data automatically without defined behavior.

### Delete

- Tabs themselves do not perform deletion.
- Destructive actions inside a tab MUST follow GEMS Button and Modal guidelines.
- Do not use an active-tab change to trigger deletion.

### Approval / Revision / Rejection

- Tabs may separate approval information, evidence, or history when supported by the workflow.
- Approval controls and confirmation dialogs MUST follow their own GEMS guidelines.
- Tabs MUST NOT replace approval steps, business status, or action confirmation.

---

## 8. Responsive Layout & Placement

### Desktop

- Use the official `Breakpoint=Desktop` variant.
- Select `sm` or `md` according to the component hierarchy.
- Apply the supported `Full width` property.
- Place Tabs within the relevant page or section container.
- Preserve the relationship between tab navigation and its content.

### Mobile

- Use the official `Breakpoint=Mobile` variant.
- Preserve supported tab dimensions and interaction behavior.
- Ensure labels remain readable.
- Follow the official handling of limited horizontal space.
- Do not shrink typography, spacing, or indicators manually to force more tabs.

### Placement Rules

- Place Tabs after the relevant page or section heading, following the matching GEMS pattern.
- Keep the content panel directly associated with its tab navigation.
- Maintain consistent placement for equivalent pages.
- Do not use Tabs as a substitute for the primary Application Navigation.
- Avoid nesting multiple tab groups unless an approved GEMS pattern requires it.

---

## 9. Related GEMS Guidelines

Tabs MUST follow all applicable existing GEMS Foundation and component rules.

### Foundation Dependencies

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | Brand General, semantic colors, active and interaction states |
| `Foundation/typography.md` | Tab labels and text hierarchy |
| `Foundation/spacing-dan-radius.md` | Tab spacing, gaps, and radius |
| `Foundation/effect-styles.md` | Official component effects when applicable |
| `Foundation/icons.md` | Official icons when supported by the component |
| `Foundation/design-annotations.md` | Design behavior and implementation notes |
| `Foundation/application-navigation` | Distinction between primary navigation and local Tabs |

### Related Component Guidelines

Follow the relevant existing guidelines for:
- **Page Header / Section Header:** Placement and page hierarchy.
- **Button / Button Group:** Actions or controls inside tab content.
- **Input / Dropdown / Checkbox:** Form elements inside tabs.
- **Data Table / Pagination:** Tabular content and navigation.
- **Badge / Tag:** Status and classification.
- **Chart:** Data visualization where appropriate.
- **Alert / Notification:** Contextual feedback.
- **Modal:** Confirmation and destructive actions.
- **Loading Indicator:** Loading states.
- **Progress Steps:** Sequential workflows that should not use Tabs.

Each component retains its own official GEMS specifications.

---

## 10. Strict GEMS Compliance

**MUST**
- Use official GEMS Tabs components and available variants.
- Preserve the original component instance and properties where supported.
- Select Tabs only when content grouping requires them.
- Use correct `Current`, `Type`, `Size`, and `State` properties.
- Follow `Full width` and `Breakpoint` properties for Horizontal Tabs.
- Derive labels and content from the product's HSD/BRD.
- Follow official GEMS Page Samples and UX Patterns.
- Maintain accessibility, keyboard focus, and correct content switching.
- Use Foundation and related components consistently.

**MUST NOT**
- Use CCM Tabs, CCM variants, or CCM-specific styling.
- Recreate official Tabs using custom Frames or ordinary Buttons.
- Invent unsupported tab types, variants, or states.
- Hardcode custom colors, typography, spacing, radius, or effects.
- Detach or override official component styling without approval.
- Mix unrelated tab styles in one group.
- Use Tabs as primary Application Navigation.
- Replace sequential Progress Steps with Tabs.
- Add unnecessary tabs or duplicate content.
- Invent tab labels or business workflows unsupported by the product.
- Change or discard user data unexpectedly during tab switching.

---

## 11. AI Selection & Human Approval

AI MUST determine:

1. **Necessity:** Does the page actually need Tabs?
2. **Context:** What related information or views should be grouped?
3. **Type:** Which official GEMS tab type matches the intended interface?
4. **Size & Layout:** Which supported size, full-width setting, and breakpoint apply?
5. **Content:** What labels and content panels are required by HSD/BRD?
6. **Behavior:** What are the active state, switching behavior, loading, empty, and error conditions?

Use existing product documentation and relevant GEMS examples before requesting additional information.

**Human Approval Required**

If the requirements demand a new tab interaction, unsupported variant, or component structure unavailable in GEMS, AI MUST request Human Approval before implementation.

Combine unresolved questions into one concise confirmation. Do not repeatedly ask about requirements already established in HSD/BRD.

**Fallback:** Use the closest appropriate official GEMS component or existing UX Pattern. Explain any unresolved limitation; do not create a new visual variant without approval.

---

## 12. Final AI Instruction

**AI MUST use official GEMS Tabs components whenever tab-based content navigation is required.**

Select the correct component variant, size, state, breakpoint, and layout based on official GEMS specifications, relevant Page Samples, UX Patterns, and product requirements.

AI MUST independently determine whether Tabs improve the user experience. Not every page, form, or detail view needs Tabs.

Maintain correct active states, content hierarchy, responsive behavior, and integration with other GEMS components.

**Never use CCM components or styling. Never invent unsupported Tabs variants or visual properties without Human Approval.**

**GEMS Design System is the single source of truth for Tabs visual specifications.**
