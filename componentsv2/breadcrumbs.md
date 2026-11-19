
# GEMS Design System — Components / Breadcrumbs

> **MANDATORY:** All Breadcrumb navigation MUST use official GEMS General Breadcrumbs components, supported variants, and original component properties. Breadcrumbs-CCM and CCM-specific navigation patterns are strictly prohibited.

## 1. Sources & Priority

**Official References**
- [GEMS Breadcrumbs](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-38024)
- [GEMS Breadcrumb Button Base](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-40864)
- [GEMS General Breadcrumbs Variants](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-40937)
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1105-7310)

**Priority Order**
1. **Official General Breadcrumbs:** Source of truth for structure, variants, properties, dimensions, and visual specifications.
2. **GEMS Application Navigation & Page Header:** Define the surrounding navigation and page hierarchy.
3. **GEMS Components & Foundation:** Define icons, typography, colors, and interaction states.
4. **Page Samples & UX Patterns:** Reference for contextual application.
5. **HSD/BRD:** Define product modules, page hierarchy, routes, and user permissions.
6. **General UI/UX Principles:** Fallback only when GEMS provides no specific guidance.

**Component Restrictions**
- MUST use General Breadcrumbs at node `240:40937`.
- MUST use official `_Breadcrumb button base` when applicable.
- MUST NOT use `Breadcrumbs-CCM` or CCM-specific navigation patterns.
- MUST NOT copy CCM Breadcrumb layouts and recreate them using General colors.
- MUST NOT use custom Breadcrumb components when official GEMS components are available.

---

## 2. Purpose & Usage

Breadcrumbs shows the current page's location within the application's navigation hierarchy.

It helps users:
- Understand their current location.
- Recognize parent pages or sections.
- Navigate back to accessible parent levels.
- Understand relationships between nested pages.

### When to Use

| Context | Recommendation |
|---|---|
| Nested Detail Page | Use when parent hierarchy is meaningful |
| Deep Management Page | Use when multiple navigation levels exist |
| Settings Subpage | Use when the page belongs to a structured hierarchy |
| Nested Configuration Page | Use when parent navigation improves orientation |
| Main Dashboard | Usually omit |
| Top-level Module Page | Usually omit |
| Standalone Page | Follow the approved page layout |
| Modal / Dialog | Do not add Breadcrumbs |
| Multi-step Form | Use Progress Steps when appropriate |
| Tab Navigation | Use official Tabs |
| Application Navigation | Use the official Application Navigation component |

### Usage Rules

- MUST determine whether Breadcrumbs improves navigation clarity.
- MUST represent the actual information hierarchy.
- MUST use meaningful labels matching the product terminology.
- MUST follow relevant GEMS Page Samples and UX Patterns.
- MUST keep Breadcrumbs consistent across pages with equivalent hierarchy.
- MUST NOT add Breadcrumbs solely for decoration.
- MUST NOT automatically add Breadcrumbs to every page.

**Core Principle:** Breadcrumbs represents hierarchical location, not browsing history.

---

## 3. Available Breadcrumbs Variants

**Official Component:** `Breadcrumbs`  
**Figma Node:** `240:40937`

### Available Properties

| Property | Available Values |
|---|---|
| `Divider` | `Slash`, `Chevron` |
| `Type` | `Text`, `Text with line`, `Button brand`, `Button gray` |
| `Breakpoint` | `Desktop`, `Mobile` |

The official GEMS component provides **16 configurations**.

### Official Variants

| Divider | Type | Breakpoint |
|---|---|---|
| `Slash` | `Text` | `Desktop` |
| `Slash` | `Text with line` | `Desktop` |
| `Slash` | `Button brand` | `Desktop` |
| `Slash` | `Button gray` | `Desktop` |
| `Chevron` | `Text` | `Desktop` |
| `Chevron` | `Text with line` | `Desktop` |
| `Chevron` | `Button brand` | `Desktop` |
| `Chevron` | `Button gray` | `Desktop` |
| `Slash` | `Text` | `Mobile` |
| `Slash` | `Text with line` | `Mobile` |
| `Slash` | `Button brand` | `Mobile` |
| `Slash` | `Button gray` | `Mobile` |
| `Chevron` | `Text` | `Mobile` |
| `Chevron` | `Text with line` | `Mobile` |
| `Chevron` | `Button brand` | `Mobile` |
| `Chevron` | `Button gray` | `Mobile` |

### Variant Rules

- MUST select one of the 16 official configurations.
- MUST use the supported Divider, Type, and Breakpoint properties.
- MUST preserve original component structure and visual properties.
- MUST maintain consistency within the same Application Shell.
- MUST NOT create additional Types or custom Dividers.
- MUST NOT manually combine different variants.
- MUST NOT change visual properties outside GEMS.

---

## 4. Breadcrumb Type Selection

Select Type according to the approved product pattern and required visual hierarchy.

| Type | Usage |
|---|---|
| `Text` | Standard text-based hierarchical navigation |
| `Text with line` | Text-based navigation using the official line-separated presentation |
| `Button brand` | Official brand-emphasis Breadcrumb presentation |
| `Button gray` | Official neutral-emphasis Breadcrumb presentation |

### Type Rules

- MUST choose a Type that matches the relevant GEMS Page Sample or approved layout.
- MUST preserve the official visual treatment of the selected Type.
- MUST maintain consistent presentation across related pages.
- MUST use official General brand and semantic colors.
- MUST NOT choose `Button brand` merely to make Breadcrumbs more visually prominent.
- MUST NOT substitute custom Buttons for official Breadcrumb elements.
- MUST NOT mix different Breadcrumb Types within one navigation sequence unless supported by the original component.

### Divider Selection

| Divider | Usage |
|---|---|
| `Slash` | Hierarchical separation using the official slash divider |
| `Chevron` | Hierarchical separation using the official directional divider |

- MUST use official divider assets and spacing.
- MUST preserve consistent divider usage across the sequence.
- MUST NOT invent additional divider icons or symbols.
- MUST NOT change divider colors or dimensions manually.

---

## 5. Breadcrumb Button Base

**Official Component:** `_Breadcrumb button base`  
**Figma Node:** `240:40864`

### Available Properties

| Property | Available Values |
|---|---|
| `Current` | `True`, `False` |
| `Type` | `Text`, `Button brand`, `Button gray` |
| `Icon` | `True`, `False` |
| `State` | `Default`, `Hover`, `Focused` |

The official component provides **36 configurations**.

### Property Rules

**Current**
- Use `Current=True` for the current destination.
- Use `Current=False` for parent destinations.
- MUST NOT mark multiple locations as Current within one Breadcrumb trail.

**Type**
- MUST match the selected Breadcrumb presentation.
- MUST preserve official styling.

**Icon**
- Use `Icon=True` only when the official pattern requires an icon.
- Use `Icon=False` when an icon adds no meaningful value.
- MUST use official GEMS Icons and sizes.
- MUST NOT add decorative icons to every level automatically.

**State**
- MUST preserve official Default, Hover, and Focused visuals.
- MUST NOT invent custom active or hover styles.
- MUST NOT assume a visual state automatically authorizes navigation behavior.

---

## 6. Breadcrumb Hierarchy & Structure

Breadcrumbs MUST reflect the actual parent-child relationship between pages.

### Recommended Structure

`Parent → Child → Current Page`

Example:

`Settings / User Management / User Detail`

This example illustrates hierarchy only. The actual labels MUST follow product terminology and available routes.

### Hierarchy Rules

- MUST arrange levels from the highest relevant parent to the current page.
- MUST represent the correct navigation hierarchy.
- MUST identify the current page accurately.
- MUST use the same terminology as Application Navigation and Page Header.
- MUST ensure each parent destination resolves to a valid, permitted route.
- MUST NOT display unrelated modules as ancestors.
- MUST NOT generate hierarchy from the order of previously visited pages.
- MUST NOT invent parent pages that do not exist.

### Current Page

- MUST display the current destination according to the official GEMS Current variant.
- SHOULD avoid redundant navigation to the already active page.
- MUST preserve the current-page semantic indication.
- MUST NOT create multiple conflicting active destinations.

---

## 7. Relationship with Other Components

Breadcrumbs complements existing navigation components. It does not replace them.

| Component | Responsibility |
|---|---|
| Application Navigation | Main application modules and navigation hierarchy |
| Navigation Bar | Top-level application navigation and global controls |
| Breadcrumbs | Current page location within a hierarchy |
| Page Header | Page identity, description, and contextual actions |
| Tabs | Switching between related content views |
| Progress Steps | Structured sequential process stages |

### Integration Rules

- MUST follow `Foundation/application-navigation` for product navigation structure.
- MUST maintain consistency with the Page Header title.
- MUST follow the approved Application Shell.
- MUST preserve the official Breadcrumb placement in GEMS Page Samples.
- MUST NOT use Breadcrumbs as a duplicate Sidebar or Navigation Bar.
- MUST NOT use Breadcrumbs for tabs or step-based workflows.
- MUST NOT add multiple competing Breadcrumb trails.

**Core Principle:** Application Navigation answers "Where can I go?" Breadcrumbs answers "Where am I within this hierarchy?"

---

## 8. Breadcrumbs in CRUD Workflows

Breadcrumbs MAY support CRUD workflows when they involve nested pages.

### Usage Matrix

| CRUD Context | Recommendation |
|---|---|
| Create Page | Use only when the page hierarchy benefits from Breadcrumbs |
| Read / Detail Page | Use when users need parent-page navigation |
| Edit Page | Use when navigation back to parent context is meaningful |
| Delete Confirmation | Do not use Breadcrumbs inside the Modal |
| List / Table Page | Usually omit if already a top-level module |
| Nested List | Use when the parent hierarchy is meaningful |

### Create & Edit

- MUST preserve the correct parent hierarchy.
- MUST NOT treat Breadcrumb navigation as Save or Cancel.
- MUST follow the approved unsaved-changes behavior when users navigate away.
- MUST NOT discard entered data without appropriate confirmation.

### Detail Page

- MAY provide navigation to the parent list or management page.
- MUST use valid routes and authorized destinations.
- MUST NOT invent intermediate hierarchy levels.

### Delete

- MUST use official GEMS Button and Modal patterns.
- MUST NOT use Breadcrumbs as a destructive action control.
- MUST NOT add a Breadcrumb trail inside Delete Confirmation.

---

## 9. Long Hierarchies & Truncation

Deep navigation hierarchies may require a compact presentation.

The official GEMS examples show a compact representation using an ellipsis for intermediate levels.

### Rules

- MUST preserve the actual hierarchy.
- MUST keep the current destination identifiable.
- MUST follow the official GEMS compact presentation when applicable.
- MUST preserve access to required parent destinations according to the approved interaction pattern.
- MUST NOT invent an arbitrary maximum number of Breadcrumb items.
- MUST NOT remove essential hierarchy information without an approved alternative.
- MUST NOT create a custom overflow menu without a supported GEMS pattern.

If a required hierarchy cannot be represented by an official variant, request Human Approval.

---

## 10. Desktop & Mobile Behavior

### Desktop

- MUST use `Breakpoint=Desktop`.
- MUST preserve official alignment, spacing, typography, and divider placement.
- MUST maintain a clear hierarchy and readable labels.
- MUST use the approved Breadcrumb Type.

### Mobile

- MUST use `Breakpoint=Mobile`.
- MUST preserve the official responsive presentation.
- MUST maintain identification of the current page.
- MUST use supported compact hierarchy behavior when applicable.
- MUST preserve accessible navigation to relevant parent destinations.

### Responsive Restrictions

- MUST NOT manually shrink Desktop variants to imitate Mobile.
- MUST NOT invent custom breakpoints or responsive layouts.
- MUST NOT hide the current page label without an approved pattern.
- MUST NOT create unsupported horizontal scrolling or overflow behavior.
- MUST NOT replace Breadcrumbs with custom mobile navigation without Human Approval.

---

## 11. Interaction & Accessibility

### Interaction Rules

- Parent Breadcrumb items MUST navigate to their intended destinations.
- The current destination MUST be represented accurately.
- Hover and Focused states MUST follow GEMS.
- Navigation MUST respect user roles and permissions.
- Invalid or inaccessible destinations MUST NOT be exposed as functional links.
- Breadcrumbs MUST NOT execute CRUD actions.

### Accessibility

Breadcrumbs MUST:

- Use appropriate breadcrumb navigation semantics.
- Provide an accessible label for the navigation region.
- Identify the current page programmatically.
- Support keyboard navigation for interactive ancestors.
- Preserve visible focus indicators.
- Use meaningful accessible names for icon-only links.
- Maintain readable typography and contrast.
- Avoid relying solely on color to indicate the current page.
- Treat decorative dividers as non-interactive.

---

## 12. Foundation & Component Dependencies

Breadcrumbs MUST follow existing GEMS guidelines.

### Foundation

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | Official General and semantic colors |
| `Foundation/typography.md` | Official GEMS Figma Text Styles |
| `Foundation/spacing-dan-radius.md` | Spacing, dimensions, and radius |
| `Foundation/effect-styles.md` | Borders, focus rings, and effects |
| `Foundation/icons.md` | Official navigation and divider icons |
| `Foundation/application-navigation` | Product navigation hierarchy |
| `Foundation/design-annotations.md` | Relevant component and layout annotations |

### Related Components

Follow corresponding GEMS guidelines when applicable:

- `page-header.md`
- `navigation-bar.md`
- `button.md`
- `dropdown.md`
- `modal.md`
- `progress-steps.md`

Use the repository's actual filenames if different.

### Dependency Rules

- MUST use official GEMS General color tokens.
- MUST apply complete existing Text Styles.
- MUST preserve official spacing, radius, borders, and effects.
- MUST use official GEMS icon assets and sizes.
- MUST preserve original component instances where supported.
- MUST NOT hardcode HEX/RGB/HSL or unsupported typography and spacing values.
- MUST NOT introduce CCM-specific styling or components.
- MUST NOT override original component properties.

---

## 13. Strict Rules

### MUST

- Use official GEMS General Breadcrumbs.
- Select one of the 16 supported main configurations.
- Use supported Breadcrumb Button Base properties.
- Determine whether Breadcrumbs is necessary.
- Represent the correct page hierarchy.
- Identify the current page accurately.
- Preserve valid parent navigation.
- Follow Application Navigation and Page Header hierarchy.
- Follow GEMS Page Samples and UX Patterns.
- Apply all relevant Foundation guidelines.

### MUST NOT

- Use `Breadcrumbs-CCM` or CCM-specific patterns.
- Create custom Breadcrumb components or dividers.
- Recreate official instances with detached frames.
- Modify original dimensions, colors, typography, or spacing.
- Add Breadcrumbs automatically to every page.
- Use browsing history as the Breadcrumb hierarchy.
- Invent parent pages or invalid routes.
- Display multiple conflicting current-page states.
- Use Breadcrumbs as Tabs, Progress Steps, or Application Navigation.
- Use Breadcrumbs to perform CRUD actions.
- Introduce unsupported responsive or overflow behavior.
- Override original GEMS component specifications.

---

## 14. AI Implementation Instructions

When generating UI using GEMS:

1. **Identify Page Hierarchy:** Determine whether the page has meaningful parent destinations.
2. **Determine Necessity:** Use Breadcrumbs only when hierarchical navigation improves orientation.
3. **Retrieve Official Component:** Use General Breadcrumbs at node `240:40937`; exclude CCM.
4. **Select Configuration:** Choose supported Divider, Type, and Breakpoint values.
5. **Configure Items:** Use official Breadcrumb Button Base with correct Current, Icon, Type, and State properties.
6. **Apply Navigation:** Use actual product routes, hierarchy, and permissions from HSD/BRD.
7. **Preserve GEMS:** Follow official component properties, Foundation guidelines, Page Samples, and UX Patterns.

**Human Approval Required When:**
- The required hierarchy cannot be represented by an official GEMS variant.
- A necessary mobile or overflow behavior is unavailable.
- The product's parent navigation structure is ambiguous.
- The requested design conflicts with official component specifications.

Combine related clarification questions into one confirmation whenever possible.

If the official component or property cannot be accessed or verified, request the necessary Figma access or specifications. Do not invent unsupported details.

---

## Final Instruction

**AI MUST use official GEMS General Breadcrumbs, select supported variants, and represent the actual product navigation hierarchy.**

**Breadcrumbs MUST show hierarchical page location—not browsing history, CRUD actions, or workflow progress.**

**Do not automatically add Breadcrumbs to every page. Use them only when the hierarchy benefits the user.**

**Breadcrumbs-CCM, custom variants, unsupported styling, and invented navigation routes are strictly prohibited.**

**GEMS Design System is the single source of truth for Breadcrumbs visual specifications and supported interaction behavior.**
