
# GEMS Design System — Components / Navigation Bar

> **CRITICAL — SOURCE LOCK:** All application side navigation MUST use the official GEMS General `Navigation Bar` component at node `4352:126998`. The deprecated/draft `Draft - GEMS Slide Bar` at node `2714:24723` is STRICTLY PROHIBITED, including all of its child components, variants, and instances. CCM navigation components are also prohibited.

**Execution:** Claude AI + Figma MCP  
**Scope:** Application Side Navigation / Module Navigation / Menu / Submenu  
**Governance:** Human Module Instruction + GEMS General + HSD/BRD  
**Default Navigation State:** Expanded  
**Component Source:** `4352:126998` ONLY

---

## 1. Mandatory Source Selection

### 1.1 Approved Navigation Bar

**Official Component**
- Name: `Navigation Bar`
- File: `GEMS Design System`
- File Key: `vaAJgd6yZ7l9TrIuF04671`
- Node ID: `4352:126998`
- Status: **APPROVED SOURCE**

AI MUST:
1. Access the exact approved Navigation Bar node.
2. Inspect the available `Module` variants.
3. Select the variant matching the Human's requested application module.
4. Select the appropriate supported navigation state.
5. Reuse the official GEMS component instance.
6. Preserve the original component structure, visuals, and library references.

### 1.2 Prohibited Navigation Sources

| Source | Node ID | Usage |
|---|---|---|
| `Navigation Bar` | `4352:126998` | **REQUIRED** |
| `Draft - GEMS Slide Bar` | `2714:24723` | **PROHIBITED** |
| `Draft - FAMS navigation` | `698:1460` | **PROHIBITED** |
| CCM navigation components | Any CCM node | **PROHIBITED** |
| Custom Sidebar / Slide Bar | Any custom source | **PROHIBITED** |

**STRICT RULES**

AI MUST NOT:
- Use `Draft - GEMS Slide Bar`, even if its design looks identical.
- Copy any frame, instance, component, or variant from node `2714:24723`.
- Use draft components as a fallback.
- Recreate a draft design using General colors.
- Use CCM components or styling.
- Select navigation based on visual similarity alone.
- Assume that all components inside the GEMS file are approved.

**Important:** Source selection MUST be based on the approved component node and module identity, NOT on component appearance.

---

## 2. Human Instruction Determines Module

The Human's application/module instruction is the primary selector for Navigation Bar.

### 2.1 Module Selection Matrix

The inspected approved Navigation Bar contains these application modules:

| Human Instruction | Required Navigation Bar |
|---|---|
| ISS | `Module=ISS` |
| Sini-Saja | `Module=Sini-Saja` |
| iCore | `Module=iCore` |
| Synova | `Module=Synova` |
| Mitigasi | `Module=Mitigasi` |

These are the currently inspected modules. AI MUST recheck the approved node when additional modules are introduced.

### 2.2 Example — Human Requests ISS

**Human Instruction:**

"Buat dashboard untuk modul ISS."

**Mandatory AI Behavior:**

1. Identify the application module: `ISS`.
2. Open the approved Navigation Bar source: `4352:126998`.
3. Find the matching configuration: `Module=ISS`.
4. Select its official Expanded state by default.
5. Insert or reuse the official ISS Navigation Bar.
6. Apply the appropriate ISS menu hierarchy.
7. Highlight the correct active destination.
8. Preserve all official GEMS General visual properties.

**Expected Selection:**

`Navigation Bar → Module=ISS → State=Expand`

**Forbidden Selection:**

`Draft - GEMS Slide Bar → Theme=Primary → State=Expanded`

These are different component sources and MUST NOT be treated as interchangeable.

### 2.3 Module Selection Rules

AI MUST:
- Read the Human's requested module before selecting any Navigation Bar.
- Match the module to the official approved component.
- Preserve the selected application's menu structure.
- Follow approved HSD/BRD navigation requirements.
- Apply role-based permissions.

AI MUST NOT:
- Automatically choose ISS when another module is requested.
- Combine menus from different modules.
- Select modules based on the current Figma canvas selection.
- Use whichever navigation component appears first in search results.
- Infer a module from brand colors alone.
- Invent an unsupported module variant.

### 2.4 Missing Module

If the Human requests a module unavailable in the approved Navigation Bar:

1. Recheck node `4352:126998` for newly added variants.
2. Verify the exact module name.
3. If unavailable, report the missing official module.
4. Request Human Approval before proposing any alternative.

**Never use `Draft - GEMS Slide Bar` or CCM as a fallback.**

---

## 3. Expanded vs Collapsed — Default Decision

**MANDATORY: Expanded is the default and preferred navigation state.**

Collapsed is optional and is used only when justified by actual layout constraints, user preference, or approved requirements.

### 3.1 Selection Matrix

| Condition | Required Decision |
|---|---|
| Human specifies a module only | Expanded |
| Dashboard | Expanded |
| Management / List Page | Expanded |
| Detail Page | Expanded |
| Create / Edit Form | Expanded |
| Settings / Master Data | Expanded |
| Reports / Analytics | Expanded |
| Data Table with many columns | Try Expanded first |
| Complex Chart / Analytics | Try Expanded first |
| Limited horizontal workspace | Collapsed MAY be used if necessary |
| Human explicitly requests Collapsed | Collapsed |
| User manually collapses navigation | Collapsed |
| Approved responsive pattern requires Collapsed | Collapsed |

### 3.2 Expanded Rules

AI MUST:
- Prioritize Expanded as the initial state.
- Preserve visible menu labels.
- Preserve navigation hierarchy and readability.
- Use the official Expanded configuration of the requested module.
- Maintain consistent Application Shell behavior.

AI MUST NOT automatically collapse navigation merely because a page contains tables, charts, or forms.

### 3.3 Collapsed Rules

AI MAY use Collapsed when:
- Expanded navigation materially restricts the available workspace.
- Content cannot remain usable after applying the approved responsive layout.
- The Human explicitly requests Collapsed.
- The user chooses Collapsed.
- Approved product requirements specify Collapsed.

Before selecting Collapsed, AI MUST:
1. Evaluate the available content width.
2. Attempt the official Expanded layout.
3. Check whether normal GEMS responsive behavior resolves the space constraint.
4. Confirm that Collapsed is necessary or explicitly requested.
5. Use the matching official Collapsed variant for the SAME module.

### 3.4 Navigation State Decision

**Required Decision Order:**

`Human Module → Approved Navigation Bar → Expanded Default → Evaluate Layout → Collapsed Only If Needed`

**Critical Rule:** Expanded and Collapsed are states of the approved module Navigation Bar, not permission to switch component sources.

---

## 4. Official Module States

The approved Navigation Bar contains the following inspected configurations:

| Module | Expanded | Collapsed |
|---|---|---|
| ISS | Available | Available |
| Sini-Saja | Available | Available |
| iCore | Available | Available |
| Synova | Available | Available |
| Mitigasi | Available | Available |

### Verified Reference Names

Examples:
- `Module=ISS, State=Expand`
- `Module=ISS, State=Collapse`
- `Module=Sini-Saja, State=Expand`
- `Module=Sini-Saja, State=Collapse`
- `Module=Synova, State=Expand`
- `Module=Synova, State=Collapse`

Some Expanded references, including iCore and Mitigasi, may have a module-only name without an explicit `State=Expand` property in their inspected metadata.

AI MUST use the actual available instance and properties. Do not invent property values or rename variants to force consistency.

### Size References

The inspected component examples include:
- Expanded navigation: 312 px width.
- Collapsed navigation: 72 px width.

These are observed reference dimensions, not universal breakpoint specifications.

AI MUST preserve the official instance's sizing behavior rather than manually applying these numbers to unrelated layouts.

---

## 5. Official Navigation Components

The approved Navigation Bar uses related GEMS General navigation components.

| Component | Responsibility |
|---|---|
| `Navigation Bar` | Full application side navigation |
| `_Nav item base` | Standard navigation item |
| `_Nav item button` | Compact navigation item/button |
| `_Nav item dropdown base` | Expandable navigation item foundation |
| `_Nav item dropdown base menu` | Application-specific parent menu |
| `Base_Sub Menu` | Application-specific nested submenu |

These supporting components MUST be used only within the approved GEMS navigation structure and according to their available properties.

### 5.1 `_Nav item base`

Inspected properties:

| Property | Values |
|---|---|
| `Current` | `True`, `False` |
| `Theme` | `Default`, `Gray dark` |
| `State` | `Default`, `Hover`, `Focused` |
| `Text` | `true` in the inspected configurations |

Use for standard navigation destinations when supported by the selected Navigation Bar.

### 5.2 `_Nav item button`

Inspected properties:

| Property | Values |
|---|---|
| `Current` | `True`, `False` |
| `Size` | `md`, `lg` |
| `Theme` | `Default`, `Brand`, `Gray dark` |
| `State` | `Default`, `Hover`, `Focused` |

Use for compact navigation controls when required by the official layout.

### 5.3 `_Nav item dropdown base`

Inspected properties:

| Property | Values |
|---|---|
| `Open` | `True`, `False` |
| `Current` | `True`, `False` |
| `Theme` | `Default`, `Brand`, `Gray dark` |

Use for expandable navigation groups when supported.

### 5.4 `_Nav item dropdown base menu`

Inspected variant naming includes:
- `App`
- `Menu`
- `Action`, when applicable.

Use the exact approved application and parent-menu configuration.

### 5.5 `Base_Sub Menu`

Inspected variant naming includes:
- `App`
- `Menu`
- `SubMenu`
- `Expand`

Supported expansion examples:
- `Expand=Collapsed`
- `Expand=Expanded`

### Component Restrictions

AI MUST NOT:
- Replace the full Navigation Bar with an individual `_Nav item` component.
- Construct a new Navigation Bar from individual items when the correct full module instance already exists.
- Mix support components from an unrelated application.
- Invent unsupported combinations or styles.

**Priority:** Reuse the complete approved module Navigation Bar first. Supporting components are for its documented internal behavior, not alternative navigation sources.

---

## 6. Parent Menu & Submenu Behavior

### Parent Menu

Use an expandable parent menu only when its navigation hierarchy contains supported child destinations.

AI MUST:
- Select the correct `App` and `Menu`.
- Use the matching supported `Action`.
- Preserve approved children.
- Respect role-based access.
- Maintain current-route indication.

### Submenu

Use `Base_Sub Menu` only for approved nested navigation.

AI MUST:
- Match `App`, `Menu`, and `SubMenu`.
- Select the appropriate supported `Expand` value.
- Preserve parent-child relationships.
- Maintain correct active navigation.

### Important Distinction

The following are separate conditions:

| Property | Meaning |
|---|---|
| Navigation Bar `State` | Full side navigation Expanded/Collapsed |
| Navigation item `Open` | Individual navigation group open/closed |
| Parent menu `Action` | Menu-specific Expand/Collapse configuration |
| Submenu `Expand` | Nested submenu expanded/collapsed |
| Navigation item `Current` | Active/current navigation condition |

**Collapsing the entire Navigation Bar MUST NOT automatically be interpreted as collapsing every parent menu's business hierarchy.**

Keep the state and behavior relationships consistent with the approved GEMS implementation.

---

## 7. Navigation Bar Usage

### When to Use

| Page | Usage |
|---|---|
| Dashboard | Use approved module Navigation Bar |
| Management List | Use approved module Navigation Bar |
| Detail Page | Preserve Application Shell navigation |
| Create / Edit Page | Preserve navigation when using the main Application Shell |
| Report Page | Use approved module Navigation Bar |
| Master Data | Use approved module Navigation Bar |
| Settings | Use approved module Navigation Bar |
| Authentication | Follow dedicated authentication layout |
| Standalone / Public Page | Follow its approved page layout |
| Modal / Dialog | Do not create an additional Navigation Bar |

### Rules

AI MUST:
- Maintain consistent navigation across related application pages.
- Use the same approved module source.
- Preserve current navigation context.
- Use the correct Expanded/Collapsed state.

AI MUST NOT:
- Add duplicate side navigation.
- Change modules between pages without approved requirements.
- Use Navigation Bar as Tabs or Breadcrumbs.
- Add unrelated global actions.
- Insert a draft Navigation Bar into an existing approved Application Shell.

---

## 8. Active Navigation & Permissions

AI MUST:
- Identify the active route.
- Apply the correct current-menu state.
- Maintain parent-menu and submenu context.
- Display only permitted navigation destinations.
- Follow approved HSD/BRD and RBAC requirements.
- Keep navigation consistent when the user changes pages.

AI MUST NOT:
- Invent routes or permission rules.
- Highlight unrelated destinations.
- Treat Expanded as equivalent to Current.
- Expose unauthorized actions.
- Assume every role has access to every menu present in Figma.

**A menu existing in GEMS does not automatically mean it is available to every user.**

---

## 9. Responsive & Layout Rules

### Expanded Layout

AI MUST:
- Start with official Expanded navigation.
- Maintain content readability.
- Follow GEMS spacing, grid, and responsive behavior.
- Preserve accessible navigation labels.

### Collapsed Layout

When legitimately required, AI MUST:
- Use the official Collapsed variant of the same application module.
- Preserve recognized navigation destinations.
- Use supported icons and current-state indicators.
- Provide the approved means of returning to Expanded.
- Keep the horizontal Navbar and content layout consistent.

### Responsive Restrictions

AI MUST NOT:
- Use the deprecated draft sidebar for responsive screens.
- Invent mobile-specific navigation components.
- Manually resize Expanded navigation to simulate Collapsed.
- Hide essential destinations without an approved pattern.
- Use unsupported breakpoints or custom hamburger menus.

If responsive requirements cannot be satisfied by approved GEMS components, request Human Approval.

---

## 10. Figma MCP Component Retrieval Rules

**This section is mandatory for AI-assisted Figma generation.**

### Retrieval Sequence

1. Read the Human's application module.
2. Open the official GEMS file.
3. Navigate to node `4352:126998`.
4. Confirm the node is named `Navigation Bar`.
5. Inspect available module variants.
6. Select the exact requested module.
7. Choose Expanded by default.
8. Select the corresponding official component/variant.
9. Insert or reuse the component in the target design.
10. Verify the resulting component identity and visual output.

### Mandatory Source Validation

Before using an instance, AI MUST verify:

| Check | Requirement |
|---|---|
| Source File | Official GEMS Design System |
| Source Node | `4352:126998` or an approved descendant |
| Component Family | `Navigation Bar` |
| Module | Matches Human instruction |
| State | Expanded by default |
| Draft Source | Not used |
| CCM Source | Not used |
| Component Connection | Preserved where supported |

### Forbidden Retrieval Behavior

AI MUST NOT:
- Search for "sidebar" and select the first matching component.
- Prefer an older component because it appears earlier in search results.
- Select `Draft - GEMS Slide Bar` because its properties include `State=Expanded`.
- Copy a draft instance and change its appearance.
- Use the currently selected Figma layer as a replacement for the approved source.
- Use custom Frames when an approved module component exists.

### Final Verification

Before reporting completion, AI MUST confirm:
- Correct source component.
- Correct module.
- Correct state.
- Correct active navigation.
- Correct menu hierarchy.
- No draft or CCM component used.
- No unsupported overrides.

If instance provenance cannot be verified, do not claim the result complies with GEMS.

---

## 11. Foundation & Related Guidelines

Navigation Bar MUST follow:

- `Foundation/color.md`
- `Foundation/typography.md`
- `Foundation/spacing-dan-radius.md`
- `Foundation/effect-styles.md`
- `Foundation/icons.md`
- `Foundation/misc-icons.md`
- `Foundation/logo.md`
- `Foundation/application-navigation`
- `Foundation/design-annotations.md`

Use relevant official guidelines for:
- Horizontal Navbar.
- Button.
- Input Dropdown.
- Tooltip.
- Avatar.
- Page Header.
- Breadcrumbs.

**Brand Rule:** Use GEMS General styling. Never use CCM brand colors or tokens.

---

## 12. Human Approval & Future Modules

Human Approval is required when:
- The requested module is absent from node `4352:126998`.
- The approved component lacks a required state.
- A new parent menu or submenu variant is necessary.
- Navigation hierarchy conflicts with HSD/BRD.
- Role permissions are unclear.
- Required responsive behavior is unavailable.
- The source component cannot be accessed or verified.

AI MUST consolidate unresolved questions into one confirmation.

AI MUST NOT use a draft or CCM component while waiting for approval.

### Future Expansion

When GEMS adds new approved modules:

1. Reinspect `4352:126998`.
2. Verify the new module.
3. Identify its available Expanded and Collapsed states.
4. Inspect associated menu and submenu configurations.
5. Update the module inventory when appropriate.
6. Use the newly approved official component.

**The module list is extensible; the approved source restriction remains mandatory.**

---

## 13. Strict Compliance Checklist

Before completing the design:

- [ ] Human-requested module identified.
- [ ] Approved Navigation Bar node `4352:126998` used.
- [ ] Exact module variant selected.
- [ ] Expanded used by default.
- [ ] Collapsed used only when justified or explicitly requested.
- [ ] Official menu/submenu hierarchy preserved.
- [ ] Active navigation matches the current route.
- [ ] Role permissions followed.
- [ ] GEMS General tokens and components preserved.
- [ ] No draft component or descendant used.
- [ ] No CCM component used.
- [ ] No unsupported custom navigation.
- [ ] Final component provenance verified.

---

## 14. Official Figma References

### REQUIRED — Approved Navigation Bar

[Navigation Bar — Official Source](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=4352-126998)

**Node:** `4352:126998`

### Supporting GEMS Components

- [_Nav item base](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=345-5116)
- [_Nav item button](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=410-2248)
- [_Nav item dropdown base](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=345-5292)
- [_Nav item dropdown base menu](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=4306-6530)
- [Base_Sub Menu](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=4315-66154)

### Related Documentation

[Application Navigation — Component Page](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=345-1601)

### PROHIBITED — Never Use

[Draft - GEMS Slide Bar](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2714-24723)

**Node:** `2714:24723`  
**Usage:** STRICTLY FORBIDDEN

Also prohibited:
- `Draft - FAMS navigation`
- All CCM Navigation components
- All unsupported custom Sidebar or Slide Bar patterns

---

## Final AI Instruction

**AI MUST use the official GEMS General Navigation Bar at node `4352:126998` and select the module specified by the Human.**

If the Human requests ISS, select the official `Module=ISS` Navigation Bar.

If the Human requests Sini-Saja, select `Module=Sini-Saja`.

Apply the same rule to every other officially supported module.

**Expanded is the mandatory default. Collapsed is optional and requires justification or explicit instruction.**

**AI MUST NEVER use `Draft - GEMS Slide Bar` at node `2714:24723`, any descendant of that draft, or any CCM navigation component.**

**If the approved component is unavailable, request Human Approval rather than substituting another component.**

**The Human determines the application module. The approved GEMS Navigation Bar determines the component. GEMS properties determine the visual state.**
