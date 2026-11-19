
# GEMS Design System — Dashboard Guidelines

> **MANDATORY:** All dashboards MUST use official GEMS General Design System components, foundations, and approved dashboard patterns. AI MUST analyze business requirements before selecting KPIs, charts, tables, filters, or layouts. Use GEMS Dashboard Style01, Style02, or Style03 only. CCM designs, components, variants, and styling are strictly prohibited.

**Execution:** Claude AI + Figma MCP
**Scope:** Dashboard UI/UX Design Generation
**Governance:** Human-in-the-Loop
**Instruction Priority:** Mandatory

## 1. Dashboard Design Principles

A GEMS Dashboard is a decision-support interface that presents meaningful information according to the product's business objectives and user roles.

**Core Principles**
1. Data determines the visualization, not the opposite.
2. Every KPI, Chart, Table, and Filter MUST have a meaningful purpose.
3. Information hierarchy MUST prioritize the user's most important decisions.
4. Use only relevant components and sections; do not fill unused space with unnecessary visualizations.
5. Preserve visual consistency with GEMS General Design System.
6. Follow approved HSD/BRD for all metrics, calculations, permissions, and interactions.
7. Use responsive layout and supported component variants.
8. Never use CCM or create unsupported GEMS variants.

**Critical Rule:**

> The number of charts does not determine dashboard quality. If information is clearer as a KPI Card or Data Table, AI MUST NOT force it into a chart.

---

## 2. Source of Truth & Priority

AI MUST use the following source hierarchy:

| Priority | Source | Responsibility |
|---|---|---|
| 1 | Approved HSD/BRD & Data | Business requirements, KPI definitions, calculations, permissions |
| 2 | GEMS Component Guidelines | Component selection, usage, variants, states, and behavior |
| 3 | Official GEMS Figma | Component instances, variables, visual properties |
| 4 | GEMS Dashboard Style01–03 | Approved dashboard layout and visual composition |
| 5 | GEMS Page Samples & UX Patterns | Contextual layout, interaction, and CRUD behavior |
| 6 | Approved ISS Dashboard References | Practical dashboard composition examples |

**Rules**
- Read only relevant guidelines and references for the current dashboard.
- Follow official GEMS components and existing library properties.
- References provide design guidance, not permission to copy unrelated business content.
- ISS examples MUST NOT override GEMS component rules or Foundation tokens.
- If requirements conflict, distinguish business-rule conflicts from visual-specification conflicts.
- Request Human Approval for material unresolved conflicts.
- Never invent unavailable component specifications or business data.

---

## 3. Approved Dashboard Styles

The official GEMS Dashboard page contains multiple design sections.

**ONLY THESE THREE STYLES ARE ALLOWED:**

| Style | Official Section | Usage |
|---|---|---|
| Style01 | `Style01` | Approved GEMS dashboard layout reference |
| Style02 | `Style02` | Approved GEMS dashboard layout reference |
| Style03 | `Style03` | Approved GEMS dashboard layout reference |

AI MUST inspect the actual content of all three official GEMS styles when selecting a dashboard direction.

### 3.1 Style Selection Rules

AI MUST:
- Evaluate the product's data complexity, content hierarchy, and dashboard objectives.
- Select the most suitable existing GEMS dashboard style.
- Follow its relevant layout structure, proportions, spacing, and visual hierarchy.
- Adapt content, KPI definitions, chart selection, and sections to actual business requirements.
- Preserve the official GEMS General component styling.
- Maintain consistency when multiple dashboard pages belong to the same product.

AI MUST NOT:
- Automatically select Style01 for every product.
- Combine unrelated layout elements from different styles without a clear functional reason.
- Copy all sections from a sample when the product does not need them.
- Invent a fourth dashboard style.
- Recreate dashboard components with custom Frames when official GEMS components exist.

### 3.2 Strict CCM Exclusion

The GEMS Dashboard Figma page also contains a section named:

`Dashbord / CCM / Option 1`

**THIS SECTION IS PROHIBITED.**

AI MUST NOT:
- Use `Dashbord / CCM / Option 1` as a dashboard reference.
- Copy its layout, colors, visual hierarchy, or component styling.
- Use `Horizontal tabs CCM` or any CCM-specific component.
- Use CCM-specific KPI Cards, charts, filters, navigation, or visual properties.
- Substitute CCM brand colors for GEMS General colors.
- Reuse CCM styling because it appears visually similar to GEMS.
- Use CCM as a fallback when a General component is unavailable.

**Selection Rule:**

`GEMS Style01 / Style02 / Style03 → Official GEMS General Components → Approved Product Content`

Never:

`CCM Dashboard → GEMS Dashboard`

**Important:** A frame's name alone is insufficient to establish which style it belongs to. Identify Style01, Style02, and Style03 through their parent sections in the official GEMS Dashboard page.

---

## 4. Dashboard Content & Information Hierarchy

AI MUST determine content based on business meaning and data availability.

### 4.1 Recommended Information Hierarchy

Use the relevant GEMS style to organize:

1. **Page Header:** Dashboard title, description, and necessary page actions.
2. **Global Filters:** Relevant date periods and dimensions.
3. **KPI Summary:** High-priority values and operational indicators.
4. **Analytical Content:** Appropriate charts, comparisons, and trends.
5. **Detailed Information:** Supporting tables, rankings, or operational records.
6. **Contextual Actions:** Navigation, export, or drill-down when required.

This represents a logical hierarchy, not a mandatory fixed layout.

AI MUST follow the selected official GEMS style for actual composition and placement.

### 4.2 Content Selection Matrix

| Information Need | Preferred Presentation |
|---|---|
| Single important metric | KPI Card |
| Comparison across categories | Bar Chart |
| Change over time | Line Chart |
| Part-to-whole composition | Pie / Doughnut Chart when appropriate |
| Progress toward a defined target | Supported Gauge / Progress visualization |
| Multiple comparable dimensions | Radar Chart when analytically justified |
| Detailed operational records | Data Table |
| Current workflow status | Badge |
| Historical actions | Activity Feed |
| No available data | Empty State |

AI MUST NOT automatically generate every component in this matrix.

---

## 5. KPI Cards & Metrics

KPI Cards communicate important numerical information that supports user decisions.

### 5.1 KPI Selection

A KPI MUST have:
- A meaningful business definition.
- A reliable data source.
- A defined calculation or aggregation method.
- A clear unit or format.
- A relevant relationship to dashboard objectives.

Examples of possible KPIs:
- Total requests.
- Active records.
- Completed transactions.
- Pending items.
- Total operational volume.
- Percentage of utilization.

These are examples, not mandatory dashboard metrics.

### 5.2 KPI Rules

AI MUST:
- Prioritize important KPIs.
- Use consistent number formatting.
- Include relevant units.
- Display comparison periods only when data supports them.
- Explain increases or decreases accurately.
- Use official GEMS components and styling.

AI MUST NOT:
- Create KPIs solely to fill the grid.
- Invent calculations or comparison values.
- Display percentage changes without a valid baseline.
- Assume an increase is always positive or a decrease is always negative.
- Use unsupported decorative KPI Cards.

### 5.3 KPI Calculation Principles

- Define numerator and denominator for percentages.
- Identify aggregation rules: sum, average, count, ratio, or distinct count.
- Clarify whether metrics represent actual, planned, estimated, or target values.
- Use consistent units and periods.
- Distinguish zero values from missing data.
- Never show fabricated performance trends.

---

## 6. Chart Selection & Usage

All charts MUST follow the existing GEMS `componentsv2/chart.md` guideline.

### 6.1 Chart Selection Matrix

| Chart | Appropriate Usage |
|---|---|
| Line Chart | Trends and time-series analysis |
| Vertical Bar Chart | Comparisons across categories or periods |
| Horizontal Bar Chart | Comparisons where category labels benefit from horizontal layout |
| Bar & Line Chart | Related metrics with compatible analytical meaning |
| Pie / Doughnut Chart | Meaningful part-to-whole proportions |
| Activity Gauge | Progress against an approved target |
| Radar Chart | Comparable multidimensional assessments |

The selected chart MUST exist in the official GEMS General library.

### 6.2 Chart Rules

AI MUST:
- Select chart types according to data structure and analytical purpose.
- Use official chart variants and styling.
- Include meaningful titles, labels, units, and legends when required.
- Maintain consistent data categories and time periods.
- Use GEMS semantic and data-visualization colors.
- Follow supported axis, grid, and tooltip behavior.
- Use official Card Header and related components where applicable.

AI MUST NOT:
- Use any CCM chart or CCM-specific chart styling.
- Invent chart types or visual variants.
- Use decorative charts without analytical value.
- Misrepresent data with misleading scales.
- Use Pie/Doughnut charts for unsuitable comparisons.
- Use Radar charts without meaningful comparable dimensions.
- Force charts where KPI Cards or Data Tables communicate information better.
- Invent data, targets, percentages, or trends.

### 6.3 Chart Interaction

Use only interactions supported by the selected chart component and approved requirements:
- Tooltip.
- Legend.
- Filtering.
- Period selection.
- Drill-down.
- Export.
- Detail navigation.

Do not introduce unsupported interactions or assume every chart must be clickable.

---

## 7. Filters & Dashboard Periods

Dashboard filters MUST follow official GEMS Input, Input Dropdown, Date & Time Picker, Button Group, and related guidelines.

### 7.1 Filter Selection

Use filters only when relevant to the dashboard's content.

Possible filter dimensions:
- Date / period.
- Location.
- Department.
- Category.
- Status.
- Operational area.
- Other approved product-specific dimensions.

AI MUST select the appropriate official GEMS component based on the filter's function and documented component rules.

**Never replace an official Input-based filter with Dropdown or Button Group solely for visual preference.**

### 7.2 Dashboard Periods

Potential periods:
- Hari Ini.
- Minggu Ini.
- Bulan Ini.
- Tahun Ini.
- Custom Periode.

These periods are options, not mandatory defaults.

AI MUST obtain approval for:
- Supported periods.
- Default period.
- Filter-based navigation versus separate dashboard views.
- Aggregation behavior.
- Data availability.

### 7.3 Filter Behavior

AI MUST:
- Apply active filters consistently to related KPIs, Charts, and Tables.
- Preserve logical relationships between filters.
- Keep date-range interpretation consistent.
- Use supported selected, default, disabled, and error states.
- Provide reset behavior when applicable.
- Update dependent content according to the approved workflow.

AI MUST NOT:
- Add unnecessary filters.
- Invent filter values.
- Show contradictory data across sections using the same filter context.
- Reset unrelated filters without approved behavior.
- Assume all dashboard widgets use the same filter when HSD/BRD specifies different scopes.

---

## 8. Data Tables & Detailed Information

Use official GEMS Data Table components for detailed information that benefits from structured rows and columns.

### Rules

AI MUST:
- Select columns based on actual data requirements.
- Follow GEMS Table, Badge, Pagination, and related guidelines.
- Provide relevant filters and sorting only when supported.
- Display status using official GEMS Badge components.
- Preserve consistency between chart summaries and their underlying records.
- Support relevant detail navigation when required.

AI MUST NOT:
- Convert detailed records into charts unnecessarily.
- Add unrelated columns or actions.
- Invent records to fill a table.
- Use CCM tables, badges, pagination, or controls.
- Add CRUD actions without role permissions and business requirements.

---

## 9. Dashboard Layout & Component Integration

### 9.1 Mandatory Component Usage

AI MUST use the official GEMS General component library for all applicable elements.

| Requirement | Guideline |
|---|---|
| Page navigation | `Foundation/application-navigation` |
| Page title and actions | `componentsv2/page-header.md` |
| Section or card headings | `componentsv2/section-header.md`, `card-header.md` |
| Buttons | `componentsv2/button.md` |
| Filter controls | `componentsv2/input.md`, `input-dropdown.md` |
| Date selection | `componentsv2/date-time-picker.md` |
| View switching | `componentsv2/tabs.md`, `button-group.md` |
| Charts | `componentsv2/chart.md` |
| Data status | `componentsv2/badge.md` |
| Data classification | `componentsv2/tag.md` |
| Pagination | `componentsv2/pagination.md` |
| Empty content | `componentsv2/empty-state.md` |
| Loading | `componentsv2/loading-indicator.md` |
| Feedback | `componentsv2/alert.md`, `notification.md` |
| Confirmation | `componentsv2/modal.md` |
| Activity history | `componentsv2/activity-feeds.md` |

For Data Tables and other components, use the corresponding existing GEMS guideline if available.

### 9.2 Foundation Dependencies

All dashboard elements MUST follow:

- `Foundation/color.md`
- `Foundation/typography.md`
- `Foundation/spacing-dan-radius.md`
- `Foundation/effect-styles.md`
- `Foundation/icons.md`
- `Foundation/misc-icons.md`
- `Foundation/logo.md`
- `Foundation/design-annotations.md`

**Brand Rule:** Use GEMS Brand General. Never use Brand CCM.

### 9.3 Layout Rules

- Follow the selected GEMS Dashboard Style01, Style02, or Style03.
- Preserve spacing, alignment, card hierarchy, and responsive behavior.
- Group related metrics and visualizations logically.
- Use official GEMS layout and spacing tokens.
- Use shadows only where defined by relevant GEMS components.
- Maintain consistent chart and card placement across related dashboards.
- Keep the most important information easy to find.
- Do not introduce decorative content merely to fill the page.

### 9.4 Responsive Rules

- Use official responsive components and variants.
- Maintain readable data presentation.
- Adapt chart and table layouts according to supported patterns.
- Preserve access to important filters and actions.
- Do not manually reduce typography or spacing below GEMS specifications.
- Do not invent unsupported mobile navigation or component variants.

---

## 10. Reference Implementation — ISS Dashboards

ISS dashboards are approved contextual references for composition and practical usage.

They demonstrate combinations of official GEMS components, including:
- Page Header.
- Input Dropdown filters.
- Card Header.
- Charts.
- Data Tables.
- Pagination.
- Badge.
- Button Group and related actions.

### Usage Matrix

| Reference | Contextual Learning |
|---|---|
| ISS Sport | Operational metrics, filter composition, supporting charts, and data sections |
| ISS Mess — Visit | Visit-related metrics and reporting layout |
| ISS Mess — Accommodation | Accommodation monitoring and operational summaries |
| ISS Mess — Meals | Food-service management metrics and reporting |
| ISS Mess — Transport | Transportation operations and monitoring |
| ISS Mess — Laundry | Laundry operational reporting |
| ISS Registrasi Asset — HRGA | HRGA and asset-related analytical presentation |

### Reference Usage Rules

AI MUST:
- Study only examples relevant to the requested product.
- Identify useful relationships between KPI Cards, Filters, Charts, and Tables.
- Follow practical grouping and information hierarchy.
- Adapt the dashboard to the target product's approved metrics.
- Continue using official GEMS General components.

AI MUST NOT:
- Copy ISS business data into unrelated products.
- Assume ISS metrics are universal.
- Copy hidden or deprecated elements merely because they exist in a reference frame.
- Copy arbitrary local overrides from reference screens.
- Substitute an ISS-specific custom component for an official GEMS General component.
- Use CCM styling even if it appears within a reference.

**Priority Rule:** ISS references guide HOW dashboard content is organized. GEMS General determines HOW the UI must look.

---

## 11. Mandatory Dashboard States

Dashboard generation MUST account for relevant data and interaction conditions.

| State | Required Behavior |
|---|---|
| Default | Dashboard displays valid data |
| Loading | Official GEMS loading presentation |
| Empty Data | No available records |
| No Results | Filters or search produce no matching records |
| Error | Data retrieval or processing fails |
| Filter Applied | Dashboard reflects selected filters |
| Filter Reset | Dashboard returns to approved default conditions |
| Partial Data | Available information is displayed accurately while missing sections are distinguished |
| Restricted | User cannot access specific data or actions |

Additional Focus, Hover, Disabled, Selected, Success, or Confirmation states MUST follow the relevant component guidelines when applicable.

### Data-State Rules

AI MUST distinguish:
- `0`: Valid numerical zero.
- `null` / unavailable: Missing value.
- Empty dataset: No records.
- No Results: Records do not match active filters.
- Error: Data could not be retrieved.

AI MUST NOT:
- Display `0` for unknown values.
- Display Empty State while data is still loading.
- Treat failed API requests as empty datasets.
- Invent values to make the dashboard appear complete.
- Use custom loading or error designs when official GEMS components exist.

---

## 12. CRUD, Interaction & UX Patterns

Dashboards primarily support monitoring and decision-making. CRUD screens are included only when business requirements justify them.

### Create
- Add creation actions only when relevant.
- Use official GEMS Button, Form, Input, and Modal patterns.
- Follow role-based permissions.

### Read / Detail
- Provide drill-down or detail navigation when required.
- Maintain consistency between dashboard metrics and detail records.
- Use official GEMS Detail Page patterns.

### Update
- Include editing workflows only when approved.
- Use official form validation, confirmation, and feedback components.
- Do not make analytical charts directly editable without explicit requirements.

### Delete
- Display destructive actions only when permitted.
- Use official GEMS confirmation patterns when required.
- Do not delete records directly from dashboard visualizations without an approved flow.

### UX Flow Diagrams

For CRUD or multi-step interactions:
- Use the approved UX Pattern.
- Define entry, action, validation, confirmation, success, and failure.
- Include a UX Flow Diagram when the interaction complexity warrants it or the approved scope requires it.
- Place the diagram near the related Figma screens according to the agreed deliverable structure.
- Do not invent unsupported user journeys.

---

## 13. Human-in-the-Loop Execution Workflow

AI MUST complete the following phases in order.

### Phase 01 — Requirements & Data Analysis

Input:
- Target Figma file.
- HSD/BRD or direct requirements.
- Available datasets.
- User roles and permissions.
- Relevant product context.

AI MUST:
1. Understand the dashboard's primary purpose and users.
2. Identify confirmed KPIs, metrics, calculations, and data sources.
3. Separate confirmed requirements from recommendations and missing information.
4. Recommend appropriate KPI Cards, Charts, and Tables.
5. Identify required filters and available dashboard periods.
6. Determine whether the data supports the proposed visualizations.
7. Produce a concise **Dashboard Data Summary**.

**Dashboard Data Summary MUST include:**
- Dashboard objective.
- Target users.
- Confirmed and recommended KPIs.
- Calculations and data sources.
- Recommended visualizations.
- Proposed filters and periods.
- Missing business information, if any.

### HUMAN APPROVAL #1 — Data & Period Confirmation

Present the Data Summary and consolidate all unresolved questions into ONE confirmation.

Ask only what is missing, including:
- Which KPIs are approved?
- Which periods are required?
- What is the default period?
- Should periods use filters or separate dashboard views?
- Are any calculations or data definitions unresolved?

**STOP until Human Approval #1 is explicitly granted.**

Do not repeatedly ask questions already answered by HSD/BRD.

### Phase 02 — Dashboard Design Planning

After Approval #1, AI MUST:

1. Read only relevant GEMS guidelines.
2. Inspect the official GEMS Dashboard Style01, Style02, and Style03.
3. Exclude all CCM dashboard sections and components.
4. Review relevant ISS dashboard references.
5. Select the most suitable approved GEMS style.
6. Map KPIs, Charts, Tables, Filters, and Actions to official GEMS components.
7. Define information hierarchy and layout.
8. Define responsive behavior and necessary UI states.
9. Identify applicable CRUD and UX flows.
10. Produce a concise **Dashboard Design Plan**.

**Dashboard Design Plan MUST include:**
- Selected GEMS dashboard style and brief rationale.
- Page structure.
- KPI and component mapping.
- Chart types and analytical purpose.
- Filters and approved periods.
- Required interactions.
- Relevant UI states.
- Applicable CRUD and UX flows.

### HUMAN APPROVAL #2 — Design Plan Confirmation

Present the Dashboard Design Plan for review.

**STOP until Human Approval #2 is explicitly granted.**

Do not generate the dashboard before approval.

### Phase 03 — Figma Generation

After Approval #2, AI MUST:

1. Confirm access to the target Figma file and required permissions.
2. Generate the approved dashboard directly in the target file when supported.
3. Use official GEMS General component instances.
4. Follow the selected GEMS Style01, Style02, or Style03.
5. Apply the correct Foundation variables and styles.
6. Use approved KPIs, calculations, periods, and filters.
7. Include necessary loading, empty, error, and interaction states.
8. Generate applicable CRUD screens and UX flows according to scope.
9. Preserve unrelated existing designs.
10. Return the actual Figma link to the completed work.

If an operation is unavailable, explain the limitation and request direction before introducing an alternative.

Never claim the dashboard was generated unless the operation actually succeeded.

---

## 14. Strict Dashboard Rules

### MUST

- Use official GEMS General Design System.
- Use only approved GEMS Dashboard Style01, Style02, or Style03.
- Follow existing GEMS Foundation and Component Guidelines.
- Use accurate business data, metrics, and calculations.
- Select KPIs, Charts, and Tables according to analytical purpose.
- Use relevant GEMS Page Samples and UX Patterns.
- Treat ISS dashboards as contextual implementation references.
- Apply consistent filter dependencies and approved periods.
- Include relevant loading, empty, error, and interaction states.
- Follow role-based access and approved business workflows.
- Obtain both Human Approvals before Figma generation.
- Preserve the existing Figma component library references when supported.

### MUST NOT

- Use Dashboard CCM, CCM components, or CCM-specific styling.
- Use `Dashbord / CCM / Option 1`.
- Use `Horizontal tabs CCM` or any other CCM-specific variant.
- Use Brand CCM instead of Brand General.
- Copy CCM layout elements into a GEMS General dashboard.
- Invent additional dashboard styles or unsupported component variants.
- Hardcode colors, typography, spacing, radius, or effects outside GEMS.
- Create decorative charts or excessive KPI Cards.
- Invent data, calculations, targets, or trends.
- Copy ISS business content into unrelated products.
- Introduce unsupported actions or CRUD workflows.
- Ignore permissions or data availability.
- Skip Human Approval gates.
- Generate only a Default State when additional relevant states are required.
- Modify unrelated designs without authorization.
- Claim implementation success without verified results.

---

## 15. Official References

### 15.1 GEMS Design System

**Main Design System**
- [GEMS Design System](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System)

**Dashboard Styles — General Only**
- [GEMS Dashboard — Style01, Style02, Style03](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1170-3296)
- [Style01 — Dashboard Frame](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3471-32889)
- [Style02 — Dashboard Frame](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1230-40696)
- [Style03 — Dashboard Frame](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3475-11056)

**General Usage**
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1105-7310)

**Strictly Prohibited**
- GEMS Dashboard section `Dashbord / CCM / Option 1`
- All CCM components, variants, and styling.

### 15.2 ISS Sport Dashboard References

- [ISS Sport — Dashboard Reference 01](https://www.figma.com/design/lwE3dtJWGTILBz6uD0IoDt/ISS-Sport?node-id=1436-74082)
- [ISS Sport — Dashboard Reference 02](https://www.figma.com/design/lwE3dtJWGTILBz6uD0IoDt/ISS-Sport?node-id=1436-70842)

### 15.3 ISS Mess Management Dashboards

- [Visit Dashboard](https://www.figma.com/design/mN91DNF9bSz4H8CnXuXPW4/ISS-Mess-Mangement?node-id=1-52698)
- [Accommodation Dashboard](https://www.figma.com/design/mN91DNF9bSz4H8CnXuXPW4/ISS-Mess-Mangement?node-id=1-47965)
- [Meals Management Dashboard](https://www.figma.com/design/mN91DNF9bSz4H8CnXuXPW4/ISS-Mess-Mangement?node-id=8-41169)
- [Transport Dashboard](https://www.figma.com/design/mN91DNF9bSz4H8CnXuXPW4/ISS-Mess-Mangement?node-id=12-110535)
- [Laundry Dashboard](https://www.figma.com/design/mN91DNF9bSz4H8CnXuXPW4/ISS-Mess-Mangement?node-id=34-189539)

### 15.4 ISS Registrasi Asset

- [HRGA Dashboard — Available Data](https://www.figma.com/design/v3ggUUZOrTe6dh9wJ21Hcy/ISS-Registrasi-Asset?node-id=576-138623)

### 15.5 GEMS AI Repository

- [GEMS AI Design — GitHub](https://github.com/dgtuixexternal/GEMS-AI-Design)

Use existing repository guidelines under:
- `Foundation/`
- `componentsv2/`
- `ux-pattern.md/`

---

## 16. Final AI Instruction

**AI MUST generate dashboards using official GEMS General Design System components and one of the three approved dashboard styles: Style01, Style02, or Style03.**

Approved requirements determine WHAT the dashboard must communicate.

GEMS Component Guidelines determine WHICH components to use and HOW they behave.

Official GEMS Figma determines component instances, variants, and visual properties.

ISS dashboards provide contextual examples of practical implementation.

Human Approval determines WHEN the AI may proceed with design generation.

**Never use CCM designs, components, colors, variants, or styling under any circumstances.**

**Never force charts, KPI Cards, filters, or actions into a dashboard when they do not support the user's actual goals.**

**GEMS General Design System is the single source of truth for all dashboard visual specifications.**
