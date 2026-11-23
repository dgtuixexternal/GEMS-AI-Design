
# GEMS Design System — Components / Navigation Bar

> **MANDATORY:** All application navigation MUST use official GEMS General Design System components. Use the approved `Navigation Bar` for module-based side navigation and `Navbar` for the top application header when required by the Application Shell. Preserve official component names, variants, properties, structure, and visual specifications. CCM components and styling are strictly prohibited.

**Scope:** Application Navigation / Navigation Bar / Menu / Submenu  
**Execution:** Claude AI + Figma MCP  
**Governance:** GEMS General + HSD/BRD + Human Approval  
**Component Strategy:** Official Component Reuse  
**Extensibility:** Supports additional approved modules and menu variants

---

## 1. Purpose & Core Principles

Navigation Bar is a shared Application Shell component responsible for displaying the product's approved navigation structure.

Its purpose is to help users:
- Access permitted modules and features.
- Identify the currently active destination.
- Navigate between parent menus and submenus.
- Expand or collapse supported navigation groups.
- Maintain consistent orientation throughout the application.

### Core Principles

1. **Official Component First**
   - MUST use existing GEMS General components.
   - MUST preserve official component instance references whenever supported.

2. **Module-Based Navigation**
   - MUST select the correct `Module` configuration.
   - MUST NOT mix unrelated application menu structures.

3. **Business-Driven Menu Structure**
   - MUST follow approved HSD/BRD, menu inventory, and role permissions.
   - MUST NOT invent menu items, routes, or access rights.

4. **Consistent Navigation Hierarchy**
   - MUST distinguish the application module, parent menu, submenu, and navigation destination.

5. **Verified Component Properties**
   - MUST use only properties and values supported by the corresponding GEMS component.

6. **Future Extensibility**
   - MUST recognize newly approved modules, menus, and variants after verifying them in Figma.
   - MUST NOT interpret new variants as automatically approved without checking their source and scope.

**Core Rule:**

`Business Requirement → Correct Module → Official Menu Component → Official Submenu Component → Supported State`

---

## 2. Component Architecture

GEMS navigation consists of different components with separate responsibilities.

| Component | Responsibility |
|---|---|
| `Navigation Bar` | Module-based side navigation |
| `_Nav item dropdown base` | Reusable navigation-item foundation |
| `_Nav item dropdown base menu` | Application-specific parent navigation menu |
| `Base_Sub Menu` | Application-specific nested submenu |
| `Navbar` | Horizontal top application header |
| `Page Header` | Current page title, description, and contextual actions |
| `Breadcrumbs` | Location within the page hierarchy |

### Critical Distinction

**`Navigation Bar` is NOT the same component as `Navbar`.**

- `Navigation Bar` contains the application-side navigation structure.
- `Navbar` is the horizontal application header.
- They may coexist within the approved Application Shell.
- Neither component automatically replaces the other.

AI MUST NOT:
- Use `Navbar` as a substitute for the side Navigation Bar.
- Reconstruct a side menu within the horizontal Navbar.
- Use `Page Header` or `Breadcrumbs` as primary application navigation.
- Use a separate generic `Sidebar` component instead of the approved Application Navigation structure.
- Duplicate the same navigation controls without a documented GEMS pattern.

---

## 3. Official Navigation Bar Modules

The GEMS Navigation Bar currently contains three identified module configurations.

| Property | Value | Application |
|---|---|---|
| `Module` | `ISS` | ISS |
| `Module` | `Sini-Saja` | Sini-Saja |
| `Module` | `iCore` | iCore |

The verified reference layouts are 312 px wide. Their inspected reference instances are 1323 px high.

These are measurements of the inspected Figma configurations, not universal responsive sizing rules.

### 3.1 Module Selection

AI MUST:

1. Identify the target application.
2. Locate the official `Navigation Bar` component.
3. Verify the available `Module` variants.
4. Select the variant matching the target application.
5. Preserve the corresponding navigation structure.
6. Adapt only supported content and properties.
7. Follow the approved application menu hierarchy.

### Selection Matrix

| Target Application | Required Module |
|---|---|
| ISS | `Module=ISS` |
| Sini-Saja | `Module=Sini-Saja` |
| iCore | `Module=iCore` |
| Other / New Application | Verify availability in the official GEMS component |

### Future Module Handling

New modules MAY be added to the GEMS component library.

When this happens, AI MUST:
- Reinspect the official `Navigation Bar` component.
- Identify the newly available `Module` value.
- Verify that the module belongs to GEMS General.
- Inspect its menu structure and supporting components.
- Select the new module only when it matches the application requirements.
- Preserve existing modules and their supported behavior.

AI MUST NOT:
- Hardcode the current three modules as the permanent complete list.
- Create a new module variant without authorization.
- Reuse another application's navigation just because it looks similar.
- Automatically merge menus from different modules.
- Copy CCM variants into GEMS General.

**Important:** The module list is extensible, but only through verified official GEMS variants.

---

## 4. Official Navigation Item Foundation

### Component: `_Nav item dropdown base`

This component provides the foundational navigation-item structure.

### 4.1 Verified Variant Properties

The inspected GEMS component contains:

| Property | Values |
|---|---|
| `Open` | `True`, `False` |
| `Current` | `True`, `False` |
| `Theme` | `Default`, `Brand`, `Gray dark` |

The current reference contains 12 combinations.

### 4.2 Variant Matrix

| Open | Current | Theme |
|---|---|---|
| False | False | Default |
| False | True | Default |
| True | False | Default |
| True | True | Default |
| False | False | Brand |
| False | True | Brand |
| True | False | Brand |
| True | True | Brand |
| False | False | Gray dark |
| False | True | Gray dark |
| True | False | Gray dark |
| True | True | Gray dark |

### 4.3 Property Rules

**Open**
- Represents the component's supported expansion condition.
- `True` selects its expanded configuration.
- `False` selects its collapsed configuration.
- MUST follow the actual component's supported behavior.

**Current**
- Represents the applicable current or active navigation condition.
- MUST correspond to the actual route or documented active-navigation rule.
- MUST NOT be assigned arbitrarily.

**Theme**
- MUST use the theme defined by the selected official GEMS configuration.
- MUST NOT be selected solely for visual preference.
- MUST preserve official colors, typography, and states.

### Strict Rules

AI MUST:
- Preserve the component name `_Nav item dropdown base`.
- Use supported properties and combinations.
- Preserve official layout, icons, text styling, and spacing.
- Distinguish active navigation from expanded navigation.

AI MUST NOT:
- Rename the component by removing its underscore.
- Invent additional `Open`, `Current`, or `Theme` values.
- Assume `Open=True` automatically means `Current=True`.
- Assume `Current=True` automatically means `Open=True`.
- Manually recreate the component using Frames or custom styling.
- Use `Theme=Brand` as permission to apply CCM branding.

**Critical Principle:**

`Open` and `Current` represent different navigation conditions.

A menu can be expanded without being the current destination.

---

## 5. Official Parent Menu Component

### Component: `_Nav item dropdown base menu`

This component contains application-specific parent menu configurations.

### 5.1 Identified Variant Naming

The inspected Figma reference uses variant names containing:

| Property | Function |
|---|---|
| `App` | Target application |
| `Menu` | Parent navigation menu |
| `Action` | Expanded or collapsed menu configuration, where applicable |

Example names:

- `App=ISS, Menu=Dashboard`
- `App=ISS, Menu=Fuel & Power Management, Action=Collapse`
- `App=ISS, Menu=Fuel & Power Management, Action=Expand`
- `App=Sini Saja, Menu=Penilaian PJO, Action=Collapse`
- `App=iCore, Menu=Management, Action=Expand`

These examples reflect inspected Figma variant names. AI MUST verify the available configuration before using it.

### 5.2 Parent Menu Selection Rules

AI MUST:

1. Identify the target application's `Module`.
2. Identify the required parent `Menu`.
3. Locate its exact official GEMS configuration.
4. Select its supported `Action` when applicable.
5. Preserve the corresponding menu labels, hierarchy, and visual structure.
6. Apply role-based visibility requirements.
7. Maintain consistency with the current route.

### 5.3 Action Behavior

The inspected parent-menu components include configurations labeled:

- `Action=Collapse`
- `Action=Expand`

AI MUST:
- Use `Collapse` for the corresponding collapsed configuration.
- Use `Expand` for the corresponding expanded configuration.
- Verify whether the menu supports both configurations.
- Preserve the actual child hierarchy and approved interactions.

AI MUST NOT:
- Assume every parent menu has both configurations.
- Create an Expand configuration for a menu that has no verified expandable variant.
- Add child menus simply to fill an expanded layout.
- Change a menu's hierarchy without approved requirements.
- Replace an existing official configuration with another application's menu variant.

### 5.4 Menu Content

Menu content MUST follow:
- Approved application menu inventory.
- Product requirements.
- Access permissions.
- Existing GEMS menu configurations.
- Approved information architecture.

AI MAY update supported content when authorized.

AI MUST NOT:
- Invent additional modules.
- Invent new navigation routes.
- Copy unrelated menu structures.
- Assume similarly named menus in different applications share the same behavior.

---

## 6. Official Submenu Component

### Component: `Base_Sub Menu`

This component provides nested navigation configurations for application-specific menus.

### 6.1 Identified Variant Naming

The inspected Figma reference contains:

| Property | Function |
|---|---|
| `App` | Application |
| `Menu` | Parent menu |
| `SubMenu` | Nested menu group |
| `Expand` | Expansion condition |

Examples:

- `App=ISS, Menu=Fuel & Power Management, SubMenu=Master Data, Expand=Collapsed`
- `App=ISS, Menu=Fuel & Power Management, SubMenu=Master Data, Expand=Expanded`
- `App=ISS, Menu=Meals Management, SubMenu=Catering, Expand=Collapsed`
- `App=ISS, Menu=Meals Management, SubMenu=Catering, Expand=Expanded`

### 6.2 Expansion Values

Identified values:

- `Expand=Collapsed`
- `Expand=Expanded`

AI MUST verify exact values and configurations in the official component.

### 6.3 Submenu Rules

AI MUST:
- Preserve the relationship between the submenu and its parent menu.
- Use the correct application-specific configuration.
- Preserve available expansion and collapse behavior.
- Follow the approved submenu hierarchy.
- Display only authorized destinations.
- Keep active-route indication consistent.

AI MUST NOT:
- Place a submenu under an unrelated parent.
- Mix submenu content from different applications.
- Invent additional hierarchy levels.
- Create unsupported Expanded or Collapsed variants.
- Use a generic dropdown as a replacement for `Base_Sub Menu`.
- Force every parent menu to have submenus.

### 6.4 Nested Navigation

A navigation hierarchy MAY contain:

`Application → Parent Menu → Submenu → Destination`

This structure is conditional.

AI MUST:
- Follow the actual approved hierarchy.
- Preserve the existing nesting depth when supported by GEMS.
- Avoid unnecessary nested levels.
- Maintain understandable labels and destinations.

AI MUST NOT assume every application uses all hierarchy levels.

---

## 7. Relationship with Horizontal Navbar

The official GEMS horizontal `Navbar` remains a separate component.

### 7.1 Verified Navbar Properties

| Property | Values |
|---|---|
| `Open` | `true`, `false` |
| `Sidebar` | `Open`, `Closed` |

### Supported Configurations

| Open | Sidebar |
|---|---|
| true | Open |
| true | Closed |
| false | Open |
| false | Closed |

The inspected horizontal Navbar configurations are 1128 × 72 px.

These measurements apply to the inspected reference components.

### 7.2 Synchronization Rules

AI MUST:
- Use the horizontal Navbar only when included in the approved Application Shell.
- Match `Sidebar=Open` with the corresponding expanded side-navigation condition.
- Match `Sidebar=Closed` with the corresponding collapsed side-navigation condition.
- Preserve the official horizontal Navbar component.
- Maintain consistent alignment and layout.

AI MUST NOT:
- Treat horizontal `Navbar.Open` as equivalent to `_Nav item dropdown base.Open`.
- Treat `Navbar.Sidebar` as a parent-menu expansion property.
- Rebuild the side Navigation Bar within Navbar.
- Add duplicate horizontal Navbars.
- Invent responsive behavior based solely on these properties.

**Important:**

`Navbar.Open`, `Navbar.Sidebar`, `_Nav item dropdown base.Open`, `_Nav item dropdown base menu.Action`, and `Base_Sub Menu.Expand` MUST be treated as distinct properties.

Their behavior must not be conflated.

---

## 8. When to Use Navigation Bar

### Usage Matrix

| Context | Usage |
|---|---|
| Main Dashboard | Use approved Application Shell |
| Management / List Page | Preserve side navigation |
| Detail Page | Preserve parent Application Shell |
| Create / Edit Page | Use when within the main application layout |
| Reports / Analytics | Follow approved Application Shell |
| Master Data | Follow approved Application Shell |
| Settings / Configuration | Follow approved Application Shell |
| Authentication | Follow dedicated authentication layout |
| Modal / Dialog | Do not create additional Navigation Bar |
| Standalone / Public Page | Follow approved standalone layout |

### Rules

AI MUST:
- Use Navigation Bar when required by the approved application layout.
- Preserve consistent navigation across related pages.
- Maintain the current user's navigation context.
- Follow appropriate role-based menu visibility.

AI MUST NOT:
- Add Navigation Bar to every Frame.
- Create duplicate side navigation within one Application Shell.
- Add navigation to Modal or Dialog content.
- Use Navigation Bar as Tabs, Breadcrumbs, Pagination, or Table Toolbar.
- Insert unrelated menus to make the navigation appear complete.

---

## 9. Menu Hierarchy & Active Navigation

### 9.1 Menu Hierarchy

Navigation content MUST follow the approved information architecture.

AI MUST:
- Identify the application's parent menus.
- Identify submenu relationships.
- Identify leaf destinations.
- Preserve correct parent-child relationships.
- Maintain consistent terminology.
- Respect user access permissions.

AI MUST NOT:
- Invent menu structures from generic UI conventions.
- Rearrange approved menus arbitrarily.
- Duplicate destinations without documented justification.
- Infer permission relationships solely from visual placement.

### 9.2 Active Navigation

When a destination is active:

- The correct navigation item MUST reflect the current route.
- Its parent navigation context MUST remain understandable.
- The active appearance MUST follow the official component.
- Expanded menus MUST follow the documented navigation behavior.

AI MUST NOT:
- Mark unrelated destinations as current.
- Use expand/collapse appearance as a replacement for active state.
- Create custom current-state colors or icons.
- Assume an expanded menu is always the currently selected destination.

### 9.3 Navigation Persistence

When users change pages:

- Preserve the selected application module.
- Update the current destination.
- Maintain authorized menu visibility.
- Follow the product's approved expansion behavior.
- Keep the Navigation Bar and horizontal Navbar consistent.

Do not invent automatic collapse, expansion, or state persistence behavior without supporting requirements.

---

## 10. Menu Interaction & States

Navigation Bar interactions depend on the corresponding official component.

| State | Usage |
|---|---|
| Default | Normal available menu |
| Current / Active | Current navigation context |
| Expanded | Child content shown |
| Collapsed | Child content hidden |
| Hover | Pointer interaction when supported |
| Focus | Keyboard focus |
| Disabled | Unavailable destination or action, when supported |
| Loading | Only when the relevant component or workflow supports it |

### Interaction Rules

AI MUST:
- Use the appropriate official GEMS variant.
- Preserve supported Hover and Focus behavior.
- Follow the actual navigation destination.
- Keep expansion and active state consistent with requirements.
- Respect permissions when rendering navigation options.
- Preserve interactive behavior and visual feedback.

AI MUST NOT:
- Invent custom transitions or animations.
- Apply unsupported interaction states.
- Use Disabled styling to indicate an active route.
- Assume every menu supports expansion.
- Add interactions to purely informational elements.
- Treat hidden design layers as active UI requirements.

### Expand / Collapse

For expandable menus:

1. Select the matching official Expanded or Collapsed configuration.
2. Preserve its official child menu structure.
3. Update the expansion condition only through the approved interaction.
4. Maintain current-route consistency.
5. Avoid losing navigation context.

### Direct Navigation

For menus without nested content:

- Navigate to the approved destination.
- Update current-route indication.
- Do not introduce unnecessary expand/collapse interactions.

---

## 11. Layout & Responsive Behavior

### 11.1 Layout

AI MUST:
- Follow the official Navigation Bar module configuration.
- Preserve original component dimensions and sizing behavior.
- Maintain consistent spacing and alignment.
- Use the approved Application Shell.
- Preserve component instances rather than reconstructing them.
- Keep navigation content readable and accessible.

AI MUST NOT:
- Manually resize official components without a supported sizing rule.
- Introduce arbitrary width, height, or spacing values.
- Rebuild internal component hierarchy using custom Frames.
- Create custom scroll or sticky behavior without a reference.
- Apply CCM layout or styling.

### 11.2 Responsive Behavior

AI MUST:
- Inspect official responsive patterns when available.
- Use supported navigation configurations.
- Preserve essential navigation access.
- Maintain compatibility with the horizontal Navbar.
- Follow any approved Desktop, Tablet, or Mobile Application Shell.

AI MUST NOT:
- Assume the desktop module configuration automatically defines mobile navigation.
- Invent a new hamburger menu.
- Introduce undocumented breakpoints.
- Hide important menu destinations without an approved alternative.
- Use an unrelated Sidebar pattern as a responsive fallback.

**Human Approval:** If responsive requirements are not defined by GEMS or the product specification, request approval before introducing an alternative.

---

## 12. Foundation & Component Dependencies

Navigation Bar MUST follow official GEMS General foundations.

### Foundation

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | Official GEMS General colors |
| `Foundation/typography.md` | Typography styles |
| `Foundation/spacing-dan-radius.md` | Spacing and corner radius |
| `Foundation/effect-styles.md` | Borders, shadows, and effects |
| `Foundation/icons.md` | Navigation and action icons |
| `Foundation/misc-icons.md` | Other supported icons |
| `Foundation/logo.md` | Approved application identity |
| `Foundation/application-navigation` | Application navigation architecture |
| `Foundation/design-annotations.md` | Applicable design annotations |

### Related Components

Use relevant GEMS guidelines when Navigation Bar includes:

- `Navbar`
- `Button`
- `Input dropdown`
- `Avatar`
- `Tooltip`
- `Badge`
- Other officially supported elements.

### Rules

AI MUST:
- Use official GEMS General components and tokens.
- Preserve exact component names.
- Preserve the correct module branding.
- Use original icons and supported variants.
- Maintain library connections when supported.

AI MUST NOT:
- Apply CCM typography, colors, or styles.
- Hardcode arbitrary visual values.
- Use third-party component libraries as substitutes.
- Recreate official GEMS components manually.
- Copy unsupported local overrides from example screens.

---

## 13. Accessibility

Navigation components MUST:

- Support keyboard navigation.
- Preserve visible focus states.
- Provide accessible names for icon-only actions.
- Identify current routes appropriately.
- Maintain a logical navigation order.
- Preserve readable labels and hierarchy.
- Support expanded/collapsed state communication where applicable.
- Avoid relying on color alone for active state.
- Prevent unauthorized or disabled actions from remaining interactive.
- Follow the project's approved accessibility requirements.

### Implementation Guidance

For web implementations, use appropriate navigation semantics and state attributes.

Examples may include:
- `aria-current="page"` for an active destination.
- `aria-expanded` for applicable expandable controls.
- Accessible labels for icon-only actions.

These are accessibility implementation requirements, not claims about Figma component properties.

Do not alter official GEMS styling unnecessarily to implement accessibility behavior.

---

## 14. AI Decision Logic

AI MUST follow this sequence.

### Step 1 — Identify Application

Determine:
- Application name.
- User role.
- Approved menu requirements.
- Existing navigation structure.
- Relevant pages and destinations.

### Step 2 — Retrieve Official Navigation Bar

Locate `Navigation Bar` in GEMS General.

Verify current available `Module` variants.

### Step 3 — Select Module

Choose the official module matching the target application.

If unavailable, check whether a new official variant has been added.

### Step 4 — Identify Menu Requirements

Map required menu items from HSD/BRD or an approved menu inventory.

Separate:
- Parent Menu.
- Submenu.
- Destination.
- Permission.
- Current Route.

### Step 5 — Select Official Menu Components

Retrieve:
- `_Nav item dropdown base`
- `_Nav item dropdown base menu`
- `Base_Sub Menu`

Use only the components actually required by the menu hierarchy.

### Step 6 — Select Component Properties

Choose relevant properties:

**Navigation Item**
- `Open`
- `Current`
- `Theme`

**Parent Menu**
- `App`
- `Menu`
- `Action` where applicable

**Submenu**
- `App`
- `Menu`
- `SubMenu`
- `Expand`

Verify the actual component configurations before applying them.

### Step 7 — Configure Navigation Hierarchy

Preserve:
- Application module.
- Menu relationships.
- Approved labels.
- Destinations.
- Role permissions.
- Current route.
- Expansion conditions.

### Step 8 — Synchronize Application Shell

If the layout also includes horizontal `Navbar`, use its official variant and synchronize the supported Sidebar condition.

### Step 9 — Apply Interaction States

Use official variants and supported state behavior.

Do not invent new component variants or transitions.

### Step 10 — Validate

Check:
- Correct application module.
- Correct parent menus.
- Correct submenu hierarchy.
- Correct component names.
- Supported variants and properties.
- Correct current route.
- Consistent expand/collapse behavior.
- Permissions.
- Icons.
- Typography.
- Spacing.
- Responsive behavior.
- Accessibility.
- No CCM usage.
- No unsupported custom components.

### Step 11 — Human Approval

Request Human Approval only when:
- A required module does not exist in GEMS.
- A menu or submenu requires a new official component variant.
- Approved menu information is missing or contradictory.
- Responsive behavior is undefined.
- An interaction requires an unsupported pattern.
- A required application identity or icon is unavailable.
- Changes would materially affect approved information architecture.

Consolidate related questions into one confirmation whenever possible.

---

## 15. Future Component Expansion

The Navigation Bar library may expand over time.

### Supported Expansion Areas

Future updates may include:
- Additional application modules.
- New parent menus.
- Additional nested submenus.
- New supported component variants.
- Updated icon associations.
- Revised navigation hierarchies.
- New responsive configurations.

### Version-Aware Rules

AI MUST:
1. Treat the current Figma library as the authoritative component inventory.
2. Reinspect relevant components when new menu requirements are introduced.
3. Identify changes to component names, properties, and available values.
4. Reuse newly approved variants only after verification.
5. Preserve backward compatibility when appropriate.
6. Distinguish official new variants from local overrides or drafts.

AI MUST NOT:
- Assume the component inventory is permanently fixed.
- Automatically create variants merely because the product adds a menu.
- Infer new property values from naming patterns alone.
- Use unpublished or unrelated references without approval.
- Modify existing component definitions without authorization.

**Extension Principle:**

`New Requirement → Inspect Current GEMS → Existing Supported Variant? → Reuse / Request Approval`

Do not create custom variants as the default response to new requirements.

---

## 16. Strict Rules

### MUST

- Use the official GEMS `Navigation Bar`.
- Select the correct `Module` configuration.
- Use official `_Nav item dropdown base` when applicable.
- Use official `_Nav item dropdown base menu` for supported parent menus.
- Use official `Base_Sub Menu` for supported nested menus.
- Keep horizontal `Navbar` separate from side Navigation Bar.
- Use approved menu names and destinations.
- Respect role-based permissions.
- Preserve original GEMS component instances, variants, and visual specifications.
- Follow GEMS General foundations.
- Verify additional modules and menu configurations before use.
- Maintain consistent navigation across the application.

### MUST NOT

- Use any CCM component, variant, or styling.
- Confuse `Navigation Bar` with horizontal `Navbar`.
- Use a custom Sidebar instead of official Application Navigation.
- Mix menu configurations from unrelated applications.
- Invent application modules, menus, submenus, routes, or permissions.
- Create unsupported component variants.
- Modify GEMS component internals without authorization.
- Rebuild official components with custom Frames.
- Hardcode arbitrary styling.
- Invent expansion or current-state behavior.
- Treat all menus as expandable.
- Treat every available variant as applicable to every application.
- Assume the current module inventory is final.
- Use new component patterns without required Human Approval.

---

## 17. Official Figma References

### 17.1 Primary — Navigation Bar

**Component:** `Navigation Bar`

**Current Modules:**
- `Module=ISS`
- `Module=Sini-Saja`
- `Module=iCore`

**Figma File Key:** `vaAJgd6yZ7l9TrIuF04671`

**Node ID:** `4352:126998`

[Official GEMS Navigation Bar](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=4352-126998)

### 17.2 Navigation Item Foundation

**Component:** `_Nav item dropdown base`

**Node ID:** `345:5292`

[Official GEMS Navigation Item Base](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=345-5292)

### 17.3 Application Menu Variants

**Component:** `_Nav item dropdown base menu`

**Node ID:** `4306:6530`

[Official GEMS Application Menu Variants](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=4306-6530)

### 17.4 Submenu Variants

**Component:** `Base_Sub Menu`

**Node ID:** `4315:66154`

[Official GEMS Submenu Variants](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=4315-66154)

### 17.5 Horizontal Navbar

**Component:** `Navbar`

**Node ID:** `410:2009`

[Official GEMS Horizontal Navbar](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=410-2009)

### 17.6 Related Navigation References

[GEMS Navigation Bar Overview](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=410-344)

[GEMS Application Navigation](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=345-1601)

[GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=904-9049)

[GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1105-7310)

---

## Final AI Instruction

**AI MUST use the official GEMS General Navigation Bar and select the correct application Module before configuring menus or submenus.**

AI MUST preserve the exact official component names:
- `Navigation Bar`
- `_Nav item dropdown base`
- `_Nav item dropdown base menu`
- `Base_Sub Menu`
- `Navbar`

AI MUST distinguish horizontal Navbar behavior from side Navigation Bar behavior.

AI MUST follow approved menu hierarchy, product requirements, role permissions, and existing GEMS component properties.

AI MUST verify newly introduced modules and menu variants directly in GEMS before using them.

**Never use CCM designs, components, colors, typography, navigation variants, or styling.**

**GEMS General Design System is the single source of truth for navigation components and visual specifications.**
