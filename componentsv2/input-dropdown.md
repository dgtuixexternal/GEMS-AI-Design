
# GEMS Design System — Components / Input Dropdown

> **MANDATORY:** All Dropdown interfaces MUST use official GEMS General components from the connected Figma Design System. Preserve original component references, variants, states, typography, colors, spacing, radius, icons, and interaction behavior. **CCM components and CCM-derived styling are strictly prohibited.**

## 1. Purpose & Source of Truth

Dropdown allows users to select values from predefined options, search within supported option lists, or interact with contextual menus.

This guideline covers:

- Input Dropdown
- Dropdown
- Dropdown Menu Items
- Dropdown List Items
- Dropdown List Headers
- Dropdown Scrollbar
- Search, Tags, selection, validation, and contextual usage

**Core Principle:** Use Dropdown for selection from defined options. Use Input Field for free-text entry. Choose components based on data and interaction—not visual similarity.

### 1.1 Reference Priority

1. **Official GEMS General Components:** Component variants, properties, states, and styling.
2. **GEMS Supporting Components:** Menu items, headers, selection indicators, and scrollbars.
3. **GEMS Page Samples & UX Patterns:** Contextual usage, placement, and behavior.
4. **Product HSD/BRD:** Option sources, selection requirements, permissions, and workflows.
5. **General UI/UX Principles:** Fallback only when GEMS provides no specific guidance.

GEMS governs visual components. HSD/BRD governs business requirements.

Read only the references relevant to the current interface.

## 2. Component Selection Matrix

| Requirement | GEMS Component | Example |
|---|---|---|
| Select a predefined option | Input Dropdown — Default | Lokasi |
| Select with contextual icon | Input Dropdown — Icon leading | Kategori |
| Select a person using avatar | Input Dropdown — Avatar leading | Karyawan |
| Select option with semantic indicator | Input Dropdown — Dot leading | Status |
| Search available options | Input Dropdown — Search | Cari Penanggung Jawab |
| Display multiple selected values | Input Dropdown — Tags | Pilih Kategori |
| Display selectable menu options | Dropdown Menu Item | Selection list |
| Display option with icon/checkbox | Dropdown List Item | Contextual options |
| Group menu options | Dropdown List Header | Menu sections |
| Open menu through icon/button/avatar | Dropdown | Contextual menu |
| Scroll long option list | Dropdown Scrollbar | Overflow menu |

### Selection Rules

- Select the component matching the required interaction.
- Use official GEMS General components and supported properties.
- Follow HSD/BRD for option sources and selection rules.
- Do not replace Dropdown with free-text Input without an approved reason.
- Do not introduce Search, Tags, or multi-selection automatically.
- Do not recreate existing GEMS components manually.

## 3. Input Dropdown

### 3.1 Available Properties

| Property | Official Values |
|---|---|
| `Type` | `Default`, `Icon leading`, `Avatar leading`, `Dot leading`, `Search`, `Tags` |
| `State` | `Placeholder`, `Default`, `Focused`, `Open`, `Disabled` |

Use exact Figma property names and supported combinations.

Do not invent additional `Size`, `Destructive`, `Filled`, or `Success` properties.

### 3.2 Type Usage Matrix

| Type | When to Use | Restriction |
|---|---|---|
| Default | Standard predefined selection | Do not invent options |
| Icon leading | Icon clarifies option meaning | No decorative icons |
| Avatar leading | Options represent people/entities | Avatar data must exist |
| Dot leading | Options have semantic status indicators | Colors must follow GEMS |
| Search | Users search within approved options | Query is not automatically a selected value |
| Tags | Supported multiple selections | Multi-select must be defined |

### 3.3 Type-Specific Rules

**Default**
- Use for ordinary single-selection behavior unless requirements specify otherwise.
- Preserve the selected value and official dropdown indicator.

**Icon leading**
- Use official GEMS icons.
- Follow `Foundation/icons.md`.
- Preserve component-defined icon size, alignment, and color.

**Avatar leading**
- Use when avatars help identify options.
- Follow existing GEMS Avatar specifications.
- Do not fabricate profile images or personal information.

**Dot leading**
- Use only when dots have defined semantic meaning.
- Follow `Foundation/color.md`.
- Do not invent status colors or decorative indicators.

**Search**
- Search only within approved options.
- Keep the search query separate from the selected value.
- Follow GEMS Search interaction and no-results patterns.
- Do not invent autocomplete, remote search, minimum query length, or debounce behavior.

**Tags**
- Use only for supported multi-selection.
- Preserve selected tags.
- Follow HSD/BRD for selection limits and removal behavior.
- Distinguish selection-based Tags Dropdown from free-text Tags Input.

## 4. Input Dropdown States

### 4.1 State Matrix

| State | Condition | Behavior |
|---|---|---|
| `Placeholder` | No selection | Displays placeholder |
| `Default` | Dropdown closed | Displays current value or normal appearance |
| `Focused` | Control receives focus | Official focus styling |
| `Open` | Menu is visible | Displays official dropdown menu |
| `Disabled` | Selection unavailable | Non-interactive |

### 4.2 State Rules

**Placeholder**
- Use contextual placeholder text.
- Do not treat placeholder as a selected value.

**Default**
- Preserve the selected value.
- Restore closed appearance when the menu closes.

**Focused**
- Maintain official GEMS focus styling.
- Preserve keyboard accessibility.

**Open**
- Display the correct GEMS menu and option structure.
- Preserve selected-option indicators.
- Do not assume every Dropdown Type uses identical menu dimensions.

**Disabled**
- Prevent opening or selection changes.
- Explain unavailability when necessary.
- Do not use Disabled as a validation-error indicator.

## 5. Dropdown Menu Items

### 5.1 Available Properties

| Property | Official Values |
|---|---|
| `Selected` | `True`, `False` |
| `Type` | `Default`, `Icon leading`, `Avatar leading`, `Dot leading` |
| `State` | `Default`, `Hover`, `Disabled` |

**Important:** `Selected` is a separate component property, not a State.

### 5.2 Selection & State Matrix

| Property / State | Meaning |
|---|---|
| Selected=False | Option is not selected |
| Selected=True | Option is selected |
| Default | Normal appearance |
| Hover | Pointer-hover appearance |
| Disabled | Option cannot be selected |

### 5.3 Menu Item Rules

- Use official GEMS menu-item variants.
- Keep selected indicators synchronized with the Dropdown value.
- Preserve original labels, icons, avatars, and dots.
- Use official Hover and Disabled styling.
- Prevent selection of disabled options.
- Do not treat Hover as Selected.
- Do not invent selected-state styling or unsupported combinations.

## 6. Dropdown List Items & Headers

### 6.1 Dropdown List Item Properties

| Property | Official Values |
|---|---|
| `Icon` | `True`, `False` |
| `Checkbox` | `True`, `False` |
| `State` | `Default`, `Hover`, `Disabled` |
| `Divider` | `True`, `False` |

Use only combinations supported by the component.

### 6.2 List Item Rules

**Icon**
- Use only when meaningful.
- Follow `Foundation/icons.md`.

**Checkbox**
- Use when an approved selection pattern requires it.
- Do not assume Checkbox automatically means multi-selection.

**Divider**
- Use only for meaningful separation.
- Do not add dividers to every option by default.

**Disabled**
- Preserve official styling and prevent selection.

### 6.3 Dropdown List Header

Available configurations:

| Type | Purpose |
|---|---|
| `Header` | Standard section heading |
| `Avatar group` | Header with avatar-group presentation |

**Rules**
- Use headers for meaningful option grouping.
- Preserve official GEMS Text Styles and spacing.
- Use Avatar Group only when supported by the product.
- Do not invent group labels or avatar data.
- Do not add decorative headers unnecessarily.

## 7. Dropdown & Scrollbar

### 7.1 Dropdown Properties

The separate GEMS Dropdown component provides:

| Property | Values |
|---|---|
| `Type` | `Icon`, `Button`, `Avatar` |
| `Open` | `True`, `False` |

### 7.2 Dropdown Type Usage

| Type | Usage |
|---|---|
| Icon | Icon-triggered contextual menu |
| Button | Button-triggered contextual menu |
| Avatar | Avatar-triggered contextual menu |

**Rules**
- Use the official trigger and menu configuration.
- Preserve the correct Open behavior.
- Follow `Foundation/icons.md` for Icon triggers.
- Follow `components/button.md` for Button triggers.
- Follow official GEMS Avatar specifications where applicable.
- Do not confuse `Open=True/False` with Input Dropdown `State=Open`.
- Do not turn independent CRUD actions into ordinary selection options without an approved UX Pattern.

### 7.3 Dropdown Scrollbar

Available configurations:

- `Length=25%`
- `Length=50%`
- `Length=75%`

**Rules**
- Use the official scrollbar for supported overflow menus.
- Preserve styling and placement.
- Allow scrolling when necessary.
- Do not infer fixed menu heights from documentation-frame examples.
- Do not invent scrollbar colors, dimensions, or variants.

## 8. Selection, Search & Data Behavior

### 8.1 Single Selection

- Use when only one value is permitted.
- Keep the selected value synchronized between trigger and menu.
- Follow official menu-closing behavior.
- Do not enable multiple selection.

### 8.2 Multiple Selection

- Use only when supported by HSD/BRD and GEMS.
- Preserve all valid selected values.
- Use official Tags or Checkbox patterns.
- Follow supported tag-removal behavior.
- Do not invent selection limits or duplicate rules.

### 8.3 Search Behavior

- Search within the approved dataset.
- Keep query and selected value distinct.
- Follow GEMS search, clearing, and focus behavior.
- Display contextual no-results feedback.
- Do not treat arbitrary search text as a valid option.

### 8.4 Option Source

Dropdown options MUST originate from approved sources:

- HSD/BRD
- Product master data
- Authorized APIs
- Explicit user requirements

Do not invent option values, default selections, or `Lainnya` options.

### 8.5 Dependent Dropdowns

When selections affect other fields:

- Follow product-defined dependencies.
- Update dependent options consistently.
- Preserve valid values when possible.
- Explain invalidated selections.
- Do not silently replace values.
- Do not invent dependencies.

## 9. Validation, Empty & Error Handling

### 9.1 Validation Matrix

| Condition | Behavior |
|---|---|
| Required selection missing | Display specific validation message |
| Invalid selection | Explain applicable restriction |
| Disabled option | Prevent selection |
| No options available | Display contextual empty feedback |
| Search returns no results | Display no-results feedback |
| Data request fails | Follow GEMS Error State |
| Selection corrected | Restore normal supported appearance |

### 9.2 Validation Rules

- Follow HSD/BRD for required status and valid values.
- Use verified GEMS validation patterns.
- Preserve valid selections during errors.
- Associate messages with the relevant Dropdown.
- Do not invent `Destructive` or `Success` properties.
- Do not create custom red/green borders or status icons.
- Do not use Disabled instead of validation.

### 9.3 Empty Options & No Results

**No options available**
- Display appropriate empty-option feedback.
- Keep the field label and context clear.
- Do not fabricate options.

**Search returns no results**
- Display a contextual message.
- Preserve the search query where appropriate.
- Do not automatically create a new option.

### 9.4 Loading & Error

- Follow official GEMS loading and error UX Patterns.
- Preserve selected values during recoverable failures.
- Distinguish empty datasets from failed requests.
- Do not invent custom Dropdown loading states.
- Use approved retry actions where necessary.

## 10. Contextual Usage — Forms, CRUD & Filters

### 10.1 Usage Matrix

| Context | Recommended Usage | Important Rule |
|---|---|---|
| Create Form | Appropriate Input Dropdown Type | Options from approved data |
| Edit Form | Existing selected value | Preserve valid selection |
| Employee Selection | Avatar leading / Search | Use actual employee data |
| Status Selection | Dot leading | Follow semantic colors |
| Category Selection | Default / Tags | Follow single/multi requirements |
| Page Filter | Official Input Dropdown | Follow GEMS Filter pattern |
| Table Toolbar | Appropriate Dropdown | Follow GEMS Table layout |
| Contextual Menu | Icon / Button / Avatar Dropdown | Actions must be authorized |
| Dependent Fields | Related Dropdowns | Follow defined dependencies |
| Empty Data | Official empty feedback | Do not invent options |

### 10.2 Create Form

- Use only required fields.
- Select the correct official Dropdown Type.
- Follow GEMS Form and Form Section patterns.
- Apply required/optional rules from HSD/BRD.
- Use standard GEMS Buttons for Save, Submit, and Cancel.
- Do not invent default selections.

### 10.3 Edit Form

- Display existing selections accurately.
- Preserve unchanged values.
- Follow field-level permissions.
- Handle unavailable options according to product rules.
- Do not clear selections silently.

### 10.4 Read / Detail

- Use appropriate GEMS display components for non-editable information.
- Use Disabled Dropdown only when the approved pattern requires it.
- Do not represent all read-only values as disabled controls.

### 10.5 Search & Filters

- Use official Input Dropdown for structured selection.
- Follow relevant GEMS Table, Input, and Filter patterns.
- Preserve selected filters appropriately.
- Do not introduce unsupported filter categories.
- Never substitute CCM controls.

### 10.6 CRUD Actions

Dropdown selection is not automatically a CRUD operation.

- **Create:** New options require an approved creation workflow.
- **Read:** Selection may control supported views or filters.
- **Update:** Changes may be part of an edit form; saving follows product requirements.
- **Delete:** Use GEMS Button and confirmation patterns.

Do not use ordinary selection menus as replacements for destructive-action workflows.

### 10.7 Dashboard & Reports

- Use Dropdown only when structured selection is supported.
- Follow GEMS Dashboard, Chart, and Filter patterns.
- Do not invent periods, report categories, or filter options.
- Keep displayed data consistent with selected values.

## 11. Foundation, Layout & Accessibility

### 11.1 Foundation Integration

Dropdown styling MUST follow these exact GEMS repository guidelines:

| Guideline | Requirement |
|---|---|
| `Foundation/color.md` | General semantic colors |
| `Foundation/typography.md` | Official GEMS Text Styles |
| `Foundation/spacing-dan-radius.md` | Spacing and radius variables |
| `Foundation/effect-styles.md` | Official effects where specified |
| `Foundation/icons.md` | General icons, size, and usage |
| `Foundation/misc-icons.md` | Specialized icons when applicable |
| `Foundation/design-annotations.md` | Additional approved design specifications |

Use official component properties and connected Figma variables/styles.

Do not recreate visual values manually.

### 11.2 Color

- Use official GEMS General semantic tokens.
- Preserve selected, hover, focused, and disabled appearances.
- Follow approved status colors for Dot leading.
- Do not use CCM colors.
- Do not hardcode HEX, RGB, or HSL.

### 11.3 Typography

- Apply existing GEMS Figma Text Styles.
- Preserve component-defined font size, weight, line height, and spacing.
- Maintain readable option labels.
- Do not create custom typography or detach official styles.

### 11.4 Spacing & Radius

- Preserve official component padding, dimensions, and border radius.
- Use GEMS spacing variables for surrounding layout.
- Keep trigger/menu alignment consistent.
- Do not invent custom internal spacing or radius.

### 11.5 Effects

- Use official GEMS effect styles only when specified.
- Do not add decorative shadows automatically.
- Follow existing component and Page Sample usage.

### 11.6 Icons & Avatars

- Use official GEMS icons and relevant Avatar components.
- Preserve icon style, size, alignment, and semantic color.
- Use specialized icons only when supported by `Foundation/misc-icons.md`.
- Do not invent icon sizes or fabricate avatar data.

### 11.7 Responsive

- Follow GEMS Desktop and Mobile patterns.
- Preserve usability, readable labels, and menu alignment.
- Keep dropdown menus within available screen space.
- Adapt surrounding layout instead of modifying official components.
- Do not invent responsive variants.

### 11.8 Accessibility

- Maintain visible focus indication.
- Associate labels and validation messages with controls.
- Preserve logical keyboard navigation.
- Distinguish selected, focused, hovered, and disabled states.
- Prevent interaction with disabled options.
- Use accessible names for icon-only triggers.
- Do not rely on color alone when text or accessible labels are necessary.

## 12. Strict AI Rules & Human Approval

### 12.1 Implementation Workflow

1. **Identify Data:** Determine option sources, selection rules, and permissions from HSD/BRD.
2. **Select Component:** Choose the correct GEMS General Dropdown configuration.
3. **Apply Properties:** Use only supported Type, State, Selected, Open, Checkbox, Divider, and related values.
4. **Compose Menu:** Use official Menu Items, Headers, and Scrollbar when required.
5. **Apply Foundation:** Follow official colors, typography, spacing, radius, effects, and icons.
6. **Follow UX Context:** Reference relevant GEMS Components, Page Samples, and UX Patterns.
7. **Implement Behavior:** Apply selection, search, validation, empty, error, and permission rules.
8. **Resolve Exceptions:** Request Human Approval if an unsupported component or essential business decision is required.

These are implementation instructions—not a separate validation report.

### 12.2 Strict Rules

**MUST**
- Use original GEMS General components.
- Preserve component references and supported properties.
- Follow relevant Foundation and component guidelines.
- Keep selected values and displayed content synchronized.
- Respect HSD/BRD and user permissions.
- Follow official GEMS contextual patterns.

**MUST NOT**
- Use Dropdown CCM or CCM-derived styling.
- Create custom Types, States, Sizes, or colors.
- Hardcode component styling.
- Treat `Selected` as a State.
- Confuse `Open=True/False` with `State=Open`.
- Invent unsupported Destructive, Filled, or Success properties.
- Add unsupported search or multi-selection.
- Invent option sources, labels, limits, or dependencies.
- Recreate official menu components manually.
- Change selected values silently.
- Override GEMS component specifications.

### 12.3 Human Approval

Request approval when:

- No suitable GEMS General Dropdown exists.
- Unsupported styling or interaction is required.
- Essential option sources or business behavior are undefined.
- The intended selection workflow cannot be determined safely.

Combine related questions into one confirmation.

**Fallback:** Use the closest supported GEMS General Dropdown component. If implementation requires invented styling or behavior, request Human Approval. Never use CCM.

## 13. Official Figma References & Related Guidelines

### 13.1 Main Components

| Component | Figma Reference |
|---|---|
| Dropdown Library | [GEMS Dropdown](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-4695) |
| Input Dropdown | [GEMS Input Dropdown](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-5034) |
| Dropdown | [GEMS Dropdown Component](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=410-3788) |

### 13.2 Supporting Components

| Component | Figma Reference |
|---|---|
| Dropdown List Item | [GEMS List Item](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=410-3081) |
| Dropdown Scrollbar | [GEMS Scrollbar](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=410-3457) |
| Dropdown List Header | [GEMS List Header](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=410-3132) |
| Input Dropdown Menu Item | [GEMS Menu Item](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=410-3138) |

### 13.3 Related Guidelines

**Foundation**
- `Foundation/color.md`
- `Foundation/typography.md`
- `Foundation/spacing-dan-radius.md`
- `Foundation/effect-styles.md`
- `Foundation/icons.md`
- `Foundation/misc-icons.md`
- `Foundation/design-annotations.md`

**Components**
- `components/input.md`
- `components/button.md`
- `components/button-group.md`
- `components/date-time-picker.md`

Use actual repository paths if component filenames differ.

### 13.4 GEMS Page Samples & UX Patterns

Read only relevant references for:

- Create / Edit Forms
- Detail Pages
- Search & Filters
- Data Tables
- Dashboard & Reports
- Empty / Error States
- Responsive Layouts

---

**FINAL RULE:** Every Dropdown MUST use an official GEMS General component with correct Type, State, Selected/Open behavior, menu structure, and product-specific option data. All visual properties MUST follow the official GEMS Foundations and related component guidelines. Never use CCM or invent unsupported configurations.
