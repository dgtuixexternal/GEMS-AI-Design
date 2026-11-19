
# GEMS Design System — Components / Data Table

> **MANDATORY:** All Data Tables MUST use official GEMS General Table components and supported Figma variants. AI MUST determine table structure, columns, content, and interactions based on product requirements, actual data, and relevant GEMS Page Samples & UX Patterns. CCM components and unsupported table designs are strictly prohibited.

> **CORE PRINCIPLE:** A good Data Table prioritizes relevant information, readability, and efficient user actions—not the number of columns, controls, or features.

## 1. Sources & Priority

**Official Figma References**
- [GEMS Data Display — Overview](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=23-1133)
- [GEMS Table Cell](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=347-7870)
- [GEMS Table Header Cell](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=347-9377)
- [GEMS Table Header](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1238-861)
- [GEMS Table — General](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1239-2391)
- [GEMS Table Action Base](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3170-51728)
- [GEMS Action Buttons & Icons](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3170-52403)
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1105-7310)

**Priority Order**
1. **GEMS General Table Components:** Official structure, variants, states, and visual specifications.
2. **GEMS Foundation:** Color, typography, spacing, radius, effects, and icons.
3. **GEMS Page Samples & UX Patterns:** Table composition, actions, filtering, selection, and responsive usage.
4. **HSD/BRD:** Data fields, business rules, permissions, statuses, and workflow behavior.
5. **Actual System Data:** Records, values, totals, and available actions.
6. **General UI/UX Principles:** Fallback when GEMS has no specific guidance.

GEMS defines visual implementation. HSD/BRD and actual data determine table content and functionality.

Read only the relevant Figma components and examples required for the current task.

---

## 2. Purpose & When to Use

Data Table displays structured records in rows and columns to support reading, comparing, locating, managing, and acting on information.

**Use Data Table when users need to:**
- View multiple records.
- Compare consistent attributes.
- Search or filter structured data.
- Inspect statuses across records.
- Sort information when supported.
- Select records for authorized actions.
- Access details, edit records, or execute other permitted workflows.

### Table vs Other Components

| Information Need | Recommended Component |
|---|---|
| Multiple structured records | Data Table |
| Exact values across records | Data Table |
| Single record details | Detail Page / Detail Component |
| Small collection of visually rich items | Card / List when appropriate |
| High-level metrics | KPI / Statistic Card |
| Trends or comparisons | Chart |
| Individual record status | Badge within Table |
| No records | Empty State |
| Create or edit data | Form / Modal / Relevant UX Pattern |

**Selection Rules**
- Use Table when row-column comparison improves usability.
- Do not force every dataset into a Table.
- Prefer Cards or Lists when content is primarily visual or does not benefit from tabular comparison.
- Do not overload Tables with unrelated information.
- Do not invent columns or actions solely to make the Table appear complete.

---

## 3. Official GEMS Table Components

| Component | Responsibility |
|---|---|
| `Table` | Complete table composition |
| `Table cell` | Row content and supported cell styles |
| `Table header cell` | Header-cell layout |
| `Table header` | Column labels, help, and sorting indicators |
| `Action Buttons & Icons` | Supported row actions |
| Supporting components | Badge, Avatar, Checkbox, Dropdown, Input, etc. |

**Component Rules**
- MUST use official GEMS General component instances.
- MUST preserve existing Figma component references.
- MUST use supported properties and variants.
- MUST follow official typography, colors, spacing, and interaction states.
- MUST NOT detach or manually reconstruct reusable GEMS components.
- MUST NOT replace General components with visually similar CCM components.

### Strict CCM Restriction

The referenced GEMS file includes:
- `Table CCM`
- `Pagination CCM`
- `Action Buttons & Icons` → `Property 1=CCM`

**All CCM table components, variants, pagination patterns, and actions are prohibited.**

For `Action Buttons & Icons`, use the official `Default` variant, never `CCM`.

Do not use a CCM example as the source of General Table structure.

---

## 4. Table — Available Variants

### Official Properties

| Property | Available Values |
|---|---|
| `Example` | `Team members`, `Sales`, `Companies`, `Files`, `Tenant List`, `Event Table`, `Approval` |
| `Breakpoint` | `Desktop`, `Mobile` |
| `Dividers` | `Divider line`, `Alternating fills` |

These are official example variants. Their availability differs by example and breakpoint.

### Example Usage

| Example | Appropriate Context |
|---|---|
| `Team members` | People, users, employees, or team records |
| `Sales` | Transactional or numerical records |
| `Companies` | Company or organization records |
| `Files` | Documents and file-related information |
| `Tenant List` | Tenant or entity lists with similar structure |
| `Event Table` | Event or schedule-related records |
| `Approval` | Records involving approval workflows |

**Rules**
- Select the closest relevant General Table example based on data structure.
- Examples are layout references, not permission to copy unrelated business fields.
- Use only officially available variant combinations.
- Adapt content according to HSD/BRD without replacing the official GEMS component structure.
- Do not invent an `Example` property value.
- Do not use Approval-specific actions unless the product actually includes approval behavior.

### Divider Selection

**`Divider line`**
- Separates rows using official GEMS divider treatment.
- Suitable for standard structured record tables.

**`Alternating fills`**
- Differentiates rows using official alternating background treatment.
- Suitable when available and consistent with the selected Table example.

**Rules**
- Choose divider treatment according to the relevant GEMS Page Sample.
- Preserve official fill and border tokens.
- Do not combine divider treatments into a custom style.
- Do not apply alternating fills manually when an official variant exists.

---

## 5. Table Cell — Available Styles

GEMS Table Cell supports multiple content styles, including:

| Cell Style | Purpose |
|---|---|
| `Text` | Standard text values |
| `Lead text` | Primary record identifier |
| `Lead Item Lists` / `Item Lists` | List-based cell content |
| `Badge` | Status or category labels |
| `Badges multiple` | Multiple supported labels |
| `Avatar` / `Lead avatar` | Person-related information |
| `Avatar group` | Multiple related people |
| `Lead icon` | Primary item with an icon |
| `Payment method` | Payment-related information |
| `Checkbox only` / `Lead checkbox` | Record selection |
| `Radio button only` / `Lead radio button` | Single-choice selection |
| `Toggle only` / `Lead toggle` | Supported binary control |
| `Dropdown` | Supported inline selection |
| `Date Range` | Date-range content |
| `Text Field` | Supported inline text editing |
| `Trend positive` / `Trend negative` | Positive or negative change |
| `Progress bar` | Measurable progress |
| `Star ratings` | Rating information |
| `Action icons` | Compact row actions |
| `Action buttons` | Row actions with labels |
| `Action dropdown icon` | Actions inside a menu |
| `Action buttons & icons` | Supported combined action layout |

GEMS also contains combinations of lead content with icons, avatars, payment methods, checkboxes, radio buttons, and toggles.

### Cell Properties

| Property | Examples |
|---|---|
| `Style` | Official cell styles |
| `Supporting text` | `True`, `False` where supported |
| `State` | `Default`, `Hover`, `Opened` where supported |

**Rules**
- Choose Cell Style according to the data type and purpose.
- Use `Lead text` for important identifying information when suitable.
- Use `Supporting text=True` only when secondary information adds value.
- Do not place multiple unrelated values in one cell merely to save columns.
- Use `Hover` or `Opened` only where supported by the selected component.
- Do not assume every Cell Style provides every State combination.
- Do not use editable controls in read-only tables without an actual editing requirement.
- Do not invent custom cell styles.

---

## 6. Table Header & Sorting

### Table Header Cell

Official properties:

| Property | Values |
|---|---|
| `Text` | `True`, `False` |
| `Checkbox` | `True`, `False` |
| `Color` | `White`, `Gray` |

Use only the combinations provided by GEMS.

### Table Header

Official properties:

| Property | Available Values |
|---|---|
| `Help icon` | `True`, `False` |
| `Arrow` | `False`, `Up`, `Down`, `Up & Down` |
| `State` | `Default`, `Hover` |

### Sorting Rules

- Sorting MUST correspond to actual sortable data.
- `Up` and `Down` MUST accurately reflect the active direction.
- `Up & Down` may indicate an available sorting control according to GEMS.
- `Arrow=False` is appropriate for columns without sorting.
- Do not add sorting to columns that cannot support meaningful ordering.
- Do not assume every header is sortable.
- Preserve the active sort state when navigating within the same table context if required.
- Use official GEMS header icons and states.

### Header Content

- Use concise, business-appropriate column names.
- Include units when necessary.
- Avoid ambiguous abbreviations.
- Use `Help icon=True` only when a column genuinely needs additional explanation.
- Help interactions MUST follow GEMS Tooltip guidelines.

---

## 7. Column Selection & Information Hierarchy

AI MUST determine table columns from HSD/BRD and user tasks.

### Recommended Column Priority

1. **Record Identity:** Name, reference number, or primary identifier.
2. **Essential Attributes:** Information needed to distinguish records.
3. **Operational Information:** Relevant dates, quantities, or categories.
4. **Workflow Status:** Current business state when applicable.
5. **Actions:** Permitted operations for each record.

This is a hierarchy guideline, not a requirement to include every category.

### Column Rules

- Prioritize fields users need for scanning, comparing, and deciding.
- Preserve actual business field names.
- Avoid unnecessary or redundant columns.
- Do not display sensitive information without authorization.
- Use appropriate alignment for text, numbers, and actions.
- Preserve readable column widths according to GEMS patterns.
- Do not arbitrarily truncate important identifiers.
- Use supporting text where it improves understanding.
- Do not invent fields merely to fill an available table template.

### Column Count

- No fixed column count should be invented without product requirements.
- Select columns based on relevance and available screen space.
- On constrained layouts, prioritize critical fields and follow official GEMS Mobile patterns.
- Do not hide essential information without an accessible alternative.

---

## 8. Status & Badge Usage

**Record statuses SHOULD use official GEMS Badge components when appropriate.**

Typical contexts:
- Draft.
- Submitted.
- In Progress.
- Approved.
- Rejected.
- Completed.
- Cancelled.

These are examples only. Actual status names and transitions MUST come from HSD/BRD.

### Rules

- Use official GEMS Badge variants.
- Apply semantic colors based on status meaning.
- Follow `components/badge.md`.
- Do not create custom status pills.
- Do not use Button styling to represent passive status.
- Do not make Badge interactive unless supported by the actual product behavior.
- Do not invent workflow statuses or transitions.
- Maintain consistent status terminology across Table, Detail Page, Filters, and Reports.

---

## 9. Row Actions & CRUD

Row actions MUST reflect available functionality and user permissions.

### Typical Actions

| Action | Purpose | Expected Behavior |
|---|---|---|
| View Detail | Inspect record information | Open approved detail flow |
| Edit | Modify existing record | Open approved edit flow |
| Delete | Remove record | Follow confirmation requirements |
| Download | Download available file | Use authorized file action |
| Other Actions | Product-specific operations | Follow HSD/BRD |

Do not assume all actions are available for every record.

### Action Presentation

Use official GEMS variants for:
- `Action icons`
- `Action buttons`
- `Action dropdown icon`
- `Action buttons & icons`

**Rules**
- Select the action presentation according to GEMS usage examples and available space.
- Use official General Action Buttons & Icons, never the CCM variant.
- Use icons defined by `Foundation/icons.md`.
- Provide accessible names for icon-only actions.
- Do not place all actions directly in a row when an official action menu is more appropriate.
- Do not invent actions to make the Table appear functional.
- Respect role-based permissions and record statuses.

### CRUD Workflow

**Create**
- Use the approved page-level action or form pattern.
- Do not assume Create must be available within every Table.

**View**
- Use the approved Detail Page or modal pattern.
- Preserve the record context.

**Edit**
- Use the official Form, Modal, or Inline Editing pattern when supported.
- Do not enable direct cell editing without requirements.

**Delete**
- Use confirmation when required by the approved workflow.
- Follow GEMS Modal and Background Overlay guidelines.
- Show resulting feedback using official Notification or Alert as appropriate.

---

## 10. Row Selection & Bulk Actions

Use selection controls only when users need to select one or multiple records.

### Selection Rules

- Use official GEMS Checkbox or Radio Button cell variants.
- Checkbox is appropriate for supported multiple selection.
- Radio Button is appropriate for supported single selection.
- Use header checkbox only when the table supports bulk selection.
- Do not show selection controls without a selection-related task.
- Do not invent bulk actions or permissions.
- Preserve selection state accurately across filtering and pagination according to business requirements.

### Bulk Actions

Examples may include:
- Export selected records.
- Download selected files.
- Delete selected records.
- Apply an approved status change.

**Rules**
- Bulk actions MUST be defined by product requirements.
- Disabled or unavailable actions MUST reflect actual permissions and record states.
- Destructive bulk actions MUST follow the relevant confirmation workflow.
- Do not assume a bulk action applies to records outside the current selection.

---

## 11. Search, Filter & Pagination

### Search

Use search when users need to locate records by known attributes.

**Rules**
- Searchable fields MUST come from actual data.
- Use official GEMS Search/Input components.
- Do not invent search behavior or unsupported searchable fields.
- Preserve appropriate feedback when no matching records exist.

### Filter

Use filters when users need to narrow a dataset.

Possible filters when supported:
- Status.
- Date range.
- Category.
- Department.
- Location.
- Other business attributes.

**Rules**
- Use official GEMS Dropdown, Date Picker, and related controls.
- Filter options MUST match actual business values.
- Keep displayed records consistent with selected filters.
- Do not add unnecessary filters merely to fill a toolbar.
- Follow GEMS Page Samples for filter position and composition.

### Pagination

Use official GEMS General pagination behavior and components where available.

**Rules**
- **Pagination CCM is strictly prohibited.**
- Do not copy Pagination CCM structure or styling.
- Do not invent page sizes, total counts, or navigation behavior.
- Pagination MUST reflect actual record counts and selected filters.
- Preserve the current page or reset it appropriately when filters change, according to product behavior.
- If an approved General pagination component is unavailable, request Human Approval instead of using CCM.

---

## 12. Table States & Interaction

### Common States

| State | Expected Behavior |
|---|---|
| Default | Display available records |
| Hover | Use official GEMS hover styling |
| Selected | Reflect actual selection when supported |
| Opened | Show the relevant open control state |
| Loading | Display official GEMS Loading/Skeleton pattern |
| Empty | Show official GEMS Empty State |
| No Search Results | Explain that no records match the criteria |
| Error | Show appropriate GEMS error feedback |
| Updated | Reflect confirmed changes to records |

### Rules

- Do not fabricate records to avoid an Empty State.
- Distinguish between no data and no matching search/filter results.
- Do not use hover styling as the only indication of selection.
- Do not assume all rows are clickable.
- Row navigation requires a supported destination.
- Do not introduce inline editing or drag-and-drop without an approved workflow.
- Preserve actual data and interaction state.

---

## 13. Desktop & Mobile Behavior

### Desktop

- Use official `Breakpoint=Desktop` variants.
- Preserve column hierarchy, readable spacing, and action placement.
- Use supported divider treatment and states.
- Avoid excessive horizontal content where possible.

### Mobile

- Use official `Breakpoint=Mobile` variants.
- Prioritize essential record information.
- Preserve important statuses and actions.
- Follow the actual GEMS Mobile Table example.
- Do not simply shrink the Desktop table.
- Do not invent alternative Card layouts without a relevant GEMS pattern or approval.
- Do not remove critical information merely to fit the screen.

### Responsive Rules

- Choose supported variants according to the target screen.
- Preserve readable typography, touch targets, and row relationships.
- Follow GEMS Page Samples and UX Patterns.
- Request Human Approval for unsupported responsive transformations.

---

## 14. Table Content & Data Integrity

### Data Rules

- Use actual record values or clearly identified prototype data.
- Preserve business terminology and identifiers.
- Use consistent formats for dates, numbers, currencies, and units.
- Keep row values aligned with their column meanings.
- Do not invent statuses, actions, record counts, or business relationships.
- Respect field-level permissions and sensitive data restrictions.
- Keep Table values consistent with Detail Pages and Reports.

### Prototype Data

When live data is unavailable:
- Prefer provided sample data.
- Use clearly illustrative dummy data only when the prototype permits it.
- Do not represent dummy values as real records.
- Do not invent business conclusions from sample data.

### Data Changes

- Reflect confirmed Create, Update, and Delete results.
- Do not show a successful change before it is confirmed.
- Keep pagination, filters, and displayed totals consistent after updates.
- Use official GEMS Notification for brief action feedback.
- Use official Alert for important persistent contextual information.

---

## 15. Foundation & Component Dependencies

All Table components MUST follow existing GEMS Foundation guidelines.

### Foundation References

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | Official General colors, text, borders, fills, status colors |
| `Foundation/typography.md` | Headers, cell text, supporting text, labels |
| `Foundation/spacing-dan-radius.md` | Cell padding, row spacing, containers, radius |
| `Foundation/effect-styles.md` | Approved effects where applicable |
| `Foundation/icons.md` | Sorting, row actions, navigation, controls |
| `Foundation/misc-icons.md` | Specialized icons where appropriate |
| `Foundation/design-annotations.md` | Official component specifications |

### Related Components

| Requirement | Related Guideline |
|---|---|
| Record statuses | `components/badge.md` |
| Row action buttons | `components/button.md` |
| Combined actions | `components/button-group.md` where applicable |
| Search fields | `components/input.md` |
| Dropdown filters | `components/input-dropdown.md` |
| Date filters | GEMS Date & Time Picker |
| Row selection | GEMS Checkbox / Radio Button |
| Inline binary controls | GEMS Toggle |
| Row identity | GEMS Avatar |
| Contextual explanation | `components/tooltip.md` |
| Confirmation dialogs | GEMS Modal + `components/bg-overlay.md` |
| Action feedback | `components/notification.md` |
| Contextual warnings | `components/alert.md` |
| Data analytics | `components/chart.md` |

Use actual repository paths if filenames differ.

### Visual Rules

- Preserve original GEMS General Table component references.
- Apply official GEMS Text Styles.
- Use GEMS General colors and semantic tokens.
- Preserve official cell padding, spacing, radius, dividers, and effects.
- Use official GEMS icons and icon sizes.
- Do not add decorative shadows unless defined by the official pattern.
- Do not hardcode custom HEX/RGB/HSL, typography, or unsupported dimensions.
- Do not use CCM styling under any circumstances.

---

## 16. Accessibility

**MUST**
- Provide clear and understandable column headers.
- Preserve logical row-column relationships.
- Maintain readable text and contrast.
- Ensure selection controls and actions are keyboard accessible.
- Give icon-only actions accessible names.
- Preserve visible focus and selected states.
- Communicate status through text, not color alone.
- Keep sorting direction understandable.
- Maintain usability across supported breakpoints.

**MUST NOT**
- Hide essential information behind hover-only interactions.
- Use ambiguous action icons without accessible labels.
- Make every row interactive without a meaningful destination.
- Remove relevant column context for visual minimalism.
- Introduce inaccessible custom interactions.

---

## 17. Strict AI Rules

### MUST

1. Use official **GEMS General Table** components.
2. Select appropriate Table examples and supported variants.
3. Determine columns based on actual data and user tasks.
4. Use official Table Cell and Table Header configurations.
5. Use GEMS Badge for applicable status values.
6. Use official General Action Buttons & Icons for row actions.
7. Follow actual role permissions and CRUD workflows.
8. Use official search, filter, and pagination patterns when required.
9. Follow GEMS Foundation and relevant Page Samples & UX Patterns.
10. Preserve data accuracy, responsiveness, and accessibility.
11. Request Human Approval for unsupported components or behaviors.

### MUST NOT

1. **Use Table CCM, Pagination CCM, or Action Buttons & Icons CCM.**
2. Create custom, detached, or duplicate GEMS Tables.
3. Invent unsupported Cell Styles, Table variants, or states.
4. Add unnecessary columns, actions, filters, or selection controls.
5. Invent business fields, statuses, records, totals, or workflows.
6. Use passive Badge as an action control.
7. Enable inline editing without an approved requirement.
8. Add bulk actions without an authorized selection workflow.
9. Assume every Table supports sorting, search, or row navigation.
10. Fabricate records to avoid Empty States.
11. Shrink Desktop Tables to imitate Mobile variants.
12. Hardcode styling outside official GEMS.
13. Substitute CCM patterns when a General component is unavailable.
14. Implement unsupported designs or interactions without Human Approval.

---

## 18. AI Table Selection Decision

When designing a List, Management, or Data Display page:

1. **Identify User Goal:** Determine what users need to find, compare, review, or manage.
2. **Inspect Data:** Read HSD/BRD for fields, records, statuses, permissions, and workflows.
3. **Choose Component:** Decide whether Table, Card, List, KPI, or Chart is most appropriate.
4. **Select GEMS Table:** Choose the closest supported General example, Breakpoint, and Divider variant.
5. **Define Columns:** Prioritize identifiers, relevant attributes, status, and authorized actions.
6. **Select Cell Styles:** Use official Text, Badge, Avatar, Checkbox, Action, or other supported variants.
7. **Define Interactions:** Apply sorting, search, filters, selection, and pagination only when needed.
8. **Define States:** Follow official Loading, Empty, Error, Hover, and other applicable patterns.
9. **Apply Foundation:** Preserve official GEMS colors, typography, spacing, radius, effects, and icons.
10. **Follow GEMS Context:** Reference relevant Page Samples and UX Patterns for actual composition.

### Human Approval

Request approval when:
- No suitable GEMS General table composition exists.
- A new interaction or unsupported cell variant is required.
- New bulk actions or business workflows are proposed.
- A custom responsive transformation is necessary.
- The required General pagination pattern is unavailable.

Combine related approval questions into one confirmation to minimize Claude AI context usage.

### Fallback

If a requested table pattern is unsupported:
1. Prefer an existing GEMS General variant that preserves required functionality.
2. Consider an official alternative component if it communicates the information more clearly.
3. Request Human Approval before implementing a new composition.
4. Never substitute CCM components.

> **FINAL INSTRUCTION:** Use official **GEMS General Data Table** components only when structured records benefit from tabular presentation. AI MUST prioritize relevant columns, accurate data, readable status, appropriate actions, and efficient workflows. Follow GEMS Foundation and Page Samples, preserve original Figma references, and strictly prohibit all CCM components.
