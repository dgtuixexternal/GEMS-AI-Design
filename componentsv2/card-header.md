
# GEMS Design System — Components / Card Header

> **MANDATORY:** All Card Headers MUST use the official GEMS General Card Header component. Preserve its original structure, variants, properties, typography, colors, spacing, and interaction behavior. Card Header CCM is strictly prohibited.

## 1. Sources & Priority

**Official References**
- [GEMS Card Header](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-8627)
- [GEMS General Card Header](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-15290)
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1105-7310)

**Priority Order**
1. **Official General Card Header:** Source of truth for component structure, properties, variants, dimensions, and visual specifications.
2. **GEMS Components:** Follow official specifications for nested components.
3. **Page Samples & UX Patterns:** Reference for contextual placement, hierarchy, and usage.
4. **Product Requirements (HSD/BRD):** Determine content, actions, and user permissions.
5. **General UI/UX Principles:** Fallback only when GEMS has no specific guidance.

**Component Restrictions**
- MUST use the official General Card Header at node `240:15290`.
- MUST NOT use `Card header CCM`, CCM variants, or CCM-specific Filter components.
- MUST NOT copy CCM layouts or recreate them using General colors.
- Components located in the GEMS Figma file are not automatically approved for General products.

---

## 2. Purpose & Usage

Card Header organizes a card's primary identity, supporting information, and contextual actions.

It helps users understand what the card represents and what actions are available.

### When to Use

| Context | Recommendation |
|---|---|
| Information Card | Use when a distinct title and supporting context are needed |
| Management / Summary Card | Use for meaningful identity, status, or contextual actions |
| User / Employee Card | Consider `Avatar=True` when representing a person |
| Detail Section Card | Use when the section needs its own heading or actions |
| Dashboard Card | Use only when an explicit heading or action improves clarity |
| Form Section | Follow the official Form Section component |
| Simple KPI Card | Do not automatically add Card Header |
| Small Informational Card | Omit if the content is self-explanatory |
| Modal / Dialog | Follow dedicated dialog components |
| Page Header | Use the official Page Header component instead |

**Usage Rules**
- MUST determine whether Card Header is necessary based on the card's purpose.
- MUST follow relevant GEMS Page Samples and UX Patterns.
- MUST maintain consistency across cards with similar functions.
- MUST NOT add Card Header solely for decoration.
- MUST NOT use Card Header as Page Header, Navigation Bar, Form Section, or Table Header.

**Core Principle:** Not every Card requires a Card Header. Use it only when a clear identity, supporting context, or relevant action is needed.

---

## 3. Available Variants & Properties

The official GEMS General Card Header provides two verified properties:

| Property | Available Values |
|---|---|
| `Avatar` | `True`, `False` |
| `Breakpoint` | `Desktop`, `Mobile` |

### Official Variants

| Variant | Avatar | Breakpoint | Usage |
|---|---|---|---|
| 1 | `False` | `Desktop` | Text-based header for desktop |
| 2 | `True` | `Desktop` | Identity-based header with avatar for desktop |
| 3 | `False` | `Mobile` | Text-based header for mobile |
| 4 | `True` | `Mobile` | Identity-based header with avatar for mobile |

**Variant Rules**
- MUST select one of the four official configurations.
- MUST preserve original component instances and supported properties.
- MUST choose `Breakpoint` according to the target viewport.
- MUST choose `Avatar` according to content meaning, not visual preference.
- MUST NOT invent additional variants or manually combine existing variants.

### Avatar Selection

**Use `Avatar=True` when:**
- The card represents an identifiable person.
- A profile photo, initials, or official avatar fallback is relevant.
- The official GEMS pattern includes an avatar for the same context.

Examples: Employee, User, Team Member, PIC, Approver.

**Use `Avatar=False` when:**
- The card represents general information or a section.
- The content does not require a personal identity.
- An avatar would add no meaningful information.

Examples: Configuration, Summary, General Details, Informational Sections.

Do not use a person's avatar as decoration. Product or organization identity MUST follow the appropriate GEMS Logo guidelines.

---

## 4. Component Anatomy

Preserve the original General Card Header structure.

| Element | Usage Rule |
|---|---|
| Title / Primary Text | Clearly identifies the card subject |
| Supporting Text | Adds relevant context without repeating the title |
| Avatar | Use only with the appropriate official variant |
| Badge | Use for meaningful supporting information or status |
| Action Buttons | Include only when required by the product workflow |
| More Actions | Use when supported for additional contextual actions |
| Divider / Boundary | Preserve the official component specification |

These are conditional content patterns. **Not every Card Header must contain every element.**

### Title & Supporting Text

- MUST use official GEMS Text Styles.
- MUST preserve title and supporting-text hierarchy.
- MUST use concise, product-specific wording.
- MUST follow supported wrapping or truncation behavior.
- MUST NOT manually adjust typography to fit content.
- MUST NOT copy sample text as actual product content.

### Badge

- MUST use official GEMS Badge components.
- MUST follow `badge.md` and `Foundation/color.md`.
- SHOULD use Badge only when the information has a meaningful classification, status, or supporting context.
- MUST NOT create arbitrary status labels or decorative badges.

### Avatar

- MUST use the official GEMS Avatar component.
- MUST preserve the avatar's original size and positioning within Card Header.
- MUST follow official fallback behavior when no image is available.
- MUST NOT manually insert an avatar into the `Avatar=False` variant.

---

## 5. Actions & Button Hierarchy

Card Header MAY contain contextual actions. **Buttons are optional, not mandatory.**

AI MUST determine actions based on the card's purpose, user task, and permissions.

### Action Selection

| Context | Recommendation |
|---|---|
| Informational content only | No action required |
| One important action | Use the appropriate official GEMS Button |
| Multiple actions | Follow the supported GEMS action hierarchy |
| Optional / Additional actions | Use supported secondary or overflow actions |
| Destructive action | Follow official destructive and confirmation patterns |
| Action exists elsewhere | Avoid unnecessary duplication |

### Action Rules

- MUST use official GEMS Button and Dropdown components.
- MUST preserve supported button variants, dimensions, and placement.
- MUST prioritize actions based on actual workflow importance.
- MUST respect user permissions and available product features.
- MUST use clear, meaningful action labels.
- MUST NOT add Primary, Secondary, or Tertiary actions merely because they appear in the sample.
- MUST NOT invent actions or duplicate existing functionality.
- MUST NOT expose destructive actions without the required confirmation behavior.

**Core Principle:** Button quantity and priority MUST follow user needs—not the number of buttons displayed in the Figma example.

---

## 6. Responsive Behavior

Use the official `Breakpoint` property.

### Desktop

- MUST use `Breakpoint=Desktop`.
- MUST preserve the original desktop layout, alignment, spacing, and dimensions.
- MUST maintain readable content and accessible actions.
- MUST follow the official component's supported behavior.

### Mobile

- MUST use `Breakpoint=Mobile`.
- MUST preserve the original mobile hierarchy and action placement.
- MUST follow supported text wrapping and responsive layout.
- MUST keep important information and actions accessible.
- MUST maintain suitable interactive target sizes.

**Responsive Restrictions**
- MUST NOT manually resize the Desktop variant to imitate Mobile.
- MUST NOT create custom breakpoints or responsive variants.
- MUST NOT remove essential content or actions without an approved alternative.
- MUST NOT invent unsupported mobile layouts.

If a required responsive behavior is unavailable in GEMS, request Human Approval before creating an alternative.

---

## 7. States & Interaction

Card Header is primarily a structural component. Interactive states are controlled by its nested GEMS components.

| Element | Required Behavior |
|---|---|
| Button | Follow official Button states and interactions |
| More Actions / Menu | Follow official Dropdown/Menu behavior |
| Badge | Preserve semantic meaning and supported appearance |
| Avatar | Follow official Avatar behavior |
| Other Interactive Elements | Follow their corresponding GEMS specifications |

**Interaction Rules**
- MUST preserve Default, Hover, Focus, Disabled, and Loading states when supported.
- MUST maintain appropriate keyboard access and visible focus indicators.
- MUST prevent disabled actions from being triggered.
- MUST use official loading feedback when applicable.
- MUST NOT invent custom Card Header interaction states.
- MUST NOT make the entire Card Header clickable unless the approved GEMS pattern supports it.
- MUST NOT turn static text, badges, or avatars into interactive elements without a defined requirement.

---

## 8. Content & Contextual Application

AI MUST adapt Card Header content to the actual product rather than copying Figma sample data.

### Content Decision Rules

1. Identify the card's purpose and data.
2. Determine whether Card Header is necessary.
3. Select the appropriate `Avatar` and `Breakpoint` configuration.
4. Define meaningful primary and supporting information.
5. Include Badge only when relevant.
6. Include actions only when required and permitted.
7. Follow GEMS Page Samples and UX Patterns for contextual application.

### Usage Examples

| Card Type | Header Content | Avatar | Actions |
|---|---|---|---|
| Employee Card | Name and relevant employee information | When identity is relevant | Based on permissions |
| Information Card | Title and optional description | No | Optional |
| Management Card | Entity name and supporting context | Context-dependent | Based on workflow |
| Detail Section Card | Section title and relevant description | Usually no | Only when needed |
| Dashboard Card | Data category and contextual information | Usually no | Only when useful |

These examples describe content-selection logic, not fixed templates or additional GEMS variants.

**Content Rules**
- Use terminology consistent with HSD/BRD.
- Do not invent data, roles, actions, or status labels.
- Keep related Card Headers consistent across the application.
- Avoid unnecessary information that reduces readability.
- Preserve important information across supported breakpoints.

---

## 9. Foundation & Component Dependencies

Card Header MUST follow the existing GEMS guidelines.

### Foundation

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | Official General brand and semantic colors |
| `Foundation/typography.md` | Official GEMS Figma Text Styles |
| `Foundation/spacing-dan-radius.md` | Spacing, dimensions, and radius tokens |
| `Foundation/effect-styles.md` | Borders, dividers, shadows, and effects |
| `Foundation/icons.md` | Standard icons and official sizes |
| `Foundation/misc-icons.md` | Special-purpose icons when applicable |
| `Foundation/logo.md` | Product identity and logo usage |
| `Foundation/design-annotations.md` | Relevant GEMS component and layout annotations |

### Related Components

When applicable, follow the corresponding component guidelines:

- `button.md`
- `avatar.md`
- `badge.md`
- `dropdown.md`
- `tooltip.md`

Use the actual repository filename if different.

**Dependency Rules**
- MUST use official GEMS General semantic color tokens.
- MUST apply complete existing GEMS Text Styles.
- MUST preserve official spacing, radius, borders, and effects.
- MUST use official nested component sizes and variants.
- MUST NOT hardcode HEX/RGB/HSL or unsupported typography and spacing values.
- MUST NOT add shadows simply because content is placed inside a card.
- MUST NOT override nested component specifications.
- MUST NOT introduce CCM-specific components or styling.

---

## 10. Accessibility

Card Header implementations MUST:

- Preserve clear content hierarchy.
- Maintain readable typography and adequate contrast.
- Provide accessible names for interactive elements.
- Support keyboard navigation for available controls.
- Maintain visible focus indicators.
- Avoid relying solely on color to communicate meaning.
- Provide appropriate alternatives for avatar content.
- Maintain usable actions on supported breakpoints.
- Follow the project's accessibility requirements.

---

## 11. Strict Rules

### MUST

- Use the official **GEMS General Card Header**.
- Select one of the four supported `Avatar` × `Breakpoint` variants.
- Determine whether Card Header is necessary.
- Preserve original component structure and properties.
- Follow GEMS Page Samples and UX Patterns.
- Adapt content and actions to HSD/BRD and user permissions.
- Use official GEMS nested components.
- Apply all relevant Foundation guidelines.
- Maintain consistency between cards with similar functions.

### MUST NOT

- Use `Card header CCM` or CCM-specific Filter components.
- Copy CCM visual or interaction patterns into General products.
- Create custom Card Header variants or unsupported layouts.
- Recreate official components using detached frames.
- Modify original dimensions, typography, colors, or spacing.
- Add unnecessary avatars, badges, icons, or buttons.
- Invent data, permissions, actions, or status values.
- Use Card Header as Page Header, Navigation Bar, Table Header, or Form Section.
- Introduce unsupported responsive behavior or interaction states.
- Detach or duplicate official component instances when reusable instances are available.

---

## 12. AI Implementation Instructions

When generating UI using GEMS:

1. **Identify Purpose:** Determine whether the card needs a dedicated header.
2. **Retrieve Official Component:** Use General Card Header at node `240:15290`; exclude CCM.
3. **Select Variant:** Choose `Avatar=True/False` and `Breakpoint=Desktop/Mobile`.
4. **Adapt Content:** Use product-specific titles, supporting information, and relevant badges.
5. **Determine Actions:** Add only required actions using official GEMS components.
6. **Apply GEMS Specifications:** Preserve original properties and follow Foundation dependencies.
7. **Reference Context:** Follow relevant Page Samples and UX Patterns for usage and placement.

**Human Approval Required When:**
- A necessary layout cannot be represented by official variants.
- A required interaction has no suitable GEMS component.
- Responsive behavior is unsupported by the available specifications.
- Product requirements conflict with the official component design.

Combine related clarification questions into one confirmation whenever possible.

If the official component cannot be accessed, request the necessary Figma access or specifications. Do not invent component details.

---

## Final Instruction

**AI MUST use the official GEMS General Card Header, select the correct Avatar and Breakpoint configuration, and adapt content and actions to the product's actual requirements.**

**Card Header CCM and all CCM-specific patterns are strictly prohibited.**

**Not every Card needs a Card Header, and not every Card Header needs an Avatar, Badge, or Button.**

**GEMS Design System is the single source of truth for Card Header visual specifications and supported interaction behavior.**
