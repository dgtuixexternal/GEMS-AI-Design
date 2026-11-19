
# GEMS Design System — Components / Section Footer

> **MANDATORY:** All Section Footers MUST use the official GEMS General Section Footer component. Preserve its original variants, properties, layout, typography, spacing, and interaction behavior. Custom and CCM-specific components are prohibited.

## 1. Sources & Priority

**Official References**
- [GEMS Section Footer](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-9977)
- [GEMS Section Footer Variants](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-16537)
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1105-7310)

**Priority Order**
1. **Official Section Footer:** Source of truth for component properties, variants, structure, and visual specifications.
2. **GEMS Components:** Follow official specifications for nested Buttons, Button Groups, and other controls.
3. **Page Samples & UX Patterns:** Reference for contextual usage, layout, and interaction.
4. **Product Requirements (HSD/BRD):** Determine actions, controls, content, and permissions.
5. **General UI/UX Principles:** Fallback only when GEMS provides no specific guidance.

Official GEMS specifications take precedence over custom visual preferences.

---

## 2. Purpose & Usage

Section Footer provides contextual controls, supporting links, or actions at the bottom of a section or card.

It may contain:
- Related Button Group controls.
- Supporting links or information.
- Secondary actions.
- Primary actions.

These elements are conditional and MUST follow the official component structure.

### When to Use

| Context | Recommendation |
|---|---|
| Section with contextual actions | Use `Type=Section` |
| Card with contextual actions | Use `Type=Card` |
| Section with grouped controls | Use `Button group=True` |
| Section without grouped controls | Use `Button group=False` |
| Dashboard / Report Section | Use when controls or actions are relevant |
| Detail Section | Use when section-level actions are needed |
| Information Card | Usually omit unless meaningful actions exist |
| Form Submission Area | Follow the official Form and UX Pattern specifications |
| Data Table Footer | Follow Data Table/Pagination components where applicable |
| Modal / Dialog Actions | Follow dedicated modal/dialog patterns |

### Usage Rules

- MUST determine whether a footer is necessary.
- MUST select the correct `Type` according to its parent container.
- MUST include only controls and actions relevant to the section/card.
- MUST maintain consistency across similar sections.
- MUST follow GEMS Page Samples and UX Patterns.

**MUST NOT**
- Automatically add a footer to every section or card.
- Use Section Footer as a substitute for Page Header actions.
- Use Section Footer as Pagination or a Table Toolbar.
- Add unnecessary controls merely to fill the footer.
- Duplicate actions already provided elsewhere without a defined purpose.

**Core Principle:** Section Footer exists to support contextual interaction, not to make every content container appear more complex.

---

## 3. Available Variants & Properties

**Official Component:** `Section footer`  
**Figma Node:** `240:16537`

### Component Properties

| Property | Available Values |
|---|---|
| `Type` | `Section`, `Card` |
| `Button group` | `True`, `False` |
| `Breakpoint` | `Desktop`, `Mobile` |

### Official Variants

| Variant | Type | Button group | Breakpoint |
|---|---|---|---|
| 1 | `Section` | `True` | `Desktop` |
| 2 | `Section` | `False` | `Desktop` |
| 3 | `Section` | `True` | `Mobile` |
| 4 | `Section` | `False` | `Mobile` |
| 5 | `Card` | `True` | `Desktop` |
| 6 | `Card` | `False` | `Desktop` |
| 7 | `Card` | `True` | `Mobile` |
| 8 | `Card` | `False` | `Mobile` |

### Variant Rules

- MUST select one of the eight official configurations.
- MUST use `Type=Section` for the corresponding section-level footer.
- MUST use `Type=Card` for the corresponding card-level footer.
- MUST select `Button group` according to the actual control requirements.
- MUST select `Breakpoint` according to the target viewport.
- MUST preserve official component structure and supported properties.

**MUST NOT**
- Create additional Types or unsupported variants.
- Combine different variants manually.
- Use `Button group=True` when grouped controls are unnecessary.
- Recreate the component using custom frames.

---

## 4. Type Selection

### Type: Section

Use when footer controls belong to a larger content section.

Examples:
- Changing a report period.
- Accessing additional section information.
- Performing section-level actions.
- Controlling a section-specific workflow.

**Rules**
- Actions MUST affect the corresponding section.
- Layout MUST follow the official `Type=Section` variant.
- Supporting controls MUST retain their intended scope.
- Do not introduce actions unrelated to the section.

### Type: Card

Use when footer controls belong to a specific card.

Examples:
- Performing an action on the card's data.
- Navigating to additional card details.
- Adjusting a card-specific view when supported.
- Providing a relevant secondary or primary action.

**Rules**
- Actions MUST relate to the card.
- Layout MUST follow the official `Type=Card` variant.
- Do not use card-level actions to control unrelated sections.
- Do not duplicate the card's existing actions without a valid reason.

### Selection Principle

| Question | Selection |
|---|---|
| Does the footer belong to a complete section? | `Type=Section` |
| Does the footer belong to one card? | `Type=Card` |
| Are grouped controls required? | `Button group=True` |
| Are grouped controls unnecessary? | `Button group=False` |

Choose variants based on function and parent structure—not appearance alone.

---

## 5. Button Group Usage

The `Button group` property determines whether the footer includes the official grouped-control structure.

### Use `Button group=True` When

- Multiple related options control the same section or card.
- Users need to select between meaningful alternatives.
- The official GEMS Button Group interaction pattern is appropriate.

**Example:** A reporting section may provide period choices such as predefined date ranges and a custom period option.

This is a contextual example, not a mandatory set of labels or values.

### Use `Button group=False` When

- Grouped controls are unnecessary.
- The footer only contains supporting links or actions.
- The relevant selection is already controlled elsewhere.
- The section does not require a grouped interaction.

### Button Group Rules

- MUST use the official GEMS Button Group component.
- MUST preserve its original dimensions, spacing, and states.
- MUST communicate the selected option clearly.
- MUST ensure selection changes the intended content or behavior.
- MUST use labels and values defined by the product requirements.
- MUST NOT use grouped controls for unrelated actions.
- MUST NOT copy sample options literally when they do not match the product.

**Core Principle:** Button Group must represent a meaningful selection or related control—not a decorative collection of buttons.

---

## 6. Footer Actions & Hierarchy

The official component examples include supporting content and Button actions.

However, **Primary, Secondary, and Tertiary actions are not mandatory**.

AI MUST determine which actions are appropriate.

### Action Selection

| Situation | Recommended Behavior |
|---|---|
| No relevant action | Do not force an unnecessary footer |
| Supporting information only | Use supported informational content |
| One important action | Use the appropriate official Button |
| Multiple related actions | Follow GEMS Button hierarchy |
| Optional action | Use a supported lower-emphasis action |
| Destructive action | Follow official destructive and confirmation patterns |
| Action already exists elsewhere | Avoid unnecessary duplication |

### Action Placement Rules

- MUST follow the official Section Footer layout.
- MUST use official GEMS Button components.
- MUST preserve supported Button size, variant, spacing, and alignment.
- MUST prioritize actions based on workflow importance.
- MUST use meaningful, product-specific action labels.
- MUST respect user roles and permissions.
- MUST NOT add Primary buttons merely because the Figma example contains one.
- MUST NOT duplicate Page Header or Section Header actions without a defined need.
- MUST NOT invent unsupported actions or destinations.

### Primary vs. Secondary Actions

- **Primary:** The most important action for the current section/card, when one exists.
- **Secondary:** A relevant supporting action.
- **Tertiary:** A lower-emphasis action when supported and appropriate.

Follow the official `button.md` specifications for visual appearance, variants, and states.

Do not manually invent button colors, sizes, or hierarchy.

---

## 7. Relationship with Other Components

Section Footer MUST work consistently with the parent container and surrounding components.

| Component | Responsibility |
|---|---|
| Page Header | Page identity and global page-level actions |
| Section Header | Section identity, navigation, search, and relevant top controls |
| Section Footer | Contextual controls and actions at the end of a section |
| Card Header | Card identity and card-specific top actions |
| Section Label | Compact subsection heading |
| Data Table / Pagination | Tabular data and page navigation |
| Modal / Dialog Footer | Dedicated confirmation or dialog actions |

### Integration Rules

- MUST maintain a clear hierarchy between Page, Section, and Card actions.
- MUST use Section Footer only within the appropriate parent context.
- MUST preserve official container boundaries and alignment.
- MUST keep footer actions relevant to the corresponding content.
- MUST follow related GEMS Page Samples and UX Patterns.

**MUST NOT**
- Treat Section Footer as a universal action bar.
- Replace dedicated Pagination, Modal Footer, or Form actions with Section Footer without an approved pattern.
- Duplicate an action across multiple locations unnecessarily.
- Create custom sticky footers or floating action bars without a GEMS reference.

---

## 8. Desktop & Mobile Behavior

### Desktop

- MUST use `Breakpoint=Desktop`.
- MUST preserve official horizontal layout, alignment, spacing, and dimensions.
- MUST follow the original placement of Button Group, supporting content, and actions.
- MUST maintain readable labels and accessible controls.

### Mobile

- MUST use `Breakpoint=Mobile`.
- MUST preserve the official mobile layout and control arrangement.
- MUST use the supported mobile presentation of grouped controls.
- MUST maintain access to required actions.
- MUST preserve readable labels and usable touch targets.

### Responsive Restrictions

- MUST NOT manually shrink Desktop variants to imitate Mobile.
- MUST NOT invent breakpoints or custom responsive variants.
- MUST NOT remove essential actions without an approved alternative.
- MUST NOT introduce custom stacking, overflow, or sticky behavior outside GEMS.
- MUST request Human Approval when the required responsive behavior is unsupported.

The `Breakpoint` property determines the approved component configuration. It does not authorize arbitrary responsive modifications.

---

## 9. Interaction & States

Section Footer interactions are defined by its nested components.

| Element | Required Behavior |
|---|---|
| Button Group | Official selected, hover, focus, and disabled states |
| Primary Button | Official Button interaction states |
| Secondary Button | Official Button interaction states |
| Tertiary Action | Official supported interaction behavior |
| Supporting Link | Correct destination and accessible interaction |

### Interaction Rules

- MUST preserve official interactive states.
- MUST provide visible feedback for selected options.
- MUST ensure each action performs its intended function.
- MUST prevent disabled controls from accepting actions.
- MUST use official loading feedback for asynchronous operations.
- MUST prevent unintended repeated actions when applicable.
- MUST maintain keyboard navigation and visible focus indicators.

**MUST NOT**
- Invent custom hover, selected, disabled, or loading states.
- Trigger actions unrelated to the current section or card.
- Display success feedback before an operation completes.
- Treat supporting text as an interactive link without a defined destination.

---

## 10. Content & UX Patterns

Section Footer content MUST reflect actual product requirements.

### Content Rules

- Use meaningful action labels.
- Use accurate grouped-control options.
- Match the terminology defined in HSD/BRD.
- Respect available data and user permissions.
- Keep supporting information concise.
- Preserve consistency across equivalent sections.

### Contextual Examples

| Product Context | Possible Footer Usage |
|---|---|
| Dashboard Report | Period selector and relevant report action |
| Data Summary Card | Supporting link or relevant detail action |
| Management Section | Approved section-specific action |
| Information Section | Supporting link when additional context exists |
| Detail Card | Contextual action for the card's entity |

These examples guide selection logic. They are not fixed templates and do not require every footer to contain the same controls.

**Usage Principle:** The footer should help users complete a relevant task. If it adds no meaningful function or information, omit it.

---

## 11. Foundation & Component Dependencies

Section Footer MUST follow the existing GEMS guidelines.

### Foundation

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | Official General brand and semantic colors |
| `Foundation/typography.md` | Official GEMS Figma Text Styles |
| `Foundation/spacing-dan-radius.md` | Spacing, dimensions, and radius |
| `Foundation/effect-styles.md` | Borders, dividers, and effects |
| `Foundation/icons.md` | Standard icons and official sizes |
| `Foundation/misc-icons.md` | Special-purpose icons when applicable |
| `Foundation/design-annotations.md` | Applicable layout and component annotations |

### Related Components

Follow the corresponding GEMS guidelines whenever used:

- `button.md`
- `button-group.md`
- `section-header.md`
- `card-header.md`
- `dropdown.md`
- `tooltip.md`
- `pagination.md`

Use actual repository filenames if different.

**Dependency Rules**
- MUST use official GEMS General color tokens.
- MUST apply complete existing GEMS Text Styles.
- MUST preserve official spacing, dimensions, radius, and effects.
- MUST use approved nested components and variants.
- MUST NOT hardcode HEX/RGB/HSL or unsupported typography and spacing values.
- MUST NOT introduce custom borders, shadows, or layout behavior.
- MUST NOT use CCM-specific components or styling.
- MUST NOT override nested component specifications.

---

## 12. Accessibility

Section Footer MUST:

- Maintain logical keyboard navigation.
- Provide accessible names for interactive elements.
- Preserve visible focus indicators.
- Clearly identify selected Button Group options.
- Maintain adequate contrast using official GEMS tokens.
- Avoid relying solely on color to communicate state.
- Preserve usable controls at supported breakpoints.
- Prevent disabled actions from being triggered.
- Follow the project's accessibility requirements.

---

## 13. Strict Rules

### MUST

- Use the official GEMS General Section Footer component.
- Select one of the eight supported configurations.
- Choose `Type` according to the parent container.
- Choose `Button group` according to actual control requirements.
- Choose `Breakpoint` according to the target viewport.
- Preserve original component structure and visual properties.
- Use official GEMS nested components.
- Follow relevant GEMS Page Samples and UX Patterns.
- Adapt content and actions to product requirements.
- Apply relevant Foundation guidelines.

### MUST NOT

- Use CCM-specific components or visual patterns.
- Create custom Section Footer variants.
- Recreate official components using detached frames.
- Modify original dimensions, typography, colors, or spacing.
- Add unnecessary Button Groups, links, or actions.
- Automatically add Primary, Secondary, or Tertiary buttons.
- Copy sample labels or control options without contextual relevance.
- Invent product actions, permissions, or navigation destinations.
- Duplicate controls already available elsewhere without justification.
- Replace Page Header, Section Header, Pagination, or Modal Footer.
- Create unsupported responsive or interaction patterns.
- Override official GEMS nested components.

---

## 14. AI Implementation Instructions

When generating UI using GEMS:

1. **Identify Context:** Determine whether the section or card requires a footer.
2. **Retrieve Official Component:** Use Section Footer at node `240:16537`.
3. **Select Variant:** Choose `Type=Section/Card`, `Button group=True/False`, and `Breakpoint=Desktop/Mobile`.
4. **Determine Content:** Include only meaningful supporting information, grouped controls, and actions.
5. **Apply Action Hierarchy:** Follow official GEMS Button and Button Group specifications.
6. **Preserve GEMS:** Maintain original component properties and Foundation dependencies.
7. **Follow Contextual References:** Use GEMS Page Samples and UX Patterns for placement and interaction.

**Human Approval Required When:**
- Required footer behavior cannot be represented by official variants.
- A necessary action arrangement is unsupported.
- Required responsive behavior is not specified by GEMS.
- Product requirements conflict with official component specifications.

Combine related clarification questions into one confirmation whenever possible.

If the official component cannot be accessed or its behavior cannot be determined, request the necessary Figma access or specifications. Do not invent unsupported details.

---

## Final Instruction

**AI MUST use the official GEMS Section Footer, select the correct Type, Button Group, and Breakpoint configuration, and adapt all controls and actions to the actual product requirements.**

**Not every Section or Card requires a Footer. Not every Footer requires a Button Group or Primary Button.**

**Custom components, unsupported variants, and CCM-specific patterns are prohibited.**

**GEMS Design System is the single source of truth for Section Footer visual specifications and supported interaction behavior.**
