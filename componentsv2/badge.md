
# GEMS Design System — Components / Badge

> **MANDATORY:** All Badges MUST use official GEMS General Badge components from the connected Figma Design System. Preserve original Type, Size, Icon, Color, styling, and supported behavior. **CCM components and CCM-derived styling are strictly prohibited.**

## 1. Purpose & Source of Truth

Badge is a compact visual component used to communicate status, category, condition, or short metadata associated with a record, process, or entity.

Badge helps users quickly recognize information in Tables, Lists, Cards, Dashboards, and Detail Pages.

**Core Principle:**

> Use Badge to communicate information—not to execute primary actions. Status labels and colors MUST reflect approved business meaning.

### 1.1 Primary Purposes

- Workflow status
- Approval status
- Active/inactive status
- Operational condition
- Category or classification
- Short metadata
- Other approved semantic information

### 1.2 Reference Priority

1. **Official GEMS General Badge:** Type, Size, Icon, Color, and styling.
2. **GEMS Components:** Badge usage within Table, Card, Detail, and other components.
3. **GEMS Page Samples & UX Patterns:** Contextual placement and consistency.
4. **Product HSD/BRD:** Status definitions, categories, business meaning, and permissions.
5. **Approved Semantic Mapping:** Status-to-color mapping established for the product.
6. **General UI/UX Principles:** Fallback when no specific GEMS guidance exists.

GEMS defines component styling. HSD/BRD defines business status and terminology.

Read only relevant references for the requested screen.

## 2. Component Selection Matrix

### 2.1 When to Use Badge

| Context | Purpose | Example |
|---|---|---|
| Workflow Status | Display process stage | Draft, Proposed, Processed, Finished |
| Approval Status | Display approval condition | Menunggu Persetujuan, Disetujui |
| Data Activation | Display active/inactive state | Aktif, Nonaktif |
| Operational Status | Display operational condition | Tersedia, Digunakan |
| Accommodation | Display room or accommodation condition | Terisi, Kosong |
| Transport | Display transport or placement status | Siap Ditempatkan |
| Meal Management | Display order/report status | Draft, Proposed, Finished |
| Category | Display classification | Staff, Non-Staff |
| Metadata | Display short information | Internal, Eksternal |

Examples are illustrative. Actual values MUST come from product requirements.

### 2.2 When NOT to Use Badge

| Requirement | Correct Component | Reason |
|---|---|---|
| Save data | Button | Action |
| Delete data | Button | Destructive action |
| Enable/disable setting | Toggle | Binary interaction |
| Select multiple items | Checkbox | Selection |
| Select one option | Dropdown / Radio | Selection |
| Show detailed error | Alert | System feedback |
| Show temporary notification | Toast / Notification | Event feedback |
| Change workflow status | Approved action/workflow control | Business transition |

### 2.3 Selection Rules

- Use Badge when information benefits from a compact visual label.
- SHOULD use Badge for status columns in GEMS Data Tables.
- SHOULD use Badge for important record status in Detail Pages.
- Use the same status representation across related screens.
- Do not use Badge as the default control for changing status.
- Do not assume every Badge is clickable.
- Do not add Badge solely for decoration.

## 3. Badge Component Structure

### 3.1 Available Properties

| Property | Official Values |
|---|---|
| `Size` | `sm`, `md`, `lg` |
| `Type` | `Pill color`, `Pill outline`, `Badge color`, `Badge modern` |
| `Icon` | `False`, `Dot`, `X close`, `Icon trailing`, `Icon leading`, `Text leading`, `Only`, `Country`, `Avatar` |
| `Color` | `Brand`, `Gray`, `Error`, `Warning`, `Success`, `Blue gray` / `Gray blue` as named in the selected Figma variant, `Blue light`, `Blue`, `Indigo`, `Purple`, `Pink`, `Orange` |

**Important:** Some Figma variants use `Gray blue`, while others use `Blue gray`. Preserve the exact variant name on the selected official component; do not rename properties manually.

### 3.2 Component Rules

- Use official GEMS General Badge instances.
- Preserve supported Type, Size, Icon, and Color combinations.
- Keep equivalent status Badges visually consistent.
- Do not create new component variants.
- Do not manually recreate Badge styling.
- Do not transfer CCM styling into General components.

## 4. Badge Types & Selection

### 4.1 Pill Color

Use when compact information requires a pill shape with semantic color emphasis.

**Typical contexts**
- Workflow status
- Operational condition
- Active/inactive status
- Category label

**Rules**
- Use official GEMS colors.
- Maintain consistent Type for equivalent status groups.
- Do not assign different colors to the same status without a defined reason.

### 4.2 Pill Outline

Use when a pill label requires an outlined visual treatment.

**Typical contexts**
- Metadata
- Category
- Secondary information
- Other approved contextual labels

**Rules**
- Preserve official outline and typography.
- Maintain readability.
- Do not assume Pill Outline automatically means the business information is unimportant.

### 4.3 Badge Color

Use when the relevant GEMS component or page requires a colored, non-pill Badge.

**Typical contexts**
- Table status
- Category
- Operational condition
- Short information label

**Rules**
- Use the official variant.
- Maintain consistent shapes across equivalent content.
- Do not switch between pill and non-pill styles merely for visual variety.

### 4.4 Badge Modern

Use only when a relevant GEMS component, Page Sample, or approved product pattern requires it.

**Rules**
- Preserve official styling.
- Do not make Badge Modern the universal default.
- Do not invent modernized versions of other Badge Types.

## 5. Badge Sizes

### 5.1 Available Sizes

| Size | Typical Context |
|---|---|
| `sm` | Compact Tables and Lists |
| `md` | Standard Cards and Detail information |
| `lg` | Context requiring more prominent information |

These are contextual recommendations; official GEMS component specifications take precedence.

### 5.2 Size Rules

- Use only `sm`, `md`, or `lg`.
- Preserve official dimensions, padding, radius, and typography.
- Keep Badge sizes consistent within the same Table column or status group.
- Follow relevant GEMS Page Samples and responsive layouts.
- Do not invent sizes or enlarge Badges solely for decoration.

## 6. Badge Colors & Semantic Meaning

### 6.1 Available Colors

| Color | General Usage Guidance |
|---|---|
| Gray | Neutral or low-emphasis information |
| Brand | Brand-related emphasis approved by GEMS |
| Error | Failure or relevant error condition |
| Warning | Attention or caution |
| Success | Successful or completed condition when business meaning supports it |
| Blue gray / Gray blue | Neutral classification or informational context |
| Blue light | Information or approved classification |
| Blue | Information or approved classification |
| Indigo | Approved classification |
| Purple | Approved classification |
| Pink | Approved classification |
| Orange | Approved classification |

These are semantic guidelines, not fixed status-to-color mappings.

### 6.2 Semantic Mapping Rules

- Status MUST come from HSD/BRD or approved product data.
- Color MUST come from official GEMS General variants.
- The same status with the same meaning MUST use consistent coloring within a product.
- Different statuses MAY share a color when their meanings justify it.
- Do not assign colors based solely on aesthetic preference.
- Do not assume every `Finished` status uses Success.
- Do not assume every `Draft` status uses Gray.
- Do not use Error or Warning for ordinary categories without semantic justification.
- Preserve previously approved product mappings.

### 6.3 Status-to-Color Mapping

Before implementing a set of statuses, establish the applicable mapping from available requirements or approved designs.

| Status Example | Business Meaning | Color |
|---|---|---|
| Draft | Defined by product | Approved semantic mapping |
| Proposed | Defined by product | Approved semantic mapping |
| Processed | Defined by product | Approved semantic mapping |
| Finished | Defined by product | Approved semantic mapping |
| Aktif | Defined by product | Approved semantic mapping |
| Nonaktif | Defined by product | Approved semantic mapping |

The table above does not establish final colors.

If a mapping is genuinely undefined and materially affects the design, propose a semantically appropriate GEMS color and request Human Approval before establishing it as a new product convention.

### 6.4 Status Consistency

- Preserve the same label and color across Table, Card, and Detail Page.
- Update Badge appearance when the underlying status changes.
- Do not change workflow meaning through color alone.
- Do not introduce unapproved statuses.

## 7. Badge Icon Variants

### 7.1 Available Icon Properties

| Icon | Usage |
|---|---|
| `False` | Text-only Badge |
| `Dot` | Compact status indicator |
| `X close` | Supported dismissible/removable Badge |
| `Icon trailing` | Supporting icon after label |
| `Icon leading` | Supporting icon before label |
| `Text leading` | Additional leading text |
| `Only` | Icon-only Badge when supported |
| `Country` | Country-related label |
| `Avatar` | Identity-related label |

### 7.2 Icon Rules

- Use only official GEMS icon variants.
- Follow `Foundation/icons.md`.
- Preserve icon dimensions, styling, placement, and color.
- Use `Icon=False` when an icon adds no information.
- Use `Dot` only when it provides meaningful semantic indication.
- Do not add decorative icons to every Badge.
- Icon-only Badges MUST have an accessible name.
- Do not invent icons or unsupported component combinations.

### 7.3 X Close Behavior

`X close` does not automatically mean the Badge may be removed.

A removable Badge requires:
- A supported GEMS component variant.
- Product requirements allowing removal.
- A defined consequence of removing the item.
- Appropriate keyboard and accessibility behavior.

Do not use X Close for ordinary workflow-status Badges.

### 7.4 _Badge close X

GEMS provides a separate internal component named `_Badge close X`.

Identified properties:

| Property | Values |
|---|---|
| `Type` | `Square`, `Rounded` |
| `Color` | Official GEMS component color variants |
| `State` | `Default`, `Hover` |

**Rules**
- Use the original component when required by an approved removable-Badge pattern.
- Preserve its official Type, Color, and State.
- Do not manually recreate a close icon.
- Do not interpret close-icon availability as authorization to delete business data.

## 8. Badge States & Interaction Behavior

### 8.1 Informational Badge

Badge is informational by default.

**Behavior**
- Displays the current status or category.
- Updates when the underlying data changes.
- Does not execute actions merely because it is clicked.
- Does not receive keyboard focus unless an interaction requires it.

### 8.2 Interactive Badge

Use interactive behavior only when:

1. The official GEMS component supports the interaction.
2. HSD/BRD or an approved UX Pattern establishes its purpose.
3. Business consequences are defined.
4. Accessibility requirements are satisfied.

**Rules**
- Do not make all Badges clickable.
- Do not automatically change statuses when Badges are clicked.
- Do not use Badge as a replacement for workflow action controls.
- Use supported removable-Badge behavior only when explicitly required.

## 9. Contextual Badge Patterns

### 9.1 Workflow Status

Use to display process stages in Tables, Cards, or Detail Pages.

**Examples**
- Draft
- Proposed
- Processed
- Finished

**Rules**
- Follow actual workflow definitions.
- Preserve labels and semantic mappings.
- Do not add or remove workflow stages.
- Do not use Badge as a status-transition Button.

### 9.2 Approval Status

Use only in modules with actual approval workflows.

**Examples**
- Menunggu Persetujuan
- Disetujui
- Ditolak

**Rules**
- Follow approved workflow and role permissions.
- Do not introduce approval statuses into modules without approval processes.
- Do not use Badge as Approve or Reject action.

### 9.3 Data Activation

Use to display whether a record is active or inactive.

| Requirement | Component |
|---|---|
| Display Aktif / Nonaktif | Badge |
| Change Aktif / Nonaktif | Toggle, when approved |

Do not confuse display status with the control used to change it.

### 9.4 Accommodation Status

**Examples**
- Terisi
- Kosong
- Reservasi

**Rules**
- Follow actual accommodation requirements.
- Distinguish room status from booking or request status.
- Do not invent status values.

### 9.5 Transport Status

**Examples**
- Draft
- Siap Ditempatkan
- Sudah Lengkap

**Rules**
- Follow actual transport workflows.
- Distinguish data completeness, passenger placement, and trip status.
- Do not reduce complex statuses to Aktif/Nonaktif.

### 9.6 Meal Management

**Examples**
- Draft
- Proposed
- Processed
- Finished

**Rules**
- Follow actual Meals workflow.
- Preserve status labels and approved colors.
- Do not introduce Approve/Reject statuses where the module does not support them.

### 9.7 Category Badge

**Examples**
- Staff
- Non-Staff
- Internal
- Eksternal

**Rules**
- Distinguish category from workflow status.
- Use approved GEMS semantic colors.
- Do not use Error/Warning colors for ordinary categories without a valid reason.

### 9.8 Badge in Data Table

**Recommended Pattern:** Use Badge for status columns when the relevant GEMS Table design supports it.

**Rules**
- Use consistent Badge Type and Size within equivalent rows.
- Preserve readable labels.
- Follow GEMS Table alignment and spacing.
- Keep status coloring consistent across the dataset.
- Do not replace row-action menus with Badges.
- Do not make Badges interactive unless approved.

### 9.9 Badge in Detail Page & Card

- Place Badge near the record information or status it describes.
- Preserve consistency with the corresponding Table/List.
- Follow relevant GEMS Card, Detail Page, and Page Header patterns.
- Do not invent alternative status labels for the same value.

### 9.10 Empty, Loading & Error States

**Empty**
- Follow official GEMS Empty State.
- Do not fabricate a status to avoid an empty value.

**Loading**
- Follow official GEMS Loading/Skeleton patterns.
- Do not invent Badge loading variants.

**Error**
- Use an appropriate GEMS Alert/Notification for errors.
- Do not treat Error-colored Badge as a replacement for complete error feedback.

## 10. Badge Labels & Content

### 10.1 Label Rules

- Use labels from HSD/BRD or approved product data.
- Keep labels concise and understandable.
- Preserve exact business meaning.
- Maintain consistent terminology across pages.
- Avoid unexplained abbreviations.
- Do not shorten labels in ways that change their meaning.

### 10.2 Language Consistency

- Follow the language used by the product.
- Maintain approved domain terminology.
- Avoid inconsistent Indonesian/English mixing.

### 10.3 Unknown Status

When status data is unavailable:

- Follow the approved product fallback.
- Do not automatically display Draft, Nonaktif, or Error.
- Use an approved neutral label only when appropriate.
- Do not fabricate status values or misleading colors.

## 11. Foundation, Layout & Accessibility

### 11.1 Foundation Integration

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | GEMS General semantic colors |
| `Foundation/typography.md` | Official GEMS Text Styles |
| `Foundation/spacing-dan-radius.md` | Spacing, padding, and radius |
| `Foundation/effect-styles.md` | Official effects when specified |
| `Foundation/icons.md` | General icons |
| `Foundation/misc-icons.md` | Specialized icons when applicable |
| `Foundation/design-annotations.md` | Additional approved specifications |

### 11.2 Visual Rules

- Preserve original component dimensions and properties.
- Use official GEMS General color variants.
- Apply official GEMS Text Styles.
- Maintain consistent alignment and spacing.
- Do not hardcode HEX, RGB, HSL, typography, or radius.
- Do not add arbitrary shadows or decorative effects.
- Do not use CCM styles.

### 11.3 Accessibility

**MUST**
- Keep Badge text readable.
- Communicate status meaning through text, not color alone.
- Maintain appropriate contrast.
- Provide accessible names for icon-only variants.
- Support keyboard interaction when the Badge is explicitly interactive.
- Keep informational Badges non-focusable unless required.

### 11.4 Responsive

- Follow official GEMS Page Samples and UX Patterns.
- Preserve readable labels.
- Use supported sizes appropriate to layout density.
- Maintain consistent status meaning across Desktop and Mobile.
- Do not invent responsive Badge variants.

## 12. AI Implementation Rules

### 12.1 Selection Workflow

When implementing Badge:

1. **Identify Information:** Determine whether the value represents status, category, condition, or metadata.
2. **Read HSD/BRD:** Identify approved labels and business meaning.
3. **Select Component:** Use official GEMS General Badge.
4. **Select Type & Size:** Choose supported variants according to the relevant UI context.
5. **Select Color:** Apply approved semantic mapping.
6. **Select Icon:** Use official options only when meaningful.
7. **Define Interaction:** Informational by default; interactive only when approved.
8. **Follow Context:** Apply relevant GEMS Components, Page Samples, and UX Patterns.
9. **Maintain Consistency:** Preserve labels and colors across related screens.
10. **Resolve Exceptions:** Request Human Approval for undefined semantic mappings or unsupported behavior.

These are implementation instructions, not a separate validation report.

### 12.2 Strict Rules

**MUST**
- Use official GEMS General Badge components.
- Preserve original Figma component references.
- Use supported Type, Size, Icon, and Color variants.
- Follow approved product status definitions.
- Maintain consistent semantic mappings.
- Follow GEMS Foundation guidelines.
- Use Badge as informational by default.

**MUST NOT**
- Use Badge CCM or CCM-derived styling.
- Create custom Types, Sizes, Icons, or colors.
- Hardcode component styling.
- Invent status labels or business categories.
- Choose colors purely for aesthetics.
- Assume Finished always means Success.
- Assume Draft always means Gray.
- Use Error for ordinary categories without justification.
- Make all Badges clickable.
- Interpret X Close as automatic permission to delete.
- Replace Button, Toggle, Alert, or workflow controls with Badge.
- Communicate status solely through color.
- Modify business workflows based on Badge appearance.

### 12.3 Human Approval

Request Human Approval when:

- No suitable GEMS General Badge configuration exists.
- A new semantic status-to-color mapping cannot be established from approved requirements.
- An unsupported visual or interactive variant is required.
- The business meaning of a status is unclear and affects design decisions.

Combine related questions into one confirmation.

**Fallback:** Use the closest supported GEMS General Badge configuration that accurately represents the information. If meaning or mapping cannot be established safely, request Human Approval. Never fabricate statuses or use CCM.

## 13. Official Figma References & Related Guidelines

### 13.1 Main Components

| Component | Figma Reference |
|---|---|
| Badge Library | [GEMS Badge Overview](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=345-5888) |
| Badge | [GEMS Badge Component](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=345-6118) |
| _Badge close X | [GEMS Badge Close](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=517-8953) |

### 13.2 Related Guidelines

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
- `components/toggle.md`
- `components/tooltip.md`
- Relevant GEMS Table, Card, Status, Alert, and Notification guidelines when available.

### 13.3 GEMS Page Samples & UX Patterns

Read only relevant references for:

- Data Tables and Lists
- Detail Pages
- Cards and Dashboards
- Workflow and Approval
- Operational Monitoring
- Empty and Error States
- Responsive Layouts

---

**FINAL RULE:** Badge MUST communicate accurate status, category, or short information using official GEMS General components. Apply supported Type, Size, Icon, and Color properties; use approved semantic mappings; maintain consistency across Tables, Cards, and Detail Pages; and treat Badge as informational unless interaction is explicitly supported. Never use CCM or invent unsupported status behavior.
