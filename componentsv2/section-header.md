
# GEMS Design System — Components / Section Header

> **MANDATORY:** All section headings and supported section-level controls MUST use the official GEMS General Section Header or Section Label components. Preserve original component variants, layout, typography, spacing, and interaction behavior. Do not substitute custom or CCM-specific components.

## 1. Sources & Priority

**Official References**
- [GEMS Section Header](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-9302)
- [GEMS Section Header Variants](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-16028)
- [GEMS Section Label Variants](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-16144)
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1105-7310)

**Priority Order**
1. **Official GEMS Components:** Source of truth for variants, properties, dimensions, and visual specifications.
2. **GEMS Component Guidelines:** Follow specifications for Buttons, Button Groups, Input/Search, Tabs, and other nested elements.
3. **Page Samples & UX Patterns:** Reference for contextual placement and usage.
4. **Product Requirements (HSD/BRD):** Determine section content, actions, and permissions.
5. **General UI/UX Principles:** Fallback only when GEMS provides no specific guidance.

Official GEMS component specifications take precedence over visual preferences or generic UI conventions.

---

## 2. Purpose & Component Selection

Section Header introduces a content section and may provide contextual actions, search, or navigation tabs.

Section Label provides a more compact heading for smaller content groups or subsections.

### When to Use

| Context | Recommended Component |
|---|---|
| Main content section | Section Header |
| Data management section | Section Header when section-level controls are needed |
| Dashboard section | Section Header or Section Label based on hierarchy |
| Detail page subsection | Section Label or Section Header depending on complexity |
| Form subsection | Follow official Form Section; use Section Label only when appropriate |
| Small information group | Section Label |
| Section with search | Section Header — `Type=Search` |
| Section with grouped actions | Section Header — `Type=Button group` |
| Section with navigation tabs | Section Header — `Tabs=True` |
| Page title and global page actions | Page Header |
| Card identity and card-specific actions | Card Header |
| Table-specific controls | Follow official Data Table and related components |

**Usage Rules**
- MUST determine whether a Section Header or Section Label is necessary.
- MUST select the component according to content hierarchy and function.
- MUST follow relevant GEMS Page Samples and UX Patterns.
- MUST maintain consistency between sections with equivalent purposes.
- MUST NOT add headers merely to increase visual structure.
- MUST NOT use Section Header as Page Header, Card Header, Navigation Bar, or Table Header.

**Core Principle:** Section Header organizes a meaningful content area. Its controls must serve that section, not unrelated application-level functions.

---

## 3. Available Section Header Variants

**Official Component:** `Section header`  
**Figma Node:** `240:16028`

### Component Properties

| Property | Available Values |
|---|---|
| `Tabs` | `True`, `False` |
| `Type` | `Buttons`, `Button group`, `Search` |
| `Breakpoint` | `Desktop`, `Mobile` |

The official component provides **12 configurations**.

### Official Variants

| Tabs | Type | Breakpoint |
|---|---|---|
| `False` | `Buttons` | `Desktop` |
| `False` | `Button group` | `Desktop` |
| `False` | `Search` | `Desktop` |
| `True` | `Buttons` | `Desktop` |
| `True` | `Button group` | `Desktop` |
| `True` | `Search` | `Desktop` |
| `False` | `Buttons` | `Mobile` |
| `False` | `Button group` | `Mobile` |
| `False` | `Search` | `Mobile` |
| `True` | `Buttons` | `Mobile` |
| `True` | `Button group` | `Mobile` |
| `True` | `Search` | `Mobile` |

### Variant Selection Rules

- MUST use one of the 12 official configurations.
- MUST select `Breakpoint` according to the target viewport.
- MUST use `Tabs=True` only when section-level tabs are required.
- MUST use `Tabs=False` when the section does not require tabs.
- MUST select `Type` according to the actual purpose of the section controls.
- MUST preserve the original structure and component properties.
- MUST NOT invent additional Types, Tabs states, or responsive variants.

**Important:** The presence of a Type in Figma does not mean the associated control is mandatory for every section. Select a variant based on actual requirements; do not populate controls merely to imitate the example.

---

## 4. Section Header Type Selection

### Type: Buttons

Use when a section requires one or more independent contextual actions.

Examples:
- Add data to the current section.
- Export relevant section data.
- Open section-specific settings.
- Perform another approved section-level action.

**Rules**
- MUST use official GEMS Button variants.
- MUST prioritize actions according to workflow importance.
- MUST respect product permissions.
- MUST NOT add Primary, Secondary, or Tertiary actions solely because they appear in the sample.
- MUST NOT duplicate actions already provided by Page Header or another relevant component.

### Type: Button group

Use when multiple closely related options or actions belong to one logical group and the official GEMS Button Group pattern is appropriate.

Examples:
- Switching between supported presentation modes.
- Selecting a mutually related view or option.
- Performing grouped controls defined by the product.

**Rules**
- MUST use the official GEMS Button Group component.
- MUST preserve button grouping, spacing, and selected states.
- MUST use meaningful labels and consistent option structure.
- MUST NOT use Button Group for unrelated actions.
- MUST NOT replace an approved Tabs pattern with Button Group arbitrarily.

### Type: Search

Use when users need to search content belonging to the current section.

Examples:
- Searching employees in a team section.
- Searching items in a relevant management section.
- Searching records within a defined content area.

**Rules**
- MUST use the official GEMS Search/Input component.
- MUST ensure search applies to the correct content scope.
- MUST use meaningful placeholder text.
- MUST follow official input, focus, disabled, and search behavior.
- MUST NOT add search when the section has no meaningful searchable content.
- MUST NOT duplicate an existing search control serving the same scope.

---

## 5. Tabs Usage

The `Tabs` property controls whether the Section Header includes its supported tab-navigation structure.

### Use `Tabs=True` When

- The section contains multiple related content views.
- Users need to switch between those views.
- The tabs represent a meaningful organization of content.
- GEMS Page Samples or UX Patterns support the pattern.

### Use `Tabs=False` When

- The section contains a single content view.
- Tabs do not improve navigation.
- Existing navigation already covers the same function.
- The section only requires a heading and relevant controls.

**Tabs Rules**
- MUST use official GEMS tab components and supported states.
- MUST maintain a clear active selection.
- MUST display content corresponding to the selected tab.
- MUST preserve tab order and meaningful labels.
- MUST follow official desktop and mobile presentation.
- MUST NOT create tabs merely because `Tabs=True` is available.
- MUST NOT invent unsupported tab variants or manually restyle tabs.

**Mobile:** Follow the official GEMS Mobile variant, including its supported tab-selection presentation. Do not manually force the Desktop tab row into a narrow mobile layout.

---

## 6. Section Label

**Official Component:** `Section label`  
**Figma Node:** `240:16144`

Section Label is a compact heading component for smaller sections and information groups.

### Available Properties

| Property | Available Values |
|---|---|
| `Size` | `sm`, `md` |
| `Actions` | `True`, `False` |

### Official Variants

| Variant | Size | Actions |
|---|---|---|
| 1 | `sm` | `False` |
| 2 | `md` | `False` |
| 3 | `sm` | `True` |
| 4 | `md` | `True` |

### Usage Rules

- MUST use the official Section Label component when the smaller section-heading pattern is appropriate.
- MUST select `sm` or `md` according to hierarchy and available GEMS examples.
- MUST use `Actions=True` only when the subsection requires relevant actions.
- MUST use `Actions=False` for informational headings without actions.
- MUST preserve official typography, spacing, and layout.
- MUST NOT substitute custom heading text for an available official Section Label pattern.
- MUST NOT use Section Label as a replacement for a full Section Header when search, tabs, or more complex controls are required.

**Core Principle:** Use Section Header for more complex section organization and Section Label for compact section-level hierarchy.

---

## 7. Content & Anatomy

Preserve the official GEMS component structure.

| Element | Application Rule |
|---|---|
| Section Title | Clearly identifies the content section |
| Supporting Text | Provides context when relevant |
| Buttons | Use only for required section-level actions |
| Button Group | Use for related grouped controls |
| Search | Use when section content is searchable |
| Tabs | Use for switching between related section views |
| Section Label Actions | Use only for relevant subsection actions |
| Divider / Boundary | Follow the official component specification |

### Content Rules

- MUST use concise, descriptive section titles.
- MUST use supporting text only when it adds useful context.
- MUST maintain a clear hierarchy between Page Header, Section Header, Section Label, and Card Header.
- MUST use product terminology from HSD/BRD.
- MUST keep related sections consistent.
- MUST NOT copy placeholder labels such as `Text`, `Primary`, or sample titles as final product content.
- MUST NOT invent features, actions, tabs, or data categories.

### Hierarchy

| Level | Component | Responsibility |
|---|---|---|
| Page | Page Header | Identifies the current page |
| Section | Section Header | Organizes a major content area |
| Subsection | Section Label | Identifies a smaller information group |
| Card | Card Header | Identifies content within a specific card |

Use the hierarchy according to actual content structure. Do not force every page to contain all four levels.

---

## 8. Action Placement & Decision Rules

AI MUST determine whether section-level actions are needed.

| Situation | Recommended Behavior |
|---|---|
| Section has no available actions | Do not add unnecessary controls |
| Section requires an independent action | Select supported `Type=Buttons` |
| Section requires related grouped controls | Select `Type=Button group` |
| Section data needs searching | Select `Type=Search` |
| Section contains multiple related views | Use `Tabs=True` |
| Subsection requires a small action area | Use `Section Label` with `Actions=True` |
| Action is global to the page | Prefer Page Header |
| Action belongs to a single card | Prefer Card Header |
| Action belongs specifically to a table | Follow Data Table patterns |

**Action Rules**
- MUST follow official GEMS Button and Button Group guidelines.
- MUST keep primary actions aligned with the user's most important task.
- MUST maintain role-based access and permission rules.
- MUST use meaningful action labels.
- MUST avoid duplicate actions across header levels.
- MUST NOT add actions simply to fill available space.
- MUST NOT introduce destructive actions without the required confirmation behavior.

**Core Principle:** A Section Header may contain actions, but its primary purpose remains identifying and organizing section content.

---

## 9. Responsive Behavior

### Desktop

- MUST use `Breakpoint=Desktop` for Section Header.
- MUST preserve official alignment, dimensions, spacing, and control placement.
- MUST follow the original arrangement of title, description, controls, and tabs.
- MUST maintain clear hierarchy and readable content.

### Mobile

- MUST use `Breakpoint=Mobile`.
- MUST preserve the official mobile stacking, wrapping, and control arrangement.
- MUST maintain access to essential actions and navigation.
- MUST use the supported mobile tabs pattern.
- MUST NOT shrink the Desktop variant manually to simulate Mobile.

### Section Label

Section Label provides the verified `Size` and `Actions` properties. Do not invent a separate `Breakpoint` property for Section Label.

**Responsive Restrictions**
- MUST NOT create unsupported breakpoints or custom layouts.
- MUST NOT remove required actions or navigation without an approved alternative.
- MUST NOT introduce custom scrolling, overflow, or hidden controls without a GEMS reference.
- Request Human Approval when required responsive behavior is not covered by official specifications.

---

## 10. Interaction & States

Interactive behavior MUST follow the official nested GEMS components.

| Element | Required Behavior |
|---|---|
| Buttons | Official Button states |
| Button Group | Official selection and interaction behavior |
| Search | Official Input/Search states |
| Tabs | Official active, hover, and focus states |
| Section Label Actions | Official supported action behavior |

**Rules**
- MUST preserve available Default, Hover, Focus, Active, Disabled, and Loading states.
- MUST maintain clear active states for Tabs and selection-based controls.
- MUST ensure search affects its intended data scope.
- MUST prevent disabled controls from triggering actions.
- MUST use official feedback patterns for asynchronous operations.
- MUST NOT invent custom states, animations, or interactions.
- MUST NOT turn non-interactive section titles into clickable controls without a defined requirement.

---

## 11. Foundation & Component Dependencies

Section Header and Section Label MUST follow existing GEMS guidelines.

### Foundation

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | Official Brand General and semantic colors |
| `Foundation/typography.md` | Official GEMS Text Styles |
| `Foundation/spacing-dan-radius.md` | Spacing, dimensions, and radius |
| `Foundation/effect-styles.md` | Borders, dividers, and effects |
| `Foundation/icons.md` | Standard icons and official sizes |
| `Foundation/misc-icons.md` | Special-purpose icons when applicable |
| `Foundation/design-annotations.md` | Relevant layout and component annotations |

### Related Components

Follow the corresponding GEMS component guidelines whenever used:

- `button.md`
- `button-group.md`
- `input.md`
- `dropdown.md`
- `tooltip.md`
- `page-header.md`
- `card-header.md`

Use the repository's actual filenames if different.

**Dependency Rules**
- MUST use official GEMS General semantic colors.
- MUST apply complete existing GEMS Text Styles.
- MUST preserve official spacing, radius, and effect specifications.
- MUST use approved nested components and variants.
- MUST NOT hardcode HEX/RGB/HSL or unsupported typography, spacing, and dimension values.
- MUST NOT introduce CCM styling or CCM-specific components.
- MUST NOT override official nested component specifications.

---

## 12. Accessibility

Section Header and Section Label implementations MUST:

- Preserve semantic heading hierarchy.
- Maintain readable typography and adequate contrast.
- Provide accessible names for interactive controls.
- Support keyboard navigation for Buttons, Search, and Tabs.
- Maintain visible focus indicators.
- Clearly communicate active or selected states.
- Avoid relying on color alone to communicate meaning.
- Maintain usable controls across supported viewport sizes.
- Follow the project's accessibility requirements.

---

## 13. Strict Rules

### MUST

- Use official GEMS General Section Header or Section Label components.
- Select the appropriate component based on content hierarchy.
- Use one of the 12 official Section Header configurations.
- Use one of the 4 official Section Label configurations.
- Select Tabs, Type, Breakpoint, Size, and Actions according to actual requirements.
- Preserve original component structure, variants, and visual properties.
- Follow GEMS Page Samples and UX Patterns.
- Use official nested GEMS components.
- Apply relevant Foundation guidelines.
- Adapt section content and controls to product requirements.

### MUST NOT

- Use CCM-specific components or layouts.
- Create custom Section Header or Section Label variants.
- Recreate official components using detached or manual frames.
- Modify original dimensions, typography, colors, or spacing.
- Add unnecessary Buttons, Button Groups, Search, or Tabs.
- Use Tabs for unrelated actions or content.
- Duplicate controls already available at another hierarchy level.
- Invent product actions, data categories, permissions, or navigation.
- Use Section Header as Page Header, Card Header, or Table Header.
- Introduce unsupported responsive layouts or interaction states.
- Override official nested component specifications.

---

## 14. AI Implementation Instructions

When generating UI using GEMS:

1. **Identify Section Purpose:** Determine whether the content needs Section Header, Section Label, or no additional heading.
2. **Retrieve Official Component:** Use Section Header at node `240:16028` or Section Label at node `240:16144`.
3. **Select Configuration:** Choose only the supported properties appropriate to the content and viewport.
4. **Determine Controls:** Include Buttons, Button Group, Search, Tabs, or Actions only when required.
5. **Adapt Content:** Use meaningful titles, descriptions, labels, and actions from product requirements.
6. **Preserve GEMS:** Apply official component properties and related Foundation guidelines.
7. **Follow Contextual References:** Use GEMS Page Samples and UX Patterns for hierarchy, placement, and interaction.

**Human Approval Required When:**
- A required layout cannot be represented by official variants.
- A necessary combination of controls is unsupported by the available component properties.
- A required responsive behavior is not specified by GEMS.
- Product requirements conflict with an official component specification.

Combine related clarification questions into one confirmation whenever possible.

If the official component cannot be accessed or its behavior cannot be determined, request the necessary Figma access or specifications. Do not invent unsupported component details.

---

## Final Instruction

**AI MUST use official GEMS Section Header and Section Label components, select only supported variants, and adapt their content and controls to the actual product requirements.**

**Do not automatically add Buttons, Button Groups, Search, or Tabs. Select them only when they serve a meaningful user task.**

**Custom components, unsupported variants, and CCM-specific patterns are prohibited.**

**GEMS Design System is the single source of truth for Section Header and Section Label visual specifications and supported interaction behavior.**
