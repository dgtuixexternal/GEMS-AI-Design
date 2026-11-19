
# GEMS Design System — Components / Navigation Bar

> **MANDATORY:** All application Navigation Bars MUST use the official GEMS General Navbar component. Preserve its original component structure, properties, variants, and visual specifications. CCM components are strictly prohibited.

## 1. Sources & Priority

**Official References**
- [GEMS Navigation Bar](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=410-344)
- [GEMS General Navbar](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=410-2009)
- [GEMS Application Navigation](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=345-1601)
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1105-7310)

**Priority Order**
1. **GEMS General Navbar:** Source of truth untuk component structure, variants, properties, dimensions, dan visual appearance.
2. **GEMS Application Navigation:** Source of truth untuk navigasi samping dan hubungannya dengan Navbar.
3. **GEMS Page Samples & UX Patterns:** Referensi penerapan Navbar pada halaman dan alur pengguna.
4. **Product Requirements (HSD/BRD):** Menentukan menu, informasi, akses pengguna, dan tindakan yang relevan.
5. **General UI/UX Principles:** Fallback hanya jika tidak bertentangan dengan GEMS.

Jika terdapat perbedaan, official GEMS component specifications memiliki prioritas tertinggi untuk visual dan interaction behavior.

**Component Restriction**
- MUST use the **General Navbar** at node `410:2009`.
- MUST NOT use `Navbar CCM`, CCM variants, or CCM-specific navigation patterns.
- MUST NOT use `Menu Request` or another separate component as a substitute for the official General Navbar.
- A component being located inside the GEMS Figma file does NOT automatically make it approved for General products.

---

## 2. Purpose & Usage

Navigation Bar merupakan bagian dari **Application Shell** yang menyediakan navigasi atau tindakan global pada bagian atas aplikasi.

Navbar harus konsisten dengan Application Navigation, struktur halaman, dan kebutuhan produk.

### When to Use

| Context | Usage |
|---|---|
| Dashboard | Use when the approved Application Shell includes Navbar |
| Management / List Page | Follow the existing Application Shell |
| Detail Page | Preserve Navbar from the parent layout |
| Create / Edit Page | Use when part of the main application layout |
| Reports / Analytics | Follow the approved Application Shell |
| Settings / Configuration | Follow the approved Application Shell |
| Authentication | Use the dedicated Authentication layout |
| Modal / Dialog / Overlay | Do not create an additional Navbar |
| Standalone / Public Page | Follow its approved layout |

**Usage Rules**
- MUST use Navbar when required by the approved Application Shell.
- MUST preserve Navbar consistency across pages using the same shell.
- MUST adapt navigation content to the product, user role, and available features.
- MUST NOT automatically add Navbar to every page or frame.
- MUST NOT create multiple Navbars within the same Application Shell.
- MUST NOT use Navbar as a replacement for Tabs, Breadcrumbs, Table Toolbar, or Application Navigation.

**Core Principle:** Navbar is a shared application-level component, not a decorative element or a page-specific toolbar.

---

## 3. Official Variants & Properties

The official GEMS General Navbar provides two component properties:

| Property | Available Values |
|---|---|
| `Open` | `true`, `false` |
| `Sidebar` | `Open`, `Closed` |

### Available Configurations

| Configuration | Open | Sidebar |
|---|---|---|
| 1 | `true` | `Open` |
| 2 | `true` | `Closed` |
| 3 | `false` | `Open` |
| 4 | `false` | `Closed` |

**Variant Rules**
- MUST select one of these four official configurations.
- MUST preserve the original GEMS component instance and property references when supported.
- MUST use `Sidebar=Open` when Application Navigation is expanded.
- MUST use `Sidebar=Closed` when Application Navigation is collapsed.
- MUST synchronize Navbar configuration with the actual navigation state.
- MUST NOT create additional variants or manually combine existing variants.

### Understanding `Open`

`Open` and `Sidebar` are separate properties.

- `Sidebar` represents the corresponding Application Navigation condition.
- `Open` MUST follow the behavior defined by the official Navbar component.

**Do not assume** `Open=true` means the sidebar, dropdown, notification, or another menu is open without confirming the component's actual behavior in Figma.

If the meaning of `Open` cannot be determined from the official component or its prototype, request clarification instead of inventing interaction behavior.

---

## 4. Navbar Anatomy & Content

Use the official General Navbar structure without rebuilding or modifying its internal layout.

| Element | Application Rule |
|---|---|
| Navbar Container | Preserve official size, background, border, padding, and alignment |
| Navigation Elements | Use only structures and properties supported by GEMS |
| Product Identity | Follow `Foundation/logo.md` when logo placement is supported |
| Icons | Follow official GEMS icon components |
| Buttons / Actions | Use official GEMS Button variants when required |
| Interactive Controls | Preserve available component states and behavior |
| Sidebar Integration | Match the current Application Navigation state |

The table describes rules for elements **when present or supported**. It does not require every Navbar to contain all elements.

### Content Selection

AI MUST determine Navbar content from:

1. Product purpose and module structure.
2. HSD/BRD and approved feature requirements.
3. Current user's role and permissions.
4. Existing Application Navigation hierarchy.
5. Relevant GEMS Page Samples and UX Patterns.

**Content Rules**
- Use meaningful labels that match the product terminology.
- Display only navigation or global actions relevant to the application.
- Respect role-based access and feature availability.
- Keep shared Navbar content consistent across related pages.
- Avoid duplicating functions already provided by Application Navigation or Page Header.
- Do not invent modules, menu items, permissions, notifications, or actions.

### Conditional Elements

Search, notifications, profile/avatar, menus, and action buttons MAY be used only when:

- The feature is required by the product.
- Its placement is supported by the official GEMS layout.
- The corresponding GEMS component exists.
- Its interaction and destination are defined.

**Do not add controls merely to make the Navbar look complete.**

---

## 5. Relationship with Application Navigation

Navbar and Application Navigation are different components within the same Application Shell.

| Component | Primary Responsibility |
|---|---|
| **Navigation Bar** | Top-level application navigation and supported global controls |
| **Application Navigation** | Product modules, menu hierarchy, and side navigation |
| **Page Header** | Current page identity, description, and contextual page actions |

### Integration Rules

- MUST use the official GEMS **Application Navigation**, not the separate Sidebar component.
- MUST synchronize `Sidebar=Open/Closed` with Application Navigation's actual expanded/collapsed state.
- MUST preserve the official spacing, alignment, and relationship between these components.
- MUST maintain consistent layout when navigation state changes.
- MUST keep page content aligned with the approved Application Shell.
- MUST follow `Foundation/application-navigation` for menu hierarchy, active menu, and product-specific navigation.

**MUST NOT**
- Rebuild Application Navigation inside Navbar.
- Replace Application Navigation with a custom Sidebar.
- Duplicate the same navigation hierarchy without a documented GEMS pattern.
- Create custom offsets, widths, or alignment rules to compensate for an incorrect variant.
- Use CCM navigation components or CCM styling.

### Navigation Consistency

When the user changes pages or modules:

- Current navigation must reflect the active route.
- Navbar and Application Navigation must remain synchronized.
- User permissions must continue to apply.
- Navigation state must remain consistent with the approved application behavior.

---

## 6. Interaction & States

Navbar controls MUST use interaction states provided by their original GEMS components.

| State | Usage |
|---|---|
| Default | Normal appearance and behavior |
| Hover | Feedback for supported interactive elements |
| Focus | Visible keyboard focus |
| Active / Selected | Indicates current route or selection when applicable |
| Pressed | Feedback during supported interaction |
| Disabled | Unavailable action; must not remain interactive |
| Loading | Use only where the supporting component provides it |

**Rules**
- Use only states supported by the specific GEMS component.
- Follow the actual active route; do not indicate conflicting active destinations.
- Preserve official hover, focus, selected, disabled, and loading visuals.
- Prevent repeated actions during loading when relevant.
- Do not claim an action succeeded before completion.
- Do not invent custom interaction states, animations, or feedback.
- Do not use Disabled as a substitute for Active.

For nested controls, follow their corresponding component guidelines rather than overriding their behavior from Navbar.

---

## 7. Layout & Responsive Behavior

### Layout

- MUST position Navbar according to the official Application Shell.
- MUST preserve official height, width behavior, padding, alignment, and spacing.
- MUST maintain consistent placement across pages sharing the same shell.
- MUST prevent overlap with Application Navigation and page content.
- MUST follow documented fixed, sticky, or scrolling behavior when available.

**MUST NOT**
- Resize or reconstruct Navbar manually.
- Apply unsupported fixed/sticky positioning.
- Add custom spacing or offsets outside GEMS.
- Modify internal component structure to solve layout issues.

### Desktop, Tablet & Mobile

- Use the official GEMS responsive implementation when available.
- Preserve navigation hierarchy and access to essential functions.
- Use supported component variants and responsive patterns.
- Keep Navbar and Application Navigation behavior consistent.

The verified `Open` and `Sidebar` properties are **not** responsive breakpoint properties.

**MUST NOT**
- Assume desktop variants automatically define mobile behavior.
- Invent breakpoints or responsive variants.
- Create a custom hamburger menu or mobile Navbar without an approved reference.
- Hide required navigation features without an approved alternative.

**Human Approval:** If a required responsive behavior is not defined in GEMS or an approved product sample, request approval before creating an alternative.

---

## 8. Foundation & Component Dependencies

Navbar MUST follow the existing GEMS guidelines.

### Foundation

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | Official General brand and semantic colors |
| `Foundation/typography.md` | Official GEMS Figma Text Styles |
| `Foundation/spacing-dan-radius.md` | Spacing, dimensions, and radius tokens |
| `Foundation/effect-styles.md` | Borders, shadows, and effects when specified |
| `Foundation/icons.md` | Standard navigation and action icons |
| `Foundation/misc-icons.md` | Special-purpose icons when applicable |
| `Foundation/logo.md` | Product logo selection and usage |
| `Foundation/application-navigation` | Official side navigation and integration |
| `Foundation/design-annotations.md` | Applicable layout and implementation annotations |

### Related Components

Use the corresponding GEMS component guidelines whenever Navbar includes:

- Button
- Dropdown / Menu
- Avatar
- Notification
- Badge
- Tooltip
- Other supported interactive controls

**Dependency Rules**
- Apply original GEMS component styles and supported variants.
- Preserve official color, typography, icon sizes, spacing, radius, and effects.
- Use **Brand General** rather than CCM branding.
- Do not hardcode HEX/RGB/HSL, typography values, spacing, radius, or shadows outside official GEMS definitions.
- Do not detach, duplicate, or recreate existing GEMS components when original instances are available.

---

## 9. Accessibility

Navbar and its interactive elements MUST:

- Use appropriate navigation semantics.
- Support keyboard navigation.
- Preserve visible focus indicators.
- Provide accessible names for interactive controls and icon-only actions.
- Identify the current page or active destination appropriately.
- Maintain adequate contrast using official GEMS colors.
- Avoid relying on color alone to communicate state.
- Prevent disabled controls from accepting actions.
- Preserve usability across supported viewport sizes.

Do not remove accessibility behavior to achieve visual similarity.

---

## 10. Strict Rules

### MUST

- Use the official **GEMS General Navbar**.
- Select one of the four supported `Open` × `Sidebar` configurations.
- Synchronize Navbar with official GEMS Application Navigation.
- Follow the approved Application Shell and relevant Page Samples / UX Patterns.
- Adapt supported content to the product, HSD/BRD, and user permissions.
- Preserve original component properties, dimensions, and interaction states.
- Apply all relevant GEMS Foundation and component guidelines.
- Keep navigation consistent across related pages.

### MUST NOT

- Use `Navbar CCM` or any CCM-specific navigation design.
- Treat another component, including `Menu Request`, as the General Navbar.
- Create custom Navbar components, variants, or interaction states.
- Replace GEMS instances with manually recreated frames.
- Modify internal structure, dimensions, colors, typography, or spacing outside GEMS.
- Use custom icons, buttons, or navigation controls when official components exist.
- Confuse the Navbar `Open` property with the `Sidebar` property.
- Use Navbar as Sidebar, Tabs, Breadcrumbs, or a Table Toolbar.
- Add duplicate Navbars or unnecessary global actions.
- Invent product features, routes, permissions, or navigation labels.
- Create unsupported responsive behavior without Human Approval.

---

## 11. AI Implementation Instructions

When designing or generating an application:

1. **Identify the Application Shell:** Determine whether Navbar is required based on the product, page type, and approved GEMS patterns.
2. **Use General Navbar:** Retrieve the official component at node `410:2009`. Exclude CCM components and unrelated navigation examples.
3. **Select Configuration:** Match `Sidebar` to Application Navigation and set `Open` according to its verified component behavior.
4. **Adapt Content:** Include only supported navigation elements and product-relevant global actions based on HSD/BRD and role access.
5. **Preserve GEMS:** Apply original component properties and all relevant Foundation guidelines.
6. **Follow Contextual Examples:** Consult GEMS Page Samples and UX Patterns for placement, consistency, and interaction behavior.

**Human Approval Required When:**
- The product requires a Navbar behavior not supported by official GEMS variants.
- Responsive behavior is undefined and a new pattern is necessary.
- A required global control has no suitable official component.
- The product logo is unavailable; follow the approval process in `Foundation/logo.md`.
- The available product requirements do not establish a necessary navigation or permission decision.

Request related clarification in **one consolidated confirmation** whenever possible.

If the official component cannot be accessed or its properties cannot be verified, do not invent specifications. Request the necessary Figma access, component details, or human direction.

---

## Final Instruction

**AI MUST reuse the official GEMS General Navbar, select only supported configurations, synchronize it with Application Navigation, and adapt its content to the actual product requirements.**

**CCM Navbar and CCM-specific navigation patterns are strictly prohibited.**

**GEMS Design System is the single source of truth for Navbar visual specifications and supported interaction behavior.**
